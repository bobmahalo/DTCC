---
title: "DVP  Funds-Only Settlement (FOS) Scenario: Bilateral Term SDS DVP Repo"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd179_dvp_fos_scenario_for_bilateral_term_sds_dvp_repo_042022.pdf"
pages: 25
size: "1069.3 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# DVP  Funds-Only Settlement (FOS) Scenario: Bilateral Term SDS DVP Repo

**Original File:** [gsd179_dvp_fos_scenario_for_bilateral_term_sds_dvp_repo_042022.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd179_dvp_fos_scenario_for_bilateral_term_sds_dvp_repo_042022.pdf)  
**Category:** GSD  
**Total Pages:** 25  
**File Size:** 1069.3 KB  

---

## Page 1

DVP 
Funds-Only [[settlement]] 
(FOS) 
Fixed Income Clearing Corporation
Government [[securities]] Division
Scenario: Bilateral Term SDS DVP Repo
Matched before 12 PM EST

---

## Page 2

The DVP FOS Scenario for Bilateral Term SDS DVP Repo (hereinafter, the "document") is provided as a convenience to Members and is for information 
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

 DVP Funds-Only [[settlement]] is a daily cash pass-through process that generates Netting Members and Sponsored 
Members cash [[obligations]], calculated pursuant to Rule 13 of the [[FICC]] [[GSD]] Rulebook
 Cash [[obligations]] are an aggregate credit or debit Funds-Only [[settlement]] Amount across all active eligible trades
 Funds-Only [[settlement]] Amounts can either be a funds-only payment (net debit) to [[GSD]] or a funds-only payment (net 
credit) from [[GSD]]
 [[GSD]] assigns each security a System Value to calculate the cash [[settlement]] amount of a given net position. The System 
Value is determined daily to approximate each security’s current Market Value (mark to market (MtM)) 
 Funds-Only [[settlement]] Amounts reflect changes in the value of [[securities]] MtM, cash adjustments related to the [[settlement]] 
of [[securities]], pass-through of coupon payments for term repos or failed [[obligations]] that cross a coupon date, redemptions, 
invoice amounts and miscellaneous adjustments, as applicable
 Payment of Funds-Only [[settlement]] Amounts are executed over the Federal Reserve’s National [[settlement]] Service ([[NSS]]) 
with [[DTC]] acting as a [[settlement]] Agent for [[FICC]] [[GSD]]
 Members’ Funds-Only Settling Banks will acknowledge and settle their Funds-Only [[settlement]] Amounts with [[GSD]] on 
behalf of the Members 
 Funds-Only [[settlement]] Process occurs twice daily: 
 Start of Day cycle:
 Funds-Only Settling Banks must send their acknowledgement or refusal to settle by the 
Acknowledgement Cutoff Time pursuant to [[GSD]] Rules
 [[settlement]] of Start of Day Funds-Only [[settlement]] Amounts occurs by 10:00 AM ET** 
 Intraday cycle:
 Funds-Only Settling Banks must send their acknowledgement or refusal to settle by the 
Acknowledgement Cutoff time pursuant to [[GSD]] Rules 
 [[settlement]] of Intraday Funds-Only [[settlement]] occurs by 4:30 PM ET**
DVP Funds-Only [[settlement]] (FOS) Overview*
DVP FOS Scenario for Bilateral Term SDS DVP Repo
3
*  Does not apply to Sponsored GC Trades.
** Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.

---

## Page 4

A component of DVP FOS is the Forward Mark Adjustment Payment. The combined formula for the Forward Mark 
Adjustment Payment is:
Forward Mark Adjustment Payment = [[collateral]] Mark + Finance Mark
[[FICC]] limits exposure to its Members and itself by collecting a [[collateral]] Mark whenever the market price of a 
security goes up or down. Repo Transactions starting in the future [[DO]] not have any [[collateral]] exposure, so for Repo 
Transactions that haven’t started yet, the Forward Mark Adjustment Payment equals Finance Mark and is calculated 
using the below formula (given that [[collateral]] Mark is only calculated on Repo Transactions that have started):
Forward Mark Adjustment Payment = Finance Mark = Start Money + (Start Money * System Repo Rate * Term) / 360 - End Money
Repo Transactions that have started, have [[collateral]] exposure until the business day before the End Leg [[settlement]] 
Date, so for Repo Transactions that have started or start on the next day, the combined formula for calculating the  
Forward Mark Adjustment Payment is as follows:
Forward Mark Adjustment Payment = System Value + (System Value * System Repo Rate * Remaining Term) / 360 - End Money 
[[collateral]] Mark (for Repo Transactions) protects [[FICC]] and its Members from exposure due to variation in market 
price of [[collateral]]. For Repo Transactions, it is the difference between the end money (start money + (start money * 
Contract Repo Rate * Days in Term / 360) and the System Value (current Market Value as calculated by par * system 
price + accrued coupon interest to date) of the underlying instrument / [[collateral]]. For Repo Transactions, here is the 
calculation for [[collateral]] Mark:
[[collateral]] Mark = System Value – End Money
Overview of Forward Mark component as it pertains to DVP Repo Transactions
DVP FOS Scenario for Bilateral Term SDS DVP Repo
4

---

## Page 5

The [[collateral]] Mark is calculated on a per trade basis, then aggregated to determine a final credit or debit amount. 
The System Value used for Repo Transactions is calculated to the next business day. The following criteria is used to 
select Repo Transactions that are eligible for the [[collateral]] Mark calculation:
 The Start Leg [[settlement]] Date should have occurred or be equal to next business day (i.e., Start Leg should 
have settled or be net settled during the next available netting cycle).
 Repo Transactions cannot be in a Generic [[CUSIP]].
 For Repos that have already started, the End Leg [[settlement]] Date should be greater than next available 
[[settlement]] date and the underlying [[collateral]] should not be maturing on the next available [[settlement]] date.
[[FICC]] limits exposure to its Members and itself by collecting a Finance Mark whenever the repo rate of a security 
goes up or down. The Accrued Repo Interest to Date is also calculated as part of the Finance Mark.
Finance Mark is only calculated on Repo Transactions. It is the cost to finance the repo loan amount at current 
finance rates for the remaining term of the repo (for a forward starting repo transaction this would be the original 
term, i.e., the days between start-leg and end-leg [[settlement]] date).
The Finance Mark is calculated on a per trade basis, then aggregated to determine final credit or debit amount. 
Before the Repo Start Leg [[settlement]] Date, the cash [[Borrower]] pays the Finance Mark if the System Repo Rate falls 
below the original Contract Repo Rate on the Repo Transaction and [[FICC]] passes the same amount to the cash 
lender. Similarly, the cash lender pays the Finance Mark if the System Repo Rate rises above the original Contract 
Repo Rate on the Repo Transaction and [[FICC]] passes the same amount to the cash [[Borrower]]. 
Overview of Forward Mark component as it pertains to DVP Repo Transactions (Cont.)
DVP FOS Scenario for Bilateral Term SDS DVP Repo
5

---

## Page 6

Before the Start Leg [[settlement]] Date of a Forward Starting Repo Transaction (i.e., prior to Start Leg going into the 
net) the formula used to calculate Finance Mark is:
𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹 𝑀𝑀𝐹𝐹𝑀𝑀𝑀𝑀 = 𝑆𝑆𝑆𝑆𝐹𝐹𝑀𝑀𝑆𝑆 𝑚𝑚𝑚𝑚𝐹𝐹𝐹𝐹𝑚𝑚 + 𝑆𝑆𝑆𝑆𝐹𝐹𝑀𝑀𝑆𝑆 𝑀𝑀𝑚𝑚𝐹𝐹𝐹𝐹𝑚𝑚 ∗ 𝑆𝑆𝑚𝑚𝑆𝑆𝑆𝑆𝐹𝐹𝑚𝑚 𝑅𝑅𝐹𝐹𝑅𝑅𝑚𝑚 𝑅𝑅𝐹𝐹𝑆𝑆𝐹𝐹 ∗ 𝑇𝑇𝐹𝐹𝑀𝑀𝑚𝑚
360 − 𝐸𝐸𝐹𝐹𝐸𝐸 𝑀𝑀𝑚𝑚𝐹𝐹𝐹𝐹𝑚𝑚
After the Start Leg [[settlement]] Date for a Repo Transaction, the Dealers swap cash for [[collateral]]. Since the amount 
of cash that [[FICC]] would need to borrow or invest in the event of a [[Member]]’s insolvency is now the same as the 
Market Value of the [[collateral]], the System Value will be used to calculate the Finance Mark. After the Start Leg 
[[settlement]] Date, the cash lender pays the Finance Mark to the cash [[Borrower]] (if the System Repo Rate is positive). 
After the Start Leg [[settlement]] Date, the formula used to calculate Finance Mark is:
𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹 𝑀𝑀𝐹𝐹𝑀𝑀𝑀𝑀 = 𝑆𝑆𝑚𝑚𝑆𝑆𝑆𝑆𝐹𝐹𝑚𝑚 𝑉𝑉𝐹𝐹𝑉𝑉𝑉𝑉𝐹𝐹 ∗ 𝑆𝑆𝑚𝑚𝑆𝑆𝑆𝑆𝐹𝐹𝑚𝑚 𝑅𝑅𝐹𝐹𝑅𝑅𝑚𝑚 𝑅𝑅𝐹𝐹𝑆𝑆𝐹𝐹 ∗ 𝑅𝑅𝐹𝐹𝑚𝑚𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝐹𝑅𝑅 𝑇𝑇𝐹𝐹𝑀𝑀𝑚𝑚
360
The following criteria is used to select Repo Transactions that are eligible for the Finance Mark calculation:
 Repo Transactions must be active, compared and netting eligible
 For Forward Starting and already started repos, the End Leg [[settlement]] Date should be going into the net on a 
future date, beyond the current business day.
Any Forward Mark Adjustment Payment paid/collected during the intraday Funds-Only [[settlement]] cycle, will be 
returned the next business day along with any interest (Interest Adjustment Payment) calculated on the Forward 
Mark Adjustment Payment Return using a blended rate called the Overnight Investment Rate. The Interest 
Adjustment Payment is calculated as:
Interest Adjustment Payment = Forward Mark Adjustment Payment  Return * Number of days Forward Mark is invested / 360 * Overnight Investment Rate 
Overview of Forward Mark component as it pertains to DVP Repo Transactions (Cont.)
DVP FOS Scenario for Bilateral Term SDS DVP Repo
6

---

## Page 7

Transaction Details 
Par: 25,000,000 Contract Repo Rate: 0.12%
Start Money: 25,000,000.00 [[CUSIP]]: 912810SF6 - 3.000 TBOND 02/15/49 
Final Money: 25,000,166.67 Term: 2 Days 
Trade Date/Start Date: 09/22/2021 End Date: 09/24/2021
Comparison Timestamp: Before 12:00 PM System Repo Rate: 1.8034545%  
Accrued coupon interest: $77,445.65 System Price: 125.234
Based on this trade data you can expect the following to be calculated and then collected/paid through intraday FOS on 
Day 1:
 The System Value is: 25,000,000 * 125.234 / 100 + $77,445.65 = $31,385,945.65
 The [[collateral]] Mark for the trade is: $31,385,945.65 – $25,000,166.67 = $6,385,778.98
 The Finance Mark for the trade is: $31,385,945.65 * 1.8034545% * 2 / 360 = $3,144.62
 The total intraday mark to market (Forward Mark Adjustment Payment) is: $6,385,778.98 + $3,144.62 = 
$6,388,923.60
 [[obligations]] are generated upon comparison to settle the Same-Day Settling Start Leg. The [[obligations]] are 
unsettled as of the 12:00 PM snapshot.
 The Repo Side has an obligation to deliver (25,000,000) vs. $25,000,000.00 to [[FICC]]
 The Reverse Side has an obligation to receive 25,000,000 vs. ($25,000,00.00) from [[FICC]]
 The [[collateral]] Mark for the obligation is: $31,385,945.65 – $25,000,000.00 = $6,385,945.65
 There is no Finance Mark calculated on the obligation.
 The Net [[collateral]] Mark is: $6,385,778.98 - $6,385,945.65 = ($166.67). 
 The Net Finance Mark is: $3,144.62 - $0.00 = $3,144.62
 For the Repo Side, the Total Intraday FOS amount paid is: ($166.67) + $3,144.62 = $2,977.95
 For the Reverse Side, the Total Intraday FOS amount collected is: $166.67 + ($3,144.62) = ($2,977.95)
Bilateral Term SDS DVP Repo Transaction Details on Trade Date/Start Date
DVP FOS Scenario for Bilateral Term SDS DVP Repo
7

---

## Page 8

Repo Side Trade Details F ICC Intraday System Data Intraday MtM
Par 25,000,000 25,000,000
System Price N/A 125.2340000
Coupon Interest $77,445.65 $77,445.65
Start Money $25,000,000.00 $31,385,945.65
Contract Repo Rate / System Repo Rate 0.12% 1.8034545%
Accrued Repo Interest-to-Date $166.67 $3,144.62
End Money $25,000,166.67 $31,389,090.27 $6,388,923.60
Deliver Obligation Details F ICC Intraday System Data Intraday MtM
Par 25,000,000 25,000,000
System Price N/A 125.2340000
[[settlement]] Value $25,000,000.00 $31,385,945.65 $6,385,945.65
Forward Mark Adjustment Payment (Intraday MtM) $2,977.95
Intraday Total FOS $2,977.95
Intraday FOS Summary (Day 1)
DVP FOS Scenario for Bilateral Term SDS DVP Repo
8
As the cash lender/reverse side of the DVP Repo, the FOS components would be applied as follows:
As the cash [[Borrower]]/repo side of the DVP Repo, the FOS components would be applied as follows:
Repo Side Trade Details F ICC Intraday System Data Intraday MtM
Par 25,000,000 25,000,000
System Price N/A 125.2340000
Coupon Interest $77,445.65 $77,445.65
Start Money $25,000,000.00 $31,385,945.65
Contract Repo Rate / System Repo Rate 0.12% 1.8034545%
Accrued Repo Interest-to-Date $166.67 $3,144.62
End Money $25,000,166.67 $31,389,090.27 $6,388,923.60
Deliver Obligation Details F ICC Intraday System Data Intraday MtM
Par 25,000,000 25,000,000
System Price N/A 125.2340000
[[settlement]] Value $25,000,000.00 $31,385,945.65 $6,385,945.65
Forward Mark Adjustment Payment (Intraday MtM) $2,977.95
Intraday Total FOS $2,977.95
Reverse Side Trade Details F ICC Intraday System Data Intraday MtM
Par (25,000,000) (25,000,000)
System Price N/A 125.23400000
Coupon Interest ($77,445.65) ($77,445.65)
Start Money ($25,000,000.00) ($31,385,945.65)
Contract Repo Rate / System Repo Rate 0.12% 1.8034545%
Accrued Repo Interest-to-Date ($166.67) ($3,144.62)
End Money ($25,000,166.67) ($31,389,090.27) ($6,388,923.60)
Receive Obligation Details F ICC Intraday System Data Intraday MtM
Par (25,000,000) (25,000,000)
System Price N/A 125.23400000
[[settlement]] Value ($25,000,000.00) ($31,385,945.65) ($6,385,945.65)
Forward Mark Adjustment Payment (Intraday MtM) ($2,977.95)
Intraday Total FOS ($2,977.95)

---

## Page 9

Open Position Mark I (Intraday) Report displays the trade data as follows:
DVP FOS Scenario for Bilateral Term SDS DVP Repo
9
DVP Repo (Repo Side)
DVP Repo (Reverse Side)


---

## Page 10

Intraday Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
DVP FOS Scenario for Bilateral Term SDS DVP Repo
10
DVP Repo (Repo Side) DVP Repo (Reverse Side)
Note: The Intraday Funds-Only [[settlement]] is paid/collected by 4:30 PM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 11

Transaction Details 
Par: 25,000,000 Contract Repo Rate: 0.12%
Start Money: 25,000,000.00 [[CUSIP]]: 912810SF6 - 3.000 TBOND 02/15/49 
Final Money: 25,000,166.67 Term: 2 Days 
Trade Date/Start Date: 09/22/2021 End Date: 09/24/2021
Overnight Investment Rate: 0.4200% System Repo Rate: 1.8034545%  
Accrued coupon interest: $79,483.70 System Price: 125.234
Based on this trade data you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 2:
 The System Value is: 25,000,000 * 125.234 / 100 + $79,483.70 = $31,387,983.70
 The [[collateral]] Mark is: $31,387,983.70 – $25,000,166.67 = $6,387,817.03
 The Finance Mark is: $31,387,983.70 * 1.8034545% * 1 / 360 = $1,572.41
 The total start of day mark to market (Forward Mark Adjustment Payment) is: $6,387,817.03 + $1,572.41 = 
$6,389,389.44
 The Forward Mark Adjustment Payment Return is ($2,977.95)
 The Interest Adjustment Payment is: ($2,977.95) * 1 / 360 * 0.4200% = ($0.03)
 For the Repo Side, the Total Intraday FOS amount paid is: $6,389,389.44 + ($2,977.95) + ($0.03) = 
$6,386,411.46
 For the Reverse Side, the Total Intraday FOS amount collected is: ($6,389,389.44) + $2,977.95 + $0.03 = 
($6,386,411.46)
Bilateral Term SDS DVP Repo Transaction Details on Start Date + 1
DVP FOS Scenario for Bilateral Term SDS DVP Repo
11

---

## Page 12

Start of Day FOS Summary (Day 2)
DVP FOS Scenario for Bilateral Term SDS DVP Repo
12
As the cash lender/reverse side of the DVP Repo, the FOS components would be applied as follows:
As the cash [[Borrower]]/repo side of the DVP Repo, the FOS components would be applied as follows:
Repo Side  Trade Details [[FICC]] SOD System Data SOD  MtM
Par 25,000,000 25,000,000
System Price N/A 125.2340000
Coupon Interest $79,483.70 $79,483.70
Start Money $25,000,000.00 $31,387,983.70
Contract Repo Rate / System Repo Rate 0.12% 1.8034545%
Accrued Repo Interest-to-Date $166.67 $1,572.41
End Money $25,000,166.67 $31,389,556.11 $6,389,389.44
Forward Mark Adjustment Payment Return ($2,977.95)
Interest Adjustment Payment ($0.03)
Forward Mark Adjustment Payment (SOD MtM) $6,389,389.44 
SOD Total FOS $6,386,411.46
Repo Side - Start of Day Funds-Only [[settlement]] 
Reverse Side  Trade Details [[FICC]] SOD System Data SOD  MtM
Par (25,000,000) (25,000,000)
System Price N/A 125.23400000
Coupon Interest ($79,483.70) ($79,483.70)
Start Money ($25,000,000.00) ($31,387,983.70)
Contract Repo Rate / System Repo Rate 0.12% 1.8034545%
Accrued Repo Interest-to-Date ($166.67) ($1,572.41)
End Money ($25,000,166.67) ($31,389,556.11) ($6,389,389.44)
Forward Mark Adjustment Payment Return $2,977.95 
Interest Adjustment Payment $0.03 
Forward Mark Adjustment Payment (SOD MtM) ($6,389,389.44)
SOD Total FOS ($6,386,411.46)
Reverse Side - Start of Day Funds-Only [[settlement]] 

---

## Page 13

Open Position Mark E (End of Day) Report displays the trade data as follows:
DVP FOS Scenario for Bilateral Term SDS DVP Repo
13
DVP Repo (Repo Side)
DVP Repo (Reverse Side)
COL MARK FIN MARK TL MARK APPLIED MARK
-6,387,817.03 -1,572.41 -6,389,389.44 -6,389,389.44
COL MARK FIN MARK TL MARK APPLIED MARK
6,387,817.03 1,572.41 6,389,389.44 6,389,389.44

---

## Page 14

Start of Day Funds [[settlement]] Statement displays the funds [[settlement]] components as 
follows:
DVP FOS Scenario for Bilateral Term SDS DVP Repo
14
DVP Repo (Repo Side) DVP Repo (Reverse Side)
Note: The Start of Day Funds-Only [[settlement]] is paid/collected by 10:00 AM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 15

Transaction Details 
Par: 25,000,000 Contract Repo Rate: 0.12%
Start Money: 25,000,000.00 [[CUSIP]]: 912810SF6 - 3.000 TBOND 02/15/49 
Final Money: 25,000,166.67 Term: 2 Days 
Trade Date/Start Date: 09/22/2021 End Date: 09/24/2021
Overnight Investment Rate: N/A System Repo Rate: 1.8034545%  
Accrued coupon interest: $79,483.70 System Price: 125.234
Based on this trade data you can expect the following to be calculated and then collected/paid through intraday FOS on 
Day 2:
 The System Value is: 25,000,000 * 125.234 / 100 + $79,483.70 = $31,387,983.70
 The [[collateral]] Mark is: $31,387,983.70 – $25,000,166.67 = $6,387,817.03
 The Finance Mark is: $31,387,983.70 * 1.8034545% * 1 / 360  = $1,572.41
 The total intraday mark to market (Forward Mark Adjustment Payment) is: $6,387,817.03 + $1,572.41 = 
$6,389,389.44
 The Forward Mark Adjustment Payment Return is ($6,389,389.44)
 For the Repo Side, the Total Intraday FOS amount is: $6,389,389.44 + ($6,389,389.44) =  $0.00 
 For the Reverse Side, the Total Intraday FOS amount is: $ ($6,389,389.44) + $6,389,389.44 =  ($0.00)
Bilateral Term SDS DVP Repo Transaction Details on Start Date + 1
DVP FOS Scenario for Bilateral Term SDS DVP Repo
15

---

## Page 16

Intraday FOS Summary (Day 1)
DVP FOS Scenario for Bilateral Term SDS DVP Repo
16
As the cash lender/reverse side of the DVP Repo, the FOS components would be applied as follows:
As the cash [[Borrower]]/repo side of the DVP Repo, the FOS components would be applied as follows:
Repo Side  Trade Details F ICC Intraday System Data Intraday MtM
Par 25,000,000 25,000,000
System Price N/A 125.2340000
Coupon Interest $79,483.70 $79,483.70
Start Money $25,000,000.00 $31,387,983.70
Contract Repo Rate / System Repo Rate 0.12% 1.8034545%
Accrued Repo Interest-to-Date $166.67 $1,572.41
End Money $25,000,166.67 $31,389,556.11 $6,389,389.44
Forward Mark Adjustment Payment Return ($6,389,389.44)
Forward Mark Adjustment Payment (Intraday MtM) $6,389,389.44 
Intraday Total FOS $0.00
Repo Side - Intraday Funds-Only [[settlement]] 
Reverse Side Trade Details F ICC Intraday System Data Intraday MTM
Par (25,000,000) (25,000,000)
System Price N/A 125.23400000
Coupon Interest ($79,483.70) ($79,483.70)
Start Money ($25,000,000.00) ($31,387,983.70)
Contract Repo Rate / System Repo Rate 0.12% 1.8034545%
Accrued Repo Interest-to-Date ($166.67) ($1,572.41)
End Money ($25,000,166.67) ($31,389,556.11) ($6,389,389.44)
Forward Mark Adjustment Payment Return $6,389,389.44 
Forward Mark Adjustment Payment (Intraday MtM) ($6,389,389.44)
Intraday Total FOS $0.00
Reverse Side - Intraday F unds-Only [[settlement]] 

---

## Page 17

Open Position Mark I (Intraday) Report displays the trade data as follows:
DVP FOS Scenario for Bilateral Term SDS DVP Repo
17
DVP Repo (Repo Side)
DVP Repo (Reverse Side)


---

## Page 18

Intraday Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
DVP FOS Scenario for Bilateral Term SDS DVP Repo
18
DVP Repo (Repo Side) DVP Repo (Reverse Side)
Note: The Intraday Funds-Only [[settlement]] is paid/collected by 4:30 PM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 19

Transaction Details 
Par: 25,000,000 Contract Repo Rate: 0.12%
Start Money: 25,000,000.00 [[CUSIP]]: 912810SF6 - 3.000 TBOND 02/15/49 
Final Money: 25,000,166.67 Term: 2 Days 
Trade Date/Start Date: 09/22/2021 End Date: 09/24/2021
Overnight Investment Rate: 0.4200% System Repo Rate: N/A
Accrued coupon interest: $81,521.74 System Price: 125.137
Based on this trade data you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 3:
 The End Leg went into the net the prior night.
 The New System Value is: 25,000,000 * 125.137 / 100 + $81,521.74 = $31,365,771.74
 The Repo Side has an obligation to receive 25,000,000 vs. ($31,365,771.74) from [[FICC]]
 The Reverse Side has an obligation to deliver (25,000,000) vs. $31,365,771.74 to [[FICC]]
 The Transaction Adjustment Payment (TAP) is: $31,365,771.74 - $25,000,166.67 = $6,365,605.07 
 The Forward Mark Adjustment Payment Return is ($6,389,389.44)
 The Interest Adjustment Payment is: ($6,389,389.44) * 1 / 360 * 0.4200% = ($74.54)
 The Total Start of Day FOS is: $6,365,605.07 + (6,389,389.44) + ($74.54) = ($23,858.91)
 For the Repo Side, the Total Start of Day FOS amount collected is: $6,365,605.07 + ($6,389,389.44) + 
($74.54) = ($23,858.91)
 For the Reverse Side, the Total Start of Day FOS amount paid is: ($6,365,605.07) + $6,389,389.44 + $74.54  = 
$23,858.91 
Bilateral Term SDS DVP Repo Transaction Details on End Date
DVP FOS Scenario for Bilateral Term SDS DVP Repo
19

---

## Page 20

Start of Day FOS Summary (Day 2)
DVP FOS Scenario for Bilateral Term SDS DVP Repo
20
As the cash lender/reverse side of the DVP Repo, the FOS components would be applied as follows:
As the cash [[Borrower]]/repo side of the DVP Repo, the FOS components would be applied as follows:
Repo Side  Trade Details [[FICC]] SOD System Data SOD TAP
Par 25,000,000 25,000,000
System Price N/A 125.1370000
Coupon Interest $81,521.74 $81,521.74
Start Money $25,000,000.00 $31,365,771.74
Contract Repo Rate / System Repo Rate 0.12% N/A
Accrued Repo Interest-to-Date $166.67 N/A
End Money $25,000,166.67 $31,365,771.74 $6,365,605.07
Forward Mark Adjustment Payment Return ($6,389,389.44)
Interest Adjustment Payment ($74.54)
Transaction Adjustment Payment (TAP) $6,365,605.07
Start of Day Total FOS ($23,858.91)
Repo Side - Start of Day Funds-Only [[settlement]] 
Reverse Side Trade Details [[FICC]] SOD System Data SOD TAP
Par (25,000,000) (25,000,000)
System Price N/A 125.13700000
Coupon Interest ($81,521.74) ($81,521.74)
Start Money ($25,000,000.00) ($31,365,771.74)
Contract Repo Rate / System Repo Rate 0.12% N/A
Accrued Repo Interest-to-Date ($166.67) N/A
End Money ($25,000,166.67) ($31,365,771.74) ($6,365,605.07)
Forward Mark Adjustment Payment Return $6,389,389.44 
Interest Adjustment Payment $74.54 
Transaction Adjustment Payment (TAP) ($6,365,605.07)
Start of Day Total FOS $23,858.91 
Reverse  Side - Start of Day Funds-Only [[settlement]] 

---

## Page 21

Netted Summary Report displays the trade data as follows:
DVP FOS Scenario for Bilateral Term SDS DVP Repo
21
DVP Repo (Repo Side)
DVP Repo (Reverse Side)


---

## Page 22

SOD Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
DVP FOS Scenario for Bilateral Term SDS DVP Repo
22
DVP Repo (Repo Side) DVP Repo (Reverse Side)
Note: The Start of Day (SOD) Funds-Only [[settlement]] is paid/collected by 10:00 AM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 23

Flow of Funds Summary
DVP FOS Scenario for Bilateral Term SDS DVP Repo
23
Debit Credit Total
Start Leg: Funds to [[FICC]] ($25,000,000.00) $0.00 ($25,000,000.00)
End Leg: Funds to Reverse Dealer $0.00 $31,365,771.74 $31,365,771.74
Forward Mark Adjustment Payment (Intraday MtM) ($6,389,389.44) $0.00 ($6,389,389.44)
Forward Mark Adjustment Payment Return $0.00 $6,389,389.44 $6,389,389.44
Interest Adjustment Payment $0.00 $74.54 $74.54
Transaction Adjustment Payment (TAP) ($6,365,605.07) $0.00 ($6,365,605.07)
Net Total $241.21
Reverse Dealer cash flow  w ill sum up to the accrued repo interest on the trade plus the interest on the Forw ard Mark (Interest Adjustment Payment).
Repo interest to Reverse Dealer on trade: $166.67 and Interest Adjustment Payment to Reverse Repo Dealer: $74.54
$166.67 + $74.54 = $241.21
Reverse Dealer w ill deliver back original [[collateral]] to [[FICC]] at system value (25,000,000 vs. $31,365,771.74)
Reverse Side - Flow of Funds
Debit Credit Total
Start Leg: Funds to Repo Dealer $0.00 $25,000,000.00 $25,000,000.00
End Leg: Funds to [[FICC]] ($31,365,771.74) $0.00 ($31,365,771.74)
Forward Mark Adjustment Payment (Intraday MtM) $0.00 $6,389,389.44 $6,389,389.44
Forward Mark Adjustment Payment Return ($6,389,389.44) $0.00 ($6,389,389.44)
Interest Adjustment Payment ($74.54) $0.00 ($74.54)
Transaction Adjustment Payment (TAP) $0.00 $6,365,605.07 $6,365,605.07
Net Total ($241.21)
Repo Side - Flow of Funds
Repo Dealer cash flow  w ill sum up to the accrued repo interest on the trade plus the interest on the Forw ard Mark (Interest Adjustment P ayment).
Repo interest to Repo Dealer on trade: -$166.67 and Interest Adjustment P ayment to Repo Dealer: -$74.54
-$166.671 - $74.54 = -$241.21
Repo Dealer w ill receive back original [[collateral]] from [[FICC]] at system value (25,000,000 vs. $31,365,771.74)

---

## Page 24

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
24

---

## Page 25

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD179