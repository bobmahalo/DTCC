---
title: "File Transmission Layout: DNA Status NDM"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs129_file_trans_layout_dna_status_ndm.pdf"
pages: 10
size: "296.8 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# File Transmission Layout: DNA Status NDM

**Original File:** [mbs129_file_trans_layout_dna_status_ndm.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs129_file_trans_layout_dna_status_ndm.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 296.8 KB  

---

## Page 1

 
 
 
[[FICC]] - MBSD 
FILE TRANSMISSION LAYOUT – DNA STATUS NDM FORMAT 
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
Publication Code: MBS129 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout –  DNA Status NDM Format  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction to the Documentation.................................................................................................... 4 
Purpose ....................................................................................................................................... 4 
Frequency .................................................................................................................................... 4 
Recor d La you t .............................................................................................................................. 4 
Version C on tr ol ............................................................................................................................. 5 
1. File Transmission Layout – DNA Status – NDM Format (ACCOUNT / REPORT HEADER)................... 6 
2. File Transmission Layout – DNA Status – NDM Format (DNA REQUEST DETAIL) ............................. 7 
3. File Transmission Layout – DNA Status – NDM Format (DNA TRADE ASSIGNMENT DETAIL) ............ 8 
4. File Transmission Layout – DNA Status – NDM Format (TRAILER)................................................... 9 
 

---

## Page 4

DNA Status NDM 
Introduction to the Doc umentation 4 
INTRODUCTION TO THE DOCUMENTATION 
Purpose 
This report will show all DNA requests active in the system or processed/cancelled on the current business 
day. For each DNA request, it will show the DNA status, the individual trades that [[FICC]] has assigned the DNA 
request to and any associated money differences (DNA TAP). 
Frequency 
Daily. 
Record Layout 
*All records are of equal length - 228 bytes. 
*There are 7 different record types, each uniquely identified by card code, as follows: card codes 01 through 
03, & 99. 
 
ACCOUNT / REPORT HEADER RECORD (CARD CODE 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
 
DNA REQUEST DETAIL RECORD (CARD CODE 02) 
Detail record containing a single DNA request record. 
 
DNA TRADE ASSIGNMENT DETAIL RECORD (CARD CODE 03) 
Detail record containing a single DNA trade assignment record. 
TRAILER CONTROL RECORD (CARD CODE 99) 
Trailer record indicates the end of the report for the recipient account. 
 
Sample File 
*Sample file provide d after Record Layouts section. 
 
 
 
 

---

## Page 5

DNA Status NDM 
Introduction to the Doc umentation 5 
Version Control 
Date Version # Name Description of Change  
7/16/2015 1.0 C. Swords  • Initial  version  
10/12/2015 1.01 C. Swords  Made following  updates: 
• Add Card Code  02, field  RPT-DNA2-DNA-TAP-CRDR 
(TAP Indicator)  
8/4/2016 1.02 C. Swords  Made following  updates:  
• Update  description  to co rrectly indicate that 4 
record  types,  not 3. 
• Ad d standard  title page  and  revision  his tor y. 
04/04/2022 1.03 J. Sheeran  Updated to latest [[DTCC]] B randing  
    
 

---

## Page 6

DNA Status NDM 
1. File Transmission Layout – DNA Status – NDM Format (ACCOUNT / REPORT HEADER) 6 
1. FILE TRANSMISSION LAYOUT – DNA STATUS – NDM 
FORMAT (ACCOUNT / REPORT HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-DNA1-CARD-CODE 2 N PIC 9(02) Header R ecord, Card code  = ‘01’ 
RPT-DNA1-RPT-[[ID]] 8 A/N PIC X(08) Report  [[ID]] = ‘MB8103-N’ 
     RPT-DNA1-ACC-AGG-[[ID]]     
     RPT-DNA1-PART-[[ID]] 3 N PIC 9(03) [[participant]]  [[ID]] 
RPT-DNA1-AGG 2 N PIC 9(02) Aggregate  
RPT-DNA1-ACCT 4 A PIC X(04) Account  Symbo l 
RPT-DNA1-PART-NAME 40 A/N PIC X(40) [[participant]]  Name 
RPT-DNA1-BUS-DATE 8 N PIC 9(08) Date of R eport 
FILLER 161 A PIC X(161) Filler  
Total     228 

---

## Page 7

DNA Status NDM 
2. File Transmission Layout – DNA Status – NDM Format (DNA REQUEST DETAIL) 7 
2. FILE TRANSMISSION LAYOUT – DNA STATUS – NDM 
FORMAT (DNA REQUEST DETAIL) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-DNA2-CARD-CODE 2 N PIC 9(02) DNA Reques t Detail R ecord, Card 
code  = ‘02’ 
RPT-DNA2-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-DNA2-ACCT 4 A/N PIC X(04) Account  
RPT-DNA2-DNA-[[ID]] 10 N PIC 9(10) DNA [[ID]] 
    RPT-DNA2-XREF 16 A/N PIC X(16)     DNA  R ef erence N um ber (provided by     
[[Member]]) 
    RPT-DNA2-STTL-DATE 8 N PIC 9(08) Settle m en t Date (YYYYM M D D) 
RPT-DNA2-STATUS 4 A/N PIC X(04) Status : ASGN, CANC, STLD 
RPT-DNA2-DNA-TAP 17 N PIC 9(15)V9(02)  DNA TAP 
RPT-DNA2-DNA-TAP-CRDR 1 A PIC X(01) TAP I ndicat or (C=Cr ed i t, D=De b it) 
FILLER 82 A PIC X(82) Filler  
Total 228    
 
 
 
 
 
 
 
 
 

---

## Page 8

DNA Status NDM 
3. File Transmission Layout – DNA Status – NDM Format (DNA TRADE ASSIGNMENT DETAIL) 8 
3. FILE TRANSMISSION LAYOUT – DNA STATUS – NDM 
FORMAT (DNA TRADE ASSIGNMENT DETAIL) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-DNA3-CARD-CODE 2 N PIC 9(02) DNA Trad e Assignment Detail 
Record, Card code = ‘03’ 
RPT-DNA3-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-DNA3-ACCT 4 A/N PIC X(04) Account  
RPT-DNA3-DNA-[[ID]] 10 N PIC 9(10) DNA [[ID]] 
RPT-DNA3-XREF 16 A/N PIC X(16) DNA Referenc e Number 
(provided by  [[Member]]) 
RPT-DNA3-DT3-TRADE-[[ID]]    Trade Number 
     RPT-DNA3-DT3-TRD-PFX 4 N PIC 9(04). Trade Number Prefix 
     RPT-DNA3-DT3-TRD-SFX 6 N PIC 9(06). Trad e Number Suffix 
RPT-DNA3-TRADE-TYPE 4 A/N PIC X(04) Trad e Typ e-TFTD, SBON 
RPT-DNA3-BS-IND 1 A PIC X(01) Buy/Sell Code, B=Buy, S = Sell 
RPT-DNA3-TRD-DATE 8 N PIC 9(08) Trad e Date (YYYYMMDD) 
RPT-DNA3-STTL-DATE 8 N PIC 9(08) [[settlement]] Date (YYYYMMDD) 
RPT-DNA3-PRICE 15 N PIC 9(03)V9(12) Price – In Decimal 
RPT-DNA3-ORIG-TRD-PAR 17 N PIC 9(15)V9(02) Original Trade Par 
RPT-DNA3-DNA-PAR 17 N PIC 9(15)V9(02) DNA Par Amount 
RPT-DNA3-DNA-STTL-VAL 15 N PIC 9(13)V9(02) DNA [[settlement]] Value 
FILLER 66 A PIC X(66) Filler 
Total     228 
 
 
  

---

## Page 9

DNA Status NDM 
4. File Transmission Layout – DNA Status – NDM Format (TRAILER) 9 
4. FILE TRANSMISSION LAYOUT – DNA STATUS – NDM 
FORMAT (TRAILER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-DNA99-CARD-CODE 2 N PIC 9(02) Trailer  Record, Card Code = '99' 
FILLER 13 A PIC X(13) Filler  
RPT-DNA99-ACCT 4 A/N PIC X(04) Account  Symbol 
FILLER 1 A PIC X(01) Filler  
RPT-DNA99-LOGICAL-COUNT 7 N PIC 9(07) Logical  Record Count 
FILLER 1 A PIC X(01) Filler  
RPT-DNA99-PHYSICAL-COUNT 7 N PIC 9(07) Physical  Reco rd C ount 
FILLER 193 A PIC X(193) Filler  
  Total     228  

---

## Page 10

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 