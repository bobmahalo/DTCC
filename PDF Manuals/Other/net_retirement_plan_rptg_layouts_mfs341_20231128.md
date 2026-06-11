---
title: "Networking - Retirement Plan Reporting Record Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_retirement_plan_rptg_layouts_mfs341_20231128.pdf"
pages: 32
size: "477.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Networking - Retirement Plan Reporting Record Layouts

**Original File:** [net_retirement_plan_rptg_layouts_mfs341_20231128.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_retirement_plan_rptg_layouts_mfs341_20231128.pdf)  
**Category:** Other  
**Total Pages:** 32  
**File Size:** 477.7 KB  

---

## Page 1

 
 
 
Networking 
RETIREMENT PLAN REPORTING RECORD 
LAYOUTS 
NOVEMBER 28, 2023 
 

---

## Page 2

 
 
TABLE OF CONTENTS 
History of Important Notices ............................................................................................................................... 4 
File Overview ........................................................................................................................................................ 5 
Record Sequence Order ..................................................................................................................................... 5 
Record Layouts .................................................................................................................................................... 7 
MF Retirement Plan Reporting Header Record ................................................................................................. 8 
Retirement Plan Header Record (B/F/T47 Sequence 1) .................................................................................... 8 
Retirement Plan Header Record (B/F/T47 Sequence 2) ..................................................................................10 
Retirement Plan Header Record (B/F/T47 Sequence 3) ..................................................................................13 
Retirement Plan Specific Information Header Record (B/F/T47 Sequence 4)  .................................................15 
MF Retirement Plan Reporting Detail Record ................................................................................................. 17 
Retirement Plan Detail Record (B/F/T 48) ........................................................................................................17 
MF Retirement Plan Reporting Trailer Record ................................................................................................ 20 
Retirement Plan Trailer Record (B/F/T49) ........................................................................................................20 
MF Retirement Plan Reporting DataTrak Records .......................................................................................... 22 
Datatrak Header Record ...................................................................................................................................22 
Datatrak Trailer Record ....................................................................................................................................23 
MF Retirement Plan Reporting Output Records ............................................................................................. 24 
Service Output Header Record (N00)...............................................................................................................24 
Input Acknowledgement Record (NRA) ............................................................................................................25 
Retirement Plan Grand Total Trailer Record (NRG) .........................................................................................26 
APPENDIX – Summary of Changes .................................................................................................................. 27 
Summary of changes – Effective March 25, 2019 ........................................................................................... 28 
Reject Codes ....................................................................................................................................................28 
Summary of changes – Effective February 27, 2017 ...................................................................................... 29 
Add New Fields .................................................................................................................................................29 
Reject Codes ....................................................................................................................................................29 
Summary of changes – Effective July 27, 2015 .............................................................................................. 30 
Change to Data Field Population Requirement ................................................................................................30 

---

## Page 3

 
 
Add New Values to Existing Field .....................................................................................................................30 
Summary of changes – November 18, 2014 .................................................................................................... 31 
 

---

## Page 4

Retirement Plan Reporting Record Layouts 
History of Important Notices 4 
HISTORY OF IMPORTANT NOTICES 
See the Appendix for the summary of changes. 
Effective Date Important Notice 
November 28, 2023 Record was rebranded and reviewed.  
May 2, 2023 Record was rebranded and reviewed. 
March 25, 2019 Please see: 
a8658 P&S 8233 Dated December 19, 2018 
February 27, 2017 Please see Important Notice: 
a8286 P&S 7861 Dated November 8, 2016 
July 27, 2015 Please see Important Notice: 
a7997 P&S 7572 Dated March 12, 2015 
November 18, 2014 Added the File Overview, Record Sequence Order and Record Layout 
references. See Table of Contents. 
March 18, 2013 Please see Important Notices: 
a7471 P&S 7041 Dated August 16, 2012 and  
a7576 P&S 7146 Dated January 30, 2013 

---

## Page 5

Retirement Plan Reporting Record Layouts 
File Overview 5 
FILE OVERVIEW 
1. These records are a fixed 300-byte. 
2. Files sent to [[NSCC]] are by Plan. However, if there are multiple recipients (firms) that are to receive 
information about a plan, separate files are to be created for each firm (Clearing/Settling Firm Number 
(Recipient Number) 
3. Participants transmitting files to [[NSCC]] (DataTrak) must also program to receive files from [[NSCC]] 
(AutoRoute). If [[NSCC]] rejects any records or files occurs, [[NSCC]] communicates this information through 
AutoRoute records. 
4. Firms and TPA’s that send files to [[NSCC]] will also need to program to receive the Acknowledgement 
Record (NRA) sent by [[NSCC]]. 
5. Multiple Detail records (B/T48) can be sent in one file. Detail records sent for a plan should only pertain to 
that plan and the firm listed on the records. 
Record Sequence Order 
Files sent to [[NSCC]] will have the following record order: 
HDR.S DataTrak Header 
B/T 47 Header Seq 1 
B/T 47 Header Seq 2 
B/T 47 Header Seq 3 (Optional) 
B/T 47 Header Seq 4 (Optional/Conditional) 
B/T 48 Detail Record 
B/T 48 Detail Record (if applicable) 
B/T 48 Detail Record (if applicable) 
B/T49 Trailer 
END.S DataTrak Trailer 
 
 
Participants that submitted RPR files to [[NSCC]] will need to program to receive the NRA record:  
1 Trans AutoRoute Header (Optional) 
N00 Service Output Header 
NRA Input /acknowledgement 
 
Retirement Plan Reporting Files sent from [[NSCC]] will have the following record order: 
1 Trans AutoRoute Header (Optional) 
N00 Service Output Header (Application Header) 
B/T 47 Header Seq 1 
B/T 47 Header Seq 2 
B/T 47 Header Seq 3 (Optional) 
B/T 47 Header Seq 4 (Optional/Conditional) 
B/T 48 Detail Record 
B/T 48 Detail Record (if sent to [[NSCC]]) 
B/T 48 Detail Record (if sent to [[NSCC]]) 
B/T49 Trailer 
NRG Grand Total Trailer 
 
Please note that participants that create and submit files to [[NSCC]] with DataTrak Header/Trailer records must 
also program to receive files sent from [[NSCC]] with AutoRoute Header. If [[NSCC]] rejects any data on inbound 
(DataTrak) files, this information will be communicated back via outbound AutoRoute files.  

---

## Page 6

Retirement Plan Reporting Record Layouts 
File Overview 6 
Record Sequence Structure Examples Sent TO [[NSCC]] 
Example 1: The submitter will create files for all the Security Issue [[ID]]’s pertaining to one Plan. If there are 
multiple dealers, the file sent will be broken down per [[Broker]]/Dealer (recipient of file). The example below 
shows the structure of a file if TPA 1111 is sending [[Broker]] Dealers AAAA and BBBB for Plan [[ID]] 1234567. 
HDR.S DataTrak Header  
Header Record 47 
-Plan [[ID]] 1234567 
-Clearing/Settling Firm Number AAAA 
-TPA Number 1111 
Detail Record 48 for this dealer within this plan 
Trailer Record 49 for same parameters as stated in Header 
 
Header Record 47 
-Plan [[ID]] 1234567, 
-Clearing/Settling Firm Number BBBB 
-TPA Number 1111 
Detail Record 48 for this dealer within this plan 
Trailer Record 49 for same parameters as stated in Header 
END.S DataTrak Trailer 
 
All sequences used should be sent in order within its record type. 
 
Example 2: Using a reference above – if [[Broker]]/Dealer BBBB has 3 Security Issue IDs, the record sequence 
order would be: 
 
HDR.S DataTrak Header 
Header Record 47 
-Plan [[ID]] 1234567, 
-Clearing/Settling Firm Number BBBB 
-TPA Number 111 
(3 Detail 48 Records for this dealer within this plan) 
-Security Issue [[ID]] 999999999 
-Security Issue [[ID]] 888888888 
-Security Issue [[ID]] 777777777 
Trailer Record 49 for same parameters as stated in Header 
END.S DataTrak Trailer 

---

## Page 7

Retirement Plan Reporting Record Layouts 
Record Layouts 7 
RECORD LAYOUTS 
The column headings are as follows: 
Field Name The name of the field. 
Start The position in which the field starts. 
End The position in which the field ends. 
Len The length of the field in bytes. 
Type The type of the field: 
A/N = Alphanumeric 
N = Numeric 
Description Field description (format, valid values, conditional requirements, etc.). 
Req/Opt Indicates whether the field is optional or required: 
O = Optional 
R = Required 
OC = Generally optional, but required upon specified conditions 
RC = Generally required, but optional upon specified conditions 
Reject Code The Networking reject code which indicates that this field is invalid. 
 
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

---

## Page 8

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Header Record 8 
MF RETIREMENT PLAN REPORTING HEADER RECORD 
Retirement Plan Header Record (B/F/T47 Sequence 1) 
Required Record 
Input from TPA or Record Keeper (on behalf of TPA) to [[NSCC]] 
Output from [[NSCC]] to Firm 
Retirement Plan Header Record (B/F/T47 sequence 1) 
Sequence 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N B = Firm 
T = TPA 
F = Fund (for future use) 
R 01 
Record Type 2 3 2 A/N 47 R 02 
Sequence Number 4 5 2 A/N 01 R 37 
Plan [[ID]] Number 6 17 12 A/N Unique internal recordkeeping account 
number for the plan 
R U1 
Plan Tax [[ID]] 18 26 9 N Tax [[ID]] or EIN for plan sponsor (Tax [[ID]] 
for the PLAN) 
R Q4 
DOL Plan Code Number 27 29 3 N 3 digit code assigned by Department of 
Labor to the plan 
O Q5 
Clearing/Settling Firm 
Number (Deliverer 
Number) 
30 33 4 A/N [[NSCC]] number of party submitting the 
file 
Required when System Code = B 
OC 
I2/T9 
Executing [[Broker]] (Agent 
for Firm) 
34 37 4 A/N The firm that clears through the 
[[Broker]]/dealer [[NSCC]] [[Member]] 
O  
Clearing/Settling Firm 
Number (Recipient 
Number) 
38 41 4 A/N [[NSCC]] number for recipient of the file R F4 
Filler 42 43 2 A/N Space R  
TPA Number 44 47 4 A/N Required when System Code = T OC G0 
Start Date for Period 48 55 8 A/N Business start date for period 
ddmmccyy 
R N7 
End Date for Period 56 63 8 A/N Business end date for period 
ddmmccyy 
R N8 

---

## Page 9

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Header Record 9 
Sequence 1 
Field Name 
Start End Len Type Description Opt/ 
Req 
Rej 
Code 
Plan [[Fiduciary]] Name 64 93 30 A/N [[Fiduciary]] responsible for the plan 
(A person or an entity named as the 
[[Fiduciary]] in the written plan document 
or through a process described in the 
plan. The named [[Fiduciary]] can be 
identified by office or by name.) 
O NA Plan [[Fiduciary]] Address 
Line #1 
94 128 35 A/N 1st line of Plan [[Fiduciary]]/Sponsor’s 
address 
O NA 
Plan [[Fiduciary]] Address 
Line #2 
129 163 35 A/N 2nd line of Plan [[Fiduciary]]/Sponsor’s 
address 
O  
Plan [[Fiduciary]] City 164 196 33 A/N City name of Plan [[Fiduciary]]/Sponsor’s 
address 
O NA 
Plan [[Fiduciary]] State 197 198 2 A/N 2-byte alpha code of state of Plan 
[[Fiduciary]]/Sponsor’s address 
If provided: must be a valid State Code. 
O Q9 
Plan [[Fiduciary]] Zip 199 209 11 A/N Zip Code 
5-digit Zip Code + 4-digit Zip-Four 
 
+ 2 digits for future postal expansion 
O NA 
Filler 210 291 82 A/N  R  
[[NSCC]] Reject Indicator 292 292 1 N Input: Space 
 
Output: 
0 = Accepted by [[NSCC]]  
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code # 1 293 294 2 A/N Input: Space 
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 2 295 296 2 A/N Input: Space 
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 3 297 298 2 A/N Input: Space 
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 4 299 300 2 A/N Input: Space 
Output: Reject Code or space 
R  
 
 
  

---

## Page 10

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Header Record 10 
Retirement Plan Header Record (B/F/T47 Sequence 2) 
Required Record 
Input from TPA or Record Keeper (on behalf of TPA) to [[NSCC]] 
Output from [[NSCC]] to Firm 
Retirement Plan Header Record (B/F/T47 sequence 2) 
Sequence 2  
Field Name 
Start End Len Type Description Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N B = Firm 
T = TPA 
F = Fund (for future use) 
R 01 
Record Type 2 3 2 A/N 47 R 02 
Sequence Number 4 5 2 A/N 02 R 37 
Underlying Firm Symbol 
(UFS) 
6 9 4 A/N Number that identifies the Underlying 
Firm (Banks/Trusts/Record Keepers/ 
TPA’s) that clear through another entity 
O  
Record Keeper Name 10 39 30 A/N Record Keeper Name that identifies the 
plan 
R R1 
Program Name 40 69 30 A/N Program name created by the Product 
Provider 
R R2 
Product Provider 70 89 20 A/N Entity that created the Program R R3 
Plan Type 90 91 2 A/N 01 = 401K 
02 = Individual K 
03 = 403B 
04 = Profit Sharing 
05 = Money Purchase Plan 
06 = 457 
07 = Deferred Compensation 
08 = Defined Benefit 
09 = Cash Balance 
10 = Taft-Hartley 
11 = Multiple Employer Plans 
R R4 
Plan Status 92 92 1 A/N A = Active 
B = Abandoned 
T = Terminated (if plan is terminated but 
has assets) 
R R5 

---

## Page 11

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Header Record 11 
Sequence 2  
Field Name 
Start End Len Type Description Opt/ 
Req 
Rej 
Code 
Plan Status Date 93 100 8 A/N Required if Plan Status = B 
(Abandoned) or 
T (Terminated) 
ddmmccyy 
OC R6 
Overall Plan Assets 101 116 16 N Total value of the Plan as of end of 
period 
99,999,999,999,999.99 
Zeros are allowed 
R R7 
Number of Security Issue 
[[ID]]’s in the Plan 
117 120 4 N Number of Security Issue [[ID]]’s in the 
plan with a balance > 0 
9,999 
(may include both registered and 
unregistered Security Issue [[ID]]’s) 
R R8 
Total Participants in Plan 121 126 6 N Number of participants in the plan with a 
balance > 0 
999,999 
Zeros are allowed 
R R9 
ERISA Flag 127 127 1 A/N Identify if Plan is ERISA or not 
Y = Yes 
N= No 
U= Unknown 
R S0 
Record Keeper Start Date 128 135 8 A/N Plan Start Date at Record Keeper 
ddmmccyy 
O K2 
Record Keeper End Date 136 143 8 A/N Plan End Date at Record Keeper 
ddmmccyy 
O K2 
Dealer Maint Date 144 151 8 A/N Date of last dealer change at the plan 
level 
ddmmccyy 
O K2 
Rep Maint Date 152 159 8 A/N Date of last representative change at the 
plan level 
ddmmccyy 
O K2 
Branch [[ID]] 160 168 9 A/N Branch number for financial advisor. O  
Rep [[ID]] 169 177 9 A/N Code issued internally by the [[Broker]] 
dealer 
O  
Rep Name 178 192 15 A/N Financial Advisor affiliated with the plan O  

---

## Page 12

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Header Record 12 
Sequence 2  
Field Name 
Start End Len Type Description Opt/ 
Req 
Rej 
Code 
Contribution Amount for 
the Plan 
193 208 16 N Net amount of all purchase 
Contributions at the Plan level 
99,999,999,999,999.99 
 
Zeros are allowed 
R S1 Distribution Amount for 
the Plan 
209 224 16 N Net amount of all distributions at the 
Plan level 
99,999,999,999,999.99 
 
Zeros are allowed 
R S2 Contribution Amount 
Credit/Debit Indicator 
 
 
225 225 1 A/N Blank = Credit 
D = Debit 
 
This indicator specifies if the value 
provided in the “Contribution Amount for 
the Plan” field is positive (Credit) or 
negative (Debit) 
O W8 
Distribution Amount 
Credit/Debit Indicator 
 
 
226 226 1 A/N Blank = Debit C = Credit 
 
This indicator specifies if the value 
provided in the “Distribution Amount for 
the Plan” field is positive (Debit) or 
negative (Credit) 
O W9 
Filler 227 300 74 A/N Space R  
 
 
  

---

## Page 13

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Header Record 13 
Retirement Plan Header Record (B/F/T47 Sequence 3) 
Optional Record 
Input from TPA or Record Keeper (on behalf of TPA) to [[NSCC]] 
Output from [[NSCC]] to Firm 
Retirement Plan Header Record (B/F/T47 sequence 3) 
Sequence 3 
Field Name   
Start End Len Type Description Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N B = Firm  
T = TPA 
F = Fund (for future use) 
R 01 
Record Type 2 3 2 A/N 47 R 02 
Sequence Number 4 5 2 A/N 03 R 37 
Plan Sponsor Name 6 35 30 A/N Name of Plan Sponsor 
(A specific entity, generally a company 
or employer that establishes a 
retirement plan (e.g., 401(k) or 403(b)) 
for the benefit of the employees.) 
O  
Plan Sponsor Address 
Line #1 
36 70 35 A/N 1st line of Sponsor’s address 
Required if Plan Sponsor Name is 
populated 
OC S3 
Plan Sponsor Address 
Line #2 
71 105 35 A/N 2nd line of Sponsor’s address O  
Plan Sponsor City 106 138 33 A/N Name of city 
Required if Plan Sponsor Name is 
populated 
OC S4 
Plan Sponsor State 139 140 2 A/N 2-byte alpha code of state 
Required if Plan Sponsor Name is 
populated 
OC S5 
Plan Sponsor Zip 141 151 11 A/N Zip Code 
5-digit Zip Code + 4-digit Zip-Four 
 
+ 2 digits for future postal expansion 
 
Required if Plan Sponsor Name is 
populated 
OC S6 
Email Address of Plan 
Sponsor 
152 211 60 A/N  O  
Email Address of Plan 
[[Fiduciary]] 
212 271 60 A/N  O  

---

## Page 14

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Header Record 14 
Sequence 3 
Field Name   
Start End Len Type Description Opt/ 
Req 
Rej 
Code 
Filler 272 300 29 A/N Space R  
 
 
  

---

## Page 15

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Header Record 15 
Retirement Plan Specific Information Header Record (B/F/T47 
Sequence 4) 
Optional/Conditional Record 
Input from TPA or Record Keeper (on behalf of TPA) to [[NSCC]] 
Output from [[NSCC]] to Firm 
This record is required if 
• Plan Type = 11 (Multiple Employer Plan) in B/F/T47 Sequence 2 
Retirement Plan Specific Information Header Record (B/F/T47 sequence 4) 
Sequence 4        
Field Name 
Start End Len Type Description Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N B = Firm  
T = TPA 
F = Fund (for future use) 
R 01 
Record Type 2 3 2 A/N 47 R 02 
Sequence Number 4 5 2 A/N 04 R 37 
Secondary Plan [[Fiduciary]] 
Name 
6 35 30 A/N Secondary [[Fiduciary]] responsible for the 
plan 
Required if Plan Type = 11 (Multiple 
Employer Plan) 
OC S7 
Secondary Plan [[Fiduciary]] 
Address Line #1 
36 70 35 A/N 1st line of Secondary Plan 
[[Fiduciary]]/Sponsor’s address 
Required if Secondary Plan [[Fiduciary]] is 
populated 
OC S8 
Secondary Plan [[Fiduciary]] 
Address Line #2 
71 105 35 A/N 2nd line of Secondary Plan 
[[Fiduciary]]/Sponsor’s address 
O  
Secondary Plan [[Fiduciary]] 
City 
106 138 33 A/N City name of Secondary Plan 
[[Fiduciary]]/Sponsor’s address 
Required if Secondary Plan [[Fiduciary]] is 
populated 
OC S9 
Secondary Plan [[Fiduciary]] 
State 
139 140 2 A/N 2-byte alpha code of state of Secondary 
Plan [[Fiduciary]]/Sponsor’s address 
Required if Secondary Plan [[Fiduciary]] is 
populated 
OC T0 
Secondary Plan [[Fiduciary]] 
Zip Code 
141 151 11 A/N Zip Code 
5-digit Zip Code + 4-digit Zip-Four +       
2 digits for future postal expansion 
 
Required if Secondary Plan [[Fiduciary]] is 
populated 
OC T1 

---

## Page 16

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Header Record 16 
Sequence 4        
Field Name 
Start End Len Type Description Opt/ 
Req 
Rej 
Code 
Filler 152 300 149 A/N Space R  

---

## Page 17

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Detail Record 17 
MF RETIREMENT PLAN REPORTING DETAIL RECORD 
Retirement Plan Detail Record (B/F/T 48) 
Required Record 
Input from TPA or Record Keeper (on behalf of TPA) to [[NSCC]] 
Output from [[NSCC]] to Firm 
Retirement Plan Detail Record (B/F/T48) 
Field Name Start End Len Type Description Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N B = Firm 
T = TPA 
F = Fund (for future use) 
R 01 
Record Type 2 3 2 A/N 48 R 02 
Filler 4 5 2 A/N Space R  
Security Issue [[ID]] 6 14 9 A/N Security Issue [[ID]] 
(may include both registered and 
unregistered Security Issue [[ID]]’s) 
R 05 
Product Investment Type 15 16 2 A/N 01 = Mutual Fund 
02 = ETFs 
03 = Collective Funds (CITs) 
04 = Separate Accounts 
05 = Annuities 
 
99 = Other 
R T2 
Define Product 
Investment Type 
17 46 30 A/N Description required if Product 
Investment Type [[Option]] = 99 
OC T3 
Fund Account for the 
Plan 
47 66 20 A/N Fund account number at the fund where 
the plans assets can be found for this 
Security Issue [[ID]] 
O  
QDIA 67 67 1 A/N Is this Security Issue [[ID]] a QDIA 
investment? 
Y = Yes 
N = No 
U = Unknown 
R T4 

---

## Page 18

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Detail Record 18 
Field Name Start End Len Type Description Opt/ 
Req 
Rej 
Code 
Participants in Security 
Issue [[ID]] 
68 73 6 N Number of participants with balance in 
the Security Issue [[ID]] (at end of period) 
999,999 
Zeros are allowed 
R T5 
[[shares]] in Security Issue 
[[ID]] 
74 89 16 N Month end [[shares]] in Security Issue [[ID]] 
for the plan 
999,999,999,999.9999 
Zeros are allowed 
R T6 
Month End Assets for 
Security Issue [[ID]] 
90 105 16 N Month end assets in the Security Issue 
[[ID]] for the plan 
99,999,999,999,999.99 
Zeros are allowed 
R T7 
Avg. Daily Assets for 
Security Issue [[ID]] 
106 121 16 N Average daily market value based on 
calendar days in the period for the plan 
in the Security Issue [[ID]] 
99,999,999,999,999.99 
Zeros are allowed 
O U2 
Price 
 
 
122 133 12 N 999,999.999999 
 
Price of the Security Issue [[ID]] Zeroes are 
NOT allowed 
Best Practice: 
This field should contain the price for the 
“Security Issue [[ID]]” (Detail Record 48 
position 6-14). It should reference the 
price that was used to calculate “Month 
End Assets for Security Issue [[ID]]” field 
value (Detail Record 48, position 90-
105) and should also reflect the price 
calculated on the last 
day of the reported 
period (“End date for Period” field – 
Header record 47, sequence 1 position 
56-63). 
R 47 
Filler 134 291 158 A/N Space R  
[[NSCC]] Reject Indicator 292 292 1 N Input: Space 
 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
R  
[[NSCC]] Reject Code # 1 293 294 2 A/N Input: Space 
Output: Reject Code or space 
R  

---

## Page 19

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Detail Record 19 
Field Name Start End Len Type Description Opt/ 
Req 
Rej 
Code 
[[NSCC]] Reject Code # 2 295 296 2 A/N Input: Space 
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 3 297 298 2 A/N Input: Space 
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 4 299 300 2 A/N Input: Space 
Output: Reject Code or space 
R  

---

## Page 20

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Trailer Record 20 
MF RETIREMENT PLAN REPORTING TRAILER RECORD 
Retirement Plan Trailer Record (B/F/T49) 
Required Record 
Input from TPA or Record Keeper (on behalf of TPA) to [[NSCC]] 
Output from [[NSCC]] to Firm 
Retirement Plan Trailer Record (B/F/T49) 
Field Name Start End Len Type Description Opt/ 
Req 
Rej 
Code 
System Code 1 1 1 A/N B = Firm 
T = TPA 
F = Fund (for future use) 
R 01 
Record Type 2 3 2 A/N 49 R 02 
Filler 4 5 2 A/N Space R  
Plan [[ID]] Number 6 17 12 A/N Unique internal recordkeeping a/c # for 
the plan 
R U1 
Filler 18 29 12 A/N  R  
Clearing/Settling Firm 
Number (Deliverer 
Number) 
30 33 4 A/N Required when System Code = B OC 
I2/T9 
Clearing/Settling Firm 
Number (Recipient 
Number) 
34 37 4 A/N  R F4 
Filler 38 49 12 A/N Space R  
TPA Number 50 53 4 A/N Required when System Code = T OC G0 
Total Security Issue [[ID]]’s 54 59 6 N 999,999 R T8 
Total Records 60 68 9 N 999,999,999 
(Including Headers and Trailers) 
R G8 
Filler 69 291 223 A/N Space R  
[[NSCC]] Reject Indicator 292 292 1 N Input: Space 
 
Output: 
0 = Accepted by [[NSCC]] 
1 = Rejected by [[NSCC]] 
R  

---

## Page 21

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Trailer Record 21 
Field Name Start End Len Type Description Opt/ 
Req 
Rej 
Code 
[[NSCC]] Reject Code # 1 293 294 2 A/N Input: Space 
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 2 295 296 2 A/N Input: Space 
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 3 297 298 2 A/N Input: Space 
Output: Reject Code or space 
R  
[[NSCC]] Reject Code # 4 299 300 2 A/N Input: Space 
Output: Reject Code or space 
R  

---

## Page 22

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting DataTrak Records 22 
MF RETIREMENT PLAN REPORTING DATATRAK 
RECORDS 
Datatrak Header Record 
Required on Input from Fund / Firm to [[NSCC]] 
DataTrak Header Record 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value ‘HDR.S’ R 
DATATRAK SYSID 6 10 5 A/N Value ’26590’ R 
Literal 11 16 6 A/N Value ‘.E00.C’ R 
Originator Clearing # 17 20 4 A/N  R 
Literal 21 22 2 A/N Value ‘.S’ R 
Sub Originator 23 26 4 A/N  R 
Processing Date 27 34 8 N mmddccyy R 
File Description 35 59 25 A/N Value ‘MF Retirement Plan ’ R 
Multi Batch Indicator 60 60 1 A/N Single Batch = Space  
Multi Batch = N 
Last Batch = Y 
R 
Multi Batch Number 61 63 3 N Zeroes when not Multi Batch R 
Filler 64 300 237 A/N Space R 
 
 
  

---

## Page 23

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting DataTrak Records 23 
Datatrak Trailer Record 
Required 
DataTrak Trailer Record 
Field Name Start End Len Type Description Opt/ 
Req 
Literal 1 5 5 A/N Value ‘END.S’ R 
DATATRAK SYSID 6 10 5 A/N Value ’26590’ R 
Literal 11 16 6 A/N Value ‘.E00.C’ R 
Originator Clearing # 17 20 4 A/N  R 
Literal 21 22 2 A/N Value ‘.S’ R 
Sub Originator 23 26 4 A/N  R 
Data File Record Count 27 33 7 N Datatrak Header or Trailer not included in 
count 
O 
Filler 34 300 267 A/N Space R 

---

## Page 24

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Output Records 24 
MF RETIREMENT PLAN REPORTING OUTPUT RECORDS 
Service Output Header Record (N00) 
Retirement Plan Reporting Service Output Header Record 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N 00 = Output Header 
Sequence Number 4 4 1 N 1 
MRO Recipient Number 5 8 4 N  
Literal 9 19 11 A/N Value '11111111111' 
Transmission Date 20 27 8 A/N mmddccyy 
Autoroute File [[ID]] 28 35 8 A/N Value '02101322' 
Literal 36 55 20 A/N Value ‘MF Retirement Plan ‘ 
Filler 56 300 245 A/N Space 
 
 
  

---

## Page 25

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Output Records 25 
Input Acknowledgement Record (NRA) 
Output from [[NSCC]] to Fund/Firm 
Retirement Plan Input Acknowledgement Record (NRA) 
Field Name Start End Len Type Description 
System Code 1 1 1 A/N N = [[NSCC]] 
Record Type 2 3 2 A/N RA = Retirement Plan Acknowledgement 
Filler 4 5 2 A/N Space 
Clearing/Settling Firm Number 
(Deliverer 
Number) or TPA 
6 9 4 A/N [[NSCC]] number of party submitting the file 
Clearing/Settling Firm 
Number (Recipient Number) 
10 13 4 A/N [[NSCC]] number for recipient of the file 
Processing Date 14 21 8 N mmddccyy 
Total Records in File 22 31 10 N 9,999,999,999 
Including Headers and Trailers 
Accepted Records Count 32 41 10 N 9,999,999,999 
Rejected Records Count 42 51 10 N 9,999,999,999 
Filler 52 300 249 A/N Space 
 
 
  

---

## Page 26

Retirement Plan Reporting Record Layouts 
MF Retirement Plan Reporting Output Records 26 
Retirement Plan Grand Total Trailer Record (NRG) 
Required on Output 
The Grand Total Trailer record is used to recap all records on output from [[NSCC]]. It is sent to both the 
submitting and receiving participants. 
Retirement Plan Grand Total Trailer Record (NRG) 
Field Name Start End Len Type Description Opt/ 
Req 
System Code 1 1 1 A/N Output 
N = [[NSCC]] 
R 
Record Type 2 3 2 A/N RG = Retirement Plan Grand Total Trailer R 
Filler 4 5 2 A/N Space R 
Clearing/Settling Firm 
Number (Recipient Number) 
6 9 4 A/N  R 
Total Records Count 10 20 11 N 99,999,999,999 
Total Number of physical records per 
recipient (output from [[NSCC]]) 
R 
Filler 11 300 280 A/N Space R 
 
 

---

## Page 27

Retirement Plan Reporting Record Layouts 
APPENDIX – Summary of Changes 27 
APPENDIX – SUMMARY OF CHANGES 
The following Summary of Changes are listed in chronological order, starting with the most recent changes.  
 

---

## Page 28

Retirement Plan Reporting Record Layouts 
Summary of changes – Effective March 25, 2019 28 
SUMMARY OF CHANGES – EFFECTIVE MARCH 25, 2019 
Reject Codes 
The following new [[NSCC]] reject code will be utilized to reject transactions that fail Ocode validation:  
Reject Code Description 
X8 [[participant]] is not valid for the Submitter and/or Product 

---

## Page 29

Retirement Plan Reporting Record Layouts 
Summary of changes – Effective February 27, 2017 29 
SUMMARY OF CHANGES – EFFECTIVE FEBRUARY 27, 
2017 
Add New Fields 
Field Name Record Type and Field Location Description Rej 
Code 
Contribution 
Amount 
Credit/Debit 
Indicator 
47 seq#2,start 225, end 225, Length 
1, A/N, Optional 
Blank = Credit 
D = Debit 
 
This indicator specifies if the value provided in 
the “Contribution Amount for the Plan” field is 
positive (Credit) or negative (Debit) 
W8 Distribution 
Amount 
Credit/Debit 
Indicator 
47 seq#2,start 226, end 226, Length 
1, A/N, Optional 
Blank = Debit  
C = Credit 
 
This indicator specifies if the value provided in 
the “Distribution Amount for the Plan” field is 
positive (Debit) or negative (Credit) 
W9 
Price 48, start 122, end 133, Length 12, N, 
Required 
999,999.999999 
Price of the Security Issue [[ID]] 
Zeroes are NOT allowed 
Best Practice: 
This field should contain the price for the 
“Security Issue [[ID]]” (Detail Record 48 position 
6-14). It should reference the price that was 
used to calculate “Month End Assets for 
Security Issue [[ID]]” field value (Detail Record 
48, position 90-105) and should also reflect the 
price calculated on the last day of the reported 
period (“End date for Period” field – Header 
record 47, sequence 1 position 56- 
63). 
47 
Reject Codes 
The following new reject code have been added: 
Reject Code Description 
W8 Contribution Amount Credit/Debit Indicator is Invalid 
W9 Distribution Amount Credit/Debit Indicator is Invalid 
 
The changes described above are highlighted in the layouts. 

---

## Page 30

Retirement Plan Reporting Record Layouts 
Summary of changes – Effective July 27, 2015 30 
SUMMARY OF CHANGES – EFFECTIVE JULY 27, 2015 
Change to Data Field Population Requirement 
Field Name Record Type and Location Current 
Requirement 
New 
Requirement 
DOL Plan Code Number 47 seq#1, start 27, end 29 length 3, N Required Optional 
Plan [[Fiduciary]] Name 47 seq#1, start 64, end 93, length 30, A/ N Required Optional 
Plan [[Fiduciary]] Address Line #1 47 seq#1, start 94, end 128, length 35, A/ N Required Optional 
Plan [[Fiduciary]] City 47 seq#1, start 164, end 196, length 33, A/ N Required Optional 
Plan [[Fiduciary]] State 47 seq#1, start 197, end 198, length 2, A/ N Required Optional 
Plan [[Fiduciary]] Zip 47 seq#1, start 199, end 209, length 11, A/ N Required Optional 
Add New Values to Existing Field 
Field Name Record Type and Field Location Description Rej Code 
ERISA Flag 47 seq#2,start 127, end 127, Length 1, A/N, 
Required 
Identify if Plan is ERISA or not  
Y = Yes 
N= No 
U = Unknown 
S0 
QDIA 48, start 67, end 67, Length 1, A/N, Required Is this Security Issue [[ID]] a QDIA 
investment? 
Y = Yes N = No 
U = Unknown 
T4 

---

## Page 31

Retirement Plan Reporting Record Layouts 
Summary of changes – November 18, 2014 31 
SUMMARY OF CHANGES – NOVEMBER 18, 2014 
November 18, 2014 Added the File Overview, Record Sequence Order and Record Layout references. See 
Table of Contents. 
 
 

---

## Page 32

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: November 28, 2023 
Publication Code: MFS341 
Service: Networking 
Title: Retirement Plan Reporting Record Layouts 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
  