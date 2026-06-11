---
title: "DTCC Limit Monitoring Position Input Specifications "
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/lm115_position_input_spec_2022Jun27.pdf"
pages: 2
size: "139.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# DTCC Limit Monitoring Position Input Specifications 

**Original File:** [lm115_position_input_spec_2022Jun27.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/lm115_position_input_spec_2022Jun27.pdf)  
**Category:** Other  
**Total Pages:** 2  
**File Size:** 139.6 KB  

---

## Page 1

 
 
INPUT SPECIFICATIONS 
[[DTCC]] LIMIT MONITORING 
Position Input Specifications 
JULY 5, 2016 
This document explains the Position Input file that provides clearing members with the ability to submit 
positions. 
Note: 
All fields are required, except the Submitting Firm [[ID]] field that you must populate when the submitting market [[ID]] is 060 
([[OTC]]) and UTC Account [[ID]]. 
[[DTCC]] Limit Monitoring - PTM Positions Input File 
CDTS Product [[ID]]: 21878 
Detail Record 
Field Name Length Type Comments 
Process Date 8 A/N Format = CCYYMMDD 
Buy/Sell Indicator 1 A/N Values:  
• B 
• S 
Clearing [[Broker]] [[ID]] 8 A/N Format will be 99999999. 
Executing [[Broker]] [[ID]] 8 A/N Format will be 99999999. Required. Must be populated. 
Submitting Market [[ID]] 3 A/N Format is 999. 
Required. Must be populated. 
Submitting Firm [[ID]] 8 A/N Must be present only if Submitting Market [[ID]] = 060. 
Otherwise, populate with spaces. The format is 99999999. 
UTC Account [[ID]] 32 A/N Optional. 
Security ISIN 12 A/N 9 or 12 characters. When 9 – start from first byte 
Trade Quantity 15 NUM Format will be 999999999999999 
Contract Amount 17 NUM Format will be 99999999999999999 with an assumed 
decimal point before the last two numbers. 
Action Code 4 A/N Action Code Values: 
• INCR  
• DECR  
• DELT 
Filler 102 A/N Value = Spaces 
 
 

---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: June 27, 2022 
Publication Code: LM115 
Service: [[DTCC]] Limit Monitoring 
Title: Position Input Specifications 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
