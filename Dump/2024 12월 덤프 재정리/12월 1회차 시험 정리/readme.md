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