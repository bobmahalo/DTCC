---
title: "NSCC Primary Market Create/Redeem Functional Requirements"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf228a_T1-CBRD_2024Jan26.pdf"
pages: 14
size: "481.4 KB"
category: "ETF"
ingested_on: "2026-06-05"
---

# NSCC Primary Market Create/Redeem Functional Requirements

**Original File:** [etf228a_T1-CBRD_2024Jan26.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/etf228a_T1-CBRD_2024Jan26.pdf)  
**Category:** ETF  
**Total Pages:** 14  
**File Size:** 481.4 KB  

---

## Page 1

 
 
ACCELERATED [[settlement]] (T+1) 
[[NSCC]] [[primary market]] CREATE/REDEEM 
FUNCTIONAL REQUIREMENTS 
JANUARY 26, 2023 
 

---

## Page 2

 
 
TABLE OF CONTENTS 
 
Introduction .......................................................................................................................................................... 3 
Functional Requirements: Near Real-Time Create/Redeem Processing........................................................ 4 
Primary Cycle Cutoff T+1 .................................................................................................................................... 4 
[[ETF]] Reporting Through Universal Trade Capture (UTC) Output ....................................................................... 4 
Critical Data Elements From [[ETF]] Instruction Detail Blotter................................................................................ 5 
FIX Output Fields ........................................................................................................................................... 6 
UTC Fix Output .............................................................................................................................................. 8 
Print Image Instruction Detail Blotter ............................................................................................................. 9 
Additional [[collateral]] Related Fields .................................................................................................................. 10 
Print Version Instruction Detail Blotter .............................................................................................................. 11 
Machine Readable Output (MRO) AutoRoute File (Production 02081673/PSE/U 02981673) ........................ 11 
UTC Output Requirements ............................................................................................................................... 12 
Subscriptions ................................................................................................................................................... 12 
Create and Redeem Secondary Cycle ............................................................................................................ 12 
[[settlement]] Date Assignment Rules ................................................................................................................ 12 
Updated Formats and Resource Links ............................................................................................................ 13 
 

---

## Page 3

Functional Requirements 
Introduction 3 
INTRODUCTION 
The financial services industry, in coordination with its regulators, is planning to shorten the [[settlement]] cycle for 
equities, corporate [[Bonds]], municipal [[Bonds]], unit investment trusts, and financial instruments comprised of 
these security types (for example: ADRs, ETFs), from the current cycle of trade date plus two business days 
(T+2) to trade date plus one business day (T+1). Although the T+1 transition date remains an open issue as of 
the time this document was written, the document assumes a September 3, 2024, transition date to a T+1 
[[settlement]] cycle. The T+1 transition date is subject to final regulatory approval. Assuming the above date is 
agreed upon, the first T+1 trade date will be Tuesday, September 3, 2024. 
A copy of this document can be obtained from [[DTCC]] at https://www.[[DTCC]].com and from the industry’s T +1 site 
at https://www.[[DTCC]].com/ust1/documentation. For more resources, see Updated Formats and Resource Links. 
Based on the considerations published in the initial white paper to the Industry in December 2021 [[NSCC]] will 
develop near real-time reporting for the [[primary market]] Create/Redeem service with near real-time output 
through Universal Trade Capture (UTC). 
Below are the original considerations / recommendations published in the T1 white paper: 
• Development of a near real-time create/redeem process after 7 P.M. in [[NSCC]]’s [[primary market]] service. 
• Distribution of Trade Capture messaging through UTC in near real-time for Create/Redeem trade. 
• Distribution of [[ETF]] Instruction Detail Blotter with [[settlement]] details prior to current 9 P.M. cycle. 
 
Processing Create and Redeem orders near real-time and providing near real-time UTC output earlier than the 
current batch process (8:00 P.M. Create/Redeem and 9:00 P.M. output) will allow ample time for [[ETF]] Agents 
and/or Authorized Participants (APs) to submit [[CNS]] exemptions. Based on the near real-time processing start 
and end times it will also provide a wider window for Create/Redeem orders to make the [[CNS]] night cycle and 
the primary CTS cycle. 

---

## Page 4

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 4 
FUNCTIONAL REQUIREMENTS: NEAR REAL-TIME 
CREATE/REDEEM PROCESSING 
Primary Cycle Cutoff T+1 
The current primary cycle cutoff of 8:00 P.M. Eastern Time (ET) will be expanded until 8:45 P.M. ET. The 
expansion allows as many orders as possible to make the [[CNS]] night cycle and the primary distribution of the 
Consolidated Trade Summary (CTS). The [[ETF]] reporting of the [[ETF]] Instruction Detail Blotter 
(02981254 PSE/U, 02261254 Production) continues to be distributed at 9:00 P.M. ET. 
For all CTS and [[CNS]] cycle changes along with [[CNS]] exemption processing rules and cutoff, see the 
Accelerated [[settlement]] (T+1) [[DTC]], [[NSCC]], and ITP Functional Changes document available at: 
https://www.[[DTCC]].com/-/media/Files/PDFs/T2/T1-Functional-Changes.pdf 
The following chart shows [[ETF]] reports in scope with the new cutoff and distribution times that will be effective 
with accelerated [[settlement]] T+1. 
Report or File Name Test File Production 
File 
Input/Output Cycles 
Enhanced Create/Redeem Instruction Data Input File 
(Agents only) 
41300 11300 2:00 P.M.-8:45 P.M.  
Hard Cutoff Primary 
Cycle 
 Enhanced [[ETF]] Create and Redeem Instruction Output (Blotter) 
MRO 
02981254 02261254 9:00 P.M. (T) 
(unchanged) 
Enhanced Create/Redeem Instruction 
Detail Print Image Report 
02980291 02260291 9:00 P.M. (T) 
(unchanged)
 
Enhanced [[ETF]] End of Day Create/Redeem 
Receipt/Reject Report  
 
02980098 02120098 8:45 P.M. (T) 
Enhanced [[ETF]] Intraday Create/Redeem Receipt/Reject 
Report  
 
02981954 02261954 Intraday upon receipt. 
UTC Fix Output Fix/MQ Fix MQ  
 
With the introduction of T+1 accelerated [[settlement]], [[NSCC]] will accelerate its pricing sources and begin 
processing Create/Redeem instruction files (41300 PSE/U, 11300 Production) in near real-time beginning at 
approximately 6:30 P.M. ET.  
• The primary cycle continues to open at 2:00 P.M. ET, any order files received prior to completion of 
pricing (approximately 6:30 P.M. ET) generates the [[ETF]] Enhanced Intraday Create/Redeem 
Receipt/Reject Report (02981954 PSE/U, 02261954 Production) in near real-time. 
• At completion of pricing, [[NSCC]] processes any order instruction files received to that point and continues 
to process incoming order instruction files in near real-time. 
[[ETF]] Reporting Through Universal Trade Capture (UTC) Output 
The real time processing will generate [[ETF]] trades to [[NSCC]]’s Universal Trade Capture (UTC) system in near 
real-time with near real-time UTC output detailing the [[ETF]] and component trades between the [[ETF]] Agent and 

---

## Page 5

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 5 
Authorized [[participant]] (AP). For the functional requirements for reception of the UTC output, see the UTC 
Output Requirements section. 
UTC will capture all critical data elements from the [[ETF]] Instruction Detail Blotter that are critical for 
reconciliation and [[settlement]] inclusive of [[collateral]] fields for non-[[CNS]] eligible underlying components and 
distribute in near real-time output as well as Machine Readable Output (MRO file: Production 02081673 / 
PSE/U 02981673). 
Critical Data Elements From [[ETF]] Instruction Detail Blotter 
Review the critical fields from the [[ETF]] Instruction Detail Blotter that will appear in the UTC near real-time and 
MRO output. To help illustrate the critical fields along with their placement in UTC near real-time output, see 
the recent print image blotter figure. 
Transaction [[ID]] – [[ETF]] Agent submitted transaction [[ID]] to associate the [[ETF]] and Component Trades for each 
specific Create and Redeem order. Transaction [[ID]] will appear on UTC output in the Order [[ID]] field, 
• When the fix tag 54 Buy Indicator equals 1 (Buy), the fix tag 37 Order [[ID]] is populated with the Create 
Transaction [[ID]]. 
• When fix tag 54 Buy Indicator equals 2 (Sell), the fix tag 37 Order [[ID]] is populated with Redeem 
Transaction [[ID]]. 
  

---

## Page 6

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 6 
FIX Output Fields 
FIX 
Tag 
No. 
Desc Length 
(MAX) 
Type FIX 
Type 
UTC FIX Values Legacy MRO Values 
54 Buy 
Indicator 
1 A/N Char 1 = Buy 
2 = Sell 
3 = Buy minus 
4 = Sell plus 
5 = Sell short 
6 = Sell short exempt  
B = Buy cover 
1 = Buy 
2 = Sell 
(Position 159) 
37 Order [[ID]] 32 A/N String Unique Order [[ID]] or Branch 
Sequence Number 
Order [[ID]]  
(Position 281 295) 
[[ETF]] Create/Redeem Transaction [[ID]]: 
• Create Transaction [[ID]]  when the fix 
tag 54 Buy Indicator =  1 (Buy). 
• Redeem Transaction [[ID]]  when the fix 
tag 54 Buy Indicator =  2 (Sell). 
 
[[settlement]] Location – [[NSCC]] indicator to specify [[CNS]] versus non-[[CNS]] eligible component CUSIPs. 
• UTC will populate fix tag 577 = 6 for [[CNS]] Eligible ETFs and Components on UTC output. 
• UTC will populate fix tag 577 = 4 for non-[[CNS]] eligible components on UTC output. 
FIX 
Tag 
No. 
Description Length 
(MAX) 
Type FIX 
Type 
UTC FIX Values Legacy MRO Values 
577 Netting 
Indicator 
(Clearing 
Instruction) 
1 N Int 1 = Excluded From All 
Netting (in CTS) 
2 = Bi lateral trade date 
Netting Only (Foreign 
[[securities]]) 
3 = Excluded from Clearing 
(only trade capture) 
4 = [[participant]] Instructed 
Special Trade (in CTS) 
5 = Multilateral Netting 
(B/O) 
6 = Clear Against Central 
Counterparty ([[CNS]]) 
• B = Trade for Trade (No Netting) or 
Foreign T+2 and Older 
• F= Foreign B/O (Bi-lateral Netting) 
Foreign & T+0 or T+1 
• Z = No CTS reporting/ No 
Netting/NoBalanceOrders “ “ if Reject 
• New value for UTC. This was a 
separate field on legacy MRO 
• N = B/O (Multi-lateral Netting) Non 
[[CNS]] C = [[CNS]] (Netting) 
(Position 234 – Netting Indicator) 
(Position 235 – Special Trade Code) 
 
  

---

## Page 7

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 7 
Security Type Code – Generated by [[NSCC]] to identify the [[ETF]] leg versus the underlying component trades. 
UTC populates fix tag 460 = 19 Exchange Traded Managed Fund, on the [[ETF]] leg of the trade on UTC output. 
Note 
UTC will only populate Tag 460 = 19 Exchange Traded Managed Fund on the [[ETF]] trade that can be used in conjunction 
with the Transaction [[ID]]. This tag is not populated when an [[ETF]] is an underlying component. 
 
FIX Tag 
No. 
Description Length 
(MAX) 
Type FIX 
Type 
UTC FIX Values Legacy MRO Values 
460 Security Type 
(Product) 
2 N Int 3 = Corporate 
5 = [[Equity]] 
11 = Municipal 
12 = Other 
14 = [[UIT]] 
15 = Cal 
16 = Put 
17 = Future 
18 = Narrow-based Future 
19 = Exchanged Traded 
Managed Fund 
ES = [[Equity]] [[Stock]] 
C = Bond 
EU = [[Equity]] Unit 
FD = Future Debt (Bond)  
FE = Future [[Equity]] ([[Stock]])  
FU = Future Unit 
M = Municipal Bond  
OC = [[Option]] Call  
OP = [[Option]] Put 
U  =  Unit Investment  Trust 
(Position 152 – 157) 
• [[settlement]] Value – For [[CNS]] eligible Components UTC will continue to populate Tags 381 and 118 
with [[settlement]] Value.  
FIX Tag 
No. 
Description Length 
(MAX) 
Type FIX 
Type 
UTC FIX Values Legacy MRO Values 
381 Principal Trade Amount 
(Gross Trade Amt) 
17 A/N Amt Unit Price x Share Quantity 
16 Digits + 1 (period indicating 
two decimal point offset) 
Price x  Quantity 
Two Decimal  Positions 
(Position 185 – 200) 
118 Net [[settlement]] Amount 
(Net Money) 
17 A/N Amt Net [[settlement]] Money (as 
provided by market) 
16 Digits + 1 (period indicating 
two decimal point offset) 
(Position 250 – 265) 
•  
  

---

## Page 8

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 8 
The following figure shows a clip from Print Image Instruction Detail Blotter to help illustrate critical fields 
listed above that will be populated on UTC output. 
 
• Accrued Interest 
When a Create or Redeem order includes fixed income components [[NSCC]] includes the Accrued Interest 
amount for each component trade on UTC output. Accrued Interest will be populated in Tag 137 on UTC 
output and also on UTC MRO as shown in this section. 
• Transaction Fee 
The [[ETF]] Agent transaction fee that [[NSCC]] passes through on the Instruction Detail Blotter and is sent to 
[[DTC]] [[settlement]] as Code 54 Standard or Code 55 Custom will be populated in Tag 137 Commission / 
Explicit Fee. 
UTC Fix Output 
FIX 
Tag 
No. 
Description Length 
(MAX) 
Type FIX 
Type 
UTC FIX Values Legacy MRO Values 
139 MiscFeeType 2 A/N Char 2 = Tax N/A – New field in UTC. 
137 Accrued Interest 
Amount 
10 A/N Amt Accrued Interest Amount 
 
9 Digits + 1 (period 
indicating two decimal 
point offset) 
Position 241 - 249 
Corporate and Municipal Bond 
Interest from [[ETF]] Create/Redeem 
Order.  
 
  


---

## Page 9

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 9 
FIX 
Tag 
No. 
Description Length 
(MAX) 
Type FIX Type UTC FIX Values Legacy MRO Values 
136 NoMiscFees 1 N NumInGroup 4 N/A – New field in UTC. 
137 Commission / 
Explicit Fee 
9 A/N Amt Total Explicit Fee or Commission 
Amount 
8 Digits + 1 (period indicating two 
decimal point offset) 
Position 339 – 346 
[[ETF]] Agent 
Transaction Fee. 
• Code 54 Standard 
• Code 55 Custom 
Print Image Instruction Detail Blotter 
 
  


---

## Page 10

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 10 
Additional [[collateral]] Related Fields 
See also the Instruction Detail Blotter  screen print. 
Payment Order Amount – The payment order amount for non-[[CNS]] eligible components will be reported in Fix 
Tag 884 [[ETF]] TFT [[collateral]] on UTC output.  
From the Instructional Detail Blotter for the Alliant Energ component, the payment order amount reported in Fix 
Tag 884 [[ETF]] TFT [[collateral]] is $5,125.32. 
 
 
FIX Tag 
No. 
Description Length 
(MAX) 
Type FIX 
Type 
UTC FIX Values Legacy MRO 
Values 
884 [[ETF]] TFT 
[[collateral]] 
17 A/N Amt [[collateral]] Value for Non-[[CNS]] 
Components 
Total [[collateral]] Amount Per 
Create/Redeem Order 
16 Digits + 1 (period indicating two 
decimal point offset) 
N/A - New field in 
UTC. 
 
Net [[settlement]] Value – The Component [[settlement]] Value plus or minus the [[collateral]] payment order 
(Redeem or Create) continues to be reported in Fix Tags 381 and 118 Gross and Net Amount, Example 
$30,751.92. This is the amount [[ETF]] Agents and APs will make DVP/RVP, which effectively reclaims the 
[[collateral]] posted. 
FIX Tag 
No. 
Description Length 
(MAX) 
Type FIX 
Type 
UTC FIX Values Legacy MRO Values 
381 Principal Trade Amount 
(Gross Trade Amt) 
17 A/N Amt Unit Price x Share Quantity 
16 Digits + 1 (period indicating 
two decimal point offset) 
Price x  Quantity 
Two Decimal  Positions 
(Position 185 – 200) 
118 Net [[settlement]] Amount 
(Net Money) 
17 A/N Amt Net [[settlement]] Money (as 
provided by market) 
16 Digits + 1 (period indicating 
two decimal point offset) 
(Position 250 – 265) 
 
  


---

## Page 11

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 11 
Total Payment Order Amount – This is the total [[collateral]] for all non-[[CNS]] eligible components on a Create or 
Redeem Order. This amount will be reported in Fix Tag 884 [[ETF]] TFT [[collateral]] on UTC output on the [[ETF]] leg 
of a Create or Redeem Order only. This amount represents the total [[collateral]] per order that is sent to 
Inventory Management System (IMS) at [[DTC]] [[settlement]] which is collected through an Special Payment Order 
(SPO). NOTE: As detailed above individual payment order amounts per each component are reported in the 
same FIX Tag 884 [[ETF]] TFT [[collateral]] on component trades only. The sum of all Payment Order Amounts for 
trades with the same Transaction [[ID]] will be equal to the Total Payment Order Amount on the [[ETF]] leg of the 
UTC trades. 
Important Notes: 
• As illustrated in the Print Version Instructional Detail Blotter, Total Component [[settlement]] Value plus or 
minus the Cash Amount is always the Value reported for [[settlement]] of the [[ETF]] Creation Units. In the 
example shown, the amount $14, 359,998.18 continues to be reported as the [[ETF]] Creation Unit 
[[settlement]] Value in Fix Tags 381 and 118 Gross and Net on UTC output.  
TOTAL COMPONENT VALUE DEBITED:             14,284,220.890000  
CASH VALUE CREDITED:                           75,777.290000  
TOTAL [[ETF]] VALUE CREDITED:                  14,359,998.180000   
• UTC output will now provide the Transaction [[ID]] and the Security Type =19 on the [[ETF]] leg of UTC trades, 
allowing participants to differentiate the Total Payment Order Amount on the [[ETF]] trade versus the 
individual Payment Order Amount on the component trades. 
• I n cases when underlying components are 100% [[CNS]] eligible, no [[collateral]] needs to be reported. In this 
scenario, the Fix Tag 884 [[ETF]] TFT [[collateral]] is not reported on UTC output. 
Print Version Instruction Detail Blotter 
 
 
Machine Readable Output (MRO) AutoRoute File (Production 
02081673/PSE/U 02981673) 
All data elements described above that will be reported on UTC near real-time output is also available through 
Machine Readable Output (MRO) file, in hourly cycles. While this may seem to be an easier development, the 


---

## Page 12

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 12 
final Cycle 13 that makes the [[CNS]] Night Cycle and primary CTS cycle will not be distributed until 
approximately 9:05 P.M. ET with the prior cycle at 8:00 P.M. ET.  
UTC Output Requirements 
UTC near real-time output is available through Message Queue (MQ) or Fix Engine. Fix Engine is typically 
used by exchanges and firms who also submit either Qualified Special Representative (QSR) or CORR trades 
to UTC. Since [[ETF]] reporting through UTC only requires UTC output, it is recommended that [[ETF]] Agents and 
APs interested in this [[Option]] choose an MQ set up. 
Firms that choose the near real-time UTC Fix output [[Option]] should contact NSCCIntegration@[[DTCC]].com to 
establish connectivity to an MQ server. When [[NSCC]] launch UTC in 2017, firms receiving output only were not 
required to set up an MQ channel in PSE/U test region. As soon as connectivity was complete, their 
subscriptions were activated in Production. Since this is a new [[Option]] for T+1, it is highly recommended that 
firms establish both a test and production MQ channel. The [[NSCC]] Integration team fully coordinates 
onboarding, connectivity, and testing for firms choosing this [[Option]]. Firms considering UTC Fix output through 
MQ should contact [[NSCC]] Integration as soon as possible to start the onboarding and connectivity process to 
shorten lead time for completion. 
Subscriptions 
After the MQ channel connectivity is complete, NSCCIntegration@[[DTCC]].com arranges for the UTC output 
subscriptions (UTCO for output, ETFUTCO included [[ETF]] Market 920 on output). 
Create and Redeem Secondary Cycle 
As detailed above, the Primary Cycle Create and Redeem cutoff time will be expanded until 8:45 P.M. ET for 
T+1. The Secondary Cycle will begin at approximately 9:05 P.M. ET after distribution of the Primary Cycle 
Instruction Detail Blotter. Any Create and Redeem files received after the 8:45 P.M. ET primary cycle cutoff will 
be held and processed at the start of the secondary cycle.  
• Create and Redeem Order Instruction files that miss the 8:45 P.M. ET Primary Cutoff will be held and 
processed at the beginning of the Secondary cycle at approximately 9:05 P.M. ET. 
• All files received after 9:05 P.M. ET will be processed in near real-time and sent to UTC and generate 
UTC output in near real-time. UTC output in the Secondary cycle will include all fields from [[ETF]] 
Instruction Detail Blotter, as detailed above in the Primary Cycle processing section. 
• The secondary cycle submission cutoff for Create and Redeem order instructions remains at 
11:00 P.M. ET, with distribution of the [[ETF]] Instruction Detail Blotter at 11:15 P.M. ET. 
• Create and Redeem orders processed in the Secondary cycle will not make the [[CNS]] night cycle or the 
Primary CTS cycle. These orders are processed in the day cycle on [[settlement]] date. 
[[settlement]] Date Assignment Rules 
• [[NSCC]] will implement coding changes to its [[ETF]] Create/Redeem application to update the rules this 
system uses to assign the [[settlement]] date to transactions.  
• The following changes will apply to all trades submitted for the [[ETF]] Create and Redeem process using 
the Enhanced [[ETF]] Create and Redeem Instruction Input MRO: DATATRAK Production 11300 / 
PSE/U 41300). Members are reminded that these changes will also be reflected in any [[ETF]] output that is 
distributed to them.  
o Transactions submitted with a value = spaces (Regular Way) or a value = 1 (Next Day) in the 
[[settlement]] Code field (Position 58) of the DATATRAK 11300 layout will be updated to be assigned a 
regular way [[settlement]] date of one business day after trade date. 

---

## Page 13

Functional Requirements 
Functional Requirements: Near Real-Time Create/Redeem Processing 13 
o Transactions submitted with a value = 2, 3, 4, or 5 in the [[settlement]] Code Field (Position 58) will be 
for extended [[settlement]]. The actual value submitted in that field will equal the numbers of days in the 
extended [[settlement]].  
o Similar to UTC processing of As Of regular way trades, the [[ETF]] Create/Redeem process will have 
rules to support the conversion process based on the submitted trade date. For As Of trades 
received on XX-XX-XXXX or later with a T = XX-XX-XXXX or earlier, [[NSCC]] internal code will 
assign regular way [[settlement]] with the pre-conversion rules where the [[settlement]] date is X business 
days after the submitted trade date. The internal code will only apply post conversion date [[settlement]] 
assignment rules (specified above) for trades with a T = XX-XX-XXXX and later.  
 
DATATRAK Production 11300/PSE 41300 Type 2–Instruction Record 
Record length=300 
Required for all instructions. 
Seq Description Length Start Type Comments Required or 
Optional Field 
10 [[settlement]] Code 
(previously 
called Shortened 
[[settlement]] 
Code) 
1 58 A/N • Space = [[default]] for Regular Way 
(Next day [[settlement]] = regular 
way) 
• 1 = Next Day Regular Way 
• 2 = Extended Two Day [[settlement]] 
• 3 = Three Day [[settlement]] 
• 4 = Four Day [[settlement]] 
• 5 = Five Day [[settlement]] 
Required 
11 Cash Only 
Indicator 1 59 A/N • Y = Cash only (no components 
settled) 
• space = not cash only 
Required 
 
For conversion processing of Regular Way and As Of Regular Way trades over the conversion launch period, 
tentatively scheduled for September 3, 2024 that is awaiting regulatory approval, see the T+1 functional 
document available from the T+1 site at: https://www.[[DTCC]].com/ust1/documentation  
Updated Formats and Resource Links 
This document includes relevant sections of input and output formats.  
• For the Shortening the US Equities [[settlement]] Cycle (T+1) documentation, see UST1. This site also 
includes the Accelerated [[settlement]] (T+1) [[DTC]], [[NSCC]], and ITP Functional Changes document. 
• For the full updated formats, see the [[ETF]] Release section of the [[DTCC]] Learning Center. 
• For the current [[ETF]] and UTC formats, see [[ETF]] Technical Resources and UTC Technical Resources.  
 

---

## Page 14

 
 
© 2024 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation [[DTCC]]. The services described herein are 
provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  
[[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and 
regulations of the particular country or countries in which such entity operates. Please see www.[[DTCC]].com for more 
information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: January 26, 2024 
Publication Code: ETF228 
Service: Accelerated [[settlement]] T+1 
Title: [[NSCC]] [[primary market]] Create/Redeem Functional Requirements  
 
   