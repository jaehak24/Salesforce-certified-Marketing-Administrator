### NTO subscribers clicks a link in an NTO email. Prior to clicking, the subscriber had a bounced status in Marketing Cloud. What would be the effects of the click on the subscriber's status?

> Status remains as Bounced. the bounced count is unchanged


### Marketing cloud admin has scheduled a query on daily basis. They notice the qyery sometimes fails to execute. How would the admin ensure a notification is received when the query fails?
> Add the Email address in the automation notification settings


# SFTP
> 파일을 주고 받을 대 사용하는 인터넷 통신 규약, 신뢰할 수 있는 데이터 스트림을 통해서 SSH 파일 전송하는 프로토콜 또는 보안 파일 전송 프로토콜

### NTO requiers all subscriber files placed on the SFTP for import to be encrypted. Which activity in Automation Studio could be used to decrypt the file to preapre for importing?
> File Transfer activity

### Marketing cloud admin has configured a Tracking extract which includes all atttributes for their global regions. However, the adming notices accented characters in the customer's names appear jumbled in the extracted file. which setting could solve this issue?
> Change character Encoding to UTF-8

### NTO runs a nightly automation consisting of a FIle Transfer and a File Import. Following an update from the engineerign team, the automation began failing. The Marketing Cloud admin suspects the CSV file now had an invalid format. How could the admin receive a file of the bad data rows to confirm this theory?
> Update the import definition to include a notification email address

## What are entry source types for Journey builder?
> Data Extension, <U>audience studio</U>, API Event, Data Based Event

### NTO wants to segment audiences based on Sales Cloud data. where would their Cloud admin configure Sales Cloud Objects to be synce and leveraged in Markeitng Cloud?
> Contact Builder &rightarrow; Data sources

### NTO wants to leverage the REST API for an external application they plan to build. Where sould their Marketing Cloud admin set up permissions to allow REST authentication?
> Installed package

### To precent retention of stagnant data, NTO wnats any inactive data stored in data extension to be cleared 12 months

> Apply a Row based Retention to each data extension as it is created, set to 12 months

#### NTO uses Sender Authentication Package for branding purposes. Their German business unit is configured with the SAP domain de.ntomarketing.com. The german NTO team is preparing for a campaign and wants to use customized CloudPages with the domain de-special.ntomarketing.com. How could the Marketing Cloud admin meet this requirement?
> Purchase a private domain for use in CloudPages.

### NTO wants to copy journeys across business units. What coyld be used to replicate journey structure so it can be easily recreated in another account?
> Package Manager

### NTO hired a new Marketing cloud admin, who was told all emails come from info@email.not.com. The previous admin did not leave any documentation. What should confirm a Sender Authentication Package(SAO) has been set up on the account?
> Upon receiving a email, all tracked links start with click.email.nto.com

## NTO installed Query studio for Marketing cloud, however, users are reporting they do NOT have access. How should the marketing cloud admin enseure users have acess?
> Allow acess package acess on appropriate Roles.

## NTO has imported a file into All subscribers. They then received a results files starting admin@example.com could NOT be imported. Whcih error code would the file contain for this record?
> list detective

### Marketing cloud admin is using the Import Wizard to import data into a non-sendable data extension, but receives an error indicating the import type being used requires a primary key. Which import type could the admin uses instead?
> Overwrite

### Marketing cloud admin has been asked to update their Marketing Cloud SFTP user passwordd. Where in Setup could they accommplish this task?
> Data management

### Marketing cloud admin has been asked to include Sales Cloud data in their queries. Which feature would allow this functionality?
> Synchronized Data sourcces

### Nto uses Marketing Cloud Connect to leverage Slaes Cloud data in their Journeys. A user reported the data coming from slaes cloud is NOT up to date. Where should the Marketing Cloud admin begin troubleshooting?
> Contact Builder> Data sources

### NTO uses DoubleClick Bid Manager, Facebook Ads, and Google Analytics to manage advertising spend. They want to combine these data sources with marketing Cloud's API to identify their most effective campaigns. What feature should be recommended?
> Datorama

## NTO has a mobbile app. Which production would allow them to send push notification to sustomers with their mobile app?
> Journey builder Builder(if there is mobilepush than mobile push is the answer)


### Maketing Cloud admin is tasked with requesting Marketing CLoud Connect Multi-Org enablement. What consideration should be given to the preference/profile for this integration?
> Multi-Org <U>does not support the standard profile/preference</U> center for the business unit setup

### NTO just purchase Marketing Cloud. Which task would the Marketing Cloud admin be guided through in Setup Assistant?
> Building the data structure used to <U>>store</U> audience information

### NTO is preparing to send a promotional email. The audience file was laoded into a data extension but it does not display for the Marketing Cloud admin scheduling the send what sould the admin confirm to resolve the issue?
> The data extension is marked as sendable

### The marketing Cloud admin for NTO wants to build an audience with Adevertising Studio which mimics the traits of their most valuable customers. Which network supports look alike directly from Advertising Studio?
> Facebook

### NTO does not want to store email addresses or phone numbers within Marketing cloud. Which feature should they use?
> Tokenized Sending

### NTO wants to use synchronized Data Sources to sync Contact Data from Salesforce CRM. However, they only want to sync records they want to sync records they would be able to reduce the amount of data being brought over. Whcich filtering option could be used when configuring the Contact synced object?
> Select all records where HasOptedOutofEmail is False

### NTO is building a journey which randomly send different versions of an initial welcome email to new subscribers; However, subscrbers receive the same follow-up email two week later. To improve maintainability of their email content, NTO wants to use five completely different emails, rather than having one email with dynamic content. Which activity would allow them to build the journey with the fewest activities possible?
> Join Activity

### Marketing CLoud admin needs to warm their account's Dedicated IP . what's option for segmentation aligns with the IP warming process.
> Segment subscribers by subscriver opt-in date

### Marketing Cloud admin has been asked to get the last 30 days of Bounce data from their account. What should the admin use to get ganular data in bulk in pre-defined format?
> Automation Studio Tracking Extract

### NTO purchased one sender Authentication package(SAP) to ensure their branding is on every marketing communication. What would be achieved with SAP?
> <U>Image URLS</U> are wrapped with the appropriate brand URL

#### NTO uses data extenstion for all of their email audiences. Customer reports they updated their email address week ago but continues to receive the NTO Daily Digest email at their old address. The marketing Cloud admin has confirmed the new email address is present in the appropriate data extension. What consideration 
> The email address in All Subscrivers is prioritized

## Where would a Marketing Cloud admin view all verified email address?
> address management

### NTO wants a business analyst to import contact lists. The analyst has the following Marketing cloud roles: Marketing Cloud Channel Manager and Marketing cloud Viewer. The analyst logged in but is unable to import contact lists. 
> Remove marketing cloud Viewer

## Which data structure could be configured to appear in the out-of-the-box Subscription Center?
> Publish Lists

### Marketing Cloud admin at NTO is exploring wheter they need to seperate their brands into seprate business units. When should the admin create seprate business units for each of NTO's Brand?
> Brand-specific private domains are required for images and links

### Marketing cloud admin wants to ensure email sends exclude their testing prefix of[PREVIEW] in the subject line when deploying from Email studio. What should the admin do to prevent the prefix from deploying in live sends?
> add [PREVIEW] to the subject line <U>validation lsits</U>

### Marketing cloud admin is asked by the marketing team to ensure a default Header and Footer be added to emails. Where under setup could this be created?
> Account setting

### Marketing cloud admin wants to cinfigure a new keyword for an upcoming SMS campaign. After entering the desired keyword <U>CELEBRATE</U> the admin notices the keyword is unavailable. What issue could the admin be facing?
>  Keyword is used within another business unit

#### Marketing cloud admin has been asked to grant full administrator permission to a new user. Which two standard roles should be selected for the new user?
> administrator and Marketing Cloud Administrator

## Marketing cloud admin discover large send are not meeting send speed goals set by the organization. What functionality woruld get messages out the door faster?
>  Burst sendng

#### Marketing cloud admin wants to create an SFTP user for the first time, Which consideration should be taken when configuring SFTP user?
> By default, the username is the MID for the current Marketing Cloud MID.

### NTO wants to have specific permission restrictions applied to all users in a business unit. How should they accomplish this?
>  Assign a role to business unit


### User asks a Marketing cloud admin to update and increase their session <U>timeout setting</U>. Which consideration should the admin review before making this update?
> change impact all users

### Marketing Cloud admin wants to ensure sensitive information needed for email sends is NOT imported and stored in Marketing cloud , What solution should they implemetn?
> tokenized sending

## Marketing Cloud admin wants to create a <U>suppression list for hard-bounced email addresses</U>. Where the details be found?
> Bounce data View

##### Marketing Cloud admi nhas noticed a File Drop Automation has been failing on the Import File activity. The automation is configured with a filename pattern, so the filename is expected to begin with customer_import. The import is configured to look for a file named customer import_%%Year%%%%Month%%%%Day%%.csv, however, the admin notices the filenames include seconds and milliseconds. How should the admin fix the issue?
> USE %%6Filename_From_trigger%% in the Import File Activity


### NTO is global brand that includes many subsidery brands <U>under the parent umbrella</U>. NTO is the Enterpricse business unit and also has a child business unit used for sending promotional emails. How should the rest of the business unit be organized?
>  Create a single child business unit for the other brands to share and standarlized naming conventions.

## What element of CAN-SPAM should the marketing Cloud admin ensure are present for each commercail send?
> Preference Center link and Physical mailing address

### Marketing cloud admin is asked to add a set of four queries strigs automatically to all the links in an email sent via email studio
> Paramter Manager

## Marketing Cloud admin has been asked to update theri Marketing Cloud SFTP user password. Where in Setup could they accomplish this task?
> Data management


dump test 참조


https://www.exam-answer.com/marketing-cloud-admin-tracking-extract-accented-characters