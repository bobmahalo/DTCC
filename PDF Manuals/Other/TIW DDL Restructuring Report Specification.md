---
title: "TIW DDL - Restructuring Reports Specification"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/TIW%20DDL%20Restructuring%20Report%20Specification.pdf"
pages: 9
size: "362.5 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# TIW DDL - Restructuring Reports Specification

**Original File:** [TIW DDL Restructuring Report Specification.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/TIW%20DDL%20Restructuring%20Report%20Specification.pdf)  
**Category:** Other  
**Total Pages:** 9  
**File Size:** 362.5 KB  

---

## Page 1

TIW Restructuring Reports 
1 
 
[[DTCC]] Public (White) 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
 
 
TIW DDL: 
RESTRUCTURING REPORTS 
 
SPECIFICATION DOCUMENT 
 
 

---

## Page 2

TIW Restructuring Reports 
Page 2 
    
 
[[DTCC]] Public (White) 
TRIGGERING STATUS REPORT 
Description 
The purpose of this report is to provide selected trade information on all transactions which are 
eligible for triggering under a restructuring event, and the status of the existing triggering activity, 
together with details of all triggering messages submitted on those transactions. 
Functionality 
The report will be automatically generated from the day the event master record is active up to and 
including the cash [[settlement]] date of that event. 
The report will display a complete list of transactions eligible for triggering for each Restructuring 
event 
Report Frequency 
M-F except New Year’s Day and Christmas Day. 
It generates every 2 hours in a day between “Trigger Period End Date” and “Movement Period End 
Date” Or until Event is closed (if there is no Movement date).  
16:00 EST 
15:00 EST 
13:00 EST 
11:00 EST 
10:00 EST 
09:00 EST 
08:00 EST 
07:00 EST 
06:00 EST 
05:00 EST 
04:00 EST 
03:00 EST 
02:00 EST 
Report Availability 
Report will be available in the DDL GUI Report download section. 
Last 7 Calendar Days’ reports are available. 
Note: For past report dates, only the last report of the day will remain available for download on later 
dates. 
Report Recipients 
[[participant]] Account Type (N). This is the account which is the party on the trade. Either Party or the 
Counterparty. 
Report Type 
External 
Autoroute [[ID]] 
02501681 
File Name 
Triggering Status Report 
Report Header 
This report contains one row of headers on the first line of the report 
Page Header 
The report is segmented for each Restructuring event and each segment will have a new header row. 
The headers may be filtered and/or sorted, allowing participants to see details for a particular event or 
date. 
 
 

---

## Page 3

TIW Restructuring Reports 
Page 3 
    
 
[[DTCC]] Public (White) 
Report Criteria: 
 
a) This report will pick up the transactions eligible for triggering from the warehouse for the ACTIVE 
Restructuring Event. 
 
b) All trades with the Position Status in 
 Certain 
 Uncertain 
 
C) Based on the Trigger / Movement of the trades, the report will show the associated details. 
 
Report field Description: 
Data Filed Description 
Event Name Event Name  
Event Type Code Event Type code -Restructuring or “Old Restructuring” 
[[participant]] [[ID]] Submitting [[participant]] [[ID]] 
Product Type Product type -CDS/CDT 
Reference Entity Name Reference Entity Name 
[[Buyer]] [[ID]] [[participant]] code/identifier for the [[Buyer]] 
[[Buyer]] Name [[Buyer]] Name 
[[Buyer]] TRI [[Buyer]] trade reference identifier  
[[Seller]] [[ID]] [[Seller]] External Identifier  
[[Seller]] Name [[Seller]] Name  
[[Seller]] TRI [[Seller]] trade reference identifier  
[[DTCC]] Reference Number [[DTCC]] TRI  
TIW Status 1.Certain 
2. Uncertain 
Calc-Flag Status Y/N 
Scheduled Termination Date Transaction scheduled termination date 
Tier Tier of the ISIN/RED [[ID]]  
Currency Currency of the transaction 
Current Notional Amount Current Notional Amount 
Untriggered Amount The notional which at the time of the report has not been applied to 
any triggering messages 
[[Buyer]] Triggered Amount The amount of notional triggered by any [[Buyer]] trigger messaging, as 
per the Triggering Position in the transaction history of the transaction 
[[Buyer]] Trigger Maturity Bucket 
[[Buyer]] Trigger Maturity Bucket based Event Bucket and Trade 
Schedule Termination date 
Blank if [[Buyer]] Triggered Amount is zero 
[[Seller]] Triggered Amount The amount of notional triggered by any [[Seller]] trigger messaging, as 
per the Triggering Position in the transaction history of the transaction 
[[Seller]] Trigger Maturity Bucket Blank if [[Seller]] Triggered Amount is zero 
Message Submitter [[ID]] [[DTCC]] [[ID]] of the party submitting each message 
Message Submitter Name Submitter [[participant]] name for each message 
Message Type CEN, NOTIFYCEN, MOVEMENT 
Message Processing Date Date of the message was SUBMITTED for Processing 
Message Processing Time Time of the message was Processing 
Triggering party 
For NOTIFYCEN the value in the Triggering Party field is Triggered 
party [[participant]] [[ID]]. 
For CEN and MOVEMENT “[[Seller]]” if the message submitter [[ID]] is 
[[Seller]] [[ID]], “[[Buyer]]” if the message submitter [[ID]] is [[Buyer]] [[ID]]. 
Triggering Amount As per the value in the Amount field of the message 
Message Status Rejected, Disabled, Applied, Unapplied or Partially Applied 
Current Maturity Bucket Current Maturity Bucket  
Clearing Agent Trade Reference [[ID]] #2 Clearing Agent Trade Reference [[ID]]#2 
 
 

---

## Page 4

TIW Restructuring Reports 
Page 4 
    
 
[[DTCC]] Public (White) 
TRIGGERING SUMMARY REPORT 
Description 
The purpose of this report is to provide summary information on triggering activity to the users. 
Functionality 
The report will be automatically generated once per day by the Warehouse, from the day the Maturity 
Bucket and Trigger/Movement period details are populated on the event master record, until and 
including the calendar day following the Trigger or Movement [[Option]] End Date. 
 If there is no movement window, the report will generate until the end of the Triggering Period. 
 If there is a movement window, the report will generate until the end of the Movement [[Option]] 
Window. 
The report will only contain the requesting user’s positions. 
Report Frequency 
M-F except New Year’s Day and Christmas Day. 
It generates every 2 hours in a day between “Trigger Period End Date” and “Movement Period End 
Date” Or until Event is closed (if there is no Movement date).  
16:00 EST 
15:00 EST 
13:00 EST 
11:00 EST 
10:00 EST 
09:00 EST 
08:00 EST 
07:00 EST 
06:00 EST 
05:00 EST 
04:00 EST 
03:00 EST 
02:00 EST 
Report Availability 
Report will be available in the DDL GUI Report download section. 
Last 7 Calendar Days’ reports are available. 
Note: For past report dates, only the last report of the day will remain available for download on later 
dates. 
Report Recipients 
[[participant]] Account Type (N). This is the account which is the party on the trade. Either Party or the 
Counterparty. 
Report Type 
External 
Autoroute [[ID]] 
02501675 
File Name 
Triggering Summary Report 
Report Header 
This report contains one row of headers on the first line of the report 
Report Structure 
The report has two sections: 
I. Summary data of daily and cumulative triggering volume by maturity bucket 
II. List of transactions triggered to each maturity bucket, with a separate section for each of the 
valid Maturity Buckets 
 

---

## Page 5

TIW Restructuring Reports 
Page 5 
    
 
[[DTCC]] Public (White) 
Report Criteria: 
a) The report has two sections: 
 
Section One: 
 Summary data of daily and cumulative triggering volume by maturity bucket 
 The report will count the number of eligible transactions triggered on triggering date by each 
maturity bucket for the ACTIVE Restructuring Event. 
 Count the Total number of transactions on triggering date for all maturity buckets. 
 If more than one ACTIVE Restructuring Events are available, then report will show the 
multiple entries in the section One for each restructuring event. 
 
 Section Two: 
 List of transactions triggered to each maturity bucket, with a separate section for each of the 
valid Maturity Buckets 
 Report will pick up the latest position and Trade details will be shown on the report for the 
triggered transaction counted for each maturity bucket in section One.  
 
b) All trades with the Position Status in 
 Certain 
 Uncertain 
Report field Description: 
 
Section One:  
 
Maturity 
Bucket 2.5Y 5Y 7.5Y Total 
Date (T+0) # triggered 
trades 
# triggered 
trades 
# triggered 
trades 
Total triggered trades in 
bucket 
Date (T+1) # triggered 
trades 
# triggered 
trades 
# triggered 
trades 
Total triggered trades in 
bucket 
Date (T+N) Trigger details will continue to be shown every day until Trigger Period End Date. 
Hereafter, Movement details will be shown until Movement Window End Date. 
 
 
Section Two: 
Section Title: Maturity Bucket 2.5YR (and so on for each Maturity Bucket) 
Data Field Description 
[[participant]] [[ID]] Submitting [[participant]] [[ID]] 
Product Type  Product type  
Tier Tier of the Trade  
Reference Entity Reference Entity Name 
[[Buyer]] [[ID]]  [[participant]] code/identifier for the [[Buyer]] 
[[Buyer]] Name [[Buyer]] Name 
[[Buyer]] TRI  [[Buyer]] trade reference identifier  
[[Seller]] [[ID]]  [[Seller]] External Identifier  
[[Seller]] Name  [[Seller]] Name  
[[Seller]] TRI  [[Seller]] trade reference identifier  
[[DTCC]] Reference Number [[DTCC]] TRI  
TIW Status 1. Certain 
2. Uncertain 
Calc-Flag Status Y/N 
Scheduled Termination Date Transaction scheduled termination date 
Currency Currency of the transaction 
Current Notional Amount Current Notional Amount 
Triggered Amount The triggered amount ([[Buyer]] or [[Seller]]) pertaining to that Maturity 
Bucket 

---

## Page 6

TIW Restructuring Reports 
Page 6 
    
 
[[DTCC]] Public (White) 
 
RS TRADE SPLIT REPORT 
Description 
This report provides the details of trade reference number before and after the spinoff process. 
The report provides the old and new reference details during the split process after end of trigger 
period and until movement period ends or the Event is closed. 
Report Frequency 
Report runs between “Trigger Period End Date” and “Movement Period End Date” Or until Event is 
closed.  
M-F except New Year’s Day and Christmas Day. 
The report will be generated on every day at 16:30 EST when there is active Restructuring Event. 
Report Availability 
Report will be available in the DDL GUI Report download section. 
Last 7 Calendar Days’ reports are available. 
Report Recipients 
[[participant]] Account Type (N). This is the account which is the party on the trade. Either Party or the 
Counterparty. 
Report Type 
External 
Autoroute [[ID]] 
02501801 
File Name 
RS Trade Split Report 
Report Criteria: 
 
a) Report runs between “Trigger Period End Date” and “Movement Period End Date” Or until 
Event is closed. 
 
b) The report will pick up below details of triggered transaction (Position Trigger Status is ‘CEP-
MOVEMENT’ or 'CEP-COMPLETE') after end of the triggering period for an ACTIVE 
Restructuring Event. 
 
Original Transaction details, it includes: 
 Original trade reference number of the party in the triggered transaction. 
 Original notional amount and Currency of the old trade that is triggered. 
 
New Transaction details, it includes:   
 New trade reference number of the party/counterparty who triggered the transaction. 
Note: If the new trade reference is not provided by the [[participant]], then the TIW will create a 
reference as per the rule. 
 New notional amount and Currency i.e., Triggered Amount by the party/counterparty 
 Split type: The old trade is marked as “[[Buyer]] Trigger” or “[[Seller]] Trigger” based on the 
priority rules of trigger message application 
 Maturity Bucket:  Maturity Bucket assigned for the spin-off trade reference. Available 
maturity buckets are 2.5Y, 5Y, 7.5Y,10Y, 12.5Y, 15Y, 20Y and 20+Y 
  

---

## Page 7

TIW Restructuring Reports 
Page 7 
    
 
[[DTCC]] Public (White) 
Report field Description: 
 
Data Filed  Description 
Triggered Trade Ref Original Trade Reference number of the party/counterparty 
who triggered the transaction.  
Original Notional Amount The Original notional amount on original trade before 
splitting.  
Original Notional Currency Original Notional Currency 
Clearing Agent Trade Reference [[ID]] #2 Clearing Agent Trade Reference [[ID]] #2 
Split Type [[Seller]] Triggered /[[Buyer]] Triggered / Untriggered 
New Trade Reference 
Split creates new trade with new trade reference of the 
party/counterparty who triggered the transaction that New 
Trade reference Number   
New Notional Amount The current notional amount of the new trade after splitting 
for the amount triggered by [[Buyer]] or [[Seller]].  
New Notional Currency New Notional Currency 
Maturity Bucket Maturity Bucket  
 
 
  

---

## Page 8

TIW Restructuring Reports 
Page 8 
    
 
[[DTCC]] Public (White) 
EXCEPTION REPORT RESTRUCTURING 
Description 
This report shows the trades that have failed in the Restructuring Event processing with the 
exception reason.  
Functionality 
This report will display the exceptional trades captured under the Restructuring event processing only 
(i.e., those unable to be processed successfully). 
Error Codes prefixed with "RS..." and "R0..." 
Report Frequency 
This report will be generated every day at 16.30 EST. 
Report Availability 
Report will be available in the DDL GUI Report download section. 
Last 7 Calendar Days’ reports are available. 
Report Recipients 
[[participant]] Account Type (N). This is the account which is the party on the trade. Either Party or the 
Counterparty. 
Report Type 
External 
Autoroute [[ID]] 
02501695 
File Name 
Exception report restructuring 
Report Criteria: 
a) This report will be produced whilst the Restructuring Event is ACTIVE. 
b) This report lists the exception reason for trades for which the event processing either was not 
attempted or failed for "ACTIVE" Restructuring Events.  
 The exception may occur at any stage of the Restructuring event processing 
 The possible exceptions are related to: 
o Any reason for which trade is Uncertain  
o Missing Information on the position which is required for Restructuring event 
processing  
 
TIW have also introduced extra column in the DDL report -Exception Code, which will show the 
exception error code that was produced during processing as shown below:  
 
Exception Reason Current Notional 
Amount Currency Clearing Agent 
TRI #2 
Exception 
Code 
Submission prior to 
Movement Period       RS12 
Trigger Not Found 
for the Position       RS05 
 
 
  

---

## Page 9

TIW Restructuring Reports 
Page 9 
    
 
[[DTCC]] Public (White) 
Report Field Description 
 
Data Filed  Description 
[[participant]] [[ID]] Submitting [[participant]] [[ID]] 
Product Type Product type  
[[participant]] TRI [[participant]] Trade reference Number  
Counterparty [[ID]] Counterparty [[ID]]  
Counterparty Name Counterparty account Name  
Counterparty TRI Counterparty Trade Reference Number  
[[DTCC]] TRI [[DTCC]] TRI 
Event Name Restructuring Event Name 
Processing Phase Processing Phase 
Exception Reason Exception Reason 
Current Notional Amount Current Notional Amount  
Currency Currency  
Clearing Agent TRI #2 Clearing Agent TRI 2 
Exception Code Exception code  
 
www.[[DTCC]].com 