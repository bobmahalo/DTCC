---
title: "DVP Funds-Only Settlement (FOS) Scenario: Bilateral Overnight SDS DVP Repo Matched before 12 PM EST"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd178_dvp_fos_scenario_for_bilateral_overnight_sds_dvp_repo_042022.pdf"
pages: 17
size: "738.9 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# DVP Funds-Only Settlement (FOS) Scenario: Bilateral Overnight SDS DVP Repo Matched before 12 PM EST

**Original File:** [gsd178_dvp_fos_scenario_for_bilateral_overnight_sds_dvp_repo_042022.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd178_dvp_fos_scenario_for_bilateral_overnight_sds_dvp_repo_042022.pdf)  
**Category:** GSD  
**Total Pages:** 17  
**File Size:** 738.9 KB  

---

## Page 1

DVP 
Funds-Only [[settlement]] 
(FOS) 
Fixed Income Clearing Corporation
Government [[securities]] Division
Scenario: Bilateral Overnight SDS DVP Repo
Matched before 12 PM EST

---

## Page 2

The DVP FOS Scenario for Bilateral Overnight SDS DVP Repo (hereinafter, the "document") is provided as a convenience to Members and is for 
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
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
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
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
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
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
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
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
6

---

## Page 7

Transaction Details 
Par: 50,000,000 Contract Repo Rate: 0.17%
Start Money: 50,000,000.00 [[CUSIP]]: 912828R69 - 1.625 TNOTE 05/31/23 
Final Money: 50,000,236.11 Term: Overnight - 1 Day 
Trade Date/Start Date: 09/22/2021 End Date: 09/23/2021
Comparison Timestamp: Before 12:00 PM System Repo Rate: 1.8034545% 
Accrued coupon interest: $253,073.77 System Price: 102.441000
Based on this trade data you can expect the following to be calculated and then collected/paid through intraday FOS on 
Day 1:
 The System Value is: 50,000,000 * 102.441000 / 100 + $253,073.77 = $51,473,573.77
 The [[collateral]] Mark for the trade is: $51,473,573.77 – $50,000,236.11 = $1,473,337.66
 The Finance Mark for the trade is: $51,473,573.77 * 1.8034545% * 1 / 360 = $2,578.62
 The total intraday mark to market (Forward Mark Adjustment Payment) is: $1,473,337.66 + $2,578.62 = 
$1,475,916.28
 [[obligations]] are generated upon comparison to settle the Same-Day Settling Start Leg. The [[obligations]] are 
unsettled as of the 12:00 PM snapshot.
 The Repo Side has an obligation to deliver (50,000,000) vs. $50,000,000.00 to [[FICC]]
 The Reverse Side has an obligation to receive 50,000,000 vs. ($50,000,00.00) from [[FICC]]
 The [[collateral]] Mark for the obligation is: $51,473,573.77 – $50,000,000.00 = $1,473,573.77
 There is no Finance Mark calculated on the obligation.
 The Net [[collateral]] Mark is: $1,473,337.66 - $1,473,573.77 = ($236.11). 
 The Net Finance Mark is: $2,578.62 - $0.00 = $2,578.62
 For the Repo Side, the Total Intraday FOS amount paid is: ($236.11) + $2,578.62 = $2,342.51
 For the Reverse Side, the Total Intraday FOS amount collected is: $236.11 + ($2,578.62) = ($2,342.51)
Bilateral Overnight SDS DVP Repo Transaction Details on Trade Date/Start Date
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
7

---

## Page 8

Intraday FOS Summary (Day 1)
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
8
As the cash lender/reverse side of the DVP Repo, the FOS components would be applied as follows:
As the cash [[Borrower]]/repo side of the DVP Repo, the FOS components would be applied as follows:
Repo Side Trade Details F ICC Intraday System Data Intraday MtM
Par 50,000,000 50,000,000
System Price N/A 102.4410000
Coupon Interest $253,073.77 $253,073.77
Start Money $50,000,000.00 $51,473,573.77
Contract Repo Rate / System Repo Rate 0.17% 1.8034545%
Accrued Repo Interest-to-Date $236.11 $2,578.62
End Money $50,000,236.11 $51,476,152.39 $1,475,916.28
Deliver Obligation Details F ICC Intraday System Data Intraday MtM
Par 50,000,000 50,000,000
System Price N/A 102.4410000
[[settlement]] Value $50,000,000.00 $51,473,573.77 $1,473,573.77
Forward Mark Adjustment Payment (Intraday MtM) $2,342.51
Intraday Total FOS $2,342.51
Reverse Side Trade Details F ICC Intraday System Data Intraday MtM
Par (50,000,000) (50,000,000)
System Price N/A 102.44100000
Coupon Interest ($253,073.77) ($253,073.77)
Start Money ($50,000,000.00) ($51,473,573.77)
Contract Repo Rate / System Repo Rate 0.17% 1.8034545%
Accrued Repo Interest-to-Date $236.11 ($2,578.62)
End Money ($50,000,236.11) ($51,476,152.39) ($1,475,916.28)
Receive Obligation Details F ICC Intraday System Data Intraday MtM
Par (50,000,000) (50,000,000)
System Price N/A 102.44100000
[[settlement]] Value ($50,000,000.00) ($51,473,573.77) ($1,473,573.77)
Forward Mark Adjustment Payment (Intraday MtM) ($2,342.51)
Intraday Total FOS ($2,342.51)

---

## Page 9

Open Position Mark I (Intraday) Report displays the trade data as follows:
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
9
DVP Repo (Repo Side)
DVP Repo (Reverse Side)


---

## Page 10

Intraday Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
10
DVP Repo (Repo Side) DVP Repo (Reverse Side)
Note: The Intraday Funds-Only [[settlement]] is paid/collected by 4:30 PM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 11

Transaction Details 
Par: 50,000,000 Contract Repo Rate: 0.17%
Start Money: 50,000,000.00 [[CUSIP]]: 912828R69 - 1.625 TNOTE 05/31/23 
Final Money: 50,000,236.11 Term: Overnight - 1 Day 
Trade Date/Start Date: 09/22/2021 End Date: 09/23/2021
Overnight Investment Rate: 0.4200% System Repo Rate: N/A
Accrued coupon interest: $255,293.72 System Price: 102.4410000
Based on this trade data you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 2:
 The End Leg went into the net the prior night.
 The New System Value is: 50,000,000 * 102.4410000 / 100 + $255,293.72 = $51,475,793.72
 The Repo Side has an obligation to receive 50,000,000 vs. ($51,475,793.72) from [[FICC]]
 The Reverse Side has an obligation to deliver (50,000,000) vs. $51,475,793.72 to [[FICC]]
 The Transaction Adjustment Payment (TAP) is: $51,475,793.72 - $50,000,236.11 = $1,475,557.61 
 The Forward Mark Adjustment Payment Return is ($2,342.51)
 The Interest Adjustment Payment is: ($2,342.51) * 1 / 360 * 0.4200% = ($0.03)
 The Total Start of Day FOS is: $1,475,557.61 + ($2,342.51) + ($0.03) = 1,473,215.07
 For the Repo Side, the Total Start of Day FOS amount collected is: $1,475,557.61 + ($2,342.51) + ($0.03) = 
$1,473,215.07
 For the Reverse Side, the Total Start of Day FOS amount paid is: ($1,475,557.61) + $2,342.51 + $0.03 = 
($1,473,215.07) 
Bilateral Overnight SDS DVP Repo Transaction Details on End Date
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
11

---

## Page 12

Start of Day FOS Summary (Day 2)
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
12
As the cash lender/reverse side of the DVP Repo, the FOS components would be applied as follows:
As the cash [[Borrower]]/repo side of the DVP Repo, the FOS components would be applied as follows:
Repo Side  Trade Details [[FICC]] SOD System Data SOD TAP
Par 50,000,000 50,000,000
System Price N/A 102.4410000
Coupon Interest $255,293.72 $255,293.72
Start Money $50,000,000.00 $51,475,793.72
Contract Repo Rate / System Repo Rate 0.17% N/A
Accrued Repo Interest-to-Date $236.11 N/A
End Money $50,000,236.11 $51,475,793.72 $1,475,557.61
Forward Mark Adjustment Payment Return ($2,342.51)
Interest Adjustment Payment ($0.03)
Transaction Adjustment Payment (TAP) $1,475,557.61
Start of Day Total FOS $1,473,215.07
Repo Side - Start of Day Funds-Only [[settlement]] 
Reverse Side Trade Details [[FICC]] SOD System Data SOD TAP
Par (50,000,000) (50,000,000)
System Price N/A 102.44100000
Coupon Interest ($255,293.72) ($255,293.72)
Start Money ($50,000,000.00) ($51,475,793.72)
Contract Repo Rate / System Repo Rate 0.17% N/A
Accrued Repo Interest-to-Date ($236.11) N/A
End Money ($50,000,236.11) ($51,475,793.72) ($1,475,557.61)
Forward Mark Adjustment Payment Return $2,342.51 
Interest Adjustment Payment $0.03 
Transaction Adjustment Payment (TAP) ($1,475,557.61)
Start of Day Total FOS ($1,473,215.07)
Reverse Side - Start of Day Funds-Only [[settlement]] 

---

## Page 13

Netted Summary Report displays the trade data as follows:
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
13
DVP Repo (Repo Side)
DVP Repo (Reverse Side)


---

## Page 14

SOD Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
14
DVP Repo (Repo Side) DVP Repo (Reverse Side)
Note: The Start of Day (SOD) Funds-Only [[settlement]] is paid/collected by 10:00 AM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 15

Flow of Funds Summary
DVP FOS Scenario for Bilateral Overnight SDS DVP Repo 
15
Debit Credit Total
Start Leg: Funds to Repo Dealer $0.00 $50,000,000.00 $50,000,000.00
End Leg: Funds to [[FICC]] ($51,475,793.72) $0.00 ($51,475,793.72)
Forward Mark Adjustment Payment (Intraday MtM) $0.00 $2,342.51 $2,342.51
Forward Mark Adjustment Payment Return ($2,342.51) $0.00 ($2,342.51)
Interest Adjustment Payment ($0.03) $0.00 ($0.03)
Transaction Adjustment Payment (TAP) $0.00 $1,475,557.61 $1,475,557.61
Net Total ($236.14)
Repo Side - Flow of Funds
Repo Dealer cash flow  w ill sum up to the accrued repo interest on the trade plus the interest on the Forw ard Mark (Interest Adjustment P ayment).
Repo interest to Repo Dealer on trade: -$236.11and Interest Adjustment P ayment to Repo Dealer: -$0.03
-$236.11 - $0.03 = -$236.14
Repo Dealer w ill receive back original [[collateral]] from [[FICC]] at system value (50,000,000 vs. $51,475,793.72)
Debit Credit Total
Start Leg: Funds to [[FICC]] ($50,000,000.00) $0.00 ($50,000,000.00)
End Leg: Funds to Reverse Dealer $0.00 $51,475,793.72 $51,475,793.72
Forward Mark Adjustment Payment (Intraday MtM) ($2,342.51) $0.00 ($2,342.51)
Forward Mark Adjustment Payment Return $0.00 $2,342.51 $2,342.51
Interest Adjustment Payment $0.00 $0.03 $0.03
Transaction Adjustment Payment (TAP) ($1,475,557.61) $0.00 ($1,475,557.61)
Net Total $236.14
Reverse Side - Flow of Funds 
Reverse Dealer cash flow  w ill sum up to the accrued repo interest on the trade plus the interest on the Forw ard Mark (Interest Adjustment P ayment).
Repo interest to Reverse Dealer on trade: $236.11 and Interest Adjustment P ayment to Reverse Repo Dealer: $0.03
$236.11 + $0.03 = $236.14
Reverse Dealer w ill deliver back original [[collateral]] to [[FICC]] at system value (50,000,000 vs. $51,475,793.72)

---

## Page 16

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
16

---

## Page 17

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD178