---
title: "MF Info Xchange Data Dictionary"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfix_data_dictionary_mfs342_20240108.pdf"
pages: 222
size: "2882.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MF Info Xchange Data Dictionary

**Original File:** [mfix_data_dictionary_mfs342_20240108.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfix_data_dictionary_mfs342_20240108.pdf)  
**Category:** Other  
**Total Pages:** 222  
**File Size:** 2882.1 KB  

---

## Page 1

 
 
         
 
 
MF INFO XCHANGE 
DATA DICTIONARY 
JANUARY 8, 2024 
 

---

## Page 2

 
 
REVISION HISTORY 
Date Revision 
December 18, 2023 Revised to reference enhancements listed in Important Notice a9349 (dated November 
15, 2023). 
Updated the following sections: 
• “Create Notification Step 1”. Updated description for “Event Status” field. 
• “Create Notification Step 2 – [[Dividend]]/Capital Gain Schedule”.   Updated “Change 
Indicator” field name in the “UI Field Name” column. 
• “Create Notification Step 2 – Fund Reopening“. Updated description for “Reopening 
Fund Trade Date for new accounts”, “Reopening Fund Trade Date for Existing 
Investors Subsequent Buys/Exchanges In” and “Reopening Fund Trade Date for 
Sells” fields. 
• “Create Notification Step 2 – Interval/Tender Fund Transaction Schedule”. Updated 
“Change Indicator” field name in the “UI Field Name” column. 
• “Create Notification Step 2 – Share Class Conversion/Exchange”. Updated 
description for “Conversion Date”, “Networking Share Class Conversion Activity 
Records (F55) Date”, “Anticipated Extended NAV availability date” and “Client 
Notification Date” fields.  
July 3, 2023 Updated the following sections: 
• “Overview”. Added additional standalone fields: “clientNb”, “companyName”, 
“recipientClientNb”, “recipientName”, “distributionId”, “receivedDate”, “recipientClientNb”, 
“recipientName”, “accountName”, “clienNb”, “distributionStatus”, “submittedBy”, 
“dateSubmitted”, “distributionDate”. 
• “Create Notification Step 2 – Fund Closure – Hard Close”. Added “Fund Number” field. 
• “Create Notification Step 2 – Fund Closure - [[liquidation]]”. Added “Fund Number” field. 
• “Create Notification Step 2 – Fund Closure – Soft Close”. Updated description for 
“allowableExceptionNew” and “allowableException” fields. 
• “Create Notification Step 2 – Fund Merger”. Added “From Fund Number” field. 
• “Create Notification Step 2 – Fund Name Change”. Added “From Fund Number” field. 
• “Create Notification Step 2 – Fund Reopening”. Added “Fund Number” and “The fund 
prospectus has been stickered or reprinted” fields. Updated “Reopening fund trade date 
for new accounts” and “Reopening fund trade date for existing investors subsequent 
buys/exchanges in” fields.  
• “Create Notification Step 2 – Interval/Tender Fund Transaction Schedule”. Added “Year” 
field. 
• “Create Notification Step 2 – Issue Notification”. Added “Issue Type” field. 

---

## Page 3

MF INFO XCHANGE 
Overview 3 
 
 
  
Date Revision 
• “Create Notification Step 2 – New Fund/New Share Class Launch”. Added “Notification” 
field. 
• “Create Notification Step 2 – Purchase Maximum Change”. Added “Fund Number” field. 
• “Create Notification Step 2 – Purchase Minimum Change”. Added “Fund Number” field. 
• “Create Notification Step 2 – Share class Conversion/Exchange”. Added “Number of 
months/years [[shares]] must age” field. Updated description for the “sharesMy” field.  
• “Create Notification Step 2” – Share Split”. Added “shareSplitType” field. 
• “Create Notification Step 2 – [[transfer agent]] Change/Fund Acquisition”. Added 
notificationType” field. Updated description for “acceptedOrRejected” and “[[settlement]]” 
fields. 
• “Create Notification Step 2 – Unscheduled Market Close”. Added “eventName” field. 
Updated description for “eFundName” and “eSecIssueId” fields. 
• “Create Notification Step 4 (Submitter = Firm, Event Type = Large Trade Notification)”. 
Updated description for “Designated Recipients” field. 
• “Create Notification Step 4  - US Holiday Announcement”. Added “holiday” field. 
December 14, 2022 Updated “Create Notification Step 2” sections with “rowId” and “status” fields. 
March 23, 2022 Updated “Create Notification Step 1” section. Updated “UI Definition” and “API Definition” 
fields for Effective Date and Effective Time fields. 
February 17, 2022 Updated “Create Notification Step 2 – Large Trade Notification” section. Removed a duplicate 
“Fund [[DTCC]] [[participant]] Number” field. 
November 17, 2021 Initial publication 
  

---

## Page 4

MF INFO XCHANGE 
Overview 4 
 
TABLE OF CONTENTS 
Overview .................................................................................................................................................................... 5 
Create Notification Step 1 .......................................................................................................................................... 7 
Create Notification Step 2 -  Account History Purge ................................................................................................ 10 
Create Notification Step 2 -  Benchmark Change .................................................................................................... 18 
Create Notification Step 2 -  [[Dividend]]/Capital Gain Schedule ................................................................................. 20 
Create Notification Step 2 -  Expense Ratio Change ............................................................................................... 26 
Create Notification Step 2 -  Fee/Breakpoint Change .............................................................................................. 29 
Create Notification Step 2 -  Fund Closure – Hard Close ........................................................................................ 68 
Create Notification Step 2 -  Fund Closure – [[liquidation]] ......................................................................................... 72 
Create Notification Step 2 -  Fund Closure – Soft Close ......................................................................................... 81 
Create Notification Step 2 -  Fund Merger ............................................................................................................... 95 
Create Notification Step 2 -  Fund Name Change ................................................................................................. 106 
Create Notification Step 2 -  Fund Reopening ....................................................................................................... 109 
Create Notification Step 2 -  Interval/Tender Fund Transaction Schedule ............................................................ 112 
Create Notification Step 2 - Issue Notification ....................................................................................................... 118 
Create Notification Step 2 -  Large Trade Threshold Change ............................................................................... 122 
Create Notification Step 2 -  Large Trade Notification ........................................................................................... 125 
Create Notification Step 2 - New Fund/New Share Class Launch ........................................................................ 130 
Create Notification Step 2 -  Price/Rate Error ........................................................................................................ 133 
Create Notification Step 2 -  Prospectus Change .................................................................................................. 142 
Create Notification Step 2 -  Purchase Maximum Change .................................................................................... 145 
Create Notification Step 2 -  Purchase Minimum Change ..................................................................................... 148 
Create Notification Step 2 -  Share Class Conversion/Exchange .......................................................................... 152 
Create Notification Step 2 -  Share Class Eligibility Change ................................................................................. 156 
Create Notification Step 2 -  Share Split ................................................................................................................ 159 
Create Notification Step 2 -  Subadvisor Change .................................................................................................. 168 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition ................................................................ 170 
Create Notification Step 2 -  Unscheduled Market Close (UMC) ........................................................................... 188 
Create Notification Step 2 -  Upcoming [[Proxy]] ....................................................................................................... 204 
Create Notification Step 2 -  US Holiday Announcement ...................................................................................... 207 
Create Notification Step 4 (Submitter = Fund) ....................................................................................................... 218 
Create Notification Step 4 (Submitter = Firm, Event Type = Large Trade Notification)  ......................................... 220 
 

---

## Page 5

MF INFO XCHANGE 
Overview 5 
 
 
OVERVIEW 
MF Info Xchange facilitates and centralizes the delivery and receipt of time-critical notifications, including 
corporate actions, service disruptions and other critical alerts, which typically require communications between 
funds and intermediaries. The service facilitates two-way real time communication. 
Applying technology to notifications eliminates the manual email, phone call and fax process. MF Info Xchange 
effectively standardizes, streamlines, and reduces risk throughout the communication process. The service also 
includes an event calendar for receivers to view date-critical events, upcoming informational events, and historical 
details. 
MF Info Xchange features an intuitive and dynamic web interface and provides real -time notifications with a 
complete audit trail. Access to event data is readily available, on-demand, through the user interface (UI) as well 
as the API enabled platform. 
Note: This document provides a data dictionary of the data elements corresponding to Steps1, 2 and 4 of the 
notification in the notification submitter’s UI screen (for each MF Info Xchange event type) – notification/event type 
data elements on the Excel file generated by the system. For the list of all additional fields returned by MF Info 
Xchange API calls, please refer to the MF Info Xchange API Capabilities – Technical Guide.  
 
 
 
 
• Step 1 – initialStep (API term).  
Note:  
“eventType” field is a Step 1 field in the UI, however it is not included in the “initialStep” on the API endpoints. 
This field will appear as a standalone field in the API endpoints and will not be included with the “initialStep” 
fields. 
• Step 2 – notificationData (API term) 
• Step 4 – finalizationStep (API term) 
Event [[ID]] (“eventId” field, A/N, max size 255 char) is a unique number generated and assigned to the notification 
by the MF Info Xchange system. This field will appear as a standalone field in the API endpoints (will not be 
included in any of the above sections).  
Additional standalone fields returned by “Notification Search” API endpoints: 
• “clientNb” (A/N, max size 8 char) and “companyName” (A/N, max size 256 char) – these fields identify the 
submitter of the notification ([[DTCC]] [[participant]] number and company name). 


---

## Page 6

MF INFO XCHANGE 
Overview 6 
 
• “recipientClientNb” (A/N, max size 8 char) and “recipientName” (A/N, max size 256 char) – these fields 
identify the receiver of the notification ([[DTCC]] [[participant]] number and company name). 
• distributionId (A/N, max size 255 char) - Unique number generated and assigned to each successful 
distribution of a notification by the MF Info Xchange system. 
• “receivedDate” field (mm/dd/ccyy) – date when the notification was received.  
• “recipientClientNb” (A/N, max size 8 char) and “recipientName” (A/N, max size 256 char) - these fields identify 
the receiver’s information ([[DTCC]] [[participant]] number and company name). 
• “accountName” (A/N, max size 256 char) and “clientNb” (A/N, max size 8 char) fields identify notification 
submitter (company name and [[DTCC]] [[participant]] number) information. 
• “distributionStatus” field (A/N, max size 255 char) – distribution status of the notification. Will contain one of 
the following options:  
o Draft 
o Pending Distribution 
o Revised-Pending Distribution 
o Distributed 
• “distributionDate” field (mm/dd/ccyy) – date the notification was last distributed 
• “dateSubmitted” (mm/dd/ccyy) field – notification submission date, indicates the date of the most recent 
update to the notification  
• “submittedBy” field (A/N, max size 255 char) – provides user [[ID]] of the user who made the last update to the 
notification 
  

---

## Page 7

MF INFO XCHANGE 
Create Notification Step 1 7 
 
CREATE NOTIFICATION STEP 1 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
  
Event Type   eventType A/N R 255 Selection List of all 
Event Types 
(Notifications) 
 
Can select from drop 
down 
  
Event Type should 
be populated with 
one of the event 
types from 
description  
• Account/History Purge 
• Benchmark Change 
• [[Dividend]]/Capital Gain 
Schedule 
• Expense Ratio Change 
• Fee/Breakpoint Change 
• Fund Closure - Hard 
Close 
• Fund Closure – 
[[liquidation]] 
• Fund Closure – Soft Close 
• Fund Merger 
• Fund Name Change 
• Fund Reopening 
• Interval/Tender Fund 
Transaction Schedule 
• Issue Notification 
• Large Trade Notification 
• Large Trade Threshold 
Change 
• New Fund/New Share 
Class Launch 
• Price/Rate Error 
• Prospectus Change 
• Purchase Maximum 
Change 
• Purchase Minimum 
Change 
• Share Class 
Conversion/Exchange 
• Share Class Eligibility 
Change 
• Share Split 
• Subadvisor Change 
• [[transfer agent]] 
Change/Fund Acquisition 
• Unscheduled Market 
Close (UMC) 
• Upcoming [[Proxy]] 
• US Holiday 
Announcement  
Event Status  notificatio
nStatus 
A/N R 255 Selection List of all 
Event Status 
Can select from drop 
down 
Event Status should 
be populated with 
one of the event 
types from 
description 
 
• Initial Notification 
• Update 
• Reminder 
• Resolved 
• Cancelled 
• Closed 

---

## Page 8

MF INFO XCHANGE 
Create Notification Step 1 8 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
  
 
Newly created notifications must 
be set to “Initial Notification”. 
 
“Resolved” is allowed only for 
Event Type=Issue, not allowed for 
any other Event Types. 
Effective 
Date 
effectiveD
ate 
Date OC 10 This field is not 
allowed for Event 
Types: 
 - [[Dividend]]/ 
Capital Gain 
Schedule 
- Interval/ 
Tender Fund   
- Transaction    
Schedule 
- Price/Rate Error 
 and will not be 
displayed on the 
screen for these 
event types. 
 
This field is required 
for all other event 
types. 
Effective Date is 
required   
for all event types 
except: 
- [[Dividend]]/ 
 Capital Gain   
Schedule 
- Interval/ 
Tender Fund   
- Transaction    
Schedule 
- Price/Rate Error 
 
Effective Date is not 
allowed for the 
above referenced 
event types. 
 
 
 MM/DD/CCYY 
 
This date can be backdated 
 
Effective 
Time 
effectiveTi
me 
A/N OC 50 Can select from drop 
down 
  
This field is not 
allowed for Event   
  Types: 
 - [[Dividend]]/ 
Capital Gain 
Schedule 
- Interval/ 
Tender Fund   
- Transaction    
Schedule 
- Price/Rate Error 
 and will not be 
displayed on the 
screen for these 
event types.  
 
 This field is required 
for all other event 
types. 
Can be populated 
with Values from 
Description  
 
This field is not 
allowed for Event   
  Types: 
 - [[Dividend]]/ 
Capital Gain 
Schedule 
- Interval/ 
Tender Fund   
- Transaction    
Schedule 
- Price/Rate Error 
   
This field is required 
for all other event 
types. 
  
• Open Of Market 
• Close of Market 
• N/A 
Contact 
Name 
contactNa
me 
A/N OC 255     Required for Event Type Large 
Trade Notification 
 
Special characters allowed: 
`!@#%^&*()_+-[]\',./ 

---

## Page 9

MF INFO XCHANGE 
Create Notification Step 1 9 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
  
 
Contact 
Number 
contactNu
mber 
A/N OC 40     Required for Event Type Large 
Trade Notification 
 
Special characters allowed: 
!@#%^&*()_+-\ 
 
Contact 
Email 
contactE
mail 
A/N OC 100     Required for Event Type Large 
Trade Notification 
 
Email must be in the proper 
format: 
Recipient name@   Domain name 
  
where:  
Recipient Name - #$&*_+-/.'       
Domain - _. 
   
 
Cancellation 
Reason 
cancellati
onReason 
A/N OC 255     Required if  
Event Status = 'Cancelled', not 
allowed for all other Event 
Statuses. 
 
Special characters allowed 
 
Contact 
Company 
contactCo
mpany 
A/N OC 60   Required for Event Type Large 
Trade Notification, 
not allowed for all other Event 
Types 
 
Special characters allowed 
 
 
  

---

## Page 10

MF INFO XCHANGE 
Create Notification Step 2 -  Account History Purge 10 
 
CREATE NOTIFICATION STEP 2 -  ACCOUNT HISTORY PURGE 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
"Closed" 
Level 3 
accounts 
with an 
"Establish 
Date" on or 
before: 
clsdLevAcct
Date 
DATE O 10 calendar picker  MM/DD/CCYY 
This Date can be backdated 
"Closed" 
Level 3 
accounts 
with a"Last 
Activity 
Date" on or 
before: 
clsdLevAct
Date 
DATE  O 10 calendar picker  MM/DD/CCYY 
This Date can be backdated 
All other 
accounts 
with a 
closed 
status on 
or before: 
allOthAcct
Date 
DATE O 10 calendar picker  MM/DD/CCYY 
This Date can be backdated 
Applicable 
Matrix 
Levels: 
appMatLev
el 
A/N  O   Can select ‘All’, 
One or Multiple 
Options 
If All is selected, 
no other value 
can be selected 
Can be populated 
with 
Values 
from the 
Description Column 
(Can be populated 
with  
One or Multiple 
Options 
If All is selected, no 
other value can be 
selected) 
•All 
•Matrix Level 0 
•Matrix Level 3 
•Matrix Level 4 
Exceptions 
Apply 
accExcAppl
y 
A/N  O   User can change 
selection to ‘Yes’ 
If “Yes” is 
selected, then 
the Exception 
info table will be 
displayed on the 
UI. 
Can be populated 
with 
Values 
from the 
Description Column 
 
•No 
•Yes 
 
Defaults to ‘No’ 
Exception 
 
(Exceptions 
table 
allowed if 
accPurgeEx
ception 
A/N  O   One row is 
assigned to each 
selected [[Option]] 
 
User will click 
additional row if 
another  
Can be populated 
with 
Values 
from the 
Description Column 
 
• Omnibus 
• 529  
• LOI  
• Head of Chain for ROA 
• Other (specify) 

---

## Page 11

MF INFO XCHANGE 
Create Notification Step 2 -  Account History Purge 11 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Exceptions 
Apply = 
“Yes”) 
Exception will be 
selected. 
 
If “Yes” is 
selected in 
Exceptions Apply, 
then the 
Exception info 
table will be 
displayed on the 
UI. 
Repeating Data 
Exception – 
Other 
 
(Exceptions 
table 
allowed if 
Exceptions 
Apply = 
“Yes”) 
other A/N  O/C 100 If “Other” is 
selected in 
Exception, then 
this field is 
required. 
Else, this field is 
greyed out and 
cannot be 
populated 
 
If “Yes” is 
selected in 
Exceptions Apply, 
then the 
Exception info 
table will be 
displayed on the 
UI. 
Repeating Data 
If “Other” is 
selected in 
Exception, then this 
field is required 
Description for ‘Other’ 
exception 
 
Special characters allowed 
 
 
 
 
 
 
 
 
 
 
 
Comment 
 
(Exceptions 
table 
allowed if 
Exceptions 
Apply = 
“Yes”) 
comment A/N  O 1000    Comment for more 
information about selected 
Exception 
 
Special characters allowed 
 
N/A status 
 
(Exceptions 
table 
allowed if 
Exceptions 
Apply = 
“Yes”) 
A/N O/C 1 N/A Can be populated 
with values from 
the Description 
Column 
 
Not allowed on the 
“Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, "status" 
must be "I".  
If "rowId" is provided, 
"status" must be "D" or "U". 

---

## Page 12

MF INFO XCHANGE 
Create Notification Step 2 -  Account History Purge 12 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
endpoint if the 
respective table 
contains data. All 
existing rows within 
this table must be 
provided with the 
corresponding 
“rowId” and 
“status” fields.  
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Exceptions 
table 
allowed if 
Exceptions 
Apply = 
“Yes”) 
Integer O/C 11 N/A Not allowed on the 
“Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows within 
this table must be 
provided with the 
corresponding 
“rowId” and 
“status” fields. 
Required if 
status is one of the following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new row 
 
If "rowId" is blank, "status" 
must be "I".  
If "rowId" is provided, 
"status" must be "D" or "U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info Xchange. 
“Receive Notification Data for 
an Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the rowIds 
assigned to each row of the 
table 
Account 
History will 
be Purged 
fidAccounts A/N  O   Can select from 
drop down    
  
 Can be populated 
with 
Values 
from the 
Description Column 
 
[[Fiduciary]] Accounts  
•No 
•Yes 
Exceptions 
Apply 
fidExcApply A/N  O   Can select from 
drop down  
 
If “Yes” is 
selected in 
[[Fiduciary]] 
Exceptions Apply, 
then the 
Can be populated 
with 
Values 
from the 
Description Column 
 
[[Fiduciary]] Accounts Apply 
•No 
•Yes 
 
Defaults to ‘No’ 

---

## Page 13

MF INFO XCHANGE 
Create Notification Step 2 -  Account History Purge 13 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
[[Fiduciary]] 
Exceptions info 
table will be 
displayed on the 
UI. 
 
Defaults to ‘No’ 
 
Historical 
Purge Year 
histPurgFid
Year 
A/N  O/C 50   This field is required if 
Account History will be 
Purged  (Closed [[Fiduciary]] 
Accounts)  is “Yes” 
 
 
Special characters allowed 
 
Account 
History will 
be Purged 
nonFidAcco
unts 
A/N  O   Can select from 
drop down  
Can be populated 
with 
Values 
from the 
Description Column 
 
Non- [[Fiduciary]] Accounts 
Apply  
Values are: 
•No 
•Yes 
Exceptions 
Apply 
nonFidExcA
pply 
A/N  O   Can select from 
drop down  
  
If “Yes” is 
selected in Non-
[[Fiduciary]] 
Exceptions Apply, 
then the Non-
[[Fiduciary]] 
Exceptions info 
table will be 
displayed on the 
UI. 
Defaults to ‘No’ 
Can  be populated 
with 
Values 
from the 
Description Column 
 
Non- [[Fiduciary]] Accounts 
Apply   
•No 
•Yes 
  
Defaults to ‘No’ 
Historical 
Purge Year 
histPurgNo
nFidYear 
A/N  O/C 50      This field is required if  
Account History will be 
Purged (Closed Non-[[Fiduciary]] 
Accounts) is “Yes” 
 
Special characters allowed 
    
 
Exception 
 
([[Fiduciary]]  
Accounts 
Exceptions 
table 
available if  
fidExceptio
n 
A/N  O  100 If “Yes” is 
selected in 
[[Fiduciary]] 
Exceptions Apply, 
then the 
[[Fiduciary]] 
Exceptions info 
table will be 
 If “Yes” is selected 
in [[Fiduciary]] 
Exceptions Apply, 
then the [[Fiduciary]] 
Exceptions can be 
populated 
[[Fiduciary]] Exception  

---

## Page 14

MF INFO XCHANGE 
Create Notification Step 2 -  Account History Purge 14 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Exceptions 
Apply = 
‘Yes’ 
For Closed 
[[Fiduciary]] 
Accounts  
) 
   
 
displayed on the 
UI  
Comment 
 
([[Fiduciary]]  
Accounts 
Exceptions 
table 
available if  
Exceptions 
Apply = 
‘Yes’ 
For Closed 
[[Fiduciary]] 
Accounts  
) 
 
fidCommen
t 
A/N  O  1000  If “Yes” is 
selected in 
[[Fiduciary]] 
Exceptions Apply, 
then the 
[[Fiduciary]] 
Exceptions info 
table will be 
displayed on the 
UI 
If “Yes” is selected 
in [[Fiduciary]] 
Exceptions Apply, 
then the [[Fiduciary]] 
Exceptions can be 
populated 
Comment for more 
information about [[Fiduciary]] 
Exception 
  
 
Special characters allowed 
 
N/A 
 
status 
 
([[Fiduciary]]  
Accounts 
Exceptions 
table 
available if  
Exceptions 
Apply = 
‘Yes’ 
For Closed 
[[Fiduciary]] 
Accounts  
) 
 
A/N O/C 1 N/A Can be populated 
with values from 
the Description 
Column 
 
Not allowed on the 
“Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows within 
this table must be 
provided with the 
corresponding 
“rowId” and 
“status” fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, "status" 
must be "I".  
If "rowId" is provided, 
"status" must be "D" or "U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A 
 
rowId 
 
([[Fiduciary]]  
Accounts 
Exceptions 
Integer O/C 11 N/A Not allowed on the 
“Create a 
Notification” 
endpoint. 
 
Required if 
status is one of the following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  

---

## Page 15

MF INFO XCHANGE 
Create Notification Step 2 -  Account History Purge 15 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
table 
available if  
Exceptions 
Apply = 
‘Yes’ 
For Closed 
[[Fiduciary]] 
Accounts  
) 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows within 
this table must be 
provided with the 
corresponding 
“rowId” and 
“status” fields. 
 
Not allowed if  
status = ‘I’  - Insert new row 
 
If "rowId" is blank, "status" 
must be "I".  
If "rowId" is provided, 
"status" must be "D" or "U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info Xchange. 
“Receive Notification Data for 
an Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the rowIds 
assigned to each row of the 
table 
Exception nonFidExce
ption 
A/N   O 100 If “Yes” is 
selected in 
[[Fiduciary]] 
Exceptions Apply, 
then the Non-
[[Fiduciary]] 
Exceptions info 
table will be 
displayed on the 
UI. 
 If “Yes” is selected 
in Non-[[Fiduciary]] 
Exceptions Apply, 
then the Non-
[[Fiduciary]] Exceptions 
can be populated 
Non-[[Fiduciary]] Exception  
 
Special characters allowed 
 
Comment nonFidCom
ment 
A/N  O  1000  If “Yes” is 
selected in 
[[Fiduciary]] 
Exceptions Apply, 
then the Non-
[[Fiduciary]] 
Exceptions info 
table will be 
displayed on the 
UI 
If “Yes” is selected 
in Non-[[Fiduciary]] 
Exceptions Apply, 
then the Non-
[[Fiduciary]] Exceptions 
can be populated 
Comment for more 
information about Non-
[[Fiduciary]] Exception 
  
 
Special characters allowed 
 
N/A 
 
status 
 
(Non-
[[Fiduciary]]  
Accounts 
Exceptions 
A/N O/C 1 N/A Can be populated 
with values from 
the Description 
Column 
 
Not allowed on the 
“Create a 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  

---

## Page 16

MF INFO XCHANGE 
Create Notification Step 2 -  Account History Purge 16 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
table 
available if  
Exceptions 
Apply = 
‘Yes’ 
For Closed 
Non-
[[Fiduciary]] 
Accounts  
) 
 
 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows within 
this table must be 
provided with the 
corresponding 
“rowId” and 
“status” fields.  
If "rowId" is blank, "status" 
must be "I".  
If "rowId" is provided, 
"status" must be "D" or "U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A 
 
rowId 
 
([[Fiduciary]]  
Accounts 
Exceptions 
table 
available if  
Exceptions 
Apply = 
‘Yes’ 
For Closed 
Non-
[[Fiduciary]] 
Accounts  
) 
 
Integer O/C 11 N/A Not allowed on the 
“Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows within 
this table must be 
provided with the 
corresponding 
“rowId” and 
“status” fields. 
Required if 
status is one of the following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new row 
 
If "rowId" is blank, "status" 
must be "I".  
If "rowId" is provided, 
"status" must be "D" or "U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info Xchange. 
“Receive Notification Data for 
an Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the rowIds 
assigned to each row of the 
table 
Comments accntPurge
Comment 
A/N  O 4000    Comment field to be used for 
additional comments 
 
Special characters allowed 
 
 

---

## Page 17

MF INFO XCHANGE 
Create Notification Step 2 -  Account History Purge 17 
 
 
  

---

## Page 18

MF INFO XCHANGE 
Create Notification Step 2 -  Benchmark Change 18 
 
CREATE NOTIFICATION STEP 2 -  BENCHMARK CHANGE 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
To Tracking 
Index 
  
toTrackIn
dex 
A/N O 100   This field will accept special 
characters 
Temporary 
Tracking 
Index 
  
tempTrac
kIndex 
A/N O 100   This field will accept special 
characters 
Fund 
Number 
 
(Impacted 
Funds table) 
  
fundNum
ber 
A/N O 8    
Security 
Issue [[ID]] 
  
(Impacted 
Funds table) 
secIssueId A/N O  9    
Fund Name 
  
(Impacted 
Funds table) 
fundNam
e 
A/N O 60    
Ticker 
  
(Impacted 
Funds table) 
fundTicke
r 
A/N O 12    
Share Class 
 
(Impacted 
Funds table) 
  
fundShare
Class 
A/N O 20    
N/A 
 
status 
 
(Impacted 
Funds 
table) 
 
A/N O/C 1 N/A Can be populated 
with values from 
the Description 
Column 
 
Not allowed on the 
“Create a 
Notification” 
endpoint. 
 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, "status" must be 
"I".  

---

## Page 19

MF INFO XCHANGE 
Create Notification Step 2 -  Benchmark Change 19 
 
UI Field 
Name 
API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows within 
this table must be 
provided with the 
corresponding 
“rowId” and 
“status” fields.  
If "rowId" is provided, "status" must 
be "D" or "U". 
“status”=”D” or “U” is not allowed 
when “rowId” is blank. 
“status”=”I” is not allowed when 
“rowId” is provided. 
 
 
  
 
N/A 
 
rowId 
 
(Impacted 
Funds 
table) 
 
Intege
r 
O/C 11 N/A Not allowed on the 
“Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows within 
this table must be 
provided with the 
corresponding 
“rowId” and 
“status” fields. 
Required if 
status is one of the following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep existing row  
 
Not allowed if  
status = ‘I’  - Insert new row 
 
If "rowId" is blank, "status" must be 
"I".  
If "rowId" is provided, "status" must 
be "D" or "U". 
“status”=”D” or “U” is not allowed 
when “rowId” is blank. 
“status”=”I” is not allowed when 
“rowId” is provided. 
 
“rowId” values must correspond to 
the values assigned by MF Info 
Xchange. “Receive Notification Data 
for an Event [[ID]]” endpoint must be 
called to return the current version 
of the notification with the rowIds 
assigned to each row of the table 
Comment 
  
benchmar
kCommen
t 
A/N O 4000   This field will accept special 
characters 
  
  

---

## Page 20

MF INFO XCHANGE 
Create Notification Step 2 -  [[Dividend]]/Capital Gain Schedule 20 
 
CREATE NOTIFICATION STEP 2 -  [[Dividend]]/CAPITAL GAIN 
SCHEDULE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Quarter  quarter A/N OC  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
 
The Quarter for the 
schedule 
 
•1st Quarter 
•2nd Quarter 
•3rd Quarter 
•4th Quarter 
 
  
Not Allowed if Month   
populated 
 
Month 
  
month A/N OC  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
The Month for the 
schedule 
 
•January 
•February 
•March 
•April 
•May 
•June 
•July 
•August 
•September 
•October 
•November 
•December 
 
Not allowed  if Quarter  is  
populated 
 
 
Notification   notificatio
n 
A/N O  Can select one or 
more  values 
from drop down 
list 
Can be populated 
with 
Values 
from the 
Description 
Column 
 
Can populate one 
or more values 
from drop down 
list 
•[[Dividend]]/Capital Gain  
Distribution Schedule 
•Revised [[Dividend]]/Capital 
Gain Distribution Schedule 
•[[Dividend]] Declaration 
•Estimated Rates 
•Actual Rates 
•Distribution Frequency 
Changes 

---

## Page 21

MF INFO XCHANGE 
Create Notification Step 2 -  [[Dividend]]/Capital Gain Schedule 21 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Fund Number  
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
 
fundNum
ber 
A/N O 8    
Security Issue [[ID]]  
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
 
secIssueId A/N O  9    
Fund Name 
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
 
fundNam
e 
A/N O 60     
Ticker  
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
 
fundTicke
r 
A/N O 12     
 
Share Class 
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
 
fundShare
Class 
A/N O 20     
Change Indicator 
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
 
changeInd
icator 
A/N O  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
•Y   
•A  
•D 
Where:  
Y-change 
A-add 
D-delete  
Distribution Type  
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
 
distributio
nType 
A/N O  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
•[[Dividend]] 
•Capital Gain 
•Special [[Dividend]] 
Projected/Actual 
Indicator   
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
projected
ActualIndi
cator 
A/N O  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
•Projected  
•Actual 

---

## Page 22

MF INFO XCHANGE 
Create Notification Step 2 -  [[Dividend]]/Capital Gain Schedule 22 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
 
Record Date 
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
recordDat
e 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be backdated 
Ex Date 
 
([[Dividend]]/Capital 
Gain Schedule table) 
  
exDate Date O 10 Calendar picker  MM/DD/CCYY  
This date can be backdated 
Reinvest Date 
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
  
reinvestD
ate 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be backdated 
Payable Date 
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
  
payableDa
te 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be backdated 
Estimated/Actual 
Rate Indicator 
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
  
estimated
ActualRat
eIndicator 
 A/N O  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
•Estimated 
•Actual 
Rate Per Share 
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
  
ratePerSh
are 
A/N O 19   999999999.999999999 
Short Term 
  
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
 
shortTerm A/N O 19   999999999.999999999 
Long Term  
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
 
longTerm A/N O 19   999999999.999999999 

---

## Page 23

MF INFO XCHANGE 
Create Notification Step 2 -  [[Dividend]]/Capital Gain Schedule 23 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Total Capital Gains 
 
([[Dividend]]/Capital 
Gain Distribution 
Schedule table) 
  
totalCapit
alGain 
A/N O 19   999999999.999999999 
N/A 
 
  
  
status 
 
([[Dividend]]/
Capital 
Gain 
Distributio
n 
Schedule 
table) 
  
 
A/N O/C 1 N/A Can be populated 
with values from 
the Description 
Column 
 
Not allowed on 
the “Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows 
within this table 
must be provided 
with the 
corresponding 
“rowId” and 
“status” fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, "status" 
must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A 
  
rowId 
 
([[Dividend]]/
Capital 
Gain 
Distributio
n 
Schedule 
table) 
 
Intege
r 
O/C 11 N/A Not allowed on 
the “Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows 
within this table 
must be provided 
with the 
corresponding 
“rowId” and 
“status” fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new row 
 
If "rowId" is blank, "status" 
must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 

---

## Page 24

MF INFO XCHANGE 
Create Notification Step 2 -  [[Dividend]]/Capital Gain Schedule 24 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must be 
called to return the current 
version of the notification 
with the rowIds assigned to 
each row of the table 
Fund Number 
  
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
ddfcFund
Number 
A/N O 8    
Security Issue [[ID]] 
 
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
ddfcSecIss
ueId 
A/N O  9    
Fund Name 
 
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
ddfcFund
Name 
A/N O 60    
Ticker  
 
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
ddfcFund
Ticker 
A/N O 12    
Share Class 
 
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
  
ddfcFundS
hareClass 
A/N O 20    
Change Indicator  
  
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
ddfcChan
geIndicato
r 
A/N O  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
•Y   
•A  
•D 
Where:  
Y-change 
A-add 
D-delete 

---

## Page 25

MF INFO XCHANGE 
Create Notification Step 2 -  [[Dividend]]/Capital Gain Schedule 25 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Current Distribution 
Type  
 
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
 
currentDis
tributionT
ype 
A/N O  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
 •Daily Accrual 
 •[[Equity]] 
New Distribution 
Type  
 
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
newDistri
butionTyp
e 
A/N O  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
 •Daily Accrual 
 •[[Equity]] 
Distribution Change 
Effective Date 
  
distributio
nChangeE
ffectiveDa
te 
Date O 10 calendar picker    MM/DD/CCYY 
This date can be backdated 
 
Current Distribution 
Frequency  
 
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
currentDis
tributionF
requency 
A/N O  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
•Monthly 
•Quarterly 
•Semi-Annual 
•Annual 
New Distribution 
Frequency  
 
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
newDistri
butionFre
quency 
A/N O  Can select from 
drop down 
Can be populated 
with 
Values 
from the 
Description 
Column 
•Monthly 
•Quarterly 
•Semi-Annual 
•Annual 
Date(s) of Next 
Distribution 
 
([[Dividend]] 
Distribution  
Frequency Changes 
table) 
 
 
datesOfN
extDistrib
ution 
A/N O 250   Free form text no date 
validation 
 
Special characters allowed 
Comment notificatio
nCommen
t 
A/N O 4000    
 
Special characters allowed 
 
 

---

## Page 26

MF INFO XCHANGE 
Create Notification Step 2 -  Expense Ratio Change 26 
 
CREATE NOTIFICATION STEP 2 -  EXPENSE RATIO CHANGE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Security Issue [[ID]] 
  
(Impacted Funds 
table) 
secIssueId A/N O  9    
Fund Name 
 
(Impacted Funds 
table) 
  
fundName A/N O 60    
Ticker 
  
(Impacted Funds 
table) 
 
fundTicker A/N O 12    
Share Class 
  
(Impacted Funds 
table) 
fundShareCl
ass 
A/N O 20    
From Net Expense 
Ratio (%)  
 
(Impacted Funds 
table) 
fromNetExp
Ratio 
A/N O 11    99.99999999 
To Net Expense 
Ratio (%) 
  
(Impacted Funds 
table) 
toNetExpRa
tio 
A/N O 11    99.99999999 
From Gross Expense 
Ratio (%) 
 
(Impacted Funds 
table) 
  
fromGrsExp
Ratio 
A/N O 11    99.99999999 
To Gross Expense 
Ratio (%) 
 
(Impacted Funds 
table) 
  
toGrsExpRat
io 
A/N O 11    99.99999999 
N/A 
  
status 
 
(Impacted 
Funds table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  

---

## Page 27

MF INFO XCHANGE 
Create Notification Step 2 -  Expense Ratio Change 27 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A 
  
rowId 
 
(Impacted 
Funds table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 

---

## Page 28

MF INFO XCHANGE 
 28 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comment 
  
expenseRati
oComment 
A/N O 4000   Field length 4,000  
 
Special characters allowed 
 
  

---

## Page 29

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 29 
 
CREATE NOTIFICATION STEP 2 -  FEE/BREAKPOINT CHANGE 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
12b-1 Security Issue [[ID]]  
 
(Impacted Funds / 12b-1 
Fee Change table) 
b12SecI
ssueId 
A/N O  9    
12b-1 Fund Name  
 
(Impacted Funds / 12b-1 
Fee Change table)) 
b12Fun
dName 
A/N O 60    
12b-1 Ticker  
 
(Impacted Funds / 12b-1 
Fee Change table) 
b12Fun
dTicker 
A/N O 12    
12b-1 Share Class  
 
(Impacted Funds / 12b-1 
Fee Change table) 
b12Fun
dShare
Class 
A/N O 20    
12b-1 Change Type 
  
(Impacted Funds / 12b-1 
Fee Change table) 
change
Type 
A/N O  Can select from 
drop down 
Can be 
populated 
with 
Values 
from the 
Description 
Column 
 
• Suspend Fee 
• Reinstate Fee 
• Reinstate a portion 
of Fee 
• Change Fee 
• Other 
12b-1 Change Type Other 
(specify)  
 
(Impacted Funds / 12b-1 
Fee Change table) 
change
TypeOt
her 
A/N OC 50   Required if 12b-1 Change 
Type is “Other” 
 
Special characters allowed 
 
12b-1 Fee In Prospectus 
(%)  
 
(Impacted Funds / 12b-1 
Fee Change table) 
  
feeInPr
ospectu
s 
A/N O 10 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99.9999999 
 
   
Fee Currently Paid (%)  
 
(Impacted Funds / 12b-1 
Fee Change table) 
feeCurr
entlyPai
d 
A/N O 10 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
 99.9999999 
 
   

---

## Page 30

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 30 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
12b-1 New Fee Payment 
(%)  
 
(Impacted Funds / 12b-1 
Fee Change table) 
newFee
Paymen
t 
A/N O 10 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99.9999999 
 
   
12b-1 Current: 12b-1 
discontinues after 
(number of months) 
 
(Impacted Funds / 12b-1 
Fee Change table) 
current
Disconti
nues 
A/N O 3   999 
12b-1 New: 12b-1 
discontinues after 
(number of months)  
 
(Impacted Funds / 12b-1 
Fee Change table) 
newDis
continu
es 
A/N O 3   999 
 12b-1 Current: Deferred 
until (number of months) 
 
 (Impacted Funds / 12b-1 
Fee Change table) 
current
Deferre
d 
A/N O 3   999 
12b-1 New: Deferred until 
(number of months) 
    
(Impacted Funds / 12b-1 
Fee Change table) 
newDef
erred 
A/N O 3   999 
 12b-1 Current: Start at 
(breakpoint) 
 
(Impacted Funds / 12b-1 
Fee Change table) 
current
Breakp
oint 
A/N O 17   99999999999999.99 
12b-1 New: Start at 
(breakpoint) 
 
newBre
akpoint 
A/N O 17   99999999999999.99 

---

## Page 31

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 31 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds table 
/12b-1 Fee Change table)  
 
12b-1 Account Type   
 
(Impacted Funds / 12b-1 
Fee Change table) 
account
Type 
A/N O  100    
Service Fund  
Number 
 
  (Impacted Funds / 12b-1 
Fee Change table) 
sfFund
Numbe
r 
A/N O 8      
Service Security Issue [[ID]]   
 
(Impacted Funds / 12b-1 
Fee Change table) 
sfSecIss
ueId 
A/N O 9    
N/A status 
 
(Impact
ed 
Funds / 
12b-1 
Fee 
Change 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A  rowId 
 
(Impact
ed 
Funds / 
12b-1 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  

---

## Page 32

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 32 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Fee 
Change 
table) 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Service Fund Name 
  
(Impacted Funds / Service 
Fee Change ) 
sfFund
Name 
A/N O 60    
Service Ticker  
 
(Impacted Funds / Service 
Fee Change) 
sfFundT
icker 
A/N O 12    
Service Share Class  
 
(Impacted Funds / Service 
Fee Change) 
sfFundS
hareCla
ss 
A/N O  20    
Service Change Type 
 
(Impacted Funds / Service 
Fee Change) 
sfChang
eType 
A/N O  Can select from 
drop down 
Can be 
populated 
with 
Values 
from the 
Description 
Column 
 
• Suspend Fee 
• Reinstate Fee 
• Reinstate a portion 
of Fee 
• Change Fee 
• Other 
Service Change Type 
Other (specify)  
 
sfChang
eTypeO
ther 
A/N OC 50 This field will be 
greyed on the UI 
unless “Other” is 
 Required if  Change Type 
is “Other” 

---

## Page 33

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 33 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds / Service 
Fee Change) 
selected for 
Change Type 
 
If the user 
changes the 
Change Type to 
something other 
than “Other” 
then the field is 
cleared and is 
disabled. 
Service Fee In Prospectus   
 
(Impacted Funds / Service 
Fee Change) 
sfFeeIn
Prospec
tus 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
   
Service Fee In Prospectus 
(Format Value)   
 
(Impacted Funds / Service 
Fee Change) 
sfFeeIn
ProFmt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with 
Values 
from the 
Description 
Column 
 
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 
Service Fee Currently Paid    
 
(Impacted Funds / Service 
Fee Change) 
sfFeeCu
rPaid 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
 
Service Fee Currently Paid 
(Format Value)  
 
(Impacted Funds / Service 
Fee Change) 
sfFeeCu
rPaidF
mt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if    Fee  
Currently Paid is 
populated 

---

## Page 34

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 34 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Service New Fee Payment 
  
(Impacted Funds / Service 
Fee Change) 
sfNewF
eePay 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
 
   
Service Fee New Fee 
Payment (Format Value) 
 
(Impacted Funds / Service 
Fee Change) 
sfNewF
eePayF
mt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if New Fee 
Payment is populated 
Service Account Type  
  
(Impacted Funds / Service 
Fee Change) 
sfAccou
ntType 
A/N O 100     
N/A status 
 
(Impact
ed 
Funds / 
Service 
Fee 
Change
) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 35

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 35 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
N/A rowId 
 
(Impact
ed 
Funds / 
Service 
Fee 
Change
) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Distribution Fund 
Number 
 
(Impacted Funds /  
Distribution Fee table) 
dfFund
Numbe
r 
A/N O 8      
Distribution Security Issue 
[[ID]] 
 
(Impacted Funds /  
Distribution Fee table) 
dfSecIss
ueId 
A/N O  9    
Distribution Fund Name 
 
(Impacted Funds /  
Distribution Fee table) 
dfFund
Name 
A/N O 60    
Distribution Ticker 
 
(Impacted Funds /  
Distribution Fee table) 
dfFund
Ticker 
A/N O 12    

---

## Page 36

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 36 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Distribution Share Class 
 
(Impacted Funds /  
Distribution Fee table) 
dfFund
ShareCl
ass 
A/N O 20    
Distribution Change Type 
 
(Impacted Funds /  
Distribution Fee table) 
dfChan
geType 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Suspend Fee 
• Reinstate Fee 
• Reinstate a portion 
of Fee 
• Change Fee 
• Other 
Distribution Change Type 
Other (specify) 
 
(Impacted Funds /  
Distribution Fee table) 
dfChan
geType
Other 
A/N OC 50 This field will be 
greyed on the UI 
unless “Other” is 
selected for 
Change Type 
 
If the user 
changes the 
Change Type to 
something other 
than “Other” 
then the field is 
cleared and is 
disabled. 
 Required if  Change Type 
is “Other” 
Distribution Fee In 
Prospectus 
 
(Impacted Funds /  
Distribution Fee table) 
dfFeeIn
Prospec
tus 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
 
   
Distribution Fee In 
Prospectus (Format Value) 
 
(Impacted Funds /  
Distribution Fee table) 
dfFeeIn
ProFmt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 
Distribution Fee Currently 
Paid   
 
(Impacted Funds /  
Distribution Fee table) 
dfFeeC
urPaid 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
 99999999999999.999999
999  
   

---

## Page 37

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 37 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
screens/views 
and Excel files 
generated by the 
system 
Distribution Fee Currently 
Paid (Format Value) 
 
(Impacted Funds /  
Distribution Fee table) 
dfFeeC
urPaidF
mt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee Currently 
Paid  is populated 
 
Distribution New Fee 
Payment 
 
(Impacted Funds /  
Distribution Fee table) 
dfNewF
eePay 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
   
Distribution New Fee 
Payment (Format Value) 
 
(Impacted Funds /  
Distribution Fee table) 
dfNewF
eePayF
mt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if New Fee 
Payment  is populated 
Distribution Account Type  
 
(Impacted Funds /  
Distribution Fee table) 
dfAcco
untTyp
e 
A/N O 100     
N/A status 
 
 
(Impact
ed 
Funds /  
Distribu
tion Fee 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 

---

## Page 38

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 38 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
 
  
 
N/A 
 
rowId 
 
 
(Impact
ed 
Funds /  
Distribu
tion Fee 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
IRA Custodial Annual Fund 
Number 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaFund
Numbe
r 
A/N O 8      

---

## Page 39

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 39 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
IRA Custodial Annual 
Security Issue [[ID]] 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaSecIs
sueId 
A/N O  9    
IRA Custodial Annual Fund 
Name 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaFund
Name 
A/N O 60    
IRA Custodial Annual 
Ticker 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaFund
Ticker 
A/N O 12    
IRA Custodial Annual 
Share Class 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaFund
ShareCl
ass 
A/N O 20    
IRA Custodial Annual 
Change Type 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table)  
icaChan
geType 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Suspend Fee 
• Reinstate Fee 
• Reinstate a portion 
of Fee 
• Change Fee 
• Other 
IRA Custodial Annual 
Change Type Other 
(specify) 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaChan
geType
Other 
A/N OC 50 This field will be 
greyed on the UI 
unless “Other” is 
selected for 
Change Type 
 
If the user 
changes the 
Change Type to 
something other 
than “Other” 
then the field is 
cleared and is 
disabled. 
 Required if  Change Type 
is “Other” 
IRA Custodial Annual Fee 
In Prospectus 
 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaFeeI
nProsp
ectus 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
 99999999999999.999999
999  
 

---

## Page 40

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 40 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
portal 
screens/views 
and Excel files 
generated by the 
system 
IRA Custodial Annual Fee 
In Prospectus (Format 
Value) 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaFeeI
nProFm
t 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 
IRA Custodial Annual Fee 
Currently Paid   
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaFeeC
urPaid 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
   
IRA Custodial Annual Fee 
Currently Paid (Format 
Value) 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaFeeC
urPaidF
mt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee Currently 
Paid is populated 
IRA Custodial Annual New 
Fee Payment 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaNew
FeePay 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
  
IRA Custodial Annual New 
Fee Payment (Format 
Value) 
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table)  
icaNew
FeePay
Fmt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if New Fee  is 
populated 

---

## Page 41

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 41 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
IRA Custodial Annual 
Account Type  
 
(Impacted Funds / IRA 
Custodial Annual Fee 
Change table) 
icaAcco
untTyp
e 
A/N O 100     
N/A status 
 
 
(Impact
ed 
Funds / 
IRA 
Custodi
al 
Annual 
Fee 
Change 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
 
(Impact
ed 
Funds / 
IRA 
Custodi
al 
Annual 
Fee 
Change 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 

---

## Page 42

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 42 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
the 
correspondin
g “rowId” and 
“status” 
fields. 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
529 Sponsor Annual Fund 
Number 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
saFund
Numbe
r 
A/N O 8      
529 Sponsor Annual 
Security Issue [[ID]] 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
saSecIss
ueId 
A/N O  9    
529 Sponsor Annual Fund 
Name 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
saFund
Name 
A/N O 60    
529 Sponsor Annual 
Ticker 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
 
saFund
Ticker 
A/N O 12    
529 Sponsor Annual Share 
Class 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
saFund
ShareCl
ass 
A/N O 20    
529 Sponsor Annual 
Change Type 
 
saChan
geType 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
• Suspend Fee 
• Reinstate Fee 
• Reinstate a portion 
of Fee 

---

## Page 43

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 43 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
 
from 
Description  
• Change Fee 
• Other 
529 Sponsor Annual 
Change Type Other 
(specify) 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
saChan
geType
Other 
A/N OC 50 This field will be 
greyed on the UI 
unless “Other” is 
selected for 
Change Type 
 
If the user 
changes the 
Change Type to 
something other 
than “Other” 
then the field is 
cleared and is 
disabled. 
 Required if  Change Type 
is “Other” 
529 Sponsor Annual Fee 
In Prospectus 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
 
saFeeIn
Prospec
tus 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999    
529 Sponsor Annual Fee 
In Prospectus (Format 
Value) 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
 
saFeeIn
ProFmt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 
529 Sponsor Annual Fee 
Currently Paid  
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
saFeeC
urPaid 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
 
   

---

## Page 44

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 44 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
529 Sponsor Annual Fee 
Currently Paid (Format 
Value) 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
saFeeC
urPaidF
mt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee Currently 
Paid is  populated 
529 Sponsor Annual New 
Fee Payment 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
saNewF
eePay 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
 
   
 529 Sponsor Annual New 
Fee Payment (Format 
Value) 
 
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
saNewF
eePayF
mt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if  New Fee 
Payment is populated 
529 Sponsor Annual 
Account Type 
  
(Impacted Funds / 529 
Sponsor Annual Fee 
Change table) 
 
saAcco
untTyp
e 
A/N O 100     
N/A 
 
status 
 
(Impact
ed 
Funds / 
529 
Sponso
r 
Annual 
Fee 
Change 
table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 

---

## Page 45

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 45 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
 
  
 
N/A 
 
rowId 
 
(Impact
ed 
Funds / 
529 
Sponso
r 
Annual 
Fee 
Change 
table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Short Term Redemption 
Fund Number 
 
(Short Term Redemption 
Fee table) 
 
strfcFu
ndNu
mber 
A/N O 8      

---

## Page 46

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 46 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Short Term Redemption 
Security Issue [[ID]] 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcSe
cIssueI
d 
A/N O  9    
Short Term Redemption 
Fund Name 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcFu
ndNa
me 
A/N O 60    
Short Term Redemption 
Ticker 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcFu
ndTick
er 
A/N O 12    
Short Term Redemption 
Share Class 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcFu
ndShar
eClass 
A/N O 20    
Short Term Redemption 
Change Type 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcCh
angeTy
pe 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Suspend Fee 
• Reinstate Fee 
• Reinstate a portion 
of Fee 
• Change Fee 
• Other 
Short Term Redemption 
Change Type Other 
(specify) 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcCh
angeTy
peOth
er 
A/N OC 50 This field will be 
greyed on the UI 
unless “Other” is 
selected for 
Change Type 
 
If the user 
changes the 
Change Type to 
something other 
than “Other” 
then the field is 
cleared and is 
disabled. 
 Required if  Change Type 
is “Other” 
Short Term Redemption 
Fee In Prospectus 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcFe
eInPro
spectu
s 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
 99999999999999.999999
999  
   

---

## Page 47

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 47 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
portal 
screens/views 
and Excel files 
generated by the 
system 
Short Term Redemption 
Fee In Prospectus (Format 
Value) 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcFe
eInPro
Fmt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 
Short Term Redemption 
Fee Currently Paid  
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcFe
eCurPa
[[ID]] 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
   
Short Term Redemption 
Fee Currently Paid 
(Format Value) 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcFe
eCurPa
idFmt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 
Short Term Redemption 
New Fee Payment 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcNe
wFeeP
ay 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
 
   
Short Term Redemption 
New Fee Payment 
(Format Value) 
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
strfcNe
wFeeP
ayFmt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 

---

## Page 48

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 48 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Short Term Redemption 
Account Type  
 
(Impacted Funds / Short 
Term Redemption Fee 
table) 
 
strfcAc
countT
ype 
A/N O 100     
N/A status 
 
 
(Impact
ed 
Funds / 
Short 
Term 
Redem
ption 
Fee 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impact
ed 
Funds / 
Short 
Term 
Redem
ption 
Fee 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  

---

## Page 49

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 49 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Purchase Fee Security 
Issue [[ID]] 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcSecI
ssueId 
A/N O 9    
Purchase Fee Fund Name 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcFun
dName 
A/N O 60    
Purchase Fee Ticker 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcFun
dTicker 
A/N O 12    
Purchase Fee Share Class 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcFun
dShare
Class 
A/N O 20    
Purchase Fee Change 
Type 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcCha
ngeTyp
e 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Suspend Fee 
• Reinstate Fee 
• Reinstate a portion 
of Fee 
• Change Fee 
• Other 

---

## Page 50

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 50 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Purchase Fee Change 
Type Other (specify) 
 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcCha
ngeTyp
eOther 
A/N OC 50 This field will be 
greyed on the UI 
unless “Other” is 
selected for 
Change Type 
 
If the user 
changes the 
Change Type to 
something other 
than “Other” 
then the field is 
cleared and is 
disabled. 
 Required if  Change Type 
is “Other” 
Purchase Fee In 
Prospectus 
 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcFeeI
nProsp
ectus 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
 
   
Purchase Fee In 
Prospectus (Format Value) 
  
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcFeeI
nProF
mt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 
Purchase Fee Currently 
Paid   
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcFee
CurPai
d 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
    
Purchase Fee Currently 
Paid (Format Value) 
 
pfcFee
CurPai
dFmt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 

---

## Page 51

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 51 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
Required if Fee in 
Prospectus is populated 
Purchase New Fee 
Payment 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcNe
wFeeP
ay 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999  
 
   
Purchase New Fee 
Payment (Format Value) 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcNe
wFeeP
ayFmt 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 
Purchase Account Type 
 
(Impacted Funds / 
Purchase Fee Change 
table) 
 
pfcAcc
ountTy
pe 
A/N O 100     
N/A 
 
status 
 
(Impact
ed 
Funds / 
Purchas
e Fee 
Change 
table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 52

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 52 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
N/A 
 
rowId 
 
(Impact
ed 
Funds / 
Purchas
e Fee 
Change 
table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Redemption Fee Schedule 
Fund Number 
 
(Impacted Funds / Current 
Schedule / New Schedule 
table) 
 
rfscFu
ndNu
mber 
A/N O 8    
Redemption Fee Schedule 
Security Issue [[ID]] 
 
rfscSec
IssueId 
A/N O  9    

---

## Page 53

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 53 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds / Current 
Schedule / New Schedule 
table) 
 
Redemption Fee Schedule 
Fund Name 
 
(Impacted Funds / Current 
Schedule / New Schedule 
table) 
 
 
rfscFu
ndNa
me 
A/N O 60    
Redemption Fee Schedule 
Ticker 
 
(Impacted Funds / Current 
Schedule / New Schedule 
table) 
 
rfscFu
ndTick
er 
A/N O 12    
Redemption Fee Schedule 
Share Class 
(Impacted Funds / Current 
Schedule / New Schedule 
table) 
 
 
rfscFu
ndShar
eClass 
A/N O 20    
Current Redemption Fee 
Amount 
 
(Impacted Funds / Current 
Schedule / New Schedule 
table) 
 
rfscCur
RedFe
eAmt 
A/N OC 17   99999999999999.99 
If Current Redemption 
Fee Percentage is 
populated this field 
cannot be populated 
Current Redemption Fee 
Percentage 
 
(Impacted Funds / Current 
Schedule / New Schedule 
table) 
 
 
rfscCur
RedFe
ePerce
nt 
A/N OC 6   99.999 
If Current Redemption 
Fee Amount is populated 
this field cannot be 
populated 
New Redemption Fee 
Amount 
 
(Impacted Funds / Current 
Schedule / New Schedule 
table) 
 
rfscNe
wRedF
eeAmt 
A/N OC 17   99999999999999.99 
If New Redemption Fee 
Percentage is populated 
this field cannot be 
populated 
 
New Redemption Fee 
Percentage 
 
rfscNe
wRedF
eePerc
ent 
A/N OC 6   99.999 
If New Redemption Fee 
Amount is populated this 
field cannot be populated 

---

## Page 54

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 54 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds / Current 
Schedule / New Schedule 
table) 
 
 
N/A 
 
status 
 
(Impact
ed 
Funds / 
Current 
Schedul
e / New 
Schedul
e table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A 
 
rowId 
 
(Impact
ed 
Funds / 
Current 
Schedul
e / New 
Schedul
e table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 

---

## Page 55

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 55 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
correspondin
g “rowId” and 
“status” 
fields. 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Breakpoint Schedule Fund 
Number 
 
(Impacted Funds table) 
bscFun
dNum
ber 
A/N O 8    
Breakpoint Schedule 
Security Issue [[ID]] 
 
(Impacted Funds table) 
bscSec
IssueId 
A/N O  9    
Breakpoint Schedule Fund 
Name 
 
(Impacted Funds table) 
bscFun
dName 
A/N O 60    
Breakpoint Schedule 
Ticker 
 
(Impacted Funds table) 
bscFun
dTicker 
A/N O 12    
Breakpoint Schedule 
Share Class 
 
(Impacted Funds table) 
bscFun
dShare
Class 
A/N O 20    
N/A status 
 
(Impact
ed 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 

---

## Page 56

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 56 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impact
ed 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 

---

## Page 57

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 57 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Current Breakpoint 
Minimum Account Value  
 
 
(Current / New Schedule  
table) 
bscCur
LowBr
kSch 
A/N O 17   99999999999999.99 
Current Breakpoint 
Maximum Account Value  
 
 
(Current / New Schedule  
table) 
bscCur
UpBrk
Sch 
A/N O 17   99999999999999.99 
Current Sales Charge Rate 
(%)  
 
 
(Current / New Schedule  
table) 
bscCur
SalesC
harge 
A/N O 6   99.999  
Current Dealer 
Concession Rate (%) 
 
 
(Current / New Schedule  
table) 
bscCur
DealCo
nRate 
A/N O 6   99.999  
Current [[underwriter]] Rate 
(%) 
 
 
(Current / New Schedule  
table) 
bscCur
Under
Rate 
A/N O 6   99.999 
New Breakpoint Minimum 
Account Value  
 
(Current / New Schedule  
table) 
bscNe
wLowB
rkSch 
A/N O 17    99999999999999.99 
New Breakpoint 
Maximum Account Value  
 
(Current / New Schedule  
table) 
 
bscNe
wUpBr
kSch 
A/N O 17   99999999999999.99 
New Sales Charge Rate 
(%) 
 
(Current / New Schedule  
table) 
bscNe
wSales
Charge 
A/N O 6   99.999 
New Dealer Concession 
Rate (%) 
 
(Current / New Schedule  
table) 
bscNe
wDeal
ConRat
e 
A/N O 6   99.999 

---

## Page 58

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 58 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
New [[underwriter]] Rate (%) 
 
(Current / New Schedule  
table) 
bscNe
wUnde
rRate 
A/N O 6    99.999 
N/A status 
 
(Curren
t / New 
Schedul
e  
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Curren
t / New 
Schedul
e  
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 

---

## Page 59

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 59 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
g “rowId” and 
“status” 
fields. 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
CDSC Schedule Fund 
Number 
 
(Impacted Funds table) 
cdscFu
ndNu
mber 
A/N O 8    
 
CDSC Schedule Security 
Issue [[ID]] 
 
(Impacted Funds table) 
cdscSe
cIssueI
d 
A/N O  9    
CDSC Schedule Fund 
Name 
 
(Impacted Funds table)  
cdscFu
ndNa
me 
A/N O 60    
CDSC Schedule Ticker 
 
(Impacted Funds table)  
cdscFu
ndTick
er 
A/N O 12    
CDSC Schedule Share 
Class 
 
(Impacted Funds table) 
cdscFu
ndShar
eClass 
A/N O 20    
N/A status 
 
(Impact
ed 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 

---

## Page 60

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 60 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impact
ed 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 

---

## Page 61

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 61 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Current CDSC Schedule 
Lower Limit 
 
(Current / New Schedule  
table) 
cdscCu
rLowBr
kSch 
A/N O 17   99999999999999.99 
Current CDSC Schedule 
Upper Limit 
 
(Current / New Schedule  
table) 
cdscCu
rUpBrk
Sch 
A/N O 17   99999999999999.99 
Current CDSC Rate (%) 
 
(Current / New Schedule  
table) 
cdscCu
rRate 
A/N O 10   99.9999999 
Current Holding Period in 
months ([[shares]] redeemed 
within this period are 
subject to CDSC charge) 
 
(Current / New Schedule  
table) 
cdscCu
rHoldP
eriod 
A/N O 3   999 
New CDSC Schedule 
Lower Limit 
 
(Current / New Schedule  
table) 
cdscNe
wLowB
rkSch 
A/N O 17   99999999999999.99 
New CDSC Schedule 
Upper Limit 
 
(Current / New Schedule  
table) 
cdscNe
wUpBr
kSch 
A/N O 17   99999999999999.99 
New CDSC Rate (%) 
 
(Current / New Schedule  
table) 
cdscNe
wRate 
A/N O 10   99.9999999 
New Holding Period in 
months ([[shares]] redeemed 
within this period are 
subject to CDSC charge) 
 
(Current / New Schedule  
table) 
cdscNe
wHold
Period 
A/N O 3   999 
N/A status 
 
(Curren
t / New 
Schedul
e  
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  

---

## Page 62

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 62 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Curren
t / New 
Schedul
e  
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 

---

## Page 63

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 63 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
rowIds assigned to each 
row of the table 
Other 1 Fund Number 
 
(Impacted Funds table) 
o1Fun
dNum
ber 
A/N O 8      
Other 1 Security Issue [[ID]] 
 
(Impacted Funds table) 
o1SecI
ssueId 
A/N O  9    
Other 1 Fund Name 
 
(Impacted Funds table) 
o1Fun
dName 
A/N O 60    
Other 1 Ticker 
 
(Impacted Funds table)  
o1Fun
dTicker 
A/N O 12    
Other 1 Share Class 
 
(Impacted Funds table) 
o1Fun
dShare
Class 
A/N O 20    
N/A status 
 
(Impact
ed 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 64

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 64 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
N/A rowId 
 
(Impact
ed 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Other 1 Current Fee 
 
(Current / New table) 
o1CurF
ee 
N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Suspend Fee 
• Reinstate Fee 
• Reinstate a portion 
of Fee 
• Change Fee 
• Other 
Other 1 Current Fee 
Format Value 
 
(Current / New table) 
o1CurF
eeFmt
Val 
A/N OC 50 This field will be 
greyed on the UI 
unless “Other” is 
selected for 
Change Type 
 
If the user 
changes the 
Change Type to 
something other 
than “Other” 
then the field is 
 Required if  Change Type 
is “Other” 

---

## Page 65

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 65 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
cleared and is 
disabled. 
Other 1 New Fee 
 
(Current / New table) 
o1New
Fee 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999 
   
Other 1 New Fee Format 
Value 
 
(Current / New table) 
o1New
FeeFm
tVal 
A/N OC   Can select from 
drop down  
Can be 
populated 
with Values 
from 
Description  
• Rate (%) 
• BPS 
• Dollar Amount 
 
Required if Fee in 
Prospectus is populated 
Other 1 Account Type 
 
(Current / New table) 
o1Acc
ountTy
pe 
A/N O 24 Value is stored as 
entered. For 
example, if a 
client enters 
1.123000, this 
value is stored. 
This value is 
displayed on all 
portal 
screens/views 
and Excel files 
generated by the 
system 
 99999999999999.999999
999 
 
   
N/A status 
 
(Curren
t / New 
Schedul
e  
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 

---

## Page 66

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 66 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Curren
t / New 
Schedul
e  
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 

---

## Page 67

MF INFO XCHANGE 
Create Notification Step 2 -  Fee/Breakpoint Change 67 
 
UI Field Name API 
Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
rowIds assigned to each 
row of the table 
Comment notific
ationC
omme
nt 
A/N O 4000   Comment field to be used 
for additional comments 
 
  

---

## Page 68

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Hard Close 68 
 
CREATE NOTIFICATION STEP 2 -  FUND CLOSURE – HARD 
CLOSE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Fund Number 
 
(Impacted Funds 
table) 
fundNumber A/N O 8    
Security Issue [[ID]] 
 
(Impacted Funds 
table) 
secIssueId A/N O 9    
Fund Name 
 
(Impacted Funds 
table) 
fundName A/N O 60    
Ticker 
 
(Impacted Funds 
table) 
fundTicker A/N O 12    
Share Class 
 
(Impacted Funds 
table) 
fundShareCl
ass 
A/N O 20     
N/A status 
 
(Impacted 
Funds table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 69

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Hard Close 69 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
the 
correspondin
g “rowId” and 
“status” 
fields.  
N/A rowId 
 
(Impacted 
Funds table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Is the Fund expected 
to re-open 
isFundReOp
en 
A/N O  Can select from 
drop down 
Can  be 
populated 
from 
Description 
• Yes 
• No 
The fund prospectus 
has been Stickered or 
Reprinted   
prospectusSt
ickRep 
A/N O  Can select from 
drop down 
Can  be 
populated 
from 
Description 
• Yes 
• No 
Closing Fund Last 
Trade Date for New 
Investors 
Purchases/Exchanges 
In 
txnNewEffD
ate 
Date O  calendar picker     MM/DD/CCYY  
This date can be 
backdated 

---

## Page 70

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Hard Close 70 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
 
Closing Fund Last 
Trade Date for New 
Investors 
Purchases/Exchanges 
In 
Exceptions Apply 
txnNewExcA
pply 
A/N O  Can select from 
drop down 
Can  be 
populated 
from 
Description 
• No 
• Yes (complete 
New [[investor]] 
Exception table) 
  
Defaults to ‘No’  
 
 
 
 
 
Closing Fund Last 
Trade Date for 
Existing Investors 
Subsequent 
Purchases/Exchanges 
In  
txnExistEffD
ate 
Date O 10 calendar picker     MM/DD/CCYY  
This date can be 
backdated 
Closing Fund Last 
Trade Date for 
Existing Investors 
Subsequent 
Purchases/Exchanges 
In 
Exceptions Apply 
txnExistExcA
pply 
A/N O  Can select from 
drop down 
Can  be 
populated 
from 
Description 
• No 
• Yes (complete 
Existing [[investor]] 
Exception table) 
 
Defaults to ‘No’  
 
New Investors 
Exceptions 
Description 
 
(New Investors 
Exceptions table 
0Ballowed if Closing 
Fund Last Trade Date 
for all New [[investor]] 
Purchases/Exchanges 
In = “Yes”)  
allowableExc
eptionNew 
A/N O 1000      
Special characters allowed  
New Investors 
Activity Allowed 
 
(New Investors 
Exceptions table 
allowed if Closing 
Fund Last Trade Date 
for all New [[investor]] 
Purchases/Exchanges 
In = “Yes”) 
activityAllow
edNew 
A/N O  Can select from 
drop down 
Can  be 
populated 
from 
Description 
• Yes 
• No 
New Investors 
Exceptions Comment 
 
commentNe
w 
A/N O 1000     
Special characters allowed 

---

## Page 71

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Hard Close 71 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(New Investors 
Exceptions table 
allowed if Closing 
Fund Last Trade Date 
for all New [[investor]] 
Purchases/Exchanges 
In = “Yes”) 
Existing Investors 
Exceptions 
Description 
 
(Existing Investors 
Exceptions table 
allowed if Closing 
Fund Last Trade Date 
for all Existing 
[[investor]]’s 
Purchases/Exchanges 
In = “Yes”) 
allowableExc
eption 
A/N O 1000    Special characters allowed 
Existing Investors 
Activity Allowed 
 
(Existing Investors 
Exceptions table 
allowed if Closing 
Fund Last Trade Date 
for all Existing 
[[investor]]’s 
Purchases/Exchanges 
In = “Yes”) 
activityAllow
ed 
A/N O  Can select from 
drop down 
Can  be 
populated 
from 
Description 
• Yes 
• No 
Existing Investors 
Comment 
 
(Existing Investors 
Exceptions table 
allowed if Closing 
Fund Last Trade Date 
for all Existing 
[[investor]]’s 
Purchases/Exchanges 
In = “Yes”) 
 
fundHardClo
seComment 
A/N O 1000       
Comment comment A/N O 4000       
Special characters allowed 
 
 
 
 
 
  

---

## Page 72

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – [[liquidation]] 72 
 
CREATE NOTIFICATION STEP 2 -  FUND CLOSURE – 
[[liquidation]] 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Fund Number 
 
(Impacted Funds 
table) 
fundNum
ber 
A/N O 8    
Security Issue [[ID]] 
 
(Impacted Funds 
table) 
secIssueId A/N O 9    
Fund Name 
(Impacted Funds 
table) 
fundName A/N O 60    
Ticker 
 
(Impacted Funds 
table) 
fundTicker A/N O 12    
Share Class 
 
(Impacted Funds 
table) 
fundShareC
lass 
A/N O 20     
Extended NAV 
 
(Impacted Funds 
table)  
extendedN
av 
A/N O 19   999999999.999999999 
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 73

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – [[liquidation]] 73 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
The fund prospectus 
has been Stickered or 
Reprinted  
prospectus
StickRep 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
T2-Liquidating Fund 
Last Trade Date for 
New [[investor]] 
Purchases/Exchanges 
In  
t2Date1 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 

---

## Page 74

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – [[liquidation]] 74 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
T2- Liquidating Fund 
Last Trade Date for 
Existing Investors 
Subsequent 
Purchases/Exchanges 
In  
t2Date2 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T2- Liquidating Fund 
Last Trade Date for 
Redemptions/Exchan
ges out 
 
  
t2Date3 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T2- Liquidating Fund 
will settle all 
Fund/SERV trades 
T+1 beginning  
t2Date4 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T2-Last Date ACATS 
will be accepted  
t2Date5 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T2-Last Date for 
Automatic 
Investment 
Purchases  
t2Date6 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T2-Last Date for 
Systematic 
Withdrawals (SWIP)  
t2Date7 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
DCC&S- Liquidating 
Fund Last DCC&S 
Trade Date for New 
Investors 
Purchases/Exchanges 
In 
  
dccsDate1 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
 DCC&S- Liquidating 
Fund Last DCC&S 
Trade Date for 
Existing Investors 
Purchases/Exchanges 
In 
dccsDate2 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
DCC&S- Liquidating 
Fund Last DCC&S 
Trade Date for 
Redemptions/Exchan
ges out 
  
dccsDate3 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
DCC&S-Last Date for 
Automatic 
Investment 
Purchases 
  
dccsDate4 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 

---

## Page 75

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – [[liquidation]] 75 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
DCC&S-Last Date for 
Systematic 
Withdrawals (SWIP) 
  
dccsDate5 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T1- Liquidating Fund 
Last Trade Date for 
New [[investor]] 
Purchases/Exchanges 
In 
  
t1Date1 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T1- Liquidating Fund 
Last Trade Date for 
Existing Investors 
Purchases/Exchanges 
In 
  
t1Date2 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T1- Liquidating Fund 
Last Trade Date for 
Redemptions/Exchan
ges out 
  
t1Date3 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T1-Last Date for 
Automatic 
Investment 
Purchases 
  
t1Date4 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
T1-Last Date for 
Systematic 
Withdrawals (SWIP) 
  
t1Date5 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Exceptions Apply  exceptionIn
d 
A/N O  Can select from 
drop down 
 
This will [[default]] 
to “NO” if Yes is 
selected the 
Allowable 
Exception table 
will be displayed 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
 Defaults to ‘No’ 
Allowable exceptions 
for Initial and 
Subsequent 
Investments and 
Exchanges In  
 
(Exceptions apply 
table) 
allowableE
xception 
A/N O 1000   Only Available if the user 
selects Exceptions Apply 
=Yes 
 
SYSTEM will allow 10 
Exceptions 
 
Special characters allowed 
Activity Allowed 
  
(Exceptions apply 
table) 
activityAllo
wed 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
 

---

## Page 76

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – [[liquidation]] 76 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Only Available if the user 
selects Exceptions Apply 
=Yes 
 
SYSTEM will allow 10 
Exceptions 
Comment  
 
(Exceptions apply 
table) 
comment A/N O    Only Available if the user 
selects Exceptions Apply 
=Yes 
 
SYSTEM will allow 10 
Exceptions 
 
Special characters allowed 
Liquidating Fund Last 
Trade Date for New 
[[investor]] 
Purchases/Exchanges 
In 
  
dtDate1 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Liquidating Fund Last 
Trade Date for 
Existing Investors 
Purchases/Exchanges 
In 
  
dtDate2 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Liquidating Fund Last 
Trade Date for 
Redemptions/Exchan
ges out 
  
dtDate3 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Other Direct Trading 
Considerations 
Comment field  
dtConsider
ations 
A/N O 1000   Special characters allowed 
Liquidating Fund 
[[Dividend]]/Capital 
Gain Anticipated 
Record Date  
  
antRecDate
New 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Liquidating Fund 
[[Dividend]] / Capital 
Gain Anticipated Ex 
Date    
antExDateE
xist 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Liquidating Fund 
[[Dividend]]/Capital 
Gain Anticipated 
Payable Date  
antPayDate Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
NAV-Anticipated 
Extended NAV 
availability date  
navDate1 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
NAV-Number of 
decimal places the 
navDecPlac
esTxt 
N O 1    

---

## Page 77

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – [[liquidation]] 77 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Extended NAV will 
contain  
Last date Networking 
maintenance (B51) 
records will be 
accepted 
  
netDateB5
1 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Networking Activity 
Records (F55) Date 
  
netDate1 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Networking Activity 
Records (F55) 
Transaction Type 
value   
netF55Txt A/N O 250   Special characters allowed 
Networking Activity 
Record (F55) Cash 
Disbursement 
Indicator value  
  
netF55Cash
Disb 
A/N O 250   Special characters allowed 
Networking Activity 
N75 [[settlement]] 
record [[settlement]] 
Type  
netN75Sett
Type 
A/N O 250   Special characters allowed 
Networking Activity 
N75 [[settlement]] 
record [[settlement]] 
Indicator  
netN75Sett
Ind 
A/N O 250   Special characters allowed 
Anticipated cash 
[[settlement]] date 
  
netAntCash
SettDate 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Networking Position 
Files (F58) Date(s): 
  
netDate3 Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
 
Can be populated up to 5 
dates 
Sales charge waived 
– NAV to Client 
Indicator  
navToClien
tInd 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description 
•Yes 
•No 
Sales charge waived 
– NAV to Client 
Effective Date 
  
navToClien
tDate 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Sales charge waived 
– NAV to Client Share 
Class  
navToClien
tShr 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•All 
•Specify 

---

## Page 78

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – [[liquidation]] 78 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Sales charge waived 
– NAV to Client 
Specify Share Class    
navToClien
tShrSpecify 
A/N O 250   Special characters allowed 
Fronted Commission 
waived – No FA 
payout Indicator 
  
feeComm
WaiveInd 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Yes 
•No 
Fronted Commission 
waived – No FA 
payout Effective Date 
  
feeComm
WaiveDate 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Fronted Commission 
waived – No FA 
payout Share Class 
  
feeComm
WaiveShr 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Class C 
•Specify 
Fronted Commission 
waived – No FA 
payout Specify Share 
Class 
   
feeComm
WaiveShrS
pecify 
A/N O 250   Special characters allowed 
Finder’s Fee Fronted 
Commission waived 
– No FA payout 
Indicator 
  
findFeeCo
mmWaiveI
nd 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Yes 
•No 
Finder’s Fee Fronted 
Commission waived 
– No FA payout 
Effective Date 
  
findFeeCo
mmWaiveD
ate 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Finder’s Fee Fronted 
Commission waived 
– No FA payout Share 
Class 
  
findFeeCo
mmWaiveS
hr 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•All 
•Specify 
Finder’s Fee Fronted 
Commission waived 
– No FA payout 
Specify Share Class 
  
findFeeCo
mmWaiveS
hrSpec 
A/N O 250   Special characters allowed 
Waive CDSC in other 
funds if they were 
exchanged from the 
liquidating fund 
indicator 
  
feeWaiveC
dscLiqInd 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Yes 
•No 
Waive CDSC in other 
funds if they were 
exchanged from the 
feeWaiveC
dscLiqIndD
ate 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 

---

## Page 79

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – [[liquidation]] 79 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
liquidating fund 
Effective Date 
    
Fee Waivers for CDSC 
  
feeWaivers
CdscYesNo 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Yes 
•No 
Fee Waivers for CDSC 
starting Effective 
Date 
  
feeWaivers
CdscDate 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Fee Waivers for STR 
  
feeWaivers
StrYesNo 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Yes 
•No 
Fee Waivers for STR 
starting Effective 
Date 
  
feeWaivers
StrDate 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
12b-1 Fees 
suspended 
  
b1FeesSusp
endedYesN
o 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Yes 
•No 
12b-1 Fees 
suspended starting 
Effective Date 
  
b1FeesSusp
endedDate 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Distribution Fee 
change 
  
distFeeChgI
nd 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Yes 
(complete Distribution 
Fee Change table) 
•No 
 
Defaults to ‘No’ 
 
Distribution Fee 
change Effective 
Date 
  
distFeeChg
Date 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
Service Fee change 
  
feeServiceC
hgInd 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Yes 
(complete Distribution 
Fee Change table) 
•No 
 
Defaults to ‘No’ 
 
Service Fee change 
Effective Date 
  
feeServiceC
hgDate 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 

---

## Page 80

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – [[liquidation]] 80 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Distribution Fee 
Security Issue [[ID]] 
  
(Distribution Fee 
Changes table) 
secIssueIdD
istFee 
A/N 0 9   Only Available if the user 
selects Distribution Fee 
Change  =Yes 
 
SYSTEM will allow 10 
Distribution Fee Changes 
Distribution Fee 
Share Class 
 
(Distribution Fee 
Changes table) 
  
fundShareC
lassDistFee 
A/N O 20   Only Available if the user 
selects Distribution Fee 
Change  =Yes 
 
SYSTEM will allow 10 
Distribution Fee Changes 
Distribution Fee 
Original Distribution 
Fee 
  
(Distribution Fee 
Changes table) 
origDistFee A/N O 250   Only Available if the user 
selects Distribution Fee 
Change  =Yes 
 
SYSTEM will allow 10 
Distribution Fee Changes 
Distribution Fee New 
Distribution Fee 
 
(Distribution Fee 
Changes table)  
newDistFee A/N O 250   Only Available if the user 
selects Distribution Fee 
Change  =Yes 
 
System  will allow 10 
Distribution Fee Changes 
Service Fee Security 
Issue [[ID]] 
 
(Service Fee Changes 
table)  
securityIssu
eIdServFee 
A/N 0 9   Only Available if the user 
selects Distribution Fee 
Changes  =Yes 
 
System  will allow 10 
Exceptions 
Service Fee Share 
Class 
 
(Service Fee Changes 
table) 
fundShareC
lassServFee 
A/N O 20   Only Available if the user 
selects Service Fee 
Change  =Yes 
 
SYSTEM will allow 10 
Service Fee Changes 
Service Fee Original 
Distribution Fee 
 
(Service Fee Changes 
table)  
origServFee A/N O 250   Only Available if the user 
selects Service Fee 
Change  =Yes 
Can select 
 
SYSTEM will allow 10 
Service Fee Changes 
Service Fee New 
Distribution Fee 
 
(Service Fee Changes 
table)  
newServFe
e 
A/N O 250   Only Available if the user 
selects Service Fee 
Change  =Yes 
 
SYSTEM will allow 10 
Service Fee Changes 
Comment 
 
fundLiquid
ationComm
ent 
A/N O 4000   Special characters allowed 

---

## Page 81

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 81 
 
CREATE NOTIFICATION STEP 2 -  FUND CLOSURE – SOFT 
CLOSE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Security Issue [[ID]] 
 
(Impacted Funds 
table) 
secIssueId A/N O 9    
Fund Name 
 
(Impacted Funds 
table) 
fundName A/N O 60    
Ticker 
 
(Impacted Funds 
table) 
fundTicker A/N O 12    
Share Class 
 
(Impacted Funds 
table) 
fundShareC
lass 
A/N O 20     
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 82

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 82 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
“status” 
fields.  
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Is the Fund expected 
to re-open 
isFundReO
pen 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
The fund prospectus 
has been Stickered or 
Reprinted 
prospectus
StickRep 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Closing Fund Last 
Trade Date for New 
Investors 
Purchases/Exchanges 
In 
txnNewEff
Date 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 

---

## Page 83

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 83 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
 
Closing Fund Last 
Trade Date for New 
Investors 
Purchases/Exchanges 
In 
Exceptions Apply 
txnNewExc
Apply 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•      Yes (complete New 
[[investor]] Exception table) 
• No 
 
If yes is selected, the New 
Investors exception table 
will be displayed 
 
Defaults to ‘No’ 
 
New investors in 
Private Banks can 
purchase and 
exchange into the 
Fund 
 
(New [[investor]] 
Exceptions table) 
 
allowableE
xceptionNe
w 
A/N O     New investors in Private 
Banks can purchase and 
exchange into the Fund 
 
 
 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity allowed   
 
(New [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
New fund-of-funds 
can purchase and 
exchange into the 
Fund 
(New [[investor]] 
Exceptions table) 
 
allowableE
xceptionNe
w 
A/N O     New fund-of-funds can 
purchase and exchange 
into the Fund 
 
 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity allowed   
 
(New [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 

---

## Page 84

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 84 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
The portfolio 
manager of the fund 
and members of the 
fund’s portfolio 
management team 
can purchase and 
exchange into the 
Fund and open new 
accounts in this fund 
 
(New [[investor]] 
Exceptions table) 
 
allowableE
xceptionNe
w 
A/N O     The portfolio manager of 
the fund and members of 
the fund’s portfolio 
management team can 
purchase and exchange 
into the Fund and open 
new accounts in this fund 
 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity   
 
(New [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
New Automatic 
Investment Plans are 
allowed to be set up 
 
(New [[investor]] 
Exceptions table) 
 
allowableE
xceptionNe
w 
A/N O     New Automatic 
Investment Plans are 
allowed to be set up 
 
 
 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity allowed   
 
(New [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
Previously closed 
accounts can be re-
open (e.g. Purchase 
more [[shares]] later if 
they redeem all of 
their [[shares]]) 
 
(New [[investor]] 
Exceptions table) 
allowableE
xceptionNe
w 
A/N O     Previously closed 
accounts can be re-open 
(e.g. Purchase more 
[[shares]] later if they 
redeem all of their [[shares]]) 
 
 
 
 

---

## Page 85

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 85 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity allowed   
 
(New [[investor]] 
Exceptions table) 
 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
Clients who have a 
signed LOI (dated 
prior to the 
announcement of 
the Soft Close) are 
allowed to purchase 
 
(New [[investor]] 
Exceptions table) 
allowableE
xceptionNe
w 
A/N O     Clients who have a signed 
LOI (dated prior to the 
announcement of the Soft 
Close) are allowed to 
purchase 
 
 
 
 
 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity allowed   
 
(New [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
Trustee and officers 
of the Trust are 
permitted to open 
new accounts in this 
Fund 
 
(New [[investor]] 
Exceptions table) 
allowableE
xceptionNe
w 
A/N O     Trustee and officers of the 
Trust are permitted to 
open new accounts in this 
Fund 
 
 
  
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity allowed   
 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
• Yes 
• No 

---

## Page 86

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 86 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(New [[investor]] 
Exceptions table) 
with Values 
from 
Description  
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
Existing investors are 
allowed to open new 
accounts (for 
example, if a client 
owns an IRA account 
and wants to 
purchase or 
exchange in this fund 
in a Retail Account) 
 
(New [[investor]] 
Exceptions table) 
allowableE
xceptionNe
w 
A/N O     Existing investors are 
allowed to open new 
accounts (for example, if a 
client owns an IRA 
account and wants to 
purchase or exchange in 
this fund in a Retail 
Account) 
   
 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity allowed   
 
(New [[investor]] 
Exceptions table)  
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
New purchases of 
this fund are allowed 
if the client holds 
positions in another 
fund within the same 
family 
 
(New [[investor]] 
Exceptions table) 
allowableE
xceptionNe
w 
A/N O     New purchases of this 
fund are allowed if the 
client holds positions in 
another fund within the 
same family 
 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity    
  
(New [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment 
   
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 

---

## Page 87

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 87 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
New purchases of 
this fund are allowed 
if the client holds 
fund positions in 
another account with 
the same address of 
record 
 
(New [[investor]] 
Exceptions table) 
allowableE
xceptionNe
w 
A/N O     New purchases of this 
fund are allowed if the 
client holds fund positions 
in another account with 
the same address of 
record  
 
 
 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity allowed   
 
(New [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
New purchases of 
this fund are allowed 
if the client holds 
fund positions in 
another account with 
the same primary 
SSN 
allowableE
xceptionNe
w 
A/N O     New purchases of this 
fund are allowed if the 
client holds fund positions 
in another account with 
the same primary SSN  
 
This field is allowed if  
 Yes is selected for New 
Investors exception table  
Activity allowed  
 
(New [[investor]] 
Exceptions table)  
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment  
 
(New [[investor]] 
Exceptions table)  
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
New purchases of 
this fund are allowed 
if the client holds 
fund positions in 
another account with 
the same name on 
the account 
registration 
 
allowableE
xceptionNe
w 
A/N O     New purchases of this 
fund are allowed if the 
client holds fund positions 
in another account with 
the same name on the 
account registration 
 
 
This field is allowed if  

---

## Page 88

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 88 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(New [[investor]] 
Exceptions table) 
 Yes is selected for New 
Investors exception table  
Activity allowed  
 
(New [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
Client defined field 
 
 
(New [[investor]] 
Exceptions table) 
allowableE
xceptionNe
w 
A/N O     This field has no [[default]] in 
UI Field Name. It is an 
enterable, free-form field 
used to create a custom 
exception. It is allowed if  
Yes is selected for New 
Investors exception table  
 
SYSTEM allows up to 10 
free-form New Exceptions 
to be entered. 
Activity allowed  
 
(New [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
SYSTEM allows up to 10 
New Exceptions to enter 
Comment   
 
(New [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
 
SYSTEM allows up to 10 
New Exceptions to enter 
Closing Fund Last 
Trade Date for 
Existing Investors 
Subsequent 
Purchases/Exchanges 
In  
txnExistEff
Date 
Date O 10 Calendar Picker  MM/DD/CCYY 
This date can be 
backdated 
 
 
  
Closing Fund Last 
Trade Date for 
Existing Investors 
Subsequent 
Purchases/Exchanges 
In 
Exceptions Apply 
txnExistExc
Apply 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•      Yes (complete 
Existing [[investor]] 
Exception table) 
• No 
If yes is selected, the 
Existing Investors 

---

## Page 89

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 89 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
exception table will be 
displayed 
 
Defaults to ‘No’ 
 
Existing investors can 
continue to purchase 
through [[Dividend]] & 
capital gain reinvest 
 
(Existing [[investor]] 
Exceptions table) 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed   
 
(Existing [[investor]] 
Exceptions table) 
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Existing investors in 
[[Broker]]/dealer 
advisory-fee 
programs can 
purchase [[shares]] & 
exchange into the 
fund 
 
(Existing [[investor]] 
Exceptions table) 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed 
 
(Existing [[investor]] 
Exceptions table)   
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Existing RIA and Bank 
Trust firms that have 
an investment 
allocation to the 
Fund in a fee-based 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  

---

## Page 90

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 90 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
advisory accounts 
can add new 
investors 
 
(Existing [[investor]] 
Exceptions table) 
Activity allowed   
 
(Existing [[investor]] 
Exceptions table) 
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Existing 
[[Broker]]/dealers that 
have an investment 
allocation to the 
Fund in a fee-based 
advisory accounts 
can add new 
investors 
 
(Existing [[investor]] 
Exceptions table) 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed   
 
(Existing [[investor]] 
Exceptions table)  
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Existing investors in 
private banks can 
continue to purchase 
& exchange into the 
Fund 
 
(Existing [[investor]] 
Exceptions table) 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed   
 
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
• Yes 
• No 

---

## Page 91

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 91 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Existing [[investor]] 
Exceptions table)  
with Values 
from 
Description  
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Existing investors in 
401(k), Single K, 
403(b), pension, 
profit sharing plans, 
defined benefit 
plans, SIMPLE IRAs, 
SEP IRAs can 
purchase and 
exchange into the 
fund 
 
(Existing [[investor]] 
Exceptions table)  
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed   
 
(Existing [[investor]] 
Exceptions table)  
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table)  
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Existing employer 
sponsored 
retirement plans that 
have an investment 
allocation to the 
Fund can add new 
participants 
 
(Existing [[investor]] 
Exceptions table) 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed   
 
(Existing [[investor]] 
Exceptions table) 
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 

---

## Page 92

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 92 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Existing shareholders 
in Roth IRAs, 
Traditional ITAs, 
Rollover IRAs can 
purchase and 
exchange into the 
Fund 
 
(Existing [[investor]] 
Exceptions table)  
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed   
 
(Existing [[investor]] 
Exceptions table) 
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Existing investors in 
college savings 
programs that 
currently have the 
Fund within their 
investment options 
can purchase and 
exchange into the 
Fund 
 
(Existing [[investor]] 
Exceptions table) 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed   
 
(Existing [[investor]] 
Exceptions table) 
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 

---

## Page 93

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 93 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Existing investors in 
self-directed 
brokerage accounts 
can purchase and 
exchange into the 
Fund 
 
(Existing [[investor]] 
Exceptions table) 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed   
 
(Existing [[investor]] 
Exceptions table) 
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
All accounts types 
can redeem or 
exchange out of the 
Fund 
 
(Existing [[investor]] 
Exceptions table) 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed   
 
(Existing [[investor]] 
Exceptions table) 
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Existing Automatic 
Investment Plans can 
continue to run 
 
(Existing [[investor]] 
Exceptions table) 
allowableE
xception 
A/N O     This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
Activity allowed  
 
(Existing [[investor]] 
Exceptions table) 
activityAllo
wed 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table 

---

## Page 94

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Closure – Soft Close 94 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
comment  A/N O  1000   This field is allowed if  
 Yes is selected for 
Existing Investors 
exception table  
 
Special characters allowed 
Client defined field 
 
(Existing  [[investor]] 
Exceptions table) 
allowableE
xceptionNe
w 
A/N O     This field has no [[default]] in 
UI Field Name. It is an 
enterable, free-form field 
used to create a custom 
exception. It is allowed if  
Yes is selected for Existing 
Investors exception table  
 
SYSTEM allows up to 10 
free-form New Exceptions 
to be entered. 
Activity allowed  
 
(Existing [[investor]] 
Exceptions table) 
activityAllo
wedNew 
A/N O   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
SYSTEM allows up to 10 
Existing Exceptions to 
enter 
Comment   
 
(Existing [[investor]] 
Exceptions table) 
commentN
ew 
A/N O  1000   This field is allowed if  
 Yes is selected for New 
Investors exception table 
 
Special characters allowed 
 
SYSTEM allows up to 10 
Existing Exceptions to 
enter 
Comment fundSoftClo
seCommen
t 
A/N O  4000   Special characters allowed 
 
  

---

## Page 95

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 95 
 
CREATE NOTIFICATION STEP 2 -  FUND MERGER 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
From Fund Number 
 
(Impacted Funds 
table) 
fromFund
Number 
A/N O 8    
From Security Issue 
[[ID]]  
 
(Impacted Funds 
table) 
fromSecIs
sueId 
A/N O 9    
From Fund Name  
 
(Impacted Funds 
table) 
fromFund
Name 
A/N O 60    
From Ticker  
 
(Impacted Funds 
table) 
fromFund
Ticker 
A/N O 12    
From Share Class 
  
(Impacted Funds 
table) 
fromFund
ShareClas
s 
A/N O 20     
From NAV  
 
(Impacted Funds 
table) 
fromFund
Nav 
A/N O 19    999999999.999999999 
 
To Fund Number  
 
(Impacted Funds 
table) 
toFundNu
mber 
A/N O 8     
To Security Issue [[ID]] 
(Impacted Funds 
table) 
  
toSecIssue
[[ID]] 
A/N 0 9    
To Fund Name 
 
(Impacted Funds 
table)   
toFundNa
me 
A/N 0 60    
To Ticker 
 
(Impacted Funds 
table)  
toFundTic
ker 
A/N O 12    
To Share Class 
  
toFundSh
areClass 
A/N O 20    

---

## Page 96

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 96 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds 
table) 
To NAV  
 
(Impacted Funds 
table) 
extended
Nav 
A/N O 19    999999999.999999999 
 
Merger Ratio (the 
number of Survivor 
Fund [[shares]] for each 
share of Retiring 
Fund)  
 
(Impacted Funds 
table) 
mergerRa
tio 
A/N O 16     
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 

---

## Page 97

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 97 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
[[Proxy]] [[vote]] Day 
  
proxyVote
Day 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
[[Proxy]] Status 
  
proxyStat
us 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Pending 
• Approved 
• Not Approved 
The fund prospectus 
has been Stickered or 
Reprinted:  
  
prospectu
sStickRep 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
T2-Retiring Fund Last 
Trade Date for New 
[[investor]] 
Purchases/Exchanges 
In 
  
t2Date1 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T2-Retiring Fund Last 
Trade Date for 
Existing Investors 
Subsequent 
Purchases/Exchanges 
In 
t2Date2 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 

---

## Page 98

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 98 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
  
T2-Retiring Fund Last 
Trade Date for 
Redemptions/Exchan
ges out 
  
t2Date3 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T2-Retiring Fund will 
settle all Fund/SERV 
trades T+1 beginning 
  
t2Date5 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T2-Last Date ACATS 
will be accepted 
  
t2Date6 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T2-Last Date for 
Automatic 
Investment 
Purchases 
  
t2Date7 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T2-Last Date for 
Systematic 
Withdrawals (SWIP) 
  
t2Date8 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T1-Retiring Fund Last 
Trade Date for New 
[[investor]] 
Purchases/Exchanges 
In 
  
t1Date1 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T1-Retiring Fund Last 
Trade Date for 
Existing Investors 
Purchases/Exchanges 
In 
  
t1Date2 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T1-Retiring Fund Last 
Trade Date for 
Redemptions/Exchan
ges out 
  
t1Date3 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T1-Retiring Fund Last 
Trade Date for [[NSCC]] 
Transfers In or Out 
(same day 
[[settlement]]) 
  
 
t2Date4 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
T1-Last Date for 
Automatic 
Investment 
Purchases 
t1Date4 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 

---

## Page 99

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 99 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
  
T1-Last Date for 
Systematic 
Withdrawals (SWIP) 
  
t1Date5 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
DCC&S-Retiring Fund 
Last DCC&S Trade 
Date for New 
[[investor]] 
Purchases/Exchanges 
In 
  
dccsDate1 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
DCC&S-Retiring Fund 
Last DCC&S Trade 
Date for Existing 
Investors 
Purchases/Exchanges 
In 
  
dccsDate2 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
DCC&S-Retiring Fund 
Last DCC&S Trade 
Date for 
Redemptions/Exchan
ges out 
  
dccsDate3 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
DCC&S-Last Date for 
Automatic 
Investment 
Purchases 
  
dccsDate4 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
DCC&S-Last Date for 
Systematic 
Withdrawals (SWIP) 
  
dccsDate5 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Exceptions Apply 
  
exceptionI
nd 
A/N R   Radio button 
 
This will [[default]] 
to “NO” if Yes is 
selected the 
Allowable 
Exception table 
will be displayed 
Can be 
selected from 
Description 
• Yes 
• No  
  
 
Defaults to ‘No’ 
Allowable exceptions 
for Initial and 
Subsequent 
Investments and 
Exchanges In 
 
(Allowable 
exceptions Apply 
table) 
allowable
Exception 
A/N O  1000   Can be populated only if  
Exceptions Apply = Yes 
 
  
 
 
 
SYSTEM allows up to 10 
Allowable exceptions  

---

## Page 100

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 100 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
 
 
  
Activity Allowed 
 
(Allowable 
exceptions Apply 
table) 
activityAll
owed 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
SYSTEM allows up to 10 
Allowable exceptions 
Comment 
  
(Allowable 
exceptions Apply 
table)  
comment A/N O 1000   SYSTEM allows up to 10 
Allowable exceptions 
 
Special characters allowed 
Retiring Fund Last 
Trade Date for New 
[[investor]] 
Purchases/Exchanges 
In 
  
dtDate1 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Retiring Fund Last 
Trade Date for 
Existing Investors 
Purchases/Exchanges 
In 
  
dtDate2 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Retiring Fund Last 
Trade Date for 
Redemptions/Exchan
ges out 
  
dtDate3 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Other Direct Trading 
Considerations 
Comment field 
  
dtConside
rations 
A/N O 1000   Special characters allowed  
Special-Retiring Fund 
[[Dividend]]/Capital 
Gain Anticipated 
Record Date  
  
sdcgdDate
1 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Special-Retiring Fund 
[[Dividend]]/Capital 
Gain Anticipated Ex 
Date: 
  
sdcgdDate
2 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Special -Fund Accrual 
pay date (if accrual is 
not moved to the 
“To” fund): 
  
sdcgdDate
3 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Special-
[[Dividend]]/Capital 
Gain Reinvestment 
dividendC
apitalSele
ct 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
• Reinvest into Old Fund 
• Reinvest into New Fund 

---

## Page 101

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 101 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
  from 
Description  
Special-Will the 
“From” fund accrual 
be paid out prior to 
the merger? 
  
fundAccru
alSelect 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Special-Retiring Fund 
[[Dividend]]/Capital gain 
Anticipated Payable 
Date 
  
sdcgdDate
4 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Other Special 
[[Dividend]]/Capital 
Gain Distribution 
Considerations  
  
specialDiv
Considera
tion 
A/N O 4000   Special characters allowed 
Regular-Retiring 
Fund 
[[Dividend]]/Capital 
Gain Anticipated 
Record Date  
rdcgdDate
1 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Regular-Retiring 
Fund [[Dividend]] / 
Capital Gain 
Anticipated Ex Date  
rdcgdDate
2 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Regular-Retiring 
Fund 
[[Dividend]]/Capital 
Gain Anticipated 
Payable Date  
  
rdcgdDate
3 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Other Regular 
[[Dividend]]/Capital 
Gain Distribution 
Considerations  
  
regDivCon
sideration 
A/N O 4000   Special characters allowed 
NAV - Retiring Fund 
NAV will be extended 
  
retFundEx
tended 
A/N O   Can select from 
drop down 
 
If Retiring Fund 
NAV will be 
extended is 
“Yes” then the 
Retiring Fund 
NAV section will 
be displayed 
otherwise that 
section will not 
be displayed on 
the UI 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
 

---

## Page 102

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 102 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
NAV Retiring -
Retiring Fund NAV 
will be used to 
process the merger 
  
 
processM
ergerSelec
t 
A/N OC 
 
  
 Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
• N/A 
 
must be “N” if “Merger 
Ratio will be used to 
process merger” field = “Y 
 
  
NAV - Survivor Fund 
NAV will be extended 
  
surviveFu
ndExtend
ed 
A/N O  Can select from 
drop down 
 
If Survivor Fund 
NAV will be 
extended is 
“Yes” then the 
Survivor Fund 
NAV section will 
be displayed 
 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
NAV Survivor - 
Survivor Fund NAV 
will be used to 
process the merger 
  
surviveFu
ndUsed 
A/N OC 
 
  
   • Yes 
• No 
• N/A 
 
 
must be “N” if “Merger 
Ratio will be used to 
process merger” field = 
“Y” 
NAV Retiring-
Anticipated Extended 
NAV availability date: 
  
  
navDate1 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
NAV Retiring -
Number of decimal 
places the Retiring 
Fund NAV will 
contain: 
  
  
navDecPla
cesTxt 
N O 1    
NAV Retiring -
Transaction types the 
Extended NAV would 
apply: 
 
  
  
extended
NavSelect 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Only merger 
transactions 
• All activity including 
merger transactions 
NAV Retiring -Date 
NAV will revert to 2 
decimal places   
navDate2 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 

---

## Page 103

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 103 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
NAV Survivor-
Anticipated Extended 
NAV availability date  
  
surviveNa
vDate1 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
NAV Survivor -
Number of decimal 
places the Survivor 
Fund NAV will 
contain  
  
surviveNa
vDecPlace
sTxt 
N O 1    
NAV Survivor -
Transaction types the 
Extended NAV would 
apply: 
 
  
surviveExt
endedNav
Select 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•  Only merger 
transactions 
• All activity including 
merger transactions 
NAV Survivor -Date 
NAV will revert to 2 
decimal places: 
 
  
surviveNa
vDate2 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Anticipated Merger 
Ratio availability date 
  
mrDate1 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Number of decimal 
places the ratio will 
contain 
  
mrDecPla
cesTxt 
N O 1    
Merger Ratio will be 
used to process the 
merger 
  
mergerRa
tioSelect 
A/N OC 
 
  
 Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
must be “N” if “Retiring 
Fund NAV and/or Survivor 
Fund NAV will be used to 
process merger” = “Y”   
Networking Merger 
Activity Records 
(F55) Date  
  
netDate1 Date O 250   Special characters allowed 
Networking Merger 
Activity Records 
(F55) Transaction 
Type value  
  
netF55Txt A/N O 250   Must be a Transaction 
Type code corresponding 
to the values in 
the  “Transaction Type” 
field on the Networking 
Activity Detail F55 record 
New/Surviving 
Accounts Networking 
Fund Account 
Response records 
(F51)/FAN Mail Date  
  
netDate2 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 

---

## Page 104

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 104 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Networking Position 
Files (F58) Date(s)  
  
netDate3 Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Can be more than one 
date. The limit on the 
number of dates is 5. 
Fee Waivers for CDSC 
  
feeWaiver
sCdscYesN
o 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Fee Waivers for CDSC 
starting Trade Date 
  
feeWaiver
sCdscDate 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Fee Waivers for STR 
  
feeWaiver
sStrYesNo 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Fee Waivers for STR 
starting Trade Date 
  
feeWaiver
sStrDate 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
12b-1 Fees 
suspended 
  
b1FeesSus
pendedYe
sNo 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
12b-1 Fees 
suspended starting 
Trade Date 
  
b1FeesSus
pendedDa
te 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Distribution Fee 
suspended 
  
distFeeSu
spendedY
esNo 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Distribution Fee 
suspended starting 
Trade Date 
  
distFeeSu
spendedD
ate 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Service Fee 
suspended 
  
svcFeeSus
pendedYe
sNo 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Service Fee 
suspended starting 
Trade Date 
  
svcFeeSus
pendedDa
te 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 

---

## Page 105

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Merger 105 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Comment 
 
fundMerg
erComme
nt 
A/N O 4000   Special characters allowed 
 
 
 
 
 
 
 
 
  

---

## Page 106

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Name Change 106 
 
CREATE NOTIFICATION STEP 2 -  FUND NAME CHANGE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
From Fund Number 
 
(Impacted Funds 
table) 
fromFund
Number 
A/N O 8    
From Security Issue [[ID]]  
 
(Impacted Funds 
table) 
fromSecIs
sueId 
A/N O 9    
From Fund Name  
 
(Impacted Funds 
table)  
fromFund
Name 
A/N O  60   The “To Fund Name” 
cannot match this field 
From Ticker  
 
(Impacted Funds 
table)   
fromFund
Ticker 
A/N O 12    
From Share Class  
 
(Impacted Funds 
table)  
fromFund
ShareClas
s 
A/N O 20    
To Fund Number 
 
(Impacted Funds 
table)  
toFundNu
mber 
A/N O 8    
To Security Issue [[ID]] 
 
(Impacted Funds 
table)  
toSecIssue
[[ID]] 
A/N O 9    
To Fund Name 
 
(Impacted Funds 
table)  
toFundNa
me 
A/N O  60   The “From Fund Name” 
cannot match this field 
To Ticker  
 
(Impacted Funds 
table) 
toFundTic
ker 
A/N O 12    
To Share Class 
  
(Impacted Funds 
table) 
toFundSh
areClass 
A/N O 20    
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 

---

## Page 107

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Name Change 107 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the 
values assigned by 
MF Info Xchange. 

---

## Page 108

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Name Change 108 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
“Receive Notification 
Data for an Event [[ID]]” 
endpoint must be 
called to return the 
current version of 
the notification with 
the rowIds assigned 
to each row of the 
table 
The fund prospectus 
has been Stickered or 
Reprinted:  
  
prospectu
sStickRep 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Comment 
 
fundNam
eChangeC
omment 
A/N O 4000   Special characters allowed 
 
  

---

## Page 109

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Reopening 109 
 
CREATE NOTIFICATION STEP 2 -  FUND REOPENING 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Fund Number 
 
(Impacted Funds 
table) 
fundNum
ber 
A/N O 8    
Security Issue [[ID]]  
 
(Impacted Funds 
table) 
secIssueId A/N O 9    
Fund Name 
 
(Impacted Funds 
table)   
fundNam
e 
A/N O 60     
Ticker   
 
(Impacted Funds 
table) 
fundTicke
r 
A/N O 12    
Share Class 
 
(Impacted Funds 
table) 
  
fundShare
Class 
A/N O 20    
Current Fund Status  
 
(Impacted Funds 
table) 
currentFu
ndStatus 
A/N O     • Soft Closed 
• Hard Closed 
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 

---

## Page 110

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Reopening 110 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 

---

## Page 111

MF INFO XCHANGE 
Create Notification Step 2 -  Fund Reopening 111 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
1BThe fund prospectus 
has been Stickered or 
Reprinted select a 
value / Yes / No 
 
prospectu
sStickRep 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
Reopening Fund Trade 
Date for new accounts  
   
newAcctT
radeDate 
Date O 10   MM/DD/CCYY 
 
This date can be 
backdated 
 
Reopening Fund Trade 
Date for Existing 
Investors Subsequent 
Buys/Exchanges In 
    
subExchTr
adeDate 
Date O 10    MM/DD/CCYY 
 
This date can be 
backdated 
 
Reopening Fund Trade 
Date for Sells 
   
sellsTrade
Date 
Date O 10   MM/DD/CCYY 
 
This date can be 
backdated 
 
Comment 
 
fundReop
eningCom
ment 
A/N O 4000   Special charters allowed 
 
  

---

## Page 112

MF INFO XCHANGE 
Create Notification Step 2 -  Interval/Tender Fund Transaction Schedule 112 
 
 
CREATE NOTIFICATION STEP 2 -  INTERVAL/TENDER FUND 
TRANSACTION SCHEDULE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Year Year N R 4   Year (e.g. 2023) 
Quarter 
  
quarter A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• 1st Quarter 
• 2nd Quarter 
• 3rd Quarter 
• 4th Quarter 
 
  
Not allowed if Month   
populated 
Month 
  
month A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• January 
• February 
• March 
• April 
• May 
• June 
• July 
• August 
• September 
• October 
• November 
• December 
  
Not allowed if Quarter  is 
populated 
Notification Type 
   
notificatio
nType 
A/N R  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Interval Fund 
• Tender Offer 
Notification   notificatio
n 
A/N R  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Initial Schedule 
• Revised 
Schedule 
Fund Number 
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
 
  
fundNum
ber 
A/N O 8    

---

## Page 113

MF INFO XCHANGE 
Create Notification Step 2 -  Interval/Tender Fund Transaction Schedule 113 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Security Issue [[ID]] 
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
secIssueId A/N O  9    
Fund Name 
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
fundNam
e 
A/N O 60    
Ticker 
 
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
  
fundTicke
r 
A/N O 12    
Share Class  
 
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
fundShare
Class 
A/N O 20    
Frequency / Tender 
Indicator  
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
frequency
TenderInd
icator 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Monthly 
• Quarterly 
• Yearly 
• Ad-hoc 
• Tender 
Repurchase / 
Subscription Indicator 
  
(Interval/Tender Fund 
Transaction Schedule 
table) 
repurchas
eSubscript
ionIndicat
or 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Repurchase 
• Subscription 
Change Indicator  
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
changeInd
icator 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•Y   
•A  
•D 
 
Where:  
Y-change 
A-add 
D-delete  
Projected/Confirmed 
Indicator 
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
projected
Confirmed
Indicator 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Projected  
• Confirmed 
Window Dates – 
Period Start Date 
 
periodStar
tDate 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 

---

## Page 114

MF INFO XCHANGE 
Create Notification Step 2 -  Interval/Tender Fund Transaction Schedule 114 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
 
Window Dates – 
Period End Date  
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
periodEnd
Date 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Holder Record Date  
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
recordDat
e 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
[[NSCC]] Trade Date 
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
 
nsccTrade
Date 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Last Cycle on Trade 
Date 
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
lastCycleo
nTradeDat
e 
N O 10   MM/DD/CCYY 
This date can be 
backdated 
 
N/A status 
 
(Interval/T
ender 
Fund 
Transactio
n 
Schedule 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 115

MF INFO XCHANGE 
Create Notification Step 2 -  Interval/Tender Fund Transaction Schedule 115 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
g “rowId” and 
“status” 
fields.  
N/A rowId 
 
(Interval/T
ender 
Fund 
Transactio
n 
Schedule 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
As of Transactions 
Allowed 
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
asOfTrans
actionsAll
owed 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
• TBD 
Rejected Transaction 
Reprocess Date 
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
rejectedTr
ansaction
OnReproc
essDate 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Pricing Date 
 
pricingDat
e 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 

---

## Page 116

MF INFO XCHANGE 
Create Notification Step 2 -  Interval/Tender Fund Transaction Schedule 116 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
 
[[settlement]] Date 
  
(Interval/Tender Fund 
Transaction Schedule 
table) 
settlemen
tDate 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Trading Pre-
Notification – 
Required  
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
required A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
Trading Pre-
Notification - Required 
by (date) 
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
requiredB
yDate 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Will Pro-Rate? 
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
willProRat
e 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
• TBD 
[[Pro-Rata]] Percentage 
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
rate A/N O 19   999999999.999999999 
 
Repurchase Fee- 
Repurchase Fee will 
be charged? 
  
(Interval/Tender Fund 
Transaction Schedule 
table) 
repurchas
eFeeWillB
eCharged 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
• TBD 
Repurchase Fee - 
Repurchase Fee 
 
(Interval/Tender Fund 
Transaction Schedule 
table)  
repurchas
eFee 
A/N O 100    
Proposed Percentage 
to be repurchased 
 
(Interval/Tender Fund 
Transaction Schedule 
table) 
  
proposed
Percentag
eToBeRep
urchased 
A/N O 9   999.99999 
Cannot be greater than 
100 

---

## Page 117

MF INFO XCHANGE 
Create Notification Step 2 -  Interval/Tender Fund Transaction Schedule 117 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Comment 
  
notificatio
nCommen
t 
A/N O 4000   Special characters allowed 
 
 
  

---

## Page 118

MF INFO XCHANGE 
Create Notification Step 2 - Issue Notification 118 
 
CREATE NOTIFICATION STEP 2 - ISSUE NOTIFICATION 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Issue Type issueType A/N R  Can select from 
drop down 
 
Can be 
populated 
with Values 
from 
Description  
• Unexpected Market 
Close 
• Commission Payment 
Delay 
• 12b-1 Service Fee 
Delay 
• [[NSCC]] Trade 
Confirmation Delay 
• [[NSCC]] Networking File 
Delay 
• Pricing Delay 
• Early Market Close 
• Other 
 
Issue Description (if 
Issue Type Other) 
  
issueType
Desc 
A/N OC 1000   Required if Issue Type is 
“Other” otherwise this 
field should not be 
displayed 
 
Special characters allowed 
 
What is the level of 
Impact for this issue  
issueType
LevelImpa
ct 
A/N R  Can select from 
drop down 
 
 
If level of impact 
for this issue = 
“Fund complex 
wide”, Section 
Anticipated 
Resolution 
should be 
displayed.  
 
If level of impact 
for this issue = 
“Specific to a 
particular 
Fund/Security 
Issue [[ID]]”, 
Section 
Impacted Funds 
should be 
displayed. 
Can be 
populated 
with Values 
from 
Description  
• Fund complex 
wide 
• Specific to a 
particular 
Fund/Security 
Issue [[ID]] 
Fund Number 
 
(Impacted Funds 
table)  
fundNum
ber 
A/N O 8   Can be populated if field 
What is the level of 
Impact for this issue = 
‘Specific to a particular 
Fund/Security Issue [[ID]])’ 
 

---

## Page 119

MF INFO XCHANGE 
Create Notification Step 2 - Issue Notification 119 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Security Issue [[ID]] 
  
(Impacted Funds 
table) 
secIssueId A/N O 9   Can be populated if field 
What is the level of 
Impact for this issue = 
‘Specific to a particular 
Fund/Security Issue [[ID]])’ 
 
Fund Name 
 
(Impacted Funds 
table)  
fundNam
e 
A/N O 60   Can be populated if field 
What is the level of 
Impact for this issue = 
‘Specific to a particular 
Fund/Security Issue [[ID]])’ 
 
Ticker 
 
(Impacted Funds 
table)  
fundTicke
r 
A/N O 12   Can be populated if field 
What is the level of 
Impact for this issue = 
‘Specific to a particular 
Fund/Security Issue [[ID]])’ 
 
Share Class 
 
(Impacted Funds 
table)  
fundShare
Class 
A/N O 20   Can be populated if field 
What is the level of 
Impact for this issue = 
‘Specific to a particular 
Fund/Security Issue [[ID]])’ 
 
Effective Date 
 
(Impacted Funds 
table)  
fundEffect
iveDate 
Date O 10   MM/DD/CCYY 
This date can be 
backdated 
 
Can be populated if field 
What is the level of 
Impact for this issue = 
‘Specific to a particular 
Fund/Security Issue [[ID]])’ 
Anticipated Resolution 
Date and Time 
  
(Impacted Funds 
table)  
antResDat
eTime 
A/N O 25   Can be populated if field 
What is the level of 
Impact for this issue = 
‘Specific to a particular 
Fund/Security Issue [[ID]])’ 
 
Special characters allowed 
Comment 
 
(Impacted Funds 
table)  
impFunds
Comment
s 
A/N O 1000   Can be populated if field 
What is the level of 
Impact for this issue = 
‘Specific to a particular 
Fund/Security Issue [[ID]])’ 
 
Special characters allowed 
N/A   status 
 
(Impacted 
Funds 
table   
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  

---

## Page 120

MF INFO XCHANGE 
Create Notification Step 2 - Issue Notification 120 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/a rowId 
 
(Impacted 
Funds 
table   
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 

---

## Page 121

MF INFO XCHANGE 
Create Notification Step 2 - Issue Notification 121 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
rowIds assigned to each 
row of the table 
Anticipated Resolution 
Date and Time 
 
(Anticipated 
Resolution table) 
  
resAntRes
DateTime 
A/N O 25   Can be populated if field 
What is the level of 
Impact for this issue = 
‘Fund complex wide’ 
 
 
Special characters allowed 
Comment 
 
(Anticipated 
Resolution table)  
resComm
ent 
A/N O 1000   Can be populated if field 
What is the level of 
Impact for this issue = 
‘Fund complex wide’ 
 
Special characters allowed 
Comments 
  
notificatio
nCommen
t 
A/N O 4000   Special characters allowed 
 
 
  

---

## Page 122

MF INFO XCHANGE 
Create Notification Step 2 -  Large Trade Threshold Change 122 
 
CREATE NOTIFICATION STEP 2 -  LARGE TRADE THRESHOLD 
CHANGE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Security Issue [[ID]] 
 
(Impacted Funds 
table)  
secIssueId A/N O 9    
Fund Name  
 
(Impacted Funds 
table) 
fundNam
e 
A/N O 60    
Ticker  
 
(Impacted Funds 
table) 
fundTicke
r 
A/N O 12    
Share Class 
 
(Impacted Funds 
table)  
fundShare
Class 
A/N O 20    
Large Trade 
Notification Required 
 
(Impacted Funds 
table)  
ltNotifReq A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Large Trade Threshold 
Amount 
 
(Impacted Funds 
table)  
ltDolThres
hold 
A/N OC 17   99999999999999.99 
 
Required if Large Trade 
Notification Required 
(current) is “Yes”  
Large Trade 
Notification Required 
 
(Impacted Funds 
table)  
ltNotifReq
New 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Large Trade Threshold 
Amount 
  
(Impacted Funds 
table) 
ltDolThres
holdNew 
A/N OC 17   99999999999999.99 
 
Required if  Large Trade 
Notification Required 
(new)  is “Yes” 
 
N/A status 
 
(Impacted 
Funds 
table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  

---

## Page 123

MF INFO XCHANGE 
Create Notification Step 2 -  Large Trade Threshold Change 123 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 

---

## Page 124

MF INFO XCHANGE 
Create Notification Step 2 -  Large Trade Threshold Change 124 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comments 
 
largeTrad
eCommen
t 
A/N O 4000   Special characters allowed 
  

---

## Page 125

MF INFO XCHANGE 
Create Notification Step 2 -  Large Trade Notification 125 
 
CREATE NOTIFICATION STEP 2 -  LARGE TRADE 
NOTIFICATION 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Anticipated Trade 
Date 
 
(Large Trade Details 
table) 
antiTrade
Date 
   Date  R 10 This field is 
protected from 
edit 
 MM/DD/CCYY 
 
Auto populated  to 
Effective Date from Step 1 
 
Anticipated 
[[settlement]] 
 
(Large Trade Details 
table) 
antiSettle
ment 
    A/N R  Can select from 
drop down 
Can be populated 
with Values from 
Description  
• T 
• T  + 1 
• T  + 2 
• Other 
 
 
Defaulted to T + 1 
Anticipated 
[[settlement]] – Other 
 
(Large Trade Details 
table) 
antiSettle
mentOthe
r 
       A/N OC 4   Required if Anticipated 
[[settlement]] = ‘Other’, 
otherwise - protected 
Security Issue [[ID]] 
 
(Large Trade Details 
table) 
secIssueId A/N OC 9   Required if Ticker is not 
populated 
Ticker 
 
(Large Trade Details 
table) 
fundTicke
r 
A/N OC 12       
Required if Security is not 
populated 
Fund Name 
 
(Large Trade Details 
table) 
fundNam
e 
A/N R  60   Special characters allowed 
Fund [[DTCC]] [[participant]] 
Number 
 
(Large Trade Details 
table) 
fundPartN
umber 
A/N R 8   Fund [[DTCC]] [[participant]] 
Number in the details 
table must match the 
Fund [[DTCC]] [[participant]] 
Number if populated 
Fund Account Number 
 
(Large Trade Details 
table) 
fundAccN
umber 
A/N OC 20   Required if BIN Number is 
not populated and 
Order Type is any of: 
Subsequent Purchase, 
Redemption, Voluntary 
Share Class Exchange 
BIN Number 
 
(Large Trade Details 
table) 
binNumbe
r 
A/N OC 20   Required if Fund Account 
Number is not populated 
and Order Type is any of: 
Subsequent Purchase, 

---

## Page 126

MF INFO XCHANGE 
Create Notification Step 2 -  Large Trade Notification 126 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Redemption, Voluntary 
Share Class Exchange 
Account Type 
 
(Large Trade Details 
table) 
accountTy
pe 
A/N O  Can select from 
drop down 
Can be populated 
with Values from 
Description  
• Retail 
• Institutional 
• Omnibus 
• Retirement 
•      Trust 
Account 
Representative 
Number 
 
(Large Trade Details 
table) 
accRepNu
mber 
A/N O 9    
Account 
Representative Name 
 
(Large Trade Details 
table)  
accRepNa
me 
A/N O 15    
Trade Method 
 
 
(Large Trade Details 
table) 
tradeMet
hod 
A/N R  Can select from 
drop down 
Can be populated 
with Values from 
Description  
• Automated 
(non-
Fund/SERV) 
• Manual 
• Fund/SERV 
(DCC&S) 
• Fund/SERV     
         (non-DCC&S) 
Order Type 
 
(Large Trade Details 
table) 
orderType A/N R  Can select from 
drop down 
Can be populated 
with Values from 
Description  
• Initial Purchase    
• Subsequent 
Purchase 
• Redemption 
• Voluntary Share 
Class Exchange 
Buy side Security Issue 
[[ID]] (voluntary share 
class exchange) 
 
(Large Trade Details 
table) 
buySecIss
ueId 
A/N OC 9    Required if Buy side 
Ticker is not populated 
and Order Type is 
Voluntary Share Class 
Exchange 
  
Not allowed if Order 
Type is Initial Purchase 
Subsequent Purchase 
Redemption 
 
 
  
Buy side Ticker 
(voluntary share class 
exchange) 
 
(Large Trade Details 
table) 
buyTicker A/N OC 12    Required if Buy side 
Security Issue [[ID]] is not 
populated and Order 
Type is Voluntary Share 
Class Exchange  
 

---

## Page 127

MF INFO XCHANGE 
Create Notification Step 2 -  Large Trade Notification 127 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Not allowed for Order 
Types: 
Initial Purchase 
Subsequent  Purchase 
Redemption 
 
Buy side Fund Name 
(voluntary share class 
exchange) 
 
(Large Trade Details 
table) 
buyFundN
ame 
A/N OC 60   Required if  Order Type is 
Voluntary Share Class 
Exchange 
 
Not allowed for Order 
Types: 
Initial Purchase 
Subsequent Purchase 
Redemption 
 
Buy Side account # 
(voluntary share class 
exchange) 
 
(Large Trade Details 
table) 
buyAccou
nt 
A/N O  20      
Not allowed for Order 
Types: 
Initial Purchase 
Subsequent purge 
Purchase 
Redemption 
 
Trade Amount 
 
(Large Trade Details 
table) 
tradeAmo
unt 
A/N R 17   99999999999999.99 
Time Horizon 
(months) 
 
(Large Trade Details 
table) 
timeHoriz
on 
A/N O 2   Allowed values from  
01 to 99 
Submitting Agent [[ID]] 
for Trade 
 
(Large Trade Details 
table) 
subAgentI
dTrade 
A/N O 8    
Submitting Agent 
Name for Trade 
 
(Large Trade Details 
table) 
subAgent
Name 
A/N R 30    
Settling Agent [[ID]] for 
Trade 
 
(Large Trade Details 
table) 
settAgentI
dTrade 
A/N O 8    
Settling Agent Name 
for Trade 
 
settAgent
Name 
A/N O 30    

---

## Page 128

MF INFO XCHANGE 
Create Notification Step 2 -  Large Trade Notification 128 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Large Trade Details 
table) 
Underlying Firm 
Symbol – 
Correspondent 
 
(Large Trade Details 
table) 
undFirmS
ymbol 
A/N O 5    
Underlying Firm Name 
– Correspondent 
 
(Large Trade Details 
table) 
undFirmN
ame 
A/N O 30    
Large Trade Dollar 
Threshold Amount 
 
(Large Trade Details 
table) 
largeTrad
eDollorTh
reshold 
A/N R 17   99999999999999.99 
 
This field is populated 
from MFPS Database 
 
Should be populated to 
‘Not Available in MF 
Profile Security’ if not 
available in MFPS’ 
N/A status 
 
(Large 
Trade 
Details 
table) 
A/N O/C 1 N/A Can be populated 
with values from 
the Description 
Column 
 
Not allowed on 
the “Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows 
within this table 
must be provided 
with the 
corresponding 
“rowId” and 
“status” fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Large 
Trade 
Details 
table) 
Integer O/C 11 N/A Not allowed on 
the “Create a 
Notification” 
endpoint. 
 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  

---

## Page 129

MF INFO XCHANGE 
Create Notification Step 2 -  Large Trade Notification 129 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. All 
existing rows 
within this table 
must be provided 
with the 
corresponding 
“rowId” and 
“status” fields. 
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comments largeTrad
eCommen
t 
A/N O 4000   Special characters 
allowed 
 
 
 
  

---

## Page 130

MF INFO XCHANGE 
Create Notification Step 2 - New Fund/New Share Class Launch 130 
 
CREATE NOTIFICATION STEP 2 - NEW FUND/NEW SHARE 
CLASS LAUNCH 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Notification  notificatio
nType 
A/N R  Can select from 
drop down 
 
Can be 
populated 
with Values 
from 
Description  
 
• New Fund 
• New Share Class 
 
Number of New Funds 
  
noOfNew
Funds 
A/N O  2 This field is only 
available if 
Notification 
selection is 
“New Fund” 
otherwise it 
should be not 
displayed on UI  
 
This field is 
only available 
if Notification 
selection is 
“New Fund” 
If the Notification 
selection is “New Share 
Class” then this field 
should be populated with 
“N/A” on the Excel 
Template 
Fund information is 
available in [[NSCC]] 
MFPS Profile Security 
Database  
 
  
fundInfor
mation 
A/N R  Can select from 
drop down 
 
 
  
 
Can be 
populated 
with Values 
from 
Description  
 
  
 
• Yes 
• No 
• Will be Added on 
 
Fund Information Date fundInfor
mationDa
te 
Date OC 10 Calendar picker  MM/DD/CCYY 
This field can be 
backdated 
 
Required if Fund 
information is available in 
[[NSCC]] MFPS Profile 
Security Database  
= “Will be Added on” 
Fund Number 
 
(Fund Information 
table)  
fundNum
ber 
A/N O 8    
Security Issue [[ID]] 
  
(Fund Information 
table) 
secIssueId A/N O 9    
Fund Name 
 
(Fund Information 
table)  
fundNam
e 
A/N O 60    
Ticker 
 
fundTicke
r 
A/N O 12    

---

## Page 131

MF INFO XCHANGE 
Create Notification Step 2 - New Fund/New Share Class Launch 131 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
(Fund Information 
table)  
Share Class 
 
(Fund Information 
table)  
 
  
fundShare
Class 
A/N O 20    
[[NSCC]] Fund/SERV 
Eligible 
 
(Fund Information 
table)   
nsccFundE
ligible 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Tax [[ID]] 
 
(Fund Information 
table)  
taxId A/N O 15   Special characters allowed 
N/A status 
 
(Fund 
Informati
on table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Fund 
Informati
on table) 
 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  

---

## Page 132

MF INFO XCHANGE 
Create Notification Step 2 - New Fund/New Share Class Launch 132 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comment 
 
 
Notificatio
nCommen
t 
 
A/N O 4000   Special characters allowed 
 
  

---

## Page 133

MF INFO XCHANGE 
Create Notification Step 2 -  Price/Rate Error 133 
 
CREATE NOTIFICATION STEP 2 -  PRICE/RATE ERROR 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Fund Number 
 
(Impacted Funds 
table) 
fundNum
ber 
A/N O 8    
Security Issue [[ID]] 
  
(Impacted Funds 
table) 
secIssueId A/N O  9    
Fund Name 
 
(Impacted Funds 
table)   
fundNam
e 
A/N R 60    
Ticker 
 
(Impacted Funds 
table)  
fundTicke
r 
A/N O 12    
Share Class 
 
(Impacted Funds 
table)  
fundShare
Class 
A/N O 20    
Price/Trade Date 
 
(Impacted Funds 
table)  
tradeDate Date R 10 Calendar picker  MM/DD/CCYY 
This date can be 
backdated 
Original NAV   
 
(Impacted Funds 
table) 
originalNa
v 
A/N OC 19   9999999999.99999999 
 
This field not allowed  if   
issue Type is Rate 
Revised NAV 
  
(Impacted  Funds 
table) 
revisedNa
v 
A/N OC 19   9999999999.99999999 
This field not allowed  if   
issue Type is Rate 
Original Rate 
 
(Impacted Funds 
table) 
originalRa
te 
A/N OC 10   99.9999999  
 
This field not allowed if 
Issue Type is Price 
Revised Rate 
  
(Impacted Funds 
table) 
revisedRat
e 
A/N OC 10   99.9999999  
 
This field not allowed if 
Issue Type is Price 

---

## Page 134

MF INFO XCHANGE 
Create Notification Step 2 -  Price/Rate Error 134 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Rate Type 
  
(Impacted Funds 
table) 
rateType A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Daily Accrual 
[[Dividend]] 
• [[Equity]] [[Dividend]] 
• Special [[Dividend]] 
• Short Term 
Capital Gain 
• Long Term 
Capital Gain  
  
This field not allowed if 
Issue Type is Price 
Accrual Period Start 
Date 
  
(Impacted Funds 
table) 
accuralPer
iodStartD
ate 
Date O 10 Calendar picker  MM/DD/CCYY 
This date can be 
backdated 
 
This field not allowed if 
Issue Type is Price 
Accrual Period End 
Date 
 
(Impacted Funds 
table) 
  
accuralPer
iodEndDat
e 
Date O 10 Calendar picker  MM/DD/CCYY 
This date can be 
backdated 
 
This field not allowed if 
Issue Type is Price 
Correction sent 
through MFPS I Price 
and Rate File?  
If “Yes”, please 
provide a date when 
the correction was 
submitted. 
If “No”, please provide 
a date when the 
correction will be 
submitted.   
Enter “N/A” if not 
submitting 
 
(Impacted Funds 
table)  
correction
Sent 
A/N O 50   Special characters allowed 
Correction sent 
through MFPS I Price 
and Rate file in cycle # 
 
(Impacted Funds 
table)  
correction
Cycle 
A/N O 10   Special characters allowed 
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  

---

## Page 135

MF INFO XCHANGE 
Create Notification Step 2 -  Price/Rate Error 135 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the 
values assigned 
by MF Info 
Xchange. 
“Receive 
Notification Data 
for an Event [[ID]]” 
endpoint must be 
called to return 

---

## Page 136

MF INFO XCHANGE 
Create Notification Step 2 -  Price/Rate Error 136 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
the current 
version of the 
notification with 
the rowIds 
assigned to each 
row of the table 
Transaction 
Reprocessing 
Purchases Will the 
Fund reprocess? 
  
purchaseR
eprocess 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Transaction 
Reprocessing 
Purchases Date 
 
  
purchase
Date 
Date OC 10 Calendar picker  MM/DD/CCYY 
This date can be 
backdated 
 
If Transaction 
Reprocessing Purchase 
Will the Fund reprocess is 
“Yes” this field is required 
to be populated. 
Otherwise this field 
cannot be populated 
Transaction 
Reprocessing 
Purchases Does De 
Minimis apply? 
  
purchase
DeMinAp
ply 
A/N OC   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
 •Yes 
 •No 
 
If Transaction 
Reprocessing Purchase 
Will the Fund reprocess is 
“Yes” this field is required 
to be populated. 
Otherwise this field 
cannot be populated 
Transaction 
Reprocessing 
Purchases De Minimis 
$ Amount 
  
purchase
DeMinAm
t 
A/N OC 19   999999999.999999999 
 
If Transaction 
Reprocessing Purchase 
Will the Fund reprocess is 
“Yes” this field is required 
to be populated. 
Otherwise this field 
cannot be populated 
Transaction 
Reprocessing 
Redemptions Will the 
Fund reprocess? 
  
redemptio
nReproces
s 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Transaction 
Reprocessing 
Redemptions Date 
  
redemptio
nDate 
Date OC 10 Calendar picker  MM/DD/CCYY 
 
This date can be 
backdated 
 
If Transaction 
Reprocessing Purchase 
Will the Fund reprocess is 
“Yes” this field is allowed 

---

## Page 137

MF INFO XCHANGE 
Create Notification Step 2 -  Price/Rate Error 137 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
to be populated. 
Otherwise this field 
cannot be populated 
 
Transaction 
Reprocessing 
Redemptions Does De 
Minimis apply? 
  
redemptio
nDeMinA
pply 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
 •Yes 
 •No 
 
If Transaction 
Reprocessing 
Redemptions Will the 
Fund reprocess is “Yes” 
this field is allowed to be 
populated. Otherwise this 
field cannot be populated 
Transaction 
Reprocessing 
Redemptions De 
Minimis $ Amount 
  
redemptio
nDeMinA
mt 
A/N OC 19    999999999.999999999 
 
If Transaction 
Reprocessing 
Redemptions Will the 
Fund reprocess is “Yes” 
this field is  allowed to be 
populated. Otherwise this 
field cannot be populated 
Transaction 
Reprocessing 
Exchanges In Will the 
Fund reprocess? 
  
exchanges
InReproce
ss 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Transaction 
Reprocessing 
Exchanges In Date 
  
exchanges
InDate 
Date OC 10 Calendar picker  MM/DD/CCYY 
 
This date can be 
backdated 
 
If Transaction 
Reprocessing Exchanges 
In Will the Fund reprocess 
is “Yes” this field is 
allowed to be populated. 
Otherwise this field 
cannot be populated 
 
Transaction 
Reprocessing 
Exchanges In Does De 
Minimis apply? 
  
exchanges
InDeMinA
pply 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
 
If Transaction 
Reprocessing Exchanges 
In Will the Fund reprocess 
is “Yes” this field is 
allowed to be populated. 
Otherwise this field 
cannot be populated 
Transaction 
Reprocessing 
exchanges
InDeMinA
mt 
 A/N OC 19   999999999.999999999 
 

---

## Page 138

MF INFO XCHANGE 
Create Notification Step 2 -  Price/Rate Error 138 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Exchanges In De 
Minimis $ Amount 
  
If Transaction 
Reprocessing Exchanges 
In Will the Fund reprocess 
is “Yes” this field is 
allowed to be populated. 
Otherwise this field 
cannot be populated 
Transaction 
Reprocessing 
Exchanges Out Will 
the Fund reprocess? 
  
exchanges
OutRepro
cess 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Transaction 
Reprocessing 
Exchanges Out Date  
exchanges
OutDate 
A/N OC 10 Calendar picker  MM/DD/CCYY 
 
This date can be 
backdated 
 
If Transaction 
Reprocessing Exchanges 
Out Will the Fund 
reprocess is “Yes” this 
field is allowed to be 
populated.  
Otherwise this field 
cannot be populated 
 
Transaction 
Reprocessing 
Exchanges Out Does 
De Minimis apply?  
exchanges
OutDeMin
Apply 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
If Transaction 
Reprocessing Exchanges 
Out Will the Fund 
reprocess is “Yes” this 
field is allowed to be 
populated. Otherwise this 
field cannot be populated 
Transaction 
Reprocessing 
Exchanges Out De 
Minimis $ Amount 
  
exchanges
OutDeMin
Amt 
A/N OC 19   999999999.999999999 
 
If Transaction 
Reprocessing Exchanges 
Out Will the Fund 
reprocess is “Yes” this 
field is allowed to be 
populated. Otherwise this 
field cannot be populated 
Transaction 
Reprocessing [[Dividend]] 
Reinvestment Will the 
Fund reprocess?  
divReinvR
eprocess 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Transaction 
Reprocessing [[Dividend]] 
Reinvestment Date 
 
  
divReinvD
ate 
A/N OC 10 Calendar picker  MM/DD/CCYY 
 
This date can be 
backdated 
 

---

## Page 139

MF INFO XCHANGE 
Create Notification Step 2 -  Price/Rate Error 139 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
If Transaction 
Reprocessing [[Dividend]] 
Will the Fund reprocess is 
“Yes” this field is allowed 
to be populated.  
Otherwise this field 
cannot be populated 
 
Transaction 
Reprocessing [[Dividend]] 
Reinvestment Does De 
Minimis apply? 
 
  
divReinvD
eMinAppl
y 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
If Transaction 
Reprocessing [[Dividend]] 
Will the Fund reprocess is 
“Yes” this field is allowed 
to be populated. 
Otherwise this field 
cannot be populated 
Transaction 
Reprocessing [[Dividend]] 
Reinvestment De 
Minimis $ Amount 
 
divReinvD
eMinAmt 
 A/N OC 19   999999999.999999999 
 
If Transaction 
Reprocessing [[Dividend]] 
Will the Fund reprocess is 
“Yes” this field is allowed 
to be populated. 
Otherwise this field 
cannot be populated 
Transaction 
Reprocessing Share 
Class Conversions In 
Will the Fund 
reprocess? 
 
shareInRe
process 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Transaction 
Reprocessing Share 
Class Conversions In 
Date 
 
shareInDa
te 
A/N OC 10 Calendar picker  MM/DD/CCYY 
 
This date can be 
backdated 
 
If Transaction 
Reprocessing Share Class 
Conversions In Will the 
Fund reprocess is “Yes” 
this field is allowed to be 
populated.  
Otherwise this field 
cannot be populated 
 
Transaction 
Reprocessing Share 
Class Conversions In 
Does De Minimis 
apply? 
 
shareInDe
MinApply 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
If Transaction 
Reprocessing Share Class 
Conversions In Will the 
Fund reprocess is “Yes” 
this field is allowed to be 

---

## Page 140

MF INFO XCHANGE 
Create Notification Step 2 -  Price/Rate Error 140 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
populated. Otherwise this 
field cannot be populated 
Transaction 
Reprocessing Share 
Class Conversions In 
De Minimis $ Amount 
 
shareInDe
MinAmt 
A/ N OC 19   999999999.999999999 
 
If Transaction 
Reprocessing Share Class 
Conversions In Will the 
Fund reprocess is “Yes” 
this field is allowed to be 
populated. Otherwise this 
field cannot be populated 
Transaction 
Reprocessing Share 
Class Conversions Out 
Will the Fund 
reprocess? 
 
shareOut
Reprocess 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Transaction 
Reprocessing Share 
Class Conversions Out 
Date 
shareOut
Date 
A/N OC 10 Calendar picker  MM/DD/CCYY 
 
This date can be 
backdated 
 
If Transaction 
Reprocessing Share Class 
Conversions Out Will the 
Fund reprocess is “Yes” 
this field is allowed to be 
populated.  
Otherwise this field 
cannot be populated 
 
Transaction 
Reprocessing Share 
Class Conversions Out 
Does De Minimis 
apply? 
shareOut
DeMinAp
ply 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
If Transaction 
Reprocessing Share Class 
Conversions Out Will the 
Fund reprocess is “Yes” 
this field is allowed to be 
populated. Otherwise this 
field cannot be populated 
Transaction 
Reprocessing Share 
Class Conversions Out 
De Minimis $ Amount   
shareOut
DeMinAm
t 
A/N OC 19     999999999.999999999 
 
If Transaction 
Reprocessing Share Class 
Conversions Out Will the 
Fund reprocess is “Yes” 
this field is allowed to be 
populated. Otherwise this 
field cannot be populated 
Transaction 
Correction/ 
Reprocessing 
Comment  
reprocessi
ngComme
nt 
A/N O 1000   Special characters allowed 

---

## Page 141

MF INFO XCHANGE 
Create Notification Step 2 -  Price/Rate Error 141 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
Will the fund correct 
month-to-date 
accrual?  
  
monToDat
eAccural 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Month-to-date accrual 
correction date 
  
monToDat
eCorrectio
n 
Date OC 10 Calendar picker  MM/DD/CCYY 
 
This date can be 
backdated 
 
If Will the fund correct 
month-to-date accrual?  
is “Yes” this field is 
required to be populated.  
Comment  notificatio
nCommen
t 
A/N O 4000    Special characters allowed 
 
 
 
 
  

---

## Page 142

MF INFO XCHANGE 
Create Notification Step 2 -  Prospectus Change 142 
 
CREATE NOTIFICATION STEP 2 -  PROSPECTUS CHANGE   
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Security Issue [[ID]] 
 
(Impacted Funds 
table)  
secIssueId A/N O 9    
Fund Name 
 
(Impacted Funds 
table) 
fundNam
e 
A/N O 60    
Ticker 
  
(Impacted Funds 
table) 
fundTicke
r 
A/N O 12    
Share Class  
 
(Impacted Funds 
table) 
fundShare
Class 
A/N O 20    
Change Type 
 
(Impacted Funds 
table) 
  
changeTy
pe 
A/N R   Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Frequent 
Trading Policy 
• Load Waivers 
• Involuntary 
Share Class 
Exchange 
• Voluntary Share 
Class Moves 
• Reinstatement 
Privilege 
• Other 
 
Change Type-Other    
 
(Impacted Funds 
table) 
changeTy
peOther 
A/N OC 100   Allowed if Change Type = 
Other 
 
Special characters allowed 
From 
 
(Impacted Funds 
table) 
  
from A/N O 1000   Special characters allowed 
To 
 
(Impacted Funds 
table) 
  
to A/N O 1000   Special characters allowed 
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 

---

## Page 143

MF INFO XCHANGE 
Create Notification Step 2 -  Prospectus Change 143 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 

---

## Page 144

MF INFO XCHANGE 
Create Notification Step 2 -  Prospectus Change 144 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comment 
  
prospectu
sCommen
t 
A/N O 4000   Special characters allowed 
  

---

## Page 145

MF INFO XCHANGE 
Create Notification Step 2 -  Purchase Maximum Change 145 
 
CREATE NOTIFICATION STEP 2 -  PURCHASE MAXIMUM 
CHANGE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Fund Number 
 
(Impacted Funds 
table) 
fundNum
ber 
A/N O 8    
Security Issue [[ID]] 
 
(Impacted Funds 
table) 
secIssueId A/N O 9    
Fund Name 
 
(Impacted Funds 
table)  
fundNam
e 
A/N O 10    
Ticker 
 
(Impacted Funds 
table)  
fundTicke
r 
A/N O 12    
Share Class 
 
(Impacted Funds 
table)  
fundShare
Class 
A/N O 20     
From Maximum Value 
  
 
(Impacted Funds 
table) 
fromMax
Value 
A/N OC 17   99999999999999.99 
 
From Maximum Value & 
To Maximum Value 
should not be same 
 
 Required if “To Maximum 
Value” or “Maximum 
Change Applies to” is 
populated 
  
To Maximum Value 
 
(Impacted Funds 
table)  
  
toMaxVal
ue 
 A/N OC 17   99999999999999.99 
From Maximum Value & 
To Maximum Value 
should not be same 
 
Required if “From 
Maximum Value” or 
“Maximum Change 
Applies to” is populated 
 
 
Maximum Change 
Applies to 
  
maxChang
eAppliesT
o 
 A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
• Maximum Account 
Value Amount 

---

## Page 146

MF INFO XCHANGE 
Create Notification Step 2 -  Purchase Maximum Change 146 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds 
table)  
 
from 
Description  
• Maximum Purchase 
Amount  
Required if “From 
Maximum Value” or “To 
Maximum Value” is 
populated 
Maximum Account 
Value Code 
  
(Impacted Funds 
table)  
 
maxAccVa
lCode 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Fund Complex 
•       Share Class  
•  Individual Security      
Issue [[ID]] 
 
Allowed when “Maximum 
Change Applies To” 
=Maximum Account Value 
Amount”.   
 
Not allowed when 
“Maximum Change 
Applies To” =Maximum 
Purchase Amount”. 
Exceptions 
  
(Impacted Funds 
table)   
impFunds
Exception
s 
A/N O 250    
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 147

MF INFO XCHANGE 
Create Notification Step 2 -  Purchase Maximum Change 147 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
“status” 
fields.  
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comment 
 
notificatio
nCommen
t 
A/N O 4000    
 
 
 
  

---

## Page 148

MF INFO XCHANGE 
Create Notification Step 2 -  Purchase Minimum Change 148 
 
CREATE NOTIFICATION STEP 2 -  PURCHASE MINIMUM 
CHANGE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Fund Number 
 
(Impacted Funds 
table) 
fundNum
ber 
A/N O 8    
        
Security Issue [[ID]] 
  
(Impacted Funds 
table)  
secIssueId A/N O 9    
Fund Name 
 
(Impacted Funds 
table)   
fundNam
e 
A/N O 10    
Ticker 
 
(Impacted Funds 
table)  
fundTicke
r 
A/N O 12    
Share Class 
 
(Impacted Funds 
table)   
fundShare
Class 
A/N O 20     
From Minimum Value 
  
(Impacted Funds 
table)  
 
fromMinV
alue 
A/N OC 17   99999999999999.99 
From Minimum Value & 
To Minimum Value should 
not be same 
 
Required if “To Minimum 
Value” or “Minimum 
Change Applies to” is 
populated 
  
To Minimum Value 
 
(Impacted Funds 
table)  
 
  
toMinValu
e 
 A/N OC 17   99999999999999.99 
From Minimum Value & 
To Minimum Value should 
not be same 
 
Required if “From 
Minimum Value” or 
“Minimum Change Applies 
to” is populated 
 
 

---

## Page 149

MF INFO XCHANGE 
Create Notification Step 2 -  Purchase Minimum Change 149 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Minimun Change 
Applies to 
 
(Impacted Funds 
table)  
 
 
minChang
eAppliesT
o 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•  Minimum Initial   
Purchase Amount 
• Minimum Subsequent 
Purchase Amount 
• Minimum IRA/Roth 
IRA Initial Purchase 
Amount 
• Minimum IRA/Roth 
IRA Subsequent Purchase 
Amount 
• Minimum Coverdell 
IRA Purchase Amount 
• Minimum Coverdell 
IRA Subsequent Purchase 
Amount 
• Minimum Wrap 
Initial Purchase Amount 
• Minimum Wrap 
Subsequent Purchase 
Amount 
• Minimum Qualified 
Plans Initial Purchase 
Amount 
• Minimum Qualified 
Plans Subsequent 
Purchase Amount 
• Minimum 
Periodic/Systematic 
Investment Purchase 
Amount   
• Minimum Initial 
Purchase Amount Non-
Qualified Plan 
• Minimum 
Subsequent Purchase 
Amount Non-Qualified 
Plan 
• Minimum Initial 
Purchase Amount 
(Omnibus Account) 
• Minimum 
Subsequent Purchase 
Amount (Omnibus 
Account) 
• Minimum Initial 
Purchase Amount via an 
Exchange 
• Minimum 
Subsequent Purchase 
Amount via an Exchange 
 
Required if From 
Minimum Value or To 

---

## Page 150

MF INFO XCHANGE 
Create Notification Step 2 -  Purchase Minimum Change 150 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Minimum Value is 
populated 
  
 
Exceptions 
 
(Impacted Funds 
table)   
impFunds
Exception
s 
A/N O 250   Special characters allowed 
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  

---

## Page 151

MF INFO XCHANGE 
Create Notification Step 2 -  Purchase Minimum Change 151 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comment 
 
 
notificatio
nCommen
t 
A/N O 4000   Special characters allowed 
 
 
  

---

## Page 152

MF INFO XCHANGE 
Create Notification Step 2 -  Share Class Conversion/Exchange 152 
 
CREATE NOTIFICATION STEP 2 -  SHARE CLASS 
CONVERSION/EXCHANGE 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Number of 
months/years [[shares]] 
must age 
sharesAge N O 3   Number of months/years 
[[shares]] must age. Numeric 
value 
Number of 
months/years [[shares]] 
must age 
sharesMy A/N OC   Select from 2 
radial buttons 
Can be 
populated 
with Values 
from 
Description 
 
Number of Months/years 
[[shares]] must age 
 
• Months 
• Years 
 
Required if “Number of 
months/years [[shares]] must 
age” (sharesAge) field is 
populated with a valid 
value. 
From Fund Number 
 
(Impacted Funds 
table)    
fromFund
Number 
A/N O 8    
From Security Issue [[ID]] 
  
(Impacted Funds 
table)   
fromSecIs
sueId 
A/N O 9    
From Fund Name 
 
(Impacted Funds 
table)    
fromFund
Name 
A/N O 60    
From Ticker 
 
(Impacted Funds 
table)    
fromFund
Ticker 
A/N O 12    
From Share Class 
  
(Impacted Funds 
table)   
fromFund
ShareClas
s 
A/N O 20    
To Fund Number 
  
(Impacted Funds 
table)   
toFundNu
mber 
A/N O 8    
To Security Issue [[ID]] 
 
(Impacted Funds 
table)    
toSecIssue
[[ID]] 
A/N O 9    
To Fund Name 
 
toFundNa
me 
A/N O 60    

---

## Page 153

MF INFO XCHANGE 
Create Notification Step 2 -  Share Class Conversion/Exchange 153 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds 
table)    
To Ticker 
  
(Impacted Funds 
table)    
toFundTic
ker 
A/N O 12    
To Share Class 
 
(Impacted Funds 
table)    
toFundSh
areClass 
A/N O 20    
Conversion Date 
  
(Impacted Funds 
table)    
conversio
nDate 
Date O 10 Calendar picker  MM/DD/CCYY 
This date can be 
backdated 
 
N/A status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  

---

## Page 154

MF INFO XCHANGE 
Create Notification Step 2 -  Share Class Conversion/Exchange 154 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Exceptions Apply 
  
exceptionI
nd 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No  
 
Defaults to ‘No’ 
Exceptions 
  
(Exceptions table) 
comment A/N O 1000   Special characters allowed 
 
SYSTEM allows up to 10 
exceptions 
Networking Share 
Class Conversion 
Activity Records (F55) 
Date  
  
netDateF5
5 
Date O 10 Calendar picker  MM/DD/CCYY 
This date can be 
backdated 
 
Networking Share 
Class Conversion 
Activity Records (F55) 
Transaction Type 
value 
  
netF55Tra
nTypeVal 
A/N O 250   Special characters allowed 
Extended NAV (Y/N) 
  
extended
NavInd 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•     Yes 
•     No 

---

## Page 155

MF INFO XCHANGE 
Create Notification Step 2 -  Share Class Conversion/Exchange 155 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Anticipated Extended 
NAV availability date 
  
extended
NavDate 
Date O 10 Calendar picker  MM/DD/CCYY 
This date can be 
backdated 
 
Extended NAV applies 
to: Closing Fund / New 
Fund 
  
extended
NavApplie
s 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Closing Fund 
• New Fund 
Client Notification 
Date  
clientNotif
icationDat
e 
Date O 10 Calendar picker  MM/DD/CCYY 
This date can be 
backdated 
 
Comment 
 
  
shareClass
ConExcCo
mment 
A/N O 4000   Special characters allowed 
 
 
  

---

## Page 156

MF INFO XCHANGE 
Create Notification Step 2 -  Share Class Eligibility Change 156 
 
CREATE NOTIFICATION STEP 2 -  SHARE CLASS ELIGIBILITY 
CHANGE 
 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Share Class 
 
(Impacted Share Class 
table)  
shareClass A/N O 20    
 Current Eligibility 
Language 
 
(Impacted Share Class 
table)  
currentEli
gibilityLan
g 
A/N O 250   Special characters allowed 
Impacted Share Class 
– Change in Eligibility 
 
(Impacted Share Class 
table)  
changeInE
ligibility 
A/N OC  250 The UI will 
expand to 
display 
everything 
entered in the 
field 
 Not allowed  
If Change Type = 
“Reminder”   
 
Special characters allowed 
New Eligibility 
Language 
 
(Impacted Share Class 
table)  
newEligibi
lityLang 
A/N OC  250   Not allowed  
If Change Type = 
“Reminder”   
 
Special characters allowed 
Fund Number 
 
(Impacted Funds 
table)  
fundNum
ber 
A/N O 8    
Security Issue [[ID]]  
 
(Impacted Funds 
table) 
secIssueId A/N O 9    
Fund Name 
 
(Impacted Funds 
table)  
fundNam
e 
A/N O 60    
Ticker  
 
(Impacted Funds 
table) 
fundTicke
r 
A/N O 12    
Share Class  
 
(Impacted Funds 
table) 
fundShare
Class 
A/N O 20    
N/A status 
 
A/N O/C 1 N/A Can be 
populated 
with values 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 

---

## Page 157

MF INFO XCHANGE 
Create Notification Step 2 -  Share Class Eligibility Change 157 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted 
Funds 
table) 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 

---

## Page 158

MF INFO XCHANGE 
Create Notification Step 2 -  Share Class Eligibility Change 158 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comment 
  
notificatio
nCommen
t 
A/N O 4000   Special characters allowed 
 
 
  

---

## Page 159

MF INFO XCHANGE 
Create Notification Step 2 -  Share Split 159 
 
CREATE NOTIFICATION STEP 2 -  SHARE SPLIT  
 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Share Split Type shareSplit
Type 
A/N O  Can select from 
drop down 
 Can be 
populated 
with Values 
from 
Description 
• Forward Split 
• Reverse Split 
• Reverse and Forward 
Split 
 
The splits will apply to 
shareholders of record 
as of  
splitApply
Date 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be 
backdated 
Fund Number 
 
(Impacted Funds– 
Forward Split table) 
  
fsFundNu
mber 
A/N O 8 If “Forward 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Forward Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Forward 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Security Issue [[ID]]  
 
(Impacted Funds– 
Forward Split table) 
fsSecIssue
[[ID]] 
A/N O 9 If “Forward 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Forward Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Forward 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Fund Name 
  
(Impacted Funds– 
Forward Split table) 
fsFundNa
me 
A/N O 60 If “Forward 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Forward Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Forward 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Ticker 
  
fsFundTic
ker 
A/N O 12 If “Forward 
Split” or 
Can be 
populated if     
 

---

## Page 160

MF INFO XCHANGE 
Create Notification Step 2 -  Share Split 160 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted Funds– 
Forward Split table) 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Forward Split 
table will be 
displayed on the 
UI 
 
“Forward 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
Share Class 
  
(Impacted Funds– 
Forward Split table) 
fsFundSha
reClass 
A/N O 20 If “Forward 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Forward Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Forward 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Tax [[ID]] 
  
(Impacted Funds– 
Forward Split table) 
fsTaxId  A/N  O 15 If “Forward 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Forward Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Forward 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Forward  Split Ratio 
(New to Old) 
(format: 4:1) 
  
(Impacted Funds– 
Forward Split table) 
fwdSplitR
atio 
A/N  O 50 If “Forward 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Forward Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Forward 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
  
  
 
Networking Activity 
File (F55) 
Transaction Code   
 
(Impacted Funds– 
Forward Split table) 
fsNetActFi
le 
A/N O 20 If “Forward 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Can be 
populated if     
“Forward 
Split” or 
“Reverse and 
Forward 
 

---

## Page 161

MF INFO XCHANGE 
Create Notification Step 2 -  Share Split 161 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Impacted Funds 
– Forward Split 
table will be 
displayed on the 
UI 
 
Split” as 
Share Split 
Type is 
selected   
N/A status 
 
(Impacted 
Funds– 
Forward 
Split table 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds– 
Forward 
Split table 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 

---

## Page 162

MF INFO XCHANGE 
Create Notification Step 2 -  Share Split 162 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
the 
correspondin
g “rowId” and 
“status” 
fields. 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Fund Number 
  
(Impacted Funds– 
Reverse Split table) 
 
rsFundNu
mber 
A/N O 8 If “Reverse 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Reverse Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Reverse 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Security Issue [[ID]] 
 
(Impacted Funds– 
Reverse Split table) 
 
 
  
rsSecIssue
[[ID]] 
A/N O 9 If “Reverse 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Reverse Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Reverse 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Fund Name 
 
(Impacted Funds– 
Reverse Split table) 
 
  
rsFundNa
me 
A/N O 60 If “Reverse 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Reverse Split 
table will be 
displayed on the 
UI 
Can be 
populated if     
“Reverse 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 

---

## Page 163

MF INFO XCHANGE 
Create Notification Step 2 -  Share Split 163 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
 
Ticker 
 
(Impacted Funds– 
Reverse Split table) 
 
  
rsFundTic
ker 
A/N O 12 If “Reverse 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Reverse Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Reverse 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Share Class 
 
(Impacted Funds– 
Reverse Split table) 
 
  
rsFundSha
reClass 
A/N O 20 If “Reverse 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Reverse Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Reverse 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Tax [[ID]]  
 
(Impacted Funds– 
Reverse Split table) 
 
rsTaxId  A/N  O 15 If “Reverse 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Reverse Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Reverse 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Reverse Split Ratio 
(New to Old) 
(format: 1:4) 
 
(Impacted Funds– 
Reverse Split table) 
 
  
revSplitRa
tio 
A/N  O 50 If “Reverse 
Split” or 
“Reverse and 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Reverse Split 
table will be 
displayed on the 
UI 
 
Can be 
populated if     
“Reverse 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
 
Networking Activity 
File (F55) 
Transaction Code 
rsNetActFi
le 
A/N O 20 If “Reverse 
Split” or 
“Reverse and 
Can be 
populated if     
“Reverse 
 

---

## Page 164

MF INFO XCHANGE 
Create Notification Step 2 -  Share Split 164 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
   
(Impacted Funds– 
Reverse Split table) 
 
Forward Split” 
as Share Split 
Type is selected,    
Impacted Funds 
– Reverse Split 
table will be 
displayed on the 
UI 
 
Split” or 
“Reverse and 
Forward 
Split” as 
Share Split 
Type is 
selected   
N/A 
 
status 
 
(Impacted 
Funds– 
Reverse 
Split 
table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A 
 
rowId 
 
(Impacted 
Funds– 
Reverse 
Split 
table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  

---

## Page 165

MF INFO XCHANGE 
Create Notification Step 2 -  Share Split 165 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Yes/No 
Blackout Date(s)  
   
blackoutD
ateYesOr
No 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Date(s)  
Blackout Date(s)   
  
blackoutD
ate 
Date OC 10 Calendar Picker 
On the UI 
After one date is 
selected User 
will be 
prompted – 
‘Add additional 
date, click on 
icon to Select’ 
Field box  for 
‘Blackout Date 
(s)’ will only be 
added if User 
decides to add 
additional date.    
 
 MM/DD/CCYY 
 
Required If Blackout 
Date(s) is Yes, this field 
must have a value. 
This field can have from 1 
to 5 dates 
 
Not allowed if Blackout 
Date (s) is ‘No’ 
 
  
 
Yes/No   
Will the fund accept 
DCC&S trades 
submitted  
on Blackout Date+1 as 
of Trade Date= 
Blackout  Date?   
dccsTrade
YesOrNo 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Date(s)   
Will the fund accept 
DCC&S trades 
submitted on Blackout 
dccsTrade
Dates 
     This field will be 
greyed out on 
UI 
 Not Allowed 

---

## Page 166

MF INFO XCHANGE 
Create Notification Step 2 -  Share Split 166 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Date+1 as of Trade 
Date= Blackout  Date?  
  
Direct Trading Date  
  
manualTr
adeDate 
Date O 10 Calendar Picker 
     
 MM/DD/CCYY 
  
This field can have from 1 
to 5 dates 
 
  
 
Instructions for 
placing manual trades 
   
manualTr
ade 
A/N O 500    
Trade estimated cut-
off time   
teTime A/N OC     Can select from 
drop down 
 Time Allowed based on 
half hour selection: 
• 0:30 
• 1:00 
• 1:30 
• 2:00 
• 2:30 
• 3:00 
• 3:30 
• 4:00 
• 4:30 
• 5:00 
• 5:30 
• 6:00 
• 6:30 
• 7:00 
• 7:30 
• 8:00 
• 8:30 
• 9:00 
• 9:30 
• 10:00 
• 10:30 
• 11:00 
• 11:30 
• 12:00 
• 12:30  
 
Required if AM/PM 
and/or Time Zone are 
populated 
 
 
Trade estimated cut-
off time   
 
AM/PM 
teTimeAm
Pm 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• AM 
• PM 
 
Required if Time or/and 
Time Zone are populated 

---

## Page 167

MF INFO XCHANGE 
Create Notification Step 2 -  Share Split 167 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
 
Trade Estimates 
Time Zone  
teTimeZo
ne 
A/N OC  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Eastern Time 
• Central Time 
• Mountain Time 
• Pacific Time 
• Alaska Time 
• Hawaii Time  
 
Required if Time or/and 
AM/PM are populated 
 
 
Trade Estimates 
Date 
  
  
teDate Date O 10 Calendar Picker  MM/DD/CCYY 
 
This date can be 
backdated 
Last date pre-split 
NAV will be sent  
  
lastDate Date O 10 Calendar Picker  MM/DD/CCYY 
 
This date can be 
backdated 
First date NAV will 
reflect post-split value 
  
firstDate Date O 10 Calendar Picker  MM/DD/CCYY 
 
This date can be 
backdated 
[[shares]] of the 
impacted funds will be 
offered on a split 
adjusted basis 
beginning on:  
   
splitAdjDa
te 
Date O 10 Calendar Picker  MM/DD/CCYY 
 
This date can be 
backdated 
This transaction is: 
   
taxTran A/N O    • Non-Taxable 
• Taxable 
 
Defaults to ‘ Non-Taxable’ 
Comment 
  
shareSplit
Comment 
A/N O 4000   Special characters allowed 
 
  

---

## Page 168

MF INFO XCHANGE 
Create Notification Step 2 -  Subadvisor Change 168 
 
CREATE NOTIFICATION STEP 2 -  SUBADVISOR CHANGE 
 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Subadvisor Change To  
  
to A/N O 250    
Fund Number 
 
(Impacted Funds 
table) 
  
fundNum
ber 
A/N O 8    
Security Issue [[ID]] 
 
(Impacted Funds 
table) 
secIssueId A/N O 9    
Fund Name 
  
(Impacted Funds 
table) 
fundNam
e 
A/N O 60    
Ticker 
  
(Impacted Funds 
table) 
fundTicke
r 
A/N O 12    
Share Class 
   
(Impacted Funds 
table) 
fundShare
Class 
A/N O 20    
N/A) status 
 
(Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 169

MF INFO XCHANGE 
Create Notification Step 2 -  Subadvisor Change 169 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
N/A rowId 
 
(Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comment 
 
  
subadviso
rCommen
t 
A/N O 4000    
 
  
 
 
  

---

## Page 170

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 170 
 
CREATE NOTIFICATION STEP 2 -  [[transfer agent]] 
CHANGE/FUND ACQUISITION 
 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Notification Type notificationT
ype 
A/N R  Can select from 
drop down 
Can be 
populated with 
Values from 
Description 
• Fund Acquisition 
with [[transfer agent]] 
(TA) Change 
• Fund Acquisition 
without Transfer 
Agent (TA) Change 
• [[transfer agent]] (TA) 
Change 
 
Acquisition Retiring 
Company Name  
retiringCom
panyName 
A/N O 100 If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected, 
then the 
Acquisition 
table will be 
displayed on the 
UI 
Can be 
populated if 
“Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected 
 
Acquisition Acquiring 
Company Name 
  
 
acquiringCo
mpanyName 
A/N O 100 If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected, 
then the 
Acquisition 
table will be 
displayed on the 
UI 
Can be 
populated if 
“Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected 
 
Fund Company Name 
 
(Impacted [[NSCC]] 
Participants Numbers 
table) 
  
 
fundCompan
yName 
A/N O 100 If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
 

---

## Page 171

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 171 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Notification 
Type is selected, 
then the 
Impacted [[NSCC]] 
[[participant]] 
Numbers table 
will be displayed 
on the UI 
without TA 
Change” 
Notification 
Type is selected 
[[NSCC]] [[participant]] 
Number 
  
(Impacted [[NSCC]] 
Participants Numbers 
table) 
  
 
nsccParticip
antNumber 
A/N O 8 If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected, 
then the 
Impacted [[NSCC]] 
[[participant]] 
Numbers table 
will be displayed 
on the UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected 
 
[[NSCC]] [[participant]] 
Number will be 
changed 
 
(Impacted [[NSCC]] 
Participants Numbers 
table) 
  
 
  
nsccParticip
antNumber
WillBeChang
ed 
A/N O  Can be selected 
from drop down 
 
If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected, 
then the 
Impacted [[NSCC]] 
[[participant]] 
Numbers table 
will be displayed 
on the UI 
Can be selected 
from 
Description 
 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected 
• Yes 
• No 
New [[NSCC]] [[participant]] 
Number 
  
(Impacted [[NSCC]] 
Participants Numbers 
table) 
  
 
newNsccPart
icipantNumb
er 
A/N OC 8 If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected, 
then the 
Impacted [[NSCC]] 
[[participant]] 
Numbers table 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“Fund 
Acquisition 
without TA 
Change” 
Notification 
Type is selected 
Required if  
the “[[NSCC]] [[participant]] 
Number”  is  “Yes” 
  
Not allowed if  
the “[[NSCC]] [[participant]] 
Number”  is  “No” 
 

---

## Page 172

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 172 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
will be displayed 
on the UI 
[[transfer agent]] from 
Name  
 
([[transfer agent]] 
Information 
Table) 
fromTANam
e 
A/N O 100 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
U 
Can be 
populated if  
“Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] from 
Phone Number(s)  
 
([[transfer agent]] 
Information 
Table) 
fromTAPhon
eNumber 
A/N O 50 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] from 
Fax(s) 
 
([[transfer agent]] 
Information 
Table) 
  
fromTAFax A/N O 50 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] from 
Email 
  
([[transfer agent]] 
Information 
Table) 
fromTAEmail A/N O 100 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
Email must be in the 
proper format: 
Recipient name@   
Domain name 
  
 
[[transfer agent]] from 
Office Hours (from – 
to times) 
  
([[transfer agent]] 
Information 
Table) 
fromTAOffic
eHours 
A/N O 50 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 

---

## Page 173

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 173 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Info table will be 
displayed on the 
UI 
[[transfer agent]] from 
Mailing Address 
(regular mail) 
 
([[transfer agent]] 
Information 
Table) 
 
  
fromTAMaili
ngAddressRe
gular 
A/N O 500 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] from 
Mailing Address 
(overnight mail) 
  
([[transfer agent]] 
Information 
Table) 
 
fromTAMaili
ngAddressO
vernight 
A/N O 500 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] from 
Wire Transfer 
Instructions 
 
([[transfer agent]] 
Information 
Table) 
   
fromTAWire A/N O 500 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] from 
Website URL 
  
([[transfer agent]] 
Information 
Table) 
fromTAWeb
siteUrl 
A/N O 100 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] to 
Name 
 
([[transfer agent]] 
Information 
Table) 
toTAName A/N O 100 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
 

---

## Page 174

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 174 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
  [[transfer agent]] 
Info table will be 
displayed on the 
UI 
Notification 
Type is selected 
[[transfer agent]] to 
Phone Number(s) 
  
([[transfer agent]] 
Information 
Table) 
toTAPhoneN
umber 
A/N O 50 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] to 
Fax(s) 
   
([[transfer agent]] 
Information 
Table) 
toTAFax A/N O 50 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] to 
Email 
 
 
([[transfer agent]] 
Information 
Table) 
  
toTAEmail A/N O 100 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
Email must be in the 
proper format: 
Recipient name@   
Domain name 
  
 
[[transfer agent]] to 
Office Hours (from – 
to times) 
  
([[transfer agent]] 
Information 
Table) 
toTAOfficeH
ours 
A/N O 50 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] to 
Mailing Address 
(regular mail) 
 
([[transfer agent]] 
Information 
toTAMailing
AddressRegu
lar 
A/N O 500 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
 

---

## Page 175

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 175 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Table) 
  
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Notification 
Type is selected 
[[transfer agent]] to 
Mailing Address 
(overnight mail) 
  
([[transfer agent]] 
Information 
Table) 
toTAMailing
AddressOver
night 
A/N O 500 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] to Wire 
Transfer Instructions 
  
([[transfer agent]] 
Information 
Table) 
toTAWire A/N O 500 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
[[transfer agent]] to 
Website URL 
 
([[transfer agent]] 
Information 
Table) 
 
  
toTAWebsite
Url 
A/N O 100 If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected, 
then the 
[[transfer agent]] 
Info table will be 
displayed on the 
UI 
Can be 
populated  
If “Fund 
Acquisition with 
TA Change” or 
“TA Change” 
Notification 
Type is selected 
 
Account Numbers will 
change 
  
accountNum
berWillChan
ge 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No  
TA Fund Numbers will 
change 
 
  
taFundNum
berWillChan
ge 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 
Security Issue IDs will 
change 
 
  
securityIssue
IdWillChang
e 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 
Ticker symbols will 
change 
  
tickerSymbol
WillChange 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 

---

## Page 176

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 176 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Retiring Funds Current 
[[NSCC]] [[participant]] 
Number 
 
(Impacted Funds 
table) 
  
currNSCCNu
mber 
A/N O 8    
Retiring Funds Fund 
Number 
 
(Impacted Funds 
table) 
 
fromFundNu
mber 
A/N O 8    
Retiring Funds 
Security Issue [[ID]] 
  
(Impacted Funds 
table) 
 
fromSecIssu
eId 
A/N O 9    
Retiring Funds Fund 
Name 
  
(Impacted Funds 
table) 
 
fromFundNa
me 
A/N O 60    
Retiring Funds Ticker 
 
(Impacted Funds 
table) 
 
fromFundTic
ker 
A/N O 12    
Retiring Funds Share 
Class 
 
(Impacted Funds 
table) 
 
fromFundSh
areClass 
A/N O 20    
Acquiring Funds New 
[[NSCC]] [[participant]] 
Number 
  
(Impacted Funds 
table) 
 
newNSCCNu
mber 
A/N O 8    
Acquiring Funds Fund 
Number 
 
(Impacted Funds 
table) 
 
  
toFundNum
ber 
A/N O 8    
Acquiring Funds 
Security Issue [[ID]] 
 
toSecIssueId A/N O 9    

---

## Page 177

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 177 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
(Impacted Funds 
table) 
 
Acquiring Funds Fund 
Name 
  
toFundNam
e 
A/N O 60    
Acquiring Funds Ticker 
 
(Impacted Funds 
table) 
 
toFundTicke
r 
A/N O 12    
Acquiring Funds Share 
Class 
 
(Impacted Funds 
table) 
 
toFundShare
Class 
A/N O 20    
N/A 
 
status 
 
(Impacted 
Funds table) 
 
A/N O/C 1 N/A Can be 
populated with 
values from the 
Description 
Column 
 
Not allowed on 
the “Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. 
All existing rows 
within this table 
must be 
provided with 
the 
corresponding 
“rowId” and 
“status” fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A) rowId 
 
(Impacted 
Funds table) 
 
Integer O/C 11 N/A Not allowed on 
the “Create a 
Notification” 
endpoint. 
 
Required on the 
“Update a 
Notification” 
endpoint if the 
respective table 
contains data. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 

---

## Page 178

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 178 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
All existing rows 
within this table 
must be 
provided with 
the 
corresponding 
“rowId” and 
“status” fields. 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Trading through [[NSCC]] 
Fund/SERV 
Transactions 
 
T +1 [[settlement]] 
transaction A/N R     Hard Coded Value 
‘T + 1 [[settlement]]’ 
  
Trading through [[NSCC]] 
Fund/SERV Start Date 
- Transaction T+1 
[[settlement]] 
  
tranDate1 Date 0 10   MM/DD/CCYY  
This date can be 
backdated 
Trading through [[NSCC]] 
Fund/SERV End Date - 
Transaction T+1 
[[settlement]] 
   
tranDate2 Date 0 10   MM/DD/CCYY  
This date can be 
backdated 
Trading through [[NSCC]] 
Fund/SERV 
Accepted/Rejected - 
Transaction T+1 
[[settlement]]  
acceptedOrR
ejected 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Accepted 
• Rejected 
 
 
Trading through [[NSCC]] 
Fund/SERV [[settlement]] 
- Transaction T+1 
[[settlement]] 
 
[[settlement]] A/N O 50    
Trading through [[NSCC]] 
Fund/SERV Start Date 
- Transaction 
[[settlement]] greater 
than T+1  
transaction A/N R     Hard Coded Value 
‘[[settlement]] greater than 
T+1’ 
  

---

## Page 179

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 179 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Trading through [[NSCC]] 
Fund/SERV Start Date 
- Transaction 
[[settlement]] greater 
than T+1   
tranDate1 Date 0 10   MM/DD/CCYY  
This date can be 
backdated 
Trading through [[NSCC]] 
Fund/SERV Start Date 
- Transaction 
[[settlement]] greater 
than T+1    
tranDate2 Date 0 10   MM/DD/CCYY  
This date can be 
backdated 
Trading through [[NSCC]] 
Fund/SERV 
Accepted/Rejected - 
Transaction 
[[settlement]] greater 
than T+1 
acceptedOrR
ejected 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Accepted 
• Rejected 
 
 
Trading through [[NSCC]] 
Fund/SERV [[settlement]] 
- Transaction 
[[settlement]] greater 
than T+1 
 
[[settlement]] A/N O 50    
Trading through [[NSCC]] 
Fund/SERV Start Date 
– DCC&S Trades 
transaction A/N R     Hard Coded Value 
‘DCC&S Trades’ 
  
Trading through [[NSCC]] 
Fund/SERV Start Date 
– DCC&S Trades 
  
tranDate1 Date 0 10   MM/DD/CCYY  
This date can be 
backdated 
Trading through [[NSCC]] 
Fund/SERV End Date - 
DCC&S Trades 
  
tranDate2 Date 0 10   MM/DD/CCYY  
This date can be 
backdated 
Trading through [[NSCC]] 
Fund/SERV 
Accepted/Rejected - 
DCC&S Trades 
  
acceptedOrR
ejected 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Accepted 
• Rejected 
 
 
Trading through [[NSCC]] 
Fund/SERV [[settlement]] 
- DCC&S Trades 
  
[[settlement]] A/N O 50    
Trading through [[NSCC]] 
Fund/SERV 
Transactions 
 
Free Form 
 
  
transaction A/N O 50    Free Form field 
  
Can add up to 5 additional 
rows 
Trading through [[NSCC]] 
Fund/SERV Start Date 
  
tranDate1 Date 0 10   MM/DD/CCYY  
This date can be 
backdated 
 

---

## Page 180

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 180 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Can add up to 5 additional 
rows 
Trading through [[NSCC]] 
Fund/SERV End Date 
  
tranDate2 Date 0 10   MM/DD/CCYY  
This date can be 
backdated 
 
Can add up to 5 additional 
rows 
Trading through [[NSCC]] 
Fund/SERV 
Accepted/Rejected 
  
acceptedOrR
ejected 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Accepted 
• Rejected 
 
Can add up to 5 additional 
rows 
Trading through [[NSCC]] 
Fund/SERV [[settlement]] 
  
[[settlement]] A/N O 50   Can add up to 5 additional 
rows 
Transactions received 
on the effective date 
before: 
Hour 
  
transRecTim
eHour 
A/N OC  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• 1:00 
• 2:00 
• 3:00 
• 4:00 
• 5:00 
• 6:00 
• 7:00 
• 8:00 
• 9:00 
• 10:00 
• 11:00 
• 12:00 
 
Required if AM/PM, Time 
Zone or 
Rejected/Accepted is 
populated 
 
  
Transactions received 
on the effective date 
before: AM/PM 
  
transRecTim
eAmPm 
A/N OC  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• AM 
• PM 
 
Required if Hour, Time 
Zone or 
Rejected/Accepted is 
populated 
   
Transactions received 
on the effective date 
before: 
Time Zone 
  
transRecTim
eZone 
A/N OC  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Eastern Time 
• Central Time 
• Mountain Time 
• Pacific Time 
• Alaska Time 
• Hawaii Time 
 
Required if Hour, AM/PM 
or    Rejected/Accepted is 
populated 
 

---

## Page 181

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 181 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
  
Transactions received 
on the effective date 
before: 
Rejected/ Accepted 
  
transEffDate
AcceptedOr
Rejected 
A/N OC  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Rejected 
• Accepted 
 
This field is required if 
Hour, AM/PM or Time 
Zone is populated 
 
 
This field will be 
combined with the fields 
(Transactions received on 
the effective date before 
Hour, Time Zone, 
Rejected/Accepted) and 
placed in the 
TRANS_REC_TIME field on 
the Excel Template.  
Exactly as below: 
“Transactions received on 
the effective date before 
2:00 PM Eastern Time will 
be Rejected” 
 
If this field is not 
populated, then nothing 
will be added to the Excel 
template 
Rejected transactions 
must be resubmitted 
starting:   
Date 
 
  
rejTranReSu
bDate 
Date OC 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
 
Required if Hour, AM/PM 
or Time Zone is populated 
Rejected transactions 
must be resubmitted 
starting:   
Hour 
  
rejTranReSu
bHour 
A/N OC  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• 1:00 
• 2:00 
• 3:00 
• 4:00 
• 5:00 
• 6:00 
• 7:00 
• 8:00 
• 9:00 
• 10:00 
• 11:00 
• 12:00 
 
Required if  Date, Hour or 
Time Zone  is populated 
 
  

---

## Page 182

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 182 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Rejected transactions 
must be resubmitted 
starting:   
AM/PM 
  
rejTranReSu
bAmPm 
A/N OC  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• AM 
• PM 
 
Required if  Date, AM/PM, 
Time Zone  is populated 
 
  
Rejected transactions 
must be resubmitted 
starting:   
Time Zone 
  
rejTranReSu
bTimeZone 
A/N OC  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Eastern Time 
• Central Time 
• Mountain Time 
• Pacific Time 
• Alaska Time 
• Hawaii Time 
 
Required if Date, Hour, 
AM/PM  is populated 
 
  
NAV [[NSCC]] Mutual 
Fund Price/Rate file 
will be delivered on 
  
navDate1 Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
 
  
NAV [[NSCC]] Mutual 
Fund Price/Rate file 
will be delivered by 
  
navDecPlace
sTxt 
A/N O 100    
Record Type 
 
Retiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent  
recordType A/N R    Hardcoded  value: 
‘Retiring TA Networking 
Account 
Conversion/Update (F51) 
will be sent’ 
 
Retiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent 
(Yes/No) 
  
networkingY
esNo 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 
Retiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent 
(Date) 
  
networkingD
ate 
Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
 
  
Retiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent 
(Transaction Type) 
 
  
networkingT
ranType 
A/N O 20 On The UI this 
field will be 
defaulted to 
‘N/A’ and 
greyed out and 
cannot be 
changed. The 
Excel Template 
is already 
Should be 
populated to 
‘N/A’ 
 Defaulted to  ‘N/A’ 

---

## Page 183

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 183 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
populated with 
‘N/A’ in the field 
Retiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent 
(Initiating/Consuming 
TA) 
  
networkingS
ubmittingTA 
A/N O 100    
Record Type 
 
Acquiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent  
recordType A/N R    Hardcoded  value: 
‘Acquiring TA Networking 
Account 
Conversion/Update (F51) 
will be sent’ 
 
Acquiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent 
(Yes/No) 
  
networkingY
esNo 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 
Acquiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent 
(Date) 
  
networkingD
ate 
Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
 
  
Acquiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent 
(Transaction Type) 
  
networkingT
ranType 
A/N O 20 On The UI this 
field will be 
defaulted to 
‘N/A’ and 
greyed out and 
cannot be 
changed. The 
Excel Template 
is already 
populated with 
‘N/A’ in the field 
Should be 
populated to 
‘N/A’ 
 Defaulted to  ‘N/A’ 
Acquiring TA 
Networking Account 
Conversion/Update 
(F51) will be sent 
(Initiating/Consuming 
TA) 
  
networkingS
ubmittingTA 
A/N O 100    
Record Type 
‘Networking Activity 
File (F55)’ 
recordType A/N R    Hardcoded  value: 
‘Networking Activity File 
(F55)’ 
Networking Activity 
File (F55) (Yes/No) 
  
networkingY
esNo 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 
Networking Activity 
File (F55) (Date) 
networkingD
ate 
Date O 10 Calendar picker   MM/DD/CCYY  

---

## Page 184

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 184 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
  
This date can be 
backdated 
 
  
Networking Activity 
File (F55) (Transaction 
Type) 
 
  
networkingT
ranType 
A/N O 20        
Networking Activity 
File (F55) 
(Initiating/Consuming 
TA) 
  
networkingS
ubmittingTA 
A/N O 100    
Record Type 
 
Retiring TA 
Networking Position 
Reporting (F58) will be 
sent 
recordType A/N R    Hardcoded  value: 
‘Retiring TA Networking 
Position Reporting (F58) 
will be sent’ 
 
Retiring TA 
Networking Position 
Reporting (F58) will be 
sent (Yes/No) 
  
networkingY
esNo 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 
Retiring TA 
Networking Position 
Reporting (F58) will be 
sent (Date) 
  
networkingD
ate 
Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
 
  
Retiring TA 
Networking Position 
Reporting (F58) will be 
sent (Transaction 
Type) 
 
  
networkingT
ranType 
A/N O 20 On The UI this 
field will be 
defaulted to 
‘N/A’ and 
greyed out and 
cannot be 
changed. The 
Excel Template 
is already 
populated with 
‘N/A’ in the field 
Should be 
populated to 
‘N/A’ 
 Defaulted to  ‘N/A’ 
Retiring TA 
Networking Position 
Reporting (F58) will be 
sent 
(Initiating/Consuming 
TA) 
 
  
networkingS
ubmittingTA 
A/N O 100    
Record Type 
 
Acquiring TA 
Networking Position 
recordType A/N R    Hardcoded  value: 
‘Acquiring TA Networking 
Position Reporting (F58) 
will be sent’ 
 

---

## Page 185

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 185 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Reporting (F58) will be 
sent 
Acquiring TA 
Networking Position 
Reporting (F58) will be 
sent (Yes/No) 
  
networkingY
esNo 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 
Acquiring TA 
Networking Position 
Reporting (F58) will be 
sent (Date) 
  
networkingD
ate 
Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
 
  
Acquiring TA 
Networking Position 
Reporting (F58) will be 
sent (Transaction 
Type) 
  
networkingT
ranType 
A/N O 20 On The UI this 
field will be 
defaulted to 
‘N/A’ and 
greyed out and 
cannot be 
changed. The 
Excel Template 
is already 
populated with 
‘N/A’ in the field 
Should be 
populated to 
‘N/A’ 
 Defaulted to  ‘N/A’ 
Acquiring TA 
Networking Position 
Reporting (F58) will be 
sent 
(Initiating/Consuming 
TA) 
  
networkingS
ubmittingTA 
A/N O 100    
Record Type 
 
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be accepted 
recordType A/N R    Hardcoded  value: 
‘Networking Account 
Conversion/Update/Trans
fer (B50, B51 and B52) will 
be accepted’ 
 
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be accepted 
(Yes/No) 
  
networkingY
esNo 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be accepted 
(Date) 
  
networkingD
ate 
Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
 
  
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be accepted 
(Transaction Type)  
networkingT
ranType 
A/N O 20 On The UI this 
field will be 
defaulted to 
‘N/A’ and 
greyed out and 
cannot be 
Should be 
populated to 
‘N/A’ 
 Defaulted to  ‘N/A’ 

---

## Page 186

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 186 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
changed. The 
Excel Template 
is already 
populated with 
‘N/A’ in the field 
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be accepted 
(Initiating/Consuming 
TA) 
  
networkingS
ubmittingTA 
A/N O 100    
Record Type 
 
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be confirmed 
recordType A/N R    Hardcoded  value: 
‘Networking Account 
Conversion/Update/Trans
fer (B50, B51 and B52) will 
be confirmed’ 
 
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be confirmed 
(Yes/No) 
  
networkingY
esNo 
A/N O  Can select from 
drop down 
Can be 
populated with 
Values from 
Description  
• Yes 
• No 
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be confirmed 
(Date) 
 
  
networkingD
ate 
Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
 
  
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be confirmed 
Transaction Type) 
  
networkingT
ranType 
A/N O 20 On The UI this 
field will be 
defaulted to 
‘N/A’ and 
greyed out and 
cannot be 
changed. The 
Excel Template 
is already 
populated with 
‘N/A’ in the field 
Should be 
populated to 
‘N/A’ 
 Defaulted to  ‘N/A’ 
Networking Account 
Conversion/Update/Tr
ansfer (B50, B51 and 
B52) will be confirmed 
(Initiating/Consuming 
TA) 
  
networkingS
ubmittingTA 
A/N O 100    
Additional 
Considerations 
  
additionalCo
nsiderYesNo 
A/N O      • Yes 
• No 
 

---

## Page 187

MF INFO XCHANGE 
Create Notification Step 2 -  [[transfer agent]] Change/Fund Acquisition 187 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
Additional 
Considerations 
Description 
  
additionalCo
nsideration 
A/N O 1000 If “Additional 
Considerations” 
is “Yes”, then 
the Additional 
Considerations 
section is 
displayed on the 
UI 
Can be 
populated  
If “Additional 
Considerations” 
is “Yes” 
The limit on the number 
of rows is 5 
Comment 
  
transferAge
ncyCommen
t 
A/N O 4000    
 
  

---

## Page 188

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 188 
 
CREATE NOTIFICATION STEP 2 -  UNSCHEDULED MARKET 
CLOSE (UMC)   
 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Event Name eventNam
e 
A/N R 500   Provide/enter UMC event 
name 
All considerations 
described in this 
notification apply to 
  
notifApply A/N R  Can select from 
drop down 
 
If “Fund 
Complex Wide 
with the 
exception of the 
funds listed 
below”  
Is selected, then 
the Exception 
Funds table will 
be displayed on 
the UI 
Can be 
populated 
with Values 
from 
Description  
• Fund Complex Wide 
• Fund Complex Wide 
with the exception of 
the funds listed below  
 
  
Exception Funds Fund 
Number 
  
(Exception Funds 
table) 
eFundNu
mber 
A/N O 8   Allowed if “Fund Complex 
Wide with the exception 
of the funds listed below”  
Is selected 
Exception Funds 
Security Issue [[ID]] 
 
(Exception Funds 
table)  
eSecIssueI
d  
A/N O  9   If “Fund Complex Wide 
with the exception of the 
funds listed below”  
Is selected 
Exception Funds Fund 
Name 
  
(Exception Funds 
table) 
eFundNa
me  
A/N O 60   If “Fund Complex Wide 
with the exception of the 
funds listed below”  
Is selected 
Exception Funds 
Ticker 
  
(Exception Funds 
table) 
eFundTick
er 
A/N O 12   If “Fund Complex Wide 
with the exception of the 
funds listed below”  
Is selected 
Exception Funds Share 
Class 
 
(Exception Funds 
table)  
eFundSha
reClass 
A/N O 20   If “Fund Complex Wide 
with the exception of the 
funds listed below”  
Is selected 

---

## Page 189

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 189 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
N/A status 
 
(Exceptio
n Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Exceptio
n Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 

---

## Page 190

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 190 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Trading Through [[NSCC]] 
Fund/SERV - Non-
DCC&S Transactions 
with Trade Date=UMC 
Effective Date will be 
accepted 
  
nonDCCST
radeDate
UMC 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Trading Through [[NSCC]] 
Fund/SERV - Non-
DCC&S Transactions 
with Trade Date prior 
to UMC Effective Date 
will be accepted 
  
nonDCCST
radeDate
BeforeUM
C 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Trading Through [[NSCC]] 
Fund/SERV - DCC&S 
transactions with 
Trade Date=UMC 
Effective Date will be 
accepted 
  
dCCSTrad
eDateUM
C 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Trading Through [[NSCC]] 
Fund/SERV - DCC&S 
transactions with 
Trade Date prior to 
UMC Effective Date 
will be accepted 
  
dCCSTrad
eDateBefo
reUMC 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Trading Through [[NSCC]] 
Fund/SERV - 
[[settlement]] of all 
accepted Fund/SERV 
transactions 
scheduled to settle on 
UMC Effective Date 
will occur 
  
fundSettU
MC 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
[[default]] to ‘Yes’ 
Non-[[NSCC]] Trading - 
Transactions with 
Trade Date=UMC 
nonNSCCT
radeDate
UMC 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
• Yes 
• No 

---

## Page 191

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 191 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Effective Date will be 
accepted _  
from 
Description  
Non-[[NSCC]] Trading - 
Transactions with 
Trade Date prior to 
UMC Effective Date 
will be accepted 
 
  
nonNSCCT
radeDate
BeforeUM
C 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Non-[[NSCC]] Trading - 
[[settlement]] of all 
accepted transactions 
scheduled to settle on 
UMC Effective Date 
will occur 
 
  
nonNSCCS
ettUMC 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Non-[[NSCC]] Trading - 
Incoming wires will be 
accepted 
  
nonNSCCI
nWire 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Non-[[NSCC]] Trading - 
Outgoing wires will be 
sent 
  
nonNSCC
OutWire 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Trade Estimate cut-off 
time 
  
tradeEstC
utOffTime 
A/N O  25    
Networking 
Transactions - 
Transactions will be 
accepted 
  
networkin
gTransacti
ons 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Networking 
Transactions - Account 
Conversion - New 
Account (B50) – 
transactions received 
on UMC Effective Date 
will be acknowledged 
on 
  
netTransA
ccConvNe
wAcc 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be 
backdated 
Networking 
Transactions - Account 
Conversion - Update 
(B51) – transactions 
received on UMC 
Effective Date will be 
acknowledged on  
netTransA
ccConvUp
date 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be 
backdated 

---

## Page 192

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 192 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Networking 
Transactions - Account 
Transfer (B52) – 
transactions received 
on UMC Effective Date 
will be acknowledged 
on 
 
  
netTransA
ccTransAc
k 
Date O  Calendar picker  MM/DD/CCYY  
This date can be 
backdated 
Networking 
Transactions - Account 
Transfer (B52) – 
transactions received 
on UMC Effective Date 
will be processed with 
an Effective Date of  
netTransA
ccTransEff
Date 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be 
backdated 
Networking 
Transactions - Share 
Aging (F75) 
transactions will be 
sent on 
  
netTransS
hareAging 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be 
backdated 
Networking 
Transactions - Activity 
(F55) transactions will 
be sent on 
  
netTransA
ctivity 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be 
backdated 
Networking 
Transactions - Position 
Reporting files will be 
sent on 
  
netTranPo
sReportin
g 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be 
backdated 
Networking 
Transactions - SPAC 
files will be sent on 
  
netTransS
PAC 
Date O 10 Calendar picker  MM/DD/CCYY  
This date can be 
backdated 
ACATS Transactions - 
Transactions received 
on UMC Effective Date 
will be accepted 
  
acatsTran
sAccept 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
ACATS Transactions - 
Transactions received 
on UMC Effective Date 
will be processed on 
  
acatsTran
sProcess 
Date OC 10 Calendar picker 
 
This field will be 
greyed on the UI 
unless “Yes” is 
selected for 
field 
“Transactions 
received on 
UMC Effective 
  
 
 
MM/DD/CCYY  
This date can be 
backdated 
 
Not allowed unless “Yes” 
is selected for field 
“Transactions received on 
UMC Effective Date will 
be accepted” 

---

## Page 193

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 193 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Date will be 
accepted” 
ACATS Transactions - 
Acknowledgement will 
be transmitted on 
  
acatsAck Date OC 10 Calendar picker 
 
This field will be 
greyed on the UI 
unless “Yes” is 
selected for 
field 
“Transactions 
received on 
UMC Effective 
Date will be 
accepted” 
  
 
 
MM/DD/CCYY  
This date can be 
backdated 
 
Not allowed unless “Yes” 
is selected for field 
“Transactions received on 
UMC Effective Date will 
be accepted” 
ACATS Transactions – 
[[settlement]] 
  
acatsSett Date OC 10 Calendar picker 
 
This field will be 
greyed on the UI 
unless “Yes” is 
selected for 
field 
“Transactions 
received on 
UMC Effective 
Date will be 
accepted” 
  
 
 
MM/DD/CCYY  
This date can be 
backdated 
 
Not allowed unless “Yes” 
is selected for field 
“Transactions received on 
UMC Effective Date will 
be accepted” 
Cumulative rate will 
be provided on  
  
cumulativ
eRateProv
ided 
Date O 10 Calendar picker 
 
If Cumulative 
rate will be 
provided on 
Date  is 
provided, then 
the Cumulative 
Rate – Impacted 
Funds table will 
be displayed on 
the UI 
 
 
  
  
 
 
MM/DD/CCYY  
This date can be 
backdated 
 
  
Cumulative rate 
Accrual period start 
date 
  
cumulativ
eRateAccr
ualPeriod
Start 
Date O 10 Calendar picker 
 
If Cumulative 
rate will be 
provided on 
Date is 
provided, then 
this field will be 
available 
otherwise this 
This field is 
allowed only  
If Cumulative 
rate will be 
provided on 
Date  is 
provided 
 
 
MM/DD/CCYY  
This date can be 
backdated 
 
  

---

## Page 194

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 194 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
will be greyed 
out on the UI 
 
  
Cumulative Accrual 
period end date 
  
cumulativ
eRateAccr
ualPeriod
End 
Date O 10 Calendar picker 
 
If Cumulative 
rate will be 
provided on 
Date is 
provided, then 
this field will be 
available 
otherwise this 
will be greyed 
out on the UI 
 
  
This field is 
allowed only  
If Cumulative 
rate will be 
provided on 
Date  is 
provided 
  
 
 
MM/DD/CCYY  
This date can be 
backdated 
 
  
Cumulative Rate Fund 
Number 
 
(Cumulative Rate 
Impacted Funds table) 
  
cRFundNu
mber 
A/N O 8    
Cumulative Rate 
Security Issue [[ID]] 
 
(Cumulative Rate 
Impacted Funds table) 
 
  
cRSecIssu
eId 
A/N O  9    
Cumulative Rate Fund 
Name 
 
(Cumulative Rate 
Impacted Funds table) 
 
  
cRFundNa
me 
A/N O 60    
Cumulative Rate 
Ticker 
 
(Cumulative Rate 
Impacted Funds table) 
 
  
cRFundTic
ker 
A/N O 12    
Cumulative Rate Share 
Class 
 
(Cumulative Rate 
Impacted Funds table) 
 
  
cRFundSh
areClass 
A/N O 20    

---

## Page 195

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 195 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
N/A 
 
status 
 
(Cumulati
ve Rate 
Impacted 
Funds 
table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A 
 
rowId 
 
(Cumulati
ve Rate 
Impacted 
Funds 
table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 

---

## Page 196

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 196 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Single day rate will be 
provided on UMC date 
  
singleDay
Rate 
A/N O  Can select from 
drop down 
 
If “Yes” is 
selected, then 
the Single Day 
Rate – Impacted 
Funds table will 
be displayed on 
the UI 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No  
 
Single Day Rate Fund 
Number  
  
(Single Day Rate – 
Impacted Funds 
table) 
sDFundNu
mber 
A/N O 8  Can be 
populated 
only if Single 
day rate will 
be provided 
on UMC date 
field  
= ‘Yes’ 
 
 
Single Day Rate 
Security Issue [[ID]]  
  
(Single Day Rate – 
Impacted Funds 
table) 
sDSecIssu
eId 
A/N O  9  Can be 
populated 
only if Single 
day rate will 
be provided 
on UMC date 
field  
= ‘Yes’ 
 
Single Day Rate Fund 
Name 
  
(Single Day Rate – 
Impacted Funds 
table) 
sDFundNa
me 
A/N O 60  Can be 
populated 
only if Single 
day rate will 
be provided 
on UMC date 
field  
= ‘Yes’ 
 
Single Day Rate Ticker 
 
(Single Day Rate – 
Impacted Funds 
table)  
sDFundTic
ker 
A/N O 12  Can be 
populated 
only if Single 
day rate will 
be provided 
 

---

## Page 197

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 197 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
on UMC date 
field  
= ‘Yes’ 
 
Single Day Rate Share 
Class 
  
(Single Day Rate – 
Impacted Funds 
table) 
sDFundSh
areClass 
A/N O 20  Can be 
populated 
only if Single 
day rate will 
be provided 
on UMC date 
field  
= ‘Yes’ 
 
 N/A status 
 
 
(Single 
Day Rate 
– 
Impacted 
Funds 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Single 
Day Rate 
– 
Impacted 
Funds 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 

---

## Page 198

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 198 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Record Date Revised 
  
recordDat
eRevised 
A/N O  Can select from 
drop down 
 
If “Yes” is 
selected, then 
the 
Record/Ex/Paya
ble Dates – 
Impacted Funds 
table will be 
displayed on the 
UI 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
Ex Date Revised 
  
exDateRe
vised 
A/N O  Can select from 
drop down 
 
If “Yes” is 
selected, then 
the 
Record/Ex/Paya
ble Dates – 
Impacted Funds 
table will be 
displayed on the 
UI 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
 
   
Payable Date Revised 
  
payableDa
teRevised 
A/N O  Can select from 
drop down 
 
If “Yes” is 
selected, then 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 

---

## Page 199

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 199 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
the 
Record/Ex/Paya
ble Dates – 
Impacted Funds 
table will be 
displayed on the 
UI 
Record/Ex/Payable 
Dates Fund Number 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
  
rEPFundN
umber 
A/N O 8  Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
 
 
 Record/Ex/Payable 
Dates Security Issue 
[[ID]] 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
 
  
rEPSecIssu
eId 
A/N O  9  Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
 
 
Record/Ex/Payable 
Dates Fund Name 
 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
 
rEPFundN
ame 
A/N O 60  Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
 
 
Record/Ex/Payable 
Dates Ticker 
 
 
 
 
rEPFundTi
cker 
A/N O 12  Can be 
populated 
only if  
Record Date 
Revised 
or/and 
 

---

## Page 200

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 200 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
 
Record/Ex/Payable 
Dates Share Class 
 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
 
rEPFundS
hareClass 
A/N O 20  Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
 
 
Original Record Date 
 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
 
rEPOrigina
lReocrdDa
te 
Date O 10 Calendar picker Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
MM/DD/CCYY  
This date can be 
backdated 
Rescheduled Record 
Date 
 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
  
rEPResche
duledReco
rdDate 
Date O 10 Calendar picker Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
MM/DD/CCYY  
This date can be 
backdated 
Original Ex Date 
 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
  
rEPOrigina
lExDate 
Date O 10 Calendar picker Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
MM/DD/CCYY  
This date can be 
backdated 

---

## Page 201

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 201 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
Rescheduled Ex Date 
 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
 
rEPResche
duledExD
ate 
Date O 10 Calendar picker Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
MM/DD/CCYY  
This date can be 
backdated 
Original Payable Date 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
 
rEPOrigina
lPayableD
ate 
Date O 10 Calendar picker Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
MM/DD/CCYY  
This date can be 
backdated 
Rescheduled Payable 
Date 
 
 
(Record/Ex/Payable 
Dates – Impacted 
Funds table) 
 
rEPResche
duledPaya
bleDate 
Date O 10 Calendar picker Can be 
populated 
only if  
Record Date 
Revised 
or/and 
Ex Date 
Revised 
or/and  
Payable Date 
Revised 
= ‘Yes’ 
MM/DD/CCYY  
This date can be 
backdated 
N/A 
 
status 
 
(Record/E
x/Payable 
Dates – 
Impacted 
Funds 
table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 

---

## Page 202

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 202 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A 
 
rowId 
 
(Record/E
x/Payable 
Dates – 
Impacted 
Funds 
table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 

---

## Page 203

MF INFO XCHANGE 
Create Notification Step 2 -  Unscheduled Market Close (UMC) 203 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
NAV will be calculated 
  
navCalc A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Call Centers - Will be 
open 
 
ccOpen A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
• Yes 
• No 
Call Centers – From 
 
 
ccFrom A/N O 25 If Call Centers – 
Will be Open is 
“Yes”, then this 
field will be 
available 
otherwise this 
will be greyed 
out on the UI 
Can be 
populated 
only If Call 
Centers – Will 
be Open is 
“Yes” 
 
Call Centers – To 
 
ccTo A/N O 25 If Call Centers – 
Will be Open is 
“Yes”, then this 
field will be 
available 
otherwise this 
will be greyed 
out on the UI 
Can be 
populated 
only If Call 
Centers – Will 
be Open is 
“Yes” 
 
Comment  notificatio
nCommen
t 
A/N O 4000    
 
 
  

---

## Page 204

MF INFO XCHANGE 
Create Notification Step 2 -  Upcoming [[Proxy]] 204 
 
CREATE NOTIFICATION STEP 2 -  UPCOMING [[Proxy]] 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
[[Proxy]] Statement Link:   proxyLink A/N O 255    
[[Proxy]] Voting 
Timeframe:  
  
proxyVote
Date 
 A/N O 500    
Record Date: 
  
recordDat
e 
Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
Voting Date/Board 
meeting:   
  
voteDate Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
Adjournment Date: 
  
adjDate Date O 10 Calendar picker   MM/DD/CCYY  
This date can be 
backdated 
Outbound Solicitation 
Required: 
  
outSoliRe
q 
A/N O  Can select from 
drop down 
Can be 
populated 
with Values 
from 
Description  
•     Yes 
•     No 
Solicitation Firm Name 
  
soliFirmN
ame 
A/N O 60    
[[Proxy]] Website Link: 
  
proxyWeb
Link 
A/N O 255    
Fund Number 
 
(Impacted Funds 
table) 
  
fundNum
ber 
A/N O 8    
Security Issue [[ID]] 
  
(Impacted Funds 
table) 
secIssueId A/N O 9    
Fund Name 
 
(Impacted Funds 
table) 
fundNam
e 
A/N O 60    
Ticker 
  
(Impacted Funds 
table) 
fundTicke
r 
A/N O 12    
Share Class 
 
(Impacted Funds 
table)   
fundShare
Class 
A/N O 20    
N/A 
 
status 
 
A/N O/C 1 N/A Can be 
populated 
Values allowed: 
• ‘I’ - Insert new row 

---

## Page 205

MF INFO XCHANGE 
Create Notification Step 2 -  Upcoming [[Proxy]] 205 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Impacted 
Funds 
table) 
 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Impacted 
Funds 
table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 

---

## Page 206

MF INFO XCHANGE 
Create Notification Step 2 -  Upcoming [[Proxy]] 206 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
[[Proxy]] Information: 
  
proxyInfo A/N O 4000    
Comment  upcoming
ProxyCom
ment 
A/N O 4000    
 
 
 
 
 
 
  

---

## Page 207

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 207 
 
CREATE NOTIFICATION STEP 2 -  US HOLIDAY 
ANNOUNCEMENT 
 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Holiday holiday A/N R  Can select from 
drop down 
Can be 
populated 
with Values 
from the 
Description 
Column 
• New Year’s Day 
• Martin Luther King, 
Jr. Day 
• President’s Day 
• Good Friday 
• Memorial Day 
• Juneteenth 
• Independence Day 
• Labor Day 
• Columbus Day 
• Veteran’s Day 
• Thanksgiving Day 
• Christmas Day 
• Other 
Holiday Other 
Description 
holidayOt
herDesc 
A/N OC 50    Required if  
Holiday = “Other”,  
otherwise – not allowed  
[[NYSE]]  [[NYSE]] A/N R  Can select from 
drop down 
 
   
Can be 
populated 
with Values 
from 
Description    
• Open 
• Closed 
• Early Close 
Federal Reserve    
federalRe
serve 
A/N R  Can select from 
drop down 
 
   
Can be 
populated 
with Values 
from 
Description    
• Open 
• Closed 
Early Close Date 
  
earlyClose
Date 
Date O 10 calendar picker 
 
This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
MM/DD/CCYY  
This date can be 
backdated 
Early Close Time  
 
earlyClose
Time 
A/N O 8 This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
  

---

## Page 208

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 208 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
section should 
not be displayed 
Early Close Fund Type  
 
(Early Close 
Consideration table) 
 
fundType A/N O 20 This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
Can add up to 5 additional 
rows 
Early Close Trading 
Open 
 
 
(Early Close 
Consideration table) 
  
tradingOp
en 
A/N O  Can select from 
drop down 
 
This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
Can be 
populated 
with Values 
from 
Description  
 
 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
• Yes 
• No 
 
 
Can add up to 5 additional 
rows 
Early Close Wire 
[[settlement]] 
 
(Early Close 
Consideration table) 
  
wireSettle
ment 
A/N O  Can select from 
drop down 
 
 
This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
Can be 
populated 
with Values 
from 
Description  
 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
• Yes 
• No 
 
 
  
Early Close Trading 
Deadline    
 
(Early Close 
Consideration table) 
 
tradingDe
adline 
A/N O 20  This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
  
Early Close Call Center 
Open 
 
(Early Close 
Consideration table) 
 
callCenter
Open 
A/N O  Can select from 
drop down 
 
 
This field is only 
available if the 
[[NYSE]] is “Early 
Can be 
populated 
with Values 
from 
Description  
 
• Yes 
• No 
 
 
  

---

## Page 209

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 209 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
Early Close Call Center 
Hours 
 
 
(Early Close 
Consideration table) 
 
callCenter
Hours 
A/N O 20 This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
  
N/A 
 
status 
 
(Early 
Close 
Considera
tion table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A 
 
rowId 
 
(Early 
Close 
Considera
tion table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 

---

## Page 210

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 210 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Fund Number  
 
 
(Early Close Impacted 
Fund table) 
fundNum
ber 
A/N O 8 This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
  
Security Issue [[ID]] 
 
(Early Close Impacted 
Fund table) 
  
secIssueId A/N O 9 This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
  
Fund Name 
  
(Early Close Impacted 
Fund table) 
fundNam
e 
A/N O 60 This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
  
Ticker 
 
fundTicke
r 
A/N O 12 This field is only 
available if the 
This field is 
only available 
  

---

## Page 211

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 211 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
(Early Close Impacted 
Fund table) 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
Share Class 
 
(Early Close Impacted 
Fund table) 
fundShare
Class 
A/N O 20 This field is only 
available if the 
[[NYSE]] is “Early 
Close” 
otherwise the 
Early Close 
section should 
not be displayed 
This field is 
only available 
if the [[NYSE]] is 
“Early Close” 
otherwise this 
field is not 
allowed 
  
N/A status 
 
(Early 
Close 
Impacted 
Fund 
table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 
N/A rowId 
 
(Early 
Close 
Impacted 
Fund 
table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  

---

## Page 212

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 212 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Holiday 
Considerations Date 
 
(Holiday Consideration 
table) 
hcDate Date O 10 This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed  
MM/DD/CCYY  
This date can be 
backdated 
 
 
  
Holiday 
Considerations Fund 
Type 
 
(Holiday Consideration 
table) 
hcFundTy
pe 
A/N O 20 This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
  
Holiday 
Considerations 
Trading Open  
 
(Holiday Consideration 
table) 
hcTrading
Open 
A/N O  Can select from 
drop down 
 
 
This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Can be 
populated 
with Values 
from 
Description  
 
This field is 
only available 
if the Federal 
• Yes 
• No 
 
 
  

---

## Page 213

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 213 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Holiday 
Considerations 
section should 
not be displayed 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
Holiday 
Considerations Trade 
[[settlement]] T+0 
(Holiday Consideration 
table) 
  
hcTradeSe
ttlement0 
A/N O  Can select from 
drop down 
 
 
 
This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
Can be 
populated 
with Values 
from 
Description  
 
 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
• Yes 
• No 
 
 
  
Holiday 
Considerations Trade 
[[settlement]] T+1 
  
(Holiday Consideration 
table) 
hcTradeSe
ttlement1 
A/N R  This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
• Yes 
• No 
• N/A 
 
 
  
Holiday 
Considerations Wire 
[[settlement]] 
  
(Holiday Consideration 
table) 
hcWireSet
tlement 
A/N OC  Can select from 
drop down 
 
 
This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
Can be 
populated 
with Values 
from 
Description  
 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
• Yes 
• No 
 
 
  
Holiday 
Considerations 
Trading Deadline   
 
(Holiday Consideration 
table) 
hcTrading
Deadline 
A/N O 20 This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
  

---

## Page 214

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 214 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Holiday 
Considerations Call 
Center Open 
  
(Holiday Consideration 
table) 
hcCallCen
terOpen 
A/N O  Can select from 
drop down 
 
This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
Can be 
populated 
with Values 
from 
Description  
 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
• Yes 
• No 
 
  
Holiday 
Considerations Call 
Center Hours 
  
(Holiday Consideration 
table) 
hcCallCen
terHours 
A/N O 20 This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
  
N/A status 
 
(Holiday 
Considera
tion table) 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields.  
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 215

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 215 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
N/A rowId 
 
(Holiday 
Considera
tion table) 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Fund Number 
  
(Holiday Consideration 
Impacted Funds table) 
hcFundNu
mber 
A/N O 8 This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
  
Security Issue [[ID]] 
  
(Holiday Consideration 
Impacted Funds table) 
hcSecIssu
eId 
A/N O 9 This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
  

---

## Page 216

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 216 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Fund Name 
  
(Holiday Consideration 
Impacted Funds table) 
hcFundNa
me 
A/N O 60 This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
  
Ticker 
  
(Holiday Consideration 
Impacted Funds table) 
hcFundTic
ker 
A/N O 12 This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
  
Share Class 
 
(Holiday Consideration 
Impacted Funds table) 
  
hcFundSh
areClass 
A/N O 20 This field is only 
available if the 
Federal Reserve 
is “Closed” 
otherwise the 
Holiday 
Considerations 
section should 
not be displayed 
This field is 
only available 
if the Federal 
Reserve is 
“Closed” 
otherwise this 
field is not 
allowed 
  
N/A 
 
status 
 
(Holiday 
Considera
tion 
Impacted 
Funds 
table) 
 
A/N O/C 1 N/A Can be 
populated 
with values 
from the 
Description 
Column 
 
Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
Values allowed: 
• ‘I’ - Insert new row 
• ‘D’ - Delete existing row 
• ‘U’ – Update or Keep   
   existing row   
  
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
 
  
 

---

## Page 217

MF INFO XCHANGE 
Create Notification Step 2 -  US Holiday Announcement 217 
 
 
 
 
 
 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
correspondin
g “rowId” and 
“status” 
fields.  
N/A 
 
rowId 
 
(Holiday 
Considera
tion 
Impacted 
Funds 
table) 
 
Integer O/C 11 N/A Not allowed 
on the 
“Create a 
Notification” 
endpoint. 
 
Required on 
the “Update a 
Notification” 
endpoint if 
the respective 
table contains 
data. All 
existing rows 
within this 
table must be 
provided with 
the 
correspondin
g “rowId” and 
“status” 
fields. 
Required if 
status is one of the 
following: 
• ‘D’ - Delete existing row  
• ‘U’ – Update or Keep 
existing row  
 
Not allowed if  
status = ‘I’  - Insert new 
row 
 
If "rowId" is blank, 
"status" must be "I".  
If "rowId" is provided, 
"status" must be "D" or 
"U". 
“status”=”D” or “U” is not 
allowed when “rowId” is 
blank. 
“status”=”I” is not allowed 
when “rowId” is provided. 
 
“rowId” values must 
correspond to the values 
assigned by MF Info 
Xchange. “Receive 
Notification Data for an 
Event [[ID]]” endpoint must 
be called to return the 
current version of the 
notification with the 
rowIds assigned to each 
row of the table 
Comment  notificatio
nCommen
t 
A/N O 4000     
        

---

## Page 218

MF INFO XCHANGE 
Create Notification Step 4 (Submitter = Fund) 218 
 
 
CREATE NOTIFICATION STEP 4 (SUBMITTER = FUND) 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Distribution List distributio
nList 
A/N O 4000 Can select from drop 
down. 
The drop-down 
selection is made up of 
lists created by the 
Fund. If no Distribution 
List is created, then the 
Fund has nothing to 
select. 
  
The Fund can select 
“ALL Distribution Lists” 
to include all their 
distribution lists 
Can be populated 
with one or multiple 
Distribution List IDs   
 or ‘All Distribution 
Lists’. 
 
  
Firms 
 
portalFirm
s 
A/N R 4000 Can select from drop 
down 
 
The drop down list will 
include all Firms 
who have signed up for 
the system portal  
 
Can be populated 
with the following 
Values: 
    
• ‘0’  - All Firms 
• ’1’ -  Non-
Subscribing 
Firms(s) 
• [[participant]] 
Number(s)   
 
Only Firms who 
have signed up for 
the system can be 
populated  
 as [[participant]] 
Numbers 
• All Firms 
• Non-
Subscribing 
Firms(s) 
• [[participant]] 
Numbers 
(One or Multiple 
[[participant]] Numbers can 
be selected/provided)  
   
 
[[default]] is All Firms  
     
Designated 
Recipients 
receiverE
mailList 
AN OC 4000 Can  select  from drop 
down 
 
The drop-down 
[[participant]] list will 
include all Firms who 
have signed up for 
system portal , have 
designated recipients 
for the Notification and  
were  selected by 
submitting Fund  in 
‘Firms’   
 
Can be populated 
with the following 
values:  
  
• ‘-1’ - "Non 
Subscribing 
Firms" is selected 
in Access to 
Portal Firms  
 
• ‘0’ - Include 
emails provided   
by ALL recipients 
selected in 
•Include emails provided 
by All subscribing 
recipients ([[default]] value) 
•[[DO]] NOT include emails 
provided by recipients 
•Include emails provided 
ONLY by recipients 
selected in “Access to 
Portal View” 
• [[participant]] Numbers 
(One or Multiple 
[[participant]] Numbers can 
be selected/provided)  

---

## Page 219

MF INFO XCHANGE 
Create Notification Step 4 (Submitter = Fund) 219 
 
 
  
 
  
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
  
  
“Access to Portal 
View” 
 
• ‘1’ - [[DO]] NOT 
include emails 
provided by 
recipients 
 
• ’2’ Include 
emails 
provided ONLY 
by recipients 
selected in 
“Access to 
Portal View” 
 
• [[participant]](s) 
Number (if Fund 
[[DTCC]] [[participant]] 
Number in Step 
2 subscribes to 
MF INFO 
XCHANGE and 
has designated 
recipients for 
the Notification 
 
Only Firms who 
have signed up for 
the system  
and have 
designated 
recipients for the 
Notification can be 
provided. 
 
  
 
 
 
    
 Required if  
 value for Firms not =  
‘Non-Subscribing Firm(s)’ 

---

## Page 220

MF INFO XCHANGE 
Create Notification Step 4 (Submitter = Firm, Event Type = Large Trade Notification) 220 
 
CREATE NOTIFICATION STEP 4 (SUBMITTER = FIRM, EVENT 
TYPE = LARGE TRADE NOTIFICATION) 
 
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
Distribution 
List 
distributionList A/N O 4000 Can select from drop 
down. 
The drop-down 
selection is made up 
of lists created by the 
Firm. If no 
Distribution List is 
created, then the 
Firm has nothing to 
select. 
  
The Firm can select 
“ALL Distribution 
Lists” to include all of 
their distribution lists 
Can be populated with one or 
multiple Distribution List IDs   
 or ‘All Distribution Lists’. 
  
  
Fund Company 
 
portalFirms A/N   4000 Defaults to Fund 
[[DTCC]] [[participant]] 
Number provided in 
Step 2 if [[participant]] 
subscribes to MF 
INFO XCHANGE OR 
To ‘Non-Subscribing 
Fund’ if Fund [[DTCC]] 
[[participant]] Number 
provided in Step 2 
does not subscribe to 
MF INFO XCHANGE 
 
Data field is 
protected/not 
allowed on the UI. 
 
Defaults to Fund [[DTCC]]  
[[participant]] Number in Step 2 
if [[participant]] subscribes to MF 
INFO XCHANGE OR 
To ‘Non-Subscribing Fund’ if 
[[NSCC]] [[participant]] Number in 
Step 2 does not subscribe to 
MF INFO XCHANGE 
 
This field is not allowed on 
the “Create a Notification” 
and “Update a Notification” 
API endpoints. 
 
  
Fund Company 
receiving this Large 
Trade Notification 
Designated 
Recipients 
receiverEmailLi
st 
A/N OC  4000 Can  select  from 
drop down 
 
The drop-down  list 
will include the Fund 
[[DTCC]] [[participant]] in 
Step2  if Fund has 
designated recipients 
for the Notification.   
 
[[default]] 
Can be populated with the 
following Values: 
  
• ‘-1’ - "Non Subscribing 
Firms" is selected in 
Access to Portal Firms  
 
•  ‘1’ - [[DO]] NOT include 
emails provided by 
recipients 
 
• ’2’  - 
•[[DO]] NOT include 
emails provided by 
recipients 
•Include emails 
provided ONLY by 
recipients selected in 
“Access to Portal 
View” 
• [[participant]] 
Number (if Fund 
[[DTCC]] [[participant]] 
Number in Step 2 

---

## Page 221

MF INFO XCHANGE 
Create Notification Step 4 (Submitter = Firm, Event Type = Large Trade Notification) 221 
 
  
 
UI Field Name API Field 
Name 
Type O/C/R Length UI Definition API Definition  Description 
   / Values 
 
 
 
value for Fund not 
signed up for MF Info 
Xchange  =  ‘Non-
Subscribing Fund’ is 
null’  
 
[[default]] value for  
Fund   Number in 
Fund Company  is ‘ 
Include emails 
provided ONLY by 
recipients selected in 
“Access to Portal 
View” 
 
If the Fund Number 
selected in Step 2 
does not subscribe to 
MF Info Xchange, this 
field will be 
protected/not 
allowed in the UI. 
 
 
 
  
  
 - Include emails provided 
ONLY by recipients selected 
in “Access to Portal View” 
  
 
If the Fund Number selected 
in Step2 does not subscribe to 
MF Info Xchange, this field 
can be blank or “-1”. If this 
field is left blank on the API 
call, the system will [[default]] it 
to “-1” 
 
If the Fund Number selected 
in Step2 subscribes to MF Info 
Xchange, this field can be 
blank or “1” or “2”. If this 
field is left blank on the API 
call, the system will [[default]] to 
“2”. 
 
 
subscribes to MF 
INFO XCHANGE and 
has designated 
recipients for the 
Notification 
 

---

## Page 222

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of 
The Depository Trust & Clearing Corporation. 
 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal entity, 
subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
. 
 
 
Doc Date: January 8, 2024 
Publication Code: MFS342 
Service: MF Info Xchange 
Title: MF Info Xchange Data Dictionary 
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 