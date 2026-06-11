---
title: "Trading Relationship Management User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/nscc111_trm_ug_2022Oct26.pdf"
pages: 41
size: "3193.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Trading Relationship Management User Guide

**Original File:** [nscc111_trm_ug_2022Oct26.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/nscc111_trm_ug_2022Oct26.pdf)  
**Category:** Other  
**Total Pages:** 41  
**File Size:** 3193.1 KB  

---

## Page 1

 
 
 
EQUITIES CLEARING 
TRADING RELATIONSHIP MANAGEMENT USER GUIDE 
OCTOBER 26, 2022 
 


---

## Page 2

 
 
TABLE OF CONTENTS 
About the Trading Relationship Management System .................................................................................... 4 
How Were Trading Relationships Managed in the Past? .................................................................................... 4 
Trading Relationship Management Roles .......................................................................................................... 4 
Trading Relationship Management Process ..................................................................................................... 5 
Updating Relationships ....................................................................................................................................... 5 
System Alerts ...................................................................................................................................................... 5 
About Effective Dates ......................................................................................................................................... 6 
Effective Dates for Executing [[Broker]] IDs ........................................................................................................... 6 
When the Effective Date is Today ...................................................................................................................... 6 
Future Effective Dates ....................................................................................................................................... 6 
Accessing the Trading Relationship Management System ............................................................................. 7 
Using the Dashboard .......................................................................................................................................... 7 
Viewing the Dashboard ....................................................................................................................................... 8 
Displaying the Dashboard Page .......................................................................................................................... 9 
Managing Relationships .................................................................................................................................... 10 
Adding New Relationships ................................................................................................................................ 10 
Adding New Correspondent Clearing Trading Relationships ........................................................................... 11 
Adding a New QSR Trading Relationship ........................................................................................................ 12 
Approving Pending Relationships ..................................................................................................................... 13 
Add [[Broker]] IDs to an Existing Relationship ....................................................................................................... 15 
Search Relationships ......................................................................................................................................... 16 
Rejecting Pending Relationships ..................................................................................................................... 18 
Spreadsheet Upload Process ........................................................................................................................... 19 
Start with the Most Recent Spreadsheet Template .......................................................................................... 21 
Preparing the Upload Spreadsheet .................................................................................................................. 21 
About the Spreadsheet Template ..................................................................................................................... 22 
Example Spreadsheets ..................................................................................................................................... 24 
Example One ................................................................................................................................................... 24 

---

## Page 3

 
 
Example Two ................................................................................................................................................... 24 
Example Three ................................................................................................................................................ 25 
Example Four .................................................................................................................................................. 25 
Example Five ................................................................................................................................................... 25 
Uploading Spreadsheets ................................................................................................................................... 26 
Displaying Uploaded Spreadsheets .................................................................................................................. 27 
Reviewing and Correcting Upload Errors ......................................................................................................... 28 
Searching Relationships ................................................................................................................................... 30 
Downloading Search Results ............................................................................................................................ 30 
Deleting Active Relationships ........................................................................................................................... 31 
Approving or Rejecting Delete Active Relationship Requests .......................................................................... 33 
Updating Relationships ..................................................................................................................................... 34 
Retracting a Pending Relationship Request ..................................................................................................... 35 
Managing Contacts ............................................................................................................................................ 37 
Viewing Group Contact Information .................................................................................................................. 37 
Updating Contact Information ........................................................................................................................... 38 
Search for Contacts .......................................................................................................................................... 39 
Viewing the Affiliates List .................................................................................................................................. 40 
 

---

## Page 4

Trading Relationship Management User Guide 
About the Trading Relationship Management System 4 
ABOUT THE TRADING RELATIONSHIP MANAGEMENT 
SYSTEM 
The Trading Relationship Management system provides a web-based system that allows eligible [[NSCC]] 
Members to manage online both their Qualified Special Representative (QSR) and Correspondent Clearing 
relationships. 
For Correspondent Clearing and QSR trades to pass editing in [[NSCC]]'s Universal Trade Capture (UTC) 
system, relationships between the QSR/Special Representative and correspondents must be established in the 
Trading Relationship Management system. In addition to these, you can now manage relationships for bond 
special representatives and [[ETF]] authorized participants ([[ETF]] agent and authorized [[participant]] relationship). 
The Trade Relationship Management system automates the method by which members can establish, monitor, 
and maintain these relationships. 
How Were Trading Relationships Managed in the Past? 
The Trading Relationship Management system replaced the manual paper-based process (9A and 9B 
agreements) that managed [[NSCC]]’s Qualified Special Representative (QSR) and Correspondent Clearing 
relationships. Previously, the Correspondent Clearing and Qualified Special Representative (QSR) 
relationships with correspondents were established through a manual process involving the submission of 9A 
and 9B agreements through fax or e-mail to [[DTCC]] Account Administration. The 9A agreement was submitted 
by the QSR (in a QSR relationship) or Special Representative (SR) (in a Correspondent Clearing relationship). 
The 9B agreement was submitted by the correspondent. In the case of a tri-party QSR agreement, Attachment 
1 was signed by the execution platform. 
Trading Relationship Management Roles 
The following table describes the roles: 
Name Description 
Special Representative (SR) A [[Member]] or a registered [[Clearing Agency]] that designates members for which it acts. 
Correspondent Clearing Service A trade reporting service that processes [[Equity]] and corporate bond trades executed 
by the special representative. 
Qualified Special 
Representative (QSR) 
An [[NSCC]] full service [[Member]] who has been granted status for the purpose of locking 
in trades for other [[NSCC]] members and/or their correspondent. 
Sponsors For relationships involving non-U.S. participants, the non-U.S. [[participant]] must be 
sponsored. An example of a sponsor is CDS Clearing and Depository Services Inc. 
(CDS), the Canadian national depository service. CDS serves as a sponsor for all 
Canadian participants. 
For relationships where one or both participants are sponsored participants, the 
sponsors must approve both new relationships and updates to existing relationships. 

---

## Page 5

Trading Relationship Management User Guide 
Trading Relationship Management Process 5 
TRADING RELATIONSHIP MANAGEMENT PROCESS 
The Universal Trade Capture (UTC) system uses the relationship between clearing members and their 
executing [[Broker]] IDs as part of its trade validation process. The UTC system always edits QSR and 
Correspondent Clearing trades at the clearing [[Member]] level. When the two clearing members in a QSR or 
Correspondent Clearing relationship agree, the UTC system requires at least one executing [[Broker]] [[ID]] on each 
side of the trade as part of its trade validation process. By maintaining your executing [[Broker]] IDs through the 
Trading Relationship Management system, you are able to successfully minimize trade rejections from the 
UTC system due to missing or inaccurate executing [[Broker]] IDs. 
Updating Relationships 
You can update any of the information for relationships that you have saved, but not yet submitted. After data 
has been submitted, you can: 
• Change the executing [[Broker]] requirement. 
• Add executing brokers with appropriate effective dates. 
These updates must be approved by your counterparty to be applied to the trading relationship. 
For relationships where one or both participants are sponsored participants, the sponsors must approve 
changes to the relationship. For more information about sponsors, see Roles. 
System Alerts 
The system sends alerts to all involved parties: qualified special representative special representative, 
correspondent, sponsor, if applicable, when any of the following occurs: 
• N ew relationship added. 
• N ew relationship approved or rejected. 
• R elationship deleted. 
• R elationship updated. 
• R elationship becomes either active or inactive. 
A reminder alert is sent to all parties each day that an agreement is pending approval. The system sends alerts 
through: 
• Shows alerts on the Dashboard. 
• E mail notification. 
• Message Queue (MQ) or FIX message delivered to each party subscribed to the notification. 
  

---

## Page 6

Trading Relationship Management User Guide 
Trading Relationship Management Process 6 
About Effective Dates 
The effective date is the earliest date a new relationship may begin, or that an update to a relationship may 
take effect. It can apply to the relationship as a whole or to individual executing brokers who are part of the 
relationship. 
Note:  
If the effective date is not a business day, the update to the relationship is active on the next business day. 
Effective Dates for Executing [[Broker]] IDs 
For trading relationships that include executing [[Broker]] IDs, you can select a different effective date for each 
individual executing [[Broker]] [[ID]], as long as that date is equal to or later than the overall effective date for the 
trading relationship. 
When the Effective Date is Today 
Any changes to trading relationships that are made using the current day as an effective date, once approved 
by all involved parties, become effective within a few minutes. 
Future Effective Dates 
You can select effective dates that occur in the future. After your changes are approved by all involved parties, 
the system makes those changes on the effective dates you have selected. 

---

## Page 7

Trading Relationship Management User Guide 
Accessing the Trading Relationship Management System 7 
ACCESSING THE TRADING RELATIONSHIP 
MANAGEMENT SYSTEM 
Access to the Trading Relationship Management system is controlled by individuals designated as access 
coordinators at the [[Member]] firm. Access coordinator authorization forms are available in the Access 
Coordinator Forms section.  
For access to the Trading Relationship Management system, contact your firm’s super access coordinators 
(SACs) and access coordinators (ACs). They register and manage user access to [[DTCC]] products. For SACs 
that need access to any Equities Clearing products and services, email [[NSCC]] Integration at 
NSCCIntegration@[[DTCC]].com. 
Using the Dashboard 
After logging in to the Trading Relationship Management system, the Dashboard appears. It displays alerts for 
relationships that: 
• Your counterparty created and that requires your attention. 
• You created and that requires your counterparty's attention. 
• You have saved, but not yet submitted. 
These can include the trading relationships in the following statuses: 
• Pending Approval 
• Pending Delete Approval 
• Saved 
The Dashboard also displays alerts for spreadsheet upload errors. 
  

---

## Page 8

Trading Relationship Management User Guide 
Accessing the Trading Relationship Management System 8 
Viewing the Dashboard 
The Dashboard displays information in the following sections: 
• Trading Relationships Pending 
• Trading Relationships Pending with Others 
• Spreadsheet Errors 
 
From the Dashboard page, you can approve, reject, or delete pending relationships. You can also approve or 
reject requests to delete active relationships. To display details for that relationship, click the [[participant]] [[ID]]. 
See Also: 
• Approving Pending Relationships 
• Rejecting Pending Relationships 
• Approving or Rejecting a Delete Active Relationship Request 


---

## Page 9

Trading Relationship Management User Guide 
Accessing the Trading Relationship Management System 9 
You can also research spreadsheet upload problems. To display the spreadsheet, from the Trading 
Relationship Spreadsheet column click the spreadsheet name link. To display the error messages for a 
spreadsheet, click the  icon for that spreadsheet in the Details column. For more information, see Reviewing 
and Correcting Upload Errors. 
Displaying the Dashboard Page 
To return to the Dashboard from any page within the Trading Relationship Management system, click 
Dashboard from the main menu. 


---

## Page 10

Trading Relationship Management User Guide 
Managing Relationships 10 
MANAGING RELATIONSHIPS 
After one side of the relationship has entered the details for that relationship, that relationship appears in 
pending status, waiting for either approval or rejection by the counterparty. At this point, the counterparty can 
approve or reject the entire relationship, or approve or reject specific executing brokers within the relationship. 
After a new relationship is approved by all involved parties, the relationship becomes active on the first 
business day equal to or after the requested effective date. The QSRs and SRs can now send trades to [[NSCC]] 
containing the new relationship. 
For relationships where one or both participants are sponsored participants, the sponsors must approve new 
relationships. For more information about sponsors, see Roles. 
Adding New Relationships 
Use the Trading Relationship Management system to add Correspondent Clearing and QSR relationships. 
Either the correspondent or the qualified special representative/special representative (QSR/SR) can enter the 
details for a particular relationship into the Trading Relationship Management system, through the online web 
interface or by uploading a spreadsheet. 
To use the spreadsheet upload process to add new trading relationships. 
1. Based on the template, create a spreadsheet that contains all of the required information for each
 
relationship. 
To see additional tips, move your mouse over the heading for each column. 
2. If the relationship includes executing brokers, enter one row for each executing [[Broker]]. 
For each row, set the Executing [[Broker]] [[ID]] for Trade Editing column to Y. 
For each row, repeat all of the information for that relationship, except for the following: 
• R ole: Indicate which side of the relationship (QSR, SR, or CRSP) that the executing [[Broker]] [[ID]] on this 
row belongs to. 
• Executing [[Broker]] [[ID]]: Include at least one [[Broker]] [[ID]] per side (as defined by the Role column) of the 
relationship. 
• Executing [[Broker]] Effective Date: Provide the effective date for the executing [[Broker]] [[ID]]. 
 


---

## Page 11

Trading Relationship Management User Guide 
Managing Relationships 11 
 
3. Save the spreadsheet as either an .xls or .xlsx file. 
Adding New Correspondent Clearing Trading Relationships 
Either the correspondent or the special representative can set up a new Correspondent Clearing trading 
relationship through the online web interface. 
Note:  
• Sponsors, acting on behalf of the participants they sponsor, can set up new trading relationships. 
• For relationships where one or both participants are sponsored participants, the sponsors must also approve new 
relationships. For more information about sponsors, see Roles. 
All new relationships become active on the effective date once approved by the counterparty. 
To add a new relationship: 
4. From the main menu, click New Relationship. 
The Create New Trading Relationship page appears. 
5. Complete the Trading Relationship Information section of the page: 
a. In the Trading Relationship Type field, select Correspondent Clearing. 
b. Select an Effective Date. 
c. You can use the calendar tool  to select the effective date. To learn more about effective dates, 
see About Effective Dates. 
d. In the Trading Relationship Role drop down menu, select your role in the trading relationship. 
e. For example, if you are a special representative, select Special Representative. If you are the 
correspondent, select Correspondent. 
f. In the Executing [[Broker]] for Trade Editing field, select Yes or No to indicate whether an executing 
[[Broker]] [[ID]] is required. 
6. Complete the Qualified Special Representative/Special Representative Information and Correspondent 
Information sections of the page: 
a. Your [[participant]] Name and [[participant]] [[ID]] are populated for you. 
b. You can use the [[participant]] [[ID]] look up tool  to look up your counterparty's [[participant]] [[ID]]. 
  


---

## Page 12

Trading Relationship Management User Guide 
Managing Relationships 12 
c. If you set the Executing [[Broker]] for Trade Editing field to Yes, provide at least one executing [[Broker]] [[ID]] 
for each side of the relationship. 
 
d. In the Requested Effective Date field, provide an effective date for each executing [[Broker]] [[ID]] that you 
enter. 
e. U se the calendar tool   to select the date. 
f. To learn more about effective dates, see About Effective Dates. 
g. To add additional rows, click Add. To remove rows, click the selection box for that row and click 
Remove. 
7. To save your work to complete at a later time, click Save. 
Your saved relationships appear on the Dashboard. You can also perform a search for
 relationships in the 
Saved status. 
8. To submit the new relationship for approval by your counterparty, click Submit. 
The system prompts you to read and acknowledge a legal statement. 
9. Read the statement, click the selection box, and click I agree. 
The system sends an alert to your counterparty notifying them that a relationship is pending their 
approval. 
Adding a New QSR Trading Relationship 
Either the correspondent or the qualified special representative can set up a new QSR trading relationship 
through the online web interface. 
Note: 
• Sponsors, acting on behalf of the participants they sponsor, can set up new trading relationships. 
• For relationships where one or both participants are sponsored participants, the sponsors must also approve new 
relationships. For more information about sponsors, see Roles. 
After receiving the counterparty approval, all new relationships become active on the requested effective date. 
1. From the main menu, click New Relationship. 
The Create New Trading Relationship page appears. 
2. Complete the Trading Relationship Information section of the page: 
a. In the Trading Relationship Type field, select Qualified Special Representative. 
b. Select an Effective Date. 
c. You can use the calendar tool   to select the date. 
d. To learn more about effective dates, see About Effective Dates. 


---

## Page 13

Trading Relationship Management User Guide 
Managing Relationships 13 
e. From the Trading Relationship Role drop-down menu, select your role in the trading relationship. 
For example, if you are a QSR, select Qualified Special Representative. If you are the correspondent, 
select Correspondent. 
f. From the QSR Execution Platform drop-down list, select a platform. 
g. In the Executing [[Broker]] for Trade Editing field, select Yes or No to indicate whether or not an 
executing [[Broker]] [[ID]] is required. 
3. Complete the Qualified Special Representative/Special Representative Information and Correspondent 
Information sections of the page: 
a. Your [[participant]] Name and [[participant]] [[ID]] are populated for you. 
b. You can use the [[participant]] [[ID]] look up tool  to look up your counterparty's [[participant]] [[ID]]. 
c. If you set the Executing [[Broker]] for Trade Editing field to Yes, provide at least one executing [[Broker]] [[ID]] 
for each side of the relationship. 
 
d. In the Requested Effective Date field, provide an effective date for each executing [[Broker]] [[ID]] that you 
enter. 
e. You can use the calendar tool   to select the date. To learn more about effective dates, see About 
Effective Dates. 
f. To add additional rows, click Add. To remove rows, click the selection box for that row and click 
Remove. 
4. To sa ve  your work to complete at a later time, click Save. 
Your saved relationships appear on the Dashboard. You can also perform a search for relationships in the 
Saved status. 
5. To submit the new relationship for approval by your counterparty, click Submit. 
The system prompts you to read and acknowledge a legal statement. 
6. Read the statement, click the selection box, and click I agree. 
The system sends an alert to your counterparty to advise them that a relationship is pending their 
approval. 
Approving Pending Relationships 
After one side of the relationship has entered the details for that relationship, that relationship appears in 
pending status, waiting to be approved or rejected by the counterparty. The counterparty can approve or reject 
the entire relationship, or approve or reject specific executing brokers within the relationship. 
After the relationship is approved, the relationship becomes active on the first business day equal to or after 
the requested effective date. The QSRs and SRs can now send trades to [[NSCC]] containing the new 
relationship. 


---

## Page 14

Trading Relationship Management User Guide 
Managing Relationships 14 
For relationships where one or both participants are sponsored participants, the sponsors must approve new 
relationships. You can approve pending relationships submitted by your counterparty. You can approve all 
executing brokers, approve some, reject some, and/or leave some for further research. 
Note:  
For relationships where one or both participants are sponsored participants, the sponsors must also approve new 
relationships. For more information about sponsors, see Roles. 
1.  From the Dashboard page, click the [[participant]] [[ID]] for any trading relationship that appears in the 
Pending Approval status. The Trading Relationship detail page appears.  
Note:  
You can also use the search function to display relationships in the Pending Approval status. For more information, see 
Searching Relationships. 
2. To approve the relationship for all executing [[Broker]] IDs, click Approve All. 
 
3. To approve specific executing [[Broker]] IDs for either the qualified special representative/special 
representative or the correspondent, click the selection box for those executing [[Broker]] IDs and click 
Approve. 
 
4. To approve all [[Broker]] IDs for either the qualified special representative/special representative or the 
correspondent, click the All check box in that section, and click Approve. 
The system prompts you to read and acknowledge a legal statement. 
5. Read the legal statement, click the selection box, and click I agree. The system updates the pending 
trading relationship. 
If the effective date of the relationship is the current day, the trading relationship becomes active within a 
few minutes. 


---

## Page 15

Trading Relationship Management User Guide 
Managing Relationships 15 
Add [[Broker]] IDs to an Existing Relationship 
You can use the spreadsheet upload process to add executing [[Broker]] IDs to existing relationships. 
1. Based on the template, create a spreadsheet that contains all of the required information for each 
relationship you want to update. 
To see additional tips, move your mouse over the heading for each column. 
2. Make sure that the following fields match the trading relationship that you want to update:  
• Trading Relationship Type 
• Submitting Party  
• QSR/SR [[participant]] [[ID]] 
• Correspondent [[participant]] [[ID]] 
3. Create a separate row for each executing [[Broker]] [[ID]] that you want to add.  
Each row should contain the same information, except for the following: 
• Role: This is the role (QSR, SR, or CRSP) for executing [[Broker]] [[ID]] on this row. 
• Executing [[Broker]] [[ID]]: This identifies the executing [[Broker]]. 
• Executing [[Broker]] Effective Date: This is the effective date for the executing [[Broker]] [[ID]].  
4. Save the spreadsheet as either an .xls or .xlsx file. 
 
  

---

## Page 16

Trading Relationship Management User Guide 
Search Relationships 16 
SEARCH RELATIONSHIPS 
You can search for your trading relationships linked to the current or selected [[participant]]. Search returns a list 
of all relationships depending upon your search criteria. You can search by: 
• Trading Relationship Criteria – which includes the ability to search by: 
• Trading Relationship Type 
• Requested Effective Date 
• Trading Relationship Status 
• QSR Execution Platform 
• Actual Effective Date 
• Executing [[Broker]] [[ID]] for Trade Editing 
• Special Representative -which includes the ability to search by: 
• [[participant]] [[ID]] 
• Executing [[Broker]] [[ID]] 
• [[participant]] Name 
• Correspondent/Authorized [[participant]] Information 
• [[participant]] [[ID]] 
• Executing [[Broker]] [[ID]] 
• [[participant]] Name 

---

## Page 17

Trading Relationship Management User Guide 
Search Relationships 17 
 


---

## Page 18

Trading Relationship Management User Guide 
Rejecting Pending Relationships 18 
REJECTING PENDING RELATIONSHIPS 
You can reject pending relationships that have been submitted by your counterparty. Reject all executing 
brokers, or only reject some, approve some, and/or leave some for further research. 
Note:  
For relationships where one or both participants are sponsored participants, the sponsors must approve new relationships. 
Sponsors may also reject the pending relationship. For more information about sponsors, see Roles. 
1. From the Dashboard page, click a [[participant]] [[ID]] for any trading relationship that appears in the Pending 
Approval status. 
The Trading Relationship detail page appears. 
Note:  
You can also use the search function to display relationships in the Pending Approval status. For more information, 
see Searching Relationships. 
2. To reject the relationship for all executing [[Broker]] IDs, explain the reason for the rejection in the Rejection 
Comments field and click Reject All. 
 
3. To reject a specific executing [[Broker]] [[ID]], in either the Correspondent or Qualified Special 
Representative/Special Representative section: 
a. Click the selection box for that [[Broker]] [[ID]]. 
b. In the Reject Comments field, explain the reason for the rejection, and then click Reject. 
 
4. To reject all [[Broker]] IDs, in either the Correspondent or Qualified Special Representative/Special 
Representative section: 
a. Explain the reason for the rejection in the Reject Comments field. 
b. Click the All check box, and then click Reject. 


---

## Page 19

Trading Relationship Management User Guide 
Spreadsheet Upload Process 19 
SPREADSHEET UPLOAD PROCESS 
To upload a Microsoft Excel spreadsheet containing new trading relationships and updates to existing 
relationships: 
Note: 
Your spreadsheet cannot exceed 1000 rows. 
1. Start with the most recent version of the spreadsheet template. 
 
For more information, see Start with the Most Recent Spreadsheet Template. 
2. Enter your relationship details. 
 
 
For more details, see Preparing the Upload Spreadsheet and Example Spreadsheets. 


---

## Page 20

Trading Relationship Management User Guide 
Spreadsheet Upload Process 20 
3. Save the spreadsheet as an Excel Workbook file. 
 
4. From the Upload Trading Relationship page, submit the upload spreadsheet you have created. For more 
information, see Uploading the Spreadsheet. 
 
5. If the system rejects your spreadsheet, investigate the error, correct it, and then submit the spreadsheet 
again. For more information, see Reviewing and Correcting Upload Errors. 
  


---

## Page 21

Trading Relationship Management User Guide 
Spreadsheet Upload Process 21 
Start with the Most Recent Spreadsheet Template 
To prepare spreadsheets for upload, you need the most recent version of the spreadsheet template. 
1. From the main menu, click Upload Tool. 
2. Click the Click to download Spreadsheet Template link. 
 
Your computer's response depends on which browser software you are using and how that browser is 
configured. In the most typical setup, you are prompted to either open or save the file. 
3. To open the file, click Open. 
4. To save the file, click Save. 
Preparing the Upload Spreadsheet 
After you have downloaded and saved the spreadsheet template (see Start with the Most Recent  Spreadsheet 
Template), you are ready to create new spreadsheets containing new relationships and updates to existing 
relationships. 
  


---

## Page 22

Trading Relationship Management User Guide 
Spreadsheet Upload Process 22 
About the Spreadsheet Template 
After you open the spreadsheet template, you'll notice that it is color coded. 
 
Here is a description for what each color signifies. 
 
Blue fields are mandatory. If no data is entered in these fields, the file 
is rejected. 
 
 
Orange fields are conditional. These fields may be required depending 
on information you have entered in other related fields. 
 
 
Gray fields are reserved for future use. [[DO]] not enter information in 
these fields. 
To display hints for a column, move your mouse over the column heading. 


---

## Page 23

Trading Relationship Management User Guide 
Spreadsheet Upload Process 23 
 
Tips 
• [[DO]] not insert rows above row 3 (the column headings). 
• [[DO]] not modify the order of the columns. 
• [[DO]] not modify the format of the columns. 
• You can insert a small number of rows within the spreadsheet, if desired, for organizational and readability 
purposes. 
• Your spreadsheet can have a maximum of 1000 rows. 
• Use the drop-down menus where available. 
• For date fields, the required format is MM/DD/YYYY. 
• For [[participant]] [[ID]] fields, leading zeros are not required. For example, you can enter 000000123 as simply 
123. 
  


---

## Page 24

Trading Relationship Management User Guide 
Spreadsheet Upload Process 24 
Example Spreadsheets 
The examples below demonstrate completed spreadsheets for various scenarios. 
Example One 
A Correspondent relationship, submitted by the special representative, without executing [[Broker]] IDs. In this 
example, the highlighted area shows a single relationship. . When the Executing [[Broker]] [[ID]] for Trade Editing 
field is set to N, executing [[Broker]] IDs are not required. 
 
Example Two 
A Correspondent relationship, submitted by the special representative, with executing [[Broker]] IDs. In this 
example, the highlighted area shows a single relationship, with one [[Broker]] [[ID]] for the correspondent side, and 
one [[Broker]] [[ID]] for the special representative side. When the Executing [[Broker]] [[ID]] for Trade Editing field is set to 
Y, there must be at least one [[Broker]] [[ID]] per side of the relationship. Use the Role field to specify the side for 
each [[Broker]] [[ID]]. 
 
  


---

## Page 25

Trading Relationship Management User Guide 
Spreadsheet Upload Process 25 
Example Three 
A QSR relationship, submitted by the QSR, without executing [[Broker]] IDs. In this example, the highlighted area 
shows a single relationship. When the Executing [[Broker]] [[ID]] for Trade Editing field is set to N, executing [[Broker]] 
IDs are not required. 
 
Example Four 
A QSR relationship, submitted by the QSR, with executing [[Broker]] IDs. In this example, the highlighted areas 
show two separate relationships. Both relationships include two [[Broker]] IDs for the QSR side, and one [[Broker]] [[ID]] 
for the correspondent side. When the Executing [[Broker]] [[ID]] for Trade Editing field is set to Y, there must be at 
least one [[Broker]] [[ID]] per side of the relationship. Use the Role field to specify the side for each [[Broker]] [[ID]]. 
 
Example Five 
The correspondent adds [[Broker]] IDs to an existing QSR relationship. In this example, one new [[Broker]] [[ID]] is 
being added to the correspondent side of the relationship, and one new [[Broker]] [[ID]] is being added to the QSR 
side of the relationship. Use the Role field to specify the side of the relationship for each [[Broker]] [[ID]]. 
 


---

## Page 26

Trading Relationship Management User Guide 
Uploading Spreadsheets 26 
UPLOADING SPREADSHEETS 
Prepare your spreadsheet. See Preparing the Upload Spreadsheet. Next, upload the spreadsheet through the 
Trading Relationship Management web interface. 
1. From the main menu, click Upload Tools. 
The Upload Trading Relationship Tools page appears. 
2. Click Browse. 
 
3. [[Locate]] and select your spreadsheet. 
4. Click Submit. 
The system prompts you to read and acknowledge a legal statement. 
5. Read the statement, click the selection box, and then click I agree. 
The system validates your spreadsheet and either accepts it or rejects it. The results appear at the bottom 
of the page. 
For accepted spreadsheets, the system displays a link to your spreadsheet, and displays a status of 
Completed. 
For rejected spreadsheets, the system displays a link to your spreadsheet, and displays a status of 
Spreadsheet contains errors. The system also displays an   information icon in the Details column. Click 
the icon to display error messages. For more information, see Reviewing and Correcting Upload Errors. 
  


---

## Page 27

Trading Relationship Management User Guide 
Uploading Spreadsheets 27 
Displaying Uploaded Spreadsheets 
You can use the spreadsheet search to display both accepted and rejected spreadsheets for a specific date 
range. 
Notes: 
When you submit a spreadsheet, the system either accept or reject it and display the results at the bottom of the page. 
The system also displays rejected spreadsheets on the Dashboard page. 
1. From the main menu, click Upload Tools. 
The Upload Trading Relationship Tools page appears. 
2. In the Search Spreadsheet section, in the From and To fields, enter a date range for your search. 
 
You can use the calendar tool  to select the dates. 
3. Click Search. 
The system displays the spreadsheets that you have uploaded that fall within the date range you selected. 
4. To open a spreadsheet, click the spreadsheet name in the Trading Relationship Spreadsheet column. 
5. To display the error messages for spreadsheets that the system has rejected, click the  Details icon. 
  


---

## Page 28

Trading Relationship Management User Guide 
Uploading Spreadsheets 28 
Reviewing and Correcting Upload Errors 
To review and correct upload errors: 
1. Access the spreadsheet you want to work with. 
When spreadsheets are rejected during the upload process, the system displays a link to your 
spreadsheet, and displays a status of Spreadsheet contains errors. 
 
 
You can access rejected spreadsheets through the Dashboard page or through the spreadsheet search. See 
Displaying Uploaded Spreadsheets. 
2. To display error messages for a spreadsheet, click the  information icon. The Spreadsheet Errors page 
appears: 
 
3. To display the spreadsheet, click the spreadsheet name from the Trading Relationship Spreadsheet 
column. 
 
  


---

## Page 29

Trading Relationship Management User Guide 
Uploading Spreadsheets 29 
Correct the errors and resubmit the spreadsheet. The following table shows a list of Common Spreadsheet 
Errors and their solutions: 
Issue Solution 
Invalid information Resubmit with valid data. This could be due to numeric information appearing where alpha 
was expected, alpha where numeric was expected, etc. 
Missing information Enter all required fields. 
Only one side of the 
relationship submitted 
Enter all required fields, including the QSR/SR and Correspondent [[participant]] IDs. 
[[participant]] [[ID]] does not exist Resubmit the spreadsheet with valid [[participant]] IDs. 
Missing executing [[Broker]] IDs If the Executing [[Broker]] [[ID]] for Trade Editing column is set to Y, enter at least one 
executing [[Broker]] [[ID]] for each side of the relationship. 

---

## Page 30

Trading Relationship Management User Guide 
Searching Relationships 30 
SEARCHING RELATIONSHIPS 
As a qualified special representative, special representative, or correspondent with appropriate system 
privileges, you can search trading relationships in which your firm participates. 
Sponsors with appropriate system privileges can search the trading relationships that they sponsor. You can 
download your search results. 
1. From the main menu, click Search Relationship. 
The Search Trading Relationship page appears. Use this page to enter criteria for your search. 
From the Trading Relationship Criteria section, you can limit your search to specific trading
 relationships 
by entering criteria such as the relationship type, status, effective date (requested and/or actual), QSR 
execution platform, and/or the executing [[Broker]] [[ID]]. 
2. In either the Qualified Special Representative/Special Representative Information section or the 
Correspondent section, click the  icon. 
The system pre-fills the [[participant]] Name and [[participant]] [[ID]] fields in that section with your information, 
based upon the currently selected [[participant]] account. 
3. You can further refine your search by completing any of the remaining fields on the page. 
4. Click Search. 
The system displays your search results at the bottom of the page. 
5. To download your search results in the Microsoft Excel spreadsheet format, click the   Excel icon. 
6. To view details for a specific trading relationship, click the button in the Select column for that relationship, 
and click Show Details. 
The details page for that relationship appears. 
Downloading Search Results 
After you perform a search, you can download your results in the Microsoft Excel format. 
1. Perform a search. 
For more information, see Searching Relationships. 
2. Click the Export to: icon  located just above your search results on the right. 
To view data downloaded in the Microsoft Excel format, you need to have Microsoft Excel (or a similar 
application capable of displaying spreadsheet data) installed on your computer. 
After you click the Export to: icon , your computer's response depends on which browser you are using 
and how that browser is configured. In the most typical setup, you are prompted to either open or save the 
file. 
3. To open the file, click Open. 
4. To save the file for later use, click Save. 


---

## Page 31

Trading Relationship Management User Guide 
Deleting Active Relationships 31 
DELETING ACTIVE RELATIONSHIPS 
You can delete relationships in which your firm participates that are in active status. Approval by your 
counterparty is not required. You can delete the entire relationship or delete any of the executing [[Broker]] IDs 
within the relationship. 
Note:  
Deleting active trading relationships must be approved by an individual with supervisor-level privileges within your firm. 
Deleting executing brokers for active trading relationships must also be approved by an individual with supervisor level 
privileges within your firm. 
When an existing relationship is deleted and approved by the QSR/SR or correspondent, the relationship 
becomes inactive and any trades submitted with the deleted relationship is pended until end of the day. 
With appropriate system privileges, you can delete active trading relationships. Deleting active trading 
relationships must be approved by an individual with supervisor-level privileges within your firm. You can also 
delete executing [[Broker]] IDs for a trading relationship in the Active status.  
Note: 
An individual with supervisor-level privileges within your firm can either approve or reject the delete request 
You cannot delete relationships that you have created and is in the Pending Approval status. If you need to 
remove a trading relationship in the Pending Approval status, you can [[DO]] one of the following actions: 
• Ask the counterparty to reject the relationship. See Rejecting Pending Relationships. 
• Ask the [[DTCC]] Account Administration to delete the relationship. 
To delete active trading relationships: 
1. Use the search function to display the detail page for the active relationship you want to delete: 
• Perform a search for trading relationships in the Active status. For more information, see Searching 
Relationships. 
• In the search results, for each trading relationship you want to work with, click the selection box and 
click Show Details. 
The detail page for that trading relationship appears. 
• Click Update. 
2. In the Deletion Effective Date field near the bottom of the page, provide an effective date for the delete. 
You can use the calendar tool  to select a date. 
3. Click Delete Relationship. 
The system prompts you to confirm the delete. 
4. Click Ok. 
The Trading Relationship is moved to the Pending Delete Approval status. 
  


---

## Page 32

Trading Relationship Management User Guide 
Deleting Active Relationships 32 
To delete an executing [[Broker]] [[ID]]: 
1. Click the selection box for that [[Broker]] [[ID]]. 
2. Select a Delete Effective Date for that [[Broker]] [[ID]]. 
3. Click Delete Executing [[Broker]]. 
To delete all executing [[Broker]] IDs for either side of the trading relationship: 
1. Click the All selection box. 
2. Provide a Delete Effective Date for each [[Broker]] [[ID]]. 
3. Click Delete Executing [[Broker]]. 
 
To add an executing [[Broker]] [[ID]]: 
1. In an empty row, type the [[Broker]] [[ID]] and select an Effective Date. 
Click Add to create additional rows as needed. 
Click Remove to take away unneeded rows. 
Notes: 
You can use the calendar tool  to select dates. For more information, see About Effective Dates. If you are removing 
all executing [[Broker]] IDs for either side of the relationship, you can enter a Delete. 
The Effective D ate, at the bottom of the page, applies to all executing [[Broker]] IDs that you are removing. 
  


---

## Page 33

Trading Relationship Management User Guide 
Deleting Active Relationships 33 
Approving or Rejecting Delete Active Relationship Requests 
Deleting active trading relationships must be approved by an individual with supervisor-level privileges within 
your firm. Deleting executing brokers for active trading relationships must also be approved by an individual 
with supervisor-level privileges within your firm. Individuals with supervisor-level privileges within your firm can 
also reject requests to delete active relationships. 
To approve or reject a delete active relationship request: 
Note:  
If an intraday delete is not approved on the day it was entered, the request carry over on subsequent days until it is deleted 
or rejected. 
1. If necessary, click Dashboard on the main menu. 
The dashboard displays all pending relationships for your account. 
2. Click the [[participant]] [[ID]] for the relationship in the Pending Delete Approval status that you want to either 
approve or reject. 
3. To approve the deletion of the entire trading relationship, or to approve all deletions of executing [[Broker]] 
IDs for the trading relationship, click Approve All. 
 
4. To reject the deletion of the entire trading relationship or to reject all deletions of executing [[Broker]] IDs for 
the trading relationship, click Reject All. 
 


---

## Page 34

Trading Relationship Management User Guide 
Deleting Active Relationships 34 
To approve or reject the deletion of specific executing [[Broker]] IDs within either the Qualified Special 
Representative/Special Representative or Correspondent section of the relationship, click the selection 
box for those IDs and click Approve or Reject. 
 
To approve or reject the deletion of all executing [[Broker]] IDs within either the Qualified Special 
Representative/Special Representative or Correspondent section of the relationship, click the All 
selection box in that section and click Approve or Reject. 
If the requested effective date is the current date or prior, the delete is effective within minutes. If the requested 
effective date is in the future, the delete is effective on the first business day equal to or after the requested 
effective date. 
Updating Relationships 
You can update any of the information for relationships that you have saved but have not yet submitted. After 
the data has been submitted, you can change the executing [[Broker]] requirement and add executing brokers 
with appropriate effective dates. Updates must be approved by your counterparty to be applied to the trading 
relationship. 
Note:  
Sponsors, acting on behalf of the participants they sponsor, can also update trading relationships. For relationships where 
one or both participants are sponsored participants, the sponsors must approve updates to existing relationships. Sponsors 
may also reject updates to existing relationships. For more information about sponsors, see Roles. 
After data has been submitted, you can: 
• Change the executing [[Broker]] requirement. 
• Add executing brokers with appropriate effective dates. 
To update relationships: 
Updates for relationships that you have submitted must be approved by your counterparty to be applied to the 
trading relationship. 
1. Perform a search for the trading relationship you want to update. 
For more information, see Searching Relationships. 
2. In the search results, for the trading relationship you want to work with, click the selection box and click 
Show Details. 
3. From the details page, click Update. 
4. Modify the trading relationship as needed. 


---

## Page 35

Trading Relationship Management User Guide 
Deleting Active Relationships 35 
If you are working with a trading relationship that you have previously saved but have not submitted, you 
can modify any editable field. If this is a trading relationship that has been submitted or is active, you can 
modify the executing [[Broker]] [[ID]] information. For information about modifying your executing [[Broker]] IDs, 
see the Modifying Executing [[Broker]] IDs table. 
5. Click Submit. 
The system prompts you to read and acknowledge a legal statement. 
6. Read the statement, click the selection box, and click I agree. 
Retracting a Pending Relationship Request 
You can retract trading relationship requests that your firm submitted and that are pending with other system 
users. 
To retract a pending relationship request: 
1. Login to Trading Relationship Management System. 
2. Select your [[participant]] [[ID]]. 
3. Click Go. 
4. Click a hyperlink from the Trading Relationships Pending with Others section. 
5. When the detailed page opens, click Retract. 


---

## Page 36

Trading Relationship Management User Guide 
Deleting Active Relationships 36 
 


---

## Page 37

Trading Relationship Management User Guide 
Managing Contacts 37 
MANAGING CONTACTS 
Viewing Group Contact Information 
You can view your firm’s user contact information from the Contacts tab that displays a page that allows you to: 
• Search your contacts. 
• Add a new contact. 
• Select and update a contact. 
• Select and delete a contact. 
• Select and view a contact. 
 
  


---

## Page 38

Trading Relationship Management User Guide 
Managing Contacts 38 
Updating Contact Information 
You can add, update, delete, or view information in your firm’s contact list from the Contacts tab from the main 
menu. Within the Contacts tab, you are able to update the following information: 
• Contact Type – group or individual 
• Name 
• Phone Number 
• Email Address 
• Message Type 
• Relationship Type – QSR/Correspondent Clearing 
• Share Contact Information –allows you to expose your contact information to system users at other firms. 
 
  


---

## Page 39

Trading Relationship Management User Guide 
Managing Contacts 39 
Search for Contacts 
You can search Trading Relationship Management contacts based on different search criteria. After searching, 
a list of all contact information that fit your criteria is returned along with who have opted-in to share their details. 
To search contacts: 
1. From the main menu, click the Contacts tab. 
2. From the submenu, click the Search Contacts tab. 
3. Enter your [[participant]] [[ID]] or [[participant]] Name. 
Note:  
You can select Starts With or Contains when searching by [[participant]] Name/ 
4. Click Search. 
 
5. When the desired [[participant]] appears in the [[participant]] Information section, click Retrieve Contacts. 
 


---

## Page 40

Trading Relationship Management User Guide 
Viewing the Affiliates List 40 
VIEWING THE AFFILIATES LIST 
You can view the affiliates list from the Affiliates tab. The list of affiliates ([[NSCC]] Participants) that share the 
same Global Ultimate Parent (GUP) for the logged-in [[participant]] appears. 
 
 


---

## Page 41

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the [[DTCC]] brand name by certain affiliates of The Depository Trust & 
Clearing Corporation ([[DTCC]]).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 26, 2022 
Publication Code: NSCC111 
Service: Equities Clearing 
Title: Trading Relationship Management User Guide 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 