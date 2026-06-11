---
title: "MFPS II - Fund/SERV Data Variable Length Record Layouts – Part 5"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part5_FundSERV_variable_layouts_mfs330_20230926.pdf"
pages: 9
size: "347.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II - Fund/SERV Data Variable Length Record Layouts – Part 5

**Original File:** [mfps2_part5_FundSERV_variable_layouts_mfs330_20230926.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part5_FundSERV_variable_layouts_mfs330_20230926.pdf)  
**Category:** Other  
**Total Pages:** 9  
**File Size:** 347.6 KB  

---

## Page 1

 
 
Mutual Fund Profile Service II 
FUND/SERV DATA VARIABLE LENGTH RECORD 
LAYOUTS – PART 5 
SEPTEMBER 26, 2023 
 
 
 
 
 
 
 
 
 
 

---

## Page 2

FUND/SERV Data Variable Length Record Layouts – Part 5 
HISTORY OF CHANGES/IMPORTANT NOTICES 2 
TABLE OF CONTENTS 
HISTORY OF CHANGES/IMPORTANT NOTICES ............................................................................... 3 
02.21 FUND/SERV SECURITY MASTER DATA (027) ........................................................................ 4 
Output from [[NSCC]] .......................................................................................................................... 4 
 
 

---

## Page 3

FUND/SERV Data Variable Length Record Layouts – Part 5 
HISTORY OF CHANGES/IMPORTANT NOTICES 3 
HISTORY OF CHANGES/IMPORTANT NOTICES 
Dates Description 
September 26, 2023  Record was rebranded and reviewed.  
Effective Date: May 1, 2023 MFPSII [[participant]] Profile database was decommissioned. Records 
013 (Fund/SERV [[participant]]  Master Data) and 014 (MFPS 
Fund/SERV [[participant]] Retirement Data) were removed in 
accordance with these changes. 
Please See Important Notice a9279 P&S 8852 
Dated March 21, 2023 
July 8, 2022 Record was rebranded and reviewed. 
Effective Date: March 25, 2019 Please see Important Notice: a8658 P&S 8233 
Dated December 19, 2018 
Effective Date: March 27, 2006 Please see Important  Notice: a6171 P&S 5741 
Dated December 21, 2005 
Effective Date: November 14, 2005 Please see Important  Notice: a6084 P&S 5654 
Dated August 10, 2005 
Effective Date: August 29, 2005 Please see Important  Notice a6062 P&S 5632 
Dated July 6, 2005 

---

## Page 4

FUND/SERV Data Variable Length Record Layouts – Part 5 
02.21 FUND/SERV SECURITY MASTER DATA (027) 4 
02.21 FUND/SERV SECURITY MASTER DATA (027) 
Output from [[NSCC]] 
(Information extracted from Fund/SERV Security Master  file) 
02.21 Fund/SERV Security Master Data (027) 
 
Field Name Start End Len Type Description 
Record Length 1 4 4 N 0232, 0306, 0380, …., 0750 
Physical Sequence 
Number 
5 6 2 A/N  
Logical Sequence Number 7 8 2 A/N 01 
Filler 9 10 2 A/N Space 
Originator Type Indicator 11 11 1 A/N N = [[NSCC]] 
Profile Type 12 13 2 A/N 05 = Security Issue 
Record Type 14 16 3 A/N 027 = Fund/SERV  Security Master 
Information 
Action Type 17 17 1 A/N A = add 
C = change 
D = delete 
Security Fund Number 18 21 4 A/N  
Filler 22 22 1 A/N Space 
Recipient Number 23 26 4 A/N Space = All recipients 
Filler 27 32 6 A/N Space 
Submission  Date 33 40 8 A/N ccyymmdd 
Filler 41 48 8 A/N Space 
Security Issue Country 
Code 
49 50 2 A/N  

---

## Page 5

FUND/SERV Data Variable Length Record Layouts – Part 5 
02.21 FUND/SERV SECURITY MASTER DATA (027) 5 
Field Name Start End Len Type Description 
Security Issue [[ID]] 51 59 9 A/N  
ISIN Security  Issue Check 
Digit 
60 60 1 A/N  
Offering First Trade Date 61 68 8 A/N ccyymmdd 
Offering Last Trade Date 69 76 8 A/N ccyymmdd 
Filler 77 84 8 A/N Space 
Security Type 85 86 2 A/N See Fund/SERV® Security Type Identifiers 
Registration Indicator 87 87 1 A/N 0 = Input Date 
1 = [[settlement]] Date 
[[underwriter]]/Tender 
Indicator 
88 88 1 A/N T = Tender 
U =  [[Underwriting]] 
Space = N/A 
Alternate [[settlement]] 
Indicator 
89 89 1 A/N 0 = No 
1 = Yes 
Currency Code 90 92 3 A/N USD = Same  day $ [[settlement]] 
USN = Next day $ [[settlement]] 
Alternate [[settlement]] 
Currency Code 
93 95 3 A/N USD = Same  day $ [[settlement]] 
USN = Next day $ [[settlement]] 
Alternate [[settlement]] Cycle 96 98 3 N Number of Days 
Exchange [[settlement]] 
Cycle 
99 101 3 N Number of Days 
Money Market Cutoff 
Purchase Time 
102 105 4 A/N hhmm 
Money Market Cutoff 
[[liquidation]] Time 
106 109 4 A/N hhmm 
Alternate [[transfer agent]] 
Indicator 
110 110 1 A/N 0 = No 
1 = Yes 

---

## Page 6

FUND/SERV Data Variable Length Record Layouts – Part 5 
02.21 FUND/SERV SECURITY MASTER DATA (027) 6 
Field Name Start End Len Type Description 
As Of Process Range 111 113 3 N Number of calendar days 
Order [[settlement]] Cycle 114 116 3 N Number of business days 
As Of [[settlement]] Cycle 117 119 3 N Number of business days 
Cash Adjustment 
[[settlement]] Cycle 
120 122 3 N Number of business days 
Alternate Exchange Fund 
Number 
123 126 4 A/N  
Effective Start Date 127 134 8 A/N ccyymmdd 
Effective End Date 135 142 8 A/N ccyymmdd 
Firm Exit Indicator 143 143 1 A/N 0 = Not allowed 
1 = Allowed 
Cash Adjustment Indicator 144 144 1 A/N 0 = Not allowed 
1 = Allowed 
Exchanges Indicator 145 145 1 A/N 0 = Not allowed 
1 = Allowed 
Filler 146 164 19 A/N Space 
Offering [[settlement]] Date 165 172 8 A/N ccyymmdd 
Security Description 173 232 60 A/N 
 
Start of Alternate [[settlement]] Firm section 
Alternate Order [[settlement]] 
Cycle Firm 1 
233 236 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 2 
237 240 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 3 
241 244 4 A/N  

---

## Page 7

FUND/SERV Data Variable Length Record Layouts – Part 5 
02.21 FUND/SERV SECURITY MASTER DATA (027) 7 
Field Name Start End Len Type Description 
Alternate Order [[settlement]] 
Cycle Firm 4 
245 248 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 5 
249 252 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 6 
253 256 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 7 
257 260 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 8 
261 264 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 9 
265 268 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 10 
269 272 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 11 
273 276 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 12 
277 280 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 13 
281 284 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 14 
285 288 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 15 
289 292 4 A/N  
Alternate Order [[settlement]] 
Cycle Firm 16 
293 296 4 A/N 
 
Alternate Order [[settlement]] 
Cycle Firm 17 
297 300 4 A/N 
 
  

---

## Page 8

FUND/SERV Data Variable Length Record Layouts – Part 5 
02.21 FUND/SERV SECURITY MASTER DATA (027) 8 
Field Name Start End Len Type Description 
Alternate Order [[settlement]] 
Cycle Firm 18 
301 304 4 A/N  
Filler 305 306 2 A/N 
 
Alternate [[settlement]] Firm may repeat up to 112 times (7 occurrences) 

---

## Page 9

 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The Depository 
Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing 
Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal entity, subject to 
the laws and regulations of the particular country or countries in which such entity operates. Please see www.[[DTCC]].com for more 
information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: September 26, 2023 
Publication Code: MFS330 
Service: Mutual Fund Profile Service II 
Title: Fund/SERV Data Variable Length Record Layouts – Part 5 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 