---
title: "Fund/SERV - Fund Initiated Liquidations: Best Practices"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs303_fund_initiated_liquidations_bp_20230727.pdf"
pages: 9
size: "277.4 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Fund/SERV - Fund Initiated Liquidations: Best Practices

**Original File:** [mfs303_fund_initiated_liquidations_bp_20230727.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfs303_fund_initiated_liquidations_bp_20230727.pdf)  
**Category:** Other  
**Total Pages:** 9  
**File Size:** 277.4 KB  

---

## Page 1

 
 
Networking 
FUND INITIATED LIQUIDATIONS: BEST PRACTICES 
JULY 27, 2023 
 

---

## Page 2

 
 
REVISION HISTORY 
Date Changes 
July 27, 2023 Document rebranded. Content reviewed and refreshed. Duplicate clause removed. 
July 20, 2022 Learning upgrade caused some links to break.  These are now corrected. 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
Pre-Process Scrubbing ........................................................................................................................................ 5 
Processing ............................................................................................................................................................ 6 
File Indicators ...................................................................................................................................................... 6 
Reporting Responsibilities .................................................................................................................................. 8 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 4

Fund Initiated Liquidations: Best Practices 
Introduction 4 
INTRODUCTION 
In 2009 Members of the Investment Company Institute's [[Broker]]/Dealer Advisory Committee recognized the 
need and then initiated the addition of Networking Activity indicators in order to capture Fund initiated 
transactions. The indicators identify Fund Activity for Fund Closings, Fund Initiated Small Balance Liquidations 
and Target Payment Plans. 
These transaction types create a [[settlement]] via the Networking [[settlement]] File for [[Broker]] -controlled accounts, 
allowing Firms to systematically process the transactions and corresponding payments.  
The functionality associated with these indicators identifies and settles Fund generated liquidations for Fund 
Closings, Small balance Liquidations and Target Payment Plans. 
Note 
The Related Activity Reporting Records Layouts (F55) #1 are available on Learning https://dtcclearning.com/products-and-
services/mutual-fund-services/networking.html  
 

---

## Page 5

Fund Initiated Liquidations: Best Practices 
Pre-Process Scrubbing 5 
PRE-PROCESS SCRUBBING 
The practice used by "most" Funds in a Fund Closing or Small Balance [[liquidation]] is to communicate to all 
Firms impacted, via telephone or e-mail. For some Small Balance Liquidations, Funds provide Firms 
spreadsheets of accounts for scrubbing/exemption review prior to processing liquidations. 
(Examples of exemptions are IRA vs. Retail or where a Systematic Contribution (SIP/PAC/PIP) is 
established at the Firm. Accounts subject to CDSC fees and how they will be as a result of the Fund 
Originated [[liquidation]] are also identified. Firms note exempted accounts and return file to Fund). 
In some cases, Firms are allotted a certain period of time to place liquidations through [[NSCC]] directly. Once the 
[[liquidation]] period is over, the Funds will [[Liquidate]] all remaining accounts. 
Target Date funds have various methods of distributing Fund initiated payments designed to m eet 
shareholders retirement income needs. These methods range from check, wires, or [[NSCC]] Networking SWP 
[[settlement]]. As with Fund originated distributions for fund closing or small balance redemptions, firms will 
benefit significantly from the automated communication and [[settlement]] process.  

---

## Page 6

Fund Initiated Liquidations: Best Practices 
Processing 6 
PROCESSING 
The Networking Activity Detail file contains transaction types for Fund Closing, Small Balance Liquidations and 
Target Payment Plans. These transaction types in conjunction with the Cash Disbursement Indicator and 
Activity [[settlement]] Type DRD (Direct Redemption) will trigger the Fund liquidations to update the Firm's 
systems. Network Levels 0 and 4 will result in a Fund check to customer. Other levels will settle money through 
the Networking [[settlement]] File. 
File Indicators 
I. F55 Activity Reporting Records Activity Detail-Transaction Type 
• 29 = Fund Closing 
• 30 = Small Balance [[liquidation]] 
• 31 = Target Payment Plans 
Note 
Funds submit direct redemption via an F55 record with the appropriate transaction type (29, 30 or 31 as defined above). 
Cash disbursement indicator will be coded as follows. 
Table 1 Networked Accounts 
Network Level Transaction Type Cash Disbursement Ind. [[settlement]] 
0 29 = Fund Closing 2 = Customer Check 
Trust Ntwk'd 29 6 = Cast to Trust Networking [[settlement]] 
3 29 0 = Cash to Firm Networking [[settlement]] 
4 29 2 = Customer Check Wire 
    
0 30 = Small Balance 2 = Customer Check 
Trust Ntwk'd 30 6 = Cast to Trust Networking [[settlement]] 
3 30 0 = Cash to Firm Networking [[settlement]] 
4 30 2 = Customer Check Wire 
    
0 31 = Target Payment 2 = Customer Check 
Trust Ntwk'd 31 6 = Cast to Trust Networking [[settlement]] 
3 31 0 = Cash to Firm Networking [[settlement]] 
4 31 2 = Customer Check Wire 
 
 

---

## Page 7

Fund Initiated Liquidations: Best Practices 
Processing 7 
 
Table 2 Omnibus Accounts 
Transaction Type Cash Disbursement Ind. [[settlement]] 
29 = Fund Closing 0 = Cash to Firm Networking [[settlement]] 
30 = Small Balance N/A  
31 = Target Payment N/A  
 
Settlements via the Networking [[settlement]] File generate an "N75" transaction. The [[settlement]] Type will 
indicate DRD (Direct Redemption) with a [[settlement]] Indicator of "A" (Activity [[settlement]]).  
Upon receiving the F55 activity record Firms will update their proprietary systems to reflect the activity to the 
shareholder accounts, including payment to client where Cash Disbursement Indicators are "Cash to Firm" and 
"Cash to Trust". Payment to Firm will be made via the Networking [[settlement]] File.  

---

## Page 8

Fund Initiated Liquidations: Best Practices 
Reporting Responsibilities 8 
REPORTING RESPONSIBILITIES 
Confirmation, statement, and tax reporting responsibilities are modified for Fund Initiated Liquidations. Direct 
Liquidations on level 3 accounts due to a Fund Closing, Small Balance [[liquidation]] or Target Payment will be 
the responsibility of the Firm. 
Table 3 Reporting Responsibilities 
Reporting Responsibility Level Three Level Four Trust Networked 
Confirm (Fund/SERV® Trades) Firm Fund Trust Company 
Confirm (Non-Fund/SERV®) Firm Fund Trust Company 
Monthly Statement Firm Fund Trust Company 
Quarterly Statements Firm Fund Trust Company 
Year-End Statement Firm Fund Trust Company 
1099D Firm Fund Trust Company 
1099B (Wire Orders) Firm Firm Trust Company 
1099B (Direct Liquidations) Firm Fund Trust Company 
1099 R/W2P (When Applicable) Custodian/Trustee Custodian/Trustee Trust Company 
5498 (When Applicable) Custodian/Trustee Custodian/Trustee Trust Company 
1042S Firm Fund Trust Company 
Proxies Firm/Fund Fund Trust Company 
Interested Party Mailings Firm Fund Trust Company 

---

## Page 9

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: July 27, 2023 
Publication Code: MFS303 
Service: Networking 
Title: Fund Initiated Liquidations: Best Practices 
For More Information 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
Or visit us on the web at: 
www.dtcclearning.com  