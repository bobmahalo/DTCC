---
title: "DVP  Funds-Only Settlement (FOS) Scenario: Forward Settling DVP Buy-Sell Matched after 12 PM EST"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd219_dvp_fos_scenario_for_fwd_settling_dvp_buy-sell_20240117.pdf"
pages: 22
size: "928.7 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# DVP  Funds-Only Settlement (FOS) Scenario: Forward Settling DVP Buy-Sell Matched after 12 PM EST

**Original File:** [gsd219_dvp_fos_scenario_for_fwd_settling_dvp_buy-sell_20240117.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd219_dvp_fos_scenario_for_fwd_settling_dvp_buy-sell_20240117.pdf)  
**Category:** GSD  
**Total Pages:** 22  
**File Size:** 928.7 KB  

---

## Page 1

DVP 
Funds-Only [[settlement]] 
(FOS) 
Fixed Income Clearing Corporation
Government [[securities]] Division
Scenario: Forward Settling DVP Buy-Sell
Matched after 12 PM EST

---

## Page 2

The DVP FOS Scenario for Forward Settling DVP Buy-Sell (hereinafter, the "document") is provided as a convenience to Members and is for information 
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

➢ DVP Funds-Only [[settlement]] is a daily cash pass-through process that generates Netting Members and Sponsored 
Members cash [[obligations]], calculated pursuant to Rule 13 of the [[FICC]] [[GSD]] Rulebook
➢ Cash [[obligations]] are an aggregate credit or debit Funds-Only [[settlement]] Amount across all active eligible trades
➢ Funds-Only [[settlement]] Amounts can either be a funds-only payment (net debit) to [[GSD]] or a funds-only payment (net 
credit) from [[GSD]]
➢ [[GSD]] assigns each security a System Value to calculate the cash [[settlement]] amount of a given net position. The System 
Value is determined daily to approximate each security’s current Market Value (mark to market (MtM)) 
➢ Funds-Only [[settlement]] Amounts reflect changes in the value of [[securities]] MtM, cash adjustments related to the [[settlement]] 
of [[securities]], pass-through of coupon payments for term repos or failed [[obligations]] that cross a coupon date, redemptions, 
invoice amounts and miscellaneous adjustments, as applicable
➢ Payment of Funds-Only [[settlement]] Amounts are executed over the Federal Reserve’s National [[settlement]] Service ([[NSS]]) 
with [[DTC]] acting as a [[settlement]] Agent for [[FICC]] [[GSD]]
➢ Members’ Funds-Only Settling Banks will acknowledge and settle their Funds-Only [[settlement]] Amounts with [[GSD]] on 
behalf of the Members 
➢ Funds-Only [[settlement]] Process occurs twice daily: 
➢ Start of Day cycle:
➢ Funds-Only Settling Banks must send their acknowledgement or refusal to settle by the 
Acknowledgement Cutoff Time pursuant to [[GSD]] Rules
➢ [[settlement]] of Start of Day Funds-Only [[settlement]] Amounts occurs by 10:00 AM ET** 
➢ Intraday cycle:
➢ Funds-Only Settling Banks must send their acknowledgement or refusal to settle by the 
Acknowledgement Cutoff time pursuant to [[GSD]] Rules 
➢ [[settlement]] of Intraday Funds-Only [[settlement]] occurs by 4:30 PM ET**
DVP Funds-Only [[settlement]] (FOS) Overview* 
DVP FOS Scenario for Forward Settling DVP Buy-Sell   
3
*  Does not apply to Sponsored GC Trades.
** Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.

---

## Page 4

A component of DVP FOS is the Forward Mark Adjustment Payment. The combined formula for the Forward Mark 
Adjustment Payment is:
Forward Mark Adjustment Payment = [[collateral]] Mark + Finance Mark
[[FICC]] limits exposure to its Members and itself by collecting a [[collateral]] Mark whenever the market price of a 
security goes up or down. For buy-sell transactions, the Forward Mark Adjustment Payment equals the [[collateral]] 
Mark and is calculated using the below formula (given that Finance Mark is only calculated on Repo Transactions 
that have started):
Forward Mark Adjustment Payment = [[collateral]] Mark
[[collateral]] Mark (for buy-sell transactions) protects [[FICC]] and its Members from exposure due to variation in market 
price of [[collateral]]. For buy-sell transactions, it is the difference between contract money (value at which trade was 
executed) and the System Value (current Market Value) of the underlying instrument / [[collateral]]. For buy-sell 
transactions, here is the calculation for [[collateral]] Mark:
[[collateral]] Mark = System Value – Contract Money
The [[collateral]] Mark is calculated on a per trade basis, then aggregated to determine a final credit or debit amount. 
The System Value used for buy-sell transactions is calculated to the contractual [[settlement]] date.
Overview of Forward Mark component as it pertains to buy-sell transactions
DVP FOS Scenario for Forward Settling DVP Buy-Sell  
4

---

## Page 5

The following criteria is used to select buy-sell transactions that are eligible for the [[collateral]] Mark calculation:
▪ Buy-sell transactions that have a [[settlement]] date greater than the next [[settlement]] date.
▪ Buy-sell transactions must be active, compared and netting eligible.
Any Forward Mark Adjustment Payment paid/collected during the intraday Funds-Only [[settlement]] cycle, will be 
returned the next business day along with any interest (Interest Adjustment Payment) calculated on the Forward 
Mark Adjustment Payment Return using a blended rate called the Overnight Investment Rate. The Interest 
Adjustment Payment is calculated as:
Interest Adjustment Payment = Forward Mark Adjustment Payment  Return * Number of days Forward Mark is invested / 360 * Overnight Investment Rate 
Overview of Forward Mark component as it pertains to buy-sell transactions (Cont.)
DVP FOS Scenario for Forward Settling DVP Buy-Sell
5

---

## Page 6

Transaction Details 
Par: 35,000,000 Contract Price: 99.00
Final Money: 34,854,008.15 [[CUSIP]]: 912828R36 - 1.625 TNOTE 05/15/26 
Trade Date: 09/22/2021 [[settlement]] Date: 09/24/2021
Comparison Timestamp: After 12:00 PM Forward Period: 2 Days 
Accrued coupon interest: $204,008.15 
Based on this trade data you can expect the following on Trade Date:
➢ [[FICC]] will not pay or collect intraday MtM as the trade was matched after 12:00 PM ET on Trade Date. 
➢ Funds-Only [[settlement]] will be calculated based on end of day ([[EOD]]) prices and paid/collected on the following 
business day as part of the Start of Day Funds [[settlement]] Cycle. 
Forward Settling DVP Buy-Sell Transaction Details on Trade Date
DVP FOS Scenario for Forward Settling DVP Buy-Sell
6

---

## Page 7

Transaction Details 
Par: 35,000,000 Contract Price: 99.00
Final Money: 34,854,008.15 [[CUSIP]]: 912828R36 - 1.625 TNOTE 05/15/26 
Trade Date: 09/22/2021 [[settlement]] Date: 09/24/2021
Accrued coupon interest: $204,008.15 Forward Period: 2 Days 
System Price: 103.848
Based on this trade data you can expect the following to be calculated and then collected/paid through 
Start of Day FOS on Day 2:
➢ The System Value is: 35,000,000 * 103.848 / 100 + $204,008.15 = $36,550,808.15
➢ The [[collateral]] Mark for the trade is: $36,550,808.15 – $34,854,008.15 = $1,696,800.00
➢ The total Start of Day mark to market (Forward Mark Adjustment Payment) is $1,696,800.00 
➢ For the [[Buyer]], the Total Start of Day FOS amount collected is: $36,550,808.15 + ($34,854,008.15) = $1,696,800.00
➢ For the [[Seller]], the Total Start of Day FOS amount paid is: ($36,550,808.15) + $34,854,008.15 = ($1,696,800.00)
Forward Settling DVP Buy-Sell Transaction Details on Trade Date + 1
DVP FOS Scenario for Forward Settling DVP Buy-Sell   
7

---

## Page 8

Start of Day FOS Summary (Day 2)
DVP FOS Scenario for Forward Settling DVP Buy-Sell
8
As the [[Seller]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
As the [[Buyer]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
Buy Side Trade Details [[FICC]] SOD System Data SOD  MTM
Par 35,000,000 35,000,000
System Price 99.0000000 103.8480000
Coupon Interest $204,008.15 $204,008.15
Forward Period 2 2
End Money $34,854,008.15 $36,550,808.15 $1,696,800.00
Start of Day Total FOS $1,696,800.00
Sell Side Trade Details [[FICC]] SOD System Data SOD  MTM
Par (35,000,000) (35,000,000)
System Price 99.0000000 103.84800000
Coupon Interest ($204,008.15) ($204,008.15)
Forward Period 2 2
End Money ($34,854,008.15) ($36,550,808.15) ($1,696,800.00)
Start of Day Total FOS ($1,696,800.00)

---

## Page 9

Forward Mark Report displays the trade data as follows:
DVP FOS Scenario for Forward Settling DVP Buy-Sell
9
DVP Buy-Sell Trade (Buy Side)
DVP Buy-Sell Trade (Sell Side)


---

## Page 10

Open Position Mark E (End of Day) Report displays the trade data as follows:
DVP FOS Scenario for Forward Settling DVP Buy-Sell
10
DVP Buy-Sell Trade (Buy Side)
DVP Buy-Sell Trade (Sell Side)


---

## Page 11

Start of Day Funds [[settlement]] Statement displays the funds [[settlement]] components as 
follows:
DVP FOS Scenario for Forward Settling DVP Buy-Sell
11
DVP Buy-Sell Trade (Buy Side) DVP Buy-Sell Trade (Sell Side)
Note: The Start of Day (SOD) Funds-Only [[settlement]] is paid/collected by 10:00 AM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 12

Transaction Details 
Par: 35,000,000 Contract Price: 99.00
Final Money: 34,854,008.15 [[CUSIP]]: 912828R36 - 1.625 TNOTE 05/15/26 
Trade Date: 09/22/2021 [[settlement]] Date: 09/24/2021
Accrued coupon interest: $204,008.15 Forward Period: 2 Days 
System Price: 103.848 
Based on this trade data you can expect the following to be calculated and then collected/paid through intraday 
FOS on Day 2:
➢ The System Value is: 35,000,000 * 103.848000 / 100 + $204,008.15 = $36,550,808.15
➢ The [[collateral]] Mark for the trade is: $36,550,808.15 – $34,854,008.15 = $1,696,800.00
➢ The total intraday mark to market (Forward Mark Adjustment Payment) is $1,696,800.00 
➢ The Forward Mark Adjustment Payment Return is ($1,696,800.00)
➢ For the [[Buyer]], the Total Intraday FOS amount is: $1,696,800.00 + ($1,696,800.00) = $0.00
➢ For the [[Seller]], the Total Intraday FOS amount is: ($1,696,800.00) + $1,696,800.00 = ($0.00)
Forward Settling DVP Buy-Sell Transaction Details on Trade Date + 1
DVP FOS Scenario for Forward Settling DVP Buy-Sell
12

---

## Page 13

Intraday FOS Summary (Day 2)
DVP FOS Scenario for Forward Settling DVP Buy-Sell
13
As the [[Seller]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
As the [[Buyer]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
Buy Side   Trade Details [[FICC]] Intraday System Data Intraday  MTM
Par 35,000,000 35,000,000
System Price 99.0000000 103.8480000
Coupon Interest $204,008.15 $204,008.15
Forward Period 2 2
End Money $34,854,008.15 $36,550,808.15 $1,696,800.00
Forward Mark Adjustment Payment Return ($1,696,800.00)
Forward Mark Adjustment Payment (Intraday MtM) $1,696,800.00
Intraday Total FOS $0.00
Buy Side - Intraday Funds-Only [[settlement]] 
Sell Side Trade Details [[FICC]] Intraday System Data Intraday  MTM
Par (35,000,000) (35,000,000)
System Price 99.0000000 103.84800000
Coupon Interest ($204,008.15) ($204,008.15)
Forward Period 2 2
End Money ($34,854,008.15) ($36,550,808.15) ($1,696,800.00)
Forward Mark Adjustment Payment Return $1,696,800.00
Forward Mark Adjustment Payment (Intraday MtM) ($1,696,800.00)
Intraday Total FOS $0.00
Sell Side - Intraday Funds-Only [[settlement]] 

---

## Page 14

Open Position Mark I (Intraday) Report displays the trade data as follows:
DVP FOS Scenario for Forward Settling DVP Buy-Sell
14
DVP Buy-Sell Trade (Buy Side)
DVP Buy-Sell Trade (Sell Side)


---

## Page 15

Intraday Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
DVP FOS Scenario for Forward Settling DVP Buy-Sell
15
DVP Buy-Sell Trade (Buy Side) DVP Buy-Sell Trade (Sell Side)
Note: The Intraday Funds-Only [[settlement]] is paid/collected by 4:30 PM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules f or the current timeframes.


---

## Page 16

Transaction Details 
Par: 35,000,000 Contract Price: 99.00
Final Money: 34,854,008.15 [[CUSIP]]: 912828R36 - 1.625 TNOTE 05/15/26 
Trade Date: 09/22/2021 [[settlement]] Date: 09/24/2021
Overnight Investment Rate: 0.4200% Forward Period: 2 Days 
Accrued coupon interest: $204,008.15 System Price: 103.617
Based on this trade data you can expect the following to be calculated and then collected/paid through Start of Day 
on Day 3:
➢ The Buy-Sell Transactions went into the net the prior night.
➢ The New System Value is: 35,000,000 * 103.617 / 100 + $204,008.15 = $36,469,958.15
➢ The [[Buyer]] has an obligation to receive 35,000,000 vs. ($36,469,958.15) from [[FICC]]
➢ The [[Seller]] has an obligation to deliver (35,000,000) vs. $36,469,958.15 to [[FICC]]
➢ The Transaction Adjustment Payment (TAP) is: $36,469,958.15 - $34,854,008.15 = $1,615,950.00 
➢ The Forward Mark Adjustment Payment Return is ($1,696,800.00)
➢ The Interest Adjustment Payment is: ($1,696,800.00) * 1 / 360 * 0.4200% = ($19.80)
➢ The Total Start of Day FOS is: $1,615,950.00 + ($1,696,800.00) + ($19.80) = ($80,869.80) 
➢ For the [[Buyer]], the Total Start of Day FOS amount collected is: $1,615,950.00 + ($1,696,800.00) + ($19.80) = 
($80,869.80) 
➢ For the [[Seller]], the Total Start of Day FOS amount paid is: ($1,615,950.00) + $1,696,800.00 + $19.80 = 
$80,869.80 
Forward Settling DVP Buy-Sell Transaction Details on [[settlement]] Date
DVP FOS Scenario for Forward Settling DVP Buy-Sell
16

---

## Page 17

Start of Day FOS Summary (Day 2)
DVP FOS Scenario for Forward Settling DVP Buy-Sell
17
As the [[Seller]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
As the [[Buyer]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
Buy Side  Trade Details [[FICC]] SOD System Data SOD TAP
Par 35,000,000 35,000,000
System Price 99.0000000 103.6170000
Coupon Interest $204,008.15 $204,008.15
Forward Period 2 2
End Money $34,854,008.15 $36,469,958.15 $1,615,950.00
Forward Mark Adjustment Payment Return ($1,696,800.00)
Interest Adjustment Payment ($19.80)
Transaction Adjustment Payment (TAP) $1,615,950.00
Start of Day Total FOS ($80,869.80)
Buy Side - Start of Day Funds-Only [[settlement]] 
Sell Side  Trade Details [[FICC]] SOD System Data SOD TAP
Par (35,000,000) (50,000,000)
System Price 99.0000000 103.61700000
Coupon Interest ($204,008.15) ($204,008.15)
Forward Period 2 2
End Money ($34,854,008.15) ($36,469,958.15) ($1,615,950.00)
Forward Mark Adjustment Payment Return $1,696,800.00 
Interest Adjustment Payment $19.80 
Transaction Adjustment Payment (TAP) ($1,615,950.00)
Start of Day Total FOS $80,869.80 
Sell Side - Start of Day Funds-Only [[settlement]] 

---

## Page 18

Netted Summary Report displays the trade data as follows:
DVP FOS Scenario for Forward Settling DVP Buy-Sell
18
DVP Buy-Sell Trade (Buy Side)
DVP Buy-Sell Trade (Sell Side)


---

## Page 19

SOD Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
DVP FOS Scenario for Forward Settling DVP Buy-Sell
19
DVP Buy-Sell Trade (Buy Side) DVP Buy-Sell Trade (Sell Side)
Note: The Start of Day (SOD) Funds-Only [[settlement]] is paid/collected by 10:00 AM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 20

Flow of Funds Summary
DVP FOS Scenario for Forward Settling DVP Buy-Sell
20
As the [[Seller]] of the DVP Buy-Sell Trade, the day over day FOS calculations would be:
As the [[Buyer]] of the DVP Buy-Sell Trade, the day over day FOS calculations would be:
Debit Credit Total
Funds from [[Buyer]] $0.00 $34,854,008.15 $34,854,008.15
Funds to [[FICC]] ($36,469,958.15) $0.00 ($36,469,958.15)
Forward Mark Adjustment Payment (Intraday MtM) $0.00 $1,696,800.00 $1,696,800.00
Forward Mark Adjustment Payment Return ($1,696,800.00) $0.00 ($1,696,800.00)
Interest Adjustment Payment ($19.80) $0.00 ($19.80)
Transaction Adjustment Payment (TAP) $0.00 $1,615,950.00 $1,615,950.00
Net Total ($19.80)
Buy Side - Flow of Funds
[[Buyer]]'s cash flow  w ill sum up to the interest on the Forw ard Mark Adjustment Payment.
Interest Adjustment Payment to [[Buyer]]: -$19.80
[[Buyer]] w ill receive [[collateral]] from [[FICC]] at system value (35,000,000 vs. $36,469,958.15)
Debit Credit Total
Funds to [[Seller]] ($34,854,008.15) $0.00 ($34,854,008.15)
Funds from [[FICC]] $0.00 $36,469,958.15 $36,469,958.15
Forwarrd Mark Adjustment Payment (Intraday MtM) ($1,696,800.00) $0.00 ($1,696,800.00)
Forward Mark Adjustment Payment Return $0.00 $1,696,800.00 $1,696,800.00
Interest Adjustment Payment $0.00 $19.80 $19.80
Transaction Adjustment Payment (TAP) ($1,615,950.00) $0.00 ($1,615,950.00)
Net Total $19.80
[[Seller]]'s cash flow  w ill sum up to the interest on the Forw ard Mark Adjustment Payment.
Interest Adjustment Payment to [[Seller]]: $0.32
[[Seller]] w ill deliver [[collateral]] to [[FICC]] at system value (35,000,000 vs. $36,469,958.15)
Sell Side - Flow of Funds

---

## Page 21

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
21

---

## Page 22

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD219