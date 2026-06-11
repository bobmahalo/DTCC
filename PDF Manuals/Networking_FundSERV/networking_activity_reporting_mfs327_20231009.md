---
title: "Networking - Activity Reporting Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/networking_activity_reporting_mfs327_20231009.pdf"
pages: 52
size: "757.6 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Networking - Activity Reporting Record Layouts

**Original File:** [networking_activity_reporting_mfs327_20231009.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/networking_activity_reporting_mfs327_20231009.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 52  
**File Size:** 757.6 KB  

---

## Page 1

 
 
 
 
 
Networking 
ACTIVITY REPORTING RECORD LAYOUTS 
OCTOBER 9, 2023 
 

---

## Page 2

Activity Reporting Record Layouts 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 4 
Activity Detail (F55) .............................................................................................................................................. 5 
Activity Detail (F55) #1 ........................................................................................................................................ 5 
Activity Detail (F55) #2 ........................................................................................................................................ 9 
Activity Detail (F55) #3 – Supplemental Record ...............................................................................................11 
Activity Detail (F55) #4 ......................................................................................................................................13 
Activity Detail (F55) #5 ......................................................................................................................................15 
Activity Detail (F55) #6 ......................................................................................................................................17 
Activity/Balance Input /Output Trailer (F56) .................................................................................................... 20 
Activity/Balance Input /Output Trailer (F56) #1 .................................................................................................20 
Activity/Balance Input/Output Trailer (F56) #2 ..................................................................................................22 
Year-End Tax Reporting (F45) ........................................................................................................................... 24 
Year-End Tax Reporting (F45) #1 - Year-To-Date ...........................................................................................24 
Year-End Tax Reporting (F45) #2 - Individual Reallocation Record ................................................................26 
Input Records’ Layout ....................................................................................................................................... 28 
Activity File Datatrak Header ............................................................................................................................28 
Activity File Datatrak Trailer ..............................................................................................................................29 
Output Records’ Layout .................................................................................................................................... 30 
Activity [[settlement]] Summary Output Detail (N75) ............................................................................................30 
Activity [[settlement]] Summary Output Trailer (N76) ...........................................................................................32 
Input Acknowledgment - Activity (NAC) ............................................................................................................33 
Output Header Activity File (N00) .....................................................................................................................34 
Output Header - Activity [[settlement]] Summary (N00) .......................................................................................35 
APPENDIX – Summary of Changes .................................................................................................................. 36 
Summary of Changes – effective Q1, 2019 ...................................................................................................... 37 
Summary of changes – effective Q4, 2017 ...................................................................................................... 38 
Summary of changes – effective Q1, 2017 ...................................................................................................... 39 
Summary of changes – effective Q3, 2016 ...................................................................................................... 40 
Summary of changes – effective Q4, 2013 ...................................................................................................... 42 

---

## Page 3

Activity Reporting Record Layouts 
History of Important Notices 3 
Summary of changes – effective Q1, 2013 ...................................................................................................... 44 
Summary of changes – effective Q4 (December 5), 2011 .............................................................................. 47 
Summary of changes – effective Q4 (October 17), 2011 ................................................................................ 48 
Summary of changes – effective Q2, 2011 ...................................................................................................... 51 
 

---

## Page 4

Activity Reporting Record Layouts 
History of Important Notices 4 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notices 
October 9, 2023 Record has been rebranded and reviewed. 
March 25, 2019 Please see Important Notices: 
a8658 P&S 8233 Dated December 19, 2018 
November 20, 2017 Please see Important Notices:  
a8402 P&S 7977Dated June 1, 2017 
February 27, 2017 Please see Important Notices:  
a8286 P&S 7861 Dated November 8, 2016 
September 26, 2016 Please see Important Notices:  
a8159 P&S 7734 Dated February 03, 2016 
November 18, 2013 Please see Important Notices:  
a7665 P&S 7235 Dated July 03, 2013 
December 05, 2011 Please see Important Notices:  
a7256 P&S 6826 Dated July 29, 2011 
October 17, 2011 Please see Important Notices:  
a7241 P&S 6811 Dated July 8, 2011 
June 13, 2011 Please see Important Notices:  
a7175 P&S 6745 Dated March 7th, 2011 
November 22, 2010 Please see Important Notices:  
a7044 P&S 6615 Dated August 17, 2010 
June 14, 2010 Please see Important Notices:  
a6948 P&S 6518 Dated February 18, 2010 
May 18, 2009 Please see Important Notices:  
a6791 P&S 6361 Dated February 17, 2009 
October 20, 2008 Please see Important Notices:  
a6658 P&S 6228 Dated July 11, 2008 
November 20, 2006 Please see Important Notices:  
a6295 P&S 5865 Dated August 29, 2006 
a6272 P&S 5842 Dated July 17, 2006 
Sept. 19, 2005 Please see Important Notice: 
a6035 P&S 5605 Dated May 26, 2005 

---

## Page 5

Activity Reporting Record Layouts 
Activity Detail (F55) 5 
ACTIVITY DETAIL (F55) 
Activity Detail (F55) #1 
Required Record 
Input from Fund 
Output from [[NSCC]] to Firm  
The Networking activity detail record is used by the fund to report non-Fund/SERV trade information to the firm. 
Activity Reporting Records Activity Detail (F55) #1 
#1 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 55 = Activity Detail R 
Sequence Number 4 5 2 A/N 01 R 
Clearing/Settling Firm 
Number 
6 9 4 N  R 
Clearing/Settling Fund 
Number 
10 13 4 N  R 
Security Issue [[ID]] 
Number 
14 22 9 N  R 
Transaction Type 23 24 2 A/N 01 = Direct Purchase  
02 = Direct Redemption  
03 = Pre-Authorized Check (PAC)  
04 = Check Redemption  
05 = LOI Adjustment  
06 = ROA Adjustment  
07 = [[Dividend]] Adjustment  
08 = Long Term Capital Gain Adjustment 
09 = Fund Price Adjustment  
10 = Exchange Ex-Fund/SERV  
11 = [[Fiduciary]] Fees  
12 = Reinvest from other Fund  
13 = Direct Transfer  
14 = Systematic Withdrawal Plan  
15 = Exchange Fee  
16 = Certificate Deposit  
17 = Short Term Cap Gain Adjustment  
18 = [[Dividend]] Related Transaction  
R 

---

## Page 6

Activity Reporting Record Layouts 
Activity Detail (F55) 6 
#1 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
19 = N/A  
20 = N/A  
21 = Share Adjustment  
22 = Share Class Exchange  
23 = Fund Merger Activity  
24 = Purchase Cancellation  
25 = Redemption Cancellation  
26 =Gain on Collectables Adjustment 
27 = Section 1202 Gain Adjustment  
28 = Un-recaptured Section 1250 - Gain 
Adjustment  
29 = Fund Closing  
30 = Small Balance [[liquidation]] 
31 = Target Payment Plans  
32 = Accrual Adjustment  
33 = Transfer From - Cancellation 
34 = Transfer To - Cancellation 
35 = Direct Voluntary Cross Class Exchange   
50 = Closing balance record  
Note: 
Transaction Description Codes can also be used.  
For a complete list of Transaction Description 
Codes please refer to the “Networking Transaction 
Codes” list at https://dtcclearning.com/products-
and-services/mutual-fund-services/codes.html 
Transaction Description Codes “AZ=Initial 
Purchase” and “A@=Subsequent Purchase” added 
as sub-category codes under Transaction Type 
“01=Direct Purchase”. 
 
Best Practice for direct purchase transaction 
description codes: 
• Transaction Description Codes “AZ=Initial 
Purchase” and “A@=Subsequent Purchase” 
should be used in lieu of Transaction Type 
“01=Direct Purchase”. 
• Direct Purchase transactions that utilize 
Transaction Description Codes (other than AZ 
and A@) listed under Transaction Type 
“01=Direct Purchase” on the Networking 
Transaction Codes list should continue to 
provide these sub-category codes. 
Firm/Fund Identification 
Number  
25 44 20 A/N  R 

---

## Page 7

Activity Reporting Record Layouts 
Activity Detail (F55) 7 
#1 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Effective Date 45 52 8 N mmddccyy R 
Share/Balance Amount 53 65 13 N 999,999,999.9999 
Required if Share/Balance Amount - Extended is 
NOT provided in record F55 sequence #4. 
Otherwise, it is not allowed. 
OC 
Share/Balance 
Indicator 
66 66 1 A/N 1 = Book [[shares]]  
2 = Physical [[shares]] 
R 
Debit/Credit Indicator 67 67 1 A/N 1 = Debit ([[shares]] and Money)  
2 = Credit ([[shares]] and Money)  
3 = N/A (for Transaction Type 50) 
R 
Dollar Amount 68 83 16 N Optional if Transaction Type 32 (Accrual 
Adjustment).               
99,999,999,999,999.99 
RC 
Network Control 
Indicator 
84 84 1 A/N 0 = Matrix Level 0  
3 = Matrix Level 3  
4 = Matrix Level 4 
R 
[[Dividend]] Code 85 85 1 N 0 = [[Dividend]] Cash/Ltcg- Cash/Stcg- Cash  
1 = [[Dividend]] Reinvest/Ltcg- Reinvest/Stcg-
Reinvest  
2 = [[Dividend]] Cash/Ltcg- Cash/Stcg- Reinvest  
3 = [[Dividend]] Cash/Ltcg- Reinvest/Stcg-Reinvest  
4 = [[Dividend]] Cash/Ltcg- Reinvest/Stcg-Cash  
5 = [[Dividend]] Reinvest/Ltcg- Cash/Stcg-Cash  
6 = [[Dividend]] Reinvest/Ltcg- Reinvest/Stcg-Cash  
7 = [[Dividend]] Reinvest/Ltcg- Cash/Stcg-Reinvest 
R 
[[Margin]] Account 
Indicator 
86 86 1 A/N 0 = No  
1 = Yes 
R 
Combined TEFRA/NRA 
Indicator 
87 87 1 A/N 1 = Tefra  
2 = NRA  
3 = None 
R 
Load Type Indicator 88 88 1 A/N Required for Transaction Types 01 (including 
Transaction Description Codes starting with ‘A’), 
03, 09, 10 (including Transaction Description 
Codes starting with ‘J’), and 24. 
• 0 = Other  
• 1 = Front-End Load 
OC 

---

## Page 8

Activity Reporting Record Layouts 
Activity Detail (F55) 8 
#1 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Firm/Fund Identification 
Indicator 
89 89 1 A/N 1 = Fund (FIN)  
2 = Firm (BIN) 
R 
Social Code 90 91 2 A/N See Social Code list at  
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html 
R 
Membership Identifier 92 93 2 A/N Required for Transaction Type = 
 13 (Direct Transfer), 
 33 (Transfer from – Cancellation), 
 34 (Transfer to – Cancellation). 
 
00 = N/A 
01 = Trust 
02 = TPA/Investment Agent 
OC 
Opposing Membership 
Identifier 
94 95 2 A/N Required if Transaction Type = 
13 (Direct Transfer);  
33 (Transfer From – Cancellation); 
34 (Transfer To – Cancellation). 
 
Opposing Membership Identifiers: 
 
00 = N/A 
01 = Trust 
OC 
Filler 96 98 3 A/N Space R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 
  

---

## Page 9

Activity Reporting Record Layouts 
Activity Detail (F55) 9 
Activity Detail (F55) #2 
Optional Conditional Record 
Input from Fund  
Output from [[NSCC]] to Firm  
This record is required for all transaction types with the exception of types 11 and 50.  
Activity Reporting Records Activity Detail (F55) #2 
#2 of 6 
Field Name   
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 N 55 = Activity Detail R 
Sequence Number 4 5 2 A/N 02 R 
Clearing/Settling Firm 
Number 
6 9 4 N  R 
Clearing/Settling Fund 
Number 
10 13 4 N  R 
Security Issue Number 14 22 9 A/N  R 
Original Trade Date/ 
Payable Date for [[Dividend]] 
Adj 
23 30 8 N mmddccyy R 
Price 31 42 12 N 999999.999999 R 
Currency Indicator 43 45 3 A/N USD or spaces R 
IRA Year of Contribution 
Code 
46 46 1 A/N 1 = Current Year  
2 = Prior Year  
3 = N/A 
R 
Cross Security Issue 
Number 
47 55 9 A/N Required for Transaction Types  
10 = Exchange Ex-Fund/SERV 
12 = Reinvest from other Fund 
22 = Share Class Exchange  
23 = Fund Merger Activity 
35  = Direct Voluntary Cross Class Exchange 
 
Also Required for Transaction Description 
Codes starting with ‘J’ and ‘W’ 
OC 
Description 56 84 29 A/N Required for Transaction Type 21 (including 
Transaction Description Code starting with ‘U’)  
OC 

---

## Page 10

Activity Reporting Record Layouts 
Activity Detail (F55) 10 
#2 of 6 
Field Name   
Start End Len Type Description  Opt/ 
Req 
[[Dividend]] Rate 85 89 5 N 99.999  
Required for Transaction Type 07 and 08  
OC 
Agent for Firm Number 90 93 4 A/N  O 
529 Transfer Reason 
Code 
94 94 1 A/N 1 = Owner – Resignation 
2 = Owner – Death 
3 = Owner – Divorce 
4 = Beneficiary Change - In Family 
5 = Beneficiary Change - Out of Family 
6 = In Kind 
7 = UGMA/UTMA (Age of Majority) 
O 
IRS 529 Annual Strategy 
Change Counter 
95 95 1 A/N 0 thru 9 O 
Filler 96 98 3 A/N Space R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 
 
 
  

---

## Page 11

Activity Reporting Record Layouts 
Activity Detail (F55) 11 
Activity Detail (F55) #3 – Supplemental Record 
Optional Conditional Record 
Input from Fund  
Output from [[NSCC]] to Firm  
This record is used to report financial trade information from direct fund activity where reporting responsibility is 
with the firm.  
The record is required for: 
• Transaction Type = 01 (including Transaction Description Codes starting with ‘A’), 03, 09, 10 (including 
Transaction Description Codes starting with ‘J’), and 24, if Load Type Indicator = 1; 
• Transaction Type = 02 (including Transaction Description Codes starting with ‘B’), 07, 08, 14, 17, 29, 30, 
31, and 32.    
• Membership Identifier = 02 (TPA/Investment Agent).   
Activity Reporting Records Activity Detail (F55) #3 
#3 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 N 55 = Activity Detail R 
Sequence Number 4 5 2 A/N 03  R 
Clearing/Settling Firm 
Number 
6 9 4 N  R 
Clearing/Settling Fund 
Number 
10 13 4 N  R 
Security Issue Number 14 22 9 A/N  R 
Withholding Indicator 23 23 1 A/N 1 = NRA  
2 = TEFRA Backup  
3 = TEFRA Pension 
O 
Withholding Amount 24 39 16 N 99,999,999,999,999.99 O 
Exchange Fee 40 43 4 N 99.99 O 
Sales Charge Rate 44 47 4 N 9.999  
If Load Type Indicator = 1, must be provided (but 
allowed to be zero) for the Transaction Type 01 
(including Transaction Description Code starting 
with ‘A’), 03, 09, 10 (including Transaction 
Description Code starting with ‘J’), and 24. 
OC 
Commission/CDSC 
Amount 
48 63 16 N 99,999,999,999,999.99 O 

---

## Page 12

Activity Reporting Record Layouts 
Activity Detail (F55) 12 
#3 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Cash Disbursement 
Indicator 
64 64 1 A/N Required for Transaction Type 02 (including 
Transaction Description Code starting with ‘B’), 
07, 08, 14, 17, 29, 30, and 31. 
• 0 = Cash To Firm ([[settlement]] through [[NSCC]] 
Generates Record (N75) for Transaction 
Types 02 (including Transaction Description 
Code starting with ‘B’), 14, 29, 30 and 31 
only)  
• 1 = Firm  
• 2 = Customer  
• 3 = Payee (for Dividends)  
• 4 = Cross Fund Reinvestment  
• 5 = 1099 Update Only  
• 6 = Cash to Trust ([[settlement]] through [[NSCC]] 
Generates Record (N75) for Transaction 
Types 02 (including Transaction Description 
Code starting with ‘B’), 14, 29, 30 and 31 
only)  
OC 
Buy/Sell Indicator 65 65 1 A/N 1 = Buy  
2 = Sell  
3 or Spaces = N/A 
O 
TPA/Investment Agent 
Number 
66 69 4 A/N Required for Membership Identifier 02 
(TPA/Investment Agent) 
OC 
Accrual Indicator  70 70 1 A/N Required for Transaction Type 32 (Accrual 
Adjustment). 
1 = Credit  
2 = Debit  
3 = Accrual Money Balance (Bucket Balance) 
OC 
Transfer Disbursement 
[[Option]] – Accruals 
71 71 1 A/N 2 = Cash to Customer – Delivering Firm  
4 = Reinvest – Receiving Firm (bucket to bucket) 
O 
Accrual Money Amount / 
Accrual Money Account 
Balance 
72 87 16 N Required for Transaction Type 32 (Accrual 
Adjustment).              
99,999,999,999,999.99  
 
This field should be:  
If Transaction type = 13 or 32, Accrual Money 
Amount;  
If Transaction type = 50, Accrual Money Account 
Balance 
OC 
Filler 88 98 11 A/N Space O 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 13

Activity Reporting Record Layouts 
Activity Detail (F55) 13 
Activity Detail (F55) #4 
Optional Conditional Record 
Input from Fund  
Output from [[NSCC]] to Firm  
This record is used to report financial trade information from direct fund activity where reporting responsibility is 
with the firm. 
This record is required: 
• If Share/Balance Amount is NOT provided in record F55 sequence #1.  
• If Transaction Type in the record F55 sequence #1 equals: 
o 13 (Direct Transfer) or 
o 33 (Transfer From – Cancellation) or 
o 34 (Transfer To – Cancellation).  
 
Otherwise, it is optional.   
Activity Reporting Records Activity Detail (F55) #4 
#4 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 N 55 = Activity Detail R 
Sequence Number 4 5 2 A/N 04  R 
Clearing/Settling Firm 
Number 
6 9 4 N  R 
Clearing/Settling Fund 
Number 
10 13 4 N  R 
Security Issue Number 14 22 9 A/N  R 
Original Control Number 23 37 15 A/N Required if Transaction Type 13 (“Direct 
Transfer”) in record F55 sequence #1. 
OC 
Control Number Correction 
Indicator 
38 38 1 A/N Space or ‘C’ through ‘Z’ O 
Opposing Fund Account 
Number 
39 58 20 A/N Required if Transaction Type = 
13 (Direct Transfer) 
33 (Transfer From – Cancellation)  
34 (Transfer To – Cancellation) 
 
Value is generated by the Fund 
OC 

---

## Page 14

Activity Reporting Record Layouts 
Activity Detail (F55) 14 
#4 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Share/Balance Amount – 
Extended 
59 74 16 N 999,999,999,999.9999 
 
Required if Share/Balance Amount is NOT 
provided in record F55 sequence #1. 
Otherwise, it is not allowed. 
OC 
Original Control Number 
Indicator 
75 75 1 A/N Required if Original Control Number field in 
record F55 sequence #4 is populated. 
 
1 = Fund/SERV Control Number 
2 = Networking Control Number 
3 = Manual Reference Number 
OC 
Underlying Customer 
Account Number 
76 95 20 A/N Underlying Customer Account Number at the 
Firm receiving the F55 record 
O 
Filler 96 98 3 A/N Space R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 
 
 
  

---

## Page 15

Activity Reporting Record Layouts 
Activity Detail (F55) 15 
Activity Detail (F55) #5  
Optional Conditional Record 
Input from Fund  
Output from [[NSCC]] to Firm  
This record is required if the Transaction Type in the record F55 sequence #1 equals:  
• 13 (Direct Transfer);  
• 33 (Transfer From – Cancellation);  
• 34 (Transfer To – Cancellation).  
 
Otherwise, it is optional.   
Activity Reporting Records Activity Detail (F55) #5 
#5 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 N 55 = Activity Detail R 
Sequence Number 4 5 2 A/N 05  R 
Clearing/Settling Firm 
Number 
6 9 4 N  R 
Clearing/Settling Fund 
Number 
10 13 4 N  R 
Security Issue Number 14 22 9 A/N  R 
Opposing Clearing/Settling 
Firm Number 
23 26 4 N [[NSCC]] [[participant]] number of the Firm or Fund 
(in the case of a direct Level 0 Account). 
 
Required if Transaction Type = 
13 (Direct Transfer) 
33 (Transfer From – Cancellation) 
34 (Transfer To – Cancellation) 
OC 
Opposing Network Control 
Indicator 
27 27 1 A/N 0 = Matrix Level 0  
3 = Matrix Level 3 
4 = Matrix Level 4 
 
Required if Transaction Type = 
13 (Direct Transfer),  
33 (Transfer From – Cancellation), 
34 (Transfer To – Cancellation). 
OC 

---

## Page 16

Activity Reporting Record Layouts 
Activity Detail (F55) 16 
#5 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Opposing Underlying 
Customer Account Number 
28 47 20 A/N  O 
Omnibus Account Indicator 48 48 1 A/N Omnibus Account Indicator Flag  
0 or blank = N; 
1 = Y 
O 
Cost Basis Money Amount 49 64 16 N 99,999,999,999,999.99 
 
This field should be populated for 529 accounts, 
when applicable. 
O 
Earnings to Date  Money 
Amount 
65 80 16 N 99,999,999,999,999.99 
 
This field should be populated for 529 accounts, 
when applicable. 
O 
Negative Earnings to Date 
Indicator 
81 81 1 A/N N = Negative 
Space = Positive 
 
This field should be populated for 529 accounts, 
when applicable. 
O 
Opposing 
Originating/Underlying Firm 
Number 
82 85 4 A/N Opposing Originating [[Broker]] Firm number 
 
(The underlying firm’s [[NSCC]] [[ID]] number, for 
firms transacting through an MF Agent) 
O 
Originating/Underlying Firm 
Number 
86 89 4 A/N Originating [[Broker]] Firm number 
 
(The underlying firm’s [[NSCC]] [[ID]] number, for 
firms transacting through an MF Agent) 
O 
Filler 90 98 9 A/N Space R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 
 
 
  

---

## Page 17

Activity Reporting Record Layouts 
Activity Detail (F55) 17 
Activity Detail (F55) #6  
Optional Conditional Record  
Input from Fund  
Output from [[NSCC]] to Firm  
This record is required if “Transaction Type” on record F55 sequence #1 equals:  
• BN - Money Market [[Liquidity]] Fee or  
• BO - Money Market [[Liquidity]] Fee with CDSC. 
 
Otherwise, it is optional.   
Activity Reporting Records Activity Detail (F55) #6 
#6 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 N 55 = Activity Detail R 
Sequence Number 4 5 2 A/N 06  R 
Clearing/Settling Firm 
Number 
6 9 4 N  R 
Clearing/Settling Fund 
Number 
10 13 4 N  R 
Security Issue Number 14 22 9 A/N  R 
FATCA Withholding 
Indicator 
 
23 23 1 A/N 0 = No  
1 = Yes 
O 
FATCA Withholding Rate 24 25 2 N .99 
Required for FATCA Withholding Indicator 1 
(Yes). Zeroes allowed. 
OC 
FATCA Withholding 
Amount 
26 41 16 N 99,999,999,999,999.99 
Required for FATCA Withholding Indicator 1 
(Yes). Zeroes allowed. 
OC 

---

## Page 18

Activity Reporting Record Layouts 
Activity Detail (F55) 18 
#6 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Redemption Fee Rate 42 48 7 N 99.99999 
Required when “Transaction Type” field is 
populated with one of the following “Transaction 
Description Codes”:  
• ‘BN’=Money Market [[Liquidity]] Fee or 
• ‘BO’=Money Market [[Liquidity]] Fee with 
CDSC 
 
Zero value is not allowed when this field is 
required. 
 
This field can be utilized to pass the 
Redemption Fee Rate for the following fee 
types: 
• Money Market [[Liquidity]] Fee 
• Short Term Redemption (STR) Fee 
 
This field can be utilized to communicate a 
Short Term Redemption (STR) Fee Rate if 
“Transaction Type” field is populated with one of 
the following “Transaction Description Codes”: 
• ‘BH’=Short Term Redemption Fee or 
• ‘BI’=Short Term Redemption Fee with 
CDSC 
OC 
Redemption Fee Money 
Amount 
49 64 16 N 99,999,999,999,999.99 
Required when “Transaction Type” field is 
populated with one of the following “Transaction 
Description Codes”:  
• ‘BN’=Money Market [[Liquidity]] Fee or 
• ‘BO’=Money Market [[Liquidity]] Fee with 
CDSC 
Zero value is not allowed when this field is 
required. 
 
This field can be utilized to pass the 
Redemption Fee Money Amount for the 
following fee types: 
• Money Market [[Liquidity]] Fee 
• Short Term Redemption (STR) Fee 
 
This field can be utilized to communicate a 
Short Term Redemption (STR) Fee Money 
Amount if “Transaction Type” field is populated 
with one of the following “Transaction 
Description Codes”: 
• ‘BH’=Short Term Redemption Fee or 
• ‘BI’=Short Term Redemption Fee with 
CDSC 
OC 
Account Representative [[ID]] 65 73 9 A/N Account Representative [[ID]] O 

---

## Page 19

Activity Reporting Record Layouts 
Activity Detail (F55) 19 
#6 of 6 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Branch Identification 
Number 
74 82 9 A/N Branch [[ID]] Number O 
Account Open Date 83 90 8 A/N mmddccyy 
Must be a valid calendar date 
 
Best Practice: 
Date of account establishment for the particular 
Security Issue [[ID]].  This is NOT the date of 
account funding. 
O 
Filler 91 98 8 A/N Space R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 20

Activity Reporting Record Layouts 
Activity/Balance Input /Output Trailer (F56) 20 
ACTIVITY/BALANCE INPUT /OUTPUT TRAILER (F56) 
Activity/Balance Input /Output Trailer (F56) #1 
Input from Fund – Optional Record 
Output from [[NSCC]] to Firm – Required Record 
Activity Reporting Records Activity/Balance input/output Trailer (F56) #1 
#1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 N 56 = Activity Detail R 
Sequence Number 4 5 2 A/N 01 - Trailer Record R 
Fund Clearing Number /  
Recipient Number 
6 9 4 N Fund Clearing Number - on Input from 
Fund to [[NSCC]]; 
Recipient Number - on Output from 
[[NSCC]] to [[participant]] 
R 
Processing Date 10 17 8 N mmddccyy R 
Total Number of Direct Purchase 
Transactions 
18 22 5 N Total for Transaction Type 01 
(including Transaction Description 
Codes starting with ‘A’) 
O 
Total Number of Direct Redemption 
Transactions 
23 27 5 N Total for Transaction Type 02 
(including Transaction Description 
Codes starting with ‘B’),  29,  30, and 
31 
O 
Total Number of PAC Transactions 28 32 5 N Total for Transaction Type 03  O 
Total Number of Check Redemption 
Transactions 
33 37 5 N Total for Transaction Type 04 O 
Total Number of LOI Adjustment 
Transactions 
38 42 5 N Total for Transaction Type 05 O 
Total Number of ROA Adjustment 
Transactions 
43 47 5 N Total for Transaction Type 06 O 
Total Number of [[Dividend]] Adjustment 
Transactions 
48 52 5 N Total for Transaction Type 07 O 
Total Number of Long Term Cap 
Gain Adjustment Transactions 
53 57 5 N Total for Transaction Type 08, 26, 27, 
and 28 
O 
Total Number of Fund Price 
Adjustment Transactions 
58 62 5 N Total for Transaction Type 09 O 

---

## Page 21

Activity Reporting Record Layouts 
Activity/Balance Input /Output Trailer (F56) 21 
#1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Total Number of Exchange 
Transactions 
63 67 5 N Total for Transaction Type 10 
(including Transaction Description 
Codes starting with ‘J’) 
O 
Total Number of [[Fiduciary]] Fee 
Transactions 
68 72 5 N Total for Transaction Type 11 
(including Transaction Description 
Codes starting with ‘K’) 
O 
Total Number of Cross Reinvest 
Transactions 
73 77 5 N Total for Transaction Type 12 O 
Total Number of Direct Transfer 
Transactions 
78 82 5 N Total for Transaction Type 13 O 
Total Number of Accrual Adjustment 
Transactions 
83 87 5 N Total for Transaction Type 32 O 
Total Number of Transfer From - 
Cancellation Transactions 
88 92 5 N Total for Transaction Type 33 O 
Total Number of Transfer To - 
Cancellation Transactions 
93 97 5 N Total for Transaction Type 34 O 
Filler 98 100 3 A/N Space R 
 
 
  

---

## Page 22

Activity Reporting Record Layouts 
Activity/Balance Input /Output Trailer (F56) 22 
Activity/Balance Input/Output Trailer (F56) #2 
Input from Fund – Optional Record 
Output from [[NSCC]] to Firm – Required Record 
Activity Reporting Records Activity/Balance Input/Output Trailer (F56) #2 
#2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 N 56 = Activity Detail R 
Sequence Number 4 5 2 A/N 02 - Trailer Record R 
Fund Clearing Number /  
Recipient Number 
6 9 4 N Fund Clearing Number - on Input from 
Fund to [[NSCC]]; 
Recipient Number - on Output from [[NSCC]] 
to [[participant]]. 
R 
Processing Date 10 17 8 N mmddccyy R 
Total Number of Share 
Adjustment Transactions 
18 22 5 N Total for Transaction Type 21 (including 
Transaction Description Codes starting 
with ‘U’) 
O 
Total Number of Other 
Transactions 
23 27 5 N Total for Transaction Type 23 (including 
Transaction Description Codes starting 
with ‘W’), 24, and 25.  
O 
Total Number of Closing 
Balance Transactions 
28 32 5 N Total for Transaction Type 50 O 
Total Number of SWP 
Transactions 
33 37 5 N Total for Transaction Type 14  O 
Total Number of Exchange 
Fee Transactions 
38 42 5 N Total for Transaction Type 15 (including 
Transaction Description Codes starting 
with ‘O’) 
O 
Total Number of Certificate 
Deposits 
43 47 5 N Total for Transaction Type 16 (including 
Transaction Description Codes starting 
with ‘P’) 
O 
Total Number of Short Term 
Cap Gain Adjustments 
48 52 5 N Total for Transaction Type 17 O 
Total Number of Year-End 
Reporting Transactions 
53 57 5 N Total for Record Type 45 sequence 01 O 
Total Number of [[Dividend]] 
Related Transactions 
58 62 5 N Total for Transaction Type 18 (including 
Transaction Description Codes starting 
with ‘R’) 
O 

---

## Page 23

Activity Reporting Record Layouts 
Activity/Balance Input /Output Trailer (F56) 23 
#2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Total Number of Share Class 
Exchanges 
63 67 5 N Total for Transaction Type 22 (including 
Transaction Description Codes starting 
with ‘V’) 
O 
Filler 68 69 2 A/N Space R 
Total Number of Records 70 77 8 N 99,999,999  
(Including Headers and Trailers) 
O 
Total Number of Voluntary 
Cross Class Exchanges 
78 82 5 N Total for Transaction Type 35 O 
Filler 83 100 18 A/N Space R 

---

## Page 24

Activity Reporting Record Layouts 
Year-End Tax Reporting (F45) 24 
YEAR-END TAX REPORTING (F45) 
Year-End Tax Reporting (F45) #1 - Year-To-Date  
Input from Fund to [[NSCC]] 
Output from [[NSCC]] to Firm  
Year-End Tax Reporting includes the sequence numbers 01 and 02. Sequence 01 is for generic year -to-date 
information. Sequence 02 is for detail on reallocations done throughout the year. The generic year -to-date 
information may be submitted independently, but the detail on reallocations cannot.  
If more than one reallocation has been declared for a particular Security Issue, each detail record, 02, must be 
accompanied by a generic first record, 01.  
Activity Reporting Records Year-End Tax Reporting (F45) #1 - Year-To-Date 
#1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 45 = Year-End Reporting R 
Sequence Number 4 5 2 A/N 01 R 
Clearing/Settling Firm # 6 9 4 N  R 
Clearing/Settling Fund # 10 13 4 N  R 
Security Issue Number 14 22 9 A/N  R 
Fund’s Tax Identification # 23 31 9 A/N  R 
Fee Type (A) 32 32 1 A/N 0 = Not Applicable  
1 = Fund Expense (Credit)  
2 = Fund Expense (Debit) 
R 
Fee Type (B) 33 33 1 A/N 0 = Not Applicable  
1 = Investment Expenses (Credit)  
2 = Investment Expenses (Debit) 
R 
Fee Type (C) 34 34 1 A/N 0 = Not Applicable  
1 = Other (Credit)  
2 = Other (Debit) 
R 
Fee Amount as a 
Percentage of Year to Date 
Distributions (Type A) 
35 40 6 N 999.999  
Required when Fee Type (A) = 1 or 2  
Not Allowed [Must be Zero or Space] when 
Fee Type (A) = 0 
OC 

---

## Page 25

Activity Reporting Record Layouts 
Year-End Tax Reporting (F45) 25 
#1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Fee Amount as a 
Percentage of Year to Date 
Distributions (Type B) 
41 46 6 N 999.999  
Required when Fee Type (B) = 1 or 2  
Not Allowed [Must be Zero or Space] when 
Fee Type (B) = 0 
OC 
Fee Amount as a 
Percentage of Year to Date 
Distributions (Type C) 
47 52 6 N 999.999  
Required when Fee Type (C) = 1 or 2  
Not Allowed [Must be Zero or Space] when 
Fee Type (C) = 0 
OC 
Foreign Tax Credit 53 58 6 N 999.999  
As a Percentage of Year To Date Distributions 
O 
Spill-Over Distribution Rate - 
(Current Year) 
59 64 6 N 999.999 O 
Spill-Over Distribution Rate - 
(Last Year) 
65 70 6 N 999.999 O 
TPA/Investment Agent 
Number 
71 74 4 A/N  O 
Filler 75 98 24 A/N Space R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 
 
 
  

---

## Page 26

Activity Reporting Record Layouts 
Year-End Tax Reporting (F45) 26 
Year-End Tax Reporting (F45) #2 - Individual Reallocation Record  
Input from Fund to [[NSCC]] 
Output from [[NSCC]] to Firm  
Activity Reporting Records Year-End Tax Reporting (F45) #2 - Individual Reallocation Record 
#2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 45 = Year-End Reporting R 
Sequence Number 4 5 2 A/N 02 R 
Clearing/Settling Firm # 6 9 4 N  R 
Clearing/Settling Fund # 10 13 4 N  R 
Security Issue Number 14 22 9 A/N  R 
Reallocation “From” 23 23 1 A/N 1 = Non-Taxable Distributions  
2 = Short Term Capital Gains  
3 = Long Term Capital Gains  
4 = Dividends  
5 = Return of Capital (Capital Surplus)  
6 = Taxable Distributions 
R 
Reallocation “To” 24 24 1 A/N 1 = Non-Taxable Distributions  
2 = Short Term Capital Gains  
3 = Long Term Capital Gains  
4 = Dividends  
5 = Return of Capital (Capital Surplus)  
6 = Taxable Distributions 
R 
Reallocation Amount as a 
Percentage of the Distribution 
25 30 6 N 999.999 R 
Record Date 31 38 8 N mmddccyy R 
Payable Date 39 46 8 N mmddccyy R 
Foreign Tax Credit as a 
Percentage of the Distribution 
47 52 6 N 999.999 O 
Fee Type (A) 53 53 1 A/N 0 = Not Applicable  
1 = Fund Expense (Credit)  
2 = Fund Expense (Debit) 
R 

---

## Page 27

Activity Reporting Record Layouts 
Year-End Tax Reporting (F45) 27 
#2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Fee Type (B) 54 54 1 A/N 0 = Not Applicable  
1 = Investment expenses (Credit)  
2 = Investment expenses (Debit) 
R 
Fee Type (C) 55 55 1 A/N 0 = Not Applicable  
1 = Other (Credit)  
2 = Other (Debit) 
R 
Fee Amount as a Percentage 
of Year to Date Distributions 
(Type A) 
56 61 6 N 999.999  
Required when Fee Type (A) = 1 or 2  
Not Allowed [Must be Zero or Space] when 
Fee Type (A) = 0 
OC 
Fee Amount as a Percentage 
of Year to Date Distributions 
(Type B) 
62 67 6 N 999.999  
Required when Fee Type (B) = 1 or 2  
Not Allowed [Must be Zero or Space] when 
Fee Type (B) = 0 
OC 
Fee Amount as a Percentage 
of Year to Date Distributions 
(Type C) 
68 73 6 N 999.999  
Required when Fee Type (C) = 1 or 2  
Not Allowed [Must be Zero or Space] when 
Fee Type (C) = 0 
OC 
Spill-Over Distribution Indicator 74 74 1 N 0 = No  
1 = Yes 
R 
Filler 75 80 6 A/N Space R 
Filler 81 98 18 A/N Space R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 28

Activity Reporting Record Layouts 
Input Records’ Layout 28 
INPUT RECORDS’ LAYOUT 
Activity File Datatrak Header  
Input from Fund to [[NSCC]]  
Activity File Datatrak Header 
Field Name  Start End Len Type Description  Opt/ 
Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value ‘26597’ R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value 'NETWORKING FUND ACT. INP’ R 
Multi Batch Indicator 60 60 1 A/N N = Not last batch  
Y = Last batch 
R 
Multi Batch Number 61 63 3 N  R 
Filler 64 100 37 A/N Space R 
 
 
  

---

## Page 29

Activity Reporting Record Layouts 
Input Records’ Layout 29 
Activity File Datatrak Trailer  
Input from Fund to [[NSCC]]  
Activity File Datatrak Trailer 
Field Name  Start End Len Type Description  Opt/ 
Req 
Literal 1 5 5 A/N Value 'END.S' R 
DATATRAK SYSID 6 10 5 A/N Value '26597' R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Data File Record Count 27 33 7 N DATATRAK Header & Trailer not included in 
count 
R 
Filler 34 100 67 A/N Space R 

---

## Page 30

Activity Reporting Record Layouts 
Output Records’ Layout 30 
OUTPUT RECORDS’ LAYOUT 
Activity [[settlement]] Summary Output Detail (N75)  
Output from [[NSCC]] to Funds and Firms  
Activity [[settlement]] Summary Output Detail (N75) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 75 = Detail 
Sequence Number 4 4 1 A/N 1 
MRO Recipient Number 5 8 4 N  
Security Issue Number 9 17 9 A/N  
Pay - Receive Code 18 18 1 N 2 = Your Debit  
4 = Your Credit 
Contra Clearing [[Member]] 19 22 4 N  
[[settlement]] Date 23 30 8 N mmddccyy 
Filler 31 40 10 A/N Space 
[[settlement]] Value 41 56 16 N 99,999,999,999,999.99 
[[settlement]] Type 57 59 3 A/N ‘DRD’ = Direct Redemption  
‘SWP’ = Systematic Withdrawal 
[[settlement]] Indicator 60 60 1 A/N ‘A’ = Activity [[settlement]]  
‘T’ = TEFRA Withholding 
Trade Date 61 68 8 N mmddccyy 
Firm/Fund Identification Number  69 88 20 A/N  
Detail [[Margin]] Account Indicator 89 89 1 A/N 0 = NO  
1 = YES 
Currency Indicator 90 92 3 A/N For future use 
Firm/Fund Identification Indicator  93 93 1 A/N 1 = Fund (FIN)  
2 = Firm (BIN) 
TPA/Investment Agent or Firm 
Number 
94 97 4 A/N Firm Number when MRO Recipient  
Type = ‘A’ or ‘T’. 
Otherwise, TPA/Investment Agent Number, 
or space 

---

## Page 31

Activity Reporting Record Layouts 
Output Records’ Layout 31 
Field Name  Start End Len Type Description  
Filler 98 131 34 A/N Space 
MRO Recipient Type 132 132 1 A/N ‘A’ = Investment Agent 
‘B’ = Firm 
‘F’ = Fund 
‘T’ = TPA 
 
 
  

---

## Page 32

Activity Reporting Record Layouts 
Output Records’ Layout 32 
Activity [[settlement]] Summary Output Trailer (N76)  
Output from [[NSCC]] to Funds and Firms  
Activity [[settlement]] Summary Output Trailer (N76) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 76 = Trailer Totals 
Sequence Number 4 4 1 A/N 1 
MRO Recipient 5 8 4 N  
Literal 9 19 11 A/N 99999999999 
Literal 20 27 8 A/N ACTIVTRL 
[[settlement]] Date 28 35 8 N mmddccyy 
Number of Debit Items 36 41 6 N 999,999 
Total Debit Amount 42 57 16 N 99,999,999,999,999.99 
Number of Credit Items 58 63 6 N 999,999 
Total Credit Amount 64 79 16 N 99,999,999,999,999.99 
Currency Indicator 80 82 3 A/N For future use 
Filler 83 131 49 A/N Space 
MRO Recipient Type 132 132 1 A/N ‘A’ = Investment Agent 
‘B’ = Firm 
‘F’ = Fund 
‘T’ = TPA 
 
 
  

---

## Page 33

Activity Reporting Record Layouts 
Output Records’ Layout 33 
Input Acknowledgment - Activity (NAC) 
Output from [[NSCC]] to Fund  
Input Acknowledgment - Activity (NAC) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N AC = Activity 
Filler 4 4 1 A/N Space 
Clearing/Settling Fund # 5 8 4 N  
Processing Date 9 16 8 N mmddccyy 
Total Records Received 17 24 8 N 99,999,999  
(Includes any Headers and Trailers) 
Filler 25 100 76 A/N Space 
 
 
  

---

## Page 34

Activity Reporting Record Layouts 
Output Records’ Layout 34 
Output Header Activity File (N00)  
Output Header Activity File (N00) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 4 1 A/N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '11111111111' 
Transmission Date 20 27 8 N mmddccyy 
Autoroute File [[ID]] 28 35 8 A/N Value '02102029' 
Literal 36 43 8 A/N Value 'ACTIVITY' 
Filler 44 100 57 A/N Space 
 
 
  

---

## Page 35

Activity Reporting Record Layouts 
Output Records’ Layout 35 
Output Header - Activity [[settlement]] Summary (N00)  
Output Header - Activity [[settlement]] Summary (N00) 
Field Name  Start End Len Type Description  
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 4 1 A/N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '11111111111' 
Transmission Date 20 27 8 N mmddccyy 
Autoroute File [[ID]] 28 35 8 A/N Value '02102429' 
Literal 36 52 17 A/N Value 'ACTIVITYSETTLEMNT' 
Filler 53 132 80 A/N Space 
 
 

---

## Page 36

Activity Reporting Record Layouts 
APPENDIX – Summary of Changes 36 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  

---

## Page 37

Activity Reporting Record Layouts 
Summary of Changes – effective Q1, 2019 37 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 38

Activity Reporting Record Layouts 
Summary of changes – effective Q4, 2017 38 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2017  
Rename of Existing Fields 
New Field Name Record Type and Location Old Name 
Filler F45, seq#2, start 75, end 80, length 6, A/N, R 5 Year Capital Gain Rate 

---

## Page 39

Activity Reporting Record Layouts 
Summary of changes – effective Q1, 2017 39 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2017  
Added New Fields 
Field Name Location  Requirements 
Account Representative 
[[ID]]  
F55 seq.#6, start  65, end 73 , length 9, A/N, 
Optional 
Account Representative [[ID]] 
Branch Identification 
Number 
F55 seq.#6, start  74, end 82 , length 9, A/N, 
Optional 
Branch [[ID]] Number 
Account Open Date F55 seq.#6, start  83, end 90 , length 8, A/N, 
Optional 
mmddccyy 
Must be a valid calendar date.  
Best Practice: 
Date of account establishment for the 
particular Security Issue [[ID]].  This is 
NOT the date of account funding. 
 
Added New “Transaction Description Codes” for Existing Field 
Field Name Location  Transaction Type value Add Transaction Description Code 
Transaction Type  F55 seq.#1, start  23, end 24, 
length 2, Required 
01  - Direct Purchase AZ =  Initial Purchase 
A@ =  Subsequent Purchase 
 
Reject Codes 
The following new reject code has been added: 
Reject Code Description 
Q8 Account Open Date is invalid 

---

## Page 40

Activity Reporting Record Layouts 
Summary of changes – effective Q3, 2016 40 
SUMMARY OF CHANGES – EFFECTIVE Q3, 2016  
Added New “Transaction Description Codes” for Existing Field 
Field Name Location  Transaction Type value Add Transaction Description Code 
Transaction 
Type  
F55 seq.#1, start  23, 
end 24, length 2, 
Required 
02  - Direct Redemption BN =  Money Market [[Liquidity]] Fee 
BO =  Money Market [[Liquidity]] Fee with CDSC 
 
Added New Fields 
New Field 
Name 
Record Type and Location Requirements 
Redemption 
Fee  Rate 
F55 seq#6, start 42, end 48, length 7, N, OC 99.99999 
 
Required when “Transaction Type” field is 
populated with one of the following “Transaction 
Description Codes”:  
• ‘BN’=Money Market [[Liquidity]] Fee  or 
• ‘BO’=Money Market [[Liquidity]] Fee with CDSC 
 
Zero value is not allowed when this field is required. 
 
This field can be utilized to pass the Redemption 
Fee Rate for the following fee types: 
• Money Market [[Liquidity]] Fee 
• Short Term Redemption (STR) Fee 
 
This field can be utilized to communicate a Short 
Term Redemption (STR) Fee Rate if  “Transaction 
Type” field is populated with one of the following 
“Transaction Description Codes”: 
• ‘BH’=Short Term Redemption Fee or 
• ‘BI’=Short Term Redemption Fee with CDSC 

---

## Page 41

Activity Reporting Record Layouts 
Summary of changes – effective Q3, 2016 41 
New Field 
Name 
Record Type and Location Requirements 
Redemption 
Fee Money 
Amount 
F55 seq#6, start 49, end 64, length 16, N, OC 99,999,999,999,999.99 
 
Required when “Transaction Type” field is 
populated with one of the following “Transaction 
Description Codes”:  
• ‘BN’=Money Market [[Liquidity]] Fee  or 
• ‘BO’=Money Market [[Liquidity]] Fee with CDSC 
 
Zero value is not allowed when this field is required. 
 
This field can be utilized to pass the Redemption 
Fee Money Amount for the following fee types: 
• Money Market [[Liquidity]] Fee 
• Short Term Redemption (STR) Fee 
 
This field can be utilized to communicate a Short 
Term Redemption (STR) Fee Money Amount if  
“Transaction Type” field is populated with one of 
the following “Transaction Description Codes”: 
• ‘BH’=Short Term Redemption Fee or 
• ‘BI’=Short Term Redemption Fee with CDSC 
 
Requirements Changed for Existing Records 
Record Record Name Changed Requirements  
F55 sequence # 6 Activity Reporting Records 
Activity Detail (F55) #6 
Optional/Conditional  
This record is required if  “Transaction Type” = ‘BN’ or ‘BO’ 
(record F55 sequence #1) 
 Otherwise, it is optional.   
 
Reject Codes 
The following new reject codes have been added: 
Reject Code Description 
Q6 Redemption Fee Rate missing/invalid 
Q7 Redemption Fee Money Amount missing/invalid     

---

## Page 42

Activity Reporting Record Layouts 
Summary of changes – effective Q4, 2013 42 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2013  
Requirements Changed for Existing Field 
Field Name Location  Old requirements New requirement 
Membership 
Identifier 
F55 seq.#1, start 92, end 93,     
length 2, OC 
Required for Transaction 
Types 
13 (Direct Transfer) 
 
00 = N/A  
01 = Trust  
02 = TPA/Investment Agent 
Required for Transaction Types 
 13 (Direct Transfer) 
33 (Transfer from – Cancellation) 
34 (Transfer to – Cancellation)  
00 = N/A  
01 = Trust  
02 = TPA/Investment Agent 
Filler/  
Reject Code 
F55 seq.#2, start 99, end100,    
length 2, R 
 (Documentation correction) 
Space Input: Space  
Output: Reject Code 
Filler/ 
Reject Code 
F55 seq.#3, start 99, end100,   
length 2, R 
(Documentation correction) 
Space Input: Space  
Output: Reject Code 
Filler/ 
Reject Code 
F55 seq.#4, start 99, end100,   
length 2, R 
(Documentation correction) 
Space Input: Space  
Output: Reject Code 
Filler/ 
Reject Code 
F55 seq.#5, start 99, end100,   
length 2, R 
(Documentation correction) 
Space Input: Space  
Output: Reject Code 
 
Added New Fields 
New Field Name Record Type and Location Requirements 
Opposing Membership 
Identifier 
F55 seq. #1, start 94, end 95, length 2, 
OC.  
Optional Conditional. Required if Transaction Type = 
13 (Direct Transfer);  
33 (Transfer From – Cancellation); 
34 (Transfer To – Cancellation). 
Opposing Membership Identifiers: 
00 = N/A 
01 = Trust 
Opposing 
Originating/Underlying 
Firm Number 
F55 seq. #5, start 82, end 85, length 4, 
O.  
Optional. 
Opposing Originating [[Broker]] Firm number 

---

## Page 43

Activity Reporting Record Layouts 
Summary of changes – effective Q4, 2013 43 
New Field Name Record Type and Location Requirements 
(The underlying firm’s [[NSCC]] [[ID]] number, for firms 
transacting through an MF Agent) 
Originating/Underlying 
Firm Number 
F55 seq. #5, start 86, end 89, length 
4,O  
Optional. 
Originating [[Broker]] Firm number 
(The underlying firm’s [[NSCC]] [[ID]] number, for firms 
transacting through an MF Agent) 
 
Requirements Changed for Existing Record 
Record Record Name Changed Requirements  
F55 sequence #5 Activity Reporting Records 
Activity Detail (F55) #5 
Optional Record 
Optional Conditional Record. (Documentation correction) 
This record is required If the Transaction Type in the record F55 
sequence #1 equals: 
• 13 (Direct Transfer); 
• 33 (Transfer From – Cancellation) ; 
• 34 (Transfer To – Cancellation). 
Otherwise, it is optional. 
 
FATCA: Added New Records 
Record Record Name Requirements 
F55 sequence #6 Activity Reporting Records Activity Detail (F55) #6 Optional Record 
 
FATCA: Added New Fields 
New Field Name Record Type and Location Requirements 
FATCA  Withholding 
Indicator 
F55 seq#6, start 23, end 23, length 1, A/N, 
Optional    
0 = No  
1 = Yes 
FATCA  Withholding  
Rate 
F55 seq#6, start 24, end 25, length 2, N , 
OC 
.99 
 
Required for FATCA Withholding Indicator 1 (Yes). 
Zeroes are allowed. 
FATCA  Withholding 
Amount 
F55 seq#6, start 26, end 41, length 16, N 
,OC 
99,999,999,999,999.99 
 
Required for FATCA Withholding Indicator 1 (Yes). 
Zeroes are allowed.     

---

## Page 44

Activity Reporting Record Layouts 
Summary of changes – effective Q1, 2013 44 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2013  
Added New Fields 
New Field Name Record Type and Location Requirements 
Total Number of Voluntary 
Cross Class Exchanges 
F56 seq.# 2, start 78, end 82, length 5, 
Optional 
Total for Transaction Type 35  
 
Added New Value for Existing Field 
Field Name Location  Add New value 
Transaction Type  F55 seq.#1, start  23, end 24, length 2, 
Required 
35 = Direct Voluntary Cross Class 
Exchange 
 
Requirements Changed for Existing Field 
Field Name Location  Old requirements New requirement 
Network Control 
Indicator 
F55 seq.#1, start 84, end 84, 
length 1, Required 
0 = Level 0  
1 = Level 1  
2 = Level 2  
3 = Level 3  
4 = Level 4 
0 = Matrix Level 0  
3 = Matrix Level 3  
4 = Matrix Level 4 
 
(Removed 1 = Level 1; 2 = Level 2 
effective Q1, 2013) 
Also updated description to “Matrix 
Level” 
Cross Security 
Issue Number 
F55 seq.#2, start  47, end 55, 
length 9, Optional Conditional 
Required for Transaction 
Types 10 (including 
Transaction Description 
Code starting with ‘J’), 12, 
and 23 (including 
Transaction Description 
code starting with ‘W’) 
Required for Transaction Types  
10 = Exchange Ex-Fund/SERV 
12 = Reinvest from other Fund 
22 = Share Class Exchange 
23 = Fund Merger Activity 
35  = Direct Voluntary Cross Class 
Exchange  
Also Required for Transaction 
Description Codes starting with ‘J’ and 
‘W’.  

---

## Page 45

Activity Reporting Record Layouts 
Summary of changes – effective Q1, 2013 45 
Field Name Location  Old requirements New requirement 
Opposing Fund 
Account Number 
F55 seq.#4, start 39, end 58, 
length 20, Optional Conditional  
Required for Transaction 
Type 13 (Direct Transfer). 
Value is generated by the 
Fund. 
Required if Transaction Type = 
13 (Direct Transfer) 
33 (Transfer From – Cancellation) 
34 (Transfer To – Cancellation) 
 
Value is generated by the Fund 
Opposing 
Clearing/Settling 
Firm Number 
F55 seq.#5, start 23, end 26, 
length 4, Optional Conditional 
[[NSCC]] [[participant]] number 
of the Firm or Fund (in the 
case of a direct Level 0 
Account). 
[[NSCC]] [[participant]] number of the Firm or 
Fund (in the case of a direct Level 0 
Account)  
 
Required if Transaction Type = 
13 (Direct Transfer) 
33 (Transfer From – Cancellation) 
34 (Transfer To – Cancellation) 
Opposing 
Network Control 
Indicator 
F55 seq.#5, start 27, end 27, 
length 1, Optional Conditional 
0 = Level 0  
1 = Level 1  
2 = Level 2  
3 = Level 3  
4 = Level 4 
0 = Matrix Level 0  
3 = Matrix Level 3 
4 = Matrix Level 4 
 
Required if Transaction Type = 
13 (Direct Transfer) 
33 (Transfer From – Cancellation) 
34 (Transfer To – Cancellation) 
 
Also Updated description to “Matrix 
Level” 
 
Requirements Changed for Existing Record 
Record Record Name Changed Requirements  
F55 sequence # 4 Activity Reporting Records 
Activity Detail (F55) #4 
This record is required:  
• If Share/Balance Amount is NOT provided in record F55 
sequence #1.  
• If Transaction Type = 13 (Direct Transfer) in record F55 
sequence #1. 
• If Transaction Type = 33 (Transfer From – Cancellation) in 
record F55 sequence #1.  
• If Transaction Type = 34 (Transfer To – Cancellation) in record 
F55 sequence #1. 

---

## Page 46

Activity Reporting Record Layouts 
Summary of changes – effective Q1, 2013 46 
Record Record Name Changed Requirements  
F55 sequence #5 Activity Reporting Records 
Activity Detail (F55) #5 
This record is required:  
• If Transaction Type =13 (Direct Transfer) in record F55 
sequence #1. 
• If Transaction Type = 33 (Transfer From – Cancellation) in 
record F55 sequence #1.  
• If Transaction Type = 34 (Transfer To – Cancellation) in record 
F55 sequence #1. 
Otherwise, it is optional. 

---

## Page 47

Activity Reporting Record Layouts 
Summary of changes – effective Q4 (December 5), 2011 47 
SUMMARY OF CHANGES – EFFECTIVE Q4 (DECEMBER 
5), 2011  
Added New Value for Existing Field 
Field Name Location  Add New value 
Transaction Type  F55 seq.#1, start  23, end 24, length 2, Required 33 = Transfer From - Cancellation 
34 = Transfer To - Cancellation 
 
Added New Fields 
New Field Name Record Type and Location Requirements 
Total Number of Transfer From 
- Cancellation Transactions 
F56 seq.# 1, start 88, end 92, length 5, Optional Total for Transaction Type 33  
Total Number of Transfer To - 
Cancellation Transactions 
F56 seq.# 1, start 93, end 97, length 5, Optional Total for Transaction Type 34  

---

## Page 48

Activity Reporting Record Layouts 
Summary of changes – effective Q4 (October 17), 2011 48 
SUMMARY OF CHANGES – EFFECTIVE Q4 (OCTOBER 
17), 2011  
Added New Record 
Record Record Name Requirements  
F55 sequence # 5 Activity Reporting Records - Activity 
Detail (F55) #5 
Optional. 
This record should be populated for Transaction Type 13 
(Direct Transfer). 
 
Added New Fields 
New Field Name Record Type and Location Requirements 
Social Code F55 seq. #1, start 90, end 91, length 2  Required 
Membership Identifier F55 seq.# 1, start 92, end 93, length 2,  
Optional/Conditional 
Required for Transaction Type 13 
(Direct Transfer). 
00 = N/A 
01 = Trust 
02 = TPA/Investment Agent 
Opposing Clearing/Settling 
Firm Number 
F55 seq.# 5, start 23, end 26, length 4, Optional [[NSCC]] [[participant]] number of the Firm or 
Fund (in the case of a direct Level 0 
Account). 
Opposing Network Control 
Indicator 
F55 seq.# 5, start 27, end 27, length 1, Optional 0 = Level 0  
1 = Level 1  
2 = Level 2  
3 = Level 3  
4 = Level 4  
Opposing Underlying 
Customer Account Number  
F55 seq.# 5, start 28, end 47, length 20, Optional  
Omnibus Account Indicator F55 seq.# 5, start 48, end 48, length 1, Optional Omnibus Account Indicator Flag  
0 or blank = N; 
1 = Y 
Cost Basis Money Amount  F55 seq.# 5, start 49, end 64, length 16, Optional 99,999,999,999,999.99 
Earnings to Date Money 
Amount  
F55 seq.# 5, start 65, end 80, length 16, Optional 99,999,999,999,999.99 
Negative Earnings to Date 
Indicator 
F55 seq.# 5, start 81, end 81, length 1, Optional N = Negative 
Space = Positive 

---

## Page 49

Activity Reporting Record Layouts 
Summary of changes – effective Q4 (October 17), 2011 49 
New Field Name Record Type and Location Requirements 
Total Number of Accrual 
Adjustment Transactions 
F56 seq.# 1, start 83, end 87, length 5, Optional Total for Transaction Type 32 (Accrual 
Adjustment). 
 
Added New Value for Existing Field 
Field Name Location  Add New value 
Transaction Type  F55 seq.#1, start  23, end 24, length 2, 
Required 
32 = Accrual Adjustment 
 
Requirements for Changed for Existing Fields 
Field Name Location  Old requirements New requirement 
Dollar Amount F55 seq.#1, start 68, end 83, 
length 16  
Required Required/Conditional 
Optional for Transaction Type 32 
(Accrual Adjustment). 
TPA/Investment 
Agent Number 
F55 seq.#3, start 66, end 69, 
length 4 
Optional Optional/Conditional 
Required for Membership Identifier = 02  
Transfer 
Disbursement 
Indicator – Accrual 
 
New name of the 
field: 
Accrual Indicator 
F55 seq.#3, start 70, end 70, 
length 1 
Optional Optional/Conditional 
Required for Transaction Type 32 
(Accrual Adjustment) 
Accrual Money 
Amount / Accrual 
Money Account 
Balance 
F55 seq.#3, start 72, end 87, 
length 16 
Optional 
99,999,999,999,999.99  
 
This field should be:  
If Transaction type = 13, 
Accrual Money Amount;  
If Transaction type = 50, 
Accrual Money Account 
Balance  
Optional/Conditional 
Required if Transaction Type 32 (Accrual 
Adjustment)  
 
If Transaction type = 13 or 32, Accrual 
Money Amount;  
If Transaction type = 50, Accrual Money 
Account Balance 
Opposing Account 
Number 
 
New name of the 
field: 
Opposing Fund 
Account Number 
F55 seq.#4, start 39, end 58, 
length 20 
Optional  Optional / Conditional 
Required for Transaction Type 13 (Direct 
Transfer). 
 
Value is generated by the Fund. 
 

---

## Page 50

Activity Reporting Record Layouts 
Summary of changes – effective Q4 (October 17), 2011 50 
Requirements Changed for Existing Record 
Record Record Name Changed Requirements  
F55 sequence # 3 Activity Reporting Records 
Activity Detail (F55) #3 
This record is required for: 
• Transaction Type = 01 (including Transaction Description Code 
starting with ‘A’), 03, 09, 10 (including Transaction Description 
Codes starting with ‘J’), and 24, if Load Type Indicator = 1; 
• Transaction Type = 02 (including Transaction Description Code 
starting with ‘B’), 07, 08, 14, 17, 29, 30, 31, and 32.  
• Membership Identifier = 02.  

---

## Page 51

Activity Reporting Record Layouts 
Summary of changes – effective Q2, 2011 51 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2011 
Add New Fields 
New Field Name Record Type and Location Requirements 
Original Control Number 
Indicator 
F55 seq.# 4, start 75, end 75, length 1,  
Optional/Conditional 
Required if Original Control Number field 
in record F55 sequence #4 is populated. 
 
1  =  Fund/SERV Control Number 
2  =  Networking Control Number 
3  =  Manual Reference Number 
Underlying Customer 
Account Number 
F55 seq.# 4, start 76 end 95, length 20,    
Optional 
Underlying Customer Account Number at 
the Firm receiving the F55 record 
 
Requirements Changed for Existing Field 
Field Name Location  Old 
requirements 
New requirement 
Original Control 
Number 
F55 seq.#4, start  23, end 37, length 15 Optional Optional/Conditional 
Required if Transaction Type = 13 in 
record F55 sequence #1.  
 
Requirements Changed for Existing Records 
Record Record Name Changed Requirements  
F55 sequence # 4 Activity Reporting Records Activity Detail (F55) #4 This record is required: 
• If Share/Balance Amount is NOT provided 
in record F55 sequence #1. 
• If Transaction Type is equal to 13 in record 
F55 sequence #1. (Effective Q2, 2011)  
 Otherwise, it is optional.   
 
 
 

---

## Page 52

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 9, 2023 
Publication Code: MFS327 
Service: Networking 
Title: Activity Reporting Record Layouts 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
  