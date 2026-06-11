---
title: "DTCC Payment aXis: Commission & Fee Settlement Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/comm-fee_sett_record_layouts_mfs311_20230807.pdf"
pages: 41
size: "545.5 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# DTCC Payment aXis: Commission & Fee Settlement Record Layouts

**Original File:** [comm-fee_sett_record_layouts_mfs311_20230807.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/comm-fee_sett_record_layouts_mfs311_20230807.pdf)  
**Category:** Rules  
**Total Pages:** 41  
**File Size:** 545.5 KB  

---

## Page 1

 
 
 
Payment aXis 
COMMISSION & FEE [[settlement]] RECORD 
LAYOUTS 
AUGUST 3, 2023 
 

---

## Page 2

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Returned Payments Header Record 2 
REVISION HISTORY 
See the Appendix for the summary of changes. 
Effective Date Important Notices 
August 3, 2023 • Record has been rebranded and reviewed 
• Summary of Changes has been moved to back of document 
Effective March 25, 2019 Please see Important Notices: 
a8658 P&S 8233 Dated December 19, 2018 
Effective November 20, 2017 Please see Important Notices: 
a8402 P&S 7977 Dated June 1, 2017 
Effective February 27, 2017 Please see Important Notices: 
a8286 P&S 7861 Dated November 8, 2016 
Effective April 27, 2015 Please see Important Notices: 
a7926 P&S 7501 Dated November 4, 2014 
Effective February 2013 Please see Important Notices: 
a7567 P&S 7137 Dated January 9, 2013 and 
a7472 P&S 7042 Dated August 16, 2012  
 
Effective February 11, 2013 Please see Important Notices: 
a7567 P&S 7137 Dated January 9, 2013, and  
a7464 P&S 7034 Dated July 31, 2012 
Effective December 5, 2005 Please see Important Notices: 
a6092 P&S 5662 Dated August 17, 2005, and  
a6089 P&S 5659 Dated August 12, 2005 
 

---

## Page 3

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Returned Payments Header Record 3 
TABLE OF CONTENTS 
Mutual Fund [[DTCC]] Payment aXis Returned Payments Header Record ......................................................... 4 
Mutual Fund [[DTCC]] Payment aXis Security Header Record ............................................................................ 7 
Mutual Fund [[DTCC]] Payment aXis Detail Record #1 ....................................................................................... 10 
Mutual Fund [[DTCC]] Payment aXis Detail Record #2 ....................................................................................... 12 
Mutual Fund [[DTCC]] Payment aXis Detail Record #3 ....................................................................................... 14 
Mutual Fund [[DTCC]] Payment aXis Security Trailer Record ........................................................................... 16 
Mutual Fund [[DTCC]] Payment aXis Grand Total Input/Output Trailer Record ............................................... 18 
Mutual Fund [[DTCC]] Payment aXis Service DataTrak Header Record ........................................................... 20 
Mutual Fund [[DTCC]] Payment aXis Service DataTrak Trailer Record ............................................................ 21 
Mutual Fund [[DTCC]] Payment aXis Detail Reject Record ................................................................................ 22 
Mutual Fund [[DTCC]] Payment aXis Grand Total Trailer Record ..................................................................... 24 
Mutual Fund [[DTCC]] Payment aXis Security Issue [[ID]] [[settlement]] Detail Record  .......................................... 25 
Mutual Fund [[DTCC]] Payment aXis [[settlement]] Record by Contra [[participant]] .............................................. 26 
Mutual Fund [[DTCC]] Payment aXis Grand Total [[settlement]] Record .............................................................. 27 
Mutual Fund [[DTCC]] Payment aXis Service Output Header Record ............................................................... 28 
Mutual Fund [[DTCC]] Payment aXis [[settlement]] Summary Output Header Record  ........................................ 29 
Mutual Fund [[DTCC]] Payment aXis Input Acknowledgement Record ............................................................ 30 
APPENDIX – Summary of Changes .................................................................................................................. 31 
Summary of Changes – effective Q1, 2019 ...................................................................................................... 32 
Summary of changes – effective Q4, 2017 ...................................................................................................... 33 
Summary of changes – effective Q1, 2017 ...................................................................................................... 34 
Summary of changes – effective Q2, 2015 ...................................................................................................... 37 
Summary of changes – effective Q4, 2013 ...................................................................................................... 38 
Summary of changes – effective Q1 (March 18), 2013 ................................................................................... 39 
Summary of changes – effective Q1 (February 11), 2013 .............................................................................. 40 
 

---

## Page 4

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Returned Payments Header Record 4 
MUTUAL FUND [[DTCC]] PAYMENT AXIS RETURNED 
PAYMENTS HEADER RECORD 
This header record was created in response to the DoL [[Fiduciary]] Rule to allow firms to return payments to the 
original deliverer. Firms will utilize this header record to return payments that are not permitted by their internal 
policies and procedures. 
Notes: 
1. This record can be submitted by Firms only. Firms will utilize this Header record to return payments to original 
deliverers. 
2. Header Record 15 is NOT allowed when Header Record 30 is provided. 
3. Firms utilizing this header record to return payments must adhere to the existing record structure by submitting the 
following set of records: 
• Header Record 15 
• Detail Record(s) 31 
• Trailer Record 32 
• Grand Total Trailer Record 33 
4. Detail Records 31 received in combination with a Header Record 30 or Header Record 15 where “[[settlement]] 
Indicator” field is populated with “1=No [[settlement]]” or “2=Test” will NOT be settled through [[DTCC]] Payment aXis. 
Input/Output 
Mutual Fund [[DTCC]] Payment aXis Returned Payments Header Record 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N B = Delivering Firm 
This record can be submitted by Firms only. 
R 
Record Type 2 3 2 A/N 15 = Header for Returned Payments R 
Filler 4 5 2 A/N Space R 
Receiving Firm /Fund 
Number 
6 9 4 N Firms will utilize this Header record to return 
payments to the original deliverer 
R 
Agent For Receiving Firm 10 13 4 A/N  O 
Delivering Firm Number 14 17 4 A/N This record can be submitted by Firms only R 
Security Issue Country 
Code 
18 19 2 A/N Space R 

---

## Page 5

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Returned Payments Header Record 5 
Field Name Start End Len Type Description Opt/ 
Req 
Security Issue [[ID]] 20 28 9 A/N Can be registered or non-registered Security 
Issue [[ID]]  
Best Practice:  
Best practice algorithm for internal client-
created (non-registered) Security Issue IDs: 
NNNNXXXXX, where  
• NNNN – [[NSCC]] [[participant]] 
number of the record submitter  
• XXXXX – alpha/numeric sequence 
R 
Security Issue Check Digit 29 29 1 A/N Space R 
Fund/Firm Processing 
Date 
30 37 8 N mmddccyy  
Best Practice:  
This field should be populated with the original 
processing date as provided on the original 
record that is being returned 
R Commission Type 38 39 2 A/N 01 = Front End  
02 = Basis Point 
03 = Re-Invested [[Dividend]]  
04 = CDSC Advance 
05 = Promotional  
06 = Finders Fee  
07 = 12b-1 Fee 
08 = Supplemental 
09 = Negotiated Commission  
10 = Pre-Paid Commission  
11 = Wrap Fee Commission 
12 = Finder Fee Wire Commission  
13 = Service Fee 
14 = Record-keeping Fee  
15 = Advisor Paid Fee 
16 = 401(K) Fee 
17 = Level Indirect Retirement Plan 
Compensation 
18 = Level Fee Based Retirement Plan 
Compensation 
 
Best Practice: 
This field should be populated with the same 
value (commission type) as the original 
payment that is being returned. 
R 

---

## Page 6

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Returned Payments Header Record 6 
Field Name Start End Len Type Description Opt/ 
Req 
Debit/Credit Indicator 40 40 1 N 2 = Credit 
 
This record must be a Credit (return payment to 
the original payer) 
R 
Filler 41 41 1 A/N Space R 
[[settlement]] Indicator 42 42 1 A/N ‘ ‘ = [[settlement]] 
1 = No [[settlement]]  
2 = Test 
(Space or 1 required if Commission Type = 10) 
 
Space = [[settlement]] 
OC 
Record Date 43 50 8 N mmddccyy 
 
(12B-1 funds) 
O 
Security Issue [[ID]] Indicator 51 51 1 A/N Blank 
1 = Internal client-created Security Issue [[ID]] 
2 = Registered Product-Level Security Issue [[ID]] 
 
This field is Required (must be populated with 
“1” or “2”) if “Commission Type” field 
= 17 or 18 
OC 
Filler 52 84 33 A/N Space R 
Returned Payment 
Reason Code 
85 86 2 A/N 01 = Commission Type / Social Code 
combination not allowed by firm 
 
02 = Non Approved Provider 
R 
Reject Code # 1 87 88 2 A/N Input: Filler - Space Output: Reject Code # 1 O 
Reject Code # 2 89 90 2 A/N Input: Filler - Space Output: Reject Code # 2 O 
Reject Code # 3 91 92 2 A/N Input: Filler - Space Output: Reject Code # 3 O 
Reject Code # 4 93 94 2 A/N Input: Filler - Space Output: Reject Code # 4 O 
Reject Code # 5 95 96 2 A/N Input: Filler - Space Output: Reject Code # 5 O 
Reject Code # 6 97 98 2 A/N Input: Filler - Space Output: Reject Code # 6 O 
Reject Code # 7 99 100 2 A/N Input: Filler - Space Output: Reject Code # 7 O 

---

## Page 7

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Security Header Record 7 
MUTUAL FUND [[DTCC]] PAYMENT AXIS SECURITY 
HEADER RECORD 
Input/Output 
Notes: 
1. Header Record 30 is NOT allowed when Header Record 15 is provided. 
2. Detail Records 31 received in combination with a Header Record 30 or Header Record 15 where “[[settlement]] 
Indicator” field is populated with “1=No [[settlement]]” or “2=Test” will NOT be settled through [[DTCC]] Payment aXis. 
Mutual Fund [[DTCC]] Payment aXis Security Header Record 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N B = Delivering Firm  
F = Fund 
R 
Record type 2 3 2 N 30 = Header R 
Filler 4 5 2 A/N Space R 
Receiving Firm # 6 9 4 N  R 
Agent For Receiving Firm 10 13 4 A/N  O 
Delivering Firm/Fund # 14 17 4 A/N  R 
Security Issue Country 
Code 
18 19 2 A/N Space R 
Security Issue [[ID]] 20 28 9 A/N Can be registered or non-registered Security 
Issue [[ID]] 
Best Practice: 
Best practice algorithm for internal client- 
created (non-registered) Security Issue IDs: 
NNNNXXXXX, where 
• NNNN = [[NSCC]] [[participant]] number of 
the record submitter 
• XXXXX = alpha/numeric sequence 
R 
Security Issue Check Digit 29 29 1 A/N Space R 
Fund/Firm Processing 
Date 
30 37 8 N mmddccyy R 

---

## Page 8

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Security Header Record 8 
Field Name Start End Len Type Description Opt/ 
Req 
Commission Type 38 39 2 A/N 01 = Front End  
02 = Basis Point 
03 = Re-Invested [[Dividend]]  
04 = CDSC Advance 
05 = Promotional  
06 = Finders Fee  
07 = 12b-1 Fee 
08 = Supplemental 
09 = Negotiated Commission  
10 = Pre-Paid Commission  
11 = Wrap Fee Commission 
12 = Finder Fee Wire Commission  
13 = Service Fee 
14 = Record-keeping Fee  
15 = Advisor Paid Fee 
16 = 401(K) Fee 
17 = Level Indirect Retirement Plan 
Compensation 
18 = Level Fee Based Retirement Plan 
Compensation 
 
Best Practice: 
Commission Types 17 and 18 will be provided 
by record keepers when communicating and 
remitting “levelized” compensation to firms. 
R 
Debit/Credit Indicator 40 40 1 N 1 = Debit 
2 = Credit 
R 
Debit Reason Code 41 41 1 A/N Required If Debit/Credit Indicator = 1 
 
1 = Adjustment Reclaim  
2 = Commission Reclaim 
3 = Statement of Intent Reclaim  
4 = Trade Cancellation 
5 = Other 
OC 

---

## Page 9

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Security Header Record 9 
Field Name Start End Len Type Description Opt/ 
Req 
[[settlement]] Indicator 42 42 1 A/N ‘ ‘ = [[settlement]] 
1 = No [[settlement]]  
2 = Test 
 
(Space or 1 required if Commission Type = 10) 
OC 
Record Date 43 50 8 N mmddccyy  
(12B-1 funds) 
O 
Security Issue [[ID]] Indicator 51 51 1 A/N • Blank 
• 1 = Internal client-created Security Issue [[ID]] 
• 2 = Registered Product-Level Security 
Issue [[ID]] 
 
This field is Required (must be populated with 
“1” or “2”) if “Commission Type” field = 17 or 18 
OC 
Filler 52 86 35 A/N Space R 
Reject Code # 1 87 88 2 A/N Input: Filler - Space Output: Reject Code # 1 O 
Reject Code # 2 89 90 2 A/N Input: Filler - Space Output: Reject Code # 2 O 
Reject Code # 3 91 92 2 A/N Input: Filler - Space Output: Reject Code # 3 O 
Reject Code # 4 93 94 2 A/N Input: Filler - Space Output: Reject Code # 4 O 
Reject Code # 5 95 96 2 A/N Input: Filler - Space Output: Reject Code # 5 O 
Reject Code # 6 97 98 2 A/N Input: Filler - Space Output: Reject Code # 6 O 
Reject Code # 7 99 100 2 A/N Input: Filler - Space Output: Reject Code # 7 O 
 
 
 
  

---

## Page 10

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Detail Record #1 10 
MUTUAL FUND [[DTCC]] PAYMENT AXIS DETAIL RECORD 
#1 
Input/Output 
Mutual Fund [[DTCC]] Payment aXis Detail Record #1 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N B = Delivering Firm 
F = Fund 
R 
Record Type 2 3 2 A/N 31 R 
Sequence Number 4 4 1 A/N 1=Detail Comm. [[settlement]] R 
Networking Control 
Indicator 
5 5 1 A/N 0 = Not Networked 
3 = Matrix Level 3 
4 = Matrix Level 4 
R 
Commission Amount 6 21 16 N 99,999,999,999,999.99 R 
Customer Account 
Indicator 
22 22 1 A/N 1 = Dealer 
2 = Fund 
R 
Customer Account 23 42 20 A/N  R 
SSN/EIN Number 
Indicator 
43 43 1 A/N 0 = Tax [[ID]] Number 
1 = Social Security Number 
2 = [[investor]] TIN/EIN  
R 
SSN/EIN Number  44 52 9 A/N  R 
Branch [[ID]] Number 53 61 9 A/N  R 
Account Representative 
Number 
62 70 9 A/N  O 
Wrap Account Indicator 71 71 1 A/N 0 = Non-Wrap Account 
1 = Wrap Account 
R 
Name Indicator 72 72 1 A/N Required if name is not blank; 
‘C’ = Customer name  
‘R’ = Representative name 
OC 
Name 73 87 15 A/N  O 

---

## Page 11

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Detail Record #1 11 
Field Name Start End Len Type Description Opt/ 
Req 
Social Code 88 89 2 A/N See Social Code list at 
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html 
under General Codes on the [[DTCC]] Learning 
Center. 
R 
Filler 90 100 11 A/N Space R 
 
 
 
  

---

## Page 12

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Detail Record #2 12 
MUTUAL FUND [[DTCC]] PAYMENT AXIS DETAIL RECORD 
#2 
Input/Output 
Note:  
Required for trade related commission types (01, 02, 03, 04) 
Mutual Fund [[DTCC]] Payment aXis Detail Record #2 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N B = Delivering Firm 
F = Fund 
R 
Record Type 2 3 2 A/N 31 R 
Sequence Number 4 4 1 A/N 2 R 
Name Indicator 5 5 1 A/N Required if name is not blank; 
‘C’ = Customer name 
‘R’ = Representative name 
OC 
Name 6 20 15 A/N Name 2 O 
Commission Rate 21 25 5 N 9.9999 
Required if Commission Type = 01, 02, 03 or 04 
OC 
Gross Amount of 
Trade/Total Security 
Assets 
26 41 16 N 99,999,999,999,999.99 
Required if Commission Type = 01, 02, 03 or 04 
OC 
Share Quantity of Trade 42 54 13 N 999,999,999.9999 
Required if Commission Type = 01, 02, 03 or 04 
OC 
Price per Share 55 66 12 N 999,999.999999 
Required if Commission Type = 01, 02, 03 or 04 
OC 
Currency Indicator 67 69 3 A/N USD or spaces R 
Trade Date 70 77 8 A/N mmddccyy 
Required if Commission Type = 01, 02, 03 or 04 
OC 
Transaction Type 78 78 1 A/N Required if Commission Type = 01, 02, 03 or 
04. 
1 = Initial Purchase 
2 = Subsequent Purchase 3 = Wrap Purchase 
4 = 529 Purchase 
5 = Systematic Investment Purchase 
OC 

---

## Page 13

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Detail Record #2 13 
Field Name Start End Len Type Description Opt/ 
Req 
Assets Eligible for Trails 79 94 16 N 99,999,999,999,999.99 O 
Filler 95 100 6 A/N Space R 
 
 
  

---

## Page 14

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Detail Record #3 14 
MUTUAL FUND [[DTCC]] PAYMENT AXIS DETAIL RECORD 
#3 
Input/Output 
Notes: 
This record is optional 
Mutual Fund [[DTCC]] Payment aXis Detail Record #3 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N B = Delivering Firm  
F = Fund 
R 
Record Type 2 3 2 A/N 31 R 
Sequence Number 4 4 1 A/N 3 R 
Plan Account Number 5 24 20 A/N Plan Account at the Trust, TPA, or Record 
Keeper 
O 
Plan Account Number 
Indicator 
25 25 1 A/N Required if Plan Account Number is provided 
 
1 = Trust 
2 = TPA 
3 = Record Keeper 
OC 
Customer Account 
Indicator 2 
26 26 1 A/N 1 = Dealer 
2 = Fund 
 
Required if “Customer Account 2” field is 
populated 
 
Best Practice: 
• “Customer Account Indicator 2” and 
“Customer Account 2” fields will be used in 
combination with the “Customer Account 
Indicator” and “Customer Account” fields. 
Clients should provide both the Dealer and 
Fund account numbers (if both accounts 
are available).
 
• The value in this field should not be the 
same as the value in the “Customer 
Account Indicator” field. 
OC 

---

## Page 15

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Detail Record #3 15 
Field Name Start End Len Type Description Opt/ 
Req 
Customer Account 2 27 46 20 A/N Required if “Customer Account Indicator 2” field 
is populated 
 
Customer Account (Dealer or Fund) as 
specified in the “Customer Account Indicator 2” 
field 
 
Best Practice: 
The value in this field should not be the same 
as the value in the “Customer Account” field. 
OC 
Filler 47 100 54 A/N Space R 
 
 
  

---

## Page 16

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Security Trailer Record 16 
MUTUAL FUND [[DTCC]] PAYMENT AXIS SECURITY 
TRAILER RECORD 
Input/Output 
Mutual Fund [[DTCC]] Payment aXis Security Trailer Record 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N B = Delivering Firm 
F = Fund 
The value in this field Must be the same as the 
value on the Header record 30 or Header record 
15. 
R 
Record Type 2 3 2 A/N 32 R 
Filler 4 9 6 A/N Space R 
Delivering Firm/Fund # 10 13 4 A/N The value in this field Must be the same as the 
value on the Header record 30 or Header record 
15. 
R 
Security Issue Country 
Code 
14 15 2 A/N Space R 
Security Issue [[ID]] 16 24 9 A/N The value in this field Must be the same as the 
value on the Header record 30 or Header record 
15. 
R 
Security Issue Check Digit 25 25 1 A/N Space R 
Total Records 26 33 8 N 99,999,999  
Including Header and Trailer 
R 
Debit/Credit Indicator 34 34 1 A/N 1 = Debit 
2 = Credit 
Value ‘1’ = Debit is NOT allowed in combination 
with Header Record ‘15’ 
The value in this field Must be the same as the 
value on the Header record 30 or Header record 
15. 
R 
Dollar Amount 35 50 16 N 99,999,999,999,999.99 R 
Filler 51 86 36 A/N Space R 
Reject Code #1 87 88 2 A/N Input: Space 
Output: Reject Code #1 
R 
Reject Code #2 89 90 2 A/N Input: Space 
Output: Reject Code #2 
R 

---

## Page 17

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Security Trailer Record 17 
Field Name Start End Len Type Description Opt/ 
Req 
Reject Code #3 91 92 2 A/N Input: Space 
Output: Reject Code #3 
R 
Reject Code #4 93 94 2 A/N Input: Space 
Output: Reject Code #4 
R 
Reject Code #5 95 96 2 A/N Input: Space 
Output: Reject Code #5 
R 
Reject Code #6 97 98 2 A/N Input: Space 
Output: Reject Code #6 
R 
Reject Code #7 99 100 2 A/N Input: Space 
Output: Reject Code #7 
R 
 
 
 
  

---

## Page 18

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Grand Total Input/Output Trailer Record 18 
MUTUAL FUND [[DTCC]] PAYMENT AXIS GRAND TOTAL 
INPUT/OUTPUT TRAILER RECORD 
Input from Fund, Output to Fund (If Rejected)  
Input from Firm, Output to Firm (If Rejected) 
Mutual Fund [[DTCC]] Payment aXis Grand Total Input/Output Trailer Record 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N B = Delivering Firm  
F = Fund 
The value in this field Must be the same as the 
value on the Header record 30 or 
Header record 15. 
R 
Record Type 2 3 2 A/N 33 R 
Filler 4 5 2 A/N Space R 
Receiving Firm / Fund # 6 9 4 A/N The value in this field Must be the same as the 
value on the Header record 30 or Header record 
15. 
R 
Delivering Firm/Fund # 10 13 4 A/N The value in this field Must be the same as the 
value on the Header record 30 or Header record 
15. 
R 
Total Records 14 22 9 N 999,999,999 
Including Headers and Trailers 
R 
Total Debit Dollar Amount 23 38 16 N 99,999,999,999,999.99 R 
Total Credit Dollar Amount 39 54 16 N 99,999,999,999,999.99 R 
Filler 55 86 32 A/N Space R 
Reject Code #1 87 88 2 A/N Input: Space 
Output: Reject Code #1 
R 
Reject Code #2 89 90 2 A/N Input: Space 
Output: Reject Code #2 
R 
Reject Code #3 91 92 2 A/N Input: Space 
Output: Reject Code #3 
R 
Reject Code #4 93 94 2 A/N Input: Space 
Output: Reject Code #4 
R 
Reject Code #5 95 96 2 A/N Input: Space 
Output: Reject Code #5 
R 

---

## Page 19

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Grand Total Input/Output Trailer Record 19 
Field Name Start End Len Type Description Opt/ 
Req 
Reject Code #6 97 98 2 A/N Input: Space 
Output: Reject Code #6 
R 
Reject Code #7 99 100 2 A/N Input: Space 
Output: Reject Code #7 
R 
 
 
 
 
  

---

## Page 20

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Service DataTrak Header Record 20 
MUTUAL FUND [[DTCC]] PAYMENT AXIS SERVICE 
DATATRAK HEADER RECORD 
Input from Fund / Firm to [[NSCC]] 
Mutual Fund [[DTCC]] Payment aXis Service DataTrak Header Record 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value ‘HDR.S’ R 
DATATRAK SYSID 6 10 5 A/N Value ‘26088’ R 
Literal 11 16 6 A/N Value ‘.E00.C’ R 
Originator Clearing # 17 20 4 A/N  R 
Literal 21 22 2 A/N Value ‘.S’ R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value ‘COMMISSION [[settlement]]’ R 
Multi Batch Indicator 60 60 1 A/N Single Batch = Space  
Multi Batch = N 
Last Batch = Y 
R 
Multi Batch Number 61 63 3 N Zeroes when not Multi Batch R 
Filler 64 100 37 A/N Space R 
 
 
 
  

---

## Page 21

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Service DataTrak Trailer Record 21 
MUTUAL FUND [[DTCC]] PAYMENT AXIS SERVICE 
DATATRAK TRAILER RECORD 
Input from Fund / Firm to [[NSCC]] 
Mutual Fund [[DTCC]] Payment aXis Service DataTrak Trailer Record 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value ‘END.S’ R 
DATATRAK SYSID 6 10 5 A/N Value ‘26088’ R 
Literal 11 16 6 A/N Value ‘.E00.C’ R 
Originator Clearing # 17 20 4 A/N  R 
Literal 21 22 2 A/N Value ‘.S’ R 
Sub Originator 23 26 4 A/N  R 
Data File Record Count 27 33 7 N Datatrak Header or Trailer not included in count R 
Filler 34 100 67 A/N Space R 
 
 
 
  

---

## Page 22

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Detail Reject Record 22 
MUTUAL FUND [[DTCC]] PAYMENT AXIS DETAIL REJECT 
RECORD 
Output from [[NSCC]] to Funds/Firms 
Mutual Fund [[DTCC]] Payment aXis Detail Reject Record 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N B = Delivering Firm  
F = Fund 
Record Type 2 3 2 A/N 31 
Sequence Number 4 4 1 A/N 9=Detail Reject Record 
Networking Control 
Indicator 
5 5 1 A/N 0 = Not Networked  
3 = Matrix Level 3 
4 = Matrix Level 4 
Commission Amount 6 21 16 N 99,999,999,999,999.99 
Customer Account 
Indicator 
22 22 1 A/N 1 = Dealer 
2 = Fund 
Customer Account 23 42 20 A/N  
SSN/EIN Number 
Indicator 
 
43 43 1 A/N 0 = Tax [[ID]] Number 
1 = Social Security Number 
2= [[investor]] TIN/EIN 
SSN/EIN Number 44 52 9 A/N  
Branch Number 53 61 9 A/N  
Account Representative 
Number 
62 70 9 A/N  
Wrap Account Indicator 71 71 1 A/N 0 = No-Wrap Account  
1 = Wrap Account 
Reject Code #1 72 73 2 A/N  
Reject Code #2 74 75 2 A/N  
Reject Code #3 76 77 2 A/N  
Reject Code #4 78 79 2 A/N  
Reject Code #5 80 81 2 A/N  
Reject Code #6 82 83 2 A/N  

---

## Page 23

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Detail Reject Record 23 
Field Name Start End Len Type Description 
Reject Code #7 84 85 2 A/N  
Filler 86 87 2 A/N Space 
Social Code 88 89 2 A/N  
Filler 90 100 11 A/N Space 
 
 
 
  

---

## Page 24

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Grand Total Trailer Record 24 
MUTUAL FUND [[DTCC]] PAYMENT AXIS GRAND TOTAL 
TRAILER RECORD 
Output from [[NSCC]] to Receiving Firms 
Mutual Fund [[DTCC]] Payment aXis Grand Total Trailer Record 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 34 
Filler 4 5 2 A/N Space 
Receiving Firm # 6 9 4 A/N  
Processing Date 10 17 8 A/N mmddccyy 
Total Records 18 26 9 N 999,999,999 
Including Headers and Trailers 
Debit Dollar Amount 27 42 16 N 99,999,999,999,999.99 
Credit Dollar Amount 43 58 16 N 99,999,999,999,999.99 
Filler 59 100 42 A/N Space 
  

---

## Page 25

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Security Issue [[ID]] [[settlement]] Detail Record 25 
MUTUAL FUND [[DTCC]] PAYMENT AXIS SECURITY ISSUE 
[[ID]] [[settlement]] DETAIL RECORD 
Output from [[NSCC]] to Firms and Funds 
Mutual Fund [[DTCC]] Payment aXis Security Issue [[ID]] [[settlement]] Detail Record 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 N 38 = Security Issue [[ID]] [[settlement]] Detail 
Filler 4 5 2 A/N Space 
MRO Recipient Number 6 9 4 N  
Security Issue Country 
Code 
10 11 2 A/N  
Security Issue [[ID]] 12 20 9 A/N  
Security Issue Check Digit 21 21 1 A/N  
Pay - Receive Code 22 22 1 N 2 = Your Debit  
4 = Your Credit 
Contra Clearing Number 23 26 4 N  
[[settlement]] Date 27 34 8 N mmddccyy 
Processing Date 35 42 8 N mmddccyy 
[[settlement]] Value 43 58 16 N 99,999,999,999,999.99 
Currency Indicator 59 61 3 A/N For future use 
Omni Pay-Receive Code 62 62 1 N 2 = Your Debit  
4 = Your Credit 
Omni [[settlement]] Value 63 79 17 N 999,999,999,999,999.99 
TPA/Investment Agent or 
Firm Number * 
80 83 4 A/N  
Filler 84 99 16 A/N Space 
MRO Recipient Type 100 100 1 A/N A = Investment Agent*  
B = Delivering Firm 
F = Fund 
T = TPA* 
 

---

## Page 26

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis [[settlement]] Record by Contra [[participant]] 26 
MUTUAL FUND [[DTCC]] PAYMENT AXIS [[settlement]] 
RECORD BY CONTRA [[participant]] 
Output from [[NSCC]] to Firms/Funds 
Mutual Fund [[DTCC]] Payment aXis [[settlement]] Record By Contra [[participant]] 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 N 39 = Contra [[participant]] [[settlement]] Detail 
Filler 4 5 2 A/N Space 
MRO Recipient Number 6 9 4 N  
Pay/Receive Code 10 10 1 N 2 = Your Debit  
4 = Your Credit 
Contra Clearing Number 11 14 4 N  
[[settlement]] Date 15 22 8 N mmddccyy 
Processing Date 23 30 8 N mmddccyy 
[[settlement]] Value 31 46 16 N 99,999,999,999,999.99 
Currency Indicator 47 49 3 A/N For future use 
Omni Pay-Receive Code 50 50 1 N 2 = Your Debit  
4 = Your Credit 
Omni [[settlement]] Value 51 67 17 N 999,999,999,999,999.99 
Filler 68 99 32 A/N Space 
MRO Recipient Type 100 100 1 A/N A = Investment Agent*  
B = Delivering Firm 
F = Fund  
T = TPA* 
 
 
  

---

## Page 27

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Grand Total [[settlement]] Record 27 
MUTUAL FUND [[DTCC]] PAYMENT AXIS GRAND TOTAL 
[[settlement]] RECORD 
Output from [[NSCC]] to Firms/Funds 
Mutual Fund [[DTCC]] Payment aXis Grand Total [[settlement]] Record 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 N 40 = Grand Total [[settlement]] 
Filler 4 5 2 A/N Space 
MRO Recipient Number 6 9 4 N  
Pay/Receive Code 10 10 1 N 2 = Your Debit  
4 = Your Credit 
[[settlement]] Date 11 18 8 N mmddccyy 
Processing Date 19 26 8 N mmddccyy 
[[settlement]] Value 27 42 16 N 99,999,999,999,999.99 
Currency Indicator 43 45 3 A/N For future use 
Omni Pay-Receive Code 46 46 1 N 2 = Your Debit  
4 = Your Credit 
Omni [[settlement]] Value 47 63 17 N 999,999,999,999,999.99 
Filler 64 99 36 A/N Space 
MRO Recipient Type 100 100 1 A/N A = Investment Agent*  
B = Delivering Firm 
F = Fund  
T = TPA* 

---

## Page 28

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Service Output Header Record 28 
MUTUAL FUND [[DTCC]] PAYMENT AXIS SERVICE OUTPUT 
HEADER RECORD 
Mutual Fund [[DTCC]] Payment aXis Service Output Header Record 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 4 1 N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '11111111111' 
Transmission Date 20 27 8 A/N mmddccyy 
Autoroute File [[ID]] 28 35 8 A/N Value '02102202' 
Literal 36 45 10 A/N Value ‘COMMISSION’ 
Filler 46 100 55 A/N Space 
 

---

## Page 29

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis [[settlement]] Summary Output Header Record 29 
MUTUAL FUND [[DTCC]] PAYMENT AXIS [[settlement]] 
SUMMARY OUTPUT HEADER RECORD 
Mutual Fund [[DTCC]] Payment aXis [[settlement]] Summary Output Header Record 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 4 1 N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '11111111111' 
Transmission Date 20 27 8 A/N mmddccyy 
Autoroute File [[ID]] 28 35 8 A/N Value ' 02102203' 
Literal 36 45 10 A/N Value ‘COMMISSION’ 
Filler 46 100 55 A/N Space 
 
 
 
  

---

## Page 30

Commission & Fee [[settlement]] Record Layouts 
Mutual Fund [[DTCC]] Payment aXis Input Acknowledgement Record 30 
MUTUAL FUND [[DTCC]] PAYMENT AXIS INPUT 
ACKNOWLEDGEMENT RECORD 
Output from [[NSCC]] to Fund/Firm 
Mutual Fund [[DTCC]] Payment aXis Input Acknowledgement Record 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N CM = Commission [[settlement]] 
Filler 4 5 2 A/N Space 
Delivering Fund/Firm # 6 9 4 N  
Processing Date 10 17 8 N mmddccyy 
Total Records in File 18 25 8 N 999,999,999 
Including Headers and Trailers 
Debit Dollar Amount, 
Accepted Records 
26 41 16 N 99,999,999,999,999.99 
Credit Dollar Amount, 
Accepted Records 
42 57 16 N 99,999,999,999,999.99 
Debit Dollar Amount, 
Rejected Records 
58 73 16 N 99,999,999,999,999.99 
Credit Dollar Amount, 
Rejected Records 
74 89 16 N 99,999,999,999,999.99 
Filler 90 100 11 A/N Space 
 
 
  

---

## Page 31

Commission & Fee [[settlement]] Record Layouts 
APPENDIX – Summary of Changes 31 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 
 
  

---

## Page 32

Commission & Fee [[settlement]] Record Layouts 
Summary of Changes – effective Q1, 2019 32 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 
 
  

---

## Page 33

Commission & Fee [[settlement]] Record Layouts 
Summary of changes – effective Q4, 2017 33 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2017 
RENAME EXISTING FIELDS 
Old Field Name Record Type and Location New Name 
SSN/TIN Number Indicator B/F 31 seq.#1, start 43, end 43, length 1, A/N, R SSN/EIN Number Indicator 
SSN/TIN Number B/F 31 seq.#1, start 44, end 52, length 9, A/N, R SSN/EIN Number 
SSN/TIN Indicator B/F 31 seq.#1, start 43, end 43, length 1, A/N 
(Output Record from [[NSCC]] – Detail Reject 
Record) 
 
SSN/EIN Number Indicator 
SSN/TIN B/F 31 seq.#1, start 44, end 52 length 9, A/N 
(Output Record from [[NSCC]] – Detail Reject 
Record) 
 
SSN/EIN Number 
 
ADD NEW VALUE FOR EXISTING FIELDS 
New Field Name Record Type, Location, field type New Value added 
SSN/EIN 
Number Indicator 
B/F 31 seq.#1, start 43, end 43, length 1, A/N 0 = Tax [[ID]] Number 
1 = Social Security Number 
2 = [[investor]] TIN/EIN 
SSN/EIN 
Number Indicator 
B/F 31 seq.#1, start 43, end 43, length 1, A/N (Output 
Record from [[NSCC]] – Detail Reject Record) 
0 = Tax [[ID]] Number 
1 = Social Security Number 
2 = [[investor]] TIN/EIN 
 
  

---

## Page 34

Commission & Fee [[settlement]] Record Layouts 
Summary of changes – effective Q1, 2017 34 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2017 
ADD NEW RECORD 
Record Record Name Requirements 
B15 Sequence #1 Mutual Fund [[DTCC]] Payment aXis 
Returned Payments Header Record 
This record can be submitted by Firms only. 
Firms will utilize this Header record to return 
payments to the original deliverer. 
 
ADD NEW FIELD 
New Field Name Record Type and field location New Field Name 
Security Issue [[ID]] 
Indicator 
B/F30 seq#1, start 51, end 51, length 1, 
OC, A/N 
• Blank 
• 1 = Internal client-created Security Issue 
[[ID]] 
• 2 = Registered Product-Level Security 
Issue [[ID]] 
This field is Required (must be populated with “1” or 
“2”) if “Commission Type” field = 17 or 18 
Customer Account 
Indicator 2 
B/F31 seq#3, start 26, end 26, length 1, 
O, A/N 
1 = Dealer 
2 = Fund 
Required if “Customer Account 2” field is populated 
 
Best Practice: 
• “Customer Account Indicator 2” and 
Customer Account 2” fields will be used in 
combination with the existing Customer 
Account Indicator” and “Customer 
Account” fields. Clients should provide 
both the Dealer and Fund account 
numbers 
(if both accounts are available). 
• The value in this field should not be the 
same as the value in the “Customer 
Account Indicator” field. 
Customer Account 2 B/F31 seq#3, start 27, end 46, length 20, 
O, A/N 
Required if “Customer Account Indicator 2” field is 
populated 
Customer Account (Dealer or Fund) as specified in 
the “Customer Account Indicator 2” field 
Best Practice: 
The value in this field should not be the same as the 
value in the “Customer Account” field. 
 

---

## Page 35

Commission & Fee [[settlement]] Record Layouts 
Summary of changes – effective Q1, 2017 35 
ADD NEW VALUE FOR EXISTING FIELDS  
Field Name Record Type and field location New Field Name 
Commission Type B/F30 seq#1, start 38, end 39, length 2, 
R, A/N 
17 = Level Indirect Retirement Plan Compensation 
18 = Level Fee Based Retirement Plan 
Compensation  
Best Practice:  
Commission Types 17 and 18 will be provided by 
record-keepers when communicating and remitting 
“levelized” compensation to firms. 
Transaction Type B/F31 seq#2, start 78, end 78, length 1, 
OC,A/N 
5 = Systematic Investment Purchase 
 
CHANGE REQUIREMENT FOR EXISTING FIELD  
Field Name Record Type and field location Old Requirement New Requirement 
Debit/Credit Indicator B/F 32 seq.#1, start 34, end 34, length 1, 
A/N, Req 
1 = Debit  
2 = Credit 
1 = Debit  
2 = Credit  
Value ‘1’ = Debit is NOT 
allowed in combination with 
Header Record ‘15’. 
 
RENAME EXISTING FIELDS (DOCUMENTATION CHANGES) 
New Field Name Record Type and field location Old Field Name 
Receiving Firm 
/ Fund # 
B/F 33 seq.#1, start 6, end 9, length 4, 
Req, A/N 
Receiving Firm # 
Social Code B/F 31 seq.#9, start 88 end 89, length 2 
(Output Record from [[NSCC]] – Detail 
Reject Record) 
Filler 
 
DOCUMENTATION CHANGES – CLARIFY FIELD DESCRIPTIONS  
The following fields will be updated in the description section of the record layouts to clearly indicate the current 
[[NSCC]] editing rules to state that the values in these fields must match the values prov ided on the Header 
Record 30 and Header Record 15. There are NO system changes. This is a documentation change only.  
Field Name Record Type and field location Requirement and Description 
System Code B/F 32 seq.#1, start 1, end 1, length 1, Req, A/N 
B/F 33 seq.#1, start 1, end 1, length 1, Req, A/N 
The value in this field Must be the same as 
the value on the Header record 30 or 
Header record 15. 
Receiving Firm 
/ Fund # 
B/F 33 seq.#1, start 6, end 9, length 4, Req, A/N The value in this field Must be the same as 
the value on the Header record 30 or 
Header record 15. 

---

## Page 36

Commission & Fee [[settlement]] Record Layouts 
Summary of changes – effective Q1, 2017 36 
Field Name Record Type and field location Requirement and Description 
Delivering Firm/Fund # B/F 32 seq.#1, start 10, end 13, length 4, Req, A/N 
B/F 33 seq.#1, start 10, end 13, length 4, Req, A/N 
The value in this field Must be the same as 
the value on the Header record 30 or 
Header record 15. 
 
Security Issue [[ID]] 
 
B/F 32 seq.#1, start 16, end 24, length 9, Req, A/N 
The value in this field Must be the same as 
the value on the Header record 30 or 
Header record 15. 
 
Debit/Credit Indicator 
 
B/F 32 seq.#1, start 34, end 34, length 1, Req, A/N 
The value in this field Must be the same as 
the value on the Header record 30 or 
Header record 15. 
 
DOCUMENTATION CHANGES – ALIGN FIELD REQUIREMENTS TO FIELD DESCRIPTIONS (UPDATE 
FROM “OPTIONAL” TO “OPTIONAL CONDITIONAL”) 
The following fields are currently described and edited as Optional/Conditional; however they are classified as 
Optional in the “Optional/Conditional” column of the record layouts. This is a documentation change only to 
update these fields’ classification from “Optional” to “Optional/Conditional” in the “Optional/Conditional” column 
of the record layouts. 
Field Name Record Type and field location Old New 
Debit Reason Code B/F 30 seq.#1, start 41, end 41, length 1, A/N O OC 
[[settlement]] Indicator B/F 30 seq.#1, start 42, end 42, length 1, A/N O OC 
Name Indicator B/F 31 seq.#1, start 72, end 72, length 1, A/N O OC 
Name Indicator B/F 31 seq.#2, start 5 end 5, length 1, A/N O OC 
Commission Rate B/F 31, seq.#2, start 21, end 25, length 5, N O OC 
Gross Amount of Trade/Total Security Assets B/F 31 seq.#2, start 26, end 41, length 16, N O OC 
Share Quantity of Trade B/F 31 seq.#2, start 42, end 54, length 13, N O OC 
Price per Share B/F 31 seq.#2, start 55, end 66, length 12, N O OC 
Trade Date B/F 31 seq.#2, start 70, end 77, length 8, A/N O OC 
Transaction Type B/F 31 seq.#2, start 78, end 78, length 1, A/N O OC 
REJECT CODES  
The following new reject code have been added: 
New Field Name Record Type and field location 
R0 Security Issue [[ID]] Indicator is missing/invalid 
X5 Returned Payment Reason Code is Missing/Invalid 
X6 Customer Account Indicator 2 is Missing/Invalid 
X7 Customer Account 2 is Missing 

---

## Page 37

Commission & Fee [[settlement]] Record Layouts 
Summary of changes – effective Q2, 2015 37 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2015 
REQUIREMENTS CHANGED FOR EXISTING FIELD 
Field Name Record Type and Location Old Requirement New Requirement 
Social Code B/F 31 seq.#1, start 88, end 89, length 2, A/N Optional Required 
 
 
  

---

## Page 38

Commission & Fee [[settlement]] Record Layouts 
Summary of changes – effective Q4, 2013 38 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2013 
EXISTING FILLER CORRECTION 
Field Name Old Location Corrected Location Comments 
Filler B/F31 seq#1, start 88, end 100, 
length 13, A/N, Required 
B/F31 seq#1, start 90, end 100, 
length 11, A/N, Required 
Documentation Correction 
 
ADD NEW RECORD 
Record Record Name Requirements 
B/F Sequence #3 Mutual Fund [[DTCC]] Payment aXis Detail Record #3 Optional 
 
ADD NEW FIELD 
New Field Name Record Type and Location Requirements 
Plan Account 
Number 
B/F31 seq#3, start 5, end 24, length 20, A/N Plan account at the Trust, TPA, or 
Record Keeper 
Plan Account 
Number Indicator 
B/F31 seq#3, start 25, end 25, length 1, A/N Required if Plan account Number is 
provided 
1 = Trust 
2 = TPA 
3 = Record Keeper 
 
  

---

## Page 39

Commission & Fee [[settlement]] Record Layouts 
Summary of changes – effective Q1 (March 18), 2013 39 
SUMMARY OF CHANGES – EFFECTIVE Q1 (MARCH 18), 
2013 
REQUIREMENTS CHANGED FOR EXISTING FIELD 
Field Name Location Old Requirement New Requirement 
Network Control 
Indicator 
B/F 31 seq.#1, start 5, 
end 5, length 1, Required 
0 = Not Networked 
1 through ‘4’ = Level # 
0 = Not Networked  
3 = Matrix Level 3 
4 = Matrix Level 4 
 
(Removed 1 = Level 1; 2 = Level 2 
effective Q1, 2013) 
Description also updated to “Matrix 
Level” 
Network Control 
Indicator 
B/F 31 seq.#9, start 5, 
end 5, length 1, Required 
0 = Not Networked 
1 through ‘4’ = Level # 
0 = Not Networked  
3 = Matrix Level 3 
4 = Matrix Level 4 
 
(Removed 1 = Level 1; 2 = Level 2 
effective Q1, 2013) 
Description also updated to “Matrix 
Level” 
 
  

---

## Page 40

Commission & Fee [[settlement]] Record Layouts 
Summary of changes – effective Q1 (February 11), 2013 40 
SUMMARY OF CHANGES – EFFECTIVE Q1 (FEBRUARY 
11), 2013 
RENAME COMMISSION [[settlement]] 
In light of the enhancements to the Commission [[settlement]] Service, allowing for the invoicing and [[settlement]] 
of Omnibus invoices and to better capture the essence of the service, as part of implementation, the system 
was renamed to [[DTCC]] Payment aXis. 
ADD NEW FIELD 
New Field Name Record Type and Location Requirements 
Omni Pay-Receive Code N38, start 62, end 62, Length 1, N 
N39, start 50, end 50, Length 1, N 
N40, start 46, end 46, Length 1, N 
2 = Your Debit  
4 = Your Credit 
Omni [[settlement]] Value N38, start 63, end 79, Length 17, N 
N39, start 51, end 67, Length 17, N 
N40, start 47, end 63, Length 17, N 
999,999,999,999,999.99 
TPA/Investment Agent or Firm 
Number* 
N38, start 80, end 83, Length 4, A/N  
MRO Recipient Type N38, start 100, end 100, Length 1, A/N 
N39, start 100, end 100, Length 1, A/N 
N40, start 100, end 100, Length 1, A/N 
A = Investment Agent*  
B = Delivering Firm 
F = Fund  
T = TPA* 
 
This field will be populated when 
the “Omni [[settlement]] Value” field 
is not blank 
 
Note: * Placeholder field/value for Third Party Fees (Omnibus Invoicing Phase II) 
 

---

## Page 41

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. 
TOGETHER, and the Interlocker graphic are registered and unregistered trademarks of The Depository Trust & 
Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: August 3, 2023 
Publication Code: MFS311 
Service: Payment aXis 
Title: Commission & Fee [[settlement]] Record Layouts  
 
For More Information 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 