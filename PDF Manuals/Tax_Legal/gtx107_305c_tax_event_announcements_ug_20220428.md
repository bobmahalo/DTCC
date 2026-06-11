---
title: "305(c) Tax Event Announcements User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gtx107_305c_tax_event_announcements_ug_20220428.pdf"
pages: 18
size: "822.9 KB"
category: "Tax_Legal"
ingested_on: "2026-06-05"
---

# 305(c) Tax Event Announcements User Guide

**Original File:** [gtx107_305c_tax_event_announcements_ug_20220428.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gtx107_305c_tax_event_announcements_ug_20220428.pdf)  
**Category:** Tax_Legal  
**Total Pages:** 18  
**File Size:** 822.9 KB  

---

## Page 1

 
 
 
 
 
GLOBAL TAX SERVICES 
305(C) TAX EVENT ANNOUNCEMENTS USER GUIDE 
VERSION 1.0 
APRIL 28, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: April 28, 2022 
Publication Code: GTX107 
Service: Global Tax Services 
Title: 305(c) Tax Event Announcements User Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Summary ............................................................................................................................................................... 4 
Quick FAQs ........................................................................................................................................................... 5 
MyDTCC ([[DTCC]] Portal) ........................................................................................................................................ 6 
Corporate Actions Web ....................................................................................................................................... 7 
How to search for 305(c) Tax Event Announcements? ...................................................................................... 7 
Payable Date Searches..................................................................................................................................... 9 
Special Searches .............................................................................................................................................. 9 
Search Results ..................................................................................................................................................10 
CA Web 305(c) Tax Event Announcements .....................................................................................................11 
Event-Level Information ..................................................................................................................................11 
LENS .................................................................................................................................................................... 13 
LENS Dashboard ..............................................................................................................................................14 
Results ..............................................................................................................................................................15 
ISO 20022 Messaging ........................................................................................................................................ 16 
Event Identification............................................................................................................................................16 
Relevant ISO 20022 Messages ........................................................................................................................16 
[[DTCC]] Website ..................................................................................................................................................... 17 
 

---

## Page 4

305(c) Tax Event Announcements User Guide 
Summary 4 
SUMMARY 
305(c) Tax Event Announcements are available in [[The Corporation]] Actions Web (CA Web). Section 305(c) of 
the Internal Revenue Code considers that holders of convertible [[securities]] may be deemed to have received a 
[[Dividend]] as a result of a corporate action on the underlying common [[Stock]]. Issuers of convertible [[securities]] are 
required to file IRS Form 8937 if a conversion rate adjustment (CRA) results in a distribution under Section 
305(c). In addition to cost basis adjustments, financial [[Institutions]] may have requirements to withhold tax on 
the deemed distribution and to perform year-end tax reporting for the deemed distribution to holders. 
[[DTC]] creates 305(c) Tax Event Announcements based on issuers’ IRS Form 8937 and stores the forms in our 
Legal Notice System (LENS).   
The topics discussed in this guide include: 
• Quick FAQs 
• MyDTCC Portal 
• CA Web / 305(c) Tax Event Announcements 
• LENS 
• ISO 2022 Messaging 
  

---

## Page 5

305(c) Tax Event Announcements User Guide 
Quick FAQs 5 
QUICK FAQS 
1. What happens when [[DTC]] receives a Conversion Rate Adjustment (CRA) letter from the [[issuer]] or their 
[[transfer agent]]?  
o [[DTC]] will create a conditional 305(c) Tax Event with an indefinite payable date. The payable date will 
be updated when we receive further communication from the [[issuer]] such as  IRS form 8937. If so, the 
payable date will be updated with a final date.  
2. How does [[DTC]] confirm the 305(c) Deemed [[Dividend]] amount? 
o Issuers will provide [[DTC]] an IRS Form 8937 with the necessary details such as the effective date of 
the adjustment and the amount of the 305(c) deemed distribution.  
3. How [[DO]] I search for 305(c) Tax Event Announcements?  
o You can search for 305(c) Tax Event Announcements by using CA Web’s Event Search [[Option]]. 
Please see page 7 for more information.  
4. What happens if [[issuer]] sends out a CRA letter but doesn’t provide a Form 8937 to [[DTC]]? 
o [[DTC]] will attempt multiple inquires for the confirmation from the [[issuer]], if there is n o Form 8937 or the 
[[issuer]] was nonresponsive, the CRA adjustments will be treated as 305(c) Deemed Dividends.  
o [[DTC]] will calculate the amounts as per industry standards and publish an important notice with all the 
events that were manually calculated around end of January of the following calendar year.  
5. Where can I download the IRS Form 8937 that the issuers have provided to [[DTC]]?  
o The IRS Form 8937s are stored in [[DTC]]’s LENS service. Please see page 13 for more information.  
6. Where is the section 305(c) deemed distribution amount located in CA Web?  
o The section 305(c) deemed distribution amount is stated in each 305(c) Tax Event Announcement’s  
Cash Rate field.  
7. What are the ISO 20022 specifications for 305(c) Tax Event Announcement?  
o Event Type: TNDP 
o Sub Event Type: C305 
o TNDP Indicator: US01 
8. What are the CA Web specifications?  
o Event Type: Tax Event 
o Sub Event Type: 305(c) Deemed [[Dividend]] 
 

---

## Page 6

305(c) Tax Event Announcements User Guide 
MyDTCC ([[DTCC]] Portal) 6 
MYDTCC ([[DTCC]] PORTAL) 
MyDTCC, the portal home page for [[DTCC]], lists various systems to which participants can request access. For 
the purposes of this guide, the two systems explained are CA Web and LENS.  
 
 
  


---

## Page 7

305(c) Tax Event Announcements User Guide 
Corporate Actions Web 7 
CORPORATE ACTIONS WEB 
Corporate Actions Web (CA Web) allows you to view and work with corporate action event information in a 
variety of ways including allocations and the number of announcements created daily.  
This section explains how to search for 305(c) Tax Event Announcements. 
From the [[DTCC]] Portal, please click CA Web to enter the system. 
How to search for 305(c) Tax Event Announcements? 
Please start by selecting Announcements > Event Search from the main menu bar. 
 
 
  


---

## Page 8

305(c) Tax Event Announcements User Guide 
Corporate Actions Web 8 
Click the Advanced Search tab. 
 
 


---

## Page 9

305(c) Tax Event Announcements User Guide 
Corporate Actions Web 9 
Payable Date Searches 
For 305(c) Tax Event Announcements, Tax Product Management recommends searching by the payable 
dates. Due to the nature of our [[DTC]]’s communication with the [[issuer]], valid Payable Dates signals the final 
communication with the [[issuer]]. Additionally, it allows searches for four quarters of the calendar year.  
1. Under Event Group, check “Distributions.” 
2. Under Event/Sub Type, select Tax Event and, if applicable, the specific event type: 
o 305(c) Deemed Dividends 
3. In the Date area, select Date Criteria. 
o Declared Payable Date: Choose a date such as 01/01/XXXX or 03/31/XXXX.  
o Enter “+” days forward or “-“ days prior to the selected date. 90 days is the maximum time period 
before or after your selected date. 
4. After entering these parameters, click Search. 
Special Searches 
The [[Option]] below is used for specific scenarios such as announcement edits or latest updates. I f you are 
looking for these type of search features, please continue below:  
In the Date area, select System Date Criteria. 
The following are the most popular system date criteria used for Announcement searches:  
• Create Date and Time: Displays announcements that were initially created within the specified timeframe. 
• Key Data Updated Date and Time: Displays announcements that had one or more of key data fields 
updated within the specified timeframe. Some key data fields are Record Date,  Payable Date, and Cash 
Rate. 
• Updated Date and Time: Displays announcements that had any of the fields updated within the specified 
timeframe: for example, Comments, Ex-Date, Instruction Cutoff days, etc.  
• Enter an appropiate date and duration of interest: “+” days forward or “-“ days prior to the selected date. 
90 days is the maximum time period before or after your selected date. 
 
After entering these parameters, click Search. 
  

---

## Page 10

305(c) Tax Event Announcements User Guide 
Corporate Actions Web 10 
Search Results 
After locating the results, the screen displays all CA Web events located in the data range determined by your 
search criteria. The announcements search results can be filtered to show all events or only events in which 
you hold a position. By [[default]], the screen displays all available columns. These can be narrow ed down to 
what you deem relevant by clicking the Customize Result Columns icon. 
 
  


---

## Page 11

305(c) Tax Event Announcements User Guide 
Corporate Actions Web 11 
CA Web 305(c) Tax Event Announcements 
Each CA Web event contains payment, [[Entitlement]], adjustments, and other related information about this 
single event. This guide presents examples from one Tax Event Announcement. 
Event-Level Information 
Each event has a unique corporation action identifier under the CA [[ID]] column. This example references CA [[ID]] 
129948985. 
 
Event Type: Tax Event 
This event type distinguishes various amounts of tax information from other announcements at [[DTC]]. Tax Event 
announcements include information-only announcements regarding taxable events that may give rise to 
information and/or withholding [[obligations]] which occur even in the absence of an actual distribution of [[Dividend]] 
and interest payment or amounts to be reported in the 1042-S.  
Sub Event Type:  
305(c) Deemed [[Dividend]] 
Record Date 
This field indicates the date used for position capture. The Record Date field for 305(c) Tax E vent 
Announcement is set to the day prior to the Payable Date. 
Declared Payable Date 
This field is used for the date of the deemed distribution. The date of the deemed distribution for sub event type 
305(c) Deemed Dividends. 
 
  


---

## Page 12

305(c) Tax Event Announcements User Guide 
Corporate Actions Web 12 
[[DTC]] Cash Rate 
(5) This field is used for the amount of the 305(c) deemed distribution as generally provided on IRS Form 8937. 
 
1042-S Income Code 
(6) For deemed dividends under IRC 305(c), the 1042-S Income Code will generally be set to 06: “Dividends 
paid by U.S. corporations – general.”   
 
 
 
 
  


---

## Page 13

305(c) Tax Event Announcements User Guide 
LENS 13 
LENS 
LENS offers access to a comprehensive online library of notices concerning [[DTC]] eligible [[securities]] . For the 
purpose of this guide, we will search for IRS tax form 8937s. Please note that if you have never used LENS, 
you should view the [[DTC]] fee schedule for more information about the billing structure.  
From the [[DTCC]] Portal, please click LENS to enter the system. 
 
  


---

## Page 14

305(c) Tax Event Announcements User Guide 
LENS 14 
LENS Dashboard 
The dashboard summarizes on a daily basis the new notices that have been added to the database. We will 
use a search filter to display all Form 8937s in LENS. 
 
1. Under Notice Search, enter the following parameters: 
Select a Search Type: Notice Type/Subtype 
Notice type: LG (Legal) 
Sub-type: Cost Basis 
Search Date: Enter the date range for your search. Pick a start date and select the current business day 
for your end date. 
Note: 
You can search for notices within the past five years. Use mm/dd/yyyy format or select a date using the calendar 
tool. 
2. Click Search.  


---

## Page 15

305(c) Tax Event Announcements User Guide 
LENS 15 
Results 
Please note that one form, 8937, can represent multiple 305(c) deemed dividends. You can proceed to view 
individual notices or download multiple files at the same time. Also, you can filter results based on your criteria 
or export all the results into a spreadsheet.  
Note that there are fees associated with this. Please view [[DTC]]’s fee guide if you are not a subscriber.  
 


---

## Page 16

305(c) Tax Event Announcements User Guide 
ISO 20022 Messaging 16 
ISO 20022 MESSAGING 
ISO 20022 messaging provides the most up-to-date process for receiving real-time data. To get started with 
ISO 20022 messaging for your firm, contact the Corporate Actions Modernization mailbox at 
camodernization@[[DTCC]].com. While testing, clients may submit inquiries and/or comments to this mailbox as 
well. Once your company is active in the production environment, inquiries should be directed to the Customer 
Help Center at 888-382-2721. 
Event Identification  
All events are identified by a single identification number (its CA [[ID]], or “COAF” as it is known in ISO 20022) 
that follows the event through its lifecycle. All subsequent messages and communications relating to this event 
are referenced by this number. 
Relevant ISO 20022 Messages 
The messages that are sent concerning Tax Event announcements include: 
• Corporate Action Notification (CANO) – This message contains all of the information known about a 
corporate action: event details, event status, security description and details, relevant dates, and more.  
• Corporate Action Cancellation (CACN) – This message is a notification of a canceled corporate action 
event. 
• Corporate Action Movement Confirmation (CACO) – This message indicates that a payment has been 
made as a result of an earlier corporate action. 

---

## Page 17

305(c) Tax Event Announcements User Guide 
[[DTCC]] Website 17 
[[DTCC]] WEBSITE 
The [[DTCC]] website ([[DTCC]].com) is the primary repository for general information and documentation concerning 
the latest Corporate Actions functionality. Clients can review the published documentation, download user 
guides, and use the website to stay up to date on new developments. [[DTCC]] 305(c) Tax Event Announcement 
information can be viewed at www.[[DTCC]].com/305c. 
See http://www.[[DTCC]].com/[[settlement]]-and-[[Asset]]-services/corporate-actions-processing/iso-20022-messaging-
specifications for the latest messaging specifications by category.  
 
 

---

## Page 18

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 