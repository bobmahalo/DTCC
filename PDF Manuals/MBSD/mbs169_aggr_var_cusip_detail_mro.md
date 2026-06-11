---
title: "MBSD Aggregate VaR CUSIP Detail Report (FYICusipDtl) MRO"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs169_aggr_var_cusip_detail_mro.pdf"
pages: 8
size: "313.5 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD Aggregate VaR CUSIP Detail Report (FYICusipDtl) MRO

**Original File:** [mbs169_aggr_var_cusip_detail_mro.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs169_aggr_var_cusip_detail_mro.pdf)  
**Category:** MBSD  
**Total Pages:** 8  
**File Size:** 313.5 KB  

---

## Page 1

 
FIXED INCOME CLEARING CORPORATION 
MBSD AGGREGATE VAR [[CUSIP]] DETAIL REPORT (FYICUSIPDTL) MRO 
VERSION 3.0 
MARCH 10, 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself 
does not provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: March 10, 2023 
Publication Code:  MBS169 
Service: Mortgage -Backed [[securities]] Division  
Title: MBSD Aggregate  VaR [[CUSIP]] Detail Report (FYICusipDtl) MRO 

---

## Page 3

 
 
TABLE OF CONTENTS 
Report Information ............................................................................................................................................................................... 4 
General Information ............................................................................................................................................................................ 4 
Header / Trailer Records...................................................................................................................................................................... 4 
Application Header Record .................................................................................................................................................................  4 
Application Trailer Record................................................................................................................................................................... 5 
D ata Reco rd ...................................................................................................................................................................................... 6 
General Format................................................................................................................................................................................. 6 
 

---

## Page 4

MBSD Aggregate VaR [[CUSIP]] Detail Report (FYICusipDtl) MRO 
Report Information  4 
REPORT INFORMATION 
General Information 
Product No.  Product Name 
13982395 Test - MBSD Aggregate VaR  [[CUSIP]] Detail Report ( FYICusipDtl ) 
13162395 Prod - MBSD Aggregate VaR [[CUSIP]] Detail Report ( FYICusipDtl ) 
Header / Trailer Records 
Application Header Record 
Field Name Length Start End Type Comments 
CHARACTER SET 1 1 1 A/N “A” = ASCII, “E” = EBCDIC 
BLOCK SIZE 5 2 6 N ‘00896’; VARIES BY RECORD TYPE 
SOURCE NAME 4 7 10 A/N “RFL” 
FILLER 8 11 18 A/N ALWAYS = SPACES 
DESTINATION NAME 5 19 23 A/N MBSD [[participant]] [[ID]] 
FILLER 8 24 31 A/N ALWAYS = “_AVCD     “ 
DATE/TIME 22 32 53 A/N SYSTEM GENERATED TIMESTAMP 
DD-MMM-YYYY HH:MM:SS.H 
19-JAN-1989 10:45:15.2 
FILLER 843 54 896 A/N ALWAYS = SPACES 
 
  

---

## Page 5

MBSD Aggregate VaR CU SIP Detail Report (FYICusipDtl) MRO 
Report Information  5 
Application Trailer Record 
Field Name Length Start End Type Comments 
TRAILER [[ID]] 5 1 5 A/N ALWAYS = “TRAIL”  
NUMBER OF RECORDS  5 6 10 N TOTAL NUMBER OF RECORDS IN FILE  
CHECKSUM 5 11 15 N XOR OF CHECKSUMS OF ALL DATA 
RECORDS (FOR FUTURE USE) ALWAYS BLANK FOR NOW.  
DISCLAIMER 772 16 787 A/N MRO LEGAL DISCLAIMER: 
This report is for information only, provided as -is, not required of 
[[FICC]], and contains unverified information ( ‘Information ’) which may 
change. It is not a substitute for an external advisor. Members should 
independently obtain and monitor  the Information and related 
documentation.  [[FICC]] DOES NOT REPRESENT THE ACCURACY, 
ADEQUACY, TIMELINESS, COMPLETENESS OR FITNESS FOR 
ANY PARTICULAR PURPOSE OF THIS REPORT OR THE 
INFORMATION AND SHALL NOT BE LIABLE FOR (1) ANY LOSS 
RELATED TO OR ARISING OUT OF THE ACT OR PROCESS OF 
PROVIDING THE INFORMATION (INCLUDING MISTAKES, 
ERRORS, OMISSIONS, INT ERRUPTIONS, DELAYS OR 
DEFECTS), UNLESS DIRECTLY CAUSED BY [[FICC]]’S GROSS 
NEGLIGENCE OR WILLFUL MISCONDUCT OR (2) ANY SPECIAL, 
CONSEQUENTIAL, EXEMPLARY, INCIDENTAL OR PUNITIVE 
DAMAGES. 
FILLER 109 788 896 A/N FILLED WITH SPACES 
 
Note: 
The first 10 characters for each record in the initial file generated by the Risk system will contain the Remote [[ID]] (8 characters for Remo te [[ID]] followed by 2 blank 
spaces). This information is for CDTS processing only. CDTS will remove the first 10 characters before sending it to the participants. This format file only reflects the 
final state of the MRO that the participants will receive 
  

---

## Page 6

MBSD Aggregate VaR [[CUSIP]] Detail Report (FYICusipDtl) MRO 
Report Information  6 
Data Record 
General Format 
Field Name Length Start End Type Comments 
RECORD NUMBER **  5 1 5 N SEQUENTIAL NUMBER OF THE LOGICAL RECORD STARTING 
WITH 00001 
PHYSICAL RECORD 
LENGTH ** 5 6 10 N NOT GREATER THAN 896 
CHECKSUM ** 5 11 15 N 
THE CRC16 OF THE PHYSICAL RECORD 
(RESERVED FOR FUTURE USE)  
SEGMENT LOCATION **  1 16 16 N 
WHERE THIS PHYSICAL RECORD IS  
LOCATED IN THE LOGICAL RECORD:  
3 = ONLY RECORD, 1 = FIRST RECORD,  
0 = MIDDLE RECORD, 2 = LAST RECORD 
RECORD [[ID]] 2 17 18 N RECORD TYPE – ALWAYS 99 
[[participant]] AGGREGATE 
[[ID]] 15 19 33 A/N MBSD [[participant]] AGGREGATE [[ID]] 
[[participant]] AGGREGATE 
NAME 80 34 113 A/N MBSD [[participant]] AGGREGAT E NAME 
BUSINESS DATE 10 114 123 A/N BUSINESS DATE 
REQUIREMENT DATE 10 124 133 A/N REQUIREMENT DATE 
LEGAL ENTITY [[ID]]  15 134 148 A/N   
LEGAL ENTITY NAME 80 149 228 A/N   
CATEGORY 30 229 258 A/N [[Broker]]/DEALER etc . 
[[CUSIP]] 9 259 267 A/N   
AGENCY/PRODUCT 30 268 297 A/N   
SECURITY CLASS 1 298 298 A/N   

---

## Page 7

MBSD Aggregate VaR [[CUSIP]] Detail Report (FYICusipDtl) MRO 
Report Information  7 
Field Name Length Start End Type Comments 
[[settlement]] DATE 10 299 308 A/N   
DESCRIPTION 80 309 388 A/N   
TRADE TYPE 1 389 389 A/N   
OPEN PAR 20 390 409 N   
[[settlement]] PRICE 14 410 423 N   
[[settlement]] AMOUNT  20 424 443 N   
VAR CONTRIBUTION 
AMOUNT 20 444 463 N   
VAR CONTRIBUTION 
PERCENT 14 464 477 N   
GROSS MARKET VALUE 20 478 497 N   
VAR PRICING 3 498 500 A/N  ‘P’ or ‘IBH’ 
WEIGHT PERCENT 14 501 514 N   
MARKET PRICE 14 515 528 N   
MARKET VALUE 20 529 548 N   
FILLER 347 549 895 A/N ALWAYS = SPACES 
CONFIRMATION 
CONTINUED 1 896 896 A/N 
" " = ONLY RECORD (NO OVERFLOW  
RECORD) 
"1" = FIRST OF MANY RECORDS (IF  
OVERFLOW RECORDS ARE  
REQUIRED) 
"2" = LAST OF MANY RECORDS (IF  
TWO OR MORE RECORDS ARE  
REQUIRED) 
 
**Standard 16 Bytes 

---

## Page 8

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 