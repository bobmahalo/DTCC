---
title: "Fund/SERV - Variable Length Record Layouts (Part 2)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_variable_part2_layout_mfs317_20230907.pdf"
pages: 59
size: "769.6 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Fund/SERV - Variable Length Record Layouts (Part 2)

**Original File:** [fs_variable_part2_layout_mfs317_20230907.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_variable_part2_layout_mfs317_20230907.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 59  
**File Size:** 769.6 KB  

---

## Page 1

 
 
 
Fund/SERV® 
VARIABLE LENGTH RECORD LAYOUTS (PART 2) 
SEPTEMBER 7, 2023 
 

---

## Page 2

Variable Length Record Layouts (Part 2) 
Cash Adjustment (011) 2 
HISTORY OF CHANGES 
Dates Important Notices 
September 7, 2023 Record has been rebranded and reviewed. 
March 10, 2023 • 529 Account Plan fields added to 018 and 019 records (effective May 15, 
2023). 
  Please see Important Notice:  
  a9267 P&S 8840 Dated February 10, 2023 
• Summary of Changes has been moved to back of document 
• Record has been rebranded 
Effective Date: March 28, 2022 Please see Important Notices: 
a9045 P&S 8618 & a9044 P&S 8617 Dated September 2, 2021 
December 7, 2021 Document links updated due to launch of new Learning Center 
Effective Date: March 25, 2019 Please see Important Notice: 
a8658 P&S a8233 Dated December 19, 2018 
Effective Date: November 20, 2017 Please see Important Notice: 
a8402 P&S 7977 Dated June 1, 2017 
Effective Date: September 26, 2016      Please see Important Notice: 
a8159 P&S 7734 Dated February 3, 2016 
Effective Date: February 29, 2016 Please see Important Notice: 
a8107 P&S 7682 Dated October 27, 2015 
Effective Date:  July 27, 2015 Please see Important Notice:  
a7997 P&S 7572 Dated March 12, 2015 
Effective Date:  April 27, 2015 Please see Important Notice:  
a7926 P&S 7501 Dated November 4, 2014 
Documentation Changes a7865  P&S 7435 Dated July 2, 2014 
Effective Date:  July 28, 2014 Please see Important Notice:  
a7701 P&S 7371 Dated May 15, 2014 (REVISED) 
a7701 P&S 7371 Dated March 17, 2014 
Effective Date:  November 18, 2013 Please see Important Notice:  
a7665 P&S 7235 Dated July 3, 2013 
Effective Date:  March 18, 2013 Please see Important Notice:  
a7472 P&S 7042 Dated August 16, 2012 (enhancement details) 
a7567 P&S 7137 Dated January 9, 2013 (revised dates) 
a7570 P&S 7140 Dated January 11, 2013 
Documentation Changes Please see Important Notice: 
a7592 P&S 7162 Dated March 1, 2013 

---

## Page 3

Variable Length Record Layouts (Part 2) 
Cash Adjustment (011) 3 
Dates Important Notices 
Effective Date:  April 23, 2012 Please see Important Notice:  
A7355 P&S 6925 Dated January 12, 2012 
Note: On 2/27/2012 a correction was made to 401 Records to reflect the 
changes that were made in accordance with Important Notice a6272 P&S 
5842.   
The Fund Account Indicator 4 (New Account – U.S. Tax Resident Living Abroad) 
has been added to Account Representative Name, Account Representative 
Number and Branch Identification Number fields as part of conditional 
requirements. 
Effective Date:  December 5, 2011 Please see Important Notice:  
a7256 P&S 6826 Dated July 29, 2011 
Effective Date:  October 17, 2011 Please see Important Notice:  
a7241 P&S 6811 Dated July 8, 2011 
Effective Date: June 13, 2011 Please see Important Notice:  
a7175 P&S 6745 Dated March 7, 2011 
Effective Date: January 18, 2011 Please see Important Notice:  
a7079 P&S 6650 Dated October 18, 2010 
Effective Date: November 22, 2010 Please see Important Notice:  
a7044 P&S 6615 Dated August 17, 2010 
Effective Date: December 7, 2009 Please see Important Notice:  
a6874 P&S 6444 Dated September 17, 2009 
Effective Date: October 5, 2009 Please see Important Notice:  
a6819 P&S 6389 Dated May 8, 2009  
Effective Date: December 1, 2008 Please see Important Notices:  
a6667 P&S 6237 Dated July 29, 2008 
a6653 P&S 6223 Dated July 7, 2008 
a6620 P&S 6190 Dated May 20, 2008 

---

## Page 4

Variable Length Record Layouts (Part 2) 
Cash Adjustment (011) 4 
TABLE OF CONTENTS 
Cash Adjustment (011) ........................................................................................................................................ 5 
02.08.01 Cash Adjustment (011) ........................................................................................................................ 5 
Short Registration (400) ...................................................................................................................................... 9 
02.09.01 Short Registration (400)....................................................................................................................... 9 
Full Registration (401) ....................................................................................................................................... 12 
02.10.01 Full Registration (401) .......................................................................................................................12 
ACATS Transfer (018) ........................................................................................................................................ 28 
02.11.01 ACATS Transfer (018) .......................................................................................................................28 
ACATS Transfer Acknowledgment/Rejection (019) ........................................................................................ 41 
02.12.01 ACATS Transfer Acknowledgment/Rejection (019) ..........................................................................41 
Transfer of Retirement [[Asset]] (ToRA) (210) ..................................................................................................... 45 
02.13.01 Transfer of Retirement [[Asset]] (ToRA) (210) .......................................................................................45 
ToRA Acknowledgment (211); ToRA Confirmation (212); ToRA Reconfirmation (213)  .............................. 48 
02.14.01 ToRA Acknowledgment (211) ............................................................................................................48 
Defined Contribution Plan (DCP Information) (002) ....................................................................................... 52 
02.15.01 Defined Contribution Plan (DCP Information) (002) ..........................................................................52 
Retiring [[participant]] (090) ................................................................................................................................... 55 
02.16.01 Retiring [[participant]] (090) ...................................................................................................................55 
 
 
 

---

## Page 5

Variable Length Record Layouts (Part 2) 
Cash Adjustment (011) 5 
CASH ADJUSTMENT (011) 
02.08.01 Cash Adjustment (011) 
When ToRA related (ToRA Indicator = ‘1’ or ‘2’), Firm means Receiving Fund, and Fund means 
Delivering Fund 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0197 R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N A = Investment Agent 
B = Firm 
F = Fund 
T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 10 11 2 A/N Space R  
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 011 = Cash Adjustment 
 
R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space  R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use  R  

---

## Page 6

Variable Length Record Layouts (Part 2) 
Cash Adjustment (011) 6 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Type 43 44 2 A/N Required if 24 (Money Market) and 
ToRA Indicator = space  
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file.  [[NSCC]] leverages the 
Fund/SERV Security master file 
to determine value and 
associated processing rules. 
Output: [[NSCC]] populates with 
the value in the Fund/SERV 
Security master file. 
OC 150 
Control Number 45 59 15 A/N  R 005 
Filler 60 61 2 A/N Space  R  
Reason Code 62 63 2 A/N 01 = [[Dividend]] deduct 
02 = [[Dividend]] accrual 
03 = [[Dividend]] payout 
04 = Commission billing 
05 = Commission adjustment  
06 = Systematic withdrawal 
07 = Contingent deferred sales 
charge 
08 = Long term capital gain 
09 = Short term capital gain 
10 = Market fluctuation  
11 = Return of dealer allowance 
99 = Other  
R 032 
Submission Date 64 71 8 N mmddccyy  R 101 
ToRA (Transfer of 
Retirement [[Asset]]) 
Indicator 
72 72 1 A/N 1 = ToRA related (submitted by the 
receiving fund) 
2 = ToRA related (submitted by the 
delivering fund) 
Space = Not ToRA related 
R 186 
Filler 73 82 10 A/N Space R  

---

## Page 7

Variable Length Record Layouts (Part 2) 
Cash Adjustment (011) 7 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[settlement]] Override 
Reason Code  
83 84 2 A/N Required if Anticipated [[settlement]] 
Date is provided. 
01 = Wrap fee account 
02 = 401K 
03 = Other 
OC 179 
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Required if: 
Originator Type =( T or A or V) 
OR  
Membership Identifier = 02 or 03 
OC 188 
Filler 93 104 12 A/N Space R  
Adjustment Amount 105 120 16 N 99,999,999,999,999.99 R 033 
Currency Indicator 121 123 3 A/N  O 110 
Debit/Credit Code 124 125 2 A/N DB = Debit firm 
CR = Credit firm 
R 034 
Original Control Number 126 140 15 A/N Required if ToRA Indicator = 1 or 2 OC 163 
Original Correction 
Indicator 
141 141 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / 
cancellation 
Space = No correction 
O 164 
Memo Field 142 150 9 A/N  O  
Anticipated [[settlement]] 
Date 
151 158 8 A/N mmddccyy 
Required if [[settlement]] Override 
Reason Code is provided 
O 180 
Filler 159 173 15 A/N Space R  

---

## Page 8

Variable Length Record Layouts (Part 2) 
Cash Adjustment (011) 8 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Membership Identifier 174 175 2 A/N 01 = Trust [[Member]] 
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 176 197 22 A/N Space R  

---

## Page 9

Variable Length Record Layouts (Part 2) 
Short Registration (400) 9 
SHORT REGISTRATION (400) 
02.09.01 Short Registration (400) 
For subsequent purchases only  
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0197 R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N B = Firm 
S = Service Provider for B = Firm 
R 187 
Filler 10 11 2 A/N Space R  
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 400 = Short Registration R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  

---

## Page 10

Variable Length Record Layouts (Part 2) 
Short Registration (400) 10 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Type 43 44 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value 
against the Fund/SERV Security 
master file.  [[NSCC]] leverages the 
Fund/SERV Security master file 
to determine value and 
associated processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 45 59 15 A/N  R 005 
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / 
cancellation 
Space = No correction 
R 006 
Filler 61 63 3 A/N Space R  
Submission Date 64 71 8 N mmddccyy R 101 
Filler 72 79 8 A/N Space R  
Book/Physical Share 
Indicator 
80 80 1 A/N 0 = Book [[shares]] - firm name 
1 = Book [[shares]] - customer name  
2 = Physical [[shares]] 
Must be 0 or 1 for Money Market 
trades 
R 015 PI Delivery Indicator 81 81 1 A/N Required if Book/Physical Share 
Indicator = 2.  
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm 
OC 039 
Filler 82 84 3 A/N Space R  
[[NSCC]] Rejection Indicator 85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  

---

## Page 11

Variable Length Record Layouts (Part 2) 
Short Registration (400) 11 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code 
R  
Filler 89 92 4 A/N Space R  
Service Provider Number 93 96 4 A/N Required if Originator Type = S OC 215 
Filler 97 104 8 A/N Space R  
Filler 105 118 14 A/N Space R  
Customer Name 119 138 20 A/N  R 063 
Filler 139 139 1 A/N Space R  
Customer Account 
Number 
140 159 20 A/N  R 011 
Customer Account 
Number Indicator 
160 160 1 A/N 1 = Fund 
2 = Firm 
R 048 
Agent for Firm Number 161 164 4 A/N  O  
Filler 165 166 2 A/N Space R  
SSN/EIN Indicator 167 167 1 A/N 0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN  
R 102 
SSN/EIN Number 168 176 9 A/N  R 103 
Filler 177 197 21 A/N Space R  

---

## Page 12

Variable Length Record Layouts (Part 2) 
Full Registration (401) 12 
FULL REGISTRATION (401) 
02.10.01 Full Registration (401) 
For either new or subsequent purchases 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length 
  
1 4 4 N 0383, 0476, 0569, 0662, 0755 
(With 0 payables/beneficiaries, Not 
allowed for Section 529 (Registration 
Type = 1)).  
0848, 0941, 1034, 1127  
(With 1 payable/beneficiary) 
1220, 1313, 1406, 1499  
(With 2 payables/beneficiaries) 
1592, 1685, 1778, 1871  
(With 3 payables/beneficiaries) 
1964, 2057, 2150, 2243  
(With 4 payables/beneficiaries) 
2336, 2429, 2522, 2615  
(With 5 payables/beneficiaries) 
2708, 2801, 2894, 2987  
(With 6 payables/beneficiaries) 
3080 
(record length must be 3080 if 
FATCA attributes are included) 3173 
(record length must be 3173 if 
[[intermediary]] Program Indicator, 
Servicing Group, and Additional 
Relationship information is included) 
R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N A = Investment Agent 
B = Firm  
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 10 11 2 A/N Space R  

---

## Page 13

Variable Length Record Layouts (Part 2) 
Full Registration (401) 13 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 401 = Full Registration R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  
Security Issue Type 43 44 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file.  [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 45 59 15 A/N  R 005 
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / 
cancellation 
Space = No correction 
R 006 
Filler 61 63 3 A/N Space R  
Submission Date 64 71 8 N mmddccyy R 101 
Filler 72 79 8 A/N Space R  
Book/Physical Share 
Indicator 
80 80 1 A/N 0 = Book [[shares]] - firm name R 015 

---

## Page 14

Variable Length Record Layouts (Part 2) 
Full Registration (401) 14 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
1 = Book [[shares]] - customer name 
2 = Physical [[shares]] 
Must be 0 or 1 for Money Market 
trades 
PI Delivery Indicator 81 81 1 A/N Required if Book/Physical Share 
Indicator = 2. 
0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm 
OC 039 Filler 82 84 3 A/N Space R  
[[NSCC]] Rejection Indicator 85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
89 92 4 A/N Required if Originator Type = T or P 
or A or V 
OC 188 
Service Provider Number 93 96 4 A/N Required if Originator Type = S or P OC 215 
Filler 97 104 8 A/N Space R  
Filler 105 118 14 A/N Space R  
Customer Name 119 138 20 A/N  R 063 
Fund Account Indicator 139 139 1 A/N 0 = New account – U.S.  
1 = New account – non-U.S.  
2 = Existing account – U.S. 
3 = Existing account – non-U.S.  
4 = New account – US Tax Resident 
Living Abroad  
5 = Existing account – US Tax 
Resident Living Abroad 
R 010 
Customer Account 
Number 
140 159 20 A/N Required for existing account (Fund 
Account Ind = 2 or 3)  
OC 011 
Customer Account 
Number Indicator 
160 160 1 A/N Required if Customer Account 
Number is provided. 
1 = Fund 
OC 048 

---

## Page 15

Variable Length Record Layouts (Part 2) 
Full Registration (401) 15 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
2 = Firm 
Agent for Firm Number 161 164 4 A/N Required if Originator Type = V (TPP) OC 271 
Network Control Indicator 165 165 1 A/N 0 = Non-networked  
3 = Matrix level 3 
4 = Matrix level 4 
R 047 
Registration Type 166 166 1 A/N 0 = Regular registration 
1 = Section 529 registration 
O 235 
SSN/EIN Indicator 167 167 1 A/N 0 = Tax [[ID]] number 
1 = Social security number 
2 = [[investor]] TIN/EIN  
R 102 
SSN/EIN Number 168 176 9 A/N  R 103 
Customer/Owner U.S. 
Citizenship Indicator 
177 177 1 A/N Required for Section 529 registration 
(Registration Type = 1). 
0 = U.S. citizen 
1 = Not U.S. citizen 
OC 236 
Target Date Fund 
Indicator 
178 178 1 A/N 0 = No 
1 = Yes 
O 260 
Age Based Indicator 179 179 1 A/N 1 = Aggressive 
2 = Moderate 
3 = Conservative 
O 267 
Age Based Roll Exempt 
Indicator 
180 180 1 A/N 0 = No, account is not exempt and 
will be included within Automatic Age 
Roll Events 
1 = Yes, account is exempt from 
Automatic Age Roll   Events 
O 268 
Customer/Owner U.S. 
Resident Alien Indicator 
181 181 1 A/N 0 = No 
1 = Yes 
O 269 
Successor Owner 
Indicator 
182 182 1 A/N Required if Section 529 (Registration 
Type = 1). Not allowed otherwise. 
0 = No  
1 = Yes 
OC 270 
Underlying Firm Symbol 
(UFS)  
183 186 4 A/N Number that identifies the Underlying 
Firm (Banks/Trusts/Record 
Keepers/TPA’s) that clear through 
another entity 
O  
Filler  187 197 11 A/N Space R  

---

## Page 16

Variable Length Record Layouts (Part 2) 
Full Registration (401) 16 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[Dividend]] Code 198 198 1 A/N  [[Dividend]] LTCG STCG 
0 =  Cash  Cash  Cash 
1 =  Reinvest  Reinvest  Reinvest 
2 =  Cash  Cash  Reinvest 
3 =  Cash  Reinvest  Reinvest 
4 =  Cash  Reinvest  Cash 
5 =  Reinvest  Cash  Cash 
6 =  Reinvest  Reinvest  Cash 
7 =  Reinvest  Cash  Reinvest 
 
R 123 
Withhold Indicator  199 199 1 A/N W9 indications 
0 = Certified (W-9 on file) 
1 = Failure to provide tin 
2 = Failure to certify tin 
3 = Notification of incorrect TIN from 
the Secretary of Treasury (Withhold 
due to B Notice) 
4 = Failure to certify backup 
withholding status 
5 = Voluntary disclosure from payee 
of affirmative backup withholding 
status 
6 = Notification to commence Backup 
Withholding from Secretary of 
Treasury for underreporting [[Dividend]] 
and/or interest payments (Withhold 
due to C Notice) 
7 = Applied for social security number 
8 = Exempt recipient 
9 = Account(s) subject to both B and 
C Notice Withholding 
W8 indications 
A = Uncertified foreign account (no 
W8 form on file-backup withholding 
necessary) 
B = Certified foreign [[Beneficial Owner]] 
account (form W8-BEN on file) 
C = Certified foreign [[intermediary]] 
account (form W8-IMY on file) 
D = Certified valid foreign account 
(form W8-ECI on file with ITIN) 
R 124 

---

## Page 17

Variable Length Record Layouts (Part 2) 
Full Registration (401) 17 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
E = Certified foreign exempt account 
(form W8-EXP on file) 
F = W8 on file - no treaty rate claimed 
G = W8 Beneficiary with TIN on file 
H = W-8BEN-E on file/documentary 
evidence 
I = Voluntary FATCA withholding - W-
8BEN-E on file/documentary 
evidence 
J = W8-IMY or W-8BEN-E pending 
Payable Information 
Indicator 
200 200 1 A/N 0 = Address of record  
1 = Payable address 
2 = Automatic clearing house 
3 = Cash to firm 
4 = Cross fund reinvest 
5 = Cash to Trust 
R 125 
Customer Name End 
Line Indicator 
201 201 1 A/N 1-6 = Line number where name ends R 126 
Customer Zip Code 202 212 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 
digits for future postal expansion 
R 127 
Social Code 213 214 2 A/N See Social Code List at 
https://dtcclearning.com/documents/
mutual-fund-services-1/mfs-cross-
product/codes-8/2498-social-
codes/file.html under General Codes. 
R 128 
NAV Account Indicator 215 215 1 A/N 0 = No  
1 = Yes 
R 129 
[[Margin]] Account Indicator 216 216 1 A/N 0 = No 
1 = Yes 
R 079 
Check Writing Privileges 
Indicator 
217 217 1 A/N 0 = No 
1 = Yes 
R 083 
State of Sale (State 
Code) 
218 219 2 A/N See state code list in Fund/SERV 
manual 
R 012 
Country of Origin 
(Country Code) 
220 221 2 A/N Required for foreign account (Fund 
Account Ind = 1 or 3).  
In this case, the value 'OC' (Other 
Country) is not allowed 
OC 067 
Account Representative 
Name 
222 236 15 A/N Required for new networked account  
(Network Control Ind = 3 or 4, and 
Fund Account Ind = 0, 1  or 4)  
OC 076 

---

## Page 18

Variable Length Record Layouts (Part 2) 
Full Registration (401) 18 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Account Representative 
Number 
237 245 9 A/N Required for new networked account  
(Network Control Ind = 3 or 4, and 
Fund Account Ind = 0, 1  or 4)  
OC 075 
Branch Identification 
Number 
246 254 9 A/N Required for new networked account 
(Network Control Ind = 3 or 4, and 
Fund Account Ind = 0, 1  or 4) 
OC 035 
New Firm of Record 255 258 4 A/N Space  (for Network use only) R 086 
Number of Payables/ 
Beneficiaries 
259 260 2 N 00-06. 
(00-05 for Money Market purchase 
involving interactive [[participant]]).   
Must be > 00 if Payable Information 
Indicator = 1 or 2  
R 130 W8 Certification Date 261 268 8 N mmddccyy 
Required if Withhold Indicator = B, C, 
D or E  
OC 211 
W8 Expiration Date 269 276 8 N mmddccyy 
Required if Withhold Indicator = D or 
E  
OC 212 
W8 Override NRA 
Special Rate 
277 281 5 N 99.999 O 213 
W8 Qualified 
[[intermediary]] Indicator  
282 282 1 A/N Required if Withhold Indicator = C. 
1 = QI (qualified [[intermediary]] - 
primary withholding) 
2 = QI (Qualified [[intermediary]] - non-
withholding) 
3 = Non-QI (non-Qualified 
[[intermediary]] - non-withholding, not 
the [[Beneficial Owner]]) 
4 = Partnership (withholding) 
5 = Partnership (non-withholding) 
6 = U. S. branch (non-withholding) 
7 = Trust (withholding) 
8 = Trust (non-withholding) 
9 = Territory Financial Institution 
OC 214 
W8 Override Country 
Code 
283 284 2 A/N The value 'OC' (Other Country) is not 
allowed 
O 067 
Standard [[ID]] 285 290 6 A/N  O  
Customer Name/Address 
Line 1 
291 325 35 A/N  R 131 

---

## Page 19

Variable Length Record Layouts (Part 2) 
Full Registration (401) 19 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Customer Name/Address 
Line 2 
326 360 35 A/N  O  
Plan Account Number  361 380 20 A/N Plan account at the Trust, TPA, or 
Record Keeper 
O  
Plan Account Number 
Indicator  
381 381 1 A/N Required if Plan Account Number is 
provided.  
1 = Trust  
2 = TPA  
3= Record Keeper 
O/C 277 Filler 382 383 2 A/N Space R  
Customer Name/Address 
Line 3 
384 418 35 A/N  O  
Customer Name/Address 
Line 4 
419 453 35 A/N  O  
Filler 454 476 23 A/N Space R  
Customer Name/Address 
Line 5 
477 511 35 A/N  O  
Columns 512-546 for regular registration (Registration Type = 0) 
Customer Name/Address 
Line 6  
512 546 35 A/N  O  
Columns 512-546 for Section 529 registration (Registration Type = 1) 
Customer City 512 544 33 A/N  R 238 
Customer State 545 546 2 A/N  R 239 
Filler 547 569 23 A/N Space R  
Memo Field 570 581 12 A/N  O  
ACH (Automatic Clearing 
House) Indicator 
582 582 1 A/N 0 = No 
1 = Yes 
O 081 
Systematic Contribution 
(SIP/PAC/PIP) Indicator 
583 583 1 A/N 0 = No 
1 = Yes 
O 082 
SWP (Systematic 
Withdrawal Plan) 
Indicator 
584 584 1 A/N 0 = No 
1 = Yes 
O 083 
ROA/LOI Value 585 600 16 N 99,999,999,999,999.99  O 028 
LOI Number/Date 601 608 8 A/N  O  

---

## Page 20

Variable Length Record Layouts (Part 2) 
Full Registration (401) 20 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Related Trade Indicator 609 609 1 A/N 0 = No 
1 = Yes 
O 065 
Related Account Number 610 629 20 A/N  O  
Related Account Number 
Indicator 
630 630 1 A/N Required if Related Account Number 
is provided. 
1 = Fund 
2 = Firm 
3 = Customer 
OC 157 
SWP/PAC Effective Date 631 638 8 N mmddccyy O 132 
Customer Gender 639 639 1 A/N F = Female 
M = Male  
O 237 
Filler 640 662 23 A/N Space  R  
CDSC Payment Code 663 663 1 A/N 0 = Gross 
1 = Net 
2 = Not applicable  
O 133 
Disbursement Options 664 664 1 A/N 0 = Fixed cash amount 
1 = Fixed percentage 
2 = Fixed [[shares]] 
3 = Declining balance 
O 134 
Disbursement Amount 665 680 16 N Format according to Disbursement 
[[Option]]: 
0 = 99,999,999,999,999.99 
1 = 999,999.9999999999 
2 = 999,999,999,999.9999 
3 = 999,999,999,999.9999 
O 135 
Monthly Payment 
Indicators 
681 692 12 A/N These 12 bytes represent 12 months 
respectively: 
1st byte  = January, 
2nd byte = February, etc. 
For each byte: 
0 = No payment this month  
1 = Yes payment this month 
O 136 
Payment Date Indicator 693 694 2 A/N 01-31 = Day of month 
L = Last day of month 
N = Normal fund cycle 
O 137 

---

## Page 21

Variable Length Record Layouts (Part 2) 
Full Registration (401) 21 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Retirement Tax Indicator 695 696 2 A/N Required if Payable 1 Address [[Option]] 
is provided and indicates systematic 
withdrawal. 
01 = Premature withdrawal 
02 = Rollover 
03 = Disability 
04 = Death 
05 = Prohibited 
06 = Other 
07 = Normal 
08 = Refund by excess contributions 
09 = Divorce 
10 = Plan revoked 
11 = Fund transfer 
99 = Not applicable 
OC 138 
Shareholder Bank 
Account Number  
697 716 20 A/N  O  
Shareholder Bank 
Account Type 
717 717 1 A/N Required if Shareholder Bank 
Account Number is provided.  
0 = Checking 
1 = Savings 
2 = Other  
OC 139 
First Check Date 718 725 8 N mmddccyy O 140 
ABA Routing Number 726 734 9 A/N Required if Payable Information 
Indicator denotes automatic clearing 
house 
OC 141 
Cost Basis [[Option]] 735 735 1 A/N 0 = Unknown 
1 = FIFO (First In First Out) 
2 = LIFO (Last In First Out) 
3 = High Cost 
4 = Low Cost 
5 = Average Cost 
6 = Select Lot 
O 165 
Filler 736 755 20 A/N Space R  
Start of Payable/Beneficiary 1 section. 
Note: 
The first portion of this section (bytes 756 through 848) has three different formats. Address [[Option]] field (column 788) 
indicates which format is being used as follows: 

---

## Page 22

Variable Length Record Layouts (Part 2) 
Full Registration (401) 22 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
• If Payable 1 Address [[Option]] Field in Record 9A = 1, 2, …9, then this portion is in Payable format. 
• If Beneficiary/Successor Address [[Option]] Field = A, B, C or D, then record 9 is in Beneficiary/Successor Owner 
format. 
• If Payable 1 Address [[Option]] Field in Record 9 = E or F, then record 9 is in Payable of X-[[settlement]] format. 
The following are bytes 756 through 848 for Payable (Address [[Option]] = 1, 2, …9) 
Payable 1 Account 
Number 
756 775 20 A/N Required if Payable Information 
Indicator = 2 
OC 142 
Payable 1 Zip Code 776 786 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 
digits for future postal expansion. 
Required if Payable Information 
Indicator = 1 
OC 144 
Payable 1 Name End 
Line Indicator 
787 787 1 A/N Required if Payable Information 
Indicator = 1 or 2. 
1-6 = Line number where name ends 
OC 145 
Payable 1 Address 
[[Option]] 
788 788 1 A/N Required if Payable Information 
Indicator = 1 or 2. 
1 = Dividends 
2 = Systematic withdrawals 
3 = Automatic drafts 
4 = [[Dividend]] and automatic drafts 
and systematic withdrawals 
5 = [[Dividend]] and automatic drafts 
6 = [[Dividend]] and systematic 
withdrawals 
7 = Automatic drafts and systematic 
withdrawals 
8 = Cross fund reinvest 
9 = Alternate payable 
OC 146 
Payable 1 Account 
Number Indicator 
789 789 1 A/N Required if Payable 1 Account 
Number is provided.  
1 = Fund 
2 = Firm 
OC 143 
Payable 1 Security Issue 
Country Code 
790 791 2 A/N Space. For future use R  
Payable 1 Security Issue 
[[ID]] 
792 800 9 A/N 
Required if Payable 1 Address [[Option]] 
= 8 
OC 156 
Payable 1 Security Issue 
Check Digit 
801 801 1 A/N Space. For future use R  
Alternate Payable 1 
Indicator 
802 802 1 A/N Required if Payable 1 Address [[Option]] 
= 9. 
OC 166 

---

## Page 23

Variable Length Record Layouts (Part 2) 
Full Registration (401) 23 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
0 = Non-payable mailing address 
1 = Bank registration (for PAC) 
2 = Other 
Alternate Payable 1 
Reason 
803 822 20 A/N Required if Alternate Payable 1 
Indicator = 2. 
OC 167 
Filler 823 848 26 A/N Space R  
The following are bytes 756 through 848 of Beneficiary/Successor Owner. 
Required for Section 529 registration (Registration Type = 1) 
• For Section 529 Plan (Registration Type = 1) at least one 529 Beneficiary (Beneficiary/Successor 
Owner Address [[Option]] = ‘C’) is required.  
• A Successor Owner (Beneficiary/Successor Owner Address [[Option]] = ‘D’) is required if Successor 
Owner Indicator = 1 and Section 529 (Registration Type = 1) and not allowed otherwise.  
• Not more than one Successor Owner is allowed. 
• Beneficiary/Successor Owner Address [[Option]] = ‘C’ or ‘D’ are not allowed for Regular 
Registration (Registration Type = 0). 
Beneficiary/Successor 
Owner Date of Birth 
756 763 8 N mmddccyy R 203 
Shareholder Date of Birth 764 771 8 N mmddccyy R 204 
Filler 772 775 4 A/N Space R  
Beneficiary/Successor 
Owner Zip Code 
776 786 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 
digits for future postal expansion. 
O 144 
Beneficiary/Successor 
Owner Name End Line 
Indicator 
787 787 1 A/N Required if Beneficiary/Successor 
Owner Name/Address is provided. 
1-6 = Line number where name ends 
OC 145 
Beneficiary/Successor 
Owner Address [[Option]] 
788 788 1 A/N A = Primary IRA Beneficiary  
B = Secondary IRA Beneficiary 
C = 529 Beneficiary 
D = 529 Successor Owner 
R 146 
Beneficiary/Successor 
Owner Relationship 
Indicator 
789 789 1 A/N 1 = Spouse 
2 = Non-Relative 
3 = Grandchild 
4 = Relative 
5 = Child 
O 205 
Filler 790 791 2 A/N Space R  
Beneficiary/Successor 
Owner SSN/EIN Number 
792 800 9 A/N Required if Beneficiary/Successor 
Owner Address [[Option]] is “C” or “D”. 
OC 103 

---

## Page 24

Variable Length Record Layouts (Part 2) 
Full Registration (401) 24 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Beneficiary/Successor 
Owner SSN/EIN Indicator 
801 801 1 A/N Required if Beneficiary/Successor 
Owner SSN/EIN Number is provided.   
0 = Tax [[ID]] number 
1 = Social security number 
OC 102 
Filler 802 802 1 A/N Space R  
Beneficiary Percentage 
Rate 
803 808 6 N 999.999 R 184 
Date of Event 809 816 8 N mmddccyy O 217 
Beneficiary/Successor 
Owner U.S. Citizenship 
Indicator 
817 817 1 A/N Required if Beneficiary/Successor 
Owner Address [[Option]] is “C” or “D”.  
0 = U.S. citizen 
1 = Not U.S. citizen 
OC 240 
Beneficiary Gender 818 818 1 A/N F = Female 
M = Male 
O 241 
Filler 819 848 30 A/N Space R  
The following are bytes 756 through 848 for Payable of x-[[settlement]] 
(Payable 1 Address [[Option]] = E or F) 
Payable 1 Bank Account 
Number 
756 775 20 A/N  R 142 
Payable 1 Bank ABA 
Routing Number 
776 784 9 A/N  R 141 
Filler 785 787 3 A/N Space R  
Payable 1 Address 
[[Option]] 
788 788 1 A/N E = ACH on demand 
F = Bank wire 
R 146 
Payable 1 Bank Account 
Type 
789 789 1 A/N 1 = Checking 
2 = Saving 
3 = Other 
R 143 
Filler 790 848 59 A/N Space R  
End of the first portion of Payable/Beneficiary 1 section (bytes 756 through 848) which has three different 
formats. 
The following is the rest of Payable/Beneficiary 1 section. 
For Payable of x-[[settlement]], Name/Address Line 1 contains Shareholder Name 1 (optional), and Name/Address 
Line 2 contains Shareholder Name 2 

---

## Page 25

Variable Length Record Layouts (Part 2) 
Full Registration (401) 25 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Payable/Beneficiary/Succ
essor Owner 1 
Name/Address Line 1 
849 883 35 A/N Required for Payable if Payable 
Information Indicator = 1 or 2. 
 
Required for IRA Beneficiary, 529 
Beneficiary or 529 Successor Owner 
OC 147 
Payable/Beneficiary/Succ
essor Owner 1 
Name/Address Line 2 
884 918 35 A/N  O  
Filler 919 941 23 A/N Space R  
Payable/Beneficiary/Succ
essor Owner 1 
Name/Address Line 3 
942 976 35 A/N  O  
Payable/Beneficiary/Succ
essor Owner 1 
Name/Address Line 4 
977 1011 35 A/N  O  
Filler 1012 1034 23 A/N Space R  
Payable/Beneficiary/Succ
essor Owner 1 
Name/Address Line 5 
1035 1069 35 A/N  O  
Columns 1070-1104 for regular registration (Registration Type = 0) 
Payable/Beneficiary 1 
Name/Address Line 6 
1070 1104 35 A/N  O  
Columns 1070-1104 for Section 529 registration (Registration Type = 1) 
Beneficiary/Successor 
Owner 1 City 
1070 1102 33 A/N Optional if Successor Owner 
Indicator = 1 and 
Beneficiary/Successor Owner 
Address [[Option]] = “D”. 
Otherwise, this field is required. 
RC 242 
Beneficiary/Successor 
Owner 1 State 
1103 1104 2 A/N Optional if Successor Owner 
Indicator = 1 and 
Beneficiary/Successor Owner 
Address [[Option]] = “D”. 
Otherwise, this field is required. 
RC 243 
Filler 1105 1127 23 A/N Space R  
End of Payable/Beneficiary 1 section 

---

## Page 26

Variable Length Record Layouts (Part 2) 
Full Registration (401) 26 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Note: 
The last section of 372 bytes (or less if not all Name/Address lines are included) may repeat itself 5 more times for 
additional 5 payables/Beneficiaries (4 more times for additional 4 Payables / Beneficiaries for Money Market purchase 
involving interactive [[participant]]). 
Columns 2988 – 3044 for FATCA Attributes 
Chapter 4 Status Code 2988 2989 2 A/N See Chapter 4 Status Code List at: 
https://dtcclearning.com/documents/
mutual-fund-services-1/mfs-cross-
product/codes-8/2240-chapter-4-
status-codes/file.html under General 
Codes. 
O 278 
Global [[intermediary]] 
Identification Number  
2990 3014 25 A/N IRS issued number to identify and 
establish FATCA status of a Foreign 
Financial Institution (FFI) 
O  
Underlying Client’s 
Foreign Tax [[ID]]  
3015 3039 25 A/N Foreign Tax [[ID]] of Underlying Client O  
FATCA Override Special 
Rate  
3040 3044 5 N 99.999 O 279 
Filler 3045 3080 36 A/N Space R  
[[intermediary]] Program  
Indicator – 1 
 
 
 
 
3081 3084 4 A/N Indicates the program, platform, or 
channel applicable to an account.  
Examples may include: 
• Program indicator for advisory 
accounts 
• Distribution channel applicable to 
the   account (e.g., retail, RIA, 
etc.) 
• Retirement platform pertaining to 
the account 
Values are uniquely defined by each 
[[intermediary]]. 
O  
[[intermediary]] Program  
Indicator – 2 
 
 
3085 3088 4 A/N Further defines the program, 
platform, or channel applicable to an 
account.  
Values are uniquely defined by each 
[[intermediary]]. 
O  
Servicing Group [[ID]] 
 
 
3089 3097 9 A/N This field is used to communicate 
aggregated servicing relationships or 
define additional relationships on 
accounts. 
Examples may include: 
• Consolidating (Super) Branches 
• Third-party administrators (TPAs) 
• Investment Advisers 
O  

---

## Page 27

Variable Length Record Layouts (Part 2) 
Full Registration (401) 27 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
• Consultants 
This field does not replace the main 
branch field on the account. 
Values are uniquely defined by each 
[[intermediary]]. 
Additional Relationship [[ID]] 
– 1 
 
 
3098 3117 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts. 
Values are uniquely defined by each 
[[intermediary]].  
O  
Additional Relationship [[ID]] 
– 2 
 
 
3118 3137 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts. 
Values are uniquely defined by each 
[[intermediary]]. 
O  
Filler 3138 3173 36 A/N Space R  

---

## Page 28

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 28 
ACATS TRANSFER (018) 
02.11.01 ACATS Transfer (018) 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified 
Field Name  Start End Len Type Description  
Record Length 1 4 4 N 0755, 0848, 0941  
(With no payables) 
1034, 1127, 1220, 1313  
(With 1 payable) 
1406, 1499, 1592, 1685  
(With 2 payables) 
1778, 1871, 1964, 2057  
(With 3 payables) 
2150, 2243, 2336, 2429  
(With 4 payables) 
2522, 2615, 2708, 2801  
(With 5 payables) 
2894, 2987, 3080, 3173  
(With 6 payables) 
Physical Sequence Number 5 6 2 A/N 01 
Logical Sequence Number  7 8 2 A/N 01 
Originator Type 9 9 1 A/N B = Firm 
F = Fund 
Filler 10 11 2 A/N Space 
Firm Number 12 15 4 N  
Filler 16 18 3 A/N Space 
Record Type 19 21 3 A/N 018 = ACATS Transfer 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
Filler 23 23 1 A/N Space 
Fund Number 24 27 4 N  
Filler 28 30 3 A/N Space 
Security Issue Country Code 31 32 2 A/N Space. For future use 

---

## Page 29

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 29 
Field Name  Start End Len Type Description  
Security Issue [[ID]] 33 41 9 A/N  
Security Issue Check Digit 42 42 1 A/N Space. For future use 
Filler 43 44 2 A/N Space 
Fund/SERV Control Number 45 59 15 A/N  
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / 
cancellation  
Space = No correction 
Filler 61 63 3 A/N Space 
Processing Date 64 71 8 N mmddccyy 
Filler 72 79 8 A/N Space 
Book/Physical Share Indicator 80 80 1 A/N 1 = Transfer in & out: book [[shares]] 
2 = Transfer in : book [[shares]] 
Transfer out: physical [[shares]] 
PI Delivery Indicator 81 81 1 A/N 0 = Deliver to customer 
1 = Deliver to firm 
2 = Deliver to agent for firm 
Space = N/A 
Filler 82 88 7 A/N Space 
TPA/Investment Agent Number 89 92 4 A/N  
Filler 93 95 3 A/N Space 

---

## Page 30

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 30 
Field Name  Start End Len Type Description  
Secondary Social Security 
Number  
96 104 9 A/N Secondary Social Security Number 
associated to Account 
ACATS will populate this field with the 
value in the ‘Original Receiver Customer 
SS Number/Tax [[ID]] Secondary’ field from 
the Transfer Input (TI). This field is used for 
PTF’s when Fund is either the deliverer or 
receiver. 
If the Fund is a deliverer and the Firm is the 
receiver this field is the ‘Original Receiver 
Customer SS Number Secondary’ from the 
TI record. The value in the ‘Original 
Receiver Customer SS Number Secondary’ 
on the TI record may be different from the 
SSN/EIN on the FR record or the Receiving 
Customer’s Primary Social Security 
Number on the TI record. 
Best Practice: The secondary social 
security number should be applied to 
search criteria when identifying accounts 
that may have multiple account owners. 
Filler 105 118 14 A/N Space 
Customer Name 119 138 20 A/N  
Fund Account Indicator 139 139 1 A/N 0 = New account – domestic 
1 = New account – foreign 
2 = Existing account – domestic 
3 = Existing account – foreign 
4 = New account – US Tax Resident Living 
Abroad  
5 = Existing account – US Tax Resident 
Living Abroad  
Customer Account Number at 
Fund 
140 159 20 A/N  
Filler 160 160 1 A/N Space 
Agent for Firm Number 161 164 4 A/N  
Network Control Indicator 165 165 1 A/N 0 = Non-networked  
3 = Matrix level 3 
4 = Matrix level 4 
Filler 166 166 1 A/N Space 

---

## Page 31

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 31 
Field Name  Start End Len Type Description  
SSN/EIN Indicator 167 167 1 A/N ACATS populates this field with one of the 
following values from the Fund Registration 
(FR) record: 
 
0 = Tax [[ID]] Number 
1 = Social Security Number 
2=  [[investor]] EIN (Employee Identification 
Number) 
 
Exception: 
If ACATS does not receive an FR record, 
the [[default]] value for this field is ‘0’. 
SSN/EIN Number 168 176 9 A/N ACATS populates this field with the 
SSN/EIN submitted on the FR by the 
receiver. 
Exceptions: 
For a PTF where the Fund is a receiver, if 
ACATS does not receive an FR record from 
the Firm, ACATS populates this field with 
the value in the ‘Receiving Customer’s 
Primary Social Security Number’ from the 
Transfer Initiation (TI) record. 
For a PTF where the Fund is a deliverer, if 
ACATS does not get a FR from the Firm, 
ACATS populates this field with the 
Receiving [[participant]]’s Tax [[ID]] number from 
the ACATS [[participant]] master file. 
For all other transfer types, if ACATS does 
not receive an FR record, ACATS 
populates this field with the Receiving 
[[participant]]’s Tax [[ID]] number from the 
ACATS [[participant]] master file. 
Original Deliverer Customer 
Account Number 
177 196 20 A/N Underlying Customer Account Number at 
the Delivering Firm 
Filler 197 197 1 A/N Space 
[[Dividend]] Code 198 198 1 A/N  [[Dividend]] LTCG STCG 
0 = Cash Cash Cash 
1 = Reinvest Reinvest Reinvest 
2 = Cash Cash Reinvest 
3 = Cash Reinvest Reinvest 
4 = Cash Reinvest Cash 
5 = Reinvest Cash Cash 

---

## Page 32

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 32 
Field Name  Start End Len Type Description  
6 = Reinvest  Reinvest Cash  
7 = Reinvest  Cash Reinvest 
 
Withhold Indicator 199 199 1 A/N W9 indications 
0 = Certified (W-9 on file) 
1 = Failure to provide tin 
2 = Failure to certify tin 
3 = Notification of incorrect TIN from the 
Secretary of Treasury (Withhold due to B 
Notice) 
4 = Failure to certify backup withholding 
status 
5 = Voluntary disclosure from payee of 
affirmative backup withholding status 
6 = Notification to commence Backup 
Withholding from Secretary of Treasury for 
underreporting [[Dividend]] and/or interest 
payments (Withhold due to C Notice) 
7 = Applied for social security number 
8 = Exempt recipient 
9 = Account(s) subject to both B and C 
Notice Withholding 
W8 indications 
A = Uncertified foreign account (no W8 
form on file-backup withholding necessary) 
B = Certified foreign [[Beneficial Owner]] 
account (form W8-BEN on file) 
C = Certified foreign [[intermediary]] account 
(form W8-IMY on file) 
D = Certified valid foreign account (form 
W8-ECI on file with ITIN) 
E = Certified foreign exempt account (form 
W8-EXP on file) 
F = W8 on file - no treaty rate claimed 
G = W8 Beneficiary with TIN on file 
Payable Information Indicator 200 200 1 A/N 0 = Address of record 
1 = Payable address 

---

## Page 33

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 33 
Field Name  Start End Len Type Description  
2 = Automatic clearing house 
3 = Cash to firm 
4 = Cross fund reinvest 
Customer Name End Line 
Indicator 
201 201 1 A/N 1-6 = Line number where name ends 
Customer Zip Code 202 212 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 digits 
for future postal expansion 
Social Code 213 214 2 A/N See Social Code List at 
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html under General 
Codes. 
NAV Account Indicator 215 215 1 A/N 0 = No 
1 = Yes 
[[Margin]] Account Indicator 216 216 1 A/N 0 = No 
1 = Yes 
Check Writing Privileges 
Indicator 
217 217 1 A/N 0 = No 
1 = Yes 
State of Sale (State Code) 218 219 2 A/N See state code list in Fund/SERV manual 
Country of Origin (Country 
Code) 
220 221 2 A/N  
Account Representative Name 222 236 15 A/N  
Account Representative 
Number 
237 245 9 A/N  
Branch Identification Number 246 254 9 A/N  
Filler 255 258 4 A/N Space 
Number of Payables 259 260 2 N 00-06 
W8 Certification Date 261 268 8 N mmddccyy 
W8 Expiration Date 269 276 8 N mmddccyy 
W8 Override NRA Special 
Rate 
277 281 5 N 99.999 

---

## Page 34

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 34 
Field Name  Start End Len Type Description  
W8 Qualified [[intermediary]] 
Indicator 
282 282 1 A/N 1 = QI (qualified [[intermediary]] - primary 
withholding) 
2 = QI (Qualified [[intermediary]] - non-
withholding) 
3 = Non-QI (non-qualified [[intermediary]] - 
non-withholding, not the [[Beneficial Owner]]) 
4 = Partnership (withholding) 
5 = Partnership (non- withholding) 
6 = U. S. branch (non- withholding) 
7 = Trust (withholding) 
8 = Trust (non-withholding) 
W8 Override Country Code 283 284 2 A/N  
Filler 285 290 6 A/N Space 
Customer Name/Address Line 
1 
291 325 35 A/N  
Customer Name/Address Line 
2 
326 360 35 A/N  
Filler  361 383 23 A/N Space 
Customer Name/Address Line 
3 
384 418 35 A/N  
Customer Name/Address Line 
4 
419 453 35 A/N  
Filler 454 476 23 A/N Space 
Customer Name/Address Line 
5 
477 511 35 A/N  
Customer Name/Address Line 
6 
512 546 35 A/N  
Originating Receiver Customer 
Account Number at Firm  
547 566 20 A/N Underlying Customer Account Number at 
the Originating Firm 
Filler 567 569 3 A/N Space 
Start of additional ACATS Transfer information (bytes 570-755) 
Transaction Type 570 570 1 A/N 1 = Transfer to new account 
2 = Transfer to existing account 
3 = Firm of record change only 
Account Type Indicator 571 571 1 A/N 1 = Customer name 
2 = [[street name]] 

---

## Page 35

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 35 
Field Name  Start End Len Type Description  
Customer Account Number at 
Firm 
572 591 20 A/N  
Delivering Firm Number 592 595 4 A/N  
Customer Account Number at 
Fund (Delivering Firm) 
596 615 20 A/N  
Customer Account Number at 
Firm (Delivering Firm) 
616 635 20 A/N  
Network Control Indicator 
(Delivering Firm) 
 
636 636 1 A/N 0 = Non-networked  
3 = Matrix level 3 
4 = Matrix level 4 
Agent for Delivering Firm 
Number 
637 640 4 A/N  
Fraction Indicator 641 641 1 A/N 1 = Transfer fraction 
2 = [[liquidation]] fraction 
Full/Partial Indicator 642 642 1 A/N 0 = Full - move all [[shares]] in the account at 
the Fund 
1 = Partial - move the exact share quantity 
specified 
Transfer Share Quantity 643 656 14 N 9,999,999,999.9999 
CDSC Transfer Indicator 657 657 1 A/N Space 
Delivering Firm Share Aging 
Indicator 
658 658 1 A/N 1 = The delivering firm or fund company will 
provide the share aging information in an 
automated fashion through the Networking 
Share Aging file. 
2 = The delivering firm or fund company will 
provide the share aging information outside 
of the system. 
Membership Identifier 659 660 2 A/N 01 = Trust [[Member]] 
Membership Identifier 
(Delivering Firm) 
661 662 2 A/N 01 = Trust [[Member]] 
Transfer Money Amount 663 678 16 N 99,999,999,999,999.99 
Currency Indicator 679 681 3 A/N  
[[default]] Registration 682 682 1 A/N 0 = No [[default]] 
1 = [[default]] Registration 
ACATS Control Number 683 702 20 A/N  
Transfer Disbursement [[Option]] 
- Accruals 
703 703 1 A/N 2 = Cash to customer - Delivering firm 

---

## Page 36

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 36 
Field Name  Start End Len Type Description  
4 = Reinvest - Receiving firm (bucket to 
bucket) 
Transfer Disbursement [[Option]] 
- Fractional [[Cash-in-Lieu]] 
704 704 1 A/N 0 = Cash to [[Broker]] - Delivering firm 
1 = Reinvest - Delivering firm 
2 = Cash to customer - Delivering firm 
3 = Cash to [[Broker]] - Receiving firm 
4 = Reinvest - Receiving firm 
5 = Cash to customer - Receiving firm 
Transfer Disbursement [[Option]] 
– Residuals 
705 705 1 A/N 0 = Cash to [[Broker]] - Delivering firm 
1 = Reinvest - Delivering firm 
2 = Cash to customer - Delivering firm 
3 = Cash to [[Broker]] - Receiving firm 
4 = Reinvest - Receiving firm  
5 = Cash to customer - Receiving firm 
NRA Tax 706 707 2 N .99 
[[settlement]] Date 708 715 8 A/N mmddccyy 
Accrual Money Amount 716 731 16 N 99,999,999,999,999.99 
Accrual Money Amount 
Indicator 
732 732 1 A/N A = All  
B = None 
Customer SSN/EIN Number 733 741 9 A/N ACATS populates this field with the value in 
the ‘Receiving Customer’s Primary Social 
Security’ field from the TI record.  This field 
is used for PTFs only, when Fund is either 
the deliverer or the receiver.   
The rule above is true in all circumstances, 
both when the receiver submits the FR 
record and when ACATS uses a [[default]] 
registration. 
Note: 
The value in the ‘Receiving Customer’s 
Primary Social Security Number’ on the TI 
record may be different from the SSN/EIN 
on the FR record.  
ACATS Account Type  742 743 2 A/N See list in ACATS Manual 
Gift/Donation Indicator 744 744 1 A/N 0 or Space = No, not a gift or donation 
1 = Yes, it is a gift or donation 
Originating Receiver Firm 
Number 
745 748 4 A/N Originating receiving [[Broker]] firm number 

---

## Page 37

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 37 
Field Name  Start End Len Type Description  
Originating Delivering Firm 
Number 
749 752 4 A/N Originating delivering [[Broker]] firm number 
Filler 753 755 3 A/N Space 
End of additional ACATS Transfer information 
Memo Field 756 767 12 A/N  
ACH (Automatic Clearing 
House) Indicator 
768 768 1 A/N 0 = No 
1 = Yes 
PAC (Pre Authorized Checks) 
Indicator 
769 769 1 A/N 0 = No 
1 = Yes 
SWP (Systematic Withdrawal 
Plan) Indicator 
770 770 1 A/N 0 = No 
1 = Yes 
ROA/LOI Value 771 786 16 N 99,999,999,999,999.99 
LOI Number/Date 787 794 8 A/N  
Related Trade Indicator 795 795 1 A/N 0 = No 
1 = Yes 
Related Account Number 796 815 20 A/N  
Related Account Number 
Indicator 
816 816 1 A/N 1 = Fund 
2 = Firm 
SWP/PAC Effective Date 817 824 8 N mmddccyy 
IRS 529 Annual Strategy 
Change Counter 
 
Effective 05/15/2023 
825 825 1 A/N 0 thru 9  
 
Number of strategy changes that 
occurred during a calendar year. 
Earnings to Date Money 
Amount 
 
Effective 05/15/2023 
826 841 16 N 99,999,999,999,999.99 
 
Earnings of [[shares]] being transferred. 
Negative Earnings to Date 
Indicator 
 
Effective 05/15/2023 
842 842 1 A/N N  = Negative                  
Space = Positive 
 
Indicates if the earnings amount is 
negative. 
Filler 843 848 6 A/N Space 
CDSC Payment Code 849 849 1 A/N 0 = Gross 

---

## Page 38

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 38 
Field Name  Start End Len Type Description  
1 = Net 
2 = Not applicable 
Disbursement Options 850 850 1 A/N 0 = Fixed cash amount 
1 = Fixed percentage 
2 = Fixed [[shares]] 
3 = Declining balance 
Disbursement Amount 851 866 16 N Format according to Disbursement [[Option]]: 
0 = 99,999,999,999,999.99 
1 = 999,999.9999999999 
2 = 999,999,999,999.9999 
3 = 999,999,999,999.9999 
Monthly Payment Indicators 867 878 12 A/N These 12 bytes represent 12 months 
respectively:  
1st byte = January, 
2nd byte = February, etc.  
For each byte: 
0 = No payment this month  
1 = Yes payment this month 
Payment Date Indicator 879 880 2 A/N 01-31 = Day of month 
L = Last day of month 
N = Normal fund cycle 
Retirement Tax Indicator 881 882 2 A/N 01 = Premature withdrawal 
02 = Rollover 
03 = Disability 
04 = Death 
05 = Prohibited 
06 = Other 
07 = Normal 
08 = Refund by excess contributions 
09 = Divorce 
10 = Plan revoked 
11 = Fund transfer 
99 = Not applicable 
Shareholder Bank Account 
Number 
883 902 20 A/N  
Shareholder Bank Account 
Type 
903 903 1 A/N 0 = Checking 
1 = Savings 

---

## Page 39

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 39 
Field Name  Start End Len Type Description  
2 = Other 
First Check Date 904 911 8 N mmddccyy 
ABA Routing Number 912 920 9 A/N  
Cost Basis [[Option]] 921 921 1 A/N 0 = Unknown 
1 = FIFO (First In First Out) 
2 = LIFO (Last In First Out) 
3 = High Cost 
4 = Low Cost 
5 = Average Cost 
6 = Select Lot 
Cost Basis Money Amount 
 
Effective 05/15/2023 
922 937 16 N 99,999,999,999,999.99 
Original cost of the [[shares]] being 
transferred. 
Filler 938 941 4 A/N Space 
Start of Payable #1 section 
Payable 1 Account Number 942 961 20 A/N  
Payable 1 Zip Code 962 972 11 A/N 5-digit Zip Code + 4-digit Zip - Four + 2 
digits for future postal expansion. 
Payable 1 Name End Line 
Indicator 
973 973 1 A/N 1-6 = Line number where name ends 
Payable 1 Address [[Option]] 974 974 1 A/N 1 = Dividends 
2 = Systematic withdrawals  
3 = Automatic drafts 
4 = [[Dividend]] and automatic drafts and 
systematic withdrawals 
5 = [[Dividend]] and automatic drafts 
6 = [[Dividend]] and systematic withdrawals 
7 = Automatic drafts and systematic 
withdrawals 
8 = Cross fund reinvest 
9 = Alternate payable 
Payable 1 Account Number 
Indicator 
975 975 1 A/N 1 = Fund 
2 = Firm 
Payable 1 Security Issue 
Country Code 
976 977 2 A/N Space. For future use 
Payable 1 Security Issue [[ID]] 978 986 9 A/N  

---

## Page 40

Variable Length Record Layouts (Part 2) 
ACATS Transfer (018) 40 
Field Name  Start End Len Type Description  
Payable 1 Security Issue 
Check Digit 
987 987 1 A/N Space. For future use 
Alternate Payable 1 Indicator 988 988 1 A/N 0 = Non-payable mailing address 
1 = Bank registration (for PAC) 
2 = Other 
Alternate Payable 1 Reason 989 1008 20 A/N  
Filler 1009 1034 26 A/N Space 
Payable 1 Name/Address Line 
1 
1035 1069 35 A/N  
Payable 1 Name/Address Line 
2 
1070 1104 35 A/N  
Filler 1105 1127 23 A/N Space 
Payable 1 Name/Address Line 
3 
1128 1162 35 A/N  
Payable 1 Name/Address Line 
4 
1163 1197 35 A/N  
Filler 1198 1220 23 A/N Space 
Payable 1 Name/Address Line 
5 
1221 1255 35 A/N  
Payable 1 Name/Address Line 
6 
1256 1290 35 A/N  
Filler 1291 1313 23 A/N Space 
End of Payable #1 section 
Note: 
The last section of 372 bytes (or less if not all Name/Address lines are included) may repeat itself 5 more times for 
additional 5 payables. 

---

## Page 41

Variable Length Record Layouts (Part 2) 
ACATS Transfer Acknowledgment/Rejection (019) 41 
ACATS TRANSFER ACKNOWLEDGMENT/REJECTION 
(019) 
02.12.01 ACATS Transfer Acknowledgment/Rejection (019) 
Input from funds to [[NSCC]] 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0197, 0290 R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N F = Fund R 187 
Filler 10 11 2 A/N Space R  
Receiving Firm 
Number 
12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 019 = ACATS Transfer 
Acknowledgment/ 
Rejection 
R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test  
R 122 
Filler 23 23 1 A/N Space  R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  
Filler  43 44 2 A/N Space R  
Fund/SERV Control 
Number 
45 59 15 A/N  R 005 
Filler 60 63 4 A/N Space R  

---

## Page 42

Variable Length Record Layouts (Part 2) 
ACATS Transfer Acknowledgment/Rejection (019) 42 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Submission Date 64 71 8 N mmddccyy R 101 
Delivering Firm 
Number 
72 75 4 A/N  R 008 
Filler 76 76 1 A/N Space R  
Fund Reject Code 77 79 3 A/N Value other than space or zero 
indicates rejection 
R 022 
Filler 80 80 1 A/N Space R  
PI Delivery Indicator 81 81 1 A/N 0 = Deliver to customer  
1 = Deliver to firm 
2 = Deliver to agent for firm 
O 039 
Filler 82 84 3 A/N Space R  
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space  
Output: Reject code 
R  
Fund [[settlement]] Date  89 96 8 A/N Field Format: 
mmddccyy 
 
Must be valid calendar date and 
formatted correctly. 
 
Field Requirements: 
- Required for ACAT 
Acknowledgements  
- Optional for ACAT Rejects 
 
Best Practice for Acknowledgements: 
- Funds should populate this field 
with the trade date. This date 
represents the effective date the 
transfer moved on the books of the 
Fund. 
RC 280 

---

## Page 43

Variable Length Record Layouts (Part 2) 
ACATS Transfer Acknowledgment/Rejection (019) 43 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Note: 
For Funds that process “as-of” 
transfers, the “as of” date should be 
used. 
Best Practice for Rejects: 
- Funds should not populate this field 
if the ACAT is rejected. 
Filler 97 104 8 A/N Space R  
Actual Share Quantity 
Transferred 
105 118 14 N 9,999,999,999.9999 
Optional if transfer is rejected by fund 
RC 019 
Customer Account 
Number At Fund  
(Receiving Firm)  
119 138 20 A/N  R 011 
Customer Account 
Number At Fund 
Indicator (Receiving 
Firm) 
139 139 1 A/N 1 = Fund 
2 = Firm  
R 048 
Certificate Date 140 147 8 N mmddccyy O 037 
Certificate Number 148 157 10 A/N  O  
Filler 158 164 7 A/N Space R  
Network Control 
Indicator 
 
165 165 1 A/N 0 = Non-networked  
3 = Matrix level 3 
4 = Matrix level 4 
R 047 
ACATS Control 
Number 
166 185 20 A/N  R 005 
Transfer 
Disbursement [[Option]] - 
Accruals 
186 186 1 A/N 2 = Cash to customer - Delivering 
firm 
4 = Reinvest - Receiving firm (bucket 
to bucket) 
O 134 
Transfer 
Disbursement [[Option]] - 
Fractional [[Cash-in-Lieu]] 
187 187 1 A/N 0 = Cash to [[Broker]] – Delivering firm 
1 = Reinvest - Delivering firm  
2 = Cash to customer - Delivering 
firm 
3 = Cash to [[Broker]] - Receiving firm 
4 = Reinvest - Receiving firm 
5 = Cash to customer - Receiving 
firm  
O 134 

---

## Page 44

Variable Length Record Layouts (Part 2) 
ACATS Transfer Acknowledgment/Rejection (019) 44 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Transfer 
Disbursement [[Option]] - 
Residuals 
188 188 1 A/N 0 = Cash to [[Broker]] - Delivering firm 
1 = Reinvest - Delivering firm  
2 = Cash to customer - Delivering 
firm 
3 = Cash to [[Broker]] - Receiving firm 
4 = Reinvest - Receiving firm 
5 = Cash to customer - Receiving 
firm  
O 134 
Fund CDSC Transfer 
Indicator 
189 189 1 A/N Space O 209 
Filler 190 197 8 A/N Space R  
Accrual Money 
Amount 
198 213 16 N 99,999,999,999,999.99  O 111 
Accrual Money 
Amount Indicator 
214 214 1 A/N A = All 
B = None 
C = Not accepted 
O 112 
IRS 529 Annual 
Strategy Change 
Counter 
 
Effective 05/15/2023 
215 215 1 A/N 0 thru 9  
 
If populated, only 0 thru 9 are 
allowed. 
 
Number of strategy changes that 
occurred during a calendar year. 
O 287 
Earnings to Date 
Money Amount 
 
Effective 05/15/2023 
216 231 16 N 99,999,999,999,999.99 
 
Earnings of [[shares]] being 
transferred
. 
 
O 262 
Negative Earnings 
to Date Indicator 
 
Effective 05/15/2023 
232 232 1 A/N N  = Negative                      
Space = Positive 
 
If populated, only ‘N’ is allowed. 
Indicates if the earnings amount is 
negative. 
O 263 
Cost Basis Money 
Amount 
 
Effective 05/15/2023 
233 248 16 N 99,999,999,999,999.99 
Original cost of the [[shares]] being 
transferred. 
O 261 
Filler 249 290 42 A/N Space R  

---

## Page 45

Variable Length Record Layouts (Part 2) 
Transfer of Retirement [[Asset]] (ToRA) (210) 45 
TRANSFER OF RETIREMENT [[Asset]] (TORA) (210) 
02.13.01 Transfer of Retirement [[Asset]] (ToRA) (210) 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0290 R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N F = Fund R 187 
Filler 10 11 2 A/N Space R  
Receiving Fund 
Number 
12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 210 = Transfer of Retirement [[Asset]] 
(ToRA) 
R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Delivering Fund 
Number 
24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  
Security Issue Type 43 44 2 A/N  O 150 
Control Number 45 59 15 A/N  R 005 
Filler 60 60 1 A/N Space R  
Transaction Type 61 61 1 A/N 0 = Full transfer 
1 = Partial transfer 
2 = Full distribution to Alternate 
address 
R 017 

---

## Page 46

Variable Length Record Layouts (Part 2) 
Transfer of Retirement [[Asset]] (ToRA) (210) 46 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
3 = Partial distribution to Alternate 
address 
Must be 2 or 3 if Receiving Fund 
Plan Type = 9  
Transaction Code 62 63 2 A/N Required if transaction Type = 1.  
01 = Percentage transfer 
02 = Share quantity 
03 = Money amount 
OC 018 
Submission Date 64 71 8 N mmddccyy  R 101 
Filler 72 80 9 A/N Space R  
[[Broker]] of Record for 
Delivering Fund [[Asset]] 
81 84 4 A/N  O  
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors  
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code 
R  
Filler  89 104 16 A/N Space  R  
Share Quantity 105 118 14 N 9,999,999,999.9999 
Required if Transaction Code = 02 
OC 019 
Customer Account 
Number at Delivering 
Fund 
119 138 20 A/N  R 020 
Receiving Fund Plan 
Type 
139 139 1 A/N 0 = IRA 
1 = IRA rollover 
2 = SEP IRA 
3 = 403B 
4 = Roth IRA 
5 = Simple IRA 
6 = Education IRA 
7 = SARSEP 
8 = Roth conversion IRA 
9 = Traditional to Roth conversion 
IRA 
R 183 

---

## Page 47

Variable Length Record Layouts (Part 2) 
Transfer of Retirement [[Asset]] (ToRA) (210) 47 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
A = Inherited Traditional IRA 
B = Inherited Roth IRA 
C = Inherited Roth conversion IRA 
Must be 9 if Transaction Type = 2 or 
3 
Percentage Rate 140 144 5 N 99.999 
Required if Transaction Code = 01 
OC 184 
Original Roth IRA 
Date (As known by the 
receiving fund) 
145 152 8 N mmddccyy O 185 
Customer Zip Code 153 163 11 A/N 5-digit Zip Code  +  4-digit Zip-Four  
+  2 digits for future postal expansion  
R 127 
Filler 164 197 34 A/N Space R  
Money Amount 198 213 16 N 99,999,999,999,999.99  
Required if Transaction Code = 03  
OC 019 
Currency Indicator 214 216 3 A/N  O 110 
Filler 217 224 8 A/N Space R  
Customer Name at 
receiving Fund 
225 259 35 A/N  R 063 
SSN/EIN Number at 
Receiving Fund 
260 268 9 A/N  R 103 
IRA Withholding 
Percentage 
269 273 5 N 99.999 
Allowed only if Receiving Fund Plan 
Type = 9 
O 158 
SSN/EIN Indicator 
(Receiving Fund)  
274 274 1 A/N 0 = Tax [[ID]] number  
1 = Social security number  
2 = [[investor]] TIN/EIN  
O 102 
Filler 275 290 16 A/N Space R  

---

## Page 48

Variable Length Record Layouts (Part 2) 
ToRA Acknowledgment (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 48 
TORA ACKNOWLEDGMENT (211); TORA 
CONFIRMATION (212); TORA RECONFIRMATION (213)  
02.14.01 ToRA Acknowledgment (211) 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0383 R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type  9 9 1 A/N F = Fund R 187 
Filler 10 11 2 A/N Space R  
Receiving Fund 
Number 
12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 211 = ToRA Acknowledgment 
212 = ToRA Confirmation 
213 = ToRA Reconfirmation 
R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Delivering Fund 
Number 
24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  
Security Issue Type 43 44 2 A/N  O 150 
Control Number 45 59 15 A/N  R 005 
Filler 60 60 1 A/N Space  R  

---

## Page 49

Variable Length Record Layouts (Part 2) 
ToRA Acknowledgment (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 49 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Transaction Type 61 61 1 A/N 0 = Full transfer 
1 = Partial transfer 
2 = Full distribution to Alternate 
address 
3 = Partial distribution to Alternate 
address 
Must be 2 or 3 if Receiving Fund 
Plan Type = 9  
R 017 
Transaction Code 62 63 2 A/N Required if Transaction Type = 1. 
01 = Percentage transfer 
02 = Share quantity 
03 = Money amount 
OC 018 
Submission Date 64 71 8 N mmddccyy R 101 
Trade Date 72 79 8 N mmddccyy 
Required for record types 212 and 
213 
OC 016 
Filler 80 80 1 A/N Space R  
[[Broker]] of Record for 
Delivering Fund [[Asset]] 
81 84 4 A/N  O  
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code  
R  
Filler 89 104 16 A/N Space  R  
Share Quantity 105 118 14 N 9,999,999,999.9999 
Required for record type 212 and 
213.  
Required for record type 211 if 
Transaction Code = 02 
OC 019 
Customer Account 
Number at Delivering 
Fund 
119 138 20 A/N  R 020 
Delivering Fund Plan 
Type 
139 139 1 A/N 0 = IRA R 183 

---

## Page 50

Variable Length Record Layouts (Part 2) 
ToRA Acknowledgment (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 50 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
1 = IRA rollover 
2 = SEP IRA 
3 = 403B 
4 = Roth IRA 
5 = Simple IRA 
6 = Education IRA 
7 = SARSEP 
8 = Roth conversion IRA 
9 = Traditional to Roth conversion 
IRA 
A = Inherited Traditional IRA 
B = Inherited Roth IRA 
C = Inherited Roth conversion IRA 
Must be 9 if Transaction Type =  2 or 
3 
Percentage Rate 140 144 5 N 99.999 
Required if Transaction Code = 01  
OC 184 
Original Roth IRA 
Date (As known by the 
delivering fund) 
145 152 8 N mmddccyy 
Required if delivering Fund Plan 
Type = 4 or 8  
OC 185 
Customer Zip Code 153 163 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 
2 digits for future postal expansion  
R 127 
Uncollected [[shares]] 164 177 14 N Share Field,  Format: 
9,999,999,999.9999 
O 266 
Filler 178 197 20 A/N Space  R  
Money Amount 198 213 16 N 99,999,999,999,999.99  
Required if Transaction Code = 03  
OC 019 
Currency Indicator 214 216 3 A/N   O 110 
Anticipated [[settlement]] 
Date 
217 224 8 A/N mmddccyy 
For record types 212 and 213 only. 
Input: Space 
Output: Anticipated [[settlement]] date 
R  
Customer Name at 
Delivering Fund 
225 259 35 A/N  R 063 
SSN/EIN Number at 
Delivering Fund 
260 268 9 A/N  R 103 

---

## Page 51

Variable Length Record Layouts (Part 2) 
ToRA Acknowledgment (211); ToRA Confirmation (212); ToRA Reconfirmation (213) 51 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
IRA Withholding 
Percentage 
269 273 5 N 99.999 
Allowed only if Delivering Fund Plan 
Type = 9 
O 158 
SSN/EIN Indicator 
(Delivering Fund)  
274 274 1 A/N 0 = Tax [[ID]] number  
1 = Social security number  
2 = [[investor]] TIN/EIN 
O 102 
Filler 275 290 16 A/N Space R  
Fee Amount 291 298 8 N 999,999.99 O 115 
Fee Type 299 299 1 A/N Required if Fee Amount > 0. 
1 = [[liquidation]] fee 
2 = Redemption fee 
3 = Surrender fee 
OC 116 
Amount Due 300 315 16 N 99,999,999,999,999.99 
For record type 211, this amount 
shows [[Asset]] value at 
acknowledgment time.  
For record types 212 or 213, this 
amount will be settled by [[NSCC]] 
R 026 
Price Per Share 316 327 12 N 999,999.999999 
Optional for record type 211 
RC 027 
Accrual Amount 328 343 16 N 99,999,999,999,999.99  O 111 
Accrual Indicator 344 344 1 A/N Required if Accrual Amount is 
provided. 
0 = Included in Amount Due 
1 = Paid via Cash Adjustment 
2 = Paid outside system 
OC 112 
Withholding Amount 345 360 16 N 99,999,999,999,999.99  
Allowed only if Delivering Fund Plan 
Type = 9 
O 113 
Filler 361 383 23 A/N Space R  

---

## Page 52

Variable Length Record Layouts (Part 2) 
Defined Contribution Plan (DCP Information) (002) 52 
DEFINED CONTRIBUTION PLAN (DCP INFORMATION) 
(002) 
02.15.01 Defined Contribution Plan (DCP Information) (002) 
Field Name  Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Record Length 1 4 4 N 0197, 0290, 0383, …, 2987 R 152 
Physical Sequence 
Number 
5 6 2 A/N 01 R 004 
Logical Sequence 
Number 
7 8 2 A/N 01 R 004 
Originator Type 9 9 1 A/N A = Investment Agent 
B = Firm 
F = Fund 
T = TPA  
R 187 
Filler 10 11 2 A/N Space R  
Firm Number 12 15 4 N  R 008 
Filler 16 18 3 A/N Space R  
Record Type 19 21 3 A/N 002 = Defined Contribution Plan 
Information 
R 002 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
R 122 
Filler 23 23 1 A/N Space R  
Fund Number 24 27 4 N  O 100 
Filler 28 30 3 A/N Space R  
Security Issue Country 
Code 
31 32 2 A/N Space. For future use R  
Security Issue [[ID]] 33 41 9 A/N  R 007 
Security Issue Check 
Digit 
42 42 1 A/N Space. For future use R  
Security Issue Type 43 44 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
OC 150 

---

## Page 53

Variable Length Record Layouts (Part 2) 
Defined Contribution Plan (DCP Information) (002) 53 
Field Name  Start End Len Type Description Opt/ 
Req 
Reject 
Code 
the Fund/SERV Security master 
file.  [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
Control Number 45 59 15 A/N  R 005 
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / 
cancellation 
Space = No correction 
R 006 
Filler 61 63 3 A/N Space R  
Submission Date 64 71 8 N mmddccyy  R 101 
Filler 72 82 11 A/N Space  R  
Number of DC 
information sections 
83 84 2 N Maximum of 31  R 049 
[[NSCC]] Rejection 
Indicator 
85 85 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
2 = Rejected by [[NSCC]], multiple 
errors  
R  
[[NSCC]] Reject Code 86 88 3 A/N Input: Space 
Output: Reject code  
R  
TPA/Investment Agent 
Number         
89 92 4 A/N Required if Originator Type = T or A   OC 188 
Filler 93 104 12 A/N Space  R  
Start of DC information section #1 (required) 
DC Amount Code 1 105 107 3 A/N See DC Amount Code List. R 190 
DC Amount 1 108 123 16 N 99,999,999,999,999.99 R 191 
DC Debit/Credit 
Indicator 1 
124 124 1 A/N 1 = Debit 
2 = Credit 
R 192 
DC Amount Code 2 125 127 3 A/N See DC Amount Code List.  
Required if DC Amount 2 > 0 
OC 193 

---

## Page 54

Variable Length Record Layouts (Part 2) 
Defined Contribution Plan (DCP Information) (002) 54 
Field Name  Start End Len Type Description Opt/ 
Req 
Reject 
Code 
DC Amount 2 128 143 16 N 99,999,999,999,999.99  
Required if DC Amount Code 2 is 
provided 
OC 194 
DC Debit/Credit 
Indicator 2 
144 144 1 A/N Required if DC Amount Code 2 is 
provided. 
1 = Debit 
2 = Credit 
OC 195 
DC Amount Code 3 145 147 3 A/N See DC Amount Code List.  
Required if DC Amount 3 > 0 
OC 196 
DC Amount 3 148 163 16 N 99,999,999,999,999.99  
Required if DC Amount Code 3 is 
provided 
OC 197 
DC Debit/Credit 
Indicator 3 
164 164 1 A/N Required if DC Amount Code 3 is 
provided. 
1 = Debit 
2 = Credit 
OC 198 
DC Amount Code 4 165 167 3 A/N See DC Amount Code List.  
Required if DC Amount 4 > 0 
OC 199 
DC Amount 4 168 183 16 N 99,999,999,999,999.99  
Required if DC Amount Code 4 is 
provided 
OC 200 
DC Debit/Credit 
Indicator 4 
184 184 1 A/N Required if DC Amount Code 4 is 
provided. 
1 = Debit 
2 = Credit 
OC 201 
Filler 185 197 13 A/N Space R  
Notes: 
1. The last section of 93 bytes (positions 105 to 197) may repeat itself 30 more times to a total of 124 DC amounts. 
2. DC Amount Codes must be in ascending order and cannot repeat themselves, i.e. each DC Amount Code must be 
greater than the one preceded it in the same transaction. 

---

## Page 55

Variable Length Record Layouts (Part 2) 
Retiring [[participant]] (090) 55 
RETIRING [[participant]] (090) 
02.16.01 Retiring [[participant]] (090) 
Output from [[NSCC]] to firms and funds. When relating to ToRA (Transfer of Retirement [[Asset]]), Firm 
means Receiving Fund, and Fund means Delivering Fund  
Field Name  Start End Len Type Description  
Record Length 1 4 4 N 0290 
Physical Sequence Number 5 6 2 A/N 01 
Logical Sequence Number 7 8 2 A/N 01 
Originator Type 9 9 1 A/N N = [[NSCC]] 
Filler 10 11 2 A/N Space 
Original Firm Number 12 15 4 N  
Filler 16 18 3 A/N Space 
Record Type 19 21 3 A/N 090 = Retiring [[participant]] 
Test Indicator 22 22 1 A/N 0 = Production 
1 = Test 
Filler 23 23 1 A/N Space 
Original Fund Number 24 27 4 N  
Filler 28 30 3 A/N Space 
Security Issue Country 
Code 
31 32 2 A/N Space. For future use 
Security Issue [[ID]] 33 41 9 A/N  
Security Issue Check Digit 42 42 1 A/N Space. For future use 
Security Issue Type 43 44 2 A/N  
Control Number 45 59 15 A/N  
Correction Indicator 60 60 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] correction / cancellation 
Space = No correction 
Action Code 61 61 1 A/N P = Purge 
C = Convert 
Transaction Code 62 63 2 A/N 01 = Initial purchase 
02 = Subsequent purchase 

---

## Page 56

Variable Length Record Layouts (Part 2) 
Retiring [[participant]] (090) 56 
Field Name  Start End Len Type Description  
03 = Partial [[liquidation]] 
04 = Full [[liquidation]] 
05 = Full exchange 
06 = Partial exchange 
07 = Post settle correct/cancel purchase 
08 = Post settle correct/cancel [[liquidation]] 
Effective Date   64 71 8 N mmddccyy 
Trade Date (when available) 72 79 8 N mmddccyy 
Filler 80 80 1 A/N Space 
Processing Type 81 81 1 A/N 1 = Order, Cash Adjustment or ToRA 
2 = Exchange 
3 = Registration 
Debit/Credit Indicator 82 83 2  DB = Debit firm 
CR = Credit firm 
NS = No [[settlement]] 
Filler 84 85 2 A/N Space 
Status 86 88 3 A/N 0A1 = Due to Settle 
081 = Order Not Acted Upon 
083 = Registration Pending 
084 = Extended Correction Transfer Not 
Acted Upon 
085 = Pending Release to [[settlement]] 
086 = Pending Correction Confirmation 
087 = Pending Registration Acknowledgment 
088 = Pending Exchange Reconfirmation 
089 = Post [[settlement]] Correction / 
Cancellation Not Acted Upon 
091 = Pending ToRA Acknowledgment 
092 = Pending ToRA Confirmation 
TPA/Investment Agent/TPP 
Number 
89 92 4 A/N  
Service Provider Number 93 96 4 A/N  
Filler 97 104 8 A/N Space 
Original Record Type 105 107 3 A/N 001 = Firm Order 
003 = Post [[settlement]] Correction by Firm 
004 = As-Of Order 

---

## Page 57

Variable Length Record Layouts (Part 2) 
Retiring [[participant]] (090) 57 
Field Name  Start End Len Type Description  
007 = Fund Originated Order 
009 = Fund Originated As-Of Order 
011 = Cash Adjustment 
015 = Exchange 
021 = Post [[settlement]] Exchange Cancellation 
by Fund 
026 = Post [[settlement]] Correction by Fund 
139 = Post [[settlement]] Cancellation by Firm 
140 = Post [[settlement]] Cancellation by Fund  
200 = Extended Correction Transfer 
210 = Transfer of Retirement [[Asset]] (ToRA) 
Share Quantity 108 121 14 N 9,999,999,999.9999 
Filler 122 123 2 A/N Space 
Anticipated [[settlement]] Date 124 131 8 A/N mmddccyy 
(Zero if not established yet) 
Exchange To Security Issue 
Country Code (when 
Process Type = 2) 
132 133 2 A/N  
Exchange To Security Issue 
[[ID]] (when Process Type = 2) 
134 142 9 A/N  
Exchange To Security Issue 
Check Digit (when Process 
Type = 2) 
143 143 1 A/N  
Exchange To Security Issue 
Type (when Process Type = 
2) 
144 145 2 A/N  
Exchange To Money 
Amount (when Process 
Type = 2) 
146 161 16 N 99,999,999,999,999.99 
Exch To Currency Indicator 
(when Process Type = 2) 
162 164 3 A/N  
Exchange To Share 
Quantity (when Process 
Type = 2) 
165 178 14 N 9,999,999,999.9999 
Filler 179 197 19 A/N Space 
Money Amount 198 213 16 N 99,999,999,999,999.99 
Currency Indicator 214 216 3 A/N  
Retiring [[participant]] Number 217 220 4 N  

---

## Page 58

Variable Length Record Layouts (Part 2) 
Retiring [[participant]] (090) 58 
Field Name  Start End Len Type Description  
Surviving [[participant]] 
Number (when Action Code 
= C) 
221 224 4 A/N  
Filler 225 290 66 A/N Space 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 59

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 7, 2023 
Publication Code: MFS317 
Service: Fund/SERV® 
Title: Variable Length Record Layouts (Part 2) 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 