---
title: "MF Info Xchange API Capabilities - Technical Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfix_api_capabilities_technical_guide_mfs354_20240108.pdf"
pages: 34
size: "712.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MF Info Xchange API Capabilities - Technical Guide

**Original File:** [mfix_api_capabilities_technical_guide_mfs354_20240108.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfix_api_capabilities_technical_guide_mfs354_20240108.pdf)  
**Category:** Other  
**Total Pages:** 34  
**File Size:** 712.8 KB  

---

## Page 1

 
 
  
 
 
MF Info Xchange 
MF INFO XCHANGE API CAPABILITIES – 
TECHNICAL GUIDE 
JANUARY 8, 2024 
 
 
 

---

## Page 2

MF Info Xchange API Capabilities – Technical Guide 
Overview 2 
 
REVISION HISTORY 
Date Revision 
December 18, 2023 Updated the following section to reference API enhancements listed in Important Notice 
a9349 (dated November 15, 2023): 
“Create and Distribute a Notification” section under “Create a Notification”. Added a 
note regarding “notificationStatus” field on the “Create a Notification” endpoint. 
September 8, 2023 Document rebranded and reviewed.  
July 3, 2023 Updated sections: 
• “Glossary” – added “recipientClientNb”, “recipientName”, “dateSubmitted”, “submittedBy” 
fields 
• “Notification Receiver Functionality – API calls”  → “Receive Notifications” → “Invoke one 
of the following endpoints to get a list of received notifications” – added references to 
“clientNb”, “companyName”, “receivedDate”, “recipeintClientNb” and “recipientName” 
fields to the “Notes sub-section. 
• “Notification Receiver Functionality – API calls”  → “Receive Notifications” → “Receive 
notification details” – added references to “receivedDate”, “accountName” and “clientNb” 
fields to the “Notes subs-section. Removed references to the “distributionStatus” field. 
March 10, 2023 Updated a “Notifications with repeatable sections” section under the “Update a Notification” 
section 
December 14, 2022 Updated the following sections to reference API enhancements listed in Important Notice 
a9226 (dated November 11, 2022): 
• “Create and Distribute a Notification” section under “Create a Notification”. 
Added references to the Row [[ID]] parameter. 
• “Update a Notification” section – added a “Notifications with repeatable sections” 
section. 
• “Receive Notifications” section – added references to Distribution [[ID]], Row [[ID]] and Status 
parameters. 
March 23, 2022 Updated sections: 
• “Create and Distribute a Notification” section under “Notification Submitter Functionality – 
API Calls”. Updated create/distribute flow and finalization step requirements. 
• “Update a Notification” section under “Notification Submitter Functionality – API Calls”. 
Updated finalization step requirements. 
• “Endpoint Parameters – additional considerations” section. Added “Fields with multiple 
values” sub-section. 
February 17, 2022 Updated sections: 
▪ “Update a Notification” section under “Notification Submitter Functionality – API Calls”. 
Added a best practice for the “Update a Notification” endpoint. 
▪ “Receive a Notification” section under “Notification Receiver Functionality – API Calls”. 
Added best practice for the Distribution [[ID]] parameter.  
November 17, 2021 Initial publication (Important notice a9071, dated November 11, 2021) 

---

## Page 3

MF Info Xchange API Capabilities – Technical Guide 
Overview 3 
TABLE OF CONTENTS 
1. Overview ........................................................................................................................................................... 4 
2. Glossary ............................................................................................................................................................ 7 
3. Notification Submitter Functionality – API calls ........................................................................................... 9 
1. Create/Update/Delete Distribution Lists ............................................................................................... 9 
2. Retrieve All Active Distribution Lists ..................................................................................................10 
3. Create and Distribute a Notification ...................................................................................................11 
4. Delete a Notification ...........................................................................................................................14 
5. Update a Notification ..........................................................................................................................14 
6. Receive My Created Notifications ......................................................................................................16 
7. Receive A List of Organizations Subscribing to MF Info Xchange ....................................................17 
8. Receive A List of Clients and Their Email Designations ....................................................................17 
9. Receive MF Profile Security data .......................................................................................................17 
10. Create and Distribute a Notification - Flow Diagram ..........................................................................18 
11. Receive my Consolidated [[Dividend]]/Capital Gain or Interval/Tender Fund Schedule  .......................20 
4. Notification Receiver Functionality – API calls ........................................................................................... 21 
1. Receive Notifications ..........................................................................................................................21 
2. Receive Consolidated [[Dividend]]/Capital Gain or Interval/Tender Fund Schedule  .............................25 
5. Endpoint Parameters – additional considerations ..................................................................................... 27 
6. Frequently Asked Questions ........................................................................................................................ 31 
7. Data Dictionary ............................................................................................................................................... 33 
 

---

## Page 4

MF Info Xchange API Capabilities – Technical Guide 
Overview 4 
1. OVERVIEW 
MF Info Xchange facilitates and centralizes the delivery and receipt of time-critical notifications, including 
corporate actions, service disruptions and other critical alerts, which typically require communications between 
funds and intermediaries. The service facilitates two-way real time communication. 
Applying technology to notifications eliminates the manual email, phone call and fax process. MF Info Xchange 
effectively standardizes, streamlines, and reduces risk throughout the communication process. The service 
also includes an event calendar for receivers to view date-critical events, upcoming informational events and 
historical details. 
MF Info Xchange features an intuitive and dynamic web interface and provides real-time notifications with a 
complete audit trail. Access to event data is readily available, on-demand, through the user interface (UI) as 
well as the API enabled platform. 
 
MF INFO 
XCHANGE
Notification data
FUNDS
Create and 
distribute 
notifications via UI 
and/or API calls
Receive 
notifications via 
Email. Notification 
data is available via 
UI and API calls
FIRMS
Create and 
distribute 
notifications via UI 
and/or API calls
Receive 
notifications via 
Email. Notification 
data is available via 
UI and API calls
RECEIVERS NOT 
SUBSCRIBING TO MF INFO 
XCHANGE
Receive notifications via Email
 
 
This document provides a high-level overview of the MF Info Xchange API usage scenarios, endpoints, and 
flow diagrams. This document must be reviewed in conjunction with the following:  
• MF Info Xchange API specs (available in the [[DTCC]] API Marketplace1) 
• MF Info Xchange User Guide (available on the [[DTCC]] Learning site)  
 
1 Please contact your Relationship Manager to request access to the [[DTCC]] API Marketplace.  

---

## Page 5

MF Info Xchange API Capabilities – Technical Guide 
Overview 5 
“Notification Submitter Functionality – API calls” and “Notification Receiver Functionality – API calls” sections of 
this document contain various scenarios and associated API endpoints. Scenarios that require multiple API 
calls will list all required endpoints and the order of the calls.  
For a complete list of endpoint parameters and expected results/data elements, please refer to the MF Info 
Xchange API specs (available in the [[DTCC]] API Marketplace). Certain API models described in the MF Info 
Xchange API specs are utilized by both “create” (POST/PUT) and “receive” (GET) endpoints, therefore a 
model in the Marketplace might list a parameter that is required/optional on the “receive” endpoint but is not 
allowed on the “create” endpoint. This document calls out these special cases and provides additional 
information regarding these parameters. 
For information on field formats please refer to the “Data Dictionary” section of this document. 
In the event the submitting organization has opted to use the notification workflow approval process, their API 
calls to create/update/delete/distribute notifications will bypass this process resulting in a distributed 
notification. 
In order to utilize API functionality, clients must subscribe to MF Info Xchange as well as MF Info Xchange 
APIs. Service providers can create/receive data on behalf of their clients who are subscribing to MF Info 
Xchange and MF Info Xchange APIs and have authorized their service provider to act on their behalf. In 
addition, your organization needs a robot [[ID]] provisioned by your Access Coordinator with one of the following 
roles: 
• Create and Modify Data Request – API ONLY. This robot persona user has access to create, update, and 
delete data via APIs 
• Pull Data Request – API ONLY. This robot persona user has access to pull data via APIs. 
 
MF Info Xchange API endpoints are grouped by functionality in the [[DTCC]] API Marketplace. Each section 
contains a listing of endpoints with the corresponding list of input and output parameters.  
• Submit Notifications (Create, Update, Delete, Distribute)  
o Endpoints: Create a Notification, Distribute a Notification, Redistribute to All, Redistribute to New, 
Update a Notification, Delete a Notification, Receive Profile Security Data 
• Query Notifications (Submitter View) 
o Search and receive notifications created by the Submitter’s organization  
o Endpoints: Search Notifications by Ocode, Search Notifications by Security Issue IDs, Search 
Notifications by [[participant]] Number, Receive Notification Details 
• Query Consolidated Schedules (Submitter View) 
o Search and receive consolidated schedules created by the Submitter’s organization  
o Endpoints: Receive Consolidated Schedules by Ocode, Receive Consolidated Schedules by Security 
Issue IDs, Receive Consolidated Schedules by [[participant]] Number 
• Query Notifications (Receiver View) 
o Search and receive notifications received by the Receiver’s organization  
o Endpoints: Search Notifications by Ocode, Search Notifications by Security Issue IDs, Search 
Notifications by [[participant]] Number, Receive Notification Details 
• Query Consolidated Schedules (Receiver View) 
o Search and receive consolidated schedules received by the Receiver’s organization 
o Endpoints: Receive Consolidated Schedules by Ocode, Receive Consolidated Schedules by Security 
Issue IDs, Receive Consolidated Schedules by [[participant]] Number 
• Query Finalization Step Data Necessary for Notification Distribution 
o Receive data required on the finalization step (distribution) of the notification  

---

## Page 6

MF Info Xchange API Capabilities – Technical Guide 
Overview 6 
o Endpoints: Receive a list of the submitter’s active distribution lists, Receive a list of clients 
subscribing to MF Info Xchange, Receive notification receivers’ emails designations 
• Distribution List Actions (Create, Update, Delete) 
o Endpoints: Create a distribution list, Add a contact to a distribution list, Delete a contact from a 
distribution list, Update contact details, Receive distribution list details, Receive Contact  Details, 
Delete distribution list – validate if it is being used, Delete distribution list without validation 
 
Notes: 
• When invoking API endpoints, all parameter names within the endpoint URL (e.g.  
/client/{clientId}/notifications/) must be provided in lowercase format. Parameter values must be provided 
in the format specified within the endpoint model (refer to the MF Info Xchange API specs), this includes 
uppercase vs. lowercase, spaces, etc. Input parameter names must be provided in camel case (e.g., 
notificationReceivedDateStart). 
• Each invoked endpoint will return “message” and “status” fields.  
o “status” field provides a response code. For example, code 200 indicates a successful execution of 
the call. For a complete list of all response codes, please refer to the MF Info Xchange API specs 
(available in the [[DTCC]] API Marketplace). 
o “message” field provides a message corresponding to the response code (for example “Success”)  
 
 

---

## Page 7

MF Info Xchange API Capabilities – Technical Guide 
Glossary 7 
2. GLOSSARY 
Business 
Term 
API Term Definition 
Notification 
Submitter 
submitted The party that creates and distributes a notification through MF Info 
Xchange. Fund and firm clients have access to both notification 
submitter as well as notification receiver functionality. For example, 
fund [[Companies]] can submit Fund Merger notifications (notification 
submitter functionality) and receive Large Trade Notifications 
(notification receiver functionality). 
Notification 
Receiver 
received Receiver of a notification generated and distributed through MF Info 
Xchange.  
Fund and firm clients have access to both notification submitter as well 
as notification receiver functionality. For example, firm [[Companies]] can 
receive Fund Merger notifications (notification receiver functionality) 
and submit Large Trade Notifications (notification submitter 
functionality).  
Event [[ID]]  eventId Unique number generated and assigned to the notification by the MF 
Info Xchange system 
Event Type eventType Notification type (e.g., Fund Merger, Fund Rename, etc.) 
Event Status eventStatus 
notificationStatus 
Status of a Notification (e.g., Initial Notification, Update, Reminder, etc.)  
Event Effective 
Date  
effectiveDate  Effective date of the event.   
Event Effective 
Time 
effectiveTime When the event becomes effective, at the open of market or close of 
market  
Distribution 
Status  
distributionStatus Indicates whether event is in Draft, Pending Distribution, Revised-
Pending Distribution or Distributed status.   
Distribution List 
Name 
listName Name of the distribution list (created by the client at the time of 
distribution list creation) 
Distribution List 
[[ID]] 
listId Unique number generated and assigned to the distribution list by the 
MF Info Xchange system 
Client [[ID]] clientID 
clientNb 
recipientClientNb 
Eight-character [[DTCC]] [[participant]] Number that uniquely identifies a 
Client 
Company [[ID]] companyId [[ID]] ([[participant]] Number) associated with a Company 
Distribution 
Date 
distributionDate Date the event was last distributed 
Distribution [[ID]] distId (submitter side) 
distributionId (receiver side) 
Unique number generated and assigned to each successful distribution 
of a notification by the MF Info Xchange system. 

---

## Page 8

MF Info Xchange API Capabilities – Technical Guide 
Glossary 8 
Business 
Term 
API Term Definition 
Distribution 
Start Date 
distributionDateStart First Distribution Date when searching for notifications (“from” date) 
Distribution End 
Date 
distributionDateEnd Last Distribution Date when searching for notifications (“to” date) 
Effective Start 
Date 
effectiveDateStart First Effective Date when searching for notifications (“from” date) 
Effective End 
Date 
effectiveDateEnd Last Effective Date when searching for notifications (“to” date) 
Firm Company 
[[ID]] 
companyId [[ID]] ([[participant]] Number) associated with a Firm 
Fund Company 
[[ID]] 
companyId [[ID]] ([[participant]] Number) associated with a Fund 
Notification 
Received Start 
Date 
notificationReceivedDateStart First Receive Date when searching for notifications (“from” date) 
Notification 
Received End 
Date  
notificationReceivedDateEnd Last Receive Date when searching for notifications (“to” date) 
Notification 
Received Date 
receivedDate Date when notification was last received by the receiver 
Pagination totalNumberOfRecords 
pageNumber  
totalPages  
pageSize 
Page representation of the response 
Security Issue 
[[ID]] 
securityIssueIdArray 
securityIssueId 
List of Security Issue IDs when searching for notifications 
Company / 
Organization 
Name 
companyName 
accountName 
recipientName 
Name of the organization associated with the [[participant]] Number 
Repeatable 
section 
Repeatable section Notification table/array where clients can add/update/delete one or 
more rows within this section/table (for example “Impacted Funds” 
table) 
Row [[ID]] rowId Unique number generated and assigned by the MF Info Xchange 
system to each row within a repeatable section of the notification 
Submitted Date 
and Submitted 
By 
dateSubmitted 
submittedBy 
Notification submitter user name and notification submission date 
(creation, update, etc.) 
 

---

## Page 9

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 9 
3. NOTIFICATION SUBMITTER FUNCTIONALITY – API 
CALLS 
This section provides API endpoint information for notification submitters. 
1. Create/Update/Delete Distribution Lists 
o Create Distribution List 
POST  /client/{clientId}/distribution-list/ 
This endpoint allows clients to create a new distribution list with up to 1,000 contacts. The response 
will return a system generated Distribution List [[ID]] (listId) and a message indicating that the 
Distribution list was saved successfully. 
 
o Update Distribution Lists 
Clients can utilize the following endpoints to update an existing distribution list.  
» Add a contact 
POST  /client/{clientId}/distribution-list/{listId}/contact/  
This endpoint allows clients to add a contact to an existing distribution list. A separate call must 
be made for each new contact.  
» Delete a contact 
DELETE /client/{clientId}/distribution-list/{listId}/contact/{contactId}  
This endpoint allows clients to delete a contact from an existing distribution list. A separate call 
must be made for each contact that needs to be deleted from the list. 
This endpoint requires a Contact [[ID]] for the contact that is being deleted. To retrieve a contact [[ID]], 
clients must invoke the “Receive Distribution List Details” endpoint. 
» Update a contact 
PUT  /client/{clientId}/distribution-list/{listId}/contact/{contactId}   
This endpoint allows clients to update a contact on an existing distribution list. A separate call 
must be made for each contact that needs to be revised. 
This endpoint requires a Contact [[ID]] for the contact that is being updated. To retrieve a contact 
[[ID]], clients must invoke the “Receive Distribution List Details” endpoint. 
» Receive Details for one contact 
GET  /client/{clientId}/distribution-list/{listId}/contact/{contactId}  
This endpoint allows clients to receive contact information (email, first name, last name, etc.) for 
a specific Contact [[ID]] on a given Distribution List. 
 
o Delete Distribution Lists  
Clients can utilize the following endpoints to delete an existing active distribution list. 
» Delete Distribution List with validation  
Validate if the Distribution List [[ID]] is being used by one or more Event IDs (with an Event Status 
other than “Closed” or “Cancelled”). 

---

## Page 10

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 10 
DELETE  /client/{clientId}/distribution-list/{listId} 
If the Distribution List [[ID]] is being used by notification(s)/Event [[ID]](s) with an Event Status other 
than “Closed” or “Cancelled”, the list will NOT be deleted, and the call will result in a warning 
message with a list of all Event IDs that utilize this Distribution List [[ID]]. 
If the Distribution List [[ID]] is NOT being used by notification(s)/Event [[ID]](s) with an Event Status 
other than “Closed” or “Cancelled”, the list will be deleted. 
» Delete Distribution List without validation 
[[DO]] NOT validate if the Distribution List [[ID]] is being used by one or more Event IDs (with Event 
Status other than “Closed” or “Cancelled”). 
The system will not validate whether this list is being used by any notifications and will delete the 
list and remove it from all notifications where this list was explicitly selected. 
DELETE  /client/{clientId}/distribution-list/{listId}/override-delete 
Once the list is deleted it will be removed from all Event IDs that currently have this list explicitly selected. I f a 
new list is created with the same list name, the system will assign a NEW Distribution List [[ID]] to this newly 
created list. Future distributions of any existing Event IDs that previously contained this list name (prior to list 
deletion) will need to be updated with the new Distribution List [[ID]] if this list must be used when subsequently 
distributing those notifications.  
 
2. Retrieve All Active Distribution Lists 
1. Receive a list of all active distribution lists 
GET  /client/{clientId}/distribution-list 
This endpoint allows clients to request and receive a list of their organization’s active Distribution Lists 
(available within MF Info Xchange).  
To receive the contents of any of the active distribution lists, clients must invoke the Receive 
Distribution List Details endpoint. 
2. Receive Distribution List Details 
GET  /client/{clientId}/distribution-list/{listId} 
This endpoint allows clients to retrieve all contacts for a given active distribution list. A separate call 
must be made for each distribution list that is of interest. 
 

---

## Page 11

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 11 
The following diagram depicts all Distribution List activity (with the corresponding endpoints) that is available 
via API calls. 
Create Distribution List 
(endpoint: Create 
Distribution List)
Update Distribution List 
(endpoints: Add a Contact, 
Delete a Contact, Update 
a Contact)
Receive Distribution List 
Contacts 
(endpoints: Receive a list 
of all active distribution 
lists, Receive Distribution 
List Details)
Distribution List is saved in 
the MF Info Xchange 
database
Delete Distribution List 
(endpoints: Delete 
Distribution List with 
validation, Delete 
Distribution List without 
validation)
Receive Details for One 
Contact
(endpoints: Receive 
Details for one contact)
 
 
3. Create and Distribute a Notification 
To create a notification, you must invoke the following endpoints in the order outlined below. 
a) Create a Notification  
POST  /client/{clientId}/notifications/ 
This endpoint allows clients to create a new event notification. The “201” success response will return 
a system generated Event [[ID]] (eventId) and Distribution Status (distributionStatus)  and the newly 
saved notification object (all data elements and values for this notification provided by the client). The 
returned notification object will also contain Row IDs (“rowId” fields) assigned by the system to each 
row of the repeatable section. These Row IDs apply to API users only (will not be displayed in the 
Notification audit trail within the UI). 
To distribute the notification, clients must call the “Distribute Notification” endpoint. Alternatively, 
clients can login to the MF Info Xchange and distribute the notification through the UI.  
Notes:  
• “Create a Notification”, “Update a Notification” and “Receive Notification Details” (both submitter and 
receiver) endpoints utilize the same API model. The following fields will be returned when requesting 
notification details (“Receive Notification Details” endpoint). These fields are not allowed on the “Create a 
Notification” and “Update a Notification” endpoints: 
o accountName 
o eventID  
o clientNb 
o submittedBy 
o dateSubmitted 

---

## Page 12

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 12 
• The “notificationStatus” field on the “Create a Notification” endpoint must be populated with “Initial 
Notification”. 
• “Initial Step” fields utilize the same model for all Event Types; however, the following exceptions apply: 
o contactCompany – this field is required for Large Trade Notifications, it is not allowed for 
other Event Types 
o effectiveDate and effectiveTime fields are not allowed for [[Dividend]]/Capital Gain Schedule, 
Interval/Tender Fund Transaction Schedule and Price/Rate Error notifications. These 
fields are required for all other event types. 
• “Finalization Step” fields utilize the same model for all Event Types; however, the following exceptions 
apply: 
o portalFirms – this field is not allowed for Large Trade Notifications; it is required for all 
other Event Types. For Large Trade Notifications, the system will [[default]] this field to the 
fund provided in Step 2/body of the notification ([[NSCC]] [[participant]] number if the fund is 
subscribing to MF Info Xchange or “1” - for the non-subscribing fund).  
• The following Large Trade Notification fields are read only parameters on the UI and are not allowed on the 
“Create a Notification” endpoint: 
o largeTradeDollarThreshold 
o antiTradeDate (will be defaulted by the system to the Effective Date “effectiveDate”) 
• “status” and “rowId” fields (listed in the Marketplace models within tables/arrays) are not allowed on this 
endpoint.  
 
Finalization Step fields are not required on this endpoint. If not provided, the system will apply and save 
the following defaults in the database: 
• Fund originated notifications 
o portalFirms field (Firms) – “0” (All Firms) 
o receiverEmailList field (Emails Designated by Recipients) – “0” (Include emails provided by 
ALL subscribing recipients) 
• Large Trade Notifications – receiving fund DOES NOT subscribe to MF Info Xchange 
o portalFirms field (Firms) – “1” (Non-subscribing Funds) 
o receiverEmailList field (Emails Designated by Recipients)  – “-1” (Email designations were 
not found for the selection made within the “Access to Portal View” fields) 
• Large Trade Notifications – receiving fund DOES subscribe to MF Info Xchange 
o portalFirms field (Firms) – “nnnn” ([[NSCC]] [[participant]] Number of the fund selected in Step 
2) 
o receiverEmailList field (Emails Designated by Recipients) – “2” (Include emails provided 
‘ONLY’ by recipients selected in “Access to Portal View”) 
 
Notifications saved with Distribution Status=Pending Distribution or Revised Pending Distribution can be 
distributed. For the notification to be eligible for distribution, “Finalization Step” (step 4) data must be 
present (saved) when this notification was created and/or updated. 

---

## Page 13

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 13 
Notes:  
• Finalization step data elements are optional on this endpoint. If it is not provided, Distribution Status will be 
set to Draft. To distribute a draft notification, finalization step data must be provided by invoking an “Update 
a Notification” endpoint.  
• If you are not utilizing a distribution list and instead providing a list of email addresses in the “Emails” field, 
please note the maximum size of this field (refer to the Data Dictionary). If the list of email addresses you 
are planning to provide within the “Emails” field exceeds the maximum size of this field, your call will be 
rejected. Clients are advised to create and use distribution list(s) instead of providing multiple email 
addresses in the “Emails” field. 
• For Large Trade Notifications the “portalFirms” field is not allowed and must be blank. The system will utilize 
the value provided in the “fundPartNumber” field (impacted fund [[participant]] number) of the notification. In 
the event the notification is being distributed to a fund that does not subscribe to MF Info Xchange, the 
system will [[default]] this field to “1” (“Non-Subscribing Fund(s)”.)  
• It is recommended that you make a “Receive Notification Details” call to validate the details of the 
notification as well as the “finalization step” (distribution instructions) prior to invoking the distribution 
endpoint(s).  
o In the event any of the notification details need to be revised prior to the distribution, you must 
utilize the “Update a Notification” endpoint to make the necessary revisions to the notification. 
o In the event a distribution list that was previously provided within the finalization step of the 
notification has been deleted, the associated Distribution List [[ID]] will no longer be listed on this 
event. Therefore, if a new Distribution List [[ID]] is required, it will need to be provided prior to 
distributing or redistributing the notification (must utilize the “Update a Notification” endpoint to add 
a new Distribution List [[ID]]). 
• It is recommended that you also make a “Receive Distribution List Details” call to validate the details of any 
distribution lists that will be used to distribute the notification. In the event any of these distribution lists 
require revisions, you must update the list prior to distributing the notification.  Please refer to the 
“Create/Update/Delete Distribution List” section. 
 
b) Distribute a Notification  
POST  /client/{clientId}/notifications/{eventId}/distribute 
This endpoint allows clients to distribute a notification with the Distribution Status = Pending 
Distribution or Revised Pending Distribution. 
This endpoint requires an Event [[ID]]. 
c) Redistribute a Notification 
Clients can utilize one of the following endpoints to Redistribute their previously distributed 
notifications. 
Notes:  
• It is recommended that you make a “Receive Notification Details” call to validate the details of the 
“finalization step” (distribution instructions). In the event a distribution list that was previously provided within 
the finalization step of the notification has been deleted, the associated Distribution List [[ID]] will no longer be 
listed on this event. Therefore, if a new Distribution List [[ID]] is required, it will need to be provided (via 
“Update a Notification” endpoint) prior to redistributing the notification. 
• It is recommended that you also make a “Receive Distribution List Details” call to validate the details of any 
distribution lists that will be used to redistribute the notification. In the event any of these distribution lists 
require revisions, you must update the list prior to redistributing the notification. Please refer to the 
“Create/Update/Delete Distribution List” section. 
 
Redistribute the notification to all specified recipients 
POST  /client/{clientId}/notifications/{eventId}/redistribute/all 
» Clients can redistribute a previously distributed notification to all recipients. For example, when 
sending multiple reminders of an upcoming event. 

---

## Page 14

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 14 
» The Distribution Status of the notification must be “Distributed”. 
» This endpoint requires an Event [[ID]]. 
 
Redistribute the notification to newly added recipients 
POST  /client/{clientId}/notifications/{eventId}/redistribute/new 
» Clients can redistribute a previously distributed notification to the recipients added since the last 
distribution of this notification. For example, if additional organizations or distribution lists have  
been added to the notification, or additional contacts have been added to the distribution list(s) 
since the last distribution. 
» The Distribution Status of the notification must be “Distributed”. 
» This endpoint requires an Event [[ID]]. 
 
4. Delete a Notification 
DELETE  /client/{clientId}/notifications/{eventId}/delete 
Notifications with Distribution Status=Draft or Pending Distribution can be deleted from the system by invoking 
this endpoint. 
 
5. Update a Notification 
PUT  /client/{clientId}/notifications/{eventId}/update 
This endpoint allows clients to update an existing notification. Clients can update notifications with Distribution 
Status=Draft, Pending Distribution, Revised-Pending Distribution, Distributed.  
Updating a notification with Distribution Status=Distributed will change the status to Revis ed-Pending 
Distribution. 
Notes:  
• The notification data provided within this endpoint will replace the existing version of the notification in the 
system, therefore it is important to ensure that all previously provided data elements are provided on the 
“Update a Notification” endpoint, otherwise these data elements will be replaced with blank values upon 
successful processing of the update endpoint. 
• Finalization step data must be also provided on this endpoint. 
 
Notifications with “repeatable” sections 
When updating “repeatable” sections within a notification, clients are required to provide the “status” and 
“rowId” fields for each record being updated, deleted or retained within a “repeatable” section. 
o To update data within the row, clients must provide a "status" of "U"  and the “rowId”  that was assigned to 
this row by the system . Row Ids must be obtained/saved from the “201” response received  during Create 
Notification (if the data returned by the “Create Notification” endpoint was saved in the client’s system) or 
from calling the “Receive Notification” endpoint: GET /client/{clientId}/submitted/notifications/{eventId}.  
o To delete a row, provide a "status" of "D" and the “rowId” 
o If an existing row is not being updated or deleted, it must be provided with a “status” of “U” and the “rowId”. 

---

## Page 15

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 15 
Each existing rowId must be provided with a “U” or a “D” status. 
o To add a new row, clients must provide a "status" of "I" to each record being added (“rowId” must be blank , 
it will be assigned by the system when the API call is processed by the system. ) 
Please note, in certain instances, notifications created via UI might have an empty row in the “repeatable section” 
if that section was not populated  at the time of notification creation . When making an update/PUT call for the 
notifications with an empty row in the “repeatable section”, clients must provide this row with the associated row 
[[ID]] and a status (“U” to retain this empty row or “D” to delete it). 
The “200” response on a successful update/PUT will include the newly updated notification object containing the 
new rowIds for all new records added (as well as the existing row ids). 
For a complete list of notifications’ “repeatable” sections with the associated “status” and “rowId” fields, please 
refer to the Data Dictionary. 
 
To distribute a revised notification, clients must call the “Distribute Notification” endpoint.  
If the only revision to the notification impacted the “finalization step” (notification distribution instructions), the 
notification Distribution Status will not be changed. Therefore, to distribute this notification, clients will need to 
call one of the “Redistribute a Notification” endpoints (depending on whether the notification must be 
redistributed to all or only to newly added recipients). 
The following chart illustrates the Notification Distribution flow: 
 
Create a Notification 
(endpoint: Create a 
Notification)
Was Finalization 
Step data provided?
Save notification 
with the Finalization 
Step data 
(Distribution 
Status=Pending 
Distribution)
Save notification 
without the 
finalization step data 
(Distribution 
Status=Draft)
YES
NO
Does notification 
and/or finalization 
step require 
revisions?
Provide updated 
notification, all 
notification data 
must be provided 
(endpoint: Update a 
Notification) 
YES
Distribute Notification 
(endpoints: Distribute 
Notification, 
Redistribute to All 
Notification, 
Redistribute to New 
Notification)
NO
 

---

## Page 16

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 16 
 
6. Receive My Created Notifications  
Clients can request and receive notifications created by their organization ([[DTCC]] [[participant]] Number). This 
includes notifications with Distribution Status = Draft / Pending Distribution / Revised-Pending Distribution / 
Distributed. To receive notifications submitted by your organization, you must invoke the following endpoints in 
the order outlined below. The listing will include all notifications (based on the provided search criteria) that 
were created via API calls and/or UI. 
a) Invoke one of the following endpoints to get a list of submitted notifications:  
Notes:  
• Only one of these endpoints should be invoked. The returned list will contain all notifications created by your 
organization (regardless of the notifications’ Distribution Status and method – API vs UI).  
• Each notification returned by the following endpoints will have an “approvalStatus” field. Approval Status is 
automatically assigned to each notification for those organizations that utilize the approval workflow. This 
field is part of the model for all notifications.  
This field will be blank if 1) your organization is not utilizing the approval workflow or 2) your 
organization is utilizing the approval workflow, but the notification was created and/or distributed via an 
API call.  
If your organization utilizes the approval workflow, this field will contain the latest approval status if the 
notification was created and/or distributed via UI. 
 
o Receive a list of notifications submitted by the [[participant]] Number(s) associated with the provided 
OCODE 
GET  /ocode/{ocode}/submitted/notifications 
This endpoint is intended for clients and/or service providers whose Ocodes are associated with 
multiple [[DTCC]] [[participant]] Numbers subscribing to MF Info Xchange. 
The endpoint will return a list of notifications created by each [[participant]] Number associated with the 
provided Ocode.  
o Clients with one [[DTCC]] [[participant]] Number and/or service providers whose Ocodes are NOT 
associated with multiple [[DTCC]] [[participant]] Numbers can utilize the following endpoint to Receive a 
list of notifications submitted by the provided [[participant]] Number. 
GET  /client/{clientId}/submitted/notifications/search 
o Clients and/or service providers can receive a list of notifications (submitted by the provided 
[[participant]] Number) that contain one or more of the specified Security Issue IDs 
GET  /client/{clientId}/submitted/notifications/[[securities]] 
NOTE:  
A notification (Event [[ID]]) may be returned multiple times – if the notification contains more than one of the 
specified Security Issue IDs (once for each requested Security Issue [[ID]] provided within the notification). 
 
b) Receive Notification Details 
GET  /client/{clientId}/submitted/notifications/{eventId} 
Once you have received a list of notifications (utilizing one of the above endpoints), you can make 
calls to retrieve individual notification details by invoking this endpoint. A separate call must be made 
for each notification that is of interest. 

---

## Page 17

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 17 
 
Note:  
Notification details will contain a “status” field (within tables/arrays). This field is for [[DTCC]] use only and will be 
blank.  
 
7. Receive A List of Organizations Subscribing to MF Info Xchange 
GET  /subscribing-clients  
If a notification is being distributed to specific organizations (for example FirmA and FirmB, rather than “All” 
subscribing clients), you will need to provide a list of subscribing [[participant]] numbers in the finalization step 
when distributing a notification (to display the notification on these receivers’ MF Info Xchange portals and to 
allow them to request the data via API calls).  
This endpoint will return a list of all [[DTCC]] clients subscribing to MF Info Xchange. Based on this list, you will be 
able to determine if the intended receivers of your notification are subscribing to the service. If a notification is 
meant for a specific organization(s) that [[DO]] not subscribe (based on the data returned by this endpoint), 
“portalFirms” field in the finalization step (provided on the Create a Notification or Update a Notification 
endpoints) must be populated with “1” (non-subscribing firms).  
 
8. Receive A List of Clients and Their Email Designations 
GET  /client/{clientId}/receiver-emails 
This endpoint returns a list of MF Info Xchange clients and their email designations for a specific Event Type. A 
separate call must be made for each event type that is of interest. This list will not return any clients who did 
not provide email designations for the specified Event Type.  
Clients are advised to invoke this endpoint prior to distributing a notification to determine if any additional email 
addresses/distribution lists need to be added to the notification distribution instructions  (“finalization step”).  
Firms sending Large Trade Notifications are advised to invoke this endpoint before distributing their 
notifications to determine if the receiving funds have designated email addresses.  
 
9. Receive MF Profile Security data  
GET  /client/{clientId}/notifications/firm-profile-data/{participantNumber} 
This endpoint returns MF Profile Security data (including the Large Trade Dollar Threshold Amount  – 
“largeTradeDollarThreshold” field) for a specified Security Issue [[ID]] and Fund [[participant]] Number.  
“fundStatus” field provides a fund status: Open, Closed-Liquidated or Closed-Merged. 
Note:  
Firm clients can search for one or multiple Security Issue IDs (“secIssueId” parameter). If this parameter is not provided on 
the endpoint, search results will return MF Profile Security data for all Security Issue IDs for the specified Fund [[participant]] 
Number. 
Firms are advised to invoke this endpoint (prior to creating and distributing a Large Trade Notification) to receive the large 
trade threshold $ amount for Security Issue [[ID]](s) that require a Large Trade Notification. Based on the returned threshold 
and the trade $ amount, firms will determine if a Large Trade Notification is required for this trade. 

---

## Page 18

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 18 
 
10. Create and Distribute a Notification - Flow Diagram 
The following diagrams depicts the steps required to create and distribute a notification. The charts also 
reference additional functionality (endpoints) that will assist you when creating and distributing a notification via 
API calls.  
Corresponding API endpoints are listed within each action item. This is only a pictorial view. For more 
information, please refer to the endpoints described in this section.  Please refer to the MF Info Xchange User 
Guide for more information on how to create/distribute a notification. 
• Create and distribution a notification (excludes Large Trade Notifications)  
 
 
Create/Update Notification 
(endpoints: Create a 
Notification, Update a 
Notification)
Distribute a Notification
 (endpoints: Distribute a 
Notification, Redistribute to 
All, Redistribute to New)
Create/Update Distribution 
List. Review Distribution List 
(endpoints: Create 
Distribution List, Update 
Distribution List, Receive 
Distribution List Details)
Clients subscribing to MF 
Info Xchange 
(endpoint: Receive a list of 
organizations subscribing to 
MF Info Xchange)
Review Receivers  Email 
Designations 
(endpoint: Receive a List of 
Clients and their Email 
designations for an Event 
Type)
Review Notification Details 
(endpoint: Receive 
Notification Details) 
1. Notification is displayed 
on the Receivers  portals 
and Event Calendars and is 
available via API calls
2. Notification Emails are 
sent to the Receivers 
NOTE: Endpoints 1, 2 and 3 will return data required in order to 
distribute a notification (endpoint: Distribute a Notification)
1
2 3
 

---

## Page 19

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 19 
• Create and distribute a Large Trade Notification 
Retrieve (from Profile Security) 
large trade threshold for the 
impacted Fund
(endpoint: Receive Profile Security 
Data)
Retrieve a list of clients 
subscribing to MF Info Xchange 
(endpoint: Receive a list of 
organizations subscribing to MF 
Info Xchange)
Is large trade threshold 
available?
Proceed with notification?
END
YES
Does trade 
$ amount exceed 
large trade threshold 
in Profile 
Security? 
Large Trade Notification
Can contain multiple trades. All trades must be for the same Fund [[DTCC]] Part Number and the same Anticipated Trade Date
Does the impacted  fund 
subscribe to 
MF Info Xchange? 
Retrieve a list of funds with their 
email designations for Large Trade 
Notifications (endpoint: Receive a 
list of clients and their email 
designations)
Did the fund
 designate email(s) for Large Trade 
Notifications?
Create and Distribute Large Trade Notification (endpoints: Create a Notification, 
Distribute a Notification)
Note: If the fund does not subscribe to MF Info Xchange and/or did not designate 
emails, provide fund s email address(s) and proceed to create and distribute a 
large trade notification
NO
YES
YES
NO
NO
YES NO
YES
NO
Large Trade Notification - 1) created/saved in MF Info Xchange database 2) 
distributed to the impacted fund 3) generates email(s) to the receiving fund 4) 
posted to the firm s portal 5) posted to the fund s portal (if the fund subscribes to 
MF Info Xchange) 6) fund (if subscribes to MF Info Xchange) can view notification 
via the portal and/or API call
 
 
 
 
 
 
 
 
 

---

## Page 20

MF Info Xchange API Capabilities – Technical Guide 
Notification Submitter Functionality – API calls 20 
11. Receive my Consolidated [[Dividend]]/Capital Gain or 
Interval/Tender Fund Schedule 
Fund Clients can request and receive their organization’s consolidated [[Dividend]]/Capital Gain or 
Interval/Tender Fund schedule (based on all schedules submitted by their organization) by making one of the 
following calls. The schedule includes all notification data (submitted via API calls and/or UI).  
Note:  
Only one of the following endpoints should be invoked. The returned list will contain all schedules submitted by your 
organization and distributed to the receiving firms. Notifications with Distribution Status = Draft, Pending Distribution will not 
be included in the consolidated schedule. Notifications with Distribution Status = Revised Pending Distribution will be 
included with the data that was present on the notification at the time of the last distribution. A separate call must be made 
for each schedule type. 
• Receive a consolidated schedule of all events submitted by the [[participant]] Number(s) associated with 
your OCODE for the specified schedule type 
GET  /ocode/{ocode}/submitted/notifications/consolidated-schedule 
This endpoint is intended for clients and/or service providers whose Ocodes are associated with multiple 
[[DTCC]] [[participant]] Numbers subscribing to MF Info Xchange. 
Note:  
The endpoint will return consolidated schedules created by each fund client associated with the provided Ocode.  
• Receive a consolidated schedule of all events submitted by your organization for the specified schedule 
type 
GET  /client/{clientId}/submitted/notifications/consolidated-schedule 
Clients with one [[DTCC]] [[participant]] Number and/or service providers whose Ocodes are NOT associated 
with multiple [[DTCC]] [[participant]] Numbers can invoke this endpoint to receive a consolidated schedule 
created by their [[participant]] Number. 
• Clients and/or service providers can receive a consolidated schedule of all events (submitted by your 
organization) that contain one or more of the specified Security Issue IDs 
GET  /client/{clientId}/submitted/notifications/consolidated-schedule/[[securities]] 
The endpoint will return a consolidated schedule (filtered by Security Issue IDs) created by your 
organization.  

---

## Page 21

MF Info Xchange API Capabilities – Technical Guide 
Notification Receiver Functionality – API calls 21 
4. NOTIFICATION RECEIVER FUNCTIONALITY – API 
CALLS 
This section contains API endpoint information for notification receivers. 
1. Receive Notifications 
To receive notifications that were distributed to your organization/[[DTCC]] [[participant]] Number, you must invoke 
the following endpoints in the order outlined below. 
This data may only be used for the benefit of; or on behalf of the [[NSCC]] [[participant]] that is explicitly stat ed 
within the returned dataset. Subscribing clients must authorize their service providers to receive the data on 
their behalf, the service provider is not authorized to redistribute such data and must acquire data for those 
clients that have subscribed to the service and API’s.  
 
a) Invoke one of the following endpoints to get a list of received notifications: 
Notes: 
• Only one of these endpoints should be invoked. The returned list will contain all notifications received by 
your organization. 
• The returned list will contain “clientNb” and “companyName” fields identifying the submitter’s information 
([[participant]] number and company name). It will also contain “receivedDate” field identifying when the 
notification was received. Searching Notification by Ocode will also return “recipientClientNb” and 
“recipientName” fields identifying the receiver’s information ([[participant]] number and company name). 
• When requesting a list of received notifications, you can provide a received period 
(notificationReceivedDateStart and notificationReceivedDateEnd parameters).  
o For example, to receive a list of notifications distributed to your organization ([[participant]] 
Number) between December 1 and December 5, you can provide input parameters where 
notificationReceivedDateStart=12/01/2021 and notificationReceivedDateEnd=12/05/2021.  
o If you are making a call to receive a list of notifications multiple times a day for the same 
“received” date, both parameters must be set to the same date. For example, if you make 
a call every 30 minutes to receive notifications distributed to your [[participant]] Number 
today, both fields must be set to today’s date. 
• It is possible to receive the same Event [[ID]] multiple times. This could happen when 
o a call to receive the list of notifications is made multiple times a day for the same received 
period and/or  
o a call to receive the list of notifications does not include search criteria that would exclude 
previously received Event IDs and/or 
o the sender distributed a reminder or update and this action resulted in an updated 
distribution (Last Received Date).  
Therefore, it is important to check both “receivedDate” field and notification details to determine if you have 
already received this version of the notification (Event [[ID]]). 
 
  
 

---

## Page 22

MF Info Xchange API Capabilities – Technical Guide 
Notification Receiver Functionality – API calls 22 
• Notification search endpoints will return a Distribution [[ID]] (distributionId - unique number generated and 
assigned to each successful distribution of a notification by the MF Info Xchange system) for each received 
notification (Event [[ID]]). At the time of distribution, if there were any updates to the notification, a new 
Distribution [[ID]] will be assigned. Distribution [[ID]] can be used by the receiver to determine if the same 
version of the notification was previously received. It is recommended that clients save Distribution [[ID]] with 
the event details. 
• The following steps must be followed to determine if a notification has already been received. For each 
Event [[ID]] returned by notification search endpoints, check if this Event [[ID]] already exists on your system 
(from the previous calls).  
o If the Event [[ID]] already exists on your system, compare Distribution [[ID]] from the results returned by 
the current call with that of the Distribution [[ID]] stored on your system. 
• If Distribution [[ID]] is different, there was an update to the notification data and “Receive 
Notification Details” endpoint must be invoked to receive the revised notification. 
▪ If Distribution [[ID]] is the same, there was no update to the notification data and no further 
action is needed at this time. 
o If the Event [[ID]] does not exist on your system, you can request and receive notification data by 
invoking the “Receive Notification Details” endpoint. 
• Clients can also utilize the Distribution [[ID]] (“distributionId”) optional input parameter to retrieve data since 
their last API call. This will filter out notifications (Distribution Ids) that were received in a prior call. 
Distribution [[ID]] can be used as a standalone input/search parameter, as well as in combination with the 
other available input parameters. In order to filter out Distribution Ids that were received in a prior call(s) 
clients must provide the latest received Distribution [[ID]]. The system will check if any additional Distribution 
Ids were distributed to this client and will return only those Distribution Ids that are greater (received after) 
than the one provided within the API endpoint call. For example, if the last received Distribution [[ID]] was 
“10”, the next API call must specify “distributionId”=10. If any Distribution IDs greater than “10” were 
received by this client, the system will return these Distribution IDs (excluding Distribution [[ID]]=10). 
 
Distribution [[ID]] can be used as a single input parameter as well as in combination with other optional input 
parameters. For example, clients can search for Interval Funds notifications received since their last call for 
the Interval Funds notifications. In this case clients will need to provide “eventType” and “distributionId” 
parameters on the search endpoint. 
 
The following example illustrates the usage of “distributionId” parameter when requesting a list of 
notifications received since their last API call: 
Fund ABC distributes the following notifications to Firm XYZ: 
Event [[ID]] Distribution Date/Time Distribution [[ID]] 
12344 11/30/2022 9pm 1110 
12355 12/01/2022 9am 
12/01/2022 11am (notification update) 
1120 
1130 
12366 12/01/2022 2pm 1140 
12377 12/01/2022 10pm 1150 
 
 
 
 
 

---

## Page 23

MF Info Xchange API Capabilities – Technical Guide 
Notification Receiver Functionality – API calls 23 
Firm XYZ makes 3 API calls per day: at 12pm, 4pm and 11:59pm to get a list of notifications received 
during that day. The last/highest Distribution [[ID]] received in a prior API call is provided on each API call.  
API call made by Firm XYZ 
on date/time 
Distribution [[ID]] provided by Firm XYZ on 
the API call 
Event [[ID]] and Distribution [[ID]] 
returned by the API call 
11/30/2022 11:59pm 1105 (last distribution [[ID]] received via the 
previous API call) 
Event [[ID]] 12344 
Distribution [[ID]] 1110 
12/01/2022 12pm 1110 (last distribution [[ID]] received via the 
previous API call) 
Event [[ID]] 12355 
Distribution [[ID]] 1130 
Note: Distribution [[ID]] 1120 will not 
be returned since the notification 
was updated and the system returns 
the later version/Distribution [[ID]] 1130 
12/01/2022 4pm 1130 (last distribution [[ID]] received via the 
previous API call) 
Event [[ID]] 12366 
Distribution [[ID]] 1140 
12/01/2022 11:59pm 1140 (last distribution [[ID]] received via the 
previous API call) 
Event [[ID]] 12377 
Distribution [[ID]] 1150 
 
o Receive a list of notifications received by the [[participant]] Number(s) associated with the provided 
OCODE 
This endpoint is intended for clients and/or service providers whose Ocodes are associated with 
multiple [[DTCC]] [[participant]] Numbers subscribing to MF Info Xchange. 
GET  /ocode/{ocode}/received/notifications 
Note:  
If the same Event [[ID]]/Notification was sent to more than one [[participant]] Number associated with the provided 
OCODE, this Event [[ID]]/Notification will be returned multiple times (once for each [[participant]] Number to which it 
was sent). This information will identify which [[participant]] Numbers received this notification.  
o Clients with one [[DTCC]] [[participant]] Number and/or service providers whose Ocodes are NOT 
associated with multiple [[DTCC]] [[participant]] Numbers are advised to call the fo llowing endpoint to 
Receive a list of notifications received by the provided [[participant]] Number 
GET  /client/{clientId}/received/notifications/search 
o Clients and/or service providers can Receive a list of notifications (received by the provided 
[[participant]] Number) that contain one or more of the specified Security Issue IDs. This will allow firms 
to receive only notifications for the requested [[securities]] and reduce the noise by not returning event 
types that [[DO]] not reference any of the Security Issue IDs provided on the endpoint. 
GET  /client/{clientId}/received/notifications/[[securities]] 
 

---

## Page 24

MF Info Xchange API Capabilities – Technical Guide 
Notification Receiver Functionality – API calls 24 
Notes: 
• A notification (Event [[ID]]) that contains multiple Security Issue IDs from the supplied list of [[securities]], will be 
returned multiple times – once for each Security Issue [[ID]] identified by the system. 
• It is recommended that you invoke this endpoint once a new Security Issue [[ID]] is setup on your platform as 
the returned list of notifications might change depending on the list of provided Security Issue IDs. 
• The maximum number of characters that can be provided in the endpoint URL is 7,168. Therefore, if your 
list of Security Issue IDs exceeds the total number of allowed characters, the list must be split into multiple 
API calls to ensure that the number of characters on each endpoint does not exceed the maximum 
supported amount.  
 
b) Receive notification details 
Once you have received a list of notifications (utilizing one of the above endpoints), you can make 
calls to retrieve notification details. A separate call must be made for each notification (Event [[ID]]) that 
is of interest. 
GET  /client/{clientId}/received/notifications/{eventId} 
It is recommended that you make a call to receive notification details up until the Effective Date of the 
notification as notification data could have been updated by the sender.  
Notes: 
• Notification details will contain “receivedDate”, “accountName” and “clientNb” fields identifying notification 
received date and submitter information (company name and [[DTCC]] [[participant]] number). 
• Notification details will contain a “status” field (within tables/arrays). This field is for [[DTCC]] use only and will 
be blank 
• “contactCompany” field will contain a Contact Company on a Large Trade Notification. It will be blank on all 
other event types. 
• “rowId” field will contain system assigned row ids. This will apply only to the “repeatable” sections of the 
notifications. Notification receivers can discard/ignore these values or save these Row Ids with the 
notification data. In the event another version of the notification is received, clients can utilize Row Ids to 
identify if the new version of the repeatable section had any changes (by comparing data received to the 
previous version of the data with the same Row [[ID]]). For a complete list of notifications’ “repeatable” sections 
with the associated “status” and “rowId” fields, please refer to the Data Dictionary. 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 25

MF Info Xchange API Capabilities – Technical Guide 
Notification Receiver Functionality – API calls 25 
The following diagram depicts a flow of “Receive Notification” endpoints: 
Receive a list of notifications 
distributed to the [[participant]] 
Number(s) associated with 
the Ocode
Receive a list of notifications 
distributed to the receiver s 
[[participant]] Number
Receive a list of notifications 
(distributed to the receiver s 
[[participant]] Number) that 
contain one or more of the 
specified Security Issue IDs
OR
OR
Receive Notification Details 
for a specific Event [[ID]]
Identify Event IDs 
that are of interest
 
2. Receive Consolidated [[Dividend]]/Capital Gain or Interval/Tender 
Fund Schedule 
You can request and receive a consolidated [[Dividend]]/Capital Gain or Interval/Tender Fund schedule by 
making one of the following calls. 
This data may only be used for the benefit of; or on behalf of the [[NSCC]] [[participant]] that is explicitly stated 
within the returned dataset. Subscribing clients must authorize their service providers to receive the data on 
their behalf, the service provider is not authorized to redistribute such data and must  acquire data for those 
clients that have subscribed to the service and API’s.  
Note:  
Only one of these endpoints should be invoked. The returned list will contain all schedules received by your organization. 
• Receive a consolidated schedule of all underlying events received by the [[participant]] Number(s) 
associated with your OCODE for the specified schedule type 
GET  /ocode/{ocode}/received/notifications/consolidated-schedule  
This endpoint is intended for clients and/or service providers whose Ocodes are associated with multiple 
[[DTCC]] [[participant]] Numbers subscribing to MF Info Xchange. 
Note:  
The endpoint will return consolidated schedules for each receiving firm associated with the provided Ocode. If the 
same underlying Event [[ID]] was shared with multiple firms associated with the provided Ocode, this schedule will 
appear on each receiving firm’s consolidated schedule.  
Each firm’s consolidated schedule might differ from the other firms’ schedules. For example, Firm A’s 
consolidated schedule might be different from Firm B’s consolidated schedule (since consolidated 
schedules are based on the underlying fund notifications which may not have been shared with all firms).  
 
 

---

## Page 26

MF Info Xchange API Capabilities – Technical Guide 
Notification Receiver Functionality – API calls 26 
• Receive a consolidated schedule of all underlying events received by your organization for the specified 
schedule type 
GET  /client/{clientId}/received/notifications/consolidated-schedule  
Clients with one [[DTCC]] [[participant]] Number and/or service providers whose Ocodes are NOT associated 
with multiple [[DTCC]] [[participant]] Numbers can invoke this endpoint to receive a consolidated schedule. 
 
• Clients and/or service providers can receive a consolidated schedule (received by your organization) that 
contain one or more of the specified Security Issue IDs 
GET  /client/{clientId}/received/notifications/consolidated-schedule/[[securities]]  
Receive a consolidated schedule of all events for the specified schedule type ( shared with the provided 
[[participant]] Number) that contain one or more of the specified Security Issue IDs. 
 
Notes: 
• The endpoint will return a consolidated schedule (filtered by Security Issue IDs) for the provided [[participant]] 
Number.   
• The maximum number of characters that can be provided in the endpoint URL is 7,168. Therefore, if your 
list of Security Issue IDs exceeds the total number of allowed characters, the list must be split into multiple 
calls to ensure that the number of characters on each endpoint does not exceed the maximum supported 
amount. 
 
 

---

## Page 27

MF Info Xchange API Capabilities – Technical Guide 
Endpoint Parameters – additional considerations 27 
5. ENDPOINT PARAMETERS – ADDITIONAL 
CONSIDERATIONS 
This section provides additional information on the key endpoint parameters listed in the [[DTCC]] API 
Marketplace. 
“Receive Notifications” Endpoints 
The following search parameters are available on the “Receive Notifications” endpoints (applies to both 
Receiver and Submitter functionality) when requesting a list of notifications by utilizing Ocode/[[participant]] 
Number/Security Issue IDs endpoints: 
• Event Status 
• Event Type 
• Effective Date Start Date 
• Effective Date End Date 
• Notification Received Start Date – on the Receiver’s endpoints.  Notification Distributed Start Date – on 
the Submitter’s endpoints 
• Notification Received End Date – on the Receiver’s endpoints.  Notification Distributed End Date – on the 
Submitter’s endpoints. 
• Company [[ID]](s) - on the Receiver’s Endpoints.  Provide a list of notification submitters ([[participant]] 
numbers). For example, if you want to receive a list of notifications provided by Organization A and 
Organization B. 
• Security Issue [[ID]](s) – Notifications filtered by Security Issue IDs endpoints. Provide a list of Security Issue 
IDs to filter search results. 
• Client [[ID]] – on all endpoints (excluding ocode endpoints). [[participant]] Number of the client making the call.  
 Receive Notifications (receiver API endpoints) Receive Notifications (submitter API 
endpoints) 
 Search by Ocode Search by 
[[participant]] 
Number 
Search by 
Security 
Issue IDs 
Search 
by 
Ocode 
Search by 
[[participant]] 
Number 
Search by 
Security 
Issue IDs 
Input 
parameters 
(on all 
endpoints) 
Event Status, Event Type, Effective Date Start Date, 
Effective Date End Date, Notification Received Start 
Date, Notification Received End Date, Company [[ID]](s), 
Distribution [[ID]] 
 
Event Status, Event Type, Effective Date 
Start Date, Effective Date End Date, 
Notification Distributed Start Date, 
Notification Distributed End Date  
Additional 
Input 
parameters 
ocode clientid clientid, 
Security 
Issue [[ID]](s) 
ocode clientid clientid, 
Security 
Issue [[ID]](s) 
Output 
parameters 
(on all 
endpoints) 
clientNb, companyName, distributionId, receivedDate, clientNb, distributionId 
Additional 
output 
parameters 
recipientClientNb, 
recipientName 
     

---

## Page 28

MF Info Xchange API Capabilities – Technical Guide 
Endpoint Parameters – additional considerations 28 
 
“clientNb” and “companyName” – these fields identify the submitter of the notification ([[participant]] number and 
company name). 
“recipientClientNb” and “recipientName” – these fields identify the receiver of the notification ([[participant]]  
number and company name). 
 
“Receive Notification Data” Endpoints 
• The following input search parameters are required on the “Receive notification data by Event [[ID]]” 
endpoints (both submitter and receiver endpoints): 
o Client [[ID]] 
o Event [[ID]] 
 
• The following output parameters will be returned by the endpoint (in addition to the event notification data): 
o Submitter Search (Receive notifications data for an Event [[ID]] that was submitted by the provided 
[[participant]] Number – “view own notification”): 
- eventId 
- eventType 
- distributionStatus 
- submittedBy 
- dateSubmitted 
- distributionDate 
- accountName 
- clientNb 
o Receiver Search (Receive notifications data for an Event [[ID]] that was shared with the provided 
[[participant]] Number – “view received notification”): 
- eventId 
- eventType 
- receivedDate 
- accountName 
- clientNb 
“clientNb” and “accountName” – these fields identify the submitter of the notification ([[participant]] number and 
company name). 
 
“Receive Consolidated Schedules” Endpoints 
The following search parameters are available on the “Receive Consolidated Schedules” endpoints (applies 
to both Receiver and Submitter functionality) when requesting consolidated schedules by utilizing 
Ocode/[[participant]] Number/Security Issue IDs endpoints: 
• Event Type 
• Date 
• Year 

---

## Page 29

MF Info Xchange API Capabilities – Technical Guide 
Endpoint Parameters – additional considerations 29 
• Quarter 
• Month 
• Fund Number(s) - on the Receiver’s Endpoints ([[participant]] numbers).  Provide a list of funds to filter 
search results. For example, if you want to receive Consolidated Schedules provided by Organization A 
and Organization B. 
 Receive Consolidated Schedule (receiver API 
endpoints) 
Receive Consolidated Schedule 
(submitter API endpoints) 
 Search by Ocode Search by 
[[participant]] 
Number 
Search by 
Security Issue 
IDs 
Search 
by 
Ocode 
Search by 
[[participant]] 
Number 
Search by 
Security 
Issue IDs 
Input 
parameters (on 
all endpoints) 
Event Type, Date, Year, Quarter, Month Event Type, Date, Year, Quarter, Month 
Additional 
Input 
parameters 
ocode clientid, Fund 
Number(s)  
clientid, 
Fund 
Number(s), 
Security Issue 
[[ID]](s) 
ocode clientid clientid, 
Security 
Issue [[ID]](s) 
Output 
parameters (on 
all endpoints) 
clientNB, companyName clientNb, companyName 
Additional 
output 
parameters 
recipientClientNb, 
recipientName 
     
 
Event Type – schedule type ([[Dividend]]/Capital Gain Schedule OR Interval/Tender Fund Transaction Schedule) 
“clientNb” and “companyName” – these fields identify the submitter of the schedules (fund [[participant]] number 
and [[participant]] name). 
“recipientClientNb” and “recipientName” – these fields identify the receiver of the schedules (firm [[participant]] 
number and [[participant]] name). 
Pagination 
• Input parameters 
• “pageSize” and “pageNumber” fields on the “receive data” endpoints allow users to specify the number of 
records to be returned on each page and page number. 
o “pageSize” field – clients can provide the number of records to be returned on each page. The [[default]] 
value is 100 but can be changed to a different number. 
o “pageNumber” field – clients can provide the page to be returned when making a call. The [[default]] 
value is 1 
For example, Receive Notifications endpoints will return a list of notifica tions based on the provided input  
parameters. To manage the number of returned records, clients can specify the number of records per page and 
which page (if there are multiple pages) to be returned. If there are multiple pages, clients must make another 
call with the next page number to receive the next page. Therefore , if you request 200 records per page, and 
there are 20 pages in total, you will need to make 20 calls to receive the entire list (each call should request the 
next pageNumber: 2, 3, 4 , …., 20) and would show 200 records.  “pageSize” and “page Number” are optional 
input parameters and if not provided they will be defaulted to 100 and 1 respectively.  

---

## Page 30

MF Info Xchange API Capabilities – Technical Guide 
Endpoint Parameters – additional considerations 30 
 
• Output (results) fields 
Returned results will contain the following pagination fields: 
o “pageNumber” field – will display the value provided on the input parameter 
o “pageSize” field- will display the value provided on the input parameter 
o “totalPages” field – will display the total number of pages for the invoked endpoint  
o “totalNumberOfRecords” field – will display the total number of records for the invoked endpoint 
 
Revision information on the Notification Submitter’s endpoints 
Notification submitters can create/update notifications and distribution lists via API calls. When requesting the 
current version of the notification or distribution list, the results will also show fields that provide information on 
the update (Who made the last update? When was the last update made?). The following fields will display this 
information: 
• Distribution List endpoints 
o “updatedBy” field displays the username of the user who made the last update 
o “lastUpdatedTs” field displays the date and timestamp of the last update 
 
• Search notifications endpoints 
o “lastUpdated” field displays the username of the user who made the last update 
o “lastUpdatedBy” field displays the date of the last update 
 
Fields with multiple values 
The following notification fields allow multiple values. The values will be separated as follows  on the returned 
results (when receive notification endpoints are invoked). The same format must be followed when invoking 
create/update notification endpoints. 
• finalizationStep – all event types 
o emails – multiple values must be separated by commas without spaces (e.g. value1,value2,value3) 
o portalFirms - multiple values must be separated by semicolons without spaces (e.g. 
value1;value2;value3) 
o receiverEmailList - multiple values must be separated by semicolons without spaces (e.g. 
value1;value2;value3) 
o distributionList - multiple values must be separated by semicolons without spaces (e.g. 
value1;value2;value3) 
• Account/History Purge notification – “appMatLevel” field (Account Purge Criteria – Applicable Matrix 
Levels). Multiple values must be separated by commas with spaces (e.g. value1, value2, value3) 
• [[Dividend]]/Capital Gain Schedule notification – “notification” field. Multiple values must be separated by 
commas without spaces (e.g. value1,value2,value3).  

---

## Page 31

MF Info Xchange API Capabilities – Technical Guide 
Frequently Asked Questions 31 
6. FREQUENTLY ASKED QUESTIONS 
1. What [[DO]] I need to [[DO]] to start using MF Info Xchange APIs? 
Clients must subscribe to MF Info Xchange and MF Info Xchange APIs.  Please contact your Relationship 
or Account Manager for assistance with service subscriptions. 
 
2. What user [[ID]] / role does my organization need to utilize API capabilities? 
Your organization needs a robot [[ID]] provisioned by your Access Coordinator with one of the following roles : 
o Create and Modify Data Request – API ONLY. This robot persona user has access to create, update, 
and delete data via APIs 
o Pull Data Request – API ONLY. This robot persona user has access to pull data via APIs. 
 
3. Can I create and distribute notifications via API calls? 
Yes, you can create and distribute notifications via API calls. 
 
4. Can I receive notification data via API calls? 
Yes, you can receive notification data via API calls. 
 
5. If I utilize API capabilities to send and/or receive notification data, does my contra party need to use 
APIs as well?    
No, MF Info Xchange supports submission and receipt of notification data via UI as well as API calls. There 
is no dependency between the method used to create/distribute notification data vs the method used by 
the receivers to access the data.   
 
6. If I utilize API capabilities to send and/or receive notification data, can I continue t o use the UI? 
Yes, communication methods (UI and API calls) are not mutually exclusive. You can create a notification 
via API and update/distribute it through the UI or vice versa.  
In addition, you can utilize APIs for certain functionality (for example to send and/or receive certain types of 
notifications) but use the UI for other event types. 
 
7. If I create and distribute notification(s) via APIs, will the system generate emails to the receivers?  
Yes, you will need to provide distribution list(s) and/or emails when distributing a notification via APIs. 
Emails will also be generated based on the instructions provided in the Distribute Notification API call.  
 
8. If I utilize API calls to receive notification data, will I continue to receive emails?  
Yes, if you designated email(s) for this event type and/or notification submitter includes your designated 
emails or provides your email address(s) when distributing a notification, you will receive an email with the 
excel attachment. 
 
 
 

---

## Page 32

MF Info Xchange API Capabilities – Technical Guide 
Frequently Asked Questions 32 
9. If I utilize API calls to receive notification data, will I be able to see these notifications on my 
dashboard in the UI? 
Yes, all notifications distributed to your [[participant]] Number will appear on your MF Info Xchange portal.  
 
10.  If I utilize API calls to create and distribute notifications, will I be able to see these notifications on 
my dashboard in the UI? 
Yes, all notifications created via API calls will be available on your MF Info Xchange portal.  
 
11. If I utilize API calls to create and distribute notifications, will the receiver be able to see these 
notifications on their dashboard/calendar in the UI? 
Yes, event IDs created via API calls will be available on the subscribing receivers’ portals.  
 

---

## Page 33

MF Info Xchange API Capabilities – Technical Guide 
Data Dictionary 33 
7. DATA DICTIONARY 
This section provides a data dictionary of the data elements corresponding to Steps1, 2 and 4 of the 
notification in the UI (for each MF Info Xchange event type). 
 
Step 1 – initialStep (API term).  
Note:  
“eventType” field is a Step 1 field in the UI, however it is not included in the “initialStep” on the API endpoints. This field will 
appear as a standalone field in the notification model and will not be included within the “initialStep” fields. 
Step 2 – notificationData (API term) 
Step 4 – finalizationStep (API term) 
Notes: 
• All dates must be submitted in the mm/dd/yyyy format. 
• All [[participant]] number fields must be submitted as an 8-byte value. If the number is less than 8 bytes, you must add 
leading zeroes. For example, 00001234 or 00000123 or 00000012 or 00000001. 
 
Data Dictionary 
mfix-data-dictionary.
pdf
 
 
 


---

## Page 34

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: January 8, 2024 
Publication Code: MFS354 
Service: MF Info Xchange 
Title: MF Info Xchange API Capabilities – Technical Guide  
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 