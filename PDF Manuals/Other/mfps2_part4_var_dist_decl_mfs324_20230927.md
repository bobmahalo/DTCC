---
title: "MFPS II - Distribution Declaration Variable Length Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part4_var_dist_decl_mfs324_20230927.pdf"
pages: 25
size: "422.0 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II - Distribution Declaration Variable Length Record Layouts

**Original File:** [mfps2_part4_var_dist_decl_mfs324_20230927.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part4_var_dist_decl_mfs324_20230927.pdf)  
**Category:** Other  
**Total Pages:** 25  
**File Size:** 422.0 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
DISTRIBUTION DECLARATION VARIABLE LENGTH 
RECORD LAYOUTS 
SEPTEMBER 27, 2023 
 
  

---

## Page 2

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration 12b-1 (040) 2 
TABLE OF CONTENTS 
Distribution Declaration 12b-1 (040)................................................................................................................... 4 
02.14 Distribution Declaration 12b-1 (040) ......................................................................................................... 4 
Distribution Declaration Capital Gains (041) ..................................................................................................... 7 
02.15 Distribution Declaration Capital Gains (041) ............................................................................................ 7 
Distribution Declaration [[Dividend]] (042) ........................................................................................................... 10 
02.16 Distribution Declaration [[Dividend]] (042) ..................................................................................................10 
Distribution Declaration General Earnings (043) ............................................................................................ 13 
02.17 Distribution Declaration General Earnings (043) ....................................................................................13 
Distribution Declaration Municipal Earnings (044) ......................................................................................... 15 
02.18 Distribution Declaration Municipal Earnings (044) .................................................................................15 
APPENDIX ........................................................................................................................................................... 17 
Summary of Changes – Effective Q1, 2019 ..................................................................................................... 18 
Reject Codes ....................................................................................................................................................18 
Summary of Changes - Effective Q4, 2017 ...................................................................................................... 19 
Change to Data Field Valid Values ...................................................................................................................19 
Distribution Declaration Capital Gains Record (041) ......................................................................................19 
Summary of Changes - Effective Q1, 2016 ...................................................................................................... 20 
Change to Data Field Population Requirement ................................................................................................20 
Distribution Declaration Capital Gains Record (041) ......................................................................................20 
Distribution Declaration [[Dividend]] Record (042) ..............................................................................................20 
Summary of Changes – Effective Q2, 2014 ..................................................................................................... 21 
Distribution Declaration [[Dividend]] Record (042) ..............................................................................................21 
Distribution Declaration [[Dividend]] Record (042) ..............................................................................................21 
Summary of Changes – Effective Q1, 2013 ..................................................................................................... 23 
1. Distribution Declaration Capital Gains Record (041) – Section 02.15 ..........................................................23 
2. Distribution Declaration [[Dividend]] Record (042) – Section 02.16 .................................................................23 
Summary of Changes – Effective Q4, 2010 ..................................................................................................... 24 
1. Distribution Declaration Capital Gains (041) – Section 02.15 ......................................................................24 
2. Distribution Declaration General Earnings (043) – Section 02.17 ................................................................24 

---

## Page 3

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration 12b-1 (040) 3 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notice 
September 27, 2023 Document rebranded and reviewed.  
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

## Page 4

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration 12b-1 (040) 4 
DISTRIBUTION DECLARATION 12B-1 (040) 
02.14 Distribution Declaration 12b-1 (040) 
Input/Output 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length  1 4 4 N 0158, 0232  
Must be 158 if Action Type = ‘D’  
R 0088 
Physical Sequence 
Number  
5 6 2 A/N  R 0080 
Logical Sequence 
Number  
7 8 2 A/N 01  R 0080 
Filler  9 9 1 A/N Space  R  
Filler  10 10 1 A/N Space. Place holder for Reminder  R  
Originator Type 
Indicator  
11 11 1 A/N ‘F’ = Fund  R 0081 
Profile Type  12 13 2 A/N 03 = Distribution Declaration  R 0082 
Record Type  14 16 3 A/N 040 = Distribution Declaration  
12b-1 Data  
R 0083 
Action Type  17 17 1 A/N A = add  
C = change  
D = delete  
R 0349 
Submitting [[participant]] 
Number  
18 21 4 A/N  R 0100 
Filler  22 32 11 A/N Space.  R  
Submission Date  33 40 8 A/N ccyymmdd  R 0036 
Filler  41 48 8 A/N Space. Place holder for Effective Date  R  
Security Issue Country 
Code  
49 50 2 A/N See ISO Country Codes  
@  
R 0153 
Security Issue [[ID]]  51 59 9 A/N @  R 0040 
ISIN Security Issue 
Check Digit  
60 60 1 A/N @  R 0041 
Projected/Actual 
Indicator  
61 61 1 A/N 0 = Projected   @  
1 = Actual  
R 0283 

---

## Page 5

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration 12b-1 (040) 5 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Filler  62 78 17 A/N Space  R  
Test Indicator  79 79 1 A/N Space = Production  
1 = Test  
R 0089 
[[NSCC]] Rejection 
Indicator  
80 80 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected By [[NSCC]], Multiple 
errors  
R  
[[NSCC]] Reject Code 1  81 84 4 A/N Input: Space  
Output: Reject code or space  
R  
12b-1 Single Rate  85 102 18 N 999999999.999999999 1  
Not allowed with Pre/Post rates and 
vice versa.   @@  
O 0094 
12b-1 Pre Agreement 
Payable Date  
103 110 8 A/N ccyymmdd 1  @@  O 0301 
12b-1 Pre Agreement 
Record Date  
111 118 8 A/N ccyymmdd  O 0298 
12b-1 Pre Agreement 
Avg [[Asset]] Start Date  
119 126 8 A/N ccyymmdd  O 0299 
12b-1 Pre Agreement 
Avg [[Asset]] End Date  
127 134 8 A/N ccyymmdd  O 0300 
12b-1 Post Agreement 
Payable Date  
135 142 8 A/N ccyymmdd 
1 
Req'd if Single Rate present. @@  
O 0305 
12b-1 Post Agreement 
Record Date  
143 150 8 A/N ccyymmdd  O 0302 
Filler  151 158 8 A/N Space  R  
12b-1 Post Agreement 
Avg [[Asset]] Start Date  
159 166 8 A/N ccyymmdd  O 0303 
12b-1 Post Agreement 
Avg [[Asset]] End Date  
167 174 8 A/N ccyymmdd  O 0304 
 
1 One of the Payable Dates or Single Rate must be present  

---

## Page 6

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration 12b-1 (040) 6 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
12b-1 Pre Rate  175 192 18 N 999999999.999999999  
Req'd if 12-b1 Pre Agreement 
Payable Date present,  
disallowed if Single Rate present, 
otherwise allowable  
O 0152 
12b-1 Post Rate  193 210 18 N 999999999.999999999  
Req'd if 12-b1 Post Agreement 
Payable Date present,  
disallowed if Single Rate present, 
otherwise allowable  
O 0168 
Filler  211 232 22 A/N Space  R  
 

---

## Page 7

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration Capital Gains (041) 7 
DISTRIBUTION DECLARATION CAPITAL GAINS (041) 
02.15 Distribution Declaration Capital Gains (041) 
Input/Output 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length  1 4 4 N 0158  
Must be 158 if Action Type = ‘D’  
R 0088 
Physical Sequence 
Number  
5 6 2 A/N  R 0080 
Logical Sequence 
Number  
7 8 2 A/N 01  R 0080 
Filler  9 9 1 A/N Space  R  
Filler  10 10 1 A/N Space. Place holder for Reminder.  R  
Originator Type 
Indicator  
11 11 1 A/N ‘F’ = Fund  R 0081 
Profile Type  12 13 2 A/N 03 = Distribution Declaration  R 0082 
Record Type  14 16 3 A/N 041 = Distribution Declaration Capital 
Gains Data  
R 0083 
Action Type  17 17 1 A/N A = add;  
C = change;  
D = delete  
R 0349 
Submitting [[participant]] 
Number  
18 21 4 A/N  R 0100 
Filler  22 32 11 A/N Space R  
Submission Date  33 40 8 A/N ccyymmdd  R 0036 
Filler  41 48 8 A/N Space. Place holder for Effective 
Date.  
R  
Security Issue Country 
Code  
49 50 2 A/N See ISO Country Code           @  R 0153 
Security Issue [[ID]]  51 59 9 A/N @  R 0040 
ISIN Security Issue 
Check Digit  
60 60 1 A/N @  R 0041 
Projected/Actual 
Indicator  
61 61 1 A/N 0 = Projected      @  
1 = Actual  
R 0283 

---

## Page 8

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration Capital Gains (041) 8 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Filler  62 78 17 A/N Space  R  
Test Indicator  79 79 1 A/N Space = Production  
1 = Test  
R 0089 
[[NSCC]] Rejection 
Indicator  
80 80 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], Multiple 
Errors  
R  
[[NSCC]] Reject Code 1  81 84 4 A/N Input : Space  
Output: Reject code or space  
R  
Capital Gain Indicator  85 85 1 A/N 0 = Undetermined projected gain  
1 = Short Term Capital Gain  
2 = Long Term Gain 
3 = Gain on Collectables 
4 = Section 1202 Gain  
5 = Unrecaptured Section 1250 Gain  
@  
R 0294 
Distribution Indicator  86 86 1 A/N 0 = N/A (Projected only)  
1 = Spillover  
2 = Reclassification  
3 = Regular Distribution  
@ 
R 0337 
Capital Gain Record 
Date  
87 94 8 A/N ccyymmdd  R 0289 
Capital Gain Ex Date 95 102 8 A/N ccyymmdd  R 0290 
Capital Gain Reinvest 
Date  
103 110 8 A/N ccyymmdd  
Required if Projected/Actual  
Indicator = 1 (Actual) 
OR 
If Capital Gain Amount field is 
populated 
Reinvest Date must be equal or 
greater than Record Date  
OC 0291 
Capital Gain Payable 
Date  
111 118 8 A/N ccyymmdd    @  R 0292 

---

## Page 9

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration Capital Gains (041) 9 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Capital Gain Amount  119 136 18 N 999999999.999999999  
If populated, Capital Gain 
Reinvestment Date is required 
OC 0293 
Reinvest Price  137 154 18 N 999999999.999999999  O 0297 
Filler  155 158 4 A/N Space  R  

---

## Page 10

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration [[Dividend]] (042) 10 
DISTRIBUTION DECLARATION [[Dividend]] (042)  
02.16 Distribution Declaration [[Dividend]] (042) 
Input/Output 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length  1 4 4 N 0158, 0232  
Must be 158 if Action Type = ‘D’  
R 0088 
Physical Sequence 
Number  
5 6 2 A/N  R 0080 
Logical Sequence 
Number  
7 8 2 A/N 01  R 0080 
Filler  9 9 1 A/N Space  R  
Filler  10 10 1 A/N Space. Place holder for Reminder  R  
Originator Type 
Indicator  
11 11 1 A/N ‘F’ = Fund  R 0081 
Profile Type  12 13 2 A/N 03 = Distribution Declaration  R 0082 
Record Type  14 16 3 A/N 042 = Distribution Declaration 
[[Dividend]]  
R 0083 
Action Type  17 17 1 A/N A = add  
C = change  
D = delete  
R 0349 
Submitting [[participant]] 
Number  
18 21 4 A/N  R 0100 
Filler  22 32 11 A/N Space  R  
Submission Date  33 40 8 A/N ccyymmdd  R 0036 
Filler  41 48 8 A/N Space. Place holder for Effective Date  R  
Security Issue Country 
Code  
49 50 2 A/N See ISO Country Codes   @  R 0153 
Security Issue [[ID]]  51 59 9 A/N @  R 0040 
ISIN Security Issue 
Check Digit  
60 60 1 A/N @  R 0041 
Projected/Actual 
Indicator  
61 61 1 A/N 0 = Projected    @  
1 = Actual  
R 0283 
Filler  62 78 17 A/N Space  R  

---

## Page 11

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration [[Dividend]] (042) 11 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Test Indicator  79 79 1 A/N Space = Production  
1 = Test  
R 0089 
[[NSCC]] Rejection 
Indicator  
80 80 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], Multiple 
Errors  
R  
[[NSCC]] Reject Code 1  81 84 4 A/N Input: Space  
Output: Reject code or space  
R  
Distribution Indicator  85 85 1 A/N 0 = N/A (Projected only)  
1 = Spillover  
2 = Reclassification  
3 = Regular Distribution  
5 = Special  
@  
R 0337 
[[Dividend]] Type  86 86 1 A/N 1 = Daily Accrual  
2 = [[Equity]]  
R 0141 
[[Dividend]] Record Date  87 94 8 A/N ccyymmdd  
Required when “[[Dividend]] Type” = 2 
([[Equity]]). 
Not allowed for “[[Dividend]] Type” = 1 
(Daily Accrual) 
OC 0284 
[[Dividend]] Ex Date  95 102 8 A/N ccyymmdd  
Required when “[[Dividend]] Type” = 2 
([[Equity]])  
OC 0285 
[[Dividend]] Reinvest 
Date  
103 110 8 A/N ccyymmdd  
Required when “Projected/Actual 
Indicator” = 1 (Actual)  
OC 0286 
[[Dividend]] Payable Date  111 118 8 A/N ccyymmdd  @  
Required when “Projected/Actual 
Indicator” = 1 (Actual)  
OC 0287 

---

## Page 12

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration [[Dividend]] (042) 12 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[Dividend]] Payable 
Amount  
119 136 18 N 999999999.999999999  
Required when: 
1) “[[Dividend]] Type” field = 2 ([[Equity]]) 
AND the “[[Dividend]] Record Date”, 
“[[Dividend]] Reinvest Date”, and 
“[[Dividend]] Payable Date” are all 
present. 
OR 
2) “Projected/Actual Indicator” = 1 
(Actual) 
OC 0288 
Reinvest Price  137 154 18 N 999999999.999999999  O 0297 
Filler  155 158 4 A/N Space  R  
Payout Rate Period 
Start Date  
159 166 8 A/N ccyymmdd 
Required if “[[Dividend]] Type” = 1 (Daily 
Accrual).  
Not allowed if “[[Dividend]] Type” = 2 
([[Equity]]). 
OC 0295 Payout Rate Period 
End Date  
167 174 8 A/N ccyymmdd  
Required if “[[Dividend]] Type” = 1 (Daily 
Accrual).  
Not allowed if “[[Dividend]] Type” = 2 
([[Equity]]). 
OC 0296 
Actual Days in Pay 
Period  
175 177 3 N 999  O 0151 
Filler  178 232 55 A/N Space  R  

---

## Page 13

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration General Earnings (043) 13 
DISTRIBUTION DECLARATION GENERAL EARNINGS 
(043)  
02.17 Distribution Declaration General Earnings (043) 
Input/Output 
(At least one of the fields after position 84 must be present) 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length  1 4 4 N 0158, 0232  
Must be 084 if Action Type = ‘D’  
R 0088 
Physical Sequence 
Number  
5 6 2 A/N  R 0080 
Logical Sequence 
Number  
7 8 2 A/N 01  R 0080 
Filler  9 9 1 A/N Space  R  
Filler  10 10 1 A/N Space. Place holder for Reminder  R  
Originator Type 
Indicator  
11 11 1 A/N ‘F’ = Fund  R 0081 
Profile Type  12 13 2 A/N 03 = Distribution Declaration  R 0082 
Record Type  14 16 3 A/N 043 = Distribution Declaration 
General Earnings  
R 0083 
Action Type  17 17 1 A/N A = add;  
C = change;  
D = delete  
R 0349 
Submitting [[participant]] 
Number  
18 21 4 A/N  R 0100 
Filler  22 32 11 A/N Space  R  
Submission Date  33 40 8 A/N ccyymmdd  R 0036 
Filler  41 48 8 A/N Space. Place holder for Effective Date  R  
Security Issue Country 
Code  
49 50 2 A/N See ISO Country Codes 
@  
R 0153 
Security Issue [[ID]]  51 59 9 A/N @  R 0040 
ISIN Security Issue 
Check Digit  
60 60 1 A/N @  R 0041 

---

## Page 14

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration General Earnings (043) 14 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
0041 Projected/Actual 
Indicator  
61 61 1 A/N 0 = Projected      @  
1 = Actual  
R 0283 
Payable Date  62 69 8 A/N ccyymmdd         @  R 0376 
Distribution Type  70 70 1 A/N D = [[Dividend]]     @  
C = Cap Gains  
R 0377 
Capital Gain Indicator  71 71 1 A/N Required if Distribution Type = C.  
0 = Undetermined projected gain  
1 = Short Term Capital Gain  
2 = Long Term Gain 
3 = Gain on Collectables 
4 = Section 1202 Gain  
5 = Unrecaptured Section 1250 Gain 
@  
OC 0294 Filler  72 78 7 A/N Space  R  
Test Indicator  79 79 1 A/N Space = Production  
1 = Test  
R 0089 
[[NSCC]] Rejection 
Indicator  
80 80 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], Multiple 
Errors  
R  
[[NSCC]] Reject Code 1  81 84 4 A/N Input : Space  
Output: Reject code or space  
R  
Earnings Subject to 
AMT  
85 100 16 N 99,999,999,999,999.99  O 0306 
Earnings From US 
Govt [[obligations]]  
101 116 16 N 99,999,999,999,999.99  O 0308 
Foreign Tax Credits  117 132 16 N 99,999,999,999,999.99  O 0309 
Return of Capital  133 148 16 N 99,999,999,999,999.99  O 0310 
Filler  149 158 10 A/N Space  R  
Foreign Tax Credit 
Rate  
159 176 18 N 999999999.999999999  O 0224 
Filler  177 232 56 A/N Space  R  

---

## Page 15

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration Municipal Earnings (044) 15 
DISTRIBUTION DECLARATION MUNICIPAL EARNINGS 
(044) 
02.18 Distribution Declaration Municipal Earnings (044) 
Input/Output  
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length  1 4 4 N 0158, 0232, 0306, …., 1934  
Must be 084 if Action Type = ‘D’  
R 0088 
Physical Sequence 
Number  
5 6 2 A/N  R 0080 
Logical Sequence 
Number  
7 8 2 A/N 01  R 0080 
Filler  9 9 1 A/N Space  R  
Filler  10 10 1 A/N Space.  
Place holder for Reminder  
R  
Originator Type 
Indicator  
11 11 1 A/N ‘F’ = Fund  R 0081 
Profile Type  12 13 2 A/N 03 = Distribution Declaration  R 0082 
Record Type  14 16 3 A/N 044 = Distribution Declaration 
Municipal Earnings  
R 0083 
Action Type  17 17 1 A/N A = add;  
C = change;  
D = delete  
R 0349 
Submitting [[participant]] 
Number  
18 21 4 A/N  R 0100 
Filler  22 32 11 A/N Space  R  
Submission Date  33 40 8 A/N ccyymmdd  R 0036 
Filler  41 48 8 A/N Space.  
Place holder for Effective Date  
R 0044 
Security Issue Country 
Code  
49 50 2 A/N See ISO Country Codes @  R 0153 
Security Issue [[ID]]  51 59 9 A/N @  R 0040 
ISIN Security Issue 
Check Digit  
60 60 1 A/N @  R 0041 

---

## Page 16

Distribution Declaration Variable Length Record Layouts 
Distribution Declaration Municipal Earnings (044) 16 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Projected/Actual 
Indicator  
61 61 1 A/N 0 = Projected @  
1 = Actual  
R 0283 
Year of Filing  62 65 4 A/N ccyy  @  R 0369 
Number of States  66 67 2 N 1 - 50  R 0311 
Filler  68 78 11 A/N Space  R  
Test Indicator  79 79 1 A/N Space = Production  
1 = Test  
R 0089 
[[NSCC]] Rejection 
Indicator  
80 80 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], Multiple 
Errors  
R  
[[NSCC]] Reject Code 1  81 84 4 A/N Input : Space  
Output: Reject code or space  
R  
Start of Earnings section 
State of Earnings 1  85 86 2 A/N  R 0370 
Rate of Earnings 1 87 104 18 N 999999999.999999999 R 0371 
Earnings Amount 1  105 120 16 N 99,999,999,999,999.99  R 0312 
State of Earnings 2  121 122 2 A/N  R 0370 
Rate of Earnings 2  123 140 18 N 999999999.999999999  R 0371 
Earnings Amount 2  141 156 16 N 99,999,999,999,999.99  R 0312 
Filler  157 158 2 A/N Space  R  
Earnings section can repeat up to 25 times (50 states) 
 
 

---

## Page 17

Distribution Declaration Variable Length Record Layouts 
APPENDIX 17 
APPENDIX 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 

---

## Page 18

Distribution Declaration Variable Length Record Layouts 
Summary of Changes – Effective Q1, 2019 18 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
0388 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 19

Distribution Declaration Variable Length Record Layouts 
Summary of Changes - Effective Q4, 2017 19 
SUMMARY OF CHANGES - EFFECTIVE Q4, 2017 
Change to Data Field Valid Values 
1) Remove 4 = 5-Year Capital Gain as a valid [[Option]] for Distribution Indicator 
Distribution Declaration Capital Gains Record (041) 
Field Name  Start End Type Current 
Description 
New Description 
Distribution 
Indicator  
86 86 A/N 0 = N/A (Projected only)  
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

---

## Page 20

Distribution Declaration Variable Length Record Layouts 
Summary of Changes - Effective Q1, 2016 20 
SUMMARY OF CHANGES - EFFECTIVE Q1, 2016  
Change to Data Field Population Requirement 
1. Capital Gain Ex Date is changed from Optional to Required.  
Distribution Declaration Capital Gains Record (041) 
Field Name  Start End Type Description Previous 
Opt/Req 
Opt/Req 
Capital Gain Ex 
Date 
95 102 A/N ccyymmdd  O R 
 
2. [[Dividend]] Ex Date is changed from Optional to Optional/Conditional. 
Distribution Declaration [[Dividend]] Record (042) 
Field Name  Start End Type Current 
Description 
New Description Previous 
Opt/Req 
Opt/Req 
[[Dividend]] 
Ex Date 
95 102 A/N ccyymmdd  ccyymmdd 
Required if [[Dividend]]  
Type=2 ([[Equity]]) 
O OC 

---

## Page 21

Distribution Declaration Variable Length Record Layouts 
Summary of Changes – Effective Q2, 2014 21 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2014  
1. Field description requirement change: 
Distribution Declaration [[Dividend]] Record (042) 
Field 
Name  
Start End Len Type Previous Description  New Description Previous 
Opt/Req 
Opt/ 
Req 
Reinvest 
Price  
137 154 18 N 999999999.999999999  
Req’ds Divd. Payable Amount. 
999999999.999999999  OC O 
 
2. The following field descriptions were updated to reflect current record requirements. These revisions are 
documentation updates only and no coding changes have been effected. 
Distribution Declaration [[Dividend]] Record (042) 
Field 
Name  
Start End Len Type Previous Description New Description Opt/ 
Req 
[[Dividend]] 
Record 
Date  
87 94 8 A/N ccyymmdd 
Required for Equities 
Projected & Actuals. 
Disallowed for Accruals. 
ccyymmdd 
Required when “[[Dividend]]  
Type” = 2 ([[Equity]]). 
Not allowed for “[[Dividend]]  
Type” = 1 (Daily Accrual) 
OC 
[[Dividend]] 
Reinvest 
Date  
103 110 8 A/N ccyymmdd 
Required for actuals. 
ccyymmdd  
Required when “Projected/Actual 
Indicator” = 1 (Actual)  
OC 
[[Dividend]] 
Payable 
Date  
111 118 8 A/N ccyymmdd @ 
Required for actuals. 
ccyymmdd @  
Required when “Projected/Actual 
Indicator” = 1 (Actual)  
OC 
[[Dividend]] 
Payable 
Amount  
119 136 18 N 999999999.999999999 
 
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
2) “Projected/Actual  
Indicator” = 1 (Actual) 
OC 

---

## Page 22

Distribution Declaration Variable Length Record Layouts 
Summary of Changes – Effective Q2, 2014 22 
Field 
Name  
Start End Len Type Previous Description New Description Opt/ 
Req 
Payout 
Rate 
Period 
Start Date  
159 166 8 A/N ccyymmdd  
Required for all Accruals. 
Disallowed for Equities. 
ccyymmdd  
Required if “[[Dividend]] Type” = 1 (Daily 
Accrual).  
Not allowed if “[[Dividend]] Type” = 2 
([[Equity]]). 
OC 
Payout 
Rate 
Period End 
Date  
167 174 8 A/N ccyymmdd  
Required for all Accruals. 
Disallowed for Equities. 
ccyymmdd  
Required if “[[Dividend]] Type” = 1 (Daily 
Accrual).  
Not allowed if “[[Dividend]] Type” = 2 
([[Equity]]). 
OC 

---

## Page 23

Distribution Declaration Variable Length Record Layouts 
Summary of Changes – Effective Q1, 2013 23 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2013  
1. Distribution Declaration Capital Gains Record (041) – Section 02.15 
Previous Field 
Name  
New Field Name Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Gain  
Ex Date  
Capital Gain 
Ex Date 
95 102 8 A/N ccyymmdd O 0290 
2. Distribution Declaration [[Dividend]] Record (042) – Section 02.16 
Field Name  Start End Len Type Previous Description  New Description Opt/ 
Req 
Reject 
Code 
Distribution 
Indicator  
85 85 1 A/N 0 = N/A (Projected only)  
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

## Page 24

Distribution Declaration Variable Length Record Layouts 
Summary of Changes – Effective Q4, 2010 24 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2010  
1. Distribution Declaration Capital Gains (041) – Section 02.15 
a. Field description requirement change: 
1. Gain Indicator (start 85, end 85, length 1) 
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
2. Distribution Declaration General Earnings (043) – Section 02.17 
a. Field description requirement change: 
2. Capital Gain Indicator (start 85, end 85, length 1) 
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

## Page 25

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 27, 2023 
Publication Code: MFS324 
Service: Mutual Fund Profile Service II 
Title: Distribution Declaration Variable Length Record Layouts  
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 