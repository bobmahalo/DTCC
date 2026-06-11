---
title: "Fund/SERV Technical Guide, Chapter 7: Section 529 Qualified Tuition Programs Fund/SERV and Networking"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_techguide_ch7_mfs249_20220721.pdf"
pages: 28
size: "523.0 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# Fund/SERV Technical Guide, Chapter 7: Section 529 Qualified Tuition Programs Fund/SERV and Networking

**Original File:** [fs_techguide_ch7_mfs249_20220721.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_techguide_ch7_mfs249_20220721.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 28  
**File Size:** 523.0 KB  

---

## Page 1

 
 
 
FUND/SERV ® 
CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® 
AND NETWORKING 
JULY 21, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: July 21, 2022 
Publication Code: MFS249 
Service: Fund/SERV® 
Title: Fund/SERV Technical Manual - Chapter 7: Section 529 Qualified Tuition Programs Fund/SERV and Networking 
 
 

---

## Page 3

 
 
CHANGE HISTORY 
 
Dates Descripton 
July 21, 2022 Corrected links that broke due to Learning upgrade.   
March 12, 2021 Rebranded 
July 10, 2020 Broken links corrected.  
 
  

---

## Page 4

 
 
TABLE OF CONTENTS 
 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV ............................................................... 6 
Qualified Higher Education Expenses (QHEE) .................................................................................................. 6 
State and Federal Tax Advantages .................................................................................................................... 6 
Tax Benefits ........................................................................................................................................................ 6 
Account Owners and Beneficiaries ..................................................................................................................... 7 
Account Owners/Participants ............................................................................................................................ 7 
Beneficiaries ...................................................................................................................................................... 7 
Contributions ....................................................................................................................................................... 7 
Investment Options ............................................................................................................................................. 7 
Marketing Section 529 Plans .............................................................................................................................. 8 
Successor Owner................................................................................................................................................ 8 
Types of Withdrawals ......................................................................................................................................... 8 
Qualified Withdrawals ........................................................................................................................................ 8 
Nonqualified Withdrawals .................................................................................................................................. 8 
[[NSCC]] Administrative Requirements................................................................................................................... 9 
Fund/SERV Processing Rules and System Modifications.................................................................................. 9 
New Security Type Code................................................................................................................................... 9 
Transactions ....................................................................................................................................................... 9 
Original Transactions ........................................................................................................................................ 9 
Subsequent Transactions.................................................................................................................................. 9 
Exchange Orders ............................................................................................................................................10 
Registration .......................................................................................................................................................10 
Registration Requirements ..............................................................................................................................10 
Fund/SERV Registration Record (401) ...........................................................................................................10 
Fund/SERV Order (001) and Related Records ................................................................................................12 
Social Codes .....................................................................................................................................................17 
Record Layouts .................................................................................................................................................17 

---

## Page 5

 
 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING ...................................................... 18 
[[Broker]]/Fund Account Conversion Records A/B/F/T 50/51– Sequence #1.......................................................18 
Account Type ..................................................................................................................................................18 
Customer Zip Code .........................................................................................................................................18 
Account / Owner U.S. Citizenship Indicator ....................................................................................................19 
Owner Date of Birth .........................................................................................................................................19 
[[Broker]]/Fund Account Conversion Records A/B/F/T 50/51 – Sequence # 3 ...................................................19 
Age Based Indicator ........................................................................................................................................19 
Age Based Roll Exempt Indicator ...................................................................................................................20 
Account/Owner U.S. Resident Alien Indicator.................................................................................................20 
[[Broker]]/Fund Account Conversion Records A/B/F/T 50/51- Sequence #4 .......................................................20 
Account City & Account State .........................................................................................................................20 
Number of Beneficiaries and/or Successor Owner .........................................................................................21 
Successor Owner Indicator .............................................................................................................................21 
Sequence Record Grouping for the [[Broker]]/Fund Account Conversion Records A/B/F/T 50/51  ......................21 
[[Broker]]/Fund Account Conversion Records A/B/T52, F52 Sequence #1..........................................................24 
Transaction Type Field ....................................................................................................................................24 
529 Transfer Reason Code .............................................................................................................................24 
IRS 529 Annual Strategy Change Counter .....................................................................................................25 
Updated Fields on the [[Broker]]/Fund Account Conversion Records A/B/T52, F53 –  Sequence #3 ..................25 
529 Rollover Required Fields – “Cost Basis Dollar Amount” & “Earnings to Date” ........................................25 
Negative Earnings to Date Indicator ...............................................................................................................26 
Activity Reporting Records Activity Detail F55 - Sequence # 2 ........................................................................26 
Updated Activity Reporting Records Activity Detail F55 – Sequence #5 .........................................................27 
 
 

---

## Page 6

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 6 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR 
FUND/SERV 
The purpose of this guide is to provide the mutual fund industry with the information necessary to process 
purchase orders and subsequent purchase orders for Section 529 plans in an automated environment.  
The information in this guide is designed as a summary of the law and is provided for your convenience. It is 
not intended to represent the law itself and should not be used for this purpose.  
Section 529 Qualified Tuition Programs are established and operated by a state or a state agency. They 
enable residents and non-residents to contribute on a tax-favored basis to a fund for qualified higher education 
expenses of account beneficiaries. Account owners establish accounts in a statutory trust fund. Their cash 
contributions are invested according to the investment options they select.  
Please use the Web site for your state's 529 program in order to gain answers pertaining to a specific plan. 
You can use the URL https://www.policygenius.com/blog/a-state-by-state-guide-to-529-plans/ to reach these 
sites. 
Qualified Higher Education Expenses (QHEE) 
Students enrolled in accredited Eligible Educational [[Institutions]], including:  
• foreign [[Institutions]] offering post-secondary degrees (which may include graduate level degrees)  
• approved vocational schools  
 
may claim expenses. Claims can be made for tuition, fees, books, certain supplies and equipment, and, in 
some cases, for rent and board.  
State and Federal Tax Advantages 
Several programs offer state resident taxpayers participating in these programs an annual income tax 
deduction. State income tax deduction differs based on the state or states in which the account owner pays 
that tax. There is federal and state deferral on earnings on a Section 529 account.  
Tax Benefits  
• Qualified distributions are fully exempt from federal income tax.  
• Account owners can move tax-free from one state’s plan to another once a year without changing the 
plan’s beneficiary.  
 

---

## Page 7

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 7 
Account Owners and Beneficiaries 
Account Owners/Participants 
Anyone can participate. Parents, grandparents, relatives, or friends can open an account regardless of where 
they reside or what their income may be. The account owner is the person with ownership and control of the 
Section 529 account, usually the donor.  
Note: 
Many Section 529 plans refer to the account owner as the [[participant]]. 
Beneficiaries  
The designated beneficiary is the individual for whom the account is established for the purpose of paying 
future college costs. A Section 529 savings program has a designated beneficiary for each account, with the 
possible exception of accounts established by state or local governments or 501(C)(3) organizations. A 
beneficiary may be:  
• Anyone intending to go to college. This includes a child, grandchild, spouse, relative, someone not related 
to the account owner, or the account owner him or herself.  
• A person of any age.  
Contributions  
Each state program has its own contribution limits. (Refer to the rules and regulations of individual states.) 
Competition between states has led to improvements in investment choices and the number of choices 
available.  
Investment Options  
The program manager can offer:  
1. Portfolios where their underlying assets are registered mutual fund [[shares]].  
o Contributions are used to purchase interests in the program portfolios that entitle an account holder 
to a share of the assets that are held by the trust and expressed as a number of units.  
o Interests are considered municipal fund [[securities]] not registered with the [[SEC]].  
o An IRS notice of September 7, 2001, states that account owners can now move their money from 
one investment [[Option]] to another. The number of investment strategy changes allowed during one 
calendar year is set by the IRS.   This can only be made from one ‘broad-based’ investment strategy 
to another.  
2. Individual mutual fund [[shares]]  
3. Stable value [[Option]]  
 

---

## Page 8

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 8 
Marketing Section 529 Plans  
Accounts are sold by registered representatives, brokers, and dealers (Advisor -sold), and also can be 
purchased directly from the distributor (Direct-sold). The following applies to Advisor – sold versions of Section 
529 plans.  
• [[Broker]]/Dealers should check with the Municipal [[securities]] Rulemaking Board (MSRB) and their primary 
regulator to determine their eligibility to distribute interests in Section 529 plans. The MSRB considers 
interests in the program to be municipal fund [[securities]].  
• In order to supervise municipal fund [[securities]], every dealer must have either a municipal fund [[securities]] 
limited principal (Series 51), or a municipal [[securities]] principal (Series 53).  
Successor Owner 
The account owner may designate a successor owner of the account.  
• In the event of the death of the account owner, the successor owner will automatically become the new 
account owner.  
• The successor owner may have the right to change the designated beneficiary in the account. (Refer to 
individual state program rules and regulations.)  
• The successor owner will be required to provide the program manager with a certified copy of the death 
certificate of the account owner.  
Types of Withdrawals 
There are three types of withdrawals:  
• Qualified  
• Nonqualified  
• Withdrawals on account of death, disability, or scholarship.  
Qualified Withdrawals  
A withdrawal from an account that is used to pay the qualified higher education expenses of the designated 
beneficiary.  
Nonqualified Withdrawals  
Any withdrawal from an account other than the following:  
• A qualified withdrawal  
• A withdrawal by reason of the death or disability of the beneficiary  
• A withdrawal due to a scholarship received by the beneficiary as long as the amount withdrawn does not 
exceed the scholarship.  

---

## Page 9

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 9 
Note: 
A nonqualified withdrawal is subject to a penalty (a percentage of the earnings portion of the withdrawal). 
[[NSCC]] Administrative Requirements  
Before transactions in Fund/SERV® can be processed for Section 529 plans participants must:  
• Complete the ‘Security Issue [[ID]] Add’ form which can be found in the Participants Section of the [[DTCC]] 
Wealth Management website at https://portal.[[DTCC]].com. 
• Call Mutual Fund Services 212-855-8877 for guidance on getting access the [[participant]] and Security Add 
forms.  
Fund/SERV Processing Rules and System Modifications 
New Security Type Code  
Security Type Code (61) identifies a Security Issue [[ID]] that belongs to a Section 529 plan.  
Transactions  
Original Transactions  
[[NSCC]] passes original transactions, particularly [[Broker]] transactions, for example, Orders (001), As -Of Orders 
(004) and Exchanges (015), to the Fund. The Fund decides whether to confirm the transaction or to reject it. 
Reminders will be sent if the transaction is not confirmed by the Fund in the normal processing timeframe.  
Subsequent Transactions  
Fund/SERV will process subsequent transactions for example, Firm Delete (102), Firm Exit (139), Correction 
(003), and Cash Adjustment (011), in accordance with Fund/SERV system rules. There will be no exception 
processing for Section 529 plan accounts.  
[[NSCC]] will not reject any transactions (for example, Automated Customer Account Transfer Service [ACATS] 
Transfer/Acknowledgement/Rejection, Transfer of Retirement [[Asset]] Service [ToRA]) where the security issue 
type identifier code in the system is 61, Section 529 Account-Qualified Tuition Program.  
[[NSCC]] will not edit for consistency between the [[Asset]] Type Indicator and the new values added to Security 
Type, NAV Reason Code, [[settlement]] Override Reason Code, and Social Code.  
 
In these situations, it is up to the Fund to decide whether to accept or reject the transactions.  

---

## Page 10

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 10 
The [[Asset]] Type Indicator cannot be changed by a subsequent transaction from 529  D, E, P or Q to something 
else nor can the indicator be changed from something else to D, E, P or Q. Any subsequent transaction made 
with the intent to change the indicator in this way, will be rejected by Fund/SERV.  
A Section 529 order cannot be changed by a subsequent transaction (such as a correction or confirmation) 
from one type to another. An order cannot be changed from a Section 529 order to a non– Section 529 order 
and vice versa.  
Exchange Orders  
Although an exchange order (record type 015) is one transaction, it involves both a redemption and a 
purchase.  
Note: 
The format on the purchase side of the record has been modified. The format of the redemption side will not be changed at 
the present time. [[NSCC]] will pass the exchange order to the Fund and they will confirm or reject the transaction. 
Registration  
Registration Requirements  
If an initial purchase is processed through Fund/SERV, a full registration is required according to current 
Fund/SERV rules.  
A registration, full or short, is not allowed on a subsequent transaction.  
If a registration is made against an initial purchase and the order was later changed to become a subsequent 
transaction through a correction or confirmation, the registration process must be completed as in regular 
Fund/SERV orders.  
Fund/SERV Registration Record (401)  
The following fields have been added or updated to support 529 Plan processing:  
1. The Date of Event (DOE) field. The date of event is the date the beneficiary is expected to enter college.  
2. Additional indicators in the Payable/Beneficiary/Successor Owner Address [[Option]] field:  
o C = 529 Beneficiary  
o D = 529 Successor Owner.  
3. There are 6 payable records available on the registration record. Starting with Record 9, it can have a 
Payable format (values 1-9) or Beneficiary/Successor Owner format (values A-D). If Payable Address 
[[Option]] = 1, 2, 9, then record 9 is in Payable format. If Beneficiary/Successor Owner Address [[Option]] = A, 
B, C, or D, then record 9 is in Beneficiary/Successor Owner format.  
4. To accommodate 529 Beneficiary and 529 Successor Owner information, these additional existing 
payable records are to be used to communicate Payable information, and/or 529 Beneficiary information, 
and/or 529 Successor Owner information.  

---

## Page 11

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 11 
 
Example: if Beneficiary/Successor Owner Address [[Option]] = C, then record 9 represents 529 Beneficiary. 
If Beneficiary/Successor Owner Address [[Option]] = D, then record 9 represents 529 Successor Owner.  
 
5. Registration Type. This field is optional. The values are:  
o 0 = Regular Registration  
o 1 = Section 529 Registration  
6. Aged Based Indicator 
o 1 – Aggressive  
o 2 – Moderate  
o 3 - Conservative  
7. Age Based Roll Exempt Indicator.  
o 0 = No, account is not exempt and will be included within Automatic Roll Events  
o 2 = Yes, account is exempt from Automatic Roll Events  
8. Customer/Owner U.S. Resident Alien Indicator.  
o 0 = No 
o 1 = Yes 
9. Successor Owner Indicator. Required when the Registration Type = 1, Section 529. The values are: 
o 0 = No 
o 1 = Yes 
10. Customer/Owner US Citizenship Indicator. Required when the Registration Type= 1, Section529 
Registration. The values are: 
o 0 = U.S. Citizen 
o 1 = Non-U.S. Citizen 
11. Customer City and Customer State. This field is required when the Registration Type = 1, Section 529 
Registration. See Record 6, Customer Name/Address Line 6. 
12. Customer Gender. This field is optional. The values are: 
o F = Female 
o M = Male 
13. When the Beneficiary/Successor Owner Address [[Option]] (Record 9) field indicates that Record 9 is in 
Beneficiary/Successor Owner format (values A-D) and the Registration Type = 1, Section 529 
Registration, the Beneficiary/Successor Owner Zip Code and the Beneficiary/Successor Owner SSN/EIN 
Number fields must be populated.  
14. Beneficiary/Successor Owner U.S. Citizenship Indicator (Record 9). This field is required when the 
Beneficiary/Successor Owner Address [[Option]] is “C” or “D”. The values are: 
o 0 = U.S. Citizen 
o 1 = Non-U.S. Citizen 
15. Beneficiary Gender. This field is optional. The values are: 
o F = Female 
o M = Male 
16. Three values have been added to the Beneficiary Relationship Indicator. 
o 3 = Grandchild  
o 4 = Relative  
o 5 = Child  

---

## Page 12

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 12 
17. For Registration Type = 1 (Section 529 Registration), the Beneficiary/Successor Owner 1 City and 
Beneficiary/Successor Owner 1 State fields are optional when the Successor Owner Indicator = 1 (Yes) 
and Address [[Option]] = D (529 Successor Owner) otherwise these fields are required. See Record 12, 
Payable/Beneficiary/Successor Owner 1 Name/Address Line 6. 
Fund/SERV Order (001) and Related Records 
1. The following four values pertaining to Section 529 transactions are in the Transaction Type field for 
Fund/SERV record types 001, 004, 005, 006, 007, 009, 140, 003, 025, and 026. They are valid selections 
when the value in the Transaction Code field is “03 = Partial [[liquidation]]” or “04 = Full [[liquidation]].”  
o 8 = 529 [[participant]] Distribution  
o 9 = 529 Beneficiary Distribution  
o A = 529 School Distribution  
o B = 529 Rollover Distribution  
2. Code (05) for Section 529 accounts has been added to the [[settlement]] Override Reason Codes. This code 
enables a firm to select the way in which the Section 529 trade should settle without regard to the Fund’s 
Security Profile. The firm does this by providing the Anticipated [[settlement]] Date in the Fund/SERV Order 
for the transaction and using the reason code for invoking the override. The Fund in turn has the [[Option]] of 
confirming or rejecting the Section 529 order.  
3. Code (09) for Section 529 account has been added to the NAV Reason Codes. This code qualifies a Net 
[[Asset]] Value trade for the Section 529 purchase order.  
4. Beneficiary SSN/EIN Number. This field is optional/conditional. You can enter either the beneficiary’s 
social security number or tax identification number. This field is required for all Section 529 Plan 
Purchases when the value in the “[[Asset]] Type Indicator” field is equal to:  
o D = Section 529 Account  
o E = UGMA account transferred to Section 529 Account  
o P = 529 Previous Year Contribution (new value)  
o Q = 529 Rollover Contribution (new value)  
 
and the value in the “Transaction Code” field is either “01= Initial Purchase” or “02 = Subsequent 
Purchase.” The following record types are affected:  
o Order (“001”)  
o As-Of Order (“004”)  
o Confirmation (“005”)  
o Reconfirmation (“006”)  
o Fund Originated Order (“007”)  
o Fund Originated As-Of Order (“009”)  
o Post-[[settlement]] Cancellation by Fund (“140”)  
o Correction (“003”)  
o Correction Confirmation (“025”)  
o Post-[[settlement]] Correction by Fund (“026”)  
 
 

---

## Page 13

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 13 
5. Beneficiary SSN/EIN Indicator. This field is optional. If the Beneficiary SSN/EIN Number field is filled, then 
the Beneficiary SSN/EIN Indicator must be either: 
o 0 = [[ID]] number  
o 1 = Social Security Number  
6. The [[Asset]] Type Indicator field contains the following indicator codes: 
o D = 529 Current Year Contribution  
o E = UGMA Account transferred to Section 529 Account.  
o P = 529 Previous Year Contribution  
o Q = 529 Rollover Contribution  
 
These codes qualify the type of contribution that is being made by the Section 529 purchase order.  
7. The “IRA/529 [[liquidation]] Indicator” field accommodates both IRA and Section 529 Plan liquidations. It is  
optional/conditional. The following values are included in “IRA/529 [[liquidation]] Indicator” field:  
o A = Qualified  
o B = Non-Qualified 
o D = 529 Owner Change 
o E = 529 Beneficiary Change – In-Family 
 
This field is required for Section 529 Plan liquidations if the value in the “Transaction Type” 
field is equal to: 
o 8 = 529 [[participant]] Distribution 
o 9 = 529 Beneficiary Distribution 
o A = 529 School Distribution 
o B = 529 Rollover Distribution 
 
This field is in following record types:  
o Order (“001”) 
o As-Of Order (“004”) 
o Confirmation (“005”) 
o Reconfirmation (“006”) 
o Fund Originated Order (“007”) 
o Fund Originated As-Of Order (“009”) 
o Post-[[settlement]] Cancellation by Fund (“140”) 
o Correction (“003”) 
o Correction Confirmation (“025”) 
o Post-[[settlement]] Correction by Fund (“026”) 
 
8. The “Original IRA/[[liquidation]] Indicator” field accommodates both IRA and Section 529 Plan liquidations.  
This field is in the following record types: 
o Correction (“003”) 
o Correction Confirmation (“025”) 
o Post-[[settlement]] Correction by Fund (“026”) 

---

## Page 14

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 14 
9. Firms are required to indicate whether a 529 purchase is a Previous Year Contribution or a Rollover. 
Value D will allow Firms to indicate if the 529 Purchase is a Current Year Contribution. The following two  
values are available in the “[[Asset]] Type Indicator” field:  
o P = 529 Previous Year  
o Q = 529 Rollover Contribution  
 
The following record types include this field:  
o Order (“001”)  
o As-Of Order (“004”)  
o Confirmation (“005”)  
o Reconfirmation (“006”)  
o Fund Originated Order (“007”)  
o Fund Originated As-Of Order (“009”)  
o Post-[[settlement]] Cancellation by Fund (“140”)  
o Correction (“003”)  
o Correction Confirmation (“025”)  
o Post-[[settlement]] Correction by Fund (“026”)  
 
10. “Cost Basis Money Amount” field and “Earnings to Date Money Amount” field are optional/conditional and 
are used to capture the money amounts needed for accurate preparation and processing of the 
shareholders’ Tax Reporting.  
 
These fields are required if the “[[Asset]] Type Indicator” field value is equal to “Q = 529 Rollover 
Contribution.” Each field will be 16 bytes (99,999,999,999,999.99). The [[default]] value for this field will be 
zeroes. These fields are available on the following records:  
o Order (“001”)  
o As-Of Order (“004”)  
o Confirmation (“005”)  
o Reconfirmation (“006”)  
o Fund Originated Order (“007”)  
o Fund Originated As-Of Order (“009”)  
o Post-[[settlement]] Cancellation by Fund (140)  
o Correction (“003”)  
o Correction Confirmation (“025”)  
o Post-[[settlement]] Correction by Fund (“026”)  
 
11. “Negative Earnings to Date Indicator” field:  
 
It is important for funds and firms to know whether the new “Earnings To Date” field contains a negative or 
positive number.  
The “Negative Earnings to Date Indicator” field is used to identify a negative amount in the “Earnings to 
Date” field.  
The valid value for this optional field is either “N” or a space (blank). If this field is left blank, it will mean 
the Earnings to Date are positive earnings.  
o N = Negative  

---

## Page 15

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 15 
o Space (blank) = Positive  
 
This field is on the following records:  
o Order (“001”)  
o As-Of Order (“004”)  
o Confirmation (“005”)  
o Reconfirmation (“006”)  
o Fund Originated Order (“007”)  
o Fund Originated As-Of Order (“009”)  
o Post-[[settlement]] Cancellation by Fund  
o Correction (“003”)  
o Correction Confirmation (“025”)  
o Post-[[settlement]] Correction by Fund (“026”)  
 
Order – Record Type 001 – Record 6 of 6 
Field Name Start End Len Type Description Opt/Req Reject 
Code 
Cost Basis Money 
Amount 
45 60 16 N 99,999,999,999,999.99 This field is 
required if the [[Asset]] Type Indicator = 
Q.  
This field is not required for any other 
[[Asset]] Types. 
OC 261 
Earnings to Date 
Dollar Amount 
61 76 16 N 99,999,999,999,999.99 This field is 
required if the [[Asset]] Type Indicator = 
Q. This field is not required for any 
other [[Asset]] Types. 
OC 262 
Negative Earnings 
to Date Indicator 
77 77 1 A/N N = Negative Spaces = Positive O 263 
Filler 78 100 21 A/N Space R  
 
12. Required records  
Fund/SERV Fixed length format Record sequence # 6 for Orders (001), Record sequence #7 for As of 
Orders (004) and Corrections (003); Variable length format Record length 569 for Orders, and record 
length 662 for the As of Orders are:  
o "Required when Redemption Fee Indicator is provided or [[Asset]] Type Indicator = Q (529 Rollover 
Contribution)"  
 
 
  

---

## Page 16

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 16 
 
The following are the layouts affected by the requirement stated above. 
Record Type Record Sequence #  (Fixed 
Length Format) 
Record Length 
(Variable Length Format) 
001 – Order 6 569 
004 - As-Of Order 
005 - Confirmation 
006 - Reconfirmation 
007 - Fund Originated Order 
009 - Fund Originated As-Of Order 
140 - Post [[settlement]] Cancellation by Fund 
7 662 
003 - Correction  
025 - Correction Confirmation 
026 - Post [[settlement]] Correction by Fund 
7 662 
 
13. Format for Record 9 of 32 on Record 401 Full Registration  
 
The “Beneficiary/Successor Owner Address [[Option]]” field values indicate the type of Beneficiary on the 
Full Registration (401) record and what record format should be followed.  
If the value in the “Beneficiary/Successor Owner Address [[Option]]” field is A (Primary IRA Beneficiary), B 
(Secondary IRA Beneficiary), C (529 Beneficiary) or D (529 Successor Owner), then record 9 of the Full 
Registration is in Beneficiary/Successor Owner format.  
Record 9 of 32 (Beneficiary) - Required for Section 529 registration (Registration Type = 1) 
 
Note: Record 9 has three different formats. Address [[Option]] field (column 40) indicates which format is being used as 
follows:  
• If Address [[Option]] = 1, 2, … 9, then record 9 is in Payable format.  
• If Address [[Option]] = A, B, C, or D, then record 9 is in Beneficiary/Successor Owner format.  
• If Address [[Option]] = E or F, then record 9 is in Payable of x-[[settlement]] format.  
 
14. Description for Value B in the “Transaction Type” Field  
The description for value B in the “Transaction Type” field has been changed from B = 529 Rollover to B = 
529 Rollover Distribution to be consistent with the other new values being added that relate to 529 
distributions.  
 
This field is on the following Record Types:  
o Order (“001”)  
o As-Of Order (“004”)  
o Confirmation (“005”)  

---

## Page 17

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529-QUALIFIED TUITION PROGRAMS-FOR FUND/SERV 17 
o Reconfirmation (“006”)  
o Fund Originated Order (“007”)  
o Fund Originated As-Of Order (“009”)  
o Post-[[settlement]] Cancellation by Fund (“140”)  
o Correction (“003”)  
o Correction Confirmation (“025”)  
o Post-[[settlement]] Correction by Fund (“026”)  
Social Codes 
The following new social codes have been added to indicate the type of transfers into a Section 529 Plan account 
and to identify the account as a 529 account: 
37 Section 529 Account – Qualified Tuition Program  
38 UGMA/UTMA transferred into Section 529  
39 Section 529 transferred into new Section 529  
40 IRA transferred into section 529  
41 Series E/Series I U.S. Savings [[Bonds]] transferred into Section 529  
61 Joint Owner Section 529 
62 529 Trust 
 
Record Layouts  
Record layouts can be access on the Learning Center at https://dtcclearning.com/products-and-services/mutual-
fund-services/record-layouts.html 
 
 

---

## Page 18

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 18 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR 
NETWORKING 
The purpose of this section is to highlight key fields within Networking as they relate to 529 Plan Accounts. For 
more detail on Networking in general please refer to the Networking Technical User Guide.  
[[Broker]]/Fund Account Conversion Records A/B/F/T 50/51– Sequence 
#1 
Account Type  
This optional field indicates whether the new account or maintenance transacted through Networking is for a 
Section 529 Plan Account.  
The valid values for the new optional “Account Type” field are:  
o 0 = Regular Account  
o 1 = Section 529 Account  
Field Name Start End Len Type Description Opt/Req 
50/51 
Account Type 88 88 1 A/N 0 = Regular Account  
1 = Section 529 Account 
OO 
 
If an incorrect or invalid value is populated in the “Account Type” field, [[NSCC]] will reject using the following 
reject code:  
o J4 - Account Type is Invalid  
Customer Zip Code  
When the “Account Type” field value is 1 = Section 529 Account, the “Customer Zip Code” field will be 
required. 
Field Name Start End Len Type Description Opt/Req 
50/51 
Customer Zip Code 67 75 9 A/N 5 digit Zip Code + 4 digit Zip-Four Required 
for Section 529 Account (when Account Type 
= 1)  
OC/OC 
 

---

## Page 19

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 19 
When the “Account Type” field value is 1 = Section 529 Account, and the Customer Zip Code is not provided, 
the last field will be rejected by [[NSCC]] using the following reject code:  
o J9 – Customer Zip Code missing for Section 529 Account 
Account / Owner U.S. Citizenship Indicator  
When the “Account Type” field value is 1 = Section 529 Account, the “Account/Owner U.S. Indicator” field will 
be required. 
Field Name Start End Len Type Description Opt/Req 
50/51 
Account / Owner U.S 
Citizenship Indicator 
89 89 1 A/N Required for Section 529 Account (Account 
Type = 1) 
 0 = U.S. citizen  
1 = Not U.S. citizen 
OC/O 
Owner Date of Birth  
When the “Account Type” field value is 1 = Section 529 Account, the “Owner Date of Birth” field will be 
required. 
Field Name Start End Len Type Description Opt/Req 
50/51 
Owner Date of Birth 90 97 8 A/N Required for Section 529 Account  
(Account Type = 1)  
mmddccyy 
OC/O 
 
[[Broker]]/Fund Account Conversion Records A/B/F/T 50/51 – Sequence # 3 
Age Based Indicator  
The “Age Based Indicator” field is optional. 
Field Name Start End Len Type Description Opt/Req 
50/51 
Age Based 
Indicator 
96 96 1 A/N 1 = Aggressive  
2 = Moderate  
3 = Conservative 
O/O 
 

---

## Page 20

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 20 
Age Based Roll Exempt Indicator  
The “Age Based Roll Exempt Indicator” field is optional. 
Field Name Start End Len Type Description Opt/Req 
50/51 
Age Based Roll 
Exempt Indicator 
97 97 1 A/N 0 = No, Account is not exempt and will be 
included within automatic age roll event;  
1 = Yes, Account is exempt from automatic 
age roll event. 
O/O 
Account/Owner U.S. Resident Alien Indicator  
When the “Account Type” field value is 1 = Section 529 Account, the optional “Owner Date of Birth” field will be 
required. 
Field Name Start End Len Type Description Opt/Req 
50/51 
Account /Owner 
U.S. Resident 
Alien Indicator 
98 98 1 A/N 0 = No  
1 = Yes 
O/O 
[[Broker]]/Fund Account Conversion Records A/B/F/T 50/51- Sequence 
#4  
Account City & Account State  
When the “Account Type” field value is 1 = Section 529 Account, the existing Account Name/Address Line 6 
will require the “Account City” field and Account State” field. 
Columns 45-79 for Section 529 Account (Account = 1)  
Account City 
 
45 77 33 A/N Required for Section 529 Account (Account 
Type = 1)  
R/O 
Account State 
 
78 79 2 A/N Required for Section 529 Account (Account 
Type = 1)  
R/O 
Filler 80 100 21 A/N Space  R/R 
 
When the “Account Type” field value = 1, the “Account City” and “Account State” fields are required, if the 
required fields are not provided a reject code will be generated by [[NSCC]] and the transaction will be rejected to 
the submitter: 
J5 - Account City or/and Account State missing for Section 529 Account  

---

## Page 21

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 21 
Number of Beneficiaries and/or Successor Owner  
When the “Account Type” field value is 1 = Section 529 Account, the optional “Number of Beneficiaries and/or 
Successor Owner” field will be required. 
Field Name Start End Len Type Description Opt/Req 
50/51 
Number of Beneficiaries 
and/or Successor Owner 
80 81 1 N Required for Section 529 Account (Account 
Type = 1) 
OC/O 
 
Successor Owner Indicator  
When the “Account Type” field value is 1 = Section 529 Account, the optional “Successor Owner Indicator” field 
will be required. 
Field Name Start End Len Type Description Opt/Req 
50/51 
Successor Owner Indicator 82 82 1 A/N Required for Section 529 Account (Account 
Type = 1)  
 
0 = No  
1 = Yes  
Not allowed otherwise 
OC/O 
 
Sequence Record Grouping for the [[Broker]]/Fund Account Conversion 
Records A/B/F/T 50/51  
A Grouping of Sequence Records for Additional Registration Information, necessary for Section 529 Accounts 
were added to Networking. Each group consists of four records with specific sequence numbers, as follows:  
Group 1 (#13 through #16 with 13 and 14 required) is required if Number of Beneficiaries/Successor Owner = 01  
Group 2 (#17 through #20 with 17 and 18 required) is required if Number of Beneficiaries/Successor Owner > 01  
Group 3 (#21 through #24 with 21 and 22 required) is required if Number of Beneficiaries/Successor Owner > 02  
Group 4 (#25 through #28 with 25 and 26 required) is required if Number of Beneficiaries/Successor Owner > 03  
Group 5 (#29 through #32 with 29 and 30 required) is required if Number of Beneficiaries/Successor Owner > 04  
Group 6 (#33 through #36 with 33 and 34 required) is required if Number of Beneficiaries/Successor Owner > 05  
 
Group 1 will be required for Section 529 Accounts (Account= 1).  
A succeeding group must be submitted for each additional Beneficiary. 
At least one 529 Beneficiary (Beneficiary/Successor Owner Address [[Option]] = C) is required.  

---

## Page 22

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 22 
A Successor Owner (Beneficiary/Successor Owner Address [[Option]] = D) is required when the Successor 
Owner Indicator =1 and Account Type = 1 (indicating Section 529 Plan). A Successor Owner is not allowed if 
these two conditions are not met and no more than one Successor Owner is allowed.  
Beneficiary/Successor Owner Address [[Option]] = ‘C’ or ‘D’ are not allowed for Regular Account (Account Type = 
0).  
Sequences #13 through #16 are required if Number of Beneficiaries/ Successor Owner > 00.  
Sequence # 13 
Field Name Start End Len Type Description Opt/Req 
50/51 
Beneficiary/Successor 
Owner Address [[Option]]  
 
10 10 1 A/N A = Primary IRA Beneficiary  
B = Secondary IRA Beneficiary  
C = 529 Beneficiary  
D = 529 Successor Owner 
R/O 
Beneficiary/Successor 
Owner Date of Birth 
11 18 8 N mmddccyy R/O 
Beneficiary/Successor 
Owner U.S Citizenship 
Indicator 
19 19 1 A/N Required if Beneficiary/Successor Owner Address 
[[Option]] = “C‟ or “D‟.  
0 = U.S. citizen  
1 = Not U.S. citizen 
OC/C 
Beneficiary/Successor 
Owner SSN/EIN Number  
 
20 28 9 A/N Required if Beneficiary/Successor Owner Address 
[[Option]] = “C‟ or “D‟. 
OC/C 
Beneficiary/Successor 
Owner SSN/EIN Indicator  
 
29 29 1 A/N Required if Beneficiary/Successor Owner SSN/EIN 
Number is provided  
0 = Tax [[ID]] number  
1 = Social security number 
OC/C 
Beneficiary/Successor 
Owner Relationship 
Indicator  
 
30 30 1 A/N Required if Beneficiary/Successor Owner Address 
[[Option]] of “C‟ is provided  
1 = Spouse  
2 = Non-Relative 
 3 = Grandchild 
 4 = Relative 
5 = Child 
OC/C 
Beneficiary/Successor 
Owner Name End Line 
Indicator  
 
31 31 1 A/N Required if Beneficiary/Successor Owner 
Name/Address is provided  
1-4 = Line number where name ends 
OC/C 
Beneficiary/Successor 
Owner Zip Code  
 
32 42 11 A/N 5 digit Zip Code + 4 digit Zip-Four + 2 digits for 
future postal expansion. 
O/C 

---

## Page 23

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 23 
Field Name Start End Len Type Description Opt/Req 
50/51 
Date of Event  
(The date when the 
Beneficiary will enter 
College)  
43 50 8 N mmddccyy O/C 
 
Sequence # 14 – 16  
Sequence’s 14 – 16 contain fields for the “Beneficiary / Successor Owner” Name/Address. Sequence 14 & 16 
each contain to occurrences while sequence # 16 contains one for a total of 5 occurrences. As at least one 
beneficiary is required for each Section 529 account (Account Type = 1) the first “Beneficiary / Successor 
Owner Name/Address” is required. Each additional occurrence is optional. 
Field Name Start End Len Type Description Opt/Req 
Beneficiary/ Successor Owner 
Name/Address Line #1 
10 44 35 A/N  R/O 
Beneficiary/ Successor Owner 
Name/Address Line #2 
45 79 35 A/N  O/O 
 
 
Fields repeated in records 15 and 16 – Beneficiary/Successor Owner Name/Address #3 & 4 (10-44 & 45-79 
respectively) in sequence 15, Beneficiary/Successor Owner Name/Address #5 sequence # 16 (10- 44).  
Sequence # 16 (only) 
Field Name Start End Len Type Description Opt/Req 
Beneficiary/ Successor Owner 
City 
45 77 33 A/N  O/O 
Beneficiary/ Successor Owner 
State 
78 79 2 A/N  O/O 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 24

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 24 
[[Broker]]/Fund Account Conversion Records A/B/T52, F52 Sequence #1  
Transaction Type Field  
Note: 
Participants should communicate 529 transfers using the “In-Kind” [[Option]] found on Sequence #1 in the “Transfer Reason 
Code” field. 
Field Name Start End Len Type Description Opt/Req 
Transaction Type 25 25 1 A/N 1 = Sub-Account Credit  
2 = Transfer  
3 = Account Conversion / Update 
Acknowledgment  
4 = Mass [[Broker]] to [[Broker]] Conversion  
5 = Non-Networking Transfer  
6 = Change in [[Broker]]/Dealer - Change 
To B/D  
7 = Change in [[Broker]]/Dealer - Change 
From B/D  
8 = Non ACAT eligible transfer 
([[participant]] or [[CUSIP]] is not ACAT 
eligible) 
9 = ACAT Mutual Fund Fail Cleanup 
Transaction Type 6 or 7 allowed for 
Record Type F53 only. 
R/R 
529 Transfer Reason Code  
The 529 Transfer Reason Code field identifies, in the event of a transfer, the reason for the transfer.  
Field Name Start End Len Type Description Opt/Req 
529 Transfer Reason Code 92 92 1 A/N 1 = Owner - Resignation  
2 = Owner - Death 
3 = Owner - Divorce  
4 = Beneficiary Change – In Family  
5 = Beneficiary Change – Out of Family 
6 = In Kind  
7 = UGMA/UTMA (Age of Majority)  
 
O/O 
 

---

## Page 25

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 25 
IRS 529 Annual Strategy Change Counter  
The IRS recognizes that there are situations that may warrant a change in investment strategies for 529 
accounts. As such the IRS has designated that a plan is not in violation if there is a change in strategy. The 
“IRS 529 Strategy Change Counter” provides the means to identify annual changes in strategy. Participants 
should review their state website or contact the IRS for the limits on 529 strategy changes all owed. 
IRS 529 Annual Strategy Change Counter 
Field Name Start End Len Type Description Opt/Req 
IRS 529 Annual Strategy 
Change Counter 
93 93 1 A/N 0 thru 9 O/O 
 
Updated Fields on the [[Broker]]/Fund Account Conversion Records 
A/B/T52, F53 – Sequence #3  
December 7, 2009 changes required Sequence #3 be submitted when the “Transaction Type” field located on 
Record #1 equals “4 - Mass [[Broker]] to [[Broker]] Conversion” or “‘8 – 529 Rollover”. [[Option]] 8 (529 Rollover) has 
been eliminated (effective October 17, 2011). Therefore Sequence #3 will only be required when “Transaction 
Type” field is equal to “4 – Mass [[Broker]] to [[Broker]] Conversion”. (Participants should communicate 529 transfers 
by using the “In-Kind” [[Option]] found on Sequence #1 in the “Transfer Reason Code” field.)  
If Sequence #3 is missing for Transaction Type = 4 [[NSCC]] will reject that transaction using the following Reject 
Code:  
58 - Additional Input required for this transaction type. 
529 Rollover Required Fields – “Cost Basis Dollar Amount” & “Earnings to 
Date”  
The “Cost Basis Dollar Amount” and “Earnings to Date” fields were added to the [[Broker]] / Fund Account 
Conversion Records A/B/T52, F53 Sequence #3 to comply with 12/7/2009 changes. These were originally 
optional/conditional fields; however, due to the elimination of Transaction Type [[Option]] 8 (529 Rollover) for 
Networking files, the requirements for these fields have been changed to optional only. The new changes are 
effective October 17, 2011.  
Each field will be 16 bytes in length and in the following format: 99,999,999,999,999.99. Zeros will be allowed 
to be entered for each field. 
Field Name Start End Len Type Description Opt/Req 
Cost Basis Money Amount 53 68 16 N 99,999,999,999,999.99 O/O 
Earnings to Date Money 
Amount 
69 84 16 N 99,999,999,999,999.99 O/O 
 

---

## Page 26

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 26 
If an invalid value is input, [[NSCC]] will reject using new reject codes as follows:  
J6 - Cost Basis Money Amount missing/invalid  
J7 - Earnings to Date Money Amount missing/invalid  
Negative Earnings to Date Indicator  
The “Negative Earnings to Date Indicator” field is an optional field that identifies whether the Earning Amount is 
negative or positive. The valid value for this optional field is either “N” or a space (blank). It should be noted 
that the [[default]] for this field will be a space (blank) = Positive Earnings to Date. If this field is left blank, it will 
mean the Earnings to Date is a positive number. 
Field Name Start End Len Type Description Opt/Req 
Negative Earnings to Date 
Indicator 
85 85 1 A/N N = Negative  
Space = Positive 
O/O 
 
If an invalid value is entered in the “Negative Earnings to Date Indicator” field, [[NSCC]] will reject using the new 
reject codes below:  
J8 - Negative Earnings to Date Indicator invalid 
Activity Reporting Records Activity Detail F55 - Sequence # 2  
Two new fields have been added to the F55 Activity Detail record; the 529 Transfer Reason Code and the IRS 
529 Annual Strategy Change Counter. 
Field Name Start End Len Type Description Opt/Req 
529 Transfer Reason Code  
 
94 94 1 A/N 1 = Owner – Resignation  
2 = Owner - Death  
3 = Owner - Divorce  
4 = Beneficiary Change – In Family  
5 = Beneficiary Change – Out of Family  
6 = In Kind  
7 = UGMA/UTMA (Age of Majority) 
O 
IRS 529 Annual Strategy 
Change Counter 
95 95 1 A/N 0 thru 9 O 
 
If invalid values are populated for either of these fields a reject code will be generated by [[NSCC]] and the 
transaction will be rejected to the submitter. The respective reject codes are as follows:  
L8 - 529 Transfer Reason Code is Missing/Invalid  
L9 – IRS 529 Annual Strategy Change Counter is Missing/Invalid  

---

## Page 27

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 27 
Updated Activity Reporting Records Activity Detail F55 – Sequence #5  
Activity Reporting Records Activity Detail (F55) #5  
Field Name Start End Len Type Description Opt/Req 
Cost Basis Money Amount 49 64 16 N 99,999,999,999,999.99 
This field should be populated for 529 
accounts, when applicable. 
O 
Earnings to Date  Money 
Amount 
65 80 16 N 99,999,999,999,999.99 
This field should be populated for 529 
accounts, when applicable. 
O 
Negative Earnings to Date 
Indicator 
 
81 81 1 A/N N = Negative 
Space = Positive 
This field should be populated for 529 
accounts, when applicable. 
O 
 
 

---

## Page 28

CHAPTER 7 SECTION 529 QUALIFIED TUITION PROGRAMS FUND/SERV® AND NETWORKING 
SECTION 529 – QUALIFIED TUITION PROGRAMS-FOR NETWORKING 28 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 