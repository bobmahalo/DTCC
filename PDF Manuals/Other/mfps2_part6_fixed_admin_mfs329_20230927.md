---
title: "MFPS II - Administrative Fixed Length Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part6_fixed_admin_mfs329_20230927.pdf"
pages: 13
size: "389.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II - Administrative Fixed Length Record Layouts

**Original File:** [mfps2_part6_fixed_admin_mfs329_20230927.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps2_part6_fixed_admin_mfs329_20230927.pdf)  
**Category:** Other  
**Total Pages:** 13  
**File Size:** 389.6 KB  

---

## Page 1

 
 
 
Mutual Fund Profile Service II 
ADMINISTRATIVE FIXED LENGTH RECORD LAYOUTS 
 
SEPTEMBER 27, 2023 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 2

Administrative Fixed Length Record Layouts 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ................................................................................................................. 3 
Record Type 080 – User File Request .................................................................................................. 4 
02.22.01 User File Request (080) ...................................................................................................... 4 
[[NSCC]] Output Header (000) .................................................................................................................... 6 
02.23.01 [[NSCC]] Output Header (000) Record 1 of 1 .......................................................................... 6 
Trailer (999) ............................................................................................................................................. 7 
02.24.01 Trailer (999) Record 1 of 1 .................................................................................................. 7 
Datatrak Header ...................................................................................................................................... 8 
02.25.01 Datatrak Header Record 1 of 1 ............................................................................................ 8 
Datatrak Trailer ....................................................................................................................................... 9 
02.26.01 Datatrak Trailer Record 1 of 1 ............................................................................................. 9 
Multiple REject Codes (120) ................................................................................................................ 10 
02.27.01 Multiple Reject Codes (120) Record 1 of 2 ........................................................................ 10 
02.27.02 Multiple Reject Codes (120) Record 2 of 2 ........................................................................ 12 
 
 

---

## Page 3

Administrative Fixed Length Record Layouts 
History of Important Notices 3 
HISTORY OF IMPORTANT NOTICES 
Effective Date Important Notice 
September 27, 2023 Record has been rebranded and reviewed.  
Effective Date: May 1, 2023 MFPSII [[participant]]  Profile database was decommissioned. Please See 
Important Notice a9279 P&S 8852 
Dated March 21, 2023. 
 
The User File Request (080) and Multiple Reject Codes (120) records were updated 
accordingly. 
March 25, 2019 Please see Important Notice: a8658 P&S 8233 Dated December  
19, 2018 
March 27, 2006 Please see Important Notice: a6171 P&S 5741 Dated December  
21, 2005 
November 14, 2005 Please see Important Notice: a6084 P&S 5654 Dated August 10, 
2005 
August 29, 2005 Please see Important Notice a6062 P&S 5632 Dated July 6, 2005 

---

## Page 4

Administrative Fixed Length Record Layouts 
Record Type 080 – User File Request 4 
RECORD TYPE 080 – USER FILE REQUEST 
02.22.01 User File Request (080)  
Required 
Input to [[NSCC]]. User Request sent to [[NSCC]] for  MFPS data f iles to be sent back to the requester. 
Record 1 of 1 
Field Name 
 
Start 
 
End 
 
Len 
 
Type 
 
Description 
Opt/ 
Req 
Reject 
Code 
Physical Sequence Number 1 2 2 A/N   R 0080 
Logical Sequence Number 3 4 2 A/N 01  R 0080 
Filler 5 6 2 A/N Space  R  
Originator Type Indicator 
(Requestor of the 
Information) 
7 7 1 A/N Input: 
F = Fund  
B = Firm  
T = TPA 
 
Output: 
N = [[NSCC]] 
 R 0081 
Requested Profile Type 8 9 2 A/N 00 = All types 
03 = Distribution Declaration 
06 = Security Issue  
FS = FUND/SERV Security Issue 
 R 0082 
Record Type 10 12 3 A/N 080 = User File Request Record  R 0083 
Filler 13 13 1 A/N Space  R  
Submitting 
[[participant]] Number 
14 17 4 A/N @  R 0100 
Filler 18 18 1 A/N Space  R  
Requested 
[[participant]] Number 
19 22 4 A/N Firm or Fund number 
Mutually exclusive with “Security Issue [[ID]]” 
(Only one of them could be filled  or 
neither) 
 O 0340 
Filler 23 28 6 A/N Space  R  
Submission Date 29 36 8 A/N ccyymmdd  R 0036 
 

---

## Page 5

Administrative Fixed Length Record Layouts 
Record Type 080 – User File Request 5 
Record 1 of 1 
Field Name 
 
Start 
 
End 
 
Len 
 
Type 
 
Description 
Opt/ 
Req 
Reject 
Code 
Requested [[participant]] 
Type 
37 37 1 A/N ‘F’ = Fund (*) 
‘B’ = Firm 
‘T’ = TPA 
O 0231 
Requested Data Level 38 38 1 A/N For Future Use 
Space 
R  
Filler 39 43 5 A/N Space R  
Security Issue Country 
Code 
44 45 2 A/N See ISO Country Codes O 0153 
Security Issue [[ID]] 46 54 9 A/N Mutually exclusive  with “Requested 
[[participant]] 
Number” (Only one of them could be Filled 
or neither) 
O 0040 
ISIN Security Issue 
Check Digit 
55 55 1 A/N  O 0041 
Requested “From” 
Payable Date 
56 63 8 A/N Distribution Declaration only O 0352 
Requested “To” 
Payable Date 
64 71 8 A/N Distribution Declaration only O 0353 
Filler 72 74 3 A/N Space R  
Test Indicator 75 75 1 A/N Space = Production 
1 = Test 
R 0089 
[[NSCC]] Rejection 
Indicator 
76 76 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], 
Multiple Errors 
3 = Warning message 
R  
[[NSCC]] Reject Code 1 77 80 4 A/N Input: Space 
Output: Reject code, warning code, or space 
R  

---

## Page 6

Administrative Fixed Length Record Layouts 
[[NSCC]] Output Header (000) 6 
[[NSCC]] OUTPUT HEADER (000)  
02.23.01 [[NSCC]] Output Header (000) Record 1 of 1 
Output from [[NSCC]]. 
 
Record 1 of 1  
Field Name 
Start End Len Type Description 
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Filler 5 6 2 A/N Space 
Originator Type 7 7 1 A/N N = [[NSCC]] 
Filler 8 9 2 A/N Space 
Record Type 10 12 3 A/N 000 = [[NSCC]] Output Header 
Recipient Number 13 16 4 N Zero if  global record, [[participant]] no. if  specific 
record 
Transmission Date 17 24 8 N ccyymmdd 
Filler 25 25 1 A/N Space 
Literal 26 29 4 A/N FILE 
AutoRoute File Number 30 37 8 A/N  
AutoRoute File Cycle 38 39 2 A/N  
File Description 40 59 20 A/N MUTUAL FUND PROFILE 
Filler 60 80 21 A/N Space 

---

## Page 7

Administrative Fixed Length Record Layouts 
Trailer (999) 7 
TRAILER (999) 
02.24.01 Trailer (999) Record 1 of 1 
Required 
Input/Output 
Record 1 of 1  
Field Name 
Start End Len Type Description Opt/ 
Req 
Physical Sequence 
Number 
1 2 2 A/N  R 
Logical Sequence 
Number 
3 4 2 A/N 01 R 
Filler 5 6 2 A/N Space R 
Originator Type 7 7 1 A/N B = Firm  
F = Fund 
N = [[NSCC]] 
T = TPA 
R 
Filler 8 9 2 A/N Space R 
Record Type 10 12 3 A/N 999 = Trailer R 
Recipient Number 13 16 4 N Zero if global record; Receiving [[participant]], 
if specific record. 
R 
Submission Date 17 24 8 N ccyymmdd R 
Total Price/Rate 
Transactions 
25 31 7 N 9,999,999 R 
Total [[participant]] 
Transactions 
32 38 7 N 9,999,999 R 
Total Security 
Transactions 
39 45 7 N 9,999,999 R 
Total Distribution 
Declaration 
Transactions 
46 52 7 N 9,999,999 R 
Filler 53 73 21 A/N Space R 
Total Other Transactions 74 80 7 N 9,999,999 R 

---

## Page 8

Administrative Fixed Length Record Layouts 
Datatrak Header 8 
DATATRAK HEADER 
02.25.01 Datatrak Header Record 1 of 1 
Required 
Input to [[NSCC]] 
This is the first record in any file submitted to MFPS through Datatrak. 
 
Record 1 of 1  
Field Name 
Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N HDR.S R 
File [[ID]] 6 10 5 A/N  R 
Literal 11 16 6 A/N .E00.C R 
Originator [[ID]] 17 20 4 A/N  R 
Literal 21 22 2 A/N .S R 
Sub Originator [[ID]] 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N MUTUAL FUND PROFILE R 
Multibatch Last Batch 
Indicator 
60 60 1 A/N N = Not last batch Y 
= Last batch 
R 
Multibatch Batch 
Counter 
61 63 3 N  R 
Filler 64 80 17 A/N Space R 

---

## Page 9

Administrative Fixed Length Record Layouts 
Datatrak Trailer 9 
DATATRAK TRAILER 
02.26.01 Datatrak Trailer Record 1 of 1 
Required 
Input to [[NSCC]] 
This is the last record in any file submitted to MFPS through Datatrak. 
 
Record 1 of 1  
Field Name 
Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N END.S R 
File [[ID]] 6 10 5 A/N  R 
Literal 11 16 6 A/N .E00.C R 
Originator [[ID]] 17 20 4 A/N  R 
Literal 21 22 2 A/N .S R 
Sub Originator [[ID]] 23 26 4 A/N  R 
Total Records 27 33 7 N 9,999,999 
Total # of records in file excluding Datatrak 
header and trailer 
R 
Filler 34 80 47 A/N Space R 

---

## Page 10

Administrative Fixed Length Record Layouts 
Multiple REject Codes (120) 10 
MULTIPLE REJECT CODES (120) 
02.27.01 Multiple Reject Codes (120) Record 1 of 2 
Output from [[NSCC]] 
This record will be created by [[NSCC]] for each rejected transaction that has been rejected for more than one 
reason. 
Record 1 of 2  
Field Name 
Start End Len Type Description 
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Filler 5 6 2 A/N Space 
Originator Type Indicator 7 7 1 A/N ‘N’ = [[NSCC]] 
Profile Type 8 9 2 A/N 03 = Distribution Declaration 06 
= Security Issue 
Record Type 10 12 3 A/N 120 = Multiple Reject Codes 
Filler 13 13 1 A/N Space 
Submitting [[participant]] 
Number 
14 17 4 A/N  
Filler 18 18 1 A/N Space 
Recipient Number 19 22 4 A/N  
Filler 23 28 6 A/N Space 
Submission Date 29 36 8 N ccyymmdd 
Filler 37 45 9 A/N Space 
Security Issue Country 
Code 
46 47 2 A/N  
Security Issue [[ID]] 48 56 9 A/N  

---

## Page 11

Administrative Fixed Length Record Layouts 
Multiple REject Codes (120) 11 
Record 1 of 2  
Field Name 
Start End Len Type Description 
ISIN Security  Issue Check 
Digit 
57 57 1 A/N  
Original Record Type 58 60 3 A/N The rejected transaction record type 
Filler 61 80 20 A/N Space 

---

## Page 12

Administrative Fixed Length Record Layouts 
Multiple REject Codes (120) 12 
02.27.02 Multiple Reject Codes (120) Record 2 of 2 
Record 2 of 2  
Field Name 
Start End Len Type Description 
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 02 
Filler 5 6 2 A/N Space 
[[NSCC]] Reject Code 2 7 10 4 A/N  
[[NSCC]] Reject Code 3 11 14 4 A/N  
[[NSCC]] Reject Code 4 15 18 4 A/N  
[[NSCC]] Reject Code 5 19 22 4 A/N  
[[NSCC]] Reject Code 6 23 26 4 A/N  
[[NSCC]] Reject Code 7 27 30 4 A/N  
[[NSCC]] Reject Code 8 31 34 4 A/N  
Filler 35 80 46 A/N Space 

---

## Page 13

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The Depository 
Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal entity, 
subject to the laws and regulations of the particular country or countries in which such entity operates. Please see www.[[DTCC]].com 
for more information on [[DTCC]], its affiliates and the services they offer.    
 
Doc Date: September 27, 2023  
Publication Code: MFS329  
Service: Mutual Fund Profile Service II  
Title: Administrative Fixed Length Record Layouts 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 