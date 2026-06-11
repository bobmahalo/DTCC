---
title: "GCF Repo Funds-Only Settlement (FOS) Scenario: Forward-Starting CCIT™ Transaction"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd196_gcf_repo_fos_scenario_for_fwd_st_ccit_transaction_20220623.pdf"
pages: 44
size: "1414.9 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GCF Repo Funds-Only Settlement (FOS) Scenario: Forward-Starting CCIT™ Transaction

**Original File:** [gsd196_gcf_repo_fos_scenario_for_fwd_st_ccit_transaction_20220623.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd196_gcf_repo_fos_scenario_for_fwd_st_ccit_transaction_20220623.pdf)  
**Category:** GSD  
**Total Pages:** 44  
**File Size:** 1414.9 KB  

---

## Page 1

GCF Repo  
Funds-Only [[settlement]] 
(FOS) 
Fixed Income Clearing Corporation
Government [[securities]] Division
Scenario: Forward-Starting CCIT™ Transaction

---

## Page 2

The GCF Repo FOS Scenario for Forw ard Starting CCIT™ Transaction (hereinafter, the "document") is provided as a convenience to Members and is for 
information purposes only. Although [[FICC]] may make this document available to Members, it shall be under no obligation to [[DO]] s o, nor having once or more 
done so, shall [[FICC]] have a continuing obligation to make available this document or other related information of a certain ty pe.
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

 GCF Repo Funds-Only [[settlement]] amounts are paid/collected once a day at 10:00 AM.
 For CCIT Members’ CCIT Activity, GCF Repo Funds-Only [[settlement]] is a daily process that includes the 
calculation of Accrued Interest which is captured as the CCIT Daily Repo Interest component.  
 For Netting Members’ CCIT Activity, GCF Repo Funds-Only [[settlement]] is a daily process that includes the 
calculations of the following components: GCF Forward Mark Adjustment Payment/Return, CCIT Daily Repo 
Interest or GCF Transaction Adjustment Payment (TAP) and the GCF Interest Adjustment Payment. 
 These components are captured on the GCF Funds [[settlement]] Report that is generated to the GCF section of 
[[FICC]] Report Center.
*
 The GCF Forward Mark Adjustment Payment/Return is equal to the sum of the GCF Interest Rate Mark and 
Accrued Repo Interest-to-Date. 
GCF Forward Mark Adjustment Payment = Accrued Repo Interest -to-Date + GCF Interest Rate Mark 
 Accrued Interest passes from the Netting [[Member]] (cash [[Borrower]]) to the CCIT [[Member]] (cash lender) daily. On 
[[settlement]] date, the total repo interest is calculated and collected through the GCF Transaction Adjustment 
Payment (TAP) component for the Netting [[Member]] and is calculated and paid through the CCIT Daily Repo 
Interest component for the CCIT [[Member]]. 
 Accrued Interest on a CCIT Transaction is captured as the Accrued Repo Interest-to-Date and is calculated as: 
Accrued Repo Interest -to-Date = Contract Repo Rate * Start Money * Number of days between the next business date and the Start D ate / 360 
*For additional clarification, please note that the Invoice Amount and the Miscellaneous Adjustment Amount is not reported on the GCF Funds [[settlement]] 
Report but may be applicable to Members of the CCIT Service or GCF Repo Service and is reported on the Start of Day Funds Set tlement Statement that 
is generated nightly and posted to the Funds -Only [[settlement]] Folder w ithin [[FICC]] Repot Center. 
GCF Repo Funds-Only [[settlement]] (FOS) Overview for a Forward Starting CCIT Transaction
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
3

---

## Page 4

 The calculation of the GCF Interest Rate Mark takes into account the difference between the Contract Repo Rate 
on the trade and the System Repo Rate. If the System Repo Rate is less than the Contract Repo Rate on the 
trade, then the GCF Interest Rate Mark for the cash [[Borrower]] will be negative (debit) and for the cash lender it will 
be positive (credit). If the System Repo Rate is greater than the Contract Repo Rate on the trade, then the GCF 
Interest Rate Mark for the cash [[Borrower]] will be positive (credit) and for the cash lender it will be negative (debit).
GCF Interest Rate Mark = (System Repo Rate – Contract Repo Rate) * Start Money * Remaining days in term / 360
 For a CCIT Transaction, the following would apply to the GCF Interest Rate Mark:
 CCIT Members will not be credited or debited the GCF Interest Rate Mark
 Netting Members will only be debited the GCF Interest Rate Mark but not credited the GCF Interest 
Rate Mark. The GCF Interest Rate Mark is one of the components of the GCF Forward Mark. When a 
Netting [[Member]] is debited, the collected amount will be debited on the FOS statement as GCF 
Forward Mark Adjustment Payment. The debit would be held by [[FICC]] overnight and then returned to 
the Netting [[Member]] the following business day as a credit for the same amount (GCF Forward Mark 
Adjustment Payment Return).
 Interest accrued on the GCF Forward Mark Adjustment Payment is also applied on the following business day. 
This interest is the GCF Interest Adjustment Payment component.
GCF Interest Adjustment Payment = GCF Forward Mark Adjustment Payment * Overnight Investment Rate / 360
 [[FICC]] takes this approach with respect to CCIT Members because no market action would be required by [[FICC]] 
in the event of a CCIT [[Member]]’s [[default]]. This is due to the perfected security interest [[FICC]] would have in the 
CCIT [[Member]]’s underlying repo [[securities]].
GCF Repo Funds-Only [[settlement]] (FOS) Overview for a Forward Starting CCIT 
Transaction (Cont.)
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
4

---

## Page 5

Transaction Details 
Start Money: $1,000,000,000.00 GCF Repo Generic [[CUSIP]]: TR30 - 371487AE9
Final Money: $1,000,015,000.00 Term: 3 Days 
Contract Repo Rate: 0.18% Trade Date: 07/19/2021
Start Date: 07/20/2021 End Date: 07/23/2021
Based on this trade data you can expect the following :
 Daily accrued interest is: 0.18% * $1,000,000,000 / 360 = $5,000.00
 The total repo interest is: 0.18% * $1,000,000,000 * 3 / 360 = $15,000.00
 The principal of $1,000,000,000.00 is settled via Tri-Party and the Total Repo Interest of $15,000.00 is settled via 
FOS over a 3-day period.
Forward Starting CCIT Transaction Details
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
5

---

## Page 6

Transaction Details 
Start Money: $1,000,000,000.00 GCF Repo Generic [[CUSIP]]: TR30 - 371487AE9
Final Money: $1,000,015,000.00 Term: 3 Days
Contract Repo Rate: 0.18% Trade Date: 07/19/2021
Start Date: 07/20/2021 End Date: 07/23/2021
System Repo Rate: 0.18%
Based on this trade data calculated on Trade Date you can expect the following components to be collected for Start 
of Day FOS on Day 1:
 Accrued Repo Interest to Date is $0.00.
 The CCIT Daily Repo Interest for the CCIT [[Member]] is $0.00.
 The CCIT Daily Repo Interest for the Netting [[Member]] is $0.00.
 The GCF Interest Rate Mark is $0.00.
 The GCF Forward Mark Adjustment Payment is $0.00.
 For the CCIT [[Member]] (Cash Lender), the Total Start of Day FOS amount is $0.00.
 For the Netting [[Member]] (Cash [[Borrower]]), the Total Start of Day FOS amount is $0.00.
Forward Starting CCIT Transaction Details on Day 1 
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
6

---

## Page 7

 Based on the trade data, the CCIT Trade Report generated on Day 1 will report the following:
 CCIT Daily Repo Interest: $0.00 
CCIT Trade Report – Day 1 – Repo Side (Netting [[Member]]):
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
7


---

## Page 8

 Based on the trade data, the CCIT Trade Report generated on Day 1 will report the following:
 CCIT Daily Repo Interest: $0.00 
CCIT Trade Report – Day 1 – Reverse Side (CCIT [[Member]]):
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
8


---

## Page 9

 Based on the trade data, the GCF Finance Report generated on Day 1 will report the following:
 CCIT Daily Repo Interest: $0.00
 GCF Forward Mark: $0.00
GCF Finance Report – Day 1 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
9


---

## Page 10

 Based on the trade data, the GCF Finance Report generated on Day 1 will report the following:
 CCIT Daily Repo Interest: $0.00
 GCF Forward Mark: $0.00
GCF Finance Report – Day 1 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
10


---

## Page 11

 Based on the trade data, the GCF Forward Mark Report generated on Day 1 will report the following:
 GCF Forward Mark: $0.00
GCF Forward Mark Report – Day 1 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
11


---

## Page 12

 Based on the trade data, the GCF Forward Mark Report generated on Day 1 will report the following:
 GCF Forward Mark: $0.00
GCF Forward Mark Report – Day 1 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
12


---

## Page 13

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 1 will report the following:
 CCIT Repo Interest: $0.00
 T otal Paid/Collected: $0.00
GCF Funds [[settlement]] Report – Day 1 – Repo (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
13


---

## Page 14

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 1 will report the following:
 CCIT Repo Interest: $0.00
 T otal Paid/Collected: $0.00
GCF Funds [[settlement]] Report – Day 1 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
14


---

## Page 15

Transaction Details 
Start Money: $1,000,000,000.00 GCF Repo Generic [[CUSIP]]: TR30 - 371487AE9
Final Money: $1,000,015,000.00 Term: 3 Days 
Contract Repo Rate: 0.18% Trade Date: 07/19/2021
Start Date: 07/20/2021 End Date: 07/23/2021
System Repo Rate: 1.20%
Based on this trade data, you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 2:
 Accrued Repo Interest-to-Date is: 0.18% * $1,000,000,000 *1 / 360 = $5,000.00.
 The CCIT Daily Repo Interest for the CCIT [[Member]] is $5,000.00.
 The CCIT Daily Repo Interest for the Netting [[Member]] is ($5,000.00).
 The GCF Interest Rate Mark for the CCIT [[Member]] is: (0.18% - 1.2%) * $1,000,000,000 * 2 / 360 = ($56,667.67).
 The GCF Interest Rate Mark for the Netting [[Member]] is: (0.18% - 1.2%) * $1,000,000,000 * 2 / 360 = $56,667.67.*
 The GCF Forward Mark Adjustment Payment is not applied.**
 For the CCIT [[Member]] (Cash Lender), the Total Start of Day FOS amount is $5,000.00.
 For the Netting [[Member]] (Cash [[Borrower]]), the Total Start of Day FOS amount s ($5,000.00)
.
*If the System Repo Rate is greater than the Contract Repo Rate on the trade, then the GCF Interest Rate Mark for the cash bor row er w ill be positive (credit) 
and for the cash lender it w ill be negative (debit).
**CCIT Members w ill not be credited or debited the GCF Interest Rate Mark. Netting Members w ill only be debited the GCF Interes t Rate Mark but not 
credited the GCF Interest Rate Mark. In this scenario, a credit GCF Interest Rate Mark w as calculated for the Netting [[Member]] and a debit GCF Interest Rate 
Mark w as calculated for the CCIT [[Member]]. The GCF Interest Rate Mark is one of the components of the GCF Forw ard Mark. Therefore, the GCF Forw ard 
Mark Adjustment Payment w ill not be applied. 
Forward Starting CCIT Transaction Details on Day 2
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
15

---

## Page 16

 Based on the trade data, the CCIT Trade Report generated on Day 2 will report the following:
 CCIT Daily Repo Interest: ($5,000.00) 
CCIT Trade Report – Day 2 – Repo Side (Netting [[Member]]):
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
16


---

## Page 17

 Based on the trade data, the CCIT Trade Report generated on Day 2 will report the following:
 CCIT Daily Repo Interest: $5,000.00 
CCIT Trade Report – Day 1 – Reverse Side (CCIT [[Member]]):
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
17


---

## Page 18

 Based on the trade data, the GCF Finance Report generated on Day 2 will report the following:
 CCIT Daily Repo Interest: ($5,000.00)
 GCF Interest Rate Mark: $56,666.67 (not applied)
 GCF Forward Mark Adjustment Payment: $56,666.67 (not applied)
GCF Finance Report – Day 2 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
18


---

## Page 19

 Based on the trade data, the GCF Finance Report generated on Day 2 will report the following:
 CCIT Daily Repo Interest: $5,000.00 
 GCF Interest Rate Mark: ($56,666.67) (not applied)
 GCF Forward Mark Adjustment Payment: ($56,666.67) (not applied)
GCF Finance Report – Day 1 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
19


---

## Page 20

 Based on the trade data, the GCF Forward Mark Report generated on Day 2 will report the following:
 GCF Forward Mark: $0.00
GCF Forward Mark Report – Day 2 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
20


---

## Page 21

 Based on the trade data, the GCF Forward Mark Report generated on Day 2 will report the following:
 GCF Forward Mark: $0.00
GCF Forward Mark Report – Day 2 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
21


---

## Page 22

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 2 will report the following:
 CCIT Repo Interest: ($5,000.00)
 T otal Paid/Collected: ($5,000.00) 
GCF Funds [[settlement]] Report – Day 2 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
22


---

## Page 23

 Based on the trade data, the GCF Funds [[settlement]] Report generated on Day 2 will report the following:
 CCIT Repo Interest: $5,000.00
 T otal Paid/Collected: $5,000.00
GCF Funds [[settlement]] Report – Day 2 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
23


---

## Page 24

Transaction Details 
Start Money: $1,000,000,000.00 GCF Repo Generic [[CUSIP]]: TR30 - 371487AE9
Final Money: $1,000,015,000.00 Term: 3 Days 
Contract Repo Rate: 0.18% Trade Date: 07/19/2021
Start Date: 07/20/2021 End Date: 07/23/2021
System Repo Rate: 0.234%
Based on this trade data, you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 3:
 Accrued Repo Interest-to-Date is: 0.18% * $1,000,000,000 *2 / 360 = $10,000.00.
 The CCIT Daily Repo Interest for the CCIT [[Member]] is $5,000.00.
 The CCIT Daily Repo Interest for the Netting [[Member]] is ($5,000.00).
 The GCF Interest Rate Mark for the CCIT [[Member]] is: (0.18% - .234%) * $1,000,000,000 * 1 / 360 = ($1,500.00).
 The GCF Interest Rate Mark for the Netting [[Member]] is: (0.18% - .234%) * $1,000,000,000 * 1 / 360 = $1,500.00.*
 The GCF Forward Mark Adjustment Payment is not applied.**
 For the CCIT [[Member]] (Cash Lender), the Total Start of Day FOS amount is $5,000.00.
 For the Netting [[Member]] (Cash [[Borrower]]), the Total Start of Day FOS amount is ($5,000.00).
*
If the System Repo Rate is greater than the Contract Repo Rate on the trade, then the GCF Interest Rate Mark for the cash bor row er w ill be positive (credit) 
and for the cash lender it w ill be negative (debit).
**CCIT Members w ill not be credited or debited the GCF Interest Rate Mark. Netting Members w ill only be debited the GCF Interes t Rate Mark but not 
credited the GCF Interest Rate Mark. In this scenario, a credit GCF Interest Rate Mark w as calculated for the Netting [[Member]] and a debit GCF Interest Rate 
Mark w as calculated for the CCIT [[Member]]. The GCF Interest Rate Mark is one of the components of the GCF Forw ard Mark. Therefore, the GCF Forw ard 
Mark Adjustment Payment w ill not be applied. 
Forward Starting CCIT Transaction Details on Day 3
GCF/CCIT FOS: CCIT [[Member]] vs. Netting [[Member]] View on Forward Starting CCIT™ Trade
24

---

## Page 25

 Based on the trade data, the CCIT Trade Report generated on Day 3 will report the following:
 CCIT Daily Repo Interest: ($5,000.00) 
CCIT Trade Report – Day 3 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
25


---

## Page 26

 Based on the trade data, the CCIT Trade Report generated on Day 3 will report the following:
 CCIT Daily Repo Interest: $5,000.00
CCIT Trade Report – Day 3 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
26


---

## Page 27

 Based on the trade data, the GCF Finance Report generated for Day 3 will report the following:
 CCIT Daily Repo Interest: ($5,000.00)
 GCF Interest Rate Mark: $1,500.00 (not applied)
 GCF Forward Mark Adjustment Payment: $1,500.00 (not applied)
GCF Finance Report – Day 3 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
27


---

## Page 28

 Based on the trade data, the GCF Finance Report generated for Day 3 will report the following:
 CCIT Daily Repo Interest: $5,000.00
 GCF Interest Rate Mark: ($1,500.00) (not applied)
 GCF Forward Mark Adjustment Payment: ($1,500.00) (not applied)
GCF Finance Report – Day 3 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
28


---

## Page 29

 Based on the trade data, the GCF Forward Mark Report generated for Day 3 will report the following:
 GCF Forward Mark: $0.00
GCF Forward Mark Report – Day 3 – Repo Side (Netting [[Member]])
GCF/CCIT FOS: CCIT [[Member]] vs. Netting [[Member]] View on Forward Starting CCIT™ Trade
29


---

## Page 30

 Based on the trade data, the GCF Forward Mark Report generated for Day 3 will report the following:
 GCF Forward Mark: $0.00
GCF Forward Mark Report – Day 3 – Reverse Side (CCIT [[Member]])
GCF/CCIT FOS: CCIT [[Member]] vs. Netting [[Member]] View on Forward Starting CCIT™ Trade
30


---

## Page 31

 Based on the trade data, the GCF Funds [[settlement]] Report generated for Day 3 will report the following:
 CCIT Repo Interest: ($5,000.00)
 T otal Paid/Collected: ($5,000.00) 
GCF Funds [[settlement]] Report – Day 3 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
31


---

## Page 32

 Based on the trade data, the GCF Funds [[settlement]] Report generated for Day 1 will report the following:
 CCIT Repo Interest: $5,000.00
 T otal Paid/Collected: $5,000.00
GCF Funds [[settlement]] Statement – Day 3 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
32


---

## Page 33

Transaction Details 
Start Money: $1,000,000,000.00 GCF Repo Generic [[CUSIP]]: TR30 - 371487AE9
Final Money: $1,000,015,000.00 Term: 3 Days 
Contract Repo Rate: 0.18% Trade Date: 07/19/2021
Start Date: 07/20/2021 End Date: 07/23/2021
System Repo Rate: 1.20%
Based on this trade data, you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day on End Date:
 Accrued Interest to Date is 0.18% * $1,000,000,000 *1 / 360 = $15,000.00
 The Transaction Adjustment Payment is ($15,000.00)
 The Daily CCIT Repo Interest is $5,000.00
 For the CCIT [[Member]], the Total Start of Day FOS amount paid is $5,000.00
 For the Netting [[Member]], the Total Start of Day FOS amount collected is $10,000.00 + ($15,000.00 ) = 
($5,000.00)
Forward Starting CCIT Transaction Details on End Date
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
33

---

## Page 34

 Based on the trade data, the CCIT Trade Report generated for End Date will report the following:
 CCIT Daily Repo Interest: ($5,000.00) 
CCIT Trade Report – End Date – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
34


---

## Page 35

 Based on the trade data, the CCIT Trade Report generated for End Date will report the following:
 CCIT Daily Repo Interest: $5,000.00
CCIT Trade Report – End Date – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
35


---

## Page 36

 Based on the trade data, the GCF Finance Report generated for End Date will report the following:
 CCIT Daily Repo Interest: $10,0000.00
 GCF Transaction Adjustment Payment: ($15,000.00)
GCF Finance Report – End Date – Repo Side (Netting [[Member]])
GCF/CCIT FOS: CCIT [[Member]] vs. Netting [[Member]] View on Forward Starting CCIT™ Trade
36


---

## Page 37

 Based on the trade data, the GCF Finance Report generated for End Date will report the following:
 CCIT Daily Repo Interest: $5,000.00
GCF Finance Report – End Date – Reverse Side (CCIT [[Member]])
GCF/CCIT FOS: CCIT [[Member]] vs. Netting [[Member]] View on Forward Starting CCIT™ Trade
37


---

## Page 38

 Based on the trade data, the GCF Final [[settlement]] Report generated for End Date will report the following:
 The Final Money is ($1,000,015,000.00).
 Principal of ($1,000,000,000.00) is settled via Tri-Party and total repo interest of ($15,000.00) is 
settled via FOS.
GCF Final [[settlement]] Report – End Date – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
38


---

## Page 39

 Based on the trade data, the GCF Final [[settlement]] Report generated for End Date will report the following:
 The Final Money is $1,000,015,000.00.
 Principal of $1,000,000,000.00 is settled via Tri-Party and total repo interest of $15,000.00 is 
settled via FOS.
GCF Final [[settlement]] Report – End Date – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
39


---

## Page 40

 Based on the trade data, the GCF Funds [[settlement]] Report generated for End Date will report the following:
 GCF Transaction Adjustment Payment: ($15,000.00)
 CCIT Repo Interest: $10,000.00
 T otal Paid/Collected: ($5,000.00)
GCF Funds [[settlement]] Statement – End Date – Repo Side (Netting [[Member]])
GCF/CCIT FOS: CCIT [[Member]] vs. Netting [[Member]] View on Forward Starting CCIT™ Trade
40


---

## Page 41

 Based on the trade data, the GCF Funds [[settlement]] Report generated for End Date will report the following:
 CCIT Repo Interest: $5,000.00
 T otal Paid/Collected: $5,000.00
GCF Funds [[settlement]] Report – End Date – Reverse Side (CCIT [[Member]])
GCF/CCIT FOS: CCIT [[Member]] vs. Netting [[Member]] View on Forward Starting CCIT™ Trade
41


---

## Page 42

Forward Starting CCIT Transaction – GCF FOS Summary Day over Day
GCF Repo FOS Scenario for Forward Starting CCIT™ Transaction 
42
As the cash [[Borrower]]/repo side of the CCIT Transaction, the FOS components would be applied as follows:
As the cash lender/reverse side of the CCIT Transaction, the FOS components would be applied as follows:
Remaining Business Days in Term T 3 2 1 0 NET FOS
Business Day in Term T 0 1 2 3
7/19/2021 7/20/2021 7/21/2021 7/22/2021 7/23/2021
GCF Transaction Adjustment Payment  $            -    $            -    $                -    $                -    $ (15,000.00)
GCF Forward Mark Adjustment Payment  $            -    $            -    $                -    $                -    $                  -   
GCF Forward Mark Adjustment Payment Return  $            -    $            -    $                -    $                -    $                  -   
GCF Interest Adjustment Payment  $            -    $            -    $                -    $                -    $                  -   
CCIT Daily Repo Interest    $            -    $            -    $ (5,000.00)  $ (5,000.00)  $   10,000.00 
      
Total FOS  $            -    $            -    $ (5,000.00)  $ (5,000.00)  $    (5,000.00)  $ (15,000.00)
Repo Side (Netting [[Member]] View/Cash [[Borrower]])
Remaining Business Days in Term T 3 2 1 0 NET FOS
Business Day in Term T 0 1 2 3
7/19/2021 7/20/2021 7/21/2021 7/22/2021 7/23/2021
GCF Transaction Adjustment Payment  $            -    $            -    $                -    $                -    $                  -   
GCF Forward Mark Adjustment Payment  $            -    $            -    $                -    $                -    $                  -   
GCF Forward Mark Adjustment Payment Return  $            -    $            -    $                -    $                -    $                  -   
GCF Interest Adjustment Payment  $            -    $            -    $                -    $                -    $                  -   
CCIT Daily Repo Interest    $            -    $            -    $   5,000.00  $   5,000.00  $     5,000.00 
      
Total FOS  $            -    $            -    $   5,000.00  $   5,000.00  $     5,000.00  $   15,000.00 
Reverse Side (CCIT [[Member]] View/Cash Lender)

---

## Page 43

T o access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
43

---

## Page 44

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Cleari ng Corporation (“[[DTCC]]”). [[DTCC]] itself  
does not provide such services. Each of these affiliates is a separate legal entity, subject to the law s and regulations of the particular country or countries in w hich 
such entity operates. Please see w ww.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD196