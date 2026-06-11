---
title: "Standardized Data Reporting Technical Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_sdr_techguide_mfs165_20220408.pdf"
pages: 67
size: "835.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Standardized Data Reporting Technical Guide

**Original File:** [net_sdr_techguide_mfs165_20220408.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_sdr_techguide_mfs165_20220408.pdf)  
**Category:** Other  
**Total Pages:** 67  
**File Size:** 835.9 KB  

---

## Page 1

 
 
 
 
NETWORKING 
STANDARDIZED DATA REPORTING TECHNICAL GUIDE 
APRIL 8, 2022 
 


---

## Page 2

 
 
Copyright© © 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. 
TOGETHER, and the Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing 
Corporation. 
 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The 
Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these 
affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in 
which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the 
services they offer. 
By accessing this document, you acknowledge, accept and agree to the foregoing [[obligations]] and restrictions. 
 
Doc Info: April 8, 2022 
Publication Code: MFS165 
Service: Networking 
Title: Standardized Data Reporting Technical Guide 
 
 
 
 
  

---

## Page 3

 
 
REVISION HISTORY 
Date  Updates 
April 8, 2022 Learning upgrade caused some link(s) to break.  Links have been corrected. 
01/08/2021 Updated Saturday’s last cycle output time to 2:00pm (p.42) to align with revised 
processing schedule (Important Notice a8905) 
Nov. 11, 2019 Reference links corrected. 
July 5, 2011 Updated to coordinate with SDR changes effective October 2011 
May 3, 2007 Updated for Insurance Company Processing and other modifications. 
June 9, 2006 Added “Select Validation Rules” 
Added additional values to Partial Responses indicator and Transaction Type 
August 7, 2006 Please see Important Notice # A6213 P&S# 5783,  
Dated March 8, 2006, Effective Date August 7, 2006 
 
 
 
 

---

## Page 4

 
 
TABLE OF CONTENTS  
Overview ............................................................................................................................................................... 8 
Record Layouts ................................................................................................................................................... 8 
Sample Scenarios ................................................................................................................................................ 9 
Sample Scenarios Overview ............................................................................................................................... 9 
Request on a Super Omnibus Account .............................................................................................................. 9 
SDR Request Record (F 20) ............................................................................................................................. 9 
SDR Request Record (F 20) ...........................................................................................................................10 
Request on a Super Omnibus Account-Acknowledgement Response ............................................................11 
Acknowledgment Response ............................................................................................................................11 
SDR Header (B/U 21) ....................................................................................................................................11 
SDR Acknowledgment (B/U 22) ....................................................................................................................12 
Request on a Super Omnibus Account-Summary Response Records ............................................................13 
Summary Response Records .........................................................................................................................13 
SDR Header (B/U 21) ....................................................................................................................................13 
SDR Summary (B/U 25) (Plan 1) ...................................................................................................................14 
SDR Summary (B/U 25) (Plan 2) ...................................................................................................................16 
SDR Trailer (B/U 27) ......................................................................................................................................17 
Request on a Plan ............................................................................................................................................18 
SDR Request Record (F 20) ...........................................................................................................................19 
Request on a Plan-Response Records ............................................................................................................20 
Response Records ..........................................................................................................................................20 
SDR Header (B/U 21) ....................................................................................................................................20 
SDR Detail (B/U 24) #1 ..................................................................................................................................21 
SDR Detail (B/U 24) #2 ..................................................................................................................................21 
SDR Detail (B/U 24) #3 ..................................................................................................................................22 
SDR Trailer (B/U 27) ......................................................................................................................................23 
Request on an [[investor]] Omnibus Account .......................................................................................................23 
SDR Request Record (F 20) ...........................................................................................................................23 

---

## Page 5

 
 
SDR Header (B/U 21) ......................................................................................................................................24 
SDR Detail (B/U 24) #1 ...................................................................................................................................24 
SDR Detail (B/U 24) #2 ...................................................................................................................................25 
SDR Detail (B/U 24) #3 ...................................................................................................................................26 
SDR Detail (B/U 24) #4 ...................................................................................................................................26 
SDR Detail (B/U 24) #5 ...................................................................................................................................27 
SDR Detail (B/U 24) #6 ...................................................................................................................................27 
SDR Trailer (B/U 27) .......................................................................................................................................28 
Rep Level Data # 1 ...........................................................................................................................................29 
SDR Request Record (F 20) ...........................................................................................................................29 
Rep Level Data # 1-Response Records ...........................................................................................................30 
SDR Header (B/U 21) ......................................................................................................................................30 
SDR Detail (B/U 24) #1 ...................................................................................................................................30 
SDR Detail (B/U 24) #2 ...................................................................................................................................31 
SDR Trailer (B/U 27) .......................................................................................................................................31 
Stop Recurring Request ...................................................................................................................................32 
SDR Request Record (F 20) ...........................................................................................................................32 
Rep Level Data # 2 ...........................................................................................................................................33 
SDR Request Record (F 20) ...........................................................................................................................33 
Rep Level Data # 2-Response Records ...........................................................................................................33 
SDR Header (B/U 21) ......................................................................................................................................33 
SDR Detail (B/U 24) #1 ...................................................................................................................................34 
SDR Detail .......................................................................................................................................................35 
(B/U 24) #2 ......................................................................................................................................................35 
SDR Trailer (B/U 27) .......................................................................................................................................35 
Other Scenarios ................................................................................................................................................36 
Business Processing ......................................................................................................................................... 40 
Inquiry Request Data ........................................................................................................................................40 
Data Request Types ........................................................................................................................................40 
Acknowledgement, [[NSCC]] Reject and Firm Reject Data ..................................................................................41 

---

## Page 6

 
 
Acknowledgment Data ....................................................................................................................................41 
[[NSCC]] Reject Data ..........................................................................................................................................41 
Firm Reject Data .............................................................................................................................................41 
Response Data .................................................................................................................................................42 
[[NSCC]] Reminders .............................................................................................................................................42 
System Processing ............................................................................................................................................ 43 
System Interface and Datatrak & Autoroute Schedule .....................................................................................43 
Systems Interface ............................................................................................................................................43 
Datatrak and Autoroute Schedule ...................................................................................................................43 
Processing Flow ................................................................................................................................................43 
Process Flow using ftp (batch) on data request input/output and response input/output.  ..............................44 
Process flow over HTTPS using [[DTCC]] WebDirect ........................................................................................45 
List of SDR File Record Types .........................................................................................................................45 
SDR Request Data File Structure .....................................................................................................................46 
Record Structure for Request Record (Input) .................................................................................................46 
Record Structure for Request (Output to Firm) ...............................................................................................46 
Record Structure for Request (Output to Fund) ..............................................................................................47 
SDR Response Data File Structure ..................................................................................................................47 
Record Structure for SDR Response Input Data file ........................................................................................47 
Record Structure for Detail Information Only (Input) .......................................................................................48 
Record Structure for Summary Information Only (Input) ................................................................................48 
Record Structure for Both Detail and Summary Information (Input) ...............................................................48 
Record Structure for a Variety of Responses (Input) ........................................................................................49 
Record Structure for a Variety of Responses (Output to Fund) .......................................................................51 
Record Structure for a Variety of Responses (Output to Firm) ........................................................................52 
[[NSCC]] Data and File Sorting .............................................................................................................................54 
Guidelines for User Search Criteria and Data Sorting ....................................................................................54 
Field Definitions ................................................................................................................................................55 
SDR Inquiry Request Data (Sent by Funds to Firms) .....................................................................................55 
SDR Acknowledgment Data ............................................................................................................................59 

---

## Page 7

 
 
SDR Response Data (Sent by Firms to Funds) ..............................................................................................59 
Reject Codes and Validation Rules ..................................................................................................................64 
Reject Codes ...................................................................................................................................................64 
Select Validation Rules ...................................................................................................................................64 
Control Number and Reminder Process ........................................................................................................64 
Fund, Firm, and Underlying Firm ...................................................................................................................65 
Header and Trailer .........................................................................................................................................65 
Records between Header and Trailer ............................................................................................................65 
 

---

## Page 8

Standardized Data Reporting Technical Guide 
Overview 8 
OVERVIEW 
The Investment Company Institute's Standardized Data Reporting Working Group created the design for a 
standard, automated facility for funds to request and receive shareholder trading information from 
intermediaries through [[NSCC]]. This solution is referenced as SDR throughout this document. SDR is designed 
to provide the funds with a robust mechanism to request data from intermediaries as their compliance and 
monitoring programs warrant. The mechanism allows for varying functionality such as data requests at a 
summary level (plan/omnibus account level data) or detail level ([[participant]]/shareholder level data), data 
requests for a specific date or a period of time, and for data requests submitted on a regular or periodic basis. 
This Guide includes examples of data request and response scenarios, providing samples of data records and 
fields used in the process. It also provides field definitions and syntax that govern the structure and forma t of 
the files. 
For best practices on various issues identified by the Investment Company Institute's Best Practices Taskforce, 
please reference the  Standardized Data Reporting Best Practices guide within the [[DTCC]] Learning Center.   
Items covered in the "Best Practices" guide include: 
• Best Practices 
• Naming Conventions and Terminology 
• Working Assumptions 
Record Layouts 
The Standardized Data Reporting records are available under Networking tab of the Record Layouts section on 
[[DTCC]]’s Learning Center at https://dtcclearning.com/products-and-services/mutual-fund-services/record-
layouts.html 
 
 

---

## Page 9

Standardized Data Reporting Technical Guide 
Sample Scenarios 9 
SAMPLE SCENARIOS 
Sample Scenarios Overview 
In this section are examples of SDR records for common scenarios. The examples  are not intended to be a 
comprehensive list and may be updated as appropriate. Funds and Firms are encouraged to initiate a dialogue 
to discuss scenarios that are common to their respective business models but are not illustrated below.  
Please refer to the SDR Record Layouts for data field positions and syntax requirements. The 
layouts are available at https://dtcclearning.com/products-and-services/mutual-fund-
services/record-layouts.html 
Request on a Super Omnibus Account 
• Super Omnibus Request and Response (2 plans) 
• Summary Level – The fund provides the fund account number or the firm account number. Both account 
numbers may also be provided to provide the firm with additional information to identify the account. The 
Firm determines that the fund account is a super omnibus account and provides only summary data.  
• 1 Day 
SDR Request Record (F 20) 
Record 1 of 2 
Field Name Description 
Originator Type F = Fund 
Record Type 20 = SDR Request 
Sequence Number 01 
SDR Control Number 564350580000001 
SDR Request Type 01 = Fund Account level 
This request type is used when a Plan [[ID]] or [[investor]] Omnibus Account Number is 
not specified. 
Only the high-level account identifiers are provided. (i.e., fund account number 
and/or firm account number) 
Firm Number 0675 
In this example, there is an "underlying firm," which indicates that the firm is a 
service provider acting on behalf of another firm. 
Underlying Firm 0004 
This is the firm that is using a service provider to support the SDR functionality. 
Underlying Firm Indicator 03 = UFS Number 

---

## Page 10

Standardized Data Reporting Technical Guide 
Sample Scenarios 10 
Field Name Description 
Fund Number 5643 
Fund Account Number CA1000231 
Either the fund account number or firm account number is provided. In this 
example, both are provided. 
Firm Account Number 13454637 
Either the fund account number or firm account number is provided. In this 
example, both are provided. 
From Date 02282005 
Must be the current date, or a valid historical date. 
Security Issue [[ID]] 261465763 
Plan [[ID]]/[[investor]] Omnibus 
Account Number 
 
Omnibus Account Indicator  
SSN/TIN  
Filler  
[[NSCC]] Reject Indicator  
Filler / Reject Code 1  
Filler / Reject Code 2  
Filler / Reject Code 3  
Filler / Reject Code 4  
SDR Request Record (F 20) 
Record 2 of 2 
Field Name Description 
Originator Type F = Fund 
Record Type 20 = SDR Request 
Sequence Number 02 
Recurring Indicator 02282005 
This date is optional for current date or recurring requests. It should be provided 
for historical requests or requests with a date range. This example optionally 
provides the date for a single current day request.  
To Date  
Includes Category 2 
Transactions? 
 

---

## Page 11

Standardized Data Reporting Technical Guide 
Sample Scenarios 11 
Field Name Description 
RR Number  
RR Branch  
RR Firm  
Original SDR Control Number  
Threshold Amount  
Transaction Type  
Fund/SERV
® Control Number  
Filler  
 
Request on a Super Omnibus Account-Acknowledgement Response 
Acknowledgment Response 
SDR Header (B/U 21) 
Record 1 of 1 
Field Name Description 
Originator Type B = Firm 
Record Type 21 = SDR Header 
Sequence Number 01 
SDR Control Number 564350580000001 
SDR Response Number 067550580000001 
Response Type 04 = Acknowledgment 
Partial Response Indicator 0 = Full 
Acknowledgments are always Full. 
Firm Number 0675 
Underlying Firm 0004 
The firm should echo back information provided by the fund. 
Underlying Firm Indicator 03 = UFS Number 
Fund Number 5643 
Fund Account Number CA1000231 
Firm Account Number 13454637 

---

## Page 12

Standardized Data Reporting Technical Guide 
Sample Scenarios 12 
Field Name Description 
Security Issue [[ID]] 261465763 
Response Type • 01 = Summary Level 
• 02 = Detail Level 
• 03 = Both Summary and Detail 
• 04 = Acknowledgment 
• 05 = Firm Reject 
Correction Indicator  
Fund/SERV® Control Number  
Filler  
[[NSCC]] Reject indicator  
Filler / Reject Code 1  
Filler / Reject Code 2  
Filler / Reject Code 3  
Filler / Reject Code 4  
SDR Acknowledgment (B/U 22) 
• Input From Firm To [[NSCC]] 
• Output From [[NSCC]] To Fund 
• Record 1 of 1 (Required) 
 
This Acknowledgment record is submitted within the Header and Trailer. The Acknowledgment is the 
first response from the Firm to the Fund for a specific SDR Request. 
(Trailer record is required but not shown in example.) 
[[NSCC]] WILL NOT validate the proper sequence for submitting the Acknowledgment and SDR Detail 
Response records. 
Field Name Description 
Originator Type B = Firm 
Record Type 22 = SDR Acknowledgment 
Sequence Number 01 
Acknowledgment Indicator 0 = Response is Provided 
Firm is acknowledging and will provide a response. 
Anticipate Response Date 03312005 
Date by which the firm is expected to provide a response. 

---

## Page 13

Standardized Data Reporting Technical Guide 
Sample Scenarios 13 
Field Name Description 
Anticipated Response File 
Frequency 
0 = Full File 
Firm is anticipating sending a full file. 
Underlying Firm This field on the Header is used only on Summary records to specify the underlying 
firm on a plan or [[investor]] omnibus account. 
Underlying Firm Indicator  
Filler  
[[NSCC]] Reject Indicator Input: Space Output: 
• 0 = Accepted by [[NSCC]] 
• 1 = Rejected by [[NSCC]] 
Filler / Reject Code 1 Input: Space 
Output: Reject Code 
Filler / Reject Code 2 Input: Space 
Output: Reject Code 
Filler / Reject Code 3 Input: Space 
Output: Reject Code 
Filler / Reject Code 4 Input: Space 
Output: Reject Code 
Request on a Super Omnibus Account-Summary Response Records 
Summary Response Records 
SDR Header (B/U 21) 
Record 1 of 1 
Field Name Description 
Originator Type B = Firm 
Record Type 21 = SDR Header 
Sequence Number 01 
SDR Control Number 564350580000001 
SDR Response Number 067550590000001 
Response Type 01 = Summary Level 
The firm determines that the account is a super omnibus account and submits a 
"Summary Level" response type. 
Partial Response Indicator 0 = Full/Final Response 

---

## Page 14

Standardized Data Reporting Technical Guide 
Sample Scenarios 14 
Field Name Description 
In this example, the response contains all requested data in one file. This response 
is marked as a full/final response 
Firm Number 0675 
Underlying Firm 0004 
The firm should echo back information provided by the fund. 
Underlying Firm Indicator 03 = UFS Number 
Fund Number 5643 
Fund Account Number CA1000231 
Firm Account Number 13454637 
Security Issue [[ID]] 261465763 
Correction Indicator  
Fund/SERV® Control Number  
Filler  
[[NSCC]] Reject Indicator  
Filler / Reject Code 1  
Filler / Reject Code 2  
Filler / Reject Code 3  
Filler / Reject Code 4  
SDR Summary (B/U 25) (Plan 1) 
Record 1 of 1 
Field Name Description 
Originator Type B = Firm 
Record Type 25 = SDR Summary 
25 = SDR Summary 01 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
PLAN014354321 
The firm identifies all plans and [[investor]] omnibus accounts in the super omnibus 
account and provides summary data. 
This is the first plan identified in the super omnibus account. 
Omnibus Account Indicator 0 = Plan [[ID]] 
Indicates that the account above is a plan. 
NAV Date 02282005 

---

## Page 15

Standardized Data Reporting Technical Guide 
Sample Scenarios 15 
Field Name Description 
Dollar Value of All [[participant]]/ 
Shareholder Buys 
 
Dollar Value of All [[participant]]/ 
Shareholder Sells 
 
Dollar Value of Category 1 
[[participant]]/ Shareholder Buys 
10000000 (i.e., $100,000.00) 
Dollar Value of Category 1 
[[participant]]/ Shareholder Sells 
45000000 (i.e., $450,000.00) 
Number of Category 1 [[participant]]/ 
Shareholder Buys 
00000004 (i.e., 4 buys on this particular day within this plan) 
Number of Category 1 [[participant]]/ 
Shareholder Sells 
00000003 (i.e., 3 sells on this particular day within this plan) 
Underlying Firm This number is not necessary since it is provided on the request and 
returned on the Header. 
Underlying Firm Indicator  
Social Code 12 = 401k (non-prototype) 
Filler  
[[NSCC]] Reject Indicator Input: Space Output: 
• 0 = Accepted by [[NSCC]] 
• 1 = Rejected by [[NSCC]] 
Filler / Reject Code 1 Input: Space 
Output: Reject Code 
Filler / Reject Code 2 Input: Space 
Output: Reject Code 
Filler / Reject Code 3 Input: Space 
Output: Reject Code 
Filler / Reject Code 4 Input: Space 
Output: Reject Code 
 
  

---

## Page 16

Standardized Data Reporting Technical Guide 
Sample Scenarios 16 
SDR Summary (B/U 25) (Plan 2) 
Record 1 of 1 
Field Name Description 
Originator Type B = Firm 
Record Type 25 = SDR Summary 
Sequence Number 01 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
PLAN0574532 
This is the second plan identified in the super omnibus account. 
Omnibus Account Indicator 0 = Plan [[ID]] 
NAV Date 02282005 
Dollar Value of All [[participant]]/ 
Shareholder Buys 
 
Dollar Value of All [[participant]]/ 
Shareholder Sells 
 
Dollar Value of Category 1 
[[participant]]/ Shareholder Buys 
4500000 (i.e., $45,000.00) 
Dollar Value of Category 1 
[[participant]]/ Shareholder Sells 
1500000 (i.e., $15,000.00) 
Number of Category 1 [[participant]]/ 
Shareholder Buys 
00000001 
Number of Category 1 [[participant]]/ 
Shareholder Sells 
00000001 
Underlying Firm This number is not necessary since it is provided on the request and 
returned on the Header. 
Underlying Firm Indicator  
Social Code 12 = 401k (non-prototype) 
Filler  
[[NSCC]] Reject Indicator Input: Space Output: 
• 0 = Accepted by [[NSCC]] 
• 1 = Rejected by [[NSCC]] 
Filler / Reject Code 1 Input: Space 
Output: Reject Code 
Filler / Reject Code 2 Input: Space 
Output: Reject Code 
Filler / Reject Code 3 Input: Space 
Output: Reject Code 

---

## Page 17

Standardized Data Reporting Technical Guide 
Sample Scenarios 17 
Field Name Description 
Filler / Reject Code 4 Input: Space 
Output: Reject Code 
SDR Trailer (B/U 27) 
Record 1 of 1 
Field Name Description 
Originator Type B = Firm 
Record Type 27 = SDR Trailer 
Sequence Number 01 
SDR Control Number 564350580000001 
SDR Response Number 067550590000001 
Firm Number 0675 
Fund Number 5643 
Security Issue [[ID]] 261465763 
Total Acknowledgment Items 
within this Group 
000000000 
Total Reject Items within this 
Group 
000000000 
Total Detail Items within this 
Group 
000000000 (Total number of record type 24, sequence 01.) 
Total Summary Items within this 
Group 
000000002 (Total number of record type 25, sequence 01.) 
Total Records within this Group 000000004 (Total number of physical records including headers and trailers.) 
Total [[NSCC]] Accepted Input – 
Acknowledgment Items 
Input: Space 
Output: Total number of [[NSCC]] accepted record type 22 with sequence 01. Zeroes 
allowed. 
Total [[NSCC]] Accepted Input –
Reject Items 
Input: Space 
Output: Total number of [[NSCC]] accepted record type 23 with sequence 01. Zeroes 
allowed. 
Total [[NSCC]] Accepted Input – 
Detail Items 
999,999,999 
Input: Space 
Output: Total number of [[NSCC]]-accepted record type 24 with sequence 01. Zeroes 
allowed 
Total [[NSCC]] Accepted Input –
Summary Items 
999,999,999 
Input: Space Output: Total number of [[NSCC]]-accepted record type 25 with 
sequence 01. Zeroes allowed. 

---

## Page 18

Standardized Data Reporting Technical Guide 
Sample Scenarios 18 
Field Name Description 
Total [[NSCC]] Rejected Input –
Acknowledgment Items 
Input: Space 
Output: Total number of [[NSCC]] rejected record type 22 with sequence 
01. Zeroes allowed. 
Total [[NSCC]] Rejected Input–Reject 
Items 
Input: Space 
Output: Total number of [[NSCC]] rejected record type 23 with sequence 
01. Zeroes allowed. 
Total [[NSCC]] Rejected Input–Detail 
Items 
999,999,999 
Input: Space 
Output: Total number of [[NSCC]]-rejected record type 24 with sequence 
01. Zeroes allowed. 
Total [[NSCC]] Rejected Input–
Summary Items 
999,999,999 
Input: Space 
Output: Total number of [[NSCC]]-rejected record type 25 with sequence 
01. Zeroes allowed. 
Filler  
[[NSCC]] Reject Indicator Input: Space Output: 
l 0 = Accepted by [[NSCC]] 
l 1 = Rejected by [[NSCC]] 
Filler / Reject Code 1 Input: Space 
Output: Reject Code 
Filler / Reject Code 2 Input: Space 
Output: Reject Code 
Filler / Reject Code 3 Input: Space 
Output: Reject Code 
Filler / Reject Code 4 Input: Space 
Output: Reject Code 
Request on a Plan 
• This particular example is a follow-up request from the Super Omnibus Account request (Example #1).  
• This request may also be used separately for any plan, regardless of whether it belongs to a super 
omnibus account or not. 
• Submitted on 03/07/2005 
• Plan level request & response 
• Detail level 
• Historical data request 
• 5 days from 02/28/05 to 03/04/05 
• Non-recurring 

---

## Page 19

Standardized Data Reporting Technical Guide 
Sample Scenarios 19 
• 10,000.00 threshold 
• Buys only 
• Acknowledgment is required but not shown in example. 
SDR Request Record (F 20) 
Key Fields/Data Description 
SDR Control Number 56435 
SDR Request Type 02 = Plan Level 
The fund is indicating that the account is a plan. Since the account at the fund is a 
super omnibus account, the fund has provided the plan [[ID]] to identify that particular 
plan within the super omnibus account.  If the account at the fund was not a super 
omnibus account, then the fund account number may be sufficient to identify the 
plan. 
Firm Number 0675 
In this example, there is an "underlying firm," which indicates that the firm is a 
service provider acting on behalf of another firm. 
Underlying Firm 0004 
This is the firm that is using a service provider to support the SDR functionality. 
Underlying Firm Indicator 03 
UFS Number 
Fund Number 564350600000001 
Fund Account Number CA1000231 
Either the fund account number or firm account number is provided. In this 
example, both are provided. 
Firm Account Number 13454637 
Either the fund account number or firm account number is provided. In this 
example, both are provided. 
From Date 02282005 
Security Issue [[ID]] 261465763 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
PLAN014354321 
In this example, the fund is indicating that the account is a plan and has 
provided the Plan [[ID]] for which it is requesting plan [[participant]] information. 
• For super omnibus accounts, this information is necessary to request information 
for a particular plan or [[investor]] omnibus account.  
• For non-super omnibus accounts, the fund account number or firm account 
number may be sufficient to identify the account. 
• When a Plan [[ID]] or [[investor]] Omnibus Account is provided, the Request Type 
should be set accordingly.  
• Best Practice: This account number should only be provided if the Request Type 
is “02” or “03”. 

---

## Page 20

Standardized Data Reporting Technical Guide 
Sample Scenarios 20 
Key Fields/Data Description 
Omnibus Account Indicator 0 = PLAN [[ID]] 
To Date 03042005 
Threshold Amount 000010000 
The fund is specifying that it is only interested in transactions that have a minimum 
of $10,000. 
Transaction Type 01 = Buy 
The fund is specifying that it is only interested in buy transactions. 
Request on a Plan-Response Records 
Response Records 
SDR Header (B/U 21) 
Key Fields/Data Description 
SDR Control Number 564350600000001 
SDR Response Number 067550610000001 
Response Type 02 = Detail Level 
Since the request was at a plan level, the firm will provide details of the plan to 
participants in the plan. 
Partial Response Indicator 0 = Full/Final Response 
In this example, the response contains all requested data in one file. This 
response is marked as a full/final response. 
Firm Number 0675 
Underlying Firm 0004 
The firm should echo back information provided by the fund. 
Underlying Firm Indicator 03 
UFS Number 
Fund Number 5643 
Fund Account Number CA1000231  
The firm should echo back information provided by the fund. 
Firm Account Number 13454637 
The firm should echo back information provided by the fund. 
Security Issue [[ID]] 261465763 

---

## Page 21

Standardized Data Reporting Technical Guide 
Sample Scenarios 21 
SDR Detail (B/U 24) #1 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
PLAN014354321 
The firm should echo back information provided by the fund. 
Omnibus Account Indicator 0 = Plan [[ID]] 
SSN / TIN 234232345 
This is the SSN of the first [[participant]] identified in the plan. 
SSN / TIN Indicator 2 = SSN 
NAV Date 02282005 
Transaction Type 01 = Buy 
Transaction category 1 = Category 1 
Transaction Code 09 = Exchange 
Optionally provided description of the transaction 
Dollar Amount 0000000002500000 (i.e., $25,000 Buy) 
Share Amount 00000250000000 (i.e., 25,000 [[shares]]) 
Price 000001000000 (i.e., Price = $1.00) 
Transaction Source  0 = [[participant]] 
This indicates that the buy was initiated by the [[participant]] (e.g., this is the 
purchase side of a cross-fund exchange) 
[[participant]]-directed transactions are the [[default]] transaction source. This example 
optionally specifies the source for illustration purposes. 
Customer Name JOHN SMITH 
The name is optionally provided by the firm. 
SDR Detail (B/U 24) #2 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
PLAN014354321 
The firm should echo back information provided by the fund. 
Omnibus Account Indicator 0 = Plan [[ID]] 
SSN / TIN 234232345 
This is the second detail record for this particular [[participant]]. It occurs on a 
different day. 
SSN / TIN Indicator 2 = SSN 
NAV Date 03022005 

---

## Page 22

Standardized Data Reporting Technical Guide 
Sample Scenarios 22 
Key Fields/Data Description 
This is the second detail record for this particular [[participant]]. It occurs on a 
different day. 
Transaction Type 01 = Buy 
Transaction category 1 = Category 1 
Transaction Code 23 = Rebalance. 
Optionally provided description of the transaction 
Dollar Amount 0000000005000000 (i.e., $50,000 Buy) 
Share Amount 00000250000000 (i.e., 25,000 [[shares]]) 
Price 000002000000 (i.e., Price = $2.00) 
Transaction Source 0 = [[participant]]  
This is a [[participant]]-directed buy. 
Customer Name JOHN SMITH  
The name is optionally provided by the firm. 
SDR Detail (B/U 24) #3 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
PLAN014354321 
Omnibus Account Indicator 0 = Plan [[ID]] 
SSN / TIN 234670001 
This is the SSN of the first [[participant]] identified in the plan 
SSN / TIN Indicator 2 = SSN 
NAV Date 03032005 
Transaction Type 05 = Transfer In 
Transaction category 1 = Category 1 
Transaction Code 08 = Transfer. 
Optionally provided description of the transaction 
Dollar Amount 0000000001000000 (i.e., $10,000 Buy) 
Share Amount 00000100000000 (i.e., 10,000 [[shares]]) 
Price 000001000000 (i.e., Price = $1.00) 
Transaction Source 0 = [[participant]] 
Customer Name JOE THOMPSON III 

---

## Page 23

Standardized Data Reporting Technical Guide 
Sample Scenarios 23 
SDR Trailer (B/U 27) 
Key Fields/Data Description 
SDR Control Number 5643066001 
Firm Number 0675 
Fund Number 5643 
Security Issue [[ID]] 261465763 
Total Detail Items within this Group 000000003  
(Total number of record type 24, sequence 01.) 
Total Summary Items within this 
Group 
000000000  
(Total number of record type 25, sequence 01.) 
Total Records within this Group 000000005  
(Total number of physical records including headers and trailers.) 
Request on an [[investor]] Omnibus Account 
• [[investor]] Omnibus Account. 
• Fund Account Number provided. 
• [[investor]] Omnibus Account Number provided. 
• Detail level. 
• Three days historical. 
• All other fields have [[default]] data. 
• Acknowledgment is required but not shown in example. 
SDR Request Record (F 20) 
Key Fields/Data Description 
SDR Control Number 553452520000001 
SDR Request Type 03 = [[investor]] Omnibus 
The fund is indicating that the account is an [[investor]] omnibus account and has 
optionally provided the [[investor]] omnibus account number. 
Firm Number 2205 
Fund Number 5534 
Fund Account Number 1234567891 
Only the fund account number is provided, and it relates to [[investor]] omnibus 
accounts held by the firm. 
From Date 09012005 
Security Issue [[ID]] 880210505 

---

## Page 24

Standardized Data Reporting Technical Guide 
Sample Scenarios 24 
Key Fields/Data Description 
To Date 09032005 
 
SDR Header (B/U 21) 
Key Fields/Data Description 
SDR Control Number 553452520000001 
SDR Response Number 220552530000001 
Response Type 02 = Detail Level 
Since the request was at an [[investor]] omnibus account level, the firm provides 
details of the shareholders in the account. 
Partial Response Indicator 0 = Full/Final Response 
In this example, the response contains all requested data in one file. This 
response is marked as a full/final response. 
Firm Number 2205 
Fund Number 5534 
Fund Account Number 00000000001234567891 
Security Issue [[ID]] 880210505 
 
SDR Detail (B/U 24) #1 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
00000000000112233445 
In this example, there are multiple individuals within the fund account number. 
Each individual (SSN/TIN) is assigned an internal account number ([[investor]] 
omnibus account number) by the firm. 
This is the first individual/[[investor]] account within the omnibus account that is 
held at the fund. 
Omnibus Account Indicator  1 = [[investor]] Omnibus Account 
SSN/TIN 111111111 
This is the SSN of the first [[participant]] identified in the plan. 
SSN/TIN Indicator 2 = SSN 
NAV Date 09012005 
Transaction Type 01 = Buy 
Transaction Category 1 = Category 1 
Transaction Code 09 = Exchange 

---

## Page 25

Standardized Data Reporting Technical Guide 
Sample Scenarios 25 
Key Fields/Data Description 
Optionally provided description of the transaction 
Dollar Amount 0000000001000000 (i.e., $10,000.00 buy) 
Share Amount 00000004612546 (i.e., 461.2546 [[shares]]) 
Price 000021680000 (i.e., $21.68) 
SDR Detail (B/U 24) #2 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
00000000000112233445   
This is still the account number of the first [[investor]] identified in the omnibus 
account. 
Omnibus Account Indicator 1 = [[investor]] Omnibus Account 
SSN/TIN 111111111 
This is still the SSN of the first [[investor]] identified in the omnibus account. 
SSN/TIN Indicator 2 = SSN 
NAV Date 09022005 
This is the second detail record identified for this particular [[investor]]. The activity 
occurs on a different day within the date range provided. 
Transaction Type 02 = Sell 
Transaction Category 1 = Category 1 
Dollar Amount 0000000001035516 (i.e., $10,355.16 sell) 
Share Amount 00000004612546 (i.e., 461.2546 [[shares]]) 
Price 000021680000 (i.e., $22.45) 
 
• Bought one day at a price of $21.68 and sold the next day at the price of $22.45 for a profit of 
$355.16.  STR (short-term redemption) info was also not provided. This scenario may prompt 
follow up. 
 
 
 

---

## Page 26

Standardized Data Reporting Technical Guide 
Sample Scenarios 26 
SDR Detail (B/U 24) #3 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
00000000000001234567 
In this example, there are multiple individuals within the fund account number. 
Each individual (SSN/TIN) is assigned an internal account number ([[investor]] 
omnibus account number) by the firm. 
This is the second individual/[[investor]] account within the omnibus account that is 
held at the fund. 
Omnibus Account Indicator 1 = [[investor]] Omnibus 
SSN/TIN 123456789 
This is the TIN of the second shareholder identified in the omnibus account. 
SSN/TIN Indicator 1 = TIN 
NAV Date 09012005 
Transaction Type 01 = Buy 
Transaction Category 1 = Category 1 
Dollar Amount 0000000002532344 (i.e., $25,323.44 buy) 
Share Amount 00000011680553 (i.e., 1,168.0553 [[shares]]) 
Price 000021680000 (i.e., $21.68) 
SDR Detail (B/U 24) #4 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
00000000000001234567 
In this example, there are multiple individuals within the fund account number. 
Each individual (SSN/TIN) is assigned an internal account number ([[investor]] 
omnibus account number) by the firm. 
This is the second individual/[[investor]] account within the omnibus account that is 
held at the fund. 
Omnibus Account Indicator 1 = [[investor]] Omnibus 
SSN/TIN 123456789 
This is the TIN of the second shareholder identified in the omnibus account. 
SSN/TIN Indicator 1 =TIN 
NAV Date 09032005 
Transaction Type 01 = Buy 
Transaction Category 1 = Category 1 
Dollar Amount 0000000002500000 (i.e., $25,000.00 buy) 
Share Amount 00000011494253 (i.e., 1,149.4253 [[shares]]) 

---

## Page 27

Standardized Data Reporting Technical Guide 
Sample Scenarios 27 
Key Fields/Data Description 
Price 000021750000 (i.e., $21.75) 
 
[[investor]] Omnibus Account 1234567, SSN 123456789 bought [[shares]] on 09/01/2005 and on 09/03/2005. No 
[[shares]] sold from this Security Issue [[ID]], but frequent trading is occurring based on the three days. This may 
prompt question on whether sell side exchanges are short term. 
SDR Detail (B/U 24) #5 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
00000000000007654321 
This is the third individual/[[investor]] account within the omnibus account that is 
held at the fund. 
Omnibus Account Indicator 1 = [[investor]] Omnibus 
SSN/TIN 978654321 
This is the SSN of the third shareholder identified in the omnibus account. 
SSN/TIN Indicator 2 = SSN 
NAV Date 09012005 
Transaction Type 01 = Buy 
Transaction Category 1 = Category 1 
Dollar Amount 0000000010000000 (i.e., $100,000.00 buy) 
Share Amount 00000046125461 (i.e., 4612.5461 [[shares]]) 
Price 000021680000 (i.e., $21.68) 
SDR Detail (B/U 24) #6 
Key Fields/Data Description 
SDR Detail (B/U 24) #6 00000000000001726354 
This is the fourth individual/[[investor]] account within the omnibus account that is 
held at the fund. 
Omnibus Account Indicator 1 = [[investor]] Omnibus 
SSN/TIN 895746231 
This is the SSN of the fourth shareholder identified in the omnibus account. 
SSN/TIN Indicator 2 = SSN 
NAV Date 09012005 
Transaction Type 02 = Sale 

---

## Page 28

Standardized Data Reporting Technical Guide 
Sample Scenarios 28 
Key Fields/Data Description 
Transaction Category 1 = Category 1 
Dollar Amount 0000000001000000 
($10,000.00) 
Share Amount 00000004612546 
(461.2546 [[shares]]) 
Price 000021680000 
($21.68) 
SDR Trailer (B/U 27) 
Key Fields/Data Description 
SDR Control Number 5534224001 
Firm Number 2205 
Fund Number 5534 
Security Issue [[ID]] 880210505 
Total Detail Items within this Group 000000006 
(Total number of record type 24, sequence 01). 
Total Summary Items within this 
Group 
000000000 
(Total number of record type 25, sequence 01.) 
Total Records within this Group 000000008 (for illustration purpose) (Total number of physical records including 
headers and trailers.) 
 
  

---

## Page 29

Standardized Data Reporting Technical Guide 
Sample Scenarios 29 
Rep Level Data # 1 
SDR Request Record (F 20) 
• Fund requests rep level data. 
• Recurring 
• Assumes that the current date is 08/31/2005. 
• Fund sends request to stop recurring data. 
• Optional record 3 not provided. 
• Acknowledgment is required but not shown in example.  
 
Record 1 of 3 (Required) 
Key Fields/Data Description 
SDR Control Number 589452430000001 
SDR Request Type 05 = Rep Level 
The fund is requesting shareholder transactions where a particular rep is 
associated, within a fund account for a particular Security Issue [[ID]]. 
Firm Number 0164 
Fund Number 5894 
Fund Account Number 1567972746 
In this example, only the fund account number is provided. The rep level detail 
can only be provided for one particular omnibus account (i.e., plan [[ID]] or [[investor]] 
omnibus account). This assumes that the fund account number is sufficient to 
identify the plan/[[investor]] omnibus account. 
From Date 08312005 
Since this request is a recurring request, this date should be the current date. 
However, this date is ignored by the firm, who provides daily data beginning on 
the date that it receives the request. 
Security Issue [[ID]] 315805200 
Recurring Indicator 1 = Yes 
Includes Category 2 Transactions? 0 = No 
RR Number 615UELE 
This information must be provided on rep level requests. 
RR Branch 615 

---

## Page 30

Standardized Data Reporting Technical Guide 
Sample Scenarios 30 
Rep Level Data # 1-Response Records 
SDR Header (B/U 21) 
Firm sends responses on a daily basis. Response header, optional header record 2 not provided.  
Key Fields/Data Description 
SDR Control Number 589452430000001 
SDR Control Number 016452440000001 
Response Type 02 = Detail Level 
This response is for a Rep Level request that also provided an [[investor]] omnibus 
account number for which detail shareholder information is available. 
Partial Response Indicator 1 = Partial Response 
Firm Number 0164 
Fund Number 5894 
Fund Account Number 1567972746 
The firm should echo back information provided by the fund. 
Firm Account Number EX1ACCOUNT1 
Additional account information may be provided by the Firm. 
Security Issue [[ID]] 315805200 
Correction Indicator 0 = Regular 
SDR Detail (B/U 24) #1 
• Firm sends responses on a daily basis. 
(Only one day's sample data is shown. When available, additional detail records should be provided for 
each SSN/TIN and for each day within the date requested date range.) 
• Using Detail Records 1 & 2, optional record 3 not provided. 
• For brevity, only two example detail records are provided. 
 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
EX1ACCOUNT1 
In this example, the firm account number, which is cross- referenced to the 
fund account number, is the same as the [[investor]] omnibus account. 
Omnibus Account Indicator 1 = [[investor]] Omnibus Account 
SSN/TIN 111111111 
SSN/TIN Indicator 2 = SSN 
NAV Date 08312005 

---

## Page 31

Standardized Data Reporting Technical Guide 
Sample Scenarios 31 
Key Fields/Data Description 
Transaction Type 01 = Buy 
Transaction Category 1 = Category 1 
Dollar Amount 0000000001000000 (i.e., $10,000.00 Buy) 
Share Amount 00000005000000 (i.e., 500.0000 [[shares]]) 
Price 000000200000 (i.e., $20.00) 
Transaction Source 0 = [[participant]] 
RR Number 615EULE 
RR Branch 615 
SDR Detail (B/U 24) #2 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
EX1ACCOUNT1 
Omnibus Account Indicator 1 = [[investor]] Omnibus Account 
SSN/TIN 222222222 
SSN/TIN Indicator 2 = SSN 
NAV Date 08312005 
Transaction Type 02 = Sell 
Transaction Category 1 = Category 1 
Dollar Amount 00000000200000 (i.e., 2,000.00 Sell) 
Share Amount 00000001000000 (i.e., 1,000.000 [[shares]]) 
Price 20.000 
STR Fee Amount 000000200000 (i.e., $20.0000) 
Transaction Source 1 = Rep 
RR Number 615EULE 
RR Branch 615 
SDR Trailer (B/U 27) 
Key Fields/Data Description 
SDR Control Number Rep Example 
Firm Number 0164 

---

## Page 32

Standardized Data Reporting Technical Guide 
Sample Scenarios 32 
Key Fields/Data Description 
Fund Number 5894 
Security Issue [[ID]] 315805200 
Total Detail Items within this Group 000000002 
(Total number of record type 24, sequence 01.) 
Total Summary Items within this Group 000000000 
(Total number of record type 25, sequence 01.) 
Total Records within this Group 000000004 
(Total number of physical records including headers and trailers.) 
Stop Recurring Request 
SDR Request Record (F 20) 
Request to stop recurring response (example #6). Records 1 & 2 only. 
Key Fields/Data Description 
SDR Control Number 589452470000001 
SDR Request Type 06 = Stop Recurring 
Firm Number 0164 
Fund Number 5894 
Fund Account Number 1567972746 
From Date 09302005 (Today's date) 
Security Issue [[ID]] 315805200 
RR Number 615UELE 
RR Branch 615 
Original SDR Control Number 
Used to stop a recurring request. 
589452430000001 
 
• Fund immediately stops request. Response data is not sent. 
 
 

---

## Page 33

Standardized Data Reporting Technical Guide 
Sample Scenarios 33 
Rep Level Data # 2 
SDR Request Record (F 20) 
• Fund requests rep. level data. 
• Historical data. 
• Optional record 3 not provided. 
• Acknowledgment is Required but not shown in example.  
 
Record 1 of 3 (Required) 
Key Fields/Data Description 
SDR Control Number 589452430000001 
SDR Request Type 05 = Rep Level 
Firm Number 0164 
Fund Number 5894 
Fund Account Number 1567972746 
From Date 08012005 
Security Issue [[ID]] 315805200 
Recurring Indicator 1 = Yes 
To Date 08312005 
Includes Category 2 Transactions? 0 = No 
Rep Level Data # 2-Response Records 
SDR Header (B/U 21) 
• Firm sends response to provide data for the 23 business days requested. 
• Firm could send partial response, but this example is full and final. 
• Response header, optional header record 2 not provided. 
 
Key Fields/Data Description 
SDR Control Number 589452430000001 
SDR Response Number 016452430000001 
Response Type 02 = Detail Level 
Partial Response Indicator 0 = Full/Final Response 
Firm Number 0164 

---

## Page 34

Standardized Data Reporting Technical Guide 
Sample Scenarios 34 
Key Fields/Data Description 
Fund Number 5894 
Fund Account Number 1567972746 
The firm should echo back information provided by the fund. 
Firm Account Number EX2ACCOUNT2 
Additional account information may be provided by the firm. 
Security Issue [[ID]] 315805200 
Correction Indicator 0 = Regular 
 
• Firm sends a one-time full response detail for the requested rep. 
• Using Detail Records 1 & 2, optional record 3 not provided. 
• For brevity, only two example detail records are provided. 
SDR Detail (B/U 24) #1 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
EX2ACCOUNT2 
Omnibus Account Indicator 1 = [[investor]] Omnibus Account 
SSN/TIN 111111111 
SSN/TIN Indicator 2 = SSN 
NAV Date 08152005 
Transaction Type 01 = Buy 
Transaction Category 1 = Category 1 
Dollar Amount 0000000001000000 (i.e., $10,000.00 buy) 
Share Amount 00000005000000 (i.e., 500.0000 [[shares]]) 
Price 000000200000 (i.e., $20.0000) 
Transaction Source 0 = [[participant]] 
RR Number 615EULE 
RR Branch 615 

---

## Page 35

Standardized Data Reporting Technical Guide 
Sample Scenarios 35 
SDR Detail  
(B/U 24) #2 
Key Fields/Data Description 
Plan [[ID]]/[[investor]] Omnibus Account 
Number 
EX2ACCOUNT2 
Omnibus Account Indicator 1 = [[investor]] Omnibus Account 
SSN/TIN 222222222 
SSN/TIN Indicator 2 = SSN 
NAV Date 09262005 
Transaction Type 02 = Sell 
Transaction Category 1 = Category 1 
Dollar Amount 0000000002000000 (i.e., $20,000.00 buy) 
Share Amount 00000010000000 (i.e., 1,000.0000 [[shares]]) 
Price 000000200000 (i.e., $20.0000000) 
STR Fee Amount 0020000 (i.e., $200.00) 
Transaction Source 1 = Rep 
RR Number 615EULE 
RR Branch 615 
SDR Trailer (B/U 27) 
Key Fields/Data Description 
SDR Control Number 589452430000001 
Firm Number 0164 
Fund Number 5894 
Security Issue [[ID]] 315805200 
Total Detail Items within this Group 000000002 
(Total number of record type 24, sequence 01.) 
Total Summary Items within this Group 000000000 
(Total number of record type 25, sequence 01.) 
Total Records within this Group 00000004 (for illustration purpose) 
(Total number of physical records including headers and trailers.) 

---

## Page 36

Standardized Data Reporting Technical Guide 
Sample Scenarios 36 
 
Other Scenarios 
Scenario Fund and Firm Processing 
Super Omnibus Account with various 
omnibus and non- omnibus accounts 
Fund 
• Fund submits fund level request. 
• Provides fund account number or firm account number. 
If the first-tier [[intermediary]] does not act as the conduit for data 
requests: 
• Work with the fund to contact the second-tier [[intermediary]] that 
maintains the shareholder level data. 
• Disclose to the fund the contact information for the second- tier 
[[intermediary]] that maintains the shareholder level data. 
Firm 
• Firm submits a Header Record (B/U 21) with a Response Type of 
03 = Both Detail and Summary Data. 
• Submits, first, a Detail Record (B/U 24) for each individual account 
found in the super omnibus account. 
• Submits Summary Record (B/U 25) for each plan found in the 
super omnibus account. 
• Submits Summary Record (B/U 25) for each [[investor]] omnibus 
account found in the super omnibus account. 
• Submits a Trailer Record (B/U 27). 
Partial Acknowledgment Fund 
Fund submits request with a date range 
Firm 
• The request is for a two-day historical data at a plan level. 
• The response is sent in one file; however, the firm may decide to 
send each day's data on separate days. 
• On Day 1, the firm sends in the first file (Header, Detail, Trailer). 
The Partial Indicator on the Header Record will be marked as  
1 = Partial. 
• This indicates to the fund that this file is a partial response to the 
SDR Request identified by the SDR Control Number. 
• On Day 2, the firm sends the second file. The Header Record 
contains the Partial Indicator marked as 0 = Full/Final 
Response. 
• This indicates to the fund that this file is the final response to the 
SDR Request identified by the SDR Control Number. 
• This also suggests that the fund should have received a previous 
file marked as a partial response. 

---

## Page 37

Standardized Data Reporting Technical Guide 
Sample Scenarios 37 
Scenario Fund and Firm Processing 
Partial Acknowledgment (Recurring) Fund 
• Fund submits a request that is marked as recurring. This indicates 
that the firm should send daily files until requested to stop. 
• Fund submits a Stop Recurring request to discontinue the daily 
files. 
• The Original SDR Control must be provided with the Stop 
Recurring request. 
Firm 
• For each of the daily files sent by the firm, the Partial 
Acknowledgment will be marked as 1 = Partial Response. 
• As soon as the firm receives the Stop Recurring request, it will no 
longer send a file. 
• Since sending of the file has stopped, a file containing a partial 
acknowledgment marked as 0 = Full/Final Response cannot be 
sent. 
Partial Acknowledgment (Other) Fund 
Fund submits a request 
Firm 
• The firm may send partial files to split up large files. The firm may 
also send partial files for various other reasons. 
• Each file must be marked accordingly as a partial or full/final 
response. 
• Each response file will also contain a unique SDR Response 
Number. 
• Corrections can then be isolated to the partial file with the 
appropriate SDR Control Number and SDR Response Number 
combination. 
Category 2 Transaction Fund 
• Fund submits a request at the appropriate account or [[investor]] 
level. 
• Provides the necessary account number or SSN information for the 
appropriate level. 
• Submits the Includes Category 2 Transaction field marked as  
1 = Yes. 
• This indicates the request is for both Category 1 and Category 2 
transactions. 
• This request will retrieve all activity for an account or [[investor]] 
and may result in an excessive amount of data. 
Firm 
• The firm submits a Detail Response. 
• A Detail record is provided for each individual (SSN), for one 
particular day, for a single transaction activity. 
• The transaction in each Detail includes the Transaction 
Source field marked as either 1 = Category 1 or 2 = Category 
2. (Space is equivalent to "1".) 
• The firm submits details on all transactions in each individual's 
account and marks the transaction source accordingly 

---

## Page 38

Standardized Data Reporting Technical Guide 
Sample Scenarios 38 
Scenario Fund and Firm Processing 
Correction Indicator Fund 
Fund submits a request that is marked as recurring. 
This indicates that the firm should send daily files until requested to stop. 
Firm 
• On Day 1, the firm submits a regular detail response file (i.e., 
Correction Indicator is space or 0 = Regular). 
• Each response file will contain a unique SDR Response 
Number. 
• Corrections can then be isolated to the partial file with the 
appropriate SDR Control Number and SDR Response Number 
combination. 
• On Day 2, the firm sends in another regular detail response file. 
• Also on Day 2, the firm sends a detail response file with a 
Correction Indicator marked as 1 = Correction against the file 
from Day 1. 
• The SDR Response Number is provided and used by the firm to 
isolate the correction to that particular partial file (i.e., Day 1 file). 
• Corrections may be done for any file, partial or full/final, detail or 
summary, etc. 
• Corrections are done against a set of data and NOT for 
specific details or a subset of details. The correction file 
should overwrite the previously sent regular file. 
Fund/SERV® Control Number Request Fund 
• Fund submits a Fund/SERV® Control Number Request type. 
• Provides the Fund/SERV® control number. 
• Provides the fund account number or firm account number. 
• Provides all other required data. 
Firm 
• Firm retrieves all transactions related to a Fund/SERV® control 
number. 
• Returns the Fund/SERV® control number on the Header Record. 
• Provides Detail records for each individual (SSN) for each 
transaction type. 
Non-[[NSCC]] Initiated Transaction 
(Response Data sent through [[NSCC]]) 
Fund 
• Fund calls the firm and requests information. 
• Provides the necessary information to the firm. 
• Firm provides an SDR Response Number that is used to return the 
data through [[NSCC]]. 
Firm 
• Firm runs query to retrieve requested data. 
• Firm uses the [[NSCC]] formats and creates a response file. 
• Provides the SDR Response Number in the Header record. 
• Uses the same number in the SDR Control Number field. 
• Submits file to [[NSCC]]. 

---

## Page 39

Standardized Data Reporting Technical Guide 
Sample Scenarios 39 
Scenario Fund and Firm Processing 
Transaction Code Fund 
Submits request with the necessary information to the firm. 
Firm 
• Firm runs query to retrieve requested data. 
• Firm uses the [[NSCC]] formats and creates a response file. 
• Response includes "Transaction Code" field in the Detail record for 
each trading activity. Firm uses the appropriate code to describe the 
transaction code (e.g., 09 = Exchange). 
• Submits file to [[NSCC]]. 

---

## Page 40

Standardized Data Reporting Technical Guide 
Business Processing 40 
BUSINESS PROCESSING 
The business process and interaction between the funds and intermediaries vary based on the situation. 
Intermediaries are also referred to as "Firms" and a Fund's [[CUSIP]] is also referred to as "[[SEC]] urity Issue [[ID]]" in 
the context of the [[NSCC]] SDR functionality and documentation. Funds are expected to provide all the 
necessary information for the intermediaries to retrieve the underlying shareholder's information. This results in 
detailed data being returned by the [[intermediary]] to the fund. 
In cases where a super omnibus account is involved, summary data will first be provided by the firm to the 
fund. The fund is provided with high-level data regarding the plans or [[investor]] omnibus accounts that are 
combined into the super omnibus account. The fund is then able to use the additional data from the Summary 
to send a more specific inquiry request (e.g., using a plan [[ID]] to limit the inquiry to the shareholders in that 
particular plan.) 
If the fund already has the specific data that can be provided and linked to the individual shareholders, the 
"Summary" request and response process is not needed. An initial request that contains enough detailed 
information is always answered by the firm with a response containing shareholder trading information, even 
on a super omnibus account. 
Inquiry Request Data 
Data on the shareholder's trading activity may be sent by the firm to the fund on an ad - hoc or daily scheduled 
basis. Regularly scheduled files (e.g., ongoing daily files) should be requested manually by the fund from the 
firm. The response files from the firm, whether they are as a result of a request done manually or through 
[[NSCC]], may be sent through SDR. 
SDR also allows the funds to make data requests from the firm. Various types of requests are used through 
[[NSCC]], including: 
Data Request Types 
• Fund Account Level 
• Plan Level 
• [[investor]] Omnibus Account Level 
• Fund/SERV® Control Number Request 
• Rep Level 
• Stop Recurring 
 
The format for the fund request input file/message will be the same for all request types, but different data is 
necessary based on the requests. Each request type indicates the additional data field used to refine the 
queries for the firm to extract data, accordingly. Additional search criteria may also be included to refine 
requests, such as threshold amount, [[CUSIP]]/Security Issue [[ID]], and transaction type.  

---

## Page 41

Standardized Data Reporting Technical Guide 
Business Processing 41 
Note: 
When using a threshold amount, only transactions with currency amounts greater than or equal to the threshold amount will 
be included in the response data. 
Rep Level information is generally not maintained on insurance company and may result in a reject if 
requested, using SDR Reject Code 76 – Rep Level Request Not Supported. 
Other data fields provide additional instructions that customize the request and the resulting response data. For 
example, since Category 1 transaction information is the assumed [[default]] search parameter, funds may use 
the "Includes Category 2 Transactions" field to indicate that it is requesting both Category 1 and  Category 2 
transactions. Other fields that modify the search parameters include from/to dates, transaction types, and 
threshold amounts. 
Note: 
The data that is actually provided on the request is the ultimate driver of the type or level of the request. For example, a 
fund account level request that also contains SSN info will result in shareholder level information rather than fund account 
level information. 
Acknowledgement, [[NSCC]] Reject and Firm Reject Data 
Acknowledgment Data 
The initial response from the firm to the fund is an Acknowledgment record. The Acknowledgment is a 
proactive indication from the firm that it has received the request from the fund and will also turn off the [[NSCC]] 
SDR Reminder record. 
[[NSCC]] Reject Data 
[[NSCC]] performs preliminary validations of SDR requests received from funds and of SDR responses provided 
by firms. Files or records that [[DO]] not pass the [[NSCC]] validation are returned to the submitter with the 
appropriate reject code. 
Note: 
A set of response records may be partially rejected. For example, a response may contain ten detail records and one of 
those records may not pass validation. [[NSCC]] rejects the single record and returns it to the firm along with an [[NSCC]]-
generated header and trailer to complement the rejected record. 
Firm Reject Data 
Firms may also reject the fund's data request but use the Reject record to [[DO]] so. An appropriate reject code 
must be provided. Situations may arise where firms acknowledge an SDR request, and later learn that the 
request cannot be fulfilled. In this instance, firms should submit a Reject record with the appropriate reason 
code for the previously acknowledged SDR request. A full listing of SDR reject codes can be found on the 
Learning Center https://dtcclearning.com/products-and-services/mutual-fund-services/networking/standardized-
data-reporting-sdr.html#heading-2 

---

## Page 42

Standardized Data Reporting Technical Guide 
Business Processing 42 
Response Data 
There are various levels of information in super omnibus accounts. For example, a super omnibus account, 
identified by a fund account number or [[intermediary]] account number (BIN) (fund account level), may contain 
assets from multiple retirement plans (plan level), and in turn, each plan contains multiple participants or 
underlying shareholders. 
Due to this complexity, the activity and corresponding data related to these accounts is significant. In order to 
control the volume of data that could potentially be extracted and sent to the fund for these super omnibus 
accounts, it is important to retrieve data at a summary level (fund account level request).  
When a request is submitted against a super omnibus account, it is expected that summary data will be 
returned by the firm to the fund for plans or [[investor]] omnibus accounts that are contained within the super 
omnibus account. Detailed information may also be sent for individual shareholder accounts that are a part of 
the super omnibus account. 
The summary data provides sufficient information to help the funds identify specific plans or [[investor]] omnibus 
accounts where trading is occurring frequently. The fund would then be able to request data at a plan level or 
[[investor]] omnibus account level and obtain detailed information about the underlying participants/shareholders.  
Detail response data is expected to be provided on shareholders when a request is made against specific 
plans, [[investor]] omnibus accounts, or individuals specified by the SSN. 
[[NSCC]] Reminders 
[[NSCC]] SDR Reminders are records that notify the fund, the firm, and possibly other related parties that an 
appropriate response has not been made to an SDR Request. [[NSCC]] sends a Reminder record for Requests 
with SDR Control Numbers that have not been acted upon with an Acknowledgment record or a Reject record. 
Only Acknowledgment or Reject record responses can turn off Reminders. Detail or Summary records [[DO]] 
not turn off Reminders. 
Reminders will be sent for a period of 10 processing days (including Saturday) from the original date on which 
the SDR Control Number is stored on the [[NSCC]] database. 
After this timeframe, the SDR Control Numbers will be deleted from the system.  
The first Reminder is sent on the first business day after the submission date of the SDR Request and is sent 
via the last cycle of the day (M-F, 4 P.M. ET; Sat, 2 P.M. ET.) Reminders are sent with the Autoroute Output 
file within the SDR Request record stream. Within this stream, firms receive Request record s plus Reminders, 
and funds receive [[NSCC]] Request Rejects plus Reminders. 

---

## Page 43

Standardized Data Reporting Technical Guide 
System Processing 43 
SYSTEM PROCESSING 
System Interface and Datatrak & Autoroute Schedule 
Systems Interface 
Two different interfaces are used to support this enhancement. HTTPS protocol is used for web in put and 
output using the [[DTCC]] WebDirect, and FTP/NDM are used for input and output of flat files over the [[DTCC]] 
SMART Network. 
Datatrak and Autoroute Schedule 
Data files for this functionality are assigned Datatrak SYSIDs and Autoroute numbers. This informa tion is 
available in the Mutual Fund Services section of the Learning Center under Schedules. Reference the 
"Networking and Omni/SERV Transmission Schedule" document. All SDR transmission information is 
available, including the [[participant]] service (testing) environment: 
Processing Flow 
 


---

## Page 44

Standardized Data Reporting Technical Guide 
System Processing 44 
Process Flow using ftp (batch) on data request input/output and response 
input/output. 
 
1. Fund sends a data request to [[NSCC]] during the acceptable input timeframe. 
2. [[NSCC]] does a preliminary validation, which will result in accepted or rejected records. 
3. [[NSCC]] stages the records to the appropriate destination and output files. 
4. At the appropriate output time, [[NSCC]] sends rejects back to the fund and accepted records to the 
intermediaries. (Other records may also be sent to the intermediaries and funds as part of the 
output file.) 
5. The [[intermediary]] will take the data request records and may run some preliminary validation, which 
will result in accepted or rejected records.  
6. If [[intermediary]] rejects, then the reject record will be submitted to [[NSCC]] during the input 
timeframe. [[NSCC]] will pass back to the fund in the output file. 
7. If [[intermediary]] accepts, then it will process the request. The first step is for the [[intermediary]] to 
prepare and submit an Acknowledgment to [[NSCC]] during the appropriate input timeframe. [[NSCC]] will 
pass to the fund in the output file. 
8. The process to retrieve the data may take some time and may result in a reject or a response with 
data. 
9. The [[intermediary]] will respond with a data response. Or, if after querying its systems the 
[[intermediary]] identifies an issue with the data request, the [[intermediary]] will send reject records with 
the applicable reject code to [[NSCC]].  
10. [[NSCC]] does a preliminary validation, which will result in accepted or rejected records.   
11. At the appropriate output time, [[NSCC]] sends rejects back to the [[intermediary]] and accepted data 
records to the funds. (Other records may also be sent to the intermediaries and funds as part of the 
output file.) 
Note: 
[[NSCC]] will modify the trailer record being sent to the fund to include the number of accepted and rejected 
Summary/Detail records. This will allow the fund to know whether they received a complete set of data for their data 
request. 
12. [[NSCC]] will send SDR Reminders each day for a period of 10 processing days as long as an SDR 
Request Control Number has not been acted upon with an Acknowledgment or Reject record. Detail or 
Summary records [[DO]] not turn off Reminders. After 10 processing days, a Reminder is no longer sent. 

---

## Page 45

Standardized Data Reporting Technical Guide 
System Processing 45 
Acknowledgement, Reject, and Detail/Summary Response records may still be sent even after the 
Reminders are discontinued. 
Process flow over HTTPS using [[DTCC]] WebDirect 
1. Fund can upload MRO file using [[DTCC]] WebDirect Upload function. 
2. [[NSCC]] does a preliminary validation. 
3. [[NSCC]] will make the processed file available for download via the [[DTCC]] WEBDIRECT  
List of SDR File Record Types 
Record Type Submitted By 
Record Type 20 = SDR Request Fund (F) 
Record Type 21 = SDR Header Firm (B), Underlying Firm (U) 
Record Type 22 = SDR Acknowledgment Firm (B), Underlying Firm (U) 
Record Type 23 = SDR Reject Firm (B), Underlying Firm (U) 
Record Type 24 = SDR Detail Firm (B), Underlying Firm (U) 
Record Type 25 = SDR Summary Firm (B), Underlying Firm (U) 
Record Type 27 = SDR Trailer Firm (B), Underlying Firm (U) 
Record Type 28 = SDR Reminder [[NSCC]] (N) 
Record Type 29 = SDR Grand Total Trailer B, U, and F 
 
Other records used for the SDR process include: 
Record Type Submitted By 
Datatrak Header All 
Datatrak Trailer All 
Autoroute Header All 
[[NSCC]] Output Header [[NSCC]] 
 
 
 

---

## Page 46

Standardized Data Reporting Technical Guide 
System Processing 46 
SDR Request Data File Structure 
Provided below is the standard format and structure for the SDR Request Input/Output Data file. The examples 
include input from the Fund to [[NSCC]], output from [[NSCC]] to the Firm, and output from [[NSCC]] to the Fund. 
Output may include Reminders to both Fund and Firm. 
Record Structure for Request Record (Input) 
Following is the standard format and structure for the SDR Request Input Data file that is sent from the Fund to 
[[NSCC]]. 
Datatrak Header Datatrak Header 
Record type '20' Request 1 
Record type '20'  
Record type '20' Request 2 
Record type '20' Request 3 
Record type '20' Request n-1 
Record type '20' Request n 
Record type '29' Grand Total Trailer 
Datatrak Trailer Datatrak Trailer 
 
Record Structure for Request (Output to Firm) 
The following is the standard format and structure for the SDR Request Output Data file that is sent from 
[[NSCC]] to the Firm.  
Autoroute Header Autoroute Header 
[[NSCC]] Output Header [[NSCC]] Output Header 
Record type '20' Request 1 
Record type '20'  
Record type '20' Request 2 
Record type '20' Request n-1 
Record type '20' Request n 
Record type N'28' Reminder 1 
Record type N'28' Reminder n 
Record type '29' Grand Total Trailer 

---

## Page 47

Standardized Data Reporting Technical Guide 
System Processing 47 
Record Structure for Request (Output to Fund) 
The following is the standard format and structure for the SDR Request Output Data file that is sent from 
[[NSCC]] to the Fund. 
Autoroute Header Autoroute Header 
[[NSCC]] Output Header [[NSCC]] Output Header 
[[NSCC]] Reject of Record type '20' [[NSCC]] Reject 1 
[[NSCC]] Reject of Record type '20'  
[[NSCC]] Reject of Record type '20' [[NSCC]] Reject n 
Record type N'28' Reminder 1 
Record type N'28' Reminder n 
Record type '29' Grand Total Trailer 
SDR Response Data File Structure 
The standard format and structure of the SDR Response Data file may be used through [[NSCC]] or 
through other means of communication between funds and firms. 
The SDR Data "Response" (Acknowledgment, Firm Reject, Detail, Summary) Input/Output file on mainframe 
has "groups" of records that contain a header, detail records and a trailer. Each group represents an account at 
the fund for a particular firm within a particular Security Issue [[ID]]. Each detail represents transactions for a 
specific shareholder/[[participant]] (SSN) within a specific plan/[[investor]] omnibus account (if applica ble). 
Summary records apply to super omnibus accounts and may be used within the header/trailer group instead of 
detail records. Each summary record represents a single plan or [[investor]] omnibus account within the super 
omnibus account. This record contains summary level information that helps the funds identify specific plans or 
[[investor]] omnibus accounts where trading is occurring frequently. 
The Input file may contain a variety of records including Acknowledgment, Firm Rejects, Details, and 
Summaries. These records are placed into groups that are identified through a separate Application Header 
and Trailer. The output file to the Fund contains these records that have not been rejected by [[NSCC]]. The 
output file to the Firm contains the records that have been rejected by [[NSCC]]. 
Record Structure for SDR Response Input Data file 
The following is the standard format and structure for the SDR Response Input Data file  that is sent from the 
firm to the fund. 

---

## Page 48

Standardized Data Reporting Technical Guide 
System Processing 48 
Record Structure for Detail Information Only (Input) 
Record Type '21' Header Group 
Record type '24' Detail 1 
Record type '24' Detail 2 
Record type '24' Detail n-1 
Record type '24' Detail n 
Record Type '27' Trailer Group 
Record Structure for Summary Information Only (Input) 
 
Record Type '21' Header Group 
Record type '25' Summary 1 
Record type '25' Summary 2 
Record type '25' Summary 3 
Record type '25' Summary n-1 
Record type '25' Summary n 
Record Type '27' Trailer Group 
Record Structure for Both Detail and Summary Information (Input) 
 
Record Type '21' Header Group 
Record type '24' Detail 1 
Record type '24' Detail 2 
Record type '24' Detail n-1 
Record type '24' Detail n 
Record type '25' Summary 1 
Record type '25' Summary 2 
Record type '25' Summary 3 
Record type '25' Summary n-1 
Record type '25' Summary n 
Record type '27' Trailer Group 

---

## Page 49

Standardized Data Reporting Technical Guide 
System Processing 49 
Record Structure for a Variety of Responses (Input) 
Datatrak Header Datatrak Header 
Record type '21' Header Group 1 
Record type '22' Acknowledgment 1 
Record type '27' Trailer Group 1 
 
Record type '21' Header Group 2 
Record type '22' Acknowledgment 2 
Record type '27' Trailer Group 2 
 
Record type '21' Header Group 3 
Record type '23' Firm Reject 1 
Record type '27' Trailer Group 3 
 
Record type '21' Header Group 4 
Record type '24' Detail 1 
Record type '24' Detail 2 
Record type '24' Detail n-1 
Record type '24' Detail n 
Record type '27' Trailer Group 4 
 
Record type '21' Header Group 5 
Record type '25' Summary 1 
Record type '25' Summary 2 
Record type '25' Summary 3 
Record type '25' Summary n-1 
Record type '25' Summary n 
Record type '27' Trailer Group 5 
 
Record type '21' Header Group 6 
Record type '24' Detail 1 

---

## Page 50

Standardized Data Reporting Technical Guide 
System Processing 50 
Record type '24' Detail 2 
Record type '24' Detail n-1 
Record type '24' Detail n 
Record type '25 Summary 1 
Record type '25 Summary 2 
Record type '25 Summary 3 
Record type '25 Summary n-1 
Record type '25 Summary n 
Record type '27' Trailer Group 6 
Record type '29' Grand Total Trailer 
Datatrak Trailer Trailer Group 
 
  

---

## Page 51

Standardized Data Reporting Technical Guide 
System Processing 51 
Record Structure for a Variety of Responses (Output to Fund) 
Following is the standard format and structure for the SDR "Response" (Acknowledgment, Firm Reject, Detail, 
Summary) Output Data file that is sent from the [[NSCC]] to the fund. 
Autoroute Header Autoroute Header 
[[NSCC]] Output Header [[NSCC]] Output Header 
Record type '21' Header Group 1 
Record type '22' Acknowledgment 1 
Record type '27' Trailer Group 1 
 
Record type '21' Header Group 2 
Record type '22' Acknowledgment 2 
Record type '27' Trailer Group 2 
 
Record type '21' Header Group 3 
Record type '23' Firm Reject 1 
Record type '27' Trailer Group 3 
 
Record type '21' Header Group 4 
Record type '24' Detail 1 
Record type '24' Detail 2 
Record type '24' Detail n-1 
Record type '24' Detail n 
Record type '27' Trailer Group 4 
 
Record type '21' Header Group 5 
Record type '25' Summary 1 
Record type '25' Summary 2 
Record type '25' Summary 3 
Record type '25' Summary n-1 
Record type '25' Summary n 
Record type '27' Trailer Group 5 

---

## Page 52

Standardized Data Reporting Technical Guide 
System Processing 52 
 
Record type '21' Header Group 6 
Record type '24' Detail 1 
Record type '24' Detail 2 
Record type '24' Detail n-1 
Record type '24' Detail n 
Record type '25 Summary 1 
Record type '25 Summary 2 
Record type '25 Summary 3 
Record type '25 Summary n-1 
Record type '25 Summary n 
Record type '27' Trailer Group 6 
Record type '29' Grand Total Trailer 
Datatrak Trailer Trailer Group 
 
Record Structure for a Variety of Responses (Output to Firm) 
Following is the standard format and structure for the SDR "Response" (Acknowledgment, Firm Reject, Detail, 
Summary) Output Data file that is sent from the [[NSCC]] to the firm. 
Autoroute Header Autoroute Header 
[[NSCC]] Output Header [[NSCC]] Output Header 
[[NSCC]] Reject of Record type '21' Header Group 1 
[[NSCC]] Reject of Record type '22' Acknowledgment 1 
[[NSCC]] Reject of Record type '27' Trailer Group 1 
 
[[NSCC]] Reject of Record type '21' Header Group 2 
[[NSCC]] Reject of Record type '22' Acknowledgment 2 
[[NSCC]] Reject of Record type '27' Trailer Group 2 
 
[[NSCC]] Reject of Record type '21' Header Group 3 
[[NSCC]] Reject of Record type '23' Firm Reject 1 

---

## Page 53

Standardized Data Reporting Technical Guide 
System Processing 53 
[[NSCC]] Reject of Record type '27' Trailer Group 3 
 
[[NSCC]] Reject of Record type '21' Header Group 4 
[[NSCC]] Reject of Record type '24' Detail 1 
[[NSCC]] Reject of Record type '24' Detail 2 
[[NSCC]] Reject of Record type '24' Detail n-1 
[[NSCC]] Reject of Record type '24' Detail n 
[[NSCC]] Reject of Record type '27' Trailer Group 4 
 
[[NSCC]] Reject of Record type '21' Header Group 5 
[[NSCC]] Reject of Record type '25' Summary 1 
[[NSCC]] Reject of Record type '25' Summary 2 
[[NSCC]] Reject of Record type '25' Summary 3 
[[NSCC]] Reject of Record type '25' Summary n-1 
[[NSCC]] Reject of Record type '25' Summary n 
[[NSCC]] Reject of Record type '27' Trailer Group 5 
 
[[NSCC]] Reject of Record type '21' Header Group 6 
[[NSCC]] Reject of Record type '24' Detail 1 
[[NSCC]] Reject of Record type '24' Detail 2 
[[NSCC]] Reject of Record type '24' Detail n-1 
[[NSCC]] Reject of Record type '24' Detail n 
[[NSCC]] Reject of Record type '25 Summary 1 
[[NSCC]] Reject of Record type '25 Summary 2 
[[NSCC]] Reject of Record type '25 Summary 3 
[[NSCC]] Reject of Record type '25 Summary n-1 
[[NSCC]] Reject of Record type '25 Summary n 
[[NSCC]] Reject of Record type '27' Trailer Group 6 
Record type '29' Grand Total Trailer 
Datatrak Trailer Trailer Group 
 

---

## Page 54

Standardized Data Reporting Technical Guide 
System Processing 54 
1. An error in format within the Header or Trailer results in an [[NSCC]] reject for all records from the header to 
the trailer (including header and trailer). 
2. Trailers may be used by Participants to validate the number of records; however, [[NSCC]] does NOT 
reject "group" records if the respective trailer information does not match the actual records 
submitted. [[NSCC]] only rejects for invalid format and syntax. See also "Header and Trailer 
Validation." 
3. [[NSCC]] modifies the trailer record being sent to the fund to include the number of accepted and 
rejected summary/detail records. This allows the fund to know whether they received a complete 
set of data for their data request. 
[[NSCC]] Data and File Sorting 
[[NSCC]] does not require nor validate any particular sorting order on the input files submitted to [[NSCC]]. However, 
[[NSCC]] does sort the output to the recipients based on the following criteria:  
1. Recipient Number 
2. Recipient Type 
3. Security Issue [[ID]] 
4. SDR Control Number 
5. Record Type within a group (i.e., within a header and trailer group) 
Guidelines for User Search Criteria and Data Sorting 
The criteria and sorting order that is used by the firms in performing the search on their systems is shown 
below. This same order should be used to submit the information to [[NSCC]]. This is only a guidelin e and is not 
enforced by [[NSCC]]. See above, for [[NSCC]] Sorting. 
1. Fund/Security Issue [[ID]] 
2. Account Identifier–The lowest level account identified from the following fields are to be used.  
• Fund Account Number or Firm Account Number 
• Plan [[ID]] or [[investor]] Omnibus Account Number 
• SSN/TIN 
For example, if a fund account number is provided and represents a super omnibus account number, and 
a Plan [[ID]] is also provided, then the Plan [[ID]] within the position is used. Only the [[participant]] level 
transactions for that Plan [[ID]] is provided. 
Another example is when a fund account number is provided and represents a Plan and an SSN 
representing a [[participant]] or contract holder is also provided. In this example, the SSN within the Plan is 
used and only the activity for the single [[participant]] is provided. 
3. NAV Date or Trade Date 
The date on which a net [[Asset]] value for a mutual fund security is calculated. Some systems [[DO]] not contain 
a NAV date field. The process date or trade date is equal to NAV date. 
 
 
 
 

---

## Page 55

Standardized Data Reporting Technical Guide 
System Processing 55 
4.  Transaction Type 
The query on the firm's systems should result in Summary data or Detail data sorted with the following 
sample structure: 
 
Firm/Fund/Security Issue [[ID]] 
Super Omnibus Fund Account Number/Plan [[ID]] or [[investor]] Omnibus Account Number 
 
SSN/TIN (Shareholder 1) 
Trade Date 1 
Trans Type (Buy) 
Trans Type (Sell) 
... 
Trade Date 2 
Trans Type (Buy) 
Trans Type (Sell) 
 
SSN/TIN (Shareholder 2) 
Trade Date 1 
Trans Type (Buy) 
Trans Type (Sell) 
... 
Trade Date 2 
Trans Type (Buy) 
Trans Type (Sell) 
Field Definitions 
SDR Inquiry Request Data (Sent by Funds to Firms) 
The format for the fund request input file/message is the same for all requests, but different data is necessary 
based on the requests. The request types indicate which additional data field is used to refine the queries that 
the firm runs on their database to extract data. Additional search criteria may also be included such as 
threshold amount, Security Issue [[ID]], and transaction type. 
The data that may be found on the request include the data elements outlined in the table below:  

---

## Page 56

Standardized Data Reporting Technical Guide 
System Processing 56 
 
Data Element Definition/Comments 
SDR Control Number Algorithm = ppppyjjjnnnnnnn 
• pppp = Fund’s [[participant]] Number 
• y = Last digit of year 
• jjj = Julian Date 
• nnnnnnn = Unique sequential number assigned by fund 
Request Type Required. Identifies the request or response type with the corresponding data. 
• 01 = Fund Account Level 
• 02 = Plan Level 
• 03 = [[investor]] Omnibus Account Level 
• 04 = Fund/SERV Control Number Request 
• 05 = Rep Level 
• 06 = Stop Recurring 
Fund Number 4 A/N. Required. Requesting Fund’s [[NSCC]] [[participant]] Number. 
Firm Number 4 A/N. Required. Target Firm’s [[NSCC]] [[participant]] Number. 
Underlying Firm 4 A/N. Optional. 
The Firm Number field above may be a first-tier [[intermediary]] and the 
Underlying Firm would then be the second-tier [[intermediary]]; 
- OR - 
The Firm Number may be a Service Provider’s [[NSCC]] [[participant]] Number, 
and the Underlying Firm would be the first or second-tier [[intermediary]]’s [[ID]] 
number (that is using a service provider for the purpose of supporting the SDR 
functionality.) The underlying Firm’s number may be the [[NSCC]] [[Member]] or 
DSO number, the [[OTC]] symbol, or the “UFS Number (Underlying Firm 
Symbol)” see Underlying Firm Indicator 
Underlying Firm Indicator Optional/Conditional. Required when Underlying Firm is provided. 
May be used to qualify the underlying firm identifier that is being used in the 
field above. 
• 01 = [[NSCC]] Number 
• 02 = [[OTC]] Symbol 
• 03 = UFS Number 
Security Issue [[ID]] 9 A/N. Required. Requesting fund’s Security Issue [[ID]] number. Will be used to 
retrieve data for a specific Security Issue [[ID]]. 

---

## Page 57

Standardized Data Reporting Technical Guide 
System Processing 57 
Data Element Definition/Comments 
Recurring Indicator Optional. May be used to request daily data to be sent on an ongoing basis. 
• 0 = No 
• 1 = Yes 
“No” or a space means a one-time request. 
“Yes” means daily data is to be sent indefinitely until a “Stop Recurring” 
request type is sent. 
Note: 
Note that the “From Date” should be the current date; however, the firm 
processes the request as a recurring request beginning on the date that it 
receives the request. 
The account identifiers tell the firm how to find the account in question. The identifiers include fund account number, firm 
account number, plan [[ID]], [[investor]] omnibus account number, and SSN/TIN. 
At minimum, the firm or fund account number is required, but all account identifiers may be provided. When multiple 
fields are provided, the firm should identify the lowest level identifier and provide only that particular level’s data. 
For example, if a fund account number is provided and represents a super omnibus account number, and a Plan [[ID]] is 
also provided, then the Plan [[ID]] within that particular position is used. Only the [[participant]] level transactions for that 
particular Plan [[ID]] are provided. 
Another example is when a fund account number is provided and represents a Plan, and an SSN representing a 
[[participant]] is also provided, then the SSN is used. Only the activity for that single [[participant]] within the designated plan is 
provided 
The identifiers are used in the following manner: 
• Super omnibus accounts are identified only by fund/firm account number. 
• Plan accounts are identified only by fund/firm account number or by plan [[ID]]. 
• [[investor]] Omnibus Accounts are identified only by fund/firm account number or by [[investor]] omnibus 
account number. 
• Participants, shareholders or contract holders are identified by SSN/TIN and Customer Level Account 
Number. 
Fund Account Number 20 A/N. Optional/Conditional. Required if Firm Account Number is not 
provided. Refers to the account number that is set up by the fund. 
Fund account numbers should provide only the core account number; 
and should not include the fund number. The fund number should be 
derived from the Security Issue [[ID]], similar to the numbers used on 
Fund/SERV. 
Firm Account Number (e.g., BIN) 20 A/N. Optional/Conditional. Required if Fund Account Number is not 
provided. Refers to the account number that is set up by the firm. 
Plan [[ID]] 
Should be provided to go to a Plan 
Level. 
20 A/N. Optional/Conditional. Optional unless the SDR request type is 02 
(Plan Level) or 03 ([[investor]] Omnibus Account Level); if so, they (one or the 
other) become required. 
May be used to retrieve data only for a specific plan. Defined as the retirement 
Plan’s [[ID]] as assigned by the recordkeeper. 
[[investor]] Omnibus Account Number 
Should be provided to go to an 
[[investor]] Omnibus Account Level. 
20 A/N. Optional/Conditional. Optional unless the SDR request type is 02 
(Plan Level) or 03 ([[investor]] Omnibus Account Level), if so, they (one or the 
other) become required. 

---

## Page 58

Standardized Data Reporting Technical Guide 
System Processing 58 
Data Element Definition/Comments 
May be used to retrieve data only for a specific [[investor]] omnibus account. 
SSN/TIN 
Should be provided to go to a 
specific [[participant]] Level. 
9 N. Optional. Defines the social security number or tax identification number 
of the underlying shareholder. 
From Date mm/dd/ccyy. Required. Current date or earlier date parameter for requested 
data. Defined as the NAV date. 
Should be current date for recurring request. Future-dated requests are 
not allowed; however, [[NSCC]] does not validate the date field. See also 
Recurring Indicator. 
To Date mm/dd/ccyy. Optional. Later date parameter for requested data. Defined as 
the NAV date. 
Transaction Type Optional. May be used to retrieve data only for a specific transaction type. 
Defines the transaction that the underlying shareholder has requested on the 
account. The transaction types are limited to: 
• 01 = Buy  
• 2 = Sell 
Transactions are assumed to be Category 1 transaction types as defined 
earlier in this paper, unless otherwise specified. See “Category 1 and 
Category 2 Transactions” in the SDR User Guide Best Practices document on 
the learning center at https://dtcclearning.com/products-and-services/mutual-
fund-services/networking/standardized-data-reporting-sdr.html 
A Space means that the query is for all available transactions, which would 
include transfers. 
Threshold Amount 999,999,999. Optional. May be used to retrieve data only with a minimum net 
money amount. 
Generally defined as gross but recordkeepers may only be storing net 
amounts. 
Includes Category 2 Transactions (Y/N) Optional. May be used to retrieve both Category 1 and Category 2 data. 
“0” is requesting the Category 1 transactions only ([[default]]) 
“1” is requesting all transactions (i.e., both Category 1 and Category 2 
transactions.) 
• 0 = No 
• 1 = Yes 
Category 2 transactions may only be retrieved along with Category 1 
transactions. Category 2 transactions cannot be requested separately. 
SPACE is considered 0 = No.  If YES, then Category 2 transactions are 
also provided by the firm (i.e., along with Category 1 transactions). 
Registered Representative (RR) 
Number 
9 A/N. Optional/Conditional. Required when Request Type is 5 = Rep Level. 
Refers to the Registered Rep’s number. Equivalent to the number that would 
be sent via Fund/SERV. 
RR Branch 9 A/N. Optional. Branch [[ID]] to which the RR is associated. 

---

## Page 59

Standardized Data Reporting Technical Guide 
System Processing 59 
Data Element Definition/Comments 
RR Firm 
(Not Clearing/Correspondent 
Relationship) 
8 A/N. Optional. The [[ID]] number of the dealer to which the RR is associated. 
This field should not be used for the correspondent in a clearing firm 
relationship. Should not be used if the same as Firm Number, described on 
page 56. 
Fund/SERV Control Number 15 A/N. Optional. May be used to retrieve data only for a specific Fund/SERV 
Control Number. 
Original SDR Control Number Optional. May be used for a stop of a recurring request. May also be used in 
the future in situations where original SDR control number is needed. 
Algorithm = ppppyjjjnnnnnnn 
• pppp = Fund’s [[participant]] Number 
• y = Last digit of year 
• jjj = Julian Date 
• nnnnnnn = Unique sequential number assigned by fund 
SDR Acknowledgment Data 
The Acknowledgment is the initial response from the firm to the fund. The acknowledgment is a proactive 
indication from the firm that it has received the request from the fund and is considered the point on which firm 
response time to requests is based. The Acknowledgment may also be used by the firm to indicate the 
approximate amount of time that it takes to generate a data response back to the fund. It contains a number of 
fields that are specific to the record and are described below. 
Data Element Definition/Comments 
Acknowledgment Indicator Required. 
• 0 = Response will be Provided 
• 1 = Request will be Forwarded to the Underlying Firm 
Anticipated Response 
Date 
mmddccyy. Optional. 
Provides the date on which the firm anticipates that the response data will be provided to 
the fund. 
Anticipated Response File 
Frequency 
Optional. Indicates whether the firm provides the data response in a single complete file or 
in multiple partial files, if it can be determined. 
• 01 = Full Response 
• 02 = Partial Response 
Underlying Firm 4 A/N. Optional. 
Provides the underlying firm that may be involved in providing requested data. 
SDR Response Data (Sent by Firms to Funds) 
Firms provide summary data when a request is submitted against a super omnibus account. Detailed 
information may also be sent for individual shareholder accounts that are a part of the s uper omnibus account. 

---

## Page 60

Standardized Data Reporting Technical Guide 
System Processing 60 
Detail response data is expected to be provided on shareholders when a request is made against specific 
plans, [[investor]] omnibus accounts, or individuals specified by the SSN. 
The table below, Response Data Definitions, shows data that may be sent by the firm to the fund through 
[[NSCC]]. Files sent on a regular daily schedule are requested manually by the fund; but may be sent using SDR. 
Note: 
This table does not provide data elements for summary data.  
The summary data provides sufficient information to help the funds identify specific plans or [[investor]] omnibus 
accounts where trading is occurring frequently. The fund would then be able to request data at a plan level or 
[[investor]] omnibus account level and obtain detailed information about the underlying participants/shareholders. 
 Response Data Definitions 
Data Elements Definition/Comments 
This is the high-level data that identifies the request from the fund (SDR Control Number) and the account to 
which the data belongs. For retirement accounts, multiple plans and/or participants may exist under a single 
account. 
SDR Control Number Required. 
This is the control number assigned by the fund. See SDR Control Number in Request 
Data Definitions. 
Or, this is the same as the SDR Response Number (see below) for a response provided 
against a request made outside of [[NSCC]]. 
SDR Response Number Required. 
Algorithm = ppppyjjjnnnnnnn 
• pppp = Firm’s [[participant]] Number 
• y = Last digit of year 
• jjj = Julian Date 
• nnnnnnn = Unique sequential number assigned by firm 
Used to identify the SDR response, either to an SDR request via [[NSCC]] or a request done 
ex-[[NSCC]]. 
Response Type Required. Immediately identifies the level of data. 
• 01= Summary Level 
• 02 = Detail Level 
• 03 = Both Summary and Detail 
The record layout field also includes the following to identify acknowledgments and 
rejects. 
• 04 = Acknowledgment 
• 05 = Firm Reject 
Fund Number 4 A/N. Required. Fund’s [[NSCC]] [[participant]] Number. 
Firm Number 4 A/N. Required. Firm’s [[NSCC]] [[participant]] Number. 

---

## Page 61

Standardized Data Reporting Technical Guide 
System Processing 61 
Data Elements Definition/Comments 
Underlying Firm 4 A/N. Optional. 
The Firm Number field above may be a first-tier [[intermediary]] and the underlying firm 
would then be the second-tier [[intermediary]]; 
- OR - 
The Firm Number may be a service provider’s [[NSCC]] [[participant]] Number, and the 
Underlying Firm would be the first or second-tier [[intermediary]]’s [[ID]] number (that is using a 
service provider for the purpose of supporting the SDR functionality.) 
The underlying firm’s number may be the [[NSCC]] [[Member]] or DSO number, the [[OTC]] 
symbol, or the “UFS Number”. See Underlying Firm Indicator. 
Underlying Firm Indicator Optional/Conditional. Required when Underlying Firm is provided. 
May be used to qualify the underlying firm identifier that is being used in the field above. 
• 01 = [[NSCC]] Number 
• 02 = [[OTC]] Symbol 
• 03 = UFS Number (Standard number for trusts and recordkeepers. Assigned and 
maintained by the [[NSCC]]. The list of intermediaries and UFS identifiers are 
available in the Mutual Fund Services section on dtcclearning.com. 
Fund Account Number 20 A/N. Optional/Conditional. Required if Firm Account Number is not provided. Refers to 
the account number that is set up by the fund. 
Firm Account Number (e.g., 
BIN) 
20 A/N. Optional/Conditional. Required if Fund Account Number is not provided. Refers to 
the account number that is set up by the firm. 
Security Issue [[ID]] (From/Sell 
Side on Exchange) 
9 A/N. Required. 
Partial Response Indicator Optional. Used to identify whether the file provides complete information for a data 
request. 
• 0 = Full Response/Final Response 
• 1 = Partial Response 
• 2 = Incomplete Response/Final Response 
Space will be considered 0 = Full Response. 
• 0 = Full/Final Response means the file is a full response to a request, or the last of 
multiple files that have been previously sent. The multiple files will come when 
firms respond to a request with large data by sending multiple files. 
• 1 = Partial Response means there will be additional files to come. May be used for 
a recurring file. 
• 2 = Incomplete response means the firm has provided some information but 
cannot provide a complete response to satisfy the request. 
Note: 
Responses to recurring requests are not followed by a “final response” indicator 
because the firm would stop sending the data. The firm is not able to know that a 
file is final until they receive a Stop Recurring request from the fund. 

---

## Page 62

Standardized Data Reporting Technical Guide 
System Processing 62 
Data Elements Definition/Comments 
This is the transaction activity data, which is generally sorted at the highest account level (e.g., Plan [[ID]]), then at 
the [[participant]] level (e.g., SSN/TIN), then trade date (if multiple are requested), and finally by transaction type. 
This record is repeated for each of the sort criteria (e.g., Plan [[ID]]), when more than one plan exists for the fund 
account. 
Regardless of the request type, the sort on the data sent to the fund should be the same so that the same file 
layouts may be used. 
Plan [[ID]] 20 A/N. Optional/Conditional. Required if [[investor]] Omnibus Account Number is not 
provided. Plan’s [[ID]] as assigned by the recordkeeper. 
Plan Name 35 A/N. Optional. Retirement plan’s name. 
[[investor]] Omnibus Account 
Number 
20 A/N. Optional/Conditional. Required if Plan [[ID]] is not provided. This is the account 
number for the [[investor]] omnibus account, as assigned by the firm. 
SSN/TIN 9 N. Required. Defines the social security number or tax identification number of the 
underlying shareholder. 
SSN/TIN Indicator Required with SSN/TIN. This indicator is equivalent to the indicator found on Fund/SERV. 
The values include: 
• 1 = TIN 
• 2 = SSN 
• 3 = [[investor]]’s TIN 
Customer Name 35 A/N. Optional. The customer name refers to the SSN/TIN that is provided. 
Customer Level Account 
Number 
30 A/N. Optional. The customer level account number is the [[participant]], 
contract/policyholder, or BIN number at the [[investor]] level. The customer level account 
number may be used in combination with the source system [[ID]] to identify the transactions 
for the specific individual within the designated system or platform. 
Source System [[ID]] 10 A/N. Optional. The system [[ID]] identifies the source system or platform in which the 
activity has occurred and has been recorded. The source system [[ID]] may be used in 
combination with the customer level account number to identify the transactions for the 
specific individual within the designated system or platform. 
NAV Date mm/dd/ccyy. Required. Date of NAV pricing for the transaction. 
Contra Security Issue [[ID]] 
(To/Buy Side on Exchange) 
9 A/N. Optional on Exchanges. 
Transaction Type Required. Defines the transaction that the underlying shareholder has requested on the 
account. The transaction types are limited to: 
• 01 = Buy 
• 02 = Sell 
• 03 = Exchange (Intra-Fund Buy Side) 
• 04 = Exchange (Intra-Fund Sell Side) 
• 05 = Transfer In 
• 06 = Transfer Out 
Transactions are assumed to be Category 1 transaction types as defined earlier in this 
paper, unless otherwise specified. See “Category 1 and Category 2 Transactions” in 
Section V for examples of the respective transactions. 

---

## Page 63

Standardized Data Reporting Technical Guide 
System Processing 63 
Data Elements Definition/Comments 
Transaction Code Optional. Used to indicate detailed/specific transaction codes that fall under the 
respective Transaction Types. 
See list in Record Layouts or SDR User Guide Best Practices documents in the learning 
center on the Learning Center. 
Trade Net Amount Due 99,999,999,999,999.99. Optional/Conditional. The net amount that was settled for the 
trade. Optional if Transaction Type = 05, or if Transaction Code = 7 or 52. 
Trade Share Amount 9,999,999,999.9999. Required. 
Share Amount is not maintained on recordkeeping systems for insurance [[Companies]]. In 
those instances, AUV or unit value should be provided and unit value indicator field 
should be flagged. 
Unit Value Indicator Optional. Used to indicate whether the trade share amount represents [[shares]] or units. 
• Space or 0 = [[shares]] 
• 1 = Units 
Price on Trade 999,999.999999. Optional/Conditional. Defined as the price applied to the particular trade. 
Optional if Transaction Type = 05, or if Transaction Code = 7 or 52. 
STR Fee Amount 999,999.99. Optional. Defines the Short-Term Redemption fee paid on a transaction. 
Indicates whether or not fees are being assessed by the recordkeeper/firm. 
CDSC Amount 999,999.99. 
Optional. Defines the Contingent Deferred Sales Charge paid on a transaction. 
Transaction [[ID]] 20 A/N. Optional. E.g., Record-keeper transaction/reference [[ID]] number. 
RR Number 9 A/N. Optional. Registered rep’s number. Equivalent to number that would be sent via 
Fund/SERV. 
RR Branch 9 A/N. Optional. Branch [[ID]] to which the RR is associated. 
RR Firm 
(Not 
Clearing/Correspondent 
Relationship) 
8 A/N. Optional. The [[ID]] number of the dealer to which the RR is associated. This field 
should not be used for the correspondent in a clearing firm relationship. Should not be 
used if the same as Firm Number, described on page 57. 
Agent for Firm Number 4 A/N. Optional. The introducing firm or correspondent if a clearing relationship exists. 
This firm is the middle-level firm between the [[intermediary]] and the RR firm. For 
example, on a super omnibus account, XYZ Firm controls the super omnibus 
account and processes for AZ123 Clearing (who is the agent for firm). The agent for 
firm then clears for the RR firm (e.g., ABC Advisors). 
Transaction Category Required. Indicates whether the transaction is Category 1 or Category 2. See User Guide 
for list and definitions of transactions, and their category classification. 
• 1 = Category 1 
• 2 = Category 2 
Transaction Source Optional. Defines the source that directed the transaction. 
• 0 = [[participant]]/Shareholder 
• 1 = Plan/Administrator 
• 2 = Rep 
• 3 = Firm Cannot Differentiate 

---

## Page 64

Standardized Data Reporting Technical Guide 
System Processing 64 
Data Elements Definition/Comments 
• 4 = Recordkeeper or Insurance Carrier 
Correction Indicator Optional. 
• 0 = Regular File 
• 1 = Correction File 
The correction indicator value of ‘1’ (correction file) is only used to correct an 
entire file of data that was previously sent by the Firm. The correction indicator 
applies to the response for a particular SDR request, identified by a control number 
(and ideally SDR Response Number) for a particular date (e.g., for historical or 
recurring). 
The records contained within this Main Header should replace and overwrite the 
original records. 
Space is considered 0 = Regular File. 
Reject Codes and Validation Rules 
Reject Codes 
[[NSCC]] may reject records that [[DO]] not comply with the record layouts and the validation rules contained within 
the layouts. Firms may also reject the data requests from the funds for various reasons. Reject codes and 
descriptions that may be used by [[NSCC]] and Firms in the SDR system can be found in the Standardized Data 
Reporting section of the learning center. 
Select Validation Rules 
A number of validation rules are provided below to help users in understanding certain [[NSCC]] SDR processing.  
Control Number and Reminder Process 
• [[NSCC]] will edit the control number from the fund so that it starts with the submitting fund number.  
• If a request was not acknowledged or rejected, [[NSCC]] will send out reminders.  
• The reminders will continue for a period of up to 10 days or until an acknowledgment or reject is 
submitted, whichever comes first. Detail or Summary records [[DO]] not turn off reminders. 
• [[NSCC]] will check the control number, fund number, and firm number on the acknowledgement/ reject in 
order to match it up to a request. 
• This will allow [[NSCC]] to identify "unmatched" requests, which will trigger a Reminder.  
• If there is a match of a control number, but the related information does not match (e.g., fund number and 
firm number), then [[NSCC]] will reject the acknowledgement/ reject. A Reminder will then be sent for that 
control number. 
Note: 
[[NSCC]] will not check the control number coming from the firm on the detail response record because this response 
could be from a request that occurred outside of the service. 

---

## Page 65

Standardized Data Reporting Technical Guide 
System Processing 65 
Fund, Firm, and Underlying Firm 
• Firm and fund must be on the Networking [[participant]] master. 
• The underlying firm on the Request record will not be validated. 
• An underlying firm can respond directly to a request as long as the underlying firm is val [[ID]] on the 
Networking [[participant]] master. 
• If the fund specifies the underlying firm on the request, then [[NSCC]] will check to see if a submitting 
underlying firm is the same as on the fund request, as long as the request information still resides on the 
[[NSCC]] database. 
Note: 
The original information will be deleted from the database when the control number for a request has been matched 
up to an Acknowledgment or Reject record. 
• If a firm submits data and puts the underlying firm number in the record as informat ion, [[NSCC]] will not edit 
that underlying firm number. 
• [[NSCC]] will not route to all three parties. [[NSCC]] will only route to the primary destination, e.g., fund to firm, 
firm to fund, or underlying firm to fund. 
Header and Trailer 
• If Header (21) is rejected, the whole group will be rejected. Records in the group other than the Header 
(21) will be assigned reject code 84 = Header Record Missing or Invalid. No other editing will be 
performed on records in the group. 
• If Trailer (27) is rejected, the whole group will be rejected. Records in the group which would have been 
otherwise accepted will be assigned reject code 85 = Trailer Record Missing or Invalid.  
• In addition to syntax checking (as described in the layout document), Trailer (27) will be rejected if the 
value in field Total Records does not match the total records in the group as calculated by the program.  
• Counters on the Trailer (27), other than Total Records, will not be compared to the number of records of 
that type in the group. In other words, Trailer (27) will not be rejected if counters other than Total Records 
[[DO]] not match the number of records of that type in the group. 
• When at least one record between Header (21) and Trailer (27) is rejected (while the whole group is not 
rejected as described above), a new Header (21) and Trailer (27) will be created in order to send the 
rejected records as a group back to the submitting firm. 
• When Header (21) and Trailer (27) are accepted but all the records in between are rejected, an "empty 
group" (Header and Trailer with no record in between) will be sent to the fund. 
Note: 
This is the practice in other Networking group data (such as [[Dividend]] and Position). 
Records between Header and Trailer 
• Only one Firm Reject (23) is allowed between Header (21) and Trailer (27). No other record is allowed 
between Header (21) and Trailer (27) if Firm Reject (23) is supplied. 

---

## Page 66

Standardized Data Reporting Technical Guide 
System Processing 66 
• Only one Acknowledgement (22) is allowed between Header (21) and Trailer (27).  No other record is 
allowed between Header (21) and Trailer (27) if Acknowledgement (22) is supplied. 
• Multiple Details (24) and Summaries (25) are allowed between Header (21) and Trailer (27).  
• Only one Acknowledgement (22) is allowed between Header (21) and Trailer (27).  No other record is 
allowed between Header (21) and Trailer (27) if Acknowledgement (22) is supplied. 
• When more than one Acknowledgment (22) is provided between Header (21) and Trailer (27), the first 
valid Acknowledgement (22) will be accepted and the rest will be rejected by [[NSCC]]  
• Only one Firm Reject (23) is allowed between Header (21) and Trailer (27). No other record is allowed 
between Header (21) and Trailer (27) if Firm Reject (23) is supplied. 
• When more than one Reject (23) is provided between Header (21) and Trailer (27), the first valid Reject 
(23) will be accepted and the rest will be rejected by [[NSCC]]. 
• Multiple Details (24) and Summaries (25) are allowed between Header (21) and Trailer (27). 
• Record types between Header (21) and Trailer (27) must correspond to field Response Type on Header 
(21). Record types that [[DO]] not correspond to Response Type will be rejected.  For example, Summary 
records (25) will be rejected if Response Type = 02 (Detail level). 

---

## Page 67

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 