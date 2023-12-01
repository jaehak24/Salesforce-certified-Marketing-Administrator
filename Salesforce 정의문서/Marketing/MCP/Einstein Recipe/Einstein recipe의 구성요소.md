import requests
import os
import pandas as pd
from contants import BestOnTable as BT
from datetime import datetime, timedelta
from dateutil.relativedelta import relativedelta
import json
import subprocess
import logging
from logging.handlers import RotatingFileHandler
import time
import shutil

TAG = "[GP]"

base_url = "https://bestonmall.co.kr/api2/tableData"

currentDir = os.path.dirname(os.path.realpath(__file__))
saveDir = "C:\\Pentaho\Files\\beston"
logDir = "C:\\Utils\\BestOn_API\\log"
uploadLogDir = "C:\\Pentaho\Files\\beston\\log"

table_list_BO = [
  BT.ES_MEMBERHACKOUT.value,
  BT.ES_ORDER.value,
  BT.ES_ORDERGOODS.value,
  BT.ES_GOODS.value,
    
  BT.ES_CATEGORYGOODS.value,
  BT.ES_GOODSOPTION.value,
  BT.KM_STORE.value,
  BT.KM_STOREZONECODE.value,
  BT.ES_COUPON.value,
    
  BT.ES_COUPONOFFLINECODE.value,
  BT.ES_MEMBERCOUPON.value,
  BT.ES_ORDERCOUPON.value,
  BT.ES_CART.value,
  BT.ES_WISH.value,
    
  BT.ES_PLUSREVIEWARTICLE.value,
  BT.ES_DISPLAYTHEME.value,
  BT.ES_DISPLAYEVENTGROUPTHEME.value,
  BT.ES_TIMESALE.value,
  BT.ES_MEMBER.value,
]

current_idx = 0
log_file = 'BestonAPI.log'
# 에러발생시 재실행할 맥스 횟수 
retry_error_Limit = 3 
 
global is_error_exist
is_error_exist = False

def start():
   # global is_error_exist
    #is_error_exist = False
    retry_error = 0 
    total_page = 0
    try:
        for table in table_list_BO:
            start_time = datetime.now()
            df = pd.DataFrame()
            params = {
                'tableName': '',
                'page': 1,
                'date1': getParamDate(True,table),
                'date2': getParamDate(False,table),
                'dateKey': 'regDt'
            }
            # params = {
            #     'tableName': '',
            #     'page': 1,
            #     'date1': getParamDate(table),
            #     'date2': getParamDate(table)
            # }
            
            current_page = 1
            params['tableName'] = table
                
            print(f"{TAG} Starting : {table}_{params['dateKey']}")
            logger.debug(f"{TAG} Starting : {table}_{params['dateKey']}")
            
            while True:
                response = requests.get(base_url, params=params)
                
                try:
                    
                    parsed_data = response.json()
                    # 데이터를 제대로 불러왔으므로 에러카운트 초기화
                    retry_error = 0
                except ValueError:
                    print(f"{TAG} {table} error msg : {response.text}")
                    logger.debug(f"{TAG} {table} json형식 에러 : {response.text}")
                    retry_error +=1
                    time.sleep(3)
                    # 재시도 횟수 초과. 다음 100건으로 넘어감
                    if retry_error >= retry_error_Limit:
                        # 만약 테이블의 첫 100건 호출부터 에러라면 총페이지를 알수 없으므로 다음 테이블로 넘김
                        is_error_exist = True
                        if total_page <= current_page:
                            logger.debug(f"{TAG} {table} 재시도횟수 3회 발생. 다음 테이블 실행")
                            retry_error = 0
                            
                            
                            if len(df):
                                # 파일저장
                                df.to_csv(f"{saveDir}\{table}_{params['dateKey']}.csv", index=False, encoding="UTF-8")
                                end_time = datetime.now()
                                sec = (end_time - start_time)
                                logger.debug(f"{TAG} {table}_{params['dateKey']}.csv 파일생성 완료. 소요시간 : {sec}")
                            
                                # 등록일자, 수정일자별 파일이 1개씩 필요한 테이블들의 경우
                                if need_regDt_modDt(table=table) and params['dateKey'] == 'regDt':
                                    params['dateKey'] = 'modDt'
                                    df = pd.DataFrame()
                                    current_page = 1
                                    params['page'] = current_page
                                    continue
                            
                            break
                        # 재시도횟수 초과. 다음 100건 호출
                        else:
                            current_page += 1
                            params['page'] = current_page
                            logger.debug(f"{TAG} {table} 재시도횟수 3회 발생. 다음 100건 호출")
                            is_error_exist = True
                            retry_error = 0
                            continue
                    else:
                        logger.debug(f"{TAG} {table}  json형식 에러 발생. 재시도횟수 : {retry_error}")
                        
                        
                if retry_error == 0:
                    if not "error" in parsed_data:
                        total_page = parsed_data['page']['pageTotal']
                        print(f'{TAG} total_page : {total_page}, current_page : {current_page}')
                        # pageTotal이 0이면 데이터가 없다는 의미
                        if total_page == 0:
                            print(f'{TAG} data empty')
                            logger.debug(f'{TAG} Table : {table}, data empty')
                            df.to_csv(f"{saveDir}\{table}_{params['dateKey']}.csv", index=False, encoding="UTF-8")
                            end_time = datetime.now()
                            sec = (end_time - start_time)
                            logger.debug(f"{TAG} {table}_{params['dateKey']}.csv 빈 파일생성 완료. 소요시간 : {sec}")
                            
                            if need_regDt_modDt(table=table) and params['dateKey'] == 'regDt':
                                params['dateKey'] = 'modDt'
                                df = pd.DataFrame()
                                current_page = 1
                                params['page'] = current_page
                                continue
                            
                            break
                        
                        data_list = parsed_data['data']
                        
                        if table == BT.ES_MEMBER.value or table == BT.ES_ORDER.value:
                            # es_member 복호화 필드 : memNm, email, phone, cellPhone, birthDt
                            if table == BT.ES_MEMBER.value:
                                for item in data_list:
                                    memNm = item['memNm']
                                    memNm  = decrypt(memNm)
                                    item['memNm'] = memNm
                                    
                                    email = item['email']
                                    email  = decrypt(email)
                                    item['email'] = email
                                    
                                    phone = item['phone']
                                    phone  = decrypt(phone)
                                    item['phone'] = phone
                                    
                                    cellPhone = item['cellPhone']
                                    cellPhone  = decrypt(cellPhone)
                                    item['cellPhone'] = cellPhone
                                    
                                    birthDt = item['birthDt']
                                    birthDt  = decrypt(birthDt)
                                    item['birthDt'] = birthDt
                                    
                            # es_order 복호화 필드 : orderEmail, bankSender 
                            # CDP에서는 안쓰는 필드이므로 복호화 없이 공백 삽입                           
                            else:
                                for item in data_list:      
                                    item['orderEmail'] = ''
                                    item['bankSender'] = ''
                    
                        data_list = removeColumns(table, data_list)
                        
                        df_temp = pd.DataFrame(data_list)
                        df = pd.concat([df, df_temp], ignore_index=True)
                    
                        if total_page == current_page:
                            df.to_csv(f"{saveDir}\{table}_{params['dateKey']}.csv", index=False, encoding="UTF-8")
                            end_time = datetime.now()
                            sec = (end_time - start_time)
                            logger.debug(f"{TAG} {table}_{params['dateKey']}.csv 파일생성 완료. 소요시간 : {sec}")
                        
                            # 등록일자, 수정일자별 파일이 1개씩 필요한 테이블들의 경우
                            if need_regDt_modDt(table=table) and params['dateKey'] == 'regDt':
                                params['dateKey'] = 'modDt'
                                df = pd.DataFrame()
                                current_page = 1
                                params['page'] = current_page
                                continue
                            
                            break
                        else:
                            current_page += 1
                            params['page'] = current_page
                    else:
                        print(f"{TAG} {table} error msg : {parsed_data['error']}")
                        logger.debug(f"{TAG} {table} error msg : {parsed_data['error']}")
                        break
            
    except requests.exceptions.Timeout as errd:
        is_error_exist = True
        print(f'{TAG} Timeout Error : ', errd)
        logger.error(f'{TAG} Timeout Error : ', errd)
    except requests.exceptions.ConnectionError as errc:
        is_error_exist = True
        print(f'{TAG} Error Connecting : ', errc)
        logger.error(f'{TAG} Error Connecting : ', errc)
    except requests.exceptions.HTTPError as errb:
        is_error_exist = True
        print(f'{TAG} Http Error : ', errb)
        logger.error(f'{TAG} Http Error : ', errb)
    except UnicodeEncodeError as e:
        is_error_exist = True
        print(f'{TAG} UnicodeEncode Error : ', e)
        logger.error(f'{TAG} UnicodeEncode Error : ', e)
    except Exception as e:
        is_error_exist = True
        print(f'{TAG} Any Exception Error : ', e)
        logger.error(f'{TAG} Any Exception Error : ', e)

#암호화된 텍스트 복호화 
def decrypt(encrypted_text):
    # php코드에서 인코딩된 텍스트 복호화가 파이썬에서 안되어 php에서 복호화처리
    params = {
        'encrypted_str': encrypted_text,
    }   
    
    php_cmd = ['php', f'{currentDir}/decrypt.php', 'decrypt', json.dumps(params)]
    
    php_output = subprocess.check_output(php_cmd)
    decrypted_text = php_output.decode('utf-8').strip('null')        
    return decrypted_text


# CDI DB 스키마에 맞게 컬럼 제거
def removeColumns(table_name, data_list):
    if table_name == BT.ES_MEMBER.value:
         for item in data_list:
            del(item['loginLimit'])
    elif table_name == BT.ES_ORDER.value:
        for item in data_list:
            del(item['mileagePolicy'])
            del(item['couponPolicy'])
            del(item['pgTid'])
            del(item['pgSettleNm'])
            del(item['pgSettleCd'])
            del(item['checkoutData'])
    elif table_name == BT.ES_ORDERGOODS.value:
        for item in data_list:
            del(item['cateAllCd'])
            del(item['deliveryLog'])
            del(item['checkoutData'])
            del(item['sendSmsFl'])
            del(item['goodsDiscountInfo'])
            del(item['goodsMileageAddInfo'])
            del(item['invoiceNo']) #integer형인데 중간에 하이픈 들어오는 값이 넘어와서 DB에는 안넣음
    elif table_name == BT.ES_GOODS.value:
        for item in data_list:
            del(item['goodsMustInfo'])
            del(item['goodsDiscountGroupMemberInfo'])
            del(item['goodsDescription'])
            del(item['goodsDescriptionMobile'])
            del(item['goodsDescriptionSameFl'])
            del(item['externalVideoFl'])        
            del(item['externalVideoUrl'])        
            del(item['externalVideoWidth'])        
            del(item['externalVideoHeight'])
            
            goodsNm = item['goodsNm']
            goodsNm = goodsNm.replace('\xa0', ' ')
            item['goodsNm'] = goodsNm
    elif table_name == BT.ES_CATEGORYGOODS.value:
        for item in data_list:
            del(item['cateHtml1'])
            del(item['cateHtml2'])
            del(item['cateHtml3'])
            del(item['cateHtml1Mobile'])
            del(item['cateHtml2Mobile'])
            del(item['cateHtml3Mobile'])    
    elif table_name == BT.ES_DISPLAYTHEME.value:
        for item in data_list:        
            del(item['fixGoodsNo'])
            del(item['pcContents'])
            del(item['mobileContents'])
            
    return data_list

# 등록일자, 수정일자 둘다 필요한 테이블
def need_regDt_modDt(table):
    target_tables = [
        BT.ES_ORDER.value, BT.ES_COUPONOFFLINECODE.value, 
        BT.ES_MEMBERCOUPON.value, BT.ES_ORDERCOUPON.value,
        BT.ES_MEMBER.value
    ]
    if table in target_tables:
        return True
    else: 
        return False

# 파라미터에 들어갈 검색일자 구하는 함수
def getParamDate(date1, table_name):
    # 전체일자가 필요한 테이블
    all_date_tables = [BT.ES_MEMBERHACKOUT.value, BT.ES_GOODS.value,
                       BT.ES_CATEGORYGOODS.value, BT.KM_STORE.value, BT.KM_STOREZONECODE.value,
                       BT.ES_COUPON.value, BT.ES_DISPLAYTHEME.value,
                       BT.ES_DISPLAYEVENTGROUPTHEME.value, BT.ES_TIMESALE.value]

    # 1년치가 필요한 테이블
    year_date_tables = [BT.ES_CART.value, BT.ES_WISH.value]
    
    if table_name in all_date_tables:
        return '' #검색일자가 필요없으면 ''전달
    elif table_name in year_date_tables:
        if date1 is True:
            return getYearAgo()
        else:
            return getToday()
    else:
        return getToday()
        
                
# 오늘 날짜 yyyy-MM-dd
# 배치가 새벽에 실행되느라 실제는 어제 날짜임
def getToday():
    # today = datetime.today().strftime("%Y-%m-%d")  
    yesterday = datetime.today() - timedelta(days=1)
    yesterday_str = yesterday.strftime("%Y-%m-%d")
    return yesterday_str    

def getYearAgo():  
    yesterday = datetime.today() - timedelta(days=1)
    yearAgo = yesterday - timedelta(days=365)
    yearAgo_str = yearAgo.strftime("%Y-%m-%d")
    return yearAgo_str  

def getYesterDay():
    today = datetime.today()
    yesterday = today - timedelta(days=1)    
    return yesterday.strftime("%Y-%m-%d")


def isExistFile(name):
    if os.path.isfile(name):
        return True
    else:
        return False

def renameLog(logFile):
    yesterday = datetime.today() - timedelta(days=1)
    convert_yesterday = yesterday.strftime("%Y-%m-%d")
    try:
        os.rename(f'{logDir}\BestonAPI.log', f'{logDir}\BestonAPI_{convert_yesterday}.log')
    except Exception as e:
        print(f'{TAG} Any Exception Error : ', e)

def renameTodayLog(logFile):    
    today = datetime.today().strftime("%Y-%m-%d")  
    try:
        log = f'BestonAPI_{today}_Error.log' if is_error_exist is True else f'BestonAPI_{today}.log'
        print(f'{TAG} log : ', log)
        os.rename(logFile, f'{logDir}\{log}')
        shutil.copy(f'{logDir}\{log}', f'{uploadLogDir}\{log}') 
    except Exception as e:
        print(f'{TAG} Any Exception Error : ', e)


if __name__ == "__main__":
    # if isExistFile(log_file):
    #     renameLog('BestonAPI')
    
    logger = logging.getLogger()
    logger.setLevel(logging.DEBUG)
    formatter = logging.Formatter(u'%(asctime)s [%(levelname)s] %(message)s')
    log_max_size = 10 * 1024 * 1024  ## 10MB
    log_file_count = 20 
    rotatingFileHandler = RotatingFileHandler(
        filename=f'{logDir}\BestonAPI.log',
        maxBytes=log_max_size,
        backupCount=log_file_count,
        encoding='utf-8'
    )
    rotatingFileHandler.setFormatter(formatter)
    logger.addHandler(rotatingFileHandler)

    start_time = datetime.now()
    start()
    
    end_time = datetime.now()
    sec = (end_time - start_time)
    elapsed_time = sec
    print(f'{TAG} elapsedTime: {elapsed_time}')
    logger.debug(f'{TAG} [{getToday()}] BestonAPI 총 소요시간 : {elapsed_time}')
    rotatingFileHandler.close()
    logger.removeHandler(rotatingFileHandler)

    if isExistFile(f'{logDir}\BestonAPI.log'):
        renameTodayLog(f'{logDir}\BestonAPI.log')
   
        
         
    
