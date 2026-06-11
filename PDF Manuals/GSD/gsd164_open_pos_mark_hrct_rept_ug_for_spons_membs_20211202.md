---
title: "FICC GSD: Open Position Mark Haircut Report User Guide for Sponsoring Members"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd164_open_pos_mark_hrct_rept_ug_for_spons_membs_20211202.pdf"
pages: 10
size: "284.5 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# FICC GSD: Open Position Mark Haircut Report User Guide for Sponsoring Members

**Original File:** [gsd164_open_pos_mark_hrct_rept_ug_for_spons_membs_20211202.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd164_open_pos_mark_hrct_rept_ug_for_spons_membs_20211202.pdf)  
**Category:** GSD  
**Total Pages:** 10  
**File Size:** 284.5 KB  

---

## Page 1

 
[[FICC]] – [[GSD]]  
OPEN POSITION MARK [[Haircut]] REPORT USER GUIDE FOR SPONSORING MEMBERS 
VERSION 2.0 
DECEMBER 02, 2021 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself 
does not provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: December 02, 2021 
Publication Code: GSD164 
Service: [[FICC]] – [[GSD]]  
Title: Open Position Mark [[Haircut]] Report User Guide for Sponsoring Members 
 
 
The Open Position Mark [[Haircut]] Report User Guide for Sponsoring Members (hereinafter, the "document") is provided as a convenience to Members and is for 
information purposes only. Although [[FICC]] may make this document available to Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, 
shall [[FICC]] have a continuing obligation to make available this document or other related information of a certain type.  
 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose of any information provided to Members 
in this document, which is provided as-is. [[FICC]] shall not be liable for any loss related to such information (or the act or process of providing such 
information) resulting directly or indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from interruptions, delays, or defects arising from 
or related to providing this guide; and (2) any special, consequential, exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members and other authorized users of the document will find the most current version of 
the document on [[DTCC]]’s Learning Center site, 
www.dtcclearning.com. [[FICC]] shall bear no responsibility for any losses associated with the failure of Members or 
other authorized users to follow [[FICC]]’s most current document. 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Open Position Mark [[Haircut]] Report for Sponsoring Members ....................................................................................................................................... 4 
Report Description: .................................................................................................................................................................................................... 4 
Frequency: ................................................................................................................................................................................................................. 4 
Header: ...................................................................................................................................................................................................................... 4 
Open Position Mark [[Haircut]] Report Fields: ............................................................................................................................................................... 5 
 

---

## Page 4

Open Position Mark [[Haircut]] Report User Guide for Sponsoring Members 
Open Position Mark [[Haircut]] Report for Sponsoring Members 4 
OPEN POSITION MARK [[Haircut]] REPORT FOR SPONSORING MEMBERS 
Report Description: 
The Open Position Mark [[Haircut]] Report provides Sponsoring Members details regarding the [[mark-to-market]] calculations that [[FICC]] applies to each 
Sponsored [[Member]] Trade. The report shows the amount of the [[Haircut]] received from a Sponsored [[Member]] or given to a Sponsored [[Member]] for 
each Sponsored [[Member]] Trade, as well as how much money is owed to or owed by each Sponsored [[Member]] to their Sponsoring [[Member]] resulting 
from [[FICC]]’s [[mark-to-market]] calculations. The report is available as a text file containing tilde-delimited data. This report user guide displays sample 
data as it would appear in MS Excel. 
Note:  
The Open Position Mark [[Haircut]] Report displays details from the perspective of the Sponsored [[Member]]. 
Frequency: 
Intraday, End of Day 
 
Header: 
[[Member]] [[ID]]: [[Member]]’s account number. 
[[Member]] Name: [[Member]]’s account name. 
Appears on the Report as: [[Member]]’s account 
number and account name as it appears on the 
Initial [[Haircut]] Report. 
  
Header 
[[Member]] [[ID]]: 9XXX 
[[Member]] Name: [[FICC]] Test Account / Omnibus 
Appears on the Report as: [[participant]] 9XXX – [[FICC]] TEST ACCOUNT OMNIBUS 
Table 1: Report Header: Open Position Mark [[Haircut]] Report 

---

## Page 5

Open Position Mark [[Haircut]] Report User Guide for Sponsoring Members 
Open Position Mark [[Haircut]] Report for Sponsoring Members 5 
Open Position Mark [[Haircut]] Report Fields: 
1 2 3 4 5 6 7 8 9 10 11 
BUS DT SETT DT PROD [[CUSIP]] TID TRD DATE START DATE CONTRACT SETT DATE EXT REFERENCE TYPE SYMBOL 
1-May-20 4-May-20 TBOND 912810QY7 trade_id1 5/1/2020 5/1/2020 5/4/2020 xref1 REPO TESTA 
1-May-20 4-May-20 TNOTE 912828ZN3 trade_id2 5/1/2020 5/1/2020 5/4/2020 xref2 REPO TESTA 
1-May-20 4-May-20 TIPSNT 912828H45 trade_id3 5/1/2020 5/1/2020 5/4/2020 xref3 REVR TESTB 
1-May-20 4-May-20 TNOTE 912828ZN3 trade_id4 5/1/2020 5/1/2020 5/4/2020 xref4 REVR TESTB 
1-May-20 4-May-20 SPONGC 84910LAA4 trade_id5 5/1/2020 5/1/2020 5/4/2020 xref5 REVR TESTB 
Table 2: Open Position Mark [[Haircut]] Report Fields (partial view) 
1. Business Date (BUS DT): This is Business Date of the report.  
2. [[settlement]] Date (SETT DT): This is the expected [[settlement]] Date for the trade being reported. 
3. Product (PROD): This represents the Product classifications to which [[securities]] belong (i.e., CASH, AGENCY, SPONGC, TBOND, TIPSBD, 
TIPSNT, TNOTE, AGCY, TR30, USTIPS, FFFIX, STRIPS, TBILL, etc.).  
Note: 
The Product for Sponsored GC trade will always be SPONGC. 
4. [[CUSIP]]: Committee on Uniform [[securities]] Identification Procedures identifying number for an Eligible Netting Security. 
5. Trade [[ID]] (TID): The Trade [[ID]] is a unique [[GSD]] generated identifier assigned to each transaction. 
6. Trade Date (TRD): The trade date that the [[Member]] indicated on their trade submission to [[FICC]] [[GSD]]’s RTTM system. 
7. Start Date: This represents the [[settlement]] date for the Start Leg of a Repo Transaction. 
Note:  
Start Date field would only apply to Repo Transactions. For the outright Buy and Sell Transactions this field will be blank. 
8. Contract [[settlement]] Date (CONTRACT SETT DATE): The contractual [[settlement]] date that the [[Member]] submitted on the trade to [[FICC]] [[GSD]]’s  
RTTM system. 
9. External Reference (EXT REFERENCE): This is the unique identifier that the [[Member]] submitted on the trade to [[FICC]] [[GSD]]’s RTTM system. 
10. [Trade] Type (TYPE): REPO, REVR, BUY or SELL. 
11. Symbol: This is the Five-character identifier for the Sponsored [[Member]]. 
 

---

## Page 6

Open Position Mark [[Haircut]] Report User Guide for Sponsoring Members 
Open Position Mark [[Haircut]] Report for Sponsoring Members 6 
 
 
12 13 14 15 16 17 18 19 
QUANTITY START AMOUNT SYS PRC CONTRACT PRICE SYSTEM VALUE CONTRACT VALUE SYSTEM REPO RATE CONTRACT REPO RATE 
50,000,000 64,579,999.99 130.5273 0 65,898,265.38 64,580,807.24 0.07168911 0.15 
50,000,000 49,000,000.00 99.9219 0 49,961,629.35 49,000,612.50 0.07168911 0.15 
50,000,000 54,947,990.19 102.342 0 55,926,026.08 54,948,127.56 0.07168911 0.03 
50,000,000 48,969,761.53 99.9219 0 49,961,629.35 48,969,883.95 0.07168911 0.03 
50,000,000 50,000,000.00 100 0 50,000,000.00 50,000,010.00 0.07168911 0.03 
Table 3: Open Position Mark [[Haircut]] Report Fields (partial view) 
 
12. Quantity: The Par amount that the [[Member]] submitted on the trade to [[FICC]] [[GSD]]’s RTTM system. 
13. Start Amount: The Start Amount is the Contract Value for the Start Leg of the Repo Transaction that the [[Member]] submitted to [[FICC]] [[GSD]]’s 
RTTM system. 
14. System Price (SYS PRC): The System Price established by [[FICC]] for the underlying Eligible Netting Security. 
15. Contract Price: The contract price for Buy/Sell trade that the [[Member]] submitted to [[FICC]] [[GSD]]’s RTTM system. 
Note:  
Contract Price field is not applicable to Repo Transactions and therefore will appear as zero in this report when a Repo Transactions is displayed in this report. 
16. System Value: The System Value is Corporation’s system calculated value for a given [[CUSIP]] based on the System Price. 
17. Contract Value: The Contract Value is the dollar value to be settled on the Scheduled [[settlement]] Date for the trade. For Repo Transactions 
this is the End Money. 
18. System Repo Rate: The System Repo Rate is the uniform repo rate calculated by [[The Corporation]] to be the market repo rate for Repo 
Transactions on given a [[CUSIP]] with the same remaining duration as a given Repo Transaction. 
19. Contract Repo Rate: The Contract Repo Rate is the rate the [[Member]] submitted on a given Repo Transaction to [[FICC]] [[GSD]]’s RTTM system. 
 
  

---

## Page 7

Open Position Mark [[Haircut]] Report User Guide for Sponsoring Members 
Open Position Mark [[Haircut]] Report for Sponsoring Members 7 
20 21 22 23 
INITIAL [[Haircut]] CURRENT [[Haircut]] [[Haircut]] DEFICIT [[Haircut]] SURPLUS 
1,178,808.14 1,317,458.14 0 138650 
968,816.85 961,016.85 -7800 0 
1,039,495.22 977,898.52 61596.7 0 
921,395.40 991,745.40 0 -70350 
Table 4: Open Position Mark [[Haircut]] Report Fields (partial view)∗ 
20. Initial [[Haircut]]∗∗: The Initial [[Haircut]] is the absolute value of the difference between the System Value of [[collateral]] for the Start Leg using the 
latest System Price and the Start Amount on the Repo Transaction. 
21. Current [[Haircut]]**: The Current [[Haircut]] is the difference between the System Value of [[collateral]] at the time of the calculation and the Final 
Money on the Repo Transaction. 
22. [[Haircut]] Deficit**: The [[Haircut]] Deficit is the amount, if any, by which the Initial [[Haircut]] exceeds the Current [[Haircut]]. 
Note:  
There will be a deficit or surplus calculated for O/N Repo Transactions that were compared before noon or term Repo Transactions that have started. A positive value 
in this field indicates money owed to the Sponsored [[Member]] by the Sponsoring [[Member]]. A negative value in this field indicates money owed to the Sponsoring 
[[Member]] by the Sponsored [[Member]]. 
23. [[Haircut]] Surplus**: The [[Haircut]] Surplus is the amount, if any, by which the Current [[Haircut]] exceeds the Initial [[Haircut]]. 
Note:  
There will be a deficit or surplus calculated for O/N Repo Transactions that were compared before noon or term Repo Transactions that have started. A positive value 
in this field indicates money owed to the Sponsored [[Member]] by the Sponsoring [[Member]]. A negative value in this field indicates money owed to the Sponsoring 
[[Member]] by the Sponsored [[Member]]. 
 
∗ Line 20 - 23 explanation for the calculations shown on the screenshots: 
a. If the Current [[Haircut]] is greater than the Initial [[Haircut]], then the [[collateral]] went up in value. The Sponsoring [[Member]] which received the [[collateral]] from their [[collateral]] provider (cash [[Borrower]]) 
Sponsored [[Member]], now has a surplus (excess) and owes the excess back to their Sponsored [[Member]]. 
b. If the Current [[Haircut]] is less than the Initial [[Haircut]], then [[collateral]] went down in value. The Sponsoring [[Member]] which received the [[collateral]] from their [[collateral]] provider (cash [[Borrower]]) 
Sponsored [[Member]], now has a deficit (shortage), so the Sponsored [[Member]] owes the deficit to the Sponsoring [[Member]]. 
c. If the Current [[Haircut]] is less than the Initial [[Haircut]] and the [[collateral]] went down in value, then the cash lender Sponsored [[Member]] now has less of the [[Haircut]] (deficit) than they require so they 
are owed money by the Sponsoring [[Member]].  
d. If the Current [[Haircut]] is greater than the Initial [[Haircut]]. Cash lender Sponsored [[Member]] has more [[Haircut]] than they need so they owe money the excess (surplus) to the Sponsoring [[Member]]. 
∗∗ This field is not applicable to Sponsored GC trades and therefore will appear as blank filled in this report when a Sponsored GC trade is displayed in this report. 

---

## Page 8

Open Position Mark [[Haircut]] Report User Guide for Sponsoring Members 
Open Position Mark [[Haircut]] Report for Sponsoring Members 8 
 
24 25 26 
INTEREST RATE MARK GC INTEREST RATE MARK FINANCING MARK 
  393.68 
  298.48 
  -334.11 
  -298.48 
 -300  
Table 5: Open Position Mark [[Haircut]] Report Fields (partial view) 
24. Interest Rate Mark*: The Interest Rate Mark is the product of the principal value of the Repo Transaction on the Scheduled [[settlement]] Date for 
its Start Leg multiplied by a factor equal to the absolute difference between the System Repo Rate established by [[The Corporation]] for such 
Repo Transaction and its Contract Repo Rate, and then multiplied by a fraction, the numerator of which is the number of calendar days from the 
Scheduled [[settlement]] Date for the Start Leg of the Repo Transaction until the Scheduled [[settlement]] Date for the End Leg of the Repo 
Transaction and the denominator of which is 360. 
Note:  
The Interest Rate Mark is only calculated on Forward Starting Repo Transactions. For all other trade types, this field will appear as blank filled in this report. 
25. GC Interest Rate Mark: The GC Interest Rate Mark is used to [[mark-to-market]] the unaccrued portion of the repo interest for the Sponsored GC 
trades based on the current System Repo Rate. This FOS component captures the same risk and calculates in the same way as the GCF 
Interest Rate Mark for GCF Repo Transactions. 
Note:  
The GC Interest Rate Mark is only calculated on Sponsored GC trades. For all other trade types, this field will appear as blank filled in this report. 
26. Financing Mark∗: The Financing Mark calculates the repo interest for the remainder of a given repo’s term using the System Repo Rate. 
Financing Mark is calculated by multiplying the Market Value of the Repo Transaction by System Repo Rate established by [[The Corporation]] for 
 
∗ This field is not applicable to Sponsored GC trades and therefore will appear as blank filled in this report when a Sponsored GC trade is displayed in this report. 
 

---

## Page 9

Open Position Mark [[Haircut]] Report User Guide for Sponsoring Members 
Open Position Mark [[Haircut]] Report for Sponsoring Members 9 
such Repo Transaction, and then multiplied by a fraction, the numerator of which is the number of calendar days from the current Business Day 
until the Scheduled [[settlement]] Date for the Repo Transaction and the denominator of which is 360. 
27 28 29 
TOTAL MARK INTEREST AP FORWARD MARK AP 
139043.68 -0.193116222 1317851.82 
-7501.52 0.010418778 961315.33 
61262.59 -0.085086931 -978232.63 
-70648.48 0.098122889 -992043.88 
-300 0.000416667 -300 
Table 6: Open Position Mark [[Haircut]] Report Fields (partial view) 
27. Total Mark: The Total Mark is the sum of the [[Haircut]] Deficit, [[Haircut]] Surplus, Interest Rate Mark, GC Interest Rate Mark and Financing Mark 
calculated for a given Sponsored [[Member]] Trade. 
Note: 
A positive value in the Total Mark column denotes the total mark, excluding the Initial [[Haircut]], that the Sponsoring [[Member]] owes their Sponsored [[Member]] on a given 
Sponsored [[Member]] Trade.  
28. Interest Adjustment Payment (Interest AP): The Interest Adjustment Payment accounts for the overnight use of funds based on the Total 
Mark amount paid to or collected from  [[FICC]] on the previous Business Day. The Interest Adjustment Payment will be displayed on the intraday 
Open Position Mark [[Haircut]] Report, but the aggregate value will be paid/collected during the start of day Funds-Only [[settlement]] cycle.  
29. Forward Mark Adjustment Payment (Forward Mark AP): The Forward Mark Adjustment Payment is the sum of the [[collateral]] Mark, 
Financing Mark and Interest Rate Mark of a particular sponsored trade. The sum of the values in the Forward Mark Adjustment Payment column 
is equal to the value that appears on the Funds-Only [[settlement]] Report. 

---

## Page 10

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 