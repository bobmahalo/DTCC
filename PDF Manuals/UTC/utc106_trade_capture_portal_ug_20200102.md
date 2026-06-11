---
title: "Trade Capture Portal User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc106_trade_capture_portal_ug_20200102.pdf"
pages: 15
size: "1492.5 KB"
category: "UTC"
ingested_on: "2026-06-05"
---

# Trade Capture Portal User Guide

**Original File:** [utc106_trade_capture_portal_ug_20200102.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc106_trade_capture_portal_ug_20200102.pdf)  
**Category:** UTC  
**Total Pages:** 15  
**File Size:** 1492.5 KB  

---

## Page 1

 
 
UNIVERSAL TRADE CAPTURE (UTC) 
TRADE CAPTURE PORTAL USER GUIDE 
VERSION 1.2 
JANUARY 2, 2020 
 


---

## Page 2

 
 
© 2020 The Depository Trust & Clearing Corporation. All rights reserved.   
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Info: January 2, 2020 
Publication Code: UTC106 
Service: Universal Trade Capture 
Title: Trade Capture Portal User Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
Contacts .............................................................................................................................................................. 4 
Features .............................................................................................................................................................. 4 
Logging In ........................................................................................................................................................... 4 
Universal Trade Capture Summary .................................................................................................................... 7 
Unsubmitted Group Actions ................................................................................................................................ 8 
Adding Transaction ........................................................................................................................................... 8 
Discarding Groups ........................................................................................................................................... 10 
Submitting Groups ........................................................................................................................................... 11 
Transactions Actions ........................................................................................................................................ 11 
Viewing Transactions Within a Group ............................................................................................................. 11 
Transaction Fields ........................................................................................................................................... 12 
Viewing a Single UTC Transaction ................................................................................................................. 12 
Updating a Single UTC Transaction ................................................................................................................ 13 
Discarding a Single UTC Transaction ............................................................................................................. 14 
 

---

## Page 4

Trade Capture Portal User Guide 
Introduction 4 
INTRODUCTION 
Universal Trade Capture (UTC) is the primary vehicle for markets and clearing firms to submit transactions to 
[[NSCC]] for clearance processing. UTC offers messaging input to support most transactions, which is required to 
meet [[NSCC]] real-time submission requirements. 
To supplement the real-time interface, [[NSCC]] offers correspondent clearing transaction entry through the 
[[DTCC]] Portal. Customers use correspondent clearing Portal entry primarily for exception processing that 
cannot be performed through standard methods. 
Contacts 
Use the following [[NSCC]] contacts for information about UTC: 
• For general questions or MRO setup, contact [[NSCC]] Support at NSCCSupport@[[DTCC]].com. 
• For business inquiries, contact the [[NSCC]] Integration Team at NSCCIntegrationTeam@[[DTCC]].com. 
You can also contact your [[DTCC]] Relationship Manager. 
Features 
The Universal Trade Capture (UTC) application enables you to perform the following functions: 
• Add Transactions 
• View Transactions 
• Update Transactions 
• Discard Transactions 
• Cancel Groups 
• Submit Groups 
Logging In 
A valid user [[ID]] and password are required for entry to the [[DTCC]] Portal. If you [[DO]] not already have a user [[ID]], 
contact your firm’s Super Access Coordinator and request the inquiry and submit [[Entitlement]]. The [[DTCC]] Portal 
can be accessed through https://portal.[[DTCC]].com. If you need access to a product not listed in your portal, click 
the Need Access to Another Product? A list of your firm’s super access coordinators for each product 
appears.  
  


---

## Page 5

Trade Capture Portal User Guide 
Introduction 5 
To access the application, your super access coordinator must provide you with two entitlements: CLD and 
UTC. CLD enables access to the Clearing Dashboard, which contains the various [[Equity]] clearing applications. 
UTC entitles you to begin using the UTC application. The following table shows the available applications-
specific entitlements: 
Access Description Glossary Definition 
UTC Transaction Inquiry Enables you to view current and 
previously submitted transactions. 
Access the UTC Web application and 
view current and previously submitted 
UTC transactions. You cannot add or 
submit transactions. 
UTC Transaction Enter Provides you with the ability to enter 
transactions. You must have INQUIRY 
access as a prerequisite. 
Enter and discard transactions in the 
UTC Web application. You must have 
INQUIRY access as a prerequisite. 
You [[DO]] not have the ability to submit 
transactions. 
UTC Transaction Submit Allows you to submit groups of 
transactions for the [[participant]]'s 
accounts. You must have INQUIRY 
access as a prerequisite. 
Submit and discard groups of 
transactions for [[participant]]'s accounts. 
You must have INQUIRY access as a 
prerequisite. You [[DO]] not require 
access to ENTER, but without this 
access you can only submit and 
discard groups. 
 
To log in to the Trade Capture Portal: 
1. Navigate to the [[DTCC]] Portal log in page available at https://portal.[[DTCC]].com/C. The following figure shows 
the Login page: 
 


---

## Page 6

Trade Capture Portal User Guide 
Introduction 6 
2. Type your [[DTCC]] portal log in credentials. After logging into the portal, the [[Equity]] Clearing Dashboard 
displays. When selected, the common landing page, as shown in the following figure, appears. 
 
3. Select the  UTC icon  
The UTC Web application launches the application in a new window. 


---

## Page 7

Trade Capture Portal User Guide 
Universal Trade Capture Summary 7 
UNIVERSAL TRADE CAPTURE SUMMARY 
UTC submissions are structured as transactions and groups. A transaction is the individual clearance entry 
between two entities. One or many transactions are contained within a group, which is the primary item that is 
submitted for processing. Per [[participant]] account, only one group can be unsubmitted at a time. 
The Summary page is the UTC home page. You only have access to [[participant]] accounts associated with your 
login [[ID]], and you can only view one account at a time.  
Upon login, if unsubmitted and previously submitted groups exist, the Summary page, as shown in the 
following figure displays. You can only see groups for accounts associated with your login [[ID]]. 
 
The following table shows the fields available in the Summary page: 
Name Description 
Group [[ID]] Group [[ID]] for a submitted group. 
Submission Date/Time Submission date and time of the submitted group in DD/MM/YYYY hh:mm format. 
Creation Date/Time Date and time of the first transaction added in the group in DD/MM/YYYY hh:mm 
format. 
[[participant]] [[participant]] [[ID]] associated with the group. 
Create User [[ID]] User [[ID]] of the user who created the first transaction in the group. 
Submit [[ID]] User [[ID]] of the user who submitted the group. 
Entered 
Transactions/Submitted 
Number of transaction submitted in the group, regardless of the status. 


---

## Page 8

Trade Capture Portal User Guide 
Universal Trade Capture Summary 8 
Name Description 
Status Status of the group. There can be only one Unsubmitted Group per [[participant]]. 
Search Search and filter data across all the rows. By typing in the box, any row with the 
data entered that matches the criteria will be displayed. 
Unsubmitted Group Actions 
You can perform the following actions for each group from the Summary page: 
• View Transactions–From the Transaction page, view the transactions involved in the selected Group. The 
action is initiated by clicking on the Group [[ID]] link. 
The Action column contains the list of available actions that you can take on the selected Group. 
•  Add Transactions–From the Add Transaction page, add new transactions. 
•  Discard Group–Confirm the action when prompted. This action removes all transactions in the group 
and marks the group discarded. 
•  Submit Group–This action submits the entire group. 
Adding Transaction 
To add another transaction to the group, click  Add Transaction. The Add Transaction page that displays 
allows you to add a transaction to an existing group. The page is broken up into the following sections to help 
you manage the large number of fields. 
• [[Buyer]] 
• [[Seller]] 
• Trade 


---

## Page 9

Trade Capture Portal User Guide 
Universal Trade Capture Summary 9 
The following figure shows the [[Buyer]] section of the Add Transaction page: 
 
The following figure shows the [[Seller]] section of the Add Transaction page: 
 


---

## Page 10

Trade Capture Portal User Guide 
Universal Trade Capture Summary 10 
The following figure shows the Trade section of the Add Transaction page: 
 
After completing all mandatory fields, click the Add Transaction link or select from the Action Menu in the 
summary page to add a transaction to the existing group. After populating the form and clicking Add 
Transaction, a Success or Error message displays. If successful, the new transaction is added. 
If adding a transaction failed for any reason, the Add Transaction page appears again with an error message 
and all fields prepopulated with your prior input. You can edit the fields, and then submit the transaction again. 
Upon successful submission, the page clears all data entry elements, and you can add another transaction. 
To return to the Summary page without saving any changes, Click Cancel. 
Discarding Groups 
To discard a group, click  Discard Group. Confirm the action by clicking OK. All unsubmitted transactions 
are discarded, and the group is set to discard. This group no longer exist. 
To return to the Transaction page without discarding any groups, Click Cancel. 


---

## Page 11

Trade Capture Portal User Guide 
Universal Trade Capture Summary 11 
Submitting Groups 
To submit a group, click  Submit Group. Confirm the action by clicking OK. Upon clicking OK the group is 
added to the database. The transactions page displays a success message. 
To return to the Transaction page without discarding any groups, Click Cancel. 
Transactions Actions 
There are two actions you can take on individual transactions within Groups that have not been submitted.  
•  Update Transaction allows you to update the transaction. 
•  Discard Transaction enables you to discard the transaction from the group. 
Viewing Transactions Within a Group 
The Transactions page displays a summary of all the transactions currently associated with the group. From 
this page, you can view, add, update, discard, and upload transactions. To view transactions, click the Group 
[[ID]] link for the group that you want to view. For both Submitted and Expired groups, you can view only 
transactions.  


---

## Page 12

Trade Capture Portal User Guide 
Universal Trade Capture Summary 12 
You can navigate to the Transactions page, shown in the following figure, by selecting View Transactions for 
any group from the Summary page. 
 
Transaction Fields 
For more information about the fields, values, and definitions, see the UTC layout and UTC specification 
documents available from the UTC Input/Output Message Formats section of the [[DTCC]] Learning Center.  
Viewing a Single UTC Transaction  
The View Transaction page, shown in the following figure, displays the details of an UTC transaction already 
entered, with each input field as read-only. Click the hyperlinked transaction [[ID]] to make these details appear.  
To return to the Summary page without saving any changes, Click Cancel. 


---

## Page 13

Trade Capture Portal User Guide 
Universal Trade Capture Summary 13 
The following figure shows the View Transaction page for a single UTC transaction: 
 
Updating a Single UTC Transaction  
Use the Update Transaction page to update a single UTC transaction within an unsubmitted group. You can 
access the Update Transaction page, shown in the following figure, by selecting  Update Transactions 
from a transaction. All fields are text input fields except Market, which is a selection drop down. All fields are 
editable and prepopulated with the transaction details.  
Click Update to update the transaction with a success message if it submitted or an error message if your 
update fails to submit.  
To return to the Summary page without saving any changes, click Cancel. 
 
  


---

## Page 14

Trade Capture Portal User Guide 
Universal Trade Capture Summary 14 
Discarding a Single UTC Transaction 
To discard a single UTC transaction, click  Discard from any transaction row. Confirm the action by clicking 
OK. The transaction is removed from the current unsubmitted group. 
To return to the Transaction page without discarding any transaction, Click Cancel. 
 


---

## Page 15

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 