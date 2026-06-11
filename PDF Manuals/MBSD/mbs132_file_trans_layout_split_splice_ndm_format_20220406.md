---
title: "File Transmission Layout: Split/Splice NDM Layout"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs132_file_trans_layout_split_splice_ndm_format_20220406.pdf"
pages: 9
size: "287.0 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# File Transmission Layout: Split/Splice NDM Layout

**Original File:** [mbs132_file_trans_layout_split_splice_ndm_format_20220406.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs132_file_trans_layout_split_splice_ndm_format_20220406.pdf)  
**Category:** MBSD  
**Total Pages:** 9  
**File Size:** 287.0 KB  

---

## Page 1

 
 
 
[[FICC]] - MBSD 
FILE TRANSMISSION LAYOUT: SPLIT/SPLICE NDM LAYOUT 
VERSION 1.01 
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
Publication Code: MBS132 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout -  Split/Splice NDM Layout  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction to the Documentation.................................................................................................... 4 
Purpose ....................................................................................................................................... 4 
Frequency .................................................................................................................................... 4 
Recor d La you t .............................................................................................................................. 4 
Version C on tr ol ............................................................................................................................. 5 
1. File Transmission Layout – Split/Splice – NDM Layout (HEADER).................................................... 6 
2. File Transmission Layout – Split/Splice – NDM Layout (Split Splice DETAIL Record) ........................ 7 
3. File Transmission Layout – Split/Splice – NDM Layout (TRAILER) ................................................... 8 
 

---

## Page 4

Split/Splice NDM Layout  
Introduction to the Doc umentation 4 
INTRODUCTION TO THE DOCUMENTATION 
Purpose 
The Split / Splice Report reflects trades involved in a split/splice operation, including the original transactions 
canceled and replacement trades generated. 
Frequency 
Daily. 
Record Layout 
*All records are of equal length - 228 bytes. 
*There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
 
ACCOUNT / REPORT HEADER RECORD (CARD CODE 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
 
DEALER DETAIL RECORD (CARD CODE 02) 
Detail record containing split/splice activities. 
 
TRAILER CONTROL RECORD (CARD CODE 99) 
Trailer record indicates the end of the report for the recipient account. 
 
 
 
 
 
 
 
 
 

---

## Page 5

Split/Splice NDM Layout  
Introduction to the Doc umentation 5 
Version Control 
Date Version # Name Description of Change  
8/4/2015 1.0 C. Swords  Initial  version  
04/04/2022 1.01 J. Sheeran Updated [[DTCC]] branding template 
 

---

## Page 6

Split/Splice NDM Layout  
Introduction to the Doc umentation 6 
1. FILE TRANSMISSION LAYOUT – SPLIT/SPLICE – NDM 
LAYOUT (HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-SS1-CARD-CODE 2 N PIC 9(02) Header Record, Card Code  = '01' 
RPT-SS1-RPT-[[ID]] 8 A/N PIC X(08) R eport [[ID]] = 'M B8109- N’ 
RPT-SS1-ACC-AGG-[[ID]]     
RPT-SS1-PART 3 N PIC 9(03) [[participant]]  [[ID]] 
RPT-SS1-AGG 2 A/N PIC 9(02) Aggregate  
RPT-SS1-ACCT 4 A/N PIC X(04) Account  Symbol 
RPT-SS1-[[participant]]-NAME 40 A/N PIC X(40) [[participant]]  Name 
RPT-SS1-BUS-DATE 8 A/N PIC X(08) Date of R eport (YYYYMM D D)  
FILLER 161 A PIC X(161) Filler  
Total     228 

---

## Page 7

Split/Splice NDM Layout  
Introduction to the Doc umentation 7 
2. FILE TRANSMISSION LAYOUT – SPLIT/SPLICE – NDM 
LAYOUT (SPLIT SPLICE DETAIL RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-SS2-CARD-CODE 2 N PIC 9(02) Split / Splice  Detail R ecord, Card 
Code  = '02' 
RPT-SS2-[[CUSIP]] 9 A/N PIC X(09) [[CUSIP]] 
RPT-SS2-ACCT 4 A/N PIC X(04) Account  Symbol 
RPT-SS2-SS-OPERATION_ID 16 A/N     PIC X(16) Split Splice  Operation  [[ID]] 
RPT-SS2-ACTIVITY 4 A/N PIC X(04) Activity  Type  
•    SPCX(for  original  dealer  trades  
canceled)  
• SPCR (fo r replacement  trades  
created)  
RPT-SS2-TRAN-TRADE-[[ID]] 10 N PIC 9(10) Transaction Number (for canceled trades) 
or Trade Number (for  replacement  
trades)  
RPT-SS2-SUB-INTERNAL-
XREF 
15 A/N PIC X(15) In tern al XREF /T rad e # 
RPT-SS2-TRADE-TYPE 4 A/N PIC X(04) Trade  Type -TFTD,  SBOD 
RPT-SS2-BS-INDICATOR 1 A/N PIC X(01) B = Buy, S = Sell 
RPT-SS2-TRADE-DATE 8 N PIC 9(08) Trade  Date (YYYYMM D D)  
RPT-SS2-MATCH-DATE 8 N PIC 9(08) Match Date (YYYYMM D D)  
RPT-SS2-SETTL-DATE 8 N PIC 9(08) Settle m en t Date  (YYYYM M D D) 
RPT-SS2-FMAT-PMAT 4 A/N PIC X(04) Match Status fo r replacemen t trades; FMAT 
or PMAT 
RPT-SS2-CONTRA-ACCT 4 A/N PIC X(04) Contra  Account  
RPT-SS2-DLR-PRICE 15 N PIC 9(03)V9(12)  Trade  Price - In Decimal  
RPT-SS2-PAR-VALUE 13 N PIC 9(11)V9(02)  Par Value  
RPT-SS2-TRD-SUB-TYPE 4 N     PIC X(04) Trade  Sub-Typ e = blank  or TBA 
FILLER 99 A PIC X(99) Filler  
     
     
Total 228    
 
 

---

## Page 8

Split/Splice NDM Layout  
Introduction to the Doc umentation 8 
3. FILE TRANSMISSION LAYOUT – SPLIT/SPLICE – NDM 
LAYOUT (TRAILER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-RPC99-CARD-CODE 2 N PIC 9(02) Trailer  Record, Card Code = '99' 
FILLER 13 A PIC X(13) Filler  
RPT-RPC99-ACCT 4 A/N PIC X(04) Account  Symbol 
FILLER 1 A PIC X(01) Filler  
RPT-RPC99-LOGICAL-COUNT 7 N PIC 9(07) Logical  Record Count 
FILLER 1 A PIC X(01) Filler  
RPT-RPC99-PHYSICAL-COUNT 7 N PIC 9(07) Physical  Reco rd C ount 
FILLER 193 A PIC X(193) Filler  
Total     228 
 

---

## Page 9

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 