---
title: "CCP PID TAP Detail MRO Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs149_mro_ccp_pid_tap_det.pdf"
pages: 10
size: "277.9 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# CCP PID TAP Detail MRO Format

**Original File:** [mbs149_mro_ccp_pid_tap_det.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs149_mro_ccp_pid_tap_det.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 277.9 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUT – CCP PID TAP DETAIL MRO FORMAT  
VERSION 1.01 
AUGUST 24, 2016 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: August 24, 2016 
Publication Code: MBS149 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout - CCP PID TAP Detail MRO Format 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................... 4 
File Transmission Layout Overview ................................................................................................................... 5 
CCP Pool Instruct TAP Detail Report NDM Format ........................................................................................... 5 
Purpose ............................................................................................................................................................. 5 
Frequency.......................................................................................................................................................... 5 
Record Layouts ................................................................................................................................................. 5 
Account/Report Header Records (Card Code 01) ........................................................................................... 5 
Pool Instruct TAP Detail Record (Card Code 02) ............................................................................................ 5 
Trailer Control Record (Card Code 99) ........................................................................................................... 5 
Format Codes .................................................................................................................................................... 6 
File Transmission Layout – CCP Pool Instruct Tap Detail– NDM Format ...................................................... 7 
Header ................................................................................................................................................................ 7 
Pool Instruct TAP Detail Record ......................................................................................................................... 8 
Trailer .................................................................................................................................................................. 9 
 

---

## Page 4

File Transmission Layout – CCP PID TAP Detail MRO FOrmat 
Version Control Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
4/1/2013 Original MBSD Initial Version 
7/16/2015 1.0 C. Swords Updated to support [[Novation]]: 
• Update description to indicate that MRO includes results of 
Expanded Pool Net on SIFMA CSD-1.  
8/24/2016 1.01 C. Swords Made following informational changes: 
• Standard title page and revision history 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
 
  

---

## Page 5

File Transmission Layout – CCP PID TAP Detail MRO FOrmat 
File Transmission Layout Overview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
CCP Pool Instruct TAP Detail Report NDM Format 
Purpose 
The Pool Instruct TAP Detail Report reflects the individual PIDs processed in the current day’s daily, and if 
SIFMA 24hr day, expanded Pool Netting cycles. The PIDs processed are reflected, along with their associated 
Transaction Adjustment Payment (“TAP”). 
Frequency 
Daily. 
Record Layouts 
*All records are of equal length - 228 bytes. 
* There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Pool Instruct TAP Detail Record (Card Code 02) 
Detail record containing a single pool instruct TAP record. 
Trailer Control Record (Card Code 99) 
Trailer record indicates the end of the report for the recipient account. 
  

---

## Page 6

File Transmission Layout – CCP PID TAP Detail MRO FOrmat 
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

File Transmission Layout – CCP PID TAP Detail MRO FOrmat 
File Transmission Layout – CCP Pool Instruct Tap Detail– NDM Format 7 
FILE TRANSMISSION LAYOUT – CCP POOL INSTRUCT 
TAP DETAIL– NDM FORMAT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PIT-DT1-CARD-CODE 2 N ## PIC 9(02) Card code = ‘01’ 
RPT-PIT-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report [[ID]] = ‘MB8013-N” 
RPT-PIT-DT1-ACC-AGG-[[ID]]      
     RPT-PIT-DT1-PART-[[ID]] 3 N ### PIC 9(03) [[participant]] [[ID]] 
     RPT-PIT-DT1-AGG 2 N ## PIC 9(02) Aggregate Number 
RPT-PIT-DT1-ACCT 4 A AAAA PIC X(04) Account Symbol 
RPT-PIT-DT1-BUS-DATE 8 N YYYYMMDD PIC 9(08) Date of Report 
FILLER 201 A AAAA… PIC X(201) Filler 
Total   228 
  

---

## Page 8

File Transmission Layout – CCP PID TAP Detail MRO FOrmat 
File Transmission Layout – CCP Pool Instruct Tap Detail– NDM Format 8 
Pool Instruct TAP Detail Record  
Detail record containing a single pool instruct TAP record. 
Field Name Length Type Format Cobol 
Picture 
Description/Notes 
RPT-PIT-DT2-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘02’ 
RPT-PIT-DT2-SETTLE- 
MONTH 
6 N YYYYMM PIC 9(06) [[settlement]] Month 
RPT-PIT-DT2-TBA-[[CUSIP]] 9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-PIT-DT2-POOL-
NUMBER 
6 A/N XXXXXX PIC X(06) Pool Number (zero- padded) 
RPT-PIT-DT2-POOL-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) Pool [[CUSIP]] 
RPT-PIT-DT2-DLVRY-
DATE 
8 N YYYYMMDD PIC 9(08) Delivery Date 
RPT-PIT-DT2-PID 16 A/N XXXXXXXXXXXXXXXX PIC X(16) Pool [[ID]] 
(space-padded) 
RPT-PIT-DT2-XREF 16 A/N XXXXXXXXXXXXXXXX PIC X(16) X-Reference (space- padded) 
RPT-PIT-DT2-BUY-SELL-
CODE 
1 A B or S PIC X(01) Buy/Sell Code 
RPT-PIT-DT2-CTRA-
CONTRA- AGG 
     
     RPT-PIT-DT2-CTRA-    
     PART-[[ID]] 
3 N ### PIC 9(03) Contra [[participant]] [[ID]] 
     RPT-PIT-DT2-CTRA- 
     AGG 
2 N ## PIC 9(02) Contra Aggregate 
RPT-PIT-DT2-CONTRA-[[ID]] 4 A AAAA PIC X(04) Contra [[ID]] 
RPT-PIT-DT2-ORIG-FACE 15 N ############### PIC 9(15) Original Face (zero- padded) 
RPT-PIT-DT2-CURR-
FACE 
17 N ################# PIC 
9(15)V9(02) 
Current Face (zero- padded) 
RPT-PIT-DT2-ORIG-
TRADE- PRICE 
15 N ############### PIC 
9(03)V9(12) 
Original Trade Price (zero-
padded) 
RPT-PIT-DT2-SETTLE-
VALUE 
17 N ################# PIC 
9(15)V9(02) 
[[settlement]] Value (zero-padded) 
RPT-PIT-DT2-[[FICC]]-
PRICE 
15 N ############### PIC 
9(03)V9(12) 
[[FICC]] Price (zero-padded) 
RPT-PIT-DT2-CLEAR-
[[FICC]]- VALUE 
17 N ################# PIC 
9(15)V9(02) 
Clearance Value vs. [[FICC]] 
(zero-padded) 

---

## Page 9

File Transmission Layout – CCP PID TAP Detail MRO FOrmat 
File Transmission Layout – CCP Pool Instruct Tap Detail– NDM Format 9 
Field Name Length Type Format Cobol 
Picture 
Description/Notes 
RPT-PIT-DT2-TAP 17 N ################# PIC 
9(15)V9(02) 
Transaction 
Adjustment Payment (zero-
padded) 
RPT-PIT-DT2-TAP-
CREDIT- DEBIT 
1 A C or D PIC X(01) Transaction Adjustment 
Payment Credit or Debit 
FILLER 32 A AAAA… PIC X(32) Filler 
Total   228 
    
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PIT-DT99-CARD-CODE 2 N ## PIC 9(02) Card code = ‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler 
RPT-PIT-DT99-ACCT 4 A AAAA PIC X(04) Account Symbol 
FILLER 1 A A PIC X(01) Filler 
RPT-PIT-DT99-LOGICAL-
COUNT 
7 N ####### PIC 9(07) Logical Record 
Count (zero- 
padded) 
FILLER 1 A A PIC X(01) Filler 
RPT-PIT-DT99-PHYSICAL-
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