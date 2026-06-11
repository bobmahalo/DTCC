---
title: "1042-S Classifications Tax Event Announcements User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gtx109_1042s_classifications_tax_event_announcements_ug_20220630.pdf"
pages: 17
size: "651.6 KB"
category: "Tax_Legal"
ingested_on: "2026-06-05"
---

# 1042-S Classifications Tax Event Announcements User Guide

**Original File:** [gtx109_1042s_classifications_tax_event_announcements_ug_20220630.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gtx109_1042s_classifications_tax_event_announcements_ug_20220630.pdf)  
**Category:** Tax_Legal  
**Total Pages:** 17  
**File Size:** 651.6 KB  

---

## Page 1

 
 
 
GLOBAL TAX SERVICES 
1042-S CLASSIFICATIONS TAX EVENT ANNOUNCEMENTS USER GUIDE 
VERSION 1.0 
JUNE 30, 2022 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
Doc Date: June 30, 2022 
Publication Code: GTX109 
Service: Global Tax Services 
Title: 1042-S Classifications Tax Event Announcements User Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 4 
Quick FAQs ........................................................................................................................................................... 5 
MyDTCC ([[DTCC]] Portal) ........................................................................................................................................ 6 
Searching for 1042-S Classifications Tax Event Announcement ....................................................................... 7 
Payable Date Search ........................................................................................................................................ 8 
Special Searches .............................................................................................................................................. 9 
Search Results ................................................................................................................................................ 11 
CA Web 1042-S Classifications Tax Event Announcement ........................................................................... 12 
Event-Level Information .................................................................................................................................... 12 
CA Link ................................................................................................................................................................ 14 
ISO 20022 Messaging ........................................................................................................................................ 15 
Event Identification ........................................................................................................................................... 15 
Relevant ISO 20022 Messages ........................................................................................................................ 15 
Additional Resources ........................................................................................................................................ 16 
[[DTCC]] Website .................................................................................................................................................. 16 
 

---

## Page 4

1042-S Classifications Tax Event Announcements User Guide 
Overview 4 
OVERVIEW 
[[DTCC]]’s 1042-S Classification Tax Event Announcements provide classification information on distributions that 
have multiple components for IRS Form 1042-S tax withholding and reporting purposes. [[DTC]] generally 
sources the information for 1042-S Classification Announcements directly from issuers. [[DTC]]’s 1042-S 
Classifications Tax Event Announcements are available in Corporation Actions Web (CA Web) and via ISO 
20022 messaging. 
This guide provides a brief explanation of 1042-S Classifications Tax Event Announcement and how to search 
for the announcements in CA Web. 
The topics discussed in this guide include: 
• Quick FAQs 
• MyDTCC Portal 
• CA Web / 1042-S Classifications Tax Event Announcement 
• 1042-S Classifications Tax Event Announcement Event Level Information 
• ISO 20022 Messaging 
  

---

## Page 5

1042-S Classifications Tax Event Announcements User Guide 
Quick FAQs 5 
QUICK FAQS 
1. How [[DO]] I search for 1042-S Classifications Tax Event Announcements?  
• Using the CA Web Event Level Search function. See page 7 for more information. 
2. When does [[DTC]] create 1042-S Classifications Tax Event Announcements?  
• When the distribution is subject to two or more tax classifications for 1042-S reporting purposes. 
3. What cash distributions won’t be utilizing the 1042-S Classifications Tax Event Announcements? 
• Some distributions that are eligible for [[DTC]]’s TaxRelief service, such as certain Canadian cash 
dividends that are subject to both Canadian and US tax withholding.  
• D istributions that only have a single tax classification. These announcements will appear as they [[DO]] 
today.  
4. How [[DO]] [[DTC]] participants know the primary cash distribution is subject to multiple tax classifications and 
that there will be a linked 1042-S Classifications Tax Event Announcement? 
• The primary cash distribution will be classified with 1042-S Income Code 099 to indicate multiple tax 
classifications.  
5. How will I know what primary cash distribution the 1042-S Classification Tax Event announcement is 
related to?  
• In each 1042-S Classifications Tax Event Announcement there is a Related Events tab with CA 
Links. The CA Links display the primary cash distribution’s Corporate Action Identifier (CA [[ID]]). See 
page 14 for more information.  
6. Why is there no 1042-S IRS Income Code in the payout?  
• Generally, this indicates the income is not subject to a reportable 1042-S Income Code under the 
1042-S Instructions.  
7. What are the ISO 20022 specifications for 1042-S Classification Tax Event Announcements?  
• Event Type: OTHR  
• Sub Event Type: RCLA  
• TNDP Indicator: US04 

---

## Page 6

1042-S Classifications Tax Event Announcements User Guide 
MyDTCC ([[DTCC]] Portal) 6 
MYDTCC ([[DTCC]] PORTAL) 
MyDTCC, the portal home page for [[DTCC]], lists various systems to which participants can request access. For 
the purposes of this guide, CA Web will be the primary resource. You can launch CA Web from MyDTCC. 
 
Figure 1: MyDTCC – CA Web 
 
  


---

## Page 7

1042-S Classifications Tax Event Announcements User Guide 
MyDTCC ([[DTCC]] Portal) 7 
Corporate Actions Web (CA Web) allows you to view and work with corporate action event information in a 
variety of methods including allocations and the number of new announcements created daily. 
This section explains how to search for 1042-S Classifications Tax Event Announcement. 
Searching for 1042-S Classifications Tax Event Announcement 
1. Select Announcements > Event Search from the CA Web Main (top) Menu bar. 
 
Figure 2: Event Search 
 
  


---

## Page 8

1042-S Classifications Tax Event Announcements User Guide 
MyDTCC ([[DTCC]] Portal) 8 
2. The Event Search page opens. Click the Advanced Search tab. 
 
Figure 3: Advanced Search 
This walkthrough continues in the Payable Date Search section below this figure. 
Payable Date Search 
For 1042-S Classifications Tax Event Announcements, Tax Product Management recommends searching 
based on Date Criteria. Generally, most users are looking for events paid within a date range.  
3. Under Event Group, check Distributions. 
 
Figure 4: Payable Date Search 
4. Under Event/Sub Type, select Tax Event and, if applicable, the specific event type. Here we’ve selected 
1042-S Classifications. 


---

## Page 9

1042-S Classifications Tax Event Announcements User Guide 
MyDTCC ([[DTCC]] Portal) 9 
5. Select Declared Payable Date from the Date Criteria (Select a date range) dropdown options. 
 
Figure 5: Declared Payable Date 
6. Use the calendar icon that appears next to choose a date upon which to base your search. For example, 
01/01/XXXX or 03/31/XXXX. 
7. Enter “+” days forward or “-“ days prior to the selected date to create your search range. 90 days is the 
maximum number you may enter before or after your selected date. 
8. After entering these parameters, click Search. 
 
Figure 6: Declared Payable Date Search 
To continue this walkthrough and see results based on a Payable Date search, see page 11. To learn about 
Special Searches, continue reading below. 
Special Searches 
Special Searches are used for specific scenarios such as announcement edits or latest updates. The following 
walkthrough demonstrates how to perform such a search. After following “Searching for 1042-S Classifications” 
steps 1 – 4 (above), skip to step 5 (below).  
5. S elect one of the following from the System Date Criteria (Select a date range) dropdown options (these 
are the most popular stystem date criteria used for Announcement searches): 


---

## Page 10

1042-S Classifications Tax Event Announcements User Guide 
MyDTCC ([[DTCC]] Portal) 10 
• Create Date and Time: Displays announcements that were initially created within the specified 
timeframe. 
• Key Data Updated Date and Time: Displays announcements that had one or more of key data fields 
updated within the specified timeframe. Some key data fields are Record Date, Payable Date, and 
Cash Rate. 
• Updated Date and Time: Displays announcements that had any of the fields updated within the 
specified timeframe: for example, Comments, Ex-Date, Instruction Cutoff days, etc.  
6. Use the calendar icon that appears next to choose a date upon which to base your search. For example, 
01/01/XXXX or 03/31/XXXX. 
7. Enter “+” days forward or “-“ days prior to the selected date to create your search range. 90 days is the 
maximum number you may enter before or after your selected date. 
8. After entering these parameters, click Search. 
 
Figure 7: Special Search 
 
 


---

## Page 11

1042-S Classifications Tax Event Announcements User Guide 
MyDTCC ([[DTCC]] Portal) 11 
Search Results 
After locating the results, the screen displays all CA Web events located in the data range determined by your 
search criteria. The announcements search results can be filtered to show all events or only events in which 
you hold a position. By [[default]], the screen displays all available columns. These can be narrowed down to 
what you deem relevant by clicking the Customize Result Columns icon. 
 
Figure 8: Event Search Results 


---

## Page 12

1042-S Classifications Tax Event Announcements User Guide 
CA Web 1042-S Classifications Tax Event Announcement 12 
CA WEB 1042-S CLASSIFICATIONS TAX EVENT 
ANNOUNCEMENT 
Each CA Web event contains payment, [[Entitlement]], adjustments, and other related information about this 
single event. This guide presents examples from one 1042-S Classifications Tax Event announcement. 
Event-Level Information 
Each event has a unique corporation action identifier under the CA [[ID]] column. This example references CA [[ID]] 
534046699. 
 
Figure 9: CA Web Event Level Details 
• Event Type - Tax Event: Tax Event announcements include information-only announcements 
regarding taxable events that may give rise to information and/or withholding [[obligations]] which occur 
even in the absence of an actual distribution of [[Dividend]] and interest payment or amounts to be 
reported in the 1042-S. 
• Sub Event Type: 1042-S Classifications. 
• Declared Payable Date: The date will reflect the primary cash distribution payable date. 
• Record Date: The record date will reflect the primary cash distribution record date. 
The Options/Payouts section is expanded on the next page. 
  


---

## Page 13

1042-S Classifications Tax Event Announcements User Guide 
CA Web 1042-S Classifications Tax Event Announcement 13 
Options/Payouts 
This section will list at least two or more payouts as per the source information, such as the [[issuer]] or the 
offering document. Payout 1 in Figure 10 (below) is visible while Payout 2 would appear further down the 
screen. Each payout will be either be classified with a 1042-S IRS Income Code or no 1042-S IRS Income 
Code. 
• [[DTC]] Cash Rate: This amount that is attributed to the associated 1042-S IRS Income code. 
• 1042-S Income Code: For 1042-S Classifications, the payout will be classified based on the IRS 
1042-S IRS Income Code table. The 1042-S Income Code can include 01: “Interest paid by U.S. 
obligors – general”, 06: “Dividends paid by U.S. corporations – general.”, 27: “Publicly traded 
partnership distributions subject to IRC section 1446” and other codes based on the income 
descriptions provided by the [[issuer]].  
Figure 10: Options/Payouts 

---

## Page 14

1042-S Classifications Tax Event Announcements User Guide 
CA Link 14 
CA LINK  
In each CA Web event, if there is another corporate action that has a connection with the current event, then a 
CA Web Corporate Action Identifier (CA [[ID]]) link will appear on the Related Events tab. The CA Links section 
displays the corresponding CA [[ID]](s) that may need the [[participant]]’s attention. Only primary cash distributions 
with multiple tax classifications will have 1042-S Classifications (which are linked to the primary cash 
distribution).  
In the example below, the 1042-S Classification links to a primary cash distribution that has multiple tax 
classifications. Under CA Links, the following information will be provided:  
• CA [[ID]] – Corporate Action Identifier. 
• Link Type – Corresponding Event. 
• [[CUSIP]] – [[CUSIP]] from the attributable cash distribution.  
• [[issuer]] Description – Security Description. 
• Record Date – Record Date from the attributable cash distribution.  
• Payable Date – Payable Date from the attributable cash distribution.  
• [[DTC]] Cash Rate – Cash Rate from the attributable cash distribution. 
 
Figure 11: CA Link - 1042-S Classifications 

---

## Page 15

1042-S Classifications Tax Event Announcements User Guide 
ISO 20022 Messaging 15 
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
• Corporate Action Notification (CANO). This message contains all the information known about a 
corporate action: event details, event status, security description and details, relevant dates, and 
more. 
• Corporate Action Cancellation (CACN). This message is a notification of a canceled corporate 
action event. 
• Corporate Action Movement Confirmation (CACO). This message indicates that a payment has 
been made because of an earlier corporate action. 
 

---

## Page 16

1042-S Classifications Tax Event Announcements User Guide 
Additional Resources 16 
ADDITIONAL RESOURCES 
[[DTCC]] Website 
The [[DTCC]] website ([[DTCC]].com) is the primary repository for general information and documentation concerning 
the latest Corporate Actions functionality. Clients can review published documentation, download user guides, 
and use the website to stay up to date on new developments.  
See the ISO 20022 Messaging Specifications page on [[DTCC]].com for the latest messaging specifications by 
category.  
 
 

---

## Page 17

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 