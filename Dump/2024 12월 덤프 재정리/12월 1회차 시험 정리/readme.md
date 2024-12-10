# 1. What is the recommended security setting for session timeout?
마케팅 클라우드의 세션 타임아웃 설정으로 적절한 시간은?
> 20 mins

# 2. Which standard Marketing Cloud role creates and delivers messages through applicable channel apps?
> Marketing cloud content editor/publisher

# 3. Business units are used to …?
마케팅 클라우드의 BU(Business Unit)은 조직의 공간 내에서 데이터의 전송과
구조에 있어서 관리가 용이하다. 

# 4. Which deliverability best practice helps you build a positive sending reputation with ISPs?
> ISP 의 스팸 필터링에 걸리지 않기 위해서는 IP Warming이라는 작업을 통해서 발송 주체에 대한 '명성'을 유지해야 한다.

# 5. What Marketing Cloud feature can you use to view data from an individual send?
> 마케팅 클라우드 이메일 캠페인에 있어서 Tracking은 고객의 트리거, 발송결과, 여정에 대한 정보를 개인별로 전사한다.


# 6. What are some options for exporting reports?
> reports를 받는 방법에는 크게 2가지의 방법이 있는데 1번은 FRP를 통해 받을 수 있고 2번째는 FTP를 통해 받을 수 있다.

# 7. Which statement best describes a contact and a subscriber?
1. a contact is a person you are going to send messages to. A subscriber opted to receive communications or belongs to a particular channel.

2. a contact is a person who opts in to receive communication through a specified channel. A subscriber is anyone who sends you a message.

3. a contact us always a subscriber. a subscriber is always a contact.

4. a contact is a person who opts in to text messages. a subscriber is a person who opts in to email messages.

Contact는 발송을 한 전화번호부에 있는 사람이고 Subscriber는 발송을 하기로 동의 받은 주체를 말한다. 집합으로 보면 Contact가 모집합이고 Subscriber가 부분집합이라고 볼수 있다.


# 8. What is used by Salesforce to uniquely identify a contact throughout Marketing Cloud?
> answer is Contact ID

* 마케팅 전체에 대한 시스템 레코드로 작용할 수 있는 것은 Contact ID (마케팅 클라우드 사용자 입장에서는 보이지 않고, 시스템이 발급하는 번호)

* 마케팅 클라우드 내 사용자가 정의하는 고객 키를 Contact Key


# 9. What should you create to synchronize objects from Service Cloud, pull the information into Marketing Cloud, and share contact data with business units?
 >service cloud에서 마케팅 클라우드로 오브젝트를 연결하기 위해서는 Marketing cloud 내 data designer에서 service cloud 오브젝트의 각 field들을 정의해주고 contact 연결해주는 attribute group 설정을 진행한후에 오브젝트를 연결해주어야 한다.

 # 10. Which of the following are all reasons to know your Marketing Cloud instance? (choose 3)

 1. The instance is needed to configure the Web Collect URL, SOAP Web Services API and more.
 > 인스턴스는 web collect URL, SOAP web service API 등등의 API의 설정을 하기 위해서는 인스턴스 정보를 알아야 한다.

 2. The instance helps you use the release schedule to predict when new features are released to your account.
 3. The instance helps you monitor any performance concerns on the Salesforce Trust site.


# 11. Why is whitelisting the entire set of IP ranges for your region a best practice?

1. It ensures Salesforce login pools can process end users' login authentication when accessing Salesforce.

2. It avoids unintended service disruptions due to movement between primary and secondary instances.
> instance 이동에 있어서 이동시에도 문제가 없게 하기 위해 전 지역에 대한 ip 허용이 필요하다.


# Which of the following are true about All Contacts in Contact Builder? (choose 3)

1. All Contacts contain All Subscribers plus anything marked as a Population.

2. All Contacts function at the Enterprise/Parent level.

3. All Contacts function across all Channels in Marketing Cloud.


# 13. What Salesforce Editions work with Marketing Cloud Connect? (choose 3)
마케팅 클라우드가 세일즈포스와 인터페이스 하기 위해서는
다음과 같이 라이센스가 필요하다.
1. unlimited
2. Developer
3. Enterprise

# 14. Before you can enable marketers to include the Distributed Marketing content blocks in emails, you need to do two things?
마케터가 Marketing Cloud에 접속하기 위해서, 다음과 같은 절차를 진행해야 한다.
1. Add the Distributed Marketing installed package to your Marketing Cloud account.
> 마케팅 클라우드에서 Distributed Marketing 을 account(조직) 내에 설치해야한다.
2. Add the custom content blocks that you want to use as components.
> 마케터가 원하는 컨텐츠를 이메일에 첨부하기 위해서는, custom content block을 추가해야 한다.


# 15.What are potential risks of using Non-Scope by User Data Access configuration for Marketing Cloud Connect? (choose two)
> 고객에 대한 접근 권한 (scope)를 설정하지 않는다면 다음과 같은 문제가 발생할 수 있다.
1. Users may be able to view more records than they should have access to in CRM, creating a security risk.
> 마케팅 클라우드와 CRM의 권한 설정은 별도이므로 세일즈포스에서 정해진 권한보다도 더 많이 볼 수 있다.
2. A User may run a report displaying only records visible to them but containing additional records they don't see, causing a send to deploy to more contacts than intended.
> 마케터들이 보는 권한보다도 더 많은 레코드들이 인지되지 못한 채, 발송을 진행할 수 있기 때문에, 예상 했던것 보다 더 많은 수의 발송이 이루어질 수 있다.


# 16. Whitelist the following domains, if you have policies to whitelist only MC domains: (choose 3)?
1. Exacttarget.com
> Exacttarget.com 는 마케팅 클라우드의 메인 도메인이다. 언제나 whitelist에 포함되어야 하며, 모든 api, ftp, stream 등등의
인터페이스를 위해서 열어야 한다.

2. *.marketingcloudapps.com
> *.marketingcloudapps.com는 와일드 카드 도메인으로서, marketingcloudapps.com의 서브도메인을 
전부 커버한다. 마케팅 클라우드에서 제공하는 다양한 애플리캐이션의 도메인을 포함한다.

3. Bounce.exacttarget.com
> 이메일 바운스에 대한 도메인으로서, 이메일 바운스가 일어났을 때의 알림을 위해서 해당 
도메인에 대한 whitelist 처리는 진행해야 된다.

### 17.The Northern Trail Outfitters (NTO) marketing team is launching a new email campaign. NTO's Email Specialist wants to perform quality assurance checks on the email prior to send and has asked about using the Validate functionality for this effort. Which three items will Validate check in an email message
1. Each content area specified in a dynamic content rule exists.
> 다이나믹 룰이 적용된 이메일의 content area에 Validation이 검증을 진행한다.
검증 목록으로는 
 * 이메일의 구조와 맞게 area가 설정되어 있는지
 * 이메일의 내용과 컨텐츠가 일치하는지 여부를 판단한다.(맥락이 아닌 생김의 구조가)

2. Correct syntax is used on any AmpScript in the email's code.
> 이메일 코드에 AmpScript가 정확하게 기입되었는지 확인을 해준다.

3. Personalization strings map to attributes or data extension fields
> 개인화된 문자열들이 data extension의 맵핑되어 있는 records 들과 일치하는지 여부도 검증을 해준다.


## 18. A Marketing Cloud admin wants to maximize login security to ensure that data is protected. Which two settings are recommended?
> 마케팅 클라우드의 보안을 위한 권장 사항으로서는 다음과 같다.

1. The invalid logins before lockout set to 3 attempts.
> 로그인 실패 시도는 3번까지

2. The login expires after inactivity set to 90 Days.
> 로그인을 하지않은지 90일이 지나면 로그인 세션이 expire 되게 설정

## 19. Global Conveyors has a new business unit. What should Admin do before creating business units?
> 신규 BU(비즈니스 단위가 조직에 추가)가 추가된다면 data extension에 추가되는 것은 뒤에 작업해야 할 내용이고
>> 조직의 구조를 business unit에 맞게 조정해야 된다.
* Map your Organizational Structure for business unit


## 20. Northern Trail Outfitters wants to switch on the out-of-the-box audit trail functionality in the Marketing Cloud account, however they cannot see the option to enable it. What could be the likely cause?
> User is missing the marketing cloud administrator rights.
제품 내에 기능이 보이지 않는 기능에 대해서는 admin 권한이 필요하다.

# 21. What are the requirements for Distributed Marketing: (choose 3)?
1. Salesforce Marketing Cloud with Journey Builder
> 저니 빌더가 있어야 Distributed Marketing을 할 수 있다.
2. Salesforce Sales Cloud, Service Cloud, Financial Services Cloud (FSC), or Community Cloud (Partner Community License or Login, only)
> 고객에 대한 데이터를 제공해줄 Salesforce 다른 제품군이 필요하다.
3. Salesforce Connect with the ability to connect to one external data source
분산 마케팅에 속해 있는 모든 sales user는 마케팅 클라우드 라이센스가 포함된 계정을 가지고 있어야 한다.


# 22. Which account type merges an account with a contact in a single view?
1. Person Account
> contact는 마케팅 클라우드의 단일 고객에 대한 단위이다. person account는 이에 대한 통합된 계정을 보는 한 단위이다.


### 23. Northern Trail Outfitters (NTO) is adding Mobile Studio to its marketing tools. Currently, NTO uses Email Studio and Journey Builder to send email messages. They are using a unique alphanumeric as the Subscriber Key in Email Studio. What should the administrator do to prevent duplicates across all Marketing Cloud channels?
1. Use a single Contact Key value.
> 다른 채널과의 고객 충돌을 방지하기 위해서, 한 조직 내에 있는 마케팅 클라우드 내의 고객 contact key 또는 subscriber key를 통일 시키는 것이 좋다. 
>> Ex> moblestudio > subscriber key 123456 , mobile studio> contact key 123456


# 24. Which application serves as your real-time, direct line to understanding customer data?
1. Audience Builder

# 25. Global Conveyors wants to track impression by job report. Which two considerations Admin should keep in mind (Choose 2)?
1. Only emails that use dynamic content can be tracked using these reports.
2. Only emails that use AMPscript can be tracked using these reports.
> 잡 리포트를 통한 이메일 캠페인을 위한 이메일 구성 사항으로는 다음과 같이 2가지 방법으로 마케팅을 해야 한다.
* 이메일 안에 AMP Script가 있어야 한다.
* Dynamic content 존이 구성 되어 있어야 한다.

# 26. Choose the correct steps needed to apply administrative permissions for Marketing Cloud Connect: (choose two)?
1. Enable Marketing Cloud for AppExchange User and Marketing Cloud for AppExchange Admin for the Salesforce CRM Administrator User

2. Edit the CRM User Page Layout to add the Marketing Cloud for AppExchange User and Marketing Cloud for AppExchange Admin Fields


 # 27 Salesforce -> Marketing Cloud Connect
  CRM에서 마케팅 클라우드로 연결하기 위한 준비물은 다음과 같다.
  
  1. 라이센스
  > 필요한 라이센스는 각 제품별로 상이한데 다음과 같다. 
  * SalesCloud: Unlimited, Enterprise, Performance, Developer
  * Marketing Cloud: Core edition, Advanced edition, Agency edition, Enterprise 1.0 Lock and Publish. Enterprise 2.0 edition, Reseller edition, marketing Cloud sandbox


  # 28 Which IPs should be whitelisted when first configuring MC?
  마케팅 클라우드를 구축함에 있어서 IP 관리에 있어서 가장 먼저 해야 할 것은 현재 있는 지역에 대한 IP를 전부 허용 하는 것이다.
> Whitelist the entire set of IP ranges for your region.

# 29.Additional IP Whitelisting is required for the following when configuring MC Connect: (choose 3)?
IP 에 대한 화이트 리스트에 있어서 다음과 같이 부가적으로 작업을 진행해야 한다.
1. IP Addresses for Notification and Identity Validation Emails
> 밸리데이션 매일과 문제에 대한 알림을 주는 이메일에 대한 IP 화이트리스팅이 필요하다.
2. Global IP Whitelist Ranges for General MC Connect Functionality
> 마케팅 클라우드에 다른 제품을 연결하기 위해서 글로벌로 화이트 리스트를 열어두되 마케팅 클라우드 한정으로 오픈을 해야 하낟.

3. Set of specific ranges for MC Connect functionality
> 마케팅 클라우드의 기느을 위해 기능과 관련된 IP 허용을 해야 한다.

# Which field CANNOT be updated in Company Information?
> Account Name


## 30 Global Conveyors is determining the marketing cloud instance (MID). What can the admin do with this information?
MID 정보 (인스턴스 고유 ID)를 기반으로 admin은 API 정보를 정의할수 있다.
* web collect url은 무관하다.
* Marketing cloud connect URL은 MID와 무관하다.

# marketign cloud tennant types
1. Enterprise 2.0: A tennant is the top-level account and all associated business units
2. Enterprise: A tennant is the top-level account and associated On-your behalf or Lock & Publish business units 
3. Core: A tennant is a single account
4. Agency: Each top-level account and each associated client account is a seperate tenant.


## 31.Global Conveyors requested the Admin configure a spam filter to exempt certain email messages from being filtered or rejected. Which process should the Admin apply?
> Allow listing

## 32. When modifying the Lead/Contact Page Layouts in CRM for Marketing Cloud Connect, add: (choose 3)?
마케팅 클라우드를 세일즈 클라우드로 연결을 할때 
Sales Cloud permission set에서 다음과 같이 Contact page layout에 다음 3개의 field를 추가해야 한다.
1.  Individual Email Results
2. Lead/ Contact Actions
3. Email Sends


#  33. Northern Trail Outfitters' Marketing Cloud admin wants to ensure certain subscribers' opens and clicks are NOT tracked at their request, in accordance with the EU's General Data Protection Regulation. In which two ways should the administrator configure these settings? (Choose 2)
eu의 고객 행동 추적이 안되므로, 해당 고객에 대해서 선택을 해줘야 된다. 그러므로 답은 하단과 같다.

1. Enable the DoNotTrack Attribute on each Subscriber.
> EU에 속해 있는 고객에 대해서 만든 속성 DoNotTrack을 체크해 줘야 한다.
2. Create a Preference Attribute called DoNotTrack.
> EU에 속해 있는 고객에 대해서 DoNotTrack을 활성화 하기 위해 다음 이름으로 컬럼을 만들어줘야 한다.

# 34. A marketing team accidentally sends SMS campaigns intended for 4 p.m. at 4 a.m. They would like to use a Blackout Window to prevent this from happening again. Which two actions would a Blackout Window prevent? (Choose 2)

1. Sends manually initiated during the Blackout Window.
> 블랙아웃 기간에 수동으로 발송 하는 것에 대해서 방지가 된다.
2. Scheduling sends during the Blackout Window.
> 블랙아웃 기간 중 예약 발송된 건에 대해서 방지가 된다.


# 35. Northern Trail Outfitters enabled enhanced sender profile feature. The NTO admin wants to create personalized email sends to their customers using the names of specific customer service representatives. While the content of the send remains same across the email send, the marketer wants the From Name to appear different for each subscriber. What are next steps for email personalization?

틀림 1회

1. Create a workflow to update member status.
2. Create a sender profile that uses AMPscript to dynamically pull information from the subscriber attributes populated by Salesforce information.


# 36. Which statements are true about Marketing Cloud and Marketing Cloud Connect when using Non-Scope by User configuration? (choose 3)
non-scope by user란 말은 시스템 계정, 거의 어드민이다. 그렇기 때문에 퍼미션에서 거의 벗어난다고 볼 수 있다.

1. Within the Marketing Cloud, returned subscribers are not limited to what is visible to the user initiating the send.
> 보낸 사람 뿐만 아니라, 마케팅 클라우드 내에 있는 모든 subscribers 들을 볼수 있다.
2. Password policies are not in effect, making this configuration easy to maintain because passwords do not expire.
> 패스워드 설정에서 never expier를 선택한다면, 비밀번호 reset을 주기적으로 설정하지 않아도 된다.
3. An administrator can set up a user without entering a password.
> 연결하는 과정에 있어서 admin 즉 non-scope 유저는 비밀번호를 입력하지 않아도 된다.

# 37.Which send process can use Sender Profiles? (Choose 3)
1. Guided Sends
> Template을 사용하는 메일 발송 프로세스 
2. User Initiated Sends
> 사용자가 마케팅 클라우드를 사용해서 발송하는 메일 프로세스
3. Triggered sends
> 고객의 어떤 해동 또는 ,API 등등 외부의 작용으로 발송 하게되는 프로세스


# 38. Northern Trail Outfitters wants to drive additional online sales. They are interested in using Einstein to recommend similar items to customers during the checkout process. Which two terms would they add to their website to accomplish this?

1. Recommendation Code
> 아인슈타인 추천인 코드 관련 JS 코드
2. Email Conversion Code
> 고객의 행동, 움직임 등등과 관련된 JS 코드

# 39. An email marketing manager is planning to send a promotional email to one million subscribers. Which data structure should be used?
> Data extension

data extension을 활용하는것이 대용량 발송면에서 호환성이나, 사용 면에서 유용하다.

# 40. Setup Assistant provides information and resources for configuring a new Marketing Cloud account. Which two topics does Setup Assistant cover?
(choose 2)
보기 중 최우선 순위로 선택하여야 하는 것은 다음 2 옵션을 선택해야, 기본적인 마케팅 클라우드 운영이 가능하다.
1. Setting up data structure
2. Managing the Enhance SFTP 
> 인입 또는 reporting의 출력을 위해서는 SFTP에 대한 설정을 진행해야 한다.

# 41. Northern Trail Outfitters has Marketing Cloud users who need data extension View and Update permissions for campaigns related to B2C sales, but not any permissions for campaigns related to B2B sales. How should they accomplish this?
B2B 세일즈 팀과 B2C 세일즈 팀에 대한 권한 분리가 필요한데 해당 질문은 저니에 대한</br>
권한 분리가 필요하다. 그렇다면, 데이터에 대한 권한 분리가 필요하는데 이를 저니를 저장하는
폴더에 권한을 설정해서 분리가 가능하다.
> Create seperate folders and add permissions

#### 42 A customer has an eCommerce site and imports data into three data extensions daily: Orders, Order_Details, and Products. The data extensions contain the following information: - Orders: OrderId, CustomerID, OrderNumber, OrderDate, OrderTotal, GrandTotal - Order_Details: ProductId, OrderID, Qty, UnitPrice, ExtendedPrice, Discount - Products: ProductId, SKU, Name, Description, Cost, Price. Which two actions should be taken in Data Designer? ( choose 2)
Data designer의 데이터 릴레이션 정의에 대한 문제로, 틀린 이유는 제품과 제품 상세 페이지에 대해서 1대 1의 관계를 고려하지 못했기 때문이다.
결론부터 말하면 정답은
1. Create a one-to-one relationship between Order_Details and Products.
2. Create a one-to-many relationship between Orders and Order_Details.

> 자명하게도, '주문'과 '주문 상세'는 1대 다의 관계를 가져야 한다. 
주문에 대해서 '여러가지' 상세 정보가 표기 될 수 있기 때문에, 주문: 주문상세 는 1:다의 관계를 가진다.


> 주문상세와 제품은 주문상세가 여러가지 제품을 가질 수 있지만, 문제에서는 제품 ID 값을 field로 가지기에, 한 주문 코드에
여러 제품을 가질 수 있어, 주문상세와 제품은 1대 1에 관계를 자긴다.

# 43. Northern Trail Outfitters has five business units in their Marketing Cloud account. All business units should be configured to use the same SFTP directory. How should this setup be achieved?
> SFTP 보안에 관련된 문제이다. 문제에서는 NTO에 다섯개의 BU가 존재하고, 모든 BU가 한 SFTP 디렉토리를 공유하고 있다고 말하고 있다.
1. All child business units should have an individual SFTP user
> 각 BU에 대해 각자의 SFTP 사용자를 가지고 있어야 한다. 이는 각 데이터 전송에 대한 추적이 가능하고(각 SFTP 사용자에 대해)
파일의 전송 및 버전 관리에 용이하다. 또한 각, 사용자에 대한 권한 계층 관리를 할 수 있기도 하기 때문이다.

## 44.A Marketing Cloud admin is tasked with requesting Marketing Cloud Connect Multi-Org enablement. What consideration should be given to the preference profile centers for this integration?
1. Multi-org does not support the standard profile preference center for the business units.
> 복수의 org에 대한 BU의 표준 profile preference center에 대한 지원을 하지 않는다.
복수 오그에 대한 설정 및 권한 자체는 표준이 아니다. 표준 자체는 단일 BU의 데이터 이관에 따른 profile preference center  관리가 표준이다.

profile preference center 관리 자체는 마케팅 클라우드 email studio 내에서 이루어진다.

#### 45. A large retail company has selected Marketing Cloud and has asked to be fully migrated from their existing platform in three weeks. They have communicated the following: They currently have 3 million customers. They email customers twice a week with no known deliverability issues. Their contract includes one Sender Authentication Package (SAP). Which two responses articulate proper IP warming?(choose 2)
1. IP ramp-up takes four to six weeks to be able to fully send to all 3 million customers.
> IP ramp-up(ISP로부터 신뢰를 얻기 위한 작업)은 30~60일정도가 소요된다. (4~9주 정도)
2. IP ramp-up is important to establish a positive sender reputation.
> IP ramp-up 작업을 진행해야, ISP로부터 신뢰를 받고, 이메일 마케팅의 발송에 대해서, 스팸으로 처리되는 불상사로부터 벗어날 수 있다.

### 46. A customer will provide a single daily file on the Marketing Cloud SFTP at 3 AM and needs an alert if the file is not present on time. The file needs to be imported into a staging data extension, separated into two different data extensions. Which workflow should meet these requirements?
> 파일의 SFTP 인입에 대한 알림을 받기 위해선느 File Drop automation이 아닌 scheduled Automation을 진행해야 한다.


# 47. What functionality is contained in Journey Builder that does not exist in Automation Studio?
1. The ability to initiate triggers based on a customer's behavior or interaction with your brand
> 실시간성으로 처리되는 데이터에 한해서는 Automation


#### 47. A Marketing Cloud admin notices Individual Email Results are NOT being pushed back into Sales Cloud for a particular end user. The admin of Marketing Cloud Connect is functioning properly. What should the admin confirm about the data extension?
> The data extension is located in the Salesforce Data Extensions folder.
마케팅 클라우드 내에서 발송한 이메일 결과를 담는 데이터가 sales cloud로 데이터가 들어오지 않는 건에 대하여 어디를 점검해야 한다는 질문이다. 발송 결과에 대해서는 shared가 아닌 data extension 폴더에 해당 데이터를 저장한다. 



##### 48. Northern Trail Outfitters is setting up new hires on its instance of Marketing Cloud, which includes Email Studio, Mobile Connect, and Social Studio. One of the hires needs to manage the operations of all of the North American Business Units. What two roles, custom or standard, could be assigned to this user to meet the requirement? (choose 2)
1.  Marketing Cloud Administrator
2.  Marketing Cloud Regional or Local Administrator

 ### 49. A Marketing Cloud admin wants to configure a new keyword for an upcoming SMS campaign. After entering the desired keyword CELEBRATION, the admin notices the keyword is unavailable. What issue could the admin be facing?
 > Keyword is used within another business unit
 >> 마케팅 클라우드 내에 있는 키워드는 모든 BU를 통틀어서 유니크하다. 그렇기 때문에 다른 BU에서 사용하고 있다면 마케팅 클라우드 내에서 해당 키워드를 중복으로 생성할 수 없다.

 #### 50. NTO wants to use complex criteria to identify subscribers for a special promotional email. Especially they want to target subscribers who opened or engaged with an email within the last 30 days and live within 10 miles of an NTO store. What should NTO do to create this audience?

복잡한 데이터에 대한 필터 처리는 SQL 쿼리를 통해 처리해야 한다. data filter는 세일즈포스 가이드라인에 따르면 간단한 데이터 처리에 대한 갈림을 위해서 사용된다.
> SQL Queries

#### 51. What elements of CAN-SPAM should the Marketing Cloud admin ensure are present for each Commercial send?
> Business name and physical mailing address
>> CAN-SPAM(마케팅에 대한 규제) 규정을 지키기 위해서는 메일 발송에 있어서 연락이 가능한 수단이 적힌 회사 로고 내지는 이름이 있어야 하며, 이는 1번인 회사 이름과 연락처(이메일)이 이에 해당한다.

#### 52. A customer needs to link demographic information to its contact model in Contact Builder. What type of relationship should be used?
> 컨택트와 고객의 위치 정보는 일대다 관계로 맵핑되어야 한다.

One-to-Many Relationship

### 53. Northern Trail Outfitters (NTO) has the Discover Reporting Tool. Which two report types could help NTO drive their mobile adoption strategy? (choose 2)
1. Email Sending Performance Report
2. Email Performance by Device
> 이메일 performance report를 통해 전쳉의 bounce rate, ctr 등등을 확인하고 이 중 기기별 performance를 보면서 모바일 도입 전략 지원이 가능하다.


 

#### 54. Northern Trail Outfitters (NTO) hired a new Marketing Cloud admin, who was told all emails come from info@email.nto.com. The previous admin did not leave any documentation. Which aspects would confirm a Sender Authentication Package (SAP) has been set up on the account?
(choose 2)
SAP은 마케팅 클라우드의 이메일 마케팅에 있어서 발송인의 신원을 인증케 하는 패키지다. Sender Authentication Package. 영업 대표를 통해서 구매가 가능하며, 패키지 포함 목록으로는 
 * Domain
 * Branded link: 해당 회사의 URL을 회사의 도메인으로 변경해서, 일관된 고객 경험을 유지하게 한다.
 * Dedicated IP address: 회사의 IP 주소를 단일 주소로 고정케 한다.
 * Reply Mail Management (RMM): 이메일 답변에 대한 관리를 지원하게 해준다.


1. Cloudpages personalized URLs are served from cloud.email.nto.com
> SAP을 회사의 도메인이 고정된다. 클라우드 페이지의 트래킹 url의 도메인이 SAP에서 구입한 회사에 할당된 고정 도메인인지 확인을 해보면, SAP을 구매했는지 아닌지 구별이 가능하다.

2. The login page for Marketing Cloud Users is login.email.nto.com and is branded with NTO colors.
> 마케팅 클라우드 로그인 시, 계정의 뒤가 cloud.email.nto.com로 고정되고, 회사의 브랜드 로고 색으로 고정이 되어 있으면 이는 SAP을 구매한것이다.


### 55. A customer wants Sales Cloud users to create and send Marketing Cloud emails. Which two recommendations should the consultant make?
(choose 2)
1. The consultant should enable the Create Email feature on the user Profile in the Sales Cloud.
> 세일즈 클라우드 사용자가 이메일 생성 및 발송을 진행하기 위해서 기존에 존재하던 세일즈 클라우드 계정의 권한에서 '이메일 생성하기' 권한을 활성화 해야 한다.

#### 56. Northern Trail Outfitters uses Marketing Cloud Connect to leverage Sales Cloud data in their journeys. A user recently reported the data coming from Sales Cloud is NOT up to date. Where should the Marketing Cloud admin begin troubleshooting?

1. Contact Builder > Data Sources
2. Contact Builder > Synchronized Data Extensions

#### 57. A Marketing Cloud admin has scheduled a query on a daily basis. They notice the query sometimes fails to execute. How would the admin ensure a notification is received when the query fails?
> Add their Email Address in the automation Runtime Error or Skipped Run Notification Settings



#### 58. A Marketing Cloud admin is asked to append an Urchin Tracking Module (UTM) variable string to links in emails. What functionality would allow this?
> Web Analytics Connector

이메일의 UTM을 추가하는 것은 Web Analytic Connector에서 관리한다, + GA 4 UTM

#### 59. A Marketing Cloud Administrator noticed a File Drop Automation has been failing on the Import File activity. The automation is configured with a filename pattern, so the filename is expected to begin with customer import. The import is configured to look for a file named Customer import %%Year%%%% Month%%%%Day%%.csv, however, the admin notices the filenames Include seconds and milliseconds what should the admin do to fix the issue?
초와 밀리세컨즈가 포함된 파일이더라도 파일을 임포트하기 위해서는 시간 형식으로 파일을 받기 보다는 import file activity로 설정해야 이름에 초나 밀리세컨즈로 해도 파일을 받을 수 있다.
> Use %%FILENAME_FROM_TRIGGER%% in the Import File Activity



### 60. Northern Trail Outfitters has noticed an issue with their sends today. Which two links in Setup Home could be used to troubleshoot the issue? (choose 2)
1. System Status
> 세일즈포스의 실시간 서비스를 모니터링할 수 있는 링크다.

2. Failed Sends
> MC에 있는 이메일 발송 중 미발송 건에 대한 로깅을 할 수 있는 링크다.


### 61. When customers use the Marketing Cloud default Profile Center link to unsubscribe, it causes users to not receive emails from any other business unit. What could explain this behavior?
> The Business Unit Unsubscribe Settings is set to Subscribers will be unsubscribed from all business units in the Enterprise

MC의 profile center의 기능 중 하나로 [Subscribers will be unsubscribed from all business units in the Enterprise] 라는 기능이 존재해
BU subscriber setting에서 고객을 Enterprise에서 구독을 해제할 수 있다.

### 62. Northern Trail Outfitters (NTO) only has enough licenses for their staff. A campaign manager is out on parental leave. How should NTO create a new user to fill in?
> <b>Disable</b> the campaign manager's user and create a new user


#### 63. When setting up a Send Log data extension for long-term success in Salesforce Marketing Cloud, Northern Trail Outfitters should consider the following three key factors
1. Add custom fields not included in the Send Log Template
> amp 스크립트 또는 Personalization string과 같은 데이터들은 template에 없는 데이터들로 분석과, auditing(회사의 마케팅 평가) 
2. Log attribute data necessary for auditing communication
> auditing을 위해서 subscriber key, emailAddresses, relevant metadata등등을 로깅해야 한다.
3. Apply an appropriately-scoped Data Retention period
> data extension에 대해서 너무 많이 쌓인 데이터에 대해서는 retention이 가해여쟈 하기에 적절한 retention 셋팅이 필요하다.


#### 64. A Marketing Cloud admin wants to create a suppression list for hard-bounced email addresses Where could the details be found?
> Query the Bounce Data View

마케팅 클라우드 내에는 bounce 되어 있는 


#### 65. Northern Trail Outfitters wants to segment audiences based on Sales Cloud data. Where would their Marketing Cloud admin configure Sales Cloud Objects to be synced and leveraged in Marketing Cloud?
> Contact Builder > Data Sources

세일즈 클라우드 데이터 중 일부를 세그먼트해서 sync 하기 위해서는 Data sources에서 atrribute를 정의함에 따라 진행할 수 있다.

### 66. How are publication lists used in the Marketing Cloud?
> To allow subscribers to opt-down/out instead of unsubscribing from all.

publication list는 고객의 구독을 관리하는 링크다.

##### 67. While setting up Marketing Cloud Connect, a Marketing Cloud admin navigates to the Marketing Cloud tab in Sales Cloud to complete the integration. The admin then receives the following error message: - Insufficient User Permissions. You have not been designated as an integrated Marketing Cloud user. Contact your system administrator. The admin notices the Marketing Cloud for AppExchange Admin option is selected when looking at the user settings. What action should correct the issue?
> Apply the Marketing Cloud for AppExchange User option as well

'Insufficient User Permissions. You have not been designated as an integrated Marketing Cloud user' 다음과 같은 에러가 나오는 이유는, 마케팅 클라우드 어드민 권한은 있지만 app exchange에 대한 권한이 없기 때문에 나오는 에러이다.

### Business Units are available in which tenant type?
1. Enterprise 1.0
>  Publish or On-Your-Behalf Business Units. 과 같은 BU를 지원한다.
2. Enterprise 2.0
> 모든 BU 권한이 가능하며, 자녀 부모 같은 상속 관계도 가능하다.


### A _______ in Contact Builder provides a single view of a customer and displays all their interactions with your brand?
> contact record


### A contact is managed and related through the different channels using a single _____. This is a unique identifier that you assign to a contact?
> Contact Key


## What is used by Salesforce to uniquely identify a contact throughout Marketing Cloud?
> Contact ID


## _________ are used to categorize distinct subgroups of contacts?
> Populations 

###  Which type of data source connects two different contact data tables to each other based on a particular field?
> Attribute Group


### 68. By default, the data extension retention policy deletes unused data extensions after how long?
> 6 months

사용하지 않는 DE는 <b>6개월 뒤</b>에 지워진다.

# 69. Which of the following statements applies to retention settings?
> You cannot remove the configured data retention settings once you configure them.

## 70. What do you use to synchronize Sales Cloud and Service Cloud data with Marketing Cloud?
> Marketing Cloud Connect

## 71. What should you create to synchronize objects from Service Cloud, pull the information into Marketing Cloud, and share contact data with business units?
> Create a synchronized data extension.

## 72. What value do you need to review the status of a Contact Delete request?
> Operation ID

contact delete에 대한 요청에 대해서 확인을 하기 위해서는 해당 작업에 대한 operation ID 가 필요하다.

## Where do contact deletions take place in Enterprise 2.0 accounts?
> Top-level accounts and all business units in the specified Enterprise 2.0 account.


## A ______ is a collection of components and applications that makes the connection between your Salesforce CRM and Marketing Cloud accounts work?
> Managed Package


# Before installing the managed package, what CRM feature needs to be enabled?
> Record types on the Contact and Lead objects

# Where do you integrate Marketing Cloud Connect users?
> Marketing Cloud Setup

## A person in this role assigns Marketing Cloud roles to users and manages channels, apps, and tools?
> Marketing Cloud Administrator


## A person in this role views cross-channel marketing activity that results in the Marketing Cloud?
> Marketing Cloud Viewer

# Marketing Cloud allows up to _______ FTP users per MID?
> 10

# _____________________________ store information about individual people by combining certain account and contact fields into a single record?
> Person Account


#### 73. Northern Trail Outfitters (NTO) has a franchise model which allows locally-owned stores to operate under the corporate umbrella. They are required by corporate policy to email each franchisee a monthly statement, but the statement cannot be publicly accessible. Which Marketing Cloud product should NTO purchase as a solution?
> Distributed Sending


#### 74. Set up or edit the tracking parameters that are appended to the links in messages sent from your Salesforce Marketing Cloud account using?
> Parameter Manager


#### 75. Northern Trail Outfitters (NTO) wants to limit who can receive Marketing Cloud tracking data via email from their Account to any email associated with their domain (ntoretail.com). Which steps should be taken to implement this? (Choose 2)
1. Enforce Export Email Allowlist
2. Add a Domain to the Export Email Allowlist


### 76. Use ________________________________ to copy the design of a journey, data extension, attribute group in the contact data model, or automation, and deploy it to other Marketing Cloud business units or enterprises?
> Deploy management


### 77. NTO wants to format links for consumption by Google Analytics 360. NTO wants to make sure they do not have any data which could be considered Personally Identifiable information (PII) within their links. Which three values could be used as personalization strings in query string parameters?(choose 3)
1. Subscriber ID
2. Product Code
3. Application ID


 이메일과 이름은 GA 정책에 어긋난다.

 # 78. Where in Setup can you edit email Headers & Footers?
 > Account setting

 #### 79. A Marketing Cloud admin is configuring the Marketing Cloud data model for the first time. They are using Journey Builder to send messages to customers, based on if there has been an order or not. There are two existing data model, Customers and Orders: - Customers contain information about subscribers including Email Address, First Name, Last name. - Orders contains information about the orders and include the unique identifier of the customer. In which two ways should the admin configure Data Designer to allow this data to be used within a Journey?(choose 2)
 1. Link the Orders data extension to the Customers data extension using a One-to-Many relationship
 2. Link the Customers data extension to the data model using the Customer ID


# 80.Which is NOT a Data Retention delete option?
> Data extensions



# 81. A customer is interested in designing a solution to ensure that subscribers only receive categories of emails that they want to receive. The built-in subscription center will be used as part of the solution. Which feature should be utilized to make this happen?

> Publication center

메일에 대한 발송 처리에 있어서 고객이 원하는 목록에 따른 발송을 하기 위해서는, publication center를 통한 설정으로 고객이 원하는 취향에 따라 발송이 되게 설정한다.



# 82. Which of the following statements applies to retention settings?
> You cannot remove the configured data retention settings once you configure them.