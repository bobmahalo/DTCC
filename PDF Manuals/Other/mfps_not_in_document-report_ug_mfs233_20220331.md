---
title: "MFPS II: Not in Document Report"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps_not_in_document-report_ug_mfs233_20220331.pdf"
pages: 14
size: "943.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# MFPS II: Not in Document Report

**Original File:** [mfps_not_in_document-report_ug_mfs233_20220331.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mfps_not_in_document-report_ug_mfs233_20220331.pdf)  
**Category:** Other  
**Total Pages:** 14  
**File Size:** 943.6 KB  

---

## Page 1

 
 
 
MUTUAL FUND PROFILE SECURITY II  
NOT IN DOCUMENT REPORT 
MARCH  2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: March 31, 2022 
Publication Code: MFS233 
Service: [[Mutual Funds]] Profile Service II Profile Security 
Title: Not in Document Report 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction .......................................................................................................................................................... 4 
Overview ............................................................................................................................................................. 4 
Generate a Not in Document (NID) Report ........................................................................................................ 5 
Review Not in Document (NID) Report ............................................................................................................... 7 
Review Not in Document (NID) Report – Social Codes Only ........................................................................... 8 
Review and Acknowledge NID Data Point Values ............................................................................................ 9 
Update a Data Point .......................................................................................................................................... 9 
Acknowledge Data Point(s) ............................................................................................................................. 10 
Modify the Review Period .................................................................................................................................. 12 
Daily Variance Summary Email ......................................................................................................................... 13 
 

---

## Page 4

Not In Document Report 
Introduction 4 
INTRODUCTION 
Overview 
Recent enhancements were implemented to the Mutual Fund Profile Service II – Profile Security database 
(MFPS II- Profile Security).  These enhancements provide security improvements, greater data entry 
efficiencies and increased reporting intelligence to support the data review process. This document outlines 
how to generate a Not in Document (NID) Report, review and acknowledge the NID data point and modify 
review cycles 
NID data points cannot be extracted from a legal filing and cannot be validated against Profile Security, 
therefore, Fund clients are responsible to manually review and verify the data point values for accuracy.  To 
assist Fund clients in the review process, the NID report has been updated to include a periodic process which 
now requires Fund clients to periodically review and acknowledge the data point value.  Since the report is 
generated at the Security Issue [[ID]] level for every data point attribute classified as NID, bulk review functionality 
has been incorporated into the report allowing you to sort and review these data points are various levels.   

---

## Page 5

Not In Document Report 
Generate a Not in Document (NID) Report 5 
GENERATE A NOT IN DOCUMENT (NID) REPORT 
From Profile Security, expand the Report section and select Not in Document Report from the list of reports. 
 
 
 
1. From the Not in Document Report page, select your Management Company in the Select a Company 
field, if you have more than one Management Company account. 
2. You can generate the report with the following data point criteria: 
a. Extractable 
b. Non-extractable (Excluding Social Codes) 
c. All (excluding Social Codes), which is the [[default]] selection, or 
d. Only Social Codes 
3. Select your data point and click run report. 
 
Data Point Criteria Definition 
Extractable Select Extractable to run a report for data points that have become silent, 
meaning they are typically disclosed in a filing document, but have not 
been identified through Profile Security. 


---

## Page 6

Not In Document Report 
Generate a Not in Document (NID) Report 6 
Data Point Criteria Definition 
Non-extractable (Excluding Social 
Codes) 
Select Non-extractable (excluding Social Codes) to run a report for the pre-
defined data points that are never disclosed in a prospectus. 
All (excluding Social Codes), which 
is the [[default]] selection 
Select All (excluding Social Codes) to run a report for both extractable and 
non-extractable data points, excluding Social Codes. 
Only Social Codes Select Only Social Codes to run a report specifically for social codes. 
Social codes are also pre-defined data points that are never disclosed in a 
prospectus. 
 
Note: 
The report you generate will include all NID data points, regardless of when they became NID so there is no filter selection 
for start and end dates. 

---

## Page 7

Not In Document Report 
Review Not in Document (NID) Report 7 
REVIEW NOT IN DOCUMENT (NID) REPORT 
 
Each report displays the following sortable columns: 
• Fund Portfolio - The name of the fund. 
• Share Class - A unique identifier that identifies the share class. 
• Ticker - The Fund-Created, [[NASDAQ]] or other symbol for this fund. 
• Security Issue [[ID]] - [[DTCC]] Identifier for this fund. 
• Data Point- The attribute that is NID. 
• Profile Value The value of the data point attribute. 
• Extractable - Extractable, which indicates whether a data point is considered an extractable data point or a 
pre-determined NID data points 
• Acknowledgement – Values include  
o Yes - if the data point value has been reviewed and acknowledged within its given review period 
o Review Required - if a data point’s review cycle is up or  
o No - for a data point that has just been populated and classified as NID, with its value not yet 
reviewed and acknowledged. 
• Acknowledged By - identifies the most recent user to review and acknowledge the data point value. 
• Acknowledged Date – Date the NID was acknowledged. 
• NID Effective Date – Date that the data point became NID.  
 
Note: 
You can download a copy of your report in Excel. 


---

## Page 8

Not In Document Report 
Review Not in Document (NID) Report 8 
Review Not in Document (NID) Report – Social Codes Only 
You can use the Not In Document Report to run a report that contains Data Points for Social Codes only.  This 
report returns all data points related to social codes.  You can use the text box in the data point column to 
narrow results by a particular code. 
 
In the Data Point column, enter the term social code followed by the number and then a comma, to limit the 
results.  For example, to review all data points related to Social Code 8, enter Social Code 8,..  The results on 
screen will be limited to your criteria entered.  
 
 


---

## Page 9

Not In Document Report 
Review and Acknowledge NID Data Point Values 9 
REVIEW AND ACKNOWLEDGE NID DATA POINT 
VALUES 
Use the column sort and filter as needed to [[Locate]] the NID data points requiring your attention and review 
them.  While Funds have multiple sort and review methods available to select from, below are some 
recommended methods for reviewing the data:  
• Sort by Data Point attribute, then Profile Value 
• Sort by Share Class, then Data Point attribute followed by Profile Value 
• Sort by Fund Portfolio, then Data Point attribute followed by Profile Value 
 
After reviewing the data points, there are a few actions you can take: 
• Update the value of a data point before acknowledging 
• Acknowledge a data point individually 
• Bulk acknowledge multiple data point values 
Update a Data Point 
If you need to update the value of a data point before acknowledging it, complete the following steps: 
1. After finding the data point, click the Security Issue [[ID]] link to go to the Fund Detail section.  
2. Use the Find a Data Point search field to find the specific data point.  
3. Update the value and then return to the NID Report page.  When you make the update, you have the 
following options: 
a. Schedule Change: Update the value but schedule the change.  The attribute will retain its current 
value until the selected date, when it will change to the new value. 
b. Draft Change:  The attribute will retain its current value indefinitely.  Draft changes can be applied 
manually at any future time. 
c. Save and Apply Now: The attribute value will be updated immediately. 
4. Repeat this process for any additional data points that need to be updated.   
5. Run your report again. 

---

## Page 10

Not In Document Report 
Review and Acknowledge NID Data Point Values 10 
 
Acknowledge Data Point(s) 
If a data point value is valid, you can acknowledge it individually or with other valid data point values.  
To acknowledge a data point: 
1. Select the boxes for the data points you want to acknowledge and click acknowledge selected.  You can 
select one data point or many.  
2. The Acknowledge NID Data Points dialog box pops up. It confirms the number of data points you are 
acknowledging, with a warning that your acknowledgement cannot be undone. 
3. Click Acknowledge to continue with your acknowledgement. 
4. Once your acknowledgements have been processed, a “Success” message appears, indicating the 
number of NID data points that you have acknowledged.   
 
 
 


---

## Page 11

Not In Document Report 
Review and Acknowledge NID Data Point Values 11 
5. Returning to the report, you will notice that the Acknowledgement status is updated to “Yes” for the 
selected data points. The Acknowledged By and Acknowledged Date fields for those selected data 
points are updated with your username and the date. 
 


---

## Page 12

Not In Document Report 
Modify the Review Period 12 
MODIFY THE REVIEW PERIOD 
For each fund, you can modify the review period for the data points. The [[default]] review cycle for Not in 
Document data points is set for 365 days. You can modify the review period to occur between 1 to 365 days. 
To modify the review period,  
1. Go to Settings and select your Management Company 
2. Click Edit 
3. Change the NID Acknowledgement Reset Days choose any value between 1 to 365 days 
4. Make your changes and click Save 
 


---

## Page 13

Not In Document Report 
Daily Variance Summary Email 13 
DAILY VARIANCE SUMMARY EMAIL 
To help facilitate the review of these data points, once the number of review days has passed and the NID data 
point is labeled as “Review Required”, the Daily Variance Summary Email will reflect the number of NIDs data 
points that require review. 
 
 
 
 


---

## Page 14

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 