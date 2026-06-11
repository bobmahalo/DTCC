---
title: "UTC Intraday MRO (02081673) Trade Capture Data - Output Format"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc113_trade_capture_intraday_mro_02081673_2021Jun22.pdf"
pages: 17
size: "705.3 KB"
category: "UTC"
ingested_on: "2026-06-05"
---

# UTC Intraday MRO (02081673) Trade Capture Data - Output Format

**Original File:** [utc113_trade_capture_intraday_mro_02081673_2021Jun22.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/utc113_trade_capture_intraday_mro_02081673_2021Jun22.pdf)  
**Category:** UTC  
**Total Pages:** 17  
**File Size:** 705.3 KB  

---

## Page 1

UNIVERSAL TRADE CAPTURE (UTC) 
UTC INTRADAY MRO (02081673) TRADE CAPTURE DATA - OUTPUT FORMAT
JUNE 22, 2021


---

## Page 2

© 2021 [[DTCC]]. All rights reserved.   [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. 
TOGETHER, and the Interlocker graphic are registered and unregistered trademarks of The Depository Trust 
& Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The 
Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of 
these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or 
countries in which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its 
affiliates and the services they offer.
 
Doc Info: June 22, 2021
Publication Code: UTC113
Service:Universal Trade Capture (UTC)
Title: UTC Intraday MRO (02081673) Trade Capture Data - Output Format 

---

## Page 3

UTCIntradayMRO(02081673)TradeCaptureData 3
UTC INTRADAY MRO (02081673) TRADE CAPTURE DATA
View the details of the UTC intraday MRO (02081673) trade capture data output format.
Notes
 l All A/N fields are initialized to spaces ( ). Fields populated with spaces are not transmitted.
 l All numeric fields are initialized to zero (Ø).
 l For rejected transactions, some fields with defined values may be populated with a space ( ). 
 l Fields that are not required on input are not validated and are passed on output as reported to [[DTCC]]. See the 
UTC Input Message Formats. 
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
Reversal/Correction 
(Trade Report 
Trans Type)                         
1 1 1 N 0 = New Trade
2 = Replace (correct)
4 = Reverse (cancel)
" " = Original Trade
C = Correction by Market 
N = Correction by [[NSCC]] 
R = Reversal by Market 
S = Reversal by [[NSCC]] 
D = Don't Count Trade 
K = Don't Count Reversal Trade
L = Don't Count Correction Trade
(Position 338)
Pricing Variance 
Indicator
(PriceType)
1 2 2 N % change from last night’s 
closing price 
0 = No Variance 
1 = 25% 
2 = 50% 
3 = 75% 
4 = Greater than 75%
N/A – New field in UTC.
Security [[ID]] Symbol
(Symbol)
15 3 17 A/N Security Symbol Security Symbol
(Position 125 - 139)
ISIN
(Security [[ID]])
12 18 29 A/N Country Code, [[CUSIP]], and 
check digit.
ISIN 
(Position 140 – 151)
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 4

UTCIntradayMRO(02081673)TradeCaptureData 4
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
Security Type 
(Product)
2 30 31 N 3 = Corporate
5 = [[Equity]]
11 = Municipal
12 = Other
14 = [[UIT]]
15 = Call
16 = Put
17 = Future
18 = Narrow-based Future
19 = Exchange Traded Managed 
Fund
ES = [[Equity]] [[Stock]] 
C = Bond
EU = [[Equity]] Unit
FD = Future Debt (Bond)
FE = Future [[Equity]] ([[Stock]])
FU = Future Unit
M = Municipal Bond
OC = [[Option]] Call
OP = [[Option]] Put
U = Unit Investment Trust
 
(Position 152 – 157)
[[settlement]] Location2 32 33 A/N DT = [[DTC]]
EC = EuroCCP
DT = [[DTC]]
(Position 239 – 240)
Share Quantity
(Last Qty)
11 34 44 N Share Quantity Share Quantity
(Position 160 – 170)
Unit Price
(Last Px)
13 45 57 A/N 12 Digits + 1 (period indicating 
six decimal point offset)
12 Digits
(Position 172 – 183)
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 5

UTCIntradayMRO(02081673)TradeCaptureData 5
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
Market
(Last Mkt)
3 58 60 A/N 010 = [[NYSE]] S/E
020 = [[NYSE]] MKT (AMEX)
025 = [[NYSE]] 2
030 = [[NYSE]] ARCA S/E
035 = [[NYSE]] ARCA II
040 = Chicago S/E
060 = Over the Counter
070 = Options Clearing Corp.
080 = National [[Stock Exchange]]
090 = [[Prime Broker]]/ OMGEO
100 = Corresponding Clearing
110 = [[NASDAQ]]
130 = BATS BZX
135 = BATS BYX
140 = [[NASDAQ]] OMX BX
145 = [[NASDAQ]] OMX PHLX
150 = Direct Edge A (EDGA)
160 = Direct Edge X (EDGX)
170 = IEX [[Stock Exchange]]
185 = Long Term [[Stock]] 
Exchange
190 = MIAX Pearl Equities 
Exchange
195 = Members Exchange
920 = [[ETF]] Create/Redeem 
(available by subscription)
Originating Market
(Position 105 – 108)
Trade Date 8 61 68 N CCYYMMDD CCYYMMDD
(Position 217 – 224)
Transaction Time 9 69 77 A/N Time of Execution (market’s 
time zone)
HHMMSSMSS
Time of Execution (market’s time 
zone)
HHMMSSMSS
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 6

UTCIntradayMRO(02081673)TradeCaptureData 6
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
[[settlement]] Type 1 78 78 A/N 0 = Regular
1 = Cash
2 = Next Day
6 = [[Seller]]’s [[Option]] (Future)
7 = When Issued
" " = Regular Way 
CA = Cash 
ND = Next Day
 
### = Delayed Delivery ([[Seller]]’s 
[[Option]]) number of business days 
up to 180 -- * The actual 
[[settlement]] date is displayed for 
the Sellers [[Option]].
 
(Position 236 – 238)
[[settlement]] Date 8 79 86 N CCYYMMDD 
99991231 – [[default]] value for a 
When Issued trade 
If the trade is rejected, the 
[[settlement]] date is spaces.
CCYYMMDD 
99991231 When and if Issued
(Position 225 – 232)
Side Indicator 1 87 87 A/N 1 = Buy
2 = Sell
3 = Buy minus
4 = Sell plus 
5 = Sell short 
6 = Sell short exempt
B = Buy cover
1 = Buy
2 = Sell
 
(Position 159)
Order [[ID]] 32 88 119 A/N Unique Order [[ID]] or Branch 
Sequence Number.
Order [[ID]]
(Position 281 295)
Market Control 
Number
32 120 151 A/N Market Control Number/ TA 
(Turn Around) Number
Executing [[ID]]
(Position 266 – 280)
Client Order [[ID]] 32 152 183 A/N OATS/Regulatory Assigned 
Number
Client Order [[ID]]
(Position 296-325)
Original Execution 
[[ID]]
32 184 215 A/N Original Execution [[ID]] / TA (Turn 
Around) Number
TA Number
(Position 326-334)
Execution [[ID]] 32 216 247 A/N Execution [[ID]] N/A – New field in UTC.
Clearing [[Broker]]                         8 248 255 A/N [[NSCC]] [[participant]] Number [[NSCC]] [[participant]] Number 
(Position 9-12)
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 7

UTCIntradayMRO(02081673)TradeCaptureData 7
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
Entering / Executing 
[[Broker]]
8 256 263 A/N Market Mnemonic / MPID Executing [[Broker]]
(Position 28-31)
 
Entering [[Broker]]
(Position 47-50)
Introducing [[Broker]]                         8 264 271 A/N Introducing [[Broker]] – Party who 
initiated the trade.                         
N/A – New field in UTC.
Badge [[ID]] 8 272 279 A/N Badge [[ID]] Badge Number for the specialist 
or [[Broker]].
(Position 51 – 54)
Contra Clearing 
[[Broker]]
8 280 287 A/N [[NSCC]] [[participant]] Number [[NSCC]] [[participant]] Number
(Position 70-73)
Contra  Entering / 
Executing [[Broker]]
8 288 295 A/N Market Mnemonic / MPID Contra Executing [[Broker]]
(Position 85-88)
Contra Introducing 
[[Broker]]
8 296 303 A/N Introducing [[Broker]] N/A – New field in UTC.
Contra Badge [[ID]] 8 304 311 A/N Badge [[ID]] N/A – New field in UTC.
Submitted By 
[[participant]] 
1 312 312 A/N 0=byMarket
1 = by [[Buyer]] [[participant]]
2=bySellerParticipant
N/A – New field in UTC.
Account Number 32 313 344 A/N Client’s Account Number N/A – New field in UTC.
House Client 
Indicator
(Account Type)
1 345 345 N 1 = Account Customer                         
3 = House Trader                         
4 = [[Market Maker]]                          (Floor Trader)
N/A – New field in UTC.
Step In – Step Out 
Indicator                      
1 346 346 A/N 0 = Regular
2 = StepIn                         
3 = StepOut                         
N/A – New field in UTC.
Previously reported in the Special 
Trade indicator.
(Position 235)
Odd Lot Indicator 1 347 347 A/N N = No (Round Lot)  
Y = Yes (Odd Lot)  
(Position 171 – 171)
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 8

UTCIntradayMRO(02081673)TradeCaptureData 8
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
Netting Indicator
(Clearing Instruction)
1 348 348 N  l 1 = Excluded From All 
Netting (in CTS)
 
 l 2 = Bi-lateral trade date 
Netting Only (Foreign 
[[securities]])
 l 3 = Excluded from Clearing 
(only trade capture)
 
 l 4 = [[participant]] Instructed 
Special Trade (in CTS) 
 l 5 = Multilateral Netting (B/O)
 
 l 6 = Clear Against Central 
Counterparty ([[CNS]])
 l B = Trade-for-trade (No 
Netting) or Foreign T+2 and 
Older
 l F = Foreign B/O (Bi-lateral 
Netting) Foreign & T+0 or T+1
 l Z = No CTS reporting/ No 
Netting/NoBalanceOrders “ “ 
if Reject
 
 l New value for UTC. This 
used to be a separate field on 
legacy MRO 
 l N = B/O (Multi-lateral Netting) 
Non [[CNS]]
 
 l C = [[CNS]] (Netting) 
 
(Position 234 – Netting Indicator) 
(Position 235 – Special Trade 
Code)
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 9

UTCIntradayMRO(02081673)TradeCaptureData 9
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
Source of 
Transaction / Market 
System
(Trade Input Source)
2 349 350 A/N [[NYSE]]/[[NYSE]](MKT):
 l O = OCS
 l P = PTP 
 l S = Step Out
 l F = Force([[Broker]] or DMM) 
[[NYSE]] 2: 
 l NB = [[NYSE]] [[Bonds]]
 l BT = [[NYSE]] Blocked 
 l MP = [[NYSE]] Match Point 
Chicago [[Stock Exchange]]: 
 l CH = Trades occurring at 
CHX
 l AW = Trades occurring away 
from CHX
[[NYSE]]:
XNYS = New York or [[NYSE]] 
Alternext US.
[[OTC]]:
 l A = TRF
 l D = Portal
 l E = EACT
 l N = [[NASDAQ]] Step-Outs
 l Q = QSR/ECN                         
 l U = [[NYSE]] AGU
 l X = [[NYSE]] TRF
 l OR = [[OTC]] Reporting Facility
 l AD = Alt Display Facility
[[OTC]]: 
XADF = Alt Display Facility
XNAS = [[NASDAQ]] 
XOTC = Over the Counter 
(See position 109 to 112 for TRF 
reporting)
CORR:
“ “ (space) = External Position 
Movement
M = Internal Position Movement 
CORR: 
COR = Correspondent Clearing
 
(Position 109 – 112)
Currency 3 351 353 A/N USD = US Dollars
[[default]] is USD
USD = US Dollars 
(Position 201 – 203)
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 10

UTCIntradayMRO(02081673)TradeCaptureData 10
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
Order Capacity 1 354 354 A/N [[NYSE]]
A = Not a [[Member]] / [[Member]] 
organization and not an 
individual [[investor]].
C = Program trade, non-index 
arbitrage for the proprietary 
account of a [[Member]]/[[Member]] 
organization or affiliate.
D = Program trade, index 
arbitrage,  for the proprietary 
account of a [[Member]]/[[Member]] 
organization or affiliate.
I = Individual [[investor]], not a 
discretionary or managed 
account.
J = Program trade, index 
arbitrage, for account of 
individual [[investor]].
K = Program trade, non-index 
arbitrage, for account of 
individual [[investor]].
P = Non-[[Program Trading]] for the 
proprietary account of a 
[[Member]]/[[Member]] organization or 
affiliate.
Q = Proprietary trade by a 
[[Member]] on the Floor relating to 
the [[Member]]’s own error.
S = Designated [[Market Maker]]
U = Program trade, index 
arbitrage and agency.
Y = Program trade, non-index 
arbitrage and agency.
 
All other markets
A = Agency
F = Firm
Capacity code 
(Position 104)
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 11

UTCIntradayMRO(02081673)TradeCaptureData 11
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
P = Principal
R = Riskless Principal
V = Mixed
Principal Trade 
Amount
(Gross Trade Amt)
17 355 371 A/N Unit Price x Share Quantity
16 Digits + 1 (period indicating 
two decimal point offset)
Price x Quantity 
Two Decimal Positions
(Position 185 – 200)
Net [[settlement]] 
Amount
(Net Money)
17 372 388 A/N Net [[settlement]] Money (as 
provided by market) 
16 Digits + 1 (period indicating 
two decimal point offset)
(Position 250 – 265)
Don’t Count 
Indicator ([[SEC]] 31 
Fees)
1 389 389 A/N D = Don’t Count 
P = Don’t Count; [[participant]] 
pays
Note: If tag #58 is not reported 
on [[NSCC]] FIX or MQ trade 
capture output, the sell side 
contract amount was included 
(Counted) in Section 31 market 
totals for applicable markets. 
Some markets are not eligible for 
Section 31 processing. As such, 
they are not counted for Section 
31 fees regardless of the Don’t 
Count Indicator value submitted 
on input.  All transactions in the 
following markets are reported 
as blank in the Don’t Count 
Indicator (tag 58) field. 
 
Market 
Code Market Name
060 [[OTC]]
070 OCC
090 OMGEO
100 Correspondent 
Clearing
New field in UTC. 
This information is denoted in the 
Reversal/Correction field of the 
Legacy MRO.
(Position 338)
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 12

UTCIntradayMRO(02081673)TradeCaptureData 12
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
Commission / 
Explicit Fee
9 390 398 A/N Total Explicit Fee or 
Commission Amount 
8 Digits + 1 (period indicating 
two decimal point offset)
Position 339 – 346
Other Fees 7 399 405 A/N Other Fees 
6 Digits + 1 (period indicating 
two decimal point offset)
Position 347 – 352
Taxes 8 406 413 A/N Taxes 
7 Digits + 1 (period indicating 
two decimal point offset)
Position 353 – 359
Accrued Interest 
Amount 
10 414 423 A/N Accrued Interest Amount 
9 Digits + 1 (period indicating 
two decimal point offset)
Position 241 – 249
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 13

UTCIntradayMRO(02081673)TradeCaptureData 13
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
[[Liquidity]] Indicator
(Exchange Rule)
1 424 424 A/N (For [[NYSE]] Executions)
[[Liquidity]] Indicators
1 = Taker
2 = Provider
3 = Blended
4 = Opening/Prior Day Order
5 = Opening
6 = Closing
7 = Closing/MOC/LOC Order
8 = Retail Order Provider 
9 = Retail Order Taker
F = 3rd Party Algo @ [[NYSE]]
G = 3rd Party Algo Away
 
Market Center Values
A = [[NYSE]] MKT (AMEX)
B = [[NASDAQ]] BX
C = National
D = [[NASD]]
M = Chicago
P = ARCA
T = [[NASDAQ]]
X = [[NASDAQ]] PHLX
Y = BATSY
J = Direct Edge A
K = Direct Edge X
(For [[NYSE]] Executions) 
[[Liquidity]] Indicators 
1 = Taker 
2 = Provider 
3 = Blended 
4 = Opening Prior Day Order 
5 = Opening 
6 = Closing 
7 = Closing MOC/ LOC Order 
8 = Specialist 
9 = Odd Lot 
 
[[NYSE]] Only: 
(For Routed Away Orders)
Market Center Values 
A = [[NYSE]] Alternext US 
C = National 
D = [[NASD]] 
F = Executed at [[NYSE]] 
G = Executed at Away Market 
I = ISE 
M = Chicago 
P = Arca 
T = [[NASDAQ]] 
X = Philadelphia 
Z = BATS 
 
(Position 399)
Future Use 1 425 425  Future Use Future Use
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 14

UTCIntradayMRO(02081673)TradeCaptureData 14
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
[[NSCC]] Reject 
Codes
2 426 427 N 0 = Accepted Trade 
1 = Reject Invalid [[participant]] 
Info 
2 = Reject Invalid Trade Date 
3 = Reject Invalid Security 
4 = Reject Invalid Quantity 
5 = Reject Invalid Price 
6 = Reject Invalid Trade Source 
7 = Reject Invalid Market 
8 = Reject Multiple Rejects
9 = Reject Invalid Relationship 
10 = Reject Invalid Explicit Fee 
12 = Reject Invalid Message 
Type 
13 = Reject Invalid Trade Type 
14 = Reject Invalid Sending 
Entity (ineligible for submitted 
market, [[participant]], subsystem) 
15 = Reject Invalid Trade 
Sequence Number 
16 = Reject Invalid Submitted-by 
Indicator 
17 = Reject Invalid Number of 
Sides 
18 = Reject Unknown 
Instrument 
19 = Reject Invalid Introducing 
[[Broker]] 
20 = Reject Invalid 
Executing/Entering [[Broker]]
21 = Reject Invalid [[settlement]] 
Date 
22 = Reject Invalid [[settlement]] 
Type 
23 = Reject Invalid Principal 
Trade Amount 
ØØ = No [[NSCC]] Rejects 
01 = Invalid [[participant]] 
02 = Invalid Trade Date 
03 = Invalid Security 
04 = Invalid Quantity 
05 = Invalid Price 
06 = Invalid Trade Source 
07 = Invalid Trade Originator 
08 = Multiple Rejects 
09 = Invalid Value 
10 = Invalid Explicit Fee 
 
(Position 336 – 337)
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 15

UTCIntradayMRO(02081673)TradeCaptureData 15
UTC Intraday MRO (02081673)
Trade Capture Data – Output Format
Total Length: 477 bytes
Description Length 
(MAX)
StarEnd TypeUTC FIX Values Legacy MRO Values
24 = Reject Invalid Net Settling 
Amount 
25 = Reject Invalid Currency 
Code 
26 = Reject Invalid [[settlement]] 
Days 
27 = Reject Invalid Buy or Sell 
Type Code 
28 = Pend Invalid [[participant]] 
29 = Pend Invalid Relationship 
30 = Pend Invalid Security 
31 = Pend Invalid Sending Entity 
(ineligible for submitted market, 
[[participant]], subsystem) 
32 = Pend Potentially Erroneous
33 = Pend Invalid Affiliate 
Relationship 
50 = Reject Invalid Execution 
Time 
53 = Reject Invalid Affiliate 
Relationship
Filler 50 428 477 A/N Reserved for future use.  
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 16

UTCIntradayMRO(02081673)TradeCaptureData 16
UTC MRO Multicycle Output Times
The National [[securities]] Clearing Corporation ([[NSCC]]), a subsidiary of The Depository Trust & Clearing Corporation 
([[DTCC]]), obtains trade comparison and trade reporting data at regular intervals throughout the business day and 
distributes the output in the form of machine-readable-output (MRO). The following is a schedule of multi-cycle output 
times for the distribution of MRO. All times are US Eastern Time zones.
File Name Approximate Cycle Times Intraday AutoRoute Format
 
 
Universal Trade Capture
9:00 a.m.
 
10:00 a.m.
 
11:00 a.m.
 
Noon
1:00 p.m.
 
2:00 p.m.
 
3:00 p.m.
 
4:00 p.m.
5:00 p.m.
 
6:00 p.m.
 
7:00 p.m.
 
8:00 p.m.
 
9:00 p.m.
 
10:30 p.m.
 
By 1:00 a.m. (last cycle 98)
 
 
02081673
UTCIntradayMRO(02081673)TradeCaptureData-OutputFormat

---

## Page 17

FOR MORE INFORMATION
Email [[DTCC]] Learning at:
corelearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com