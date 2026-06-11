---
title: "File Transmission Layout: Compressed Open Commitment NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs128_file_trans_layout_compressed_open_commit_ndm_20220406.pdf"
pages: 15
size: "377.8 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# File Transmission Layout: Compressed Open Commitment NDM Format

**Original File:** [mbs128_file_trans_layout_compressed_open_commit_ndm_20220406.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs128_file_trans_layout_compressed_open_commit_ndm_20220406.pdf)  
**Category:** MBSD  
**Total Pages:** 15  
**File Size:** 377.8 KB  

---

## Page 1

 
 
 
[[FICC]] - MBSD 
FILE TRANSMISSION LAYOUT – COMPRESSED OPEN COMMITMENT NDM 
FORMAT 
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
Publication Code: MBS128 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout : Compressed Open Commitment NDM Format  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction to the Documentation.................................................................................................... 4 
Purpose ....................................................................................................................................... 4 
Frequency .................................................................................................................................... 4 
Recor d La you t .............................................................................................................................. 4 
Version C on tr ol ............................................................................................................................. 5 
1. File Transmission Layout – Compressed Open Commitment – NDM Format (Header) ....................... 6 
2. File Transmission Layout – Compressed Open Commitment – NDM Format ([[CUSIP]]/Class Header) ... 7 
3. File Transmission Layout – Compressed Open Commitment – NDM Format (Dealer Detail Record) ... 8 
4. File Transmission Layout – Compressed Open Commitment – NDM Format ([[CUSIP]] CLASS FOOTER 
RECORD) .......................................................................................................................................10  
5. File Transmission Layout – Compressed Open Commitment – NDM Format (REPORT FOOTER 
RECORD) .......................................................................................................................................11  
6. File Transmission Layout – Compressed Open Commitment – NDM Format ([[Broker]] DETAIL 
RECORD) .......................................................................................................................................12  
7. File Transmission Layout – Compressed Open Commitment – NDM Format (Trailer) .......................14  
 

---

## Page 4

Compressed Open Commitment  NDM 
Introduction to the Doc umentation 4 
INTRODUCTION TO THE DOCUMENTATION 
Purpose 
The Compressed Open Commitment report reflects all compared trades in their current state. 
Frequency 
Daily. 
Record Layout 
*All records are of equal length - 220 bytes. 
*There are 8 different record types, each uniquely identified by card code, as follows: card codes 01 through 
07, & 99. 
*The end of the report is signified by the 99 or “trailer” record. 
 
ACCOUNT / REPORT HEADER RECORD (CARD CODE 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
 
[[CUSIP]] HEADER RECORD (CARD CODE 02) 
Header record detailing [[settlement]] month, year, [[CUSIP]] and [[CUSIP]] description. 
 
DEALER DETAIL RECORD (CARD CODE 03) 
Detail record containing a single TCR or CAN. 
 
[[CUSIP]] FOOTER RECORD (CARD CODE 05) 
Detail record containing [[CUSIP]] totals. 
 
REPORT FOOTER RECORD (CARD CODE 06) 
Detail record containing total values. 
 
[[Broker]] DETAIL RECORD (CARD CODE 07) 
[[Broker]] detail record containing trade details. 
 
TRAILER CONTROL RECORD (CARD CODE 99) 
Trailer record indicates the end of the report for the recipient account. 
 

---

## Page 5

Compressed Open Commitment  NDM 
Introduction to the Doc umentation 5 
Version Control 
Date Version # Name Description of Change  
4/3/2001 Original MBSD Initial version 
7/16/2015 1.0 C. Swords Removed obsolete information and updated to support 
[[Novation]]: 
• In Card Code 03 (DEALER DETAIL 
RECORD), added commission amount, 
trade sub- type and SPT pool  number 
using filler at end of record. 
• In Card Code 07 ([[Broker]] DETAIL RECORD), 
added buy and sell dealer commission 
amount using filler at end of record. 
• Card Code 04 (TCR / CAN SPECIAL 
INSTRUCTIONS RECORD) removed as obsolete. 
2/27/2016 1.01 C. Swords Made following changes: 
• In Card Code 06 (DEALER DETAIL 
RECORD),  updated length of SPT pool 
number to 6; added Original Par. 
• In Card Code 08 ([[Broker]] DETAIL RECORD), 
added trade sub-type, SPT pool number and 
original par. 
8/11/2016 1.02 C. Swords Made following informational changes: 
• Add comment on Give-Up field that will 
be blank for [[Novation]]-eligible trades 
• Add comment on SBOO that applicable for TBA 
CUSIPs not eligible for [[Novation]] only. 
04/05/2022 1.03 J. Sheeran Updated to latest [[DTCC]] branding 
 

---

## Page 6

Compressed Open Commitment  NDM 
1. File Transmission Layout – Compressed Open Commitment – NDM Format (Header) 6 
1. FILE TRANSMISSION LAYOUT – COMPRESSED OPEN 
COMMITMENT – NDM FORMAT (HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-PS1- CA RD- CODE 2 N PIC 9(02) Header Record,  Card Code  = 
'01' 
RPT-PS1- RPT- [[ID]] 8 A/N PIC X(08) Report  [[ID]] = 'MB4891-A' 
RPT-PS1-ACC-AGG- [[ID]]     
     RPT-PS1-PART  3 N PIC 9(03) [[participant]]  [[ID]] 
     RPT-PS1-AGG 2 A/N PIC 9(02) Aggregate  
RPT-PS1-ACC T 4 A/N PIC X(04) Account  Symbol 
RPT-PS1-[[participant]]-NA ME 40 A/N PIC X(40) [[participant]]  Name 
RPT-PS1- BUS- DA TE 8 A/N PIC X(08) Date of Report  (YYYYMMDD) 
RPT-PS1- PASS 1 A/N PIC X(01) Pass Indicator  (A=Morning or 
P=Evening)  
FILLER 152 A PIC X(152) Filler  
Total     220 

---

## Page 7

Compressed Open Commitment  NDM 
2. File Transmission Layout – Compressed Open Commitment – NDM Format ([[CUSIP]]/Class  Header) 7 
2. FILE TRANSMISSION LAYOUT – COMPRESSED OPEN 
COMMITMENT – NDM FORMAT ([[CUSIP]]/CLASS HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-OCC- DT2- CA RD- CODE 2 N PIC 9(02). [[CUSIP]] Header, Card Code  = '02' 
RPT-OCC-DT2-STT L-YY 4 N PIC 9(04). [[settlement]] Year (YYYY) 
RPT-OCC-DT2-STTL- MM 2 N PIC 9(02). [[settlement]] Month  (MM) 
RPT-OCC- DT2- [[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] 
    FILLER 1 A PIC X(01).     Filler  
    RPT-OCC- DT2-A CCOUNT 4 A/N PIC X(04). Account  Symbol 
FILLER 10 A PIC X(10). Filler  
RPT-OCC- DT2- [[CUSIP]]- DESC 40 A/N PIC X(40). [[CUSIP]] Description  
RPT-OCC- DT2- MKT- PRC 15 N PIC 9(03)V9(12). Market Price 
FILLER 133 A PIC X(133). Filler  
Total 220    
 
 
 
 
 
 
 
 
 

---

## Page 8

Compressed Open Commitment  NDM 
3. File Transmission Layout – Compressed Open Commitment – NDM Format (Deal er Detail Rec ord) 8 
3. FILE TRANSMISSION LAYOUT – COMPRESSED OPEN 
COMMITMENT – NDM FORMAT (DEALER DETAIL 
RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-OCC- DT3- CA RD- CODE 2 N PIC 9(02). Dealer Detail Record,  Card 
Code  = '03' 
RPT-OCC- DT3-STTL-YYYY 4 N PIC 9(04). [[settlement]] Year (YYYY) 
RPT-OCC- DT3-STTL- MM 2 N PIC 9(02). [[settlement]] Month (MM) 
RPT-OCC- DT3- [[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] 
FILLER 1 A/N PIC X(01). Filler  
RPT-OCC- DT3-A CCOUNT 4 A/N PIC X(04). Account  Symbol 
RPT-OCC- DT3- TRADE- [[ID]].    Trade Number 
RPT-OCC- DT3-TRD- PFX 4 N PIC 9(04). Trade Number Prefix 
RPT-OCC- DT3-TRD- SFX 6 N PIC 9(06). Trade Number Suffix 
RPT-OCC- DT3-XREF 15 A/N PIC X(15). Internal  XREF/Trade # 
RPT-OCC- DT3- TRD-STATUS 4 A/N PIC X(04). Trade Status - FMAT, PMAT, 
PSET, FSET 
 
 
RPT-OCC- DT3- TRD-TY PE 
 
 
4 
 
 
A/N 
 
 
PIC X(04). 
Trade Type -TFTD, SBOD, 
OPTN, SBOO, SBON 
(SBOO for TBA CUSIPs  not 
eligible for  [[Novation]] only)  
RPT-OCC- DT3-BS-IND  1 A/N PIC X(01). B = Buy, S = Sell 
RPT-OCC- DT3- TRD- DATE 8 A/N PIC X(08). Trade Date (YYYYMMDD) 
RPT-OCC- DT3-STTL- DATE 8 A/N PIC X(08). [[settlement]] Date (YYYYMMDD) 
RPT-OCC- DT3-MCH-DATE 8 A/N PIC X(08). Match Date (YYYYMMDD) 
RPT-OCC- DT3-GU- DATE 8 A/N PIC X(08). Give-Up Date (YYYYMMDD) (for 
trades eligible for  [[Novation]],  this  
field  will  be blank)  
RPT-OCC- DT3- CTRA 4 A/N PIC X(04). Contra  Account  
RPT-OCC- DT3- BRKR 4 A/N PIC X(04). [[Broker]]  Account  Symbol 
RPT-OCC- DT3-STTL- PRICE 15 N PIC 9(03)V9(12). [[settlement]] Price - In Decimal 
RPT-OCC- DT3- OPEN- PAR 13 N PIC 9(11)V9(02). Open  Par Value 
RPT-OCC- DT3-STTL-VAL 13 N PIC 9(11)V9(02). [[settlement]] Value 

---

## Page 9

Compressed Open Commitment  NDM 
3. File Transmission Layout – Compressed Open Commitment – NDM Format (Deal er Detail Rec ord) 9 
Field Name Length Type Cobol Picture Description/Comments  
RPT-OCC- DT3-COMM 7 N PIC 9(05)V9(02). Commission  Amount  – as 
dollar  value 
RPT-OCC- DT3- TRD-SUB- TY PE 4 A/N PIC X(04). Trade Sub-Type  - TBA, SPT, 
STIP 
RPT-OCC- DT3-SPT- POOL- NUMBER 6 A/N PIC X(06). SPT Pool  Number 
RPT-OCC- DT3- ORIG- PA R 13 N PIC 9(11)V9(02). Original Par Value 
FILLER 53 A PIC X(53). Filler  
Total     220 
 
 
  

---

## Page 10

Compressed Open Commitment  NDM 
4. File Transmission Layout – Compressed Open Commitment – NDM Format ([[CUSIP]] CLASS FOOTER RECORD) 10 
4. FILE TRANSMISSION LAYOUT – COMPRESSED OPEN 
COMMITMENT – NDM FORMAT ([[CUSIP]] CLASS FOOTER 
RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-OCC-DT5-CARD-CODE 2 A/N PIC X(02). [[CUSIP]] Footer,  Card Code  = '05' 
RPT-OCC-DT5-STTL-YY 4 A/N PIC X(04). [[settlement]] Year (YYYY) 
RPT-OCC-DT5-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM)  
RPT-OCC-DT5-[[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] 
FILLER 1 A PIC X(01). Filler  
RPT-OCC-DT5-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
FILLER 10 A/N PIC X(10) Filler  
RPT-OCC-DT5-BOP 13 N PIC 9(11)V9(02). Buy Open  Par Value 
RPT-OCC-DT5-BCON 13 N PIC 9(11)V9(02). Buy [[settlement]] Value 
RPT-OCC-DT5-BPL 13 N PIC 9(11)V9(02). Buy Profit / Loss  
RPT-OCC-DT5-BPL-CRDR 1 A PIC X(01). Buy Profit / Loss  Indicator  
(C=Credit,  D=Debit) 
RPT-OCC-DT5-SOP 13 N PIC 9(11)V9(02). Sell Open  Par Value 
RPT-OCC-DT5-SCON 13 N PIC 9(11)V9(02). Sell [[settlement]] Value 
RPT-OCC-DT5-SPL 13 N PIC 9(11)V9(02). Sell Profit / Loss  
RPT-OCC-DT5-SPL-CRDR 1 A PIC X(01). Sell Profit / Loss  Indicator  
(C=Credit, D=Debit)  
FILLER 108 A/N PIC X(108). Filler  
  Total     220 
 
  

---

## Page 11

Compressed Open Commitment  NDM 
5. File Transmission Layout – Compressed Open Commitment – NDM Format (REPORT FOOTER RECORD) 11 
5. FILE TRANSMISSION LAYOUT – COMPRESSED OPEN 
COMMITMENT – NDM FORMAT (REPORT FOOTER 
RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-OCC-DT6-CARD-CODE 2 A/N PIC X(02). Report  Footer,  Card Code  = '06' 
FILLER 16 A/N PIC X(16) Filler  
RPT-OCC-DT6-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
FILLER 10 A/N PIC X(10) Filler  
RPT-OCC-DT6-FW-BUY-ITM 4 A/N PIC X(04). Forward  Buy Item Count  
RPT-OCC-DT6-FW-BUY-OPAR 13 N PIC 9(11)V9(02). Forward  Buy Open  Par Value 
RPT-OCC-DT6-FW-BUY-STTL 13 N PIC 9(11)V9(02). Forward  Buy [[settlement]] Value 
RPT-OCC-DT6-FW-SEL-ITM 4 A/N PIC X(04). Forward  Sell Item Count  
RPT-OCC-DT6-FW-SEL-OPAR 13 N PIC 9(11)V9(02). Forward  Sell Open  Par Value 
RPT-OCC-DT6-FW-SEL-STTL 13 N PIC 9(11)V9(02). Forward  Sell [[settlement]] Value 
RPT-OCC-DT6-FL-BUY-ITM 4 A/N PIC X(04). Fail Buy Item Count  
RPT-OCC-DT6-FL-BUY-OPAR 13 N PIC 9(11)V9(02). Fail Buy Open  Par Value 
RPT-OCC-DT6-FL-BUY-STTL 13 N PIC 9(11)V9(02). Fail Buy [[settlement]] Value 
RPT-OCC-DT6-FL-SEL-ITM 4 A/N PIC X(04). Fail Sell Item Count  
RPT-OCC-DT6-FL-SEL-OPAR 13 N PIC 9(11)V9(02). Fail Sell Open  Par Value 
RPT-OCC-DT6-FL-SEL-STTL 13 N PIC 9(11)V9(02). Fail Sell [[settlement]] Value 
RPT-OCC-DT6-AF-BUY-ITM 4 A/N PIC X(04). Aged Fail Buy Item Count  
RPT-OCC-DT6-AF-BUY-OPAR 13 N PIC 9(11)V9(02). Aged Fail Buy Open  Par Value 
RPT-OCC-DT6-AF-BUY-STTL 13 N PIC 9(11)V9(02). Aged Fail Buy [[settlement]] Value 
RPT-OCC-DT6-AF-SEL-ITM 4 A/N PIC X(04). Aged Fail Sell Item Count  
RPT-OCC-DT6-AF-SEL-OPAR 13 N PIC 9(11)V9(02). Aged Fail Sell Open  Par Value 
RPT-OCC-DT6-AF-SEL-STTL 13 N PIC 9(11)V9(02). Aged Fail Sell [[settlement]] Value 
FILLER 8 A/N PIC X(08). Filler  
  Total     220 
 
  

---

## Page 12

Compressed Open Commitment  NDM 
6. File Transmission Layout – Compressed Open Commitment – NDM Format ([[Broker]] DETAIL RECORD) 12 
6. FILE TRANSMISSION LAYOUT – COMPRESSED OPEN 
COMMITMENT – NDM FORMAT ([[Broker]] DETAIL 
RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-OCC- DT7- CA RD- CODE 2 N PIC 9(02). [[Broker]]  Detail Record,  Card Code  
= '07' 
RPT-OCC- DT7-STTL-YYYY 4 N PIC 9(04). [[settlement]] Year (YYYY) 
RPT-OCC- DT7-STTL- MM 2 N PIC 9(02). [[settlement]] Month (MM) 
RPT-OCC- DT7- [[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] 
FILLER 1 A/N PIC X(01). Filler  
RPT-OCC- DT7-A CCOUNT 4 A/N PIC X(04). Account  Symbol 
RPT-OCC- DT7- TRADE- [[ID]].    Trade Number 
RPT-OCC- DT7-TRD- PFX 4 N PIC 9(04). Trade Number Prefix 
RPT-OCC- DT7-TRD- SFX 6 N PIC 9(06). Trade Number Suffix 
RPT-OCC- DT7-XR EF 15 A/N PIC X(15). Internal  XREF/Trade # 
RPT-OCC- DT7- TRD-STATUS 4 A/N PIC X(04). Trade Status - FMAT, PMAT, 
PSET, FSET 
RPT-OCC- DT7- TRD-TY PE 4 A/N PIC X(04). Trade Type  - TFTD,SBOD 
RPT-OCC- DT7- TRD- DATE 8 A/N PIC X(08). Trade Date (YYYYMMDD) 
RPT-OCC- DT7-STTL- DATE 8 A/N PIC X(08). [[settlement]] Date (YYYYMMDD) 
RPT-OCC- DT7-MCH-DATE 8 A/N PIC X(08). Match Date (YYYYMMDD) 
RPT-OCC- DT7-GVUP-DATE 8 A/N PIC X(08). Give-Up Date (YYYYMMDD) (for 
trades eligible  for [[Novation]],  this  
field  will be blank)  
RPT-OCC- DT7-BUY 4 A/N PIC X(04). Buy Dealer Account  Symbol 
RPT-OCC- DT7- SELL 4 A/N PIC X(04). Sell Dealer Account  Symbol 
RPT-OCC- DT7-STTL- PRICE 15 N PIC 9(03)V9(12). [[settlement]] Price - In Decimal 
RPT-OCC- DT7- OPEN- PAR 13 N PIC 9(11)V9(02). Open  Par Value 
RPT-OCC- DT7-STTL-VAL 13 N PIC 9(11)V9(02). [[settlement]] Value 
RPT-OCC- DT7-BUY- COMM 7 N PIC 9(05)v9(02) Buy Dealer Commission  – In 
Decimal 
RPT-OCC- DT7-SELL- COMM 7 N PIC 9(05)v9(02) Sell Dealer Commission  – In 
Decimal 

---

## Page 13

Compressed Open Commitment  NDM 
6. File Transmission Layout – Compressed Open Commitment – NDM Format ([[Broker]] DETAIL RECORD) 13 
Field Name Length Type Cobol Picture Description/Comments  
RPT-OCC- DT7- TRD-SUB- TY PE 4 A/N PIC X(04). Trade Sub-Type  - TBA, SPT, 
STIP 
RPT-OCC- DT7-SPT- POOL- NUMBER 6 A/N PIC X(06). SPT Pool  Number 
RPT-OCC- DT7- ORIG- PA R 13 N PIC 9(11)V9(02). Original Par Value 
FILLER 47 A/N PIC X(47). Filler  
Total     220  
 
  

---

## Page 14

Compressed Open Commitment  NDM 
7. File Transmission Layout – Compressed Open Commitment – NDM Format (Trailer) 14 
7. FILE TRANSMISSION LAYOUT – COMPRESSED OPEN 
COMMITMENT – NDM FORMAT (TRAILER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-OCC- DT99- CARD- CODE  2 N PIC 9(02). Trailer  Record,  Card Code  = '99' 
FILLER 13 A PIC X(13). Filler  
RPT-OCC- DT99-ACCT 4 A/N PIC X(04). Account  Symbol 
FILLER 1 A PIC X(01). Filler  
RPT-OCC- DT99-LOGICAL- COUNT 7 N PIC 9(07). Logical  Record  Count  
FILLER 1 A PIC X(01). Filler  
RPT-OCC- DT99- PHYSICAL- COUNT 7 N PIC 9(07). Physical  Record  Count  
FILLER 185 A PIC X(185). Filler  
Total     220        
    

---

## Page 15

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 