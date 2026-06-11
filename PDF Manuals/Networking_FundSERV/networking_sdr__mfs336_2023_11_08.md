---
title: "networking_sdr__mfs336_2023_11_08.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/networking_sdr__mfs336_2023_11_08.pdf"
pages: 50
size: "565.3 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# networking_sdr__mfs336_2023_11_08.pdf

**Original File:** [networking_sdr__mfs336_2023_11_08.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/networking_sdr__mfs336_2023_11_08.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 50  
**File Size:** 565.3 KB  

---

## Page 1

 
 
 
Networking 
STANDARDIZED DATA REPORTING (SDR) 
NOVEMBER 8, 2023 
 

---

## Page 2

Standardized Data Reporting (SDR) 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 4 
Record Layouts .................................................................................................................................................... 5 
SDR Request (F20) ............................................................................................................................................... 7 
Record 1 of 2 ...................................................................................................................................................... 7 
Record 2 Of 2 ...................................................................................................................................................... 9 
SDR Header (B/U21) ........................................................................................................................................... 11 
Record 1 of 1 ....................................................................................................................................................11 
SDR Acknowledgment (B/U22) ......................................................................................................................... 14 
Record 1 of 1 ....................................................................................................................................................14 
SDR Reject (B/U23) ............................................................................................................................................ 16 
Record 1 of 1 ....................................................................................................................................................16 
SDR Detail (B/U24) ............................................................................................................................................. 17 
Record 1 of 2 ....................................................................................................................................................17 
Record 2 of 2 ....................................................................................................................................................20 
SDR Summary (B/U25) ....................................................................................................................................... 21 
Record 1 of 2 ....................................................................................................................................................21 
Record 2 of 2 ....................................................................................................................................................25 
SDR Trailer (B/U27) ............................................................................................................................................ 28 
Record 1 of 2 ....................................................................................................................................................28 
Record 2 of 2 ....................................................................................................................................................30 
SDR Reminder (N28) .......................................................................................................................................... 32 
Record 1 of 1 ....................................................................................................................................................32 
SDR Grand Total Trailer (B/F/N/U29) ................................................................................................................ 33 
Record 1 of 1 ....................................................................................................................................................33 
SDR [[NSCC]] Output Header (N00) ...................................................................................................................... 34 
Record 1 of 1 ....................................................................................................................................................34 
Datatrak Header .................................................................................................................................................. 35 
Record 1 of 1 ....................................................................................................................................................35 
Datatrak Trailer ................................................................................................................................................... 36 

---

## Page 3

Standardized Data Reporting (SDR) 
History of Important Notices 3 
Record 1 of 1 ....................................................................................................................................................36 
APPENDIX – Summary of Changes .................................................................................................................. 37 
Summary of changes – effective Q1, 2019 ...................................................................................................... 38 
Summary of changes – effective Q3, 2013 ...................................................................................................... 39 
Summary of changes – effective Q2, 2012 ...................................................................................................... 40 
Summary of changes – effective Q4, 2011 ...................................................................................................... 41 
Summary of changes – effective Q4, 2008 ...................................................................................................... 44 
Summary of changes – effective Q2, 2007 ...................................................................................................... 48 
 

---

## Page 4

Standardized Data Reporting (SDR) 
History of Important Notices 4 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notices 
November 8, 2023 Record is rebranded and reviewed. 
May 12, 2023 Record is rebranded and reviewed. 
March 25, 2019 Please see Important Notices:  
a8658 P&S 8233 Dated December 19, 2018 
September 05, 2013 Please see Important Notices: 
a7693 P&S 7263 Dated September 5, 2013 
April 23, 2012 Please see Important Notices: 
a7355 P&S 6925 Dated January 12, 2012 
October 17, 2011 Please see Important Notices: 
a7241 P&S 6811 Dated July 8, 2011 
October 20, 2008 Please see Important Notices: 
a6642 P&S 6212 Dated June 25, 2008  
a6655 P&S 6225 Dated July 07, 2008 
June 18, 2007 Please see Important Notices: 
a6446 P&S 6016 Dated May 3, 2007  
a6435 P& #6005 Dated April 25, 2007 
August 7, 2006 Please see Important Notices: 
a6266 P&S 5836 Dated July 7, 2006  
a6254 P&S 5824 Dated June 12, 2006  
a6213 P&S 5783 Dated March 8, 2006 

---

## Page 5

Standardized Data Reporting (SDR) 
Record Layouts 5 
RECORD LAYOUTS 
The following are Networking Standardized Data Reporting (SDR) Record Layouts. The column headings are 
as follows: 
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
SDR Reject Code - The SDR reject code which indicates that this field is invalid. 
Note:  
Reject codes used for SDR are different then reject codes used for other Networking applications 
Notes: 
• Alphanumeric type fields may include any character in the computer character set but should not include unprintable 
characters such as Low-Value, High-Value, Comp-3 fields, etc., since these kinds of characters may cause problems 
during transmission time. 
• Numeric type fields may include digits (0-9) only. 
• Required fields mean the following: 
a. Fields with specified list of values must have one of those values. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above 
but must not be spaces. 
c. Numeric type fields without a specified list of values must be numeric greater than zero. 
d. Fields with other requirements must follow these requirements (for example Firm Number must be valid and 
eligible for Networking). 
• Optional fields mean the following: 
a. Fields with specified list of values must have one of those values or space. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first note above. 
c. Numeric type fields without specified list of values must be numeric or space. 
d. Fields with other requirements must follow these requirements or may be space (for example Fund Number must 
be valid and eligible for Fund/SERV or may be space) 

---

## Page 6

Standardized Data Reporting (SDR) 
Record Layouts 6 
• All dates in the layouts have the format mmddccyy (except where otherwise indicated) where:  
mm = Month 
dd = Day in month  
cc = Century 
yy = Year in century 
Example: 
June 15, 2022 is represented as: 06152022 
September 3, 2023 is represented as: 09032023 

---

## Page 7

Standardized Data Reporting (SDR) 
SDR Request (F20) 7 
SDR REQUEST (F20) 
Record 1 of 2 
Required 
Input From Fund To [[NSCC]] 
Output From [[NSCC]] To Firm (accepted) and Fund (rejected) 
Note:  
SDR Request records [[DO]] NOT have an application header (Record type 21) or trailer (record type 27) record 
SDR Fund Request (F20) Record 1 of 2 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N F = Fund R 01 
Record Type 2 3 2 A/N 20 = SDR Request R 02 
Sequence Number 4 5 2 A/N 01 R 03 
SDR Control Number 6 20 15 A/N ppppyjjjnnnnnnn 
Where: 
pppp = Fund Number 
y = Last digit of year 
jjj = Julian Date 
nnnnnnn = Unique sequential number 
assigned by fund 
R 04 
Firm Number 21 24 4 A/N  R 06 
Fund Number 25 28 4 A/N  R 09 
Security Issue [[ID]] 29 37 9 A/N  R 13 
Underlying Firm 
Number 
38 41 4 A/N Required when Underlying Firm Indicator 
is provided. 
Must be a valid [[NSCC]] Number when 
Underlying Firm Indicator =‘01’. 
OC 07 
Underlying Firm 
Indicator 
42 43 2 A/N Required when Underlying Firm Number 
is provided. Not allowed otherwise. 
01 = [[NSCC]] Number 
02 = [[OTC]] Symbol 
03 = UFS 
OC 08 Fund Account Number 44 63 20 A/N Required if Firm Account Number is not 
provided. 
OC 10 

---

## Page 8

Standardized Data Reporting (SDR) 
SDR Request (F20) 8 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Firm Account Number 64 83 20 A/N Required if Fund Account Number is not 
provided. 
OC 11 
Fund/SERV Control 
Number 
84 98 15 A/N Required if SDR Request Type = 04 OC  
SDR Request Type 99 100 2 A/N 01 = Fund Account Level  
02 = Plan Level 
03 = [[investor]] Omnibus Account Level 
04 = Fund/SERV Control Number 
Request 
05 = Rep Level 
06 = Stop Recurring 
R 05 
From Date 101 108 8 A/N mmddccyy R 12 
SSN/TIN 109 117 9 A/N  O 16 
Filler 118 141 24 A/N Space R  
[[NSCC]] Reject Indicator 142 142 1 A/N Input: Space Output: 
0 = Accepted by [[NSCC]] 1 = Rejected by 
[[NSCC]] 
R  
[[NSCC]] Reject Code 1 143 144 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 145 146 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 147 148 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 4 149 150 2 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 9

Standardized Data Reporting (SDR) 
SDR Request (F20) 9 
Record 2 Of 2 
Optional/ Conditional  
Input from Fund to [[NSCC]] 
Output from [[NSCC]] to Firm (accepted) and Fund (rejected) 
This record is required if SDR Request Type field of F20 record 1 equals 02 (Plan Level) or 03 ([[investor]] 
Omnibus Account Level) 
SDR Fund Request (F20) Record 2 of 2 
Record 2 Of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N F = Fund R 01 
Record Type  2 3 2 A/N 20 = SDR Request R 02 
Sequence Number 4 5 2 A/N 02 R 03 
Plan [[ID]]/[[investor]] Omnibus 
Account Number 
6 25 20 A/N Required if SDR Request Type 
equals one of the following: 
02 = Plan Level or 
03 = [[investor]] Omnibus Account 
Level 
OC 14 
Omnibus Account 
Indicator 
26 26 1 A/N Required if Plan [[ID]]/[[investor]] 
Omnibus Account Number is 
provided 
0 = Plan [[ID]] 
1 = [[investor]] Omnibus Account 
OC 15 
Recurring Indicator 27 27 1 A/N 0 = No 
1 = Yes 
O 17 
To Date 28 35 8 A/N mmddccyy O 18 
Includes Category 2 
Transactions? 
36 36 1 A/N 0 = No 
1 = Yes 
O 19 
Registered Representative 
(RR) Number 
37 45 9 A/N Required if SDR Request Type is 05 
= Rep Level. 
OC 20 
RR Branch 46 54 9 A/N  O 21 
RR Firm 55 62 8 A/N  O 22 
Original SDR Control 
Number 
63 77 15 A/N Used to stop a recurring request. O 23 
Threshold Amount 78 86 9 N 999,999,999 
Threshold Amount is equal to or 
greater than (=>) Amount 
Requested. 
O 24 

---

## Page 10

Standardized Data Reporting (SDR) 
SDR Request (F20) 10 
Record 2 Of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Transaction Type 87 88 2 A/N 01 = Buy 
02 = Sell 
Space means that the request is for 
all transactions, which may include 
transfers. 
O 25 
Filler 89 150 62 A/N Space R  

---

## Page 11

Standardized Data Reporting (SDR) 
SDR Header (B/U21) 11 
SDR HEADER (B/U21) 
Record 1 of 1 
Required 
Input From Firm To [[NSCC]] 
Output From [[NSCC]] To Fund and Firm 
The SDR Header record is used to introduce SDR Acknowledgment (B/U22), Reject (B/U23), Detail (B/U24) 
and/or Summary (B/U25) records. 
SDR Header (B/U21) Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N B = Firm 
U = Underlying Firm 
R 01 
Record Type 2 3 2 A/N 21 = SDR Header R 02 
Sequence Number 4 5 2 A/N 01 R 03 
SDR Control Number 6 20 15 A/N The SDR Control Number submitted 
by the fund 
OR – 
The SDR Response Number (see 
start 101, end 115) for a response 
provided against a request made 
outside of [[NSCC]]. 
R 04 
Firm Number 21 24 4 A/N  R 06 
Fund Number 25 28 4 A/N  R 09 
Security Issue [[ID]] 29 37 9 A/N  R 13 
Underlying Firm 
Number 
38 41 4 A/N Required when 
Originator Type = ‘U’ or 
Underlying Firm Indicator is 
provided. 
Must be a valid [[NSCC]] Number when 
Originator Type = ‘U’ or 
Underlying Firm Indicator =‘01’. 
OC 07 

---

## Page 12

Standardized Data Reporting (SDR) 
SDR Header (B/U21) 12 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Underlying Firm 
Indicator 
42 43 2 A/N Required when Underlying Firm 
Number is provided. Not allowed 
otherwise. 
01 = [[NSCC]] Number 02 = [[OTC]] 
Symbol 03 = UFS 
 
Must equal ‘01’ when Originator Type 
= ‘U’. 
OC 08 
Fund Account Number 44 63 20 A/N Required if Firm Account Number is 
not provided. 
OC 10 
Firm Account Number 64 83 20 A/N Required if Fund Account Number is 
not provided. 
OC 11 
Fund/SERV Control 
Number 
84 98 15 A/N  O  
Response Type 99 100 2 A/N 01 = Summary Level  
02 = Detail Level 
03 = Both Summary and Detail  
04 = Acknowledgment 
05 = Firm Reject 
R 28 
SDR Response Number 101 115 15 A/N  R 27 
Partial Response 
Indicator 
116 116 1 A/N 0 = Full/Final Response  
1 = Partial Response 
2 = Incomplete/Final Response 
R 29 
Correction Indicator 117 117 1 A/N 0 = Regular 
1 = Correction 
O 30 
Filler 118 141 24 A/N Space R  
[[NSCC]] Reject Indicator 142 142 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 143 144 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 145 146 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 147 148 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 13

Standardized Data Reporting (SDR) 
SDR Header (B/U21) 13 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
[[NSCC]] Reject Code 4 149 150 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 14

Standardized Data Reporting (SDR) 
SDR Acknowledgment (B/U22) 14 
SDR ACKNOWLEDGMENT (B/U22) 
Record 1 of 1 
Required 
Input From Firm To [[NSCC]] 
Output From [[NSCC]] To Fund (accepted) and Firm (rejected) 
Note:  
This Acknowledgment record will be submitted within the Header (B/U21) and Trailer (B/U27). The Acknowledgment should 
be the first response from the Firm to the Fund for a specific SDR Request. However, [[NSCC]] will not validate the proper 
sequence for submitting the Acknowledgment and SDR Detail Response records. 
SDR Acknowledgment (B/U22) Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N B = Firm 
U = Underlying Firm 
R 01 
Record Type 2 3 2 A/N 22 = SDR Acknowledgment R 02 
Sequence Number 4 5 2 A/N 01 R 03 
Acknowledgment 
Indicator 
6 6 1 A/N 0 = Response will be Provided 
1 = Request will be Forwarded to the 
Underlying Firm 
R 67 
Anticipated Response 
Date 
7 14 8 A/N mmddccyy O 68 
Anticipated Response 
File Frequency 
15 15 1 A/N 0 = Full Response 
1 = Partial Response 
O 69 
Filler 16 141 126 A/N Space R  
[[NSCC]] Reject Indicator 142 142 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 143 144 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 145 146 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 147 148 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 15

Standardized Data Reporting (SDR) 
SDR Acknowledgment (B/U22) 15 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
[[NSCC]] Reject Code 4 149 150 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 16

Standardized Data Reporting (SDR) 
SDR Reject (B/U23) 16 
SDR REJECT (B/U23) 
Record 1 of 1 
Required 
Input From Firm To [[NSCC]] 
Output From [[NSCC]] To Fund (accepted) and Firm (rejected) 
Note:  
This Reject record will be submitted within the Header (B/U21) and Trailer (B/U27). 
SDR Reject (B/U23) Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N B = Firm 
U = Underlying Firm 
R 01 
Record Type 2 3 2 A/N 23 = SDR Reject R 02 
Sequence Number 4 5 2 A/N 01 R 03 
Firm Reject Code 1 6 7 2 A/N  R 66 
Firm Reject Code 2 8 9 2 A/N  O 66 
Firm Reject Code 3 10 11 2 A/N  O 66 
Firm Reject Code 4 12 13 2 A/N  O 66 
Filler 14 141 128 A/N Space R  
[[NSCC]] Reject Indicator 142 142 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 143 144 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 145 146 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 147 148 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 4 149 150 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 17

Standardized Data Reporting (SDR) 
SDR Detail (B/U24) 17 
SDR DETAIL (B/U24) 
Record 1 of 2 
Required 
Input From Firm To [[NSCC]] 
Output From [[NSCC]] To Fund (accepted) and Firm (rejected) 
The Detail records represent the Shareholder SSN/TIN within a particular Plan [[ID]] or [[investor]] Omnibus 
Account. The Detail may be repeated within the Header (B/U21) and Trailer (B/U27) records.  
SDR Detail (B/U24) Record 1 of 2 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N B = Firm 
U = Underlying Firm 
R 01 
Record Type 2 3 2 A/N 24 = SDR Detail R 02 
Sequence Number 4 5 2 A/N 01 R 03 
Plan [[ID]]/[[investor]] 
Omnibus Account 
Number 
6 25 20 A/N  O 14 
Omnibus Account 
Indicator 
26 26 1 A/N Required if Plan [[ID]]/[[investor]] Omnibus 
Account Number is provided 
 
0 = Plan [[ID]] 
1 = [[investor]] Omnibus Account 
OC 15 SSN/TIN 27 35 9 A/N  R 16 
SSN/TIN Indicator 36 36 1 A/N 0 = Tax [[ID]] number 
1 = Social security number 2 = [[investor]] 
TIN/EIN 
R 32 
NAV Date 37 44 8 A/N mmddccyy R 33 
Transaction Type 45 46 2 A/N 01 = Buy 
02 = Sell 
03 = Exchange (Intra-Fund Buy Side) 
04 = Exchange (Intra-Fund Sell Side) 
05 = Transfer in (such as ACATS, 
Networking B52, and transfers in 
kind)  
06 = Transfer out (such as ACATS, 
Networking B52, and transfers in 
kind) 
R 25 

---

## Page 18

Standardized Data Reporting (SDR) 
SDR Detail (B/U24) 18 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Transaction Code 
 
(Used to indicate 
detailed/specific 
transaction codes that 
fall under the 
respective Transaction 
Types) 
47 48 2 A/N 01 = Employee Contribution  
02 = Employer Contribution  
03 = Additional Contribution  
04 = Loan repayment-principal  
05 = Loan repayment-interest  
06 = Forfeiture 
07 = Adjustments  
08 = Fund Transfer  
09 = Exchange 
10 = Conversion Balance Transfer  
11 = Non-discrimination refund  
12 = Loan Distribution 
13 = In-service distribution  
14 = Installment Distribution  
15 = Termination Distribution  
16 = Hardship Distribution  
17 = Lump Sum Distribution  
18 = QDRO Distributions 
19 = Required Minimum Distribution  
20 = STR Fee 
21 = CDSC Fee 
22 = Other Fees  
23 = Rebalance 
24 = Return of Excess Distribution  
25 = Rollover 
50 = Initial/Subsequent Purchase  
51 = Sell/Redemption 
52 = Physical Transfer of [[shares]] 
53 = Automated or Systematic 
Transaction 
60 = Credits  
61 = Free Look 
62 = Annuitization 
63 = Reversals 
O 34 
Transaction Category 49 49 1 A/N 1 = Category 1 
2 = Category 2 
R 35 

---

## Page 19

Standardized Data Reporting (SDR) 
SDR Detail (B/U24) 19 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Dollar Amount 50 65 16 N 99,999,999,999,999.99 
Optional if Transaction Type = 05 or 06, 
or if Transaction Code = 7 or 52. 
RC 36 
Share Amount 66 79 14 N 9,999,999,999.9999 R 37 
Price 80 91 12 N 999,999.999999 
Optional if Transaction Type = 05 or 06, 
or if Transaction Code = 7 or 52. 
RC 38 
Transaction [[ID]] 92 111 20 A/N  O  
Contra Security Issue 
[[ID]] 
112 120 9 A/N  O 40 
Social Code 121 122 2 A/N See Social Code list at  
https://dtcclearning.com/documents/
mutual-fund-services-1/mfs-cross-
product/codes-8/2498-social-
codes/file.html 
O 53 
Unit Value Indicator 123 123 1 A/N 0 or Space = [[shares]]  
1 = Units 
O 98 
Source System [[ID]] 124 133 10 A/N  O  
Filler 134 141 8 A/N Space R  
[[NSCC]] Reject Indicator 142 142 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 143 144 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 145 146 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 147 148 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 4 149 150 2 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 20

Standardized Data Reporting (SDR) 
SDR Detail (B/U24) 20 
Record 2 of 2 
Optional 
Input From Firm To [[NSCC]] 
Output From [[NSCC]] To Fund (accepted) and Firm (rejected) 
SDR Detail (B/U24) Record 2 of 2 
Record 2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N B = Firm 
U = Underlying Firm 
R 01 
Record Type 2 3 2 A/N 24 = SDR Detail R 02 
Sequence Number 4 5 2 A/N 02 R 03 
STR Fee Amount 6 12 7 N 99,999.99 O 41 
CDSC Amount 13 19 7 N 99,999.99 O 42 
Transaction Source 20 20 1 A/N 0 = [[participant]]/Shareholder 
1 = Plan/Administrator 
2 = Rep 
3 = Firm Cannot Differentiate  
4 = Record keeper or 
Insurance Carrier 
O 43 
Registered 
Representative (RR) 
Number 
21 29 9 A/N  O 20 
RR Branch 30 38 9 A/N  O 21 
RR Firm 39 46 8 A/N  O 22 
Agent For Firm 47 50 4 A/N  O  
Plan Name 51 85 35 A/N  O  
Customer Name 86 120 35 A/N  O  
Customer Level Account 
Number 
121 150 30 A/N  O  

---

## Page 21

Standardized Data Reporting (SDR) 
SDR Summary (B/U25) 21 
SDR SUMMARY (B/U25) 
Record 1 of 2 
Required 
Input From Firm To [[NSCC]] 
Output From [[NSCC]] To Fund (accepted) and Firm (rejected) 
This Summary record will be submitted within the Header (B/U21) and Trailer (B/U27). It replaces the Detail 
records (B/U24) as a response for each plan or [[investor]] omnibus account. 
Dollar Values [[DO]] not include Transfers, which are not recorded with a price or value.  
SDR Summary (B/U25) Record 1 of 2 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N B = Firm 
U = Underlying Firm 
R 01 
Record Type 2 3 2 A/N 25 = SDR Summary R 02 
Sequence Number 4 5 2 A/N 01 R 03 
Plan [[ID]]/[[investor]] Omnibus 
Account Number 
6 25 20 A/N One of the following is required: Plan [[ID]] 
or 
[[investor]] Omnibus Account Number 
R 14 
Omnibus Account Indicator 26 26 1 A/N 0 = Plan [[ID]] 
1 = [[investor]] Omnibus Account 
R 15 
NAV Date 27 34 8 A/N mmddccyy R 33 

---

## Page 22

Standardized Data Reporting (SDR) 
SDR Summary (B/U25) 22 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Dollar Value of ALL 
[[participant]]/ Shareholder 
Buys 
35 50 16 N 99,999,999,999,999.99 
Required if none of the following are 
provided: 
- Dollar Value of ALL 
[[participant]]/Shareholder Sells; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of CATEGORY 1 
[[participant]] /Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of CATEGORY 1 
[[participant]] /Shareholder Exchanges 
(Intra-Fund Sell-Side). 
OC 47 
Dollar Value of ALL 
[[participant]]/ Shareholder 
Sells 
51 66 16 N 99,999,999,999,999.99 
Required if none of the following are 
provided: 
- Dollar Value of ALL 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Sells; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys; 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of CATEGORY 1 
[[participant]] /Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of CATEGORY 1 
[[participant]] /Shareholder Exchanges 
(Intra-Fund Sell-Side). 
OC 48 

---

## Page 23

Standardized Data Reporting (SDR) 
SDR Summary (B/U25) 23 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Dollar Value of 
CATEGORY 1 
[[participant]]/ Shareholder 
Buys 
67 82 16 N 99,999,999,999,999.99 
Required if none of the following are 
provided: 
- Dollar Value of ALL [[participant]]/ 
Shareholder Buys; 
- Dollar Value of ALL 
[[participant]]/Shareholder Sells; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side). 
OC 49 
Dollar Value of 
CATEGORY 1 
[[participant]]/ Shareholder 
Sells 
83 98 16 N 99,999,999,999,999.99 
Required if none of the following are 
provided: 
- Dollar Value of ALL [[participant]]/ 
Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys; 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of CATEGORY 1 
[[participant]] /Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of CATEGORY 1 
[[participant]] /Shareholder Exchanges 
(Intra-Fund Sell-Side). 
OC 50 
Number of CATEGORY 1 
[[participant]]/ 
Shareholder Buys 
99 106 8 N 99,999,999 O 51 

---

## Page 24

Standardized Data Reporting (SDR) 
SDR Summary (B/U25) 24 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Number of CATEGORY 
1 [[participant]]/ Shareholder 
Sells 
107 114 8 N 99,999,999 O 52 
Underlying Firm Number 115 118 4 A/N  O 07 
Underlying Firm Indicator 119 120 2 A/N Required when Underlying Firm 
Number is provided. Not allowed 
otherwise. 
01 = [[NSCC]] Number 02 = [[OTC]] Symbol 
03 = UFS 
OC 08 
Social Code 121 122 2 A/N See Social Code list at 
https://dtcclearning.com/documents/
mutual-fund-services-1/mfs-cross-
product/codes-8/2498-social-
codes/file.html 
O 53 
Filler 123 141 19 A/N Space R  
[[NSCC]] Reject Indicator 142 142 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 143 144 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 145 146 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 147 148 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 4 149 150 2 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 25

Standardized Data Reporting (SDR) 
SDR Summary (B/U25) 25 
Record 2 of 2 
Optional 
Input From Firm To [[NSCC]] 
Output From [[NSCC]] To Fund (accepted) and Firm (rejected) 
SDR Summary (B/U25) Record 2 of 2 
Record 2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N B = Firm 
U = Underlying Firm 
R 01 
Record Type 2 3 2 A/N 25 = SDR Summary R 02 
Sequence Number 4 5 2 A/N 02 R 03 
Dollar Value of ALL 
[[participant]]/ 
Shareholder 
Exchanges (Intra Fund 
Buy-Side) 
6 21 16 N 99,999,999,999,999.99 
Required if none of the following are 
provided: 
- Dollar Value of ALL 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges (Intra-
Fund Sell-Side); 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Exchanges (Intra-
Fund Buy-Side); 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Exchanges (Intra-
Fund Sell-Side). 
OC 54 

---

## Page 26

Standardized Data Reporting (SDR) 
SDR Summary (B/U25) 26 
Record 2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Dollar Value of ALL 
[[participant]]/ 
Shareholder 
Exchanges (Intra Fund 
Sell-Side) 
22 37 16 N 99,999,999,999,999.99 
Required if none of the following are 
provided: 
- Dollar Value of ALL 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges (Intra-
Fund Buy-Side); 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Exchanges (Intra-
Fund Buy-Side); 
- Dollar Value of CATEGORY 1 [[participant]] 
/Shareholder Exchanges (Intra-Fund Sell-
Side). 
OC 55 
Dollar Value of 
CATEGORY 1 of 
[[participant]]/ 
Shareholder 
Exchanges (Intra Fund 
Buy-Side) 
38 53 16 N 99,999,999,999,999.99 
Required if none of the following are 
provided: 
- Dollar Value of ALL 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges (Intra-
Fund Buy-Side); 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges (Intra-
Fund Sell-Side); 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Exchanges (Intra-
Fund Sell-Side). 
OC 56 

---

## Page 27

Standardized Data Reporting (SDR) 
SDR Summary (B/U25) 27 
Record 2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Dollar Value of 
CATEGORY 1 
[[participant]]/ 
Shareholder 
Exchanges (Intra Fund 
Sell-Side) 
54 69 16 N 99,999,999,999,999.99 
Required if none of the following are 
provided: 
- Dollar Value of ALL 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Sells; 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges (Intra-
Fund Buy-Side); 
- Dollar Value of ALL 
[[participant]]/Shareholder Exchanges (Intra-
Fund Sell-Side); 
- Dollar Value of CATEGORY 1 [[participant]] 
/Shareholder Exchanges (Intra-Fund Buy-
Side). 
OC 57 
Number of 
CATEGORY 1 
[[participant]]/ 
Shareholder 
Exchanges (Intra Fund 
Buy-Side) 
70 77 8 N 99,999,999 O 58 
Number of 
CATEGORY 1 
[[participant]]/ 
Shareholder 
Exchanges (Intra Fund 
Sell-Side) 
78 85 8 N 99,999,999 O 59 
Number of [[shares]] in 
Plan/[[investor]] Omnibus 
Account 
86 99 14 N 9,999,999,999.9999 O 60 
[[EOD]] Dollar Balance 100 115 16 N 99,999,999,999,999.99 O 61 
Filler 116 150 35 A/N Space R  

---

## Page 28

Standardized Data Reporting (SDR) 
SDR Trailer (B/U27) 28 
SDR TRAILER (B/U27) 
Record 1 of 2 
Required 
Input From Firm To [[NSCC]] 
Output From [[NSCC]] To Fund and Firm 
The SDR Trailer record Sequence #1 is used to recap the SDR Acknowledgment (B/U22), Reject (B/U23), 
Detail (B/U24) and/or Summary (B/U25) records. 
SDR Trailer (B/U27) Record 1 of 2 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N B = Firm 
U = Underlying Firm 
R 01 
Record Type 2 3 2 A/N 27 = SDR Trailer R 02 
Sequence Number 4 5 2 A/N 01 R 03 
SDR Control Number 6 20 15 A/N Same as in the Header (B/U21) R 04 
Firm Number 21 24 4 A/N Same as in the Header (B/U21) R 06 
Fund Number 25 28 4 A/N Same as in the Header (B/U21) R 09 
Security Issue [[ID]] 29 37 9 A/N Same as in the Header (B/U21) R 13 
Underlying Firm 
Number 
38 41 4 A/N Same as in the Header (B/U21) OC 07 
SDR Response 
Number 
42 56 15 A/N Same as in the Header (B/U21) R 27 
Total Acknowledgment 
Items 
57 65 9 N 999,999,999 
Number of record type 22 with 
sequence 01 within this group  
(Zero Allowed) 
R 88 
Total Reject Items 66 74 9 N 999,999,999 
Number of record type 23 with 
sequence 01 within this group  
(Zero Allowed). 
R 89 
Total Detail Items 75 83 9 N 999,999,999 
Number of record type 24 with 
sequence 01 within this group (Zeroes 
Allowed). 
R 62 

---

## Page 29

Standardized Data Reporting (SDR) 
SDR Trailer (B/U27) 29 
Record 1 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Total Summary Items 84 92 9 N 999,999,999 
Number of record type 25 with 
sequence 01 within this group (Zeroes 
Allowed). 
R 63 
Total Records 93 101 9 N 999,999,999 
Total number of PHYSICAL records 
(including SDR headers and trailers) 
within this group. 
R 64 
Filler 102 141 40 A/N Space R  
[[NSCC]] Reject Indicator 142 142 1 A/N Input: Space  
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 143 144 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 145 146 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 147 148 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 4 149 150 2 A/N Input: Space 
Output: Reject code or space 
R  
 
 
  

---

## Page 30

Standardized Data Reporting (SDR) 
SDR Trailer (B/U27) 30 
Record 2 of 2 
Output from [[NSCC]] to Fund and firm 
The SDR Trailer record Sequence #2 is used by [[NSCC]] to inform Firms and Funds of the number of items that 
have been accepted or rejected by [[NSCC]] on input. 
SDR Trailer (B/U27) Record 2 of 2 
Record 2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Originator Type 1 1 1 A/N B = Firm 
U = Underlying Firm 
R 01 
Record Type 2 3 2 A/N 27 = SDR Trailer R 02 
Sequence Number 4 5 2 A/N 02 R 03 
Total Input 
Acknowledgment 
Items accepted 
6 14 9 N 999,999,999 
Number of record type 22 with 
sequence 01 accepted by [[NSCC]] on 
input. 
R  
Total Input Reject 
Items Accepted 
15 23 9 N 999,999,999 
Input: Space 
Output: Number of record type 23 with 
sequence 01 accepted by [[NSCC]] on 
input. 
R  
Total Input Detail Items 
Accepted 
24 32 9 N 999,999,999 
Input: Space 
Output: Number record type 24 with 
sequence 01 accepted by [[NSCC]] on 
input. 
R  
Total Input Summary 
Items Accepted 
33 41 9 N 999,999,999 
Input: Space 
Output: Number of record type 25 with 
sequence 01 accepted by [[NSCC]] on 
input. 
R  
Total Input 
Acknowledgment 
Items Rejected 
42 50 9 N 999,999,999 
Input: Space 
Output: Number of record type 22 with 
sequence 01 rejected by [[NSCC]] on 
input. 
R  
Total Input Reject 
Items Rejected 
51 59 9 N 999,999,999 
Input: Space 
Output: Number of record type 23 with 
sequence 01 rejected by [[NSCC]] on 
input. 
R  

---

## Page 31

Standardized Data Reporting (SDR) 
SDR Trailer (B/U27) 31 
Record 2 of 2 
Field Name 
Start End Len Type Description Opt/ 
Req 
SDR 
Reject 
Code 
Total Input Detail Items 
Rejected 
60 68 9 N 999,999,999 
Input: Space 
Output: Number of record type 24 with 
sequence 01 rejected by [[NSCC]] on 
input. 
R  
Total Input 
Summary Items 
Rejected 
69 77 9 N 999,999,999 
Input: Space 
Output: Number of record type 25 with 
sequence 01 rejected by [[NSCC]] on 
input 
R  
Filler 78 150 73 A/N Space R  

---

## Page 32

Standardized Data Reporting (SDR) 
SDR Reminder (N28) 32 
SDR REMINDER (N28) 
Record 1 of 1 
Output from [[NSCC]] to Fund and Firm 
Note:  
SDR Reminder records [[DO]] NOT have an application header (21) or trailer (27) record 
Record 1 of 1 
Field Name 
Start End Len Type Description 
Originator Type 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 28 = SDR Reminder 
Sequence Number 4 5 2 A/N 01 
SDR Control Number 6 20 15 A/N  
Firm Number 21 24 4 A/N  
Fund Number 25 28 4 A/N  
Security Issue [[ID]] 29 37 9 A/N  
Underlying Firm Number 38 41 4 A/N  
Reminder Age 42 44 3 N 001-998 = Reminder Age (in business days, 
including Saturday) 
999 = Final Reminder, SDR Request has been 
removed from database 
Filler 45 150 106 A/N Space 

---

## Page 33

Standardized Data Reporting (SDR) 
SDR Grand Total Trailer (B/F/N/U29) 33 
SDR GRAND TOTAL TRAILER (B/F/N/U29) 
Record 1 of 1 
Required  
Input/Output 
The SDR grand total trailer record is used to recap all records for a submitting [[participant]] (on input to [[NSCC]]) or 
receiving [[participant]] (on output from [[NSCC]]). 
SDR Grand Total Trailer (B/F/N/U29) Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
Originator Type 1 1 1 A/N Input: 
B = Firm  
F = Fund 
U = Underlying Firm 
 
Output: 
N = [[NSCC]] 
R 
Record Type 2 3 2 A/N 29 = SDR Grand Total Trailer R 
Sequence Number 4 5 2 A/N 01 R 
[[participant]] Number 6 9 4 A/N Input: Submitter (Originator)  
Output: Recipient 
R 
Total records 10 18 9 N 999,999,999 
Total number of PHYSICAL records per 
submitter (input to [[NSCC]]) or recipient (output 
from [[NSCC]]) 
R 
Filler 19 150 132 A/N Space R 

---

## Page 34

Standardized Data Reporting (SDR) 
SDR [[NSCC]] Output Header (N00) 34 
SDR [[NSCC]] OUTPUT HEADER (N00) 
Record 1 of 1 
Output from [[NSCC]] to Fund and Firm 
This is the first record in [[NSCC]] output SDR file. 
SDR Output Header (N00) Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description 
System Code (Originator 
Type) 
1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = SDR [[NSCC]] Output Header 
Sequence Number 4 5 2 A/N 01 
Recipient Number 6 9 4 A/N  
Literal 10 20 11 A/N 11111111111 
Transmission Date 21 28 8 A/N ccyymmdd 
Autoroute File [[ID]] 29 36 8 A/N Value '02100298' (Fund Request)  
or '02100327’ (Firm Response) 
Literal 37 53 17 A/N Value 'SDR Fund Request'  
or 'SDR Firm Response’ 
Filler 54 150 97 A/N Space 

---

## Page 35

Standardized Data Reporting (SDR) 
Datatrak Header 35 
DATATRAK HEADER 
Record 1 of 1 
Required 
Input from Fund and Firm to [[NSCC]] 
This is the first record in any SDR file submitted through Datatrak. 
Datatrak Header Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value '26398' (Fund input)  
or '26327' (Firm input) 
R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value 'MF SDR FUND INPUT'  
or 'MF SDR FIRM INPUT' 
R 
Multi-batch Last Batch 
Indicator 
60 60 1 A/N N = Not last batch  
Y = Last batch 
R 
Multi-batch Batch 
Counter 
61 63 3 N  R 
Filler 64 150 87 A/N Space R 

---

## Page 36

Standardized Data Reporting (SDR) 
Datatrak Trailer 36 
DATATRAK TRAILER 
Record 1 of 1 
Required 
Input from Fund and Firm to [[NSCC]] 
This is the last record in any SDR file submitted through Datatrak. 
Datatrak Trailer Record 1 of 1 
Record 1 of 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N END.S R 
DATATRAK SYSID 6 10 5 A/N Value ‘26398’ (Fund input)  
or ‘26327’ (Firm input) 
R 
Literal 11 16 6 A/N .E00.C R 
Originator [[ID]] 17 20 4 A/N  R 
Literal 21 22 2 A/N .S R 
Sub Originator [[ID]] 23 26 4 A/N  R 
Total Records 27 33 7 A/N 9,999,999 
Total # of records in file excluding Datatrak 
header and trailer 
R 
Filler 34 150 117 A/N Space R 
 
 
 
  

---

## Page 37

Standardized Data Reporting (SDR) 
APPENDIX – Summary of Changes 37 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes. 
 

---

## Page 38

Standardized Data Reporting (SDR) 
Summary of changes – effective Q1, 2019 38 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 39

Standardized Data Reporting (SDR) 
Summary of changes – effective Q3, 2013 39 
SUMMARY OF CHANGES – EFFECTIVE Q3, 2013 
Format Changed for Existing Field 
Field Name Location Old format New format 
Transmission Date N00 seq.#1, start 21, end 28, length 8, A/N mmddccyy ccyymmdd  
(Documentation change) 

---

## Page 40

Standardized Data Reporting (SDR) 
Summary of changes – effective Q2, 2012 40 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2012 
Eliminate Reject Codes 
The following reject codes have been permanently eliminated effective April 23, 2012:  
• 31 - Did not find data that matches the request 
• 39 - Tran [[ID]] is invalid 
• 44 - Agent for Firm is invalid 
• 45 - Plan Name is Invalid 
• 46 - Customer Name is Invalid 
• 65 - Reject Indicator Missing or Invalid 
 
Eliminate SDR Reject Code from Record Layout 
Field Name Current Location and Requirement Current SDR Reject 
Code 
New SDR 
Reject Code 
Transaction [[ID]] B/U24 record 1, start 92, end 111, length 20, A/N, Optional 39  

---

## Page 41

Standardized Data Reporting (SDR) 
Summary of changes – effective Q4, 2011 41 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2011 
Requirements Changed for Existing Fields 
Field Name Current location and 
requirement 
New 
Requir 
ement 
New Description 
Plan [[ID]]/[[investor]] Omnibus 
Account Number 
F20 record 2, start 6, end 
25, length 20, Optional 
OC Required if SDR Request Type equals one of 
the following: 
02 = Plan Level or 
03 = [[investor]] Omnibus Account Level 
Threshold Amount F20 record 2, start 78, 
end 
86, length 9, Optional 
 999,999,999 
Threshold Amount is equal to or 
greater than (=>) Amount Requested. 
Omnibus Account Indicator B/U24 record 1, start 26, 
end 26, length 1, 
Optional 
OC Required if Plan [[ID]]/[[investor]] Omnibus 
Account Number is provided 
0 = Plan [[ID]] 
1 = [[investor]] Omnibus Account 
Transaction Code B/U24 record 1, start 47, 
end 48, length 2, 
Optional 
 53 = Automated or Systematic Transaction 
Plan [[ID]]/[[investor]] Omnibus 
Account Number 
B/U25 record 1, start 6, 
end 25, length 20, 
Required 
 One of the following is required: Plan [[ID]] or 
[[investor]] Omnibus Account Number 
Dollar Value of ALL 
[[participant]]/ Shareholder Buys 
B/U25 record 1, start 35 
end 50, length 16, OC 
 99,999,999,999,999.99 
Required if none of the following are 
provided: 
Dollar Value of ALL 
[[participant]]/ Shareholder Sells 
B/U25 record 1, start 51 
end 66, length 16, OC 
 99,999,999,999,999.99 
Required if none of the following are 
provided: 
Dollar Value of CATEGORY 1 
[[participant]]/ Shareholder Buys 
B/U25 record 1, start 67 
end 82, length 16, OC 
 99,999,999,999,999.99 
Required if none of the following are 
provided: 
Dollar Value of CATEGORY 1 
[[participant]]/ Shareholder Sells 
B/U25 record 1, start 83 
end 98, length 16, OC 
 99,999,999,999,999.99 
Required if none of the following are 
provided: 
Dollar Value of ALL 
[[participant]]/ Shareholder 
Exchanges (Intra Fund Buy-
Side) 
B/U25 record 2, start 6 
end 21, length 16, OC 
 99,999,999,999,999.99 
Required if none of the following are 
provided: 
Dollar Value of ALL 
[[participant]]/ Shareholder 
B/U25 record 2, start 22  99,999,999,999,999.99 

---

## Page 42

Standardized Data Reporting (SDR) 
Summary of changes – effective Q4, 2011 42 
Field Name Current location and 
requirement 
New 
Requir 
ement 
New Description 
Exchanges (Intra Fund Sell-
Side) 
end 37, length 16, OC Required if none of the following are 
provided: 
Dollar Value of CATEGORY 1 
of [[participant]]/ Shareholder 
Exchanges (Intra Fund Buy-
Side) 
B/U25 record 2, start 38 
end 53, length 16, OC 
 99,999,999,999,999.99 
Required if none of the following are 
provided: 
Dollar Value of CATEGORY 1 
[[participant]]/ Shareholder 
Exchanges (Intra Fund Sell-
Side) 
B/U25 record 2, start 54 
end 69, length 16, OC 
 99,999,999,999,999.99 
Required if none of the following are 
provided: 
 
Included Reject Codes for Existing Fields 
Field Name Current Location and Requirement Description SDR 
Reject 
Code 
Registered 
Representative (RR) 
Number 
B/U24 record 2, start 21, end 29, 
length 9, Optional 
 20 
RR Branch B/U24 record 2, start 30, end 38, 
length 9, Optional 
 21 
RR Firm B/U24 record 2, start 39, end 46, 
length 8, Optional 
 22 
Total 
Acknowledgment 
Items 
B/U27 record 1, start 57, end 65, 
length 9, Required 
999,999,999 
Number of record type 22 with sequence 01 
within this group (Zero Allowed) 
88 
Total Reject Items B/U27 record 1, start 66, end 74, 
length 9, Required 
999,999,999 
Number of record type 23 with sequence 01 
within this group (Zero Allowed). 
89 
Total Detail Items B/U27 record 1, start 75, end 83, 
length 9, Required 
999,999,999 
Number of record type 24 with sequence 
01 within this group (Zeroes Allowed). 
62 
Total Summary Items B/U27 record 1, start 84, end 92, 
length 9, Required 
999,999,999 
Number of record type 25 with sequence 01 
within this group (Zeroes Allowed). 
63 
Total Records B/U27 record 1, start 93, end 101, 
length 9, Required 
999,999,999 
Total number of PHYSICAL records 
(including SDR headers and trailers) within 
this group. 
64 

---

## Page 43

Standardized Data Reporting (SDR) 
Summary of changes – effective Q4, 2011 43 
 
New Reject Codes 
The following reject code has been added: 
A2 = Plan [[ID]] Requested is Closed 
A3 = Requested Criteria Matched – No Transaction Activity Exists 
 
Requirement Changed for Existing Record 
Record Name Current 
Requirement 
New Requirement SDR 
Reject 
Code 
SDR Fund Request 
(F20) Record 2 of 2 
Optional Optional Conditional 
This record is required if SDR Request Type field of F20 
record 1 equals 02 (Plan Level) or 03 ([[investor]] Omnibus 
Account Level) 
94 
 

---

## Page 44

Standardized Data Reporting (SDR) 
Summary of changes – effective Q4, 2008 44 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2008 
1. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1. Underlying Firm 
Number 
SDR Request (F20) Record 1, 
start 38, end 41, length 4 
Required when Underlying Firm Indicator is provided. 
Must be a valid [[NSCC]] Number when Underlying Firm 
Indicator = ‘01’. 
SDR Header (B/U21) Record 1, 
start 38, end 41, length 4 
Required when Originator Type = ‘U’ or Underlying Firm 
Indicator is provided. 
Must be a valid [[NSCC]] Number when Originator Type = ‘U’ 
or Underlying Firm Indicator = ‘01’. 
2. Underlying Firm 
Indicator 
SDR Request (F20) Record 1, 
start 42, end 43, length 2. 
Required when Underlying Firm Number is provided. Not 
allowed otherwise. 
01 = [[NSCC]] Number 
02 = [[OTC]] Symbol 
03 = UFS 
SDR Header (B/U21) Record 1, 
start 42, end 43, length 2. 
Required when Underlying Firm Number is provided. Not 
allowed otherwise. 
01 = [[NSCC]] Number 
02 = [[OTC]] Symbol 
03 = UFS 
Must equal ‘01’ when Originator Type = ‘U’. 
SDR Summary (B/U25) Record 
1, start 119, end 120, length 2. 
Required when Underlying Firm Number is provided. Not 
allowed otherwise. 
01 = [[NSCC]] Number 
02 = [[OTC]] Symbol 
03 = UFS 

---

## Page 45

Standardized Data Reporting (SDR) 
Summary of changes – effective Q4, 2008 45 
Field Name Location Modified requirement 
3. Dollar Value of ALL 
[[participant]]/ Shareholder 
Buys 
SDR Summary (B/U25) Record 
1, start 35, end 50, length 16 
Required if all the following are not provided: 
- Dollar Value of ALL [[participant]]/Shareholder Sells; 
- Dollar Value of CATEGORY 1 [[participant]]/Shareholder 
Buys; 
- Dollar Value of CATEGORY 1 [[participant]]/Shareholder 
Sells; 
- Dollar Value of All [[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of All [[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of Category 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Buy-Side); 
- Dollar Value of Category 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Sell-Side). 
4. Dollar Value of ALL 
[[participant]]/ Shareholder 
Sells 
SDR Summary (B/U25) Record 
1, start 51, end 66, length 16 
Required if all the following are not provided: 
- Dollar Value of ALL [[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 [[participant]]/Shareholder 
Sells; 
- Dollar Value of CATEGORY 1 [[participant]]/Shareholder 
Buys; 
- Dollar Value of All [[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of All [[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of Category 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Buy-Side); 
- Dollar Value of Category 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Sell-Side). 
5. Dollar Value of 
CATEGORY 1 
[[participant]]/ Shareholder 
Buys 
SDR Summary (B/U25) Record 
1, start 67, end 82, length 16 
Required if all the following are not provided: 
- Dollar Value of ALL [[participant]]/ Shareholder Buys; 
- Dollar Value of ALL [[participant]]/Shareholder Sells; 
- Dollar Value of CATEGORY 1 [[participant]]/Shareholder 
Sells; 
- Dollar Value of All [[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of All [[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of Category 1 [[participant]]/Shareholder 
Exchanges (Intra-Fund Buy-Side); 
- Dollar Value of Category 1 [[participant]]/Shareholder 
Exchanges (Intra-Fund Sell-Side). 

---

## Page 46

Standardized Data Reporting (SDR) 
Summary of changes – effective Q4, 2008 46 
Field Name Location Modified requirement 
6. Dollar Value of 
CATEGORY 1 
[[participant]]/ Shareholder 
Sells 
SDR Summary (B/U25) Record 
1, start 83, end 98, length 16 
Required if all the following are not provided: 
- Dollar Value of ALL [[participant]]/ Shareholder Sells; 
- Dollar Value of ALL [[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 [[participant]]/Shareholder 
Buys; 
- Dollar Value of ALL [[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of ALL [[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Buy-Side); 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Sell-Side). 
7. Dollar Value of ALL 
[[participant]]/Shareholder 
Exchanges (Intra-Fund 
Buy-Side); 
SDR Summary (B/U25) Record 
2, start 6, end 21, length 16 
Required if all the following are not provide d: 
- Dollar Value of ALL [[participant]]/Shareholder Sells; 
- Dollar Value of ALL [[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Buys; 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Sells; 
- Dollar Value of ALL [[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of CATEGORY 1 [[participant]]/Shareholder 
Exchanges (Intra-Fund Buy-Side); 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Sell-Side). 
8. Dollar Value of ALL 
[[participant]]/Shareholder 
Exchanges (Intra-Fund 
Sell-Side) 
SDR Summary (B/U25) Record 
2, start 22, end 37, length 16 
Required if all the following are not provided: 
- Dollar Value of ALL [[participant]]/Shareholder Sells; 
- Dollar Value of ALL [[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Buys; 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Sells; 
- Dollar Value of ALL [[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Buy-Side); 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Sell-Side). 

---

## Page 47

Standardized Data Reporting (SDR) 
Summary of changes – effective Q4, 2008 47 
Field Name Location Modified requirement 
9. Dollar Value of 
CATEGORY 1 
[[participant]]/Shareholder 
Exchanges (Intra-Fund 
Buy-Side) 
SDR Summary (B/U25) Record 
2, start 38, end 53, length 16 
Required if all the following are not provided: 
- Dollar Value of ALL [[participant]]/Shareholder Sells; 
- Dollar Value of ALL [[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Buys; 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Sells; 
- Dollar Value of ALL [[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of ALL [[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Sell-Side). 
10. Dollar Value of 
CATEGORY 1 
[[participant]]/Shareholder 
Exchanges (Intra-Fund 
Sell-Side) 
SDR Summary (B/U25) Record 
2, start 54, end 69, length 16 
Required if all the following are not provided: 
- Dollar Value of ALL [[participant]]/Shareholder Sells; 
- Dollar Value of ALL [[participant]]/Shareholder Buys; 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Buys; 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Sells; 
- Dollar Value of ALL [[participant]]/Shareholder Exchanges 
(Intra-Fund Buy-Side); 
- Dollar Value of ALL [[participant]]/Shareholder Exchanges 
(Intra-Fund Sell-Side); 
- Dollar Value of CATEGORY 1 [[participant]] /Shareholder 
Exchanges (Intra-Fund Buy-Side). 
 
2. New Reject Codes 
The following reject codes have been added: 
• 99 = Firm is Not [[Member]] of SDR service 
• A0 = Fund is Not [[Member]] of SDR service 
• A1 = Underlying Firm is Not [[Member]] of SDR service 

---

## Page 48

Standardized Data Reporting (SDR) 
Summary of changes – effective Q2, 2007 48 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2007 
1. New Fields Added 
The following new fields have been added: 
Field Name Location Description 
1. Unit Value Indicator SDR Detail (B/U24) 
Record 1, start 123, end 123, length 1 
0 or Space = [[shares]]  
1 = Units 
2. Source System [[ID]] SDR Detail (B/U24) 
Record 1, start 124, end 133, length 10 
 
3. Customer Level Account 
Number 
SDR Detail (B/U24) 
Record 2, start 121, end 150, length 30 
 
 
2. New Values to Existing Fields 
New values have been added to the following fields: 
Field Name Location New Values 
1. Transaction Code SDR Detail (B/U24) 
Record 1, start 47, end 48, length 2 
60 = Credits  
61 = Free Look 
62 = Annuitization 
63 = Reversals 
2. Transaction Source SDR Detail (B/U24) 
Record 2, start 20, end 20, length 1 
4 = Record keeper or  
Insurance Carrier 
 
3. Requirements Changed for Existing Fields 
Requirements have been changed for the following fields: 
Field Name Location Modified requirement 
1. Dollar Amount SDR Detail (B/U24) 
Record 1, start 50, end 65, length 16 
Optional if Transaction Type = 05 or 
06 , or if Transaction Code = 7 or 52 
2. Price SDR Detail (B/U24) 
Record 1, start 80, end 91, length 12 
Optional if Transaction Type = 05 or 
06 , or if Transaction Code = 7 or 52 

---

## Page 49

Standardized Data Reporting (SDR) 
Summary of changes – effective Q2, 2007 49 
Field Name Location Modified requirement 
3. Dollar Value of ALL 
[[participant]]/ Shareholder 
Buys 
SDR Summary (B/U 25) 
Record 1, start 35, end 50, length 16 
Required if all the following are not provided: 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys 
- Dollar Value of ALL [[participant]]/Shareholder Sells 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Sells 
4. Dollar Value of ALL 
[[participant]]/ Shareholder 
Sells 
SDR Summary (B/U25) 
Record 1, start 51, end 66, length 16 
Required if all the following are not provided: 
- Dollar Value of CATEGORY 1 [[participant]]/ 
Shareholder Sells 
- Dollar Value of ALL [[participant]]/Shareholder Buys 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys 
5. Dollar Value of 
CATEGORY 1 [[participant]]/ 
Shareholder Buys 
SDR Summary (B/U25) 
Record 1, start 67, end 82, length 16 
Required if all the following are not provided: 
- Dollar Value of ALL [[participant]]/ Shareholder 
Buys 
- Dollar Value of ALL [[participant]]/Shareholder Sells 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Sells 
6. Dollar Value of 
CATEGORY 1 [[participant]]/ 
Shareholder Sells 
SDR Summary (B/U25) 
Record 1, start 83, end 98, length 16 
Required if all the following are not provided: 
- Dollar Value of ALL [[participant]]/ Shareholder 
Sells 
- Dollar Value of ALL [[participant]]/Shareholder Buys 
- Dollar Value of CATEGORY 1 
[[participant]]/Shareholder Buys 
 
4. New Reject Codes 
The following reject code has been added: 
• 98 = Unit Value Indicator invalid

---

## Page 50

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: November 8, 2023 
Publication Code: MFS336 
Service: Networking 
Title: Standardized Data Reporting (SDR) 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 