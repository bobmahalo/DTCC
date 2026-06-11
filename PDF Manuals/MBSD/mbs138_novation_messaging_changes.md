---
title: "MBSD RTTM Novation: SWIFT Interactive Messaging Changes"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs138_novation_messaging_changes.pdf"
pages: 35
size: "451.5 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD RTTM Novation: SWIFT Interactive Messaging Changes

**Original File:** [mbs138_novation_messaging_changes.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs138_novation_messaging_changes.pdf)  
**Category:** MBSD  
**Total Pages:** 35  
**File Size:** 451.5 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
MBSD RTTM [[Novation]]: SWIFT INTERACTIVE MESSAGING CHANGES 
VERSION 1.0.7 
JULY 19, 2017 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
This document (the “Document”) is provided as a convenience to members and is for informational purposes only. The 
specific processes and services referenced in this Document are subject to the U.S. [[securities]] and Exchange 
Commission’s approval of the Clearing Rules of the Mortgage-Backed [[securities]] Division (“MBSD”) of the Fixed Income 
Clearing Corporation (“[[FICC]]”). 
 
This Document should not be regarded as a definitive or exhaustive description of [[FICC]]/MBSD’s services or risk-
management framework; nor should it be regarded as a substitute for the Clearing Rules, which govern in all respects, the 
relationship between [[FICC]]/MBSD and its members. In all cases, members should refer to the Clearing Rules for a 
complete statement of [[FICC]]/MBSD procedures, [[obligations]], and requirements. Nothing in this Document shall be deemed 
to impose any [[obligations]] on [[FICC]]/MBSD that are not set forth in the Clearing Rules, and in the case of any discrepancy 
between this Document and the Clearing Rules, the Clearing Rules shall govern. The services and risk-management 
practices described in this Document may be amended at any time without prior notice. 
 
 
Doc Date: July 14, 2017 
Publication Code: MBS138 
Service: Fixed Income Clearing Corporation: 
Title: MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................... 5 
Overview of MBS [[Novation]] ................................................................................................................................. 7 
Changes to SWIFT-Based Interactive Messaging .............................................................................................. 7 
1. Trade Comparison ........................................................................................................................................... 8 
1.1 Trade Submission via RTTM® ...................................................................................................................... 8 
1.1.1 Trade Types ............................................................................................................................................. 8 
[[settlement]] Balance Order Destined (“SBOD”) ................................................................................................ 8 
Trade-for-Trade (“TFTD”) ................................................................................................................................ 9 
TBA Options .................................................................................................................................................. 10 
1.1.2 Minimum/Multiple Par Sizes ................................................................................................................... 10 
1.2 Dealer/Dealer vs. [[Broker]]/Dealer Trade Comparison .................................................................................. 11 
1.2.1 Trade Instructs ....................................................................................................................................... 11 
1.2.2 Trade Comparison .................................................................................................................................. 11 
1.2.3 Comparison (Match) Method .................................................................................................................. 12 
1.2.4 Commission Processing ......................................................................................................................... 13 
1.3 RTTM® Action for Uncompared Trades ...................................................................................................... 13 
1.4 RTTM® Actions for Compared Trades ........................................................................................................ 14 
2. Trade [[Novation]] ............................................................................................................................................... 16 
3. TBA Net ........................................................................................................................................................... 17 
4. [[DO]] Not Allocate (“DNA”) ................................................................................................................................ 18 
5. Pool Notifications ........................................................................................................................................... 20 
5.1 Submission Methods .................................................................................................................................. 20 
5.2 Types of EPN Messages ............................................................................................................................ 20 
5.3 Allocation Processing ................................................................................................................................. 21 
Allocations to TBA Trades ............................................................................................................................... 21 
Allocations to STIP Trades .............................................................................................................................. 22 
5.4 After the Allocation Process ........................................................................................................................ 22 
6. Pool Comparison ........................................................................................................................................... 23 

---

## Page 4

 
 
6.1 Pool Submission via RTTM® ....................................................................................................................... 23 
Automatic Generation in RTTM ....................................................................................................................... 23 
Direct Submission into RTTM ......................................................................................................................... 23 
6.2 RTTM® Actions on Uncompared Pool Instructs .......................................................................................... 24 
6.3 RTTM® Actions for Compared Pool Instructs ............................................................................................. 25 
6.4 EPN Actions on Pool Instructs .................................................................................................................... 26 
6.5 Customer Delivery Requests ...................................................................................................................... 26 
7. Pool Netting .................................................................................................................................................... 28 
8. Pool Conversion ............................................................................................................................................. 29 
STIP Allocations ................................................................................................................................................ 29 
SPT Trades ....................................................................................................................................................... 29 
Cash (Same day) Trades .................................................................................................................................. 29 
9. DNA [[settlement]]/TBA Reprice ....................................................................................................................... 31 
DNA [[settlement]] ................................................................................................................................................ 31 
Expanded Pool Net Results .............................................................................................................................. 31 
Allocation Variance TAP ................................................................................................................................... 32 
TBA Reprice ...................................................................................................................................................... 32 
10. Administrative Messages ............................................................................................................................ 33 
RTTM® Trade Matching and Netting Service Messages .................................................................................. 33 
Pool Comparison and Netting Service Messages ............................................................................................ 33 
 

---

## Page 5

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 5 
VERSION CONTROL PAGE 
Date Version # Name Description of Change 
04/28/2015 0.1 DRAFT C. Swords Initial version 
07/15/2015 1.0 C. Swords Made following changes: 
• Refer to [[FICC]] accounts as FTBA, FSPT and FSTI, rather than FICT, 
FICA and FICB. 
• No longer automatically purge uncompared trades after system-
configured number of days. 
• Add details on how commission reflected in MT518 Trade Novated 
message (separate commission from price) 
• Add details on split/splice matching and introduction of “[[Broker]] match 
identifier” (BASK) to assist in linking dealer trades against a [[Broker]]. 
• Provide DNA matching rules, including trade date and original trade 
par. 
• Provide details on “pool reference” number (EPNX) available on 
allocation message, to flow through to associated Pool Instruct 
Advisories. 
• Provide details on Trade Date validations/usage on Pool Instructs. 
10/15/2015 1.0.1 C. Swords Made following changes: 
• Trade Date missing from table of DNA match criteria 
• Expanded Pool Net selection criteria is “delivery date >= next 
business day” (previously was noted as delivery date > next business 
day). 

---

## Page 6

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 6 
Date Version # Name Description of Change 
2/11/2016 1.0.2 C. Swords Made following changes: 
• Section 1.2.2 Trade Comparison, highlight fact that RTTM- assigned 
Trade [[ID]] is only returned on MT509 Match messages when exact 
matched; split/splice does not return this [[ID]]. However, the Trade [[ID]] is 
always returned in MT518 Trade Novated messages. 
• Section 1.3 RTTM Action for Uncompared Trades, remove comment 
about new TBA trade DK codes associated with STIP trades; existing 
codes will be leveraged. 
• Section 1.4 RTTM Action for Compared Trades, highlight fact that for 
MT515 Cancel post-[[Novation]], RTTM will accept contra as either 
[[FICC]] [[Novation]] account or original [[Broker]]. This is done to minimize 
impact to [[Member]]’s systems. 
• Section 2 Trade [[Novation]], clarify that if GUP tag is submitted on 
[[Novation]]-eligible trade in MT515, this tag will be ignored (rather then 
reject entire message) 
• Section 4 [[DO]] Not Allocate, add 1) support to target specific trades via 
RTTM-defined Trade [[ID]], and remove optional DNA term “original 
trade par”; 2) introduce new message 
• MT518 “DNA Assigned”; 3) indicate that DNA price is to 9 digits; 4) 
clarify that cutoff for DNA submission is when receive MT599 SDNA 
message at approximately 4:30pm on 48 and 24hr day. 
• Section 6.1 Pool Submission via RTTM, add note that matching of 
pool instruct is performed on 1st 6 digits precision only; when 
matched, [[Member]]’s PID is updated to reflect full price and receives 
MT518 “Pool Instruct Matched with Modifications” to reflect this. 
• 6.2 RTTM Actions on Uncompared Pool Instructs, highlight fact that 
“force-compare” message reflects both Pool Instruct creation and 
match; a separate MT509 will not be generated. 
• Section 10 Administrative Messages, corrected typographical error, 
the start/end of Expanded Pool Net code is SEPN and EEPN, 
respectively. 
3/7/2016 1.0.3 C. Swords Made following changes: 
• Corrected [[Novation]] Message tag from 22F::PROC/DTCY/NOVT to 
22F::PROC/GSCC/NOVT. 
• Updated footnotes showing syntax of TRID and EPNX in Special 
Instruction field of ON to reflect that value is enclosed by “=”. For 
example, reference number of “12345” is represented as 
“EPNX=12345=”. 
• One Screen Input DNA Replay message will support create and 
cancel; DNA Create reflected as processing code SCDN + message 
function NEWM; DNA Cancel reflected as processing code SCDN + 
message function CANC. 
3/29/2016 1.0.4 C. Swords Made following changes: 
• Corrected typographical error where mentioned expanded pool net 
runs on CSD, but it runs on CSD-1 
• 9 DNA [[settlement]]/TBA Reprice-Add Variance TAP 
• 4 [[DO]] Not Allocate–indicate that when a DNA is submitted in terms 
only mode, the full trade price to 9 decimal places must be provided. 
If submitted in trade [[ID]] mode, the trade price must still be provided 
but [[FICC]] will only validate the 1st 6 decimal places 

---

## Page 7

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 7 
Date Version # Name Description of Change 
9/21/2016 1.0.5 C. Swords Made following changes: 
• Corrected typographical error where mentioned (page 6) that RTTM-
assigned Trade [[ID]] used for STIP trade allocation was returned in 
MT518 [[Novation]] message via tag 20C::COMM, when it should be 
tag 20C::LIST. 
5/5/2017 1.0.6 C. Swords Made following changes: 
• Section 8 Pool Conversion: provide more details on PID to POID 
pool conversion for STIP trades. 
7/14/2017 1.0.7 C. Swords Made following changes: 
• Section 6.2 RTTM Actions on Uncompared Pool Instructs: add 
footnote to indicate that force compare occurs at various times of 
day. 
• Section 7 Pool Netting: add footnote indicating examples of non-
netting-eligible pool allocations, including SIFMA over-variance 
exception and late turnaround. 
• Section 4 [[DO]] Not Allocate (DNA): update verbiage to indicate that 
DNA Assigned message means DNA has been assigned to 
individual trades; previously, it indicated that this message returned 
individual Trade [[ID]]’s of associated trades but this only occurs for 
DNA submitted via Trade [[ID]] (not terms). 
n/a n/a [[DTCC]] 
Learning 
Updated formatting only. Content is unchanged. 
Overview of MBS [[Novation]] 
The mortgage-backed [[securities]] (MBS) [[Novation]] project is a conversion to operational [[Novation]] and a 
simplification of the netting and [[settlement]] process that will enable MBSD to retire inefficient processing such 
as NOS. It will expand and extend the services rolled out with Pool Netting, which introduced the comparison, 
trade guarantee, netting and CCP [[settlement]] of pool allocations submitted in satisfaction of members’ 
outstanding to be announced (TBA) [[obligations]]. MBSD will continue to require bilateral matching and to 
support dealer-to-dealer and [[Broker]]-to-dealer trade submission. 
Changes to SWIFT-Based Interactive Messaging 
[[FICC]] has updated the existing messaging specifications for trade submission to RTTM® to support the MBS 
[[Novation]] initiative. All messaging input and output was analyzed, and changes limited to minimize [[Member]]-
facing changes. The following document will walk through the new and updated business processes introduced 
with MBS [[Novation]] and the resulting impact to interactive messaging.  
Note: 
This document only highlights the key changes to messaging and is not intended to be an exhaustive source of all 
changes. 

---

## Page 8

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 8 
1. TRADE COMPARISON 
Mortgage-backed [[securities]] are not traded through a formal exchange but rather through the over-the- counter 
market. As such, upon trade execution MBSD members submit all mandatory trade details, in the form of 
Trade Instructs, to MBSD for comparison of the trade details submitted against them by their counterparties. 
The trade comparison service is mandatory for all MBSD Clearing Members. 
The core of MBSD’s trade comparison service is its Real Time Trade Matching® (“RTTM®”) system. This is an 
interactive system that enables members to automate the submission and matching of their trades throughout 
the trading day. 
Using SWIFT-based message formats or web entry, RTTM® provides a common platform for collecting and 
matching trade data, enabling the parties to a trade to monitor and manage the status of their trades in real 
time. The result is a confirmation for trade executions that is legal and binding. 
1.1 Trade Submission via RTTM® 
Members will be able to submit trade input to the RTTM® system via three input media: 
1. SWIFT-based Interactive Messaging (all trade types); 
2. Multi-batch files in SWIFT-based message format (all trade types); 
3. RTTM ® Web Front End (all trade types); or 
4. Proprietary Batch Files (SBOD, TFTD/TBA and OPTN only) 
1.1.1 Trade Types 
The following types of trades will be eligible for MBSD’s trade comparison service: 
[[settlement]] Balance Order Destined (“SBOD”) 
TBA Trades submitted to MBSD for TBA Netting will be submitted as SBO Destined (“SBOD”) and scheduled 
for net according to the SIFMA calendar. SBOD trades must be submitted in eligible TBA [[securities]] and may 
be submitted in round million or odd-lot values. As a result of the net, one or more SBON [[obligations]] will be 
generated for each [[Member]] within each TBA [[CUSIP]]; these SBON will be versus [[FICC]]’s TBA [[Novation]] account 
(referred to as FTBA) at system price. The cash difference between the SBOD trade price and system price will 
be calculated and result in a “TBA”
1 cash obligation, payable on associated SIFMA CSD. Members must 
allocate pools to these SBON trades via EPN during the allocation process, unless excluded from allocation 
through [[DO]] Not Allocate (pair-off) request submitted via RTTM. If allocated, these pools will subsequently be 
eligible for Pool Netting. 
 
1 This new cash obligation type replaces the existing “SBD” cash event. 

---

## Page 9

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 9 
Note: 
The par value (36B::CONF//FAMT) on SBOD submitted via MT515, and reported in MT518, may now be odd-lot or round 
million. 
Trade-for-Trade (“TFTD”) 
Not all trades submitted to RTTM® for comparison are netting destined. Members can also submit trades as 
Trade-for-Trade (“TFTD”), which are trades precluded from TBA Netting. MBSD will have three categories of 
TFTDs: 
1. TFTD TBA: TBA trades may be excluded from the TBA Net for various reasons, including the trade is 
submitted post-TBA netting, or both members agree to not submit the trade as netting destined. Similar to 
SBONs, members must allocate pools to TFTD TBAs via EPN during the allocation process, and these 
pools will subsequently be eligible for Pool Netting. 
2. TFTD with Stipulations (“STIP”): STIP trades are trades in which there is a stipulation on one or more of 
the trade terms. Although members submit trades into RTTM® indicating that they are STIP, the actual 
stipulated terms are unknown to [[FICC]]. STIPs can be submitted in round millions and odd lots. 
Note: 
TFTD STIP (/TDSVSTIP) is a new trade service type that is specified in the MT515 Trade Instruction Processing 
Narrative (70E::TPRO). This information will also be reported in the MT518. 
Members must allocate pools to STIPs via EPN during the allocation process; however, the pools are not 
Pool Netting eligible. As allocations to STIP are not fungible, the specific STIP trade to target must be 
identified on the ON using the RTTM-assigned Trade [[ID]]. 
Note: 
The RTTM-assigned Trade [[ID]] used to identify the STIP trade to target for allocation is always returned to [[Member]] via 
RTTM® Assigned Reference (20C::LIST) in the MT518 [[Novation]] message. 
3. TFTD Specified Pool Trade (“SPT”): A SPT is a trade in which one of the agreed to terms is a specific 
pool and original face. The parties to the trade have a legal obligation to deliver that specified pool in order 
to satisfy the terms of the trade. Members may identify the pool using a variety of means; 1) pool number 
and associated TBA [[CUSIP]], 2) pool [[CUSIP]] or 3) pool number and [[issuer]]. 
Notes: 
• In addition to the pool number, the members may now identify pool [[CUSIP]] (/CUSP) and/or pool [[issuer]] 
(/ISSE) under the pool identification (13B::POOL) tag in the MT515. 
• When a pool is uniquely identified via these new sub-qualifiers, the associated TBA [[CUSIP]] (35B::/US) in the 
MT515 is no longer necessary and may be set to “NONCUSIP”. 
Regardless of which method a [[Member]] utilizes on submission to identify a pool, the system will translate 
this to pool number and associated TBA [[CUSIP]] and reflect this on subsequent output. The pool 
identification methods used by members [[DO]] not have to be the same for trade comparison. 
 

---

## Page 10

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 10 
Note: 
When a pool is uniquely identified via these new sub-qualifiers, the associated TBA [[CUSIP]] (35B::/US) in the MT515 is 
no longer necessary and may be set to “NONCUSIP”. 
SPT trades are not allocated via EPN, since the pool number and original face is already known at the 
time of submission. On the evening before CSD, SPT trades are “converted” meaning that the SPT trade 
is automatically settled (via system-generated NOS) and corresponding receive and delivery pool 
[[obligations]]
2 generated for [[settlement]] at the Clearing Banks on the next business day. 
Note: 
If a SPT is bilaterally matched in RTTM® on CSD or later (e.g. SPT is “as-of”), this conversion will occur immediately 
and in real-time, ready for [[settlement]] at the Clearing Banks. See Section 8:Pool Conversion for details on this 
conversion process. 
TBA Options 
RTTM® compares put and [[Call option]] trades submitted by members. On the evening of expiration date, if the 
members have not already canceled the [[Option]], RTTM® will purge the [[Option]] trade regardless of whether it is in 
or out of the money. 
Note: 
Options will no longer be eligible for [[Broker]] submission via any method, including MT515. As such, sub-qualifier 
(/TDSVOPTN) in the Trade Instruction Processing Narrative (70E::TPRO) can longer be used for [[Broker]] trade instructs. 
Members [[DO]] not allocate pools to [[Option]] trades, and [[FICC]] will not novate [[Option]] trades. [[FICC]] will not 
systemically generate a TBA trade for an in-the-money [[Option]], nor calculate or process any money movements 
associated with the execution or expiration of an [[Option]] trade. 
1.1.2 Minimum/Multiple Par Sizes 
There are different minimum and multiple rules for the various trade types. The table below lists the minimum 
and multiple amounts for each trade type. The maximum trade size for RTTM® submission is unchanged from 
today, set at a dollar less than 10 billion, i.e. $9,999,999,999. 
Trade Type Minimum Par Multiple Par Maximum Par 
SBOD 1000 1.00 9,999,999,999 
TFTD TBA 1000 1.00 9,999,999,999 
TFTD SPT 1,000/25K original face3 1.00 9,999,999,999 
TFTD STIP 1000 1.00 9,999,999,999 
OPTN 1,000,000 1,000,000 9,999,000,000 
 
2 These are also known as “Pool [[obligations]]” (POID). 
3 Minimum differs based on product. 

---

## Page 11

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 11 
Note: 
For all TFTD trades, the minimum is now 1,000 and multiple of 1.00, as specified in the par value (36B::CONF//FAMT) in 
MT515 “Trade Instructs” and corresponding MT518 advisories. 
1.2 Dealer/Dealer vs. [[Broker]]/Dealer Trade Comparison 
Regardless of the legal entity type of the MBSD [[Member]], from a system perspective, MBSD supports two 
types of trade submission and comparison: 
• Dealer vs. Dealer: These are trades executed directly between two Dealers, as principal. 
• [[Broker]] vs. Dealer: These are trades executed between two Dealers ([[Buyer]] and [[Seller]]), as principal, 
facilitated by a [[Broker]], acting as agent. 
1.2.1 Trade Instructs 
All members submit trade details in the form of “Trade Instructs.” RTTM® validates all trade submissions upon 
entry, regardless of the method of input. Certain fields are required on Trade Instructs; if any mandatory fields 
are missing, RTTM
® will reject the trade. 
Note: 
The reject codes/reasons reported in the MT509 “Trade Instruct Rejected” message (25D::IPRC//REJT) have been updated 
in support of [[Novation]]. 
When a dealer trade instruct is submitted successfully, RTTM® immediately assigns the trade a unique 
Transaction [[ID]] number. [[Broker]] trades, on the other hand, must be “balanced”, meaning that trade instructs for 
both sides of the trade have been submitted. Once a [[Broker]] trade is balanced, RTTM® will assign the [[Broker]] 
trade a Transaction [[ID]]. These Transaction IDs are used by members to identify their unmatched trades. 
As soon as a dealer trade, or balanced [[Broker]] trade, is created and assigned a Transaction [[ID]], an “advice” is 
generated for the counterparty to notify them that activity has been submitted against them. 
1.2.2 Trade Comparison 
When a dealer trade is submitted, RTTM® will compare the terms of the trade against previously submit 
counterparty trades and if they match, the Transaction [[ID]] will be replaced by a unique RTTM-assigned Trade 
[[ID]]. The dealer trade is considered “matched” (also referred to as “compared”). This occurs regardless of 
whether the counterparty on the dealer trade is a dealer or [[Broker]]. 
Note: 
When a trade is matched, [[FICC]] will send the Dealer an MT509 “Trade Matched” message (:25D::MTCH//MACH). This 
MT509 may contain the MBSD assigned Trade [[ID]] (20C::COMM), indicating the new identifier for the compared trade, 
depending on match “mode” (see next section) on Comparison Methods. 
Because [[Broker]] trades are two-sided, they go through a two phase match process; when one side of a [[Broker]] 
trade matches a dealer trade, the [[Broker]] trade is “partially matched” (PMAT); when the other side of the [[Broker]] 

---

## Page 12

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 12 
trade matches, the [[Broker]] trade is now “fully matched” (FMAT). When these match event occur, the [[Broker]] 
trade Transaction [[ID]] will be replaced by a unique RTTM-assigned Trade [[ID]]. 
Note: 
When a [[Broker]] trade is partially matched, [[FICC]] will send the [[Broker]] an MT509 “Trade PMAT–Short” 
(:25D::MTCH/DTCY/MAPS) or MT509 “Trade PMAT–Long” (:25D::MTCH/DTCY/MAPL), depending on if the [[Broker]] sell or 
buy side matched. When the unmatched Dealer of a PMAT trade matches the [[Broker]], the [[Broker]] will receive an MT509 
“Trade Fully Matched” message (:25D::MTCH/DTCY/MAFM). These MT509 will contain the RTTM® assigned Match Trade 
[[ID]] (20C::COMM), indicating the new identifier for the compared trade. 
1.2.3 Comparison (Match) Method 
MBSD will first attempt to compare each trade based on all trade terms matching exactly; this involves a single 
buy and sell trade. 
Note: 
When a trade is matched via exact match, the MT509 “Trade Matched” message will contain the RTTM-assigned identifier in 
the Trade [[ID]] (20C::COMM) field. 
If an exact match is not found and the trade is a brokered trade, MBSD will then apply the Net Position Match 
logic which involves multiple trades and requires the total net par of a set of trades with the same terms to 
match. In order to achieve Net Position Match, a process called “split/splice” is used. Once RTTM
® identifies a 
set of trades that match on net position, it will “split” or “splice” the Dealer’s trades to match the [[Broker]]’s trades. 
Specifically, MBSD will cancel the Dealer trades, and create new Dealer trades that exactly match the [[Broker]]’s 
submissions
4. 
Notes: 
• Currently, when split/splice matching occurs, [[FICC]] generates MT509 “Trade Matched” messages for each dealer 
trade matched/canceled, and MT518 “Comparison Request Cancel (due to match)” for the advisories the new 
dealer trades matched against. The generation of the new dealer trades does not get reported via SWIFT.  
 
Note, however, the new dealer trades created are subject to [[Novation]] and as such, will result in MT518 “Trade 
Novated” message once [[Novation]] occurs–see Section 2 for details. 
 
To assist members in linking trades involved in a match versus a [[Broker]], whether subject to split/splice or exact 
match, [[FICC]] will now generate a “[[Broker]] match identifier” for each match event versus a [[Broker]], and return this 
common identifier in the match, advisory cancel and [[Novation]] messages above (using tag 20C::BASK). 
• When a trade is matched via split/splice match, the MT509 “Trade Matched” message will not contain the RTTM-
assigned Trade [[ID]]; however, this identifier will be returned in the MT518 “Trade Novated” message 
(:22F::PROC/GSCC/NOVT). 
Not all trades are eligible for Net Position Match. 
• Net Position Match is only applied to Dealer vs. [[Broker]] trades 
 
4 For original Dealer trades that are “split” into multiple smaller trades, the replacement trades will have the same XREF as the original trade; for trades that are 
“spliced” into a single trade, the XREF will be blank. 

---

## Page 13

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 13 
• Net Position Match is only applied to SBOD and TFTD/TBA trades 
• STIP and SPT trades are not eligible for Net Position Match (a.k.a. “split/splice” processing). 
Note: 
STIP trades are a new type of trade introduced in [[Novation]] and may be matched via exact match only on a 1-1 basis. 
1.2.4 Commission Processing 
Brokers may charge the Dealers with whom they trade a commission. The commission information may be 
included by the submitting [[Broker]] and Dealer upon trade submission to RTTM®. MBSD collects all 
commissions on a monthly basis from the Dealers and passes the money to the Brokers. Commission is 
paid/collected the month following the CSD of the trade on Class B [[settlement]] date for matched trades. 
MBSD processes rate-based commission only, in which the [[Broker]] always submits the price exclusive of 
commission, whereas Dealers can submit the trade price either inclusive or exclusive of commission. 
Note: 
Flat commission will be eliminated with MBS [[Novation]]. As such, flat charges indicator (22F::CATB//FLAT) is no longer 
available. 
1.3 RTTM® Action for Uncompared Trades 
A trade will remain uncompared if either party to the trade has not submitted their side of the trade to RTTM® or 
if the terms of the submitted trade [[DO]] not match the terms of the counterparty’s trade submission. 
After a Trade Instruct has been submitted to RTTM®, but before it has been bilaterally compared, members can 
Affirm, DK, Cancel or Modify the Trade Instruct. 
• Affirms (Dealers Only): Affirms are used by Dealers to ‘agree’ to a counterparty’s Advice resulting in a 
compared trade. An Advice is a notification that an activity has been submitted against a [[Member]] by its 
counterparty. 
• DKs (Brokers and Dealers): A DK may be submitted by either the [[Buyer]] or the [[Seller]] to inform its 
counterparty via a DK Advice that it “does not know” (or that the [[Member]] disagrees with the terms of) the 
Trade Instruct being submitted. This will result in the Trade Instruct being assigned a “DK” state in the 
system. Counterparties must take action to resolve DK states by reviewing the terms of a submitted Trade 
Instruct and, if necessary, canceling and resubmitting the Trade Instruct. Once a Trade Instruct is 
compared, a DK cannot be submitted against it. 
Once the DK has passed all validations, the targeted Trade Instruct will be placed in a DK state but will 
remain eligible for comparison; DKs are informational only. If a [[Member]] has submitted the DK in error, it 
may submit a new Trade Instruct for bilateral matching against the counterparty’s Trade Instruct that is in 
the DK state, or it can affirm the Advice via RTTM
® Web. 
• Cancels (of Uncompareds): This action is used by members to delete their uncompared trades. 
Uncompared trades can be canceled unilaterally by the submitting [[Member]]. 
• Modify (Dealer): Dealers cannot modify uncompared trades. They must cancel the Trade Instruct and 
then resubmit. 

---

## Page 14

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 14 
• Modify ([[Broker]]): For PMAT trades, Brokers can use the “modify” action to update an XREF and/or to 
correct the uncompared side of a PMAT trade when the correction required is due to an erroneous 
counterparty or commission. 
Note: 
Currently if the [[Broker]] modifies the XREF of a PMAT trade, the DK status will be removed from the trade. With MBS 
[[Novation]], the DK status will only be removed if trade terms are modified on a PMAT trade (i.e. counterparty or 
commission). 
1.4 RTTM® Actions for Compared Trades 
A trade will become compared if both parties to the trade have submitted their side of the trade to RTTM® and if 
the terms of the submitted trade required for comparison match the terms of the counterparty’s trade 
submission. 
There are limited RTTM
® actions for compared trades. A compared (or matched) Trade Instruct may be either 
canceled or modified, as described below. 
Note: 
Once a dealer receives an MT518 “Trade Novated” message (:22F::PROC/GSCC/NOVT), any action targeting the novated 
trade should contain the same trade details as reflected in the message, i.e. the counterparty must be designated as the 
appropriate [[FICC]] [[Novation]] account, not the original counterparty on the trade. 
The exception to this is cancel of a novated trade, where RTTM will not reject a Cancel record targeting a brokered trade 
with an incorrect contra party due to [[Novation]]. In other words, Dealers can either submit the original [[Broker]] or the [[FICC]] 
[[Novation]] account on the MT515 Cancel submitted to RTTM, as appropriate for their systems. 
• Modify (Brokers and Dealers): Brokers and Dealers can modify a fully matched trade to update the 
XREF, but for any other modifications, the trade must be bilaterally canceled and resubmitted. 
Cancels: Since MBSD requires bilateral matching, where both parties to the trade must agree to the 
terms of the trade for it to be considered valid, in order for a compared trade to be canceled, the same 
parties to the trade must also agree to the cancel. A trade will remain compared until the cancel is 
matched. 
Once a trade is novated, the dealer must submit the cancel against the appropriate [[FICC]] [[Novation]] 
account; the cancel will be forwarded to the original counterparty. Only if both dealers agree to the cancel 
will the trades be canceled. 
Trades can only be canceled during certain periods in a trade’s lifecycle, as indicated below. 
 
Trade Type Period Cancel Allowed 
SBOD Must be canceled prior to onset of associated TBA net. 
TFTD/TBA Unallocated TFTD/TBA can be canceled prior to 48hr day only. 
TFTD/STIP Unallocated TFTD/STIP can be canceled prior to CSD only. 

---

## Page 15

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 15 
Trade Type Period Cancel Allowed 
TFTD/SPT TFTD/SPT can be canceled prior to CSD only5. 
OPTN OPTN can be canceled until end-of-day before expiration date, at which time RTTM® will 
automatically purge. 
Note: 
The cancel rules governing TFTD/TBA and SPT trades have changed in support of the [[Novation]] service. The reject 
codes/reasons reported in the MT509 “Cancel Rejected” message (25D::IPRC//REJT) have been updated 
appropriately. 
• Uncancels: The [[Member]] submitting a Cancel Request can change its mind and “uncancel” a trade, as 
long as the counterparty has not already compared the “Cancel Request”. If a [[Member]] submits an 
“Uncancel,” the trade will revert to the (previous) compared state. 
• DKs of Cancels: A “DK of Cancel Request” may be submitted by either the [[Buyer]] or the [[Seller]] to inform 
its counterparty via a “DK of Cancel Request Advice” that it “does not know” the Cancel Request being 
submitted. This will result in the Cancel Request being assigned a “DK” state in the system. The DK will 
only be removed if the trade is bilaterally canceled or if the Cancel is removed (via an Uncancel action). 
 
5 The SPT trades can be canceled up to 4:30pm, when the Pool Conversion process is run. See Section 8:Pool Conversion for details. 

---

## Page 16

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 16 
2. TRADE [[Novation]] 
For Dealer vs. Dealer trades, when both parties to a trade have submitted their side of the trade to [[FICC]], and 
all fields required for comparison match exactly, the trade will achieve a matched (compared) state. [[FICC]] will 
novate the Dealers’ trade upon comparison and become the counterparty to the trade, i.e. [[FICC]]’s [[Novation]] 
account will become the [[Buyer]] to every [[Seller]] and the [[Seller]] to every [[Buyer]]
6. 
For [[Broker]] vs. Dealer trades, only fully matched (“FMAT”) trades will be novated. The counterparty to each 
Dealer trade will become a [[FICC]] [[Novation]] account, and this account will be listed as the counterparty on all 
trade output. As stated earlier, [[FICC]] will only novate FMAT trades and will not novate versus a [[Broker]]. 
[[FICC]] will utilize separate [[Novation]] accounts for TBA, SPT and STIP activity, referred throughout this document 
as indicated below
7. 
FTBA [[FICC]] [[Novation]] account for generic TBA trades (TFTD/TBA) and SBON [[obligations]]. 
FSPT [[FICC]] [[Novation]] account for SPT trades 
FSTI [[FICC]] [[Novation]] account for STIP trades 
 
Once [[Novation]] occurs, members will be notified of this event, along with the new counterparty. 
Notes: 
• Dealers will receive an MT518 “Trade Novated” message (:22F::PROC/GSCC/NOVT) when a trade is novated. 
Brokers will not receive this message, since only Dealer trades are novated. The MT518 “Trade Novated” 
message will contain all trade details, and any action targeting a novated trade (e.g. Cancel Request) must 
contain the same trade details as reflected in the message. 
 
Note that when a dealer has submitted a brokered trade with a price inclusive of commission, the [[Novation]] 
message will reflect the price exclusive of commission in the price field (90A::DEAL/PRCE) and commission value 
in amount field (19A::LOCO//USD) 
• S ince [[FICC]] is novating all FMAT brokered trades, the Give- Up (“GUP”) process will be eliminated. As such, the 
number of GUP days will be removed as a trade input field (70E::TPRO/tag, sub- qualifier /GUPP) on the MT515 
and corresponding MT518; if included in a MT515 [[Novation]]- eligible trade, this tag will be ignored. 
 
6 [[Option]] trades are not novated. 
7 These are account mnemonics only; they [[DO]] not represent the actual account names that will be used. 

---

## Page 17

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 17 
3. TBA NET 
Fully matched (and therefore novated) SBOD trades are processed through MBSD’s TBA netting service, 
which is run according to the SIFMA calendar on 72hr day. This netting service supports SBOD trades submit 
in GDM as well as odd-lots and will result in one or more SBON [[obligations]] versus [[FICC]]’s TBA [[Novation]] 
account (FTBA) priced at the TBA [[CUSIP]]’s “system price”8. A “TBA” cash differential will be generated to 
account for the difference between SBOD trade price and system price. 
Note: 
The TBA Net has been expanded in the [[Novation]] service to include odd-lot netting. In addition, all resulting [[obligations]] will 
be versus [[FICC]]’s TBA [[Novation]] account (FTBA) and therefore result in SBON [[obligations]] (SBO versus non-original 
counterparty); SBOO [[obligations]] (SBO versus original counterparty) will no longer be generated. 
 
8 The TBA [[CUSIP]] “system price” is the prior day’s [[EOD]] price, which is the same as the current day’s pool net price. 

---

## Page 18

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 18 
4. [[DO]] NOT ALLOCATE (“DNA”) 
When members have two or more offsetting SBON and/or TFTD/TBA positions with the same TBA [[CUSIP]] and 
CSD, they may “pair-off” these positions and exclude them from the allocation process, thereby avoiding the 
need to make delivery of these pools. This process, referred to as “[[DO]] Not Allocate (DNA)”, is available for 
trades settling on SIFMA CSD only and may be submitted via RTTM® on 48hr and 24hr day from opening until 
the cutoff at approximately 4:30pm. As the offsetting positions may have different prices, a cash differential 
called DNA will be generated to account for the differences. 
Note: 
The cutoff for DNA submission and, on 48hr day, start of DNA [[settlement]] is announced via the MT599 “Start of Pool 
Conversion, DNA [[settlement]] and TBA Reprice” (/GSCC/SDNR) message. It is anticipated to begin at 4:30pm, after EPN 
close. 
A DNA can be submit in 2 “modes”; a) terms only mode means members specify terms of the buy/sell 
positions to target and RTTM® will select the specific trades to assign the DNA to; and b) trade [[ID]] mode 
means members specify trade terms as well as specific trades to target. 
The DNA fields are listed in the table below. 
 Field Name Description 
TBA Terms: Common trade terms for the DNA requested 
1 Account [[ID]] Account identifier 
2 CSD Contract [[settlement]] date 
3 TBA [[CUSIP]] TBA [[CUSIP]] (9 characters) 
Sell Terms: The [[Seller]] price, trade date and amount of par to DNA, with optional Trade [[ID]] of specific trade to target. 
These fields are repeating, with at least 1 sell specified per DNA. 
4a Price Trade price 
4b Trade Date Trade date 
4c Par Par to DNA 
4d Trade [[ID]] Trade [[ID]] of targeted trade-Optional 
Buy Terms: The [[Buyer]] price, trade date and amount of par to DNA, with optional Trade [[ID]] of specific trade to target. 
These fields are repeating, with at least 1 buy specified per DNA. 
5a Price Trade price 
5b Trade Date Trade date 
5c Par Par to DNA 
5d Trade [[ID]] Trade [[ID]] of targeted trade-Optional 
Reference: [[Member]] identification 

---

## Page 19

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 19 
 Field Name Description 
6 DNA Reference [[Member]]-specified unique DNA reference number, used for members to uniquely 
identify their DNA submissions. 
 
As can be seen above, members identify the general trade terms of account, CSD and TBA [[CUSIP]], then detail 
the specific buy/sell prices and trade date to target, along with par amount to DNA. Members may also identify 
specific trades to assign the DNA to by providing associated Trade Ids; if no target Trade Ids are provided, 
RTTM will select trades to assign the DNA to from among those with matching terms. 
Note: 
When a DNA is submitted in terms only mode, the full trade price to 9 decimal places must be provided. If submitted in 
trade [[ID]] mode, the trade price must still be provided but [[FICC]] will only validate the 1st 6 decimal places. 
The DNA may specify sell versus buy positions on a 1-1, 1-many, many-1 and many-many relationship; 
however, the request must be balanced, i.e. total buy par = total sell par. 
Note: 
Members can submit DNA Requests via a MT515 “[[DO]] Not Allocate Request” Message (22F::PROC/GSCC/DNAL). They 
will receive a MT509 “DNA Accepted” Message in response (25D::IPRC/GSCC/DNAL), along with RTTM-assigned DNA 
identifier (20C::LIST). This message will be followed by a MT518 “DNA Assigned” Message (25D::IPRC/GSCC/DNAP), 
indicating that the DNA has been assigned to specific trades as targeted by user (if DNA submitted in “trade [[ID]]” mode) or 
trades selected by RTTM
® (if DNA submitted in “terms” mode). 
If the [[Member]] submits the DNA Request via RTTM® Web, they will receive a MT518 “Screen Input DNA Replay” Message 
(22F::PROC/GSCC/SDNA, message function NEWM) to enable the [[Member]] to load the DNA details into their system, 
including Trade [[ID]] assignment details. 
[[FICC]] will validate the request to ensure there is enough position matching the terms specified to support the 
request and in a manner that conforms with SIFMA Good Delivery Guidelines. 
When successfully submitted, RTTM® immediately assigns the request a unique DNA [[ID]]. This identifier may be 
used to identify their DNA requests, along with the [[Member]] supplied XREF. 
If, after submission, a [[Member]] wishes to cancel their DNA request, they may [[DO]] so up until the DNA request is 
settled by the system during the “DNA [[settlement]] and TBA Reprice” process, run in the afternoon prior to 
CSD. 
Note: 
Members can submit DNA Cancel Requests via a MT515 “[[DO]] Not Allocate Cancel Request” Message 
(22F::PROC/GSCC/CDNA), along with [[Member]]-specified XREF or RTTM-assigned DNA [[ID]]. They will receive a MT509 
“DNA Cancel Accepted and Processed” Message in response (25D::IPRC/GSCC/CDNA). 
If the [[Member]] submits the DNA Cancel Request via RTTM® Web, they will receive a MT518 “Screen Input DNA Replay” 
Message (22F::PROC/GSCC/SDNA, message function CANC) to enable the [[Member]] to record the cancel in their system. 

---

## Page 20

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 20 
5. POOL NOTIFICATIONS 
MBSD’s Electronic Pool Notification (“EPN”) service is used by sellers to convey details of pools they will 
deliver in satisfaction of their TBA [[obligations]]. 
For the TBA trade to be eligible for [[settlement]] on CSD, the [[Seller]] must notify the [[Buyer]] of the mortgage pools it 
plans to deliver by 3:00 p.m. (ET) on 48-hour day. Given the time sensitive nature of the allocation process, all 
EPN messages are time-stamped and EPN applies multiple time-stamps to messages, including the official T2 
time-stamp which used to determine good delivery, i.e. the pools were allocated prior to 3:00 p.m. (15:00:01 is 
late delivery). 
As central counterparty to all TBA trades, allocations must be submitted by sellers versus the appropriate [[FICC]] 
[[Novation]] account. Once validated for message structure, [[FICC]] will perform validations to ensure the allocation 
conforms to SIFMA Guidelines and associated TBA position exists in the system. [[FICC]] will then turn the 
allocation to one or more matching buyers, and submit the allocations to the RTTM Pool Comparison system 
for further processing (see Section 6:Pool Comparison below). 
Note: 
Previously, [[FICC]] only validated the content of the messages to ensure they conformed to the message structure 
requirements; it was the buying [[Member]]’s responsibility to DK an allocation if it did not meet good-delivery guidelines or the 
terms of the trade. As counterparty to all allocations, [[FICC]] will now perform full business rule validations and DK the [[Seller]] 
as necessary. 
5.1 Submission Methods 
There are two methods for submitting pool information via EPN: 
1. EaSy Pool (ESP): EaSy Pool is a Web-based application for EPN message entry, message display, 
reporting, and administration. 
2. Computer-to-Computer Interface (CTCI): This interface provides an on-line, real-time, automated 
message exchange with EPN. 
5.2 Types of EPN Messages 
EPN users may exchange different types of messages to accomplish notification. 
• Original Notification (“ON”): Used by the [[Seller]] to notify the [[Buyer]] of the pools it will deliver for an 
outstanding TBA position. 
• Cancel & Correct (“CC”): Also known as the Pool Substitution message, this message allows a [[Seller]] to 
notify the [[Buyer]] to disregard the pools from a previously submitted ON message and to replace those 
pools with the new pool details provided in the CC message. 
• Don’t Know (“DK”): Used by the [[Buyer]] to notify a [[Seller]] that it does not agree with the terms of the 
previously sent ON. Buyers can also DK a CC for replacement pools or other valid DK reasons. 
• Cancel (“CX”): Used by the [[Seller]] to notify a [[Buyer]] to disregard the terms of a previously sent ON. 

---

## Page 21

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 21 
Note: 
As allocations submitted to [[FICC]] are fully validated and turned to subsequent buyers, once accepted by [[FICC]] they can no 
longer be canceled by the sellers. In other words, cancel “CX” messages submit by sellers versus a [[FICC]] [[Novation]] account 
will be rejected by EPN, and never generated by [[FICC]]. 
5.3 Allocation Processing 
EPN messages are limited to a maximum number of good delivery millions and pools. Each message has two 
main components: 1) the header, which contains information pertaining to the TBA trade, and 2) the pool detail, 
which contains the information for the allocated pools. The pools are allocated in “lots”, with terminators 
designating where a lot begins and ends. 
Note: 
As mentioned, pool allocations submitted via EPN will automatically be fed to the RTTM Pool Comparison system for 
further processing (see Section 6 for details). To assist reconciliation between EPN and RTTM Pool Comparison systems, 
a “pool reference” number may be defined for each allocation in EPN9, which will be passed to the Pool Comparison 
system and reflected in subsequent SWIFT MT518 messaging for the associated pool advisory/instructs using a new “pool 
reference” qualifier in the existing “trade processing narrative” field (70E::TPRO/EPNX). 
Note that the pool reference is [[Member]]-specified by sellers (as they submit into EPN), and generated by [[FICC]] for buyers 
(as [[FICC]] generates the EPN allocation for buyers). 
Allocations to TBA Trades 
Members allocate to TBA trades by specifying matching trade terms. [[FICC]] will ensure that there is sufficient 
position in the system among matching SBON and TFTD/TBA trades, and that the allocation adheres to SIFMA 
Guidelines. Once validated, these allocations are turned by [[FICC]] to one or more matching buyers and the 
corresponding TBA trade positions decremented; if allocated within SIFMA variance, the TBA trades are 
automatically closed. 
Note: 
Allocations to TBA trades received by [[FICC]] with incorrect delivery date are not adequate grounds for an automatic DK. 
[[FICC]] will adjust the date per SIFMA Guidelines and report the corrected date in the allocations turned to the [[Buyer]](s). 
Allocations to TBA trades may be submitted as GDM lots and, for the residual tail, as odd-lot. 
Note: 
Allocations to TBA trades with bad-lot terminators are not supported by [[FICC]] and will be DK’ed. 
 
9 This information is specified in the EPN pool details “special instructions” field for ON or replacement pool on CC, using format “EPNX=value=” For example, 
a reference of “1234567890” is represented as “EPNX=1234567890=”. 

---

## Page 22

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 22 
Allocations to STIP Trades 
Members allocate to STIP trades by uniquely identifying the STIP trade to target. 
Note: 
The Trade [[ID]] must be specified in the special instructions field of EPN message header10. This Trade [[ID]] is assigned to a 
fully matched and novated trade by [[FICC]] and returned to the [[Member]] via SWIFT messaging in the MT518 “Trade Novated” 
message (:22F::PROC/GSCC/NOVT). 
[[FICC]] will ensure that there is sufficient position in the targeted trade, but as [[FICC]] has no knowledge of the 
actual stipulations associated with the trade, will not verify against full SIFMA Guidelines11. [[FICC]] will turn the 
allocation to the [[Buyer]] on the STIP trade, and it is the sole responsibility of the receiving [[Member]] to DK the 
allocation if it does not meet the agreed upon terms. 
Note: 
Previously, STIP trades were booked as generic TBA and settled away from [[FICC]]. With the introduction of STIP trade 
processing in [[Novation]], all allocations and subsequent settlements will occur thorough [[FICC]] as central counterparty. 
Once turned to the appropriate [[Buyer]], the corresponding STIP trade position is decremented. Unlike 
allocations to generic TBA trades, STIP trades are subsequently closed (fully decremented) differently, based 
on terminator logic. 
• Stipulated trades that are out of SIFMA variance are closed using bad-delivery (a.k.a. bid-list) terminator 
8889. When received by [[FICC]], this indicates that the STIP is fully allocated and should be closed; it is not 
subject to SIFMA variance. 
• STIP trades subject to standard variance are allocated using GDM or odd-lot terminators, in the same 
manner as generic TBAs. [[FICC]] will automatically close the trade once it is allocated within SIFMA 
variance. 
5.4 After the Allocation Process 
After members have allocated mortgage pools to their TBA SBON and TFTD positions, the pools are then 
eligible for MBSD’s Pool Comparison and Netting services, which are explained in Section 6: Pool Comparison 
and Section 7: Pool Netting respectively. 
Allocations to STIP trades are eligible for MBSD’s Pool Comparison and Conversion service, as described in 
Section 6: Pool Comparison and Section 8: Pool Conversion respectively. 
 
10 The format is “TRID=value=” For example, “TRID=1234567890= “. 
11 [[FICC]] will not validate SIFMA variance when allocated using bad-delivery (bid-list) terminators, nor validate pool counts per lot (regardless of how 
allocated/lot terminators) 

---

## Page 23

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 23 
6. POOL COMPARISON 
MBSD’s Pool Comparison service is used to communicate pool details (in the form of Pool Instructs) to 
members based on their allocations submitted via EPN. In addition, it allows members to designate pool 
allocations that should be precluded from being “netted away” via netting, resulting in the [[settlement]] of a pool 
obligation between the [[Member]] and [[FICC]]. 
6.1 Pool Submission via RTTM® 
Pool input is generated in RTTM® through two methods: 1) automatically via EPN submissions and 2) directly 
into RTTM® via various input media. 
Automatic Generation in RTTM 
All allocations versus [[FICC]] processed through the EPN system result in an “advice” being generated in RTTM® 
notifying the [[Member]] of that an activity has been submitted against them from [[FICC]]. These allocations are fully 
validated by [[FICC]] and may contain additional or corrected pool details, not provided on the [[Seller]] [[Member]]’s 
allocation. 
Notes: 
• The advice is communicated as an MT518 “Comparison Request” (22F::PROC/DTCY/CMPR). To assist 
reconciliation between EPN submissions and corresponding “advices”, members may optionally specify a “pool 
reference” number for each allocation in EPN1212, which will be reflected in the advisory using a new “pool 
reference” qualifier in the existing “trade processing narrative” field (70E::TPRO/EPNX). 
• Trade details provided in an EPN allocation are reflected in the pool MT518 “Comparison Request” 
(22F::PROC/DTCY/CMPR). This includes the full trade price of 9 decimal places. 
 
Note, However, when a [[Member]] submits an allocation with incorrect delivery date, [[FICC]] will automatically adjust 
the date per SIFMA Guidelines and report this change back to the members in the corresponding pool MT518 
“Comparison Request” (22F::PROC/DTCY/CMPR). 
If this advisory remains uncompared at the end of the processing day, [[FICC]] will automatically generate a 
matching “Pool Instruct” on the [[Member]]’s behalf. 
Note: 
Members are no longer required to submit Pool Instructs directly into the RTTM® system, though they may optionally 
choose to [[DO]] so. These submissions are no longer required as [[FICC]] will automatically generate matching pool instructs 
based on EPN submissions. 
Direct Submission into RTTM 
 
12 As previously indicated, this information may be specified in the EPN pool details “special instructions” field for ON and replacement pool on CC, using 
format “EPNX=value=”. For example, a reference number of “REFABC” is reflected as “EPNX=REFABC=”. 

---

## Page 24

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 24 
Members may also submit pool input (and associated actions) directly into RTTM® via three input media: 
1. SWIFT-based Interactive Messaging; 
2. Multi-batch files in SWIFT-based message format; 
3. RTTM ® Web Front End. 
 
RTTM® will validate these pool submissions upon entry, regardless of the method of input. Certain fields are 
required on Pool Instructs; if any mandatory fields are missing, RTTM® will reject the trade. 
Note: 
In the MT515 “Pool Instruct” message, the Trade Date (98C::TRAD) will no longer be ignored but rather validated to ensure 
that it is a valid calendar date. 
When a pool instruct is submitted, RTTM® will compare the terms of the instruct against previously received 
advisories and if all pool details are the same (price up to 6 digit precision only), the instructs are considered 
“matched” (also referred to as “compared”). 
Notes: 
• In the MT515 “Pool Instruct” message, the Trade Date (98C::TRAD) is now a matching field for comparison (date 
portion only; time is not used for matching). 
• When a Pool Instruct and advisory are matched with price differences in the 7-9th digit precision, the [[Member]]’s 
Pool Instruct is updated to reflect the full price (as specified in the advisory). As done today, the members will 
receive a MT518 “Pool Instruct Matched with Modifications” (22F::PROC/DTCY/CMPM) to reflect this. 
• As allocations submitted via EPN result in [[Member]] “advisories”, pool instructs submitted directly into RTTM® 
should automatically compare against these EPN-initiated advisories, as long as the terms specified in the 
allocation and instruct match. 
 
If the information submitted on the ON and Pool Instruct are not the same, the corresponding [[FICC]] advisory and 
pool instruct will not match; the pool instruct will be uncompared in the system. As previously mentioned, if the 
advisory remains uncompared at the end of the processing day, [[FICC]] will automatically generate a matching “Pool 
Instruct” on the [[Member]]’s behalf. 
 
Note, when [[FICC]] adjusts the delivery date on the allocation per SIFMA Guidelines, the pool instruct submitted 
must contain the corrected date or comparison versus the advisory will not occur. 
6.2 RTTM® Actions on Uncompared Pool Instructs 
A Pool Instruct submit directly into RTTM® will remain uncompared if the [[Member]] has not submitted an EPN 
allocation with matching terms. 
After a Pool Instruct has been submitted to RTTM®, but before it has been compared, members can Cancel or 
Modify the Pool Instruct or add a CDR. 
• Cancels (of Uncompareds): This action is used by members to delete their uncompared pool instructs. 
Uncompared instructs can be canceled unilaterally by the submitting [[Member]]. 

---

## Page 25

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 25 
• Modify: With the exception of the CDR field (explained later in 6.5 Customer Delivery Requests), 
members may modify any of the data on their previously submitted Pool Instruct, prior to comparison. 
 
Pool Instruct “Advisories” resulting from EPN allocations remain uncompared in RTTM® until the [[Member]] 
affirms the advisory, submits a matching Pool Instruct or the system force-compares on [[Member]]-behalf. 
• Affirms: Affirms are used by Members to ‘agree’ to a contra-side Advisory resulting in a matched pool. 
Affirms are only possible via RTTM® Web. In order to match a pool via other methods of input, members 
must submit Pool Instructs. 
Note: 
DK of Pool Instruct “Advisories” is no longer a supported action as all advisories are automatically generated based on 
[[Member]] allocations submitted via EPN. DK requests were previously available via MT515 “DK Request” 
(22F::PROC/DTCY/TDDK). 
If a [[Member]] elects to bypass affirming or submitting a matching Pool Instruct directly into RTTM, [[FICC]] will 
automatically generate a matching pool instruct on the [[Member]]’s behalf by the end of the processing day13. 
This process is referred to as “force-compare”. 
Note: 
Members will receive an MT518 “Screen Input Replay–Force Compare” message (:22F::PROC/DTCY/SITR) when a pool 
instruct is automatically generated and matched. The MT518 “Screen Input Replay” message will contain all pool details, 
along with reason code indicating this was a result of force-compare process. 
Note that this message indicates that a new message was generated and matched; a separate MT509 “Trade Matched” 
message will not be generated. 
In addition, to assist reconciliation between EPN submissions and these instructs, the “pool  reference” number specified in 
the corresponding EPN allocation, if any, will be returned as a new “pool reference” qualifier in the existing “trade 
processing narrative” field (70E::TPRO/EPNX). 
6.3 RTTM® Actions for Compared Pool Instructs 
After a Pool Instruct has been bilaterally compared, members can Cancel or Modify the Compared Pool 
Instruct. 
• Cancels: A “Cancel” may be submitted by the [[Member]] to cancel a Pool Instruct compared on the current 
business day only. The [[Member]]’s Pool Instruct will be cancelled and the corresponding advisory from 
[[FICC]] will revert to an Uncompared State, but the advisory will not be deleted from the system. If the 
[[Member]] does not resubmit a matching Pool Instruct by the end of the day, this advisory will be force-
compared at the end of the day. 
 
13 Force compare occurs at various times in the day depending on whether they are subject to further processing; e.g. prior to Pool Netting, prior to Pool 
Conversion, in real time or at End of Day. 

---

## Page 26

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 26 
Note: 
Compared Pool Instructs may only be canceled on the day comparison has occurred; attempts to cancel Pool 
Instructs compared on a prior business day will be rejected. The reject codes/reasons reported in the MT509 “Cancel 
Rejected” message (25D::CPRC//REJT) have been updated in support of these new rules. 
• Modify: Post comparison, the only data members may modify is the Pool Instruct’s XREF. The 
counterparty is not notified when a submitter modifies its XREF. 
6.4 EPN Actions on Pool Instructs 
As previously indicated, allocations versus [[FICC]] processed through the EPN system result in “advices” being 
generated in RTTM®. These advices inform the members of activities submitted against them from [[FICC]]. When 
members subsequently DK or CC previously submitted ON, corresponding changes occur in the Pool 
Comparison system. 
• DK: When a [[Buyer]] DK’s an allocation via EPN, the corresponding Pool Instruct “advices” previously 
created for both [[Buyer]] and [[Seller]] are canceled. If either Pool Instruct advisory was compared, the 
[[Member]]’s Pool Instruct will revert to the uncompared status. 
Note: 
The existing MT509 “Pool Instruct has been Unmatched” (25D::MTCH//NMAT) message will be used to inform the 
[[Member]] that their Pool Instruct is no longer compared, with reason code (NMAT//CPCA) indicating that this is due to 
counterparty ([[FICC]]) action. 
• CC: When a [[Seller]] CC’s an allocation via EPN prior to pool netting, the corresponding Pool Instruct 
“advices” previously created for both [[Buyer]] and [[Seller]] are canceled, and replacement advisories 
generated. If either original Pool Instruct advisory was compared, the [[Member]]’s Pool Instruct will revert to 
the uncompared status. 
Note: 
The existing MT509 “Pool Instruct has been Unmatched” (25D::MTCH//NMAT) message will be used to inform the 
[[Member]] that their Pool Instruct is no longer compared, with reason code (NMAT//CPCA) indicating that this is due to 
counterparty ([[FICC]]) action. 
• Delivery Date Change: RTTM® may update the delivery date on a Pool Instruct. This is typically done at 
the request of [[Member]], or due to industry-wide change of processing date. 
Note: 
To communicate to members a delivery date change, the existing MT518 “Post- Comparison Modification Advice (of 
the recipient’s trade)” will be used (22F::PROC/DTCY/MDAD). 
6.5 Customer Delivery Requests 
A Customer Delivery Request (“CDR”) may be submitted by [[Member]] to preclude selected Pool Instructs from 
being “netted away” via netting, resulting in the [[settlement]] of a pool obligation between the [[Member]] and [[FICC]]. 
The CDR feature was developed by [[FICC]] to support members’ trading and delivery strategies. Members have 

---

## Page 27

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 27 
the ability to submit CDRs globally at either the Pool Number level (to preclude all Pool Instructs in that Pool 
Number from being netted away) or at the TBA [[CUSIP]] level (to preclude Pool Instructs for all Pool Numbers 
associated with that TBA [[CUSIP]] from being netted away). 
A CDR indicator can be submitted on the Pool Instruct or it can be applied to a Pool Instruct post- submission 
at any time prior to Pool Netting. CDRs are always unilateral actions taken by the submitter. 
CDR “release” is also available to remove a previously applied CDR from a Pool Instruct at any time prior to 
Pool Netting. This action will make the targeted Pool Instruct available for netting, and may be submit at the 
individual instruct level, or globally at either the Pool Number or TBA [[CUSIP]] level. 

---

## Page 28

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 28 
7. POOL NETTING 
Pool Instructs allocated to TBA [[obligations]] stemming from TBA Netting (SBON positions) and TBA Trade- for-
Trade (TFTD14) activity are processed through MBSD’s pool netting service. This service nets instructs 
deemed netting-eligible within a particular Pool Number, and then converts them into receive and delivery pool 
[[obligations]] versus [[FICC]] at a system price15. Pool Instructs determined to be ineligible for netting are directly 
converted into receive and delivery pool [[obligations]], also versus [[FICC]] at the same system price. 
Notes: 
• All pool [[obligations]] resulting from TBA activity (TFTD/TBA and SBON) are generated v ersus [[FICC]]’s TBA 
[[settlement]] account, referred to as [[FICC]]. 
• As part of the [[Novation]] service, all Pool Instructs will result in pool [[obligations]] versus [[FICC]], regardless of whether 
netting eligible or not. Members are no longer required to settle non- netting eligible Pool Instructs outside of [[FICC]]. 
All receive and delivery pool [[obligations]] generated from the pool netting service are delivered to the Clearing 
Banks for [[settlement]] on the pool obligation delivery date. In addition, the cash difference between the system 
price and corresponding TBA Obligation (Pool Instruct) price is calculated and results in a pool “TAP” cash 
obligation, payable on the next business day. 
Although Pool Netting runs daily, the majority of pool netting activity follows the SIFMA calendar. 
Note: 
An additional pool net cycle is run on SIFMA CSD-1 in support of DNA [[settlement]] and TBA Reprice processing. This cycle 
includes all Pool Instructs with delivery date greater than the next business date. See Section 9: DNA [[settlement]]/TBA 
Reprice for details. 
In order for a Pool Instruct to be eligible for this service, the Pool Instruct must be compared and have a 
delivery date equal to the next business day
16. Pool Instructs with CSD in the current month are eligible for net 
position process; those falling outside this range or otherwise deemed ineligible17 for netting are converted 
directly. 
Note: 
All Pool Instructs included in the pool netting service receive a MT509 “Pool Bound to Net” message, followed by an “In 
Net” message (for those included in the net position process) or “Non-Net Converted” message (for those excluded from 
the net position process and directly converted). 
The “Non-Net Converted” message is new (25D::IPRC/DTCY/NECV) and replaces the now obsolete “Out of Net” message 
(25D::IPRC/DTCY/NNCT). 
 
14 SPT trades and STIP allocations are not eligible for pool netting. 
15 The system price is assigned by [[FICC]] and is the previous day’s end-of-day price of the pool at the TBA [[CUSIP]] level. 
16 In some instances, a Pool Instruct is included in the current day Pool Netting service even though it’s delivery date is > next business day (NBD). This 
occurs for late turnaround ([[Buyer]] Pool Instruct will be processed same day as [[Seller]]’s) and pools part of over-variance SIFMA exception (all Pool Instructs in 
lot are processed same day). 
17 Reasons for a pool instruct to be ineligible for netting include (but not limited to) late turnaround or pools part of a SIFMA over-variance exception. 

---

## Page 29

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 29 
8. POOL CONVERSION 
As part of the [[Novation]] service, all pool settlements, including those specified in SPT trades, allocated to STIP 
trades, or submit as cash (same-day) trades, are settled through [[FICC]]. 
Notes: 
• Previously, SPT and STIP trades were settled outside of [[FICC]] and their actual [[settlement]] communicated to [[FICC]] 
via Notifications of [[settlement]] (NOS) submitted into RTTM®. 
• The Pool Conversion process is a new service introduced in [[Novation]]. The start and end of this process is 
announced via new MT599 messages “Start of Pool Conversion, DNA [[settlement]] and TBA Reprice” 
(DTCY/SDNR) and “End of Pool Conversion, DNA [[settlement]] and TBA Reprice” (DTCY/EDNR), and is expected 
to run at 4:30pm after EPN close. 
STIP Allocations 
Pool Instructs targeting STIP trades, which are not eligible for the pool netting service, are directly converted 
into pool [[obligations]] on the day before “lot-level” delivery date18 or, in some cases, as a result of CC 
processing on bidlists19. Resulting receive and delivery [[obligations]] will be versus [[FICC]]’s STIP [[settlement]] 
account (referred to as FSTI) at trade price, and delivered to the Clearing Banks for [[settlement]] on the delivery 
day. 
Note: 
The new MT509 “STIP Pool Instruct Converted” message (25D::IPRC/DTCY/PDCV) notifies the [[Member]] that their Pool 
Instruct was converted to a corresponding pool obligation. 
SPT Trades 
Specified Pool Trades are directly converted into pool [[obligations]] on the day before contractual [[settlement]] 
date. In a similar manner to STIP allocations, resulting receive and delivery [[obligations]] will be versus [[FICC]]’s 
SPT [[settlement]] account (referred to as FSPT) at trade price, and delivered to the Clearing Banks for 
[[settlement]] on CSD. 
Cash (Same day) Trades 
Allocations submit as cash trades for same day [[settlement]], or SPT trades bilaterally matched with CSD less 
then or equal to the current business day, will be immediately converted to pool [[obligations]] and sent to the 
Clearing Banks for [[settlement]]. These [[obligations]] will at trade price versus the appropriate [[FICC]] [[settlement]] 
account ([[FICC]], FSPT or FSTI), depending on type of activity. 
 
18 STIP PIDs are converted at the “lot” level, meaning that all PIDs in a lot are converted at the same time; specifically, on the day before the minimum delivery 
date within the lot. Regardless of when a PID is converted, the resulting POID will have the delivery date as on the original PID. 
19 When a bidlist with a mix of PID and POIDs is targeted in a CC, the outstanding PIDs may first be converted to POIDs allowing the CC to operate on pools 
of the same type (all POIDs). 

---

## Page 30

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 30 
Note: 
For Pool Instructs booked for same-day [[settlement]] that target SBON or TFTD/TBA trade, a MT509 “Non-Net Converted” 
(25D::IPRC/DTCY/NECV) message will be generated; for allocations targeting STIP trades, a MT509 “STIP Pool Instruct 
Converted” (25D::IPRC/DTCY/PDCV) message will be generated. 
Conversions associated with SPT trades occur post-CSD and therefore [[DO]] not generate messaging. 

---

## Page 31

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 31 
9. DNA [[settlement]]/TBA REPRICE 
As part of the [[Novation]] service, when members have two or more offsetting SBON and/or TFTD/TBA trades 
with the same terms20 (not including price), they may “pair-off” these positions and exclude them from the 
allocation process, thereby avoiding the need to make delivery of these pools. The process of identifying 
offsetting positions to exclude from allocation is called “[[DO]] Not Allocate (DNA)” (see Section 4: [[DO]] Not Allocate 
(“DNA”) for details on DNA submissions via RTTM). 
DNA requests are “settled” on the day before SIFMA CSD, meaning that the associated TBA position is 
marked as settled and cash [[obligations]] generated that are payable on CSD. To support the cash [[settlement]] of 
DNA requests, a secondary process called “Reprice” is employed which will reprice open trades (unallocated 
and not DNAed) to the system price and generate offsetting cash [[obligations]], also payable on CSD. 
Notes: 
• Prior to repricing, an “expanded” pool net cycle (in addition to the daily cycle) will be run that will process all 
allocations regardless of delivery date, thereby resolving all Pool Instructs prior to the TBA reprice event. As part 
of these netting cycles on 24hr day, cash differences on the variance on all allocated positions is also determined 
and, combined with the reprice cash [[obligations]], will support the DNA cash [[settlement]]. 
• T he DNA [[settlement]] /TBA Reprice process is a new service introduced in [[Novation]]. The start and end of this 
process is announced via new MT599 messages “Start of Pool Conversion, DNA [[settlement]] and TBA Reprice” 
(DTCY/SDNR) and “End of Pool Conversion, DNA [[settlement]] and TBA Reprice” (DTCY/EDNR), and is expected 
to run at 4:30pm after EPN close; 
DNA [[settlement]] 
On the day before CSD, DNA requests are “settled” by drawing down targeted trades TBA position21 and 
generating a “DNA” cash differential to account for the associated price differences, payable on the next 
business date. 
Expanded Pool Net Results 
In order to prepare for the TBA Reprice process, an “expanded” Pool Net cycle is run which includes all 
compared Pool Instructs targeting SBON and TFTD/TBA trades with delivery date >= next business day and 
CSD on the next business day. 
Note: 
New Administrative MT599 “Start of Expanded Pool Net” (DTCY/SXPN) and “End of Expanded Pool Net” (DTCY/EXPN) 
messages announce the start and end of this process. 
In the same manner as daily Pool Net, compared Pool Instructs that are netting-eligible will be run through a 
netting process and result in pool [[obligations]] versus [[FICC]]’s TBA [[settlement]] account ([[FICC]]) at the system 
 
20 The “terms” are: account, buy/sell indicator, TBA [[CUSIP]] and SIFMA CSD. 
21 This is executed via generation of a new kind of system-generated NOS, referred to as “DNA NOS”. 

---

## Page 32

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 32 
price, whereas instructs not netting-eligible22 will converted directly into pool [[obligations]], also versus [[FICC]] at 
system price. These [[obligations]] will be sent to the Clearing Banks for [[settlement]] on the associated delivery 
date. An “EXP” cash differential is created to account for the associated price differences. 
Note: 
As with daily Pool Net, Pool Instructs included in the expanded pool netting service receive a MT509 “Pool Bound to Net” 
message, followed by an “In Net” message (for those included in the net position process) or “Non-Net Converted” 
message (for those excluded from the net position process and directly converted). 
Allocation Variance TAP 
The cash [[obligations]] generated from the daily Pool Net (“TAP”) and expanded Pool Net cycle (“EXP”) are 
based on the current face of the pools, which may be slightly over/under the targeted position due to variance. 
A “VAR” cash differential is created to account for the associated price differences on this variance, payable on 
the next business day. 
TBA Reprice 
Once the DNA [[settlement]] and Expanded Pool Net processes have completed, the TBA Reprice process will 
fully settle open TBA trades
23, automatically generate replacement trades at system price and create “RPC” 
cash differentials to account for the associated price differences, payable on the next business date. 
Note: 
The sum of the cash [[obligations]] generated from the daily pool net (“TAP”), expanded pool net (“EXP”), allocation variance 
(“VAR”) and reprice (“RPC”) are used to offset cash [[obligations]] generated from the DNA [[settlement]] process (“DNA”), 
thereby leaving [[FICC]] flat from as cash perspective. 
 
22 For example, PID targets trade with CSD in prior month, or late turn-around. 
23 This is executed via generation of a new kind of system-generated NOS, referred to as “RPC NOS”. 

---

## Page 33

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 33 
10. ADMINISTRATIVE MESSAGES 
RTTM® notifies [[Member]] systems regarding various system events, such as start and end-of-day processing. 
These are communicated via MT599 messages. 
RTTM® Trade Matching and Netting Service Messages 
1. RTTM® Start-of-day (/GSCC/GSOD/)–Notify members that the RTTM® system is available for submission 
of transactions to be included in that day’s matching process. 
2. AM Pass Submission Cutoff (/GSCC/APSC/)–Notify members that any transaction submitted after this 
point will not be included in the clearing system AM pass. On Netting days, submissions that were 
received by RTTM® after this point, which were due to net that day, will be rejected by RTTM®. 
3. Start of Pool Conversion, DNA [[settlement]] and TBA Reprice (/GSCC/SDNR)–Notify members that the 
daily Pool Conversion process has started and, for SIFMA 24hr day, the DNA [[settlement]] and TBA 
Reprice Process has begun. Cancel of compared SPT trades and DNA submissions with CSD of next 
business day are no longer accepted by RTTM® and will be rejected. 
4. End of Pool Conversion, DNA [[settlement]] and TBA Reprice (/GSCC/EDNR)–Notify members that Pool 
Conversion, DNA [[settlement]] and TBA Reprice Process has completed. 
5. End-of-day Matching Submission Cutoff (/GSCC/EDCS/)–Notify members that RTTM® will not accept 
any more transaction submissions for inclusion in that day’s matching process. Any transactions 
submitted after this point will be held and included in the next business day’s matching process. 
6. End-of-day Interactive Output Completed (/GSCC/EODC/)–Notify members the RTTM® system has 
completed matching processing, and that no more interactive comparison messages will be sent by the 
system for that business day. 
Pool Comparison and Netting Service Messages 
1. Pool Comparison/Netting Start-of-day (/DTCY/GSOD/)–Notify members that the pool comparison and 
netting system is available for submission of transactions to be included in that day’s comparison process. 
2. Pool Net Start (/DTCY/SOPN/)–Notify members that the daily pool net service has begun. Inputs received 
after this will still be included in the current day’s comparison process, but not eligible for the current day’s 
daily pool netting process. 
3. Pool Net End (/DTCY/EOPN/)–Notify members that the daily pool net service has completed. 
4. Expanded Pool Net Start (/DTCY/SEPN/)–Notify members that the expanded pool net service has 
begun. 
5. Expanded Pool Net End (/DTCY/EEPN/)–Notify members that the expanded pool net service has 
completed. 
6. End-of-day Pool Comparison/Netting Submission Cutoff (/DTCY/EDCS/)–Notify members that RTTM
® 
pool comparison and netting service will not accept any more transactions for inclusion in that day’s 
matching process. Any transactions submitted after this point will be held and included in the next 
business day’s matching process. 

---

## Page 34

MBSD RTTM [[Novation]]: SWIFT Interactive Messaging Changes 
Version Control Page 34 
7. End-of-day Pool Comparison/Netting Interactive Output Completed (/DTCY/EODC/)–Notify members 
the RTTM® pool comparison and netting service has completed matching processing, and that no more 
interactive comparison messages will be sent by the system for that business day. 
Note: 
The MT599 “Start of Pool Conversion, DNA [[settlement]] and TBA Reprice” (/GSCC/SDNR), “Start of Expanded Pool Net” 
(DTCY/SEPN), “End of Expanded Pool Net” (DTCY/EEPN) and “End of Pool Conversion, DNA [[settlement]] and TBA 
Reprice” (/GSCC/EDNR) are new messages introduced in [[Novation]]. 
 
 

---

## Page 35

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 