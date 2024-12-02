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