---
title: "CCP Pool Obligation Activity Report NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs146_mro_ccp_pool_oblig_act.pdf"
pages: 9
size: "279.3 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# CCP Pool Obligation Activity Report NDM Format

**Original File:** [mbs146_mro_ccp_pool_oblig_act.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs146_mro_ccp_pool_oblig_act.pdf)  
**Category:** MBSD  
**Total Pages:** 9  
**File Size:** 279.3 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUT – CCP POOL OBLIGATION ACTIVITY NDM 
LAYOUT  
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
Publication Code: MBS146 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout - Pool Obligation Activity NDM Layout 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................... 4 
File Transmission Layout Overview ................................................................................................................... 5 
CCP Pool Obligation Activity Report NDM Format ............................................................................................. 5 
Purpose ............................................................................................................................................................. 5 
Frequency.......................................................................................................................................................... 5 
Record Layouts ................................................................................................................................................. 5 
Account/Report Header Records (Card Code 01) ........................................................................................... 5 
Pool Obligation Activity Detail Record (Card Code 02) ................................................................................... 5 
Trailer Control Record (Card Code 99) ........................................................................................................... 5 
Format Codes .................................................................................................................................................... 5 
File Transmission Layout – CCP Pool Obligation Activity– NDM Format ...................................................... 6 
Header ................................................................................................................................................................ 6 
Pool Obligation Activity Detail Record ................................................................................................................ 7 
Trailer .................................................................................................................................................................. 8 
 

---

## Page 4

File Transmission Layout – CCP Pool Obligation Activity NDM Layout 
Version Control Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
4/1/2013 Original MBSD Initial Version 
7/16/2016 1.0 C. Swords Made following enhancements to support [[Novation]]: 
In Card Code 02 (POOL OBLIGATION ACTIVITY DETAIL RECORD), 
added trade date using filter at end of record. 
8/24/2016 1.01 C. Swords Made following informational changes: 
• In Card Code 02 (POOL OBLIGATION ACTIVITY DETAIL RECORD), 
updated to reflect TMPG Charges output in production MRO 
(erroneously omit from documentation) 
• Standard title page and revision history 
10/6/2016 1.02 C. Swords Made the following changes: 
• In Card Code 02 (POOL OBLIGATION ACTIVITY DETAIL RECORD), 
field Trade Date (RPT-POS-DT2-TRADE-DATE), updated Type N to A, 
and Cobol Picture from PIC 9(08) to X(08), due to fact that this field is 
blank for [[obligations]] resulting from  generic TBA activity 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
 
  

---

## Page 5

File Transmission Layout – CCP Pool Obligation Activity NDM Layout 
File Transmission Layout Overview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
CCP Pool Obligation Activity Report NDM Format 
Purpose 
Reflects creation of and all subsequent updates to Pool [[obligations]] (POIDs) 
Frequency 
Daily. 
Record Layouts 
*All records are of equal length - 228 bytes. 
*There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Pool Obligation Activity Detail Record (Card Code 02) 
Detail record containing a single status item for a pool obligation record. 
Trailer Control Record (Card Code 99) 
Trailer record indicates the end of the report for the recipient account. 
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

## Page 6

File Transmission Layout – CCP Pool Obligation Activity NDM Layout 
File Transmission Layout – CCP Pool Obligation Activity– NDM Format 6 
FILE TRANSMISSION LAYOUT – CCP POOL 
OBLIGATION ACTIVITY– NDM FORMAT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-POA-DT1-CARD-CODE 2 N ## PIC 9(02) Card code = ‘01’ 
RPT-POA-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report [[ID]] = ‘MB8005-N” 
RPT-POA-DT1-ACC-AGG-[[ID]]      
     RPT-POA-DT1-PART-[[ID]] 3 N ### PIC 9(03) [[participant]] [[ID]] 
     RPT-POA-DT1-AGG 2 A/N ## PIC 9(02) Aggregate 
RPT-POA-DT1-ACCT 4 A AAAA PIC X(04) Account Symbol 
RPT-POA-DT1-BUS-DATE 8 N YYYYMMDD PIC 9(08) Date of Report 
FILLER 201 A AAAA… PIC X(201) Filler 
Total   228 
 
  

---

## Page 7

File Transmission Layout – CCP Pool Obligation Activity NDM Layout 
File Transmission Layout – CCP Pool Obligation Activity– NDM Format 7 
Pool Obligation Activity Detail Record 
Detail record containing a single status item for a pool obligation record. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-POA-DT2-CARD-CODE 2 N ## PIC 9(02) Card code = ‘02’ 
RPT-POA-DT2-SETTLE-
MONTH 
6 N YYYYMM PIC 9(06) [[settlement]] Month 
RPT-POA-DT2-TBA-[[CUSIP]] 9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-POA-DT2-POOL-
NUMBER 
6 A/N XXXXXX PIC X(06) Pool Number (zero-
padded) 
RPT-POA-DT2-POOL-[[CUSIP]] 9 A/N XXXXXXXXX PIC X(09) Pool [[CUSIP]] 
RPT-POA-DT2-ACTIVITY-
CODE 
4 A AAAA PIC X(04) Activity Code (space- 
padded) 
RPT-POA-DT2-STATUS-
CODE 
4 A AAAA PIC X(04) Status Code (space- 
padded) 
RPT-POA-DT2-POID 14 N ############## PIC 9(14) Pool Obligation [[ID]] (zero-
padded) 
RPT-POA-DT2-BUY-SELL-
CODE 
1 A B or S PIC X(01) Buy/Sell Code 
RPT-POA-DT2-SETTL-DATE 8 N YYYYMMDD PIC 9(08) [[settlement]] Date 
RPT-POA-DT2-DLVRY-DATE 8 N YYYYMMDD PIC 9(08) Delivery Date 
RPT-POA-DT2-CONTRA-[[ID]] 4 A AAAA PIC X(04) Contra [[ID]] 
RPT-POA-DT2-ORIG-FACE 15 N ############### PIC 9(15) Original Face (zero-
padded) 
RPT-POA-DT2-CURR-FACE 17 N ################# PIC 9(15)V9(02) Current Face (zero-
padded) 
RPT-POA-DT2-PRICE 15 N ############### PIC 9(03)V9(12) Trade Price (zero-
padded) 
RPT-POA-DT2-EXPECT-NET- 
MONEY 
15 N ############### PIC 9(13)V9(02) Expected Net Money 
(zero- padded) 
RPT-POA-DT2-ACTUAL- 
CLEAR- MONEY 
15 N ############### PIC 9(13)V9(02) Actual Clearance Money 
(zero- padded) 
RPT-FAL-DT2-TMPG 15 N ############### PIC 9(13)V9(02) TMPG Charges (zero- 
padded) 
RPT-FAL-DT2-TMPG-CREDIT- 
DEBIT 
1 A C or D PIC X(01) TMPG Credit or Debit 
RPT-POA-DT2-TRADE-DATE 8 A YYYYMMDD PIC X(08) Trade Date, if exist 
FILLER 52 A AAAA… PIC X(52) Filler 
Total   228 

---

## Page 8

File Transmission Layout – CCP Pool Obligation Activity NDM Layout 
File Transmission Layout – CCP Pool Obligation Activity– NDM Format 8 
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-POA-DT99-CARD-CODE 2 N ## PIC 9(02) Card code = ‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler 
RPT-POA-DT99-ACCT 4 A AAAA PIC X(04) Account Symbol 
FILLER 1 A A PIC X(01) Filler 
RPT-POA-DT99-LOGICAL-
COUNT 
7 N ####### PIC 9(07) Logical Record 
Count (zero- 
padded) 
FILLER 1 A A PIC X(01) Filler 
RPT-POA-DT99-PHYSICAL-
COUNT 
7 N ####### PIC 9(07) Physical Record 
Count (zero-
padded) 
FILLER 193 A AAAA… PIC 9(193) Filler 
Total   228 
 
 
 
 
 

---

## Page 9

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 