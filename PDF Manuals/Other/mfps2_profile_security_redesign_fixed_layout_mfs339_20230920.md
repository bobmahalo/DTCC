---
title: "MFPS II - Profile Security Database – Fixed Length Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_profile_security_redesign_fixed_layout_mfs339_20230920.pdf"
pages: 118
size: "1082.5 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II - Profile Security Database – Fixed Length Record Layouts

**Original File:** [mfps2_profile_security_redesign_fixed_layout_mfs339_20230920.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_profile_security_redesign_fixed_layout_mfs339_20230920.pdf)  
**Category:** Other  
**Total Pages:** 118  
**File Size:** 1082.5 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
PROFILE SECURITY DATABASE – FIXED LENGTH 
RECORD LAYOUTS 
SEPTEMBER 20, 2023 
 

---

## Page 2

Profile Security Database – Fixed Length Record Layouts 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 6 
Record Type 020 – General Profile ..................................................................................................................... 7 
Record 1 of 10 (Required) .................................................................................................................................. 7 
Record 2 of 10 (Required) ................................................................................................................................10 
Record 3 of 10 (Required) ................................................................................................................................11 
Record 4 of 10 (Required) ................................................................................................................................14 
Record 5 of 10 (Required) ................................................................................................................................16 
Record 6 of 10 (Required) ................................................................................................................................19 
Record 7 of 10 (Required) ................................................................................................................................22 
Record 8 of 10 (Required) ................................................................................................................................24 
Record 9 of 10 (Required) ................................................................................................................................25 
Record 10 of 10 (Required) ..............................................................................................................................26 
Record Type 021 – Blue Sky Data .................................................................................................................... 27 
Record 1 of 4 (Required) ..................................................................................................................................27 
Record 2 of 3 (Required) ..................................................................................................................................29 
Record 3 of 4 (Required) ..................................................................................................................................31 
Record 4 of 4 (Optional) ...................................................................................................................................32 
Record Type 022 – CDSC Data ......................................................................................................................... 34 
Record 1 of 18 (Required) ................................................................................................................................34 
Record 2 of 18 (Required) ................................................................................................................................36 
Record 3 of 18 (Required) ................................................................................................................................40 
Record 4 of 18 (Required) ................................................................................................................................41 
Record 5 of 18 (Optional) .................................................................................................................................42 
Record 6 of 18 (Optional) .................................................................................................................................43 
Records 4 to 6 Above Can Repeat for Up to 5 Schedules as Follows: ............................................................43 
Record Type 023 – Breakpoint Schedules ...................................................................................................... 44 
Record 1 of 13 (Required) ................................................................................................................................44 
Record 2 of 13 (Required) ................................................................................................................................46 
Record 3 of 13 (Required) ................................................................................................................................47 

---

## Page 3

Profile Security Database – Fixed Length Record Layouts 
History of Important Notices 3 
Records 4 of 13 (Required) ..............................................................................................................................48 
Records 4 Through 13 (Optional) .....................................................................................................................49 
Record Type 024 – Commission Data .............................................................................................................. 50 
Record 1 of 18 (Required) ................................................................................................................................50 
Record 2 of 18 (Required) ................................................................................................................................53 
Record 3 of 18 (Required) ................................................................................................................................54 
Record 4 of 18 (Required) ................................................................................................................................55 
Record 5 of 18 (Optional) .................................................................................................................................56 
Record 6 of 18 (Optional) .................................................................................................................................57 
Records 4 to 6 Above Can Repeat for Up to 5 Agreements as Follows: .........................................................57 
Record Type 025 – [[NSCC]] Social Code Eligibility ........................................................................................... 58 
Record 1 of 3 (Required) ..................................................................................................................................58 
Record 2 of 3 (Required) ..................................................................................................................................60 
Record 3 of 3 (Required) ..................................................................................................................................61 
Record Type 026 –Short Term Redemption Data ........................................................................................... 62 
Record 1 of 4 (Required) ..................................................................................................................................62 
Record 2 of 4 (Required) ..................................................................................................................................64 
Record 3 of 4 (Required) ..................................................................................................................................66 
Record 4 of 4 (Required) ..................................................................................................................................67 
Record Type 029 – Linkage Rules Data ........................................................................................................... 68 
Record 1 of 4 (Required) ..................................................................................................................................68 
Record 2 of 4 (Required) ..................................................................................................................................71 
Record 3 of 4 (Required) ..................................................................................................................................72 
Record 4 of 4 (Optional) ...................................................................................................................................73 
Record Type 030 – Master Tables Maintenance Record ................................................................................ 75 
Record 1 of 4 (Required) ..................................................................................................................................75 
Record 2 of 4 (Required) ..................................................................................................................................77 
Record 3 of 4 (Required) ..................................................................................................................................78 
Record 4 of 4 (Required) ..................................................................................................................................79 
Record Type 031 – Fees and Expenses ........................................................................................................... 80 

---

## Page 4

Profile Security Database – Fixed Length Record Layouts 
History of Important Notices 4 
Record 1 of 3 (Required) ..................................................................................................................................80 
Record 2 of 3 (Required) ..................................................................................................................................82 
Record 3 of 3 (Required) ..................................................................................................................................83 
Record Type 032 – 408(b) (2) Specific ............................................................................................................. 84 
Record 1 of 4 (Required) ..................................................................................................................................84 
Record 2 of 4 (Required) ..................................................................................................................................86 
Record 3 of 4 (Required) ..................................................................................................................................87 
Record 4 of 4 (Required) ..................................................................................................................................88 
Record Type 033 – Money Market Fund Data .................................................................................................. 89 
Record 1 of 3 ....................................................................................................................................................89 
Record 2 of 3 ....................................................................................................................................................91 
Record 3 of 3 ....................................................................................................................................................92 
Appendix A: Valid Values for Investment Class Code ................................................................................... 93 
Appendix B: Valid Values for Social Code ...................................................................................................... 95 
Social Codes .....................................................................................................................................................95 
Appendix C: Modifications to Social Code field edits .................................................................................. 106 
Background .....................................................................................................................................................106 
APPENDIX D: SUMMARY OF CHANGES ....................................................................................................... 108 
Summary of Changes – Effective date March 28, 2022 ................................................................................ 109 
New Product Type Code – Interval Fund (48) ................................................................................................109 
Summary of Changes – Effective date August 26, 2019 .............................................................................. 110 
Social Code .....................................................................................................................................................110 
Summary of Changes – Effective date March 25, 2019 ................................................................................ 111 
Reject Codes ..................................................................................................................................................111 
Summary of changes – Effective date July 13, 2018 .................................................................................... 112 
Summary of changes – Effective date July 9, 2018 ...................................................................................... 113 
Existing Fields Modified ..................................................................................................................................113 
Summary of changes – Effective date August 22, 2016 ............................................................................... 115 
Existing Fields Modified ..................................................................................................................................115 
Summary of changes – Effective date May 31, 2016 .................................................................................... 116 

---

## Page 5

Profile Security Database – Fixed Length Record Layouts 
History of Important Notices 5 
New Record Type Added ................................................................................................................................116 
Summary of changes – Effective date May 20, 2013 .................................................................................... 117 
New Record Type Added ................................................................................................................................117 
 

---

## Page 6

Profile Security Database – Fixed Length Record Layouts 
History of Important Notices 6 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notice 
September 20, 2023 Record rebranded and reviewed.  
May 1, 2023 MFPSII [[participant]] Profile database was decommissioned.  
Please See Important Notice a9279 P&S 8852 Dated March 21, 2023 
 
There were two versions of User File Request (080) records.  As part 
of decommissioning of [[participant]] Database, the 080 record within 
this guide was moved to MFPS2 Part 6 records 
March 28, 2022 a9044 P&S 8617 Dated September 2, 2021 
August 26, 2019 a8711 P&S 8286 dated May 30, 2019 
March 25, 2019 a8658 P&S 8233 dated December 19, 2018 
July 13, 2018 a8584 P&S 8159 dated July 13, 2018 
July 9, 2018 a8532 P&S 8107 dated March 20, 2018 (revised May 9, 2018) 
August 22, 2016 a8227 P&S 7802 dated July 11, 2016 
May 31, 2016  a8163 P&S 7738 dated February 10, 2016 
November 30, 2015  a8073 P&S 7648 dated August 27, 2015 
September 22, 2014 &  
October 6, 2014 
a7876 P&S 7446 dated July 31, 2014 
July 28, 2014 a7825 P&S 7395 dated April 24, 2014 
June 30, 2014 a7702 P&S 7372 dated March 20, 2014 
Target second quarter 2014 a7699 P&S 7369 dated March 14, 2014 
May 20, 2013 a7608 P&S 7178 dated March 25, 2013 
May 20, 2013 a7608 P&S 7178 dated March 25, 2013 
November 24, 2008 a6717 P&S 6287 dated October 1, 2008 
August 18, 2008 a6675 P&S 6245 dated August 15, 2008  
a6650 P&S 6220 dated June 30, 2008  
a6640 P&S 6210 dated June 20, 2008  
a6614 P&S 6184 dated May 14, 2008 
March 27, 2006 a7171 P&S 5741 dated December 21, 2005 

---

## Page 7

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 7 
RECORD TYPE 020 – GENERAL PROFILE 
Record 1 of 10 (Required) 
Input/Output (Batch) 
(If Action Type = ‘D’, submit only records 1 & 2.) 
RECORD TYPE 020 – GENERAL PROFILE 
Record 1 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Reminder Indicator 6 6 1 A/N Output Only; Space on input 
‘R’ = Reminder on output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 020 = Security Issue General 
Profile Data  
R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 45 46 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue Check Digit 56 56 1 A/N @ R 0041 
Distribution Reinvestment 
Eligible Code 
57 57 1 A/N 0 = No 
1 = Yes 
R 0180 

---

## Page 8

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 8 
Record 1 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Distribution Reinvestment Load 
Code 
58 58 1 A/N 0 = No 
1 = Yes 
Req.'d if Distribution Reinvestment 
Eligible Code = ‘1’ 
OC 0522 
Redemption Amount Code 59 59 1 A/N 0 = [[shares]] 
1 = Dollars 
2 = Both 
R 0356 
Cross Fund Distribution 
Reinvestment Eligible Code 
60 60 1 A/N 0 = No 
1 = Yes 
R 0188 
Cross Fund Distribution 
Reinvestment Load Code 
61 61 1 A/N 0 = No 
1 = Yes 
Req.'d if Cross Fund Distribution 
Reinvestment Eligible Code = 1 
OC 0189 
Automatic Investment Eligible 
Code 
62 62 1 A/N 0 = No 
1 = Yes 
R 0523 
Automatic Withdrawal Eligible 
Code 
63 63 1 A/N 0 = No 
1 = Yes 
R 0524 
Filler  
 
  
64 67 4 A/N Space R  
DCC&S Eligible 68 68 1 A/N 0 = No 
1 = Yes 
R 0810 

---

## Page 9

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 9 
Record 1 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Defined Contribution Clearance 
& [[settlement]] (DCC&S) Cut-Off 
Cycle  
 
 
69 72 4 A/N 0001 = [[NSCC]] Cycle 01 
0002 = [[NSCC]] Cycle 02 
0003 = [[NSCC]] Cycle 03 
0004 = [[NSCC]] Cycle 04  
0005 = [[NSCC]] Cycle 05 
0006 = [[NSCC]] Cycle 06 
0007 = [[NSCC]] Cycle 07 
0008 = [[NSCC]] Cycle 08 
0009 = [[NSCC]] Cycle 09 
0010 = [[NSCC]] Cycle 10 
0011 = [[NSCC]] Cycle 11 
0012 = [[NSCC]] Cycle 12 
LF01 = [[NSCC]] Late File Cycle 01 
LF02 = [[NSCC]] late File Cycle 02 
LF03 = [[NSCC]] Late File Cycle 03 
LF98 = [[NSCC]] Late File Cycle 98 
 
Required if DCC&S Eligible  
field = 1 (Yes) 
OC 0811 
Filler 73 74 2 A/N Space R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 76 76 1 A/N Input: Space 
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

## Page 10

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 10 
Record 2 of 10 (Required) 
RECORD TYPE 020 – GENERAL PROFILE 
Field Name  Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @ R 0526 
Load Type Code 27 27 1 A/N 0 = Front-End Load 
1 = Back-End Load 
2 = Level Load 
3 = Hybrid 
4 = No Load 
5 = Load Other 
R 0154 
NAV Employee Code 28 28 1 A/N 0 = No 
1 = Yes 
R 0325 
NAV Wrap Code 29 29 1 A/N 0 = No 
1 = Yes 
R 0327 
ROA Eligible Code 30 30 1 A/N 0 = No 
1 = Yes 
R 0156 
Maximum Purchase Amount 31 46 16 N 99999999999999.99 R 0521 
Minimum Initial Purchase Amount 47 62 16 N 99999999999999.99 R 0166 
Minimum Subsequent Purchase Amount 63 78 16 N 99999999999999.99 R 0169 
Filler  79 80 2 A/N Space R  
 
 
  

---

## Page 11

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 11 
Record 3 of 10 (Required) 
RECORD TYPE 020 – GENERAL PROFILE 
Record 3 of 10 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
[[Dividend]] Accrual Purchase T+1 
Start Date Code 
 
 
67 67 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0812 
[[Dividend]] Accrual Redemption 
T+1 Stop Date Code 
 
 
68 68 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0813 
[[Dividend]] Accrual Partial 
Exchange Out Stop Date Code  
 
 
69 69 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0814 
[[Dividend]] Accrual Partial 
Exchange In Start Date Code 
 
  
70 70 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0815 

---

## Page 12

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 12 
Record 3 of 10 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
[[Dividend]] Accrual Partial 
Transfer Out Stop Date Code 
 
 
71 71 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0816 
[[Dividend]] Accrual ACAT Transfer 
In Start Date Code 
 
72 72 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0817 
[[Dividend]] Accrual ACAT Transfer 
Out Stop Date  
 
 
73 73 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0818 
DCC&S [[Dividend]] Accrual 
Purchase Start Date Code 
 
 
74 74 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0819 
DCC&S [[Dividend]] Accrual 
Purchase “G” indicator (Share 
Class Conversion) Start Date 
Code 
 
 
75 75 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0820 

---

## Page 13

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 13 
Record 3 of 10 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
DCC&S [[Dividend]] Accrual 
Purchase “L” indicator (Omnibus 
[[Dividend]] Reconciliation) Start 
Date Code 
 
 
76 76 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0821 
DCC&S [[Dividend]] Accrual 
Redemption Stop Date Code 
 
 
77 77 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0822 
DCC&S [[Dividend]] Accrual 
Redemption “G” indicator 
(Share Class Conversion) Stop 
Date Code 
 
 
78 78 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0823 
DCC&S [[Dividend]] Accrual 
Redemption “L” indicator 
(Omnibus [[Dividend]] 
Reconciliation) Stop Date Code 
 
 
79 79 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code 
= 1 or 2 
OC 0824 
Filler 80 80 1 A/N Space R  
 
 
  

---

## Page 14

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 14 
Record 4 of 10 (Required) 
RECORD TYPE 020 – GENERAL PROFILE 
Record 4 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 04 R 0080 
Filler 5 6 2 A/N Space R  
Minimum Coverdell IRA 
Purchase Amount 
7 22 16 N 99999999999999.99 R 0228 
Minimum Coverdell IRA 
Subsequent Purchase 
Amount 
23 38 16 N 99999999999999.99 R 0165 
Minimum Wrap Initial 
Purchase Amount 
39 54 16 N 99999999999999.99 R 0320 
Minimum Wrap Subsequent 
Purchase Amount 
55 70 16 N 99999999999999.99 R 0530 
Share Conversion Cycle 
Eligibility Method Code 
71 71 1 A/N 0 = Anniversary Day 
1 = Anniversary Month – First Day 
2 = Anniversary Month – Last Day 
3 = Anniversary Year 
4 = Month after Anniversary 
 
Req.’d if Share Conversion Cycle 
Code Not = ‘0’ 
OC 0533 

---

## Page 15

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 15 
Record 4 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Share Conversion Cycle 
Date  
72 73 2 A/N 01 – 31 = Day of Month 
FF = First Business Day 
LL = Last Business Day 
EM = Mondays 
ET = Tuesdays 
EW = Wednesdays 
ER = Thursdays 
EF = Fridays 
1M – 4M, LM = Mondays 
1T – 4T, LT = Tuesdays 
1W – 4W, LW = Wednesdays 
1R – 4R, LR = Thursdays 
1F – 4F, LF = Fridays  
 
Req.’d if Share Conversion Cycle 
Code Not = ‘0’ 
OC 0535 
Share Conversion Cycle 
Date Day Code 
74 74 1 A/N 0 = Next Business Day 
1 = Prior Business Day 
 
Req’d if “Share Conversion Cycle 
Date” not = (“FF” or “LL”) 
OC 0536 Eligible for Externalized 
Commission 
 
 
75 75 1 A/N 0 = No 
1 = Yes 
R 0825 
Large Trade Notification 
Required 
 
 
76 76 1 A/N 0 = No, Large Trade Notification is 
Not Required 
1 = Yes, Large Trade Notification is 
Required 
R 0826 
Filler 77 80 4 A/N  R  
 
 
  

---

## Page 16

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 16 
Record 5 of 10 (Required) 
RECORD TYPE 020 – GENERAL PROFILE 
Record 5 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 05 R 0080 
Filler 5 6 2 A/N Space R  
Minimum "Qualified Plans" 
Initial Purchase Amount 
7 22 16 N 99999999999999.99 R 0531 
Minimum "Qualified Plans" 
Subsequent Purchase Amount 
23 38 16 N 99999999999999.99 R 0532 
Maximum Account Value 39 54 16 N 99999999999999.99 R 0538 
Maximum Account Value Code 55 55 1 A/N 0 = Fund Complex 
1 = Share Class 
2 = Individual Security Issue [[ID]] 
R 0539 
Share Conversion Cycle Code 56 56 1 A/N 0 = [[shares]] [[DO]] Not Convert 
1 = Weekly 
2 = Monthly 
3 = Quarterly 
4 = Semi-Annually 
5 = Annually 
R 0218 
Share Conversion Age 57 59 3 N 999 
Req.’d if Share Conversion Cycle 
Code is NOT = 0  
OC 0540 
Share Conversion Cycle 
Starting Month 
60 61 2 N 99 
Req.’d if Share Conversion Cycle 
Code equal to ‘3’, or ‘4’, or ‘5’ 
OC 0541 
NAV Repurchase Code 62 62 1 A/N 0 = No 
1 = Yes, Same class Only 
2 = Yes, Different class Only 
3 = Yes, Same or Different Class 
R 0324 
NAV Repurchase Days 63 65 3 N 999 
Req.’d if NAV Repurchase Code = 
“1”, “2” or “3” 
OC 0543 
Filler 66 66 1 A/N Space R  

---

## Page 17

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 17 
Record 5 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
NAV Repurchase Frequency 
Code 
67 68 2 A/N 01 = Once per year 
02 = Twice per year 
03 = No restrictions 
04 = Once in a lifetime 
98 = Other (see Prospectus) 
 
Req.’d if NAV Repurchase  
Code = ‘1’ , ‘2’ or ‘3’ 
OC 0546 
CDSC Rules Apply Code 69 69 1 A/N 0 = No 
1 = Yes 
2 = Yes, Finder’s Fee / Jumbo 
Purchases Only 
 
 
R 0509 
Breakpoint Rules Apply Code 70 70 1 A/N 0 = No 
1 = Yes 
R 0510 
12b-1 Commission Rules Apply 
Code 
71 71 1 A/N 0 = No 
1 = Yes 
R 0511 
LOI Rules Apply Code 72 72 1 A/N 0 = No 
1 = Yes 
R 0512 
[[Dividend]] Accrual Full 
Exchange In Start Date Code 
 
 
73 73 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Req’d if 
[[Dividend]] Type Code = 1 or 2 
OC 0636 
[[Dividend]] Accrual Full 
Exchange Out Stop Date Code 
 
 
74 74 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Req’d if 
[[Dividend]] Type Code = 1 or 2 
OC 0637 

---

## Page 18

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 18 
Record 5 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[Dividend]] Accrual Full Transfer 
IN Start Date Code 
 
  
75 75 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Req’d if 
[[Dividend]] Type Code = 1 or 2 
OC 0638 
[[Dividend]] Accrual Partial 
Transfer IN Start Date Code 
 
 
76 76 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Req’d if 
[[Dividend]] Type Code = 1 or 2 
OC 0639 
[[Dividend]] Accrual Full Transfer 
OUT Stop Date Code 
 
 
77 77 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Req’d if 
[[Dividend]] Type Code = 1 or 2 
OC 0640 
Number of Eligible Social 
Codes 
78 80 3 N 999 R 0641 
 
 
  

---

## Page 19

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 19 
Record 6 of 10 (Required) 
RECORD TYPE 020 – GENERAL PROFILE 
Record 6 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 06 R 0080 
Filler 5 6 2 A/N Space R  
Product Type Code 7 8 2 A/N 01 = Mutual Fund 
02 = Money Market Mutual Fund 
03 = [[UIT]] (Unit Investment Trust) 
04 = Closed-End Mutual Fund 
05 = GIC (Guaranteed Investment 
Contract) 
06 = Stable Value Fund 
07 = Separate Account 
08 = Bank Collective Trust 
09 = Offshore (NRA) Fund 
10 = BIC (Bank Investment Contract) 
11 = Section 529 College Savings Plan 
12 = Offshore U.S. Dollar Enhanced ( 
[[DO]] not use- domestic funds on Profile 
Security only) 
13 = Offshore Non-U.S. Dollar 
Enhanced ( [[DO]] not use – domestic 
funds on Profile Security only) 
14 = Annuity (with underlying mutual 
funds) 
15 = Section 529 Money Market Fund 
48 = Interval Fund 
 
Best Practice: When Product Type 
Code = 02 (Money Market Mutual 
Fund) or 15 (Section 529 Money 
Market Fund), Record Type 033 - 
‘Money Market Fund Data’ should also 
be submitted. 
R 0227 
Investment Class Code 9 10 2 A/N See Appendix A R 0157 
Date of Current Prospectus 11 18 8 A/N ccyymmdd R 0236 
Date of Most Recent 
Prospectus Supplement 
19 26 8 A/N ccyymmdd R 0614 

---

## Page 20

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 20 
Record 6 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Offering Type Code 27 27 1 A/N 0 = Continuous 
1 = Selling Period 
R 0173 
Purchase Eligibility Code 28 28 1 A/N 0 = All (New and Existing) 
1 = Existing Only 
2 = Closed 
3 = Restrictions Apply (see 
Prospectus) 
R 0197 
Restricted Redemption 
Code 
29 29 1 A/N 0 = No 
1 = Yes 
R 0198 
Exchange Buy Eligibility 
Code 
30 30 1 A/N 0 = All (New and Existing) 
1 = Existing Only 
2 = Closed 
3 = Restrictions Apply (see 
Prospectus) 
 
R 0362 
Exchange Sell Eligibility 
Code 
31 31 1 A/N 0 = No 
1 = Yes 
R 0616 
Redemption Fee Code 32 32 1 A/N 0 = No Non-Short-Term Redemption 
Fee 
1 = Percentage 
2 = Fixed Dollar 
R 0184 
Redemption Fee Amount 33 48 16 N 99999999999999.99 
Req’d if Redemption Fee Code = 2 
OC 0185 
Redemption Fee 
Percentage 
49 53 5 N 99.999 
Req’d if Redemption Fee Code = 1 
OC 0615 
Selling Period Open Date 54 61 8 A/N ccyymmdd R 0210 
Minimum Periodic/ 
Systematic Investment 
Purchase Amount 
62 77 16 N 99999999999999.99 R 0537 
NAV Repurchase CDSC 
Reimbursement Code 
78 78 1 A/N 0 = Not applicable 
1 = Not reimbursed 
2 = Reimbursed 
3 = Reimbursed through purchase of 
additional [[shares]] at NAV 
 
Req.’d if NAV Repurchase Code = ‘1’, 
‘2’, or ‘3’ 
OC 0545 

---

## Page 21

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 21 
Record 6 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[Dividend]] Accrual Bulk Rate 
Method Code 
79 79 1 A/N 0 = Prior Business Day 
1 = Next Business Day 
2 = Not Applicable; Individual Rates 
Provided 
Req’ d If [[Dividend]] Type Code = ‘1’ or = 
‘2’ 
OC 0633 
[[Dividend]] Accrual Month 
End Bulk Rate Method 
Code 
80 80 1 A/N 0 = Prior Business Day 
1 = Next Business Day 
2 = Split Prior/Next Business Day 
3 = Not Applicable; Individual Rates 
Provided  
 
Req’ d If [[Dividend]] Type Code = ‘1’ or = 
‘2’ 
OC 0634 
 
 
  

---

## Page 22

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 22 
Record 7 of 10 (Required) 
RECORD TYPE 020 – GENERAL PROFILE 
Record 7 of 10  
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
3 4 2 A/N 07 R 0080 
Filler 5 6 2 A/N Space R  
Selling Period Close 
Date 
7 14 8 A/N ccyymmdd R 0211 
[[Dividend]] Type Code 15 15 1 A/N 0 = Record Date 
1 = Daily Accrual 
2 = Compounded Daily Accrual 
3 = Fund Does Not Pay 
Dividends 
R 0212 
[[Dividend]] Accrual 
Purchase T+2 Start 
Date Code 
 
 
16 16 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1 
Req’d if 
[[Dividend]] Type Code = 1 or 2 
OC 0617 
[[Dividend]] Accrual 
Redemption T+2 Stop 
Date Code 
 
 
17 17 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
 
Req’d if 
[[Dividend]] Type Code = 1 or 2 
OC 0618 
[[Dividend]] Frequency 
Code 
18 18 1 A/N 0 = Monthly 
1 = Quarterly 
2 = Semi-Annually 
3 = Annually 
 
Req’d if [[Dividend]] Type Code Not 
= 3 
OC 0213 

---

## Page 23

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 23 
Record 7 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Exchange Fee Code 19 19 1 A/N 0 = No Exchange Fee 
1 = Percentage 
2 = Fixed Dollar 
R 0149 
Exchange Fee Amount 20 35 16 N 99999999999999.99 
Req’d if Exchange Fee Code = 2 
OC 0150 
Exchange Fee 
Percentage 
36 40 5 N 99.999 
Req’d if Exchange Fee Code = 1 
OC 0619 
Large Trade Threshold 
Dollar Amount 
 
 
41 56 16 N 99999999999999.99 
Required if Large Trade 
Notification Required = 1 (Yes) 
OC 0827 
Fund Status Code 57 57 1 A/N 0 = Open 
1 = Closed – Liquidated 
2 = Closed - Merged 
R 0239 
STR Rules Apply Code 58 58 1 A/N 0 = No 
1 = Yes 
R 0621 
Symbol 59 70 12 A/N Req’ if “Symbol Code” not = “2” OC 0163 
Symbol Code 71 71 1 A/N 0 = Fund Created 
1 = [[NASDAQ]] 
2 = Proposed 
3= Not Applicable 
R 0507 
Internal Fund Number 72 79 8 A/N  R 0200 
ROA/ LOI Aggregation 
Inclusion Code 
 
 
80 80 1 A/N 0 = No 
1 = ROA (Renamed) 
2 = LOI  (New Value) 
3 = ROA & LOI  (New Value) 
R 0632 
 
 
  

---

## Page 24

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 24 
Record 8 of 10 (Required) 
RECORD TYPE 020 – GENERAL PROFILE 
Record 8 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 08 R 0080 
Filler 5 6 2 A/N Space R  
Share Conversion 
Receiving Security [[ID]] 
7 18 12 A/N Req.’d if Share Conversion Cycle 
Code in “020” Not = ‘0’ 
OC 0219 
Merged Security [[ID]] 19 30 12 A/N Req.’d if Fund Status Code in  
“020” = ‘2’ 
OC 0241 
Statement Security [[ID]] Short 
Name 
31 40 10 A/N  R 0628 
Statement Security [[ID]] 
Medium Name 
41 60 20 A/N  R 0629 
NAV Repurchase Share 
Class 
61 80 20 A/N Req.’d If NAV Repurchase Code = ‘2’ 
or ‘3’  
OC 0542 
 
 
  

---

## Page 25

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 25 
Record 9 of 10 (Required) 
RECORD TYPE 020 – GENERAL PROFILE 
Record 9 of 10 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 09 R 0080 
Filler 5 6 2 A/N Space R  
Fund Family Brand Name 7 66 60 A/N  R 0528 
Fiscal Year-End Day 67 70 4 N mmdd R 0613 
NAV Repurchase Account 
Eligibility Code 
71 72 2 A/N 01 = Same account where 
redemption occurred 
02 = Any account with the same 
registration 
03 = Any account eligible to be 
linked for ROA 
 
Req.’d if NAV Repurchase  
Code = ‘1’, ‘2’ or ‘3’ 
OC 0544 
CDSC Aging Applies 73 73 1 A/N 0 = No 
1 = Yes 
R 0697 
Filler 74 80 7 A/N  R  
 
 
  

---

## Page 26

Profile Security Database – Fixed Length Record Layouts 
Record Type 020 – General Profile 26 
Record 10 of 10 (Required) 
RECORD TYPE 020 – GENERAL PROFILE 
Record 10 of 10  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 10 R 0080 
Filler 5 6 2 A/N Space R  
Statement Security [[ID]] Long Name 7 46 40 A/N  R 0630 
Minimum IRA/Roth IRA Initial Purchase 
Amount 
47 62 16 N 99999999999999.99 R 0355 
Minimum IRA/Roth IRA Subsequent 
Purchase Amount 
63 78 16 N 99999999999999.99 R 0354 
NAV Purchases Eligible for ROA Code 79 79 1 A/N 0 = No 
1 = Yes 
R 0475 
NAV Purchases Eligible for LOI Code 80 80 1 A/N 0 = No 
1 = Yes 
R 0476 

---

## Page 27

Profile Security Database – Fixed Length Record Layouts 
Record Type 021 – Blue Sky Data 27 
RECORD TYPE 021 – BLUE SKY DATA 
Record 1 of 4 (Required) 
Input/Output (Batch) 
(If Action Type = ‘D’, submit only records 1 & 2.) 
Record Type 021 – Blue Sky Data 
Record 1 of 4   
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Reminder Indicator 6 6 1 A/N Output Only; Space on input 
‘R’ = Reminder on Output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 021 = Security Issue Blue Sky R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 45 46 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue Check Digit 56 56 1 A/N @ R 0041 
Blue Sky Eligible State Postal 
Code 1 
57 58 2 A/N Standard Fund/SERV State 
Code  
R 0242 
Blue Sky Eligible State Postal 
Code 2 
59 60 2 A/N Standard Fund/SERV State 
Code  
O 0242 

---

## Page 28

Profile Security Database – Fixed Length Record Layouts 
Record Type 021 – Blue Sky Data 28 
Record 1 of 4   
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Blue Sky Eligible State Postal 
Code 3 
61 62 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 4 
63 64 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 5 
65 66 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 6 
67 68 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 7 
69 70 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 8 
71 72 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 9 
73 74 2 A/N  R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 76 76 1 A/N Input: Space 
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

## Page 29

Profile Security Database – Fixed Length Record Layouts 
Record Type 021 – Blue Sky Data 29 
Record 2 of 3 (Required) 
Record Type 021 – Blue Sky Data 
Record 2 of 3  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @ R 0526 
Blue Sky Eligible State Postal 
Code 10 
27 28 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 11 
29 30 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 12 
31 32 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 13 
33 34 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 14 
35 36 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 15 
37 38 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 16 
39 40 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 17 
41 42 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 18 
43 44 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 19 
45 46 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 20 
47 48 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 21 
49 50 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 22 
51 52 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 23 
53 54 2 A/N Standard Fund/SERV State 
Code  
O 0242 

---

## Page 30

Profile Security Database – Fixed Length Record Layouts 
Record Type 021 – Blue Sky Data 30 
Record 2 of 3  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Blue Sky Eligible State Postal 
Code 24 
55 56 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 25 
57 58 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 26 
59 60 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 27 
61 62 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 28 
63 64 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 29 
65 66 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 30 
67 68 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 31 
69 70 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 32 
71 72 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 33 
73 74 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 34 
75 76 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 35 
77 78 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 36 
79 80 2 A/N Standard Fund/SERV State 
Code  
O 0242 
 
 
  

---

## Page 31

Profile Security Database – Fixed Length Record Layouts 
Record Type 021 – Blue Sky Data 31 
Record 3 of 4 (Required) 
Record Type 021 – Blue Sky Data 
Record 3 of 4  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Blue Sky Eligible State Postal 
Code 37 
67 68 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 38 
69 70 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 39 
71 72 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 40 
73 74 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 41 
75 76 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 42 
77 78 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 43 
79 80 2 A/N Standard Fund/SERV State 
Code  
O 0242 
 
 
  

---

## Page 32

Profile Security Database – Fixed Length Record Layouts 
Record Type 021 – Blue Sky Data 32 
Record 4 of 4 (Optional) 
Record Type 021 – Blue Sky Data 
Record 4 of 4  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 04 R 0080 
Filler 5 6 2 A/N Space R  
Blue Sky Eligible State Postal 
Code 44 
7 8 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 45 
9 10 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 46 
11 12 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 47 
13 14 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 48 
15 16 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 49 
17 18 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 50 
19 20 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 51 
21 22 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 52 
23 24 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 53 
25 26 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 54 
27 28 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 55 
29 30 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 56 
31 32 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 57 
33 34 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 58 
35 36 2 A/N Standard Fund/SERV State 
Code  
O 0242 

---

## Page 33

Profile Security Database – Fixed Length Record Layouts 
Record Type 021 – Blue Sky Data 33 
Record 4 of 4  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Blue Sky Eligible State Postal 
Code 59 
37 38 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 60 
39 40 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 61 
41 42 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 62 
43 44 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 63 
45 46 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Filler 47 80 34 A/N  R  

---

## Page 34

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 34 
RECORD TYPE 022 – CDSC DATA 
Record 1 of 18 (Required) 
Input/Output (Batch) 
Record Type 022 – CDSC Data 
Record 1 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Reminder Indicator 6 6 1 A/N Output Only; Space on Input. 
‘R’ = Reminder on Output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security 
Issue 
R 0082 
Record Type 10 12 3 A/N 022 = Security Issue CDSC 
Data  
R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 45 46 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue Check Digit 56 56 1 A/N @ R 0041 
Advanced Commission Rate 
(formerly CDSC Commission Rate) 
57 65 9 N 99.9999999 R 0547 
CDSC Death Waiver Code 66 66 1 A/N 0 = No 
1 = Yes 
R 0341 

---

## Page 35

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 35 
Record 1 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
CDSC Disability Waiver Code 67 67 1 A/N 0 = No 
1 = Yes 
R 0342 
CDSC Divorce Waiver Code 68 68 1 A/N 0 = No 
1 = Yes 
R 0367 
CDSC Correction Waiver Code 69 69 1 A/N 0 = No 
1 = Yes 
R 0179 
Filler 70 74 5 A/N  R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
R  
[[NSCC]] Reject Code  77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 36

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 36 
Record 2 of 18 (Required) 
Record Type 022 – CDSC Data 
Record 2 of 18 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @ R 0526 
CDSC Systematic Withdrawal 
Waiver Code 
27 27 1 A/N 0 = No 
1 = Yes 
R 0549 
CDSC Defined Contribution Waiver 
Code 
28 28 1 A/N 0 = No 
1 = Yes 
R 0550 
CDSC Hardship Waiver Code 29 29 1 A/N 0 = No 
1 = Yes 
R 0551 
CDSC Termination Distribution 
Waiver Code 
30 30 1 A/N 0 = No 
1 = Yes 
R 0552 
CDSC Involuntary Distribution 
Waiver Code 
31 31 1 A/N 0 = No 
1 = Yes 
R 0553 
CDSC Forfeiture Distribution 
Waiver Code 
32 32 1 A/N 0 = No 
1 = Yes 
R 0554 
CDSC Loan Distribution Waiver 
Code 
33 33 1 A/N 0 = No 
1 = Yes 
R 0555 
CDSC Excess Contribution 
Distribution Waiver Code 
34 34 1 A/N 0 = No 
1 = Yes 
R 0556 
CDSC Qualified Distribution 
Waiver Code 
35 35 1 A/N 0 = No 
1 = Yes 
R 0557 
CDSC Qualified Distribution 
Waiver Age 
36 38 3 N 99.9 
Req.’d if CDSC Qualified 
Distribution Waiver Code = ‘1’ 
OC 0558 

---

## Page 37

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 37 
Record 2 of 18 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
CDSC Aging Method Code 39 39 1 A/N 0 = Anniversary Date 
1 = Anniversary Month - 1st 
Day 
2 = Anniversary Month - Last 
Day 
3 = Anniversary Year 
4 = Month after Anniversary 
R 0559 
CDSC Calculation Method Code 40 40 1 A/N 0 = Lower of Cost or Market 
1 = Higher of Cost or Market 
2 = Current Market 
3 = Original Cost 
4 = Use Accumulated Dollars 
R 0560 
CDSC Redemption Hierarchy 
Method Code (assumption is free 
[[shares]] always first) 
41 41 1 A/N 0 = Lot Level Appreciation 
1 = Account Level Appreciation 
2 = Proportional Lot 
3 = Preferred Lot 
4 = Breakpoint Lot 
5 = Reverse Lot Level 
Appreciation 
6 = Commissionable Dollars 
Appreciation 
7 = Commission and Free 
Dollars Appreciation 
8 = Lot Level Depreciation Only 
R 0561 
CDSC Exchange Hierarchy 
Method Code 
42 42 1 A/N 0 = Lot Level Appreciation 
1 = Account Level Appreciation 
2 = Proportional Lot 
3 = Preferred Lot 
4 = Breakpoint Lot 
5 = Reverse Lot Level 
Appreciation 
6 = Commissionable Dollars 
Appreciation 
7 = Commission and Free 
Dollars Appreciation 
8 = Lot Level Depreciation Only 
R 0562 

---

## Page 38

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 38 
Record 2 of 18 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
CDSC Transfer Hierarchy Method 
Code 
43 43 1 A/N 0 = Lot Level Appreciation 
1 = Account Level Appreciation 
2 = Proportional Lot 
3 = Preferred Lot 
4 = Breakpoint Lot 
5 = Reverse Lot Level 
Appreciation 
6 = Commissionable Dollars 
Appreciation 
7 = Commission and Free 
Dollars Appreciation 
R 0563 
CDSC Exchange Buy Aging 
Schedule Code 
44 44 1 A/N 0 = Use Buy Fund Schedule 
1 = Retain Sell Fund Schedule 
2 = Longer of Buy or Sell Fund 
Schedule 
3 = Shorter of Buy or Sell Fund 
Schedule 
R 0564 
CDSC Aging Start Date 45 45 1 A/N 0 = Trade Date 
1 = [[settlement]] Date 
R 0565 
CDSC Death Waiver Time Period 46 47 2 N In months 
Req.’d if CDSC Death Waiver 
Code = ‘1’ 
OC 0566 
CDSC Required Minimum 
Distribution Amount Code 
48 48 1 A/N 0 = Waived on Fund Amount 
1 = Waived on Full Amount 
 
Req.’d if CDSC Qualified 
Distribution Waiver Code = 1 
OC 0567 Number of CDSC Schedules 49 50 2 N 99 
Maximum 5 Schedules 
R 0568 
CDSC Free Systematic Withdrawal 
Waiver Percentage 
51 55 5 N 999.99 
Req’d if CDSC Systematic 
Withdrawal Waiver Code = ‘1’ 
O/C 0694 

---

## Page 39

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 39 
Record 2 of 18 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Alternate CDSC / Compensation 
Schedule Exists 
56 56 1 A/N 0 = No 
1 = Yes – waived dealer 
concession, no CDSC, 
immediate trails 
R 0695 
Filler 57 80 24 A/N  R  
 
 
  

---

## Page 40

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 40 
Record 3 of 18 (Required) 
Record Type 022 – CDSC Data 
Record 3 of 18 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Filler 67 80 14 A/N  R  
 
 
  

---

## Page 41

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 41 
Record 4 of 18 (Required) 
Record Type 022 – CDSC Data 
Record 4 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 04 R 0080 
Filler 5 6 2 A/N Space R  
CDSC Schedule 1 Lower Limit 7 22 16 N 99999999999999.99 R 0569 
CDSC Schedule 1 Upper Limit  23 38 19 N 99999999999999.99 R 0570 
Number of CDSC rates in Schedule 1 39 40 2 N 99 
Maximum 15 Rates 
R 0571 
CDSC Schedule 1 Share Age-1  41 43 3 N 999 R 0245 
CDSC Schedule 1 Rate-1 44 52 9 N 99.9999999 R 0246 
CDSC Schedule 1 Share Age-2 53 55 3 N 999 O 0245 
CDSC Schedule 1 Rate-2 56 64 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-3 65 67 3 N 999 O 0245 
CDSC Schedule 1 Rate-3 68 76 9 N 99.9999999 O 0246 
Filler 77 80 4 A/N  R  
 
 
  

---

## Page 42

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 42 
Record 5 of 18 (Optional) 
Record Type 022 – CDSC Data 
Record 5 of 18  
Field Name 
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 05 R 0080 
Filler 5 6 2 A/N Space R  
CDSC Schedule 1 Share Age-4  7 9 3 N 999 O 0245 
CDSC Schedule 1 Rate-4 10 18 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-5 19 21 3 N 999 O 0245 
CDSC Schedule 1 Rate-5 22 30 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-6 31 33 3 N 999 O 0245 
CDSC Schedule 1 Rate-6 34 42 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-7 43 45 3 N 999 O 0245 
CDSC Schedule 1 Rate-7 46 54 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-8 55 57 3 N 999 O 0245 
CDSC Schedule 1 Rate-8 58 66 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-9 67 69 3 N 999 O 0245 
CDSC Schedule 1 Rate-9 70 78 9 N 99.9999999 O 0246 
Filler 79 80 2 A/N  R  
 
 
  

---

## Page 43

Profile Security Database – Fixed Length Record Layouts 
Record Type 022 – CDSC Data 43 
Record 6 of 18 (Optional) 
Record Type 022 – CDSC Data 
Record 6 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 06 R 0080 
Filler 5 6 2 A/N Space R  
CDSC Schedule 1 Share Age-10  7 9 3 N 999 O 0245 
CDSC Schedule 1 Rate-10 10 18 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-11 19 21 3 N 999 O 0245 
CDSC Schedule 1 Rate-11 22 30 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-12 31 33 3 N 999 O 0245 
CDSC Schedule 1 Rate-12 34 42 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-13 43 45 3 N 999 O 0245 
CDSC Schedule 1 Rate-13 46 54 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-14 55 57 3 N 999 O 0245 
CDSC Schedule 1 Rate-14 58 66 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-15 67 69 3 N 999 O 0245 
CDSC Schedule 1 Rate-15 70 78 9 N 99.9999999 O 0246 
Filler 79 80 2 A/N  R  
Records 4 to 6 Above Can Repeat for Up to 5 Schedules as Follows: 
Schedule 2 – Record 7 through 9 
Schedule 3 – Record 10 through 12 
Schedule 4 – Record 13 through 15 
Schedule 5 – Record 16 through 18 

---

## Page 44

Profile Security Database – Fixed Length Record Layouts 
Record Type 023 – Breakpoint Schedules 44 
RECORD TYPE 023 – BREAKPOINT SCHEDULES 
Record 1 of 13 (Required) 
Input/Output (Batch) 
(If Action Type = ‘D’, submit only records 1 & 2) 
Record Type 023 – Breakpoint Schedules 
Record 1 of 13 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Reminder Indicator 6 6 1 A/N Output Only; Space on 
input 
‘R’ = Reminder on 
Output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical 
Security Issue 
R 0082 
Record Type 10 12 3 A/N 023 = Security Issue 
Breakpoint Schedule 
Data  
R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 45 46 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue Check Digit 56 56 1 A/N @ R 0041 

---

## Page 45

Profile Security Database – Fixed Length Record Layouts 
Record Type 023 – Breakpoint Schedules 45 
Record 1 of 13 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Finder’s Fee/Jumbo Breakpoint Blending 
Applies Code  
(formerly Breakpoint Blending Applies 
Code) 
57 57 1 A/N 0 = No 
1 = Yes 
R 0610 
Number of Breakpoints 58 59 2 N 99 
maximum 10 breakpoints 
R 0247 
Filler 60 74 15 A/N  R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
R  
[[NSCC]] Reject Code  77 80 4 A/N Input: Space 
Output: Reject code or 
space 
R  
 
 
  

---

## Page 46

Profile Security Database – Fixed Length Record Layouts 
Record Type 023 – Breakpoint Schedules 46 
Record 2 of 13 (Required) 
Record Type 023 – Breakpoint Schedules 
Record 2 of 13  
Field Name 
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @ R 0526 
Filler 27 80 54 A/N  R  
 
 
  

---

## Page 47

Profile Security Database – Fixed Length Record Layouts 
Record Type 023 – Breakpoint Schedules 47 
Record 3 of 13 (Required) 
Record Type 023 – Breakpoint Schedules 
Record 3 of 13 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Filler 67 80 14 A/N  R  
 
 
  

---

## Page 48

Profile Security Database – Fixed Length Record Layouts 
Record Type 023 – Breakpoint Schedules 48 
Records 4 of 13 (Required) 
Record Type 023 – Breakpoint Schedules 
Records 4 of 13  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 04 R 0080 
Filler 5 6 2 A/N Space R  
Breakpoint Minimum Account Value 7 22 16 N 99999999999999.99 R 0248 
Breakpoint Maximum Account Value 23 38 16 N 99999999999999.99 R 0249 
Breakpoint Sales Charge Rate 39 43 5 N 99.999 R 0611 
Breakpoint Dealer Concession Rate 44 48 5 N 99.999 R 0251 
Breakpoint [[underwriter]] Rate 49 53 5 N 99.999 R 0612 
Filler 54 80 27 A/N  R  
 
 
  

---

## Page 49

Profile Security Database – Fixed Length Record Layouts 
Record Type 023 – Breakpoint Schedules 49 
Records 4 Through 13 (Optional) 
(The previous record (#4) may repeat itself 9 more times for 9 additional Breakpoint Schedules.)  
Logical Sequence Numbers should be:  If Number of Breakpoints is greater than: 
Breakpoint Schedule 2 - Logical Sequence Number: 5 1 
Breakpoint Schedule 3 - Logical Sequence Number: 6 2 
Breakpoint Schedule 4 - Logical Sequence Number: 7 3 
Breakpoint Schedule 5 - Logical Sequence Number: 8 4 
Breakpoint Schedule 6 - Logical Sequence Number: 9 5 
Breakpoint Schedule 7 - Logical Sequence Number: 10 6 
Breakpoint Schedule 8 - Logical Sequence Number: 11 7 
Breakpoint Schedule 9 - Logical Sequence Number: 12 8 
Breakpoint Schedule 10 - Logical Sequence Number: 13 9 

---

## Page 50

Profile Security Database – Fixed Length Record Layouts 
Record Type 024 – Commission Data 50 
RECORD TYPE 024 – COMMISSION DATA 
Record 1 of 18 (Required) 
Input/Output (Batch) 
(If Action Type = ‘D’, submit only records 1 & 2) 
Record Type 024 – Commission Data 
Record 1 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Reminder Indicator 6 6 1 A/N Output Only; Space on Input.  
‘R’ = Reminder on Output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 024 = Security Issue Commission 
Data  
R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 45 46 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
56 56 1 A/N @ R 0041 
12b-1 Payment Frequency 
Code 
57 57 1 A/N 0 = Monthly 
1 = Quarterly 
2 = Semi-Annually 
3 = Annually 
R 0269 

---

## Page 51

Profile Security Database – Fixed Length Record Layouts 
Record Type 024 – Commission Data 51 
Record 1 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
12b-1 Redemption Hierarchy 
Code 
58 58 1 A/N 0 = First In/First Out (FIFO) 
1 = Last In/First Out (LIFO) 
2 = Proportional 
R 0268 
12b-1 Calculation Method 
Code 
59 59 1 A/N 0 = Average Daily Basis 
1 = Record Date [[shares]] 
R 0252 
12b-1 Average Daily [[Asset]] 
Calculation Start Day 
60 61 2 A/N 01 -31 = Day of Month 
FF = First Business Day 
LL = Last Business Day 
Req.’d If 12b-1 Calculation Method 
Code = ‘0’ 
OC 0572 
12b -1 Record Date  62 63 2 A/N 01 -30 = Day of Month 
FF = First Business Day 
LL = Last Business Day 
LC = Last Calendar Day 
Req.’d If 12b-1 Calculation Method 
Code = ‘1’ 
OC 0573 
12b-1 Record Date Day Code 64 64 1 A/N 0 = Next Business Day 
1 = Prior Business Day 
 
Req’ d If 12b-1 Record Date 
not=’FF’ or not=’LL’ 
OC 0574 
12b-1 Start Month 65 66 2 N Req’d if 12b-1 Payment  
Frequency Code = ‘1’ or ‘2’ or ‘3’ 
 0575 
12b-1 [[Dividend]] Share Aging 
Code 
67 67 1 A/N 0 = No 
1 = Yes 
R 0576 
Filler 68 74 7 A/N  R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 

---

## Page 52

Profile Security Database – Fixed Length Record Layouts 
Record Type 024 – Commission Data 52 
Record 1 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[NSCC]] Rejection Indicator 76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
R  
[[NSCC]] Reject Code  77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 53

Profile Security Database – Fixed Length Record Layouts 
Record Type 024 – Commission Data 53 
Record 2 of 18 (Required) 
Record Type 024 – Commission Data 
Record 2 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @ R 0526 
Number of 12b-1 Agreements 27 29 3 N 999 
maximum 5 Agreements 
R 0579 
Filler 30 80 51 A/N  R  
 
 
  

---

## Page 54

Profile Security Database – Fixed Length Record Layouts 
Record Type 024 – Commission Data 54 
Record 3 of 18 (Required) 
Record Type 024 – Commission Data 
Record 3 of 18  
Field Name 
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Filler 67 80 14 A/N  R  
 
 
  

---

## Page 55

Profile Security Database – Fixed Length Record Layouts 
Record Type 024 – Commission Data 55 
Record 4 of 18 (Required) 
Record Type 024 – Commission Data 
Record 4 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 04 R 0080 
Filler 5 6 2 A/N Space R  
12b-1 Agreement 1 Date 7 14 8 A/N ccyymmdd 
@ 
R 0254 
12b-1 Post-Agreement 1 Rate 15 23 9 N 99.9999999 R 0255 
Number of 12b-1 Additional Rates for 
Agreement 1 
24 26 3 N maximum 15 rates R 0346 
Agreement 1 12b-1 Maximum Share Age 1 27 29 3 N In month R 0344 
Agreement 1 12b-1 Rate 1 30 38 9 N 99.9999999 R 0345 
Agreement 1 12b-1 Maximum Share Age 2 39 41 3 N In month O 0344 
Agreement 1 12b-1 Rate 2 42 50 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum Share Age 3 51 53 3 N In month O 0344 
Agreement 1 12b-1 Rate 3 54 62 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum Share Age 4 63 65 3 N In month O 0344 
Agreement 1 12b-1 Rate 4 66 74 9 N 99.9999999 O 0345 
Filler 75 80 6 A/N  R  
 
 
  

---

## Page 56

Profile Security Database – Fixed Length Record Layouts 
Record Type 024 – Commission Data 56 
Record 5 of 18 (Optional) 
Record Type 024 – Commission Data 
Record 5 of 18  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 05 R 0080 
Filler 5 6 2 A/N Space R  
Agreement 1 12b-1 Maximum Share Age 5 7 9 3 N In month R 0344 
Agreement 1 12b-1 Rate 5 10 18 9 N 99.9999999 R 0345 
Agreement 1 12b-1 Maximum Share Age 6 19 21 3 N In month O 0344 
Agreement 1 12b-1 Rate 6 22 30 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum Share Age 7 31 33 3 N In month O 0344 
Agreement 1 12b-1 Rate 7 34 42 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum Share Age 8 43 45 3 N In month O 0344 
Agreement 1 12b-1 Rate 8 46 54 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum Share Age 9 55 57 3 N In month O 0344 
Agreement 1 12b-1 Rate 9 58 66 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum Share Age 10 67 69 3 N In month O 0344 
Agreement 1 12b-1 Rate 10 70 78 9 N 99.9999999 O 0345 
Filler 79 80 2 A/N  R  
 
 
  

---

## Page 57

Profile Security Database – Fixed Length Record Layouts 
Record Type 024 – Commission Data 57 
Record 6 of 18 (Optional) 
Record Type 024 – Commission Data 
Record 6 of 18 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 06 R 0080 
Filler 5 6 2 A/N Space R  
Agreement 1 12b-1 Maximum Share Age 11 7 9 3 N In month R 0344 
Agreement 1 12b-1 Rate 11 10 18 9 N 99.9999999 R 0345 
Agreement 1 12b-1 Maximum Share Age 12 19 21 3 N In month O 0344 
Agreement 1 12b-1 Rate 12 22 30 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum Share Age 13 31 33 3 N In month O 0344 
Agreement 1 12b-1 Rate 13 34 42 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum Share Age 14 43 45 3 N In month O 0344 
Agreement 1 12b-1 Rate 14 46 54 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum Share Age 15 55 57 3 N In month O 0344 
Agreement 1 12b-1 Rate 15 58 66 9 N 99.9999999 O 0345 
Filler 67 80 14 A/N  R  
Records 4 to 6 Above Can Repeat for Up to 5 Agreements as Follows: 
Agreement 2 – Record 7 through 9 
Agreement 3 – Record 10 through 12 
Agreement 4 – Record 13 through 15 
Agreement 5 – Record 16 through 18 

---

## Page 58

Profile Security Database – Fixed Length Record Layouts 
Record Type 025 – [[NSCC]] Social Code Eligibility 58 
RECORD TYPE 025 – [[NSCC]] SOCIAL CODE ELIGIBILITY 
Record 1 of 3 (Required) 
Input/Output (Batch) 
(If Action Type = ‘D’, submit only records 1 & 2) 
Record Type 025 – [[NSCC]] Social Code Eligibility 
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
Reminder Indicator 6 6 1 A/N Output Only; Space on Input. ‘R’ = 
Reminder on Output 
R  
Originator Type 
Indicator 
7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 025 = Security Issue Purchase Eligibility 
Social Code Tables  
R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes 
Spaces for [[default]] 
O 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue 
Check Digit 
56 56 1 A/N @ R 0041 
Filler 57 74 18 A/N  R  

---

## Page 59

Profile Security Database – Fixed Length Record Layouts 
Record Type 025 – [[NSCC]] Social Code Eligibility 59 
Record 1 of 3  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection 
Indicator 
76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple Errors 
R  
[[NSCC]] Reject Code  77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 60

Profile Security Database – Fixed Length Record Layouts 
Record Type 025 – [[NSCC]] Social Code Eligibility 60 
Record 2 of 3 (Required) 
Record Type 025 – [[NSCC]] Social Code Eligibility 
Record 2 of 3  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @ R 0526 
Eligible Social Code 27 29 3 A/N Value entered in Cols 27 -29 will be 
validated except when entry is “ALL”. 
See Appendix B for valid [[NSCC]] 
Eligible Social Codes 
R 0614 
Eligibility Code 30 30 1 A/N 0 = Eligible, No Restrictions 
1 = Eligible, Restriction may apply 
2 = Eligible at NAV, Restriction may 
apply  
R 0615 
Eligible Date 31 38 8 A/N ccyymmdd 
Req’ d if Eligibility-Code not = ‘0’ 
OC 0645 
Number of Eligible 
Participants Minimum 
39 41 3 N 999 
(See Appendix C for edit criteria)  
OC 0646 
Number of Active 
Participants Minimum 
42 44 3 N 999 
(See Appendix C for edit criteria) 
OC 0647 
Minimum [[Asset]] Size for 
Eligibility 
45 60 16 N 99999999999999.99 
(See Appendix C for edit criteria) 
OC 0648 
Maximum [[Asset]] Size for 
Eligibility 
61 76 16 N 99999999999999.99 R 0649 
Relationship between 
[[participant]] Minimum and 
[[Asset]] Size 
77 77 1 A/N 0 = Both must be met 
1 = Either must be met 
(See Appendix C for Additional 
Validation Rules) 
O/C 0696 
Filler 78 80 3 A/N  R  
 
 
  

---

## Page 61

Profile Security Database – Fixed Length Record Layouts 
Record Type 025 – [[NSCC]] Social Code Eligibility 61 
Record 3 of 3 (Required) 
Record Type 025 – [[NSCC]] Social Code Eligibility 
Record 3 of 3 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Filler 67 80 14 A/N  R  

---

## Page 62

Profile Security Database – Fixed Length Record Layouts 
Record Type 026 –Short Term Redemption Data 62 
RECORD TYPE 026 –SHORT TERM REDEMPTION DATA 
Record 1 of 4 (Required) 
Input/Output (Batch) 
(If Action Type = ‘D’, submit only records 1 & 2.) 
Record Type 026 –Short Term Redemption Data 
Record 1 of 4 
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
Reminder Indicator 6 6 1 A/N Output Only; Space on Input. ‘R’ = 
Reminder on Output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 026 = Short Term Redemption Data  R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue 
Check Digit 
56 56 1 A/N @ R 0041 
STR Minimum Amount 57 72 16 N 99999999999999.99 R 0580 
STR Share Aging Method 
Code 
73 73 1 A/N 0 = Calendar Days 
1 = Business Days 
R 0581 

---

## Page 63

Profile Security Database – Fixed Length Record Layouts 
Record Type 026 –Short Term Redemption Data 63 
Record 1 of 4 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
STR Redemption 
Methodology Code 
74 74 1 A/N 0 = First In/First Out (FIFO) 
1 = Last In/First Out (LIFO) 
R 0582 
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple Errors 
R  
[[NSCC]] Reject Code  77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 64

Profile Security Database – Fixed Length Record Layouts 
Record Type 026 –Short Term Redemption Data 64 
Record 2 of 4 (Required) 
Record Type 026 –Short Term Redemption Data 
Record 2 of 4  
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @ R 0526 
STR Correction Waiver Code 27 27 1 A/N 0 = No 
1 = Yes 
R 0584 
STR Death Waiver Code 28 28 1 A/N 0 = No 
1 = Yes 
R 0585 
STR Disability Waiver Code 29 29 1 A/N 0 = No 
1 = Yes 
R 0586 
STR Qualified Distribution Waiver 
Code 
30 30 1 A/N 0 = No 
1 = Yes 
R 0587 
STR Qualified Distribution Waiver 
Age 
31 33 3 N 99.9 
Req’d if STR Qualified 
Distribution Waiver Code = “1” 
OC 0588 
STR Divorce Waiver Code 34 34 1 A/N 0 = No 
1 = Yes 
R 0589 
STR Systematic Withdrawal 
Waiver Code 
35 35 1 A/N 0 = No 
1 = Yes 
R 0590 
STR Defined Contribution Waiver 
Code 
36 36 1 A/N 0 = No 
1 = Yes 
R 0591 
STR Hardship Distribution Waiver 
Code 
37 37 1 A/N 0 = No 
1 = Yes 
R 0592 
STR Automatic Rebalance 
Waiver Code 
38 38 1 A/N 0 = No 
1 = Yes 
R 0593 
STR Termination Distribution 
Waiver Code 
39 39 1 A/N 0 = No 
1 = Yes 
R 0594 
STR Involuntary Distribution 
Waiver Code 
40 40 1 A/N 0 = No 
1 = Yes 
R 0595 

---

## Page 65

Profile Security Database – Fixed Length Record Layouts 
Record Type 026 –Short Term Redemption Data 65 
Record 2 of 4  
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
STR Forfeitures Distribution 
Waiver Code 
41 41 1 A/N 0 = No 
1 = Yes 
R 0596 
STR Loan Distribution Waiver 
Code 
42 42 1 A/N 0 = No 
1 = Yes 
R 0597 
STR Excess Contribution 
Distribution Waiver Code 
43 43 1 A/N 0 = No 
1 = Yes 
R 0598 
STR Wrap Fee Waiver Code 44 44 1 A/N 0 = No 
1 = Yes 
R 0599 
STR Plan Fee Waiver Code 45 45 1 A/N 0 = No 
1 = Yes 
R 0600 
STR Reinvested [[shares]] Waiver 
Code 
46 46 1 A/N 0 = No 
1 = Yes 
R 0601 
STR Exchange Buy Schedule 
Code 
47 47 1 A/N 0 = Retain Sell Fund Schedule 
1 = Use Buy Fund Schedule 
2 = Longer of Buy or Sell Fund 
Schedule 
3 = Shorter of Buy or Sell Fund 
Schedule 
R 0602 
STR Exchange Buy Aging Date 
Code 
48 48 1 A/N 0 = Original Date 
1 = Exchange Date 
R 0603 
STR Aging Start Date Code 49 49 1 A/N 0 = Trade Date 
1 = [[settlement]] Date 
R 0604 
STR Eligible Transaction Code 50 50 1 A/N 0 = Redemptions 
1 = Exchanges 
2 = Both 
R 0605 
STR Payout Calculation Amount 
Code 
51 51 1 A/N 0 = Net Proceeds 
1 = Gross Proceeds 
R 0606 
Number of STR Rates 52 54 3 N 999 R 0607 
Filler 55 80 26 A/N  R  
 
 
  

---

## Page 66

Profile Security Database – Fixed Length Record Layouts 
Record Type 026 –Short Term Redemption Data 66 
Record 3 of 4 (Required) 
Record Type 026 –Short Term Redemption Data 
Record 3 of 4 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Filler 67 80 14 A/N  R  
 
 
  

---

## Page 67

Profile Security Database – Fixed Length Record Layouts 
Record Type 026 –Short Term Redemption Data 67 
Record 4 of 4 (Required) 
Record Type 026 –Short Term Redemption Data 
Record 4 of 4 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 04 R 0080 
Filler 5 6 2 A/N Space R  
STR Share Age 1 7 9 3 N 999 R 0608 
STR Rate 1 10 18 9 N 99.9999999 R 0609 
STR Share Age 2 19 21 3 N 999 O 0608 
STR Rate 2 22 30 9 N 99.9999999 O 0609 
STR Share Age 3 31 33 3 N 999 O 0608 
STR Rate 3 34 42 9 N 99.9999999 O 0609 
STR Share Age 4 43 45 3 N 999 O 0608 
STR Rate 4 46 54 9 N 99.9999999 O 0609 
STR Share Age 5 55 57 3 N 999 O 0608 
STR Rate 5 58 66 9 N 99.9999999 O 0609 
Filler 67 80 14 A/N  R  

---

## Page 68

Profile Security Database – Fixed Length Record Layouts 
Record Type 029 – Linkage Rules Data 68 
RECORD TYPE 029 – LINKAGE RULES DATA 
Record 1 of 4 (Required) 
Input/Output (Batch) 
Record Type 029 – Linkage Rules Data 
Record 1 of 4 
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
Reminder Indicator 6 6 1 A/N Output Only; Space on input 
‘R’ = Reminder on output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 029 = Security Issue Breakpoint Linkage 
Rules Data  
R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue 
Check Digit 
56 56 1 A/N @ R 0041 
Link Across Dealer Code 57 57 1 A/N 0 = No 
1 = Yes 
R 0631 

---

## Page 69

Profile Security Database – Fixed Length Record Layouts 
Record Type 029 – Linkage Rules Data 69 
Record 1 of 4 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
ROA Calculation 
Methodology Code 
58 59 2 A/N 01 = [[shares]] X [[public offering]] Price 
(POP) 
02 = [[shares]] X Net [[Asset]] Value (NAV) 
03 = Gross Dollars Invested (Purchases 
Only) 
04 = Net Dollars Invested (Purchases 
less Redemptions) 
05 = Greater of [[shares]] X [[public offering]] 
Price or Gross Dollars Invested 
06 = Greater of [[shares]] X Net [[Asset]] 
Value or Gross Dollars Invested 
07 = Greater of [[shares]] X [[public offering]] 
Price or Net Dollars Invested 
08 = Greater of [[shares]] X Net [[Asset]] 
Value or Net Dollars Invested 
99 = ROA Does Not Apply 
R 0454 
Link by Spouse Code 60 60 1 A/N 0 = No 
1 = Yes 
R 0477 
Link by Civil Union Code 61 61 1 A/N 0 = No 
1 = Yes 
R 0478 
Link by Domestic 
Partnership Code 
62 62 1 A/N 0 = No 
1 = Yes 
R 0479 
Link by Common Law 
Marriage Code 
63 63 1 A/N 0 = No 
1 = Yes 
R 0480 
Link by Parent Code 64 64 1 A/N 0 = No 
1 = Yes 
R 0481 
Link by Step Parent 
Code 
65 65 1 A/N 0 = No 
1 = Yes 
R 0482 
Link by Legal Guardian 
Code 
66 66 1 A/N 0 = No 
1 = Yes 
R 0483 
Link by Child Code 67 67 1 A/N 0 = No 
1 = Yes 
R 0484 
Child Maturation Age 68 70 3 N 999 
Req’d if “Link by Child Code” = “1” 
OC 0485 
Link by Stepchild Code 71 71 1 A/N 0 = No 
1 = Yes 
R 0486 

---

## Page 70

Profile Security Database – Fixed Length Record Layouts 
Record Type 029 – Linkage Rules Data 70 
Record 1 of 4 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Link by Sibling Code 72 72 1 A/N 0 = No 
1 = Yes 
R 0487 
Link by Grandchildren 
Code 
73 73 1 A/N 0 = No 
1 = Yes 
R 0488 
Link by Grandparents 
Code 
74 74 1 A/N 0 = No 
1 = Yes 
R 0489 
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection 
Indicator 
76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple Errors 
R  
[[NSCC]] Reject Code  77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 71

Profile Security Database – Fixed Length Record Layouts 
Record Type 029 – Linkage Rules Data 71 
Record 2 of 4 (Required) 
Record Type 029 – Linkage Rules Data 
Record 2 of 4 
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
Share Class Name 7 26 20 A/N @ R 0526 
Link by Father-In-
Law Code 
27 27 1 A/N 0 = No 
1 = Yes 
R 0490 
Link by Mother-In-
Law Code 
28 28 1 A/N 0 = No 
1 = Yes 
R 0491 
Link by Brother-In-
Law Code 
29 29 1 A/N 0 = No 
1 = Yes 
R 0492 
Link by Sister-In-Law 
Code 
30 30 1 A/N 0 = No 
1 = Yes 
R 0493 
Link by Trust 
Beneficiary Code 
31 31 1 A/N 0 = No 
1 = Yes 
R 0503 
Link by Trust 
Grantor Code 
32 32 1 A/N 0 = No 
1 = Yes 
R 0504 
Link by Household 
Code  
33 33 1 A/N 0 = No 
1 = 9 Digit Zip Code 
2 = 9 Digit Zip Code, Last Name, and Tax 
Identification number (2 out of 3 ) 
R 0692 
Link by Custodian 
Code 
34 34 1 A/N 0 = No 
1 = Yes 
R 0693 
Filler 35 80 46 A/N  R  
 
 
  

---

## Page 72

Profile Security Database – Fixed Length Record Layouts 
Record Type 029 – Linkage Rules Data 72 
Record 3 of 4 (Required) 
Record Type 029 – Linkage Rules Data 
Record 3 of 4 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Filler 67 80 14 A/N  R  
 
 
  

---

## Page 73

Profile Security Database – Fixed Length Record Layouts 
Record Type 029 – Linkage Rules Data 73 
Record 4 of 4 (Optional) 
Record Type 029 – Linkage Rules Data 
Record 4 of 4 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 04 R 0080 
Filler 5 6 2 A/N Space R  
LOI Fulfillment Calculation 
Methodology Code 
7 8 2 A/N 01 = Gross Dollars Invested (Purchases 
Only) 
02 = Net Dollars Invested (Purchases 
less Redemptions) 
03 = [[shares]] X [[public offering]] Price 
04 = [[shares]] X Net [[Asset]] Value 
05 = Greater of [[shares]] X Net [[Asset]] 
Value or Gross Dollars Invested 
06 = Greater of [[shares]] X Public 
Offering Price or Gross Dollars Invested 
07 = Greater of [[shares]] X Net [[Asset]] 
Value or Net Dollars Invested 
08 = Greater of [[shares]] X Public 
Offering Price or Net Dollars Invested 
Req’d if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0459 
LOI Fulfillment Period 9 11 3 N 999 
Req’d if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0460 
LOI Alternate Fulfillment 
Period 
12 14 3 N 999 
Req’d if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0623 
LOI Minimum Amount 15 30 16 N 99999999999999.99 
Req’d if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0462 

---

## Page 74

Profile Security Database – Fixed Length Record Layouts 
Record Type 029 – Linkage Rules Data 74 
Record 4 of 4 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
LOI Minimum Initial 
Purchase Amount Type 
Code 
31 31 1 A/N 0 = Percentage 
1 = Dollar Amount 
Req’d if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0624 LOI Minimum Initial 
Purchase Amount 
32 47 16 N 99999999999999.99 
Req’d if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0625 
LOI Backdating Allowed 
Code 
48 48 1 A/N 0 = No 
1 = Yes 
Req’d if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0651 LOI Backdating Days 49 51 3 N 999 
Req’d if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
and 
LOI Backdating Allowed Code = “1” 
OC 0626 
Filler 52 80 29 A/N  R  

---

## Page 75

Profile Security Database – Fixed Length Record Layouts 
Record Type 030 – Master Tables Maintenance Record 75 
RECORD TYPE 030 – MASTER TABLES MAINTENANCE 
RECORD 
Record 1 of 4 (Required) 
For Fund Input Only – Used to change Share Class Name, Fund Portfolio Name, or Security Issue [[ID]]; or 
to Delete a Security Issue [[ID]] 
Record Type 030 – Master Tables Maintenance Record 
Record 1 of 4  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Reminder Indicator 6 6 1 A/N Output Only; Space on input 
‘R’ = Reminder on output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 030 = Master Tables Maintenance 
Record 
R 0083 
Action Type 13 13 1 A/N C = change 
(Class Name, Portfolio Name, 
Security [[ID]])  
D = Delete 
(Security [[ID]]) 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 45 46 2 A/N See ISO Country Codes 
Req.’d if Target Field = ‘S’  
R 0153 
Security Issue [[ID]] 47 55 9 A/N Req.’d if Target Field = ‘S’  R 0040 
ISIN Security Issue Check 
Digit 
56 56 1 A/N Req.’d if Target Field = ‘S’  R 0041 
Filler 57 57 1 A/N Space R 0153 

---

## Page 76

Profile Security Database – Fixed Length Record Layouts 
Record Type 030 – Master Tables Maintenance Record 76 
Record 1 of 4  
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Target Field 58 58 1 A/N C – Class Name 
P – Portfolio [[ID]] 
S – Security [[ID]] 
R 0670 
New Security Issue Country 
Code 
59 60 2 A/N See ISO Country Codes 
Req.’d if Target Field = ‘S’ and Action 
Type = ‘C’ 
OC 0671 
New Security Issue [[ID]] 61 69 9 A/N Req.’d if Target Field = ‘S’ and Action 
Type = ‘C’ 
OC 0672 
New ISIN Security Issue 
Check Digit 
70 70 1 A/N Req.’d if Target Field = ‘S’ and Action 
Type = ‘C’ 
OC 0673 
Filler 71 74 4 A/N Space R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 76 76 1 A/N Input: Space 
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

## Page 77

Profile Security Database – Fixed Length Record Layouts 
Record Type 030 – Master Tables Maintenance Record 77 
Record 2 of 4 (Required) 
Record Type 030 – Master Tables Maintenance Record 
Record 2 of 4 
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
Share Class Name 7 26 20 A/N Req.’d if Target Field = ‘C’  OC 0526 
New Share Class Name  27 46 20 A/N Req.’d if (Target Field = ‘C’ and Action 
Type = ‘C’)  
OC 0674 
Filler  47 80 34 A/N Space R  
 
 
  

---

## Page 78

Profile Security Database – Fixed Length Record Layouts 
Record Type 030 – Master Tables Maintenance Record 78 
Record 3 of 4 (Required) 
Record Type 030 – Master Tables Maintenance Record 
Record 3 of 4 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N Req.’d if Target Field = ‘P’ OC 0527 
Filler  67 80 14 A/N Space R  
 
 
  

---

## Page 79

Profile Security Database – Fixed Length Record Layouts 
Record Type 030 – Master Tables Maintenance Record 79 
Record 4 of 4 (Required) 
Record Type 030 – Master Tables Maintenance Record 
Record 4 of 4 
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
3 4 2 A/N 04 R 0080 
Filler 5 6 2 A/N Space R  
New Fund Portfolio 
Name 
7 66 60 A/N Req.’d if Target Field = ‘P’ and Action Type 
= ‘C’ 
OC 0527 
Filler  67 80 14 A/N Space R  

---

## Page 80

Profile Security Database – Fixed Length Record Layouts 
Record Type 031 – Fees and Expenses 80 
RECORD TYPE 031 – FEES AND EXPENSES 
Record 1 of 3 (Required) 
Input/Output 
Record Type 031 – Fees and Expenses 
Record 1 of 3 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Reminder Indicator 6 6 1 A/N Output Only; Space on input 
‘R’ = Reminder on output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 031 = Security Issue Fees and 
Expenses Data 
R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
56 56 1 A/N @ R 0041 
Fees and Expenses As Of 
Date 
57 64 8 N ccyymmdd R 0760 
Total Annual Operating 
Expenses 
65 69 5 N 99.999 
Req’d if “Waiver Fee Indicator = 0” 
OC 0761 

---

## Page 81

Profile Security Database – Fixed Length Record Layouts 
Record Type 031 – Fees and Expenses 81 
Record 1 of 3 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Fee Waiver Indicator 
(No/Yes)  
70 70 1 N 0=No 
1=Yes 
R 0762 
Filler 71 74 4 A/N  R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple 
Errors 
  
[[NSCC]] Reject Code  77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 82

Profile Security Database – Fixed Length Record Layouts 
Record Type 031 – Fees and Expenses 82 
Record 2 of 3 (Required) 
Record Type 031 – Fees and Expenses 
Record 2 of 3 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @ R 0526 
Net Annual Operating 
Expenses 
27 31 5 N 99.999 
Req’d if “Waiver Fee Indicator = 1” 
OC 0763 
Fee Waiver Rate 32 36 5 N 99.999 
Req’d if “Waiver Fee Indicator = 1” 
OC 0763 
Filler 37 80 44 A/N  R  
 
 
  

---

## Page 83

Profile Security Database – Fixed Length Record Layouts 
Record Type 031 – Fees and Expenses 83 
Record 3 of 3 (Required) 
Record Type 031 – Fees and Expenses 
Record 3 of 3 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Filler 67 80 14 A/N  R  

---

## Page 84

Profile Security Database – Fixed Length Record Layouts 
Record Type 032 – 408(b) (2) Specific 84 
RECORD TYPE 032 – 408(B) (2) SPECIFIC  
Record 1 of 4 (Required) 
Input/Output 
Record Type 032 – 408(b)(2) Specific Data 
Record 1 of 4 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Reminder Indicator 6 6 1 A/N Output Only; Space on input 
‘R’ = Reminder on output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 032 = 408(b)(2) Specific Data R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country 
Code 
45 46 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
56 56 1 A/N @ R 0041 
Portfolio Turnover Rate 57 62 6 N  R 0752 
Filler 63 74 12 A/N Space R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 

---

## Page 85

Profile Security Database – Fixed Length Record Layouts 
Record Type 032 – 408(b) (2) Specific 85 
Record 1 of 4 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[NSCC]] Rejection Indicator 76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple 
Errors 
  
[[NSCC]] Reject Code  77 80 4 A/N Input: Space 
Output: Reject code or space 
R  
 
  

---

## Page 86

Profile Security Database – Fixed Length Record Layouts 
Record Type 032 – 408(b) (2) Specific 86 
Record 2 of 4 (Required) 
Record Type 032 – 408(b)(2) Specific Data 
Record 2 of 4 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @ R 0526 
Minimum Initial Purchase 
Amount via Exchange 
27 42 16 N  R 0753 
Minimum Subsequent 
Purchase Amount via 
Exchange 
43 58 16 N  R 0754 
Filler 59 80 22 N Space R  
 
 
  

---

## Page 87

Profile Security Database – Fixed Length Record Layouts 
Record Type 032 – 408(b) (2) Specific 87 
Record 3 of 4 (Required) 
Record Type 032 – 408(b)(2) Specific Data 
Record 3 of 4 
Field Name  
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Filler 67 80 14 A/N Space R  
 
 
  

---

## Page 88

Profile Security Database – Fixed Length Record Layouts 
Record Type 032 – 408(b) (2) Specific 88 
Record 4 of 4 (Required) 
Record Type 032 – 408(b)(2) Specific Data 
Record 4 of 4  
Field Name 
Start End Len Type Description Opt/ Req Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 04 R 0080 
Filler 5 6 2 A/N Space   
Minimum Initial Purchase Amount 
Non-Qualified Plan  
7 22 16 N  R 0755 
Minimum Subsequent Purchase 
Amount Non-Qualified Plan  
23 38 16 N  R 0756 
Minimum Initial Purchase Amount 
(Omnibus Account) 
39 54 16 N  R 0757 
Minimum Subsequent Purchase 
Amount (Omnibus Account) 
55 70 16 N  R 0758 
Filler 71 80 10 A/N Space R  

---

## Page 89

Profile Security Database – Fixed Length Record Layouts 
Record Type 033 – Money Market Fund Data 89 
RECORD TYPE 033 – MONEY MARKET FUND DATA  
Record 1 of 3 
Record Type 033 – Money Market Fund Data - 
Record 1 of 3 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 01 R 0080 
Filler 5 5 1 A/N Space R  
Reminder Indicator 6 6 1 A/N Output Only; Space on input 
‘R’ = Reminder on output 
R  
Originator Type Indicator 7 7 1 A/N ‘F’ = Fund R 0081 
Profile Type 8 9 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 10 12 3 A/N 033 = Money Market Fund Data  R 0083 
Action Type 13 13 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
14 17 4 A/N @ R 0100 
Filler 18 28 11 A/N Space R  
Submission Date 29 36 8 A/N ccyymmdd R 0036 
 Profile Effective Date 37 44 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 45 46 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 47 55 9 A/N @ R 0040 
ISIN Security Issue Check Digit 56 56 1 A/N @ R 0041 
[[Liquidity]] Fee / Redemption Gate 
Eligibility Fund Indicator 
57 57 1 A/N 0 – No, Fund is not subject not 
Money Market [[Liquidity]] Fees/ 
Redemption Gates 
1 – Yes, Fund is subject to (may 
potentially impose) Money 
Market [[Liquidity]] 
Fee/Redemption Gate 
R 0792 

---

## Page 90

Profile Security Database – Fixed Length Record Layouts 
Record Type 033 – Money Market Fund Data 90 
Record 1 of 3 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Money Market Fund Indicator 
Note: 
Required when the Product Type 
Code = “02” (Money Market 
Mutual Fund) on the General 
Profile Record - Record Type 
020  
58 58 1 A/N 1 = Retail MM 
2 = Institutional MM 
3 = Government MM 
R 0790 
Number of NAV Strikes 
Field must be populated with at 
least ‘01’ when the Money 
Market Fund Indicator equal ‘2’ 
(Institutional Money Market) . 
Values of 02 through 10 should 
be populated when the number 
of NAV Strike Times are greater 
than ‘1’ 
 
Field must populated with “00’ 
when the Money Market Fund 
Indicator = ‘1’(Retail Money 
Market) or ‘3’ (Government 
Money Market)  
59 60 2 N  R 0794 
NAV Strike Time 1 
Field is required when the Money 
Market Fund Indicator = ‘2’ 
(Institutional Money Market) 
 
Field should be ‘Blank” when the 
Money Market Fund Indicator = 
“1” (Retail Money Market) or “3” 
(Government Money Market) 
61 66 6 A/N Hhmmss O/C 0791 
Filler 67 74 8 A/N space R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test  
R 0089 
[[NSCC]] Reject Indicator 76 76 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]] 
Multiple Errors 
  
[[NSCC]] Reject Code  77 80 4 A/N Input: Space 
Output: Reject Code or space 
  
 

---

## Page 91

Profile Security Database – Fixed Length Record Layouts 
Record Type 033 – Money Market Fund Data 91 
Record 2 of 3 
Record Type 033 – Money Market Fund Data - 
Record 2 of 3 
Field Name  
Start End Len Type Description Opt/ 
Req 
Req 
Reject 
Code 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 02 R 0080 
Filler 5 6 2 A/N Space R  
Share Class Name 7 26 20 A/N @  R 0526 
NAV Strike Time 2 27 32 6 A/N hhmmss OC 0791 
NAV Strike Time 3 33 38 6 A/N hhmmss OC 0791 
NAV Strike Time 4 39 44 6 A/N hhmmss OC 0791 
NAV Strike Time 5 45 50 6 A/N hhmmss OC 0791 
NAV Strike Time 6 51 56 6 A/N hhmmss OC 0791 
NAV Strike Time 7 57 62 6 A/N hhmmss OC 0791 
NAV Strike Time 8 63 68 6 A/N hhmmss OC 0791 
NAV Strike Time 9 69 74 6 A/N hhmmss OC 0791 
NAV Strike Time 10 75 80 6 A/N hhmmss OC 0791 
 
 
  

---

## Page 92

Profile Security Database – Fixed Length Record Layouts 
Record Type 033 – Money Market Fund Data 92 
Record 3 of 3 
Record Type 033 – Money Market Fund Data - 
Record 3 of 3  
Field Name 
Start End Len Type Description Opt/ 
Req 
Req 
Reject 
Code 
Code 
Physical Sequence Number 1 2 2 A/N  R 0080 
Logical Sequence Number 3 4 2 A/N 03 R 0080 
Filler 5 6 2 A/N Space R  
Fund Portfolio Name 7 66 60 A/N @ R 0527 
Filler 67 80 14 A/N  R  

---

## Page 93

Profile Security Database – Fixed Length Record Layouts 
Appendix A: Valid Values for Investment Class Code 93 
APPENDIX A: VALID VALUES FOR INVESTMENT CLASS 
CODE 
01 = Aggressive Growth Fund 
02 = Growth Fund 
03 = Sector Fund 
04 = Emerging Market Fund 
05 = Global [[Equity]] Fund 
06 = International [[Equity]] Fund 
07 = Regional [[Equity]] Fund 
08 = Growth and Income Fund 
09 = [[Equity]] Income Fund 
10 = [[Asset]] Allocation Fund 
11 = Balanced Fund 
12 = Flexible Portfolio Fund 
13 = Income-Mixed Fund 
14 = Corporate Bond Fund 
15 = Intermediate- Term Corporate Bond Fund 
16 = Short-Term Corporate Bond Fund 
17 = High Yield Bond Fund 
18 = Global Bond Fund 
19 = Short-Term Global Bond Fund 
20 = World Bond Fund 
21 = Government General Bond Fund 
22 = Intermediate-Term Government Bond Fund 
23 = Short-Term Government Bond Fund 
24 = Mortgage-Backed Fund 
25 = Strategic Income Bond Fund 
26 = State Municipal Bond Fund 

---

## Page 94

Profile Security Database – Fixed Length Record Layouts 
Appendix A: Valid Values for Investment Class Code 94 
27 = Short-Term State Municipal Bond Fund 
28 = National Municipal General Bond Fund 
29 = National Municipal Short-Term Bond Fund 
30 = Taxable Government Money Market Fund 
31 = Taxable Non-Government Money Market Fund 
32 = Tax-Exempt National Money Market Fund 
33 = Tax-Exempt State Money Market Fund 
 

---

## Page 95

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 95 
APPENDIX B: VALID VALUES FOR SOCIAL CODE 
[[DTCC]] does not advise on tax reporting requirements. Use of any information herein or any other web 
site referred to herein is for general information only and does not represent tax advice either express 
or implied. 
Social Codes 
Firms may use the following Social Codes to categorize the type of accounting methods that they want to 
establish.  
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
01 Individual Use for non-[[Fiduciary]] accounts registered to an individual.  
 
Best Practice: Fund is responsible for tax reporting unless level 3 
or trust networked. 
N/A Female  This social code was eliminated Nov. 18, 2013. See Important 
Notice a7665 (posted July 3, 2013). 
 
Best Practice: Map to Social Code 01 
03 Joint Tenants  Use for accounts registered to multiple individuals, including 
Tenants in Common, Tenants by Entirety, Community Property.  
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
04 C Corporations  Use for accounts registered to C Corporations, including 
incorporated entities and LLC’s that elect to be treated as a 
corporation. Excludes Partnerships (social code 52) and S 
Corporations (social code 63).  
 
Best Practice: Firm is responsible for tax reporting. 
05 Insurance [[Companies]]  Use for Insurance Company product accounts that are fund level 
omnibus.  
 
Best Practice: Firm is responsible for tax reporting.  
06 [[Broker]]/Dealer Omnibus Use for [[Broker]]/Dealer house accounts that are fund level 
omnibus.  
 
Best Practice: Firm is responsible for tax reporting. 
07 Bank/Trust Omnibus Use for Bank and Trust accounts that are fund level omnibus.  
 
Best Practice: Firm is responsible for tax reporting. 
08 Individual Retirement Account 
(fund-prototype) 
Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 

---

## Page 96

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 96 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
09 Individual Retirement Account - Rollover 
(fund-prototype) 
Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 
N/A KEOGH  This social code was eliminated Nov. 18, 2013. See Important 
Notice a7665 (posted July 3, 2013). 
 
Best Practice: Map to either social code 34 or 50. 
11 Profit Sharing Plan (non-prototype)  Use for non-prototype profit sharing plans which are maintained in 
a plan level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting.  
12 401(k) Plan (non-prototype) Use for non-prototype 401(k) accounts maintained in plan level 
omnibus accounts.  
 
Best Practice: Firm is responsible for tax reporting. 
13 Money Purchase Pension Plan 
(non-prototype) 
Use for non-prototype pension plans which are maintained in a 
plan level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting. 
14 UGMA/UTMA Use for Uniform Gifts to Minors Act and Uniform Transfer to Minor 
Act Accounts.  
 
Best Practice: Fund is responsible for tax reporting unless level 3 
or trust networked. 
15 Trust - Retail  Use for trusts where an individual is registered as trustee for the 
Trust and the TIN belongs to the trustee.  
 
Best Practice: Fund is responsible for tax reporting unless level 3 
or trust networked. 
16 Individual [[Fiduciary]]  Use for non-retirement [[Fiduciary]] accounts (i.e., guardian, 
conservator, escrow, agent, etc.). 
 
Best Practice: Fund is responsible for tax reporting unless level 3 
or trust networked.  
17 Individual Retirement Account (non-
prototype) 
Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
18 [[Broker]]/Dealer FBO  Use for accounts registered in the firm’s name under their TIN.  
 
Best Practice: Firm is responsible for tax reporting. 

---

## Page 97

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 97 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
19 403(b) Plan (non-prototype) Use for non-prototype 403(b) accounts maintained at the plan 
level omnibus level.  
 
Best Practice: Firm is responsible for tax reporting. 
20 457(b) Plan (non-prototype) Use for non-prototype 457(b) plans which are maintained in a plan 
level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting. 
21 Non-Profit Organization Use for Non-Profit Organization accounts.  
 
Best Practice: Fund is responsible for tax reporting unless level 3 
or trust networked.  
22 Roth IRA (fund-prototype) Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 
23 Roth IRA (non-prototype) Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
24 Roth Conversion IRA (fund-prototype) Use for accounts registered under the fund’s custodial IRA plan. 
 
Best Practice: Fund is responsible for tax reporting. 
25 Roth Conversion IRA (non-prototype) Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
26 Education IRA (fund-prototype) Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 
27 Education IRA (non-prototype) Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
28 Individual Retirement Account - Rollover 
(non-prototype) 
Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
29 Individual Retirement Account - Spousal 
(fund-prototype) 
Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 

---

## Page 98

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 98 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
30 Individual Retirement Account - Spousal 
(non-prototype) 
Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
31 Simple IRA (fund-prototype) Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 
32 Simple IRA (non-prototype) Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
33 Simplified Employee Pension (SEP-IRA) 
(fund-prototype) 
Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 
34 Simplified Employee Pension (SEP-IRA) 
(non-prototype) 
Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
35 SARSEP (fund-prototype) Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 
36 SARSEP (non-prototype) Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
37 Section 529 Plan - Qualified State Tuition 
Program 
Use for Section 529 Plan accounts - Qualified State Tuition 
Program. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
38 UGMA/UTMA transferred into Section 
529 Plan  
Use for UGMA/UTMA accounts transferred into Section 529 Plan 
accounts. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
39 Section 529 Plan transferred into new 
Section 529 Plan  
Use for Section 529 Plan accounts transferred into new Section 
529 Plan accounts which are maintained at the [[participant]] FBO 
account level. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
40 IRA transferred into Section 529 Plan  Use for IRA's transferred into Section 529 Plan accounts which 
are maintained at the [[participant]] FBO account level. 
 

---

## Page 99

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 99 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
Best Practice: Fund is responsible for tax reporting unless level 3. 
41 Series E/Series I U.S. Saving [[Bonds]] 
transferred into Section 529 Plan  
Use for Series E/Series I U.S. Saving [[Bonds]] transferred into 
Section 529 Plan accounts which are maintained at the [[participant]] 
FBO account level. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
42 Bank/Trust FBO  Use when a Bank or Trust Company acts as custodian or trustee 
for an underlying shareholder (non-retirement). Accounts are 
registered in the firm's name under their TIN  
 
Best Practice: Firm is responsible for tax reporting. 
43 Profit Sharing Plan FBO [[participant]] 
Name/Account # (fund-prototype) 
Use for fund-prototype profit sharing plans which are maintained 
at the [[participant]] FBO account level.  
 
Best Practice: Fund is responsible for tax reporting.  
44 401(k) Plan FBO [[participant]] 
Name/Account # (fund-prototype) 
Use for fund-prototype 401(k) plans which are maintained at the 
[[participant]] FBO account level.  
 
Best Practice: Fund is responsible for tax reporting. 
45 Money Purchase Pension Plan FBO 
[[participant]] Name/Account #  
(fund-prototype) 
Use for fund-prototype money purchase pension plans which are 
maintained at the [[participant]] FBO account level.  
 
Best Practice: Fund is responsible for tax reporting. 
46 403(b) Plan FBO [[participant]] 
Name/Account # (fund-prototype) 
Use for fund-prototype 403(b) accounts maintained in [[participant]] 
FBO level accounts.  
 
Best Practice: Fund is responsible for tax reporting. 
47 Health Savings Account FBO [[participant]] 
Name/Account # (fund-prototype) 
Use for fund-prototype Health Savings Accounts which are 
maintained in a [[participant]] FBO level account.  
 
Best Practice: Fund is responsible for tax reporting. 
48 Health Savings Account (non-prototype) Use for non-prototype Health Savings Accounts which are 
maintained in a plan level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting. 
49 Single K (fund-prototype) Use for fund-prototype Single K plan accounts (i.e., a defined 
contribution retirement plan with one [[participant]]). 
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
50 Single K (non-prototype) Use for non-prototype Single K plan accounts (i.e., a defined 
contribution retirement plan with one [[participant]]). 
 

---

## Page 100

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 100 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
Best Practice: Firm is responsible for tax reporting. 
51 Non-Qualified Deferred Compensation 
Plan (non-prototype; [[participant]] directed) 
Use for non-prototype, non-qualified deferred compensation plans 
which are maintained in a plan level omnibus account. 
Participants direct investments in these accounts.  
 
Best Practice: Firm is responsible for tax reporting. 
52 Partnerships Use for accounts registered to Partnerships, including LLC’s that 
elect to be treated as partnerships.  
 
Best Practice: Fund is responsible for tax reporting. 
53 Defined Benefit Plan (non-prototype) Use for non-prototype, defined benefit plan accounts which are 
maintained in a plan level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting. 
54 Sole Proprietorships Use for business accounts registered in an individual’s name.  
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
55 Governmental Entities Use for accounts registered under state or federal entities, as well 
as subdivisions thereof.  
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
56 Real Estate Investment Trusts Use for REIT accounts.  
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
57 Roth 401(k) Plan FBO [[participant]] 
Name/Account # (fund-prototype) 
Use for fund-prototype Roth 401(k) accounts which are 
maintained at the [[participant]] FBO account level (fund-prototype). 
 
Best Practice: Fund is responsible for tax reporting. 
58 Roth 401(k) Plan (non-prototype) Use for non-prototype, Roth 401(k) accounts which are 
maintained at a plan omnibus level.  
 
Best Practice: Firm is responsible for tax reporting. 
59 Roth 403(b) Plan FBO [[participant]] 
Name/Account # (fund-prototype) 
Use for fund-prototype Roth 403(b) accounts which are 
maintained at the [[participant]] FBO account level.  
 
Best Practice: Fund is responsible for tax reporting. 
60 Roth 403(b) Plan (non-prototype) Use for non-prototype, Roth 403(b) accounts which are 
maintained at the plan omnibus level. 
 
Best Practice: Firm is responsible for tax reporting. 

---

## Page 101

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 101 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
61 Section 529 Plan - Joint Owner  Use for Section 529 education savings plan registered to joint 
owners. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
62 Section 529 Plan - Trust Use for Section 529 education savings plan registered to a trust. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
63 S Corporation  Use for accounts registered to S Corporations, including 
incorporated entities and LLC's that elect to be treated as a 
corporation. Excludes Partnerships (social code 52) and C 
Corporations (social code 04). 
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
64 Retirement Plan Super Omnibus  
(non-prototype) 
Use for non-prototype accounts representing only multiple 
retirement plans. 
 
Best Practice: Firm is responsible for tax reporting. 
65 Transfer On Death – Individual 
 
Use for a transfer on death account established for an individual 
account registration.  
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
66 Transfer On Death - Joint Tenant with 
Rights of Survivorship or Tenants by 
Entirety 
Use for a transfer on death account established for a multiple 
owner registration. 
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
67 Section 529 Plan - Entity  Use to distinguish an "Entity" owning a 529 Plan from other 
owners. An Entity would be defined as University, Foundation, 
Scholarship Fund, etc. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
68 Section 529 Plan – Corporate 
 
Use for accounts with a Corporation owning a 529 Plan. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
69 457(b) Plans - FBO [[participant]] 
Name/Account # (fund-prototype) 
 
Use for fund-prototype 457(b) plans which are maintained in a 
[[participant]] FBO account. 
 
Best Practice: Fund is responsible for tax reporting. 
70 457(f) Plans (non-prototype) Use for non-prototype 457(f) plans which are maintained in a plan 
level omnibus account.  
 

---

## Page 102

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 102 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
Best Practice: Firm is responsible for tax reporting. 
71 Non-Qualified Deferred Compensation 
Plan (non-prototype; not [[participant]] 
directed) 
 
Use for non-prototype, non-qualified deferred compensation plans 
which are maintained in a plan level omnibus account. 
Participants [[DO]] not direct investments in these accounts. 
 
Best Practice: Firm is responsible for tax reporting. 
72 Non-Qualified 403(b) Plans 
(non-prototype 
Use for non-prototype, non-qualified plans which are maintained in 
a plan level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting. 
73 403(b) Plan FBO [[participant]] 
Name/Account (non-prototype) 
Use for non-prototype 403(b) accounts maintained at the 
[[participant]] FBO level.  
 
Best Practice: Firm is responsible for tax reporting. 
74 Fund of Funds - '40 Act Registered Use for an account that is a Fund of Funds that is '40 Act 
registered. 
 
Best Practice: Firm is responsible for tax reporting. 
75 Fund of Funds - Non-'40 Act Registered Use for unitized or non-'40 act registered Fund of Fund accounts. 
 
Best Practice: Firm is responsible for tax reporting. 
76 IRA Beneficiary Distribution Account 
(fund-prototype) 
Use for beneficiaries or successor beneficiaries of Traditional, 
Rollover, SEP, SAR-SEP or SIMPLE IRA's. 
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
77 Roth IRA Beneficiary Distribution 
Account (fund-prototype) 
Used for beneficiaries or successor beneficiaries of Roth IRAs. 
 
Best Practice: Fund is responsible for tax reporting. 
78 401(k) Plan FBO [[participant]] 
Name/Account # (non-prototype) 
Use for non-prototype 401(k) accounts maintained at the 
[[participant]] FBO level.  
 
Best Practice: Firm is responsible for tax reporting. 
79 Profit Sharing Plan FBO [[participant]] 
Name/Account # (non-prototype) 
Use for non-prototype Profit Sharing plan accounts maintained at 
the [[participant]] FBO level.  
 
Best Practice: Firm is responsible for tax reporting. 
80 Money Purchase Pension Plan FBO 
[[participant]] Name/Account # 
(non-prototype) 
Use for non-prototype Money Purchase Pension Plan accounts 
maintained at the [[participant]] FBO level.  
 
Best Practice: Firm is responsible for tax reporting. 

---

## Page 103

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 103 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
81 Health Savings Account FBO [[participant]] 
Name/Account # 
(non-prototype) 
Use for non-prototype Health Saving Accounts (HSA's) maintained 
at the [[participant]] FBO level.  
 
Best Practice: Firm is responsible for tax reporting. 
82 Government Sponsored Plan (non-
prototype) 
Use for non-prototype Government-sponsored plan accounts 
(described in Internal Revenue Service Code 414(d)) and 
maintained in a plan level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting. 
83 Insurance Company Group Trust or 
Pooled Separate Account Limited to 
retirement plan assets. 
Use for Insurance Company accounts established to hold assets 
of the group trust or pooled separate accounts. Excludes 
insurance [[Companies]] (social code 05). 
 
Best Practice: Firm is responsible for tax reporting.  
84 Investment Clubs; Unions; 
Unincorporated Association; 
Miscellaneous Organizations 
Use for accounts registered to unincorporated associations (i.e., 
groups that have organized themselves under a specific name, 
but have not adopted any business form such as a corporation or 
partnership. 
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
85 Estate Account Use for accounts registered to executors or personal 
representatives of an estate.  
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
86 Fund of Funds - '40 Act Registered - 
Retirement Assets Only 
 
(Effective date 07/28/2014) 
Use for '40 Act registered Fund of Fund accounts that are limited 
to retirement assets. 
 
Best Practice: Firm is responsible for tax reporting. 
87 Fund of Funds – Non-’40 Act Registered 
– Retirement Assets Only 
Use for unitized or non-'40 act registered Fund of Fund accounts 
that are limited to retirement assets. 
 
Best Practice: Firm is responsible for tax reporting. 
88 Coverdell ESA Beneficiary Distribution 
Account (fund-prototype) 
Use for beneficiaries or successor beneficiaries of Coverdell 
Education Savings Accounts. 
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
89 Individual Retirement Accounts - Super 
Omnibus (non-prototype) 
Use for non-prototype accounts representing only IRA assets for 
multiple IRA shareowners. 
 
Best Practice: Firm is responsible for tax reporting. 

---

## Page 104

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 104 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
90 Simple 401(k) Plan (non-prototype) Use for non-prototype Simple 401(k) plans which are maintained 
in a plan level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting.  
91 Simple 401(k) Plan FBO [[participant]] 
Name/Account # (non-prototype) 
Use for non-prototype Simple 401(k) plans which are maintained 
at the [[participant]] FBO account level.  
 
Best Practice: Firm is responsible for tax reporting.  
92 Simple 401(k) Plan FBO [[participant]] 
Name/Account # (fund-prototype) 
Use for fund-prototype Simple 401(k) plans which are maintained 
at the [[participant]] FBO account level.  
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked.  
93 Single Defined Benefit Plan 
(non-prototype) 
Use for non-prototype Single Defined Benefit plan account (i.e., a 
defined benefit retirement plan with one [[participant]]). 
 
Best Practice: Firm is responsible for tax reporting.  
94 Non-U.S. Governmental Entities Use for accounts registered under non-U.S., foreign governments 
as well as subdivisions thereof.  
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
95 Trust – Institutional Use when a Bank or Trust Company acts as custodian or trustee 
for an underlying shareholder or entity (non-retirement). Accounts 
are registered in the firm's name under their TIN 
 
Best Practice: Firm is responsible for tax reporting. 
96 457(b) Plans FBO [[participant]] 
Name/Account # (non-prototype) 
Use for non-prototype 457(b) plans which are maintained in a 
[[participant]] FBO account. 
 
Best Practice: Firm is responsible for tax reporting. 
97 Single K Plans FBO [[participant]] 
Name/Account # (non-prototype) 
Use for non-prototype Single K Plan Accounts (i.e., a defined 
contribution retirement plan with one [[participant]]) which are 
maintained in a [[participant]] FBO account. 
 
Best Practice: Firm is responsible for tax reporting. 
98 Roth 401(k) Plans FBO [[participant]] 
Name/Account # (non-prototype) 
Use for non-prototype Roth 401(k) accounts which are maintained 
at the [[participant]] FBO account level (non-prototype). 
 
Best Practice: Firm is responsible for tax reporting. 
99 Other  Social Code 99 will not be retired at this time. 
 
See Important Notice A# 8031 posted 5/15/2015. 

---

## Page 105

Profile Security Database – Fixed Length Record Layouts 
Appendix B: Valid Values for Social Code 105 
Social 
Code 
[[NSCC]] Social Code Description  Definition and Best Practice 
A0 Roth 403(b) Plans FBO [[participant]] 
Name/Account # (non-prototype) 
Use for non-prototype Roth 403(b) accounts which are maintained 
at the [[participant]] FBO account level. 
 
Best Practice: Firm is responsible for tax reporting. 
A1 457(f) Plans FBO [[participant]] 
Name/Account # (non-prototype) 
Use for non-prototype 457(f) plans which are maintained in a 
[[participant]] FBO account. 
 
Best Practice: Firm is responsible for tax reporting. 
A2 
 
Single K Plans FBO [[participant]] 
Name/Account # (fund-prototype) 
Use for fund-prototype Single K Plan Accounts (i.e., a defined 
contribution retirement plan with one [[participant]]) which are 
maintained in a [[participant]] FBO account. 
 
Best Practice: Fund is responsible for tax reporting. 
A3 401(k) Plan (fund-prototype) Use for fund-prototype 401(k) accounts maintained in plan level 
omnibus accounts. 
 
Best Practice: Record-keeper is responsible for tax reporting. 
A4 Section 529 ABLE Use for Section 529 ABLE Plan accounts 
 
Best Practice: Fund is responsible for tax reporting unless level 3 
or omnibus. 
A5 SIMPLE Group Trust IRA (fund-
prototype) 
(Effective 8/26/2019) 
Use for accounts registered under the fund’s custodial group trust 
plan. 
 
Best Practice: Fund is responsible for tax reporting. 

---

## Page 106

Profile Security Database – Fixed Length Record Layouts 
Appendix C: Modifications to Social Code field edits 106 
APPENDIX C: MODIFICATIONS TO SOCIAL CODE FIELD 
EDITS 
Effective December 4, 2008 
Background 
The 5 conditional social code fields requiring clarification are: 
• Relationship between [[participant]] Minimum and [[Asset]] Size" field 
• "Number of Eligible Participants Minimum" field 
• "Number of Active Participants Minimum" field 
• "Minimum [[Asset]] Size for Eligibility" field 
• "Maximum [[Asset]] size for Eligibility" field 
 
These fields are assigned to the Share Class Level in the hierarchal database and can be found in the Social 
Code tab on screen. 
The “Eligibility Code” field is used to indicate whether the Social Code is eligible to purchase the fund, or 
eligible to purchase the fund only if it meets certain requirements, or eligible to purchase the fund at NAV if it 
meets certain minimum [[participant]] and/or [[Asset]] size requirements. 
The allowable values for the "Eligibility Code" field are: 
• 0 = Eligible , No Restrictions 
• 1 = Eligible, Restrictions May Apply; and 
• 2 = Eligible at NAV, Restrictions May Apply 
 
If the Eligibility Code is 1 = Eligible Restrictions May Apply or 2 = Eligible at NAV, Restrictions May Apply, then 
the above mentioned Social Code fields become conditionally optional for input. 
As noted in the Dictionary Supplement, for funds with no restrictions on the type of account that may purchase, 
all social codes should be populated. For funds with restrictions, i.e., a class of [[shares]] available only to 
retirement plans, only social codes eligible to purchase should be populated. 
The Social Code fields were also intended to capture an NAV eligibility policy, such as Retirement Plans with 
$1M in assets OR 100 eligible participants, may purchase at NAV. 
The "Relationship Between [[participant]] Minimum and [[Asset]] Size" field is asking whether the fund allows Plans 
with 100 eligible employees or $1 million in assets to buy A [[shares]] at NAV. 
For example, if the Eligible / Active [[participant]] Minimums and the [[Asset]] Size for eligibility must be met before 
investment is permitted, the value "0 = Both Must Be Met" would be selected. Alternatively, if either the 
[[participant]] Minimums or [[Asset]] Size for Eligibility can be met to permit investment, the value of "1 = Either Must  
Be Met" would be selected. 
Effective December 4, 2008, the following edit criteria will apply. 
i. If the "Eligibility Code" field = "0 = Eligible, No Restrictions, or "1 = Eligible, Restrictions May Apply", then 
the "Relationship between [[participant]] Minimum and [[Asset]] Size" field must be left blank/ not allowed.  If not 
blank, a reject message will appear on screen advising Number of Active Participants Minimum must be 
blank when Eligibility Code is equal to 0 or 1. 

---

## Page 107

Profile Security Database – Fixed Length Record Layouts 
Appendix C: Modifications to Social Code field edits 107 
If the "Eligibility Code" field = " 2 = Eligible at NAV, Restrictions May Apply", then the "Relationship 
between [[participant]] Minimum and [[Asset]] Size" field is Required. 
 
ii. If the "Relationship between [[participant]] Minimum and [[Asset]] Size" field has one of the following values of " 
0", "1", or " space/blank", then the edit criteria is as follows: 
 
a. "0= Both must be met" then: 
• "Minimum [[Asset]] Size for Eligibility" field is Required 
• At least one of "Number of Eligible Participants Minimum" and "Number of Active Participants 
Minimum" must be populated; and more than one of these two fields will also be 
accepted/allowed 
b. "1 -Either must be met" then: 
• At least one of the fields "Number of Eligible Participants Minimum", "Number of Active 
Participants Minimum", "Minimum [[Asset]] Size for Eligibility" must be populated; and more than 
one of these three fields is also accepted/ allowed. 
c. "Blank /space" 
• All of the fields "Number of Eligible Participants Minimum", "Number of Active Participants 
Minimum", "Minimum [[Asset]] Size for Eligibility" fields must be blank/ not allowed.  If not blank, a 
reject message will appear on screen. 
 
iii. Modified Edits for the following fields: 
a. There will be no edit comparison (greater than/less than) between "Number of Eligible Participants 
Minimum" and "Number of Active Participants Minimum". 
b. There will also be no edit comparison between "Minimum [[Asset]] Size for Eligibility" and "Maximum 
[[Asset]] Size for Eligibility" because the minimum and maximum [[Asset]] sizes are independent fields.  
c. The "Maximum [[Asset]] Size for Eligibility" field is now always a Required numeric field.  If it is not 
applicable, then funds should follow the best practice for input to this field:  
Best Practice: If the maximum [[Asset]] size for eligibility does not apply, a fund would input all 9s in this 
field. 
 

---

## Page 108

Profile Security Database – Fixed Length Record Layouts 
APPENDIX D: SUMMARY OF CHANGES 108 
APPENDIX D: SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 
 

---

## Page 109

Profile Security Database – Fixed Length Record Layouts 
Summary of Changes – Effective date March 28, 2022 109 
SUMMARY OF CHANGES – EFFECTIVE DATE MARCH 
28, 2022 
New Product Type Code – Interval Fund (48) 
Field Name  Location Description Values Updated (Red) 
Product Type Code Record 020 Position 7-8 01 = Mutual Fund 
02 = Money Market Mutual Fund 
03 = [[UIT]] (Unit Investment Trust) 
04 = Closed-End Mutual Fund 
05 = GIC (Guaranteed Investment 
Contract) 
06 = Stable Value Fund 
07 = Separate Account 
08 = Bank Collective Trust 
09 = Offshore (NRA) Fund 
10 = BIC (Bank Investment Contract) 
11 = Section 529 College Savings Plan 
12 = Offshore U.S. Dollar Enhanced 
([[DO]] not use- domestic funds on Profile 
Security only) 
13 = Offshore Non-U.S. Dollar 
Enhanced ([[DO]] not use – domestic 
funds on Profile Security only) 
14 = Annuity (with underlying mutual 
funds) 
15 = Section 529 Money Market Fund 
48 = Interval Fund 
 
Best Practice: When Product Type 
Code = 02 (Money Market Mutual 
Fund) or 15 (Section 529 Money 
Market Fund), Record Type 033 - 
‘Money Market Fund Data’ should also 
be submitted. 

---

## Page 110

Profile Security Database – Fixed Length Record Layouts 
Summary of Changes – Effective date August 26, 2019 110 
SUMMARY OF CHANGES – EFFECTIVE DATE AUGUST 
26, 2019 
Social Code 
The following new Social Code will be added: 
Social 
Code  
[[NSCC]] Social Code Description Definition and Best Practice 
A5 SIMPLE Group Trust IRA (fund-
prototype) 
(Effective 8/26/2019) 
Use for accounts registered under the fund’s custodial group 
trust plan. 
Best Practice: Fund is responsible for tax reporting. 

---

## Page 111

Profile Security Database – Fixed Length Record Layouts 
Summary of Changes – Effective date March 25, 2019 111 
SUMMARY OF CHANGES – EFFECTIVE DATE MARCH 
25, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code  Description 
0388 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 112

Profile Security Database – Fixed Length Record Layouts 
Summary of changes – Effective date July 13, 2018 112 
SUMMARY OF CHANGES – EFFECTIVE DATE JULY 13, 
2018 
 
Field Name  Location Description Values Updated (Red) 
[[Dividend]] Accrual 
Redemption T+1 Stop Date 
Code 
Record 020 Sequence 3 Position 68 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
[[Dividend]] Accrual Partial 
Exchange Out Stop Date 
Code  
Record 020 Sequence 3 Position 69 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date - 1  
[[Dividend]] Accrual Partial 
Transfer Out Stop Date Code 
Record 020 Sequence 3 Position 71 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date – 1 
[[Dividend]] Accrual ACAT 
Transfer Out Stop Date  
Record 020 Sequence 3 Position 73 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date – 1 
DCC&S [[Dividend]] Accrual 
Redemption Stop Date Code 
Record 020 Sequence 3 Position 77 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date – 1 
DCC&S [[Dividend]] Accrual 
Redemption “G” indicator 
(Share Class Conversion) 
Stop Date Code 
Record 020 Sequence 3 Position 78 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date – 1 
DCC&S [[Dividend]] Accrual 
Redemption “L” indicator 
(Omnibus [[Dividend]] 
Reconciliation) Stop Date 
Code 
Record 020 Sequence 3 Position 79 0 = [[settlement]] Date -1 
1 = [[settlement]] Date 
2 = Trade Date 
3 = Trade Date – 1 

---

## Page 113

Profile Security Database – Fixed Length Record Layouts 
Summary of changes – Effective date July 9, 2018 113 
SUMMARY OF CHANGES – EFFECTIVE DATE JULY 9, 
2018 
New Field Name  Location Description 
Eligible for Externalized Commission Record 020 Sequence 4 Position 75 A new required field to indicate share 
classes eligible for Externalized 
Commission. 
Large Trade Notification 
AND 
Large Trade Dollar Threshold Amount 
Record 020 Sequence 4 Position 76 
 
Record 020 Sequence 7 Position 41-56 
New required fields to indicate if a Firm 
should notify the Fund when a large 
trade dollar amount threshold is met for 
a security. 
DCC&S Eligible 
AND 
Defined Contribution Clearance and 
[[settlement]] (DCC&S) Cut –off Cycle 
Record 020 Sequence 1 Position 68 
 
Record 020 Sequence 1 Position 69-72 
New required fields to provide the 
[[NSCC]] Cycle cut-off cycle for DCC&S 
trades, rather than the time of day 
currently provided in the ‘DCC&S Cut-
Off Time’ field. 
In conjunction with the addition of these 
two fields, the ‘DCC&S Cut-Off Time” 
was removed and replaced by filler 
space. This will provide clarity 
regarding the cut-off time for DCC&S 
trades by providing the [[NSCC]] Cycle, 
rather than the time of day. 
[[Dividend]] and DCC&S Accrual 
Start/Stop fields 
Record 020 Sequence 3 Position 67-79 New optional/conditional fields to 
provide additional accrual methodology 
details (start/stop dates) for a security. 
Existing Fields Modified 
Existing Field Name  Location Description 
CDSC Rules Apply Record 020 Sequence 5 Position 69 New data point value for this existing field to 
indicate when CDSC applies for Finder’s 
Fee/Jumbo Purchase Only. This will eliminate 
confusion as to how to populate and interpret 
CDSC and commission data where advanced 
commission and CDSC rules only apply in 
certain situations (i.e., for $1 million + Jumbo 
purchases).  
ROA Aggregation Inclusion Record 020 Sequence 7 Position 80 This existing field was renamed to “ROA/LOI 
Aggregation Inclusion”. Updates to existing 
values and the addition of new values were 
added to differentiate between ROA 
aggregation rules vs. LOI aggregation rules. 
[[Dividend]] and DCC&S Accrual 
Start/Stop fields 
Record 020 Sequence 5 Position 73-
77 
Record 020 Sequence 7 Position 16-
17 
Rename existing fields to provide additional 
accrual methodology details (start/stop dates) 
for a security. 

---

## Page 114

Profile Security Database – Fixed Length Record Layouts 
Summary of changes – Effective date July 9, 2018 114 
Existing Field Name  Location Description 
Exchange Buy Eligibility Record 020 Sequence 6 Position 30 New data point value to identify when 
restrictions apply to exchange buy purchases. 
Only Purchases Eligibility had this [[Option]]. By 
adding this value to Exchange Buy Eligibility, 
these two data points will have the same 
value options. 
Social Codes  Addition of new Social Codes. The new social 
codes necessitate leveraging alpha/numeric 
values. [[NSCC]] record layouts currently 
support alpha/numeric values for the Social 
Code field; clients should review their systems 
to ensure they are able to support 
alpha/numeric social code values. 

---

## Page 115

Profile Security Database – Fixed Length Record Layouts 
Summary of changes – Effective date August 22, 2016 115 
SUMMARY OF CHANGES – EFFECTIVE DATE AUGUST 
22, 2016 
Existing Fields Modified 
Modified Field Name  Location Description 
Product Type Code Record Type 020 (General Profile), 6 of 
10 
Bytes 7-8 
Additional Product Type added: 
 
15 = Section 529 Money Market Funds 
For new Security Issue [[ID]] Adds, when 
Product Type Code = 02 Money Market 
Mutual Fund or Product Type Code = 
15 Section 529 Money Market Funds, 
then Record Type 033, Money Market 
Fund Data should also be submitted 

---

## Page 116

Profile Security Database – Fixed Length Record Layouts 
Summary of changes – Effective date May 31, 2016 116 
SUMMARY OF CHANGES – EFFECTIVE DATE MAY 31, 
2016 
New Record Type Added 
New Record Number  Name of Record  Sequences 
RECORD TYPE 033 Money Market Fund Data 1-3 

---

## Page 117

Profile Security Database – Fixed Length Record Layouts 
Summary of changes – Effective date May 20, 2013 117 
SUMMARY OF CHANGES – EFFECTIVE DATE MAY 20, 
2013 
New Record Type Added 
New Record Number  Name of Record  Sequences 
RECORD TYPE 032 408(b) (2) Specific Data 1-4 
 
 
 
 

---

## Page 118

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 20, 2023 
Publication Code: MFS339 
Service: Mutual Fund Profile Service II 
Title: Profile Security Database – Fixed Length Record Layouts  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 