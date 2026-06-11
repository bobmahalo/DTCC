---
title: "DVP Funds-Only Settlement (FOS) Scenario: Next Day Settling DVP Buy-Sell Matched before 12 PM EST"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd177_dvp_fos_scenario_for_next_day_settling_dvp_buy-sell_042022.pdf"
pages: 16
size: "691.5 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# DVP Funds-Only Settlement (FOS) Scenario: Next Day Settling DVP Buy-Sell Matched before 12 PM EST

**Original File:** [gsd177_dvp_fos_scenario_for_next_day_settling_dvp_buy-sell_042022.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd177_dvp_fos_scenario_for_next_day_settling_dvp_buy-sell_042022.pdf)  
**Category:** GSD  
**Total Pages:** 16  
**File Size:** 691.5 KB  

---

## Page 1

DVP 
Funds-Only [[settlement]] 
(FOS) 
Fixed Income Clearing Corporation
Government [[securities]] Division
Scenario: Next Day Settling DVP Buy-Sell  
Matched before 12 PM EST

---

## Page 2

The DVP FOS Scenario for Next Day Settling DVP Buy-Sell (hereinafter, the "document") is provided as a convenience to Members and is for information 
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
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
3
* Does not apply to Sponsored GC Trades.
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
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
4

---

## Page 5

The following criteria is used to select buy-sell transactions that are eligible for the [[collateral]] Mark calculation:
 Buy-sell transactions that have a [[settlement]] date greater than the next [[settlement]] date.
 Buy-sell transactions must be active, compared and netting eligible.
Any Forward Mark Adjustment Payment paid/collected during the intraday Funds-Only [[settlement]] cycle, will be 
returned the next business day along with any interest (Interest Adjustment Payment) calculated on the Forward 
Mark Adjustment Payment Return using a blended rate called the Overnight Investment Rate. The Interest 
Adjustment Payment is calculated as:
Interest Adjustment Payment = Forward Mark Adjustment Payment  Return * Number of days Forward Mark is invested / 360 * Overnight Investment Rate 
Overview of Forward Mark component as it pertains to buy-sell transactions (Cont.)
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
5

---

## Page 6

Transaction Details
Par: 50,000,000 Contract Price: 100.2890625
Final Money: 50,245,584.24 [[CUSIP]]: 91282CCJ8 - 0.875 TNOTE 06/30/26 
Trade Date: 09/22/2021 [[settlement]] Date: 09/23/2021
Comparison Timestamp: Before 12:00 PM Forward Period: 1 Day 
Accrued coupon interest: $101,052.99 System Price: 100.344000
Based on this trade data you can expect the following to be calculated and then collected/paid through intraday FOS on 
Day 1:
 The System Value is: 50,000,000 * 100.344000 / 100 + $101,052.99 = $50,273,052.99
 The [[collateral]] Mark for the trade is: $50,273,052.99 – $50,245,584.24 = $27,468.75
 The total intraday mark to market (Forward Mark Adjustment Payment) is = $27,468.75 
 For the [[Buyer]], the Total Intraday FOS amount collected is: $50,273,052.99 + ($50,245,584.24) = $27,468.75
 For the [[Seller]], the Total Intraday FOS amount paid is: ($50,273,052.99) + $50,245,584.24 = ($27,468.75)
Next Day Settling DVP Buy-Sell Transaction Details on Trade Date
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
6

---

## Page 7

Intraday FOS Summary (Day 1)
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
7
As the [[Seller]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
As the [[Buyer]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
Buy Side Trade Details F ICC Intraday System Data Intraday MTM
Par 50,000,000 50,000,000
System Price 100.2890625 100.3440000
Coupon Interest $101,052.99 $101,052.99
Forward Period 1 1
End Money $50,245,584.24 $50,273,052.99 $27,468.75
Intraday Total FOS $27,468.75
Sell Side Trade Details F ICC Intraday System Data Intraday MTM
Par (50,000,000) (50,000,000)
System Price 100.2890625 100.34400000
Coupon Interest ($101,052.99) ($101,052.99)
Forward Period 1 1
End Money ($50,245,584.24) ($50,273,052.99) ($27,468.75)
Intraday Total FOS ($27,468.75)

---

## Page 8

Open Position Mark I (Intraday) Report displays the trade data as follows:
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
8
DVP Buy-Sell Trade (Buy Side)
DVP Buy-Sell Trade (Sell Side)


---

## Page 9

Intraday Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
9
DVP Buy-Sell Trade (Buy Side) DVP Buy-Sell Trade (Sell Side)
Note: The Intraday Funds-Only [[settlement]] is paid/collected by 4:30 PM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 10

Transaction Details 
Par: 50,000,000 Contract Price: 100.2890625
Final Money: 50,245,584.24 [[CUSIP]]: 91282CCJ8 - 0.875 TNOTE 06/30/26 
Trade Date: 09/22/2021 [[settlement]] Date: 09/23/2021
Overnight Investment Rate: 0.4200% Forward Period: 1 Day 
Accrued coupon interest: $101,052.99 System Price: 100.344000
Based on this trade data you can expect the following to be calculated and then collected/paid through Start of Day 
FOS on Day 2:
 The Buy-Sell Transactions went into the net the prior night.
 The New System Value is: 50,000,000 * 100.344000 / 100 + $101,052.99 = $50,273,052.99
 The [[Buyer]] has an obligation to receive 50,000,000 vs. ($50,273,052.99) from [[FICC]]
 The [[Seller]] has an obligation to deliver (50,000,000) vs. $50,273,052.99 to [[FICC]]
 The Transaction Adjustment Payment (TAP) is: $50,273,052.99 - $50,245,584.24 = $27,468.75 
 The Forward Mark Adjustment Payment Return is ($27,468.75)
 The Interest Adjustment Payment is: ($27,468.75) * 1 / 360 * 0.4200% = ($0.32)
 The Total Start of Day FOS is: $27,468.75 + ($27,468.75) + ($0.32) = ($0.32) 
 For the [[Buyer]], the Total Start of Day FOS amount collected is: $27,468.75 + ($27,468.75) + ($0.32) = ($0.32) 
 For the [[Seller]], the Total Start of Day FOS amount paid is: ($27,468.75) + $27,468.75 + $0.32 = $0.32 
Next Day Settling DVP Buy-Sell Transaction Details on [[settlement]] Date
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
10

---

## Page 11

Start of Day FOS Summary (Day 2)
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
11
As the [[Seller]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
As the [[Buyer]] of the DVP Buy-Sell Trade, the FOS components would be applied as follows:
Buy Side  Trade Details [[FICC]] SOD System Data SOD TAP
Par 50,000,000 50,000,000
System Price 100.2890625 100.3440000
Coupon Interest $101,052.99 $101,052.99
Forward Period 1 1
End Money $50,245,584.24 $50,273,052.99 $27,468.75
Forward Mark Adjustment Payment Return ($27,468.75)
Interest Adjustment Payment ($0.32)
Transaction Adjustment Payment (TAP) $27,468.75
Start of Day Total FOS ($0.32)
Buy Side - Start of Day Funds-Only [[settlement]] 
Sell Side   Trade Details [[FICC]] SOD System Data SOD TAP
Par (50,000,000) (50,000,000)
System Price 100.2890625 100.34400000
Coupon Interest ($101,052.99) ($101,052.99)
Forward Period 1 1
End Money ($50,245,584.24) ($50,273,052.99) ($27,468.75)
Forward Mark Adjustment Payment Return $27,468.75 
Interest Adjustment Payment $0.32 
Transaction Adjustment Payment (TAP) ($27,468.75)
Start of Day Total FOS $0.32 
Sell Side - Start of Day Funds-Only [[settlement]] 

---

## Page 12

Netted Summary Report displays the trade data as follows:
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
12
DVP Buy-Sell Trade (Buy Side)
DVP Buy-Sell Trade (Sell Side)


---

## Page 13

SOD Funds [[settlement]] Statement displays the funds [[settlement]] components as follows:
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
13
DVP Buy-Sell Trade (Buy Side) DVP Buy-Sell Trade (Sell Side)
Note: The Start of Day (SOD) Funds-Only [[settlement]] is paid/collected by 10:00 AM ET. Refer to the Schedule of Timeframes within the [[GSD]] Rules for the current timeframes.


---

## Page 14

Flow of Funds Summary
DVP FOS Scenario for Next Day Settling DVP Buy-Sell 
14
As the [[Seller]] of the DVP Buy-Sell Trade, the day over day FOS calculations would be:
As the [[Buyer]] of the DVP Buy-Sell Trade, the day over day FOS calculations would be:
Debit Credit Total
Funds from [[Buyer]] $0.00 $50,245,584.24 $50,245,584.24
Funds to [[FICC]] ($50,273,052.99) $0.00 ($50,273,052.99)
Forward Mark Adjustment Payment (Intraday MtM) $0.00 $27,468.75 $27,468.75
Forward Mark Adjustment Payment Return ($27,468.75) $0.00 ($27,468.75)
Interest Adjustment Payment ($0.32) $0.00 ($0.32)
Transaction Adjustment Payment (TAP) $0.00 $27,468.75 $27,468.75
Net Total ($0.32)
[[Buyer]]'s cash flow  w ill sum up to the interest on the Forw ard Mark Adjustment Payment.
Interest Adjustment Payment to [[Buyer]]: -$0.32
[[Buyer]] w ill receive [[collateral]] from [[FICC]] at system value (50,000,000 vs. $50,273,052.99)
Buy Side - Flow of Funds
Debit Credit Total
Funds to [[Seller]] ($50,245,584.24) $0.00 ($50,245,584.24)
Funds from [[FICC]] $0.00 $50,273,052.99 $50,273,052.99
Forward Mark Adjustment Payment (Intraday MtM) ($27,468.75) $0.00 ($27,468.75)
Forward Mark Adjustment Payment Return $0.00 $27,468.75 $27,468.75
Interest Adjustment Payment $0.00 $0.32 $0.32
Transaction Adjustment Payment (TAP) ($27,468.75) $0.00 ($27,468.75)
Net Total $0.32
Sell Side - Flow of Funds
[[Seller]]'s cash flow  w ill sum up to the interest on the Forw ard Mark Adjustment P ayment.
Interest Adjustment P ayment to [[Seller]]: $0.32
[[Seller]] w ill deliver [[collateral]] to [[FICC]] at system value (50,000,000 vs. $50,273,052.99)

---

## Page 15

To access additional self-paced learning, 
how-to videos, guides and other 
documentation, visit:
www.dtcclearning.com
For all support services
www.[[DTCC]].com/client-center
15

---

## Page 16

© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: GSD177