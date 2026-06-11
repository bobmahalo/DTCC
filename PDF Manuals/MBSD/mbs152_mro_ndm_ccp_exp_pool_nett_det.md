---
title: "CCP Pool Obligation Pending Settlement Report NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs152_mro_ndm_ccp_exp_pool_nett_det.pdf"
pages: 12
size: "330.6 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# CCP Pool Obligation Pending Settlement Report NDM Format

**Original File:** [mbs152_mro_ndm_ccp_exp_pool_nett_det.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs152_mro_ndm_ccp_exp_pool_nett_det.pdf)  
**Category:** MBSD  
**Total Pages:** 12  
**File Size:** 330.6 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUT – CCP EXPANDED POOL NETTING DETAIL 
FORMAT 
VERSION 1.03 
APRIL 17, 2018 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: April 17, 2018 
Publication Code: MBS152 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout - CCP Expanded Pool Netting Detail Report 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................... 4 
File Transmission Layout Overview ................................................................................................................... 5 
CCP Expanded Pool Netting Detail Report Format ............................................................................................ 5 
Purpose ............................................................................................................................................................. 5 
Frequency.......................................................................................................................................................... 5 
Record Layouts ................................................................................................................................................. 5 
Account/Report Header Records (Card Code 01) ........................................................................................... 5 
[[CUSIP]]/Pool Record Header (Card Code 02) .................................................................................................. 5 
Pool Instruct Detail Record (Card Code 03) .................................................................................................... 5 
Pool Obligation Detail Record (Card Code 04) ............................................................................................... 5 
Trailer Control Record (Card Code 99) ........................................................................................................... 5 
Format Codes .................................................................................................................................................... 6 
File Transmission Layout – CCP Expanded Pool Netting Detail Report–Format .......................................... 7 
Header ................................................................................................................................................................ 7 
[[CUSIP]]/Pool Header ............................................................................................................................................ 8 
Pool Instruct Detail Record ................................................................................................................................. 9 
Pool Obligation Record ..................................................................................................................................... 10 
Trailer ................................................................................................................................................................ 11 
 

---

## Page 4

File Transmission Layout – CCP Expanded Pool Netting Detail Format 
Version Control Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
7/16/2015 1.0 C. Swords Initial version 
8/4/2016 1.01 C. Swords Made following updates: 
• Add standard title page and revision history 
11/25/2016 1.02 C. Swords Made following informational changes: 
• Remove NDM from document name 
4/17/2018 1.03 J. Xie Adding clarification on PID field format: 
• Clarify that PID-[[ID]] 16-character fixed-length alpha- numeric field 
is left padded with 2 zeros. 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
 
  

---

## Page 5

File Transmission Layout – CCP Expanded Pool Netting Detail Format 
File Transmission Layout Overview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
CCP Expanded Pool Netting Detail Report Format 
Purpose 
The Expanded Pool Netting Detail Report reflects the results of the current day’s expanded (or second) pool 
netting cycle in detail. 
Frequency 
Per SIFMA calendar on 24hr day. 
Record Layouts 
*All records are of equal length - 228 bytes. 
* There are 5 different record types, each uniquely identified by card code, as follows: card codes 01 through 
04, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
[[CUSIP]]/Pool Record Header (Card Code 02) 
Control record which signifies the beginning of the next [[CUSIP]]. 
Pool Instruct Detail Record (Card Code 03) 
Detail record containing a single netting activity item for a pool instruct record. 
Pool Obligation Detail Record (Card Code 04) 
Detail record containing a single netting activity item for a pool obligation record. 
Trailer Control Record (Card Code 99) 
Trailer record indicates the end of the report for the recipient account. 
  

---

## Page 6

File Transmission Layout – CCP Expanded Pool Netting Detail Format 
File Transmission Layout Overview 6 
Format Codes 
# - digit 
X - alphanumeric  
A - letter 
Y - year 
M - month 
D - day 
Note:   
If a number is padded, it will be padded with zeroes on the left in the integer part and on the right in the decimal part (if one 
exists). If text is padded, it will be padded with spaces on the right. 

---

## Page 7

File Transmission Layout – CCP Expanded Pool Netting Detail Format 
File Transmission Layout – CCP Expanded Pool Netting Detail Report–Format 7 
FILE TRANSMISSION LAYOUT – CCP EXPANDED POOL 
NETTING DETAIL REPORT–FORMAT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PND-DT1-CARD-CODE 2 N ## PIC 9(02) Card code = ‘01’ 
RPT-PND-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report [[ID]] = ‘MB8104-N” 
RPT-PND-DT1-ACC-AGG-[[ID]]      
     RPT-PND-DT1-PART-[[ID]] 3 N ### PIC 9(03) [[participant]] [[ID]] 
     RPT-PND-DT1-AGG 2 N ## PIC 9(02) Aggregate Number 
RPT-PND-DT1-ACCT 4 A AAAA PIC X(04) Account Symbol 
RPT-PND-DT1-BUS-DATE 8 N YYYYMMDD PIC 9(08) Date of Report 
FILLER 201 A AAAA… PIC X(201) Filler 
Total   228 
  

---

## Page 8

File Transmission Layout – CCP Expanded Pool Netting Detail Format 
File Transmission Layout – CCP Expanded Pool Netting Detail Report–Format 8 
[[CUSIP]]/Pool Header 
Control record which signifies the beginning of the next [[CUSIP]]. 
Field Name Length Type Format Cobol 
Picture 
Description/Notes 
RPT-PND-DT2-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘02’ 
RPT-PND-DT2-TBA-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-PND-DT2-POOL-
NUMBER 
6 A/N XXXXXX PIC X(06) Pool Number (zero-padded) 
RPT-PND-DT2-POOL-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) Pool [[CUSIP]] 
RPT-PND-DT2-SETTL-
PRICE 
15 N ############### PIC 
9(03)V9(12) 
[[settlement]] Price (zero-padded) 
RPT-PND-DT2-DLVRY-
DATE 
8 N YYYYMMDD PIC 9(08) Delivery Date 
RPT-PND-DT2-TRADE-
ADJ 
17 N ################# PIC 
9(15)V9(02) 
Trade Adjustment (zero-
padded) 
RPT-PND-DT2-TRADE-
ADJ- CREDIT-DEBIT 
1 A C or D PIC X(01) Trade Adjustment Credit or 
Debit 
RPT-PND-DT2-FAIL-
MARK 
17 N ################# PIC 
9(15)V9(02) 
Fail Mark (zero- padded) 
RPT-PND-DT2-FAIL-
MARK- CREDIT-DEBIT 
1 A C or D PIC X(01) Fail Mark Credit or Debit 
FILLER 179 A AAAA… PIC X(179) Filler 
   Total     228 
 
  

---

## Page 9

File Transmission Layout – CCP Expanded Pool Netting Detail Format 
File Transmission Layout – CCP Expanded Pool Netting Detail Report–Format 9 
Pool Instruct Detail Record 
Detail record containing a single netting activity item for a pool instruct record. 
Field Name Length Type Format Cobol 
Picture 
Description/Notes 
RPT-PND-DT3-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘03’ 
RPT-PND-DT3-SETTL-
DATE 
8 N YYYYMMDD PIC 9(08) [[settlement]] Date 
RPT-PND-DT3-DLVRY-
DATE 
8 N YYYYMMDD PIC 9(08) Delivery Date 
RPT-PND-DT3-PID 16 A/N ################ PIC 9(16) Pool [[ID]] 
(Left zero- padded) 1 
RPT-PND-DT3-OID 10 N ########## PIC 9(10) Obligation [[ID]] (zero- padded) 
RPT-PND-DT3-BUY-
SELL-CODE 
1 A B or S PIC X(01) Buy/Sell Code 
RPT-PND-DT3-XREF 16 A/N XXXXXXXXXXXXXXXX PIC X(16) X-Reference (space- padded) 
RPT-PND-DT3-LONG-
ORIG-FACE 
15 N ############### PIC 9(15) Long Original Face (zero-
padded) 
RPT-PND-DT3-LONG-
CURR-FACE 
17 N ################# PIC 
9(15)V9(02) 
Long Current Face (zero-
padded) 
RPT-PND-DT3-SHORT-
ORIG-FACE 
15 N ############### PIC 9(15) Short Original Face (zero-
padded) 
RPT-PND-DT3-SHORT-
CURR-FACE 
17 N ################# PIC 
9(15)V9(02) 
Short Current Face (zero-
padded) 
RPT-PND-DT3-DEBIT-
NET-MONEY 
15 N ############### PIC 
9(13)V9(02) 
Debit Net Money (zero-padded) 
RPT-PND-DT3-CREDIT-
NET-MONEY 
15 N ############### PIC 
9(13)V9(02) 
Credit Net Money (zero-padded) 
FILLER 73 A AAAA… PIC X(73) Filler 
   Total     228 
1 For example: If PID value is 0005948-041018, in the MRO 16-character field that’s left padded 
with 0s, it will be 000005948-041018. In current system, PID is 14-character long. 
 
 
  

---

## Page 10

File Transmission Layout – CCP Expanded Pool Netting Detail Format 
File Transmission Layout – CCP Expanded Pool Netting Detail Report–Format 10 
Pool Obligation Record 
Detail record containing a single netting activity item for a pool obligation record. 
Field Name Length Type Format Cobol 
Picture 
Description/Notes 
RPT-PND-DT4-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘04’ 
RPT-PND-DT4-POID 14 N ############## PIC 9(14) Pool [[ID]] 
(zero- padded) 
RPT-PND-DT4-BUY-
SELL-CODE 
1 A B or S PIC X(01) Buy/Sell Code 
RPT-PND-DT4-SETTL-
DATE 
8 N YYYYMMDD PIC 9(08) [[settlement]] Date 
RPT-PND-DT4-DLVRY-
DATE 
8 N YYYYMMDD PIC 9(08) Delivery Date 
RPT-PND-DT4-CONTRA-
[[ID]] 
4 A XXXX PIC X(04) Contra [[ID]] 
RPT-PND-DT4-LONG-
ORIG-FACE 
15 N ############### PIC 9(15) Long Original Face (zero-
padded) 
RPT-PND-DT4-LONG-
CURR-FACE 
17 N ################# PIC 
9(15)V9(02) 
Long Current Face (zero-
padded) 
RPT-PND-DT4-SHORT-
ORIG-FACE 
15 N ############### PIC 9(15) Short Original Face (zero-
padded) 
RPT-PND-DT4-SHORT-
CURR-FACE 
17 N ################# PIC 
9(15)V9(02) 
Short Current Face (zero-
padded) 
RPT-PND-DT4-DEBIT-
NET-MONEY 
15 N ############### PIC 
9(13)V9(02) 
Debit Net Money (zero-padded) 
RPT-PND-DT4-CREDIT-
NET- MONEY 
15 N ############### PIC 
9(13)V9(02) 
Credit Net Money (zero-padded) 
FILLER 97 A AAAA… PIC X(97) Filler 
   Total     228 
 
  
  

---

## Page 11

File Transmission Layout – CCP Expanded Pool Netting Detail Format 
File Transmission Layout – CCP Expanded Pool Netting Detail Report–Format 11 
   
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PND-DT99-CARD-CODE 2 N ## PIC 9(02) Card code = ‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler 
RPT-PND-DT99-ACCT 4 A AAAA PIC X(04) Account Symbol 
FILLER 1 A A PIC X(01) Filler 
RPT-PND-DT99-LOGICAL-
COUNT 
7 N ####### PIC 9(07) Logical Record 
Count (zero- 
padded) 
FILLER 1 A A PIC X(01) Filler 
RPT-PND-DT99- PHYSICAL- 
COUNT 
7 N ####### PIC 9(07) Physical Record 
Count (zero- 
padded) 
FILLER 193 A AAAA… PIC 9(193) Filler 
Total   228 
 
 
 
 
 

---

## Page 12

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 