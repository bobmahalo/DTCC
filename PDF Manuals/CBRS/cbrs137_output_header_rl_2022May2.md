---
title: "CBRS Application Output Header and Trailer Record Layout"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs137_output_header_rl_2022May2.pdf"
pages: 2
size: "161.8 KB"
category: "CBRS"
ingested_on: "2026-06-05"
---

# CBRS Application Output Header and Trailer Record Layout

**Original File:** [cbrs137_output_header_rl_2022May2.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cbrs137_output_header_rl_2022May2.pdf)  
**Category:** CBRS  
**Total Pages:** 2  
**File Size:** 161.8 KB  

---

## Page 1

 
 
COST BASIS REPORTING SERVICE (CBRS) 
CBRS APPLICATION OUTPUT HEADER AND TRAILER RECORD 
REVISION DATE: NOVEMBER 26, 2010 
CBRS Application Output Header 
The following table shows the CBRS application output header: 
Field Name Length Start End Type Comments 
Record Type 1 1 1 A/N H 
Record Length 4 2 5 A/N 61 – Variable Length 
AutoRoute Product [[ID]] 8 6 13 A/N 02400264 
File Description 30 14 43 A/N Cost Basis Transaction MRO 
Distribution Side 4 44 47 A/N Last four digits of the distribution firm’s CBRS 
Account [[ID]] number 
Processing Date 8 48 55 A/N CCYYMMDD 
Multi-Cycle Indicator 1 56 56 A/N Single Cycle = Space 
Multi-Cycle Nbr. 4 57 60 A/N Zeroes 
Variable-Length Record Indicator 1 61 61 A/N Variable Length = * 
Future Use 19 62 80 A/N Spaces 
END OF RECORD 
CBRS Application Output Trailer 
The following table shows the CBRS application output trailer: 
Field Name Length Start End Type Comments 
Record Type 1 1 1 A/N T 
Record Length 4 2 5 A/N 70 – Variable Length 
AutoRoute Product [[ID]] 8 6 13 A/N 02400264 
File Description 30 14 43 A/N Cost Basis Transaction MRO 
Distribution Side 4 44 47 A/N Last four digits of the distribution firm’s CBRS 
Account [[ID]] number 
Processing Date 8 48 55 A/N CCYYMMDD 
Multi-Cycle Indicator 1 56 56 A/N Single Cycle = Space 
Multi-Cycle Nbr. 4 57 60 A/N Zeroes 
Variable-Length Record Indicator 1 61 61 A/N Variable Length = * 
Item Count 9 62 70 A/N Transmission count (includes Header and Trailer) 
END OF RECORD 
 

---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: May 2, 2022 
Publication Code: CBRS137 
Service: Cost Basis Reporting Service (CBRS) 
Title: CBRS Application Output Header and Trailer Record Layout 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 