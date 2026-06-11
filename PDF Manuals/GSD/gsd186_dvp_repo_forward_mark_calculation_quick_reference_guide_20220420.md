---
title: "DVP Repo Forward Mark Calculation Quick Reference Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd186_dvp_repo_forward_mark_calculation_quick_reference_guide_20220420.pdf"
pages: 7
size: "204.5 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# DVP Repo Forward Mark Calculation Quick Reference Guide

**Original File:** [gsd186_dvp_repo_forward_mark_calculation_quick_reference_guide_20220420.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd186_dvp_repo_forward_mark_calculation_quick_reference_guide_20220420.pdf)  
**Category:** GSD  
**Total Pages:** 7  
**File Size:** 204.5 KB  

---

## Page 1

 
 
 
[[FICC]] – [[GSD]]  
DVP REPO FORWARD MARK CALCULATION QUICK REFERENCE GUIDE 
VERSION 1.0.1 
APRIL 20, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: April 20,2022 
Publication Code: GSD186 
Service: [[FICC]] – [[GSD]]  
Title: DVP Repo Forward Mark Calculation Quick Reference Guide 
 
The DVP Repo Forward Mark Calculation Quick Reference Guide (hereinafter, the "document") is provided as a 
convenience to Members and is for information purposes only. Although [[FICC]] may make this document available to 
Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing 
obligation to make available this document or other related information of a certain type.  
 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to Members in this document, which is provided as-is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members and other authorized users of the 
document will find the most current version of the document on [[DTCC]]’s Learning Center site, 
www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow 
[[FICC]]’s most current document. 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
DVP Repo – Forward Mark Calculation .............................................................................................................. 4 
Overview ............................................................................................................................................................. 4 
Mechanics of a DVP Repo Transaction .............................................................................................................. 4 
Trade Details for an Example Repo Transaction ................................................................................................ 4 
Breakdown of Calculation for DVP Repo Trade Example ................................................................................. 5 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
Note: 
This guide has been written with the presumption that the user is familiar with [[GSD]]’s products, services and supporting 
applications. 

---

## Page 4

DVP Repo Forward Mark Calculation Quick Reference Guide 
 
 
DVP REPO – FORWARD MARK CALCULATION 
Overview 
This guide is intended to show the user how the Forward Mark Adjustment Payment (herein referred to as 
“Forward Mark”) component of Funds-Only [[settlement]] is calculated on a Term DVP Repo Transaction 
submitted to [[FICC]] [[GSD]] for comparison, [[Novation]], netting and [[settlement]]. Forward Mark is a [[mark-to-market]] on 
a repo trade. In general, [[mark-to-market]] captures the difference between the value of a trade at the inception 
and its value at the current market price. 
Mechanics of a DVP Repo Transaction 
A Repurchase agreement (repo) is just a collateralized loan. At the start of a Repo Transaction (Repo Start 
Date), the Repo Party (Dealer A) borrows cash from the Reverse Repo Party (Dealer B) in exchange for 
[[collateral]]. The Repo Transaction is executed as DVP or delivery of [[collateral]] versus the payment of cash.  
At the end of a repo term (Repo End Date), Dealer A returns the borrowed cash to Dealer B and Dealer B in 
turn gives back the [[collateral]]. Also, at the end of the repo term, Dealer A pays to Dealer B repo interest on the 
borrowed cash (assuming the agreed upon contract repo rate is positive). 
Trade Details for an Example Repo Transaction  
To explain how the Forward Mark Adjustment Payment is calculated, we’ll use the below trade details as an 
example of a DVP Repo Transaction.  
Example Trade Details 
Current Business Date  9/27/2021  
Trade Date  8/11/2021  
Repo Start Date  8/16/2021 
Repo End Date  10/4/2021  
Par Value 20,000,000.00  
Contract Repo Rate  0.13 
Start Money  20,500,000.00  
Final Money  20,503,627.36 
Transaction Type  Reverse Repo1 
System Price  100.422 
System Value  20,158,992.39  
System CoC  0.10 
Accrued Coupon Interest 74,592.39  
[[collateral]] Mark  -344,634.97  
Finance Mark  335.98  
Forward Mark Adjustment Payment -344,298.99  
 
1 The above calculations of the Forward Mark Adjustment Payment are displayed from the perspective of the Reverse Repo Party. 

---

## Page 5

DVP Repo Forward Mark Calculation Quick Reference Guide 
 
 
Breakdown of Calculation for DVP Repo Trade Example   
 
On Start Leg [[settlement]] Date, the Repo Party (Cash [[Borrower]]) delivers [[collateral]] in exchange for cash and the 
Reverse Repo Party (Cash Lender) receives [[collateral]] in exchange for cash.  
 
Using the Trade Details from the example on the previous page, $20,000,000.00 Par Value of a given [[CUSIP]] is  
loaned temporarily to the Repo Party at a contract value of $20,500,000.00. This is the amount of cash being 
borrowed.  
 
On End Leg [[settlement]] Date, the Repo Party (Cash [[Borrower]]) returns the borrowed cash along with the interest 
on the cash, based on an agreed upon rate. In this example the interest is calculated as:  
 
$20,500,000.00* 0.13/100/360 * 49 days = $3,627.36.  
 
The sum of the Contract Value of the Start Leg (Start Money) and the Repo Interest calculated based on the 
Start Money gives you Final Money (Contract Value of the End Leg). Using the same example above, the Final 
Money on the Repo is calculated as:  
 
$20,500,000.00 + $3,627.36 = $20,503,627.36 
 
Twice a day the value of the loaned [[collateral]] and the market repo rate change. These 2 aspects drive the 
valuation of the repo trade’s Current System Value (Repo Current System Value).  
 
The [[mark-to-market]] (MtM) on a repo trade is the difference between the Final Money and the Repo 
Current System Value.  
 
 
 
 
Note: 
This calculation is from the perspective of a Repo Party. The calculation is the opposite for the Reverse Party. 
 
Calculation of a Repo Current System Value:  
 
The Repo Current System Value is determined by the current value of the loaned [[collateral]] plus the repo 
interest that would be earned on the value of this [[collateral]] for the remainder of the repo term using the current 
System Repo Rate.  
 
Current market value of the [[collateral]] (System Value) is the (clean price) of the [[collateral]] plus accrued coupon 
interest to the next business date (only for end of day calculation/ next business day start of day FOS 
collection):  
 
System Value = Par * System Price/100 + Accrued Coupon Interest = $20,000,000.00 * 100.422/100 + 
$74,592.39 = $20,158,992.39  
 
The repo interest that would be earned on the current value of the [[collateral]] for the remainder of the term using 
the current market repo rate is labeled Finance Mark and it is calculated as follows:  
 
Finance Mark = Current value of the [[collateral]] * System Repo Rate* Remaining term of the original trade =  
 
= System Value * System Repo Rate/100 * ([[settlement]] Date – Business Date – 1)/360 =  
= $20,158,992.39 * 0.10/100 * 6 /360 = $335.98  
Repo MtM = Final Money – Repo Current System Value*  

---

## Page 6

DVP Repo Forward Mark Calculation Quick Reference Guide 
 
 
 
In [[GSD]]’s terminology repo [[mark-to-market]] is called Forward Mark.  
 
             
             
   
= $20,503,627.36 – ($20,158,992.39 + $335.98) = $344,298.99  
 
 
The calculations shown above are for a Repo dealer (Repo dealer is a cash [[Borrower]]). For a Reverse dealer the 
Forward Mark is -$344,298.99  
 
In the above table and in the customer facing reports Forward Mark is broken into 2 components: [[collateral]] 
Mark and Finance Mark.  
 
Finance Mark was already discussed.  
 
[[collateral]] Mark is a difference between the System Value (the current value of the [[collateral]]) and the  
Final Money:  
 
 
= $20,158,992.39 – $20,503,627.36 = -$344,634.97  
 
In summary: 
 
= -$344,634.97 + $335.98 = -$344,298.99   
Repo Current System Value = System Value + Finance Mark 
Forward Mark = Final Amount – Repo Current System Value 
[[collateral]] Mark = System Value – Final Money 
Forward Mark = [[collateral]] Mark + Finance Mark 

---

## Page 7

DVP Repo Forward Mark Calculation Quick Reference Guide 
 
 
 
 
 
 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 