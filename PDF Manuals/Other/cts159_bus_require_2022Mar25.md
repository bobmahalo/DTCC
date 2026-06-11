---
title: "Consolidated Trade Summary (CTS) Business Requirements"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cts159_bus_require_2022Mar25.pdf"
pages: 41
size: "480.3 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# Consolidated Trade Summary (CTS) Business Requirements

**Original File:** [cts159_bus_require_2022Mar25.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cts159_bus_require_2022Mar25.pdf)  
**Category:** Other  
**Total Pages:** 41  
**File Size:** 480.3 KB  

---

## Page 1

CONSOLIDATED TRADE SUMMARY 
(CTS) 
CUSTOMER BUSINESS REQUIREMENTS 
VERSION 2.5 
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
Publication Code: CTS159 
Service: Consolidated Trade Summary (CTS) 
Title: Customer Business Requirements 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Revision History ................................................................................................................................................... 6 
1. About this Guide .............................................................................................................................................. 7 
Contact Us .......................................................................................................................................................... 7 
2. Terminology ...................................................................................................................................................... 8 
3. Domestic Trades with Various [[settlement]] Cycles ...................................................................................... 10 
Domestic When (and As If) Issued or When Distributed [[securities]] Trade .......................................................10 
Domestic [[securities]] Trade With a [[settlement]] Cycle Between 4 and 180 Days...............................................10 
Domestic [[securities]] Trade With 3 Day [[settlement]] ...........................................................................................10 
Domestic [[securities]] Trade with 2 Day [[settlement]] ...........................................................................................11 
Domestic [[securities]] Trade Settling in 1 Day ....................................................................................................11 
Domestic [[securities]] Trade Settling the Same Day ...........................................................................................11 
4. Foreign [[securities]] Trades with Various [[settlement]] Cycles ...................................................................... 12 
Foreign When Issued or When Distributed [[securities]] Trade ...........................................................................12 
Foreign [[securities]] Trade With a [[settlement]] Cycle 4 to 180 Days ...................................................................12 
Foreign [[securities]] Trade With 3 Day [[settlement]] .............................................................................................13 
Foreign [[securities]] Trade With 2 Day [[settlement]] .............................................................................................13 
Foreign [[securities]] Trade Settling in 1 Day .......................................................................................................13 
Foreign [[securities]] Trade Settling Same Day ...................................................................................................14 
Net Reason Codes for Foreign Trades .............................................................................................................14 
5. Trade for Trade (Non-[[CNS]], Not Guaranteed) .............................................................................................. 15 
[[Broker]] Submitted Trade-for-Trade ....................................................................................................................15 
[[participant]] Not Eligible for Netting ....................................................................................................................15 
[[securities]] Not Eligible for Netting .....................................................................................................................16 
6. Change in [[CNS]] Eligibility .............................................................................................................................. 17 
7. Universal Flip .................................................................................................................................................. 18 
8. Netting Processes (Non-[[CNS]]) ....................................................................................................................... 19 
Multi-Lateral Netting ..........................................................................................................................................19 
Pricing Non-[[CNS]], Guaranteed Transactions ....................................................................................................19 

---

## Page 4

 
 
Bilateral Netting .................................................................................................................................................20 
9. Data Elements................................................................................................................................................. 21 
Field Names and Values ...................................................................................................................................21 
[[participant]] – (8 Bytes) .....................................................................................................................................21 
Market Code – (3 Bytes) .................................................................................................................................21 
Symbol – (15 Bytes). .......................................................................................................................................22 
[[CUSIP]]/ISIN – (12 Bytes) .................................................................................................................................22 
[[Stock]]/Bond Indicator – (1 Byte) ......................................................................................................................22 
Trade Date – (8 Bytes) ....................................................................................................................................22 
[[settlement]] Date – (8 Bytes) ............................................................................................................................22 
[[NSCC]] Receive Date – (8 Bytes) .....................................................................................................................22 
CTS Date – (8 Bytes) ......................................................................................................................................22 
CTS Cycle – (1 Byte) .......................................................................................................................................23 
[[CNS]] Indicator – (1 Byte) .................................................................................................................................23 
Guarantee Indicator – (1 Byte) ........................................................................................................................23 
Netting Indicator – (1 Byte)..............................................................................................................................23 
Net Reason Code – (3 Bytes) .........................................................................................................................24 
Foreign Indicator – (1 Byte) .............................................................................................................................26 
When Issued Indicator – (1 Byte) ....................................................................................................................26 
As Of Indicator – (1 Byte) ................................................................................................................................26 
Step In/Out Indicator – (1 Byte) .......................................................................................................................27 
Currency – (3 Bytes) .......................................................................................................................................27 
Depository – (2 Bytes) .....................................................................................................................................27 
Buy/Purchase Item count – (9 Bytes) ..............................................................................................................27 
Buy/Purchase Quantity – (13 Bytes) ...............................................................................................................27 
Buy/Purchase Amount – (17 Bytes) ................................................................................................................27 
Sell Item Count – (9 Bytes) .............................................................................................................................27 
Sell Quantity – (13 Bytes)................................................................................................................................27 
Sell Amount – (17 Bytes).................................................................................................................................27 
Balance Order Record ......................................................................................................................................31 

---

## Page 5

 
 
Contra-[[participant]] – (8 Bytes) .........................................................................................................................31 
Balance Order Issue Date – (8 Bytes) ............................................................................................................31 
Balance Order Control Number – (12 Bytes) ..................................................................................................31 
Trade Dates – (8 Bytes) ..................................................................................................................................31 
Receive Order or Deliver Order – (2 Bytes) ....................................................................................................31 
Balance Order Quantity – (13 Bytes) ..............................................................................................................31 
Balance Order Value – (17 Bytes) ..................................................................................................................31 
Cash Adjustment...............................................................................................................................................32 
Cash Adjustment Code – 2 Bytes) ..................................................................................................................32 
Price – (12 Bytes) ............................................................................................................................................32 
Debit or Credit – (1 Byte).................................................................................................................................32 
Cash Adjustment – (17 Bytes) ........................................................................................................................32 
10. Distribution of the CTS ................................................................................................................................ 33 
Autoroute Products ...........................................................................................................................................33 
Set Up the Subscription to Receive the New File .............................................................................................33 
Frequency of the CTS Files ..............................................................................................................................33 
File Output–Autoroute Products .......................................................................................................................34 
Online Query .....................................................................................................................................................34 
11. Testing Requirements ................................................................................................................................. 35 
12. Timeline of Changes to Consolidated Trade Summary (CTS) ................................................................. 36 
13. Questions and Answers .............................................................................................................................. 37 
 

---

## Page 6

CTS Customer Business Requirements 
Revision History 6 
REVISION HISTORY 
The following table shows the revision history: 
 
DATE  VERSION  AUTHOR  DESCRIPTION  
January 26, 2015 1.0 – 1.4  Janice DiTore  Drafts  
February 13, 2015 1.5  Janice DiTore  First publication  
January 25, 2016 2.0  Janice DiTore  Net Reason Codes added, Timeline updates  
March 22, 2016 2.1  Janice DiTore  Updated Net Reason Code table to include 
T+2. See Net Reason Codes.  
January 12, 2017 2.2  Casey Sorochen  Update Cash Adjustments due to Functional 
Specification  
June 14, 2017 2.3  Tim Garrett  Updated debits, credits and cash adjustments 
not separated with a comma in CSV output 
October 5, 2020 2.4 Lou Lepore Updated the market codes. See Market 
Codes. 
March 25, 2022 2.5 Peter Smith Updated the Net Reason Codes. 

---

## Page 7

CTS Customer Business Requirements 
About this Guide 7 
1. ABOUT THIS GUIDE 
The purpose of this business requirements document is to provide customers with an understanding of how the 
trades received by the National [[securities]] Clearing Corporation Universal Trade Capture (UTC) system will be 
processed downstream and appear on the issuance of the new Consolidated Trade Summary (CTS). The 
business requirements contained herein have been reviewed with a representative group of firms who 
volunteered one or more individuals to assist with their development. 
The existing CTS files use a legacy application that will be rewritten. Where possible, the terminology used for 
CTS is consistent with Universal Trade Capture (UTC). 
This document will define what data is included in the new Consolidated Trade Summary and when it will be 
presented to the customer. The changes from the legacy CTS process to the new process will be included with 
a description of service. 
To understand the rules and procedures surrounding the processing for Universal Trade Capture (UTC), 
Consolidated Trade Summary (CTS), and [[CNS]]
® systems; see the [[NSCC]] Rules and Procedures available in 
the Legal & Regulatory section of the [[DTCC]].com site. 
All changes are subject to the [[Securities and Exchange Commission]] ([[SEC]]) approval. 
Contact Us 
Use the following [[NSCC]] contacts for information about CTS. You can also contact your [[DTCC]] Relationship 
Manager or obtain general assistance by visiting the [[DTCC]] Client Center. 
For… Contact… 
General questions and product support [[NSCC]] Support by email at NSCCSupport@[[DTCC]].com 
Setup and testing [[NSCC]] Integration by email at 
NSCCIntegration@[[DTCC]].com 
Issues with logging on to the system [[DTCC]] Client Support. Call the following number, and then 
follow the prompt for product support. 
• For US and Canada, call 1 888–382–2721. 
• For the UK, Europe, and Asia, call +1 212–855–8099. 
 

---

## Page 8

CTS Customer Business Requirements 
Terminology 8 
2. TERMINOLOGY 
ACRONYM OR TERM  DEFINITION  
As of  Time from trade date to [[settlement]] date [[DO]] not fit standard industry conventions 
due to either the trade being submitted after the trade date or the [[settlement]] date 
being adjusted because it is past the stated contractual [[settlement]] date on the 
trade.  
Bilateral net  Combine trades with like characteristics between two contras  
CMU RTTM  Corporate, Municipal and Unit Investment Trust Real-Time Trade Matching  
[[CNS]]  Provides continuous net [[settlement]]. [[CNS]] is [[NSCC]]’s central counterparty  
CPD  Central Pricing Database a.k.a. [[DTCC]]’s Price database  
CTS  Consolidated Trade Summary  
[[default]] Pricing  If a price is not available or is not current, then [[default]] values are used.  
Stocks = $1.00 per share  
[[Bonds]] = $ 0.00 and marks the obligation as trade for trade  
[[DO]]  Delivery Orders  
[[DTC]]  [[Depository Trust Company]]  
[[DTCC]]  Depository Trust and Clearing Corporation  
Extended [[settlement]]  AKA [[Seller]]’s [[Option]]. The [[settlement]] cycle between trade date and [[settlement]] date 
is longer than the industry standard of 3 days. The maximum length of a 
[[settlement]] cycle accepted at [[DTCC]] is 180 days.  
F  Foreign [[securities]] as defined on [[DTCC]]’s security master file  
ISIN  International Security Identification Number,  
([[DTCC]] version: [[CUSIP]] modified with check digit)  
MUNI  Municipal [[securities]]  
Multi-lateral net  Combine trades with like characteristics between multiple contras.  
Non-[[CNS]]  The [[obligations]] will not be settled by [[NSCC]]’s Central Counterparty, ([[CNS]]).  
[[NSCC]]  National [[securities]] Clearing Corporation  
Same Day Settling  Trade submitted to UTC where the [[settlement]] date is the day of receipt.  
[[Seller]]’s [[Option]]  Term used by UTC for submitting an extended [[settlement]] trade.  
RO  Receive Orders  
SD  [[settlement]] date  
SP  [[Broker]] indication of Special Trade Processing on original trade submission from 
marketplace requesting to settle trade for trade (Submission of X converts to SP.)  
TD  Trade date  

---

## Page 9

CTS Customer Business Requirements 
Terminology 9 
ACRONYM OR TERM  DEFINITION  
TT  Trade for Trade as determined by [[NSCC]] security master file 
UTC Universal Trade Capture 
WI When (and as if) Issued/Distributed 
 
NEW TERMS  DEFINITION  
Non-[[CNS]], guaranteed  [[obligations]] that are not be included in the [[CNS]] [[settlement]] processing at [[NSCC]]; 
however, they are included in multi-lateral netting, allotting, and re-pricing with a 
uniform [[settlement]] price applied. (See [[NSCC]] Rules for Guarantee). 
Non-[[CNS]], not guaranteed  [[obligations]] that will not be included in the [[CNS]] [[settlement]] processing at [[NSCC]], 
and will be bilaterally aggregated or netted, unless designated as trade for trade. 
02  Cash Adjustment line code 02 for non-[[CNS]], guaranteed [[obligations]]. 
23  Cash Adjustment line code 23 for non-[[CNS]], not guaranteed [[obligations]]. 
[[Stock]]/Bond  Security is classified as a [[Stock]] or bond on the [[DTCC]] security master file. 
NP  No current price is available for the security. 
Step in/out  The Step in or Step out value as specified on the trade received by UTC. 

---

## Page 10

CTS Customer Business Requirements 
Domestic Trades with Various [[settlement]] Cycles 10 
3. DOMESTIC TRADES WITH VARIOUS [[settlement]] 
CYCLES 
Transactions received by [[NSCC]] where the [[securities]] and clients are full service members settling in the [[CNS]]  
system will be labeled as [[CNS]] and included on the CTS. Timing of the [[CNS]] eligible transactions appearance 
on the CTS depends on the status of the security as either When (and as if) Issued or When Distributed; or the 
timing relative to the [[settlement]], based on the receipt of the trade. Processing methodology for [[CNS]] eligible 
transactions is not being changed. 
Domestic When (and As If) Issued or When Distributed [[securities]] 
Trade 
When (and as if) Issued municipal [[securities]] are submitted to the CMU RTTM for matching and reporting. The 
CMU RTTM application will define the [[settlement]] date when known and pass the trades to UTC on [[settlement]] 
date minus two days (SD-2). The CMU RTTM process for WI will apply to all matched [[securities]], including 
syndicates. The CTS will display the trades as when issued using an indicator on [[settlement]] date minus two 
days. 
When Distributed domestic [[Equity]] trades will be accepted by UTC from any marketplace and held until 
[[settlement]] date minus two days when it will be included in the CTS extract. The CTS will display the trades as 
when issued using an indicator. 
Domestic [[securities]] Trade With a [[settlement]] Cycle Between 4 and 
180 Days 
UTC accepts trades with a [[settlement]] cycle between 4 and 180 days which are commonly called “Extended 
[[settlement]]” trades. If the timeframe from the trade date to [[settlement]] date is between 4 and 180 days, UTC will 
accept the trade and hold it until [[settlement]] Date less two days (SD–2) when it will appear on the CTS. CTS 
[[obligations]] with extended [[settlement]] periods have a Trade Type indicator of [[Seller]]’s [[Option]].  
Domestic [[securities]] Trade With 3 Day [[settlement]] 
Most domestic trades whether [[CNS]] or non-[[CNS]] are submitted on the trade date with a [[settlement]] date three 
days later. The matched trades will be accepted from the marketplace and included in the standard clearance 
processes where the [[obligations]] will be summarized by [[settlement]] date and listed on the next day’s CTS cycle 
1 (night of trade date plus one day (T+1).) 

---

## Page 11

CTS Customer Business Requirements 
Domestic Trades with Various [[settlement]] Cycles 11 
Domestic [[securities]] Trade with 2 Day [[settlement]] 
Both [[CNS]] and Non-[[CNS]] transactions received two days before [[settlement]] date will be included on the CTS 
cycle 1 the night of receipt where appropriate according to the netting criteria. The trade date for a security 
settling in two days can be either in the past, for a late submission; or today, as a transaction with a shortened 
[[settlement]] cycle. 
Domestic [[securities]] Trade Settling in 1 Day 
Transactions that are received from the marketplace by UTC where the [[settlement]] is scheduled for the next 
business day are shown on the CTS system on the night of receipt if accepted before close of business (21:00 
ET). If the one day settling trade is received after close of business of the prior day but before the issuance of 
the following day’s CTS, it is included in the CTS cycle 1. 
Domestic [[securities]] Trade Settling the Same Day 
Any transaction received by UTC where the [[settlement]] date equals the date of receipt is called a Same Day 
Settling trade. Depending on the time of receipt of the same day settling trade, the CTS will include it on one of 
two cycles. 
• If the trade is received prior to 11:30 Eastern Time, including the trade date, [[settlement]] date, and receipt 
date, on January 29, 2015, the trade is listed on the CTS cycle 3 on January 29, 2015. 
• If the trade is received after 11:30 Eastern Time, on January 29, 2015, with the trade date and [[settlement]] 
date of January 29, 2015, it is assigned the next available [[settlement]] date and included on the CTS cycle 
1, on the night of receipt, January 29, 2015. 
TRADE DATE  DATE 
RECEIVED BY 
UTC  
DAYS UNTIL 
[[settlement]]  
[[settlement]] 
DATE  
CTS 
CALENDAR 
DATE  
CYCLE 1 (MAIN) 
CYCLE 3 
(SUPPLEMENTAL)  
11/19/2014  11/19/2014  78  1/29/2015  1/27/2015  Cycle 1  
1/26/2015  1/26/2015  3  1/29/2015  1/27/2015  Cycle 1  
1/26/2015  1/27/2015  
before 21:00 ET  
2  1/29/2015  1/27/2015  Cycle 1  
1/26/2015  1/29/2015 before 
11:30 ET  
0  1/29/2015  1/29/2015  Cycle 3  
1/29/2015  
after 11:30 ET 
1/29/2015  
Assigned  
1/30/2015 
1/29/2015 Cycle 1 
1/20/2015  1/27/2015  2  1/29/2015  1/29/2015  Cycle 1  
 
• End of day processing is assumed to be 21:00 Eastern Time for this business requirement document. 

---

## Page 12

CTS Customer Business Requirements 
Foreign [[securities]] Trades with Various [[settlement]] Cycles 12 
4. FOREIGN [[securities]] TRADES WITH VARIOUS 
[[settlement]] CYCLES 
Both UTC and the CTS identify foreign [[securities]] trades by using the foreign [[securities]] value in the special 
trade processing indicator field of the [[DTCC]] [[securities]] master file. Every trans action identified as a foreign 
security will be marked accordingly on the CTS with a foreign indicator. 
All other [[securities]] are considered domestic. 
Foreign [[securities]] trades will be included on the main CTS on the night of receipt, and have an indicator of 
foreign. The foreign [[securities]] trade files Auto Route Product [[ID]] # 02022231 for Machine Readable Output 
(MRO) and # 02020232 for Print Image will both be discontinued. 
Foreign [[securities]] trades are classified as non-[[CNS]], not guaranteed; therefore, CTS treatment will be either 
bilateral netting or trade for trade. Any cash adjustment resulting from bilateral netting of foreign [[securities]] 
transactions will be sent to [[DTC]] [[settlement]] Line Code 23. 
Foreign When Issued or When Distributed [[securities]] Trade 
Foreign [[securities]] trades in when issued status must have a [[settlement]] date defined to be accepted for 
processing. 
The Foreign when issued trade will be accepted by UTC and appear on the CTS on the night of receipt with a 
WI indicator. 
Foreign [[securities]] Trade With a [[settlement]] Cycle 4 to 180 Days 
Foreign [[securities]] trades with a [[settlement]] date between 4 and 180 days in the future should be submitted to 
UTC using the extended trade capability known as “[[Seller]]’s [[Option]]” combined with the number of days until 
[[settlement]]. The foreign [[securities]] trade will be on the CTS the night of receipt only. The following are some 
examples: 
• Trade date is 1/26/2015 received by UTC the same day, with a [[settlement]] date of 3/3/2015, which is 26 
days in the future; it would be seen on the main CTS on the night of 1/26/2015. 
• If the trade date of 1/15/2015 on a foreign [[securities]] trade received on 1/26/2015 for a [[settlement]] date of 
1/29/2015, then it would be included on the CTS cycle 1 on the night of 1/26/2015.  
• If the foreign [[securities]] trade traded on 1/12/2015 for a [[settlement]] date of 1/29/2015 but was not received 
by UTC until 1/28/2015 then it would appear on the CTS cycle 1 on the night of 1/28/2015.  If the foreign 
[[securities]] trade date were 1/20/2015 with a [[settlement]] date of 1/29/2015 and not received by UTC until 
1/29/2015 (regardless of time), it is assigned the next available [[settlement]] date of 1/30/2015 and appear 
on the 1/29/2015 CTS cycle 1 file. 

---

## Page 13

CTS Customer Business Requirements 
Foreign [[securities]] Trades with Various [[settlement]] Cycles 13 
Trade Date  Date received by UTC  # days until 
[[settlement]]  
[[settlement]] Date  Date of CTS Cycle  
1/26/2015  1/26/2015  26  3/3/2015  1/26/2015, main  
1/15/2015  1/26/2015  9  1/29/2015  1/26/2015, main  
1/12/2015  1/28/2015  12  1/29/2015  1/28/2015, main  
1/20/2015  1/29/2015  7  1/29/2015  
Assigned 1/30/2015  
1/29/2015, main  
 
• End of day processing is assumed to be 21:00 ET for this Business Requirement document.  
Foreign [[securities]] Trade With 3 Day [[settlement]] 
Foreign [[securities]] trades settling in three days will be submitted to UTC as a Regular Way submissions and will 
appear on the main CTS the night of receipt. If the foreign [[securities]] transaction trade date equals January 26, 
2015, the [[settlement]] date is January 29, 2015, and it was received on January 26, 2015, it is included on the 
CTS cycle 1 the night of January 26, 2015. 
Foreign [[securities]] Trade With 2 Day [[settlement]] 
Many foreign (a.k.a. non-domestic) markets are now using a trade date plus two days (T+2) [[settlement]] cycle. 
Firms wanting to conform to the T+2 [[settlement]] of foreign [[securities]] should submit foreign [[securities]] trades to 
the Universal Trade Capture (UTC) system with the trade date and the [[settlement]] type of “[[Seller]]’s [[Option]]” 
indicating the number of days until [[settlement]] equal to 2. (See [[NSCC]] Important Notice A#7871, dated July 18, 
2014.) 
Foreign [[securities]] Trade Settling in 1 Day 
Foreign [[securities]] trades which are received from the marketplace by UTC where the [[settlement]] is scheduled 
for the next business day will be shown on the CTS on night of receipt if accepted before close of business 
(21:00 Eastern Time). 
• If the foreign [[securities]] trade traded on January 28, 2015 for a [[settlement]] date of January 29, 2015, but 
was not received by UTC until January 28, 2015 before close of business (21:00 ET),  and it appears on 
the CTS cycle 1 on the night of January 28, 2015 
• If the foreign [[securities]] trade traded on January 28, 2015 for a [[settlement]] date of January 29, 2015 but 
was not received by UTC until January 28, 2015 after close of business (21:00 ET), it is assigned the next 
available [[settlement]] date of January 30, 2015, and it appears on the CTS cycle 1 on the night of January 
29, 2015 

---

## Page 14

CTS Customer Business Requirements 
Foreign [[securities]] Trades with Various [[settlement]] Cycles 14 
Foreign [[securities]] Trade Settling Same Day 
UTC will reject a foreign [[securities]] trade submitted to UTC as “Cash, Same Day Settling” where the trade date, 
[[settlement]] date and UTC receipt date are all on the same day. 
• If the foreign [[securities]] trade, submitted as Cash, Same Day Settling, has a trade date of January 29, 
2015, [[settlement]] date of January 29, 2015 and it is submitted to UTC on January 29, 2015, it is rejected. 
Net Reason Codes for Foreign Trades 
• 024-Foreign security is received 1 or more days before [[settlement]] date. Transactions will be bilaterall y 
netted, not guaranteed. 
• 041-Original trade record in a foreign security was submitted with the request to process as trade for 
trade. It will be processed as trade for trade, not guaranteed. 
• 046-The security is known as foreign and settles in one day. It will be processed as trade for trade, not 
guaranteed. 

---

## Page 15

CTS Customer Business Requirements 
Trade for Trade (Non-[[CNS]], Not Guaranteed) 15 
5. TRADE FOR TRADE (NON-[[CNS]], NOT GUARANTEED) 
Multiple reasons exist for trades to be settled individually, (trade for trade), rather than aggregated or netted. 
Client preference, the client membership type, the security classification, availability for [[settlement]], and lack of 
a current price are all factors in the determination of trade for trade [[settlement]]. If the trade is  eligible for more 
than one of the trade-for-trade designations, the hierarchy is as listed below, with a [[Broker]] submitted trade for 
trade taking the highest priority. 
[[Broker]] Submitted Trade-for-Trade 
If the trade is executed with the marketplace designated trade for trade, (regardless of whether the domestic or 
foreign security is [[Equity]] or fixed income); the (SP) indicator will be received by Universal Trade Capture (UTC) 
and reflected on the Consolidated Trade Summary (CTS) as Net Reason Code:  
• 040-Original domestic security trade was submitted with the request to process as trade for tr ade. 
[[participant]] Not Eligible for Netting 
[[NSCC]] has limited membership categories for clients that [[DO]] not desire to be full service [[Member]] participating. 
The [[NSCC]] limited membership allows for the client to submit municipal [[securities]] trades for matching an d 
reporting by the CMU RTTM application. The trades matched as municipal comparison only trades are not sent 
to [[CNS]] or netted in any way. The municipal comparison only trades will be shown on the CTS as trade for 
trade as Net Reason Code: 
• 051-Either one or both parties to the trade are not eligible for [[CNS]] processing. It will be processed as 
trade for trade, not guaranteed. 
  

---

## Page 16

CTS Customer Business Requirements 
Trade for Trade (Non-[[CNS]], Not Guaranteed) 16 
[[securities]] Not Eligible for Netting 
If the trade is submitted with no trade for trade designation by the [[Broker]], however the [[DTCC]] master file has 
classified the security as one not eligible for either the bilateral or multi-lateral netting processes, then the Net 
Reason Code specific to the condition will be applied. 
Trades may not be eligible for non-[[CNS]] netting when submitted to the clearing corporation with a [[settlement]] 
cycle shorter than is standard practice for the security or after the [[settlement]] date.  
Here are some examples of non-[[CNS]] transactions submitted with shortened [[settlement]] cycles: 
• The trade date of a domestic [[Equity]] trade is Monday, January 26, 2015 with a [[settlement]] date of Thursday 
January 29, 2015; however, the trade was submitted to the marketplace on Wednesday, January 28, 
2015. The late submission of the trade settling the next day excludes the item from non-[[CNS]] netting. 
• The trade date was Wednesday, January 21, 2015 with a [[settlement]] date of January 29, 2015; however, 
the trade was not entered in CMU RTTM until January 28, 2015. The comparison system assigns a next 
day [[settlement]] and the trade is not eligible for non-[[CNS]] netting. 

---

## Page 17

CTS Customer Business Requirements 
Change in [[CNS]] Eligibility 17 
6. CHANGE IN [[CNS]] ELIGIBILITY 
Trades received by UTC are denoted on UTC output as [[CNS]] or non-[[CNS]]; (whether near real-time via 
message or on the end of day trade contract file(s).) Internal to [[DTCC]], the Ris k management process is also 
engaged to know the trades which have been identified as [[CNS]] eligible. A typical domestic trade is settling 
three days after it was traded then received by [[DTCC]]. That same trade will be included on the main 
Consolidated Trade Summary (CTS) on the night of trade date plus one day. When the CTS is produced a 
validation is made to verify that the trades marked as [[CNS]] by UTC are still eligible. If the trade was labeled by 
UTC as [[CNS]] eligible; then before the CTS is produced, eligibility of the security changes; the CTS will process 
it as a non-[[CNS]] transaction. 
• For example, if the trade date was January 26, 2015 and it was sent to UTC on that date with a [[settlement]] 
date of January 29, 2015, then the CTS would include it on the main CTS the night of January 27, 2015. 
The classification on the CTS is the determination of [[CNS]]; non-[[CNS]], guaranteed; or non-[[CNS]], not 
guaranteed is the indication of the [[obligations]] guarantee and method of [[settlement]]  

---

## Page 18

CTS Customer Business Requirements 
Universal Flip 18 
7. UNIVERSAL FLIP 
Some clients use a process known as Universal Flip where the executing [[Broker]] uses another [[Broker]] to settle 
their [[obligations]] at [[DTC]]. The trades of the submitting [[Broker]] are flipped to the settling [[Broker]] upon receipt in 
UTC. The CTS display the universally flipped [[obligations]] with the market code Flip (FLP). All downstream 
processes after the flip from the submitting [[Broker]] to the settling [[Broker]] will be business as usual.  

---

## Page 19

CTS Customer Business Requirements 
Netting Processes (Non-[[CNS]]) 19 
8. NETTING PROCESSES (NON-[[CNS]]) 
Non-[[CNS]] trade activity that is not identified as trade for trade is considered for so me type of netting during the 
clearance processing, based on the security, trade [[settlement]] cycle and whether current pricing is available. 
Depending on the netting used the trade is determined to be non-[[CNS]], guaranteed or non-[[CNS]], not 
guaranteed. 
Multi-Lateral Netting 
Only domestic [[securities]] are eligible for multi-lateral netting. Foreign [[securities]] trades are not included in any 
multi-lateral netting. 
The netting process looks for trades with the same [[CUSIP]] and [[settlement]] date and summarizes by 
marketplace. See the example in the Summarized Trade Data section. The multi-lateral netting then 
encompasses all the transactions for a given [[settlement]] date per [[CUSIP]] and re- prices all the [[obligations]] to a 
uniform [[settlement]] price using the Central Pricing Database current price before netting and allotting. The final 
results are shown as receive order and deliver order records. See the example in the Balance Order Record 
Example section. 
Trades included in the multi-lateral netting process are non-[[CNS]], guaranteed. Any cash adjustment resulting 
from the re-pricing and netting will be sent to [[DTC]] [[settlement]] Line Code 02 as a non-[[CNS]], guaranteed Cash 
Adjustment. 
Pricing Non-[[CNS]], Guaranteed Transactions 
Rules for pricing used for non-[[CNS]], guaranteed transactions which are included in the multi-lateral netting 
process are as follows: 
• The Uniform [[settlement]] Price in the Central Pricing Database (CPD) at [[DTCC]] must be 5 days or newer to 
be used for re-pricing a non-[[CNS]], guaranteed obligation. 
• [[default]] pricing will no longer be applied. 
• If no price is available, then the obligation will be marked trade for trade and not re- priced. 
• Sub-penny pricing using more than 2 positions to the right of the decimal will be aligned with [[CNS]] 
processing. [[obligations]] where the price per share is less than one US cent will be priced to be consistent 
with other guaranteed services. 
  

---

## Page 20

CTS Customer Business Requirements 
Netting Processes (Non-[[CNS]]) 20 
Bilateral Netting 
Both domestic and foreign [[securities]] trades that are not designated as trade for trade are eligible for bilateral 
netting. All trades against the same [[CUSIP]], [[settlement]] date, and contra-party are summarized by the 
marketplace. See the example in the Summarized Trade Data section. The net of all buy and sell records for a 
given [[settlement]] date (typically) results in one receive order or deliver order. See the example in the Netted 
Trade Data section. Trades included in the bilateral netting process are non-[[CNS]], not guaranteed. Any cash 
adjustment resulting from the bilateral netting will be sent to [[DTC]] [[settlement]] Line Code 23 as a non- [[CNS]], not 
guaranteed Cash Adjustment. 

---

## Page 21

CTS Customer Business Requirements 
Data Elements 21 
9. DATA ELEMENTS 
Field Names and Values 
This section contains the field names used on the CTS output. 
[[participant]] – (8 Bytes) 
[[NSCC]] number of the owner of the trade record on the CTS. 
Market Code – (3 Bytes) 
The Market Code denotes the marketplace where the trade originated. 
The CTS is using the same market codes as UTC. 
MARKET CODE MARKET DESCRIPTION 
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
150 DIRECT EDGE EDGA 
160 DIRECT EDGE EDGX 
170 IEX [[Stock Exchange]] 

---

## Page 22

CTS Customer Business Requirements 
Data Elements 22 
MARKET CODE MARKET DESCRIPTION 
185 LONG TERM [[Stock Exchange]] 
190 MIAX PEARL EQUITIES EXCHANGE  
195 MEMBERS EXCHANGE 
910 RTTM CORPORATE [[Bonds]] 
911 RTTM MUNI [[Bonds]] 
912 RTTM [[UIT]] 
920 EXCHANGE TRADED FUNDS 
Symbol – (15 Bytes). 
The trading symbol used by the marketplace will appear in the symbol column. This field will expand up to 
provide room for suffix information. 
[[CUSIP]]/ISIN – (12 Bytes) 
The [[CUSIP]] or ISIN identifies the security using the country code, followed by [[CUSIP]] and a check digit.  
[[Stock]]/Bond Indicator – (1 Byte) 
A [[Stock]] or bond indicator will define the security type as either an [[Equity]] ([[Stock]]) or fixed income (bond).  
Trade Date – (8 Bytes) 
The trade date defines the date the trade was executed. 
[[settlement]] Date – (8 Bytes) 
The [[settlement]] date reflected on the CTS is not always the original contractual [[settlement]] date it is the date the 
trade is expected to settle at the depository. 
[[NSCC]] Receive Date – (8 Bytes) 
The [[NSCC]] receive date states when the trade was received by UTC. It was previously c alled the “Processing 
Date” 
CTS Date – (8 Bytes) 
The CTS date is the business date on which the CTS report is produced.  
  

---

## Page 23

CTS Customer Business Requirements 
Data Elements 23 
CTS Cycle – (1 Byte) 
The CTS is produced in three separate cycles, previously known as the main file and supplemental file.  
CTS CYCLE  LEGACY COMMON NAME  APPROXIMATE TIME OF DISTRIBUTION  
1  Main CTS  On or before 21:00 ET  
2  Supplemental  On or before 24:00 ET  
3  Supplemental  On or before 12:00 ET  
[[CNS]] Indicator – (1 Byte) 
The [[CNS]] indicator designates the trade as either [[CNS]] eligible or non-[[CNS]]. 
Guarantee Indicator – (1 Byte) 
The guarantee indicator denotes the trade as guaranteed or not guaranteed. 
• [[CNS]] trades are guaranteed until settled. 
• Non-[[CNS]] trades are either guaranteed or not guaranteed. 
o Non-[[CNS]] guaranteed means the trade was included in multi-lateral netting. 
o Non-[[CNS]], not guaranteed trades are made up of bilaterally netted trades and trades settling trade for 
trade. 
Netting Indicator – (1 Byte) 
• Designates the trade netting type 
o Multi-lateral netting for [[CNS]] or non-[[CNS]] guaranteed [[obligations]] 
o Bilateral netting for non-[[CNS]], not guaranteed [[obligations]] 
o Trade for Trade 
  

---

## Page 24

CTS Customer Business Requirements 
Data Elements 24 
Net Reason Code – (3 Bytes) 
Net Reason Codes are being used to provide the granularity needed to gain transparency about why a 
transaction was netted (multi-laterally, bilaterally) or remained as trade for trade. 
NRC#  SHORT DESCRIPTION  LONG DESCRIPTION  
001  [[CNS]] >SDS  [[CNS]] eligible trade settling in the future  
002  [[CNS]] SDS  [[CNS]] eligible trade received before 11:30 ET, settling today  
003  [[CNS]] OCC Accord Trade  [[CNS]] eligible OCC Accord trade settling in the future.  
In T2 [[settlement]] cycle, OCC Accord trades are identified in UTC as 
regular trades having input value of market code = 070. [[Stock]] 
Options are either Calls (Security Type = 15) or Puts (Security Type 
= 16). Futures are either Futures (Security Type = 17) or Narrow 
Based Futures (Security Type = 18).  
Due to the OCC Accord, standard [[settlement]] for Options and 
Futures are not guaranteed until the [[NSCC]] clearing fund has been 
collected. Since this does not occur until 10:00AM on the next 
business day, CTS reporting of OCC standard [[settlement]] Options 
and Futures for trades that are [[CNS]] or guaranteed balance order 
eligible are delayed until CTS cycle 3.  
010  Multi-net, Non-[[CNS]] [[Stock]] > 1DS or 
1DS cycle 3  
Non-[[CNS]] eligible [[Stock]] trade that settles in the future.  
1DS in Cycle 3 net. 
011  Multi-net, Non [[CNS]]  
OCC Accord Trade  
OCC Accord trade that is no longer [[CNS]] eligible.  
012  Multi-net, Non-[[CNS]]  
Across multiple NRC  
Non-[[CNS]] eligible trade that was Multi-laterally netted across NRC 
10, 11, 13, 14. The NRC is only assigned to the Balance Order.  
013  Multi-net, [[CNS]] under Reorg 1DS  Guaranteed Delivery or Cover/Protect period will be calculated as 
expiration date plus two days in a T+2 [[settlement]]  
As of RW trade received between CTS cycle 2 & 3 in a [[CNS]] eligible 
security undergoing a voluntary Corporate Action will be Multi 
laterally netted and reported on CTS Cycle 3.  
014  Multi-net, [[CNS]] OCC Accord Trade, 
Reorg 1DS  
OCC Accord trade submitted As of RW (T+1) trade received before 
CTS cycle 3 undergoing Reorg Tender Offer will be reported on 
CTS Cycle 1.  
020  Bilateral–Non-[[CNS]]  
[[Equity]] Special >SDS  
Non-[[CNS]] [[Equity]], noted as special trade processing on SMD, 
settling in the future.  
021  Bilateral–Non-[[CNS]]  
Bond Special > SDS  
Non-[[CNS]] bond, noted as special trade processing on SMD or from 
CMU, settling in the future.  
022  Bilateral–Non-[[CNS]]  
[[Equity]] 1DS  
Non-[[CNS]] [[Equity]] settling in one day, available on all cycles. 
023  Bilateral–Non-[[CNS]]  
Non-Std >1DS  
Non-[[CNS]], Non-Standard (Cash, Next Day, or [[Seller]]’s [[Option]]) trade 
settling in two or more days. (T3 >1DS) (T2 > 2DS). 

---

## Page 25

CTS Customer Business Requirements 
Data Elements 25 
NRC#  SHORT DESCRIPTION  LONG DESCRIPTION  
024  Bilateral, Foreign [[securities]] > 1DS  Foreign [[securities]] setting in two or more days, available on all 
cycles. Bilateral netting with no re-pricing.  
025  Bilateral  
Non-[[CNS]] Bond. >SDS  
Non-[[CNS]] Corporate bond or [[UIT]] settling in the future, available all 
cycles  
026  Bilateral, Net across multiple NRC  Non-[[CNS]] trades netting bilaterally, then across bilateral codes, all 
cycles. This NRC is only assigned to the Balance Order. 
040  TFT, [[Broker]] Submitted-Domestic  TFT, [[Broker]] specified on original domestic (US) trade  
041  TFT, [[Broker]] Submitted–Foreign  TFT, [[Broker]] specified on original foreign [[securities]] trade  
042  TFT, Non-[[CNS]] [[Equity]] Special-SDS  TFT, SMF denotes security as special trade processing, trade 
settles today. 
043  TFT, Non-[[CNS]] Bond Special-SDS  TFT, Non-[[CNS]] bond submitted via CMU RTTM or security was 
designated as special trade processing on SMF. Trade settles 
today. 
044  TFT, Non-[[CNS]]–SDS  TFT, Non-[[CNS]] bond that settles today, submitted today. 
045  TFT, Non-[[CNS]]  
Non-Std SDS/1DS  
TFT, Submitted as non-standard [[settlement]], (Cash, Next Day, 
Sellers [[Option]]) settles 1day or same day. 
046  TFT, Foreign 1DS  TFT, Foreign security settles in 1 day. 
047  TFT, Non-[[CNS]]  
Municipal  
TFT, Municipal security not eligible for [[CNS]]. 
048  TFT, Muni [[syndicate]] Take Down  TFT, When issued municipal security entered in CMU RTTM as part 
of a [[syndicate]] Take Down,  
049  TFT, Baby Bond, Mixed or Odd Lot  TFT, Trade Quantity is less than standard denomination  
Bond-baby bond, [[Stock]] in odd lot or mixed lot. 
050  TFT, Non-[[CNS]]  
Sub-penny valued bond  
TFT, Non-[[CNS]] eligible bond that is valued at less than one cent. 
051  TFT, [[Broker]] is not a [[Member]] of [[CNS]]  TFT, Municipal Comparison only members trades submitted for 
comparison only.  
052  TFT, [[CNS]] as of RW [[CNS]] Reorg 
Tender SDS/1DS  
TFT, [[CNS]] eligible trade submitted as of RW on T+1 after CTS cycle 
3 and the security is undergoing Voluntary Reorg.  
053  TFT, [[CNS]] Non Std Reorg/Div; 
SDS/1DS  
TFT, [[CNS]] eligible trade submitted as a Non-Standard [[settlement]] 
today or next day. Security is experiencing Mandatory or Voluntary 
Reorg, or [[Dividend]] distribution whereby [[Margin]] cannot be collected 
in time and the [[CNS]] Projection would exclude the trade.  
054  TFT, [[CNS]] Non-Std Reorg Tender 
SDS/1DS  
TFT, [[CNS]] eligible trade submitted as a Non-Standard [[settlement]], 
Security is in the Protect period for Reorg Tender Offer where the 
[[Margin]] cannot be collected in time and the [[CNS]] Projection would 
exclude the trade. 

---

## Page 26

CTS Customer Business Requirements 
Data Elements 26 
NRC#  SHORT DESCRIPTION  LONG DESCRIPTION  
055 TFT, Non-[[CNS]] [[ETF]] CR/RD 
 
All Fixed Income and [[Equity]] components originating from the [[ETF]] 
market (920) assigned as TFT will be reported with the locked in 
counterparty identified from the order. No netting will be applied. 
099  TFT, Undefined Net Reason Code  TFT, Transaction does not meet the criteria for any other net reason 
code  
100  Non-Settling-Cash Trade Missed SDS 
Cutoff  
Not on CTS.  
SDS trade that missed the 11:30 ET cutoff for CTS cycle 3, reported 
only on UTC. 
101  Non-Settling–ETMF  
Report Only Trade  
Not on CTS.  
Exchange Traded Mutual Fund, reported only on UTC. 
102  Non-Settling-Trade Pending UTC Edit  Not on CTS.  
Trade pended in the UTC edit. 
103  Non-Settling-UTC Trade Reject  Not on CTS UTC rejected the trade. 
Foreign Indicator – (1 Byte) 
The Foreign indicator signifies that the [[DTCC]] security master file has marked the security as a non- domestic 
(foreign) issue. 
When Issued Indicator – (1 Byte) 
The When Issued indicator denotes that the security was received as either a when (and as if) issued, or a 
when distributed security. The [[DTCC]] security master file will note this security as in original issuance status.  
As Of Indicator – (1 Byte) 
The As Of indicator denotes that the trade was submitted with as of attributes. 
• T-the receipt date was after trade date 
• S-the [[settlement]] date has been changed by either a trade capture or clearance system at [[DTCC]].  
o The same day settling trade may have been received too late to be included in today’s [[settlement]] 
cycle; therefore, it is assigned the next available [[settlement]] date. 
o The trade received by UTC today has a [[settlement]] date in the past; therefore, the next available 
[[settlement]] date is assigned. 
o The delivery date and [[settlement]] date on a trade submitted to the CMU RTTM system [[DO]] not equal.  
  

---

## Page 27

CTS Customer Business Requirements 
Data Elements 27 
Step In/Out Indicator – (1 Byte) 
The step in or step out indicator is the same as shown on the UTC contract sheets. The step in/ out indicator is 
not a netting criteria and is available only on the summarized trade data. 
Currency – (3 Bytes) 
All transactions are represented in U.S. Dollars. 
Depository – (2 Bytes) 
The depository defines the expected location of [[settlement]]. 
• [[DTC]]-[[Depository Trust Company]] 
• Other-Any other depository 
Buy/Purchase Item count – (9 Bytes) 
The buy item count defines the number of buy trades included in the record. 
Buy/Purchase Quantity – (13 Bytes) 
The buy quantity is the aggregate buy quantity. 
Buy/Purchase Amount – (17 Bytes) 
The buy amount is the aggregate buy money amount. 
Sell Item Count – (9 Bytes) 
The sell item count is the number of sell trades included in the record. 
Sell Quantity – (13 Bytes) 
The sell quantity is the aggregate sell quantity. 
Sell Amount – (17 Bytes) 
The sell amount is the aggregate sell money amount. 
 

---

## Page 28

CTS Customer Business Requirements 
Data Elements 28 
Summarized Trade Data Example 
Summarized Trade Data Example 
Record # 
[[participant]] 
Market 
Symbol 
ISIN/[[CUSIP]] 
[[Stock]]/Bond 
Trade Date 
[[NSCC]] Receive Date 
[[settlement]] Date 
CTS Report Date 
CTS Rpt Cycle/Section 
[[CNS]]/Non-[[CNS]] 
Guaranteed 
Trade for Trade 
When Issued 
Foreign 
As-of 
Step in/Step Out 
Currency 
Depository 
Buy Item Count 
Buy Quantity 
Buy Amount 
Sell Item Count 
Sell Quantity 
Sell Amount 
1 123 100 AA ABC123456789 S 2/4/2015 2/4/2015 2/12/2015 2/10/2015 9pm 2DS C Y  W    USD D 7 70 700 4 40 400 
2 123 100 AA ABC123456789 S 2/9/2015 2/9/2015 2/12/2015 2/10/2015 9pm 2DS C Y      USD D 10 100 1000 5 50 500 
3 123 100 AA ABC123456789 S 2/9/2015 2/10/2015 2/12/2015 2/10/2015 9pm 2DS C Y    T  USD D 1 10 100    
4 123 100 AA ABC123456789 S 2/9/2015 2/12/2015 2/12/2015 2/10/2015 Noon SDS C Y    T  USD D    1 4 40 
5 123 100  ABC123456789 S 2/9/2015 2/13/2015 2/13/2015 2/13/2015 Noon SDS C Y    S  USD D    1 3 30 
6 123 100 MM MNO987654321 S 2/9/2015 2/9/2015 2/12/2015 2/10/2015 9pm 2DS C Y      USD D 5 50 500    
7 123 100 MM MNO987654321 S 2/9/2015 2/9/2015 2/12/2015 2/10/2015 9pm 2DS C Y      USD D 4 40 400 6 60 600 
8 123 100 DD DEF234567891 S 2/9/2015 2/9/2015 2/12/2015 2/10/2015 9pm 2DS N Y     I USD D 20 200 2000 22 220 2200 
9 123 100 DD DEF234567891 S 2/9/2015 2/10/2015 2/12/2015 2/10/2015 9pm 2DS N Y    T O USD D 6 60 600    
10 123 100 GG GHI345678912 B 2/9/2015 2/9/2015 2/12/2015 2/10/2015 9pm 2DS N N PT     USD D    1 7 70 

---

## Page 29

CTS Customer Business Requirements 
Data Elements 29 
11 123 100 GG GHI345678912 B 2/9/2015 2/11/2015 2/12/2015 2/11/2015 9pm 1DS N N SP   T  USD D    1 2 20 
12 123 100 GG GHI345678912 B 2/9/2015 2/11/2015 2/12/2015 2/11/2015 9pm 1DS N N TT   T  USD D    2 5  
13 123 100 AA ABC234567890 S 2/9/2015 2/9/2015 2/13/2015 2/11/2015 9pm 2DS C C      USD D 1 8 80    
14 123 100 AA ABC234567890 S 2/10/2015 2/10/2015 2/13/2015 2/11/2015 9pm 2DS C C      USD D 25 250 2500 17 170 1700 
15 123 100 KK JKL112345678 S 2/10/2015 2/10/2015 2/13/2015 2/10/2015 9pm 3DS N N   F   USD O 1 6 60 3 5 50 
 
  

---

## Page 30

CTS Customer Business Requirements 
Data Elements 30 
Netted Trade Data Example 
The example is being used for illustrative purposes only and is subject to change. The field sizes and values will be appropr iately sized and populated in the 
production version. Color coding was used to help the user associate the summary of records to the Netted Trade Data.  
Netted Trade Data Example 
Record # 
[[participant]] 
Market 
Symbol 
ISIN/[[CUSIP]] 
[[Stock]]/Bond 
Trade Date 
[[NSCC]] Receive Date 
[[settlement]] Date 
CTS Report Date 
CTS Rpt Cycle/Section 
[[CNS]]/Non-[[CNS]] 
Guaranteed 
Trade for Trade 
When Issued 
Foreign 
As-of 
Step in/Step Out 
Currency 
Depository 
Buy Item Count 
Buy Quantity 
Buy Amount 
Sell Item Count 
Sell Quantity 
Sell Amount 
a 123 100  ABC123456789 S   2/12/2015 2/10/2015 9PM 2DS C         18 180 1800 9 90 900 
b 123 100  ABC123456789 S   2/12/2015 2/10/2015 Noon SDS C            1 4 40 
c 123 100  ABC123456789 S   2/13/2015 2/13/2015 Noon SDS C            1 3 30 
d 123 100  MNO987654321 S   2/12/2015 2/10/2015 9PM 2DS C         5 50 500    
e 123 100  MNO987654321 S   2/12/2015 2/10/2015 9PM 2DS C         4 40 400 6 60 600 
f 123 100  DEF234567891 S   2/12/2015 2/10/2015 9PM 2DS N         26 260 2600 22 220 2200 
g 123 100  GHI345678912 B   2/12/2015 2/10/2015 9PM 2DS N PT           1 7 70 
h 123 100  GHI345678912 B   2/12/2015 2/11/2015 9PM 2DS N SP           1 2 20 
i 123 100  GHI345678912 B   2/12/2015 2/11/2015 9PM 2DS N TT           2 5 50 
j 123 100  ABC234567890 S   2/13/2015 2/11/2015 9PM 2DS C         26 258 2580 17 170 1700 

---

## Page 31

CTS Customer Business Requirements 
Data Elements 31 
Note the records are presented without final netting of buys and sells. 
Balance Order Record 
Contra-[[participant]] – (8 Bytes) 
The contra is the counterparty to the obligation(s). 
Balance Order Issue Date – (8 Bytes) 
The balance order issue date defines the processing date on which the receive order or deliver order was 
created. 
Balance Order Control Number – (12 Bytes) 
The balance order control number is a unique identifier created and assigned by [[DTCC]] for each receive order 
and deliver order. A Julian date is imbedded in the balance order control number.  
Trade Dates – (8 Bytes) 
The trade date on a receive order or deliver order will be the earliest date in the grouping that is netted. 
Receive Order or Deliver Order – (2 Bytes) 
Receive or deliver order is the designation of whether the quantity and amount are to be received or delivered.  
Balance Order Quantity – (13 Bytes) 
The balance order quantity is the security quantity of the receive order or deliver order. Only whole number 
quantities will appear on the CTS. Fractions are not included. 
Balance Order Value – (17 Bytes) 
The Balance Order Value is the money amount of the receiver order or deliver order.  
Balance Order Record Example 
Balance Order Record Example 

---

## Page 32

CTS Customer Business Requirements 
Data Elements 32 
record # 
[[participant]] 
Contra 
[[participant]] 
[[CUSIP]]/ISIN 
Balance Order 
Control Number 
Trade Date 
[[settlement]] Date 
Guarantee 
Trade for Trade 
Foreign 
Receive 
Order/Deliver 
Od  
Quantity 
Amount 
f 123 456 456DEF234567891 123456789013 2/9/2015 2/12/2015 Y PT  RO 40 420 
g 123 789 GHI345678912 123456789014 2/9/2015 2/12/2015 N SP  [[DO]] 7 70 
h 123 789 GHI345678912 123456789015 2/9/2015 2/12/2015 N TT  [[DO]] 2 20 
i 123 897 GHI345678912 123456789016 2/9/2015 2/12/2015 N   [[DO]] 5 50 
k 123 456 JKL112345678 123456789017 2/10/2015 2/13/2015 N  F [[DO]] 1 10 
Cash Adjustment 
This section provides information about cash adjustments. 
Cash Adjustment Code – 2 Bytes) 
• 02–[[DTC]] Line Code for Non-[[CNS]], guaranteed cash adjustments from multi-lateral netting. 
• 23–[[DTC]] Line Code for Non-[[CNS]], not guaranteed cash adjustments resulting from bilateral netting. 
Price – (12 Bytes) 
The price per share or unit used to re-price the multi-laterally netted [[obligations]]. 
Debit or Credit – (1 Byte) 
• - equals Debit 
• + equals Credit 
Cash Adjustment – (17 Bytes) 
The value of the cash adjustment sent to [[DTC]] [[settlement]], which will be broken out for each [[CUSIP]].  
Cash Adjustment Record Example 
Record # [[participant]] [[CUSIP]]/ISIN Cash Adjustment 
Line Code 
Cash Amount 
f 123 DEF234567891 02 +20 

---

## Page 33

CTS Customer Business Requirements 
Distribution of the CTS 33 
10. DISTRIBUTION OF THE CTS 
Autoroute Products 
The existing Legacy AutoRoute Product [[ID]]’s will be sunset in 2017 as a hard cut to the new files.  New Auto 
Route product [[ID]]’s have been created to distribute the Consolidated Trade Summary in both machine to 
machine output (MRO) and Comma Separate Value (CSV) versions. 
The text print image will be discontinued. 
Set Up the Subscription to Receive the New File 
To subscribe to the new AutoRoute product [[ID]]’s being created to distribute the CTS to customers contact 
NSCCSupport@[[DTCC]].com 
Frequency of the CTS Files 
The CTS cycle 1 will continue to be distributed on or before 21:00 ET daily. The CTS cycle 1 will contain 
domestic [[obligations]] settling in 1 or 2 days and foreign [[securities]] [[obligations]] received during the course of the 
business day, regardless of future [[settlement]] date. 
The CTS cycle 2 will continue to be distributed about 24:00 ET daily and contain the one day [[obligations]]. 
The CTS cycle 3 will be sent out on or before 12:00 ET daily containing same day and one day settling 
domestic and foreign [[securities]] [[obligations]]. 
  

---

## Page 34

CTS Customer Business Requirements 
Distribution of the CTS 34 
File Output–Autoroute Products 
All AutoRoute products on this table are being decommissioned in 2017. 
PUBLISHED 
TIME OF 
DISTRIBUTION  
LEGACY FILE NAME— 
TO BE SUNSET IN 2017  
EXISTING AUTOROUTE 
TEST PRODUCT [[ID]] #  
EXISTING AUTOROUTE 
PRODUCTION PRODUCT [[ID]] #  
22:00 Consolidated Trade Summary  
Main report, Cycle 1  
MRO:  02982354 MRO:  02042354 
Print Image:  02980353 Print Image:  02040353 
01:00 Consolidated Trade Summary  
Supplemental1, Cycle 2  
(Historically empty) 
MRO:  02980954 MRO:  02040954 
Print Image  02980953 Print Image:  02040953 
13:00 Consolidated Trade Summary  
Supplemental2, Cycle 3 
MRO:  02980954 MRO:  02040954 
Print Image:  02980953 Print Image:  02040953 
      
22:00  Foreign [[securities]] Trades  MRO:  02982231 MRO:  02022231 
Print Image: 02980232 Print Image: 02020232 
 
Output to be discontinued includes: The Foreign [[securities]] Trades. The data will be incorporated into the new 
CTS file output using one AutoRoute Product [[ID]] with three cycles. 
Online Query 
The CTS data will be available through an online query tool. More information about the search and results 
screens will be available in a future Important Notice. 

---

## Page 35

CTS Customer Business Requirements 
Testing Requirements 35 
11. TESTING REQUIREMENTS 
All [[NSCC]] clients will be required to participate in the testing to receive and use the new Auto Route Product 
files being created as part of this CTS re-write project. 
• Test files of canned data were created and are available for clients. 
o AutoRoute Product [[ID]] # 029902339 (for machine to machine output, MRO) 
o AutoRoute Product [[ID]] # 029902340 (for comma separate version, CSV) 
• Firms should use the new test files to run down stream in their internal processing.  
• Testing details will be released via Important Notice and posted to the [[DTCC]] Learning website to provide 
expectations for the testing phase. 

---

## Page 36

CTS Customer Business Requirements 
Timeline of Changes to Consolidated Trade Summary (CTS) 36 
12. TIMELINE OF CHANGES TO CONSOLIDATED TRADE 
SUMMARY (CTS) 
(The timeline presented is subject to approval by the [[SEC]].) 
• Quarter 1, 2015—Customer Outreach 
o CTS Working Group meetings held 
o Business Requirements published 
o Information sessions held with clients 
• Quarter 4, 2015—Technical specifications available 
o CTS Output File Formats published 
o Customers begin analysis and planning 
• Quarter 1, 2016---CTS Build completion 
o [[DTCC]] and Customers CTS building completed 
o Monthly industry calls held 
• Quarter 3, 2016---[[DTCC]] internal testing underway 
• January 2017---Customer testing 
o Testing between [[DTCC]] and Customer using the new CTS file formats 
• June 2017---Firms convert to the new CTS output file formats 
o Legacy CTS files decommissioned (Hard Cut) 

---

## Page 37

CTS Customer Business Requirements 
Questions and Answers 37 
13. QUESTIONS AND ANSWERS 
Q When Does the Calendar Advance to the Next Day for CTS Processing? 
A Consolidated Trade Summary (CTS) advances to the next available business date after the issuance of 
the CTS cycle 2 daily. 
Q What Files are Being Eliminated Due to the CTS Re-Write? 
A The following AutoRoute Product IDs are scheduled for elimination. 
PUBLISHED 
TIME OF 
DISTRIBUTION  
LEGACY FILE NAME— 
SUNSET 2017  
EXISTING AUTOROUTE 
TEST PRODUCT [[ID]] #  
EXISTING AUTOROUTE 
PRODUCTION PRODUCT [[ID]] # 
22:00 Consolidated Trade Summary  
Main report, Cycle 1  
MRO:  02982354 MRO:  02042354 
Print Image:  02980353 Print Image:  02040353 
01:00 Consolidated Trade Summary  
Supplemental1, Cycle 2  
(Historically empty) 
MRO:  02980954 MRO:  02040954 
Print Image  02980953 Print Image:  02040953 
13:00 Consolidated Trade Summary  
Supplemental2, Cycle 3 
MRO:  02980954 MRO:  02040954 
Print Image:  02980953 Print Image:  02040953 
      
22:00  Foreign [[securities]] Trades  MRO:  02982231 MRO:  02022231 
Print Image: 02980232 Print Image: 02020232 
 
Q What files replace the CTS files that are being sunset? 
A The CTS system has created AutoRoute Product IDs for the CTS files. Each firm should subscribe to 
both the test and production versions of the CTS output files. 
PUBLISHED TIME 
OF DISTRIBUTION  
FILE NAME TEST AUTOROUTE # PRODUCTION AUTOROUTE # 
 
22:00 
01:00 
1300 
Consolidated Trade Summary  
Cycle 1  
Cycle 2 
Cycle 3 
MRO:  02982339 MRO:  02042339 
CSV  02982340 CSV 02042340 
  

---

## Page 38

CTS Customer Business Requirements 
Questions and Answers 38 
Q Is CTS output produced using the same schedule? 
A Yes 
• CTS cycle 1 continues to be produced after close of business on or before 21:00 Eastern Time. 
• CTS cycle 2, typically an empty file, is distributed about midnight Eastern Time. 
• CTS cycle 3 continues to be produced on or before 12:00 Eastern Time. 
Q What fields on the CTS Output are discontinued? 
A The following CTS fields and records have been discontinued: 
• Change in Eligibility–states that the trade was previously marked for another [[settlement]] path. For 
example: a non-[[CNS]] eligible obligation identified by UTC is now [[CNS]] eligible at the time the CTS was 
produced. 
• Bond Indicator-identified a summarized record as Registered or Coupon Bond. 
• Net Record Layout-this data will be provided in a Trade Summary record (Gross Record) and can be 
derived. Net Buy/Sell quantities and values. 
• Control number source—consisted of a limited list of markets 
o Record Non-[[CNS]]; 
o [[OTC]] Foreign; 
o [[ABS]] ([[NYSE]]) Bond; 
o Corporate [[OTC]] [[Bonds]]; 
o Municipal [[Bonds]]; 
o Unit Investment Trust 
• Municipal Balance Order records will not be separated with a unique record identifier.  
• [[participant]] Clearing Agent – Unique to the municipal record, but seldom used. 
• [[participant]] Executing [[Broker]] – Unique to the municipal record, but seldom used. 
• Contra Clearing Agent – Unique to the municipal record, but seldom used. 
• Contra Executing [[Broker]] – Unique to the municipal record, but seldom used. 
  

---

## Page 39

CTS Customer Business Requirements 
Questions and Answers 39 
Q What CTS field values have changed? 
A Field values have been broken out to provide more accurate details: 
• Market codes are consistent with UTC and identify each of the marketplaces, currently 23. For a complete 
list of marketplaces., see the Market Code section. (Expanded from 2 to 3 bytes) 
• Symbol-trading symbol of [[CUSIP]]/ISIN will be on Trade Summary record. (expanded from 4 to 15 bytes)  
• [[CUSIP]]/ISIN-security identifier using 2-byte country code, 9-byte [[CUSIP]], followed by 1-byte check digit. 
(Expanding from 9-byte [[CUSIP]] to 12-byte ISIN) 
• [[Stock]]/Bond-this indicator denotes trade as [[Stock]] or bond.  
• Trade Date–will represent the trade date noted on the trade as received by UTC.  
• [[NSCC]] Receive Date–date the trade was received into UTC, previously known as processing date.  
• Non-[[CNS]], guaranteed/Non-[[CNS]], not guaranteed–used in combination with non-[[CNS]] to denote that an 
obligation is guaranteed (multi-laterally netted) or not guaranteed, meaning bilaterally netted or trade for 
trade.  
• Net Reason Codes 
• When Issued-indicator for identifying the new issuance of a security 
• • Foreign [[securities]]-indicator noting the security is classified as foreign according to the [[DTCC]] security 
master file. 
• As of Indicator--specifies that the trade was submitted with as of attributes. (Previously this field contained 
values for as of, foreign, trade for trade, special trade, and when issued.) 
o T-the receipt date is after trade date 
o S-the [[settlement]] date has been changed by either a trade capture or clearance system at [[DTCC]].  
» The same day settling trade may have been received too late to be included in today’s 
[[settlement]] cycle; therefore, it is assigned the next available [[settlement]] date. 
» The trade today has a [[settlement]] date in the past; therefore, the next available [[settlement]] date 
is assigned. 
» The delivery date and [[settlement]] date on a trade submitted to the CMU RTTM system [[DO]] not 
equal. 
• Step in/out–the step in or step out indicator received by UTC on the trade. 
• Depository--defines the expected location of [[settlement]] 
o [[DTC]]-[[Depository Trust Company]] 

---

## Page 40

CTS Customer Business Requirements 
Questions and Answers 40 
o Other-Any other depository 
• Quantity & Values will be expanded 
• Cash Adjustment Code 
o 02–[[DTC]] Line Code for non-[[CNS]], guaranteed cash adjustments from multi-lateral netting. 
o 23–[[DTC]] Line Code for non-[[CNS]], not guaranteed cash adjustments resulting from bilateral netting. 
• Cash Adjustment will carry a price on a per share or unit basis for each [[CUSIP]].  
Q If a security is ineligible for netting can it be settled in [[CNS]]? 
A [[securities]] ineligible for netting are also excluded from [[CNS]] [[settlement]]. 
Q What is the best practice for [[CNS]] eligible trades submitted to UTC After 11:30 Eastern Time on 
the [[settlement]] date using the Cash Indicator? 
A Trades received by UTC after 11:30 Eastern Time on the [[settlement]] date using the Cash submission 
code are rejected. As a best practice, firms settle the Cash trades as ex-clearing. 
Q What happens when a current price is unavailable on a Non-[[CNS]] security that is eligible for multi-
lateral netting? 
A [[securities]] where the current price is not available may only be bilaterally netted or marked as trade for 
trade, non-[[CNS]], not guaranteed. 
Q If a [[Broker]] submits an X Special Trade indicator to request trade-for-trade [[settlement]] at [[DTC]], how 
does it appear in CTS? 
A [[Broker]] submitted requests for trade for trade processing will be designated as trade for trade, non- [[CNS]], 
not guaranteed. 
Q Does the CTS balance order record show the cash portion of each [[mark-to-market]] difference 
separated from the cash adjustment sent to [[DTC]] [[settlement]]? 
A No. The CTS provides the mark to market difference, but the information flow continues to aggregate all 
cash differences into the daily [[DTC]] [[settlement]] Cash Adjustment (either 02 or 23.)  
 

---

## Page 41

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 