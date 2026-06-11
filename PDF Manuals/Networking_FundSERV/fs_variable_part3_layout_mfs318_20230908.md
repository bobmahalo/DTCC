---
title: "Fund/SERV: Variable Length Record Layouts (Part 3)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_variable_part3_layout_mfs318_20230908.pdf"
pages: 63
size: "710.5 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Fund/SERV: Variable Length Record Layouts (Part 3)

**Original File:** [fs_variable_part3_layout_mfs318_20230908.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_variable_part3_layout_mfs318_20230908.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 63  
**File Size:** 710.5 KB  

---

## Page 1

 
 
 
Fund/SERV® 
VARIABLE LENGTH RECORD LAYOUTS (PART 3) 
SEPTEMBER 8, 2023 
 

---

## Page 2

Variable Length Record Layouts (Part 3) 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092) 2 
HISTORY OF CHANGES 
Dates Important Notices 
September 8, 2023 Record has been rebranded and reviewed.  
March 10, 2023 • 529 Account Plan fields added to 018 and 019 records (effective May 15, 
2023). 
  Please see Important Notice:  
  a9267 P&S 8840 Dated February 10, 2023 
• Summary of Changes has been moved to back of document 
• Record has been rebranded 
Effective Date: March 28, 2022 Please see Important Notices: 
a9045 P&S 8618 & a9044 P&S 8617 Dated September 2, 2021 
December 7, 2021 Document links updated due to launch of new Learning Center 
Effective Date: March 25, 2019 Please see Important Notice: 
a8658 P&S a8233 Dated December 19, 2018 
Effective Date: November 20, 2017 Please see Important Notice: 
a8402 P&S 7977 Dated June 1, 2017 
Effective Date: September 26, 2016      Please see Important Notice: 
a8159 P&S 7734 Dated February 3, 2016 
Effective Date: February 29, 2016 Please see Important Notice: 
a8107 P&S 7682 Dated October 27, 2015 
Effective Date:  July 27, 2015 Please see Important Notice:  
a7997 P&S 7572 Dated March 12, 2015 
Effective Date:  April 27, 2015 Please see Important Notice:  
a7926 P&S 7501 Dated November 4, 2014 
Documentation Changes a7865  P&S 7435 Dated July 2, 2014 
Effective Date:  July 28, 2014 Please see Important Notice:  
a7701 P&S 7371 Dated May 15, 2014 (REVISED) 
a7701 P&S 7371 Dated March 17, 2014 
Effective Date:  November 18, 2013 Please see Important Notice:  
a7665 P&S 7235 Dated July 3, 2013 
Effective Date:  March 18, 2013 Please see Important Notice:  
a7472 P&S 7042 Dated August 16, 2012 (enhancement details) 
a7567 P&S 7137 Dated January 9, 2013 (revised dates) 
a7570 P&S 7140 Dated January 11, 2013 

---

## Page 3

Variable Length Record Layouts (Part 3) 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092) 3 
Dates Important Notices 
Documentation Changes Please see Important Notice: 
a7592 P&S 7162 Dated March 1, 2013 
Effective Date:  April 23, 2012 Please see Important Notice:  
A7355 P&S 6925 Dated January 12, 2012 
Note: On 2/27/2012 a correction was made to 401 Records to reflect the 
changes that were made in accordance with Important Notice a6272 P&S 
5842.   
The Fund Account Indicator 4 (New Account – U.S. Tax Resident Living Abroad) 
has been added to Account Repre sentative Name, Account Representative 
Number and Branch Identification Number fields as part of conditional 
requirements. 
Effective Date:  December 5, 2011 Please see Important Notice:  
a7256 P&S 6826 Dated July 29, 2011 
Effective Date:  October 17, 2011 Please see Important Notice:  
a7241 P&S 6811 Dated July 8, 2011 
Effective Date: June 13, 2011 Please see Important Notice:  
a7175 P&S 6745 Dated March 7, 2011 
Effective Date: January 18, 2011 Please see Important Notice:  
a7079 P&S 6650 Dated October 18, 2010 
Effective Date: November 22, 2010 Please see Important Notice:  
a7044 P&S 6615 Dated August 17, 2010 
Effective Date: December 7, 2009 Please see Important Notice:  
a6874 P&S 6444 Dated September 17, 2009 
Effective Date: October 5, 2009 Please see Important Notice:  
a6819 P&S 6389 Dated May 8, 2009  
Effective Date: December 1, 2008 Please see Important Notices:  
a6667 P&S 6237 Dated July 29, 2008 
a6653 P&S 6223 Dated July 7, 2008 
a6620 P&S 6190 Dated May 20, 2008 

---

## Page 4

Variable Length Record Layouts (Part 3) 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092) 4 
TABLE OF CONTENTS 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092)  ........................................................... 6 
02.17.01 Reminders (080) .................................................................................................................................. 6 
Firm/TPA/Investment Agent/TPP Input Trailer (999) ......................................................................................... 8 
02.18.01 Firm/TPA Input Trailer (999) ................................................................................................................ 8 
Fund Input Trailer (999) ..................................................................................................................................... 10 
02.19.01 Find Input Trailer (999) ......................................................................................................................10 
[[NSCC]] Output Header (000) ................................................................................................................................ 11 
02.20.01 [[NSCC]] Output Header (000) ..............................................................................................................11 
[[NSCC]] Output Trailer (999) ................................................................................................................................. 12 
02.21.01 [[NSCC]] Output Trailer (999) ................................................................................................................12 
Grand Total Trailer (GTT) .................................................................................................................................. 14 
02.22.01 Grand Total Trailer (GTT) ..................................................................................................................14 
Settling Trade Detail (070); X -[[settlement]] Trade Detail (072); Settling Trade Detail for TPA/Investment 
Agent/TPP (074) .................................................................................................................................................. 15 
02.23.01 Settling Trade Detail (070) .................................................................................................................15 
Settling Trade Trailer (071); X -[[settlement]] Trade Trailer (073); Settling Trade Trailer for TPA/Investment 
Agent/TPP (075) .................................................................................................................................................. 18 
02.24.01 Settling Trade Trailer (071) ................................................................................................................18 
Multiple Reject Codes (120) .............................................................................................................................. 20 
02.25.01 Multiple Reject Codes (120) ..............................................................................................................20 
Data Trak Header ................................................................................................................................................ 22 
02.26.01 DataTrak Header Record 1................................................................................................................22 
Data Trak Trailer ................................................................................................................................................. 23 
02.27.01 DataTrak Trailer Record 1 .................................................................................................................23 
Firm Exit (139) ..................................................................................................................................................... 24 
02.28.01 Firm Exit (139) ...................................................................................................................................24 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026)  ................... 28 
02.29.01 Correction (003) .................................................................................................................................28 
SSN/EIN Suffix .................................................................................................................................................... 57 
02.30.01 SSN/EIN SUFFIX ...............................................................................................................................57 

---

## Page 5

Variable Length Record Layouts (Part 3) 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092) 5 
Interval Fund Acknowledgement (030) ............................................................................................................ 60 
02.31.01 Acknowledgement (030) ....................................................................................................................60 
 
  

---

## Page 6

Variable Length Record Layouts (Part 3) 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092) 6 
REMINDERS (080, 081, 082, 083, 084, 085, 086, 087, 088, 
089, 091, 092) 
02.17.01 Reminders (080) 
Output from [[NSCC]]. For record types 091 and 092, Firm means Receiving Fund, and Fund means  
Delivering Fund. 
Field Name  Start End Len Type Description  
Record Length 1 4 4 N 0104 
Physical Sequence Number 5 6 2 A/N 01 
Logical Sequence Number 7 8 2 A/N 01  
Originator Type 9 9 1 A/N N = [[NSCC]]  
Filler 10 11 2 A/N Space 
Firm Number (for record 
type 080 this is the 
receiving firm) 
12 15 4 N  
Filler 16 18 3 A/N Space 
Record Type 19 21 3 A/N 080 =Pending ACATS Transfer 
Acknowledgment (output from [[NSCC]] to funds 
only) 
081 = Order Not Acted Upon 
082 = Deletion of Order Not Acted Upon 
083 = Pending Registration 
084 = Extended Correction Transfer Not Acted 
Upon 
085 = Pending Release to [[settlement]] 
086 = Pending Correction Confirmation 
087 = Pending Registration Acknowledgment 
088 = Pending Exchange Reconfirmation 
089 = Post [[settlement]] Correction/Cancellation 
Not Acted Upon 
091 = Pending ToRA Acknowledgment 
092 = Pending ToRA Confirmation 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
Filler 23 23 1 A/N Space 
Fund Number 24 27 4 N  

---

## Page 7

Variable Length Record Layouts (Part 3) 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092) 7 
Field Name  Start End Len Type Description  
Filler 28 30 3 A/N Space 
Security Issue Country 
Code 
31 32 2 A/N Space. For future use 
Security Issue [[ID]] 33 41 9 A/N  
Security Issue Check Digit 42 42 1 A/N Space. For future use  
Security Issue Type 43 44 2 A/N  
Control Number 45 59 15 A/N  
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / cancellation 
Space = No correction  
ACATS TIF Number 61 74 14 A/N For record type 080 Only. 
First 14 bytes of ACATS Control Number 
Delivering Firm Number 75 78 4 A/N For record type 080 only 
Reminder Age 79 82 4 N 1-9998 = Reminder age (in business days) 
9999 = Pending period expired, original 
transaction deleted by Fund/SERV 
Reminder 080 record with age 9999 will no 
longer be sent to Funds (Important Notice 
A8107) 
ACATS [[Asset]] Sequence 
Number 
83 88 6 A/N For record type 080 Only. 
Last 6 bytes of ACATS Control Number 
TPA/Investment Agent/TPP 
Number 
89 92 4 A/N  
Service Provider Number 93 96 4 A/N  
Original Record Type 97 99 3 A/N  
Filler 100 104 5 A/N Space 

---

## Page 8

Variable Length Record Layouts (Part 3) 
Firm/TPA/Investment Agent/TPP Input Trailer (999) 8 
FIRM/TPA/INVESTMENT AGENT/TPP INPUT TRAILER 
(999) 
02.18.01 Firm/TPA Input Trailer (999) 
Input from firms, TPAs and Investment Agents to [[NSCC]] 
Field Name  Start End Len Type Description  Opt/ 
Req 
Record Length 1 4 4 N 0104 R 
Physical Sequence 
Number 
5 6 2 A/N 01 R 
Logical Sequence 
Number 
7 8 2 A/N 01 R 
Originator Type 9 9 1 A/N A = Investment Agent 
B = Firm 
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = Third Party Provider  
R 
Filler 10 11 2 A/N Space R 
Firm/TPA/SP/Investment 
Agent /TPP Number 
12 15 4 N  R 
Filler 16 18 3 A/N Space R 
Record Type 19 21 3 A/N 999 = Trailer R 
Submission Date 22 29 8 N mmddccyy R 
Total Order Transactions 30 35 6 N 999,999 R 
Total Firm Delete 
Transactions 
36 41 6 N 999,999 R 
Total Correction 
Transactions 
42 47 6 N 999,999 R 
Total As-Of Transactions 48 53 6 N 999,999 R 
Total Registration 
Transactions 
54 59 6 N 999,999 R 
Total Exchange 
Transactions 
60 65 6 N 999,999 R 
Filler 66 71 6 A/N Space R 

---

## Page 9

Variable Length Record Layouts (Part 3) 
Firm/TPA/Investment Agent/TPP Input Trailer (999) 9 
Field Name  Start End Len Type Description  Opt/ 
Req 
Total Other Transactions 72 77 6 N 999,999 R 
Filler 78 104 27 A/N Space R 

---

## Page 10

Variable Length Record Layouts (Part 3) 
Fund Input Trailer (999) 10 
FUND INPUT TRAILER (999) 
02.19.01 Find Input Trailer (999) 
Input from funds to [[NSCC]] 
Field Name Start End Len Type Description  Opt/ 
Req 
Record Length 1 4 4 N 0104 R 
Physical Sequence 
Number 
5 6 2 A/N 01 R 
Logical Sequence 
Number 
7 8 2 A/N 01 R 
Originator Type 9 9 1 A/N F = Fund R 
Filler 10 11 2 A/N Space R 
Fund Number 12 15 4 N  R 
Filler 16 18 3 A/N Space R 
Record Type 19 21 3 A/N 999 = Trailer R 
Submission Date 22 29 8 N mmddccyy R 
Total Confirmation 
Transactions 
30 35 6 N 999,999 R 
Total Reconfirmation 
Transactions 
36 41 6 N 999,999 R 
Total Fund Order 
Transactions 
42 47 6 N 999,999 R 
Total Release to 
[[settlement]] Transactions 
48 53 6 N 999,999 R 
Total Fund Delete 
Transactions 
54 59 6 N 999,999 R 
Filler 60 71 12 A/N Space  R 
Total Other Transactions 72 77 6 N 999,999 R 
Filler 78 104 27 A/N Space R 

---

## Page 11

Variable Length Record Layouts (Part 3) 
[[NSCC]] Output Header (000) 11 
[[NSCC]] OUTPUT HEADER (000) 
02.20.01 [[NSCC]] Output Header (000) 
Output from [[NSCC]] 
Field Name Start End Len Type Description  
Record Length  1 4 4 N 0104 
Physical Sequence 
Number 
5 6 2 A/N 01 
Logical Sequence Number 7 8 2 A/N 01 
Originator Type 9 9 1 A/N N = [[NSCC]] 
Filler 10 11 2 A/N Space 
Recipient Number 12 15 4 N  
Filler 16 18 3 A/N Space 
Record Type 19 21 3 A/N 000 = [[NSCC]] Output Header 
Transmission Date 22 29 8 N mmddccyy 
Literal 30 33 4 A/N FILE 
AutoRoute File Number 34 41 8 A/N  
AutoRoute File Cycle 42 43 2 A/N  
File Description 44 61 18 A/N [[Mutual Funds]] INPUT 
or 
SETT TRADE HEADER 
or 
XSETT TRADE HEADER 
or 
FIRM LATE INPUT 
or 
[[Mutual Funds]] MCS 
or 
SETT TRD HDR MCS 
 
Filler 62 104 43 A/N Space  

---

## Page 12

Variable Length Record Layouts (Part 3) 
[[NSCC]] Output Trailer (999) 12 
[[NSCC]] OUTPUT TRAILER (999) 
02.21.01 [[NSCC]] Output Trailer (999) 
Output from [[NSCC]] 
Field Name Start End Len Type Description  
Record Length 1 4 4 N 0197 
Physical Sequence Number 5 6 2 A/N 01 
Logical Sequence Number 7 8 2 A/N 01 
Originator Type 9 9 1 A/N N = [[NSCC]] 
Filler 10 11 2 A/N Space 
Recipient Number 12 15 4 N  
Filler 16 18 3 A/N Space 
Record Type 19 21 3 A/N 999 = Trailer 
Transmission Date 22 29 8 N mmddccyy 
Total Order Transactions 30 35 6 N 999,999 
Total Firm Delete 
Transactions 
36 41 6 N 999,999 
Total Correction 
Transactions 
42 47 6 N 999,999 
Total As-Of Transactions 48 53 6 N 999,999 
Total Confirmation 
Transactions 
54 59 6 N 999,999 
Total Reconfirmation 
Transactions 
60 65 6 N 999,999 
Total Fund Order 
Transactions 
66 71 6 N 999,999 
Total Release to [[settlement]] 
Transactions 
72 77 6 N 999,999 
Total Fund Delete 
Transactions 
78 83 6 N 999,999 
Total Registration 
Transactions 
84 89 6 N 999,999 
Total Reminders 90 95 6 N 999,999 

---

## Page 13

Variable Length Record Layouts (Part 3) 
[[NSCC]] Output Trailer (999) 13 
Field Name Start End Len Type Description  
Filler 96 104 9 A/N Space 
Total Cash Adjustments 
Transactions 
105 110 6 N 999,999 
Total Exchange Order 
Transactions 
111 116 6 N 999,999 
Total Exchange 
Confirmation Transactions 
117 122 6 N 999,999 
Total Exchange 
Reconfirmation Transactions 
123 128 6 N 999,999 
Filler 129 164 36 A/N Space 
Total Other Transactions 165 170 6 N 999,999 
Filler 171 197 27 A/N Space 

---

## Page 14

Variable Length Record Layouts (Part 3) 
Grand Total Trailer (GTT) 14 
GRAND TOTAL TRAILER (GTT) 
02.22.01 Grand Total Trailer (GTT) 
Output from [[NSCC]]. This trailer record is available upon request. It is especially beneficial for service 
bureaus or transfer agents or any other processor who handles multiple [[NSCC]] participants or 
members. 
Field Name Start End Len Type Description  
Record Length 1 4 4 N 0104 
Physical Sequence Number 5 6 2 A/N 01 
Logical Sequence Number 7 8 2 A/N 01 
Originator Type 9 9 1 A/N N = [[NSCC]] 
Filler 10 18 9 A/N Space 
Record Type 19 21 3 A/N GTT = Grand Total Trailer 
Transmission Date 22 29 8 N mmddccyy 
Total Records 30 37 8 N 99,999,999 
Grand total # of output records including 
headers and trailers  
Literal 38 56 19 A/N GRAND TOTAL TRAILER 
Filler 57 57 1 A/N Space 
AutoRoute File Number 58 65 8 A/N  
AutoRoute File Cycle 66 67 2 A/N  
Filler 68 104 37 A/N Space 

---

## Page 15

Variable Length Record Layouts (Part 3) 
Settling Trade Detail (070); X-[[settlement]] Trade Detail (072); Settling Trade Detail for TPA/Investment Agent/TPP (074) 15 
SETTLING TRADE DETAIL (070); X-[[settlement]] TRADE 
DETAIL (072); SETTLING TRADE DETAIL FOR 
TPA/INVESTMENT AGENT/TPP (074) 
02.23.01 Settling Trade Detail (070) 
Output from [[NSCC]] 
Field Name Start End Len Type Description  
Record Length 1 4 4 N 0197 
Physical Sequence Number 5 6 2 A/N 01 
Logical Sequence Number 7 8 2 A/N 01 
Originator Type 9 9 1 A/N N = [[NSCC]] 
Filler 10 11 2 A/N Space 
Recipient Number 12 15 4 N  
Filler 16 18 3 A/N Space 
Record Type 19 21 3 A/N 070 = Settling Trade Detail 
072 = X-[[settlement]] trade detail 
074 = Settling Trade Detail for 
TPA/Investment Agent/TPP 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
Filler 23 23 1 A/N Space 
Contra [[participant]] Number 24 27 4 N  
Filler 28 30 3 A/N Space 
Security Issue Country 
Code 
31 32 2 A/N Space. For future use 
Security Issue [[ID]] 33 41 9 A/N  
Security Issue Check Digit 42 42 1 A/N Space. For future use 
Security Issue Type  43 44 2 A/N   
Control Number  45 59 15 A/N   

---

## Page 16

Variable Length Record Layouts (Part 3) 
Settling Trade Detail (070); X-[[settlement]] Trade Detail (072); Settling Trade Detail for TPA/Investment Agent/TPP (074) 16 
Field Name Start End Len Type Description  
Correction/Exchange 
Indicator 
60 60 1 A/N A = Exchange From (credit firm, debit fund) 
B = Exchange To (debit firm, credit fund) 
C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction/cancellation 
Y = Post [[settlement]] cancellation Exchange 
From (debit firm, credit, fund) 
Z = Post [[settlement]] cancellation Exchange To 
(credit firm, debit fund) 
P, Y and Z not permitted if the Security Issue 
Type field value is 63 and [[settlement]] Override 
Reason Code field value is space 
Trade Type 61 63 3 A/N ADJ = Cash Adjustment 
CXL = Cancelled [[Underwriting]]/Tender 
RAT = Transfer of Retirement [[Asset]] 
TND = Tender 
UND = [[Underwriting]] 
XCH = Exchange 
Space = None of the above 
[[settlement]] Date 64 71 8 N mmddccyy 
Trade Date 72 79 8 N mmddccyy 
Agent for Firm Number 80 83 4 A/N  
Buy/Sell Code 84 84 1 A/N 2 = Buy (recipient debit) 
4 = Sell (recipient credit) 
Filler 85 87 3 A/N Space 
Recipient Type 88 88 1 A/N B = Firm (Receiving fund if a ToRA item) 
F = Fund (Delivering fund if a ToRA item) 
T = TPA/Investment Agent 
S = Service Provider 
V = TPP (Third Party Provider) 
Firm or TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Firm Number when Recipient Type = T or V. 
Otherwise, TPA/Investment Agent/TPP 
Number 
Service Provider or Firm 
Number 
93 96 4 A/N Firm Number when Recipient Type = S. 
Otherwise, Service Provider Number 
Filler 97 114 18 A/N Space 
*Share Quantity 115 128 14 N 9,999,999,999.9999 

---

## Page 17

Variable Length Record Layouts (Part 3) 
Settling Trade Detail (070); X-[[settlement]] Trade Detail (072); Settling Trade Detail for TPA/Investment Agent/TPP (074) 17 
Field Name Start End Len Type Description  
*Price Per Share 129 140 12 N 999,999.999999 
[[settlement]] Money Amount 141 156 16 N 99,999,999,999,999.99 
Currency Indicator 157 159 3 A/N For record type 070/074: 
USD = Same day [[settlement]] 
USN = Next day [[settlement]] 
EUR or GBP 
For record type 072: 
Any currency code 
[[settlement]] Indicator 160 160 1 A/N A = Automatic [[settlement]] 
F = Fund approved [[settlement]] 
Space = Cash Adjustment  
Contra Exchange Security 
Issue Country Code 
161 162 2 A/N Space. For future use 
Contra Exchange Security 
Issue [[ID]] 
163 171 9 A/N  
Contra Exchange Security 
Issue Check Digit 
172 172 1 A/N Space. For future use 
Filler 173 197 25 A/N Space 
Note: 
For the Exchange To side, values in the Share Quantity and Price Per Share fields reflect the information contained on ‘To’ 
section #1 of the Exchange Confirmation/Reconfirmation/Post [[settlement]] Cancellation transactions (record types 
016/017/021). 

---

## Page 18

Variable Length Record Layouts (Part 3) 
Settling Trade Trailer (071); X-[[settlement]] Trade Trailer (073); Settling Trade Trailer for TPA/Investment Agent/TPP (075) 18 
SETTLING TRADE TRAILER (071); X-[[settlement]] 
TRADE TRAILER (073); SETTLING TRADE TRAILER FOR 
TPA/INVESTMENT AGENT/TPP (075) 
02.24.01 Settling Trade Trailer (071) 
Output from [[NSCC]] 
Field Name  Start End Len Type Description  
Record Length 1 4 4 N 0197 
Physical Sequence Number 5 6 2 A/N 01 
Logical Sequence Number 7 8 2 A/N 01 
Originator Type 9 9 1 A/N N = [[NSCC]] 
Filler 10 11 2 A/N Space 
Recipient Number 12 15 4 N  
Filler 16 18 3 A/N Space 
Record Type 19 21 3 A/N 071 = Settling Trade Trailer 
073 = X-[[settlement]] trade trailer 
075 = Settling Trade Trailer for 
TPA/Investment Agent/ TPP 
Literal 22 36 15 A/N ‘999999999999999’ 
Literal 37 48 12 A/N For record type 071: 
SETT.TRD.TRL 
For record type 073: 
XSETT.TRD.TR 
For record type 075: 
NSETT.TRD.TR 
[[settlement]] Date 49 56 8 N mmddccyy 
Debit Items 57 62 6 N 999,999 
Debit Share Quantity 63 77 15 N 99,999,999,999.9999 
Filler 78 104 27 A/N Space 
Debit Money Amount 105 121 17 N 999,999,999,999,999.99 
Currency Indicator - Debit 122 124 3 A/N For record type 071/075: 
USD = Same day [[settlement]] 

---

## Page 19

Variable Length Record Layouts (Part 3) 
Settling Trade Trailer (071); X-[[settlement]] Trade Trailer (073); Settling Trade Trailer for TPA/Investment Agent/TPP (075) 19 
Field Name  Start End Len Type Description  
USN = Next day [[settlement]] 
EUR or GBP 
For record type 073: 
Any currency code 
Credit Items 125 130 6 N 999,999 
Credit Share Quantity 131 145 15 N 99,999,999,999.9999 
Credit Money Amount 146 162 17 N 999,999,999,999,999.99 
Currency Indicator - Credit 163 165 3 A/N For record type 071/075: 
USD = Same day [[settlement]] 
USN = Next day [[settlement]] 
EUR or GBP 
For record type 073: 
Any currency code 
Filler 166 197 32 A/N Space  

---

## Page 20

Variable Length Record Layouts (Part 3) 
Multiple Reject Codes (120) 20 
MULTIPLE REJECT CODES (120) 
02.25.01 Multiple Reject Codes (120) 
Output from [[NSCC]]. This record will be created by [[NSCC]] for each rejected transaction that has been 
rejected for more than one reason. 
When relating to ToRA (Transfer of Retirement [[Asset]]), Firm means Receiving Fund, and Fund means 
Delivering Fund 
Field Name  Start End Len Type Description  
Record Length 1 4 4 N 0104 
Physical Sequence Number 5 6 2 A/N 01 
Logical Sequence Number 7 8 2 A/N 01 
Originator Type 9 9 1 A/N N = [[NSCC]] 
Filler 10 11 2 A/N Space 
Firm Number 12 15 4 N  
Filler 16 18 3 A/N Space 
Record Type 19 21 3 A/N 120 = Multiple Reject Codes 
Test Indicator 22 22 1 A/N  
Filler 23 23 1 A/N  
Fund Number 24 27 4 N  
Filler 28 30 3 A/N Space 
Security Issue Country 
Code 
31 32 2 A/N  
Security Issue [[ID]] 33 41 9 A/N  
Security Issue Check Digit 42 42 1 A/N  
Security Issue Type  43 44 2 A/N  
Control Number 45 59 15 A/N  
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / cancellation 
Space = No correction 
Original Record Type 61 63 3 A/N The rejected transaction record type 
[[NSCC]] Reject Code 2 64 66 3 A/N  

---

## Page 21

Variable Length Record Layouts (Part 3) 
Multiple Reject Codes (120) 21 
Field Name  Start End Len Type Description  
[[NSCC]] Reject Code 3 67 69 3 A/N  
[[NSCC]] Reject Code 4 70 72 3 A/N  
[[NSCC]] Reject Code 5 73 75 3 A/N  
[[NSCC]] Reject Code 6 76 78 3 A/N  
[[NSCC]] Reject Code 7 79 81 3 A/N  
[[NSCC]] Reject Code 8 82 84 3 A/N  
Filler 85 88 4 A/N Space 
TPA/Investment Agent/TPP 
Number 
89 92 4 A/N  
Service Provider Number 93 96 4 A/N  
Filler 97 104 8 A/N Space 

---

## Page 22

Variable Length Record Layouts (Part 3) 
Data Trak Header 22 
DATA TRAK HEADER 
02.26.01 DataTrak Header Record 1 
This is the first record in any file submitted to Fund/SERV through DataTrak. 
Field Name  Start End Len Type Description  Opt/ 
Req 
Literal 1 1 5 5 A/N HDR.S R 
DataTrak Sysid 6 10 5 A/N System Identifier R 
Literal 2 11 12 2 A/N .E (period, E) R 
Literal 3 13 14 2 A/N ‘00’ R 
Literal 4  15 16 2 A/N .C (period, C) R 
Originator [[ID]] 17 20 4 A/N  R 
Literal 5 21 22 2 A/N .S (period, S) R 
Sub Originator [[ID]] 23 26 4 A/N Submitted by [[Broker]] R 
Submission Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N  R 
Multi Batch Last Batch 
Indicator 
60 60 1 A/N No Multi Batch = Spaces 
N = Multi-Batch, Not last batch 
Y = Multi-Batch, Last batch 
R 
Multi Batch Number 61 63 3 N No Multi-Batch = Spaces 
Multi-Batch = Sequential # starting with 
001 
R 
Filler 64 64 1 A/N Space R 
Variable Length Record 
Indicator 
65 65 1 A/N Variable Length = “*” 
Fixed Length = Space 
R 
Filler 66 100 35 A/N Space R 

---

## Page 23

Variable Length Record Layouts (Part 3) 
Data Trak Trailer 23 
DATA TRAK TRAILER 
02.27.01 DataTrak Trailer Record 1 
This is the last record in any file submitted to Fund/SERV through DataTrak.  
Field Name  Start End Len Type Description  Opt/ 
Req 
Literal 1 1 5 5 A/N END.S R 
DataTrak Sysid 6 10 5 A/N  R 
Literal 2 11 12 2 A/N .E (period, E) R 
Literal 3 13 14 2 A/N ‘00’ R 
Literal 4  15 16 2 A/N .C (period, C) R 
Originator [[ID]] 17 20 4 A/N Submitter R 
Literal 21 22 2 A/N .S (period, S) R 
Sub Originator [[ID]]  23 26 4 A/N Submitted for [[Broker]] R 
Record Count 27 33 7 N 9,999,999 
Optional Field – Total # of records in file 
excluding DataTrak header and trailer 
R 
Filler 34 80 47 A/N Space R 

---

## Page 24

Variable Length Record Layouts (Part 3) 
Firm Exit (139) 24 
FIRM EXIT (139) 
02.28.01 Firm Exit (139) 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0197, 0290 R  
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N A = Investment Agent 
B = Firm 
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 10 11 2 A/N Space R  
Firm Number  12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 139 = Firm Exit R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use  R  
Security Issue Type 43 44 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
OC 150 

---

## Page 25

Variable Length Record Layouts (Part 3) 
Firm Exit (139) 25 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
Control Number 45 59 15 A/N  R 005 
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] cancellation 
Space = No correction 
R 006 
Filler 61 61 1 A/N Space R  
Transaction Code 62 63 2 A/N Required if Correction Indicator = P. 
01 = Initial purchase 
02 = Subsequent purchase 
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
05 = Full exchange 
06 = Partial exchange 
07 = Post settle correct / cancel 
purchase 
08 = Post settle correct / cancel 
[[liquidation]]. 
07 and 08 are allowed only if 
Correction Indicator = P 
OC 018 
Submission Date 64 71 8 N mmddccyy R 101 
Trade Date 72 79 8 N mmddccyy O 037 
Filler 80 84 5 A/N Space R  
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code  
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Required if Originator Type = T or P 
or A or V 
OC 188 

---

## Page 26

Variable Length Record Layouts (Part 3) 
Firm Exit (139) 26 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Service Provider 
Number 
93 96 4 A/N Required if Originator Type = S or P OC 215 
Filler 97 104 8 A/N Space R  
Original Control 
Number 
105 119 15 A/N  O  
Original Correction 
Indicator 
120 120 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / 
cancellation 
Space = No correction 
O 164 
Customer Account 
Number at Firm 
121 140 20 A/N Required if Correction Indicator = P 
and Original Control Number is not 
provided and Original Customer 
Account Number at Fund is not 
provided. 
OC 020 
Customer Account 
Number at Fund 
141 160 20 A/N Required if Correction Indicator = P 
and Original Control Number is not 
provided and Original Customer 
Account Number at Firm is not 
provided.  
OC 011 
Anticipated [[settlement]] 
Date 
161 168 8 A/N Input: Space 
Output: [[settlement]] Date mmddccyy 
R 180 
Standard [[ID]] 169 174 6 A/N  O  
As-Of Reason Code 175 176 2 A/N 01 = Incorrect Firm/Fund Account 
Number 
02 = Incorrect Share Quantity/Dollar 
Quantity 
03 = Incorrect security issue [[ID]] 
04 = Customer renege 
05 = Incorrect Sales Charge 
Breakpoint 
07 = Blue sky violation 
09 = Delay in Firm Trade 
Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV Reject 
12 = DCC&S (see [[Asset]] Type 
Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
R 109 
Filler 177 197 21 A/N Space R  

---

## Page 27

Variable Length Record Layouts (Part 3) 
Firm Exit (139) 27 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original Share 
Quantity 
198 211 14 N 9,999,999,999.9999 
Required if Correction Indicator = P 
and Original Control Number is not 
provided  
OC 019 
Original Money 
Amount 
212 227 16 N 99,999,999,999,999.99 
Required if Correction Indicator = P 
and Original Control Number is not 
provided  
OC 019 
Original Amount Due 228 243 16 N 99,999,999,999,999.99 
Required if Correction Indicator = P 
and Original Control Number is not 
provided 
OC 026 
Memo Field 244 263 20 A/N  O  
Filler 264 290 27 A/N Space R  

---

## Page 28

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 28 
CORRECTION (003); CORRECTION CONFIRMATION 
(025); POST [[settlement]] CORRECTION BY FUND (026) 
02.29.01 Correction (003) 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length 
 
  
1 4 4 N With no SSN/EIN Suffix: 
0290, 0383, 0476, 0569, 0662, 
0755, 0848, 0941, 1034, 1127, 
1220, 1313 
(Must be 0569 or greater for all 
record types except 003) 
 
0662 is required when 
“Redemption Fee Indicator” is 
provided or “[[Asset]] Type Indicator” 
= Q, U, V or W or “Money Market 
[[Liquidity]] Fee / Redemption Gate 
Indicator” is provided. 
 
1313 is required if [[intermediary]] 
Program Indicator, Servicing 
Group, and Additional 
Relationship information is 
provided. 
R 152 
Physical Sequence 
Number 
5 6 2 A/N 01  R 004 
Logical Sequence 
Number 
7 8 2 A/N 01  R 004 
Originator Type 9 9 1 A/N A = Investment Agent 
B = Firm 
F = Fund 
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = Third Party Provider (TPP) 
R 187 
Filler 10 11 2 A/N Space  R  
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space  R  

---

## Page 29

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 29 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Type 19 21 3 A/N 003 = Correction 
025 = Correction Confirmation 
026 = Post [[settlement]] Correction 
by fund 
Record Type 026 not Permitted If 
the Security Issue Type field value 
is 63 and [[settlement]] Override 
Reason Code field value is space  
RC 002/275 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use  R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  
Security Issue Type 43 44 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file 
to determine value and 
associated processing rules. 
Output: [[NSCC]] populates with 
the value in the Fund/SERV 
Security master file. 
OC 150 
Control Number 45 59 15 A/N  R 005 
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / 
cancellation 
Must be P for record type 026 
P not Permitted If the Security 
Issue Type field value is 63 and 
[[settlement]] Override Reason Code 
field value is space 
RC 006 

---

## Page 30

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 30 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Transaction Type 61 61 1 A/N 0 = Single purchase 
1 = Letter of intent 
2 = Rights of accumulation 
3 = Net [[Asset]] value 
4 = Group purchase 
5 = CDSC [[liquidation]] 
8 = 529 [[participant]] Distribution 
9 = 529 Beneficiary Distribution 
A = 529 School Distribution 
B = 529 Rollover Distribution 
E = 529 In-State Plan Transfer 
Distribution 
F = 529 Registration Change 
 
Only 5, 8, 9, A, B, E or F are 
allowed if Transaction Code = “03” 
or “04” 
03 (Partial [[liquidation]]) 
04 (Full [[liquidation]]) 
R 017 
Transaction Code 
 
 
62 63 2 A/N 01 = Initial purchase 
02 = Subsequent purchase 
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
07 = Post settle correct/cancel 
purchase 
08 = Post settle correct/cancel 
[[liquidation]]. 
Must be 03 or 04 or 08 if 
Transaction Type = 5. 
07 and 08 allowed only if 
Correction Indicator = P. 
07 and 08 not permitted if the 
Security Issue Type field value is 
63 and [[settlement]] Override 
Reason Code field value is space. 
 
For record type 003, 025 
For Security Type = 48 (Interval 
Fund) future dated orders, only 03 
and 04 are allowed. 
RC 018 
Submission Date 64 71 8 N mmddccyy R 101 

---

## Page 31

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 31 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Trade Date 
 
 
72 79 8 N mmddccyy 
 
For record type 003, 025 
Future trade date is allowed if 
Security Type = 48 (Interval Fund) 
and Transaction Code = 03 (Partial 
[[liquidation]]) or 04 (Full 
[[liquidation]]). 
 
Best Practice: 
Trade Date for future dated Interval 
Fund repurchase orders should be 
populated with the Repurchase 
Pricing Date communicated by the 
Fund. 
R 016 
Book/Physical Share 
Indicator 
80 80 1 A/N 0 = Book [[shares]] - firm name 
1 = Book [[shares]] - customer name 
2 = Physical [[shares]] 
3 = Both book and physical [[shares]] 
Must be 0 or 1 for Money Market 
trades 
R 015 
PI Delivery Indicator 81 81 1 A/N Required for all purchases if 
Book/Physical Share Ind = 2. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm  
OC 039 Filler 82 82 1 A/N Space R  
[[settlement]] Override 
Reason Code 
83 84 2 A/N Required (but must not be 04) if 
Anticipated [[settlement]] Date is 
provided. 
01 = Wrap fee account 
02 = 401K 
03 = Other 
04 = X-[[settlement]] 
05 = Section 529 Account - 
Qualified State Tuition Program 
06 = X-[[settlement]] offshore 
enhanced (allowed for Security 
Types 62 and 63 only) 
07 = Refer to [[Asset]] Type Indicator 
Must be space for settling EUR 
and GBP transactions (Security 
Issue Type 63 only). 
OC 179 

---

## Page 32

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 32 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors  
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Required if: 
Originator Type = (T or P or A or V) 
OR  
Membership Identifier = 02 or 03. 
 
If Originator Type = T or P, then 
[[Asset]] Type Indicator must be F 
through O or S or T (indicating 
DCC&S) 
OC 188 
Service Provider Number 93 96 4 A/N Required if Originator Type = S or 
P 
OC 215 
SSN/EIN Start Section 
Number 
97 98 2 A/N See SSN/EIN Start Section 
Number in the Introduction section. 
Required if SSN/EIN records are 
provided. Not allowed otherwise.  
OC 257 
Total SSN/EIN Sections 99 100 2 N Required if SSN/EIN records are 
provided. Not allowed otherwise.  
OC 258 
Filler 101 104 4 A/N Space R  
Share Quantity 105 118 14 N 9,999,999,999.9999 
Optional for record type 003 if full 
[[liquidation]] or if Money Amount > 0  
R 019 
Customer Account 
Number at Firm 
119 138 20 A/N Optional if [[settlement]] Override 
Reason Code = 04 or 06 OR 
Membership Identifier is provided. 
RC 020 
Fund Account Indicator 139 139 1 A/N 0 = New account – U.S. 
1 = New account – non-U.S. 
2 = Existing account – U.S. 
3 = Existing account – non-U.S. 
4 = New account – US Tax 
Resident Living Abroad 
5 = Existing account – US Tax 
Resident Living Abroad 
R 010 

---

## Page 33

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 33 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Customer Account 
Number at Fund 
140 159 20 A/N Required for all non-networked 
liquidations (Network Control Ind = 
0 and Trans Code = 03, 04 or 08) 
OC 011 

---

## Page 34

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 34 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[Asset]] Type Indicator 160 160 1 A/N 0 = Not applicable 
1 = Current year payment 
2 = Prior year payment 
3 = IRA rollover 
4 = [[Asset]] transfer 
5 = Employee - prior year 
6 = Employee - current year 
7 = Employer - prior year 
8 = Employer - current year 
9 = Non-fund prototype IRA 
A = Non-fund qualified plan 
C = Salary Reduction Contribution 
D = 529 Current Year Contribution 
E = UGMA account transferred to 
Section 529 Account 
F = 529 Underlying Fund Trades 
G = Share Class Conversion 
H = Health Savings Account 
I = Insurance Fund Transactions 
J = Non-Qualified Retirement Plan 
K = Qualified Retirement Plan 
L = Omnibus [[Dividend]] 
Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year 
Contribution 
Q = 529 Rollover Contribution 
S = Omnibus Short-Term Capital 
Gain Reconciliation 
T = Omnibus Long-Term Capital 
Gain Reconciliation 
U = 529 In–State Plan Transfer 
Contribution 
V = 529 Owner Change 
W = 529 Beneficiary Change-In-
Family 
Note: 
D, P, Q, U, V and W indicate 
Section 529 Plan. 
R 013 

---

## Page 35

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 35 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Agent for Firm 161 164 4 A/N Required if Originator Type = V 
(TPP) 
OC 271 
Network Control 
Indicator  
165 165 1 A/N 0 = Non-networked 
3 = Matrix level 3 
4 = Matrix level 4 
R 047 
Fraction Indicator 166 166 1 A/N 0 = Round up 
1 = Round down 
2 = Issue fraction 
3 = Not applicable 
R 014 
Gross [[settlement]] 
Indicator 
167 167 1 A/N 0 = Not applicable 
1 = Settle net 
2 = Settle gross 
R 094 
Transaction Received 
Time 
168 173 6 N hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market 
[[Liquidity]] Fee / Redemption Gate 
Indicator” = ‘F’ (Fund). 
 
Record Type 025: 
Must contain the same value as 
provided by the firm on the 
Correction transaction (record type 
003). [[NSCC]] will reject if a fund 
provided value is different from the 
value submitted by the firm. 
OC 168 
Membership Identifier 174 175 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 176 176 1 A/N  R  
Transaction Payment 
Type Indicator 
177 177 1 A/N 
 
Required if [[settlement]] Override 
Reason Code = 04. 
1 = Shareholder wire 
2 = Shareholder ACH 
3 = Address of Record (AOR). 
3 allowed for [[liquidation]] 
(Transaction Code = 03 or 04) only 
O 216 
Transaction Bank 
Account Number 
178 197 20 A/N Required if Transaction Payment 
Type Indicator = 1 or 2 
OC 142 

---

## Page 36

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 36 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Money Amount 198 213 16 N 99,999,999,999,999.99 
Optional for record type 003 if full 
[[liquidation]] or if Share Quantity > 0 
R 019 
Currency Indicator 214 216 3 A/N  O 110 
Anticipated [[settlement]] 
Date 
 
 
217 224 8 A/N mmddccyy 
For Security Issue Type = 63, 
Required if [[settlement]] Override 
Reason Code is space 
For other Security Types: 
1. Required if [[settlement]] 
Override Reason Code is 
provided and is not 04 or 06 
(x-[[settlement]] domestic). 
2. Not allowed if [[settlement]] 
Override Reason Code = 04. 
 
For record type 003 
This field should not be populated 
when Security Type = 48, and 
Transaction Code = 03 (Partial 
[[liquidation]]) or 04 (Full 
[[liquidation]]). If populated, [[NSCC]] 
will [[default]] the value to 12319999 
and pass the order to the Fund. 
OC 180 
Branch Identification 
Number 
225 233 9 A/N Optional under the following 
conditions: 
• Membership Identifier = 01 or 
02 and Agent for Firm Number 
is not provided. 
• Originator Type = V(TPP) 
RC 035 
Related Trade Indicator 234 234 1 A/N 0 = No 
1 = Yes  
R 065 
Related Trade Identifier 235 236 2 A/N Required if Related Trade Indicator 
= 1 
OC 105 
Customer Name 237 256 20 A/N  R 063 
SSN/EIN Indicator 257 257 1 A/N 0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN  
R 102 
SSN/EIN Number 258 266 9 A/N   R 103 

---

## Page 37

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 37 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[liquidation]] Indicator 267 267 1 A/N Required if Trans Type = 5. 
1 = Gross 
2 = Net 
4 = Correction 
5 = Death 
6 = Disability 
7 = Mandatory distribution 
8 = Systematic withdrawal 
9 = Defined contribution 
A = Hardship 
B = No commission paid 
C = 529 Plan-Specific 
D = 529 Plan Account - Beneficiary 
Disability 
E = 529 Plan Account – 
Beneficiary Death 
F = 529 Plan Account – Beneficiary 
Scholarship 
Notes: 
• 4 through F should apply only 
to transactions with CDSC 
Waivers 
• C through F should only apply 
to Section 529 plans. 
OC 046 

---

## Page 38

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 38 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
NAV Reason Code 268 268 1 A/N Required if Trans Type = 3. 
0 = Other 
1 = Net [[Asset]] value transfer 
2 = Repurchase 
3 = Employee 
4 = Error correction 
5 = Wrap fee account 
6 = NAV commissionable 
7 = Commissionable defined 
contribution plan 
8 = Non-commissionable defined 
contribution plan 
9 = Section 529 Account - 
Qualified State Tuition Program 
A = [[Dividend]] reinvestment trade 
B = Trust Company NAV per 
Agreement 
C = Refer to [[Asset]] Type Indicator 
D = Deminimis Amount Processed 
at NAV 
E = Self Directed Brokerage 
Account 
OC 104 
State of Sale (State 
Code) 
269 270 2 A/N Required for Transaction Codes 
 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 012 
Redemption Fee 
Indicator 
271 271 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee 
3 = Money Market [[Liquidity]] Fee 
with CDSC 
 
Values “0” and “1” are not allowed 
for record type 025 if this field was 
blank on the original Correction 
transaction (record type 003). 
 
Values “2” and “3” are allowed for 
record type 025 if this field was 
blank on the original Correction 
transaction (record type 003). 
O 248 

---

## Page 39

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 39 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Short-Term Redemption 
Fee Waiver Indicator 
272 272 1 A/N 1 = STR waiver due to correction 
2 = Death 
3 = Disability 
4 = Mandatory distribution 
5 = Systematic withdrawal 
6 = Defined contribution 
7 = Hardship 
8 = Auto Rebalance 
9 = DC – Termination Distribution 
A = DC – Involuntary Distribution 
B = DC – Forfeitures 
C = DC – Loans 
D = DC – Excess Contributions 
E = Wrap Program 
F = Fund of Funds 
G = Divorce / QDRO 
H = Plan fees QDRO 
O 249 
Filler 273 273 1 A/N Space  R  
Correction Type 
Indicator 
274 274 1 A/N 0 = Not applicable 
1 = Correction only 
2 = Correction 
3 = Rebill  
O 108 

---

## Page 40

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 40 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Correction Reason Code 275 276 2 A/N 01 = Incorrect Firm/Fund Account 
Number 
02 = Incorrect Share 
Quantity/Dollar Quantity 
03 = Incorrect security issue [[ID]] 
04 = Customer renege 
05 = Incorrect Sales Charge 
Breakpoint 
07 = Blue sky violation 
09 = Delay in Firm Trade 
Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV 
Reject 
12 = DCC&S (see [[Asset]] Type 
Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
Note: 
The values ‘00’, ‘06’ and ‘08’ have 
been removed. 
R 109 
Transaction ABA 
Routing Number 
277 285 9 A/N Required if Transaction Payment 
Type Indicator = 1 or 2  
OC 141 
De-minimis repurchase 
waiver code 
 
 
286 286 1 A/N ‘blank’ or 0 = No; 
1 = Yes” 
 
Allows Firms to indicate if an 
Interval Fund repurchase order is 
eligible for de-minimis treatment in 
accordance with the Fund’s 
prospectus. 
 
Should only be populated for an 
Interval Fund in record type 003. 
O  
Filler 
 
287 288 2 A/N Space  R  

---

## Page 41

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 41 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Omnibus Account 
Indicator 
289 289 1 A/N 0 = Not Omnibus Account 
1 = Omnibus Account 
2 = Omnibus B to A Conversion 
Purchase 
3 = Omnibus B to A Conversion 
Redemption 
4 = Omnibus Cash [[Dividend]] 
Redemption 
5 = Omnibus Reinvest [[Dividend]] 
Purchase 
6 = Omnibus Cash Capital Gain 
Redemption 
7 = Omnibus Reinvest Capital Gain 
Purchase 
O 234 
Trade Date Forward 
Indicator 
290 290 1 A/N 0 = Trade Date not forwarded 
1 = Trade Date forwarded 
2 = Trade Date being corrected 
For record type 003: 
a. Must be 2 if Trade Date is not 
equal to Trade Date on order. 
b. Must be 1 if Trade Date equals 
Trade Date on order and Trade 
Date on order is forwarded. 
c. Must be 0 if Trade Date equals 
Trade Date on order and Trade 
Date on order is not forwarded. 
 
Trade Date forwarded is only 
allowed if: 
• Security Type = 48 (Interval 
Fund) and Transaction Code = 
03 (Partial [[liquidation]]) or 04 
(Full [[liquidation]]). 
• Security Type = 62 or 63 
 
For record type 025: 
Must be same as on record 003. 
OC 229 
Related Account 
Number 
291 310 20 A/N  O  
Related Account 
Number Indicator 
311 311 1 A/N Required if Related Account 
Number is provided. 
1 = Fund 
2 = Firm 
3 = Customer 
OC 157 

---

## Page 42

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 42 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Related Account 
Security Issue Country 
Code 
312 313 2 A/N Space. For future use R  
Related Account 
Security Issue [[ID]] 
314 322 9 A/N Required if Related Account 
Number is provided 
OC 107 
Related Account 
Security Issue Check 
Digit 
323 323 1 A/N Space. For future use R  
Country of Origin 
(Country Code) 
324 325 2 A/N 
Required for non-omnibus account 
(Omnibus Account Indicator = ‘0’ or 
space) if State of Sale (State 
Code) = ‘FF’ 
OC 067 
Sales Charge Rate 326 329 4 N 9.999 
Must be provided (but allowed to 
be zero) for purchase (Transaction 
Code = '01', '02' or '07') if Load 
Type Indicator = 1. 
OC 025 
ROA/LOI Value 330 345 16 N 99,999,999,999,999.99  O 064 
LOI Number/Date 346 353 8 A/N  O  

---

## Page 43

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 43 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
IRA/529 [[liquidation]] 
Indicator 
354 354 1 A/N 0 = Not applicable 
1 = Distribution – premature 
2 = Distribution – disability 
3 = Distribution – death 
4 = Distribution – normal 
5 = Hardship withdrawal 
6 = Loan 
7 = Rollover 
8 = Adjust prior year excess 
9 = Adjust current year excess 
A = Qualified 
B = Non-Qualified 
C = Distribution – Non-Taxable 
D = 529 Owner Change 
E = 529 Beneficiary Change – In-
Family 
Notes: 
A and B are required if Transaction 
Type = 
8 = (529 [[participant]] Distribution) 
9 = (529 Beneficiary Distribution) 
A = (529 School Distribution 
B = (529 Roll Over Distribution) 
C is required if Transaction Type = 
E (529 In-State Plan Transfer 
Distribution) 
D or E is required if Transaction 
Type = F (529 Registration 
Change) 
OC 106 
Short [[settlement]] 
Indicator 
355 355 1 A/N 0 = Not applicable 
1 = Short due to correction 
O 169 

---

## Page 44

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 44 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Periodic Frequency 
Indicator 
356 356 1 A/N Required if [[liquidation]] Indicator = 
8 or Program Transaction Indicator 
= 1. 
0 = Weekly 
1 = Monthly 
2 = Bi-monthly 
3 = Quarterly 
4 = Semiannual 
5 = Annual 
6 = Non-Periodic (Ad Hoc) 
OC 083 
Shareholder Date of 
Birth 
357 364 8 N mmddccyy 
For 529 use this field for 
Beneficiary Date of Birth 
O 204 
Social Code 365 366 2 A/N Required when “Transaction 
Code” = 01 – Initial Purchase 
 
See Social Code List at 
https://dtcclearning.com/document
s/mutual-fund-services-1/mfs-
cross-product/codes-8/2498-social-
codes/file.html under General 
Codes. 
OC 128 
Beneficiary SSN/EIN 
Number 
367 375 9 A/N Required if [[Asset]] Type Indicator = 
D, E, P, Q, U, V or W and 
Transaction Code = 01 or 02 
 
[[Asset]] Type Indicators 
D (529 Current Year Contribution) 
E (UGMA account transferred to 
Section 529 Account) 
P (529 Previous Year Contribution) 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-
Family) 
 
Transaction Codes 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 103 

---

## Page 45

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 45 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Beneficiary SSN/EIN 
Indicator 
376 376 1 A/N 
 
Required if Beneficiary SSN/EIN 
Number is provided. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = Beneficiary TIN/EIN 
OC 102 
Standard [[ID]] 377 382 6 A/N  O  
Program Transaction 
Indicator 
383 383 1 A/N 1 = Systematic Withdrawal Plan 
(SWP) 
2 = Target Date Fund [[liquidation]] 
3 = Systematic Contribution 
(SIP/PAC/PIP) 
4 = Rebalance Purchase 
(Systematic) 
5 = Rebalance Redemption 
(Systematic) 
O 259 
Account Representative 
Number 
384 392 9 A/N  O  
Account Representative 
Name 
393 407 15 A/N  O  
Confirm Number 408 419 12 A/N  O  
Filler 420 431 12 A/N Space R  
IRA Withholding 
Percentage 
432 436 5 N 99.999  O 158 
Non-Taxable Percentage 437 441 5 N 99.999  O 159 
Non-Taxable Money 
Amount 
442 457 16 N 99,999,999,999,999.99  O 160 
Closeout Fee Indicator  458 458 1 A/N 0 = [[DO]] not deduct 
1 = Deduct  
O 161 
LOI Indicator 459 459 1 A/N 0 = New 
1 = Existing 
O 162 
Original Control Number 460 474 15 A/N  O  

---

## Page 46

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 46 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original Correction 
Indicator 
475 475 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / 
cancellation 
Space = No correction 
P not permitted if the Security 
Issue Type field value is 63 and 
[[settlement]] Override Reason Code 
field value is space. 
O 164 
Filler 476 476 1 A/N Space  R  
Withholding Amount 477 492 16 N 99,999,999,999,999.99  O 113 
Withholding Type 493 493 1 A/N Required if Withholding Amount > 
0. 
1 = Tefra backup 
2 = Tefra pension 
3 = Foreign withholding 
OC 114 Fee Amount 494 501 8 N 999,999.99  O 115 
Fee Type 502 502 1 A/N Required if Fee Amount > 0. 
1 = [[liquidation]] fee 
2 = Other 
OC 116 
Amount Due 503 518 16 N 99,999,999,999,999.99 
Optional for record type 003. 
This amount will be settled by 
[[NSCC]] 
RC 026 
Price Per Share 519 530 12 N 999999.999999 
Optional for record type 003  
RC 027 
Loss/Gain Amount 531 538 8 N 999,999.99 O 031 
Loss/Gain Indicator 539 539 1 A/N Required if Loss/Gain Amount > 0. 
0 = Loss 
1 = Gain 
OC 117 
Firm Concession 540 548 9 N 9,999,999.99 O 044 
Accrual Amount 549 564 16 N 99,999,999,999,999.99 O 111 
Accrual Indicator 565 565 1 A/N Required if Accrual Amount > 0. 
0 = Included in Amount Due 
1 = Paid via Cash Adjustment 
2 = Paid outside system 
OC 112 

---

## Page 47

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 47 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Debit/Credit Indicator 566 567 2 A/N Required for record type 026. 
Required for record type 025 if 
Correction Indicator = P. 
Not allowed otherwise. 
DB = Debit firm 
CR = Credit firm 
NS = No [[settlement]] (Amount Due 
must be zero) 
[[NSCC]] will settle Amount Due 
according to this indicator rather 
than Transaction Code. 
OC 034 
Breakpoint Change 
Reason Code  
568 568 1 A/N 1 = ROA value at fund 
2 = LOI at fund 
3 = The higher of cost or market 
value at fund 
4 = Jumbo Pricing 
5 = Wrap Account 
6 = NAV Account 
7 = Amount Processed at NAV  
O 246 
Load Type Indicator  569 569 1 A/N 0 = Other 
1 = Front-End Load 
Required for record types 025 and 
026 if purchase (Transaction Code 
= ‘01’, ‘02’ or ’07’). 
OC 247 
Redemption Fee Rate 570 576 7 N 99.99999 
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with 2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
 
Zero value is not allowed when this 
field is required and “Redemption 
Fee Indicator” = 2 or 3. 
 
If “Redemption Fee Indicator” = 0 
or 1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Rate 
OC 250 

---

## Page 48

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 48 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
STR Fee Share Quantity 577 590 14 N 9,999,999,999.9999 
 
For all record types: 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record type 003: 
Required when “Redemption Fee 
Indicator” is provided and 
“Redemption Fee Money Amount” 
= 0 or Space. 
 
For record type 025: 
If zero or Space, and “Redemption 
Fee Indicator” is provided, will not 
override the “STR Fee Share 
Quantity” in the database. 
 
For all record types: 
Not allowed when “Redemption 
Fee Indicator” is populated with 
either ‘2’ (Money Market [[Liquidity]] 
Fee) or ‘3’ (Money Market [[Liquidity]] 
Fee with CDSC). 
OC 251 

---

## Page 49

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 49 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Redemption Fee Money 
Amount  
591 606 16 N 99,999,999,999,999.99 
 
For all record types: 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record type 003: 
Required when “Redemption Fee 
Indicator” is provided and “STR 
Fee Share Quantity” = 0 or Space. 
 
For record type 025: 
Required when “Redemption Fee 
Indicator “is provided. 
 
For all record types: 
Required when “Redemption Fee 
Indicator” is populated with either 
‘2’ (Money Market [[Liquidity]] Fee) or 
‘3’ (Money Market [[Liquidity]] Fee 
with CDSC). 
Zero value is not allowed when this 
field is required. 
 
If “Redemption Fee Indicator” = 0 
or 1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Money 
Amount. 
OC 252 
Cost Basis Money 
Amount 
607 622 16 N Required if the [[Asset]] Type 
Indicator = Q, U, V or W. 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-
Family) 
Format: 
99,999,999,999,999.99 
Zeros are allowed 
OC 261 

---

## Page 50

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 50 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Earnings to Date Money 
Amount 
623 638 16 N Required if the [[Asset]] Type 
Indicator = Q, U, V or W. 
Q (529 Rollover Contribution) 
U (529 In–State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change- 
In-Family) 
Format: 
99,999,999,999,999.99 
Zeros are allowed 
OC 262 
Negative Earnings to 
Date Indicator 
639 639 1 A/N N = Negative 
Spaces = Positive 
O 263 
Money Market [[Liquidity]] 
Fee / Redemption Gate 
Indicator 
640 640 1 A/N F = Fund. 
B = [[intermediary]] 
 
For record type 025: 
Must contain the same value as 
provided on the Correction 
transaction (record type 003). 
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
O 282 
Transaction Received 
Date  
641 648 8 A/N mmddccyy 
 
Required if the “Money Market 
[[Liquidity]] Fee / Redemption Gate 
Indicator” = F. 
 
For record Type 025: 
Must contain the same value as 
provided on the Correction 
transaction (record type 003). 
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
OC 283 

---

## Page 51

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 51 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Aggregated Order 
Indicator  
649 649 1 A/N Required if the “Money Market 
[[Liquidity]] Fee / Redemption Gate 
Indicator” = “F” or “B”. 
• 1 = Transactions are not 
aggregated 
• 2 = Transactions are 
aggregated by “like” orders 
(purchases separate from 
redemptions) 
• 3 = Transactions are net of 
purchases and redemptions 
• 4 = Unknown at time of 
placement 
 
For record type 025: 
Must contain the same value as 
provided on the Correction 
transaction (record type 003). 
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
OC 284 
Filler 650 662 13 A/N Space R  
Original Customer 
Account Number at Firm 
663 682 20 A/N Required if all the following occur: 
• Correction Indicator = P 
• Original Control Number is not 
provided 
• Original Customer Account 
Number at Fund is not provided  
OC 020 
Original Customer 
Account Number at Fund 
683 702 20 A/N Required if all the following occur: 
• Correction Indicator = P 
• Original Control Number is not 
provided 
• Original Customer Account 
Number at Firm is not provided 
OC 011 Memo Field 703 722 20 A/N  O  
Filler 723 755 33 A/N Space  R  
Original Share Quantity 756 769 14 N 9,999,999,999.9999 
Required if Correction Indicator = 
'P' and Original Control Number is 
not provided 
OC 019 
Original Money Amount 770 785 16 N 99,999,999,999,999.99 
Required if Correction Indicator = P 
and Original Control Number is not 
provided 
OC 019 

---

## Page 52

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 52 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original Amount Due 786 801 16 N 99,999,999,999,999.99 
Required if Correction Indicator = P 
and Original Control Number is not 
provided 
OC 026 
Original Price Per Share 802 813 12 N 999,999.999999 
Required if Correction Indicator = P 
and Original Control Number is not 
provided 
OC 027 
Filler 814 848 35 A/N Space R  
Original Transaction 
Type 
849 849 1 A/N  O 017 
Original Transaction 
Code 
850 851 2 A/N  O 018 
Original Book/Physical 
Share Indicator 
852 852 1 A/N  O 015 
Original PI Delivery 
Indicator 
853 853 1 A/N  O 039 
Original [[settlement]] 
Override Reason Code 
854 855 2 A/N  O 179 
Original Fund Account 
Indicator 
856 856 1 A/N  O 010 
Original [[Asset]] Type 
Indicator 
857 857 1 A/N  O 013 
Original Agent for Firm 
Number 
858 861 4 A/N  O  
Original Network Control 
Indicator 
862 862 1 A/N  O 047 
Original Fraction 
Indicator 
863 863 1 A/N  O 014 
Original Gross 
[[settlement]] Indicator  
864 864 1 A/N  O 094 
Original Membership 
Identifier 
865 866 2 A/N  O 181 
Original [[settlement]] Date 867 874 8 A/N mmddccyy  O 180 
Original Branch 
Identification Number  
875 883 9 A/N  O 035 
Original Related Trade 
Indicator 
884 884 1 A/N  O 065 

---

## Page 53

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 53 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original Related Trade 
Identifier 
885 886 2 A/N  O 105 
Original Customer Name 887 906 20 A/N  O 063 
Original SSN/EIN 
Indicator 
907 907 1 A/N  O 102 
Original SSN/EIN 
Number 
908 916 9 A/N  O 103 
Original [[liquidation]] 
Indicator 
917 917 1 A/N  O 046 
Original NAV Reason 
Code 
918 918 1 A/N  O 104 
Original State of Sale 
(State Code) 
919 920 2 A/N  O 012 
Original Correction Type 
Indicator 
921 921 1 A/N  O 108 
Original Extended 
Correction Reason Code 
922 923 2 A/N  O 109 
Filler 924 941 18 A/N Space  R  
Original Related Account 
Number 
942 961 20 A/N  O  
Original Related Account 
Number Indicator 
962 962 1 A/N  O 157 
Original Related Account 
Security Issue Country 
Code 
963 964 2 A/N  O  
Original Related Account 
Security Issue [[ID]] 
965 973 9 A/N  O 107 
Original Related Account 
Security Issue Check 
Digit 
974 974 1 A/N  O  
Original Country of 
Origin (Country Code) 
975 976 2 A/N  O  
Original Sales Charge 
Rate 
977 980 4 N 9.999 O 025 
Original ROA/LOI Value 981 996 16 N 99,999,999,999,999.99 O 064 
Original LOI 
Number/Date 
997 1004 8 A/N  O  

---

## Page 54

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 54 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original IRA/529 
[[liquidation]] Indicator 
1005 1005 1 A/N  O 106 
Original Short [[settlement]] 
Indicator 
1006 1006 1 A/N  O 169 
Original Periodic 
Frequency Indicator 
1007 1007 1 A/N  O 083 
Filler 1008 1034 27 A/N Space R  
Original Account 
Representative Number 
1035 1043 9 A/N  O  
Original Account 
Representative Name 
1044 1058 15 A/N  O  
Original Confirm Number 1059 1070 12 A/N  O  
Original IRA Withholding 
Percentage  
1071 1075 5 N 99.999  O 158 
Original Non-Taxable 
Percentage 
1076 1080 5 N 99.999 
 
O 159 
Original Non-Taxable 
Money Amount 
1081 1096 16 N 99,999,999,999,999.99 
 
O 160 
Original Closeout Fee 
Indicator 
1097 1097 1 A/N  O 161 
Original LOI Indicator 1098 1098 1 A/N  O 162 
Filler 1099 1127 29 A/N Space R  
Original Withholding 
Amount 
1128 1143 16 N 99,999,999,999,999.99 O 113 
Original Withholding 
Type 
1144 1144 1 A/N  O 114 
Original Fee Amount 1145 1152 8 N 999,999.99 O 115 
Original Fee Type 1153 1153 1 A/N  O 116 
Original Loss/Gain 
Amount 
1154 1161 8 N 999,999.99 O 031 
Original Loss/Gain 
Indicator 
1162 1162 1 A/N  O 117 
Original Firm 
Concession 
1163 1171 9 N 9,999,999.99 
 
O 044 

---

## Page 55

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 55 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original Accrual Amount 1172 1187 16 N 99,999,999,999,999.99 
 
O 111 
Original Accrual Indicator 1188 1188 1 A/N  O 112 
Filler 1189 1220 32 A/N Space R  
[[intermediary]] Program  
Indicator – 1 
 
 
1221 1224 4 A/N Indicates the program, platform, or 
channel applicable to an account. 
 
Examples may include: 
• Program indicator for advisory 
accounts 
• Distribution channel applicable 
to the account (e.g., retail, RIA, 
etc.) 
• Retirement platform pertaining 
to the account 
Values are uniquely defined by 
each [[intermediary]]. 
O  
[[intermediary]] Program  
Indicator – 2 
 
 
1225 1228 4 A/N Further defines the program, 
platform, or channel applicable to 
an account. 
 
Values are uniquely defined by 
each [[intermediary]]. 
O  
Servicing Group [[ID]] 
 
 
1229 1237 9 A/N This field is used to communicate 
aggregated servicing relationships 
or define additional relationships 
on accounts. 
 
Examples may include: 
• Consolidating (Super) 
Branches 
• Third-party administrators 
(TPAs) 
• Investment Advisers 
• Consultants 
This field does not replace the 
main branch field on the account. 
 
Values are uniquely defined by 
each [[intermediary]]. 
O  

---

## Page 56

Variable Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 56 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Additional Relationship 
[[ID]] – 1 
 
 
1238 1257 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing 
relationships between accounts. 
 
Values are uniquely defined by 
each [[intermediary]]. 
O  
Additional Relationship 
[[ID]] – 2 
 
 
1258 1277 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing 
relationships between accounts. 
 
Values are uniquely defined by 
each [[intermediary]]. 
O  
Filler 
 
1278 1313 36 A/N Space R  

---

## Page 57

Variable Length Record Layouts (Part 3) 
SSN/EIN Suffix 57 
SSN/EIN SUFFIX 
02.30.01 SSN/EIN SUFFIX 
Rules: 
 
1. This suffix contains a list of SSN/EIN Numbers and SSN/EIN Indicators. 
2. The suffix (as its name suggests) can be submitted only as a suffix to a submitted record type as Order 
(001), As-Of order (004), etc. It cannot be submitted independently. 
3. The suffix is comprised of sections. Each section is 93 byte long. 
4. Each section in the suffix, except the last one, must contain 9 SSN/EIN Numbers and Indicators. 
5. The last SSN/EIN section of the suffix can contain less than 9 SSN/EIN numbers and indicators, but they 
must be presented in a row without Space in between. The section must still be 93 byte long, with Space 
from the last SSN/EIN number to the end of the section. 
Example: 
To submit 12 SSN/EIN numbers and indicators, the suffix should contain two sections as follows: 
• The first section must have 9 SSN/EIN numbers and indicators 
• The second section must have SSN/EIN numbers and indicators 1, 2 and 3. The rest of this section must be 
Space. 
6. Up to 11 sections are allowed in one suffix (up to 99 SSN/EIN Numbers and Indicators).  
7. The Start and End positions of each field in the suffix depends on the position at which the suffixed item 
ends (before the suffix starts). 
Note: 
The E in the layout below represents the following: 
a. For the first SSN/EIN section, the position of the last byte of the suffixed item (before the suffix starts). 
b. For any other SSN/EIN section, the position of the last byte of the previous section 
 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
SSN/EIN Indicator 1 E+1 E+1 1 A/N Required if SSN/EIN Number 1 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 1 E+2 E+10 9 A/N  O 103 
SSN/EIN Indicator 2 E+11 E+11 1 A/N Required if SSN/EIN Number 2 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 2 E+12 E+20 9 A/N  O 103 

---

## Page 58

Variable Length Record Layouts (Part 3) 
SSN/EIN Suffix 58 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
SSN/EIN Indicator 3 E+21 E+21 1 A/N Required if SSN/EIN Number 3 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 3 E+22 E+30 9 A/N  O 103 
SSN/EIN Indicator 4 E+31 E+31 1 A/N Required if SSN/EIN Number 4 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 4 E+32 E+40 9 A/N  O 103 
SSN/EIN Indicator 5 E+41 E+41 1 A/N Required if SSN/EIN Number 5 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 5 E+42 E+50 9 A/N  O 103 
SSN/EIN Indicator 6 E+51 E+51 1 A/N Required if SSN/EIN Number 6 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 6 E+52 E+60 9 A/N  O 103 
SSN/EIN Indicator 7 E+61 E+61 1 A/N Required if SSN/EIN Number 7 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 7 E+62 E+70 9 A/N  O 103 
SSN/EIN Indicator 8 E+71 E+71 1 A/N Required if SSN/EIN Number 8 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 8 E+72 E+80 9 A/N  O 103 
SSN/EIN Indicator 9 E+81 E+81 1 A/N Required if SSN/EIN Number 9 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 9 E+82 E+90 9 A/N  O 103 
Invalid Field Indicator E+91 E+91 1 A/N Input: Space 
Output: Indicates whether a field in 
R  

---

## Page 59

Variable Length Record Layouts (Part 3) 
SSN/EIN Suffix 59 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
this section is invalid, when the record 
is rejected by [[NSCC]]. 
0 = All fields are valid 
1 = SSN/EIN Indicator invalid 
2 = SSN/EIN Number invalid 
Space = Suffix not verified (may 
happen when the suffixed item is 
rejected for other reasons)  
Invalid Field Number E+92 E+92 1 A/N Input: Space 
Output: Indicates which field in this 
section is invalid, when the record is 
rejected by [[NSCC]]. 
0 = All fields in this section are valid 
1-9 = Invalid field number in this 
section 
Space = Suffix not verified (may 
happen when the suffixed item is 
rejected for other reasons) 
R  
Filler E+93 E+93 1 A/N Space R  

---

## Page 60

Variable Length Record Layouts (Part 3) 
Interval Fund Acknowledgement (030) 60 
INTERVAL FUND ACKNOWLEDGEMENT (030) 
02.31.01 Acknowledgement (030) 
 
This Record is optional and only allowed for acknowledging an Order (001) or Correction (003) when: 
Security Type = 48 (Interval Fund) AND Transaction Type = ‘03 - Partial [[liquidation]]’ or ’04 – Full 
[[liquidation]]’. 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0197 R  
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N F = Fund R 187 
Filler 10 11 2 A/N Space R  
Firm Number  12 15 4 N [[NSCC]] will reject if value does not 
match Order (001) or Correction 
(003). 
R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 030 = Interval Fund Acknowledgment R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Fund Number 24 27 4 N If populated must match value on 
Order (001) or Correction (003). 
O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N [[NSCC]] will reject if value does not 
match Order (001), or Correction 
(003). 
R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use  R  
Security Issue Type 43 44 2 A/N Notes: 
[[NSCC]] does not validate the value 
against the Fund/SERV Security 
O  

---

## Page 61

Variable Length Record Layouts (Part 3) 
Interval Fund Acknowledgement (030) 61 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
Control Number 45 59 15 A/N [[NSCC]] will reject if value does not 
match Order (001), or Correction 
(003). 
R 005 
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
Space = No correction 
 
Best Practice: 
• Populate when acknowledging a 
Correction (003). Value must 
match latest correction indicator. 
• [[DO]] not populate when 
acknowledging an Order (001). 
R 006 
Filler 61 61 1 A/N Space R  
Transaction Code 62 63 2 A/N 03 = Partial [[liquidation]] 
04 = Full [[liquidation]]  
OC 018 
Submission Date 64 71 8 N mmddccyy R 101 
Trade Date 72 79 8 N mmddccyy 
 
[[NSCC]] will reject if value does not 
match Order (001), or Correction 
(003). 
O 016 
Filler 80 84 5 A/N Space R  
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code  
R  
Filler  89 104 16 A/N Filler R  

---

## Page 62

Variable Length Record Layouts (Part 3) 
Interval Fund Acknowledgement (030) 62 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Customer Account 
Number at Firm 
105 124 20 A/N Required if ‘Customer Account 
Number at Fund’ field is not 
populated. 
RC 020 
Customer Account 
Number at Fund 
125 144 20 A/N 
Required if ‘Customer Account 
Number at Firm’ field is not populated.
 
RC 011 
Filler 145 197 53 A/N Space R  
 
 

---

## Page 63

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 8, 2023 
Publication Code: MFS318 
Service: Fund/SERV® 
Title: Variable Length Record Layouts (Part 3) 
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 
 
 