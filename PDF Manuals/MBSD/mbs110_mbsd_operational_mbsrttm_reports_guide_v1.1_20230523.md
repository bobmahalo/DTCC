---
title: "MBSD Operational MBS RTTM Reports Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs110_mbsd_operational_mbsrttm_reports_guide_v1.1_20230523.pdf"
pages: 17
size: "374.6 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD Operational MBS RTTM Reports Guide

**Original File:** [mbs110_mbsd_operational_mbsrttm_reports_guide_v1.1_20230523.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs110_mbsd_operational_mbsrttm_reports_guide_v1.1_20230523.pdf)  
**Category:** MBSD  
**Total Pages:** 17  
**File Size:** 374.6 KB  

---

## Page 1

 
MORTGAGE-BACKED [[securities]] 
(MBS)  
MBSD OPERATIONAL MBS RTTM REPORTS GUIDE 
VERSION 1.1 
NOVEMBER 1, 2018 
 


---

## Page 2

 
 
Copyright © 2018 by The Depository Trust & Clearing Corporation (“[[DTCC]]”).  
All rights reserved. This work (including, without limitation, all text, images, logos, compilation and design) is proprietar y  and  
protected by copyright, and is for the exclusive use of users authorized by [[DTCC]]. If this work is received from [[DTCC]] in any 
electronic medium, authorized users of this work are granted a limited, non- exclusive, non- transferable, non -sublicensable 
and freely revocable license to make reproductions and transmissions necessary for downloading and storage of this work 
on the users' computers and to print one or more paper copies from the electronic version for their own use. Other than to 
this limited extent, no part of this work (including any paper copies thereof or print versions thereof) may be printed, copi ed, 
altered, modified,  posted, reproduced, displayed, published, sold, licensed, used or distributed (including by transmission) 
in any form or by any means, or stored in any information stor age and retrieval system, without [[DTCC]]'s prior written 
permission.  
All product or serv ice names are the property of their respective owners.  
 
Doc Info: November 1, 2018 
Publication Code:  MBS110 
Service: [[FICC]] MBSD 
Title: MBSD Operational MBS RTTM Report s Guide 
 

---

## Page 3

MBSD Operational MBS RTTM Reports Guide 
Introduction 3 
TABLE OF CONTENTS 
Introduction..................................................................................................................................... 4 
RTTM Supplemental P&S Report....................................................................................................... 5 
About the RTTM Supplemental P&S (Purchase and Sale) Report .......................................................... 5 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n ............................................................................ 5 
Account Header Information .......................................................................................................... 5 
TBA [[CUSIP]] Header Information ..................................................................................................... 6 
Trade Details............................................................................................................................... 6 
Print Ima ge  Re port Sor t Or der .......................................................................................................... 8 
Trades Involved in Split / Splice Report ............................................................................................. 9 
About the Trades Involved in Split / Splice Report ................................................................................ 9 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n ............................................................................ 9 
Account Header Information .......................................................................................................... 9 
TBA [[CUSIP]] Header Information ................................................................................................... 10 
Trade Details............................................................................................................................. 10 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 11 
MBS TBA All Rejects Report ............................................................................................................12  
About the MBS TBA All Rejects Report ............................................................................................ 12 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 12 
Account Header Information ........................................................................................................ 12 
Trade Details............................................................................................................................. 12 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 13 
RTTM Uncompared Trade Report .....................................................................................................14  
About the RTTM Uncompared Trade Report ..................................................................................... 14 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 14 
Account Header Information ........................................................................................................ 15 
TBA [[CUSIP]] Header Information ................................................................................................... 15 
Trade Details............................................................................................................................. 15 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 16 

---

## Page 4

MBSD Operational MBS RTTM Reports Guide 
Introduction 4 
INTRODUCTION 
The purpose of this guide is to explain the reports produced by the Mortgage-Backed [[securities]] Division of the 
Fixed Income Clearing Corporation pertaining to MBS RTTM (Real Time Trade Management). This guide 
assumes that the reader has a general knowledge of mortgage-backed [[securities]] processing.  
All the reports in this guide may be downloaded and printed from MBSD RTTM Web Report Center. To access 
MBSD RTTM Web Report Center, visit: https://webficc.[[DTCC]].net/ps/ct_logon.html. These reports are available in 
print format (.pdf) only. 
The reports explained in this guide are those that can be viewed in Report Center within the MBS RTTM 
section. Which reports are viewable and the order in which they may appear is determined in part by the date 
(today’s date or a past date) and time of day at which a search is made.  
 
Figure 1: [[FICC]] Report Center (MBS RTTM [Reports] link highlighted) 
This guide provides the following information about each MBS RTTM Report: 
• Report Summary 
• Report Purpose 
• Report Format 
o Print Image 
o MRO (Machine Readable Output) 
o Tilde-Separated (including an overview of standard header row fields, if applicable) 
• Report Section/Layout (including account header, TBA [[CUSIP]] header, trade detail and sub-total/total 
information where applicable) 
• Report Sort Order. 
 


---

## Page 5

MBSD Operational MBS RTTM Reports Guide 
RTTM Supplemental P&S Report 5 
RTTM SUPPLEMENTAL P&S REPORT 
About the RTTM Supplemental P&S (Purchase and Sale) Report 
Members use the RTTM Supplemental Purchase and Sale Report to have a complete audit trail of actions 
taken on trades entered into the MBSD Clearing system. If a trade is compared but then canceled in the same 
pass, or if a compared trade is modified and canceled in the same pass, the activity is not reflected on the 
Clearing Purchase and Sale Report. This “Supplemental” version of the report is the only place where the 
[[Member]] can view this activity. 
The RTTM Supplemental Purchase and Sale (P&S) Report is produced at the end of each pass (afternoon or 
evening pass) on every business date to reflect all trades that have both been compared (also referred to as 
“matched”) and canceled within a single pass. For example, if a trade is submitted, compared and then 
canceled within the afternoon pass (after 4 p.m.), all three trade events will be reported on the PM version of 
the RTTM Supplemental P&S report: 
1. TCR (Trade Create) activity. 
2. MAT (Trade Match) activity. 
3. CAN (Trade Cancel) activity. 
 
If a matched trade is modified and canceled within a single pass, the MFY (Trade Modify) activity will also 
appear on this report. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing. Note that in general, the layout of print-image reports is subject to change. They will be produced as a 
PDF file and will have extension “.pdf”. 
Print-image reports are generated: 
• For participants that are active and not EPN-only; and 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual Trade details are listed with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]  A three -digit number is assigned to each [[Member]].  

---

## Page 6

MBSD Operational MBS RTTM Reports Guide 
RTTM Supplemental P&S Report 6 
FIELD  EXPLANATION  
AGGREGATE 
NUMBER  
A two-character alphanumeric following the [[participant]] [[ID]], which links an Account [[ID]] ([[participant]] 
Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk management 
and cash [[settlement]] reporting purposes.  
[[participant]] 
NAME  
The name of the [[Member]]. 
[[participant]] 
SYMBOL  
A 4-character identifier, the [[participant]] Symbol  represents the primary level of system 
identification. Trade submission occurs at the account level.  
DATE OF REPORT The date the report was created.  
PASS INDICATOR  AM or PM system pass. MBSD has two system passes. The AM pass is run in the afternoon, a nd 
the PM pass occurs in the evening. To learn more about the timeframes, please refer to the 
MBSD Processing Schedule & Timeframes document which may be found in the P articipant 
Reference Documentation (MBS) section on www.[[DTCC]].com . 
PRODUCT MBS Product Field: Will always be MBS  
 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information: 
FIELD  EXPLANATION  
[[CUSIP]]  The nine -character TBA [[CUSIP]]. 
DESCRIPTION  The security class code of the security reported on the trade (Agency, Product, Coupon, Maturit y) 
followed by t he Agency and Product Code description.  
 
Trade Details 
Displays information on each TBA or SPT trade. 
FIELD  EXPLANATION  
ACTIVITY  Activity Type Codes are used to identify the type of activity being reported. The RTTM 
Supplemental P&S Report can reference many events, reported as activity types, including:  
• TCR activity type is reported for the members’  compared TBA Trades and SPTs .  
• CAN activity type is reported for the members’  compared canceled TBA Trades and SPTs.  
• MOD activity type is reported for the members’ modification of their XREF for their 
compared TBA Trades and SPTs .  
• MAT activity type is reported for the members’ matched TBA Trades and SPTs. 
POOL # For Specified Pool Trades (only) , the pool number that will be settled for the trade.  
XREF  The XREF is assigned by the [[Member]] –it’s alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]]–the [[Member]] cannot have any other trades in the 
system with that same XREF.  

---

## Page 7

MBSD Operational MBS RTTM Reports Guide 
RTTM Supplemental P&S Report 7 
FIELD  EXPLANATION  
TFTD SUB TYPE The type of TFTD is provided to distinguish between TFTD TBA, SPT or STIP trades . 
TRAN [[ID]] Transaction [[ID]]: The Transaction [[ID]] is the number assigned by RTTM to  transactions prior to 
comparison. Once the trade is compared/matched, a Trade Number is assigned.  
TRD NUMBER  Trade Number: The trade number is a unique 10- digit number assigned by [[FICC]] to a compared 
trade.  
TRD ST  The RTTM Supplemental P&S Report incl udes the following trade status types:  
• FMAT trade status type is reported for trades that are Fully Matched. For a dealer -to-dealer 
trade, this means that both the buying and selling dealers have submitted trade details into 
MBSD and all mandatory matching fields submitted by both have been the same (i.e., have 
matched). For a brokered trade, this means that th e [[Broker]] has matched both the buying 
dealer and the selling dealer on the trade.  
• PMAT trade status type is reported for brokered trades that are Partially Matched . This 
means that the [[Broker]] has matched either the buying dealer’s trade submission or the s elling 
dealer’s trade submission, but not both. The trade being reported in PMAT status is the side 
that has been matched.  
• NONE: Uncompared trade.  When the trade is uncompared, the corresponding TRD 
NUMBER field will be black.   
When the trade status is reviewed in conjunction with activity type, and the trade type, the current 
disposition of the trade can be readily identified.  
Note 
Cancel Requests and Pending Cancels will not appear on the RTTM Supplemental Purchase & 
Sale report.  
TRD TYPE  The RTTM Supp lemental P&S Report  includes the following trade types:  
• TFTD trade type is reported when the TBA [[CUSIP]] is not netting eligible, one party to the trade 
is not eligible for TBA netting or netting is not desired by either side of the trade .  
• SBOD trade type is reported (pre -TBA netting) when a [[Member]]’s trade is [[settlement]] Balance 
Order Destined , which is another way of saying that the trade will be included in TBA Netting 
when the TBA netting date for its security class is reached. Status must be FMAT to be netted.  
• OPTN trade type is reported for [[Option]]  trades (PUTS/CALL). These must be canceled by 
members prior to the [[Option]]’s expiry date. Options are not eligible for TBA netting.  
The trade type basically conveys the TBA netting designation of the trade. Prior to TBA netting, 
the trade type indicates whether a trade is destined for TBA netting or not (meaning it will be 
settled without netting on a trade -for-trade basis). The trade type is also used to identify trades in 
options, which are not eligible for TBA netting.  
BUY/SELL  Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
T/D  Trade Date: The date the trade was executed between the members.  
S/D  [[settlement]] Date: The contractual [[settlement]] date of the trade.  
For SBOD and OPTN trades, the date is reflected as the month and year with  “01” for the day 
(e.g. 07/01/2018). The [[settlement]] date is based on the SIFMA Class of the trade.  
CONTRA  Contraside: This is the contraside to the trade. Once [[Novation]] occurs, the  contra on the trade will 
display the appropriate [[FICC]] [[Novation]] account  (FTBA, FSPT, or FSTI). This is applicable to 
dealers only.  

---

## Page 8

MBSD Operational MBS RTTM Reports Guide 
RTTM Supplemental P&S Report 8 
FIELD  EXPLANATION  
CMSSN  Commission: Only applies to brokered trades, and even then,  it is optional. The commission 
amount listed will be debi ted from the dealer and credited to the [[Broker]] the month following the 
CSD of a trade on Class B [[settlement]] day.  
PRICE  This is the price that the dealer submitted on the trade. For a brokered trade with commission, 
the dealer may include the price either inclusive or exclusive of commission. If the dealer 
included the price inclusive of commission, then the dealer price will be a different price than the 
[[settlement]] price.  
PAR/ORIG FACE The par value of the trade (original face) is reported in this f ield. For specified pool trades, the 
current face is displayed.  
CURRENT FACE  The current value of the pool. It is determined by multiplying the original face of the pool by the 
current factor.  
FINAL MONEY  The [[settlement]] amount of the trade. This is equal to the par multiplied by the price. For SPTs, the 
final money equals current face multiplied by price plus accrued interest.  
  
Print Image Report Sort Order 
The Purchase and Sale Report is sorted as follows: 
1. TBA [[CUSIP]]. 
2. POOL #. 
3. TRAN [[ID]]. 
4. Sequence of Events.  
5. CONTRA. 
 

---

## Page 9

MBSD Operational MBS RTTM Reports Guide 
Trades Involved in Split / Splice Report 9 
TRADES INVOLVED IN SPLIT / SPLICE REPORT 
About the Trades Involved in Split / Splice Report 
A unique business practice associated with [[Broker]] trading is “ticket splitting and splicing.” This occurs when 
trades with matching terms submitted by a [[Broker]] and Dealer [[DO]] not match on par value on a trade-by-trade 
basis, but they [[DO]] match on a net par basis (i.e., the total par of the trade(s) submitted by the Dealer matches 
the total par of the trade(s) submitted by the [[Broker]]). Although [[Broker]] trades are never subject to “split-splice 
processing,” MBSD will “split” or “splice” Dealer trades when necessary to match [[Broker]] trades. For example, if 
a Dealer has a single trade with a par value equal to the sum of the par values for three trades submitted by 
the [[Broker]] with the same trade terms, the Dealer’s single trade will “split” by canceling the Dealer’s original 
trade and establishing three new trades for the Dealer that exactly match those submitted by the [[Broker]]. 
Conversely, [[FICC]] will also combine (or “splice”) a dealer’s multiple submissions into a single trade to match a 
[[Broker]]’s submission if all trade terms match and the total par on the dealer’s submitted trade equals the total 
par on the trade submitted by the [[Broker]]. Specified Pool Trades and Stipulated Trades are excluded from 
split/splice processing.  
The Trades Involved in Split / Splice Report allows Dealers to know which trades were cancelled by RTTM due 
to split/splice processing and which trades were created by RTTM due to split/splice processing. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing. Note that in general, the layout of print-image reports is subject to change. They will be produced as a 
PDF file and will have extension “.pdf”. 
Print-image reports are generated: 
• For participants that are active and not EPN-only; and 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual trade details are listed with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]  A three -digit number is assigned to each [[Member]].  
AGGREGATE 
NUMBER  
A two-character alphanumeric following the [[participant]] [[ID]], which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk 
management and cash [[settlement]] reporting purposes.  

---

## Page 10

MBSD Operational MBS RTTM Reports Guide 
Trades Involved in Split / Splice Report 10 
FIELD  EXPLANATION  
[[participant]] NAME  The name of the [[Member]]. 
[[participant]] 
SYMBOL  
A 4-character identifier, the [[participant]] Symbol  represents the primary level of system 
identification. Trade submission o ccurs at the account level. 
DATE OF REPORT  The date the report was created.  
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD  EXPLANATION  
[[CUSIP]]  The nine -character TBA [[CUSIP]].  
SECURITY 
DESCRIPTION  
The agency type .  
ASSN [[ID]] Split/Splice Association [[ID]] that is used to tie together all trades involved in the split/splice 
matching 
Trade Details 
Displays information on each TBA trade. 
FIELD  EXPLANATION  
TRADE DATE The date the trade was executed between the members.  
[[settlement]] DATE The contractual [[settlement]] date of the trade. For SBOD trades, the date is reflected as the 
month and year with “01” for the day (e.g. 07/01/201 8). The [[settlement]] date is based on the 
SIFMA Class of the trade, which can be determined by the TBA [[CUSIP]]. For TFTD TBAs, the 
[[settlement]] date is dictated by the [[Member]].  
TXN TYPE Transaction Type: The only relevant transaction types for split/splice processing are SBOD and 
TFTD TBA trades. SPT, STIPs, and Options are not eligible for split/splice processing.  
EXTERNAL 
REFERENCE 
The External Reference (XREF) is assigned by the [[Member]] –it’s alphanumeric, extending from 
1 to 16 characters in length. It must be unique to that [[Member]] –the [[Member]] cannot have any 
other trades in the system with that same XREF.  
For trades that are spliced (two or more trades combined to form a new trade), the XREF field is 
reported as blank, since RTTM does not know which XREF to apply to the trade.  
For trades that are split (one trade divided to create two or more trades), the same XREF gets 
applied to all trades.  
TRAN/TRADE [[ID]] Transaction [[ID]]: The Transaction [[ID]] is assigned by RTTM when a transaction is submitted  to 
RTTM.  
The Trade [[ID]] is assigned by RTTM when a trade is bilaterally compared.  

---

## Page 11

MBSD Opera tional MBS RTTM Reports Guide 
Trades Involved in Split / Splice Report 11 
FIELD  EXPLANATION  
Note 
Even though the same XREF is applied to both trades when a trade is split, each individual 
trade is assigned a unique Trade [[ID]].  
PMAT PMAT: Partially Matched [[Broker]]/Dealer Trade. From a Dealer perspective, this means that it 
has matched its side of the trade with the [[Broker]], but the Dealer on the other side has not.  
FMAT FMAT: Fully Matched [[Broker]]/Dealer Trade.  
BUY/SELL Indicates if the [[Member]] was buying or s elling the MBS Security.  
CONT [[ID]] Contraside: This is the contraside to the trade.  
QUANTITY The par value of the trade.  
PRICE  This is the price that the dealer submitted on the trade.  
COMMISSION  Only applies to brokered trades, and even then , it is optional. The commission amount listed will 
be debited from the dealer and credited to the [[Broker]] the month following the CSD of trade on B 
[[settlement]] day.  
Print Image Report Sort Order 
The Trades Involved in Split / Splice Report is sorted as follows: 
1. [[settlement]] Date = earliest to latest. 
2. TBA [[CUSIP]] = ascending order. 
3. PAR. 
 

---

## Page 12

MBSD Operational MBS RTTM Reports Guide 
MBS TBA All Rejects R eport 12 
MBS TBA ALL REJECTS REPORT 
About the MBS TBA All Rejects Report 
The TBA All Reject Report is produced once daily to allow viewing of transactions that were rejected by the 
[[FICC]] Mortgage-Backed [[securities]] Division. To learn more about the timeframes of the processes relevant to 
this report, please refer to the MBSD Processing Schedule & Timeframes document which may be found in the 
[[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com. 
Print Image (pdf) Report Section/Layout Information 
This report is available in MBSD RTTM Web Report Center in a readable format. Note that in general, the 
layout of print-image reports is subject to change. They will be produced as a PDF file and will have extension 
“.pdf”.  
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART [[ID]] [[participant]] Account [[ID]]  
[[participant]] 
NAME 
MBSD [[participant]] Name.  
Trade Details 
Displays information on each TBA or SPT trade. 
FIELD  EXPLANATION  
EXTERNAL XREF The External Reference (XREF) is assigned by the [[Member]] –it’s alphanumeric, extending 
from 1 to 16 characters in length. It must be unique to that [[Member]] –the [[Member]] cannot have 
any other trades in the system with that same XREF. Under the “XREF MODIFY” sect ion of 
the report, this field is labeled as “EXPECTED XREF ,” indicating the XREF the [[Member]] was 
targeting to modify.  
REF NUMBER For CANCEL rejects only –  The Trade [[ID]] or the Transaction [[ID]] . Transaction [[ID]]: The 
Transaction [[ID]] is assigned by RTTM when a transaction is submitted to RTTM.  
The Trade [[ID]] is assigned by RTTM when a trade is bilaterally compared.   
Under the “XREF MODIFY” section of the report, this field is labeled as “EXPECTED TID,” 
indicating the targeted TID associated with the XREF the [[Member]] was trying to modify.  
SECURITY/POOL #  The TBA [[CUSIP]] and pool number of the rejected transaction 
TXN Transaction Type: The MBS TBA All Rejects Report includes the following transaction types:  

---

## Page 13

MBSD Operational MBS RTTM Reports Guide 
MBS TBA All Rejects R eport 13 
FIELD  EXPLANATION  
• SBOD (SBO Destined)  trade type is reported (pre -TBA netting) when a [[Member]]’s trade is 
[[settlement]] Balance Order Destined, which is another way of saying that the trade will be 
included in TBA Netting when the TBA netting date for its security class is reached. Status 
must be FMAT to be netted.  
• TFTD (Trade-for-Trade) trade type is reported when the TBA [[CUSIP]] is not netting 
eligible, one party to the trade is not eligib le for TBA netting or netting is not desired by 
either side of the trade 
• OPTN ([[Option]])  trade type is reported for [[Option]] trades (PUTS/CALL). These must be 
canceled by members to prior to the [[Option]]’s expiry date. Options are not eligible for TBA 
netting.  
INTENDED XREF The attempted, new XREF. The Intended XREF is  under the “XREF MODIFY” section only.  
TRADE DT The date the trade was executed between the members.  
SETTLE DT [[settlement]] Date of the TBA/SPT trade.  
[[Buyer]] The [[Buyer]]’s Account [[ID]]. 
[[Seller]] The [[Seller]]’s Account [[ID]]. 
PAR/FINAL MONEY PAR: TBA trade par value/original face value for specified pool trade.  
FINAL MONEY: Final money submitted by the [[participant]] (specified pool trades only).  
PRICE Trade Price.  
T Price Type Indicator . 
COMMISSION  Commission monies owed to the [[Broker]] . 
REJECT REASON An explanation of why the trade submission/action was rejected . 
Print Image Report Sort Order 
The MBS TBA All Rejects report is sorted as follows: 
1. Instruct. 
2. Cancel. 
3. Modify. 
4. DK. 
  
 

---

## Page 14

MBSD Operational MBS RTTM Reports Guide 
RTTM Uncompared Trade Report 14 
RTTM UNCOMPARED TRADE REPORT 
About the RTTM Uncompared Trade Report 
This report is designed to show uncompared trades and uncompared cancels of previously compared trades 
resulting from the MBSD trade matching process. 
The RTTM Uncompared Trade Report is used by members to view their submitted trades that have not been 
matched by a counterparty. Such trades appear on this report as uncompared trades. Members also use this 
report to view trades submitted by counterparties against them for which they did not submit a corresponding 
trade for matching and comparison. These requests for comparison requests/advisories also appear on this 
report. 
In addition to showing uncompared trades, this report also shows uncompared cancels of compared trades. In 
order for a compared trade to be canceled, both parties must submit Cancels with matching trade details 
targeting the matched trade to be canceled. If the [[Member]] submits a Cancel versus a compared trade, but its 
counterparty does not submit a corresponding Cancel with matching trade details, a Pending Cancel (PCN) will 
be reported to the [[Member]]. If the [[Member]]’s counterparty submits a Cancel and the [[Member]] does not submit a 
corresponding Cancel with matching trade details, a Pending Cancel Advisory (PCR) will be reported to the 
[[Member]]. 
Uncompared TFTD/SBODs and options are not deleted from RTTM, but remain until they are either canceled 
or compared. The RTTM Uncompared Trade Report will continue to show those items every day. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing. Note that in general, the layout of print-image reports is subject to change. They will be produced as a 
PDF file and will have extension “.pdf”. 
Print-image reports are generated: 
• For participants that are active and not EPN-only; and 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual Uncompared Trade details are listed with the 
following data. 
  

---

## Page 15

MBSD Operational MBS RTTM Reports Guide 
RTTM Uncompared Trade Report 15 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART [[ID]]  A 4-character identifier, the [[participant]] Symbol represents the primary level of system 
identification. Trade submission occurs at the account level.  
PART NAME  [[participant]] Name. The name of the [[Member]].  
AS OF DATE  Date of the report.  
SETTLE DATE  The contractual [[settlement]] date of the trade. For SBOD trades, the date is reflected as the 
month and year with “01” for the day (e.g. 07/01/2018 ). The [[settlement]] date is based on the 
SIFMA Class of the trade, which can be determined by the TBA [[CUSIP]]. For TFTD TBAs, the 
[[settlement]] date is dictated by the [[Member]] . 
PRODUCT  MBS Product Field: Will always be MBS.  
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD  EXPLANATION  
[[CUSIP]]  The TBA [[CUSIP]]. 
Trade Details 
Displays information on each TBA trade. 
FIELD  EXPLANATION  
UCD  Uncompared Deletes  – Deleted Uncompareds =  Y. 
POOL #  The pool number is only included for Specified Pool Trades. For SPTs, the pool number is one 
of the agreed upon trade terms. This is the only indicator  on the r eport that the trade is an SPT. 
MAT DATE  Maturity Date: For Specified Pool Trades, the Maturity Date of the underlying pool.  
TRADE DATE  The date the trade was executed between the members . 
TXN  The RTTM Uncompared Trade Report includes the following trade types:  
• SBOD ([[settlement]] Balance Order Destined)  trade type is reported (pre -TBA netting) whe n 
a [[Member]]’s trade is [[settlement]] Balance Order Destined, which is another way of saying that 
the trade will be included in TBA Netting when the TBA netting date for its security class is 
reached. Status must be FMAT to be netted.  
• TFTD (Trade-for-Trade) trade type is reported when the TBA [[CUSIP]] is not netting eligible, 
one party to the trade is not eligible for TBA netting or netting is not desired by either side of 
the trade . 

---

## Page 16

MBSD Operational MBS RTTM Reports Guide 
RTTM Uncompared Trade Report 16 
FIELD  EXPLANATION  
• OPTN ([[Option]])  trade type is reported for [[Option]] trades (PUTS/CALL). These must be 
canceled by members to prior to the [[Option]]’s expiry date. Options are not eligible for TBA 
netting.  
EXTERNAL 
REFERENCE  
The External Reference (XREF) is assigned by the [[Member]] –it’s alphanumeric, extending from 
1 to 16 characters in length. It must be unique to that [[Member]] –the [[Member]] cannot have any 
other trades in the system with that same XREF.  
BUY/SELL  Buy or Sell . 
MSG TYPE  Transaction Status:  
• UNC – Uncompared  
• REQ – Advisory  
• PCN – Pending Cancel  
• PCR – Pending Cancel Advisor y  
CONTRA/PART [[ID]]/  
EXEC  
Contraside’s [[participant]] [[ID]]: The MBSD Account Number associated with the 
contraside/counterparty.  
PAR/ORIG FACE  The par value of the trade (original f ace) is reported in this field.   
CURRENT FACE  The current value of the pool. It is determined by multiplying the original face of the pool by the 
current factor. The difference between the current face of a pool from one month to the next is 
the amount of principal that the [[investor]] (i.e . owner of the pools) has received.  
Current face as calculated by RTTM, based on current factor. 
FINAL MONEY  The [[settlement]] amount of the trade. This is equal to the par multiplied by the price. For SPTs, 
the final money equals current face multiplied by price plus accrued interest.  
TRADE/SETT’L 
PRICE  
Trade Price: This is the price that the dealer submitted on the trade). For a brokered trade with 
commission, the dealer may include the price either inclusive or exclusive of commission. If t he 
dealer included the price inclusive of commission, then the dealer price will be a different p rice 
than the [[settlement]] price.  
COMMISSION 
MONEY  
The commission monies owed to the [[Broker]] . 
Print Image Report Sort Order 
The Netting Conversion Report is sorted as follows: 
1. [[settlement]] Date = earliest to latest. 
2. TBA [[CUSIP]] = ascending order. 
3. Pool Number = ascending order. 
4. Buy/Sell. 
5. Trade Date. 
6. Par Value. 
7. Contra. 
  

---

## Page 17

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at:  
CoreLearning@[[DTCC]].com  
Or visit us on the web at:  
www.dtcclearning.com 