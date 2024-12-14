### 1. Northern Trail Outfitters wants to drive additional online sales. They are interested in using Einstein to recommend similar items to customers during the checkout process. Which two terms would they add to their website to accomplish this?
1.  Recommendation Code
2.  Collect Code


### 2. Northern Trail Outfitters wants to set up their Send Log data extension. Which three considerations should be made for long term success ( choose 3 w)

1. Apply an appropriately-scoped Data Retention period
2. Log attribute data necessary for auditing communications
3. Add custom fields not included in the Send Log Template


### 3. What are potential risks of using Non-Scope by User Data Access configuration for Marketing Cloud Connect(choose 2)
1. A User may run a report containing records visible to them but not the Salesforce System User, causing <b>zero emails</b> to be sent.
2. A User may run a report displaying only records visible to them but containing additional records they don't see, causing a send to deploy to more contacts than intended.



### 4. While setting up Marketing Cloud Connect, a Marketing Cloud admin navigates to the Marketing Cloud tab in Sales Cloud to complete the integration. The admin then receives the following error message: - <u>Insufficient User Permissions. You have not been designated as an integrated Marketing Cloud user</u>. Contact your system administrator. The admin notices the Marketing Cloud for AppExchange Admin option is selected when looking at the user settings. What action should correct the issue?

> Apply the Marketing Cloud for AppExchange User option as well


#### 5. A customer is developing a new eCommerce section of their website and plans to leverage transactional data in customer journeys. Which two Marketing Cloud features will support this effort?

1. Data Designer

2. Cloud Pages


#### 6. Where in Setup can you edit email Headers & Footers?
> Account Settings



#### 7. A customer is interested in designing a solution to ensure that subscribers only receive categories of emails that they want to receive. The built-in subscription center will be used as part of the solution. Which feature should be utilized to make this happen?
> Profile center



#### 8. Northern Trail Outfitters wants to drive additional online sales. They are interested in using Einstein to recommend similar items to customers during the checkout process. Which two terms would they add to their website to accomplish this?
1.  Recommendation Code
2.  Collect Code


#### 9. Northern Trail Outfitters' Marketing Cloud admin wants to ensure certain subscribers' opens and clicks are NOT tracked at their request, in accordance with the EU's General Data Protection Regulation. In which two ways should the administrator configure these settings? (Choose 2)
1.  Create a Preference Attribute called DoNotTrack.
2. Enable the DoNotTrack Attribute on each Subscriber.


#### 10. Choose the correct steps needed to apply administrative permissions for Marketing Cloud Connect: (choose two)?
1. Edit the CRM User Page Layout to add the Marketing Cloud for AppExchange User and Marketing Cloud for AppExchange Admin Fields
2. Enable Marketing Cloud for AppExchange User and Marketing Cloud for AppExchange Admin for the Salesforce CRM Administrator User



#### 11. Which of the following statements applies to retention settings?
> You cannot remove the configured data retention settings once you configure them.


#### 12. Northern Trail Outfitters (NTO) has a franchise model which allows locally-owned stores to operate under the corporate umbrella. They are required by corporate policy to email each franchisee a monthly statement, but the statement cannot be publicly accessible. Which Marketing Cloud product should NTO purchase as a solution?

> Email Attachments
 
 프랜차이즈는 이메일 어태치


#### 13. 질문 69
오답
A Marketing Cloud admin is asked to append an Urchin Tracking Module (UTM) variable string to links in emails. What functionality would allow this?
> Web Analytics Connector

UTM은 Web analytic connector


#### 14. A customer will provide a single daily file on the Marketing Cloud SFTP at 3 AM and needs an alert if the file is not present on time. The file needs to be imported into a staging data extension, separated into two different data extensions. Which workflow should meet these requirements?

> Scheduled Automation: Import File Activity > SQL Query Activity 1 > SQL Query Activity 2
 
 3am 은 파일 트랜스퍼 없고 스케줄이다



 #### 15. What Salesforce Editions work with Marketing Cloud Connect? (choose 3)
 1. unlimited
 2. enterprise
 3. developer



 #### 16.  A customer wants to automate a series of three emails as part of a Membership Renewal drip campaign. Email #1 will be sent one month prior to the member's renewal date. Email #2 will be sent one week prior to the member's renewal date. Email #3 will be sent on the member's renewal date. A master audience is updated in real time via the API. Which steps should be included in the customer's automation?

 세 갈래로 발송되는 발송 형태는
 THREE FILTER

 > Three Filter Activities > three Send Activities to the filtered audiences.



 #### 17. Additional IP Whitelisting is required for the following when configuring MC Connect: (choose 3)?

 1. Global IP Whitelist Ranges for General MC Connect Functionality
 2. IP Addresses for Notification and Identity Validation Emails
 3. Regional Salesforce Send IP Addresses



 #### 18. Which send process can use Sender Profiles? (Choose 3)
 1. Guided sends
 2. triggered sends
 3. User Initiated sends


 #### 19. Northern Trail Outfitters (NTO) hired a new Marketing Cloud admin, who was told all emails come from info@email.nto.com. The previous admin did not leave any documentation. Which aspects would confirm a Sender Authentication Package (SAP) has been set up on the account?

 인수인계 안하면 트랙이랑, url 이 help.nto면 됨



 #### 19. Northern Trail Outfitters (NTO) wants to limit who can receive Marketing Cloud tracking data via email from their Account to any email associated with their domain (ntoretail.com). Which steps should be taken to implement this? (Choose 2)
 이메일 발송에 대해서는 IP whitelist는 스팸임

 1. Enforce Export Email Allowlist
 2. Add a Domain to the Export Email Allowlist



 #### 20.When modifying the Lead/Contact Page Layouts in CRM for Marketing Cloud Connect, add: (choose 3)?
 1. Lead/Contact Actions
 2. email sends
 3. Individual Email Results



 #### 21. Where do contact deletions take place in Enterprise 2.0 accounts?

 > Top-level accounts and all business units in the specified Enterprise 2.0 account.


 #### 22. Set up or edit the tracking parameters that are appended to the links in messages sent from your Salesforce Marketing Cloud account using?
 트래킹 파라미터는 
 > Prameter manager



#### 23. By default, the data extension retention policy deletes unused data extensions after how long?
> 6 months


#### 24. Where do you integrate Marketing Cloud Connect users?
> Marketing cloud setup



#### 25. Which of the following are true about All Contacts in Contact Builder? (choose 3)
1. All Contacts function across all Channels in Marketing Cloud.
2. All Contacts function at the Enterprise/Parent level.
3. All Contacts contain All Subscribers plus anything marked as a Population.