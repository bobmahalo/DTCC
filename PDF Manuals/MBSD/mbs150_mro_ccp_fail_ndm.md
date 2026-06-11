---
title: "CCP Fail NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs150_mro_ccp_fail_ndm.pdf"
pages: 10
size: "278.9 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# CCP Fail NDM Format

**Original File:** [mbs150_mro_ccp_fail_ndm.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs150_mro_ccp_fail_ndm.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 278.9 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUT – CCP FAIL NDM LAYOUT 
VERSION 1.02 
OCTOBER 6, 2016 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 6, 2016 
Publication Code: MBS150 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout – CCP Fail NDM Layout 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................... 4 
File Transmission Layout Overview ................................................................................................................... 5 
CCP Fail Report NDM Format ............................................................................................................................ 5 
Purpose ............................................................................................................................................................. 5 
Frequency.......................................................................................................................................................... 5 
Record Layouts ................................................................................................................................................. 5 
Account/Report Header Records (Card Code 01) ........................................................................................... 5 
Pool Obligation Fail Detail Record (Card Code 02) ......................................................................................... 5 
Trailer Control Record (Card Code 99) ........................................................................................................... 5 
Format Codes .................................................................................................................................................... 6 
File Transmission Layout – CCP Fail Report– NDM Format ............................................................................ 7 
Header ................................................................................................................................................................ 7 
Pool Obligation Fail Detail Record ...................................................................................................................... 8 
Trailer .................................................................................................................................................................. 9 
 

---

## Page 4

File Transmission Layout – CCP Fail NDM Layout 
Version Control Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
4/1/2013 Original MBSD Initial Version 
7/16/2016 1.0 C. Swords Updated to support [[Novation]]: 
• In Card Code 02 (POOL OBLIGATION FAIL DETAIL 
RECORD), added trade date using filler at end of record. 
8/15/2016 1.01 C. Swords Made following updates: 
• In Card Code 02 (POOL OBLIGATION FAIL DETAIL 
RECORD), updated to reflect TMPG Charges output in 
production MRO (erroneously omit from documentation) 
10/6/2016 1.02 C. Swords Made following changes: 
• In Card Code 02 (POOL OBLIGATION FAIL DETAIL RECORD), 
field Trade Date (RPT-FAL-DT2-TRADE- DATE), updated Type 
from N to A, and Cobol Picture from PIC 9(08) to X(08), due to 
fact that this field is blank for [[obligations]] resulting from generic 
TBA activity 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
 
  

---

## Page 5

File Transmission Layout – CCP Fail NDM Layout 
File Transmission Layout Overview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
CCP Fail Report NDM Format 
Purpose 
The Fail Report reflects all failing Pool [[obligations]] (POID’s) versus [[FICC]] (POID Delivery Date = Report Date) 
Frequency 
Daily. 
Record Layouts 
*All records are of equal length - 228 bytes. 
* There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Pool Obligation Fail Detail Record (Card Code 02) 
Detail record containing a single failing pool obligation record. 
Trailer Control Record (Card Code 99) 
Trailer record indicates the end of the report for the recipient account. 
  

---

## Page 6

File Transmission Layout – CCP Fail NDM Layout 
File Transmission Layout Overview 6 
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

File Transmission Layout – CCP Fail NDM Layout 
File Transmission Layout – CCP Fail Report– NDM Format 7 
FILE TRANSMISSION LAYOUT – CCP FAIL REPORT– 
NDM FORMAT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-FAL-DT1-CARD-CODE 2 N ## PIC 9(02) Card code = ‘01’ 
RPT-FAL-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report [[ID]] =‘MB8011-N” 
RPT-FAL-DT1-ACC-AGG-[[ID]]      
     RPT-FAL-DT1-PART-[[ID]] 3 N ### PIC 9(03) [[participant]] [[ID]] 
     RPT-FAL-DT1-AGG 2 A/N ## PIC 9(02) Aggregate 
RPT-FAL-DT1-ACCT 4 A AAAA PIC X(04) Account Symbol 
RPT-FAL-DT1-BUS-DATE 8 N YYYYMMDD PIC 9(08) Date of Report 
FILLER 201 A AAAA… PIC X(201) Filler 
Total   228 
  

---

## Page 8

File Transmission Layout – CCP Fail NDM Layout 
File Transmission Layout – CCP Fail Report– NDM Format 8 
Pool Obligation Fail Detail Record 
Detail record containing a single failing pool obligation record. 
Field Name Length Type Format Cobol 
Picture 
Description/Notes 
RPT-FAL-DT2-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘02’ 
RPT-FAL-DT2-SETTLE-
MONTH 
6 N YYYYMM PIC 9(06) [[settlement]] Month 
RPT-FAL-DT2-TBA-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-FAL-DT2-POOL-
NUMBER 
6 A/N XXXXXX PIC X(06) Pool Number (zero-padded) 
RPT-FAL-DT2-POOL-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) Pool [[CUSIP]] 
RPT-FAL-DT2-STATUS-
CODE 
4 A AAAA PIC X(04) Status Code (space-padded) 
RPT-FAL-DT2-POID 14 N ############## PIC 9(14) Pool Obligation [[ID]] (zero-padded) 
RPT-FAL-DT2-BUY-
SELL-CODE 
1 A B or S PIC X(01) Buy/Sell Code 
RPT-FAL-DT2-SETTL-
DATE 
8 N YYYYMMDD PIC 9(08) [[settlement]] Date 
RPT-FAL-DT2-DLVRY-
DATE 
8 N YYYYMMDD PIC 9(08) Delivery Date 
RPT-FAL-DT2-CONTRA-
[[ID]] 
4 A XXXX PIC X(04) Contra [[ID]] 
RPT-FAL-DT2-ORIG-
FACE 
15 N ############### PIC 9(15) Original Face (zero-padded) 
RPT-FAL-DT2-CURR-
FACE 
17 N ################# PIC 
9(15)V9(02) 
Current Face (zero-padded) 
RPT-FAL-DT2-PRICE 15 N ############### PIC 
9(03)V9(12) 
Trade Price (zero- padded) 
RPT-FAL-DT2-NET-
MONEY 
15 N ############### PIC 
9(13)V9(02) 
Net Money (zero- padded) 
RPT-FAL-DT2-P-AND-I 15 N ############### PIC 
9(13)V9(02)
 
Principal and Interest 
(zero- padded) 
RPT-FAL-DT2-P-AND-I-
CREDIT- DEBIT 
1 A C or D PIC X(01) Principal and 
Interest Credit or Debit 
RPT-FAL-DT2-TMPG 15 N ############### PIC 
9(13)V9(02) 
TMPG Charges (zero- padded) 

---

## Page 9

File Transmission Layout – CCP Fail NDM Layout 
File Transmission Layout – CCP Fail Report– NDM Format 9 
Field Name Length Type Format Cobol 
Picture 
Description/Notes 
RPT-FAL-DT2-TMPG-
CREDIT- DEBIT 
1 A C or D PIC X(01) TMPG Credit or Debit 
RPT-FAL-DT2-TRADE-
DATE 
8 A YYYYMMDD PIC X(08) Trade Date, if exists 
FILLER 55 A AAAA… PIC X(55) Filler 
Total   228 
    
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-FAL-DT99-CARD-CODE 2 N ## PIC 9(02) Card code = ‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler 
RPT-FAL-DT99-ACCT 4 A AAAA PIC X(04) Account Symbol 
FILLER 1 A A PIC X(01) Filler 
RPT-FAL-DT99-LOGICAL-
COUNT 
7 N ####### PIC 9(07) Logical Record 
Count (zero- 
padded) 
FILLER 1 A A PIC X(01) Filler 
RPT-FAL-DT99-PHYSICAL-
COUNT 
7 N ####### PIC 9(07) Physical Record 
Count (zero-
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