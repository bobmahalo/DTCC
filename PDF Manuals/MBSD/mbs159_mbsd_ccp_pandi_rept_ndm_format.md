---
title: "CCP Pool Obligation Pending Settlement Report NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs159_mbsd_ccp_pandi_rept_ndm_format.pdf"
pages: 10
size: "270.5 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# CCP Pool Obligation Pending Settlement Report NDM Format

**Original File:** [mbs159_mbsd_ccp_pandi_rept_ndm_format.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs159_mbsd_ccp_pandi_rept_ndm_format.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 270.5 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUTS FOR MBSD CCP P&I REPORT NDM FORMAT  
VERSION 1.00 
NOVEMBER 18, 2008 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: November 18, 2008 
Publication Code: MBS159 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layouts for MBSD CCP P&I Report – NDM Format 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................... 4 
File Transmission Layout Overview ................................................................................................................... 5 
MBSD CCP P&I Report - NDM Format .............................................................................................................. 5 
Purpose ............................................................................................................................................................. 5 
Frequency.......................................................................................................................................................... 5 
Record Layouts ................................................................................................................................................. 5 
Account/Report Header Records (Card Code 01) ........................................................................................... 5 
Pool Obligation P&I Detail Record (Card Code 02) ......................................................................................... 5 
Trailer Control Record (Card Code 99) ........................................................................................................... 5 
Format Codes .................................................................................................................................................... 5 
File Transmission Layout FOr P&I Report – NDM Format ............................................................................... 6 
Header ................................................................................................................................................................ 6 
Pool Obligation P&I Detail Record ...................................................................................................................... 7 
Trailer .................................................................................................................................................................. 9 
 

---

## Page 4

File Transmission Layouts For MBSD CCP P&I Report NDM Format 
Version Control Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
11/18/2008 Original MBSD Initial Version 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
 
  

---

## Page 5

File Transmission Layouts For MBSD CCP P&I Report NDM Format 
File Transmission Layout Overview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
MBSD CCP P&I Report - NDM Format  
Purpose 
The P&I Report reflects [[FICC]] P&I calculations. 
Frequency 
Daily. 
Record Layouts 
*All records are of equal length - 228 bytes. 
*There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Pool Obligation P&I Detail Record (Card Code 02) 
Detail record containing P&I associated with a failing pool obligation and record date. 
Trailer Control Record (Card Code 99) 
Trailer record indicates the end of the report for the recipient account. 
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

## Page 6

File Transmission Layouts For MBSD CCP P&I Report NDM Format 
File Transmission Layout FOr P&I Report – NDM Format 6 
FILE TRANSMISSION LAYOUT FOR P&I REPORT – NDM 
FORMAT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Format Cobol Picture Description/Comments 
RPT-PNI-DT1-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘01’ 
RPT-PNI-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report [[ID]] = ‘MB8012-N” 
RPT-PNI-DT1-ACC-AGG-
[[ID]] 
     
RPT-PNI-DT1-PART-[[ID]] 3 N ### PIC 9(03) [[participant]] [[ID]] 
RPT-PNI-DT1-AGG 2 A/N ## PIC 9(02) Aggregate 
RPT-PNI-DT1-ACCT 4 A AAAA PIC X(04) Account Symbol 
RPT-PNI-DT1-BUS-DATE 8 N YYYYMMDD PIC 9(08) Date of Report 
FILLER 201 A AAAA… PIC X(201) Filler 
Total        228 
 
  

---

## Page 7

File Transmission Layouts For MBSD CCP P&I Report NDM Format 
File Transmission Layout FOr P&I Report – NDM Format 7 
Pool Obligation P&I Detail Record 
Detail record containing P&I associated with a failing pool obligation and record date. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PNI-DT2-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘02’ 
RPT-PNI-DT2-
SETTLE-MONTH 
6 N YYYYMM PIC 9(06) [[settlement]] Month 
RPT-PNI-DT2-TBA-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-PNI-DT2-POOL-
NUMBER 
6 A/N XXXXXX PIC X(06) Pool Number (zero-
padded) 
RPT-PNI-DT2-POOL-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) Pool [[CUSIP]] 
RPT-PNI-DT2-
STATUS-CODE 
4 A AAAA PIC X(04) Status Code (space-
padded) 
RPT-PNI-DT2-BUY-
SELL-CODE 
1 A B or S PIC X(01) Buy/Sell Code 
RPT-PNI-DT2-POID 14 N ############## PIC 9(14) Pool Obligation [[ID]] (zero-
padded) 
RPT-PNI-DT2-SETTL-
DATE 
8 N YYYYMMDD PIC 9(08) [[settlement]] Date 
RPT-PNI-DT2-DLVRY-
DATE 
8 N YYYYMMDD PIC 9(08) Delivery Date 
RPT-PNI-DT2-ORIG-
FACE 
15 N ############### PIC 9(15) Original Face (zero-
padded) 
RPT-PNI-DT2-CURR-
FACE-SD 
17 N ################# PIC 
9(15)V9(02) 
Current Face on 
[[settlement]] Date (zero-
padded) 
RPT-PNI-DT2-PRICE 15 N ############### PIC 
9(03)V9(12) 
Obligation Price (zero-
padded) 
RPT-PNI-DT2-
RECORD-DATE 
8 N YYYYMMDD PIC 9(08) Record Date this P&I 
payment relates to 
RPT-PNI-DT2-CURR-
FACTOR-DATE 
8 N YYYYMMDD PIC 9(08) Factor date for this record 
date’s payment (Current 
Factor Date) 
RPT-PNI-DT2-CURR-
FACTOR 
12 N ############ PIC 9(3)V9(9) Factor for this record 
date’s payment (Current 
Factor). 
Note that if this factor is 
not yet known, then this 
field will be all zeroes and 

---

## Page 8

File Transmission Layouts For MBSD CCP P&I Report NDM Format 
File Transmission Layout FOr P&I Report – NDM Format 8 
Field Name Length Type Format Cobol Picture Description/Notes 
the Blackout indicator set 
to Y. 
RPT-PNI-DT2-PREV-
FACTOR-DATE 
8 N YYYYMMDD PIC 9(08) Previous factor date 
RPT-PNI-DT2-PREV-
FACTOR 
12 N ############ PIC 9(3)V9(9) Previous factor 
RPT-PNI-DT2-CURR-
FACE-REVISED 
17 N ################# PIC 
9(15)V9(02) 
Revised Current Face 
using Current Factor. 
Note that if the Blackout 
indicator is set to Y, this 
field will be all zeroes. 
RPT-PNI-DT2-PRIN 15 N ############### PIC 
9(13)V9(02) 
Principal Payment (zero- 
padded). 
Note that if the Blackout 
indicator is set to Y, this 
field will be all zeroes. 
RPT-PNI-DT2-PRIN-
CREDIT-DEBIT 
1 A C or D PIC X(01) Principal Payment Credit 
or Debit 
RPT-PNI-DT2-INT 15 N ############### PIC 
9(13)V9(02)
 
Interest Payment (zero-
padded). 
RPT-PNI-DT2-INT-
CREDIT-DEBIT 
1 A C or D PIC X(01) Interest Payment Credit or 
Debit 
RPT-PNI-DT2-P-N-I 15 N ############### PIC 
9(13)V9(02)
 
Total P&I Payment (zero- 
padded). 
Note that if the Blackout 
indicator is set to Y, this 
field will be all zeroes. 
RPT-PNI-DT2-P-N-I-
CREDIT-DEBIT 
1 A C or D PIC X(01) Total P & I Payment Credit 
or Debit 
RPT-PNI-DT2-
BLACKOUT 
1 A Y or N PIC X(01) Indicate if factor 
associated with the 
Current Factor Date is 
unknown. 
If so, the Current Factor, 
Revised Current Face, 
Principal Payment and 
Total P&I Payment will be 
all zeroes.
 
Total   228 
  

---

## Page 9

File Transmission Layouts For MBSD CCP P&I Report NDM Format 
File Transmission Layout FOr P&I Report – NDM Format 9 
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PNI-DT99-CARD-CODE 2 N ## PIC 9(02) Card code = ‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler 
RPT-PNI-DT99-ACCT 4 A AAAA PIC X(04) Account Symbol 
FILLER 1 A A PIC X(01) Filler 
RPT-PNI-DT99-LOGICAL-
COUNT 
7 N ####### PIC 9(07) Logical Record 
Count (zero- 
padded) 
FILLER 1 A A PIC X(01) Filler 
RPT-PNI-DT99-PHYSICAL-
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