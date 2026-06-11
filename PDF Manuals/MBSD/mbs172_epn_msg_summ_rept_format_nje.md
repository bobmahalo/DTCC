---
title: "EPN Message Summary Report Format – NJE File Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs172_epn_msg_summ_rept_format_nje.pdf"
pages: 16
size: "371.4 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# EPN Message Summary Report Format – NJE File Layouts

**Original File:** [mbs172_epn_msg_summ_rept_format_nje.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs172_epn_msg_summ_rept_format_nje.pdf)  
**Category:** MBSD  
**Total Pages:** 16  
**File Size:** 371.4 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
EPN MESSAGE SUMMARY REPORT FORMAT – NJE FILE LAYOUTS 
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
Publication Code:  MBS172 
Service: Fixed Income Clearing Corporation 
Title: EPN Message Summary Report Format – NJE File Layouts

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control ............................................................................................................................... 4 
File Transmission Layout Overview .................................................................................................. 5 
EPN Mess ag e Summary Repo rt Fo rmat............................................................................................. 5 
Purpose ....................................................................................................................................... 5 
Frequency .................................................................................................................................... 5 
Recor d La you ts............................................................................................................................. 5 
EPN Message Summary Report Format – NJE File Layouts ................................................................ 7 
EPN Mess ag e Summary – Header Record (01)................................................................................... 7 
EPN Mess ag e Summary – [[SEC]] urity Sub head ing  Reco rd (02) ................................................................ 7 
EPN Mess ag e Summary – Contra Totals Record (03) .......................................................................... 8 
EPN Mess ag e Summary – Contra Totals Record (04) ........................................................................ 10 
EPN Mess ag e Summary – [[CUSIP]] Totals Record (05) ........................................................................ 11 
EPN Mess ag e Summary – [[CUSIP]] Totals Record (06) ........................................................................ 14 
EPN Mess ag e Summary – Report Trailer Record (99)........................................................................ 15 
 

---

## Page 4

EPN Message Summary Report Format – NJE File Layouts 
Version C ontrol 4 
VERSION CONTROL 
Date Version Name Description of Change 
07/19/2006 Original MBSD Initial Version 
3/13/2023 2.0 J. Sheeran Updated formatting only. Content is unchanged 
 
 
 
 
 

---

## Page 5

EPN Message Summary Report Format – NJE File Layouts  
File Transmission Layout Ov erview 5 
FILE TRANSMISSION LAYOUT OVERVIEW 
EPN Message Summary Report Format 
Purpose 
The EPN Message Summary report summarizes messages sent and received for all [[participant]] accounts. The 
AutoRoute product [[ID]] for COB Message Summary Report is 13150382 and the [[EOD]] Message Summary 
Report is 13150385 
Frequency 
Daily (Close of Business & End of Day). 
Record Layouts 
All records are of equal length - 275 bytes 
There are 7 different record types, each uniquely identified by card code, as follows: card codes 0l through 06, 
& 99. 
Account/Report Header Record (Card Code 01) 
Control record which signifies the beginning of the report for a given account. Contains recipient 
account and report identification items. 
Security Subheading Record (Card Code 02) 
Control record which signifies the beginning of the next security class. 
Contra Totals Record (Card Code 03)* 
Contains totals for message types ON (original notification), DK (DKS), CX (cancels) that were sent/received 
within this class for the recipient account. 
Contra Totals Record (Card Code 04)* 
Contains totals for message type CC (Cancel and Correct) that were sent/received within this class for the 
recipient account. 
Security Totals Record (Card Code 05)* 
Contains totals for message types ON (original notification), DK (DKs), CX (cancels) within this 
class for the recipient account 

---

## Page 6

EPN Message Summary Report Format – NJE File Layouts  
File Transmission Layout Ov erview 6 
Security Totals Record (Card Code 06)* 
Contains totals for message types CC (Cancel and Correct) within this class for the recipient account 
Trailer Control Recrd (Card Code 99) 
Trailer record indicates the end of the report for the recipient account. 
* MBSD accumulates totals for Original Face, Current Face, Principal, Interest, and Net Money. If any of these 
fields is non-numeric, an incomplete total indicator is set to ‘*’ for the respective field. 
  

---

## Page 7

EPN Message Summary Report Format – NJE File Layouts  
EPN Message Summary Report Format – NJE File Layouts 7 
EPN MESSAGE SUMMARY REPORT FORMAT – NJE 
FILE LAYOUTS 
EPN Message Summary – Header Record (01) 
Control record which signifies the beginning of the report for a given account. Contains recipient account and 
report identification items. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT1-CARD-CODE 2 N PIC 9(02). Header Record,  Card Code  = '01' 
RPT-MSR-DT1-RPT-[[ID]] 8 A/N PIC X(08). Report  [[ID]] = 'MB3341-A' 
RPT-MSR-DT1-[[participant]]-
[[ID]] 
3 N PIC 9(03). [[participant]]  [[ID]] 
RPT-MSR-DT1-AGG-MBR 2 N PIC 9(02). Aggregate  Number 
RPT-MSR-DT1-ACCOUNT 4 A/N PIC X(4). Account  Symbol 
RPT-MSR-DT1-PART-NAME 40 A/N PIC X(40). [[participant]]  Name 
RPT-MSR-DT1-BUS-DATE 6 N PIC 9(06). Date of Activity  (MMDDYY) 
RPT-MSR-DT1-PASS 2 A/N PIC X(02). Pass Indicator  (CB = Close  of Business,  ED = End  
of Day) 
RPT-MSR-DT1-BUS-DATE2 6 N PIC 9(06). Date of  Report  (MMDDYY) 
RPT-MSR-DT1-TIME-STAMP 6 N PIC 9(06). Report  Time Stamp (will be zero filled)  
FILLER 196 A/N PIC X(196).  
 275    
EPN Message Summary – Security Subheading Record (02) 
Control record which signifies the beginning of the next security class. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT2-CARD-CODE 2 N PIC 9(02). Security Subheading,  Card Code  = '02' 
RPT-MSR-DT2-ACCOUNT 4 A/N PIC X(04). Submitter Account  Symbol 
RPT-MSR-DT2-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MSR-DT2-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MSR-DT2-TBA-[[CUSIP]] 10 A/N PIC X(10). TBA [[CUSIP]] (9 alphanumerics  followed  by blank)  
FILLER 4 A/N PIC X(4).  

---

## Page 8

EPN Message Summary Report Format – NJE File Layouts  
EPN Message Summary Report Format – NJE File Layouts 8 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT2-TBA-[[CUSIP]]-
DESC 
40 A/N PIC X(40). TBA [[CUSIP]] Description  
FILLER 211 A/N PIC X(211).  
 275    
EPN Message Summary – Contra Totals Record (03) 
Contains totals for message types ON (original notification), DK (DKS), CX (cancels) that were sent/received 
within this class for the recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT3-CARD-CODE 2 N PIC 9(02). Contra Totals, Card Code  = '03' 
RPT-MSR-DT3-ACCOUNT 4 A/N PIC X(04). Submitter Account  Symbol 
RPT-MSR-DT3-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MSR-DT3-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MSR-DT3-TBA-[[CUSIP]] 10 A/N PIC X(10). TBA [[CUSIP]] (9 alphanumerics  followed  by 
blank)  
RPT-MSR-DT3-CONTRA 4 A/N PIC X(04). Contra Account  
RPT-MSR-DT3-ONR-NBR-MSG 7 N PIC 9(07). Number of Messages  Received  (ON) 
RPT-MDR-DT3-ONR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-ONR-ORG-FACE 13 N PIC 9(13). Original Face Value Received  (ON) 
RPT-MSR-DT3-ONR-ORG-FACE-SGN 1 A/N PIC X(01). Original Face Value Received  (ON) Sign  
Indicator  ('-' or blank)  
RPT-MDR-DT3-ONR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-ONR-NET-MONEY 15 N PIC 
9(13)V9(02) 
Net Money  Received  (ON) 
RPT-MSR-DT3-ONR-NET-MONEY-
SGN 
1 A/N PIC X(01). Net Money  Received  (ON) Sign  Indicator  ('-' 
or blank)  
RPT-MSR-DT3-ONS-NBR-MSG 7 N PIC 9(07). Number of Messages  Sent (ON) 
RPT-MDR-DT3-ONS-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-ONS-ORG-FACE 13 N PIC 9(13). Original Face  Value Sent (ON) 
RPT-MSR-DT3-ONS-ORG-FACE-SGN 1 A/N PIC X(01). Original Face Value Sent (ON) Sign Indicator  
('-' or blank)  
RPT-MDR-DT3-ONS-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-ONS-NET-MONEY 15 N PIC 
9(13)V9(02) 
Net Money  Sent (ON) 

---

## Page 9

EPN Message Summary Report Format – NJE File Layouts  
EPN Message Summary Report Format – NJE File Layouts 9 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT3-ONS-NET-MONEY-
SGN 
1 A/N PIC X(01). Net Money  Sent (ON) Sign  Indicator  ('-' or 
blank)  
RPT-MSR-DT3-DKR-NBR-MSG 7 N PIC 9(07). Number of Messages  Received  (DKs) 
RPT-MDR-DT3-DKR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-DKR-ORG-FACE 13 N PIC 9(13). Original Face Value Received  (DKs) 
RPT-MSR-DT3-DKR-ORG-FACE-SGN 1 A/N PIC X(01). Original Face Value Received  (DKs) Sign  
Indicator  ('-' or blank)  
RPT-MDR-DT3-DKR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-DKR-NET-MONEY 15 N PIC 
9(13)V9(02) 
Net Money  Received  (DKs) 
RPT-MSR-DT3-DKR-NET-MONEY-
SGN 
1 A/N PIC X(01). Net Money  Received  (DKs) Sign  Indicator  ('-' 
or blank)  
RPT-MSR-DT3-DKS-NBR-MSG 7 N PIC 9(07). Number of Messages  Sent (DKs) 
RPT-MDR-DT3-DKS-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-DKS-ORG-FACE 13 N PIC 9(13). Original Face  Value Sent (DKs) 
RPT-MSR-DT3-DKS-ORG-FACE-SGN 1 A/N PIC X(01). Original Face Value Sent (DKs) Sign Indicator  
('-' or blank)  
RPT-MDR-DT3-DKS-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-DKS-NET-MONEY 15 N PIC 
9(13)V9(02) 
Net Money  Sent (DKs) 
RPT-MSR-DT3-DKS-NET-MONEY-
SGN 
1 A/N PIC X(01). Net Money  Sent (DKs) Sign  Indicator (' -' or 
blank)  
RPT-MSR-DT3-CXR-NBR-MSG 7 N PIC 9(07). Number of Messages  Received  (CX) 
RPT-MDR-DT3-CXR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-CXR-ORG-FACE 13 N PIC 9(13). Original Face Value Received  (CX) 
RPT-MSR-DT3-CXR-ORG-FACE-SGN 1 A/N PIC X(01). Original Face Value Received (CX) Sign  
Indicator (' -' or blank)  
RPT-MDR-DT3-CXR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-CXR-NET-MONEY 15 N PIC 
9(13)V9(02) 
Net Money  Received  (CX) 
RPT-MSR-DT3-CXR-NET-MONEY-
SGN 
1 A/N PIC X(01). Net Money  Received  (CX) Sign  Indicator  ('-' 
or blank)  
RPT-MSR-DT3-CXS-NBR-MSG 7 N PIC 9(07). Number of Messages  Sent (CX) 
RPT-MDR-DT3-CXS-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-CXS-ORG-FACE 13 N PIC 9(13). Original Face  Value Sent (CX) 

---

## Page 10

EPN Message Summary Report Format – NJE File Layouts  
EPN Message Summary Report Format – NJE File Layouts 10 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT3-CXS-ORG-FACE-SGN 1 A/N PIC X(01). Original Face Value Sent (CX) Sign Indicator  
('-' or blank)  
RPT-MDR-DT3-CXS-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-CXS-NET-MONEY 15 N PIC 
9(13)V9(02) 
Net Money  Sent (CX) 
RPT-MSR-DT3-CXS-NET-MONEY-
SGN 
1 A/N PIC X(01). Net Money  Sent (CX) Sign  Indicator  ('-' or 
blank)  
FILLER 17 A/N PIC X(17).  
 275    
EPN Message Summary – Contra Totals Record (04) 
Contains totals for message type CC (Cancel and Correct) that were sent/received within this class for the 
recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT3-CARD-CODE 2 N PIC 9(02). Contra Totals, Card Code  = '04' 
RPT-MSR-DT3-ACCOUNT 4 A/N PIC X(04). Submitter Account  Symbol 
RPT-MSR-DT3-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MSR-DT3-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MSR-DT3-TBA-[[CUSIP]] 10 A/N PIC X(10). TBA [[CUSIP]] (9 alphanumerics  followed  by blank)  
RPT-MSR-DT3-CONTRA 4 A/N PIC X(04). Contra Account  
RPT-MSR-DT3-CCR-NBR-MSG 7 N PIC 9(07). Number of Messages  Received  (CC) 
RPT-MDR-DT3-CCR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-CCR-ORG-FACE 13 N PIC 9(13). Original Face Value Received  (CC) 
RPT-MSR-DT3-CCR-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Received (CC) Sign  Indicator  
('-' or blank)  
RPT-MDR-DT3-CCR-NET-INC 1 A/N PIC X(01). Incomplete  Total Indicator (* = incomplete)  
RPT-MSR-DT3-CCR-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Net Money  Received  (CC) 
RPT-MSR-DT3-CCR-NET-
MONEY-SGN 
1 A/N PIC X(01). Net Money  Received  (CC) Sign  Indicator  ('-' or 
blank)  
RPT-MSR-DT3-[[CCS]]-NBR-MSG 7 N PIC 9(07). Number of Messages  Sent (CC) 
RPT-MDR-DT3-[[CCS]]-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-[[CCS]]-ORG-FACE 13 N PIC 9(13). Original Face  Value Sent (CC) 

---

## Page 11

EPN Message Summary Report Format – NJE File Layouts  
EPN Message Summary Report Format – NJE File Layouts 11 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT3-[[CCS]]-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Sent (CC) Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT3-[[CCS]]-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT3-[[CCS]]-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Net Money  Sent (CC) 
RPT-MSR-DT3-[[CCS]]-NET-
MONEY-SGN 
1 A/N PIC X(01). Net Money  Sent (CC) Sign  Indicator  ('-' or blank)  
FILLER 173 A/N PIC X(173).  
 275    
EPN Message Summary – [[CUSIP]] Totals Record (05) 
Contains totals for message types ON (original notification), DK (DKs), CX (cancels) within this class for the 
recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT4-CARD-CODE 2 N PIC 9(02). [[CUSIP]] Totals, Card Code =  '05' 
RPT-MSR-DT4-ACCOUNT 4 A/N PIC X(04). Submitter Account  Symbol 
RPT-MSR-DT4-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MSR-DT4-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MSR-DT4-TBA-[[CUSIP]] 10 A/N PICX(10). TBA [[CUSIP]] (9 alphanumerics  followed  by blank)  
FILLER 4 A/N PIC X(04).  
RPT-MSR-DT4-ONR-NBR-MSG 7 N PIC 9(07). Number of Messages  Received  (ON) 
RPT-MDR-DT4-ONR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-ONR-ORG-FACE 13 N PIC 9(13). Original Face Value Received  (ON) 
RPT-MSR-DT4-ONR-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Received  (ON) Sign  Indicator  
('-' or blank)  
RPT-MDR-DT4-ONR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-ONR-NET-
MONEY 
15 N PIC 
9(13)V9(02) 
Net Money  Received  (ON) 
RPT-MSR-DT4-ONR-NET-
MONEY-SGN 
1 A/N PIC X(01). Net Money  Received  (ON) Sign  Indicator  ('-' or 
blank)  
RPT-MSR-DT4-ONS-NBR-MSG 7 N PIC 9(07). Number of Messages  Sent (ON) 
RPT-MDR-DT4-ONS-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-ONS-ORG-FACE 13 N PIC 9(13). Original Face  Value Sent (ON) 

---

## Page 12

EPN Message Summary Report Format – NJE File Layouts  
EPN Message Summary Report Format – NJE File Layouts 12 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT4-ONS-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Sent (ON) Sign Indicator  ('-' 
or blank)  
RPT-MDR-DT4-ONS-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-ONS-NET-
MONEY 
15 N PIC 9(13) 
V9(02) 
Net Money  Sent (ON) 
RPT-MSR-DT4-ONS-NET-
MONEY-SGN 
1 A/N PIC X(01). Net Money  Sent (ON) Sign  Indicator  ('-' or blank)  
RPT-MSR-DT4-DKR-NBR-MSG 7 N PIC 9(07). Number of Messages  Received  (DKs) 
RPT-MDR-DT4-DKR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-DKR-ORG-FACE 13 N PIC 9(13). Original Face Value Received  (DKs) 
RPT-MSR-DT4-DKR-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Received  (DKs) Sign  Indica t or 
('-' or blank)  
RPT-MDR-DT4-DKR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-DKR-NET-
MONEY 
15 N PIC 9(13) 
V9(02) 
Net Money  Received  (DKs) 
RPT-MSR-DT4-DKR-NET-
MONEY-SGN 
1 A/N PIC X(01). Net Money  Received  (DKs) Sign  Indicator  ('-' or 
blank)  
RPT-MSR-DT4-DKS-NBR-MSG 7 N PIC 9(07). Number of Messages  Sent (DKs) 
RPT-MDR-DT4-DKS-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-DKS-ORG-FACE 13 N PIC 9(13). Original Face  Value Sent (DKs) 
RPT-MSR-DT4-DKS-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Sent (DKs) Sign Indicator  ('-' 
or blank)  
RPT-MDR-DT4-DKS-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-DKS-NET-
MONEY 
15 N PIC 9(13) 
V9(02) 
Net Money  Sent (DKs) 
RPT-MSR-DT4-DKS-NET-
MONEY-SGN 
1 A/N PIC X(01). Net Money  Sent (DKs) Sign  Indicator (' -' or blank)  
RPT-MSR-DT4-CXR-NBR-MSG 7 N PIC 9(07). Number of Messages  Received  (CX) 
RPT-MDR-DT4-CXR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-CXR-ORG-FACE 13 N PIC 9(13). Original Face Value Received  (CX) 
RPT-MSR-DT4-CXR-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Received (CX) Sign  Indicator 
('-' or blank)  
RPT-MDR-DT4-CXR-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-CXR-NET-
MONEY 
15 N PIC 9(13) 
V9(02) 
Net Money  Received  (CXs) 
RPT-MSR-DT4-CXR-NET-
MONEY-SGN 
1 A/N PIC X(01). Net Money  Received  (CXs) Sign  Indicator  ('-' or 
blank)  

---

## Page 13

EPN Message Summary Report Format – NJE File Layouts  
EPN Message Summary Report Format – NJE File Layouts 13 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT4-CXS-NBR-MSG 7 N PIC 9(07). Number of Messages  Sent (CXs) 
RPT-MDR-DT4-CXS-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-CXS-ORG-FACE 13 N PIC 9(13). Original Face  Value Sent (CXs) 
RPT-MSR-DT4-CXS-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Sent (CXs) Sign Indicator  ('-' 
or blank)  
RPT-MDR-DT4-CXS-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-CXS-NET-
MONEY 
15 N PIC 9(13) 
V9(02) 
Net Money  Sent (CX) 
RPT-MSR-DT4-CXS-NET-
MONEY-SGN 
1 A/N PIC X(01). Net Money  Sent (CX) Sign  Indicator  ('-' or blank)  
FILLER 17 A/N PIC X(17).  
 275    
 
 
  

---

## Page 14

EPN Message Summary Report Format – NJE File Layouts  
EPN Message Summary Report Format – NJE File Layouts 14 
EPN Message Summary – [[CUSIP]] Totals Record (06) 
Contains totals for message type CC (Cancel and Correct) within this class for the recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT4-CARD-CODE 2 N PIC 9(02). [[CUSIP]] Totals, Card Code =  '06' 
RPT-MSR-DT4-ACCOUNT 4 A/N PIC X(04). Submitter Account  Symbol 
RPT-MSR-DT4-STTL-YY 2 A/N PIC X(02). [[settlement]] Year (YY) 
RPT-MSR-DT4-STTL-MM 2 A/N PIC X(02). [[settlement]] Month (MM) 
RPT-MSR-DT4-TBA-[[CUSIP]] 10 A/N PICX(10). TBA [[CUSIP]] (9 alphanumerics  followed  by blank)  
FILLER 4 A/N PIC X(04).  
RPT-MSR-DT4-CCR-NBR-MSG 7 N PIC 9(07). Number of Messages  Received  (CC) 
RPT-MDR-DT4-CCR-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-CCR-ORG-
FACE 
13 N PIC 9(13). Original Face Value Received  (CC) 
RPT-MSR-DT4-CCR-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Received (CC) Sign  Indicator  
('-' or blank)  
RPT-MDR-DT4-CCR-NET-INC 1 A/N PIC X(01). Incomplete  Total Indicator (* = incomplete)  
RPT-MSR-DT4-CCR-NET-
MCCEY 
15 N PIC 
9(13)V9(02) 
Net Money  Received  (CC) 
RPT-MSR-DT4-CCR-NET-
MCCEY-SGN 
1 A/N PIC X(01). Net Money  Received  (CC) Sign  Indicator  ('-' or 
blank)  
RPT-MSR-DT4-[[CCS]]-NBR-MSG 7 N PIC 9(07). Number of Messages  Sent (CC) 
RPT-MDR-DT4-[[CCS]]-ORG-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-[[CCS]]-ORG-
FACE 
13 N PIC 9(13). Original Face  Value Sent (CC) 
RPT-MSR-DT4-[[CCS]]-ORG-
FACE-SGN 
1 A/N PIC X(01). Original Face Value Sent (CC) Sign  Indicator  ('-' or 
blank)  
RPT-MDR-DT4-[[CCS]]-NET-INC 1 A/N PIC X(01). Incomplete  Total  Indicator  (* = incomplete)  
RPT-MSR-DT4-[[CCS]]-NET-
MCCEY 
15 N PIC 9(13) 
V9(02) 
Net Money  Sent (CC) 
RPT-MSR-DT4-[[CCS]]-NET-
MCCEY-SGN 
1 A/N PIC X(01). Net Money  Sent (CC) Sign  Indicator  ('-' or blank)  
FILLER 173 A/N PIC X(173).  
 275    
 

---

## Page 15

EPN Message Summary Report Format – NJE File Layouts  
EPN Message Summary Report Format – NJE File Layouts 15 
EPN Message Summary – Report Trailer Record (99) 
Trailer record indicates the end of the report for the recipient account. 
Field Name Length Type Cobol Pic Description/comment  
RPT-MSR-DT9-CARD-CODE 2 N PIC 9(02). Report  Trailer  Record,  Card Code  = '99' 
FILLER 13 A/N PIC X(13).  
RPT-MSR-DT9-ACCOUNT 4 A/N PIC X(04). Account  Symbol 
FILLER 1 A/N PIC X(01).  
RPT-MSR-DT9-LOGICAL-
COUNT 
7 N PIC 9(07). Logical  Record  Count  
FILLER 1 A/N PIC X(01).  
RPT-MSR-DT9-PHYSICAK-
COUNT 
7 N PIC 9(07). Physical  Record Count  
FILLER 240 A/N PIC X(240).  
 275    

---

## Page 16

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 