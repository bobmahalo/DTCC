---
title: "GSD GCF Repo FOS Scenario: Overnight CCIT™ Transaction "
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd193_gcf_repo_fos_scenario_overnight_ccit_trans_20220513.pdf"
pages: 11
size: "537.7 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD GCF Repo FOS Scenario: Overnight CCIT™ Transaction 

**Original File:** [gsd193_gcf_repo_fos_scenario_overnight_ccit_trans_20220513.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd193_gcf_repo_fos_scenario_overnight_ccit_trans_20220513.pdf)  
**Category:** GSD  
**Total Pages:** 11  
**File Size:** 537.7 KB  

---

## Page 1

GCF Repo 
Funds-Only [[settlement]] 
(FOS) 
Fixed Income Clearing Corporation
Government [[securities]] Division
Scenario: Overnight CCIT™ Transaction 

---

## Page 2

The GCF Repo FOS Scenario for Overnight CCIT™ Transaction (hereinafter, the "document") is provided as a convenience to Members and is for 
information purposes only. Although [[FICC]] may make this document available to Members, it shall be under no obligation to [[DO]] so, nor having once or more 
done so, shall [[FICC]] have a continuing obligation to make available this document or other related information of a certain type.
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose of any information provided to Members in 
this document, which is provided as-is. [[FICC]] shall not be liable for any loss related to such information (or the act or process of providing such information) 
resulting directly or indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful misconduct on the part of 
[[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from interruptions, delays, or defects arising from or related to providing this 
guide; and (2) any special, consequential, exemplary, incidental, or punitive damages. 
Further, the information contained in this document is subject to change. Members and other authorized users of the document will find the most current 
version of the document on [[DTCC]]’s Learning Center site, www.dtcclearning.com. [[FICC]] shall bear no responsibility for any losses associated with the 
failure of Members or other authorized users to follow [[FICC]]’s most current document.
Disclaimer
GCF Repo FOS Scenario for Overnight CCIT™ Transaction 

---

## Page 3

 GCF Repo Funds-Only [[settlement]] amounts are paid/collected once a day at 10:00 AM.
 For CCIT Members’ CCIT Activity, GCF Repo Funds-Only [[settlement]] is a daily process that includes the 
calculation of Accrued Interest which is captured as the CCIT Daily Repo Interest component.  
 For Netting Members’ CCIT Activity, GCF Repo Funds-Only [[settlement]] is a daily process that includes the 
calculations of the following components: CCIT Daily Repo Interest or GCF Transaction Adjustment Payment 
(TAP), GCF Forward Mark Adjustment Payment/Return, and the GCF Interest Adjustment Payment. 
 These components are captured on the GCF Funds [[settlement]] Report that is generated to the GCF section of 
[[FICC]] Report Center.
*
 For an overnight CCIT Transaction, the GCF Repo Funds-Only [[settlement]] process consists of the passing of 
Accrued Interest from the Netting [[Member]] (cash [[Borrower]]) to the CCIT [[Member]] (cash lender). On [[settlement]] 
date, the total repo interest is calculated and collected through the GCF Transaction Adjustment Payment (TAP) 
component for the Netting [[Member]] and is calculated and paid through the CCIT Daily Repo Interest component 
for the CCIT [[Member]]. 
 Accrued Interest on a CCIT Transaction is captured as the Accrued Repo Interest-to-Date and is calculated as: 
Accrued Repo Interest-to-Date = Contract Repo Rate * Start Money * Number of days between the next business date and the Start Date / 360 
*For additional clarification, please note that the Invoice Amount and the Miscellaneous Adjustment Amount is not reported on the GCF Funds [[settlement]] 
Report but may be applicable to Members of the CCIT Service or GCF Repo Service and is reported on the Start of Day Funds [[settlement]] Statement that 
is generated nightly and posted to the Funds-Only [[settlement]] Folder within [[FICC]] Repot Center. 
GCF Repo Funds-Only [[settlement]] (FOS) Overview for CCIT
GCF Repo FOS Scenario for Overnight CCIT™ Transaction 
3

---

## Page 4

Transaction Details 
Start Money: $500,000,000.00 GCF Repo Generic [[CUSIP]]: FFFIX - 371487AL3
Final Money: $500,001,666.67 Term: Overnight - 1 Day
Contract Repo Rate: 0.12% Trade Date: 07/20/2021
Start Date: 07/20/2021 End Date: 07/21/2021
Based on this trade data you can expect the following on Day 1:
 The total repo interest is: 0.12% * 500,000,000 * 1 / 360 = $1,666.67.
 The principal of $500,000,000.00 is settled via Tri-Party and the Total Repo Interest of $1,666.67 is settled via 
FOS at 10:00 AM the next morning.
 On [[settlement]] Date through FOS, [[FICC]] will collect ($1,666.67) GCF Transaction Adjustment Payment from the 
Netting [[Member]] (cash [[Borrower]]) and pay $1,666.67 CCIT Daily Repo Interest to the CCIT [[Member]] (cash 
lender). 
Overnight CCIT Transaction Details on Trade Date/Start Date
GCF Repo FOS Scenario for Overnight CCIT™ Transaction 
4

---

## Page 5

GCF Funds [[settlement]] Report displays the funds [[settlement]] components as follows:
GCF Repo FOS Scenario for Overnight CCIT™ Transaction 
5
Repo Side (Netting [[Member]] View)
Reverse Side (CCIT [[Member]] View)


---

## Page 6

CCIT Trade Report displays the trade details as follows:
GCF Repo FOS Scenario for Overnight CCIT™ Transaction 
6
Repo Side (Netting [[Member]] View)
Reverse Side (CCIT [[Member]] View)


---

## Page 7

 Based on the trade data, the GCF Final [[settlement]] Report generated at end of day provides the 
following:
 The Final Money is $500,001,667.67. 
 Principal of $500,000,000.00 is settled via Tri-Party and total repo interest of ($1,666.67) is 
settled via FOS.
GCF Final [[settlement]] Report displays the trade details as follows for the Repo Side:
GCF Repo FOS Scenario for Overnight CCIT™ Transaction 
7


---

## Page 8

 Based on the trade data, the GCF Final [[settlement]] Report generated at end of day provides the 
following:
 The Final Money is $500,001,667.67. 
 Principal of $500,000,000.00 is settled via Tri-Party and total repo interest of $1,666.67 is 
settled via FOS.
GCF Final [[settlement]] Report displays the trade details as follows for the Reverse Side:
GCF Repo FOS Scenario for Overnight CCIT™ Transaction 
8


---

## Page 9

Transaction Details 
Start Money: $500,000,000.00 GCF Repo Generic [[CUSIP]]: FFFIX - 371487AL3
Final Money: $500,001,666.67 Term: Overnight - 1 Day
Contract Repo Rate: 0.12% Trade Date: 07/20/2021
Start Date: 07/20/2021 End Date: 07/21/2021
Based on this trade data on Trade Date/Start Date you can expect the following to be calculated and then 
collected/paid through Start of Day FOS on End Date:
 The Accrued Repo Interest-to-Date is: 0.12% * $500,000,000 *1 / 360 = $1,666.67.
 The Transaction Adjustment Payment is ($1,666.67).
 The CCIT Daily Repo Interest is $1,666.67.
 For the CCIT [[Member]] (Cash Lender), the Total Start of Day FOS amount is $1,666.67.
 For the Netting [[Member]] (Cash [[Borrower]]), the Total Start of Day FOS amount is ($1,666.67).
 The Principal of $500,000,000.00 is settled via Tri-Party.
Overnight CCIT Transaction Details on End Date
GCF Repo FOS Scenario for Overnight CCIT™ Transaction 
9

---

## Page 10

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
10

---

## Page 11

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD193