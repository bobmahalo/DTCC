---
title: "CCP Pool Compared Pool Instruct NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs154_mro_file_transmission_layout_CCP%20Compared%20Pool%20Instruct%20NDM%20Format.pdf"
pages: 10
size: "282.5 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# CCP Pool Compared Pool Instruct NDM Format

**Original File:** [mbs154_mro_file_transmission_layout_CCP Compared Pool Instruct NDM Format.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs154_mro_file_transmission_layout_CCP%20Compared%20Pool%20Instruct%20NDM%20Format.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 282.5 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUT – CCP POOL COMPARED POOL INSTRUCT 
NDM FORMAT   
VERSION 1.03 
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
Publication Code: MBS154 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout - CCP Compared Pool Instruct NDM Format 

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
Compared Pool Instruct Detail Record (Card Code 02) .................................................................................. 5 
Trailer Control Record (Card Code 99) ........................................................................................................... 5 
Format Codes .................................................................................................................................................... 5 
File Transmission Layout – CCP COMpared Pool Instruct– NDM Format ..................................................... 6 
Header ................................................................................................................................................................ 6 
Pool Instruct Status Item Detail Record .............................................................................................................. 7 
Trailer .................................................................................................................................................................. 9 
 

---

## Page 4

File Transmission Layout – CCP Pool Compared Pool Instruct NDM Format 
Version Control Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
4/1/2013 Original MBSD Initial Version 
7/16/2015 1.0 C. Swords Updated to support [[Novation]]: 
• Add Card Code 02, field RPT-CPI-DT2-TRADE-DATE (Trade 
Date) 
10/12/2015 1.01 C. Swords Made following updates: 
• Add Card Code 02, field RPT-CPI-DT2-EPN-REF (EPN Pool 
Reference) 
8/15/2016 1.02 C. Swords Made following informational changes: 
• Standard title page and revision history 
10/6/2016   Made the following changes: 
• In Card Code 02 (COMPARED POOL INSTRUCT DETAIL 
RECORD), field Trade Date (RPT-CPI-DT2-TRADE-DATE), 
updated Type from N to A, and Cobol Picture from PIC 9(08) to 
X(08), due to fact that this field is blank for PIDs with non-
[[Novation]]-eligible CUSIPs 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
 
  

---

## Page 5

File Transmission Layout – CCP Pool Compared Pool Instruct NDM Format 
File Transmission Layout Overview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
CCP Pool Instruct Activity Report NDM Format 
Purpose 
Reflects current day’s Compared Pool Instructs (“PIDs”) and their current state. 
Frequency 
Daily. 
Record Layouts 
*All records are of equal length - 228 bytes. 
*There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 through 
02, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Compared Pool Instruct Detail Record (Card Code 02) 
Detail record containing a single status item for a compared pool instruct record.   
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

File Transmission Layout – CCP Pool Compared Pool Instruct NDM Format 
File Transmission Layout – CCP COMpared Pool Instruct– NDM Format 6 
FILE TRANSMISSION LAYOUT – CCP COMPARED POOL 
INSTRUCT– NDM FORMAT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-CPI-DT1-CARD-CODE 2 N ## PIC 9(02) Card code = ‘01’ 
RPT-CPI-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report [[ID]] = ‘MB8006-N” 
RPT-CPI-DT1-ACC-AGG-[[ID]]      
    RPT-CPI-DT1-PART-[[ID]] 3 N ### PIC 9(03) [[participant]] [[ID]] 
    RPT-CPI-DT1-AGG 2 A/N ## PIC 9(02) Aggregate 
RPT-CPI-DT1-ACCT 4 A AAAA PIC X(04) Account Symbol 
RPT-CPI-DT1-BUS-DATE 8 N YYYYMMDD PIC 9(08) Date of Report 
FILLER 201 A AAAA… PIC X(201) Filler 
Total   228 
  

---

## Page 7

File Transmission Layout – CCP Pool Compared Pool Instruct NDM Format 
File Transmission Layout – CCP COMpared Pool Instruct– NDM Format 7 
Pool Instruct Status Item Detail Record 
Detail record containing a single status item for a compared pool instruct record.   
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-CPI-DT2-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘02’ 
RPT-CPI-DT2-SETTLE-
MONTH 
6 N YYYYMM PIC 9(06) [[settlement]] Month 
RPT-CPI-DT2-TBA-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-CPI-DT2-POOL-
NUMBER 
6 A/N XXXXXX PIC X(06) Pool Number (zero- 
padded) 
RPT-CPI-DT2-POOL-
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) Pool [[CUSIP]] 
RPT-CPI-DT2-
MARKET-PRICE 
12 N ############ PIC 9(03)V9(09) Market Price (zero- 
padded) 
RPT-CPI-DT2-STATUS-
CODE 
4 A AAAA PIC X(04) Status Code (space- 
padded) 
RPT-CPI-DT2-CID 16 N ################ PIC 9(16) Compared Pool [[ID]] 
(zero- padded) 
RPT-CPI-DT2-BUY-
SELL-CODE 
1 A B or S PIC X(01) Buy/Sell Code 
RPT-CPI-DT2-XREF 16 A/N XXXXXXXXXXXXXXXX PIC X(16) X-Reference 
RPT-CPI-DT2-PID 16 A/N XXXXXXXXXXXXXXXX PIC X(16) Pool [[ID]] 
(space- padded) 
RPT-CPI-DT2-ENTRY-
DATE 
8 N YYYYMMDD PIC 9(08) Entry Date 
RPT-CPI-DT2-COMP-
DATE 
8 N YYYYMMDD PIC 9(08) Comparison Date 
RPT-CPI-DT2-SETTL-
DATE 
8 N YYYYMMDD PIC 9(08) [[settlement]] Date 
RPT-CPI-DT2-DLVRY-
DATE 
8 N YYYYMMDD PIC 9(08) Delivery Date 
RPT-CPI-DT2-CTRA-
CONTRA-AGG 
     
     RPT-CPI-DT2-CTRA- 
     PART-[[ID]] 
3 N ### PIC 9(03) Contra [[participant]] [[ID]] 
     RPT-CPI-DT2-CTRA-  
     AGG 
2 A/N ## PIC 9(02) Contra Aggregate 

---

## Page 8

File Transmission Layout – CCP Pool Compared Pool Instruct NDM Format 
File Transmission Layout – CCP COMpared Pool Instruct– NDM Format 8 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-CPI-DT2-
CONTRA-[[ID]] 
4 A AAAA PIC X(04) Contra [[ID]] 
RPT-CPI-DT2-ORIG-
FACE 
15 N ############### PIC 9(15) Original Face (zero- 
padded) 
RPT-CPI-DT2-CURR-
FACE 
17 N ################# PIC 9(15)V9(02) Current Face (zero- 
padded) 
RPT-CPI-DT2-PRICE 15 N ############### PIC 
9(03)V9(12) 
Trade Price (zero- 
padded) 
RPT-CPI-DT2-NET-
MONEY 
15 N ############### PIC 9(13)V9(02) Net Money (zero- 
padded) 
RPT-CPI-DT2-CDR 3 A Y-I, Y-P, Y-T or N PIC X(03) Customer Delivery 
Request Indicator 
(space- padded) 
RPT-CPI-DT2-
REPRICE 
1 A Y or N PIC X(01) Reprice Indicator 
RPT-CPI-DT2-TRADE-
DATE 
8 A YYYYMMDD PIC X(08) Trade Date 
RPT-CPI-DT2-EPN-REF 16 A/N ################ PIC X(16) EPN Pool Reference 
Total  228 

---

## Page 9

File Transmission Layout – CCP Pool Compared Pool Instruct NDM Format 
File Transmission Layout – CCP COMpared Pool Instruct– NDM Format 9 
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-CPI-DT99-CARD-CODE 2 N ## PIC 9(02) Card code =‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler 
RPT-CPI-DT99-ACCT 4 A AAAA PIC X(04) Account Symbol 
FILLER 1 A A PIC X(01) Filler 
RPT-CPI-DT99-LOGICAL-
COUNT 
7 N ####### PIC 9(07) Logical Record 
Count (zero- 
padded) 
FILLER 1 A A PIC X(01) Filler 
RPT-CPI-DT99-PHYSICAL-
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