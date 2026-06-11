---
title: "CMU RTTM Print Image Activity Reports"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cmu110_print-reports-2021Nov16.pdf"
pages: 58
size: "1686.1 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# CMU RTTM Print Image Activity Reports

**Original File:** [cmu110_print-reports-2021Nov16.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cmu110_print-reports-2021Nov16.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 58  
**File Size:** 1686.1 KB  

---

## Page 1

CORPORATE, MUNICIPAL, AND [[UIT]] 
(CMU)
CMU RTTM
PRINT IMAGE ACTIVITY REPORTS
VERSION 2.5
NOVEMBER 16, 2021


---

## Page 2

© 2020 [[DTCC]]. All rights reserved.   [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and 
the Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust 
& Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate 
legal entity, subject to the laws and regulations of the particular country or countries in which such entity operates. 
Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Doc Info: November 16, 2021
Publication Code: CMU113
Service: Corporate, Municipal, and [[UIT]] (CMU)
Title: CMU RTTM Print Image Activity Reports 

---

## Page 3

TABLE OF CONTENTS
1. OVERVIEW 4
Contacts 4
2. REPORT CENTER 5
3. VIEWING ACTIVITY REPORTS AND SHORTCUTS 7
4. ENHANCED MATCHING REPORT 8
5. PURGE REPORT 11
6. REGULAR WAY ACTIVITY REPORT – [[OTC]]/[[UIT]] 14
7. REGULAR WAY ACTIVITY REPORT – MUNI 18
8. REJECT REPORT 22
Reject Reason Codes 24
9. REPRICED TRADES REPORT 25
10. WHEN ISSUED DETAIL TRANSACTION REPORT 28
11. WHEN ISSUED  REPORT 32
When Issued Report – [[syndicate]] Transaction 32
When Issued Report – Non-[[syndicate]] Transaction 36
12. TOTALS AT THE END OF EACH ACTIVITY REPORT 40
Totals Page for MUNI, When Issued [[syndicate]] and Non-[[syndicate]], and [[OTC]]/[[UIT]] Reports 41
Totals Exhibit for When Issued Detail Report 42
13. COLUMN AND FIELD DESCRIPTIONS 44

---

## Page 4

1. Overview 4
1. OVERVIEW
This document is intended for [[NSCC]] members and participants that use the CMU RTTM Activity reports to review, 
reconcile, and balance their trades. It explains how to read the CMU RTTM Activity reports, not how to enter, modify, or 
delete a trade. For instructions about trade entry and modifications,  see the CMU RTTM Web User Guide and other 
useful information available in the CMU User Guides section of the Learning Center.
In general:
l These reports are available the next business day after submission. If there is no activity for a [[participant]] on a
business day, a report is generated indicating that there was no activity.  On non-processing days for RTTM (for
example, holidays, or weekends), no reports are generated.
l The reports reflect the trades on submission date and their current end-of-day trade status, which includes
administrative matching, [[settlement]] disposition, and re-pricing updates.
l Trades that are unmatched will continuously appear on each day’s Activity Report until the status changes to
Matched, Canceled, or DKed. Then, these trades appear only once on the processing day of the Match, Cancel or
DK event. (Note: This statement applies to trade types, except for [[syndicate]] source trades.) On Submission Date
+ 2, Unmatched trades are systematically purged at the end of day.
l Each report is divided into two (2) sections – the Buy/Sell trades, followed by the Comparison-only trades. They are
sorted by [[CUSIP]] number in ascending order.  Within each [[CUSIP]], matched trades are listed first, next Advisories,
then unmatched trades (for example, Cancels, DKs, and Memos).
l Matched trades are reflected only once on the report upon matching.
l Unmatched, Advisories, Cancels, DKs, and Memo status trades are shaded/highlighted to visually emphasize that
they are not matched.
l All advisories are reflected as submitted from the aspect of the contra. (For example, if ABC Corp. submits a buy
against XYZ Ltd., XYZ would have a sell advisory on its report for this trade.) Advisories will continuously appear
on each day’s Activity Report until trade state changes and then, reflect once with the updated status.
Contacts
For CMU matching questions, [[DO]] one of the following:
l Call [[DTCC]] Client Support at 1-888-382-2721 (select [[Option]] 5, and then 4).
l Email [[CNS]] Operations at cashiering@[[DTCC]].com.
l Enter an inquiry using the [[DTC]] [[PBS]] WINS system.
For RTTM® Web Password issues:
l If you are not a super access coordinator (SAC) or access coordinator at your firm, contact your firm’s SAC or
access coordinator to reset your password.
l If you are a SAC or access coordinator for your firm, contact [[DTCC]] Client Support at 1 888 382-2721. (Select [[Option]]
5, and then 1).
See also: CMU RTTM Super Access Coordinator Guide
For problems with data communication or RTTM Web access issues or further CMU matching questions, call 
[[DTCC]] Client Support at 1 888 382-2721. (Select [[Option]] 5, and then 4).
Print Image Activity Reports

---

## Page 5

2. Report Center 5
2. REPORT CENTER
The Report Center, available from the CMU RTTM Web application, includes your archived end-of-day reports. 
Reports are in both comma-separated value (CSV) and portable document format (PDF). You can view or print reports. 
The following table shows the report name, Today's Report link, and the CSV or PDF file name. The CSV or PDF file 
name include the date of the report and a unique identifier. To access these eight CMU-RTTM Print Image Activity 
reports, select Report Center from the CMU RTTM Web application:
Report Name Today's Report Link CSV or PDF File Name
Enhanced Matching Report Enhanced Matching Enhanced_Matching_Report_
Purge Report Purge Purge_Report_
Regular Way Activity Report – [[OTC]]/[[UIT]] RW Activity [[OTC]] RW_Activity_CORP_UIT_
Regular Way Activity Report – MUNI RW Activity Muni RW_Activity_MUNI_
Reject Report Reject Reject_Report_
Repriced Trades Report Repriced Trades Repriced_Report_Participant_
When Issued Detail Transaction Report WI Detail Trans WI_Detail_Transaction_
When Issued  Report When Issued When_Issued_
To access reports:
1. Select Report Center from the Main menu. You can also access reports from the current business day by clicking
a link in the Today's Report section of the Home Page Statistics.
2. From the Group Name section of the CMU Reports page, click CMU RTTM. The CMU RTTM reports are displayed.
Print Image Activity Reports

---

## Page 6

2.ReportCenter 6
 3. From the CMU RTTM list of reports, click a link to view current end-of-day reports. Otherwise, from the Report Date 
field, select  a specific date, and then click View Reports. 
 4. After the reports display in the CMU RTTM section, select one of the options for the report that you want to view:
 l For current end-of-day reports, click 
  Download from the reports listed. 
 l For yesterday's end-of-day reports, click 
  Retrieve Latest, and then select the report.
 l For a specific date report, enter the date in the Report Date field, click 
  View Reports, and then 
select the report. 
PrintImageActivityReports

---

## Page 7

3.ViewingActivityReportsandShortcuts 7
3. VIEWING ACTIVITY REPORTS AND SHORTCUTS
CMU-RTTM Print Image reports are available in PDF or CSV format. View the PDF reports using Adobe Acrobat 
Reader, version 5.0 or higher, available at https://get.adobe.com/reader/. After accessing the report that you want to 
view, use the shortcuts , as highlighted in the following figure, to :
 l Save (
 ) a copy of the report to your local or the firm's network drive. Alternatively, click File > Save or Save As. 
 l Print (
 ) the report. Alternatively, click File > Print. 
 o It is recommended that you print your reports on legal size paper.
 o Remember to change your printer's orientation to Landscape.
 l Search the report (
 ) by [[CUSIP]], contra [[Broker]], quantity, final money, X-ref, and TID). Alternatively, click Edit 
> Find. 
 l Zoom in for detail or zoom out to view more of the page. Alternatively, click View > Zoom. 
PrintImageActivityReports

---

## Page 8

4.EnhancedMatchingReport 8
4. ENHANCED MATCHING REPORT
This report displays trades that RTTM has systematically matched. The three (3) most common reasons are:
 l Trade matched with money tolerance.
 l Submitted trade date different, but all other trade details match.
 l If a bilateral WI trade is unmatched at the end of the day and the trade details exactly match a [[syndicate]] trade, then 
RTTM treats it as a [[syndicate]] target trade and matches it to a [[syndicate]] sell.
Note
This report includes all trades regardless of the market type.
For an explanation of the fields and columns highlighted in the  Enhanced Matching Report, shown in the following 
figure,  see Table 4.1.  
The following table describes the columns and fields that appear in the Enhanced Matching report, which is accessible 
from the Report Center in the CMU RTTM Web application.  For more information about accessing the 
CMU RTTM Web application, see the CMU RTTM Web User Guide.
PrintImageActivityReports

---

## Page 9

4.EnhancedMatchingReport 9
Column/Field 
Name
Description
Processing Date Date and time the report was generated and produced by the RTTM system. Generally, the 
processing date and the business date are the same.
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Market Indicates the market in which the trades occurred, such as MUNI, [[syndicate]], or [[UIT]], and their 
trade disposition, such as  buy, sell, or comparison only.
XREF
(external reference 
number)
[[participant]] submitted trade reference number.
Contra XREF Trade reference number submitted by the contraparty.
Contra Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Buy/Sell Indicates whether you were on the buy or sell-side of a trade.
 Note: 
The Buy/Sell indicator does not appear on the Regular Way, When Issued, When Issued Detail 
Transaction, and Regular Way Activity – [[OTC]]/[[UIT]] reports since this indicator is reflected in the 
Market field. 
Quantity Quantity amount of the transaction.
Final Money Net [[settlement]] amount as submitted by the [[participant]] or as calculated by the RTTM system.
Original Final 
Money
Original net [[settlement]] amount as submitted by the [[participant]] or as calculated by the RTTM 
system.
P/Y/F
(Pricing Method)
Indicates the pricing method used in submitting a trade: 
 l P = dollar price*
 l Y = yield*
 l F = final money
Note: 
The Price and Yield methods apply only to WI/[[syndicate]] trades.
Trade Date Date the trade was executed.
Original Trade DateOriginal date the trade was executed.
Table 4.1  Enhanced Matching Report Field and Column Descriptions
PrintImageActivityReports

---

## Page 10

4.EnhancedMatchingReport 10
Column/Field 
Name
Description
Trd Typ 
(Trade Type)
Indicates the type of trade submission:
 l Bilateral (BIL)
 l QSR target (QSR TGT)
 l [[syndicate]] (SYN)
 l [[syndicate]] target (SYN TGT)
 l QSR
Notes:
Although not referenced in the [[NSCC]] rules, this term is frequently used in the RTTM system to 
describe the submission type, such as bilateral, [[syndicate]] or QSR.
Original Trade TypeOriginal type of trade  as submitted by the [[participant]]. 
 
Corr 
(Correspondent)
Four-character [[NASD]] [[Broker]] symbol of the [[Broker]] that executed the trade.
Contra Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Contra Corr
(Contra’s 
Correspondent)
Four-character [[NASD]] executing [[Broker]] symbol of your contraparty.
Settle Date 
([[settlement]] Date)
[[settlement]] date for a trade as submitted by the [[participant]] or assigned by [[NSCC]].
Note: 
If the trade is uncompared/unmatched, or if the [[settlement]] date is unavailable for a WI/[[syndicate]] 
trade, the [[settlement]] date is blank.
TID
(Transaction [[ID]])
Reference number generated by the RTTM system and used to identify a specific transaction.
[[CUSIP]] (and 
description)
Security description information is supplied by a third-party vendor and [[NSCC]] should not be 
held responsible for any errors or omissions in content.
[[participant]] Totals
(on the Purge 
Report) (# Items, 
Sum of Par)
Total number of items that have been purged by RTTM and their total par value.
Note: 
Trades that are canceled by your firm [[DO]] not appear on the Purge Report, but [[DO]] appear on the 
Activity reports.
Table 4.1  Enhanced Matching Report Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 11

5.PurgeReport 11
5. PURGE REPORT
This report reflects trades that have been deleted from RTTM. Unmatched trades on the system at the end of the day 
on Submission Date + 2 are automatically purged. 
Note
This report includes all trades regardless of the market type.
For an explanation of the fields and columns available in the Purge Report, shown in the following figure,  see Table 5.1. 
The following table describes the columns and fields that appear in the Purge report, which is accessible from the 
Report Center in the CMU RTTM Web application.  For more information about accessing the CMU RTTM Web 
application, see the CMU RTTM Web User Guide.
PrintImageActivityReports

---

## Page 12

5.PurgeReport 12
Column/Field 
Name
Description
Processing Date Date and time the report was generated and produced by the RTTM system. Generally, the 
processing date and the business date are the same.
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Market Indicates the market in which the trades occurred, such as MUNI, [[syndicate]] or [[UIT]], and their 
trade disposition, such as  buy, sell, or comparison only.
Trade Date Date the trade was executed.
Settle Date 
([[settlement]] Date)
[[settlement]] date for a trade as submitted by the [[participant]] or assigned by [[NSCC]].
Note: 
If the trade is uncompared/unmatched, or if the [[settlement]] date is unavailable for a WI/[[syndicate]] 
trade, the [[settlement]] date is blank.
Buy/Sell Indicates whether you were on the buy or sell-side of a trade.
 Note: 
The Buy/Sell indicator does not appear on the Regular Way, When Issued, When Issued Detail 
Transaction, and Regular Way Activity – [[OTC]]/[[UIT]] reports since this indicator is reflected in the 
Market field. 
XREF
(external reference 
number)
[[participant]] submitted trade reference number.
Contra Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Quantity Quantity amount of the transaction.
Price/Yield Numeric representation of the dollar price or yield figure submitted by the [[participant]].
P/Y/F
(Pricing Method)
Indicates the pricing method used in submitting a trade: 
 l P = dollar price*
 l Y = yield*
 l F = final money
Note: 
The Price and Yield methods apply only to WI/[[syndicate]] trades.
Concession 
(Concession Rate)
For WI/[[syndicate]] trades only.
This field is applicable only if the [[participant]] selects Yield as the pricing method, and enters a 
concession. This field can be either + or -.
Accrued Interest Either the interest amount submitted by the [[participant]] or the calculated accrued interest if RTTM 
prices the trade.
Final Money Either the net [[settlement]] amount as submitted by the [[participant]] or as calculated by the RTTM 
system.
Table 5.1  Purge Report
PrintImageActivityReports

---

## Page 13

5.PurgeReport 13
Column/Field 
Name
Description
Ext Day
(Extended 
[[settlement]] Day(s))
For WI Trades only.
Number of days that a trade settles beyond the distribution date.
Corr 
(Correspondent)
Four-character [[NASD]] [[Broker]] symbol of the [[Broker]] that executed the trade.
Contra Corr
(Contra’s 
Correspondent)
Four-character [[NASD]] executing [[Broker]] symbol of your contraparty.
Purge Reason Values are:
 l DELE – Deleted due to the end of life of an Unmatched/ Uncompared trade.
 l DEDK – Deleted due to contra DK.
 l DEME – Deleted due to life of a When Issue Memo trade.
 l DEPE – Deleted due to life of a Pending (When Issue) trade.
 l DESE – Deleted due to security detail differences.
TID
(Transaction [[ID]])
Reference number generated by the RTTM system and used to identify a specific transaction.
[[CUSIP]] (and 
description)
Security description information is supplied by a third-party vendor and [[NSCC]] should not be held 
responsible for any errors or omissions in content.
[[participant]] Totals
(# Items, Sum of 
Par)
Total number of items that have been purged by RTTM and their total par value.
Note: 
Trades that are canceled by your firm [[DO]] not appear on the Purge Report, but [[DO]] appear on the 
Activity reports.
Price For When Issued trades, done without final money. When applicable, this information displays in 
the Price/Yield column.
Table 5.1  Purge Report (Continued)
PrintImageActivityReports

---

## Page 14

6.RegularWayActivityReport–[[OTC]]/[[UIT]] 14
6. REGULAR WAY ACTIVITY REPORT – [[OTC]]/[[UIT]]
This report reflects activity for [[Over-The-Counter]] ([[OTC]]) and unit investment trust ([[UIT]]) transactions and their end of day 
trade status.   For an explanation of the fields and columns available in the Regular Way Activity Report – [[OTC]]/[[UIT]], 
shown in the following figure,  see Table 6.1. 
The following table describes the columns and fields that appear in the Regular Way Activity Report – [[OTC]]/[[UIT]], which 
is accessible from the Report Center in the CMU RTTM Web application.  For more information about accessing the 
CMU RTTM Web application, see the CMU RTTM Web User Guide.
Column/Field Name Description
Processing Date Date and time the report was generated and produced by the RTTM system. Generally, 
the processing date and the business date are the same.
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Market Indicates the market in which the trades occurred, such as MUNI, [[syndicate]], or [[UIT]], and 
their trade disposition, such as  buy, sell, or comparison only.
Trade Date Date the trade was executed.
Table 6.1  Regular Way Activity Report – [[OTC]]/[[UIT]] Field and Column Descriptions
PrintImageActivityReports

---

## Page 15

6.RegularWayActivityReport–[[OTC]]/[[UIT]] 15
Column/Field Name Description
Orig Dlv Date
(Original Delivery Date)
[[settlement]] date submitted by the [[participant]].
Corr 
(Correspondent)
Four-character [[NASD]] [[Broker]] symbol of the [[Broker]] that executed the trade.
Contra Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Contra Corr
(Contra’s Correspondent)
Four-character [[NASD]] executing [[Broker]] symbol of your contraparty.
Quantity Quantity amount of the transaction.
Final Money Either the net [[settlement]] amount as submitted by the [[participant]] or as calculated by the 
RTTM system.
Accrued Interest Either the interest amount submitted by the [[participant]] or the calculated accrued interest if 
RTTM prices the trade.
Trd Stat 
(Trade Status)
Reflects the latest status of a trade. 
Note: UM, AV, ME, and AVM trades are continuously reflected on the report until the trade is either 
dropped or the status changes.
 l UM=Unmatched trade
 l CXL=Canceled trade
 l AV=Advisory state
 l AVM=Advisory Memo state
 l MT=Matched trade
 l DK=DK state
 l ME=Memo state
 l AC=Canceled Advisory state
Sett Disp
([[settlement]] Disposition)
Indicates how a matched trade is anticipated to settle. The values are:
 l [[CNS]] = [[CNS]] netting
 l TFT = trade for trade
 l NCN = balance order netting for corporate [[Bonds]] and UITs only. 
If no [[settlement]] disposition is assigned, the field is blank.
Step Out S indicates that the trade was submitted with a step in the Contra Trader [[ID]] field.
 l On unmatched trades, both the unmatched and advisory firms see the S indicator.
 l On matched trades, only the firms that submitted the S indicator see it.
 l If step was not submitted, the field is blank.
REV
(Reversal Indicator)
R indicates that a trade was submitted as a reversal; otherwise, the field is blank.
Notes:
 l A reversal is used to exactly offset a previously submitted matched trade that is no 
longer eligible for cancellation.
 l A bilateral reversal requires the contra side to submit for a match.
Table 6.1  Regular Way Activity Report – [[OTC]]/[[UIT]] Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 16

6.RegularWayActivityReport–[[OTC]]/[[UIT]] 16
Column/Field Name Description
Spl Ind
(Special Trade Indicator)
Indicates if a trade was submitted or assigned with any special [[settlement]] values that 
preclude it from [[CNS]] [[settlement]]/netting. The values are:
 l A = AAA security
 l F = Comparison only
 l B = Ex-legal
 l G = Bearer only
 l D = Ex-Interest
 l H = Registered only
 l E = Called
 l X = [[participant]] assigned trade for trade
Note: 
If a [[syndicate]] or WI trade is subsequently assigned a comparison only status after the 
initial submission date, the trade is updated to a status of comparison only (F). This most 
frequently occurs when the [[CUSIP]] for a matched [[syndicate]] or WI trade is canceled.
Enh Mat
(Enhanced Match Indicator)
Y indicates that a trade was matched using RTTM enhanced matching; otherwise, the field is blank. 
The most common reason for enhanced matching is that a trade falls within money tolerances and 
matches on the [[Seller]]’s value.
Trd Typ 
(Trade Type)
Indicates the type of trade submission:
 l Bilateral (BIL)
 l QSR target (QSR TGT)
 l [[syndicate]] (SYN)
 l [[syndicate]] target (SYN TGT)
 l QSR
Notes:
 l Although not referenced in the [[NSCC]] rules, this term is frequently used in the RTTM 
system to describe the submission type (e.g., bilateral, [[syndicate]] or QSR).
 l There is no specific column or field for the trade type on the report, but the trade type is 
reflected in the report name.
Subm Date
(Submission Date)
Date that the trade was submitted to the RTTM application. 
Note: If a trade remains unmatched (for example, the contraparty does not submit the 
corresponding trade details), they are removed from the Activity report after Submission Date+ 2.
Settle Date 
([[settlement]] Date)
The [[settlement]] date as submitted by the [[participant]] or assigned by [[NSCC]]. 
Note: If the trade is unmatched/uncompared, the [[settlement]] date is blank.
XREF
(external reference number)
[[participant]] submitted trade reference number.
TID
(Transaction [[ID]])
Reference number generated by the RTTM system and used to identify a specific 
transaction.
[[CUSIP]] (and description)Security description information is supplied by a third-party vendor and [[NSCC]] should not 
be held responsible for any errors or omissions in content.
Table 6.1  Regular Way Activity Report – [[OTC]]/[[UIT]] Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 17

6.RegularWayActivityReport–[[OTC]]/[[UIT]] 17
Column/Field Name Description
Buy/Sell Indicates whether you were on the buy or sell-side of a trade.
Note: 
The Buy/Sell indicator does not appear on the Regular Way, When Issued, When Issued 
Detail Transaction, and Regular Way Activity – [[OTC]]/[[UIT]] reports since this indicator is 
reflected in the Market field. 
Matched/Compared For Regular Way reports for MUNI and [[OTC]]/[[UIT]]:
 l Totals on these reports reflect all Matched/Compared submitted on trade date.
For WI Syndicates:
 l Matched/Compared totals includes all trades with a [[syndicate]] status of match and 
[[syndicate]], regardless of submission.
 l Includes the Total Par value of all Matched/Compared trades and their total final 
money amount.
Unmatched/Uncompared l For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all 
Unmatched/Uncompared submitted on trade date.
 l For When Issued (Non-[[syndicate]]) - All totals for Unmatched/Uncompared reflect 
current day’s submissions..
Advisories For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all 
Advisories submitted on trade date.
For WIs (Non-[[syndicate]]) - All totals for Advisories reflect current day’s submissions.
 l Totals Match/Unmatch 
on T for Regular Way
 l Totals Match/Unmatch 
on T for WI
 l Combined total number of trades (compared/matched and uncompared/unmatched) 
that have been submitted by your firm on trade date. Does not include trade rejects.
 l Same as Regular Way, but the totals include all of the trade dates.
Grand Totals Sum of all items.
Table 6.1  Regular Way Activity Report – [[OTC]]/[[UIT]] Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 18

7.RegularWayActivityReport–MUNI 18
7. REGULAR WAY ACTIVITY REPORT – MUNI
The Regular Way Activity report reflects activity for municipal (MUNI) transactions and their end of day trade status. 
For an explanation of the fields and columns highlighted in the Regular Way Activity Report – MUNI, shown in the 
following figure,  see Table 7.1.
The following table describes the columns and fields that appear in the Regular Way Activity Report – MUNI, which is 
accessible from the Report Center in the CMU RTTM Web application.  For more information about accessing the 
CMU RTTM Web application, see the CMU RTTM Web User Guide.
Column/Field Name Description
Processing Date Date and time the report was generated and produced by the RTTM system. Generally, 
the processing date and the business date are the same.
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Market Indicates the market in which the trades occurred, such as MUNI, [[syndicate]], or [[UIT]], and 
their trade disposition, such as  buy, sell, or comparison only.
Trade Date Date the trade was executed.
Table 7.1  Regular Way Activity Report - MUNI Field and Column Descriptions
PrintImageActivityReports

---

## Page 19

7.RegularWayActivityReport–MUNI 19
Column/Field Name Description
Orig Dlv Date
(Original Delivery Date)
[[settlement]] date submitted by the [[participant]].
Corr 
(Correspondent)
Four-character [[NASD]] [[Broker]] symbol of the [[Broker]] that executed the trade.
Contra Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Contra Corr
(Contra’s Correspondent)
Four-character [[NASD]] executing [[Broker]] symbol of your contraparty.
Quantity Quantity amount of the transaction.
Final Money Either the net [[settlement]] amount as submitted by the [[participant]] or as calculated by the 
RTTM system.
Accrued Interest Either the interest amount submitted by the [[participant]] or the calculated accrued interest if 
RTTM prices the trade.
Trd Stat 
(Trade Status)
Reflects the latest status of a trade. 
Note: UM, AV, ME, and AVM trades are continuously reflected on the report until the trade is either 
dropped or the status changes.
 l UM=Unmatched trade
 l CXL=Canceled trade
 l AV=Advisory state
 l AVM=Advisory Memo state
 l MT=Matched trade
 l DK=DK state
 l ME=Memo state
 l AC=Canceled Advisory state
Sett Disp
([[settlement]] Disposition)
Indicates how a matched trade is anticipated to settle. The values are:
 l [[CNS]] = [[CNS]] netting
 l TFT = trade for trade
 l NCN = balance order netting for corporate [[Bonds]] and UITs only. 
If no [[settlement]] disposition is assigned, the field is blank.
Step Out S indicates that the trade was submitted with a step in the Contra Trader [[ID]] field.
 l On unmatched trades, both the unmatched and advisory firms see the S indicator.
 l On matched trades, only the firms that submitted the S indicator see it.
 l If step was not submitted, the field is blank.
REV
(Reversal Indicator)
R indicates that a trade was submitted as a reversal; otherwise, the field is blank.
Notes:
 l A reversal is used to exactly offset a previously submitted matched trade that is no 
longer eligible for cancellation.
 l A bilateral reversal requires the contra side to submit for a match.
Table 7.1  Regular Way Activity Report - MUNI Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 20

7.RegularWayActivityReport–MUNI 20
Column/Field Name Description
Spl Ind
(Special Trade Indicator)
Indicates if a trade was submitted or assigned with any special [[settlement]] values that 
preclude it from [[CNS]] [[settlement]]/netting. The values are:
 l A = AAA security
 l F = Comparison only
 l B = Ex-legal
 l G = Bearer only
 l D = Ex-Interest
 l H = Registered only
 l E = Called
 l X = [[participant]] assigned trade for trade
Note: 
If a [[syndicate]] or WI trade is subsequently assigned a comparison only status after the 
initial submission date, the trade is updated to a status of comparison only (F). This most 
frequently occurs when the [[CUSIP]] for a matched [[syndicate]] or WI trade is canceled.
Enh Mat
(Enhanced Match Indicator)
Y indicates that a trade was matched using RTTM enhanced matching; otherwise, the field is blank. 
The most common reason for enhanced matching is that a trade falls within money tolerances and 
matches on the [[Seller]]’s value.
Trd Typ 
(Trade Type)
Indicates the type of trade submission:
 l Bilateral (BIL)
 l QSR target (QSR TGT)
 l [[syndicate]] (SYN)
 l [[syndicate]] target (SYN TGT)
 l QSR
Notes:
Although not referenced in the [[NSCC]] rules, this term is frequently used in the RTTM 
system to describe the submission type, such as bilateral, [[syndicate]] or QSR.
Subm Date
(Submission Date)
Date that the trade was submitted to the RTTM application. 
Note: If a trade remains unmatched (for example, the contraparty does not submit the 
corresponding trade details), they are removed from the Activity report after Submission Date+ 2.
Settle Date 
([[settlement]] Date)
The [[settlement]] date as submitted by the [[participant]] or assigned by [[NSCC]]. 
Note: If the trade is unmatched/uncompared, the [[settlement]] date is blank.
XREF
(external reference number)
[[participant]] submitted trade reference number.
TID
(Transaction [[ID]])
Reference number generated by the RTTM system and used to identify a specific 
transaction.
[[CUSIP]] (and description)Security description information is supplied by a third-party vendor and [[NSCC]] should not 
be held responsible for any errors or omissions in content.
Table 7.1  Regular Way Activity Report - MUNI Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 21

7.RegularWayActivityReport–MUNI 21
Column/Field Name Description
Buy/Sell Indicates whether you were on the buy or sell-side of a trade.
Note: 
The Buy/Sell indicator does not appear on the Regular Way, When Issued, When Issued 
Detail Transaction, and Regular Way Activity – [[OTC]]/[[UIT]] reports since this indicator is 
reflected in the Market field. 
Matched/Compared For Regular Way reports for MUNI and [[OTC]]/[[UIT]]:
 l Totals on these reports reflect all Matched/Compared submitted on trade date.
For WI Syndicates:
 l Matched/Compared totals includes all trades with a [[syndicate]] status of match and 
[[syndicate]], regardless of submission.
 l Includes the Total Par value of all Matched/Compared trades and their total final 
money amount.
Unmatched/Uncompared l For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all 
Unmatched/Uncompared submitted on trade date.
 l For When Issued (Non-[[syndicate]]) - All totals for Unmatched/Uncompared reflect 
current day’s submissions..
Advisories For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all 
Advisories submitted on trade date.
For WIs (Non-[[syndicate]]) - All totals for Advisories reflect current day’s submissions.
 l Totals Match/Unmatch 
on T for Regular Way
 l Totals Match/Unmatch 
on T for WI
 l Combined total number of trades (compared/matched and uncompared/unmatched) 
that have been submitted by your firm on trade date. Does not include trade rejects.
 l Same as Regular Way, but the totals include all of the trade dates.
Grand Totals Sum of all items.
Table 7.1  Regular Way Activity Report - MUNI Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 22

8.RejectReport 22
8. REJECT REPORT
This report reflects the trades that RTTM has rejected.  At the end of the day, all rejected records are purged from the 
system.  For an explanation of the fields and columns available in the Reject  Report, shown in the following figure,  see 
Table 8.1. For the reject reason codes and error conditions that cause a reject, see Reject Reason Codes.
Note
This report includes all trades regardless of the market type.
The following table describes the columns and fields that appear in the Reject report, which is accessible from the 
Report Center in the CMU RTTM Web application.  For more information about accessing the CMU RTTM Web 
application, see the CMU RTTM Web User Guide.
Column/Field 
Name
Description
Processing 
Date
Date and time the report was generated and produced by the RTTM system. Generally, the 
processing date and the business date are the same.
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
Table 8.1  Reject Report Field and Column Descriptions
PrintImageActivityReports

---

## Page 23

8.RejectReport 23
Column/Field 
Name
Description
[[participant]] 
Name
[[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Market Indicates the market in which the trades occurred, such as MUNI, [[syndicate]] or [[UIT]], and their trade 
disposition, such as  buy, sell, or comparison only.
XREF
(external 
reference 
number)
[[participant]] submitted trade reference number.
Buy/Sell Indicates whether you were on the buy or sell-side of a trade.
Note: 
The Buy/Sell indicator does not appear on the Regular Way, When Issued, When Issued Detail 
Transaction, and Regular Way Activity – [[OTC]]/[[UIT]] reports since this indicator is reflected in the 
Market field. 
Trade Date Date the trade was executed.
Settle Date 
([[settlement]] 
Date)
[[settlement]] date for a trade as submitted by the [[participant]] or assigned by [[NSCC]].
Note: 
If the trade is uncompared/unmatched, or if the [[settlement]] date is unavailable for a WI/[[syndicate]] 
trade, the [[settlement]] date is blank.
Ext Day
(Extended 
[[settlement]] Day
(s))
For WI Trades only.
Number of days that a trade settles beyond the distribution date.
Contra [[ID]] Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Quantity Quantity amount of the transaction.
Price Numeric representation of the dollar price or yield figure submitted by the [[participant]].
Final Money Either the net [[settlement]] amount as submitted by the [[participant]] or as calculated by the RTTM 
system.
Reject Reason
(on the Reject 
Report)
Indicates why a trade was rejected from the system. See Reject Reason Codes.
Create Date
(on the Reject 
Report)
Date that the trade was rejected by the RTTM system.
Total Items
(on the Reject 
Report)
Total number of trades rejected by the RTTM system on that day.
Table 8.1  Reject Report Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 24

8.RejectReport 24
Reject Reason Codes
The following table shows the reject reason codes and error conditions:
Reject Error Code 
Qualifiers
Error Conditions Reject Error Code 
Qualifiers
Error Conditions
GSCC/E001 External Reference Error GSCC/E201 Turnaround Number Error
GSCC/E002 Previous External Reference 
Error
GSCC/E202 Market of Execution Error
GSCC/E003 Trade Not Eligible For 
Cancellation
GSCC/E203 Trade Type/Target Indicator 
Error
GSCC/E004 Unknown Security GSCC/E204 Destination Indicator Error
GSCC/E005 Bad Quantity GSCC/E205 Inconsistent Recipient 
Information
GSCC/E006 Bad Trade Date GSCC/E206 Issue Type Error
GSCC/E007 Bad [[settlement]] Date GSCC/E207 [[settlement]] Date Adjustment 
Error
GSCC/E008 Bad Price GSCC/E208 [[settlement]] Type Error
GSCC/E009 Bad Amount GSCC/E209 Interest Error
GSCC/E010 Bad [[Buyer]] Party GSCC/E210 Concession Error
GSCC/E011 Bad [[Seller]] Party GSCC/E211 Branch Sequence Number 
Error
GSCC/E012 [[Broker]] Reference Number 
Error
GSCC/E212 Unknown Target Application
GSCC/E013 Transaction Type Error GSCC/E998 Trade Not Found
GSCC/E014 Price Method Error GSCC/E999 Other Bad Data
GSCC/E015 Commission Error GSCC/F001 Illegal Operation Attempted
GSCC/E016 Password Error GSCC/F002 Internal Process Error
GSCC/E017 [[Buyer]] Executing Firm Error GSCC/F999 Non-SWIFT Compliant 
Message
GSCC/E018 [[Seller]] Executing Firm Error   
Message Reject Reason Codes
The following table shows the Don’t Know (DK) reason codes:
DK Reason Codes DK Reasons
E100 Unknown Cancel
E106 Incorrect Account Symbol
E107 Duplicate Trade
Don't Know (DK) Reason Codes
PrintImageActivityReports

---

## Page 25

9.RepricedTradesReport 25
9. REPRICED TRADES REPORT
For an explanation of the fields and columns available in the Repriced  Report, shown in the following figure,  see Table 
9.1. 
The following table describes the columns and fields that appear in the Repriced report, which is accessible from the 
Report Center in the CMU RTTM Web application.  For more information about accessing the CMU RTTM Web 
application, see the CMU RTTM Web User Guide.
Column/Field 
Name
Description
Processing Date Date and time the report was generated and produced by the RTTM system. Generally, the 
processing date and the business date are the same.
[[CUSIP]] (and 
description)
Security description information is supplied by a third-party vendor and [[NSCC]] should not be held 
responsible for any errors or omissions in content.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Table 9.1  Repriced Report Field and Column Descriptions
PrintImageActivityReports

---

## Page 26

9.RepricedTradesReport 26
Column/Field 
Name
Description
Buy/Sell Indicates whether you were on the buy or sell-side of a trade.
 Note: 
The Buy/Sell indicator does not appear on the Regular Way, When Issued, When Issued Detail 
Transaction, and Regular Way Activity – [[OTC]]/[[UIT]] reports since this indicator is reflected in the 
Repriced Trades Report field. 
[[participant]] [[ID]] [[participant]]’s four-digit [[NSCC]] clearing number.
XREF
(external reference 
number)
[[participant]] submitted trade reference number.
Prev Day  
Update Type  
Reprice Reason  
Trd Type  
Corr 
(Correspondent)
Four-character [[NASD]] [[Broker]] symbol of the [[Broker]] that executed the trade.
Contra Corr
(Contra’s 
Correspondent)
Four-character [[NASD]] executing [[Broker]] symbol of your contraparty.
Trans Type  
Quantity Quantity amount of the transaction.
Accrued Interest Either the interest amount submitted by the [[participant]] or the calculated accrued interest if RTTM 
prices the trade.
Final Money Either the net [[settlement]] amount as submitted by the [[participant]] or as calculated by the RTTM 
system.
Trade Date Date the trade was executed.
STLMT Date 
([[settlement]] Date)
[[settlement]] date for a trade as submitted by the [[participant]] or assigned by [[NSCC]].
Note: 
If the trade is uncompared/unmatched, or if the [[settlement]] date is unavailable for a WI/[[syndicate]] 
trade, the [[settlement]] date is blank.
State Code Indicates the : 
 l UM = 
 l MT = 
  
Contra Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Price/Yield Numeric representation of the dollar price or yield figure submitted by the [[participant]].
Table 9.1  Repriced Report Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 27

9.RepricedTradesReport 27
Column/Field 
Name
Description
P/Y/F
(Pricing Method)
Indicates the pricing method used in submitting a trade: 
 l P = dollar price*
 l Y = yield*
 l F = final money
Note: 
The Price and Yield methods apply only to WI/[[syndicate]] trades.
Concession 
(Concession Rate)
For WI/[[syndicate]] trades only.
This field is applicable only if the [[participant]] selects Yield as the pricing method, and enters a 
concession. This field can be either + or -.
  
Ext Day
(Extended 
[[settlement]] Day(s))
For WI Trades only.
Number of days that a trade settles beyond the distribution date.
Purge Reason Values are:
 l DELE – Deleted due to the end of life of an Unmatched/ Uncompared trade.
 l DEDK – Deleted due to contra DK.
 l DEME – Deleted due to life of a When Issue Memo trade.
 l DEPE – Deleted due to life of a Pending (When Issue) trade.
 l DESE – Deleted due to security detail differences.
TID
(Transaction [[ID]])
Reference number generated by the RTTM system and used to identify a specific transaction.
[[participant]] Totals
(# Items, Sum of 
Par)
Total number of items that have been purged by RTTM and their total par value.
Note: 
Trades that are canceled by your firm [[DO]] not appear on the Purge Report, but [[DO]] appear on the 
Activity reports.
Price For When Issued trades, done without final money. When applicable, this information displays in 
the Price/Yield column.
Table 9.1  Repriced Report Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 28

10.WhenIssuedDetailTransactionReport 28
10. WHEN ISSUED DETAIL TRANSACTION REPORT
This report reflects the when issued (WI) and [[syndicate]] trades that have been forwarded to the [[NSCC]] [[settlement]] 
system on [[settlement]] Date-2 or [[settlement]]-1.  For an explanation of the fields and columns available in the When 
Issued Detail Transaction Report, shown in the following figure,  see Table 10.1.
The following table describes the columns and fields that appear in the When Issued Detail Transaction report, which is 
accessible from the Report Center in the CMU RTTM Web application.  For more information about accessing the 
CMU RTTM Web application, see the CMU RTTM Web User Guide.
Column/Field Name Description
Processing Date Date and time the report was generated and produced by the RTTM system. Generally, 
the processing date and the business date are the same.
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Market Indicates the market in which the trades occurred, such as MUNI, [[syndicate]], or [[UIT]], and 
their trade disposition, such as  buy, sell, or comparison only.
Trade Date Date the trade was executed.
Corr 
(Correspondent)
Four-character [[NASD]] [[Broker]] symbol of the [[Broker]] that executed the trade.
Table 10.1  When Issued Detail Report Field and Column Descriptions
PrintImageActivityReports

---

## Page 29

10.WhenIssuedDetailTransactionReport 29
Column/Field Name Description
Contra Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Contra Corr
(Contra’s Correspondent)
Four-character [[NASD]] executing [[Broker]] symbol of your contraparty.
Quantity Quantity amount of the transaction.
Final Money Either the net [[settlement]] amount as submitted by the [[participant]] or as calculated by the 
RTTM system.
Accrued Interest Either the interest amount submitted by the [[participant]] or the calculated accrued interest if 
RTTM prices the trade.
Trd Stat 
(Trade Status)
Reflects the latest status of a trade. 
Note: UM, AV, ME, and AVM trades are continuously reflected on the report until the trade is either 
dropped or the status changes.
 l UM=Unmatched trade
 l CXL=Canceled trade
 l AV=Advisory state
 l AVM=Advisory Memo state
 l MT=Matched trade
 l DK=DK state
 l ME=Memo state
 l AC=Canceled Advisory state
Sett Disp
([[settlement]] Disposition)
A [[settlement]] disposition indicates how a matched trade is anticipated to settle. These 
values are:
 l [[CNS]] = [[CNS]] netting
 l TFT = trade for trade.
Step Out S indicates that the trade was submitted with a step in the Contra Trader [[ID]] field.
 l On unmatched trades, both the unmatched and advisory firms see the S indicator.
 l On matched trades, only the firms that submitted the S indicator see it.
 l If step was not submitted, the field is blank.
Rev
(Reversal Indicator)
R indicates that a trade was submitted as a reversal; otherwise, the field is blank.
Notes:
 l Reversal is used to exactly offset a previously submitted matched trade that is no 
longer eligible for cancellation.
Table 10.1  When Issued Detail Report Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 30

10.WhenIssuedDetailTransactionReport 30
Column/Field Name Description
Spl Ind
(Special Trade Indicator)
Indicates if a trade was submitted or assigned with any special [[settlement]] values that 
preclude it from [[CNS]] [[settlement]]/netting. The values are:
 l A = AAA security
 l F = Comparison only
 l B = Ex-legal
 l G = Bearer only
 l D = Ex-Interest
 l H = Registered only
 l E = Called
 l X = [[participant]] assigned trade for trade
Note: 
If a [[syndicate]] or WI trade is subsequently assigned a comparison only status after the 
initial submission date, the trade is updated to a status of comparison only (F). This most 
frequently occurs when the [[CUSIP]] for a matched [[syndicate]] or WI trade is canceled.
Enh Mat
(Enhanced Match Indicator)
Y indicates that a trade was matched using RTTM enhanced matching; otherwise, the field is blank. 
The most common reason for enhanced matching is that a trade falls within money tolerances and 
matches on the [[Seller]]’s value.
Trd Typ (Trade Type) Indicates the type of trade submission – either Bilateral (BIL) or [[syndicate]] (SYN).
Note: Although not referenced in the [[NSCC]] rules, this term is frequently used in the RTTM 
system to describe the submission type (bilateral, [[syndicate]] or QSR).
Subm Date
(Submission Date)
Date that the trade was submitted to the RTTM application. 
Note: If a trade remains unmatched (for example, the contraparty does not submit the 
corresponding trade details), they are removed from the Activity report after Submission Date+ 2.
Settle Date 
([[settlement]] Date)
Distribution date of the security. Also known as the Firm [[settlement]] Date.
If the trade was submitted as an extended [[settlement]] date trade, the [[settlement]] date will 
reflect the [[settlement]] date submitted by the [[participant]].
XREF
(external reference number)
[[participant]] submitted trade reference number.
TID
(Transaction [[ID]])
Reference number generated by the RTTM system and used to identify a specific 
transaction.
[[CUSIP]] (and description)Security description information is supplied by a third-party vendor and [[NSCC]] should not 
be held responsible for any errors or omissions in content.
Ext Day
(Extended [[settlement]] 
Days)
Number of days that a trade settles beyond the distribution date.
Price/Yield Numeric representation of the dollar price or yield figure submitted by the [[participant]].
Table 10.1  When Issued Detail Report Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 31

10.WhenIssuedDetailTransactionReport 31
Column/Field Name Description
P/Y/F
(Pricing Method)
Indicates whether the trade was submitted with a:
 l Dollar price = P
 l Yield = Y
 l Final money = F
Concess 
(Concession Rate)
For WI/[[syndicate]] trades only.
This field is applicable only if the [[participant]] selects Yield as the pricing method, and 
enters a concession. This field can be either + or -.
Buy/Sell Indicates whether you were on the buy or sell-side of a trade.
Note: 
The Buy/Sell indicator does not appear on the Regular Way, When Issued, When Issued 
Detail Transaction, and Regular Way Activity – [[OTC]]/[[UIT]] reports since this indicator is 
reflected in the Market field. 
Grand Totals Sum of all items.
Table 10.1  When Issued Detail Report Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 32

11.WhenIssuedReport 32
11. WHEN ISSUED  REPORT
The When Issued Report reflects activity for [[syndicate]] and when issued (WI), non-[[syndicate]], transactions and their 
corresponding end of day trade status. For an example of each type of When Issued Report and description of the 
fields, see:
 l When Issued Report – [[syndicate]] Transaction
 l When Issued Report – Non-[[syndicate]] Transaction
When Issued Report – [[syndicate]] Transaction
For an explanation of the fields and columns available in the When Issued  Report, shown in the following figure,  see 
Table 11.1.
The following table describes the columns and fields that appear in the When Issued report containing [[syndicate]] 
activity, which is accessible from the Report Center in the CMU RTTM Web application.  For more information about 
accessing the CMU RTTM Web application, see the CMU RTTM Web User Guide.
PrintImageActivityReports

---

## Page 33

11.WhenIssuedReport 33
Column/Field Name Description
Processing Date Date and time the report was generated and produced by the RTTM system. Generally, 
the processing date and the business date are the same.
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Market Indicates the market in which the trades occurred, such as MUNI, [[syndicate]], or [[UIT]], and 
their trade disposition, such as  buy, sell, or comparison only.
Trade Date Date the trade was executed.
Corr 
(Correspondent)
Four-character [[NASD]] [[Broker]] symbol of the [[Broker]] that executed the trade.
Contra Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Contra Corr
(Contra’s Correspondent)
Four-character [[NASD]] executing [[Broker]] symbol of your contraparty.
Quantity Quantity amount of the transaction.
Final Money Either the net [[settlement]] amount as submitted by the [[participant]] or as calculated by the 
RTTM system.
Accrued Interest Either the interest amount submitted by the [[participant]] or the calculated accrued interest if 
RTTM prices the trade.
Step Out S indicates that the trade was submitted with a step in the Contra Trader [[ID]] field.
 l On unmatched trades, both the unmatched and advisory firms see the S indicator.
 l On matched trades, only the firms that submitted the S indicator see it.
 l If step was not submitted, the field is blank.
Rev
(Reversal Indicator)
R indicates that a trade was submitted as a reversal; otherwise, the field is blank.
Notes:
 l Reversal is used to exactly offset a previously submitted matched trade that is no 
longer eligible for cancellation.
 l Bilateral reversal requires the contra side to submit for a match.
Table 11.1  When Issued [[syndicate]] Activity Report Field and Column Descriptions
PrintImageActivityReports

---

## Page 34

11.WhenIssuedReport 34
Column/Field Name Description
Spl Ind
(Special Trade Indicator)
Indicates if a trade was submitted or assigned with any special [[settlement]] values that 
preclude it from [[CNS]] [[settlement]]/netting. The values are:
 l A = AAA security
 l F = Comparison only
 l B = Ex-legal
 l G = Bearer only
 l D = Ex-Interest
 l H = Registered only
 l E = Called
 l X = [[participant]] assigned trade for trade
Note: 
If a [[syndicate]] or WI trade is subsequently assigned a comparison only status after the 
initial submission date, the trade is updated to a status of comparison only (F). This most 
frequently occurs when the [[CUSIP]] for a matched [[syndicate]] or WI trade is canceled.
Enh Mat
(Enhanced Match Indicator)
Y indicates that a trade was matched using RTTM enhanced matching; otherwise, the field is blank. 
The most common reason for enhanced matching is that a trade falls within money tolerances and 
matches on the [[Seller]]’s value.
Trd Typ 
(Trade Type)
Indicates the type of trade submission:
 l Bilateral (BIL)
 l QSR target (QSR TGT)
 l [[syndicate]] (SYN)
 l [[syndicate]] target (SYN TGT)
 l QSR
Notes:
 l Although not referenced in the [[NSCC]] rules, this term is frequently used in the RTTM 
system to describe the submission type (e.g., bilateral, [[syndicate]] or QSR).
 l * There is no specific column or field for Trade Type on the report, but the trade type is 
reflected in the report name.
Subm Date
(Submission Date)
Date that the trade was submitted to the RTTM application. 
Note: If a trade remains unmatched (for example, the contraparty does not submit the 
corresponding trade details), they are removed from the Activity report after Submission Date+ 2.
Settle Date 
([[settlement]] Date)
Distribution date of the security. Also known as the Firm [[settlement]] Date.
If the trade was submitted as an extended [[settlement]] date trade, the [[settlement]] date will 
reflect the [[settlement]] date submitted by the [[participant]].
XREF
(external reference number)
[[participant]] submitted trade reference number.
TID
(Transaction [[ID]])
Reference number generated by the RTTM system and used to identify a specific 
transaction.
Table 11.1  When Issued [[syndicate]] Activity Report Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 35

11.WhenIssuedReport 35
Column/Field Name Description
[[CUSIP]] (and description)Security description information is supplied by a third-party vendor and [[NSCC]] should not 
be held responsible for any errors or omissions in content.
Ext Day
(Extended [[settlement]] 
Days)
Number of days that a trade settles beyond the distribution date.
Price/Yield Numeric representation of the dollar price or yield figure submitted by the [[participant]].
P/Y/F
(Pricing Method)
Indicates whether the trade was submitted with a:
 l Dollar price = P
 l Yield = Y
 l Final money = F
Concess 
(Concession Rate)
For WI/[[syndicate]] trades only.
This field is applicable only if the [[participant]] selects Yield as the pricing method, and 
enters a concession. This field can be either + or -.
Syn Stat 
([[syndicate]] Status)
Appears in the [[syndicate]] section of the WI report and reflects one of the following trade 
states:
 l SYN = Unmatched status
 l DK = DK status
 l AVM = Memo advisory status
 l MT = Matched status
 l ME = Memo status
 l AC = Canceled by [[syndicate]] Manager
 l CXL = Cancel status
Buy/Sell Indicates whether you were on the buy or sell-side of a trade.
Note: 
The Buy/Sell indicator does not appear on the Regular Way, When Issued, When Issued 
Detail Transaction, and Regular Way Activity – [[OTC]]/[[UIT]] reports since this indicator is 
reflected in the Market field. 
Matched/Compared For Regular Way reports for MUNI and [[OTC]]/[[UIT]]:
 l Totals on these reports reflect all Matched/Compared submitted on trade date.
For WI Syndicates:
 l Matched/Compared totals includes all trades with a [[syndicate]] status of match and 
[[syndicate]], regardless of submission.
 l Includes the Total Par value of all Matched/Compared trades and their total final 
money amount.
Table 11.1  When Issued [[syndicate]] Activity Report Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 36

11. When Issued Report 36
Column/Field Name Description
Unmatched/Uncompared l For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all
Unmatched/Uncompared submitted on trade date.
l For When Issued (Non-[[syndicate]]) - All totals for Unmatched/Uncompared reflect
current day’s submissions..
Advisories For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all 
Advisories submitted on trade date.
For WIs (Non-[[syndicate]]) - All totals for Advisories reflect current day’s submissions.
l Totals Match/Unmatch
on T for Regular Way
l Totals Match/Unmatch
on T for WI
l Combined total number of trades (compared/matched and uncompared/unmatched)
that have been submitted by your firm on trade date. Does not include trade rejects.
l Same as Regular Way, but the totals include all of the trade dates.
Grand Totals Sum of all items.
Table 11.1  When Issued [[syndicate]] Activity Report Field and Column Descriptions (Continued)
When Issued Report – Non-[[syndicate]] Transaction
For an explanation of the fields and columns available in the When Issued  Report, shown in the following figure,  
see Table 11.2.
The following table describes the columns and fields available in the When Issued (WI) Activity report.
Print Image Activity Reports

---

## Page 37

11.WhenIssuedReport 37
Column/Field Name Description
Processing Date Date and time the report was generated and produced by the RTTM system. Generally, 
the processing date and the business date are the same.
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Market Indicates the market in which the trades occurred, such as MUNI, [[syndicate]], or [[UIT]], and 
their trade disposition, such as  buy, sell, or comparison only.
Trade Date Date the trade was executed.
Corr 
(Correspondent)
Four-character [[NASD]] [[Broker]] symbol of the [[Broker]] that executed the trade.
Contra Four-digit [[NSCC]] [[participant]] clearing number of the contraparty.
Contra Corr
(Contra’s Correspondent)
Four-character [[NASD]] executing [[Broker]] symbol of your contraparty.
Quantity Quantity amount of the transaction.
Final Money Either the net [[settlement]] amount as submitted by the [[participant]] or as calculated by the 
RTTM system.
Accrued Interest Either the interest amount submitted by the [[participant]] or the calculated accrued interest if 
RTTM prices the trade.
Trd Stat 
(Trade Status)
Reflects the latest status of a trade. 
Note: UM, AV, ME, and AVM trades are continuously reflected on the report until the trade is either 
dropped or the status changes.
 l UM=Unmatched trade
 l CXL=Canceled trade
 l AV=Advisory state
 l AVM=Advisory Memo state
 l MT=Matched trade
 l DK=DK state
 l ME=Memo state
 l AC=Canceled Advisory state
Step Out S indicates that the trade was submitted with a step in the Contra Trader [[ID]] field.
 l On unmatched trades, both the unmatched and advisory firms see the S indicator.
 l On matched trades, only the firms that submitted the S indicator see it.
 l If step was not submitted, the field is blank.
Rev
(Reversal Indicator)
R indicates that a trade was submitted as a reversal; otherwise, the field is blank.
Notes:
 l Reversal is used to exactly offset a previously submitted matched trade that is no 
longer eligible for cancellation.
Table 11.2  When Issued (WI) Activity - Non-Syndicated Transactions Field and Column Descriptions
PrintImageActivityReports

---

## Page 38

11.WhenIssuedReport 38
Column/Field Name Description
Spl Ind
(Special Trade Indicator)
Indicates if a trade was submitted or assigned with any special [[settlement]] values that 
preclude it from [[CNS]] [[settlement]]/netting. The values are:
 l A = AAA security
 l F = Comparison only
 l B = Ex-legal
 l G = Bearer only
 l D = Ex-Interest
 l H = Registered only
 l E = Called
 l X = [[participant]] assigned trade for trade
Note: 
If a [[syndicate]] or WI trade is subsequently assigned a comparison only status after the 
initial submission date, the trade is updated to a status of comparison only (F). This most 
frequently occurs when the [[CUSIP]] for a matched [[syndicate]] or WI trade is canceled.
Enh Mat
(Enhanced Match Indicator)
Y indicates that a trade was matched using RTTM enhanced matching; otherwise, the field is blank. 
The most common reason for enhanced matching is that a trade falls within money tolerances and 
matches on the [[Seller]]’s value.
Trd Typ 
(Trade Type)
Indicates the type of trade submission:
 l Bilateral (BIL)
 l QSR target (QSR TGT)
 l [[syndicate]] (SYN)
 l [[syndicate]] target (SYN TGT)
 l QSR
Notes:
Although not referenced in the [[NSCC]] rules, this term is frequently used in the RTTM 
system to describe the submission type (e.g., bilateral, [[syndicate]] or QSR).
Subm Date
(Submission Date)
Date that the trade was submitted to the RTTM application. 
Note: If a trade remains unmatched (for example, the contraparty does not submit the 
corresponding trade details), they are removed from the Activity report after Submission Date+ 2.
Settle Date 
([[settlement]] Date)
Distribution date of the security. Also known as the Firm [[settlement]] Date.
If the trade was submitted as an extended [[settlement]] date trade, the [[settlement]] date will 
reflect the [[settlement]] date submitted by the [[participant]].
XREF
(external reference number)
[[participant]] submitted trade reference number.
TID
(Transaction [[ID]])
Reference number generated by the RTTM system and used to identify a specific 
transaction.
[[CUSIP]] (and description)Security description information is supplied by a third-party vendor and [[NSCC]] should not 
be held responsible for any errors or omissions in content.
Table 11.2  When Issued (WI) Activity - Non-Syndicated Transactions Field and Column Descriptions (Contin-
ued)
PrintImageActivityReports

---

## Page 39

11.WhenIssuedReport 39
Column/Field Name Description
Ext Day
(Extended [[settlement]] 
Days)
Number of days that a trade settles beyond the distribution date.
Price/Yield Numeric representation of the dollar price or yield figure submitted by the [[participant]].
P/Y/F
(Pricing Method)
Indicates whether the trade was submitted with a:
 l Dollar price = P
 l Yield = Y
 l Final money = F
Concess 
(Concession Rate)
For WI/[[syndicate]] trades only.
This field is applicable only if the [[participant]] selects Yield as the pricing method, and 
enters a concession. This field can be either + or -.
Buy/Sell Indicates whether you were on the buy or sell-side of a trade.
Note: 
The Buy/Sell indicator does not appear on the Regular Way, When Issued, When Issued 
Detail Transaction, and Regular Way Activity – [[OTC]]/[[UIT]] reports since this indicator is 
reflected in the Market field. 
Matched/Compared For Regular Way reports for MUNI and [[OTC]]/[[UIT]]:
 l Totals on these reports reflect all Matched/Compared submitted on trade date.
For WI Syndicates:
 l Matched/Compared totals includes all trades with a [[syndicate]] status of match and 
[[syndicate]], regardless of submission.
 l Includes the Total Par value of all Matched/Compared trades and their total final 
money amount.
Unmatched/Uncompared l For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all 
Unmatched/Uncompared submitted on trade date.
 l For When Issued (Non-[[syndicate]]) - All totals for Unmatched/Uncompared reflect 
current day’s submissions..
Advisories For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all 
Advisories submitted on trade date.
For WIs (Non-[[syndicate]]) - All totals for Advisories reflect current day’s submissions.
 l Totals Match/Unmatch 
on T for Regular Way
 l Totals Match/Unmatch 
on T for WI
 l Combined total number of trades (compared/matched and uncompared/unmatched) 
that have been submitted by your firm on trade date. Does not include trade rejects.
 l Same as Regular Way, but the totals include all of the trade dates.
Grand Totals Sum of all items.
Table 11.2  When Issued (WI) Activity - Non-Syndicated Transactions Field and Column Descriptions (Contin-
ued)
PrintImageActivityReports

---

## Page 40

12.TotalsattheEndofEachActivityReport 40
12. TOTALS AT THE END OF EACH ACTIVITY REPORT
At the end of each section is a Totals page. Each report, except the When Issued Detail Transaction report,  is grouped 
in the following manner:
 l Matched/Compared
 l Unmatched/Uncompared
 l Advisories
 l Totals Match/Unmatched/Advisories
Note
Regular Way only shows totals for trades submitted on trade date.  WI shows totals for all trades submitted that day.
Each group summarizes the # of items submitted by par and amount.
The following table shows the key points to remember:
Totals Key Points
Totals for the MUNI 
and [[OTC]]/[[UIT]] 
Reports
 l Totals on these reports reflect all Matched/Compared, Unmatched/Uncompared, and 
Advisories submitted on the trade date.
 l Buy/Sell sections of the report (except for the Comparison Only section) include only 
Matched, Unmatched, and Advisory trade status types. Cancels, DKs, and Memos are not 
included in the totals.
 l For the Comparison Only section, includes all comparison only trades.
When Issued 
[[syndicate]] Totals
 l Matched/Compared totals includes all trades with a [[syndicate]] Status of match and [[syndicate]] 
regardless of submission.
 l Unmatched and Advisories totals [[DO]] not apply to Syndicates.
 l Totals appear at the end of the report.
When Issued Non-
[[syndicate]] Totals
Totals are regardless of submission date, and include only Matched, Unmatched, and Advisory 
trade status types. Cancels, DKs, and Memos are not included in the totals.
When Issued Detail 
Transaction Totals
Groups trades in [[CUSIP]] order by [[CNS]] versus trade-for-trade (TFT), and then by the number of 
items, par, final money, and accrued interest.
PrintImageActivityReports

---

## Page 41

12.TotalsattheEndofEachActivityReport 41
Totals Page for MUNI, When Issued [[syndicate]] and Non-[[syndicate]], and [[OTC]]/[[UIT]] Reports
The totals page for the MUNI, When Issued, and [[OTC]]/[[UIT]] reports are the same. For an explanation of the fields and 
columns highlighted in the example Totals page, shown in the following figure,  see Table 12.1.  
The following table describes the columns and fields that appear on the Totals page for the reports:
Column/Field Name Description
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Market Indicates the market in which the trades occurred, such as MUNI, [[syndicate]], or [[UIT]], and 
their trade disposition, such as  buy, sell, or comparison only.
Matched/Compared For Regular Way reports for MUNI and [[OTC]]/[[UIT]]:
 l Totals on these reports reflect all Matched/Compared submitted on trade date.
For WI Syndicates:
 l Matched/Compared totals includes all trades with a [[syndicate]] status of match and 
[[syndicate]], regardless of submission.
 l Includes the Total Par value of all Matched/Compared trades and their total final 
money amount.
Unmatched/Uncompared l For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all 
Unmatched/Uncompared submitted on trade date.
 l For When Issued (Non-[[syndicate]]) - All totals for Unmatched/Uncompared reflect 
current day’s submissions..
Table 12.1  Totals Page: Field and Column Descriptions
PrintImageActivityReports

---

## Page 42

12.TotalsattheEndofEachActivityReport 42
Column/Field Name Description
Advisories For Regular Way Reports for MUNI and [[OTC]]/[[UIT]] - Totals on these reports reflect all 
Advisories submitted on trade date.
For WIs (Non-[[syndicate]]) - All totals for Advisories reflect current day’s submissions.
 l Totals Match/Unmatch 
on T for Regular Way
 l Totals Match/Unmatch 
on T for WI
 l Combined total number of trades (compared/matched and uncompared/unmatched) 
that have been submitted by your firm on trade date. Does not include trade rejects.
 l Same as Regular Way, but the totals include all of the trade dates.
Table 12.1  Totals Page: Field and Column Descriptions (Continued)
Totals Exhibit for When Issued Detail Report
For an explanation of the fields and columns highlighted in the example Totals page for the When Issued Details report, 
shown in the following figure,  see Table 12.2.  
The following table describes the columns and fields that appear on the Totals page for the reports: 
Column/Field Name Description
[[participant]] [[participant]]’s four-digit [[NSCC]] clearing number.
[[participant]] Name [[participant]]’s name as it is known on [[NSCC]] [[Broker]] Master File.
Table 12.2  Totals Page: Field and Column Descriptions
PrintImageActivityReports

---

## Page 43

12.TotalsattheEndofEachActivityReport 43
Column/Field Name Description
 l Totals 
Match/Unmatch on 
T for Regular Way
 l Totals 
Match/Unmatch on 
T for WI
 l Combined total number of trades (compared/matched and uncompared/unmatched) that 
have been submitted by your firm on trade date. Does not include trade rejects.
 l Same as Regular Way, but the totals include all of the trade dates.
Sett Disp
([[settlement]] Disposition)
Indicates how a matched trade is anticipated to settle. The values are:
 l [[CNS]] = [[CNS]] netting
 l TFT = trade for trade
 l NCN = balance order netting for corporate [[Bonds]] and UITs only. 
If no [[settlement]] disposition is assigned, the field is blank.
Quantity Quantity amount of the transaction.
Final Money Either the net [[settlement]] amount as submitted by the [[participant]] or as calculated by the 
RTTM system.
Accrued Interest Either the interest amount submitted by the [[participant]] or the calculated accrued interest if 
RTTM prices the trade.
Grand Totals Sum of all items.
Table 12.2  Totals Page: Field and Column Descriptions (Continued)
PrintImageActivityReports

---

## Page 44

13. COLUMN AND FIELD DESCRIPTIONS
The following table describes the columns and fields that appear on each of the CMU Activity reports accessible from the Report Center in the CMU RTTM 
Web application. For more information about accessing the CMU RTTM Web application, see the CMU RTTM Web User Guide. 
Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Processing Date Date and time the report was 
generated and produced by the 
RTTM system. Generally, the 
processing date and the 
business date are the same.
ü ü ü ü ü ü ü ü
[[participant]] [[participant]]’s four-digit [[NSCC]] 
clearing number.
ü ü ü ü ü ü ü ü
[[participant]] Name [[participant]]’s name as it is 
known on [[NSCC]] [[Broker]] Master 
File.
ü ü ü ü ü ü ü ü
Market Indicates the market in which 
the trades occurred, such as 
MUNI, [[syndicate]], or [[UIT]], and 
their trade disposition, such as  
buy, sell, or comparison only.
ü ü ü ü ü ü ü ü
Trade Date Date the trade was executed. ü ü ü ü ü ü ü ü
Orig Dlv Date
(Original Delivery Date)
[[settlement]] date submitted by 
the [[participant]].
N/A N/A ü ü N/A N/A N/A N/A
Corr 
(Correspondent)
Four-character [[NASD]] [[Broker]] 
symbol of the [[Broker]] that 
executed the trade.
ü ü ü ü N/A ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 44

---

## Page 45

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Contra Four-digit [[NSCC]] [[participant]] 
clearing number of the 
contraparty.
ü ü ü ü ü ü ü ü
Contra Corr
(Contra’s Correspondent)
Four-character [[NASD]] 
executing [[Broker]] symbol of your 
contraparty.
ü ü ü ü N/A ü ü ü
Quantity Quantity amount of the 
transaction.
ü ü ü ü ü ü ü ü
Final Money Either the net [[settlement]] 
amount as submitted by the 
[[participant]] or as calculated by 
the RTTM system.
ü ü ü ü ü ü ü ü
Accrued Interest Either the interest amount 
submitted by the [[participant]] or 
the calculated accrued interest 
if RTTM prices the trade.
N/A ü ü ü N/A ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 45

---

## Page 46

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Trd Stat 
(Trade Status)
Reflects the latest status of a 
trade:
 l UM * = Unmatched trade
 l AV * = Advisory state
 l MT = Matched trade
 l AVM * = Advisory Memo 
state
 l CXL = Canceled trade
 l AC = Canceled Advisory 
state
 l DK = DK state
 l ME* = Memo
Note: 
*UM, AV, AVM, and ME trades 
are continuously reflected on 
the report until the trade is 
either dropped or the status 
changes. See also ([[syndicate]] 
Status)
N/A N/A ü ü N/A N/A ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 46

---

## Page 47

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Sett Disp
([[settlement]] Disposition)
Indicates how a matched trade 
is anticipated to settle. The 
values are:
 l [[CNS]] = [[CNS]] netting
 l TFT = trade for trade
 l NCN = balance order netting 
for corporate [[Bonds]] and 
UITs only. 
If no [[settlement]] disposition is 
assigned, the field is blank.
N/A N/A ü ü N/A N/A N/A ü
Step Out 
(Step Out Indicator)
S indicates that the trade was 
submitted with a step in the Contra 
Trader [[ID]] field.
 l On unmatched trades, both 
the unmatched and advisory 
firms see the S indicator.
 l On matched trades, only the 
firms that submitted the S 
indicator see it.
 l If step was not submitted, 
the field is blank.
N/A N/A ü ü N/A ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 47

---

## Page 48

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
REV
(Reversal Indicator)
R indicates that a trade was 
submitted as a reversal; otherwise, 
the field is blank.
Notes:
 l Reversal is used to exactly 
offset a previously 
submitted matched trade 
that is no longer eligible for 
cancellation.
 l Bilateral reversal requires 
the contra side to submit for 
a match.
N/A N/A ü ü N/A ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 48

---

## Page 49

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Spl Ind
(Special Trade Indicator)
Indicates if a trade was 
submitted or assigned with any 
special [[settlement]] values that 
preclude it from [[CNS]] 
[[settlement]]/netting. The values 
are:
 l A = AAA security
 l F = Comparison only
 l B = Ex-legal
 l G = Bearer only
 l D = Ex-Interest
 l H = Registered only
 l E = Called
 l X = [[participant]] assigned 
trade for trade
Note: 
If a [[syndicate]] or WI trade is 
subsequently assigned a 
comparison only status after the 
initial submission date, the 
trade is updated to a status of 
comparison only (F). This most 
frequently occurs when the 
[[CUSIP]] for a matched [[syndicate]] 
or WI trade is canceled.
N/A N/A ü ü N/A ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 49

---

## Page 50

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Enh Mat
(Enhanced Match 
Indicator)
Y indicates that a trade was 
matched using RTTM 
enhanced matching; otherwise, 
the field is blank. The most 
common reason for enhanced 
matching is that a trade falls 
within money tolerances and 
matches on the [[Seller]]’s value.
N/A N/A ü ü N/A ü ü ü
Trd Typ 
(Trade Type)
Indicates the type of trade 
submission:
 l Bilateral (BIL)
 l QSR target (QSR TGT)
 l [[syndicate]] (SYN)
 l [[syndicate]] target (SYN TGT)
 l QSR
Notes:
 l Although not referenced in 
the [[NSCC]] rules, this term is 
frequently used in the RTTM 
system to describe the 
submission type (e.g., 
bilateral, [[syndicate]] or QSR).
 l * There is no specific column 
or field for trade type on the 
report, but the trade type is 
reflected in the report name.
N/A N/A ü ü N/A ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 50

---

## Page 51

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Subm Date 
(Submission Date)
Date that the trade was 
submitted to the RTTM system.
N/A N/A ü ü N/A ü ü ü
Settle Date 
([[settlement]] Date)
[[settlement]] date for a trade as 
submitted by the [[participant]] or 
assigned by [[NSCC]].
Note: 
If the trade is 
uncompared/unmatched, or if 
the [[settlement]] date is 
unavailable for a WI/[[syndicate]] 
trade, the [[settlement]] date is 
blank.
ü ü ü ü ü ü ü ü
XREF#
(external reference 
number)
[[participant]] submitted trade 
reference number.
ü ü ü ü ü ü ü ü
TID
(Transaction [[ID]])
Reference number generated 
by the RTTM system and used 
to identify a specific transaction.
ü ü ü ü N/A ü ü ü
[[CUSIP]] (and description)Security description information 
is supplied by a third-party 
vendor and [[NSCC]] should not 
be held responsible for any 
errors or omissions in content.
ü ü ü ü ü ü ü ü
Ext Day
(Extended [[settlement]] 
Days)
For WI Trades only.
Number of days that a trade 
settles beyond the distribution 
date.
N/A ü N/A N/A ü ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 51

---

## Page 52

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Price/Yield Numeric representation of the 
dollar price or yield figure 
submitted by the [[participant]].
N/A ü N/A N/A ü ü ü ü
P/Y/F
(Pricing Method)
Indicates the pricing method 
used in submitting a trade: 
 l P = dollar price*
 l Y = yield*
 l F = final money
Note: 
The Price and Yield methods 
apply only to WI/[[syndicate]] 
trades.
ü ü N/A N/A ü ü ü ü
Concess 
(Concession Rate)
For WI/[[syndicate]] trades only.
This field is applicable only if 
the [[participant]] selects Yield as 
the pricing method, and enters 
a concession. This field can be 
either + or -.
N/A ü N/A N/A ü ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 52

---

## Page 53

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Syn Stat 
([[syndicate]] Status)
Appears in the [[syndicate]] 
section of the WI Report, and 
reflects one of the following 
trade states:
 l SYN = Unmatched status
 l ME = Memo status
 l MT = Matched status
 l AVM = Memo advisory 
status
 l DK = DK status
 l AC = [[syndicate]] Manager 
Canceled
ü ü ü ü ü ü ü ü
Contra XREF# Trade reference number 
submitted by the contraparty.
ü N/A N/A N/A N/A N/A N/A N/A
Buy/Sell Indicates whether you were on 
the buy or sell-side of a trade.
Note: 
The Buy/Sell indicator does not 
appear on the Regular Way, 
When Issued, When Issued 
Detail Transaction, and Regular 
Way Activity – [[OTC]]/[[UIT]] reports 
since this indicator is reflected 
in the Market field. 
ü ü ü ü ü ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 53

---

## Page 54

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Purge Reason Values are:
 l DELE – Deleted due to the 
end of life of an 
Unmatched/ Uncompared 
trade.
 l DEDK – Deleted due to 
contra DK.
 l DEME – Deleted due to life 
of a When Issue Memo 
trade.
 l DEPE – Deleted due to life 
of a Pending (When Issue) 
trade.
 l DESE – Deleted due to 
security detail differences.
N/A ü N/A N/A N/A N/A N/A N/A
[[participant]] Totals
(on the Purge Report) (# 
Items, Sum of Par)
Total number of items that have 
been purged by RTTM and their 
total par value.
Note: 
Trades that are canceled by 
your firm [[DO]] not appear on the 
Purge Report, but [[DO]] appear on 
the Activity reports.
N/A ü N/A N/A N/A N/A N/A N/A
Price
(on the both Purge and 
Reject Reports)
For When Issued trades, done 
without final money.
N/A ü N/A N/A N/A N/A N/A N/A
PrintImageActivityReports
13.ColumnandFieldDescriptions 54

---

## Page 55

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Reject Reason
(on the Reject Report)
Indicates why a trade was 
rejected from the system. See 
Reject Reason Codes.
N/A N/A N/A N/A ü N/A N/A N/A
Create Date
(on the Reject Report)
Date that the trade was rejected 
by the RTTM system.
N/A N/A N/A N/A ü N/A N/A N/A
Total Items
(on the Reject Report)
Total number of trades rejected 
by the RTTM system on that 
day.
N/A N/A N/A N/A ü N/A N/A N/A
Matched/Compared For Regular Way reports for 
MUNI and [[OTC]]/[[UIT]]:
 l Totals on these reports 
reflect all 
Matched/Compared 
submitted on trade date.
For WI Syndicates:
 l Matched/Compared totals 
includes all trades with a 
[[syndicate]] status of match 
and [[syndicate]], regardless of 
submission.
 l Includes the Total Par value 
of all Matched/Compared 
trades and their total final 
money amount.
N/A N/A ü ü N/A ü ü N/A
PrintImageActivityReports
13.ColumnandFieldDescriptions 55

---

## Page 56

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
Unmatched/Uncompared l For Regular Way Reports 
for MUNI and [[OTC]]/[[UIT]] - 
Totals on these reports 
reflect all 
Unmatched/Uncompared 
submitted on trade date.
 l For When Issued (Non-
[[syndicate]]) - All totals for 
Unmatched/Uncompared 
reflect current day’s 
submissions..
N/A N/A ü ü N/A ü ü N/A
Advisories For Regular Way Reports for 
MUNI and [[OTC]]/[[UIT]] - Totals on 
these reports reflect all 
Advisories submitted on trade 
date.
For WIs (Non-[[syndicate]]) - All 
totals for Advisories reflect 
current day’s submissions.
N/A N/A ü ü N/A ü ü N/A
PrintImageActivityReports
13.ColumnandFieldDescriptions 56

---

## Page 57

Column/Field Name Description Enhanced 
Matching
PurgeRegular 
Way–
[[OTC]]/[[UIT]]
Regular 
Way–
MUNI
RejectWhen 
Issued–
[[syndicate]]
When 
Issued–
Non-
[[syndicate]]
When 
Issued 
Detail 
Transaction
 l Totals Match/Unmatch 
on T for Regular Way
 l Totals Match/Unmatch 
on T for WI
 l Combined total number of 
trades (compared/matched 
and 
uncompared/unmatched) 
that have been submitted by 
your firm on trade date. 
Does not include trade 
rejects.
 l Same as Regular Way, but 
the totals include all of the 
trade dates.
N/A N/A ü ü N/A ü ü N/A
Grand Totals Sum of all items. N/A N/A ü ü N/A ü ü ü
PrintImageActivityReports
13.ColumnandFieldDescriptions 57

---

## Page 58

FOR MORE INFORMATION
Email [[DTCC]] Learning at:
CoreLearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com