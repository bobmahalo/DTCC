---
title: "Networking - Dividend Reporting Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_DividendReporting_mfs331_2023_10_09.pdf"
pages: 49
size: "591.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Networking - Dividend Reporting Record Layouts

**Original File:** [net_DividendReporting_mfs331_2023_10_09.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_DividendReporting_mfs331_2023_10_09.pdf)  
**Category:** Other  
**Total Pages:** 49  
**File Size:** 591.9 KB  

---

## Page 1

 
 
 
Networking 
[[Dividend]] REPORTING RECORD LAYOUTS 
OCTOBER 9, 2023 
 

---

## Page 2

[[Dividend]] Reporting Record Layouts 
 
History of Important Notices 2 
 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 4 
[[Dividend]] Header (F61, 62) ................................................................................................................................... 5 
[[Dividend]] Header (F61, 62) #1 ............................................................................................................................ 5 
[[Dividend]] Header (F61, 62) #2 ............................................................................................................................ 7 
[[Dividend]]/Capital Gain Detail for Cash Accounts not Subject to Withholding (F63) ..................................... 8 
Cash Accounts Not Subject to Withholding (F63) #1 ......................................................................................... 8 
Cash Accounts Not Subject to Withholding (F63) #2 .......................................................................................10 
[[Dividend]]/Capital Gain Detail for Cash Accounts Subject to Withholding (F64)  .......................................... 11 
Cash Accounts Subject to Withholding (F64) #1 ..............................................................................................11 
Cash Accounts Subject to Withholding (F64) #2 ..............................................................................................13 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Not Subject to Withholding (F65) ............... 14 
Reinvest Accounts Not Subject to Withholding (F65) #1 ..................................................................................14 
Reinvest Accounts Not Subject to Withholding (F65) #2 ..................................................................................16 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Subject to Withholding (F66) ...................... 17 
Reinvest Accounts Subject to Withholding (F66) #1 ........................................................................................17 
Reinvest Accounts Subject to Withholding (F66) #2 ........................................................................................19 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts – Supplemental Record (F67) ..................... 20 
Reinvest Accounts – Supplemental Record (F67) ............................................................................................20 
[[Dividend]]/Capital Gain First Trailer by Firm (F68) ........................................................................................... 22 
First Trailer by Firm (F68) .................................................................................................................................22 
[[Dividend]]/Capital Gain Second Trailer by Firm (F69) ...................................................................................... 23 
Second Trailer by Firm (F69) #1 .......................................................................................................................23 
Second Trailer by Firm (F69) #2 .......................................................................................................................24 
[[Dividend]]/Capital Grand Total Trailer Record (F70)......................................................................................... 25 
Grand Total Trailer Record (F70) .....................................................................................................................25 
Input Records’ Layout ....................................................................................................................................... 26 
[[Dividend]] File Datatrak Header ..........................................................................................................................26 

---

## Page 3

[[Dividend]] Reporting Record Layouts 
 
History of Important Notices 3 
 
[[Dividend]] File Datatrak Trailer ...........................................................................................................................27 
[[Dividend]] [[settlement]] Reversal File Datatrak Header ........................................................................................28 
[[Dividend]] [[settlement]] Reversal File Datatrak Trailer ..........................................................................................29 
[[Dividend]]/Capital Gain [[settlement]] Reversal .....................................................................................................30 
Output Records’ Layout .................................................................................................................................... 31 
[[Dividend]] [[settlement]] Summary - Output Detail (N80) .......................................................................................31 
[[Dividend]] [[settlement]] Summary - Output Trailer (N81) ......................................................................................33 
Output Header [[Dividend]] File (N00) ..................................................................................................................34 
Output Header - [[Dividend]] [[settlement]] Summary (N00) ....................................................................................35 
Input Acknowledgment - [[Dividend]] (NDV) .........................................................................................................36 
APPENDIX – Summary of Changes .................................................................................................................. 37 
Summary of Changes – effective Q1, 2019 ...................................................................................................... 38 
Summary of changes – effective Q4, 2017 ...................................................................................................... 39 
Summary of changes – effective Q2, 2015 ...................................................................................................... 40 
Summary of changes – effective Q3, 2014 ...................................................................................................... 41 
Summary of changes – effective November 25th, 2013 ................................................................................. 42 
Summary of changes – effective Q4, 2013 ...................................................................................................... 43 
Summary of changes – effective Q1, 2013 ...................................................................................................... 46 
Summary of changes – effective Q4, 2011 ...................................................................................................... 47 
Summary of changes – effective Q4, 2010 ...................................................................................................... 48 
  

---

## Page 4

[[Dividend]] Reporting Record Layouts 
 
History of Important Notices 4 
 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notices 
October 9, 2023 Record has been rebranded and reviewed.  
March 25, 2019 Please see Important Notices: 
a8658 P&S 8233 Dated December 19, 2018 
November 20, 2017 Please see Important Notices: 
a8402 P&S 7977 Dated June 1, 2017 
April 27, 2015 Please see Important Notices: 
a7926 P&S 7501 Dated November 4, 2014 
July 28, 2014 Please see Important Notices: 
a7687 P&S 7357 Dated February 24, 2014 
March 18, 2013 Please see Important Notices: 
a7472 P&S 7042 Dated August 16, 2012, and  
a7567 P&S 7137 Dated January 9, 2013 
October 17, 2011 Please see Important Notices: 
a7241 P&S 6811 Dated July 8, 2011 
November 22, 2010 Please see Important Notices: 
a7044 P&S 6615 Dated August 17, 2010 
June 14, 2010 Please see Important Notices: 
a6948 P&S 6518 Dated February 18, 2010 
October 20, 2008 Please see Important Notices: 
# A6658 P&S# 6228 Dated July 11, 2008 
September 17, 2007 Please see Important Notices: 
a6444 P&S 6014 Dated May 01, 2007 
November 20, 2006 Please see Important Notices: 
a6295 P&S 5865 Dated August 29, 2006 # A6272 P&S# 5842 
Dated July 17, 2006 
March 19, 2005 Please see Important Notice: 
a5976 P&S 5546 Dated February 4, 2005 

---

## Page 5

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]] Header (F61, 62) 5 
 
[[Dividend]] HEADER (F61, 62) 
[[Dividend]] Header (F61, 62) #1 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
The [[Dividend]] Header record introduces a series of detail records relevant to a particular fund’s distribution. 
This record precedes Security Issue, and distribution type grouping. 
[[Dividend]] Header (F61, 62) seq #1 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 61 = [[Dividend]] 
62 = Cap Gain 
R 
Capital Gain Indicator 4 4 1 A/N Required for Record Type 62. 
1 = Short Term Capital Gain 2 = Long Term 
Gain 
3 = Gain on Collectables 
4 = Section 1202 Gain 
5 = Unrecaptured Section 1250. 
(Effective Q4, 2017) 
OC 
Fund Payout Cycle 5 6 2 N 01 = Monthly 
02 = Quarterly 
03 = Semi-Annual 
04 = Annual 
05 = Periodic 
06 = Special 
07 = [[Stock]] Split 
R 
[[Dividend]] Distribution Type 7 7 1 N 1 = Daily Accrual 
2 = Declared Distribution 
R 
Clearing/Settling Firm 
Number 
8 11 4 N  R 
Security Issue Number 12 20 9 A/N  R 

---

## Page 6

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]] Header (F61, 62) 6 
 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Record Date 21 28 8 N mmddccyy 
Optional for [[Dividend]] Distribution Type 1. 
RC 
Reinvest Date 29 36 8 N mmddccyy 
Optional for [[Dividend]] Distribution Type 1. 
RC 
Payable Date 37 44 8 N mmddccyy 
Must be equal or greater than Record Date. 
R 
[[Dividend]] Rate/Capital 
Gain Rate 
45 49 5 N 99.999 
Blanks not allowed. Zeros allowed. 
R 
Balance Date 50 57 8 N mmddccyy R 
Posting Date 58 65 8 N mmddccyy R 
[[Dividend]] Debit/Credit 
Indicator 
66 66 1 A/N 1 = Not Applicable 
2 = [[Dividend]] Reversal (Debit) 
3 = [[Dividend]] Correction (Credit)  
4 = [[Dividend]] Debit 
5 = [[Dividend]] Credit 
R Memo Field 67 78 12 A/N  O 
Accrual Starting Date 79 86 8 N mmddccyy 
Required if [[Dividend]] Distribution Type = 1 Daily 
Accrual. 
OC 
Spillover [[Dividend]] 
Indicator 
87 87 1 A/N 0 = No 
1 = Yes 
O 
Clearing/Settling Fund # 88 91 4 A/N  R 
TPA/Investment Agent 
Number 
92 95 4 A/N  O 
Agent for Firm Number 96 99 4 A/N  O 
Filler 100 100 1 A/N Space R 
Filler 101 106 6 A/N Space R 
Sequence Number 107 108 2 A/N 01 R 
Filler/Reject Code 109 110 2 A/N Input: Space Output: Reject Code R 

---

## Page 7

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]] Header (F61, 62) 7 
 
[[Dividend]] Header (F61, 62) #2 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
The [[Dividend]] Header record introduces a series of detail records relevant to a particular fund’s distribution. 
This record precedes Security Issue, and distribution type grouping. 
[[Dividend]] Header (F61, 62) seq #2 
#2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 61 = [[Dividend]]  
62 = Cap Gain 
R 
Filler 4 7 4 A/N Space R 
Clearing/Settling Firm 
Number 
8 11 4 A/N  R 
Security Issue Number 12 20 9 A/N  R 
Filler 21 87 67 A/N Space R 
Clearing/Settling Fund # 88 91 4 A/N  R 
[[Dividend]] Rate/Capital 
Gain Rate - Extended 
92 106 15 N 999,999.999999999 
Blanks not allowed. 
Zeros allowed ONLY if [[Dividend]]/Capital Gain 
Rate field is zero. 
 
Funds that [[DO]] NOT calculate an extended rate 
must enter the rate provided in the [[Dividend]] 
Rate/Capital Gain Rate field (start 45 - end 49 in 
Seq #1) in this field as well. 
R 
Sequence Number 107 108 2 A/N 02 R 
Filler/Reject Code 109 110 2 A/N Input: Space Output: Reject Code R 

---

## Page 8

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail for Cash Accounts not Subject to Withholding (F63) 8 
 
[[Dividend]]/CAPITAL GAIN DETAIL FOR CASH 
ACCOUNTS NOT SUBJECT TO WITHHOLDING (F63) 
Cash Accounts Not Subject to Withholding (F63) #1 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
[[Dividend]]/Capital Gain Detail for Cash Accounts Not Subject to Withholding (F63) #1 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 63 R 
Network Control Indicator 4 4 1 A/N 0 = Matrix Level 0 
3 = Matrix Level 3 
4 = Matrix Level 4 
R 
Firm/Fund Identification # 5 24 20 A/N  R 
Cash [[Dividend]]/Capital Gain 
Amount 
25 40 16 N 99,999,999,999,999.99 R 
Fee Amount 41 46 6 N 9,999.99 R 
Fee Type 47 47 1 N 1 = Not Applicable 
2 = Fund Expense (Credit) 
3 = Fund Expense (Debit) 
4 = Other (Credit) 
5 = Other (Debit) 
R 
Payment Days 48 50 3 N  O 
Cash Disbursement Indicator 51 51 1 N 1 = Cash to Firm 
2 = Cash to Customer 
3 = Cash to Payable Address 
4 = Cross Fund Reinvest 
5 = 1099 Update Only 
6 = Cash to Trust 
R 

---

## Page 9

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail for Cash Accounts not Subject to Withholding (F63) 9 
 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Account Share Balance 52 64 13 N 999,999,999.9999 
Required if Account Share Balance – 
Extended is NOT provided. 
Otherwise, it is not allowed. 
OC 
Filler 65 66 2 A/N Space R 
Filler 67 68 2 A/N Space R 
Account Share Balance – 
Extended 
69 84 16 N 999,999,999,999.9999 
Required if Account Share Balance is NOT 
provided. 
Otherwise, it is not allowed. 
OC 
Filler 85 87 3 A/N Space R 
Social Code 88 89 2 A/N See Social Code list at 
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html under Codes in 
[[Mutual Funds]] section in the [[DTCC]] Learning 
Center. 
R 
Firm/Fund Identification 
Indicator 
90 90 1 A/N 1 = Fund (FIN) 
2 = Firm (BIN) 
R 
Filler 91 106 16 A/N Space R 
Sequence Number 107 108 2 A/N 01 
Required if record F63 #2 follows. 
OC 
Filler/Reject Code 109 110 2 A/N Input: Space Output: Reject Code R 
 
 
  

---

## Page 10

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail for Cash Accounts not Subject to Withholding (F63) 10 
 
Cash Accounts Not Subject to Withholding (F63) #2 
Optional Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
[[Dividend]]/Capital Gain Detail for Cash Accounts Not Subject to Withholding (F63) #2 
#2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 63 R 
Filler 4 93 90 A/N Space R 
Record Date [[shares]] 94 106 13 N 999,999,999.9999 O 
Sequence Number 107 108 2 A/N 02 R 
Filler/Reject Code 109 110 2 A/N Input: Space Output: Reject Code R 

---

## Page 11

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail for Cash Accounts Subject to Withholding (F64) 11 
 
[[Dividend]]/CAPITAL GAIN DETAIL FOR CASH 
ACCOUNTS SUBJECT TO WITHHOLDING (F64) 
Cash Accounts Subject to Withholding (F64) #1 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
[[Dividend]]/Capital Gain Detail for Cash Accounts Subject to Withholding (F64) #1 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 64 R 
Network Control Indicator 4 4 1 A/N 0 = Matrix Level 0 
3 = Matrix Level 3 
4 = Matrix Level 4 
R 
Firm/Fund Identification # 5 24 20 A/N  R 
Cash [[Dividend]]/Capital Gain 
Amount 
25 40 16 N 99,999,999,999,999.99 R 
Fee Amount 41 46 6 N 9,999.99 R 
Fee Type 47 47 1 N 1 = Not Applicable 
2 = Fund Expense (Credit)  
3 = Fund Expense (Debit)  
4 = Other (Credit) 
5 = Other (Debit) 
R 
Cash Disbursement 
Indicator 
48 48 1 N 1 = Cash to Firm 
2 = Cash to Customer 
3 = Cash to Payable Address  
4 = Cross Fund Reinvest 
5 = 1099 Update Only 
6 = Cash to Trust 
R 
Payment Days 49 51 3 N  O 

---

## Page 12

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail for Cash Accounts Subject to Withholding (F64) 12 
 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
NRA/TEFRA 
Withholding Indicator 
52 52 1 A/N Required if FATCA Withholding Indicator of 
Rec F64 seq#2 = 0 
1 = NRA 
2 = TEFRA 
OC 
NRA/TEFRA 
Withholding Rate 
53 54 2 N Required if FATCA Withholding Indicator of 
Rec F64 seq#2 = 0 
.99 (expressed as a decimal) 
OC 
NRA/TEFRA 
Withholding Amount 
55 70 16 N Required if FATCA Withholding Indicator of 
Rec F64 seq#2 = 0 
99,999,999,999,999.99 
OC 
Account Share Balance 71 83 13 N 999,999,999.9999 
Required if Account Share Balance – 
Extended is NOT provided in record F64 
sequence #2. 
Otherwise, it is not allowed. 
OC 
Filler 84 87 4 A/N Space R 
Social Code 88 89 2 A/N See Social Code list at  
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html under Codes in 
[[Mutual Funds]] section in the [[DTCC]] Learning 
Center. 
R 
Firm/Fund Identification 
Indicator 
90 90 1 A/N 1 = Fund (FIN) 
2 = Firm (BIN) 
R 
Filler 91 106 16 A/N Space R 
Sequence Number 107 108 2 A/N 01 
Required if record F64 sequence #2 follows. 
OC 
Filler/Reject Code 109 110 2 A/N Input: Space Output: Reject Code R 
 
 
  

---

## Page 13

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail for Cash Accounts Subject to Withholding (F64) 13 
 
Cash Accounts Subject to Withholding (F64) #2 
Required Record (Effective Q2, 2015)  
Input from Fund to [[NSCC]] 
Output from [[NSCC]] to Firm 
[[Dividend]]/Capital Gain Detail for Cash Accounts Subject to Withholding (F64) #2 
#2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 64 R 
Filler 4 58 55 A/N Space R 
FATCA Withholding 
Indicator 
59 59 1 A/N 0 = No 
1 = Yes 
(BLANK is not allowed) 
R 
FATCA Withholding Rate 60 61 2 N .99 (expressed as a decimal) 
Required for FATCA Withholding Indicator 1 
(Yes). Zeroes are allowed. 
OC 
FATCA Withholding 
Amount 
62 77 16 N 99,999,999,999,999.99 
Required for FATCA Withholding Indicator 1 
(Yes). Zeroes are allowed. 
OC 
Record Date [[shares]] 78 90 13 N 999,999,999.9999 O 
Account Share Balance - 
Extended 
91 106 16 N 999,999,999,999.9999 
 
Required if Account Share Balance is NOT 
provided in record F64 sequence #1. 
Otherwise, it is not allowed. 
OC Sequence number 107 108 2 A/N 02 R 
Filler/Reject Code 109 110 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 14

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Not Subject to Withholding (F65) 14 
 
[[Dividend]]/CAPITAL GAIN DETAIL RECORD FOR 
REINVEST ACCOUNTS NOT SUBJECT TO 
WITHHOLDING (F65) 
Reinvest Accounts Not Subject to Withholding (F65) #1 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Not Subject to Withholding (F65) #1 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 65 R 
Network Control Indicator 4 4 1 A/N 0 = Matrix Level 0 
3 = Matrix Level 3 
4 = Matrix Level 4 
R 
Firm/Fund Identification # 5 24 20 A/N  R 
Gross [[Dividend]]/Capital Gain 
Amount 
25 40 16 N 99,999,999,999,999.99 R 
Reinvest Price 41 52 12 N 999,999.999999 R 
Currency Indicator 53 55 3 A/N USD or spaces R 
Payment Days 56 58 3 N 999 O 
Reinvest [[shares]] 59 71 13 N 999,999,999.9999 R 
Account Share Balance 72 84 13 N 999,999,999.9999 
Required if Account Share Balance – 
Extended is NOT provided in record F65 
sequence #2. 
Otherwise, it is not allowed. 
OC Fee Amount 85 90 6 N 9,999.99 R 

---

## Page 15

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Not Subject to Withholding (F65) 15 
 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Fee Type 91 91 1 N 1 = Not Applicable 
2 = Fund Expense (Credit)  
3 = Fund Expense (Debit)  
4 = Other (Credit) 
5 = Other (Debit) 
R 
Filler 92 93 2 A/N Space R 
Filler 94 95 2 A/N Space R 
Filler 96 103 8 A/N Space R 
Social Code 104 105 2 A/N See Social Code list at  
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html under Codes in 
[[Mutual Funds]] section in the [[DTCC]] Learning 
Center. 
R 
Firm/Fund Identification 
Indicator 
106 106 1 A/N 1 = Fund (FIN) 
2 = Firm (BIN) 
R 
Sequence Number 107 108 2 A/N 01 
Required if record F65 sequence #2 follows 
OC 
Filler/Reject Code 109 110 2 A/N Input: Space  
Output: Reject Code 
R 
 
 
  

---

## Page 16

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Not Subject to Withholding (F65) 16 
 
Reinvest Accounts Not Subject to Withholding (F65) #2 
Optional Conditional Record  
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
This record is required: 
• if Account Share Balance is NOT provided in record F65 sequence #1; 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Not Subject to Withholding (F65) #2 
#2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 65 R 
Filler 4 61 58 A/N Space R 
Record Date [[shares]] 62 74 13 N 999,999,999.9999 O 
Account Share Balance - 
Extended 
75 90 16 N 999,999,999,999.9999 
Required if Account Share Balance is NOT 
provided in record F65 sequence #1. 
Otherwise, it is not allowed. 
OC 
Filler 91 106 16 A/N Space R 
Sequence number 107 108 2 A/N 02 R 
Filler/Reject Code 109 110 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 17

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Subject to Withholding (F66) 17 
 
[[Dividend]]/CAPITAL GAIN DETAIL RECORD FOR 
REINVEST ACCOUNTS SUBJECT TO WITHHOLDING 
(F66) 
Reinvest Accounts Subject to Withholding (F66) #1 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Subject to Withholding (F66) #1 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 66 R 
Network Control Indicator 4 4 1 A/N 0 = Matrix Level 0 
3 = Matrix Level 3 
4 = Matrix Level 4 
R 
Firm/Fund Identification # 5 24 20 A/N  R 
Gross [[Dividend]]/Capital Gain 
Amount 
25 40 16 N 99,999,999,999,999.99 R 
Payment Days 41 43 3 N 999 O 
NRA/TEFRA 
Withholding Indicator 
44 44 1 A/N Required if FATCA Withholding Indicator of 
Rec F66 seq#2 = 0 
1 = NRA 
2 = TEFRA 
OC 
NRA/TEFRA 
Withholding Rate 
45 46 2 N Required if FATCA Withholding Indicator of 
Rec F66 seq#2 = 0 
.99 (expressed as a decimal) 
OC 
NRA/TEFRA 
Withholding Amount 
47 62 16 N Required if FATCA Withholding Indicator of 
Rec F66 seq#2 = 0 
99,999,999,999,999.99 
OC 
Reinvest Price 63 74 12 N 999999.999999 R 
Currency Indicator 75 77 3 A/N USD or spaces R 

---

## Page 18

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Subject to Withholding (F66) 18 
 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reinvest [[shares]] 78 90 13 N 999,999,999.9999 R 
Account Share Balance 91 103 13 N 999,999,999.9999 
Required if Account Share Balance – Extended 
is NOT provided in record F66 sequence #2. 
Otherwise, it is not allowed. 
OC 
Filler 104 105 2 A/N Space R 
Firm/Fund Identification 
Indicator 
106 106 1 A/N 1 = Fund (FIN) 
2 = Firm (BIN) 
R 
Sequence Number 107 108 2 A/N 01 R 
Filler 
or Reject Code 
109 110 2 A/N Input: Filler space Output: Reject Code R 
 
 
  

---

## Page 19

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Subject to Withholding (F66) 19 
 
Reinvest Accounts Subject to Withholding (F66) #2 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts Subject to Withholding (F66) #2 
#2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 66 R 
Social Code 4 5 2 A/N See Social Code list at 
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html under Codes in 
the Mutual Fund section of the [[DTCC]] Learning 
Center. 
R 
Filler 6 58 53 A/N Space R 
FATCA Withholding 
Indicator 
59 59 1 A/N 0 = No 
1 = Yes 
(BLANK is not allowed) 
R 
FATCA Withholding Rate 60 61 2 N .99 (expressed as a decimal) 
Required for FATCA Withholding Indicator 1 
(Yes). Zeroes are allowed. 
OC 
FATCA Withholding Amount 62 77 16 N 99,999,999,999,999.99 
Required for FATCA Withholding Indicator 1 
(Yes). Zeroes are allowed. 
OC 
Record Date [[shares]] 78 90 13 N 999,999,999.9999 O 
Account Share Balance - 
Extended 
91 106 16 N 999,999,999,999.9999 
Required if Account Share Balance is NOT 
provided in record F66 sequence #1. 
Otherwise, it is not allowed. 
OC 
Sequence number 107 108 2 A/N 02 R 
Filler/Reject Code 109 110 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 20

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts – Supplemental Record (F67) 20 
 
[[Dividend]]/CAPITAL GAIN DETAIL RECORD FOR 
REINVEST ACCOUNTS – SUPPLEMENTAL RECORD 
(F67) 
Reinvest Accounts – Supplemental Record (F67) 
Optional Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
The Supplemental [[Dividend]]/Capital Gain Detail Record for Reinvest Accounts is utilized as an optional record 
for any reinvest accounts, with withholding, that require the reporting of fees for a particular [[Dividend]] as 
referenced in the proceeding header record. 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts – Supplemental Record (F67) 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 67 R 
Network Control Indicator 4 4 1 A/N 0 = Matrix Level 0 
3 = Matrix Level 3 
4 = Matrix Level 4 
R 
Firm/Fund Identification # 5 24 20 A/N  R 
Fee Amount 25 30 6 N 9,999.99 R 
Fee Type 31 31 1 N 1 = Not Applicable 
2 = Fund Expense (Credit)  
3 = Fund Expense (Debit)  
4 = Other (Credit) 
5 = Other (Debit) 
R 
Filler 32 33 2 A/N Space R 
Filler 34 35 2 A/N Space R 
Filler 36 87 52 A/N Space R 

---

## Page 21

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Detail Record for Reinvest Accounts – Supplemental Record (F67) 21 
 
Field Name Start End Len Type Description Opt/ 
Req 
Social Code 88 89 2 A/N See Social Code list at 
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html under Codes in 
the Mutual Fund section of the [[DTCC]] Learning 
Center. 
R 
Firm/Fund Identification 
Indicator 
90 90 1 A/N 1 = Fund (FIN) 
2 = Firm (BIN) 
R 
Filler 91 106 16 A/N Space R 
Sequence Number 107 108 2 A/N 01 O 
Filler/Reject Code 109 110 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 22

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain First Trailer by Firm (F68) 22 
 
[[Dividend]]/CAPITAL GAIN FIRST TRAILER BY FIRM (F68) 
First Trailer by Firm (F68) 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
The [[Dividend]]/capital gain trailer records by Security Issue and firm are used to recap the detail records that 
follow each [[Dividend]] header record. Record types 68 and 69 are both required trailer records.  
[[Dividend]]/Capital Gain First Trailer by Firm (F68) 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 68 R 
Filler 4 4 1 A/N Space R 
Firm Clearing Number 5 8 4 N  R 
Security Issue Number 9 17 9 A/N  R 
Total Cash Accounts 18 23 6 N 999,999 R 
Total Cash [[Dividend]]/Capital 
Gain Amount 
24 39 16 N 99,999,999,999,999.99 R 
Total Cash to Firm 40 55 16 N 99,999,999,999,999.99 R 
Total Cash to Customer 56 71 16 N 99,999,999,999,999.99 R 
Total Cash to Payable 72 87 16 N 99,999,999,999,999.99 R 
Total Cash to Cross Reinvest 88 103 16 N 99,999,999,999,999.99 R 
TPA/Investment Agent 
Number 
104 107 4 A/N Required only if it exist in Header Record OC 
Filler 108 108 1 A/N Space R 
Filler/Reject Code 109 110 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 23

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Second Trailer by Firm (F69) 23 
 
[[Dividend]]/CAPITAL GAIN SECOND TRAILER BY FIRM 
(F69) 
Second Trailer by Firm (F69) #1 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
[[Dividend]]/Capital Gain Second Trailer by Firm (F69) #1 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 69 R 
Trailer Sequence Number 4 4 1 A/N 1 
Required if record F69 #2 follows. 
OC 
Firm Clearing Number 5 8 4 N  R 
Security Issue Number 9 17 9 A/N  R 
Total Reinvest 
[[Dividend]]/Capital Gain Amount 
18 33 16 N 99,999,999,999,999.99 R 
Total Amount Withheld 34 49 16 N 99,999,999,999,999.99 R 
Total TEFRA Withholdings 50 65 16 N 99,999,999,999,999.99 R 
Total NRA Withholdings 66 81 16 N 99,999,999,999,999.99 R 
Total Reinvested [[shares]] 82 94 13 N 999,999,999.9999 R 
Total Reinvest Accounts 95 100 6 N 999,999 R 
Total Records 101 108 8 N 99,999,999 
Including Headers and Trailers 
R 
Filler/Reject Code 109 110 2 A/N Input: Space  
Output: Reject Code 
R 
 
 
  

---

## Page 24

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Gain Second Trailer by Firm (F69) 24 
 
Second Trailer by Firm (F69) #2 
Optional Conditional Record  
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
This record is required if FATCA Withholding Amount is greater than zero in the F64 #2 or F66 #2 records  
[[Dividend]]/Capital Gain Second Trailer by Firm (F69) #2 
#2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 69 R 
Trailer Sequence Number 4 4 1 A/N 2 R 
Firm Clearing Number 5 8 4 N  R 
Security Issue Number 9 17 9 A/N  R 
Total FATCA Withholdings 18 33 16 N 99,999,999,999,999.99 
Required if FATCA Withholding Amount is 
greater than zero in F64 #2 or F66 #2 
records. 
OC 
Filler 34 108 75 N Space R 
Filler/Reject Code 109 110 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 25

[[Dividend]] Reporting Record Layouts 
 
[[Dividend]]/Capital Grand Total Trailer Record (F70) 25 
 
[[Dividend]]/CAPITAL GRAND TOTAL TRAILER RECORD 
(F70) 
Grand Total Trailer Record (F70) 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
This [[Dividend]]/capital gain grand total trailer record is used to recap all [[Dividend]] records, including headers and 
trailers, for a [[participant]]’s entire transmission. 
[[Dividend]]/Capital Grand Total Trailer Record (F70) 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 70 = Grand Total Trailer R 
Filler 4 5 2 A/N Space R 
Fund Clearing Number / 
Recipient Number 
6 9 4 N Fund Clearing Number - on Input from 
Fund to [[NSCC]]; 
Recipient Number - on Output from [[NSCC]] 
to [[participant]] 
R 
Total [[Dividend]]/Capital Gain 
Records 
10 17 8 N 99,999,999 
Including Headers and Trailers 
R 
Filler 18 110 93 A/N Space R 

---

## Page 26

[[Dividend]] Reporting Record Layouts 
 
Input Records’ Layout 26 
 
INPUT RECORDS’ LAYOUT 
[[Dividend]] File Datatrak Header 
Input from Fund to [[NSCC]] 
[[Dividend]] File Datatrak Header 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value ‘26596’ R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value 'NETWORKING FUND DIV. INP’ R 
Multi Batch Indicator 60 60 1 A/N N = Not last batch  
Y = Last batch 
R 
Multi Batch Number 61 63 3 N  R 
Filler 64 110 47 A/N Space R 
 
 
  

---

## Page 27

[[Dividend]] Reporting Record Layouts 
 
Input Records’ Layout 27 
 
[[Dividend]] File Datatrak Trailer 
Input from Fund to [[NSCC]] 
[[Dividend]] File Datatrak Trailer 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'END.S' R 
DATATRAK SYSID 6 10 5 A/N Value '26596' R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Data File Record Count 27 33 7 N DATATRAK Header & Trailer not included 
in count 
R 
Filler 34 110 77 A/N Space R 
 
 
  

---

## Page 28

[[Dividend]] Reporting Record Layouts 
 
Input Records’ Layout 28 
 
[[Dividend]] [[settlement]] Reversal File Datatrak Header 
Input from Fund to [[NSCC]] 
[[Dividend]] [[settlement]] Reversal File Datatrak Header 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value '26195' R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value 'MFN DIV. SETT REV REQUEST' R 
Multi Batch Indicator 60 60 1 A/N N = Not last batch  
Y = Last batch 
R 
Multi Batch Number 61 63 3 N  R 
Filler 64 80 17 A/N Space R 
 
 
  

---

## Page 29

[[Dividend]] Reporting Record Layouts 
 
Input Records’ Layout 29 
 
[[Dividend]] [[settlement]] Reversal File Datatrak Trailer 
Input from Fund to [[NSCC]] 
[[Dividend]] [[settlement]] Reversal File Datatrak Trailer 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'END.S' R 
DATATRAK SYSID 6 10 5 A/N Value '26195' R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Data File Record Count 27 33 7 N DATATRAK Header & Trailer not included in 
count 
R 
Filler 34 80 47 A/N Space R 
 
 
  

---

## Page 30

[[Dividend]] Reporting Record Layouts 
 
Input Records’ Layout 30 
 
[[Dividend]]/Capital Gain [[settlement]] Reversal 
Input from Fund to [[NSCC]] 
The record is used to reverse the [[Dividend]] [[settlement]] figures of the previous day for a Fund.  
[[Dividend]]/Capital Gain [[settlement]] Reversal 
Field Name Start End Len Type Description Opt/ 
Req 
Fund Number 1 4 4 A/N  R 
6- digit Reversal Date 5 10 6 A/N mmddyy 
Required if 8-digit date is Space 
OC 
8- digit Reversal date 11 18 8 A/N mmddccyy 
Required if 6-digit date is Space 
OC 
Filler 19 80 62 A/N Space R 

---

## Page 31

[[Dividend]] Reporting Record Layouts 
 
Output Records’ Layout 31 
 
OUTPUT RECORDS’ LAYOUT 
[[Dividend]] [[settlement]] Summary - Output Detail (N80) 
Output from [[NSCC]] to Funds and Firm s 
[[Dividend]] [[settlement]] Summary - Output Detail (N80) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 80= Detail [[settlement]] Output 
Sequence Number 4 4 1 A/N 1 
MRO Recipient Number 5 8 4 N  
Security Issue Number 9 17 9 A/N  
Pay-Receive Code 18 18 1 N 2 = Your Debit  
4 = Your Credit 
Contra Clearing [[Member]] # 19 22 4 N  
[[settlement]] Date 23 30 8 N mmddccyy 
Fund Symbol 31 40 10 A/N  
[[settlement]] Value 41 56 16 N 99,999,999,999,999.99 
[[settlement]] Type 57 59 3 A/N DIV = [[Dividend]] [[settlement]] 
DVC = [[Dividend]] Correction  
DVR = [[Dividend]] Reversal 
[[settlement]] Indicator 60 60 1 A/N 'D’ = [[Dividend]] [[settlement]] 
'N' = Non-Resident Alien Tax Withheld  
'S' = Spillover [[Dividend]] 
'T' = TEFRA Withholding 
‘F’ = FATCA Withholding 
Record Date 61 68 8 N mmddccyy 
Payable Date 69 76 8 N mmddccyy 
[[Dividend]] Distribution Indicator 77 77 1 A/N 1 = [[Dividend]]  
2 = Cap Gain 

---

## Page 32

[[Dividend]] Reporting Record Layouts 
 
Output Records’ Layout 32 
 
Field Name Start End Len Type Description 
[[Dividend]] [[settlement]] Funds Type 78 78 1 A/N N = Next-Day Funds  
S = Same-Day Funds 
TPA/Investment Agent or Firm 
Number 
79 82 4 A/N Firm Number if MRO Recipient Type = ‘A’ or ‘T’. 
Otherwise, TPA/Investment Agent Number, or 
space 
Filler 83 89 7 A/N Space 
Currency Indicator 90 92 3 A/N For future use 
Filler 93 131 39 A/N Space 
MRO Recipient Type 132 132 1 A/N ‘A’ = Investment Agent  
‘B’ = Firm 
‘F’ = Fund  
‘T’ = TPA 
 
 
  

---

## Page 33

[[Dividend]] Reporting Record Layouts 
 
Output Records’ Layout 33 
 
[[Dividend]] [[settlement]] Summary - Output Trailer (N81) 
Output from [[NSCC]] to Funds and Firm s 
[[Dividend]] [[settlement]] Summary - Output Trailer (N81) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 81 = Trailer Totals 
Sequence Number 4 4 1 A/N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '99999999999' 
Literal 20 27 8 A/N Value 'SETT.TRL' 
Same Day [[settlement]] Date 28 35 8 N mmddccyy 
Debit Items Same Day [[settlement]] 36 41 6 N 999,999 
Debit Amount Same Day 
[[settlement]] 
42 57 16 N 99,999,999,999,999.99 
Credit Items Same Day [[settlement]] 58 63 6 N 999,999 
Credit Amount Same Day 
[[settlement]] 
64 79 16 N 99,999,999,999,999.99 
Debit Items Next Day [[settlement]] 80 85 6 N 999,999 
Debit Amount Next Day [[settlement]] 86 101 16 N 99,999,999,999,999.99 
Credit Items Next Day [[settlement]] 102 107 6 N 999,999 
Credit Amount Next Day 
[[settlement]] 
108 123 16 N 99,999,999,999,999.99 
Next Day [[settlement]] Date 124 131 8 N mmddccyy 
MRO Recipient Type 132 132 1 A/N ‘A’ = Investment Agent  
‘B’ = Firm 
‘F’ = Fund 
‘T’ = TPA 
 
 
  

---

## Page 34

[[Dividend]] Reporting Record Layouts 
 
Output Records’ Layout 34 
 
Output Header [[Dividend]] File (N00) 
Output from [[NSCC]] to Funds and Firm s 
Output Header [[Dividend]] File (N00) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 4 1 A/N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '11111111111' 
Transmission Date 20 27 8 N mmddccyy 
Autoroute File [[ID]] 28 35 8 A/N Value '02102026' 
Literal 36 43 8 A/N Value '[[Dividend]]' 
Filler 44 110 67 A/N Space 
 
 
  

---

## Page 35

[[Dividend]] Reporting Record Layouts 
 
Output Records’ Layout 35 
 
Output Header - [[Dividend]] [[settlement]] Summary (N00) 
Output from [[NSCC]] to Funds and Firms 
Output Header - [[Dividend]] [[settlement]] Summary (N00) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 4 1 A/N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '11111111111' 
Transmission Date 20 27 8 N mmddccyy 
Autoroute File [[ID]] 28 35 8 A/N Value '02102193' 
Literal 36 52 17 A/N Value '[[Dividend]] SETTLE' 
Filler 53 132 80 A/N Space 
 
 
  

---

## Page 36

[[Dividend]] Reporting Record Layouts 
 
Output Records’ Layout 36 
 
Input Acknowledgment - [[Dividend]] (NDV) 
Output from [[NSCC]] to Fund 
Input Acknowledgment - [[Dividend]] (NDV) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N DV = [[Dividend]] 
Filler 4 4 1 A/N Space 
Clearing/Settling Fund # 5 8 4 N  
Processing Date 9 16 8 N mmddccyy 
Total Records Received 17 24 8 N 99,999,999 
(Includes any Headers and Trailers) 
Filler 25 110 86 A/N Space 
 
 

---

## Page 37

[[Dividend]] Reporting Record Layouts 
 
APPENDIX – Summary of Changes 37 
 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes. 
 

---

## Page 38

[[Dividend]] Reporting Record Layouts 
 
Summary of Changes – effective Q1, 2019 38 
 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 39

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective Q4, 2017 39 
 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2017 
Change to Description to Existing Fields 
Field Name Record Type and Location Old Description New Description 
Capital Gain Indicator 61/62 seq#1, start 4, end 4, 
length 1, N, OC 
Required for Record Type 62.  
1 = Short Term Capital Gain  
2 = Long Term Gain 
3 = Gain on Collectables  
4 = Section 1202 Gain  
5 = Unrecaptured Section 
1250.  
Must be equal 2 or 3 when 5-
Year Capital Gain Rate is 
Provided. 
Required for Record Type 62.  
1 = Short Term Capital Gain  
2 = Long Term Gain 
3 = Gain on Collectables  
4 = Section 1202 Gain  
5 = Unrecaptured Section 
1250. 
 
Rename of Existing Fields 
New Field Name Record Type and Location Old Name 
Filler 61/.62, seq#1, start 101, end 106, length 6, A/N, R 5-Year Capital Gain Rate 
Filler F63 seq#1, start 91, end 106, length 16, A/N, R 
F64 Seq#1, start 91, end 106, length 16, A/N, R 
F65 Seq#2, start 91, end 106, length 16, A/N, R 
F67, start 91, end 106, length 16, A/N, R 
5-Year Capital Gain Amount 

---

## Page 40

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective Q2, 2015 40 
 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2015 
Rename and Change of Requirements for Existing Fields 
Field Name Record Type, Location, field type New Requirement and Description 
NRA/TEFRA 
Withholding Indicator 
64 seq#1, start 52, end 52, length 1, A/N, 
OC 
Required if FATCA Withholding Indicator of Rec 
F64 seq#2 = 0 
1 = NRA 
2 = TEFRA 
NRA/TEFRA 
Withholding Indicator 
66 seq#1, start 44, end 44, length 1, A/N, 
OC 
Required if FATCA Withholding Indicator of Rec 
F66 seq#2 = 0 
1 = NRA 
2 = TEFRA 
NRA/TEFRA 
Withholding Rate 
64 seq#1, start 53, end 54, length 2, N, OC Required if FATCA Withholding Indicator of Rec 
F64 seq#2 =0 
.99 (expressed as a decimal) 
NRA/TEFRA 
Withholding Rate 
66 seq#1, start 45, end 46, length 2, N, OC Required if FATCA Withholding Indicator of Rec 
F66 seq#2 =0 
.99 (expressed as a decimal) 
NRA/TEFRA 
Withholding Amount 
64 seq#1, start 55, end 70, length 16, N, 
OC 
Required if FATCA Withholding Indicator of Rec 
F64 seq#2 = 0 
99,999,999,999,999.99 
NRA/TEFRA 
Withholding Amount 
66 seq#1, start 47, end 62, length 16, N, 
OC 
Required if FATCA Withholding Indicator of Rec 
F66 seq#2 = 0 
99,999,999,999,999.99 
FATCA Withholding 
Indicator 
64 seq#2, start 59, end 59, length 1, A/N, 
R 
66 seq#2, start 59, end 59, length 1, A/N, 
R 
0 = No 
1 = Yes 
(BLANK is not allowed) 
 
Requirements Changed for Existing Record 
Record Record Name Old Requirements New Requirements 
F64 sequence #2 [[Dividend]]/Capital Gain Detail Record 
For Cash Accounts Subject To 
Withholding (F64) #2 
Optional Conditional Record. Required Record. 

---

## Page 41

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective Q3, 2014 41 
 
SUMMARY OF CHANGES – EFFECTIVE Q3, 2014 
Rename Existing Fields 
New Field Name Record Type and Location Old Name 
Filler F63 seq#1, start 65, end 66, length 2, A/N, R 
F64 Seq#1, start 84, end 85, length 2, A/N, R 
F65 Seq#1, start 92, end 93, length 2, A/N, R 
F66 Seq#1, start 104, end 105, length 2, A/N, R 
F67, start 32, end 33, length 2, A/N, R 
Fund Alpha Code 
Filler F63 seq#1, start 67, end 68, length 2, A/N, R 
F64 Seq#1, start 86, end 87, length 2, A/N, R 
F65 Seq#1, start 94, end 95, length 2, A/N, R 
F66 Seq#1, start 109, end 110, length 2, A/N, R 
F67, start 34, end 35, length 2, A/N, R 
Firm Alpha Code 

---

## Page 42

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective November 25th, 2013 42 
 
SUMMARY OF CHANGES – EFFECTIVE NOVEMBER 
25TH, 2013 
Requirements Clarified for Existing Fields 
Field Name Record Type, Location, field type Requirement and Description 
[[Dividend]] Rate/ 
Capital Gain Rate 
61/62 seq#1, start 45, end 49, length 5, 
N 
Required. 99.999 
Blanks not allowed.  
Zeros allowed 
[[Dividend]] Rate/ 
Capital Gain Rate - 
Extended 
61/62 seq#2, start 92, end 106, length 
15, N 
Required. 999,999.999999999 
Blanks not allowed. 
Zeros allowed ONLY if [[Dividend]]/Capital Gain Rate field 
is zero 

---

## Page 43

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective Q4, 2013 43 
 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2013 
Add New Records 
Record Record Name Requirements 
F61/62 sequence 
#2 
[[Dividend]] Header (F61/62) #2 Required 
F63 sequence #2 [[Dividend]]/Capital Gain Detail For Cash 
Accounts Not Subject To Withholding 
(F63) #2 
Optional 
 
Added New Field 
Field Name Record Type and Location Requirement 
[[Dividend]] Rate/ 
Capital Gain Rate - 
Extended 
61/62 seq#2, start 92, end 106, length 15, N Required. 999,999.999999999 
Record Date [[shares]] seq#2, start 94, end 106, length 13, N 
seq#2, start 78, end 90, length 13, N 
seq#2, start 62, end 74, length 13, N 
seq#2, start 78, end 90, length 13, N 
Optional 
 
999,999,999.9999 
 
Change Description for Existing Fields 
Field Name Record Type and Location Old Description New Description 
[[Dividend]] Distribution Type 61/62 seq#1, start 7, end 7, 
length 1, N, Required 
1 = Accrual 
2 = [[Equity]] 
1 = Daily Accrual 
2 = Declared Distribution 
 
Requirements Changed for Existing Record 
Record  Record Name  Old Requirements  New Requirements 
F66 sequence #2 [[Dividend]]/Capital Gain Detail  
Record For Reinvest 
Accounts  
Subject To Withholding (F66) 
#2 
Optional Conditional Record. 
This record is required if F66  
sequence #1 is provided. 
Required Record. 
(Documentation Correction) 
 
 

---

## Page 44

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective Q4, 2013 44 
 
Requirements Changed for Existing Fields 
Field Name  Record Type, Location, Current 
Requirements  
New Requirement and Description 
Sequence Number 61/62 seq#1, start 107, end 108, length 
2, A/N, Optional 
01 
Required. 
Sequence Number 63 seq#1, start 107, end 108, length 2, 
A/N, Optional 
01 
Optional Conditional. 
Required if record F63 seq #2 follow s. 
Sequence Number 66 seq #1, start 107, end 108, length 2, 
A/N, OC 
Required if record F66 sequence #2 
follow s. 
01 
Required. (Documentation correction) 
 
FATCA: Added New Field 
Field Name Record Type and Location Requirement 
FATCA Withholding 
Indicator 
64 seq#2, start 59, end 59, length 1, A/N, 
Optional 
66 seq#2, start 59, end 59, length 1, A/N, 
Optional 
0 = No 
1 = Yes 
FATCA Withholding 
Rate 
64 seq#2, start 60, end 61, length 2, N , OC 
66 seq#2, start 60, end 61, length 2, N , OC 
.99 (expressed as a decimal) 
Required for FATCA Withholding Indicator 1 
(Yes). Zeroes are allow ed. 
FATCA Withholding 
Amount 
64 seq#2, start 62, end 77, length 16, N ,OC 
66 seq#2, start 62, end 77, length 16, N ,OC 
99,999,999,999,999.99 
 
Required for FATCA Withholding Indicator 1 
(Yes). Zeroes are allow ed. 
Trailer Sequence 
Number 
69 seq#1, start 4, end 4, length 1, A/N ,OC 1 
Required if record F69 #2 follow s. 
Total FATCA 
Withholdings 
69 seq#2, start 18, end 33, length 16, N ,OC 99,999,999,999,999.99 
Required if FATCA Withholding Amount is 
greater than zero in F64 #2 or F66 #2 records. 
 
 
 
 
 

---

## Page 45

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective Q4, 2013 45 
 
FATCA: Add New Record 
Record Record Name Requirements 
F69 sequence #2 [[Dividend]] Second Trailer (F69) #2 Optional Conditional. 
Required if FATCA Withholding Amount is greater than 
zero in F64 #2 or F66 #2 records. 
 
FATCA: Added New Value to Existing Field 
Field Name Record Type and Location Requirement 
[[settlement]] Indicator N80, start 60, end 60, length 1, A/N 'D’ = [[Dividend]] [[settlement]] 
'N' = Non Resident Alien Tax Withheld 'S' = 
Spillover [[Dividend]] 
'T' = TEFRA Withholding 
‘F’ = FATCA Withholding 

---

## Page 46

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective Q1, 2013 46 
 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2013 
Requirements Changed for Existing Fields 
Field Name Record Type, Location, Current 
Requirements 
New Requirement and Description 
Network Control Indicator F63, start 4, end 4, length 1, A/N, R  
F64 Seq#1, start 4, end 4, length 1, A/N,  
R F65 Seq#1, start 4, end 4, length 1, A/N,  
R F66 Seq#1, start 4, end 4, length 1, A/N,  
R F67, start 4, end 4, length 1, A/N, R 
0 = Matrix Level 0 
3 = Matrix Level 3 
4 = Matrix Level 4 
 
(Removed 1 = Level 1; 2 = Level 2 effective 
Q1, 2013) 
Also updated description to “Matrix Level” 

---

## Page 47

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective Q4, 2011 47 
 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2011 
Added new Field 
Field Name  Record Type and Location Requirement 
Social Code F63, start 88, end 89, length 2  
F64 seq#1, start 88, end 89, length 2  
F65 seq#1, start 104, end 105, length 2  
F66 seq#2, start 4, end 5, length 2  
F67, start 88, end 89, length 2 
Required 
 
Requirements Changed for Existing Record 
Record Record Name Old Requirements New Requirements 
F66 sequence # 2 [[Dividend]]/Capital Gain 
Detail Record For Reinvest 
Accounts Subject To 
Withholding (F66) #2 
Optional Conditional Record. 
This record is required if Account 
Share Balance is NOT provided in 
record F66 sequence #1.  
Otherwise it is optional. 
Optional Conditional Record. 
This record is required if F66 
sequence #1 is provided. 

---

## Page 48

[[Dividend]] Reporting Record Layouts 
 
Summary of changes – effective Q4, 2010 48 
 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2010 
Change Description of Existing Fields 
Field Name  Record Type and Location Old Description New Description 
Capital Gain 
Indicator 
61/62, start 4, end 4, length 1,  
Optional / Conditional 
Required for Record Type 62.  
 
1 = Short Term Capital Gain  
2 = 20% Rate Gain  
3 = 28% Rate Gain  
4 = Section 1202 Gain  
5 = Unrecaptured Section 1250.  
 
Must be equal 2 or 3 when  
5-Year Capital Gain Rate is 
Provided. 
Required for Record Type 62.  
 
1 = Short Term Capital Gain  
2 = Long Term Gain 
3 = Gain on Collectables  
4 = Section 1202 Gain  
5 = Unrecaptured Section 1250.  
 
Must be equal 2 or 3 when 5-Year 
Capital Gain Rate is Provided. 
 
 
 

---

## Page 49

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 9, 2023 
Publication Code: MFS331 
Service: Networking 
Title: [[Dividend]] Reporting Record Layouts  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 