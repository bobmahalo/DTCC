---
title: "TIW Reporting and User Interface Changes"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/TIW%20Reporting%20and%20User%20Interface%20Changes.pdf"
pages: 16
size: "644.8 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# TIW Reporting and User Interface Changes

**Original File:** [TIW Reporting and User Interface Changes.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/TIW%20Reporting%20and%20User%20Interface%20Changes.pdf)  
**Category:** Other  
**Total Pages:** 16  
**File Size:** 644.8 KB  

---

## Page 1

TRADE INFORMATION WAREHOUSE
TIW Reporting and User Interface Changes
April 29, 2022

---

## Page 2

2
[[DTCC]] TIW – Reporting.  What [[DO]] you need to know?
Reporting 
Changes New Report Format Requirements [[DTCC]] TIW Legacy Value New [[DTCC]] TIW Value (standardized format)
HEADER
Format
All column names will be enclosed with double quotes 
and separated by a single comma (,)
"Product Type", "Product Type",
Any spaces would be trimmed, and the columns and 
data would be left aligned
"Matrix Transaction Type$“
($ symbol denotes Space)
"Matrix Transaction Type"
Spaces are not required after last header column 6179 spaces Not Required
Three Columns Blank in Legacy Following 3 columns are always blank in Legacy. "Affected 
Notional Amount", "Affected Notional Currency", "Affected 
Notional Transaction Type"
DDL is populating them for all PTE’s. 
"Affected Notional Amount", "Affected Notional Currency", "Affected 
Notional Transaction Type"
Regulatory Fields Regualtory fields may be populated Regulatory fields will be NULL
DATA
Format
All data will be enclosed with double quotes, trimmed 
for spaces and separated with a single comma at the 
end
“     " “”
Any spaces will be trimmed "CreditDefaultSwapShort$$$$$$$$",
($ symbol denotes Space)
"0000N8V3            " 
"CreditDefaultSwapShort“
"00001442"
All amount fields will be displayed in the report as 
stored in the DB and as in the inbound message
“     5000000.00000“
"         0.00000"
"5000000.00000“
"0.00000" (JPY Currency would be an exception here considering that we 
[[DO]] not use a decimal point for JPY)
Report fields with Rate, Price, Percent and 
Attachment/Exhaustion Point etc. will keep the 
precision intact as it comes in the inbound. For 
instance, if any of the above fields come with 7 decimal 
points, we will show 7 decimal points in the report
Fixed Rate: “     2.0000000000“
Reference Price: “     84.18084“
Independent Percent: "    25.00000 “
Attachment Point: "    15.00000 “
Exhaustion Point: "    100.00000 “
Recovery Price: "   10.0000000000“
Floating rate for initial calculation period: “ 0.00000“
Spread: "   .00000"
Fixed Rate: "2.0000000000“
Reference Price: "84.18084“
Independent Percent: "25.00000“
Attachment Point: "15.00000“
Exhaustion Point: "100.00000“
Recovery Price: "10.0000000000“
Floating rate for initial calculation period:"0.00000“
Spread: "0.00000"
Date Format will follow the ISO convention of YYYY -
MM-DD
Time Format 
"2018-01-08"
“01/06/2018”
04.24.51 
"2018-02-02" (ISO Format)
11:10:27
• Column names and order of existing TIW reports are not changing.
• Data contained within each field will be consistent with what you use today, with some minor exceptions.
• TIW will only contain Confirmed trades and as a result the Trade Status field will always be “Confirmed.” Lifecycle events that are 
“Reserved,” will have a Warehouse Status of either “Certain” or “Uncertain.”

---

## Page 3

3
Access / 
Login
• URL to login is the same as what’s used today.
• Login credentials are migrated from legacy to new TIW (i.e., there will be no change to your User [[ID]]).
• You will be contacted with respect to any other changes that could impact your login experience prior to go-live. 
Look & Feel
• Look has changed (different color schema) but feel is consistent with legacy.
• Navigation of the most used screens has not changed. For example, Dashboard, New Position Screen and Report 
Download Screens are the same.
Four Notable 
Changes
Restructuring Dashboard1 Search Menu2
Position Status Search3 Upload Screen4
Position Details5
[[DTCC]] TIW – GUI.  What [[DO]] you need to know?


---

## Page 4

4
Legacy State Restructuring Dashboard
Points to note:
• Delivered and Received message activity is consolidated into one GUI accordion.
• You must appropriately select “Apply as CEN” vs “Cancel NotifyCEN.”

---

## Page 5

5
New Restructuring Dashboard
Points to note:
• Created separate accordions / sections to segregate between “Delivered” and “Received” messaging activity for 
Triggers and Movements.
• “Apply as CEN” button is placed with “Message Activity - Received” accordion allowing users to apply CEN.
• “Cancel Notify CEN” button is placed with “Message Activity - Delivered” accordion allowing users to cancel notify CEN.


---

## Page 6

6
Legacy State Search Menu
Points to note:
Legacy search options are extensive and relate to both matching and [[settlement]] related data attributes.

---

## Page 7

7
New Search Menu
Points to note:
• Search menu has been reduced from 18 templates to 6.
• Each search template relates to the lifecycle event data that the Trade Information Warehouse stores. For example, 
Position and Netting related queries.

---

## Page 8

8
New Position Search Menu
Points to note:
• Position search menu has been enhanced so that a user can search on the “Warehouse Sub-state.” This allows you to 
filter trades based on one of the inactive states (For example, Terminated and Assigned).
• “Status” lookup has been removed from the screen – DDL only contains “Confirmed” trades.


---

## Page 9

9
Legacy State Upload Screen
Points to note:
Allows for the upload of trades – in the target state TIW this will change to only Adherence, Triggering and CalcFlag.


---

## Page 10

10
New Upload Screen
Points to note:
• The “Upload File” Function only allows you to upload your Adherence population, Triggering, Movement and Calc Flag. 

---

## Page 11

11
Legacy Position Detail Screen
Points to note:
Trade is displayed at a Transactional level.


---

## Page 12

12
New Position Detail Screen
Points to note:
Lifecycle Event Information displays activity on your position (i.e., Trade, Assignment, Termination).


---

## Page 13

13
Sr # GUI Area Functional 
Area TIW (Legacy) DDL
1 Restructuring 
Dashboard Restructuring
1) Delivered and Received activity is 
consolidated into one GUI accordion. 
2) User has to appropriately select 'Apply 
as CEN' vs 'Cancel NotifyCEN'.
1) Created separate accordions / sections to segregate between 'Delivered' and 
'Received' messaging activity for Triggers and Movements.
From a [[participant]] perspective, it is visually easier in DDL to separate and understand 
delivered vs received activity from
2) 'Apply as CEN' button is placed with 'Received' accordion allowing user participants 
to Apply CEN
3) 'Cancel Notify CEN' button is placed with 'Delivered' accordion allowing user to 
cancel notifyCEN.
2 GUI Menu Search' Menu
Search options are - a) General b) 
Backload search c) Assignment d) 
Reference entity e) Workflow field f) Latest 
Submission g) Best match h) Event driven 
termination i) Workflow tool j) Warehouse 
push k) unconfirmed fee l) Disable m) 
Inactive n) Pre-warehouse o) Bulk 
Amendment p) Cleared Search q) 
Reporting search r) Block trade search
Search menu has options for - a) Position Search b) Workflow field search c) Cleared 
Search d) Adherence search e) Net Payment search f) Net Payment history. 
Other search options are not built in DDL requirement.
3 GUI Menu
Search Menu -> 
Position Search 
page
1) in TIW, there is no warehouse substate 
concept. Trades become inactive as a part 
of state change and hence search is based 
on 'Inactive' trades
1) 'Warehouse sub state' added to the selection criteria. This allows [[participant]] to filter 
trades based on one of the specific inactive states - Terminated, Assigned, Matured, 
Exercised etc.
2) 'Status' lookup removed from the screen as we are only going to have 'confirmed' 
trades in DDL (So there is no relevance of having Unconfirmed, Alleged etc. search in 
DDL)
4 GUI Menu Transaction 
Form Menu
1) Transaction Form menu in TIW allows to 
initiate PTEs - Termination, Assignment, 
Disable etc. 
1) Transaction Form menu only has an [[Option]] of 'Trade Adherence' that pulls up 
positions in the warehouse and allows the participants to perform bulk adherence for 
selected positions and selected events.
2) All other 'Transaction Form' menu options removed from DDL as DDL won't allow 
capturing Trades and PTE manually as is the case in the legacy TIW system.
5 GUI Menu Download' 
menu
1) Download only has the [[Option]] of 'Download Search Results' 
2) There are no options for 'Bulk Amendment' and 'Spreadsheets' 
[[DTCC]] TIW - GUI Changes

---

## Page 14

14
Sr # GUI Area Functional 
Area TIW (Legacy) DDL
6 GUI Menu Uploads menu
Upload menu has 
options for - a) Upload 
b) Bulk upload c) 
Reactivate upload
Upload menu has options for - a) Upload file (allows bulk upload) and b) upload history
7 GUI Menu Web User 
Guide Menu
Web user guide has 
link to 'Credit user 
guide'
Credit user guide is not yet created and built. There is no link to Web user guide as yet in DDL. 
8 GUI Menu Reports Menu Reports menu has 2 options - a) Report download b) Adhoc Reports
9 GUI Menu
Restructuring 
Dashboard 
Menu
Not present in TIW New menu item 'Restructuring Dashboard' is added to top level menu that takes user participants directly to 
Restructuring Dashboard screen.
10 Dashboard DDL 
Dashboard
1) TIW has 
'Warehouse - Copper' 
dashboard
1) Dashboard has 4 widgets - a) DDL - Credit b) DDL - [[settlement]] c) DDL - Event Processing b) DDL -
Restructuring. 
2) There is no widget for 'Warehouse - Copper' as you see in TIW (given that all position are 'Gold' contract 
in DDL)
11 Position 
Details
Position Search 
Results
a) Position search results displayed in DDL have following columns - Trade Date, Product type, Ref 
Number, [[participant]] [[ID]], Counterparty [[ID]], Underlying, Fixed Rate, Amount, Position type.  These columns are 
more or less in line with existing TIW columns
b) These columns are removed from DDL as all trades are captured in DDL as confirmed positions-
Status, Warehouse Pushed, Warehouse status, Select transactions to compare, Msg
12 Position 
Details Position View
a) There is no life cycle 
events accordion in 
TIW. Different 
accordions are shows 
based on the type of 
PTE performed on the 
position.
a) 'Life Cycle Event Information' accordion added that lists down all the PTEs and life cycle transactions in a 
chronological order. All these transactions are expandable and displays the details of each PTE. When user 
clicks on a particular row, it dynamically renders the data for position, workflow fields etc. that is relevant at 
that point in time.
b) Following 3 accordions are removed from DDL as 'Reporting fields / parameters' not in scope for DDL
Reporting Summary
Reporting Fields
Counterparty Reporting Fields
c) 'Warehouse - Event Adherence' accordion added that encapsulates manual event adherence.
[[DTCC]] TIW - GUI Changes

---

## Page 15

15
Sr # GUI Area Functional 
Area TIW (Legacy) DDL
13 Position 
Details
Position View -
Amendment 
Comparison
Not present in TIW
a) 'Compare' functionality is introduced in DDL wherein user can select 2 amendment records / trade & 
amendment record etc. and compare all economic and non-economic details side by side. All 
differences between versions are highlighted.
14 Reports Reports-> Ad 
hoc Reports 
1) Ad hoc reports selection 
has different options in TIW
a) DDL supports options for - 21 Day cashflow report, Adherence status report by account, Credit daily 
activity report, Payment exception report, Position recon report
b) These reports are removed from DDL as not relevant -Unconfirmed transaction report, Alleged 
transaction report, daily activity report, daily rejected report, daily GTR error report, Real time net 
report, Central [[settlement]] eligibility report, TRIChange daily report, [[SEC]] Live backload prediction
15 Reports Reports -> 
report download a) No tabs for DSMatch vs TIW report download (As DSMatch functionality is discontinued in DDL)
[[DTCC]] TIW - GUI Changes

---

## Page 16

16
© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services. Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in which 
such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer.
Publication Code: DS350