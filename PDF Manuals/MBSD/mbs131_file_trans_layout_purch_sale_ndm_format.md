---
title: "File Transmission Layout: Purchase & Sale NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs131_file_trans_layout_purch_sale_ndm_format.pdf"
pages: 14
size: "327.7 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# File Transmission Layout: Purchase & Sale NDM Format

**Original File:** [mbs131_file_trans_layout_purch_sale_ndm_format.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs131_file_trans_layout_purch_sale_ndm_format.pdf)  
**Category:** MBSD  
**Total Pages:** 14  
**File Size:** 327.7 KB  

---

## Page 1

 
 
 
[[FICC]] - MBSD 
FILE TRANSMISSION LAYOUT: PURCHASE & SALE NDM FORMAT 
VERSION 1.03 
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
Publication Code: MBS131 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout –  Purchase & Sale NDM Format  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction to the Documentation.................................................................................................... 4 
Purpose ....................................................................................................................................... 4 
Frequency .................................................................................................................................... 4 
Recor d La you t .............................................................................................................................. 4 
Version C on tr ol ............................................................................................................................. 5 
1. File Transmission – Purchase and Sale – NDM Format (HEADER) ................................................... 6 
2. File Transmission – Purchase and Sale – NDM Format ([[CUSIP]] / CLASS HEADER) ............................ 7 
3. File Transmission – Purchase and Sale – NDM Format (DEALER DETAIL RECORD) ......................... 8 
4. File Transmission – Purchase and Sale – NDM Format (NOS DETAIL RECORD) ..............................10  
5. File Transmission – Purchase and Sale – NDM Format ([[Broker]] DETAIL RECORD) .......................11  
6. File Transmission – Purchase and Sale – NDM Format (TRAILER) ..................................................13  
 

---

## Page 4

Purchase and Sales Report NDM 
Introduction to the Doc umentation 4 
INTRODUCTION TO THE DOCUMENTATION 
Purpose 
The Purchase and Sale Report reflects compared trades from the current date as well as any subsequent 
activity associated with a trade i.e., [[Novation]], cancel, settle, etc. 
Frequency 
Daily. 
Record Layout 
*All records are of equal length - 202 bytes. 
*There are 7 different record types, each uniquely identified by card code, as follows: card codes 01 through 
06, & 99. 
 
ACCOUNT / REPORT HEADER RECORD (CARD CODE 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
 
[[CUSIP]] HEADER RECORD (CARD CODE 02) 
Control record which signifies the beginning of the next [[CUSIP]]. 
 
DEALER DETAIL RECORD (CARD CODE 03) 
Detail record containing a single trade formatted for dealer accounts only. 
 
SETTLEMENTS RECORD (CARD CODE 05) 
The number of NOSs (notification of [[settlement]]) per trade is not related to the number contained on a logical 
record. For every NOS encountered for a given trade, one (Card code 05) will be transmitted. 
 
[[Broker]] DETAIL RECORD (CARD CODE 06) 
Detail record containing a single trade formatted for [[Broker]] account only. 
 
TRAILER CONTROL RECORD (CARD CODE 99) 
Trailer record indicates the end of the report for the recipient account. 

---

## Page 5

Purchase and Sales Report NDM 
Introduction to the Doc umentation 5 
Version Control 
Date Version # Name Description of Change  
4/3/2001 Original MBSD • Initial  version  
7/16/2015 1.0 C. Swords  Removed  obsolete  information  and updated to support 
[[Novation]]:  
• In Card Code  03 (DEALER DETAIL RECORD), 
added  trade sub-type and SPT pool number using 
filler  at end of record;  added  NOV as valid  type of 
activity. 
• In Card Code  06 ([[Broker]] DETAIL 
RECORD), replaced  [[Option]] type with filler,  as 
now  obsolete.  
• Card Code  04 (SPECIAL INSTRUCTIONS 
RECORD) removed  as obsolete.  
2/27/2016 1.01 C. Swords  Made following  changes: 
• In Card Code  03 (DEALER DETAIL RECORD), 
added  RCRT as valid  type of activity.  
8/24/2016 1.02 C. Swords  Made following  informational  changes:  
• Ad d title page  and  revision  his tor y. 
4/04/2022 1.03 J. Sheeran  Updated [[DTCC]] branding template  
 

---

## Page 6

Purchase and Sales Report NDM 
Introduction to the Doc umentation 6 
1. FILE TRANSMISSION – PURCHASE AND SALE – NDM 
FORMAT (HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-PS1- CA RD- CODE 2 N PIC 9(02). Header Record,  Card Code  = 
'01' 
RPT-PS1- RPT- [[ID]] 8 A/N PIC X(08). Report  [[ID]] = 'MB4761-A' 
     RPT-PS1-ACC- AGG-[[ID]]. 3 N PIC 9(03). [[participant]]  [[ID]] 
      RPT-PS1-PA RT- [[ID]] 2 A/N PIC 9(02). Aggregate  
RPT-PS1-AGG 4 A/N PIC X(04). Account  Symbol 
RPT-PS1-ACC T 40 A/N PIC X(40). [[participant]]  Name 
RPT-PS1-[[participant]]-NA ME 8 A/N PIC X(08). Date of Report  (YYYYMMDD) 
RPT-PS1- BUS- DA TE 1 A/N PIC X(01).   Pass Indicator  (A=Morning or 
P=Evening)  
RPT-PS1- PASS 134 A PIC X(134). Filler  
Total     202 

---

## Page 7

Purchase and Sales Report NDM 
Introduction to the Doc umentation 7 
2. FILE TRANSMISSION – PURCHASE AND SALE – NDM 
FORMAT ([[CUSIP]] / CLASS HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-PS2- CA RD- CODE 2 N PIC 9(02). [[CUSIP]] Record,  Card Code  = 
'02' 
RPT-PS2-[[settlement]] -
YEAR  
4 N PIC 9(04). [[settlement]] Year (YYYY) 
RPT-PS2-[[settlement]]- 
MONTH 
2 N PIC 9(02). [[settlement]] Month  (MM) 
RPT-PS2- [[CUSIP]]. 9 A/N PIC X(09). [[CUSIP]] 
    FILLER 1 A PIC X(01).     Filler  
    RPT-PS2-ACC T 4 A/N PIC X(04). Account  Symbol 
FILLER 10 A PIC X(10). Filler  
RPT-PS2- [[CUSIP]]-
DESCRIPTION 
40 A/N PIC X(40). [[CUSIP]] Description  
FILLER 130 A PIC X(130). Filler  
Total 202    
 
 
 
 
 
 
 
 
 

---

## Page 8

Purchase and Sales Report NDM 
Introduction to the Doc umentation 8 
3. FILE TRANSMISSION – PURCHASE AND SALE – NDM 
FORMAT (DEALER DETAIL RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-PS3- CA RD- CODE 2 N PIC 9(02). Dealer Detail Record,  Card 
Code  = '03' 
RPT-PS3-[[settlement]] -YEAR  4 N PIC 9(04). [[settlement]] Year (YYYY) 
RPT-PS3-[[settlement]]- MONTH 2 N PIC 9(02). [[settlement]] Month (MM) 
RPT-PS3- [[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] 
FILLER 1 A/N PIC X(01). Filler  
RPT-PS3-ACC T 4 A/N PIC X(04). Account  Symbol 
RPT-PS3- TRA DE- [[ID]].    Trade Number 
RPT-PS3- TRD- PREFIX- NBR 4 N PIC 9(04). Trade Number Prefix 
RPT-PS3- TRD-SUFFIX- NBR 6 N PIC 9(06). Trade Number Suffix 
RPT-PS3-ACT IVIT Y 6 A/N PIC X(06). Activity Type -  TCR, CAN, GUP, 
MOD, NOS, NCVT, NCRT, NOV 
RPT-PS3- SUB- INTERNAL-XREF 15 A/N PIC X(15). Internal  XREF/Trade # 
RPT-PS3- TRADE-TY PE 4 A/N PIC X(04). Trade Type -TFTD,SBOD,OPTN, 
SBOO, SBON 
RPT-PS3-[[Option]]- TYPE 4 A/N PIC X(04). [[Option]] Type  - 'PUTS' or 'CALL' 
RPT-PS3-BS-INDICATOR  1 A/N PIC X(01). B = Buy, S = Sell 
RPT-PS3- TRADE-DA TE 8 A/N PIC X(08). Trade Date (YYYYMMDD) 
RPT-PS3-MATCH- DATE 8 A/N PIC X(08). Match Date (YYYYMMDD) 
RPT-PS3-SETTL- DA TE 8 A/N PIC X(08). [[settlement]] Date (YYYYMMDD) 
RPT-PS3-GIVE- UP-DATE 8 A/N PIC X(08). Give-Up Date (YYYYMMDD) 
RPT-PS3- ENTRY-DA TE 8 A/N PIC X(08). Entry Date (YYYYMMDD) 
RPT-PS3- CONTRA-ACCT 4 A/N PIC X(04). Contra  Account  
RPT-PS3-[[Broker]] -ACCT  4 A/N PIC X(04). [[Broker]]  Account  Symbol 
RPT-PS3-BRKR-COMM ISS I ON 7 N PIC 9(05)V9(02). [[Broker]]  Commission  
RPT-PS3- TRADE-STATUS 4 A/N PIC X(04). Trade Status - FMAT, PMAT, 
PSET, FSET, PCAN, CAN, NCAN 
RPT-PS3- DLR- PRICE 15 N PIC 9(03)V9(12). Trade Price - In Decimal 
RPT-PS3- STTL- PRICE 15 N PIC 9(03)V9(12). [[settlement]] Trade Price - In 
Decimal 

---

## Page 9

Purchase and Sales Report NDM 
Introduction to the Doc umentation 9 
Field Name Length Type Cobol Picture Description/Comments  
RPT-PS3- PA R-VALUE 13 N PIC 9(11)V9(02). Par Value or Amortized Value 
RPT-PS3- CONTRACT-VALUE 13 N PIC 9(11)V9(02). [[settlement]] Value 
PT-PS3-TRD- SUB- TYPE 4 A/N PIC X(04). Trade Sub-Type  - TBA, SPT, 
STIP 
RPT-PS3-SPT- POOL- NUMBER 7 A/N PIC X(07). SPT Pool  Number 
FILLER 14 A PIC X(14). Filler  
Total     202 
 
  

---

## Page 10

Purchase and Sales Report NDM 
Introduction to the Doc umentation 10 
4. FILE TRANSMISSION – PURCHASE AND SALE – NDM 
FORMAT (NOS DETAIL RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-PS5- CA RD- CODE 2 N PIC 9(02). NOS Detail Record,  Card Code  
= '05' 
RPT-PS5-[[settlement]] -YEAR  4 N PIC 9(04). [[settlement]] Year (YYYY) 
RPT-PS5-[[settlement]]- MONTH 2 N PIC 9(02). [[settlement]] Month (MM) 
RPT-PS5- [[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] 
FILLER 1 A/N PIC X(01). Filler  
RPT-PS5-ACC T 4 A/N PIC X(04). Account  Symbol 
RPT-PS5- TRA DE- [[ID]].    Trade Number 
     RPT-PS5- TRD- PREFIX- NBR 4 N PIC 9(04). Trade Number Prefix 
     RPT-PS5- TRD-SUFFIX- NBR 6 N PIC 9(06). Trade Number Suffix 
RPT-PS5- POOL 9 A/N PIC X(09). Pool  Number-1 
RPT-PS5-AMORT-VALUE  13 N PIC 9(11)V9(02). Amortized Value-1 
RPT-PS5- POOL- CONTROL- NBR 15 A/N PIC X(15). Internal  XREF/Trade #-1 
RPT-PS5-MATCH- DATE 8 A PIC X(08) Date the NOS Transaction  was 
Matched  
FILLER 125 A PIC X(125). Filler  
   Total 202 
 
 
  

---

## Page 11

Purchase and Sales Report NDM 
Introduction to the Doc umentation 11 
5. FILE TRANSMISSION – PURCHASE AND SALE – NDM 
FORMAT ([[Broker]] DETAIL RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-PS6- CA RD- CODE 2 N PIC 9(02). [[Broker]]  Detail Record,  Card Code  
= '06' 
RPT-PS6-[[settlement]] -YEAR  4 N PIC 9(04). [[settlement]] Year (YYYY) 
RPT-PS6-[[settlement]]- MONTH 2 N PIC 9(02). [[settlement]] Month (MM) 
RPT-PS6- [[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] 
FILLER 1 A/N PIC X(01). Filler  
RPT-PS6-ACC T 4 A/N PIC X(04). Account  Symbol 
RPT-PS6-ACT IVIT Y 6 A/N PIC X(06). Activity  Type  - TCR, CAN, GUP, 
MOD, NCVT 
RPT-PS6- TRA DE- [[ID]].    Trade Number 
     RPT-PS6- TRD- PREFIX- NBR 4 N PIC 9(04). Trade Number Prefix 
     RPT-PS6- TRD-SUFFIX- NBR 6 N PIC 9(06). Trade Number Suffix 
RPT-PS6- SUB- INTERNAL-XREF 15 A/N PIC X(15). Internal  XREF/Trade # 
RPT-PS6- TRADE-TY PE 4 A/N PIC X(04). Trade Type  - TFTD, SBOD 
RPT-PS6-[[Option]]- TYPE- FILLER 4 A/N PIC X(04). [[Option]] Type  - 'PUTS' or 'CALL'- 
Filler  
  
RPT-PS6- TRADE-DA TE 8 A/N PIC X(08). Trade Date (YYYYMMDD) 
RPT-PS6-MATCH- DATE 8 A/N PIC X(08). Match Date (YYYYMMDD) 
RPT-PS6-SETTL- DA TE 8 A/N PIC X(08). [[settlement]] Date (YYYYMMDD) 
for TFTD, 
Trades  Only  
RPT-PS6-GIVE- UP-DATE 8 A/N PIC X(08). Give-Up Date (YYYYMMDD) 
RPT-PS6- ENTRY-DA TE 8 A/N PIC X(08). Trade Entry Date (YYYYMMDD) 
RPT-PS6- BUY-ACCT 4 A/N PIC X(04). Buy Dealer Account  
RPT-PS6-BUY- CO MMISSION 7 N PIC 9(05)V9(02). Buy Dealer Commission  
RPT-PS6- BUY- PRICE 15 N PIC 9(03)V9(12). Buy Dealer Price - In Decimal 
RPT-PS6-SELL-A CCT 4 A/N PIC X(04). Sell Dealer Account  
RPT-PS6-SELL- COMMISSION 7 N PIC 9(05)V9(02). Sell Dealer Commission  
RPT-PS6-SELL- PRICE 15 N PIC 9(03)V9(12). Sell Dealer Price - In Decimal 

---

## Page 12

Purchase and Sales Report NDM 
Introduction to the Doc umentation 12 
Field Name Length Type Cobol Picture Description/Comments  
RPT-PS6- TRADE-STATUS 4 A/N PIC X(04). Trade Status - FMAT, PMAT, 
PCAN, CAN 
RPT-PS6- STTL- PRICE 15 N PIC 9(03)V9(12). [[settlement]] Trade Price - In 
Decimal 
RPT-PS6- PA R-VALUE 13 N PIC 9(11)V9(02). Par Value 
RPT-PS6- CONTRACT-VALUE 13 N PIC 9(11)V9(02). [[settlement]] Value 
FILLER 4 A PIC X(04). Filler  
   Total      202 
 
 
  

---

## Page 13

Purchase and Sales Report NDM 
Introduction to the Doc umentation 13 
6. FILE TRANSMISSION – PURCHASE AND SALE – NDM 
FORMAT (TRAILER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-P99- CARD- CODE  2 N PIC 9(02). Trailer  Record,  Card Code  = '99' 
FILLER 13 A PIC X(13). Filler  
RPT-PS99-A CCT 4 A/N PIC X(04). Account  Symbol 
FILLER 1 A PIC X(01). Filler  
RPT-PS99-LOGICAL- COUNT  7 N PIC 9(07). Logical  Record  Count  
FILLER 1 A PIC X(01). Filler  
RPT-PS99- PHYSICAL- COUNT 7 N PIC 9(07). Physical  Record  Count  
FILLER 167 A PIC X(167). Filler  
  Total     202  

---

## Page 14

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 