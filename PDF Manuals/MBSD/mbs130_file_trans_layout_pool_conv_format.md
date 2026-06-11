---
title: "File Transmission Layout: Pool Conversion Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs130_file_trans_layout_pool_conv_format.pdf"
pages: 12
size: "320.1 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# File Transmission Layout: Pool Conversion Format

**Original File:** [mbs130_file_trans_layout_pool_conv_format.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs130_file_trans_layout_pool_conv_format.pdf)  
**Category:** MBSD  
**Total Pages:** 12  
**File Size:** 320.1 KB  

---

## Page 1

 
 
 
[[FICC]] - MBSD 
FILE TRANSMISSION LAYOUT: POOL CONVERSION FORMAT 
VERSION 1.05 
APRIL 06, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: April 6, 2022 
Publication Code: MBS130 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout : Pool Conversion  Format 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction to the Documentation.................................................................................................... 4 
Purpose ....................................................................................................................................... 4 
Frequency .................................................................................................................................... 4 
Recor d La you t .............................................................................................................................. 4 
Version C on tr ol ............................................................................................................................. 5 
1. File Transmission Layout – Pool Conversion – Form at (HE ADE R) ................................................... 6 
2. File Transmission Layout – Pool Conversion – Format (CONVERTED TRADE DETAIL) ..................... 7 
3. File Transmission Layout – Pool Conversion – Format (CONVERTED PID DETAIL)........................... 8 
4. File Transmission Layout – Pool Conversion – Format (RESULTING POID DETAIL).........................10  
5. File Transmission Layout – Pool Conversion – Format (TRAILER) ..................................................11  
 

---

## Page 4

Pool Conversion 
Introduction to the Doc umentation 4 
INTRODUCTION TO THE DOCUMENTATION 
Purpose 
Reflects Specified Pool Trades (“SPT”), Stipulated Trades (“STIP”) and generic TBA allocations converted to 
Pool [[obligations]] (POIDs) at the trade execution price for delivery next business day. 
Frequency 
Daily. 
Record Layout 
*All records are of equal length - 228 bytes. 
*There are 5 different record types, each uniquely identified by card code, as follows: card codes 01 through 
04, & 99. 
 
ACCOUNT / REPORT HEADER RECORD (CARD CODE 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
 
CONVERTED TRADE DETAIL RECORD (CARD CODE 02) 
Detail record containing a single converted trade record. 
 
CONVERTED POOL INSTRUCT DETAIL RECORD (CARD CODE 03) 
Detail record containing a single converted pool instruct record. 
 
RESULTING POOL OBLIGATION DETAIL RECORD (CARD CODE 04) 
Detail record containing a single resulting pool obligation record. 
 
TRAILER CONTROL RECORD (CARD CODE 99) 
Trailer record indicates the end of the report for the recipient account. 
 
Sample File 
*Sample file provided after Record Layouts section. 
 

---

## Page 5

Pool Conversion 
Introduction to the Doc umentation 5 
Version Control 
Date Version # Name Description of Change  
7/16/2015 1.0 C. Swords  Initial  version  
8/4/2016 1.01 C. Swords  Made following  updates:  
• Card Code 03, field RPT-CNV3-PID-[[ID]] 
(Pool Instruct  Identifier) is  alphanumeric, 
not  numeric.  
• Card Code 03, field RPT -CNV3-TRADE-SUB-
TYPE (Targeted  Trade Sub-Type) can be STIP 
or TBA; SPT is not a valid  [[Option]].  
• Card Code 04, field RPT -CNV4-PID-[[ID]] 
(Associated Pool  Instruct Identifier) is  A/N, 
rather than  N. 
• Ad d title page  and  revision  his tor y 
10/13/2016 1.02 C. Swords  Mad e following  updates:  
• Card Code 04 (Resulting POID Detail), field RPT -
CNV4-ASC- TRADE-[[ID]] (Associated Trade 
Number) is not populated for  POIDs resulting  from 
generic  TBA trades; it is only  populated for SPT 
trades and  STIP allocations.  
• Updated  remo ve NDM from document  n ame 
7/20/2017 1.03 C. Swords  Mad e following  informational  changes:  
• Card Code 04 Resulting POID Detail Record – 
make comment  that Trade [[ID]] (RPT-CNV4-ASC-
TRADE-[[ID]], reflected as  prefix/suffix)  is only 
populated  for SPT trades or STIP PIDs. 
4/17/2018 1.04 J. Xie Adding clarification on PID field  format: 
• Clarify that PID-[[ID]] 16-character fixed -length alpha -
numeric  field  is left padded with 2 zeros. 
04/04/2022 1.05 J. Sheeran  Updated to latest [[DTCC]] Branding  
 

---

## Page 6

Pool Conversion 
1. File Transmission Layout – Pool Conv ersion – Format (HEADER) 6 
1. FILE TRANSMISSION LAYOUT – POOL CONVERSION 
– FORMAT (HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-CNV1-CARD-CODE 2 N PIC 9(02) Header Record,  Card code  = ‘01’ 
RPT-CNV1-RPT-[[ID]] 8 A/N PIC X(08) Report  [[ID]] = ‘MB8102-N’ 
RPT-CNV1-ACC-AGG-[[ID]]     
     RPT-CNV1-PART-[[ID]] 3 N PIC 9(03) [[participant]]  [[ID]] 
     RPT-CNV1-AGG 2 N PIC 9(02) Aggregate  
RPT-CNV1-ACCT 4 A PIC X(04) Account  Symbol 
RPT-CNV1-PART-NAME 40 A/N PIC X(40) [[participant]]  Name 
RPT-CNV1-BUS-DATE 8 N PIC 9(08) Date of Report  
FILLER 161 A PIC X(161) Filler  
Total     228 

---

## Page 7

Pool Conversion 
2. File Transmission Layout – Pool Conv ersion – Format (CONVERTED TRADE DETAIL) 7 
2. FILE TRANSMISSION LAYOUT – POOL CONVERSION 
– FORMAT (CONVERTED TRADE DETAIL) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-CNV2-CARD-CODE 2 N PIC 9(02) Converted  Trade Detail Record,  Card 
code  
= ‘02’ 
RPT-CNV2-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-CNV2-ACCT 4 A/N PIC X(04) Account  Symbol 
RPT-CNV2-TRADE-[[ID]]     
         RPT-CNV2-TRD-PFX 4 N PIC 9(04)     Trade Number Prefix 
         RPT-CNV2-TRD-SFX 6 N PIC 9(06) Trade Number Suffix 
RPT-CNV2-XREF 15 A/N PIC X(15) Internal  XREF / Trade # 
RPT-CNV2-TRADE-TYPE 4 A/N PIC X(04) Trade Type -TFTD 
RPT-CNV2-TRADE-SUB-
TYPE 
4 A/N PIC X(04) Trade Sub-Type  - SPT 
RPT-CNV2-BS-IND 1 A PIC X(01) Buy/Sell Code,  B=Buy, S = Sell 
RPT-CNV2-TRD-DATE 8 N PIC 9(08) Trade Date (YYYYMMDD) 
RPT-CNV2-STTL-DATE 8 N PIC 9(08) [[settlement]] Date (YYYYMMDD) 
RPT-CNV2-CTRA 4 A/N PIC X(04) Contra  Account  
RPT-CNV2-POOL-NUMBER 6 A/N PIC X(06) Pool  Number 
RPT-CNV2-POOL-[[CUSIP]] 9 A/N PIC X(09) Pool  [[CUSIP]] 
RPT-CNV2-STTL-PRICE 15 N PIC 9(03)V9(12) [[settlement]] Price – In Decimal 
RPT-CNV2-ORIG-FACE 15 N PIC 9(15) Original Face 
RPT-CNV2 -CURR - FACE 17 N PIC 9(15)V9(02) Current Face 
RPT-CNV2-NET-MONEY 15 N PIC 9(13)V9(02) Net Money  
RPT-CNV2-NET-MONEY-
CRDR 
1 A PIC X(01) Net Money  Indicator  (C=Credit,  D=Debit) 
FILLER 81 A PIC X(81) Filler  
Total 228    
 
 
 
 
 
 
 
 
 

---

## Page 8

Pool Conversion 
3. File Transmission Layout – Pool Conv ersion – Format (CONVERTED PID DET AIL) 8 
3. FILE TRANSMISSION LAYOUT – POOL CONVERSION 
– FORMAT (CONVERTED PID DETAIL) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-CNV3-CARD-CODE 2 N PIC 9(02) Converted  PID Detail Record,  Card 
code = ‘03’ 
RPT-CNV3-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-CNV3-ACCT 4 A/N PIC X(04) Account  Symbol 
RPT-CNV3-PID-[[ID]] 16 A/N PIC X(16) Pool  Instruct Identifier. Left 
padded with 2   leading 0s1.  
RPT-CNV3-STIP -TRADE-[[ID]]     
     RPT-CNV3-STIP-TRD-PFX 4 N PIC 9(04) Targeted  Trade Number Prefix 
     RPT-CNV3-STIP-TRD-SFX 6 N PIC 9(06) Targeted  Trade Number Suffix 
RPT-CNV3-XREF 15 A/N PIC X(15) Targeted  Trade Internal  XREF / 
Trade # 
RPT-CNV3-TRADE-TYPE 4 A/N PIC X(04) Targeted  Trade Type -TFTD, 
SBON 
RPT-CNV3-TRADE-SUB-TYPE 4 A/N PIC X(04) Targeted  Trade Sub-Type  – STIP, 
TBA 
RPT-CNV3-BS-IND 1 A PIC X(01) Buy/Sell Code,  B=Buy, S = Sell 
RPT-CNV3-TRD-DATE 8 N PIC 9(08) Trade Date (YYYYMMDD) 
RPT-CNV3-STTL-DATE 8 N PIC 9(08) [[settlement]] Date (YYYYMMDD) 
RPT-CNV3-DLVRY-DATE 8 N PIC 9(08) Delivery  Date (YYYYMMDD) 
RPT-CNV3-CTRA 4 A/N PIC X(04) Contra  Account  
RPT-CNV3-POOL-NUMBER 6 A/N PIC X(06) Pool  Number 
RPT-CNV3-POOL-[[CUSIP]] 9 A/N PIC X(09) Pool  [[CUSIP]] 
RPT-CNV3-STTL-PRICE 15 N PIC 9(03)V9(12) [[settlement]] Price – In Decimal 
RPT-CNV3-ORIG-FACE 15 N PIC 9(15) Original Face 
RPT-CNV3 -CURR - FACE 17 N PIC 9(15)V9(02) Current Face 
RPT-CNV3-NET-MONEY 15 N PIC 9(13)V9(02) Net Money  
RPT-CNV3-NET-MONEY-CRDR 1 A PIC X(01) Net Money  Indicator  (C=Credit,  
D=Debit) 
 
1 For example: If PID value is 0005948-041018, in the MRO 16-character field that’s left padded with 0s, it will 
be 000005948-041018. In current system, PID is 14-character long. 

---

## Page 9

Pool Conversion 
3. File Transmission Layout – Pool Conv ersion – Format (CONVERTED PID DETAIL) 9 
Field Name Length Type Cobol Picture Description/Comments  
FILLER 57 A PIC X(57) Filler  
Total     228 
 
  

---

## Page 10

Pool Conversion 
4. File Transmission Layout – Pool Conv ersion – Format (RESULTING POID DETAIL) 10 
4. FILE TRANSMISSION LAYOUT – POOL CONVERSION 
– FORMAT (RESULTING POID DETAIL) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-CNV4-CARD-CODE 2 N PIC 9(02) Resulting  POID Detail Record,  
Card code  = ‘04’ 
RPT-CNV4-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-CNV4-ACCT 4 A/N PIC X(04) Account  Symbol 
RPT-CNV4-POID 14 N PIC 9(14) Pool  Obligation  [[ID]] 
RPT-CNV4-PID-[[ID]] 16 A/N PIC X(16) Associated Pool Instruct Identifier  
(for POIDs resulting  from PID 
only).  When  populated,  it is left 
padded with 2 leading 0s.  
RPT-CNV4-ASC-TRADE-[[ID]]     
     RPT-CNV4-ASC-TRD-PFX 4 N PIC 9(04) Associated Trade Number Prefix 
(for POIDs resulting  from SPT 
trades or STIP PIDs only)  
     RPT-CNV4-ASC-TRD-SFX 6 N PIC 9(06) Associated Trade Number Suffix 
(for POIDs resulting  from SPT 
trades or STIP PIDs only)  
RPT-CNV4-BS-IND 1 A PIC X(01) Buy/Sell Code,  B=Buy, S = Sell 
RPT-CNV4-TRD-DATE 8 N PIC 9(08) Trade Date (YYYYMMDD) 
RPT-CNV4-STTL-DATE 8 N PIC 9(08) [[settlement]] Date (YYYYMMDD) 
RPT-CNV4-DLVRY-DATE 8 N PIC 9(08) Delivery  Date (YYYYMMDD) 
RPT-CNV4-CTRA 4 A/N PIC X(04) Contra  Account  
RPT-CNV4-POOL-NUMBER 6 A/N PIC X(06) Pool  Number 
RPT-CNV4-POOL-[[CUSIP]] 9 A/N PIC X(09) Pool  [[CUSIP]] 
RPT-CNV4-STTL-PRICE 15 N PIC 9(03)V9(12) [[settlement]] Price – In Decimal 
RPT-CNV4-ORIG-FACE 15 N PIC 9(15) Original Face 
RPT-CNV4 -CURR - FACE 17 N PIC 9(15)V9(02) Current Face 
RPT-CNV4-NET-MONEY 15 N PIC 9(13)V9(02) Net Money  
RPT-CNV4-NET-MONEY-CRDR 1 A PIC X(01) Net Money  Indicator  (C=Credit,  
D=Debit) 
FILLER 66 A PIC X(66) Filler  
   Total 228 
 

---

## Page 11

Pool Conversion 
5. File Transmission Layout – Pool Conv ersion – Format (TRAILER) 11 
5. FILE TRANSMISSION LAYOUT – POOL CONVERSION 
– FORMAT (TRAILER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-CNV99-CARD-CODE 2 N PIC 9(02) Trailer  Record,  Card Code  = '99' 
FILLER 13 A PIC X(13) Filler  
RPT-CNV99-ACCT 4 A/N PIC X(04) Account  Symbol 
FILLER 1 A PIC X(01) Filler  
RPT-CNV99-LOGICAL-COUNT 7 N PIC 9(07) Logical  Record  Count  
FILLER 1 A PIC X(01) Filler  
RPT-CNV99-PHYSICAL-COUNT 7 N PIC 9(07) Physical  Record  Count  
FILLER 193 A PIC X(193) Filler  
  Total     228  

---

## Page 12

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 