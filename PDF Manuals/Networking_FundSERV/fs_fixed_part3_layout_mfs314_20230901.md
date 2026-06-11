---
title: "Fund/SERV - Fixed Length Record Layouts (Part 3)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_fixed_part3_layout_mfs314_20230901.pdf"
pages: 108
size: "1016.5 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Fund/SERV - Fixed Length Record Layouts (Part 3)

**Original File:** [fs_fixed_part3_layout_mfs314_20230901.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_fixed_part3_layout_mfs314_20230901.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 108  
**File Size:** 1016.5 KB  

---

## Page 1

 
 
 
Fund/SERV® 
FIXED LENGTH RECORD LAYOUTS (PART 3) 
SEPTEMBER 1, 2023 
 

---

## Page 2

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 2 
 
HISTORY OF IMPORTANT NOTICES 
Dates Important Notices 
September 1, 2023 Record has been rebranded and reviewed. 
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

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 3 
 
Dates Important Notices 
Documentation Changes Please see Important Notice: 
a7592 P&S 7162 Dated March 1, 2013 
Effective Date:  April 23, 2012 Please see Important Notice: 
A7355 P&S 6925 Dated January 12, 2012  
Note: On 2/27/2012 a correction was made to 401 Records to reflect the 
changes that were made in accordance with Important Notice a6272 P&S 
5842.   
The Fund Account Indicator 4 (New Account – U.S. Tax Resident Living Abroad) 
has been added to Account Representative Name, Account Representative 
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

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 4 
 
TABLE OF CONTENTS 
ACATS Transfer Acknowledgement/Rejection (019) ........................................................................................ 7 
02.12.01 ACATS Transfer Acknowledgement/Rejection (019) Record 1 of 3  ................................................... 7 
02.12.02 ACATS Transfer Acknowledgement/Rejection (019) Record 2 of 3  .................................................10 
02.12.03 ACATS Transfer Acknowledgement/Rejection (019) Record 3 of 3 .................................................12 
Transfer of Retirement [[Asset]] (ToRA) (210) ..................................................................................................... 13 
02.13.01 Transfer of Retirement [[Asset]] (ToRA) (210) Record 1 of 3 ................................................................13 
02.13.02 Transfer of Retirement [[Asset]] (ToRA) (210) Record 2 of 3 ................................................................15 
02.13.03 Transfer of Retirement [[Asset]] (ToRA) (210) Record 3 of 3 ................................................................17 
ToRA Acknowledgement (211); ToRA Confirmation (212); ToRA Reconfirmation (213) ............................ 18 
02.14.01 ToRA Acknowledgement (211) Record 1 of 4 ...................................................................................18 
02.14.02 ToRA Acknowledgement (211) Record 2 of 4 ...................................................................................20 
02.14.03  ToRA Acknowledgement (211) Record 3 of 4 ..................................................................................22 
02.14.04 ToRA Acknowledgement (211) Record  4 of 4 ..................................................................................23 
Defined Contribution Plan (DCP) Information (002) ....................................................................................... 24 
02.15.01 Defined Contribution Plan (DCP) Information (002) Record 1 of 32 .................................................24 
02.15.02 Defined Contribution Plan (DCP) Information (002) Record 2 of 32 .................................................27 
02.15.03 Defined Contribution Plan (DCP) Information (002) Record 3 through 32  ........................................29 
Retiring [[participant]] (090) ................................................................................................................................... 30 
02.16.01 Retiring [[participant]] (090) Record 1 of 3 ............................................................................................30 
02.16.02 Retiring [[participant]] (090) Record 2 of 3 ............................................................................................33 
02.16.03 Retiring [[participant]] (090) Record 3 of 3 ............................................................................................35 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092)  ......................................................... 36 
02.17.01 Reminders (080) Record 1 of 1 .........................................................................................................36 
Firm/TPA/Investment Agent/TPP Input Trailer (999) ....................................................................................... 38 
02.18.01 Firm/TPA/Investment Agent Input Trailer (999) Record 1 of 1 ..........................................................38 
Fund Input Trailer (999) ..................................................................................................................................... 40 
02.19.01 Fund Input Trailer (999) Record 1 of 1 ..............................................................................................40 
[[NSCC]] Output Header (000) ................................................................................................................................ 41 

---

## Page 5

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 5 
 
02.20.01 [[NSCC]] Output Header (000) Record 1 of 1 ........................................................................................41 
[[NSCC]] Output Trailer (999) ................................................................................................................................. 42 
02.21.01 [[NSCC]] Output Trailer (999) Record 1 of 2 .........................................................................................42 
02.21.02 [[NSCC]] Output Trailer (999) Record 2 of 2 .........................................................................................44 
Grand Total Trailer (GTT) .................................................................................................................................. 45 
02.22.01 Grand Total Trailer (GTT) Record 1 of 1 ...........................................................................................45 
Settling Trade Detail (070); X -[[settlement]] Trade Detail (072); Settling Trade Detail for TPA/Investment 
Agent/TPP (074) .................................................................................................................................................. 46 
02.23.01 Settling Trade Detail (070) Record 1 of 2 ..........................................................................................46 
02.23.02 Settling Trade Detail (070) Record  2 of 2 .........................................................................................49 
Settling Trade Trail er (071); X -[[settlement]] Trade Trailer (073); Settling Trade Trailer for TPA/Investment 
Agent/TPP (075) .................................................................................................................................................. 50 
02.24.01 Settling Trade Trailer (071) Record 1 of 2 .........................................................................................50 
02.24.02 Settling Trade Trailer (071) 2 of 2 ......................................................................................................51 
Multiple Reject Codes (120) .............................................................................................................................. 52 
02.25.01 Multiple Reject Codes (120) Record 1 of 1 ........................................................................................52 
DataTrak Header ................................................................................................................................................. 54 
02.26.01 DataTrak Header Record 1 of 1 ........................................................................................................54 
DataTrak Trailer .................................................................................................................................................. 55 
02.27.01 DataTrak Trailer Record 1 of 1 ..........................................................................................................55 
Firm Exit (139) ..................................................................................................................................................... 56 
02.28.01 Firm Exit (139) Record 1 of 3.............................................................................................................56 
02.28.02 Firm Exit (139) Record 2 of 3.............................................................................................................59 
02.28.03 Firm Exit (139) Record 3 of 3.............................................................................................................61 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026)  ................... 62 
02.29.01 Correction (003) Record 1 of 14 ........................................................................................................62 
02.29.02 Correction (003) Record 2 of 14 ........................................................................................................68 
02.29.03 Correction (003) Record 3 of 14 ........................................................................................................71 
02.29.04 Correction (003) Record 4 of 14 ........................................................................................................77 
02.29.05 Correction (003) Record 5 of 14 ........................................................................................................81 

---

## Page 6

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 6 
 
02.29.06 Correction (003) Record 6 of 14 ........................................................................................................83 
02.29.07 Correction (003) Record 7 of 14 ........................................................................................................85 
02.29.08 Correction (003) Record 8 of 14 ........................................................................................................90 
02.29.09 Correction (003) Record 9 of 14 ........................................................................................................91 
02.29.10 Correction (003) Record 10 of 14 ......................................................................................................92 
02.29.11 Correction (003) Record 11 of 14 ......................................................................................................94 
02.29.12 Correction (003) Record 12 of 14 ......................................................................................................96 
02.29.13 Correction (003) Record 13 of 14 ......................................................................................................97 
02.29.14 Correction (003) Record 14 of 14 ......................................................................................................98 
SSN/EIN Suffix Record 1 of 1 .......................................................................................................................... 100 
02.30.01 SSN/EIN Suffix Record 1 of 1 ..........................................................................................................100 
Interval Fund Acknowledgement (030) .......................................................................................................... 104 
02.31.01 Acknowledgement (030) Record 1 of 2 ...........................................................................................104 
02.31.01 Acknowledgement (030) Record 2 of 2 ...........................................................................................107 
 
  
 
 
 
 
 

---

## Page 7

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 7 
 
ACATS TRANSFER ACKNOWLEDGEMENT/REJECTION 
(019) 
02.12.01 ACATS Transfer Acknowledgement/Rejection (019) Record 1 
of 3 
Required 
Input from funds to [[NSCC]]  
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N F = Fund R 187 
Filler 6 7 2 A/N Space R  
Receiving Firm 
Number 
8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 019 = ACATS Transfer 
Acknowledgment/ Rejection 
R 002 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use R  
Filler 39 40 2 A/N Space R  
Fund/SERV Control 
Number 
41 55 15 A/N  R 005 

---

## Page 8

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 8 
 
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Filler 56 59 4 A/N Space R  
Submission Date 60 67 8 N mmddccyy R 101 
Delivering Firm 
Number 
68 71 4 A/N  R 008 
Filler 72 72 1 A/N Space R  
Fund Reject Code 73 75 3 A/N Value other than space or zero 
indicates rejection 
R 022 
Filler 76 76 1 A/N Space R  
PI Delivery Indicator 77 77 1 A/N 0 = Deliver to customer  
1 = Deliver to firm  
2 = Deliver to agent for firm 
O 039 
Filler 78 80 3 A/N Space R  
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  

---

## Page 9

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 9 
 
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Fund [[settlement]] Date  85 92 8 A/N Field Format: 
Mmddccyy 
 
Must be valid calendar date and 
formatted correctly. 
 
Field Requirements: 
- Required for ACAT 
Acknowledgements  
- Optional for ACAT Rejects 
 
Best Practice for Acknowledgements: 
- Funds should populate this field 
with the trade date. This date 
represents the effective date the 
transfer moved on the books of the 
Fund. 
Note: 
For Funds that process “as-of” 
transfers, the “as of” date should be 
used. 
Best Practice for Rejects: 
- Funds should not populate this 
field if the ACAT is rejected. 
RC 280 
Filler 93 100 8 A/N Space R  
 
 
  

---

## Page 10

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 10 
 
02.12.02 ACATS Transfer Acknowledgement/Rejection (019) Record 2 
of 3 
Required 
Input from funds to [[NSCC]] 
Record 2 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Actual Share 
Quantity Transferred 
8 21 14 N 9,999,999,999.9999  
Optional if transfer is rejected by fund 
RC 019 
Customer Account 
Number At Fund 
(Receiving Firm) 
22 41 20 A/N  R 011 
Customer Account 
Number At Fund 
Indicator (Receiving 
Firm) 
42 42 1 A/N 1 = Fund  
2 = Firm 
R 048 
Certificate Date 43 50 8 N mmddccyy O 037 
Certificate Number 51 60 10 A/N  O  
Filler 61 67 7 A/N Space R  
Network Control 
Indicator (Receiving 
Firm) 
68 68 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
ACATS Control 
Number 
69 88 20 A/N  R 005 
Transfer 
Disbursement 
[[Option]] - Accruals 
89 89 1 A/N 
2 = Cash to customer - Delivering firm  
4 = Reinvest - Receiving firm (bucket 
to bucket) 
O 134 
Transfer 
Disbursement 
[[Option]] - Fractional 
[[Cash-in-Lieu]] 
90 90 1 A/N 0 = Cash to [[Broker]] - Delivering firm  
1 = Reinvest - Delivering firm  
2 = Cash to customer - Delivering firm  
3 = Cash to [[Broker]] - Receiving firm  
4 = Reinvest - Receiving firm  
O 134 

---

## Page 11

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 11 
 
Record 2 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
5 = Cash to customer - Receiving firm 
Transfer 
Disbursement 
[[Option]] - Residuals  
91 91 1 A/N 0 = Cash to [[Broker]] - Delivering firm  
1 = Reinvest - Delivering firm  
2 = Cash to customer - Delivering firm  
3 = Cash to [[Broker]] - Receiving firm  
4 = Reinvest - Receiving firm  
5 = Cash to customer - Receiving firm 
O 134 
Fund CDSC 
Transfer Indicator  
92 92 1 A/N Space O 209 
Filler 93 100 8 A/N Space R  
 
 
  

---

## Page 12

Fixed Length Record Layouts (Part 3) 
ACATS Transfer Acknowledgement/Rejection (019) 12 
 
02.12.03 ACATS Transfer Acknowledgement/Rejection (019) Record 3 
of 3 
Required 
Input from funds to [[NSCC]] 
Record 3 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Accrual Money Amount 8 23 16 N 99,999,999,999,999.99 O 111 
Accrual Money Amount 
Indicator 
24 24 1 A/N A = All  
B = None  
C = Not accepted 
O 112 
IRS 529 Annual 
Strategy Change 
Counter 
 
Effective 05/15/2023 
25 25 1 A/N 0 thru 9  
If populated, only 0 thru 9 are 
allowed. 
 
The number of strategy changes 
that occurred during a calendar 
year. 
O 287 
Earnings to Date 
Money Amount 
 
Effective 05/15/2023 
26 41 16 N 99,999,999,999,999.99 
 
Earnings of [[shares]] being 
transferred. 
O 262 
Negative Earnings to 
Date Indicator 
 
Effective 05/15/2023 
42 42 1 A/N N = Negative                    
Spaces = Positive 
 
 Indicates if the earnings 
amount is  negative. 
O 263 
Cost Basis Money 
Amount 
 
Effective 05/15/2023 
43 58 16 N 99,999,999,999,999.99 
 
Provide original cost of the [[shares]] 
that are being transferred. 
O 261 
Filler 59 100 42 A/N Space R  

---

## Page 13

Fixed Length Record Layouts (Part 3) 
Transfer of Retirement [[Asset]] (ToRA) (210) 13 
 
TRANSFER OF RETIREMENT [[Asset]] (TORA) (210) 
02.13.01 Transfer of Retirement [[Asset]] (ToRA) (210) Record 1 of 3 
Required 
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N F = Fund R 187 
Filler 6 7 2 A/N Space R  
Receiving Fund 
Number 
8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 210 = Transfer of Retirement [[Asset]] 
(ToRA) 
R 002 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Delivering Fund 
Number 
20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use R  
Security Issue Type 39 40 2 A/N  O 150 
Control Number 41 55 15 A/N  R 005 
Filler 56 56 1 A/N Space R  

---

## Page 14

Fixed Length Record Layouts (Part 3) 
Transfer of Retirement [[Asset]] (ToRA) (210) 14 
 
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Transaction Type 57 57 1 A/N 0 = Full transfer  
1 = Partial transfer  
2 = Full distribution to Alternate 
address  
3 = Partial distribution to Alternate 
address  
Must be 2 or 3 if Receiving Fund 
Plan Type = 9 
R 017 
Transaction Code 58 59 2 A/N Required if transaction Type = 1.  
01 = Percentage transfer  
02 = Share quantity  
03 = Money amount 
OC 018 
Submission Date 60 67 8 N mmddccyy R 101 
Filler 68 76 9 A/N Space R  
[[Broker]] of Record for 
Delivering Fund [[Asset]] 
77 80 4 A/N  O  
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  
Filler 85 100 16 A/N Space R  
 
 
  

---

## Page 15

Fixed Length Record Layouts (Part 3) 
Transfer of Retirement [[Asset]] (ToRA) (210) 15 
 
02.13.02 Transfer of Retirement [[Asset]] (ToRA) (210) Record 2 of 3 
Required 
Record 2 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Share Quantity 8 21 14 N 9,999,999,999.9999  
Required if Transaction Code = 02 
OC 019 
Customer Account 
Number at Delivering 
Fund 
22 41 20 A/N  R 020 
Receiving Fund Plan 
Type 
42 42 1 A/N 0 = IRA  
1 = IRA rollover  
2 = SEP IRA  
3 = 403B  
4 = Roth IRA  
5 = Simple IRA  
6 = Education IRA  
7 = SARSEP  
8 = Roth conversion IRA  
9 = Traditional to Roth conversion IRA  
A = Inherited Traditional IRA  
B = Inherited Roth IRA  
C = Inherited Roth conversion IRA  
Must be 9 if Transaction Type = 2 or 3 
R 183 
Percentage Rate 43 47 5 N 99.999  
Required if Transaction Code = 01 
OC 184 
Original Roth IRA Date 
(As known by the 
receiving fund) 
48 55 8 N mmddccyy O 185 

---

## Page 16

Fixed Length Record Layouts (Part 3) 
Transfer of Retirement [[Asset]] (ToRA) (210) 16 
 
Record 2 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Customer Zip Code 56 66 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 
digits for future postal expansion 
 
R 127 
Filler 67 100 34 A/N Space R  
 
 
  

---

## Page 17

Fixed Length Record Layouts (Part 3) 
Transfer of Retirement [[Asset]] (ToRA) (210) 17 
 
02.13.03 Transfer of Retirement [[Asset]] (ToRA) (210) Record 3 of 3 
Required 
Record 3 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Money Amount 8 23 16 N 99,999,999,999,999.99  
Required if Transaction Code = 03 
OC 019 
Currency Indicator 24 26 3 A/N  O 110 
Filler 27 34 8 A/N Space R  
Customer Name at 
Receiving Fund 
35 69 35 A/N  R 063 
SSN/EIN Number at 
Receiving Fund 
70 78 9 A/N  R 103 
IRA Withholding 
Percentage 
79 83 5 N 99.999  
Allowed only if Receiving Fund Plan 
Type = 9 
O 158 
SSN/EIN Indicator 
(Receiving Fund) 
84 84 1 A/N 0 = Tax [[ID]] number  
1 = Social security number  
2 = [[investor]] TIN/EIN 
O 102 
Filler 85 100 16 A/N Space R  

---

## Page 18

Fixed Length Record Layouts (Part 3) 
ToRA Acknowledgement (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 18 
 
TORA ACKNOWLEDGEMENT (211); TORA 
CONFIRMATION (212); TORA RECONFIRMATION (213)  
02.14.01 ToRA Acknowledgement (211) Record 1 of 4 
Required 
Record 1 of 4 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N F = Fund R 187 
Filler 6 7 2 A/N Space R  
Receiving Fund 
Number 
8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 211 = ToRA Acknowledgment  
212 = ToRA Confirmation  
213 = ToRA Reconfirmation 
R 002 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Delivering Fund 
Number 
20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use R  
Security Issue Type 39 40 2 A/N  O 150 
Control Number 41 55 15 A/N  R 005 
Filler 56 56 1 A/N Space R  

---

## Page 19

Fixed Length Record Layouts (Part 3) 
ToRA Acknowledgement (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 19 
 
Record 1 of 4 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Transaction Type 57 57 1 A/N 0 = Full transfer  
1 = Partial transfer  
2 = Full distribution to Alternate 
address  
3 = Partial distribution to Alternate 
address  
Must be 2 or 3 if Delivering Fund 
Plan Type = 9 
R 017 
Transaction Code 58 59 2 A/N Required if transaction Type = 1.  
01 = Percentage transfer  
02 = Share quantity  
03 = Money amount 
OC 018 
Submission Date 60 67 8 N mmddccyy R 101 
Trade Date 68 75 8 N mmddccyy 
Required for record types 212 and 
213 
OC 016 
Filler 76 76 1 N Space R  
[[Broker]] of Record for 
Delivering Fund [[Asset]] 
77 80 4 A/N  O  
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  
Filler 85 100 16 A/N Space R  
 
 
  

---

## Page 20

Fixed Length Record Layouts (Part 3) 
ToRA Acknowledgement (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 20 
 
02.14.02 ToRA Acknowledgement (211) Record 2 of 4 
Required 
Record 2 of 4 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Share Quantity 8 21 14 N 9,999,999,999.9999  
Required for record type 212 and 213.  
Required for record type 211 if 
Transaction Code = 02 
OC 019 
Customer Account 
Number at Delivering 
Fund 
22 41 20 A/N  R 020 
Delivering Fund Plan 
Type 
42 42 1 A/N 0 = IRA  
1 = IRA rollover  
2 = SEP IRA  
3 = 403B  
4 = Roth IRA  
5 = Simple IRA  
6 = Education IRA  
7 = SARSEP  
8 = Roth conversion IRA  
9 = Traditional to Roth conversion IRA  
A = Inherited Traditional IRA  
B = Inherited Roth IRA  
C = Inherited Roth conversion IRA  
Must be 9 if Transaction Type = 2 or 3 
R 183 
Percentage Rate 43 47 5 N 99.999  
Required if Transaction Code = 01 
OC 184 
Original Roth IRA Date 
(As known by the 
delivering fund) 
48 55 8 N mmddccyy  
Required if delivering Fund Plan Type 
= 4 or 8 
OC 185 

---

## Page 21

Fixed Length Record Layouts (Part 3) 
ToRA Acknowledgement (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 21 
 
Record 2 of 4 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Customer Zip Code 56 66 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 
digits for future postal expansion 
R 127 
Uncollected [[shares]] 67 80 14 N Share Field, Format: 
9,999,999,999.9999 
O   266 
Filler 81 100 20 A/N Space R  
 
 
  

---

## Page 22

Fixed Length Record Layouts (Part 3) 
ToRA Acknowledgement (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 22 
 
02.14.03  ToRA Acknowledgement (211) Record 3 of 4 
Required 
Record 3 of 4 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Money Amount 8 23 16 N 99,999,999,999,999.99  
Required if Transaction Code = 03 
OC 019 
Currency Indicator 24 26 3 A/N  O 110 
Anticipated [[settlement]] 
Date 
27 34 8 A/N mmddccyy  
For record types 212 and 213 only.  
Input: Space  
Output: Anticipated [[settlement]] date 
R  
Customer Name at 
Delivering Fund 
35 69 35 A/N  R 063 
SSN/EIN Number at 
Delivering Fund 
70 78 9 A/N  R 103 
IRA Withholding 
Percentage 
79 83 5 N 99.999  
Allowed only if Receiving Fund Plan 
Type = 9 
O 158 
SSN/EIN Indicator 
(Delivering Fund) 
84 84 1 A/N 0 = Tax [[ID]] number  
1 = Social security number  
2 = [[investor]] TIN/EIN 
O 102 
Filler 85 100 16 A/N Space R  
 
 
  

---

## Page 23

Fixed Length Record Layouts (Part 3) 
ToRA Acknowledgement (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 23 
 
02.14.04 ToRA Acknowledgement (211) Record  4 of 4 
Required 
Record 4 of 4 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Fee Amount 8 15 8 N 999,999.99 O 115 
Fee Type 16 16 1 A/N Required if Fee Amount > 0.  
1 = [[liquidation]] fee  
2 = Redemption fee  
3 = Surrender fee 
OC 116 
Amount Due 17 32 16 N 99,999,999,999,999.99  
For record type 211, this amount 
shows [[Asset]] value at 
acknowledgment time.  
For record types 212 or 213, this 
amount will be settled by [[NSCC]] 
R 026 Price Per Share 33 44 12 N 999,999.999999  
Optional for record type 211 
RC 027 
Accrual Amount 45 60 16 N 99,999,999,999,999.99 O 111 
Accrual Indicator 61 61 1 A/N Required if Accrual Amount is 
provided.  
0 = Included in Amount Due  
1 = Paid via Cash Adjustment  
2 = Paid outside system 
OC 112 
Withholding Amount 62 77 16 N 99,999,999,999,999.99  
Allowed only if Delivering Fund Plan 
Type = 9 
O 113 
Filler 78 100 23 A/N Space R  

---

## Page 24

Fixed Length Record Layouts (Part 3) 
Defined Contribution Plan (DCP) Information (002) 24 
 
DEFINED CONTRIBUTION PLAN (DCP) INFORMATION 
(002) 
02.15.01 Defined Contribution Plan (DCP) Information (002) Record 1 
of 32 
Required 
Record 1 of 32 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N A = Investment Agent 
B = Firm  
F = Fund 
T = TPA 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 002 = Defined Contribution Plan 
Information 
R 002 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use R  

---

## Page 25

Fixed Length Record Layouts (Part 3) 
Defined Contribution Plan (DCP) Information (002) 25 
 
Record 1 of 32 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Type 39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation  
Space = No correction 
R 006 
Filler 57 59 3 A/N Space R  
Submission Date 60 67 8 N mmddccyy R 101 
Filler 68 78 11 A/N Space R  
Number of Records 
Beyond Record #1 
79 80 2 A/N Space R 049 
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  

---

## Page 26

Fixed Length Record Layouts (Part 3) 
Defined Contribution Plan (DCP) Information (002) 26 
 
Record 1 of 32 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
TPA/Investment Agent 
Number 
85 88 4 A/N Required if Originator Type = T or A  OC 188 
Filler 89 100 12 A/N Space R  
 
 
  

---

## Page 27

Fixed Length Record Layouts (Part 3) 
Defined Contribution Plan (DCP) Information (002) 27 
 
02.15.02 Defined Contribution Plan (DCP) Information (002) Record 2 
of 32 
Required. 
Record 2 of 32 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
DC Amount Code 1 8 10 3 A/N See DC Amount Code List. R 190 
DC Amount 1 11 26 16 N 99,999,999,999,999.99 R 191 
DC Debit/Credit 
Indicator 1 
27 27 1 A/N 1 = Debit  
2 = Credit 
R 192 
DC Amount Code 2 28 30 3 A/N See DC Amount Code List.  
Required if DC Amount 2 > 0 
OC 193 
DC Amount 2 31 46 16 N 99,999,999,999,999.99  
Required if DC Amount Code 2 is 
provided 
OC 194 
DC Debit/Credit 
Indicator 2 
47 47 1 A/N Required if DC Amount Code 2 is 
provided.  
1 = Debit  
2 = Credit 
R 195 
DC Amount Code 3 48 50 3 A/N See DC Amount Code List.  
Required if DC Amount 3 > 0 
OC 196 
DC Amount 3 51 66 16 N 99,999,999,999,999.99  
Required if DC Amount Code 3 is 
provided 
OC 197 
DC Debit/Credit 
Indicator 3 
67 67 1 A/N Required if DC Amount Code 3 is 
provided.  
1 = Debit  
2 = Credit 
R 198 
DC Amount Code 4 68 70 3 A/N See DC Amount Code List.  
Required if DC Amount 4 > 0 
OC 199 

---

## Page 28

Fixed Length Record Layouts (Part 3) 
Defined Contribution Plan (DCP) Information (002) 28 
 
Record 2 of 32 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
DC Amount 4 71 86 16 N 99,999,999,999,999.99  
Required if DC Amount Code 4 is 
provided 
OC 200 
DC Debit/Credit 
Indicator 4 
87 87 1 A/N Required if DC Amount Code 4 is 
provided.  
1 = Debit  
2 = Credit 
R 201 
Filler 88 100 13 A/N Space R  
 
 
  

---

## Page 29

Fixed Length Record Layouts (Part 3) 
Defined Contribution Plan (DCP) Information (002) 29 
 
02.15.03 Defined Contribution Plan (DCP) Information (002) Record 3 
through 32  
Optional  
The previous record (#2) may repeat itself 30 more times with Logical Sequence Numbers 03 through 
32 to a total of 124 DC amounts.  
Note: 
DC Amount Codes must be in ascending order and cannot repeat themselves, i.e., each DC Amount Code must be greater 
than the one preceded it in the same transaction. 

---

## Page 30

Fixed Length Record Layouts (Part 3) 
Retiring [[participant]] (090) 30 
 
RETIRING [[participant]] (090) 
02.16.01 Retiring [[participant]] (090) Record 1 of 3 
Output from [[NSCC]] to firms and funds. When relating to ToRA (Transfer of Retirement [[Asset]]), Firm 
means Receiving Fund, and Fund means Delivering Fund  
Record 1 of 3 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N N = [[NSCC]] 
Filler 6 7 2 A/N Space 
Original Firm Number 8 11 4 N  
Filler 12 14 3 A/N Space 
Record Type 15 17 3 A/N 090 = Retiring [[participant]] 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
Filler 19 19 1 A/N Space 
Original Fund Number 20 23 4 N  
Filler 24 26 3 A/N Space 
Security Issue Country 
Code 
27 28 2 A/N Space. For future use 
Security Issue [[ID]] 29 37 9 A/N  
Security Issue Check Digit 38 38 1 A/N Space. For future use 
Security Issue Type 39 40 2 A/N  
Control Number 41 55 15 A/N  
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction  
P = Post [[settlement]] correction/cancellation  
Space = No correction 
Action Code 57 57 1 A/N P = Purge  
C = Convert 

---

## Page 31

Fixed Length Record Layouts (Part 3) 
Retiring [[participant]] (090) 31 
 
Record 1 of 3 
Field Name  
Start End Len Type Description  
Transaction Code 58 59 2 A/N 01 = Initial purchase  
02 = Subsequent purchase  
03 = Partial [[liquidation]]  
04 = Full [[liquidation]]  
05 = Full exchange  
06 = Partial exchange  
07 = Post settle correct/cancel purchase  
08 = Post settle correct/cancel [[liquidation]] 
Effective Date 60 67 8 N mmddccyy 
Trade Date (when available) 68 75 8 N mmddccyy 
Filler 76 76 1 A/N Space 
Processing Type 77 77 1 A/N 1 = Order, Cash Adjustment or ToRA  
2 = Exchange  
3 = Registration 
Debit/Credit Indicator 78 79 2 A/N DB = Debit firm  
CR = Credit firm  
NS = No [[settlement]] 
Filler 80 81 2 A/N Space 
Status 82 84 3 A/N 0A1 = Due to Settle  
081 = Order Not Acted Upon  
083 = Registration Pending  
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
TPA/Investment Agent/TPP 
Number 
85 88 4 A/N  

---

## Page 32

Fixed Length Record Layouts (Part 3) 
Retiring [[participant]] (090) 32 
 
Record 1 of 3 
Field Name  
Start End Len Type Description  
Service Provider Number 89 92 4 A/N  
Filler 93 100 8 A/N Space 
 
 
  

---

## Page 33

Fixed Length Record Layouts (Part 3) 
Retiring [[participant]] (090) 33 
 
02.16.02 Retiring [[participant]] (090) Record 2 of 3 
Output from [[NSCC]] 
Record 2 of 3 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 02 
Filler 5 7 3 A/N Space 
Original Record Type 8 10 3 A/N 001 = Firm Order  
003 = Post [[settlement]] Correction by Firm  
004 = As-Of Order  
007 = Fund Originated Order  
009 = Fund Originated As-Of Order  
011 = Cash Adjustment  
015 = Exchange  
021 = Post [[settlement]] Exchange Cancellation 
by Fund  
026 = Post [[settlement]] Correction by Fund  
139 = Post [[settlement]] Cancellation by Firm  
140 = Post [[settlement]] Cancellation by Fund  
200 = Extended Correction Transfer  
210 = Transfer of Retirement [[Asset]] (ToRA) 
Share Quantity 11 24 14 N 9,999,999,999.9999 
Filler 25 26 2 A/N Space 
Anticipated [[settlement]] Date 27 34 8 A/N mmddccyy  
(Zero if not established yet) 
Exchange To Security Issue 
Country Code (when 
Process Type = 2) 
35 36 2 A/N  
Exchange To Security Issue 
[[ID]] (when Process Type = 2) 
37 45 9 A/N  
Exchange To Security Issue 
Check Digit (when Process 
Type = 2) 
46 46 1 A/N  
Exchange To Security Issue 
Type (when Process Type = 
2) 
47 48 2 A/N  

---

## Page 34

Fixed Length Record Layouts (Part 3) 
Retiring [[participant]] (090) 34 
 
Record 2 of 3 
Field Name  
Start End Len Type Description  
Exchange To Money 
Amount (when Process 
Type = 2) 
49 64 16 N 99,999,999,999,999.99 
Exch To Currency Indicator 
(when Process Type = 2) 
65 67 3 A/N  
Exchange To Share 
Quantity (when Process 
Type = 2) 
68 81 14 N 9,999,999,999.9999 
Filler 82 100 19 A/N Space 
 
 
  

---

## Page 35

Fixed Length Record Layouts (Part 3) 
Retiring [[participant]] (090) 35 
 
02.16.03 Retiring [[participant]] (090) Record 3 of 3 
Output from [[NSCC]] 
Record 3 of 3 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 03 
Filler 5 7 3 A/N Space 
Money Amount 8 23 16 N 99,999,999,999,999.99 
Currency Indicator 24 26 3 A/N  
Retiring [[participant]] Number 27 30 4 A/N  
Surviving [[participant]] 
Number (when Action Code 
= C) 
31 34 4 A/N  
Filler 35 100 66 A/N Space 

---

## Page 36

Fixed Length Record Layouts (Part 3) 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092) 36 
 
REMINDERS (080, 081, 082, 083, 084, 085, 086, 087, 088, 
089, 091, 092) 
02.17.01 Reminders (080) Record 1 of 1 
Output from [[NSCC]] to firms and funds. For record types 091 and 092, Firm means Receiving Fund, and 
Fund means Delivering Fund  
Record 1 of 1  
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N N = [[NSCC]] 
Filler 6 7 2 A/N Space 
Firm Number 
(for record type 080 this is 
the receiving firm) 
8 11 4 N  
Filler 12 14 3 A/N Space 
Record Type 15 17 3 A/N 080 =Pending ACATS Transfer 
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
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
Filler 19 19 1 A/N Space 

---

## Page 37

Fixed Length Record Layouts (Part 3) 
Reminders (080, 081, 082, 083, 084, 085, 086, 087, 088, 089, 091, 092) 37 
 
Record 1 of 1  
Field Name  
Start End Len Type Description  
Fund Number 20 23 4 N  
Filler 24 26 3 A/N Space 
Security Issue Country 
Code 
27 28 2 A/N Space. For future use 
Security Issue [[ID]] 29 37 9 A/N  
Security Issue Check Digit 38 38 1 A/N Space. For future use 
Security Issue Type 39 40 2 A/N  
Control Number 41 55 15 A/N  
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction  
P = Post [[settlement]] correction/cancellation  
Space = No correction 
ACATS TIF Number 57 70 14 A/N For record type 080 Only.  
First 14 bytes of ACATS Control Number 
Delivering Firm Number 71 74 4 A/N For record type 080 only 
Reminder Age 75 78 4 N 1-9998 = Reminder age (in business days)  
9999 = Pending period expired, original 
transaction deleted by Fund/SERV 
Reminder 080 record with age 9999 will no 
longer be sent to Funds (Important Notice 
A8107) 
ACATS [[Asset]] Sequence 
Number 
79 84 6 A/N For record type 080 Only.  
Last 6 bytes of ACATS Control Number 
TPA/Investment Agent/TPP 
Number 
85 88 4 A/N  
Service Provider Number 89 92 4 A/N  
Original Record Type 93 95 3 A/N  
Filler 96 100 5 A/N Space 

---

## Page 38

Fixed Length Record Layouts (Part 3) 
Firm/TPA/Investment Agent/TPP Input Trailer (999) 38 
 
FIRM/TPA/INVESTMENT AGENT/TPP INPUT TRAILER 
(999) 
02.18.01 Firm/TPA/Investment Agent Input Trailer (999) Record 1 of 1 
Required. Input from firms, TPA/TPPs and Investment Agents to [[NSCC]]  
Record 1 of 1 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Physical Sequence 
Number 
1 2 2 A/N  R 
Logical Sequence 
Number 
3 4 2 A/N 02 R 
Originator Type 5 5 1 A/N A = Investment Agent 
B = Firm  
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider) 
R 
Filler 6 7 2 A/N Space R 
Firm/TPA/SP/Investment 
Agent/TPP Number 
8 11 4 N  R 
Filler 12 14 3 A/N Space R 
Record Type 15 17 3 A/N 999 = Trailer R 
Submission Date 18 25 8 N mmddccyy R 
Total Order Transactions 26 31 6 N 999,999 R 
Total Firm Delete 
Transactions 
32 37 6 N 999,999 R 
Total Correction 
Transactions 
38 43 6 N 999,999 R 
Total As-Of Transactions 44 49 6 N 999,999 R 
Total Registration 
Transactions 
50 55 6 N 999,999 R 
Total Exchange 
Transactions 
56 61 6 N 999,999 R 
Filler 62 67 6 A/N Space R 

---

## Page 39

Fixed Length Record Layouts (Part 3) 
Firm/TPA/Investment Agent/TPP Input Trailer (999) 39 
 
Record 1 of 1 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Total Other Transactions 68 73 6 N 999,999 R 
Filler 74 100 27 A/N Space R 

---

## Page 40

Fixed Length Record Layouts (Part 3) 
Fund Input Trailer (999) 40 
 
FUND INPUT TRAILER (999)  
02.19.01 Fund Input Trailer (999) Record 1 of 1 
Required. Input from funds to [[NSCC]]  
Record 1 of 1 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Physical Sequence 
Number 
1 2 2 A/N  R 
Logical Sequence 
Number 
3 4 2 A/N 01 R 
Originator Type 5 5 1 A/N F = Fund R 
Filler 6 7 2 A/N Space R 
Fund Number 8 11 4 N  R 
Filler 12 14 3 A/N Space R 
Record Type 15 17 3 A/N 999 = Trailer R 
Submission Date 18 25 8 N mmddccyy R 
Total Confirmation 
Transactions 
26 31 6 N 999,999 R 
Total Reconfirmation 
Transactions 
32 37 6 N 999,999 R 
Total Fund Order 
Transactions 
38 43 6 N 999,999 R 
Total Release to 
[[settlement]] Transactions 
44 49 6 N 999,999 R 
Total Fund Delete 
Transactions 
50 55 6 N 999,999 R 
Filler 56 67 12 A/N Space R 
Total Other Transactions 68 73 6 N 999,999 R 
Filler 74 100 27 A/N Space R 

---

## Page 41

Fixed Length Record Layouts (Part 3) 
[[NSCC]] Output Header (000) 41 
 
[[NSCC]] OUTPUT HEADER (000) 
02.20.01 [[NSCC]] Output Header (000) Record 1 of 1 
Output from [[NSCC]]  
Record 1 of 1 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N N = [[NSCC]] 
Filler 6 7 2 A/N Space 
Recipient Number 8 11 4 N  
Filler 12 14 3 A/N Space 
Record Type 15 17 3 A/N 000 = [[NSCC]] Output Header 
Transmission Date 18 25 8 N mmddccyy 
Literal 26 29 4 A/N FILE 
AutoRoute File Number 30 37 8 A/N  
AutoRoute File Cycle 38 39 2 A/N  
File Description 40 57 18 A/N [[Mutual Funds]] INPUT  
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
Filler 58 100 43 A/N Space 

---

## Page 42

Fixed Length Record Layouts (Part 3) 
[[NSCC]] Output Trailer (999) 42 
 
[[NSCC]] OUTPUT TRAILER (999)  
02.21.01 [[NSCC]] Output Trailer (999) Record 1 of 2 
Output from [[NSCC]]  
Record 1 of 2 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N N = [[NSCC]] 
Filler 6 7 2 A/N Space 
Recipient Number 8 11 4 N  
Filler 12 14 3 A/N Space 
Record Type 15 17 3 A/N 999 = Trailer 
Transmission Date 18 25 8 N mmddccyy 
Total Order Transactions 26 31 6 N 999,999 
Total Firm Delete 
Transactions 
32 37 6 N 999,999 
Total Correction 
Transactions 
38 43 6 N 999,999 
Total As-Of Transactions 44 49 6 N 999,999 
Total Confirmation 
Transactions 
50 55 6 N 999,999 
Total Reconfirmation 
Transactions 
56 61 6 N 999,999 
Total Fund Order 
Transactions 
62 67 6 N 999,999 
Total Release to [[settlement]] 
Transactions 
68 73 6 N 999,999 
Total Fund Delete 
Transactions 
74 79 6 N 999,999 
Total Registration 
Transactions 
80 85 6 N 999,999 

---

## Page 43

Fixed Length Record Layouts (Part 3) 
[[NSCC]] Output Trailer (999) 43 
 
Record 1 of 2 
Field Name  
Start End Len Type Description  
Total Reminders 86 91 6 N 999,999 
Filler 92 100 9 A/N Space 
 
 
  

---

## Page 44

Fixed Length Record Layouts (Part 3) 
[[NSCC]] Output Trailer (999) 44 
 
02.21.02 [[NSCC]] Output Trailer (999) Record 2 of 2 
Output from [[NSCC]]  
Record 2 of 2 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 02 
Filler 5 7 3 A/N Space 
Total Cash Adjustments 
Transactions 
8 13 6 N 999,999 
Total Exchange Order 
Transactions 
14 19 6 N 999,999 
Total Exchange 
Confirmation Transactions 
20 25 6 N 999,999 
Total Exchange 
Reconfirmation 
Transactions 
26 31 6 N 999,999 
Filler 32 67 36 A/N Space 
Total Other Transactions 68 73 6 N 999,999 
Filler 74 100 27 A/N Space 

---

## Page 45

Fixed Length Record Layouts (Part 3) 
Grand Total Trailer (GTT) 45 
 
GRAND TOTAL TRAILER (GTT)  
02.22.01 Grand Total Trailer (GTT) Record 1 of 1 
Output from [[NSCC]]. This trailer record is available upon request. It is especially beneficial for service 
bureaus or transfer agents or any other processor who handles multiple [[NSCC]] participants or 
members.  
Record 1 of 1 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N N = [[NSCC]] 
Filler 6 14 9 A/N Space 
Record Type 15 17 3 A/N GTT = Grand Total Trailer 
Transmission Date 18 25 8 N mmddccyy 
Total Records 26 33 8 N 99,999,999  
Grand total # of output records including 
headers and trailers 
Literal 34 52 19 A/N GRAND TOTAL TRAILER 
Filler 53 53 1 A/N Space 
AutoRoute File Number 54 61 8 A/N  
AutoRoute File Cycle 62 63 2 A/N  
Filler 64 100 37 A/N Space 

---

## Page 46

Fixed Length Record Layouts (Part 3) 
Settling Trade Detail (070); X-[[settlement]] Trade Detail (072); Settling Trade Detail for TPA/Investment Agent/TPP (074) 46 
 
SETTLING TRADE DETAIL (070); X-[[settlement]] TRADE 
DETAIL (072); SETTLING TRADE DETAIL FOR 
TPA/INVESTMENT AGENT/TPP (074) 
02.23.01 Settling Trade Detail (070) Record 1 of 2 
Output from [[NSCC]]  
Record 1 of 2 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N N = [[NSCC]] 
Filler 6 7 2 A/N Space 
Recipient Number 8 11 4 N  
Filler 12 14 3 A/N Space 
Record Type 15 17 3 A/N 070 = Settling Trade Detail  
072 = X-[[settlement]] Trade Detail 
074 = Settling Trade Detail for 
TPA/Investment Agent/TPP 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
Filler 19 19 1 A/N Space 
Contra [[participant]] Number 20 23 4 N  
Filler 24 26 3 A/N Space 
Security Issue Country 
Code 
27 28 2 A/N Space. For future use 
Security Issue [[ID]] 29 37 9 A/N  
Security Issue Check Digit 38 38 1 A/N Space. For future use 
Security Issue Type 39 40 2 A/N  
Control Number 41 55 15 A/N  

---

## Page 47

Fixed Length Record Layouts (Part 3) 
Settling Trade Detail (070); X-[[settlement]] Trade Detail (072); Settling Trade Detail for TPA/Investment Agent/TPP (074) 47 
 
Record 1 of 2 
Field Name  
Start End Len Type Description  
Correction/Exchange 
Indicator 
56 56 1 A/N A = Exchange From (credit firm, debit fund)  
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
Trade Type 57 59 3 A/N ADJ = Cash Adjustment  
CXL = Cancelled [[Underwriting]]/Tender  
RAT = Transfer of Retirement [[Asset]]  
TND = Tender  
UND = [[Underwriting]]  
XCH = Exchange  
Space = None of the above 
[[settlement]] Date 60 67 8 N mmddccyy 
Trade Date 68 75 8 N mmddccyy 
Agent for Firm Number 76 79 4 A/N  
Buy/Sell Code 80 80 1 A/N 2 = Buy (recipient debit)  
4 = Sell (recipient credit) 
Filler 81 83 3 A/N Space 
Recipient Type 84 84 1 A/N B = Firm (Receiving fund if a ToRA item)  
F = Fund (Delivering fund if a ToRA item)  
T = TPA/Investment Agent  
S = Service Provider 
V = TPP (Third Party Provider) 
Firm or TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Firm Number when Recipient Type = T or V.  
Otherwise, TPA/Investment Agent/TPP 
Number  

---

## Page 48

Fixed Length Record Layouts (Part 3) 
Settling Trade Detail (070); X-[[settlement]] Trade Detail (072); Settling Trade Detail for TPA/Investment Agent/TPP (074) 48 
 
Record 1 of 2 
Field Name  
Start End Len Type Description  
Service Provider or Firm 
Number 
89 92 4 A/N Firm Number when Recipient Type = S.  
Otherwise, Service Provider Number 
Filler 93 100 8 A/N Space 
 
 
  

---

## Page 49

Fixed Length Record Layouts (Part 3) 
Settling Trade Detail (070); X-[[settlement]] Trade Detail (072); Settling Trade Detail for TPA/Investment Agent/TPP (074) 49 
 
02.23.02 Settling Trade Detail (070) Record  2 of 2 
Output from [[NSCC]]  
Record 2 of 2 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Filler 5 17 13 A/N Space 
*Share Quantity 18 31 14 N 9,999,999,999.9999 
*Price Per Share 32 43 12 N 999,999.999999 
[[settlement]] Money Amount 44 59 16 N 99,999,999,999,999.99 
Currency Indicator 60 62 3 A/N For record type 070/074:  
USD = Same day [[settlement]]  
USN = Next day [[settlement]]  
EUR or GBP 
For record type 072: 
Any currency code 
[[settlement]] Indicator 63 63 1 A/N A = Automatic [[settlement]]  
F = Fund approved [[settlement]]  
Space = Cash Adjustment 
Contra Exchange Security 
Issue Country Code 
64 65 2 A/N Space. For future use 
Contra Exchange Security 
Issue [[ID]] 
66 74 9 A/N  
Contra Exchange Security 
Issue Check Digit 
75 75 1 A/N Space. For future use 
Filler 76 100 25 A/N Space 
 
*Note: 
For the Exchange To side, values in the Share Quantity and Price Per Share fields reflect the information contained on 
record #8 of the Exchange Confirmation/Reconfirmation/Post [[settlement]] Cancellation transactions (record types 
016/017/021). 

---

## Page 50

Fixed Length Record Layouts (Part 3) 
Settling Trade Trailer (071); X-[[settlement]] Trade Trailer (073); Settling Trade Trailer for TPA/Investment Agent/TPP (075) 50 
 
SETTLING TRADE TRAILER (071); X-[[settlement]] 
TRADE TRAILER (073); SETTLING TRADE TRAILER FOR 
TPA/INVESTMENT AGENT/TPP (075) 
02.24.01 Settling Trade Trailer (071) Record 1 of 2 
Output from [[NSCC]] 
Record 1 of 2 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N N = [[NSCC]] 
Filler 6 7 2 A/N Space 
Recipient Number 8 11 4 N  
Filler 12 14 3 A/N Space 
Record Type 15 17 3 A/N 071 = Settling Trade Trailer  
073 = X-[[settlement]] Trade Trailer 
075 = Settling Trade Trailer for 
TPA/Investment Agent/TPP 
Literal 18 32 15 A/N  ‘999999999999999’ 
Literal 33 44 12 A/N For record type 071:  
SETT.TRD.TRL  
For record type 073:  
XSETT.TRD.TR 
For record type 075: 
NSETT.TRD.TR 
[[settlement]] Date 45 52 8 N mmddccyy 
Debit Items 53 58 6 N 999,999 
Debit Share Quantity 59 73 15 N 99,999,999,999.9999 
Filler 74 100 27 A/N Space 
 
 

---

## Page 51

Fixed Length Record Layouts (Part 3) 
Settling Trade Trailer (071); X-[[settlement]] Trade Trailer (073); Settling Trade Trailer for TPA/Investment Agent/TPP (075) 51 
 
02.24.02 Settling Trade Trailer (071) 2 of 2 
Output from [[NSCC]] 
Record 2 of 2 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 02 
Filler 5 7 3 A/N Space 
Debit Money Amount  8 24 17 N 999,999,999,999,999.99 
Currency Indicator - Debit 25 27 3 A/N For record type 071/075:  
USD = Same day [[settlement]]  
USN = Next day [[settlement]]  
EUR or GBP 
For record type 073: 
Any currency code 
Credit Items 28 33 6 N 999,999 
Credit Share Quantity 34 48 15 N 99,999,999,999.9999 
Credit Money Amount 49 65 17 N 999,999,999,999.99 
Currency Indicator - Credit 66 68 3 A/N For record type 071/075:  
USD = Same day [[settlement]]  
USN = Next day [[settlement]]  
EUR or GBP 
For record type 073: 
Any currency code 
Filler 69 100 32 A/N Space 

---

## Page 52

Fixed Length Record Layouts (Part 3) 
Multiple Reject Codes (120) 52 
 
MULTIPLE REJECT CODES (120)  
02.25.01 Multiple Reject Codes (120) Record 1 of 1 
Output from [[NSCC]]. This record will be created by [[NSCC]] for each rejected transaction that has been 
rejected for more than one reason.  
When relating to ToRA (Transfer of Retirement [[Asset]]), Firm means Receiving Fund, and Fund means 
Delivering Fund.  
Record 1 of 1 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N N = [[NSCC]] 
Filler 6 7 2 A/N Space 
Firm Number 8 11 4 N  
Filler 12 14 3 A/N Space 
Record Type 15 17 3 A/N 120 = Multiple Reject Codes 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
Filler 19 19 1 A/N Space 
Fund Number 20 23 4 N  
Filler 24 26 3 A/N Space 
Security Issue Country 
Code 
27 28 2 A/N Space. For future use 
Security Issue [[ID]] 29 37 9 A/N  
Security Issue Check Digit 38 38 1 A/N Space. For future use 
Security Issue Type 39 40 2 A/N  
Control Number 41 55 15 A/N  
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction  
P = Post [[settlement]] correction/cancellation  
Space = No correction 
Original Record Type 57 59 3 A/N The rejected transaction record type 

---

## Page 53

Fixed Length Record Layouts (Part 3) 
Multiple Reject Codes (120) 53 
 
Record 1 of 1 
Field Name  
Start End Len Type Description  
[[NSCC]] Reject Code 2 60 62 3 A/N  
[[NSCC]] Reject Code 3 63 65 3 A/N  
[[NSCC]] Reject Code 4 66 68 3 A/N  
[[NSCC]] Reject Code 5 69 71 3 A/N  
[[NSCC]] Reject Code 6  72 74 3 A/N  
[[NSCC]] Reject Code 7  75 77 3 A/N  
[[NSCC]] Reject Code 8  78 80 3 A/N  
Filler  81 84 4 A/N Space 
TPA/Investment Agent/TPP 
Number 
85 88 4 A/N  
Service Provider Number  89 92 4 A/N  
Filler 93 100 8 A/N Space 

---

## Page 54

Fixed Length Record Layouts (Part 3) 
DataTrak Header 54 
 
DATATRAK HEADER 
02.26.01 DataTrak Header Record 1 of 1 
Required. This is the first record in any file submitted to Fund/SERV through DataTrak.  
Record 1 of 1 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Literal 1 1 5 5 A/N HDR.S R 
DataTrak Sysid 6 10 5 A/N System Identifier R 
Literal 2 11 12 2 A/N .E (period, E) R 
Literal 3 13 14 2 A/N ‘00’ R 
Literal 4  15 16 2 A/N .C (period, C) R 
Originator [[ID]] 17 20 4 A/N  R 
Literal 5 21 22 2 A/N ‘.S’ (period, S) R 
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

## Page 55

Fixed Length Record Layouts (Part 3) 
DataTrak Trailer 55 
 
DATATRAK TRAILER  
02.27.01 DataTrak Trailer Record 1 of 1 
Required. This is the last record in any file submitted to Fund/SERV through DataTrak.  
Record 1 of 1 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Literal 1 1 5 5 A/N END.S R 
DataTrak Sysid 6 10 5 A/N  R 
Literal 2 11 12 2 A/N .E (period, E) R 
Literal 3 13 14 2 A/N ‘00’ R 
Literal 4  15 16 2 A/N .C (period, C) R 
Originator [[ID]] 17 20 4 A/N Submitter R 
Literal 21 22 2 A/N .S R 
Sub Originator [[ID]]  23 26 4 A/N Submitted for [[Broker]] R 
Record Count 27 33 7 N 9,999,999  
Optional Field – Total # of records in file 
excluding DataTrak header and trailer 
R 
Filler 34 80 47 A/N Space R 

---

## Page 56

Fixed Length Record Layouts (Part 3) 
Firm Exit (139) 56 
 
FIRM EXIT (139) 
02.28.01 Firm Exit (139) Record 1 of 3 
Required  
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N A = Investment Agent 
B = Firm  
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 139 = Firm Exit  R 002 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code  
27 28 2 A/N Space. For future use R  
Security Issue [[ID]]  29 37 9 A/N  R 007 
Security Issue Check 
Digit  
38 38 1 A/N Space. For future use R  

---

## Page 57

Fixed Length Record Layouts (Part 3) 
Firm Exit (139) 57 
 
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Type  39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction  
P = Post [[settlement]] 
correction/cancellation  
Space = No correction 
R 006 
Filler 57 57 1 A/N Space R  
Transaction Code 58 59 2 A/N Required if Correction Indicator = 'P'.  
01 = Initial purchase  
02 = Subsequent purchase  
03 = Partial [[liquidation]]  
04 = Full [[liquidation]]  
05 = Full exchange  
06 = Partial exchange  
07 = Post settle correct/cancel 
purchase  
08 = Post settle correct/cancel 
[[liquidation]].  
07 and 08 are allowed only if 
Correction Indicator = P 
OC 018 
Submission Date 60 67 8 N mmddccyy R 101 
Trade Date 68 75 8 N mmddccyy O 037 
Filler 76 80 5 A/N Space R  

---

## Page 58

Fixed Length Record Layouts (Part 3) 
Firm Exit (139) 58 
 
Record 1 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Required if Originator Type = T or P 
or A or V 
OC 188 
Service Provider 
Number 
89 92 4 A/N Required if Originator Type = S or P OC 215 
Filler 93 100 8 A/N Space R  
 
 
  

---

## Page 59

Fixed Length Record Layouts (Part 3) 
Firm Exit (139) 59 
 
02.28.02 Firm Exit (139) Record 2 of 3 
Required  
Record 2 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Original Control 
Number 
8 22 15 A/N  O  
Original Correction 
Indicator 
23 23 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]]  
correction/cancellation  
Space = No correction 
O 164 
Customer Account 
Number at Firm 
24 43 20 A/N Required if Correction Indicator = P 
and Original Control Number is not 
provided and Original Customer 
Account Number at Fund is not 
provided. 
OC 020 
Customer Account 
Number at Fund 
44 63 20 A/N Required if Correction Indicator = P  
and Original Control Number is not 
provided  
and Original Customer Account 
Number at Firm is not provided. 
OC 011 Anticipated [[settlement]] 
Date 
64 71 8 A/N Input: Space  
Output: [[settlement]] Date mmddccyy 
R 180 
Standard [[ID]] 72 77 6 A/N  O  

---

## Page 60

Fixed Length Record Layouts (Part 3) 
Firm Exit (139) 60 
 
Record 2 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
As-Of Reason Code 78 79 2 A/N 01 = Incorrect Firm/Fund Account 
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
Filler 80 100 21 A/N Space R  
 
 
  

---

## Page 61

Fixed Length Record Layouts (Part 3) 
Firm Exit (139) 61 
 
02.28.03 Firm Exit (139) Record 3 of 3 
Required if Correction Indicator = ‘P’ and Original Control Number is not provided.  
Record 3 of 3 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Original Share 
Quantity 
8 21 14 N 9,999,999,999.9999  
Required if Correction Indicator = P  
and Original Control Number is not 
provided 
OC 019 
Original Money 
Amount 
22 37 16 N 99,999,999,999,999.99  
Required if Correction Indicator = P  
and Original Control Number is not 
provided 
OC 019 
Original Amount Due 38 53 16 N 99,999,999,999,999.99  
Required if Correction Indicator = P  
and Original Control Number is not 
provided 
OC 026 
Memo Field 54 73 20 A/N  O  
Filler 74 100 27 A/N Space R  

---

## Page 62

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 62 
 
CORRECTION (003); CORRECTION CONFIRMATION 
(025); POST [[settlement]] CORRECTION BY FUND (026) 
02.29.01 Correction (003) Record 1 of 14 
Required 
Record 1 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N A = Investment Agent 
B = Firm  
F = Fund 
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 003 = Correction  
025 = Correction Confirmation  
026 = Post [[settlement]] Correction 
by fund 
Record Type 026 not permitted if 
the Security Issue Type field value 
is 63 and [[settlement]] Override 
Reason Code field value is space 
RC 002/275 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  

---

## Page 63

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 63 
 
Record 1 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Country 
Code  
27 28 2 A/N Space. For future use R  
Security Issue [[ID]]  29 37 9 A/N  R 007 
Security Issue Check 
Digit  
38 38 1 A/N Space. For future use R  
Security Issue Type  39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file. [[NSCC]] leverages the 
Fund/SERV Security master file 
to determine value and 
associated processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction  
P = Post [[settlement]] 
correction/cancellation  
Must be P for record type 026  
P not permitted if the Security Issue 
Type field value is 63 and 
[[settlement]] Override Reason Code 
field value is space 
RC 006 

---

## Page 64

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 64 
 
Record 1 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Transaction Type 57 57 1 A/N 0 = Single purchase  
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
 
58 59 2 A/N 01 = Initial purchase  
02 = Subsequent purchase  
03 = Partial [[liquidation]]  
04 = Full [[liquidation]]  
07 = Post settle correct/cancel 
purchase  
08 = Post settle correct/cancel 
[[liquidation]].  
Must be 03 or 04 or 08 if 
Transaction Type = 5.  
07 and 08 allowed only if Correction 
Indicator = P. 
07 and 08 not permitted if the 
Security Issue Type field value is 63 
and [[settlement]] Override Reason 
Code field value is space 
 
For record type 003, 025 
For Security Type = 48 (Interval 
Fund) future dated orders, only 
03 and 04 are allowed. 
RC 018 
Submission Date 60 67 8 N mmddccyy R 101 

---

## Page 65

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 65 
 
Record 1 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Trade Date 
 
 
68 75 8 N mmddccyy 
 
For record type 003, 025 
Future trade date is allowed if 
Security Type = 48 (Interval 
Fund) and Transaction Code = 03 
(Partial [[liquidation]]) or 04 (Full 
[[liquidation]]). 
 
Best Practice: 
Trade Date for future dated 
Interval Fund repurchase orders 
should be populated with the 
Repurchase Pricing Date 
communicated by the Fund. 
R 016 
Book/Physical Share 
Indicator 
76 76 1 A/N 0 = Book [[shares]] - firm name  
1 = Book [[shares]] - customer name  
2 = Physical [[shares]]  
3 = Both book and physical [[shares]]  
Must be 0 or 1 for Money Market 
trades 
R 015 
PI Delivery Indicator 77 77 1 A/N Required for all purchases if 
Book/Physical Share Ind = 2.  
0 = Deliver to customer  
1 = Deliver to firm  
2 = Deliver to agent for firm 
OC 039 Filler 78 78 1 A/N Space R  

---

## Page 66

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 66 
 
Record 1 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[settlement]] Override 
Reason Code 
79 80 2 A/N Required (but must not be 04) if 
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
Must be space for settling EUR and 
GBP transactions (Security Issue 
Type 63 only). 
OC 179 
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Required if: 
Originator Type = (T or P or A or V)  
OR  
Membership Identifier = 02 or 03 
 
If Originator Type = T or P, then 
[[Asset]] Type Indicator must be F 
through O, or S or T  
(indicating DCC&S) 
OC 188 
Service Provider Number 89 92 4 A/N Required if Originator Type = S or P OC 215 
SSN/EIN Start Sequence 
Number 
93 94 2 A/N See SSN/EIN Start Sequence 
Number in the Introduction section. 
Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 257 

---

## Page 67

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 67 
 
Record 1 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Total SSN/EIN Records 95 96 2 N Required if SSN/EIN Suffix is 
provided. Not allowed otherwise.  
OC 258 
Filler 97 100 4 A/N Space R  
 
 
  

---

## Page 68

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 68 
 
02.29.02 Correction (003) Record 2 of 14 
Required 
Record 2 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Share Quantity 8 21 14 N 9,999,999,999.9999  
Optional for record type 003 if full 
[[liquidation]] or if Money Amount > 0 
RC 019 
Customer Account 
Number at Firm 
22 41 20 A/N Optional if [[settlement]] Override 
Reason Code = 04, 06 OR if 
Membership Identifier is provided. 
RC 020 
Fund Account Indicator 42 42 1 A/N 0 = New account – U.S.  
1 = New account – non-U.S. 
2 = Existing account – U.S.  
3 = Existing account – non-U.S.  
4 = New account – U.S. Tax Resident 
Living Abroad  
5 = Existing account – U.S. Tax 
Resident Living Abroad  
R 010 
Customer Account 
Number at Fund 
43 62 20 A/N Required for all non-networked 
liquidations  
(Network Control Ind = 0 and Trans 
Code = 03, 04 or 08) 
OC 011 
[[Asset]] Type Indicator 63 63 1 A/N 0 = Not applicable  
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
R 013 

---

## Page 69

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 69 
 
Record 2 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
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
L = Omnibus [[Dividend]] Reconciliation 
M = Variable Annuity 
N = Wrap Program 
O = Defined Benefit Plan 
P = 529 Previous Year Contribution 
Q = 529 Current Year Contribution  
S = Omnibus Short-Term Capital Gain 
Reconciliation 
T = Omnibus Long-Term Capital Gain 
Reconciliation 
U = 529 In – State Plan Transfer 
Contribution 
V = 529 Owner Change 
W = 529 Beneficiary Change-In-
Family  
Note: 
D, P, Q, U, V and W indicate Section 
529 Plan. 
Agent for Firm Number 64 67 4 A/N Required if Originator Type = V (TPP). OC 271 
Network Control 
Indicator  
68 68 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Fraction Indicator 69 69 1 A/N 0 = Round up  
1 = Round down  
2 = Issue fraction  
3 = Not applicable 
R 014 

---

## Page 70

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 70 
 
Record 2 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Gross [[settlement]] 
Indicator 
70 70 1 A/N 0 = Not applicable  
1 = Settle net  
2 = Settle gross 
R 094 
Transaction Received 
Time 
71 76 6 N hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = ‘F’ (Fund). 
 
Record Type 025: 
Must contain the same value as 
provided by the firm on the Correction 
transaction (record type 003). [[NSCC]] 
will reject if a fund provided value is 
different from the value submitted by 
the firm. 
OC 168 
Membership Identifier 77 78 2 A/N 01 = Trust [[Member]]  
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 79 79 1 A/N  R  
Transaction Payment 
Type Indicator 
80 80 1 A/N Required if [[settlement]] Override 
Reason Code = 04.  
1 = Shareholder wire  
2 = Shareholder ACH  
3 = Address of Record (AOR).  
3 allowed for [[liquidation]] (Transaction 
Code = 03 or 04) only 
OC 216 
Transaction Bank 
Account Number 
81 100 20 A/N required if Transaction Payment Type 
Indicator = 1 or 2 
OC 142 
 
 
  

---

## Page 71

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 71 
 
02.29.03 Correction (003) Record 3 of 14 
Required 
Record 3 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Money Amount 8 23 16 N 99,999,999,999,999.99  
Optional for record type 003 if full 
[[liquidation]]  
or if Share Quantity > 0 
RC 019 
Currency Indicator 24 26 3 A/N  O 110 
Anticipated [[settlement]] 
Date 
 
 
27 34 8 A/N mmddccyy  
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
[[liquidation]]) or 04 (Full [[liquidation]]). If 
populated, [[NSCC]] will [[default]] the 
value to 12319999 and pass the order 
to the Fund. 
OC 180 
Branch Identification 
Number 
35 43 9 A/N Optional under the following 
conditions: 
• Membership Identifier = 01 or 02, 
and Agent for Firm Number is not 
provided. 
• Originator Type = V (TPP) 
RC 035 

---

## Page 72

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 72 
 
Record 3 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Related Trade Indicator 44 44 1 A/N 0 = No  
1 = Yes 
R 065 
Related Trade Identifier 45 46 2 A/N Required if Related Trade Indicator = 
1 
OC 105 
Customer Name 47 66 20 A/N  R 063 
SSN/EIN Indicator 67 67 1 A/N 0 = Tax [[ID]] number  
1 = Social security number  
2 = [[investor]] TIN/EIN 
R 102 
SSN/EIN Number 68 76 9 A/N  R 103 
[[liquidation]] Indicator 77 77 1 A/N Required if Trans Type = 5.  
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
Note: 
4 through B should apply only to 
transactions with CDSC Waiver  
C = 529 Plan-Specific 
D = 529 Plan Account - Beneficiary 
Disability 
E = 529 Plan Account – Beneficiary 
Death 
F = 529 Plan Account – Beneficiary 
Scholarship 
 
Notes: 
• 4 through F should apply only to 
transactions with CDSC Waivers 
• C through F should only apply to 
Section 529 plans. 
OC 046 

---

## Page 73

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 73 
 
Record 3 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
NAV Reason Code  78 78 1 A/N Required if Trans Type = 3.  
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
9 = Section 529 Account - Qualified 
State Tuition Program  
A = [[Dividend]] reinvestment trade  
B = Trust Company NAV per 
Agreement 
C = Refer to [[Asset]] Type Indicator  
D = Deminimis Amount Processed at 
NAV  
E = Self Directed Brokerage Account 
OC 104 
State of Sale (State 
Code) 
79 80 2 A/N Required for Transaction Codes 
 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 012 
Redemption Fee 
Indicator  
81 81 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee 
3 = Money Market [[Liquidity]] Fee with 
CDSC 
 
Values “0” and “1” are not allowed for 
record type 025 if this field was blank 
on the original Correction transaction 
(record type 003). 
 
Values “2” and “3” are allowed for 
record type 025 if this field was blank 
on the original Correction transaction 
(record type 003). 
O 248 

---

## Page 74

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 74 
 
Record 3 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Short-Term Redemption 
Fee Waiver Indicator 
82 82 1 A/N 1 = STR waiver due to correction  
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
G = Divorce/QDRO 
H = Plan fees QDRO 
O 249 
Filler 83 83 1 A/N Space R  
Correction Type Indicator 84 84 1 A/N 0 = Not applicable  
1 = Correction only  
2 = Correction 3 = Rebill 
O 108 

---

## Page 75

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 75 
 
Record 3 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Correction Reason Code 85 86 2 A/N 01 = Incorrect Firm/Fund Account 
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
Note: 
The values ‘00’, ‘06’ and ‘08’ have 
been removed. 
R 109 
Transaction ABA Routing 
Number 
87 95 9 A/N Required if Transaction Payment 
Type Indicator = 1 or 2 
OC 141 
De-minimis repurchase 
waiver code 
 
96 96 1 A/N For record type 003  
blank or 0 = No; 
1 = Yes 
 
Allows Firms to indicate if an Interval 
Fund repurchase order is eligible for 
de-minimis treatment in accordance 
with the Fund’s prospectus. 
 
Should only be populated for an 
Interval Fund. 
O 286 
Filler 97 98 2 A/N Space R  

---

## Page 76

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 76 
 
Record 3 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Omnibus Account 
Indicator 
99 99 1 A/N 0 = Not Omnibus Account  
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
100 100 1 A/N 0 = Trade Date not forwarded  
1 = Trade Date forwarded  
2 = Trade Date being corrected  
For record type 003:  
a. Must be 2 if Trade Date not equal 
Trade Date on order.  
b. Must be 1 if Trade Date equal 
Trade Date on order and Trade Date 
on order is forwarded.  
c. Must be 0 if Trade Date equal 
Trade Date on order and Trade Date 
on order is not forwarded. 
 
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
 
 
  

---

## Page 77

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 77 
 
02.29.04 Correction (003) Record 4 of 14 
Required if any of the following fields in this record are required: 
• Sales Charge Rate  
• Country of Origin (Record Type 003) 
• IRA/529 [[liquidation]] Indicator 
• Periodic Frequency Indicator  
• Beneficiary SSN/EIN Number 
• Social Code (when “Transaction Code”-01) 
Record 4 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 04 R 004 
Filler 5 7 3 A/N Space R  
Related Account 
Number 
8 27 20 A/N  O  
Related Account 
Number Indicator 
28 28 1 A/N Required if Related Account Number 
is provided.  
1 = Fund  
2 = Firm  
3 = Customer 
OC 157 
Related Account 
Security Issue Country 
Code 
29 30 2 A/N Space. For future use R  
Related Account 
Security Issue [[ID]] 
31 39 9 A/N Required if Related Account Number 
is provided 
OC 107 
Related Account 
Security Issue Check 
Digit 
40 40 1 A/N Space. For future use R  
Country of Origin 
(Country Code) 
41 42 2 A/N Required for non-omnibus account 
(Omnibus Account Indicator = ‘0’ or 
space) if State of Sale (State Code) = 
‘FF’ 
OC 067 
Sales Charge Rate 43 46 4 A/N 9.999  
Must be provided (but allowed to be 
zero) for purchase (Transaction Code 
= '01', '02' or '07') if Load Type 
Indicator = 1 
OC 025 

---

## Page 78

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 78 
 
Record 4 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
ROA/LOI Value 47 62 16 N 99,999,999,999,999.99 O 064 
LOI Number/Date 63 70 8 A/N  O  
IRA/529 [[liquidation]] 
Indicator 
71 71 1 A/N 0 = Not applicable  
1 = Distribution - premature  
2 = Distribution - disability  
3 = Distribution - death  
4 = Distribution - normal  
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
A = (529 School Distribution)  
C is required if Transaction Type = E 
(529 In-State Plan Transfer 
Distribution) 
D or E is required if Transaction Type 
= F (529 Registration Change) 
OC 106 
Short [[settlement]] 
Indicator 
72 72 1 A/N 0 = Not applicable  
1 = Short due to correction 
O 169 

---

## Page 79

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 79 
 
Record 4 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Periodic Frequency 
Indicator 
73 73 1 A/N Required if [[liquidation]] Indicator = 8 or 
Program Transaction Indicator = 1.  
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
74 81 8 N mmddccyy  
For 529 use this field for Beneficiary 
Date of Birth 
O 204 
Social Code 82 83 2 A/N Required when “Transaction 
Code” = 01 – Initial Purchase 
See Social Code List at 
https://dtcclearning.com/documents/m
utual-fund-services-1/mfs-cross-
product/codes-8/2498-social-
codes/file.html under General Codes. 
OC 128 
Beneficiary SSN/EIN 
Number 
84 92 9 A/N Required if [[Asset]] Type Indicator = D, 
E, P, U, V, or W and Transaction 
Code = 01 or 02 
 
[[Asset]] Type Indicators 
D (529 Current Year Contribution)  
E (UGMA account transferred to 
Section 529 Account)  
P (529 Previous Year Contribution) 
Q (529 Rollover Contribution)  
U (529 In – State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-  
In-Family) 
 
Transaction Codes 
01 (Initial purchase) 
02 (Subsequent purchase) 
OC 103 

---

## Page 80

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 80 
 
Record 4 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Beneficiary SSN/EIN 
Indicator 
93 93 1 A/N Required if Beneficiary SSN/EIN 
Number is provided.  
0 = Tax [[ID]] number  
1 = Social security number  
2 = Beneficiary TIN/EIN 
OC 102 Standard [[ID]] 94 99 6 A/N  O  
Program Transaction 
Indicator 
100 100 1 A/N 1 = Systematic Withdrawal Plan 
(SWP) 
2 = Target Date Fund [[liquidation]]  
3 = Systematic Contribution 
(SIP/PAC/PIP) 
4 = Rebalance Purchase (Systematic) 
5 = Rebalance Redemption 
(Systematic) 
O 259 
 
 
  

---

## Page 81

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 81 
 
02.29.05 Correction (003) Record 5 of 14 
Optional  
Record 5 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 05 R 004 
Filler 5 7 3 A/N Space R  
Account 
Representative 
Number 
8 16 9 A/N  O  
Account 
Representative Name 
17 31 15 A/N  O  
Confirm Number 32 43 12 A/N  O  
Filler 44 55 12 A/N  R  
IRA Withholding 
Percentage 
56 60 5 N 99.999 O 158 
Non-Taxable 
Percentage 
61 65 5 N 99.999 O 159 
Non-Taxable Money 
Amount 
66 81 16 N 99,999,999,999,999.99 O 160 
Closeout Fee Indicator 82 82 1 A/N 0 = [[DO]] not deduct  
1 = Deduct 
O 161 
LOI Indicator 83 83 1 A/N 0 = New  
1 = Existing 
O 162 
Original Control 
Number 
84 98 15 A/N  O  

---

## Page 82

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 82 
 
Record 5 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original Correction 
Indicator 
99 99 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation  
Space = No correction 
P not permitted if the Security Issue 
Type field value is 63 and [[settlement]] 
Override Reason Code field value is 
space 
O 164 
Filler 100 100 1 A/N Space R  
 
 
  

---

## Page 83

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 83 
 
02.29.06 Correction (003) Record 6 of 14 
Required for record types 025 and 026. Optional for record type 003.  
Record 6 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 06 R 004 
Filler 5 7 3 A/N Space R  
Withholding Amount 8 23 16 N 99,999,999,999,999.99 O 113 
Withholding Type 24 24 1 A/N Required if Withholding Amount > 0.  
1 = Tefra backup  
2 = Tefra pension  
3 = Foreign withholding 
OC 114 
Fee Amount 25 32 8 N 999,999.99 O 115 
Fee Type 33 33 1 A/N Required if Fee Amount > 0.  
1 = [[liquidation]] fee  
2 = Other 
OC 116 
Amount Due 34 49 16 N 99,999,999,999,999.99  
Optional for record type 003.  
This amount will be settled by [[NSCC]] 
RC 026 
Price Per Share 50 61 12 N 999999.999999  
Optional for record type 003 
RC 027 
Loss/Gain Amount 62 69 8 N 999,999.99 O 031 
Loss/Gain Indicator 70 70 1 A/N Required if Loss/Gain Amount > 0.  
0 = Loss  
1 = Gain 
OC 117 
Firm Concession 71 79 9 N 9,999,999.99 O 044 
Accrual Amount 80 95 16 N 99,999,999,999,999.99 O 111 
Accrual Indicator 96 96 1 A/N Required if Accrual Amount > 0.  
0 = Included in Amount Due  
1 = Paid via Cash Adjustment  
2 = Paid outside system 
OC 112 

---

## Page 84

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 84 
 
Record 6 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Debit/Credit Indicator 97 98 2 A/N Required for record type 026.  
Required for record type 025 if 
Correction Indicator = P.  
Not allowed otherwise.  
DB = Debit firm  
CR = Credit firm  
NS = No [[settlement]] (Amount Due 
must be zero)  
[[NSCC]] will settle Amount Due 
according to this indicator rather than 
Transaction Code. 
OC 034 
Breakpoint Change 
Reason Code 
99 99 1 A/N 1 = ROA value at fund  
2 = LOI at fund  
3 = The higher of cost or market value 
at fund  
4 = Jumbo Pricing  
5 = Wrap Account  
6 = NAV Account 
7 = Amount Processed at NAV  
O 246 
Load Type Indicator 100 100 1 A/N 0 = Other  
1 = Front-End Load  
Required for record types 025 and 
026 if purchase (Transaction Code = 
‘01’, ‘02’ or ’07’). 
OC 247  
 
  

---

## Page 85

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 85 
 
02.29.07 Correction (003) Record 7 of 14 
Required when Redemption Fee Indicator is provided or [[Asset]] Type Indicator = Q, U, V or W.  
Optional for all other [[Asset]] Types.  
Record 7 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 07 R 004 
Filler 5 7 3 A/N Space R  
Redemption Fee Rate 8 14 7 N 99.99999 
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required and “Redemption 
Fee Indicator”= ‘2’ or ‘3’. 
 
If “Redemption Fee Indicator” = 0 or 
1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Rate. 
OC 250 

---

## Page 86

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 86 
 
Record 7 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
STR Fee Share 
Quantity  
15 28 14 N 9,999,999,999.9999 
 
For all record types: 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record type 003: 
Required when “Redemption Fee 
Indicator” is provided and 
“Redemption Fee Money Amount” = 
0 or Space. 
 
For record type 025: 
If zero or Space, and “Redemption 
Fee Indicator” is provided, will not 
override the “STR Fee Share 
Quantity” in the database. 
 
For all record types: 
Not allowed when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
OC 251 

---

## Page 87

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 87 
 
Record 7 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Redemption Fee 
Money Amount  
29 44 16 N 99,999,999,999,999.99 
 
For all record types: 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record type 003: 
Required when “Redemption Fee 
Indicator” is provided and “STR Fee 
Share Quantity” = 0 or Space. 
 
For record type 025: 
Required when “Redemption Fee 
Indicator “is provided. 
 
For all record types: 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required. 
 
If “Redemption Fee Indicator” = 0 or 
1, this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Money 
Amount.  
OC 252 
Cost Basis Money 
Amount  
45 60 16 N Required if the [[Asset]] Type Indicator 
= Q, U, V or W. 
Q (529 Rollover Contribution)  
U (529 In – State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-
Family) 
Format:  
99,999,999,999,999.99 
Zeros are allowed 
OC 261 

---

## Page 88

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 88 
 
Record 7 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Earnings to Date 
Money Amount 
61 76 16 N Required if the [[Asset]] Type Indicator 
= Q, U, V or W. 
Q (529 Rollover Contribution)  
U (529 In – State Plan Transfer 
Contribution) 
V (529 Owner Change) 
W (529 Beneficiary Change-In-
Family) 
Format:  
99,999,999,999,999.99  
Zeros are allowed 
OC 262 
Negative Earnings to 
Date Indicator 
77 77 1 A/N N = Negative  
Spaces = Positive  
O 263 
Money Market 
[[Liquidity]] 
Fee/Redemption Gate 
Indicator  
78 78 1 A/N F = Fund.  
B = [[intermediary]] 
 
For record type 025: 
Must contain the same value as 
provided on the Correction 
transaction (record type 003). [[NSCC]] 
will reject if a fund provided value is 
different from the value submitted by 
the firm. 
O 282 
Transaction Received 
Date  
79 86 8 A/N mmddccyy 
 
Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
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

## Page 89

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 89 
 
Record 7 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject Code 
Aggregated Order 
Indicator  
87 87 1 A/N Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = “F” or “B”. 
• 1 = Transactions are not 
aggregated  
• 2 = Transactions are aggregated 
by “like” orders (purchases 
separate from redemptions) 
• 3 = Transactions are net of 
purchases and redemptions 
• 4 = Unknown at time of 
placement 
 
For record type 025: 
Must contain the same value as 
provided on the Correction 
transaction (record type 003). [[NSCC]] 
will reject if a fund provided value is 
different from the value submitted by 
the firm. 
OC 284 
Filler 88 100 13 A/N Space R  
 
 
  

---

## Page 90

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 90 
 
02.29.08 Correction (003) Record 8 of 14 
Required if Correction Indicator = ‘P’ and Original Control Number is not provided.  
Record 8 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 08 R 004 
Filler 5 7 3 A/N Space R  
Original Customer 
Account Number at 
Firm 
8 27 20 A/N Required if all the following occur:  
• Correction Indicator = P 
• Original Control Number is not 
provided 
• Original Customer Account 
Number at Fund is not provided 
OC 020 
Original Customer 
Account Number at 
Fund 
28 47 20 A/N Required if all the following occur:  
• Correction Indicator = P 
• Original Control Number is not 
provided 
• Original Customer Account 
Number at Firm is not provided 
OC 011 
Memo Field 48 67 20 A/N  O  
Filler 68 100 33 A/N Space R  
 
 
  

---

## Page 91

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 91 
 
02.29.09 Correction (003) Record 9 of 14 
Required if Correction Indicator = ‘P’ and Original Control Number is not provided.  
Record 9 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 09 R 004 
Filler 5 7 3 A/N Space R  
Original Share 
Quantity 
8 21 14 N 9,999,999,999.9999  
Required if Correction Indicator = P 
and Original Control Number is not 
provided 
OC 019 
Original Money 
Amount 
22 37 16 N 99,999,999,999,999.99  
Required if Correction Indicator = P 
and Original Control Number is not 
provided 
OC 019 
Original Amount Due 38 53 16 N 99,999,999,999,999.99  
Required if Correction Indicator = P 
and Original Control Number is not 
provided 
OC 026 
Original Price Per 
Share 
54 65 12 N 999,999.999999  
Required if Correction Indicator = P 
and Original Control Number is not 
provided 
OC 027 
Filler 66 100 35 A/N Space R  
 
 
  

---

## Page 92

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 92 
 
02.29.10 Correction (003) Record 10 of 14 
Optional 
Record 10 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 10 R 004 
Filler 5 7 3 A/N Space R  
Original Transaction 
Type  
8 8 1   O 017 
Original Transaction 
Code 
9 10 2   O 018 
Original Book/Physical 
Share Indicator 
11 11 1   O 015 
Original PI Delivery 
Indicator 
12 12 1   O 039 
Original [[settlement]] 
Override Reason Code 
13 14 2   O 179 
Original Fund Account 
Indicator 
15 15 1   O 010 
Original [[Asset]] Type 
Indicator 
16 16 1   O 013 
Original Agent for Firm 
Number 
17 20 4   O  
Original Network 
Control Indicator 
21 21 1   O 047 
Original Fraction 
Indicator 
22 22 1   O 014 
Original Gross 
[[settlement]] Indicator 
23 23 1   O 094 
Original Membership 
Identifier 
24 25 2   O 181 
Original [[settlement]] 
Date 
26 33 8  mmddccyy O 180 
Original Branch 
Identification Number 
34 42 9   O 035 

---

## Page 93

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 93 
 
Record 10 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original Related Trade 
Indicator 
43 43 1   O 065 
Original Related Trade 
Identifier 
44 45 2   O 105 
Original Customer 
Name 
46 65 20   O 063 
Original SSN/EIN 
Indicator 
66 66 1 A/N  O 102 
Original SSN/EIN 
Number 
67 75 9 A/N  O 103 
Original [[liquidation]] 
Indicator 
76 76 1 A/N  O 046 
Original NAV Reason 
Code 
77 77 1 A/N  O 104 
Original State of Sale 
(State Code) 
78 79 2 A/N  O 012 
Original Correction 
Type Indicator 
80 80 1 A/N  O 108 
Original Correction 
Reason Code 
81 82 2 A/N  O 109 
Filler 83 100 18 A/N Space R  
 
 
  

---

## Page 94

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 94 
 
02.29.11 Correction (003) Record 11 of 14 
Optional 
Record 11 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 11 R 004 
Filler 5 7 3 A/N Space R  
Original Related 
Account Number 
8 27 20 A/N  O  
Original Related 
Account Number 
Indicator 
28 28 1 A/N  O 157 
Original Related 
Account Security Issue 
Country Code 
29 30 2 A/N  O  
Original Related 
Account Security Issue 
[[ID]] 
31 39 9 A/N  O 107 
Original Related 
Account Security Issue 
Check Digit 
40 40 1 A/N  O  
Original Country of 
Origin (Country Code) 
41 42 2 A/N  O  
Original Sales Charge 
Rate 
43 46 4 N 9.999 O 025 
Original ROA/LOI 
Value 
47 62 16 N 99,999,999,999,999.99 O 064 
Original LOI 
Number/Date 
63 70 8 A/N  O  
Original IRA/529 
[[liquidation]] Indicator 
71 71 1 A/N  O 106 
Original Short 
[[settlement]] Indicator 
72 72 1 A/N  O 169 

---

## Page 95

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 95 
 
Record 11 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Original Periodic 
Frequency Indicator 
73 73 1 A/N  O 083 
Filler 74 100 27 A/N Space R  
 
 
  

---

## Page 96

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 96 
 
02.29.12 Correction (003) Record 12 of 14 
Optional 
Record 12 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 12 R 004 
Filler 5 7 3 A/N Space R  
Original Account 
Representative 
Number 
8 16 9 A/N  O  
Original Account 
Representative Name 
17 31 15 A/N  O  
Original Confirm 
Number 
32 43 12 A/N  O  
Original IRA 
Withholding 
Percentage 
44 48 5 N 99.999 O 158 
Original Non-Taxable 
Percentage 
49 53 5 N 99.999 O 159 
Original Non-Taxable 
Money Amount 
54 69 16 N 99,999,999,999,999.99 O 160 
Original Closeout Fee 
Indicator 
70 70 1 A/N  O 161 
Original LOI Indicator 71 71 1 A/N  O 162 
Filler 72 100 29 A/N Space R  
 
 
  

---

## Page 97

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 97 
 
02.29.13 Correction (003) Record 13 of 14 
Optional 
Record 13 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 13 R 004 
Filler 5 7 3 A/N Space R  
Original Withholding 
Amount 
8 23 16 N 99,999,999,999,999.99 O 113 
Original Withholding 
Type 
24 24 1 A/N  O 114 
Original Fee Amount 25 32 8 N 999,999.99 O 115 
Original Fee Type 33 33 1 A/N  O 116 
Original Loss/Gain 
Amount 
34 41 8 N 999,999.99 O 031 
Original Loss/Gain 
Indicator 
42 42 1 A/N  O 117 
Original Firm 
Concession 
43 51 9 N 9,999,999.99 O 044 
Original Accrual 
Amount 
52 67 16 N 99,999,999,999,999.99 O 111 
Original Accrual 
Indicator 
68 68 1 A/N  O 112 
Filler 69 100 32 A/N Space R  
 
 
  

---

## Page 98

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 98 
 
02.29.14 Correction (003) Record 14 of 14 
Optional 
Record 14 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 14 R 004 
Filler 5 7 3 A/N Space R  
[[intermediary]] Program  
Indicator – 1 
8 11 4 A/N Indicates the program, platform, or 
channel applicable to an account.  
Examples may include: 
• Program indicator for advisory 
accounts 
• Distribution channel applicable to 
the account (e.g., retail, RIA, etc.) 
• Retirement platform pertaining to 
the account 
Values are uniquely defined by each 
[[intermediary]]. 
O  
[[intermediary]] Program  
Indicator – 2 
12 15 4 A/N Further defines the program, platform, 
or channel applicable to an account.  
Values are uniquely defined by each 
[[intermediary]].  
O  
Servicing Group [[ID]] 16 24 9 A/N This field is used to communicate 
aggregated servicing relationships or 
define additional relationships on 
accounts. 
Examples may include: 
• Consolidating (Super) Branches 
• Third-party administrators (TPAs) 
• Investment Advisers 
• Consultants 
This field does not replace the main 
branch field on the account.  
Values are uniquely defined by each 
[[intermediary]]. 
O  
Additional Relationship  
[[ID]] – 1 
25 44 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts.  
Values are uniquely defined by each 
[[intermediary]].  
O  

---

## Page 99

Fixed Length Record Layouts (Part 3) 
Correction (003); Correction Confirmation (025); Post [[settlement]] Correction by Fund (026) 99 
 
Record 14 of 14 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Additional Relationship  
[[ID]] – 2 
45 64 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts.  
Values are uniquely defined by each 
[[intermediary]].  
O  
Filler 65 100 36 A/N Space R  

---

## Page 100

Fixed Length Record Layouts (Part 3) 
SSN/EIN Suffix Record 1 of 1 100 
 
SSN/EIN SUFFIX RECORD 1 OF 1 
02.30.01 SSN/EIN Suffix Record 1 of 1 
Optional 
Rules: 
This suffix contains a list of SSN/EIN Numbers and SSN/EIN Indicators.  
The suffix (as its name suggests) can be submitted only as a suffix to a submitted record type as Order (001), 
As-Of order (004), etc. It cannot be submitted independently. 
Up to 11 records are allowed in one suffix (up to 99 SSN/EIN Numbers and Indicators).  
The physical sequence number of the first record in an SSN/EIN suffix is one more than the physical sequence 
number of the last submitted record of the item being suffixed (but see item 6 below). 
The physical sequence number of each record after the first one is one more than the physical sequence 
number of the previous record (but see item 6 below). 
The first digit of the physical sequence number of the last record of the suffix is 9.  
Note: 
The first digit of the physical sequence number of the last record of the item being suffixed is NOT 9, since it’s followed by 
the suffix and is not regarded as the last record of the whole transaction.  
The logical sequence number of the first record in an SSN/EIN suffix is one more than the logical sequence 
number of the last submitted record of the item being suffixed (see examples in item SSN/EIN Start Sequence 
Number in the Introduction section). 
The logical sequence number of each record after the first one is one more than the logical sequence number 
of the previous record. 
All SSN/EIN records in a transaction, except the last one, must contain 9 SSN/EIN numbers and indicators.  
The last SSN/EIN record in a transaction can contain less than 9 SSN/EIN numbers and indicators, but they 
must be presented in a row without Space in between. 
Example:  
To submit 12 SSN/EIN numbers and indicators, the suffix should contain two records as follows: 
• The first record must have 9 SSN/EIN numbers and indicators 
• The second record must have SSN/EIN numbers and indicators 1, 2 and 3. The rest of this record must be Space. 
Record 1 of 1 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N Previous Logical Sequence Number + 
1 
R 004 
Filler 5 7 3 A/N Space R  

---

## Page 101

Fixed Length Record Layouts (Part 3) 
SSN/EIN Suffix Record 1 of 1 101 
 
Record 1 of 1 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
SSN/EIN Indicator 1 8 8 1 A/N Required if SSN/EIN Number 1 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 1 9 17 9 A/N  O 103 
SSN/EIN Indicator 2 18 18 1 A/N Required if SSN/EIN Number 2 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 SSN/EIN Number 2 19 27 9 A/N  O 103 
SSN/EIN Indicator 3 28 28 1 A/N Required if SSN/EIN Number 3 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 3 29 37 9 A/N  O 103 
SSN/EIN Indicator 4 38 38 1 A/N Required if SSN/EIN Number 4 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 4 39 47 9 A/N  O 103 
SSN/EIN Indicator 5 48 48 1 A/N Required if SSN/EIN Number 5 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 SSN/EIN Number 5 49 57 9 A/N  O 103 
SSN/EIN Indicator 6 58 58 1 A/N Required if SSN/EIN Number 6 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 

---

## Page 102

Fixed Length Record Layouts (Part 3) 
SSN/EIN Suffix Record 1 of 1 102 
 
Record 1 of 1 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
SSN/EIN Number 6 59 67 9 A/N  O 103 
SSN/EIN Indicator 7 68 68 1 A/N Required if SSN/EIN Number 7 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 
SSN/EIN Number 7 69 77 9 A/N  O 103 
SSN/EIN Indicator 8 78 78 1 A/N Required if SSN/EIN Number 8 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 SSN/EIN Number 8 79 87 9 A/N  O 103 
SSN/EIN Indicator 9 88 88 1 A/N Required if SSN/EIN Number 9 is 
provided. Not allowed otherwise. 
0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
OC 102 SSN/EIN Number 9 89 97 9 A/N  O 103 
Invalid Field Indicator 98 98 1 A/N Input: Space 
Output: Indicates whether a field in 
this record is invalid when the record 
is rejected by [[NSCC]]. 
0 = All fields are valid 
1 = SSN/EIN Indicator invalid 
2 = SSN/EIN Number invalid 
Space = Suffix not verified (may 
happen when the suffixed item is 
rejected for other reasons)  
R  

---

## Page 103

Fixed Length Record Layouts (Part 3) 
SSN/EIN Suffix Record 1 of 1 103 
 
Record 1 of 1 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Invalid Field Number 99 99 1 A/N Input: Space 
Output: Indicates which field in this 
record is invalid when the record is 
rejected by [[NSCC]]. 
0 = All fields in this record are valid 
1-9 = Invalid field number in this 
record 
Space = Suffix not verified (may 
happen when the suffixed item is 
rejected for other reasons) 
R  
Filler 99 100 1 A/N Space R  

---

## Page 104

Fixed Length Record Layouts (Part 3) 
Interval Fund Acknowledgement (030) 104 
 
INTERVAL FUND ACKNOWLEDGEMENT (030)  
02.31.01 Acknowledgement (030) Record 1 of 2  
This record is optional and only allowed for acknowledging an Order (001) or Correction (003) when: 
Security Type = 48 (Interval Fund) AND Transaction Type = ‘03 - Partial [[liquidation]]’ or ’04 – Full 
[[liquidation]]’. 
If submitted, both Sequence 1 and 2 are required.  
RECORD 1 OF 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N F = Fund  R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N [[NSCC]] will reject if value does not match 
Order (001) or Correction (003). 
R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 030 = Interval Fund Acknowledgment R 002 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N If populated must match value on Order 
(001) or Correction (003). 
O 100 
Filler 24 26 3 A/N Space R  
Security Issue 
Country Code  
27 28 2 A/N Space. For future use R  
Security Issue [[ID]]  29 37 9 A/N [[NSCC]] will reject if value does not match 
Order (001), or Correction (003). 
R 007 
Security Issue Check 
Digit  
38 38 1 A/N Space. For future use R  

---

## Page 105

Fixed Length Record Layouts (Part 3) 
Interval Fund Acknowledgement (030) 105 
 
RECORD 1 OF 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Type  39 40 2 A/N Notes: 
[[NSCC]] does not validate the value 
against the Fund/SERV Security master 
file. [[NSCC]] leverages the Fund/SERV 
Security master file to determine value 
and associated processing rules. 
Output: [[NSCC]] populates with the value 
in the Fund/SERV Security master file. 
O  
Control Number 41 55 15 A/N [[NSCC]] will reject if value does not match 
Order (001), or Correction (003). 
R 005 
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction 
 
Space = No correction 
 
Best Practice: 
• Populate when acknowledging a 
Correction (003). Value must match 
latest correction indicator. 
• [[DO]] not populate when 
acknowledging an Order (001). 
R 006 
Filler 57 57 1 A/N Space R  
Transaction Code 58 59 2 A/N 03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
R 018 
Submission Date 60 67 8 N mmddccyy R 101 
Trade Date 68 75 8 N mmddccyy  
 
[[NSCC]] will reject if value does not match 
Order (001), or Correction (003). 
R 016 
Filler 76 80 5 A/N Space R  
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple errors 
R  

---

## Page 106

Fixed Length Record Layouts (Part 3) 
Interval Fund Acknowledgement (030) 106 
 
RECORD 1 OF 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  
Filler 85 100 16 A/N Space R  
 
 
  

---

## Page 107

Fixed Length Record Layouts (Part 3) 
Interval Fund Acknowledgement (030) 107 
 
02.31.01 Acknowledgement (030) Record 2 of 2 
Record 2 of 2  
Field Name  
Start End Length Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Customer Account 
Number at Firm 
8 27 20 A/N Required if ‘Customer Account 
Number at Fund’ field is not 
populated. 
RC 020 
Customer Account 
Number at Fund 
28 47 20 A/N Required if ‘Customer Account 
Number at Firm’ field is not 
populated. 
RC 011 
Filler 48 100 53 A/N Space R  
 
 

---

## Page 108

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 1, 2023 
Publication Code: MFS314 
Service: Fund/SERV® 
Title: Fixed Length Record Layouts (Part 3) 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 