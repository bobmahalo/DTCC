---
title: "CCP Pool Instruct Activity NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs153_mro_file_transmission_layout_CCP%20Pool%20Instruct%20Activity%20NDM%20Format.pdf"
pages: 10
size: "281.9 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# CCP Pool Instruct Activity NDM Format

**Original File:** [mbs153_mro_file_transmission_layout_CCP Pool Instruct Activity NDM Format.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs153_mro_file_transmission_layout_CCP%20Pool%20Instruct%20Activity%20NDM%20Format.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 281.9 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUT – CCP POOL INSTRUCT ACTIVITY NDM 
FORMAT   
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
 
 
Doc Date: October 6,2016 
Publication Code: MBS153 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout - CCP Pool Instruct Activity NDM Format 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................... 4 
File Transmission Layout Overview ................................................................................................................... 5 
CCP Pool Instruct Activity Report NDM Format ................................................................................................. 5 
Purpose ............................................................................................................................................................. 5 
Frequency.......................................................................................................................................................... 5 
Record Layouts ................................................................................................................................................. 5 
Account/Report Header Records (Card Code 01) ........................................................................................... 5 
Pool Instruct Activity Item Detail Record (Card Code 02) ............................................................................... 5 
Trailer Control Record (Card Code 99) ........................................................................................................... 5 
Format Codes .................................................................................................................................................... 5 
File Transmission Layout – CCP Pool Instruct Activity– NDM Format .......................................................... 6 
Header ................................................................................................................................................................ 6 
Pool Instruct Activity Item Detail Record ............................................................................................................ 7 
Trailer .................................................................................................................................................................. 9 
 

---

## Page 4

File Transmission Layout – CCP Pool Instruct Activity NDM Format 
Version Control Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
4/1/2013 Original C. Swords Initial Version 
7/16/2016 1.0 C. Swords Updated to support [[Novation]]: 
• In Card Code 02 (POOL INSTRUCT ACTIVITY DETAIL 
RECORD), added trade date and EPN Pool Reference using 
filler at end of record. 
8/24/2016 1.01 C. Swords Made following informational changes: 
• Standard title page and revision history 
10/6/2016 1.02 C. Swords Made the following changes: 
• In Card Code 02 (POOL INSTRUCT ACTIVITY ITEM DETAIL 
RECORD), field Trade Date (RPT-PIA-DT2-TRADE-DATE), 
updated Type from N to A, and Cobol Picture from PIC 9(08) to 
X(08), due to fact that this field is blank for PIDs with non-
[[Novation]]-eligible CUSIPs 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
 
  

---

## Page 5

File Transmission Layout – CCP Pool Instruct Activity NDM Format 
File Transmission Layout Overview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
CCP Pool Instruct Activity Report NDM Format 
Purpose 
The Pool Instruct Activity Report reflects newly compared Pool Instructs (PID’s) and all subsequent updates. 
Frequency 
Daily. 
Record Layouts 
*All records are of equal length - 228 bytes. 
*There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Pool Instruct Activity Item Detail Record (Card Code 02) 
Detail record containing a single activity item for a pool instruct record. 
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

File Transmission Layout – CCP Pool Instruct Activity NDM Format 
File Transmission Layout – CCP Pool Instruct Activity– NDM Format 6 
FILE TRANSMISSION LAYOUT – CCP POOL INSTRUCT 
ACTIVITY– NDM FORMAT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PIA-DT1-CARD-CODE 2 N ## PIC 9(02) Card code = ‘01’ 
RPT-PIA-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report [[ID]] = ‘MB8004-N’ 
RPT-PIA-DT1-ACC-AGG-[[ID]]      
     RPT-PIA-DT1-PART-[[ID]] 3 N ### PIC 9(03) [[participant]] [[ID]] 
     RPT-PIA-DT1-AGG 2 A/N ## PIC 9(02) Aggregate 
RPT-PIA-DT1-ACCT 4 A AAAA PIC X(04) Account Symbol 
RPT-PIA-DT1-BUS-DATE 8 N YYYYMMDD PIC 9(08) Date of Report 
FILLER 201 A AAAA… PIC X(201) Filler 
Total   228 
  

---

## Page 7

File Transmission Layout – CCP Pool Instruct Activity NDM Format 
File Transmission Layout – CCP Pool Instruct Activity– NDM Format 7 
Pool Instruct Activity Item Detail Record 
Detail record containing a single activity item for a pool instruct record. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PIA-DT2-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘02’ 
RPT-PIA-DT2-SETTLE-
MONTH 
6 N YYYYMM PIC 9(06) [[settlement]] Month 
RPT-PIA-DT2-TBA-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-PIA-DT2-POOL-
NUMBER 
6 A/N XXXXXX PIC X(06) Pool Number (zero-
padded) 
RPT-PIA-DT2-POOL-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) Pool [[CUSIP]] 
RPT-PIA-DT2-
ACTIVITY-CODE 
4 A AAAA PIC X(04) Activity Code (space-
padded) 
RPT-PIA-DT2-STATUS-
CODE 
4 A AAAA PIC X(04) Status Code (space-
padded) 
RPT-PIA-DT2-CID 16 N ################ PIC 9(16) Compared Pool [[ID]] 
(zero- padded) 
RPT-PIA-DT2-BUY-
SELL-CODE 
1 A B or S PIC X(01) Buy/Sell Code 
RPT-PIA-DT2-XREF 16 A/N XXXXXXXXXXXXXXXX PIC X(16) X-Reference (space-
padded) 
RPT-PIA-DT2-PID 16 A/N XXXXXXXXXXXXXXXX PIC X(16) Pool [[ID]] 
(space- padded) 
RPT-PIA-DT2-ENTRY-
DATE 
8 N YYYYMMDD PIC 9(08) Entry Date 
RPT-PIA-DT2-COMP-
DATE 
8 N YYYYMMDD PIC 9(08) Comparison Date 
RPT-PIA-DT2-SETTL-
DATE 
8 N YYYYMMDD PIC 9(08) [[settlement]] Date 
RPT-PIA-DT2-DLVRY-
DATE 
8 N YYYYMMDD PIC 9(08) Delivery Date 
RPT-PIA-DT2-CTRA-
CONTRA- AGG 
     
     RPT-PIA-DT2-CTRA- 
     PART-[[ID]] 
3 N ### PIC 9(03) Contra [[participant]] [[ID]] 
     RPT-PIA-DT2-CTRA-     
     AGG 
2 A/N ## PIC 9(02) Contra Aggregate 

---

## Page 8

File Transmission Layout – CCP Pool Instruct Activity NDM Format 
File Transmission Layout – CCP Pool Instruct Activity– NDM Format 8 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PIA-DT2-
CONTRA-[[ID]] 
4 A AAAA PIC X(04) Contra [[ID]] 
RPT-PIA-DT2-ORIG-
FACE 
15 N ############### PIC 9(15) Original Face (zero-
padded) 
RPT-PIA-DT2-CURR-
FACE 
17 N ################# PIC 
9(15)V9(02) 
Current Face (zero-
padded) 
RPT-PIA-DT2-PRICE 15 N ############### PIC 
9(03)V9(12) 
Trade Price (zero-
padded) 
RPT-PIA-DT2-NET-
MONEY 
15 N ############### PIC 
9(13)V9(02) 
Net Money (zero-
padded) 
RPT-PIA-DT2-CDR 3 A Y-I, Y-P, Y-T or N PIC X(03) Customer Delivery 
Request Indicator 
(space- padded) 
RPT-PIA-DT2-REPRICE 1 A Y or N PIC X(01) Reprice Indicator 
RPT-PIA-DT2-TRADE-
DATE 
8 A YYYYMMDD PIC X(08) Trade Date 
RPT-PIA-DT2-EPN-REF 16 A/N XXXXXXXXXXXXXXXX PIC X(16) EPN Pool Reference 
FILLER 8 A AAAA… PIC X(8) Filler 
Total   228 

---

## Page 9

File Transmission Layout – CCP Pool Instruct Activity NDM Format 
File Transmission Layout – CCP Pool Instruct Activity– NDM Format 9 
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PIA-DT99-CARD-CODE 2 N ## PIC 9(02) Card code = ‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler 
RPT-PIA-DT99-ACCT 4 A AAAA PIC X(04) Account Symbol 
FILLER 1 A A PIC X(01) Filler 
RPT-PIA-DT99-LOGICAL-
COUNT 
7 N ####### PIC 9(07) Logical Record 
Count (zero-
padded) 
FILLER 1 A A PIC X(01) Filler 
RPT-PIA-DT99-PHYSICAL-
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