---
title: "GSD Clearing Fund Summary MRO"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd217_clf_summ_mro_20231206.pdf"
pages: 8
size: "297.4 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD Clearing Fund Summary MRO

**Original File:** [gsd217_clf_summ_mro_20231206.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd217_clf_summ_mro_20231206.pdf)  
**Category:** GSD  
**Total Pages:** 8  
**File Size:** 297.4 KB  

---

## Page 1

 
[[FICC]] – [[GSD]] 
[[GSD]] CLEARING FUND SUMMARY: MRO FORMAT 
VERSION 2.4 
EFFECTIVE DATE: JANUARY 22, 2024 
 

---

## Page 2

 
 
TABLE OF CONTENTS 
Clearing Fund Summary MRO Information ....................................................................................................... 3 
Application Header Record ................................................................................................................................. 3 
Application Trailer Record .................................................................................................................................. 3 
Example ............................................................................................................................................................. 4 
Data Record ........................................................................................................................................................ 4 
 

---

## Page 3

[[GSD]] Clearing Fund Summary: MRO Format 
Clearing Fund Summary MRO Information 3 
CLEARING FUND SUMMARY MRO INFORMATION 
Product No. Product Name 
08982383 Test - [[GSD]] Clearing Fund Summary MRO 
08182383 Prod - [[GSD]] Clearing Fund Summary MRO 
. 
Application Header Record 
Field Name Length Start End Type Comments 
Character Set 1 1 1 A/N “A” = ASCII, “E” = EBCDIC 
Block Size 5 2 6 N ‘00960’; varies by record type 
Source Name 4 7 10 A/N “CFM” 
Filler 8 11 18 A/N Always = spaces 
Destination Name 5 19 23 A/N [[GSD]] Deposit [[ID]] 
Filler 8 24 31 A/N Always = “_CF     “ 
Date/Time 22 32 53 A/N System-generated timestamp 
DD-MMM-YYYY HH:MM:SS.H 
19-JAN-1989 10:45:15.2 
Filler 907 54 960 A/N Always = spaces 
 
Application Trailer Record 
Field Name Length Start End Type Comments 
Trailer [[ID]] 5 1 5 A/N Always = “TRAIL” 
Number of Records 5 6 10 N Total number of records in file 
Checksum 5 11 15 N XOR of checksums of all data records (for 
future use). Always blank for now. 
Filler 945 16 960 A/N Deposit [[ID]] followed by Business Date and 
remaining filled with spaces.  
 
  

---

## Page 4

[[GSD]] Clearing Fund Summary: MRO Format 
Clearing Fund Summary MRO Information 4 
Example 
00001234  E00960CFM      01234_NET    05-MAY-2015 12:26:48.0                                                          
00001234  0000100960      39901234XXXXXXXXXXXXXX./ HF      05/05/2015NET XXXXXXXXXXXXXX.                
STARTOFDAY000           000           000           000           000           000           000           000           000           
000           000           000           000           000………… 
00001234  TRAIL00001     123405-MAY-2015                                                                               
Note: 
The first 10 characters (8 for [[participant]] and 2 blank spaces) for each record are for CDTS processing only. CDTS will 
remove the first 10 characters before sending it to the participants. 
Data Record 
Field Name Length Start End Type Comments 
Record Number ** 5 1 5 N Sequential number of the logical record 
starting with “00001”. 
Physical record length ** 5 6 10 N Not greater than 960 
Checksum ** 5 11 15 N The CRC16 of the physical record (reserved 
for future use). Always blank for now. 
Segment Location ** 1 16 16 N Where this physical record is located in the 
logical record: 
• 3 = only record 
• 1 = first record 
• 2 = last record 
• 0 = middle record 
Record [[ID]] 2 17 18 N Record type: always 99 
Deposit [[ID]] 15 19 33 A/N [[GSD]] Deposit [[participant]] Number 
Deposit Name 80 34 113 A/N [[GSD]] Deposit [[participant]] Name 
Business Date 10 114 123 A/N Business Date associated with CF 
Requirement Date 10 124 133 A/N  
[[Margin]] Type 6 134 139 A/N Ex: NET or NOTNET 
Legal Entity Name 80 140 219 A/N  
Cycle 15 220 234 A/N Ex: SOD, INTRADAY, ADHOC 
Total Required Fund Deposit 14 235 248 N  
Total Clearing Funds on 
Deposit (at [[collateral]] Value) 
14 249 262 N  
Excess/Deficit 14 263 276 N  

---

## Page 5

[[GSD]] Clearing Fund Summary: MRO Format 
Clearing Fund Summary MRO Information 5 
Field Name Length Start End Type Comments 
Minimum Cash Requirement 14 277 290 N  
Cash on Deposit 14 291 304 N  
Cash Excess/Deficit 14 305 318 N  
Minimum Cash + Treasuries 
Value Requirement 
14 319 332 N  
Cash + Treasuries Value on 
Deposit 
14 333 346 N  
Cash + Treasuries Deficit 14 347 360 N  
Excess Capital Ratio (ECR) 14 361 374 N Excess Capital Ratio. ECR will be populated 
if the value is greater than or equal to 0.5, 
otherwise “N/A”. 
[[FICC]] VaR 14 375 388 N  
Coverage Component (CC) 14 389 402 N  
CME Cross [[Margin]] Eligible 
VaR 
14 403 416 N  
[[mark-to-market]] (MTM)  14 417 430 N  
Cash Obligation Items (COI)  14 431 444 N  
Principal & Interest Related 
Charges (PIRC)  
14 445 458 N  
Blackout Period Exposure 
(BPE)  
14 459 472 N Blackout Period Exposure (BPE) 
Portfolio Differential 14 473 486 N  
Confidence Level Charge 14 487 500 N  
Implied Volatility Charge 14 501 514 N  
Membership Type Minimum 
Adjustment 
14 515 528 N  
TURFD 14 529 542 N  
Minimum Deposit Special 
Charge 
14 543 556 N  
Excess Capital [[Premium]]  14 557 570 N (i.e., ‘HIGH-LEVERAGE [[Premium]]’) 
[[Margin]] [[Liquidity]] Adjustment 
(MLA) 
14 571 584 N  
Watch List Adjustment 14 585 598 N  
Legal Risk Surcharge 14 599 612 N  

---

## Page 6

[[GSD]] Clearing Fund Summary: MRO Format 
Clearing Fund Summary MRO Information 6 
Field Name Length Start End Type Comments 
GCF [[Premium]] Charge  14 613 626 N  
GCF Repo Event Charge  14 627 640 N  
Special Charges 14 641 654 N  
IMTM 14 655 668 N  
Intraday Supplemental Fund 
Deposit 
14 669 682 N  
Blackout Period Exposure 
Backtesting Charge 
14 683 696 N  
[[Margin]] [[Proxy]] 14 697 710 N  
Special Charge Due to 
Position Change Backtest 
Deficiencies 
14 711 724 N  
Special Charge Due to 
Adequate Assurances 
14 725 738 N  
Special Charge Due to 
Backtest Deficiencies 
14 739 752 N  
Regular Backtesting Charge 14 753 766 N  
Intraday Backtesting Charge 14 767 780 N  
GCF EUI Special Charge 14 781 794 N  
Sum Charges 14 795 808 N  
Failing Below Minimum 
Financial Requirements 14 809 822 N  
Failure to Provide a 
Confirmation of an OFAC 
Program Letter 
14 
823 836 N  
Failure to Submit Required 
Financial, Regulatory and 
Other Information, including 
Required Notifications 
14 
837 850 N  
Failure to Timely Submit 
Annual Non-Domestic Legal 
Opinions or Outside Counsel 
Letter 
14 
851 864 N  
Prohibition of Pre-Netting: 
Failure to Identify Non-
[[Member]] Covered Affiliates 
and Fulfill Trade Submission 
Requirements 
14 865 878 N  

---

## Page 7

[[GSD]] Clearing Fund Summary: MRO Format 
Clearing Fund Summary MRO Information 7 
Field Name Length Start End Type Comments 
Prohibition of Pre-Netting: 
Failure to Identify Non-
[[Member]] Foreign Affiliates 
and Fulfill Trade Reporting 
Requirements 
14 879 892 N  
Sponsoring [[Member]] – 
Failure to Comply with the 
Minimum Financial 
Standards Set Forth for 
Sponsoring Members 
14 893 906 N  
Sum [[collateral]] [[Premium]] 14 907 920 N  
Filler 39 921 959 A/N Always = spaces 
Confirmation Continued 1 960 960 A/N " " = only record (no overflow record) 
      
** STANDARD 16 BYTES 
 

---

## Page 8

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
The [[GSD]] Clearing Fund Summary MRO (hereinafter, the "document") is provided as a convenience to Members and is for 
information purposes only. Although [[FICC]] may make this document available to Members, it shall be under no obligation to 
[[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing obligation to make available this document or other 
related information of a certain type.  
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to Members in this document, which is provided as-is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
Further, the information contained in this document is subject to change. Members and other authorized users of the 
document will find the most current version of the document on [[DTCC]]’s Learning Center site, 
www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow 
[[FICC]]’s most current document. 
 
Doc Date: December 6, 2023 (effective January 22, 2024) 
Publication Code: GSD217 
Service: [[FICC]] – [[GSD]]   
Title: [[GSD]] Clearing Fund Summary: MRO Format 
 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 