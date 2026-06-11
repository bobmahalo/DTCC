---
title: "Non-ISO Fixed Length Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps1_NON_ISO_fixed_layouts_mfs176_20201123.pdf"
pages: 29
size: "496.1 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Non-ISO Fixed Length Record Layouts

**Original File:** [mfps1_NON_ISO_fixed_layouts_mfs176_20201123.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps1_NON_ISO_fixed_layouts_mfs176_20201123.pdf)  
**Category:** Other  
**Total Pages:** 29  
**File Size:** 496.1 KB  

---

## Page 1

  
 
 
MUTUAL FUND PROFILE SERVICE I 
NON-ISO FIXED LENGTH RECORD LAYOUTS 
OCTOBER 30, 2020 
 
 


---

## Page 2

 
 
© 2020 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: October 30, 2020 
Publication Code: MFS176 
Service: Mutual Fund Profile Service I 
Title: Non-ISO Fixed Length Record Layouts 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
History of Important Notices Type ..................................................................................................................... 4 
Summary of Changes .......................................................................................................................................... 5 
Effective Q4, 2020 .............................................................................................................................................. 5 
Effective Q1, 2019 .............................................................................................................................................. 7 
Effective Q1, 2017 .............................................................................................................................................. 7 
Effective Q3, 2016 .............................................................................................................................................. 7 
Effective Q2, 2013 ............................................................................................................................................ 10 
Effective Q2, 2011 ............................................................................................................................................ 10 
Introduction ........................................................................................................................................................ 11 
Fixed Length Format .......................................................................................................................................... 12 
Record Layouts .................................................................................................................................................. 13 
Notes: ................................................................................................................................................................ 13 
Price/Rate Record (030) ..................................................................................................................................... 16 
Record 1 of 4 .................................................................................................................................................... 16 
Record 2 of 4 .................................................................................................................................................... 19 
Record 3 of 4 .................................................................................................................................................... 22 
Record 4 of 4 .................................................................................................................................................... 23 
[[NSCC]] Output Header Record (000) .................................................................................................................. 25 
Record 1 of 1 .................................................................................................................................................... 25 
Trailer Record (999) ........................................................................................................................................... 26 
Record 1 of 1 .................................................................................................................................................... 26 
Datatrak Header .................................................................................................................................................. 27 
Record 1 of 1 .................................................................................................................................................... 27 
Datatrak Trailer ................................................................................................................................................... 28 
Record 1 of 1 .................................................................................................................................................... 28 
 

---

## Page 4

Non-ISO Fixed Length Record Layouts 
History of Important Notices Type 4 
[[DTCC]] Internal (Green) 
HISTORY OF IMPORTANT NOTICES TYPE  
Effective Date: November 23, 2020  Important Notice a8917, P&S 8490 Dated October 19, 2020 
July 31, 2020  Document rebranded  
Effective Date: March 25, 2019 Important Notice a8658, P&S 8233 Dated December 19, 2018 
Documentation Changes Important Notice a8354, P&S 7929 Dated March 22, 2017 
Effective Date: September 26, 2016 Important Notice a8159, P&S 7734 Dated Feb 3, 2016 
Effective Date: May 24, 2013 Important Notice a7587, P&S 7157 Dated Feb 15, 2013 
Effective Date: May 31, 2011 Important Notice a7156, P&S 6726 Dated Feb 7, 2011 
 

---

## Page 5

Non-ISO Fixed Length Record Layouts 
Summary of Changes 5 
[[DTCC]] Internal (Green) 
SUMMARY OF CHANGES  
Effective Q4, 2020 
 
1. Price/Rate layout – Record 2 of 4 
 
a. Added new fields: 
 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Negative Rate 
Correction Indicator 
 
(effective 11/23/20) 
51 51 1 A/N Space = Negative Rate not 
provided 
 
1 = Original Negative Rate 
2 = Correction to Negative Rate 
O 0407 
Negative Rate  
 
(effective 11/23/20) 
 
 
 
52  64  13 N 9,999.999999999  
 
Required and must be greater than 
zero when ‘Negative Rate 
Correction Indicator’ = 1. 
 
Required (but allowed to be zero) if 
‘Negative Rate Correction 
Indicator’ = 2. 
 
Not allowed if Negative Rate 
Correction Indicator = space. 
OC 0408 
 
b. Field description requirement changes: 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Rate Correction 
Indicator 
8 8 1 A/N Space = Rate not provided 
 
1 = Original Rate 
2 = Correction to Rate 
 
Required when ‘Negative Rate 
Correction Indicator’ = 1 (Original 
Negative Rate). 
(effective 11/23/20) 
(see Record Layouts Note 6c) 
OC 0084 

---

## Page 6

Non-ISO Fixed Length Record Layouts 
Summary of Changes 6 
[[DTCC]] Internal (Green) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Rate 
 
 
 
9 26 18 N 999,999,999.999999999 
 
Required (but allowed to be zero) if 
Rate Correction Indicator = 1 or 2. 
Not allowed if Rate Correction 
Indicator = space. 
 
Required and must be = 0 when 
‘Negative Rate Correction 
Indicator’ is populated with a 1 
(Original Negative Rate). 
(effective 11/23/20) 
 
For JPY Currency only, each of the 
last nine positions must be populated 
with a value of 0. 
Example: A Rate of JPY 111 should 
be entered as 
000000111000000000. 
OC 0086 
Daily [[Dividend]] Day 
Count 
 
 
27 29 3 N 999 
Required if Rate Correction Indicator 
= 1 or 2 and Distribution Type = ‘6’. 
 
Required if Negative Rate 
Correction Indicator = 2, and 
Distribution Type = ‘6’. 
(effective 11/23/20) 
 
Not allowed otherwise 
OC 0055 
 
c. Added new Reject Codes: 
 
Reject Code Description 
0407 Negative Rate Correction Indicator is missing/invalid 
0408 Negative Rate is missing/invalid 
 
 

---

## Page 7

Non-ISO Fixed Length Record Layouts 
Summary of Changes 7 
[[DTCC]] Internal (Green) 
Effective Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
0388 [[participant]] is not valid for the Submitter and/or Product 
Effective Q1, 2017 
1. Price/Rate Record 30 layout  
 
a. Documentation Change – Modify Field Descriptions: 
 
1. Originator Type (sequence 1, start 5, end 5, length 1) 
 Current Requirement: Required 
A = [[NASD]] 
F = Fund 
 New Requirement: Required 
F = Fund 
Effective Q3, 2016 
1. Price/Rate layout  
 
a. Field description requirement change: 
 
1. Price Correction Indicator (sequence 01, start 45, and end 45, length 1) 
 Current Requirement: Optional/Required. 
Space = Price not provided 
1 = Original Price 
2 = Correction Price 
(See Record Layouts Note 6.) 
 New Requirement: Optional/Required  
Space = Price not provided 
1 = Single NAV Fund-Original Price 
2 = Single NAV Fund–Correction to Price 
(See Record Layouts Note 6a) 
3 = Multiple NAVs Fund–Original Price 
4 = Multiple NAVs Fund–Correction to Price 

---

## Page 8

Non-ISO Fixed Length Record Layouts 
Summary of Changes 8 
[[DTCC]] Internal (Green) 
(See Record Layouts Note 6b) 
2. Price (NAV) (sequence 01, start 46, end 63, length 18) 
 Current Requirement: Required if Price Correction Indicator = 1 or 2. 
Not allowed if Price Correction Indicator = space. 
 
For JPY Currency only, each of the last nine positions Must be 
populated with a value 0f 0. 
Example: A Price of JPY 111 should be entered as 
00000011100000000. 
 New Requirement: Required if Price Correction Indicator = 1, 2, 3, or 4. 
Not allowed if Price Correction Indicator = space. 
 
For JPY Currency only, each of the last nine positions Must be 
populated with a value 0f 0. 
Example: A Price of JPY 111 should be entered as 
00000011100000000. 
 
b. Field description change: 
 
1. Effective Date (sequence 01, start 37, end 44, length 8) 
 Current Description: ccyymmdd 
If Price is provided, must be valid business day and cannot be 
future date. 
If only Rate and/or Cumulative Rate are provided, can be any 
calendar date 
 New Description: ccyymmdd 
If Price is provided: 
If Price is provided, must be valid business day and cannot be 
future dated. 
Effective Date of the price. 
Multiple NAVs Fund–this is the Price strike date. 
For example, if the fund provides a price at 12pm on 9/10/15, 
the “Effective Date” of this price will be “20150910”. 
If Rate is provided: 
If only Rate and/or Cumulative Rate are provided, can be any 
calendar date. 
 
  

---

## Page 9

Non-ISO Fixed Length Record Layouts 
Summary of Changes 9 
[[DTCC]] Internal (Green) 
c. Add New Optional Conditional Sequence 04 to Existing Records 
 
Sequence 04 is required if Price Correction Indicator is ‘3 = Multiple NAVs Fund–Original Price’ or ‘4 = Multiple 
NAVs Fund–Correction to Price’. 
Sequence 04 is not allowed if Price Correction Indicator is Space, ‘1 = Single NAV Fund-Original Price’, ‘2 = 
Single NAV Fund–Correction to Price. 
Sequence 04 contains the new data fields. 
1. Price (NAV) Start Time (start 8, end 13, length 6) 
 Requirement: Optional Conditional 
hhmmss Eastern Time 
The start time of the price is 1 (one) second after the 
previous price was provided. For example, the fund may 
strike a price three times a day: 9am, 12pm and 3pm. The 
“Price (NAV) Start Time” of the 12pm price will be “090001” 
(9:00:01am). 
Similarly, the “Price (NAV) Start Time” of the 9am price will 
be “150001” (3:00:01pm) since the previous price was 
calculated at 3pm on the previous day. 
Required when Price Correction Indicator = ‘3’ or ‘4’. 
Not allowed if “Price Correction Indicator” is 1, 2 or space 
(blank). 
2 Price (NAV) Start Date (start 14, end 21, length 8) 
 Requirement: Optional Conditional 
Ccyymmdd 
Date of the price start time. For example, if the fund strikes a 
price at 12pm on 9/10/15, the “Price (NAV) Start Date” will be 
“20150910”. If the fund strikes a price at 3pm on 9/9/15 and 
the next one at 9am on 9/10/15, the “Price (NAV) Start Date” 
of the 9am price will be “20150909” (9/9/2015). 
Must be a valid business date. 
Must be on or before “Effective Date”. 
Required when Price Correction Indicator = ‘3’ or ‘4’. 
Not allowed if “Price Correction Indicator” is 1, 2 or space 
(blank). 
3 Price (NAV) Strike Time (start 22, end 27, length 6) 
 Requirement: Optional Conditional 
hhmmss Eastern Time 
This field must contain the strike time of the price. For 
example, if the fund strikes a price at 3pm, the “Price (NAV) 
Strike Time” will be “150000” (3pm). 
Required when Price Correction Indicator = ‘3’ or ‘4’. 

---

## Page 10

Non-ISO Fixed Length Record Layouts 
Summary of Changes 10 
[[DTCC]] Internal (Green) 
Not allowed if “Price Correction Indicator” is 1, 2 or space 
(blank). 
4 Price (NAV) Indicator (start 28, end 29, length 2) 
 Requirement: Optional Conditional 
Numeric 
The value in this field will indicate whether a particular price 
is the 1st, 2nd, etc. price of the day. 
Valid Values: 01–99 
Zero (0) is not a valid value. 
Required when Price Correction Indicator = ‘3’ or ‘4’. 
Not allowed if “Price Correction Indicator” is 1, 2 or space 
(blank). 
Effective Q2, 2013 
2. Price/Rate layout – Record 1 of 3 
 
a. Field description requirement change: 
 
1. Currency Indicator (start 64, end 66, length 3) 
 Current Requirement: Required. 
USD, EUR and GBP 
 New Requirement: Required. 
USD, EUR, GBP, AUD, CAD, CHF, CNY, HKD, JPY, NOK, SEK 
and SGD 
Effective Q2, 2011 
1. Price/Rate layout – Record 1 of 3 
 
a. Field description requirement change: 
 
1. Currency Indicator (start 64, end 66, length 3) 
 Current Requirement: Required. 
USD 
 New Requirement: Required. 
USD, EUR or GBP 

---

## Page 11

Non-ISO Fixed Length Record Layouts 
Introduction 11 
[[DTCC]] Internal (Green) 
INTRODUCTION 
Some of the features of the Mutual Fund Profile Service (MFPS) [[NSCC]] (non-ISO) records layout features are: 
1. Records can be received or submitted in either of two formats: fixed length or variable length. 
2. Data received or submitted interactively (via MQM) must be in variable length format. 
3. This document describes the MFPS [[NSCC]] (non-ISO) fixed length record layouts. 

---

## Page 12

Non-ISO Fixed Length Record Layouts 
Fixed Length Format 12 
[[DTCC]] Internal (Green) 
FIXED LENGTH FORMAT 
Each fixed length transaction consists of one or more 80-byte long records. 
Each 80-byte long record starts with the following two fields: 
1. Physical Sequence Number (bytes 1-2) 
2. Logical Sequence Number (bytes 3-4) 
 
The physical sequence number of the first record in a submitted transaction must be 01 and should increase by 
one from record to record within the transaction. 
The physical sequence number of the last record in a submitted transaction must start with 9. 
The logical sequence numbers within a submitted transaction must be in ascending order and cannot exceed 
the maximum allowed for that transaction (see record layouts). 
Example: The following are valid sequence numbers for Price/Rate transactions: 0101 9203 
Notes: 
1. The last physical sequence number is 92 (rather than 02) to indicate that it is the last physical record of this Price/Rate 
transaction. 
2. Logical sequence number 02 (optional record) is not included in this Price/Rate transaction. 

---

## Page 13

Non-ISO Fixed Length Record Layouts 
Record Layouts 13 
[[DTCC]] Internal (Green) 
RECORD LAYOUTS 
The following record types will be used by MFPS and are detailed in this document: 
000-[[NSCC]] Output Header 
030-Price and Rate 
999-Trailer 
Also detailed in this document are Datatrak Header, Datatrak Trailer and MFPS reject code list. 
The column headings in this document are as follows: 
Start The position where the field starts. 
End The position where the field ends. 
Len The length of the field in bytes 
Type The type of the field: 
A/N = Alphanumeric 
N = Numeric 
Field Name The name of the field. 
Description Field description (format, valid values, conditional requirements, etc.). 
Opt/Req Indicates whether the field is optional or required: 
O = Optional 
R = Required 
OC = Generally optional, but required upon specified conditions 
RC = Generally required, but optional upon specified conditions 
Reject Code The reject code which indicates that this field is invalid. 
 
Notes: 
1. Alphanumeric type fields may include any character in the computer character set but should not include 
unprintable characters such as Low-Value, High-Value, Comp-3 fields, etc., since these kinds of 
characters may cause problems during transmission time. 
2. Numeric type fields may include digits (0-9) only. 
3. Required fields mean the following: 
a. Fields with specified list of values must have one of those values. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first 
note above but must not be spaces. 
c. Numeric type fields without a specified list of values must be numeric greater than zero. 

---

## Page 14

Non-ISO Fixed Length Record Layouts 
Record Layouts 14 
[[DTCC]] Internal (Green) 
d. Fields with other requirements must follow those requirements (for example Firm Number must be 
valid and eligible for MFPS). 
4. Optional fields mean the following: 
a. Fields with specified list of values must have one of those values or space. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first 
note above. 
c. Numeric type fields without specified list of values must be numeric or space. 
d. Fields with other requirements must follow those requirements or may be space (for example Fund 
Number must be valid and eligible for Fund/SERV or may be space) 
5. All dates in the layouts have the format ccyymmdd (except where otherwise indicated) where: 
cc = Century 
yy = Year in century 
mm = Month 
dd = Day in month 
Examples: 
June 8, 2006 is represented as: 20060608 
December 14, 2006 is represented as: 20061214 
6. Handling multiple Prices/Rates: 
 
6a Price (NAV)-Single NAV Fund 
A fund might submit an original price and one/multiple price corrections within the same cycle for the 
same Security Issue [[ID]] and Effective Date. In this scenario only the latest price correction received 
during this cycle will be distributed by [[NSCC]] (the original price will not be distributed). As a result, 
clients may receive a correction to price without previously receiving the original price. Clients should 
treat this price correction as the latest most up-to-date* price for the same combination of Security 
Issue [[ID]] and Effective Date. 
Note* 
A fund might submit another price correction (or multiple corrections) for the same combination of Security Issue [[ID]] and 
Effective Date in a subsequent cycle. The latest price correction will be distributed in the cycle it was received. 
6b Price (NAV)–Multiple NAVs Fund 
A fund might submit an original price and one/multiple price corrections within the same cycle for the 
same Security Issue [[ID]], Effective Date and Price (NAV) Indicator. In this scenario only the latest price 
correction received during this cycle will be distributed by [[NSCC]] (the original price will not be 
distributed). As a result, clients may receive a correction to price without previously receiving the 
original price. Clients should treat this price correction as the latest most up-to-date* price for the same 
combination of Security Issue [[ID]], Effective Date and Price (NAV) Indicator. 

---

## Page 15

Non-ISO Fixed Length Record Layouts 
Record Layouts 15 
[[DTCC]] Internal (Green) 
Note* 
A fund might submit another price correction (or multiple corrections) for the same combination of Security Issue [[ID]], 
Effective Date and Price (NAV) Indicator in a subsequent cycle. The latest price correction will be distributed in the cycle it 
was received. 
6c [[Dividend]] Rate 
A fund might submit an original [[Dividend]] rate and one/multiple [[Dividend]] rate corrections within the 
same cycle for the same Security Issue [[ID]], Effective Date, Distribution Type and Distribution Indicator. 
In this scenario only the latest [[Dividend]] rate correction received during this cycle will be distributed by 
[[NSCC]] (the original [[Dividend]] rate will not be distributed). As a result, clients may receive a correction to 
[[Dividend]] rate without previously receiving the original [[Dividend]] rate. Clients should treat this [[Dividend]] 
rate correction as the latest most up-to-date* [[Dividend]] rate for the same combination of Security Issue 
[[ID]], Effective Date, Distribution Type and Distribution Indicator. 
Note* 
A fund might submit another [[Dividend]] rate correction (or multiple corrections) for the same combination of Security Issue [[ID]], 
Effective Date, Distribution Type and Distribution Indicator in a subsequent cycle. The latest [[Dividend]] rate correction will be 
distributed in the cycle it was received. 
6d Cumulative Rate 
A fund might submit an original cumulative rate and one/multiple cumulative rate corrections within the 
same cycle for the same Security Issue [[ID]] and Effective Date. In this scenario only the latest 
cumulative rate correction received during this cycle will be distributed by [[NSCC]] (the original 
cumulative rate will not be distributed). As a result, clients may receive a correction to cumulative rate 
without previously receiving the original cumulative rate. Clients should treat this cumulative rate 
correction as the latest most up-to-date* cumulative rate for the same combination of Security Issue [[ID]] 
and Effective Date. 
Note* 
A fund might submit another cumulative rate correction (or multiple corrections) for the same combination of Security Issue 
[[ID]] and Effective Date in a subsequent cycle. The latest cumulative rate correction will be distributed in the cycle it was 
received. 
(Modified Q3, 2016) 

---

## Page 16

Non-ISO Fixed Length Record Layouts 
Price/Rate Record (030) 16 
[[DTCC]] Internal (Green) 
PRICE/RATE RECORD (030) 
Record 1 of 4 
Required 
Price/Rate Record (030) Record 1 of 4 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 01 R 0080 
Originator Type 5 5 1 A/N F = Fund R 0081 
Security Issue Symbol 
Indicator 
6 6 1 A/N Required if Security Issue Symbol is 
provided. 
N = [[NASD]] 
P = Proposed 
OC 0400 
Filler 7 7 1 A/N Space R  
Profile Type 8 9 2 A/N 01 = Price/Rate R 0082 
Record Type 10 12 3 A/N 030 = Price/Rate R 0083 
Submitting [[participant]] 
Number 
13 16 4 A/N Input: Submitting [[participant]] number 
Output: 
To Price/Rate recipient: [[NSCC]] 
To Price/Rate submitter: 
Submitting [[participant]] number 
R 0059 
Security Issue 
Country Code 
17 18 2 A/N  R 0040 
Security Issue [[ID]] 19 27 9 A/N  R 0040 
Security Issue Check 
Digit 
28 28 1 A/N  R 0041 
Submission Date 29 36 8 N ccyymmdd R 0036 

---

## Page 17

Non-ISO Fixed Length Record Layouts 
Price/Rate Record (030) 17 
[[DTCC]] Internal (Green) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Effective Date 37 44 8 N ccyymmdd 
If Price is provided 
If Price is provided, must be a valid 
business day and cannot be future 
dated. 
Effective Date of the Price. 
Multiple NAVs Fund–this is the Price 
strike date. For example, if the fund 
provides a price at 12pm on 9/10/15, 
the ”Effective Date” of this price will 
be “20150910”. 
If Rate is provided 
If only Rate and/or Cumulative Rate 
are provided, can be any calendar 
date 
 
R 0044 
Price Correction 
Indicator 
45 45 1 A/N Space = Price not provided 
1 = Single NAV Fund-Original Price 
2 = Single NAV Fund–Correction to 
Price (see Record Layouts Note 6a) 
3 = Multiple NAVs Fund–Original 
Price 
4 = Multiple NAVs Fund–Correction 
to Price (see Record Layouts Note 
6b) 
 
O 0084 
Price (NAV) 46 63 18 N 999,999,999.999999999 
Required if Price Correction Indicator 
= 1, 2, 3, or 4. 
Not allowed if Price Correction 
Indicator = space. 
For JPY Currency only, each of the 
last nine positions must be populated 
with a value of 0. 
Example: A Price of JPY 111 should 
be entered as 000000111000000000 
OC 0085 
Currency Indicator 64 66 3 A/N USD, EUR, GBP, AUD, CAD, CHF, 
CNY, HKD, JPY, NOK, SEK or SGD 
R 0087 
Test Indicator 67 67 1 A/N Space = Production 
1 = Test 
R 0089 
Security Issue Symbol 68 75 8 A/N Required if Security Issue Symbol 
Indicator is provided 
OC 0401 

---

## Page 18

Non-ISO Fixed Length Record Layouts 
Price/Rate Record (030) 18 
[[DTCC]] Internal (Green) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
[[NSCC]] Rejection 
Indicator 
76 76 1 A/N Input: Space 
Output: 
To Price/Rate recipient: 
0 = Accepted 
To Price/Rate submitter: 
1 = Record rejected 
2 = Price accepted, Rate or 
Cumulative Rate rejected 
3 = Price rejected, Rate or 
Cumulative Rate accepted 
R  
[[NSCC]] Reject Code 1 77 80 4 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 19

Non-ISO Fixed Length Record Layouts 
Price/Rate Record (030) 19 
[[DTCC]] Internal (Green) 
Record 2 of 4 
Optional 
Price/Rate Record (030) Record 2 of 4 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 02 R 0080 
Filler 5 7 3 A/N Space R  
Rate Correction 
Indicator 
8 8 1 A/N Space = Rate not provided 
 
1 = Original Rate 
2 = Correction to Rate 
 
Required when ‘Negative Rate 
Correction Indicator’ = 1 (Original 
Negative Rate). 
(effective 11/23/20) 
(see Record Layouts Note 6c) 
OC 0084 
Rate 
 
 
 
9 26 18 N 999,999,999.999999999 
 
Required (but allowed to be zero) if 
Rate Correction Indicator = 1 or 2. 
Not allowed if Rate Correction 
Indicator = space. 
 
Required and must be = 0 when 
‘Negative Rate Correction 
Indicator’ is populated with a 1 
(Original Negative Rate). 
(effective 11/23/20) 
 
For JPY Currency only, each of the 
last nine positions must be populated 
with a value of 0. 
Example: A Rate of JPY 111 should 
be entered as 
000000111000000000. 
OC 0086 

---

## Page 20

Non-ISO Fixed Length Record Layouts 
Price/Rate Record (030) 20 
[[DTCC]] Internal (Green) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Daily [[Dividend]] Day 
Count 
 
 
27 29 3 N 999 
Required if Rate Correction Indicator 
= 1 or 2 and Distribution Type = ‘6’. 
 
Required if Negative Rate 
Correction Indicator = 2, and 
Distribution Type = ‘6’. 
(effective 11/23/20) 
 
Not allowed otherwise. 
OC 0055 
Rate Rejection 
Indicator 
30 30 1 A/N Applies only if [[NSCC]] Rejection 
Indicator = 2 or 3. 
Input: Space 
Output: 
Space = N/A 
0 = Rate accepted by [[NSCC]] 
1 = Rate rejected by [[NSCC]] 
R  
Cumulative Rate 
Correction Indicator 
31 31 1 A/N Space = Cumulative Rate not 
provided 
1 = Original Cumulative Rate 
2 = Correction to Cumulative Rate  
 
(see Record Layouts Note 6d) 
O 0402 
Cumulative Rate 32 44 13 N 9,999.999999999 
Required (but allowed to be zero) if 
Cumulative Rate Correction Indicator 
= 1 or 2. 
 
Not allowed if Cumulative Rate 
Correction Indicator = space. 
 
For JPY Currency only, each of the 
last nine positions must be populated 
with a value of 0. 
Example: A Cumulative Rate of JPY 
111 should be entered as 
0111000000000 
OC 0403 
Cumulative Rate Day 
Count 
45 47 3 N 999 
Required if Cumulative Rate 
Correction Indicator = 1 or 2. 
Not allowed if Cumulative Rate 
Correction Indicator = space. 
OC 0404 

---

## Page 21

Non-ISO Fixed Length Record Layouts 
Price/Rate Record (030) 21 
[[DTCC]] Internal (Green) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Cumulative Rate 
Rejection Indicator 
48 48 1 A/N Applies only if [[NSCC]] Rejection 
Indicator = 2 or 3. 
Input: Space 
Output: 
Space = N/A 
0 = Cumulative Rate accepted by 
[[NSCC]] 
1 = Cumulative Rate rejected by 
[[NSCC]] 
R  
Notes: 
1: The 2 fields below (Distribution Type and Distribution Indicator), together with Security Issue and Effective Date 
constitute a unique key. A rate can be sent per Security Issue, Effective Date and any combination of these fields. 
2: If rate (non-negative or negative) is provided and both Distribution Type and Distribution Indicator are not provided, 
the record will be accepted, and the fields will be populated by Profile I as follows: Distribution Type = ‘6’, Distribution 
Indicator = ‘3’. 
 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Distribution Type 49 49 1 A/N Required if rate is provided (but see 
Note 2 above). 
Not allowed otherwise. 
1 = Short Term Capital Gain 
2 = Long Term Gain 
3 = Gain on Collectables 
4 = Section 1202 Gain 
5 = Unrecaptured Section 1250 Gain 
6 = Daily Accrual [[Dividend]] 
7 = [[Equity]] [[Dividend]] 
OC 0377 
Distribution Indicator 50 50 1 A/N Required if rate is provided (but see 
Note 2 above). 
Not allowed otherwise. 
 
1 = Spillover 
3 = Regular Distribution 
OC 0337 
Negative Rate 
Correction Indicator 
 
(effective 11/23/20) 
51 51 1 A/N Space = Negative Rate not 
provided 
 
1 = Original Negative Rate 
2 = Correction to Negative Rate 
O 0407 

---

## Page 22

Non-ISO Fixed Length Record Layouts 
Price/Rate Record (030) 22 
[[DTCC]] Internal (Green) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Negative Rate  
 
(effective 11/23/20) 
 
 
 
52  64  13 N 9,999.999999999  
 
Required and must be greater than 
zero when ‘Negative Rate 
Correction Indicator’ = 1. 
 
Required (but allowed to be zero) if 
‘Negative Rate Correction 
Indicator’ = 2. 
 
Not allowed if Negative Rate 
Correction Indicator = space. 
 
OC 0408 
[[NSCC]] Reject Code 2 65 68 4 A/N Input : Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 69 72 4 A/N Input : Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 4 73 76 4 A/N Input : Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 5 77 80 4 A/N Input : Space 
Output: Reject code or space 
R  
Record 3 of 4 
Optional 
Price/Rate Record (030) Record 3 of 4 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 03 R 0080 
Filler 5 7 3 A/N Space R  
Security Issue 
Description 
8 77 70 A/N  O  
Filler 78 80 3 A/N Space R  

---

## Page 23

Non-ISO Fixed Length Record Layouts 
Price/Rate Record (030) 23 
[[DTCC]] Internal (Green) 
Record 4 of 4 
Optional Conditional 
Sequence 04 is required if “Price Correction Indicator” is ‘3’ = Multiple NAVs Fund–Original Price, or ‘4’ = 
Multiple NAVs Fund–Correction to Price. 
Sequence 04 is not allowed if “Price Correction Indicator” is Space, ‘1’ = Single NAV Fund-Original Price, or ‘2’ 
= Single NAV Fund–Correction to Price. 
Price/Rate Record (030) Record 4 of 4 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 0080 
Logical Sequence 
Number 
3 4 2 A/N 04 R 0080 
Filler 5 7 3 A/N Space R  
Price (NAV) 
Start Time 
8 13 6 A/N hhmmss Eastern Time 
The start time of the price is 1 (one) 
second after the previous price was 
provided. For example, the fund may 
strike a price three times a day: 9am, 
12pm and 3pm. The “Price (NAV) 
Start Time” of the 12pm price will be 
“090001” (9:00:01am). Similarly, the 
“Price (NAV) Start Time” of the 9am 
price will be “150001” (3:00:01pm) 
since the previous price was 
calculated at 3pm on the previous 
day. 
Required if “Price Correction 
Indicator” = ‘3’ or ‘4’. 
Not allowed if “Price Correction 
Indicator” is 1, 2 or space (blank). 
 
OC 0770 

---

## Page 24

Non-ISO Fixed Length Record Layouts 
Price/Rate Record (030) 24 
[[DTCC]] Internal (Green) 
Field Name Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Price (NAV) 
Start Date 
14 21 8 A/N ccyymmdd 
Date of the price start time. For 
example, if the fund strikes a price at 
12pm on 9/10/15, the “Price (NAV) 
Start Date” will be “20150910”. If the 
fund strikes a price at 3pm on 9/9/15 
and the next one at 9am on 9/10/15, 
the “Price (NAV) Start Date” of the 
9am price will be “20150909” 
(9/9/2015). 
Must be a valid business date. Must 
be on or before “Effective Date”. 
Required if “Price Correction 
Indicator” = ‘3’ or ‘4’. 
Not allowed if “Price Correction 
Indicator” is 1, 2 or space (blank). 
 
OC 0771 
Price (NAV) 
Strike Time 
22 27 6 A/N hhmmss Eastern Time 
This field must contain the strike time 
of the price. For example, if the fund 
strikes a price at 3pm, the “Price 
(NAV) Strike Time” will be “150000” 
(3pm). 
Required if “Price Correction 
Indicator” = ‘3’ or ‘4’. 
Not allowed if “Price Correction 
Indicator” is 1, 2 or space (blank). 
 
OC 0772 
Price (NAV) 
Indicator 
28 29 2 N The value in this field will indicate 
whether a particular price is the 1st, 
2nd, etc. price of the day. 
Valid Values: 01–99 
Required if “Price Correction 
Indicator” = ‘3’ or ‘4’. 
Zero (0) is not a valid value. 
Not allowed if “Price Correction 
Indicator” is 1, 2 or space (blank). 
Best Practice: For the last/end of day 
NAV strike, Funds should indicate a 
value of “98”. 
 
OC 0773 
Filler 30 80 51 A/N Spaces 
 
R  

---

## Page 25

Non-ISO Fixed Length Record Layouts 
[[NSCC]] Output Header Record (000) 25 
[[DTCC]] Internal (Green) 
[[NSCC]] OUTPUT HEADER RECORD (000) 
Record 1 of 1 
Output from [[NSCC]] 
[[NSCC]] Output Header Record (000) Record 1 of 1 
Field Name Start End Len Type Description 
Physical Sequence 
Number 
1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N N = [[NSCC]] 
Filler 6 9 4 A/N Space 
Record Type 10 12 3 A/N 000 = [[NSCC]] Output Header 
Recipient Number 13 16 4 N Zero if global record, [[participant]] Number if 
specific record 
Transmission Date 17 24 8 N ccyymmdd 
Filler 25 25 1 A/N Space 
Literal 26 29 4 A/N FILE 
AutoRoute File Number 30 37 8 A/N  
AutoRoute File Cycle 38 39 2 A/N  
File Description 40 59 20 A/N MUTUAL FUND PROFILE 
Filler 60 80 21 A/N Space 

---

## Page 26

Non-ISO Fixed Length Record Layouts 
Trailer Record (999) 26 
[[DTCC]] Internal (Green) 
TRAILER RECORD (999) 
Record 1 of 1 
Required 
Trailer Record (999) Record 1 of 1 
Field Name Start End Len Type Description Opt/ 
Req 
Physical Sequence 
Number 
1 2 2 A/N  R 
Logical Sequence 
Number 
3 4 2 A/N 01 R 
Originator Type 5 5 1 A/N B = Firm 
F = Fund 
N = [[NSCC]] 
T = TPA 
R 
Filler 6 9 4 A/N Space R 
Record Type 10 12 3 A/N 999 = Trailer R 
[[participant]] Number 13 16 4 N Input : Submitting [[participant]] Number 
Output: Zero if global record, receiving 
[[participant]] Number if specific record 
R 
Submission Date 17 24 8 N ccyymmdd R 
Total Price/Rate 
Transactions 
25 30 6 N 999,999 R 
Filler 31 74 44 A/N Space R 
Total Other Transactions 75 80 6 N 999,999 R 

---

## Page 27

Non-ISO Fixed Length Record Layouts 
Datatrak Header 27 
[[DTCC]] Internal (Green) 
DATATRAK HEADER 
Record 1 of 1 
Required. This is the first record in any file submitted to MFPS through Datatrak. 
Datatrak Header Record 1 of 1 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N HDR.S R 
File [[ID]] 6 10 5 A/N 32344 R 
Literal 11 16 6 A/N .E00.C R 
Originator [[ID]] 17 20 4 A/N  R 
Literal 21 22 2 A/N .S R 
Sub Originator [[ID]] 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N MUTUAL FUND PROFILE R 
Multibatch Last Batch 
Indicator 
60 60 1 A/N N = Not last batch 
Y = Last batch 
R 
Multibatch Batch 
Counter 
61 63 3 N  R 
Filler 64 80 17 A/N Space R 

---

## Page 28

Non-ISO Fixed Length Record Layouts 
Datatrak Trailer 28 
[[DTCC]] Internal (Green) 
DATATRAK TRAILER 
Record 1 of 1 
Required. This is the last record in any file submitted to MFPS through Datatrak. 
Datatrak Trailer Record 1 of 1 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N END.S R 
File [[ID]] 6 10 5 A/N 32344 R 
Literal 11 16 6 A/N .E00.C R 
Originator [[ID]] 17 20 4 A/N  R 
Literal 21 22 2 A/N .S R 
Sub Originator [[ID]] 23 26 4 A/N  R 
Total Records 27 33 7 N 9,999,999 
Total # of records in file excluding 
Datatrak header and trailer 
R 
Filler 34 80 47 A/N Space R 
 

---

## Page 29

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 