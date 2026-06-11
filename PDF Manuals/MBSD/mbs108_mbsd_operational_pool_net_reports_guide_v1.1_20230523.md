---
title: "MBSD Operational Pool Net Reports Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs108_mbsd_operational_pool_net_reports_guide_v1.1_20230523.pdf"
pages: 104
size: "910.4 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD Operational Pool Net Reports Guide

**Original File:** [mbs108_mbsd_operational_pool_net_reports_guide_v1.1_20230523.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs108_mbsd_operational_pool_net_reports_guide_v1.1_20230523.pdf)  
**Category:** MBSD  
**Total Pages:** 104  
**File Size:** 910.4 KB  

---

## Page 1

 
MORTGAGE-BACKED [[securities]] 
(MBS)  
MBSD OPERATIONAL POOL NET REPORTS GUIDE 
VERSION 1.1 
OCTOBER 11, 2018 
 


---

## Page 2

 
 
Copyright © 2018 by The Depository Trust & Clearing Corporation (“[[DTCC]]”).  
All rights reserved. This work (including, without limitation, all text, images, logos, compilation and design) is proprietar y  and  
protected by copyright and is for the exclusive use of users authorized by [[DTCC]]. If this work is received from [[DTCC]] in any 
electronic medium, authorized users of this work are granted a limited, non -exclusive, non- transferable, non -sublicensable 
and freely revocable license to make reproductions and transmissions necessary for downloading and stor age of this work 
on the users' computers and to print one or more paper copies from the electronic version for their own use. Other than to 
this limited extent, no part of this work (includ ing any paper copies thereof or print versions thereof) may be printed, copied, 
altered, modified, posted, reproduced, displayed, published, sold, licensed, used or distributed (including by transmission) 
in any form or by any means, or stored in any infor mation stor age and retrieval system, without [[DTCC]]'s prior written 
permission.  
All product or service names are the property of their respective owners.  
 
Doc Info: October 11, 2018 
Publication Code:  MBS108 
Service: [[FICC]] MBSD 
Title: MBSD Operational Pool Net Report s Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction....................................................................................................................................11  
Cash Trade POID Conversion Report ...............................................................................................12  
The Cash Trade POID Conversion Report Explained ......................................................................... 12 
About the Cash Trade POID Conversion Report ................................................................................ 12 
Report Format.............................................................................................................................. 12 
MRO Reports.............................................................................................................................. 12 
Print Image Report Layout ............................................................................................................. 13 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 13 
Account Header Information ........................................................................................................ 13 
TBA [[CUSIP]] Header Information ................................................................................................... 14 
Original SPT Trades / PIDs ......................................................................................................... 14 
Generated POIDs ...................................................................................................................... 15 
Sub-Totals ................................................................................................................................ 15 
Print Imag e Repo rt So rt Ord er ....................................................................................................... 16 
Expanded Pool Net Detail Report .....................................................................................................17  
The Expanded Pool Net Detail Report Explained ............................................................................... 17 
About the Expanded Pool Net Detail Report...................................................................................... 17 
Report Format.............................................................................................................................. 17 
MRO Reports.............................................................................................................................. 18 
Print Image Report Layout ............................................................................................................. 18 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 18 
Account Header Information ........................................................................................................ 18 
TBA [[CUSIP]] Header Information ................................................................................................... 19 
Pool Details .............................................................................................................................. 19 
Pool Level (PID) Sub-To t als ........................................................................................................ 20 
Pool Netting (POID) Totals .......................................................................................................... 20 
Pool Number Netted Totals ......................................................................................................... 20 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 21 

---

## Page 4

 
 
Expanded Pool Net Summary Report ...............................................................................................22  
The Expanded Pool Net Summary Report Explained.......................................................................... 22 
About the Expanded Pool Net Summary Report ................................................................................ 22 
Report Format.............................................................................................................................. 22 
MRO Reports.............................................................................................................................. 23 
Print Image Report Layout ............................................................................................................. 23 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 23 
Account Header Information ........................................................................................................ 23 
TBA [[CUSIP]] Header Information ................................................................................................... 24 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 24 
MBSD CCP Compared Pending Pool Add Report ..............................................................................25  
About the MBSD CCP Compared Pending Pool Add Report................................................................ 25 
Report Format.............................................................................................................................. 25 
Print Image Report Layout ............................................................................................................. 25 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 25 
Account Header Information ........................................................................................................ 26 
TBA [[CUSIP]] Header Information ................................................................................................... 26 
Trade Details............................................................................................................................. 26 
Report Sub-Totals ...................................................................................................................... 27 
Report Footer ............................................................................................................................ 28 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 28 
MBSD CCP Compared Pool Instruct Report ......................................................................................29  
About the MBSD CCP Compared Pool Instruct Report ....................................................................... 29 
Report Format.............................................................................................................................. 29 
MRO Reports.............................................................................................................................. 29 
Print Image Layout Information ....................................................................................................... 30 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 30 
Account Header Information ........................................................................................................ 30 
TBA [[CUSIP]] Header Information ................................................................................................... 30 
Trade Details............................................................................................................................. 31 

---

## Page 5

 
 
Report Sub-Totals ...................................................................................................................... 32 
Report Footer ............................................................................................................................ 32 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 33 
MBSD CCP Fail Report ....................................................................................................................34  
About the MBSD CCP Fail Report ................................................................................................... 34 
Report Format.............................................................................................................................. 34 
MRO Reports.............................................................................................................................. 34 
Print Image Layout Information ....................................................................................................... 34 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 35 
Account Header Information ........................................................................................................ 35 
TBA [[CUSIP]] Header Information ................................................................................................... 35 
Trade Details............................................................................................................................. 36 
Pool Level Sub-Totals................................................................................................................. 36 
Report Footer ............................................................................................................................ 37 
Print Imag e Repo rt So rt Ord er ....................................................................................................... 38 
MBSD CCP Modify Report ...............................................................................................................39  
About the MBSD CCP Modify Report ............................................................................................... 39 
Report Format.............................................................................................................................. 39 
Print Image Layout Information ....................................................................................................... 39 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 39 
Account Header Information ........................................................................................................ 40 
Trade Details............................................................................................................................. 40 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 41 
MBSD CCP P & I Report ..................................................................................................................43  
About the MBSD CCP P & I Report .................................................................................................  43 
Report Format.............................................................................................................................. 43 
MRO Reports.............................................................................................................................. 43 
Print Image Layout Information ....................................................................................................... 44 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 44 
Account Header Information ........................................................................................................ 44 

---

## Page 6

 
 
TBA [[CUSIP]] Header Information ................................................................................................... 44 
Trade Details............................................................................................................................. 45 
Pool Level Sub-Totals................................................................................................................. 45 
Report Footer ............................................................................................................................ 46 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 46 
MBSD CCP PID/NOS Assignment Report ..........................................................................................47  
About the MBSD CCP PID/NOS Assignment Report .......................................................................... 47 
Report Format.............................................................................................................................. 47 
Print Image Layout Information ....................................................................................................... 47 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 47 
Account Header Information ........................................................................................................ 48 
TBA [[CUSIP]] Header Information ................................................................................................... 48 
Trade Details............................................................................................................................. 48 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 49 
MBSD CCP Pool Instruct Activity Report ..........................................................................................50  
About the MBSD CCP Pool Instruct Activity Report ............................................................................ 50 
Report Format.............................................................................................................................. 51 
MRO Reports.............................................................................................................................. 51 
Print Image Layout Information ....................................................................................................... 51 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 52 
Account Header Information ........................................................................................................ 52 
TBA [[CUSIP]] Header Information ................................................................................................... 52 
Trade Details............................................................................................................................. 52 
Report Sub-Totals ...................................................................................................................... 55 
Report Footer ............................................................................................................................ 55 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 56 
MBSD CCP Pool Instruct Tap Detail Report.......................................................................................57  
About the MBSD CCP Pool Instruct TAP Detail Report ....................................................................... 57 
Report Format.............................................................................................................................. 57 
MRO Reports.............................................................................................................................. 57 

---

## Page 7

 
 
Print Image Layout Information ....................................................................................................... 58 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 58 
Account Header Information ........................................................................................................ 58 
TBA [[CUSIP]] Header Information ................................................................................................... 59 
Trade Details............................................................................................................................. 59 
Pool Level Sub-Totals................................................................................................................. 60 
Report Footer ............................................................................................................................ 61 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 61 
MBSD CCP Pool Netting Detail Report..............................................................................................63  
About the MBSD CCP Pool Netting D etail Repo rt .............................................................................. 63 
Report Format.............................................................................................................................. 63 
MRO Reports.............................................................................................................................. 64 
Print Image Layout Informa tion ....................................................................................................... 64 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 64 
Account Header Information ........................................................................................................ 64 
TBA [[CUSIP]] Header Information ................................................................................................... 65 
Trade Details............................................................................................................................. 65 
Pool Level Sub-Totals................................................................................................................. 66 
Report Footer ............................................................................................................................ 66 
Pool Number Netted Totals ......................................................................................................... 66 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 67 
MBSD CCP Pool Netting Summary Report ........................................................................................68  
About the MBSD CCP Pool Netting Summary Report ......................................................................... 68 
Report Format.............................................................................................................................. 68 
MRO Reports.............................................................................................................................. 68 
Print Image Report Layout ............................................................................................................. 68 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 69 
Account Header Information ........................................................................................................ 69 
TBA [[CUSIP]] Header Information ................................................................................................... 69 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 70 

---

## Page 8

 
 
MBSD CCP Pool Obligation Activity Report ......................................................................................71  
About the MBSD CCP Pool Obligation Activity Report ........................................................................ 71 
Report Format.............................................................................................................................. 71 
MRO Reports.............................................................................................................................. 71 
Print Image Layout Information ....................................................................................................... 72 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 72 
Account Header Information ........................................................................................................ 72 
TBA [[CUSIP]] Header Information ................................................................................................... 72 
Trade Details............................................................................................................................. 73 
Pool Level Sub-Totals................................................................................................................. 74 
Report Footer ............................................................................................................................ 75 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 76 
MBSD CCP Pool Obligation Pending [[settlement]] Report ....................................................................77  
About the MBSD CCP Pool Obligation Pending [[settlement]] Report....................................................... 77 
Report Format.............................................................................................................................. 77 
MRO Reports.............................................................................................................................. 77 
Print Image Layout Information ....................................................................................................... 77 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 78 
Account Header Information ........................................................................................................ 78 
TBA [[CUSIP]] Header Information ................................................................................................... 78 
Trade Details............................................................................................................................. 79 
Pool Level Sub-Totals................................................................................................................. 80 
Report Footer ............................................................................................................................ 80 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 81 
MBSD CCP Uncompared Report ......................................................................................................82  
About the MBSD CCP Compared Pool Instruct Report ....................................................................... 82 
Report Format.............................................................................................................................. 82 
MRO Reports.............................................................................................................................. 82 
Print Image Layout Information ....................................................................................................... 83 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 83 

---

## Page 9

 
 
Account Header Information ........................................................................................................ 83 
TBA [[CUSIP]] Header Information ................................................................................................... 83 
Trade Details............................................................................................................................. 84 
Report Sub-Totals ...................................................................................................................... 85 
Report Footer ............................................................................................................................ 86 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 86 
MBSD TMPG Monthly Recap Report................................................................................................. 87 
About the MBSD TMPG Monthly Recap Report................................................................................. 87 
Report Format.............................................................................................................................. 87 
MRO Reports.............................................................................................................................. 87 
Print Image Report Layout ............................................................................................................. 88 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 88 
Account Header Information ........................................................................................................ 88 
TBA [[CUSIP]] Header Information ................................................................................................... 88 
Trade Details............................................................................................................................. 89 
Pool Level Sub-Totals................................................................................................................. 89 
Report Footer ............................................................................................................................ 90 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 91 
MBSD RTTM [[participant]] Reprice Report ...........................................................................................92  
About the MBSD RTTM [[participant]] Reprice Report............................................................................ 92 
Report Format.............................................................................................................................. 92 
Print Image Report Layout ............................................................................................................. 92 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 92 
Account Header Information ........................................................................................................ 93 
TBA [[CUSIP]] Header Information ................................................................................................... 93 
Trade Details............................................................................................................................. 93 
Print Ima ge  Re port Sor t Or der ....................................................................................................... 94 
POID Conversion Report .................................................................................................................95  
The POID Conversion Report Explained .......................................................................................... 95 
About the POID Conversion Report .................................................................................................  95 

---

## Page 10

 
 
Report Format.............................................................................................................................. 95 
MRO Reports.............................................................................................................................. 96 
Print Image Report Layout ............................................................................................................. 96 
Print Imag e Repo rt Sectio n Info rmatio n........................................................................................... 96 
Account Header Information ........................................................................................................ 96 
TBA [[CUSIP]] Header Information ................................................................................................... 97 
Original SPT Trad es  /  P [[ID]] s ......................................................................................................... 97 
Generated POIDs ...................................................................................................................... 98 
Sub-Totals ................................................................................................................................ 98 
Print Re port Sor t Or der ................................................................................................................ 99 
POID Factor Update Report ........................................................................................................... 100 
The POID Factor Update Report Explained .....................................................................................100  
About the POID Factor Update Report ............................................................................................100  
Report Format.............................................................................................................................100  
MRO Reports.............................................................................................................................100  
Print Image Report Layout ............................................................................................................101  
Print Imag e Repo rt Sectio n Info rmatio n..........................................................................................101  
Account Header Information .......................................................................................................101  
Pool Header Information ............................................................................................................101  
POIDs .....................................................................................................................................102  
Sub-Totals ...............................................................................................................................102  
Print Imag e Repo rt So rt Ord er ......................................................................................................103  
 

---

## Page 11

MBSD Operational Pool Net Reports Guide 
Introduction 11 
INTRODUCTION 
The purpose of this guide is to explain the reports produced by the Mortgage-Backed [[securities]] Division of the 
Fixed Income Clearing Corporation pertaining to MBS Pool Net processing. This guide assumes that the 
reader has a general knowledge of mortgage-backed [[securities]] processing.  
All MRO Report layouts can be found in the [[FICC]] MBSD User Documentation section of the [[DTCC]] website 
(http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/[[FICC]]-mbsd-us er-documentation) (look for the Machine 
Readable Output (MRO) section.) 
To access MBSD RTTM Web Report Center, visit: https://webficc.[[DTCC]].net/ps/ct_logon.html. 
The reports explained in this guide are those that can be viewed in Report Center within the MBS PoolNet 
section. Which reports are viewable and the order in which they may appear is determined in part by the date 
(today’s date or a past date) and time of day at which a search is made.  
 
Figure 1: [[FICC]] Report Center (MBS PoolNet [Reports] link highlighted) 
This guide provides the following information about each MBS Pool Net Report: 
• Report Purpose and/or Summary 
• Report Format 
o MRO (Machine Readable Output) – if applicable 
o Print Image 
o Tilde-Separated (including an overview of standard header row fields) – if applicable 
• Report Section/Layout (including account header, TBA [[CUSIP]] header, trade detail and sub-total/total 
information where applicable) 
• Report Sort Order. 


---

## Page 12

MBSD Operational Pool Net Reports Guide 
Cash Trade POID Conv ersion R eport 12 
CASH TRADE POID CONVERSION REPORT 
The Cash Trade POID Conversion Report Explained 
To see an example of the Cash Trade POID Conversion Report while you learn about its use, available 
formats, layout, header information and sort order, please visit the MBS [[Novation]] Reports Explained page on 
the [[DTCC]] Learning Center. It may be helpful to have it open while reading this guide as it will allow you to view 
actual reports in full size and interact with them to learn more. 
About the Cash Trade POID Conversion Report 
The Cash Trade POID Conversion Report is a daily, end-of-day report and captures the following cash trades 
converted to POIDs at trade price on a real-time basis: 
• Same-Day Generic PID: PID targeting TFTD/TBA or SBON with DD = today submitted on current 
business day result in POIDs vs FTBA at trade price; 
• Same-Day STIP PID: PID targeting STIP with DD = today submitted on current business day result in 
POIDs vs FSTI at trade price; 
• “As-of” SPT: SPT trade with CSD = today submitted on current business day, as well as SPT trades with 
CSD = NBD that were submitted and matched after the trade conversion process is run. In both scenarios, 
the SPT result in POIDs vs FSPT at trade price. 
 
These cash trades will result in POID and be sent to Clearing Bank for immediate [[settlement]]. If settled, POID 
will reflect settled; else will reflect pending with DD rolled to next business day. To learn more about the 
timeframes of the processes relevant to this report, please refer to the MBSD Processing Schedule & 
Timeframes document which may be found in the [[participant]] Reference Documentation (MBS) section on 
www.[[DTCC]].com. 
Report Format  
The Cash Trade POID Conversion Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the Cash Trade POID 
Conversion Report is available in NDM only. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM Cash Trade Conversion. (All new firms must receive the NDM format.) 
 

---

## Page 13

MBSD Operational Pool Net Reports Guide 
Cash Trade POID Conv ersion R eport 13 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Print Image Report Layout 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note 
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report details the SPT trades and STIP and generic TBA allocations converted to POIDs on the current 
business day grouped by [[settlement]] month/year and TBA [[CUSIP]].  The report is divided into multiple sections, 
beginning with an Account Header and a TBA [[CUSIP]] Header. The next three sections provide information 
specific to SPT trades, STIP allocations, and generic TBA allocations. Within these sections, the original SPT 
trade/PIDs are listed, followed by resulting POIDs. Report Sub-Totals are also provided.  
Print Image Report Section Information 
Within each section, the individual Cash Trade POID Conversion details are listed, with the following data.  
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
[[participant]]/ 
AGGREGATE 
A three -digit number is assigned to each [[Member]] followed by a 2- digit number or alphanumeric 
identifier . 
ACCOUNT 
DESCRIPTION 
The account name. 
ACCOUNT [[ID]] The four -character account symbol . 
BUSINESS DATE A date field showing the current business date. 
  

---

## Page 14

MBSD Operational Pool Net Reports Guide 
Cash Trade POID Conv ersion R eport 14 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA CUSP of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD EXPLANATION 
[[settlement]] 
MONTH/YEAR 
[[settlement]] month and year . 
TBA [[CUSIP]] 9-character To Be Announced [[CUSIP]] . 
SECURITY CLASS Description of this TBA [[CUSIP]] . 
Original SPT Trades / PIDs 
Displays information on each SPT trade or allocation converted.  
FIELD EXPLANATION 
TRADE NBR Trade number on associated trade. 
TRADE XREF The XREF is assigned by the [[Member]] – it's alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]] – the [[Member]] cannot have any other trades in the 
system with that same XREF.  
PID Pool Instruct identifier (displayed for allocation conversions of STIP trades only) . 
B/S B or S (Buy or Sell) . 
T/D Trade Date (for SPT trades only) . 
D/D Delivery Date. 
S/D Contractual [[settlement]] Date. 
CONTRA Contra on the trade, equal to FSPT for SPT trades, FSTI for STIP PIDs and FTBA for generic 
TBA PIDs. 
POOL NBR Pool Number. 
POOL [[CUSIP]] Pool [[CUSIP]]. 
STTL PRICE Price, exclusive of commission . 
ORIG FACE Original face . 
CURR FACE Current face. 
NET MONEY Net money . 
CR/DR Indicator  Net money indicator, “CR” for credit, “DR” for debit . 
  

---

## Page 15

MBSD Operational Pool Net Reports Guide 
Cash Trade POID Conv ersion R eport 15 
Generated POIDs 
Displays information on each POID created.  
FIELD EXPLANATION 
POID NBR POID identifier (Pool Obligation [[ID]] Number) . 
TRADE NBR Trade number associated with this POID . 
PID Pool Instruct identifier (displayed for allocation conversions of STIP trades and Generic TBA 
TFTDs). 
B/S B or S (Buy or Sell) . 
D/D Delivery Date on POID . 
S/D Contract [[settlement]] Date . 
CONTRA Contra on the trade, equal FSPT for SPT POIDs, FSTI for STIP  POIDs and FTBA for generic 
TBA POIDs. 
POOL NBR Pool number on the POID . 
POOL [[CUSIP]] Pool [[CUSIP]] on the POID . 
STTL PRICE [[settlement]] price on the POID . 
ORIG FACE Original face on the POID . 
CURR FACE Current face on the POID . 
NET MONEY Net money on the POID . 
CR/DR Indicator  Net money indicator, “CR” for credit, “DR” for debit . 
Sub-Totals 
Sub-totals are provided for the following: 
• Sub-totals per MM/YYYY and TBA [[CUSIP]]  
• Sub-totals per Section (SPT, STIP and generic TBA)  
• Sub-totals per Report   
 
Where: 
• Orig Face = Net value of ORIG FACE of all trades, signed with “-“ if short 
• Current Face = Net value of CURR FACE of all trades, signed with “-“ if short 
• Net Money = Net value of NET MONEY of all trades, signed with “-“ if <$0. 
  

---

## Page 16

MBSD Operational Pool Net Reports Guide 
Cash Trade POID Conv ersion R eport 16 
Print Image Report Sort Order 
1. SPT section, followed by STIP section, followed by generic TBA section. 
2. SPT trades/PIDs, followed by POIDs. 
3. [[settlement]] Month/Year = earliest to latest. 
4. TBA [[CUSIP]] = ascending order. 
 
For SPT trades: 
1. [[settlement]] Date = earliest to latest. 
2. Trade Number (ascending). 
 
For PIDs: 
1. Delivery Date = earliest to latest. 
2. Trade Number (ascending). 
 
For POIDs (regardless of source): 
1. Same order as associated SPT trades/PIDs. 
Note  
The POIDs are not sorted by POID order but rather follow the same order as associated SPT trade/PID from which they 
were generated from. By doing this, cross -referencing between the 2 sections will be easier.  
 
  

---

## Page 17

MBSD Operational Pool Net Reports Guide 
Expanded Pool N et Detail Report 17 
EXPANDED POOL NET DETAIL REPORT 
The Expanded Pool Net Detail Report Explained 
To see an example of the Expanded Pool Net Detail Report while you learn about its use, available formats, 
layout, header information and sort order, please visit the MBS [[Novation]] Reports Explained page on the [[DTCC]] 
Learning Center. It may be helpful to have it open while reading this guide as it will allow you to view actual 
reports in full size and interact with them to learn more. 
About the Expanded Pool Net Detail Report 
The Expanded Pool Net Detail Report is produced on 24-hour Day as prescribed by the SIFMA Calendar and 
provides detailed results of Expanded Pool Net, which includes all allocations (PIDs) with delivery date >= next 
business day, associated cash differential and resulting POIDs versus [[FICC]] at system price. To learn more 
about the timeframes of the processes relevant to this report, please refer to the MBSD Processing Schedule & 
Timeframes document which may be found in the [[participant]] Reference Documentation (MBS) section on 
www.[[DTCC]].com. 
The Expanded Pool Net Detail Report reflects all Pool Instructs that have been included in the Expanded Pool 
Netting cycle. The report is separated into three sections: 
1. The PID section – a listing of all Pool Instructs that have gone into the Expanded Pool Net identified by the 
Pool IDs (PIDs) assigned by [[FICC]] and the XREFs assigned by the members; 
2. The POID section – a listing of the net Pool [[obligations]] stemming from the Expanded Pool Netting 
process identified by their Pool Obligation IDs (POIDs); and 
3. A Recap section – showing netting results across all pools eligible for the current netting cycle.  
 
The Expanded Pool Net Transaction Adjustment Payments (EXP TAPs) are also provided on this report. 
Report Format  
The Expanded Pool Net Detail Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
  

---

## Page 18

MBSD Operational Pool Net Reports Guide 
Expanded Pool N et Detail Report 18 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the Expanded Pool Net 
Detail Report is available in NDM only. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM CCP Exp Pool Netting Detail. (All new firms must receive the NDM format.)  
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist–there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Print Image Report Layout 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Pool 
Details, Pool Level (PID) Sub-Totals, Pool Netting (POID) Totals, and Pool Number Netted Totals. 
Print Image Report Section Information 
Within each section, the individual Expanded Pool Net details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to each 
[[Member]] (followed by) the two -character alphanumeric aggregate.  
PART [[ID]] The four -character  account symbol . 
[DATE OF REPORT] The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgage -Backed Security. 

---

## Page 19

MBSD Operational Pool Net Reports Guide 
Expanded Pool N et Detail Report 19 
TBA [[CUSIP]] Header Information 
Displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] included in this 
report. 
FIELD EXPLANATION 
TBA [[CUSIP]] The nine -character TBA [[CUSIP]]. 
POOL NUMBER The pool number allocated to the TBA trade that will be settled for the trade. 
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
STTL PRICE [[settlement]] Price: Current day Pool Net price (system price) . 
Pool Details 
Displays information most relevant to events taking place during the Pool Netting phase of the trade life cycle.  
FIELD EXPLANATION 
S/D [[settlement]] Date: The contractual [[settlement]] date of the TBA trade . 
D/D Delivery Date: The date that the pools submitted on the Pool Instructs are scheduled to be 
delivered in satisfaction of the TBA trade. 
PID Pool [[ID]]: Transaction [[ID]] assigned to each individual Pool Instruct by Pool Netting. As such, each 
PID represents a Pool Instruct.  PIDs appear in the top half, or "PID section" of the Expanded 
Pool Net Detail Report.  
POID Pool Obligation [[ID]]: Identifier assigned to pool [[obligations]] vs. [[FICC]]. Each POID therefore 
represents the [[Member]]'s obligation to received or deliver [[securities]] versus payment with 
[[FICC]]. POIDs appear in the bottom half, or "POID section" of the Expanded Pool Net Detail 
Report.  
CONTRA Contra on the trade, equal to [[FICC]]’s [[settlement]] Account ([[FICC]]) under the “POID section”.  
B/S BUY/SELL: Indicates whether the trade is a "buy" or a "sell" from the [[Member]]'s perspective.  
XREF The XREF is assigned by the [[Member]] – it's alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]] – the [[Member]] cannot have any other trades in the 
system with that same XREF.  
LONG ORIG FACE Long Original Face: Original Face of netting eligible buy pool instructs.  
LONG CURR. FACE  Long Current Face: Current Face of netting eligible buy pool instructs.  
SHORT ORIG FACE Short Original Face: Original Face of netting eligible sell pool instructs.  
SHORT CURR. FACE Short Current Face: Current Face of netting eligible sell pool instructs.  
DEBIT NET MONEY Debit [[settlement]] Proceeds. The Net Money of netting eligible buy pool instructs.  
CREDIT NET 
MONEY 
Credit [[settlement]] Proceeds. The Net Money of netting eligible sell pool instructs.  
 

---

## Page 20

MBSD Operational Pool Net Reports Guide 
Expanded Pool N et Detail Report 20 
Pool Level (PID) Sub-Totals 
Displays pool level sub-totals. 
FIELD EXPLANATION 
TOTAL [B/S] This is the sum of the Total Long & Short Positions (displayed as Original Face and Current 
Face) of all netting eligible Pool Instructs.  
NET FAIL Net Fail Position: Reserved for future use.  
NET NET Final Net Position (long or short) displayed as Original Face and Current Face of all netting 
eligible Pool Instructs. 
Pool Netting (POID) Totals 
All a [[Member]]'s receive and deliver [[obligations]] established by Pool Netting are shown totaled, including Pool 
Transaction Adjustment Payments ("Pool TAPs") that provides overall position buy and sell totals.  
FIELD EXPLANATION  
TOTAL [B/S] This is the sum of the Total Long & Short Positions (displayed as Original Face and Current 
Face) of all netting eligible Pool Instructs.  
TRADE 
ADJUSTMENT 
PAYMENT (TAP)  
[[FICC]]-generated funds adjustment ensuring [[participant]]'s original Net Money achieved.  
FAIL MARK Reserved for future use.  
NET Net of Transaction Adjustment Payment (TAP) and Fail Mark (when applicable).  
Pool Number Netted Totals 
FIELD EXPLANATION 
DELIVERY DATE Projected date of clearance. 
LONG VS [[FICC]] 
(ORIG. FACE) 
Original face of receive(s) versus [[FICC]] generated via expanded pool netting. 
LONG VS [[FICC]] 
(CURR. FACE) 
Current face of receive(s) versus [[FICC]] generated via expanded pool netting . 
[[FICC]] RVP NET 
MONEY 
Total Net Money of participants receives vs. payment (longs) against the [[FICC]] . 
SHORT VS. [[FICC]] 
(ORIG. FACE) 
Original face of deliveries versus [[FICC]] generated via expanded pool netting. 
SHORT VS. [[FICC]] 
(CURR. FACE) 
Current face of deliveries versus [[FICC]] generated via expanded pool netting . 
[[FICC]] DVP NET 
MONEY 
Total net money of [[participant]]’s  deliveries vs. payment (shorts) against the [[FICC]] . 

---

## Page 21

MBSD Operational Pool Net Reports Guide 
Expanded Pool N et Detail Report 21 
FIELD EXPLANATION 
[[FICC]] NET 
LONG/SHORT 
(ORIG. FACE) 
Total long/short original face versus [[FICC]] . 
[[FICC]] NET 
LONG/SHORT 
(CURR. FACE) 
Total long/short current face versus [[FICC]] . 
[[FICC]] NET NET 
MONEY 
Total Final Net Money (debit or credit) of all Pool [[obligations]] . 
TOTAL 
TRANSACTION 
ADJUSTMENT 
PAYMENT (“TAP”)  
[[FICC]]-generated funds adjustment (TAP) ensuring [[participant]]’s original net money achieved . 
Print Image Report Sort Order 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number = ascending order. 

---

## Page 22

MBSD Operational Pool Net Reports Guide 
Expanded Pool N et Summary Report 22 
EXPANDED POOL NET SUMMARY REPORT 
The Expanded Pool Net Summary Report Explained 
To see an example of the Expanded Pool Net Summary Report while you learn about its use, available 
formats, layout, header information and sort order, please visit the MBS [[Novation]] Reports Explained page on 
the [[DTCC]] Learning Center. It may be helpful to have it open while reading this guide as it will allow you to view 
actual reports in full size and interact with them to learn more. 
About the Expanded Pool Net Summary Report 
The Expanded Pool Net Summary Report is produced on 24-hour Day as prescribed by the SIFMA Calendar 
and provides summary results of Expanded Pool Net, which includes all allocations (PIDs) with delivery date 
>= next business day, associated cash differential and resulting POIDs versus [[FICC]] at system price. To learn 
more about the timeframes of the processes relevant to this report, please refer to the MBSD Processing 
Schedule & Timeframes document which may be found in the [[participant]] Reference Documentation (MBS) 
section on www.[[DTCC]].com. 
The Expanded Pool Net Summary Report reflects the results of the current day's Expanded Pool Netting cycle, 
summarized at the TBA [[CUSIP]] level and at the actual Pool Number level. 
Members use this report to validate and balance the results of the current day's Expanded Pool Netting cycle – 
long, short and net positions and associated Pool Transaction Adjustment Payments (EXP TAPs). Unlike the 
Expanded Pool Netting Detail Report, this report does not list individual Pool Instructions or resulting pool 
[[obligations]]. This report does not contain activity or status codes. 
Report Format  
The Expanded Pool Net Summary Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
  

---

## Page 23

MBSD Operational Pool Net Reports Guide 
Expanded Pool N et Summary Report 23 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the Expanded Pool Net 
Summary Report is available in NDM only. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM CCP Exp Pool Netting Summary. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Print Image Report Layout 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into two sections: The Account Header, and the TBA [[CUSIP]] Header. 
Print Image Report Section Information 
Within each section, the individual Expanded Pool Net Summary details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number:  The three-digit [[participant]] [[ID]] assigned to each 
[[Member]] (followed by) the two -character alphanumeric aggregate.  
ACCT NAME The name of the account . 
PART [[ID]] The four -character account symbol . 
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
 
  

---

## Page 24

MBSD Operational Pool Net Reports Guide 
Expanded Pool N et Summary Report 24 
TBA [[CUSIP]] Header Information 
Displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] included in this 
report. 
FIELD EXPLANATION 
TBA [[CUSIP]] The nine -character TBA [[CUSIP]] of reported pool . 
POOL NUMBER The pool number allocated to the TBA trade that will be settled for the trade. 
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
DELIVERY DATE The delivery date of the pool number. A pool number can have more than one delivery date.  
LONG VS. [[FICC]] 
(ORIG. FACE) 
Total long position of all netting eligible buy pool instructs repor ted as Original Face . 
LONG VS. [[FICC]] 
(CURR. FACE) 
Total long position of all netting eligible buy pool instructs repor ted as Current Face . 
[[FICC]] RVP NET 
MONEY 
Total Net Money of reported l ong position. 
SHORT VS. [[FICC]] 
(ORIG. FACE) 
Total [[short position]] of all netting eligible sell pool instructs reported as Original Face. 
SHORT VS. [[FICC]] 
(CURR. FACE) 
Total [[short position]] of all netting eligible sell pool instructs reported as Current Face. 
[[FICC]] DVP NET 
MONEY 
Total Net Money of reported [[short position]] . 
[[FICC]] NET 
LONG/SHORT 
(ORIG. FACE) 
Net of total long & short positions repor ted as Original Face . 
[[FICC]] NET 
LONG/SHORT 
(CURR. FACE) 
Net of total long & short positions repor ted as Current  Face. 
[[FICC]] NET NET 
MONEY 
Net of net monies/reported long and shor t positions . 
TOTAL TRADE 
ADJUSTMENT 
PAYMENT (TAP)  
[[FICC]]-generated funds adjustment ensuring [[participant]]’s original Net Money achieved. Will 
show as “EXP” on Cash [[settlement]] Detail Report.  
Print Image Report Sort Order 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number = ascending order. 

---

## Page 25

MBSD Operational Pool Net Reports Guide 
MBSD CCP Compared Pending Pool Add Report 25 
MBSD CCP COMPARED PENDING POOL ADD REPORT 
About the MBSD CCP Compared Pending Pool Add Report 
The MBSD CCP Compared Pending Pool Add Report is produced each day at close of business to reflect all 
Compared Pool Instructs Pending Pool Add. Pool Instructs are placed in the Pending Pool Add state when all 
required information for the pool is not on [[FICC]]’s master files, or the pool has been marked as ineligible – a 
rare condition. 
This report is cumulative. That is, the Pool Instruct will remain on the report and in a Pending Pool Add state 
until it is cancelled or until [[FICC]] Masterfile is updated with the required information. 
Members may use the MBSD CCP Compared Pending Pool Add Report to view all their Compared Pool 
Instructs that remain in a Pending Pool Add state post comparison. 
Report Format  
The MBSD CCP Compared Pending Pool Add Report is available in MBSD RTTM Web Report Center solely in 
Print Image format (a readable format suitable for printing). 
Print Image Report Layout 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Report Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section, the individual MBSD CCP Compared Pending Pool Add details are listed, with the 
following data. 
  

---

## Page 26

MBSD Operational Pool Net Reports Guide 
MBSD CCP Compared Pending Pool Add Report 26 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to each 
[[Member]] (followed by) the two -character alphanumeric aggregate which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk 
management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary level of 
system identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] 
MONTH AND YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY.  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the trade.  
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Allocation. 
FIELD  EXPLANATION  
STATUS By [[default]], the only Activity reported on the Compared Pending Pool Add report will be Pending 
Pool Add Compared (PPCP ) activity. 
CID Compared Pool [[ID]]: [[FICC]] -assigned identification assigned to a pair of compared PIDs.  
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
XREF The XREF is assigned by the [[Member]] – it’s alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]] – the [[Member]] cannot have any other trades in the 
system with that same XREF.  
PID Pool [[ID]]: Transaction [[ID]] assigned by Pool Netting.  
E/D Entry Date: Date of submission resulting in the transaction.  
C/D Comparison Date: Date that buying and selling [[participant]]’s Pool Instr ucts get compared.  

---

## Page 27

MBSD Operational Pool Net Reports Guide 
MBSD CCP Compared Pending Pool Add Report 27 
FIELD  EXPLANATION  
S/D [[settlement]] Date: The contractual [[settlement]] date of the trade.  
D/D Delivery Date: The date that the pools submitted on the Pool Instructs are scheduled to be 
delivered in satisfaction of the TBA trade.  
CONTRA AGG  Contra -side Identifier: Consists of contr a-side Clearing [[participant]] Number and Aggregate.  
CONTRA [[ID]] Contra -side’s Clearing Account Symbol.  
ORIG FACE Original Face: The par value of the trade is reported in this field.  
CURR FACE Current Face: The current value of the pool. It is determined by multiplying the original face of 
the pool by the current factor.  
PRICE Trade Price: This is the [[settlement]] price of the trade.  
NET MONEY Projected clearance funds.  
CDR Customer Delivery Request: Y -T if applied at the TBA [[CUSIP]] level, Y -P if applied at the pool 
number level, and Y -I if applied via the initial pool instruct (reflects only to submitter of the 
CDR). 
REPRICE Populated with a Yes or No. If populated as “YES,” impact of Reprice is reflected in Current 
Face and [[settlement]] Value fields.  
Report Sub-Totals 
Report Sub-Totals are reflected at the TBA [[CUSIP]] level. 
FIELD  EXPLANATION  
ORIGINAL FACE 
OPEN SELL 
This is the sum of the Original Face for all sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
OPEN SELL 
This is the sum of the Current Face for all sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN 
SELL 
This is the sum of the net money for all sell positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE 
OPEN BUY 
This is the sum of the Original Face for all buy positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
OPEN BUY 
This is the sum of the Current Face for all buy posi tions for the TBA [[CUSIP]] and S/D. 
NET MONEY OPEN 
BUY 
This is the sum of the net money for all buy positions for the TBA [[CUSIP]] and S/D . 
ORIGINAL FACE NET 
OPEN 
This is the sum of the Original Face for all buy  and sell  positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
NET OPEN 
This is the sum of the Current Face for all  buy and  sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY NET 
OPEN 
This is the sum of the net money for all buy and sell positions for the TBA [[CUSIP]]  and S/D. 

---

## Page 28

MBSD Operational Pool Net Reports Guide 
MBSD CCP Compared Pending Pool Add Report 28 
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
ORIGINAL FACE 
OPEN SELL 
This is the sum of the Original Face for all sell positions on the report.  
CURRENT FACE 
OPEN SELL 
This is the sum of the Current Face for all sell positions on the report.  
NET MONEY OPEN 
SELL 
This is the sum of the net money for all sell positions on the report . 
ORIGINAL FACE 
OPEN BUY 
This is the sum of the Original Face for all buy positions on the report.  
CURRENT FACE 
OPEN BUY 
This is the sum of the Current Face for all buy positions on the report.  
NET MONEY OPEN 
BUY 
This is the sum of the net money for all buy positions on the report . 
ORIGINAL FACE NET 
OPEN 
This is the sum of the Original Face for all buy and sell positions on the report.  
CURRENT FACE 
NET OPEN 
This is the sum of the Current Face for all buy and sell positions on the report.  
NET MONEY NET 
OPEN 
This is the sum of the net money for all  buy and  sell positions on the report . 
Print Image Report Sort Order 
The MBSD CCP Compared Pending Pool Add Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number = ascending order. 

---

## Page 29

MBSD Operational Pool Net Reports Guide 
MBSD CCP Compared Pool Instruct Report 29 
MBSD CCP COMPARED POOL INSTRUCT REPORT 
About the MBSD CCP Compared Pool Instruct Report 
The MBSD CCP Compared Pool Instruct Report is produced each day at the close of business to reflect all 
compared pool instructs that are open in the system (i.e. remain in a Pending Pool Add state post comparison). 
This report is cumulative. As such, pool instructs remain on the report until they are canceled for one of the 
following reasons: 
1. They remained in Pending Pool Add status when the cutoff for inclusion in the applicable pool netting or 
conversion cycle was reached; 
2. They were evaluated for inclusion in pool netting, but did not meet the established criteria;  or 
3. They were included in pool netting or conversion (and therefore replaced by pool [[settlement]] [[obligations]]). 
 
Members will use the MBSD CCP Compared Pool Instruct Report to view all their compared pool instructs to 
determine which are available to be included in the pool netting cycle or pool conversion.  
Note  
Compared pool instructs in Pending Pool Add status would not be included in the pool netting cycle if the pending status is 
not lifted prior to the cutoff for pool netting.  
Report Format  
The MBSD CCP Compared Pool Instruct Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP 
Compared Pool Instruct Report is available in NDM only. The MRO format can be found at 
http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM Compared Pool Instruct Status. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
  

---

## Page 30

MBSD Operational Pool Net Reports Guide 
MBSD CCP Compared Pool Instruct Report 30 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Report Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade Details are listed with the following 
data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to ea ch 
[[Member]] (followed by) the two -character alphanumeric aggregate which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk 
management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4-character identifier, the Account [[ID]] represents the primary level of 
system identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was created.  
PRODUCT Product Code Description. This is MBS for  Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] 
MONTH AND YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY. 
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  

---

## Page 31

MBSD Operational Pool Net Reports Guide 
MBSD CCP Compared Pool Instruct Report 31 
FIELD  EXPLANATION  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the trade.  
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
MARKET PRICE  Current market price as determined by MBSD which is used for determining P&L of the trade.  
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Allocation. 
FIELD  EXPLANATION  
STATUS The MBSD CCP Compared Pool Instruct Report will show either COMP or PPCP, designating 
that the Pool Instruct has been bilaterally compared or that it has been bilaterally compared and 
its pool is Pending Pool Add.  
CID Compared Pool [[ID]]: [[FICC]] -assigned identification assigned to a pair of compared PIDs.  
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
XREF The XREF is assigned by the [[Member]] – it’s alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]] – the [[Member]] cannot have any other trades in the 
system with that same XREF.  
T/D Trade Date of the trade . 
EPN XREF EPN Pool Reference Number: The EPN Pool Reference number associated with this pool 
instruct, if any, is displayed.  
PID Pool [[ID]]: Transaction [[ID]] for the Pool Instruct . 
E/D Entry Date: Date of submission resulting in the transaction.  
C/D Comparison Date: Date that buying and selling [[participant]]’s Pool Instr ucts get compared.  
S/D [[settlement]] Date: The contractual [[settlement]] date of the trade.  
D/D Delivery Date: The date that the pools submitted on the Pool Instructs are scheduled to be 
delivered in satisfaction of the TBA trade.  
CONTRA AGG  Contra -side Identifier: Consists of contr a-side Clearing [[participant]] Number and Aggregate.  
CONTRA [[ID]] Contra -side’s Clearing Account Symbol.  
ORIG FACE Original Face: The par value of the trade is reported in this field.  
CURR FACE Current Face: The current value of the pool. It is determined by multiplying the original face of 
the pool by the current factor.  
PRICE Trade Price: This is the [[settlement]] price of the trade exclusive of commission.  
NET MONEY Projected clearance funds.  
CDR Customer Delivery Request: Y -T if applied at the TBA [[CUSIP]] level, Y -P if applied at the pool 
number level, and Y -I if applied via the initial pool instruct (reflects only to submitter of the 
CDR). 

---

## Page 32

MBSD Operational Pool Net Reports Guide 
MBSD CCP Compared Pool Instruct Report 32 
FIELD  EXPLANATION  
REPRICE Populated with a Yes or No. If populated as “YES,” impact of Reprice is reflected in Current 
Face and [[settlement]] Value fields.  
Report Sub-Totals 
Report Sub-Totals are reflected at the TBA [[CUSIP]] level. 
FIELD  EXPLANATION  
ORIGINAL FACE 
OPEN SELL 
This is the sum of the Original Face for all sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
OPEN SELL 
This is the sum of the Current Face for all sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN 
SELL 
This is the sum of the net money for all sell positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE 
OPEN BUY 
This is the sum of the Original Face for all buy positions for the TBA [[CUSIP]] and S/D. 
CURRENT FACE 
OPEN BUY 
This is the sum of the Current Face for all buy positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN 
BUY 
This is the sum of the net money for all buy positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE NET 
OPEN 
This is the sum of the Original Face for all  buy and  sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
NET OPEN 
This is the sum of the Current Face for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY NET 
OPEN 
This is the sum of the net money for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
ORIGINAL FACE OPEN SELL  This is the sum of the Original Face for all sell positions on the report.  
CURRENT FACE OPEN SELL  This is the sum of the Current Face for all sell positions on the report.  
NET MONEY OPEN SELL This is the sum of the net money for all sell positions on the report . 
ORIGINAL FACE OPEN BUY This is the sum of the Original Face for all buy positions on the report.  
CURRENT FACE OPEN BUY  This is the sum of the Current Face for all buy positions on the report.  
NET MONEY OPEN BUY This is the sum of the net money for all buy positions on the report . 

---

## Page 33

MBSD Operational Pool Net Reports Guide 
MBSD CCP Compared Pool Instruct Report 33 
FIELD  EXPLANATION  
ORIGINAL FACE NET OPEN  This is the sum of the Original Face for all buy and sell positions on the report.  
CURRENT FACE NET OPEN  This is the sum of the Current Face for all  buy and  sell positions o n the report.  
NET MONEY NET OPEN  This is the sum of the net money for all buy and sell positions on the report . 
Print Image Report Sort Order 
The MBSD CCP Compared Pool Instruct Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]]/Security Class = ascending order. 
3. Pool Number = ascending order. 

---

## Page 34

MBSD Operational Pool Net Reports Guide 
MBSD CCP Fail Report 34 
MBSD CCP FAIL REPORT 
About the MBSD CCP Fail Report 
This report is produced each day at the close of business to reflect all failing pool [[obligations]] (POIDs) that are 
awaiting [[settlement]] versus [[FICC]]. That is, it contains all POIDs in which the delivery date is equal to the 
report date, but the contractual [[settlement]] date is in the past. Members will use the MBSD CCP Fail 
Report to monitor and track all settlements versus [[FICC]] in a fail state. This report is an extract of the failed 
POIDs reported on the MBSD CCP Pool Obligation Pending [[settlement]] Report. The only applicable status on 
this report is RND, which reflects that the failed POIDs are awaiting [[settlement]] versus [[FICC]] (as receive and 
deliver [[obligations]]). This report is cumulative, but the delivery date is changed to the next business day each 
night. 
Report Format  
The MBSD CCP Fail Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP Fail 
Report is available in NDM only. All MRO Report layouts can be found in the [[FICC]] MBSD User Documentation 
section of the [[DTCC]] website (http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/[[FICC]]-mbsd-user-
documentation#MachineReadableOutput) Look for: 
• NDM MBSD CCP Fail Report. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  

---

## Page 35

MBSD Operational Pool Net Reports Guide 
MBSD CCP Fail Report 35 
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Pool Level Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade Details are listed with the following 
data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to each 
[[Member]] (followed by) the two -character alphanumeric aggregate which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to  an aggregate for risk 
management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary level of 
system identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] 
MONTH AND YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY.  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the trade. 
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
 
  

---

## Page 36

MBSD Operational Pool Net Reports Guide 
MBSD CCP Fail Report 36 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Netting. 
FIELD  EXPLANATION  
STATUS The only applicable Status on this report is RND, to reflect that the failed POIDs are awaiting 
[[settlement]] versus [[FICC]] , FSPT, or FSTI  (as receive and deliver [[obligations]]).  
POID Pool Obligation  [[ID]]: Identifier assigned to pool settlements versus [[FICC]], FSPT, or FSTI . 
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
T/D Trade Date: The Trade Date field is populated based on trade type.  
• SPT trades: Trade Date will reflect the associated SPT trade date.  
• STIP allocations: Trade Date will reflect the associated STIP trade date.  
• Generic TBA trade allocations: Trade Date will be blank.  
S/D [[settlement]] Date: The contractual [[settlement]] date of the TBA trade. 
D/D Delivery Date: The date that the pools submitted on the Pool Instructs are scheduled to be 
delivered in satisfaction of the TBA trade.  
CONTRA Contra -side Identifier: Consists of contr a-side’s Clearing [[participant]] Number and Aggregate.  
[[FICC]], FSPT, or FSTI . 
ORIG FACE Original Face: The par value of the trade is reported in this field.  
CURR FACE Current Face: The current value of the pool. It is determined by multiplying the original face of 
the pool by the current factor.  
PRICE Price of the Pool Obligation . 
NET MONEY Clearance funds based on the price . 
P & I Principal and Interest: Reflects MBSD -calculated P & I impact ( CR = credit to [[Member]]; DR = 
debit to [[Member]]) of failing POID . 
TMPG CHARGE Reflects the total TMPG fail finance charge associated with the pool obligation.  
Pool Level Sub-Totals 
Pool Level Sub-Totals are reflected at the TBA [[CUSIP]] level. 
FIELD  EXPLANATION  
ORIGINAL FACE 
OPEN SELL 
This is the sum of the Original Face for all sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
OPEN SELL 
This is the sum of the Current Face for all sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN 
SELL 
This is the sum of the clearance funds based on the  trade terms (Net Money) for all sell 
positions for the TBA [[CUSIP]] and S/D.  
P & I OPEN SELL This is the sum of the calculated P & I impact (CR = cr edit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all sell positions for the TBA [[CUSIP]] and S/D.  

---

## Page 37

MBSD Operational Pool Net Reports Guide 
MBSD CCP Fail Report 37 
FIELD  EXPLANATION  
TMPG ACCRUAL 
OPEN SELL 
This is the sum of the TMPG fail finance charges associated with the settled pool obligation for 
all sell positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE 
OPEN BUY 
This is the sum of the Original Face for all buy positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
OPEN BUY 
This is the sum of the Current Face for all buy positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN 
BUY 
This is the sum of the clearance funds based on the  trade terms (Net Money) for all buy 
positions for the TBA [[CUSIP]] and S/D.  
P & I OPEN BUY This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all buy positions for the TBA [[CUSIP]] and S/D.  
TMPG ACCRUAL 
OPEN BUY 
This is the sum of the TMPG fail finance charges associated with the settled pool obligation for 
all the buy positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE 
NET OPEN 
This is the sum of the Original Face for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
NET OPEN 
This is the sum of the Current Face for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY NET 
OPEN 
This is the sum of the clearance funds based on the  trade terms (Net Money) for all buy and sell 
positions for the TBA [[CUSIP]] and S/D.  
P & I NET OPEN This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing  POIDs for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
TMPG CHARGE NET 
OPEN 
This is the sum of the TMPG fail finance charges associated with the settled pool obligation for 
all the buy and sell positions for the TBA [[CUSIP]] and S/D.  
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
ORIGINAL FACE 
OPEN SELL 
This is the sum of the Original Face for all sell positions on the report.  
CURRENT FACE 
OPEN SELL 
This is the sum of the Current Face for all sell positions on the report.  
NET MONEY OPEN 
SELL 
This is the sum of the clearance funds based on the  trade terms (Net Money) for all sell 
positions on the report.  
P & I OPEN SELL This is the sum of the ca lculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all sell positions on the report.  
TMPG CHARGE 
OPEN SELL 
This is the sum of the T MPG fail finance charges associated with the settled pool obligation for 
all the sell positions on the report.  
ORIGINAL FACE 
OPEN BUY 
This is the sum of the Original Face for all buy positions on the report.  

---

## Page 38

MBSD Operational Pool Net Reports Guide 
MBSD CCP Fail Report 38 
FIELD  EXPLANATION  
CURRENT FACE 
OPEN BUY 
This is the sum of the Current Face for all buy positions on the report.  
NET MONEY OPEN 
BUY 
This is the sum of the clearance funds based on the  trade terms (Net Money) for all buy 
positions on the report.  
P & I OPEN SELL This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all buy p ositions on the report.  
TMPG CHARGE 
OPEN BUY 
This is the sum of the T MPG fail finance charges associated with the settled pool obligation for 
all the buy positions on the report.  
ORIGINAL FACE NET 
OPEN 
This is the sum of the Original Face for all buy and sell positions on the report.  
CURRENT FACE 
NET OPEN 
This is the sum of the Current Face for all buy and sell positions on the report.  
NET MONEY NET 
OPEN 
This is the sum of the clearance funds based on the  trade terms (Net Money) for all buy and sell 
positions on the report.  
P & I NET OPEN This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
TMPG CHARGE NET 
OPEN 
This is the sum o f the TMPG fail finance charges associated with the settled pool obligation for 
all the buy and sell positions on the report.  
Print Image Report Sort Order 
The MBSD CCP Fail Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number. 
4. [[settlement]] Date. 
5. Buys (secondary D/D sort). 
6. Sells (secondary D/D sort). 
7. POID Number = ascending order. 

---

## Page 39

MBSD Operational Pool Net Reports Guide 
MBSD CCP Modify Report 39 
MBSD CCP MODIFY REPORT 
About the MBSD CCP Modify Report 
The MBSD CCP Modify Report is produced each day at the close of business to reflect all instances where one 
or more terms of an uncompared pool instruct were modified (and the pool instruct remains in an uncompared 
state). Exceptions to this feature include: 
• Modifying the target account [[ID]] will not be reported on the MBSD CCP Modify Report. (In that instance, 
the target uncompared/advisory conditions will be canceled.) 
• Modifying the X-reference of a compared pool instruct will not be displayed on this report. (Those events 
will be reported to the submitting [[Member]] via the Pool Instruct Activity Report.) 
• The CDR field cannot be modified. (CDRs can only be applied and/or released via specific CDR 
commands.) 
This report is not cumulative. That is, an Uncompared Pool Instruct which has had a term(s) modified will be 
reported only once (in its original state and final disposition), on the day the activity occurs. Members will use 
the MBSD CCP Modify Report to view, track and monitor instances where an Uncompared Pool Instruct had a 
term(s) modified. 
Report Format  
This report is available in MBSD RTTM Web Report Center solely in Print Image format (a readable format 
suitable for printing). 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, and Trade Details. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade details are listed with the following data.  

---

## Page 40

MBSD Operational Pool Net Reports Guide 
MBSD CCP Modify Report 40 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to ea ch 
[[Member]] (followed by) the two -character alphanumeric aggregate which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk 
management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary level of 
system identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Netting. 
FIELD  EXPLANATION  
XREF • The XREF is assigned by the [[Member]] – it's alphanumeric, extending from 1 to 16 
characters in length. It must be unique to that [[Member]] – the [[Member]] cannot have any other 
trades in the system with that same XREF.  
ACTIVITY STATUS (Activity Value) Status Types:  
• (UNCP) UNCP – Submitter’s pool instruct does not compare with input of target contra -side 
and results in an uncompared pool instruct condition. 
• (UNCP) PPUN – Submitter’s pool instruct does not compare with input of target contra -side 
and results in an uncompared pool instruct condition and the pool is in Pending Pool Add 
status. 
• (UNCP) ADV – An advisory conditio n is created when a contra-side’s submission of a pool 
instruct does not compare with the [[Member]]’s input.  
• (UNCP) ADVP – An advisory condition is created when a contra -side’s submission of a 
pool instruct does not compare with the [[Member]]’s input and the pool is in Pending Pool 
Add status. 
• (UCAN) ADVC – Submitter’s unilateral cancel of a compared pool instruct results in the 
cancellation of the target pool instruct and the creation of a pool instruct advisory condition 
(since the counterparty’s pool instruct is reverted to an Uncompared status).  
• (UCAN) ADCP – Submitter’s unilateral cancel of a compared pool instruct results in the 
cancellation of the targeted pool instruct and the creation of a pool instruct advisory 
condition and pool is Pending Pool Add stat us (since the counterparty’s pool instruct is 
reverted to an Uncompared Pending Pool Add state).  
• (UCAN) UNCP – An uncompared condition is created when a contra -side submits a 
unilateral cancel of a compared pool instruct.  
• (UCAN) PPUN – An uncompared condit ion is created when a contra- side submits a 
unilateral cancel of a compared pool instruct and the pool is Pending Pool Add status.  
• (REPR) PPUN – The addition of a Pending Pool Add status to an existing uncompared 
PID. 
• (REPR) UNCP – The removal of a Pending Pool Add status to an existing uncompared 
PID. 

---

## Page 41

MBSD Operational Pool Net Reports Guide 
MBSD CCP Modify Report 41 
FIELD  EXPLANATION  
• (MFY) No value – An uncompared pool instr uct advisory condition. It's applicable to the 
target contra in all instances except where the submitting members modified the target 
contra.  
PID Pool [[ID]]: Transaction [[ID]] assigned for the Pool Instruct . 
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
TBA [[CUSIP]] The nine -character TBA [[CUSIP]]. 
POOL NUMBER The pool number allocated to the TBA trade that will be settled for the trade. 
E/D Entry Date: Date of submission resulting in the transaction.  
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
S/D Contractual [[settlement]] Date. 
D/D Delivery Date: Projected date of clearance. 
CONTRA Contra -side Identifier: Consists of contra -side’s Clearing [[participant]] Number and Aggregate.   
CONTRA [[ID]] Contra -sides’  Clearing Account Symbol.  
PRICE For PIDs resulting from trades that are: 
• SBON: the [[FICC]] system price used from TBA Netting or [[FICC]] system price due to Reprice 
process. 
• TFTD/TBA: Can be either the original trade price or the [[FICC]] system price due to the 
Reprice process .  
• STIP: Original trade price.  
NET MONEY Projected clearance funds based on the price . 
CDR Y-T if applied at the TBA [[CUSIP]] level; Y- P if applied at the pool -number level, and Y-I if applied 
via the initial pool instruct (reflects only to submitter of the CDR) . 
REPRICE Reprice Indicator: Populated with a Yes or No. If populated as “YES” impact of reprice reflected 
in the Current Face and [[settlement]] Value fields . 
DK CODE Reason for DK (same DK codes currently used in EPN will be used for this process). 
Submission of a DK will not prevent subsequent matching or cancel.  
Print Image Report Sort Order 
The MBSD CCP Modify Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number. 
4. Contra-side [[participant]] Number & Aggregate. 
5. Contra-side Account [[ID]]. 
6. [[settlement]] Date. 
7. Buys (secondary D/D sort). 

---

## Page 42

MBSD Operational Pool Net Reports Guide 
MBSD CCP Modify Report 42 
8. Sells (secondary D/D sort). 
9. Activity Values (Alpha order). 
10. Status Values (Alpha order). 
11. PID number. 

---

## Page 43

MBSD Operational Pool Net Reports Guide 
MBSD CCP P & I Report 43 
MBSD CCP P & I REPORT 
About the MBSD CCP P & I Report 
The MBSD CCP P & I Report is produced each day at close of business to reflect the current day’s Principal 
and Interest amount that has been calculated for each Fail Obligation that remains outstanding in the system. 
As a Pool Obligation (POID) passes over each record date for its underlying pool, this report shows the 
calculated P & I that is accruing. Collection and disbursement of P & I by [[FICC]] will be limited to instances 
where the length of time the settled POID had been failing exceeds the Fedwire [[securities]] Service Automated 
Claims Adjustment Process (ACAP) tracking limits (currently six months). 
Report Format  
The MBSD CCP P & I Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP P & I 
Report is available in NDM only. All MRO Report layouts can be found in the [[FICC]] MBSD User Documentation 
section of the [[DTCC]] website (http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/[[FICC]]-mbsd-user-
documentation#MachineReadableOutput) Look for: 
• File Transmission Layouts for MBSD CCP P&I Report NDM Format. (All new firms must receive the NDM 
f ormat.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
  

---

## Page 44

MBSD Operational Pool Net Reports Guide 
MBSD CCP P & I Report 44 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Pool Level Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade details are listed with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to each 
[[Member]] (followed by) the two -character alphanumeric aggregate which links  an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk 
management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary level of 
system identification. Trade submission occurs at the account level.  
[DATE OF REPORT]  The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] 
MONTH AND YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY.  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  

---

## Page 45

MBSD Operational Pool Net Reports Guide 
MBSD CCP P & I Report 45 
FIELD  EXPLANATION  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the trade.  
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Netting. 
FIELD  EXPLANATION  
STATUS The MBSD CCP P & I  Report shows two statuses:  
• RND indicating a Pool Obligation (POID) has not settled versus [[FICC]], FSPT, or FSTI . 
• SETT indicating a Pool Obligation (POID) settled versus [[FICC]], FSPT, or FSTI on the report 
date (current day).  
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
POID Pool Obligation  [[ID]]: Identifier assigned to pool settlements versus [[FICC]] . 
S/D [[settlement]] Date: The contractual [[settlement]] date of the TBA trade. 
D/D Delivery Date: The date that the pools submitted on the Pool Instructs are scheduled to be 
delivered in satisfaction of the TBA trade.  
ORIG FACE Original Face: The par value of the trade is reported in this field.  
CURR FACE (AS OF 
S/D) 
Current Face As -Of-[[settlement]] Date: The current value of the pool. It is determined by 
multiplying the original face of the pool by the current factor.  
PRICE Price of the Pool Obligation.  
FACTOR DATE Date of current factor (see Factor, below).  
FACTOR Current factor applicable to pool number (during blackout period field populated with “*********”).  
REVISED CURRENT 
FACE 
Current Face based on preceding Factor.  
PRINCIPAL POID-Level Principal: MBSD calculated Principal impact (CR = credit to [[Member]] and DR = 
debit to [[Member]]) of POID.  
INTEREST POID-Level Interest: MBSD calculated Interest impact (CR = credit to [[Member]] and DR = debit 
to [[Member]]) of POID.  
TOTAL Total of POID-level Principal and Interest components.  
Pool Level Sub-Totals 
Pool Level Sub-Totals are reflected at the TBA [[CUSIP]] level. 
FIELD  EXPLANATION  
TYPE Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
POOL NUMBER The pool number allocated to the TBA trade that will be settled for the trade.  

---

## Page 46

MBSD Operational Pool Net Reports Guide 
MBSD CCP P & I Report 46 
FIELD  EXPLANATION  
UNITS Total number of outstanding POIDs on the report.  
CURRENT FACE Sub-total of the Current Face amounts for the outstanding POIDs.  
PRINCIPAL Sub-total of the MBSD calculated Principal impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of POIDs on the report.  
INTEREST Sub-total of the MBSD calculated Interest impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of POIDs on the  report.  
TOTAL P & I  This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of POIDs on the report . 
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
PRINCIPAL This is the sum of the principal for all outstanding positions on the report.  
INTEREST This is the sum of the interest for all outstanding positions on the report.  
TOTAL P & I This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) for all outstanding POIDs on the report.  
Print Image Report Sort Order 
The MBSD CCP P & I Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number. 
4. [[settlement]] Date. 
5. Sells (secondary D/D sort). 
6. Buys (secondary D/D sort). 
7. POID Number = ascending order. 

---

## Page 47

MBSD Operational Pool Net Reports Guide 
MBSD CCP PID/NOS Assignment Report 47 
MBSD CCP PID/NOS ASSIGNMENT REPORT 
About the MBSD CCP PID/NOS Assignment Report 
The MBSD CCP PID/NOS Assignment Report is produced each day at close of business to reflect all 
instances of a single Pool Instruct (PID) or [[FICC]]’s Internal Notification of [[settlement]] (NOS) being assigned to 
multiple TBA [[obligations]] (OIDs). Members use this report to balance their Pool Instructs versus their assigned 
TBA positions/trades. 
This report is not cumulative. That is, a Pool Instruct (PID) or [[FICC]]’s Internal Notification of [[settlement]] (NOS) 
assigned to multiple TBA [[obligations]] (OIDs) is reported only once on the day the activity occurs. 
There are no activity or status codes associated with this report. 
Report Format  
This report is available in MBSD RTTM Web Report Center solely in Print Image format (a readable format 
suitable for printing). 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, TBA [[CUSIP]] Header, and Trade 
Details. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade details are listed with the following data. 
  

---

## Page 48

MBSD Operational Pool Net Reports Guide 
MBSD CCP PID/NOS Assignment Report 48 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to ea ch 
[[Member]] (followed by) the two -character alphanumeric aggregate which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk 
management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary level of 
system identification. Trade submission occurs at the account level.  
[DATE OF REPORT] The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] 
MONTH AND YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY.  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the trade.  
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Netting. 
FIELD  EXPLANATION  
PID Pool [[ID]]: Transaction [[ID]] of the Pool Instruct . 
XREF The XREF is assigned by the [[Member]] – it's alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]] – the [[Member]] cannot have any other trades in the 
system with that same XREF.  
NOS CONTROL 
NUMBER 
[[FICC]]’s internal NOS Control Number . 
APPLIED OID  Target OID Number: Clearing OIDs targeted by assignment of a PID . 
CONTRA AGG  Contra -side Identifier: Consists of contr a-side’s Clearing [[participant]] Number and Aggregate.  
CONTRA [[ID]] Contra -side’s Clearing Account Symbol.  

---

## Page 49

MBSD Operational Pool Net Reports Guide 
MBSD CCP PID/NOS Assignment Report 49 
Print Image Report Sort Order 
The MBSD CCP PID/NOS Assignment Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number. 
4. PID sorted low-to-high based on PID number (secondary Contra-side [[participant]] Number/Aggregate & 
Contra-side Account [[ID]] sort). 
5. Sells (secondary D/D sort). 
6. NOS Control Number sorted low-to-high (secondary Contra-side [[participant]] Number/Aggregate & Contra-
side Account [[ID]] sort. 

---

## Page 50

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Activity Report 50 
MBSD CCP POOL INSTRUCT ACTIVITY REPORT 
About the MBSD CCP Pool Instruct Activity Report 
The MBSD CCP Pool Instruct Activity Report is produced each day at close of business to reflect all activity 
that either establishes or targets a compared Pool Instruct for the current business day. This report is not 
cumulative. That is, each activity is reported only once, on the day the activity occurs. (Note that if multiple 
actions are taken for a specific Pool Instruct, multiple activities may be reported for that Pool Instruct on a given 
day.) 
Members must allocate pools to their TBA [[obligations]] via EPN and [[FICC]] will generate a Pool Instruct based on 
the EPN submission details. Members have the [[Option]] to bilaterally submit instructions to match [[FICC]]’s Pool 
Instructs or allow [[FICC]] to force compare Pool Instructs prior to Pool Net and Pool Conversion process on 
Delivery Date. [[Member]]’s Pool Instructs must be submitted to FTBA for TBA Trades and FSTI for STIP trades.  
Members may use the MBSD CCP Pool Instruct Activity Report to validate and balance their compared Pool 
Instructs, as well as monitor subsequent updates made to those Instructs, versus the data in their internal 
applications. This report may also be useful to identify and fix breaks. 
The MBSD CCP Pool Instruct Activity Report includes the following activities: 
The [[Member]]’s compared Pool Instructs. This includes: 
• Pool Instructs compared as the result of the [[Member]] submitting a matching Pool Instruct versus [[FICC]]’s 
generated Pool Instruct;  
• Pool Instructs that have been affirmed by the [[Member]] versus [[FICC]]’s generated Pool Instruct; 
• Pool Instructs compared due to a modification made either by the [[Member]] and/or system modify (e.g., a 
date change made by the system due to a new holiday – such as the death of a president – could trigger a 
comparison event); 
• Pool Instructs compared via force comparison by [[FICC]] prior to Pool Netting and Pool Conversion. 
 
The [[Member]]’s canceled Pool Instructs. This includes: 
• Uncompared Pool Instructs that the [[Member]] has unilaterally canceled. Note: when a Cancel Correct (CC) 
message on EPN is submitted cancelling the original pools allocated, the associated [[Member]] Pool 
Instruct will go into an uncompared state. Once uncompared, the Pool Instruct can be cancelled.  
• Compared Pool Instructs that met selection criteria for Pool Netting or Pool Conversion and are therefore 
canceled (to be replaced with Pool [[obligations]]). 
 
  

---

## Page 51

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Activity Report 51 
The [[Member]]’s updated Pool Instructs. This includes: 
• Compared Pool Instructs that are updated to be in Pending Pool Add status; 
• Compared Pool Instructs in Pending Pool Add status that have the pending status lifted; 
• Compared Pool Instructs that have a CDR applied; 
• Compared Pool Instructs that have a CDR released; 
• Compared Pool Instructs for which the [[Member]] modifies its XREF (unique reference number for the 
Instruct); 
• Compared Pool Instructs that are included in a repricing (and remain eligible for Pool Netting); and 
• Compared Pool Instructs that are modified by the system (such as the date change noted above).  
Report Format  
The MBSD CCP Pool Instruct Activity Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP Pool 
Instruct Activity Report is available in NDM only. The MRO format can be found at 
http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM Pool Instruct Activity. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 

---

## Page 52

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Activity Report 52 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Report Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade details are listed with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned 
to each [[Member]] (followed by) the two -character alphanumeric aggregate which links 
an Account [[ID]] ([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked 
to an aggregate for risk management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary 
level of system identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] MONTH AND 
YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY.  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the 
trade. 
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Allocation. 
FIELD  EXPLANATION  
ACTIVITY • FCMP – Force -Compare . 
• MFYD – Modify Delivery Date. 
• PNCV – Pool Netting Converted PID to POID . 
• PDCV – STIP PID Converted to POID . 
• COMP - Pool instruct compared. 
• REPR - Pool reprice . 

---

## Page 53

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Activity Report 53 
FIELD  EXPLANATION  
• MFYX – Modify . 
• CDRA - CDR applied . 
• CDRR - CDR releas ed. 
• MFYS - [[FICC]] system modify . 
• UCAN - Unilateral PID cancel (applicable to contra- side of a unilateral cancel) . 
• REPR - Pool reprice . 
• SCAN - Targeted pool net executed . 
• NET - PID accepted via pool netting . 
STATUS (Activity Value) Status Types:  
• (FCMP) COMP – Force -Compare: Generated when a [[Member]]’s PID is “force-
compared”, e.g. system generated a matching pool instruct on [[Member]]’s behalf 
due to an uncompared [[FICC]] advisory at the end of the business  day. 
• (MFYD) COMP – Modify Delivery Date: Generated when the delivery date on a 
[[Member]]’s PID is automatically changed by the system. This delivery date change is 
initiated by [[FICC]] O perations at [[Member]]’s request, or due to industry -wide change 
of processing  date. 
• (PNCV) CANC – Pool Netting Converted PID t o POID: Generated when a 
[[Member]]’s non -netting-eligible PID is converted to a POID via pool  netting.  
• (PDCV) CANC – STIP PID Converted to POID: Generated when a [[Member]]’s STIP 
PID is converted to a POID via the conversion  process. 
• (COMP) COMP - Pool instruct bilaterally compared . 
• (REPR) COMP - Pool instruct previously Pending Pool Add placed in a compared 
state due to [[FICC]] repricing of pool resulting in the Pending Pool Add status being 
lifted (Note: if the [[FICC]] reprice event targeted a PID previously in a compared state 
and there was no negative impact to the supporting TBA position, the status of the 
PID would remain unchanged) . 
• (COMP) PPCP - Pool instruct bilaterally compared and pool is Pending Pool Add. 
• (REPR) PPCP - Pool instruct previously in a compared state is placed in Compared 
Pending Pool Add state due to [[FICC]] repricing of pool (note: if the [[FICC]] reprice 
event targeted a compared PID currently in a Pending Pool Add state, and the 
reprice had no impact to the supporting TBA position, the status of the  PID would 
remain unchanged) . 
• (MFYX) remains as COMP or PPCP - [[Member]] modification of a compared pool 
instruct’s XREF. 
• (CDRA) remains as COMP or PPCP - Customer delivery request (“CDR”) applied to 
compared pool instruct . 
• (CDRR) remains as COMP or PPCP - Release of a previously applied customer 
delivery request (“CDR”) . 
• (MFYS) remains as COMP or PPCP - [[FICC]] modification of a compared pool 
instruct  
• (UCAN) CANC - Unilateral cancel of a compared pool instruct results in the 
cancellation of the target pool instr uct reported to the submitter of the PID cancel 
and the contra -side. 
• (INSF) CANC - Compared pool instr uct is canceled due to a change in the 
supporting TBA position resulting in a TBA position being less than the value of the 
pool instruct (i.e. NOS and/or  TBA cancel processing) . 
• (REPR) CANC - Compared pool instruct is canceled due to the repricing of the pool 
resulting in the supporting TBA position being less than the value of the pool (i.e., 
adjustment to TBA record and/or increase in pool factor) . 
• (SCAN) CANC - Cancellation of a compared pool instr uct in a Pool Pending Add 
state upon the start of the target pool netting cycle . 

---

## Page 54

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Activity Report 54 
FIELD  EXPLANATION  
• (NET) CANC - Cancellation of a [[Member]]’s compared pool instruct that meets the 
selection criteria for the target pool netting cycle. 
T/D Trade Date of the trade. 
CID Compared Pool [[ID]]: [[FICC]] -assigned identification assigned to a pair of compared PIDs.  
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s 
perspective.  
XREF The XREF is assigne d by the [[Member]] – it’s alphanumeric, extending from 1 to 16 
characters in length. It must be unique to that [[Member]] – the [[Member]] cannot have any 
other trades in the system with that same XREF.  
EPN XREF [[ID]] EPN Pool Reference Number: The EPN Pool Reference n umber associated with this 
pool instruct, if any, is displayed.  
PID Pool [[ID]]: Transaction [[ID]] of the Pool Instruct . 
E/D Entry Date: Date of submission resulting in the transaction.  
C/D Comparison Date: Date that the Pool Instructs get compared.  
S/D [[settlement]] Date: The contractual [[settlement]] date of the trade.  
D/D Delivery Date: The date that the pools submitted on the Pool Instructs are scheduled to 
be delivered in satisfaction of the TBA trade.  
CONTRA AGG  Contra -side Identifier: Consists of contr a-side Clearing [[participant]] Number and 
Aggregate.  
CONTRA [[ID]] Contra -side’s Clearing Account Symbol.  
ORIG FACE Original Face: The par value of the trade is reported in this field.  
CURR FACE Current Face: The curren t value of the pool. It is determined by multiplying the original 
face of the pool by the current factor.  
PRICE For PIDs resulting from trades that are: 
• SBON: the [[FICC]] system price used from TBA Netting or [[FICC]] system price due to 
Reprice process . 
• TFTD/TBA: Can be either the original trade price or the [[FICC]] system price due to 
the Reprice process . 
• STIP: Original trade price . 
NET MONEY Projected clearance funds  based on the price . 
CDR Customer Delivery Request: Y -T if applied at the TBA [[CUSIP]] level , Y-P if applied at the 
pool number level, and Y -I if applied via the initial pool instruct (reflects only to submitter 
of the CDR). 
REPRICE Populated with a Yes or No. If populated as “YES,” impact of Reprice is reflected in 
Current Face and [[settlement]] Value fields.  
 
  

---

## Page 55

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Activity Report 55 
Report Sub-Totals 
Report Sub-Totals are reflected at the TBA [[CUSIP]] level. 
FIELD  EXPLANATION  
ORIGINAL FACE TOTAL 
SELL 
This is the sum of the Original Face for all sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE TOTAL 
SELL 
This is the sum of the Current Face for all sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY TOTAL  SELL This is the sum of the net money  for all sell positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE TOTAL  
BUY 
This is the sum of the Original Face for all buy positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE TOTAL  
BUY 
This is the sum of the Current Face for all buy positions for the TBA [[CUSIP]] and S/D.  
NET MONEY TOTAL  BUY This is the sum of the net money  for all buy positions for the TBA [[CUSIP]] and S/D.  
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
ORIGINAL FACE TOTAL  
SELL 
This is the sum of the Original Face for all sell positions on the report.  
CURRENT FACE TOTAL  
SELL 
This is the sum of the Current Face for all sell positions on the report.  
NET MONEY TOTAL  SELL This is the sum of the net money  for all sell positions on the report.  
ORIGINAL FACE TOTAL  
BUY 
This is the sum of the Original Face for all buy positions on the report.  
CURRENT FACE TOTAL  
BUY 
This is the sum of the Current Face for all buy positions on the report.  
NET MONEY TOTAL  BUY This is the sum of the net money  for all buy positions on the report.  
 
  

---

## Page 56

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Activity Report 56 
Print Image Report Sort Order 
Activity reported via this report will fall under one of the following categories and the report will be sorted 
accordingly: 
• [[FICC]] Administrative Activity 
• Pool Instruct Comparison and Update Activity 
 
Within the above categories, the MBSD CCP Pool Instruct Activity Report is sorted as follows: 
1. [[settlement]] Month/Year.  
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level). 
3. Pool Number. 
4. Contra-side [[participant]] Number & Aggregate. 
5. Contra-side Account [[ID]]. 
6. [[settlement]] Date. 
7. Buys (secondary D/D sort). 
8. Sells (secondary D/D sort).  
9. Activity Values (Alpha order). 
10. Status Values (Alpha order). 
11. PID number. 

---

## Page 57

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Tap Detail Report 57 
MBSD CCP POOL INSTRUCT TAP DETAIL REPORT 
About the MBSD CCP Pool Instruct TAP Detail Report 
The MBSD CCP Pool Instruct "TAP" Detail Report is produced each day at close of business to reflect all 
compared Pool Instructs eligible for the current business day's Pool Netting cycle and Pool Conversion and the 
associated Transaction Adjustment Payment for each individual Pool Instruct. All PIDs processed through the 
daily net, Pool Conversion, and all PIDs processed through the Expanded Pool Net (on SIFMA 24hr day only), 
whether netting-eligible or not, will be reflected in this report. This report is not cumulative. That is, each activity 
is reported only once, on the day the activity occurs. 
Members use the MBSD CCP Pool Instruct TAP Detail Report to identify, validate and balance Pool Netting 
assigned TAP calculations based on the [[settlement]] Value of the initially compared Pool Instruct and the [[FICC]] 
assigned price applied via Pool Netting (excluding Stipulated trades which use the original trade price). 
Report Format  
The MBSD CCP Pool Instruct TAP Detail Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP Pool 
Instruct TAP Detail Report is available in NDM only. The MRO format can be found at 
http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM CCP PID TAP Detail. (All new firms must receive the NDM format.)  
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
  

---

## Page 58

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Tap Detail Report 58 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Pool Level Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade details are listed with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] 
assigned to each [[Member]] (followed by) the two -character alphanumeric aggregate 
which links an Account [[ID]] ([[participant]] Symbol) to the [[participant]] [[ID]]. Every account 
must be linked to an aggregate for risk management and cash [[settlement]] reporting 
purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary 
level of system identification. Trade submission occurs at the account level.  
[DATE OF REPORT]  The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
 
  

---

## Page 59

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Tap Detail Report 59 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] MONTH AND 
YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY.  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the 
trade. 
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
D/D Delivery Date: The date that the pools underlying the TBA trade are scheduled to be 
delivered.  
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Netting. 
FIELD  EXPLANATION  
PID • Pool [[ID]]: Transaction [[ID]] assigned to the Pool Instruct . 
XREF The XREF is assigned by the [[Member]] – it’s alphanumeric, extending from 1 to 16 
characters in length. It must be unique to that [[Member]] – the [[Member]] cannot have any 
other trades in the system with that same XREF.  
Note: The (PID) XREF will be blank if the PID was created  due to system “force-
compare”. Only when a [[Member]] has explicitly submitted a PID for bilateral 
comparison will an XREF be included.  
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s 
perspective.  
CONTRA AGG  Contra -side [[ID]] entifier: Consists of contra -side Clearing [[participant]] Number and 
Aggregate.  
CONTRA [[ID]] Contra -side’s Clearing Account Symbol.  
ORIG FACE Original Face: The par value of the trade is reported in this field.  
CURR FACE Current Face: The current value of the pool. It is determined by multiplying the origina l 
face of the pool by the current factor.  
ORIGINAL TRADE PRICE Price at which the pool was allocated.  
[[settlement]] VALUE Original [[settlement]] Value: Projected [[settlement]] value based on Original Trade Price.  
[[FICC]] PRICE [[FICC]]’s system price . 
CLEAR VALUE VS. [[FICC]]  Clearance Value Versus [[FICC]]: Projected funds versus [[FICC]] upon clearance based 
on [[FICC]] applied pool price.  
TRANSACTION ADJ. 
PAYMENT 
This is the difference of the Original [[settlement]] Value and projected funds versus 
[[FICC]]. DR indicates debit and CR indicate s credit . 

---

## Page 60

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Tap Detail Report 60 
Pool Level Sub-Totals 
Pool Level Sub-Totals are reflected at the TBA [[CUSIP]] level. 
FIELD  EXPLANATION  
ORIGINAL FACE OPEN BUY This is the sum of the Original Face for all buy positions for the TBA [[CUSIP]] and 
S/D. 
CURRENT FACE OPEN BUY  This is the sum of the Current Face for all buy positions for the TBA [[CUSIP]] and 
S/D. 
[[settlement]] VALUE OPEN 
BUY 
This is the sum of the [[settlement]] Value for all buy  positions for the TBA [[CUSIP]] and 
[[[settlement]] Date]. 
CLEAR VALUE VS. [[FICC]] OPEN 
BUY 
This is the sum of the Projected Funds versus [[FICC]] upon clearance for all buy 
positions for the TBA [[CUSIP]] and [[[settlement]] Date]. 
TRANSACTION ADJ. PAYMENT 
OPEN BUY 
This is the  sum of the  differences of the Original [[settlement]] Value and projected 
funds versus [[FICC]] for all buy positions for the TBA [[CUSIP]] and [[[settlement]] Date].  
ORIGINAL FACE OPEN SELL  This is the sum of the Original Face for all sell positions for the TBA [[CUSIP]] and 
S/D. 
CURRENT FACE OPEN SELL  This is the sum of the Current Face for all sell positions for the TBA [[CUSIP]] and 
S/D. 
[[settlement]] VALUE OPEN 
SELL 
This is the sum of the [[settlement]] Value for all sell positions for the TBA [[CUSIP]] and 
[[[settlement]] Date]. 
CLEAR VALUE VS. [[FICC]] OPEN 
SELL 
This is the sum of the Projected Funds versus [[FICC]] upon clearance for all sell 
positions for the TBA [[CUSIP]] and [[[settlement]] Date]. 
TRANSACTION ADJ. PAYMENT 
OPEN SELL 
This is the sum of the  differences of the  Original [[settlement]] Value and projected 
funds versus [[FICC]] for all sell positions for the TBA [[CUSIP]] and [[[settlement]] Date].  
ORIGINAL FACE NET OPEN  This is the sum of the Original Face for all buy and sell positions for the TBA [[CUSIP]] 
and S/D. 
CURRENT FACE NET OPEN This is the sum of the Current Face for all buy and sell positions for the TBA [[CUSIP]] 
and S/D. 
[[settlement]] VALUE NET 
OPEN 
This is the sum of the [[settlement]] Value for all buy and sell positions for the TBA 
[[CUSIP]] and [[[settlement]] Da te]. 
CLEAR VALUE VS. [[FICC]] NET 
OPEN 
This is the sum of the Projected Funds versus [[FICC]] upon clearance for all buy and 
sell positions for the TBA [[CUSIP]] and [[[settlement]] Date]. 
TRANSACTION ADJ. PAYMENT 
NET OPEN 
This is the sum of the  difference of the  Origin al [[settlement]] Value and projected 
funds versus [[FICC]] for all buy and sell positions for the TBA [[CUSIP]] and [[[settlement]] 
Date]. 
 
  

---

## Page 61

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Ins truct Tap Detail Report 61 
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
ORIGINAL FACE OPEN BUY This is the sum of the Original Face for all buy positions on the report.  
CURRENT FACE OPEN BUY  This is the sum of the Current Face for all buy positions on the report.  
[[settlement]] VALUE OPEN 
BUY 
This is the sum of the [[settlement]] Value for all buy positions on the report.  
CLEAR VALUE VS. [[FICC]] OPEN 
BUY 
This is the sum of the Projected Funds versus [[FICC]] upon clearance for all buy 
positions on the report.  
TRANSACTION ADJ. PAYMENT 
OPEN BUY 
This is th e sum of the difference of the Original [[settlement]] Value and projected 
funds versus [[FICC]] for all buy positions on the report.  
ORIGINAL FACE OPEN SELL  This is the sum of the Original Face for all sell positions on the report.  
CURRENT FACE OPEN SELL  This is the sum of the Current Face for all sell positions on the report.  
[[settlement]] VALUE OPEN 
SELL 
This is the sum of the [[settlement]] Value for all sell positions on the report.  
CLEAR VALUE VS. [[FICC]] OPEN 
SELL 
This is the sum of the Projected Funds versu s [[FICC]] upon clearance for all sell 
positions on the report.  
TRANSACTION ADJ. PAYMENT 
OPEN SELL 
This is the sum of the difference of the Original [[settlement]] Value and projected 
funds versus [[FICC]] for all sell positions on the report.  
ORIGINAL FACE NET OPEN  This is the sum of the Original Face for all buy and sell positions on the report.  
CURRENT FACE NET OPEN This is the sum of the Current Face for all buy and sell positions on the report.  
[[settlement]] VALUE NET 
OPEN 
This is the sum of the [[settlement]] Value for all buy and sell positions on the report.  
CLEAR VALUE VS. [[FICC]] NET 
OPEN 
This is the sum of the Projected Funds versus [[FICC]] upon clearance for all buy and 
sell positions on the report.  
TRANSACTION ADJ. PAYMENT 
NET OPEN 
This is the sum of the difference of the  Original [[settlement]] Value and projected 
funds versus [[FICC]] for all buy and  sell positions on the report.  
Print Image Report Sort Order 
The MBSD CCP Pool Instruct TAP Detail Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number (report reflects sub-totals at the Pool Number level). 
4. Contra-side [[participant]] Number & Aggregate (low to high). 
5. Contra-side Account [[ID]] (Alpha order/low to high). 
6. Buys (secondary Original Face sort). 

---

## Page 62

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Instruct Tap Detail Report 62 
7. Sells (secondary Original Face sort). 
8. Buys (secondary D/D sort). 
9. Value of TAP (credits then debits, both low to high). 
  

---

## Page 63

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Netting Detail Report 63 
MBSD CCP POOL NETTING DETAIL REPORT 
About the MBSD CCP Pool Netting Detail Report 
The MBSD CCP Pool Netting Detail Report is produced daily after the Pool Net cycle is run to reflect all Pool 
Instructs that have been included in the current Pool Netting cycle. This report also includes non-netting-
eligible Pool Instructs that target TBA trades (TFTD/TBA and SBON) and are converted to POIDs on a 1-1 
basis as part of the daily pool net cycle. The report is separated into three sections: 
1. The PID section – a listing of all Pool Instructs that have gone into the net identified by the Pool IDs (PIDs) 
assigned by [[FICC]] and the XREFs assigned by the members; 
2. The POID section – a listing of the net Pool [[obligations]] stemming from the Pool Netting process identified 
by their Pool Obligation IDs (POIDs); and 
3. A Recap section – showing netting results across all pools eligible for the current netting cycle. 
 
The PID section of this report shows all Pool Instructs that were included in the current Pool Netting cycle. The 
PID XREF will be blank when the PID was created due to system “force-compare”. Only when a [[Member]] has 
explicitly submitted a PID for bilateral comparison will an XREF be included; 
The POID section of the report lists all the members receive and deliver [[obligations]] established by Pool 
Netting. This report provides all the information the [[Member]] needs in order to conduct [[settlement]] versus [[FICC]] 
as CCP. Pool Transaction Adjustment Payments (Pool TAPs) are also provided on this report.  
Members use the MBSD CCP Pool Netting Detail Report to validate and balance the results of the current 
day’s MBSD CCP Pool Netting cycle. This includes the individual Pool Instructions that were processed as part 
of the current day’s Pool Netting cycle as well as the resulting clearance [[obligations]] created versus [[FICC]] as 
CCP. 
Report Format  
The MBSD CCP Pool Netting Detail Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
  

---

## Page 64

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Netting Detail Report 64 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP Pool 
Netting Detail Report is available in NDM only. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM CCP Pool Netting Detail. (All new firms must receive the NDM format.)  
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Pool Level Sub-Totals, and Report Footer. Note that PIDs/POIDs with same TBA [[CUSIP]] and Pool 
Number are grouped together, separated by a TBA [[CUSIP]]/Pool Number “header” row. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade details are listed with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to 
each [[Member]] (followed by) the two -character alphanumeric aggregate which links an 
Account [[ID]] ([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an 
aggregate for risk management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary level 
of system identification. Trade submission occurs at the account level.  

---

## Page 65

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Netting Detail Report 65 
FIELD  EXPLANATION  
[DATE OF REPORT]  The date the report  was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  
POOL NUMBER Pool Number: The pool number allocated to the TBA trade that will be settled for the 
trade. 
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
STTL PRICE [[settlement]] Price: [[FICC]] system price used for Pool Netting. 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Netting. 
FIELD  EXPLANATION  
S/D [[settlement]] Date: The contractual [[settlement]] date of the trade.  
D/D Delivery Date: The date that the pools submitted on the Pool Instructs are scheduled to be 
delivered in satisfaction of the TBA trade.  Due to late- turnaround scenarios where the pool net 
cycle processes [[Buyer]] PIDs with DD > NBD, not all PIDs in this report have the same DD.  
PID Pool [[ID]]: Transaction [[ID]] assigned to each individual Pool Instruct. PIDs appear in the top half, 
or "PID section" of the Pool Netting Detail Report.  
POID Pool Obligation [[ID]]: Identifier assigned to pool [[obligations]] vs. [[FICC]]. Each POID therefore 
represents the [[Member]]'s obligation to received or deliver [[securities]] versus payment with [[FICC]]. 
POIDs appear in the bottom half, or "POID section" of the Pool Netting Detail Report.  
CONTRA  The counterparty account in which the POID is facing. All POIDs resulting from  the Pool Net 
will have [[FICC]] as the counterparty. CONTRA appears in the bottom half, or "POID section" 
of the Pool Netting Detail Report.  
B/S BUY/SELL: Indicates whether the trade is a "buy" or a "sell" from the [[Member]]'s perspective.  
XREF The XREF is assigned by the [[Member]] – it’s alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]] – the [[Member]] cannot have any other trades in the 
system with that same XREF.   
Note: The (PID) XREF will be blank if the PID was created due to system “force-
compare”. Only when a [[Member]] has explicitly submitted a PID for bilateral comparison 
will an XREF be included.  
LONG ORIG FACE Long Original Face: Total Original Face of all netting eligible buy pool instructs.  
LONG CURR. FACE  Long Current Face: Total Current Face of all netting eligible buy pool instructs.  

---

## Page 66

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Netting Detail Report 66 
FIELD  EXPLANATION  
SHORT ORIG FACE Short Original Face: Total Original Face of all netting eligible sell pool instructs.  
SHORT CURR. FACE Short Current Face: Total Current Face of all netting  eligible sell pool instructs.  
DEBIT NET MONEY Debit [[settlement]] Proceeds. The Net Money of all netting eligible buy pool instructs.  
CREDIT NET MONEY  Credit [[settlement]] Proceeds. The Net Money of all netting eligible sell pool instructs.  
Pool Level Sub-Totals 
Pool Level Sub-Totals are shown in the top half, or PID section of the report and are reflected at the TBA 
[[CUSIP]] level.  
FIELD  EXPLANATION  
TOTAL [B/S] This is the sum of the Total Long & Short Positions (displayed as Original Face and Current  
Face) of all netting eligible Pool Instructs.  
NET FAIL Net Fail Position: Reserved for future use.  
NET NET Final Net Position (long or short) displayed as Original Face and Current Face of all netting 
eligible Pool Instructs.  
Report Footer 
All a [[Member]]'s receive and deliver [[obligations]] established by Pool Netting are shown totaled, including Pool 
Transaction Adjustment Payments ("Pool TAPs") that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
TOTAL [B/S] This is the sum of the Total Long & Short Positions (displayed as Original Face and Current 
Face) of all netting eligible Pool Instructs.  
TRADE 
ADJUSTMENT 
PAYMENT (TAP)  
[[FICC]]-generated funds adjustment ensuring [[participant]]'s original Net Money is achieved.  
FAIL MARK Reserved for future use.  
NET Net of Transaction Adjustment Payment (TAP) and Fail Mark (when applicable).  
Pool Number Netted Totals 
The Pool Number Netted Totals have been expanded to provide sub-totals per delivery date. 
FIELD  EXPLANATION  
DELIVERY DATE Projected date of clearance. 
LONG VS [[FICC]] 
(ORIG. FACE) 
Original face of receive(s) versus [[FICC]] generated via pool netting. 

---

## Page 67

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Netting Detail Report 67 
FIELD  EXPLANATION  
LONG VS [[FICC]] 
(CURR. FACE) 
Current face of receive(s) versus [[FICC]] generated via pool netting. 
[[FICC]] RVP NET 
MONEY 
Total Net Money of participants receives vs. payment (longs) against the [[FICC]] . 
SHORT VS. [[FICC]] 
(ORIG. FACE) 
Original face of deliveries versus [[FICC]] generated via pool netting. 
SHORT VS. [[FICC]] 
(CURR. FACE) 
Current face of deliveries versus [[FICC]] generated via pool netting. 
[[FICC]] DVP NET 
MONEY 
Total net money of participants ’ deliveries vs. payment (shorts) against the [[FICC]] . 
[[FICC]] NET 
LONG/SHORT (ORIG. 
FACE) 
Total long/short original face versus [[FICC]] . 
[[FICC]] NET 
LONG/SHORT 
(CURR. FACE) 
Total long/short current face versus [[FICC]] . 
[[FICC]] NET NET 
MONEY 
Total Final Net Money (debit or credit) of all Pool [[obligations]].  
TOTAL 
TRANSACTION 
ADJUSTMENT 
PAYMENT (“TAP”) 
[[FICC]]-generated funds adjustment (TAP) ensuring [[participant]]’s original net money is achieved . 
Print Image Report Sort Order 
The MBSD CCP Pool Netting Detail Report has a high-level sort order as follows 
1. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
2. Pool Number (report reflects sub-totals at the Pool Number level). 
3. Pool [[CUSIP]] Number. 
 
The sort criteria for PIDs/POIDs with same TBA [[CUSIP]] and Pool Number are as follows:  
1. Netting Eligible PIDs. 
2. Non-Netting Eligible PIDs 
a. DD = NBD 
b. DD > NBD 

---

## Page 68

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Netti ng Summary Report 68 
MBSD CCP POOL NETTING SUMMARY REPORT 
About the MBSD CCP Pool Netting Summary Report 
The MBSD CCP Pool Netting Summary Report is produced each day at close of business to reflect the results 
of the current day's Pool Netting cycle, summarized at the TBA [[CUSIP]] level and at the actual Pool Number 
level. 
Members use this report to validate and balance the results of the current day's Pool Netting cycle – long, short 
and net positions and associated Pool Transaction Adjustment Payments (Pool TAPs). Unlike the Pool Netting 
Detail Report, this report does not list individual Pool Instructions or resulting pool [[obligations]]. This report does 
not contain activity or status codes. 
Report Format  
The MBSD CCP Pool Netting Summary Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP Pool Net 
Summary Report is available in NDM only. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM CCP Pool Netting Summary. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Print Image Report Layout 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  

---

## Page 69

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Netti ng Summary Report 69 
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into two sections: The Account Header, and the TBA [[CUSIP]] Header. 
Print Image Report Section Information 
Within each section, the individual MBSD CCP Pool Netting Summary details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to each 
[[Member]] (followed by) the two -character  alphanumeric aggregate which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for 
risk management and cash [[settlement]] reporting purposes.  
PART [[ID]] In this report, the Part [[ID]] refers to the Account [[ID]], which is also called the [[participant]] Symbol: 
A 4-character identifier, the Account [[ID]] represents the primary level of system identification. 
Trade submission occurs at the account level.  
PART NAME The name of the [[Member]]. 
[DATE OF REPORT] The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header. 
FIELD EXPLANATION 
TBA [[CUSIP]] The nine -character TBA [[CUSIP]] of reported pool . 
POOL NUMBER The pool number allocated to the TBA trade that will be settled for the trade. 
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
DELIVERY DATE The delivery date of the pool number. A pool number can have more than one delivery date.  
LONG VS. [[FICC]] 
(ORIG. FACE) 
Total long position of all netting eligible buy pool instructs repor ted as Original Face . 
LONG VS. [[FICC]] 
(CURR. FACE) 
Total long position of all netting eligible buy pool instructs repor ted as Current Face . 
[[FICC]] RVP NET 
MONEY 
Total Net Money of reported long position . 

---

## Page 70

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Netti ng Summary Report 70 
FIELD EXPLANATION 
SHORT VS. [[FICC]] 
(ORIG. FACE) 
Total [[short position]] of all netting eligible sell pool instructs reported as Original Face . 
SHORT VS. [[FICC]] 
(CURR. FACE) 
Total [[short position]] of all netting eligible sell pool instructs reported as Current Face. 
[[FICC]] DVP NET 
MONEY 
Total Net Money of reported [[short position]] . 
[[FICC]] NET 
LONG/SHORT (ORIG. 
FACE) 
Net of total long & s hort positions reported as Original Face. 
[[FICC]] NET 
LONG/SHORT (CURR. 
FACE) 
Net of total long & short positions repor ted as Current Face . 
[[FICC]] NET NET 
MONEY 
Net of net monies/reported long and shor t positions . 
TOTAL TRADE 
ADJUSTMENT 
PAYMENT (TAP)  
[[FICC]]-generated funds adjustment ensuring [[participant]]’s original Net Money is achieved.  
Print Image Report Sort Order 
The Pool Netting Summary Report has a high-level sort order as follows: 
1. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level).  
2. Pool Number.  
3. Pool [[CUSIP]] Number. 

---

## Page 71

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Activity Report 71 
MBSD CCP POOL OBLIGATION ACTIVITY REPORT 
About the MBSD CCP Pool Obligation Activity Report 
The MBSD CCP Pool Obligation Activity Report is produced each day at close of business to reflect all Pool 
[[obligations]] established for the current business date and any updates made to existing Pool [[obligations]] on the 
current business date. This report is not cumulative. (Note: As this report is not cumulative, fails for previous 
days are not included on this POID version of a P&S report.) 
Members use this report to further validate results of the current day’s Pool Netting cycle and Pool Conversion, 
as well as to review subsequent updates made to pool [[settlement]] [[obligations]] established for members versus 
[[FICC]] as CCP. 
Report Format  
The MBSD CCP Pool Obligation Activity Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP Pool 
Obligation Activity Report is available in NDM only. The MRO format can be found at 
http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM CCP Pool Obligation Activity. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
  

---

## Page 72

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Activity Report 72 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Pool Level Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade Details are listed with the following 
data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to 
each [[Member]] (followed by) the two -character alphanumeric aggregate which links an 
Account [[ID]] ([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an 
aggregate for risk management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary level of 
system identification. Trade submission occurs at the account level.  
[DATE OF REPORT]  The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] MONTH 
AND YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY.  

---

## Page 73

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Activity Report 73 
FIELD  EXPLANATION  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the trade.  
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Netting and 
Pool Conversion. 
FIELD  EXPLANATION  
ACTIVITY/STATUS A combination of Activity and Status codes are used to identify the type of activity being 
reported. The MBSD CCP Pool Obligation Activity Report can reference many events, 
each reported as an activity type with an associated status code.  These codes include:  
• NET/RND – Pool Obligation (POID) generated via the current  day’s Pool Netting cycle 
pending [[FICC]] [[settlement]] (receive and deliver).  
• SUBC/CANC – Pool Obligation (POID) canceled as a result of a Pool Substitution (via 
an EPN-generat ed Cancel and Correct message).  
• SUBA/RND – Pool Obligation (POID) created as a result of a Pool Substitution (via an 
EPN-generated Cancel and Correct message) which is pending [[FICC]] [[settlement]] . 
• FNEW/RND – Pool Obligation (POID) administratively creat ed by [[FICC]] and pending 
[[FICC]] [[settlement]]. 
• FCAN/CANC – Pool Obligation (POID) adm inistratively canceled by [[FICC]].  
• SETT/SETT – [[FICC]] [[settlement]] executed discharging Pool Obligation.  
• PNCV/RND – Non -netting -eligible POID generated: Generated when a [[Member]]’s 
non- netting-eligible PID is converted to a POID in the pool netting process.  
• PD CV/RND – STIP POID generated : Generated when a STIP PID is converted to a 
POID in the conversion process.  
• STCV/RND – SPT POID generated: Generated when a [[Member]]’s SPT trade is 
converted to a POID in the conversion process.  
• CXFC/CANC – POID cancel via factor update: Generated when a POID is canceled 
due to a factor correction. Always appears in correlation with REFC  below. 
• REFC/RND – POID created via factor update: Generated when a replacement POID 
is created due to a factor correction. Always appears in correlation with CXFC above.  
• CXDK/CANC – POID cancel due to DK of CC : Generated when a CC is DK ’d, 
causing the replacement POID to be canceled. Always appears in correlation with 
REDK below . 
• REDK/RND – POID reestablished due to DK of CC : Generated when a CC is DK ’d, 
causing the original POID canceled due to CC to be restored.  
POID Pool Obligation  [[ID]]: Identifier assigned to pool settlements versus [[FICC]] . 
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s 
perspective.  
T/D Trade Date: The Trade Date field is populated based on trade type.  
• SPT trades: Trade Date will reflect the associated SPT trade date.  
• STIP allocations: Trade Date will reflect the associated STIP trade date.  
• Generic TBA trade allocations: Trade Date will be blank.  

---

## Page 74

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Activity R eport 74 
FIELD  EXPLANATION  
S/D [[settlement]] Date: The contractual [[settlement]] date of the TBA trade. 
D/D Delivery Date: The date that the pools submitted are scheduled to be delivered in 
satisfaction of the TBA trade. 
CONTRA Contra -side Identifier: Consists of contr a-side’s Clearing [[participant]] Number and 
Aggregate.  
• [[FICC]]: Generic TBA Account .  
• FSTI: [[FICC]]’s Stipulated Account.  
• FSPT: [[FICC]]’s Specified Pool Trade Account . 
ORIG FACE Original Face: The par value of the trade is reported in this field.  
CURR FACE Current Face: The current value of the pool. It is determined by multiplying the original 
face of the pool by the current factor.  
PRICE For SPT, STIP, and Generic TBA Pool Conversions: Trade Pric e.  
[[obligations]] vs [[FICC]] via Pool Netting: [[FICC]] System price used for Pool Netting. 
EXPECTED NET MONEY Projected clearance funds based on the price . 
ACTUAL CLEARANCE 
MONEY 
Funds amount processed at settling bank.  
TMPG CHARGE Reflects the total TMPG fail finance charge associated with the settled pool obligation.  
Pool Level Sub-Totals 
Pool Level Sub-Totals are reflected at the TBA [[CUSIP]] level. 
FIELD  EXPLANATION  
ORIGINAL FACE 
OPEN SELL 
This is the sum of the Original Face for all sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
OPEN SELL 
This is the sum of the Current Face for all sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN 
SELL 
This is the sum of the projected clearance funds based on the price  (Net Money) for all sell 
positions for the TBA [[CUSIP]] and S/D.  
CLEARANCE MONEY 
OPEN SELL 
This is the sum of the funds amount processed at settling bank for all sell positions for the TBA 
[[CUSIP]] and S/D.  
TMPG CHARGE 
OPEN SELL 
This is the sum of the TMPG fail finance charges associated with the settled pool obligation for 
all sell positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE 
OPEN BUY 
This is the sum of the Original Face for all buy positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
OPEN BUY 
This is the sum of the Current Face for all buy positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN 
BUY 
This is the sum of the projected clearance funds based on the price  (Net Money) for all buy 
positions for the TBA [[CUSIP]] and S/D.  

---

## Page 75

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Activity Report 75 
FIELD  EXPLANATION  
CLEARANCE MONEY 
OPEN BUY 
This is the sum of the funds amount processed at settling bank for all buy positions for the TBA 
[[CUSIP]] and S/D.  
TMPG CHARGE 
OPEN BUY 
This is the sum of the TMPG fail finance charges associated with the settled pool obligation for 
all the buy positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE 
NET OPEN 
This is the sum of the Original Face for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE 
NET OPEN 
This is the sum of the Current Face for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY NET 
OPEN 
This is the sum of the projected clearance funds based on the price  (Net Money) for all buy and 
sell positions for the TBA [[CUSIP]] and S/D.  
CLEARANCE MONEY 
NET OPEN 
This is the sum of the funds amount processed at settling bank for all buy and sell positions for 
the TBA [[CUSIP]] and S/D.  
TMPG CHARGE NET 
OPEN 
This is the sum of the TMPG fail finance charges associated with the settled pool obligation for 
all the buy and sell positions for the TBA [[CUSIP]] and S/D.  
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
ORIGINAL FACE 
OPEN SELL 
This is the sum of the Original Face for all sell positions on the report.  
CURRENT FACE 
OPEN SELL 
This is the sum of the Current Face for all sell positions on the report.  
NET MONEY OPEN 
SELL 
This is the sum of the projected clearance funds based on the price  (Net Money) for all sell 
positions on the report.  
CLEARANCE MONEY 
OPEN SELL 
This is the sum of the funds amount processed at settling bank for all sell positions on the 
report.  
TMPG CHARGE 
OPEN SELL 
This is the sum of the T MPG fail finance charges associated with the settled pool obligation for 
all the sell positions on the report.  
ORIGINAL FACE 
OPEN BUY 
This is the sum of the Original Face for all buy positions on the report.  
CURRENT FACE 
OPEN BUY 
This is the sum of the Current Face for all buy positions on the report.  
NET MONEY OPEN 
BUY 
This is the sum of the projected clearance funds based on the price  (Net Money) for all buy 
positions on the report.  
CLEARANCE MONEY 
OPEN BUY 
This is the sum of the funds amount processed at settling bank for all buy positions on the 
report.  
TMPG CHARGE 
OPEN BUY 
This is the sum of the T MPG fail finance charges associated with the settled pool obligation for 
all the buy positions on the report . 

---

## Page 76

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Activity Report 76 
FIELD  EXPLANATION  
ORIGINAL FACE NET 
OPEN 
This is the sum of the Original Face for all buy and sell positions on the report.  
CURRENT FACE 
NET OPEN 
This is the sum of the Current Face for all buy and sell positions on the report.  
NET MONEY NET 
OPEN 
This is the sum of the projected clearance funds based on the price  (Net Money) for all buy and 
sell positions on the report.  
CLEARANCE MONEY 
NET OPEN 
This is the sum of the funds amount processed at settling bank for all buy and sell positions on 
the rep ort. 
TMPG CHARGE NET 
OPEN 
This is the sum of the T MPG fail finance charges associated with the settled pool obligation for 
all the buy and sell positions on the report.  
Print Image Report Sort Order 
Activity reported via this report will fall under one of the following categories and the report will be sorted 
accordingly: 
1. Creation of Pool [[obligations]]. 
2. Pool Obligation Updates. 
 
Within the above categories, the MBSD CCP Pool Obligation Activity Report is sorted as follows:  
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number. 
4. [[settlement]] Date. 
5. Buys (secondary D/D sort). 
6. Sells (secondary D/D sort). 
7. Activity Values (Alpha order). 
8. Status Values (Alpha order). 
9. POID number. 

---

## Page 77

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Pending [[settlement]] Report 77 
MBSD CCP POOL OBLIGATION PENDING [[settlement]] 
REPORT 
About the MBSD CCP Pool Obligation Pending [[settlement]] Report 
The MBSD CCP Pool Obligation Pending [[settlement]] Report is produced each day at close of business to 
reflect all open Pool [[obligations]] (POIDs). This includes POIDs established via the current day’s Pool Netting 
cycle for daily and Expanded Pool Netting, Pool Conversion, as well as failed POIDs from previous days. This 
report provides a comprehensive listing of all the [[Member]]’s open [[settlement]] [[obligations]] with [[FICC]].  
Members use this report to monitor and track all outstanding settlements versus [[FICC]]. 
Report Format  
The MBSD CCP Pool Obligation Pending [[settlement]] Report is produced in two formats 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP Pool 
Obligation Pending [[settlement]] Report is available in NDM only. The MRO format can be found at 
http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM CCP Pool Obligation Pending [[settlement]].  
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 

---

## Page 78

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Pendi ng [[settlement]] Report 78 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Pool Level Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade Details are listed with the following 
data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to 
each [[Member]] (followed by) the two -character alphanumeric aggregate which links an 
Account [[ID]] ([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an 
aggregate for risk management and cash [[settlement]] reporti ng purposes.  
PART [[ID]] In this report, the Part [[ID]] refers to the Account [[ID]], which is also called the [[participant]] 
Symbol: A 4-character identifier, the Account [[ID]] represents the primary level of system 
identification. Trade submission occurs at the account level.  
[DATE OF REPORT] The date the report was created.  
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] MONTH 
AND YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY.  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the trade.  
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
MARKET PRICE  Current market price as determined by MBSD which is used for determining P&L of the 
trade. 
 
  

---

## Page 79

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Pendi ng [[settlement]] Report 79 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Netting and 
Pool Conversion. 
FIELD  EXPLANATION  
STATUS • RND – Reflecting that the open POIDs are awaiting [[settlement]] versus [[FICC]] (as receive and 
deliver [[obligations]]).  
• CANC – Indicating a Pool Obligation (POID) canceled as the result of a Pool Substitution 
processed via an EPN -generated Cancel and Correct message.  
• FCAN – Indicating a Pool Obligation (POID) administratively canceled by [[FICC]].  
• SETT – Indicating a Pool Obligation (POID) settled versus [[FICC]] on the report date (current 
day).  
POID Pool Obligation [[ID]]: Identifier assigned to pool settlements vs. [[FICC]].  
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
T/D Trade Date: The Trade Date field is populated based on trade type.  
• SPT trades: Trade Date will reflect the associated SPT trade date.  
• STIP allocations: Trade Date will reflect the associated STIP trade date.  
• Generic TBA trade allocations: Trade Date will be blank.  
S/D [[settlement]] Date: The contractual [[settlement]] date of the trade.  
D/D Delivery Date: The date that the pools submitted are scheduled to be delivered in satisfaction of 
the TBA trade.  
CONTRA Contra -side Identifier: Consists of contr a-side’s Clearing [[participant]] Number and Aggregate.  
• [[FICC]]: Generic TBA Account.  
• FSTI: [[FICC]]’s Stipulated Account.  
• FSPT: [[FICC]]’s Specified Pool Trade  Account . 
ORIG FACE Original Face: The par value of the trade is reported in this field.  
CURR FACE Current Face: The current value of the pool. It is determined by multiplying the original face of 
the pool by the current factor.  
PRICE For SPT, STIP, and Generic TBA Pool Conversions: Trade Pric e. 
[[obligations]] vs [[FICC]] via Pool Netting: [[FICC]] System price used for Pool Netting. 
NET MONEY Projected clearance funds.  
P & I Principle & Interest: Reflects MBSD calculated P&I impact (CR = credit  to [[Member]] and DR = 
debit to [[Member]]) of failing POID.  
 
  

---

## Page 80

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Pendi ng [[settlement]] Report 80 
Pool Level Sub-Totals 
Pool Level Sub-Totals are reflected at the TBA [[CUSIP]] level. 
FIELD  EXPLANATION  
ORIGINAL FACE OPEN 
SELL 
This is the sum of the Original Face for all sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE OPEN 
SELL 
This is the sum of the Current Face for all sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN SELL This is the sum of the net money  for all sell positions for the TBA [[CUSIP]] and S/D.  
P & I OPEN SELL This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all sell positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE OPEN 
BUY 
This is the sum of the Original Face for all buy positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE OPEN 
BUY 
This is the sum of the Current Face for all buy positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN BUY This is the sum of the net money  for all buy positions for the TBA [[CUSIP]] and S/D.  
P & I OPEN BUY This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all buy positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE 
NET OPEN 
This is the sum of the Original Face for all buy and sell positions for the TBA [[CUSIP]] and 
S/D. 
CURRENT FACE NET 
OPEN 
This is the sum of the Current Face for all buy and sell positions for the TBA [[CUSIP]] and 
S/D. 
NET MONEY NET OPEN  This is the sum of Net M oney for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
P & I NET OPEN This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all buy and sell positions for the TBA [[CUSIP]] and S/D.  
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
ORIGINAL FACE OPEN 
SELL 
This is the sum of the Original Face for all sell positions on the report.  
CURRENT FACE OPEN 
SELL 
This is the sum of the Current Face for all sell positions on the report.  
NET MONEY OPEN SELL This is the sum of the net money  for all sell positions on the report.  
P & I OPEN SELL This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all sell positions on the report.  

---

## Page 81

MBSD Operational Pool Net Reports Guide 
MBSD CCP Pool Obligation Pendi ng [[settlement]] Report 81 
FIELD  EXPLANATION  
ORIGINAL FACE OPEN 
BUY 
This is the sum of the Original Face for all buy positions on the report.  
CURRENT FACE OPEN 
BUY 
This is the sum of the Current Face for all buy positions on the report.  
NET MONEY OPEN BUY This is the sum of the net money  for all buy positions on the report.  
P & I OPEN SELL This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all buy positions on the report.  
ORIGINAL FACE NET 
OPEN 
This is the sum of the Original Face for all buy and sell positions on the report.  
CURRENT FACE NET 
OPEN 
This is the sum of the Current Face for all buy and sell positions on the report.  
NET MONEY NET OPEN  This is the sum of the Net Money for all buy and sell positions on the report.  
P & I OPEN SELL This is the sum of the calculated P & I impact (CR = credit to [[Member]] and DR = debit to 
[[Member]]) of failing POIDs for all buy and sell positions on the report.  
Print Image Report Sort Order 
The MBSD CCP Pool Obligation Pending [[settlement]] Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest. 
3. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level). 
4. Pool Number. 
5. [[settlement]] Date. 
6. Buys (secondary D/D sort). 
7. Sells (secondary D/D sort). 
8. Status Values (Alpha Order). 
9. POID number. 
  

---

## Page 82

MBSD Operational Pool Net Reports Guide 
MBSD CCP Uncompared R eport 82 
MBSD CCP UNCOMPARED REPORT 
About the MBSD CCP Compared Pool Instruct Report 
The MBSD CCP Uncompared Report is produced daily at close of business to reflect the final disposition of all 
Uncompared Pool Instructs that remain in an Uncompared or Advisory state on the current business day. (A 
Pool Instruct is reported as Uncompared when a submitting firm enters a Pool Instruct and it is not matched 
versus [[FICC]]’s system generated Pool Instruct created from the EPN submissions. A Pool Instruct is reported 
as an Advisory when the [[FICC]] system generated Pool Instruct has been created and the firm has not 
submitted a matching Pool Instruct.   
This report is cumulative. That is, Pool Instructs in Uncompared or Advisory states will continue to be included 
on the report each day until the Pool Instruct is either compared, canceled by the [[Member]] or canceled by the 
system. 
Members may use the MBSD CCP Uncompared Report to identify Pool Instructs that have not yet been 
compared with [[FICC]].  The report may also be used to review any actions subsequently taken on Uncompared 
or Advisory Pool Instructs, such as cancels or other status changes. 
Report Format  
The MBSD CCP Compared Pool Instruct Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the MBSD CCP 
Uncompa red Report is available in NDM only. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. Look for: 
 
• MRO NDM CCP Uncompared. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
  

---

## Page 83

MBSD Operational Pool Net Reports Guide 
MBSD CCP Uncompared R eport 83 
Print Image Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Report Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section of the print image (pdf) report, the individual Trade Details are listed with the following 
data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned 
to each [[Member]] (followed by) the two -character alphanumeric aggregate which links an 
Account [[ID]] ([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to 
an aggregate for risk management and cash [[settlement]] reporting purposes.  
PART [[ID]] [[participant]] Symbol: A 4 -character identifier, the Account [[ID]] represents the primary level 
of system identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was created.  
PRODUCT Product Code  Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information. 
FIELD  EXPLANATION  
[[[settlement]] MONTH 
AND YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY. 
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  

---

## Page 84

MBSD Operational Pool Net Reports Guide 
MBSD CCP Uncompared R eport 84 
FIELD  EXPLANATION  
POOL NUM Pool Number: The pool number allocated to the TBA trade that will be settled for the 
trade. 
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
Trade Details 
The following table explains those trade details most relevant to events taking place during Pool Allocation. 
FIELD  EXPLANATION  
ACTIVITY/STATUS A combination of Activity  and  Status codes are used to identify the type of activity being 
reported. The MBSD CCP Uncompared Report can reference many events, reported as 
activity types.  Please see below for Activity and Status types:  
• (UNCP) UNCP – Submitter’s pool instruct does not c ompare with input of target 
contra -side and results in an uncompared pool instruct condition. 
• (UNCP) PPUN – Submitter’s pool instruct does not compare with input of target 
contra -side and results in an uncompared pool instruct condition and the pool is in 
Pending Pool Add status . 
• (UNCP) ADV – An advisory condition is created when a contra- side’s submission of a 
pool instruct does not compare with the [[Member]]’s input . 
• (UNCP) ADVP – An advisory condition is created when a contra -side’s submission of 
a pool instruct does not compare with the [[Member]]’s input and the pool is in Pending 
Pool Add status . 
• (UCAN) ADVC – Submitter’s unilateral cancel of a compared pool instruct results in 
the cancellation of the target pool instruct and the creation of a pool instruct a dvisory 
condition (since the counterparty’s pool instruct is reverted to an uncompared status) . 
• (UCAN) ADCP – Submitter’s unilateral cancel of a compared pool instruct results in 
the cancellation of the target pool instruct and the creation of a pool instr uct advisory 
condition and pool is Pending Pool Add status (since the counterparty’s pool instruct 
reverts to an Uncompared Pending Pool Add state) . 
• (UCAN) UNCP – An uncompared condition is created when a contra -side submits a 
unilateral cancel of a compar ed pool instruct.  
• (UCAN) PPUN – An uncompared condition is created when a contra -side submits a 
unilateral cancel of a compared pool instruct and the pool is Pending Pool Add status.  
• (REPR) PPUN – The addition of a Pending Pool Add status to an existing 
uncompared PID.  
• (REPR) UNCP – The removal of a Pending Pool Add status from an existing 
uncompared PID.  
• (CANC) ((CANC)) – Submitter cancels its uncompared pool instruct . 
• (REPR) ((CANC)) – An uncompared pool instr uct is canceled due to the repricing of 
the pool resulting in the supporting TBA position being less than the value of the pool 
or the pool’s current factor is reported as zero. 
• (SCAN) ((CANC)) – An uncompared pool instr uct is systemically canceled upon the 
start of the target pool netting cycle . 
Note: A status value in parentheses (( )) denotes that the record will reflect on the current 
day’s output only. Parentheses are used solely to  highlight events/statuses leading to a 
record’s final disposition before no longer being viewable to the partici pant.  
B/S BUY/SELL: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s 
perspective.  

---

## Page 85

MBSD Operational Pool Net Reports Guide 
MBSD CCP Uncompared R eport 85 
FIELD  EXPLANATION  
XREF The XREF is assigned by the [[Member]] – it’s alphanumeric, extending from 1 to 16 
characters in length. It must be unique to that [[Member]] – the [[Member]] cannot have any 
other trades in the system with that same XREF.  
PID Pool [[ID]]: Transaction [[ID]] assigned to the Pool Instruct . 
T/D Trade Date of the trade.  
E/D Entry Date: Date of submission resulting in the transaction.  
S/D [[settlement]] Date: The contractual [[settlement]] date of the trade.  
D/D Delivery Date: The date that the pools submitted on the Pool Instructs are scheduled to be 
delivered in satisfaction of the TBA trade.  
CONTRA AGG  Contra -side Identifier: Consists of contr a-side Clearing [[participant]] Number and Aggregate.  
CONTRA [[ID]] Contra -side’s Clearing Account Symbol.  
ORIG FACE Original Face: The par value of the trade is reported in this field.  
CURR FACE Current Face: The current value of the pool. It is determined by multiplying the original 
face of the pool by the current factor.  
PRICE Trade Price.  
NET MONEY Projected clearance funds.  
CDR Customer Delivery Request: Y -T if applied at the TBA [[CUSIP]] level, Y -P if applied at the 
pool number level, and Y -I if applied via the initial pool instruct (reflects only to submitter of 
the CDR). 
REPRICE Populated with a Yes or No. If populated as “YES,” impact of Reprice is reflected in 
Current Face and [[settlement]] Value fields.  
DK CODE DK Code is now obsolete: Previously, this output reflected the DK code on any [[Member]] 
instructs that were DK’d by the counterparty; as all instructs are now versus [[FICC]], this DK 
code field is obsolete and will no longer be populated/used.  
Report Sub-Totals 
Report Sub-Totals are reflected at the TBA [[CUSIP]] level. 
FIELD  EXPLANATION  
ORIGINAL FACE OPEN SELL  This is the sum of the Original Face for all sell positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE OPEN SELL  This is the sum of the Current Face for all sell positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN SELL This is the sum of the net money  for all sell positions for the TBA [[CUSIP]] and S/D.  
ORIGINAL FACE OPEN BUY This is the sum of the Original Face for all buy positions for the TBA [[CUSIP]] and S/D.  
CURRENT FACE OPEN BUY  This is the sum of the Current Face for all buy positions for the TBA [[CUSIP]] and S/D.  
NET MONEY OPEN BUY This is the sum of the net money  for all buy positions for the TBA [[CUSIP]] and S/D.  

---

## Page 86

MBSD Operational Pool Net Reports Guide 
MBSD CCP Uncompared R eport 86 
FIELD  EXPLANATION  
ORIGINAL FACE NET OPEN  This is the sum of the Original Face for all buy and sell positions for the TBA [[CUSIP]] 
and S/D. 
CURRENT FACE NET OPEN This is the sum of the Current Face for all buy and sell positions for the TBA [[CUSIP]] 
and S/D. 
NET MONEY NET OPEN  This is the sum of the net money  for all buy and sell positions for the TBA [[CUSIP]] and 
S/D. 
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD  EXPLANATION  
ORIGINAL FACE OPEN SELL  This is the sum of the Original Face for all sell positions on the report.  
CURRENT FACE OPEN SELL  This is the sum of the Current Face for all sell positions on the report.  
NET MONEY OPEN SELL This is the sum of the net money  for all sell positions on the report.  
ORIGINAL FACE OPEN BUY This is the sum of the Original Face for all buy positions on the report.  
CURRENT FACE OPEN BUY  This is the sum of the Current Face for all buy positions on the report.  
NET MONEY OPEN BUY This is the sum of the net money  for all buy positions on the report.  
ORIGINAL FACE NET OPEN  This is the sum of the Original Face for all buy and sell positions on the report.  
CURRENT FACE NET OPEN This is the  sum of the Current Face for all buy and sell positions on the report.  
NET MONEY NET OPEN  This is the sum of the net money  for all buy and sell positions on the report.  
Print Image Report Sort Order 
The MBSD CCP Compared Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
3. Pool Number. 
4. Contra-side [[participant]] Number & Aggregate. 
5. Contra-side Account [[ID]]. 
6. [[settlement]] Date. 
7. Buys (secondary D/D sort). 
8. Sells (secondary D/D sort). 
9. Activity Values (Alpha order). 
10. Status Values (Alpha order). 
11. PID number. 

---

## Page 87

MBSD Operational Pool Net Reports Guide 
MBSD TMPG Monthly Rec ap Report 87 
MBSD TMPG MONTHLY RECAP REPORT 
About the MBSD TMPG Monthly Recap Report 
The TMPG Monthly Recap Report is produced on the last business day of each month at the close of business 
to reflect all TMPG charges for each Pool Obligation that occurred during that month.  MBSD calculates and 
pays/collects a fail charge based on the recommendation of the Treasury Market Practices Group (“TMPG”). 
This report is not cumulative. (Note: As this report is not cumulative, Pool [[obligations]] settled from previous 
months are not included on this report.) 
The MBSD TMPG Monthly Recap Report will include the following activities: 
• All POIDs settled within the current month; 
• Number of days for which a TMPG charge is applied (by rate if applicable); 
• Total TMPG charge per POID. 
 
Members will use this report to balance MBSD generated TMPG charges versus their own internal books and 
records. 
Report Format  
The MBSD TMPG Monthly Recap Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the TMPG Monthly 
Recap Report is available in NDM only. All MRO Report layouts can be found in the [[FICC]] MBSD User 
Documentation section of the [[DTCC]] website (http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/[[FICC]]-mbsd-user-
documentation#MachineReadableOutput) Look for: 
• File Transmission Layouts for MBSD TMPG Recap Report NDM Format. 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
  

---

## Page 88

MBSD Operational Pool Net Reports Guide 
MBSD TMPG Monthly Rec ap Report 88 
Print Image Report Layout 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note 
In general, the layout of pri nt-image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header, Trade 
Details, Report Sub-Totals, and Report Footer. 
Print Image Report Section Information 
Within each section, the MBSD TMPG Monthly Recap details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three- digit [[participant]] [[ID]] assigned to 
each [[Member]] (followed by) the two -character alphanumeric aggregate. 
PART [[ID]] The four -character account symbol.  
[DATE OF REPORT] The date the report was created. 
PRODUCT Product Code Description. This is MBS for Mortgaged- Backed Security. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header. 
FIELD  EXPLANATION  
SIFMA CLASS Indicates the SIFMA [[settlement]] Class  which could be Class A, B, C, or D  
[[[settlement]] MONTH 
AND YEAR] 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY.  
TBA [[CUSIP]]  The nine -character TBA [[CUSIP]].  
  

---

## Page 89

MBSD Operational Pool Net Reports Guide 
MBSD TMPG Monthly Rec ap Report 89 
Trade Details 
The following table explains those trade details most relevant to fail charges associated with settled Pool 
[[obligations]]. 
FIELD EXPLANATION 
POID Pool Obligation [[ID]]: Identifier assigned to pool [[obligations]] vs. [[FICC]] . 
POOL NUMBER Pool Number. 
POOL [[CUSIP]] Pool [[CUSIP]] Number. 
B/S Buy or Sell . 
S/D [[settlement]] Date. 
CLEARANCE DATE Date that the pool obligation cleared.  
ORIG FACE Original Face: The par value of the pool obligation . 
CURR. FACE Current Face: The current value of the pool. It is determined by multiplying the 
original face of the pool by the current factor.  
PRICE The [[settlement]] price of the pool obligation . 
NET MONEY The dollar value in which the pool obligation settled for based on the price. 
RATE % Rate used for TMPG fail charge processing for [[settlement]] obligation fails . 
EFFECTIVE DATES (FROM/TO)  The date range for the given rate (%) . 
TMPG DAYS The number of days fail charge is assessed from original [[settlement]] date. 
ACCRUAL Total charge accrued based on the net money, TMPG rate, and the number of 
TMPG days . 
TOTAL TMPG CHARGE Reflects the total TMPG fail finance charge associated with the settled pool 
obligation.  DR is displayed for a debit and CR is displayed for a credit.  
Pool Level Sub-Totals 
At the end of each SIFMA class, there is a breakdown showing the total Credit, Debit, and Net TMPG charge 
per pool number/[[CUSIP]] number. There is also a breakdown of the total Credit, Debit and Net TMPG charge 
per TBA [[CUSIP]]. 
FIELD  EXPLANATION  
POOL NUMBER Pool Number. 
POOL [[CUSIP]] Pool [[CUSIP]]. 
CREDIT TMPG CHARGE  Total Credit TMPG Charges for the given Pool Number/Pool [[CUSIP]] . 
DEBIT TMPG CHARGE Total Debit TMPG Charges for the given Pool Number/Pool [[CUSIP]] . 

---

## Page 90

MBSD Operational Pool Net Reports Guide 
MBSD TMPG Monthly Rec ap Report 90 
FIELD  EXPLANATION  
NET TMPG CHARGE The Net TMPG Charge for the given Pool Number/Pool [[CUSIP]]. The difference 
between the Credit TMPG Charge and the Debit TMPG charge. CR = Credit, DR = 
Debit. 
TBA [[CUSIP]] To-Be-Announced [[CUSIP]] . 
CREDIT TMPG CHARGE  Total Credit TMPG Charges for the given TBA [[CUSIP]] . 
DEBIT TMPG CHARGE Total Debit TMPG Charges for the given TBA [[CUSIP]] . 
NET TMPG CHARGE The Net TMPG Charge for the given TBA [[CUSIP]]. The difference between the Credit 
TMPG Charge and the Debit TMPG charge. CR = Credit, DR = Debit . 
Report Footer 
At the end of the report, there is a breakdown showing the total items, Original Face, Current Face, Clearance 
Proceeds and TMPG Charge per buy, sell, and the net total of the buy and sells for each SIFMA [[settlement]] 
Class. In addition, there is a grand total incorporating all the SIFMA [[settlement]] Classes. 
FIELD  EXPLANATION  
CLASS A, B, C, D AND ALL  Indicates the SIFMA [[settlement]] Class. "All" indicates the grand total for all the 
SIFMA Classes . 
SELL ITEMS Total Sell items for the given SIFMA Class . 
SELL ORIGINAL FACE Total Sell Original Face for the given SIFMA Class . 
SELL CURRENT FACE  Total Sell Current Face for the given SIFMA Class . 
SELL CLEARANCE PROCEEDS Total Sell Clearance Proceeds for the given SIFMA Class . 
SELL TMPG CHARGE Total Sell TMPG Charge for the given SIFMA Class; CR = Credit, DR = Debit . 
BUY ITEMS Total Buy Items for the given SIFMA Class . 
BUY ORIGINAL FACE Total Buy Original Face for the given SIFMA Class . 
BUY CURRENT FACE Total Buy Current Face for the given SIFMA Class . 
BUY CLEARANCE PROCEEDS Total Buy Clearance Proceeds for the given SIFMA Class . 
BUY TMPG CHARGE Total Buy TMPG Charge for the given SIFMA Class; CR = Credit, DR = Debit . 
TOTAL/NET ITEMS Total Net Items of the buys and sells for the given SIFMA Class . 
TOTAL/NET ORIGINAL FACE Total Net Original Face of the buys and sells for the given SIFMA Class . 
TOTAL/NET CURRENT FACE  Total Net Current Face of the buys and sells for the given SIFMA Class . 
TOTAL/NET CLEARANCE 
PROCEEDS 
Total Net Clearance Proceeds of the buys and sells for the given SIFMA Class . 
TOTAL/NET TMPG CHARGE Total Net TMPG Charge for the buys and sells for the given SIFMA Class; CR = 
Credit, DR = Debit. 

---

## Page 91

MBSD Operational Pool Net Reports Guide 
MBSD TMPG Monthly Rec ap Report 91 
Print Image Report Sort Order 
The MBSD TMPG Monthly Recap Report is sorted as follows: 
1. SIFMA Class. 
2. [[settlement]] Month/Year = earliest to latest. 
3. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level). 
4. Pool Number. 
5. [[settlement]] Date. 
6. POID number. 

---

## Page 92

MBSD Operational Pool Net Reports Guide 
MBSD RTTM [[participant]] Reprice Report 92 
MBSD RTTM [[participant]] REPRICE REPORT 
About the MBSD RTTM [[participant]] Reprice Report 
When [[FICC]] receives pool factor updates, they are processed on a real-time basis. When a pool factor update 
is applied to a Pool Number on a Specified Pool Trade, the current face and final money are recalculated and 
updated on the SPT to reflect the change. Although the updated current face and final money are reflected on 
the OCR, the OCR does not indicate if a factor update was applied. The [[participant]] Reprice Report indicates 
when a factor update has been applied to a SPT trade, and displays the original face of the trade at time of 
submission to RTTM, the current face and then the final money prior to the factor update and the final money 
after the factor update has been processed. 
Members use this report to know when a factor update has been applied to a SPT. This report is particularly 
useful to members who [[DO]] not subscribe to SWIFT-based Interactive Messaging, since they will not receive the 
Reprice Message when a factor update is applied. This report will display a SPT on the day it is submitted to 
RTTM, and then each time a factor update is applied to the trade. [[FICC]] will only process factor updates until 
the evening of CSD. The report is only created at end-of-day. 
Report Format  
The MBSD RTTM [[participant]] Reprice Report is available in MBSD RTTM Web Report Center solely in Print 
Image format (a readable format suitable for printing). 
Print Image Report Layout 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report is divided into multiple sections, including the Account Header, the TBA [[CUSIP]] Header and Trade 
Details. 
Print Image Report Section Information 
Within each section, the individual RTTM [[participant]] Reprice details are listed, with the following data.  

---

## Page 93

MBSD Operational Pool Net Reports Guide 
MBSD RTTM [[participant]] Reprice Report 93 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
ACCOUNT [[ID]] A 4-character identifier, the Account [[ID]] represents the primary level of system identification. 
Trade submission occurs at the account level. (Also referred to as the Symbol) . 
NAME The name of the [[Member]]. 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header. Each pool must back to a TBA [[CUSIP]]. The 
pools are grouped by TBA [[CUSIP]] and listed under the TBA [[CUSIP]] Description. 
FIELD  EXPLANATION  
TBA [[CUSIP]] 
DESCRIPTION 
The TBA [[CUSIP]] and the Security Description.  
Trade Details 
The following table explains those trade details most relevant to the pool number associated with the trade. 
FIELD  EXPLANATION  
POOL # The pool number of the SPT.  
MAT DATE Maturity Date: The date the pool matures.  
S/D [[settlement]] Date: The [[settlement]] date of the trade.  
B/S Buy/Sell: Buy or Sell indicator.  
ORIGINAL FACE The par value of the pool at the time it was issued. This is the par amount entered at trade 
submission to RTTM.  
CURRENT FACE The current par value of the pool. It is determined by multiplying the original face by the 
current month’s pool factor. The difference between the original face and the current face 
is how much principal has been paid on the mortgage pool.  
PRICE The price of the trade. For brokered trades, the price reflected here is the [[settlement]] price 
or the price exclusive of commission.  
FINAL MONEY (NEW)  The final money before the factor update is  applied.  
FINAL MONEY (OLD)  The final money after the factor update is applied.  
CONTRA This is the contraside to the trade.  
XREF The XREF is assigned by the [[Member]] - it’s alphanumeric, extending from 1 to 16 
characters in length. It must be unique to that [[Member]] - the [[Member]] cannot have any 
other trades in the system with that same XREF.  

---

## Page 94

MBSD Operational Pool Net Reports Guide 
MBSD RTTM [[participant]] Reprice Report 94 
FIELD  EXPLANATION  
TRADE [[ID]]/TRAN [[ID]] If the trade is uncompared, the Transaction [[ID]] will be displayed. Otherwise, if the trade is 
compared, the Trade [[ID]] will be displayed.  
M/U This is the trade status. M = Matched and U = Unmatched.  
RSN Reason: This field indicates the reason the trade was revalued.  
• D: Used when RTTM applied a [[default]] value because the [[Member]] either did not 
include final money on the trade or the final money was incorre ct. 
• F: Used when a factor update has been applied to the trade.  
• S: Used when a security is set eligible/ineligible.  
• M: Matched with Modifications, so the price is only matched up to 6 digits to the right 
of the decimal, but one of the members submitted 9 digits to the right of the decimal.  
Print Image Report Sort Order 
The MBSD CCP Compared Pending Pool Add Report is sorted as follows: 
1. TBA [[CUSIP]] (report reflects sub-totals at the TBA [[CUSIP]] level) = ascending order. 
2. Pool Number = ascending order. 
3. [[settlement]] Date. 
4. Tran [[ID]]. 

---

## Page 95

MBSD Operational Pool Net Reports Guide 
POID Conv ersion R eport 95 
POID CONVERSION REPORT 
The POID Conversion Report Explained 
To see an example of the POID Conversion Report while you learn about its use, available formats, layout, 
header information and sort order, please visit the MBS [[Novation]] Reports Explained page on the [[DTCC]] 
Learning Center. It may be helpful to have it open while reading this guide as it will allow you to view actual 
reports in full size and interact with them to learn more. 
About the POID Conversion Report 
The POID Conversion Report is produced once daily after the DNA, TBA Reprice and Conversion process and 
reflects the following SPT trade and allocations converted to POIDs at trade price on the current business day:  
• SPT Trade: SPT trade with CSD=NBD result in POIDs vs FSPT at trade price. 
Note  
SPT trades submitted after the conversion job is run that have CSD=NBD, will be converted at [[EOD]] and reflected in 
the Cash Trade POID Conversion output.  
• STIP PID: PID targeting STIP with DD=NBD result in POIDs vs FSTI at trade price. 
• Generic PID: PID targeting novated TFTD/TBA or SBON with DD=NBD that missed the daily Pool Net 
cycle 1 result in POIDs vs [[FICC]] at trade price.  
Note  
This is only applicable to PIDs with non- SIFMA CSD, as PIDs targeting SIFMA CSD will be processed in the 
Expanded Pool Net cycle.  
To learn more about the timeframes of the processes relevant to this report, please refer to the MBSD 
Processing Schedule & Timeframes document which may be found in the [[participant]] Reference 
Documentation (MBS) section on www.[[DTCC]].com. 
Report Format  
The POID Conversion Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
  
 
1 This can occur due to operations DD update, or processing of DK on pre-net CC. 

---

## Page 96

MBSD Operational Pool Net Reports Guide 
POID Conv ersion R eport 96 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the POID Conversion 
Report is available in NDM only. The MRO format can be found at http://www.[[DTCC]].com/clearing-services/[[FICC]]-
mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM Pool Conversion. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Print Image Report Layout 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report details the SPT trades and STIP and generic TBA allocations converted to POIDs on the current 
business day grouped by [[settlement]] month/year and TBA [[CUSIP]]. The report has multiple sections, including 
ones for SPT trades, STIP allocations and generic TBA allocations. Within these sections, the original SPT 
trade/PIDs are listed, followed by resulting POIDs. This report also includes an Account Header, the TBA 
[[CUSIP]] Header, Original Trade Details, Trade Sub-Totals, Generated POIDs, and Generated POID Sub-Totals. 
Print Image Report Section Information 
Within each section, the individual POID Conversion details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
[[participant]]/ AGGREGATE A three-digit number is assigned to each [[Member]] followed by a 2- digit number or 
alphanumeric identifier . 
ACCOUNT DESCRIPTION The account name. 

---

## Page 97

MBSD Operational Pool Net Reports Guide 
POID Conv ersion R eport 97 
FIELD EXPLANATION 
ACCOUNT [[ID]] The four -character account symbol . 
BUSINESS DATE A date field showing the current business date. 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA CUSP of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD EXPLANATION 
[[settlement]] 
MONTH/YEAR 
[[settlement]] month and year . 
TBA [[CUSIP]] 9-character To Be Announced [[CUSIP]] . 
SECURITY CLASS Description of this TBA [[CUSIP]] . 
Original SPT Trades / PIDs 
Displays information on each SPT trade or allocation converted.  
FIELD EXPLANATION 
TRADE NBR Trade number on associated trade. 
TRADE XREF The XREF is assigned by the [[Member]] – it's alphanumeric, extending from 1 to 16 
characters in length. It must be unique to that [[Member]] – the [[Member]] cannot have any 
other trades in the system with that same XREF.  
PID Pool Instruct identifier (displayed for allo cation conversions of STIP and Generic TBA 
trades only) . 
B/S B or S (Buy or Sell) . 
T/D Trade Date (for SPT trades only) . 
D/D Delivery Date (for STIP and Generic TBA allocations only) . 
S/D Contractual [[settlement]] Date. 
CONTRA Contra on the trade, equal to FSPT for SPT trades, FSTI for STIP PIDs and FTBA for 
generic TBA PIDs . 
POOL NBR Pool Number. 
POOL [[CUSIP]] Pool [[CUSIP]]. 
STTL PRICE Price, exclusive of commission . 
ORIG FACE Original face . 
CURR FACE Current face. 
NET MONEY Net money . 

---

## Page 98

MBSD Operational Pool Net Reports Guide 
POID Conv ersion R eport 98 
FIELD EXPLANATION 
CR/DR Indicator  Net money indicator, “CR” for credit, “DR” for debit . 
Generated POIDs 
Displays information on each POID created.  
FIELD EXPLANATION 
POID NBR POID identifier . 
TRADE NBR Trade number associated with this POID . 
B/S B or S (Buy or Sell) . 
D/D Delivery Date on POID . 
S/D Contractual [[settlement]] Date. 
CONTRA Contra on the trade, equal FSPT for SPT POIDs, FSTI for STIP POIDs and FTBA for 
generic TBA POIDs.  
POOL NBR Pool number on the POID . 
POOL [[CUSIP]] Pool [[CUSIP]] on the POID . 
STTL PRICE [[settlement]] price on the POID . 
ORIG FACE Original face on the POID . 
CURR FACE Current face on the POID . 
NET MONEY Net money on the POID . 
CR/DR Indicator  Net money indicator, “CR” for credit, “DR” for debit . 
Sub-Totals 
Sub-totals are provided for the following: 
• Sub-totals per MM/YYYY and TBA [[CUSIP]]  
• Sub-totals per Section (SPT, STIP and generic TBA)  
• Sub-totals per Report   
 
Where: 
• Orig Face = Net value of ORIG FACE of all trades, signed with “-“ if short 
• Current Face = Net value of CURR FACE of all trades, signed with “-“ if short 
• Net Money = Net value of NET MONEY of all trades, signed with “-“ if <$0. 
  

---

## Page 99

MBSD Operational Pool Net Reports Guide 
POID Conv ersion R eport 99 
Print Report Sort Order 
1. SPT section, followed by STIP section, followed by generic TBA section. 
2. SPT trades/PIDs, followed by POIDs. 
3. [[settlement]] Month/Year = earliest to latest. 
4. TBA [[CUSIP]] = ascending order. 
 
For SPT trades: 
1. [[settlement]] Date = earliest to latest. 
2. Trade Number (ascending). 
 
For PIDs: 
1. Delivery Date = earliest to latest. 
2. Trade Number (ascending). 
 
For POIDs (regardless of source): 
1. Same order as associated SPT trades/PIDs. 
 
Note  
The POIDs are not sorted by POID order but rather follow the same order as associated SPT trade/PID from which they 
were generated from. By doing this, cross -referencing between the 2 sections will be easier.  

---

## Page 100

MBSD Operational Pool Net Reports Guide 
POID Factor Update Report 100 
POID FACTOR UPDATE REPORT 
The POID Factor Update Report Explained 
To see an example of the POID Factor Update Report while you learn about its use, available formats, layout, 
header information and sort order, please visit the MBS [[Novation]] Reports Explained page on the [[DTCC]] 
Learning Center. It may be helpful to have it open while reading this guide as it will allow you to view actual 
reports in full size and interact with them to learn more. 
About the POID Factor Update Report 
The POID Factor Update Report is a daily, end-of-day report and captures cash differences due to factor 
updates for POIDs that already settled and have CSD in blackout period. To learn more about the timeframes 
of the processes relevant to this report, please refer to the MBSD Processing Schedule & Timeframes 
document which may be found in the [[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com. 
This report allows members to reconcile the money differences based on the factor updates. The report reflects 
all settled POIDs that incurred [[settlement]] value differences due to factor update.   
Report Format  
The POID Factor Update Report is produced in two formats: 
1. Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report; 
2. Print Image format available in MBS Pool Net Report Center on the MBS Web Front End. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the POID Factor Update 
Report is available in NDM only. The MRO format can be found at http://www.[[DTCC]].com/clearing-services/[[FICC]]-
mbsd/mbs-[[Novation]]-documentation. Look for: 
• MRO NDM Pool Obligation Factor Update. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist – there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
  

---

## Page 101

MBSD Operational Pool Net Reports Guide 
POID Factor Update Report 101 
Print Image Report Layout 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only; 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report begins with Account Header information then details all POIDs with [[settlement]] value differences 
due to factor update processed on the current business day, grouped by [[settlement]] month/year, TBA [[CUSIP]] 
and pool number/[[CUSIP]]. 
Print Image Report Section Information 
Within each section, the individual POID Factor Update details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
[[participant]]/ AGGREGATE A three -digit number is assigned to each [[Member]] followed by a 2- digit number or 
alphanumeric identifier . 
ACCOUNT DESCRIPTION The account name. 
ACCOUNT [[ID]] The four -character account symbol . 
BUSINESS DATE A date field showing the current business date. 
Pool Header Information 
Within each section, displays information on pool of current grouping; 1 per pool [[CUSIP]] included in this report. 
FIELD EXPLANATION 
[[settlement]] MONTH/YEAR  Contractual [[settlement]] month and year . 
TBA [[CUSIP]] 9-character To Be Announced [[CUSIP]] .    
POOL NUMBER Pool number . 
POOL [[CUSIP]] Pool [[CUSIP]].   

---

## Page 102

MBSD Operational Pool Net Reports Guide 
POID Factor Update Report 102 
FIELD EXPLANATION 
[[settlement]] FACTOR  Assumed factor for [[settlement]] Month/Year for this pool, which was in effect when 
this POID settled . 
UPDATED FACTOR  Updated factor for [[settlement]] Month/Year for this pool . 
POIDs  
Displays information on each POID that was updated due to a factor update. 
FIELD EXPLANATION 
POID NBR POID identifier . 
B/S B or S (Buy or Sell) . 
D/D Delivery Date on POID, which is also the date this POID settled . 
S/D Contractual [[settlement]] Date. 
CONTRA Contra on the trade, equal FSPT for SPT trades, FSTI for STIP trades and [[FICC]] for 
TFTD/TBA and SBON [[obligations]] . 
STTL PRICE [[settlement]] price on the POID . 
ORIG FACE Original face on the POID . 
STTL CURR FACE Current face on the POID based on [[settlement]] Factor . 
STTL NET MONEY Net money ([[settlement]] value) on the POID, based on [[settlement]] Factor . 
UPD CURR FACE Current face on the POID based on Updated Factor . 
UPD NET MONEY Net money ([[settlement]] value) on the POID, based on Updated Factor . 
DIFFERENCE NET MONEY  Difference in [[settlement]] and updated net money.  
CR/DR Indicator  Difference Net Money indicator, “CR” for credit, “DR” for debit . 
Sub-Totals 
Sub-totals for the DIFFERENCE NET MONEY are provided for the following:  
• Sub-totals per MM/YYYY, TBA [[CUSIP]] and Pool;  
• Sub-totals per Report.  
  

---

## Page 103

MBSD Operational Pool Net Reports Guide 
POID Factor Update Report 103 
Print Image Report Sort Order 
1. Contractual [[settlement]] Month/Year = earliest to latest. 
2. TBA [[CUSIP]] = ascending order. 
3. Pool Number = ascending order. 
 
For POIDs trades: 
1. Contractual [[settlement]] Date = earliest to latest. 
2. Trade Number (ascending). 
 

---

## Page 104

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at:  
CoreLearning@[[DTCC]].com  
Or visit us on the web at:  
www.dtcclearning.com 