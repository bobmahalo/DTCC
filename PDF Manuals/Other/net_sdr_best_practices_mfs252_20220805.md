---
title: "Standardized Data Reporting: Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_sdr_best_practices_mfs252_20220805.pdf"
pages: 62
size: "1138.0 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Standardized Data Reporting: Best Practices

**Original File:** [net_sdr_best_practices_mfs252_20220805.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/net_sdr_best_practices_mfs252_20220805.pdf)  
**Category:** Other  
**Total Pages:** 62  
**File Size:** 1138.0 KB  

---

## Page 1

 
 
NETWORKING 
STANDARDIZED DATA REPORTING BEST PRACTICES 
AUGUST 5, 2022 
 


---

## Page 2

 
 
Copyright© © 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. 
TOGETHER, and the Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing 
Corporation. 
 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The 
Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these 
affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in 
which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the 
services they offer. 
By accessing this document, you acknowledge, accept and agree to the foregoing [[obligations]] and restrictions. 
 
Doc Info: August 5, 2022 
Publication Code: MFS252 
Service: Networking 
Title: Standardized Data Reporting: Best Practices 
 
 
 
 
 
  

---

## Page 3

 
 
REVISION HISTORY 
 
Revision Dates Revisions 
August 5, 2022 Learning upgrade caused some link(s) to break.  Links have been corrected.  
Jan. 8, 2021 Updated Saturday’s last cycle output time to 2:00pm (p.21) to align with revised 
processing schedule (Important Notice a8905) 
Dec. 23, 2019 Document refresh due to rebranding and links corrected to Learning. 
Feb. 15, 2012 Updated with comments regarding sunsetting of SDR Reject Codes. 
July 5, 2011 Updated by SDR Task Force.  This Guide is updated to coordinate with 
changes effective October 2011.  
May 25, 2010 Updated with comments from SDR Rejects Task Force. 
May 3, 2007 Updated for Insurance Company Processing and other modifications. 
June 9, 2006 Added Best Practice for Incomplete Responses and Fund/SERV Correction  
Orders. 
Aug. 7, 2006 Please see Important Notice a6213, P&S 5783, Dated March 8, 2006. 
June 18, 2007 Please see Important Notice a6446, P&S 6016, Dated May 3, 2007. 
 
 
 

---

## Page 4

 
 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 7 
Background and Objectives ................................................................................................................................ 7 
Overview............................................................................................................................................................ 7 
Scope ................................................................................................................................................................ 8 
Naming Conventions and Terminology .............................................................................................................. 8 
SDR ................................................................................................................................................................... 8 
[[intermediary]] ...................................................................................................................................................... 9 
First-Tier [[intermediary]] ....................................................................................................................................... 9 
Underlying [[intermediary]] .................................................................................................................................... 9 
[[participant]]/Contract or Policyholder/Shareholder ...........................................................................................10 
Omnibus Account ............................................................................................................................................10 
Plan .................................................................................................................................................................10 
[[investor]] Omnibus Account ..............................................................................................................................11 
Super Omnibus Account .................................................................................................................................11 
Super Omnibus Example 1 ............................................................................................................................11 
Super Omnibus Example 2 ............................................................................................................................12 
Transaction Source .........................................................................................................................................12 
NAV Date or Trade Date .................................................................................................................................12 
Ad-hoc Data Requests ....................................................................................................................................12 
Transaction Type–Buys ...................................................................................................................................13 
Transaction Type–Sells ...................................................................................................................................13 
Transaction type-Transfers .............................................................................................................................13 
Working Assumptions .......................................................................................................................................13 
Field Validation ................................................................................................................................................13 
Category 1 Transactions .................................................................................................................................14 
Summary Data ................................................................................................................................................14 
Detail Data .......................................................................................................................................................15 
Account Identifiers ...........................................................................................................................................15 

---

## Page 5

 
 
Shareholder Recordkeeping............................................................................................................................16 
Processing Flows ............................................................................................................................................... 18 
Business Processing ........................................................................................................................................18 
Inquiry Request Data .......................................................................................................................................18 
Data Request Types ......................................................................................................................................18 
Acknowledgment Data ....................................................................................................................................19 
[[NSCC]] Reject Data ..........................................................................................................................................19 
[[intermediary]] Reject Data.................................................................................................................................20 
Response Data ................................................................................................................................................20 
[[NSCC]] Reminders ............................................................................................................................................20 
System Processing ...........................................................................................................................................21 
Process Flow using ftp (batch) on data request input/output and response input/output  ...............................22 
Process flow over HTTPS using MyDTCC portal ..........................................................................................22 
Best Practices ..................................................................................................................................................... 23 
Category 1 and Category 2 Transactions .........................................................................................................23 
Category 1 Transactions ...................................................................................................................................23 
Category 2 Transactions ...................................................................................................................................24 
Transaction Definitions ....................................................................................................................................25 
Commonly utilized Retirement Plan, Variable Insurance, and [[Broker]] Dealer transaction codes. ................26 
Adjustment Processing ....................................................................................................................................31 
Additional Transaction Codes ........................................................................................................................31 
Additional Transaction Codes Commonly Utilized by Variable Insurance Firms: .........................................32 
Data Range Requests ......................................................................................................................................33 
Historical Data Requests ..................................................................................................................................33 
SDR Acknowledgement ....................................................................................................................................34 
SDR Reject Record...........................................................................................................................................34 
Scenario 1 .......................................................................................................................................................35 
Scenario 2 .......................................................................................................................................................35 
Incomplete Responses .....................................................................................................................................36 
Request Time for Data Requests .....................................................................................................................37 

---

## Page 6

 
 
Summary Data ..................................................................................................................................................38 
Social Code .......................................................................................................................................................39 
Super Omnibus Accounts .................................................................................................................................41 
Model #1 ..........................................................................................................................................................41 
Process Flow .................................................................................................................................................42 
Model #2 ..........................................................................................................................................................42 
Process Flow .................................................................................................................................................43 
Model #3 ..........................................................................................................................................................44 
Process Flow .................................................................................................................................................45 
Omnibus Accounts ............................................................................................................................................45 
Chain of [[intermediary]] Relationships .................................................................................................................47 
SDR Control Number and SDR Response Number .........................................................................................48 
SDR Control Number ......................................................................................................................................48 
SDR Response Number ..................................................................................................................................49 
Correction Indicator and Fund/SERV® Correction Orders ................................................................................49 
Correction Indicator .........................................................................................................................................49 
Fund/SERV® Correction Orders ......................................................................................................................49 
Recurring Accounts, Foreign Accounts and Restrictions .................................................................................50 
Recurring Requests .........................................................................................................................................50 
Foreign Accounts ............................................................................................................................................50 
Restrictions ......................................................................................................................................................50 
Appendix A ......................................................................................................................................................... 51 
Financial Activity Reporting (FAR) Transaction Type Definitions with SDR Category and Transaction Codes
 .........................................................................................................................................................................51 
 

---

## Page 7

Standardized Data Reporting Best Practices 
 
 
 
Overview 7 
 
 
 
OVERVIEW 
Background and Objectives 
Frequent trading in [[Mutual Funds]] may have harmful effects on the management company, its portfolio, and its 
long-term investors. Frequent trading may dilute the value of the fund [[shares]], disrupt the management of a 
fund's portfolio, raise fund transaction costs, affect the fund's [[Liquidity]], and result in unwanted taxable capital 
gains for the remaining shareholders. Funds employ various strategies to detect and deter frequent trading, 
including assessing a fee on redemptions made a short time after the purchase of the [[shares]] has occurred and 
surveillance to ensure compliance with funds' frequent trading or market timing policies. 
Mutual fund [[shares]] that are purchased by investors through [[Broker]]-dealers, banks, insurance [[Companies]], and 
retirement plan administrators ("intermediaries") may be combined with other investors' fund [[shares]] and 
registered in the name of the [[intermediary]] in a single omnibus account. For the funds to monitor the 
shareholder account for frequent trading, and appropriately evaluate and potentially assess any applicable 
redemption fees, the funds must be able to identify the investors and their respective trading activity within the 
omnibus account. 
On May 23, 2005, [[SEC]] Rule 22c-2 went into effect with a final compliance date of October 16, 2007. Rule 22c-
2, in part, requires funds to enter into written agreements with their intermediaries, under which the 
intermediaries must, upon request, provide funds with certain shareholder identity and trading information for 
those positions representing the omnibus account assets. This requirement will enable funds to determine 
whether their frequent trading or market-timing policies are being followed, monitor the frequency of trading, 
and determine whether redemption fees are being properly assessed, if applicable. 
Overview 
The Investment Company Institute's Standardized Data Reporting Working Group created the design for a 
standard, automated facility for funds to request and receive shareholder trading information from 
intermediaries through [[NSCC]]. This solution is referenced as SDR throughout this document. SDR is designed 
to provide the funds with a robust mechanism to request data from intermediaries as their compliance and 
monitoring programs warrant. The mechanism allows for varying functionality such as data requests at a 
summary level (plan/omnibus account level data) or detail level ([[participant]]/shareholder level data), data 
requests for a specific date or a period, and for data requests submitted on a regular or periodic basis.  
This guide provides best practices for using SDR and corresponds to the processing flow, record layouts, and 
the Technical Overview document. Future changes to the record layouts may invalidate the specific examples 
provided in this guide, but the concepts and the primary data illustrated in the examples would likely still apply.  
 

---

## Page 8

Standardized Data Reporting Best Practices 
 
 
 
Overview 8 
 
 
 
Many of the best practices and examples may apply to other processing mechanisms used outside of the 
[[DTCC]] systems. Firms utilizing the [[DTCC]] Web Direct solution via the [[DTCC]] systems may also use this 
document as a guideline. 
Scope 
This guide describes the standard usage of SDR as developed by the Best Practices Taskforce of the 
Investment Company Institute's Standardized Data Reporting Working Group 
The best practices detailed within this document provide a framework in which the SDR functionality should be 
utilized. These best practices have been drafted to address 22c-2 data requests, acknowledgments, and 
responses for common scenarios and business relationships currently in existence between funds and 
intermediaries. As such, the best practices detailed within this guide [[DO]] not address all scenarios or business 
relationships that may exist or arise between funds and intermediaries. 
Where situations arise that differ and are not addressed herein, funds and intermediaries are encouraged to 
discuss these scenarios and relationships in detail in order to reach an understanding as to the data requests 
that can be supported by the [[intermediary]] or its designee, and the timeframes in which the data can be 
provided. 
SDR and the corresponding best practices may not be applicable to gathering information for plan level 
unitization, fund of funds, Section 529 plans, and common collective trusts, which are considered to be out of 
the scope of scenarios addressed by the Standardized Data Reporting Working Group. Funds may still request 
data for these purposes on a manual basis. 
Naming Conventions and Terminology 
To assist in understanding terminology and the various entities referenced in this User Guide, the following list 
of definitions is provided. Please note that these descriptions serve as functional definitions and should not be 
construed as the legal or technical definitions of the terms below. 
SDR 
Standard Data Reporting (SDR) is an industry reference to the automated facility for funds to request and 
receive shareholder trading information from intermediaries through [[NSCC]]. SDR provides both file formats and 
an [[NSCC]]-facilitated reporting mechanism between funds and intermediaries of trade transactions for a specific 
date(s). Aggregate transaction detail for a period of time, as a whole, is not supported by SDR  e.g., rolled up 
transaction totals for a period of time. 

---

## Page 9

Standardized Data Reporting Best Practices 
 
 
 
Overview 9 
 
 
 
[[intermediary]] 
The [[intermediary]] is the company or entity from which the fund is requesting data. On a retirement account, the 
[[intermediary]] is typically the recordkeeper. The [[intermediary]] may also be a [[Broker]]/dealer, trust company, 
clearing firm, insurance company, third party administrator, or service provider. 
As suggested by the terminology, intermediaries may have different business models. However, it is commonly 
agreed that intermediaries may provide: 
• Custodial and/or trustee services that offer plan level accounting and safekeeping of assets 
• Trading services for underlying intermediaries whereby the [[intermediary]] acts as a conduit to the fund for 
an underlying firm 
• Sub-Transfer agency or [[participant]] level recordkeeping services 
• Shareholder services 
 
These services may be provided as a bundled service offering or as separate services.  
The [[intermediary]] is identified in the "firm" data field in the [[NSCC]] SDR record layouts.  The two terms are used 
interchangeably in this guide. The entity provided in the [[intermediary]] field may be a first-tier or Underlying 
[[intermediary]], described below. From an [[NSCC]] perspective, the [[intermediary]] is the [[NSCC]] [[participant]] to which 
the request will go directly. 
First-Tier [[intermediary]] 
A first-tier [[intermediary]] is defined as an [[intermediary]] that has an existing contractual relationship with the fund 
to act as a conduit for executing transactions, regardless of whether the first-tier [[intermediary]] provides plan or 
[[participant]]-level recordkeeping services or has the underlying shareholder's transaction level detail. 
The first-tier [[intermediary]] is not a data field in the [[NSCC]] SDR record layouts. This term is used in this Guide to 
clarify the roles and relationships among the "chain of intermediaries" that may exist in transactions that are 
executed with the fund. 
Underlying [[intermediary]] 
An Underlying [[intermediary]] is defined as a related entity that transacts with the funds through services 
provided by a first-tier [[intermediary]]. Underlying firm numbers (UFS codes) are assigned and maint ained by 
[[NSCC]]. The Underlying Firm Symbol (UFS) List is available on dtcclearning.com. The underlying [[intermediary]] 
is a data field in the [[NSCC]] SDR record layouts. When this field is used, it implies that:  
1. The "Firm" field in the record layouts contains the first-tier [[intermediary]] and the "Underlying Firm" field 
contains the Underlying [[intermediary]], or 

---

## Page 10

Standardized Data Reporting Best Practices 
 
 
 
Overview 10 
 
 
 
2. The "Firm" field in the record layouts contains the service provider that the first-tier or underlying 
[[intermediary]] is using to support the SDR functionality. The underlying [[intermediary]], in this case, may be 
the first-tier or Underlying [[intermediary]]. 
 
[[participant]]/Contract or Policyholder/Shareholder 
These are the individual investors, which are also known as participants in a retirement account, contract or 
policyholders in variable insurance, or shareholders in an omnibus or individual retail account. These terms are 
used interchangeably throughout this paper. Participants/Contracts or Policyholders/Shareholders must be 
identified using an SSN or TIN. Customer-Level Account Number may also be provided by the [[intermediary]], in 
addition to an SSN or TIN. 
The term "shareholder" is defined in Rule 22c-2, and as provided in the [[SEC]]'s Final Rule Release, "includes a 
[[Beneficial Owner]] of [[securities]] held in [[nominee]] name, a [[participant]] in a [[participant]] -directed employee benefit 
plan, and a holder of interests in a master-feeder fund or an insurance company separate account organized 
as a unit investment trust. The term does not include a fund that relies on section 12(d)(1)(G) of the Act to 
invest in other funds in the same fund group. These funds often are used as conduits, allowing a shareholder 
to invest in multiple funds in the complex through a single fund. Although shareholders in the conduit fund may 
engage in abusive trading strategies, a conduit fund itself would appear to have little incentive to engage in 
such strategies because they may adversely affect another fund in the same complex. The definition of 
"shareholder" also excludes a section 529 account or the holder of an interest in such an account. The loss of 
tax benefits that a holder would incur as a result of changing investments more than once a year makes it 
unlikely that the holder would use a section 529 account for short-term trading." 
Omnibus Account 
An Omnibus Account held at the fund represents assets for multiple investors. The assets are often registered 
in the name of the [[intermediary]] or in the name of the trustee or custodian for the benefit of the plan at the fund. 
Examples would include one retirement plan, one trust, or multiple retail shareholder ac count assets held in 
one account at the fund. An omnibus account may be identified using a fund account number or [[intermediary]] 
account number (BIN), both of which are cross-referenced to each other in the internal systems of the fund or 
its [[transfer agent]], and the firm (e.g., trust, [[Broker]]/dealer, recordkeeper, etc.). 
Plan 
A plan is a retirement plan, including 401(k), 403(b), etc. or defined benefit plan, and contains multiple plan 
participants. A plan may be identified using a Plan [[ID]]. A plan may also be identified using a fund account 
number or a BIN, when a fund account corresponds to a single plan. For some intermediaries, the Plan [[ID]] may 
be the same as the BIN. 

---

## Page 11

Standardized Data Reporting Best Practices 
 
 
 
Overview 11 
 
 
 
There are two types of Plans: those with [[participant]] investment direction and those without [[participant]] 
direction. In a plan with [[participant]] direction (such as 401(a) or 403(b)), the underlying [[participant]] is the 
shareholder or client for purposes of this paper. In a plan without [[participant]] direction (such as a Pension Plan 
or Defined Benefit Plan), the plan is equivalent to the "shareholder" or "client" since the plan or its agent has 
the investment discretion. 
[[investor]] Omnibus Account 
[[investor]] omnibus accounts may contain retail accounts, Networking matrix level 3 accounts, IRAs, and other 
tax-deferred accounts, all of which are contained within a single account and represent multiple shareholders. 
The [[investor]] omnibus account may be identified using the [[investor]] omnibus account number, or the fund 
account number/BIN, when a fund account corresponds to a single [[investor]] omnibus account. For some 
intermediaries, the [[investor]] omnibus account number may be the same as the  BIN. 
Super Omnibus Account 
A super omnibus account is an account that is held at the fund and may contain assets of more than on e 
omnibus account, several [[intermediary]] omnibus accounts, and potentially assets of individual shareholder 
accounts held by the [[intermediary]]. The [[intermediary]] accounts within the super omnibus account may include a 
plan-level retirement account containing multiple participants, or an omnibus retail/trust/institutional account 
containing multiple shareholders. A super omnibus account may be identified using a fund account number or 
[[intermediary]] account number (BIN), both of which are cross-referenced to each other. 
Super Omnibus Example 1 
 
• Individual accounts on the books of the insurance company; 1 account on the books of the fund  
• Trading is aggregated at the Security [[ID]] level – 1 net buy/sell reflecting the cumulative activity of all 
shareholders 
• Initial SDR request from funds would be a Summary request. Response would summarize Plan level 
activity for the requested time period. Fund would determine which Plan was source of frequent trading.  
• Subsequent SDR request would be a Detail request for the suspected Plan. 
 


---

## Page 12

Standardized Data Reporting Best Practices 
 
 
 
Overview 12 
 
 
 
Super Omnibus Example 2 
 
• Individual, plan, and [[participant]] accounts on the insurance company books; single account on the fund 
books. 
• Trading is aggregated at the Security [[ID]] level – 1 net buy/sell reflecting the cumulative activity of all 
shareholders. 
• Initial SDR response will be a Summary record for each plan and Detail record for each customer.  
• If Plan B is the source of frequent trading, Fund will send Detail SDR request for Plan B. If Plan A is the 
source, then the trade activity will be obtained from the 2nd Tier. 
Transaction Source 
The SDR Transaction Source field is used to indicate the party responsible for submitting/directing the original 
transaction instructions. This could be the shareholder/[[participant]], representative, or recordkeeper/insurance 
carrier. 
NAV Date or Trade Date 
The date on which a net [[Asset]] value for a Security [[ID]] is calculated. Some systems [[DO]] not contain a field called 
NAV date. The process, cycle, or trade date should be equal to NAV date. 
A corrected transaction would use an effective, as-of, or reversal date to make the customer whole. The 
correction procedure would generally backdate the trade to use the NAV price that was in effect when the 
transaction should have been processed. The corrected transaction would be traded at today's NAV price and 
gain/loss risk would be held at the [[intermediary]] level. 
Ad-hoc Data Requests 
Ad-hoc data requests are unscheduled, intermittent requests of various purposes submitted by the funds to the 
intermediaries. 


---

## Page 13

Standardized Data Reporting Best Practices 
 
 
 
Overview 13 
 
 
 
Transaction Type–Buys 
Buys under the SDR Transaction Type field are purchase transactions communicated by intermediaries to 
funds. Intermediaries that provide record keeping services may, and often [[DO]], aggregate initial purchase, 
subsequent purchase, interfund buy side exchanges, or intra-fund buy side transfers and communicate the 
aggregate purchase amount as a Buy to the fund. 
Transaction Type–Sells 
Sells under the SDR Transaction Type field are redemption transactions communicated by intermediaries to 
funds. Intermediaries that provide record keeping services may, and often [[DO]], aggregate redemptions, 
interfund sell side exchanges, or intra-fund sell side transfers and communicate the aggregate redemption as a 
Sell to the fund. 
Transaction type-Transfers 
Transfers (transfer in/transfer out) under the SDR Transaction Type field are in-kind transfers of [[shares]] 
between accounts communicated to funds via manual instruction or automated transactions via ACATS, or 
Networking B52 records. Note: these transactions are all share movements within the same Security [[ID]].  
Working Assumptions 
These working assumptions are the initial set of best practices, which are the basis for the design of SDR. 
Subsequent processing flows and record layouts were developed based on these working assumptions. 
Adherence to these working assumptions is critical to achieving standard utilization of SDR. 
Field Validation 
The Opt/Req Field indicates whether a field must be coded (Required), can be bypassed (Optional), or is 
dependent on conditions (OC or RC). [[NSCC]] validates data supplied is complete, as described below. [[NSCC]] 
also validates that the format is correct (when applicable) before sending through to the receiving party. Below 
are the different coding options & [[obligations]]: 
R = Required 
This field must be completed. [[NSCC]] will validate the following criteria. If coding is not completed properly, the 
record will be rejected. 
• Information is accurate (when it can be validated by [[NSCC]]). 
• Correct format must be followed (if specified). 
• If options are offered in the Description field, [[NSCC]] will check that a legitimate value was used.  
 

---

## Page 14

Standardized Data Reporting Best Practices 
 
 
 
Overview 14 
 
 
 
O = Optional 
This field does not have to be completed. However, if the field is utilized, [[NSCC]] will check that the following 
criteria are met. If not, the record will be rejected. 
• Correct format must be followed (if specified). 
• Information is accurate (when it can be validated by [[NSCC]]). 
• If options are offered in the Description field, [[NSCC]] will check that a legitimate value was used.  
 
RC = Required/Conditional 
This indicates the field is generally required but can be optional upon specific conditions. The record layouts 
will state what the conditions are. If conditions are met, this field may be bypassed. [[NSCC]] will check the 
following criteria. If coding is not completed properly, the record will be rejected.  
• Correct format must be followed (if specified). 
• Information is accurate (when it can be validated by [[NSCC]]) 
• If options are offered in the Description field, [[NSCC]] will check that a legitimate value was used. 
 
OC = Optional/Conditional 
This indicates the field is generally optional; but required upon specific conditions.  The Record Layouts will 
state what the conditions are. If conditions are met, these fields must be utilized. [[NSCC]] will check the following 
criteria. If coding is not completed properly, the record will be rejected. 
• Correct format must be followed (if specified). 
• Information is accurate (when it can be validated by [[NSCC]]) 
• If options are offered in the Description field, [[NSCC]] will check that a legitimate  [[Option]] was used. 
Category 1 Transactions 
Transactions provided through SDR are assumed to be Category 1 transactions (as defined later in this 
document) unless otherwise specified. See the "Best Practices" section of this guide for definitions and 
examples of Category 1 and Category 2 transactions. 
Summary Data 
Summary data is the high-level information regarding the plans, trusts, and/or [[investor]] omnibus accounts that 
are combined into a super omnibus account. It is assumed that only summary data will first be passed for 
super omnibus accounts. This summary data provides sufficient information to help the funds identify specific 
plans where trading is occurring frequently. The fund would then be able to request data at a plan/trust level 

---

## Page 15

Standardized Data Reporting Best Practices 
 
 
 
Overview 15 
 
 
 
and obtain detailed information about the underlying participants. The same applies to the trusts, [[investor]] 
omnibus accounts, and the underlying shareholders. 
The process of first providing summary data is necessary because a request against a super omnibus account 
may produce a prohibitive amount of response data at a shareholder level. To avoid having to process this 
large amount of data for super omnibus accounts, summary data will instead be provided.  
For example, a super omnibus account should provide summary data for the retirement plans or trusts and 
detail data for individual investors when no summary or rollup to a plan is available.  
In some cases where the recordkeeper is unable to provide plan-level trade activity, the fund is encouraged to 
request detailed trade activity using dollar thresholds to reduce the volume of data. Some intermediaries may 
average one million transactions per day. Analysis performed at one company identified that less than 1% of all 
transactions are over $10,000, whereas 86% are below $100. 
Detail Data 
On super omnibus accounts that contain individual shareholder accounts along with multiple plans and [[investor]] 
omnibus accounts, the [[intermediary]] will provide detail information for the individual shareholders. In this 
situation, the response for the super omnibus account contains both summary and detail data. Also, data 
requests at a plan or [[investor]] omnibus account level will always result in detail data. Lastly, when specific 
shareholder level information (e.g., SSN) is provided by the fund on an inquiry request, the intermediaries will 
provide detailed trading information to the fund for that specific shareholder. 
Account Identifiers 
Depending on the account setup, there may be several levels of data that can be retrieved, e.g., data at a 
super omnibus level, plan or [[investor]] omnibus account level, and individual shareholder level. The account 
identifiers on the request tell the [[intermediary]] how to find the account and shareholder in question; and 
determine the level of data that can be returned to the fund. 
The identifiers include the fund account number, [[intermediary]] account number (BIN), plan [[ID]], [[investor]] omnibus 
account number, and SSN/TIN. The identifiers are used in the following manner:  
• Super omnibus accounts are identified only by fund/[[intermediary]] account number.  
• Plan accounts are identified only by fund/[[intermediary]] account number or by plan [[ID]].  
• [[investor]] omnibus accounts are identified only by fund/[[intermediary]] account number or by [[investor]] 
omnibus account number. 
• Participants, contract holders, or shareholders are identified only by SSN/TIN and customer-level account 
number. 
 

---

## Page 16

Standardized Data Reporting Best Practices 
 
 
 
Overview 16 
 
 
 
At a minimum, the [[intermediary]] or fund account number is required on a data request, but all account 
identifiers may be provided. When multiple fields are provided, the [[intermediary]] will identify the lowest level 
identifier and provide only that particular level's data. 
For example, if a fund account number is provided and represents a super omnibus account number, and a 
Plan [[ID]] is also provided, then the Plan [[ID]] will be used. Only the [[participant]] level transactions for that particular 
Plan [[ID]] will be provided. 
Another example is if a fund account number is provided and represents a Plan, and an SSN representing a 
[[participant]] is also provided, then the SSN will be used. Only the activity for that single [[participant]] will be 
provided. 
Shareholder Recordkeeping 
Intermediaries that provide shareholder-level recordkeeping services often maintain and categorize [[participant]] 
level data based on the source of money (e.g., employee contribution, exchanges, loans, etc.). Transactions 
will be identified on the recordkeeping system according to the fund and source of money. For example, in a 
defined contribution plan where a shareholder, who has an outstanding loan, receives a company match, a nd 
makes contributions on a periodic basis via payroll deduction, the [[intermediary]] will record the following 
transactions per fund per contribution: 
Credit - employee contribution, fund 1 - $xx.00 
Credit - employer match, fund 1 - $xx.00 
Credit - loan repayment – principal, fund 1 - $xx.00 
Credit - loan repayment – interest, fund 1 - $xx.00 
Debit - loan repayment – loan fund - $xx.00 
If these were the only shareholder transactions in the fund on a given day, the fund would see a trade for the 
aggregate of employee contribution, employer match, and loan repayment (principal and interest). Where 
intermediaries net all trades (buy/sell, adjustments, etc.) from all participants into an omnibus account (which is 
commonly the case), aggregating the transaction types into a meaningful transaction to the fund will be 
performed based on the above noted definitions of the transaction types. 
When requesting detailed data at a [[participant]]/contract holder/shareholder level, it is also important to note the 
following about shareholder recording systems in the retirement and variable insurance arena:  
• Most recordkeeping systems are built to offer an open investment platform and therefore [[DO]] not 
differentiate between fund families. An exchange within a fund family will be recorded in the same manner 
as an exchange between two unrelated fund families. 

---

## Page 17

Standardized Data Reporting Best Practices 
 
 
 
Overview 17 
 
 
 
• Exchanges can be from one to many funds and are often transmitted to the funds as a buy and a sell as 
opposed to an exchange. 
• Transaction types can be both positive and negative. For example, an employee contribution, which is 
commonly a credit to a [[participant]], may also be processed as a negative, as in a situation where a prior 
period contribution was posted for an incorrect amount. The error is often corrected by posti ng a negative 
contribution or reversal to offset the prior contribution, thereby bringing the shareholder's account in 
balance. 
• Adjustment transactions are generally difficult to classify as either category 1 or category 2 transactions, 
since the transactions are usually the result of an error at various levels (plan, [[intermediary]] or a 
combination of the two). Adjustment transactions generally have a unique transaction type that can be a 
debit or credit transaction. 
• Recordkeeping systems [[DO]] not generally differentiate if a transaction is initiated at the direction of an 
advisor. 
• Transactions involving an automatic rebalancing of the account directed by an advisor will generally 
appear as a Category 1 transaction. 
• Non-discretionary rebalancing programs will be a category 2. If the contract holder or advisor can make 
off-cycle rebalancing changes taking immediate effect, then that would be considered category 1. If 
intermediaries cannot differentiate between non-discretionary and shareholder-initiated, then the [[default]] is 
category 1. 

---

## Page 18

Standardized Data Reporting Best Practices 
 
 
 
Processing Flows 18 
 
 
 
PROCESSING FLOWS 
Business Processing 
The business process and interaction between the funds and intermediaries vary based on the situation. 
Intermediaries are also referred to as "Firms" and a Fund's Security [[ID]] is also referred to as a "Security [[ID]] ". 
Funds are expected to provide all the necessary information for the intermediaries to retrieve the underlying 
shareholder's information. This will result in detailed data being returned by the [[intermediary]] to the fund.  
In cases where a super omnibus account is involved, summary data will first be provided by the [[intermediary]] to 
the fund. The fund will be provided with high-level data regarding the plans or [[investor]] omnibus accounts that 
are combined into the super omnibus account. The fund will then be able to use the additional data from the 
summary to send a more specific inquiry request (e.g., using a plan [[ID]] to limit the inquiry to the shareholders in 
that particular plan.) 
Certainly, if the fund already has the specific data that can be provided and linked to the individual 
shareholders, then the "Summary" Request and response process is not needed. An initial request that 
contains enough detailed information (i.e. Security [[ID]]/Security [[ID]], NAV Date(s), Plan [[ID]] and SSN) will always 
be answered by the [[intermediary]] with a response containing shareholder trading information, even on a super 
omnibus account. 
Inquiry Request Data 
Data on the shareholder's trading activity may be sent by the [[intermediary]] to the fund on an ad- hoc or daily 
scheduled basis. Regularly scheduled files (e.g., ongoing daily files) should be requested manually by the fund 
from the [[intermediary]]. The response files from the [[intermediary]], whether they are as a result of a request done 
through [[NSCC]] or another channel, may be sent through SDR. 
SDR also allows the funds to make data requests from the [[intermediary]]. Various types  of requests will be used 
through [[NSCC]] including: 
Data Request Types 
• Fund Account Level 
• Plan Level 
• [[investor]] Omnibus Account Level 
• Fund/SERV® Control Number Request 
• Rep Level 
• Stop Recurring 
 

---

## Page 19

Standardized Data Reporting Best Practices 
 
 
 
Processing Flows 19 
 
 
 
The format for the fund request input file/message will be the same for all request types, but different data will 
be necessary based on the requests. Each request type will indicate the additional data field used to refine the 
queries for the [[intermediary]] to extract data, accordingly. Additional search criteria may also be included to 
refine requests, such as threshold amount, Security [[ID]] and transaction type. Note: when using a threshold 
amount, only transactions with currency amounts greater than or equal to the threshold amount will be included 
in the response data. Rep Level information is generally not maintained on insurance [[Companies]] and may 
result in a reject if requested, using SDR Reject Code 76–Rep Level Request Not Supported. 
Other data fields will provide additional instructions that will customize the request and the resulting response 
data. For example, since Category 1 Transaction information is the assumed [[default]] search parameter, funds 
may use the "Includes Category 2 Transactions" field to indicate that it is requesting both Category 1 and 
Category 2 transactions. Other fields that modify the search parameters include from/to dates, transaction 
types, and threshold amounts. 
Note 
The data that is actually provided on the request will be the ultimate driver of the type or level of the request. For example, 
a fund account level request that also contains SSN info will result in shareholder level information rather than fund account 
level information. 
 
Acknowledgment Data 
The initial response from the [[intermediary]] to the fund will be an Acknowledgment record. The Acknowledgment 
will be a proactive indication from the [[intermediary]] that it has received the request from the fund and will also 
turn off the [[NSCC]] SDR Reminder record. 
[[NSCC]] Reject Data 
[[NSCC]] performs preliminary validations of SDR requests received from funds and of SDR responses provided 
by intermediaries. Files or records that [[DO]] not pass the [[NSCC]] validation will be returned to the submitter with 
the appropriate reject code. A selection of [[NSCC]] validation rules are provided in the Standardized Data 
Reporting Technical Guide. 
Note 
A set of response records may be partially rejected. For example, a response may contain ten detail records and one of 
those records may not pass validation. [[NSCC]] will reject the single record and return it to the [[intermediary]] along with a 
[[NSCC]]-generated header and trailer to complement the rejected record. 

---

## Page 20

Standardized Data Reporting Best Practices 
 
 
 
Processing Flows 20 
 
 
 
[[intermediary]] Reject Data 
Intermediaries may also reject the fund's data request but will use the Reject record to [[DO]] so. An appropriate 
reject code must be provided. Situations may arise where Intermediaries acknowledge an SDR request, and 
later learn that the request cannot be fulfilled. In this instance Intermediaries should submit a Reject record with 
the appropriate reason code for the previously acknowledged SDR request. A full listing of Standardized Data 
Reporting reject codes can be found on Learning website in the Mutual Fund section. 
Response Data 
There are various levels of information in super omnibus accounts. For example, a super omnibus account, 
identified by a fund account number or [[intermediary]] account number (BIN) (fund account level), may contain 
assets from multiple retirement plans (plan level), and in turn, each plan contains multiple participants or 
underlying shareholders. 
Due to this complexity, the activity and corresponding data related to these accounts is significant. In order to 
control the volume of data that could potentially be extracted and sent to the fund for these super omnibus 
accounts, it will be important to retrieve data at a summary level (fund account level request).  
When a request is submitted against a super omnibus account, it is expected that summary data will be 
returned by the [[intermediary]] to the fund for plans or [[investor]] omnibus accounts that are contained within the 
super omnibus account. Detailed information may also be sent for individual shareholder accounts that are a 
part of the super omnibus account. 
The summary data will provide sufficient information to help the funds identify specific plans or [[investor]] 
omnibus accounts where trading is occurring frequently. The fund would then be able to request data at a plan 
level or [[investor]] omnibus account level and obtain detailed information about the underlying 
participants/shareholders. 
Detail response data is expected to be provided on shareholders when a request is made against specific 
plans, [[investor]] omnibus accounts or individuals specified by the SSN. 
[[NSCC]] Reminders 
[[NSCC]] SDR Reminders are records that will notify the fund, the [[intermediary]], and possibly other related parties 
that an appropriate response has not been made to an SDR Request. [[NSCC]] will send a Reminder record f or 
Requests with SDR Control Numbers that have not been acted upon with an Acknowledgment record or a 
Reject record. Only Acknowledgment or Reject record responses can turn off Reminders. Detail or Summary 
records will not turn off Reminders. 
Reminders will be sent for a period of 10 processing days (including Saturday) from the original date in which 
the SDR Control Number is stored on the [[NSCC]] database. After this timeframe, the SDR Control Numbers will 
be deleted from the system. 

---

## Page 21

Standardized Data Reporting Best Practices 
 
 
 
Processing Flows 21 
 
 
 
The first Reminder will be sent on the first business day after the submission date of the SDR Request and will 
be sent via the last cycle of the day (M-F, 4pm ET; Sat, 2pm, ET.) Reminders will be sent with the Autoroute 
Output file within SDR Request record stream. Within this stream, Intermediaries will receive Request records 
plus Reminders, and Funds will receive [[NSCC]] Request Rejects plus Reminders. 
System Processing 
Two different interfaces are used to support this enhancement. HTTPS protocol is used for web input and 
output using the MyDTCC portal, and FTP/NDM are used for input and output of flat files over the [[DTCC]] 
SMART Network. 
Output files (e.g., [[NSCC]]-accepted data requests from funds going to intermediaries, shareholder trading data 
and reject records) will not be provided through the http(s) facility and will only go out as flat files on mainframe.  
The transmission of ftp input files occurs three times per day every Monday through Friday. Processing on 
Saturday is also available and occurs three times per day. SDR transmission schedule (listed in the  
Networking and Omni/SERV schedule document) is available in the [[Mutual Funds]] section of the Learning 
Center.  
The Service Level Agreement for this product is from 6:00 a.m.to 3:00 p.m. Monday –Friday. 
SDR Data Request and Response – the flowchart below shows the process for both https(s) and ftp/ndm. 
 


---

## Page 22

Standardized Data Reporting Best Practices 
 
 
 
Processing Flows 22 
 
 
 
Process Flow using ftp (batch) on data request input/output and response 
input/output 
1. Fund sends a data request to [[NSCC]] during the acceptable input timeframe. 
2. [[NSCC]] does a preliminary validation, which will result in accepted or rejected records.  
3. [[NSCC]] stages the records to the appropriate destination and output files. 
4. At the appropriate output time, [[NSCC]] sends rejects back to the fund and accepted records to the 
intermediaries. (Other records may also be sent to the intermediaries and funds as part of the output file.)  
5. The [[intermediary]] will take the data request records and may run some preliminary validation, which will 
result in accepted or rejected records. 
6. If [[intermediary]] rejects, then the reject record will be submitted to [[NSCC]] during the input timeframe. [[NSCC]] 
will pass back to the fund in the output file. 
7. If [[intermediary]] accepts, then it will process the request. The first step is for the [[intermediary]] to prepare 
and submit an Acknowledgment to [[NSCC]] during the appropriate input timeframe. [[NSCC]] will pass to the 
fund in the output file. 
8. The process to retrieve the data may take some time and may result in a reject or a response with data.  
9. The [[intermediary]] will respond with a data response. Or, if after querying its systems the [[intermediary]] 
identifies an issue with the data request, the [[intermediary]] will send reject records with the applicable reject 
code to [[NSCC]]. 
10. [[NSCC]] does a preliminary validation, which will result in accepted or rejected records.  
At the appropriate output time, [[NSCC]] sends rejects back to the [[intermediary]] and accepted data records to 
the funds. (Other records may also be sent to the intermediaries and funds as part of the output file.)   
Note 
[[NSCC]] will modify the trailer record being sent to the fund to include the number of accepted and rejected Summary/Detail 
records. This will allow the fund to know whether they received a complete set of data for their data request. 
11. [[NSCC]] will send SDR Reminders each day for a period of 10 processing days as long as an SDR Request 
Control Number has not been acted upon with an Acknowledgment or Reject record. Detail or Summary 
records [[DO]] not turn off Reminders. After 10 processing days, a Reminder is no longer sent. 
Acknowledgement, Reject, and Detail/Summary Response records may still be sent even after the 
Reminders are discontinued. 
Process flow over HTTPS using MyDTCC portal  
1. Fund can upload MRO file using the MyDTCC portal Upload function @ at https://portal.[[DTCC]].com 
2. [[NSCC]] does a preliminary validation. 
3. [[NSCC]] will make the processed file available for download via the MyDTCC. 

---

## Page 23

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 23 
 
 
 
BEST PRACTICES 
These best practices will not be enforced through [[NSCC]] validation but are expectations that must be 
followed to enable standard processing. 
Category 1 and Category 2 Transactions 
Rule 22c-2 requires that intermediaries enter into agreements with funds to provide certain share holder identity 
and trading information. Funds will require this information to monitor the frequency of short -term trading and to 
enforce their frequent trading or market timing policies. As frequent trading or market timing policies vary by 
fund, so too will the funds' data requirements, as established by their surveillance programs.  
Transactions provided through SDR are assumed to be Category 1 transactions, unless otherwise 
specified. Funds will need to determine whether Category 1 transactions, as defined below, provide the 
appropriate level of detail to meet its market timing and redemption fee monitoring criteria.  
Where Category 1 transactions are sufficient for the fund to run its surveillance programs, funds should request 
only Category 1 transactions via the SDR Request record. Where Category 1 transactions are not sufficient for 
the fund to run its surveillance programs, funds should request both Category 1 and Category 2 transactions. 
Intermediaries are then required to provide all transactions. 
It is important to note that the current SDR functionality does not provide funds the ability to filter out individual 
transaction codes. The current [[Option]] is to receive Category 1 transactions or all transactions.  
Category 1 Transactions 
Category 1 transactions will include transactions that are commonly considered to be activity directed by either 
the shareholder, financial advisor, or an investment [[Fiduciary]], and other transaction types where investors may 
have sufficient control to perform market timing activities. 
Category 1 transactions with regard to [[participant]] directed retirement plans where the "underlying [[participant]]" 
or "beneficiary" in the plan makes the investment decisions from a menu of investment options in plans such as 
401(a) (i.e., Money pension and profit-sharing plan), 401(k), 403(b), and 457. 
All trades resulting from a [[participant]] electively trading to sell one investment [[Option]] in the plan to purchase 
another investment [[Option]] will be considered Category 1 transactions. This would include an exchange or 
transfer within a fund family or between unaffiliated fund families. 
Example–[[participant]] initiates sale of fund A to buy fund B. 
Example–An investment advisor initiates sale of fund A to buy fund B on behalf of the [[participant]].  

---

## Page 24

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 24 
 
 
 
[[Asset]] Rebalancing Programs directed by either the [[participant]], plan sponsor, or financial advisor would also be 
considered Category 1 Transactions. 
Example–A plan offers an auto rebalance feature as a plan service. The [[participant]] subscribes to the services 
and elects a model (e.g., 60% stocks, 30% [[Bonds]], 10% cash) as a macro tool to meet the investment 
objectives. This service is scheduled to occur on a regular basis: however, it can be adjusted immediately upon 
request. 
Example–An investment advisor offers an [[Asset]] allocation feature as a plan service to individual participants. 
The [[participant]] subscribes to the services and elects a model (e.g., 60% stocks, 30% [[Bonds]], 10% cash) as a 
macro tool to meet the investment objectives. This service is scheduled to occur on a regular basis or by 
request. 
Example–A plan is operated with a preset investment allocation model (e.g., 60% [[Stock]], 20% bond, 20% cash) 
and initiates trades to reset the plan to the model on a scheduled basis or by request.  
Category 1 includes transactions for non-[[participant]] directed retirement plans where: 
• The "[[participant]]" receives the benefit but does not provide investment direction, and  
• The trustee, investment advisor, plan sponsor, or other entity makes the investment decisions for the 
"plans" such as Pension Plans, SERPS, Non-Qualified Deferred Compensation Plans (where [[participant]] is 
entitled to a benefit but has no investment discretion), 403(b), and Defined Benefit Plans.  
 
Category 1 transactions will include all trades placed by the plan or its designated agent electively to sell one 
investment [[Option]] in the plan and purchase another investment [[Option]]. 
Example–A plan or its designated agent initiates sales of fund A to buy fund B. 
Example–An investment advisor initiates the sale of fund A to buy fund B on behalf of the plan.  
Category 1 transactions within a [[Broker]] Dealer environment will include: 
1. Purchase (initial & subsequent) 
2. Exchange (same fund family) buy and sell side 
3. Sell/Redemption (partial or full [[liquidation]]) 
4. Transfer of [[shares]] in 
5. Transfer of [[shares]] out 
Category 2 Transactions 
Category 2 transactions will include transactions that are commonly considered to be systematic or non-
directed where the shareholder, financial advisor, or an investment [[Fiduciary]] does not exercise direct control 
over the investment decisions that would result in market timing or excessive trading.  

---

## Page 25

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 25 
 
 
 
Category 2 transactions occur where the shareholder, financial advisor or an investment [[Fiduciary]] is one step 
removed from the transactions and where those transactions generally occur via systematic or automated 
investment elections. 
Category 2 transactions as they relate to [[participant]] directed retirement plans where the "underlying 
[[participant]]" or "beneficiary" in the plan makes the investment decisions from a menu of investment options in 
plans (such as 401(a) (i.e. Money pension and profit sharing plan), 401(k), 403(b), and 457) will include, but 
are not limited to, the following list of transactions: 
1. Contributions 
• Employee Contributions 
• Matching employer Contributions 
2. Earnings 
3. [[intermediary]] Administration 
• Corrections 
4. Loan Repayments 
• Loan repayment principal 
• Loan repayment interest 
5. Plan Directed Purchases 
6. Fund Replacements 
7. Adjustments 
8. Plan Conversion 
9. Forfeiture 
10. [[participant]] Distributions 
Transaction Definitions 
The following is a list of commonly used transactions by intermediaries that provide shareholder recordkeeping 
services. The list is not intended to be all-inclusive, but rather the intent is to provide a listing of transactions 
that may be utilized by intermediaries within the response record to provide the requesting funds with an 
appropriate level of detail for the fund to utilize within its surveillance program.  
Intermediaries should review the following list and utilize the transaction codes as applicable to their business.  
Since variable annuities (VA) are an insurance product, even though ultimately invested in [[Mutual Funds]], there 
are many transaction types used for VA that are unique to that product. In an effort to  provide consistency 
between VA transactions and existing SDR transaction types, [[NSCC]]'s Insurance Services' Financial Activity 
Reporting (FAR) codes were chosen as representative of VA transactions and mapped to SDR transaction 
codes. For more information, see Appendix A. FAR Transaction Types Definitions. Use of FAR codes as a 
basis for translating VA activity to SDR transactions should minimize definitional differences on SDR responses 
between insurance carriers and mutual fund [[Companies]]. 

---

## Page 26

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 26 
 
 
 
Commonly utilized Retirement Plan, Variable Insurance, and [[Broker]] Dealer transaction 
codes. 
Transaction Transaction 
Type 
Transaction 
Category 
Transaction 
Code  
Definition 
Employee 
contribution 
Buys Category 2 01 A contribution is money that is 
invested into a [[participant]]'s retirement 
account. Employee contributions are 
always 100% vested. 
Employer 
contribution 
Buys Category 2 02 An employer contribution is money 
that is invested into a [[participant]]'s 
retirement account for the benefit of 
the employee by the employer. 
Employer's contributions (when 
made) may be subject to vesting. 
Additional 
contribution 
Buys Category 2 03 “Additional contribution” may also be 
described as a “Catch Up 
Contribution” 
Loan repayment – 
principal 
Buys Category 2 04 
A loan repayment is money a 
[[participant]] pays back to his/her plan 
account as a result of taking a loan. 
The repayment is generally reinvested 
based on the [[participant]]'s then-
current investment elections. 
Loan repayment – 
interest 
Buys Category 2 05 Interest accrued as part of a 
[[participant]] loan. Typically paid at the 
time of loan repayment. 

---

## Page 27

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 27 
 
 
 
Transaction Transaction 
Type 
Transaction 
Category 
Transaction 
Code  
Definition 
Forfeitures  Buys or Sells Category 2 06 Monies deposited into the [[participant]] 
account by the employer for the 
benefit of the employee and are not 
fully vested at the time a [[participant]] 
terminates from the plan. These funds 
can be reallocated to other plan 
participants or utilized by the plan for 
other purposes. 
 
Forfeitures are the non-vested 
benefits that a [[participant]] loses if they 
terminate employment before 
becoming 100% vested. This means 
that if a [[participant]] is 60% vested in 
their employer money at the time of 
separation, he/she would forfeit 40% 
of those employer assets. 
 
In the event of a re-allocation, buys 
and sells may be communicated as 
the forfeitures may be re-allocated 
from one shareholder account to 
others, or in the event where the 
forfeiture proceeds are utilized to pay 
plan expenses, the funds would be 
raised by communicating sells to the 
fund. 
Adjustments  
(see note below) 
Buys or Sells Category 2 07 An adjustment is a financial 
transaction that is processed with a 
trade date earlier than the current 
date to correct a previous transaction. 
 
Adjustment trades may result in gains 
or losses to the fund, for example, 
when a transaction request is 
received in good order before 4:00 
p.m. but not processed on that day. A 
gain or loss must always be handled 
within the plan in which the error 
occurs. 
 

---

## Page 28

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 28 
 
 
 
Transaction Transaction 
Type 
Transaction 
Category 
Transaction 
Code  
Definition 
Exchange or 
Transfer  
Buys or Sells Category 1 08, 09 An exchange/transfer is the buy of 
[[shares]], dollars, or a percentage of a 
[[participant]]'s holdings from one 
investment [[Option]] to another. 
Conversion balance 
transfer 
Buys or Sells Category 2 10 A plan event that consists of the buys 
and sells between funds or transfer-in 
and transfer-out of the entire 
investments of a plan [[Asset]]. 
Non-discrimination 
refund 
Sells Category 2 11 A return of employer or employee 
contributions into the plan as a result 
of the failure to meet minimum 
contribution limits. 
Loan distribution Sell Category 2 12 A loan in a retirement account on 
plans that allow for loans, is a 
[[participant]] borrowing money against 
the account for general purposes 
and/or to purchase a primary 
residence, based on the terms of the 
plan's loan program. 
In-service 
distribution 
Sell Category 2 13 In-service withdrawals are 
withdrawals from the plan taken by a 
[[participant]] while he is still employed 
by the plan sponsor. The withdrawal 
type and amount are based on criteria 
and restrictions defined in the Plan 
Document. 
Installment 
distribution 
Sell Category 2 14 A plan can allow a [[participant]] to 
receive their termination distribution 
payment over a defined period. 

---

## Page 29

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 29 
 
 
 
Transaction Transaction 
Type 
Transaction 
Category 
Transaction 
Code  
Definition 
Termination 
distribution 
Sell Category 2 15 Upon termination, a [[participant]] has 
the [[Option]] of either: 
 
Taking a cash distribution for the 
amount of the [[participant]]'s 401k 
account. If the [[participant]] chooses to 
[[DO]] so, 20% will be held for income tax 
purposes, in addition to a 10% 
penalty tax if the [[participant]] is under 
the age of 59 1/2. Upon death or 
disability, a [[participant]]'s account will 
be available to the [[participant]] or a 
beneficiary for distribution as well. 
 
Electing a rollover distribution to a tax-
qualified account or the [[participant]]'s 
new employer’s 401k offering (if 
allowed by the plan document), 
thereby postponing withholding until 
qualified distributions are made. 
Hardship 
withdrawals 
Sells Category 2 16 A withdrawal requested by a 
[[participant]] that is defined as a pre-
determined circumstance outlined by 
the plan. 
Lump sum 
distribution 
Sells Category 2 17 This [[Option]] will be used by 
participants who request the entire 
account to be paid to them directly. 
The [[Mutual Funds]] will be liquidated, 
and the [[Stock]] may be issued in-kind 
or liquidated. If the [[participant]] elects 
to issue the [[Stock]] in-kind, it may be 
sent to the [[participant]] or issued to a 
retail account. 
QDRO distribution Sell Category 2 18 Distribution made under a Qualified 
Domestic Relations Order 
RMD distribution Sell Category 2 19 Required Minimum Distribution 
Fees Sell Category 2 20, 21, 22 Fees are charges assessed to the 
plan and/or the plan's participants 
according to the plan's Service 
Agreement for services provided. 

---

## Page 30

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 30 
 
 
 
Transaction Transaction 
Type 
Transaction 
Category 
Transaction 
Code  
Definition 
Rebalance 
Transaction 
Buys or Sells Category 1 23 A transaction initiated by an 
immediate, off-cycle process or 
directed by a shareholder, investment 
[[Fiduciary]], or financial advisor to 
reallocate balances within funds to a 
predefined percentage amongst 
available investment options. This 
transaction will result in offsetting buy, 
sells, or exchanges amongst the 
investment options available to the 
shareholder within his/her account. 
Return of Excess 
Contributions 
Sell Category 2 24 A transaction initiated by the party 
responsible plan ERISA compliance 
to return previously invested 
employee contributions to 
shareholders for situations where the 
party action is required to keep the 
plan compliant. This transaction will 
result in a distribution to the 
shareholder for an amount equal to 
the excess contribution previously 
made to the plan. 
Rollover Buy Category 2 25 Rollover contribution 
[[Dividend]] Buy Category 2 54 A distribution of a portion of a 
company's earnings, decided by the 
board of directors, to a class of its 
shareholders. Generally, retirement 
plans elect the re-investment [[Option]] in 
order to have the distribution 
purchase additional [[shares]] of the 
[[CUSIP]]. As a result, financial 
intermediaries that provide 
recordkeeping services [[DO]] not pass a 
trade on dividends, but rather update 
shareholder records to reflect the 
distribution via an increase of [[shares]] 
equal to the distribution rate.  In the 
event that a cash [[Option]] is elected, a 
trade will be passed and should be 
treated as an employee contribution 
described above. 

---

## Page 31

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 31 
 
 
 
Adjustment Processing 
Adjustment transactions are defined by the SDR Users Guide as a Category 2 transaction that may be a Buy 
or Sell, further defined as: 
• An adjustment is a financial transaction that is processed with a trade date earlier than the current date to 
correct a previous transaction. Any trades processed in this manner are considered adjustments.  
• Adjustment trades may result in gains or losses to the fund; for example, when a transaction request is 
received in good order before 4:00 p.m. but not processed on that day. A gain or loss must always be 
handled within the plan in which the error occurs. 
 
No best practice can be established for the processing of adjustments since each firm will establish processes, 
procedures, and controls tailored to their systems, oversight, and regulatory requirements. SDR functionality 
has been built to allow intermediaries to report adjustment transactions to funds. In situations where funds 
have inquiries regarding the booking or processing of adjustment transactions by intermediaries, funds are 
encouraged to contact the [[intermediary]] directly regarding the transactions in question.  
 
Additional Transaction Codes  
Transaction Transaction 
Type 
Transaction 
Category 
Transaction 
Code  
Definition 
Initial/Subsequent 
Purchase 
Buys Category 1 50 To obtain ownership of a [[CUSIP]] 
or other [[Asset]] in exchange for 
money or value. Also called a 
“buy.” 
 
Sell/Redemption Sells Category 1 51 The return of an [[investor]]'s 
principal in mutual fund [[shares]], at 
or prior to maturity. 
 
Transfer of [[shares]]  Buys or Sells Category 1 52 When used to move [[shares]] of 
previously purchased mutual 
funds between or within CUSIPs.   
Movement of [[shares]] between 
CUSIPs should be designated 
with the applicable Transaction 
Type associated with the 
transaction.   
Movement of [[shares]] within the 
same [[CUSIP]] is optional as there 
is no financial impact to the 
shareholder or Fund. 

---

## Page 32

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 32 
 
 
 
Transaction Transaction 
Type 
Transaction 
Category 
Transaction 
Code  
Definition 
Automated or 
systematic 
transactions 
Buys or Sells Category 2 53 Transactions related to 
“systematic or programmatic” 
rebalancing, dollar cost averaging, 
and/or systematic 
purchases/withdrawals. 
 
 
Additional Transaction Codes Commonly Utilized by Variable Insurance Firms: 
Transaction Transaction 
Type 
Transaction 
Category 
Transaction 
Code  
Definition 
Credits Buys Category 2 55 Used to report credits received in 
an exchange or as a bonus, such 
as retention, maturity, face 
amount threshold, or interest 
during a period. 
 
Free Look Sells Category 1 56 Cancellation of a contract during 
the period of time or “free look” 
period where the contract is 
terminated and [[Premium]] is 
returned. 
 
Annuitization  Sells Category 2 57 The contract has moved from the 
accumulation to the payout phase 
as a full or partial annuitization. 
 

---

## Page 33

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 33 
 
 
 
Transaction Transaction 
Type 
Transaction 
Category 
Transaction 
Code  
Definition 
Reversals Buys or Sells Category 2 58 Reversal is a financial transaction 
that is processed with a trade date 
earlier than the current date to 
correct the contract holder or 
[[participant]] record by reversing the 
original transaction. 
 
Reversals may result in gains or 
losses to the contract holder; for 
example, when a transaction 
request is received in good order 
before 4:00 p.m., but not 
processed correctly on that day. A 
gain or loss must always be 
handled within the plan or 
[[intermediary]] in which the error 
occurs. 
 
The transaction codes listed above correspond to valid values to be utilized in the SDR Detail Response record 
(field 47-48). 
Data Range Requests 
The SDR Request (F20) record provides functionality for funds to request data for a specific date range by 
providing both a “From Date” and a “To Date” within the F20 Request. Funds electing to request data for a 
specific date range should limit the date range request to a 90-day period. 
Funds are expected to use previously retrieved data rather than making separate and redundant requests. For 
example, if a fund has been requesting recurring daily data for a particular time frame, then the fund should not 
also subsequently request data for the same or overlapping time period using the “from” and “to” dates.  
[[NSCC]] will not validate the “From Date” field except to ensure that it is provided since it is a required field in 
SDR. This date should be set to the current date for requests on the current day's activity and for recurring 
requests. Previous dates are used for historical requests. Future dated requests are not allowed.  
Historical Data Requests 
Historical data requests should be limited to a period of one year. Most systems commonly archive data 
older than one year in a non-production region, which is not generally connected to the production systems into 
which the F20 Request record would be received. Data requests for time periods greater than one year may be 
time-consuming from both a systems and personnel perspective, and therefore should be treated as a one- off. 

---

## Page 34

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 34 
 
 
 
In these cases, the fund must make the data request via phone or other electronic communications directly 
with the [[intermediary]]. 
SDR Acknowledgement 
Intermediaries should always provide an SDR Acknowledgment record to the fund. The Acknowledgment 
should be provided within one business day of receipt of the request. The Acknowledgment record 
provides the fund with affirmative acknowledgment that the SDR request has been received and establishes 
the point in time from which the Best Practices turn-around time will be measured. 
The Acknowledgment Indicator within the record provides for two response types intended to cover the majority 
of acknowledgment responses: 
• 0 = Response will be provided 
• 1 = Request will be forwarded to Underlying Firm 
 
Intermediaries should provide the appropriate response within the acknowledgment.  
In the event that an acknowledgment record will not be sent, intermediaries should provide an SDR Reject 
Record as described below. In instances where the requested data cannot be provided within the Best Practice 
timeframe described below, a dialogue should be initiated with the fund. 
Acknowledgement of Stop Recurring Requests: SDR functionality has been built so that all requests, 
including stop recurring, require an Acknowledgment or Reject. Best Practice: SDR infrastructure has been 
built to require all requests to be acknowledged by intermediaries. For those SDR requests that  go 
unacknowledged, [[NSCC]] will generate reminders for a period of 10 days. Therefore, intermediaries should 
acknowledge all requests received from [[NSCC]] to avoid receiving ongoing reminders.  
SDR Reject Record 
For SDR Request files that pass [[NSCC]]'s preliminary file and record validation, and in cases where an 
[[intermediary]] does not plan to provide an acknowledgement record within one business day and expects to 
reject the request, the [[intermediary]] should provide a reject record as soon as practicable. This shou ld be done 
no later than one business day from the receipt of the data request. 
Funds initiate SDR requests for underlying data (summary and/or detail) from intermediaries. There are 
conditions in which the [[intermediary]] will not be able to respond with data and will need to respond with an 
SDR reject record. Intermediaries should not respond to the fund with an empty header/trailer record in 
lieu of an SDR reject record. Various reject codes are available to the [[intermediary]] to designate the 
reasoning as to why a fund's request for data will not be satisfied. Please refer to the Standardized Data 
Reporting (SDR) Reject Codes for complete listing of all reject codes. 

---

## Page 35

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 35 
 
 
 
In cases where funds submit Plan Level (Detail) Data SDR Requests for fund accounts in which only summary 
level information is available, intermediaries should reject the request with Reject Code 81– "Account is Non-
Omnibus (Single Shareholder)". An example of this would be a fund submitting a detailed data request either 
as an initial request on a fully disclosed account, or as a follow-up data request to a summary data request for 
which data was previously provided on an account for a Defined Benefit or Pension Plan.  
In cases where funds submit Plan Level data requests for underlying [[participant]] d ata within a specific Plan, but 
the Plan is no longer present on the [[intermediary]]'s recordkeeping system, intermediaries should reject the 
request with Reject Code A2-"Plan [[ID]] Requested is Closed". 
In cases where funds submit SDR requests when there is an absence of trade data for the NAV date(s) 
requested, the [[intermediary]] should reject the requests using Reject Code A3- "Request Criteria Matched-No 
Transaction Activity Exists". If funds submit SDR requests for Category 1 transactions, yet only Category 2 
transactions occurred for the NAV date(s) requested, they should also be rejected by the [[intermediary]] using 
Reject Code A3. The following outlines the two scenarios and best practices guidelines on the handling of the 
SDR data requests when all account criteria are met but there is no corresponding transaction activity 
processed for the requested date or time period. 
Scenario 1 
Request for data (single day or multiple days) where no trade activity has been communicated to the fund by 
the [[intermediary]]. 
Best Practices: 
• As a matter of course, funds should not send SDR requests for summary and/or detail data for dates 
(single or multiple days) on which the funds have no trades booked from the [[intermediary]] to whom the 
SDR request would be submitted. 
• For situations where a fund submits a single-date or multiple-day SDR request to an [[intermediary]] for a 
date or date range on which the [[intermediary]] did not communicate/confirm trading, the SDR request 
should be rejected by the [[intermediary]] via a reject code of A3–"Requested Criteria Matched-No 
Transaction Activity Exists”. 
Scenario 2 
Request for data (single day or multiple days) where trade activity has been communicated to the fund by the 
[[intermediary]]; however, there is no Category 1 trade information to report.  
• Intermediaries must provide Category 1 trade activity unless otherwise specified within the SDR request 
by the fund. For instances where a fund submits a single date or multiple day SDR request to an 
[[intermediary]] for a date or date range on which the [[intermediary]] does not have records of Category 1 
trades, the SDR request should be rejected by the [[intermediary]] via a reject code of A3– "Requested 

---

## Page 36

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 36 
 
 
 
Criteria Matched-No Transaction Activity Exists". This scenario assumes that the SDR request 
submitted by the fund is following the established best practice: [[DO]] not include Category 2 transactions 
(Category 1 transactions only). 
• For instances where a fund submits a single date or multiple day SDR request to an [[intermediary]] for both 
Category 1 and Category 2 transactions for a date or date range on which the [[intermediary]] does not have 
record of Category 1 trade information, the [[intermediary]] should respond to the fund with the applicable 
Category 2 data, if it exists. 
 
Note 
Multiple Day Requests: In cases where a fund makes a multiple day request (e.g., a seven-day request) for which trade 
data is available for only five of the seven days, the [[intermediary]] should provide the data for those five days based only on 
the criteria in the request file. For those days (e.g., two) where no data is provided, it should be understood that no data is 
available; funds should be able to reconcile the lack of no trade data by reviewing its books and records to confirm that no 
trade was booked for those days for that [[intermediary]]. In situations where the lack of a response does not reconcile to the 
fund’s records, subsequent SDR requests should be made for the dates in question. 
Using the example above, if the [[intermediary]] is providing five of the seven days, and those five days represent  
all of the activity for the SDR request, the [[intermediary]] could set the Partial Response Indicator to 0 (Full/Final 
Response) or 2 (Incomplete/Final Response), whichever is appropriate for the transmitted data. This should 
alert the fund that no data is available for the other two days. If the [[intermediary]] provides five of the seven days 
but is still investigating the other two days, the [[intermediary]] could set the Partial Response Indicator to 1 
(Partial Response) to alert the fund that more detail may be provided separately.  
Incomplete Responses 
In situations where intermediaries are not able to complete a request, the final response file should be marked 
with a value of "2" = Incomplete/Final Response in the Partial Response Indicator field. This will indicate to the 
fund that some information has been provided but the [[intermediary]] cannot provide a complete response to fully 
satisfy the request. 
For example, a Super Omnibus Fund Account contains five accounts on the Trust System. Four out of the five 
accounts are [[participant]]-level accounts, but the fifth account is an omnibus plan held at another external 
system for which the [[intermediary]] cannot get data. The data for the four accounts should be sent to the fund, 
and the file (or the last of multiple files) should be marked as an Incomplete/Final Response. 
The fund would then know that the information is incomplete, and that no additional files or information will be 
sent by the [[intermediary]]. The fund can work with the [[intermediary]] outside of the system to gather the missing 
data. 

---

## Page 37

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 37 
 
 
 
Request Time for Data Requests 
Rule 22c-2 requires that intermediaries provide funds with shareholder and transaction activity upon request. 
Funds and firms will enter into agreements, which will govern the response timeframes for t hese requests. 
As a best practice when utilizing the SDR functionality, intermediaries should adhere to a process whereby 
routine SDR data requests are processed and responded to within 1-5 business days for routine requests. 
A routine SDR data request is defined as an SDR request that falls within the best practice for date 
range and for Category 1 transactions. 
Additionally, funds and intermediaries should agree on timeframes for data requests that may inherently result 
in a voluminous amount of data or are complex and cannot be processed within existing cycles without 
interrupting day-to-day operations. Additional time may be required during high-volume processing times such 
as month-end, quarter-end, or year-end batch cycles. 
Funds and intermediaries should also consider establishing a timeframe for situations where the first -tier 
[[intermediary]] does not maintain the requested data on its internal systems. The data may be maintained by an 
Underlying [[intermediary]]; therefore, the first-tier [[intermediary]] will be dependent on the Underlying [[intermediary]] 
to provide the data. This situation may warrant additional time for the first-tier [[intermediary]] to retrieve data from 
the Underlying [[intermediary]] and to subsequently respond to the fund's data request.  
Notwithstanding the special situations described above, the best practice is to reply to fund requests for data is 
1-5 business days, unless otherwise previously negotiated between the funds and intermediaries. Within a 
chain of [[intermediary]] relationships, the best practice to replying to fund requests for data is 5-10 business 
days, unless otherwise previously negotiated between the fund and intermediaries.  
In circumstances where SDR data requests cannot be completed within the best practice timeframe described 
above or otherwise previously negotiated, intermediaries should provide the requested data within the 
prescribed time contained within the required written agreement with the funds.  
The following is an example of the flow for routine SDR requests responded to within the best practice 
standard of 1-5 business days: 
Step 1: Day 0 
• Fund initiates data request SDR F20 request type 01 or 02. 
• [[NSCC]] processes data request. 
• [[intermediary]] receives the request and acknowledges receipt via an acknowledgement record. The 
acknowledgment marks the point in which the turnaround time for the data response is based.  
 
Step 2: Day 1–5 
• [[intermediary]] processes SDR request. 

---

## Page 38

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 38 
 
 
 
• [[intermediary]] responds to fund within five business days unless otherwise previously agreed upon with the 
fund initiating the SDR request. 
 
Step 3: Day 6–x 
• Fund analyzes data from [[intermediary]]. 
• For Super Omnibus Accounts, fund analyzes the summary plan data to determine if additional detailed 
shareholder data is required from [[intermediary]] and the detailed data provided for individual accounts. 
• For Omnibus accounts, the response record will contain detailed shareholder data.  
 
Step 4: Day x 
• For Super Omnibus Accounts, if the fund (after analyzing the summary level data provided in the 
response record by the [[intermediary]]) determines that additional data is required from financial 
[[intermediary]], a detailed data request SDR F20, data request type 02, 03 is submitted to [[NSCC]] specifying 
which plan, trust, or [[investor]] omnibus account requires individual [[investor]]-level data. 
• This additional request initiates a new cycle beginning with Step 1 above.  
• Shareholder trade data from 2nd tier intermediaries will require 10 days to respond.  
Summary Data 
Summary data is the high-level information regarding the plans, trusts, and/or [[investor]] omnibus accounts that 
are combined into a super omnibus account. It is assumed that only summary data will first be passed for plans 
or trusts in super omnibus accounts. This summary data will provide sufficient information to help the funds 
identify specific plans where trading is occurring frequently. The fund would then be able to request data at a 
plan/trust level and obtain detailed information about the underlying participants. The same will apply to the 
trusts, [[investor]] omnibus accounts, and the underlying shareholders. If a super omnibus account also contains 
individual accounts, then individual [[investor]] data will be passed as well. 
The process of first providing summary data is necessary because a request against a super omnibus account 
may produce a prohibitive amount of response data at a shareholder level. To avoid having to process this 
large amount of data for super omnibus accounts, summary data will instead be provided.  
In scenarios where the data request is made of a first-tier [[intermediary]] that also provides [[participant]]/contract or 
policyholder/shareholder recordkeeping services, the [[intermediary]] should, to the greatest extent possible that 
the data is maintained and accessible, provide all the optional/conditional data on SDR Summary rec ord      
B/U 25 for response types 1 and 2 including, but not limited to: 
1. Dollar Value of All [[participant]]/Shareholder Buys 
2. Dollar Value of All [[participant]]/Shareholder Sells 
3. Dollar Value of Category 1 [[participant]]/Shareholder Buys 
4. Dollar Value of Category 1 [[participant]]/Shareholder Sells 

---

## Page 39

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 39 
 
 
 
5. Number of Category 1 [[participant]]/Shareholder Buys 
6. Number of Category 1 [[participant]]/Shareholder Sells 
7. Dollar Value of All of [[participant]]/Shareholder Exchanges (Intra Fund Buy-Side) 
8. Dollar Value of All [[participant]]/Shareholder Exchanges (Intra Fund Sell-Side) 
9. Dollar Value of Category 1 of [[participant]]/Shareholder Exchanges (Intra Fund Buy-Side) 
10. Dollar Value of Category 1 [[participant]]/Shareholder Exchanges (Intra Fund Sell-Side) 
11. Number of Category 1 [[participant]]/Shareholder Exchanges (Intra Fund Buy-Side) 
12. Number of Category 1 [[participant]]/Shareholder Exchanges (Intra Fund Sell-Side) 
13. Number of [[shares]] in Plan/[[investor]] Omnibus Account 
 
In scenarios where the summary data request is made of a first-tier [[intermediary]] that does not provide 
[[participant]]/shareholder recordkeeping services, the [[intermediary]] should provide the summary data that is 
maintained, which at a minimum should contain the dollar value of all buys and sells.  
Social Code 
To provide adequate disclosure within the summary data, Intermediaries should provide the appropriate “social 
code” (if known) in the Summary record. The social code should be populated or left blank if not known.  
The social code will provide a unique identifier to help funds determine whether the lowest level of data is being 
provided based on the account type indicated by the social code. The availability of the social code may help to 
eliminate subsequent SDR detail requests for accounts on which no additional data is maintained by the 
[[intermediary]], such as “53 Defined Benefit Plan (non-prototype)”. 
Social Codes on which funds would seek additional detail data include:  
Social Code [[NSCC]] Social Code Best Practice Usage 
05 Insurance [[Companies]]  Use for Insurance Company product accounts that are fund level 
omnibus.   
Best Practice: Firm is responsible for tax reporting.  
06 [[Broker]]/Dealer Omnibus  Use for [[Broker]]/Dealer house accounts that are fund level 
omnibus.  
Best Practice: Firm is responsible for tax reporting. 
07 Bank/Trust Omnibus  Use for Bank and Trust accounts that are fund level omnibus.  
Best Practice: Firm is responsible for tax reporting. 
11 Profit Sharing Plan (non-
prototype)  
Use for Insurance Company product accounts that are fund level 
omnibus.   
Best Practice: Firm is responsible for tax reporting.  
12 401(k) Plan (non-
prototype) 
Use for non-prototype 401(k) accounts maintained in plan level 
omnibus accounts.   

---

## Page 40

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 40 
 
 
 
Social Code [[NSCC]] Social Code Best Practice Usage 
Best Practice: Firm is responsible for tax reporting. 
13 Money Purchase Pension 
Plan (non-prototype) 
 
Use for non-prototype pension plans which are maintained in a 
plan level omnibus account.   
Best Practice: Firm is responsible for tax reporting. 
19 403(b) (non-prototype)  Use for non-prototype 403(b) accounts maintained at the plan 
level omnibus level. Firm is responsible for tax reporting.  
43 Profit Sharing Plan FBO 
[[participant]] 
Name/Account # (fund-
prototype) 
Use for fund-prototype profit sharing plans which are maintained 
at the [[participant]] FBO account level.  
Best Practice: Fund is responsible for tax reporting.  
48  Health Savings Account 
(HSA) (non-prototype)  
Use for non-prototype Health Savings Accounts which are 
maintained in a plan level omnibus account.  
Best Practice: Firm is responsible for tax reporting. 
51 Non-Qualified Deferred 
Compensation Plan (non-
prototype; [[participant]] 
directed) 
Use for non-prototype, non-qualified deferred compensation plans 
which are maintained in a plan level omnibus account. 
Participants direct investments in these accounts.   
Best Practice: Firm is responsible for tax reporting. 
58 Roth 401(k) Plan (non-
prototype) 
Use for non-prototype, Roth 401(k) accounts which are 
maintained at a plan omnibus level.  
Best Practice: Firm is responsible for tax reporting. 
60 Roth 403(b) Plan (non-
prototype) 
Use for non-prototype, Roth 403(b) accounts which are 
maintained at the plan omnibus level. 
Best Practice: Firm is responsible for tax reporting. 
 
Note: 
The use of the term "non-prototype" in the context of Social Codes is from the fund's perspective. Therefore, an 
[[intermediary]] that provides services to a custom and prototype 401K plan (other than those utilizing a fund prototype 
document) may report the plan as a social code 12 – 401K (non-prototype). 
 
A full listing of Social Codes can be found on  [[DTCC]] Learning under Codes in the Mutual Fund section 
https://dtcclearning.com/products-and-services/mutual-fund-services.html 
 
 
 

---

## Page 41

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 41 
 
 
 
Super Omnibus Accounts 
For a super omnibus account, the first data response from intermediaries to funds should be summary level 
data. If after reviewing the summary data from the [[intermediary]], the fund determines that additional trade data 
is warranted, the fund should submit a detailed data request to retrieve shareholder data.  
The following flow charts provide an overview of the flow for an SDR data request from a fund to an 
[[intermediary]] for a super omnibus relationship. 
For a super omnibus account, funds will receive summary data at a plan or account level. The fund will review 
the overall trading activity in these accounts to determine if additional shareholder data is required within a 
particular plan or [[investor]] omnibus account. The fund may then submit a subsequent request for additional 
data. 
Model #1 
The model depicted in the following flowchart is one where the first-tier [[intermediary]] is both the trading conduit 
and shareholder recordkeeper on a Super Omnibus account, which holds Plan Level sub- accounts.  
Process for Super Omnibus Accounts Where Account Holds Only Plan Level Accounts
 


---

## Page 42

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 42 
 
 
 
Process Flow 
• Fund sends a data request to [[NSCC]] during the acceptable input timeframe. 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records. 
• [[NSCC]] stages the records to the appropriate destination and output files. 
• At the appropriate output time, [[NSCC]] sends rejects back to the fund and accepted records to the 
intermediaries. 
• The [[intermediary]] will take the data request records and may run some preliminary validation, which will 
result in accepted or rejected records. 
• If [[intermediary]] rejects, then the reject record will be submitted to [[NSCC]] during the input timeframe. [[NSCC]] 
will pass back to the fund in the output file. 
• If [[intermediary]] accepts, then it will process the request. 
o The first step is for the [[intermediary]] to prepare and submit an Acknowledgment to [[NSCC]] during the 
appropriate input timeframe. 
o [[NSCC]] will pass to the fund in the output file. 
• The [[intermediary]] will query its systems and provide the data response record to [[NSCC]] within the agreed-
upon timeframes with the fund. 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records.  
• At the appropriate output time, [[NSCC]] sends rejects back to the [[intermediary]] and accepted data records to 
the funds. 
• If the funds, after reviewing and analyzing the summary level data for compliance with the funds' market 
timing policies, determine that additional data is required, then funds would submit a detailed data 
request. 
 
The detailed data request should be focused on a specific plan/account, and to the extent possible on 
Category 1 transactions. An appropriate level of detail should be provided such that the [[intermediary]] can filter 
out unwanted or unneeded data in the detailed data response record. 
Model #2 
The model depicted in the following flowchart is one where the first-tier [[intermediary]] is both the trading conduit 
and shareholder recordkeeper on a Super Omnibus account, which holds Plan Level and individual 
shareholder accounts. 
 
 
 
 

---

## Page 43

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 43 
 
 
 
Process for Super Omnibus Accounts where account holds plan and [[participant]] accounts  
 
Process Flow 
• Fund sends a data request to [[NSCC]] during the acceptable input timeframe. 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records.  
• [[NSCC]] stages the records to the appropriate destination and output files. 
• At the appropriate output time, [[NSCC]] sends rejects back to the fund and accepted records to the 
intermediaries. 
• The [[intermediary]] will take the data request records and may run some preliminary validation, which will 
result in accepted or rejected records. 
• If [[intermediary]] rejects, then the reject record will be submitted to [[NSCC]] during the input timeframe. [[NSCC]] 
will pass back to the fund in the output file. 
• If [[intermediary]] accepts, then it will process the request. 
o The first step is for the [[intermediary]] to prepare and submit an Acknowledgment to [[NSCC]] during the 
appropriate input timeframe. 
o [[NSCC]] will pass to the fund in the output file. 
• The [[intermediary]] will query its systems and provide the data response record to [[NSCC]] within the agreed-
upon timeframes with the fund. 
• The [[intermediary]] will provide summary data for plan level accounts and detail data for individual 
shareholders held in subaccounts within the super omnibus accounts. 


---

## Page 44

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 44 
 
 
 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records.  
• At the appropriate output time, [[NSCC]] sends rejects back to the [[intermediary]] and accepted data records to 
the funds. 
• If the funds, after reviewing and analyzing the summary level data for compliance with the funds' market 
timing policies, determine that additional data is required, then funds would submit a detailed data 
request. 
 
The detailed data request should be focused on a specific plan/account, and to the extent possible on 
Category 1 or Category 2 transactions. An appropriate level of detail should be provided such that the 
[[intermediary]] can filter out unwanted or unneeded data in the detailed data response record. 
Model #3 
The model depicted in the following flowchart is one where the first-tier [[intermediary]] is both the trading conduit 
and shareholder recordkeeper on a Super Omnibus account with Plan Level sub-accounts on which the 
[[intermediary]] has previously provided summary level data to the Fund. The Fund is subsequently submitting a n 
SDR request for Detail for identified plans. 
Process for Requesting Detailed Data Within a Super Omnibus Account 
 


---

## Page 45

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 45 
 
 
 
Process Flow 
• Fund sends a data request to [[NSCC]] during the acceptable input timeframe. 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records.  
• [[NSCC]] stages the records to the appropriate destination and output files. 
• At the appropriate output time, [[NSCC]] sends rejects back to the fund and accepted records to the 
intermediaries. 
• The [[intermediary]] will take the data request records and may run some preliminary validation, which will 
result in accepted or rejected records. 
• If [[intermediary]] rejects, then the reject record will be submitted to [[NSCC]] during the input timeframe. [[NSCC]] 
will pass back to the fund in the output file. 
• If [[intermediary]] accepts, then it will process the request. 
o The first step is for the [[intermediary]] to prepare and submit an Acknowledgment to N SCC during the 
appropriate input timeframe. 
o [[NSCC]] will pass to the fund in the output file. 
• The [[intermediary]] will query its systems and provide the data response record to [[NSCC]] within the agreed 
upon timeframes with the fund. 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records. 
• At the appropriate output time, [[NSCC]] sends rejects back to the [[intermediary]] and accepted data records to 
the funds. 
Omnibus Accounts 
Funds will be able to retrieve the underlying shareholder transaction information within a specified omnibus 
account. If the fund has the specific plan [[ID]] or [[investor]] omnibus account number, then this information should 
be provided on the request to help the [[intermediary]] focus on a specific plan/accou nt. 
Additionally, if the fund has determined that it needs both Category 1 and 2 transactions, then the fund should 
indicate this on the request. An appropriate level of detail should be provided such that the [[intermediary]] can 
filter out unwanted or unneeded data in the detailed data response record.  
 
The model depicted in the following flowchart is one where the first-tier [[intermediary]] is both the trading conduit 
and shareholder recordkeeper on an Omnibus account. 
 
 
 
 

---

## Page 46

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 46 
 
 
 
Omnibus Account Process 
 
Process Flow 
• Fund sends a data request to [[NSCC]] during the acceptable input timeframe. 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records.  
• [[NSCC]] stages the records to the appropriate destination and output files. 
• At the appropriate output time, [[NSCC]] sends rejects back to the fund and accepted records to the 
intermediaries. 
• The [[intermediary]] will take the data request records and may run some preliminary validation, which will 
result in accepted or rejected records. 
• If [[intermediary]] rejects, then the reject record will be submitted to [[NSCC]] during the input timeframe. [[NSCC]] 
will pass back to the fund in the output file. 
• If [[intermediary]] accepts, then it will process the request. 
o The first step is for the [[intermediary]] to prepare and submit an Acknowledgment to [[NSCC]] during the 
appropriate input timeframe. 
o [[NSCC]] will pass to the fund in the output file. 
• The [[intermediary]] will query its systems and provide the data response record to [[NSCC]] within the agreed-
upon timeframes with the fund. 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records. At the appropriate 
output time, [[NSCC]] sends rejects back to the [[intermediary]] and accepted data records to the funds.  


---

## Page 47

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 47 
 
 
 
Chain of [[intermediary]] Relationships 
Business relationships exist where one or more underlying intermediaries transact business with a fund 
through a first-tier [[intermediary]] that acts as the trading conduit. The first-tier [[intermediary]] commonly does not 
provide shareholder recordkeeping services in this type of construct. 
The following flowchart provides a flow for requests that are either a subsequent data request for Super 
Omnibus accounts, or an initial data request for an Omnibus account in a Chain of [[intermediary]] relationshi p. 
Detail request process in chain of [[intermediary]] relationship where shareholder data is maintained by 
Underlying [[intermediary]]
 
 
Process Flow 
• Fund sends a data request to [[NSCC]] during the acceptable input timeframe. 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records. 
• [[NSCC]] stages the records to the appropriate destination and output files. 
• At the appropriate output time, [[NSCC]] sends rejects back to the fund and accepted records to the 
intermediaries. 


---

## Page 48

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 48 
 
 
 
• The [[intermediary]] will take the data request records and may run some preliminary validation, which will 
result in accepted or rejected records. 
• If [[intermediary]] rejects, then the reject record will be submitted to [[NSCC]] during the input timeframe. [[NSCC]] 
will pass back to the fund in the output file. 
• If [[intermediary]] accepts, then it will process the request. 
o The first step is for the [[intermediary]] to prepare and submit an Acknowledgment to [[NSCC]] during the 
appropriate input timeframe. 
o [[NSCC]] will pass to the fund in the output file. 
• If the First-Tier [[intermediary]] acts as the conduit for data requests: 
a. The first-tier [[intermediary]] will work with the underlying [[intermediary]] to gather the requested data.  
b. The Underlying [[intermediary]] will query its systems and provide the data response record to the first-
tier [[intermediary]]. The response to the first-tier [[intermediary]] may be via [[NSCC]] or otherwise and will 
be negotiated between the first-tier [[intermediary]] and the underlying [[intermediary]]. 
c. The first-tier [[intermediary]] will respond to [[NSCC]] within the agreed-upon timeframes. 
• [[NSCC]] does a preliminary validation, which will result in accepted or rejected records. At the appropriate 
output time, [[NSCC]] sends rejects back to the [[intermediary]] and accepted data records to the funds.  
• If the First-Tier [[intermediary]] does not act as the conduit for data requests: 
a. Work with the fund to contact the underlying [[intermediary]] that maintains the shareholder level data.  
b. Disclose to the fund the contact information for the underlying [[intermediary]] that maintains the 
shareholder level data. 
c. The fund would follow up and work with the first-tier and underlying intermediaries as to the 
mechanism and timing for the response of the requested data. 
d. Response may be provided via [[NSCC]] or otherwise and will be negotiated between the funds and the 
underlying [[intermediary]]. 
SDR Control Number and SDR Response Number 
SDR Control Number 
The SDR Control Number is the unique number that identifies the fund's request for data. The format outlined 
below and in the SDR record layouts will not be validated by [[NSCC]]; but, should be followed as a best practice. 
[[NSCC]] will only validate that the number is provided since the field is required. 
The SDR Control Number is always required. On the Response Header, when the request is initiated outside 
[[NSCC]] (and therefore does not have a fund-generated SDR Control Number), the [[intermediary]] should still 
provide an SDR Control Number (and may be the same as the SDR Response Number; see below).  
ppppyjjjnnnnnnn 
pppp = [[participant]] Number  

---

## Page 49

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 49 
 
 
 
y = Last digit of year 
jjj = Julian Date 
nnnnnnn = Unique sequential number assigned by the fund. 
SDR Response Number 
The SDR Response Number is the unique number that identifies the SDR response, either to an SDR request 
via [[NSCC]] or a request done outside the [[NSCC]]. The format outlined below and in the SDR record layouts will 
not be validated by [[NSCC]]; but, must be followed as a best practice. [[NSCC]] will only validate that the number is 
provided since the field is required. 
ppppyjjjnnnnnnn 
pppp = [[participant]] Number  
y = Last digit of year 
jjj = Julian Date 
nnnnnnn = Unique sequential number assigned by the [[intermediary]]. 
Several SDR Response Numbers may correspond to a single SDR Request Control Number when partial files 
are provided, or when there are daily files sent for recurring requests. In these situations, the SDR Response 
Number will be important if a correction needs to be made for a specific response file.  
Correction Indicator and Fund/SERV® Correction Orders 
Correction Indicator 
The correction indicator is only used to correct an entire file of data that was previously sent by an 
[[intermediary]]. The correction indicator applies to the response for a particular SDR request, identified by the 
SDR Control Number and the SDR Response Number for a particular date (e.g., for historical or recurring).  
The records contained within the Main Header that is indicated as a correction should replace and overwrite 
the original records 
Fund/SERV® Correction Orders 
Data requests on Fund/SERV® correction orders will require the Fund/SERV® control number, but not the 
Fund/SERV® correction indicator. Data provided on a control number will be assumed to be for the final status 
of the order, which may be a corrected order. 

---

## Page 50

Standardized Data Reporting Best Practices 
 
 
 
Best Practices 50 
 
 
 
Recurring Accounts, Foreign Accounts and Restrictions 
Recurring Requests 
The recurring indicator is used to request daily data from the [[intermediary]] on an ongoing basis and until the 
recurring request is "stopped" by the fund. The activity date for the first file should be the dat e on which the 
[[intermediary]] received the request, regardless of the date provided in the "From Date" field. To avoid confusion, 
funds should follow the best practice of using the current date on a recurring request. The original SDR Control 
Number is required by the fund when stopping the recurring request. 
Foreign Accounts 
Intermediaries that provide shareholder recordkeeping services may hold foreign accounts for non- resident 
aliens that [[DO]] not have social security numbers. Intermediaries should include t hese accounts in the response 
data provided to the funds by identifying them with the appropriate ITIN or GIIN, or a dummy SSN such as 999-
99-999 when ITINs or GIINs are not available. The SSN/TIN field is required and cannot be left blank. Funds 
may then question these accounts and obtain additional information via verbal communication with the 
intermediaries. 
Restrictions 
Restrictions and warnings are not supported by SDR Networking at this time. Although best practices were 
discussed by the Standardized Data Reporting Working Group and common practices were outlined, it is 
incumbent upon the parties to negotiate the method and timing with enforcement.  

---

## Page 51

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 51 
 
 
 
APPENDIX A 
Financial Activity Reporting (FAR) Transaction Type Definitions with SDR 
Category and Transaction Codes 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
29 Exchange 
Credit 
  2 60 Buy  Client Used to report lump 
sum credit received 
when one contract is 
exchanged for 
another. 
129 Exchange 
Credit 
Reversal 2 63    Reversal of Exchange 
Credit (129). 
95 Extra Credit   2 60 Buy  Carrier For an interest bonus 
on a certain period, a 
credit is issued. Used 
to report cash value 
adjustments.  
188 Extra Credit Reversal 2 63    Reversal of an 
interest bonus on a 
certain period, a credit 
is issued. Used to 
report reversal cash 
value adjustments.  
98 Fixed Bonus   2 60 Buy  Carrier Carrier contribution 
into a contract due to 
a fixed bonus, which 
may be a maturity 
bonus, persistency 
bonus, or retention 
bonus.  
191 Fixed Bonus Reversal 2 63    Reversal of carrier 
contribution into a 
contract due to a fixed 
bonus, which may be 
a maturity bonus, 
persistency bonus, or 
retention bonus. 
90 Internal 
[[Premium]] 
  1 50 Buy  Client Used by carriers for 
receipt of the 
[[Premium]] from internal 
surrender for the 
purchase of a new 
contract.  Also:  
internal product 
exchange on a non-
qualified contract or 
ambiguous 
exchanges. 

---

## Page 52

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 52 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
183 Internal 
[[Premium]] 
Reversal 2 63    Cancellation of 
[[Premium]] received 
from internal 
surrender for the 
purchase of a new 
contract. 
91 Internal 
Rollover 
  1 50 Buy  Client Used by carriers for 
receipt of the 
[[Premium]] from an 
internal surrender for 
the purchase of a new 
contract.  Also:  
internal product 
exchange on a 
qualified contract. 
184 Internal 
Rollover 
Reversal 2 63    Cancellation of 
[[Premium]] received 
from internal 
surrender for the 
purchase of a new 
contract. 
40 Jumbo Credit   2 60 Buy  Carrier Extra interest credit if 
a certain [[Premium]] 
amount is reached. 
140 Jumbo Credit Reversal 2 63    Reversal of extra 
interest if a certain 
[[Premium]] amount is 
reached. 
93 Other 
Contribution 
  2 03 Buy  Carrier Catch-all for added 
payments that are 
made to the policy by 
the carrier.  
186 Other 
Contribution 
Reversal 2 63    Reversal of added 
payments that are 
made to the policy by 
the carrier.  
75 [[Premium]] – New 
(Original) 
  1 50 Buy  Client Initial payment 
received on the 
contract. 
76 [[Premium]] – New 
(Original) 
Reversal 2 63    Reversal of initial 
payment received on 
the contract. 
78 [[Premium]] – 
Subsequent 
  1 50 Buy  Client Additional payment 
received on the 
contract. May include 
[[Premium]] paid by loan. 
79 [[Premium]] – 
Subsequent 
Reversal 2 63    Reversal of additional 
payment received on 
the contract. May 
include [[Premium]] paid 
by loan. 

---

## Page 53

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 53 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
415 Loan 
Repayment 
  2 04 Buy  Client A loan payment 
received by the policy 
owner to reduce the 
loan balance which 
could include principal 
and/or interest. 
514 Loan 
Repayment 
Reversal 2 63    Reversal of a loan 
payment received by 
the policy owner to 
reduce the loan 
balance which could 
include principal 
and/or interest. 
LRI Loan 
Repayment 
Interest 
  2 05 Buy  Client Categorizes interest 
separate from 
principal 
199 Loan 
Repayment 
Interest 
Reversal 2 63    Reversal of 
categorizing interest 
separate from 
principal 
19 Reinstatement   2 03 Buy  Client Payment received on 
policy that was in 
lapsed status which 
puts the policy back in 
force. Formally 
'Cancellation 
(Reinstatement)'. 
119 Reinstatement  Reversal 2 63    Reversal of payment 
received on policy 
that was in lapsed 
status which puts the 
policy back in force. 
Formally 'Cancellation 
(Reinstatement)'. 
419 Bill PAC   1 50 Buy  Client Not used for Life 
processing. 
414 Face Decrease   2 22 Buy  Client Not used for Life 
processing.  
413 Face Increase   2 22 Buy  Client Not used for Life 
processing. A non-
financial activity. 
27 Interest 
Crediting  
  Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Posting or crediting of 
interest to a fixed 
account. 
127 Interest 
Crediting  
Reversal Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Reversal of posting or 
crediting of interest to 
a fixed account. 

---

## Page 54

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 54 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
13 Adjustment – 
Units 
  2 07 Buy/Sell Carrier Unit adjustment 
transaction to make a 
correction to the fund 
units due to an 
insurance carrier 
administrative 
adjustment. Could 
change policy value, 
either increasing or 
decreasing. 
113 Adjustment – 
Units 
Reversal 2 63    Reversal of unit value 
correction. 
28 Adjustment - 
Value  
  2 07 Buy/Sell Carrier Value adjustment 
transaction to make a 
correction to the 
policy cash value. 
Could increase or 
decrease policy cash 
value. 
128 Adjustment - 
Value 
Reversal 2 63    Reversal of value 
adjustment 
transaction. 
14 Administrative 
Fee 
  2 22 Sell Carrier Other charges 
assessed against the 
policy for 
administration. 
114 Administrative 
Fee 
Reversal 2 63    Reversal of other 
charges assessed 
against the policy for 
administration. 
15 Annual Fee   2 22 Sell Carrier Yearly administrative 
charges. 
115 Annual Fee Reversal 2 63    Reversal of yearly 
administrative 
charges. 
94 Fee [[liquidation]]   2 22 Sell Carrier Fee liquidations are 
used to represent fee 
payments withdrawn 
from the annuity 
contract such as fees 
for Investment 
Advisor services, 
Annual Enhanced 
Death Benefit Rider 
fees, and Guaranteed 
Minimum Withdrawal 
Benefit fees. 
187 Fee [[liquidation]] Reversal 2 63    Reversal of Fee 
[[liquidation]] (94) 
65 Front End Load   Does Not 
Apply  
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
The sales commission 
charged at the time of 
purchase.  

---

## Page 55

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 55 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
165 Front End Load Reversal Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Reversal of the sales 
commission charged 
at the time of 
purchase.  
125 Cost of 
Insurance 
  2 22 Sell Carrier A charge applied for 
the cost of insurance 
based on insured age, 
sex, smoker status, 
etc. and the net 
amount at risk. 
521 Cost of 
Insurance 
Reversal 2 63    Reversal of a charge 
applied for the cost of 
insurance based on 
insured age, sex, 
smoker status, etc. 
and the net amount at 
risk. 
26 Mortality and 
Expense Risk 
Charge 
  2 22 Sell Carrier Fee designed to cover 
various risks and 
expenses assumed 
by the insurer. 
126 Mortality and 
Expense Risk 
Charge 
Reversal 2 63    Reversal of fee 
designed to cover 
various risks and 
expenses assumed 
by the insurer. 
42 Loan Payout   2 12 Sell Client Charge to the loan 
balance as a result of 
an automatic [[Premium]] 
loan, loan interest 
capitalization, or 
payment requested 
loan amount to the 
policy owner.   
196 Loan Payout Reversal 2 63    Reversal of charge to 
the loan balance as a 
result of an automatic 
[[Premium]] loan, loan 
interest capitalization 
or payment requested 
loan amount to the 
policy owner.  
23 Death Claim   2 15 Sell Client All portions of death 
benefit payable upon 
death to beneficiary. 
123 Death Claim Reversal 2 63    Reversal of all 
portions of death 
benefit payable upon 
death to beneficiary. 

---

## Page 56

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 56 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
30 Free Look   1 61 Sell Client A cancellation of a 
contract during the 
period of time 
immediately after 
contract issue in 
which the client may 
choose to terminate 
the contract.  
Typically, at least 10 
days from the contract 
issue date.  
182 Free Look Reversal 2 63    Reversal of a 
cancellation of a 
contract during the 
period of time 
immediately after 
contract issue in 
which the client may 
choose to terminate 
the contract.  
Typically, at least 10 
days from the contract 
issue date. - See 
comment in 30. 
32 Free Look 
[[Premium]] 
Cancellation 
  1 61 Sell Client Cancellation of 
contract during free 
look period resulting 
in return of [[Premium]] 
to policy owner. 
130 Free Look 
[[Premium]] 
Cancellation 
Reversal 2 63    Reversal of 
cancellation of 
contract during free 
look period resulting 
in return of [[Premium]] 
to policy owner. 
31 Free Look 
Value 
Cancellation 
  1 61 Sell Client Cancellation of 
contract during free 
look period resulting 
in return of policy 
value to policy owner. 
131 Free Look 
Value 
Cancellation 
Reversal 2 63    Reversal of 
cancellation of 
contract during free 
look period resulting 
in return of policy 
value to policy owner. 
16 Full 
Annuitization 
  2 62 Sell Client Total contract amount 
has moved to the 
payout phase. 
116 Full 
Annuitization 
Reversal 2 63    Reversal of the total 
contract amount to 
moving to the payout 
phase. 

---

## Page 57

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 57 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
33 Full Surrender   2 17 Sell Client A complete surrender 
of the policy resulting 
in a lump sum 
payment to the policy 
owner. 
133 Full Surrender Reversal 2 63    Reversal of a 
complete surrender of 
the policy resulting in 
a lump sum payment 
to the policy owner. 
92 Internal 
Surrender 
  2 17 Sell Client This is used for any 
internal surrender 
such as an exchange 
or lapse.   
195 Internal 
Surrender 
Reversal 2 63    Reversal of any 
internal surrender 
such as an exchange 
or lapse. See 
comment for 92. 
44 Minimum 
Required 
Distribution 
Payout 
  2 19 Sell Client Required payment to 
client on qualified 
plans when client has 
attained age 70 1/2.  
145 Minimum 
Required 
Distribution 
Payout 
Reversal 2 63    Reversal of comment 
for 44 
206 Over 
Contribution 
Withdrawal 
  2 24 Sell Client/Carrier Client-initiated 
withdrawal to correct 
an over-contribution 
to a qualified plan.  
306 Over 
Contribution 
Withdrawal 
Reversal 2 63    Reversal of a client-
initiated withdrawal to 
correct an over-
contribution to a 
qualified plan. 
47 Partial 
Annuitization 
  2 62 Sell Client Partial conversion of 
policy value from the 
accumulation phase 
to the payout phase.  
147 Partial 
Annuitization 
Reversal 2 63    Reversal of a partial 
conversion of policy 
value from the 
accumulation phase 
to the payout phase.  
48 Partial 
Surrender 
  1 51 Sell Client Payment to client 
associated with 
surrendering partial 
value of the contract. 
148 Partial 
Surrender 
Reversal 2 63    Reversal of a 
Payment to client 
associated with 
surrendering partial 
value of the contract. 

---

## Page 58

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 58 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
250 Return of 
Excess 
Contributions 
  2 24 Sell Client Return of 
[[Premium]]/deposit to 
the policy owner.  
Some possible 
situations 
include a) to maintain 
the policy status as a 
life insurance contract 
(non-MEC), b) 
violation of Guideline 
[[Premium]]/TEFRA 
limits, c) violation of 
product limits, d) 
account value forced  
307 Return of 
Excess 
Contributions 
Reversal 2 63    Reversal of 
[[Premium]]/deposit to 
the policy owner.  
Some possible 
situations include a) 
to maintain the policy 
status as a life 
insurance contract 
(non-MEC), b) 
violation of Guideline 
[[Premium]]/TEFRA 
limits, c) violation of 
product limits, d) 
account value forced 
99 Substantial 
Equal 
Payments 
  2 53 Sell Client Payment to client 
associated a 
scheduled series of 
substantially equal 
payments for the life 
expectancy of the 
[[participant]], which 
must continue for a 
minimum of 5 years or 
until age 59 1/2, 
whichever is longer.  
193 Substantial 
Equal Payment 
Reversal 2 63    Reversal of a 
payment to client 
associated a 
scheduled series of 
substantially equal 
payments for the life 
expectancy of the 
[[participant]], which 
must continue for a 
minimum of 5 years or 
until age 59 1/2, 
whichever is longer.  

---

## Page 59

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 59 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
50 Systematic 
Withdrawal 
  2 53 Sell Client Client-initiated 
withdrawal of a 
percentage or a level 
dollar amount from 
the contract on a 
monthly, quarterly, 
semiannual, or annual 
basis.  
192 Systematic 
Withdrawal 
Reversal 2 63    Reversal of a client-
initiated withdrawal of 
a percentage or a 
level dollar amount 
from the contract on a 
monthly, quarterly, 
semiannual, or annual 
basis.  
400 Automatic Loan 
Repayment 
  2 04 Buy Client Systematic repayment 
of an outstanding 
loan. 
401 Automatic Loan 
Repayment 
Reversal 2 63    Reversal of 400 
410 Loan [[default]]   Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
A loan is defaulted 
when the repayment 
is not received within 
the specified/agreed 
upon date. The loan 
[[default]] transaction 
may also produce a 
1099R that is issued 
to the [[participant]] who 
defaulted.  
411 Loan [[default]] Reversal Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Reversal of 411 
transaction. 
432 Periodic 
Annuitization 
Payment 
  2 53 Sell Client Actual payout of 
annuitized contract 
234 Periodic 
Annuitization 
Payment 
Reversal 2 63    Reversal of actual 
payout of annuitized 
contract 
17 [[Asset]] Allocation   2 53 Buy/Sell Carrier Used for automatic 
(program-controlled) 
scheduled fund 
transfer. 
117 [[Asset]] Allocation Reversal 2 63    Reversal of automatic 
(program-controlled) 
scheduled fund 
transfer. 

---

## Page 60

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 60 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
18 [[Asset]] 
Rebalancing 
  1 23 Buy/Sell Client Client specifies a % 
allocation to maintain 
on the policy. The 
account is 
automatically 
rebalanced on a 
periodic basis 
(defined by the policy 
owner) through an 
internally generated 
transaction. 
118 [[Asset]] 
Rebalancing 
Reversal 2 63    Reversal of client 
specifies a % 
allocation to maintain 
on the policy. The 
account is 
automatically 
rebalanced on a 
periodic basis 
(defined by the policy 
owner) through an 
internally generated 
transaction. 
22 Dollar Cost 
Average 
  2 53 Buy/Sell Client An automated 
process, initiated 
request by the policy 
owner, to transfer out 
$ or % to be 
redistributed to other 
funds. 
122 Dollar Cost 
Average 
Reversal 2 63    Reversal of an 
automated process, 
initiated request by 
the policy owner, that 
transferred out $ or % 
to be redistributed to 
other funds. 
34 Fund Transfer   1 08,09 Buy/Sell Client Transfer of funds, not 
part of an automated 
fund transfer program, 
from 1 or more 
underlying funds to 
other underlying 
funds. 
134 Fund Transfer Reversal 2 63    Reversal of a transfer 
of funds, not part of 
an automated fund 
transfer program, 
from 1 or more 
underlying funds to 
other underlying 
funds. 

---

## Page 61

Standardized Data Reporting Best Practices 
 
 
 
Appendix A 61 
 
 
 
Code 
# 
Code Name SDR 
Transaction 
Category 
SDR 
Transaction 
Code 
SDR 
Transaction      
Type 
SDR              
Source 
Definition  
35 Future Transfer   Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Reports that a 1035 
Exchange has been 
received but not 
funded. 
135 Future Transfer Reversal Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Reversal of 35. 
 XO Group 
Rebalance 
  1 08,09 Buy/Sell Client Group Rebalances 
are used to represent 
subaccount 
rebalancing 
transactions done on 
a large group of 
contracts specifically 
initiated by 
Investment Advisors 
305 Group 
Rebalance 
Reversal 2 63    Reversal of Group 
Rebalance (XO) 
173 Renewal   Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Renewal transactions 
are used to represent 
renewals of fixed 
buckets within the 
annuity upon maturity 
174 Renewal Reversal Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
No detection of usage 
by life or annuity 
users.   
66 Market Value 
Adjustment 
  Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Market Value 
Adjustment 
transactions are used 
to represent the 
positive or negative 
adjustment when 
money is withdrawn 
or transferred from a 
fixed bucket, and the 
rate has changed 
since the bucket was 
opened. 
166 Market Value 
Adjustment 
Reversal Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Reversal of Market 
Value Adjustment (66) 
420 Payment 
Correction 
  2 07 Buy/Sell Carrier Used for 
miscellaneous 
accounting 
adjustments 
24 Payment 
Correction 
Reversal 2 63    Reversal of 420 
417 Rate Change   Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Means for carrier to 
communicate rate 
change.   
421 Reissue   Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Does Not 
Apply 
Sent for fixed 
contracts that reach 
their duration and the 
contract is renewed 
with a new rate and 
duration 

---

## Page 62

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 