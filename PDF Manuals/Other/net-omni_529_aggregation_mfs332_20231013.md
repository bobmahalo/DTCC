---
title: "Networking - Omni/SERV - 529 Aggregation Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net-omni_529_aggregation_mfs332_20231013.pdf"
pages: 31
size: "466.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Networking - Omni/SERV - 529 Aggregation Record Layouts

**Original File:** [net-omni_529_aggregation_mfs332_20231013.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net-omni_529_aggregation_mfs332_20231013.pdf)  
**Category:** Other  
**Total Pages:** 31  
**File Size:** 466.6 KB  

---

## Page 1

 
 
 
Networking - Omni/SERV 
529 AGGREGATION RECORD LAYOUTS 
OCTOBER 13, 2023 
 

---

## Page 2

529 Aggregation Record Layouts 
History of Important Notices 2 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 3 
File Overview ........................................................................................................................................................ 4 
Record Sequence Order ..................................................................................................................................... 4 
Record Layouts .................................................................................................................................................... 6 
529 Aggregation Header (B/F/G10) ..................................................................................................................... 7 
529 Aggregation Account Level Detail (B/F11) ................................................................................................. 9 
529 Aggregated Detail (G12) ............................................................................................................................. 15 
529 Aggregation Trailer (B/F/G14) .................................................................................................................... 19 
529 Aggregation Grand Total Trailer (B/F/G16) ............................................................................................... 21 
Input Record Layout .......................................................................................................................................... 22 
Datatrak Header ................................................................................................................................................22 
Datatrak Trailer .................................................................................................................................................23 
Output Record Layout ....................................................................................................................................... 24 
[[NSCC]] Output Header (N00) .............................................................................................................................24 
APPENDIX – Summary of Changes .................................................................................................................. 25 
Summary of Changes – effective Q4, 2020 ...................................................................................................... 26 
Summary of Changes – effective Q1, 2019 ...................................................................................................... 27 
Summary of Changes – effective Q3, 2018 ...................................................................................................... 28 
Summary of changes – effective Q2, 2015 ...................................................................................................... 29 
 

---

## Page 3

529 Aggregation Record Layouts 
History of Important Notices 3 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notices 
October 13, 2023 Records rebranded and reviewed.  
May 11, 2023 Record rebranded and reviewed. 
November 16, 2020 Please see Important Notices: 
a8881 P&S 8454 Dated August 06, 2020 
March 25, 2019 Please see Important Notices: 
a8658 P&S 8233 Dated December 19, 2018 
August 22, 2018 A number of Description fields in these record layouts have been 
updated to align with the language adopted during a review of the 529 
Aggregation best practices. 
April 27, 2015 Please see Important Notices: 
a7926 P&S 7501 Dated November 4, 2014 
November 18, 2014 Added File Overview & Record Sequence Order 
(see Table of Contents) 
March 21, 2011 Please see Important Notices: 
a7120 P&S 6691 Dated December 16, 2010 

---

## Page 4

529 Aggregation Record Layouts 
File Overview 4 
FILE OVERVIEW 
1. The 529 Aggregation Records are fixed and 480 bytes. 
2. Files sent to [[NSCC]] are for a Submitting [[participant]] Number, for each Program State Code, for a 
Receiving [[participant]]. 
3. Firms, Funds and Aggregators must program to transmit files to [[NSCC]] (DataTrak) and must also program 
to receive files from [[NSCC]] (AutoRoute): 
a. Firms (System Code = B) or Funds (System Code = F) must program to transmit files to [[NSCC]] 
(DataTrak 26945) and must also program to receive files from [[NSCC]] via: 
- AutoRoute 02101945 – to receive back the [[NSCC]] rejected records; 
- AutoRoute 02101946 – to receive the accepted by [[NSCC]] data from Aggregator to that 
Firm/Fund. 
b. Aggregators (System Code = G) must program to transmit files to [[NSCC]] (DataTrak 26946) and must 
also program to receive files from [[NSCC]] via: 
- AutoRoute 02101946 – to receive back the [[NSCC]] rejected records; 
- AutoRoute 02101945 – to receive the accepted by [[NSCC]] data from Firm/Fund to that 
Aggregator. 
4. Multiple Detail Records (B/F11 and G12) can be sent in one file. These records will be defined, per 
grouping, between header and trailer records. In the case of 529 Aggregation records, a Program State 
Code in the Detail records must = Program State Code of the Header and the Trailer records.  
Record Sequence Order 
Firms/Funds should transmit records to [[NSCC]] in the following sequence order:  
HDR.S DataTrak Header 26945 
B/F10 529 Aggregation Header 
B/F11 Detail Records 
B/F14 529 Aggregation Trailer 
B/F16 529 Aggregation Grand Total Trailer (Optional) - [[NSCC]] will create the B/F16 on the output to Aggregator. 
End.S DataTrak 26945 Trailer 
 
[[NSCC]] will transmit records to the Aggregator in the following sequence order:  
1 Trans AutoRoute Header (Optional) 
N00 [[NSCC]] Output Header 02101945 
B/F10 529 Aggregation Header 
B/F11 Detail Records 
B/F14 529 Aggregation Trailer 
B/F16 529 Aggregation Grand Total Trailer (Optional) - [[NSCC]] will create the B/F16 on the output to Aggregator. 
 
Aggregated files from Aggregator sent to [[NSCC]] will be transmitted in the following order:  
 
HDR.S DataTrak Header 26946 
G10 Aggregation Header 
G12 Aggregated Detail (when applicable) 
G14 Aggregation Trailer 
G16 Grand Total Trailer (Optional) - [[NSCC]] will create the G16 on output from the Aggregator 
End.S DataTrak Trailer 26946 
 
 

---

## Page 5

529 Aggregation Record Layouts 
File Overview 5 
Aggregated files from [[NSCC]] to firms/funds will be transmitted in the following order:  
1 Trans AutoRoute Header (Optional) 
N00 [[NSCC]] Output Header 02101945 
G10 Aggregation Header 
G12 Aggregated Detail (when applicable) 
G14 Aggregation Trailer 
G16 Grand Total Trailer (Optional) - [[NSCC]] will create the G16 on output from the Aggregator 
---------------------------------------------------------------------------------------------------------------------------------------  
 
 
File Structure Examples Sent to [[NSCC]] 
 
 
Example 1: 
The submitting firm/fund will create files for each recipient, per State Plan. In this example the firm submitting to [[NSCC]] has 
with multiple state plans with multiple receiving participants. 
Firm AAAA has NY and KS state plans. NY plans will be sent to Fund 1111 and 2222. KS plans will be sent to Fund 1111. 
The format is as follows: 
HDR.S DataTrak Header 26945 
B/F10 Header – Submitting [[participant]] #AAAA, (NY) state, Receiving [[participant]] #1111 
B/F11 Detail Record (NY) 
B/F11 Detail Record (NY) 
B/F11 Detail Record (NY) 
B/F14 Trailer - Submitting [[participant]] #AAAA, (NY), Receiving [[participant]] #1111  
 
B/F10 – Submitting [[participant]] #AAAA, (KS) state, Receiving [[participant]] #1111 
B/F11 Detail Record (KS) 
B/F11 Detail Record (KS) 
B/F14 Trailer - Submitting [[participant]] #AAAA, (KS), Receiving [[participant]] #1111 
 
B/F10 - Submitting [[participant]] #AAAA, (NY) state, Receiving [[participant]] #2222 
B/F11 Detail Record (NY) 
B/F14 Trailer -Submitting [[participant]] #AAAA, (NY), Receiving [[participant]] #2222 
B/F16 529 Aggregation Grand Total Trailer (Optional) 
End.S DataTrak Trailer 26945 
 
Example 2: 
Aggregator is sending [[NSCC]] a file that has both matched account(s) for one firm and empty header/trailers signifying no 
matches for a second dealer/recipient. 
Aggregator (GGGG) is returning data to firms AAAA & PPPP. 
1) Matched 1 account for firm AAAA for NY plan 
2) Returning empty header/trailer records to firm PPPP to signify that data was received but no matches occurred for that 
firm’s data. 
Best Practice: Aggregators are to send back empty header/trailers to firms when no matches occur. 
HDR.S DataTrak Header 26946 
G10 Header – Submitting Aggregator #GGGG (NY) state, Receiving [[participant]] #AAAA 
G12 Detail Record (NY) (1 detail record for matched account) 
G14 Trailer- Submitting Aggregator #GGGG, (NY) state, Receiving [[participant]] #AAAA 
 
G10 Header – Submitting Aggregator #GGGG (LA), Receiving [[participant]] #PPPP (no matches) 
G14 Trailer – Submitting Aggregator #GGGG (LA), Receiving [[participant]] #PPPP 
G16 Grand Total Trailer (Optional) - [[NSCC]] will create the G16 on output from the Aggregator 
End.S DataTrak Trailer 26946 

---

## Page 6

529 Aggregation Record Layouts 
Record Layouts 6 
RECORD LAYOUTS 
The following are Networking Omni/SERV - 529 Aggregation Record Layouts. The column headings are as 
follows: 
Field Name - The name of the field. 
Start - The position in which the field starts 
End - The position in which the field ends 
Len - The length of the field in bytes 
Type - The type of the field: 
A/N = Alphanumeric  
N = Numeric 
Description - Field description (format, valid values, conditional requirements, etc.). 
Req/Opt - Indicates whether the field is optional or required: 
O = Optional  
R = Required  
OC = Generally optional, but required upon specified conditions  
RC = Generally required, but optional upon specified conditions 
Reject Code - The Networking reject code which indicates that this field is invalid. 
 
• Alphanumeric type fields may include any character in the computer character set but  should not include 
unprintable characters such as Low-Value, High-Value, Comp-3 fields, etc., since these kinds of 
characters may cause problems during transmission time. 
• Numeric type fields may include digits (0-9) only. 
• Required fields mean the following: 
a. Fields with specified list of values must have one of those values. 
b. Alphanumeric type fields without specified list of values may have any value as described in the first 
note above but must not be spaces. 
c. Numeric type fields without a specified list of values must be numeric greater than zero.  
d. Fields with other requirements must follow these requirements (for example Submitting [[participant]] 
Number must be valid and eligible for Networking). 
• Optional fields mean the following: 
a. Fields with specified list of values must have one of those values or space.  
b. Alphanumeric type fields without specified list of values may have any value as described in the first 
note above. 
c. Numeric type fields without specified list of values must be numeric or space.  
d. Fields with other requirements must follow these requirements or may be space.  
• All dates are in MMDDCCYY format. (March 15, 2010, for example, would be represented as 03152010)  

---

## Page 7

529 Aggregation Record Layouts 
529 Aggregation Header (B/F/G10) 7 
529 AGGREGATION HEADER (B/F/G10) 
Required 
Input from Firm/Fund OR Fund Aggregator to [[NSCC]] 
Output from [[NSCC]] to Fund Aggregator OR Firm/Fund 
529 Aggregation Header (B/F/G10) 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
B/F/G 
System Code 1 1 1 A/N B = Firm 
F = Fund 
G = Fund Aggregator 
Code that identifies the [[intermediary]] 
submitting records (Firm, Fund or 
Aggregator) 
R 01 
Record Type 2 3 2 A/N 10 = 529 Aggregation Header R 02 
Program State Code 4 5 2 A/N Alpha abbreviation identifying the 529 
state. 
State codes are available on [[DTCC]]’s 
Learning site at 
https://dtcclearning.com/documents/m
utual-fund-services/cross-product-
documentation-infomation/2239-state-
codes/file.html 
R A1 
Submitting [[participant]] 
Number  
6 9 4 A/N 4-Digit [[NSCC]] [[participant]] Number of 
[[intermediary]] submitting file 
Must be valid [[NSCC]] [[participant]] 
Number. 
R 03/04/M7 
Receiving [[participant]] 
Number  
10 13 4 A/N 4-Digit [[NSCC]] [[participant]] Number of 
[[intermediary]] receiving file 
Must be valid [[NSCC]] [[participant]] 
Number 
R M7/M7/03 
Current System Date 14 21 8 A/N  MMDDCCYY R K2 
Filler 22 473 452 A/N Space R  
[[NSCC]] Reject Indicator 474 474 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code 1 475 476 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 8

529 Aggregation Record Layouts 
529 Aggregation Header (B/F/G10) 8 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
B/F/G 
[[NSCC]] Reject Code 2 477 478 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 479 480 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 9

529 Aggregation Record Layouts 
529 Aggregation Account Level Detail (B/F11) 9 
529 AGGREGATION ACCOUNT LEVEL DETAIL (B/F11) 
Required 
Input from Firm/Fund to [[NSCC]] 
Output from [[NSCC]] to Fund Aggregator (if accepted), OR to Firm/Fund (if rejected) 
529 Aggregation Account Level Detail (B/F11) 
Field Name  Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N B = Firm 
F = Fund 
Code that identifies the [[intermediary]] submitting 
records (Firm or Fund) 
R 
Record Type 2 3 2 A/N 11 = 529 Aggregation Account Level Detail R 
Program State Code 4 5 2 A/N Alpha abbreviation identifying the 529 state. 
State codes are available on [[DTCC]]’s Learning 
site at https://dtcclearning.com/documents/mutual-
fund-services/cross-product-documentation-
infomation/2239-state-codes/file.html 
R 
Account Number OR 
[[Broker]]/Dealer [[ID]]  
6 25 20 A/N A/C Number Assigned by each Manager OR 
[[Broker]]/Dealer [[ID]] (BIN #) 
R 
Account Owner SSN/TIN 26 34 9 A/N Social Security Number or Tax Identification 
Number of the [[Registered Owner]] of account 
R 
Account Owner Name 35 69 35 A/N Name of [[Registered Owner]] of the account R 
Beneficiary SSN/TIN  70 78 9 A/N Social Security Number or Tax Identification 
Number of the registered beneficiary of account 
R 
Beneficiary Name 79 113 35 A/N Name of registered beneficiary on the account R 
529 Plan Type 114 114 1 A/N There are 2 types of College 529 Plans (Savings 
and Prepaid). This field identifies which type was 
established 
S= Savings 
P = Prepaid 
R 
Market Value Date 115 122 8 A/N MMDDCCYY 
Date of previous business day (Super Sheet Date) 
R 
Market Value  123 138 16 N 99,999,999,999,999.99 
Firm sends Account’s Market Value for transaction 
date, using transaction date closing NAV x closing 
share balance (e.g.: including that day’s 
transaction values in the calculation). The purpose 
of the field is to inform the Aggregator of the 
market value after current day transactions.  
R 

---

## Page 10

529 Aggregation Record Layouts 
529 Aggregation Account Level Detail (B/F11) 10 
Field Name  Start End Len Type Description  Opt/ 
Req 
Prior Year Ending Market 
Value  
139 154 16 N 99,999,999,999,999.99 
Ending market value as of the previous year’s 
close of business 12/31. 
O 
Filler 155 155 1 A/N Space R 
Firm’s Pre-transaction 
Market Value 
156 171 16 N 99,999,999,999,999.99 
Firm sends Account’s Market Value for transaction 
date, using transaction date closing NAV x 
opening share balance (e.g.: not including that 
day’s transaction values in the calculation). The 
purpose of the field is to inform the Aggregator of 
the market value prior to current day transactions.  
O 
Filler 172 187 16 A/N Space R 
Transaction Reversal 
Indicator 
188 188 1 A/N 0 or Blank = No 
1 = Yes 
Identifies if transaction was reversed. 
O 
LTD ‘NET’ Contributions 
Amount 
189 204 16 N 99,999,999,999,999.99 
The netted Grand Total Basis Portion of all 
activity. 
(basis purchases-basis liquidations) made to an 
account since inception (including current day 
activity) 
Required if either the LTD Contributions ONLY 
Amount or LTD Withdrawals ONLY Amount fields 
are NOT populated. (see following 2 fields) 
OC 
LTD Contributions ONLY 
Amount 
205 220 16 N 99,999,999,999,999.99 
Grand Total Basis Portion of all purchases since 
inception of account (including current day 
activity) 
Required if LTD ‘NET’ Contributions Amount is 
NOT Available 
OC 
LTD Withdrawals ONLY 
Amount 
221 236 16 N 99,999,999,999,999.99 
Grand Total Basis Portion of all liquidations since 
inception of account (including current day 
activity) 
Required if LTD ‘NET’ Contributions Amount is 
NOT Available. 
OC Current Year Contribution 
Amount  
237 252 16 N 99,999,999,999,999.99 
YTD Contribution Amount at the Beneficiary Only 
level 
O 
Current Contribution 
(Purchase) Amount  
253 268 16 N 99,999,999,999,999.99 
Dollar Value of Current Contribution (purchase 
only). 
O 

---

## Page 11

529 Aggregation Record Layouts 
529 Aggregation Account Level Detail (B/F11) 11 
Field Name  Start End Len Type Description  Opt/ 
Req 
Current Contribution 
(Purchase) Date 
269 276 8 A/N MMDDCCYY 
Trade Date of Current Contribution. 
 
Required if Current Contribution (Purchase) 
Amount is identified. 
OC 
Filler 277 292 16 A/N Space R 
Current Distribution 
(Redemption) Amount  
293 308 16 N 99,999,999,999,999.99 
Dollar Value of Current Distribution (redemption 
only). 
O 
Current Distribution 
(Redemption) Date 
309 316 8 A/N MMDDCCYY 
Trade Date of Current Distribution. 
 
Required if Current Distribution (Redemption) 
Amount is identified. 
OC 
Negative Earnings 317 332 16 N 99,999,999,999,999.99 
Redemption on an entire position resulted in 
negative earnings. This is at the 
Owner/Beneficiary level. 
O 
Investment Election 
Rebalance Date 1 
333 340 8 A/N MMDDCCYY 
Trade Date of first account investment election 
rebalance change. 
Multiple trades on same day are counted as one). 
O 
Investment Election 
Rebalance Date 2 
341 348 8 A/N MMDDCCYY 
Trade Date of second account investment election 
rebalance change. 
Multiple trades on same day are counted as one). 
O 
Investment Election 
Rebalance Date 3 
349 356 8 A/N MMDDCCYY 
Trade Date of third account investment election 
rebalance change. 
Multiple trades on same day are counted as one). 
O 
Investment Election 
Rebalance Date 4 
357 364 8 A/N MMDDCCYY 
Trade Date of fourth account investment election 
rebalance change. 
Multiple trades on same day are counted as one). 
O 
Investment Election 
Rebalance Date 5 
365 372 8 A/N MMDDCCYY 
Trade Date of fifth account investment election 
rebalance change. 
Multiple trades on same day are counted as one). 
O 

---

## Page 12

529 Aggregation Record Layouts 
529 Aggregation Account Level Detail (B/F11) 12 
Field Name  Start End Len Type Description  Opt/ 
Req 
Investment Election 
Rebalance Date 6 
373 380 8 A/N MMDDCCYY 
Trade Date of sixth account investment election 
rebalance change. 
Multiple trades on same day are counted as one). 
O 
Investment Election 
Rebalance Date 7 
381 388 8 A/N MMDDCCYY 
Trade Date of seventh account investment 
election rebalance change. 
Multiple trades on same day are counted as one). 
O 
Investment Election 
Rebalance Date 8 
389 396 8 A/N MMDDCCYY 
Trade Date of eighth account investment election 
rebalance change. 
Multiple trades on same day are counted as one). 
O 
Investment Election 
Rebalance Reversal 
Indicator 
397 397 1 A/N 0 or Blank = No 
1 = Yes 
This field should be populated with value of 1 
(yes) if reversal activity occurs on a previous 
investment election rebalance transaction. If no 
rebalance reversal occurred, enter zero or leave 
blank. 
O 
Investment Election 
Rebalance Reversal Date 
398 405 8 A/N MMDDCCYY 
Trade Date of most recent account investment 
election rebalance change. 
Required if Investment Election Rebalance 
Reversal Indicator is identified. 
OC 
Account Owner SSN/TIN 
Indicator 
406 406 1 A/N 0 = Tax [[ID]] Number 
1 = Social Security Number 
Identifies if the number submitted in the ‘Account 
Owner SSN/TIN’ field is a Social Security or Tax 
Identification Number  
R Beneficiary SSN/TIN 
Indicator 
407 407 1 A/N 0 = Tax [[ID]] Number 
1 = Social Security Number 
Identifies if the number submitted in the 
‘Beneficiary SSN/TIN’ field is a Social Security or 
Tax Identification Number  
R 

---

## Page 13

529 Aggregation Record Layouts 
529 Aggregation Account Level Detail (B/F11) 13 
Field Name  Start End Len Type Description  Opt/ 
Req 
UGMA/UTMA Indicator 408 408 1 A/N 0 = Other 
1 = UGMA/UTMA 
 
Identifies if the account type is an UGMA (Uniform 
Gift to Minors Act) or UTMA (Uniform Transfer to 
Minors Act) 
Or 
Other type of account 
R 
Surviving Principal 409 424 16 N Used to report the amount of principal to be 
adjusted to surviving accounts 
 
99,999,999,999,999.99 
 
Best Practice for B/F11 Records: 
Firms/Funds will enter the dollar amount of 
principal to be adjusted to surviving accounts. 
O 
Surviving Principal 
Debit/Credit Indicator 
425 425 1 A/N Indicates if dollars reported in Surviving Principal 
field should be debited or credited to surviving 
account(s). 
1 = Debit 
2 = Credit 
 
Required if Surviving Principal field is populated. 
OC 
Originating/ Underlying 
Firm Number 
 
426 429 4 A/N Originating Firm Number. 
 
(The underlying firm’s [[NSCC]] [[ID]] number, for firms 
transacting through an MF Agent). 
 
If provided, must be a valid [[NSCC]] [[participant]] 
Number. If not a valid [[NSCC]] [[participant]] Number, 
the transaction will be rejected utilizing reject code 
‘U5’. 
O 
Filler 430 473 44 A/N Space R 
[[NSCC]] Reject Indicator 474 474 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
R 
[[NSCC]] Reject Code 1 
 
475 476 2 A/N Input: Space 
Output: Reject code or space 
R 
[[NSCC]] Reject Code 2 
 
477 478 2 A/N Input: Space 
Output: Reject code or space 
R 

---

## Page 14

529 Aggregation Record Layouts 
529 Aggregation Account Level Detail (B/F11) 14 
Field Name  Start End Len Type Description  Opt/ 
Req 
[[NSCC]] Reject Code 3 479 480 2 A/N Input: Space 
Output: Reject code or space 
R 

---

## Page 15

529 Aggregation Record Layouts 
529 Aggregated Detail (G12) 15 
529 AGGREGATED DETAIL (G12) 
Required 
Input from Fund Aggregator to [[NSCC]] 
Output from [[NSCC]] to Firm/Fund (if accepted), or Fund Aggregator (if rejected) 
529 Aggregated Detail (G12) 
Field Name  Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N Code that identifies the [[intermediary]] 
submitting records 
G = Fund Aggregator  
R 
Record Type 2 3 2 A/N 12 = 529 Aggregated Detail R 
Program State Code 4 5 2 A/N Alpha abbreviation identifying the 529 state. 
State codes are available on [[DTCC]]’s Learning 
site at 
https://dtcclearning.com/documents/mutual-
fund-services/cross-product-documentation-
infomation/2239-state-codes/file.html 
R Account Number OR 
[[Broker]]/Dealer [[ID]]  
6 25 20 A/N 
Identifies the account number OR [[Broker]]/Dealer 
[[ID]] (BIN#) of the [[intermediary]] receiving 
Aggregated (G12) file. It does not name any 
participants with ‘matched’ data. 
R 
Account Owner SSN/TIN 26 34 9 A/N Social Security Number or Tax Identification 
Number of the [[Registered Owner]] of account 
R 
Account Owner Name 35 69 35 A/N Name of [[Registered Owner]] of the account. R 
Beneficiary SSN/TIN 70 78 9 A/N Social Security Number or Tax Identification 
Number of the registered beneficiary of account 
R 
Beneficiary Name 79 113 35 A/N Name of registered beneficiary on the account R 
Filler 114 114 1 A/N Space R 
Market Value Date 115 122 8 A/N MMDDCCYY 
Date of previous business day (Super Sheet 
Date) 
R 
Market Value  123 138 16 N 99,999,999,999,999.99 
Aggregated Current Market Value at the 
Owner/Beneficiary Level for all holdings in the 
State Plan, across providers if applicable. 
R 
Prior Year Ending Market 
Value  
139 154 16 N 99,999,999,999,999.99 
Aggregated total of previous year’s ending 
market value at the Beneficiary Only Level. 
O 

---

## Page 16

529 Aggregation Record Layouts 
529 Aggregated Detail (G12) 16 
Field Name  Start End Len Type Description  Opt/ 
Req 
Plan Cap Met or 
Exceeded Limit Reached 
155 155 1 A/N Space = No 
Y = Yes 
Indicates whether the aggregated value of 
accounts at the Beneficiary Only level for all 
holdings within a State have met or exceeded 
the State’s limit. 
O Firm’s Pre-transaction 
Market Value 
156 171 16 N 99,999,999,999,999.99 
Firm’s Aggregated Pre-transaction Market 
Value for accounts at Owner/Beneficiary level 
O 
Firm’s Post-transaction 
Market Value 
172 187 16 N 99,999,999,999,999.99 
Firm’s Aggregated Post-transaction Market 
Value for accounts at Owner/Beneficiary level 
O 
Filler 188 188 1 A/N Space R 
LTD ‘NET’ Contributions 
Amount 
189 204 16 N 99,999,999,999,999.99 
Aggregated total of inception-to-Date Basis 
Portion of Net Business at Owner/ Beneficiary 
Level including current day activity. 
(LTD Contributions Basis – Distributions Basis) 
R 
Filler 205 236 32 A/N Space R 
Current Year Contribution 
Amount  
237 252 16 N 99,999,999,999,999.99 
Aggregated total of YTD Contributions at the 
Beneficiary level  
O 
Current Contribution 
(Purchase) Amount  
253 268 16 N 99,999,999,999,999.99 
Grand total (Dollar Value) of Current 
Contributions for ALL participants at the 
Beneficiary Only level 
O 
Current Contribution 
(Purchase) Date 
269 276 8 A/N MMDDCCYY 
Trade Date of Current Contribution(s). 
Required if Current Contribution (Purchase) 
Amount is identified. 
OC 
Principal Portion of 
Distribution 
277 292 16 N 99,999,999,999,999.99 
Aggregator will send back the calculated 
principal amount of a distribution. Value will not 
be aggregated across other accounts. 
O 
Current Distribution 
(Redemption) Amount  
293 308 16 N 99,999,999,999,999.99 
Grand total (Dollar Value) of Current 
Distributions for ALL participants at the account 
level 
O 

---

## Page 17

529 Aggregation Record Layouts 
529 Aggregated Detail (G12) 17 
Field Name  Start End Len Type Description  Opt/ 
Req 
Current Distribution 
(Redemption) Date 
309 316 8 A/N MMDDCCYY 
Trade Date of Current Distribution(s). 
Required if Current Distribution (Redemption) 
Amount is identified 
OC 
Negative Earnings 317 332 16 N 99,999,999,999,999.99 
Redemption on an entire position resulted in 
negative earnings. This is a prorated value 
based on the market value. This will only be 
sent to those participants with remaining value. 
O 
YTD Investment Election 
Rebalance Counter 
333 334 2 N 99 
Count of ALL Investment Election Changes 
made at Intermediaries in current year at 
Owner/Beneficiary level. This record-keeping 
process is performed by the Aggregator. 
 
Required if Investment Election Rebalance Date 
Is populated 
OC 
Grand Total Market Value 335 350 16 N 99,999,999,999,999.99 
Aggregated Market Value for all Positions with 
all Firms/Plan Providers at Beneficiary Only 
Level including current day activity. 
R 
Grand Total LTD 
Contributions Amount 
351 366 16 N 99,999,999,999,999.99 
Aggregated LTD Contributions for all Positions 
with all Firms/Plan Providers at Beneficiary Only 
Level including current day activity. 
R 
Account Owner SSN/TIN 
Indicator 
367 367 1 A/N 0 = Tax [[ID]] Number 
1 = Social Security Number 
Identifies if the number submitted in the 
‘Account Owner SSN/TIN’ field is a Social 
Security or Tax Identification Number  
R Beneficiary SSN/TIN 
Indicator 
368 368 1 A/N 0 = Tax [[ID]] Number 
1 = Social Security Number 
Identifies if the number submitted in the 
‘Beneficiary SSN/TIN’ field is a Social Security 
or Tax Identification Number  
R 
UGMA/UTMA Indicator 369 369 1 A/N 0 = Other 
1 = UGMA/UTMA  
 
Identifies if the account type is an UGMA 
(Uniform Gift to Minors Act) or UTMA (Uniform 
Transfer to Minors Act) 
Or 
Other type of account 
R 

---

## Page 18

529 Aggregation Record Layouts 
529 Aggregated Detail (G12) 18 
Field Name  Start End Len Type Description  Opt/ 
Req 
Surviving Principal 370 385 16 N Used to report the amount of principal to be 
adjusted to surviving accounts 
 
99,999,999,999,999.99 
 
Best Practice for G12 Records: 
Aggregator will calculate and enter dollar 
amount of principal to be adjusted to surviving 
accounts  
O Surviving Principal 
Debit/Credit Indicator 
386 386 1 A/N Indicates if dollars reported in Surviving 
Principal field should be debited or credited to 
surviving account(s) 
1 = Debit 
2 = Credit 
 
Required if Surviving Principal field is populated 
OC 
Originating/ Underlying 
Firm Number 
 
387 390 4 A/N Originating Firm Number. 
 
(The underlying firm’s [[NSCC]] [[ID]] number, for 
firms transacting through an MF Agent). 
 
If provided, must be a valid [[NSCC]] [[participant]] 
Number. If not a valid [[NSCC]] [[participant]] 
Number, the transaction will be rejected utilizing 
reject code ‘U5’. 
O 
Filler 391 473 83 A/N Space R 
[[NSCC]] Reject Indicator 
 
474 474 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
R 
[[NSCC]] Reject Code 1 
 
475 476 2 A/N Input: Space 
Output: Reject code or space 
R 
[[NSCC]] Reject Code 2 
 
477 478 2 A/N Input: Space 
Output: Reject code or space 
R 
[[NSCC]] Reject Code 3 
 
479 480 2 A/N Input: Space 
Output: Reject code or space 
R 

---

## Page 19

529 Aggregation Record Layouts 
529 Aggregation Trailer (B/F/G14) 19 
529 AGGREGATION TRAILER (B/F/G14) 
Required 
Input from Firm/Fund OR Fund Aggregator to [[NSCC]] 
Output from [[NSCC]] to Fund Aggregator OR Firm/Fund 
529 Aggregation Trailer (B/F/G14) 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
B/F/G 
System Code 1 1 1 A/N B = Firm 
F = Fund 
G = Fund Aggregator 
Code that identifies the 
[[intermediary]] submitting records 
(Firm, Fund or Aggregator) 
R 01 
Record Type 2 3 2 A/N 14 = 529 Aggregation Trailer R 02 
Program State Code 4 5 2 A/N Alpha abbreviation identifying the 
529 state. 
State codes are available on 
[[DTCC]]’s Learning site at 
https://dtcclearning.com/documents/
mutual-fund-services/cross-product-
documentation-infomation/2239-
state-codes/file.html 
R A1 
Submitting [[participant]] 
Number  
6 9 4 A/N 4-Digit [[NSCC]] [[participant]] Number of 
[[intermediary]] submitting file 
Must be valid [[NSCC]] [[participant]] 
Number. [[NSCC]] will check this 
number matches the Submitting 
[[participant]] Number on Header.  
R 03/04/M7 
Receiving [[participant]] 
Number  
10 13 4 A/N 4-Digit [[NSCC]] [[participant]] Number of 
[[intermediary]] receiving file 
Must be valid [[NSCC]] [[participant]] 
Number 
R M7/M7/03 
Total Number of Records 14 22 9 N 999,999,999 
Total Number of records in file 
(including header and trailer) 
O  
Filler 23 473 451 A/N Space R  
[[NSCC]] Reject Indicator 474 474 1 A/N Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
R  

---

## Page 20

529 Aggregation Record Layouts 
529 Aggregation Trailer (B/F/G14) 20 
Field Name  Start End Len Type Description  Opt/ 
Req 
Reject 
Code 
B/F/G 
[[NSCC]] Reject Code 1 475 476 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 2 477 478 2 A/N Input: Space 
Output: Reject code or space 
R  
[[NSCC]] Reject Code 3 479 480 2 A/N Input: Space 
Output: Reject code or space 
R  

---

## Page 21

529 Aggregation Record Layouts 
529 Aggregation Grand Total Trailer (B/F/G16) 21 
529 AGGREGATION GRAND TOTAL TRAILER (B/F/G16) 
Optional Input record from Firm/Fund OR Fund Aggregator to [[NSCC]] 
Required Output record from [[NSCC]] to Firm/Fund OR Fund Aggregator 
This record is used to recap all 529 Aggregation records including headers and trailers for a [[participant]]’s entire 
transmission. 
529 Aggregation Grand Total Trailer (B/F/G16) 
Field Name  Start End Len Type Description  Opt/ 
Req 
System Code 1 1 1 A/N B = Firm 
F = Fund 
G = Fund Aggregator 
Code that identifies the [[intermediary]] 
submitting records (Firm, Fund or 
Aggregator) 
R 
Record Type 2 3 2 A/N 16 = 529 Aggregation Grand Total Trailer R 
Filler 4 5 2 A/N Space R 
Submitting [[participant]] 
Number / Recipient Number
 
6 9 4 A/N 4-Digit [[NSCC]] [[participant]] Number identifying 
either the Submitting or Receiving 
[[intermediary]]. Information is dependent on 
originating source. 
Must be valid [[NSCC]] [[participant]] Number. 
 
This record is optional for intermediaries; but 
required for [[NSCC]] 
R 
Total Number of Records 10 18 9 N 999,999,999 
Number of records included in the file 
(including Headers and Trailers) 
R 
Filler 19 480 462 A/N Space R 

---

## Page 22

529 Aggregation Record Layouts 
Input Record Layout 22 
INPUT RECORD LAYOUT 
Datatrak Header 
Required 
Input from Firm/Fund OR Fund Aggregator to [[NSCC]] 
This is the first record in any 529 Aggregation file submitted through DATATRAK.  
Datatrak Header  
Field Name  Start End Len Type Description  Opt/ 
Req 
Literal 1 5 5 A/N Value 'HDR.S' R 
DATATRAK SYSID 6 10 5 A/N Value ‘26945’ (OMNI/SERV 529 AGGREGATION) 
     or ‘26946’ (OMNI/SERV 529 AGGREGATED) 
R 
Literal 11 16 6 A/N Value '.E00.C' R 
Originator 17 20 4 A/N  R 
Literal 21 22 2 A/N Value '.S' R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N MMDDCCYY R 
File Description 35 59 25 A/N Value ‘OMNI/SERV 529 AGGREGATION’ 
or ‘OMNI/SERV 529 AGGREGATED ’ 
R 
Multi-batch Last 
Batch Indicator 
60 60 1 A/N N = Not last batch 
Y = Last batch 
R 
Multi-batch Batch 
Counter 
61 63 3 N  R 
Filler 64 480 417 A/N Space R 
 
 
  

---

## Page 23

529 Aggregation Record Layouts 
Input Record Layout 23 
Datatrak Trailer 
Required 
Input from Firm/Fund OR Fund Aggregator to [[NSCC]] 
This is the last record in any 529 Aggregation file submitted through Datatrak.  
Datatrak Trailer 
Field Name  Start End Len Type Description  Opt/ 
Req 
Literal 1 5 5 A/N Value ‘END.S’ R 
DATATRAK SYSID 6 10 5 A/N Value ‘26945’ (OMNI/SERV 529 AGGREGATION) 
Or ‘26946’ (OMNI/SERV 529 AGGREGATED) 
R 
Literal 11 16 6 A/N Value ‘.E00.C’ R 
Originator [[ID]] 17 20 4 A/N  R 
Literal 21 22 2 A/N Value ‘.S’ R 
Sub Originator [[ID]] 23 26 4 A/N  R 
Total Records 27 33 7 A/N 9,999,999 
Total # of records in the file excluding DATATRAK 
header and trailer 
R 
Filler 34 480 447 A/N Space R 

---

## Page 24

529 Aggregation Record Layouts 
Output Record Layout 24 
OUTPUT RECORD LAYOUT 
[[NSCC]] Output Header (N00) 
Required 
Output from [[NSCC]] to FUND Aggregator and FIRM/FUND 
[[NSCC]] Output Header (N00) 
Field Name  Start End Len Type Description  
Originator Type 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 5 2 A/N 01 
Recipient Number 6 9 4 A/N  
Literal 10 20 11 A/N ‘11111111111’ 
Transmission Date 21 28 8 A/N MMDDCCYY 
AutoRoute file [[ID]] 29 36 8 A/N Value ‘02101945’ 
Value ‘02101946’  
Literal 37 66 30 A/N Value ‘OMNI/SERV 529 AGGREGATION FILE’ 
Or ‘OMNI/SERV 529 AGGREGATED FILE’ 
Filler 67 480 414 A/N Space 
 
 

---

## Page 25

529 Aggregation Record Layouts 
APPENDIX – Summary of Changes 25 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  

---

## Page 26

529 Aggregation Record Layouts 
Summary of Changes – effective Q4, 2020 26 
SUMMARY OF CHANGES – EFFECTIVE Q4, 2020 
New Fields Added 
New Field Name Location Description 
Originating/ Underlying 
Firm Number 
Detail (B/F11) start 426, end 429, 
length 4, A/N, Optional 
 
Detail (G12) start 387, end 390, 
length 4, A/N, Optional 
Originating Firm Number. 
 
(The underlying firm’s [[NSCC]] [[ID]] number, for firms 
transacting through an MF Agent). 
 
If provided, must be a valid [[NSCC]] [[participant]] Number. 
If not a valid [[NSCC]] [[participant]] Number, the transaction 
will be rejected utilizing reject code ‘U5’. 
[[NSCC]] Reject Indicator Detail (B/F11) start 474, end 474, 
length 1, A/N, Required 
 
Detail (G12) start 474, end 474, 
length 1, A/N, Required 
Input: Space 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
[[NSCC]] Reject Code 1 Detail (B/F11) start 475, end 476, 
length 2, A/N, Required 
 
Detail (G12) start 475, end 476, 
length 2, A/N, Required 
Input: Space 
Output: Reject code or space 
[[NSCC]] Reject Code 2 Detail (B/F11) start 477, end 478, 
length 2, A/N, Required 
 
Detail (G12) start 477, end 478, 
length 2, A/N, Required 
Input: Space 
Output: Reject code or space 
[[NSCC]] Reject Code 3 Detail (B/F11) start 479, end 480, 
length 2, A/N, Required 
 
Detail (G12) start 479, end 480, 
length 2, A/N, Required 
Input: Space 
Output: Reject code or space 
 
Reject Code 
The following existing MF Networking reject code will be utilized to reject transactions that fail new field 
validation:  
Reject Code Description 
U5 Originating/Underlying Firm Number is invalid  

---

## Page 27

529 Aggregation Record Layouts 
Summary of Changes – effective Q1, 2019 27 
SUMMARY OF CHANGES – EFFECTIVE Q1, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 28

529 Aggregation Record Layouts 
Summary of Changes – effective Q3, 2018 28 
SUMMARY OF CHANGES – EFFECTIVE Q3, 2018 
Field Description Modifications 
A number of Field Descriptions were updated to align with the language adopted during the review of best practices. 
These descriptions were incorporated into the record layouts and removed from best practices. 

---

## Page 29

529 Aggregation Record Layouts 
Summary of changes – effective Q2, 2015 29 
SUMMARY OF CHANGES – EFFECTIVE Q2, 2015 
Existing Fields Modified 
Modified Field Name Location Description 
Account Owner 
SSN/TIN 
Detail (B/F11) start 26, end 34, length 9, A/N, R 
Detail (G12) start 26, end 34, length 9, A/N, R 
SSN/TIN of Account Owner 
Beneficiary SSN/TIN Detail (B/F11) start 70, end 78, length 9, A/N, R 
Detail (G12) start 70, end 78, length 9, A/N, R 
SSN/TIN of Beneficiary 
 
New Fields Added 
New Field Name Location Description 
Account Owner 
SSN/TIN Indicator 
Detail (B/F11) start 406, end 406, length 1, A/N, R 
 
Detail (G12) start 367, end 367, length 1, A/N, R 
Account Owner SSN/TIN Indicator 
0 = Tax [[ID]] Number 
1 = Social Security Number 
Beneficiary 
SSN/TIN Indicator 
Detail (B/F11) start 407, end 407, length 1, A/N, R 
 
Detail (G12) start 368, end 368, length 1, A/N, R 
Beneficiary SSN/TIN Indicator 
0 = Tax [[ID]] Number 
1 = Social Security Number 
UGMA/UTMA 
Indicator 
Detail (B/F11) start 408, end 408, length 1, A/N, R 
 
Detail (G12) start 369, end 369, length 1, A/N, R 
UGMA/UTMA Indicator 
Identifies if the account type is an 
UGMA (Uniform Gift to Minors 
Act)/UTMA (Uniform Transfer to 
Minors Act) 
Or 
Other type of account. 
 
0 = Other 
1 = UGMA/UTMA 
Surviving Principal Detail (B/F11) start 409, end 424, length 16, N, O 
 
Detail (G12) start 370, end 385, length 16, N, O 
Surviving Principal 
Used to report the amount of principal 
to be adjusted to surviving accounts 
99,999,999,999,999.99 
 
Best Practice: 
B/F11 - Firms/Funds will report any 
surviving principal. 
G12 – Aggregator will calculate and 
report the amount to be debited or 
credited to each surviving account. 

---

## Page 30

529 Aggregation Record Layouts 
Summary of changes – effective Q2, 2015 30 
New Field Name Location Description 
Surviving Principal 
Debit/Credit 
Indicator 
Detail (B/F11) start 425, end 425, length 1, A/N, OC 
 
Detail (G12) start 386, end 386, length 1, A/N, OC 
Indicates if dollars reported in 
Surviving Principal field should be 
debited or credited to surviving 
account (s) 
1 = Debit 
2 = Credit 
Required if Surviving Principal field is 
populated. 
 
 
 

---

## Page 31

© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: October 13, 2023 
Publication Code: MFS332 
Service: Networking - Omni/SERV 
Title: 529 Aggregation Record Layouts  
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 