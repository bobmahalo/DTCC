---
title: "MFPS II - Profile Security Database – Variable Length Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_profile_security_redesign_var_layouts_mfs276_20230920.pdf"
pages: 83
size: "911.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II - Profile Security Database – Variable Length Record Layouts

**Original File:** [mfps2_profile_security_redesign_var_layouts_mfs276_20230920.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_profile_security_redesign_var_layouts_mfs276_20230920.pdf)  
**Category:** Other  
**Total Pages:** 83  
**File Size:** 911.6 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
PROFILE SECURITY DATABASE – VARIABLE 
LENGTH RECORD LAYOUTS 
SEPTEMBER 20, 2023 
 

---

## Page 2

Profile Security Database – Variable Length Record Layouts 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 4 
Start of Record Type 020 – General Profile ....................................................................................................... 5 
Input/Output (Batch)............................................................................................................................................ 5 
Start of Record Type 021 – Blue Sky Data ....................................................................................................... 19 
Input/Output (Batch)..........................................................................................................................................19 
Start of Record Type 022 - CDSC Data ............................................................................................................ 24 
Input / Output (Batch) .......................................................................................................................................24 
Start of Record Type 023 – Breakpoint Schedules ......................................................................................... 30 
Input/Output (Batch)..........................................................................................................................................30 
Start of Record Type 023 – Breakpoint Schedules .........................................................................................30 
Start of Record Type 024 – Commission Data ................................................................................................ 33 
Input/Output (Batch)..........................................................................................................................................33 
Start of Record Type 025 – [[NSCC]] Social Code Eligibility .............................................................................. 37 
Input/Output (Batch)..........................................................................................................................................37 
Start of Record Type 026 – Short Term Redemption Data ............................................................................. 39 
Input/Output (Batch)..........................................................................................................................................39 
Start of Record Type 029 – Linkage Rules Data ............................................................................................. 43 
Input/Output (Batch)..........................................................................................................................................43 
Start of Record Type 030 – Master Table Maintenance Record .................................................................... 48 
Fund Input Only ................................................................................................................................................48 
Fees and Expenses (Record Type 031) ........................................................................................................... 50 
Input/Output ......................................................................................................................................................50 
408(B) (2) Specific Data (Record Type 032) ..................................................................................................... 52 
Input/Output ......................................................................................................................................................52 
Money Market Fund Data (Record Type 033) .................................................................................................. 54 
Input/Output ......................................................................................................................................................54 
Appendix A: Valid Values for Investment Class Code ................................................................................... 57 
Appendix B – Valid Values for Social Code .................................................................................................... 59 
Appendix C: Modifications to Social Code Field Edits .................................................................................. 70 

---

## Page 3

Profile Security Database – Variable Length Record Layouts 
History of Important Notices 3 
Background .......................................................................................................................................................70 
APPENDIX D: SUMMARY OF CHANGES ......................................................................................................... 72 
Summary of Changes – Effective date March 28, 2022 .................................................................................. 73 
New Product Type Code – Interval Fund (48) ..................................................................................................73 
Summary of Changes – Effective date August 26, 2019 ................................................................................ 74 
Social Code .......................................................................................................................................................74 
Summary of Changes – Effective date March 25, 2019 .................................................................................. 75 
Reject Codes ....................................................................................................................................................75 
Summary of changes – Effective date July 13, 2018 ...................................................................................... 76 
Correction to Field Values Descriptions ...........................................................................................................76 
Summary of changes – Effective date July 9, 2018 ........................................................................................ 77 
New Fields Added .............................................................................................................................................77 
Existing Fields Modified ....................................................................................................................................77 
Summary of changes – Effective date August 22, 2016 ................................................................................. 79 
Summary of changes – Effective date May 31, 2016 ...................................................................................... 80 
New Record Type Added ................................................................................................................................... 81 
Summary of changes – Effective date May 20, 2013 ...................................................................................... 82 
New Record Type Added ..................................................................................................................................82 
 

---

## Page 4

Profile Security Database – Variable Length Record Layouts 
History of Important Notices 4 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Please See Important Notice 
September 20, 2023 Record rebranded and reviewed.  
May 1, 2023 MFPSII [[participant]] Profile database was 
decommissioned.  
Please See Important Notice a9279 P&S 8852 
Dated March 21, 2023 
 
There were two versions of User File Request (080) 
records.  As part of decommissioning of [[participant]] 
Database, the 080 record within this guide was moved 
to MFPS2 Part 6 records. 
March 28, 2022   a9044 P&S 8617 Dated September 2, 2021 
August 26, 2019 a8711 P&S 8286 dated May 30, 2019 
March 25, 2019 a8658 P&S 8233 dated December 19, 2018 
July 13, 2018 a8584 P&S 8159 dated July 13, 2018 
July 9, 2018 a8532 P&S 8107 dated March 20, 2018 (revised May 9, 
2018) 
August 22, 2016 a8227 P&S 7802 dated July 11, 2016 
May 31, 2016  a8163 P&S 7738 dated February 10, 2016 
November 30, 2015  #8073 P&S 7648 dated August 27, 2015 
September 22, 2014 & October 6, 2014 
July 28, 2014 
June 30, 2014 
Target second quarter 2014 
May 20, 2013 
a7876 P&S 7446 dated July 31, 2014 
a7825 P&S 7395 dated April 24, 2014 
a7702 P&S 7372 dated March 20, 2014 
a7699 P&S 7369 dated March 14, 2014 
a7608 P&S 7178 dated March 25, 2013 
May 20, 2013 a7608 P&S 7178 dated March 25, 2013 
November 24, 2008 a6717 P&S 6287 dated October 1, 2008 
August 18, 2008 a6675 P&S 6245 dated August 15, 2008  
a6650 P&S 6220 dated June 30, 2008  
a6640 P&S 6210 dated June 20, 2008  
a6614 P&S 6184 dated May 14, 2008 
March 27, 2006 a7171 P&S 5741 dated December 21, 2005 

---

## Page 5

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 5 
START OF RECORD TYPE 020 – GENERAL PROFILE 
Input/Output (Batch) 
Start of Record Type 020 – General Profile 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0750 
Must be 0232 if Action Type = ‘D’ 
R 0088 
Physical Sequence Number 5 6 2 A/N  R 0080 
Logical Sequence Number 7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output Only; Space on input 
‘R’ = Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 020 = Security Issue General 
Profile Data  
R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 49 50 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
60 60 1 A/N @ R 0041 
Distribution Reinvestment 
Eligible Code 
61 61 1 A/N 0 = No 
1 = Yes 
R 0180 

---

## Page 6

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 6 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Distribution Reinvestment 
Load Code 
62 62 1 A/N 0 = No 
1 = Yes 
Required if Distribution Reinvest 
Eligible Code = ‘1’ 
OC 0522 
Redemption Amount Code 63 63 1 A/N 0 = [[shares]] 
1 = Dollars 
2 = Both 
R 0356 
Cross Fund Distribution 
Reinvestment Eligible Code 
64 64 1 A/N 0 = No 
1 = Yes 
R 0188 
Cross Fund Distribution 
Reinvestment Load Code 
65 65 1 A/N 0 = No 
1 = Yes 
Required if Cross Fund Distribution 
Reinvestment Eligible Code = 1 
OC 0189 
Automatic Investment 
Eligible Code 
66 66 1 A/N 0 = No 
1 = Yes 
R 0523 
Automatic Withdrawal 
Eligible Code 
67 67 1 A/N 0 = No 
1 = Yes 
R 0524 
Filler  68 71 4 A/N Space R  
DCC&S Eligible 
 
72 72 1 A/N 0 = No 
1 = Yes 
R 0810 
Defined Contribution 
Clearance & [[settlement]] 
(“DCC&S”) Cut-Off Cycle 
 
 
73 76 4 A/N 0001 = [[NSCC]] Cycle 01 
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
LF02 = [[NSCC]] Late File Cycle 02 
LF03 = [[NSCC]] Late File Cycle 03 
LF98 = [[NSCC]] Late File Cycle 98 
 
Required if DCC&S Eligible field = 
1 (Yes) 
OC 0811 
Filler 77 78 2 A/N Space R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 

---

## Page 7

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 7 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
R  
[[NSCC]] Reject Code 1 81 84 4 A/N Input : Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N @ R 0526 
Load Type Code 105 105 1 A/N 0 = Front-End Load 
1 = Back-End Load 
2 = Level Load 
3 = Hybrid 
4 = No Load 
5 = Load Other 
R 0154 
NAV Employee Code 106 106 1 A/N 0 = No  
1 = Yes 
R 0325 
NAV Wrap Code 107 107 1 A/N 0 = No  
1 = Yes 
R 0327 
ROA Eligible Code 108 108 1 A/N 0 = No  
1 = Yes 
R 0156 
Maximum Purchase Amount 109 124 16 N 99999999999999.99 R 0521 
Minimum Initial Purchase 
Amount 
125 140 16 N 99999999999999.99 R 0166 
Minimum Subsequent 
Purchase Amount 
141 156 16 N 99999999999999.99 R 0169 
Filler  157 158 2 A/N Space R  
Fund Portfolio Name 159 218 60 A/N @ R 0527 
[[Dividend]] Accrual Purchase 
T+1 Start Date Code 
 
 
219 219 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0812 
 

---

## Page 8

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 8 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[Dividend]] Accrual 
Redemption T+1 Stop Date 
Code 
 
 
220 220 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0813 
 
[[Dividend]] Accrual Partial 
Exchange Out Stop Date 
Code 
 
 
221 221 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0814 
 
[[Dividend]] Accrual Partial 
Exchange In Start Date 
Code 
 
 
222 222 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0815 
 
[[Dividend]] Accrual Partial 
Transfer Out Stop Date 
Code 
 
 
223 223 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0816 
 
[[Dividend]] Accrual ACAT 
Transfer in Start Date Code 
 
 
224 224 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0817 
 

---

## Page 9

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 9 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[Dividend]] Accrual ACAT 
Transfer Out Stop Date 
 
 
225 225 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0818 
 
DCC&S [[Dividend]] Accrual 
Purchase Start Date Code 
 
 
226 226 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0819 
 
DCC&S [[Dividend]] Accrual 
Purchase “G” indicator 
(Share Class Conversion) 
Start Date Code 
 
227 227 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0820 
 
DCC&S [[Dividend]] Accrual 
Purchase “L” indicator 
(Omnibus [[Dividend]] 
Reconciliation) Start Date 
Code 
 
228 228 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0821 
DCC&S [[Dividend]] Accrual 
Redemption Stop Date Code 
 
 
229 229 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0822 

---

## Page 10

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 10 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
DCC&S [[Dividend]] Accrual 
Redemption “G” indicator 
(Share Class Conversion) 
Stop Date Code 
 
 
230 230 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0823 
DCC&S [[Dividend]] Accrual 
Redemption “L” indicator 
(Omnibus [[Dividend]] 
Reconciliation) Stop Date 
Code 
 
 
231 231 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
O/C 0824 
Filler 232 232 1 A/N Space R  
Minimum Coverdell IRA 
Purchase Amount 
233 248 16 N 99999999999999.99 R 0228 
Minimum Coverdell IRA 
Subsequent Purchase 
Amount 
249 264 16 N 99999999999999.99 R 0165 
Minimum Wrap Initial 
Purchase Amount 
265 280 16 N 99999999999999.99 R 0320 
Minimum Wrap Subsequent 
Purchase Amount 
281 296 16 N 99999999999999.99 R 0530 
Share Conversion Cycle 
Eligibility Method Code 
297 297 1 A/N 0 = Anniversary Day 
1 = Anniversary Month – First Day 
2 = Anniversary Month – Last Day 
3 = Anniversary Year 
4 = Month after Anniversary 
 
Req.’d if Share Conversion Cycle 
Code Not = ‘0’ 
OC 0533 

---

## Page 11

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 11 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Share Conversion Cycle 
Date  
298 299 2 A/N 01 – 31 = Day of Month  
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
300 300 1 A/N 0 = Next Business Day 
1 = Prior Business Day 
 
Required if “Share Conversion 
Cycle Date” not = (“FF” or “LL”) 
OC 0536 Eligible for Externalized 
Commission  
 
 
301 301 1 A/N 0 = No 
1 = Yes 
R 0825 
Large Trade Notification 
Required 
 
302 302 1 A/N 0 = No, large Trade Notification Is 
Not Required 
1 = Yes, Large Trade Notification Is 
Required 
R 0826 
Filler 303 306 4 A/N Space R  
Minimum "Qualified Plans" 
Initial Purchase Amount 
307 322 16 N 99999999999999.99 R 0531 
Minimum "Qualified Plans" 
Subsequent Purchase 
Amount 
323 338 16 N 99999999999999.99 R 0532 
Maximum Account Value 339 354 16 N 99999999999999.99 R 0538 
Maximum Account Value 
Code 
355 355 1 A/N 0 = Fund Complex 
1 = Share Class 
2 = Individual Security Issue [[ID]] 
R 0539 

---

## Page 12

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 12 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Share Conversion Cycle 
Code 
356 356 1 A/N 0 = [[shares]] [[DO]] Not Convert 
1 = Weekly 
2 = Monthly 
3 = Quarterly 
4 = Semi-Annually 
5 = Annually 
R 0218 
Share Conversion Age 357 359 3 N 999 
Required if Share Conversion 
Cycle Code is NOT = 0  
OC 0540 
Share Conversion Cycle 
Starting Month 
360 361 2 N 99 
Required if Share Conversion 
Cycle Code equal to ‘3’, or ‘4’, or 
‘5’ 
OC 0541 
NAV Repurchase Code 362 362 1 A/N 0 = No 
1 = Yes, Same class Only 
2 = Yes, Different class 
Only 
3 = Yes, Same or Different Class 
R 0324 
NAV Repurchase Days 363 365 3 N 999 
Required if NAV Repurchase Code 
= “1”, “2” or “3” 
OC 0543 
Filler 366 366 1 A/N Space R  
NAV Repurchase Frequency 
Code 
367 368 2 A/N 01 = Once per year 
02 = Twice per year 
03 = No restrictions 
04 = Once in a lifetime 
98 = Other (see Prospectus) 
 
Required if NAV Repurchase Code 
= ‘1’, ‘2’ or ‘3’ 
OC 0546 
CDSC Rules Apply Code 369 369 1 A/N 0 = No  
1 = Yes 
2 = Yes, Finder’s Fee / Jumbo 
Purchases Only 
 
 
R 0509 
Breakpoint Rules Apply 
Code 
370 370 1 A/N 0 = No  
1 = Yes 
R 0510 

---

## Page 13

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 13 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
12b-1 Commission Rules 
Apply Code 
371 371 1 A/N 0 = No 
1 = Yes 
R 0511 
LOI Rules Apply Code 372 372 1 A/N 0 = No 
1 = Yes 
R 0512 
[[Dividend]] Accrual Full 
Exchange In Start Date 
Code 
 
 
373 373 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
OC 0636 
[[Dividend]] Accrual Full 
Exchange Out Stop Date 
Code 
 
 
374 374 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if  
[[Dividend]] Type Code = 1 or 2 
OC 0637 
[[Dividend]] Accrual Full 
Transfer IN Start Date Code 
 
 
375 375 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if  
[[Dividend]] Type Code = 1 or 2 
OC 0638 
[[Dividend]] Accrual Partial 
Transfer IN Start Date Code 
 
 
376 376 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
 Required if [[Dividend]] Type Code = 
1 or 2 
OC 0639 
[[Dividend]] Accrual Full 
Transfer OUT Stop Date 
Code 
 
 
377 377 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if [[Dividend]] Type Code = 
1 or 2 
OC 0640 

---

## Page 14

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 14 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Number of Eligible Social 
Codes 
378 380 3 N 999 R 0641 
Product Type Code 381 382 2 A/N 01 = Mutual Fund 
02 = Money Market Mutual Fund 
03 = [[UIT]] (Unit Investment Trust) 
04 = Closed-End Mutual Fund 
05 = GIC (Guaranteed Investment 
Contract) 
06 = Stable Value Fund 
07 = Separate Account 
08 = Bank Collective Trust 
09 = Offshore (NRA) Fund 
10 = BIC (Bank Investment 
Contract) 
11 = Section 529 College Savings 
Plan 
12 = Offshore U.S. Dollar 
Enhanced ( [[DO]] not use – domestic 
funds on Profile Security only) 
13 = Offshore Non-U.S. Dollar 
Enhanced ([[DO]] not use - domestic 
funds on Profile Security only) 
14 = Annuity (with underlying 
[[Mutual Funds]]) 
15 = Section 529 Money Market 
Fund 
48 = Interval Fund 
 
Best Practice: When Product Type 
Code = 02 (Money Market Mutual 
Fund) or 15 (Section 529 Money 
Market Fund), Record Type 033 - 
‘Money Market Fund Data’ should 
also be submitted. 
R 0227 
Investment Class Code 383 384 2 A/N See Appendix A R 0157 
Date of Current Prospectus 385 392 8 A/N ccyymmdd R 0236 
Date of Most Recent 
Prospectus Supplement 
393 400 8 A/N ccyymmdd R 0614 
Offering Type Code 401 401 1 A/N 0 = Continuous 
1 = Selling Period 
R 0173 

---

## Page 15

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 15 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Purchase Eligibility Code 402 402 1 A/N 0 = All (New and Existing) 
1 = Existing Only 
2 = Closed 
3 = Restrictions Apply (see 
Prospectus) 
R 0197 
Restricted Redemption Code 403 403 1 A/N 0 = No 
1 = Yes 
R 0198 
Exchange Buy Eligibility 
Code 
404 404 1 A/N 0 = All (New and Existing) 
1 = Existing Only 
2 = Closed 
3 = Restrictions Apply (see 
Prospectus)  
R 0362 
Exchange Sell Eligibility 
Code 
405 405 1 A/N 0 = No 
1 = Yes 
R 0616 
Redemption Fee Code 406 406 1 A/N 0 = No Non-Short-Term 
Redemption Fee 
1 = Percentage 
2 = Fixed Dollar 
R 0184 
Redemption Fee Amount 407 422 16 N 99999999999999.99 
 Required if Redemption       
 Fee Code = 2 
OC 0185 
Redemption Fee Percentage 423 427 5 N 99.999 
Required if Redemption Fee Code 
= 1 
OC 0615 
Selling Period Open Date 428 435 8 A/N ccyymmdd R 0210 
Minimum 
Periodic/Systematic 
Investment Purchase 
Amount 
436 451 16 N 99999999999999.99 R 0537 
NAV Repurchase CDSC 
Reimbursement Code 
452 452 1 A/N 0 = Not applicable 
1 = Not reimbursed 
2 = Reimbursed 
3 = Reimbursed through purchase 
of additional [[shares]] at NAV 
 
Required if NAV Repurchase Code 
= ‘1’ , ‘2’ or ‘3’ 
OC 0545 

---

## Page 16

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 16 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[Dividend]] Accrual Bulk Rate 
Method Code 
453 453 1 A/N 0 = Prior Business Day 
1 = Next Business Day 
2 = Not Applicable Individual Rates 
Provided 
 
Required If [[Dividend]] Type Code = 
‘1’ or = ‘2’ 
OC 0633 
[[Dividend]] Accrual Month End 
Bulk Rate Method Code 
454 454 1 A/N 0 = Prior Business Day 
1 = Next Business Day 
2 = Split Prior/Next Business Day 
3 = Not Applicable Individual Rates 
Provided  
 
Required If [[Dividend]] Type Code = 
‘1’ or = ‘2’ 
OC 0634 
Selling Period Close Date 455 462 8 A/N ccyymmdd R 0211 
[[Dividend]] Type Code 463 463 1 A/N 0 = Record Date 
1 = Daily Accrual 
2 = Compounded Daily Accrual 
3 = Fund Does Not Pay Dividends 
R 0212 
[[Dividend]] Accrual Purchase 
T+2 Start Date Code 
 
 
464 464 1 A/N 0 = [[settlement]] Date 
1 = [[settlement]] Date + 1 
2 = Trade Date 
3 = Trade Date + 1  
 
Required if  
[[Dividend]] Type Code = 1 or 2 
OC 0617 
[[Dividend]] Accrual 
Redemption T+2 Stop Date 
Code 
 
 
465 465 1 A/N 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
 
Required if  
[[Dividend]] Type Code = 1 or 2 
OC 0618 

---

## Page 17

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 17 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[Dividend]] Frequency Code 466 466 1 A/N 0 = Monthly 
1 = Quarterly 
2 = Semi-Annually 
3 = Annually 
 
Required if [[Dividend]] Type Code 
Not = 3 
OC 0213 
Exchange Fee Code 467 467 1 A/N 0 = No Exchange Fee 
1 = Percentage 
2 = Fixed Dollar 
R 0149 
Exchange Fee Amount 468 483 16 N 99999999999999.99 
Required if Exchange Fee Code = 
2 
OC 0150 
Exchange Fee Percentage 484 488 5 N 99.999 
Required if Exchange Fee Code = 
1 
OC 0619 
Large Trade Threshold 
Dollar Amount 
 
 
489 504 16 A/N 99999999999999.99 
Required if Large Trade 
Notification Required = 1 (Yes) 
R 0827 
Fund Status Code 505 505 1 A/N 0 = Open 
1 = Closed – Liquidated 
2 = Closed - Merged 
R 0239 
STR Rules Apply Code 506 506 1 A/N 0 = No 
1 = Yes 
R 0621 
Symbol 507 518 12 A/N Req’ if “Symbol Code” not = “3” OC 0163 
Symbol Code 519 519 1 A/N 0 = Fund Created 
1 = [[NASDAQ]] 
2 = Proposed 
3= Not Applicable 
R 0507 
Internal Fund Number 520 527 8 A/N  R 0200 
ROA/ LOI Aggregation 
Inclusion Code 
 
 
528 528 1 A/N 0 = No 
1 = ROA  
2 = LOI   
3 = ROA & LOI   
R 0632 

---

## Page 18

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 020 – General Profile 18 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Share Conversion Receiving 
Security [[ID]] 
529 540 12 A/N Required if Share Conversion 
Cycle Code in “020” Not = ‘0’ 
OC 0219 
Merged Security [[ID]] 541 552 12 A/N Required if Fund Status Code in 
“020” = ‘2’ 
OC 0241 
Statement Security [[ID]] Short 
Name 
553 562 10 A/N  R 0628 
Statement Security [[ID]] 
Medium Name 
563 582 20 A/N  R 0629 
NAV Repurchase Share 
Class 
583 602 20 A/N Required If NAV Repurchase Code 
= ‘2’ or ‘3’  
OC 0542 
Fund Family Brand Name 603 662 60 A/N  R 0528 
Fiscal Year-End Day 663 666 4 N mmdd R 0613 
NAV Repurchase Account 
Eligibility Code 
667 668 2 A/N 01 = Same account where 
redemption occurred 
02 = Any account with the same 
registration 
03 = Any account eligible to be 
linked for ROA 
 
Required if NAV Repurchase Code 
= ‘1’, ‘2’ or ‘3’ 
OC 0544 
CDSC Aging Applies 669 669 1 A/N 0 = No 
1 = Yes 
R 0697 
Filler 670 676 7 A/N  R  
Statement Security [[ID]] Long 
Name 
677 716 40 A/N  R 0630 
Minimum IRA/Roth IRA 
Initial Purchase Amount 
717 732 16 N 99999999999999.99 R 0355 
Minimum IRA/Roth IRA 
Subsequent Purchase 
Amount 
733 748 16 N 99999999999999.99 R 0354 
NAV Purchases Eligible for 
ROA Code 
749 749 1 A/N 0 = No 
1 = Yes 
R 0475 
NAV Purchases Eligible for 
LOI Code 
750 750 1 A/N 0 = No 
1 = Yes 
R 0476 

---

## Page 19

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 021 – Blue Sky Data 19 
START OF RECORD TYPE 021 – BLUE SKY DATA 
Input/Output (Batch) 
Start of Record Type 021 – Blue Sky Data 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0232,0306 
Must be 0232 if Action Type = 
‘D’ 
R 0088 
Physical Sequence Number 5 6 2 A/N  R 0080 
Logical Sequence Number 7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output Only; Space on input 
‘R’ = Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security 
Issue 
R 0082 
Record Type 14 16 3 A/N 021 = Security Issue Blue Sky R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 49 50 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check Digit 60 60 1 A/N @ R 0041 
Blue Sky Eligible State Postal 
Code 1 
61 62 2 A/N Standard Fund/SERV State 
Code  
R 0242 
Blue Sky Eligible State Postal 
Code 2 
63 64 2 A/N Standard Fund/SERV State 
Code  
O 0242 

---

## Page 20

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 021 – Blue Sky Data 20 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Blue Sky Eligible State Postal 
Code 3 
65 66 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 4 
67 68 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 5 
69 70 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 6 
71 72 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 7 
73 74 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 8 
75 76 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 9 
77 78 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
R  
[[NSCC]] Reject Code 1 81 84 4 A/N Input : Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N @ R 0526 
Blue Sky Eligible State Postal 
Code 10 
105 106 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 11 
107 108 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 12 
109 110 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 13 
111 112 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 14 
113 114 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 15 
115 116 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 16 
117 118 2 A/N Standard Fund/SERV State 
Code  
O 0242 

---

## Page 21

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 021 – Blue Sky Data 21 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Blue Sky Eligible State Postal 
Code 17 
119 120 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 18 
121 122 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 19 
123 124 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 20 
125 126 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 21 
127 128 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 22 
129 130 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 23 
131 132 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 24 
133 134 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 25 
135 136 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 26 
137 138 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 27 
139 140 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 28 
141 142 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 29 
143 144 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 30 
145 146 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 31 
147 148 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 32 
149 150 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 33 
151 152 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 34 
153 154 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 35 
155 156 2 A/N Standard Fund/SERV State 
Code  
O 0242 

---

## Page 22

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 021 – Blue Sky Data 22 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Blue Sky Eligible State Postal 
Code 36 
157 158 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Fund Portfolio Name 159 218 60 A/N @ R 0527 
Blue Sky Eligible State Postal 
Code 37 
219 220 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 38 
221 222 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 39 
223 224 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 40 
225 226 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 41 
227 228 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 42 
229 230 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 43 
231 232 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 44 
233 234 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 45 
235 236 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 46 
237 238 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 47 
239 240 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 48 
241 242 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 49 
243 244 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 50 
245 246 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 51 
247 248 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 52 
249 250 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 53 
251 252 2 A/N Standard Fund/SERV State 
Code  
O 0242 

---

## Page 23

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 021 – Blue Sky Data 23 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Blue Sky Eligible State Postal 
Code 54 
253 254 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 55 
255 256 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 56 
257 258 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 57 
259 260 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 58 
261 262 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 59 
263 264 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 60 
265 266 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 61 
267 268 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 62 
269 270 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Blue Sky Eligible State Postal 
Code 63 
271 272 2 A/N Standard Fund/SERV State 
Code  
O 0242 
Filler 273 306 34 A/N  R  

---

## Page 24

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 022 - CDSC Data 24 
START OF RECORD TYPE 022 - CDSC DATA 
Input / Output (Batch) 
Start of Record Type 022- CDSC Data 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 232,454,…,1342 
Must be 0232 if Action  
Type = ‘D’ 
R 0088 
Physical Sequence Number 5 6 2 A/N  R 0080 
Logical Sequence Number 7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output Only; Space on input  
‘R’ = Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 022 = Security Issue CDSC Data  R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 49 50 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check Digit 60 60 1 A/N @ R 0041 
Advanced Commission Rate 
(formerly CDSC Commission 
Rate)  
61 69 9 N 99.9999999 R 0547 
CDSC Death Waiver Code 70 70 1 A/N 0 = No  
1 = Yes 
R 0341 

---

## Page 25

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 022 - CDSC Data 25 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
CDSC Disability Waiver Code 71 71 1 A/N 0 = No  
1 = Yes 
R 0342 
CDSC Divorce Waiver Code 72 72 1 A/N 0 = No  
1 = Yes 
R 0367 
CDSC Correction Waiver Code 73 73 1 A/N 0 = No  
1 = Yes 
R 0179 
Filler 74 78 5 A/N  R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
R  
[[NSCC]] Reject Code  81 84 4 A/N Input: Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N @ R 0526 
CDSC Systematic Withdrawal 
Waiver Code 
105 105 1 A/N 0 = No  
1 = Yes 
R 0549 
CDSC Defined Contribution 
Waiver Code 
106 106 1 A/N 0 = No  
1 = Yes 
R 0550 
CDSC Hardship Waiver Code 107 107 1 A/N 0 = No  
1 = Yes 
R 0551 
CDSC Termination Distribution 
Waiver Code 
108 108 1 A/N 0 = No  
1 = Yes 
R 0552 
CDSC Involuntary Distribution 
Waiver Code 
109 109 1 A/N 0 = No  
1 = Yes 
R 0553 
CDSC Forfeiture Distribution 
Waiver Code 
110 110 1 A/N 0 = No  
1 = Yes 
R 0554 
CDSC Loan Distribution Waiver 
Code 
111 111 1 A/N 0 = No  
1 = Yes 
R 0555 
CDSC Excess Contribution 
Distribution Waiver Code 
112 112 1 A/N 0 = No  
1 = Yes 
R 0556 

---

## Page 26

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 022 - CDSC Data 26 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
CDSC Qualified Distribution 
Waiver Code 
113 113 1 A/N 0 = No  
1 = Yes 
R 0557 
CDSC Qualified Distribution 
Waiver Age 
114 116 3 N 99.9 
Required if CDSC Qualified 
Distribution Waiver Code = ‘1’ 
OC 0558 
CDSC Aging Method Code 117 117 1 A/N 0 = Anniversary Date 
1 = Anniversary Month - 1st Day 
2 = Anniversary Month - Last Day 
3 = Anniversary Year 
4 = Month after Anniversary 
R 0559 
CDSC Calculation Method Code 118 118 1 A/N 0 = Lower of Cost or Market 
1 = Higher of Cost or Market 
2 = Current Market 
3 = Original Cost 
4 = Use Accumulated Dollars 
R 0560 
CDSC Redemption Hierarchy 
Method Code (assumption is 
free [[shares]] always first) 
119 119 1 A/N 0 = Lot Level Appreciation 
1 = Account Level Appreciation 
2 = Proportional Lot 
3 = Preferred Lot 
4 = Breakpoint Lot 
5 = Reverse Lot Level   
Appreciation 
6 = Commissionable Dollars 
Appreciation 
7 = Commission and Free Dollars 
Appreciation 
8 = Lot Level Depreciation Only 
R 0561 
CDSC Exchange Hierarchy 
Method Code 
120 120 1 A/N 0 = Lot Level Appreciation 
1 = Account Level Appreciation 
2 = Proportional Lot 
3 = Preferred Lot 
4 = Breakpoint Lot 
5 = Reverse Lot Level 
Appreciation 
6 = Commissionable Dollars 
Appreciation 
7 = Commission and Free Dollars 
Appreciation 
8 = Lot Level Depreciation Only 
R 0562 

---

## Page 27

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 022 - CDSC Data 27 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
CDSC Transfer Hierarchy 
Method Code 
121 121 1 A/N 0 = Lot Level Appreciation 
1 = Account Level Appreciation 
2 = Proportional Lot 
3 = Preferred Lot 
4 = Breakpoint Lot 
5 = Reverse Lot Level 
Appreciation 
6 = Commissionable Dollars 
Appreciation 
7 = Commission and Free Dollars 
Appreciation 
R 0563 
CDSC Exchange Buy Aging 
Schedule Code 
122 122 1 A/N 0 = Use Buy Fund Schedule 
1 = Retain Sell Fund Schedule 
2 = Longer of Buy or Sell Fund 
Schedule 
3 = Shorter of Buy or Sell Fund 
Schedule 
R 0564 
CDSC Aging Start Date 123 123 1 A/N 0 = Trade Date 
1 = [[settlement]] Date 
R 0565 
CDSC Death Waiver Time 
Period 
124 125 2 N In months 
Required if CDSC Death Waiver 
Code = ‘1’ 
OC 0566 
CDSC Required Minimum 
Distribution Amount Code 
126 126 1 A/N 0 = Waived on Fund Amount 
1 = Waived on Full Amount 
 
Required if CDSC Qualified 
Distribution Waiver Code = 1 
OC 0567 Number of CDSC Schedules 127 128 2 N 99 
Maximum 5 Schedules 
R 0568 
CDSC Systematic Withdrawal 
Waiver Percentage 
129 133 5 N 999.99 
Required if CDSC Systematic 
Withdrawal Waiver Code = ‘1’ 
O/C 0694 
Alternate CDSC / Compensation 
Schedule Exists 
134 134 1 A/N 0 = No 
1 = Yes –waived dealer 
concession, no CDSC, 
immediate trails 
R 0695 
Filler 135 158 24 N  R  
Fund Portfolio Name 159 218 60 A/N @ R 0527 

---

## Page 28

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 022 - CDSC Data 28 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Filler 219 232 14 N  R  
Start of Schedule 1 section 
CDSC Schedule 1 Lower Limit 233 248 16 N 99999999999999.99 R 0569 
CDSC Schedule 1 Upper Limit  249 264 16 N 99999999999999.99 R 0570 
Number of CDSC rates in 
Schedule 1 
265 266 2 N 99 
Maximum 15 Rates 
R 0571 
CDSC Schedule 1 Share Age-1  267 269 3 N 999 R 0245 
CDSC Schedule 1 Rate-1 270 278 9 N 99.9999999 R 0246 
CDSC Schedule 1 Share Age-2 279 281 3 N 999 O 0245 
CDSC Schedule 1 Rate-2 282 290 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-3 291 293 3 N 999 O 0245 
CDSC Schedule 1 Rate-3 294 302 9 N 99.9999999 O 0246 
Filler 303 306 4 N  R  
CDSC Schedule 1 Share Age-4  307 309 3 N 999 O 0245 
CDSC Schedule 1 Rate-4 310 318 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-5 319 321 3 N 999 O 0245 
CDSC Schedule 1 Rate-5 322 330 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-6 331 333 3 N 999 O 0245 
CDSC Schedule 1 Rate-6 334 342 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-7 343 345 3 N 999 O 0245 
CDSC Schedule 1 Rate-7 346 354 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-8 355 357 3 N 999 O 0245 
CDSC Schedule 1 Rate-8 358 366 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-9 367 369 3 N 999 O 0245 
CDSC Schedule 1 Rate-9 370 378 9 N 99.9999999 O 0246 
Filler 379 380 2 N  R  
CDSC Schedule 1 Share Age-10  381 383 3 N 999 O 0245 
CDSC Schedule 1 Rate-10 384 392 9 N 99.9999999 O 0246 

---

## Page 29

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 022 - CDSC Data 29 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
CDSC Schedule 1 Share Age-11 393 395 3 N 999 O 0245 
CDSC Schedule 1 Rate-11 396 404 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-12 405 407 3 N 999 O 0245 
CDSC Schedule 1 Rate-12 408 416 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-13 417 419 3 N 999 O 0245 
CDSC Schedule 1 Rate-13 420 428 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-14 429 431 3 N 999 O 0245 
CDSC Schedule 1 Rate-14 432 440 9 N 99.9999999 O 0246 
CDSC Schedule 1 Share Age-15 441 443 3 N 999 O 0245 
CDSC Schedule 1 Rate-15 444 452 9 N 99.9999999 O 0246 
Filler 453 454 2 N  R  
End of Schedule 1 section; Start of Schedule 2 section 
 
Positions 233 through 454 above can repeat for up to 5 schedules as follows: 
Schedule 2 – Positions 455 through 676  
Schedule 3 – Positions 677 through 898  
Schedule 4 – Positions 899 through 1120  
Schedule 5 – Positions 1121 through 1342 

---

## Page 30

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 023 – Breakpoint Schedules 30 
START OF RECORD TYPE 023 – BREAKPOINT 
SCHEDULES 
Input/Output (Batch) 
Start of Record Type 023 – Breakpoint Schedules 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 232,0306,0454, 972 
Must be 0232 if Action Code = 
‘D’ 
R 0088 
Physical Sequence Number 5 6 2 A/N  R 0080 
Logical Sequence Number 7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output Only; Space on input 
‘R’ = Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 023 = Security Issue 
Breakpoint Schedule Data ( 
Class Level ) 
R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 49 50 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check Digit 60 60 1 A/N @ R 0041 
Finder’s Fee/Jumbo Breakpoint 
Blending Applies Code (formerly 
61 61 1 A/N 0 = No R 0610 

---

## Page 31

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 023 – Breakpoint Schedules 31 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Breakpoint Blending Applies 
Code) 
1 = Yes 
2 = Yes, Finder’s Fee / Jumbo 
Purchases Only 
Number of Breakpoints 62 63 2 N 99 
maximum 10 breakpoints 
R 0247 
Filler 64 78 15 A/N  R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
R  
[[NSCC]] Reject Code  81 84 4 A/N Input: Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N @ R 0526 
Filler 105 158 54 A/N  R  
Fund Portfolio Name 159 218 60 A/N @ R 0527 
Filler 219 232 14 A/N  R  
Start of Rates Data 
Breakpoint Minimum Account 
Value 
233 248 16 N 99999999999999.99 R 0248 
Breakpoint Maximum Account 
Value 
249 264 16 N 99999999999999.99 R 0249 
Breakpoint Sales Charge Rate 265 269 5 N 99.999 R 0611 
Breakpoint Dealer Concession 
Rate 
270 274 5 N 99.999 R 0251 
Breakpoint [[underwriter]] Rate 275 279 5 N 99.999 R 0612 
Filler 280 306 27 A/N  R  
Rates Data can repeat 9 more times for a total of 10 Breakpoints 
 
Breakpoint 2 – position 307 through 380 
Breakpoint 3 – position 381 through 454 
Breakpoint 4 – position 455 through 528 
Breakpoint 5 – position 529 through 602 

---

## Page 32

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 023 – Breakpoint Schedules 32 
Breakpoint 6 – position 603 through 676 
Breakpoint 7 – position 677 through 750 
Breakpoint 8 – position 751 through 824 
Breakpoint 9 – position 825 through 898 
Breakpoint 10 – position 899 through 972 

---

## Page 33

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 024 – Commission Data 33 
START OF RECORD TYPE 024 – COMMISSION DATA 
Input/Output (Batch) 
Start of Record Type 024 – Commission Data 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 232,454,…,1342 
Must be 0232 if Action Type = ‘D’ 
R 088 
Physical Sequence Number 5 6 2 A/N  R 0080 
Logical Sequence Number 7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output Only; Space on Input.  
‘R’ = Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 024 = Security Issue Commission 
Data  
R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 49 50 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
60 60 1 A/N @ R 0041 
12b-1 Payment Frequency 
Code 
61 61 1 A/N 0 = Monthly 
1 = Quarterly 
2 = Semi-Annually 
3 = Annually 
R 0269 

---

## Page 34

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 024 – Commission Data 34 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
12b-1 Redemption Hierarchy 
Code 
62 62 1 A/N 0 = First In/First Out (FIFO) 
1 = Last In/First Out (LIFO) 
2 = Proportional 
R 0268 
12b-1 Calculation Method 
Code 
63 63 1 A/N 0 = Average Daily Basis 
1 = Record Date [[shares]] 
R 0252 
12b-1 Average Daily [[Asset]] 
Calculation Start Day 
64 65 2 A/N 01 -31 = Day of Month 
FF = First Business Day 
LL = Last Business Day  
Required If 12b-1 Calculation 
Method Code = ‘0’ 
OC 0572 
12b -1 Record Date  66 67 2 A/N 01 - 30 = Day of Month 
FF = First Business Day 
LL = Last Business Day  
LC = Last Calendar Day 
Required If 12b-1 Calculation 
Method Code = ‘1’ 
OC 0573 
12b-1 Record Date Day Code 68 68 1 A/N 0 = Next Business Day 
1 = Prior Business Day 
Req’ d If 12b-1 Record Date 
not=’FF’ or not=’LL’ 
OC 0574 
12b-1 Start Month 69 70 2 N Required if 12b-1 Payment 
Frequency Code = ‘1’ or ‘2’ or ‘3’ 
 0575 
12b-1 [[Dividend]] Share Aging 
Code 
71 71 1 A/N 0 = No 
1 = Yes 
R 0576 
Filler 72 78 7 A/N  R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
R  
[[NSCC]] Reject Code  81 84 4 A/N Input: Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N @ R 0526 

---

## Page 35

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 024 – Commission Data 35 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Number of 12b-1 Agreements 105 107 3 N 999 
maximum 5 Agreements 
R 0579 
Filler 108 158 51 A/N  R  
Fund Portfolio Name 159 218 60 A/N @ R 0527 
Filler 219 232 14 A/N  R  
Start of Agreements 1 section 
12b-1 Agreement 1 Date 233 240 8 A/N ccyymmdd 
@ 
R 0254 
12b-1 Post-Agreement 1 Rate 241 249 9 N 99.9999999 R 0255 
Number of 12b-1 Additional 
Rates for Agreement 1 
250 252 3 N maximum 15 rates R 0346 
Agreement 1 12b-1 Maximum 
Share Age 1 
253 255 3 N In month R 0344 
Agreement 1 12b-1 Rate 1 256 264 9 N 99.9999999 R 0345 
Agreement 1 12b-1 Maximum 
Share Age 2 
265 267 3 N In month O 0344 
Agreement 1 12b-1 Rate 2 268 276 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum 
Share Age 3 
277 279 3 N In month O 0344 
Agreement 1 12b-1 Rate 3 280 288 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum 
Share Age 4 
289 291 3 N In month O 0344 
Agreement 1 12b-1 Rate 4 292 300 9 N 99.9999999 O 0345 
Filler 301 306 6 A/N  R  
Agreement 1 12b-1 Maximum 
Share Age 5 
307 309 3 N In month R 0344 
Agreement 1 12b-1 Rate 5 310 318 9 N 99.9999999 R 0345 
Agreement 1 12b-1 Maximum 
Share Age 6 
319 321 3 N In month O 0344 
Agreement 1 12b-1 Rate 6 322 330 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum 
Share Age 7 
331 333 3 N In month O 0344 

---

## Page 36

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 024 – Commission Data 36 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Agreement 1 12b-1 Rate 7 334 342 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum 
Share Age 8 
343 345 3 N In month O 0344 
Agreement 1 12b-1 Rate 8 346 354 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum 
Share Age 9 
355 357 3 N In month O 0344 
Agreement 1 12b-1 Rate 9 358 366 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum 
Share Age 10 
367 369 3 N In month O 0344 
Agreement 1 12b-1 Rate 10 370 378 9 N 99.9999999 O 0345 
Filler 379 380 2 A/N  R  
Agreement 1 12b-1 Maximum 
Share Age 11 
381 383 3 N In month R 0344 
Agreement 1 12b-1 Rate 11 384 392 9 N 99.9999999 R 0345 
Agreement 1 12b-1 Maximum 
Share Age 12 
393 395 3 N In month O 0344 
Agreement 1 12b-1 Rate 12 396 404 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum 
Share Age 13 
405 407 3 N In month O 0344 
Agreement 1 12b-1 Rate 13 408 416 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum 
Share Age 14 
417 419 3 N In month O 0344 
Agreement 1 12b-1 Rate 14 420 428 9 N 99.9999999 O 0345 
Agreement 1 12b-1 Maximum 
Share Age 15 
429 431 3 N In month O 0344 
Agreement 1 12b-1 Rate 15 432 440 9 N 99.9999999 O 0345 
Filler 441 454 14 A/N  R  
 
Positions 233 through 454 above can repeat for up to 5 agreements as follows: 
Agreements2 – Positions 455 through 676  
Agreements3 – Positions 677 through 898  
Agreements4 – Positions 899 through 1120  
Agreements5 – Positions 1121 through 1342 

---

## Page 37

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 025 – [[NSCC]] Social Code Eligibility 37 
START OF RECORD TYPE 025 – [[NSCC]] SOCIAL CODE 
ELIGIBILITY 
Input/Output (Batch) 
Start of Record Type 025 – [[NSCC]] Social Code Eligibility 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 232 
Must be 0232 if Action Type = ‘D’ 
R 0088 
Physical Sequence Number 5 6 2 A/N  R 0080 
Logical Sequence Number 7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output only; Space on input  
‘R’ = Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 025 = Security Issue Purchase 
Eligibility Social Code Tables  
R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 49 50 2 A/N See ISO Country Codes 
Spaces for [[default]] 
O 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
60 60 1 A/N @ R 0041 
Filler 61 78 18 A/N  R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 

---

## Page 38

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 025 – [[NSCC]] Social Code Eligibility 38 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
R  
[[NSCC]] Reject Code  81 84 4 A/N Input: Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N @ R 0526 
Eligible Social Code 105 107 3 A/N Value entered in Cols 106 -107 will 
be validated  
except when entry is “ALL” 
 
See Appendix B for valid [[NSCC]] 
Eligible Social Codes 
R 0643 
Eligibility Code 108 108 1 A/N 0 = Eligible, No Restrictions 
1 = Eligible, Restriction may apply 
2 = Eligible at NAV, Restriction may 
apply  
R 0644 
Eligible Date 109 116 8 A/N CCYYMMDD 
Required if Eligibility-Code not= ‘0’ 
OC 0645 
Number of Eligible 
Participants Minimum 
117 119 3 N 999 
(See Appendix C for edit criteria)  
OC 0646 
Number of Active Participants 
Minimum 
120 122 3 N 999 
(See Appendix C for edit criteria)  
OC 0647 
Minimum [[Asset]] Size for 
Eligibility 
123 138 16 N 99999999999999.99 
(See Appendix C for edit criteria) 
OC 0648 
Maximum [[Asset]] Size for 
Eligibility 
139 154 16 N 99999999999999.99 R 0649 
Relationship between 
[[participant]] Minimum and 
[[Asset]] Size 
155 155 1 A/N 0 = Both must be met 
1 = Either must be met  
See Appendix C for Additional 
Validation Rules  
O/C 0696 
Filler 156 158 3 A/N  R  
Fund Portfolio Name 159 218 60 A/N @ R 0527 
Filler 219 232 14 A/N  R  

---

## Page 39

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 026 – Short Term Redemption Data 39 
START OF RECORD TYPE 026 – SHORT TERM 
REDEMPTION DATA 
Input/Output (Batch) 
Start of Record Type 026 – Short Term Redemption Data 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0306 
Must be 0232 if Action Type = ‘D’ 
R 0088 
Physical Sequence Number 5 6 2 A/N  R 0080 
Logical Sequence Number 7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output only; Space on input  
‘R’ = Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 026 = Short Term Redemption Data  R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 49 50 2 A/N See ISO Country Codes 
 
R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
60 60 1 A/N @ R 0041 
STR Minimum Amount 61 76 16 N 99999999999999.99 R 0580 
STR Share Aging Method 
Code 
77 77 1 A/N 0 = Calendar Days 
1 = Business Days 
R 0581 

---

## Page 40

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 026 – Short Term Redemption Data 40 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
STR Redemption 
Methodology Code 
78 78 1 A/N 0 = First In/First Out (FIFO) 
1 = Last In/First Out (LIFO) 
R 0582 
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple 
Errors 
R  
[[NSCC]] Reject Code  81 84 4 A/N Input: Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N @ R 0526 
STR Correction Waiver Code 105 105 1 A/N 0 = No 
1 = Yes 
R 0584 
STR Death Waiver Code 106 106 1 A/N 0 = No 
1 = Yes 
R 0585 
STR Disability Waiver Code 107 107 1 A/N 0 = No 
1 = Yes 
R 0586 
STR Qualified Distribution 
Waiver Code 
108 108 1 A/N 0 = No 
1 = Yes 
R 0587 
STR Qualified Distribution 
Waiver Age 
109 111 3 N 99.9 
Required if STR Qualified 
Distribution Waiver Code = “1” 
OC 0588 
STR Divorce Waiver Code 112 112 1 A/N 0 = No 
1 = Yes 
R 0589 
STR Systematic Withdrawal 
Waiver Code 
113 113 1 A/N 0 = No 
1 = Yes 
R 0590 
STR Defined Contribution 
Waiver Code 
114 114 1 A/N 0 = No 
1 = Yes 
R 0591 
STR Hardship Distribution 
Waiver Code 
115 115 1 A/N 0 = No 
1 = Yes 
R 0592 
STR Automatic Rebalance 
Waiver Code 
116 116 1 A/N 0 = No 
1 = Yes 
R 0593 

---

## Page 41

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 026 – Short Term Redemption Data 41 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
STR Termination Distribution 
Waiver Code 
117 117 1 A/N 0 = No 
1 = Yes 
R 0594 
STR Involuntary Distribution 
Waiver Code 
118 118 1 A/N 0 = No 
1 = Yes 
R 0595 
STR Forfeitures Distribution 
Waiver Code 
119 119 1 A/N 0 = No 
1 = Yes 
R 0596 
STR Loan Distribution 
Waiver Code 
120 120 1 A/N 0 = No 
1 = Yes 
R 0597 
STR Excess Contribution 
Distribution Waiver Code 
121 121 1 A/N 0 = No 
1 = Yes 
R 0598 
STR Wrap Fee Waiver Code 122 122 1 A/N 0 = No 
1 = Yes 
R 0599 
STR Plan Fee Waiver Code 123 123 1 A/N 0 = No 
1 = Yes 
R 0600 
STR Reinvested [[shares]] 
Waiver Code 
124 124 1 A/N 0 = No 
1 = Yes 
R 0601 
STR Exchange Buy 
Schedule Code 
125 125 1 A/N 0 = Retain Sell Fund Schedule 
1 = Use Buy Fund Schedule 
2 = Longer of Buy or Sell Fund 
Schedule 
3 = Shorter of Buy or Sell Fund 
Schedule 
R 0602 
STR Exchange Buy Aging 
Date Code 
126 126 1 A/N 0 = Original Date  
1 = Exchange Date 
R 0603 
STR Aging Start Date Code 127 127 1 A/N 0 = Trade Date 
1 = [[settlement]] Date 
R 0604 
STR Eligible Transaction 
Code 
128 128 1 A/N 0 = Redemptions 
1 = Exchanges 
2 = Both 
R 0605 
STR Payout Calculation 
Amount Code 
129 129 1 A/N 0 = Net Proceeds 
1 = Gross Proceeds 
R 0606 
Number of STR Rates 130 132 3 N 999 R 0607 
Filler 133 158 26 A/N  R  

---

## Page 42

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 026 – Short Term Redemption Data 42 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Fund Portfolio Name 159 218 60 A/N @ R 0527 
Filler 219 232 14 A/N  R  
STR Share Age 1 233 235 3 N 999 R 0608 
STR Rate 1 236 244 9 N 99.9999999 R 0609 
STR Share Age 2 245 247 3 N 999 O 0608 
STR Rate 2 248 256 9 N 99.9999999 O 0609 
STR Share Age 3 257 259 3 N 999 O 0608 
STR Rate 3 260 268 9 N 99.9999999 O 0609 
STR Share Age 4 269 271 3 N 999 O 0608 
STR Rate 4 272 280 9 N 99.9999999 O 0609 
STR Share Age 5 281 283 3 N 999 O 0608 
STR Rate 5 284 292 9 N 99.9999999 O 0609 
Filler 293 306 14 A/N  R  

---

## Page 43

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 029 – Linkage Rules Data 43 
START OF RECORD TYPE 029 – LINKAGE RULES DATA 
Input/Output (Batch) 
Start of Record Type 029 – Linkage Rules Data 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0306 
Must be 0232 if Action Type = ‘D’ 
R 0088 
Physical Sequence 
Number 
5 6 2 A/N  R 0080 
Logical Sequence 
Number 
7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output Only; Space on input 
‘R’ = Reminder on output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 029 = Security Issue Breakpoint 
Linkage Rules Data  
R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country 
Code 
49 50 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
60 60 1 A/N @ R 0041 
Link Across Dealer Code 61 61 1 A/N 0 = No 
1 = Yes 
R 0631 

---

## Page 44

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 029 – Linkage Rules Data 44 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
ROA Calculation 
Methodology Code 
62 63 2 A/N 01 = [[shares]] X [[public offering]] Price 
(POP) 
02 = [[shares]] X Net [[Asset]] Value (NAV) 
03 = Gross Dollars Invested (Purchases 
Only) 
04 = Net Dollars Invested (Purchases 
less Redemptions) 
05 = Greater of [[shares]] X Public 
Offering Price or Gross Dollars Invested 
06 = Greater of [[shares]] X Net [[Asset]] 
Value or Gross Dollars Invested 
07 = Greater of [[shares]] X Public 
Offering Price or Net Dollars Invested 
08 = Greater of [[shares]] X Net [[Asset]] 
Value or Net Dollars Invested 
99 = ROA Does Not Apply 
R 0454 
Link by Spouse Code 64 64 1 A/N 0 = No 
1 = Yes 
R 0477 
Link by Civil Union Code 65 65 1 A/N 0 = No 
1 = Yes 
R 0478 
Link by Domestic 
Partnership Code 
66 66 1 A/N 0 = No 
1 = Yes 
R 0479 
Link by Common Law 
Marriage Code 
67 67 1 A/N 0 = No 
1 = Yes 
R 0480 
Link by Parent Code 68 68 1 A/N 0 = No 
1 = Yes 
R 0481 
Link by Step Parent Code 69 69 1 A/N 0 = No 
1 = Yes 
R 0482 
Link by Legal Guardian 
Code 
70 70 1 A/N 0 = No 
1 = Yes 
R 0483 
Link by Child Code 71 71 1 A/N 0 = No 
1 = Yes 
R 0484 
Child Maturation Age 72 74 3 N 999 
Required if “Link by Child Code” = “1” 
OC 0485 
Link by Stepchild Code 75 75 1 A/N 0 = No 
1 = Yes 
R 0486 

---

## Page 45

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 029 – Linkage Rules Data 45 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Link by Sibling Code 76 76 1 A/N 0 = No 
1 = Yes 
R 0487 
Link by Grandchildren 
Code 
77 77 1 A/N 0 = No 
1 = Yes 
R 0488 
Link by Grandparents 
Code 
78 78 1 A/N 0 = No 
1 = Yes 
R 0489 
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple Errors 
  
[[NSCC]] Reject Code  81 84 4 A/N Input: Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N @ R 0526 
Link by Father-In-Law 
Code 
105 105 1 A/N 0 = No 
1 = Yes 
R 0490 
Link by Mother-In-Law 
Code 
106 106 1 A/N 0 = No 
1 = Yes 
R 0491 
Link by Brother-In-Law 
Code 
107 107 1 A/N 0 = No 
1 = Yes 
R 0492 
Link by Sister-In-Law 
Code 
108 108 1 A/N 0 = No 
1 = Yes 
R 0493 
Link by Trust Beneficiary 
Code 
109 109 1 A/N 0 = No 
1 = Yes 
R 0503 
Link by Trust Grantor 
Code 
110 110 1 A/N 0 = No 
1 = Yes 
R 0504 
Link by Household Code  111 111 1 A/N 0 = No 
1 = 9 Digit Zip Code 
2 = 9 Digit Zip Code, Last Name and 
Tax Identification number (2 out of 3 ) 
R 0692 
Link by Custodian Code 112 112 1 A/N 0 = No 
1 = Yes 
R 0693 
Filler 113 158 46 A/N  R  

---

## Page 46

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 029 – Linkage Rules Data 46 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Fund Portfolio Name 159 218 60 A/N @ R 0527 
Filler 219 232 14 A/N  R  
LOI Fulfillment Calculation 
Methodology Code 
233 234 2 A/N 01 = Gross Dollars Invested (Purchases 
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
 
Required if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0459 
LOI Fulfillment Period 235 237 3 N 999 
 
Required if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0460 
LOI Alternate Fulfillment 
Period 
238 240 3 N 999 
Required if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0623 
LOI Minimum Amount 241 256 16 N 99999999999999.99 
 
Required if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0462 
LOI Minimum Initial 
Purchase Amount Type 
Code 
257 257 1 A/N 0 = Percentage 
1 = Dollar Amount 
 
Required if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0624 

---

## Page 47

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 029 – Linkage Rules Data 47 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
LOI Minimum Initial 
Purchase Amount 
258 273 16 N 99999999999999.99 
Required if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0625 
LOI Backdating Allowed 
Code 
274 274 1 A/N 0 = No 
1 = Yes 
Required if : 
‘LOI Rules Apply Code’ in Record  
‘020’ = ‘1’ 
OC 0651 LOI Backdating Days 275 277 3 N 999 
Required if LOI Rules Apply Code in 
Record ‘020 = “1” 
and 
LOI Backdating Allowed Code = “1” 
OC 0626 
Filler 278 306 29 A/N  R  

---

## Page 48

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 030 – Master Table Maintenance Record 48 
START OF RECORD TYPE 030 – MASTER TABLE 
MAINTENANCE RECORD 
Fund Input Only  
Used to Change a Share Class Name, Fund Portfolio Name, or a Security Issue [[ID]]; or to Delete a Security 
Issue [[ID]] from the Master Tables 
Start of Record Type 030 – Master Table Maintenance Record 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0306 R 0088 
Physical Sequence Number 5 6 2 A/N  R 0080 
Logical Sequence Number 7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output Only; Space on input R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 030 = Master Tables Maintenance 
Record 
R 0083 
Action Type 17 17 1 A/N C = change  
(Class Name, Portfolio Name, 
Security [[ID]])  
 
D = Delete  
(Security [[ID]]) 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd (current business date 
only)  
R 0044 
Security Issue Country Code 49 50 2 A/N See ISO Country Codes 
Required if Target Field = ‘S’  
OC 0153 
Security Issue [[ID]] 51 59 9 A/N Required if Target Field = ‘S’  OC 0040 
ISIN Security Issue Check 
Digit 
60 60 1 A/N Required if Target Field = ‘S’  OC 0041 

---

## Page 49

Profile Security Database – Variable Length Record Layouts 
Start of Record Type 030 – Master Table Maintenance Record 49 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Filler 61 61 1 A/N Space R 0153 
Target Field 62 62 1 A/N C – Class Name 
P – Portfolio [[ID]] 
S – Security [[ID]] 
R 0670 
New Security Issue Country 
Code 
63 64 2 A/N See ISO Country Codes 
Required if Target Field = ‘S’ and 
Action Type = ‘C’ 
OC 0671 
New Security Issue [[ID]] 65 73 9 A/N Required if Target Field = ‘S’ and 
Action Type = ‘C’ 
OC 0672 
New ISIN Security Issue 
Check Digit 
74 74 1 A/N Required if Target Field = ‘S’ and 
Action Type = ‘C’ 
OC 0673 
Filler 75 78 4 A/N Space R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple 
Errors 
R  
[[NSCC]] Reject Code 1 81 84 4 A/N Input : Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N Required if Target Field = ‘C’ OC 0526 
New Share Class Name  105 124 20 A/N Required if Target Field = ‘C’ and 
Action Type = ‘C’ 
OC 0674 
Filler  125 158 34 A/N Space R  
Fund Portfolio Name 159 218 60 A/N Required if Target Field = ‘P’ OC 0527 
Filler 219 232 14 A/N  R  
New Fund Portfolio Name 233 292 60 A/N Required if Target Field = ‘P’ and 
Action Type = ‘C’ 
OC 0675 
Filler 293 306 14 A/N  R  

---

## Page 50

Profile Security Database – Variable Length Record Layouts 
Fees and Expenses (Record Type 031) 50 
FEES AND EXPENSES (RECORD TYPE 031) 
Input/Output  
Fees and Expenses (Record Type 031) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0232 R 0088 
Physical Sequence 
Number 
5 6 2 A/N  R 0080 
Logical Sequence 
Number 
7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output only; Space on input ‘R’ = 
Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 031 = Fees and Expenses Data  R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country 
Code 
49 50 2 A/N See ISO Country Codes 
 
R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
60 60 1 A/N @ R 0041 
Fees and Expenses As Of 
Date 
61 68 8 N ccyymmdd R 0760 
Total Annual Operating 
Expenses 
69 73 5 N 99.999 
Required if “Waiver Fee Indicator” = 
0 
OC 0761 

---

## Page 51

Profile Security Database – Variable Length Record Layouts 
Fees and Expenses (Record Type 031) 51 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Fee Waiver Indicator  74 74 1 N 0=No 
1=Yes 
R 0762 
Filler 75 78 4 A/N Space R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], Multiple 
Errors 
R  
[[NSCC]] Reject Code  81 84 4 A/N Input: Space 
Output: Reject code or space 
R  
Share Class Name 85 104 20 A/N @ R 0526 
Net Annual Operating 
Expenses 
105 109 5 N 99.999 
Required if “Waiver Fee Indicator = 
1” 
OC 0763 
Fee Waiver Rate 110 114 5 N 99.999 
Required if “Waiver Fee Indicator = 
1”  
OC 0764 
Filler 115 158 44 A/N  R  
Fund Portfolio Name 159 218 60 A/N @ R 0527 
Filler 219 232 14 A/N  R  

---

## Page 52

Profile Security Database – Variable Length Record Layouts 
408(B) (2) Specific Data (Record Type 032) 52 
408(B) (2) SPECIFIC DATA (RECORD TYPE 032)  
Input/Output  
408(b)(2) Specific Data (Record Type 032) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0306 R 0088 
Physical Sequence 
Number 
5 6 2 A/N  R 0080 
Logical Sequence 
Number 
7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output only; Space on input ‘R’ = 
Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 032 = 408(b)(2) Specific Data R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country 
Code 
49 50 2 A/N See ISO Country Codes  R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
60 60 1 A/N @ R 0041 
Portfolio Turnover Rate 61 66 6 N  R 0752 
Filler 67 78 12 A/N Space R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 

---

## Page 53

Profile Security Database – Variable Length Record Layouts 
408(B) (2) Specific Data (Record Type 032) 53 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[NSCC]] Rejection Indicator 80 80 1 A/N Input: Space 
Output: 
0 = Accepted by the [[NSCC]] 
1 = Rejected by the [[NSCC]] 
2 = Rejected by the [[NSCC]], Multiple 
Errors 
  
[[NSCC]] Reject Code 81 84 4 A/N Input: Space 
Output: Reject Code or Space 
R  
Share Class Name 85 104 20 A/N @ R  
Minimum Initial Purchase 
Amount via Exchange 
105 120 16 N  R 0753 
Minimum Subsequent 
Purchase Amount via 
Exchange 
121 136 16 N  R 0754 
Filler 137 158 22 A/N Space R  
Fund Portfolio Name 159 218 60 A/N @ R 0527 
Filler  219 232 14 A/N Space R  
Minimum Initial Purchase 
Amount Non-Qualified 
Plan  
233 248 16 N  R 0755 
Minimum Subsequent 
Purchase Amount Non-
Qualified Plan 
249 264 16 N  R 0756 
Minimum Initial Purchase 
Amount (Omnibus 
Account) 
265 280 16 N  R 0757 
Minimum Subsequent 
Purchase Amount 
(Omnibus Account) 
281 296 16 N  R 0758 
Filler 297 306 10 A/N Space R  

---

## Page 54

Profile Security Database – Variable Length Record Layouts 
Money Market Fund Data (Record Type 033) 54 
MONEY MARKET FUND DATA (RECORD TYPE 033) 
Input/Output  
Money Market Fund Data (Record Type 033) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Type Length 1 4 4 N 0232 
Must be 0232 if Action Type = ‘D’ 
R 0088 
Physical Sequence Number 5 6 2 A/N  R 0080 
Logical Sequence Number 7 8 2 A/N 01 R 0080 
Filler 9 9 1 A/N Space R  
Reminder Indicator 10 10 1 A/N Output Only; Space on input 
‘R’ = Reminder on Output 
R  
Originator Type Indicator 11 11 1 A/N ‘F’ = Fund R 0081 
Profile Type 12 13 2 A/N 06 = Hierarchical Security Issue R 0082 
Record Type 14 16 3 A/N 033 = Money Market Fund Data R 0083 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
R 0349 
Submitting [[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 32 11 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Profile Effective Date 41 48 8 A/N ccyymmdd 
@ 
R 0044 
Security Issue Country Code 49 50 2 A/N See ISO Country Codes 
@ 
R 0153 
Security Issue [[ID]] 51 59 9 A/N @ R 0040 
ISIN Security Issue Check 
Digit 
60 60 1 A/N @ R 0041 
[[Liquidity]] Fee / Redemption 
Gate Eligibility Fund 
Indicator 
61 61 1 A/N 0 – No, Fund is not subject not 
Money Market [[Liquidity]] Fees/ 
Redemption Gates 
1 – Yes, Fund is subject to (may 
potentially impose) Money Market 
[[Liquidity]] Fee/Redemption Gate 
R 0792 

---

## Page 55

Profile Security Database – Variable Length Record Layouts 
Money Market Fund Data (Record Type 033) 55 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Money Market Fund 
Indicator 
 
Note: Required when the 
Product Type Code = “02” 
(Money Market Mutual Fund) 
on the General Profile 
Record - Record Type 020 
62 62 1 A/N 1 – Retail MM  
2 –Institutional MM 
3 –Government MM 
R 0790 
Number of NAV Strikes 
Field must be populated with 
at least ‘01’ when the Money 
Market Fund Indicator 
equals ‘2’ (Institutional 
Money Market) . Values of 
02 through 10 should be 
populated when the number 
of NAV Strike Times are 
greater than ‘1’ 
 
Field must populated with 
“00’ when the Money Market 
Fund Indicator equals 
‘1’(Retail Money Market) or 
‘3’ (Government Money 
Market)  
63 64 2 N  R 0794 
NAV Strike Time 1 
Note: Field is required when 
the Money Market Fund 
Indicator = ‘2’ (Institutional 
Money Market) 
 
Field should be ‘Blank” when 
the Money Market Fund 
Indicator = “1” (Retail Money 
Market) or “3” (Government 
Money Market) 
65 70 6 A/N hhmmss O/C 0791 
Filler  71 78 8 A/N space R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test  
R 0089 
[[NSCC]] Reject Indicator 80 80 1 A/N Input: Space 
Output:  
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]] 
Multiple Errors  
  

---

## Page 56

Profile Security Database – Variable Length Record Layouts 
Money Market Fund Data (Record Type 033) 56 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[NSCC]] Reject Code  81 84 4 A/N Input: Space 
Output: Reject Code or space 
  
Share Class Name 85 104 20 A/N @ R 0526 
NAV Strike Time 2 105 110 6 A/N hhmmss OC 0791 
NAV Strike Time 3 111 116 6 A/N hhmmss OC 0791 
NAV Strike Time 4 117 122 6 A/N hhmmss OC 0791 
NAV Strike Time 5 123 128 6 A/N hhmmss OC 0791 
NAV Strike Time 6 129 134 6 A/N hhmmss OC 0791 
NAV Strike Time 7 135 140 6 A/N hhmmss OC 0791 
NAV Strike Time 8 141 146 6 A/N hhmmss OC 0791 
NAV Strike Time 9 147 152 6 A/N hhmmss OC 0791 
NAV Strike Time 10 153 158 6 A/N hhmmss OC 0791 
Fund Portfolio Name 159 218 60 A/N @ 
 
R 0527 
Filler 219 232 14 A/N  R  

---

## Page 57

Profile Security Database – Variable Length Record Layouts 
Appendix A: Valid Values for Investment Class Code 57 
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

---

## Page 58

Profile Security Database – Variable Length Record Layouts 
Appendix A: Valid Values for Investment Class Code 58 
23 = Short-Term Government Bond Fund 
24 = Mortgage-Backed Fund 
25 = Strategic Income Bond Fund 
26 = State Municipal Bond Fund 
27 = Short-Term State Municipal Bond Fund 
28 = National Municipal General Bond Fund 
29 = National Municipal Short-Term Bond Fund 
30 = Taxable Government Money Market Fund 
31 = Taxable Non-Government Money Market Fund 
32 = Tax-Exempt National Money Market Fund 
33 = Tax-Exempt State Money Market Fund 
 

---

## Page 59

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 59 
APPENDIX B – VALID VALUES FOR SOCIAL CODE 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
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
fund-prototype) 
Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 
09 Individual Retirement Account - Rollover 
(fund-prototype) 
Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 
N/A KEOGH  This social code was eliminated Nov. 18, 2013. See Important 
Notice a7665 (posted July 3, 2013). 
 
Best Practice: Map to either social code 34 or 50. 

---

## Page 60

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 60 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
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
19 403(b) Plan (non-prototype) Use for non-prototype 403(b) accounts maintained at the plan 
level omnibus level.  
 
Best Practice: Firm is responsible for tax reporting. 
20 457(b) Plan (non-prototype) Use for non-prototype 457(b) plans which are maintained in a plan 
level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting. 

---

## Page 61

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 61 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
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
30 Individual Retirement Account - Spousal 
(non-prototype) 
Use for accounts not registered under the fund’s custodial IRA 
plan.  
 
Best Practice: Firm is responsible for tax reporting. 
31 Simple IRA (fund-prototype) Use for accounts registered under the fund’s custodial IRA plan.  
 
Best Practice: Fund is responsible for tax reporting. 

---

## Page 62

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 62 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
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
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
41 Series E/Series I U.S. Saving [[Bonds]] 
transferred into Section 529 Plan  
Use for Series E/Series I U.S. Saving [[Bonds]] transferred into 
Section 529 Plan accounts which are maintained at the [[participant]] 
FBO account level. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
42 Bank/Trust FBO  Use when a Bank or Trust Company acts as custodian or trustee 
for an underlying shareholder (non-retirement). Accounts are 

---

## Page 63

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 63 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
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
49 Single K (fund-prototype) Use for fund-prototype Single K plan accounts 
(i.e., a defined contribution retirement plan with one [[participant]]). 
 
Best Practice: Fund is responsible for tax reporting, unless level 3 
or trust networked. 
50 Single K (non-prototype) Use for non-prototype Single K plan accounts 
(i.e., a defined contribution retirement plan with one [[participant]]). 
 
Best Practice: Firm is responsible for tax reporting. 
51 Non-Qualified Deferred Compensation 
Plan (non-prototype; [[participant]] directed) 
Use for non-prototype, non-qualified deferred compensation plans 
which are maintained in a plan level omnibus account. 
Participants direct investments in these accounts.  
 
Best Practice: Firm is responsible for tax reporting. 

---

## Page 64

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 64 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
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
61 Section 529 Plan - Joint Owner  Use for Section 529 education savings plan registered to joint 
owners. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 

---

## Page 65

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 65 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
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
65 Transfer On Death – Individual Use for a transfer on death account established for an individual 
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
68 Section 529 Plan – Corporate Use for accounts with a Corporation owning a 529 Plan. 
 
Best Practice: Fund is responsible for tax reporting unless level 3. 
69 457(b) Plans - FBO [[participant]] 
Name/Account # (fund-prototype) 
Use for fund-prototype 457(b) plans which are maintained in a 
[[participant]] FBO account. 
 
Best Practice: Fund is responsible for tax reporting. 
70 457(f) Plans (non-prototype) Use for non-prototype 457(f) plans which are maintained in a plan 
level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting. 
71 Non-Qualified Deferred Compensation 
Plan (non-prototype; not [[participant]] 
directed) 
Use for non-prototype, non-qualified deferred compensation plans 
which are maintained in a plan level omnibus account. 
Participants [[DO]] not direct investments in these accounts. 
 

---

## Page 66

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 66 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
Best Practice: Firm is responsible for tax reporting. 
72 Non-Qualified 403(b) Plans (non-
prototype 
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
81 Health Savings Account FBO [[participant]] 
Name/Account # 
(non-prototype) 
Use for non-prototype Health Saving Accounts (HSA's) maintained 
at the [[participant]] FBO level.  
 
Best Practice: Firm is responsible for tax reporting. 

---

## Page 67

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 67 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
82 Government Sponsored Plan 
(non-prototype) 
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
90 Simple 401(k) Plan (non-prototype) Use for non-prototype Simple 401(k) plans which are maintained 
in a plan level omnibus account.  
 
Best Practice: Firm is responsible for tax reporting.  

---

## Page 68

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 68 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
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
 
Best Practice: Firm is responsible for tax reporting). 
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
A0 Roth 403(b) Plans FBO [[participant]] 
Name/Account # (non-prototype) 
Use for non-prototype Roth 403(b) accounts which are maintained 
at the [[participant]] FBO account level. 
 
Best Practice: Firm is responsible for tax reporting. 

---

## Page 69

Profile Security Database – Variable Length Record Layouts 
Appendix B – Valid Values for Social Code 69 
Social 
Code 
[[NSCC]] Social Code Description Definition and Best Practice 
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

## Page 70

Profile Security Database – Variable Length Record Layouts 
Appendix C: Modifications to Social Code Field Edits 70 
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
• 0 = Eligible, No Restrictions 
• 1 = Eligible, Restrictions May Apply; and  
• 2 = Eligible at NAV, Restrictions May Apply 
 
If the Eligibility Code is 1 = Eligible Restrictions May Apply or 2 = Eligible at NAV, Restrictions May Apply, then 
the above-mentioned Social Code fields become conditionally optional for input.  
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
I. If the "Eligibility Code" field = "0 = Eligible, No Restrictions, or "1 = Eligible, Restrictions May Apply", then 
the "Relationship between [[participant]] Minimum and [[Asset]] Size" field must be left blank/ not allowed. If not 
blank, a reject message will appear on screen advising Number of Active Participants Minimum must be 
blank when Eligibility Code is equal to 0 or 1. 

---

## Page 71

Profile Security Database – Variable Length Record Layouts 
Appendix C: Modifications to Social Code Field Edits 71 
If the "Eligibility Code" field = " 2 = Eligible at NAV, Restrictions May Apply", then the "Relationship 
between [[participant]] Minimum and [[Asset]] Size" field is Required. 
II. If the "Relationship between [[participant]] Minimum and [[Asset]] Size" field has one of the following values of " 
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
III. Modified Edits for the following fields: 
• There will be no edit comparison (greater than/less than) between "Number of Eligible 
Participants Minimum" and "Number of Active Participants Minimum".  
• There will also be no edit comparison between "Minimum [[Asset]] Size for Eligibility" and 
"Maximum [[Asset]] Size for Eligibility" because the minimum and maximum [[Asset]] sizes are 
independent fields.  
• The "Maximum [[Asset]] Size for Eligibility" field is now always a Required numeric field.  If it is not 
applicable, then funds should follow the best practice for input to this field:  
• Best Practice: if the maximum [[Asset]] size for eligibility does not apply, a fund would input all 9s in 
this field.  
 
 

---

## Page 72

Profile Security Database – Variable Length Record Layouts 
APPENDIX D: SUMMARY OF CHANGES 72 
APPENDIX D: SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 
 
 
 
  

---

## Page 73

Profile Security Database – Variable Length Record Layouts 
Summary of Changes – Effective date March 28, 2022 73 
SUMMARY OF CHANGES – EFFECTIVE DATE MARCH 
28, 2022 
New Product Type Code – Interval Fund (48) 
Field Name Location Description Values Updated (Red) 
Product Type Code Record 020 Position 7-8 01 = Mutual Fund 
02 = Money Market Mutual Fund 
03 = [[UIT]] (Unit Investment Trust) 
04 = Closed-End Mutual Fund 
05 = GIC (Guaranteed Investment Contract) 
06 = Stable Value Fund 
07 = Separate Account 
08 = Bank Collective Trust 
09 = Offshore (NRA) Fund 
10 = BIC (Bank Investment Contract) 
11 = Section 529 College Savings Plan 
12 = Offshore U.S. Dollar Enhanced ( [[DO]] not use- 
domestic funds on Profile Security only)  
13 = Offshore Non-U.S. Dollar Enhanced ( [[DO]] not use – 
domestic funds on Profile Security only)  
14 = Annuity (with underlying [[Mutual Funds]]) 
15 = Section 529 Money Market Fund 
48 = Interval Fund 
 
Best Practice: When Product Type Code = 02 (Money 
Market Mutual Fund) or 15 (Section 529 Money Market 
Fund), Record Type 033 - ‘Money Market Fund Data’ 
should also be submitted 

---

## Page 74

Profile Security Database – Variable Length Record Layouts 
Summary of Changes – Effective date August 26, 2019 74 
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

## Page 75

Profile Security Database – Variable Length Record Layouts 
Summary of Changes – Effective date March 25, 2019 75 
SUMMARY OF CHANGES – EFFECTIVE DATE MARCH 
25, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
0388 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 76

Profile Security Database – Variable Length Record Layouts 
Summary of changes – Effective date July 13, 2018 76 
SUMMARY OF CHANGES – EFFECTIVE DATE JULY 13, 
2018 
Correction to Field Values Descriptions 
Field Name Location Description Values Updated (Red) 
[[Dividend]] Accrual Redemption T+1 
Stop Date Code 
Record 020 Position 220 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
[[Dividend]] Accrual Partial Exchange 
Out Stop Date Code  
Record 020 Position 221 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date - 1  
[[Dividend]] Accrual Partial Transfer 
Out Stop Date Code 
Record 020 Position 223 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date – 1 
[[Dividend]] Accrual ACAT Transfer Out 
Stop Date  
Record 020 Position 225 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date – 1 
DCC&S [[Dividend]] Accrual 
Redemption Stop Date Code 
Record 020 Position 229 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date – 1 
DCC&S [[Dividend]] Accrual 
Redemption “G” indicator (Share 
Class Conversion) Stop Date Code 
Record 020 Position 230 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date – 1 
DCC&S [[Dividend]] Accrual 
Redemption “L” indicator (Omnibus 
[[Dividend]] Reconciliation) Stop Date 
Code 
Record 020 Position 231 0 = [[settlement]] Date -1 
1 = [[settlement]] Date  
2 = Trade Date 
3 = Trade Date – 1 

---

## Page 77

Profile Security Database – Variable Length Record Layouts 
Summary of changes – Effective date July 9, 2018 77 
SUMMARY OF CHANGES – EFFECTIVE DATE JULY 9, 
2018 
New Fields Added 
New Field Name Location Description 
Eligible for Externalized Commission Record 020 Position 301 A new required field to indicate share 
classes eligible for Externalized 
Commission. 
Large Trade Notification 
AND 
Large Trade Dollar Threshold Amount 
Record 020 Position 302 
 
Record 020 Position 489-504 
New required fields to indicate if a Firm 
should notify the Fund when a large 
trade dollar amount threshold is met for 
a security. 
DCC&S Eligible 
AND  
Defined Contribution Clearance and 
[[settlement]] (DCC&S) Cut –off Cycle 
Record 020 Position 72 
 
Record 020 Position 73-76 
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
Record 020 Position 219-231 New optional/conditional fields to 
provide additional accrual methodology 
details (start/stop dates) for a security. 
Existing Fields Modified 
Existing Field Name Location Description 
CDSC Rules Apply Record 020 Position 369 New data point value for this existing field to 
indicate when CDSC applies for Finder’s 
Fee/Jumbo Purchase Only. This will 
eliminate confusion as to how to populate 
and interpret CDSC and commission data 
where advanced commission and CDSC 
rules only apply in certain situations (i.e. for 
$1 million + Jumbo purchases). 
ROA Aggregation Inclusion Record 020 Position 528 This existing field was renamed to “ROA/LOI 
Aggregation Inclusion”. Updates to existing 
values and the addition of new values were 
added to differentiate between ROA 
aggregation rules vs. LOI aggregation rules. 

---

## Page 78

Profile Security Database – Variable Length Record Layouts 
Summary of changes – Effective date July 9, 2018 78 
Existing Field Name Location Description 
[[Dividend]] and DCC&S Accrual 
Start/Stop fields 
Record 020 Position 373-377 
Record 020 Position 464-465 
Rename existing fields to provide additional 
accrual methodology details (start/stop 
dates) for a security. 
Exchange Buy Eligibility Record 020 Position 404 New data point value to identify when 
restrictions apply to exchange buy 
purchases. Only Purchases Eligibility had 
this [[Option]]. By adding this value to Exchange 
Buy Eligibility, these two data points will have 
the same value options. 
Social Codes  Addition of new Social Codes. Addition of 
new Social Codes. The new social codes 
necessitates leveraging alpha/numeric 
values. [[NSCC]] record layouts currently 
support alpha/numeric values for the Social 
Code field; clients should review their 
systems to ensure they are able to support 
alpha/numeric social code values. 

---

## Page 79

Profile Security Database – Variable Length Record Layouts 
Summary of changes – Effective date August 22, 2016 79 
SUMMARY OF CHANGES – EFFECTIVE DATE AUGUST 
22, 2016 
 
Modified Field Name Location Description 
Product Type Code Record Type 020 (General Profile) 
Bytes 381-382 
Additional Product Type added: 
 
15 = Section 529 Money Market Funds 
For new Security Issue [[ID]] Adds, when Product Type 
Code = 02 Money Market Mutual Fund or Product 
Type Code = 15 Section 529 Money Market Funds, 
then Record Type 033, Money Market Fund Data 
should also be submitted 

---

## Page 80

Profile Security Database – Variable Length Record Layouts 
Summary of changes – Effective date May 31, 2016 80 
SUMMARY OF CHANGES – EFFECTIVE DATE MAY 31, 
2016 
Modified Field Name Location Description 
Product Type Code Record Type 020 (General Profile) 
Bytes 381-382 
Additional Product Type added: 
 
15 = Section 529 Money Market Funds 
For new Security Issue [[ID]] Adds, when 
Product Type Code = 02 Money Market 
Mutual Fund or Product Type Code = 15 
Section 529 Money Market Funds, then 
Record Type 033, Money Market Fund Data 
should also be submitted 

---

## Page 81

Profile Security Database – Variable Length Record Layouts 
New Record Type Added 81 
NEW RECORD TYPE ADDED 
New Record Number Name of Record  
RECORD TYPE 033 Money Market Fund Data 

---

## Page 82

Profile Security Database – Variable Length Record Layouts 
Summary of changes – Effective date May 20, 2013 82 
SUMMARY OF CHANGES – EFFECTIVE DATE MAY 20, 
2013 
New Record Type Added 
New Record Number Name of Record  
RECORD TYPE 032 408(b) (2) Specific Data 
 
 
 

---

## Page 83

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 20, 2023 
Publication Code: MFS276 
Service: Mutual Fund Profile Service II 
Title: Profile Security Database – Variable Length Record Layouts  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 