---
title: "MBSD File Transmission Layout: Pool Obligation Factor Update NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs162_pool_oblig_factor_upd_ndm.pdf"
pages: 9
size: "292.8 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD File Transmission Layout: Pool Obligation Factor Update NDM Format

**Original File:** [mbs162_pool_oblig_factor_upd_ndm.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs162_pool_oblig_factor_upd_ndm.pdf)  
**Category:** MBSD  
**Total Pages:** 9  
**File Size:** 292.8 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
MBSD FILE TRANSMISSION LAYOUT: 
POOL OBLIGATION FACTOR UPDATE NDM FORMAT 
VERSION 1.02 
APRIL 04, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: April 4, 2022 
Publication Code: MBS162 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout –  Pool Obligation Factor Update  NDM Format 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control ............................................................................................................................... 4 
Introduction to the Documentation.................................................................................................... 5 
Purpose ....................................................................................................................................... 5 
Frequency .................................................................................................................................... 5 
Recor d La you t .............................................................................................................................. 5 
1. File Transmission Layout:  CCP Pool Obligation Factor Update – NDM Format (HEADER) ................ 6 
2. File Transmission Layout: CCP Pool Obligation Factor Update – NDM Format (POOL OBLIGATION 
FACTOR UPDATE DETAIL RECORD).................................................................................................  7 
3. File Transmission Layout: CCP Pool Obligation Factor Update – NDM Format (TRAILER) ................. 8 
 
 
  

---

## Page 4

 
 
VERSION CONTROL 
Date Version # Name Description of Change  
07/16/2015 1.0 C. Swords  • Initial  version  
08/24/2016 1.01 C. Swords  Made following  updates:  
• In Card Code  02 (POOL OBLIGATION FACTOR 
UPDATE DETAIL RECORD), added  credit/debit  
TAP indicator.  
Add title page  and  revision histor y 
04/04/2022 1.02 J. Sheeran  Updated to latest [[DTCC]] branding  
n/a n/ [[DTCC]] Learning  Updated to latest [[DTCC]] branding  
 
  

---

## Page 5

CCP Pool Obligation Factor Update NDM  
Introduction to the Doc umentation 5 
INTRODUCTION TO THE DOCUMENTATION 
Purpose 
This report will reflect [[FICC]] calculated cash differences due to factor updates for all previously settled Pool 
[[obligations]] (“POID’s) with a Contractual [[settlement]] Date (“ CSD”) in blackout period. This report will allow 
members to reconcile the money differences based on the factor updates. 
Frequency 
Daily. 
Record Layout 
*All records are of equal length - 228 bytes. 
*There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
 
ACCOUNT / REPORT HEADER RECORD (CARD CODE 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
 
POOL OBLIGATION FACTOR UPDATE DETAIL RECORD (CARD CODE 02) 
Detail record containing a single pool obligation updated due to factor changes. 
 
TRAILER CONTROL RECORD (CARD CODE 99) 
Trailer record indicates the end of the report for the recipient account. 
 
  

---

## Page 6

CCP Pool Obligation Factor Update NDM  
Introduction to the Doc umentation 6 
1. FILE TRANSMISSION LAYOUT:  
CCP POOL OBLIGATION FACTOR UPDATE – NDM 
FORMAT (HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-FAC01-CARD-CODE 2 N PIC 9(02) Header R ecord, Card code  = ‘01’ 
RPT-FAC01-RPT-[[ID]] 8 A/N PIC X(08) Report  [[ID]] = “MB8107-N” 
RPT-FAC01-ACC-AGG-[[ID]]     
     RPT-FAC01-PART-[[ID]] 3 N PIC 9(03) [[participant]]  [[ID]] 
     RPT-FAC01-AGG 2 N PIC 9(02) Aggregate  
RPT-FAC01-ACCT 4 A PIC X(04) Account  Symbo l 
RPT-FAC01-PART-NAME 40 A/N PIC X(40) [[participant]]  Name 
RPT-FAC01-BUS-DATE 8 N PIC 9(08) Date of R eport 
FILLER 171 A PIC X(171) Filler  
Total     228 

---

## Page 7

CCP Pool Obligation Factor Update NDM  
Introduction to the Doc umentation 7 
2. FILE TRANSMISSION LAYOUT: 
CCP POOL OBLIGATION FACTOR UPDATE – NDM 
FORMAT (POOL OBLIGATION FACTOR UPDATE 
DETAIL RECORD) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-FAC02-CARD-CODE 2 N PIC 9(02) Card C ode =‘02’ 
RPT-FAC02-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-FAC02-ACCT 4 A PIC X(04) Account  Symbo l 
    RPT-FAC02-POOL-NUMBER 6 A/N PIC X(06) Pool  Number 
    RPT-FAC02-POOL-[[CUSIP]] 9 A/N PIC X(09) Pool  [[CUSIP]] 
RPT-FAC02-POID 14 N PIC 9(14) Pool  Obligation  [[ID]] 
RPT-FAC02-BUY-SELL-CODE 1 N PIC X(01) Buy/Sell  C ode, B=Buy, S=Sell 
RPT-FAC02-TRD-DATE 8 N PIC 9(08) Trade  Date (YYYYM M DD)  
RPT-FAC02-SETTL-DATE 8 N PIC 9(08) Settle m en t Date (YYYYM M D D) 
RPT-FAC02-DLVRY-DATE 8 N PIC 9(08) Delivery  Date (YYYYMM D D)  
RPT-FAC02-CONTRA-[[ID]] 4 A PIC X(04) C ont ra [[ID]] 
RPT-FAC02-ORIG-FACE 15 N PIC 9(15) Original Face  
RPT-FAC02-CURR-FACE 17 N PIC 9(15)V9(02)  Current Face 
RPT-FAC02-PRICE 15 N PIC 9(03)V9(12)  Trade Price 
RPT-FAC02-ACT-CLEAR-
MONEY 
15 N PIC 9(13)V9(02)  Actual Clearanc e M oney 
RPT-FAC02-ACT-PREV-
FACTOR 
12 N PIC 9(3)V9(9)  Previous  Factor 
RPT-FAC02-UPD-FACTOR 12 N PIC 9(3)V9(9)  Updated  Facto r 
RPT-FAC02-CURR-FACE-
REVISED 
17 N PIC 9(15)V9(02)  Revised  Current Face using updated  
factor 
RPT-FAC02-NET-MONEY-
REVISED 
15 N PIC 9(13)V9(02)  Revised  Net M oney using  updated  facto r 
RPT-FAC02-TAP 15 N PIC 9(13)V9(02)  Transaction  Adjustmen t  Paymen t (TAP) 
due to differenc e in Actual Net Money  and  
Revised  Net M oney. 
RPT-FAC02-TAP-CRDR 1 A PIC X(1) TAP I ndicat or (C=Cr ed i t, D=De b it) 
FILLER 29 A PIC X(29) Filler  
Total 228    

---

## Page 8

CCP Pool Obligation Factor Update NDM  
Introduction to the Doc umentation 8 
3. FILE TRANSMISSION LAYOUT: 
CCP POOL OBLIGATION FACTOR UPDATE – NDM 
FORMAT (TRAILER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-FAC99-CARD-CODE 2 N PIC 9(02) Trailer  Record, Card Code = '99' 
FILLER 13 A PIC X(13) Filler  
RPT-FAC99-ACCT 4 A/N PIC X(04) Account  Symbol 
FILLER 1 A PIC X(01) Filler  
RPT-FAC99-LOGICAL-COUNT 7 N PIC 9(07) Logical  Record Count 
FILLER 1 A PIC X(01) Filler  
RPT-FAC99-PHYSICAL-COUNT 7 N PIC 9(07) Physical  Reco rd C ount 
FILLER 193 A PIC X(193) Filler  
Total     228 
 
 

---

## Page 9

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 