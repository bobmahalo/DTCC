---
title: "File Transmission Layout: TBA Reprice and Variance NDM Layout"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs134_file_trans_layout_tba_repr_var_ndm_format.pdf"
pages: 10
size: "294.3 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# File Transmission Layout: TBA Reprice and Variance NDM Layout

**Original File:** [mbs134_file_trans_layout_tba_repr_var_ndm_format.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs134_file_trans_layout_tba_repr_var_ndm_format.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 294.3 KB  

---

## Page 1

 
 
 
[[FICC]] - MBSD 
FILE TRANSMISSION LAYOUT - TBA REPRICE AND VARIANCE NDM LAYOUT 
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
Publication Code: MBS134 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout -  TBA Reprice and Variance NDM Layout  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction to the Documentation.................................................................................................... 4 
Purpose ....................................................................................................................................... 4 
Frequency .................................................................................................................................... 4 
Recor d La you t .............................................................................................................................. 4 
Version C on tr ol ............................................................................................................................. 5 
1. File Transmission Layout – TBA Reprice – NDM Layout (HEADER).................................................. 6 
2. File Transmission Layout – TBA Reprice – NDM Layout (TBA REPRICE DETAIL RECORD) ............... 7 
3. File Transmission Layout – TBA Reprice – NDM Layout (TBA VARIANCE DETAIL RECORD)............. 8 
4. File Transmission Layout – TBA Reprice – NDM Layout (TRAILER) ................................................. 9 
 

---

## Page 4

TBA Reprice and Variance NDM 
Introduction to the Doc umentation 4 
INTRODUCTION TO THE DOCUMENTATION 
Purpose 
Reflects the TBA trade reprice activity occurring on the current business day. This report will allow members to 
reconcile [[FICC]] reprice activity and any associated money differences. 
Frequency 
Per SIFMA Calendar on 24hr day 
Record Layout 
*All records are of equal length - 228 bytes 
*There are 4 different record types, each uniquely identified by card code, as follows; card codes 01 through 
03, & 99. 
*The end of the report is signified by the 99 or “trailer” record. 
 
ACCOUNT / REPORT HEADER RECORD (CARD CODE 01) 
Control record which signified the beginning of the report for a given account. Contains recipient account and 
report identification items. 
 
TBA REPRICE DETAIL RECORD (CARD CODE 02) 
Detail record containing reprice activities and money differences. 
 
TBA VARIANCE DETAIL RECORD (CARD CODE 03) 
Detail record containing allocation variance information and associated money differences. 
 
TRAILER CONTROL RECORD (CARD CODE 99) 
Trailer record indicates the end of the report for the recipient account. 
 
 
  

---

## Page 5

TBA Reprice and Variance NDM 
Introduction to the Doc umentation 5 
Version Control 
Date Version #  Name Description of Change  
7/16/2015 1.0 C. Swords  Initial  version  
10/12/2016 1.01 C. Swords  Made following  updates:  
Add Card Code 02, field  RPT-RPC2-DT3-RPC-TAP-CRDR 
(TAP Indicator)  
8/4/2016 1.02 C. Swords  Made following  updates:  
Add Card Code  03 TBA Variance Detail Record  to provide  
information on variance TAP. 
3/25/2022 1.03 J.Sheeran  Updated template 
 

---

## Page 6

TBA Reprice and Variance NDM 
Introduction to the Doc umentation 6 
1. FILE TRANSMISSION LAYOUT – TBA REPRICE – NDM 
LAYOUT (HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-RPC1-CARD-CODE 2 N PIC 9(02) Header Record, Card Code  = '01' 
RPT-RPC1-RPT-[[ID]] 8 A/N PIC X(08) R eport [[ID]] = 'M B8106- N’ 
RPT-RPC1-ACC-AGG-[[ID]]     
RPT-RPC1-PART 3 N PIC 9(03) [[participant]]  [[ID]] 
RPT-RPC1-AGG 2 A/N PIC 9(02) Aggregate  
RPT-RPC1-ACCT 4 A/N PIC X(04) Account  Symbol 
RPT-RPC1-[[participant]]-NAME 40 A/N PIC X(40) [[participant]]  Name 
RPT-RPC1-BUS-DATE 8 A/N PIC X(08) Date of R eport (YYYYMM D D)  
FILLER 161 A PIC X(161) Filler  
Total     228 

---

## Page 7

TBA Reprice and Variance NDM 
Introduction to the Doc umentation 7 
2. FILE TRANSMISSION LAYOUT – TBA REPRICE – NDM 
LAYOUT (TBA REPRICE DETAIL RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-RPC2-CARD-CODE 2 N PIC 9(02) TBA Reprice Detail Record, Card 
Code = '02' 
RPT-RPC2-[[CUSIP]] 9 A/N PIC X(09) [[CUSIP]] 
RPT-RPC2-ACCOUNT 4 A/N PIC X(04) Account  Symbol 
RPT-RPC2-TRADE-[[ID]].    Trade Number 
RPT-RPC2-TRD-PFX 4 N PIC 9(04) Trade  N um ber Prefix 
RPT-RPC2-TRD-SFX 6 N PIC 9(06) Trade  Number  Suffix 
RPT-RPC2-XREF 15 A/N PIC X(15) In tern al XREF /T rad e # 
RPT-RPC2-TRD-TYPE 4 A/N PIC X(04) Trade  Type -TFTD,  SBON 
RPT-RPC2-TRD-SUB-TYPE 4 A/N PIC X(04) Trade  Sub-Typ e - TBA 
RPT-RPC2-BS-IND 1 A/N PIC X(01) B = Buy, S = Sell 
RPT-RPC2-TRD-DATE 8 A/N PIC X(08) Trade  Date (YYYYMM D D)  
RPT-RPC2-STTL-DATE 8 A/N PIC X(08) Settle m en t Date (YYYYM M D D) 
RPT-RPC2-CTRA 4 A/N PIC X(04) Contra  Account  
RPT-RPC2-PRICE 15 N PIC 9(03)V9(12)  Trade/[[settlement]]  Price 
RPT-RPC2-OPEN-PAR 13 N PIC 9(11)V9(02)  Open  Par Value 
RPT-RPC2-STTL-VAL 13 N PIC 9(11)V9(02)  [[settlement]] Value 
RPT-RPC2-REPL-TRADE-[[ID]].    Replacement  Trade Number 
RPT-RPC2-REPL-TRD-
PFX 
4 N PIC 9(04) Replacement  Trade Number Prefix 
RPT-RPC2-REPL-TRD-
SFX 
6 N PIC 9(06) Replacement  Trade Number Suffix 
RPT-RPC2-REPL-PRICE 15 N PIC 9(03)V9(12)  Replacement  Trade/System  Price 
RPT-RPC2-REPL-STTL-VAL 13 N PIC 9(11)V9(02)  Replacement  Trade [[settlement]] Value 
RPT-RPC2-RPC-TAP 17 N PIC 9(15)V9(02)  Reprice TAP 
RPT-RPC2-RPC-TAP-CRDR 1 A PIC X(1) TAP I ndicat or (C=Cr ed i t, D=De b it) 
RPT-RPC2-FILLER 62 N PIC X(62) Filler  
Total 228    
 
 
 
 
 
 

---

## Page 8

TBA Reprice and Variance NDM 
Introduction to the Doc umentation 8 
3. FILE TRANSMISSION LAYOUT – TBA REPRICE – NDM 
LAYOUT (TBA VARIANCE DETAIL RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-RPC3-CARD-CODE 2 N PIC 9(02) TBA Varianc e Detail R ecord, Card 
Code = '03' 
RPT-RPC3-[[CUSIP]] 9 A/N PIC X(09) [[CUSIP]] 
RPT-RPC3-ACCOUNT 4 A/N PIC X(04) Account  Symbol 
RPT-RPC3-TRADE-[[ID]].    Trade Number 
RPT-RPC3-TRD-PFX 4 N PIC 9(04) Trade  N um ber Prefix 
RPT-RPC3-TRD-SFX 6 N PIC 9(06) Trade  Number  Suffix 
RPT-RPC3-XREF 15 A/N PIC X(15) In tern al XREF /T rad e # 
RPT-RPC3-TRD-TYPE 4 A/N PIC X(04) Trade  Type -TFTD,  SBON 
RPT-RPC3-TRD-SUB-TYPE 4 A/N PIC X(04) Trade  Sub-Typ e - TBA 
RPT-RPC3-BS-IND 1 A/N PIC X(01) B = Buy, S = Sell 
RPT-RPC3-TRD-DATE 8 A/N PIC X(08) Trade  Date (YYYYMM D D)  
RPT-RPC3-STTL-DATE 8 A/N PIC X(08) Settle m en t Date (YYYYM M D D) 
RPT-RPC3-CTRA 4 A/N PIC X(04) Contra  Account  
RPT-RPC3-PRICE 15 N PIC 9(03)V9(12)  Trade/[[settlement]]  Price 
RPT-RPC3-VAR-PAR 13 N PIC 9(11)V9(02)  Variance Par Value 
RPT-RPC3-VAR-PAR-OU-IND 1 A PIC X(1) Variance Par I ndicat or (O=Ov er, 
U=Under)  
RPT-RPC2-REPL-PRICE 15 N PIC 9(03)V9(12)  Replacement  Trade/System  Price 
RPT-RPC3-RPC-TAP 17 N PIC 9(15)V9(02)  Variance TAP 
RPT-RPC3-RPC-TAP-CRDR-IND 1 A PIC X(1) TAP I ndicat or (C=Cr ed i t, D=De b it) 
RPT-RPC3-FILLER 97 N PIC X(97) Filler  
Total      228 

---

## Page 9

TBA Reprice and Variance NDM 
Introduction to the Doc umentation 9 
4. FILE TRANSMISSION LAYOUT – TBA REPRICE – NDM 
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

## Page 10

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 