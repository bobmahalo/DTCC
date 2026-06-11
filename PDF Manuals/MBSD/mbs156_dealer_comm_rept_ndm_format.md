---
title: "CCP Pool Obligation Pending Settlement Report NDM Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs156_dealer_comm_rept_ndm_format.pdf"
pages: 10
size: "257.5 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# CCP Pool Obligation Pending Settlement Report NDM Format

**Original File:** [mbs156_dealer_comm_rept_ndm_format.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs156_dealer_comm_rept_ndm_format.pdf)  
**Category:** MBSD  
**Total Pages:** 10  
**File Size:** 257.5 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
FILE TRANSMISSION LAYOUT FOR DEALER COMMISSION REPORT NDM 
FORMAT  
VERSION 1.00 
APRIL 3, 2001 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: April 3, 2001 
Publication Code: MBS156 
Service: Fixed Income Clearing Corporation 
Title: File Transmission Layouts for Dealer Commission Report NDM Format 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................... 4 
File Transmission Layout Overview ................................................................................................................... 5 
Dealer Commission Report NDM Format ........................................................................................................... 5 
Purpose ............................................................................................................................................................. 5 
Frequency.......................................................................................................................................................... 5 
Record Layouts ................................................................................................................................................. 5 
Account/Report Header Records (Card Code 01) ........................................................................................... 5 
Dealer Commission Detail Record (Card Code 02) ........................................................................................ 5 
Trailer Control Record (Card Code 99) ........................................................................................................... 5 
Format Codes .................................................................................................................................................... 5 
File Transmission Layout – Dealer Commission– NDM Format ..................................................................... 7 
Header ................................................................................................................................................................ 7 
Detail Record ...................................................................................................................................................... 8 
Trailer .................................................................................................................................................................. 9 
 

---

## Page 4

File Transmission Layout For Dealer Commission Report NDM Format 
Version Control Page 4 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
4/1/2013 Original MBS Initial Version 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
 
  

---

## Page 5

File Transmission Layout For Dealer Commission Report NDM Format 
File Transmission Layout Overview 5 
FILE TRANSMISSION LAYOUT OVERVIEW  
Dealer Commission Report NDM Format 
Purpose 
The Dealer Commission Report reflects all commissions and related trade data that MBSCC will, on behalf of 
the Brokers, collect from the Dealers. 
Frequency 
Monthly - Month-end. 
Record Layouts 
*All records are of equal length - 122 bytes. 
*There are 3 different logical record types, each uniquely identified by card code, as follows: card codes 01 
through 02, & 99. 
Account/Report Header Records (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Dealer Commission Detail Record (Card Code 02) 
Detail record containing commission information on a single trade formatted for the dealer accounts only. 
Trailer Control Record (Card Code 99) 
Trailer record indicates the end of the report for the recipient account. 
Format Codes 
# - digit 
X - alphanumeric  
A - letter 
Y - year 
M - month 
D – day 

---

## Page 6

File Transmission Layout For Dealer Commission Report NDM Format 
File Transmission Layout Overview 6 
Note:   
If a number is padded, it will be padded with zeroes on the left in the integer part and on the right in the decimal part (if one 
exists). If text is padded, it will be padded with spaces on the right. 

---

## Page 7

File Transmission Layout For Dealer Commission Report NDM Format 
File Transmission Layout – Dealer Commission– NDM Format 7 
FILE TRANSMISSION LAYOUT – DEALER COMMISSION– 
NDM FORMAT 
Header 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Cobol Picture Description/Comments 
RPT-CM-DT01-CARD-CODE 2 A/N PIC X(02). Header Record Card Code = '01' 
RPT-CM-DT01-REPORT-[[ID]] 8 A/N PIC X(08). Report [[ID]] - 'MB7441-A' 
RPT-CM-DT01-
[[participant]]-[[ID]] 
3 N PIC 9(03). [[participant]] [[ID]] 
RPT-CM-DT01-
AGGREGATE-NUMBER 
2 A/N PIC 9(02). Aggregate 
RPT-CM-DT01-ACCOUNT-[[ID]] 4 A/N PIC X(04). Account Symbol 
RPT-CM-DT01-
[[participant]]-NAME 
40 A/N PIC X(40). [[participant]] Name 
RPT-CM-DT01-RUN-DATE 8 A/N PIC X(08). Date of Report (YYYYMMDD) 
RPT-CM-DT01-PASS 1 A/N PIC X(01). Pass Indicator (A = Morning, P = Evening} 
FILLER 54 A/N PIC X(54).  
Total   122 
 
  

---

## Page 8

File Transmission Layout For Dealer Commission Report NDM Format 
File Transmission Layout – Dealer Commission– NDM Format 8 
Detail Record 
Detail record containing commission information on a single trade formatted for the dealer accounts only. 
Field Name Length Type Cobol Picture Description/Notes 
RPT-CM-DT02-CARD-CODE 2 A/N PIC X(02). Detail Record, Card Code = '02' 
RPT-CM-DT02-ACCT-[[ID]] 4 A/N PIC X(04). Account Symbol 
RPT-CM-DT02-GIVES-UP-
ACCT-[[ID]] 
4 A/N PIC X(04). [[Broker]] Account Symbol 
RPT-CM-DT02-CONTRA-
ACCT-[[ID]] 
4 A/N PIC X(04). Contra Account Symbol 
RPT-CM-DT02-[[Buyer]]-
[[Seller]]-IND 
1 A/N PIC X(01). B = Buy , S = Sell 
RPT-CM-DT02-
[[settlement]]-YEAR 
4 N PIC 9(04). [[settlement]] Year (YYYY) 
RPT-CM-DT02-
[[settlement]]-MONTH 
2 N PIC 9(02). [[settlement]] Month (MM) 
RPT-CM-DT02-[[CUSIP]]. 9 A/N PIC X(09). [[CUSIP]] 
FILLER 1 A PIC X(01). Filler 
RPT-CM-DT02-TRADE-DATE 8 A/N PIC X(08). Trade Date (YYYYMMDD) 
RPT-CM-DT02-TRADE-[[ID]].     
     RPT-CM-DT02-TRADE-  
PREFIX-NBR 
4 N PIC 9(04). Trade Number Prefix 
     RPT-CM-DT02-TRADE-
SUFFIX-NBR 
6 N PIC 9(06). Trade Number Suffix 
RPT-CM-DT02-INTERNL-
TRADE-NBR 
15 A/N PIC X(15). Internal XREF/Trade # 
RPT-CM-DT02-PAR-VALUE 13 N PIC 9(11)V9(02). Par Value 
RPT-CM-DT02-DEALER-
PRICE 
15 N PIC 9(03)V9(12). Dealer Price - In Decimal 
RPT-CM-DT02-STTL-PRICE 15 N PIC 9(03)V9(12). [[settlement]] Price - In Decimal 
RPT-CM-DT02-CMSN-FLAT-
FEE 
11 N PIC 9(09)V9(02). Commission Charged 
FILLER 4 A/N PIC X(04). Filler 
Total   122 
  

---

## Page 9

File Transmission Layout For Dealer Commission Report NDM Format 
File Transmission Layout – Dealer Commission– NDM Format 9 
Trailer 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Format Cobol Picture Description/Notes 
RPT-CM-DT99-CARD-CODE 2 A/N PIC X(02). Report Trailer, 
Card Code = '99' 
 
FILLER 13 A PIC X(13). Filler  
RPT-CM-DT99-ACCOUNT 4 A/N PIC X(04). Account Symbol  
FILLER 1 A PIC X(01). Filler  
RPT-CM-DT99-LOGICAL-
COUNT 
7 N PIC 9(07). Logical Record 
Count 
 
FILLER 1 A PIC X(01). Filler  
RPT-CM-DT99-PHYSICAL-
COUNT 
7 N PIC 9(07). Physical Record 
Count 
 
FILLER 87 A PIC X(87). Filler  
Total   122 
 
 
 
 
 

---

## Page 10

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 