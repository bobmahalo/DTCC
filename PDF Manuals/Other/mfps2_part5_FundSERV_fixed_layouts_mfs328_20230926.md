---
title: "MFPS II - Fund/SERV Fixed Length Record Layouts – Part 5"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part5_FundSERV_fixed_layouts_mfs328_20230926.pdf"
pages: 11
size: "277.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II - Fund/SERV Fixed Length Record Layouts – Part 5

**Original File:** [mfps2_part5_FundSERV_fixed_layouts_mfs328_20230926.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part5_FundSERV_fixed_layouts_mfs328_20230926.pdf)  
**Category:** Other  
**Total Pages:** 11  
**File Size:** 277.6 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
FUND/SERV FIXED LENGTH RECORD LAYOUTS – 
PART 5 
 
SEPTEMBER 26, 2023 
 

---

## Page 2

Fund/SERV Fixed Length Record Layouts – Part 5 
Fund/SERV Security Master Data (027) 2 
TABLE OF CONTENTS 
Fund/SERV Security Master Data (027) ............................................................................................................. 4 
02.21.01 Fund/SERV Security Master Data (027) Record 1 of 10 ..................................................................... 4 
02.21.02 Fund/SERV Security Master Data (027) Record 2 of 10 ..................................................................... 5 
02.21.03 Fund/SERV Security Master Data (027) Record 3 of 10 ..................................................................... 7 
02.21.04 Fund/SERV Security Master Data (027) Record 4 of 10 ..................................................................... 8 
02.21.05 Fund/SERV Security Master Data (027) ............................................................................................10 
Records 5 Thru 10 ...........................................................................................................................................10 
 

---

## Page 3

Fund/SERV Fixed Length Record Layouts – Part 5 
Fund/SERV Security Master Data (027) 3 
HISTORY OF CHANGES/IMPORTANT NOTICES 
Dates Description 
September 26, 2023 Record was rebranded and reviewed.  
Effective Date: May 1, 2023 MFPSII [[participant]] Profile database was decommissioned. Records 
013 (Fund/SERV [[participant]] Master Data) and 014 (MFPS 
Fund/SERV [[participant]] Retirement Data) were removed in 
accordance with these changes.  
Please see Important Notice a9279 P&S 8852 
Dated March 21, 2023 
July 8, 2022 Record was rebranded and reviewed. 
Effective Date: March 25, 2019 Please see Important Notice: a8658 p&s 8233 
Dated December 19, 2018 
Effective Date: March 27, 2006 Please see Important Notice: a6171 p&s 5741  
Dated December 21, 2005 
Effective Date: November 14, 2005 Please see Important Notice: a6084 p&s 5654  
Dated August 10, 2005 
Effective Date: August 29, 2005 Please see Important Notice a6062 p&s 5632  
Dated July 6, 2005 
 
  

---

## Page 4

Fund/SERV Fixed Length Record Layouts – Part 5 
Fund/SERV Security Master Data (027) 4 
FUND/SERV SECURITY MASTER DATA (027)  
02.21.01 Fund/SERV Security Master Data (027) Record 1 of 10  
(Output from [[NSCC]]. Information extracted from Fund/SERV Security Master file)  
Record 1 of 10 
Field Name 
Start End Len Type Description 
Physical Sequence Number  1 2 2 A/N  
Logical Sequence Number  3 4 2 A/N 01  
Filler  5 6 2 A/N Space  
Originator Type Indicator  7 7 1 A/N N = [[NSCC]]  
Profile Type  8 9 2 A/N 05 = Security Issue  
Record Type  10 12 3 A/N 027 = Fund/SERV Security Master Information  
Action Type  13 13 1 A/N A = add  
C = change  
D = delete  
Security Fund Number  14 17 4 A/N  
Filler  18 18 1 A/N Space  
Recipient Number  19 22 4 A/N Space = All recipients 
Filler  23 28 6 A/N Space  
Submission Date  29 36 8 A/N ccyymmdd  
Filler  37 44 8 A/N Space  
Security Issue Country 
Code  
45 46 2 A/N  
Security Issue [[ID]]  47 55 9 A/N  
ISIN Security Issue Check 
Digit  
56 56 1 A/N  
Offering First Trade Date  57 64 8 A/N ccyymmdd  
Offering Last Trade Date  65 72 8 A/N ccyymmdd  
Filler  73 80 8 A/N Space  
  

---

## Page 5

Fund/SERV Fixed Length Record Layouts – Part 5 
Fund/SERV Security Master Data (027) 5 
02.21.02 Fund/SERV Security Master Data (027) Record 2 of 10  
Record 2 of 10 
Field Name 
Start End Len Type Description 
Physical Sequence Number  1 2 2 A/N  
Logical Sequence Number  3 4 2 A/N 02  
Filler  5 6 2 A/N Space  
Security Type  7 8 2 A/N See Fund/SERV® Security Type Identifiers  
Registration Indicator  9 9 1 A/N 0 = Input Date  
1 = [[settlement]] Date  
[[underwriter]]/Tender 
Indicator  
10 10 1 A/N T = Tender  
U = [[Underwriting]]  
Space = N/A  
Alternate [[settlement]] 
Indicator  
11 11 1 A/N 0 = No  
1 = Yes  
Currency Code  12 14 3 A/N USD = Same day $ [[settlement]]  
USN = Next day $ [[settlement]]  
Alternate [[settlement]] 
Currency Code  
15 17 3 A/N USD = Same day $ [[settlement]]  
USN = Next day $ [[settlement]]  
Alternate [[settlement]] Cycle  18 20 3 N Number of Days 
Exchange [[settlement]] Cycle  21 23 3 N Number of Days  
Money Market Cutoff 
Purchase Time  
24 27 4 A/N hhmm  
Money Market Cutoff 
[[liquidation]] Time  
28 31 4 A/N hhmm  
Alternate [[transfer agent]] 
Indicator  
32 32 1 A/N 0 = No  
1 = Yes  
As Of Process Range  33 35 3 N Number of calendar days  
Order [[settlement]] Cycle  36 38 3 N Number of business days  
As Of [[settlement]] Cycle  39 41 3 N Number of business days  
Cash Adjustment 
[[settlement]] Cycle  
42 44 3 N Number of business days  
Alternate Exchange Fund 
Number  
45 48 4 A/N  

---

## Page 6

Fund/SERV Fixed Length Record Layouts – Part 5 
Fund/SERV Security Master Data (027) 6 
Record 2 of 10 
Field Name 
Start End Len Type Description 
Effective Start Date  49 56 8 A/N ccyymmdd  
Effective End Date  57 64 8 A/N ccyymmdd  
Firm Exit Indicator  65 65 1 A/N 0 = Not allowed  
1 = Allowed  
Cash Adjustment Indicator  66 66 1 A/N 0 = Not allowed  
1 = Allowed  
Exchanges Indicator  67 67 1 A/N 0 = Not allowed  
1 = Allowed  
Filler  68 80 13 A/N Space  
  

---

## Page 7

Fund/SERV Fixed Length Record Layouts – Part 5 
Fund/SERV Security Master Data (027) 7 
02.21.03 Fund/SERV Security Master Data (027) Record 3 of 10  
Record 3 of 10 
Field Name 
Start End Len Type Description 
Physical Sequence Number  1 2 2 A/N  
Logical Sequence Number  3 4 2 A/N 03  
Filler  5 6 2 A/N Space  
Filler  7 12 6 A/N Space  
Offering [[settlement]] Date  13 20 8 A/N ccyymmdd  
Security Description  21 80 60 A/N  
  

---

## Page 8

Fund/SERV Fixed Length Record Layouts – Part 5 
Fund/SERV Security Master Data (027) 8 
02.21.04 Fund/SERV Security Master Data (027) Record 4 of 10  
Record 4 of 10 
Field Name 
Start End Len Type Description 
Physical Sequence Number  1 2 2 A/N  
Logical Sequence Number  3 4 2 A/N 04  
Filler  5 6 2 A/N Space  
Alternate Order [[settlement]] 
Cycle Firm 1  
7 10 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 2  
11 14 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 3  
15 18 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 4  
19 22 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 5  
23 26 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 6  
27 30 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 7  
31 34 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 8  
35 38 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 9  
39 42 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 10  
43 46 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 11  
47 50 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 12  
51 54 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 13  
55 58 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 14  
59 62 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 15  
63 66 4 A/N  

---

## Page 9

Fund/SERV Fixed Length Record Layouts – Part 5 
Fund/SERV Security Master Data (027) 9 
Record 4 of 10 
Field Name 
Start End Len Type Description 
Alternate Order [[settlement]] 
Cycle Firm 16  
67 70 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 17  
71 74 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 18  
75 78 4 A/N  
Filler  79 80 2 A/N Space  
 
 
  

---

## Page 10

Fund/SERV Fixed Length Record Layouts – Part 5 
Fund/SERV Security Master Data (027) 10 
02.21.05 Fund/SERV Security Master Data (027)  
Records 5 Thru 10  
Alternate Order [[settlement]] Cycle Firm information may continue in logical records 5 through 10 up to total list 
of 112 firms.  
The record format is the same as logical record 4 in the previous section. 
 

---

## Page 11

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 26, 2023 
Publication Code: MFS328 
Service: Mutual Fund Profile Service II 
Title: Fund/SERV Fixed Length Record Layouts – Part 5 
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 