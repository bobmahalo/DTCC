---
title: "ClaimConnect™ QuickGuide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ca131_claimconnect_quickguide_v3.0_20200714.pdf"
pages: 40
size: "1826.3 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ClaimConnect™ QuickGuide

**Original File:** [ca131_claimconnect_quickguide_v3.0_20200714.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ca131_claimconnect_quickguide_v3.0_20200714.pdf)  
**Category:** Other  
**Total Pages:** 40  
**File Size:** 1826.3 KB  

---

## Page 1

 
 
 
CORPORATE ACTIONS 
CLAIMCONNECT™ QUICK GUIDE 
VERSION 3.0 
JULY 14, 2020 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: July 14, 2020 
Publication Code: CA131 
Service: Corporate Actions  
Title: ClaimConnect™ Quick Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
About ClaimConnect™ ........................................................................................................................................ 5 
ClaimConnect™ [[settlement]] Flow ....................................................................................................................... 5 
ClaimConnect™ Processing ............................................................................................................................... 6 
Claim Status ........................................................................................................................................................ 7 
Matching ................................................................................................................................................................ 8 
Dashboard ............................................................................................................................................................. 9 
Unmatched Claims.............................................................................................................................................. 9 
Claim Count by Age .......................................................................................................................................... 10 
Matched Claims / Submit a Claim / Claims Pending Action ............................................................................. 11 
Entering a Claim ................................................................................................................................................. 12 
Searching For a Claim ....................................................................................................................................... 13 
Claim Search Engine: Quick Search ................................................................................................................ 13 
Claim Search Engine: Advanced Search ......................................................................................................... 14 
Claim Status Type ........................................................................................................................................... 15 
Search Results Page ........................................................................................................................................ 16 
Claims Inquiry / View Screen ............................................................................................................................ 17 
View (Screen Areas) ......................................................................................................................................... 17 
View ................................................................................................................................................................. 18 
Additional Data ................................................................................................................................................ 18 
Claim History ................................................................................................................................................... 19 
Attachments ...................................................................................................................................................... 20 
Attaching a Document ..................................................................................................................................... 21 
Viewing a Document ....................................................................................................................................... 23 
Affirm ................................................................................................................................................................. 23 
Modify ............................................................................................................................................................... 23 
DK ..................................................................................................................................................................... 25 
Un-DK ............................................................................................................................................................... 25 
Cancel ............................................................................................................................................................... 26 

---

## Page 4

 
 
Claim Approval ................................................................................................................................................... 27 
Finding Claims Requiring Approval .................................................................................................................. 27 
Approving or Rejecting Claims ......................................................................................................................... 29 
Approve/Reject Requirements and Scenarios .................................................................................................. 30 
Client Profile ....................................................................................................................................................... 33 
Adding a Profile Entry ....................................................................................................................................... 34 
Adding to an Email Alert List ........................................................................................................................... 34 
Adding an Individual Contact .......................................................................................................................... 35 
Adding a Group Contact .................................................................................................................................. 35 
Editing an Existing Profile Entry ........................................................................................................................ 36 
Deleting an Existing Profile Entry ..................................................................................................................... 36 
Viewing Contact Information ............................................................................................................................. 36 
Setting Approval Information ............................................................................................................................ 36 
Viewing Reports ................................................................................................................................................. 39 
 

---

## Page 5

ClaimConnect™ Quick Guide 
About ClaimConnect™ 5 
ABOUT CLAIMCONNECT™ 
[[DTC]] is leveraging preexisting clearing matching technology to allow for the bilateral facilitation of claims that 
are not currently processed by [[DTC]]. Claims can be automatched by the system based on a core set of fielded 
data within the claim itself. 
For items that are not automatched, the ClaimConnect™ service allows clients to submit a claim, view and edit 
their claims, affirm a claim, DK a claim, un-DK a claim, and cancel a claim.  
ClaimConnect™ [[settlement]] Flow 
In an ideal scenario: 
1. A client submits a claim to a counterparty.  
2. That counterparty affirms the claim. 
3. The claim is open and ready to settle, just like an automatched trade.  
4. On [[settlement]] date, an SPO is made and the claim is closed. 
 
 


---

## Page 6

ClaimConnect™ Quick Guide 
About ClaimConnect™ 6 
ClaimConnect™ Processing 
The originator of the claim can perform these actions: 
1. Submit the original claim. 
2. Modify the original claim BEFORE it has been affirmed or DK’d. 
3. Modify a claim AFTER it has been DK’d by the counterparty and returned to you. 
4. Cancel the claim BEFORE it has been affirmed or DK’d by the counterparty, or AFTER it has been DK’d 
by the counterparty. 
 
The counterparty of the claim can perform these actions: 
1. Affirm a claim. This can be the original or a version that has been resubmitted by the originator after an 
initial DK. 
2. Submit a corresponding claim to automatch the original claim in the system. 
3. DK a claim sent by the originator. 
4. Cancel a DK that you have performed. 
5. Undo a DK that you have performed. 
 


---

## Page 7

ClaimConnect™ Quick Guide 
About ClaimConnect™ 7 
Claim Status 
A claim’s status changes whenever an action is performed on it: 
 
A claim is Uncompared when it is awaiting action by the counterparty. This occurs when: 
• A claim is initially submitted by the originator, 
• A claim is modified by the originator before the counterparty has taken action on it, or 
• A claim is modified by the originator after it has been DK’d by the counterparty. 
A claim is Cancelled when the originator removes their claim from the system. This occurs when: 
• The originator cancels their claim before it has been affirmed or DK’d, or 
• The originator cancels a claim that has been DK’d by the counterparty. 
A claim is Open when a matched claim is awaiting [[settlement]]. This occurs when: 
• It has been automatched by [[DTC]], or 
• It has been affirmed by the counterparty. 
A claim is Closed when a matched claim is settled at [[DTC]]. This follows a status of “Open.”  


---

## Page 8

ClaimConnect™ Quick Guide 
Matching 8 
MATCHING 
Trade information includes the following fields. The table below indicates which fields must contain identical 
information in order to be automatched by the ClaimConnect™ utility.  
Field Name Fields Must Match Exact Match Required 
Claim Xref N N 
[[CUSIP]] Y Y 
Event Type Y Y 
Credit / Debit Y Y 
ClaimConnect™ Amount Y Y* 
Contra Party Y Y 
ClaimConnect™ [[settlement]] Date Y Y 
Event Record Date Y Y 
Event Payable Date Y Y 
Event Ex-Date Y Y 
Event Effective Date Y Y 
Event Expiration Date Y Y 
Event Cash Rate Y Y 
Original Trade – Trade Date Y Y 
Original Trade – Contractual [[settlement]] Date Y Y 
Original Trade – Actual [[settlement]] Date Y Y 
Original Trade Share Quantity Y Y 
Original Trade Cash Amount Y Y 
[[participant]] Notes N N 
* In the future, there may be a matching tolerance associated with this field. In the early iterations of this 
system, though, the ClaimConnect™ amount must be an exact match. 
 
 

---

## Page 9

ClaimConnect™ Quick Guide 
Dashboard 9 
DASHBOARD 
The ClaimConnect™ dashboard is the main page for the interface. You can see at a glance the claims that are 
in each stage of the affirmation process. 
This page provides many ways to view your claims – in total or divided into different categories. 
Unmatched Claims 
 
• The 3 compartments on the left are for items that originated with you. 
• The 3 compartments on the right are for items that originated with a contra party. 
• Within each of the 6 compartments, click on a blue number link to view the debit claims, credit claims, or 
total claims (debit and credit) for each category.  


---

## Page 10

ClaimConnect™ Quick Guide 
Dashboard 10 
Claim Count by Age 
 
Any compartment allows you to view the age of debit and credit claims in that category. Clicking on the drop-
down arrow allows you to see the number of items that have been in ClaimConnect™ for: 
• 0-5 days, 
• 6-30 days, 
• 31-60 days, 
• 61-90 days, and 
• More than 90 days. 
Click the link next to any down arrow to view all items represented in the count being displayed.  


---

## Page 11

ClaimConnect™ Quick Guide 
Dashboard 11 
Matched Claims / Submit a Claim / Claims Pending Action 
 
The 2 compartments on the bottom show numbers for matched claims (regardless of the origin of the claims). 
• Open matched claims are on the left. 
• Matched claims that closed today are on the right. 
Click Submit a Claim to enter a new claim. 
Click a blue number under the Claims Pending Action pie chart to access a list of all claims that have not 
been closed or canceled. You can also view separately all debits or all credits that have not been canceled. 
The pie chart shows the proportional number of claims or dollar value for the displayed categories. 
• Click Claims to view this chart by number of claims in each category. 
• Click Values to view this chart by the dollar amount of the claims in each category. 
• Click any category to add or remove it from the pie chart.  


---

## Page 12

ClaimConnect™ Quick Guide 
Entering a Claim 12 
ENTERING A CLAIM 
 
1. From the menu bar, click Claim Management > Enter Claim. 
The “Enter Claim” page appears. The claim entry wizard consists of five sections. 
Click an Expand All  button to open all sections of the wizard.  
Click the number on the wizard to switch to that section. 
 
2. Enter all claim information in the entry fields for each section. 
Please see the Selected Field Definitions table for more information on the Settle After Match feature and 
other fields. 
3. When you have filled out all fields for an individual numbered section, click the name or number for the 
next section on the navigation strip. 
4. If you have entered all fields correctly, the section number you just completed will display an 
“All Clear” message and a check mark.  
5. To use this information for your next entry, click the Fill My Next Input Screen With This Data checkbox. 
6. Click Submit. 
7. Click OK in the submission confirmation box. A window appears that contains your claim details. This 
record now appears when you search for Comparison > Uncompared claim status types. 


---

## Page 13

ClaimConnect™ Quick Guide 
Searching For a Claim 13 
SEARCHING FOR A CLAIM 
Claim Search Engine: Quick Search 
1. From the menu bar, click Claim Management > Claim Search Engine. 
 
 
2. Select to search by Claim [[ID]] or Claim Xref. 
 
 
3. Type the identifying number of the claim. 
 
4. Click Submit. 
 
  


---

## Page 14

ClaimConnect™ Quick Guide 
Searching For a Claim 14 
Claim Search Engine: Advanced Search 
 
1. From the menu bar, click Claim Management > Claim Search Engine. 
 
 
2. Enter search criteria in the entry fields. 
 
 
3. Use the check boxes to select the claim status type you are searching for. 
 
4. Click Submit. 
  


---

## Page 15

ClaimConnect™ Quick Guide 
Searching For a Claim 15 
Claim Status Type 
Use the following Comparison search criteria to find claim items from YOUR firm: 
Search Criterion Retrieves 
All All claim items in any state that originated from your firm. 
Matched Claims that have been matched by the system and have a status of “Open.” These 
items are awaiting [[settlement]]. 
Uncompared Claims that you have sent to a contra party that are awaiting THEIR action (either 
DK or Affirm). 
DKs - Contra Claims of yours that the contra party has DK’d. These items are awaiting YOUR 
modification or cancellation. 
Cancelled Claims that you have sent to a contra party that YOU have cancelled. These items 
were either uncompared claims awaiting action or claims of yours that the 
counterparty has DK’d. 
Closed Matched claims that have settled through an SPO. 
 
Use the following Advisory search criteria to find claim items from CONTRA firms: 
Search Criterion Retrieves 
All All claim items in any state that originated from a contra firm. 
Uncompared Advisory Claims that have been made against you by a contra party. These items are 
awaiting YOUR action: Affirm or DK. 
DKs – Initiated by Part Claims that have been made against you that YOU have DK’d. These items are 
awaiting action by the contra party (either modification or cancellation). 
DKs - Contra Claims of yours that the contra party has DK’d. These items are awaiting 
modification or cancellation. 
Cancelled Advisory Claims made against you by a contra party that THEY have cancelled. These items 
were either uncompared claims against you that were awaiting action or claims 
against you that YOU have DK’d. 
 
  

---

## Page 16

ClaimConnect™ Quick Guide 
Searching For a Claim 16 
Search Results Page 
 
Click any Claim [[ID]] to view that claim record. 
  


---

## Page 17

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 17 
CLAIMS INQUIRY / VIEW SCREEN 
This screen allows you to view claims that you have sent as well as claims that are made against you. You can 
perform several functions from the Inquiry / View screen: 
• View an audit trail and history for your existing claim. 
• Modify (edit) your claim when it is in an “Uncompared” or “Uncompared DK” state. 
• Cancel your claim when it is in an “Uncompared” or “Uncompared DK” state. 
• Affirm a claim that is made against you. 
• DK a claim that is made against you. 
• Un-DK a claim that has been made against you and that you have previously DK’d. 
• Attach a PDF document to a claim. 
 
View (Screen Areas) 
Click the black bars on this page to view sets of details for each area on the screen.  


---

## Page 18

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 18 
View 
This area of the screen displays top-level information about the claim as it currently exists in the system. Fields 
of particular note include: 
Field Name Definition 
Claim Xref An alphanumeric identifier for this claim within your company only. This 
number will not appear to the contra party submitting this claim. 
Cash Claim [[settlement]] Date Use the calendar tool to select the specific [[settlement]] date for this claim. 
Participants looking to settle a claim on the next available [[settlement]] slice 
(rather than a specific date or date in the future) can click the Settle After 
Match check box.  
If a firm submits a claim with the Settle After Match feature prior to 3:00 p.m. 
(the last [[settlement]] slice for the day) and a match is found in the system, then 
the claim will match with the current date. The [[settlement]] date will also be 
updated to the current [[settlement]] date.  
If a firm submits a claim with the Settle After Match feature after 3:00 p.m. 
and a match is found in the system, then the claim will match with the current 
date. The [[settlement]] date will be updated to the next business day.  
CA [[ID]] An identifying number used for Corporate Actions events, the Corporate 
Actions [[ID]] stays with an event throughout its lifecycle. 
DK Reason The explanation for why a claim has been DK’d. Please see the DK Reason 
Codes for further explanation. 
 
Additional Data 
This area of the screen displays metadata about the claim within ClaimConnect™. Fields of particular note 
include: 
Field Name Definition 
Claim Source Code A code that identifies where this claim originated.(“PWEB” for the Web 
application or “API” for the ClaimConnect™ API). 
Claim Source The origin of this claim: “PART” for “[[participant]]. 
Claim Event The code for the corporate actions event type associated with this claim. 
 
  

---

## Page 19

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 19 
Claim History 
This area of the screen displays a record of all actions that have taken place regarding this claim and its 
movement through ClaimConnect™. Fields of particular note include: 
Field Name Definition 
Status Displays the four-letter code of the claim at the point in its history represented by each 
row in the table. 
UNCP (on your claim) Uncompared. Your claim has not been 
matched. 
UNCP (on an advisory claim) Uncompared. The claim is an advisory 
against you and has not been matched. 
DKUN (on your claim) The other party has DK’d your claim. 
DKUN (on an advisory claim) Your company has DK’d a claim against you. 
CANC (on your claim) You have canceled your claim. 
CANC (on an advisory claim) The other party has canceled their claim. 
OPEN The claim is matched but not settled. 
CLSD The claim is settled and closed. 
 
Action Event This column displays the action that was taken on each iteration of the claim. 
AFFM Affirm. The contra party to the claim has acknowledged that the 
claim submitted against them is correct. 
CMPE Compare Exact. The claim has been compared and all fields 
match. 
CNUC Canceled Uncompared. The claim has been canceled by the 
submitting party before it has been compared by the system. 
DKUC DK Uncompared. The contra party has DK’d the claim before it 
has been compared by the system. 
DLVF Delivery (Full). The claim has matched and settled. Full delivery 
of the claim has been made. 
IMSD IMS Dropped. The claim was closed (CLSD) and dropped out 
from the Inventory Management System.  
IMSR IMS Rejected. This claim has been rejected by the Inventory 
Management System. The status is now closed (CLSD). 
INST Instruct. An instruction has been made upon the claim. 
MODP Modify Matching Field(s). After the claim has been matched, at 
least one of the matching fields was modified. 
MODX Modify Non-Matching Fields Only. After the claim was matched, 
at least one non-matching field was modified. 

---

## Page 20

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 20 
Field Name Definition 
SIMS Sent to IMS. This claim was sent to the Inventory Management 
System. 
UNDK Un-DK Uncompared. An uncompared claim that was previously 
DK’d by the recipient has since been un-DK’d and is awaiting 
comparison. 
 
Attachments 
If your login allows you to enter or edit claims, you are able to upload documents in PDF format only to 
accompany a claim in the following circumstances:  
• Immediately after submitting a claim 
• When modifying a claim 
• When DK’ing a claim 
• When viewing an opened or closed claim. 
 
Either party can view the other party’s documents. A user on each side of the claim will be able to upload a 
maximum of 5 documents, meaning that a maximum of 10 documents may be uploaded per claim.  
Each PDF file has a maximum size of 10 MB, meaning that a maximum of 100 MB can be added to each claim 
in total. 
  

---

## Page 21

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 21 
Attaching a Document 
To attach a file to a claim: 
1. Click the black Attachments bar. The bar turns green and the Attachments section opens. 
 
2. Click the Add Document button. The Upload Attachment window appears. 
 
3. Select the Attachment Type from the drop-down list: 
• Company Document 
• Agent Document 


---

## Page 22

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 22 
• Original Trade Details 
• CA Web Details 
• Other 
 
4. Click Browse to select the file you are uploading. 
 
5. Type any Comments about this document. You can enter a maximum of 300 characters. If you selected 
“Other” as the Attachment Type, you can describe the attached document here. 
 
6. Click Submit to upload the document to ClaimConnect™. Alternately, click Reset to reset all fields to their 
original state. 
 
  

---

## Page 23

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 23 
Viewing a Document 
You can view documents that you and/or your contra party have uploaded to a claim. 
To view a claim’s attached document: 
1. Click the black Attachments bar. The bar turns green and the Attachments section opens. 
 
2. Click the filename in the Attachments column. The PDF opens in a separate window. 
Affirm 
Affirming a claim means that you recognize the claim against you. Here, you are accepting the information as 
presented. All fields and screen areas are read-only except: 
Field / Item Name What Can I [[DO]]? 
Claim Xref Type an identifying reference number for this claim within your company only. This 
number will not appear to [[DTC]] or the party submitting this claim. 
[[participant]] Notes Type any notes regarding this claim. These notes will be unique to your company 
and will appear in the audit trail for this claim. 
Submit Click to affirm this claim. This returns the claim record to [[DTC]] with a status of 
“Open,” the same as if the original trade were auto-matched. 
Reset Click to clear the editable fields. 
Modify 
You can modify your own claim if it has one of the following statuses: 
• Uncompared (UNCP). The contra party has taken no action on your claim. 


---

## Page 24

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 24 
• DK-Uncompared (DKUN). The contra party has DK’d your claim, sending it back to you for your 
modification or complete cancellation. 
The fields on this screen are actionable (i.e., editable or otherwise usable) as follows: 
Field Name Field Type / Format Actionable Mandatory 
Claim Xref Alphanumeric Y Y 
[[CUSIP]] Alphanumeric Y Y 
Event Type Event Type Description Y Y 
Credit / Debit Credit / Debit N Y 
ClaimConnect™ Amount 999,999,999.99 Y Y 
Contra Party XXXXXXXX Y Y 
ClaimConnect™ [[settlement]] Date mm/dd/ccyy Y Y 
Event Record Date mm/dd/ccyy Y N 
Event Payable Date mm/dd/ccyy Y N 
Event Ex-Date mm/dd/ccyy Y N 
Event Effective Date mm/dd/ccyy Y N 
Event Expiration Date mm/dd/ccyy Y N 
Event Cash Rate 999,999,999.999999 Y N 
Original Trade – Trade Date mm/dd/ccyy Y N 
Original Trade – Contractual 
[[settlement]] Date 
mm/dd/ccyy Y N 
Original Trade – Actual [[settlement]] Date mm/dd/ccyy Y N 
Original Trade Share Quantity 9,999,999,999 Y N 
Original Trade Cash Amount 9,999,999,999.99 Y N 
[[participant]] Notes Alphanumeric and special characters 
This field may be updated only in 
conjunction with at least one other 
field. A piece of trade information must 
be changed for this claim to be 
considered modified.  
Y n/a 
DK Reason Description – text 
This information is entered by the 
contra party when it marks this claim 
as “DK” and is only viewable on claims 
with a status of “DKUN.” The 
information in this field may assist you 
in your modification of this claim, but 
you cannot edit the information in it. 
N n/a 

---

## Page 25

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 25 
Field Name Field Type / Format Actionable Mandatory 
Submit Button 
Click to submit your edited claim to the 
contra party. This claim will then have 
a status of “UNCD.” 
Y n/a 
Reset Button 
Click to clear all editable fields and 
enter claim information from scratch. 
Y n/a 
DK 
DK-ing a claim means that you [[DO]] not recognize the claim against you, or that some piece of it needs 
modification by the originating [[participant]]. You are able to add a reason code for the DK and make any notes 
for your internal reference.  
All fields and screen areas are read-only except: 
Field / Item Name What Can I [[DO]]? 
[[participant]] Notes Type any notes regarding this claim. These notes will be unique to your company 
and will appear in the audit trail for this claim. 
DK Reason Select the reason that you are DK-ing this claim: 
• Bad Quantity 
• Bad Trade Date 
• Bad [[settlement]] Date 
• Bad Amount 
• Bad [[Buyer]] (Receiver – Credit) Party 
• Bad [[Seller]] (Deliverer – Debit) Party 
• Duplicate Record 
• Invalid Security Identified 
• Need Paperwork 
• Need Medallion Stamp 
• [[settlement]] Date Difference 
• Other Bad Data 
• Wrong Event Type Wrong Event Date 
• Wrong Event Rate 
Submit Click to DK this claim. This returns the claim record to [[DTC]] with a status of “DKUN,” 
or “DK Uncompared.” 
Reset Click to reset the DK Reason field. 
 
Un-DK 
Un-DK-ing a claim is simply removing the “DK” state that you have placed on a claim made against your 
company. It restores the status of the claim to “UNCP,” or “Uncompared.” 

---

## Page 26

ClaimConnect™ Quick Guide 
Claims Inquiry / View Screen 26 
All fields and screen areas are read-only except: 
Field / Item Name What Can I [[DO]]? 
[[participant]] Notes Type any notes regarding this claim. These notes will be unique to your company 
and will appear in the audit trail for this claim. 
Submit Click to un-DK this claim. This returns the claim record to [[DTC]] with a status of 
“Uncompared,” the same as if a claim were just entered. 
Reset Click to clear the [[participant]] Notes field. 
Cancel 
You can cancel a claim that you have made against a contra firm. The claim must have a status of 
“Uncompared” (“UNCP”) or “DK Uncompared” (“DKUN”). Your claim will be removed from the contra party’s 
dashboard and will remain in your dashboard with a status of “Cancelled.” 
All fields and screen areas are read-only except: 
Field / Item Name What Can I [[DO]]? 
[[participant]] Notes Type any notes regarding this claim. These notes will be unique to your company 
and will appear in the audit trail for this claim. 
Submit Click to cancel this claim. This returns the claim record to [[DTC]] with a status of 
“Cancelled.” The contra party will no longer see this claim and it can no longer be 
acted upon.  
Reset Click to clear the [[participant]] Notes field. 
 
  

---

## Page 27

ClaimConnect™ Quick Guide 
Claim Approval 27 
CLAIM APPROVAL 
The ClaimConnect™ service provides you with the ability to require that claims above a certain dollar amount 
be subject to an approval process. You are able to establish this dollar amount using the Client Profile menu.   
Note: 
You cannot approve your own claim. 
Finding Claims Requiring Approval 
You can find claims that require approval in three ways: 
1. Check the lower right window of the Dashboard. The buttons on the bottom of the compartment control 
the information that is displayed here. Clicking the here link brings you to the Claim Approval page. 
 
2. Click Claims Pending Approval in the Claim Management menu. 
 


---

## Page 28

ClaimConnect™ Quick Guide 
Claim Approval 28 
3. You can receive an hourly message containing notifications of items requiring approval. 
 
4. From here, you must log in to ClaimConnect™ and access the items requiring approval using one of the 
above methods. 
  


---

## Page 29

ClaimConnect™ Quick Guide 
Claim Approval 29 
Approving or Rejecting Claims 
Once you are at the Claims Pending Approval page, you can: 
• Approve items individually. 
• Reject items individually. 
• Bulk-approve items. 
• Bulk-reject items. 
• Download an Excel spreadsheet containing all items on this screen. 
Click the appropriate checkbox(es) and click either the Approve or Reject button. 
 
Note:  
Click the link in the Action column to view each claim before you accept or reject it. 
  


---

## Page 30

ClaimConnect™ Quick Guide 
Claim Approval 30 
Approve/Reject Requirements and Scenarios 
Approvals are required for the following actions: 
Action Required? 
New Yes 
Affirm Yes 
Modify Yes 
DK No 
Un-DK No 
Cancel Yes 
 
The following scenarios represent ways in which the Claims Pending Approval screen is used. 
Type Scenario Actions 
1. Advisory A claim is submitted against me as an 
advisory that is debiting me money. 
I will have the ability to Affirm, DK, or 
submit my own claim as a debit to 
automatch. 
1. Affirm – If I affirm the claim, it will go to the pending 
approval process assuming that:  
a) My account is set up for debit approvals, and 
b) This amount of money is a debit that is over my 
minimum threshold on the approval admin screen. 
Once this claim is approved, the matching / validation 
process will be run and this claim will be moved to an 
“OPEN” state. 
2. DK – If I DK the advisory claim, there is no approval 
required and this claim will go back to the contra party in 
a “DKUC” state. 
3. UNDK – I DK a claim and then realize that I should not 
have DK’ed it. I click the Un-DK button.  
Instead of going through the Pending Approval process, 
matching and validation will re-occur. This returns that 
claim to either an “UNCP” or “OPEN” state.  
5. I submit my own claim based on receiving the advisory 
requesting (debit) monies from me.  
Once I submit the claim, no matching / validation occurs 
yet. Instead, this claim is sent to the pending approval 
process.  
After the claim is approved, matching / validation then 
occurs. This results in the claim going into an “OPEN” 
state if matched or an “UNCP” state if not matched. 
2. I Submit I am submitting a claim and I have the 
ability to modify and cancel that claim. 
1. I submit my own claim based on receiving the advisory 
requesting (debit) monies from me.  

---

## Page 31

ClaimConnect™ Quick Guide 
Claim Approval 31 
Type Scenario Actions 
Once I submit the claim, no matching / validation occurs 
yet. Instead, this claim is sent to the pending approval 
process.   
After the claim is approved, matching / validation then 
occurs. This results in the claim going into an “OPEN” 
state if matched or an “UNCP” state if not matched. 
2. I modify my claim. 
• If I modify the amount to be below the minimum for 
approval, then the claim does not need to go back for 
approval. 
• If I change any other information on the claim and the 
amount is still above the minimum threshold requiring 
approval, the claim needs to go back for approval. 
• If I increase the value of the cash amount being 
debited, the claim needs to go back for approval. 
3. I cancel my claim. If the claim is canceled, it does not 
need to go back to the Pending Approval process. 
3. Advisory 
Modification 
Prior to 
Approval 
• [[participant]] 2 submits a claim to 
[[participant]] 1. 
• The claim was approved by 
[[participant]] 2 and goes to [[participant]] 
1 as an advisory. 
• [[participant]] 1 has the ability to Affirm, 
DK or submit their own claim as 
defined in scenario 1.   
• While [[participant]] 1 is deciding on 
which action to take, [[participant]] 2 
determines that there is a 
modification needed on the claim and 
then makes that modification. 
• Because the modification requires 
approval, [[participant]] 1 does not know 
of the modification and either affirms 
the transaction or submits an 
identical transaction to automatch.   
Whether [[participant]] 1 affirms the transaction or submits an 
identical transaction to automatch, the claim is OPEN 
(matched) and will go to [[settlement]] on the agreed-upon 
date. 
When [[participant]] 2 attempts to approve or reject the claim, 
the changes will not be accepted and an error message 
informs the [[participant]] that the claim has already been 
matched. The user should refer to this claim’s transaction 
history for more details.  
This scenario also applies when [[participant]] 1 DKs the claim 
while [[participant]] 2 is waiting for their modification to be 
approved. When the claim is DK’ed, it moves into the DKUN 
state. When [[participant]] 2 goes to approve or reject the 
claim, they will receive an error message referring them to 
review the claim’s transaction history.   
4. Rejects 
Own Claim 
I am a submitter who rejects my own 
claim prior to approval. 
I submit a claim in which my firm will be debited monies 
requiring approval. Prior to the claim being approved by 
someone at my firm, I realize I need to change something 
on the claim. I access the Claims Pending Approval screen 
and I then reject my own claim so that I am able to make the 
necessary modification.  
Note:  
While I can reject my own claim, I am unable to approve my 
own claim. 
5. Multiple 
Modifications 
I make multiple modifications while my 
claim is awaiting approval or rejection. 
If I submit a modification to my claim that requires approval 
and then subsequently make a modification or multiple 
modifications to that claim while it is pending approval, those 

---

## Page 32

ClaimConnect™ Quick Guide 
Claim Approval 32 
Type Scenario Actions 
versions will also go to the pending approval / reject 
process. 
However, if the first modification is approved, all other 
versions submitted while that initial version was pending 
approval will not be able to be approved or rejected: since 
the initial version was approved, all subsequent 
modifications are made void. 
Any future modifications must be made using the original 
modified claim. 
6. [[settlement]] 
Date Equals 
Today 
I submit a debit transaction in which the 
Cash Claim [[settlement]] Date equals 
today. It is sent to the Claims Pending 
Approval page for someone to approve 
or reject it. 
The claim is not approved on the day 
that equals the Cash Claim [[settlement]] 
Date. 
You cannot approve or reject a claim on a day past the 
[[settlement]] Date. 
When an approver from your firm attempts to [[DO]] so, they 
receive an error message stating that the claim cannot be 
approved because the Cash Claim [[settlement]] Date needs 
to be greater than or equal to the current processing date. 
The error message directs the user to reject the claim and 
input a new one. 

---

## Page 33

ClaimConnect™ Quick Guide 
Client Profile 33 
CLIENT PROFILE 
 
Use the client profile menu to: 
• Add a contact type. This can include: 
o Adding someone to an internal email alert list for particular events (Distributions, Redemptions, or 
Reorganizations). This ensures that the correct people in your firm receive the correct event 
notifications. 
o An individual contact to be viewed by external clients using ClaimConnect™. 
o A group contact to be viewed by external clients using ClaimConnect™. This can be used for a 
department email that is internally sent to specific employees (for example, 
DTCCLearning@[[DTCC]].com) 
• Edit an existing contact. This can include: 
o Someone on an internal email alert list for particular events (Distributions, Redemptions, or 
Reorganizations). This ensures that the correct people receive event notifications. 
o An individual contact to be viewed by external clients using ClaimConnect™. 


---

## Page 34

ClaimConnect™ Quick Guide 
Client Profile 34 
o A group contact to be viewed by external clients using ClaimConnect™. This can be used for a 
department email that is internally sent to specific employees (for example, 
DTCCLearning@[[DTCC]].com) 
• View contact information for other clients using ClaimConnect™. 
• Establish your firm’s claim approval requirements. This can include: 
o Indicating whether or not your firm requires approval for debit transactions. 
o Setting the minimum amount for which that approval is required. 
Adding a Profile Entry 
To add any type of contact: 
1. Click Client Profile – Manage from the Client Profile menu. 
2. Click Add Contact on the Client Profile – Manage page. The Add Contact window appears. 
Adding to an Email Alert List 
You can add different employees in your company to an email list to receive alert messages when advisory 
claims against your firm are received for particular event types. These event types are: 
• Distributions, 
• Redemptions, and 
• Reorganizations. 
Messages will be sent at one of 6 points during the day if advisories have been received for that event type. 
To add someone from your firm to an e-mail list: 
1. Click Client Profile – Manage from the Client Profile menu. 
 
2. Click Add Contact on the Client Profile – Manage page. The Add Contact window appears. 
 
3. Select “Email Alert” from the Contact Type drop-down list. 
 
4. Select the event type from the Group Name drop-down list. 
 
5. Type an email address for the person receiving the alert. 
 
6. Optionally, type a phone number for the person receiving the alert. 
 
7. Click Submit to save this individual to the email alert list. Alternately, you can click Reset to clear the 
fields. 

---

## Page 35

ClaimConnect™ Quick Guide 
Client Profile 35 
Adding an Individual Contact 
You can designate a person at your organization as the primary contact to be listed in ClaimConnect™. This 
contact will be visible to other [[Member]] firms logged into the ClaimConnect™ application when they select 
Client Profile – View from the Client Profile menu. 
To add someone from your firm to an e-mail list: 
1. Click Client Profile – Manage from the Client Profile menu. 
 
2. Click Add Contact on the Client Profile – Manage page. The Add Contact window appears. 
 
3. Select Contact Details from the Contact Type drop-down list. 
 
4. Click Individual under Type. 
 
5. Type the First Name, Last Name, and Email address for your firm’s contact. Optionally, type the 
contact’s Phone number. 
 
6. Click Submit to save this individual as a contact for your firm. Alternately, you can click Reset to clear the 
fields. 
Adding a Group Contact 
This [[Option]] allows you to enter a general email address for a mailbox at your firm. This can be used for a 
department email that is internally sent to specific employees (for example, DTCCLearning@[[DTCC]].com). 
This mailbox needs to be established in advance of its use in ClaimConnect™. 
To add an email group to your profile: 
1. Click Client Profile – Manage from the Client Profile menu. 
 
2. Click Add Contact on the Client Profile – Manage page. The Add Contact window appears. 
 
3. Select Contact Details from the Contact Type drop-down list. 
 
4. Click Group under Type. 
 
5. Type a short descriptive name for the email group in the Group Name field. 
 
6. Type the group’s email address in the Email field. 
 
7. Optionally, type a phone number associated with the group at your firm. 
 
8. Click Submit to save this group contact to the Client Profile. Alternately, you can click Reset to clear the 
fields. 

---

## Page 36

ClaimConnect™ Quick Guide 
Client Profile 36 
Editing an Existing Profile Entry 
To edit any type of contact: 
1. Click Client Profile – Manage from the Client Profile menu. 
 
2. Click the Edit  icon for the item you want to edit. 
 
3. Edit the details for this contact. 
Note:  
You can only change each contact’s details. You cannot change the contact type. 
Deleting an Existing Profile Entry 
To delete any type of contact for your firm: 
1. Click Client Profile – Manage from the Client Profile menu. 
 
2. Click the Delete  icon for the item you want to delete. 
Viewing Contact Information 
To view contact for other ClaimConnect™ [[Member]] firms: 
1. Click Client Profile – View from the Client Profile menu. The full Client Profile list appears. 
 
2. To filter the list, type search information in the filter field and click the Filter button. 
 
3. To export the list to Excel, click the Export icon.  
Setting Approval Information 
To set approval information for ClaimConnect™, you must be set up by your SAC with a ClaimConnect™ 
External Update Access profile. 
Using the Approval page, you can: 
• Indicate whether your firm requires approval for debit claims. 
• Set the minimum approval amount for these debit claims. 
• View the audit trail for changes to these two items. 
 


---

## Page 37

ClaimConnect™ Quick Guide 
Client Profile 37 
To navigate to the Approval Admin page: 
1. Click Client Profile – Approval Admin from the Client Profile menu. 
 
 
To indicate that your firm requires approval for debit claims: 
1. Click Yes under the Account Approval Indicator heading. 
 
 
To set the approval threshold for your firm: 
1. Type the minimum dollar amount for a claim that requires approval in the Approval Threshold field. 
Note:  
The [[default]] minimum amount (once “Yes” is selected) that is required for approval is $0.01. 


---

## Page 38

ClaimConnect™ Quick Guide 
Client Profile 38 
2. Click Update. 
 
 
To view the history of changes made to the approval information: 
1. Check the Audit Log table beneath the Account Approval Indicator and Approval Threshold fields. 
 
 
To download the audit log: 
1. Click the Excel button  next to the filter field. 
 


---

## Page 39

ClaimConnect™ Quick Guide 
Viewing Reports 39 
VIEWING REPORTS 
 
Click Report Center to access this page. The Report Date field defaults to today’s date. 
To retrieve the latest report: 
1. Click Retrieve Latest. 
2. Click the Download icon.  
 
To find a report by date: 
1. Select a date using the Calendar tool. 
2. Click View Reports. 
3. Click the Download icon.  
 


---

## Page 40

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 