---
title: "GCF Repo Funds-Only Settlement (FOS) Scenario: Term GCF Repo Transaction – Dealer View"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd215_gcf_repo_fos_scenario_for_term_gcf_repo-dealer_view_20231016.pdf"
pages: 29
size: "2522.9 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GCF Repo Funds-Only Settlement (FOS) Scenario: Term GCF Repo Transaction – Dealer View

**Original File:** [gsd215_gcf_repo_fos_scenario_for_term_gcf_repo-dealer_view_20231016.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd215_gcf_repo_fos_scenario_for_term_gcf_repo-dealer_view_20231016.pdf)  
**Category:** GSD  
**Total Pages:** 29  
**File Size:** 2522.9 KB  

---

## Page 1

GCF Repo
Funds-Only [[settlement]] 
(FOS)
Fixed Income Clearing Corporation
Government [[securities]] Division
Scenario: Term GCF Repo Transaction – Dealer View

---

## Page 2

The GCF Repo FOS Scenario for Term GCF Repo – Dealer View (hereinafter, the "document") is provided as a convenience to Members and is for 
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
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
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
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
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
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
4

---

## Page 5

Transaction Details
Start Money: $1,000,000,000.00 GCF Repo Generic [[CUSIP]]: FFFIX - 371487AL3
Final Money: $1,000,015,000.00 Term: 3 Days 
Transaction Type: Repo Contract Repo Rate: 0.18%
Trade Date: 09/20/2021 Start Date: 09/20/2021
End Date: 09/23/2021
Based on this trade data you can expect the following:
 Total Interest is: 0.18% * 1,000,000,000 * 3 / 360 = $15,000.00 
 Daily Accrued Interest is: 0.18% * 1,000,000,000 * 1 / 360 = $5,000.00 
 Principal of $1,000,000,000.00 is settled via Tri-Party and Total Interest of $15,000.00 is settled via FOS over a 
3-day period.
Term GCF Repo Transaction Details
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
5

---

## Page 6

Transaction Details
Start Money: $1,000,000,000.00 GCF Repo Generic [[CUSIP]]: FFFIX - 371487AL3
Final Money: $1,000,015,000.00 Term: 3 Days 
Transaction Type: Repo Contract Repo Rate: 0.18%
Trade Date: 09/20/2021 Start Date: 09/20/2021
Overnight Investment Rate: N/A End Date: 09/23/2021
Based on this trade data you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 1:
 Accrued Repo Interest-to-Date is: 0.18% * $1,000,000,000 * 1 / 360 = $5,000.00
 The GCF Interest Rate Mark is: (0.18% - 0.18%) * $ 1,000,000,000 * 2 / 360 = $0.00
 The GCF Forward Mark Adjustment Payment is: $5,000.00 + $0.00 = $5,000.00
 For the Cash [[Borrower]] (Repo Side), the Total Start of Day FOS amount paid to [[FICC]] is ($5,000.00)
 For the Cash Lender (Reverse Side), the Total Start of Day FOS amount collected from [[FICC]] is $5,000.00
Term GCF Repo Transaction Details on Day 1
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
6

---

## Page 7

 Based on the trade data, the GCF Finance Report generated on Day 1 will report the following:
 Accrued Repo Interest-to-Date: ($5,000.00) 
 GCF Forward Mark : ($5,000.00) 
GCF Finance Report – Day 1 – Repo Side (Cash [[Borrower]])
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
7


---

## Page 8

 Based on the trade data, the GCF Finance Report generated on Day 1 will report the following:
 Accrued Repo Interest-to-Date: $5,000.00 
 GCF Forward Mark : $5,000.00 
GCF Finance Report – Day 1 – Reverse Side (Cash Lender)
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
8


---

## Page 9

 Based on the trade data, the GCF Forward Mark Report generated on Day 1 will report the following:
 GCF Forward Mark: ($5,000.00)
GCF Forward Mark Report – Day 1 – Repo Side (Cash [[Borrower]])
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
9


---

## Page 10

 Based on the trade data, the GCF Forward Mark Report generated on Day 1 will report the following:
 GCF Forward Mark: $5,000.00
GCF Forward Mark Report – Day 1 – Reverse Side (Cash Lender)
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
10


---

## Page 11

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 1 will report the following:
 GCF Forward Mark Adjustment Payment: ($5,000.00)
 Total Paid/Collected: ($5,000.00) 
GCF Funds [[settlement]] Report – Day 1 – Repo Side (Cash [[Borrower]])
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
11


---

## Page 12

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 1 will report the following:
 GCF Forward Mark Adjustment Payment: $5,000.00
 Total Paid/Collected: $5,000.00 
GCF Funds [[settlement]] Report – Day 1 – Reverse Side (Cash Lender)
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
12


---

## Page 13

Transaction Details
Start Money: $1 billion ($1,000,000,000.00) GCF Repo Generic [[CUSIP]]: FFFIX - 371487AL3
Term: 3 Days (1 day left) Transaction Type: Repo
Contract Repo Rate: 0.18% Trade Date: 09/20/2021
Start Date: 09/20/2021 End Date: 09/23/2021
System Repo Rate: 0.063457% Overnight Investment Rate: 0.10%
Based on this trade data you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 2:
 Accrued Repo Interest-to-Date is: 0.18% * $1,000,000,000 * 2 / 360 = $10,000.00
 The GCF Interest Rate Mark is: (0.063457% - 0.18%) * $ 1,000,000,000 * 1 / 360 = $3,237.31
 The New GCF Forward Mark Adjustment Payment is: $10,000.00 + $3,237.31 = $13,237.31
 The GCF Forward Mark Adjustment Payment Return is ($5,000.00)
 The GCF Interest Adjustment Payment is: $5,000.00 * 0.10% / 360 = ($0.01)
 For the Cash [[Borrower]] (Repo Side), the Total Start of Day FOS amount paid to [[FICC]] is: ($13,237.31) + 
$5,000.00 + $0.01 = ($8,237.30)
 For the Cash Lender (Reverse Side), the Total Start of Day FOS amount collected from [[FICC]] is: $13,237.31 + 
($5,000.00) + ($0.01) = $8,237.30
Term GCF Repo Transaction Details on Day 2
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
13

---

## Page 14

 Based on the trade data, the GCF Finance Report generated on Day 2 will report the following:
 Accrued Repo Interest-to-Date: ($10,000.00) 
 GCF Forward Mark : ($3,237.31) 
GCF Finance Report – Day 2 – Repo Side (Cash [[Borrower]])
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
14


---

## Page 15

 Based on the trade data, the GCF Finance Report generated on Day 2 will report the following:
 Accrued Repo Interest-to-Date: $10,000.00 
 GCF Forward Mark : $3,237.31 
GCF Finance Report – Day 2 – Reverse Side (Cash Lender)
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
15


---

## Page 16

 Based on the trade data, the GCF Forward Mark Report generated on Day 2 will report the following:
 GCF Forward Mark: ($13,237.31)
GCF Forward Mark Report – Day 2 – Repo Side (Cash [[Borrower]])
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
16


---

## Page 17

 Based on the trade data, the GCF Forward Mark Report generated on Day 2 will report the following:
 GCF Forward Mark: $13,237.31
GCF Forward Mark Report – Day 2 – Reverse Side (Cash Lender)
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
17


---

## Page 18

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 2 will report the following:
 GCF Forward Mark Adjustment Payment: ($13,237.31)
 GCF Forward Mark Adjustment Payment Return: $5,000.00
 GCF Interest Adjustment Payment: $0.01
 Total Paid/Collected: ($8,237.30) 
GCF Funds [[settlement]] Report – Day 2 – Repo Side (Cash [[Borrower]])
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
18


---

## Page 19

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 2 will report the following:
 GCF Forward Mark Adjustment Payment: $13,237.31
 GCF Forward Mark Adjustment Payment Return: ($5,000.00)
 GCF Interest Adjustment Payment: ($0.01)
 Total Paid/Collected: $8,237.30 
GCF Funds [[settlement]] Report – Day 2 – Reverse Side (Cash Lender)
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
19


---

## Page 20

Transaction Details
Start Money: $1 billion ($1,000,000,000.00) GCF Repo Generic [[CUSIP]]: FFFIX - 371487AL3
Term: 3 Days (0 days left) Transaction Type: Repo
Contract Repo Rate: 0.18% Trade Date: 09/20/2021
Start Date: 09/20/2021 End Date: 09/23/2021
System Repo Rate: N/A Overnight Investment Rate: 0.10%
Based on this trade data you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 3:
 Accrued Repo Interest-to-Date is: 0.18% * $1,000,000,000 * 3 / 360 = $15,000.00
 GCF Transaction Adjustment Payment is: 0.18% * $1,000,000,000 * 3 / 360 = $15,000.00
 GCF Interest Rate Mark is not
calculated for End Leg [[settlement]] Date
 GCF Forward Mark is not calculated for End Leg [[settlement]] Date
 The GCF Forward Mark Adjustment Payment Return is ($13,237.31)
 The GCF Interest Adjustment Payment is: $13,237.31 * 0.10% / 360 = ($0.04)
 Through FOS, [[FICC]] will collect $1,762.65 from the cash [[Borrower]] and pay $1,762.65 to the cash lender. 
 For the Cash [[Borrower]] (Repo Side), the Total Start of Day FOS amount paid to [[FICC]] is: ($15,000.00) + 
$13,237.31 + $0.04 = ($1,762.65)
 For the Cash Lender (Reverse Side), the Total Start of Day FOS amount collected from [[FICC]] is: $15,000.00 + 
($13,237.31) + ($0.04) = $1,762.65
Term GCF Repo Transaction Details on Day 3
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
20

---

## Page 21

 Based on the trade data, the GCF Finance Report generated on Day 3 will report the following:
 GCF Transaction Adjustment Payment (TAP): ($15,000.00) 
GCF Finance Report – Day 3 – Repo Side (Cash [[Borrower]])
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
21


---

## Page 22

 Based on the trade data, the GCF Finance Report generated on Day 3 will report the following:
 GCF Transaction Adjustment Payment (TAP): $15,000.00 
GCF Finance Report – Day 3 – Reverse Side (Cash Lender)
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
22


---

## Page 23

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 3 will report the following:
 GCF Transaction Adjustment Payment (TAP): ($15,000.00)
 GCF Forward Mark Adjustment Payment Return: $13,237.31
 GCF Interest Adjustment Payment: $0.04
 Total Paid/Collected: ($1,762.65) 
GCF Funds [[settlement]] Report – Day 3 – Repo Side (Cash [[Borrower]])
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
23


---

## Page 24

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 3 will report the following:
 GCF Transaction Adjustment Payment (TAP): $15,000.00
 GCF Forward Mark Adjustment Payment Return: ($13,237.31)
 GCF Interest Adjustment Payment: ($0.04)
 Total Paid/Collected: $1,762.65 
GCF Funds [[settlement]] Report – Day 3 – Reverse Side (Cash Lender)
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
24


---

## Page 25

 Based on the trade data, the GCF Final [[settlement]] Report generated on Day 3 will report the following:
 The Final Money is $1,000,015,000.00. 
 Principal of $1,000,000,000.00 is settled via Tri-Party and the total repo interest of ($15,000.00) 
is settled via FOS.
GCF Final [[settlement]] Report – Day 3 – Repo Side (Cash [[Borrower]])
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
25


---

## Page 26

 Based on the trade data, the GCF Final [[settlement]] Report generated on Day 3 will report the following:
 The Final Money is $1,000,015,000.00. 
 Principal of $1,000,000,000.00 is settled via Tri-Party and the total repo interest of $15,000.00 
is settled via FOS.
GCF Final [[settlement]] Report – Day 3 – Reverse Side (Cash Lender)
GCF Repo FOS Scenario for Term GCF Repo – Dealer View
26


---

## Page 27

GCF Repo FOS Scenario for Term GCF Repo – Dealer View
Term GCF Repo Transaction –GCF Repo FOS Summary Day over Day
As the cash [[Borrower]] of the GCF Repo Transaction, the GCF Repo FOS components would be applied as follows:
As the cash lender of the GCF Repo Transaction, the GCF Repo FOS components would be applied as follows:
GCF  Repo Transaction - Reverse Side (Cash Lender)
Remaining Business Days in Term 3 2 1 0
Business Day in Term 0 1 2 3
9/20/2021 7/21/2021 7/22/2021 7/23/2021
GCF Transaction Adjustment Payment $            - $               - $                 - $  15,000.00 
GCF Forward Mark Adjustment Payment $            - $  5,000.00 $  13,237.31 $                 -
GCF Forward Mark Adjustment Payment Return $            - $               - $   (5,000.00) $(13,237.31)
GCF Interest Adjustment Payment $            - $               - $           (0.01) $           (0.04)
CCIT Daily Repo Interest   $            - $               - $                 - $                 -
Total FOS $            - $  5,000.00 $    8,237.30 $    1,762.65 
GCF Repo Transaction - Repo Side (Cash [[Borrower]])
Remaining Business Days in Term 3 2 1 0
Business Day in Term 0 1 2 3
9/20/2021 9/21/2021 9/22/2021 9/23/2021
GCF Transaction Adjustment Payment $            - $               - $                 - $(15,000.00)
GCF Forward Mark Adjustment Payment $            - $(5,000.00) $(13,237.31) $                 -
GCF Forward Mark Adjustment Payment Return $            - $               - $    5,000.00 $  13,237.31 
GCF Interest Adjustment Payment $            - $               - $            0.01 $            0.04 
CCIT Daily Repo Interest   $            - $               - $                 - $                 -
Total FOS $            - $(5,000.00) $   (8,237.30) $   (1,762.65)

---

## Page 28

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center


---

## Page 29

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD215