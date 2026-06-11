---
title: "Program and Systematic Investment Identifier: Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs301_fs_program_systematic_investment_identifier_20230727.pdf"
pages: 11
size: "271.5 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Program and Systematic Investment Identifier: Best Practices

**Original File:** [mfs301_fs_program_systematic_investment_identifier_20230727.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs301_fs_program_systematic_investment_identifier_20230727.pdf)  
**Category:** Other  
**Total Pages:** 11  
**File Size:** 271.5 KB  

---

## Page 1

 
 
 
Fund/SERV® 
PROGRAM AND SYSTEMATIC INVESTMENT 
IDENTIFIER: BEST PRACTICES 
 
JULY 27, 2023 

---

## Page 2

REVISION HISTORY 
Date  Revisions 
July 27, 2023 Document rebranded.  Content reviewed and refreshed.  Small formatting changes made. 
April 7, 2021 Document rebranded.   
  

---

## Page 3

 
 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 4 
Background and Objectives ................................................................................................................................ 4 
Scope .................................................................................................................................................................. 4 
Program Transaction Indicator ........................................................................................................................... 5 
Program Transaction Indicator (Contributions and Withdrawals)–Firm .............................................................. 5 
Scenario (Contribution) ..................................................................................................................................... 5 
Scenario (Withdrawal) ....................................................................................................................................... 5 
Program Transaction Indicator (Rebalance Transactions)–Firm ........................................................................ 6 
Scenario ............................................................................................................................................................ 6 
[[liquidation]] Indicator in CONJUNCTION with the program transaction indicator (systematic redemption)-
firm ......................................................................................................................................................................... 7 
Scenario ............................................................................................................................................................ 7 
Periodic Frequency Indicator–Firm .................................................................................................................... 8 
Scenario ............................................................................................................................................................ 8 
Program Transaction Indicator, Systematic Transaction Frequency & Periodic Frequency Indicator-Fund
................................................................................................................................................................................ 9 
Program Transaction Indicator (Withdrawals)–Fund .......................................................................................... 9 
Scenario ............................................................................................................................................................ 9 
Systematic Transaction Frequency-Fund ........................................................................................................... 9 
Periodic Frequency Indicator-Fund..................................................................................................................... 9 
Target Date Fund Indicators ............................................................................................................................. 10 
Target Date Fund Indicator–Registration .........................................................................................................10 
Scenario ..........................................................................................................................................................10 
Target Date Fund Indicator–Firm ......................................................................................................................10 
 

---

## Page 4

Program and Systematic Investment Identifier: Best Practices 
Overview 4 
OVERVIEW 
Background and Objectives 
Members of the Investment Company Institute's [[Broker]]/Dealer Advisory Committee recommended changes to 
the Fund/SERV® platform to assist funds to properly identify transactions that have special conditions such as 
being periodic or originating from fee based [[Asset]] allocation programs.  
Based on these recommendations, Fund/SERV® was modified to create a generalized framework to properly 
identify transactions from [[Asset]] allocation rebalance programs (buy, sell, exchange) that is rationally aligned 
with the existing indicators for recurring/periodic purchases in Systematic Investment Plans, Pre-Authorized 
Contribution Plans and Periodic Investment Plans (SIP/PAC/PIP) and systematic withdrawals (SWP). In 
addition, Fund/SERV® was modified to support Target Date Fund processing. 
These indicators allow funds to exempt applicable transactions from the standard business rules for fund 
minimums requirements, minimum contribution/withdrawal thresholds and frequent trading penalties including 
purchase blocks. 
In addition, the SWP (Systematic Withdrawal Plan) Frequency Indicator is Conditionally Required, allowing 
funds to calculate and track Contingent Deferred Sales Charge (CDSC) waivers. Although the indicators are 
pass-through values that will be used in downstream rules-based applications, it should be highlighted that the 
values must be passed back in transaction confirmations. The objective is to ultimately minimize manual 
exception processing and errors. 
 
Scope 
This document provides best practices associated with Fund/SERV® functionality as it relates to Program and 
Systematic Indicators associated with the transactions identified above. 

---

## Page 5

Program and Systematic Investment Identifier: Best Practices 
Program Transaction Indicator 5 
PROGRAM TRANSACTION INDICATOR 
Program Transaction Indicator (Contributions and Withdrawals)–Firm 
When applicable, firms should specifically identify systematic transactions using the Program Transaction 
Indicator for Orders (001), As of Orders (004) and Corrections (003) when the transaction is processed as a 
recurring systematic event on the brokerage system. 
Field Name Description 
Program Transaction Indicator [[default]] = Blank 
1 = Systematic Withdrawal Plan (SWP) 
2 = Target Date Fund [[liquidation]] 
3 = Systematic Contribution (SIP/PAC/PIP) 
4 = Rebalance Purchase (Systematic) 
5 = Rebalance Redemption (Systematic) 
*Conditional rule = If 1, then the Periodic Frequency 
Indicator is Required 
 
Scenario (Contribution) 
Susie Smith's account on ABC firm's brokerage system is coded for a recurring monthly investment of $500.00. 
On the 15th of each month, ABC brokerage identifies the automatic investment and systematically generates a 
purchase order through the [[NSCC]]. On the Fund/SERV
® order, ABC brokerage identifies the transaction as a 
'systematic purchase' using the Program Transaction Indicator of '3'. 
 
Scenario (Withdrawal) 
Susie Smith's account on ABC firm's brokerage system is coded for a recurring monthly distribution of $500.00. 
On the 15th of each month, ABC brokerage identifies the automatic withdrawal instruction and systematically 
generates a [[liquidation]] order through the [[NSCC]]. On the Fund/SERV
® order, ABC brokerage identifies the 
transaction as a 'systematic withdrawal' using the Program Transaction Indicator of '1'. 
Note: 
This Program Transaction Indicator value also requires a Periodic Frequency Indicator. In this case, the Periodic Frequency 
Indicator would be '1' [Monthly]. Additional information is provided on subsequent pages regarding use of the Periodic 
Frequency Indicator.)  
  

---

## Page 6

Program and Systematic Investment Identifier: Best Practices 
Program Transaction Indicator 6 
Program Transaction Indicator (Rebalance Transactions)–Firm 
When applicable, firms should specifically identify rebalance transactions using the Program Transaction 
Indicator for Orders (001), As of Orders (004) and Corrections (003) when the transaction is processed as part 
of an [[Asset]] allocation event on the brokerage system. 
Note 
The use of the indicator does not explicitly indicate whether the transaction is from a discretionary and non-discretionary 
[[Asset]] allocation program from the firm. 
 
Scenario 
Susie Smith's account at ABC brokerage is coded for an annual [[Asset]] reallocation. On March 31, ABC 
brokerage identifies all accounts scheduled for allocation and generates orders through the [[NSCC]]. Purchases 
and redemptions are thus simultaneously generated across client accounts. On the Fund/SERV
® orders, ABC 
brokerage highlights purchase transactions as 'rebalance purchases' using the Program Transaction 
Indicator of '4'; for the [[liquidation]] side of the transactions, the order would specify 'rebalance redemptions' 
using the Program Transaction Indicator of '5'. 

---

## Page 7

Program and Systematic Investment Identifier: Best Practices 
[[liquidation]] Indicator in CONJUNCTION with the program transaction indicator (systematic redemption)-firm 7 
[[liquidation]] INDICATOR IN CONJUNCTION WITH THE 
PROGRAM TRANSACTION INDICATOR (SYSTEMATIC 
REDEMPTION)-FIRM 
When applicable, firms should specifically identify systematic transactions using the Program Transaction 
Indicator for Orders (001), As of Orders (004) and Corrections (003) when the transaction is processed as a 
recurring systematic event on the brokerage system. 
 
Scenario 
Susie Smith's account on ABC brokerage is coded for a monthly withdrawal of $250.00. On the last day of 
each month, ABC brokerage identifies all accounts scheduled for recurring withdrawals and generates 
[[liquidation]] orders through [[NSCC]]. On the Fund/SERV® order, ABC brokerage identifies the transaction as a 
'systematic withdrawal' using the Program Transaction Indicator of '1'. 
Furthermore Susie Smith owns B [[shares]] and is not fully vested. In order to prevent back -end sales charges on 
her recurring withdrawals, ABC brokerage must ask the fund to waive the CDSC fee using the [[liquidation]] 
Indicator; [[Option]] '8' for Systematic Withdrawal. 
 
 

---

## Page 8

Program and Systematic Investment Identifier: Best Practices 
Periodic Frequency Indicator–Firm 8 
PERIODIC FREQUENCY INDICATOR–FIRM 
The firm must provide the systematic transaction frequency when the Program Transaction Indicator flag is 
coded to '1' for a systematic withdrawal or the [[liquidation]] Indicator is coded as an '8' for Systematic 
Withdrawal. This frequency allows the fund to calculate the eligible waiver percentages.  
 
Scenario 
Susie Smith's account on ABC brokerage is coded for a monthly withdrawal of $250.00. On the last day of 
each month, ABC brokerage identifies all accounts scheduled for recurring withdrawals and generates 
[[liquidation]] orders through [[NSCC]]. On the Fund/SERV
® order, ABC brokerage identifies the transaction as a 
'systematic withdrawal' using the Program Transaction Indicator of '1'. 
ABC brokerage also identifies the systematic withdrawal frequency as '1' for monthly using the Periodic 
Frequency Indicator on the Fund/SERV® order. 

---

## Page 9

Program and Systematic Investment Identifier: Best Practices 
Program Transaction Indicator, Systematic Transaction Frequency & Periodic Frequency Indicator-Fund 9 
PROGRAM TRANSACTION INDICATOR, SYSTEMATIC 
TRANSACTION FREQUENCY & PERIODIC FREQUENCY 
INDICATOR-FUND 
Program Transaction Indicator (Withdrawals)–Fund 
When firms populate the program indicator as a withdrawal, funds should capture that information to consider 
for fee waivers and fund policy exemptions. This is supplied when the transaction is processed as a systematic 
withdrawal on the brokerage system but not on the fund's transfer agency platform.  
 
Scenario 
Susie Smith's account on ABC brokerage is coded for a monthly withdrawal of $250.00. On the last d ay of 
each month, ABC brokerage identifies all accounts scheduled for recurring withdrawals and generates 
[[liquidation]] orders through [[NSCC]]. On the Fund/SERV
® order, ABC brokerage identifies the transaction as a 
'systematic withdrawal' using the Program Transaction Indicator of '1'. 
 
Systematic Transaction Frequency-Fund 
As a best practice, the firm must provide the systematic transaction frequency when the systematic transaction 
flag is coded to (1) = Yes. Once provided, specifically on liquidations, the fund can utilize the frequency to 
calculate percentages for CDSC waiver eligibility. 
 
Periodic Frequency Indicator-Fund 
As a best practice, funds should utilize the systematic indicators and apply to fund rules/edits.  
 

---

## Page 10

Program and Systematic Investment Identifier: Best Practices 
Target Date Fund Indicators 10 
TARGET DATE FUND INDICATORS 
Target Date Fund Indicator–Registration 
The purpose of the "Target Date Fund Indicator" field located on the Full Registration Record (Fund/SERV® 
401) is to indicate the responsibility for the origination of activity for Target Date Funds. Firms will use the field 
to indicate whether or not the fund has the responsibility to originate/calculate activity for Target Date Funds on 
their [[transfer agent]] System. The fund will use this field to set an indicator on the sub- account on their Transfer 
Agent System as a "yes or no". This will determine if the fund will (yes response on record) or will not (no 
response on record) generate/calculate Target Date Activity using the payment strategy/rate determined by the 
fund. 
Functionally, the Target Date Fund Indicator is similar to the existing optional SWP indicator in the 401 record.  
Field Name Description 
Target Date Fund Indicator 0 = No 
1 = Yes 
 
From a business perspective, it is important to comprehend whether it is firm or fund responsibility to originate 
the trading instructions. 
 
Scenario 
When initially opening an account with $10,000, Susie Smith instructs the ABC brokerage firm to enroll the 
position in the target payment strategy administered by the fund. The brokerage firm conveys this instruction to 
the fund on the Fund/SERV
® 401 full registration record. On the last day of each month, XYZ Fund generates 
the [[liquidation]], if necessary, to meet the target payment, which will be reported through the [[NSCC]] activity file.  
Note 
If a "yes" value is entered in this field the firm will NOT populate the Program Transaction Indicator on the Order record. 
Additionally, since it is an opening purchase, it would not make sense to use the Program Transaction indicator. 
 
Target Date Fund Indicator–Firm 
The use of the "Program Transaction Indicator" field on the Fund/SERV® Order Record will be used to 
indicate that the firm is accepting the responsibility to generate trading instructions. In relation to the value of 
"2” = Target Date Fund [[liquidation]]" the firm will have the ability to indicate that the purpose/intent of the 
order/redemption is part of a payment strategy, within a target date fund, which is a capital change designed to 
[[Liquidate]] an investors investment over time. When the target date indication value is indicated on an order, the 
fund will return this value on the transaction confirmation. 
Note 
The Full Registration Record (Fund/SERV® 401) would have a null value on the "Target Date Fund Indicator" Field since 
the fund does not have transactional responsibilities. 
 

---

## Page 11

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: July 27, 2023 
Publication Code: MFS301 
Service: FUND/SERV® 
Title: Program and Systematic Investment Identifier: Best Practices 
For More Information 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com  