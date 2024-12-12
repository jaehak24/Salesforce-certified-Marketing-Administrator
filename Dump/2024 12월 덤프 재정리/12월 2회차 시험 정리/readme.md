#### 1. Northern Trail Outfitters (NTO) is building a journey which randomly sends five different versions of an initial welcome email to new subscriber however, subscribers receive the same follow-up email two weeks later. To improve the maintainability of their email content, NTO wants to use 3 completely different emails, rather than having one email with dynamic content. Which activity would allow NTO to build the journey with the fewest activities possible?
> Join


# 2. Where would a Marketing Cloud admin view all verified email addresses?
> From address management

확인된 이메일에 대한 리스트를 보고 싶으면 Address management에서 확인할 수 있다.



### 3. A user asks a Marketing Cloud admin to update and increase their session timeout setting. Which three considerations should the admin review before making this update?(choose 3)
1. Change impacts all users
> 해당 변경사항은 모든 사용자에게 해당된다.

2. Security risk of unauthorized users for longer timeout settings
> 요구사항에 따라 무조건 길게 하면, 보안에 대한 취약성이 생길 수 있다는 것을 공지해야 한다.

3. Typical length of time users spend in Marketing Cloud
> 요구사항과 보안의 중간점을 찾기 위해 고객들의 접속시간 유형을 파악할 필요가 있다.

# 4. When it comes to IP Warming, what is the best segment strategy in order to ramp up your email sends?
> Separate sends by those who have opened an email in the last 30-days


## 5. A marketer wants to add a customer survey to an email, but doesn't want the customer to have to leave the email in order to take it. What tool should the marketer use?

> Email Forms

이메일 수신 화면에서 나오지 않고 서베이를 하기 위한 방법으로는 이메일에 email forms를 추가하면 된다.

## 6.When adding a new FTP account user, what is the username default?

> The MID number of the current Marketing Cloud MID

ftp 고객 계정 추가 시, 디폴트로는 마케팅 클라우드 MID가 유저네임으로 기입된다. 

## 7. How do you change the link(s) in an email that has already been sent out?

> My Tracking > Job Links tab

이미 발송된 이메일 건의 링크 변경에 대해서는 My tracking > Job Link tab을 통해 변경이 가능하다.

### Marketing Cloud Connect only recognizes subscribers that use the______________________ /_______________________ as their subscriber key in Marketing Cloud?

1. Contact ID
2. Lead ID

> 세일즈 클라우드에 대한 건이므로 subscriber key로 인식하는 것은 lead id, contact id만 가능하다.

### 9. Set the Enforce Password History value to at least _____ as a best practice?
> 8

비밀번호 자릿수에 대한 최소한의 숫자는 8이다.


### 10. Basic Audit Trail is available to all Marketing Cloud customers via Automation Studio data extracts and API and has a ____________ retention period?

> 30-day

 Basic Audit Trail에 대한 설정을 기본으로 설정 시, 30 일이 나온다.

 #### 11. Advanced Audit Trail is available via Automation Studio data extracts and API, and has a __________ retention period?
 > 60-day
 
 Basic Audit Trail에 대한 설정을 기본으로 설정 시, 60 일이 나온다.


 ## 12. Which report would you use to know the total send and response data for your account?
 > Account Send Summary


 ## 13. You are trying to delete contacts from MC account using Contact Builder UI, but cannot see the DE that you wanted to use for deletion. What could be the reason?
 > DE 가 sendable로 표시되어 있지 암ㅎ으면, contact builder UI를 통해 해당 DE에 포함된 contact를 삭제할 수 없다.


 ## 14. Which three (3) users need to be setup when enabling MC Connect?
 1. API User
 2. System User
 3. MC Connect User

 ## 15. What is the maximum number of attributes that can be used in a single Data Extension in Marketing Cloud?
 > There is no limit

 ## 16. Which of the following is NOT a type of data view in Marketing Cloud?
 > Send 
 click, bounce, open은 있으나 send에 대한 data view는 MC에 존재하지 않는다.



 #### 17. California Craft Supply (CCS) recently moved from a small email marketing platform to Marketing Cloud and has been pitched Marketing Cloud Einstein Engagement Scoring by an implementation partner. CSS has a Pro Edition Marketing Cloud Account. What are some considerations before utilizing Einstein Engagement Scoring? (Choose three.)
 1. Einstein Engagement Scoring is included with Corporate and Enterprise Editions, and is available as an add-on purchase to Pro Edition
> pro edition이라면 부가 옵션으로 구매가 가능하다. STO는 enterprise 또는 corporate 계약에서만 가능하다.

 2. Einstein Engagement Scoring can take up to 90 days to generate initial scores
> STO가 점수를 정확히 매기기 위해서는 90일이 필요하다.

 3. Einstein Engagement Scoring does not work with custom unsubscribe handling
 > 커스텀으로 unsubscribe handling에 대해서는 작동하지 않는다.


 #### 18. A Marketing Cloud admin is assigning roles and permissions for both upper-management and entry-level team members. What should the admin keep in mind while assigning roles? (Choose two.)

 1. Marketing Cloud honors the most restrictive permission

 2. If there is neither Allow nor Deny permission, the user will not be able to use feature


 #### 19. A Marketing Cloud admin is configuring Social Studio to manage social media accounts. Which two prerequisites for configuring Social Studio should the admin consider? (Choose two.)

 1. Login details for each social media account

 2. Facebook ad manager



 #### 20. Northern Trail Outfitters wants to know how customers are engaging with marketing communications they have sent over the last year. What action should be taken to populate the Einstein Engagement Scoring Dashboard?
  STO를 통한 대시보드 활성화를 위해서는 각 채널에서 집행을 해야 한다.

> Select the channels (Emails, Push, SMS) to report on then click Activate


#### 21. ABC Company has a requirement to create a distinction between marketing and transactional emails in terms of From Name and IP Address for reputation purposes. Which two actions should ABC Company take in order to create Send Classifications?

1. Define a Delivery Profile.

2. Define a Sender Profile.

> transactional main과 마케팅 발송에 대한 분리(IP와 명성)을 위해서는 dellivery profile 과 sender profile을 수정해야 한다.


#### 22. A restaurant supply company captures email subscribers and leads through trade shows. They hold a giveaway at each trade show to entice booth visitors to leave their contact information. In the past, they have used a fishbowl to capture business cards, but need to update this to an online sweepstakes entry vehicle displayed on a mounted tablet. Individuals should only be allowed to enter once, and the winner will be selected randomly. All entrants receive a follow-up email after the trade show asking them to confirm their opt-in for a monthly newsletter. Which two components are appropriate for this solution? (Choose two.)

1. Data Extension with double opt-in status defined.

2. Microsite with Smart Capture to store entrants on a data extension.


#### 23. ABC Company needs to reduce the amount of work when managing messages to customers, but cannot add any more personnel due to budget constraints. There has been an increased number of customer purchases on their website, and the team currently sends batch order confirmations. What solution will decrease manual workloads on the team and will improve their customers experience?
> A triggered message to send an email as soon as a customer completes a purchase.

미션 자체가 고객의 구매에 대한 경험을 증가하고, 발송을 일배치로 보내고 있는 상황이기 때문에,
이에 대해서는 triggered message를 활용해서 고객이 구매한 순간 이메일을 발송하는 것이 좋다.


#### 24. Northern Trail Outfitters’ employees are NOT receiving emails because the messages are being blocked by Spam filters. How could the Marketing Cloud admin address this issue?
> Provide the IT team a list of relevant IP Addresses to whitelist in their spam filter

IT 팀에 대해서, 직원 IP를 제공해줌으로써 해당 목록을 ip whitelist에 추가해야 한다.

#### 25. What are two possible outcomes when "Send as Multipart MIME" is selected during the send process?

1. Open and click activity are tracked in either version.

2. An auto-generated text version will be sent with your HTML email.

#### 26. Marketing Cloud user needs the email addresses of everyone who unsubscribed from a particular email send. This user does not know SQL and does not have access to the enhanced FTP account. What functionality should be used to retrieve the necessary data?

> My Tracking

SQL 이나 FTP를 통한 파일 주고 받음을 모르는 사용자는 발송 건중 구독을 취소한 고객의 목록을 구하긴 위해서는
My tracking을 사용한다.


#### 27. By which three standard methods could contacts be injected into a journey? ( choose 3 )
1. Sales/Service Cloud Event
2. Date-Based Event
3. CloudPages Form Submit Event


#### 28.A customer with limited technical resources has requested assistance in setting up a small email deployment that the customer will maintain long term. The email will display men’s shoes to males in the audience and women’s shoes to females in the audience. The sendable data extension contains a field with a value of Male or Female. Which method should a consultant recommended to ensure content is displayed properly within the email?
>dynamic content Wizard

Contacts의 필드에 따른 컨텐츠를 보여주는 거에 있어서는 Amp script를 사용하는 
것은 특정 데이터를 보여주는 것은 가능하지만, 이미지나 컨텐츠에 있어서는 dynamic content Wizard
가 필요하다.


#### 29. A customer wants to automate the send of a monthly promotional email. The customer will upload an audience file to their accounts Enhanced FTP on a monthly basis on the 15th day of each month, expecting the email to be deployed upon completion of the import activity. However, if the 15th of the month falls on a Saturday or Sunday, the customer will provide the file on the Friday prior to the 15th and expect the promotional email to be sent on that Friday. Given the customer's requirements, which method should be used to automate their monthly promotional email?
> Create a file drop automation which includes an Import File Activity and Send Email Activity.


#### 30.Northern Trail Outfitters is concerned with their sender reputation and needs consistent visibility into subscribers who report their email as spam. How should they determine which subscribers reported their email as spam so they can flag those records in their customer service database?
> An automation that queries the Complaint data view.

#### 31. A Marketing Cloud admin at Northern Trail Outfitters is exploring whether they need to separate their brands into separate business units. When should the admin create separate business units for each of NTO's brands?
> Brand-specific private domains need to be leveraged when wrapping images and links in email campaigns


#### 32. Northern Trail Outfitters (NTO) has expanded its marketing efforts globally and wants to implement a dedicated Sender Authentication Package. They plan to share it across each of their Marketing Cloud accounts (three accounts total). Which two considerations would help NTO determine if a Dedicated IP is the right choice? (Choose two.)
1. All of NTO’s accounts should be on the same stack
> NTO의 계정이 한 stack에 있어야 해당 IP에 대한 SAP적용이 가능하다.

2. Send volume is large enough to maintain a positive or neutral reputation
> IP 에 대한 Warming은 발송량이 좌지우지 하기때문에, 많은 양의 발송이 필요하다.


## 33. Which are the three components of Send Classifications? (Choose three.)
1. CAN Spam
2. Delivery Profile
3. Sender Profile

#### 34.The customer wants to refresh a data extension each morning by importing a CSV containing today’s date and product information. Both the date and product catalog are never the same as products can be added and removed. What import type should be used?
> Overwrite


#### 35. A user wants their Marketing Cloud Administrator to configure Send Blockouts in MobileConnect to ensure subscribers are not receiving messages in the middle of the night. What are two elements to remember when configuring Send Blockouts? (Choose two.)
1. Sends do not pause at the Send Blockout time
2. Send Blockout is based on the time zone of your Marketing Cloud account

#### 36. Northern Trail Outfitters (NTO) has decided to use Journey Builder to launch event-driven lifecycle marketing programs. These programs include personalized interactions with customers with the primary goal to increase purchase frequency. Which two pieces of customer information would help NTO achieve this objective? (Choose two.)
1. Last purchase date
2. Channel preference of customers


### 37. A new Marketing Cloud admin is tasked with creating a new FTP user. Where should the admin navigate to create the new user?
> Setup > Users


#### 38. Which 2 statements are correct about Data Designer?
1. Data extensions can be linked to either the contact record or different data extensions, including data extensions from other attribute groups.

2. Data extensions should be linked directly to the contact record prior to being linked to different data extensions.


#### 39. A large retail group consists of a corporate team and several divisions operating under different brand names. All plan to share one Marketing Cloud account. Each brand has its own marketing department and operates independently, with its own creative assets, subscribers, and data structure. What are the two reasons why the recommended account configuration is one corporate Parent account, with each brand configured as a separate child Business Unit? (Choose two.)
1. Subscribers can be maintained at the Business Unit level.
2. Brands can set their own physical address and SAP


#### 40. Which three statements should be considered before using Goals in Journey Builder? (Choose three.)
1. Goals are created to evaluate journey performance.
2. Contacts are evaluated against the goal after a wait activity.
3. Goals can act as exit criteria.


#### 41. NTO is having issues with their automations being skipped. How can you attempt to mitigate skipped runs in Automation Studio? (Choose two.)
1. Optimize the automation's schedule
>시간이 겹침에 따라 오토메이션이 스킵 될 수 있다. 그렇기에, 일정을 최적화 함에 따라 최소화 할 수 있다.

2. Optimise the number of steps in the automation
> 절차가 많음에 따라, 오토메이션이 길어져서 스킵이 될 수 있다. 단계를 최소화 하는 것도 방법이다.

#### 42.A user has stated that a file will be dropped in an FTP location and they will need a new directory created. Where do you navigate to create a new file location for the directory?
> Email Studio > Admin > Data Management

#### 43.Northern Trail Outfitters placed an encrypted file on their Marketing Cloud SFTP for import into a data extension. They are using a File Transfer Activity to decrypt the file. Where would the decrypted file be after the File Transfer Activity completes?
> Safehouse


#### 44. A customer needs to import data from an SFTP site. The customer has a few requirements: 1. Segment the contents of the file and then send emails. 2. Transfer the file to the SFTP site at various times daily. 3. Send to data extensions. What sequence of automation activities should meet these requirements?
> Scheduled Automation: Transfer File > Import File > SQL Query(s) > Send Email(s)
 

#### 45. Which statements regarding Commercial Sends and CAN-SPAM requirements are not true? (Choose two.)
1. Require a subscriber to log in or visit a second page to unsubscribe

>세컨드 페이지가 아닌 기존의 사이트에서 로그인에서 취소할 수 있게 해야 한다.

2. Process unsubscribes within 15 days.
> 15일이 아닌 10일안에 취소를 할 수 있게 처리해야 한다.

#### 46. Northern Trail Outfitters wants to import subscriber data from its data warehouse into Marketing Cloud. Which 2 fields would need minimal consideration, for scalability and size related reasons, when creating a data extension to house the data? (Choose two.)
1. number
2. text
3. Boolean
4. Decimal

> 데이터 고려시, 가장 사이즈가 작은것은 우측의 2개의 자료형 number, Boolean 이다.


#### 47. Northern Trail Outfitters (NTO) experienced a 24-hour website outage during a peak shopping day. During the outage, a number of logged-in customers' shopping sessions were disrupted. When the site is back online, the retailer would like to encourage those shoppers to return to the site and continue their shopping. What action should NTO take?
>Import a file of logged-in customers into NTO's existing Abandoned Cart journey in Journey Builder.

#### 48. Northern Trail Outfitters (NTO) assigns a 15-digit integer as their Order ID which will be used as the primary key of a data extension. The import file contains leading zeroes, but NTO does not want to include them in the final values. Which data type should they use for the Order ID field? Decimal (15,0)
> Number


#### 49. File Transfer > File Transfer > Import File > SQL Query > Wait > Send Email > SQL Query > File Transfer
> File Transfer > Import File > Filter > Wait > Send Email > Wait > SQL Query > Data Extract > File Transfer

#### 50. A marketing team needs to export specific send data from their account on a weekly basis. The data will need to be encrypted and generated with specific column names to allow for a direct import into a third-party analytics system. Which method should be used to pull the data from Marketing Cloud?

> Tracking Data Extract



#### 51. The Footwear Division of Northern Trail Outfitters (NTO) is moving to Marketing Cloud and will be using NTO's existing Marketing Cloud account. The Footwear Division team has asked for a recommendation on whether they should have a separate business unit within the existing account. Which consideration warrants the creation of a separate business unit for the Footwear Division’s instance of Marketing Cloud?

> Managing Unsubscribes for the Footwear Division only

Footwear에서 NTO의 마케팅 클라우드를 사용하면서 관리해야 할 것은 구독취소 고객들에 대한 관리를 별도로 관리해야 한다.
Footwear의 unsubscribe 고객들을 가져오든 NTO와 분리 관리를 할 필요가 있다.


#### 52.  Northern Trail Outfitters (NTO) uses data extensions to house all of their email audiences. A customer reports they unsubscribed several weeks ago but continues to receive NTO's daily emails at their old address. NTO's Marketing Cloud Admin has deleted them from the appropriate data extension. What consideration could account for this behavior?

> The email address in All Subscribers is prioritized


#### 53. Northern Trail Outfitters (NTO) keeps their subscribers in sync with their external database via the import of a CSV file which is dropped to the Marketing Cloud SFTP each day. However, NTO has realised the number of subscribers being sent emails is considerably lower than the number they were expecting based on records in their database. Which feature would allow NTO to monitor whether all records were added to the target data structure each day?
> Notification Settings within the Import File Activity



#### 54. While setting up Marketing Cloud Connect, a Marketing Cloud admin navigates to the Marketing Cloud tab in Sales Cloud to complete the integration. The admin then receives the following error message: 'Insufficient User Permissions. You have not been designated as an integrated Marketing Cloud user. Contact your system administrator'. The admin notices the Marketing Cloud for AppExchange Admin option is selected when looking at the user settings. What action should correct the issue?
> Apply the Marketing Cloud for AppExchange User option as well

#### 55. A Marketing Cloud admin is configuring the Marketing Cloud data model for the first time. Journey Builder with of messages being sent to customers, based on if there has been an order or not. There are two existing data model Orders: - Customers contains information about subscribers including Email Address, First Name, Last name. - Orders contains information about the orders and includes the unique identifier of the customer. In which two ways should the admin configure Data Designer to allow this data to be used within a Journey?
1. Link the Orders data extension to the Customers data extension using a One-to-Many relationship
> 고객 정보를 orders에 가지고 있기 때문에, 1대 다가 많다.

2. Link the Customers data extension to the data model using Customer ID
> 고객의 데이터를 customer id 를 통해 contact와 맵핑하면 된다.


#### 56. A Marketing Cloud admin is tasked with overhauling the data model for Enterprise. While the current data model is isolated to the email channel and there are plans to expand to both SMS and Push channels in the near future. Which three data preparations should be made to retain high data quality in the new mode?
1. Remove nonessential data for marketing purposes.
2. Identify and assign appropriate keys to tie records together.
3. Normalize data and fields to prevent redundancy.


#### 57.Which three options determine when a contact could enter a journey? (choose 3)
1. Re-entry at any time
2. No re-entry
3. Re-entry only after exiting

#### 58. Northern trail Outfitters (NTO) is warming a new Dedicated IP address, and they need to monitor their deliverability across major ISPs. Which bounce type would be indicative of the ISPs view of NTO’s sending reputation?
> Block

ISP가 해당 ip에 대한 메일 발송을 방지한다는 라벨로서, block을 사용한다


#### 59. A customer frequently holds seminars and other events to interface with their customers. They plan to do the following: - Use SmartCapture forms to write data into event registration data extensions. - Cross-reference the records in each registration data extension with corresponding invitation email sends. - Send a follow-up email to customers who click on the registration link in the invitation email, but do not complete registration. Which skill is needed to build an efficient solution?
> SQL


#### 60. Which two statements are correct about Send Logging?
1. AMPscript can be used to pull data from Send Logs for use within emails.
2. SQL Query Activities can reference Send Logs in combination with system data views.


#### 61. A publishing company has presented the following: 1. A need to send renewal reminders to customers whose subscriptions expire in 15 days and 7 days. 2. A campaign needs to be created and managed by a general marketing user who will not have administrative rights and who is not technical. 3.The customer's expiration date is included in the data file. What component should the customer's solution include?

1. Data Filter
2. Template-based emails
3. Automation Studio


#### 62. During discovery, the customer outlines data requirements and the anticipated use of Marketing Cloud with the following criteria: 1. Customer data will be fully refreshed every night via Import activity from the customer's data warehouse. 2. Contact records will be augmented by relational data tables via Contact Builder. 3. The customer data file will contain 5M records with 40+ attributes. 4. One attribute will house HTML code, 1000 characters max, that will be used to populate Account Access content areas in emails. 5. A customer ID will be used as the unique identifier for each contact. Which statement differentiates the use of data extensions over lists?
> Data extensions are necessary for Contact Builder

#### 63. Analyst of The Northern Trail Outfitters (NTO) marketing team needs to pull email metrics for an upcoming quarterly company meeting. These metrics need to be reported per email campaign for each of NTO's Business Units: Number of Sends, Delivery Rate, Overall Bounce Rate, Block Bounce Rate, Open Rate, Click Rate, Complaint Rate, Unsubscribe Rate. Which email report should NTO's Marketing Analyst pull from Marketing Cloud to get this information?
> Campaign Email Tracking Report


#### 64. Northern Trail Outfitters has Marketing Cloud users who need data extension View and Update permissions for campaigns related to B2C sales while restricting access to campaigns related to B2B sales. How should they accomplish this?
> Create separate folders and add permissions


#### 65. A Marketing Cloud admin is asked to understand how a certain content area within a Triggered Send Email is performing. Which report should be used?
> Impression Tracking for Triggered Sends

#### 66. Northern Trail Outfitters wants to optimize their eCommerce site by sending a follow-up Email to a customer alter an online purchase is made. What feature could be used to solicit website feedback without navigating away from the email?
> Email content block

#### 67. A Marketing Cloud admin has configured a Tracking Extract which includes all subscriber attributes for their global regions. However, the admin notices accented characters in the customers' names appear jumbled in the extracted file. Which two settings could solve this issue
1. Change Character Encoding to UTF-8
2. Select Unicode Output


#### 68. A Marketing Cloud admin wants to automatically unsubscribe customers who respond to marketing emails asking to be removed from the mailing list. Which two steps should the admin take to enable this functionality?
1. Ensure a Custom response is enabled for Automated Response in Reply mail Management
2. Select Unsubscribe Manual requests in Reply Mail Management


#### 69. Northern Trail Outfitters (NTO) is a global brand that includes many subsidiary brands under the parent umbrella. NTO is the Enterprise business unit and also has a child business unit used for sending promotional emails. How should the rest of the business units be organized?
> Create child business units for each brand and nest another level of child business units for GEOs.


#### 70. Northern Trail Outfitters has Imported a file Into All Subscribers. They then received a results file stating admin@example.com could NOT be imported. Which error code would the file contain for this record?
>  List Detective


#### 71. A Marketing Cloud admin wants to create an SFTP User for the first time. Which two considerations should be taken when configuring an SFTP User?
1.  By default, the username is the MID for the current Marketing Cloud MID.
2. Minimum password length is 12 characters.


#### 72. What are entry source types for Journey Builder?
> Data Extension, Audience Studio, API Event, Date Based Event


#### 73. Northern Trail Outfitters wants to use Synchronized Data Sources to sync Contact data from Salesforce CRM. However, they only want to sync records they would be able to send to reducing the amount of data being brought over. Which two filtering options could be used when configuring the Contact synced object?

1. Select all records with an email address
2. Select all records which are active in All Subscribers


#### 74. Northern Trail Outfitters was given a set of requirements from their governance team to protect against misuse of customer data. One item mandated Marketing Cloud users should NOT be able to export data without approval from the governance team, however, users should still be able to view data within the system. Which feature would allow compliance with this requirement?
> Export Email Allowlist


##### 75. Northern Trail Outfitters wants to have specific permission restrictions applied to all users in a business unit. How should they accomplish this?
> Assign a role to the business unit


#### 76. Einstein Recommendations uses data extensions to store user-facing information. How is this data passed to Marketing Cloud?
> Collect Tracking code


#### 77. A Marketing Cloud admin wants to ensure no one could access the API with their Marketing Cloud user credentials. Which security setting would control this behavior?
> Deselect ‘Enable Username and Password for Web Services’

#### 78. A Northern Trail Outfitter’ (NTO) subscriber clicks a link in an NTO email. Prior to the clicking, the subscriber had a bounces status in Marketing Cloud. What are the effects of the click to the subscriber’s status?
> Status is changed to Active and the bounce count is unchanged


#### 79. What should be confirmed to ensure Journey Builder directs the subscribers correctly?
> Journey Data is used for the Decision Split.


#### 80. A Marketing manager requests to receive an email, once a week, with high-level metrics in a standard format. Specifically the manager wants to know how many emails were sent in the last week. What location and activity would allow the Marketing Cloud admin to complete the request?
> Email Studio: Select “Account Send Summary” in Tracking Reports and schedule a weekly report to be sent


#### 81. A Marketing Cloud admin is setting up Northern Trail Outfitter’s newest business units and several users to assign to the new business units. How would the admin assign users to the business units?
> Search for the individual user, select their name, and click Manage Role under Business Units.

#### 82. A Marketing Cloud admin is asked to add a set of four tracking parameters automatically to all the links in an email sent via email studio. Which solution should the admin suggest?
> Web Analytics Connector


#### 83. You can receive Audit Trail records either through: (Pick Two)?
1. Marketing Cloud Automation Studio Data Extracts
2. REST API extracts.

#### 84. Which gives you access to data not available via standard tracking functions and to obtain run-time information about email send attributes?
> send Logs


#### 85. A Marketing Cloud admin needs to create a zipped file for use outside of Marketing Cloud. What should the admin consider? (Choose two.)
1. A File Transfer Location must be configured after using the Data Extract Activity
2. The fields included in a data extract file vary according to the Extract Type you choose