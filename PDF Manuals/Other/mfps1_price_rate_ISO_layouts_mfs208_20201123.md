---
title: "MFPSI - Price & Rate ISO Formatted Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps1_price_rate_ISO_layouts_mfs208_20201123.pdf"
pages: 56
size: "726.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPSI - Price & Rate ISO Formatted Record Layouts

**Original File:** [mfps1_price_rate_ISO_layouts_mfs208_20201123.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps1_price_rate_ISO_layouts_mfs208_20201123.pdf)  
**Category:** Other  
**Total Pages:** 56  
**File Size:** 726.6 KB  

---

## Page 1

 
 
 
MUTUAL FUND PROFILE SERVICE I 
PRICE AND RATE ISO FORMATTED RECORD LAYOUTS 
OCTOBER 30, 2020 
 


---

## Page 2

 
 
Copyright© © 2020 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. 
TOGETHER, and the Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing 
Corporation. 
  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Info: October 30, 2020 
Publication Code: MFS208 
Service: Mutual Fund Profile Service I 
Title: Price and Rate ISO Formatted Record Layouts 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 5 
Summary of Changes .......................................................................................................................................... 6 
Effective Q4, 2020 .............................................................................................................................................. 6 
Effective Q1, 2019 ............................................................................................................................................ 13 
Effective Q1, 2017 ............................................................................................................................................ 13 
Effective Q3, 2016 ............................................................................................................................................ 15 
Effective Q2, 2013 ............................................................................................................................................ 24 
Effective Q2, 2011 ............................................................................................................................................ 25 
Introduction ........................................................................................................................................................ 26 
Header and Trailer Blocks ................................................................................................................................. 27 
Block 1 - [[BASIC]] Header ..................................................................................................................................... 27 
Block 2 - Application Header ............................................................................................................................ 28 
Block 3 - User Header ...................................................................................................................................... 30 
Block 5 - Trailer ................................................................................................................................................. 30 
Block 4 – Messages Text ................................................................................................................................... 32 
Message Types 55X and 55Y ........................................................................................................................... 32 
Message Types 55Z ......................................................................................................................................... 41 
General Input/Output Structure ........................................................................................................................ 48 
Field Separators ................................................................................................................................................ 48 
Carriage Return/Line Feed (CrLf) ..................................................................................................................... 48 
Input/Output Formats ........................................................................................................................................ 49 
Batch Input ........................................................................................................................................................ 50 
Batch Output ..................................................................................................................................................... 50 
Interactive Input ................................................................................................................................................ 51 
Interactive Output.............................................................................................................................................. 51 
Output Messages ............................................................................................................................................... 52 
Rejected Messages ............................................................................................................................................ 54 
Whole Message Rejection ................................................................................................................................ 54 

---

## Page 4

 
 
Partial Forward Message Rejection .................................................................................................................. 54 
Security Issue Rejection ................................................................................................................................... 55 
Price/Rate Rejection ......................................................................................................................................... 55 
 

---

## Page 5

Price and Rate ISO Formatted Record Layouts 
History of Important Notices 5 
HISTORY OF IMPORTANT NOTICES 
March 17, 2022 Corrected link to 55Z 
Effective Date: November 23, 2020 Important Notice a8917, P&S 8490 Dated October 19, 2020 
June 11, 2020 Document rebranded and reviewed 
Effective Date: March 25, 2019 Important Notice a8658, P&S 8233 Dated December 19, 2018 
Documentation Changes Important Notice a8354, P&S 7929 Dated March 22, 2017 
Effective Date: September 26, 2016 Important Notice a8159, P&S 7734 Dated Feb 3, 2016 
Effective Date: May 24, 2013 Important Notice a7587, P&S 7157 Dated Feb 15, 2013 
Effective Date: May 31, 2011 Important Notice a7156, P&S 6726 Dated Feb 7, 2011 
 

---

## Page 6

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 6 
SUMMARY OF CHANGES  
Effective Q4, 2020 
 
1. Message Types 55X and 55Y (Block 4 – Messages Text) 
 
a. Added the following new fields: 
 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
O IT Cash Type 
 
Information Type  
(Negative Rate 
Correction 
Indicator) 
4a[/30x] or 
4a[[/DS/1a/1a]/23x] or 
4a[/30x/2n] 
 
DINO 
 
DINC 
 
 
Edit: 
Must correspond to Date 
literal: 
If Date literal = DDRD, then 
Info Type = DINO or DINC 
 
The /DS/ part of Sub field 2 is 
required if Info Type =  DINO 
or DINC (if not provided, the 
system will enter/DS/6/3 and 
truncate the 30-byte 
description, if provided, to 23 
bytes). It’s not allowed 
otherwise. 
The two fields following/DS/, 
together with 35B:Security 
Issue and 04A:Effective Date 
constitute a unique key. A 
35H:Amount can be sent per 
Security Issue, Effective Date 
and any combination of these 
fields. 
 
:IT:DINO/DS/6/3 
 
 
 
Original Negative Rate 
 
Negative Rate Correction 
 
 
 
 
. 

---

## Page 7

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 7 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
OC 35H Cash 
Amount 
 
Amount 
(Negative Rate) 
3a14number 
 
3a = ISO currency 
code: USD, EUR, GBP, AUD, 
CAD, CHF, CNY, HKD, JPY, 
NOK, SEK or SGD 
14number = amount 
 
Edit: 
1. Max digits in amount 
must correspond to Info 
Type as follows: 
Info Type (Negative Rate 
Correction Indicator) = 
DINO or DINC, then max 
digits = 4n.9n 
2. Required and must be > 
0 when Info Type 
(Negative Rate 
Correction Indicator) = 
DINO 
3. Required (but allowed to 
be zero) if Info Type 
(Negative Rate 
Correction Indicator) = 
DINC 
4. Not allowed if Info Type 
(Negative Rate 
Correction Indicator) 
DINO or DINC is not 
provided. 
 
For JPY Currency, a decimal 
point (,) followed by nine 0’s 
is required after the value. 
This field will contain the 
actual Negative Rate  
 
 
Example for USD Only: 
A negative rate of 0.0023 
would be expressed as: 
:IT:DINO 
:35H:USD 0,0023 
  
 
Examples for JPY Only: 
A negative rate of 2050 Yen 
would be expressed as: 
:IT:DINO 
:35H:JPY 2050,000000000 
 
 
b. Modified requirements to existing fields: 
 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
OC IT Cash Type Information Type 4a[/30x] or :IT:PRCO 

---

## Page 8

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 8 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
4a[[/DS/1a/1a]/23x] or 
4a[/30x/2n] 
 
PRCO 
 
 
PRMO 
 
DIVO 
 
CUMO 
 
 PRCC 
 
 
 
PRMC 
 
 
DIVC 
 
 
 
CUMC 
 
 
 
Edit: 
1. Must correspond to Date 
literal: 
If Date literal = PRCE, then 
Info Type = PRCO, PRCC, 
PRMO/2n, or PRMC/2n 
2n – Required if Info Type is 
PRMO or PRMC.  Numeric 
with valid values: 01, 
02,…98, 99. This value will 
indicate whether a particular 
price is the 1st, 2nd, etc. 
price of the day. 
Zero (0) is not a valid value. 
:IT:DIVO/DS/6/3 
:IT:PRMO/01 
 
Single NAV Fund – Original Price 
 
Multiple NAVs Fund – Original 
Price 
 
Rate 
 
 
Cumulative [[Dividend]] Rate 
 
Single NAV Fund - 
Correction to Price 
(See Single (NAV) Fund) 
 
Multiple NAVs Fund – Correction 
to Price 
(See Multiple NAVs Fund) 
 
Rate Correction 
(See [[Dividend]] Rate) 
 
Cumulative [[Dividend]] Rate 
Correction 
(See Cumulative Rate) 
 
 
 
If Sub-field 2 starts with /DS/, it 
must be followed by two one-byte 
fields describing Rate as follows: 
Distribution Type: 
1 = Short Term Capital Gain 
2 = Long Term Gain 
3 = Gain on Collectables 
4 = Section 1202 Gain 
5 = Unrecaptured Section 1250 
Gain 
6 = Daily Accrual [[Dividend]] 

---

## Page 9

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 9 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
2. Required and must be 
DIVO or DIVC when Info 
Type (Negative Rate 
Correction Indicator) = 
DINO. 
 
Best Practice: For the last/end of 
day NAV strike, Funds should 
indicate a value of “98”. 
2n - Is not allowed for Info 
Types other than PRMO and 
PRMC. 
If Date literal = DDRD, then Info 
Type = DIVO or DIVC  
If Date literal = CUDR, then Info 
Type = CUMO or CUMC. 
 
The /DS/ part of Sub field 2 is 
required if Info Type = DIVO or 
DIVC  (if not provided, the 
system will enter/DS/6/3 and 
truncate the 30-byte description, 
if provided, to 23 bytes).  The 
only exception is when Info 
Type (Negative Rate 
Correction Indicator) is = 
DINO or DINC, in which case 
the /DS/ part of Sub field 2 
should not be populated as 
this information would be 
provided in the Info Type 
(Negative Rate Correction 
Indicator) field. 
It’s not allowed otherwise. 
 
The two fields following/DS/, 
together with 35B:Security Issue 
and 04A:Effective Date 
constitute a unique key. A 
35H:Amount can be sent per 
Security Issue, Effective Date 
and any combination of these 
fields. 
7 = [[Equity]] [[Dividend]] 
 
Distribution Indicator: 
1 = Spillover 
3 = Regular Distribution 
 
It then can further define cash 
Type with up to 23 characters (30 
if the /DS/ section is not 
included). 

---

## Page 10

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 10 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
OC 35H Cash 
Amount 
 
Amount (NAV, Rate 
or Cumulative 
[[Dividend]] Rate) 
 
 
[N]3a19number 
 
N = indicates a negative amount 
3a = ISO currency 
code: USD, EUR, GBP, AUD, 
CAD, CHF, CNY, HKD, JPY, NOK, 
SEK or SGD 
19number = amount 
 
Edit: 
1. Amount not allowed to be 
negative (sub- field ‘N’ not 
allowed). 
2. Max digits in amount must 
correspond to Info Type as 
follows: 
If Info Type = PRCO, PRCC, 
PRMO, or PRMC, then max 
digits = 9n.9n 
If Info Type = DIVO or 
DIVC, then max digits = 
9n.9n 
If Info Type = CUMO or 
CUMC, then max digits = 
4n.9n 
3. If Info Type = PRCO, PRCC, 
PRMO, or PRMC then 
amount must be positive. 
Otherwise, amount can be 
zero 
4. Required and must = 0 if 
Info Type (Negative Rate 
Correction Indicator) = 
DINO
. 
 
For JPY Currency, a decimal 
point (,) followed by nine 0’s is 
required after the value. 
This field will contain the actual 
NAV, rate or cumulative [[Dividend]] 
rate. 
 
Examples for USD Only: 
1. A price of 1.023 per share 
would be expressed as: 
:IT:PRCO 
:35H:USD 1,023 
 
2. A zero rate would be 
expressed as: 
:IT:DIVO 
:35H:USD 0, 
 
Examples for JPY Only: 
 
1. A price of 111 Yen per share 
would be expressed as: 
:IT:PRCO 
:35H:JPY 111,000000000 
 
2. A rate of 2050 Yen would be 
expressed as: 
:IT:DIVO 
3. A cumulative rate of 8431 Yen 
would be expressed as: 
:IT:CUMO 
:35H:JPY 8431,000000000 
OC DD  [[Dividend]] Day Count 3n 
 
Edit: 
Mandatory for the following: 
This field will contain the number 
of days of a daily accrual for 
[[Dividend]] rate or cumulative 
[[Dividend]] rate. 
Example: 

---

## Page 11

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 11 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
1. Info Type DIVO/DS/6 or 
DIVC/DS/6 (valid range: 
001-365). 
2. Info Type CUMO or CUMC 
(valid range: 001-999). 
3. Info Type (Negative Rate 
Correction Indicator) 
DINO/DS/6 or 
DINC/DS/6 (valid range: 
001-365). 
Not allowed otherwise. 
Accrual for 3 days would be 
expressed as: 
:DD:003 
 
 
 
2. Message Types 55Z (Block 4 – Messages Text) 
 
a. Added the following new fields: 
 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
O IT Cash Type 
 
Information Type  
(Negative Rate 
Correction 
Indicator) 
4a[/30x] or 
4a[[/DS/1a/1a]/23x] or 
4a[/30x/2n] 
 
DINO 
DINC 
 
Edit: 
Must correspond to Date 
literal: 
If Date literal = DDRD, then 
Info Type = DINO or DINC 
 
The /DS/ part of Sub field 2 is 
required if Info Type =  DINO 
or DINC (if not provided, the 
system will enter/DS/6/3 and 
truncate the 30-byte 
description, if provided, to 23 
bytes). It’s not allowed 
otherwise. 
:IT:DINO/DS/6/3 
 
 
 
Original Negative Rate 
Negative Rate Correction 
 
 
 
 
. 

---

## Page 12

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 12 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
The two fields following/DS/, 
together with 35B:Security 
Issue and 04A:Effective Date 
constitute a unique key. A 
35H:Amount can be sent per 
Security Issue, Effective Date 
and any combination of these 
fields. 
OC 35H Cash 
Amount 
 
Amount 
(Negative Rate) 
3a14number 
 
3a = ISO currency 
code: USD, EUR, GBP, AUD, 
CAD, CHF, CNY, HKD, JPY, 
NOK, SEK or SGD 
 
14number = amount 
 
Edit: 
1. Max digits in amount 
must correspond to Info 
Type as follows: 
Info Type (Negative Rate 
Correction Indicator) = 
DINO or DINC, then max 
digits = 4n.9n 
2. Required and must be > 
0 when Info Type 
(Negative Rate 
Correction Indicator) = 
DINO 
3. Required (but allowed to 
be zero) if Info Type 
(Negative Rate 
Correction Indicator) = 
DINC 
4. Not allowed if Info Type 
(Negative Rate 
Correction Indicator) 
DINO or DINC is not 
provided. 
 
For JPY Currency, a decimal 
point (,) followed by nine 0’s 
is required after the value. 
 
This field will contain the 
actual Negative Rate  
 
 
Example for USD Only: 
A negative rate of 0.0023 
would be expressed as: 
:IT:DINO 
:35H:USD 0,0023 
  
 
Examples for JPY Only: 
A negative rate of 2050 Yen 
would be expressed as: 
:IT:DINO 
:35H:JPY 2050,000000000 

---

## Page 13

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 13 
3. Added new Reject Codes: 
 
Reject Code Description 
0407 Negative Rate Correction Indicator is missing/invalid 
0408 Negative Rate is missing/invalid 
 
Effective Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
0388 [[participant]] is not valid for the Submitter and/or Product 
Effective Q1, 2017 
4. Message Types 55X and 55Y (Block 4 – Messages Text) 
a. Documentation change – Modify Field description: 
 
Current Requirement: 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund Profile 
Field Name 
MFPS Format/Allowed 
Input Values/Input Edit 
Criteria 
Example/Comment/MFPS Output 
(When Not Same as Input) 
M TT  Transaction Type MFRP 
MFMP 
MFDD 
MFSI 
 
MFNP 
 
Edit: 
Must be MFRP for this 
phase 
Mutual Fund Rate and Price 
Mutual Fund [[Member]] Profile 
Mutual Fund [[Dividend]] Declaration 
Mutual Fund Security Issue 
Information 
Mutual Fund [[NASD]] Price 
 
MFPS output: 
MFRP - price is from fund 
MFNP - price is from [[NASD]] 

---

## Page 14

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 14 
 
New Requirement: 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund Profile 
Field Name 
MFPS Format/ Allowed 
Input Values/ Input Edit 
Criteria 
Example/Comment/ MFPS Output 
(When Not Same as Input) 
M TT  Transaction Type MFRP 
MFMP 
MFDD 
MFSI 
 
Edit: 
Must be MFRP for this 
phase 
Mutual Fund Rate and Price 
Mutual Fund [[Member]] Profile 
Mutual Fund [[Dividend]] Declaration 
Mutual Fund Security Issue 
Information 
MFPS output: 
MFRP - price is from fund 
 
 
5. Message Types 55Z (Block 4 – Messages Text) 
a. Documentation change – Modify Field description: 
 
Current Requirement 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund Profile 
Field Name 
MFPS Format/ Allowed 
Input Values/ Input Edit 
Criteria 
Example/Comment/ MFPS Output 
(When Not Same as Input) 
M TT  Transaction Type MFRP 
MFMP 
MFDD 
MFSI 
 
MFNP 
 
Mutual Fund Rate and Price 
Mutual Fund [[Member]] Profile 
Mutual Fund [[Dividend]] Declaration 
Mutual Fund Security Issue 
Information 
Mutual Fund [[NASD]] Price 
 
New Requirement: 
M/O 
/OC 
Tag SWIFT 
Field Name 
Mutual Fund Profile 
Field Name 
MFPS Format Example/Comment 
M TT  Transaction Type MFRP 
MFMP 
MFDD 
MFSI 
Mutual Fund Rate and Price 
Mutual Fund [[Member]] Profile 
Mutual Fund [[Dividend]] Declaration 
Mutual Fund Security Issue 
Information 
  

---

## Page 15

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 15 
Effective Q3, 2016 
1. Message Types 55X and 55Y (Block 4 – Messages Text) 
a. Field description requirement change: 
 
1. Cash Type – Information Type  
 Current Requirement: Required. 
4a[/30x] or 
4a[[/DS/1a/1a]/23x] 
PRCO 
DIVO  
CUMO 
PRCC 
DIVC 
CUMC 
 
Edit: 
must correspond to Date literal: 
If Date literal = PRCE, then Info Type = PRCO or PRCC. 
If Date literal = DDRD, then Info Type = DIVO or DIVC. 
If Date literal = CUDR, then Info Type = CUMO or CUMC. 
The /DS/ part of Sub field 2 is required if Info Type = DIVO or 
DIVC (if not provided, the system will enter/DS/6/3 and truncate 
the 30-byte description, if provided, to 23 bytes). It’s not allowed 
otherwise. 
The two fields following/DS/, together with 35B:Security Issue 
and 04A:Effective Date constitutes a unique key. A 35H:Amount 
can be sent per Security Issue, Effective Date and any 
combination of these fields. 
 New Requirement: Required. 
4a[/30x] or 
4a[[/DS/1a/1a]/23x] or 
4a[/30x/2n] 
 
PRCO 
PRMO 
DIVO 
CUMO 
PRMC 
DIVC 
CUMC 
 

---

## Page 16

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 16 
Edit: 
Must correspond to Date literal: 
 
If Date literal = PRCE, then Info Type = PRCO, PRCC, 
PRMO/2n, or PRMC/2n 
2n – Required if Info Type is PRMO or PRMC.  Numeric with 
valid values: 01, 02, …, 98,99.  This value will indicate 
whether a particular price is the 1st, 2nd, etc. price of the 
day. 
Zero is not a valid value. 
 
Best Practice: For the last/end of day NAV strike, Funds 
should indicate a value of “98”. 
 
2n - Is not allowed for Info Types other than PRMO and 
PRMC. 
 
If Date literal = DDRD, then Info Type = DIVO or DIVC.  
If Date literal = CUDR, then Info Type = CUMO or CUMC. 
The /DS/ part of Sub field 2 is required if Info Type = DIVO or 
DIVC (if not provided, the system will enter /DS/6/3 and truncate 
the 30-byte description, if provided, to 23 bytes). It’s not allowed 
otherwise. 
The TWO fields following /DS/, together with 35B:Security Issue 
and 04A:Effective Date constitutes a unique key. A 35H:Amount 
can be sent per Security Issue, Effective Date and any 
combination of these fields. 
2. Cash Amount – Amount (NAV, 
Rate or Cumulative [[Dividend]] 
Rate) 
 
 Current Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD, EUR, GBP, AUD, CAD, CHF, 
CNY, HKD, JPY, NOK, SEK or SGD 
19number = amount 
Edit: 
1. Amount not allowed being negative (sub- field ‘N’ not 
allowed). 
2. Max digits in amount must correspond to Info Type as 
follows:  
If Info Type = PRCO or PRCC, then max digits = 9n.9n 
If Info Type = DIVO or DIVC, then max digits = 9n.9n 
If Info Type = CUMO or CUMC, then max digits = 4n.9n 

---

## Page 17

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 17 
3,    If Info Type = PRCO or PRCC, then amount must be 
positive. Otherwise, amount can be zero 
For JPY Currency, a decimal point (,) followed by nine 0’s is 
required after the value 
 New Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD, EUR, GBP, AUD, CAD, CHF, 
CNY, HKD, JPY, NOK, SEK or SGD 
19number = amount 
Edit: 
1. Amount not allowed being negative (sub- field ‘N’ not 
allowed). 
2. Max digits in amount must correspond to Info Type as 
follows: 
If Info Type = PRCO, PRCC, PRMO, or PRMC then max 
digits = 9n.9n If Info Type = DIVO or DIVC, then max digits = 
9n.9n 
If Info Type = CUMO or CUMC, then max digits = 4n.9n 
3. If Info Type = PRCO, PRCC, PRMO, or PRMC then amount 
must be positive. Otherwise, amount can be zero 
For JPY Currency, a decimal point (,) followed by nine 0’s is 
required after the value. 
3. Date (universal) – Effective Date for Amount following 
 Current Requirement: Optional 
xxxxx/yyyymmdd 
xxxx can be 
PRCE 
DDRD 
CUDR 
 
Edit: 
1. If xxxx = PRCE, then yyyymmdd must be a valid business 
day and cannot be future dated 
2. If xxxx = DDRD or CUDR, then yyyymmdd can be any 
calendar date 

---

## Page 18

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 18 
 New Requirement: Optional Conditional 
xxxxx/yyyymmdd 
xxxx can be 
PRCE 
DDRD 
CUDR 
 
Edit: 
1. If xxxx = PRCE, then yyyymmdd must be a valid business 
day and cannot be future dated 
2. If xxxx = DDRD or CUDR, then yyyymmdd can be any 
calendar date 
3. Required if Info Type is PRMO or PRMC. 
This is the Price strike date. For example, if the fund 
provides a price at 12pm on 9/10/15, the “Effective Date” of 
this price will be “20150910”. 
 
b. New Data Fields 
 
1. Time - Price (NAV) Start Time  
 Requirement: Optional Conditional 
hhmmss/PST 
Eastern Time 
 
The start time of the price is 1 (one) second after the 
previous price was provided. For example, the fund may 
strike a price three times a day: 9am, 12pm and 3pm. The 
“Price (NAV) Start Time” of the 12pm price will be “090001” 
(9:00:01am). 
Similarly, the “Price (NAV) Start Time” of the 9am price will 
be “150001” (3:00:01pm) since the previous price was 
calculated at 3pm on the previous day. 
 
Edit: 
Required if Info Type is PRMO or PRMC. 
Not allowed for other Info Types. 

---

## Page 19

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 19 
2. Date (universal) - Price (NAV) Start Date 
 Requirement: Optional Conditional 
PMSD/yyyymmdd 
Date of the price start time.  For example, if the fund strikes 
a price at 12pm on 9/10/15, the “Price (NAV) Start Date” will 
be “20150910”. If the fund strikes a price at 3pm on 9/9/15 
and the next one at 9am on 9/10/15, the “Price (NAV) Start 
Date” of the 9am price will be “20150909” (9/9/2015). 
Edit: 
Must be a valid business day on or before effective date. 
Required if Info Type is PRMO or PRMC 
Not allowed for other Info Types. 
3. Time - Price (NAV) Strike Time 
 Requirement: Optional/Conditional 
hhmmss/PET 
Eastern Time 
This field must contain the strike time of the price. For 
example, if the fund strikes a price at 3pm, the “Price (NAV) 
Strike Time” will be “150000” (3pm). 
Edit: 
Required if Info Type is PRMO or PRMC. 
Not allowed for other Info Types. 
 
c. Change to Example/Comment/MFPS Output (When Not Same as Input) 
 
1. Date (universal) – Date price/rate is submitted 
 Current Requirement:  
Date effective for following repeating sequences of prices, daily 
accrual rates and cumulative rates. 
Example: 
04A:SUBD/20060927 = Price file submitted on Sept 27, 2006 
 Modified Example:  
Date effective for following repeating sequences of prices, daily 
accrual rates and cumulative rates except when Info Type is 
PRMO or PRMC, where this is the Submission Date only. 
Example: 
04A:SUBD/20060927 = Price file submitted on Sept 27, 2006 

---

## Page 20

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 20 
2. Cash Type- Information Type  
 Current Example: :IT:PRCO 
:IT:DIVO/DS/6/3 
Price (NAV) 
Rate 
Cumulative [[Dividend]] Rate 
Price Correction 
Rate Correction 
Cumulative [[Dividend]] Rate Correction 
if Sub-field 2 starts with /DS/, it must be followed by two one-byte 
fields describing Rate as follows: 
1. Distribution Type: 
1 = Short Term Capital Gain 
2 = Long Term Gain 
3 = Gain on Collectables 
4 = Section 1202 Gain 
5 = Unrecaptured Section 1250 Gain 
6 = Daily Accrual [[Dividend]] 
7 = [[Equity]] [[Dividend]] 
2. Distribution Indicator: 
1 = Spillover 
3 = Regular Distribution 
It then can further define cash Type with up to 23 characters (30 
if the/DS/ section is not included). 

---

## Page 21

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 21 
 Modified Example:  
:IT:PRCO 
:IT:DIVO/DS/6/3 
:IT:PRMO/01 
 
Single NAV Fund – Original Price 
Multiple NAVs Fund – Original Price 
Rate 
Cumulative [[Dividend]] Rate 
Single NAV Fund - Correction to Price 
(See a. Price – Single (NAV) Fund) 
Multiple NAVs Fund – Correction to Price 
(See b. Price – Multiple NAVs Fund) 
Rate Correction 
(See c. [[Dividend]] Rate) 
Cumulative [[Dividend]] Rate Correction 
(See d. Cumulative Rate) 
if Sub-field 2 starts with /DS/, it must be followed by two one-byte 
fields describing Rate as follows: 
1. Distribution Type: 
1 = Short Term Capital Gain 
2 = Long Term Gain 
3 = Gain on Collectables 
4 = Section 1202 Gain 
5 = Unrecaptured Section 1250 Gain 
6 = Daily Accrual [[Dividend]] 
7 = [[Equity]] [[Dividend]] 
2. Distribution Indicator: 
1 = Spillover 
3 = Regular Distribution 
It then can further define cash Type with up to 23 characters (30 
if the /DS/ section is not included). 
 

---

## Page 22

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 22 
1. Message Types 55Z (Block 4 – Messages Text) 
a. Field description requirement change: 
 
1. Cash Type – Information Type 
 Current Requirement: Required. 
4a[/30x] or 4a[[/DS/1a/1a]/23x] 
PRCO 
DIVO 
CUMO 
PRCC 
DIVC 
CUMC 
 New Requirement: Required. 
4a[/30x] or 4a[[/DS/1a/1a]/23x] or 
4a[/30x/2n] 
PRCO 
PRMO 
DIVO 
CUMO 
PRCC 
PRMC 
DIVC 
CUMC 
2n – numeric, values: 01, 02, …, 98, 99. This value will 
indicate whether a particular price is the 1st, 2nd, etc. price 
of the day. This value will indicate whether a particular price 
is the 1st, 2nd, etc. price of the day. 
2. Date (universal) – Effective Date for Amount following 
 Current Requirement: Optional 
PRCE/yyyymmdd 
DDRD/yyyymmdd 
CUDR/yyyymmdd 
 New Requirement: Optional Conditional 
PRCE/yyyymmdd 
DDRD/yyyymmdd 
CUDR/yyyymmdd 
Required if Info Type is PRMO or PRMC. 
This is the Price strike date. For example, if the fund 
provides a price at 12pm on 9/10/15, the “Effective Date” of 
this price will be “20150910”. 
 

---

## Page 23

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 23 
b. New Data Fields 
 
1. Time - Price (NAV) Start Time 
 Requirement: Optional Conditional 
hhmmss/PST 
Eastern Time 
The start time of the price is 1 (one) second after the 
previous price was provided. For example, the fund may 
strike a price three times a day: 9am, 12pm and 3pm. The 
“Price (NAV) Start Time” of the 12pm price will be “090001” 
(9:00:01am). 
Similarly, the “Price (NAV) Start Time” of the 9am price will 
be “150001” (3:00:01pm) since the previous price was 
calculated at 3pm on the previous day. 
Required if Info Type is PRMO or PRMC. 
2. Date (universal) - Price (NAV) Start Date 
 Requirement: Optional Conditional 
PMSD/yyyymmdd 
Date of the price start time. For example, if the fund strikes a 
price at 12pm on 9/10/15, the “Price (NAV) Start Date” will be 
“20150910”. If the fund strikes a price at 3pm on 9/9/15 and 
the next one at 9am on 9/10/15, the “Price (NAV) Start Date” 
of the 9am price will be “20150909” (9/9/2015). 
Required if Info Type is PRMO or PRMC 
3. Time - Price (NAV) Strike Time 
 Requirement: Optional Conditional 
hhmmss/PET 
Eastern Time 
This field must contain the strike time of the price. For 
example, if the fund strikes a price at 3pm, the “Price (NAV) 
Strike Time” will be “150000” (3pm). 
Required if Info Type is PRMO or PRMC. 
 
c. Change to Example/Comment/MFPS Output (When Not Same as Input) 
 
1. Date (universal) – Date price/ rate is submitted 
 Current Example:  
Date effective for following repeating sequences of prices, daily 
accrual rates and cumulative rates. 
Example: 
:04A:SUBD/20060927 = Price file submitted on Sept 27, 2006 

---

## Page 24

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 24 
 Modified Example:  
Date effective for following repeating sequences of prices, daily 
accrual rates and cumulative rates except when Info Type is 
PRMO or PRMC, where this is the Submission Date only. 
Example: 
:04A:SUBD/20060927 = Price file submitted on Sept 27, 2006 
Effective Q2, 2013 
1. Message Types 55X and 55Y (Block 4 – Messages Text) 
a. Field description requirement change: 
 
1. Cash Amount 
 Current Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD 
19number = amount 
 New Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD, EUR , GBP, AUD, CAD, CHF, 
CNY, HKD, JPY, NOK, SEK or SGD 
19number = amount 
 
1. Message Types 55Z (Block 4 – Messages Text) 
a. Field description requirement change: 
 
1. Cash Amount 
 Current Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD 
 New Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD, EUR, GBP, AUD, CAD, CHF, 
CNY, HKD, JPY, NOK, SEK or SGD 
19number = amount 
 

---

## Page 25

Price and Rate ISO Formatted Record Layouts 
Summary of Changes 25 
Effective Q2, 2011 
1. Message Types 55X and 55Y (Block 4 – Messages Text) 
a. Field description requirement change: 
 
1. Cash Amount 
 Current Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD 
19number = amount 
 New Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD, EUR or GBP 
19number = amount 
 
1. Message Types 55Z (Block 4 – Messages Text) 
a. Field description requirement change: 
 
1. Cash Amount 
 Current Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD 
 New Requirement: Required. 
[N]3a19number 
N = indicates a negative amount 
3a = ISO currency code: USD, EUR or GBP 
19number = amount 

---

## Page 26

Price and Rate ISO Formatted Record Layouts 
Introduction 26 
INTRODUCTION   
Mutual Fund Profile Service (MFPS) uses both ISO and non-ISO formats for input and output data. This 
document describes the ISO format. 
MFPS ISO format follows S.W.I.F.T. rules for both input and output. For more information about S.W.I.F.T. 
rules see the document Mutual Fund Profile Service (MFPS), ISO/S.W.I.F.T. MESSAGE STRUCTURE, 
REFERENCE GUIDE published by [[NSCC]]. 
A typical S.W.I.F.T. message may consist of five (5) blocks: 
1. [[BASIC]] Header Block 
2. Application Header Block 
3. User Header Block 
4. Text Block 
5. Trailer Block 
 
The following sections describe MFPS formats and edit criteria for these blocks. 

---

## Page 27

Price and Rate ISO Formatted Record Layouts 
Header and Trailer Blocks 27 
HEADER AND TRAILER BLOCKS 
This section describes MFPS formats and edit criteria for the headers and trailer blocks (blocks 1, 2, 3 and 4). 
Notes: 
1. Spaces between fields in header and trailer blocks are not allowed. The spaces between fields in the following headers 
and trailer formats are for clarification only. 
2. Under column headings MFPS Allowed Input Values or MFPS Output Values: lower case letters mean format or 
description; any other character means exact value. 
Block 1 - [[BASIC]] Header 
Format: 1 22 3 44 555555555555 6666 777777 8 
Field No. Field Name Length 
(bytes) 
MFPS Allowed Input Values MFPS Output Values (when not 
same as input) 
1 Left Curly Bracket 
(or Brace) 
1 {  
2 Block Identifier 2 1:  
3 SWIFT Application 
[[ID]] 
1 F  
4 Application Protocol 
Data Unit 
2 01  
5 SWIFT Address or 
BIC (Bank [[ID]] Code) 
12 bytes 1-4: sender clearing no 
bytes 5-7: MFP 
bytes 8-12: XXXXX 
recipient clearing no 
(when identifiable) 
6 Transmission 
Session Number 
4 0000  
7 Sequence Number 6 000000  
8 Right Curly Bracket 
(or Brace) 
1 }  
 
Total block length (in bytes): 29 
Example: {1:F015119MFPXXXXX0000000000}    
  

---

## Page 28

Price and Rate ISO Formatted Record Layouts 
Header and Trailer Blocks 28 
Block 2 - Application Header 
This block has two (2) different formats: input format and output format. 
Block 2 - Application Header, Input Format 
Format: 1 22 3 444 555555555555 6 7 888 9 
Field No. Field Name Length (bytes) MFPS Allowed Input 
Values 
1 Left Curly Bracket (or 
Brace) 
1 { 
2 Block Identifier 2 2: 
3 Input Indicator 1 I 
4 Message Type Number 3 55Y 
5 SWIFT Recipient Address 12 bytes 1-4: [[NSCC]] 
bytes 5-7: MFP 
bytes 8-12: XXXXX 
6 Message Priority Indicator 1 N 
7 Delivery Monitoring 
Indicator 
1 2 
8 Obsolescence Period 3 002 
9 Right Curly Bracket (or 
Brace) 
1 } 
 
Total block length (in bytes): 25 
Example: {2:I55YNSCCMFPXXXXXN2002}                  
  

---

## Page 29

Price and Rate ISO Formatted Record Layouts 
Header and Trailer Blocks 29 
Block 2 - Application Header, Output Format 
Format: 1 22 3 444 5555 666666666666666666666666666666 77777777 8 9 
Field No. Field Name Length (bytes) MFPS Values 
1 Left Curly Bracket (or 
Brace) 
1 { 
2 Block Identifier 2 2: 
3 Input Indicator 1 O 
4 Message Type Number 3 55X, 55Z 
5 Sender Input Time 4 Time (hhmm) 
6 Message Input Reference 30 bytes 1-8: original message 
input date (yyyymmdd) 
bytes 9-12: [[NSCC]] 
bytes 13-15: MFP 
bytes 16-20: XXXXX 
bytes 21-30: 0000000000 
7 Output Date 8 output date (yyyymmdd) 
8 Message Priority Indicator 1 N 
9 Right Curly Bracket (or 
Brace) 
1 } 
 
Total block length (in bytes): 51 
Example: {2:O55X104719950928NSCCMFPXXXXX000000000019950928N}                 
  

---

## Page 30

Price and Rate ISO Formatted Record Layouts 
Header and Trailer Blocks 30 
Block 2 - Application Header, Input versus Output Considerations 
The definition of Input and Output formats as described above are relative to the S.W.I.F.T. system. Since 
MFPS will not receive or submit messages via the S.W.I.F.T. system in this phase, they are also relative to 
MFPS. 
In the future, when MFPS starts to use the S.W.I.F.T. system for receiving and submitting messages, these 
definitions will become the opposite in relation to MFPS. 
The following chart describes this situation: 
 
Block 3 - User Header 
MFPS does not allow this block as input and does not create it as output. 
Block 5 - Trailer 
Format: 1 22 3333333333333 444444 5 
Field No. Field Name Length (bytes) MFPS Allowed Input 
Values 
MFPS Output Values 
(when not same as 
input) 
1 Left Curly Bracket (or Brace) 1 {  
2 Block Identifier 2 5:  
3 Sub-block Identifier 13 {MAC:TRAILER}  
4 Training (Test) Indicator 6 {TNG:} (see note 
below) 
 
5 Right Curly Bracket (or Brace) 1 }  
 
Maximum block length (in bytes): 23 
Example: {5:{MAC:TRAILER}{TNG:}} 


---

## Page 31

Price and Rate ISO Formatted Record Layouts 
Header and Trailer Blocks 31 
Note: 
Field #4 (Training Indicator) is optional. If it is present it indicates that this is a test message. A test message is handled as 
follows: 
1. It is edited as any other message 
2. If rejected, it is handled as any other message (returned to the submitter) 
3. If accepted, it is skipped (the database is not being updated and the message is not being sent to contra participants). 

---

## Page 32

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 32 
BLOCK 4 – MESSAGES TEXT 
This section describes MFPS formats and edit criteria for the text block. 
Message Types 55X and 55Y 
Message Type 55X - Notification: Mutual Fund Profile Price and Rate Service From [[NSCC]] to a [[participant]] 
Message Type 55Y - Instruction: Fund to [[NSCC]] / Price and Rate Information 
Notes: 
1. Under column heading M/O: M = Mandatory, O = Optional, OC = Generally optional, but mandatory upon some 
specified conditions. 
2. Under column heading MFPS Format/Allowed Values/Edit: Upper case letters mean exact value; lower case letters 
mean format (to be replaced by user value) 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
M 20 Transaction 
Reference 
number 
Reference 
number 
16x 
 
Edit: 
1st four (4) characters must be 
sending [[Member]] clearing number 
Must be unique. 
:20:0115152631234567 
MFPS output: 
  bytes 1-4 = MFPR 
  bytes 5-8 = Julian date (yddd) 
Batch: 
  byte 9 = Alphabetic 
  byte 10-13 = time (mmss) 
Online: 
  byte 9-13 = last 5 digit of task 
number 
  bytes 14-16 = sequence 
number (includes digits and 
letters) 
O 21 Related 
Reference 
Number 
Related 
Reference 
Number 
16x Used to relate this message to 
a previous message. MFPS 
does not use it to relate to a 
previous message and does not 
carry it in the output 
M TT  Transaction 
Type 
MFRP 
MFMP 
MFDD 
MFSI 
 
Edit: 
Must be MFRP for this phase 
Mutual Fund Rate and Price 
Mutual Fund [[Member]] Profile 
Mutual Fund [[Dividend]] 
Declaration 
Mutual Fund Security Issue 
Information 
MFPS output: MFRP - price is 
from fund 

---

## Page 33

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 33 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
M 04A Date 
(universal) 
 
Date price / 
rate is 
submitted 
SUBD/yyyymmdd 
Edit: 
Must be today’s business date 
Date effective for following 
repeating sequences of prices, 
daily accrual rates and 
cumulative rates except when 
Info Type is PRMO or PRMC, 
where this is the Submission 
Date only. 
Example: 
:04A:SUBD/20060927 = Price 
file submitted on Sept 27, 2006 
M 05G Time Time hhmmss[/2a/16x] Time 
2a = ISO country code 16x = 
local description 
:05G:165330/US/NYC 
The ISO country code and 
associated local description are 
optional. If these values are not 
entered the time presented is 
defined as: 
New York City, USA time (aka 
East Coast time) 
MFPS output: 
hhmmss/US/NYC 
 
Repeating Sequence level 1, Security Issue Section (at least one is required) 
 
M 35B Security Security Issue 
Number, 
Symbol and 
Description 
 ISINb12a 
 [35x] or 
 [/TS/1a/8a] 
 [3 * 35x] 
 
Edit: 
ISIN check digit is validated. 
(ISIN check digit is the last digit 
of the sub-field described as 12a. 
it is calculated using the 11 
characters preceding it). 
Symbol Indicator: 
N = [[NASD]] 
P = Proposed 
If the first line of security 
description starts with /TS/, it 
indicates a Symbol line. In this 
case, the /TS/ must be followed 
by Symbol Indicator (N = 
[[NASD]], P = Proposed), followed 
by /, followed by the security 
symbol. 
Example for USD Only: 
:35B:ISIN US2245427719 
/TS/P/ABCDX BANKAMERICA 
CO COMMON USD1 
 
Repeating Sequence level 2 (within Repeating Sequence level 1), Price/Rate section 
(At least one (1) is required. Up to twenty (20) are allowed) 

---

## Page 34

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 34 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
OC 04A Date 
(universal) 
 
Effective Date 
for amount 
following 
xxxx/yyyymmdd xxxx can be: 
PRCE 
 
DDRD 
 
CUDR 
 
Edit: 
1. If xxxx = PRCE, then 
yyyymmdd must be a valid 
business day and cannot be 
future dated 
2. If xxxx = DDRD or CUDR, 
then yyyymmdd can be any 
calendar date 
3. Required if Info Type is 
PRMO or PRMC. 
 
Multiple NAVs Fund - this is the 
Price strike date. For example, if 
the fund provides a price at 12pm 
on 9/10/15, the ”Effective Date” of 
this price will be “20150910”. 
 
 
Date effective for the NAV 
following. 
Date effective for Rate 
following. 
Date effective for cumulative 
rate following. 
This date field is to be used to 
indicate a date for a price other 
than that identified in the non-
repeating portion of the record 
(submitted date); either due to 
that price having not been 
reported on that date or in need 
of correction. 
Example: 
:04A:PRCE/20060927 = NAV 
for Sept 27, 2006 
OC IT Cash Type 
 
(modified 
effective 
11/23/20) 
Information 
Type 
4a[/30x] or 
4a[[/DS/1a/1a]/23x] or 
4a[/30x/2n] 
 
PRCO 
 
 
PRMO 
 
DIVO 
 
CUMO 
 
  
PRCC 
 
:IT:PRCO 
:IT:DIVO/DS/6/3 
:IT:PRMO/01 
 
Single NAV Fund – Original 
Price 
 
Multiple NAVs Fund – Original 
Price 
 
Rate 
 
Cumulative [[Dividend]] Rate 
 
Single NAV Fund - 
Correction to Price 
(See Single (NAV) Fund) 

---

## Page 35

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 35 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
 
PRMC 
 
 
 
DIVC 
 
CUMC 
 
 
 
 
Edit: 
1. Must correspond to Date 
literal: 
If Date literal = PRCE, then 
Info Type = PRCO, PRCC, 
PRMO/2n, or PRMC/2n 
2n – Required if Info Type is 
PRMO or PRMC.  Numeric 
with valid values: 01, 02, 
…98, 99. This value will 
indicate whether a particular 
price is the 1st, 2nd, etc. 
price of the day. 
Zero (0) is not a valid value. 
2. Required and must be 
DIVO or DIVC when Info 
Type (Negative Rate 
Correction Indicator) = 
DINO. 
 
Best Practice: For the last/end of 
day NAV strike, Funds should 
indicate a value of “98”. 
2n - Is not allowed for Info Types 
other than PRMO and PRMC. 
If Date literal = DDRD, then Info 
Type = DIVO or DIVC. 
If Date literal = CUDR, then Info 
Type = CUMO or CUMC. 
The /DS/ part of Sub field 2 is 
required if Info Type = DIVO or 
 
Multiple NAVs Fund – 
Correction to Price 
(See Multiple NAVs Fund) 
 
Rate Correction 
(See [[Dividend]] Rate) 
Cumulative [[Dividend]] Rate 
Correction 
(See Cumulative Rate) 
 
 
 
 
 
 
If Sub-field 2 starts with /DS/, it 
must be followed by two one-
byte fields describing Rate as 
follows: 
Distribution Type: 
1 = Short Term Capital Gain 
2 = Long Term Gain 
3 = Gain on Collectables 
4 = Section 1202 Gain 
5 = Unrecaptured Section 1250 
Gain 
6 = Daily Accrual [[Dividend]] 
7 = [[Equity]] [[Dividend]] 
 
Distribution Indicator: 
1 = Spillover 
3 = Regular Distribution 
 
It then can further define cash 
Type with up to 23 characters 
(30 if the /DS/ section is not 
included). 

---

## Page 36

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 36 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
DIVC (if not provided, the system 
will enter/DS/6/3 and truncate the 
30-byte description, if provided, 
to 23
 bytes).  The only 
exception is when Info Type 
(Negative Rate Correction 
Indicator) is = DINO or DINC, 
in which case the /DS/ part 
of Sub field 2 should not be 
populated as this information 
would be provided in the Info 
Type (Negative Rate 
Correction Indicator) field. 
It’s not allowed otherwise. 
 
 
The two fields following/DS/, 
together with 35B:Security Issue 
and 04A:Effective Date constitute 
a unique key. A 35H:Amount can 
be sent per Security Issue, 
Effective Date and any 
combination of these fields. 
 
OC 05G Time 
 
Price (NAV) 
Start Time 
hhmmss/PST Eastern Time 
 
The start time of the price is 1 
(one) second after the previous 
price was provided. For example, 
the fund may strike a price three 
times a day: 9am, 12pm and 
3pm. The “Price (NAV) Start 
Time” of the 12pm price will be 
“090001” (9:00:01am). 
Similarly, the “Price (NAV) Start 
Time” of the 9am price will be 
“150001” 
(3:00:01pm) since the previous 
price was calculated at 3pm on 
the previous day. 
 
Edit: 
Required if Info Type is PRMO or 
PRMC. 
Not allowed for other Info Types. 
:05G:090001/PST 

---

## Page 37

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 37 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
OC 04A Date 
(universal) 
 
Price (NAV) 
Start Date 
PMSD/yyyymmdd 
Date of the price start time.  For 
example, if the fund strikes a 
price at 12pm on 9/10/15, the 
“Price (NAV) Start Date” will be 
“20150910”. If the fund strikes a 
price at 3pm on 9/9/15 and the 
next one at 9am on 9/10/15, the 
“Price (NAV) Start Date” of the 
9am price will be “20150909” 
(9/9/2015). 
 
Edit: 
Required if  Info Type is PRMO 
or PRMC. Not allowed for other 
Info Types. 
Must be a valid business date.  
Must be on or before “Effective 
Date”. 
Example: 
:04A:PMSD/20150909 = 
Price (NAV) Start Date is 
September 9, 2015. 
OC 05G Time 
 
Price (NAV) 
Strike Time 
 
 
hhmmss/PET Eastern Time 
 
This field must contain the strike 
time of the price.  For example, if 
the fund strikes a price at 3pm, 
the “Price (NAV) Strike Time” will 
be “150000” (3pm). 
 
Edit: 
Required if Info Type is PRMO or 
PRMC. 
Not allowed for other Info Types. 
:05G:150000/PET 

---

## Page 38

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 38 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
OC 35H Cash Amount 
 
(modified 
effective 
11/23/20) 
Amount (NAV, 
Rate or 
Cumulative 
[[Dividend]] 
Rate) 
[N]3a19number 
 
N = indicates a negative amount 
3a = ISO currency 
code: USD, EUR, GBP, AUD, 
CAD, CHF, CNY, HKD, JPY, 
NOK, SEK or SGD 
19number = amount 
Edit: 
1. Amount not allowed to be 
negative (sub- field ‘N’ not 
allowed). 
2. Max digits in amount must 
correspond to Info Type as 
follows: 
If Info Type = PRCO, PRCC, 
PRMO, or PRMC, then max 
digits = 9n.9n 
If Info Type = DIVO or DIVC, 
then max digits = 9n.9n 
If Info Type = CUMO or 
CUMC, then max digits = 
4n.9n 
3. If Info Type = PRCO, PRCC, 
PRMO, or PRMC then 
amount must be positive. 
Otherwise, amount can be 
zero 
4. Required and must = 0 if 
Info Type (Negative Rate 
Correction Indicator) = 
DINO. 
 
For JPY Currency, a decimal 
point (,) followed by nine 0’s is 
required after the value. 
This field will contain the actual 
NAV, rate or cumulative 
[[Dividend]] rate. 
Examples for USD Only: 
1. A price of 1.023 per share 
would be expressed as: 
:IT:PRCO 
:35H:USD 1,023 
 
2. A zero rate would be 
expressed as: 
:IT:DIVO 
:35H:USD 0, 
 
Examples for JPY Only: 
 
1. A price of 111 Yen per 
share would be expressed 
as: 
:IT:PRCO 
:35H:JPY 111,000000000 
 
2. A rate of 2050 Yen would 
be expressed as: 
:IT:DIVO 
:35H:JPY 2050,000000000 
 
3. A cumulative rate of 8431 
Yen would be expressed 
as: 
:IT:CUMO 
:35H:JPY 8431,000000000 
OC DD  [[Dividend]] Day 
Count 
 
(modified 
effective 
11/23/20) 
3n 
 
Edit: 
Mandatory for the following: 
1. Info Type DIVO/DS/6 or 
DIVC/DS/6 (valid range: 001-
365). 
This field will contain the 
number of days of a daily 
accrual for [[Dividend]] rate or 
cumulative [[Dividend]] rate. 
Example: 
Accrual for 3 days would be 
expressed as: 
:DD:003 

---

## Page 39

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 39 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
2. Info Type CUMO or CUMC 
(valid range: 001-999). 
3. Info Type (Negative Rate 
Correction Indicator) 
DINO/DS/6 or DINC/DS/6 
(valid range: 001-365). 
 
Not allowed otherwise. 
O IT Cash Type 
 
(effective 
11/23/20) 
 
Information 
Type 
(Negative 
Rate 
Correction 
Indicator)
 
4a[/30x] or 
4a[[/DS/1a/1a]/23x] or 
4a[/30x/2n] 
 
DINO 
DINC 
 
 
Edit: 
Must correspond to Date 
literal: 
If Date literal = DDRD, then 
Info Type = DINO or DINC 
 
The /DS/ part of Sub field 2 
is required if Info Type =  
DINO or DINC (if not 
provided, the system will 
enter/DS/6/3 and truncate 
the 30-byte description, if 
provided, to 23 bytes). It’s 
not allowed otherwise. 
The two fields following/DS/, 
together with 35B:Security 
Issue and 04A:Effective Date 
constitute a unique key. A 
35H:Amount can be sent per 
Security Issue, Effective Date 
and any combination of these 
fields.
 
:IT:DINO/DS/6/3 
 
 
 
Original Negative Rate 
Correction to Negative Rate 
 
 
 
 
 

---

## Page 40

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 40 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format/Allowed Input 
Values/Input Edit Criteria 
Example/Comment/MFPS 
Output (When Not Same as 
Input) 
OC 35H Cash 
Amount 
 
(effective 
11/23/20) 
 
Amount 
(Negative 
Rate) 
3a14number 
 
3a = ISO currency 
code: USD, EUR, GBP, AUD, 
CAD, CHF, CNY, HKD, JPY, 
NOK, SEK or SGD 
 
14number = amount 
 
Edit: 
1. Max digits in amount 
must correspond to Info 
Type as follows: 
Info Type (Negative Rate 
Correction Indicator) = 
DINO or DINC, then max 
digits = 4n.9n 
2. Required and must be > 
0 when Info Type 
(Negative Rate 
Correction Indicator) = 
DINO 
3. Required (but allowed to 
be zero) if Info Type 
(Negative Rate 
Correction Indicator) = 
DINC 
4. Not allowed if Info Type 
(Negative Rate 
Correction Indicator) 
DINO or DINC is not 
provided. 
For JPY Currency, a decimal 
point (,) followed by nine 0’s 
is required after the value. 
This field will contain the 
actual Negative Rate  
 
 
Example for USD Only: 
 
A negative rate of 0.0023 
would be expressed as: 
:IT:DINO 
:35H:USD 0,0023 
 
 
Examples for JPY Only: 
 
A negative rate of 2050 Yen 
would be expressed as: 
:IT:DINO 
:35H:JPY 2050,000000000 
 
 
 
  

---

## Page 41

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 41 
Message Types 55Z 
Message Type 55Z – Generated by [[NSCC]] to communicate to the Fund a Rejected input message (55Y). 
Notes: 
1. MFPS uses this message for rejection only. 
2. All fields except Reference number and Status / Reason Code are copied from input and may not conform to the 
formatting rules specified below if they didn’t conform on input. 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format Example / Comment 
M 20 Transaction 
Reference 
number 
Reference number 16x :20:NSCC152631234567 
MFPS uses same format as 
for message 55X 
M 21 Related 
Reference 
Number 
Related Reference 
Number 
16x Can be used to relate this 
message to a previous 
message. 
MFPS puts here the 
Reference Number of the 
rejected message 
M 24C Reason / Status 
Code 
Status / Reason 
Code 
4a[/4x] 
RJCT 
ACPT 
 
MFPS uses RJCT only. 
MFPS always put Reject code. 
24C:RJCT/0101 
This can be used to specify 
a reason/status where the 
message is used to report 
on the status of a previously 
sent message. In addition to 
the status reject or accept) 
defined codes, bilaterally 
agreed upon reason codes 
may be used in this field. 
The agreed upon codes 
must be preceded by a 
slash. The reason codes for 
rejection within MFPS are to 
be defined.) To report 
multiple status codes the 
/4x is repeated; 
Example: 
24C:/RJCT/0101/0102/0103 
RJCT: This message 
reports the rejection by 
[[NSCC]] of a message 
previously sent by a fund. It 
will be followed by a reject 
reason code(s) 
ACPT: message 
acceptance 

---

## Page 42

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 42 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format Example / Comment 
M TT  Transaction Type MFRP 
MFMP 
MFDD 
 
MFSI 
Mutual Fund Rate and Price 
Mutual Fund [[Member]] 
Profile 
Mutual Fund [[Dividend]] 
Declaration 
Mutual Fund Security Issue 
Information 
M 04A Date (universal) 
 
Date price / rate is 
submitted 
SUBD/yyyymmdd Date effective for following 
repeating sequences of 
prices, daily accrual and 
cumulative rates except 
when Info Type is PRMO or 
PRMC. 
If Info Type is PRMO or 
PRMC, this is the 
Submission Date only. 
Example: 
:04A:SUBD/20200927 = 
Price file submitted on Sept 
27, 2020 
M 05G Time Time hhmmss[/2a/16x] time 
2a = ISO country code  
16x = local description 
:05G:165330/US/NYC 
The ISO country code and 
associated local description 
are optional. If these values 
are not entered the time 
presented is defined as 
New York City, USA time 
(aka East Coast time) 
Repeating Sequence level 1, Security Issue Section 
M 35B Security Security Issue 
Number, Symbol 
and Description 
ISINb12a 
[35x] or [/TS/1a/8a]  
[3*35x] 
Example for USD Only: 
:35B:ISIN 
US2245427719/TS/P/ABCD
X BANKAMERICA CO 
COMMON USD1 
Repeating Sequence level 2 (within Repeating Sequence level 1), Price/Rate section 
M 24C Reason / Status 
Code 
Status / Reason 
Code 
4a/4x 
RJCT 
ACPT 
 
MFPS uses RJCT only 
:24C:RJCT/0101 
This can be used to specify 
a reason / status where the 
message is used to report 
on the status of a previously 
sent message. In addition to 
the status (reject or accept) 
defined codes, bilaterally 
agreed upon reason codes 
may be used in this field 

---

## Page 43

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 43 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format Example / Comment 
(See MFPS Status 
code/Reject code list at the 
end of this document). The 
agreed upon codes must be 
preceded by a slash. To 
report multiple status codes 
the /4x is repeated; 
Example: 
:24C:/RJCT/0101/0102/010
3 
RJCT: This message 
reports the rejection by 
[[NSCC]] of a message 
previously sent by a fund. It 
will be followed by a reject 
reason code(s) 
ACPT: message 
acceptance 
OC 04A Date (universal) 
 
Effective Date for 
price or rate 
PRCE/yyyymmdd 
DDRD/yyyymmdd 
 
CUDR/yyyymmdd 
Required if Info Type is PRMO 
or PRMC. 
This is the Price strike date. 
For example, if the fund 
provides a price at 12pm on 
9/10/20, the ”Effective Date” of 
this price will be “20200910”. 
Date effective for the NAV 
Date effective for daily 
accrual rate 
Date effective for 
cumulative rate 
This date field is to be used 
to indicate a price for a date 
other than that identified in 
the non-repeating portion of 
the record. 
Example: 
:04A:PRCE/20200927 = 
NAV for Sept 27, 2020 

---

## Page 44

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 44 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format Example / Comment 
M IT Cash Type 
 
Information Type 4a[/30x] or 
4a[[/DS/1a/1a]/23x] 
or 
4a[/30x/2n] 
 
PRCO 
 
PRMO 
 
DIVO 
CUMO 
PRCC 
 
 PRMC 
 
DIVC 
CUMC 
 
 
2n – Required if Info Type is 
PRMO or PRMC. Numeric with 
valid values: 01, 02, 98, 99. 
This value will indicate whether 
a particular price is the 1st, 
2nd, etc. price of the day. 
:IT:PRCO 
:IT:DIVO/DS/6/3 
 
:IT:PRMO/01 
 
Single NAV Fund – Original 
Price 
Multiple NAVs Fund - 
Original Price 
Rate 
Cumulative [[Dividend]] Rate 
Single NAV Fund – 
Correction to Price 
Multiple NAVs Fund - 
Correction to Price 
Rate Correction  
Cumulative [[Dividend]] Rate 
Correction 
 
if Sub-field 2 starts with 
/DS/, it is followed by two 
one-byte fields describing 
Rate as follows: 
1. Distribution Type: 
1 = Short Term Capital 
Gain 
2 = Long Term Gain 
3 = Gain on 
Collectables 
4 = Section 1202 Gain 
5 = Unrecaptured 
Section  1250 Gain 
6 = Daily Accrual 
[[Dividend]] 
7 = [[Equity]] [[Dividend]] 
2. Distribution Indicator: 
1 = Spillover 
3 = Regular Distribution 
It then can further define 
cash Type with up to 23 
characters (30 if the /DS/ 
section is not included). 

---

## Page 45

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 45 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format Example / Comment 
M 35H Cash Amount Amount (NAV, 
Rate or 
Cumulative 
[[Dividend]] Rate) 
[N]3a19number 
 
N = indicates a negative 
amount 
3a = ISO currency code: USD, 
EUR, GBP, AUD, CAD, CHF, 
CNY, HKD, JPY, NOK, SEK or 
SGD 
19number = amount 
 
For JPY Currency, a decimal 
point (,) followed by nine 0’s is 
required after the value. 
This field will contain the 
actual NAV, Rate or 
Cumulative rate. 
Example for USD Only: 
1. A [[Dividend]] rate of 
0.0023 per share would 
be expressed as: 
:IT:DIVO 
:35H:USD 0,0023 
 
2. A zero rate would be 
expressed as: 
:IT:DIVO 
:35H:USD 0, 
 
Examples for JPY Only: 
 
1. A price of 111 Yen per 
share would be 
expressed as: 
:IT:PRCO 
:35H:JPY 
111,000000000 
 
2. A rate of 2050 Yen 
would be expressed as: 
:IT:DIVO 
:35H:JPY 
2050,000000000 
 
3. A cumulative rate of 
8431 Yen would be 
expressed as: 
:IT:CUMO 
:35H:JPY 
8431,000000000 

---

## Page 46

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 46 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format Example / Comment 
OC 05G Time 
 
Price (NAV) Start 
Time 
hhmmss/PST Eastern Time 
The start time of the price is 1 
(one) second after the previous 
price was provided. For 
example, the fund may strike a 
price three times a day: 9am, 
12pm and 3pm. The “Price 
(NAV) Start Time” of the 12pm 
price will be “090001” 
(9:00:01am). 
Similarly, the “Price (NAV) 
Start Time” of the 9am price 
will be “150001” 
(3:00:01pm) since the previous 
price was calculated at 3pm on 
the previous day. 
 
Required if Info Type is PRMO 
or PRMC. 
:05G:090001/PST 
OC 04A Date (universal) 
 
Price (NAV) Start 
Date 
PMSD/yyyymmdd 
 
Date of the price start time.  
For example, if the fund strikes 
a price at 12pm on 9/10/15, the 
“Price (NAV) Start Date” will be 
“20150910”. If the fund strikes 
a price at 3pm on 9/9/15 and 
the next one at 9am on 
9/10/15, the “Price (NAV) Start 
Date” of the 9am price will be 
“20150909” (9/9/2015). 
 
Required if Info Type is PRMO 
or PRMC. 
Example: 
:04A:PMSD/20150909  = 
Price (NAV) Start Date is 
September 9 , 2015 

---

## Page 47

Price and Rate ISO Formatted Record Layouts 
Block 4 – Messages Text 47 
M/O 
/OC 
Tag SWIFT Field 
Name 
Mutual Fund 
Profile Field 
Name 
MFPS Format Example / Comment 
OC 05G Time 
 
Price (NAV) Strike 
Time 
hhmmss/PET Eastern Time 
 
This field must contain the 
strike time of the price.  For 
example, if the fund strikes a 
price at 3pm, the “Price (NAV) 
Strike Time” will be “150000” 
(3pm). 
Required if Info Type is PRMO 
or PRMC. 
:05G:1500000/PET 
OC DD  [[Dividend]] Day 
Count 
3n This field will contain the 
number of days of a daily 
accrual for [[Dividend]] rate or 
cumulative [[Dividend]] rate. 
Example: 
Accrual for 3 days would be 
expressed as: 
:DD:003 
O IT Cash Type 
 
(effective 
11/23/20) 
Information Type  
(Negative Rate 
Correction 
Indicator)
 
4a[/30x] or 
4a[[/DS/1a/1a]/23x] or 
4a[/30x/2n] 
 
DINO 
DINC 
:IT:DINO/DS/6/3 
 
 
 
Original Negative Rate 
Negative Rate Correction 
OC 35H Cash Amount 
 
(effective 
11/23/20) 
Amount 
(Negative Rate) 
3a14number 
 
3a = ISO currency 
code: USD, EUR, GBP, AUD, 
CAD, CHF, CNY, HKD, JPY, 
NOK, SEK or SGD 
 
14number = amount 
 
 
 
This field will contain 
the actual Negative Rate  
 
Example for USD Only: 
A negative rate of 
0.0023 would be 
expressed as: 
:IT:DINO 
:35H:USD 0,0023 
Examples for JPY Only: 
A negative rate of 2050 
Yen would be expressed 
as: 
:IT:DINO 
:35H:JPY 
2050,000000000 
      

---

## Page 48

Price and Rate ISO Formatted Record Layouts 
General Input/Output Structure 48 
GENERAL INPUT/OUTPUT STRUCTURE 
This section describes the general structure that MFPS allows for input messages and creates for output 
messages. 
Field Separators 
The following are S.W.I.F.T. rules regarding field separators in the message text (block 4): 
1. Fields are separated by a CrLf. 
2. The first field is preceded by a CrLf. 
3. The last field is followed by a CrLf. 
4. When the format of a sub-field is shown on a separate line than the format of the main field (e.g. field 35B) 
the sub-field is separated from the main field by a CrLf. 
5. When the format of a field or a sub-field indicates number of lines (as the format n*n), the lines are 
separated by a CrLf. 
 
MFPS follows S.W.I.F.T. rules regarding field separators with the exception as noted in section 6.3.3 below. 
Carriage Return/Line Feed (CrLf) 
Carriage Return/Line Feed (CrLf) is a two-byte field which has different meaning and representation in EBCDIC 
based systems (as IBM mainframe) and ASCII based systems (as most PC’s and LAN’s). 
CrLf in EBCDIC Based Systems 
1. Hexadecimal representation is ’0D25’. 
2. Does not indicate end of line (or record) and does not cause the next character to start a new line (or 
record). 
3. Does not have a displayable representation. 
4. Can be seen when browsing or editing a file if the browsing or editing software has the capability of 
showing characters in their hexadecimal representation. 
 
CrLf in ASCII Based Systems 
1. Hexadecimal representation is ’0D0A’. 
2. Indicates end of line (or record) and causes the next character to start a new line (or record). 
3. May have a displayable representation (depends on the system). 
4. Cannot be seen when browsing or editing a file by standard browsing or editing software. Existence is 
indicated by the fact that one line ends and another line starts. 

---

## Page 49

Price and Rate ISO Formatted Record Layouts 
General Input/Output Structure 49 
Input/Output Formats 
MFPS accepts input and creates output in either of two formats: 
Format 1 
1. The whole message is one record as follows: 
{1: [[BASIC]] Header Block}{2: Application Header Block}{4: Text Block}{5: Trailer Block} 
2. CrLf (where required) is present with its EBCDIC representation (‘0D25’). 
 
Example: The following is an example (USD Only) of block 4 (CrLf is indicated by the symbol <0D25>. The 
block is wrapped around because the page is not wide enough): 
{4:<0D25>:20:550319950928<0D25>:TT:MFRP<0D25>:04A:SUBD/19950928<0D25>:05:174045US 
BOSTON<0D25>:35B:ISIN US999999990<0D25>TEST SECURITY ISSUE<0D25>FOR EXAMPLE 
ONLY<0D25>IT:PRCO<0D25>:35H:USD7,01<0D25>:IT:DIVO<0D25>:35H:USD0,001344<0D25>: 
DD:001<0D25>-} 
 
Format 2 
1. The message is made of multiple records 
2. CrLf is not present 
3. When CrLf is required, the record ends and the next character starts a new record. 
 
Example: The following is an example (USD Only) of this format (each line is a separate record in the input 
file): 
{1:F015505MFPXXXXX0000000000}{2:I55YNSCCMFPXXXXXN2002}{4:                                
:20:550319950928                                                                                                                                       
:TT:MFRP 
:04A:SUBD/19950928 
:05G:174045USBOSTON 
:35B:ISIN US999999990 TEST SECURITY ISSUE FOR EXAMPLE ONLY 
:IT:PRCO 
:35H:USD7,01 
:IT:DIVO 
:35H:USD0,001344 
:DD:001 
-} {5:{MAC:TRAILER}} 
 

---

## Page 50

Price and Rate ISO Formatted Record Layouts 
General Input/Output Structure 50 
Batch Input 
MFPS receives batch input through Datatrak variable length files (RECFM=VB) or fixed length files 
(RECFM=FB). The following limitations apply: 
Variable Length File 
1. Maximum record length is 3300 bytes (LRECL = 3304). 
2. Maximum message length is 3300 bytes. 
Note: 
When using Format 2 (as described above) the two bytes CrLf must be counted (even though they are not present) for 
every end of line, for the limit of 3300 bytes. 
3. Up to 20 secondary repeating sequences (Price/Rate sections) are allowed within a primary repeating 
sequence (Security Issue section). 
 
Fixed Length File 
1. Only Format 2 (as described above) is allowed. 
2. Record length is 80 bytes (LRECL = 80). 
3. Maximum message length is 3300 bytes. 
Note: 
Note the two bytes CrLf must be counted (even though they are not present) for every end of line, for the limit of 3300 
bytes. 
4. Up to 20 secondary repeating sequences (Price/Rate section) are allowed within a primary repeating 
sequence 1 (Security Issue section). 
Batch Output 
MFPS submits batch output through AutoRoute variable length files (RECFM=VB) or fixed length files 
(RECFM=FB). The following apply: 
Variable Length File 
1. Only Format 1 (as described above) is created. 
2. Maximum record (message) length is 3500 bytes (LRECL = 3504). 
3. Up to 20 secondary repeating sequences (Price/Rate sections) are created within a primary repeating 
sequence (Security Issue section). 
Note: 
When transferring an output file to an ASCII base system (as a PC or LAN) it might look like Format 2 as described above 
since EBCDIC CrLf will be translated to ASCII CrLf and create a new line. 

---

## Page 51

Price and Rate ISO Formatted Record Layouts 
General Input/Output Structure 51 
Fixed Length File 
1. Only Format 2 (as described above) is created. 
2. Record length is 90 bytes (LRECL = 90). 
3. Maximum message length is 3500 bytes. 
4. Up to 20 secondary repeating sequences (Price/Rate sections) are created within a primary repeating 
sequence (Security Issue section). 
Interactive Input 
MFPS receives interactive input through MQM queues. The following apply: 
1. Only Format 1 (as described above) is allowed. 
2. Maximum record (message) length is 3300 bytes. 
3. Up to 20 secondary repeating sequences (Price/Rate sections) are allowed within a primary repeating 
sequence (Security Issue section). 
Interactive Output 
MFPS submits interactive output through MQM queues. The following apply: 
1. Only Format 1 (as described above) is created. 
2. Maximum record (message) length is 3500 bytes. 
3. Up to 20 secondary repeating sequences (Price/Rate sections) are created within a primary repeating 
sequence (Security Issue section). 

---

## Page 52

Price and Rate ISO Formatted Record Layouts 
Output Messages 52 
OUTPUT MESSAGES 
Rejected Input Message 
• [[NSCC]] will generate Message Type 55Z to communicate Price and Rate information rejected by [[NSCC]]. 
• Reject Message 55Z will contain all fields (with the exception of the “Transaction Reference Number”) as 
provided on the rejected input message. 
• [[NSCC]] will generate the “Transaction Reference Number” on Message Type 55Z. [[NSCC]] will populate the 
“Related Reference Number” tag (tagged with ‘21’) with the “Transaction Reference Number” from the 
rejected input message. 
• [[NSCC]] reject reason code will be provided in tag ‘24C’. 
 
Accepted Price and Rate Information 
• [[NSCC]] will distribute accepted Price and Rate information via Message Type 55X 
• [[NSCC]] will generate the “Transaction Reference Number” for every output message 55X. 
 
Handling of Multiple Price and Rate Submissions for the same Security Issue [[ID]] and Effective Date. 
a. Price – Single (NAV) Fund 
A fund might submit an original price and one/multiple price corrections within the same cycle for the same 
Security Issue [[ID]] and Effective Date. In this scenario only the latest price correction received during this cycle 
will be distributed by [[NSCC]] (the original price will not be distributed). As a result, clients may receive a 
correction to price without previously receiving the original price. Clients should treat this price correction as the 
latest most up-to-date* price for the same combination of Security Issue [[ID]] and Effective Date. 
Note* 
A fund might submit another price correction (or multiple corrections) for the same combination of Security Issue 
[[ID]] and Effective Date in a subsequent cycle. The latest price correction will be distributed in the cycle it was 
received. 
b. Price – Multiple NAVs Fund 
A fund might submit an original price and one/multiple price corrections within the same cycle for the same 
Security Issue [[ID]], Effective Date and Price (NAV) Indicator. In this scenario only the latest price correction 
received during this cycle will be distributed by [[NSCC]] (the original price will not be distributed). As a result, 
clients may receive a correction to price without previously receiving the original price. Clients should treat this 
price correction as the latest most up-to-date* price for the same combination of Security Issue [[ID]], Effective 
Date and Price (NAV) Indicator. 
Note* 
A fund might submit another price correction (or multiple corrections) for the same combination of Security Issue 
[[ID]], Effective Date and Price (NAV) Indicator in a subsequent cycle. The latest price correction will be distributed in 
the cycle it was received. 

---

## Page 53

Price and Rate ISO Formatted Record Layouts 
Output Messages 53 
c. [[Dividend]] Rate 
A fund might submit an original [[Dividend]] rate and one/multiple [[Dividend]] rate corrections within the same cycle 
for the same Security Issue [[ID]], Effective Date, Distribution Type and Distribution Indicator. In this scenario only 
the latest [[Dividend]] rate correction received during this cycle will be distributed by [[NSCC]] (the original [[Dividend]] 
rate will not be distributed). As a result, clients may receive a correction to [[Dividend]] rate without previously 
receiving the original [[Dividend]] rate. Clients should treat this [[Dividend]] rate correction as the latest most up-to-
date* [[Dividend]] rate for the same combination of Security Issue [[ID]], Effective Date, Distribution Type and 
Distribution Indicator. 
Note* 
A fund might submit another [[Dividend]] rate correction (or multiple corrections) for the same combination of 
Security Issue [[ID]], Effective Date, Distribution Type and Distribution Indicator in a subsequent cycle. The latest 
[[Dividend]] rate correction will be distributed in the cycle it was received. 
d. Cumulative Rate 
A fund might submit an original cumulative rate and one/multiple cumulative rate corrections within the same 
cycle for the same Security Issue [[ID]] and Effective Date. In this scenario only the latest cumulative rate 
correction received during this cycle will be distributed by [[NSCC]] (the original cumulative rate will not be 
distributed). As a result, clients may receive a correction to cumulative rate without previously receiving the 
original cumulative rate. Clients should treat this cumulative rate correction as the latest most up-to-date* 
cumulative rate for the same combination of Security Issue [[ID]] and Effective Date. 
Note* 
A fund might submit another cumulative rate correction (or multiple corrections) for the same combination of 
Security Issue [[ID]] and Effective Date in a subsequent cycle. The latest cumulative rate correction will be distributed 
in the cycle it was received. 

---

## Page 54

Price and Rate ISO Formatted Record Layouts 
Rejected Messages 54 
REJECTED MESSAGES 
MFPS may accept or reject the whole input message, accept some Security Issue sections within the message 
and reject others, or accept some Price/Rate sections within Security Issue section and reject others. The 
different rejection types are described below. 
Whole Message Rejection 
The whole input message is being rejected. MFPS will create an output Reference Number, will move the input 
Reference Number into output Related Reference Number, and will copy the input message starting from the 
first character after the input Reference Number (or Related Reference Number if presence) into the output 
message. 
This type of rejection occurs when an error is found in a part of the message which ‘belong’ to the whole 
message. The following are some of the reasons for Whole Message Rejection: 
1. An error in the message headers 
2. An error in the message trailer 
3. An error in the fixed portion of the message text (block #4) 
 
A status code ‘WHLE’ in field 24C (Status/Reason Code) in the fixed section of the output message will 
indicate this kind of rejection. 
Partial Forward Message Rejection 
The input message is being rejected from a specific point to the end. Some Security Issue sections may have 
already been accepted or rejected before this point (see section 6.6.3). MFPS will create an output Reference 
Number, will move the input Reference Number into output Related Reference Number, and will copy the input 
message starting from point of rejection (usually the start of a Security Issue section) to the output message. 
Any input security issue which have been rejected before this point will be presence in the output message 
before that point. The order of data in the output message is the same as in the input message. 
This type of rejection occurs when a structural error is found in the input message. The following are some of 
the reasons for Partial Message Rejection: 
1. Unrecognized tag 
2. A mandatory field is missing 
3. Field or sub-field is longer than allowed. 
 
A status code ‘PRTL’ in field 24C (Status/Reason Code) in the fixed section of the output message will indicate 
this kind of rejection. Security issue sections which have been rejected before the point of partial rejection will 
carry reject codes in field 24C of the Price/Rate section which caused that rejection. 

---

## Page 55

Price and Rate ISO Formatted Record Layouts 
Rejected Messages 55 
Security Issue Rejection 
The whole Security Issue section is rejected. 
This type of rejection occurs when non-structural errors are found in the Security Issue field. The following are 
some of the reasons for Security Issue Rejection: 
1. Security Issue check digit is invalid 
2. Security Issue invalid for submitting fund 
3. Security Issue description invalid 
 
A status code ‘SECI’ in field 24C (Status/Reason Code) in the first Price/Rate section of the rejected Security 
Issue section will indicate this kind of rejection. The reason for rejection will follow this status code in that field. 
Other reject codes in this Price/Rate section and following Price/Rate sections in this Security Issue section will 
indicate if any of them is invalid as well. Price/Rate sections with no error will carry field 24C with the literal 
RJCT only and no reject codes. 
Price/Rate Rejection 
A Price/Rate section is rejected. The Security Issue section in the reject message will include rejected 
Price/Rate sections only. 
This is the ‘normal’ rejection type. It is caused by any non-structural error in a Price/Rate section field. The 
following are some of the reasons for Price/Rate Rejection: 
1. Amount is not numeric or decimal comma is missing or out of place 
2. Invalid date or time 
3. A literal does not match any of the allowed literal for this field or sub-field 
4. Field or sub-field is shorter than allowed 
5. Invalid character (not allowed by the S.W.I.F.T. network) 
 
 
 

---

## Page 56

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 