---
title: "NoA Re-Write Participant Report"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Updates%20-%20Participant%20Reports%20July%2026th.%202023.pdf"
pages: 6
size: "229.3 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# NoA Re-Write Participant Report

**Original File:** [Working Group Updates - Participant Reports July 26th. 2023.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/Working%20Group%20Updates%20-%20Participant%20Reports%20July%2026th.%202023.pdf)  
**Category:** Other  
**Total Pages:** 6  
**File Size:** 229.3 KB  

---

## Page 1

North America Working Group – June 7, 2023 
Updated: June 21, 2023, July 26, 2023
GTR North America Re-Write Phase 2
[[participant]] Reports – Summary of Updates

---

## Page 2

[[DTCC]] Public (White)
[[participant]] Report Update Summary
[[CFTC]], [[SEC]], Canada
[[CFTC]], 
Canada [[CFTC]]
Submission 
Report
Trade 
State 
Report
Trade 
State 
Activity
Trade 
State 
Allege
PPD 
Status
Valuation 
Activity
[[collateral]] 
Activity
Counterparty 1 Identifier Source (Trade 
Party 1 - [[ID]] Type)*       
Clearing [[Member]] [[ID]] Source (Trade Party 
1 - Clearing [[Broker]] [[ID]] Type)*   
Unique Product Identifier (UPI)      
Other Payment Payer [[ID]] Type 
Other Payment Receiver [[ID]] Type 
There are several updates to the Report Layouts:
• New ingested fields added to the respective reports are listed below. 
• Fields no longer ingested will continue to be reported until a new submission in the North America 
Re-Write Phase 2 is processed. 
• There will be no removed [[participant]] or regulatory reporting fields as part of this implementation. 
• [[participant]] Report Layout Samples are included on the Learning Center.
*Submission reports will continue to use inbound field names for reporting. [Trade Party 1 - [[ID]] Type] has been updated to [Counterparty 1 identifier source] 
for the NoA Re-Write Phase 2 Implementation in reports as the Outbound field name. 

---

## Page 3

[[DTCC]] Public (White)
Trade State Report – Additional UPI Data Element 
Reporting
The following will be pulled by [[DTCC]] and included in Trade State Reports 
([[participant]] and Regulatory) based on the UPI submitted:
1. UPI-[[Asset]] Class
2. UPI-Instrument Type
3. UPI-Level
4. UPI-Product
5. UPI-Additional Sub Product
6. UPI-Base Product
7. UPI-Contract Specification
8. UPI-Debt Seniority
9. UPI-Delivery Type
10.UPI-Instrument ISIN
11.UPI-Instrument LEI
12.UPI-Notional Currency
13.UPI-Notional Schedule
14.UPI-[[Option]] Exercise Style
15.UPI-[[Option]] Type
16.UPI-Other Additional Sub 
Product
17.UPI-Other Base Product
18.UPI-Other Leg Reference 
Rate
19.UPI-Other Leg Reference 
Rate Term Unit
20.UPI-Other Leg Reference 
Rate Term Value
21.UPI-Other Leg Underlier 
Characteristic
22.UPI-Other Notional Currency
23.UPI-Other Reference Rate
24.UPI-Other Sub Product
25.UPI-Other Underlier 
Characteristic
26.UPI-Place of [[settlement]]
27.UPI-Reference Rate
28.UPI-Reference Rate Term Unit
29.UPI-Reference Rate Term 
Value
30.UPI-Return or Payout Trigger

---

## Page 4

[[DTCC]] Public (White)
Trade State Report – Additional UPI Data Element 
Reporting (con’t)
The following will be included in Trade State Reports ([[participant]] and Regulatory) 
based on the UPI submitted: 
41.UPI-Underlying instrument 
ISIN
42.UPI-Underlying instrument LEI
43.UPI-Underlying Instrument 
UPI
44.UPI-Underlying [[issuer]] Type
45.UPI-Valuation Method or 
Trigger
46.UPI-Last Update Date Time
47.UPI-Status
48.UPI-Status Reason
49.UPI-CFI Delivery Type
50.UPI-CFI [[Option]] Style and 
Type
51.UPI-Classification Type
52.UPI-Short Name
53.UPI-Single or Multiple 
Currency
54.UPI-Underlier Name
55.UPI-Further Grouping
56.UPI-DSB UPI
31.UPI-[[settlement]] Currency
32.UPI-Sub Product
33.UPI-Underlier Characteristic
34.UPI-Underlying [[Asset]] Type
35.UPI-Underlying Credit Index 
Series
36.UPI-Underlying Credit Index 
Version
37.UPI-Underlying Instrument 
Index
38.UPI-Underlying Instrument 
Index Prop
39.UPI-Underlying Instrument 
Index Term Unit
40.UPI-Underlying Instrument 
Index Term Value

---

## Page 5

[[DTCC]] Public (White)
APPENDIX: Report Types
Type Description
Trade State 
Report
• Contains the latest trade state for all open trades for each unique trade that contains the relevant jurisdiction value in the R eporting destination data 
element. 
• This report is created per [[Asset]] class per jurisdiction.
• Trades which expire on or after reporting date are included.  
• Trades which have been submitted with action type TERM or EROR (and not subsequently revived) or have been submitted with action type PRTO (and 
not ported back in) are not included (even if their expiration date is in the future).
• Trade valuation data is merged onto this report.  [[collateral]] valuation data is NOT merged onto this report.
Trade Activity 
Report
• Contains all successful submissions for trade state (not PPD/RT, valuation and [[collateral]]) message types that contain the relevant jurisdictional value in 
the Reporting destination data element.
• This report is created per [[Asset]] class per jurisdiction.
Submission 
Report
• Contains all the successful (ACK) and unsuccessful (NACK) submissions submitted by the client as well as those submissions made on their behalf. 
• This report is created per [[Asset]] class per jurisdiction.
• There will be a separate [[collateral]] submission report.
Public Price 
Status Report
• Contains all the successful PPD submissions received for the reporting date, as well as PPD submissions which may have been received on a previous 
date, but which were disseminated on the reporting date. 
• The PPD status report includes transformed (rounded, capped, scaled) values as well as original values submitted.
• This report is created per [[Asset]] class per jurisdiction.
Valuation Activity 
Report 
• Contains all successful Valuation submissions processed for the reporting date.
• This report is created per [[Asset]] class per jurisdiction.
• It will be provided to submitters, reporting parties, and regulators.
[[collateral]] Activity 
Report
• Contains all successful [[collateral]] Valuation submissions processed for the reporting date.  
• This report will be produced per jurisdiction (currently [[CFTC]] only).
• This report is not produced per [[Asset]] class as the content is not [[Asset]]-class specific.
• It will be provided to submitters, reporting parties, and regulators.
Trade State Allege 
Report
• Contains the latest trade state for all open trades for each unique trade that contains the relevant jurisdiction value in the R eporting destination data 
element where the report recipient is named as “Trade Party 2” 
• This report is created per [[Asset]] class per jurisdiction.
• Trades which expire on or after reporting date are included.  
• Trades which have been submitted with action type TERM or EROR (and not subsequently revived) or have been submitted with action type PRTO (and 
not ported back in) are not included (even if their expiration date is in the future).
• Trade valuation data and [[collateral]] valuation data are NOT merged onto this report.

---

## Page 6

[[DTCC]] Public (White)
APPENDIX: Report Cycle and Submission Cutoff
Report 
Date
Report 
Run Date Reporting Includes
Monday Tuesday All applicable submissions received between 00:00:00 ET Monday up to but not including 00:00:00 
ET Tuesday
Tuesday Wednesday All applicable submissions received between 00:00:00 ET Tuesday up to but not including 
00:00:00 ET Wednesday
Wednesday Thursday All applicable submissions received between 00:00:00 ET Wednesday up to but not including 
00:00:00 ET Thursday
Thursday Friday All applicable submissions received between 00:00:00 ET Thursday up to but not including 
00:00:00 ET Friday
Friday Saturday All applicable submissions received between 00:00:00 ET Friday up to but not including 00:00:00 
ET Saturday
Saturday Sunday All applicable submissions received between 00:00:00 ET Saturday up to but not including 
00:00:00 ET Sunday
Sunday Monday
All applicable submissions received between 00:00:00 ET Sunday up to but not including 00:00:00 
ET Monday