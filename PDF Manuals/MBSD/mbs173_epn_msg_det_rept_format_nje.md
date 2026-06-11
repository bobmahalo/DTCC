---
title: "EPN Message Detail Report Format – NJE File Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs173_epn_msg_det_rept_format_nje.pdf"
pages: 18
size: "401.0 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# EPN Message Detail Report Format – NJE File Layouts

**Original File:** [mbs173_epn_msg_det_rept_format_nje.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs173_epn_msg_det_rept_format_nje.pdf)  
**Category:** MBSD  
**Total Pages:** 18  
**File Size:** 401.0 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
EPN MESSAGE DETAIL REPORT FORMAT – NJE FILE LAYOUTS 
VERSION 2.0 
MARCH 13, 2023 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in wh ich such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: March 13, 2023 
Publication Code:  MBS173 
Service: Fixed Income Clearing Corporation 
Title: EPN Message Detail Report Format –  NJE File Layouts

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control page ....................................................................................................................... 4  
File Transmission Layout Overview .................................................................................................. 5  
EPN Mess ag e D etail Fo rmat ............................................................................................................ 5  
Purpose ....................................................................................................................................... 5  
Frequency .................................................................................................................................... 5  
Recor d La you ts............................................................................................................................. 5  
EPN Message Detail Report Format – NJE FIle Layouts ...................................................................... 7  
EPN Mess ag e D etail – Header Record (01) ........................................................................................ 7  
EPN Mess ag e D etail – Security Totals Record (02).............................................................................. 8  
EPN Mess ag e D etail – Mess ag e Head er Reco rd  (03) .......................................................................... 8  
EPN Mess ag e D etail – Message Pool Information Record (04) .............................................................. 9  
EPN Mess ag e D etail – Mess ag e Typ e To tals Reco rd  (05) .................................................................. 11 
EPN Mess ag e D etail – Inbound/Outbound [[CUSIP]] Total Records (06)................................................... 12 
EPN Mess ag e D etail – Inbound/Outbound Totals Record (07) ............................................................. 14 
EPN Mess ag e D etail – Inbound/Outbound Totals Record (08) ............................................................. 16 
EPN Mess ag e D etail – Report Trailer Record (99) ............................................................................. 17 
 

---

## Page 4

EPN Message Detail Report Format – NJE File Layouts  
 
 
Version C ontrol page 4 
 
 
VERSION CONTROL PAGE 
 
Date Version # Name Description of Change  
7/19/2006 Original MBSD Initial Version  
3/13/2023 2.0 J.Sheeran  Updated formatting only. Content is unchanged.  
 
 
  

---

## Page 5

EPN Message Detail Report Format – NJE File Layouts  
 
 
File Transmission Layout Ov erview 5 
 
 
FILE TRANSMISSION LAYOUT OVERVIEW 
EPN Message Detail Format 
Purpose 
The EPN Message Detail report list details regarding messages sent and received for all [[participant]] accounts. 
Includes all messages entered since the beginning of the business day. The AutoRoute product [[ID]] for COB 
Message Detail Report is 13150381 and the [[EOD]] Message Detail Report is 13150384. 
Frequency 
Daily (Close of Business & End of Day). 
Record Layouts 
All NJE formatted records are of equal length - 287 bytes 
There are 9 different record types, each uniquely identified by card code as follows: card codes 0l through 08, 
& 99. 
Account/Report Header Record (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Security Subheading Record (Card Code 02) 
Control record which signifies the beginning of the next security class. 
Message Header Record (Card Code 03)* 
Control record which signifies the beginning of a message. Contains recipient account and message 
identification items. 
Pool Information Record (Card Code 04)* 
Detail record containing pool information for the recipient account. 
  

---

## Page 6

EPN Message Detail Report Format – NJE File Layouts  
 
 
File Transmission Layout Ov erview 6 
 
 
Message Type Totals Record (Card Code 05)** 
Contains totals for message types ON (original notification), DK (DKs), CX (cancels) & CC (Cancel and 
Correct) within this bound (inbound or outbound) & this class for the recipient account. 
Inbound/Outbound Totals Record (Card Code 06)** 
Contains Inbound (messages received from contra) & Outbound (messages sent to Contra) totals for message 
types ON (original notification), DK (DKs), CX (cancels) & CC (Cancel and Correct) for the recipient account. 
Security Totals Record (Card Code O7)** 
Contains totals for message types ON (original notification), DK (DKs) and CX (cancels) within this class for the 
recipient account. 
Security Totals Record (Card Code O8)** 
Contains totals for message type CC (Cancel and correct) within this class for the recipient account. 
Trailer Control Record (Card Code 99) 
Trailer record indicates the end of the report for the recipient account 
 
 
 
 
 
 
 
 
 
 
* All data fields on the Message Header Record (03) and Pool Information Record (04) are character format. 
** MBSD accumulates totals for Original Face, Current Face, Principal, Interest, and Net Money. If any of these 
fields is non-numeric an incomplete total indicator is set to ‘*’ for the respective field.  

---

## Page 7

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 7 
 
 
EPN MESSAGE DETAIL REPORT FORMAT – NJE FILE 
LAYOUTS 
EPN Message Detail – Header Record (01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT1-CARD-CODE 2 N PIC 9(02). Header Record,  Card Code  = '01' 
RPT-MDR-DT1-RPT-[[ID]] 8 A/N PIC X(08). Report  [[ID]] = 'MB3331-A' 
RPT-MDR-DT1-[[participant]]-[[ID]] 3 N PIC 9(03). [[participant]]  [[ID]] 
RPT-MDR-DT1-AGG-NBR 2 N PIC 9(02). Aggregate  Number 
RPT-MDR-DT1-ACCOUNT 4 A/N PIC X(4). Account  Symbol 
RPT-MDR-DT1-PART-NAME 40 A/N PIC X(40). [[participant]]  Name 
RPT-MDR-DT1-BUS-DATE 6 N PIC 9(06). Date of Activity  (MMDDYY) 
RPT-MDR-DT1-PASS 2 A/N PIC X(02). Pass Indicator  (CB = Close  of Business,  ED = 
End of Day) 
RPT-MDR-DT1-BUS-DATE2 6 N PIC 9(6). Date of Report  (MMDDYY) 
RPT-MDR-DT1-TIME-STAMP 6 N PIC 9(06). Report  Time Stamp HHMMSS (will be zero 
filled)  
FILLER 208 A/N PIC X(208).  
 287    
 
  

---

## Page 8

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 8 
 
 
EPN Message Detail – Security Totals Record (02) 
Control record which signifies the beginning of the next security class. 
Field Name Length Type Cobol 
Pic 
Description/comment  
RPT-MDR-DT2-CARD-CODE 2 N PIC 9(02). Security Totals  Record,  Card Code  = '02' 
RPT-MDR-DT2-ACCOUNT 4 A/N PICX(4). Submitter Account  Symbol 
RPT-MDR-DT2-STTL-YY 2 A/N PIC X(2). [[settlement]] Year (YY) 
RPT-MDR-DT2-STTL-MM 2 A/N PIC X(2). [[settlement]] Month (MM) 
RPT-MDR-DT2-TBA-[[CUSIP]] 10 A/N PIC 
X(10). 
TBA [[CUSIP]] (9 alphanumerics  followed  by a 
blank)  
FILLER 18 A/N PIC 
X(18). 
 
RPT-MDR-DT2-TBA-[[SEC]]-DESC 40 A/N PIC 
X(40). 
TBA [[CUSIP]] Description  
FILLER 209 A/N PIC 
X(209). 
 
 287    
EPN Message Detail – Message Header Record (03) 
Control record which signifies the beginning of a message. Contains recipient account and message 
identification items. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT3-CARD-CODE 2 N PIC 9(02). Message Header, Card Code  = '03' 
RPT-MDR-DT3-ACCOUNT 4 A/N PIC X(04). Submitter Accoun  Symbol 
RPT-MDR-DT3-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MDR-DT3-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MDR-DT3-TBA-[[CUSIP]] 10 A/N PIC X(10). TBA [[CUSIP]] (9 alphanumerics  followed  by a 
blank)  
RPT-MDR-DT3-BOUND 1 A/N PIC X(1). I = Inbound,  O= Outbound  
RPT-MDR-DT3-MSG-TYPE 2 A/N PIC X(2). Message Type, ON, CX, DK, CC 
RPT-MDR-DT3-CONTRA 4 A/N PIC X(4). Contra  Account  
RPT-MDR-DT3-MSG-[[ID]] 11 A/N PIC X(11). Message [[ID]] 
RPT-MDR-DT3-ORG-PAR 11 A/N PIC X(11). Original Trade Par 

---

## Page 9

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 9 
 
 
Field Name Length Type Cobol Pic Description/comment  
FILLER 10 A/N PIC X(10).  
RPT-MDR-DT3-PRICE 12 A/N PIC X(12). Contract  Price 
RPT-MDR-DT3-GDMM 4 A/N PIC X(4). Good Delivery  Millions 
RPT-MDR-DT3-TRD-DATE 6 A/N PIC X(6). Trade Date (MMDDYY) 
RPT-MDR-DT3-STL-DATE 6 A/N PIC X(6). [[settlement]] Date (MMDDYY) 
RPT-MDR-DT3-DEL-DATE 6 A/N PIC X(6). Delivery  Date (MMDDYY) 
RPT-MDR-DT3-INTRNL-[[ID]] 16 A/N PIC X(16). Internal  [[ID]] 
RPT-MDR-DT3-BRKR-CD 4 A/N PIC X(4). Sub-Account  
RPT-MDR-DT3-REASON-CD 4 A/N PIC X(4). Reason  Code  
RPT-MDR-DT3-TRG-MSG-[[ID]] 11 A/N PIC X(11). Target Message [[ID]] 
RPT-MDR-DT3-XREF 15 A/N PIC X(15). XREF 
FILLER 5 A/N PIC X(5).  
RPT-MDR-DT3-SPI 30 A/N PIC X(30). Special  Instructions  
RPT-MDR-DT3-TIME-STAMP1 6 A/N PIC X(6). Time Stamp #1 
RPT-MDR-DT3-TIME-STAMP2 6 A/N PIC X(6). Time Stamp #2 
RPT-MDR-DT3-TIME-STAMP3 6 A/N PIC X(6). Time Stamp #3 
RPT-MDR-DT3-TIME-STAMP4 6 A/N PIC X(6). Time Stamp #4 
RPT-MDR-DT3-TIME-STAMP5 6 A/N PIC X(6). Time Stamp #5 
RPT-MDR-NBR-POOLS 4 A/N PIC X(4). Number of pools  
RPT-MDR-DT3-POS-DUPE 1 A/N PIC X(1). Possible  Duplicate Message (X or blank)  
RPT-MDR-DT3-STATUS 4 A/N PIC X(4). Status of Message 
RPT-MDR-DT3-DATE-READ 6 A/N PIC X(6). Date Message Read 
RPT-MDR-DT3-TIME-READ 6 A/N PIC X(6). Time Message Read 
FILLER 58 A/N PIC X(58).  
 287    
EPN Message Detail – Message Pool Information Record (04) 
Detail record containing pool information for the recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT4-CARD-CODE 2 N PIC 9(02). Pool  Information,  Card Code  = '04' 

---

## Page 10

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 10 
 
 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT4-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
RPT-MDR-DT4-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MDR-DT4-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MDR-DT4-TBA-[[CUSIP]] 10 A/N PIC X(10). TBA [[CUSIP]] (9 alphanumerics  followed  by blank)  
RPT-MDR-DT4-BOUND 1 A/N PIC X(01) I = Inbound,  O= Outbound  
RPT-MDR-DT4-MSG-TYPE 2 A/N PIC X(02) Message Type, ON, CX, DK or CC 
RPT-MDR-DT4-CONTRA 4 A/N PIC X(04) Contra  Account  
RPT-MDR-DT4-MSG-[[ID]] 11 A/N PIC X(11) Message [[ID]] 
RPT-MDR-DT4-LOT 6 A/N PIC X(06) Lot-[[ID]] 
FILLER 2 A/N PIC X(02).  
RPT-MDR-DT4-POOL 7 A/N PIC X(07). Pool  Number 
RPT-MDR-DT4-ORG-FACE 9 A/N PIC X(09). Original Face Value 
RPT-MDR-DT4-ORG-FACE-SGN 1 A/N PIC X(01). Original Face Value Sign  Indicator  ('-' or blank)  
RPT-MDR-DT4-COUPON 6 A/N PIC X(06). Coupon Rate 
RPT-MDR-DT4-MAT-DATE 6 A/N PIC X(06). Maturity Date(MMDDYY) 
RPT-MDR-DT4-NEW-ISSUE 1 A/N PIC X(01). New Issue (X or blank)  
RPT-MDR-DT4-TRD-NBR 10 A/N PIC X(10). Trade Number 
RPT-MDR-DT4-CTL-NBR 15 A/N PIC X(15). Control  Number 
FILLER 15 A/N PIC X(15).  
RPT-MDR-DT4-CUR-FACE 11 A/N PIC X(11). Current Face Value 
RPT-MDR-DT4-CURR-FACE-
SGN 
1 A/N PIC X(01). Current Face Value Sign  Indicator ('-' or blank)  
RPT-MDR-DT4-FACTOR 10 A/N PIC X(10). Factor  
RPT-MDR-DT4-[[CUSIP]] 9 A/N PIC X(09). [[CUSIP]] Number 
FILLER 5 A/N PIC X(05).  
RPT-MDR-DT4-ISS-DATE 6 A/N PIC X(06) Issue Date (MMDDYY) 
RPT-MDR-DT4-TERMINATOR 4 A/N PIC X(04) Terminator  
RPT-MDR-DT4-PRINCIPAL 11 A/N PIC X(11). Principal 
RPT-MDR-DT4-INTEREST 11 A/N PIC X(11). Interest 
RPT-MDR-DT4-NET-MONEY 11 A/N PIC X(11). Net Money  

---

## Page 11

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 11 
 
 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT4-NET-MONEY-
SGN 
1 A/N PIC X(01). Net Money  Sign  Indicator  ('-' or blank)  
RPT-MDR-DT4-SPI 30 A/N PIC X(30) Special  Instructions  
FILLER 61 A/N PIC X(61).  
 287    
EPN Message Detail – Message Type Totals Record (05) 
Contains totals for message types ON (original notification), DK (DKs), CX (cancels) & CC (Cancel and 
Correct) within this bound (inbound or outbound) & this class for the recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT5-CARD-CODE 2 N PIC 9(02). Message Type  Totals,  Card Code  = '05' 
RPT-MDR-DT5-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
RPT-MDR-DT5-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MDR-DT5-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MDR-DT5-TBA-[[CUSIP]] 10 A/N PICX(10). TBA [[CUSIP]] (9 alphanumerics  followed  by a 
blank)  
RPT-MDR-DT5-BOUND 1 A/N PIC X(01). I = Inbound,  O= Outbound  
RPT-MDR-DT5--MSG-TYPE 2 A/N PIC X(02). Message Type, ON, CX, DK, CC 
FILLER 15 A/N PIC X(15).  
RPT-MDR-DT5-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT5-ORG-FACE 13 N PIC 9(13). Original Face Value 
RPT-MDR-DT5-ORG-FACE-SGN 1 A/N PIC X(01). Original Face Value Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT5-CUR-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT5-CUR-FACE 15 N PIC 
9(13)V9(02) 
Current Face Value 
RPT-MDR-DT5-CUR-FACE-SGN 1 A/N PIC X(01). Current Face Value Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT5-PRN-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT5-PRINCIPAL 15 N PIC 
9(13)V9(02) 
Principal 
RPT-MDR-DT5-INT-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  

---

## Page 12

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 12 
 
 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT5-INTEREST 15 N PIC 
9(13)V9(02) 
Interest 
RPT-MDR-DT5-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT5-NET-MONEY 15 N PIC 
9(13)V9(02) 
Net Money  
RPT-MDR-DT5-NET-MONEY-SGN 1 A/N PIC X(01). Net Money  Sign  Indicator  ('-' or blank)  
FILLER 168 A/N PIC X(168).  
 287    
EPN Message Detail – Inbound/Outbound [[CUSIP]] Total Records (06) 
Contains Inbound (messages received from contra) & Outbound (messages sent to Contra) totals for message 
types ON (original notification), DK (DKs), CX (cancels) & CC (Cancel and Correct) for the recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT6-CARD-CODE 2 N PIC 9(02). Inbound/Outbound  Totals,  Card Code = '06' 
RPT-MDR-DT6-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
RPT-MDR-DT6-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MDR-DT6-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MDR-DT6-TBA-[[CUSIP]] 10 A/N PICX(10). TBA [[CUSIP]] (9 alphanumerics  followed  by a 
blank)  
RPT-MDR-DT6-BOUND 1 A/N PIC X(01). I = Inbound,  O= Outbound  
FILLER 17 A/N PIC X(17).  
RPT-MDR-DT6-ON-NBR-MSG 7 N PIC 9(07). Total  Number of Messages  (ON) 
RPT-MDR-DT6-ON-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT6-ON-ORG-FACE 13 N PIC 9(13). Total  Original Face Value (ON) 
RPT-MDR-DT6-ON-ORG-FACE-SGN 1 A/N PIC X(01). Total  Original Face Value Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT6-ON-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT6-ON-NET-MONEY 15 N PIC 
9(13)V9(02) 
Total  Net Money  (ON) 
RPT-MDR-DT6-ON-NET-MONEY-
SGN 
1 A/N PIC X(01). Total  Net Money  (ON) Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT6-CC-NBR-MSG 7 N PIC 9(07). Total  Number of Messages  (CC) 

---

## Page 13

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 13 
 
 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT6-CC-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT6-CC-ORG-FACE 13 N PIC 9(13). Total  Original Face Value (CC) 
RPT-MDR-DT6-CC-ORG-FACE-SGN 1 A/N PIC X(01). Total  Original Face Value Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT6-CC-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT6-CC-NET-MONEY 15 N PIC 
9(13)V9(02) 
Total  Net Money  (CC) 
RPT-MDR-DT6-CC-NET-MONEY-SGN 1 A/N PIC X(01). Total  Net Money  (CC) Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT6-DK-NBR-MSG 7 N PIC X(07). Total  Number of Messages  (DK) 
RPT-MDR-DT6-DK-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT6-DK-ORG-FACE 13 N PIC 9(13). Total  Original Face Value (DK) 
RPT-MDR-DT6-DK-ORG-FACE-SGN 1 A/N PIC X(01). Total  Original Face Value Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT6-DK-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT6-DK-NET-MONEY 15 N PIC 
9(13)V9(02) 
Total  Net Money  (DK) 
RPT-MDR-DT6-DK-NET-MONEY-SGN 1 A/N PIC X(01). Total  Net Money  (DK) Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT6-CX-NBR-MSG 7 N PIC 9(07). Total  Number of Messages  (CX) 
RPT-MDR-DT6-CX-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT6-CX-ORG-FACE 13 N PIC 9(13). Total  Original Face Value (CX) 
RPT-MDR-DT6-CX-ORG-FACE-SGN 1 A/N PIC X(01). Total  Original Face Value Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT6-CX-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT6-CX-NET-MONEY 15 N PIC 
9(13)V9(02) 
Total  Net Money  (CX) 
RPT-MDR-DT6-CX-NET-MONEY-SGN 1 A/N PIC X(01). Total  Net Money  (CX) Sign  Indicator  ('-' or 
blank)  
FILLER 93 A/N PIC X(93).  
 287    
  

---

## Page 14

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 14 
 
 
EPN Message Detail – Inbound/Outbound Totals Record (07) 
Contains totals for message types ON (original notification), DK (DKs) and CX (cancels) within this class for the 
recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT7-CARD-CODE 2 N PIC 9(02). Security Totals,  Card Code  = '07' 
RPT-MDR-DT7-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
RPT-MDR-DT7-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MDR-DT7-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MDR-DT7-TBA-[[CUSIP]] 10 A/N PICX(10). TBA [[CUSIP]] (9 alphanumerics  followed  by blank)  
FILLER 18 A/N PIC X(18).  
RPT-MDR-DT7-ONR-NBR-MSG 7 N PIC 9(07). Total  Number of Messages  Received  (ON) 
RPT-MDR-DT7-ONR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-ONR-ORG-FACE 13 N PIC 9(13). Total  Original Face Value Received  (ON) 
RPT-MDR-DT7-ONR-ORG-
FACE-SGN 
1 A/N PIC X(01). Total  Original Face Value Received  (ON) Sign  
Indicator  ('-' or blank)  
RPT-MDR-DT7-ONR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-ONR-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Total  Net Money  Received  (ON) 
RPT-MDR-DT7-ONR-NET-
MONEY-SGN 
1 A/N PIC X(01). Total  Net Money  Received  (ON) Sign  Indicator  ('-' 
or blank)  
RPT-MDR-DT7-ONS-NBR-MSG 7 N PIC 9(07). Total  Number of Messages  Sent (ON) 
RPT-MDR-DT7-ONS-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-ONS-ORG-FACE 13 N PIC 9(13). Total  Original Face Value Sent (ON) 
RPT-MDR-DT7-ONS-ORG-
FACE-SGN 
1 A/N PIC X(01). Total  Original Face Value Sent (ON) Sign  Indicator  
('-' or blank)  
RPT-MDR-DT7-ONS-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-ONS-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Total  Net Money  Sent (ON) 
RPT-MDR-DT7-ONS-NET-
MONEY-SGN 
1 A/N PIC X(01). Total  Net Money  Sent (ON) Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT7-DKR-NBR-MSG 7 N PIC 9(07). Total  Number of Messages  Received  (DKs) 
RPT-MDR-DT7-DKR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-DKR-ORG-FACE 13 N PIC 9(13). Total  Original Face Value Received  (DKs) 

---

## Page 15

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 15 
 
 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT7-DKR-ORG-
FACE-SGN 
1 A/N PIC X(01). Total  Original Face Value Received  (DKS) Sign  
Indicator  ('-' or blank)  
RPT-MDR-DT7-DKR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-DKR-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Total  Net Money  Received  (DKs) 
RPT-MDR-DT7-DKR-NET-
MONEY-SGN 
1 A/N PIC X(01). Total  Net Money  Received  (DKs) Sign  Indicator  ('-' 
or blank)  
RPT-MDR-DT7-DKS-NBR-MSG 7 N PIC 9(07). Total  Number of Messages  Sent (DKs) 
RPT-MDR-DT7-DKS-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-DKS-ORG-FACE 13 N PIC 9(13). Total  Original Face Value Sent (DKs) 
RPT-MDR-DT7-DKS-ORG-
FACE-SGN 
1 A/N PIC X(01). Total  Original Face Value Sent (DKs) Sign  
Indicator  ('-' or blank)  
RPT-MDR-DT7-DKS-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-DKS-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Total  Net Money  Sent (DKs) 
RPT-MDR-DT7-DKS-NET-
MONEY-SGN 
1 A/N PIC X(01). Total  Net Money  Sent (DKs) Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT7-CXR-NBR-MSG 7 N PIC 9(07). Total  Number of Messages  Received  (CX) 
RPT-MDR-DT7-CXR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-CXR-ORG-FACE 13 N PIC X(13). Total  Original Face Value Received  (CX) 
RPT-MDR-DT7-CXR-ORG-
FACE-SGN 
1 A/N PIC X(01). Total  Original Face Value Received  (CX) Sign  
Indicator  ('-' or blank)  
RPT-MDR-DT7-CXR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-CXR-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Total  Net Money  Received  (CX) 
RPT-MDR-DT7-CXR-NET-
MONEY-SGN 
1 A/N PIC X(01). Total  Net Money  Received  (CX) Sign  Indicator  ('-' 
or blank)  
RPT-MDR-DT7-CXS-NBR-MSG 7 N PIC 9(07). Total  Number of Messages  Sent (CX) 
RPT-MDR-DT7-CXS-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-CXS-ORG-FACE 13 N PIC 9(13). Total  Original Face Value Sent (CX) 
RPT-MDR-DT7-CXS-ORG-
FACE-SGN 
1 A/N PIC X(01). Total  Original Face Value Sent (CX) Sign  Indicator  
('-' or blank)  
RPT-MDR-DT7-CXS-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-CXS-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Total  Net Money  Sent (CX) 

---

## Page 16

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 16 
 
 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT7-CXS-NET-
MONEY-SGN 
1 A/N PIC X(01). Total  Net Money  Sent (CX) Sign  Indicator  ('-' or 
blank)  
FILLER 15 A/N PIC X(15).  
 287    
EPN Message Detail – Inbound/Outbound Totals Record (08) 
Contains totals for message type CC (Cancel and correct) within this class for the recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT7-CARD-CODE 2 N PIC 9(02). Security Totals,  Card Code  = '08' 
RPT-MDR-DT7-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
RPT-MDR-DT7-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MDR-DT7-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MDR-DT7-TBA-[[CUSIP]] 10 A/N PICX(10). TBA [[CUSIP]] (9 alphanumerics  followed  by blank)  
FILLER 18 A/N PIC X(18).  
RPT-MDR-DT7-CCR-NBR-
MSG 
7 N PIC 9(07). Total  Number of Messages  Received  (CC) 
RPT-MDR-DT7-CCR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-CCR-ORG-
FACE 
13 N PIC 9(13). Total  Original Face Value Received  (CC) 
RPT-MDR-DT7-CCR-ORG-
FACE-SGN 
1 A/N PIC X(01). Total  Original Face Value Received  (CC) Sign  
Indicator  ('-' or 
blank)  
RPT-MDR-DT7-CCR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-CCR-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Total  Net Money  Received  (CC) 
RPT-MDR-DT7-CCR-NET-
MONEY-SGN 
1 A/N PIC X(01). Total  Net Money  Received  (CC) Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT7-[[CCS]]-NBR-
MSG 
7 N PIC 9(07). Total  Number of Messages  Sent (CC) 
RPT-MDR-DT7-[[CCS]]-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-[[CCS]]-ORG-
FACE 
13 N PIC 9(13). Total  Original Face Value Sent (CC) 
RPT-MDR-DT7-[[CCS]]-ORG-
FACE-SGN 
1 A/N PIC X(01). Total  Original Face Value Sent (CC) Sign  Indicator  
('-' or blank)  

---

## Page 17

EPN Message Detail Report Format – NJE File Layouts  
 
 
EPN Message D etail Report Format – NJE FIle Lay outs 17 
 
 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT7-[[CCS]]-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MDR-DT7-[[CCS]]-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Total  Net Money  Sent (CC) 
RPT-MDR-DT7-[[CCS]]-NET-
MONEY-SGN 
1 A/N PIC X(01). Total  Net Money  Sent (CC) Sign  Indicator  ('-' or 
blank)  
FILLER 171 A/N PIC X(171).  
 287    
EPN Message Detail – Report Trailer Record (99) 
Trailer record indicates the end of the report for the recipient account 
Field Name Length Type Cobol Pic Description/comment  
RPT-MDR-DT9-CARD-CODE 2 N PIC 9(02). Report  Trailer  Record,  Card Code  = '99' 
FILLER 13 A/N PIC X(13).  
RPT-MDR-DT9-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
FILLER 1 A/N PIC X(01).  
RPT-MDR-DT9-LOGICAL-
COUNT 
7 N PIC 9(7). Logical  Record  Count 
FILLER 1 A/N PIC X(1).  
RPT-MDR-DT9-PHYSICAK-
COUNT 
7 N PIC 9(07). Physical  Record  Count  
FILLER 252 A/N PIC X(252).  
 287    
 

---

## Page 18

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 