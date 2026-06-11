---
title: "Brokered Demand DVP Repo RTTM Flow"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd170_brokered_demand_dvp_repo_rttm_flow_20220316.pdf"
pages: 9
size: "401.3 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# Brokered Demand DVP Repo RTTM Flow

**Original File:** [gsd170_brokered_demand_dvp_repo_rttm_flow_20220316.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd170_brokered_demand_dvp_repo_rttm_flow_20220316.pdf)  
**Category:** GSD  
**Total Pages:** 9  
**File Size:** 401.3 KB  

---

## Page 1

Brokered Demand DVP 
Repo RTTM® Flow
Fixed Income Clearing Corporation
Government [[securities]] Division

---

## Page 2

The Brokered Demand DVP Repo RTTM® Flow (hereinafter, the "document") is provided as a convenience to Members and is for information purposes 
only. Although [[FICC]] may make this document available to Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] 
have a continuing obligation to make available this document or other related information of a certain type. 
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

Trade Matching: Brokered Demand (Same-Day Settling (SDS)/Forward Starting) DVP Repo
Dealer A ([[FICC]] [[Member]]) 
Cash [[Borrower]]/Repo/[[Seller]]
Dealer B ([[FICC]] [[Member]]) 
Cash Lender/Reverse/[[Buyer]]
2
Dealer B submits 
Rev Repo trade 
Dealer A submits 
Repo trade 
1
[[FICC]] [[GSD]]
Real-Time Trade Matching (RTTM)®
2
3
1
Note: Start Legs for both Same-day starting repos and forward starting repos will settle versus [[FICC]]. Also, note that [[Novation]] of the Demand 
trade occurs at the time [[FICC]] is in receipt of the trade from the Demand Trade Source (i.e., Repo [[Broker]]).
Dealer A
Cash [[Borrower]]/Repo/[[Seller]]
Dealer B
Cash Lender/Reverse/[[Buyer]]
Trade Comparison 
Reported to Dealer A
Trade Comparison 
Reported to Dealer B
3
Repo [[Broker]] as [[intermediary]]
Submission of Demand Brokered 
Repo vs. Dealer A & Dealer B 
2
Repo [[Broker]] as [[intermediary]]
Trade Comparison Reported to 
Repo [[Broker]]
Trade Execution Trade Execution
Brokered Demand DVP Repo RTTM® Flow 
3
Repo & Reverse Repo Trades 
are added to RTTM.

---

## Page 4

When the Repo [[Broker]] opts into the Same-Day Settling Service:
Start Leg [[settlement]]: Brokered Demand Same-Day Settling (SDS) DVP Repo 
2
SDS [[obligations]] are 
reported to Dealer A 
Dealer A communicates 
deliver instructions to their 
Clearing Bank.
SDS [[obligations]] are 
reported to Dealer B 
[[FICC]] [[GSD]] as 
central counterparty 
Dealer B communicates 
receive instructions to their 
Clearing Bank.
[[FICC]] [[GSD]] communicates receive/delivery 
instructions to their Clearing Bank.
Dealer A 
Clearing Bank
Dealer B 
Clearing Bank
[[FICC]] [[GSD]] 
Clearing Bank
[[securities]]
Contract Value
Contract Value
[[securities]]
VS.VS.
3
22
3
Note: Steps 1-3 occur same-day on the day of match. Upon the submission of the Brokered Demand Same-Day Settling (SDS) trades, i.e., 
Same-Day Starting Repo, [[GSD]] will generate same-day settling [[obligations]] to settle the Start Leg. The Start Leg will settle vs. [[FICC]]. The Repo 
[[Broker]] will be out of the [[settlement]] process. 
[[FICC]] [[GSD]]
1
[[obligations]]
 [[obligations]]
Real-Time Trade Matching (RTTM)
1
Brokered Demand DVP Repo RTTM® Flow 
4
[[settlement]] System

---

## Page 5

When the Repo [[Broker]] opts out of the Same-Day Settling Service:
Start Leg [[settlement]]: Brokered Demand Same-Day Settling (SDS) DVP Repo (Cont.)
1
Dealer A 
Dealer A communicates 
deliver instructions to their 
Clearing Bank.
Dealer B 
Dealer B communicates 
receive instructions to their 
Clearing Bank.
Repo [[Broker]] communicates 
receive/delivery instructions to their 
Clearing Bank.
Dealer A 
Clearing Bank
Dealer B 
Clearing Bank
Repo [[Broker]]’s 
Clearing Bank
[[securities]]
Contract Value
Contract Value
[[securities]]
VS.VS.
2
11
2
Note: Steps 1 & 2 occur same-day away from [[FICC]] if the Repo [[Broker]] elects not to participate in the Same-Day Settling (SDS) Service. The 
Same-Day Settling service is optional for the Repo Brokers, but mandatory for all other “Dealer” Netting Members (excluding “done-with” 
omnibus accounts). However, for Dealer Netting Members who have executed SDS Trades through a Repo [[Broker]] who has opted out of the 
service, the start leg on such transactions must settle outside of [[GSD]]. 
Repo [[Broker]] as [[intermediary]]
Brokered Demand DVP Repo RTTM® Flow 
5

---

## Page 6

Start Leg Netting and [[settlement]]: Brokered Demand Forward Starting DVP Repo 
Note: Step 1 occurs the night before [[settlement]] date. Step 2 & 3 occur on [[settlement]] date. Also, the Start Leg will settle vs. [[FICC]]. The Repo 
[[Broker]] will be out of the [[settlement]] process. TAP Adjustment is System Value – Contract Value of Start Leg.
2
Dealer A communicates 
deliver instructions to their 
Clearing Bank.
Dealer B communicates 
receive instructions to their 
Clearing Bank.
Dealer A 
Clearing Bank
Dealer B 
Clearing Bank
[[FICC]] [[GSD]] 
Clearing Bank
[[securities]]
System Value
System Value
[[securities]]
VS.VS.
3
2
3
1 1
[[FICC]] [[GSD]] as 
central counterparty 
[[FICC]] [[GSD]] communicates receive/delivery 
instructions to their Clearing Bank.
2
[[FICC]] [[GSD]]
[[obligations]]
 [[obligations]]
Real-Time Trade Matching (RTTM)
Netted [[obligations]] are 
reported to Dealer A 
Netted [[obligations]] are 
reported to Dealer B 
Brokered Demand DVP Repo RTTM® Flow 
6
Netting Engine/[[settlement]] System

---

## Page 7

End Leg Netting and [[settlement]]: Brokered Demand (Same-Day Settling/Forward Starting) 
DVP Repo
System Value
Return of 
[[securities]]
System Value
VS.VS.
Return of 
[[securities]]
Note: Step 1 occurs the night before [[settlement]] date. Step 2 & 3 occur on [[settlement]] date. Also, the End Leg [[settlement]] of an overnight As-of 
Trade eligible to settle through [[GSD]]’s Same-Day Settling Service is not depicted in this flow as the End Leg would not net prior to [[settlement]]. 
TAP Adjustment is System Value – Contract Value of End Leg (Final Money).
2
Dealer A communicates 
receiver instructions to their 
Clearing Bank.
Dealer B communicates 
deliver instructions to their 
Clearing Bank.
Dealer A 
Clearing Bank
Dealer B 
Clearing Bank
[[FICC]] [[GSD]] 
Clearing Bank
3
2
3
1 1
[[FICC]] [[GSD]] as 
central counterparty 
[[FICC]] [[GSD]] communicates receive/delivery 
instructions to their Clearing Bank.
2
[[FICC]] [[GSD]]
[[obligations]]
 [[obligations]]
Real-Time Trade Matching (RTTM)
Netted [[obligations]] are 
reported to Dealer A 
Netted [[obligations]] are 
reported to Dealer B 
Brokered Demand DVP Repo RTTM® Flow 
7
Netting Engine/[[settlement]] System

---

## Page 8

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
8

---

## Page 9

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD170