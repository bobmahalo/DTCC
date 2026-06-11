---
title: "T+1 Settlement: UTC Common Trade FIX Output Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc132a_T1-common_trade_FIX_output_2024Jan30.pdf"
pages: 26
size: "320.9 KB"
category: "UTC"
ingested_on: "2026-06-05"
---

# T+1 Settlement: UTC Common Trade FIX Output Format

**Original File:** [utc132a_T1-common_trade_FIX_output_2024Jan30.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc132a_T1-common_trade_FIX_output_2024Jan30.pdf)  
**Category:** UTC  
**Total Pages:** 26  
**File Size:** 320.9 KB  

---

## Page 1

Universal Trade Capture (UTC)
ACCELERATED [[settlement]] (T+1): UTC COMMON TRADE FIX 
OUTPUT FORMAT
JANUARY 26, 2023
View the header, data details, and trailer information for the UTC Common Trade FIX Output format.
Notes
l All A/N fields are initialized to spaces ( ). Fields populated with spaces are not transmitted.
l All numeric fields are initialized to zero (0).
l For rejected transactions, some fields with defined values may be populated with a space ( ).
l Fields that are not required on input are not validated and are passed on output as reported to [[DTCC]]. See UTC Technical Resources.

---

## Page 2

Header
View the Header record details for the UTC Common Trade FIX output format:
FIX Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO 
Values
8 BeginString 7 A/N String Identifies the beginning of a new message generated by FIX.  N/A
9 BodyLength 4 N Length Message length generated by FIX. N/A
35 Message Type (Msg 
Type)
2 A/N String AE = Trade Capture Report N/A
49 SenderCompID 4 A/N String Value = [[NSCC]]
Assigned value used to identify the firm sending the message.
N/A
56 TargetCompID 8 A/N String Assigned value used to identify receiving firm message.  N/A
34 Message Identifier 
(Msg Seq Num)                                                 
9 N SeqNum Unique message identifier.
Generated by FIX.
(May not arrive in the sequence number order when 
transmitted over Message Queue (MQ)).
N/A
52 SendingTime 21 A/N TimeStamp TimeStamp generated by FIX. N/A
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
2

---

## Page 3

Data Detail
View the Data Details for the UTC Common Trade FIX output format:
FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
571 Report [[ID]]
(Trade Report [[ID]])                                                 
15 N/A String Unique message identifier generated by 
[[NSCC]].
N/A
487 Reversal/Correction 
(Trade Report 
Trans Type)                                                 
1 N Int 0 = New Trade
2 = Replace (Correct)
4 = Reverse (Cancel)
" " = Original Trade
C = Correction by Market 
N = Correction by [[NSCC]] 
R = Reversal by Market 
S = Reversal by [[NSCC]] 
D = Don't Count Trade 
K = Don't Count Reversal Trade
L = Don't Count Correction Trade
(Position 338)
570 Previously Reported 1 A/N Boolean N = No
Y = Yes
N/A
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
3

---

## Page 4

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
423 Pricing Variance
 Indicator
(PriceType)
1 N Int % change from last night’s closing price 
0 = No Variance 
1 = 25% 
2 = 50% 
3 = 75% 
4 = Greater than 75%
N/A – New field in UTC.
55 Security [[ID]] Symbol
(Symbol)
15 A/N String Security Symbol Security Symbol
(Position 125 - 139)
22 Security [[ID]] Source 1 A/N String 4 = ISIN  
48 ISIN
(Security [[ID]])
12 A/N String Country Code 2 positions, followed by 9 pos-
ition [[CUSIP]], and one position check digit.
ISIN 
(Position 140 – 151)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
4

---

## Page 5

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
460 Security Type 
(Product)
2 N Int 3 = Corporate
5 = [[Equity]]
11 = Municipal
12 = Other
14 = [[UIT]]
15 = Call
16 = Put
17 = Future
18 = Narrow-based Future
19 = Exchange Traded Managed Fund
ES = [[Equity]] [[Stock]] 
C = Bond
EU = [[Equity]] Unit
FD = Future Debt (Bond)
FE = Future [[Equity]] ([[Stock]])
FU = Future Unit
M = Municipal Bond
OC = [[Option]] Call
OP = [[Option]] Put
U = Unit Investment Trust
(Position 152 – 157)
913 [[settlement]] Location 2 A/N String DT = [[DTC]]
EC = EuroCCP
DT = [[DTC]]
(Position 239 – 240)
32 Share Quantity 11 N Qty Share Quantity Share Quantity
31 Unit Price
(Last Px)
13 A/N Price 12 Digits + 1 (period indicating six decimal 
point offset)
12 Digits
(Position 172 – 183)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
5

---

## Page 6

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
30 Market
(Last Mkt)
3 A/N Exchange 010 = [[NYSE]] S/E
020 = [[NYSE]] MKT (AMEX)
025 = [[NYSE]] 2
030 = [[NYSE]] ARCA S/E
035 = [[NYSE]] ARCA II
040 = Chicago S/E
060 = Over the Counter
070 = Options Clearing Corp.
080 = National [[Stock]] Exchange
090 = Prime [[Broker]]/ OMGEO
100 = Corresponding Clearing
110 = [[NASDAQ]]
130 = BATS BZX
135 = BATS BYX
140 = [[NASDAQ]] OMX BX
145 = [[NASDAQ]] OMX PHLX
150 = Direct Edge A (EDGA)
160 = Direct Edge X (EDGX)
170 = IEX [[Stock]] Exchange
185 = Long Term [[Stock]] Exchange
Originating Market
(Position 105 – 108)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
6

---

## Page 7

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
190 = MIAX Pearl Equities Exchange
195 = Members Exchange
920 = [[ETF]] Create/Redeem
(available by subscription)
75 Trade Date 8 N Local Mkt DateCCYYMMDD  CCYYMMDD
(Position 217 – 224)
60 Trade Time
(Transaction Time)
9 A/N Timestamp Time of Execution (market’s time zone)
HHMMSSMSS
Time of Execution (market’s time 
zone)
HHMMSSMSS
63 [[settlement]] Type 1 A/N Char 0 = Regular
1 = Cash
2 = Next Day
6 = [[Seller]]’s [[Option]] (Future)
7 = When Issued
" " = Regular Way 
CA = Cash 
ND = Next Day
### = Delayed Delivery ([[Seller]]’s 
[[Option]]) number of business days 
up to 180 -- * The actual [[settlement]] 
date is displayed for the Sellers 
[[Option]].
(Position 236 – 238)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
7

---

## Page 8

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
64 [[settlement]] Date 8 N Local Mkt DateCCYYMMDD 
99991231 – [[default]] value for a When 
Issued trade 
If the trade is rejected, the [[settlement]] date 
is not provided.
CCYYMMDD 
99991231 When and if Issued
(Position 225 – 232)
552 Number of sides 1 N NumInGroup 1 = One Side N/A – New field in UTC.
54 Buy Indicator 1 A/N Char 1 = Buy
2 = Sell
3 = Buy minus
4 = Sell plus 
5 = Sell short 
6 = Sell short exempt
B = Buy cover
1 = Buy
2 = Sell
(Position 159)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
8

---

## Page 9

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
37 Order [[ID]] 32 A/N String Unique Order [[ID]] or Branch Sequence 
Number.
Order [[ID]]
(Position 281 295)
[[ETF]] Create/Redeem Transaction 
[[ID]]:
 l Create Transaction [[ID]]   when 
fix tag 54 Buy Indicator = 1 
(Buy).
 l  Redeem Transaction [[ID]]   when 
fix tag 54 Buy Indicator = 2 
(Sell).
198 Market Control 
Number
32 A/N String Market Control Number/ TA (Turn Around) 
Number
Executing [[ID]]
(Position 266 – 280)
11 Client Order [[ID]] 32 A/N String OATS/Regulatory Assigned Number Client Order [[ID]]
(Position 296-325)
526 Original Execution [[ID]] 32 A/N String Original Execution [[ID]] / TA (Turn Around) 
Number
TA Number
(Position 326-334)
66 Execution [[ID]] 32 A/N String Execution [[ID]] N/A – New field in UTC.
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
9

---

## Page 10

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
453 NoPartyIDs 1 N NumInGroup Number of party IDs to follow.  Must be at 
least four (Buy and Sell Clearing Brokers 
and Executing Brokers are required) and 
up to a maximum of nine can be specified.                                                 
N/A – New field in UTC.
448 Clearing [[Broker]]                                                 8 A/N String [[NSCC]] [[participant]] Number [[NSCC]] [[participant]] Number 
(Position 9-12)
452 Party Role 2 N Int 04 = Clearing Firm  N/A – New field in UTC.
448 Entering / Executing 
[[Broker]]
8 A/N String Market Mnemonic / MPID  Executing [[Broker]]
(Position 28-31)
Entering [[Broker]]
(Position 47-50)
452 Party Role 2 N Int 01 = Executing Firm N/A – New field in UTC.
448 Introducing [[Broker]]                                                 8 A/N String Introducing [[Broker]] – Party who initiated 
the trade.                                                 
N/A – New field in UTC.
452 Party Role 2 N Int 06 = Introducing Firm N/A – New field in UTC.
448 Badge [[ID]] 8 A/N String Badge [[ID]] Badge Number for the specialist or 
[[Broker]].
(Position 51 – 54)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
10

---

## Page 11

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
452 Party Role 2 N Int 11 = Initiating Trader  N/A – New field in UTC.
448 Clearing [[Broker]] 8 A/N String [[NSCC]] [[participant]] Number [[NSCC]] [[participant]] Number
(Position 70-73)
452 Party Role 2 N Int 18 = Contra Clearing Firm N/A – New field in UTC.
448 Entering / Executing 
[[Broker]]
8 A/N String Market Mnemonic / MPID Contra Executing [[Broker]]
(Position 85-88)
452 Party Role 2 N Int 37 = Contra Trader N/A – New field in UTC.
448 Introducing [[Broker]] 8 A/N String Introducing [[Broker]] N/A – New field in UTC.
452 Party Role 2 N Int 17 = Contra Firm N/A – New field in UTC.
448 Badge [[ID]] 8 A/N String Badge [[ID]] N/A – New field in UTC.
452 Party Role 2 N Int 12 = Executing Trader N/A – New field in UTC.
448 Submitted By 
[[participant]] 
1 A/N String 0 = by Market
1 = by [[Buyer]] [[participant]]
2 = by [[Seller]] [[participant]]
N/A – New field in UTC.
452 Party Role 2 N Int 36 =  Entering Trader  N/A – New field in UTC.
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
11

---

## Page 12

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
1 Account Number 32 A/N String Client’s Account Number N/A – New field in UTC.
581 Buy House Client 
Indicator
(Account Type)
1 N Int 1 = AccountCustomer                                                 
3 = HouseTrader                                                 
4 = MarketMaker                                                   
N/A – New field in UTC.
81 Step In – Step Out 
Indicator                                           
1 A/N Char 0 = Regular
2 = StepIn                                                 
3 = StepOut                                                 
N/A – New field in UTC.
Previously reported in the Special 
Trade indicator.
(Position 235)
575 Odd Lot Indicator 1 A/N Boolean N = No (Round Lot)
Y = Yes (Odd Lot)
(Position 171 – 171)
576 No of Clearing Instruc-
tions                                         1 N Int 1 = [[default]] Value N/A
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
12

---

## Page 13

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
577 Netting Indicator
(Clearing Instruction)
1 N Int  l 1 = Excluded From All Netting (in 
CTS)
 l 2 = Bilateral trade date Netting 
Only (Foreign [[securities]])
 l 3 = Excluded from Clearing (only 
trade capture)
 l 4 = [[participant]] Instructed Spe-
cial Trade (in CTS) 
 l 5 = Multilateral Netting (B/O)
 l 6 = Clear Against Central Coun-
terparty ([[CNS]])
 l B = Trade-for-trade (No Net-
ting) or Foreign T+2 and 
Older
 l F = Foreign B/O (Bilateral 
Netting) Foreign & T+0 or 
T+1
 l Z = No CTS reporting/ No 
Netting/NoBalanceOrders “ 
“ if Reject
 l New value for UTC. This 
used to be a separate field 
on legacy MRO 
 l N = B/O (Multi-lateral Net-
ting) Non [[CNS]]
 l C = [[CNS]] (Netting) 
(Position 234 – Netting Indicator) 
(Position 235 – Special Trade 
Code)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
13

---

## Page 14

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
578 Source of Transaction 
/ Market System
(Trade Input Source)
2 A/N String [[NYSE]]/[[NYSE]](MKT):
 l O = OCS
 l P = PTP 
 l S = Step Out
 l F = Force([[Broker]] or DMM) 
[[NYSE]] 2: 
 l NB = [[NYSE]] [[Bonds]]
 l BT = [[NYSE]] Blocked 
 l MP = [[NYSE]] Match Point 
Chicago [[Stock Exchange]]: 
 l CH = Trades occurring at CHX
 l AW = Trades occurring away 
from CHX
[[NYSE]]:
XNYS = New York or [[NYSE]] 
Alternext US.
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
14

---

## Page 15

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
[[OTC]]:
 l A = TRF
 l D = Portal
 l E = EACT
 l N = [[NASDAQ]] Step-Outs
 l Q = QSR/ECN                                                 
 l U = [[NYSE]] AGU
 l X = [[NYSE]] TRF
 l OR = [[OTC]] Reporting Facility
 l AD = Alt Display Facility
[[OTC]]: 
XADF = Alt Display Facility
XNAS = [[NASDAQ]] 
XOTC = Over the Counter (See 
position 109 to 112 for TRF 
reporting)
CORR:
“ “ (space) = External Position Movement
M = Internal Position Movement 
CORR: 
COR = Correspondent Clearing
(Position 109 – 112)
15 Currency Code 3 A/N Currency USD = US Dollars
[[default]] is USD
USD = US Dollars 
(Position 201 – 203)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
15

---

## Page 16

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
528 Order Capacity  1 A/N Char [[NYSE]]
A = Not a [[Member]] / [[Member]] organization 
and not an individual [[investor]].
C = Program trade, non-index arbitrage for 
the proprietary account of a 
[[Member]]/[[Member]] organization or affiliate.
D = Program trade, index arbitrage,  for 
the proprietary account of a 
[[Member]]/[[Member]] organization or affiliate.
I = Individual [[investor]], not a discretionary 
or managed account.
J = Program trade, index arbitrage, for 
account of individual [[investor]].
K = Program trade, non-index arbitrage, 
for account of individual [[investor]].
P = Non-Program trading for the 
proprietary account of a [[Member]]/[[Member]] 
organization or affiliate.
Q = Proprietary trade by a [[Member]] on the 
Floor relating to the [[Member]]’s own error.
S = Designated Market Maker
U = Program trade, index arbitrage and 
agency.
Y = Program trade, non-index arbitrage 
Capacity code 
(Position 104)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
16

---

## Page 17

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
and agency.
All other markets
A = Agency
F = Firm
P = Principal
R = Riskless Principal
V = Mixed
381 Principal Trade 
Amount
(Gross Trade Amt)
17 A/N Amt   Unit Price x Share Quantity
16 Digits + 1 (period indicating two 
decimal point offset)
Price x Quantity 
Two Decimal Positions
(Position 185 – 200)
118 Net [[settlement]] 
Amount
(Net Money)
17 A/N Amt   Net [[settlement]] Money (as provided by 
market) 
16 Digits + 1 (period indicating two 
decimal point offset)
(Position 250 – 265)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
17

---

## Page 18

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
58 Don’t Count Indicator 
([[SEC]] 31 Fees)
1 A/N String D = Don’t Count 
P = Don’t Count; [[participant]] pays
Note: If tag #58 is not reported on [[NSCC]] 
FIX or MQ trade capture output, the sell 
side contract amount was included 
(Counted) in Section 31 market totals for 
applicable markets. 
Some markets are not eligible for Section 
31 processing. As such, they are not 
counted for Section 31 fees regardless of 
the Don’t Count Indicator value submitted 
on input.  All transactions in the following 
markets are reported as blank in the Don’t 
Count Indicator (tag 58) field. Here are the 
market codes and names.
060 = Over the Counter
070 = Options Clearing Corp 
090 = Prime [[Broker]]/ OMGEO
100 = Correspondent Clearing
New field in UTC. 
This information is denoted in the 
Reversal/Correction field of the 
Legacy MRO.
(Position 338)
136 NoMiscFees 1 N NumInGroup 4 N/A – New field in UTC.
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
18

---

## Page 19

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
137 Commission / Explicit 
Fee
9 A/N Amt Total Explicit Fee or Commission Amount 
8 Digits + 1 (period indicating two decimal 
point offset)
Position 339 – 346
[[ETF]] Agent Transaction Fee.
 l Code 54 Standard
 l Code 55 Custom
139 MiscFeeType 2 A/N Char 10 = Transaction  N/A – New field in UTC.
137 Other Fees 7 A/N Amt Other Fees 
6 Digits + 1 (period indicating two decimal 
point offset)
Position 347 – 352
139 MiscFeeType 2 A/N Char 1 = Reg  N/A – New field in UTC.
137 Taxes 8 A/N Amt Taxes 
7 Digits + 1 (period indicating two decimal 
point offset)
Position 353 – 359
139 MiscFeeType 2 A/N Char 2 = Tax N/A – New field in UTC.
137 Accrued Interest 
Amount 
10 A/N Amt Accrued Interest Amount 
9 Digits + 1 (period indicating two decimal 
point offset)
Position 241 – 249
Corporate and Municipal Bond 
Interest from the [[ETF]] 
Create/Redeem Order.
139 MiscFeeType 2 A/N Char 7 = Other  N/A – New field in UTC.
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
19

---

## Page 20

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
884 [[ETF]] TFT [[collateral]] 17 A/N Amt [[collateral]] Value for Non-[[CNS]] Components 
Total [[collateral]] Amount Per 
Create/Redeem Order 16 Digits + 1 (period 
indicating two decimal point offset).
N/A – New field in UTC.
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
20

---

## Page 21

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
825 [[Liquidity]] Indicator
(Exchange Rule)
1 A/N String (For [[NYSE]] Executions)
[[Liquidity]] Indicators
1 = Taker
2 = Provider
3 = Blended
4 = Opening/Prior Day Order
5 = Opening
6 = Closing
7 = Closing/MOC/LOC Order
8 = Retail Order Provider 
9 = Retail Order Taker
F = 3rd Party Algo @ [[NYSE]]
G = 3rd Party Algo Away
Market Center Values
A = [[NYSE]] MKT (AMEX)
B = [[NASDAQ]] BX
C = National
D = [[NASD]]
M = Chicago
P = ARCA
(For [[NYSE]] Executions) [[Liquidity]] 
Indicators 
1 = Taker 
2 = Provider 
3 = Blended 
4 = Opening Prior Day Order 
5 = Opening 
6 = Closing 
7 = Closing MOC/ LOC Order 
8 = Specialist 
9 = Odd Lot 
[[NYSE]] Only: 
(For Routed Away Orders)
Market Center Values 
A = [[NYSE]] Alternext US 
C = National 
D = [[NASD]] 
F = Executed at [[NYSE]] 
G = Executed at Away Market 
I = ISE 
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
21

---

## Page 22

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
T = [[NASDAQ]]
X = [[NASDAQ]] PHLX
Y = BATSY
J = Direct Edge A
K = Direct Edge X
M = Chicago 
P = Arca 
T = [[NASDAQ]] 
X = Philadelphia 
Z = BATS 
(Position 399)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
22

---

## Page 23

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
751 [[NSCC]] Reject Codes 2 N Int 0 = Accepted Trade 
1 = Reject Invalid [[participant]] Info 
2 = Reject Invalid Trade Date 
3 = Reject Invalid Security 
4 = Reject Invalid Quantity 
5 = Reject Invalid Price 
6 = Reject Invalid Trade Source 
7 = Reject Invalid Market 
8 = Reject Multiple Rejects
9 = Reject Invalid Relationship 
10 = Reject Invalid Explicit Fee 
12 = Reject Invalid Message Type 
13 = Reject Invalid Trade Type 
14 = Reject Invalid Sending Entity 
(ineligible for submitted market, 
[[participant]], subsystem) 
15 = Reject Invalid Trade Sequence 
Number 
16 = Reject Invalid Submitted-by Indicator 
17 = Reject Invalid Number of Sides 
18 = Reject Unknown Instrument 
ØØ = No [[NSCC]] Rejects 
01 = Invalid [[participant]] 
02 = Invalid Trade Date 
03 = Invalid Security 
04 = Invalid Quantity 
05 = Invalid Price 
06 = Invalid Trade Source 
07 = Invalid Trade Originator 
08 = Multiple Rejects 
09 = Invalid Value 
10 = Invalid Explicit Fee 
(Position 336 – 337)
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
23

---

## Page 24

FIX 
Tag 
No.
Description Length 
(MAX)
Type FIX Type UTC FIX Values Legacy MRO Values
19 = Reject Invalid Introducing [[Broker]] 
20 = Reject Invalid Executing/Entering 
[[Broker]]
21 = Reject Invalid [[settlement]] Date 
22 = Reject Invalid [[settlement]] Type 
23 = Reject Invalid Principal Trade 
Amount 
24 = Reject Invalid Net Settling Amount 
25 = Reject Invalid Currency Code 
26 = Reject Invalid [[settlement]] Days 
27 = Reject Invalid Buy or Sell Type Code 
28 = Pend Invalid [[participant]] 
29 = Pend Invalid Relationship 
30 = Pend Invalid Security 
31 = Pend Invalid Sending Entity 
(ineligible for submitted market, 
[[participant]], subsystem) 
32 = Pend Potentially Erroneous
Value 
33 = Pend Invalid Affiliate Relationship 
50 = Reject Invalid Execution Time 
53 = Reject Invalid Affiliate Relationship
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
24

---

## Page 25

Trailer
View the Trailer record details for the UTC Common Trade FIX output format:
FIX Tag No. Description Length (MAX) Type FIX Type UTC FIX Values Legacy MRO Values
10 CheckSum 3 A/N String Generated by FIX FIX tag 10 is provided on 
all transactions.
AcceleratedSettlement(T+1):UTCCommonTradeFIXOutputFormat
25

---

## Page 26

© 2024 [[DTCC]]. All rights reserved.   [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation [[DTCC]]. The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of 
The Depository Trust & Clearing Corporation (“[[DTCC]]”).   [[DTCC]] itself does not provide such services.   Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see   www.[[DTCC]].com for more 
information on [[DTCC]], its affiliates and the services they offer.
 
 
Doc Date: January 30, 2024
Publication Code: UTC132a
Service: Universal Trade Capture (UTC)
Title: Accelerated [[settlement]] (T+1): UTC Common Trade FIX Output Format
For More Information
 
Email [[DTCC]] Learning at:
corelearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com