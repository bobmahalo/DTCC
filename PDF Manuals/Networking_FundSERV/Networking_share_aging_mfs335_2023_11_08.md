---
title: "Networking Share Aging Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Networking_share_aging_mfs335_2023_11_08.pdf"
pages: 23
size: "411.7 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Networking Share Aging Record Layouts

**Original File:** [Networking_share_aging_mfs335_2023_11_08.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Networking_share_aging_mfs335_2023_11_08.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 23  
**File Size:** 411.7 KB  

---

## Page 1

  
 
 
Networking 
SHARE AGING RECORD LAYOUTS 
NOVEMBER 8, 2023 
 

---

## Page 2

Share Aging Record Layouts 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 3 
Record Layouts .................................................................................................................................................... 4 
Share Aging Header (B/F75) ................................................................................................................................ 6 
Record 1 of 3 ...................................................................................................................................................... 6 
Record 2 of 3 ...................................................................................................................................................... 8 
Record 3 of 3 ...................................................................................................................................................... 9 
Share Aging Detail (B/F76) ................................................................................................................................ 10 
Record 1 of 2 ....................................................................................................................................................10 
Record 2 of 2 ....................................................................................................................................................12 
Share Aging Trailer (B/F77) ............................................................................................................................... 13 
Record 1 of 1 ....................................................................................................................................................13 
Share Aging Grand Total Trailer (B/F78) ......................................................................................................... 15 
Record 1 of 1 ....................................................................................................................................................15 
Share Aging Output Header (N00) .................................................................................................................... 16 
Record 1 of 1 ....................................................................................................................................................16 
APPENDIX – Summary of Changes .................................................................................................................. 17 
Summary of changes – modification Q3, 2021 ............................................................................................... 18 
Summary of changes – effective Q1, 2019 ...................................................................................................... 19 
Reject Codes ....................................................................................................................................................19 
Summary of changes – effective Q4, 2017 ...................................................................................................... 20 
Added New Value to Existing Field ...................................................................................................................20 
Renamed Existing Field ....................................................................................................................................20 
Summary of changes – effective Q4, 2011 ...................................................................................................... 21 
Added New Field...............................................................................................................................................21 
Summary of changes – effective Q2, 2011 ...................................................................................................... 22 
Requirements Changed For Existing Field .......................................................................................................22 
 

---

## Page 3

Share Aging Record Layouts 
History of Important Notices 3 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notices 
November 8, 2023  Document rebranded and reviewed.  
May 17, 2023 Document rebranded and reviewed. 
August 17, 2021 B/F78 (Share Aging Grand Total Trailer record) – Record Requirement Clarification 
added 
March 25, 2019 Important Notices  
a8658 P&S 8233 Dated December 19, 2018 
November 20, 2017 Important Notices  
a8402 P&S 7977 Dated June 1, 2017 
October 17, 2011 Important Notices  
  a7241 P&S 6811 Dated July 8, 2011 
June 13, 2011 Important Notices  
a7175 P&S 6745 Dated March 7th, 2011 
November 20, 2008 Important Notices  
a6842 P&S 6212 Dated June 25, 2008. 
April 10, 2006 Important Notices  
a6173 P&S 5743 Dated December 22, 2005,  
a6195 P&S 5765 Dated February 1, 2006 (Revision)  
a6203 P&S 5773 Dated February 1, 2006 (Additional Modification) 

---

## Page 4

Share Aging Record Layouts 
Record Layouts 4 
RECORD LAYOUTS 
The following are Networking Share Aging Record Layouts. The column headings are as follows: 
Start - The position where the field starts. 
End - The position where the field ends. 
Len - The length of the field in bytes 
Type - The type of the field: 
A/N = Alphanumeric  
N = Numeric 
Field Name - The name of the field. 
Description - Field description (format, valid values, conditional requirements, etc.). 
Opt/Req - Indicates whether the field is optional or required:  
O = Optional 
R = Required 
OC = Generally optional, but required upon specified conditions  
RC = Generally required, but optional upon specified conditions 
Reject Code - The reject code which indicates that this field is invalid. 
Notes: 
• Alphanumeric type fields may include any character in the computer character set, but should not include unprintable 
characters such as Low-Value, High-Value, Comp-3 fields, etc., since these kind of characters may cause problems 
during transmission time. 
• Numeric type fields may include digits (0-9) only. 
• Required fields mean the following: 
a. Fields with specified list of values must have one of those values. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above 
but must not be spaces. 
c. Numeric type fields without a specified list of values must be numeric greater than zero. 
d. Fields with other requirements must follow these requirements (for example Firm Number must be valid and 
eligible for Fund/SERV). 
• Optional fields mean the following: 
a. Fields with specified list of values must have one of those values or space. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above. 
c. Numeric type fields without specified list of values must be numeric or space. 
d. Fields with other requirements must follow these requirements or may be space (for example Fund Number must 
be valid and eligible for Fund/SERV or may be space) 
• All dates in the layouts have the format mmddccyy (except where otherwise indicated) where:  
mm = Month 
dd = Day in month  
cc = Century 

---

## Page 5

Share Aging Record Layouts 
Record Layouts 5 
yy = Year in century 
Example: 
June 15, 2023 is represented as: 06152023 
September 3, 2022 is represented as: 09032022 

---

## Page 6

Share Aging Record Layouts 
Share Aging Header (B/F75) 6 
SHARE AGING HEADER (B/F75) 
Record 1 of 3 
Required 
The Share Aging header record is used to introduce a series of Share Aging detail records for a delivering firm, 
receiving firm and security issue. 
Share Aging Header (B/F75) Record 1 of 3 
Record 1 of 3 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
System Code 
(Originator Type) 
1 1 1 A/N B = Delivering Firm  
F = Fund 
R 01 
Record Type 2 3 2 A/N 75 = Share Aging Header R 02 
Sequence Number 4 5 2 A/N 01 R 37 
Delivering Firm 
Number 
6 9 4 A/N Required if System Code = B OC 03 
Receiving Firm 
Number 
10 13 4 A/N Required if System Code = F OC 03 
Fund Number 14 17 4 A/N Required if System Code = F OC 04 
Security Issue Country 
Code 
18 19 2 A/N Space. For future use R  
Security Issue [[ID]] 20 28 9 A/N  R 05 
Security Issue Check 
Digit 
29 29 1 A/N Space. For future use R  
Processing Date 30 37 8 A/N mmddccyy R 54 
Customer SSN/EIN 
Number Indicator 
 
38 38 1 A/N 0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN  
R 64 
Customer SSN/EIN 
Number 
39 47 9 A/N  R 65 
Membership 
Identifier (Delivering 
Firm) 
48 49 2 A/N 01 = Trust [[Member]] O F9 
Membership  
Identifier (Receiving 
Firm) 
50 51 2 A/N 01 = Trust [[Member]] O F9 

---

## Page 7

Share Aging Record Layouts 
Share Aging Header (B/F75) 7 
Record 1 of 3 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Social Code 52 53 2 A/N  R 68 
Filler 54 91 38 A/N Space R  
[[NSCC]] Reject Indicator 92 92 1 A/N Input: Space Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]], caused the 
rejection of whole group of details 
2 = Created by [[NSCC]] to lead a subgroup 
of rejected details 
R  
[[NSCC]] Reject Code 1 93 94 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 95 96 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 97 98 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 4 99 100 2 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 8

Share Aging Record Layouts 
Share Aging Header (B/F75) 8 
Record 2 of 3 
Required 
Share Aging Header (B/F75) Record 2 of 3 
Record 2 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
System Code 
(Originator Type) 
1 1 1 A/N B = Delivering Firm  
F = Fund 
R 01 
Record Type 2 3 2 A/N 75 = Share Aging Header R 02 
Sequence Number 4 5 2 A/N 02 R 37 
Customer Account 
Number at Delivering 
Firm 
6 25 20 A/N  R 61 
Control/Reference 
Number 
26 45 20 A/N  R 59 
Control/Reference 
Number Indicator 
46 46 1 A/N 1 = Fund/SERV control number (should 
be used if requested through ACATS) 
2 = Networking transfer (B52) control 
number (should be used if requested 
through Networking) 
3 = Manual reference number 
R M9 
ACATS Control Number 47 66 20 A/N Should be used if requested through 
ACATS 
O  
Filler 67 100 34 A/N Space R  
 
 
  

---

## Page 9

Share Aging Record Layouts 
Share Aging Header (B/F75) 9 
Record 3 of 3 
Optional 
Share Aging Header (B/F75) Record 3 of 3 
Record 3 of 3 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
System Code 
(Originator Type) 
1 1 1 A/N B = Delivering Firm  
F = Fund 
R 01 
Record Type 2 3 2 A/N 75 = Share Aging Header R 02 
Sequence Number 4 5 2 A/N 03 R 37 
Customer Account 
Number at Receiving 
Firm 
6 25 20 A/N  O  
Customer Account 
Number at Fund 
(delivering firm) 
26 45 20 A/N  O  
Customer Account 
Number at Fund 
(receiving firm) 
46 65 20 A/N  O  
Filler 66 100 35 A/N Space R  

---

## Page 10

Share Aging Record Layouts 
Share Aging Detail (B/F76) 10 
SHARE AGING DETAIL (B/F76) 
Record 1 of 2 
Required 
Share Aging Detail (B/F76) Record 1 of 2 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
System Code 
(Originator Type) 
1 1 1 A/N B = Delivering Firm  
F = Fund 
R 01 
Record Type 2 3 2 A/N 76 = Share Aging Detail R 02 
Sequence Number 4 5 2 A/N 01 R 37 
Submitting [[participant]] 
number 
6 9 4 A/N  R 03, 04 
Share Quantity 10 22 13 N 999,999,999.9999 R 95 
Price per Share 23 34 12 N 999,999.999999 
Required if Dollar Amount is not provided 
and Transaction Code is not = 08 
OC 47 
Dollar Amount 35 50 16 N 99,999,999,999,999.99 
Required if Price per Share is not 
provided and Transaction Code is not = 
08 
OC D8 
Currency Indicator 51 53 3 A/N USD = U.S.A. dollars O G1 
Trade Date 54 61 8 A/N mmddccyy 
Optional if Transaction Code = 08 
RC C3 
Transaction Code 62 63 2 A/N 01 = Purchase 
02 = Redemption 
03 = [[Dividend]] Reinvest 
04 = Capital Gain Reinvest  
05 = Free side Load [[shares]] 
06 = Cross (exchange) Reinvest  
07 = Exchange 
08 = Share Trade Date and Price 
Unknown 
R 96 
Exchange/Cross 
Security Issue 
Country Code 
64 65 2 A/N Space. For future use R  

---

## Page 11

Share Aging Record Layouts 
Share Aging Detail (B/F76) 11 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Exchange/Cross 
Security Issue [[ID]] 
66 74 9 A/N Required if Transaction Code indicates 
Exchange or Cross (exchange) Reinvest 
OC 49 
Exchange/Cross 
Security Issue Check 
Digit 
75 75 1 A/N Space. For future use R  
[[default]] Lot Indicator 76 76 1 A/N 0 = No 
1 = Yes 
R I3 
12b-1 Indicator 77 77 1 A/N 0 = Pre-Agreement [[shares]]  
1 = Eligible [[shares]] 
2 = [[shares]] Ineligible/Not Fully Aged 
3 = [[shares]] Ineligible Due to Other 
Required if Transaction Code = 08. 
OC I4 12b-1 Lot Date 78 85 8 A/N mmddccyy 
Required if 12b-1 Indicator = 0 or 2. 
OC I5 
Filler 86 91 6 A/N Space R  
[[NSCC]] Reject 
indicator 
92 92 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
2 = Whole group rejected by [[NSCC]] 
because of a bad header or trailer 
R  
[[NSCC]] Reject Code 1 93 94 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 95 96 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 97 98 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 4 99 100 2 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 12

Share Aging Record Layouts 
Share Aging Detail (B/F76) 12 
Record 2 of 2 
Required 
Share Aging Detail (B/F76) Record 2 of 2 
Record 2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
System Code 
(Originator Type) 
1 1 1 A/N B = Delivering Firm  
F = Fund 
R 01 
Record Type 2 3 2 A/N 76 = Share Aging Detail R 02 
Sequence Number 4 5 2 A/N 02 R 37 
Chargeable Security 
Issue Country Code 
6 7 2 A/N Space. For future use R  
Chargeable Security 
Issue [[ID]] 
8 16 9 A/N  O  
Chargeable Security 
Issue Check Digit 
17 17 1 A/N Space. For future use R  
[[settlement]] Date 18 25 8 A/N mmddccyy O G7 
Memo 26 45 20 A/N  O  
Short Term 
Redemption Lot 
Date 
46 53 8 A/N mmddccyy O I6 
Jumbo Transaction 
Indicator 
54 54 1 A/N 0 = No 
1 = Yes 
O I7 
Commissionable 
Share Indicator 
55 55 1 A/N 0 = Non-commissionable  
1 = Commissionable 
R I8 
Filler 56 100 45 A/N Space R  

---

## Page 13

Share Aging Record Layouts 
Share Aging Trailer (B/F77) 13 
SHARE AGING TRAILER (B/F77) 
Record 1 of 1 
Required 
The Share Aging trailer record is used to recap the detail records for a particular delivering firm, receiving firm 
and security issue. 
Share Aging Trailer (B/F77) Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/Req Reject 
Code 
System Code (Originator 
Type) 
1 1 1 A/N B = Delivering Firm  
F = Fund 
R 01 
Record Type 2 3 2 A/N 77 = Share Aging Trailer R 02 
Sequence Number 4 5 2 A/N 01 R 37 
Delivering Firm Number 6 9 4 A/N Required if System Code = B OC 03 
Receiving Firm Number 10 13 4 A/N Required if System Code = F OC 03 
Fund Number 14 17 4 A/N  O 04 
Total Share Quantity 18 32 15 N 99,999,999,999.9999 R 95 
Total Dollar Amount 33 49 17 N 999,999,999,999,999.99 R D8 
Total Detail Items 50 57 8 N 99,999,999 
(Total number of record type 76 with 
sequence number 01). 
R G8 
Total Records 58 65 8 N 99,999,999 
(Total number of records including 
header and trailer). 
R G8 
Filler 66 91 26 A/N Space R  
[[NSCC]] Reject Indicator 92 92 1 A/N Input: Space Output: 
0 = Created by [[NSCC]] to recap an 
accepted group of details 
1 = Rejected by [[NSCC]], caused the 
rejection of whole group of details 
2 = Created by [[NSCC]] to recap a 
subgroup of rejected details 
R  
[[NSCC]] Reject Code 1 93 94 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 14

Share Aging Record Layouts 
Share Aging Trailer (B/F77) 14 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/Req Reject 
Code 
[[NSCC]] Reject Code 2 95 96 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 97 98 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 4 99 100 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 15

Share Aging Record Layouts 
Share Aging Grand Total Trailer (B/F78) 15 
SHARE AGING GRAND TOTAL TRAILER (B/F78) 
Record 1 of 1 
 
Input from Submitting [[participant]] – Optional Record 
Output from [[NSCC]] to Receiving [[participant]] – Required Record 
 
The Share Aging grand total trailer record is used to recap all records for a submitting [[participant]] (on input to 
[[NSCC]]) or receiving [[participant]] (on output from [[NSCC]]). 
Share Aging Grand Total Trailer (B/F78) Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
System Code (Originator 
Type) 
1 1 1 A/N B = Delivering Firm  
F = Fund 
R 
Record Type 2 3 2 A/N 78 = Share Aging Grand Total Trailer R 
Sequence Number 4 5 2 A/N 01 R 
Submitting/Receiving 
[[participant]] Number 
6 9 4 A/N  R 
Total records 10 18 9 N 999,999,999 (Total records including 
headers and trailers) 
R 
Filler 19 100 82 A/N Space R 

---

## Page 16

Share Aging Record Layouts 
Share Aging Output Header (N00) 16 
SHARE AGING OUTPUT HEADER (N00) 
Record 1 of 1 
Output from [[NSCC]] to firms and funds 
This is the first record in [[NSCC]] output Share Aging file. 
Share Aging Output Header (N00) Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description 
System Code (Originator Type) 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 5 2 A/N 01 
Recipient Number 6 9 4 A/N  
Literal 10 20 11 A/N 11111111111 
Transmission Date 21 28 8 A/N mmddccyy 
AutoRoute file [[ID]] 29 36 8 A/N  
Literal 37 49 13 A/N SHARE AGING 
Filler 50 100 51 A/N Space 
 

---

## Page 17

Share Aging Record Layouts 
APPENDIX – Summary of Changes 17 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 
 
  

---

## Page 18

Share Aging Record Layouts 
Summary of changes – modification Q3, 2021 18 
SUMMARY OF CHANGES – MODIFICATION Q3, 2021 
Record Description New Description 
B/F78 Required  Input from Submitting [[participant]] – Optional Record  
Output from [[NSCC]] to Receiving [[participant]] – Required Record 
  

---

## Page 19

Share Aging Record Layouts 
Summary of changes – effective Q1, 2019 19 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 20

Share Aging Record Layouts 
Summary of changes – effective Q4, 2017 20 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2017 
Added New Value to Existing Field 
Field Name Record Type and Location Description 
Customer SSN/EIN 
Number Indicator 
B/F75, record1, start 38, end 38, length 1, A/N,R 0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN 
Renamed Existing Field 
Old Name Record Type and Location New Name 
Customer SSN/EIN 
Indicator 
B/F75, record1, start 38, end 38, length 1, A/N,R Customer SSN/EIN Number Indicator 
 

---

## Page 21

Share Aging Record Layouts 
Summary of changes – effective Q4, 2011 21 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2011 
Added New Field 
Field Name Location Requirement Reject Code 
Social Code B/F75 seq.#1, start 52, end 53, length 2, A/N Required 68 

---

## Page 22

Share Aging Record Layouts 
Summary of changes – effective Q2, 2011 22 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2011 
Requirements Changed For Existing Field 
Field Name Location Old requirement New requirement 
Control/Reference 
Number 
B/F75 seq.#2, start 26, end 45, 
length 20, A/N 
Optional Required 
Control/Reference 
Number Indicator 
B/F75 seq.#2, start 46, end 46, 
length 1, A/N 
Optional/Conditional 
1 = Fund/SERV control 
number (should be used if 
requested through ACATS) 
2 = Networking transfer 
(B52) control number (should 
be used if requested through 
Networking) 
3 = Manual reference 
number 
Required 
1 = Fund/SERV control 
number (should be used if 
requested through ACATS) 
2 = Networking transfer 
(B52) control number (should 
be used if requested through 
Networking) 
3 = Manual reference 
number 
Money Market 
Commissionable Share 
Indicator 
Renamed to 
Commissionable Share 
Indicator 
B/F76 seq.#2, start 55, end 55, 
length 1, A/N 
Optional 
 
0 = Non-commissionable 
1 = Commissionable 
Required 
 
0 = Non-commissionable 
1 = Commissionable 
 
 

---

## Page 23

© 2023 [[DTCC]]. All rights reserved.  [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: November 8, 2023 
Publication Code: MFS335 
Service: Networking 
Title: Share Aging Record Layouts 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 
 
 