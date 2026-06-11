---
title: "Consolidated Trade Summary (CTS) File Layouts"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cts156_cts_file_layouts_2022Mar25.pdf"
pages: 33
size: "426.9 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Consolidated Trade Summary (CTS) File Layouts

**Original File:** [cts156_cts_file_layouts_2022Mar25.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cts156_cts_file_layouts_2022Mar25.pdf)  
**Category:** Other  
**Total Pages:** 33  
**File Size:** 426.9 KB  

---

## Page 1

 
CONSOLIDATED TRADE SUMMARY 
(CTS) 
FILE LAYOUTS 
VERSION 1.9 
MARCH 25, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Info: March 25, 2022 
Publication Code: CTS156 
Service: Consolidated Trade Summary (CTS) 
Title: File Layouts 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Revision History ................................................................................................................................................... 4 
1. Autoroute Product IDs for the Consolidated Trade Summary (CTS) Files  ................................................ 5 
2. Consolidated Trade Summary File Layout .................................................................................................... 6 
3. CTS Layout Description-Summary Record ................................................................................................. 12 
Net Reason Codes............................................................................................................................................13 
Market Codes ....................................................................................................................................................16 
4. CTS Layout Description-Balance Order Record ......................................................................................... 19 
5. Highlights of the Features ............................................................................................................................. 22 
6. CTS Mapping of New Versus Legacy File Layouts–CTS Summary Record ............................................ 23 
7. CTS Mapping of New Versus Legacy File Layouts–Balance Order Record ............................................ 27 
8. CTS Output Schedule .................................................................................................................................... 32 
Cycle 1 ..............................................................................................................................................................32 
Cycle 2 ..............................................................................................................................................................32 
Cycle 3 ..............................................................................................................................................................32 
 

---

## Page 4

File Layouts 
Revision History 4 
REVISION HISTORY 
The following table shows the revision history. 
VERSION DATE AUTHOR NOTES–SECTIONS EDITED 
1.0  Sept. 2015  Janice DiTore  Original  
1.1  Oct. 2015  Janice DiTore  Modified File Layout & Mapping, Added Net Reason Code # 
25 and section for fields eliminated.  
1.2  Dec. 2015  Janice DiTore  Added section numbering,  
Rearranged the file layout & descriptions  
Added Section 8 Output Schedule  
1.3  Jan. 2016  Janice DiTore  Added new Net Reason Code in prep of T+2  
Changed position for WI and Foreign on Trade Summary 
layout  
1.4  Feb. 2016  Janice DiTore  Updated CTS Layout dates and record [[ID]] fields changing 
“Type” from N to A/N  
1.5  March 2016  Janice DiTore  Added of [[CUSIP]] to file layouts and expanded to 300 bytes  
1.6  March 2016  Janice DiTore  Highlighted T+2 applicable requirements in yellow.  
Added Net Reason Codes 13, 14, and 54 for T+2. See Net 
Reason Codes. 
1.7  June 2017  Tim Garrett  Updated CSV Cash Adjustment, Debit/Credit Indicator, and 
Cash Adjustment Amount descriptions throughout. 
1.8 October 2020 Lou Lepore Updated the market codes. 
1.9 March 2022 Pete Smith Updated the net reason codes. 
 

---

## Page 5

File Layouts 
Autoroute Product IDs for the Consolidated Trade Summary (CTS) Files 5 
1. AUTOROUTE PRODUCT IDS FOR THE 
CONSOLIDATED TRADE SUMMARY (CTS) FILES 
The following table provides the autoroute product IDs for CTS files: 
File Production [[ID]] Test [[ID]] 
CTS Machine Readable Output (MRO) File 02042339 02982339 
CTS Comma Separated Values (CSV) Formatted File 02042340 02982340 
Note: 
The CSV file uses the same layout but contains commas between each field. 
To subscribe to the daily CTS files, contact Connectivity, Activation, and Production Support at: 1-888-382-
2721. Select [[Option]] 5, and then [[Option]] 1. 

---

## Page 6

File Layouts 
Consolidated Trade Summary File Layout 6 
2. CONSOLIDATED TRADE SUMMARY FILE LAYOUT 
Both the MRO and CSV formatted files share the same layout to give flexibility to our clients in selecting which 
version to use. The layout fields have been re-ordered. 
Consolidated Trade Summary 
AutoRoute Product [[ID]] # 02042339 Production (# 02982339 Test) Machine Readable Output (MRO) 
AutoRoute Product [[ID]] # 02042340 Production (# 02982340 Test) Comma Separated Values (CSV) 
Field Name  Length  Start  End  Type  Description/Value  
CTS Report Date  8  1  8  A/N  CTS Report Date  
Format-CCYYMMDD  
CTS Report Cycle  1  9  9  N  CTS Report Cycle number. 
• 1 = Main  
• 2 = Supplemental 1  
• 3 = Supplemental 2  
[[participant]] [[ID]]  8  10  17  A/N  [[participant]] [[ID]]  
[[settlement]] Date  8  18  25  A/N  [[settlement]] Date  
Format-CCYYMMDD  
Depository  
([[settlement]] Location)  
2  26  27  A/N  Indicates where the trade is expected to be 
settled  
• D = [[DTC]] ([[default]])  
• Blank = other (future use)  
Currency  3  28  30  A/N  Currency Indicator: USD = US Dollar  
ISIN  12  31  42  A/N  ISIN  
Record Type  2  43  44  A/N  SR – CTS Summary Record  
Summary Record [[ID]]  12  45  56  A/N  Unique [[ID]] that identifies the CTS Summary 
record.  
Contra [[participant]] [[ID]]  8  57  64  A/N  The [[DTCC]] [[participant]] [[ID]] of the CONTRA 
clearing firm.  
• The Contra is included only for bilateral and 
TFT items. 
• [[CNS]] and Multi-lateral records. This field 
contains spaces  
Netting Type  1  65  65  A/N  Netting type indicator:  
C = [[CNS]] 
M = Non-[[CNS]] Multilateral Netting 
B = Non-[[CNS]] Bilateral Netting 
T = Trade for Trade  
Net Reason Code  3  66  68  A/N  Net Reason Code explains the netting reason. 
See Net Reason Codes. 

---

## Page 7

File Layouts 
Consolidated Trade Summary File Layout 7 
Consolidated Trade Summary 
AutoRoute Product [[ID]] # 02042339 Production (# 02982339 Test) Machine Readable Output (MRO) 
AutoRoute Product [[ID]] # 02042340 Production (# 02982340 Test) Comma Separated Values (CSV) 
Field Name  Length  Start  End  Type  Description/Value  
[[CNS]] Indicator  1  69  69  A/N  Code that indicates [[CNS]] eligibility. 
• C = [[CNS]]  
• N = Non-[[CNS]] 
Guarantee Indicator  1  70  70  A/N  G = Guaranteed  
N = Not Guaranteed  
Market Code  3  71  73  A/N  Market on which the trade was executed. 
See Market Codes. 
Purchase item count  9  74  82  N Number of purchase trades  
Purchase Share Quantity  13  83  95  N  Quantity being bought  
Purchase Amount  17  96  112  N  Purchase Contract Amount  
Format–999999999999999V99  
Format–15 integer & 2 decimal positions; decimal 
is implied  
Example-12345678901234512 = 
123456789012345[.]12  
Sell item count  9  113  121  N  Number of sell trades  
Sell Share Quantity  13  122  134  N  Quantity of [[shares]] being sold.  
Sell Amount  17  135  151  N  Sell Contract Amount  
Format–999999999999999V99  
Format–15 integer & 2 decimal positions; decimal 
is implied  
Example-12345678901234512 = 
123456789012345[.]12  
Trade Date  8  152  159  A/N  Trade Date  
Format-CCYYMMDD  
[[NSCC]] Receive Date  8  160  167  A/N  Date the trade is received and  
validated by [[NSCC]]  
Format-CCYYMMDD  
As-Of Indicator  1  168  168  A/N  Indicates As-Of trade:  
• Space = Not Applicable  
• T = Trade Date As-Of  
• S = [[settlement]] Date As-Of  
Symbol  15  169  183  A/N  Trading symbol used by marketplace  
[[CUSIP]]  9  184  192  A/N  [[CUSIP]]  
[[Stock]]/Bond Indicator  1  193  193  A/N  S = [[Stock]]  

---

## Page 8

File Layouts 
Consolidated Trade Summary File Layout 8 
Consolidated Trade Summary 
AutoRoute Product [[ID]] # 02042339 Production (# 02982339 Test) Machine Readable Output (MRO) 
AutoRoute Product [[ID]] # 02042340 Production (# 02982340 Test) Comma Separated Values (CSV) 
Field Name  Length  Start  End  Type  Description/Value  
B = Bond  
Foreign Indicator  1  194  194  A/N  Foreign Indicator: 
• Y = Security is Foreign  
• N = Security is Domestic 
When Issued Indicator  1  195  195  A/N  Trade is [[secondary market]] or for a not yet issued 
security. 
• 0 = Regular way  
• 1 = When Issued  
• 2 = [[syndicate]] Takedown  
Step In/Out Indicator  1  196  196  A/N  Step In/Out indicator:  
• 0 = [[default]], (Not Applicable)  
• 2 = Step In  
• 3 = Step Out  
Trade Type Code  1  197  197  A/N  0 = Regular Way  
1 = Cash Trade  
2 = Next Day Settling Trade  
6 = [[Seller]]’s [[Option]]  
FILLER  103  198  300  A/N  Filler 
CTS Report Date  8  1  8  A/N  Same as the CTS Report Date. 
Format–CCYYMMDD  
Report Cycle  1  9  9  A/N  CTS Report Cycle  
• 1 = Main  
• 2 = Supplemental 1  
• 3 = Supplemental 2  
[[participant]] [[ID]]  8  10  17  A/N  Balance Order [[participant]] [[ID]]  
[[settlement]] Date  8  18  25  A/N  [[settlement]] Date in CCYYMMDD format  
Depository  
([[settlement]] Location)  
2  26  27  A/N  Indicates where the trade is expected to be 
settled. 
• D = [[DTCC]] ([[default]])  
• Blank = other (future use)  
Currency code  3  28  30  A/N  Currency Indicator  
USD = US Dollar  
ISIN  12  31  42  A/N  ISIN  
Record Type  2  43  44  A/N  BO = Balance Order Record  
Balance Order  
Record [[ID]]  
12  45  56  A/N  Unique [[ID]] for CTS Balance Order record that 
provides an association to CTS Trade Summary 
records.  

---

## Page 9

File Layouts 
Consolidated Trade Summary File Layout 9 
Consolidated Trade Summary 
AutoRoute Product [[ID]] # 02042339 Production (# 02982339 Test) Machine Readable Output (MRO) 
AutoRoute Product [[ID]] # 02042340 Production (# 02982340 Test) Comma Separated Values (CSV) 
Field Name  Length  Start  End  Type  Description/Value  
Contra [[participant]] [[ID]]  8  57  64  A/N  Balance Order Contra [[participant]] [[ID]]  
Netting Type  1  65  65  A/N  Netting type indicator:  
• M = Non-[[CNS]] Multilateral Netting 
• B = Non-[[CNS]] Bilateral Netting  
• T = Non-[[CNS]] Trade for Trade  
Net Reason Code  3  66  68  A/N  Net Reason Code explains the netting reason. 
See Net Reason Code.  
Receive Order/Deliver 
Order indicator  
2  69  70  A/N  [[DO]] = Deliver Order settles quantity and cash  
DC = Deliver Order settles cash adjustment only  
DS = (reserved for future use)  
RO = Receive Order settles quantity and cash  
RC = Receive Order settles cash adjustment only  
RS = (reserved for future use) 
Balance Order Control 
Number  
12  71  82  A/N  Unique [[ID]] that identifies the Balance Order 
between receiver and deliverer.  
Illogical netting code  1  83  83  A/N  Identifies Illogical bilateral netting result. 
• Space = Not applicable  
• 1 = [[shares]] and money in the same direction  
• 2 = [[outstanding shares]], zero money  
Auto Delivery indicator  1  84  84  A/N  Auto- Delivery Indicator:  
• Y = Obligation sent to [[DTC]] [[settlement]] via 
auto delivery  
• N = Auto Delivery not used  
Purchase Quantity  13  85  97  N  Quantity to be received,  
Zero if no [[shares]]  
Sell Quantity  13  98  110  N  Quantity to be delivered  
Zero if no [[shares]]  
Debit Amount  17  111  127  N  Amount to be paid for the purchased [[shares]], 
Zero if no amount  
Format–999999999999999V99  
Format–15 integer & 2 decimal positions; decimal 
is implied  
Example–12345678901234512 = 
123456789012345[.]12  
Credit Amount  17  128  144  N  Amount to be paid for the [[shares]] sold  
Zero if no amount  

---

## Page 10

File Layouts 
Consolidated Trade Summary File Layout 10 
Consolidated Trade Summary 
AutoRoute Product [[ID]] # 02042339 Production (# 02982339 Test) Machine Readable Output (MRO) 
AutoRoute Product [[ID]] # 02042340 Production (# 02982340 Test) Comma Separated Values (CSV) 
Field Name  Length  Start  End  Type  Description/Value  
Format–999999999999999V99  
Format–15 integer & 2 decimal positions; decimal 
is implied  
Example–12345678901234512 = 
123456789012345[.]12  
Price  12  145  156  N  Price per Share  
Format–999999V999999  
Format–6 integer & 6 decimal positions; decimal 
is implied  
Example–123456123456 = 123456[.]123456  
Earliest Trade Date  8  157  164  A/N  Earliest Trade Date Included  
Format- CCYYMMDD  
[[CUSIP]]  9  165  173  A/N  [[CUSIP]]  
[[Stock]]/Bond Indicator  1  174  174  A/N  S = [[Stock]]  
B = Bond  
Foreign Indicator  1  175  175  A/N  Foreign Indicator  
Y = Security is Foreign  
N = Security is Domestic 
When Issued Indicator  1  176  176  A/N  Indicates that the trade is for not yet issued 
security. 
• 0 = Regular way  
• 1 = When Issued  
• 2 = [[syndicate]] takedown  
Cash Adjustment Code  2  177  178  A/N  Cash Adjustment [[settlement]] Code:  
Space = No Cash Adjustment  
02 = Guaranteed [[obligations]];  
23 = Not Guaranteed [[obligations]].  
Cash Adjustment  
Debit/Credit Indicator  
1  179  179  A/N  Cash Adjustment Indicator  
- = Debit  
+ = Credit (Amount greater than or equal to zero)  
Note: For the CSV file version, this field is 
combined with the Cash Adjustment Amount (for 
example, +000000000004824.01)  

---

## Page 11

File Layouts 
Consolidated Trade Summary File Layout 11 
Consolidated Trade Summary 
AutoRoute Product [[ID]] # 02042339 Production (# 02982339 Test) Machine Readable Output (MRO) 
AutoRoute Product [[ID]] # 02042340 Production (# 02982340 Test) Comma Separated Values (CSV) 
Field Name  Length  Start  End  Type  Description/Value  
Cash Adjustment Amount  17  180  196  N  Cash Adjustment value amount  
(Zero if Not Applicable, no Cash Adjustment)  
Format–999999999999999V99  
Format–15 integer & 2 decimal positions; decimal 
is implied  
Example-12345678901234512 = 
123456789012345[.]12  
Note: For the CSV file version, this field is 
combined with the Cash Adjustment Debit/Credit 
Indicator (for example, +000000000004824.01)  
FILLER  104  197  300  A/N  Filler 

---

## Page 12

File Layouts 
CTS Layout Description-Summary Record 12 
3. CTS LAYOUT DESCRIPTION-SUMMARY RECORD 
CTS Report Date–the business date the CTS Summary is produced. 
CTS Report Cycle–three occurrences of the CTS Summary are created daily. Beginning with the main CTS at 
21:00 ET, (cycle 1); then the first supplemental at 24:00 ET, (cycle 2); ending with the CTS at 12:00 ET, also 
called the supplemental 2, (cycle 3). 
CTS Cycle  Common Name  Approximate Time of Distribution  
1  Main CTS  On or before 21:00 ET  
2  Supplemental 1  On or before 24:00 ET  
3  Supplemental 2  On or before 12:00 ET  
 
[[participant]] [[ID]]–the numerical [[NSCC]] account number for the owner of the trade record. 
[[settlement]] Date–date the trade is expected to settle at a depository. 
Depository–all records are currently populated with the [[default]] of [[DTC]]. As a possibility for expansion, a blank 
will be introduced to represent that [[settlement]] is expected at a depository other than [[DTC]]. 
Currency–all records are currently defaulted to US Dollars. 
ISIN–Abbreviation for International [[securities]] Identification Number. Each ISIN contains a country code 
followed by the identifier. 
Record Type–defines the string of information as the CTS Summary Record, whereby multiple like trades 
have been summarized. 
Summary Record [[ID]]–a unique alpha/numeric identifier for the Trade Summary Record. 
Contra [[participant]]–the [[NSCC]] account number for the counterparty. It will appear on a bilateral netted 
obligation or trade for trade record. Spaces will appear in this field for either the [[CNS]] or Non- [[CNS]] multi-
laterally netted [[obligations]]. 
Netting Type–defines the processing of the trade summary record as either sent to [[CNS]], or one of the Non 
[[CNS]] categories of multi-lateral net, bilateral net or trade for trade [[settlement]]. 
Net Reason Code–based on the criteria of the trade, such as a [[Broker]] submitted trade for trade designation, 
and whether the underlying security is eligible for the Continuous Net [[settlement]] ([[CNS]]) accounting processing 
at [[NSCC]], or requires special processing, and if the time of receipt and acceptance by [[NSCC]]’s Universal Trade 
Capture (UTC) system. 
Scenarios have been assigned a specific identifier to define the clearance methodology applied to the 
[[obligations]]. (Nonstandard has been defined as trades submitted using the indicator for Cash, Next Day , or 
[[Seller]]’s [[Option]].) 

---

## Page 13

File Layouts 
CTS Layout Description-Summary Record 13 
Net Reason Codes 
• C = [[CNS]] 
• M = Non-[[CNS]] Multilateral Netting 
• B = Non-[[CNS]] Bilateral Netting 
• T = Trade-for-Trade 
Type of 
Net  
Net 
Reason 
Code  
Netting Reason Code–
Short Name  
Full Description of Net Reason Code  
C 001  [[CNS]]–1D/2D  [[CNS]] eligible security received prior to [[settlement]] date will be sent to 
[[CNS]] for [[settlement]] and guaranteed.  
C 002  [[CNS]]–SD  [[CNS]] eligible security received on [[settlement]] date will be sent to 
[[CNS]] for [[settlement]] and guaranteed.  
C 003  [[CNS]]–OCC Trades  [[CNS]] eligible OCC trade received prior to [[settlement]] date which is 
required to be reported after RISK requirements are satisfied.  
M  010  Multi-lateral Net  
Non-[[CNS]]  
Non-[[CNS]] security submitted at least two days prior to [[settlement]] 
date is eligible to be priced and allocated as a multi-laterally netted 
guaranteed balance order.  
M  011  Multi-lateral Net  
Non-[[CNS]] OCC Trades  
Non-[[CNS]] OCC trade submitted on or 1 day before [[settlement]] date 
is eligible to be priced and allocated as a multi-laterally netted 
guaranteed balance order.  
CTS Cycle 3 will include all as 1D  
M  012  Multi-lateral Net  
Non-[[CNS]]  
Netting across multiple Multi-lateral net reason codes  
M  013  Multi-lateral Net  
[[CNS]] eligible  
Undergoing Reorg Tender 
Offer  
1D Cycle 3 only  
[[CNS]] eligible security which is undergoing reorganization tender offer 
within the protect period and is settling within one day.  
It will be multi-laterally netted and guaranteed.  
Only on CTS Cycle 3  
M  014  Multi-lateral Net  
OCC trade-[[CNS]] eligible 
Undergoing Reorg Tender 
Offer  
A trade originated on the OCC market that is a [[CNS]] eligible security 
which is undergoing reorganization tender offer within the protect 
period and is settling within one day. It will be multi-laterally netted 
and guaranteed. Only on CTS Cycle 3  
B  020  Bilateral Net– 
[[Equity]] Special 1D/2D  
[[Equity]] security is marked as Non-[[CNS]] special trade processing 
received 1 or more days before [[settlement]] date. Transactions will be 
bilaterally netted, not guaranteed.  
B  021  Bilateral Net– 
Bond Special 1D/2D  
Bond security is marked as Non-[[CNS]] special trade processing 
received 1 or more days before [[settlement]] date. Transactions will be 
bilaterally netted, not guaranteed.  
B  022  Bilateral Net– 
Non-[[CNS]] 1D  
Non-[[CNS]] security submitted as: Next Day or [[Seller]]’s [[Option]] to UTC 
was received 1 or more days before [[settlement]] date. Transactions 
will be bilaterally netted, not guaranteed.  

---

## Page 14

File Layouts 
CTS Layout Description-Summary Record 14 
Type of 
Net  
Net 
Reason 
Code  
Netting Reason Code–
Short Name  
Full Description of Net Reason Code  
B  023  Bilateral Net– 
Non-[[CNS]] Non-Std. 2D  
Non-[[CNS]] security submitted as: Next Day or [[Seller]]’s [[Option]] to UTC 
was received at least one day before [[settlement]] date. Transactions 
will be bilaterally netted, not guaranteed. 
 
B  024  Bilateral Net– 
Foreign > 1D  
Foreign security is received 1 or more days before [[settlement]] date. 
Transactions will be bilaterally netted, not guaranteed.  
B  025  Bilateral Net-Non-[[CNS]] 
Bond > SD  
Non-[[CNS]] Security submitted prior to [[settlement]] day. Transactions 
will be bilaterally netted, not guaranteed.  
B  026  Bilateral Net-Multiple 
reasons  
The obligation fits multiple net reason codes.  
T  040  TFT–[[Broker]] Submitted 
Domestic  
Original domestic security trade was submitted with the request to 
process as trade for trade.  
T  041  TFT–[[Broker]] Submitted 
Foreign  
Original trade record in a foreign security was submitted with the 
request to process as trade for trade. It will be processed as trade 
for trade, not guaranteed.  
T  042  TFT–[[Equity]] Special SD  The [[Equity]] security has special trade processing identified on the 
master file and was submitted on [[settlement]] day. It will be 
processed as trade for trade, not guaranteed.  
T  043  TFT–Bond Special SD  The bond security has special trade processing identified on the 
master file and was submitted on [[settlement]] day. It will be 
processed as trade for trade, not guaranteed.  
T  044  TFT–Non-[[CNS]] SD  The security is not eligible for [[CNS]] and was submitted on [[settlement]] 
day. It will be processed as trade for trade, not guaranteed.  
T  045  TFT–Non-[[CNS]] Non-Std. 
1D/SD  
The security is not eligible for [[CNS]] and was submitted as: Cash, 
Next Day or [[Seller]]’s [[Option]] either one day or on [[settlement]] day. It 
will be processed as trade for trade, not guaranteed.  
T  046  TFT–Foreign 1D  The security is known as foreign and settles in one day. It will be 
processed as trade for trade, not guaranteed.  
T  047  TFT–Non-[[CNS]] Muni  The security is a municipal, not eligible for [[CNS]].  
It will be processed as trade for trade, not guaranteed.  
T  048  TFT–[[syndicate]] Takedown 
Municipal  
The trade is a municipal when and as if issued security and part of a 
[[syndicate]] takedown, not eligible for [[CNS]]. It will be processed as 
trade for trade, not guaranteed.  
T  049  TFT–Mixed/Odd Lots  The bond quantity is determined to be either an odd lot or mixed lot. 
It will be processed as trade for trade, not guaranteed.  
T  050  TFT–Non-[[CNS]] Sub-penny 
priced [[Bonds]]  
The bond price calculates to be less than one US cent per unit. It will 
be processed as trade for trade, not guaranteed.  
T  051  TFT–Brokers ineligible for 
[[CNS]]  
Either one or both parties to the trade are not eligible for [[CNS]] 
processing. It will be processed as trade for trade, not guaranteed. 

---

## Page 15

File Layouts 
CTS Layout Description-Summary Record 15 
Type of 
Net  
Net 
Reason 
Code  
Netting Reason Code–
Short Name  
Full Description of Net Reason Code  
T  052  TFT–[[CNS]] under Reorg 
Tender Offer 1D/SD  
A [[CNS]] eligible trade was received on or one day before [[settlement]] 
date while security was undergoing a reorganization tender offer. It 
will be processed as trade for trade, not guaranteed.  
CTS Cycle 1 or 2 will contain 1D.  
T  053  TFT–[[CNS]] Non-Std. Under 
[[Dividend]] 1D/SD  
The [[CNS]] eligible trade was submitted as: Cash, Next Day or [[Seller]]’s 
[[Option]], on or one day before [[settlement]] date issuing dividends. It 
will be processed as trade for trade, not guaranteed.  
T  054  TFT–[[CNS]] Non-Std. under 
Reorg Tender Offer 1D/SD  
The [[CNS]] eligible trade was submitted as: Cash, Next Day or [[Seller]]’s 
[[Option]], one day before or on [[settlement]] date undergoing a 
reorganization tender offer. It will be processed as trade for trade, 
not guaranteed.  
T 055 TFT, Non-[[CNS]] [[ETF]] CR/RD 
 
All Fixed Income and [[Equity]] components originating from the [[ETF]] 
market (920) assigned as TFT will be reported with the locked in 
counterparty identified from the order. No netting will be applied. 
T  099  TFT- Undefined  
Net Reason Code  
The transaction was not identified by any other scenario defined on 
this chart. It will be processed as trade for trade, not guaranteed.  
T 100 Non-Stl, Cash Trade 
missed cut off 
Not on CTS. 
SDS trade that missed the 11:30 ET cutoff for CTS cycle 3, reported 
only on UTC. 
T 101 Non-Stl, ETMF Report Only 
Trade 
Not on CTS. 
Exchange Traded Mutual Fund, reported only on UTC. 
T 102 Non-STL, Trade Pending in 
UTC Edit 
Not on CTS.  
Trade pended in the UTC edit. 
T 103 Non-STL, Trade Rejected Not on CTS UTC rejected the trade. 
 
The hierarchy to determine the Net Reason Code is as follows: 
• Was the trade submitted with Special Trade for Trade Processing? 
• Are any or both parties to the trade a Comparison only [[Member]] of [[NSCC]]? 
• Is the [[CNS]] eligible trade that was submitted as Cash or Next Day [[settlement]] undergoing a Reorganization 
Tender Offer or [[Dividend]] Distribution? 
• Is the trade part of a municipal [[syndicate]] takedown? 
• Is the trade quantity size defined as an odd lot or mixed lot? 
• Does the price on the bond trade calculate to be less than one US cent per bond unit? 
• Is the trade eligible for [[CNS]]? 
• Is the security identified as a foreign (non-U.S.)? 
• Is the non-[[CNS]] trade a municipal security? 
• Does the non-[[CNS]] trade have a security requiring special trade processing as identified on the security 
master file? 

---

## Page 16

File Layouts 
CTS Layout Description-Summary Record 16 
• Was the trade submitted as non-standard [[settlement]] using the indicator for: Cash, [[Seller]]’s [[Option]] or Next 
Day [[settlement]] trade? 
• Was the trade submitted to Universal Trade Capture on [[settlement]] date after the “Cash cutoff?” Then it 
will only appear on the UTC Trade Contracts output, not the Consolidated Trade Summary.  
 
[[CNS]] Indicator–designate each record as [[CNS]] eligible or non-[[CNS]]. 
Guarantee Indicator–denotes the trade record as guaranteed or not guaranteed. 
• [[CNS]] trades are guaranteed until settled. 
• Non-[[CNS]] trades are either guaranteed or not guaranteed. 
o Non-[[CNS]] guaranteed means the trade was included in multi-lateral netting. 
o Non-[[CNS]] not guaranteed trades are made up of bilaterally netted trades and trades settling trade for 
trade. 
Market Codes 
The market code denotes the marketplace of execution where the trade originated. The following table 
provides the market codes. 
Market Code Market Description 
FLP UNIVERSAL FLIPS 
010 [[New York Stock Exchange]] 
020 [[NYSE]] MKT 
025 [[NYSE]] [[Bonds]] 
030 [[NYSE]] ARCA 
040 CHICAGO [[Stock Exchange]] 
060 OVER THE COUNTER 
070 OPTIONS CLEARING CORP 
080 [[NYSE]] NATIONAL 
090 ITP ([[Prime Broker]]) 
100 CORRESPONDENT CLEARING 
110 [[NASDAQ]] 
130 BATS BZX 
135 BATS BYX 
140 [[NASDAQ]] OMX BX 
145 [[NASDAQ]] OMX PHLX 

---

## Page 17

File Layouts 
CTS Layout Description-Summary Record 17 
Market Code Market Description 
150 DIRECT EDGE EDGA 
160 DIRECT EDGE EDGX 
170 IEX EXCHANGE 
185 Long Term [[Stock Exchange]] 
190 MIAX Pearl Equities Exchange 
195 Members Exchange 
910 RTTM CORPORATE [[Bonds]] 
911 RTTM MUNI [[Bonds]] 
912 RTTM [[UIT]] 
920 EXCHANGE TRADED FUNDS 
 
Purchase Item Count–the numerical count of purchase trades that make up the CTS Summary Record.  
Purchase Quantity–the aggregate purchase quantity. 
Purchase Amount–the aggregate purchase money amount. 
Sell Item Count–the numerical count of sell trades that make up the CTS Summary Record. 
Sell Quantity–the aggregate of sell quantities. 
Sell Amount–the aggregate sell contract amount. 
Trade Date–date the trade was executed in the marketplace as defined by the submitter.  
[[NSCC]] Receive Date–date the trade is received and validated by the [[NSCC]] Universal Trade Capture (UTC) 
system. 
As of Indicator–trade received was submitted with as of attributes. 
• T- the receipt date at [[DTCC]] was after trade date. 
• S- the [[settlement]] date has been changed by either a trade capture or clearance system at [[DTCC]].  
o The same day settling trade may have been received too late to be included in today’s [[settlement]] 
cycle; therefore, it is assigned the next available [[settlement]] date. 
o The trade received by UTC today has a [[settlement]] date in the past; therefore, the next available 
[[settlement]] date is assigned. 
o The delivery date and [[settlement]] date on a trade submitted to the CMU RTTM system [[DO]] not equal.  
  

---

## Page 18

File Layouts 
CTS Layout Description-Summary Record 18 
Symbol–the trading symbol used in the marketplace of execution. The field will be expanded to include the 
suffix information. 
[[CUSIP]]–abbreviation for Committee on Uniform Security Identification Procedures; which is a unique identifier  
assigned for each security. 
[[Stock]]/Bond Indicator–denotes the security as a [[Stock]] ([[Equity]]) or bond (fixed income). 
Foreign Indicator–the [[DTCC]] security master file knows the security as a foreign (non-domestic) issue. 
When Issued Indicator –denotes that the security was received as either a when (and as if) issued, or a when 
distributed security. The [[DTCC]] security master file will note this security as in original issuance status.  
Step in/out Indicator–the step in or step out indictor is as shown on the UTC contract sheets. The step in/out 
indicator is not criteria for netting and is only available on the summarized trade data. This step in/out indicator 
is used for [[Equity]] market trades only. 
Trade Type Code–indicates how the trade was submitted to UTC: 
• Regular Way–using the common standard for [[settlement]], 
• Cash–date of receipt equals [[settlement]] date, 
• Next Day–trade received one day prior to [[settlement]] date, 
• [[Seller]]’s [[Option]]/Delayed Delivery is for an extended [[settlement]] period. 

---

## Page 19

File Layouts 
CTS Layout Description-Balance Order Record 19 
4. CTS LAYOUT DESCRIPTION-BALANCE ORDER 
RECORD 
CTS Report Date–The balance order issue date defines the processing date on which the receive order or 
deliver order was created. 
CTS Report Cycle–three occurrences of the CTS Summary are created daily. Beginning with the main CTS at 
21:00 ET, (cycle 1); then the first supplemental at 24:00 ET, (cycle 2); ending with the CTS at 12:00 ET, also 
called the supplemental 2, (cycle 3). 
CTS Cycle  Common Name  Approximate Time of Distribution  
1  Main CTS  On or before 21:00 ET  
2  Supplemental 1  On or before 24:00 ET  
3  Supplemental 2  On or before 12:00 ET  
 
[[participant]] [[ID]]–the numerical [[NSCC]] account number for the owner of the trade record. 
[[settlement]] Date–date the trade is expected to settle at a depository. 
Depository–all records are currently populated with the [[default]] of [[DTC]]. As a possibility for expansion, a blank 
will be introduced to represent that the [[settlement]] location is expected to be at a depository other than [[DTC]].  
Currency–all records are currently defaulted to US Dollars. 
ISIN–Abbreviation for International [[securities]] Identification Number. Each ISIN contains a country code 
followed by the identifier. 
Record Type–Balance Order Record resulting from netting and allotting. 
Balance Order Record [[ID]]–unique alpha numeric identifier for the Balance Order record. 
Contra [[participant]]– the [[NSCC]] account number of the counterparty on the Receive/Deliver Order. 
Netting Type–processing of the trade summary record be sent to [[CNS]], included in a multi-lateral net, bilateral 
net or remain trade for trade. 
Net Reason Code–based on the criteria of the trade, such as a [[Broker]] submitted trade for trade designation, 
and whether the underlying security is eligible for the Continuous Net [[settlement]] ([[CNS]]) accounting processing 
at [[NSCC]], or requires special processing, and if the time of receipt and acceptance by [[NSCC]]’s Universal Trade 
Capture (UTC) system. See Net Reason Codes. 
  

---

## Page 20

File Layouts 
CTS Layout Description-Balance Order Record 20 
Receive Order/Deliver Order Indicator–specifies what should be settled: 
• RO – Receive Order made up of [[securities]] to be received and cash adjustment.  
• [[DO]] – Deliver Order made up of [[securities]] and the cash adjustment. 
• RC – Receiver is to settle only a cash adjustment, 
• DC – Deliverer is only settling a cash adjustment, 
• RS – (Reserved for future use), 
• DS – (Reserved for future use). 
 
Balance Order Control Number–The balance order control number is a unique identifier created and 
assigned by [[DTCC]] for each receive order and deliver order. A Julian date is imbedded in the balance order 
control number. 
Illogical Netting Code–identifies that the bilateral netting process results in an illogical combination of quantity 
and value. 
• Quantity and money amount are either both debit or both credit. 
• Quantity results in [[outstanding shares]] with no value amount. 
 
Auto Delivery Indicator–notes whether the deliverer utilizes the Automated Delivery Order process to send 
the obligation to [[DTC]] [[settlement]]. 
Balance Order Quantity–the security quantity of the receive order or deliver order. Only whole number 
quantities will appear on the CTS. Fractions are not included. 
Purchase Quantity 
• Quantity to be received 
• If there are no [[shares]], the field will be populated with zero. 
 
Sell Quantity 
• Quantity to be delivered 
• If there are no [[shares]], the field will be populated with zero. 
 
Debit Amount–amount of the purchase, (Receive Order). 
• If there is no amount, the field will be populated with zero. 
 
Credit Amount–amount paid for the [[shares]] sold, (Deliver Order). 
• If there is no amount, the field will be populated with zero. 
  

---

## Page 21

File Layouts 
CTS Layout Description-Balance Order Record 21 
Price–The price per share or unit used to re-price the multi-laterally netted [[obligations]]. 
Earliest Trade Date–The trade date on a receive order or deliver order will be the earliest date in the grouping 
that is netted. 
[[CUSIP]]–abbreviation for Committee on Uniform Security Identification Procedures; which is a unique identifier 
assigned for each security. 
[[Stock]]/Bond Indicator–denotes the security as a [[Stock]] ([[Equity]]) or bond (fixed income). 
Foreign Indicator–the [[DTCC]] security master file knows the security as a foreign (non-domestic) issue or 
domestic (U.S.). 
When Issued Indicator–denotes that the security was received as either a when (and as if) issued, or a when 
distributed security. The [[DTCC]] security master file will note this security as in original issuance status or 
[[syndicate]] takedown, if applicable. 
Cash Adjustment Code 
• 02–[[DTC]] Line Code for Non-[[CNS]], guaranteed cash adjustments from multi-lateral netting. 
• 23–[[DTC]] Line Code for Non-[[CNS]], not guaranteed cash adjustments resulting from bilateral netting. 
 
Cash Adjustment Value–The value of the cash adjustment sent to [[DTC]] [[settlement]] will be broken out for each 
[[CUSIP]]. 
•  + = Debit. 
• - = Credit (Amount is greater than or equal to zero.) 
 
Cash Adjustment Amount–The U.S. Dollar value of the cash adjustment sent to [[DTC]] [[settlement]] will be 
broken out for each [[CUSIP]]. 

---

## Page 22

File Layouts 
Highlights of the Features 22 
5. HIGHLIGHTS OF THE FEATURES 
• The Consolidated Trade Summary record is a summarized record of trades with like components for 
[[settlement]] Date and [[CUSIP]]. 
• Net reason codes have been assigned to each record to provide transparency about the clearing process.  
• [[settlement]] paths of [[CNS]] or Non-[[CNS]] are clearly stated for each record. 
• A guaranteed or not guaranteed, designation has been assigned to each record. 
• Non-[[CNS]] cash adjustments for [[settlement]] are now separated into the guaranteed (02) and not 
guaranteed (23) [[settlement]] codes. 
• Foreign [[securities]] trades will be included on the CTS on the night of receipt at [[DTCC]]. The foreign 
[[securities]] trades will be bilaterally netted and the earliest trade date associated with the summarized 
record will be shown. 
• Foreign [[securities]] next day [[settlement]] trades that are received after the cycle 1 cutoff (21:00 ET) but 
before the cycle 2 cutoff (24:00 ET) will be included. 
• File output will be in both machine readable (MRO) and comma separated values (CSV) formats. The 
CSV format will be downloadable to Excel. The text based Print Image legacy files have been eliminated.  

---

## Page 23

File Layouts 
CTS Mapping of New Versus Legacy File Layouts–CTS Summary Record 23 
6. CTS MAPPING OF NEW VERSUS LEGACY FILE LAYOUTS–CTS SUMMARY 
RECORD 
The file layouts [[DO]] not map on a one for one basis. The record was changed to improve transparency. The CTS Summary Record does not specifically 
map to the Gross or Net Records from the Legacy MRO file. For a detailed example, login to the [[DTCC]] Learning Center and access the Consolidated 
Trade Summary (CTS) Business Requirements. 
NEW CTS RECORD LAYOUT LEGACY RECORD SOURCE/DIFFERENCES 
FIELD NAME LENGTH DESCRIPTION OLD FIELD NAME LENGTH DESCRIPTION COMMENTS 
CTS Report Date 8 CTS Report Date    New field 
CTS Report Cycle 1 CTS Report Cycle Number 
• 1 = Main 
• 2 = Supplemental 1 
• 3 = Supplemental 2 
   New field 
[[participant]] [[ID]] 8 [[participant]] [[ID]] [[participant]] Clearing 
Number 
4  Field size increasing 
[[settlement]] Date 8 [[settlement]] Date  
CCYYMMDD 
[[settlement]] Date 8 CCYYMMDD Legacy Net Record 
Depository 
([[settlement]] Location) 
2 Indicates where the trade is 
expected to be settled. 
• D = [[DTC]] ([[default]]) 
• Blank = other (future use) 
Depository 2 D = [[DTC]] Legacy Balance Order 
Record 
Currency 3 Currency Indicator 
USD = US Dollar 
Currency 3 USD = US Dollars Legacy Net Record 
ISIN 12 ISIN [[CUSIP]] 
Constant 
9 
3 
[[CUSIP]] 
000 
Use of country code, 
[[CUSIP]], Check digit 
Record Type 2 SR-CTS Summary Record Record Type 2  Legacy Record does not 
specifically map to Gross (G1) 
or Net (N1) 

---

## Page 24

File Layouts 
CTS Mapping of New Versus Legacy File Layouts–CTS Summary Record 24 
NEW CTS RECORD LAYOUT LEGACY RECORD SOURCE/DIFFERENCES 
FIELD NAME LENGTH DESCRIPTION OLD FIELD NAME LENGTH DESCRIPTION COMMENTS 
Summary Record [[ID]] 12 Unique [[ID]] that identifies the 
CTS Summary record. 
   New field 
Contra [[participant]] [[ID]]  8  Contra [[participant]] [[ID]]  Contra Clearing 
Number  
4   Field size increasing  
Netting Type  1  Netting type indicator:  
• C = [[CNS]] 
• M = Non [[CNS]] Multilateral 
Netting 
• B = Non [[CNS]] Bilateral 
Netting 
• T = Trade for Trade  
   New field  
Net Reason Code  3  Net Reason Code explains the 
netting reason. See Net 
Reason Codes.  
   New field  
[[CNS]] Indicator  1  Code that indicates [[CNS]] 
eligibility:  
C = [[CNS]]  
N = Non-[[CNS]]  
[[CNS]]/Non-[[CNS]] 
Indicator  
1  C = [[CNS]]  
N = Non-[[CNS]]  
Legacy Net Record  
Guarantee Indicator  1  G = Guaranteed  
N = Not Guaranteed trade  
   New field  
Market Code  3  Market on which the trade was 
executed. See Market Codes.  
Market Name  2  Name of market of 
execution or source  
Legacy net record  
Purchase item count  9  Number of trades on the buy 
side.  
   New field  
Purchase Quantity  13  Quantity being bought.  Net Buy Quantity  11  99,999,999,999  Legacy Net Record  
Purchase Amount  17  Buy Contract Amount  Net Buy Value  16  99,999,999,999,999.99  Legacy Net Record  
Field size increased  
Sell item count  9  Number of trades on the sell    New field  

---

## Page 25

File Layouts 
CTS Mapping of New Versus Legacy File Layouts–CTS Summary Record 25 
NEW CTS RECORD LAYOUT LEGACY RECORD SOURCE/DIFFERENCES 
FIELD NAME LENGTH DESCRIPTION OLD FIELD NAME LENGTH DESCRIPTION COMMENTS 
side.  
Sell Quantity  13  Quantity being sold.  Net Sell Quantity  11  99,999,999,999  Legacy Net Record  
Sell Amount  17  Sell Contract Amount  Net Sell Value  16  99,999,999,999,999.99  Legacy Net Record  
Field size increased 
Trade Date  8  Trade Date 
CCYYMMDD 
   Legacy Balance Order record  
[[NSCC]] Receive Date  8  Date the trade is received and 
validated by [[NSCC]]  
   New field  
As Of Indicator  1  Indicates as-of trade:  
• Space = Not Applicable  
• T = Trade date as-of  
• S = [[settlement]] date as-of  
As of Indictor  2  AO = As Of  
FN = Foreign [[securities]]  
TT = Trade for Trade  
SP = Special  
Legacy Balance Order record  
specified As Of indicator  
Symbol  15  Trading symbol used by 
marketplace  
   Legacy Print Image only  
[[CUSIP]]  9  [[CUSIP]]      
[[Stock]]/Bond Indicator  1  S = [[Stock]]  
B = Bond  
Bond Indicator  1  Blank = Not Applicable  
0 = Registered  
1 = Coupon Bond  
Legacy net record  
Foreign Indicator  1  Foreign Indicator 
• Y = Security is Foreign 
• N = Security is Domestic  
   Legacy Balance Order record  
Broken out of As Of indicator  
When-Issue Indicator  1  Trade is [[secondary market]] or a 
not yet issued security. 
• 0 = Regular way 
• 1 = When Issued 
• 2 = [[syndicate]] Takedown 
   Legacy Balance Order record  
Broken out of As Of indicator  
Step in/out Indicator  1  Step In/Step out indicator:    New field  

---

## Page 26

File Layouts 
CTS Mapping of New Versus Legacy File Layouts–CTS Summary Record 26 
NEW CTS RECORD LAYOUT LEGACY RECORD SOURCE/DIFFERENCES 
FIELD NAME LENGTH DESCRIPTION OLD FIELD NAME LENGTH DESCRIPTION COMMENTS 
• 0 = Not Applicable 
• 1 = Step-in 
• 2 = Step Out  
Trade Type Code  1  0 = Regular Way 
1 = Cash 
2 = Next Day 
6 = Delayed Delivery, [[Seller]]’s 
[[Option]]  
   New field  
FILLER  103  Filler  Filler  2  Filler  

---

## Page 27

File Layouts 
CTS Mapping of New Versus Legacy File Layouts–Balance Order Record 27 
7. CTS MAPPING OF NEW VERSUS LEGACY FILE LAYOUTS–BALANCE 
ORDER RECORD 
NEW CTS RECORD LAYOUT LEGACY RECORD SOURCE/DIFFERENCES 
FIELD NAME LENGTH DESCRIPTION OLD FIELD NAME LENGTH DESCRIPTION COMMENTS 
CTS Report Date 8 Same as CTS Report Date  
CCYYMMDD  
Trade Date 8 CCYYMMDD Legacy Balance Order 
Report Cycle 1 CTS Report Cycle  
• 1 = Main  
• 2 = Supplemental 1  
• 3 = Supplemental 2  
   New field 
[[participant]] [[ID]] 8 Balance Order [[participant]] [[ID]] [[participant]] Clearing 
Number 
4  Field size increasing 
[[settlement]] Date 8 [[settlement]] Date  
CCYYMMDD  
[[settlement]] Date 8 CCYYMMDD Legacy Balance Order 
Depository 
([[settlement]] Location) 
2 Indicates where the trade is 
expected to be settled  
• D = [[DTCC]] ([[default]])  
• Blank = other (future use)  
   New field 
Currency code 3 Currency Indicator  
USD = US Dollar  
Currency indicator 3 USD = US Dollars Legacy Balance Order 
ISIN 12 ISIN  [[CUSIP]]  
Constant 
9 
3 
[[CUSIP]]  
000  
Legacy Balance Order 
Country code, [[CUSIP]], 
check digit  
Record Type 2 BO-Balance Order Record  Record Type 2 O1 = Balance Order Record Legacy Balance Order 
Balance Order 
Record [[ID]] 
12 
Unique [[ID]] for CTS Balance 
Order record that provides an 
association to the CTS Trade 
   New field 

---

## Page 28

File Layouts 
CTS Mapping of New Versus Legacy File Layouts–Balance Order Record 28 
NEW CTS RECORD LAYOUT LEGACY RECORD SOURCE/DIFFERENCES 
FIELD NAME LENGTH DESCRIPTION OLD FIELD NAME LENGTH DESCRIPTION COMMENTS 
Summary records. 
Contra [[participant]] [[ID]] 8 Balance Order Contra 
[[participant]] [[ID]]  
Contra [[participant]] 4  Field size increasing 
Netting Type 1 Netting type indicator: 
M = Non [[CNS]] Multilateral 
Netting 
B = Non [[CNS]] Bilateral Netting 
T = Non-[[CNS]] Trade for Trade  
   New field 
Net Reason Code  3  Net Reason Code explains the 
netting reason. 
See Net Reason Codes.  
   New field  
Receive 
Order/Deliver Order 
indicator  
2  [[DO]] = Deliver Order settles 
quantity and cash  
DC = Deliver Order settles 
cash adjustment only  
DS = (Reserved for future use)  
RO = Receive Order settles 
quantity and cash  
RC = Receive Order settles 
cash adjustment only  
RS = (Reserved for future use)  
Receive/Deliver  2  RO = Receive Balance Order  
[[DO]] = Deliver Balance Order  
Legacy Balance Order  
Additional values added  
Balance Order 
Control Number  
12  Unique [[ID]] that identifies the 
Balance Order between 
receiver and deliverer.  
Control No. Source  
Control Number  
2  
10  
01 = Record Non-[[CNS]]  
11 = [[OTC]] Foreign  
20 = [[ABS]] ([[NYSE]]) [[Bonds]]  
22 = Corporate [[OTC]] [[Bonds]]  
23 = Municipal [[Bonds]]  
24 = Unit Investment Trust  
Application Assigned Number  
Legacy Balance Order  
Eliminate source code  
Assignment of Control 
Number using unique 
random identifier  

---

## Page 29

File Layouts 
CTS Mapping of New Versus Legacy File Layouts–Balance Order Record 29 
NEW CTS RECORD LAYOUT LEGACY RECORD SOURCE/DIFFERENCES 
FIELD NAME LENGTH DESCRIPTION OLD FIELD NAME LENGTH DESCRIPTION COMMENTS 
Illogical netting code  1  Identifies Illogical bilateral 
netting results: 
1 = [[shares]] and money in the 
same direction 
2 = [[outstanding shares]] Zero 
money  
   New field  
Auto Delivery 
indicator  
1  Auto- Delivery Indicator:  
Y = Client used Auto delivery 
at [[DTC]]  
N = Client did not use Auto 
delivery for this trade  
[[DTC]] Auto [[DO]] 
Indicator  
1  Y = Deliver thru [[DTC]]  
N = Physical Delivery  
Legacy Balance Order 
Specifies only a type of 
delivery at [[DTC]]. 
Purchase Quantity  13  Quantity of [[shares]] to be 
received  
Quantity  11  99,999,999,999  Legacy Balance Order  
Sell Quantity  13  Quantity of [[shares]] to be 
delivered  
Quantity sign  1  + = Debit  
- = Credit  
Legacy Balance Order  
Debit Amount  17  Amount of purchase  Contract Value  16  99,999,999,999,999.99  Legacy Balance Order  
Credit Amount  17  Buy Contract Amount      
   Value Sign  1  + = Debit  
- = Credit  
Legacy Balance Order  
Price  12 Price per Share    New field  
[[CUSIP]]  9  [[CUSIP]]      
Earliest Trade Date  8  Earliest Trade Date Included     New field  
[[Stock]]/Bond Indicator  1  S = [[Stock]]  
B = Bond 
 
 
   New field  

---

## Page 30

File Layouts 
CTS Mapping of New Versus Legacy File Layouts–Balance Order Record 30 
NEW CTS RECORD LAYOUT LEGACY RECORD SOURCE/DIFFERENCES 
FIELD NAME LENGTH DESCRIPTION OLD FIELD NAME LENGTH DESCRIPTION COMMENTS 
Foreign Indicator  1  Foreign Indicator  
• Y = Security is Foreign  
• N = Security is Domestic 
   New field  
Separated identifier from 
Control no.  
When-Issue Indicator  1  Indicates that the trade is for 
not yet issued security 
• 0 = Regular way 
• 1 = When Issued 
• 2 = [[syndicate]] Takedown 
   New field  
Cash Adjustment 
Code  
2  Cash Adjustment [[settlement]] 
Code: 
• 02 = Guaranteed 
[[obligations]] 
• 23 = Not guaranteed 
[[obligations]] 
   New field  
Cash Adjustment 
Debit/Credit Indicator  
1  Cash Adjustment Indicator: 
- = Debit 
+ = Credit 
    
Cash Adjustment 
Value 
17 Cash adjustment Value [[Equity]] Adjustment 
Bond Adjustment 
16 
16 
99,999,999,999,999.99 Legacy Cash Adjustment 
Previously two fields Field 
size increased. 
   [[Equity]] Adjustment 
sign 
Bond Adjustment 
sign 
1 
1 
+  = Debit 
- = Credit 
Legacy Cash Adjustment 
FILLER 103 Filler Filler 89 Filler  
 
  

---

## Page 31

File Layouts 
CTS Mapping of New Versus Legacy File Layouts–Balance Order Record 31 
The following fields have been eliminated from the Legacy file: 
• Eligibility Indicator–specifies change in eligibility or no change in eligibility 
• Bond Indicator–Registered or Coupon Bond 
• [[participant]] Clearing Agent (For municipal [[securities]] only) 
• [[participant]] Executing [[Broker]] (For municipal [[securities]] only) 
• Contra Clearing Agent (For municipal [[securities]] only) 
• Contra Executing [[Broker]] (For municipal [[securities]] only) 
 

---

## Page 32

File Layouts 
CTS Output Schedule 32 
8. CTS OUTPUT SCHEDULE 
Cycle 1 
CTS main output file is produced about 21:00 Eastern Time and contains domestic trades settling within the 
next two days for both [[CNS]] and Non-[[CNS]] [[obligations]] and foreign trades received today (No matter when they 
settle). 
• • 2D = [[obligations]] settling in two days, 
o o [[CNS]] 
o o Non-[[CNS]] multi-laterally netted, bilaterally netted, trade for trade 
• • 1D = [[obligations]] settling in one day 
o o [[CNS]] 
o o Non-[[CNS]] bilaterally netted and trade for trade 
 
Cycle 2 
Issued about 24:00 Eastern Time, the incremental submissions received since the generation of CTS cycle 1.  
Items highlighted in yellow identify changes for Shortened [[settlement]] (T+2). 
• 2D = [[obligations]] settling in two days 
o [[CNS]] 
o Non-[[CNS]] multi-laterally netted, bilaterally netted, trade for trade 
• 1 D = [[obligations]] settling in one day 
o [[CNS]] 
o Non-[[CNS]] multi-laterally netted, bilaterally netted and trade for trade 
• SD = [[obligations]] settling in today’s [[settlement]]. (Not applicable for T+2.) 
o [[CNS]] 
o Non-[[CNS]] trade for trade only 
Cycle 3 
The third cycle is produced about 12:00ET (noon) and will contain same day settling [[obligations]] for either [[CNS]] 
or Non-[[CNS]]. Items highlighted in yellow identify changes for Shortened [[settlement]] (T+2).  
• 1 D = [[obligations]] settling in one day 
o [[CNS]] 
o OCC Trades multi-laterally netted 
o Non-[[CNS]] multi-laterally netted, bilaterally netted and trade for trade 
• SD = [[obligations]] to be settled today 
o [[CNS]] 
o Non-[[CNS]] trade for trade only. 

---

## Page 33

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 