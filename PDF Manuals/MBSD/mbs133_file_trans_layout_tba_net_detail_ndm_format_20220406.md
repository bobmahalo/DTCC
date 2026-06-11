---
title: "File Transmission Layout: TBA Net Detail NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs133_file_trans_layout_tba_net_detail_ndm_format_20220406.pdf"
pages: 10
size: "336.0 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# File Transmission Layout: TBA Net Detail NDM Format

**Original File:** [mbs133_file_trans_layout_tba_net_detail_ndm_format_20220406.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs133_file_trans_layout_tba_net_detail_ndm_format_20220406.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 336.0 KB  

---

## Page 1

 
 
 
[[FICC]] - MBSD 
FILE TRANSMISSION LAYOUT: TBA NET DETAIL NDM FORMAT  
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
Publication Code: MBS133 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout : TBA Net Detail NDM Format  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction to the Documentation.................................................................................................... 4 
Purpose ....................................................................................................................................... 4 
Frequency .................................................................................................................................... 4 
Recor d La you t .............................................................................................................................. 4 
Version C on tr ol ............................................................................................................................. 5 
1. File Transmission Layout – TBA Net detail – NDM Layout (HEADER) ............................................... 6 
2. File Transmission Layout – TBA Net Detail – NDM Layout (TRADE DETAIL) ..................................... 7 
3. File Transmission Layout – TBA Net Detail – NDM Layout (TRADE OBLIGATION DETAIL) ................ 8 
3. File Transmission Layout – TBA Net Detail – NDM Layout (TRAILER) .............................................. 9 
 

---

## Page 4

TBA Net Detail NDM 
Introduction to the Doc umentation 4 
INTRODUCTION TO THE DOCUMENTATION 
Purpose 
This report displays details from the TBA Net, including SBOD trades included in the SBO process along with 
corresponding TBA TAP and resulting SBON [[obligations]] versus FTBA at the [[FICC]] determined system price. 
Frequency 
Per SIFMA Calendar on Netting day 
Record Layout 
*All records are of equal length - 228 bytes. 
*There are 4 different record types, each uniquely identified by card code, as follows: card codes 01 through 
03, & 99. 
ACCOUNT / REPORT HEADER RECORD (CARD CODE 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
 
TBA DETAIL RECORD (CARD CODE 02) 
Detail record containing a single SBOD trade record included in the net. 
 
TBA OBLIGATION DETAIL RECORD (CARD CODE 03) 
Detail record containing a single resulting SBON record. 
 
TRAILER CONTROL RECORD (CARD CODE 99) 
Trailer record indicates the end of the report for the recipient account. 
 
 
 
 
 
 
 

---

## Page 5

TBA Net Detail NDM 
Introduction to the Doc umentation 5 
Version Control 
Date Version # Name Description of Change  
8/4/2015 1.0 C. Swords • Initial version 
2/27/2016 1.01 C. Swords Made following changes: 
• Card code 02 (TRADE DETAIL RECORD), 
corrected description of TBA-TAP to “TBA 
Transaction Adjustment Payment (TAP)” 
8/11/2016 1.02 C. Swords Made following changes: 
• Add title page and revision history 
3/28/2022 1.03 J. Sheeran Updated [[DTCC]] branding template 
 

---

## Page 6

TBA Net Detail NDM 
1. File Transmission Layout – TBA N et detail – NDM Layout (HEADER) 6 
1. FILE TRANSMISSION LAYOUT – TBA NET DETAIL – 
NDM LAYOUT (HEADER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-TNET1-CARD-CODE 2 N PIC 9(02) Header R ecord, Card code  = ‘01’ 
RPT-TNET1-RPT-[[ID]] 8 A/N PIC X(08) Report  [[ID]] = ‘MB8101-N’ 
RPT-TNET1-ACC-AGG-[[ID]]     
RPT-TNET1-PART-[[ID]] 3 N PIC 9(03) [[participant]]  [[ID]] 
RPT-TNET1-AGG 2 N PIC 9(02) Aggregate  
RPT-TNET1-ACCT 4 A PIC X(04) Account  Symbo l 
RPT-TNET1-PART-NAME 40 A/N PIC X(40) [[participant]]  Name 
RPT-TNET1-BUS-DATE 8 N PIC 9(08) Date of R eport 
FILLER 161 A PIC X(161) Filler  
Total     228 

---

## Page 7

TBA Net Detail NDM 
2. File Transmission Layout – TBA Net Detail – NDM Layout (TRADE DETAIL) 7 
2. FILE TRANSMISSION LAYOUT – TBA NET DETAIL – 
NDM LAYOUT (TRADE DETAIL) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-TNET2-CARD-CODE 2 N PIC 9(02) Trad e Detail Record, Card 
code = ‘02’ 
RPT-TNET2-TBA-CUS IP 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-TNET2-ACCT 4 A/N PIC X(04) Account  Symbol  
RPT-TNET2-TRADE-[[ID]]     
RPT-TNET2-TRD-PFX 4 N PIC 9(04) Trad e Number Pref ix 
RPT-TNET2-TRD-SFX 6 N PIC 9(06) Trad e Number Suffix 
RPT-TNET2-XREF 15 A/N PIC X(15) Internal XREF / Trad e # 
RPT-TNET2-TRADE-TYPE 4 A/N PIC X(04) Trade Type-SBOD 
RPT-TNET2-BS-IND 1 A PIC X(01) Buy/Sell Code, B=Buy, S = Sell 
RPT-TNET2-TRD-DATE 8 N PIC 9(08) Trad e Date (YYYYMMDD) 
RPT-TNET2-STTL-M TH-
YR 
6 N PIC 9(06) [[settlement]] Date Month and  Year 
(YYYYMM) 
RPT-TNET2-CTRA 4 A/N PIC X(04) Contra Account 
RPT-TNET2-PAR 13 N PIC 9(11)V9(02) Par 
RPT-TNET2-TRD-PRICE 15 N PIC 9(03)V9(12) Trad e Price – In Decimal 
RPT-TNET2-TRD-MONEY 13 N PIC 9(11)V9(02) [[settlement]] Value based on Trad e 
Price 
RPT-TNET2-STL-PRICE 15 N PIC 9(03)V9(12) [[settlement]] Price – In Decimal 
RPT-TNET2-STL-MONEY 13 N PIC 9(11)V9(02) [[settlement]] Value based on 
[[settlement]] Price 
RPT-TNET2-TBA-TAP 13 N PIC 9(11)V9(02) TBA Trans actio n Adjustment 
Payment (TAP) 
RPT-TNET2-TBA-TAP-
CRDR 
1 A PIC X(01) TBA TAP Indicator (C=Credit, 
D=Debit) 
FILLER 82 A PIC X(82) Filler 
Total 228    
 
 
 
 
 
 
 
 
 

---

## Page 8

TBA Net Detail NDM 
3. File Transmission Layout – TBA N et Detail – NDM Layout (TRADE OBLIGATION DETAIL) 8 
3. FILE TRANSMISSION LAYOUT – TBA NET DETAIL – 
NDM LAYOUT (TRADE OBLIGATION DETAIL) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-TNET3-CARD-CODE 2 N PIC 9(02) Trade  Obligation  Detail R ecord, 
Card code  = ‘03’ 
RPT-TNET3-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-TNET3-ACCT 4 A/N PIC X(04) Account  Symbol 
RPT-TNET3-TRADE-[[ID]]     
RPT-TNET3-TRD-PFX 4 N PIC 9(04) Trade  Number  Prefix 
RPT-TNET3-TRD-SFX 6 N PIC 9(06) Trade  Number  Suffix 
RPT-TNET3-TRADE-TYPE 4 A/N PIC X(04) Trade  Type -SBON  
RPT-TNET3-BS-IND 1 A PIC X(01) Buy/Sell  C ode, B=Buy, S = Sell 
RPT-TNET3-TRD-DATE 8 N PIC 9(08) Trade  Date (YYYYM M DD ) 
RPT-TNET3-STTL-DATE 8 N PIC 9(08) Settle m en t Date (YYYYM M D D) 
RPT-TNET3-CTRA 4 A/N PIC X(04) C ont ra Account  
RPT-TNET3-PAR 13 N PIC 9(11)V9(02) Par 
RPT-TNET3-STL-PRICE 15 N PIC 9(03)V9(12) Settle m en t Price – In Decima l 
RPT-TNET3-STL-MONEY 13 N PIC 9(11)V9(02) [[settlement]] Value 
FILLER 137 A PIC X(137) Filler  
Total      228 

---

## Page 9

TBA Net Detail NDM 
3. File Transmission Layout – TBA Net Detail – NDM Layout (TRAILER) 9 
3. FILE TRANSMISSION LAYOUT – TBA NET DETAIL – 
NDM LAYOUT (TRAILER) 
Field Name Length Type Cobol Picture Description/Comments  
RPT-TNET99-CARD-CODE 2 N PIC 9(02) Trailer  Record, Card Code = '99' 
FILLER 13 A PIC X(13) Filler  
RPT-TNET99-ACCT 4 A/N PIC X(04) Account  Symbol 
FILLER 1 A PIC X(01) Filler  
RPT-TNET99-LOGICAL-COUNT 7 N PIC 9(07) Logical  Record Count 
FILLER 1 A PIC X(01) Filler  
RPT-TNET99-PHYSICAL-COUNT 7 N PIC 9(07) Physical  Reco rd C ount 
FILLER 193 A PIC X(193) Filler  
Total     228 
 

---

## Page 10

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 