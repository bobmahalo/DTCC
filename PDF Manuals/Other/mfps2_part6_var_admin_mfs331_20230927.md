---
title: "MFPS II - Administrative Variable Length Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part6_var_admin_mfs331_20230927.pdf"
pages: 12
size: "368.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II - Administrative Variable Length Record Layouts

**Original File:** [mfps2_part6_var_admin_mfs331_20230927.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part6_var_admin_mfs331_20230927.pdf)  
**Category:** Other  
**Total Pages:** 12  
**File Size:** 368.2 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
ADMINISTRATIVE VARIABLE LENGTH RECORD 
LAYOUTS 
September 27, 2023 

---

## Page 2

Administrative Variable Length Record Layouts 
Record Type 080 – User File Request 2 
TABLE OF CONTENTS 
Record Type 080 – User File Request ................................................................................................................ 4 
02.22 User File Request (080) ............................................................................................................................ 4 
[[NSCC]] Output Header (000) .................................................................................................................................. 6 
02.23 [[NSCC]] Output Header (000) ...................................................................................................................... 6 
Trailer (999) ........................................................................................................................................................... 7 
02.24 Trailer (999) .............................................................................................................................................. 7 
Datatrak Header .................................................................................................................................................... 8 
02.25 Datatrak Header ....................................................................................................................................... 8 
Datatrak Trailer ..................................................................................................................................................... 9 
02.26 Datatrak Trailer ......................................................................................................................................... 9 
Multiple Reject Codes (120) .............................................................................................................................. 10 
02.27 Multiple Reject Codes (120) ...................................................................................................................10 
 

---

## Page 3

Administrative Variable Length Record Layouts 
Record Type 080 – User File Request 3 
HISTORY OF IMPORTANT NOTICES 
Effective Date Important Notice 
September 27, 2023 Record rebranded and reviewed.  
Effective Date: May 1, 2023 MFPSII [[participant]] Profile database was decommissioned.  
Please See Important Notice a9279 P&S 8852, Dated March 21, 2023 
 
The User File Request (080) and Multiple Reject Codes (120) records were updated 
accordingly. 
March 25, 2019 Please see Important Notice: a8658 P&S 8233 
Dated December 19, 2018 
March 27, 2006 Please see Important Notice: a6171 P&S 5741  
Dated December 21, 2005 
November 14, 2005 Please see Important Notice: a6084 P&S 5654  
Dated August 10, 2005 
August 29, 2005 Please see Important Notice a6062 P&S#5632 
Dated July 6, 2005 

---

## Page 4

Administrative Variable Length Record Layouts 
Record Type 080 – User File Request 4 
RECORD TYPE 080 – USER FILE REQUEST  
02.22 User File Request (080) 
Input to [[NSCC]] 
(User Request sent to [[NSCC]] for MFPS data files to be sent back to the requester.)  
Start of Record Type 080 – User File Request 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0084 R 0088 
Physical Sequence 
 Number 
5 6 2 A/N  R 0080 
Logical Sequence 
Number 
7 8 2 A/N 01 R 0080 
Filler 9 10 2 A/N Space R  
Originator Type 
Indicator 
(Requestor of the 
Information) 
11 11 1 A/N Input: 
   F = Fund 
   B = Firm 
   T = TPA 
Output: 
   N = [[NSCC]] 
R 0081 
Requested Profile 
Type 
12 13 2 A/N 00 = All types 
03 = Distribution Declaration 
06 = Security Issue 
FS = FUND/SERV Security Issue  
R 0082 
Record Type 14 16 3 A/N 080 = User File Request Record R 0083 
Filler 17 17 1 A/N Space R  
Submitting 
[[participant]] 
Number 
18 21 4 A/N @ R 0100 
Filler 22 22 1 A/N Space R  
Requested 
[[participant]] 
Number 
23 26 4 A/N Firm or Fund number 
 
Mutually exclusive with “Security Issue [[ID]]” 
(Only one of them could be filled or neither) 
O 0340 
Filler 27 32 6 A/N Space R  
Submission Date 33 40 8 A/N ccyymmdd R 0036 
Requested 
[[participant]] Type 
41 41 1 A/N ‘F’ = Fund (*) 
‘B’ = Firm 
‘T’ = TPA 
O 0231 

---

## Page 5

Administrative Variable Length Record Layouts 
Record Type 080 – User File Request 5 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Requested Data 
Level  
42 42 1 A/N For Future Use 
 
Space 
R 0650 
Filler 43 47 5 A/N Space  R  
Security Issue 
Country Code 
48 49 2 A/N See ISO Country Codes O 0153 
Security Issue [[ID]] 50 58 9 A/N Mutually exclusive with “Requested [[participant]] 
Number” (Only one of them could be filled or 
neither) 
O 0040 
ISIN Security Issue 
Check Digit 
59 59 1 A/N  O 0041 
Requested “From” 
 Payable Date 
60 67 8 A/N Distribution Declaration only O 0352 
Requested “To” 
 Payable Date 
68 75 8 A/N Distribution Declaration only O 0353 
Filler 76 78 3 A/N Space R  
Test Indicator 79 79 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection  
Indicator 
80 80 1 A/N Input: Space 
Output: 
    0 = Accepted by [[NSCC]] 
    1 = Rejected by [[NSCC]]  
    2 = Rejected by [[NSCC]],  
          Multiple Errors  
    3 = Warning Message   
R  [[NSCC]] Reject Code 1 81 84 4 A/N Input: Space  
Output: Reject code, warning code, or space  
R  
 

---

## Page 6

Administrative Variable Length Record Layouts 
[[NSCC]] Output Header (000) 6 
[[NSCC]] OUTPUT HEADER (000) 
02.23 [[NSCC]] Output Header (000) 
Output from [[NSCC]] 
Field Name Start End Len Type Description 
Record Length 1 4 4 N 0084 
Physical Sequence Number 5 6 2 A/N  
Logical Sequence Number 7 8 2 A/N 01 
Filler 9 10 2 A/N Space 
Originator Type 11 11 1 A/N  
N = [[NSCC]] Filler 12 13 2 A/N Space 
Record Type 14 16 3 A/N 000 = [[NSCC]] Output Header 
Recipient Number 17 20 4 N Zero if global record, [[participant]] no. if specific 
record 
Transmission Date 21 28 8 N ccyymmdd 
Filler 29 29 1 A/N Space 
Literal 30 33 4 A/N File 
AutoRoute File Number 34 41 8 A/N  
AutoRoute File Cycle 42 43 2 A/N  
File Description 44 63 20 A/N Mutual Fund Profile 
Filler 64 84 21 A/N Space 

---

## Page 7

Administrative Variable Length Record Layouts 
Trailer (999) 7 
TRAILER (999) 
02.24 Trailer (999) 
Required 
Input/Output 
Field Name Start End Len Type Description 
Record Length 1 4 4 N 0084 
Physical Sequence Number 5 6 2 A/N  
Logical Sequence Number 7 8 2 A/N 01 
Filler 9 10 2 A/N Space 
Originator Type 11 11 1 A/N B = Firm  
F = Fund  
N = [[NSCC]] 
T = TPA 
Filler 12 13 2 A/N Space 
Record Type 14 16 3 A/N 999 = Trailer 
Recipient Number 17 20 4 N Zero if global record; 
Receiving [[participant]] if specific record. 
Submission Date 21 28 8 N ccyymmdd 
Total Price/Rate 
Transactions 
29 35 7 N 9,999,999 
Total [[participant]] 
Transactions 
36 42 7 N 9,999,999 
Total Security Transactions 43 49 7 N 9,999,999 
Total Distribution 
Declaration Transactions 
50 56 7 N 9,999,999 
Filler 57 77 21 A/N Space 
Total Other Transactions 78 84 7 N 9,999,999 

---

## Page 8

Administrative Variable Length Record Layouts 
Datatrak Header 8 
DATATRAK HEADER 
02.25 Datatrak Header 
Required 
Input to [[NSCC]] 
(This is the first record in any file submitted to MFPS through DataTrak.) 
Field Name Start End Len Type Description 
Literal 1 5 5 A/N HDR.S 
File [[ID]] 6 10 5 A/N  
Literal 11 16 6 A/N .E00.C 
Originator [[ID]] 17 20 4 A/N  
Literal 21 22 2 A/N .S 
Sub Originator [[ID]] 23 26 4 A/N  
Processing Date 27 34 8 N mmddccyy 
File Description 35 59 25 A/N Mutual Fund Profile 
Multibatch Last  
Batch Indicator 
60 60 1 A/N N = Not last batch  
Y = Last batch 
Multibatch Batch Counter 61 63 3 N  
Filler 64 80 17 A/N Space 

---

## Page 9

Administrative Variable Length Record Layouts 
Datatrak Trailer 9 
DATATRAK TRAILER 
02.26 Datatrak Trailer 
Required  
Input to [[NSCC]] 
(This is the last record in any file submitted to MFPS through DataTrak.) 
Field Name Start End Len Type Description 
Literal 1 5 5 A/N END.S 
File [[ID]] 6 10 5 A/N  
Literal 11 16 6 A/N .E00.C 
Originator [[ID]] 17 20 4 A/N  
Literal 21 22 2 A/N .S 
Sub Originator [[ID]] 23 26 4 A/N  
Total Records 27 33 7 N 9,999,999 
Total # of records in file excluding DataTrak 
header and trailer 
Filler 34 80 47 A/N Space 

---

## Page 10

Administrative Variable Length Record Layouts 
Multiple Reject Codes (120) 10 
MULTIPLE REJECT CODES (120) 
02.27 Multiple Reject Codes (120) 
Output from [[NSCC]] 
(This record will be created by [[NSCC]] for each rejected transaction that has been rejected for more than one 
reason.) 
Field Name Start End Len Type Description 
Record Length 1 4 4 N 0158 
Physical Sequence Number 5 6 2 A/N  
Logical Sequence Number 7 8 2 A/N 01 
Filler 9 10 2 A/N Space 
Originator Type Indicator 11 11 1 A/N ‘N’ = [[NSCC]] 
Profile Type 12 13 2 A/N 03 = Distribution Declaration  
06 = Security Issue 
Record Type 14 16 3 A/N 120 = Multiple Reject Codes 
Filler 17 17 1 A/N Space 
Submitting [[participant]] 
Number 
18 21 4 A/N  
Filler 22 22 1 A/N Space 
Recipient Number 23 26 4 A/N  
Filler 27 32 6 A/N Space 
Submission Date 33 40 8 N ccyymmdd 
Filler 41 49 9 A/N Space 
Security Issue Country 
Code 
50 51 2 A/N  
Security Issue [[ID]] 52 60 9 A/N  
ISIN Security Issue Check 
Digit 
61 61 1 A/N  
Original Record Type 62 64 3 A/N The rejected transaction record type 
Filler 65 84 20 A/N Space 
[[NSCC]] Reject Code 2 85 88 4 A/N  
[[NSCC]] Reject Code 3 89 92 4 A/N  

---

## Page 11

Administrative Variable Length Record Layouts 
Multiple Reject Codes (120) 11 
Field Name Start End Len Type Description 
[[NSCC]] Reject Code 4 93 96 4 A/N  
[[NSCC]] Reject Code 5 97 100 4 A/N  
[[NSCC]] Reject Code 6 101 104 4 A/N  
[[NSCC]] Reject Code 7 105 108 4 A/N  
[[NSCC]] Reject Code 8 109 112 4 A/N  
Filler 113 158 46 A/N Space 

---

## Page 12

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 27, 2023 
Publication Code: MFS331 
Service: Mutual Fund Profile Service II 
Title: Administrative Variable Length Record Layouts 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
  