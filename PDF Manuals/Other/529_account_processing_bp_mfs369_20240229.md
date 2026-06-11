---
title: "529 Account Processing Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/529_account_processing_bp_mfs369_20240229.pdf"
pages: 49
size: "3269.5 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# 529 Account Processing Best Practices

**Original File:** [529_account_processing_bp_mfs369_20240229.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/529_account_processing_bp_mfs369_20240229.pdf)  
**Category:** Other  
**Total Pages:** 49  
**File Size:** 3269.5 KB  

---

## Page 1

 
 
Fund/SERV® 
529 ACCOUNT PROCESSING BEST PRACTICES 
 
FEBRUARY 29, 2024 
 
 
 

---

## Page 2

529 Account Processing Best Practices 
Change History 2 
TABLE OF CONTENTS 
Change History ..................................................................................................................................................... 4 
Overview ............................................................................................................................................................... 5 
529 Account Set-Up Overview ............................................................................................................................ 6 
529 Registration Information .............................................................................................................................. 7 
Account Registration ........................................................................................................................................... 7 
Beneficiary/Successor/Owner Address Options ................................................................................................. 7 
Social Codes ....................................................................................................................................................... 7 
529 Best Practice for Registrations and Addresses ........................................................................................... 7 
Registration ....................................................................................................................................................... 7 
Address Information ........................................................................................................................................11 
529 Account Opening ........................................................................................................................................ 14 
Level 0/4 ...........................................................................................................................................................14 
Level 3 ..............................................................................................................................................................15 
Omnibus ............................................................................................................................................................16 
Contributions to 529 Plan Accounts ................................................................................................................ 17 
Rollover Contributions to 529 Plan Accounts ................................................................................................. 21 
Rollover Contributions ......................................................................................................................................21 
Investment Strategy Changes (Aka Exchanges) ............................................................................................ 25 
Overview ...........................................................................................................................................................25 
Processing Strategy Changes - Fund/SERV® Order Records 001 and 004 ...................................................25 
Processing Strategy Changes - Fund/SERV® Exchange Record 015 ............................................................25 
Omnibus ............................................................................................................................................................28 
529 Plan Account Maintenances ...................................................................................................................... 29 
Maintenance .....................................................................................................................................................29 
529 Plan Account Transfers - Networking ....................................................................................................... 32 
529 Transfer Reason Code ..............................................................................................................................32 
Potential Tax Implications .................................................................................................................................32 
Age-Based Plans ..............................................................................................................................................32 

---

## Page 3

529 Account Processing Best Practices 
Change History 3 
Networking Transfers – Change in Beneficiary ................................................................................................32 
529 AcCount Firm/Fund Transfers – Networking ........................................................................................... 36 
ACATS-Fund/SERV 529 Plan Account Transfers – Best Practices .............................................................. 39 
Basis and Earnings ............................................................................................................................................ 42 
529 Plan Account Redemptions ....................................................................................................................... 44 
Overview ...........................................................................................................................................................44 
Qualified ............................................................................................................................................................44 
Nonqualified ......................................................................................................................................................44 
Fund/SERV® Transaction Type Field ...............................................................................................................44 
IRA/529 [[liquidation]] Indicator Field: ..................................................................................................................45 
[[liquidation]] Indicator (CDSC Waivers) for 529 Accounts ..................................................................................45 
 
  

---

## Page 4

529 Account Processing Best Practices 
Change History 4 
CHANGE HISTORY 
Date Description 
02/29/2024 Document rebranded. 
02/02/2024 Added Best Practices for ACATS-Fund/SERV 529 account transfers (pp. 39-41) 
07/10/2020 Links corrected 
  

---

## Page 5

529 Account Processing Best Practices 
Overview 5 
OVERVIEW 
A 529 plan is a tax-advantaged savings plan designed to encourage saving for future college costs. 529 plans, 
legally known as “qualified tuition plans,” are sponsored by states, state agencies, or educational [[Institutions]] 
and are authorized by Section 529 of the Internal Revenue Code. Investment options often include [[Stock]] 
[[Mutual Funds]], bond [[Mutual Funds]], and money market funds, as well as, age-based portfolios that automatically 
shift toward more conservative investments as the beneficiary gets closer to college age.  
Historically, many new 529 accounts were set up with the mailing of a physical application to the 529 program. 
This labor-intensive, paper-based process does not meet current industry standards for automated account 
set-up and trade [[settlement]]. Most accounts are held off-book, resulting in greater operational overhead and 
unrealized improvements in client service. 
Since 2010, [[NSCC]] Fund/SERV® and Networking systems have supported the automation of 529 account 
processing. 
Industry participants from the ICI BDAC 529 Task Force have documented Best Practices for 529 account 
processing. This document provides those “Best Practices” associated with Fund/SERV
® and Networking 
capabilities. 
The scope of these best practices covers Level 0/4, Level 3 and Omnibus accounts.  

---

## Page 6

529 Account Processing Best Practices 
529 Account Set-Up Overview 6 
529 ACCOUNT SET-UP OVERVIEW 
A new account can be established with or without an initial purchase. If an initial purchase is processed 
through Fund/SERV®, a full registration (401) is required (Omnibus accounts excluded). A registration, full or 
short, is not allowed on subsequent transactions. 
[[NSCC]] file layouts in Fund/SERV® incorporate 529 new account requirements including registration type, 
citizenship indicators, beneficiary relationship indicators, beneficiary/successor address fields, age based roll 
exempt indicator and successor owner indicator. Key fields required for full disclosure include Account O wner 
SSN/EIN and Date of Birth and Beneficiary SSN/EIN, Address and Date of Birth. 
Accounts without funding can be established via a B50 Networking transaction.  In order to provide proper 
recordkeeping and transparency, all accounts should be fully disclosed between Firms and Funds utilizing the 
Networking Account Conversion/Update/Transfer and Omni/SERV Position and Activity records.  
Each state sets a contribution limit for its 529 plan. Firms must monitor contribution levels in their client 
accounts to ensure maximum limits are not violated. Additionally, Firms and Funds will need to share 529 
account information across beneficiaries for each state’s plans. For this reason and others, Beneficiary SSN is 
a required field on 529 registration and initial and subsequent orders. 
 

---

## Page 7

529 Account Processing Best Practices 
529 Registration Information 7 
529 REGISTRATION INFORMATION 
Account Registration 
Registration Type values: 
• 0 = Regular Registration 
• 1 = Section 529 Registration 
Beneficiary/Successor/Owner Address Options 
• C = 529 Beneficiary 
• D = 529 Successor Owner 
Social Codes 
[[NSCC]] Social Codes drive the type of 529 account. Each account type requires a unique set of attributes. Not 
all account types are offered by all 529 programs. Please refer to your specific program(s) for available account 
types. Social Code List is available in the Mutual Fund Services section in the Learning Center:   
https://dtcclearning.com/products-and-services/mutual-fund-services/codes.html 
529 Best Practice for Registrations and Addresses 
Registration 
Below are examples of the suggested best practices for account registrations:  
• List plan name in first line of registration 
• List Account Owner in next line of registration  
• Include appropriate registration in statements 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 8

529 Account Processing Best Practices 
529 Registration Information 8 
It is possible that a registration may vary from the suggested best practice depending on a Firm  or Fund's 
business practices. Funds and Firms are strongly encouraged to discuss registration formats prior to use of 
[[NSCC]]’s 529 functionality. 
Social 
Code 
Description Registration Type Required Format Example 
37 Section 529 Plan - 
Qualified State Tuition 
Program 
Standard Registration Sponsor/Plan Name AZCP/Mythical Plan 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
Authorized Person Registration Sponsor/Plan Name AZCP/Mythical Plan 
Authorized Person John Doe AUTH Person 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
Guardian Registration Sponsor/Plan Name AZCP/Mythical Plan 
Guardian John Doe Guardian 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
38 UGMA/UTMA transferred 
into Section 529 Plan  
Single Custodian UGMA Sponsor/Plan Name AZCP/Mythical Plan 
Custodian Name John Doe CUST 
Beneficiary FBO Jane Doe 
Condition (Optional) MS/UGMA Until Age 21 
Single Custodian UTMA Sponsor/Plan Name AZCP/Mythical Plan 
Custodian Name John Doe CUST 
Beneficiary FBO Jane Doe 
Condition (Optional) VA/ UTMA Until Age 18 
Multiple [[Custodians]] UTMA Sponsor/Plan Name AZCP/Mythical Plan 
Custodian Name John Doe CUST 
Custodian Name OR Jane Doe CUST 
Beneficiary FBO Jane Doe 
Condition (Optional) TN/ UTMA Until Age 21 
39 Section 529 Plan 
transferred into new 
Section 529 Plan 
Standard Registration Sponsor/Plan Name AZCP/Mythical Plan 
Account Owner Jane Doe Owner 

---

## Page 9

529 Account Processing Best Practices 
529 Registration Information 9 
Social 
Code 
Description Registration Type Required Format Example 
Beneficiary FBO Jane Doe 
Authorized Person Registration Sponsor/Plan Name AZCP/Mythical Plan 
Authorized Person John Doe AUTH Person 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
Guardian Registration Sponsor /Plan Name AZCP/Mythical Plan 
Guardian John Doe Guardian 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
40 IRA transferred into 
Section 529 Plan 
Standard Registration Sponsor/Plan Name AZCP/Mythical Plan 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
Authorized Person Registration Sponsor/Plan Name AZCP/Mythical Plan 
Authorized Person John Doe AUTH Person 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
Guardian Registration Sponsor /Plan Name AZCP/Mythical Plan 
Guardian John Doe Guardian 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
41 Series E/Series I U.S. 
Saving [[Bonds]] 
transferred into Section 
529 Plan 
Standard Registration Sponsor/Plan Name AZCP/Mythical Plan 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
Authorized Person Registration Sponsor/Plan Name AZCP/Mythical Plan 
Authorized Person John Doe AUTH Person 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 

---

## Page 10

529 Account Processing Best Practices 
529 Registration Information 10 
Social 
Code 
Description Registration Type Required Format Example 
Guardian Registration Sponsor /Plan Name AZCP/Mythical Plan 
Guardian John Doe Guardian 
Account Owner Jane Doe Owner 
Beneficiary FBO Jane Doe 
61 Section 529 Plan - Joint 
Owner 
Joint Owner Sponsor/Plan Name AZCP/Mythical Plan 
Account Owner John Doe 
Account Owner AND Jane Doe 
Beneficiary FBO Jack Doe 
62 Section 529 Plan - Trust Single Trustee Sponsor/Plan Name AZCP/Mythical Plan 
Trustee Name John Doe TTEE 
Trust Name  Doe Family Trust 
Beneficiary  FBO Jane Doe 
Multiple Trustees Sponsor/Plan Name AZCP/Mythical Plan 
Authorized Person John & Jill Doe TTEES 
Account Owner Doe Family Trust 
Beneficiary FBO Jane Doe 
67 Section 529 Plan - Entity  Entity Registration 
(Beneficiary Not Named) 
Sponsor/Plan Name AZCP/Mythical Plan 
Entity Name ABC Scholarship Fund 
Entity Registration  
(Beneficiary Named) 
Sponsor/Plan Name AZCP/Mythical Plan 
Entity Name ABC Scholarship Fund 
Beneficiary Name FBO Jane Doe 
68 Section 529 Plan – 
Corporate 
Corporation Registration 
(Beneficiary Not Named) 
Sponsor/Plan Name AZCP/Mythical Plan 
Corporate Name ABC Inc. 
Entity Registration 
(Beneficiary Named) 
Sponsor/Plan Name AZCP/Mythical Plan 
Entity Name ABC Inc. 
Beneficiary Name FBO Jane Doe 
 

---

## Page 11

529 Account Processing Best Practices 
529 Registration Information 11 
 
Address Information 
Address information is required for account owner and beneficiary, but optional for successor owner 
(Identifying successor owner may be optional in some plans). 
Entity Account Type Required Information 
Account Owner 
 
 
 
 
 
 
Individual Owner 
Social Code 37 
Social Code 39 
Social Code 40 
Social Code 41 
Name of Owner 
Physical Address 
Social Security Number 
Date of Birth 
Citizenship (US or Resident Alien) 
 
UGMA/UTMA 
Social Code 38 
Name of Custodian 
Physical Address 
Social Security Number 
Date of Birth 
 
Individual Owner    
(Transferred 
from 529) 
Social Code 39 
Name of Owner 
Physical Address 
Social Security Number 
Date of Birth 
Citizenship (US or Resident Alien) 
 
Individual Owner   
(Transferred 
from IRA) 
Social Code 40 
Name of Owner 
Physical Address 
Social Security Number 
Date of Birth 
Citizenship (US or Resident Alien) 
 
Individual Owner  
(Transferred 
from Savings 
[[Bonds]]) 
Social Code 41 
Name of Owner 
Physical Address 
Social Security Number 
Date of Birth 
Citizenship (US or Resident Alien) 
 
Individual Owner Attributes plus: 

---

## Page 12

529 Account Processing Best Practices 
529 Registration Information 12 
Entity Account Type Required Information 
Joint Owner 
Social Code 61 
Name of Joint Owner 
Physical Address 
Social Security Number 
Date of Birth 
 
Trust Account 
Social Code 62 
Trust Name 
Date of Trust 
Tax [[ID]] of Trust 
Physical Address 
 
Entity Account 
Social Code 67 
Name of Entity (University, Foundation, Scholarship Fund, etc.) 
Physical Address 
Taxpayer [[ID]] 
 
Corporate 
Account 
Social Code 68 
Name of Organization 
Physical Address 
Taxpayer [[ID]] 
Indication of 501(c)(3)-[[default]] to non-501(c)(3) 
 
Beneficiary 
(Only one per 529 
account) 
Name 
Physical Address 
Social Security Number 
Date of Birth 
Beneficiary Relationship to Account Owner 
  
Successor Owner 
(Optional) 
Name 
Physical Address 
Social Security Number 
Date of Birth 
 
Financial Advisor Firm 
Branch Number 
Advisor [[ID]] Number 
Indicator of Funding from: 

---

## Page 13

529 Account Processing Best Practices 
529 Registration Information 13 
Entity Account Type Required Information 
Source of 529 
Funding 
UGMA/UTMA transferred into Section 529 Plan (Social Code 38) 
Section 529 Plan transferred into new Section 529 Plan (Social Code 39) 
IRA transferred into Section 529 Plan (Social Code 40) 
Series E/Series I U.S. Saving [[Bonds]] transferred into Section 529 Plan (Social Code 41) 
 
 
 
 

---

## Page 14

529 Account Processing Best Practices 
529 Account Opening 14 
529 Account Opening 
The following scenarios and charts outline the recommended steps to opening 529 accounts based on whether 
the accounts are networked or held in omnibus positions. 
Level 0/4 
Level 0 positions can be opened directly at the Fund with an associated Firm. These accounts are established 
on the Fund’s specific account application criteria. As illustrated below, they are also opened at the Firm with a 
mutual fund order and registration through Fund/SERV®. Level 4 positions are similar in nature and are 
serviced by the Fund. 
Scenario: Client wishes to open a 529 account at the Firm. The Firm initiates the order record (001) 
and the registration (401) setting the account at network level 0. 
  
 
Figure 1 Account Opening - Level 0/4 

---

## Page 15

529 Account Processing Best Practices 
529 Account Opening 15 
Level 3 
Level 3 accounts are opened and maintained by the Firm and the Firm performs all shareholders accounting 
and servicing. Accounts transferred from Fund to Firm will be addressed in the 529 Plan Account 
Maintenances section. 
Scenario: Client wishes to open a brokerage 529 account. The Client completes a 529 brokerage 
application. The advisor establishes the 529 account on the Firm’s brokerage system. The brokerage 
system establishes a new account using a Fund/SERV® 401 record. The initial contribution is 
processed using the Fund/SERV® 001 order record. 
 
Figure 2 Account Opening - Level 3 
  


---

## Page 16

529 Account Processing Best Practices 
529 Account Opening 16 
Omnibus 
In an omnibus environment, accounts are opened and maintained by the Firm, with the Firm performing all 
shareholder servicing options. In a 529 omnibus environment, the specific Fund/Firm agreement may alter the 
traditional service model. Aggregate orders are placed in Firm name (master account) and the Firm sub-
accounting system provides trade information at the client account level. 
To be fully disclosed, Omni/SERV Activity files must be provided to the Fund daily. Omni/SERV Position files 
should be sent monthly or at another mutually agreed upon interval. 
Scenario: Client wishes to open a brokerage 529 account. The Client completes a 529 brokerage 
application. The advisor establishes the 529 account on the Firm’s sub-accounting system. The 
[[Broker]]/dealer combines all client contributions and makes an aggregate investment in the omnibus 
account using a Fund/SERV® 001 order record. 
 
Figure 3 Account Opening - Omnibus 


---

## Page 17

529 Account Processing Best Practices 
Contributions to 529 Plan Accounts 17 
CONTRIBUTIONS TO 529 PLAN ACCOUNTS 
Each state sets a contribution limit for its 529 plan. Firms must monitor contribution levels in their client 
accounts to ensure maximum limits are not violated. Additionally, Firms and Funds will need to share 529 
account information across beneficiaries for each state’s plans. For this reason and others, Beneficiary SSN is 
a required field on 529 registration and initial and subsequent orders. 
When submitting contributions using the Fund/SERV® 001 order record, Firms are required to indicate the type 
of contribution made to a 529 account by populating the [[Asset]] Type Indicator field with one of the following 
values: 
• D = 529 Current Year Contribution 
• P = 529 Previous Year Contribution 
• Q =529 Rollover Contribution 
• U = 529 In-State Plan Transfer Contribution 
• V = 529 Owner Change 
• W = 529 Beneficiary Change In-Family 
 
Note:  
[[Asset]] Type Indicators Q, U, V, and W require ‘Beneficiary SSN/EIN Number’, ‘Cost Basis Money Amount’ and ‘Earnings to 
Date Money Amount’ fields on the Fund/SERV® 001 order record. 
 
 
The intent of this section is to provide some examples of fields necessary to address 529 contribution 
processing. However, there are a number of fields required for all purchase trades. In order  to see all fields and 
values necessary, please reference the Mutual Fund Fund/SERV® record layouts: 
https://dtcclearning.com/products-and-services/mutual-fund-services/record-layouts.html 
Reject Code ‘750 = 529 – Over Investment’ should be utilized when a contribution is rejected by the Fund due 
to a Subsequent contribution exceeding the 529 plan’s contribution limit. 
 
A full list of Fund/SERV® reject codes are available on the Learning Center: 
https://dtcclearning.com/products-and-services/mutual-fund-services/codes.html 
 
  

---

## Page 18

529 Account Processing Best Practices 
Contributions to 529 Plan Accounts 18 
 
Figure 4 Subsequent Contributions - Level 0/4 


---

## Page 19

529 Account Processing Best Practices 
Contributions to 529 Plan Accounts 19 
 
 
Figure 5 Subsequent Contributions - Level 3 


---

## Page 20

529 Account Processing Best Practices 
Contributions to 529 Plan Accounts 20 
 
Figure 6 Subsequent Contributions - Omnibus 
 


---

## Page 21

529 Account Processing Best Practices 
Rollover Contributions to 529 Plan Accounts 21 
ROLLOVER CONTRIBUTIONS TO 529 PLAN ACCOUNTS 
Rollover Contributions 
IRS: Any amount distributed from a Qualified Tuition Plan (QTP) is not taxable if it is rolled over to another QTP 
for the benefit of the same beneficiary or for the benefit of a [[Member]] of the beneficiary's family (including the 
beneficiary's spouse). An amount is considered rolled over if it is paid to another QTP within 60 days after the 
date of the distribution. 
Rollovers can occur in the form of moving assets from one qualified tuition plan to another, or in the case of a 
simultaneous change in registration. While Rollovers can normally occur only once within a rolling 12- month 
period, the account created as a result of processing a 529 Owner Change or 529 Beneficiary Change In-
Family Contribution would not be subject to this restriction. 
Rollover into a new account would require a Fund/SERV® 401 record be created. 
Rollover contributions can utilize the Fund/SERV® order (001,004) record with appropriate [[Asset]] Type 
indicator: 
• [[Asset]] Type Indicator Q = 529 Rollover Contribution 
 
When selected, two fields will be required to facilitate preparation of shareholder’s tax reporting:  
• Field Name: Cost Basis Money Amount 
• Field Name: Earnings to Date Money Amount 
 
Best practice: When the rollover is processed from an outside Fund/Firm, the delivering Fund/Firm is 
responsible for providing the client/receiving Firm with Cost Basis and Earnings.  
Scenario: Client with 529 account (same beneficiary) at Firm has rollover check in possession with 
cost basis and earnings information. 
Execute Fund/SERV® trade (001, [[Asset]] Type Indicator Q = 529 Rollover Contribution) on existing account with 
accompanying 529 requirements including Basis and Earnings fields (Cost Basis Dollar Amount and Earnings 
to Date Dollar Amount). 
Scenario: Client with 529 account at Firm (same beneficiary) has rollover check in possession without 
basis and earnings information. 
Execute Fund/SERV® trade (001) with accompanying 529 requirements, pending a correction when Basis and 
Earnings is received. 
In cases where all data is not present, especially Cost Basis and Earnings, missing data must be provided as 
soon as possible. In the absence of Cost Basis and Earnings data, the [[default]] is 100% earnings.  Firms should 
pursue accurate information from client and/or prior program and, upon receipt of Cost Basis and Earnings a 
correction to the Basis and Earnings associated with the shareholder’s rollover should be made on the Firm’s 
system. 
The rollover contribution process follows the same [[BASIC]] steps as a regular contribution but with the [[Asset]] 
Type Indicator = Q (529 Rollover Contribution) and additional requirements of data fields Cost Basis Money 
Amount and, Earnings to Date Money Amount, and Negative Earnings to Date Indicator (if any). 
Best Practice: All confirmations sent to client for rollover contributions should include Cost Basis Money 
Amount, Earnings to Date Money Amount, and Negative Earnings to Date (if any).  

---

## Page 22

529 Account Processing Best Practices 
Rollover Contributions to 529 Plan Accounts 22 
 
 
Figure 7 Rollover Contributions - Level 0/4 


---

## Page 23

529 Account Processing Best Practices 
Rollover Contributions to 529 Plan Accounts 23 
 
 
Figure 8 Rollover Contributions - Level 3 


---

## Page 24

529 Account Processing Best Practices 
Rollover Contributions to 529 Plan Accounts 24 
 
Figure 9 Rollover Contributions - Omnibus 
 
 


---

## Page 25

529 Account Processing Best Practices 
Investment Strategy Changes (Aka Exchanges) 25 
INVESTMENT STRATEGY CHANGES (AKA EXCHANGES) 
Overview 
Per IRS [[regulation]], an Investment Strategy Change may not occur more frequently than the IRS limit per 
calendar year with the exception of multiple investment [[Option]] changes occurring at the same time a change is 
made to the designated beneficiary of the account. 
An Investment Strategy change results in a change in the portfolio mix under the same registration. Changes in 
investment strategy are recorded and counted by the record holder of the account and reported daily via the 
529 Aggregation file.  When 529 assets are transferred between record holders, it is incumbent upon contra 
parties to inform the recipient of the account how many strategy changes have been executed within current 
calendar year using the IRS 529 Annual Strategy Change Counter field in the Networking F53 and F55 
records. 
Reject Code 751 = Exchange Exceeds IRS Strategy Change Limit should be leveraged when a Fund is 
rejecting due to Investment [[Option]] Changes Exceeding the IRS limit per calendar year.   
Processing Strategy Changes - Fund/SERV® Order Records 001 and 004 
[[Asset]] Type Indicator U (529 In-State Plan Transfer Contribution) is to be used when an owner moves assets 
between plans within the same state and the state considers this contribution a strategy change instead of a 
rollover: 
Scenario: Account Owner transfers assets from a direct-sold plan to a [[Broker]]/advisor sold plan in the 
same state. Cash moves from the direct-sold plan in a check. The Firm/Fund deposits the check into a 
Security Issue [[ID]] of the receiving plan and sends an ‘in-state’ plan transfer contribution. If the state 
counts the in-state plan transfer on the inbound plan as a strategy change, then monitor the 
contribution as a strategy change. 
Note:  
Cost Basis Money Amount and Earnings to Date Money Amount fields are required when executing trades via 
Funds/SERV with [[Asset]] Type Indicator U. 
Transaction Type E (529 In-State Plan Transfer Distribution) is to be used when an owner moves assets 
between plans in the same state and the state considers this distribution a strategy change.  
Scenario: Account Owner transfers assets from a direct-sold plan to a [[Broker]]/advisor sold plan in the 
same state. Cash moves from the direct-sold plan in a check. The delivering Firm/Fund sends an ‘in-
state’ plan transfer distribution to the receiving plan for the same owner/beneficiary. If the state counts 
the in-state plan transfer on the outbound plan as a strategy change, then monitor the distribution as a 
strategy change. 
Notes: 
• [[Asset]] Type Indicator ‘G = Share Class Conversion’ is NOT considered a Strategy Change. 
• Systematic withdrawals and contributions (Program Transaction Indicator field ‘1 = Systematic Withdrawal Plan 
(SWP)’ or ‘3 = Systematic Contribution (SIP/PAC/PIP) are NOT considered Strategy Changes. 
 
Processing Strategy Changes - Fund/SERV® Exchange Record 015 
Exchanges involve a redemption and a purchase. Typically, Fund/SERV® Exchange Order (015) 
accommodates this transaction but can be processed as separate [[liquidation]] and purchase Orders (001).  
 

---

## Page 26

529 Account Processing Best Practices 
Investment Strategy Changes (Aka Exchanges) 26 
Strategy change Transaction Types for Exchange Record 015 are: 
• 6 = Exchange to new account 
• 7 = Exchange to existing account 
 
Notes: 
Share Class Conversions (Transaction Types C and D) are NOT considered Strategy Changes 
 
Figure 10 Exchange Investment Strategy Change) - Level 0/4 


---

## Page 27

529 Account Processing Best Practices 
Investment Strategy Changes (Aka Exchanges) 27 
 
Figure 11 Exchange Investment Strategy Change) - Level 3 
 
For Level 3 accounts, The Firm or Fund is carrying the Investment Change Counter on the Firm ’s or TA’s 
system and should follow Best Practices as follows: 
• Ensure the Investment Change Counter follows current IRS rules (rules have changed i n past years) 
• Counter should be checked systematically or manually before order is placed  
• Counter should be adjusted with each order processed 
Exchanges in excess of the IRS strategy change limit per calendar year must be processed as an Owner 
Non-qualified withdrawal and new contribution.  
Note: 
Reject Code ‘751 = 529 – Over Investment’ should be utilized if investment [[Option]] changes exceed the IRS limit per 
calendar year. 
 
• Differentiate between systematic exchanges and one-off exchanges for the purpose of investment 
strategy changes. 
 
 If the systematic exchange agreement is established as part of the initial establishment of an 
account, the agreement will NOT be counted towards the Investment Change Counter.  
 
 The subsequent establishment or modification of a systematic exchange to an existing account 
agreement WILL be counted towards the Investment Change Counter. 


---

## Page 28

529 Account Processing Best Practices 
Investment Strategy Changes (Aka Exchanges) 28 
 The repeated execution of an existing systematic exchange agreement will NOT be counted 
towards the Investment Change Counter. 
 
 Age-based and Years-to-enrollment based exchanges are not counted towards the Investment 
Change Counter. 
Omnibus 
The Firm records and monitors Investment Strategy Changes in its sub-accounting system and/or brokerage 
system. 
Best Practice: Omnibus Firms may bulk exchanges within master accounts. The Firm must send daily activity 
file to Firm reflecting exchange transactions including Annual Strategy Change Counter.  
 
Figure 12 Exchange Investment Strategy Change) - Omnibus 


---

## Page 29

529 Account Processing Best Practices 
529 Plan Account Maintenances 29 
529 PLAN ACCOUNT MAINTENANCES 
Maintenance 
The following changes to the 529 account can be conducted via a Networking B51:  
• BIN - [[Broker]] Identification Number 
• Matrix level (Level 0/4 to Level 0/4 only) 
• Branch code 
• Rep code (Rep name or Rep #) 
• Change of Successor Owner information 
• Address 
• Owner/Beneficiary Name* 
Note 
* Owner and beneficiary changes must be done via transfer process. However, minor repairs to correct name may be 
allowed 
 
Figure 13 Account Maintenance - Level 0/4 


---

## Page 30

529 Account Processing Best Practices 
529 Plan Account Maintenances 30 
 
Figure 14 Account Maintenance - Level 3 


---

## Page 31

529 Account Processing Best Practices 
529 Plan Account Maintenances 31 
 
Figure 15 Account Maintenance - Omnibus 


---

## Page 32

529 Account Processing Best Practices 
529 Plan Account Transfers - Networking 32 
529 PLAN ACCOUNT TRANSFERS - NETWORKING 
Networking transfers are typically executed to change registration on an account. The Best Practice regarding 
529 accounts is to close the old and open a new account to facilitate Owner and/or Beneficiary changes.  
This can be completed using the B50 and B52 records below: 
529 Transfer Reason Code 
• 1 = Owner – Resignation 
• 2 = Owner – Death 
• 3 = Owner – Divorce 
• 4 = Beneficiary Change – In family 
• 5 = Beneficiary Change – Out of Family 
• 6 = In Kind 
• 7= UGMA/UTMA (Age of Majority) 
 
Best Practice: Of the seven 529 Transfer Reason Codes, all but 529 Transfer Reason Code “6 = In Kind,” are 
transfer codes related to changing either the Account Owner or Beneficiary information. It is recommended that 
these be completed via a B50/B52 transfer to facilitate proper books and records for tax and other purposes.  
The IRS 529 Account Strategy Change Counter field should only be populated when transferring accounts 
using 529 Transfer Reason Code “6 (In Kind)” as all other transfer types will result in the resetting of the 
Annual Strategy Change Counter.   
Potential Tax Implications 
While the tax responsibility rests with the account owner and/or beneficiary, it is a best practice to be aware of 
differences in transfer options and how they might affect the client. Consideration given to how transfers are 
processed should include 1099Q impact. Generally, a change of beneficiary in current beneficiary’s family 
creates no negative treatment. However, a change in beneficiary to an individual outside of the current 
beneficiary’s family may result in a tax-reportable transaction. 
Age-Based Plans 
When changing a beneficiary within an age-based plan, it may be necessary to align Security Issue [[ID]] to the 
age of the new beneficiary. Firms’ systems should make beneficiary changes in the existing Security Issue [[ID]] 
and subsequently roll assets to the proper Security [[ID]]. This migration process should not affect a client's 
annual strategy change. 
Networking Transfers – Change in Beneficiary 
Following are examples of best practices for change in beneficiary (529 Transfer Reason Code = 4 or 5) 
transfers: 

---

## Page 33

529 Account Processing Best Practices 
529 Plan Account Transfers - Networking 33 
 
Figure 16 Account Transfer - Level 0/4 
When a transfer is affected, the Fund should send Record Type F53 to acknowledge the transfer request and an 
F55 Activity record to the Firm indicating the closing balance on the account was transferred. Both records should 
contain the same value in the Strategy Change Counter field.  


---

## Page 34

529 Account Processing Best Practices 
529 Plan Account Transfers - Networking 34 
 
Figure 17 Account Transfer - Level 3 


---

## Page 35

529 Account Processing Best Practices 
529 Plan Account Transfers - Networking 35 
 
Figure 18 Account Transfer – Omnibus 
 


---

## Page 36

529 Account Processing Best Practices 
529 AcCount Firm/Fund Transfers – Networking 36 
529 ACCOUNT FIRM/FUND TRANSFERS – NETWORKING 
Accounts can be moved Firm to Fund and Fund to Firm (529 Transfer Reason Code = 6). Important to the 
process is the transferring of client account data, especially Basis and Earnings and Strategy Change Counter.  
 
Level 0 to Level 3 (Fund to Firm Automated) 
Accounts can transfer-in-kind between network levels (including omnibus) manually and automatically via B52.  
 
Figure 19 Automated Account Transfer - Level 0 to Brokerage 


---

## Page 37

529 Account Processing Best Practices 
529 AcCount Firm/Fund Transfers – Networking 37 
 
Figure 20 Manual Account Transfer - Level 0 to Brokerage 


---

## Page 38

529 Account Processing Best Practices 
529 AcCount Firm/Fund Transfers – Networking 38 
 
Figure 21 Account Transfer - Brokerage to Level 0 
  


---

## Page 39

529 Account Processing Best Practices 
ACATS-Fund/SERV 529 Plan Account Transfers – Best Practices 39 
ACATS-FUND/SERV 529 PLAN ACCOUNT TRANSFERS – 
BEST PRACTICES 
ACATS-Fund/SERV 529 transfers are typically utilized for Firm-to-Firm transfers when there is a change of 
dealer, or for PTF transfers (Firm to Fund/Fund to Firm). 529 account transfers initiated through ACATS 
must utilize the JSON (API and MQ) messaging format.1   
• When a 529 account transfer is initiated through an ACATS Transfer Input (TI) message, the ‘Original 
Receiver Customer Account Type’ value should be populated with a 5P (signifying the account is a 529 
plan), which will subsequently require the 529 account ‘Cost Basis Money Amount’ and the ‘IRS 529 
Strategy Change Counter’ data elements be included in the ACATS AT (Account Transfer) message 
from the delivering Firm.   
• When the deliverer of a 529 ACATS receives the TI message from the receiver, the best practice is to 
ensure the account owner social security number, beneficiary social security number, and registration 
matches.   
o If either of the social security numbers [[DO]] not match, the best practice is to reject the TI record 
using TI reject 01 (SSN/Tax [[ID]] mismatch).   
o If the registration does not match, the best practice is to reject the TI record using TI reject 02 
(Account Title Mismatch).  
• The ‘Earnings to Date Money Amount’ and ‘Negative Earnings to Date Indicator’ are optional on the AT 
message and should be populated by the delivering Firm if the information is available.  529 account 
data elements provided on the AT message will be included in the ACATS Transfer (018) record sent 
to the Fund.   
• Funds should populate the ACATS Transfer Acknowledgement/Rejection (019) record with the 529 
account data elements provided on the ACATS Transfer (018) record, which will be included in the 
ACATS Fund/SERV Statistics output file via MQ JSON messaging.  If the information is not provided 
on the 019 record, [[NSCC]] will not reject the 019 record.  
o For an ACATS PTF Fund-to-Firm transfer (i.e., pulled from Firm) where the Fund holds the 529 
account information, the Fund should supply the relevant 529 account data elements on the 
ACATS Transfer Acknowledgement/Rejection (019) record. 
o For an ACATS PTF Firm-to-Fund transfer (i.e., pushed to Fund) where the Firm holds the 529 
account information, the Firm should supply the relevant 529 account data elements on the AT 
message, which will be included on the ACATS Transfer (018) record. 
 
• Daily accrual amounts will not move with the 529 ACATS positions.  Similar to mutual fund [[shares]] 
through ACATS there are three methodologies to deliver the residual accrual money.  The accrual 
money can be delivered to the receiving Firm in the form of cash, the money can be reinvested and 
delivered to the receiving Firm in the form of [[shares]], or by Residual Credit (RCR) through ACATS. 
• Passing data to the 529 plan’s aggregator is critical.  To ensure data is consistently supplied and not 
duplicated, the best practice is for the resigning Firm to be responsible to pass data to the plan’s 
aggregator up to and including the date the ACATS posts to the Fund/SERV Statistics file. The 
receiving Firm will assume responsibility for passing data to the plan’s aggregator beginning on the 
next business day. 
 
1 For additional information on the ACATS JSON and MQ messaging format and requirements, please visit the ‘Client Interface 
Modernization and ACATS 529 Plan’ section of the ACATS Project Page  on [[DTCC]] Learning. 
 

---

## Page 40

529 Account Processing Best Practices 
ACATS-Fund/SERV 529 Plan Account Transfers – Best Practices 40 
 
 
 
 
The following workflow depicts the transfer process with the 529 account data elements for a F irm-to-
Firm transfer.  For additional transfer scenarios, including PTF 529 Account Transfers,  please visit the 
‘Client Interface Modernization and ACATS 529 Plan’ section of the ACATS Projects page on [[DTCC]] 
Learning. 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
Important Notes: 
• The ACATS 529 account data elements (IRS Strategy Change Counter, Cost Basis Money 
Amount, Earnings to Date Money Amount, and Negative Earnings to Date Indicator) are only 
supported in the JSON API and MQ messaging format.   
o Firms must leverage the JSON API or MQ format for 529 account transfers. 
o Firms will not be able to submit or receive 529 account transfers in the legacy fixed and 
variable file formats. 
 
• 529 account data elements provided by Firms on the ACATS AT message  (JSON API or MQ) 
will be included on the ACATS Transfer (018) record to Funds.  
 
• Funds will continue to receive  the ACATS Account Transfer (018) record and submit the 
ACATS Transfer Acknowledgement/Rejection (019) record,  through the existing fixed or 
variable record formats. The new ACATS JSON messaging formats only apply to Firms.  
 
 
 

---

## Page 41

529 Account Processing Best Practices 
ACATS-Fund/SERV 529 Plan Account Transfers – Best Practices 41 
ACATS-Fund/SERV: Firm to Firm 529 Account Transfer 
Party Request Day Review Day Set Prep [[settlement]] Day [[settlement]] Day + 1 
Firm A - 
Receiver 
 
 
 
 
AT data 
 
  
[[NSCC]] 
 
 
TI data 
 
AT data 
  
  
Firm B – 
Deliverer 
 
 
 
 
 
TI data 
 
 
   
Fund 
 
 
    
TI (Transfer Input) data 
submitted via JSON 
messaging (API or MQ) with 
the ‘Original Receiver 
Customer Account Type’ field 
value = 5P, signifying the 
account is a 529 plan. 
FR (Fund Registration) 
data submitted via JSON 
messaging (API or MQ). 
Fund/SERV 018 
Registration record in 
legacy (fixed/variable) 
format, inclusive of 529 data 
elements provided on the 
AT message.  
AT ([[Asset]] Transfer) data 
submitted via JSON messaging 
(API or MQ), including the 
following 529 data elements: 
• IRS Annual Strategy 
Change Counter (required) 
• Cost Basis Money Amount 
(required) 
• Earnings to Date Money 
amount (if available) 
• Negative Earnings to Date 
indicator (if available) 
Fund/SERV 018 Registration 
record (fixed/variable) format, 
inclusive of 529 data elements 
provided on the AT message.  
Fund/SERV 019 
Acknowledgement record 
(fixed/variable) format, 
inclusive of 529 data 
elements provided on the 
018 Record.  
Fund/SERV 
Stats File, 
inclusive of 529 
data elements 
provided on the 
019 record, via 
JSON MQ 
Messaging. 
529 Aggregation 
File (B/F 10) 
(transferred - 
[[shares]] Included)  
529 
Aggregation 
File (B/F 10) 
(transferred -
[[shares]] 
Removed) 
529 Master 
Aggregation 
File (G12) 
(from Fund or 
Fund’s 
Master 
Aggregator) 
Fund or 
Fund’s 
Master 
Aggregator 

---

## Page 42

529 Account Processing Best Practices 
Basis and Earnings 42 
BASIS AND EARNINGS 
Basis and earnings must be calculated on most 529 redemption and transfer transactions. When calculating 
the principal portion of a redemption, the following equation is used: 
𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅 ∗ �𝑇𝑇𝑅𝑅𝑅𝑅𝑇𝑇𝑇𝑇 𝑁𝑁𝑅𝑅𝑅𝑅 𝑃𝑃𝑃𝑃
𝑅𝑅𝑅𝑅𝑃𝑃𝑅𝑅
𝑅𝑅𝑇𝑇𝑇𝑇
𝑇𝑇𝑅𝑅𝑅𝑅𝑇𝑇𝑇𝑇 𝑀𝑀𝑇𝑇
𝑃𝑃
𝑀𝑀𝑅𝑅
𝑅𝑅 𝑉𝑉𝑇𝑇𝑇𝑇
𝑉𝑉𝑅𝑅� = 𝑃𝑃𝑃𝑃𝑅𝑅 𝑅𝑅 𝑃𝑃𝑅𝑅 𝑅𝑅𝑇𝑇𝑇𝑇  𝑃𝑃𝑅𝑅 𝑃𝑃𝑅𝑅 𝑅𝑅𝑅𝑅𝑅𝑅 𝑅𝑅 𝑜𝑜 𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅 
The total value of the redemption is multiplied by the ratio total net principal for the owner/beneficiary over total 
market value for the same owner/beneficiary combination. The example below reflects a full [[liquidation]] in one 
of three positions. 
Example 1 
A $315.00 redemption in Security Issue [[ID]] 3 is executed on Day 2X, what are the principal and earnings 
portions of this redemption?   
𝑃𝑃𝑃𝑃
𝑅𝑅𝑅𝑅𝑃𝑃𝑅𝑅
𝑅𝑅𝑇𝑇𝑇𝑇 𝑃𝑃
𝑅𝑅𝑃𝑃
𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅 𝑅𝑅
𝑜𝑜 𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅 = $315.00 ∗ � $1,800
$1,953.00� = $290.32 
𝐸𝐸𝑇𝑇
𝑃𝑃𝑅𝑅𝑅𝑅𝑅𝑅𝐸𝐸
𝐸𝐸 𝑃𝑃
𝑅𝑅𝑃𝑃
𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅 𝑅𝑅
𝑜𝑜 𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅𝑅 = $315.00 −  $290.32 = $24.68 
  Day One Day Two 
[[shares]] Price Value Principal Earnings [[shares]] Price Value Principal Earnings 
Security Issue [[ID]] 90.0000 $10.00 $900.00 $900.00 $0.00 90.0000 $11.00 $990.00 $900.00 $90.00 
Security Issue [[ID]] 120.0000 $5.00 $600.00 $600.00 $0.00 120.0000 $5.40 $648.00 $600.00 $48.00 
Security Issue [[ID]] 50.0000 $6.00 $300.00 $300.00 $0.00 50.0000 $6.30 $315.00 $300.00 $15.00 
Totals: 
  
$1,800.00 $1,800.00 $0.00 
  
$1,953.00 $1,800.00 $153.00 
 
Unlike standard principal and earnings calculation, when calculating the basis on a transfer, the delivering Firm  
should pro-rate basis and earnings across each Security Issue [[ID]] included in the transfer. This will factor in the 
effect of zero balance accounts and reduce the risk of double-counting or overlaying basis and earnings 
information. The example below includes multiple active positions as well as a closed position.  
  

---

## Page 43

529 Account Processing Best Practices 
Basis and Earnings 43 
Example 2 
A transfer out of $1,800.00 is executed on Day 3 from their two remaining Security Issus IDs. What is the principal 
that must be provided to the contra-Firm for each transfer? 
𝑆𝑆𝑅𝑅𝑃𝑃𝑉𝑉
𝑃𝑃𝑅𝑅𝑅𝑅𝑆𝑆 𝐼𝐼𝐸𝐸
𝐸𝐸𝑉𝑉𝑅𝑅 𝐼𝐼
𝐼𝐼 1 𝑇𝑇𝑃𝑃
𝑇𝑇𝑅𝑅
𝐸𝐸𝑜𝑜𝑅𝑅𝑃𝑃 𝑃𝑃𝑃𝑃
𝑅𝑅𝑅𝑅𝑃𝑃𝑅𝑅
𝑅𝑅𝑇𝑇𝑇𝑇 = $
1524.68 ∗ �$1,080
$1,800� = $914.81 
𝑆𝑆𝑅𝑅𝑃𝑃𝑉𝑉
𝑃𝑃𝑅𝑅𝑅𝑅𝑆𝑆 𝐼𝐼𝐸𝐸
𝐸𝐸𝑉𝑉𝑅𝑅 𝐼𝐼
𝐼𝐼 2 𝑇𝑇𝑃𝑃
𝑇𝑇𝑅𝑅
𝐸𝐸𝑜𝑜𝑅𝑅𝑃𝑃 𝑃𝑃𝑃𝑃
𝑅𝑅𝑅𝑅𝑃𝑃𝑅𝑅
𝑅𝑅𝑇𝑇𝑇𝑇 = $
1524.68 ∗ � $720
$1,800� = $609.87 
  Day Three Day Four 
[[shares]] Price Value Principal Earnings [[shares]] Price Value Principal Earnings 
Security Issue [[ID]] 1 90.0000 $12.00 $1,080.00 $900.00 $180.00 0.0000 $0.00 $0.00 -$14.81 $14.81 
Security Issue [[ID]] 2 120.0000 $6.00 $720.00 $600.00 $120.00 0.0000 $0.00 $0.00 -$9.87 $9.87 
Security Issue [[ID]] 3 0.0000 $0.00 $0.00 $24.68 -$24.68 0.0000 $0.00 $0.00 $24.68 -$24.68 
Totals: 
  
$1,800.00 $1,524.68 $275.32 
  
$0.00 $0.00 $0.00 
 
 
 
 
 
 

---

## Page 44

529 Account Processing Best Practices 
529 Plan Account Redemptions 44 
529 PLAN ACCOUNT REDEMPTIONS 
Overview 
Redemptions or liquidations from a Section 529 account are categorized as Qualified or Non- Qualified. 
Qualified 
A withdrawal from an account that is used to pay the qualified higher education expenses of the designated 
beneficiary. 
Nonqualified 
Nonqualified withdrawals are subject to a penalty of 10% of the earnings portion and include any withdrawal 
from an account other than the following: 
• A qualified withdrawal 
• A withdrawal by reason of the death or disability of the beneficiary 
• A withdrawal due to a scholarship received by the beneficiary as long as the amount withdrawn does not 
exceed the scholarship 
Fund/SERV® Transaction Type Field 
For a redemption, If Transaction Code = 03 (Partial [[liquidation]]) or 04 (Full [[liquidation]]) then the Transaction 
Type field must be one of the following: 
• 3 = Net [[Asset]] Value  
• 5 = CDSC [[liquidation]] 
• 8 = 529 [[participant]] Distribution 
• 9 = 529 Beneficiary Distribution 
• A = 529 School Distribution 
• B = 529 Rollover Distribution 
• E = 529 In-State Plan Transfer Distribution 
• F = 529 Registration Change 
NOTE:  
529 Registration Change redemptions are used to facilitate changes in registration as well as changes in 529 plans that 
would be considered ‘Rollovers’ with a single transaction, rather than through separate Rollover and Registration Change 
transactions. As such, each 529 Registration Change distribution should trigger the generation of Trustee to Trustee 
Transfer 1099-Q records. 

---

## Page 45

529 Account Processing Best Practices 
529 Plan Account Redemptions 45 
 
IRA/529 [[liquidation]] Indicator Field: 
If the Transaction Type field is 8 (529 [[participant]] Distribution), 9 (529 Beneficiary Distribution), A (529 School 
Distribution) or B (529 Rollover Distribution) then IRA/529 [[liquidation]] Indicator field must be one of the 
following: 
• A = Qualified 
• B = Non-Qualified 
 
If the Transaction Type field is E (529 In-State Plan Transfer Distribution) then IRA/529 [[liquidation]] Indicator 
must be 
• C = Distribution-Non-Taxable 
 
Best Practice is to utilize C (Distribution – Non-Taxable) value when: 
• Transactions are to be treated as a non-taxable event (i.e., annual brokerage fees, transfer fees, etc.). 
• When there is no owner or beneficiary change on In-State Plan Transfers, transactions are to be 
considered a Strategy Change (not a rollover). 
 
If the Transaction Type field is F (529 Registration Change) then IRA/529 [[liquidation]] Indicator must be one 
of the following: 
• D = 529 Owner Change 
• E = 529 Beneficiary Change – In-Family 
 
Best Practice for use of values D (529 Owner Change) and E (529 Beneficiary Change – In-Family): 
• When a registration changes due to a change in Owner 
• When a registration changes due to a change of Beneficiary (In-Family) 
[[liquidation]] Indicator (CDSC Waivers) for 529 Accounts 
Best Practice – For 529, CDSC-exempt redemptions, Firms and Funds should utilize the applicable CDSC 
waiver reason in the [[liquidation]] Indicator field. 
• C = 529 Plan Specific* 
• D = 529 Plan Account – Beneficiary Disability 
• E = 529 Plan Account – Beneficiary Death 
• F = 529 Plan Account – Beneficiary Scholarship 
 
*Note:  
C=529 Plan Specific – this value is only to be used if there is no other value that accurately describes the reason for 
waiving the CDSC. Otherwise, one of the values 4–B or D–F (529 Plan Accounts) is to be used. 
 

---

## Page 46

529 Account Processing Best Practices 
529 Plan Account Redemptions 46 
 
 
Figure 22 Redemptions - Level 0/4 


---

## Page 47

529 Account Processing Best Practices 
529 Plan Account Redemptions 47 
 
Figure 23 Redemptions - Level 3 
 


---

## Page 48

529 Account Processing Best Practices 
529 Plan Account Redemptions 48 
 
Figure 24 Redemptions - Omnibus 
  


---

## Page 49

 
 
© 2024 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]].  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer 
 
Doc Info: February 29, 2024 
Publication Code: MFS369 
Service: Fund/SERV® and Networking 
Title: 529 Account Processing Best Practices 
For More Information 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
 
 