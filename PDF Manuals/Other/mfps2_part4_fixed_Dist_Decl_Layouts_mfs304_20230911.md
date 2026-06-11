---
title: "MFPS II - Distribution Declaration Fixed Length Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part4_fixed_Dist_Decl_Layouts_mfs304_20230911.pdf"
pages: 35
size: "454.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II - Distribution Declaration Fixed Length Record Layouts

**Original File:** [mfps2_part4_fixed_Dist_Decl_Layouts_mfs304_20230911.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part4_fixed_Dist_Decl_Layouts_mfs304_20230911.pdf)  
**Category:** Other  
**Total Pages:** 35  
**File Size:** 454.2 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
DISTRIBUTION DECLARATION FIXED LENGTH 
RECORD LAYOUTS 
SEPTEMBER 11, 2023 
 
  

---

## Page 2

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration 12b-1 (040) 2 
TABLE OF CONTENTS 
Distribution Declaration 12b-1 (040)................................................................................................................... 5 
02.14.01 Distribution Declaration 12b-1 (040) Record 1 of 3 ............................................................................. 5 
02.14.02 Distribution Declaration 12b-1 (040) Record 2 of 3 ............................................................................. 7 
02.14.03 Distribution Declaration 12b-1 (040) Record 3 of 3 ............................................................................. 8 
Distribution Declaration Capital Gains (041) ..................................................................................................... 9 
02.15.01 Distribution Declaration Capital Gains (041) Record 1 of 2 ................................................................. 9 
02.15.02 Distribution Declaration Capital Gains (041) Record 2 of 2 ...............................................................11 
Distribution Declaration [[Dividend]] (042) ........................................................................................................... 13 
02.16.01 Distribution Declaration [[Dividend]] (042) Record 1 of 3 ......................................................................13 
02.16.02 Distribution Declaration [[Dividend]] (042) Record 2 of 3 ......................................................................15 
02.16.03 Distribution Declaration [[Dividend]] (042) Record 3 of 3 ......................................................................17 
Distribution Declaration General Earnings (043) ............................................................................................ 18 
02.17.01 Distribution Declaration General Earnings (043) Record 1 of 3 ........................................................18 
02.17.02 Distribution Declaration General Earnings (043) Record 2 of 3 ........................................................20 
02.17.03 Distribution Declaration General Earnings (043) Record 3 of 3 ........................................................21 
Distribution Declaration Municipal Earnings (044) ......................................................................................... 22 
02.18.01 Distribution Declaration Municipal Earnings (044) Record 1 of 26  ....................................................22 
02.18.02 Distribution Declaration Municipal Earnings (044) Record 2 of 26  ....................................................24 
Records 3 thru 26 .............................................................................................................................................25 
APPENDIX ........................................................................................................................................................... 26 
Summary of Changes – Effective Q1 (March 25), 2019 .................................................................................. 27 
Reject codes .....................................................................................................................................................27 
Summary of Changes – Effective Q4, 2017 ..................................................................................................... 28 
Change to Data Field Valid Values ...................................................................................................................28 
Distribution Declaration Capital Gains Record (041) Record 2 of 2 ...............................................................28 
Summary of Changes - Effective Q1, 2016 ...................................................................................................... 29 
Change to Data Field Population Requirement ................................................................................................29 
Distribution Declaration Capital Gains Record (041), Record 2 of 2 ..............................................................29 
Distribution Declaration [[Dividend]] Record (042), Record 2 of 3 ......................................................................29 

---

## Page 3

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration 12b-1 (040) 3 
Summary of Changes – Effective Q2, 2014 ..................................................................................................... 30 
Distribution Declaration [[Dividend]] Record (042), Record 2 of 3 ........................................................................30 
Distribution Declaration [[Dividend]] Record (042), Record 2 of 3 ........................................................................30 
Distribution Declaration [[Dividend]] Record (042), Record 3 of 3 ........................................................................31 
Summary of Changes – Effective Q1, 2013 ..................................................................................................... 32 
1. Distribution Declaration Capital Gains Record (041) ....................................................................................32 
2. Distribution Declaration [[Dividend]] Record (042) ...........................................................................................32 
Summary of Changes – Effective Q4, 2010 ..................................................................................................... 33 
1. Distribution Declaration Capital Gains (041) – Record 2 of 2. Section 02.15.02 .........................................33 
2. Distribution Declaration General Earnings (043) – Record 1 of 3.  Section 02.17.01 ..................................34 
 

---

## Page 4

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration 12b-1 (040) 4 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notice 
September 11, 2023 Document rebranded and reviewed. 
April 14, 2023 Document rebranded and reviewed. 
March 25, 2019 Please see Important Notice: a8658 P&S 8233 
Dated December 19, 2018 
November 20, 2017 Please see Important Notice: a8402 P&S 7977 
Dated 06/01/2017 
February 29, 2016 Please see Important Notice: a8107 P&S 7682 
Dated 10/27/2015 
April 21, 2014 Please see Important Notice: a7807 P&S 7377 
Dated March 24, 2014. 
January 14, 2013 Please see Important Notice: a7467 P&S 7037 
Dated August 6, 2012, and a7553 P&S 7123 
Dated December 17, 2012 
Nov 22, 2010 Please see Important Notice: a7044 P&S 6615 
Dated August 17, 2010 
March 27, 2006 Please see Important Notice: a6171 P&S 5741 
Dated December 21, 2005 
November 14, 2005 Please see Important Notice: a6084 P&S 5654 
Dated August 10, 2005 
August 29, 2005 Please see Important Notice a6062 P&S 5632 
Dated July 6, 2005 

---

## Page 5

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration 12b-1 (040) 5 
DISTRIBUTION DECLARATION 12B-1 (040) 
02.14.01 Distribution Declaration 12b-1 (040) Record 1 of 3 
Required 
Input/Output 
(If Action Type = ‘D’ submit record 1 and 2) 
Record 1 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Filler 6 6 1 A/N Space. Place holder for Reminder. R  
Originator Type 
Indicator 
7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 03 = Distribution Declaration R 0082 
Record Type 10 12 3 A/N 040 = Distribution Declaration  
12b-1 Data 
R 0083 
Action Type 13 13 1 A/N A = add 
C = change  
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N  R 0100 
Filler 18 28 11 A/N Space. R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Filler 37 44 8 A/N Space. Place holder for Effective 
Date. 
R  
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes @ R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue 
Check Digit 
56 56 1 A/N @ R 0041 
Projected/Actual 
Indicator 
57 57 1 A/N 0 = Projected 
1 = Actual @ 
R 0283 

---

## Page 6

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration 12b-1 (040) 6 
Record 1 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Filler 58 74 17 A/N Space R  
Test Indicator 75 75 1 A/N Space = Production  
1 = Test 
R 0089 
[[NSCC]] Rejection 
Indicator 
76 76 1 A/N Input: Space Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
2 = Rejected By [[NSCC]], Multiple 
errors 
R  [[NSCC]] Reject Code 1 77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 7

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration 12b-1 (040) 7 
02.14.02 Distribution Declaration 12b-1 (040) Record 2 of 3 
Required 
Record 2 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
12b-1 Single Rate 7 24 18 N 999999999.999999999 1 
Not allowed with Pre rates and vice 
versa. 
@ 
O 0094 
12b-1 Pre 
Agreement Payable 
Date 
25 32 8 A/N ccyymmdd 1  
@ 
O 0301 
12b-1 Pre Agreement 
Record Date 
33 40 8 A/N ccyymmdd O 0298 
12b-1 Pre Agreement 
Avg [[Asset]] Start Date 
41 48 8 A/N ccyymmdd O 0299 
12b-1 Pre Agreement 
Avg [[Asset]] End Date 
49 56 8 A/N ccyymmdd O 0300 
12b-1 Post Agreement 
Payable Date 
57 64 8 A/N ccyymmdd 
1 
Req'd if Single Rate present @ 
O 0305 
12b-1 Post 
Agreement Record 
Date 
65 72 8 A/N ccyymmdd O 0302 
Filler 73 80 8 A/N Space R  
 
 
 
  
 
1 One of the Payable Dates or Single Rate must be present.  

---

## Page 8

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration 12b-1 (040) 8 
02.14.03 Distribution Declaration 12b-1 (040) Record 3 of 3 
Optional 
Record 3 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
12b-1 Post Agreement 
Avg 
[[Asset]] Start Date 
7 14 8 A/N ccyymmdd O 0303 
12b-1 Post Agreement 
Avg [[Asset]] End Date 
15 22 8 A/N ccyymmdd O 0304 
12b-1 Pre Rate 23 40 18 N 999999999.999999999 
Req'd if 12-b1 Pre Agreement 
Payable Date present, disallowed if 
Single Rate present, otherwise 
allowable. 
O 0152 
12b-1 Post Rate 41 58 18 N 999999999.999999999 
Req'd if 12-b1 Post Agreement 
Payable Date present, disallowed if 
Single Rate present, otherwise 
allowable. 
O 0168 
Filler 59 80 22 A/N Space R  

---

## Page 9

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration Capital Gains (041) 9 
DISTRIBUTION DECLARATION CAPITAL GAINS (041) 
02.15.01 Distribution Declaration Capital Gains (041) Record 1 of 2 
Required 
Input/Output 
(If Action Type = ‘D’ submit record 1 and 2.) 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Filler 6 6 1 A/N Space. Place holder for Reminder. R  
Originator Type 
Indicator 
7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 03 = Distribution Declaration R 0082 
Record Type 10 12 3 A/N 041 = Distribution Declaration  
Capital Gains Data 
R 0083 
Action Type 13 13 1 A/N A = add; 
C = change;  
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N  R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Filler 37 44 8 A/N Space. Place holder for Effective 
Date. 
R  
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes @ R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue 
Check Digit 
56 56 1 A/N @ R 0041 
Projected/Actual 
Indicator 
57 57 1 A/N 0 = Projected 
1 = Actual @ 
R 0283 

---

## Page 10

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration Capital Gains (041) 10 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Filler 58 74 17 A/N Space R  
Test Indicator 75 75 1 A/N Space = Production 1 = Test R 0089 
[[NSCC]] Rejection 
Indicator 
76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple 
Errors 
R  
[[NSCC]] Reject Code 1 77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 11

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration Capital Gains (041) 11 
02.15.02 Distribution Declaration Capital Gains (041) Record 2 of 2 
Required 
Record 2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Gain Indicator 7 7 1 A/N 0 = Undetermined projected gain  
1 = Short Term Capital Gain 
2 = Long Term Gain 
3 = Gain on Collectables  
4 = Section 1202 Gain 
5 = Unrecaptured Section 1250 Gain 
@ 
R 0294 
Distribution Indicator 8 8 1 A/N 0 = N/A (Projected only)  
1 = Spillover 
2 = Reclassification 
3 = Regular Distribution 
@ 
(Effective Q4, 2017) 
R 0337 
Capital Gain Record 
Date 
9 16 8 A/N ccyymmdd R 0289 
Capital Gain Ex Date 17 24 8 A/N ccyymmdd R 0290 
Capital Gain Reinvest 
Date 
25 32 8 A/N ccyymmdd 
Required if Projected/Actual  
Indicator = 1 (Actual) 
OR 
If Capital Gain Amount field is 
populated 
OC 0291 
Capital Gain Payable 
Date 
33 40 8 A/N ccyymmdd @ R 0292 
Capital Gain Amount 41 58 18 N 999999999.999999999 
If populated, Capital Gain 
Reinvestment Date is required 
OC 0293 
Reinvest Price 59 76 18 N 999999999.999999999 O 0297 

---

## Page 12

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration Capital Gains (041) 12 
Record 2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Filler 77 80 4 A/N Space R  

---

## Page 13

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration [[Dividend]] (042) 13 
DISTRIBUTION DECLARATION [[Dividend]] (042) 
02.16.01 Distribution Declaration [[Dividend]] (042) Record 1 of 3 
Required 
Input/Output 
(If Action Type = ‘D’ submit only records 1 and 2.) 
Record 1 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Filler 6 6 1 A/N Space. Place holder for Reminder R  
Originator Type 
Indicator 
7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 03 = Distribution Declaration R 0082 
Record Type 10 12 3 A/N 042 = Distribution Declaration 
[[Dividend]] 
R 0083 
Action Type 13 13 1 A/N A = add; 
C = change;  
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N  R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Filler 37 44 8 A/N Space. Place holder for Effective Date R  
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes @ R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue 
Check Digit 
56 56 1 A/N @ R 0041 
Projected/Actual 
Indicator 
57 57 1 A/N 0 = Projected 
1 = Actual @ 
R 0283 

---

## Page 14

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration [[Dividend]] (042) 14 
Record 1 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Filler 58 74 17 A/N Space R  
Test Indicator 75 75 1 A/N Space = Production 1 = Test R 0089 
[[NSCC]] Rejection 
Indicator 
76 76 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple 
Errors 
R  
[[NSCC]] Reject Code 1 77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 15

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration [[Dividend]] (042) 15 
02.16.02 Distribution Declaration [[Dividend]] (042) Record 2 of 3 
Required 
Record 2 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Distribution Indicator 7 7 1 A/N 0 = N/A (Projected only)  
1 = Spillover 
2 = Reclassification 
3 = Regular Distribution  
5 = Special @ 
R 0337 
[[Dividend]] Type 8 8 1 A/N 1 = Daily Accrual 2 = [[Equity]] R 0141 
[[Dividend]] Record Date 9 16 8 A/N ccyymmdd 
Required when “[[Dividend]] Type” = 2 
([[Equity]]). 
Not allowed for “[[Dividend]] Type” = 1 
(Daily Accrual) 
OC 0284 
[[Dividend]] Ex Date 17 24 8 A/N ccyymmdd 
Required when “[[Dividend]] Type” = 2 
([[Equity]]). 
OC 0285 
[[Dividend]] Reinvest 
Date 
25 32 8 A/N ccyymmdd 
Required when “Projected/Actual 
Indicator” = 1 (Actual) 
OC 0286 
[[Dividend]] Payable 
Date 
33 40 8 A/N ccyymmdd @ 
Required when “Projected/Actual 
Indicator” = 1 (Actual) 
OC 0287 
[[Dividend]] Payable 
Amount 
41 58 18 N 999999999.999999999 
Required when: 
1) “[[Dividend]] Type” field = 2 ([[Equity]]) 
AND the “[[Dividend]] Record Date”, 
“[[Dividend]] Reinvest Date”, and “[[Dividend]] 
Payable Date” are all present. 
OR 
2) “Projected/Actual Indicator” = 1 
(Actual) 
OC 0288 
Reinvest Price 59 76 18 N 999999999.999999999 O 0297 

---

## Page 16

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration [[Dividend]] (042) 16 
Record 2 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Filler 77 80 4 A/N Space R  
 
 
  

---

## Page 17

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration [[Dividend]] (042) 17 
02.16.03 Distribution Declaration [[Dividend]] (042) Record 3 of 3 
Required 
Record 3 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Payout Rate Period 
Start Date 
7 14 8 A/N ccyymmdd 
Required if “[[Dividend]] Type” = 1 
(Daily Accrual). 
Not allowed if “[[Dividend]] Type” = 2 
([[Equity]]). 
OC 0295 Payout Rate Period 
End Date 
15 22 8 A/N ccyymmdd 
Required if “[[Dividend]] Type” = 1 
(Daily Accrual). 
Not allowed if “[[Dividend]] Type” = 2 
([[Equity]]). 
OC 0296 
Actual Days in Pay 
Period 
23 25 3 N 999 O 0151 
Filler 26 80 55 A/N Space R  

---

## Page 18

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration General Earnings (043) 18 
DISTRIBUTION DECLARATION GENERAL EARNINGS 
(043)  
02.17.01 Distribution Declaration General Earnings (043) Record 1 of 3 
Required 
Input/Output 
(If Action Type = ‘D’, submit this record and at least one of the records 2 or 3, where at least one of the fields is 
required) 
Record 1 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Filler 6 6 1 A/N Space. Place holder for Reminder R  
Originator Type 
Indicator 
7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 03 = Distribution Declaration R 0082 
Record Type 10 12 3 A/N 043 = Distribution Declaration 
General Earnings 
R 0083 
Action Type 13 13 1 A/N A = add; 
C = change;  
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N  R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Filler 37 44 8 A/N Space. Place holder for Effective Date R  
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes @ R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue 
Check Digit 
56 56 1 A/N @ R 0041 

---

## Page 19

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration General Earnings (043) 19 
Record 1 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Projected/Actual 
Indicator 
57 57 1 A/N 0 = Projected 
1 = Actual  
@ 
R 0283 
Payable Date 58 65 8 A/N ccyymmdd  
@ 
R 0376 
Distribution Type 66 66 1 A/N D = [[Dividend]]  
C = Cap Gains  
@ 
R 0377 
Capital Gain Indicator 67 67 1 A/N Required if Distribution Type = C.  
0 = Undetermined projected gain  
1 = Short Term Capital Gain 
2 = Long Term Gain 
3 = Gain on Collectables  
4 = Section 1202 Gain 
5 = Unrecaptured Section 1250 Gain 
@ 
OC 0294 
Filler 68 74 7 A/N Space R  
Test Indicator 75 75 1 A/N Space = Production  
1 = Test 
R 0089 
[[NSCC]] Rejection 
Indicator 
76 76 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple 
Errors 
R  
[[NSCC]] Reject Code 1 77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 20

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration General Earnings (043) 20 
02.17.02 Distribution Declaration General Earnings (043) Record 2 of 3 
Optional 
(If Action Type = ‘D’, submit the first record and at least one of the records 2 or 3, where at least one of the 
fields is required) 
Record 2 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Earnings Subject to 
AMT 
7 22 16 N 99,999,999,999,999.99 O 0306 
Earnings From US 
Govt [[obligations]] 
23 38 16 N 99,999,999,999,999.99 O 0308 
Foreign Tax Credits 39 54 16 N 99,999,999,999,999.99 O 0309 
Return of Capital 55 70 16 N 99,999,999,999,999.99 O 0310 
Filler 71 80 10 A/N Space R  
 
 
  

---

## Page 21

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration General Earnings (043) 21 
02.17.03 Distribution Declaration General Earnings (043) Record 3 of 3 
Optional 
(If Action Type = ‘D’, submit the first record and at least one of the records 2 or 3, where at least one of the 
fields is required) 
Record 3 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Foreign Tax Credit 
Rate 
7 24 18 N 999999999.999999999 O 0224 
Filler 25 80 56 A/N Space R  

---

## Page 22

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration Municipal Earnings (044) 22 
DISTRIBUTION DECLARATION MUNICIPAL EARNINGS 
(044) 
02.18.01 Distribution Declaration Municipal Earnings (044) Record 1 
of 26 
Required 
Input/Output 
(If Action Type = ‘D’ submit only this record.) 
Record 1 of 26 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Filler 6 6 1 A/N Space. Place holder for Reminder R  
Originator Type 
Indicator 
7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 03 = Distribution Declaration R 0082 
Record Type 10 12 3 A/N 044 = Distribution Declaration 
Municipal Earnings 
R 0083 
Action Type 13 13 1 A/N A = add 
C = change  
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N  R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Filler 37 44 8 A/N Space. Place holder for Effective Date R 0044 
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes  
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue 
Check Digit 
56 56 1 A/N @ R 0041 

---

## Page 23

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration Municipal Earnings (044) 23 
Record 1 of 26 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Projected/Actual 
Indicator 
57 57 1 A/N 0 = Projected 
1 = Actual  
@ 
R 0283 
Year of Filing 58 61 4 A/N ccyy  
@ 
R 0369 
Number of States 62 63 2 N 1 - 50 R 0311 
Filler 64 74 11 A/N Space R  
Test Indicator 75 75 1 A/N Space = Production  
1 = Test 
R 0089 
[[NSCC]] Rejection 
Indicator 
76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple 
Errors 
R  
[[NSCC]] Reject Code 1 77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 24

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration Municipal Earnings (044) 24 
02.18.02 Distribution Declaration Municipal Earnings (044) Record 2 
of 26 
Optional 
Record 2 of 26 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
State of Earnings 1 7 8 2 A/N @ R 0370 
Rate of Earnings 1 9 26 18 N 999999999.999999999 R 0371 
Earnings Amount 1 27 42 16 N 99,999,999,999,999.99 R 0312 
State of Earnings 2 43 44 2 A/N  R 0370 
Rate of Earnings 2 45 62 18 N 999999999.999999999 R 0371 
Earnings Amount 2 63 78 16 N 99,999,999,999,999.99 R 0312 
Filler 79 80 2 A/N Space R  
 
 
  

---

## Page 25

Distribution Declaration Fixed Length Record Layouts 
Distribution Declaration Municipal Earnings (044) 25 
Records 3 thru 26 
Optional 
The previous record may repeat itself for additional States up to 50. 
 

---

## Page 26

Distribution Declaration Fixed Length Record Layouts 
APPENDIX 26 
APPENDIX 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 
 

---

## Page 27

Distribution Declaration Fixed Length Record Layouts 
Summary of Changes – Effective Q1 (March 25), 2019 27 
SUMMARY OF CHANGES – EFFECTIVE Q1 (MARCH 25), 
2019 
Reject codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
0388 [[participant]] is not valid for the Submitter and/or Product. 

---

## Page 28

Distribution Declaration Fixed Length Record Layouts 
Summary of Changes – Effective Q4, 2017 28 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2017 
Change to Data Field Valid Values 
1) Remove 4 = 5-Year Capital Gain as a valid [[Option]] for Distribution Indicator 
Distribution Declaration Capital Gains Record (041) Record 2 of 2 
Field Name Start End Type Current Description New Description 
Distribution 
Indicator 
8 8 A/N 0 = N/A (Projected only)  
1 = Spillover 
2 = Reclassification 
3 = Regular Distribution 
4 = 5-Year Capital Gain  
@ 
0 = N/A (Projected only)  
1 = Spillover 
2 = Reclassification 
3 = Regular Distribution 
@ 
(Effective Q4, 2017) 

---

## Page 29

Distribution Declaration Fixed Length Record Layouts 
Summary of Changes - Effective Q1, 2016 29 
SUMMARY OF CHANGES - EFFECTIVE Q1, 2016 
Change to Data Field Population Requirement 
1) Capital Gain Ex Date is changed from Optional to Required. 
Distribution Declaration Capital Gains Record (041), Record 2 of 2 
Field Name Start End Type Description Previous 
Opt/Req 
Opt/Req 
Capital Gain 
Ex Date 
17 24 A/N ccyymmdd 0 R 
 
2) [[Dividend]] Ex Date is changed from Optional to Optional/Conditional. 
Distribution Declaration [[Dividend]] Record (042), Record 2 of 3 
Field 
Name 
Start End Type Current Description New Description Previous 
Opt/Req 
Opt/Req 
[[Dividend]] 
Ex Date 
17 24 A/N ccyymmdd ccyymmdd 
Required if [[Dividend]]  
Type =2 ([[Equity]]) 
0 OC 

---

## Page 30

Distribution Declaration Fixed Length Record Layouts 
Summary of Changes – Effective Q2, 2014 30 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2014 
1) Field description requirement change: 
Distribution Declaration [[Dividend]] Record (042), Record 2 of 3 
Field 
Name 
Start End Len Type Previous Description New Description Previous 
Opt/Req 
Opt/ 
Req 
Reinvest 
Price 
59 76 18 N 999999999.999999999  
Required for all Actuals. 
Req’ds Div. Payable 
Amount. 
999999999.999999999 OC O 
 
2) The following field descriptions were updated to reflect current record requirements. These revisions are 
documentation updates only and no coding changes have been affected. 
Distribution Declaration [[Dividend]] Record (042), Record 2 of 3 
Field 
Name 
Start End Len Type Previous Description New Description Opt/ 
Req 
[[Dividend]] 
Record 
Date 
9 16 8 A/N ccyymmdd 
Required for Equities 
Projected & Actuals. 
Disallowed for Accruals. 
ccyymmdd 
Required when “[[Dividend]] Type” = 2 
([[Equity]]).  
Not allowed for “[[Dividend]] Type” = 1 
(Daily Accrual) 
OC 
[[Dividend]] 
Reinvest 
Date 
25 32 8 A/N ccyymmdd 
Required for actuals 
ccyymmdd  
Required when “Projected/Actual 
Indicator” = 1 (Actual) 
OC 
[[Dividend]] 
Payable 
Date 
33 40 8 A/N ccyymmdd 
Required for actuals 
ccyymmdd @  
Required when “Projected/Actual 
Indicator” = 1 (Actual) 
OC 
[[Dividend]] 
Payable 
Amount 
41 58 18  N 999999999.999999999 
Required for equities if 
present all Dates (except 
Ex Date) are required. 
999999999.999999999  
Required when: 
1) “[[Dividend]] Type” field = 2 ([[Equity]]) 
AND the “[[Dividend]] Record Date”, 
“[[Dividend]] Reinvest Date”, and 
“[[Dividend]] Payable Date” are all 
present. 
OR 
2) “Projected/Actual Indicator” = 1 
(Actual) 
OC 
 

---

## Page 31

Distribution Declaration Fixed Length Record Layouts 
Summary of Changes – Effective Q2, 2014 31 
Distribution Declaration [[Dividend]] Record (042), Record 3 of 3 
Field Name Start End Len Type Previous Description New Description  
Payout Rate 
Period Start 
Date 
7 14 8 A/N ccyymmdd 
Required for all 
Accruals. Disallowed 
for Equities. 
ccyymmdd 
Required if “[[Dividend]] Type” = 1 
(Daily Accrual). Not allowed if 
“[[Dividend]] Type” = 2 ([[Equity]]). 
OC 
Payout Rate 
Period End 
Date 
15 22 8 A /N ccyymmdd 
Required for all 
Accruals. Disallowed 
for Equities. 
ccyymmdd 
Required if “[[Dividend]] Type” = 1 
(Daily Accrual). Not allowed if 
“[[Dividend]] Type” = 2 ([[Equity]]). 
OC 

---

## Page 32

Distribution Declaration Fixed Length Record Layouts 
Summary of Changes – Effective Q1, 2013 32 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2013 
1. Distribution Declaration Capital Gains Record (041) 
Previous Field Name New Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Gain Ex Date Capital Gain Ex 
Date 
17 24 8 A/N ccyymmdd O 0290 
2. Distribution Declaration [[Dividend]] Record (042) 
Field Name Start End Len Type Previous Description New Description Opt/ 
Req 
Reject 
Code 
Distribution 
Indicator 
7 7 1 A/N 0 = N/A (Projected only)  
1 = Spillover  
2 = Reclassification  
3 = Regular Distribution  
@ 
0 = N/A (Projected only)  
1 = Spillover  
2 = Reclassification  
3 = Regular Distribution 
5 = Special  
@ 
R 0337 

---

## Page 33

Distribution Declaration Fixed Length Record Layouts 
Summary of Changes – Effective Q4, 2010 33 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2010 
1. Distribution Declaration Capital Gains (041) – Record 2 of 2. 
Section 02.15.02 
a. Field description requirement change: 
1. Gain Indicator  (start 7, end 7, length 1) 
 Current Requirement: 0 = Undetermined projected gain 
  1 = Short Term Capital Gain  
  2 = 20% Rate Gain 
  3 = 28% Rate Gain 
  4 = Section 1202 Gain 
  5 = Unrecaptured Section 1250 Gain 
 New Requirement: 0 = Undetermined projected gain 
  1 = Short Term Capital Gain  
  2 = Long Term Gain 
  3 = Gain on Collectables  
  4 = Section 1202 Gain 
  5 = Unrecaptured Section 1250 Gain 

---

## Page 34

Distribution Declaration Fixed Length Record Layouts 
Summary of Changes – Effective Q4, 2010 34 
2. Distribution Declaration General Earnings (043) – Record 1 of 3.  
Section 02.17.01 
a. Field description requirement change: 
2. Capital Gain Indicator  (start 67, end 67, length 1) 
Current Requirement: 0 = Undetermined projected gain 
  1 = Short Term Capital Gain  
  2 = 20% Rate Gain 
  3 = 28% Rate Gain 
  4 = Section 1202 Gain 
  5 = Unrecaptured Section 1250 Gain 
 New Requirement: 0 = Undetermined projected gain 
  1 = Short Term Capital Gain  
  2 = Long Term Gain 
  3 = Gain on Collectables  
  4 = Section 1202 Gain 
  5 = Unrecaptured Section 1250 Gain 
 
 
 
 

---

## Page 35

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 11, 2023 
Publication Code: MFS304 
Service: Mutual Fund Profile Service II 
Title: Distribution Declaration Fixed Length Record Layouts 
 
For More Information 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 
   