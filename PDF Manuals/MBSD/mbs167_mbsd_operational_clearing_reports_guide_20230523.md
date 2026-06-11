---
title: "MBSD Operational Clearing Reports Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs167_mbsd_operational_clearing_reports_guide_20230523.pdf"
pages: 68
size: "749.5 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD Operational Clearing Reports Guide

**Original File:** [mbs167_mbsd_operational_clearing_reports_guide_20230523.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs167_mbsd_operational_clearing_reports_guide_20230523.pdf)  
**Category:** MBSD  
**Total Pages:** 68  
**File Size:** 749.5 KB  

---

## Page 1

 
MORTGAGE-BACKED [[securities]] 
(MBS)  
MBSD OPERATIONAL CLEARING REPORTS GUIDE 
VERSION 1.3 
MAY 23, 2023 
 


---

## Page 2

 
 
Copyright © 2023 by The Depository Trust & Clearing Corporation (“[[DTCC]]”).  
All rights reserved. This work (including, without limitation, all text, images, logos, compilation and design) is proprietar y  and  
protected by copyright and is for the exclusive use of users author ized by [[DTCC]]. If this work is received from [[DTCC]] in any 
electronic medium, authorized users of this work are granted a limited, non -exclusive, non- transferable, non -sublicensable 
and freely revocable license to make reproductions and transmissions necessar y for downloading and stor age of this work 
on the users' computers and to print one or more paper copies from the electronic version for their own use. Other than to 
this limited extent, no part of this work (including any paper copies thereof or print ver sions thereof) may be printed, copied, 
altered, modified, posted, reproduced, displayed, published, sold, licensed, used or distributed (including by transmission) 
in any form or by any means, or stored in any information stor age and retrieval system, without [[DTCC]]'s prior written 
permission.  
All product or service names are the property of their respective owners.  
 
Doc Info: May 23, 2023 
Publication Code:  MBS167 
Service: [[FICC]] MBSD 
Title: MBSD Operational Clearing Report s Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction..................................................................................................................................... 8  
Compressed Open Commitment Report ............................................................................................ 9  
About the Compressed Open Commitment Report............................................................................... 9  
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n ............................................................................ 9  
Account Header Information .......................................................................................................... 9  
TBA [[CUSIP]] Header Information ................................................................................................... 10 
Trade Details............................................................................................................................. 10 
TBA [[CUSIP]] Totals ..................................................................................................................... 12 
Report Footer ............................................................................................................................ 12 
Print Imag e Report Sor t Or der ........................................................................................................ 14 
Other Report Formats ................................................................................................................... 14 
MRO Reports.............................................................................................................................. 14 
Difference between MRO and Print Image Compressed OCR........................................................... 14 
Tilde Delimited Reports ................................................................................................................ 14 
Tilde He a der R ow In for ma tion...................................................................................................... 15 
Tilde De tail R ow  In forma tion  for C ompre sse d OCR ......................................................................... 15 
PMAT Report ..................................................................................................................................17  
About the PMAT Report................................................................................................................. 17 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 17 
Account Header Information ........................................................................................................ 17 
TBA [[CUSIP]] Header Information ................................................................................................... 18 
Trade Details............................................................................................................................. 18 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 20 
Other Report Formats ................................................................................................................... 20 
Purchase and Sale Report ...............................................................................................................21  
About the Purchase and Sale Report ............................................................................................... 21 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 21 
Account Header Information ........................................................................................................ 22 

---

## Page 4

 
 
TBA [[CUSIP]] Header Information ................................................................................................... 22 
Trade Details............................................................................................................................. 23 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 26 
Other Report Formats ................................................................................................................... 26 
MRO Reports.............................................................................................................................. 26 
Tilde Delimited Repo rts ................................................................................................................ 26 
Tilde He a der R ow In for ma tion...................................................................................................... 27 
Tilde Detail Row Information for Purchase and Sale Report .............................................................. 27 
Unmatched [[Margin]] Report ...............................................................................................................29  
About the Unmatched [[Margin]] Report ............................................................................................... 29 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 29 
Account Header Information ........................................................................................................ 30 
TBA [[CUSIP]] Header Information ................................................................................................... 30 
Trade Details............................................................................................................................. 30 
TBA Footer ............................................................................................................................... 31 
Report Footer ............................................................................................................................ 32 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 32 
Other Report Formats ................................................................................................................... 32 
DNA Report ....................................................................................................................................33  
About the DNA Report ................................................................................................................... 33 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 33 
Account Header Information ........................................................................................................ 34 
D NA Head er Info rmatio n ............................................................................................................. 34 
D NA  Trad e Ass ig nment D etails .................................................................................................... 34 
D NA Req uest Sub-Totals ............................................................................................................ 35 
D NA Req uest [[SEC]] tio n Sub-Totals.................................................................................................  35 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 35 
Other Report Formats ................................................................................................................... 36 
MRO Reports.............................................................................................................................. 36 
Difference between MRO and Print-imag e D NA Repo rt ................................................................... 36 

---

## Page 5

 
 
MBSCC/EPN Message Detail Report................................................................................................. 37 
About the MBSCC/EPN Message Detail Report ................................................................................ 37 
Report Section/Layout Information .................................................................................................. 37 
Report Layout/Field Information ................................................................................................... 37 
Report Sort Order ......................................................................................................................... 39 
Other Report Formats ................................................................................................................... 40 
MBSCC/EPN Message Summary Report ...........................................................................................41  
About the MBSCC/EPN Message Summary Report ........................................................................... 41 
Report Section/Layout Information .................................................................................................. 41 
Report Layout/Field Information ................................................................................................... 41 
Report Sort Order ......................................................................................................................... 42 
Other Report Formats ................................................................................................................... 42 
Open Commitment Summary Report ................................................................................................43  
About the Open Commitment Summary Report ................................................................................. 43 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 43 
Account Header Information ........................................................................................................ 43 
TBA [[CUSIP]] Header Information ................................................................................................... 44 
TBA [[CUSIP]] Totals ..................................................................................................................... 44 
Report Footer ............................................................................................................................ 45 
Print Imag e Report Sor t Or der ........................................................................................................ 46 
Other Report Formats ................................................................................................................... 46 
MRO Reports.............................................................................................................................. 46 
Difference between MRO and Print Image Open Commitment Summary Report.................................. 46 
TBA Net Detail Report .....................................................................................................................47  
About the TBA Net Detail Report..................................................................................................... 47 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 47 
Account Header Information ........................................................................................................ 47 
TBA [[CUSIP]] Header Information ................................................................................................... 48 
Original SBOD Trades ................................................................................................................ 48 
Resulting SBON ........................................................................................................................ 49 

---

## Page 6

 
 
Sub-Totals ................................................................................................................................ 49 
Print Imag e Repo rt So rt Ord er ........................................................................................................ 50 
Other Report Formats ................................................................................................................... 50 
MRO Reports.............................................................................................................................. 50 
Tilde Delimited Reports ................................................................................................................ 50 
Tilde He a der R ow In for ma tion...................................................................................................... 51 
Tild e D etail Ro w Info rmatio n fo r TBA Net D etail Repo rt.................................................................... 51 
Netting Conversion Report ..............................................................................................................52  
About the Netting Conversion Report ............................................................................................... 52 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 52 
Account Header Information ........................................................................................................ 52 
TBA [[CUSIP]] Header Information ................................................................................................... 53 
Trade Details............................................................................................................................. 53 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 54 
Other Report Formats ................................................................................................................... 54 
Cash [[settlement]] Details Report .......................................................................................................55  
Abo ut the Cas h [[settlement]] D etails  Repo rt ........................................................................................ 55 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 55 
Account Header Information ........................................................................................................ 55 
Cash Obligation Header Information ............................................................................................. 56 
Report Footer ............................................................................................................................ 57 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 57 
Other Report Formats ................................................................................................................... 57 
[[Broker]] Commission Fees Report .....................................................................................................58  
Report Summary .......................................................................................................................... 58 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 58 
Account Header Information ........................................................................................................ 58 
Trade Details............................................................................................................................. 59 
Report Totals ............................................................................................................................ 59 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 60 

---

## Page 7

 
 
Other Report Formats ................................................................................................................... 60 
MRO Reports.............................................................................................................................. 60 
Difference between MRO and Print Image [[Broker]] Commission Report............................................... 60 
Dealer Commission Fees Report ......................................................................................................61  
Report Summary .......................................................................................................................... 61 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Info rmatio n .......................................................................... 61 
Account Header Information ........................................................................................................ 61 
Trade Details............................................................................................................................. 62 
Report Totals ............................................................................................................................ 62 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 63 
Other Report Formats ................................................................................................................... 63 
MRO Reports.............................................................................................................................. 63 
Difference between MRO and Print Image Dealer Commission Report............................................... 63 
TBA Trade Reprice And Variance Report ..........................................................................................64  
About the TBA Trade Reprice and Variance Report ........................................................................... 64 
Print Imag e (pdf) Repo rt [[SEC]] tio n/Layo ut Information .......................................................................... 64 
Account Header Information ........................................................................................................ 64 
TBA [[CUSIP]] Header Information ................................................................................................... 65 
Repriced Trade Details ............................................................................................................... 65 
TBA [[CUSIP]] Sub-To t als............................................................................................................... 66 
Report Totals ............................................................................................................................ 66 
Sub-Totals ................................................................................................................................ 66 
Print Ima ge  Re port Sor t Or der ........................................................................................................ 66 
Other Report Formats ................................................................................................................... 66 
MRO Reports.............................................................................................................................. 67 
Difference between MRO and Print-image TBA Trade Reprice and Variance Report ............................ 67 
 

---

## Page 8

MBSD Operational Clearing Reports Guide 
Introduction 8 
INTRODUCTION 
The purpose of this guide is to explain the reports produced by the Mortgage-Backed [[securities]] Division of the 
Fixed Income Clearing Corporation pertaining to MBS Clearing processing. This guide assumes that the reader 
has a general knowledge of mortgage-backed [[securities]] processing.  
All MRO Report layouts can be found in the [[FICC]] MBSD User Documentation section of the [[DTCC]] website 
(http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/[[FICC]]-mbsd-us er-documentation) (look for the Machine 
Readable Output (MRO) section.) 
To access MBSD RTTM Web Report Center, visit: https://webficc.[[DTCC]].net/ps/ct_logon.html. 
The reports explained in this guide are those that can be viewed in Report Center within the MBS Clearing 
section. Which reports are viewable and the order in which they may appear is determined in part by the date 
(today’s date or a past date) and time of day at which a search is made.  
 
Figure 1: [[FICC]] Report Center (MBS Clearing [Reports] link highlighted) 
This guide provides the following information about each MBS Clearing Report: 
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

## Page 9

MBSD Operational Clearing Reports Guide 
Compressed Open C ommitment Report 9 
COMPRESSED OPEN COMMITMENT REPORT 
About the Compressed Open Commitment Report 
The MBSD Compressed Open Commitment Report (OCR) is produced on every business date to reflect all 
matched, unsettled (or open) positions on [[FICC]]’s books for a given [[Member]]. This report is cumulative. A 
trade/position will appear on the OCR from the first system pass in which it was matched. 
Members use the MBSD Compressed OCR to validate and balance their open trades/positions. The positions 
listed on the OCR are the positions guaranteed and risk managed by [[FICC]]. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual Open Commitment details are listed with the 
following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]  A three-digit  number is assigned to each [[Member]]. 
AGGREGATE 
NUMBER  
A two-character  alphanumeric following the [[participant]] [[ID]], which links an Account [[ID]] ([[participant]] 
Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk management 
and cash [[settlement]] reporting purposes.  
[[participant]] 
NAME  
The name of the [[Member]]. 
[[participant]] 
SYMBOL  
A 4-character identifier, the [[participant]] Symbol  represents the primary level of system identification. 
Trade submission occurs at the account level.  
DATE OF 
REPORT  
The date the report was created.  

---

## Page 10

MBSD Operational Clearing Reports Guide 
Compressed Open C ommitment Report 10 
FIELD  EXPLANATION  
PASS 
INDICATOR  
AM or PM system pass. MBSD has two system passes. The AM pass is run in the afternoon, and 
the PM pass occurs in the evening. To learn more about the timeframes, please refer to the MBSD 
processing Schedule & Timeframes document which may be found in the [[participant]] Reference 
Documentation (MBS) section on www.[[DTCC]].com . 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD  EXPLANATION  
[[settlement]] 
MONTH 
The [[settlement]] month of the [[CUSIP]]. 
[[settlement]] YEAR  The [[settlement]] year of the [[CUSIP]].  
[[CUSIP]]  The nine -character TBA [[CUSIP]]. 
SECURITY CLASS  The security class code of the security reported on the trade (Agency, Product, Coupon, 
Maturity). 
SECURITY 
DESCRIPTION  
The Agency and Product Code description.  
MARKET PRICE  Unless the price changes, the “AM” reports reflect the previous day’s end -of-day process while 
the “PM” reports reflect the current day’s end -of-day price. 
Trade Details 
Displays information on each TBA or SPT trade. 
FIELD  EXPLANATION  
TRADE NBR  Trade Number: The trade number is a unique 10- digit number assigned by [[FICC]] to a compared 
trade. Only compared trades are displayed on the OCR.  
XREF  The XREF is assigned by the [[Member]] –it’s alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]] –the [[Member]] cannot have any other trades in the system 
with that same XREF.  

---

## Page 11

MBSD Operational Clearing Reports Guide 
Compressed Open C ommitment Report 11 
FIELD  EXPLANATION  
TRD STAT  The MBSD Compressed Open Commitment Report includes the following trade status types:  
• FMAT trade status type is reported for trades that are Fully Matched. For a dealer -to-dealer 
trade, this means that both the buying and selling dealers have submitted trade details into 
MBSD and all mandatory matching fields submitted by both have been the same (i.e., have 
matched). For a brokered trade, this means that the [[Broker]] has matched both the buying dealer 
and the selling dealer on the trade.  
• PMAT trade status type is reported for brokered trades that are Partially Matched . This means 
that the [[Broker]] has matched either the buying dealer’s trade submission or the selling dealer’s 
trade submission, but not both. The trade being reported in PMAT status is the side that has 
been matched.  
Note  
Uncompared trades, DKs, Cancel Requests, and Pending Cancels will  not appear on the OCR.  
TRD TYPE  The MBSD Open Commitment Report includes the following trade types:  
• OPTN trade type is reported when a [[Member]] trade is an [[Option]].  
• SBOD trade type is reported (pre -TBA netting) when a [[Member]]’s trade is [[settlement]] Balance 
Order Destined , which is another way of saying that the trade will be included in TBA netting 
when the TBA netting date for its security class is reached. Status must be FMAT to be netted.  
• SBON trade type is reported (post TBA Netting) when a [[Member]]’s trade [[settlement]] Balance 
Order position went through the TBA Net. The SBON is the final net TBA [[settlement]] obligation. 
This is applicable to dealers only.  
• TFTD trade type is reported when the TBA [[CUSIP]] is not netting eligible, one party to the trade 
is not eligible for T BA netting or netting is not desired by either side of the trade .  
SUB TYPE The type of TFTD is provided to assist members with distinguishing between TFTD TB A, SPT or 
STIP trades, as well as the type of OPTN (i.e. PUT, CALL). This is applicable for both [[Broker]] and 
dealer versions (except OPTNs for brokers who cannot submit OPTN trade types)  
B/S  Buy/Sell: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
T/D  Trade Date: The date the trade was executed between the members.  
S/D  [[settlement]] Date: The contractual [[settlement]] date of the trade.  
For SBOD trades, the date is reflected as the month and year with two zeros for the day (e.g. 
07/00/2012). The [[settlement]] date is based on the SIFMA Class of the trade (see the description for 
TBA [[CUSIP]]). [[FICC]] will automatically net the trade on the SIFMA established TBA netting day.  
M/D  Match Date: The date the trade was bilaterally co mpared.  
G/U  Give-Up is obsolete since the implementation of MBSD Operational [[Novation]] and thus give -up date 
will be blank.  
CTRA Contra: Upon trade comparison, the trade becomes novated to face a [[FICC]] account as contraside 
to the trade. This is applicable to dealers only.  
BRKR  [[Broker]]: If the trade was brokered, the [[Broker]] [MBSD account symbol] will appear here.  
CMSN Commission: Commission fields have been added to display commission on a brokered trade as a 
dollar amount. For dealer versions, a single commission value is displayed. For [[Broker]] versions, 
both buy and sell commission values are shown.  
STTL PRICE  [[settlement]] Price: This is the [[settlement]] price of the trade prior to TBA netting.  

---

## Page 12

MBSD Operational Clearing Reports Guide 
Compressed Open C ommitment Report 12 
FIELD  EXPLANATION  
For dealers, the submitted price. If the dealer included the price inclusive of commission, then the 
dealer price will be a different price than the [[settlement]] price. For brokers, the submitted price. 
They separately submit the commission in the commission field.  
OPEN PAR  The par value of the trade that has not settled. 
STTL VALUE  [[settlement]] Value: The [[settlement]] value of the trade. This is equal to the open par multiplied by the 
[[settlement]] price. For SPTs the formula is different. The [[settlement]] value equals current face 
multiplied by price plus accrued interest.  
POOL NUMBER  The pool number is only included for Specified Pool Trades. For SPTs, the pool number is one of 
the agreed upon trade terms.  
  
TBA [[CUSIP]] Totals 
After the trade details for each TBA [[CUSIP]], TBA [[CUSIP]] totals are displayed for each. 
FIELD NAME  EXPLANATION  
BUY OPEN PAR  This is the sum of the open par for all buy positions for the TBA [[CUSIP]] and S/D.  
SELL OPEN PAR  This is the sum of the open par for all sell positions for the TBA [[CUSIP]] and S/D.  
NET OPEN PAR  This is the net of the buy and sell open par for the TBA [[CUSIP]] and S/D.  
BUY STTL VALUE  This is the sum of the [[settlement]] values for all buy positions for the TBA [[CUSIP]] and S/D.  
SELL STTL VALUE  This is the sum of the [[settlement]] values for all see positions for the TBA [[CUSIP]] and S/D.  
NET STTL VALUE  This is the net of the buy and sell [[settlement]] values for the TBA [[CUSIP]] and S/D.  
BUY P&L  This is the sum of the Profit/Loss for all buy positions  for the TBA [[CUSIP]] and S/D.  
SELL P&L  This is the sum of the Profit/Loss for all sell positions for the TBA [[CUSIP]] and S/D.  
NET P&L  This field reflects the net of the “buy and sell” P/L calculations. (C R=Credit, DR=Debit)  
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD NAME  EXPLANATION  
BUY FORWARD ITEMS  The number of buy trades with a [[settlement]] date greater than the day of the report.  
BUY FORWARD OPEN PAR  The sum of the open par of the buy trades with a [[settlement]] date greater than the day 
of the report.  
BUY FORWARD STTL VALUE  The sum of the [[settlement]] value of the buy trades with a [[settlement]] date greater than 
the day of the report.  
BUY FAIL ITEMS  The number of buy trades with a [[settlement]] less than or equal to the date of the 
report.  

---

## Page 13

MBSD Operational Clearing Reports Guide 
Compressed Open C ommitment Report 13 
FIELD NAME  EXPLANATION  
BUY FAIL OPEN PAR  The sum of the open par of the buy trade s with a [[settlement]] date less than or equal to 
the day of the report.  
BUY FAIL STTL VALUE  The sum of the [[settlement]] value of the buy trades with a [[settlement]] date less than or 
equal to the day of the report.  
BUY TOTAL OPEN PAR  The sum of the open par  of all buy trades.  
BUY TOTAL STTL VALUE  The sum of the [[settlement]] value of all buy trades.  
SELL FORWARD ITEMS  The number of sell trades with a [[settlement]] date greater than the day of the report.  
SELL FORWARD OPEN PAR  The sum of the open par of the sell trades with a [[settlement]] date greater than the day 
of the report.  
SELL FORWARD STTL VALUE  The sum of the [[settlement]] value of the sell trades with a [[settlement]] date greater than 
the day of the report.  
SELL FAIL ITEMS  The number of sell trades with a [[settlement]] less than or equal to the date of the 
report.  
SELL FAIL OPEN PAR  The sum of the open par of the s ell trades with a [[settlement]] date less than or equal to 
the day of the report.  
SELL FAIL STTL VALUE  The sum of the [[settlement]] value of the sell trades with a [[settlement]] date less than or 
equal to the day of the report.  
SELL TOTAL OPEN PAR  The sum of the open par of all sell trades.  
SELL TOTAL STTL VALUE  The sum of the [[settlement]] value of all sell trades.  
NET FORWARD OPEN PAR  The difference between the total buy and sell open par for trades with a [[settlement]] 
date greater than the date of the report.  
NET FORWARD STTL VALUE  The difference between the total buy and sell [[settlement]] values for trades with a 
[[settlement]] date greater than the date of the report.  
NET FAIL OPEN PAR  The difference between the total buy and sell open par for trades with a [[settlement]] 
date less than or equal to the date of the report.  
NET FAIL STTL VALUE  The difference between the total buy and sell [[settlement]] values for trades with a 
[[settlement]] date less than or equal to the date of the report.  
TOTAL NET OPEN PAR  The difference between the total buy and sell open par for all trades listed on the 
OCR.  
TOTAL NET STTL VALUE  The difference between the total buy and sell [[settlement]] values for all trades listed on 
the OCR.  
 
  

---

## Page 14

MBSD Operational Clearing Reports Guide 
Compressed Open C ommitment Report 14 
Print Image Report Sort Order 
The Compressed Open Commitment Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]]/Security Class = ascending order 
3. Type of Trade = ascending order 
4. Trade Number = ascending order. 
Other Report Formats 
The Compressed Open Commitment Report is also available in other formats: 
Report Name Afternoon Pass (AM)  Evening Pass (PM)  Format 
Compressed OCR  X X MRO, Tilde delimited  
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the Compressed Open 
Commitment Report is available in two types: RJE and NDM. All MRO Report layouts can be found in the [[FICC]] 
MBSD User Documentation section of the [[DTCC]] website (http://www.[[DTCC]].com/clearing-services/[[FICC]]-
mbsd/[[FICC]]-mbsd-user-documentation#MachineReadableOutput) Look for: 
• RJE Compressed Open Commitment Report. (RJE format is grandfathered in for existing members.) 
• NDM Compressed Open Commitment Report. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist–there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Difference between MRO and Print Image Compressed OCR 
The MRO report has several fields reflecting the value for aged fails; however, the value is displayed as zero. 
Tilde Delimited Reports 
In this format, fields are separated by a tilde (~). Files in this layout can be imported into Excel and are posted 
to Report Center (extension “.tld”) in the same location as the corresponding PDF. When downloaded, header 
field information is not retained. Tilde-separated reports are generated according to the same rules as with 
Print Image. The tilde-separated file is based on the MRO equivalent, where each row in the tilde contains data 
from various card codes. When a tilde-separated file has no data rows to include (an “empty” file condition), a 
“header” row (card code 01) will be included in the file, followed by a row indicating “no activity”. 
  

---

## Page 15

MBSD Operational Clearing Reports Guide 
Compressed Open C ommitment Report 15 
Tilde Header Row Information 
The first row in every tilde-separated file is a standard “header” row, as defined below: 
Standard Tilde -Separated File Header Row  
Field Description 
Header Record Card Code  “01”  
Report [[ID]]  Identifier specific to given report  
[[participant]] [[ID]]  3-character [[participant]] [[ID]]  
Aggregate Number  2-character aggregate  
Account  4-character account  
[[participant]] Name  40-character [[participant]] name, as taken from 
Account master files 
Report Date YYYYMMDD 
 
Tilde Detail Row Information for Compressed OCR 
Tilde “detail” rows contain information from card code 03 (dealer detail) or 07 ([[Broker]] detail), as summarized in 
the table below.  
Field Type Format Comment Populated for Card 
Code? 
Card Code  2 N PIC 9(02) 03 (dealer detail), 07 ([[Broker]] record)  03 07 
[[settlement]] Year 4 N  PIC 9(04) Format YYYY   
[[settlement]] Month  2 A/N  PIC X(02) Format MM   
[[CUSIP]] 9 A/N  PIC X(09)    
Account Symbol  4 A/N  PIC X(04)    
Trade Number  10 N  PIC 9(10)    
Internal XREF/ Trade # 15 A/N  PIC X(15)    
Trade Status 4 A/N PIC X(04) FMAT, FSET, PMAT, PSET   
Trade Type 4 A/N  PIC X(04) OPTN, SBOD, SBON, TFTD    
Buy/Sell Indicator  1 A/N  PIC X(01) B = Buy, S = Sell   
 
Trade Date 8 A/N PIC X(08) Format YYYYMMDD   
[[settlement]] Date 8 A/N  PIC X(08) Format YYYYMMDD   
Match Date 8 A/N PIC X(08) Format YYYYMMDD   
Give-Up Date 8 A/N PIC X(08) Format YYYYMMDD   

---

## Page 16

MBSD Operational Clearing Reports Guide 
Compressed Open C ommitment Report 16 
Field Type Format Comment Populated for Card 
Code? 
Contra Account  4 A/N  PIC X(04)   
 
[[Broker]] Account Symbol  4 A/N PIC X(04)    
Buy Dealer Account 
Symbol 
4 A/N PIC X(04)    
Sell Dealer Account  4 A/N PIC X(04)    
Symbol      
[[settlement]] Price 15 N  PIC 9(03)V9(12) In decimal    
Open Par Value 13 N  PIC 9(11)V9(02) 
 
  
[[settlement]] Value 13 N PIC 9(11)V9(02)    
Commission Amount  7 N PIC 9(05)V9(02) As dollar value   
Buy Dealer Commission 
Amount 
7 N  PIC 9(05)V9(02) As dollar value 
 
 
Sell Dealer Commission 
Amount 
7 N  PIC 9(05)V9(02) As dollar value 
 
 
Trade Sub-Type  4 A/N PIC X(04) CALL, PUT, SPT,STIP, TBA   
Pool Number 6 A/N PIC X(06) 
 
  
Original Par Value  13 N PIC 9(11)V9(02) 
 
  

---

## Page 17

MBSD Operational Clearing Reports Guide 
PMAT Report 17 
PMAT REPORT 
About the PMAT Report 
The MBSD PMAT Report is produced every business day after the AM and PM Pass to reflect all partially 
matched trades. PMAT trades only pertain to brokered trading activity. Brokers have a two-sided submission 
(i.e. a Trade Instruct versus the buying Dealer and a Trade Instruct versus the selling Dealer) so brokered 
trades can either be partially matched (PMAT) or fully matched (FMAT). A PMAT occurs when only one Dealer 
contraside has matched with the [[Broker]], but not both. An FMAT occurs when both the buying and selling 
Dealers and [[Broker]] have submitted Trade Instructs to RTTM, and the trade terms are consistent and matched. 
A PMAT trade is updated to FMAT when the previously unmatched Dealer contraside and its [[Broker]]’s trade 
terms match. 
Members use this report to monitor all PMAT trades where they are the matched dealer on the trade. Members 
should contact their [[Broker]] to resolve PMAT trades as quickly as possible. PMAT SBOD trades are not TBA 
netting eligible, and PMAT TFTD trades are not eligible for Allocation or Pool Netting. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”. 
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]  A three-digit  number is assigned to each [[Member]]. 
AGGREGATE 
NUMBER  
A two-character  alphanumeric following the [[participant]] [[ID]], which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk 
management and cash [[settlement]] reporting purposes.  
[[participant]] NAME  The name of the [[Member]]. 
[[participant]] 
SYMBOL  
A 4-character identifier, the [[participant]] Symbol  represents the primary level of system 
identification. Trade submission occurs at the account level.  

---

## Page 18

MBSD Operational Clearing Reports Guide 
PMAT Report 18 
FIELD  EXPLANATION  
DATE OF REPORT  The date the report was created.  
PASS INDICATOR  AM or PM system pass. MBSD has two system passes. The AM pass is run in the afternoon,  
and the PM pass occurs in the evening. To learn more about the timeframes, please refer to the 
MBSD Processing Schedule & Timeframes document which may be found in the [[participant]] 
Reference Documentation (MBS) section on www.[[DTCC]].com . 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD  EXPLANATION  
[[settlement]] 
MONTH  
The [[settlement]] month of the [[CUSIP]]. 
[[settlement]] YEAR  The [[settlement]] year of the [[CUSIP]].  
[[CUSIP]]  The nine -character TBA [[CUSIP]].  
SECURITY CLASS  The security class code of the security reported on the trade (Agency, Product, Coupon, or 
Maturity). 
SECURITY 
DESCRIPTION  
The Agency and Product Code description.  
MKT PRICE Market Price: Current market price as determined by MBSD which is used for determining P&L 
of the trade. 
Trade Details 
The following table explains those trade details most relevant to events taking place during the trade 
comparison phase of the trade life cycle. 
FIELD  EXPLANATION  
TRD #  Trade Number: The trade number is a unique 10- digit number assigned by [[FICC]] to a compar ed 
trade. Only PMAT trades are displayed on the PMAT Report. When the unmatched Dealer submits a 
matching Trade Instruct and the PMAT trade becomes FMAT, the same trade number is assigned.  
XREF  The XREF is assigned by the [[Member]] –it’s alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]] –the [[Member]] cannot have any other trades in the system 
with that same XREF.  
TRD STAT  This field reflects the trade status. Only PMAT trades appear on the PMAT Repo rt.  
• PMAT: Partially Matched [[Broker]]/Dealer Trade. From a Dealer perspective, this means that they 
have matched the trade but the Dealer on the other side has not matched the trade.  
TYP-TRD SUB • TFT Sub-Type: The type of TFTD is provided to assist members with distinguishing between 
TFTD TBA, SPT or STIP trades.  
• OPTN trade type (PUT/CALL) is reported when a [[Member]] trade is an [[Option]].  

---

## Page 19

MBSD Operational Clearing Reports Guide 
PMAT Report 19 
FIELD  EXPLANATION  
• SBOD trade type is reported (pre -TBA netting) when a [[Member]]’s trade is [[settlement]] Balance 
Order Destined , which is another way of saying that the trade will be included in TBA Netting 
when the TBA netting date for its security class is reached. Status must be FMAT to be netted.  
• TFTD trade type is reported when the TBA [[CUSIP]] is not netting eligible, one party to the trade 
is not eligible for TBA netting or netting is not desired by either side of the trade . 
Note  
SBON positions will never appear on the PMAT Report, because SBON trades are a result of the 
TBA NET. 
B/S  Buy/Sell: Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
E/D  Entry Date: The entry date for the trade (i.e., the day the [[Member]] submitted the trade to RTTM.)  
T/D  Trade Date: The date the trade was executed between the members.  
M/D  Match Date: The date the trade was bilaterally compared.  
S/D  [[settlement]] Date: The contractual [[settlement]] date of the trade. For SBOD and OPTN trades, the date 
is reflected as the month and year with two zeros for the day (e.g. 07/00/2012). The settlemen t date 
is based on the SIFMA Class of the trade. If a SBOD trade is still PMAT on the given SIFMA 
Class TBA Netting Day, RTTM will convert the SBOD trade to a TFTD. The PMAT trade will no 
longer reflect the [[settlement]] date of 07/00/2012 and will reflect the SIFMA Class [[settlement]] 
Date (e.g. 07/12/2012). 
G/U  Give-Up is obsolete since the implementation of MBSD Operational [[Novation]] and thus give -up date 
will be blank.  
CTRA  Contraside: This is the contraside to the trade. Since all PMAT trades are brokered  trades, the 
[[Broker]] will always appear here on a PMAT trade.  
BRKR  [[Broker]]: The [[Broker]] account symbol. Only brokered trades appear on the PMAT Report. The [[Broker]] 
symbol will appear here as well as under CT RA. 
CMSSN  Commission: Only applies to brokered trades, and even then,  it is optional. The commission amount 
listed will be debited from the dealer and credited to the [[Broker]] the month following the CSD of trade 
on B [[settlement]] day.  
DEALER PRICE  This is the price t hat the dealer submitted on the trade (padded with zeros past the last decimal 
place out to 12 decimal places). For a brokered trade with commission, the dealer may include the 
price either inclusive or exclusive of commission. If the dealer included the price inclusive of 
commission, then the dealer price will be a different price than the [[settlement]] price.  
STTL PRICE  [[settlement]] Price: This is the [[settlement]] price of the trade prior to TBA netting. 
For dealers, the submitted price. If the dealer included  the price inclusive of commission, then the 
dealer price will be a different price than the [[settlement]] price. For brokers, the submitted price. They 
separately submit the commi ssion in the commission field.  
MKT [[Premium]]  Market [[Premium]]: It will always just reflect z eros. Reserved for future use.  
FCAP  FCAP is obsolete since the implementation of MBSD Operational [[Novation]] and thus FCAP price  will 
be blank  
OPEN PAR  The par value of the trade that has not settled. For PMAT trades, the open par will always equal 
the original par of the trade.  

---

## Page 20

MBSD Operational Clearing Reports Guide 
PMAT Report 20 
FIELD  EXPLANATION  
ORIG PAR  Original Par: The par value of the trade that was matched and agreed to as part of the trade terms.  
STTL VAL  [[settlement]] Value: The [[settlement]] value of the trade. This is equal to the open par multiplied by the 
[[settlement]] price.  
MARKET VALUE  This is the open par of the trade multiplied by the market price, divided by 100. This is t he current 
value of the trade.  
P&L  Profit & Loss: This is the profit or loss of the trade/position. It’s the difference between the market 
value of the trade and the [[settlement]] value of the trade.  
• For “buy” trades, if the market value < [[settlement]] value, the position is in a loss. If the market 
value > [[settlement]] value, the position is in a profit.  
• For “sell” trades, if the market value < [[settlement]] value, the position is in a profit. If the market 
value > [[settlement]] value, the position is in a loss.  
• D = Debit, C = Credit.  
POOL NUMBER The pool number is only included for Specified Pool Trades. For SPTs, the pool number is one of the 
agreed upon trade terms.  
MATURITY DT  The maturity date of the pool number.  
Print Image Report Sort Order 
The PMAT Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]]/Security Class = ascending order 
3. Type of Trade = ascending order 
4. Trade Number = ascending order. 
Other Report Formats 
The PMAT Report is ONLY available in print image format: 
Report Name Afternoon Pass (AM)  Evening Pass (PM)  Format 
PMAT X X PDF 
 

---

## Page 21

MBSD Operational Clearing Reports Guide 
Purchas e and Sale Report 21 
PURCHASE AND SALE REPORT 
About the Purchase and Sale Report 
The Purchase and Sale Report is produced at the end of each pass on every business date. Events appear in 
the PM version of the P&S only, except for SPT conversion to POID which can appear in AM or PM due to 
real-time (cash) trade processing. This report is not cumulative. That is, each event is reported only once, on 
the day the event occurs.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
This report displays full details on updates to a [[participant]]’s open positions, including trade creates, 
cancellations, notification of [[settlement]], [[settlement]] Balance Order (SBO) processing updates, [[Novation]], and 
modifies of XREF. Members use the Purchase and Sale Report to validate and balance their bilaterally 
compared trades, as well as monitor subsequent updates made to those trades, versus their internal 
applications. The P&S report is [[SEC]] Rule 10b-10 Compliant (a [[SEC]] requirement of registered [[Broker]]/Dealers 
to provide confirmation to customers) and it serves as binding confirmation of the trade. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual Trade details are listed with the following data. 
  

---

## Page 22

MBSD Operational Clearing Reports Guide 
Purchas e and Sale Report 22 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]  A three-digit  number is assigned to each [[Member]]. 
AGGREGATE NUMBER  A two-character  alphanumeric following the [[participant]] [[ID]], which links an Account [[ID]] 
([[participant]] Symbol) to  the [[participant]] [[ID]]. Every account must be linked to an aggregate 
for risk management and cash [[settlement]] reporting purposes.  
[[participant]] NAME  The name of the [[Member]]. 
[[participant]] SYMBOL  A 4-character identifier, the [[participant]] Symbol  represents the primary level of system 
identification. Trade submission occurs at the account level.  
DATE OF REPORT The date the report was created.  
PASS INDICATOR  AM or PM system pass. MBSD has two system passes. The AM pass is run in the 
afternoon, a nd the PM pass occurs in the evening. To learn more about the timeframes, 
please refer to the MBSD processing Schedule & Timeframes document which may be 
found in the [[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com . 
TBA [[CUSIP]] Header Information 
In addition to the report header, there is a TBA [[CUSIP]] header that contains the following information: 
FIELD  EXPLANATION  
[[settlement]] MONTH  The [[settlement]] month of the [[CUSIP]]. 
[[settlement]] YEAR  The [[settlement]] year of the [[CUSIP]].  
[[CUSIP]]  The nine -character TBA [[CUSIP]]. 
SECURITY CLASS  The security class code of the security reported on the trade (Agency, Product, Cou pon, 
Maturity). 
SECURITY 
DESCRIPTION  
The Agency and Product Code description.  
 
  

---

## Page 23

MBSD Operational Clearing Reports Guide 
Purchas e and Sale Report 23 
Trade Details 
Displays information on each TBA or SPT trade. 
FIELD  EXPLANATION  
ACTIVITY  Activity Type Codes are used to identify the type of activity being reported. The Purchase and 
Sale Report can reference many events, reported as activity types, including:  
• CAN activity type is reported for the members’ compared canceled TBA Trades and 
SPTs.  
• MOD activity type is reported for the members’ modification of their XREF for the ir 
compared TBA Trades and SPTs.  
• NCAN activity type is reported for the members' canceled by Netting TBA Trades.  
• NCRT activity type is reported for the members' netting trade create TBA Trades.  
• NCVT activity type is reported for the members' netting conversion of SBOD trades to 
TFTD Trades on netting.   
• NOV indicates that [[Novation]] has occurred, showing the CTRA field equal to the 
appropriate [[FICC]] [[Novation]] amount . This contra will be reflected on all subsequent 
activities for this trade as well.  
• RCRT indicates this is a replacement trade generated out of the TBA Reprice process; the 
original trade is fully settled via RPCNOS and this replacement trade generated at system 
price.  
• TCR activity type is reported for the members’ compared TBA Trades and SPT s.  
Types of NOS: 
Existing activity “NOS” will be generated as a result of the following new [[Novation]] -related events, 
with control number and pool number as indicated. The events appear in PM version of the P&S 
only, except for SPT conversion to POID which can appear in AM or PM due to real -time (cash) 
trade processing.  
Event CTRL NBR Pool Number Source (times 
approximate) 
AM vs. PM 
Pass 
DNA [[settlement]]  DNANOS  999999  DNA [[settlement]] 
@ 4:30pm  
PM only  
TBA Reprice  RPCNOS  999999  TBA Reprice @ 
4:30pm  
PM only  
Netting -eligible 
PIDs converted to 
POIDs  
FICCNOS  Pool on PID  Daily Pool 
Netting @ 2pm 
(as done today)  
Expanded Pool 
Netting @ 
4:30pm  
PM only  
Non netting-
eligible PIDs 
converted to 
POIDs  
FICCNOS  Pool on PID  Daily Pool 
Netting @ 2pm 
(as done today)  
Expanded Pool 
Netting @ 
4:30pm  
Pool Conversion 
@ 4:30pm  
PM only  

---

## Page 24

MBSD Operational Clearing Reports Guide 
Purchas e and Sale Report 24 
FIELD  EXPLANATION  
Real-Time Pool 
Conversion @ 
real-time  
AM or PM  
SPT trade 
converted to 
POIDs  
SPTNOS  Pool on SPT 
trade  
Pool Conversion 
@ 4:30pm  
PM only  
Real-Time Pool 
Conversion @ 
real-time  
AM or PM  
STIP PIDs 
converted to 
POIDs  
FICCNOS  Pool on PID  Pool Conversion 
@ 4:30pm  
PM only  
Real-Time Pool 
Conversion @ 
real-time  
AM or PM 
 
External-NOS can no longer be submitted by members.  
TRD NUMBER  Trade Number: The trade number is a unique 10- digit number assigned by [[FICC]] to a compared 
trade.   
XREF  The XREF is assigned by the [[Member]] –it’s alphanumeric, extending from 1 to 16 characters in 
length. It must be unique to that [[Member]] –the [[Member]] cannot have any other trades in the 
system with that same XREF.  
TRD STATUS  The Purchas e and Sale Report includes the following trade status types:  
• FMAT trade status type is reported for trades that are Fully Matched. For a dealer -to-dealer 
trade, this means that both the buying and selling dealers have submitted trade details into 
MBSD and  all mandatory matching fields submitted by both have been the same (i.e., have 
matched). For a brokered trade, this means that the [[Broker]] has matched both the buying 
dealer and the selling dealer on the trade.  
• PMAT trade status type is reported for brokered trades that are Partially Matched . This 
means that the [[Broker]] has matched either the buying dealer’s trade submission or the selling 
dealer’s trade submission, but not both. The trade being reported in PMAT status is the side 
that has been matched.  
When the trade status is reviewed in conjunction with activity type, and the trade type, the 
current disposition of the trade can be readily identified.  
Note 
Cancel Requests and Pending Cancels will not appear on the Purchase & Sale report.  
-TYPE-TRD/SUBT  The Purchase and Sale Report includes the following trade types:  
• OPTN trade type is reported for [[Option]]  trades (PUTS/CALL). These must be canceled by 
members to prior to the [[Option]]’s expiry date. Options are not eligible for TBA netting.  
• SBOD trade type is reported (pre -TBA netting) when a [[Member]]’s trade is [[settlement]] 
Balance Order Destined , which is another way of saying that the trade will be included in 
TBA Netting when the TBA netting date for its security class is reached. Status must be 
FMAT to be netted.  

---

## Page 25

MBSD Operational Clearing Reports Guide 
Purchas e and Sale Report 25 
FIELD  EXPLANATION  
• SBON [[obligations]] will be versus the [[FICC]] TBA [[Novation]] account, priced @ system price 
and may be odd -lot value. This is applicable to dealers only.  
• TFTD trade type is reported when the TBA [[CUSIP]] is not netting eligible, one party to 
the trade is not eligible for TBA netting or netting is not desired by either side of the 
trade. It is provided to assist members with distinguishing between TFTD TBA, SPT or 
STIP trades.  
The trade type basically conveys the TBA netting designation of the t rade. Prior to TBA netting, 
the trade type indicates whether a trade is destined for TBA netting or not (meaning it will be 
settled without netting on a trade -for-trade basis). The trade type is also used to identify trades 
in options, which are not eligib le for TBA netting.  
BUY/SELL  Indicates whether the trade is a “buy” or a “sell” from the [[Member]]’s perspective.  
E/D  Entry Date: The entry date for the trade (i.e., the day the [[Member]] submitted the trade to RTTM.)  
T/D  Trade Date: The date the trade was executed between the members.  
M/D  Match Date: The date the trade was bilaterally compared.  
S/D  [[settlement]] Date: The contractual [[settlement]] date of the trade.  
For SBOD and OPTN trades, the date is reflected as the month and year with two zeros  for the 
day (e.g. 07/00/2012). The [[settlement]] date is based on the SIFMA Class of the trade.  
G/U  Give-Up is obsolete since the implementation of MBSD Operational [[Novation]] and thus give -up 
date will be blank.  
CTRA  Contra: Once [[Novation]] occurs, the contra on the trade will now display the appropriate [[FICC]] 
[[Novation]] account. This is applicable to dealer s only.  
BRKR  [[Broker]]: If the trade was brokered, the [[Broker]] [MBSD account symbol] will appear here.  
CMSSN  Commission: Only applies to brokered trades , and even then, it is optional. The commission 
amount listed will be debited from the dealer and credited to the [[Broker]] the month following the 
CSD of a trade on Class B [[settlement]] day.  
DEALER PRICE  This is the price that the dealer submitted on the trade (padded with zeros past the last decimal 
place out to 12 decimal places). For a brokered trade with commission, the dealer may include 
the price either inclusive or exclusive of commission. If the dealer included the price inclusive of 
commission, then  the dealer price will be a different price than the [[settlement]] price.  
PAR VALUE OR 
AMORT AMT  
The par value of the trade (original face) is reported in this f ield.  For specified pool trades, the 
current face is displayed.  
STTL PRICE  [[settlement]] Price: This is the [[settlement]] price of the trade exclusive of commission  prior to 
TBA netting. For SBON activity types, the [[settlement]] price is also found on the P&S report.  
STTL VALUE  [[settlement]] Value: The [[settlement]] value of the trade. This  is equal to the open par multiplied by 
the [[settlement]] price.  
POOL NUMBER  For Specified Pool Trades (only) , the pool number that will be settled for the trade.  
POOL MATURITY 
DATE  
For Specified Pool Trades (SPTs), the maturity date for the pool that will settle for the trade.  
 
  

---

## Page 26

MBSD Operational Clearing Reports Guide 
Purchas e and Sale Report 26 
Print Image Report Sort Order 
The Purchase and Sale Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]]/Security Class = ascending order 
3. T rade Number = ascending order. 
Other Report Formats 
The Purchase and Sale Report is also available in other formats: 
Report Name Afternoon Pass (AM)  Evening Pass (PM)  Format 
Purchase & Sale X X MRO, Tilde delimited  
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the Purchase and Sale 
Report is available in two types: RJE and NDM. All MRO Report layouts can be found in the [[FICC]] MBSD User 
Documentation section of the [[DTCC]] website (http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/[[FICC]]-mbsd-user-
documentation#MachineReadableOutput) Look for: 
• RJE Purchase and Sales Report. (RJE format is grandfathered in for existing members.) 
• NDM Purchase and Sales Report. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist–there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Tilde Delimited Reports 
In this format, fields are separated by a tilde (~). Files in this layout can be imported into Excel and are posted 
to Report Center (extension “.tld”) in the same location as the corresponding PDF. When downloaded, header 
field information is not retained. Tilde-separated reports are generated according to the same rules as with 
Print Image. The tilde-separated file is based on the MRO equivalent, where each row in the tilde contains data 
from various card codes. When a tilde-separated file has no data rows to include (an “empty” file condition), a 
“header” row (card code 01) will be included in the file, followed by a row indicating “no activity”. 
  

---

## Page 27

MBSD Operational Clearing Reports Guide 
Purchas e and Sale Report 27 
Tilde Header Row Information 
The first row in every tilde-separated file is a standard “header” row, as defined below: 
Standard Tilde -Separated File Header Row  
Field Description 
Header Record Card Code  “01”  
Report [[ID]]  Identifier specific to given report  
[[participant]] [[ID]]  3-character [[participant]] [[ID]]  
Aggregate Number  2-character aggregate  
Account  4-character account  
[[participant]] Name  40-character [[participant]] name, as taken from 
Account master files 
Report Date YYYYMMDD 
Tilde Detail Row Information for Purchase and Sale Report 
Tilde “detail” rows contain information from card code 03 (dealer detail), 05 (NOS detail) or 06 ([[Broker]] detail), 
as summarized in the table below.  
Field Type Format Comment Populated for Card Code?  
Card Code  2 N PIC 9(02) 03 (dealer rows), 05 (NOS rows), 
06 ([[Broker]] rows)  
03 05 06 
[[settlement]] Year 4 N  PIC 9(04) Format YYYY    
[[settlement]] Month  2 A/N  PIC X(02) Format MM    
[[CUSIP]] 9 A/N  PIC X(09)     
Account Symbol  4 A/N  PIC X(04)     
Activity Type  6 A/N PIC X(06) CAN, GUP, MOD, NCRT, NCVT, 
NOS, NOV, TCR 
   
Trade Number  10 N  PIC 9(10)     
Internal XREF/ Trade # 15 A/N  PIC X(15)     
Trade Status 4 A/N PIC X(04) CAN, FMAT, PCAN, PMAT    
Trade Type 4 A/N  PIC X(04) OPTN, SBOD, SBON, TFTD   
 
 
Trade Sub-Type  4 A/N PIC X(04) SPT, STIP, TBA    
[[Option]] Type  4 A/N PIC X(04) CALL, PUTS    
Buy/Sell Indicator  1 A/N  PIC X(01) B = Buy, S = Sell   
 
 
Trade Date 8 A/N PIC X(08) Format YYYYMMDD    

---

## Page 28

MBSD Operational Clearing Reports Guide 
Purchas e and Sale Report 28 
Field Type Format Comment Populated for Card Code?  
[[settlement]] Date 8 A/N  PIC X(08) Format YYYYMMDD  
 
 
Match Date 8 A/N PIC X(08) Format YYYYMMDD    
Give-Up Date 8 A/N PIC X(08) Format YYYYMMDD    
Trade Entry Date 8 A/N PIC X(08) Format YYYYMMDD    
Contra Account  4 A/N  PIC X(04)   
 
 
[[Broker]] Account 
Symbol 
4 A/N PIC X(04)     
[[Broker]] Commission  7 N PIC 9(05) 
V9(02) 
    
Buy Dealer Account  4 A/N PIC X(04)     
Buy Dealer 
Commission  
7 N PIC 9(05) 
V9(02) 
    
Buy Dealer Price 15 N PIC 9(03) 
V9(12) 
In decimal     
Sell Dealer Account  4 A/N PIC X(04)     
Sell Dealer 
Commission  
7 N PIC 9(05) 
V9(02) 
    
Sell Dealer Price 15 N PIC 9(03) 
V9(12) 
In decimal     
Trade Price 15 N  PIC 9(03) 
V9(12) 
In decimal     
[[settlement]] Price 15 N  PIC 9(03) 
V9(12) 
In decimal     
Par Value or Amortized 
Value 
13 N  PIC 9(11) 
V9(02) 
 
   
[[settlement]] Value 13 N PIC 9(11) 
V9(02) 
    
Pool Number 9 A/N PIC X(09) 
 
   

---

## Page 29

MBSD Operational Clearing Reports Guide 
Unmatched Margi n Report 29 
UNMATCHED [[Margin]] REPORT 
About the Unmatched [[Margin]] Report 
The Unmatched [[Margin]] Report is generated for dealers only and reflects the details supporting losses (or 
[[Margin]]) associated with [[Broker]] submitted unmatched (or PMAT) [[Broker]]/Dealer trades that have not been DK’d 
by the Dealer. This report does not list all PMAT trades where the [[Member]] is the Uncompared Dealer; it only 
lists those PMAT trades where the [[mark-to-market]] value (or unrealized P&L) is negative, meaning that the 
[[Member]] is being assessed [[Margin]] for the trade.  
Members use the Unmatched [[Margin]] Report to view unresolved [[Broker]]/Dealer Trade Create transactions that 
result in an Unmatched P&L [[Margin]] Requirement. If the [[Member]] disagrees with any of the trades on the report 
or “does not know” them, the [[Member]] should DK the trades and contact the [[Broker]]. Otherwise, the [[Member]] 
should compare the trades. 
Note 
MBSD requires all Clearing Members to deposit [[collateral]] in the form of cash and eligible [[securities]], which is referred to as  
Clearing Fund. The primary purpose of the Clearing Fund is to provide readily accessible [[Liquidity]] to facilitate [[settlement]] 
and reduce loss -related costs which may be incurred in the event of a [[Member]]’s insolvency or failure to fulfill its contractual 
[[obligations]] to MBSD. A [[Member]]’s Clearing Fund requirement is referred to as “[[Margin]].”  
The term “Mark -to-Market” means the aggregate amount of a [[Member]]’s profits and losses calculated by [[The Corporation]].  
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual trade details are listed with the following data. 
  

---

## Page 30

MBSD Operational Clearing Reports Guide 
Unmatched Margi n Report 30 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] 
[[ID]]  
A three-digit  number is assigned to each [[Member]]. 
AGGREGATE 
NUMBER  
A two-character  alphanumeric following the Participan t [[ID]], which links an Account [[ID]] ([[participant]] 
Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk management 
and cash [[settlement]] reporting purposes.  
[[participant]] 
NAME  
The name of the [[Member]]. 
[[participant]] 
SYMBOL  
A 4-charact er identifier, the [[participant]] Symbol  represents the primary level of system identification. 
Trade submission occurs at the account level.  
DATE OF 
REPORT  
The date the report was created.  
PASS 
INDICATOR  
AM or PM system pass. MBSD has two system passes. The AM pass is run in the afternoon, and the 
PM pass occurs in the evening. To learn more about the timeframes, please refer to the MBSD 
processing Schedule & Timeframes document which may be found in the [[participant]] Reference 
Documentation (MBS) section on www.[[DTCC]].com . 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD  EXPLANATION  
MONTH/YEAR  The [[settlement]] month and year of the trade.  
[[CUSIP]]  The nine -character TBA [[CUSIP]].  
SECURITY DESCRIPTION  The agency and type class of security  
Trade Details 
Displays information on each TBA or SPT trade. 
FIELD  EXPLANATION  
TRANSACTION NUMBER  Since this report only lists PMAT trades for which the [[Member]] is the Uncompared Dealer, 
the [[Member]] has not submitted a Trade Instruct to RTTM and as a result, has not been 
assigned a Transaction Number. The Transaction Number listed is the number of the 
[[Broker]]’s submission, which was included in the “Comparison Request” that the 
Uncompared Dealer received.  

---

## Page 31

MBSD Operational Clearing Reports Guide 
Unmatched Margi n Report 31 
FIELD  EXPLANATION  
SERVICE TYPE  • OPTN trade type is reported for [[Option]] trades (PUTS/CALL). These must be 
canceled by members to prior to the [[Option]]’s expiry date. Options  are not eligible 
for TBA netting.  
• SBOD trade type is reported (pre -TBA netting) when a [[Member]]’s trade is 
[[settlement]] Balance Order Destined, which is another way of saying that the trade 
will be included in TBA Netting when the TBA netting date for its [[SEC]] urity class is 
reached. Status must be FMAT to be netted.  
• TFTD trade type is reported when the TBA [[CUSIP]] is not netting eligible, one 
party to the trade is not eligible for TBA netting or netting is not desired by either 
side of the trade.  
Note 
SBON trade s can never be PMAT because they are created as a result of the TBA Netting 
process, therefore SBONs will never appear on this report.  
TRAN STAT  For this report, the Transaction State will always be UMT for Unmatched Trade.  
BUY/SELL  Buy or Sell  
SUB/TYPE The type of TFTD is provided to assist members with distinguishing between TFTD TBA, 
SPT or STIP trades.  The type of OPTN is also provided to assist members with 
distinguishing between PUT and  CALL. 
[[Broker]]  The 4-character symbol for the [[Broker]] c ounterparty.  
MARKET PRICE  The “AM” reports reflect the previous day’s end -of-day process while the “PM” reports 
reflect the current day’s end -of-day price.  
TRADE PRICE  The price of the trade.  
PAR VALUE  The quantity of the trade.  
UNREALIZED P&L  This is the profit or loss of the trade/position. It’s the difference between the market value 
of the trade and the [[settlement]] value of the trade.  
• For “buy” trades, if the market value < [[settlement]] value, the position is in a loss. If 
the market value > s ettlement value, the position is in a profit.  
• For “sell” trades, if the market value < [[settlement]] value, the position is in a profit. 
If the market value > [[settlement]] value, the position is in a loss.  
Note 
Only trades that result in a debit value will ap pear on this report.  
POOL NUMBER  The pool number is only included for Specified Pool Trades. For SPTs, the pool number is 
one of the agreed upon trade terms.  
TBA Footer 
After the trade details for the TBA [[CUSIP]], there is a TBA footer. 

---

## Page 32

MBSD Operational Clearing Reports Guide 
Unmatched Margi n Report 32 
FIELD NAME  EXPLANATION  
CLASS TOTAL  The class total sums all the unrealized P&L amounts for each uncompared trade for that 
TBA [[CUSIP]].  
Report Footer 
At the end of the report there is a report footer. 
FIELD NAME  EXPLANATION  
REPORT TOTAL  The sum of all the unrealized P&L amounts for each uncompared trade for the entire 
report.  
Print Image Report Sort Order 
The Compressed Open Commitment Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]]/Security Class = ascending order 
3. Transaction Number = ascending order. 
Other Report Formats 
The Unmatched [[Margin]] Report is o nly  available in Print-Image (PDF) format. 
Report Name Afternoon Pass (AM)  Evening Pass (PM)  Format 
Unmatched [[Margin]] Report  X X PDF 
 

---

## Page 33

MBSD Operational Clearing Reports Guide 
DNA Report 33 
DNA REPORT 
About the DNA Report 
The DNA Report is produced once daily to allow dealers to track their DNA activity and reconcile [[settlement]] 
value money differences generated by pair-offs.  To learn more about the timeframes of the processes relevant 
to this report, please refer to the MBSD Processing Schedule & Timeframes document which may be found in 
the [[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com. 
This report shows all DNA requests active in the system or processed/cancelled on the current business day.  
For each DNA request, the report shows the DNA status, the individual trades that [[FICC]] assigned to the DNA 
request to1 and any associated money differences (DNA TAP). 
Although this report is produced daily, it will only have data during SIFMA 48hr/24hr, as that is the only period 
in which DNA may be submitted/processed. 
Members use the DNA Report to reconcile their DNA activity and [[settlement]] value differences. 
Note  
Only dealer tr ades are subject to DNA; [[Broker]] s [[DO]] not receive this report.  
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
The report is divided into 3 sections based on DNA request status: 
• Assigned DNA – DNA request has been assigned to specific TBA trades by [[FICC]] and associated 
position excluded from allocation.  However, CSD has not been reached and therefore, DNA is pending 
and may still be canceled.  Assigned DNA requests will appear in this report until they are settled2 or 
canceled by the [[Member]]. 
• Settled DNA – DNA request has been processed and associated TBA position is marked as settled.  In 
addition, DNA TAP (at the aggregate level) has been generated for any price differences.  This is a final 
state for this DNA, and it will no longer appear in subsequent reports. 
 
1 DNA requests may be submitted by members based on “terms-only”, in which case [[FICC]] will select specific 
buy and sell trades to which to assign the DNA request. Members may also provide specific Trade IDs to target 
(“Trade [[ID]] mode”). 
2 DNA requests are processed during the “DNA [[settlement]]/TBA Reprice” process executed on SIFMA 24hr. 

---

## Page 34

MBSD Operational Clearing Reports Guide 
DNA Report 34 
• Canceled DNA – DNA request has been canceled by [[Member]] and the associated TBA position reopened 
for allocation. This is a final state for this DNA, and it will no longer appear in subsequent reports. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]]/Aggregate  A three -digit number is assigned to each [[Member]] followed by a 2- digit number or 
alphanumeric identifier  
Account Description  The account name 
Account [[ID]] The four -character account symbol  
Business Date A date field showing the current business date 
DNA Header Information 
Displays information on the DNA request; 1 per DNA request. 
FIELD  EXPLANATION  
S/D A date field showing the Contractual [[settlement]] date 
TBA [[CUSIP]] The TBA [[CUSIP]] on the DNA request  
SECURITY CLASS An alphanumeric description of the TBA [[CUSIP]]  
DNA# DNA identifier assigned by system to this request  
DNA REF DNA reference assigned by [[Member]] to this request  
DNA PAR Par amount assigned to this DNA request  
DNA Trade Assignment Details 
Displays information on each trade assigned to the DNA request. 
FIELD  EXPLANATION  
TRD # The Trade [[ID]] number  
TRD TYP Trade Type – TFTD or SBON 
B/S BUY or SELL 
T/D Trade Date 
S/D Contractual [[settlement]] Date 
PRICE Trade price 
ORIG TRD PAR Original trade par  

---

## Page 35

MBSD Operational Clearing Reports Guide 
DNA Report 35 
FIELD  EXPLANATION  
DNA PAR Amount of par targeted for DNA  
DNA STTL VALUE [[settlement]] value of DNA’ed par based on price 
DNA Request Sub-Totals 
Displays sub-total information for each DNA request; 1 per DNA request. 
FIELD NAME  EXPLANATION  
DNA TAP Within a DNA request, sum of all SELL “DNA STTL VALUE” minus sum of all BUY “DNA STTL 
VALUE”.  In other words, sell [[settlement]] values are positive, and buy [[settlement]] values are 
negative.  
DNA Request Section Sub-Totals 
Displays sub-total information for each report section (assigned, settled, canceled); 3 per report. 
FIELD NAME  EXPLANATION  
TOTAL DNA TAP Sum of all “DNA TAP” within report section  
Print Image Report Sort Order 
The DNA Report (sections) are sorted as follows: 
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

## Page 36

MBSD Operational Clearing Reports Guide 
DNA Report 36 
Other Report Formats 
The DNA Report is also available in MRO format. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO NDM DNA Status format of the 
DNA Report can be found at http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist–there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Difference between MRO and Print-image DNA Report 
The values reported in the .pdf format should be the same as values reported in MRO.  

---

## Page 37

MBSD Operational Clearing Reports Guide 
MBSCC/EPN Message D etail Report 37 
MBSCC/EPN MESSAGE DETAIL REPORT 
About the MBSCC/EPN Message Detail Report 
The MBSCC/EPN Message Detail Report displays the details of all messages sent and received. It is available 
in Report Center as a text (.txt) file viewable within your web browser (from which it may also be printed). 
Members may view the report after batch close of business (COB) and end-of-day ([[EOD]]) passes. These 
reports are labeled (respectively) as the MBSCC/EPN Message Detail Report C and the MBSCC/EPN 
Message Detail Report E. 
Report Section/Layout Information 
As mentioned above the MBSCC/EPN Message Detail Report is only available in text (.txt) format. What 
follows is a breakdown of the layout (including field descriptions) of the report as viewed in a web browser. 
Report Layout/Field Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  REFERENCE 
[[participant]] EPN [[participant]] [[ID]]    
AGGREGATE EPN aggregate [[ID]]    
ACCOUNT NAME EPN account name Free form up to 40 
characters  
ACCOUNT SYMBOL EPN Account [[ID]]  of report requester  XXXX format 
REPORT DATE Date of the requested report  MM/DD/YY format  
CB/ED INDICATOR Indicates close -of-business or end -of-day batch 
cycle  
CB or ED 
[[settlement]] MONTH/YEAR  [[settlement]] month and year of the proceeding 
messages  
MM/YY format  
TBA [[CUSIP]] Indicates product, agency, coupon, maturity, 
[[settlement]] month, check digit  
XXXXXXXXX format  
BOUND INDICATOR Indicates inbound or outbound section Inbound or Outbound 
MSG TYPE/SENT OR RECEIVED Indicates sent or received by message type ON, DK, CC, CX, and Sent 
or Received (e.g., ON 
Sent) 
MSG TYPE Indicates message type ON, DK, CC, and CX  
MSG [[ID]] EPN assigned message [[ID]]  99999999999 format  
CONTRA EPN Account [[ID]]  of message contra party  XXXX format 

---

## Page 38

MBSD Operational Clearing Reports Guide 
MBSCC/EPN Message Detail Report 38 
FIELD  EXPLANATION  REFERENCE 
ORIG TRD PAR Par value of the original trade 999,999,999.99 format  
PRICE [[settlement]] price 999.999999999 format  
GDMM Number of good delivery million dollar lots delivered 
in accordance with SIFMA standards  
9999 format 
T/D Trade date MM/DD/YY format  
S/D [[settlement]] Date MM/DD/YY format  
D/D Delivery date MM/DD/YY format  
INT [[ID]] Unique reference number entered by the submitter  
(displayed only to the submitter)  
Free form up to 16 
characters  
BKR CD EPN Subaccount field associated with the EPN 
message. 
Up to 4 alphanumeric 
characters  
RSN CD Reason code for the action taken, DK or 
cancellation 
9999 format 
TGT MSG (Target Message [[ID]]) Message [[ID]] referencing the 
original message being DK’d or canceled  
99999999999 format  
XREF Tag number assigned by the submitter (displayed 
only to the submitter of the message)  
Free form up to 15 
characters  
SPEC INST Informational trade terms  Free form up to 30 
characters  
T1 T1 is applied when the complete message is 
received for processing.  
HH:MM:SS format  
T2 After the message has passed all edits and is 
processed by the Message Processor, the T2 stamp 
is applied. The T2 timestamp is used to determine 
good delivery.  
HH:MM:SS format  
T3 T3 is applied to the message when it is sent to the 
outbound table by the Message Processor.  
HH:MM:SS format  
T4 T4 represents the time the message is stored 
internally by the Message Processor.  
HH:MM:SS format  
T5 T5 represents the time a message is written to the 
outbound table by the Output Formatter.  
HH:MM:SS format  
# POOLS Number of pools contained within this message 9999 format 
POS DUP EPN’s indication that output message may be a 
duplicate 
X = yes, blank = no  
LOT [[ID]] Lot-sequence of good delivery million pool(s)  XXXXXX format  
POOL Pool number  XXXXXXX format  
ORIG FACE Principal amount of MBS at date of issue 999,999,999 format  

---

## Page 39

MBSD Operational Clearing Reports Guide 
MBSCC/EPN Message D etail Report 39 
FIELD  EXPLANATION  REFERENCE 
COUPON Rate of interest recorded on the face of the 
certificate  
99.9999 format  
M/D Maturity date of the mortgage pool  MM/DD/YY format  
N (NEW ISSUE) Identifies a new pool issue  X = yes, blank = no  
TRADE # MBSD trade number  XXXXXXXXXX format  
CONTROL # Individual pool detail reference number assigned by 
the user 
Free form up to 15 
characters  
CURRENT (FACE) The outstanding principal of the mortgage  999,999,999.99 format  
FACTOR Percentage of original principal of the mortgage  9.999999999 format  
[[CUSIP]] Pool [[CUSIP]] number  XXXXXXXXX format  
I/D (Issue date) Date the mortgage pool was issued  MM/DD/YY format  
TERM(INATOR) Value of good delivery MMs of the preceding lot  9999 format ( Odd  lot = 
‘9999’ 
PRINCIPAL The monthly principal payment accrued to the pool 
delivered  
999,999,999.99 format  
INTEREST Interest accrued on the balance 999,999,999.99 format  
NET MONEY Net money  999,999,999.99 format  
SPEC INST Informational pool detail items Free form up to 30 
characters  
 
MSG TYPE/SENT OR RECEIVED 
TOTALS 
Message type/sent or received section totals of 
original face, current face, principal, interest and net 
money  
 
BOUND TOTALS Inbound or outbound section totals by message type 
(also totals number of messages)  
 
TBA [[CUSIP]] TOTALS TBA [[CUSIP]] totals or original face and net money by 
message type (also totals number of messages)  
 
Report Sort Order 
The MBSCC/EPN Message Detail Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]] = ascending order 
3. Bound (In/Out) Section = ascending order 
4. Message Type = ascending order 
5. Message [[ID]] = ascending order 
6. Contra = ascending order. 

---

## Page 40

MBSD Operational Clearing Reports Guide 
MBSCC/EPN Message D etail Report 40 
Other Report Formats 
The MBSCC/EPN Message Detail Report is only available in .txt (text) format. 
Report Name Batch COB  End-of-Day ([[EOD]]) Format 
MBSCC/EPN Message Detail Report  C X  .txt 
MBSCC/EPN Message Detail Report E   X .txt 
 

---

## Page 41

MBSD Operational Clearing Reports Guide 
MBSCC/EPN Message Summary Report 41 
MBSCC/EPN MESSAGE SUMMARY REPORT 
About the MBSCC/EPN Message Summary Report 
The MBSCC/EPN Report displays summary information for all messages sent and received. It is available in 
Report Center as a text (.txt) file viewable within your web browser (from which it may also be printed). 
Members may view the report after batch close of business (COB) and end-of-day ([[EOD]]) passes. These 
reports are labeled (respectively) as the MBSCC/EPN Message Summary Report C and the MBSCC/EPN 
Message Summary Report E. 
Report Section/Layout Information 
As mentioned above the MBSCC/EPN Message Summary Report is only available in text (.txt) format. What 
follows is a breakdown of the layout (including field descriptions) of the report as viewed in a web browser. 
Report Layout/Field Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  REFERENCE 
[[participant]] EPN [[participant]] [[ID]]    
AGGREGATE EPN aggregate [[ID]]    
ACCOUNT NAME EPN system account name Free form up to 40 
characters  
ACCOUNT SYMBOL EPN Account [[ID]]  of report requester  XXXX format 
REPORT DATE Date of the requested report  MM/DD/YY format  
CB/ED INDICATOR Indicates close -of-business or end -of-day batch cycle CB or ED 
[[settlement]] 
MONTH/YEAR 
[[settlement]] month and year of the proceeding messages  MM/YY format  
TBA [[CUSIP]] Indicates product, agency, coupon, maturity, [[settlement]] 
month, check digit  
XXXXXXXXX format  
CONTRA EPN Account [[ID]] of message contra party  XXXX format 
(MESSAGE) TYPE Indicates message type ON, DK and CX 
MSGS RECD The number of messages received during the day for each 
message type 
9999999 format  
ORIG FACE (RECD)  The principal amount of MBS at date of issue of all 
messages received during the day for each message type 
9,999,999,999,999 format  
NET MONEY (RECD)  Net money input for all messages received during the day 
for each message type 
9,999,999,999,999.99 
format 

---

## Page 42

MBSD Operational Clearing Reports Guide 
MBSCC/EPN Message Summary Report 42 
FIELD  EXPLANATION  REFERENCE 
MSGS SENT The number of messages sent during the day for each 
message type 
9999999 format  
ORIG FACE (SENT)  The principal amount of MBS at date of issue of all 
messages sent during the day for each message type 
9,999,999,999,999 format  
NET MONEY (SENT)  Net money input for all messages sent during the day for 
each message type 
9,999,999,999,999.99 
format 
TBA [[CUSIP]] TOTALS TBA [[CUSIP]] totals of original face and net money by 
message type (also totals number of messages)  
  
Report Sort Order 
The MBSCC/EPN Message Summary Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]] = ascending order 
3. Contra = ascending order 
4. Message Type = ascending order. 
Other Report Formats 
The MBSCC/EPN Message Summary Report is only available in .txt (text) format. 
Report Name Batch COB End-of-Day ([[EOD]]) Format 
MBSCC/EPN Message Summary Report C  X  .txt 
MBSCC/EPN Message Summary Report  E  X .txt 

---

## Page 43

MBSD Operational Clearing Reports Guide 
Open Commitment Summary Report 43 
OPEN COMMITMENT SUMMARY REPORT 
About the Open Commitment Summary Report 
The Open Commitment Report is produced on every business date to reflect all matched, unsettled (or open) 
positions on [[FICC]]’s books for a given [[Member]]. This report is cumulative. A trade/position will appear on the 
OCR f rom the first system pass in which it was matched. 
Members refer to the Open Commitment Summary Report if they are only interested in overall totals. No 
individual trade information is provided on the Summary OCR. The positions listed on the Summary OCR are 
the TBA positions guaranteed and risk managed by [[FICC]]. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”. 
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, TBA [[CUSIP]] totals are presented as shown in the following 
tables. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]  A three-digit  number is assigned to each [[Member]]. 
AGGREGATE NUMBER  A two-character  alphanumeric following the [[participant]] [[ID]], which links an Account 
[[ID]] ([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an 
aggregate for risk management and cash [[settlement]] reporting purposes.  
[[participant]] NAME  The name of the [[Member]]. 
[[participant]] SYMBOL  A 4-character identifier, the [[participant]] Symbol  represents the primary level of 
system identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was created.  

---

## Page 44

MBSD Operational Clearing Reports Guide 
Open Commitment Summary Report 44 
FIELD  EXPLANATION  
PASS INDICATOR  AM or PM sys tem pass. MBSD has two system passes. The AM pass is run in the 
afternoon, and the PM pass occurs in the evening. To learn more about the 
timeframes, please refer to the MBSD processing Schedule & Timeframes 
document which may be found in the [[participant]] R eference Documentation (MBS) 
section on www.[[DTCC]].com . 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD  EXPLANATION  
[[settlement]] MONTH  The [[settlement]] month of the [[CUSIP]]. 
[[settlement]] YEAR  The [[settlement]] year of the [[CUSIP]].  
[[CUSIP]]  The nine -character TBA [[CUSIP]]. 
SECURITY CLASS  The security class code of the security reported on the trade (Agency, Product, 
Coupon, Maturity).  
SECURITY DESCRIPTION  The Agency and Product Code description.  
MARKET PRICE  Unless the price changes, the “AM” reports reflect the previous day’s end -of-day 
process while the “PM” reports reflect the current day’s end -of-day price. 
TBA [[CUSIP]] Totals 
As there are no individual trade details on the Open Commitment Summary Report, the next section displays 
TBA [[CUSIP]] totals. 
FIELD NAME  EXPLANATION  
BUY OPEN PAR  This is the sum of the open par for all buy positions for the TBA [[CUSIP]] and S/D.  
SELL OPEN PAR  This is the sum of the open par for all sell positions for the TBA [[CUSIP]] and S/D.  
NET OPEN PAR  This is the net of the buy and sell open par for the TBA [[CUSIP]] and S/D.  
BUY STTL VALUE  This is the sum of the [[settlement]] values for all buy positions for the TBA [[CUSIP]] 
and S/D.  
SELL STTL VALUE  This is the sum of the [[settlement]] values for all see positions for the TBA [[CUSIP]] 
and S/D.  
NET STTL VALUE  This is the net of the buy and sell [[settlement]] values for the TBA [[CUSIP]] and S/D.  
BUY P&L  This is the sum of the Profit/Loss for all buy positions  for the TBA [[CUSIP]] and S/D.  
SELL P&L  This is the sum of the Profit/Loss for all sell positions for the TBA [[CUSIP]] and S/D.  
NET P&L  This field reflects the net of the “buy and sell” P/L calculations. (C R=Credit, 
DR=Debit)  

---

## Page 45

MBSD Operational Clearing Reports Guide 
Open Commitment Summary Report 45 
Report Footer 
At the end of the report there is a report footer that provides overall position buy and sell totals as follows: 
FIELD NAME  EXPLANATION  
BUY FORWARD ITEMS  The number of buy trades with a [[settlement]] date greater than the day of the report.  
BUY FORWARD OPEN 
PAR  
The sum of the open par of the buy trades with a [[settlement]] date greater than the day of the 
report.  
BUY FORWARD STTL 
VALUE  
The sum of the [[settlement]] value of the buy trades with a [[settlement]] date greater than the day 
of the report.  
BUY FAIL ITEMS  The number of buy trades with a [[settlement]] less than or equal to the date of the report.  
BUY FAIL OPEN PAR  The sum of the open par of the buy trade s with a [[settlement]] date less than or equal to the day 
of the report.  
BUY FAIL STTL VALUE  The sum of the [[settlement]] value of the buy trades with a [[settlement]] date less than or equal to 
the day of the report.  
BUY TOTAL OPEN 
PAR  
The sum of the open par  of all buy trades.  
BUY TOTAL STTL 
VALUE  
The sum of the [[settlement]] value of all buy trades.  
SELL FORWARD 
ITEMS  
The number of sell trades with a [[settlement]] date greater than the day of the report.  
SELL FORWARD 
OPEN PAR  
The sum of the open par of the sell trades with a [[settlement]] date greater than the day of the 
report.  
SELL FORWARD STTL 
VALUE  
The sum of the [[settlement]] value of the sell trades with a [[settlement]] date greater than the day 
of the report.  
SELL FAIL ITEMS  The number of sell trades with a [[settlement]] less than or equal to the date of the report.  
SELL FAIL OPEN PAR  The sum of the open par of the s ell trades with a [[settlement]] date less than or equal to the day 
of the report.  
SELL FAIL STTL 
VALUE  
The sum of the [[settlement]] value of the sell trades with a [[settlement]] date less than or equal to 
the day of the report.  
SELL TOTAL OPEN 
PAR  
The sum of the open par of all sell trades.  
SELL TOTAL STTL 
VALUE  
The sum of the [[settlement]] value of all sell trades.  
NET FORWARD OPEN 
PAR  
The difference between the total buy and sell open par for trades with a [[settlement]] date 
greater than the date of the report.  
NET FORWARD STTL 
VALUE  
The difference between the total buy and sell [[settlement]] values for trades with a [[settlement]] 
date greater than the date of the report.  
NET FAIL OPEN PAR  The difference between the total buy and sell open par for trades with a [[settlement]] date less 
than or equal to the date of the report.  

---

## Page 46

MBSD Operational Clearing Reports Guide 
Open Commitment Summary Report 46 
FIELD NAME  EXPLANATION  
NET FAIL STTL VALUE  The difference between the total buy and sell [[settlement]] values for trades with a [[settlement]] 
date less than or equal to the date of the report.  
TOTAL NET O PEN 
PAR  
The difference between the total buy and sell open par for all trades listed on the OCR.  
TOTAL NET STTL 
VALUE  
The difference between the total buy and sell [[settlement]] values for all trades listed on the 
OCR.  
Print Image Report Sort Order 
The Open Commitment Summary Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]]/Security Class = ascending order 
Other Report Formats 
The Open Commitment Summary Report is also available in MRO format. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the Open Commitment 
Summary Report is available in two types: RJE and NDM. All MRO Report layouts can be found in the [[FICC]] 
MBSD User Documentation section of the [[DTCC]] website (http://www.[[DTCC]].com/clearing-services/[[FICC]]-
mbsd/[[FICC]]-mbsd-user-documentation#MachineReadableOutput) Look for: 
• RJE Open Commitment Summary Report. (RJE format is grandfathered in for existing members.) 
• NDM Open Commitment Summary Report. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist–there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Difference between MRO and Print Image Open Commitment Summary Report 
The values reported in the .pdf format should be the same as values reported in MRO. 

---

## Page 47

MBSD Operational Clearing Reports Guide 
TBA Net D etail Report 47 
TBA NET DETAIL REPORT 
About the TBA Net Detail Report 
The first detail you will notice when opening the TBA Net Detail Report in the RTTM® MBS Report Center is 
that the title of the report appears as “TBA Netting Recap Report.” Nonetheless, we will be referring to it by the 
name which appears in the report list (links) under MBS Clearing reports. The TBA Net Detail Report is 
produced on 72-hour day as prescribed by the SIFMA Calendar and reflects results of TBA Net, which includes 
SBOD trades into the net, associated TBA TAP and resulting SBON [[obligations]] versus FTBA at system price.  
To learn more about the timeframes of the processes relevant to this report, please refer to the MBSD 
Processing Schedule & Timeframes document which may be found in the [[participant]] Reference 
Documentation (MBS) section on www.[[DTCC]].com.  
This report allows members to view the [[settlement]] Balance Order Destined (SBOD) that were designated for 
TBA netting and the final net TBA [[settlement]] [[obligations]] designated as [[settlement]] Balance Order (SBON) 
positions. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
This report details the SBOD trades considered in the TBA Net, and resulting SBON [[obligations]], grouped by 
[[settlement]] month/year and TBA [[CUSIP]]. Within each section, the original SBOD trade are listed, followed by 
resulting SBONs.  
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]/Aggregate [[ID]]  A three -digit number is assigned to each [[Member]] followed by a 2-digit  number or 
alphanumeric identifier  
Account Description  The account name 

---

## Page 48

MBSD Operational Clearing Reports Guide 
TBA Net D etail Report 48 
FIELD  EXPLANATION  
Account [[ID]] The four -character account symbol  
Business Date A date field showing the current business date 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD  EXPLANATION  
[[settlement]] Month/Year  [[settlement]] month and year  
TBA [[CUSIP]] Nine-digit alphanumeric To Be Announced [[CUSIP]]  
SECURITY CLASS Description of this TBA [[CUSIP]]  
[[settlement]] Price System price associated with this TBA [[CUSIP]], which is equal to prior -day [[EOD]] price 
Original SBOD Trades 
Displays information on each SBOD. 
FIELD  EXPLANATION  
TRADE NBR Trade number on SBOD trade 
TRADE XREF XREF on SBOD trade  
TYPE Always equal to “SBOD”  
B/S B or S (Buy or Sell)   
S/D Contractual [[settlement]] Date, which for SBOD has “00” as day  
CONTRA Contra on the trade, equal to [[FICC]]’s TBA [[Novation]] Account (FTBA)  
PAR Par of the SBOD Trade  
TRADE PRICE Price, exclusive of commission  
TRADE MONEY [[settlement]] Amount, based on trade price 
STTL PRICE [[settlement]] price for this TBA [[CUSIP]]  
STTL MONEY [[settlement]] Amount, based on STTL PRICE  
TBA TAP Transaction Adjustment Payment (TAP) associated with this SBOD trade  
CR/DR Indicator  “CR” for credit, “DR” for debit for TBA TAP  
  

---

## Page 49

MBSD Operational Clearing Reports Guide 
TBA Net D etail Report 49 
Resulting SBON 
Displays information on each SBON created. 
FIELD NAME  EXPLANATION  
TRADE NBR Trade number on SBON obligation  
TYPE Always equal to “SBON”  
B/S B or S (Buy or Sell)  
S/D Contractual [[settlement]] Date 
CONTRA Contra on the trade, equal to [[FICC]]’s TBA [[Novation]] Account (FTBA)  
PAR Par of the SBON Trade  
STTL PRICE [[settlement]] price on this SBON  
STTL MONEY [[settlement]] Amount based on the SBON’s STTL RPICE  
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
Note 
• “Net Long/Short” of SBOD and SBON sections should alway s be equal 
• “Net Sttl Money” + “Total TAP” should always equal “Net Trade Money”  
  

---

## Page 50

MBSD Operational Clearing  Reports Guide 
TBA Net D etail Report 50 
Print Image Report Sort Order 
The TBA Net Detail Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]] = ascending order 
 
For SBOD/SBON trades: 
1. Trade Number = ascending order. 
Other Report Formats 
The TBA Net Detail Report is also available in other formats: 
Report Name Afternoon Pass (AM)  Evening Pass (PM)  Format 
TBA Net Detail  X  MRO, Tilde delimited  
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format can be found at 
http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbs-[[Novation]]-documentation. 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist–there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Tilde Delimited Reports 
Tilde Delimited Reports are also available via Report Center (right next to the Print Image (.pdf) reports). Tilde 
Delimited Reports may be downloaded into Excel (or a similar program) to allow their data to be manipulated, 
similarly to .CSV (Comma Separated Value) files. When downloaded, header field information is not retained. 
The tilde-separated file is based on the MRO equivalent, where each row in the tilde contains data from various 
card codes and therefore has been updated to confirm to the MRO changes. Each tilde-separate file begins 
with a “header” row followed by “detail” rows containing information from card code 02 (trade SBOD detail) or 
03 (obligation SBON detail), as summarized in the tables below.   
  

---

## Page 51

MBSD Operational Clearing Reports Guide 
TBA Net D etail Report 51 
Tilde Header Row Information 
The first row in every tilde-separated file is a standard “header” row, as defined below: 
Standard Tilde -Separated File Header Row  
Field Description 
Header Record Card Code  “01”  
Report [[ID]]  Identifier specific to given report  
[[participant]] [[ID]]  3-character [[participant]] [[ID]]  
Aggregate Number  2-character aggregate  
Account  4-character account  
[[participant]] Name  40-character [[participant]] name, as taken from Account master files 
Report Date YYYYMMDD 
Tilde Detail Row Information for TBA Net Detail Report 
Field Type Format Comment Populated for Card Code?  
Card Code  2 N 02 (trade detail), 03 (obligation record)  02 03 07 
[[settlement]] Year 4 N  Format YYYY    
[[settlement]] Month  2 A/N  Format MM    
TBA [[CUSIP]]  9 A/N      
Account Symbol   4 A/N      
Trade Number   10 N      
Internal XREF/ Trade #  15 A/N    
 
 
Trade Type  4 A/N  SBOD, SBON    
Buy/Sell Indicator   1 A/N  B = Buy, S = Sell     
[[settlement]] Date  8 A/N  Format YYYYMMDD, where DD is “00” 
for “02” card codes  
  
 
Contra Account  4 A/N      
Par Value 13 N  Format 11.2    
Trade Price 15 N  In decimal, format 3.12    
Trade Money  13 N  Format 11.2    
[[settlement]] Price 15 N  In decimal, format 3.12   
 
[[settlement]] Money  13 N  Format 11.2    
TBA TAP 13 N  Format 11.2    
TBA TAP CR/DR  1 A TBA TAP indicator (C=Credit, D=Debit)     

---

## Page 52

MBSD Operational Clearing Reports Guide 
Netting Conv ersion Report 52 
NETTING CONVERSION REPORT 
About the Netting Conversion Report 
The Netting Conversion Report is produced on each TBA netting date to notify the unmatched dealer side of a 
partially matched (PMAT) SBO destined trade that has been converted to a trade-for-trade (TFTD) transaction 
to facilitate matching. 
Prior to TBA netting, some dealer members will have partially matched transactions with brokers. As these 
transactions have not been fully matched, they are not eligible for TBA netting and the matched side of every 
PMAT trade is converted by the system to a trade-for-trade (TFTD) transaction. While the conversion of the 
matched dealer’s side is reported on the [[Member]]’s P&S report, the unmatched dealer’s side is not. This report 
is used to notify the unmatched dealer of any SBOD advisories that have been converted to TFTD advisories. 
The unmatched dealer would use this report to match the newly created TFTD trades. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual Netting Conversion details are listed with the 
following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]  A three-digit  number is assigned to each [[Member]]. 
AGGREGATE NUMBER  A two-character  alphanumeric following the [[participant]] [[ID]], which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an 
aggregate for risk management and cash [[settlement]] reporting purposes.  
[[participant]] NAME  The name of the [[Member]]. 

---

## Page 53

MBSD Operational Clearing Reports Guide 
Netting Conv ersion Report 53 
FIELD  EXPLANATION  
[[participant]] SYMBOL  A 4-character identifier, the [[participant]] Symbol  represents the primary level of system 
identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was creat ed. 
PASS INDICATOR  AM or PM system pass. MBSD has two system passes. The AM pass is run in the 
afternoon, and the PM pass occurs in the evening. To learn more about the 
timeframes, please refer to the MBSD processing Schedule & Timeframes document 
which may be found in the [[participant]] Reference Documentation (MBS) section on 
www.[[DTCC]].com . 
TBA [[CUSIP]] Header Information 
Within each section, displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] 
included in this section. 
FIELD  EXPLANATION  
[[settlement]] MONTH  AND 
YEAR 
The [[settlement]] month and year of the [[CUSIP]] in format MM/YYYY. 
[[CUSIP]]  The nine -character TBA [[CUSIP]]. 
SECURITY CLASS  The security class code of the security reported on the trade (Agency, Product, 
Coupon, Maturity).  
SECURITY DESCRIPTION  The Agency and Product Code description.  
Trade Details 
Displays information on each TBA trade. 
FIELD  EXPLANATION  
TRAN TYPE  The Transaction Type indicator code identifying the MBSD transaction number.  
STATUS  Transaction status. This will indicate that the transaction is unmatched (UMT) and 
was converted to TFTD.  
TRAN NUMBER  The MBSD transaction number.  
TRADE NUMBER  The MBSD trade number. This will always be blank for Dealer members.  
[[Buyer]]  The [[Buyer]]’s Account [[ID]] .  
[[Seller]]  The [[Seller]]’s Account [[ID]] .  
 
  

---

## Page 54

MBSD Operational Clearing Reports Guide 
Netting Conv ersion Report 54 
Print Image Report Sort Order 
The Netting Conversion Report is sorted as follows: 
1. [[settlement]] Month/Year = earliest to latest 
2. TBA [[CUSIP]]/Security Class = ascending order 
3. Transaction Number = ascending order. 
Other Report Formats 
The Netting Conversion Report is not available in other formats. 
Report Name Afternoon Pass (AM)  Evening Pass (PM)  Format 
Netting Conversion Repor t   X PDF 
 

---

## Page 55

MBSD Operational Clearing Reports Guide 
Cash [[settlement]] D etails Report 55 
CASH [[settlement]] DETAILS REPORT 
About the Cash [[settlement]] Details Report 
This report displays Cash [[settlement]] Detail for a specific [[participant]]/aggregate with due date greater than 
today . The Cash [[settlement]] Detail Report includes the totals for cash obligation items (COIs) that are collected 
in the daily automated Cash [[settlement]] process. [[FICC]] collects all the COIs at the aggregate level. 
Members use the Cash [[settlement]] Details Report to view a current (or a future) day’s Cash [[settlement]]. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF  file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
There are no activity or status codes associated with the Cash [[settlement]] Details Report. Unlike other reports, 
line items are divided between the left (CR or Credit) and right (DR or Debit) sides of the report 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
DATE OF REPORT / 
PASS INDICATOR  
The date the report was created.  
AM or PM s ystem pass. MBSD has two system passes. The AM pass is run in the afternoon, a nd 
the PM pass occurs in the evening. To learn more about the timeframes, please refer to the 
MBSD processing Schedule & Timeframes document which may be found in the [[participant]]  
Reference Documentation (MBS) section on www.[[DTCC]].com . 
[[participant]]  A three-digit  number is assigned to each [[Member]]. 
AGGREGATE A two-character  alphanumeric following the [[participant]] [[ID]], which links an Account [[ID]] ([[participant]] 
Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate for risk management 
and cash [[settlement]] reporting purposes.  
DUE DATE  Date by which members can expect the Cash [[settlement]] balance to be debited or credited by 
cutoff time. 

---

## Page 56

MBSD Operational Clearing Reports Guide 
Cash [[settlement]] D etails Report 56 
Cash Obligation Header Information 
Within each section, displays information on Cash [[obligations]] items that are due to settle on the referenced 
due date. 
FIELD  EXPLANATION  
CSI (aka COI) TYPE  CSI stands for “Cash [[settlement]] Item” and COI stands for “Cash Obligation Item”  
CSI TYPE EXPLANATION 
TBA TBA Transaction Adjustment Payments  
DNA DNA Transaction Adjustment Payments  
TAP Pool Transaction Adjustment Payments  
EXP Expanded Pool Net Transaction Adjustment Payments  
RPC TBA Re-price Transaction Adjustment Payments  
VAR Variance Transaction Adjustment Payment   
FAC Factor Update Adjustment  
CLA Clearance Adjustment  
PRN Principal Payments  
INT Interest Payments  
CMS [[Broker]] Commissions  
FEE MBSD Billing Fee  
TMP TMPG charges  
CPR CPR Claims  
TMF TMPG Financing Amounts  
MIS Miscellaneous from TBA Clearing  
MSC Miscellaneous from Pool Netting  
MSE Miscellaneous from EPN  
TEM Full-month interest for TBA fail  
ATM Fail TBA interest adjust for CSD month  
PEM I in P&I 
ALM Fail pool interest adjust for CSD month 
APM Adjust to par for principal paid  
TIM TBA fail interest for current month  
PIM Pool fail interest for current month 
PFM Pool fail mark excluding interest  

---

## Page 57

MBSD Operational Clearing Reports Guide 
Cash [[settlement]] D etails Report 57 
FIELD  EXPLANATION  
MFM TBA fail mark excluding interest  
MTM Forward mark for TBA  
PTM Pool TAP mark  
MGN TBA (or any Miscellaneous TAP with a future due date)  
MGR [[Margin]] Tap Return  
MGI [[Margin]] Tap Return Interest  
MRR Mark Return 
MRI Mark Return Interest  
SIFMA CLS  SIFMA Class: The SIFMA established contractual [[settlement]] date of the TBA trade. (A, B, C, 
D) 
[[settlement]] 
AMOUNT  
The dollar value of Cash Obligation Item (reconcile this amount).  
CR/DR  Debit or Credit Indicator. DR = Debit. CR = Credit. 
 
Report Footer 
At the end of the report there is a report footer that provides total cash [[settlement]] totals as follows: 
FIELD NAME  EXPLANATION  
TOTAL CASH [[settlement]]  Net of all Cash [[obligations]]  
Print Image Report Sort Order 
The Cash [[settlement]] Details Report is sorted as follows: 
1. [[participant]] and Aggregate 
2. Due Date 
3. CSI Type. 
Other Report Formats 
The Cash [[settlement]] Details Report is not available in other formats. 
Report Name Afternoon Pass (AM)  Evening Pass (PM)  Format 
Cash [[settlement]] Details Report   X MRO, PDF 
 

---

## Page 58

MBSD Operational Clearing Reports Guide 
[[Broker]] Commission Fees Report 58 
[[Broker]] COMMISSION FEES REPORT 
Report Summary 
The [[Broker]] Commission Fees Report is used to view [[Broker]]/dealer trade detail that determines this month’s 
commission fee for trades settling in the current month. It becomes available on the last business day of the 
month during the PM pass. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual [[Broker]] Commission Fee details are listed with 
the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]  A three -digit number is assigned to each [[Member]].  
AGGREGATE NUMBER  A two-character alphanumeric following the [[participant]] [[ID]], which link s an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate 
for risk management and cash [[settlement]] reporting purposes.  
[[participant]] NAME  The name of the [[Member]]. 
[[participant]] SYMBOL  A 4-character identifier, the [[participant]] Symbol  represents the primary level of system 
identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was created.  
PASS INDICATOR  AM or PM system pass. MBSD has two syst em passes. The AM pass is run in the 
afternoon, and the PM pass occurs in the evening. To learn more about the timeframes, 
please refer to the MBSD processing Schedule & Timeframes document which may be 
found in the [[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com .  

---

## Page 59

MBSD Operational Clearing Reports Guide 
[[Broker]] Commission Fees Report 59 
Trade Details 
Displays [[Broker]]/dealer trade details for TBA or SPT trades as of the end of a given month. 
FIELD  EXPLANATION  
CONTRA ACCT MBSD Dealer [[participant]] Symbol  
B/S Buy/Sell Indicator: B – Buy; S – Sell  
STTL MTH [[settlement]] month of the trade  
STTL YR [[settlement]] year of the trade 
[[CUSIP]] TBA [[CUSIP]]: Product, Agency, Coupon, Maturity, [[settlement]] month, Check digit 
SECURITY CLASS MBSD security class code: Agency, Product, Coupon, Maturity  
TRADE DATE Trade date 
TRADE NUMBER MBSD trade number  
XREF Your internal trade reference number  
PAR Par value of the trade 
DEALER PRICE Dealer price +/- Commission  
[[settlement]] PRICE [[settlement]] price of TBA trade 
COMMISSION Dollar value of commission  
TOTAL COMMISSION FOR 
DEALER 
For specific dealer , the total commission payable  
Report Totals 
At the end of the report there is a report footer that provides overall commission fee totals as follows: 
FIELD NAME  EXPLANATION  
TOTAL COMMISSION Total commission payable for this month , resulting in a cash obligation item (COI) 
labeled as “CMS” on the Cash [[settlement]] Detail Report . 
 
  

---

## Page 60

MBSD Operational Clearing Reports Guide 
[[Broker]] Commission Fees Report 60 
Print Image Report Sort Order 
The [[Broker]] Commission Fees Report is sorted by Dealer [[participant]] Symbol. 
Other Report Formats 
The [[Broker]] Commission Fees Report is also available in MRO format. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the [[Broker]] Commission 
Fees Report is available in two types: RJE and NDM. All MRO Report layouts can be found in the [[FICC]] MBSD 
User Documentation section of the [[DTCC]] website (http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/[[FICC]]-mbsd-
user-documentation#MachineReadableOutput) Look for: 
• RJE [[Broker]] Commission Report. (RJE format is grandfathered in for existing members.) 
• NDM [[Broker]] Commission Report. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist–there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Difference between MRO and Print Image [[Broker]] Commission Report 
The values reported in the .pdf format should be the same as values reported in MRO. 

---

## Page 61

MBSD Operational Clearing Reports Guide 
Dealer Commission Fees Report 61 
DEALER COMMISSION FEES REPORT 
Report Summary 
The Dealer Commission Fees Report is used to view [[Broker]]/dealer trade detail that determines this month’s 
commission fee for trades settling in the current month. It becomes available on the last business day of the 
month during the PM pass. 
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In general, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual Dealer Commission Fee details are listed with 
the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]] [[ID]]  A three-digit  number is assigned to each [[Member]]. 
AGGREGATE NUMBER  A two-character  alphanumeric following the [[participant]] [[ID]], which links an Account [[ID]] 
([[participant]] Symbol) to the [[participant]] [[ID]]. Every account must be linked to an aggregate 
for risk management and cash [[settlement]] reporting purposes.  
[[participant]] NAME  The name of the [[Member]]. 
[[participant]] SYMBOL  A 4-character identifier, the [[participant]] Symbol  represents the primary level of system 
identification. Trade submission occurs at the account level.  
DATE OF REPORT  The date the report was created.  
PASS INDICATOR  AM or PM sys tem pass. MBSD has two system passes. The AM pass is run in the 
afternoon, and the PM pass occurs in the evening. To learn more about the timeframes, 
please refer to the MBSD processing Schedule & Timeframes document which may be 
found in the [[participant]] Reference Documentation (MBS) section on www.[[DTCC]].com .  

---

## Page 62

MBSD Operational Clearing Reports Guide 
Dealer Commission Fees Report 62 
Trade Details 
Displays [[Broker]]/dealer trade details for TBA or SPT trades as of the end of a given month. 
FIELD  EXPLANATION  
BRKR ACCT MBSD [[Broker]] Account [[ID]]  
CNTR ACCT Give-up contra Account [[ID]]  
B/S Buy/Sell Indicator: B – Buy; S – Sell  
STTL MTH [[settlement]] month of the trade  
STTL YR [[settlement]] year of the trade 
[[CUSIP]] TBA [[CUSIP]]: Product, Agency, Coupon, Maturity, [[settlement]] month, Check digit  
SECURITY CLASS MBSD security class code: Agency, Product, Coupon, Maturity  
TRADE DATE Trade date 
TRADE NUMBER MBSD trade number  
XREF Your internal trade reference number  
PAR Par value of the trade 
DEALER PRICE Dealer price +/- Commission  
[[settlement]] PRICE [[settlement]] price of TBA trade 
COMMISSION Dollar value of commission  
TOTAL COMMISSION FOR 
[[Broker]] 
For specific [[Broker]], the total commission payable 
Report Totals 
At the end of the report there is a report footer that provides overall commission fee totals as follows: 
FIELD NAME  EXPLANATION  
TOTAL COMMISSION Total commission payable for this month,  resulting in a cash obligation item (COI) 
labeled as “CMS” on the Cash [[settlement]] Detail Report . 
 
  

---

## Page 63

MBSD Operational Clearing Reports Guide 
Dealer Commission Fees Report 63 
Print Image Report Sort Order 
The Dealer Commission Fees Report is sorted by [[Broker]] Account [[ID]]. 
Other Report Formats 
The Dealer Commission Fees Report is also available in MRO format. 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the Dealer Commission 
Fees Report is available in two types: RJE and NDM. All MRO Report layouts can be found in the [[FICC]] MBSD 
User Documentation section of the [[DTCC]] website (http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/[[FICC]]-mbsd-
user-documentation#MachineReadableOutput) Look for: 
• RJE Dealer Commission Report. (RJE format is grandfathered in for existing members.) 
• NDM Dealer Commission Report. (All new firms must receive the NDM format.) 
 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist–there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Difference between MRO and Print Image Dealer Commission Report 
The values reported in the .pdf format should be the same as values reported in MRO. 

---

## Page 64

MBSD Operational Clearing Reports Guide 
TBA Trade Reprice And Varianc e Report 64 
TBA TRADE REPRICE AND VARIANCE REPORT 
About the TBA Trade Reprice and Variance Report 
The TBA Trade Reprice and Variance Report, produced on 24-hour Day as prescribed by the SIFMA Calendar, 
provides dealers with details on all TBA trades that were repriced on the current business day, meaning that 
they were settled, and replacement trades generated at the system price.  Both original and replacement trade 
information is provided, along with reprice TAP due to price differences, allowing members to reconcile these 
[[settlement]] value differences. To learn more about the timeframes of the processes relevant to this report, 
please refer to the MBSD Processing Schedule & Timeframes document which may be found in the [[participant]] 
Reference Documentation (MBS) section on www.[[DTCC]].com. 
In addition, this report provides details on variance par associated with each trade, due to allocations 
processed in the daily or expanded pool net cycles. Trade and variance par details are provided along with 
corresponding variance TAP due to price differences.  
Print Image (pdf) Report Section/Layout Information 
The Print Image format is available in MBSD RTTM Web Report Center in a readable format suitable for 
printing.  
Note  
In gene ral, the layout of print -image reports is subject to change. They will be produced as a PDF file and will have 
extension “.pdf”.  
Print-image reports are generated: 
• For participants that are active and not EPN-only. 
• For active accounts with no activity associated with the report it will indicate "no activity."  
 
Within each section of the print image (pdf) report, the individual TBA Trade Reprice and Variance details are 
listed with the following data. 
Account Header Information 
Displays information on the account associated with this report; 1 per report. 
FIELD  EXPLANATION  
[[participant]]/Aggregate  A three -digit number is assigned to each [[Member]] followed by a 2- digit number or 
alphanumeric identifier  
Account Description  The account name 
Account [[ID]] The four - character account symbol  

---

## Page 65

MBSD Operational Clearing Reports Guide 
TBA Trade Reprice And Varianc e Report 65 
FIELD  EXPLANATION  
Business Date A date field showing the current business date 
TBA [[CUSIP]] Header Information 
Displays information on TBA [[CUSIP]] of current grouping; 1 per MM/YYYY and TBA [[CUSIP]] included in this 
section. 
FIELD  EXPLANATION  
[[settlement]] Month/Year  [[settlement]] month and year  
TBA [[CUSIP]] 9-character To Be Announced [[CUSIP]]  
SECURITY CLASS Description of this TBA [[CUSIP]]  
RPC/SYSTEM PRICE Price on new trade  
Repriced Trade Details 
Displays information on each repriced trade; 1 per trade. 
FIELD  EXPLANATION  
ORIG TRD # Trade number on original trade 
XREF [[Member]] XREF 
B/S BUY or SELL 
TRD TYPE Trade Type – SBON or TFTD  
S/D Contractual [[settlement]] Date 
T/D Trade Date 
PRICE Price on original trade  
RPC PAR Amount of par subject to repricing, i.e. open par on trade  
VAR PAR Amount of par subject variance calculation, i.e. sum  of all variance calculated for individual 
allocations and assigned to this trade  
OPN STL VAL [[settlement]] value of RPC PAR based on PRICE  
VAR STL VAL [[settlement]] value of VAR PAR based on PRICE  
RPC STL VAL New [[settlement]] value of RPC PAR based on RPC/SYST EM, calculated as:  
RPC STL VAL = OPN STL VAL + RPC TAP 
RPC VAR STL VAL [[settlement]] value of VAR PAR based on RPC/SYSTEM PRICE, calculated as:  
RPC VAR STL VAL = VAR STL VAL + VAR TAP 
RPC TAP TAP associated with the repriced trade due to price differences  

---

## Page 66

MBSD Operational Clearing Reports Guide 
TBA Trade Reprice And Varianc e Report 66 
FIELD  EXPLANATION  
VAR TAP TAP associated with price difference of the TBA Obligation and the current face of the pools 
allocated in satisfaction of the obligation 
RPC TRD [[ID]] Trade number of new repriced trade 
TBA [[CUSIP]] Sub-Totals 
Displays sub-total information for each TBA [[CUSIP]] grouping. 
FIELD NAME  EXPLANATION  
RPC TAP Sum of all “RPC TAP” within this TBA [[CUSIP]] grouping  
VAR TAP Sum of all “VAR TAP” within this TBA [[CUSIP]] grouping  
Report Totals 
Displays sub-total information for report; 1 per report. 
FIELD NAME  EXPLANATION  
Total TAP Sum of all “RPC TAP” within report  
Sum of all “VAR TAP” within report  
Sub-Totals 
• Total RPC TAP per TBA [[CUSIP]] and per REPORT 
• Total VAR TAP per TBA [[CUSIP]] and per REPORT 
Print Image Report Sort Order 
The TBA Trade Reprice and Variance Report is sorted as follows: 
• [[settlement]] Month/Year = earliest to latest 
• TBA [[CUSIP]] = ascending order 
• Trade Type (SBON, TFTD) = ascending order 
• Trade [[ID]] = ascending order. 
Other Report Formats 
The TBA Trade Reprice and Variance Report is also available in MRO format.  

---

## Page 67

MBSD Operational Clearing Reports Guide 
TBA Trade Reprice And Varianc e Report 67 
MRO Reports 
MRO files are produced in fixed-length machine-readable layout. The MRO format of the TBA Trade Reprice 
and Variance Report can be found at http://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbs-[[Novation]]-
documentation. (Look for the MRO NDM TBA Reprice report.)I 
“Perfect mapping” of fields/headers between the Print Image reports and the MRO reports doesn’t exist–there 
are more headers, for example, in the MRO reports. The Print Image reports show relevant information in a 
way that is more “readable.” 
Difference between MRO and Print-image TBA Trade Reprice and Variance Report 
The values reported in the .pdf format should be the same as values reported in MRO.  

---

## Page 68

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at:  
CoreLearning@[[DTCC]].com  
Or visit us on the web at:  
www.dtcclearning.com 