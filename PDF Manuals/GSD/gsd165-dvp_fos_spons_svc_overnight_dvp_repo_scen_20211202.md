---
title: "DVP FOS - Sponsoring Service - Overnight DVP Repo Scenario"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd165-dvp_fos_spons_svc_overnight_dvp_repo_scen_20211202.pdf"
pages: 19
size: "594.9 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# DVP FOS - Sponsoring Service - Overnight DVP Repo Scenario

**Original File:** [gsd165-dvp_fos_spons_svc_overnight_dvp_repo_scen_20211202.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd165-dvp_fos_spons_svc_overnight_dvp_repo_scen_20211202.pdf)  
**Category:** GSD  
**Total Pages:** 19  
**File Size:** 594.9 KB  

---

## Page 1

DVP 
Funds-Only [[settlement]] 
(FOS) 
Fixed Income Clearing Corporation
Government [[securities]] Division
Sponsoring Service – Overnight DVP Repo Trade Scenario

---

## Page 2

The DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario (hereinafter, the "document") is provided as a convenience to Members and is 
for information purposes only. Although [[FICC]] may make this document available to Members, it shall be under no obligation to [[DO]] so, nor having once or 
more done so, shall [[FICC]] have a continuing obligation to make available this document or other related information of a certain type. 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose of any information provided to Members in 
this document, which is provided as-is. [[FICC]] shall not be liable for any loss related to such information (or the act or process of providing such information) 
resulting directly or indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful misconduct on the part of 
[[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from interruptions, delays, or defects arising from or related to providing this 
guide; and (2) any special, consequential, exemplary, incidental, or punitive damages. 
Further, the information contained in this document is subject to change. Members and other authorized users of the document will find the most current 
version of the document on [[DTCC]]’s Learning Center site, www.dtcclearning.com. [[FICC]] shall bear no responsibility for any losses associated with the 
failure of Members or other authorized users to follow [[FICC]]’s most current document.
Disclaimer

---

## Page 3

This presentation will cover the following topics as they relate to Sponsored DVP 
Overnight Repo Trades:
 DVP Funds Only [[settlement]] (FOS) Overview
 [[FICC]] as CCP on Repos
 Mark to Market and TAP components of FOS
 Repo [[settlement]] and associated cash flows
 Overnight Repo Trading Scenario where Start of Day Funds and Intraday Funds are 
paid/collected
 Examples of Start of Day Funds [[settlement]] Statement
DVP FOS – Sponsoring Service – Overnight DVP Repo Trade Scenario
What You Will Learn

---

## Page 4

 Funds-Only [[settlement]] is a daily cash pass-through process that generates Netting Members 
cash [[obligations]], calculated pursuant to Rule 13 of the [[FICC]] [[GSD]] Rulebook
 Cash [[obligations]] are an aggregate credit or debit Funds-Only [[settlement]] Amount across all 
active netting eligible trades
 Funds-Only [[settlement]] Amounts can either be a funds-only payment (net debit) to [[GSD]] or a 
funds-only payment (net credit) from [[GSD]]
 [[GSD]] assigns each security a System Value to calculate the cash [[settlement]] amount of a given 
net position. The System Value is determined daily to approximate each security’s current 
Market Value (mark to market (MTM)) 
 Funds-Only [[settlement]] Amounts reflect changes in the value of [[securities]] MTM, cash 
adjustments (Clearance Differences) related to the [[settlement]] of [[securities]], pass-through of 
coupon payments for term repos or failed [[obligations]] that cross a coupon date, invoice amounts 
and Miscellaneous Adjustments
 Payment of Funds-Only [[settlement]] Amounts are executed over the Federal Reserve’s National 
[[settlement]] Service with [[DTC]] acting as a [[settlement]] Agent for [[GSD]]
 Netting Members’ Funds-Only Settling Banks will acknowledge and settle their Funds-Only 
[[settlement]] Amounts with [[GSD]] on the Netting Members’ behalf
DVP Funds-Only [[settlement]] (FOS) Overview
DVP FOS – Sponsoring Service – Overnight DVP Repo Trade Scenario
4

---

## Page 5

 Funds-Only [[settlement]] Process occurs twice daily (Start of Day and Intraday): 
 Start of Day cycle:
 Funds-Only Settling Banks must send their acknowledgement or refusal to settle 
on the Netting Members behalf by the Acknowledgement Cutoff Time pursuant to 
[[GSD]] Rules
 [[settlement]] of Start of Day Funds-Only [[settlement]] Amounts occurs by 10:00 AM 
ET* 
 Intraday cycle:
 Funds-Only Settling Banks must send their acknowledgement or refusal to settle 
on the Netting Members behalf by the Acknowledgement Cutoff time pursuant to 
[[GSD]] Rules 
 [[settlement]] of Intraday Funds-Only [[settlement]] occurs by 4:30 PM ET* 
DVP Funds-Only [[settlement]] (FOS) Overview (Cont.)
DVP FOS – Sponsoring Service – Overnight DVP Repo Trade Scenario
5
* Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.

---

## Page 6

 Once a repo trade is matched the trade is novated to [[FICC]] and [[FICC]] becomes a counterparty to 
both parties of the trade
 [[FICC]] risk manages each client’s portfolio
 Part of a risk management practice is a daily mark to market of each repo position
[[FICC]] as Central Counterparty on a Repo trade
DVP FOS – Sponsoring Service – Overnight DVP Repo Trade Scenario
6

---

## Page 7

 In a Repo agreement the Cash [[Borrower]] (Repo client) sells the [[collateral]] [[Asset]] to the Cash 
lender and agrees to repurchase that [[collateral]] [[Asset]] on a [[settlement]] date plus pay Cash lender 
Repo interest for the borrowed cash (assuming repo rate is positive) 
 The repurchase amount plus the Repo interest is the repo Trade Final Money
 The value of the original repo changes as the value of the [[collateral]] [[Asset]] and the market repo 
rates change
 [[FICC]] takes a noon and [[EOD]] snapshot of prices and repo rates and calculates repo trade 
System Final Money
 Mark to Market is a difference between the Trade Final Money and the System Final Money
 Mark to Market is one of the component of Fund Only [[settlement]] (FOS) calculation
 FOS is paid/collected twice a day: at 4:30 PM (based on noon prices) and at 10:00 AM (based 
on [[EOD]] prices)
Overview of Mark to Market on a Repo Trade
DVP FOS – Sponsoring Service – Overnight DVP Repo Trade Scenario
7

---

## Page 8

 The following slides will cover 2 scenarios. First scenario will be for when the overnight sponsored trades are 
submitted and compared after noon, and the second scenario will cover trades submission/comparison before 
noon. In both scenarios it is assumed that the repo rate on the trade is zero.
 Scenario 1: if a trade is compared after noon, then FOS will be calculated once – at the end of the day
 Scenario 2: if a trade is compared before noon, then FOS will be calculated twice, first time at noon and the 
second time at the end of the day. After FOS is calculated at noon it will be paid/collected at 4:30pm the same day 
(shown below as Noon MTM). The following day, this payment gets reversed and the TAP is calculated. 
General Flow of FOS Calculations
DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario
8
FICCParty 1 Party 2
Day 0
Start leg 
[[settlement]]
Day 1
End leg 
[[settlement]]
TAP TAP
Scenario 1
FICCParty 1 Party 2
TAP TAP
Scenario 2
Noon MTM
Noon MTM 
return
Noon MTM 
return
Noon MTM

---

## Page 9

Sponsoring [[Member]] executes an overnight Reverse Repo versus HF Sponsored Members Z, where a Sponsoring 
[[Member]] is reversing in [[securities]] from a HF. In this example, Sponsoring [[Member]] asks HF for 2% [[Haircut]]: 
Sponsoring [[Member]] lends $98 vs. $100 of USTs
Note: [[Haircut]] amounts are a commercial matter between a Sponsoring [[Member]] and their Sponsored [[Member]].
“Done-With” trade execution example – with haircuts
DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario
9
Trade Execution. Monday: 
Sponsoring [[Member]] executes a trade with its Sponsored HF [[Member]]
Sponsoring [[Member]]
HF
Sponsored 
[[Member]] Z

---

## Page 10

Start Leg [[settlement]] of the Sponsored Trades:
The [[settlement]] of a “done-with” Sponsored Trades occurs outside of [[FICC]] directly between a Sponsoring [[Member]] 
and a Sponsored [[Member]].
Step 1a: HF Sponsored [[Member]] Z delivers USTs vs. cash from its [[custody]] Bank E to Sponsoring [[Member]]’s 
Omnibus Account at [[custody]] Bank B
Step 1b: Sponsoring [[Member]] delivers USTs vs. cash from its Omnibus Account to its Principal Account at its 
[[custody]] Bank B
Note: [[FICC]] is not requiring A Sponsoring [[Member]] to establish two separate boxes at the Clearing Bank, one for its 
Sponsoring [[Member]]’s Omnibus Account and another one for its Sponsoring [[Member]]’s Principal Account. [[FICC]] will 
accept the same [[settlement]] instructions for both accounts.
“Done-With” [[settlement]] of Start Leg Example
DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario
10
Monday: Start Leg [[settlement]] of the same day starting repos 
$100 USTs
$98
1a [[custody]] Bank E
HF
Sponsored [[Member]] Z
[[custody]] Bank B
[[custody]] Bank B
Sponsoring [[Member]]’s 
Principal Account
1b
Sponsoring [[Member]] 
Omnibus Account
$100 USTs
$98

---

## Page 11

A. Monday [[EOD]] – Netting process runs. Next day settling [[obligations]] are created and FOS is calculated: 
All [[obligations]] in a given [[CUSIP]] are settled with [[FICC]] at the same price ([[FICC]] [[EOD]] system price). Because of this, 
[[FICC]] calculates TAP to true members up to their expected proceeds. TAP amount is calculated based on the 
difference between [[FICC]] [[EOD]] system price and the [[settlement]] price for a given [[CUSIP]].  
In scenario #1, TAP = System calculated Final Money – Final Money on a Trade = $100 - $98 = $2
B. 10 a.m. FOS Payment. FOS consists entirely of TAP: 
Sponsoring [[Member]] owes $2 FOS to [[FICC]] (which in this example is just TAP), and [[FICC]] owes $2 FOS to Omnibus 
Acct
FOS Calculations – HF example. Scenario 1
DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario
11
FOS [[settlement]] 
Account [[FICC]] FOS [[settlement]] 
Account$2 TAP $2 TAP
After Unwind and all FOS 
payments, Sponsored 
[[Member]]’s Omnibus FOS 
account is long $2
Principal Account Omnibus Account

---

## Page 12

C. End Leg [[settlement]] of the Trade:
 Omnibus cash [[settlement]] account will have a credit of $2 after FOS [[settlement]]
 Omnibus [[securities]] [[settlement]] account will be in a debit position of $2 after an unwind with a HF client
 This example assumed repo interest is zero, but if there was repo interest it would have settled via TAP.
End leg [[settlement]] takes with a Sponsored [[Member]] HF client happens in two steps:
1. UST are delivered from [[FICC]]’s account to Sponsoring [[Member]]’s Omnibus Account.
This [[settlement]] occurs at the [[FICC]]’s System [[EOD]] System Price.
2. UST are onward delivered from Sponsoring [[Member]]’s Omnibus Account to Sponsoring [[Member]]’s HF client.
This [[settlement]] occurs at the trade Final Money.
FOS Calculations – HF example. Scenario 1 (Cont.) 
DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario
12
Sponsoring [[Member]]’s 
[[securities]] [[settlement]] 
Account
[[FICC]]
$100
$100 UST
Omnibus Account
[[securities]] 
[[settlement]]$100 UST
$100
[[Hedge Fund]]
$98 $100 UST
OMNI Acct short $2 
after unwind, which is 
offset by $2 credit in 
TAP 
❶
❷

---

## Page 13

A. Monday Intraday - FOS is calculated: 
At noon, [[FICC]] calculated Forward [[Margin]] (MTM) on all matched trades. In this case, assuming intraday price is $100,  
Forward [[Margin]] = Intraday Price – Trade Price = $100 - $98 = $2
B. Monday 4:30pm FOS Payment. FOS consists of Forward [[Margin]]: 
Sponsor owes $2 FOS to [[FICC]] for Forward [[Margin]] and [[FICC]] owes $2 FOS to Omnibus Acct
C. Monday [[EOD]] - FOS is calculated: 
Monday [[EOD]] FOS consists of 2 components:
1. Return of intraday forward [[Margin]]
2. TAP calculation
FOS = Return of Forward [[Margin]] + TAP = -$2 + $2 = $0
FOS Calculations – HF example. Scenario 2
DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario
13
[[FICC]]$2 Forward [[Margin]] $2 Forward [[Margin]]
FOS [[settlement]] 
Account 
Principal Account
FOS [[settlement]] 
Account
Omnibus Account

---

## Page 14

D. 10 a.m. FOS Payment: 
FOS is $0
E. Unwind of the Trade:
 FOS [[settlement]] Account for the Omnibus account will have a credit of $2 after Monday intraday FOS [[settlement]]
 Omnibus [[securities]] [[settlement]] account will be in a debit position of $2 after an unwind with a HF client
End leg [[settlement]] takes with a Sponsored [[Member]] HF client happens in two steps:
1. UST are delivered from [[FICC]]’s account to Sponsoring [[Member]]’s Omnibus Account.
This [[settlement]] occurs at the [[FICC]]’s System [[EOD]] System Price.
2. UST are onward delivered from Sponsoring [[Member]]’s Omnibus Account to 
Sponsoring [[Member]]’s HF client.
This [[settlement]] occurs at the trade Final Money.
FOS Calculations – HF example. Scenario 2 (Cont.)
DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario
14
Sponsoring [[Member]]’s 
[[securities]] [[settlement]] 
Account
[[FICC]]
$100
$100 UST
Omnibus Account
[[securities]] 
[[settlement]]$100 UST
$100
[[Hedge Fund]]
$98 $100 UST
❶
❷
$0 $0FICC FOS [[settlement]] 
Account
Omnibus Account
FOS [[settlement]] 
Account 
Principal Account

---

## Page 15

Sample of Start of Day FOS Reports

---

## Page 16

Start of Day FOS Report (Omnibus Account)
DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario
16


---

## Page 17

Start of Day FOS Report (Sponsor)
DVP FOS – Sponsored Service – Overnight DVP Repo Trade Scenario
17


---

## Page 18

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
18

---

## Page 19

© 2021 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD165