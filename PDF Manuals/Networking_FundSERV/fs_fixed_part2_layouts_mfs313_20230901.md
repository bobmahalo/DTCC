---
title: "Fund/SERV - Fixed Length Record Layouts (Part 2)"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_fixed_part2_layouts_mfs313_20230901.pdf"
pages: 86
size: "872.6 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Fund/SERV - Fixed Length Record Layouts (Part 2)

**Original File:** [fs_fixed_part2_layouts_mfs313_20230901.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_fixed_part2_layouts_mfs313_20230901.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 86  
**File Size:** 872.6 KB  

---

## Page 1

 
[[DTCC]] Internal (Green) 
 
 
 
Fund/SERV® 
FIXED LENGTH RECORD LAYOUTS (PART 2) 
SEPTEMBER 1, 2023  
 

---

## Page 2

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 2 
[[DTCC]] Internal (Green) 
TABLE OF CONTENTS 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation 
(021) ....................................................................................................................................................................... 6 
02.07.01 Exchange Confirmation (016) Record 1 of 12 ..................................................................................... 6 
02.07.02 Exchange Confirmation (016) Record 2 of 12 ..................................................................................... 9 
02.07.03 Exchange Confirmation (016) Record 3 of 12 ...................................................................................11 
02.07.04 Exchange Confirmation (016) Record 4 of 12 ...................................................................................14 
02.07.05 Exchange Confirmation (016) Record 5 of 12 ...................................................................................17 
02.07.06 Exchange Confirmation (016) Record 6 of 12 ...................................................................................19 
02.07.07 Exchange Confirmation (016) Record 7 of 12 ...................................................................................21 
02.07.08 Exchange Confirmation (016) Record 8 of 12 ...................................................................................22 
02.07.09 Exchange Confirmation (016) Record 9 of 12 ...................................................................................23 
02.07.10 Exchange Confirmation (016) Record 10 of 12 .................................................................................24 
02.07.11 Exchange Confirmation (016) Record 11 of 12 .................................................................................25 
02.07.12 Exchange Confirmation (016) Record 12 of 12 .................................................................................26 
Cash Adjustment (011) ...................................................................................................................................... 27 
02.08.01 Cash Adjustment (011) Record 1 of 2 ...............................................................................................27 
02.08.02 Cash Adjustment (011) Record 2 of 2 ...............................................................................................30 
Short Registration (400) .................................................................................................................................... 31 
02.09.01 Short Registration (400) Record 1 of 2 ..............................................................................................31 
02.09.02 Short Registration (400) Record 2 of 2 ..............................................................................................34 
Full Registration (401) ....................................................................................................................................... 35 
02.10.01 Full Registration (401) Record 1 of 34 ...............................................................................................35 
02.10.02 Full Registration (401) Record 2 of 34 ...............................................................................................38 
02.10.03 Full Registration (401) Record 3 of 34 ...............................................................................................40 
02.10.04 Full Registration (401) Record 4 of 34 ...............................................................................................44 
02.10.05 Full Registration (401) Record 5 of 34 ...............................................................................................45 
02.10.06 Full Registration (401) Record 6 of 34 ...............................................................................................46 
02.10.07 Full Registration (401) Record 7 of 34 ...............................................................................................47 
02.10.08 Full Registration (401) Record 8 of 34 ...............................................................................................48 

---

## Page 3

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 3 
[[DTCC]] Internal (Green) 
02.10.09a Full Registration (401) Record 9a of 34 (Payable) ..........................................................................50 
02.10.09b Full Registration (401) Record 9b of 34 (Beneficiary/Successor Owner)  ........................................52 
02.10.09c Full Registration (401) Record 9c of 34 (Payable Of X-[[settlement]]) ................................................54 
02.10.10 Full Registration (401) Record 10 of 34 .............................................................................................55 
02.10.11 Full Registration (401) Record 11 of 34 .............................................................................................56 
02.10.12 Full Registration (401) Record 12 of 34 .............................................................................................57 
Record 13 Through 32 ......................................................................................................................................58 
02.10.14 Full Registration (401) Record 33 of 34 .............................................................................................59 
02.10.15 Full Registration (401) Record 34 of 34 .............................................................................................60 
ACATS Transfer (018) ........................................................................................................................................ 62 
02.11.01 ACATS Transfer (018) Record 1 of 34 ..............................................................................................62 
02.11.02 ACATS Transfer (018) Record 2 of 34 ..............................................................................................64 
02.11.03 ACATS Transfer (018) Record 3 of 34 ..............................................................................................66 
02.11.04 ACATS Transfer (018) Record 4 of 34 ..............................................................................................70 
02.11.05 ACATS Transfer (018) Record 5 of 34 ..............................................................................................71 
02.11.06 ACATS Transfer (018) Record 6 of 34 ..............................................................................................72 
02.11.07 ACATS Transfer (018) Record 7 of 34 ..............................................................................................73 
02.11.08 ACATS Transfer (018) Record 8 of 34 ..............................................................................................75 
02.11.09 ACATS Transfer (018) Record 9 of 34 ..............................................................................................77 
02.11.10 ACATS Transfer (018) Record 10 of 34 ............................................................................................79 
02.11.11 ACATS Transfer (018) Record 11 of 34 ............................................................................................81 
02.11.12 ACATS Transfer (018) Record 12 of 34 ............................................................................................82 
02.11.13 ACATS Transfer (018) Record 13 of 34 ............................................................................................83 
02.11.14 ACATS Transfer (018) Record 14 of 34 ............................................................................................84 
Record 15 through 34 .......................................................................................................................................85 
 

---

## Page 4

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 4 
[[DTCC]] Internal (Green) 
HISTORY OF IMPORTANT NOTICES 
Dates Important Notices 
September 1, 2023 
Record has been rebranded and reviewed.  
March 10, 2023 
• 529 Account Plan fields added to 018 and 019 records (effective May 15, 
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
Effective Date: February 29, 2016 
Please see Important Notice: 
a8107 P&S 7682 Dated October 27, 2015 
Effective Date:  July 27, 2015 Please see Important Notice:  
a7997 P&S 7572 Dated March 12, 2015 
Effective Date:  April 27, 2015 Please see Important Notice:  
a7926 P&S 7501 Dated November 4, 2014 
Documentation Changes a7865  P&S 7435 Dated July 2, 2014 
Effective Date:  July 28, 2014 
Please see Important Notice:  
a7701 P&S 7371 Dated May 15, 2014 (REVISED) 
a7701 P&S 7371 Dated March 17, 2014 
Effective Date:  November 18, 2013 Please see Important Notice:  
a7665 P&S 7235 Dated July 3, 2013 
Effective Date:  March 18, 2013 
Please see Important Notice:  
a7472 P&S 7042 Dated August 16, 2012 (enhancement details) 
a7567 P&S 7137 Dated January 9, 2013 (revised dates) 
a7570 P&S 7140 Dated January 11, 2013 
Documentation Changes Please see Important Notice: 
a7592 P&S 7162 Dated March 1, 2013 

---

## Page 5

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 5 
[[DTCC]] Internal (Green) 
Dates Important Notices 
Effective Date:  April 23, 2012 
Please see Important Notice:  
a7355 P&S 6925 Dated January 12, 2012 
 
Note: On 2/27/2012 a correction was made to 401 Records to reflect the 
changes that were made in accordance with Important Notice a6272 P&S 
5842.   
The Fund Account Indicator 4 (New Account – U.S. Tax Resident Living 
Abroad) has been added to Account Representative Name, Account 
Representative Number and Branch Identification Number fields as part of 
conditional requirements. 
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
Effective Date: December 1, 2008 
Please see Important Notices:  
a6667 P&S 6237 Dated July 29, 2008 
a6653 P&S 6223 Dated July 7, 2008 
a6620 P&S 6190 Dated May 20, 2008 
Effective Date: October 18, 2008 
Please see Important Notices:  
a6658 P&S 6228 Dated July 11, 2008  
a6644 P&S 6214 Dated June 25, 2008 
a6643 P&S 6213 Dated June 25, 2008 
 
 

---

## Page 6

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 6 
[[DTCC]] Internal (Green) 
EXCHANGE CONFIRMATION (016); EXCHANGE 
RECONFIRMATION (017); POST [[settlement]] 
EXCHANGE CANCELLATION (021) 
02.07.01 Exchange Confirmation (016) Record 1 of 12 
Required 
Record 1 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N F = Fund R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 016 = Exchange Confirmation  
017 = Exchange Reconfirmation  
021 = Post [[settlement]] Exchange 
Cancellation 
Not permitted if the Security Issue 
Type field value is 63 and [[settlement]] 
Override Reason Code field value is 
space  
RC 002/275 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code (Exch From) 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 
(Exch From) 
29 37 9 A/N  R 007 
Security Issue Check 
Digit (Exch From) 
38 38 1 A/N Space. For future use R  

---

## Page 7

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 7 
[[DTCC]] Internal (Green) 
Record 1 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Type 
(Exch From) 
39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Correction Indicator 56 56 1 A/N Required for record type 021.  
Not allowed for record type 017.  
P = Post [[settlement]] cancellation 
OC 006 
Transaction Type  57 57 1 A/N 6 = Exchange to new account  
7 = Exchange to existing account 
C = Voluntary Cross Class Exchange 
to new account 
D = Voluntary Cross Class Exchange 
to existing account 
R 017 
Transaction Code 58 59 2 A/N 05 = Full exchange  
06 = Partial exchange 
R 018 
Submission Date 60 67 8 N mmddccyy R 101 
Trade Date 68 75 8 N mmddccyy R 016 
Book/Physical Share 
Indicator 
76 76 1 A/N 1 = Exchange from book [[shares]] to 
book [[shares]]  
2 = Exchange from book [[shares]] to 
physical [[shares]] 
R 015 
PI Delivery Indicator 77 77 1 A/N Required if Book/Physical Share 
Indicator = 2.  
0 = Deliver to customer  
1 = Deliver to firm  
2 = Deliver to agent for firm 
OC 039 Filler 78 78 1 A/N Space R  
[[settlement]] Override 
Reason Code 
79 80 2 A/N Not allowed if Correction Indicator = 
P.  
O 179 

---

## Page 8

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 8 
[[DTCC]] Internal (Green) 
Record 1 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
01 = Wrap fee account  
02 = 401K  
03 = Other  
04 = X-[[settlement]]  
05 = Section 529 Account - Qualified 
State Tuition Program  
06 = X-[[settlement]] offshore enhanced 
(allowed for Security Types 62 and 
63 only) 
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Required if Membership Identifier = 
02 or 03 
OC 188 
Service Provider 
Number 
89 92 4 A/N  OC 215 
Filler 93 100 8 A/N Space R  
 
 
  

---

## Page 9

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 9 
[[DTCC]] Internal (Green) 
02.07.02 Exchange Confirmation (016) Record 2 of 12 
Required 
Record 2 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number  
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Exch From Share 
Quantity 
8 21 14 N 9,999,999,999.9999  
Required if Transaction Code = 06  
and Exch From Money Amount 
(Gross) = 0 
OC 019 
Customer Account 
Number at Firm 
22 41 20 A/N Optional if [[settlement]] Override 
Reason Code = 04 or 06  
or if Membership Identifier is provided. 
RC 020 
New Registration 
Indicator 
42 42 1 A/N 0 = No registration required  
1 = Registration required for 
Exchange To 
R 040 
Exch From Account 
Number at Fund 
43 62 20 A/N Required if Network Control Ind (for 
From Account) = 0 
OC 011 
Filler 63 63 1 A/N Space R  
Agent for Firm Number 64 67 4 A/N  O  
Network Control 
Indicator (for the From 
Account)  
68 68 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Fraction Indicator 69 69 1 A/N 1 = Issue fraction  
2 = [[liquidation]] fraction 
R 014 
Filler 70 70 1 A/N Space R  
Transaction Received 
Time 
71 76 6 N hhmmss Eastern Time 
000000 (midnight) to 235959 
 
Required when “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = ‘F’ (Fund). 
 
For Record types 016 and 017 
OC 168 

---

## Page 10

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 10 
[[DTCC]] Internal (Green) 
Record 2 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Must contain the same value as 
provided on the Exchange transaction 
(record type 015).  
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
Membership Identifier 77 78 2 A/N 01 = Trust [[Member]]  
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 79 100 22 A/N Space R  
 
  

---

## Page 11

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 11 
[[DTCC]] Internal (Green) 
02.07.03 Exchange Confirmation (016) Record 3 of 12 
Required 
Record 3 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
Exch From Money 
Amount (Gross) 
8 23 16 N 99,999,999,999,999.99  
Required if Transaction Code = 06 
and Exch From Share Quantity = 0 
OC 019 
Exch From Currency 
Indicator (Gross) 
24 26 3 A/N  O 110 
Anticipated [[settlement]] 
Date 
27 34 8 A/N mmddccyy  
Required if [[settlement]] Override 
Reason Code is provided and is not = 
04 (x-[[settlement]] domestic).  
Not allowed if [[settlement]] Override 
Reason Code = 04. 
OC 180 
Branch Identification 
Number 
35 43 9 A/N Optional if Membership Identifier = 01 
or 02 and Agent for Firm Number is 
not provided. 
RC 035 
Related Trade 
Indicator 
44 44 1 A/N 0 = No  
1 = Yes 
R 065 
Related Trade 
Identifier 
45 46 2 A/N Required if Related Trade Indicator = 
1 
OC 105 
Customer Name 47 66 20 A/N  R 063 
Exch From Sales 
Charge Rate 
67 70 4 N 9.999 O 025 
As-Of Indicator 71 71 1 A/N 0 = Regular Exchange  
1 = As-Of Exchange 
O 021 
Discount Type 72 72 1 A/N 1 = Letter of intent  
2 = Rights of accumulation  
3 = Net [[Asset]] value 
O 208 
Filler 73 77 5 A/N Space R  

---

## Page 12

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 12 
[[DTCC]] Internal (Green) 
Record 3 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
NAV Reason Code  78 78 1 A/N Required if Discount Type = 3.  
0 = Other  
1 = Net [[Asset]] value transfer  
2 = Repurchase  
3 = Employee  
4 = Error correction  
5 = Wrap fee account  
6 = NAV commissionable  
7 = Commissionable defined 
contribution plan  
8 = Non-commissionable defined 
contribution plan  
9 = Section 529 Account - Qualified 
State Tuition Program  
A = [[Dividend]] reinvestment trade  
B = Trust Company NAV per 
Agreement 
D = Deminimis Amount Processed at 
NAV  
E = Self Directed Brokerage Account 
OC 104 
As-Of Reason Code 79 80 2 A/N Required if As-Of Indicator = 1 
01 = Incorrect Firm/Fund Account 
Number  
02 = Incorrect Share Quantity/Dollar 
Quantity  
03 = Incorrect security issue [[ID]] 
04 = Customer renege  
05 = Incorrect Sales Charge 
Breakpoint  
07 = Blue sky violation  
09 = Delay in Firm Trade 
Transmission 
10 = With Fund’s Permission 
11 = Resubmitted Fund/SERV Reject 
12 = DCC&S (see [[Asset]] Type 
Indicator) 
13 = Distribution Reversal 
14 = Prospectus Violation 
OC 109 

---

## Page 13

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 13 
[[DTCC]] Internal (Green) 
Record 3 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Redemption Fee 
Indicator  
81 81 1 A/N 0 = Short-Term Redemption (STR) 
1 = STR with CDSC 
2 = Money Market [[Liquidity]] Fee  
3 = Money Market [[Liquidity]] Fee with 
CDSC 
 
Values “0” and “1” are not allowed for 
record types 016 and 017 if this field 
was blank on the original Exchange 
transaction (record type 015). 
 
Values “2” and “3” are allowed for 
record types 016 and 017 if this field 
was blank on the original Exchange 
transaction (record type 015). 
O 248 
Short Term 
Redemption Fee 
Waiver Indicator 
82 82 1 A/N 1 = STR waiver due to correction  
2 = Death  
3 = Disability  
4 = Mandatory distribution  
5 = Systematic withdrawal  
6 = Defined contribution  
7 = Hardship  
8 = Auto Rebalance  
9 = DC–Termination Distribution  
A = DC–Involuntary Distribution  
B = DC–Forfeitures  
C = DC–Loans  
D = DC–Excess Contributions  
E = Wrap Program  
F = Fund of Funds 
G = Divorce/QDRO 
H = Plan QDRO 
O 249 
Filler 83 99 17 A/N Space R  
Trade Date Forward 
Indicator 
100 100 1 A/N 0 = Trade Date not forwarded  
1 = Trade Date forwarded.  
For record type 016 and 017:  
must be same as on original 
exchange 
OC 229  

---

## Page 14

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 14 
[[DTCC]] Internal (Green) 
02.07.04 Exchange Confirmation (016) Record 4 of 12 
Required 
Record 4 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 04 R 004 
Filler 5 7 3 A/N Space R  
Security Issue Country 
Code (Exch To) 
8 9 2 A/N Space. For future use. R  
Security Issue [[ID]] 
(Exch To) 
10 18 9 A/N  R 041 
Security Issue Check 
Digit (Exch To) 
19 19 1 A/N Space. For future use. R  
Security Issue Type 
(Exch To) 
20 21 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Exch To Account 
Number 
22 41 20 A/N Required if Book/Physical Share 
Indicator = 2 
OC 011 
Exch To Account 
Number Indicator 
42 42 1 A/N Required if Exch To Account Number 
is provided.  
1 = Fund  
2 = Firm 
OC 048 
Network Control 
Indicator (for the To 
Account)  
 
43 43 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Exch To Sales Charge 
Rate 
44 47 4 N 9.999  
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator = 
1 
OC 025 

---

## Page 15

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 15 
[[DTCC]] Internal (Green) 
Record 4 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
ROA/LOI Value 48 63 16 N 99,999,999,999,999.99 O 064 
LOI Number/Date 64 71 8 A/N  O  
State of Sale  
(State Code)  
72 73 2 A/N Required for all exchanges R 012 
Money Market [[Liquidity]] 
Fee/Redemption Gate 
Indicator  
74 74 1 A/N F = Fund.  
B = [[intermediary]] 
 
For Record Types 016 & 017 
Must contain the same value as 
provided on the Exchange transaction 
(record type 015).  
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
O 282 
Transaction Received 
Date  
75 82 8 A/N mmddccyy 
 
Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = F 
 
For Record Types 016 & 017 
Must contain the same value as 
provided on the Exchange transaction 
(record type 015).  
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
OC 283 Aggregated Order 
Indicator  
83 83 1 A/N Required if the “Money Market 
[[Liquidity]] Fee/Redemption Gate 
Indicator” = “F” or “B”. 
• 1 = Transactions are not 
aggregated  
• 2 = Transactions are aggregated 
by “like” orders (purchases 
separate from redemptions) 
• 3 = Transactions are net of 
purchases and redemptions 
• 4 = Unknown at time of placement 
 
For Record Types 016 & 017 
Must contain the same value as 
provided on the Exchange transaction 
(record type 015).  
[[NSCC]] will reject if a fund provided 
value is different from the value 
submitted by the firm. 
OC 284 

---

## Page 16

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 16 
[[DTCC]] Internal (Green) 
Record 4 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Filler 84 93 10 A/N Space R  
Standard [[ID]] 94 99 6 A/N  O  
Program Transaction 
Indicator 
100 100 1 A/N 1 = Systematic Exchange O 259 
 
 
  

---

## Page 17

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 17 
[[DTCC]] Internal (Green) 
02.07.05 Exchange Confirmation (016) Record 5 of 12 
Required when Redemption Fee Indicator is provided. 
Record 5 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 05 R 004 
Filler 5 7 3 A/N Space R  
Account 
Representative 
Number 
8 16 9 A/N  O  
Account 
Representative Name 
17 31 15 A/N  O  
Confirm Number 32 43 12 A/N  O  
Memo Field 44 63 20 A/N  O  
Redemption Fee Rate 64 70 7 N 99.99999 
 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required and “Redemption Fee 
Indicator” = 2 or 3. 
 
If “Redemption Fee Indicator” = 0 or 1, 
this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Rate. 
OC 250 
STR Fee Share 
Quantity  
71 84 14 N 9,999,999,999.9999 
 
For all record types 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record types 016 and 017: 
If zero or Space, will not override the 
“STR Fee Share Quantity” in the 
O 251 

---

## Page 18

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 18 
[[DTCC]] Internal (Green) 
Record 5 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
database. 
 
For all record types 
Not allowed when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Redemption Fee 
Money Amount  
85 100 16 N 99,999,999,999,999.99 
 
For all record types 
Not allowed if “Redemption Fee 
Indicator” is not provided. 
 
For record types 016 and 017: 
Required when “Redemption Fee 
Indicator” is provided. 
 
For all record types 
Required when “Redemption Fee 
Indicator” is populated with either ‘2’ 
(Money Market [[Liquidity]] Fee) or ‘3’ 
(Money Market [[Liquidity]] Fee with 
CDSC). 
Zero value is not allowed when this 
field is required. 
 
If “Redemption Fee Indicator” = 0 or 1, 
this field will be utilized to 
communicate a Short-Term 
Redemption (STR) Fee Money 
Amount. 
OC 252 
 
  

---

## Page 19

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 19 
[[DTCC]] Internal (Green) 
02.07.06 Exchange Confirmation (016) Record 6 of 12 
Required. 
Record 6 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 06 R 004 
Filler 5 7 3 A/N Space R  
Exch From Money 
Amount Due 
8 23 16 N 99,999,999,999,999.99  
This amount will be settled by [[NSCC]] 
as follows:  
If Correction Ind = space:  
Credit firm, debit fund.  
If Correction Ind = P:  
Debit firm, credit fund. 
R 026 
Exch From Currency 
Indicator Due 
24 26 3 A/N  O 110 
Invoke Indicator 27 27 1 A/N 1 = Yes (postpone [[settlement]] until 
reconfirmed)  
2 = No (settle Exchange).  
Must be 2 for record type 017 or if 
Correction Indicator = P 
R 043 Tefra Withholding 28 28 1 A/N 0 = No withholding  
1 = 20% withholding 
R 050 
Exch From Price Per 
Share 
29 40 12 N 999,999.999999 R 027 
Filler 41 44 4 A/N Space R  
Exch From Sales 
Charge Amount 
45 53 9 N 9,999,999.99 O 088 
Number of Records 
Beyond Record #7 
54 55 2 N Maximum of 05 R 049 
Exch To Account 
Number #2 
56 75 20 A/N  O  
Exch To Account 
Number #2 Indicator 
76 76 1 A/N Required if Exch To Account Number 
#2 is provided.  
1 = Fund  
2 = Firm 
OC 048 

---

## Page 20

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 20 
[[DTCC]] Internal (Green) 
Record 6 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Exchange Fee 77 84 8 N 999,999.99 O 042 
Filler 85 98 14 A/N Space R  
Breakpoint Change 
Reason Code 
99 99 1 A/N 1 = ROA value at fund  
2 = LOI at fund  
3 = The higher of cost or market value 
at fund  
4 = Jumbo Pricing  
5 = Wrap Account  
6 = NAV Account 
7 = Amount Processed at NAV 
O 246 
Filler 100 100 1 A/N Space R  
 
  

---

## Page 21

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 21 
[[DTCC]] Internal (Green) 
02.07.07 Exchange Confirmation (016) Record 7 of 12 
Optional 
Record 7 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 07 R 004 
Filler 5 7 3 A/N Space R  
Original Control 
Number 
8 22 15 A/N  O  
Original Correction 
Indicator 
23 23 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]]  
correction/cancellation  
Space = No correction 
O 164 
Filler 24 100 77 A/N Space R  
 
  

---

## Page 22

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 22 
[[DTCC]] Internal (Green) 
02.07.08 Exchange Confirmation (016) Record 8 of 12 
Required if Invoke Indicator = 2 
Record 8 of 12 
Field Name  
Start End Len Type Description Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 08 R 004 
Filler 5 7 3 A/N Space R  
Exch To Gross Money 
Amount 
8 23 16 N 99,999,999,999,999.99 R 019 
Exch To Money 
Amount Due 
24 39 16 N 99,999,999,999,999.99 R 026 
Exch To Total Share 
Quantity 
40 53 14 N 9,999,999,999.9999  
Represents the total for the entire 
Exchange transaction.  
This is the settled quantity. 
R 019 
Exch To Price Per 
Share 
54 65 12 N 999,999.999999 R 027 
Exch To Firm 
Concession 
66 74 9 N 9,999,999.99 O 044 
Exch To Total Money 
Amount Due 
75 90 16 N 99,999,999,999,999.99  
Represents the total for the entire 
Exchange transaction.  
This amount will be settled by [[NSCC]] 
as follows:  
If Correction Ind = space:  
 Debit firm, credit fund.  
If Correction Ind = P:  
 Credit firm, debit fund. 
R 026 
Exch To Currency 
Indicator 
91 93 3 A/N  O 110 
Exch To Load Type 
Indicator 
94 94 1 A/N 0 = Other  
1 = Front-End Load 
R 247 
Filler 95 100 6 A/N Space R  
 
 

---

## Page 23

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 23 
[[DTCC]] Internal (Green) 
02.07.09 Exchange Confirmation (016) Record 9 of 12 
Optional. Used to report additional sales charge rate 
Record 9 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 09 R 004 
Filler 5 7 3 A/N Space R  
Exch To Gross Money 
Amount 
8 23 16 N 99,999,999,999,999.99 R 019 
Exch To Money 
Amount Due 
24 39 16 N 99,999,999,999,999.99 R 026 
Exch To Total Share 
Quantity 
40 53 14 N 9,999,999,999.9999 R 019 
Exch To Price Per 
Share 
54 65 12 N 999,999.999999 R 027 
Exch To Firm 
Concession 
66 74 9 N 9,999,999.99 O 044 
Exch To Sales Charge 
Rate 
75 78 4 N 9.999  
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator = 
1 
OC 027 
Filler 79 100 22 A/N Space R  
 
  

---

## Page 24

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 24 
[[DTCC]] Internal (Green) 
02.07.10 Exchange Confirmation (016) Record 10 of 12 
Optional. Used to report additional sales charge rate 
Record 10 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 10 R 004 
Filler 5 7 3 A/N Space R  
Exch To Gross Money 
Amount 
8 23 16 N 99,999,999,999,999.99 R 019 
Exch To Money 
Amount Due 
24 39 16 N 99,999,999,999,999.99 R 026 
Exch To Total Share 
Quantity 
40 53 14 N 9,999,999,999.9999 R 019 
Exch To Price Per 
Share 
54 65 12 N 999,999.999999 R 027 
Exch To Firm 
Concession 
66 74 9 N 9,999,999.99 O 044 
Exch To Sales Charge 
Rate 
75 78 4 N 9.999  
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator = 
1 
OC 025 
Filler 79 100 22 A/N Space R  
 
  

---

## Page 25

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 25 
[[DTCC]] Internal (Green) 
02.07.11 Exchange Confirmation (016) Record 11 of 12 
Optional. Used to report additional sales charge rate 
Record 11 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 11 R 004 
Filler 5 7 3 A/N Space R  
Exch To Gross Money 
Amount 
8 23 16 N 99,999,999,999,999.99 R 019 
Exch To Money 
Amount Due 
24 39 16 N 99,999,999,999,999.99 R 026 
Exch To Total Share 
Quantity 
40 53 14 N 9,999,999,999.9999 R 019 
Exch To Price Per 
Share 
54 65 12 N 999,999.999999 R 027 
Exch To Firm 
Concession 
66 74 9 N 9,999,999.99 O 044 
Exch To Sales Charge 
Rate 
75 78 4 N 9.999  
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator = 
1 
OC 025 
Filler 79 100 22 A/N Space R  
 
  

---

## Page 26

Fixed Length Record Layouts (Part 2) 
Exchange Confirmation (016); Exchange Reconfirmation (017); Post [[settlement]] Exchange Cancellation (021) 26 
[[DTCC]] Internal (Green) 
02.07.12 Exchange Confirmation (016) Record 12 of 12 
Optional. Used to report additional sales charge rate 
Record 12 of 12 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 12 R 004 
Filler 5 7 3 A/N Space R  
Exch To Gross Money 
Amount 
8 23 16 N 99,999,999,999,999.99 R 019 
Exch To Money 
Amount Due 
24 39 16 N 99,999,999,999,999.99 R 026 
Exch To Total Share 
Quantity 
40 53 14 N 9,999,999,999.9999 R 019 
Exch To Price Per 
Share 
54 65 12 N 999,999.999999 R 027 
Exch To Firm 
Concession 
66 74 9 N 9,999,999.99 O 044 
Exch To Sales Charge 
Rate 
75 78 4 N 9.999  
Must be provided (but allowed to be 
zero) if Exch To Load Type Indicator = 
1 
OC 025 
Filler 79 100 22 A/N Space R  

---

## Page 27

Fixed Length Record Layouts (Part 2) 
Cash Adjustment (011) 27 
[[DTCC]] Internal (Green) 
CASH ADJUSTMENT (011) 
02.08.01 Cash Adjustment (011) Record 1 of 2 
Required 
When ToRA related (ToRA Indicator = ‘1’ or ‘2’), Firm means Receiving Fund, and Fund means 
Delivering Fund. 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N A = Investment Agent 
B = Firm  
F = Fund  
T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 011 = Cash Adjustment 
 
R 002 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code 
27 28 2 A/N Space. For future use. R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use R  

---

## Page 28

Fixed Length Record Layouts (Part 2) 
Cash Adjustment (011) 28 
[[DTCC]] Internal (Green) 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Type 39 40 2 A/N Required if 24 (Money Market) and 
ToRA Indicator = space 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Filler 56 57 2 A/N Space R  
Reason Code 58 59 2 A/N 01 = [[Dividend]] deduct  
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
Submission Date 60 67 8 N mmddccyy R 101 
ToRA (Transfer of 
Retirement [[Asset]]) 
Indicator 
68 68 1 A/N 1 = ToRA related (submitted by the 
receiving fund)  
2 = ToRA related (submitted by the 
delivering fund)  
Space = Not ToRA related 
R 186 
Filler 69 78 10 A/N Space R  

---

## Page 29

Fixed Length Record Layouts (Part 2) 
Cash Adjustment (011) 29 
[[DTCC]] Internal (Green) 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[settlement]] Override 
Reason Code 
79 80 2 A/N Required if Anticipated [[settlement]] 
Date is provided.  
01 = Wrap fee account  
02 = 401K  
03 = Other 
OC 179 [[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple 
errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Required if: 
Originator Type = (T or A or V) 
OR  
Membership Identifier = 02 or 03 
OC 188 
Filler 89 100 12 A/N Space R  
 
 
  

---

## Page 30

Fixed Length Record Layouts (Part 2) 
Cash Adjustment (011) 30 
[[DTCC]] Internal (Green) 
02.08.02 Cash Adjustment (011) Record 2 of 2 
Required 
Record 2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Adjustment Amount 8 23 16 N 99,999,999,999,999.99 R 033 
Currency Indicator 24 26 3 A/N  O 110 
Debit/Credit Code 27 28 2 A/N DB = Debit firm  
CR = Credit firm 
R 034 
Original Control 
Number 
29 43 15 A/N Required if ToRA Indicator 1or 2 OC 163 
Original Correction 
Indicator 
44 44 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation  
Space = No correction 
O 164 
Memo Field 45 53 9 A/N  O  
Anticipated [[settlement]] 
Date 
54 61 8 A/N mmddccyy  
Required if [[settlement]] Override 
Reason Code is provided 
O 180 
Filler 62 76 15 A/N Space R  
Membership Identifier 77 78 2 A/N 01 = Trust [[Member]]  
02 = Networking info required for 
TPA/Investment Agent 
03 = TPP (Third Party Provider) 
O 181 
Filler 79 100 22 A/N Space R  

---

## Page 31

Fixed Length Record Layouts (Part 2) 
Short Registration (400) 31 
[[DTCC]] Internal (Green) 
SHORT REGISTRATION (400) 
02.09.01 Short Registration (400) Record 1 of 2 
Required. For subsequent purchases only 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N B = Firm  
S = Service Provider for B = Firm 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 400 = Short Registration R 002 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code 
27 28 2 A/N Space. For future use. R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use. R  

---

## Page 32

Fixed Length Record Layouts (Part 2) 
Short Registration (400) 32 
[[DTCC]] Internal (Green) 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Type 39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
 correction/cancellation  
Space = No correction 
R 006 
Filler 57 59 3 A/N Space R  
Submission Date 60 67 8 N mmddccyy R 101 
Filler 68 75 8 A/N Space  R  
Book/Physical Share 
Indicator  
76 76 1 A/N 0 = Book [[shares]] - firm name  
1 = Book [[shares]] - customer name  
2 = Physical [[shares]]  
Must be 0 or 1 for Money Market 
trades 
R 015 
PI Delivery Indicator  77 77 1 A/N Required if Book/Physical Share 
Indicator = 2.  
0 = Deliver to customer  
1 = Deliver to firm  
2 = Deliver to agent for firm 
OC 039 Filler  78 80 3 A/N Space R  
[[NSCC]] Rejection 
Indicator  
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple errors  
R  

---

## Page 33

Fixed Length Record Layouts (Part 2) 
Short Registration (400) 33 
[[DTCC]] Internal (Green) 
Record 1 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[NSCC]] Reject Code  82 84 3 A/N Input: Space  
Output: Reject code 
R  
Filler 85 88 4 A/N Space R  
Service Provider 
Number 
89 92 4 A/N Required if Originator Type = S OC 215 
Filler 93 100 8 A/N Space R  
 
  

---

## Page 34

Fixed Length Record Layouts (Part 2) 
Short Registration (400) 34 
[[DTCC]] Internal (Green) 
02.09.02 Short Registration (400) Record 2 of 2 
Required 
Record 2 of 2 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Filler 8 21 14 A/N Space R  
Customer Name 22 41 20 A/N  R 063 
Filler 42 42 1 A/N Space R  
Customer Account 
Number 
43 62 20 A/N  R 011 
Customer Account 
Number Indicator 
63 63 1 A/N 1 = Fund  
2 = Firm 
R 048 
Agent for Firm Number 64 67 4 A/N  O  
Filler 68 69 2 A/N Space R  
SSN/EIN Indicator 70 70 1 A/N 0 = Tax [[ID]] number  
1 = Social security number  
2 = [[investor]] TIN/EIN 
R 102 
SSN/EIN Number 71 79 9 A/N  R 103 
Filler 80 100 21 A/N Space R  

---

## Page 35

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 35 
[[DTCC]] Internal (Green) 
FULL REGISTRATION (401) 
02.10.01 Full Registration (401) Record 1 of 34 
Required. For either new or subsequent purchases 
Record 1 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 01 R 004 
Originator Type 5 5 1 A/N A = Investment Agent 
B = Firm  
T = TPA 
S = Service Provider for B = Firm 
P = Service Provider for T = TPA 
V = TPP (Third Party Provider) 
R 187 
Filler 6 7 2 A/N Space R  
Firm Number 8 11 4 N  R 008 
Filler 12 14 3 A/N Space R  
Record Type 15 17 3 A/N 401 = Full Registration R 002 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
R 122 
Filler 19 19 1 A/N Space R  
Fund Number 20 23 4 N  O 100 
Filler 24 26 3 A/N Space R  
Security Issue Country 
Code 
27 28 2 A/N Space. For future use R  
Security Issue [[ID]] 29 37 9 A/N  R 007 
Security Issue Check 
Digit 
38 38 1 A/N Space. For future use R  

---

## Page 36

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 36 
[[DTCC]] Internal (Green) 
Record 1 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Security Issue Type 39 40 2 A/N Required if 24 (Money Market) 
Notes: 
Input: With the exception of 
Security Issue Type = 24, [[NSCC]] 
does not validate the value against 
the Fund/SERV Security master 
file. [[NSCC]] leverages the 
Fund/SERV Security master file to 
determine value and associated 
processing rules. 
Output: [[NSCC]] populates with the 
value in the Fund/SERV Security 
master file. 
OC 150 
Control Number 41 55 15 A/N  R 005 
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction 
P = Post [[settlement]] 
correction/cancellation  
Space = No correction 
R 006 
Filler 57 59 3 A/N Space R  
Submission Date 60 67 8 N mmddccyy R 101 
Filler 68 75 8 A/N Space R  
Book/Physical Share 
Indicator 
76 76 1 A/N 0 = Book [[shares]] - firm name  
1 = Book [[shares]] - customer name  
2 = Physical [[shares]]  
Must be 0 or 1 for Money Market 
trades 
R 015 
PI Delivery Indicator 77 77 1 A/N Required if Book/Physical Share 
Indicator = 2.  
0 = Deliver to customer  
1 = Deliver to firm  
2 = Deliver to agent for firm 
OC 039 Filler 78 80 3 A/N Space R  

---

## Page 37

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 37 
[[DTCC]] Internal (Green) 
Record 1 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
[[NSCC]] Rejection 
Indicator 
81 81 1 A/N Input: Space  
Output:  
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]]  
2 = Rejected by [[NSCC]], multiple errors 
R  
[[NSCC]] Reject Code 82 84 3 A/N Input: Space  
Output: Reject code 
R  
TPA/Investment 
Agent/TPP Number 
85 88 4 A/N Required if Originator Type = T or P 
or A or V 
OC 188 
Service Provider 
Number 
89 92 4 A/N Required if Originator Type = S or P OC 215 
Filler 93 100 8 A/N Space R  
 
  

---

## Page 38

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 38 
[[DTCC]] Internal (Green) 
02.10.02 Full Registration (401) Record 2 of 34 
Required 
Record 2 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 02 R 004 
Filler 5 7 3 A/N Space R  
Filler 8 21 14 A/N Space R  
Customer Name 22 41 20 A/N  R 063 
Fund Account Indicator 42 42 1 A/N 0 = New account–U.S.  
1 = New account–non-U.S.  
2 = Existing account–U.S.  
3 = Existing account–non-U.S. 
4 = New account–U.S. Tax Resident 
Living Abroad  
5 = Existing account–U.S. Tax 
Resident Living Abroad 
R 010 
Customer Account 
Number 
43 62 20 A/N Required for existing account (Fund 
Account Ind = 2 or 3) 
OC 011 
Customer Account 
Number Indicator 
63 63 1 A/N Required if Customer Account 
Number is provided.  
1 = Fund  
2 = Firm 
OC 048 
Agent for Firm Number 64 67 4 A/N Required if Originator Type = V (TPP)  OC 271 
Network Control 
Indicator 
 
68 68 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
R 047 
Registration Type 69 69 1 A/N 0 = Regular registration  
1 = Section 529 registration 
O 235 
SSN/EIN Indicator 70 70 1 A/N 0 = Tax [[ID]] number  
1 = Social security number  
2 = [[investor]] TIN/EIN 
R 102 
SSN/EIN Number 71 79 9 A/N  R 103 

---

## Page 39

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 39 
[[DTCC]] Internal (Green) 
Record 2 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Customer/Owner U.S. 
Citizenship Indicator 
80 80 1 A/N Required for Section 529 registration  
(Registration Type = 1).  
0 = U.S. citizen  
1 = Not U.S. citizen 
OC 236 
Target Date Fund 
Indicator 
81 81 1 A/N 0 = No 
1 = Yes 
O 260 
Age Based Indicator 82 82 1 A/N 1 = Aggressive 
2 = Moderate 
3 = Conservative 
O 267 
Age Based Roll 
Exempt Indicator 
83 83 1 A/N 0 = No, account is not exempt and will 
be included within Automatic Age Roll 
Events 
1 = Yes, account is exempt from 
Automatic Age Roll Events 
O 268 
Customer/Owner U.S. 
Resident Alien 
Indicator 
84 84 1 A/N 0 = No  
1 = Yes 
O 269 
Successor Owner 
Indicator 
85 85 1 A/N Required if Section 529 (Registration 
Type = 1).Not allowed otherwise. 
0 = No 
1 = Yes 
OC 270 
Underlying Firm 
Symbol (UFS) 
86 89 4 A/N  Number that identifies the Underlying 
Firm (Banks/Trusts/Record 
Keepers/TPA’s) that clear through 
another entity 
O  
Filler 90 100 11 A/N Space R  
 
 
  

---

## Page 40

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 40 
[[DTCC]] Internal (Green) 
02.10.03 Full Registration (401) Record 3 of 34 
Required 
Record 3 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 03 R 004 
Filler 5 7 3 A/N Space R  
[[Dividend]] Code 8 8 1 A/N  [[Dividend]]   LTCG  STCG  
0 =  Cash  Cash  Cash  
1 =  Reinvest   Reinvest  Reinvest 
2 =  Cash  Cash  Reinvest 
3 =  Cash  Reinvest  Reinvest 
4 =  Cash  Reinvest  Cash  
5 =  Reinvest   Cash  Cash  
6 =  Reinvest   Reinvest  Cash  
7 =  Reinvest   Cash  Reinvest 
 
R 123 

---

## Page 41

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 41 
[[DTCC]] Internal (Green) 
Record 3 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Withhold Indicator  9 9 1 A/N W9 indications  
0 = Certified (W-9 on file)  
1 = Failure to provide tin  
2 = Failure to certify tin  
3 = Notification of incorrect TIN from 
the Secretary of Treasury (Withhold 
due to B Notice) 
4 = Failure to certify backup 
withholding status  
5 = Voluntary disclosure from payee of 
affirmative backup withholding status  
6 = Notification to commence Backup 
Withholding from Secretary of 
Treasury for underreporting [[Dividend]] 
and/or interest payments (Withhold 
due to C Notice) 
[[Dividend]] and/or interest payments  
7 = Applied for social security number  
8 = Exempt recipient  
9 = Account(s) subject to both B and C 
Notice Withholding 
W8 indications  
A = Uncertified foreign account (no W8 
form on file-backup withholding 
necessary)  
B = Certified foreign [[Beneficial Owner]] 
account (form W8- BEN on file)  
C = Certified foreign [[intermediary]] 
account (form W8-IMY on file)  
D = Certified valid foreign account 
(form W8-ECI on file with ITIN)  
E = Certified foreign exempt account 
(form W8-EXP on file)  
F = W8 on file - no treaty rate claimed  
G = W8 Beneficiary with TIN on file 
H = W-8BEN-E on file/documentary 
evidence 
I = Voluntary FATCA withholding - W-
8BEN-E on file/documentary evidence 
J = W8-IMY or W-8BEN-E pending 
R 124 

---

## Page 42

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 42 
[[DTCC]] Internal (Green) 
Record 3 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Payable Information 
Indicator 
10 10 1 A/N 0 = Address of record  
1 = Payable address  
2 = Automatic clearing house  
3 = Cash to firm  
4 = Cross fund reinvest  
5 = Cash to Trust 
R 125 
Customer Name End 
Line Indicator 
11 11 1 A/N 1-6 = Line number where name ends R 126 
Customer Zip Code 12 22 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 
digits for future postal expansion 
R 127 
Social Code 23 24 2 A/N See Social Code List at 
https://dtcclearning.com/documents/m
utual-fund-services-1/mfs-cross-
product/codes-8/2498-social-
codes/file.html under General Codes. 
R 128 
NAV Account Indicator 25 25 1 A/N 0 = No    
1 = Yes 
R 129 
[[Margin]] Account 
Indicator 
26 26 1 A/N 0 = No  
1 = Yes 
R 079 
Check Writing 
Privileges Indicator 
27 27 1 A/N 0 = No  
1 = Yes 
R 083 
State of Sale (State 
Code) 
28 29 2 A/N See state code list in Fund/SERV 
manual 
R 012 
Country of Origin 
(Country Code) 
30 31 2 A/N Required for foreign account Fund 
Account Ind = 1 or 3). In this case, the 
value 'OC' Other Country) is not 
allowed 
OC 067 
Account 
Representative Name 
32 46 15 A/N Required for new networked account 
(Network Control Ind = 3 or 4, and 
Fund Account Ind = 0, 1 or 4) 
OC 076 
Account 
Representative 
Number 
47 55 9 A/N Required for new networked account 
(Network Control Ind = 3 or 4, and 
Fund Account Ind = 0, 1 or 4) 
OC 075 
Branch Identification 
Number 
56 64 9 A/N Required for new networked account 
(Network Control Ind = 3 or 4, and 
Fund Account Ind = 0, 1 or 4) 
OC 035 
New Firm of Record 65 68 4 A/N Space (for Network use only) R 086 

---

## Page 43

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 43 
[[DTCC]] Internal (Green) 
Record 3 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Number of Payables/ 
Beneficiaries 
69 70 2 N 00-06. 00-05 for Money Market 
purchase involving interactive 
[[participant]]).  
Must be > 00 if Payable Information 
Indicator = 1 or 2. 
R 130 
W8 Certification Date 71 78 8 N mmddccyy  
Required if Withhold Indicator = B, C, 
D or E 
OC 211 
W8 Expiration Date 79 86 8 N mmddccyy  
Required if Withhold Indicator = D or E 
OC 212 
W8 Override NRA 
Special Rate 
87 91 5 N 99.999 O 213 
W8 Qualified 
[[intermediary]] Indicator 
92 92 1 A/N Required if Withhold Indicator = C. 
1 = QI (qualified [[intermediary]] - primary 
withholding)  
2 = QI (Qualified [[intermediary]] non-
withholding)  
3 = Non-QI (non-Qualified 
[[intermediary]] - nonwithholding, not the 
[[Beneficial Owner]])  
4 = Partnership (withholding)  
5 = Partnership (nonwithholding)  
6 = U. S. branch (nonwithholding)  
7 = Trust (withholding)  
8 = Trust (non-withholding)  
9 = Territory Financial Institution 
OC 214 
W8 Override Country 
Code 
93 94 2 A/N The value 'OC' (Other Country) is not 
allowed 
O 067 
Standard [[ID]] 95 100 6 A/N  O  
 
 
  

---

## Page 44

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 44 
[[DTCC]] Internal (Green) 
02.10.04 Full Registration (401) Record 4 of 34 
Required 
Record 4 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 04 R 004 
Filler 5 7 3 A/N Space R  
Customer 
Name/Address Line 1 
8 42 35 A/N  R 131 
Customer 
Name/Address Line 2 
43 77 35 A/N  O  
Plan Account Number  78 97 20 A/N Plan account at the Trust, TPA, or 
Record Keeper 
O  
Plan Account Number 
Indicator  
98 98 1 A/N Required if Plan Account Number is 
provided.  
1 = Trust  
2 = TPA  
3= Record Keeper 
O/C 277 
Filler 99 100 2 A/N Space R  
 
 
  

---

## Page 45

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 45 
[[DTCC]] Internal (Green) 
02.10.05 Full Registration (401) Record 5 of 34 
Optional 
Record 5 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 05 R 004 
Filler 5 7 3 A/N Space R  
Customer 
Name/Address Line 3 
8 42 35 A/N  O  
Customer 
Name/Address Line 4 
43 77 35 A/N  O  
Filler 78 100 23 A/N Space R  
 
 
  

---

## Page 46

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 46 
[[DTCC]] Internal (Green) 
02.10.06 Full Registration (401) Record 6 of 34 
Optional 
Record 6 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 06 R 004 
Filler 5 7 3 A/N Space R  
Customer 
Name/Address Line 5 
8 42 35 A/N  O  
Columns 43-77 for regular registration (Registration Type = 0) 
Customer 
Name/Address Line 6 
43 77 35 A/N  O  
Columns 43-77 for Section 529 registration (Registration Type = 1) 
Customer City 43 75 33 A/N  R 238 
Customer State 76 77 2 A/N  R 239 
Filler 78 100 23 A/N Space R  
 
 
  

---

## Page 47

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 47 
[[DTCC]] Internal (Green) 
02.10.07 Full Registration (401) Record 7 of 34 
Optional 
Record 7 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 07 R 004 
Filler 5 7 3 A/N Space R  
Memo Field 8 19 12 A/N  O  
ACH (Automatic 
Clearing House) 
Indicator 
20 20 1 A/N 0 = No  
1 = Yes 
O 081 
Systematic 
Contribution 
(SIP/PAC/PIP) 
Indicator 
21 21 1 A/N 0 = No  
1 = Yes 
O 082 
SWP (Systematic 
Withdrawal Plan) 
Indicator 
22 22 1 A/N 0 = No  
1 = Yes 
O 083 
ROA/LOI Value 23 38 16 N 99,999,999,999,999.99 O 028 
LOI Number/Date 39 46 8 A/N  O  
Related Trade 
Indicator 
47 47 1 A/N 0 = No  
1 = Yes 
O 065 
Related Account 
Number 
48 67 20 A/N  O  
Related Account 
Number Indicator 
68 68 1 A/N Required if Related Account Number 
is provided.  
1 = Fund  
2 = Firm  
3 = Customer 
OC 157 
SWP/PAC Effective 
Date 
69 76 8 N mmddccyy O 132 
Customer Gender 77 77 1 A/N F = Female  
M = Male 
O 237 
Filler 78 100 23 A/N Space R  
  

---

## Page 48

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 48 
[[DTCC]] Internal (Green) 
02.10.08 Full Registration (401) Record 8 of 34 
Optional. Systematic withdrawals and automatic drafts 
Record 8 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 08 R 004 
Filler 5 7 3 A/N Space R  
CDSC Payment Code 8 8 1 A/N 0 = Gross  
1 = Net  
2 = Not applicable 
O 133 
Disbursement Options 9 9 1 A/N 0 = Fixed cash amount  
1 = Fixed percentage  
2 = Fixed [[shares]]  
3 = Declining balance 
O 134 
Disbursement Amount 10 25 16 N Format according to Disbursement 
[[Option]]:  
0 = 99,999,999,999,999.99  
1 = 999,999.9999999999  
2 = 999,999,999,999.9999  
3 = 999,999,999,999.9999 
O 135 
Monthly Payment 
Indicators 
26 37 12 A/N These 12 bytes represent 12 months 
respectively:  
1st byte = January,  
2nd byte = February, etc.  
For each byte:  
0 = No payment this month  
1 = Yes payment this month 
O 136 
Payment Date 
Indicator 
38 39 2 A/N 01-31 = Day of month  
L = Last day of month  
N = Normal fund cycle 
O 137 
Retirement Tax 
Indicator 
40 41 2 A/N Required if Payable 1 Address [[Option]] 
is provided and indicates systematic 
withdrawal.  
01 = Premature withdrawal  
02 = Rollover  
03 = Disability  
OC 138 

---

## Page 49

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 49 
[[DTCC]] Internal (Green) 
Record 8 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
04 = Death  
05 = Prohibited  
06 = Other  
07 = Normal  
08 = Refund by excess contributions  
09 = Divorce  
10 = Plan revoked  
11 = Fund transfer  
99 = Not applicable 
Shareholder Bank 
Account Number 
42 61 20 A/N  O  
Shareholder Bank 
Account Type 
62 62 1 A/N Required if Shareholder Bank 
Account Number is provided.  
0 = Checking  
1 = Savings  
2 = Other 
O 139 
First Check Date 63 70 8 N mmddccyy O 140 
ABA Routing Number 71 79 9 A/N Required if Payable Information 
Indicator denotes automatic clearing 
house 
OC 141 
Cost Basis [[Option]] 80 80 1 A/N 0 = Unknown 
1 = FIFO (First In First Out) 
2 = LIFO (Last In First Out) 
3 = High Cost 
4 = Low Cost 
5 = Average Cost 
6 = Select Lot 
O 165 
Filler 81 100 20 A/N Space R  
 
 
  

---

## Page 50

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 50 
[[DTCC]] Internal (Green) 
02.10.09a Full Registration (401) Record 9a of 34 (Payable) 
Note: 
Record 9 has three different formats. Address [[Option]] field (column 40) indicates which format is being used as follows: 
• If Payable 1 Address [[Option]] = 1, 2, … 9, then record 9 is in Payable format. 
• If Beneficiary/Successor Owner Address [[Option]] = A, B, C or D, then record 9 is in Beneficiary/Successor Owner 
format. 
• If Payable 1 Address [[Option]] = E or F, then record 9 is in Payable of x-[[settlement]] format.  
At least one Payable is required if Payable Information Indicator = 1 or 2.  
The following is record 9 for Payable (Payable 1 Address [[Option]] = 1, 2, … 9).  
Record 9A of 33  
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 09 R 004 
Filler 5 7 3 A/N Space R  
Payable 1 Account 
Number 
8 27 20 A/N Required if Payable Information 
Indicator = 2 
OC 142 
Payable 1 Zip Code 28 38 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 
digits for future postal expansion.  
Required if Payable Information 
Indicator = 1 
OC 144 
Payable 1 Name End 
Line Indicator 
39 39 1 A/N Required if Payable Information 
Indicator = 1 or 2.  
1-6 = Line number where name ends 
OC 145 
Payable 1 Address 
[[Option]] 
40 40 1 A/N Required if Payable Information 
Indicator = 1 or 2.  
1 = Dividends  
2 = Systematic withdrawals  
3 = Automatic drafts  
4 = [[Dividend]] and automatic drafts and 
systematic withdrawals  
5 = [[Dividend]] and automatic drafts  
6 = [[Dividend]] and systematic 
withdrawals  
7 = Automatic drafts and systematic 
withdrawals  
8 = Cross fund reinvest  
9 = Alternate payable 
OC 146 

---

## Page 51

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 51 
[[DTCC]] Internal (Green) 
Record 9A of 33  
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Payable 1 Account 
Number Indicator 
41 41 1 A/N Required if Payable 1 Account 
Number is provided.  
1 = Fund  
2 = Firm 
OC 143 
Payable 1 Security 
Issue Country Code 
42 43 2 A/N Space. For future use R  
Payable 1 Security 
Issue [[ID]] 
44 52 9 A/N Required if Payable 1 Address [[Option]] 
= 8 
OC 156 
Payable 1 Security 
Issue Check Digit 
53 53 1 A/N Space. For future use R  
Alternate Payable 1 
Indicator 
54 54 1 A/N Required if Payable 1 Address [[Option]] 
= 9.  
0 = Non-payable mailing address  
1 = Bank registration (for PAC)  
2 = Other 
OC 166 
Alternate Payable 1 
Reason 
55 74 20 A/N Required if Alternate Payable 1 
Indicator = 2. 
OC 167 
Filler 75 100 26 A/N Space R  
 
 
  

---

## Page 52

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 52 
[[DTCC]] Internal (Green) 
02.10.09b Full Registration (401) Record 9b of 34 
(Beneficiary/Successor Owner) 
Required for Section 529 registration (Registration Type = 1)  
• For Section 529 Plan (Registration Type = 1) at least one 529 Beneficiary (Beneficiary/Successor 
Owner Address [[Option]] = ‘C’) is required.  
• A Successor Owner (Beneficiary/Successor Owner Address [[Option]] = ‘D’) is required if Successor 
Owner Indicator = 1 and Section 529 (Registration Type = 1) and not allowed otherwise.  
• Not more than one Successor Owner is allowed. 
• Beneficiary/Successor Owner Address [[Option]] = ‘C’ or ‘D’ are not allowed for Regular Registration 
(Registration Type = 0). 
Record 9b of 34  
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 09 R 004 
Filler 5 7 3 A/N Space R  
Beneficiary/Successor 
Owner Date of Birth 
8 15 8 N mmddccyy R 203 
Shareholder Date of 
Birth 
16 23 8 N mmddccyy R 204 
Filler 24 27 4 A/N Space R  
Beneficiary/Successor 
Owner Zip Code 
28 38 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 
digits for future postal expansion. 
O 144 
Beneficiary/Successor 
Owner Name End Line 
Indicator 
39 39 1 A/N Required if Beneficiary/Successor 
Owner Name/Address is provided. 
1-6 = Line number where name ends 
OC 145 
Beneficiary/Successor 
Owner Address [[Option]] 
40 40 1 A/N A = Primary IRA Beneficiary  
B = Secondary IRA Beneficiary  
C = 529 Beneficiary  
D = 529 Successor Owner  
R 146 
Beneficiary/Successor 
Owner Relationship 
Indicator  
41 41 1 A/N 1 = Spouse  
2 = Non-Relative  
3 = Grandchild  
4 = Relative  
5 = Child 
O 205 
Filler 42 43 2 A/N Space R  

---

## Page 53

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 53 
[[DTCC]] Internal (Green) 
Record 9b of 34  
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Beneficiary/Successor 
Owner SSN/EIN 
Number 
44 52 9 A/N Required if Beneficiary/Successor 
Owner Address [[Option]] is “C” or “D” 
OC 103 
Beneficiary/Successor 
Owner SSN/EIN 
Indicator 
53 53 1 A/N Required if Beneficiary/Successor 
Owner SSN/EIN Number is provided.  
0 = Tax [[ID]] number  
1 = Social security number  
OC 102 
Filler 54 54 1 A/N Space R  
Beneficiary Percentage 
Rate 
55 60 6 N 999.999 R 184 
Date of Event 61 68 8 N mmddccyy O 217 
Beneficiary/Successor 
Owner U.S. Citizenship 
Indicator 
69 69 1 A/N Required if Beneficiary/Successor 
Owner Address [[Option]] is “C” or “D”  
0 = U.S. citizen  
1 = Not U.S. citizen 
OC 240 
Beneficiary Gender 70 70 1 A/N F = Female  
M = Male 
O 241 
Filler 71 100 30 A/N Space R  
 
 
  

---

## Page 54

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 54 
[[DTCC]] Internal (Green) 
02.10.09c Full Registration (401) Record 9c of 34 (Payable Of X-
[[settlement]]) 
The following record 9 will be used if the Payable 1 Address [[Option]] = E or F. 
Record 9c of 33  
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 09 R 004 
Filler 5 7 3 A/N Space R  
Payable 1 Bank 
Account Number 
8 27 20 A/N  R 142 
Payable 1 Bank ABA 
Routing Number 
28 36 9 A/N  R 141 
Filler 37 39 3 A/N Space R  
Payable 1 Address 
[[Option]] 
40 40 1 A/N E = ACH on demand  
F = Bank wire 
R 146 
Payable 1 Bank 
Account Type 
41 41 1 A/N 1 = Checking  
2 = Saving  
3 = Other 
R 143 
Filler 42 100 59 A/N Space R  
 
 
  

---

## Page 55

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 55 
[[DTCC]] Internal (Green) 
02.10.10 Full Registration (401) Record 10 of 34 
This record is required under the following conditions: 
• Section 529 Account (Registration Type = 1). 
• Payable Information Indicator = 1 or 2. 
 
This record is Optional for Payable of x-[[settlement]].  
Record 10 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 10 R 004 
Filler 5 7 3 A/N Space R  
Payable/Beneficiary/Su
ccessor Owner 1 
Name/Address Line 1 
8 42 35 A/N Required for Payable if Payable 
Information Indicator = 1 or 2.  
Required for IRA Beneficiary, 529 
Beneficiary or 529 Successor Owner 
OC 147 
Payable/Beneficiary/Su
ccessor Owner 1 
Name/Address Line 2 
43 77 35 A/N  O  
Filler 78 100 23 A/N Space R  
 
 
  

---

## Page 56

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 56 
[[DTCC]] Internal (Green) 
02.10.11 Full Registration (401) Record 11 of 34 
Optional 
Record 11 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 11 R 004 
Filler 5 7 3 A/N Space R  
Payable/Beneficiary/Su
ccessor Owner 1 
Name/Address Line 3 
8 42 35 A/N  O  
Payable/Beneficiary/Su
ccessor Owner 1 
Name/Address Line 4 
43 77 35 A/N  O 242 
Filler 78 100 23 A/N Space R  
 
 
  

---

## Page 57

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 57 
[[DTCC]] Internal (Green) 
02.10.12 Full Registration (401) Record 12 of 34 
Optional 
Record 12 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 12 R 004 
Filler 5 7 3 A/N Space R  
Payable/Beneficiary/Su
ccessor Owner 1 
Name/Address Line 5 
8 42 35 A/N  O  
Columns 43-77 for regular registration (Registration Type = 0) 
Payable/Beneficiary 1 
Name/Address Line 6 
43 77 35 A/N  O  
Columns 43-77 for Section 529 registration (Registration Type = 1) 
Beneficiary/Successor 
Owner 1 City 
43 75 33 A/N Optional if Successor Owner Indicator 
= 1 and Beneficiary/Successor Owner 
Address [[Option]] = “D”. 
Otherwise, this field is required. 
RC 242 
Beneficiary/Successor 
Owner 1 State 
76 77 2 A/N Optional if Successor Owner Indicator 
= 1 and Beneficiary/Successor Owner 
Address [[Option]] = “D”. 
Otherwise, this field is required. 
RC 243 
Filler 78 100 23 A/N Space R  
 
 
  

---

## Page 58

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 58 
[[DTCC]] Internal (Green) 
Record 13 Through 32  
Optional 
The previous group of four records (#9 through #12) may repeat itself 5 more times for additional 5 
Payables/Beneficiaries (4 more times for additional 4 Payables/Beneficiaries for Money Market 
purchase involving interactive [[participant]]).  
Logical Sequence Numbers should be as follows:  
Payable/Beneficiary 2 (Required if Number of Payables/Beneficiaries > 1) 
Logical Sequence Numbers: 13, 14, 15 and 16.  
Payable/Beneficiary 3 (Required if Number of Payables/Beneficiaries > 2) 
Logical Sequence Numbers: 17, 18, 19 and 20.  
Payable/Beneficiary 4 (Required if Number of Payables/Beneficiaries > 3) 
Logical Sequence Numbers: 21, 22, 23 and 24.  
Payable/Beneficiary 5 (Required if Number of Payables/Beneficiaries > 4) 
Logical Sequence Numbers: 25, 26, 27 and 28.  
Payable/Beneficiary 6 (Required if Number of Payables/Beneficiaries > 5) 
Logical Sequence Numbers: 29, 30, 31 and 32. 
 
 
  

---

## Page 59

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 59 
[[DTCC]] Internal (Green) 
02.10.14 Full Registration (401) Record 33 of 34 
Optional 
Record 33 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 33 R 004 
Filler 5 7 3 A/N Space R  
Chapter 4 Status Code 8 9 2 A/N See Chapter 4 Status Code List at 
https://dtcclearning.com/documents/m
utual-fund-services-1/mfs-cross-
product/codes-8/2240-chapter-4-
status-codes/file.html under the 
Codes section 
O 278 
Global [[intermediary]] 
Identification Number 
10 34 25 A/N IRS issued number to identify and 
establish FATCA status of a Foreign 
Financial Institution (FFI)  
O  
Underlying Client’s 
Foreign Tax [[ID]]  
35 59 25 A/N Foreign Tax [[ID]] of Underlying Client O  
FATCA Override 
Special Rate  
60 64 5 N 99.999 O 279 
Filler 65 100 36 A/N Space R  
 
 
  

---

## Page 60

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 60 
[[DTCC]] Internal (Green) 
02.10.15 Full Registration (401) Record 34 of 34 
Optional 
Record 34 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Physical Sequence 
Number 
1 2 2 A/N  R 004 
Logical Sequence 
Number 
3 4 2 A/N 34 R 004 
Filler 5 7 3 A/N Space R  
[[intermediary]] Program  
Indicator–1 
8 11 4 A/N Indicates the program, platform, or 
channel applicable to an account.  
Examples may include: 
• Program indicator for advisory 
accounts 
• Distribution channel applicable to 
the account (e.g., retail, RIA, etc.) 
• Retirement platform pertaining to 
the account 
Values are uniquely defined by each 
[[intermediary]]. 
O  
[[intermediary]] Program  
Indicator–2 
12 15 4 A/N Further defines the program, platform, 
or channel applicable to an account.  
Values are uniquely defined by each 
[[intermediary]].  
O  
Servicing Group [[ID]] 16 24 9 A/N This field is used to communicate 
aggregated servicing relationships or 
define additional relationships on 
accounts.  
Examples may include: 
• Consolidating (Super) Branches 
• Third-party administrators (TPAs) 
• Investment Advisers 
• Consultants 
This field does not replace the main 
branch field on the account.  
Values are uniquely defined by each 
[[intermediary]]. 
O  
Additional Relationship  
[[ID]]–1 
25 44 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts.  
Values are uniquely defined by each 
[[intermediary]].  
O  

---

## Page 61

Fixed Length Record Layouts (Part 2) 
Full Registration (401) 61 
[[DTCC]] Internal (Green) 
Record 34 of 34 
Field Name  
Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
Additional Relationship  
[[ID]]–2 
45 64 20 A/N This field is used to communicate 
additional relationship details to 
further define servicing relationships 
between accounts.  
Values are uniquely defined by each 
[[intermediary]].  
O  
Filler 65 100 36 A/N Space R  

---

## Page 62

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 62 
[[DTCC]] Internal (Green) 
ACATS TRANSFER (018) 
02.11.01 ACATS Transfer (018) Record 1 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 1 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 01 
Originator Type 5 5 1 A/N B = Firm  
F = Fund 
Filler 6 7 2 A/N Space 
Firm Number 8 11 4 N  
Filler 12 14 3 A/N Space 
Record Type 15 17 3 A/N 018 = ACATS Transfer 
Test Indicator 18 18 1 A/N 0 = Production  
1 = Test 
Filler 19 19 1 A/N Space 
Fund Number 20 23 4 N  
Filler 24 26 3 A/N Space 
Security Issue Country 
Code 
27 28 2 A/N Space. For future use 
Security Issue [[ID]] 29 37 9 A/N  
Security Issue Check Digit 38 38 1 A/N Space. For future use 
Filler 39 40 2 A/N Space 
Fund/SERV Control Number 41 55 15 A/N  
Correction Indicator 56 56 1 A/N C-N = Pre-[[settlement]] correction  
P = Post [[settlement]] correction/cancellation  
Space = No correction 
Filler 57 59 3 A/N Space 
Processing Date 60 67 8 N mmddccyy 
Filler 68 75 8 A/N Space 

---

## Page 63

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 63 
[[DTCC]] Internal (Green) 
Record 1 of 34 
Field Name  
Start End Len Type Description  
Book/Physical Share 
Indicator 
76 76 1 A/N 1 = Transfer in & out: book [[shares]]  
2 = Transfer in: book [[shares]]  
Transfer out: physical [[shares]] 
PI Delivery Indicator 77 77 1 A/N 0 = Deliver to customer  
1 = Deliver to firm  
2 = Deliver to agent for firm  
Space = N/A 
Filler 78 84 7 A/N Space 
TPA/Investment Agent 
Number 
85 88 4 A/N  
Filler 89 91 3 A/N Space 
Secondary Social Security 
Number  
92 100 9 A/N Secondary Social Security Number associated 
to Account 
ACATS will populate this field with the value in 
the ‘Original Receiver Customer SS 
Number/Tax [[ID]] Secondary’ field from the 
Transfer Input (TI). This field is used for PTF’s 
when Fund is either the deliverer or receiver.  
If the Fund is a deliverer and the Firm is the 
receiver this field is the ‘Original Receiver 
Customer SS Number Secondary’ from the TI 
record. The value in the ‘Original Receiver 
Customer SS Number Secondary’ on the TI 
record may be different from the SSN/EIN on 
the FR record or the Receiving Customer’s 
Primary Social Security Number on the TI 
record. 
Best Practice: The secondary social security 
number should be applied to search criteria 
when identifying accounts that may have 
multiple account owners. 
 
 
  

---

## Page 64

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 64 
[[DTCC]] Internal (Green) 
02.11.02 ACATS Transfer (018) Record 2 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 2 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 02 
Filler 5 7 3 A/N Space 
Filler 8 21 14 A/N Space 
Customer Name 22 41 20 A/N  
Fund Account Indicator 42 42 1 A/N 0 = New account–domestic  
1 = New account–foreign  
2 = Existing account–domestic  
3 = Existing account–foreign 
4 = New account–US Tax Resident Living 
Abroad  
5 = Existing account–US Tax Resident Living 
Abroad  
Customer Account Number 
at Fund 
43 62 20 A/N  
Filler 63 63 1 A/N Space 
Agent for Firm Number 64 67 4 A/N  
Network Control Indicator 68 68 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
Filler 69 69 1 A/N Space 
SSN/EIN Indicator 70 70 1 A/N ACATS populates this field with one of the 
following values from the Fund Registration 
(FR) record:  
0 = Tax [[ID]] Number 
1 = Social Security Number 
2= [[investor]] EIN (Employee Identification 
Number)  
Exception: 
If ACATS does not receive an FR record, the 
[[default]] value for this field is ‘0’. 

---

## Page 65

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 65 
[[DTCC]] Internal (Green) 
Record 2 of 34 
Field Name  
Start End Len Type Description  
SSN/EIN Number 71 79 9 A/N ACATS populates this field with the SSN/EIN 
submitted on the FR by the receiver.  
Exceptions: 
For a PTF where the Fund is a receiver, if 
ACATS does not receive an FR record from 
the Firm, ACATS populates this field with the 
value in the ‘Receiving Customer’s Primary 
Social Security Number’ from the Transfer 
Initiation (TI) record. 
For a PTF where the Fund is a deliverer, if 
ACATS does not get a FR from the Firm, 
ACATS populates this field with the Receiving 
[[participant]]’s Tax [[ID]] number from the ACATS 
[[participant]] master file. 
For all other transfer types, if ACATS does not 
receive an FR record, ACATS populates this 
field with the Receiving [[participant]]’s Tax [[ID]] 
number from the ACATS [[participant]] master 
file. 
Original Deliverer Customer 
Account Number  
80 99 20 A/N Underlying Customer Account Number at the 
Delivering Firm 
Filler 100 100 1 A/N Space 
 
 
  

---

## Page 66

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 66 
[[DTCC]] Internal (Green) 
02.11.03 ACATS Transfer (018) Record 3 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 3 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 03 
Filler 5 7 3 A/N Space 
[[Dividend]] Code 8 8 1 A/N  [[Dividend]]  LTCG  STCG  
0 =  Cash  Cash  Cash  
1 =  Reinvest  Reinvest  Reinvest 
2 =  Cash  Cash  Reinvest 
3 =  Cash  Reinvest  Reinvest 
4 =  Cash  Reinvest  Cash  
5 =  Reinvest  Cash  Cash  
6 =  Reinvest  Reinvest  Cash  
7 =  Reinvest  Cash  Reinvest 
 

---

## Page 67

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 67 
[[DTCC]] Internal (Green) 
Record 3 of 34 
Field Name  
Start End Len Type Description  
Withhold Indicator 9 9 1 A/N W9 indications 
0 = Certified (W-9 on file) 
1 = Failure to provide tin 
2 = Failure to certify tin 
3 = Notification of incorrect TIN from the 
Secretary of Treasury (Withhold due to B 
Notice) 
4 = Failure to certify backup withholding status 
5 = Voluntary disclosure from payee of 
affirmative backup withholding status 
6 = Notification to commence Backup 
Withholding from Secretary of Treasury for 
underreporting [[Dividend]] and/or interest 
payments (Withhold due to C Notice) 
7 = Applied for social security number 
8 = Exempt recipient 
9 = Account(s) subject to both B and C Notice 
Withholding 
W8 indications 
A = Uncertified foreign account (no W8 form 
on file-backup withholding necessary) 
B = Certified foreign [[Beneficial Owner]] account 
(form W8-BEN on file) 
C = Certified foreign [[intermediary]] account 
(form W8-IMY on file) 
D = Certified valid foreign account (form W8-
ECI on file with ITIN) 
E = Certified foreign exempt account (form 
W8-EXP on file) 
F = W8 on file - no treaty rate claimed 
G = W8 Beneficiary with TIN on file 
Payable Information 
Indicator 
10 10 1 A/N 0 = Address of record  
1 = Payable address  
2 = Automatic clearing house  
3 = Cash to firm  
4 = Cross fund reinvest  
Customer Name End Line 
Indicator 
11 11 1 A/N 1-6 = Line number where name ends 
Customer Zip Code 12 22 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 digits 
for future postal expansion 

---

## Page 68

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 68 
[[DTCC]] Internal (Green) 
Record 3 of 34 
Field Name  
Start End Len Type Description  
Social Code 23 24 2 A/N See Social Code List at 
https://dtcclearning.com/documents/mutual-
fund-services-1/mfs-cross-product/codes-
8/2498-social-codes/file.html under the Codes 
section 
NAV Account Indicator 25 25 1 A/N 0 = No  
1 = Yes 
[[Margin]] Account Indicator 26 26 1 A/N 0 = No  
1 = Yes 
Check Writing Privileges 
Indicator 
27 27 1 A/N 0 = No  
1 = Yes 
State of Sale (State Code) 28 29 2 A/N See state code list in Fund/SERV manual 
Country of Origin Country 
Code) 
30 31 2 A/N  
Account Representative 
Name 
32 46 15 A/N  
Account Representative 
Number 
47 55 9 A/N  
Branch Identification 
Number 
56 64 9 A/N  
Filler 65 68 4 A/N Space 
Number of Payables 69 70 2 N 00-06 
W8 Certification Date 71 78 8 N mmddccyy 
W8 Expiration Date 79 86 8 N mmddccyy 
W8 Override NRA Special 
Rate 
87 91 5 N 99.999 
W8 Qualified [[intermediary]] 
Indicator 
92 92 1 A/N 1 = QI (qualified [[intermediary]] - primary 
withholding)  
2 = QI (Qualified [[intermediary]] - non-
withholding)  
3 = Non-QI (non-Qualified [[intermediary]] - non-
withholding, not the [[Beneficial Owner]])  
4 = Partnership (withholding)  
5 = Partnership (non-withholding)  
6 = U. S. branch (non-withholding)  
7 = Trust (withholding)  
8 = Trust (non-withholding) 

---

## Page 69

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 69 
[[DTCC]] Internal (Green) 
Record 3 of 34 
Field Name  
Start End Len Type Description  
W8 Override Country Code 93 94 2 A/N  
Filler 95 100 6 A/N Space 
 
 
  

---

## Page 70

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 70 
[[DTCC]] Internal (Green) 
02.11.04 ACATS Transfer (018) Record 4 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 4 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 04 
Filler 5 7 3 A/N Space 
Customer Name/Address 
Line 1 
8 42 35 A/N  
Customer Name/Address 
Line 2 
43 77 35 A/N  
Filler 78 100 23 A/N Space 
 
 
  

---

## Page 71

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 71 
[[DTCC]] Internal (Green) 
02.11.05 ACATS Transfer (018) Record 5 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 5 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 05 
Filler 5 7 3 A/N Space 
Customer Name/Address 
Line 3 
8 42 35 A/N  
Customer Name/Address 
Line 4 
43 77 35 A/N  
Filler 78 100 23 A/N Space 
 
 
  

---

## Page 72

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 72 
[[DTCC]] Internal (Green) 
02.11.06 ACATS Transfer (018) Record 6 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 6 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 06 
Filler 5 7 3 A/N Space 
Customer Name/Address 
Line 5 
8 42 35 A/N  
Customer Name/Address 
Line 6 
43 77 35 A/N  
Originating Receiver 
Customer Account Number 
at Firm 
78 97 20 A/N Underlying Customer Account Number at the 
Originating Firm 
Filler 98 100 3 A/N Space 
 
 
  

---

## Page 73

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 73 
[[DTCC]] Internal (Green) 
02.11.07 ACATS Transfer (018) Record 7 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 7 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 07 
Filler 5 7 3 A/N Space 
Transaction Type 8 8 1 A/N 1 = Transfer to new account  
2 = Transfer to existing account  
3 = Firm of record change only 
Account Type Indicator 9 9 1 A/N 1 = Customer name  
2 = [[street name]] 
Customer Account Number 
at Firm 
10 29 20 A/N  
Delivering Firm Number 30 33 4 A/N  
Customer Account Number 
at Fund (Delivering Firm) 
34 53 20 A/N  
Customer Account Number 
at Firm (Delivering Firm) 
54 73 20 A/N  
Network Control Indicator 
(Delivering Firm) 
74 74 1 A/N 0 = Non-networked  
3 = Matrix level 3  
4 = Matrix level 4 
Agent for Delivering Firm 
Number 
75 78 4 A/N  
Fraction Indicator 79 79 1 A/N 1 = Transfer fraction  
2 = [[liquidation]] fraction 
Full/Partial Indicator 80 80 1 A/N 0 = Full - move all [[shares]] in the account at the 
Fund  
1 = Partial - move the exact share quantity 
specified 
Transfer Share Quantity 81 94 14 N 9,999,999,999.9999 
CDSC Transfer Indicator 95 95 1 A/N Space 
Note: 
This field will be eliminated in the future 

---

## Page 74

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 74 
[[DTCC]] Internal (Green) 
Record 7 of 34 
Field Name  
Start End Len Type Description  
Delivering Firm Share Aging 
Indicator 
96 96 1 A/N 1 = The delivering firm or fund company will 
provide the share aging information in an 
automated fashion through the Networking 
Share Aging file. 
2 = The delivering firm or fund company will 
provide the share aging information outside of 
the system. 
Membership Identifier 97 98 2 A/N 01 = Trust [[Member]] 
Membership Identifier 
(Delivering Firm) 
99 100 2 A/N 01 = Trust [[Member]] 
 
 
  

---

## Page 75

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 75 
[[DTCC]] Internal (Green) 
02.11.08 ACATS Transfer (018) Record 8 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 8 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 08 
Filler 5 7 3 A/N Space 
Transfer Money Amount 8 23 16 N 99,999,999,999,999.99 
Currency Indicator 24 26 3 A/N  
[[default]] Registration 27 27 1 A/N 0 = No [[default]]  
1 = [[default]] Registration 
ACATS Control Number 28 47 20 A/N  
Transfer Disbursement 
[[Option]] - Accruals 
48 48 1 A/N 2 = Cash to customer - Delivering firm  
4 = Reinvest - Receiving firm (bucket to 
bucket) 
Transfer Disbursement 
[[Option]] - Fractional Cash-in-
lieu 
49 49 1 A/N 0 = Cash to [[Broker]] - Delivering firm  
1 = Reinvest - Delivering firm  
2 = Cash to customer - Delivering firm  
3 = Cash to [[Broker]] - Receiving firm  
4 = Reinvest - Receiving firm  
5 = Cash to customer - Receiving firm 
Transfer Disbursement 
[[Option]] - Residuals 
50 50 1 A/N 0 = Cash to [[Broker]] - Delivering firm  
1 = Reinvest - Delivering firm  
2 = Cash to customer - Delivering firm  
3 = Cash to [[Broker]] - Receiving firm  
4 = Reinvest - Receiving firm  
5 = Cash to customer - Receiving firm 
NRA Tax 51 52 2 N .99 
[[settlement]] Date 53 60 8 A/N mmddccyy 
Accrual Money Amount 61 76 16 N 99,999,999,999,999.99 
Accrual Money Amount 
Indicator 
77 77 1 A/N A = All  
B = None 
Customer SSN/EIN Number 78 86 9 A/N ACATS populates this field with the value in 
the ‘Receiving Customer’s Primary Social 

---

## Page 76

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 76 
[[DTCC]] Internal (Green) 
Record 8 of 34 
Field Name  
Start End Len Type Description  
Security’ field from the TI record. This field is 
used for PTFs only, when Fund is either the 
deliverer or the receiver.  
The rule above is true in all circumstances, 
both when the receiver submits the FR record 
and when ACATS uses a [[default]] registration. 
Note: 
The value in the ‘Receiving Customer’s 
Primary Social Security Number’ on the TI 
record may be different from the SSN/EIN on 
the FR record. 
ACATS Account Type  87 88 2 A/N See list in ACATS Manual 
Gift/Donation Indicator  89 89 1 A/N 0 or Space = No, not a gift or donation 
1 = Yes, it is a gift or donation 
Originating Receiver Firm 
Number 
90 93 4 A/N Originating receiving [[Broker]] firm number 
Originating Delivering Firm 
Number 
94 97 4 A/N Originating delivering [[Broker]] firm number 
Filler 98 100 3 A/N Space 
 
 
  

---

## Page 77

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 77 
[[DTCC]] Internal (Green) 
02.11.09 ACATS Transfer (018) Record 9 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified. 
Record 9 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 09 
Filler 5 7 3 A/N Space 
Memo Field 8 19 12 A/N  
ACH (Automatic Clearing 
House) Indicator 
20 20 1 A/N 0 = No  
1 = Yes 
PAC (Pre Authorized 
Checks) Indicator 
21 21 1 A/N 0 = No  
1 = Yes 
SWP (Systematic 
Withdrawal Plan) Indicator 
22 22 1 A/N 0 = No  
1 = Yes 
ROA/LOI Value 23 38 16 N 99,999,999,999,999.99 
LOI Number/Date 39 46 8 A/N  
Related Trade Indicator 47 47 1 A/N 0 = No  
1 = Yes 
Related Account Number 48 67 20 A/N  
Related Account Number 
Indicator 
68 68 1 A/N 1 = Fund  
2 = Firm 
SWP/PAC Effective Date 69 76 8 N mmddccyy 
IRS 529 Annual Strategy 
Change Counter 
 
Effective 05/15/2023 
77 77 1 A/N 0 thru 9  
 
Number of strategy changes that occurred 
during a calendar year. 
Earnings to Date Money 
Amount 
 
Effective 05/15/2023 
78 93 16 N 99,999,999,999,999.99 
 
Earnings of [[shares]] being transferred. 
Negative Earnings to Date 
Indicator 
 
94 94 1 A/N N  = Negative                         
Space = Positive 

---

## Page 78

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 78 
[[DTCC]] Internal (Green) 
Record 9 of 34 
Field Name  
Start End Len Type Description  
Effective 05/15/2023 Indicates if the earnings amount is 
negative. 
Filler 95 100 6 A/N Space 
 
 
  

---

## Page 79

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 79 
[[DTCC]] Internal (Green) 
02.11.10 ACATS Transfer (018) Record 10 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 10 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 10 
Filler 5 7 3 A/N Space 
CDSC Payment Code 8 8 1 A/N 0 = Gross  
1 = Net  
2 = Not applicable 
Disbursement Options 9 9 1 A/N 0 = Fixed cash amount  
1 = Fixed percentage  
2 = Fixed [[shares]]  
3 = Declining balance 
Disbursement Amount 10 25 16 N Format according to Disbursement [[Option]]:  
0 = 99,999,999,999,999.99  
1 = 999,999.9999999999  
2 = 999,999,999,999.9999  
3 = 999,999,999,999.9999 
Monthly Payment Indicators 26 37 12 A/N These 12 bytes represent 12 months 
respectively:  
1st byte = January,  
2nd byte = February, etc.  
For each byte:  
0 = No payment this month  
1 = Yes payment this month 
Payment Date Indicator 38 39 2 A/N 01-31 = Day of month  
L = Last day of month  
N = Normal fund cycle 

---

## Page 80

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 80 
[[DTCC]] Internal (Green) 
Record 10 of 34 
Field Name  
Start End Len Type Description  
Retirement Tax Indicator 40 41 2 A/N 01 = Premature withdrawal  
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
42 61 20 A/N  
Shareholder Bank Account 
Type 
62 62 1 A/N 0 = Checking  
1 = Savings  
2 = Other 
First Check Date 63 70 8 N mmddccyy 
ABA Routing Number 71 79 9 A/N  
Cost Basis [[Option]] 80 80 1 A/N 0 = Unknown 
1 = FIFO (First In First Out) 
2 = LIFO (Last In First Out) 
3 = High Cost 
4 = Low Cost 
5 = Average Cost 
6 = Select Lot 
Cost Basis Money Amount 
 
Effective 05/15/2023 
81 96 16 N 99,999,999,999,999.99 
 
Original cost of the [[shares]] being 
transferred. 
Filler 97 100 4 A/N Space 
 
 
  

---

## Page 81

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 81 
[[DTCC]] Internal (Green) 
02.11.11 ACATS Transfer (018) Record 11 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 11 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 11 
Filler 5 7 3 A/N Space 
Payable 1 Account Number 8 27 20 A/N  
Payable 1 Zip Code 28 38 11 A/N 5-digit Zip Code + 4-digit Zip-Four + 2 digits 
for future postal expansion. 
Payable 1 Name End Line 
Indicator 
39 39 1 A/N 1-6 = Line number where name ends 
Payable 1 Address [[Option]] 40 40 1 A/N 1 = Dividends  
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
41 41 1 A/N 1 = Fund  
2 = Firm 
Payable 1 Security Issue 
Country Code 
42 43 2 A/N Space. For future use 
Payable 1 Security Issue [[ID]] 44 52 9 A/N  
Payable 1 Security Issue 
Check Digit 
53 53 1 A/N Space. For future use 
Alternate Payable 1 
Indicator 
54 54 1 A/N 0 = Non-payable mailing address  
1 = Bank registration (for PAC)  
2 = Other 
Alternate Payable 1 Reason 55 74 20 A/N  
Filler 75 100 26 A/N Space 

---

## Page 82

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 82 
[[DTCC]] Internal (Green) 
02.11.12 ACATS Transfer (018) Record 12 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 12 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 12 
Filler 5 7 3 A/N Space 
Payable 1 Name/Address 
Line 1 
8 42 35 A/N  
Payable 1 Name/Address 
Line 2 
43 77 35 A/N  
Filler 78 100 23 A/N Space 
 
 
  

---

## Page 83

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 83 
[[DTCC]] Internal (Green) 
02.11.13 ACATS Transfer (018) Record 13 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 13 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 13 
Filler 5 7 3 A/N Space 
Payable 1 Name/Address 
Line 3 
8 42 35 A/N  
Payable 1 Name/Address 
Line 4 
43 77 35 A/N  
Filler 78 100 23 A/N Space 
 
 
  

---

## Page 84

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 84 
[[DTCC]] Internal (Green) 
02.11.14 ACATS Transfer (018) Record 14 of 34 
Output from [[NSCC]] to funds. All fields pertain to the Receiving Firm except when Delivering Firm is 
specified.  
Record 14 of 34 
Field Name  
Start End Len Type Description  
Physical Sequence Number 1 2 2 A/N  
Logical Sequence Number 3 4 2 A/N 14 
Filler 5 7 3 A/N Space 
Payable 1 Name/Address 
Line 5 
8 42 35 A/N  
Payable 1 Name/Address 
Line 6 
43 77 35 A/N  
Filler 78 100 23 A/N Space 
 
 
  

---

## Page 85

Fixed Length Record Layouts (Part 2) 
ACATS Transfer (018) 85 
[[DTCC]] Internal (Green) 
Record 15 through 34  
The previous group of four records (#11 through #14) may repeat itself 5 more times for additional 5 
Payables.  
Logical Sequence Numbers should be as follows:  
Payable 2 - Logical Sequence numbers: 15, 16, 17 and 18.  
Payable 3 - Logical Sequence numbers: 19, 20, 21 and 22.  
Payable 4 - Logical Sequence numbers: 23, 24, 25 and 26.  
Payable 5 - Logical Sequence numbers: 27, 28, 29 and 30.  
Payable 6 - Logical Sequence numbers: 31, 32, 33 and 34.

---

## Page 86

 
[[DTCC]] Internal (Green) 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: September 1, 2023 
Publication Code: MFS313 
Service: Fund/SERV® 
Title: Fixed Length Record Layouts (Part 2) 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 