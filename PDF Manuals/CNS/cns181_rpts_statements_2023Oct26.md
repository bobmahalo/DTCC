---
title: "CNS Overview and Business Case"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns181_rpts_statements_2023Oct26.pdf"
pages: 81
size: "2040.8 KB"
category: "CNS"
ingested_on: "2026-06-05"
---

# CNS Overview and Business Case

**Original File:** [cns181_rpts_statements_2023Oct26.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cns181_rpts_statements_2023Oct26.pdf)  
**Category:** CNS  
**Total Pages:** 81  
**File Size:** 2040.8 KB  

---

## Page 1

[[CNS]]®
REPORTS AND STATEMENTS
NOVEMBER 12, 2020

---

## Page 2

TABLE OF CONTENTS
Preface 7
Objectives 7
Changes in This Version of the Document 8
Related Documents 8
Contact Us 8
1. [[CNS]] Overview 9
What is the [[CNS]] System? 9
Terms and Abbreviations 10
[[CNS]] Benefits 12
Example of Netting in the [[CNS]] System 12
How Does the [[CNS]] System Work? 14
What is the Role of [[DTC]] in the [[CNS]] System? 15
Reports and Statements Generated by [[CNS]] Processing 17
Business Case Outline 20
2. Part One—April 28 21
Consolidated Trade Summary (Cycle 1) 23
CNSReportsandStatements
TableOfContents 2

---

## Page 3

Consolidated Trade Summary (Cycle 1) Fields 25
Projection Report 27
Projection Report Field Descriptions 27
Project Report Example 29
[[CNS]] Extension Guidelines 29
Night Miscellaneous Activity 30
Position Prior to the Night Cycle 31
Position Prior to Night Cycle Example 32
Night [[settlement]] Activity Report 33
Night [[settlement]] Activity Field Descriptions 33
Night [[settlement]] Activity Example 34
Preliminary Cash Reconciliation – Night 36
Money Recap 36
Market Value Recap 37
[[settlement]] Reconciliation 37
Example 38
Money Recap 40
CNSReportsandStatements
TableOfContents 3

---

## Page 4

Market Value Recap 40
[[settlement]] Reconciliation 41
Position Prior to the Day Cycle 42
Position Prior to Day Cycle   Field Descriptions 42
Position Prior to Day Cycle Example 43
Day [[settlement]] Activity 44
Day [[settlement]] Activity     Field Descriptions 44
Day [[settlement]] Activity Example 45
Final Cash Reconciliation – Day 46
Accounting Summary 47
Accounting Summary Fields 47
Accounting Summary Example 49
Final Page (Totals) 50
Accounting Summary Fields 50
Accounting Summary Final Page (Totals) Example 52
[[NSCC]]   [[participant]]   Activity Balances 53
Accessing the Statement 53
CNSReportsandStatements
TableOfContents 4

---

## Page 5

Reviewing the Statement 55
3. Part Two—April 29 57
Consolidated Trade Summary 58
CTS Report Fields 59
Example 61
Projection Report 62
Example 62
Position Prior to the Night Cycle 64
Position Prior to Night Cycle Example 64
Night [[settlement]] Activity Report 65
Night [[settlement]] Activity Example 65
Preliminary Cash Reconciliation Report – Night 66
Example 66
Money Recap 66
Market Value Recap 68
[[settlement]] Reconciliation 69
Position Prior to the Day Cycle 70
CNSReportsandStatements
TableOfContents 5

---

## Page 6

Position Prior to Day Cycle Example 70
Day [[settlement]] Activity Report 71
Day [[settlement]] Activity Example 71
Final Cash Reconciliation – Day 72
Cash Reconciliation Report – Day Example 72
Accounting Summary 73
Example 73
Final Page (Totals) 74
Accounting Summary Totals Example 75
[[NSCC]]   [[participant]] Activity Balances 76
Accessing the Statement 76
Reviewing the Statement 78
CNSReportsandStatements
TableOfContents 6

---

## Page 7

PREFACE
The primary purpose of this guide is to familiarize National [[securities]] Clearing Corporation ([[NSCC]]) members with the [[CNS]]® system for continuous 
net [[settlement]]. 
This guide is not intended to serve as a legal document. All brokerage firms and [[Member]] numbers are fictional and used for illustration only. No 
statement in this guide should be construed as a legally binding rule or [[regulation]], or as creating an obligation on the part of [[NSCC]] or any person. 
See the Rules & Procedures for [[NSCC]] and other applicable parties for the legal [[obligations]] of all parties concerned. 
Objectives
This guide is designed to familiarize you with the [[CNS]] system, including reports, statements, and functions in [[CNS]] processing. Its purpose is to 
enable you to:
 l List all of the reports that are used to complete and balance daily settlements.
 l Explain each report, its function, and how it relates to each step in the [[settlement]] process.
 l Explain how the netting process works.
 l Explain what is reported on the Consolidated Trade Summary (CTS) report.
 l Distinguish between [[CNS]] and Non-[[CNS]] transactions.
 l Explain the importance of the Day/Night Miscellaneous Activity reports.
 l Explain the preliminary and final Cash Reconciliation reports and the [[settlement]] Activity reports for night and day.
CNSReportsandStatements
Preface 7

---

## Page 8

Changes in This Version of the Document
This version of the document includes an overall update to the template and numerous content changes to align with the latest version of the [[CNS]] 
system.
Related Documents
For related documents, in the [[DTCC]] Learning Center, go to Equities Clearing   - [[CNS]]® section of the Learning Center.
Contact Us
Use the following [[NSCC]] contacts for information about [[CNS]]. You can also contact your [[DTCC]] Relationship Manager or obtain general assistance 
by visiting the [[DTCC]] Client Center.
For... Contact...
General questions and product support [[NSCC]] Support by email at NSCCSupport@[[DTCC]].com.
Setup and testing     [[NSCC]] Integration by email at NSCCIntegration@[[DTCC]].com.
Issues with logging on to the system [[DTCC]] Client Support. Call the following number, and then follow the prompt for product support.
 o For US and Canada, call 1 888–382–2721.
 o For the UK, Europe, and Asia, call +1 212–855–8099.
CNSReportsandStatements
Preface 8

---

## Page 9

1. [[CNS]] OVERVIEW 
This section describes the [[CNS]]® system and includes commonly used terms throughout the guide, high-level [[CNS]] workflows and examples, and a 
brief description of the generated reports. It also includes an overview of a   multiday business case of a fictional [[Member]]'s transactions settling in the 
[[CNS]] system over two consecutive business days.
What is the [[CNS]] System?  
The [[CNS]] system is a continuous net [[settlement]] accounting and balancing system operated by the National [[securities]] Clearing Corporation ([[NSCC]]) 
that is the standard for settling equities, fixed-income, and other eligible [[securities]] at the Depository Trust Company ([[DTC]]).   [[CNS]] derives trade 
inputs from various marketplaces and other sources for a single [[settlement]] date and nets them to one position per security (long or short) per 
[[Member]] (you). The [[CNS]] system is an ongoing process; it perpetually nets a current day's settling trades with the prior business day's closing 
positions and other miscellaneous activity, producing new long or short positions per security for you each day. 
As a result, your net position in a given security is the difference between your buys and sells due to settle that day and the previous day's fail-to-
settle position. [[NSCC]] passes your [[CNS]] positions against your designated [[DTC]] positions and available [[securities]] are allocated through [[book-entry]] 
movements at [[DTC]]. In the [[CNS]] system, [[NSCC]] becomes the contra side of each compared trade. This allows you to trade large volumes of eligible 
[[securities]] with multiple [[Broker]]/dealers, but ultimately settle one net position per issue with one counterparty—[[NSCC]]. [[NSCC]] becomes the [[Buyer]] to 
every [[Seller]] and the [[Seller]] to every [[Buyer]] from a fixed point in the clearance and [[settlement]] process, in accordance with its Rules & Procedures. 
CNSReportsandStatements
1.CNSOverview 9

---

## Page 10

Terms and Abbreviations
The following table describes terms and abbreviations used throughout this guide:
Term or 
abbreviation
Description
CTS Consolidated Trade Summary—A report comprised of three cycles. See Consolidated Trade Summary (Cycle 1). 
[[Member]] [[participant]] in the [[NSCC]]. In this guide, the [[Member]] is you with the Training Account identifier.
[[PBS]] [[participant]] Browser Services—A [[DTC]] web-based system that gives you access to all depository processing functions.
position, long vs. 
short
[[CNS]] system implements long and short positions as follows:
 l Long position—Indicates the number of units of a security you are entitled to receive from the [[CNS]] system.
 l Short position—Indicates the number of units of a security you are obligated to deliver to the [[CNS]] system.
position, open vs. 
closed
[[CNS]] implements open and closed positions as follows:
 l Open position—Indicates a position in the [[CNS]] system that is not settled. In the [[CNS]] system, both open long and 
short positions are subject to continuous mark to market valuation until settled.
 l Closed position—Indicates a position in the [[CNS]] system that is settled.
[[PTS]] [[participant]] Terminal System—The terminal-based system that gives you access to all depository processing functions.
QSR Qualified Special Representative—An [[NSCC]] full service [[Member]] who has been granted status for the purpose of locking-in 
trades for other [[NSCC]] members and   their correspondents.
RTTM Real Time Trade Matching—A trade-entry and management tool that validates and matches   corporate bond, municipal 
bond, and unit investment trust ([[UIT]]) trades.
Table 1.1  Terms and abbreviations
CNSReportsandStatements
1.CNSOverview 10

---

## Page 11

Term or 
abbreviation
Description
[[settlement]] date The [[settlement]] date (SD) is the date on which a trade settles. To demonstrate the ongoing net [[settlement]] features of the 
[[CNS]] system using a business case, this guide includes two days as [[settlement]] dates:
 l Part One—April 28
 l Part Two—April 29
UTC Universal Trade Capture—A [[NSCC]] service that validates and reports [[Equity]] transactions that are submitted to [[NSCC]] by an 
exchange or by a Qualified Special Representative (QSR) that is an [[NSCC]] [[Member]].
CNSReportsandStatements
1.CNSOverview 11

---

## Page 12

[[CNS]] Benefits
When using the [[CNS]] system, you can take advantage of the following benefits:
 l Central fail control. All open fail positions, long or short, are marked to the current market value (marked to the market). A mark to the market 
represents the difference between the current market value and the original contract value.
 l Elimination of counterparty risk. At a fixed point in the clearance process, [[NSCC]] becomes the [[Seller]] to every [[Buyer]] and the [[Buyer]] to every 
[[Seller]] for all eligible [[securities]] settling in the [[CNS]] system.
 l [[Dividend]] and interest protection. Cash, [[Stock]] dividends, and bond interest are automatically debited or credited to your [[CNS]] account for open 
fail positions.
 l Minimal number of movements. By processing deliveries and receives through book entry movements, the [[CNS]] system reduces costs, min-
imizes paperwork, and can eliminate the number of physical deliveries.
 l Position protection. The [[CNS]] system provides operational facilities that protect [[securities]] involved in a corporate action such as reor-
ganization, [[Dividend]] distributions, and spin-offs.
Example of Netting in the [[CNS]] System
The following table shows an example of netting in the [[CNS]] system:
Security Counterparty
Account Number
# of [[shares]] 
Bought
# of [[shares]] 
Sold
Price per 
Share 
Debit AmountCredit Amount
XYZ 9901 100   63.875 $6,387.50  
XYZ 9902   200 63.625   $12,725.00
Table 1  Netting Example
CNSReportsandStatements
1.CNSOverview 12

---

## Page 13

Security Counterparty
Account Number
# of [[shares]] 
Bought
# of [[shares]] 
Sold
Price per 
Share 
Debit AmountCredit Amount
XYZ 9903 300   63.750 $19,125.00  
XYZ 9904 400   63.625 $25,450.00  
XYZ 9905 200   63.750 $12,750.00  
XYZ 2199   700 63.750   $44,625.00
Total   1,000 900   $63,712.50 $57,350.00
Net [[NSCC]] 100   $6,362.50 
In this example, the [[Member]] bought a total of 1,000 [[shares]] and sold a total of 900 [[shares]] of XYZ. The net position (1,000 minus 900) is a purchase 
of 100 [[shares]]. The dollar value of those [[shares]], after netting, is $6,362.50, which is subject to a mark to the market.
 l If allocation takes place on [[settlement]] day, this is the amount the [[Member]] pays.
 l If allocation does not take place on [[settlement]] date, the [[CNS]] system assigns the remaining failing position to mark to market. For example, if the 
share price on [[settlement]] date is $65.00, the [[CNS]] system sets the 100-share value to $6,500. The mark receives a credit of $137.50, which is 
the difference between the current market value and the contract value of this security ($6,500 Current Market Value less $6,362.50 Contract 
Value = $137.50 credit).
The netting procedure serves two key functions:
 l Saves members from having to handle each transaction individually.
 l Maintains mark to market value of open positions, which supports [[NSCC]]'s trade guarantee. It brings the original settling position up to the cur-
rent market value and   reduces market risk on that security position.
CNSReportsandStatements
1.CNSOverview 13

---

## Page 14

How Does the [[CNS]] System Work?
[[NSCC]] receives trades from exchanges and other trade sources such as Real Time Trade Matching (RTTM) engine or Qualified Special 
Representative (QSR). Then, it   validates and reports those trades to you throughout the trading day using the Universal Trade Capture (UTC) 
system. Within two business days of [[settlement]] date, [[NSCC]] provides a summary of all trades received for each security for you in the Consolidated 
Trade Summary (CTS) report. 
Eligible [[securities]] are forwarded to the [[CNS]] system. Trades ineligible for the [[CNS]] system either settle trade-for-trade or are included in the [[NSCC]] 
multi-lateral netted balance order process.
Each business day, the [[CNS]] system generates reports on the status and movement of [[securities]] through the clearance and [[settlement]] process. 
You can use these reports to balance daily [[settlement]] [[obligations]] and project settling positions for the following business day. The reports are made 
available as both print image and machine-readable-only (MRO) output files. For brief descriptions of the reports, see Reports and Statements 
Generated by [[CNS]] Processing.
In addition to reviewing activity through reports, you can also view the real-time [[CNS]] position for each security and a real time Cash Reconciliation 
report on the [[participant]] Browser Service ([[PBS]]). [[settlement]] balances can be viewed throughout the day and, for balancing at the end of day, 
through the following [[DTC]] access points:
 l [[NSCC]] [[participant]] Activity Balance on [[PBS]]
 l [[participant]] Terminal System ([[PTS]]) function SETP
CNSReportsandStatements
1.CNSOverview 14

---

## Page 15

What is the Role of [[DTC]] in the [[CNS]] System?
The [[CNS]] system uses the [[book-entry]] delivery facilities available at [[DTC]] to complete [[settlement]] [[obligations]]. After a transaction clears through 
[[NSCC]], the [[CNS]] system instructs [[DTC]] to deliver available [[securities]] from the delivering (or selling) account to the   [[CNS]] 888 account and then from 
the [[CNS]] 888 account to the receiving (or buying)     account. 
[[CNS]] processing for each [[settlement]] date day at [[DTC]] occurs in two processing cycles, which occur using Eastern Standard Time (EST). 
 l First is the night cycle, which occurs the night before [[settlement]] Date from approximately 8:15 P.M. to 10:45 P.M.
 l Second, processing continues again in the day cycle on [[settlement]] Date, which runs from approximately 6:30 A.M. until approximately 3:10 
P.M., provided there are no [[settlement]] extensions.
CNSReportsandStatements
1.CNSOverview 15

---

## Page 16

The following figure shows the flow of a typical security through the [[CNS]] system, from trade capture, to clearance by [[NSCC]], to release of [[securities]] 
by [[DTC]].
CNSReportsandStatements
1.CNSOverview 16

---

## Page 17

Reports and Statements Generated by [[CNS]] Processing
The following table lists the reports and statements generated by the [[CNS]] system and [[NSCC]].
Report/Autoroute 
#
When to 
use it
What it shows
Consolidated Trade 
Summary (Cycle 1)
Morning on 
SD-1
Breakdown, by security and market, of the net of all trade positions received by UTC at least two business 
days prior to [[settlement]] date. It also includes all trade positions received by UTC one business day prior to 
[[settlement]] date.
Consolidated Trade 
Summary (Cycle 2)
Early 
morning on 
SD 
After CTS Cycle 1 has been distributed and subsequent to midnight, Cycle 2 includes the breakdown, by 
security and market, of the net of all trade positions received by UTC at least two business days prior to 
[[settlement]] date. It also includes all trade positions received by UTC one business day prior to the [[settlement]] 
date. 
Note: One day settling trades reported at this time are actually settling that current business day [[settlement]] 
date
Consolidated Trade 
Summary (Cycle 3)
Midday on 
SD
Breakdown, by security and market, the net of all trade positions received by UTC on the current   [[settlement]] 
date after CTS Cycle 2 was distributed and subsequent to 11:30 A.M. Eastern Time. It also includes all trade 
positions received by UTC one business day prior to the [[settlement]] date after CTS Cycle 2 was distributed 
and 11:30 A.M. Eastern Time.
Projection Report Morning on 
SD-1
Displays the   projected netted positions, by security, for the following business day.
Position Prior to 
Night Cycle
Evening on 
SD-1
Displays the [[CNS]] settling positions in each security prior to the beginning of the night cycle.
Table 1.2  Output Generated for [[CNS]] Processing
CNSReportsandStatements
1.CNSOverview 17

---

## Page 18

Report/Autoroute 
#
When to 
use it
What it shows
Night [[settlement]] 
Activity
Morning of 
SD 
(after night 
cycle)
Displays the receives from the [[CNS]] system and delivers to the [[CNS]] system that occurred during the night 
cycle.
[Preliminary] Cash 
Reconciliation - 
Night
Morning of 
SD 
(after night 
cycle)
Displays the summary of all [[CNS]] money activity that occurred during the night cycle.
Night Miscellaneous 
Activity
Morning of 
SD 
(after night 
cycle)
Displays other transaction activity that updates a [[CNS]] position for each security processed before and 
during   the night cycle.
Position Prior to Day 
Cycle
Morning of 
SD 
(after night 
cycle)
Displays the [[CNS]] settling positions in each security prior to the beginning of the day cycle.
Day [[settlement]] 
Activity
Afternoon of 
SD 
(after day 
cycle)
Displays the receives from the [[CNS]] system and delivers to the [[CNS]] system   that occurred during the day 
cycle.
[Final] Cash 
Reconciliation - Day 
Afternoon of 
SD 
(after day 
cycle)
Displays the end-of-day summary of all [[CNS]] money activity.
CNSReportsandStatements
1.CNSOverview 18

---

## Page 19

Report/Autoroute 
#
When to 
use it
What it shows
Accounting 
Summary
Afternoon of 
SD (after day 
cycle)
Provides a summary, by security,   of all activity that occurred for that day.
[[NSCC]] [[participant]] 
Activity Balances
Throughout 
SD on 
[[settlement]] 
Web
Displays the final money amount for the [[CNS]] system and net money [[settlement]] obligation for that day.
Note: [[NSCC]] does not distribute this [[settlement]] information. Instead, view it from your online application.
CNSReportsandStatements
1.CNSOverview 19

---

## Page 20

Business Case Outline
This guide contains a two-part business case that describes [[CNS]] processing for nine initial trade positions.
 l Part One—April 28 is the first of two [[settlement]] dates for the trades. On April 28, you review [[CNS]] reports that were processed on April 26, 27, 
and 28. [[NSCC]] generates multiple versions of some of the reports, depending on the day, but the case reflects only a subset of those reports and 
statements.
 l Part Two—April 29 is the second of the two [[settlement]] dates for the trades when the final two of the nine trade positions settle and additional pos-
itions are added to your account. Similar to Part One-April 28, [[NSCC]] generates   some reports on April 28 and the balance on   April 29. You review 
and act on them on April 29.
When reading the business case, note the following:
 l Part One includes the field descriptions for the reports. For the same reports in Part Two, refer to the table of field descriptions in the Part One 
version of report.
 l The reports include ISIN identifiers. To derive the [[CUSIP]] identifier from an ISIN, take digits 3-11 from the ISIN identifier ([[DO]] not count the 
hyphens in the [[CUSIP]]). For example:
 o ISIN: US-Y8897Y305-4
 o [[CUSIP]]: Y8897Y305
 l All [[CNS]] processing occurs in Eastern Standard Time (EST).
CNSReportsandStatements
1.CNSOverview 20

---

## Page 21

2. PART ONE—APRIL 28
Today is the first of two [[settlement]] dates in this business case. For today, all reports and statements in Part One are tied to April 28 as the [[settlement]] 
date (SD). 
The following table lists the reports and statement that you manage on April 28 in this business case. As indicated in the Business Case Outline, you 
have received reports of activity about your settling positions in advance of today, April 28.   The expectation is that you review the reports and act on 
the information as appropriate. Among other reasons, two out of the nine trade positions [[DO]] not settle on April 28, thus requiring ongoing 
reconciliation by both [[NSCC]] and you.
Processed DescriptionDate Time
April 26  Not labeled Consolidated Trade Summary (Cycle 1) (one of three cycles)
April 27  00:34:30 Projection Report
Not applicable Night Miscellaneous Activity
April 27  19:26:52  Position Prior to the Night Cycle
April 27  23:04:27 Night [[settlement]] Activity Report
April 28  00:41:17 Preliminary Cash Reconciliation – Night 
April 28  00:36:48 Position Prior to the Day Cycle
Table 2.1  Part One—April 28 Reports
CNSReportsandStatements
2.PartOne—April28 21

---

## Page 22

Processed DescriptionDate Time
April 28  15:15:43 Day [[settlement]] Activity
April 28  15:43:93 Final Cash Reconciliation – Day 
April 28  15:18:03 Accounting Summary
April 28  Multiple [[NSCC]]   [[participant]]   Activity Balances
CNSReportsandStatements
2.PartOne—April28 22

---

## Page 23

Consolidated Trade Summary (Cycle 1)
The CTS contains a breakdown, by security and market, the net of all your trade positions received by UTC. The CTS reports   whether or not your 
netted positions settle in the [[CNS]] system. At the time of   a CTS cycle distribution, if [[securities]] are [[CNS]] eligible, typically those netted positions are 
also reported to the [[CNS]] system for processing. For netted positions that are not [[CNS]] eligible (or Non-[[CNS]]), [[NSCC]] reports them to the Balance 
Order Accounting system. [[NSCC]] distributes the   CTS in three cycles as shown in the following table:
Cycle Approximate 
Distribution
Reports trades received for [[settlement]] in:
1 9:00 P.M. Two business days and one business day.
2 Midnight Two business day and one-day trades received after CTS Cycle 1 and subsequent to midnight.
3 11:45 A.M. Same business day (same day settling trades received between CTS Cycle 2 and 11:30 A.M. Eastern Time). 
Additionally, one day settling trades received between CTS Cycle 2 and 11:30 A.M. EST.
After logging into the CTS Clearing Dashboard, you can access the main CTS [[settlement]] Date Totals page. The figure shows the Net Type tab for 
the [[settlement]] date of 04/28. [[Member]] 2199 [[DTCC]] Training Account has nine positions displayed in the Item Count column that are due to settle on 
April 28.   The aggregate amount of the purchases (buys) is $38,915.50. The aggregate amount of the sells is $6,468.27. One way to view the buy 
and sell details is to select the Symbol tab, as highlighted in the CTS [[settlement]] Date Totals figure. Next, click the diagonal arrow (
 ). From the 
page that opens, you can click   
  Export to download the aggregated buy and sell details by [[CUSIP]] to Microsoft Excel. 
Note
In this example, there is only one trade per security; therefore, this search displays all of the trades. However, when there is more 
than one trade in a security, you would search through the Inquiry tab. For more information about performing searches from the 
CTS Dashboard, see the Consolidated Trade Summary (CTS) Web-Based Inquiry Tool User Guide.
CNSReportsandStatements
2.PartOne—April28 23

---

## Page 24

When you click 
  Export from the CTS [[settlement]] Data Totals page, the details are export to a .csv file. The following figure shows an 
example file opened using Microsoft Excel:
CNSReportsandStatements
2.PartOne—April28 24

---

## Page 25

Consolidated Trade Summary (Cycle 1) Fields
The following table describes the columns available from the downloaded Excel file:
Field Description
[[participant]] [[ID]] Unique identifier of the [[NSCC]] [[participant]]. 
[[settlement]] Date Date on which a trade settles.
Symbol Alphabetical trading symbol of the security.
[[CUSIP]] Nine-digit alphanumeric identifier assigned by Standard & Poor’s [[CUSIP]] Service Bureau that uniquely identifies a secur-
ity.
ISIN International [[securities]] Identification Number of the security.
Item Count Number of trades in that security.
Net Quantity Net quantity of the trades in that security.
Net Amount Net amount of the trades in that security.
Symbol (%) Percentage of the trades in the symbol compared to all trades.
Buy Total Quantity Aggregate buy quantity in the security.
Sell Total Quantity Aggregate sell quantity in the security.
Buy Total Amount 
(USD)
Aggregate buy amount in the security.
Sell Total Amount 
(USD)
Aggregate sell amount in the security.
CNSReportsandStatements
2.PartOne—April28 25

---

## Page 26

As you can see, when you sum the columns for all nine [[securities]]:
 l You sold trades for a credit of $6,468.27.
 l You purchased trades for a debit of $38,915.50.
The Net Amount totals show that your trade [[settlement]] obligation in the [[CNS]] system is   a debit of $32,447.23.
CNSReportsandStatements
2.PartOne—April28 26

---

## Page 27

Projection Report
[[NSCC]] issues a daily [[CNS]] Projection Report. This report shows your   long and short positions for each security in various stages of [[settlement]]. It 
shows current positions (after night cycle), projects trades due to settle tomorrow, and lists   miscellaneous activity such as [[Stock]] dividends.
Long and short positions reflect the status in each security issue as of the time the Projection Report is prepared. These positions may change 
during the course of the [[settlement]] cycle on the day the report is issued. If your   long and short positions change during the day, the projected 
positions also change. Therefore, you must update these changed positions internally based on additional trades received and [[settlement]] activity 
that occurs throughout the day. Typically, members use the Projection Report to determine their [[CNS]] exemptions for settling short positions.
Projection Report Field Descriptions
The following table describes the fields in the Projection Report.
Field Description
Today's Current 
Position
[[CNS]] positions still open after completion of the [[CNS]] night cycle. One-day settling trades received for the current   set-
tlement date not covered or allocated in the [[CNS]] night cycle are included with positions reported under this column.
Tomorrow’s Settling 
Trades 
Purchased/Sold
Netted positions for trades settling tomorrow, corresponding to the Purchase Quantity and Sell Quantity columns on the 
Regular CTS Cycle 1 for the same [[settlement]] date.
Tomorrow’s [[Stock]] 
Dividends/Other 
Rec/Del
Netted positions resulting from [[Stock]] dividends or other miscellaneous activities such as corporate actions.
CNSReportsandStatements
2.PartOne—April28 27

---

## Page 28

Field Description
Tomorrow’s Projected 
Net Position 
Long/Short
Total of the previous three columns, showing the projected net position due for [[settlement]].
Tomorrow’s Projected 
Market Value 
LMV/SMV
Market value of the projected net positions in the previous column:
 l LMV—Long Market Value
 l SMV—Short Market Value
Currency Code Always USD (US Dollar).
ISIN ISIN identifier of the security. 
Note: The [[CUSIP]] identifier is comprised of digits 3-11 in the ISIN identifier. For example, if ISIN is US-Y8897Y305-4, 
the [[CUSIP]] is Y8897Y305.
Security Description Full name of the security.
CNSReportsandStatements
2.PartOne—April28 28

---

## Page 29

Project Report Example
Comparing the totals on the Projection Report with those on   the Consolidated Trade Summary (Cycle 1), the following figure shows that the 
[[securities]] have been marked to the market at the value of these [[securities]] at the time this report is produced. [[CNS]] updates the mark to market of all 
open positions again on [[settlement]] date.
[[CNS]] Extension Guidelines
If an extension is needed for any input submission, firms should use one of the following methods to obtain support:
 l Email [[NSCC]] Support at NSCCSupport@[[DTCC]].com.
 l Telephone [[DTCC]] Client Support at 1-888-382-2721 and follow the prompt for production support.
If [[DTCC]], at its sole discretion, extends a deadline that would significantly impact reporting times, a communication is sent out.
CNSReportsandStatements
2.PartOne—April28 29

---

## Page 30

Night Miscellaneous Activity
[[NSCC]] issues the Night   Miscellaneous Activity report on the morning of [[settlement]] date. It lists non-trade-related activity that was entered or 
removed from the [[CNS]] system before the night cycle began. Examples of non-trade related activity are as follows:
 l Reorganizations
 l Obligation Warehouse fails
 l Buy-ins
 l [[ID]] Net trades
 l Security exits resulting in [[CNS]] ineligibility and removal
In our business case, your Training Account does not have any night or day miscellaneous activity on April 28 and April 29.
If your account did have miscellaneous activity, then in the case of a security exit, the report lists the security removed from the [[CNS]] system. [[CNS]] 
then issues receive and deliver instructions to your account.
Additionally, [[NSCC]] also distributes a Day Miscellaneous Activity report   on the afternoon of [[settlement]] date. The report typically includes non-trade 
related activity processed during the day cycle such as reorganizations, Fully-Paid-For Account movements and [[ID]] Net Trades.
CNSReportsandStatements
2.PartOne—April28 30

---

## Page 31

Position Prior to the Night Cycle
The Position Prior to the Night Cycle report shows settling positions in each security prior to the beginning of the night cycle. The following table 
describes the fields in the Position Prior to Night Cycle report. 
Field Description
Today’s Net Opening 
Position Long/Short
Net opening position for each security. This is the same as the closing net position for each security position from 
prior business day as displayed on the Accounting Summary.
Today’s Settling Trades 
Purchased/Sold
Netted positions for trades settling for the current business day corresponding to the Purchased Quantity and Sell 
Quantity columns from the Regular CTS Cycle 1 and CTS   One Day [[settlement]] section (issued the day before 
[[settlement]] date).
Miscellaneous Activity 
/Rec/Del
Positions resulting from [[Stock]] dividends or other activities such as corporate actions or [[ID]] Net trades for the current 
business day.
Today’s   Net Position Prior 
to the Night Cycle 
Long/Short
Total of the previous three columns; shows the net position due for [[settlement]] in the night cycle.
Today’s Market Value 
Prior to the Night Cycle 
LMV/SMV
Market value of the net position in the previous column. This is the value of these [[securities]] at the time [[NSCC]] 
produces the report.
ISIN ISIN identifier of the security.   
Description Name of the security.
CNSReportsandStatements
2.PartOne—April28 31

---

## Page 32

Position Prior to Night Cycle Example
Comparing the totals on the Projection report and those on the Regular CTS Cycle 1, you can see in the Position Prior to Night Cycle report () that 
the [[securities]] have been marked to the market at the value of these [[securities]] at the time this report is produced. 
Description Field/Column Projection Report Position Prior to Night Cycle
Top Ships, Inc Credit Value $360.72 $347.36
Emerging Mkts Debit Value $2,980.00 $3,025.00
[[CNS]] performs another mark to market of the positions again on [[settlement]] date.
CNSReportsandStatements
2.PartOne—April28 32

---

## Page 33

Night [[settlement]] Activity Report
[[NSCC]] issues the Night [[settlement]] Activity report on [[settlement]] date and shows you the receives and deliveries of security positions to and from 
[[CNS]] and [[DTC]] during the night cycle.
Night [[settlement]] Activity Field Descriptions
The following table describes the fields in the Night [[settlement]] Activity report. 
Field Description
Received by [[CNS]]           Number of positions that have been delivered from your               [[DTC]] account into the [[CNS]] system.   
Delivered by [[CNS]]  Number of positions received by you into your [[DTC]] account   from the [[CNS]] system.
ISIN ISIN identifier for the security.
Description Full name of the security.
Current Price Today’s closing price of the security; it may be higher or lower than the contract price.
Long Market Value Today’s market value of items received by the [[CNS]] system.
Short Market Value Today’s market value of items delivered by the [[CNS]] system.
CNSReportsandStatements
2.PartOne—April28 33

---

## Page 34

Night [[settlement]] Activity Example
The report describes the [[settlement]] activity that occurred on your account during the night cycle. The following figure shows the example of seven of 
the nine open [[CNS]] positions closed. 
CNSReportsandStatements
2.PartOne—April28 34

---

## Page 35

There are still two open positions not shown on the report because they have not completed:
 l 167 [[shares]] of Top Ships, Inc that is still short (you owe) to the [[CNS]] system 
 l 250 [[shares]] of Emerging Mkts that are long (you expect to receive) in the [[CNS]] system
The activity during the night cycle represents the following:
Total long market value position  $6,234.32
Total short market value position  $37,252.50
Net total short market value $31,018.18
[[NSCC]] posts these values     to the subsequent Cash Reconciliation report (both Night and Day) on Line 14.
CNSReportsandStatements
2.PartOne—April28 35

---

## Page 36

Preliminary Cash Reconciliation – Night 
[[NSCC]] issues the preliminary Cash Reconciliation - Night report on the morning of [[settlement]] date. It summarizes all activity that occurred in the 
your account during the night cycle. [[NSCC]] issues this version after the night cycle, but before the day cycle begins. The preliminary Cash 
Reconciliation - Night report is divided into three sections: Money Recap, Market Value Recap, and [[settlement]] Reconciliation.
Money Recap
The following table describes the Money Recap section that contains all cash entries (debit or credit) on [[settlement]] date. 
Line # Field Description
1 Yesterday’s Closing Money Balance Previous day’s balance (Line 8 on yesterday’s final Cash Reconciliation - Day report).
2 Yesterday’s [[CNS]] Money [[settlement]] Previous day's [[settlement]] (Line 21 on yesterday's final Cash Reconciliation - Day report).
3 Today’s Settling Trades Trades that are due to settle today derived from all of the CTS reports (Cycles 1, 2, and 3).
4 Today’s Cash Dividends Dividends paid today.
5 Miscellaneous Money Entries Miscellaneous transactions (from the Night Miscellaneous Activity report).
6 Yesterday’s Clearing Deposit Always blank.
7 Today’s Clearing Deposit Always blank.
8 Today’s Closing Money Balance Total of Lines 1 through 5.
CNSReportsandStatements
2.PartOne—April28 36

---

## Page 37

Market Value Recap
The following table describes the Market Value Recap section that contains the market value of all security positions in the [[CNS]] system (long or 
short) on a given [[settlement]] date.
Line 
#
Field Description
9 Market Value of Today’s Opening 
Positions
Market value of positions in the [[CNS]] system that did not settle from the previous day.
10 Market Value of Today’s Settling TradesMarket value of trades due to settle today, at the current market value including mark to the 
market (compare with Line 3).
11 Market Value of Today’s [[Stock]] DividendMarket value of [[Stock]] dividends paid today (compare with Line 4).
12 Market Value of Today’s Miscellaneous 
[[Stock]] Entries
Dollar value of miscellaneous transactions (compare with Line 5).
13 Net Value Due to Settle Today Total of Lines 9 through 12.
14 Market Value of Last Night’s SettlementsMarket value of transactions that settled during the night cycle.
15 Net Value of Positions Still Open Net of Line 13 minus Line 14, showing what is due to settle in the [[CNS]] system before the day 
cycle begins.
[[settlement]] Reconciliation
The following table describes the   [[settlement]] Reconciliation section that contains the combined values of the Money Recap and Market Value 
Recap sections.
CNSReportsandStatements
2.PartOne—April28 37

---

## Page 38

Line 
#
Field Description
16 Today’s Closing Money 
Balance
Line 8 carried over.
17 Less Net Value of 
Open Positions
Line 15 carried over.
18 Current Money 
[[settlement]]
Difference between Lines 16 and 17, showing the preliminary amount due to settle.
19 Post Credit for Your 
Daytime Deliveries
Blank until day cycle ends. It appears on the final Cash Reconciliation - Day report.
20 Post Debit for Daytime 
Receives
Blank until day cycle ends. It appears on the final Cash Reconciliation - Day report.
21 Final [[CNS]] Money 
[[settlement]]
Blank until day cycle ends. It appears on the final Cash Reconciliation - Day report and as Code 82 on the final 
[[NSCC]] [[settlement]] Statement (see [[NSCC]]   [[participant]]   Activity Balances).
Table 2.2  [[settlement]] Reconciliation Descriptions
Example
The following figure shows an example of a preliminary Cash Reconciliation – Night report.
CNSReportsandStatements
2.PartOne—April28 38

---

## Page 39

CNSReportsandStatements
2.PartOne—April28 39

---

## Page 40

Money Recap
The Money Recap section of the report shows that you have a debit   of $32,447.23 for trades due to settle today (Line 3). This total is the net from   
the   Regular CTS Cycle 1 produced on April 26. If you fail to settle these positions during tonight’s night cycle, and they continue to fail after the day 
cycle completes, [[CNS]] marks to market the value of the [[securities]]   on today’s Accounting Summary. Today’s Closing Money Balance is the sum of 
Lines 1 through 8. This is the total amount of cash due to settle today as a result of [[CNS]] activity.
Market Value Recap 
The market value of all of your security positions in the [[CNS]] system today is shown in the Market Value Recap section. 
 l If you owe [[CNS]] for the security positions, the value is expressed as Short Market Value (SMV).
 l If [[CNS]] owes you for the security positions, the value is expressed as Long Market Value (LMV).
Note the following:
 l Line 10 shows an LMV of $40,235.00 and an SMV of $6,576.67, representing today’s settling trades. 
 l To determine the net value of positions that are still open before the day cycle begins (Line 15):
Line 13 shows the combined net value of all positions in Lines 9 through 12. 
Line 14 shows positions that were delivered or received by the [[CNS]] system during the night cycle but before the day cycle begins (see 
Night [[settlement]] Activity Report). Subtracting the values on Line 14 from those on Line 13 determines the net value of positions that are 
still open before the day cycle begins (Line 15). In this case, your account has an open long market value of $2,730.15.
CNSReportsandStatements
2.PartOne—April28 40

---

## Page 41

[[settlement]] Reconciliation
The totals on Lines 8 and 15 from each of the preceding two sections are carried over to Lines 16 and 17, respectively, in the [[settlement]] 
Reconciliation section. The total on Line 18 is the difference between Line 16 (credit) and Line 17 (debit). Your account’s current money [[settlement]] 
(Line 18) is a debit of $29,717.08.
On the preliminary Cash Reconciliation - Night report, Lines 19 and 20 always display asterisks because the day cycle has not yet completed. No 
figures appear here until [[NSCC]] issues the final Cash Reconciliation Statement - Day on the afternoon of [[settlement]].
CNSReportsandStatements
2.PartOne—April28 41

---

## Page 42

Position Prior to the Day Cycle
[[NSCC]] issues the Position Prior to Day Cycle report on [[settlement]] date (after the night cycle has completed) and shows the [[CNS]] settling positions in 
each security prior to the beginning of the day cycle.
Position Prior to Day Cycle  Field Descriptions
The following table describes the fields in the Position Prior to Day Cycle report. 
Field Description
Today’s Net Position Prior to Night 
Cycle Long/Short
Net opening position for each security before the night cycle. This is the same field from the Position Prior to 
the Night Cycle report.
Night Allocations Long/Short Long positions received by [[CNS]] or short positions covered to the [[CNS]] system that occurred during the night 
cycle.
Late Settling Trades Buy/Sell Trades received between Regular CTS Cycle 1 and subsequent to midnight for the current business day 
[[settlement]]. These trades appear on the CTS Cycle 2.
Miscellaneous Activity Rec/Del Positions resulting from [[Stock]] dividends or other activities such as corporate actions or [[ID]] Net trades for the 
current business day.
Today’s Net Position Prior to Day 
Cycle Long/Short
Total of the previous four columns that shows the net position due for [[settlement]] in the day cycle.
Today’s Market Value Prior to Day 
Cycle LMV/SMV
Market value of the net position in the previous column.
ISIN ISIN identifier of the security. 
Description Full name of the security.
CNSReportsandStatements
2.PartOne—April28 42

---

## Page 43

Position Prior to Day Cycle Example
The following figure shows that you have two open positions prior to the day cycle. They are:
 l 167 [[shares]] of Top Ships, Inc that are short (you owe to the [[CNS]] system).
 l 250 [[shares]] of Emerging Mkts that are long (you expect to receive from the [[CNS]] system).
CNSReportsandStatements
2.PartOne—April28 43

---

## Page 44

Day [[settlement]] Activity
[[NSCC]] issues the Day [[settlement]] Activity report on the afternoon of the [[settlement]] date (after [[CNS]] processing completes). It displays the [[CNS]] 
receives and delivers that occurred during the day cycle. 
Day [[settlement]] Activity   Field Descriptions
The following table describes the fields in the Day [[settlement]] Activity   report. 
Field Description
Received by [[CNS]]           Number of [[shares]] received by the [[CNS]] system during the day cycle.
Delivered by [[CNS]]  Number of [[shares]] delivered by the [[CNS]] system during the day cycle.
Description Full name of the security.
Current Price Current market price of the security.
Long Market Value Today’s market value of items received by the [[CNS]] system .
Short Market Value Today’s market value of items delivered by the [[CNS]] system .
CNSReportsandStatements
2.PartOne—April28 44

---

## Page 45

Day [[settlement]] Activity Example
In the following example, you made a partial delivery of 67 [[shares]] to the [[CNS]] system for Top Ships, Inc. 
Previously, you were 167 [[shares]] short and after this delivery of 67 [[shares]], you have a closing short position of 100 [[shares]] in this security. In the 
subsequent final Cash Reconciliation - Day report, you see a credit for the $137.35 value of the 67 [[shares]] (at $2.05 per share).
CNSReportsandStatements
2.PartOne—April28 45

---

## Page 46

Final Cash Reconciliation – Day 
The final Cash Reconciliation - Day report, issued on the afternoon of [[settlement]] date (after [[CNS]] processing completes), shows all information from 
the preliminary Cash Reconciliation - Night report plus day-time activity to arrive at a final [[settlement]] amount. All information is the same as that on 
the Preliminary Cash Reconciliation – Night  report, unless additional transactions are received for [[settlement]], such as same day settling trades or 
same day miscellaneous activity, by the time [[NSCC]] issues the report.
The following example shows a final partial Cash Reconciliation – Day report. 
CNSReportsandStatements
2.PartOne—April28 46

---

## Page 47

In the report, only Lines 19 through 21 differ on this report when compared to the preliminary Cash Reconciliation - Night report. 
 l Line 19, $137.35, is carried over from the Long Market Value column of the Day   [[settlement]] Activity report. No further positions were settled dur-
ing the day cycle. 
 l Line 21, $29,579.73, Final [[CNS]] Money [[settlement]], is the amount for you to settle with [[NSCC]]. Later in the business case, this amount also 
appears as a Code 82 on the   final [[NSCC]] [[settlement]] Statement (see [[NSCC]]   [[participant]]   Activity Balances).
Accounting Summary
[[NSCC]] issues the Accounting Summary on the afternoon of every business day after [[CNS]] processing has completed for the day. The report details 
all activity taking place in your [[CNS]] account. It is the primary record for controlling your firm’s [[CNS]] balancing and [[settlement]]. Activity is broken down 
by ISIN identifier.
Accounting Summary Fields
The following table describes the fields in the Accounting Summary. 
Field Description
ISIN ISIN identifier of the security.
Security Description Full name of the security.
Opening Position 
Long/Short
Today’s open position for you before any trades settled. 
Settling Trades 
Buy/Sell
The positions settling today. 
CNSReportsandStatements
2.PartOne—April28 47

---

## Page 48

Field Description
[[Stock]] Dividends/
Miscellaneous Activ 
Rec/Del
Non-trade-related security movements.
Receipts and 
Deliveries Rec/Del
Receipts by the [[CNS]] system from your [[DTC]] account and deliveries from the [[CNS]] system into your [[DTC]] account.
Closing Positions L/S Netting of opening netted positions, settling trades, [[Stock]] dividends and other miscellaneous activity, including receipts 
and deliveries.
Closing Market Price Price on which positions (long or short) are marked to the market, for the closing positions in the [[CNS]] system.
Current Market Value Closing position at the closing market price. Short closing positions result in a debit mark to the market, and long closing 
positions result in a credit mark to the market.
CNSReportsandStatements
2.PartOne—April28 48

---

## Page 49

Accounting Summary Example 
The following example shows the Accounting Summary:
All of the settling positions resulting from new settling trades were either delivered to or received by the [[CNS]] system, except the following:
 l Short position of 100 [[shares]] of Top Ships, Inc
 l Long position of 250 [[shares]] of Emerging Mkts 
CNSReportsandStatements
2.PartOne—April28 49

---

## Page 50

The Accounting Summary displays those two outstanding positions in the closing position L/S (-) column.
Final Page (Totals)
The final page of the Accounting Summary summarizes the money totals shown on the last report, Final Cash Reconciliation – Day  report. 
  Accounting Summary Fields
The following table describes the information in the three sections on the final page of the   Accounting Summary.
Field Description
Money Summary—Describes the fields in the final page of the report.
Yesterday’s Closing Balance From Line 1 of the [[CNS]] Final Reconciliation - Day.
Yesterday’s [[CNS]] [[settlement]] From Line 2 of the [[CNS]] Final Reconciliation - Day.
Today’s Opening Balance Difference between Line 1 and Line 2.
Settling Trades From Line 3 of the [[CNS]] Final Reconciliation - Day.
Cash Dividends and Interest From Line 4 of the [[CNS]] Final Reconciliation - Day.
Miscellaneous Activity From Line 5 of the [[CNS]] Final Reconciliation - Day.
Today’s Closing Balance From Line 8 of the [[CNS]] Final Reconciliation - Day.
Market Value Summary—A daily accounting of net market values from the previous pages of the Accounting Summary.
Long Market Value Total of all individual [[securities]] with long market value today.
CNSReportsandStatements
2.PartOne—April28 50

---

## Page 51

Field Description
Short Market Value Total of all individual [[securities]] with short market value today.
Net Market Value Net total of long and short market values.
[[CNS]] [[settlement]] Calculation—Net-net difference between money and market value balances.
Today’s Closing Balance Less Market Value Total carried down.
Today’s [[CNS]] [[settlement]] Difference between Today’s Closing Balance and Net Market Value.
CNSReportsandStatements
2.PartOne—April28 51

---

## Page 52

Accounting Summary Final Page (Totals) Example
The following example shows the final page of the Accounting Summary, which includes the current market values of [[securities]] shown on the 
previous page of the Accounting Summary. 
To arrive at a final net figure for [[settlement]] in the [[CNS]] system: 
Money Summary > Today's Closing Balance $32,447.23 
Market Value Summary > Net Market Value - $2,867.50 
[[CNS]] [[settlement]] Calculation > Today's [[CNS]] [[settlement]] $29,579.73(debit)
CNSReportsandStatements
2.PartOne—April28 52

---

## Page 53

[[NSCC]]  [[participant]]  Activity Balances
The [[NSCC]] [[participant]] Activity Balances provide details (by activity code) of all of your   money [[settlement]] debits and credits that are due on a 
particular [[settlement]] date. The [[CNS]] [[settlement]] Statement balance is represented by Code 82.   When [[CNS]] processing is complete, this is the same 
number that appears on the final Cash Reconciliation - Day report and Accounting Summary. 
The [[NSCC]] [[participant]] Activity Balances are available for viewing from the [[settlement]] Web Dashboard. Although you can view your balances 
throughout the day, [[NSCC]] posts the final balances after final figures are calculated at [[DTC]].
Accessing the Statement
The following figure shows how to access the [[NSCC]] [[participant]] Activity Balances. The first page on the function is your Settlements Statement: 
[[participant]] Accounts Statement. As shown in the red text in the upper-right corner of the page, Final Figures were posted at 15:40 (or 3:40 P.M.). 
To view the [[CNS]] code 082 balance for the day, click the arrow to the left of [[NSCC]] Totals, as highlighted in red in the [[participant]] Accounts 
Statement section.
CNSReportsandStatements
2.PartOne—April28 53

---

## Page 54

CNSReportsandStatements
2.PartOne—April28 54

---

## Page 55

Reviewing the Statement
This page shows the [[participant]] Accounts Statement for [[NSCC]] Totals. To view the [[CNS]] code 082 balance for the day, click the Activity Balance 
hyperlink, highlighted in the following figure, in the [[participant]] Accounts Statement section:
CNSReportsandStatements
2.PartOne—April28 55

---

## Page 56

The following figure shows that the Code 082 [[CNS]] Money [[settlement]] balance for your account is a debit of $29,579.73. 
This is the same balance in your April 28 Accounting Summary and your final Cash Reconciliation - Day report and the amount that you pay to 
[[NSCC]] for your [[CNS]] [[settlement]] activity.
CNSReportsandStatements
2.PartOne—April28 56

---

## Page 57

3. PART TWO—APRIL 29
The following table lists the reports and statement that you manage on April 29 in this business case. As indicated in the Business Case Outline, you 
have received reports of activity about your trade positions in advance of today, April 29.   The expectation is that you review the reports and act on 
the information as appropriate. Among other reasons, two out of the nine trade positions [[DO]] not settle on April 28, thus requiring   ongoing 
reconciliation by both [[NSCC]] and you.
Processed DescriptionDate Time
April 27 Not Labeled Consolidated Trade Summary (second of three cycles)
April 28  00:33:39 Projection Report
April 28  19:31:51 Position Prior to the Night Cycle
April 28  23:07:41 Night [[settlement]] Activity Report
April 29 00:21:26 Preliminary Cash Reconciliation Report – Night 
April 29  00:31:34 Position Prior to the Day Cycle
April 28  15:16:28 Day [[settlement]] Activity Report
April 28  00:00:00 Final Cash Reconciliation – Day
April 28  15:18:57 Accounting Summary
April 28 Multiple [[NSCC]]   [[participant]] Activity Balances
Table 3.1  Part Two—April 29 Reports
CNSReportsandStatements
3.PartTwo—April29 57

---

## Page 58

Consolidated Trade Summary
After logging into the CTS Clearing Dashboard, you can access the main CTS [[settlement]] Date Totals page. The figure shows the Net Type tab for 
the [[settlement]] date of 04/29/20XX. [[Member]] 2199 [[DTCC]] Training Account has ten positions displayed in the Item Count column   due to settle on 
April 29. The aggregate amount of the purchases (buys) was $38,294.00.   The aggregate amount of the sells was $24,074.55. 
One way to view the buy and sell details is to select the Symbol tab, and then click the diagonal arrow (
 ). From the page that opens, you can click   
 Export to download the aggregated buy and sell details by [[CUSIP]] to Microsoft Excel. 
Note
In this example, there is only one trade per security; therefore, this search displays all of the trades. However, when there is more 
than one trade in a security, you would search through the Inquiry tab. For more information about performing searches from the 
CTS Dashboard, see the Consolidated Trade Summary (CTS) Web-Based Inquiry Tool User Guide.
At the time of   a CTS cycle distribution, if [[securities]] are [[CNS]] eligible, typically those netted positions are also reported to the [[CNS]] system for 
processing. For netted positions that are not [[CNS]] eligible (or Non-[[CNS]]), [[NSCC]] reports them to the Balance Order Accounting system. 
CNSReportsandStatements
3.PartTwo—April29 58

---

## Page 59

When you click 
  Export, the details are export to a .csv file. The following figure shows an example file opened using Microsoft Excel:
CTS Report Fields
The following table describes the columns available from the downloaded Excel file:
Field Description
[[participant]] [[ID]] Unique identifier of the [[NSCC]] [[participant]]. 
[[settlement]] Date Date on which a trade settles.
Symbol Alphabetical trading symbol of the security.
[[CUSIP]] Nine-digit alphanumeric identifier assigned by Standard & Poor’s [[CUSIP]] Service Bureau that uniquely identifies a secur-
ity.
ISIN International [[securities]] Identification Number of the security.
Item Count Number of trades in that security.
Net Quantity Net quantity of the trades in that security.
CNSReportsandStatements
3.PartTwo—April29 59

---

## Page 60

Field Description
Net Amount Net amount of the trades in that security.
Symbol (%) Percentage of the trades in the symbol compared to all trades.
Buy Total Quantity Aggregate buy quantity in the security.
Sell Total Quantity Aggregate sell quantity in the security.
Buy Total Amount 
(USD)
Aggregate buy amount in the security.
Sell Total Amount 
(USD)
Aggregate sell amount in the security.
CNSReportsandStatements
3.PartTwo—April29 60

---

## Page 61

Example 
In the Consolidated Trade Summary, shown in the following figure, there are ten positions under ten different security symbol identifiers due to settle 
on April 29. 
The bottom of the report shows the totals and the net amounts for all ten [[securities]]:
 l You sold trades for a credit of $24,074.55.
 l You purchased trades for a debit of $38,294.00.
The Net Amount column shows that your trade [[settlement]] obligation in the [[CNS]] system is   a debit of $14,219.45.
CNSReportsandStatements
3.PartTwo—April29 61

---

## Page 62

Projection Report
[[NSCC]] issues a Projection Report after yesterday's night cycle for today’s [[settlement]]. It reflects netted positions known at the time of issuance that 
were due to settle today. For descriptions of the fields, see Projection Report.
Example
The following figure   shows the report issued yesterday morning after the night cycle. This report provides a summary of all of your netted positions 
projected to settle today. It also lists the current positions of [[securities]] from yesterday’s Projection Report that did not settle during the night cycle.
 Figure 1 Projection Report Example
CNSReportsandStatements
3.PartTwo—April29 62

---

## Page 63

This [[CNS]] Projection Report was issued after the night cycle was run for April 28 [[settlement]]. At the time the report was produced, it reported the 
open positions after the night cycle for the April 28 [[settlement]] and the projected positions reported on the CTS for April 29 [[settlement]]. When the 
Projection Report was processed, you had a short position of 167 [[shares]] of Top Ships, Inc. Remember, 67 of those [[shares]] were delivered later in 
the day cycle. Your long position of 250 [[shares]] of Emerging Mkts did not allocate and was a closing fail position after [[settlement]] completed on April 
28.
CNSReportsandStatements
3.PartTwo—April29 63

---

## Page 64

Position Prior to the Night Cycle
The   Position Prior to the Night Cycle report displays the opening position for each security   prior to the night cycle. The price used to determine the 
market value for each position is the same price used for each security from yesterday’s Accounting Summary. For descriptions of the fields, see 
Position Prior to the Night Cycle.
Position Prior to Night Cycle Example
The following example report shows the opening position for a short of 100 [[shares]] of Top Ships, Inc and the long position of 250 [[shares]] of Emerging 
Mkts. It also reports the net settling positions for April 29 [[settlement]].
CNSReportsandStatements
3.PartTwo—April29 64

---

## Page 65

Night [[settlement]] Activity Report
As shown earlier, on [[settlement]] date the Night [[settlement]] Activity report showed positions received and delivered during the night cycle. During the 
night cycle, there was [[settlement]] activity in your account described in the Example below. For descriptions of the fields, see Night [[settlement]] 
Activity Report.
Night [[settlement]] Activity Example
The following example shows that the activity occurring during this cycle represents total positions of a $26,100.00 long market value and a 
$10,907.50 short market value. [[NSCC]] posts these values   to the subsequent Cash Reconciliation reports—both Night (preliminary) and Day 
(final)—on Line 14. This results in a net total long   market value of $15,192.50. All other activity is still due to settle. 
CNSReportsandStatements
3.PartTwo—April29 65

---

## Page 66

Preliminary Cash Reconciliation Report – Night 
[[NSCC]] issues the preliminary Cash Reconciliation - Night report on the morning of [[settlement]] date.   It summarizes all activity that occurred in your 
[[CNS]] account during the night cycle. [[NSCC]] issues this version of the report after the night cycle but before the day cycle begins. The Money Recap 
section carries over totals from yesterday’s final Cash Reconciliation - Day report. For descriptions of the fields, see Preliminary Cash Reconciliation 
– Night .
Example
The following sections contain examples of the preliminary Cash Reconciliation - Night report, broken down by area of Money Recap, Market Value 
Recap, and [[settlement]] Reconciliation.
Money Recap
In the following example, the Money Recap section of the report shows that you have a debit   of $14,219.45 for trades due to settle today (Line 3). 
This total is the net from yesterday’s CTS. If you fail to settle these positions during tonight’s night cycle, and they continue to fail after the day cycle 
completes, the value of the [[securities]] is marked to the market on today’s Accounting Summary (Accounting Summary). 
CNSReportsandStatements
3.PartTwo—April29 66

---

## Page 67

CNSReportsandStatements
3.PartTwo—April29 67

---

## Page 68

Market Value Recap
In the following example, the Market Value Recap section of the report shows the market value of all of your security positions in the [[CNS]] system 
today.
The long and short market value dispositions are as follows for today's settling trades:
 l If your account owes [[NSCC]] security positions, the value is expressed as short market value (SMV). In this business case, Line 10 shows an LMV 
of $39,235.00 that you owe [[NSCC]].
 l If [[NSCC]] owes your account security positions, the value is expressed as long market value (LMV). In this business case, Line 10 shows an SMV 
of $26,100.00 that [[NSCC]] owes to your account.
Line 13 shows the combined net value of all positions in Lines 9 through 12. Line 14 shows positions that were delivered to or received by [[CNS]] 
during the night cycle but before the day cycle begins (see Night [[settlement]] Activity Report). Subtracting the values on Line 14 from those on Line 
13 determines the net value of positions that are still open before the day cycle begins (Line 15). In this case, your account has an open LMV of 
$31,305.00.
CNSReportsandStatements
3.PartTwo—April29 68

---

## Page 69

[[settlement]] Reconciliation
In Figure 3.2, the [[settlement]] Reconciliation section carries over 8 and 15 from each of the preceding two sections to Lines 16 and 17, respectively—
representing the market value of all of your security positions in the [[CNS]] system today.
 Figure 3.2  [[settlement]] Reconciliation
Today’s Closing Money Balance (Line 16) is the total amount of cash due to settle today as a result of [[CNS]] activity .
The total on Line 18 is the difference between Line 16 (credit) and Line 17 (debit). Your account's Current Money [[settlement]] (Line 18) is a credit of 
$14,218.05
Line 20 displays asterisks (*) because the day cycle has not yet completed. No amount appears on the line until [[NSCC]] issues the final Cash 
Reconciliation - Day report   during the afternoon of [[settlement]].
CNSReportsandStatements
3.PartTwo—April29 69

---

## Page 70

Position Prior to the Day Cycle
[[NSCC]] issues the Position Prior to Day Cycle report in the morning on [[settlement]] date   (after the completed night cycle). It shows you the [[CNS]] 
position in each security for your firm   prior to the beginning of the day cycle. For descriptions of the fields, see Position Prior to the Day Cycle.
Position Prior to Day Cycle Example
As shown in the following figure, after the completion of the night cycle, your account still has three open positions settling in the [[CNS]] system:
 l Short 100   [[shares]] of Top Ships, Inc
 l Long 600 [[shares]] of Alcoa Inc 
 l Long 2,060 [[shares]] of Emerging Mkts
CNSReportsandStatements
3.PartTwo—April29 70

---

## Page 71

Day [[settlement]] Activity Report
[[NSCC]] issues the Day [[settlement]] Activity report issued on the afternoon of [[settlement]] date (after [[CNS]] processing) and shows [[CNS]] receives and 
delivers that took place during the day cycle.   For descriptions of the fields, see Day [[settlement]] Activity. 
Day [[settlement]] Activity Example
As shown in the following figure, the three open positions that you had prior to the night cycle have now completed in the day cycle.
CNSReportsandStatements
3.PartTwo—April29 71

---

## Page 72

Final Cash Reconciliation – Day
[[NSCC]] issues the final Cash Reconciliation - Day - report on the afternoon of [[settlement]] day. For descriptions of the fields, see Final Cash 
Reconciliation – Day .
Cash Reconciliation Report – Day Example
The following example shows that the numbers on this report are the same as those on the Preliminary Cash Reconciliation Report – Night  report, 
except Lines 19 through 21:
 l Amount on Line 19 ($210.00) is carried over from the Long Market Value column of the Daytime [[settlement]] Activity report.
 l Amount on Line 20 ($31,515.00) is carried over from the Short Market Value column of the Daytime [[settlement]] Activity report.
 l Amount on Line 21 (debit of $17,086.95) is the amount for you to settle with [[NSCC]]. The next section shows this amount appears as a Code 82 
on the final [[NSCC]] [[participant]] Activity Balances (see Reviewing the Statement).
CNSReportsandStatements
3.PartTwo—April29 72

---

## Page 73

Accounting Summary
[[NSCC]] issues the Accounting Summary on the afternoon of every business day after [[CNS]] processing has completed for the day. The report details 
all activity taking place in your [[CNS]] account. It is the primary record for controlling your [[CNS]] balancing and [[settlement]] activity. For descriptions of 
the fields, see Accounting Summary.
Example 
The following figure shows that there are no outstanding positions in the Closing Position L/S(-) column. All positions have settled for your 
account.
CNSReportsandStatements
3.PartTwo—April29 73

---

## Page 74

Final Page (Totals)
The final page of the Accounting Summary summarizes the money totals shown on the last report, Final Cash Reconciliation – Day report. For 
descriptions of the fields, see Final Page (Totals) for Part One—April 28.
CNSReportsandStatements
3.PartTwo—April29 74

---

## Page 75

Accounting Summary Totals Example
The final page of the   Accounting Summary, as shown in the following figure, summarizes the money totals shown on the final Cash Reconciliation - 
Day report and current market values of [[securities]] shown on the previous page of the Accounting Summary. The market value is subtracted from 
the money summary to arrive at a final net amount for [[CNS]] [[settlement]].
To arrive at a final net figure for [[settlement]] in the [[CNS]] system: 
Money Summary > Today's Closing Balance $17,086.95 
Market Value Summary > Net Market Value $0.00 
[[CNS]] [[settlement]] Calculation > Today's [[CNS]] [[settlement]] $17,086.95(debit)
CNSReportsandStatements
3.PartTwo—April29 75

---

## Page 76

[[NSCC]]  [[participant]] Activity Balances
The [[NSCC]] [[participant]] Activity Balances provide details (by activity code) of all of your   money [[settlement]] debits and credits that are due on a 
particular [[settlement]] date. The [[CNS]] [[settlement]] Statement balance is represented by Code 82.   When [[CNS]] processing is complete, this will be the 
same number that appears on the final Cash Reconciliation - Day report and Accounting Summary. 
The [[NSCC]] [[participant]] Activity Balances are available for viewing through the Settlements Statement: [[participant]] Accounts Statement available 
from the [[settlement]] Web Dashboard. Although you can view your balances throughout the day, [[NSCC]] posts the final balances after final figures are 
calculated at [[DTC]].
Accessing the Statement
The following figure shows how to access the [[NSCC]] [[participant]] Activity Balances. The first page on the function is your Settlements Statement: 
[[participant]] Accounts Statement. As shown in the red text in the upper-right corner of the page, Final Figures were posted at 15:40 (or 3:40 P.M.). 
To view the [[CNS]] code 082 balance for the day, click the arrow to the left of [[NSCC]] Totals, as highlighted in red in the [[participant]] Accounts 
Statement section.
CNSReportsandStatements
3.PartTwo—April29 76

---

## Page 77

CNSReportsandStatements
3.PartTwo—April29 77

---

## Page 78

Reviewing the Statement
This page shows the [[participant]] Accounts Statement for [[NSCC]] Totals. To view the [[CNS]] code 082 balance for the day, click the Activity Balance 
hyperlink, highlighted in the following figure, in the [[participant]] Accounts Statement section:
CNSReportsandStatements
3.PartTwo—April29 78

---

## Page 79

The following figure shows that the Code 082 [[CNS]] Money [[settlement]] balance for your Training Account is a debit of $17,086.95. 
This is the same balance in your April 29 Accounting Summary and your final Cash Reconciliation - Day report and the amount that you pay to 
[[NSCC]] for your [[CNS]] [[settlement]] activity. 
Over the two-day period, the you bought [[securities]] settling on:
 l April 28 for $32,447.23 
 l April 29 for $14,219.45
The total paid for all [[securities]] was $46,666.68. To arrive at the total paid for all [[securities]]: 
CNSReportsandStatements
3.PartTwo—April29 79

---

## Page 80

April 28—You paid $29,579.73 (debit)
April 29—You paid $17,086.95 (debit)
Total paid for both [[settlement]] dates $46,666.68 (debit)
CNSReportsandStatements
3.PartTwo—April29 80

---

## Page 81

© 2023 [[DTCC]]. All rights reserved.   [[DTCC]], [[DTCC]] (Stylized) and Financial Markets. Forward. are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation [[DTCC]]. The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of 
The Depository Trust & Clearing Corporation (“[[DTCC]]”).   [[DTCC]] itself does not provide such services.   Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see   www.[[DTCC]].com for more 
information on [[DTCC]], its affiliates and the services they offer.
 
 
Doc Date: October 26, 2023
Publication Code: CNS181
Service: [[CNS]]
Title: Reports and Statements
For More Information
 
Email [[DTCC]] Learning at:
DTCCLearning@[[DTCC]].com
or visit us on the web at:
www.dtcclearning.com