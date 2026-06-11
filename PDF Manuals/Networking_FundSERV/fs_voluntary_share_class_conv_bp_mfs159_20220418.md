---
title: "VOLUNTARY SHARE CLASS CONVERSIONS: BEST PRACTICES"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_voluntary_share_class_conv_bp_mfs159_20220418.pdf"
pages: 10
size: "239.4 KB"
category: "Networking_FundSERV"
ingested_on: "2026-06-05"
---

# VOLUNTARY SHARE CLASS CONVERSIONS: BEST PRACTICES

**Original File:** [fs_voluntary_share_class_conv_bp_mfs159_20220418.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/fs_voluntary_share_class_conv_bp_mfs159_20220418.pdf)  
**Category:** Networking_FundSERV  
**Total Pages:** 10  
**File Size:** 239.4 KB  

---

## Page 1

 
 
FUND/SERV® / NETWORKING 
VOLUNTARY SHARE CLASS CONVERSIONS: BEST PRACTICES 
 
APRIL 18, 2022 
 
 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
 
 
 
Doc Info: April 18, 2022  
Publication Code: MFS159 
Service: Fund/SERV®, Networking 
Title: Voluntary Share Class Conversions: Best Practices 
 
 
  

---

## Page 3

 
 
 
CHANGE HISTORY 
Dates Changes 
04/18/2022 Learning upgrade caused some link(s) to break.  Links have been corrected. 
 
  

---

## Page 4

 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 5 
Background and Objectives ................................................................................................................................ 5 
Scope .................................................................................................................................................................. 5 
Record Layouts ................................................................................................................................................... 6 
Processing ............................................................................................................................................................ 7 
Best Practices ....................................................................................................................................................... 8 
 

---

## Page 5

Voluntary Share Class Conversions: Best Practices 
Introduction 5 
INTRODUCTION 
Background and Objectives 
This guide and list of Best Practices was prepared by industry participants of the ICI [[Broker]] Dealer Advisory 
Committee (BDAC). Their focus was to identify opportunities for operational efficiencies and reduce the 
number of manual transactions for voluntary share class conversions. 
Voluntary share class conversions (sometimes referred to as “inter-class exchanges” or “cross class 
exchanges”) were traditionally processed manually between some intermediaries and Funds. Certain 
intermediaries processed these voluntary share class conversions as a buy and a sell, which created 
[[settlement]] issues whenever one side of the transaction pended or rejected. Share class conversions may be 
one-off transactions for a specific account, or they may occur as block transactions where an entire book of 
business is converted from one class of the same Fund portfolio to another. Generally, they occur when a 
client is moving from a commission-based account to a fee-based account or when a program at an 
[[intermediary]] is moving all accounts in a Fund to another eligible share class (A share class to Institutional 
share class or an [[intermediary]]-administered C Share conversion
1, for example). In the traditional process, 
intermediaries typically either provided a letter or a spreadsheet to affect the voluntary class conversion outside 
of [[NSCC]] or utilized [[NSCC]]’s Fund/SERV® processing in the form of two separate trades. 
Processing these transactions outside of Fund/SERV® creates manual work at both the Funds and 
intermediaries, and thereby exposes both parties to risk and other considerations.  These risks include missed 
accounts/transactions as well as incorrect client positions and [[settlement]] discrepancies.  
 
Scope 
Fund/SERV® Exchange Order (015) Record and Networking Activity Record (F55) were enhanced to 
accommodate Exchange transaction types designated as a Voluntary Cross Class Exchange within the same 
Fund portfolio: 
Fund/SERV® Exchange Order (015) Record – enhanced to include new transaction types:  
• C (Voluntary Cross Class exchange to new account), and  
• D (Voluntary Cross Class exchange to existing account). 
 
Networking Activity F55 Record: enhanced to include a new transaction type 35 (Direct Voluntary Cross Class 
Exchange) vs. the existing transaction type value of 22 (Share Class Exchange) which is considered non-
reportable. The new Voluntary Share Cross Class Exchange transaction types indicate to the intermediar y that 
tax reportability is based on the Fund’s rules and intermediaries should determine whether a transaction is tax 
reportable or non-tax reportable. 
 
1 See C-Share (Level Load) Conversion:  Operational Considerations (login to ICI required). 

---

## Page 6

Voluntary Share Class Conversions: Best Practices 
Introduction 6 
The guidelines encompassed in this document provide “best practices” for the use of the Fund/SERV 015 
Exchange Order Record and Networking Activity Record (F55) when processing a Voluntary Share Class 
Conversion either through Fund/SERV® or manually at the [[transfer agent]] (TA).  
Record Layouts 
Record Layouts referred to in this document can be found in the Record Layouts section of the learning center 
at https://dtcclearning.com/products-and-services/mutual-fund-services/record-layouts.html 

---

## Page 7

Voluntary Share Class Conversions: Best Practices 
Processing 7 
PROCESSING 
The practice traditionally used by most intermediaries to submit transactions to move [[shares]] in a client account 
from one share class to another involves manual processes and coordination with Fund families and transfer 
agencies. In many cases, Fund families have restrictions established on their TA system that prevent 
shareholders from exchanging across share classes. 
These restrictions and edits are the result of the need to verify eligibility for a specific share class. Once 
verified, the transaction is completed in one of two methods: 
1. An exchange is processed manually at the Fund’s TA based upon coordination with the [[intermediary]].  
2. A sell order of the “from” Security Issue [[ID]] and an off-setting buy of the “to” Security Issue [[ID]] is submitted 
through Fund/SERV®. 
 
Both of these methods present challenges and risks to both the Fund and the [[intermediary]] . 
In the first instance, the Fund must have resources to lift the edits on the TA system and process the exchange 
– either manually or via a systemic process of creating transactions from a spreadsheet provided by the 
[[intermediary]].  The [[intermediary]] must in many cases intervene manually to reconcile and post the transactions 
to the client account on their books, manually adjusting cost basis, and coding the transaction to be bypassed 
from tax-reporting when the Fund indicates that the transaction is non-reportable. 
In the second instance, sending the transactions as sells and buys creates issues for both parties as well. For 
the [[intermediary]], again tax-reporting and cost basis must be manually addressed. However, the risk of the 
transaction creating financial exposure for the [[intermediary]] is greater if for any reason the sell side of the 
transaction rejects or has a [[settlement]] delay. The [[intermediary]] must cover the buy side transaction until 
[[settlement]] is received. Some Funds have different [[settlement]] cycles by share class where a sell of an A Share 
might settle T+2 as a [[default]] cycle and an Institutional class might [[default]] to settling T+1. For the Fund, treating 
these transactions as sells and buys may have an impact on its sales reporting and potentially its salesperson 
compensation. 

---

## Page 8

Voluntary Share Class Conversions: Best Practices 
Best Practices 8 
BEST PRACTICES 
1. A voluntary share class conversion is defined as a transaction in which the shareholder or their 
[[intermediary]] elects to change the share class of a fund portfolio. It is not a fund- originated transaction, 
such as a B to A roll. 
 
Prior to submitting/receiving a Voluntary Cross Class Exchange: 
 
2. Fund Family Transfer Agents should open exchange rules to permit transactions using the Fund/SERV 
transaction types (C = Voluntary Cross Class exchange to new account, or D = Voluntary Cross Class 
exchange to existing account) to be processed on an on-going basis rather than as needed. 
 
• Voluntary share class conversions should be communicated between the Fund and [[intermediary]] and 
assessed for impacts, including conversion policies/requirements such as CDSC liability expectations 
and large trade thresholding restrictions, to mitigate risk of rejected transactions.  
 
• With respect to fund policies, intermediaries should understand that CDSC’s, fund minimums, and 
share class eligibility rules may apply and can be found in the Mutual Fund Profile Service II - Security 
Database, prospectus or other fund documents. 
 
Submitting a Voluntary Cross Class Exchange via Fund/SERV: 
 
3. V oluntary share class conversions should be submitted to a Fund’s [[transfer agent]] by intermediaries 
utilizing the Fund/SERV 015 Exchange Order Record and leveraging transaction types: C (Voluntary 
Cross Class exchange to new account), or D (Voluntary Cross Class exchange to existing account) .  
These transaction types will allow for proper characterization and attribution at Funds with respect to tax 
treatment, sales reporting and attribution, and alignment of [[settlement]] cycles. 
 
• Intermediaries should code for transaction types ‘C’ and ‘D’ on the Fund/SERV 015 record, 
regardless of the omnibus and networking level. If intermediaries [[DO]] not code for the 015 record, then 
they should make best efforts to pre-notify Fund families in advance of submitting transactions that 
move the shareholder from one share class of a fund portfolio to another share class of the same 
portfolio so that Funds can identify these transactions in their normal activity files. 
 
• In lieu of using the Fund/SERV 015 record, if intermediaries opt to continue to send these voluntary 
share class conversions via DCC&S, they should ensure these trades are coded with an [[Asset]] Type 
Indicator of “G” (Share Class Conversion) to minimize the potential sales reporting and [[settlement]] 
issues at the Fund that can be associated with these transactions. 
 
Communicating a Voluntary Cross Class Exchange via Networking:  
 
4. For voluntary share class conversions that cannot be processed by submitting the applicable Fund/SERV 
transaction, Funds and their Transfer Agents may process them outside of Fund/SERV and communicate 
the transaction to intermediaries through the Networking Activity F55 record utilizing transaction type 35 

---

## Page 9

Voluntary Share Class Conversions: Best Practices 
Best Practices 9 
(Direct Voluntary Cross Class Exchange), rather than transaction type 22 (Share Class Exchange).  Funds 
and their Transfer Agents should review the current cross-reference of Networking transaction types to 
their [[transfer agent]] transaction coding to ensure appropriate mapping based upon the transaction.  
 
 
Important Note: 
 
Omnibus Firms should provide applicable detail and valid transaction codes in their Activity transparency files for Fund 
families to identify voluntary share class conversion transactions at the sub-account level, regardless of how they are 
processed at the Fund’s [[transfer agent]]. 
 
 
 

---

## Page 10

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 