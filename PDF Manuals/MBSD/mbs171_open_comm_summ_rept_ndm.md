---
title: "MBSD CLR Fund RequiredFile Transmission Layouts for Open Commitment Summary Report NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs171_open_comm_summ_rept_ndm.pdf"
pages: 9
size: "288.3 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD CLR Fund RequiredFile Transmission Layouts for Open Commitment Summary Report NDM Format

**Original File:** [mbs171_open_comm_summ_rept_ndm.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs171_open_comm_summ_rept_ndm.pdf)  
**Category:** MBSD  
**Total Pages:** 9  
**File Size:** 288.3 KB  

---

## Page 1

 
FIXED INCOME CLEARING CORPORATION 
FILE TRANSMISSION LAYOUTS FOR OPEN COMMITMENT SUMMARY REPORT NDM FORMAT 
VERSION 1.0 
APRIL 3, 2001 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself 
does not provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: April  3, 2001 
Publication Code:  MBS171 
Service: Mortgage -Backed [[securities]] Division  
Title: File Transmission Layouts for Open Commitment Summary Report NDM Format  

---

## Page 3

 
 
TABLE OF CONTENTS 
Report Information ............................................................................................................................................................................... 4  
General Information ............................................................................................................................................................................ 4  
File Transmission Layouts.................................................................................................................................................................... 4  
Open Commitment Summary – NDM Format – Head er Reco rd ................................................................................................................ 4  
Open Commitment Summary – NDM Format – [[CUSIP]] / Class Header Record ........................................................................................... 5  
Open Commitment Summary – NDM Format – [[CUSIP]] / Class Footer Reco rd............................................................................................. 6  
Open Commitment Summary – NDM Format – Report Footer Record ....................................................................................................... 6  
Open Commitment Summary – NDM Format – Report Trailer Record ....................................................................................................... 8  
 

---

## Page 4

File Transmission Layouts for Open Commitment Summary Report NDM Format 
Report Information  4 
REPORT INFORMATION 
General Information 
File Transmission Layouts for Open Commitment Summary Report NDM Format  
Purpose The Open Commitment Summary Report is an extract of the Open Commitment Report providing key 
[[CUSIP]] level and final totals.  
Frequency Daily, both A.M. and P.M. passes, Weekly (Friday) and Monthly ( month-end). 
All physical records are of equal length - 210 bytes. 
There are 5 different logical record types, each uniquely identified by card code, as follows: card codes 
01 through 04, & 99. 
Account / Report Header Record (Card Code 01) Control record which signifies the beginning of the report for a given account. Contains recipient account 
and report identification items.  
[[CUSIP]] Header Record (Card Code 02) Control record which signifies the beginning of the next [[CUSIP]].  
[[CUSIP]] Footer Record (Card Code 03) Detail record containing statistics (mainly totals) about trade activity within this [[CUSIP]] for the recipient 
account. 
Report Footer Record (Card Code 04) Contains trade statistics for the entire report (one account only) based on the age and status of the 
individual trades.  
Trailer Control Record (Card Code 99) Trailer record indicates the end of the report for the recipient account.  
File Transmission Layouts 
Open Commitment Summary – NDM Format – Header Record 
Field Name Length Type COBOL Picture Comments 
RPT-OCS-DT1-CARD-CODE 2 A/N PIC X(02). Header Record,  Card Code  = '01' 
RPT-OCS-DT1-RPT-[[ID]] 8 A/N PIC X(08). Report  [[ID]] - 'MB4911-A' 
RPT-OCS-DT1-ACC-AGG-[[ID]]     

---

## Page 5

File Transmissi on Layouts for Open Commitment Summary Report NDM Format 
Report Information  5 
Field Name Length Type COBOL Picture Comments 
RPT-OCS-DT1-
[[participant]]-[[ID]] 
3 N PIC 9(03). [[participant]]  [[ID]] Number 
RPT-OCS-DT1-AGG-NBR 2 A/N PIC 9(02). Aggregate  
RPT-OCS-DT1-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
RPT-OCS-DT1-[[participant]]-
NAME 
40 A/N PIC X(40). [[participant]]  Name 
RPT-OCS-DT1-BUS-DATE 8 A/N PIC X(08). Date of Report  (YYYYMMDD) 
RPT-OCS-DT1-PASS 1 A/N PIC X(01). Pass Indicator  (A = Morning or P = Evening)  
FILLER 142  A/N PIC X(142). Filler  
 210     
 
Open Commitment Summary – NDM Format – [[CUSIP]] / Class Header Record 
Field Name Length Type COBOL Picture Comments 
RPT-OCS-DT2-CARD-CODE 2 A/N PIC X(02). [[CUSIP]] Header, Card  Code  = '02' 
RPT-OCS-DT2-STTL-YY 4 A/N PIC X(04). [[settlement]] Year (YYYY format) 
RPT-OCS-DT2-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM format) 
RPT-OCS-DT2-[[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] 
FILLER 1 A PIC X(01). Filler  
RPT-OCS-DT2-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
RPT-OCS-DT2-[[CUSIP]]-DESC 40 A/N PIC X(40). [[CUSIP]] Description 
RPT-OCS-DT2-MKT-PRC 15 N PIC 9(03)V9(12). Market Price 
FILLER 133  A/N PIC X(133). Filler  
 210     
 

---

## Page 6

File Transmission Layouts for Open Commitment Summary Report NDM Format 
Report Information  6 
Open Commitment Summary – NDM Format – [[CUSIP]] / Class Footer Record 
Field Name Length Type COBOL Picture Comments 
RPT-OCS-DT3-CARD-CODE 2 A/N PIC X(02). [[CUSIP]] Footer, Card Code = '03'  
RPT-OCC-DT3-STTL-YY 4 A/N PIC X(04). [[settlement]] Year (YYYY) 
RPT-OCS-DT3-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM)  
RPT-OCS-DT3-[[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] 
FILLER 1 A PIC X(01). Filler  
RPT-OCS-DT3-ACCOUNT 4 A/N PIC X(04). Account Symbol  
RPT-OCS-DT3-BOP 13 N PIC 9(11)V9(02). Buy Open Par Value 
RPT-OCS-DT3-BCON 13 N PIC 9(11)V9(02). Buy [[settlement]] Value 
RPT-OCS-DT3-BPL 13 N PIC 9(11)V9(02). Buy Profit / Loss  
RPT-OCS-DT3-BPL-CRDR 1 A PIC X(01). Buy Profit / Loss Indicator (C=Credit, D=Debit)  
RPT-OCS-DT3-SOP 13 N PIC 9(11)V9(02). Sell Open Par Value 
RPT-OCS-DT3-SCON 13 N PIC 9(11)V9(02). Sell [[settlement]] Value 
RPT-OCS-DT3-SPL 13 N PIC 9(11)V9(02). Sell Profit / Loss  
RPT-OCS-DT3-SPL-CRDR 1 A PIC X(01). Sell Profit / Loss Indicator (C=Credit, D=Debit)  
FILLER 108  A/N PIC X(108). Filler  
 210     
 
Open Commitment Summary – NDM Format – Report Footer Record 
Field Name Length Type COBOL Picture Comments 
RPT-OCS-DT4-CARD-CODE 2 A/N PIC X(02). Report Footer, Card Code = '04'  
FILLER 16 A/N PIC X(16) Filler  

---

## Page 7

File Transmission Layouts for Open Commitment Summary Report NDM Format 
Report Information  7 
Field Name Length Type COBOL Picture Comments 
RPT-OCS-DT4-ACCOUNT 4 A/N PIC X(04). Account Symbol  
RPT-OCS-DT4-FW-BUY-ITM 4 A/N PIC X(04). Forward Buy Item Count  
RPT-OCS-DT4-FW-BUY-
OPAR 
13 N PIC 9(11)V9(02). Forward Buy Open Par Value 
RPT-OCS-DT4-FW-BUY-
STTL 
13 N PIC 9(11)V9(02). Forward Buy [[settlement]] Value 
RPT-OCS-DT4-FW-SEL-ITM 4 A/N PIC X(04). Forward Sell Item Count  
RPT-OCS-DT4-FW-SEL-
OPAR 
13 N PIC 9(11)V9(02). Forward Sell Open Par Value 
RPT-OCS-DT4-FW-SEL-
STTL 
13 N PIC 9(11)V9(02). Forward Sell [[settlement]] Value 
RPT-OCS-DT4-FL-BUY-ITM 4 A/N PIC X(04). Fail Buy Item Count  
RPT-OCS-DT4-FL-BUY-
OPAR 
13 N PIC 9(11)V9(02). Fail Buy Open Par Value 
RPT-OCS-DT4-FL-BUY-STTL 13 N PIC 9(11)V9(02). Fail Buy [[settlement]] Value 
RPT-OCS-DT4-FL-SEL-ITM 4 A/N PIC X(04). Fail Sell Item Count  
RPT-OCS-DT4-FL-SEL-
OPAR 
13 N PIC 9(11)V9(02). Fail Sell Open Par Value 
RPT-OCS-DT4-FL-SEL-STTL 13 N PIC 9(11)V9(02). Fail Sell [[settlement]] Value 
RPT-OCS-DT4-AF-BUY-ITM 4 A/N PIC X(04). Aged Fail Buy Item Count  
RPT-OCS-DT4-AF-BUY-
OPAR 
13 N PIC 9(11)V9(02). Aged Fail Buy Open Par Value 
RPT-OCS-DT4-AF-BUY-STTL 13 N PIC 9(11)V9(02). Aged Fail Buy [[settlement]] Value 
RPT-OCS-DT4-AF-SEL-ITM 4 A/N PIC X(04). Aged Fail Sell Item Count  
RPT-OCS-DT4-AF-SEL-
OPAR 
13 N PIC 9(11)V9(02). Aged Fail Sell Open Par Value 
RPT-OCS-DT4-AF-SEL-STTL 13 N PIC 9(11)V9(02). Aged Fail Sell [[settlement]] Value 

---

## Page 8

File Transmission Layouts for Open Commitment Summary Report NDM Format 
Report Information  8 
Field Name Length Type COBOL Picture Comments 
FILLER 8 A/N PIC X(08) Filler 
 210     
 
Open Commitment Summary – NDM Format – Report Trailer Record 
Field Name Length Type COBOL Picture Comments 
RPT-OCS-DT99-CARD-
CODE 
2 A/N PIC X(02). Report  Trailer,  Card Code  = '99' 
FILLER 13 A PIC X(13). Filler  
RPT-OCS-DT99-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
FILLER 1 A PIC X(01). Filler  
RPT-OCS-DT99-LOGICAL-
COUNT 
7 N PIC 9(07). Logical  Record  Count  
FILLER 1 A PIC X(01). Filler  
RPT-OCS-DT99-PHYSICAL-
COUNT 
7 N PIC 9(07). Physical  Record  Count  
FILLER 175  A PIC X(175). Filler  
 210     
 
 

---

## Page 9

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 