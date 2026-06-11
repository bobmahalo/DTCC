---
title: "mfs293_Invoicing_and_Fee_Settlement_20230727.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs293_Invoicing_and_Fee_Settlement_20230727.pdf"
pages: 68
size: "765.1 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# mfs293_Invoicing_and_Fee_Settlement_20230727.pdf

**Original File:** [mfs293_Invoicing_and_Fee_Settlement_20230727.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs293_Invoicing_and_Fee_Settlement_20230727.pdf)  
**Category:** Rules  
**Total Pages:** 68  
**File Size:** 765.1 KB  

---

## Page 1

 
 
 
Payment aXis 
INVOICING AND FEE [[settlement]] RECORD 
LAYOUTS 
JULY 27, 2023 
 

---

## Page 2

TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 4 
List of Reject and Modification Codes for Invoicing and Fee [[settlement]] ...................................................... 5 
Networking Reject Codes (to be used by [[NSCC]] only) ....................................................................................... 5 
Invoicing and Fee [[settlement]] Reject Codes (to be used by [[NSCC]] only)  .......................................................... 6 
Reject Codes to be Used by Funds to Reject/Partially Reject [[Broker]] Initiated Invoices (for Fee Types = 50, 55, 
56, 57) ................................................................................................................................................................. 7 
Modification Reason Codes to be Used by Funds to Modify [[Broker]] Initiated Invoices (for Fee Types = 55, 56, 
57) ....................................................................................................................................................................... 8 
File Overview ........................................................................................................................................................ 9 
Record Layouts .................................................................................................................................................. 11 
Invoicing and Fee [[settlement]] ........................................................................................................................... 12 
Header Record (A*/B/F/T* 41 sequence 1) ......................................................................................................12 
Header Record (A*/B/F/T* 41 sequence 2) ......................................................................................................17 
Invoicing and Fee [[settlement]] ........................................................................................................................... 20 
Account Detail Record (A*/B/F/T* 42 sequence 1) ...........................................................................................20 
Account Detail Record (A*/B/F/T* 42 sequence 2) ...........................................................................................23 
Underlying Account Detail Record (A*/B/F/T* 42 sequence 3) ........................................................................26 
Retirement/Bank Trust Account Detail Record (A*/B/F/T* 42 sequence 4)......................................................27 
Retirement/Bank Trust Account Detail Record (A*/B/F/T* 42 sequence 5)......................................................31 
Invoicing and Fee [[settlement]] ........................................................................................................................... 32 
Detail Summary Record (A*/B/F/T* 43 sequence 1) ........................................................................................32 
Detail Summary Record (A*/B/F/T* 43 sequence 2) ........................................................................................35 
Detail Summary Record (A*/B/F/T* 43 sequence 3) ........................................................................................38 
Detail Summary Record (A*/B/F/T* 43 sequence 4) ........................................................................................42 
Invoicing and Fee [[settlement]] ........................................................................................................................... 43 
Invoice Summary Record (A*/B/F/T* 44 sequence 1) ......................................................................................43 
Invoice Summary Record (A*/B/F/T* 44 sequence 2) ......................................................................................45 
Invoice Summary Record (A*/B/F/T* 44 sequence 3) ......................................................................................46 
Invoicing and Fee [[settlement]] DataTrak Records ........................................................................................... 48 

---

## Page 3

 
 
DataTrak Header Record ..................................................................................................................................48 
DataTrak Trailer Record ...................................................................................................................................49 
Invoicing and Fee [[settlement]] Output Records ............................................................................................... 50 
Service Output Header Record (N00)...............................................................................................................50 
Input Acknowledgment Record (NOM) .............................................................................................................51 
Total Trailer Record (N46) ................................................................................................................................52 
Grand Total Trailer Record (N47) .....................................................................................................................53 
Mutual Fund [[DTCC]] Payment aXis [[settlement]] Records 38, 39, 40 ................................................................ 54 
Output from [[NSCC]] to Firms and Funds............................................................................................................54 
APPENDIX – Summary of Changes .................................................................................................................. 55 
Summary of Changes – effective Q3, 2020 ......................................................................................................56 
Summary of Changes – effective Q1, 2019 ......................................................................................................57 
Summary of Changes – effective Q3, 2015 ......................................................................................................58 
Summary of Changes – effective Q4, 2014 ......................................................................................................61 
Summary of Changes – effective Q1, 2013 ......................................................................................................67 
 

---

## Page 4

Invoicing and Fee [[settlement]] Record Layouts 
History of Important Notices 4 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes 
Effective Date Important Notices 
July 27, 2023 • Summary of Changes has been moved to back of 
document. 
• Record has been rebranded and content reviewed. 
July 7, 2020  Documentation update 
Effective Date: March 25, 2019 Please see Important Notice a8658 P&S 8233 Dated December 
19, 2018 
April 28, 2016 Added the File Overview, Record Sequence Order & Record 
Layout references.  See Table of Contents. 
Effective Date: July 27, 2015 Please see Important Notice a7997  P&S 7572 
Dated March 12, 2015 
Effective Date: November 24, 2014 Please see Important Notice a7885  P&S 7455 
Dated August 18, 2014 
Effective Date: February 11, 2013 Please see Important Notice a7567  P&S 7137  
Dated January 9, 2013 
Please see Important Notice a7512  P&S 7082  
Dated October 24, 2012 
Effective Date: February 11, 2013 Please see Important Notice a7464  P&S 7034 
Dated July 31, 2012 
 
 
 
 
  

---

## Page 5

Invoicing and Fee [[settlement]] Record Layouts 
List of Reject and Modification Codes for Invoicing and Fee [[settlement]] 5 
LIST OF REJECT AND MODIFICATION CODES FOR 
INVOICING AND FEE [[settlement]] 
Networking Reject Codes (to be used by [[NSCC]] only) 
Reject Code Description 
01 System Code missing/invalid 
02 Record Type missing/invalid 
04 Clearing Settling Fund Number missing/invalid 
05 Fund [[CUSIP]] Number missing/invalid 
13 Header Record missing/invalid 
15 Networking Control Indicator missing/invalid 
29 Fee Type missing/invalid 
37 Sequence Number missing/invalid 
41 Debit/Credit Indicator missing/invalid 
54 Processing Date missing/invalid     
58 Additional Input Required for this Input Type 
B6 [[settlement]] Indicator missing/invalid 
C3 Trade Date missing/invalid 
D8 Dollar Amount missing/invalid   
F4 Receiving Firm Clearing/Settling Number missing 
F9 Membership Identifier invalid                                                       
G0 TPA /Investment Agent Number missing/invalid 
I1 Firm/Fund Identification Indicator missing/invalid 
I2 Delivering Firm Number missing/invalid 
K2 Date field has invalid date format 
M6 Detail Record is missing /invalid 
X8 [[participant]] is not valid for the Submitter and/or Product 
 
 

---

## Page 6

Invoicing and Fee [[settlement]] Record Layouts 
List of Reject and Modification Codes for Invoicing and Fee [[settlement]] 6 
Invoicing and Fee [[settlement]] Reject Codes (to be used by [[NSCC]] only) 
New Reject Code Description 
N5 Structure of record sequences is incorrect for provided fee type    
N6 Omnibus Account Number is missing  
N7 Period Start Date is missing/invalid                             
N8 Period End Date is missing/invalid                             
N9 Anticipated [[settlement]] Date is invalid                             
O0 Invoiced / [[settlement]] Amount is missing/invalid                             
O1 Underlying BIN is missing                            
O2 Rate is missing/invalid/duplicate                             
O3 Sub-Accounting Eligible Assets is missing/invalid              
O4 Sub-Accounting Ineligible Assets is missing/invalid        
O5 Sub-Accounting Excluded Assets is missing/invalid           
O6 Sub-Accounting Balance is missing/invalid                          
O7 Process Date of Trade is missing/invalid                             
O8 Sub–Account Transaction Amount is missing/invalid                             
O9 Sub-Account Trade Control Number is missing/invalid                             
P0 [[Asset]] Calculation Method is missing/invalid 
P1 Deliverer Reject Indicator is missing/invalid                             
P2 Deliverer Reject Code is invalid     
P3 Invoice Initiator is missing/invalid                  
P4 [[Asset]] Type is invalid                       
P5 Fund Account Number is missing                         
P6 Underlying Customer Type is invalid                            
P7 Number of Rates in Details does not correspond to Number of Rates in a Header 
P8 Deliverer Reject code is missing on Rejected Invoice  
P9 Omni Invoice Summary Record is missing/invalid 
Q0 Control Number is missing 
Q1 Confirm/Reject Code Indicator is missing/invalid 

---

## Page 7

Invoicing and Fee [[settlement]] Record Layouts 
List of Reject and Modification Codes for Invoicing and Fee [[settlement]] 7 
New Reject Code Description 
Q2 Number of Rates is missing/invalid 
Q3 Submitting [[participant]] is not eligible for this service 
V3 Modification Indicator is missing/invalid 
V4 Modification Reason Code is missing/invalid 
V5 Detail Record [[ID]] is missing/invalid 
V6 Eligible [[participant]] Count is missing/ invalid 
V7 Ineligible [[participant]] Count is invalid 
V8 Rate Type is missing/invalid 
V9 Rate Category is missing/invalid 
W0 Invalid Confirm/Reject and Deliverer Reject Indicator Combination 
W1 Number of Eligible Positions is missing/invalid 
W2 Number of Ineligible Positions is invalid 
W3 Eligible Assets missing/invalid 
W4 Ineligible Assets missing/invalid 
W5 Detail Summary Record [[ID]] is missing/invalid 
W6 Invalid Confirm/Reject and Modification Indicator Combination 
W7 Invalid Confirm/Reject and [[settlement]] Indicator Combination 
X8 [[participant]] is not valid for the Submitter and/or Product 
 
Reject Codes to be Used by Funds to Reject/Partially Reject [[Broker]] 
Initiated Invoices (for Fee Types = 50, 55, 56, 57) 
Codes to be used by Funds to reject [[Broker]]-initiated Omni Invoices for Fee Type = 50, 55, 56, 57 
[[OA]] Duplicate Invoice 
OB Invalid Rate 
OC [[Asset]] Value Invalid 
OD [[Asset]] Calculation Method Invalid 
OE Ineligible [[CUSIP]] 

---

## Page 8

Invoicing and Fee [[settlement]] Record Layouts 
List of Reject and Modification Codes for Invoicing and Fee [[settlement]] 8 
Codes to be used by Funds to reject [[Broker]]-initiated Omni Invoices for Fee Type = 50, 55, 56, 57 
OF Unauthorized Firm Invoice 
OG Incorrect Period 
OH Invalid Omnibus Account Number 
OI Invalid Debit/Credit Indicator 
 
Modification Reason Codes to be Used by Funds to Modify [[Broker]] 
Initiated Invoices (for Fee Types = 55, 56, 57) 
Codes to be used by Funds to modify [[Broker]]-initiated Invoices for Fee Types = 55, 56, 57 
MA Invalid Rate 
MB [[Asset]] Value Invalid 
MC [[Asset]] Calculation Method Invalid 
MD Incorrect Period 
ME Invalid Debit/Credit Indicator 
MF Incorrect Calculation 
MG Incorrect Payee 
MH Incorrect Positions 
 
 
  

---

## Page 9

Invoicing and Fee [[settlement]] Record Layouts 
File Overview 9 
FILE OVERVIEW 
1. The [[DTCC]] Payment aXis - Invoicing and Fee [[settlement]] records are fixed and 100 bytes. 
2. Files can be submitted to [[NSCC]] by a Delivering Firm for a Fund (System Code = B) or by a Delivering 
Fund for a Receiving Firm (System Code = F). 
3. Firms and Funds must program to transmit files to [[NSCC]] (DataTrak) and must also program to receive 
files from [[NSCC]] (AutoRoute): 
a. Delivering Firm (System Code = B)  or Fund (System Code = F) must program to transmit files to 
[[NSCC]] (DataTrak 26947) and must also program to receive files from [[NSCC]] via:  
• AutoRoute 02101947 – to receive back the [[NSCC]] Acknowledgement records (NOM) and 
[[NSCC]] rejected records; 
• AutoRoute 02102203 – to receive [[settlement]] data. 
b. Receiving Firm (System Code = F) or Fund (System Code = B) must program to receive files from 
[[NSCC]] via: 
• AutoRoute 02101947 – to receive accepted by [[NSCC]] files submitted by a Delivering Firm 
(System Code = B) or by a Fund (System Code = F); 
• AutoRoute 02102203 – to receive [[settlement]] data. 
4. Based on a Fee Type, multiple Detail Records (B/F42) and/or Detail Summary Records (B/F43) can be 
sent in one invoice.  These records will be defined, per grouping, between the Invoice header (B/F 41) and 
the Invoice Summary (B/F 44) records.   
5. [[NSCC]] will create: 
a. For a Delivering Firm or Fund - an Acknowledgement (NOM) and the Grand Total Trailer Record 
(N47) to recap all records included in the [[NSCC]] output File. 
b. For a Receiving Firm or Fund – a Total Trailer Record (N46) to recap all records received from 
counterparties, the Grand Total Trailer Record (N47) to recap all records included in the [[NSCC]] 
output File. 
6. For the Invoicing and Fee [[settlement]] [[NSCC]] will create [[DTCC]] Payment aXis [[settlement]] Records 38, 39 
and 40 for both – the Delivering Firm/Fund and the Receiving Firm/Fund - and transmit them via the 
AutoRoute 02102203. 
 
Invoice Structure and Record Sequence Order 
System    
Code 
Fee 
Type 
Header - 
41 Detail  - 42 Detail Summary - 43 Trailer - 44 
Seq
1 
Seq
2 
Seq
1 
Seq
2 
Seq
3 
Seq
4 
Seq
5 
Seq
1 
Seq
2 
Seq
3 
Seq
4 
Seq
1 
Seq
2 
Seq
3 
B/F 50 R R O OC X X X R R X X R R X 
B 51 R R R X R X X R X X X R X X 
B 52 R R R X R X X R X X X R X X 
B 53 R R R X R X X R X X X R X X 

---

## Page 10

Invoicing and Fee [[settlement]] Record Layouts 
File Overview 10 
 
B 54 R R R X R X X R X X X R X X 
B/F 55 R R X X X X X R R R X R R R 
B 56 R R R R X R OC R R R OC R X X 
F 56 R R OC OC X OC OC R R R OC R X X 
B/F 57 R R X X X X X R R R X R X R 

---

## Page 11

Invoicing and Fee [[settlement]] Record Layouts 
Record Layouts 11 
RECORD LAYOUTS 
The column headings are as follows:  
Field Name - The name of the field. 
Start - The position in which the field starts 
End - The position in which the field ends 
Len - The length of the field in bytes 
Type - The type of the field:  
  A/N = Alphanumeric  
  N = Numeric 
Description - Field description (format, valid values, conditional requirements, etc.). 
Req/Opt - Indicates whether the field is optional or required:  
  O = Optional  
  R = Required  
  OC = Generally optional, but required upon specified conditions  
  RC = Generally required, but optional upon specified conditions 
Reject Code - The Networking & Payment aXis reject code which indicates that this field is invalid. 
 
• Alphanumeric type fields may include any character in the computer character set but  should not include 
unprintable characters such as Low-Value, High-Value, Comp-3 fields, etc., since these kinds of 
characters may cause problems during transmission time.  
• Numeric type fields may include digits (0-9) only.  
• Required fields mean the following: 
o Fields with specified list of values must have one of those values.  
o Alphanumeric type fields without specified list of values may have any value as described in the first 
note above but must not be spaces.  
o Numeric type fields without a specified list of values must be numeric greater than zero.  
o Fields with other requirements must follow these requirements (for example Submitting [[participant]] 
Number must be valid and eligible for Networking).  
 
• Optional fields mean the following:  
o Fields with specified list of values must have one of those values or space.  
o Alphanumeric type fields without specified list of values may have any value as described in the first 
note above.  
o Numeric type fields without specified list of values must be numeric or space.  
o Fields with other requirements must follow these requirements or may be space.  
 
• All dates are in MMDDCCYY format. (March 15, 2023, for example, would be represented as 03152023) 
 

---

## Page 12

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 12 
INVOICING AND FEE [[settlement]] 
Header Record (A*/B/F/T* 41 sequence 1) 
Required on Input /Output  
Note:   
This Record A*/B/F/T* 41 sequence 1 is required for Fee Types = 50, 51, 52, 53, 54, 55, 56, 57. 
 
Header Record (A*/B/F/T* 41 sequence 1)  
Field Name  Start End Len Type Description  Opt/Req Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent *  
B = Delivering Firm  
F = Fund  
T = TPA* 
 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 41 = Header R 02 
Sequence Number 4 5 2 A/N 01 R 37 
Receiving Firm/Fund 
Number 
6 9 4 A/N [[NSCC]] [[ID]] of the Receiver R F4/04 
Agent for Receiving 
Firm 
10 13 4 A/N [[NSCC]] [[ID]] of the Agent for Receiving Firm O  
Delivering Firm/Fund 
Number  
14 17 4 A/N [[NSCC]] [[ID]] of the Deliverer R I2/04/Q
3 
Agent for Delivering 
Firm 
18 21 4 A/N [[NSCC]] [[ID]] of the Agent for Delivering Firm O  
Security Issue [[ID]]  22 30 9 A/N [[CUSIP]] 
[[NSCC]] will not validate [[CUSIP]] for eligibility.  
[[NSCC]] validates the format. 
R 05 
Control Number 31 50 20 A/N Should be populated by the Firm.  [[NSCC]] will 
not validate this format. 
 
Format (best practice): 
Sppppyjjjnnnnnnnnnnn  
Where: 
S = alpha (1 byte) 
R Q0 

---

## Page 13

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 13 
Header Record (A*/B/F/T* 41 sequence 1)  
pppp = Submitting Firm Number (4 bytes) 
y = Last digit of current year (1 byte) 
jjj = Julian Date (3 bytes) 
nnnnnnnnnnn = Unique sequential number 
assigned by firm (11 bytes) 
Membership Identifier 51 52 2 A/N 01 = Trust [[Member]] 
02 = Info required for TPA/Investment Agent  
 
O F9 
TPA/Investment Agent 
Number* 
53 56 4 A/N Required when “System Code” = A*, T* or 
Membership Identifier = 02  
*Placeholder for future use 
OC G0 
Fee Type 57 58 2 A/N 50 = Sub-Accounting 12b-1/ Shareholder 
        Service Fee 
51 = Sub-Accounting CDSC 
52 = Sub-Accounting [[Underwriting]] Fee 
        Adjustment  
53 = Sub-Accounting Short-Term Redemption 
54 = Sub-Accounting Finder’s Fee Adjustment  
55 = Sub-Accounting Service Fee 
56 = Retirement/Bank Trust Service Fee 
57 = Networking Service Fee 
 
Fee Types 51, 52, 53, 54 are not allowed when 
System Code = F. 
 
R 29 
[[settlement]] Indicator 59 59 1 A/N 1 = [[settlement]]  
2 = No [[settlement]] 
3 = Test 
4 = Omni Invoice for [[settlement]] 
5 = Omni Invoice for Non-[[settlement]] 
 
Fee Types = 50, 55, 56, 57 when “Invoice 
Initiator” = 1 (Firm): 
Fee Type 50, 55, 56, 57 transactions must use 
values “3”, “4”, or “5” when System Code = 
A*/B/T*.  
[[DTCC]] will settle Fee Type 50, 55, 56, 57(Firm 
Initiated) when: 
• System Code = F and  
• [[settlement]] Indicator = 1 ([[settlement]]) 
 and: 
R B6 

---

## Page 14

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 14 
Header Record (A*/B/F/T* 41 sequence 1)  
• Confirm/Reject Code Indicator = 1 
(Confirmed) when Fee Type = 50; or 
• Confirm/Reject Code Indicator = 1, 4 or 5 
when Fee Type = 55, 56, 57. 
 
Fee Types 51, 52, 53, 54: 
 
Fee Types 51, 52, 53, 54 transactions must use 
values “1”, “2”, or “3”.   
[[DTCC]] will settle Fee Types 51, 52, 53, 54 
when: 
• System Code = A*/B/T* and  
• [[settlement]] Indicator = 1 and  
• Confirm/Reject Code Indicator = 3 (N/A). 
 
 Fee Type = 57 when “Invoice Initiator” = 2 
(Fund): 
 
Fee Type 57 (Fund Initiated) transactions must 
use value “1”, “2”, or “3”.  
[[DTCC]] will settle Fee Type 57 when:  
• System Code = F, and  
• [[settlement]] Indicator = 1, and 
• Confirm/Reject Code Indicator = 3 (N/A). 
 
Omnibus Fund/Firm 
Account Number 
Indicator 
60 60 1 A/N Required for Fee Types 50, 51, 52, 53, 54, 55. 
Not allowed for Fee Types 56, 57.                      
[[NSCC]] will reject if provided. 
 
1 = Firm (BIN) 
2 = Fund (FIN) 
OC I1 
Omnibus Account 
Number 
61 80 20 A/N Required for Fee Types 50, 51, 52, 53, 54, 55. 
Not allowed for Fee Types 56, 57.                  
[[NSCC]] will reject if provided. 
 
Omnibus BIN or Omnibus FIN number as 
indicated in the “Omnibus Fund/Firm Account 
Number Indicator” field.  BIN is preferred. 
 
OC N6 
 
 
Fund/Firm Submission 
Date 
 
81 88 8 A/N mmddccyy 
Submission date of the file. 
R K2 
 

---

## Page 15

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 15 
Header Record (A*/B/F/T* 41 sequence 1)  
 
  
 
[[NSCC]] will validate the date format; only valid 
calendar dates are allowed.  [[NSCC]] does NOT 
validate for business dates. 
 
Best Practice:                                               
Date the deliverer submits the invoice  
 
 
 
Confirm/Reject Code 
Indicator 
89 89 1 A/N 1 = Confirmed  
2 = Rejected 
3 = N/A 
4 = Modified 
5 = Partially Rejected 
 
If System Code = A*/B/T*, value “3” = N/A is 
required. 
 
*Placeholder for future use 
 
If System Code = ‘F’ and Fee Type = 50: 
• Value “1” is required when  “Confirmed” or 
“Release to [[settlement]]” ([[settlement]] 
Indicator = 1).  
• Value “2” is required when “Rejected”. 
 
If System Code = ‘F’ and Fee Type = 55, 56, 57 
(“Invoice Initiator” = 1-Firm): 
• Value “1”, “4”, or “5” is required when 
“Confirmed”, “Modified” or “Partially 
Rejected”.  
• Value “2” is required when “Rejected”. 
• Value “1”, “4”, or “5” is required when 
“Release to [[settlement]]” ([[settlement]] 
Indicator = 1) 
If System Code = ‘F’ and Fee Type = 57 
(“Invoice Initiator” = 2-Fund): 
• Value “3” = N/A is required 
 Best Practice: 
 1) If the fund has previously confirmed an 
Invoice, they should not reject it, but should 
release to [[settlement]]. 
2) Fee Type = 50 - Partial payments are not 
allowed. Funds should settle the entire invoice 
or reject the entire invoice. Values “4” and “5” 
R Q1 

---

## Page 16

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 16 
Header Record (A*/B/F/T* 41 sequence 1)  
will be rejected by [[NSCC]] if provided for Fee 
Type 50. 
3) Fee Type = 55, 56, 57 - funds can Modify or 
Partially Reject Invoices. 
 
Number of Rates 90 91 2 A/N Required for Fee Type = 50, 55, 56, 57 
 
Number of rates for this invoice. 
The number of rates must match the total 
number of “Detail Summary” record 43 seq1. 
[[NSCC]] will reject the invoice if it does not match. 
 
Fee Type = 51, 52, 53, 54: 
This field must be blank  
 
All zero values are NOT allowed 
 
 
OC Q2 
[[NSCC]] Reject Indicator 92 92 1 A/N Input: Space 
 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
 
Note: If there are any issues with the Invoice 
(structural – missing records or formatting) 
[[NSCC]] will reject the entire Invoice 
R  
[[NSCC]] Reject Code # 1 93 94 2 A/N Input:  Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 2 95 96 2 A/N Input: Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 3 97 98 2 A/N Input: Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 4 99 100 2 A/N Input: Space  
Output: Reject Code or space 
R  
 
 
  

---

## Page 17

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 17 
Header Record (A*/B/F/T* 41 sequence 2)  
Required on Input /Output  
Note:   
This Record A*/B/F/T* 41 sequence 2 is required for Fee Types = 50, 51, 52, 53, 54, 55, 56, 57. 
 
Header Record (A*/B/F/T* 41 sequence 2)  
Field Name  Start End Len Type Description  Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent * 
B = Delivering Firm  
F = Fund  
T = TPA* 
R 01 
Record Type 2 3 2 A/N 41 = Header R 02 
Sequence Number 4 5 2 A/N 02 R 37 
Period Start Date 6 13 8 A/N mmddccyy  
Business Start Date for invoiced Period  
 
[[NSCC]] validates date format, only valid calendar 
days are allowed.   
 
R N7 
Period End Date 14 21 8 A/N mmddccyy  
Business End Date for invoiced Period  
 
[[NSCC]] validates date format, only valid calendar 
days are allowed.  
  
Period End Date MUST be after Period Start 
Date; [[NSCC]] will reject if it is not (reject code 
N8). 
R N8 
Anticipated [[settlement]] 
Date 
22 29 8 A/N mmddccyy 
Optional on [[Broker]] Invoice submissions. 
Optional on Fund Confirmation.  
 
Best Practice: 
Anticipated [[settlement]] Date should be provided 
by the Fund on their confirmation record to 
indicate a target [[settlement]] date.  This date will 
NOT trigger the actual [[settlement]] but will 
O N9 

---

## Page 18

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 18 
Header Record (A*/B/F/T* 41 sequence 2)  
provide the firm with the date the fund expect to 
release the invoice for [[settlement]]. 
 
Fee Types = 50, 55, 56, 57 (Firm Initiated)  
Should be populated by the Fund on the 
Confirmation Record for Fee Type =50, 55, 56, 
57 (if “Invoice Initiator” = 1 – Firm) if known at 
the time of Confirmation.  
 
[[DO]] not delay confirmation if the Date is 
unknown.  
 
Should be blank when the Fund releases to 
[[settlement]]. 
 
Fee Type = 57 (Fund Initiated) 
Should be blank if System Code = ‘F’ and 
“Invoice Initiator” = 2 (Fund).  [[NSCC]] will not 
reject if this field is populated when “Invoice 
Initiator” = 2 (Fund) 
 
Invoice Initiator 30 30 1 A/N Required for Fee Type = 57.  
1 = Firm 
2 = Fund 
 
Not allowed for other Fee Types.             [[NSCC]] 
will reject if provided. 
 
OC P3 
[[Asset]] Type 31 32 2 A/N Optional for Fee Types 55, 56. 
 
Not expected for fee types other than 55, 56, 
however [[NSCC]] will NOT reject if provided for 
the other fee types.  
 
The type of Advisory / WRAP account included 
in this invoice. This field allows firms to describe 
the underlying type of account(s) that are 
included on the fund invoice. 
[[Asset]] Type is used to define specific Service 
Fee Groups by account classification and/or 
product distribution type. 
 
01 = Retirement (Combined ERISA   and non-
ERISA) 
02 = ERISA 
O P4 

---

## Page 19

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 19 
Header Record (A*/B/F/T* 41 sequence 2)  
03 = Non-ERISA 
04 = Advisory 
05 = Advisory Retirement (Combined ERISA 
and non-ERISA) 
06 = Advisory/ERISA 
07 = Advisory/Non-ERISA 
08 = Defined Benefit 
09 = Correspondent 
10 = 529 
11 = Retail 
Program Name 33 82 50 A/N Optional for Fee Type = 55 
Not expected for fee types other than 55 
however [[NSCC]] will NOT reject if provided for 
the other fee types. 
 
The name of the proprietary Advisory / WRAP 
Program included in this invoice. 
 
Defines Service Fee Sub-Groups within an 
Advisory [[Asset]] Type for the purpose of creating 
unique invoice records within the same Security 
Issue. 
Best Practice: 
This field should be populated if “[[Asset]] Type” 
field is populated with an Advisory Program 
indicator. 
 
O  
Filler 83 100 18 A/N Space R  
 
 
  

---

## Page 20

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 20 
INVOICING AND FEE [[settlement]] 
Account Detail Record (A*/B/F/T* 42 sequence 1) 
Optional Conditional  
Note:  
• These are the Account Detail Record A*/B/F/T* 42 sequences 1-5.  
• This Record A*/B/F/T* 42 sequence 1: 
• Required for Fee Types = 51, 52, 53, 54, 56 **;  
• Optional for Fee Type = 50.  If Sequence 1 is submitted Sequence 2 is Required for Fee Type = 50   
• Not allowed for Fee Types = 55, 57. 
• Underlying Account Detail – for Fee Types = 50, 51, 52, 53, 54. 
• Retirement / Bank Trust Account Detail – for Fee Type = 56.  
• ** Detail Records 42 are Required for Fee Type = 56 on 1) [[Broker]] initiated invoices, 2) Invoice modification (Detail 
Records are required for the affected rate block where “Modification Indicator” field on Record 43 = “1” –Yes), 3) 
Partial Rejection (Detail Records are required for the affected rate block where “Deliverer Reject Indicator” field on 
Record 43 = “3”-Partially Rejected), 4) Release to [[settlement]] of the Modified invoice (Detail Records are required 
for the affected rate block where “Modification Indicator” field on Record 43 = “1” –Yes), 5) Release to [[settlement]] 
of the Partially Rejected Invoice.  These Detail Records 42 are Optional for 1) Confirmation without Modification, 2) 
Invoice rejection, 3) Release to [[settlement]] without Modification, 4) Release to [[settlement]] without Partial 
Rejection. 
 
Account Detail Record (A*/B/F/T* 42 sequence 1) 
Field Name  Start End Len Type Description  Opt/  
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent * 
B = Delivering Firm  
F = Fund  
T = TPA* 
R 01 
Record Type 2 3 2 A/N 42 R 02 
Sequence Number 4 5 2 A/N 01 R 37 
Debit/Credit Indicator 6 6 1 A/N 1= Debit  
2= Credit 
 
When System Code = A*/B/T*:  
- value ‘1’ - (Debit the fund) – firm requests 
fund to be debited and firm to be credited  
- value ‘2’ - (Credit the fund) – firm requests 
fund to be credited and firm to be debited  
 
R 41 

---

## Page 21

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 21 
Account Detail Record (A*/B/F/T* 42 sequence 1) 
When System Code = F and  
Fee Type = 50, 56:  
- value ‘1’ - (Debit the firm) – fund requests 
firm to be debited and fund to be credited  
- value ‘2’ - (Credit the firm) – fund requests 
firm to be credited and fund to be debited  
 
For [[Broker]]-initiated invoices (Fee Type =50, 
56) funds must provide the appropriate 
“Debit/Credit Indicator” on their response.  If 
the [[Broker]] invoice was populated with “1” 
(Debit), fund response must be a “2” (Credit) 
indicating that the firm should be credited, 
and the fund debited. 
Filler 7 8 2 A/N Space R  
Invoiced / [[settlement]] 
Amount 
9 23 15 N Dollar amount of stated fee for [[settlement]] 
9,999,999,999,999.99 
 
R O0 
Underlying Firm Symbol 
(UFS) 
24 27 4 A/N Best Practice: 
Fee Type = 56 - If the “Underlying Customer 
Type” Rec 42 seq 4 does NOT have an 
[[NSCC]] [[participant]] Number, a UFS symbol 
should be provided in the “Underlying Firm 
Symbol” field (if available) 
O  Underlying BIN 28 47 20 A/N Required for Fee Types 50, 51, 52, 53, and 
54. 
This field is not expected for Fee Types 55, 
56, 57; however, [[NSCC]] will NOT reject if 
provided. 
 
Underlying brokerage customer account 
number associated with stated account 
OC O1 
Filler 48 91 44 A/N Space R  
[[NSCC]] Reject Indicator 92 92 1 A/N Input: Space 
 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
 
Note: If there are any issues with the Invoice 
(structural – missing records or formatting) 
[[NSCC]] will reject the entire Invoice 
R  
[[NSCC]] Reject Code # 1 93 94 2 A/N Input: Space  R  

---

## Page 22

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 22 
Account Detail Record (A*/B/F/T* 42 sequence 1) 
Output: Reject Code or space  
[[NSCC]] Reject Code # 2 95 96 2 A/N Input: Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 3 97 98 2 A/N Input: Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 4 99 100 2 A/N Input: Space  
Output: Reject Code or space 
R  
 
  

---

## Page 23

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 23 
Account Detail Record (A*/B/F/T* 42 sequence 2) 
Optional Conditional  
Note:   
• This Record A*/B/F/T* 42 sequence 2: 
• Required for Fee Type = 50 when Record A*/B/F/T* 42 sequence 1 is provided;  
• Required for Fee Type = 56**; 
• Not allowed for Fee Types = 51, 52, 53, 54, 55, 57.  
• Underlying Account Detail – for Fee Types = 50. 
• Retirement / Bank Trust Account Detail – for Fee Type = 56.  
• ** Detail Records 42 are Required for Fee Type = 56 on 1) [[Broker]] initiated invoices, 2) Invoice modification (Detail 
Records are required for the affected rate block where “Modification Indicator” field on Record 43 = “1” –Yes), 3) 
Partial Rejection (Detail Records are required for the affected rate block where “Deliverer Reject Indicator” field on 
Record 43 = “3”-Partially Rejected), 4) Release to [[settlement]] of the Modified invoice (Detail Records are required 
for the affected rate block where “Modification Indicator” field on Record 43 = “1” –Yes), 5) Release to [[settlement]] 
of the Partially Rejected Invoice.  These Detail Records 42 are Optional for 1) Confirmation without Modification, 2) 
Invoice rejection, 3) Release to [[settlement]] without Modification, 4) Release to [[settlement]] without Partial 
Rejection. 
 
Account Detail Record (A*/B/F/T* 42 sequence 2)   
Field Name  Start End Len Type Description  Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 42 R 02 
Sequence Number 4 5 2 A/N 02  R 37 
Rate 6 13 8 N Fee Type = 50: 
Annualized Rate expressed in bps. 
999.99999 
Decimal point is implied. 
 
Zero values are allowed.  
 
Duplicate rates are allowed for Fee Type 56 
and NOT allowed for Fee Type 50 ([[NSCC]] will 
reject the invoice). 
R O2 

---

## Page 24

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 24 
Account Detail Record (A*/B/F/T* 42 sequence 2)   
 
Best Practice: 
Rates expressed in bps should be populated  
in the following format: 
 
25bps = 02500000 (with the decimal point it 
will read 025.00000) 
 
25.55 bps = 02555000 (with the decimal point 
it will read 025.55000) 
 
Rates expressed in $ amounts should be 
populated in the following format: 
999999.99  
$25 = 00002500 (with the decimal point it will 
read 000025.00) 
 
$25.55 = 00002555 (with the decimal point it 
will read 000025.55) 
 
Fee Type 50: 
Rate should be expressed in bps for Fee Type 
50. 
 
Fee Type 56: 
The value provided in the “Rate Type” field will 
determine whether the value supplied in the 
“Rate” field is bps vs $amount. 
Rate will be expressed in bps or $ (as defined 
in the “Rate Type” field). 
 
 
Sub-Accounting Eligible 
Assets 
14 30 17 N Required for Fee Type = 50, 56. 
 
99,999,999,999,999.99 
 
Assets eligible for Fee Type 50 or 56 
 
Zero values are allowed. 
R O3 
Sub-Accounting Ineligible 
Assets 
31 47 17 N Required for Fee Type = 50. 
Optional for Fee Type = 56. 
 
OC O4 

---

## Page 25

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 25 
Account Detail Record (A*/B/F/T* 42 sequence 2)   
999,999,999,999,999.99 
 
Dollar assets not fully aged and therefore not 
eligible for Fee Type = 50. 
Sub-Accounting Excluded 
Assets 
48 64 17 N Required for Fee Type = 50.    
Not allowed for Fee Type = 56.     
[[NSCC]] will reject if provided. 
 
999,999,999,999,999.99 
 
Dollar assets not eligible for 12b-1/ 
Shareholder Service Fees (e.g. a fund may not 
pay 12b-1 on assets in wrap accounts).   
OC O5 
Sub-Accounting Balance 65 81 17 N Required for Fee Type = 50.   
Not allowed for Fee Type = 56.  Not expected 
for Fee Type 56, however [[NSCC]] will NOT 
reject if provided. 
999,999,999,999,999.99 
 
Account balance as-of Period End Date  
Sum of Eligible, Ineligible and Excluded Assets 
for the fund/rate 
 
Zero values are allowed. 
OC O6 
Rate Type 82 82 1 A/N Required for Fee Type = 56 
Not allowed for Fee Type = 50.   [[NSCC]] will 
reject if provided for Fee Type 50. 
 
1 = [[Asset]] Based 
2 = Account Based 
OC V8 
Filler 83 100 18 A/N Space 
 
R  
 
  

---

## Page 26

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 26 
Underlying Account Detail Record (A*/B/F/T* 42 sequence 3) 
Optional Conditional  
Note:   
• This Record A*/B/F/T* 42 sequence 3: 
• Required for Fee Types = 51, 52, 53, 54. 
• Not allowed for Fee Types = 50, 55, 56, 57.  
 
Underlying Account Detail Record (A*/B/F/T* 42 sequence 3)   
Field Name  Start End Len Type Description  Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 42 R 02 
Sequence Number 4 5 2 A/N 03  R 37 
Trade Date 6 13 8 A/N mmddccyy R C3 
Process Date of Trade 14 21 8 A/N mmddccyy R O7 
Sub–Account Transaction 
Amount 
22 38 17 
 
N Amount of the sub-account transaction 
associated with stated fee type 
999,999,999,999,999.99  
   
All zero values are not allowed. 
R O8 
Sub-Account Trade 
Control Number 
 
39 58 20 A/N Will be populated by the firm.   
Will indicate the original control number 
of the trade. 
 
R O9 
Filler 59 100 42 A/N Space 
 
R  
 
  

---

## Page 27

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 27 
Retirement/Bank Trust Account Detail Record (A*/B/F/T* 42 sequence 
4) 
Optional Conditional  
Note:   
• This Record A*/B/F/T* 42 sequence 4:  
• Required for Fee Type = 56**; 
• Not allowed for Fee Types = 50, 51, 52, 53, 54, 55, 57.  
• ** Detail Records 42 are Required for Fee Type = 56 on 1) [[Broker]] initiated invoices, 2) Invoice modification (Detail 
Records are required for the affected rate block where “Modification Indicator” field on Record 43 = “1” –Yes), 3) 
Partial Rejection (Detail Records are required for the affected rate block where “Deliverer Reject Indicator” field on 
Record 43 = “3”-Partially Rejected), 4) Release to [[settlement]] of the Modified invoice (Detail Records are required 
for the affected rate block where “Modification Indicator” field on Record 43 = “1” –Yes), 5) Release to [[settlement]] 
of the Partially Rejected Invoice.  These Detail Records 42 are Optional for 1) Confirmation without Modification, 2) 
Invoice rejection, 3) Release to [[settlement]] without Modification, 4) Release to [[settlement]] without Partial 
Rejection. 
 
Retirement / Bank Trust Account Detail Record (A*/B/F/T* 42 sequence 4)  
Field Name  Start End Len Type Description  Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 42 R 02 
Sequence Number 4 5 2 A/N 04  R 37 
Fund Account Number 
 
6 25 20 A/N  R P5 
Underlying Customer Type 26 26 1 A/N This field describes the type of firm that is 
the 2nd tier [[intermediary]] on the account.   
 
1 = Recordkeeper 
2 = Bank Trust/[[Broker]] 
 
O P6 
Underlying Customer 
[[participant]] Number 
27 30 4 A/N Underlying Customer  [[NSCC]] [[participant]] 
number (if applicable) 
 
O N/A 

---

## Page 28

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 28 
Retirement / Bank Trust Account Detail Record (A*/B/F/T* 42 sequence 4)  
Best Practice: 
Recordkeeper [[NSCC]] Number if 
“Underlying Customer Type” = “1” 
Bank Trust / [[Broker]] [[NSCC]] Number if 
“Underlying Customer Type” = “2” 
Will not be validated by [[NSCC]] 
If the Underlying Customer does NOT have 
[[NSCC]] [[participant]] Number, a UFS symbol 
should be provided in the “Underlying Firm 
Symbol” field (if available) 
Modification Indicator 31 31 1 A/N Modification indicator will indicate whether 
the invoice was modified by the fund. 
 
The following values are required when 
“System Code” = ‘F’ and “Confirm/Reject 
Code Indicator” on Record 41 seq 1 = 4 
“Modified”: 
 
1 = Yes 
2 = No 
 
Otherwise, SPACE is required.  
OC V3 
Modification Reason Code 32 33 2 A/N Modification Reason Code is required when 
“Modification Indicator” field = 1 “Yes”. 
 
To be provided by the Fund if the Invoice is 
modified. 
For a complete list of Modification Reason 
Codes please refer to the “Modification 
Reason Codes” section 
OC V4 
Detail Record [[ID]] 34 40 7 N Detail Record count #.   
 
Best Practice: 
Each Detail Record must be assigned a 
unique sequential number.  Funds must 
return the same Record Number on their 
response records. 
[[NSCC]] will not validate these numbers. 
 
R V5 
Plan [[ID]] 41 52 12 A/N Unique internal (internal to 2nd tier 
[[intermediary]]) recordkeeping plan 
identification number. 
O  
Plan Name 53 87 35 A/N The Plan Name associated to the Plan [[ID]] O  

---

## Page 29

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 29 
Retirement / Bank Trust Account Detail Record (A*/B/F/T* 42 sequence 4)  
Deliverer Reject Indicator 88 88 1 A/N ‘ ‘ = N/A  
1 = Valid 
2 = Rejected  
 
Blank is required when System Code = 
A*/B/T* 
Value ‘1’ or ‘2’ is required when System 
Code = F. 
 
Fee Type = 56 
If “Confirm/Reject Code Indicator” field on 
Record Type 41 seq.1 = “5” (Partially 
Rejected), at least one of Detail Records 42 
seq.4 must have “Deliverer Reject 
Indicator” field = “2” (Rejected) for the rate 
block (a combination of Detail Records 42 
and Summary Record 43) where “Deliverer 
Reject Indicator” field on Summary Record 
43=”3”-Partially Rejected.  
 
Detail Records 42 are Optional on invoice 
reject responses (when “Confirm/Reject 
Code Indicator” field on Record 41 seq 1 is 
set to “2”=Rejected). If provided, all Detail 
Records 42 for the rejected rate block (a 
combination of Detail Records 42 and 
Summary Record 43) should be provided 
and at least one of the Detail Records 42 
should have the “Deliverer Reject Indicator” 
field set to “2”=Rejected when this rate 
block is rejected (“Deliverer Reject 
Indicator” field on Summary Record 43 is 
set to “2”=Rejected). 
R P1 
Deliverer Reject Code #1 89 90 2 A/N Space or Fund Reject Code  
 
 
When “Deliverer Reject Indicator” field on 
this Record 42 seq4 = 2 (Rejected) then 
this Record 42 seq4  must have at least 
one of the “Deliverer Reject Code” fields 
populated with a Reject Code provided by 
the Fund. 
 
 
R P2 
Deliverer Reject Code #2 91 92 2 A/N Space or Fund Reject Code  
 
 
R P2 

---

## Page 30

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 30 
Retirement / Bank Trust Account Detail Record (A*/B/F/T* 42 sequence 4)  
Deliverer Reject Code #3 93 94 2 A/N Space or Fund Reject Code  
 
 
R P2 
Deliverer Reject Code #4 95 96 2 A/N Space or Fund Reject Code  
 
 
R P2 
Filler 97 100 4 A/N Space R  
  

---

## Page 31

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 31 
Retirement/Bank Trust Account Detail Record (A*/B/F/T* 42 sequence 
5) 
Optional Conditional 
Note:   
• This Record A*/B/F/T* 42 sequence 5:  
• Required for Fee Type = 56 when Record A*/B/F/T* 42 seq.2 field “Rate Type” = 2 – Account Based ; 
• Not allowed for Fee Types = 50, 51, 52, 53, 54, 55, 57.  
 
Retirement / Bank Trust Account Detail Record (A*/B/F/T* 42 sequence 5)   
Field Name  Start End Len Type Description  Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 42 R 02 
Sequence Number 4 5 2 A/N 05 R 37 
Eligible [[participant]] Count 6 13 8 N Required when Record A*/B/F/T* 42 seq. 
2  field “Rate Type” = 2 - Account Based 
 
99,999,999 
 
Number of Plan participants eligible for 
fee payment included in this invoice (# of 
participants invested in the fund) 
 
[[participant]] Count 
OC V6 
Ineligible [[participant]] 
Count 
14 21 8 N 99,999,999 
Number of participants in the plan that 
have not invested in the fund 
O V7 
Filler 22 100 79 A/N  R  
 
  

---

## Page 32

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 32 
INVOICING AND FEE [[settlement]] 
Detail Summary Record (A*/B/F/T* 43 sequence 1) 
Required on Input/Output 
Note:   
This Record A*/B/F/T* 43 sequence 1 is required for Fee Types = 50, 51, 52, 53, 54, 55, 56, 57. 
 
Detail Summary Record (A*/B/F/T* 43 sequence 1)   
Field Name  Start End Len Type Description  Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 43 R 02 
Sequence Number 4 5 2 A/N 01 R 37 
Receiving Firm/Fund 
Number 
6 9 4 A/N [[NSCC]] [[ID]] of the Receiver R F4/04 
Delivering Firm/Fund 
Number  
10 13 4 A/N [[NSCC]] [[ID]] of the Deliverer R I2/04 
Debit/Credit Indicator 14 14 1 A/N 1 = Debit  
2 = Credit 
 
When System Code = A*/B/T*:  
- value ‘1’ -  (Debit the fund) – firm 
requests fund to be debited and firm to be 
credited  
- value ‘2’ -  (Credit the fund) – firm 
requests fund to be credited and firm to be 
debited  
 
When System Code = F  and  
Fee Type = 50, 55, 56, 57:  
- value ‘1’ -  (Debit the firm) – fund 
requests firm to be debited and fund to be 
credited  
R 41 

---

## Page 33

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 33 
Detail Summary Record (A*/B/F/T* 43 sequence 1)   
- value ‘2’ -  (Credit the firm) – fund 
requests firm to be credited and fund to be 
debited  
 
For [[Broker]] initiated invoices (Fee Type 
=50, 55, 56, 57) funds must provide the 
appropriate “Debit/Credit Indicator” on 
their response.  If the [[Broker]] invoice was 
populated with “1” (Debit), fund response 
must be a “2” (Credit) indicating that the 
firm should be credited and the fund 
debited. 
Filler 15 16 2 A/N Space R  
Dollar Amount 17 31 15 N 9,999,999,999,999.99 
 
R D8 
Filler 32 81 50 A/N Space R  
Deliverer Reject Indicator 82 82 1 A/N ‘ ‘ = N/A  
1 = Valid 
2 = Rejected  
3 = Partially Rejected 
 
Value ‘1’, ‘2’ or ‘3’ is required when 
System Code = F. 
Value “3” is NOT allowed for Fee Types 
50, 55. Value “3” is NOT allowed for Fee 
Type 57 when Invoice Initiator = 2 (Fund). 
[[NSCC]] will reject if provided.                                                
It is allowed for Fee Type 56. 
 
Blank is required when  
System Code = A*/B/T*   
    or  
System Code = ‘F’ and 
Fee Type = ‘57’ and                           
Invoice Initiator = 2 (Fund) 
 
If “Confirm/Reject Code Indicator” field on 
Record Type 41 seq.1 = “2” (Rejected), or 
= “5” (Partially Rejected), at least one of 
the 43 records of the invoice must have 
“Deliverer Reject  Indicator” field = “2” 
(Rejected) or = 3 “Partially Rejected” (for 
Fee Type 56) 
 
 
R P1 

---

## Page 34

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 34 
Detail Summary Record (A*/B/F/T* 43 sequence 1)   
Deliverer Reject Code #1 83 84 2 A/N Space or Fund Reject Code  
 
When “Deliverer Reject Indicator” field on 
this Record 43 = 2 (Rejected) or = 3 
“Partially Rejected” then this Record 43 
seq1 must have at least one of the 
“Deliverer Reject Code” fields populated 
with a Reject Code provided by the Fund. 
 
R P2 
Deliverer Reject Code #2 85 86 2 A/N Space or Fund Reject Code R P2 
Deliverer Reject Code #3 87 88 2 A/N Space or Fund Reject Code R P2 
Deliverer Reject Code #4 89 90 2 A/N Space or Fund Reject Code R P2 
Filler 91 91 1 A/N Space R  
[[NSCC]] Reject Indicator 92 92 1 A/N Input: Space 
 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
 
Note: If there are any issues with the 
Invoice (structural – missing records or 
formatting) [[NSCC]] will reject the entire 
Invoice 
R  
[[NSCC]] Reject Code #1 93 
 
94 2 A/N Input: Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code #2 95 96 2 A/N Input: Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code #3 97 98 2 A/N Input: Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code #4 99 100 2 A/N Input: Space  
Output: Reject Code or space 
R  
 
  

---

## Page 35

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 35 
Detail Summary Record (A*/B/F/T* 43 sequence 2) 
Optional Conditional 
Note:   
• This Record A*/B/F/T* 43 sequence 2:  
• Required for Fee Types = 50, 55, 56, 57; 
• Not allowed for Fee Types = 51, 52, 53, 54.  
 
Detail Summary Record (A*/B/F/T* 43 sequence 2)    
Field Name  Start End Len Type Description  Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 43 R 02 
Sequence Number 4 5 2 A/N 02 R 37 
Rate 6 13 8 N Required for Fee Types = 50, 55, 56, 57 
Zero values are allowed.           
Decimal point is implied. 
 
Duplicate rates are allowed for Fee Types 55, 
56, 57 and NOT allowed for fee type 50 
([[NSCC]] will reject the invoice). 
 
Fee Types = 50, 56: 
The value in this field must match the value 
on Record 42. 
 
Best Practice: 
Rates expressed in bps should be populated  
in the following format: 
 
25bps = 02500000 (with the decimal point it 
will read 025.00000) 
25.55 bps = 02555000 (with the decimal point 
it will read 025.55000) 
 
R O2 

---

## Page 36

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 36 
Detail Summary Record (A*/B/F/T* 43 sequence 2)    
Rates expressed in $ amounts should be 
populated in the following format: 
999999.99  
$25 = 00002500 (with the decimal point it will 
read 000025.00) 
$25.55 = 00002555 (with the decimal point it 
will read 000025.55) 
 
Fee Type 50: 
Rate should be expressed in bps for Fee 
Type 50. Annualized Rate expressed in bps. 
999.99999 
 
Fee Type 55, 56, 57: 
The value provided in the “Rate Type” field 
will determine whether the value supplied in 
the “Rate” field is bps vs $amount. 
Rate will be expressed in bps or $ (as defined 
in the “Rate Type” field) 
 
 
Sub-Accounting Eligible 
Assets 
14 30 17 N Required for Fee Types= 50, 55, 56.       
Not allowed for Fee Type = 57.  [[NSCC]] will 
reject if populated for Fee Type 57. 
 
999,999,999,999,999.99 
 
Zero values are allowed. 
OC O3 
Sub-Accounting Ineligible 
Assets 
31 47 17 N Required for Fee Type = 50, 55              
Optional for Fee Types = 56             
Not allowed for Fee Type = 57. [[NSCC]] will 
reject if populated for Fee Type 57. 
999,999,999,999,999.99  
 
 Zero values are allowed. 
OC O4 
Sub-Accounting Excluded 
Assets 
48 64 17 N Required for Fee Type = 50.                       
 
Not allowed for Fee Types = 55, 56, 57. 
[[NSCC]] will reject if populated for Fee Type 55, 
56, 57. 
 
999,999,999,999,999.99 
OC O5 

---

## Page 37

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 37 
Detail Summary Record (A*/B/F/T* 43 sequence 2)    
Sub-Accounting Balance 
 
 
 
65 81 17 N Required for Fee Types= 50. 
Not expected for Fee Type = 55, 56, 57. 
[[NSCC]] will NOT reject if populated. 
999,999,999,999,999.99 
 
Total of Sub-Accounting Eligible, Ineligible 
and Excluded Assets. 
 
Sum of the “Sub-accounting balance” fields 
from Detail Records 42 (if records 42 are 
provided) 
 
Expressed in dollars. 
 
Zero values are allowed. 
OC O6 
[[Asset]] Calculation Method 82 82 1 A/N Required for Fee Type = 50. 
 
Not expected for Fee Types = 55, 56, 57. 
[[NSCC]] will NOT reject if populated for these 
fee types.   
1 = Average Assets 
2 = Period End 
OC P0 
Filler 83 100 18 A/N Space R  
 
  

---

## Page 38

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 38 
Detail Summary Record (A*/B/F/T* 43 sequence 3) 
Optional Conditional 
Note:   
• This Record A*/B/F/T* 43 sequence 3 is required for Fee Types = 55, 56, 57.  
• Not allowed for Fee Types = 50, 51, 52, 53, 54. 
 
Detail Summary Record (A*/B/F/T* 43 sequence 3)   
Field Name  Start End Len Type Description  Opt/   
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 43 R 02 
Sequence Number 4 5 2 A/N 03 R 37 
Rate Type 6 6 1 A/N 1 = [[Asset]] Based 
2 = Account Based 
 
Fee Type = 56 
The value in this field must match the value 
on Record 42. 
R V8 
Rate Category 7 7 1 A/N Required for Fee Type = 55.               
Not allowed for Fee Types = 56, 57. [[NSCC]] 
will reject if populated for these fee types. 
 
Rate Category is used for different fee rates 
applied to accounts with CDSC and/or a Zero 
Balance.   
 
1 = With CDSC 
2 = Without CDSC 
3 = With Zero Balance 
 
OC V9 

---

## Page 39

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 39 
Detail Summary Record (A*/B/F/T* 43 sequence 3)   
Modification Indicator 8 8 1 A/N Modification indicator will be used by funds to 
indicate whether this invoice was modified by 
the fund. 
 
The following values are required when 
“System Code” = ‘F’ and “Confirm/Reject 
Code Indicator” on Record 41 seq 1 = 4 
“Modified”: 
 
1 = Yes 
2 = No 
Otherwise, SPACE is required. 
 
If “Confirm/Reject Code Indicator” field on 
Record Type 41 seq.1 = 4 “Modified” at least 
one of the 43 seq.3 records of the invoice 
must have “Modification Indicator” field = “1” 
(Yes) 
 
For “Fee Type” = 56 
If “Modification Indicator” field =”1” (Yes) on 
one or more of the preceding Detail Records 
42 seq 4, this “Modification Indicator” field 
must be “1” (Yes) 
 
OC V3 
Modification Reason 
Code 
9 10 2 A/N Modification Reason Code is required when 
“Modification Indicator” field = 1 “Yes”. 
Optional for Fee Type =56. 
 
To be provided by the Fund if the Invoice is 
modified. 
 
For a complete list of Modification Reason 
Codes please refer to the “Modification 
Reason Codes” section 
 
OC V4 
Detail Summary Record 
[[ID]] 
11 17 7 N Required for Fee Type = 55, 57. 
Optional for Fee Type = 56. 
 
9,999,999 
 
Detail Summary Record count #.   
 
Best Practice: 
OC W5 

---

## Page 40

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 40 
Detail Summary Record (A*/B/F/T* 43 sequence 3)   
 
Each Detail Summary Record must be 
assigned a unique sequential number.    
Funds must return the same Record Number 
on their response records. 
 
Number of Eligible  
Positions 
18 26 9 N Required for Fee Type = 55, 57.   
Not allowed for Fee Type = 56.                       
[[NSCC]] will reject if provided. 
 
999,999,999 
 
Number of positions eligible for payment. 
Positions that meet the criteria for Service 
Fee Calculations based upon Fund/Firm 
Agreements. 
 
Not allowed for Fee Type 56 – this 
information will be passed in the “Eligible 
[[participant]] Count” field. 
 
OC W1 Number of Ineligible 
Positions 
27 35 9 N Required for Fee Type = 55, 57.                 
Not allowed for Fee Type = 56.                       
[[NSCC]] will reject if provided. 
999,999,999 
 
Positions excluded from Service Fee 
Calculations based upon Fund/Firm 
Agreements.  Examples include minimum 
balance requirements or other account 
exclusions. 
 
Not allowed for Fee Type 56 – this 
information will be passed in the “Ineligible 
[[participant]] Count” field. 
 
Zero values are allowed. 
OC W2 
Networking Control 
Indicator 
36 36 1 A/N Required for Fee Type = 57.                  
Not expected for Fee Type = 55, 56.             
[[NSCC]] will NOT reject if provided. 
0 = Level 0 
3 = Level 3 
4 = Level 4 
OC 15 

---

## Page 41

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 41 
Detail Summary Record (A*/B/F/T* 43 sequence 3)   
Eligible Assets 37 53 17 
 
N Required for Fee Type = 57 when Record 43 
seq. 3 field “Rate Type” =   1 - [[Asset]] Based. 
Not allowed for Fee Types = 55, 56.              
[[NSCC]] will reject if provided. 
 
999,999,999,999,999.99 
 
Assets eligible for fee payment. 
Assets that meet criteria for Service Fee 
Calculations based upon Fund/Firm 
Agreements. 
 
OC W3 
Ineligible Assets 54 70 17 
 
N Required for Fee Type = 57 when Record 43 
seq. 3 field “Rate Type” = 1 - [[Asset]] Based. 
 
Not allowed for Fee Types = 55, 56.               
[[NSCC]] will reject if provided. 
 
999,999,999,999,999.99 
 
Assets excluded from Service Fee 
Calculations based upon Fund/Firm 
Agreements. Examples include minimum 
balance requirements, account exclusions, 
pre/post [[Asset]] agreements. 
 
OC W4 
Filler 71 100 30 A/N Space R  
 
 
  

---

## Page 42

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 42 
Detail Summary Record (A*/B/F/T* 43 sequence 4) 
Optional Conditional 
Note:   
• This Record A*/B/F/T* 43 sequence 4 is required for Fee Type = 56 when Record A*/B/F/T* 43 sequence 3 field 
“Rate Type” = 2 – Account Based.  
• Not allowed for Fee Types = 50, 51, 52, 53, 54, 55, 57. 
 
Detail Summary Record (A*/B/F/T* 43 sequence 4)   
Field Name  Start End Len Type Description  Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 43 R 02 
Sequence Number 4 5 2 A/N 04 R 37 
Eligible [[participant]] Count 6 13 8 N Required for Fee Type = 56 when Record 
A*/B/F/T* 43 seq. 3  field “Rate Type” = 2 - 
Account Based 
99,999,999 
 
[[participant]] Count 
Number of Plan participants eligible for fee 
payment included in this invoice (# of 
participants invested in the fund) 
 
Number of Plan participants eligible for fee 
payment 
OC V6 
Ineligible [[participant]] 
Count 
14 21 8 N 99,999,999 
 
[[participant]] Count 
Number of participants in the plan that 
have not invested in the fund 
 
O V7 
Filler 22 100 79 A/N Space R  
 

---

## Page 43

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 43 
INVOICING AND FEE [[settlement]] 
Invoice Summary Record (A*/B/F/T* 44 sequence 1) 
Required on Input/Output 
Note:   
This Record A*/B/F/T* 44 sequence 1 is required for Fee Types = 50, 51, 52, 53, 54, 55, 56, 57. 
 
Invoice Summary Record (A*/B/F/T* 44 sequence 1) 
Field Name  Start End Len Type Description  Opt 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent * 
B = Delivering Firm  
F = Fund  
T = TPA* 
 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 44 R 02 
Sequence Number 4 5 2 A/N 01 R 37 
Receiving Firm/Fund Number 6 9 4 A/N Same as in the Header (A*/B/F/T* 41) R F4/04 
Delivering Firm/Fund Number  10 13 4 A/N Same as in the Header (A*/B/F/T* 41) R I2/04 
Security Issue [[ID]] 14 22 9 A/N Same as in the Header (A*/B/F/T* 41) R 05 
Control Number 23 42 20 A/N Same as in the Header (A*/B/F/T* 41) R Q0 
Fee Type 43 44 2 A/N Same as in the Header (A*/B/F/T* 41) R 29 
Debit/Credit Indicator 45 45 1 A/N 1 = Debit  
2 = Credit 
 
When System Code = A*/B/T*:  
- value ‘1’ -  (Debit the fund) – firm 
requests fund to be debited and firm to be 
credited  
- value ‘2’ -  (Credit the fund) – firm 
requests fund to be credited and firm to be 
debited  
 
When System Code = F:  
R  

---

## Page 44

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 44 
Invoice Summary Record (A*/B/F/T* 44 sequence 1) 
- value ‘1’ -  (Debit the firm) – fund 
requests firm to be debited and fund to be 
credited  
- value ‘2’ -  (Credit the firm) – fund 
requests firm to be credited and fund to be 
debited  
 
For [[Broker]] initiated invoices (Fee Type 
=50, 55, 56, 57) funds must provide the 
appropriate “Debit/Credit Indicator” on 
their response.  If the [[Broker]] invoice was 
populated with “1” (Debit), fund response 
must be a “2” (Credit) indicating that the 
firm should be credited and the fund 
debited. 
Filler 46 47 2 A/N Space R  
Dollar Amount 48 62 15 N 9,999,999,999,999.99 
 
R D8 
Filler 63 91 29 A/N Space R  
[[NSCC]] Reject Indicator 92 92 1 A/N Input: Space 
 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
 
If there are any issues with the Invoice 
(missing fields/records or bad format) 
[[NSCC]] will reject the entire Invoice. 
 
R  
[[NSCC]] Reject Code #1 93 94 2 A/N Input: Space  
Output: Reject Code or space 
R 
 
 
[[NSCC]] Reject Code #2 95 96 2 A/N Input: Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code #3 97 98 2 A/N Input: Space  
Output: Reject Code or space 
R  
[[NSCC]] Reject Code #4 99 100 2 A/N Input: Space  
Output: Reject Code or space 
R  
 
  

---

## Page 45

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 45 
Invoice Summary Record (A*/B/F/T* 44 sequence 2) 
Optional Conditional 
Note:   
• This Record A*/B/F/T* 44 sequence 2 is required for Fee Types = 50, 55.  
• Not allowed for Fee Types = 51, 52, 53, 54, 56, 57. 
Invoice Summary Record (A*/B/F/T* 44 sequence 2) 
Field Name  Start End Len Type Description  Opt 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
R 01 
Record Type 2 3 2 A/N 44 R 02 
Sequence Number 4 5 2 A/N 02 R 37 
Sub-Accounting Eligible Assets 
 
 
6 22 17 N Required for Fee Types = 50, 55. 
999,999,999,999,999.99                 
Zero values are allowed.  
 
R O3 
 
 
Sub-Accounting Ineligible 
Assets 
 
 
23 39 17 N Required for Fee Type = 50, 55                
999,999,999,999,999.99    
Zero values are allowed.             
  
R O4 
 
 
 
Sub-Accounting Excluded 
Assets 
 
 
40 56 17 N Required for Fee Type = 50.                          
Not allowed for Fee Type = 55. [[NSCC]] will 
reject if provided.  
999,999,999,999,999.99                
OC O5 
 
 
 
Sub-Accounting Balance 
 
 
 
57 73 17 N Required for Fee Type = 50.                     
Not expected for Fee Types = 55. [[NSCC]] 
will NOT reject if provided.     
999,999,999,999,999.99                 
Sum of the “Sub-Accounting Balance” 
fields on records 43     
Zero values are allowed. 
OC O6 
 
 
 
 
 
Filler 
 
74 100 27 A/N Space R  
 

---

## Page 46

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 46 
 
 
Invoice Summary Record (A*/B/F/T* 44 sequence 3) 
Optional Conditional 
Note:   
• This Record A*/B/F/T* 44 sequence 3 is required for Fee Types = 55, 57. 
• Not allowed for Fee Types = 50, 51, 52, 53, 54, 56. 
 
Invoice Summary Record (A*/B/F/T* 44 sequence 3)  
Field Name  Start End Len Type Description  Opt 
Req 
Rej 
Code 
System Code 1 1 1 A/N A = Investment Agent* 
B = Delivering Firm  
F = Fund  
T = TPA* 
 
*Placeholder for future use 
R 01 
Record Type 2 3 2 A/N 44 R 02 
Sequence Number 4 5 2 A/N 03 R 37 
Number of Eligible Positions 6 14 9 N 999,999,999 
 
Number of payable positions 
Positions that meet the criteria for Service 
Fee Calculations based upon Fund/Firm 
Agreements. 
 
R W1 
Number of Ineligible Positions 15 23 9 N 999,999,999 
Zero values are allowed. 
Positions excluded from Service Fee 
Calculations based upon Fund/Firm 
Agreements.  Examples include minimum 
balance requirements or other account 
exclusions. 
 
R W2 

---

## Page 47

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] 47 
Invoice Summary Record (A*/B/F/T* 44 sequence 3)  
Eligible Assets 24 40 17 N Required for Fee Type = 57.         Not 
allowed for Fee Type 55.     [[NSCC]] will 
reject if provided. 
                                        
999,999,999,999,999.99 
Assets that meet criteria for Service Fee 
Calculations based upon Fund/Firm 
Agreements. 
 
Must contain the total amount for all 
“Eligible Assets” fields from Detail 
Summary Record 43 where “Rate Type” = 
1 – [[Asset]] Based. 
Assets eligible for fee payment 
OC W3 
Ineligible Assets 41 57 17 N Required for Fee Type = 57.              Not 
allowed for Fee Type 55.       [[NSCC]] will 
reject if provided. 
 
999,999,999,999,999.99 
Assets excluded from Service Fee 
Calculations based upon Fund/Firm 
Agreements. Examples include minimum 
balance requirements, account 
exclusions, pre/post [[Asset]] agreements. 
 
Must contain the total amount for all 
“Ineligible Assets” fields from Detail 
Summary Record 43 where “Rate Type” = 
1 – [[Asset]] Based. 
 
OC W4 
Filler 58 100 43 A/N Space 
 
R  
 
  

---

## Page 48

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] DataTrak Records 48 
INVOICING AND FEE [[settlement]] DATATRAK 
RECORDS 
DataTrak Header Record 
Required on Input from Fund/Firm to [[NSCC]] 
DataTrak Header Record 
Field Name  Start End Len Type Description  Opt/Req 
Literal 1 5 5 A/N Value ‘HDR.S’ R 
DATATRAK SYSID 6 10 5 A/N Value ‘26947’  R 
Literal 11 16 6 A/N Value ‘.E00.C’ R 
Originator Clearing Number 17 20 4 A/N  R 
Literal 21 22 2 A/N Value ‘.S’ R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 A/N mmddccyy R 
File Description 35 59 25 A/N Value ‘MF OMNIBUS INVOICING     ’ R 
Multi Batch Indicator 60 60 1 A/N Single Batch = Space  
Multi Batch = N  
Last Batch = Y 
R 
Multi Batch Number 61 63 3 N Zeroes when not Multi Batch R 
Filler 
 
64 100 37 A/N Space R 
 
 
  

---

## Page 49

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] DataTrak Records 49 
DataTrak Trailer Record 
Required  
DataTrak Trailer Record 
Field Name  Start End Len Type Description  Opt/ 
Req 
Literal 1 5 5 A/N Value ‘END.S’ R 
DATATRAK SYSID 6 10 5 A/N Value ‘26947’    R 
Literal 11 16 6 A/N Value ‘.E00.C’ R 
Originator Clearing Number 17 20 4 A/N  R 
Literal 21 22 2 A/N Value ‘.S’ R 
Sub Originator 23 26 4 A/N  R 
Data File Record Count 27 33 7 N Datatrak Header or Trailer not included in 
count 
O 
Filler 
 
34 100 67 A/N Space R 
 
  

---

## Page 50

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] Output Records 50 
INVOICING AND FEE [[settlement]] OUTPUT RECORDS 
Service Output Header Record (N00) 
Service Output Header Record (N00) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 4 1 A/N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '11111111111' 
Transmission Date 20 27 8 A/N mmddccyy 
AutoRoute File [[ID]] 28 35 8 A/N Value '02101947'       
Literal 36 55 20 A/N Value ‘MF OMNIBUS INVOICING’ 
Filler 56 100 45 A/N Space 
 
 
  

---

## Page 51

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] Output Records 51 
Input Acknowledgment Record (NOM) 
Output from [[NSCC]] to Fund/Firm 
Input Acknowledgement Record (NOM) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N OM = Omni Invoicing 
Filler 4 5 2 A/N Space 
Delivering Fund/Firm 
Number  
6 9 4 A/N  
Processing Date 10 17 8 A/N mmddccyy 
Total Records in File 18 25 8 N 99,999,999  
Including Headers and Trailers 
Debit Dollar Amount, 
Accepted Records 
 
26 42 17 N 999,999,999,999,999.99 
Credit Dollar Amount, 
Accepted Records 
 
43 59 17 N 999,999,999,999,999.99 
Debit Dollar Amount, 
Rejected Records 
 
60 76 17 N 999,999,999,999,999.99 
Credit Dollar Amount, 
Rejected Records 
 
77 93 17 N 999,999,999,999,999.99 
Filler 94 100 7 A/N Space 
 
 
  

---

## Page 52

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] Output Records 52 
Total Trailer Record (N46) 
Required on Output from [[NSCC]] 
The Total Trailer record is used to recap all records received from counterparties (for a receiving [[participant]]).  
Total Trailer Record (N46) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N Output 
N = [[NSCC]] 
Record Type 2 3 2 A/N 46 
Filler 4 5 2 A/N Space 
Receiving Firm/Fund 
Number  
6 9 4 A/N [[NSCC]] [[ID]] of the Receiver 
 
Total Records Count 10 18 9 N 999,999,999 
Total Number of physical records per recipient  
Total Debit Dollar Amount 19 35 17 N 999,999,999,999,999.99 
 
Total Credit Dollar Amount 36 52 17 N 999,999,999,999,999.99 
 
Filler 53 100 48 A/N Space 
 
 
  

---

## Page 53

Invoicing and Fee [[settlement]] Record Layouts 
Invoicing and Fee [[settlement]] Output Records 53 
Grand Total Trailer Record (N47) 
Required on Output from [[NSCC]] 
The Grand Total Trailer record is generated for each recipient to recap all records included in their [[NSCC]] output 
file.  
Grand Total Trailer Record (N47)  
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N Output 
N = [[NSCC]] 
Record Type 2 3 2 A/N 47 
Filler 4 5 2 A/N Space 
Receiving Firm/Fund 
Number  
6 9 4 A/N [[NSCC]] [[ID]] of the Receiver 
 
Total Records Count 10 18 9 N 999,999,999 
Total Number of physical records per recipient 
including Headers and Trailers. 
 
Filler 19 100 82 A/N Space 
 
 
  

---

## Page 54

Invoicing and Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis [[settlement]] Records 38, 39, 40 54 
MUTUAL FUND [[DTCC]] PAYMENT AXIS [[settlement]] 
RECORDS 38, 39, 40 
Output from [[NSCC]] to Firms and Funds 
Please refer to the [[DTCC]] Payment aXis Record Layouts. 

---

## Page 55

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 55 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 
  

---

## Page 56

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 56 
Summary of Changes – effective Q3, 2020 
CHANGE TO FIELD DESCRIPTION (DOCUMENTATION UPDATE)  
Field Name Record Type and 
Location 
Current Description New Description 
Period Start 
Date 
41 seq#2, start 6, end 
13 length 8, A/N, R 
mmddccyy  
Business Start Date for invoiced Period  
[[NSCC]] validates date format, only valid 
calendar days are allowed.   
Period Start Date MUST be before the 
Period End Date; [[NSCC]] will reject if it is 
not. 
mmddccyy  
Business Start Date for invoiced Period  
[[NSCC]] validates date format, only valid 
calendar days are allowed.   
Period End 
Date 
41 seq#2, start 14, 
end 21 length 8, A/N, 
R 
mmddccyy  
Business End Date for invoiced Period  
[[NSCC]] validates date format, only valid 
calendar days are allowed.   
Period Start Date MUST be before the 
Period End Date; [[NSCC]] will reject if it is 
not. 
mmddccyy  
Business End Date for invoiced Period  
[[NSCC]] validates date format, only valid 
calendar days are allowed.  
Period End Date MUST be after Period 
Start Date; [[NSCC]] will reject if it is not 
(reject code N8). 
Deliverer 
Reject 
Indicator 
43 seq#1, start 82, 
end 82 length 1, A/N, 
R 
‘ ‘ = N/A  
1 = Valid 
2 = Rejected  
3 = Partially Rejected 
 
Value “3” is NOT allowed for Fee Types 
50, 55, 57.                                        
[[NSCC]] will reject if provided.                                                
It is allowed for Fee Type 56. 
Blank is required when  
System Code = A*/B/T*   
    or  
System Code = ‘F’ and 
Fee Type = ‘57’ and                            
Invoice Initiator = 2 (Fund) 
 
Value ‘1’, ‘2’ or ‘3’ is required when 
System Code = F. 
If “Confirm/Reject Code Indicator” field 
on Record Type 41 seq.1 = “2” 
(Rejected), or = “5” (Partially Rejected), 
at least one of the 43 records of the 
invoice must have “Deliverer Reject 
Indicator” field = “2” (Rejected) or = 3 
“Partially Rejected” (for Fee Type 56) 
 
‘ ‘ = N/A  
1 = Valid 
2 = Rejected  
3 = Partially Rejected 
 
Value ‘1’, ‘2’ or ‘3’ is required when 
System Code = F. 
Value “3” is NOT allowed for Fee Types 
50, 55. Value “3” is NOT allowed for Fee 
Type 57 when Invoice Initiator = 2 (Fund). 
NSC will reject if provided.                                                
It is allowed for Fee Type 56. 
Blank is required when  
System Code = A*/B/T*   
    or  
System Code = ‘F’ and 
Fee Type = ‘57’ and Invoice Initiator = 2 
(Fund) 
 
If “Confirm/Reject Code Indicator” field on 
Record Type 41 seq.1 = “2” (Rejected), or 
= “5” (Partially Rejected), at least one of 
the 43 records of the invoice must have 
“Deliverer Reject Indicator” field = “2” 
(Rejected) or = 3 “Partially Rejected” (for 
Fee Type 56) 
 

---

## Page 57

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 57 
Summary of Changes – effective Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 
 
 
  

---

## Page 58

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 58 
Summary of Changes – effective Q3, 2015 
Change to Field Description 
Field Name Record Type and 
Location 
Current Description New Description 
Rate 42 seq#2, start 6, end 
13 length 8, N, R 
Fee Type = 50: 
Annualized Rate expressed in bps. 
999.99999 
Decimal point is implied. 
All zero values are not allowed.  
Duplicate rates are allowed for Fee Type 
56 and NOT allowed for Fee Type 50 
([[NSCC]] will reject the invoice). 
Fee Type = 50: 
Annualized Rate expressed in bps. 
999.99999 
Decimal point is implied. 
Zero values are allowed.  
Duplicate rates are allowed for Fee Type 
56 and NOT allowed for Fee Type 50 
([[NSCC]] will reject the invoice).  
Rate 43 seq#2, start 6, end 
13 length 8, N, R 
Required for Fee Types = 50, 55, 56, 57 
All zero values are not allowed.           
Decimal point is implied. 
Duplicate rates are allowed for Fee 
Types 55, 56, 57 and NOT allowed for 
fee type 50 ([[NSCC]] will reject the 
invoice). 
Fee Types = 50, 56: 
The value in this field must match the 
value on Record 42.  
Required for Fee Types = 50, 55, 56, 57 
Zero values are allowed.           
Decimal point is implied. 
Duplicate rates are allowed for Fee Types 
55, 56, 57 and NOT allowed for fee type 
50 ([[NSCC]] will reject the invoice). 
Fee Types = 50, 56: 
The value in this field must match the 
value on Record 42.  
Sub-
Accounting 
Eligible 
Assets 
42 seq#2, start 14, 
end 30 length 17, N, 
R 
Required for Fee Types= 50, 56.       
999,999,999,999,999.99 
Assets eligible for Fee Type 50 or 56 
All zero values are not allowed for Fee 
Type 50.  
Required for Fee Type = 50, 56. 
99,999,999,999,999.99 
Assets eligible for Fee Type 50 or 56 
Zero values are allowed. 
 
Sub-
Accounting 
Eligible 
Assets 
43 seq#2, start 14, 
end 30 length 17, N, 
OC 
Required for Fee Types= 50, 55, 56.       
Not allowed for Fee Type = 57.  [[NSCC]] 
will reject if populated for Fee Type 57. 
999,999,999,999,999.99 
All zero values are not allowed for Fee 
Type 50.  
Required for Fee Types= 50, 55, 56.       
Not allowed for Fee Type = 57.  [[NSCC]] will 
reject if populated for Fee Type 57. 
999,999,999,999,999.99 
Zero values are allowed. 
Sub-
Accounting 
Eligible 
Assets 
44 seq#2, start 6, end 
22 length 17, N, R 
Required for Fee Types = 50, 55. 
999,999,999,999,999.99                 
All zero values are not allowed for Fee 
Type 50.  
Required for Fee Types = 50, 55. 
999,999,999,999,999.99                 
Zero values are allowed.  
Sub-
Accounting 
Ineligible 
Assets 
 
43 seq#2, start 31, 
end 47 length 17, N, 
OC 
Required for Fee Type = 50.              
Optional for Fee Types = 55, 56.             
Not allowed for Fee Type = 57. [[NSCC]] 
will reject if populated for Fee Type 57. 
Required for Fee Type = 50, 55              
Optional for Fee Types = 56             
Not allowed for Fee Type = 57. [[NSCC]] will 
reject if populated for Fee Type 57. 

---

## Page 59

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 59 
Field Name Record Type and 
Location 
Current Description New Description 
999,999,999,999,999.99 999,999,999,999,999.99  
 Zero values are allowed.  
Sub-
Accounting 
Ineligible 
Assets 
 
44 seq#2, start 23, 
end 39 length 17, N, 
R 
Required for Fee Type = 50.                
Optional for Fee Type = 55. 
999,999,999,999,999.99      
Required for Fee Type = 50, 55                
999,999,999,999,999.99    
Zero values are allowed.    
Sub-
Accounting 
Balance 
 
42 seq#2, start 65, 
end 81 length 17, N, 
OC 
Required for Fee Type = 50.   
Not allowed for Fee Type = 56.  Not 
expected for Fee Type 56, however 
[[NSCC]] will NOT reject if provided. 
999,999,999,999,999.99 
Account balance as-of Period End Date  
Sum of Eligible, Ineligible and Excluded 
Assets for the fund/rate 
All zero values are not allowed for Fee 
Type 50.  
Required for Fee Type = 50.   
Not allowed for Fee Type = 56.  Not 
expected for Fee Type 56, however [[NSCC]] 
will NOT reject if provided. 
999,999,999,999,999.99 
Account balance as-of Period End Date  
Sum of Eligible, Ineligible and Excluded 
Assets for the fund/rate 
Zero values are allowed. 
Sub-
Accounting 
Balance 
 
43 seq#2, start 65, 
end 81 length 17, N, 
OC 
Required for Fee Types= 50. 
Not expected for Fee Type = 55, 56, 57. 
[[NSCC]] will NOT reject if populated. 
999,999,999,999,999.99 
Total of Sub-Accounting Eligible, 
Ineligible and Excluded Assets. 
Sum of the “Sub-accounting balance” 
fields from Detail Records 42 (if records 
42 are provided) 
Expressed in dollars. 
All zero values are not allowed for Fee 
Type 50.  
Required for Fee Types= 50. 
Not expected for Fee Type = 55, 56, 57. 
[[NSCC]] will NOT reject if populated. 
999,999,999,999,999.99 
Total of Sub-Accounting Eligible, Ineligible 
and Excluded Assets. 
Sum of the “Sub-accounting balance” 
fields from Detail Records 42 (if records 
42 are provided) 
Expressed in dollars. 
Zero values are allowed. 
Sub-
Accounting 
Balance 
 
44 seq#2, start 57, 
end 73 length 17, N, 
OC 
Required for Fee Type = 50.                     
Not expected for Fee Types = 55. [[NSCC]] 
will NOT reject if provided.     
999,999,999,999,999.99                 
Sum of the “Sub-Accounting Balance” 
fields on records 43     
All zero values are not allowed for Fee 
Type 50.  
Required for Fee Type = 50.                     
Not expected for Fee Types = 55. [[NSCC]] 
will NOT reject if provided.     
999,999,999,999,999.99                 
Sum of the “Sub-Accounting Balance” 
fields on records 43     
Zero values are allowed. 
Number of 
Ineligible 
Positions 
43 seq#3, start 27, 
end 35, length 17, N, 
OC 
Optional for Fee Type = 55, 57.                 
Not allowed for Fee Type = 56.       
[[NSCC]] will reject if provided. 
999,999,999 
Positions excluded from Service Fee 
Calculations based upon Fund/Firm 
Agreements.  Examples include 
Required for Fee Type = 55, 57.                 
Not allowed for Fee Type = 56. [[NSCC]] will 
reject if provided. 
999,999,999 
Positions excluded from Service Fee 
Calculations based upon Fund/Firm 
Agreements.  Examples include minimum 

---

## Page 60

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 60 
Field Name Record Type and 
Location 
Current Description New Description 
minimum balance requirements or other 
account exclusions. 
Not allowed for Fee Type 56 – this 
information will be passed in the 
“Ineligible [[participant]] Count” field. 
 
balance requirements or other account 
exclusions. 
Not allowed for Fee Type 56 – this 
information will be passed in the “Ineligible 
[[participant]] Count” field. 
Zero values are allowed. 
Number of 
Ineligible 
Positions 
44 seq#3, start 15, 
end 23, length 9, N, R 
999,999,999 
Positions excluded from Service Fee 
Calculations based upon Fund/Firm 
Agreements.  Examples include 
minimum balance requirements or other 
account exclusions. 
 
999,999,999 
Positions excluded from Service Fee 
Calculations based upon Fund/Firm 
Agreements.  Examples include minimum 
balance requirements or other account 
exclusions. 
Zero values are allowed. 
 
Change to Data Field Population Requirement 
Field Name Record Type and Location Current Requirement New Requirement 
Sub-Accounting Ineligible 
Assets 
44 seq#2, start 23, end 39 length 17, N  Optional Conditional Required 
 
Number of Ineligible 
Positions 
43 seq#3, start 27, end 35, length 17, N  Optional  
 
Optional Conditional 
 
Number of Ineligible 
Positions 
44 seq#3, start 15, end 23, length 9, N  Optional  
 
Required 
 
 
  

---

## Page 61

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 61 
Summary of Changes – effective Q4, 2014 
Add new Values to Existing Field 
Field Name Record Type and Field 
Location 
Description Rej Code 
Fee Type  41 seq#1, start 57 end 58, 
Length 2, A/N, Required 
50 = Sub-Accounting 12b-1/ Shareholder Service Fee 
51 = Sub-Accounting CDSC 
52 = Sub-Accounting [[Underwriting]] Fee Adjustment  
53 = Sub-Accounting Short-Term Redemption 
54 = Sub-Accounting Finder’s Fee Adjustment  
55 = Sub-Accounting Service Fee 
56 = Retirement/Bank Trust Service Fee 
57 = Networking Service Fee 
29 
Confirm/Reject Code 
Indicator 
41 seq#1, start 89 end 89, 
Length 1, A/N, Required 
1 = Confirmed  
2 = Rejected 
3 = N/A 
4 = Modified 
5 = Partially Rejected 
Q1 
Deliverer Reject 
Indicator 
43 seq#1, start 82 end 82, 
Length 1, A/N, Required 
‘ ‘ = N/A  
1 = Valid 
2 = Rejected  
3 = Partially Rejected 
 
Value “3” is NOT allowed for Fee Types 50, 55, 57.  
[[NSCC]] will reject if provided.                                                
It is allowed for Fee Type 56. 
 
Blank is required when  
System Code = A*/B/T*   
    or  
System Code = ‘F’ and 
Fee Type = ‘57’ and                                                   
Invoice Initiator = 2 (Find) 
 
Value ‘1’, ‘2’ or ‘3’ is required when System Code = F. 
 
P1 
 
 
 

---

## Page 62

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 62 
Add new Fields to Existing Records 
Field Name Record Type and Field Location Description Rej 
Code 
Invoice Initiator 41 seq#2, start 30 end 30, Length 
1, A/N, OC 
Required for Fee Type = 57.  
1 = Firm 
2 = Fund 
Not allowed for other Fee Types.  
[[NSCC]] will reject if provided. 
P3 
[[Asset]] Type 41 seq#2, start 31 end 32, Length 
2, A/N, O 
Optional for Fee Types 55, 56. 
Not expected for fee types other than 55, 56, however 
[[NSCC]] will NOT reject if provided for the other fee types.  
 
The type of Advisory / WRAP account included in this 
invoice. This field allows firms to describe the underlying 
type of account(s) that are included on the fund invoice. 
 
[[Asset]] Type is used to define specific Service Fee 
Groups by account classification and/or product 
distribution type. 
 
01 = Retirement (Combined ERISA   and non-ERISA) 
02 = ERISA 
03 = Non-ERISA 
04 = Advisory 
05 = Advisory Retirement (Combined ERISA and non-
ERISA) 
06 = Advisory/ERISA 
07 = Advisory/Non-ERISA 
08 = Defined Benefit 
09 = Correspondent 
10 = 529 
11 = Retail 
P4 
Program Name 41 seq#2, start 33 end 82, Length 
50, A/N, O 
Optional for Fee Type = 55 
The name of the proprietary Advisory / WRAP Program 
included in this invoice. 
Defines Service Fee Sub-Groups within an Advisory 
[[Asset]] Type for the purpose of creating unique invoice 
records within the same Security Issue. 
Best Practice: 
This field should be populated if “[[Asset]] Type” field is 
populated with an Advisory Program indicator 
Not expected for fee types other than 55 however [[NSCC]] 
will NOT reject if provided for the other fee types. 
n/a 

---

## Page 63

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 63 
Field Name Record Type and Field Location Description Rej 
Code 
 
Rate Type 42 seq#2, start 82 end 82, Length 
1, A/N, OC 
Required for Fee Type = 56 
Not allowed for Fee Type = 50.                                  
[[NSCC]] will reject if provided for Fee Type=50. 
 
1 = [[Asset]] Based 
2 = Account Based 
 
V8 
 
 
Requirements Changed for Existing Record Sequences 
 
 
 
 
 
 
Record Record Name Old Requirements  New Requirements  
42 sequence 1  Underlying (Retirement / 
Bank Trust) Account Detail 
Record (A*/B/F/T* 42 
sequence 1)   
Optional for Fee Type = 50. 
Required for Fee Types = 51, 
52, 53, 54. 
Optional for Fee Type = 50.  
Required for Fee Types = 51, 52, 53, 54, 56. 
Not Allowed for Fee Types = 55, 57. 
42 sequence 2 Underlying (Retirement / 
Bank Trust) Account Detail 
Record (A*/B/F/T* 42 
sequence 2)   
Optional Conditional for Fee 
Type = 50. Not allowed for 
Fee Types = 51, 52, 53, 54. 
Required for Fee Type = 50 when Record 
A*/B/F/T* 42 sequence 1 is provided;  
Required for Fee Type = 56. Not allowed for 
Fee Types = 51, 52, 53, 54, 55, 57. 
42 sequence 3 Underlying Account Detail 
Record (A*/B/F/T* 42 
sequence 3)   
Required for Fee Types = 51, 
52, 53, 54.  Not allowed for 
Fee Types = 50 
Required for Fee Types = 51, 52, 53, 54.   Not 
allowed for Fee Types = 50, 55, 56, 57. 
43 sequence 1 Detail Summary Record 
(A*/B/F/T* 43 sequence 1)   
Required for Fee Types = = 
50, 51, 52, 53, 54. 
Required for Fee Types = 50, 51, 52, 53, 54, 
55, 56, 57. 
43 sequence 2 Detail Summary Record 
(A*/B/F/T* 43 sequence 2)   
Required for Fee Type = 50. 
Not allowed for Fee Types = 
51, 52, 53, 54. 
Required for Fee Types = 50, 55, 56, 57.  
Not allowed for Fee Types = 51, 52, 53, 54. 
44 sequence 1 Invoice Summary Record 
(A*/B/F/T* 44 sequence 1)   
Required for Fee Types = 50, 
51, 52, 53, 54. 
Required for Fee Types = 50, 51, 52, 53, 54, 
55, 56, 57. 
44 sequence 2 Invoice Summary Record 
(A*/B/F/T* 44 sequence 2)   
Required for Fee Types = 50.  
Not allowed for Fee Types = 
51, 52, 53, 54. 
Required for Fee Types = 50, 55.                  
Not allowed for Fee Types = 51, 52, 53, 54, 56, 
57.  

---

## Page 64

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 64 
Add new Record Sequence to Existing Records 
Record  Record Name Requirements 
42 sequence # 4  Retirement / Bank Trust Account Detail 
Record (A*/B/F/T* 42 sequence 4), 
Optional Conditional   
Required for Fee Type = 56. 
Not allowed for Fee Types = 50, 51, 52, 53, 54, 55, 57 
42 sequence #5 Retirement / Bank Trust Account Detail 
Record (A*/B/F/T* 42 sequence 5), 
Optional Conditional 
Required for Fee Type = 56 when Record A*/B/F/T* 42 seq.2 
field “Rate Type” = 2 – Account Based;                                                             
Not allowed for Fee Types = 50, 51, 52, 53, 54, 55, 57 
43 sequence #3 Detail Summary Record (A*/B/F/T* 43 
sequence 3), Optional Conditional. 
Required for Fee Types = 55, 56, 57. 
Not allowed for Fee Types = 50, 51, 52, 53, 54. 
43 sequence #4 Detail Summary Record (A*/B/F/T* 43 
sequence 4), Optional Conditional 
Required for Fee Type = 56 when Record A*/B/F/T* 43 
sequence 3 field “Rate Type” = 2 – Account Based.                                                  
Not allowed for Fee Types = 50, 51, 52, 53, 54, 55, 57. 
44 sequence #3 Invoice Summary Record (A*/B/F/T* 44 
sequence 3), Optional Conditional 
Required for Fee Type = 55, 57. 
Not allowed for Fee Types = 50, 51, 52, 53, 54, 56. 
 
Add new Record 
Record  Record Name Requirements 
N47 Grand Total Trailer Record     Required on Output from [[NSCC]]  
The Grand Total Trailer record is generated for each recipient to recap all 
records included in their [[NSCC]] output file. 
 
 
Rename Existing Record 
Record  Old/New Record Name  Requirements 
N46 Grand Total Trailer Record / 
Total Trailer Record   
Required on Output from [[NSCC]]  
The Total Trailer record is used to recap all records received from counterparties 
(for a receiving [[participant]]). 
 
 
 
 
 
 
 

---

## Page 65

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 65 
Rename Existing Fields and Change Field Descriptions 
Current Field 
Name 
Record Type and 
Location 
New Field Name  New Description Old Rej 
Code 
New Rej 
Code 
Fund/Firm 
Processing 
Date  
41 seq#1, start 81, end 88 
length 8, A/N, R 
Fund/Firm 
Submission Date   
mmddccyy 
Submission date of the file. 
 
[[NSCC]] will validate the date format; 
only valid calendar dates are allowed.  
[[NSCC]] does NOT validate for 
business dates. 
 
Best Practice:                                               
Date the deliverer submits the 
invoice  
54 K2 
Omnibus 
Eligible Assets 
44 seq#2, start 6, end 22 
length 17, N, R 
Sub-Accounting 
Eligible Assets 
 
Required for Fee Types = 50, 55. 
999,999,999,999,999.99    
All zero values are not allowed for 
Fee Type 50. 
P3 O3 
Omnibus 
Ineligible 
Assets 
44 seq#2, start 23, end 39 
length 17, N, OC 
Sub-Accounting 
Ineligible Assets 
 
Required for Fee Type = 50.                
Optional for Fee Type = 55.  
999,999,999,999,999.99         
P4 O4 
Omnibus 
Excluded 
Assets 
44 seq#2, start 40, end 56 
length 17, N, OC 
Sub-Accounting 
Excluded Assets 
 
Required for Fee Type = 50.                
Not allowed for Fee Type = 55. 
[[NSCC]] will reject if provided.  
999,999,999,999,999.99              
P5 O5 
Omnibus 
Account 
Balance 
43 seq#2, start 65, end 81 
length 17, N, OC 
 
Sub-Accounting 
Balance 
Required for Fee Types= 50. 
Not expected for Fee Type = 55, 56, 
57.  [[NSCC]] will NOT reject if 
populated. 
999,999,999,999,999.99 
 
Total of Sub-Accounting Eligible, 
Ineligible and Excluded Assets. 
 
Sum of the “Sub-accounting balance” 
fields from Detail Records 42 (if 
records 42 are provided) 
 
Expressed in dollars. 
All zero values are not allowed for 
Fee Type 50. 
 
P6 
 
O6 
Omnibus 
Account 
Balance 
44 seq#2, start 57, end 73 
length 17, N, OC 
Sub-Accounting 
Balance 
Required for Fee Type = 50.                     
Not expected for Fee Types =55.                                                     
[[NSCC]] will NOT reject if provided     
 
P6 
 
O6 

---

## Page 66

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 66 
Current Field 
Name 
Record Type and 
Location 
New Field Name  New Description Old Rej 
Code 
New Rej 
Code 
999,999,999,999,999.99                 
Sum of the “Sub-Accounting 
Balance” fields on records 43     
All zero values are not allowed for 
Fee Type 50. 
 
 
 
 
  

---

## Page 67

Invoicing and Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 67 
Summary of Changes – effective Q1, 2013 
PLACEHOLDER FOR THIRD PARTY FEES (PHASE II) 
Field Name Record Type and field location Description 
System Code 41, start 1 end 1, Length 1,A/N 
42, start 1 end 1, Length 1,A/N 
43, start 1 end 1, Length 1,A/N 
44, start 1 end 1, Length 1,A/N 
A = Investment Agent* 
B = Delivering Firm  
F = Fund 
T = TPA* 
 
 
Header Record 41 Sequence 1 
Field Name Start End  LEN Type Description Opt/ 
Req 
Rej 
Code 
TPA/Investment 
Agent Number* 
53 56 4 A/N Required when “System Code” = A*, T* or 
Membership Identifier = 02 
OC G0 
 
Note:  
*- Placeholder field/value for Third Party Fees (Phase II) 
 
FIELD UPDATES 
Field Name Record Type and field location Description Rej 
Code 
Invoiced / [[settlement]] 
Amount 
42 seq#1, start 9 end 23, Length 15, N 9,999,999,999,999.99  
O0 
Dollar Amount 43 seq#1, start 17 end 31, Length 15, N 9,999,999,999,999.99 D8 
Dollar Amount 44 seq#1, start 48 end 62, Length 15, N 9,999,999,999,999.99 D8 

---

## Page 68

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: July 27, 2023 
Publication Code: MFS293 
Service: Payment aXis 
Title: Invoicing and Fee [[settlement]] Record Layouts 
For More Information 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com  
   