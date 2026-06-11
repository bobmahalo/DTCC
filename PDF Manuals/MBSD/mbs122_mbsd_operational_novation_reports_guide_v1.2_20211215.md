---
title: "MBSD Operational Novation Reports Guide v 1.2"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs122_mbsd_operational_novation_reports_guide_v1.2_20211215.pdf"
pages: 42
size: "495.0 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD Operational Novation Reports Guide v 1.2

**Original File:** [mbs122_mbsd_operational_novation_reports_guide_v1.2_20211215.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs122_mbsd_operational_novation_reports_guide_v1.2_20211215.pdf)  
**Category:** MBSD  
**Total Pages:** 42  
**File Size:** 495.0 KB  

---

## Page 1

MORTGAGE-BACKED [[securities]] 
(MBS) 
 
MBSD OPERATIONAL [[Novation]] REPORTS GUIDE 
VERSION 1.2 
DECEMBER 15, 2021 
  


---

## Page 2

Copyright © 2021 by The Depository Trust & Clearing Corporation (“[[DTCC]]”).  
This work (including, without limitation, all text, images, logos, compilation and design) is proprietary and protected by 
copyright and is for the exclusive use of users authorized by [[DTCC]]. If his work is received from [[DTCC]] in any electronic 
medium, autho rized users of this work are granted a limited, non- exclusive, non- transferable, non- sublicensable and freely 
revocable license to make reproductions and transmissions necessary for downloading and storage of this work on the 
users' computers and to print one or more paper copies from the electronic version for their own use. Other than to this 
limited extent, no part of this work (including any paper copies thereof or print versions thereof) may be printed, copied, 
altered, modified, posted, reproduced, di splayed, published, sold, licensed, used or distributed (including by transmission) 
in any form or by any means, or stored in any information stor age and retrieval system, without [[DTCC]]'s prior written 
permission.  
All product or service names are the prope rty of their respective owners.  
 
Doc Date: December 15, 2021 
Publication Code:  MBS122 
Service: [[FICC]] MBSD 
Title: MBSD Operational [[Novation]] Reports Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction..................................................................................................................................... 7 
MBS Nov atio n Repo rts .................................................................................................................... 7 
TBA Net Detail Report ...................................................................................................................... 8 
The TBA Net Detail Report Explained ................................................................................................ 8 
About the TBA Net Detail Repo rt....................................................................................................... 8 
Report Format .............................................................................................................................. 8 
Print Imag e Repo rt Layout............................................................................................................. 8 
Machine-Read ab le Output Fo rmat .................................................................................................. 8 
Tilde .......................................................................................................................................... 9 
Report Section  In forma tion ........................................................................................................... 10 
Account Header Information ........................................................................................................ 10 
TBA [[CUSIP]] Header Information ................................................................................................... 10 
Original SBOD Trades ................................................................................................................ 10 
Resulting SBON ........................................................................................................................ 11 
Sub-Totals ................................................................................................................................ 12 
Report Sort Order ........................................................................................................................ 12 
DNA Report ....................................................................................................................................13  
The DNA Report Explained ............................................................................................................ 13 
About the D NA Repo rt ................................................................................................................... 13 
Report Format ............................................................................................................................ 13 
Print Image Report Layout........................................................................................................... 13 
Machine-Read ab le Output Fo rmat ................................................................................................ 14 
Report Section  In forma tion ........................................................................................................... 14 
Account Header Information ........................................................................................................ 14 
D NA Head er Info rmatio n ............................................................................................................. 14 
D NA Trad e Ass ig nment D etails .................................................................................................... 15 
D NA Req uest Sub-Totals ............................................................................................................ 15 
D NA Req uest [[SEC]] tio n Sub-Totals.................................................................................................  16 

---

## Page 4

 
 
Report Sort Order ........................................................................................................................ 16 
TBA Trade Reprice and Variance Report ..........................................................................................17  
The TBA Trade Reprice and Variance Report Explained ..................................................................... 17 
About the TBA Trade Reprice and Variance Report ........................................................................... 17 
Report Format ............................................................................................................................ 17 
Print Image Report Layout........................................................................................................... 17 
Machine-Read ab le Output Fo rmat ................................................................................................ 17 
Report Section  In forma tion ........................................................................................................... 18 
Account Header Information ........................................................................................................ 18 
TBA [[CUSIP]] Header Information ................................................................................................... 18 
Repriced Trade Details ............................................................................................................... 18 
TBA [[CUSIP]] Sub-To t als............................................................................................................... 19 
Report Totals ............................................................................................................................ 19 
Sub-Totals ................................................................................................................................ 19 
Report Sort Order ........................................................................................................................ 20 
Expanded Pool Net Detail Report .....................................................................................................21  
The Expanded Pool Net Detail Report Explained ............................................................................... 21 
About the Expanded Pool Net Detail Report...................................................................................... 21 
Report Format ............................................................................................................................ 21 
Print Image Report Layout........................................................................................................... 22 
Machine-Read ab le Output Fo rmat ................................................................................................ 22 
Report Section  In forma tion ........................................................................................................... 22 
Account Header Information ........................................................................................................ 22 
TBA [[CUSIP]] Header Information ................................................................................................... 22 
Pool Details .............................................................................................................................. 23 
Pool Level (PID) Sub-To t als ........................................................................................................ 24 
Pool Netting (POID) Totals .......................................................................................................... 24 
Pool Number Netted Totals ......................................................................................................... 24 
Report Sort Order ........................................................................................................................ 25 
Expanded Pool Net Summary Report ...............................................................................................26  

---

## Page 5

 
 
The Expanded Pool Net Summary Report Explained.......................................................................... 26 
About the Expanded Pool Net Summary Report ................................................................................ 26 
Report Format ............................................................................................................................ 26 
Print Image Report Layout........................................................................................................... 26 
Machine-Read ab le Output Fo rmat ................................................................................................ 27 
Report Section  In forma tion ........................................................................................................... 27 
Account Header Information ........................................................................................................ 27 
TBA [[CUSIP]] Header Information ................................................................................................... 27 
Report Sort Order ........................................................................................................................ 28 
POID Factor Update Report .............................................................................................................29  
The POID Factor Update Report Explained ...................................................................................... 29 
About the POID Factor Update Report ............................................................................................. 29 
Report Format ............................................................................................................................ 29 
Print Imag e Repo rt Layout........................................................................................................... 29 
Machine-Read ab le Output Fo rmat ................................................................................................ 29 
Report Section  In forma tion ........................................................................................................... 30 
Account Header Information ........................................................................................................ 30 
Pool Header Information ............................................................................................................. 30 
POIDs ...................................................................................................................................... 30 
Sub-Totals ................................................................................................................................ 31 
Report Sort Order ........................................................................................................................ 31 
POID Conversion Report .................................................................................................................32  
The POID Conversion Report Explained .......................................................................................... 32 
About the POID Conversion Report .................................................................................................  32 
Report Format ............................................................................................................................ 32 
Print Image Report Layout........................................................................................................... 33 
Machine-Read ab le Output Fo rmat ................................................................................................ 33 
Report Section  In forma tion ........................................................................................................... 33 
Account Header Information ........................................................................................................ 33 
TBA [[CUSIP]] Header Information ................................................................................................... 33 

---

## Page 6

 
 
Original SPT Trades / PIDs ......................................................................................................... 34 
Generated POIDs ...................................................................................................................... 34 
Sub-Totals ................................................................................................................................ 35 
Report Sort Order ........................................................................................................................ 35 
Cash Trade POID Conversion Report ...............................................................................................37  
The Cash Trade POID Conversion Report Explained ......................................................................... 37 
About the Cash Trade POID Conversion Report ................................................................................ 37 
Report Format ............................................................................................................................ 37 
Print Image Report Layout........................................................................................................... 38 
Machine-Read ab le Output Fo rmat ................................................................................................ 38 
Report Section  In forma tion ........................................................................................................... 38 
Account Header Information ........................................................................................................ 38 
TBA [[CUSIP]] Header Information ................................................................................................... 38 
Original SPT Trades / PIDs ......................................................................................................... 39 
Generated POIDs ...................................................................................................................... 39 
Sub-Totals ................................................................................................................................ 40 
Report Sort Order ........................................................................................................................ 40 

---

## Page 7

Introduction 7 
INTRODUCTION 
The purpose of this guide is to explain the reports produced by the Mortgage-Backed [[securities]] Division of the 
Fixed Income Clearing Corporation pertaining to MBS [[Novation]] processing. 
MBS [[Novation]] Reports 
The MBSD has introduced eight new reports with the launch of MBS Operational [[Novation]]. This guide explains 
the purpose of each report, the formats in which it is available, the report headers and its data elements. 
Examples of each report may be viewed on the MBSD Operational [[Novation]] Reports page (with the MBS 
[[Novation]] Reports Explained tab open) in the [[DTCC]] Learning Center – a page created specifically to be used in 
tandem with this guide. Be sure to take advantage of this online resource to learn more about these eight 
reports.  
Review the table below for a summary of each MBS [[Novation]] processing-related report. 
MBS [[Novation]] Reports  
TBA Net Detail Report  Displays details about the TBA Net – including SBOD trades included in the TBA Netting 
process along with corresponding TBA TAP, and resulting SBON [[obligations]] versus [[FICC]]’s 
TBA account, FTBA at the system price. Replaced the legacy SBO Summary Report.  
DNA Report  Captures the DNA requests sent by members. This report allows members to track their 
DNA activity and reconcile money differences generated by the pair offs.  
TBA Trade Reprice and 
Variance Report  
Captures the TBA trade reprice activity occurring on SIFMA 24-hour  day. This report allows 
members to reconcile this reprice activity and any associated money differences. In addition, 
this report prov ides details on variance par associated with each trade, due to allocations 
processed in the daily or expanded pool net cycles and the resulting variance TAP.  
Expanded Pool Net 
Detail Report  
Reflects the detailed results of the expanded pool netting cycle on SIFMA 24-hour day  and 
includes the resulting Expanded Pool Net TAP (EXP) generated .  
Expanded Pool Net 
Summary Report  
Reflects the summary results of expanded  pool netting cycle on SIFMA 24-hour day and 
includes the resulting Expanded Pool Net TAP (EXP) generated . 
POID Factor Update 
Report  
Captures cash differences due to factor updates f or POIDs that already settled and have 
CSD in blackout period. This report allow s members to reconcile the money differences 
based on the factor updates.  
POID Conversion Repor t Reflects SPT trade and allocations (STIP and generic TBA) converted to PO IDs at trade 
price on the current business day.  
Cash Trade PO [[ID]] 
Conversion Report  
Provides details on cash trades (SPT and allocations) converted to PO IDs on a real-time 
basis. 
 
Additional training regarding specific MBS processing can be found in their respective sections of the [[DTCC]] 
Learning Center (www.dtcclearning.com). 

---

## Page 8

MBSD Operational [[Novation]] Reports GuIde  
 
TBA Net D etail Report 8 
TBA NET DETAIL REPORT 
The TBA Net Detail Report Explained 
To see an example of the TBA Net Detail Report while you learn about its use, available formats, layout, 
header information and sort order, please visit the MBSD Operational [[Novation]] Reports page (with the MBS 
[[Novation]] Reports Explained tab open) on the [[DTCC]] Learning Center. It may be helpful to have it open while 
reading this guide as it will allow you to view actual reports in full size and interact with them to learn more. 
Note: you will need to be logged into the Learning Center to view this content. 
About the TBA Net Detail Report 
The TBA Net Detail Report is produced on 72-hour day as prescribed by the SIFMA Calendar and reflects 
results of TBA Net, which includes SBOD trades into the net, associated TBA TAP and resulting SBON 
[[obligations]] versus FTBA at system price.  To learn more about the timeframes of the processes relevant to this 
report, please refer to the MBSD Processing Schedule & Timeframes document which may be found in the 
[[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com. 
This report allows members to view the [[settlement]] Balance Order Destined (SBOD) that were designated for 
TBA netting and the final net TBA [[settlement]] [[obligations]] designated as [[settlement]] Balance Order (SBON) 
positions. 
Report Format  
The TBA Net Detail Report is produced in three formats: 
• Print Image format available in MBS Clearing Report Center on the MBS Web Front End; 
• Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report 
• Tilde-delimited file format for members to use to upload report information in Excel spreadsheets or other 
software to perform custom analytics on report data. 
Print Image Report Layout 
This report details the SBOD trades considered in the TBA Net, and resulting SBON [[obligations]], grouped by 
[[settlement]] month/year and TBA [[CUSIP]]. Within each section, the original SBOD trade are listed, followed by 
resulting SBONs. 
Machine-Readable Output Format 
This report is also available in MRO format. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation.   

---

## Page 9

MBSD Operational [[Novation]] Reports GuIde  
 
TBA Net D etail Report 9 
Tilde 
Tilde Delimited Reports are also available via Report Center (right next to the Print Image (.pdf) reports). Tilde 
Delimited Reports may be downloaded into Excel (or a similar program) to allow their data to be manipulated, 
similarly to .CSV (Comma Separated Value) files. When downloaded, header field information is not retained. 
The tilde-separated file is based on the MRO equivalent, where each row in the tilde contains data from various 
card codes and therefore has been updated to confirm to the MRO changes.   
Each tilde-separate file begins with a “header” row followed by “detail” rows containing information from card 
code 02 (trade SBOD detail) or 03 (obligation SBON detail), as summarized in the table below.   
 
Field Type Comment Populated for Card Code?  
Card Code  2 N 02 (trade detail), 03 (obligation record)  02 03 
[[settlement]] Year 4 N  Format YYYY   
[[settlement]] Month  2 A/N  Format MM   
TBA [[CUSIP]]  9 A/N     
Account Symbol   4 A/N     
Trade Number   10 N     
Internal XREF/ Trade #  15 A/N     
Trade Type  4 A/N  SBOD, SBON   
Buy/Sell Indicator   1 A/N  B = Buy, S = Sell    
[[settlement]] Date  8 A/N  Format YYYYMMDD, where DD is “00” for 
“02” card codes  
  
Contra Account  4 A/N     
Par Value 13 N  Format 11.2   
Trade Price 15 N  In decimal, format 3.12   
Trade Money  13 N  Format 11.2   
[[settlement]] Price 15 N  In decimal, format 3.12   
[[settlement]] Money  13 N  Format 11.2   
TBA TAP 13 N  Format 11.2   
TBA TAP CR/DR  1 A TBA TAP indicator (C=Credit, D=Debit)    
  

---

## Page 10

MBSD Operational [[Novation]] Reports GuIde  
 
TBA Net D etail Report 10 
Report Section Information 
Within each section, the individual TBA net details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
[[participant]] [[ID]]/Aggregate [[ID]]  A three -digit number is assigned to each [[Member]] followed 
by a 2-digit number or alphanumeric identifier  
Account Description  The account name 
Account [[ID]] The four -character account symbol  
Business Date A date field showing the current business date 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD EXPLANATION 
[[settlement]] Month/Year  [[settlement]] month and year  
TBA [[CUSIP]] Nine-digit alphanumeric To Be Announced [[CUSIP]]  
SECURITY CLASS Description of this TBA [[CUSIP]]  
[[settlement]] Price System price associated with this TBA [[CUSIP]], which is 
equal to prior -day [[EOD]] price 
Original SBOD Trades 
Displays information on each SBOD. 
FIELD EXPLANATION 
TRADE NBR Trade number on SBOD trade 
TRADE XREF XREF on SBOD trade 
TYPE Always equal to “SBOD”  
B/S B or S (Buy or Sell)  
S/D Contract ual [[settlement]] Date, which for SBOD has “00” as 
day 

---

## Page 11

MBSD Operational [[Novation]] Reports GuIde  
 
TBA Net D etail Report 11 
FIELD EXPLANATION 
CONTRA Contra on the trade, equal to [[FICC]]’s TBA [[Novation]] 
Account (FTBA)  
PAR Par of the SBOD Trade  
TRADE PRICE Price, exclusive of commission  
TRADE MONEY [[settlement]] Amount, based on trade price 
STTL PRICE [[settlement]] price for this TBA [[CUSIP]]  
STTL MONEY [[settlement]] Amount, based on STTL PRICE  
TBA TAP Transaction Adjustment Payment (TAP) associated with 
this SBOD trade  
CR/DR Indicator  “CR” for credit, “DR” for debit for TBA TAP  
Resulting SBON 
Displays information on each SBON created. 
FIELD EXPLANATION 
TRADE NBR Trade number on SBON obligation  
TYPE Always equal to “SBON”  
B/S B or S (Buy or Sell)  
S/D Contract ual [[settlement]] Date 
CONTRA Contra on the trade, equal to [[FICC]]’s TBA [[Novation]] 
Account (FTBA)  
PAR Par of the SBON Trade  
STTL PRICE [[settlement]] price on this SBON  
STTL MONEY [[settlement]] Amount based on the SBON’s STTL RPICE  
 
  

---

## Page 12

MBSD Operational [[Novation]] Reports GuIde  
 
TBA Net D etail Report 12 
Sub-Totals 
Sub-totals are provided for the following: 
• Net Sub-totals per MM/YYYY, TBA [[CUSIP]] and SBOD, where: 
o Long Par = Total PAR of all buy trades 
o Long Money = Total TRADE MONEY of all buy trades 
o Short Par = Total PAR of all sell trades 
o Short Money = Total TRADE MONEY of all sell trades 
o Net Long/Short = Sum of “Long Par” + “Short Par”, signed with “-“ if short 
o Net Trade Money = Sum of “Long Money” + “Short Money”, signed with “-“ if  <$0 
o Total TAP = Net total of TBA TAP of all buy and sell trades, signed with “-“ if <$0 
• Net Sub-totals per MM/YYYY, TBA [[CUSIP]] and SBON, where: 
o Long Par = Total PAR of all buy SBON 
o Long Money = Total STTL MONEY of all buy SBON 
o Short Par = Total PAR of all sell SBON 
o Short Money = Total STTL MONEY of all sell SBON 
o Net Long/Short = Sum of “Long Par” + “Short Par”, signed with “-“ if short 
o Net Sttl Money = Sum of “Long Money” + “Short Money”, signed with “-“ is <$0 
Report Sort Order 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]] = ascending order  
For SBOD/SBON trades: 
1. Trade Number (ascending) 
  

---

## Page 13

MBSD Operational Nov ation Reports GuIde 
 
DNA Report 13 
DNA REPORT 
The DNA Report Explained 
To see an example of the DNA Report while you learn about its use, available formats, layout, header 
information and sort order, please visit the MBSD Operational [[Novation]] Reports page (with the MBS [[Novation]] 
Reports Explained tab open) on the [[DTCC]] Learning Center. It may be helpful to have it open while reading this 
guide as it will allow you to view actual reports in full size and interact with them to learn more. Note: you will 
need to be logged into the Learning Center to view this content. 
About the DNA Report 
The DNA Report is produced once daily to allow dealers to track their DNA activity and reconcile [[settlement]] 
value money differences generated by pair-offs.  To learn more about the timeframes of the processes relevant 
to this report, please refer to the MBSD Processing Schedule & Timeframes document which may be found in 
the [[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com. 
This report shows all DNA requests active in the system or processed/cancelled on the current business day.  
For each DNA request, the report shows the DNA status, the individual trades that [[FICC]] assigned to the DNA 
request to
1 and any associated money differences (DNA TAP). 
Although this report is produced daily, it will only have data during SIFMA 48hr/24hr, as that is the only period 
in which DNA may be submitted/processed. 
Report Format  
The DNA Report is produced in two formats: 
• Print Image format available in MBS Clearing Report Center on the MBS Web Front End; 
• Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report 
Print Image Report Layout 
The report is divided into 3 sections based on DNA request status: 
 
 
1 DNA requests may be submitted by members based on “terms-only”, in which case [[FICC]] will select specific 
buy and sell trades to which to assign the DNA request. Members may also provide specific Trade IDs to target 
(“Trade [[ID]] mode”). 

---

## Page 14

MBSD Operational [[Novation]] Reports GuIde  
 
DNA Report 14 
• Assigned DNA – DNA request has been assigned to specific TBA trades by [[FICC]] and associated 
position excluded from allocation.  However, CSD has not been reached and therefore, DNA is pending 
and may still be canceled.  Assigned DNA requests will appear in this report until they are settled2 or 
canceled by the [[Member]]. 
• Settled DNA – DNA request has been processed and associated TBA position is marked as settled.  In 
addition, DNA TAP (at the aggregate level) has been generated for any price differences.  This is a final 
state for this DNA and it will no longer appear in subsequent reports. 
• Canceled DNA – DNA request has been canceled by [[Member]] and the associated TBA position reopened 
for allocation.  This is a final state for this DNA and it will no longer appear in subsequent reports 
Machine-Readable Output Format 
This report is also available in MRO format. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation.  
Report Section Information 
Within each section, the individual DNA requests are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
[[participant]]/Aggregate  A three -digit number is assigned to each [[Member]]  followed 
by a 2-digit number or alphanumeric identifier  
Account Description  The account name 
Account [[ID]] The four -character account symbol  
Business Date A date field showing the current business date 
DNA Header Information 
Displays information on the DNA request; 1 per DNA request. 
FIELD EXPLANATION 
S/D A date field showing the Contractual S ettlement date 
TBA [[CUSIP]] The TBA [[CUSIP]] on the DNA request  
SECURITY CLASS An alphanumeric description of the TBA [[CUSIP]]  
 
2 DNA requests are processed during the “DNA [[settlement]]/TBA Reprice” process executed on SIFMA 24hr. 

---

## Page 15

MBSD Operational [[Novation]] Reports GuIde  
 
DNA Report 15 
FIELD EXPLANATION 
DNA# DNA identifier assigned by system to this request  
DNA REF DNA reference assigned by [[Member]] to this request  
DNA PAR Par-amount assigned to this DNA request  
DNA Trade Assignment Details 
Displays information on each trade assigned to the DNA request.  
FIELD EXPLANATION 
TRD # The Trade [[ID]] number 
TRD TYP Trade Type – TFTD or SBON 
B/S BUY or SELL 
T/D Trade Date 
S/D Contract ual [[settlement]] Date 
PRICE Trade price 
ORIG TRD PAR Original trade par  
DNA PAR Amount of par targeted for DNA  
DNA STTL VALUE [[settlement]] value of DNA’ed par based on price 
DNA Request Sub-Totals 
Displays sub-total information for each DNA request; 1 per DNA request. 
FIELD EXPLANATION 
DNA TAP Within a DNA request, sum of all SELL “DNA STTL 
VALUE” minus sum of all BUY “DNA STTL VALUE”.  In 
other words, sell [[settlement]] values are positive, and buy 
[[settlement]] values are negative.  
 
  

---

## Page 16

MBSD Operational [[Novation]] Reports GuIde  
 
DNA Report 16 
DNA Request Section Sub-Totals 
Displays sub-total information for each report section (assigned, settled, canceled); 3 per report.  
FIELD EXPLANATION 
TOTAL DNA TAP Sum of all “DNA TAP” within report section  
Report Sort Order 
Report Section order 
1. Assigned DNA 
2. Settled DNA 
3. Canceled DNA 
DNA Request order within report section (assigned, settled, canceled)  
1. S/D 
2. TBA [[CUSIP]] 
3. DNA# 
Trade order within DNA request  
1. Buy 
2. Sell 
3. Trade [[ID]]  
 

---

## Page 17

MBSD Operational [[Novation]] Reports GuIde  
 
TBA Trade Reprice and Varianc e Report 17 
TBA TRADE REPRICE AND VARIANCE REPORT 
The TBA Trade Reprice and Variance Report Explained 
To see an example of the TBA Trade Reprice and Variance Report while you learn about its use, available 
formats, layout, header information and sort order, please visit the MBSD Operational [[Novation]] Reports page 
(with the MBS [[Novation]] Reports Explained tab open) on the [[DTCC]] Learning Center. It may be helpful to have 
it open while reading this guide as it will allow you to view actual reports in full size and interact with them to 
learn more. Note: you will need to be logged into the Learning Center to view this content. 
About the TBA Trade Reprice and Variance Report 
The TBA Trade Reprice and Variance Report, produced on 24-hour Day as prescribed by the SIFMA Calendar, 
provides dealers with details on all TBA trades that were repriced on the current business day, meaning that 
they were settled and replacement trades were generated at the system price.  Both original and replacement 
trade information is provided, along with reprice TAP due to price differences, allowing members to reconcile 
these [[settlement]] value differences. To learn more about the timeframes of the processes relevant to this 
report, please refer to the MBSD Processing Schedule & Timeframes document which may be found in the 
[[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com. 
In addition, this report provides details on variance par associated with each trade, due to allocations 
processed in the daily or expanded pool net cycles.  Trade and variance par details are provided along with 
corresponding variance TAP due to price differences. 
Report Format  
The TBA Trade Reprice and Variance Report is produced in two formats: 
• Print Image format available in MBS Clearing Report Center on the MBS Web Front End; 
• Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report 
Print Image Report Layout 
This report details the trades repriced on the current business day, grouped by [[settlement]] month/year and TBA 
[[CUSIP]]. 
Machine-Readable Output Format 
This report is also available in MRO format. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. 
 

---

## Page 18

MBSD Operational [[Novation]] Reports GuIde  
 
TBA Trade Reprice and Varianc e Report 18 
Report Section Information 
Within each section, the individual TBA Trade Reprice and Variance details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
[[participant]]/Aggregate  A three -digit number is assigned to each [[Member]]  followed 
by a 2-digit number or alphanumeric identifier  
Account Description  The account name 
Account [[ID]] The four- character account symbol   
Business Date A date field showing the current business date 
TBA [[CUSIP]] Header Information 
Displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] included in this 
report. 
FIELD EXPLANATION 
[[settlement]] Month/Year  [[settlement]] month and year  
TBA [[CUSIP]] 9-character To Be Announced [[CUSIP]]  
SECURITY CLASS Description of this TBA [[CUSIP]]  
RPC/SYSTEM PRICE Price on new trade  
Repriced Trade Details 
Displays information on each repriced trade; 1 per trade. 
FIELD EXPLANATION 
ORIG TRD # Trade number on original trade 
XREF [[Member]] XREF 
B/S BUY or SELL 
TRD TYPE Trade Type – SBON or TFTD  
S/D Contract ual [[settlement]] Date 
T/D Trade Date 
PRICE Price on original trade  

---

## Page 19

MBSD Operational [[Novation]] Reports GuIde  
 
TBA Trade Reprice and Varianc e Report 19 
FIELD EXPLANATION 
RPC PAR Amount of par subject to repricing, i.e. open par on trade  
VAR PAR Amount of par subject variance calculation, i.e. sum  of all 
variance calculated for indiv idual allocations and assigned 
to this trade  
OPN STL VAL [[settlement]] value of RPC PAR based on PRICE  
VAR STL VAL [[settlement]] value of VAR PAR based on PRICE  
RPC STL VAL New [[settlement]] value of RPC PAR based on 
RPC/SYSTEM, calculated as:  
RPC STL VAL = OPN STL VAL + RPC TAP 
RPC VAR STL VAL [[settlement]] value of VAR PAR based on RPC/SYSTEM 
PRICE, calculated as:  
RPC VAR STL VAL = VAR STL VAL + VAR TAP 
RPC TAP TAP associated with the repriced trade due to price 
differences  
VAR TAP TAP associated with price difference of the TBA Obligation 
and the current face of the pools allocated in satisfaction of 
the obligation  
RPC TRD [[ID]] Trade number of new repriced trade 
TBA [[CUSIP]] Sub-Totals 
Displays sub-total information for each TBA [[CUSIP]] grouping. 
FIELD EXPLANATION 
RPC TAP Sum of all “RPC TAP” within this TBA [[CUSIP]] grouping  
VAR TAP Sum of all “VAR TAP” within this TBA [[CUSIP]] grouping  
Report Totals 
Displays sub-total information for report; 1 per report.  
FIELD EXPLANATION 
Total TAP Sum of all “RPC TAP” within report  
Sum of all “VAR TAP” within report  
Sub-Totals 
• Total RPC TAP per TBA [[CUSIP]] and per REPORT 
• Total VAR TAP per TBA [[CUSIP]] and per REPORT 

---

## Page 20

MBSD Operational [[Novation]] Reports GuIde  
 
TBA Trade Reprice and Varianc e Report 20 
Report Sort Order 
1. [[settlement]] Month/Year 
2. TBA [[CUSIP]] 
3. Trade Type (SBON, TFTD) 
4. Trade [[ID]]  

---

## Page 21

MBSD Operational [[Novation]] Report s GuIde 
 
Expanded Pool N et Detail Report 21 
EXPANDED POOL NET DETAIL REPORT 
The Expanded Pool Net Detail Report Explained 
To see an example of the Expanded Pool Net Detail Report while you learn about its use, available formats, 
layout, header information and sort order, please visit the MBSD Operational [[Novation]] Reports page (with the 
MBS [[Novation]] Reports Explained tab open) on the [[DTCC]] Learning Center. It may be helpful to have it open 
while reading this guide as it will allow you to view actual reports in full size and interact with them to learn 
more. Note: you will need to be logged into the Learning Center to view this content. 
About the Expanded Pool Net Detail Report 
The Expanded Pool Net Detail Report is produced on 24-hour Day as prescribed by the SIFMA Calendar and 
provides detailed results of Expanded Pool Net, which includes all allocations (PIDs) with delivery date >= next 
business day, associated cash differential and resulting POIDs versus [[FICC]] at syste m price . To learn more 
about the timeframes of the processes relevant to this report, please refer to the MBSD Processing Schedule & 
Timeframes document which may be found in the [[participant]] Reference Documentation (MBS) section on 
www.[[DTCC]].com. 
The Expanded Pool Net Detail Report reflects all Pool Instructs that have been included in the Expanded Pool 
Netting cycle. The report is separated into three sections: 
• The PID section – a listing of all Pool Instructs that have gone into the Expanded Pool Net identified by the 
Pool IDs (PIDs) assigned by [[FICC]] and the XREFs assigned by the members; 
• The POID section – a listing of the net Pool [[obligations]] stemming from the Expanded Pool Netting 
process identified by their Pool Obligation IDs (POIDs); and 
• A Recap section – showing netting results across all pools eligible for the current netting cycle.  
 
The Expanded Pool Net Transaction Adjustment Payments (EXP TAPs) are also provided on this report. 
Provisions for reporting Fail Mark have been made to this report, but will be implemented as part of planned, 
future CCP enhancements. 
Report Format  
The Expanded Pool Net Detail Report is produced in two formats: 
• Print Image format available in MBS Pool Net Report Center on the MBS Web Front End; 
• Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report. 
  

---

## Page 22

MBSD Operational [[Novation]] Reports GuIde  
 
Expanded Pool N et Detail Report 22 
Print Image Report Layout  
The Expanded Pool Netting Detail Report has a high-level sort order as follows: TBA [[CUSIP]] (report reflects 
sub-totals at the TBA [[CUSIP]] level); Pool Number; Pool [[CUSIP]] Number. 
Machine-Readable Output Format 
This report is also available in MRO format. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation.  
Report Section Information 
Within each section, the individual Expanded Pool Net details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three-
digit  [[participant]] [[ID]] assigned to each [[Member]] (followed by) 
the two -character alphanumeric aggregate  
PART [[ID]] The four character account symbol  
[DATE OF REPORT] The date the report was created. 
PRODUCT Product Code Description. This is MBS for Mortgage -
Backed Security.  
TBA [[CUSIP]] Header Information 
Displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] included in this 
report. 
FIELD EXPLANATION 
TBA [[CUSIP]] The nine -character TBA [[CUSIP]] 
POOL NUMBER The pool number allocated to the TBA trade that will be 
settled for the trade  
POOL [[CUSIP]] Pool [[CUSIP]] Number 
STTL PRICE [[settlement]] Price: Current day Pool Net price ( system p r i c e) 
 
  

---

## Page 23

MBSD Operational [[Novation]] Reports GuIde  
 
Expanded Pool N et Detail Report 23 
Pool Details 
Displays information most relevant to events taking place during the Pool Netting phase of the trade life cycle.  
FIELD EXPLANATION 
S/D [[settlement]] Date: The contractual [[settlement]] date of the 
TBA trade 
D/D Delivery Date: The date that the pools submitted on the 
Pool Instructs are scheduled to be delivered in satisfaction 
of the TBA trade  
PID Pool [[ID]]: Transaction [[ID]] assigned to each indiv idual Pool 
Instruct by Pool Netting. As such, each P [[ID]] represents a 
Pool Instruct. PIDs appear in the top half, or "P [[ID]] section" 
of the Expanded Pool Net Detail Report.  
POID Pool Obligation [[ID]] : Identifier assigned to pool [[obligations]] 
vs. [[FICC]]. Each PO [[ID]] therefore represents the [[Member]]'s 
obligation to received or deliver [[securities]] versus payment 
with [[FICC]]. POIDs appear in the bottom half, or "PO [[ID]] 
section" of the Expanded Pool Net Detail Report.  
CONTRA Contra on the trade, equal to [[FICC]]’s [[settlement]] Account 
([[FICC]]) under the “PO [[ID]] section”.  
B/S BUY/SELL: Ind icates whether the trade is a "buy" or a 
"sell" from the [[Member]]'s perspective.  
XREF The XREF is assigned by the [[Member]] – it's alphanumeric, 
extending from 1 to 16 characters in length. It must be 
unique to that [[Member]] – the [[Member]] cannot have any 
other trades in the system with that same XREF.  
LONG ORIG FACE Long Original Face:  Original Face of  netting eligible buy 
pool instructs.  
LONG CURR. FACE  Long Current Face: Current Face of netting eligible buy 
pool instructs.  
SHORT ORIG FACE Short Original Face: Original Face of netting eligible sell 
pool instructs.  
SHORT CURR. FACE Short Current Face: Current Face of netting eligible sell 
pool instructs.  
DEBIT NET MONEY Debit [[settlement]] Proceeds. The Net Money of netting 
eligible buy pool i nstructs. 
CREDIT NET MONEY  Credit [[settlement]] Proceeds. The Net Money of netting 
eligible sell pool instructs.  
 

---

## Page 24

MBSD Operational [[Novation]] Reports GuIde  
 
Expanded Pool N et Detail Report 24 
Pool Level (PID) Sub-Totals 
Displays pool level sub-totals. 
FIELD EXPLANATION 
TOTAL [B/S] This is the sum of the Total Long & Short Positions 
(displayed as Original Face and Current Face) of all netting 
eligible Pool Instructs.  
NET FAIL Net Fail Position: Reserved for future use.  
NET NET Final Net Position (long or shor t) displayed as Original 
Face and Current Face of all netting eligible Pool Instructs.
 
Pool Netting (POID) Totals 
All a [[Member]]'s receive and deliver [[obligations]] established by Pool Netting are shown totaled, including Pool 
Transaction Adjustment Payments ("Pool TAPs") that provides overall position buy and sell totals.  
FIELD EXPLANATION 
TOTAL [B/S] This is the sum of the Total Long & Short Positions 
(displayed as Original Face and Current Face) of all netting 
eligible Pool Instructs.  
TRADE ADJUSTMENT PAYMENT (TAP)  [[FICC]]-generated funds adjustment ensuring [[participant]]'s 
original Net Money achieved.  
FAIL MARK Reserved for future use.  
NET Net of Transaction Adjustment Payment (TAP) and Fail 
Mark (when applicable).  
Pool Number Netted Totals 
FIELD EXPLANATION 
DELIVERY DATE Projected date of clearance 
LONG VS [[FICC]] (ORIG. FACE)  Original face of receive(s) versus [[FICC]] generated via 
expanded pool netting  
LONG VS [[FICC]] (CURR. FACE)  Current face of receive(s) versus [[FICC]] generated via 
expanded pool netting  
[[FICC]] RVP NET MONEY Total Net Money of participants receives vs. payment 
(longs)  against the [[FICC]] 
SHORT VS. [[FICC]] (ORIG. FACE)  Original face of deliveries versus [[FICC]] generated via 
expanded pool netting  
SHORT VS. [[FICC]] (CURR. FACE)  Current face of deliveries versus [[FICC]] generated via 
expanded pool netting  

---

## Page 25

MBSD Ope rational [[Novation]] Reports GuIde 
 
Expanded Pool N et Detail Report 25 
FIELD EXPLANATION 
[[FICC]] DVP NET MONEY Total net money of participants deliveries vs. payment 
(shorts) against the [[FICC]]  
[[FICC]] NET LONG/SHORT (ORIG. FACE)  Total long/short original face versus [[FICC]]  
[[FICC]] NET LONG/SHORT (CURR. FACE)  Total long/shor t current face versus [[FICC]] 
[[FICC]] NET NET MONEY  Total Final Net Money  (debit or credit ) of all Pool 
[[obligations]] . 
TOTAL TRANSACTION ADJUSTMENT PAYMENT 
(“TAP”) 
[[FICC]]-generated funds adjustment (TAP) ensuring 
[[participant]]’s original net money achieved 
Report Sort Order 
1. [[settlement]] Month/Year 
2. TBA [[CUSIP]] 

---

## Page 26

MBSD Operational [[Novation]] Reports GuIde  
 
Expanded Pool N et Summary Report 26 
EXPANDED POOL NET SUMMARY REPORT 
The Expanded Pool Net Summary Report Explained 
To see an example of the Expanded Pool Net Summary Report while you learn about its use, available 
formats, layout, header information and sort order, please visit the MBSD Operational [[Novation]] Reports page 
(with the MBS [[Novation]] Reports Explained tab open) on the [[DTCC]] Learning Center. It may be helpful to have 
it open while reading this guide as it will allow you to view actual reports in full size and interact with them to 
learn more. Note: you will need to be logged into the Learning Center to view this content. 
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
• Print Image format available in MBS Pool Net Report Center on the MBS Web Front End; 
• Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report 
Print Image Report Layout 
The Expanded Pool Netting Summary Report has a high-level sort order as follows: TBA [[CUSIP]] (report reflects 
sub-totals at the TBA [[CUSIP]] level); Pool Number; Pool [[CUSIP]] Number. 
  

---

## Page 27

MBSD Operational [[Novation]] Reports GuIde  
 
Expanded Pool N et Summary Report 27 
Machine-Readable Output Format 
This report is also available in MRO format. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation.  
Report Section Information 
Within each section, the individual Expanded Pool Net Summary details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
PART AGG [[participant]] [[ID]] (followed by) Aggregate Number: The three-
digit  [[participant]] [[ID]] assigned to each [[Member]] (followed by) 
the two -character alphanumeric aggregate  
ACCT NAME The name of the account  
PART [[ID]] The four-character account symbol  
PRODUCT Product Code Description. This is MBS for Mortgaged-
Backed Security.  
TBA [[CUSIP]] Header Information 
Displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] included in this 
report. 
FIELD EXPLANATION 
TBA [[CUSIP]] The nine -character TBA [[CUSIP]] of reported pool  
POOL NUMBER The pool number allocated to the TBA trade that will be 
settled for the trade  
POOL [[CUSIP]] Pool [[CUSIP]] Number 
DELIVERY DATE The delivery date of the pool number. A pool number can 
have more than one delivery date.  
LONG VS. [[FICC]] (ORIG. FACE) Total long position of all netting eligible buy pool instructs 
reported as Original Face 
LONG VS. [[FICC]] (CURR. FACE)  Total long position of all netting eligible buy pool instructs 
reported as Current Face 
[[FICC]] RVP NET MONEY Total Net Mon ey of reported long position  
SHORT VS. [[FICC]] (ORIG. FACE)  Total [[short position]] of all netting eligible sell pool instructs 
reported as Original Face 

---

## Page 28

MBSD Operational [[Novation]] Reports GuIde  
 
Expanded Pool N et Summary Report 28 
FIELD EXPLANATION 
SHORT VS. [[FICC]] (CURR. FACE)  Total [[short position]] of all netting eligible sell pool instructs 
reported as Current Face 
[[FICC]] DVP NET MONEY Total Net Money of reported [[short position]]  
[[FICC]] NET LONG/SHORT (ORIG. FACE)  Net of total long & short positions repor ted as Original Face  
[[FICC]] NET LONG/SHORT (CURR. FACE)  Net of total long & short positions re ported as Current Face 
[[FICC]] NET NET MONEY  Net of net monies/reported long and shor t positions  
TOTAL TRADE ADJUSTMENT PAYMENT (TAP)  [[FICC]]-generated funds adjustment ensuring [[participant]]’s 
original Net Money achieved.  Will show as “EXP” on Cash 
[[settlement]] Detail Report.  
Report Sort Order 
1. [[settlement]] Month/Year 
2. TBA [[CUSIP]] 

---

## Page 29

MBSD Operational [[Novation]] Reports GuIde  
 
POID Factor Update Report 29 
POID FACTOR UPDATE REPORT 
The POID Factor Update Report Explained 
To see an example of the POID Factor Update Report while you learn about its use, available formats, layout, 
header information and sort order, please visit the MBSD Operational [[Novation]] Reports page (with the MBS 
[[Novation]] Reports Explained tab open) on the [[DTCC]] Learning Center. It may be helpful to have it open while 
reading this guide as it will allow you to view actual reports in full size and interact with them to learn more. 
Note: you will need to be logged into the Learning Center to view this content. 
About the POID Factor Update Report 
The POID Factor Update Report is a daily, end-of-day report and captures cash differences due to factor 
updates for POIDs that already settled and have CSD in blackout period. To learn more about the timeframes 
of the processes relevant to this report, please refer to the MBSD Processing Schedule & Timeframes 
document which may be found in the [[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com. 
This report allows members to reconcile the money differences based on the factor updates. The report reflects 
all settled POIDs that incurred [[settlement]] value differences due to factor update.   
Report Format  
The POID Factor Update Report is produced in two formats: 
• Print Image format available in MBS Pool Net Report Center on the MBS Web Front End; 
• Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report. 
Print Image Report Layout 
This report details all POIDs with [[settlement]] value differences due to factor update processed on the current 
business day, grouped by [[settlement]] month/year, TBA [[CUSIP]] and pool number/[[CUSIP]].  The report provides 
the following information. 
Machine-Readable Output Format 
This report is also available in MRO format. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation.  
  

---

## Page 30

MBSD Operational [[Novation]] Reports GuIde  
 
POID Factor Update Report 30 
Report Section Information 
Within each section, the individual POID Factor Update details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report 
FIELD EXPLANATION 
[[participant]]/Aggregate  A three-digit  number is assigned to each [[Member]] followed 
by a 2-digit number or alphanumeric identifier  
Account Description  The account name 
Account [[ID]] The four -character account symbol  
Business Date A date field showing the current business date 
Pool Header Information 
Within each section, displays information on pool of current grouping; 1 per pool [[CUSIP]] included in this report. 
FIELD EXPLANATION 
[[settlement]] Month/Year  Contract ual [[settlement]] month and year  
TBA [[CUSIP]] 9-character To Be Announced [[CUSIP]]        
Pool Number Pool number       
Pool [[CUSIP]] Pool [[CUSIP]]     
[[settlement]] Factor  Assumed factor for [[settlement]] Month/Year for this pool, 
which was in effect when this POID settled     
Updated Factor  Updated factor for [[settlement]] Month/Year for this pool  
POIDs  
Displays information on each POID that was updated due to a factor update 
FIELD EXPLANATION 
POID NBR POID identifier  
B/S B or S (Buy or Sell) 
D/D Delivery Date on PO [[ID]], which is also the date this PO [[ID]] 
settled  
S/D Contract ual [[settlement]] Date 

---

## Page 31

MBSD Operational [[Novation]] Reports GuIde  
 
POID Factor Update Report 31 
FIELD EXPLANATION 
CONTRA Contra on the trade, equal F SPT for SPT trades, FSTI for 
STIP trades and [[FICC]] for TFTD/TBA and SBON 
[[obligations]]  
STTL PRICE [[settlement]] price on the PO [[ID]] 
ORIG FACE Original face on the PO [[ID]] 
STTL CURR FACE Current face on the PO [[ID]] based on [[settlement]] Factor  
STTL NET MONEY Net money ([[settlement]] value) on the PO [[ID]], based on 
[[settlement]] Factor  
UPD CURR FACE  Current face on the PO [[ID]] based on Updated Factor  
UPD NET MONEY Net money ([[settlement]] value) on the PO [[ID]], based on 
Updated Factor  
DIFFERENCE NET MONEY  Difference in [[settlement]] and updated net money . 
CR/DR Indicator  Difference Net Money indicator, “CR” for credit, “DR” for 
debit 
Sub-Totals 
Sub-totals for the DIFFERENCE NET MONEY are provided for the following:  
• Sub-totals per MM/YYYY, TBA [[CUSIP]] and Pool  
• Sub-totals per Report  
Report Sort Order 
1. Contractual [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]] = ascending order 
3. Pool Number = ascending order 
For POIDs trades: 
1. Contractual [[settlement]] Date = earliest to latest 
2. Trade Number (ascending) 
  

---

## Page 32

MBSD Operational [[Novation]] Reports GuIde  
 
POID Conv ersion R eport 32 
POID CONVERSION REPORT 
The POID Conversion Report Explained 
To see an example of the POID Conversion Report while you learn about its use, available formats, layout, 
header information and sort order, please visit the MBSD Operational [[Novation]] Reports page (with the MBS 
[[Novation]] Reports Explained tab open) on the [[DTCC]] Learning Center. It may be helpful to have it open while 
reading this guide as it will allow you to view actual reports in full size and interact with them to learn more. 
Note: you will need to be logged into the Learning Center to view this content. 
About the POID Conversion Report 
The POID Conversion Report is produced once daily after the DNA, TBA Reprice and Conversion process and 
reflects the following SPT trade and allocations converted to POIDs at trade price on the current business day:  
• SPT Trade: SPT trade with CSD=NBD result in POIDs vs FSPT at trade price 
• STIP PID: PID targeting STIP with DD=NBD result in POIDs vs FSTI at trade price 
• Generic PID: PID targeting novated TFTD/TBA or SBON with DD=NBD that missed the daily Pool Net 
cycle 3 result in POIDs vs [[FICC]] at trade price. Note this is only applicable to PIDs with non-SIFMA CSD, 
as PIDs targeting SIFMA CSD will be processed in the Expanded Pool Net cycle. 
Note:  
SPT trades submitted after the conversion job is run that have CSD=NBD, will be converted at [[EOD]] and reflected in the 
Cash Trade POID Conversion output.  
To learn more about the timeframes of the processes relevant to this report, please refer to the MBSD 
Processing Schedule & Timeframes document which may be found in the [[participant]] Reference 
Documentation (MBS) section on www.[[DTCC]].com. 
Report Format  
The POID Conversion Report is produced in two formats: 
• Print Image format available in MBS Pool Net Report Center on the MBS Web Front End; 
• Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report. 
  
 
3 This can occur due to operations DD update, or processing of DK on pre-net CC. 

---

## Page 33

MBSD Operational [[Novation]] Reports GuIde  
 
POID Conv ersion R eport 33 
Print Image Report Layout 
This report details the SPT trades and STIP and generic TBA allocations converted to POIDs on the current 
business day grouped by [[settlement]] month/year and TBA [[CUSIP]]. The report has 3 sections; 1st for SPT 
trades, 2nd for STIP allocations and 3rd for generic TBA allocations. Within each section, the original SPT 
trade/PIDs are listed, followed by resulting POIDs. The report provides the following information. 
Machine-Readable Output Format 
This report is also available in MRO format. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation.  
Report Section Information 
Within each section, the individual POID Conversion details are listed, with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
[[participant]]/Aggregate  A three-digit  number is assigned to each [[Member]] followed 
by a 2-digit number or alphanumeric identifier  
Account Description  The account name 
Account [[ID]] The four -character account symbol  
Business Date A date field showing the current business date 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA CUSP of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD EXPLANATION 
[[settlement]] Month/Year  [[settlement]] month and year  
TBA [[CUSIP]] 9-character To Be Announced [[CUSIP]]     
SECURITY CLASS Description of this TBA [[CUSIP]]  
 
  

---

## Page 34

MBSD Operational [[Novation]] Reports GuIde  
 
POID Conv ersion R eport 34 
Original SPT Trades / PIDs 
Displays information on each SPT trade or allocation converted.  
FIELD EXPLANATION 
TRADE NBR Trade number on associated trade 
TRADE XREF XREF on associated trade  
PID Pool Instruct [[ID]] entifier (displayed for allocation conversions 
of STIP and Generic TBA trades only)  
B/S B or S (Buy or Sell) 
T/D Trade Date (for SPT trades only)  
D/D Delivery Date (for STIP and Generic TBA allocations only)   
S/D Contract ual [[settlement]] Date 
CONTRA Contra on the trade, equal to FSP T for SPT trades, F STI 
for STIP PIDs and F TBA for generic TBA PIDs 
POOL NBR Pool Number 
POOL [[CUSIP]] Pool [[CUSIP]] 
STTL PRICE Price, exclusive of commission  
ORIG FACE Original face  
CURR FACE Current face 
NET MONEY Net money  
CR/DR Indicator  Net money indicator, “CR” for credit, “DR” for debit  
Generated POIDs 
Displays information on each POID created.  
FIELD EXPLANATION 
POID NBR POID identifier  
TRADE NBR Trade number associated with this PO [[ID]] 
B/S B or S (Buy or Sell) 
D/D Delivery Date on PO [[ID]] 
S/D Contract ual [[settlement]] Date 
CONTRA Contra on the trade, equal F SPT for SPT POIDs, FSTI for 
STIP POIDs and FTBA for generic TBA PO IDs. 
POOL NBR Pool number on the PO [[ID]] 

---

## Page 35

MBSD Operational [[Novation]] Reports GuIde  
 
POID Conv ersion R eport 35 
FIELD EXPLANATION 
POOL [[CUSIP]] Pool [[CUSIP]] on the PO [[ID]] 
STTL PRICE [[settlement]] price on the PO [[ID]] 
ORIG FACE Original face on the PO [[ID]] 
CURR FACE Current face on the PO [[ID]] 
NET MONEY Net money on the PO [[ID]] 
CR/DR Indicator  Net money indicator, “CR” for credit, “DR” for debit  
Sub-Totals 
Sub-totals are provided for the following: 
• Sub-totals per MM/YYYY and TBA [[CUSIP]]  
• Sub-totals per Section (SPT, STIP and generic TBA)  
• Sub-totals per Report   
Where: 
• Orig Face = Net value of ORIG FACE of all trades, signed with “-“ if short 
• Current Face = Net value of CURR FACE of all trades, signed with “-“ if short 
• Net Money = Net value of NET MONEY of all trades, signed with “-“ if <$0 
Report Sort Order 
1. SPT section, followed by STIP section, followed by generic TBA section 
2. SPT trades/PIDs, followed by POIDs 
3. [[settlement]] Month/Year = earliest to latest 
4. TBA [[CUSIP]] = ascending order 
For SPT trades: 
1. [[settlement]] Date = earliest to latest 
2. Trade Number (ascending) 
For PIDs: 
1. Delivery Date = earliest to latest 
2. Trade Number (ascending) 
For POIDs (regardless of source) 

---

## Page 36

MBSD Operational [[Novation]] Reports GuIde  
 
POID Conv ersion R eport 36 
1. Same order as associated SPT trades/PIDs 
Note:  
The POIDs are not sorted  by POID order but rather follow the same order as associated SPT trade/P [[ID]] from which they 
were generated from. By doing this, cross -referencing between the 2 sections will be easier.  
  

---

## Page 37

MBSD Operational [[Novation]] Reports GuIde  
 
Cash Trade POID Conv ersion R eport 37 
CASH TRADE POID CONVERSION REPORT 
The Cash Trade POID Conversion Report Explained 
To see an example of the Cash Trade POID Conversion Report while you learn about its use, available 
formats, layout, header information and sort order, please visit the MBSD Operational [[Novation]] Reports page 
(with the MBS [[Novation]] Reports Explained tab open) on the [[DTCC]] Learning Center. It may be helpful to have 
it open while reading this guide as it will allow you to view actual reports in full size and interact with them to 
learn more. Note: you will need to be logged into the Learning Center to view this content. 
About the Cash Trade POID Conversion Report 
The Cash Trade POID Conversion Report is a daily, end-of-day report and captures the following cash trades 
converted to POIDs at trade price on a real-time basis: 
• Same-Day Generic PID: PID targeting TFTD/TBA or SBON with DD = today submitted on current 
business day result in POIDs vs FTBA at trade price. 
• Same-Day STIP PID: PID targeting STIP with DD = today submitted on current business day result in 
POIDs vs FSTI at trade price. 
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
• Print Image format available in MBS Pool Net Report Center on the MBS Web Front End; 
• Machine-Readable Output (MRO) format for members to use to automatically update their processing 
systems with the information contained on the report. 
  

---

## Page 38

MBSD Operational [[Novation]] Reports GuIde  
 
Cash Trade POID Conv ersion R eport 38 
Print Image Report Layout 
This report details the SPT trades and STIP and generic TBA allocations converted to POIDs on the current 
business day grouped by [[settlement]] month/year and TBA [[CUSIP]].  The report has 3 sections; 1st for SPT 
trades, 2nd for STIP allocations and 3rd for generic TBA allocations. Within each section, the original SPT 
trade/PIDs are listed, followed by resulting POIDs. 
Machine-Readable Output Format 
This report is also available in MRO format. The MRO format can be found at http://www.[[DTCC]].com/clearing-
services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. 
Report Section Information 
Within each section, the individual Cash Trade POID Conversion details are listed, with the following data.  
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD EXPLANATION 
[[participant]]/Aggregate  A three-digit  number is assigned to each [[Member]] followed 
by a 2-digit number or alphanumeric identifier  
Account Description  The account name 
Account [[ID]] The four -character account symbol  
Business Date A date field showing the current business date 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA CUSP of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD EXPLANATION 
[[settlement]] Month/Year  [[settlement]] month and year 
TBA [[CUSIP]] 9-character To Be Announced [[CUSIP]]  
SECURITY CLASS Description of this TBA [[CUSIP]]  
  

---

## Page 39

MBSD Operational [[Novation]] Reports GuIde  
 
Cash Trade POID Conv ersion R eport 39 
Original SPT Trades / PIDs 
Displays information on each SPT trade or allocation converted.  
FIELD EXPLANATION 
TRADE NBR Trade number on associated trade 
TRADE XREF XREF on associated trade  
PID Pool Instruct [[ID]] entifier (displayed for allocation conversions 
of STIP trade s only)  
B/S B or S (Buy or Sell) 
T/D Trade Date (for SPT trades only)  
D/D Delivery Date 
S/D Contract ual [[settlement]] Date 
CONTRA Contra on the trade, equal to F SPT for SPT trades, F STI 
for STIP PIDs and F TBA for generic TBA PIDs. 
POOL NBR Pool Number 
POOL [[CUSIP]] Pool [[CUSIP]] 
STTL PRICE Price, exclusive of commission  
ORIG FACE Original face  
CURR FACE Current face 
NET MONEY Net money  
CR/DR Indicator  Net money indicator, “CR” for credit, “DR” for debit  
Generated POIDs 
Displays information on each POID created.  
FIELD EXPLANATION 
POID NBR POID identifier  (Pool Obligation [[ID]] Number) 
TRADE NBR Trade number associated with this PO [[ID]] 
PID Pool Instruct [[ID]] entifier (displayed for allocation conversions 
of STIP trades only)  
B/S B or S (Buy or Sell) 
D/D Delivery Date on PO [[ID]] 
S/D Contract [[settlement]] Date  
CONTRA Contra on the trade, equal F SPT for SPT POIDs, FSTI for 
STIP POIDs and FTBA for generic TBA PO IDs 

---

## Page 40

MBSD Operational [[Novation]] Reports GuIde  
 
Cash Trade POID Conv ersion R eport 40 
FIELD EXPLANATION 
POOL NBR Pool number on the PO [[ID]] 
POOL [[CUSIP]] Pool [[CUSIP]] on the PO [[ID]] 
STTL PRICE [[settlement]] price on the PO [[ID]] 
ORIG FACE Original face on the PO [[ID]] 
CURR FACE Current face on the PO [[ID]] 
NET MONEY Net money on the PO [[ID]] 
CR/DR Indicator  Net money indicator, “CR” for credit, “DR” for debit  
Sub-Totals 
Sub-totals are provided for the following: 
• Sub-totals per MM/YYYY and TBA [[CUSIP]]  
• Sub-totals per Section (SPT, STIP and generic TBA)  
• Sub-totals per Report   
Where: 
• Orig Face = Net value of ORIG FACE of all trades, signed with “-“ if short 
• Current Face = Net value of CURR FACE of all trades, signed with “-“ if short 
• Net Money = Net value of NET MONEY of all trades, signed with “-“ if <$0 
Report Sort Order 
1. SPT section, followed by STIP section, followed by generic TBA section 
2. SPT trades/PIDs, followed by POIDs 
3. [[settlement]] Month/Year = earliest to latest 
4. TBA [[CUSIP]] = ascending order 
For SPT trades: 
1. [[settlement]] Date = earliest to latest 
2. Trade Number (ascending) 
For PIDs: 
1. Delivery Date = earliest to latest 
2. Trade Number (ascending) 

---

## Page 41

MBSD Operational [[Novation]] Reports GuIde  
 
Cash Trade POID Conv ersion R eport 41 
For POIDs (regardless of source) 
1. Same order as associated SPT trades/PIDs 
Note:  
The POIDs are not sorted by POID order but rather follow the same order as associated SPT trade/PID from which they 
were generated from. By doing this, cross -referencing between the 2 sections will be easier.  
  

---

## Page 42

MBSD Operational [[Novation]] Reports GuIde  
 
Cash Trade POID Conv ersion R eport 42 
 
 
 
FOR MORE INFORMATION 
 
Email Learning group at: 
corelearning@[[DTCC]].com 
or visit us on web at: 
www.dtcclearning.com 