---
title: "Networking Position Reporting Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/networking_positionReporting_mfs334_20231017.pdf"
pages: 25
size: "399.4 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Networking Position Reporting Record Layouts

**Original File:** [networking_positionReporting_mfs334_20231017.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/networking_positionReporting_mfs334_20231017.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 25  
**File Size:** 399.4 KB  

---

## Page 1

 
 
   
Networking 
POSITION REPORTING RECORD LAYOUTS 
OCTOBER 17, 2023 
 

---

## Page 2

Position Reporting Record Layouts 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 3 
Position Header (F57) .......................................................................................................................................... 4 
Position Detail (F58) ............................................................................................................................................. 5 
Position Detail (F58) #1 ...................................................................................................................................... 5 
Position Detail (F58) #2 ...................................................................................................................................... 7 
Position Trailer (F59) ........................................................................................................................................... 8 
Position Trailer (F59) #1 ..................................................................................................................................... 8 
Position Trailer (F59) #2 ...................................................................................................................................10 
Position Grand Total Trailer (F60) .................................................................................................................... 11 
Input Records’ Layout ....................................................................................................................................... 12 
Position File Datatrak Header ...........................................................................................................................12 
Position File Datatrak Trailer ............................................................................................................................13 
Output Records’ Layout .................................................................................................................................... 14 
Output Header Position File (N00) ....................................................................................................................14 
Input Acknowledgment - Position (NPO) ..........................................................................................................15 
APPENDIX – Summary of Changes .................................................................................................................. 16 
Summary of changes – effective Q1, 2019 ...................................................................................................... 17 
Summary of changes – effective Q1, 2017 ...................................................................................................... 18 
Summary of changes – effective Q3, 2014 ...................................................................................................... 19 
Summary of changes – effective Q1, 2013 ...................................................................................................... 20 
Summary of changes – effective Q4, 2011 ...................................................................................................... 21 
Summary of changes – effective Q2, 2010 ...................................................................................................... 22 
Summary of changes – effective Q4, 2008 ...................................................................................................... 24 
 

---

## Page 3

Position Reporting Record Layouts 
History of Important Notices 3 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notice 
October 17, 2023  Record rebranded and reviewed  
May 15, 2023 Record rebranded and reviewed 
March 25, 2019 Please see Important Notice: 
a8658 P&S 8233 Dated December 19, 2018 
February 27, 2017 Please see Important Notice: 
a8286 P&S 7861 Dated November 8, 2016 
July 28, 2014 Please see Important Notice: 
a7687 P&S 7357 Dated February 24, 2014 
March 18, 2013 Please see Important Notice: 
a7472 P&S 7042 Dated August 16, 2012, and 
a7567 P&S 7137 Dated January 9,2013 
October 17, 2011 Please see Important Notice: 
a7241 P&S 6811 Dated July 8, 2011 
June 14, 2010 Please see Important Notice: 
a6948 P&S 6518 Dated February 18, 2010 
October 20, 2008 Please see Important Notice: 
a6658 P&S 6228 Dated July 11, 2008 
November 20, 2006 Please see Important Notice: 
a6272 P&S 5842 Dated July 17, 2006 
March 19, 2005 Please see Important Notice: 
a5976 P&S 5546 Dated February 4, 2005 

---

## Page 4

Position Reporting Record Layouts 
Position Header (F57) 4 
POSITION HEADER (F57) 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
The position header record is used to introduce a series of detail position records for a particular firm and 
Security Issue. 
Position Header (F57) 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 57 = Position Header R 
Filler 4 5 2 A/N Space R 
Clearing/Settling Firm Number 6 9 4 N  R 
Clearing/Settling Fund Number 10 13 4 N  R 
Security Issue Number 14 22 9 A/N  R 
Balance Date 23 30 8 N mmddccyy R 
TPA/Investment Agent Number 31 34 4 A/N  O 
Agent for Firm Number 35 38 4 A/N  O 
Filler 39 96 58 A/N Space R 
Sequence Number 97 98 2 A/N 01 O 
Filler/Reject Code 99 100 2 A/N Input: Space Output: Reject Code R 

---

## Page 5

Position Reporting Record Layouts 
Position Detail (F58) 5 
POSITION DETAIL (F58) 
Position Detail (F58) #1 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
The position detail record is used to report individual account positions to a firm. Any account that has both 
book and physical share positions will require two position records. 
Position Detail (F58) #1 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 58 = Position Detail R 
Filler 4 4 1 A/N Space R 
Firm Identification Number 5 24 20 A/N Required if Fund Account Number is not 
provided 
OC 
Closing Book/Physical 
Balance 
25 37 13 N 999,999,999.9999 
 
Required if Closing Book/Physical Balance – 
Extended is NOT provided in record F58 
sequence #2. 
Otherwise, it is not allowed. 
OC LOI Escrow Balance 38 50 13 N 999,999,999.9999 R 
Share Balance Indicator 51 51 1 N 1 = Book [[shares]] 
2 = Physical [[shares]] 
R 

---

## Page 6

Position Reporting Record Layouts 
Position Detail (F58) 6 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
[[Dividend]] Code 52 52 1 A/N 0 = [[Dividend]] Cash/Ltcg -Cash/ Stcg-Cash 
1 = [[Dividend]] Reinvest/Ltcg- Reinvest/Stcg- 
Reinvest 
2 = [[Dividend]] Cash/Ltcg- Cash/Stcg- 
Reinvest 
3 = [[Dividend]] Cash/Ltcg- Reinvest/ Stcg- 
Reinvest 
4 = [[Dividend]] Cash/Ltcg- Reinvest/Stcg- 
Cash 
5 = [[Dividend]] Reinvest/Ltcg- Cash/Stcg- 
Cash 
6 = [[Dividend]] Reinvest/Ltcg- Reinvest/Stcg- 
Cash 
7 = [[Dividend]] Reinvest/Ltcg- Cash/ Stcg- 
Reinvest 
R 
Network Control Indicator 53 53 1 A/N 0 = Matrix Level 0 
3 = Matrix Level 3 
4 = Matrix Level 4 
R 
Filler 54 55 2 A/N Space 
This field was changed from “Fund Alpha 
Code” to Filler 
R 
Filler 56 57 2 A/N Space 
This field was changed from “Firm Alpha 
Code” to Filler 
R 
Fund Account Number 58 77 20 A/N Required if Firm Identification Number not 
provided 
OC 
Accrual Money Amount/ 
Accrual Money Account 
Balance 
78 93 16 N 99,999,999,999,999.99 O 
Filler 94 94 1 A/N Space R 
Social Code 95 96 2 A/N  R 
Sequence Number 97 98 2 A/N 01 
Required if record F58 sequence #2 follows. 
OC 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 
 
 
  

---

## Page 7

Position Reporting Record Layouts 
Position Detail (F58) 7 
Position Detail (F58) #2 
Optional Conditional Record  
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
This record is required if Closing Book/Physical Balance is NOT provided in record F58 sequence #1. 
Otherwise, it is optional. 
Position Detail (F58) #2 
#2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 58 = Position Detail R 
Account Representative [[ID]] 
 
4 12 9 A/N Account Representative [[ID]] O 
Account Representative 
Name 
 
13 27 15 A/N Account Representative Name O 
Branch Identification Number 
 
28 36 9 A/N Branch [[ID]] Number O 
Account Open Date 
 
 
37 44 8 A/N mmddccyy 
Must be a valid calendar date 
 
Best Practice: 
Date of account establishment for the 
particular Security Issue [[ID]]. This is NOT the 
date of account funding. 
O 
Filler 45 80 36 A/N Space R 
Closing Book/Physical 
Balance - Extended 
81 96 16 N 999,999,999,999.9999 
Required if Closing Book/Physical Balance is 
NOT provided in record F58 sequence #1. 
Otherwise, it is not allowed. 
OC 
Sequence Number 97 98 2 A/N 02 R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 8

Position Reporting Record Layouts 
Position Trailer (F59) 8 
POSITION TRAILER (F59) 
Position Trailer (F59) #1 
Required Record 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
The position trailer record is used to recap the detail records for a particular fund Security Issue and firm.  
Position Trailer (F59) #1 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 59 = Position Trailer R 
Filler 4 5 2 N space R 
Clearing/Settling Firm Number 6 9 4 N  R 
Total Closing Book Share 
Balance 
10 24 15 N 99,999,999,999.9999 
Required to recap Closing Book/Physical 
Balance in Detail records F58 sequence #1 
when Share Balance Indicator = 1 (Book 
[[shares]]). 
Otherwise, it is optional. 
OC 
Total LOI Escrow Share 
Balance 
25 37 13 N 999,999,999.9999 R 
Total Records 38 44 7 N 9,999,999 
(Including Headers and Trailers) 
R 
Total Accounts 45 52 8 N 99,999,999 R 
TPA/Investment Agent Number 53 56 4 A/N Required if it exists on the Header Record OC 
Total Closing Physical Share 
Balance 
57 71 15 N 99,999,999,999.9999 
Required to recap Closing Book/Physical 
Balance in Detail records F58 sequence #1 
when Share Balance Indicator = 2 
(Physical [[shares]]). 
Otherwise, it is optional. 
OC 
Filler 72 96 25 A/N Space R 
Sequence Number 97 98 2 A/N 01 
Required if record F59 sequence #2 follows 
OC 

---

## Page 9

Position Reporting Record Layouts 
Position Trailer (F59) 9 
#1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 
 
 
  

---

## Page 10

Position Reporting Record Layouts 
Position Trailer (F59) 10 
Position Trailer (F59) #2 
Optional Conditional Record  
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
This record is required to recap Closing Book/Physical Balance – Extended in Detail records F58 sequence #2. 
Otherwise, it is optional. 
Position Trailer (F59) #2 
#2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 59 = Position Trailer R 
Filler 4 5 2 N space R 
Clearing/Settling Firm Number 6 9 4 N  R 
Total Closing Book Share 
Balance – Extended 
10 26 17 N 9,999,999,999,999.9999 
 
Required to recap Closing Book/Physical 
Balance – Extended in Detail records F58 
sequence #2 when Share Balance Indicator 
= 1 (Book [[shares]]). 
Otherwise, it is optional. 
OC 
Total Closing Physical Share 
Balance – Extended 
27 43 17 N 9,999,999,999,999.9999 
 
Required to recap Closing Book/Physical 
Balance – Extended in Detail records F58 
sequence #2 when Share Balance Indicator 
= 2 (Physical [[shares]]). 
Otherwise, it is optional. 
OC 
Filler 44 96 53 A/N Space R 
Sequence Number 97 98 2 A/N 02 R 
Filler/Reject Code 99 100 2 A/N Input: Space  
Output: Reject Code 
R 

---

## Page 11

Position Reporting Record Layouts 
Position Grand Total Trailer (F60) 11 
POSITION GRAND TOTAL TRAILER (F60) 
Input from Fund to [[NSCC]]  
Output from [[NSCC]] to Firm 
The position Grand Total Trailer record is used to recap all records included in a fund’s position file.  
Position Grand Total Trailer (F60) 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N F = Fund R 
Record Type 2 3 2 A/N 60 = Position Grand Total Trailer R 
Filler 4 5 2 N Space R 
Fund Clearing Number / 
Recipient Number 
6 9 4 N Fund Clearing Number -on Input from Fund to 
[[NSCC]]; 
Recipient Number -on Output from [[NSCC]] to 
[[participant]]. 
R 
Total Position Records 10 17 8 N 99,999,999 
(Including Headers and Trailers) 
R 
Filler 18 100 83 A/N Space R 

---

## Page 12

Position Reporting Record Layouts 
Input Records’ Layout 12 
INPUT RECORDS’ LAYOUT 
Position File Datatrak Header 
Input from Fund to [[NSCC]] 
All input files must include the DATATRAK Header and End of File Trailer records. Transmissions failing these 
criteria will not be accepted. 
Position File Datatrak Header 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value ‘26326’ R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value 'NETWORKING RJE FUND POS' R 
Multi Batch Indicator 60 60 1 A/N N = Not last batch 
Y = Last batch 
R 
Multi Batch Number 61 63 3 N  R 
Filler 64 100 37 A/N Space R 
 
 
  

---

## Page 13

Position Reporting Record Layouts 
Input Records’ Layout 13 
Position File Datatrak Trailer 
Input from Fund to [[NSCC]] 
Position File Datatrak Trailer 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'END.S' R 
DATATRAK SYSID 6 10 5 A/N Value '26326' R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Data File Record Count 27 33 7 N DATATRAK Header & Trailer not included in 
count 
R 
Filler 34 100 67 A/N Space R 

---

## Page 14

Position Reporting Record Layouts 
Output Records’ Layout 14 
OUTPUT RECORDS’ LAYOUT 
Output Header Position File (N00) 
Output Header Position File (N00) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 4 1 A/N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '11111111111' 
Transmission Date 20 27 8 N mmddccyy 
Autoroute File [[ID]] 28 35 8 A/N Value '02102156' 
Literal 36 43 8 A/N Value 'POSITION' 
Filler 44 100 57 A/N Space 
 
 
  

---

## Page 15

Position Reporting Record Layouts 
Output Records’ Layout 15 
Input Acknowledgment - Position (NPO) 
Output from [[NSCC]] to Fund 
The Input Acknowledgment records are an affirmation from [[NSCC]] of any firm or fund transmission. Records 
coming into [[NSCC]] will produce an output file directed back to the originator for each application submitted. The 
four groups are Conversion, Position, Dividends and Activity. All contain a total record count and the date the 
file was processed. If there are any rejects for that particular application, they will be included on this f ile as 
well. 
Input Acknowledgment - Position (NPO) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N PO = Position 
Filler 4 4 1 A/N Space 
Clearing/Settling Fund # 5 8 4 N  
Processing Date 9 16 8 N mmddccyy 
Total Records Received 17 24 8 N 99,999,999 
(Includes any Headers and Trailers) 
Filler 25 100 76 A/N Space 
 
 

---

## Page 16

Position Reporting Record Layouts 
APPENDIX – Summary of Changes 16 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 

---

## Page 17

Position Reporting Record Layouts 
Summary of changes – effective Q1, 2019 17 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 18

Position Reporting Record Layouts 
Summary of changes – effective Q1, 2017 18 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2017 
Add New Fields 
New Name Record Type and Location Requirements 
Account Representative [[ID]] F58 seq.#2, start 4, end 12, Length 9, A/N 
, Optional 
Account Representative [[ID]] 
Account Representative 
Name 
F58 seq.#2, start 13, end 27, Length 15, 
A/N, Optional 
Account Representative Name 
Branch Identification Number F58 seq.#2, start 28, end 36, Length 9, 
A/N, Optional. 
Branch [[ID]] Number 
Account Open Date F58 seq.#2, start 37, end 44, Length 8, 
A/N , Optional 
mmddccyy 
Must be a valid calendar date  
Best Practice: 
Date of account establishment for the 
particular Security Issue [[ID]]. This is 
NOT the date of account funding. 
 
Reject Codes 
The following new reject code has been added: 
Reject Code Description 
Q8 Account Open Date is invalid 

---

## Page 19

Position Reporting Record Layouts 
Summary of changes – effective Q3, 2014 19 
SUMMARY OF CHANGES – EFFECTIVE Q3, 2014 
Rename Existing Fields 
New Field Name Record Type and Location Old Name 
Filler F58 seq.#1, start 54, end 55, length 02, A/N Fund Alpha Code 
Filler F58 seq.#1, start 56, end 57, length 02, A/N Firm Alpha Code 

---

## Page 20

Position Reporting Record Layouts 
Summary of changes – effective Q1, 2013 20 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2013 
Requirements Changed for Existing Field 
Field Name Record Type, Location, Current 
Requirements 
New Requirement and Description 
Network Control Indicator F58 seq.#1, start 53, end 53, length 1, A/N, R 0 = Matrix Level 0 
3 = Matrix Level 3 
4 = Matrix Level 4 
 
(Removed 1 = Level 1; 2 = Level 2 effective 
Q1, 2013 ) 
Description also updated to “Matrix Level” 

---

## Page 21

Position Reporting Record Layouts 
Summary of changes – effective Q4, 2011 21 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2011 
Add New Field 
New Name Record Type and Location Requirements 
Social Code F58 seq.#1, start 95, end 96, Length 02 Required 

---

## Page 22

Position Reporting Record Layouts 
Summary of changes – effective Q2, 2010 22 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2010 
Add New Record 
Record Record Name Requirements 
F58 sequence #2 Position Detail (F58) #2 Optional Conditional. Required if Closing Book/Physical Balance is 
NOT provided in record F58 sequence #1. 
F59 sequence #2 Position Trailer (F59) #2 Optional Conditional. Required to recap Closing Book/Physical 
Balance – Extended fields provided in Detail record F58 sequence 
#2 
 
Add New Fields 
New Field Name Record Type and Location Value Requirements 
Sequence Number F57, start 97, end 98, length 02 01 Optional 
F58 seq.#1, start 97, end 98, Length 02 01 Optional Conditional. Required if record F58 
sequence #2 follow s. 
F58 seq.#2, start 97, end 98, length 02 02 Required 
F59 seq.#1, start 97, end 98, length 02 01 Optional Conditional. Required if record F59 
sequence #2 follow s. 
F59 seq.#2, start 97, end 98, length 02 02 Required 
Closing 
Book/Physical 
Balance - Extended 
F58 seq.#2, start 81, end 96, length 16; 
999,999,999,999.9999 
 Optional Conditional. Required if Closing 
Book/Physical Balance is NOT provided in 
record F58 sequence #1. Otherwise it is not 
allow ed. 
Total Closing Book 
Share Balance - 
Extended 
F59 seq.#2, start 10, end 26, length 17, 
9,999,999,999,999.9999 
 Optional Conditional. Required to recap 
Closing Book/Physical Balance – Extended in 
Detail records F58 sequence #2 when Share 
Balance Indicator = 1 (Book [[shares]]). 
Total Closing 
Physical Share 
Balance - Extended 
F59 seq.#2, start 27, end 43, length 17; 
9,999,999,999,999.9999 
 Optional Conditional. Required to recap 
Closing Book/Physical Balance – Extended in 
Detail records F58 sequence #2 when Share 
Balance Indicator = 2 (Physical [[shares]]). 
 
 
 
 
 
 

---

## Page 23

Position Reporting Record Layouts 
Summary of changes – effective Q2, 2010 23 
Rename Existing Field 
New Field Name Record Type and Location Old Name 
Filler F59 seq.#1, start 4, end 5, length 02 Sequence Number 
 
Change Requirements for Existing Fields 
Field Name  Record Type, Location, Current 
Requirements 
Changed requirements 
Closing 
Book/Physical 
Balance 
F58 seq. #1, start 25, end 37, length 13; 
999,999,999.9999; Required. 
Optional Conditional. Required if Closing Book/Physical 
Balance – Extended is NOT provided in record F58 
sequence #2. Otherwise, it is not allowed. 
Total Closing 
Book Share 
Balance 
F59 seq. #1, start 10, end 24, length 15; 
99,999,999,999.9999; Required. 
Optional Conditional. Required to recap Closing 
Book/Physical Balance in Detail records F58 sequence 
#1, when Share Balance Indicator = 1 (Book [[shares]]). 
Otherwise, it is optional. 
Total Closing 
Physical Share 
Balance 
F59 seq.#1, start 57, end 71, length 15, 
99,999,999,999.9999; Optional 
Optional Conditional. Required to recap Closing 
Book/Physical Balance in Detail records F58 sequence 
#1, when Share Balance Indicator = 2 
(Physical [[shares]]). Otherwise, it is optional. 

---

## Page 24

Position Reporting Record Layouts 
Summary of changes – effective Q4, 2008 24 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2008 
Renamed Field 
The following field has been renamed: 
New Name  Record Type and Location Old Name 
TPA/Investment Agent Number 57, start 31, end 34, length 4 
59, start 53, end 56, length 4 
TPA Number 

---

## Page 25

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of 
The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 17, 2023 
Publication Code: MFS334 
Service: Networking 
Title: Position Reporting Record Layouts  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 