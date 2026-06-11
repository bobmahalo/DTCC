---
title: "File Transmission Layout - CCP Expanded Pool Netting Summary NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs151_ccp_exp_pool_net_summ_ndm.pdf"
pages: 10
size: "279.4 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# File Transmission Layout - CCP Expanded Pool Netting Summary NDM Format

**Original File:** [mbs151_ccp_exp_pool_net_summ_ndm.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs151_ccp_exp_pool_net_summ_ndm.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 279.4 KB  

---

## Page 1

 
 
1 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUT - CCP EXPANDED POOL NETTING SUMMARY 
NDM FORMAT 
VERSION 1.01 
AUGUST 24, 2016 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in wh ich such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: August 24, 2016 
Publication Code:  MBS151 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout -  CCP Expanded Pool Netting Summary NDM Format  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ....................................................................................................................... 4 
File Transmission Layout Overview .................................................................................................. 5 
CCP Expanded Pool Netting Summary Report NDM Format .................................................................  5 
Purpose ....................................................................................................................................... 5 
Frequency .................................................................................................................................... 5 
Recor d La you ts............................................................................................................................. 5 
Account/Report Header Records (Card Code 01).............................................................................. 5 
Pool Instruct Detail Record (Card Code 02)...................................................................................... 5 
Trailer Control Record (Card Code 99) ............................................................................................ 5 
Format Codes ............................................................................................................................... 6 
File Transmission Layout – CCP Expanded Pool Netting Summary Report– NDM Format ..................... 7 
Header.......................................................................................................................................... 7 
Pool Netting Summary Reco rd.......................................................................................................... 8 
Trailer ........................................................................................................................................... 9 
 

---

## Page 4

File Transmission Layout - CCP Expande d Pool Netting Summary NDM Format 
Version C ontrol Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change  
7/16/2015 1.0 C. Swords  Initial version  
8/11/2016 1.01 C. Swords  Made following  updates: 
• Add standard title page and revision history  
n/a n/a [[DTCC]] 
Learning  
Updated formatting only. Content is unchanged.  
 
  

---

## Page 5

File Transmission Layout - CCP Expanded Pool Netting Summary NDM Format 
File Transmission Layout Ov erview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
CCP Expanded Pool Netting Summary Report NDM Format 
Purpose 
The Pool Netting Summary Report reflects the results of the current day’s expanded (or second) pool netting 
cycle in summary. 
Frequency 
Per SIFMA calendar on 24hr day. 
Record Layouts 
*All records are of equal length - 228 bytes. 
* There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Pool Instruct Detail Record (Card Code 02) 
Detail record containing a single pool netting summary record. 
Trailer Control Record (Card Code 99) 
Trailer record indicates the end of the report for the recipient account. 
  

---

## Page 6

File Transmission Layout - CCP Expanded Pool Netting Summary NDM Format 
File Transmission Layout Ov erview 6 
Format Codes 
# - digit  
X - alphanumeric  
A - letter 
Y - year 
M - month 
D – day 
Note:   
If a number is padded, it will be padded with zeroes on the left in the integer part and on the right in the decimal part (if one 
exists). If text is padded, it will be padded with spaces on the right.  

---

## Page 7

File Transmission Layout - CCP Expanded Pool Netting Summary NDM Format 
File Transmission Layout – CCP Ex panded Pool Netting Summary Report– NDM Format 7 
FILE TRANSMISSION LAYOUT – CCP EXPANDED POOL 
NETTING SUMMARY REPORT– NDM FORMAT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-EPS-DT1-CARD-CODE 2 N ## PIC 9(02) Card code = ‘01’ 
RPT-EPS-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report [[ID]] = “MB8105-N” 
RPT-EPS-DT1-ACC-AGG-[[ID]]      
     RPT-EPS-DT1-PART-[[ID]] 3 N ### PIC 9(03) [[participant]] [[ID]]  
     RPT-EPS-DT1-AGG 2 N ## PIC 9(02) Aggregate Number 
RPT-EPS-DT1-ACCT 4 A AAAA PIC X(04) Account Symbol  
RPT-EPS-DT1-BUS-DATE 8 N YYYYMMDD PIC 9(08) Date of Report  
FILLER 201 A AAAA… PIC X(201) Filler  
Total   228 
  

---

## Page 8

File Transmission Layout - CCP Expanded Pool Netting Summary NDM Format 
File Transmission Layout – CCP Ex panded Pool Netting Summary Report– NDM Format 8 
Pool Netting Summary Record 
Detail record containing a single pool netting summary record. 
Field Name Length Type Format Cobol 
Picture 
Description/Notes 
RPT-EPS -DT2 -CARD-
CODE 
2 N ## PIC 9(02) Card code  = ‘02’ 
RPT-EPS -DT2 -TBA -
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-EPS -DT2 -POOL -
NUMB E R 
6 A/N XXXXXX PIC X(06) Pool Number (zero- padded) 
RPT-EPS -DT2 -POOL -
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) Pool  [[CUSIP]] 
RPT-EPS -DT2 -LONG -
[[FICC]]-ORIG - FACE 
15 N ############### PIC 9(15) Long vs [[FICC]] Original Face 
(zero-padded)  
RPT-EPS -DT2 -LONG -
[[FICC]]-CURR - FACE 
17 N ################# PIC 
9(15)V9(02)  
Long Vs [[FICC]] Current Face 
(zero-padded)  
RPT-EPS -DT2 -[[FICC]] -
RVP-NET  
17 N #################  PIC 
9(15)V9(02)  
[[FICC]] RVP Net 
(zero- padded)  
RPT-EPS -DT2 -SHORT -
[[FICC]]-ORIG - FACE 
15 N ############### PIC 9(15) Short  vs [[FICC]] Original Face 
(zero-padded)  
RPT-EPS -DT2 -SHORT -
[[FICC]]-CURR - FACE 
17 N ################# PIC 
9(15)V9(02)  
Short  Vs [[FICC]] Current Face 
(zero-padded)  
RPT-EPS -DT2 -[[FICC]] -
DVP-NET  
17 N #################  PIC 
9(15)V9(02)  
[[FICC]] DVP Net 
(zero- padded)  
RPT-EPS -DT2 -[[FICC]] -
NET-ORIG -FACE  
15 N ############### PIC 9(15) [[FICC]] Net Original Face 
(zero-padded)  
RPT-EPS -DT2 -N ET-
ORIG-FACE - CREDIT-
DEBIT 
1 A C or D PIC X(01) Net Original  Face Credit or 
Debit 
RPT-EPS -DT2 -[[FICC]] -NET -
CURR- FACE 
17 N ################# PIC 
9(15)V9(02)  
[[FICC]] Net Current Face (zero-
padded)  
RPT-EPS -DT2 -NET -
CURR- FACE- CREDIT-
DEBIT 
1 A C or D PIC X(01) Net Current Face Credit or Debit 
RPT-EPS -DT2 -[[FICC]] -
NET-NET  
17 N ################# PIC 
9(15)V9(02)  
[[FICC]] Net Net (zero- padded)  
RPT-EPS -DT2 -NET -NET - 
CRE DIT- DEBIT 
1 A C or D PIC X(01) Net Net Credit  or Debit 

---

## Page 9

File Transmission Layout - CCP Expanded Pool Netting Summary NDM Format 
File Transmission Layout – CCP Ex panded Pool Netting Summary Report– NDM Format 9 
Field Name Length Type Format Cobol 
Picture 
Description/Notes 
RPT-EPS -DT2 -TOTAL -
TRADE- ADJUST 
17 N ################# PIC 
9(15)V9(02) 
Total  Trade Adjustment  
(zero-padded)  
RPT-EPS -DT2 -TRADE -
ADJUS T- CREDIT-DEBIT 
1 A C or D PIC X(01) Trade Adjustment Credit or 
Debit 
RPT-EPS -DT2 -DLVRY -
DATE 
8 N YYYYMMDD PIC 9(08) Delivery Date 
FILLER 26 A AAAA… PIC X(26) Filler  
   Total     228 
    
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-EPS-DT99-CARD-CODE 2 N ## PIC 9(02) Card code = ‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler  
RPT-EPS-DT99-ACCT 4 A AAAA PIC X(04) Account Symbol  
FILLER 1 A A PIC X(01) Filler  
RPT-EPS-DT99-LOGICAL-
COUNT 
7 N ####### PIC 9(07) Logical Record 
Count (zero - 
padded)  
FILLER 1 A A PIC X(01) Filler  
RPT-EPS-DT99-PHYSICAL-
COUNT 
7 N ####### PIC 9(07) Physical Record 
Count (zero - 
padded)  
FILLER 193 A AAAA… PIC 9(193) Filler  
Total   228 
 
 
 
 
 

---

## Page 10

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 