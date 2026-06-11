---
title: "GCF Repo Funds-Only Settlement (FOS) Scenario: Overnight GCF Repo Transaction – Dealer View"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd173_gcf_repo_fos_scenario_for_overnight_gcf_repo-dealer_view_042022.pdf"
pages: 11
size: "975.4 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GCF Repo Funds-Only Settlement (FOS) Scenario: Overnight GCF Repo Transaction – Dealer View

**Original File:** [gsd173_gcf_repo_fos_scenario_for_overnight_gcf_repo-dealer_view_042022.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd173_gcf_repo_fos_scenario_for_overnight_gcf_repo-dealer_view_042022.pdf)  
**Category:** GSD  
**Total Pages:** 11  
**File Size:** 975.4 KB  

---

## Page 1

GCF Repo 
Funds-Only [[settlement]] 
(FOS)
Fixed Income Clearing Corporation
Government [[securities]] Division
Scenario: Overnight GCF Repo Transaction – Dealer View

---

## Page 2

The GCF Repo FOS Scenario for Overnight GCF Repo – Dealer View (hereinafter, the "document") is provided as a convenience to Members and is for 
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
GCF Repo FOS Scenario for Overnight GCF Repo – Dealer View
Disclaimer

---

## Page 3

 GCF Repo Funds-Only [[settlement]] amounts are paid/collected once a day at 10:00 AM.
 GCF Repo Funds-Only [[settlement]] is a daily process that includes the following components for Netting 
Members: the GCF Forward Mark Adjustment Payment/Return, the GCF Interest Adjustment Payment, GCF 
Transaction Adjustment Payment (TAP) and CCIT Daily Repo Interest (as applicable). These components are 
captured on the GCF Funds [[settlement]] Report that is generated to the GCF section of [[FICC]] Report Center.
 The GCF Forward Mark Adjustment Payment/Return is equal to the sum of the GCF Interest Rate Mark and 
Accrued Repo Interest-to-Date. Each day, as part of the GCF Repo FOS process, the GCF Forward Mark is 
passed from one party to another (Cash Lender to Cash [[Borrower]] and vice versa). 
GCF Forward Mark Adjustment Payment = GCF Interest Rate Mark + Accrued Repo Interest-to-Date 
 The calculation of the GCF Interest Rate Mark takes into account the difference between the Contract Repo 
Rate on the trade and the System Repo Rate. If the System Repo Rate is less than the Contract Repo Rate on 
the trade, then the GCF Interest Rate Mark for the cash [[Borrower]] will be negative (resulting in a debit) and for 
the cash lender it will be positive (resulting in a credit). On the other hand, if the System Repo Rate is greater 
than the Contract Repo Rate on the trade then the GCF Interest Rate Mark for the cash [[Borrower]] will be positive 
(resulting in a credit) and for the cash lender it will be negative (resulting in a debit).
GCF Interest Rate Mark = (System Repo Rate – Contract Repo Rate) * Start Money * Remaining days in term / 360
GCF Repo Funds-Only [[settlement]] (FOS) Overview
GCF Repo FOS Scenario for Overnight GCF Repo – Dealer View
3

---

## Page 4

 Accrued Interest on a GCF Repo Transaction is captured by the Accrued Repo Interest-to-Date.
Accrued Repo Interest-to-Date = Contract Repo Rate * Start Money * Number of days between the next business date and the Start Date / 360 
 Each day, GCF Forward Mark is passed from one counterparty to another representing the mark to market 
(MtM) on the GCF Repo Transaction.
 On the following day, the GCF Forward Mark is returned to the counterparty who paid it on the prior business 
day, along with interest on the GCF Forward Mark. This is known as the GCF Interest Adjustment Payment.
GCF Interest Adjustment Payment = GCF Forward Mark * Overnight Investment Rate / 360
 The GCF Transaction Adjustment Payment (TAP) represents the total repo interest accrued on GCF Repo 
Transactions at maturity (on [[settlement]] date) and is collected/paid on the [[settlement]] date of the GCF Repo. 
GCF TAP = Contract Repo Rate * Start Money * Total number of days in term / 360
GCF Repo Funds-Only [[settlement]] (FOS) Overview (Cont.)
GCF Repo FOS Scenario for Overnight GCF Repo – Dealer View
4

---

## Page 5

Transaction Details
Start Money: $500,000,000.00 GCF Repo Generic [[CUSIP]]: FFFIX - 371487AL3
Final Money: $500,001,666.67 Term: Overnight - 1 Day 
Transaction Type: Repo Contract Repo Rate: 0.12%
Trade Date: 09/20/2021 Start Date: 09/20/2021 
End Date: 09/21/2021
Based on this trade data you can expect the following on Day 1:
 Total repo interest is: 0.12% * 500,000,000 * 1 / 360 = $1,666.67 
 The GCF Transaction Adjustment Payment is ($1,666.67). On [[settlement]] Date through FOS, [[FICC]] will collect 
$1,666.67 from cash [[Borrower]] and pay $1,666.67 to cash lender. 
 Principal of $500,000,000.00 is settled via Tri-Party and the total repo interest of $1,666.67 is settled via FOS in 
a 1-day period.
Overnight GCF Repo Transaction Details on Trade Date/Start Date
GCF Repo FOS Scenario for Overnight GCF Repo – Dealer View
5

---

## Page 6

GCF Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
GCF Repo FOS Scenario for Overnight GCF Repo – Dealer View
6
Reverse Side (Cash Lender)
Repo Side (Cash [[Borrower]])

---

## Page 7

 Based on the trade data, the GCF Final [[settlement]] Report generated at end of day provides the 
following:
 The Final Money is $500,001,667.67. 
 Principal of $500,000,000.00 is settled via Tri-Party and the total repo interest of ($1,666.67) is 
settled via FOS.
GCF Final [[settlement]] displays GCF TAP as follows for the Repo Side (Cash [[Borrower]]): 
GCF Repo FOS Scenario for Overnight GCF Repo – Dealer View
7


---

## Page 8

 Based on the trade data, the GCF Final [[settlement]] Report generated at end of day provides the 
following:
 The Final Money is $500,001,667.67. 
 Principal of $500,000,000.00 is settled via Tri-Party and the total repo interest of $1,666.67 is 
settled via FOS.
GCF Final [[settlement]] displays GCF TAP as follows for the Reverse Side (Cash Lender): 
GCF Repo FOS Scenario for Overnight GCF Repo – Dealer View
8


---

## Page 9

Transaction Details
Start Money: $500,000,000.00 GCF Repo Generic [[CUSIP]]: FFFIX - 371487AL3
Final Money: $500,001,666.67 Term: Overnight - 1 Day 
Transaction Type: Repo Contract Repo Rate: 0.12%
Trade Date: 09/20/2021 Start Date: 09/20/2021 
End Date: 09/21/2021
Based on this trade data on Trade Date/Start Date you can expect the following to be calculated and then 
collected/paid through Start of Day FOS on End Date:
 The Total Accrued Repo Interest-to-Date is: 0.12% * 500,000,000 * 1 / 360 = $1,666.67. 
 The Transaction Adjustment Payment is ($1,666.67). 
 For the Cash [[Borrower]] (Repo Side), the Total Start of Day FOS amount paid to [[FICC]] is ($1,666.67).
 For the Cash Lender (Reverse Side), the Total Start of Day FOS amount collected from [[FICC]] is $1,666.67.
 The Principal of $500,000,000.00 is settled via Tri-Party.
Overnight GCF Repo Transaction Details on End Date
GCF Repo FOS Scenario for Overnight GCF Repo – Dealer View
9

---

## Page 10

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center


---

## Page 11

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD173