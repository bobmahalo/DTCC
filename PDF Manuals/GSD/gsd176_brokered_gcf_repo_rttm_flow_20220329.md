---
title: "Brokered GCF Repo RTTM Flow"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd176_brokered_gcf_repo_rttm_flow_20220329.pdf"
pages: 7
size: "299.4 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# Brokered GCF Repo RTTM Flow

**Original File:** [gsd176_brokered_gcf_repo_rttm_flow_20220329.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd176_brokered_gcf_repo_rttm_flow_20220329.pdf)  
**Category:** GSD  
**Total Pages:** 7  
**File Size:** 299.4 KB  

---

## Page 1

Brokered GCF Repo®
RTTM® Flow
Fixed Income Clearing Corporation
Government [[securities]] Division

---

## Page 2

The Brokered GCF Repo® RTTM® Flow  (hereinafter, the "document") is provided as a convenience to Members and is for information purposes only. 
Although [[FICC]] may make this document available to Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have 
a continuing obligation to make available this document or other related information of a certain type. 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose of any inform ation provided to Members in 
this document, w hich is provided as-is. [[FICC]] shall not be liable for any loss related to such information (or the act or process of providing such information) 
resulting directly or indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or wi llful misconduct on the part of 
[[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from interruptions, delays, or defects aris ing from or related to providing this 
guide; and (2) any special, consequential, exemplary, incidental, or punitive damages. 
Further, the information contained in this document is subject to change. Members and other authorized users of the document w ill find the most current 
version of the document on [[DTCC]]’s Learning Center site, w ww.dtcclearning.com. [[FICC]] shall bear no responsibility for any losses a ssociated w ith the 
failure of Members or other authorized users to follow  [[FICC]]’s most current document.
Disclaimer

---

## Page 3

Trade Matching: Locked-in GCF Repo
GCF Counterparty A 
([[FICC]] [[Member]]) 
Cash [[Borrower]]/Repo
GCF Counterparty B 
([[FICC]] [[Member]]) 
Cash Lender/Reverse
2
GCF Counterparty B 
affirms GCF Rev Repo 
GCF Counterparty A 
affirms GCF Repo  
1
[[FICC]] [[GSD]]
Real-Time Trade Matching (RTTM)®
2
1
Note :This trade matching flow  only applies to GCF Repo Transactions that have been successfully validated and processed by the sys tem. This flow  does not 
depict the process for rejected, unaffirmed or uncompared GCF Repo Transaction submissions. Also, note that [[Novation]] of the Lock ed-In trade occurs at the 
time [[FICC]] is in receipt of the trade from the Locked- In Trade Source (i.e., GCF-Authorized IDB).
GCF Counterparty A
Cash [[Borrower]]/Repo
GCF Counterparty B
Cash Lender/Reverse
Trade Affirmation 
reported to 
GCF Counterparty A
Trade Affirmation 
reported to 
GCF Counterparty B
3
GCF-Authorized Inter-Dealer 
[[Broker]] (IDB) as [[intermediary]]
Submission of Locked-In GCF Repo 
Transaction vs. GCF Counterparties A & B
2
GCF-Authorized IDB 
as [[intermediary]]
Trade Affirmation reported to 
GCF-Authorized IDB
Trade Execution Trade Execution
Brokered Locked-In GCF Repo® RTTM® Flow 
3
Repo & Reverse Repos are 
added to RTTM for affirmation3

---

## Page 4

Start Leg Netting and [[settlement]]: Brokered Locked-In GCF Repo 
GCF Shell Fully Collateralized 
on GCF Clearing Agent 
Bank’s Tri-party Platform
GCF Shell Fully Collateralized 
on GCF Clearing Agent Bank’s 
Tri-party Platform
[[collateral]]/Cash Locked up in [[GSD]] 
account on GCF Clearing Agent Bank’s 
Tri-party Platform
3 3
1 1
[[FICC]] [[GSD]] as 
central counterparty 
[[FICC]] [[GSD]] send file transmission of 
Members GCF Net Positions to its GCF 
Clearing Agent Bank’s Tri-party Platform
1
[[FICC]] [[GSD]]
Net Position
 Net Position
Real-Time Trade Matching (RTTM)
GCF Net [[settlement]] Position 
([[collateral]] Allocation Obligation) 
reported to 
GCF Counterparty A 
GCF Net [[settlement]] Position
(Cash Obligation/[[collateral]] 
Allocation [[Entitlement]]) 
reported to 
GCF Counterparty B 
Brokered Locked-In GCF Repo® RTTM® Flow 
4
Netting Engine
GCF Counterparty B 
satisfies Obligation on 
GCF Clearing Agent Bank’s 
Tri-party Platform
2
Note :This Start Leg netting and [[settlement]] flow  assumes that the GCF Counterparties each have only one (1) GCF Net [[settlement]] Posi tion resulting from one 
(1) overnight GCF Repo Transaction in one (1) GCF Generic [[CUSIP]] Number. 
GCF Counterparty A 
satisfies Obligation on 
GCF Clearing Agent Bank’s 
Tri-party Platform
2
[[collateral]]
Cash
Cash
[[collateral]]

---

## Page 5

End Leg Netting and [[settlement]]: Brokered Locked-In GCF Repo 
GCF Shell Unwound on 
GCF Clearing Agent Bank’s 
Tri-party Platform
GCF Shell Unwound on 
GCF Clearing Agent Bank’s 
Tri-party Platform
[[collateral]]/Cash Unwound in [[GSD]] 
account on GCF Clearing Agent Bank’s 
Tri-party Platform
3 3
1 1
[[FICC]] [[GSD]] as 
central counterparty 
[[FICC]] [[GSD]] send file transmission of 
Members GCF Net Positions to its GCF 
Clearing Agent Bank’s Tri-party Platform
1
[[FICC]] [[GSD]]
Net Position
 Net Position
Real-Time Trade Matching (RTTM)
GCF Net [[settlement]] Position 
(Cash Obligation/[[collateral]] 
Allocation [[Entitlement]]) 
reported to 
GCF Counterparty A 
GCF Net [[settlement]] Position
([[collateral]] Allocation Obligation) 
reported to 
GCF Counterparty B 
Brokered Locked-In GCF Repo® RTTM® Flow 
5
Netting Engine
GCF Counterparty B 
satisfies Obligation on 
GCF Clearing Agent Bank’s 
Tri-party Platform
2
Note :This End Leg netting and [[settlement]] flow  assumes that the GCF Counterparties each have only one (1) GCF Net [[settlement]] Positi on resulting from one 
(1) overnight GCF Repo Transaction in one (1) GCF Generic [[CUSIP]] Number from the previous day and the unw ind of the End Leg oc curs on the current day. 
The total repo interest accrued on the GCF Repo Transaction w ill settle via GCF Funds -Only [[settlement]] on the End Leg [[settlement]] Date as a GCF Transaction 
Adjustment Payment (TAP).
GCF Counterparty A 
satisfies Obligation on 
GCF Clearing Agent Bank’s 
Tri-party Platform
2
Cash
[[collateral]]
Cash 
[[collateral]]

---

## Page 6

T o access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
6

---

## Page 7

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Cleari ng Corporation (“[[DTCC]]”). [[DTCC]] itself  
does not provide such services. Each of these affiliates is a separate legal entity, subject to the law s and regulations of the particular country or countries in w hich 
such entity operates. Please see w ww.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD176