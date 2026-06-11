---
title: "Cash Trade Conversion Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs155_mro_cash_trade_conv_format.pdf"
pages: 12
size: "329.0 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# Cash Trade Conversion Format

**Original File:** [mbs155_mro_cash_trade_conv_format.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs155_mro_cash_trade_conv_format.pdf)  
**Category:** MBSD  
**Total Pages:** 12  
**File Size:** 329.0 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUT – CASH TRADE CONVERSION FORMAT 
VERSION 1.05 
MAY 9, 2018 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: May 9,2018 
Publication Code: MBS155 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layout – Cash Trade Conversion Format 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................... 4 
File Transmission Layout Overview ................................................................................................................... 5 
Cash Trade (Same Day Settle) Conversion Format ........................................................................................... 5 
Purpose ............................................................................................................................................................. 5 
Frequency.......................................................................................................................................................... 5 
Record Layouts ................................................................................................................................................. 5 
Account/Report Header Records (Card Code 01) ........................................................................................... 5 
Converted Trade Detail Record (Card Code 02) ............................................................................................. 5 
Converted Pool Instruct Detail Record (Card Code 03) .................................................................................. 5 
Resulting Pool Obligation Detail Record (Card Code 04) ............................................................................... 5 
Trailer Control Record (Card Code 99) ........................................................................................................... 5 
Format Codes .................................................................................................................................................... 6 
File Transmission Layout – Cash Trade (Same Day Settle) Conversion........................................................ 7 
Header ................................................................................................................................................................ 7 
Converted Trade Detail Record .......................................................................................................................... 8 
Converted PID Detail .......................................................................................................................................... 9 
Resulting POID Detail ....................................................................................................................................... 10 
 

---

## Page 4

File Transmission Layout – Cash Trade Conversion Format 
Version Control Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
7/16/2015 Original C. Swords Initial Version 
10/14/2015 1.01 C. Swords Made following updates: 
• Corrected length of Trade Number in Card Code 03 
8/24/2016 1.02 C. Swords Made following informational changes: 
• Standard title page and revision history 
10/27/2016 1.03 C. Swords Made following correction: 
• Card Code 03 Converted PID Detail Record – correct type of 
RPT-CRT3-PID-[[ID]] to be A/N (was N). 
• Card Code 04 Resulting POID Detail Record – correct type of 
RPT-CRT4-PID-[[ID]] to be A/N (was N). 
• Card Code 04 (RESULTING POID DETAIL RECORD), field 
Trade Date (RPT-CRT4-TRD-DATE), updated Type from N to 
A/N, and Cobol Picture from PIC 9(08) to X(08), due to fact that 
this field is blank for [[obligations]] resulting from generic TBA 
activity 
• Remove NDM from document name 
7/20/2017 1.04 C. Swords Made following informational changes: 
• Card Code 04 Resulting POID Detail Record – make comment 
that Trade [[ID]] (RPT-CRT4-ASC-TRADE-[[ID]], reflected as 
prefix/suffix) is only populated for SPT trades or STIP PIDs. 
4/17/2018 1.05 J. Xie Adding clarification on PID field format: 
• Clarify that PID-[[ID]] 16-character fixed-length alpha- numeric field 
is left padded with 2 zeros. 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
 
  

---

## Page 5

File Transmission Layout – Cash Trade Conversion Format 
File Transmission Layout Overview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
Cash Trade (Same Day Settle) Conversion Format  
Purpose 
Reflects impact on cash trades (Specified Pool Trades (“SPT”) and allocations) converted to Pool [[obligations]] 
(“POIDs”). 
Frequency 
Daily. 
Record Layouts 
*All records are of equal length - 228 bytes. 
*There are 5 different record types, each uniquely identified by card code, as follows: card codes 01 through 
04, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Converted Trade Detail Record (Card Code 02) 
Detail record containing a single converted trade record. 
Converted Pool Instruct Detail Record (Card Code 03) 
Detail record containing a single converted pool instruct record. 
Resulting Pool Obligation Detail Record (Card Code 04) 
Detail record containing a single resulting pool obligation record.   
Trailer Control Record (Card Code 99) 
Trailer record indicates the end of the report for the recipient account. 
  

---

## Page 6

File Transmission Layout – Cash Trade Conversion Format 
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

File Transmission Layout – Cash Trade Conversion Format 
File Transmission Layout – Cash Trade (Same Day Settle) Conversion 7 
FILE TRANSMISSION LAYOUT – CASH TRADE (SAME 
DAY SETTLE) CONVERSION 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Cobol Picture Description/Notes 
RPT-CRT1-CARD-CODE 2 N PIC 9(02) Header Record, Card code = ‘01’ 
RPT-CRT1-RPT-[[ID]] 8 A/N PIC X(08) Report [[ID]] = ‘MB8108-N’ 
RPT-CRT1-ACC-AGG-[[ID]]     
     RPT-CRT1-PART-[[ID]] 3 N PIC 9(03) [[participant]] [[ID]] 
     RPT-CRT1-AGG 2 N PIC 9(02) Aggregate 
RPT-CRT1-ACCT 4 A PIC X(04) Account Symbol 
RPT-CRT1-PART-NAME 40 A/N PIC X(40) [[participant]] Name 
RPT-CRT1-BUS-DATE 8 N PIC 9(08) Date of Report 
FILLER 161 A PIC X (161) Filler 
Total   228 
  

---

## Page 8

File Transmission Layout – Cash Trade Conversion Format 
File Transmission Layout – Cash Trade (Same Day Settle) Conversion 8 
Converted Trade Detail Record 
Detail record containing a single converted trade record. 
Field Name Length Type Cobol Picture Description/Notes 
RPT-CRT2-CARD-CODE 2 N PIC 9(02) Converted Trade Detail Record, Card code 
= ‘02’ 
RPT-CRT2-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-CRT2-ACCT 4 A PIC X(04) Account Symbol 
RPT-CRT2-TRADE-[[ID]]     
     RPT-CRT2-TRD-PFX 4 N PIC 9(04) Trade Number Prefix 
     RPT-CRT2-TRD-SFX 6 N PIC 9(06) Trade Number Suffix 
RPT-CRT2-XREF 15 A/N PIC X(15) Internal XREF / Trade # 
RPT-CRT2-TRADE-TYPE 4 A/N PIC X(04) Trade Type-TFTD 
RPT-CRT2-TRADE-SUB-TYPE 4 A/N PIC X(04) Trade Sub-Type - SPT 
RPT-CRT2-BS-IND 1 A PIC X(01) Buy/Sell Code, B=Buy, S = Sell 
RPT-CRT2-TRD-DATE 8 N PIC 9(08) Trade Date (YYYYMMDD) 
RPT-CRT2-STTL-DATE 8 N PIC 9(08) [[settlement]] Date (YYYYMMDD) 
RPT-CRT2-CTRA 4 A/N PIC X(04) Contra Account 
RPT-CRT2-POOL-NUMBER 6 A/N PIC X(06) Pool Number 
RPT-CRT2-POOL-[[CUSIP]] 9 A/N PIC X(09) Pool [[CUSIP]] 
RPT-CRT2-STTL-PRICE 15 N PIC 9(03)V9(12) [[settlement]] Price – In Decimal 
RPT-CRT2-ORIG-FACE 15 N PIC 9(15) Original Face 
RPT-CRT2-CURR-FACE 17 N PIC 9(15)V9(02) Current Face 
RPT-CRT2-NET-MONEY 15 N PIC 9(13)V9(02) Net Money 
RPT-CRT2-NET-MONEY-
CRDR 
1 A PIC X(01) Net Money Indicator (C=Credit, D=Debit) 
FILLER 81 A PIC X(81) Filler 
Total  228 

---

## Page 9

File Transmission Layout – Cash Trade Conversion Format 
File Transmission Layout – Cash Trade (Same Day Settle) Conversion 9 
Converted PID Detail 
Detail record containing a single converted pool instruct record. 
Field Name Length Type Cobol Picture Description/Notes 
RPT-CRT3-CARD-CODE 2 N PIC 9(02) Converted PID Detail Record, Card code = 
‘03’ 
RPT-CRT3-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-CRT3-ACCT 4 A PIC X(04) Account Symbol 
RPT-CRT3-PID-[[ID]] 16 A/N PIC X(16) Pool Instruct Identifier. Left padded with 2 
leading 0s.1 
RPT-CRT3-STIP -TRADE-[[ID]]     
     RPT-CRT3-STIP- 
     TRD-PFX 
4 N PIC 9(04) Targeted Trade Number Prefix 
     RPT-CRT3-STIP- 
     TRD-SFX 
6 N PIC 9(06) Targeted Trade Number Suffix 
RPT-CRT3-XREF 15 A/N PIC X(15) Targeted Trade Internal XREF / Trade # 
RPT-CRT3-TRADE-TYPE 4 A/N PIC X(04) Targeted Trade Type-TFTD, SBON 
RPT-CRT3-TRADE-SUB-TYPE 4 A/N PIC X(04) Targeted Trade Sub-Type – SPT, STIP, 
TBA 
RPT-CRT3-BS-IND 1 A PIC X(01) Buy/Sell Code, B=Buy, S = Sell 
RPT-CRT3-TRD-DATE 8 N PIC 9(08) Trade Date (YYYYMMDD) 
RPT-CRT3-STTL-DATE 8 N PIC 9(08) [[settlement]] Date (YYYYMMDD) 
RPT-CRT3-DLVRY-DATE 8 N PIC 9(08) Delivery Date (YYYYMMDD) 
RPT-CRT3-CTRA 4 A/N PIC X(04) Contra Account 
RPT-CRT3-POOL-NUMBER 6 A/N PIC X(06) Pool Number 
RPT-CRT3-POOL-[[CUSIP]] 9 A/N PIC X(09) Pool [[CUSIP]] 
RPT-CRT3-STTL-PRICE 15 N PIC 9(03)V9(12) [[settlement]] Price – In Decimal 
RPT-CRT3-ORIG-FACE 15 N PIC 9(15) Original Face 
RPT-CRT3-CURR-FACE 17 N PIC 9(15)V9(02) Current Face 
RPT-CRT3-NET-MONEY 15 N PIC 9(13)V9(02) Net Money 
RPT-CRT3-NET-MONEY-
CRDR 
1 A PIC X(01) Net Money Indicator (C=Credit, D=Debit) 
FILLER 57 A PIC X(57) Filler 
Total  228 
1 For example: If PID value is 0005948-041018, in the MRO 16-character field that’s left padded with 0s, it will be 000005948-041018. In current system, PID 
is 14-character long. 

---

## Page 10

File Transmission Layout – Cash Trade Conversion Format 
File Transmission Layout – Cash Trade (Same Day Settle) Conversion 10 
 
Resulting POID Detail 
Detail record containing a single resulting pool obligation record.   
Field Name Length Type Cobol Picture Description/Notes 
RPT-CRT4-CARD-CODE 2 N PIC 9(02) Resulting POID Detail Record, Card 
code = ‘04’ 
RPT-CRT4-TBA-[[CUSIP]] 9 A/N PIC X(09) TBA [[CUSIP]] 
RPT-CRT4-ACCT 4 A PIC X(04) Account Symbol 
RPT-CRT4-POID 14 N PIC 9(14) Pool Obligation [[ID]] 
RPT-CRT4-PID-[[ID]] 16 A/N PIC X(16) Associated Pool Instruct Identifier (for 
POIDs resulting from PID only). When 
populated, it is left padded with 2 leading 
0s. 
RPT-CRT4-ASC-TRADE-[[ID]]     
     RPT-CRT4-ASC-TRD-PFX 4 N PIC 9(04) Associated Trade Number Prefix (for 
POIDs resulting from SPT trades or STIP 
PIDs only) 
     RPT-CRT4-ASC-TRD-SFX 6 N PIC 9(06) Associated Trade Number Suffix (for 
POIDs resulting from SPT trades or STIP 
PIDs only) 
RPT-CRT4-BS-IND 1 A PIC X(01) Buy/Sell Code, B=Buy, S = Sell 
RPT-CRT4-TRD-DATE 8 A/N PIC X(08) Trade Date (YYYYMMDD), if exists 
RPT-CRT4-STTL-DATE 8 N PIC 9(08) [[settlement]] Date (YYYYMMDD) 
RPT-CRT4-DLVRY-DATE 8 N PIC 9(08) Delivery Date (YYYYMMDD) 
RPT-CRT4-CTRA 4 A/N PIC X(04) Contra Account 
RPT-CRT4-POOL-NUMBER 6 A/N PIC X(06) Pool Number 
RPT-CRT4-POOL-[[CUSIP]] 9 A/N PIC X(09) Pool [[CUSIP]] 
RPT-CRT4-STTL-PRICE 15 N PIC 9(03)V9(12) [[settlement]] Price – In Decimal 
RPT-CRT4-ORIG-FACE 15 N PIC 9(15) Original Face 
RPT-CRT4-CURR-FACE 17 N PIC 9(15)V9(02) Current Face 
RPT-CRT4-NET-MONEY 15 N PIC 9(13)V9(02) Net Money 
RPT-CRT4-NET-MONEY-
CRDR 
1 A PIC X(01) Net Money Indicator (C=Credit, 
D=Debit) 
FILLER 66 A PIC X(66) Filler 
Total   228 

---

## Page 11

File Transmission Layout – Cash Trade Conversion Format 
File Transmission Layout – Cash Trade (Same Day Settle) Conversion 11 
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Cobol Picture Description/Notes 
RPT-CRT99-CARD-CODE 2 N PIC 9(02) Trailer Record, Card 
Code = '99' 
FILLER 13 A PIC X(13) Filler 
RPT-CRT99-ACCT 4 A/N PIC X(04) Account Symbol 
FILLER 1 A PIC X(01) Filler 
RPT-CRT99-LOGICAL-COUNT 7 N PIC 9(07) Logical Record Count 
FILLER 1 A PIC X(01) Filler 
RPT-CRT99-PHYSICAL-COUNT 7 N PIC 9(07) Physical Record Count 
FILLER 193 A PIC X(193) Filler 
Total   228 
 
 

---

## Page 12

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 