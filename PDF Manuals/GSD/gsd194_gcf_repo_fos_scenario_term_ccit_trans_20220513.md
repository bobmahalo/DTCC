---
title: "GSD GCF Repo FOS Scenario: Term CCIT™ Transaction "
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd194_gcf_repo_fos_scenario_term_ccit_trans_20220513.pdf"
pages: 26
size: "881.1 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD GCF Repo FOS Scenario: Term CCIT™ Transaction 

**Original File:** [gsd194_gcf_repo_fos_scenario_term_ccit_trans_20220513.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd194_gcf_repo_fos_scenario_term_ccit_trans_20220513.pdf)  
**Category:** GSD  
**Total Pages:** 26  
**File Size:** 881.1 KB  

---

## Page 1

GCF Repo 
Funds-Only [[settlement]] 
(FOS) 
Fixed Income Clearing Corporation
Government [[securities]] Division
Scenario: Term CCIT™ Transaction

---

## Page 2

The GCF Repo FOS Scenario for Term CCIT™ Transaction  (hereinafter, the "document") is provided as a convenience to Members and is for information 
purposes only. Although [[FICC]] may make this document available to Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, 
shall [[FICC]] have a continuing obligation to make available this document or other related information of a certain type. 
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
GCF Forward Mark Adjustment Payment = Accrued Repo Interest-to-Date + GCF Interest Rate Mark 
 Accrued Interest passes from the Netting [[Member]] (cash [[Borrower]]) to the CCIT [[Member]] (cash lender) daily. On 
[[settlement]] date, the total repo interest is calculated and collected through the GCF Transaction Adjustment 
Payment (TAP) component for the Netting [[Member]] and is calculated and paid through the CCIT Daily Repo 
Interest component for the CCIT [[Member]]. 
 Accrued Interest on a CCIT Transaction is captured as the Accrued Repo Interest-to-Date and is calculated as: 
Accrued Repo Interest-to-Date = Contract Repo Rate * Start Money * Number of days between the next business date and the Start Date / 360 
*For additional clarification, please note that the Invoice Amount and the Miscellaneous Adjustment Amount is not reported on the GCF Funds [[settlement]] 
Report but may be applicable to Members of the CCIT Service or GCF Repo Service and is reported on the Start of Day Funds [[settlement]] Statement that 
is generated nightly and posted to the Funds-Only [[settlement]] Folder within [[FICC]] Repot Center. 
GCF Repo Funds-Only [[settlement]] (FOS) Overview for a Term CCIT Transaction
GCF Repo FOS Scenario for Term CCIT™ Transaction 
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
GCF Repo Funds-Only [[settlement]] (FOS) Overview for a Term CCIT Transaction (Cont.)
GCF Repo FOS Scenario for Term CCIT™ Transaction 
4

---

## Page 5

Transaction Details 
Start Money: $750,000,000.00 GCF Repo Generic [[CUSIP]]: FFARM - 371487AM1
Final Money: $750,006,250.00 Term: 2 Days
Contract Repo Rate: 0.15% Trade Date: 07/19/2021
Start Date: 07/19/2021 End Date: 07/21/2021
Based on this trade data you can expect the following:
 Daily accrued interest is: 0.15% * $750,000,000 / 360 = $3,125.00
 The total repo interest is: 0.15% * $750,000,000 * 2 / 360 = $6,250.00
 The principal of $750,000,000.00 is settled via Tri-Party and the Total Repo Interest of $6,250.00 is settled via 
FOS over a 2-day period.
Term CCIT Transaction Details
GCF Repo FOS Scenario for Term CCIT™ Transaction 
5

---

## Page 6

Transaction Details 
Start Money: $750,000,000.00 GCF Repo Generic [[CUSIP]]: FFARM - 371487AM1
Final Money: $750,006,250.00 Term: 2 Days 
Contract Repo Rate: 0.15% Trade Date: 07/19/2021
Start Date: 07/19/2021 End Date: 07/21/2021
System Repo Rate: 0.15%
Based on this trade data, you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 1:
 Accrued Repo Interest-to-Date is: 0.15% * $750,000,000 *1 / 360 = $3,125.00.
 The CCIT Daily Repo Interest for the CCIT [[Member]] is $3,125.00.
 The CCIT Daily Repo Interest for the Netting [[Member]] is ($3,125.00).
 The GCF Interest Rate Mark is: (0.15% - 0.15%) * $1,000,000,000 * 1 / 360 = $0.00.
 The GCF Forward Mark Adjustment Payment is $0.00.
 For the CCIT [[Member]] (Cash Lender), the Total Start of Day FOS amount is $3,125.00.
 For the Netting [[Member]] (Cash [[Borrower]]), the Total Start of Day FOS amount is ($3,125.00).
Term CCIT Transaction Details on Day 1
GCF Repo FOS Scenario for Term CCIT™Transaction 
6

---

## Page 7

 Based on the trade data, the CCIT Trade Report generated for Day 1 will report the following:
 CCIT Daily Repo Interest: ($3,125.00) 
CCIT Trade Report – Day 1 – Repo Side (Netting [[Member]]):
GCF Repo FOS Scenario for Term CCIT™ Transaction 
7


---

## Page 8

 Based on the trade data, the CCIT Trade Report generated for Day 1 will report the following:
 CCIT Daily Repo Interest: $3,125.00 
CCIT Trade Report – Day 1 – Reverse Side (CCIT [[Member]]):
GCF Repo FOS Scenario for Term CCIT™ Transaction 
8


---

## Page 9

 Based on the trade data, the GCF Finance Report generated for Day 1 will report the following:
 CCIT Daily Repo Interest: ($3,125.00)
 GCF Forward Mark Adjustment Payment: $0.00
GCF Finance Report – Day 1 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
9


---

## Page 10

 Based on the trade data, the GCF Finance Report generated for Day 1 will report the following:
 CCIT Daily Repo Interest: $3,125.00 
 GCF Forward Mark Adjustment Payment: $0.00
GCF Finance Report – Day 1 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
10


---

## Page 11

 Based on the trade data, the GCF Forward Mark Report generated for Day 1 will report the following:
 GCF Forward Mark: $0.00
GCF Forward Mark Report – Day 1 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
11


---

## Page 12

 Based on the trade data, the GCF Forward Mark Report generated for Day 1 will report the following:
 GCF Forward Mark: $0.00
GCF Forward Mark Report – Day 1 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
12


---

## Page 13

 Based on the trade data, the GCF Funds [[settlement]] Report generated for Day 1 will report the following:
 CCIT Repo Interest: ($3,125.00)
 Total Paid/Collected: ($3,125.00) 
GCF Funds [[settlement]] Report – Day 1 – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
13


---

## Page 14

 Based on the trade data, the GCF Funds [[settlement]] Report generated for Day 1 will report the following:
 CCIT Repo Interest: $3,125.00
 Total Paid/Collected: $3,125.00
GCF Funds [[settlement]] Report – Day 1 – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
14


---

## Page 15

Transaction Details 
Start Money: $750,000,000.00 GCF Repo Generic [[CUSIP]]: FFARM - 371487AM1
Final Money: $750,006,250.00 Term: 2 Days 
Contract Repo Rate: 0.15% Trade Date: 07/19/2021
Start Date: 07/19/2021 End Date: 07/21/2021
System Repo Rate: 0.0%
Based on this trade data, you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on End Date:
 Accrued Repo Interest-to-Date is: 0.15% * $750,000,000 * 2 / 360 = $6,250.00.
 GCF Transaction Adjustment Payment is: 0.15% * $750,000,000 * 2 / 360 = $6,250.00.
 The CCIT Daily Repo Interest for the CCIT [[Member]] is $3,125.00.
 The CCIT Daily Repo Interest for the Netting [[Member]] is $3,125.00.
 The GCF Transaction Adjustment Payment for the Netting [[Member]] is ($6,250.00).
 For the CCIT [[Member]] (Cash Lender), the Total Start of Day FOS amount is $3,125.00. 
 For the Netting [[Member]] (Cash [[Borrower]]), the Total Start of Day FOS amount is: $3,125.00 + ($6,250.00) = 
($3,125.00).
Term CCIT Transaction Details on End Date
GCF Repo FOS Scenario for Term CCIT™Transaction 
15

---

## Page 16

 Based on the trade data, the CCIT Trade Report generated for End Date will report the following:
 CCIT Daily Repo Interest: ($3,125.00) 
CCIT Trade Report – End Date – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
16


---

## Page 17

 Based on the trade data, the CCIT Trade Report generated for End Date will report the following:
 CCIT Daily Repo Interest: $3,125.00
CCIT Trade Report – End Date – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
17


---

## Page 18

 Based on the trade data, the GCF Finance Report generated for End Date will report the following:
 CCIT Daily Repo Interest: $3,125.00
 GCF Transaction Adjustment Payment: ($6,250.00)
GCF Finance Report – End Date – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
18


---

## Page 19

 Based on the trade data, the GCF Finance Report generated for End Date will report the following:
 CCIT Daily Repo Interest: $3,125.00
GCF Finance Report – End Date – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
19


---

## Page 20

 Based on the trade data, the GCF Final [[settlement]] Report generated for End Date will report the following:
 The Final Money is ($750,06,250.00).
 Principal of ($750,000,000.00) is settled via Tri-Party and total repo interest of ($6,250.00) is 
settled via FOS.
GCF Final [[settlement]] Report – End Date – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
20


---

## Page 21

 Based on the trade data, the GCF Final [[settlement]] Report generated for End Date will report the following:
 The Final Money is $750,06,250.00 
 Principal of $750,000,000.00 is settled via Tri-Party and total repo interest of $6,250.00 is settled 
via FOS.
GCF Final [[settlement]] Report – End Date – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
21


---

## Page 22

 Based on the trade data, the GCF Funds [[settlement]] Report generated for End Date will report the following:
 GCF Transaction Adjustment Payment: ($6,250.00)
 CCIT Repo Interest: $3,125.00
 Total Paid/Collected: ($3,125.00)
GCF Funds [[settlement]] Report – End Date – Repo Side (Netting [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
22


---

## Page 23

 Based on the trade data, the GCF Funds [[settlement]] Report generated for End Date will report the following:
 CCIT Repo Interest: $3,125.00
 Total Paid/Collected: $3,125.00
GCF Funds [[settlement]] Report – End Date – Reverse Side (CCIT [[Member]])
GCF Repo FOS Scenario for Term CCIT™Transaction 
23


---

## Page 24

Term CCIT Transaction – GCF Repo FOS Summary Day over Day
GCF Repo FOS Scenario for Term CCIT™ Transaction 
24
As the cash [[Borrower]]/repo side of the CCIT Transaction, the FOS components would be applied as follows:
As the cash lender/reverse side of the CCIT Transaction, the FOS components would be applied as follows:
Remaining Business Days in Term 2 1 0 NET FOS
Business Day in Term 0 1 2
7/19/2021 7/20/2021 7/21/2021
GCF Transaction Adjustment Payment  $            -    $               -    $ (6,250.00)
GCF Forward Mark Adjustment Payment  $            -    $               -    $                -   
GCF Forward Mark Adjustment Payment Return  $            -    $               -    $                -   
GCF Interest Adjustment Payment  $            -    $               -    $                -   
CCIT Daily Repo Interest    $            -    $(3,125.00)  $   3,125.00 
      
Total FOS  $            -    $(3,125.00)  $ (3,125.00)  $ (6,250.00)
Repo Side (Netting [[Member]] /Cash [[Borrower]])
Remaining Business Days in Term 2 1 0 NET FOS
Business Day in Term 0 1 2
7/19/2021 7/20/2021 7/21/2021
GCF Transaction Adjustment Payment  $            -    $               -    $                -   
GCF Forward Mark Adjustment Payment  $            -    $               -    $                -   
GCF Forward Mark Adjustment Payment Return  $            -    $               -    $                -   
GCF Interest Adjustment Payment  $            -    $               -    $                -   
CCIT Daily Repo Interest    $            -    $  3,125.00  $   3,125.00 
      
Total FOS  $            -    $  3,125.00  $   3,125.00  $   6,250.00 
Reverse Side (CCIT [[Member]]/Cash Lender)

---

## Page 25

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
25

---

## Page 26

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD194