---
title: "871(m) Tax Event Announcements User Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gtx108_871m_tax_event_announcements_ug_20220428.pdf"
pages: 16
size: "588.2 KB"
category: "Tax_Legal"
ingested_on: "2026-06-05"
---

# 871(m) Tax Event Announcements User Guide

**Original File:** [gtx108_871m_tax_event_announcements_ug_20220428.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gtx108_871m_tax_event_announcements_ug_20220428.pdf)  
**Category:** Tax_Legal  
**Total Pages:** 16  
**File Size:** 588.2 KB  

---

## Page 1

 
 
 
 
GLOBAL TAX SERVICES 
871(M) TAX EVENT ANNOUNCEMENTS USER GUIDE 
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
Publication Code: GTX108 
Service: Global Tax Services 
Title: 871(m) Tax Event Announcements User Guide 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Summary ............................................................................................................................................................... 4 
Quick FAQs ........................................................................................................................................................... 5 
MyDTCC ([[DTCC]] Portal) ........................................................................................................................................ 6 
Corporate Actions Web ....................................................................................................................................... 7 
How to search for 871(m) Tax Event Announcements? ..................................................................................... 7 
Payable Date Searches..................................................................................................................................... 9 
Special Searches .............................................................................................................................................. 9 
Search Results ..................................................................................................................................................10 
CA Web 871(m) Tax Event Announcements ....................................................................................................11 
Event-Level Information ..................................................................................................................................11 
CA Links ..........................................................................................................................................................13 
871(m) CA Links ............................................................................................................................................13 
ISO 20022 Messaging ........................................................................................................................................ 14 
Event Identification............................................................................................................................................14 
Relevant ISO 20022 Messages ........................................................................................................................14 
[[DTCC]] Website ..................................................................................................................................................... 15 
 

---

## Page 4

871(m) Tax Event Announcements User Guide 
Summary 4 
SUMMARY 
871(m) Tax Event Announcements are available in [[The Corporation]] Actions Web (CA Web). 871(m) Tax Event 
announcements simplifies compliance with Section 871(m) of the Internal Revenue Code by sourcing [[Dividend]] 
equivalent amounts directly from issuers and providing the information in the same manner as other corporate 
action information which allows these events to flow seamlessly into client’s tax processing engines. This guide 
provides a brief explanation of the necessary capabilities to [[Locate]] 871(m) Tax Event Announcements and 
positions held in each security.  
For [[DTC]] eligible [[securities]] that are in scope for 871(m), issuers are required to provide the timing and [[Dividend]] 
equivalent amounts to [[DTC]] as they occur throughout the life of their [[securities]].  
The topics discussed in this guide include: 
• Quick FAQs 
• MyDTCC Portal 
• CA Web / 871(m) Tax Event Announcements 
• 871(m) Tax Event Announcement Event Level information 
• ISO 20022 Messaging 
 
  

---

## Page 5

871(m) Tax Event Announcements User Guide 
Quick FAQs 5 
QUICK FAQS 
1. When does [[DTC]] announce 871(m) Tax Event Announcements?  
o [[DTC]] eligible [[securities]] that are in scope for 871(m) are attested by the [[issuer]] on the onset of 
eligibility. Afterwards, issuers are required to provide [[DTC]] with [[Dividend]] equivalent amounts as 
they occur.  
2. How can I search for 871(m) Tax Event Announcements?  
o You can search for 871(m) Tax Event announcements in CA Web Event Level search. Please 
see page 7 for more information.  
3. Does [[DTC]]’s 871(m) Tax Event Announcements provide the Timing Date?  
o Yes, [[DTC]] provides the date as confirmed from the [[issuer]] into the CA Web field Timing of the 
[[Dividend]] Equivalent Amount.  
4. Does [[DTC]]’s 871(m) Tax Event Announcements provide the underlying security that triggered the DEA?  
o Yes, when the [[issuer]] provides the underlying security that triggered the DEA, in the 871(m) Tax 
Event Announcement there will be a section called Related Events. Under this section there will 
be a CA Links section with information about the security that triggered the DEA.  
5. What field provides the 871(m) [[Dividend]] equivalent amount in CA Web?  
o The 871(m) [[Dividend]] Equivalent amount is stated in each 871(m) Tax Event Announcement’s  
Cash Rate  
6. What are the ISO 20022 specifications for 871(m) Tax Event Announcements?  
o Event Type: TNDP 
o Sub Event Type: M871 
o TNDP Indicator: US02 
7. What are the CA Web specifications?  
o Event Type: Tax Event 
o Sub Event Type: 871(m) [[Dividend]] Equivalent Amount 
 

---

## Page 6

871(m) Tax Event Announcements User Guide 
MyDTCC ([[DTCC]] Portal) 6 
MYDTCC ([[DTCC]] PORTAL) 
MyDTCC, the portal home page for [[DTCC]], lists various systems to which participants can request access. For 
the purposes of this guide, CA Web will be the primary resource.   
 
 
  


---

## Page 7

871(m) Tax Event Announcements User Guide 
Corporate Actions Web 7 
CORPORATE ACTIONS WEB 
Corporate Actions Web (CA Web) allows you to view and work with corporate action event information in a 
variety of ways including allocations and the number of announcements created daily.  
This section explains how to search for Tax Event and General Information announcement data. 
From the [[DTCC]] Portal, please click CA Web to enter the system. 
How to search for 871(m) Tax Event Announcements?  
Please start by selecting Announcements > Event Search from the main menu bar. 
 
 
  


---

## Page 8

871(m) Tax Event Announcements User Guide 
Corporate Actions Web 8 
Click the Advanced Search tab.  
 
 


---

## Page 9

871(m) Tax Event Announcements User Guide 
Corporate Actions Web 9 
Payable Date Searches 
For 871(m) Tax Event Announcements, Tax Product Management recommends searching by the payable 
date. This allows searches for four quarters of the calendar year.  
1. Under Event Group, check “Distributions.” 
2. Under Event/Sub Type, select Tax Event and, if applicable, the specific event type: 
• 871(m) [[Dividend]] Equivalent Amount 
3. In the Date area, select Date Criteria. 
• Declared Payable Date: Choose a date such as 01/01/XXXX or 03/31/XXXX.  
• Enter “+” days forward or “-“ days prior to the selected date. 90 days is the maximum time period 
before or after your selected date. 
4. After entering these parameters, click Search. 
 
Special Searches 
The [[Option]] below is used for specific scenarios such as announcement edits or latest updates. If you are 
looking for these type of search features, please continue below:  
In the Date area, select System Date Criteria. 
The following are the most popular system date criteria used for Announcement searches:  
• Create Date and Time: Displays announcements that were initially created within the specified 
timeframe. 
• Key Data Updated Date and Time: Displays announcements that had one or more of key data fields 
updated within the specified timeframe. Some key data fields are Record Date, Payable Date, and 
Cash Rate. 
• Updated Date and Time: Displays announcements that had any of the fields updated within the 
specified timeframe: for example, Comments, Ex-Date, Instruction Cutoff days, etc.  
• Enter an appropiate date and duration of interest: “+” days forward or “-“ days prior to the selected 
date. 90 days is the maximum time period before or after your selected date.  
 
After entering these parameters, click Search. 
  

---

## Page 10

871(m) Tax Event Announcements User Guide 
Corporate Actions Web 10 
Search Results 
After locating the results, the screen displays all CA Web events located in the data range determined by your 
search criteria. The announcements search results can be filtered to show all events or only events in which 
you hold a position. By [[default]], the screen displays all available columns. These can be narrowed down to 
what you deem relevant by clicking the Customize Result Columns icon. 
 
  


---

## Page 11

871(m) Tax Event Announcements User Guide 
Corporate Actions Web 11 
CA Web 871(m) Tax Event Announcements 
Each CA Web event contains payment, [[Entitlement]], adjustments, and other related information about this 
single event. This guide presents examples from one Tax Event Announcement. 
Event-Level Information 
Each event has a unique corporation action identifier under the CA [[ID]] column. This example references CA [[ID]] 
120772905. 
 
Event Type: Tax Event 
This event type distinguishes various amounts of tax information from other announcements at [[DTC]]. Tax Event 
announcements include information-only announcements regarding taxable events that may give rise to 
information and/or withholding [[obligations]] which occur even in the absence of an actual distribution of [[Dividend]]  
and interest payment or amounts to be reported in the 1042-S.  
Sub Event Type:  
871(m) [[Dividend]] Equivalent Amount 
Timing of the [[Dividend]] Equivalent Amount 
This field is used for the timing of [[Dividend]] equivalents under 1.871-15 of Treasury regulations. This field only 
appears for 871(m) [[Dividend]] Equivalent Amount sub event types. 
Record Date 
The Record date field for 871(m) DEA is set to the underlying security record date. 
Declared Payable Date 
The payable date of the underlying security for sub event type 871(m) [[Dividend]] Equivalent Amount. 


---

## Page 12

871(m) Tax Event Announcements User Guide 
Corporate Actions Web 12 
 [[DTC]] Cash Rate 
This field is used for the 871(m) [[Dividend]] Equivalent Amount rate as provided by the [[issuer]] of the section 
871(m) transaction. 
 
Linked [[CUSIP]] [[ID]]* 
This field is used to display a linked correlation to an underlying [[CUSIP]]. For 871(m) Tax Event 
Announcements, this field displays the underlying [[CUSIP]] that triggered the DEA.  
*In this instance the [[issuer]] did not provide [[DTCC]] with the underlying [[CUSIP]] for these 871(m) events and 
therefore this field does not appear in the screenshot above. 
1042-S Income Code 
For [[Dividend]] equivalent amounts under IRC 871(m), the 1042-S Income Code will generally be set to 40: 
“Other [[Dividend]] equivalents under IRC section 871(m) (formerly 871(l)).” 
 
 
 
 
  


---

## Page 13

871(m) Tax Event Announcements User Guide 
Corporate Actions Web 13 
CA Links 
In each CA Web event, if there is another corporate action that has a connection with the current event, then a 
CA Web Corporate Action Identifier (CA [[ID]]) link will appear under the “Related Events” tab. Under this section, 
“CA Links” will display the corresponding CA [[ID]](s) that may need the [[participant]]’s attention.  
871(m) CA Links 
When an [[issuer]] accompanies their [[Dividend]] equivalent amount information wi th the [[CUSIP]] of the underlying 
common [[Stock]] that triggered the DEA, a CA Link will appear to provide clients with the following additional 
information:  
• CA [[ID]] – Corporate Action Identifier 
• Link Type – Underlying Security 
• [[CUSIP]] – Underlying [[CUSIP]] that triggered the DEA as provided by the [[issuer]].  
• Event Type – Cash [[Dividend]]  
• [[issuer]] Description – Security Description 
• Ex-Date – Ex-[[Dividend]] Date for the underlying cash [[Dividend]]. 
• Record Date – Record Date for the underlying cash [[Dividend]].  
• Payable Date – Payable Date for the underlying cash [[Dividend]].  
• [[DTC]] Cash Rate – Cash Rate for the underlying cash [[Dividend]].  
 
 

---

## Page 14

871(m) Tax Event Announcements User Guide 
ISO 20022 Messaging 14 
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
• Corporate Action Notification (CANO) – This message contains all of the information known about 
a corporate action: event details, event status, security description and details, relevant dates, and 
more. 
• Corporate Action Cancellation (CACN) – This message is a notification of a canceled corporate 
action event. 
• Corporate Action Movement Confirmation (CACO) – This message indicates that a payment has 
been made as a result of an earlier corporate action. 

---

## Page 15

871(m) Tax Event Announcements User Guide 
[[DTCC]] Website 15 
[[DTCC]] WEBSITE 
The [[DTCC]] website ([[DTCC]].com) is the primary repository for general information and documentation concerning 
the latest Corporate Actions functionality. Clients can review the published documentation, download user 
guides, and use the website to stay up to date on new developments.  
See http://www.[[DTCC]].com/[[settlement]]-and-[[Asset]]-services/corporate-actions-processing/iso-20022-messaging-
specifications for the latest messaging specifications by category.  
 
 

---

## Page 16

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 