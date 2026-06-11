---
title: "File Transmission Layout: CCP Uncompared Report NDM Layout"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs127_file_trans_layout_ccp_unc_rep_ndm_20220406.pdf"
pages: 10
size: "275.0 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# File Transmission Layout: CCP Uncompared Report NDM Layout

**Original File:** [mbs127_file_trans_layout_ccp_unc_rep_ndm_20220406.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs127_file_trans_layout_ccp_unc_rep_ndm_20220406.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 275.0 KB  

---

## Page 1

 
 
 
[[FICC]] - MBSD 
FILE TRANSMISSION LAYOUT: CCP UNCOMPARED REPORT NDM LAYOUT 
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
Publication Code: MBS127 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout : CCP UNCOMPARED REPORT NDM LAYOUT  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction to the Documentation.................................................................................................... 4 
Purpose ....................................................................................................................................... 4 
Frequency .................................................................................................................................... 4 
Recor d La you t .............................................................................................................................. 4 
Version C on tr ol ............................................................................................................................. 5 
1. File Transmission Layout – CCP Uncompared – NDM Format (Header) ............................................ 6 
2. File Transmission Layout – CCP Uncompared – NDM Format (Uncompared Pool Submission Detail 
Record) ........................................................................................................................................... 7 
3. File Transmission Layout – CCP Uncompared – NDM Format (Trailer) ............................................. 9 
 

---

## Page 4

CCP Uncompared NDM 
Introduction to the Doc umentation 4 
INTRODUCTION TO THE DOCUMENTATION 
Purpose 
The Uncompared Report reflects uncompared Pool Instructs (“PID’s”) and, if applicable, DK status. 
Frequency 
Daily. 
Record Layout 
*All records are of equal length – 228 bytes. 
*There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
 
ACCOUNT / REPORT HEADER RECORD (CARD CODE 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
 
UNCOMPARED POOL SUBMISSION DETAIL RECORD (CARD CODE 02) 
Detail record containing a single uncompared pool submission. 
 
TRAILER CONTROL RECORD (CARD CODE 99) 
Trailer record indicates the end of the report for the recipient account. 
 
FORMAT CODES 
# - digit  
X - alphanumeric  
A - letter 
Y - year 
M - month  
D - day 
 
NOTE: If a number is padded, it will be padded with zeroeson the left in the integer part and on the right in the 
decimal part (if one exists). If text is padded, it will be padded with spaces on the right. 
 
Sample File 
*Sample file provided after Record Layouts section. 
 

---

## Page 5

CCP Uncompared NDM 
Introduction to the Doc umentation 5 
Version Control 
Date Version # Name Description of Change  
4/3/2001 1.0 MBSD Initial  version  
7/16/2015 1.0 C. Swords  Updated  to suppor t [[Novation]]:  
• In Card Code 02 (UNCOMPARED POOL 
SUBMISSION DETAIL RECORD), added  trade 
date using  filler  at end  of record.  
8/15/2016 1.01 C. Swords  Made following  informational  changes:  
• Ad d title page  and  revision  his tor y 
10/6/2016 1.02 C. S words Mad e following  changes:  
• In Card Code 02 (UNCOMPARED POOL 
SUBMISSION DETAIL RECORD), field  Trade Date 
(RPT-UC-DT2-TRADE- DATE), updated Type from N 
to A, and Cobol Picture  from PIC 9(08) to X(08), due 
to fact that this field is  blank  for PIDs with non -
[[Novation]] -eligible CUSIPs. 
04/05/2022 1.03 J. Sheeran  Updated to latest [[DTCC]] Branding  
 

---

## Page 6

CCP Uncompared NDM 
1. File Transmission Layout – CCP Uncompared – NDM Format (Header) 6 
1. FILE TRANSMISSION LAYOUT – CCP UNCOMPARED – 
NDM FORMAT (HEADER) 
Field Name Length Type Format Cobol Picture Description/Comments  
RPT-UC-DT1-CARD-CODE 2 N ## PIC 9(02) Card code  = ‘01’ 
RPT-UC-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report  [[ID]] = ‘MB8001-N” 
RPT-UC-DT1-ACC-AGG-[[ID]]      
     RPT-UC-DT1-PART-[[ID]] 3 N ### PIC 9(03) Particip ant [[ID]] 
     RPT-UC-DT1-AGG 2 A/N ## PIC 9(02) Aggregate  
RPT-UC-DT1-ACCT 4 A AAAA PIC X(04) Account  Symbol 
RPT-UC-DT1-BUS-DATE 8 N YYYYMMDD PIC 9(08) Date of R eport 
FILLER 201 A AAAA… PIC X(201) Filler  
Total            228 

---

## Page 7

CCP Uncompared NDM 
2. File Transmission Layout – CCP Uncompared – NDM Format (Unc ompared Pool Submission Detail Record) 7 
2. FILE TRANSMISSION LAYOUT – CCP UNCOMPARED – 
NDM FORMAT (UNCOMPARED POOL SUBMISSION 
DETAIL RECORD) 
Field Name Length Type Format Cobol Picture Description/Comments  
RPT-UC-DT2-CARD-CODE 2 N ## PIC 9(02) Card code  = ‘02’ 
RPT-UC-DT1-SETTLE-MONTH 6 N YYYYMM PIC 9(06) [[settlement]] Month 
RPT-UC-DT2-TBA-[[CUSIP]] 9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-UC-DT2-POOL-NUMBER 6 A/N XXXXXX PIC X(06) Pool Number (zero-padded)  
RPT-UC-DT2-POOL-[[CUSIP]] 9 A/N XXXXXXXXX PIC X(09) Pool  [[CUSIP]] 
RPT-UC-DT2-ACTIVITY-CODE 4 A AAAA PIC X(04) Activity Code  (space -padded) 
RPT-UC-DT2-STATUS-CODE 4 A AAAA PIC X(04) Status Code (space -padded) 
RPT-UC-DT2-BUY-SELL-CODE 1 A B or S PIC X(01) Buy/Sell  C ode 
RPT-UC-DT2-XREF 16 A/N XXXXXXXXXXXXXXXX PIC X(16) X-Reference (space -padded) 
RPT-UC-DT2-PID 16 A/N XXXXXXXXXXXXXXXX PIC X(16) Pool  [[ID]] (space - padded)  
RPT-UC-DT2-ENTRY-DATE 8 N YYYYMMDD PIC 9(08) En try Date 
RPT-UC-DT2-SETTL-DATE 8 N YYYYMMDD PIC 9(08) [[settlement]] Date 
RPT-UC-DT2-DLVRY-DATE 8 N YYYYMMDD PIC 9(08) Delivery  Date 
RPT-UC-DT2-CTRA-CONTRA-AGG      
     RPT-UC-DT2-CTRA-PART-[[ID]] 3 N ### PIC 9(03) Contra Particip ant  [[ID]] 
     RPT-UC-DT2-CTRA-AGG 2 A/N ## PIC 9(02) C ont ra Aggregat e 
RPT-UC-DT2-CONTRA-[[ID]] 4 A AAAA PIC X(04) C ont ra [[ID]] 
RPT-UC-DT2-ORIG-FACE 15 N ############### PIC 9(15) Original Face  (zero-padded)  
RPT-UC-DT2-CURR-FACE 17 N ################# PIC 9(15)V9(02)  Current Face (zero-padded)  
RPT-UC-DT2-PRICE 15 N ############### PIC 9(03)V9(12)  Trade Price (zero-padded)  
RPT-UC-DT2-NET-MONEY 15 N ############### PIC 9(13)V9(02)  Net Money  (zero-padded)  
RPT-UC-DT2-CDR 3 A Y-I, Y-P, Y-T or N PIC X(03) Custo mer Delivery  Request 
Indicator  (space -padded) 
RPT-UC-DT2-REPRICE 1 A Y or N PIC X(01) Rep rice I ndicat or 
RPT-UC-DT2-DK-CODE 4 A/N XXXX PIC X(04) D K R eason C ode  (space -
padded)  
RPT-UC-DT2-TRADE-DATE 8 A YYYYMMDD PIC X(08) Trade Date 
FILLER 44 A AAAA… PIC X(44) Filler  

---

## Page 8

CCP Uncompared NDM 
2. File Transmission Layout – CCP Uncompared – NDM Format (Unc ompared Pool Submission Detail Record) 8 
Total            228 

---

## Page 9

CCP Uncompared NDM 
3. File Transmission Layout – CCP Uncompared – NDM Format (Trailer) 9 
3. FILE TRANSMISSION LAYOUT – CCP UNCOMPARED – 
NDM FORMAT (TRAILER) 
Field Name Length Type Format Cobol Picture Description/Comments  
RPT-UC-DT99-CARD-CODE 2 N ## PIC 9(02) Card code  = ‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler  
RPT-UC-DT99-ACCT 4 A AAAA PIC X(04) Account  Symbol 
FILLER 1 A A PIC X(01) Filler  
RPT-UC-DT99-LOGICAL-COUNT 7 N ####### PIC 9(07) Logical  Reco rd C ount   (zero-
padded)  
FILLER 1 A A PIC X(01) Filler  
RPT-UC-DT99-PHYSICAL-COUNT 7 N ####### PIC 9(07) Physical  Reco rd C ount (zero-
padded)  
FILLER 193 A AAAA… PIC 9(193) Filler  
Total                          228 
 
 
  

---

## Page 10

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 