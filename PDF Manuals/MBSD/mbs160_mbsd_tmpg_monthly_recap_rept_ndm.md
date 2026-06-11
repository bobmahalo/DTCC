---
title: "MBSD TMPG Monthly Recap Report"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs160_mbsd_tmpg_monthly_recap_rept_ndm.pdf"
pages: 10
size: "296.6 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD TMPG Monthly Recap Report

**Original File:** [mbs160_mbsd_tmpg_monthly_recap_rept_ndm.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs160_mbsd_tmpg_monthly_recap_rept_ndm.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 296.6 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
MBSD TMPG MONTHLY RECAP REPORT 
VERSION 1.01 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in wh ich such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: December 2011 
Publication Code:  MBS160 
Service: Fixed Income Clearing Corporation 
Title: MBSD TMPG Monthly Recap Report  

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ....................................................................................................................... 4 
MBSD TMPG Monthy Recap Report................................................................................................... 5 
Overview ....................................................................................................................................... 5 
File Transmission Layouts Overview.................................................................................................  6 
MBSD TMPG Monthly Recap Report .................................................................................................  6 
Purpose ..................................................................................................................................... 6 
Frequency .................................................................................................................................. 6 
Account/Report Header Records (Card Code 01).............................................................................. 6 
TMPG Recap Detail Record (Card Code 02) .................................................................................... 6 
Trailer Control Record (Card Code 99) ............................................................................................ 6 
Format Codes ............................................................................................................................... 6 
File Transmission Layout For Monthly Recap Report ......................................................................... 7 
Header.......................................................................................................................................... 7 
Detail Record .................................................................................................................................  8 
Trailer ........................................................................................................................................... 9 
 

---

## Page 4

MBSD TMPG Monthly Recap Report 
Version C ontrol Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change  
December 
2011 
Original MBS Initial Version  
n/a n/a [[DTCC]] 
Learning  
Updated formatting only. Content is unchanged.  
10/12/2022 1.01 MBS Removed mockup print image of report. Report is live in production.  
 
  

---

## Page 5

MBSD TMPG Monthly Recap Report 
MBSD TMPG Monthy Rec ap R eport 5 
MBSD TMPG MONTHY RECAP REPORT  
Overview 
Note: 
This  report  is similar  to the existing  Dealer or [[Broker]]  Commission  Report 
The MBSD TMPG Monthly Recap Report is produced on the last business day of each month to reflect all Pool 
[[obligations]] (“POIDs”) subject to TMPG charges during the current month. 
This report is not cumulative. (Note: As this report is not cumulative, Pool [[obligations]] settled from previous 
months are not included on this report.) Members will use this report to balance MBSD generated TMPG 
charges versus their own internal books and records. 
The MBSD TMPG Monthly Recap Report will include the following activities: 
• All POIDs settled within the current month 
• Number of days for which a TMPG charge is applied (by rate if applicable) 
• Total TMPG charge per POID 
  

---

## Page 6

MBSD TMPG Monthly Recap Report 
File Transmission Layouts Ov erview 6 
FILE TRANSMISSION LAYOUTS OVERVIEW 
MBSD TMPG Monthly Recap Report 
Purpose 
The TMPG Monthly recap report reflects all monthly TMPG charges and rate changes on [[participant]] account 
Frequency  
Monthly (on the last business date of the month). 
• All records are of equal length - 228 bytes. 
• There are 3 different record types, each uniquely identified by card code, as follows: card codes 01 
through 02, & 99. 
 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
TMPG Recap Detail Record (Card Code 02) 
Detail record containing a single failing pool obligation record. 
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
If a number is padded, it will be padded with zeroes on the left in the integer part and on the right in the decimal part (if  one 
exists). If text is padded, it will be padded with spaces on the right.  

---

## Page 7

MBSD TMPG Monthly Recap Report 
File Transmission Layout For Monthly R ecap Report 7 
FILE TRANSMISSION LAYOUT FOR MONTHLY RECAP 
REPORT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Format Cobol Picture Description/Comments  
RPT-TRR-DT1-CARD-
CODE 
2 N ## PIC 9(02) Card code = ‘01’ 
RPT-TRR-DT1-RPT-[[ID]] 8 A/N XXXXXXXX PIC X(08) Report [[ID]] = “MB7100_N” 
RPT-TRR-DT1-ACC-
AGG-[[ID]] 
     
RPT-TRR-DT1-PART-[[ID]] 3 N ### PIC 9(03) [[participant]] [[ID]]  
RPT-TRR-DT1-AGG 2 N ## PIC 9(02) Aggregate Number 
RPT-TRR-DT1-ACCT 4 A AAAA PIC X(04) Account Symbol  
RPT-TRR-DT1-BUS-
DATE 
8 N YYYYMMDD PIC 9(08) Date of Report  
FILLER 201 A AAAA….. PIC X(201) Filler  
Total        228 
 
  

---

## Page 8

MBSD TMPG Monthly Recap Report 
File Transmission Layout For Monthly R ecap Report 8 
Detail Record 
Detail record containing a single failing pool obligation record. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-TRR- DT2 -CARD -
CODE 
2 N ## PIC 9(02) card  Code  = "02" 
RPT-TRR- DT2 -SETTLE -
MONT H 
6 N YYYYMM PIC 9(06) [[settlement]] Month 
RPT-TRR- DT2 -TBA -
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) TBA [[CUSIP]] 
RPT-TRR- DT2 -POOL -
NUMB E R 
6 A/N XXXXXX PIC X(06) Pool  Number 
RPT-TRR- DT2 -POOL -
[[CUSIP]] 
9 A/N XXXXXXXXX PIC X(09) Pool  [[CUSIP]] 
RPT-TRR- DT2 -SIFMA -
CLASS 
1 A A, B, C or D PIC X(01) SIFMA class code  
RPT-TRR- DT2 -POID  14 N ############## PIC 9(14) Pool  Obligation  [[ID]] 
RPT-TRR- DT2 -BUY -
SELLCOD E  
1 A B or S PIC X(01) Buy or sell code  
RPT-TRR- DT2 -SETTL -
DATE 
8 N YYYYMMDD PIC 9(08) [[settlement]] date 
RPT-TRR- DT2 -
CRLA N C E-DAT E 
8 N YYYYMMDD PIC 9(08) CLEARANCE DATE 
RPT-TRR- DT2 -ORIG -
FACE 
15 N ############### PIC 9(15) Original Face 
RPT-TRR- DT2 -CURR-
FACE 
17 N ################# PIC 9(15)V9(02) Current Face 
RPT-TRR- DT2 -PRICE  15 N ############### PIC 9(03)V9(12) Obligation  price 
RPT-TRR- DT2 -EXPECT -
NETMO N E Y 
15 N ############### PIC 9(13)V9(02) Net Money  
RPT-TRR- DT2 -
TMPGRAT E  
6 N ###### PIC 9(2)V9(4) Applied  TMPG Rate 
RPT-TRR- DT2 -DAYS  3 N ### PIC 9(3) Number of days  failing  
RPT-TRR- DT2 -
EFFV_F ROM_D AT E  
8 N YYYYMMDD PIC 9(08) The first date the rate became 
effective 
RPT-TRR -DT2 -
EFFV_T O_ D A T E 
8 N YYYYMMDD PIC 9(08) The last date the rate was 
effective  on 
RPT-TRR -DT2 -ACCR UA L  15 N ###############  PIC S9(13)V9(2)  TMPG fail charge accrual 

---

## Page 9

MBSD TMPG Monthly Recap Report 
File Transmission Layout For Monthly R ecap Report 9 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-PO A- D T2 -TMPG -
CRE D I T-DEBIT 
1 A C or D PIC X(01) TMPG charge Debit or Credit 
FILLER 61 A AAAA… PIC X(61) Filler 
Total   228 
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-TRR-DT99-CARD-CODE 2 N ## PIC 9(02) Card code =‘99’ 
FILLER 13 A AAAAAAAAAAAAA PIC X(13) Filler  
RPT-TRR-DT99-ACCT 4 A AAAA PIC X(04) Account Symbol  
FILLER 1 A A PIC X(01) Filler  
RPT-TRR-DT99- LOGICAL-
COUNT 
7 N ####### PIC 9(07) Logical Record 
Count (zero 
padded)  
FILLER 1 A A PIC X(01) Filler  
RPT-TRR-DT99- 
PHYSICAL-COUNT 
7 N ####### PIC 9(07) Physical Record  
Count  
(zeropadded)  
FILLER 193 A AAAA… PIC 9(193) Filler  
Total   228 
 
 
 
 

---

## Page 10

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 