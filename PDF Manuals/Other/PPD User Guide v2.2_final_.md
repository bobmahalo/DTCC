---
title: "PPD User Guide v2.2"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/PPD%20User%20Guide%20v2.2_final_.pdf"
pages: 15
size: "807.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# PPD User Guide v2.2

**Original File:** [PPD User Guide v2.2_final_.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/PPD%20User%20Guide%20v2.2_final_.pdf)  
**Category:** Other  
**Total Pages:** 15  
**File Size:** 807.6 KB  

---

## Page 1

 
Global Trade Repository 
PUBLIC PRICE DISSEMINATION DASHBOARD USER 
GUIDE 
VERSION 2.2 
OCTOBER 2023 
 
 

---

## Page 2

TABLE OF CONTENTS 
Document Revision History ................................................................................................................................ 3 
Overview ............................................................................................................................................................... 4 
Dashboards .......................................................................................................................................................... 5 
Search tab ............................................................................................................................................................. 8 
Report center ........................................................................................................................................................ 9 
Info Center .......................................................................................................................................................... 11 
APPENDIX A: Slice File Fields and Layout ..................................................................................................... 12 
 
  

---

## Page 3

DOCUMENT REVISION HISTORY 
Date Author Version Description 
September 28, 2020 AF 1.0 Initial Document 
December 4, 2020 AF 1.1 Addition of Appendix Field Descriptions 
October 22, 2021 VR 1.2 Section 2: Added capping details 
Section 3: Removed reference to cap number report 
 
August 1, 2022 JY 2.0 Updated for the North America Re-Write Changes, 
which goes live on December 2, 2022 
October 14, 2022 JY 2.1 Updated for Ticker and Search updates for the North 
America Re-Write. Minor update to RSS Feed. 
October 25, 2023 PC 2.2 Updated for new PPD Dashboard and UI changes 
 

---

## Page 4

OVERVIEW 
Public Price Dissemination (PPD) Website 
 
The Public Price Dissemination (PPD) website for derivative trades submitted to the [[CFTC]] (Commodity Futures 
Trading Commission), [[SEC]] (U.S. [[Securities and Exchange Commission]]) and Canadian jurisdictions can be 
accessed through the following URL:  https://pddata.[[DTCC]].com/gtr/dashboard.[[DO]] 
 
PPD Website Overview 
 
The PPD Website has seven main tabs and a link to this Quick Reference Guide.   The website will [[default]] to the 
Info Center.  
 
The tabs (which are described further in the sections below) are: 
 
• [[CFTC]] Dashboard: This tab contains the full details of real time transactions successfully submitted for 
[[CFTC]]. 
• [[SEC]] Dashboard: This tab contains the full details of real time transactions successfully submitted for [[SEC]]. 
• Canada Dashboard: This tab contains the full details of real time transactions successfully submitted for 
Canada. 
• Search: This screen allows for the use of filters to search for a particular transaction.  
• Report Center: This tab gives users access to prior ad hoc reports they have requested. 
• Info Center: This tab contains important messages to the user community. 
 
 
 
Available Derivative Data 
 
The PPD Website contains successfully submitted data for the following jurisdictions and [[Asset]] classes: 
 
Jurisdiction 
[[Asset]] Class 
Credit [[Equity]] Interest Rates FX Commodities 
[[CFTC]]      
[[SEC]]      
Canada      
 
The PPD website is available 7 days per week, 24 hours per day Monday through Sunday Scheduled 
maintenance is performed between 10:00 pm (ET) Saturday to 6:00 am (ET) Sunday for DDR systems. Please 
note while the PPD website will be available, PPD data successfully received during this time is queued and will 
not be published until after the scheduled maintenance period. All other functionality on the PPD website will be 
available to users during this time. 
 
On occasion, additional downtime may be required as necessary, to support time sensitive processes or 
maintenance occurring outside of Closed Hours. Data successfully received during DDR downtime is queued and 
processed once the service has resumed. Users will be notified of any additional downtime in the Info Center. 


---

## Page 5

DASHBOARDS 
 
The Dashboards are divided per jurisdiction: 
 
1. [[CFTC]] Dashboard 
2. [[SEC]] Dashboard 
3. Canada Dashboard 
 
Users must click on the respective jurisdiction link to see the PPD data related to that jurisdiction.  
 
 
 
Each jurisdiction’s dashboard has three tabs. The tabs (which are described further in the sections below) are:  
Slice Reports, Cumulative Reports and Ticker which are presented per [[Asset]] class.  
 
 
 
SLICE REPORTS TAB 
 
The Slice Reports contain all daily transaction and pricing data successfully reported during specific 
intervals, as defined by the “Slice Start” and “Slice End” times. There are individual Slice Reports for each 
[[Asset]] Class in scope for that jurisdiction. 
 
 
 
The PPD website “Slice Start”, and “Slice End” time is based on Coordinated Universal Time (UTC).  
 
To download a Slice Report (in CSV format): 
1. Select the desired [[Asset]] class tab. 
2. Click the desired report link. 
3. Save the zip file.  
 


---

## Page 6

CUMULATIVE REPORTS TAB 
 
The Cumulative Reports contain all transaction and pricing data successfully reported for a given date. Each 
day’s Cumulative Slice Report contains all transactions published for that day based on UTC. Any given 
report will contain all items reported on the selected date for a particular [[Asset]] Class. The reports     are 
available in this tab for 30 days. 
 
 
 
To download a Cumulative Slice Report (in CSV format): 
1. Select the desired [[Asset]] class tab. 
2. Select the desired date. 
3. Open or save the zip file. 
   
Report Layouts for the General and Cumulative Slice files are the same across all jurisdictions. However, field 
applicability may vary by jurisdiction. Please note per regulatory guidelines, transactions reportable to more than 
one Canadian province/territory will appear multiple times in slice reports. Reported fields and report layout are 
listed in Appendix A of this User Guide.   
 
TICKER TAB 
 
The Ticker tab organizes successfully submitted transactions according to [[Asset]] class. Users must click on the 
respective [[Asset]] class tab to see the PPD data related to each [[Asset]] class.  
 
The Ticker tab contains the latest 100 transactions with a scroll bar at the bottom of the screen. It contains the 
same fields found in the Slice Report layouts.  


---

## Page 7

 
 
 
 


---

## Page 8

SEARCH TAB 
 
The Search tab routes the user to the PPD search tool. This tool allows users to set certain transaction terms 
as search criteria for successfully submitted PPD transactions from Pre Rewrite Phase 2 and Post Rewrite 
Phase 2.  
 
Pre Rewrite Phase 2 contains successfully submitted transactions published on or before January 26, 2024.  The 
search range is six months.  Post Rewrite Phase 2 contains transactions successfully submitted on or after 
January 27, 2024.  The search is six months.  
 
PPD data is available for one year from publication. Output of this module is placed in the Report Center for the 
user to retrieve, as described later in this document.  
 
SEARCH: PRE REWRITE PHASE 2 
 
 
SEARCH: POST REWRITE PHASE 2 
 
 
To run a search: 
1. Select the relevant tab. 
2. Select the applicable Jurisdiction from the drop down. 
3. Select the [[Asset]] Class drop down. 
 
If Web Page is selected, the search results appear on the bottom portion of the page. 
 
Retrieving the Output 
 
Users can select “CSV” and use the “search” button, which will provide a CSV download of the results. 
Additionally, users can save the output to the “My Searches” tab by clicking on “Save My Search”  
The report will be saved into the “My Searches” section of the Report Center tab.


---

## Page 9

 
 
REPORT CENTER 
 
The purpose of the Report Center is to provide users with access to reports they have run in the Search 
Tab. Report delivery is regulated by “cookies” to ensure that only the user that runs the Search can 
access the output in the Report Center. It consists of two tabs: “My Searches” and “My Scheduled 
Searches”. 
 
 
 
My Searches 
 
This tab displays up to a total of five completed searches across all jurisdictions. (Refer to the Search 
tab section below on how to execute a search). If there are five searches shown, u sers will have to 
delete a saved search prior to conducting a new search query. 
 
 
To run a saved search: 
1. Select “My Searches” tab 
2. Click hyperlink 
 
To delete a saved search: 
1. Click on the “Delete” action 
 
My Scheduled Searches 
 
This tab displays the searches that are pending to be completed, by jurisdiction. 
 


---

## Page 10

Error! No text of specified style in document. 
 
REPORT CENTER 10 
 
 
 
 
 
 
 
 
 


---

## Page 11

Error! No text of specified style in document. 
 
INFO CENTER 11 
 
INFO CENTER 
 
The Info Center posts useful information to the user community such as system downtime or 
availability, scheduled maintenance, or release information. 
 
 
 
 
 


---

## Page 12

Error! No text of specified style in document. 
 
APPENDIX A: SLICE FILE FIELDS AND LAYOUT 12 
 
APPENDIX A: SLICE FILE FIELDS AND LAYOUT 
There will be three additional fields for the slice files as part of the Phase 2 implementation which have been 
added to the end of the slice files. All changes from the December 2022 Re-Write format to January 2024 Re-
Write Phase 2 implementation are highlighted below.  
Change:  Slice File Field Names 
  Dissemination Identifier 
  Original Dissemination Identifier 
 Action type 
 Event type 
  Event timestamp 
 Amendment indicator 
 [[Asset]] Class 
 Product name 
  Cleared 
 Mandatory clearing indicator 
  Execution Timestamp 
 Effective Date 
 Expiration Date 
 Maturity date of the underlier 
 Non-standardized term indicator 
 Platform identifier 
 Prime brokerage transaction indicator 
 Block trade election indicator 
 Large notional off-facility swap election indicator 
 Notional amount-Leg 1 
 Notional amount-Leg 2 
 Notional currency-Leg 1 
 Notional currency-Leg 2 
 Notional quantity-Leg 1 
 Notional quantity-Leg 2 
 Total notional quantity-Leg 1 
 Total notional quantity-Leg 2 
 Quantity frequency multiplier-Leg 1 
 Quantity frequency multiplier-Leg 2 
 Quantity unit of measure-Leg 1 
 Quantity unit of measure-Leg 2 
 Quantity frequency-Leg 1 
 Quantity frequency-Leg 2 
 Notional amount in effect on associated effective date-Leg 1 
 Notional amount in effect on associated effective date-Leg 2 
 Effective date of the notional amount-Leg 1 
 Effective date of the notional amount-Leg 2 
 End date of the notional amount-Leg 1 
 End date of the notional amount-Leg 2 
Updated field name Call amount-Leg 1 
Removed Call amount-Leg 2 

---

## Page 13

Error! No text of specified style in document. 
 
APPENDIX A: SLICE FILE FIELDS AND LAYOUT 13 
 
Change:  Slice File Field Names 
Updated field name Call currency-Leg 1 
Removed Call currency-Leg 2 
Updated field name Put amount-Leg 1 
Removed Put amount-Leg 2 
Updated field name Put currency-Leg 1 
Removed Put currency-Leg 2 
  Exchange rate 
  Exchange rate basis 
 First exercise date 
 Fixed rate-Leg 1 
 Fixed rate-Leg 2 
  [[Option]] [[Premium]] Amount 
  [[Option]] [[Premium]] Currency 
 Price 
 Price unit of measure 
 Spread-Leg 1 
 Spread-Leg 2 
 Spread currency-Leg 1 
 Spread currency-Leg 2 
 Strike Price 
 Strike price currency/currency pair 
 Post-priced swap indicator 
 Price currency 
 Price notation 
 Spread notation-Leg 1 
 Spread notation-Leg 2 
 Strike price notation 
 Fixed rate day count convention-leg 1 
 Fixed rate day count convention-leg 2 
 Floating rate day count convention-leg 1 
 Floating rate day count convention-leg 2 
 Floating rate reset frequency period-leg 1 
 Floating rate reset frequency period-leg 2 
 Floating rate reset frequency period multiplier-leg 1 
 Floating rate reset frequency period multiplier-leg 2 
 Other payment amount 
 Fixed rate payment frequency period-Leg 1 
 Floating rate payment frequency period-Leg 1 
 Fixed rate payment frequency period-Leg 2 
 Floating rate payment frequency period-Leg 2 
 Fixed rate payment frequency period multiplier-Leg 1 
 Floating rate payment frequency period multiplier-Leg 1 
 Fixed rate payment frequency period multiplier-Leg 2 
 Floating rate payment frequency period multiplier-Leg 2 
 Other payment type 
 Other payment currency 
 [[settlement]] currency-Leg 1 

---

## Page 14

Error! No text of specified style in document. 
 
APPENDIX A: SLICE FILE FIELDS AND LAYOUT 14 
 
Change:  Slice File Field Names 
 [[settlement]] currency-Leg 2 
Updated field name [[settlement]] location Leg 1 
Removed [[settlement]] location Leg 2 
 Collateralisation category 
 Custom basket indicator 
 Index factor 
 Underlier [[ID]]-Leg 1 
 Underlier [[ID]]-Leg 2 
 Underlier [[ID]] source-Leg 1 
 Underlying [[Asset]] Name 
 Underlying [[Asset]] subtype or underlying contract subtype-Leg 1 
 Underlying [[Asset]] subtype or underlying contract subtype-Leg 2 
 Embedded [[Option]] type 
 [[Option]] Type 
 [[Option]] Style 
 Package indicator 
 Package transaction price 
 Package transaction price currency 
 Package transaction price notation 
 Package transaction spread 
 Package transaction spread currency 
 Package transaction spread notation 
 Physical delivery location-Leg 1 
 Delivery Type 
New Unique Product Identifier  
New UPI FISN  
New UPI Underlier Name  
 

---

## Page 15

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]] and [[DTCC]] (Stylized) are registered and unregistered trademarks of The 
Depository Trust & Clearing Corporation. The services described herein are provided under the “[[DTCC]]” brand name by 
certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  
Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in 
which such entity operates. Please see www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they 
offer. 
Doc Date:  
Publication Code:  
Service:  
Title: 
For More Information 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 