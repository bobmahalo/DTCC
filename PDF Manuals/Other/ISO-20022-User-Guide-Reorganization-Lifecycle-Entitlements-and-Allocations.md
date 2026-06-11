---
title: "ISO 20022 Messaging for Reorganizations Entitlements and Allocations"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO-20022-User-Guide-Reorganization-Lifecycle-Entitlements-and-Allocations.pdf"
pages: 135
size: "5671.3 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO 20022 Messaging for Reorganizations Entitlements and Allocations

**Original File:** [ISO-20022-User-Guide-Reorganization-Lifecycle-Entitlements-and-Allocations.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO-20022-User-Guide-Reorganization-Lifecycle-Entitlements-and-Allocations.pdf)  
**Category:** Other  
**Total Pages:** 135  
**File Size:** 5671.3 KB  

---

## Page 1

 
 
 
 
 
 
 
[[DTC]] CORPORATE ACTIONS 
USER GUIDE:  
ISO 20022 MESSAGING FOR REORGANIZATIONS   
ENTITLEMENTS AND ALLOCATIONS 
VERSION 1.3 
MARCH 09, 2021 
 

---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in wh ich such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
This guide is meant as an educational tool to assist in your understanding of ISO 20022 messaging as it relates to 
corporate action processing at [[DTCC]]. It should not be used as a basis for systems applications coding. For coding 
purposes, please refer to specific schemas and message implementation guides that can be found at 
https://www.[[DTCC]].com/[[settlement]]- and-[[Asset]]-services/corporate-actions -pr ocessing/iso-20022-messaging- specifications . 
 
Doc Info: March 09, 2021  
Publication Code:  CA222 
Service: [[DTC]] Corporate Actions  
Title: ISO 20022 Messaging for Reorganizations : Entitlements and Allocations  
 
 

---

## Page 3

Contents  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 3 
TABLE OF CONTENTS 
An Introduction to ISO 20022 Messaging ................................................................................... 8 
What is ISO 20022 Messaging? ................................................................................................. 8 
Benefits of Using ISO 20022 Messaging for Corporate Actions .......................................................8  
Benefits of Using ISO 20022 for Reorganizations Processing ........................................................9  
How Can I Learn More? ............................................................................................................9  
Data Dictionaries, Scenarios, Message Usage Guidelines, and Event Templates .........................11  
Data Dictionaries and Applicability to Reorganization Events ........................................................ 11 
Announcements Data Dictionary ............................................................................................. 12 
Using the Events Tab .......................................................................................................... 13 
Us ing the Elements  Tab ....................................................................................................... 15 
Entitlements and Allocations Data ........................................................................................... 17 
Elections (Instructions) Data Dictionary (CAST Message) ........................................................... 19 
Reorganization Scenarios ....................................................................................................... 21 
Reorganization Event Templates .............................................................................................. 22 
Introduction.......................................................................................................................... 22 
Reorganizations Message Usage Guidelines ............................................................................ 22 
To download a MUG from MyStandards: ................................................................................ 23 
[[PBS]] – ISO 20022 System Mapping for Reorganizations .............................................................. 31 
Reorganization Event Messaging .............................................................................................32  
Co rpo rate Actio ns  Mess ag es  in the Reo rg anizatio n Lif ecyc le........................................................ 32 
Messages Out of Scope for the Reorganization Life Cycle .......................................................... 33 
How to Read an MX Identifier .................................................................................................  34 
Supp lementary  D ata and  Mes s age Extens io ns.......................................................................... 34 
Reorganization Events and their Associated ISO 20022 Messages................................................ 35 
Reorganization Events and Their Identifiers .............................................................................. 35 
Event Descriptio ns ................................................................................................................ 35 
ISO 20022 Messages per Event.............................................................................................. 49 

---

## Page 4

Contents  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 4 
Out-of-Scope ....................................................................................................................... 49 
[[BASIC]] Message Flows for Reorganization Events ........................................................................ 50 
Mand ato ry  Ev ent Mess ag e Flo ws............................................................................................ 50 
Variation One: Other Mandatory Events.................................................................................. 51 
Vo luntary Ev ent Mes sage Flows ............................................................................................. 51 
Variation One: Voluntary Events ............................................................................................ 52 
Variation Two: Voluntary Events ............................................................................................ 53 
Variation Three: Voluntary Events.......................................................................................... 54 
Mess ag e Sub sc riptio ns  and Timing .......................................................................................... 55 
Mess ag e Times .................................................................................................................... 55 
Week ly Mess ag ing Times ...................................................................................................... 56 
Holiday Processing Schedule .................................................................................................  57 
Acco unt Balanc es .................................................................................................................. 58 
Corporate Action Notification with Eligible Balance (CANO-E) Messages....................................60  
What is a CANO-E Mes sag e? .................................................................................................. 60 
Balance Eligibility ................................................................................................................... 61 
Reorganization Events Using CANO-E Messages....................................................................... 62 
When Are CANO-E Mess ag es  Generated ?................................................................................ 62 
Mandatory Events................................................................................................................. 62 
CANO-E Messaging Period for Mandatory Events .................................................................... 62 
CANO-E Daily Mess ag ing Times  for Mand ato ry Ev ents ............................................................ 64 
Voluntary Events .................................................................................................................. 64 
CANO-E Messaging Period for Voluntary Events ..................................................................... 64 
CANO-E Daily Mess ag ing Times  for Vo luntary Ev ents .............................................................. 68 
Events Out of Scope ............................................................................................................. 68 
CANO-E Week ly  Mess ag ing Times ......................................................................................... 69 
CANO-E Ho lid ay Proc ess ing  Sc hed ule .................................................................................... 69 
CANO-E Mess ag e Subsc riptio ns .............................................................................................. 69 
Information Contained on the CANO-E Mes s age ........................................................................ 70 

---

## Page 5

Contents  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 5 
Corporate Action Movement Preliminary Advice (CAPA) Messages............................................72  
What is a CAPA Message? ..................................................................................................... 72 
Reorganization Events Using CAPA Messages .......................................................................... 73 
Events Not Generating a CAPA .............................................................................................. 73 
When Are CAPA Messages Generated ? ................................................................................... 74 
CAPA Message Triggers and Periods ...................................................................................... 74 
Additional Rules for CAPA Generation ..................................................................................... 76 
CAPA Message Subscriptions ................................................................................................ 76 
CAPA Daily  Mes s aging  Times ................................................................................................ 76 
CAPA Week ly  Mess ag ing  Times ............................................................................................. 76 
CAPA Holiday Processing Schedule ........................................................................................ 77 
Information Contained on the CAPA Message ............................................................................ 77 
CAPA Ob lig ated Balanc e ....................................................................................................... 77 
CAPA Ins tructed  / Uninstructed Balance .................................................................................. 77 
CAPA Message Body ............................................................................................................ 78 
CAPA Mess ag e Ex tens io n ..................................................................................................... 79 
Corporate Action Instruction Statement Report (CAST) Messages .............................................81  
What is a CAST Message?...................................................................................................... 81 
Reorganization Events Using CAST Messages........................................................................... 82 
When Are CAST Mes s ag es Generated ?.................................................................................... 82 
CAST Mes s ag e Generatio n.................................................................................................... 82 
CAST Messaging Periods..................................................................................................... 83 
CAST Mes s ag e Subs c riptio ns  / D aily  Mes s aging  Times ............................................................. 84 
CAST Week ly Mess ag ing Times ............................................................................................. 85 
CAST Ho lid ay  Pro c ess ing Sc hed ule ........................................................................................ 85 
Pag inatio n and  CAST Mes s aging ............................................................................................. 86 
Information Contained on the CAST Mess ag e ............................................................................ 86 
Corporate Action Movement Confirmation (CACO) Messages ....................................................92  
What is a CACO Message? ..................................................................................................... 92 

---

## Page 6

Contents  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 6 
Reorganization Events Using CACO Messages .......................................................................... 93 
When Are CACO Messages Generated? ................................................................................... 93 
CACO Message Generation ................................................................................................... 93 
CACO Mess ag e Subs c rip tio ns / D aily Mess ag ing Times ............................................................. 93 
CACO Weekly Messaging Times ............................................................................................ 94 
CACO Holiday Processing Schedule ....................................................................................... 94 
[[custody]] Reorg and Reorg Deposits .......................................................................................... 94 
D eb it Mov ements  o n the CACO ............................................................................................... 95 
Multiple Movements and CACO Messages ................................................................................ 95 
Pag inatio n and  CACO Mess ag ing fo r Reo rg anizatio ns ................................................................ 95 
Information Contained on the CACO Message ........................................................................... 96 
Information Contained in the CACO Message Extension............................................................. 98 
Corporate Action Event Processing Status Advice (CAPS) Messages....................................... 100 
What is a CAPS Message? ................................................................................................... 100 
Reorganization Events Using CAPS Messages ........................................................................ 100 
When Are CAPS Messages Generated? ................................................................................. 101 
CAPS Mess ag ing No tes ...................................................................................................... 101 
Week ly Mess ag ing Times .................................................................................................... 101 
CAPS Holiday Processing Schedule ...................................................................................... 102 
Information Contained on the CAPS Mess ag e .......................................................................... 102 
Appendix A: Messaging Scenarios for Reorganization Events ................................................. 105 
Scenario 1: Man dator y Re or ga nization  Even t Flow ............................................................... 105 
Scenario 2: Events “Not Processed at [[DTCC]]” ...................................................................... 106 
Scenario 3: Tender Offers .................................................................................................  107 
Scenario 4: Exchange (144A or REGS)............................................................................... 109 
Scenario 5: Exchange Offer (Cash and [[securities]], No Sub Event) .......................................... 110 
Scenario 6: Tender Offer (Consent) .................................................................................... 112 
Scenario 7: Voluntary Merger ............................................................................................ 114 
Scenario 8: Warrant Exercise ............................................................................................ 116 

---

## Page 7

Contents  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 7 
Scenario 9: Redemption of [[Warrants]] .................................................................................. 118 
Scenario 10: Con version .................................................................................................... 119 
Scenario 11: Full Call / Maturity (Convertible [[securities]]) .......................................................... 120 
Scenario 12: Mand ato ry  Put ................................................................................................ 121 
Scenario 13: Partial Mand ato ry Put ...................................................................................... 122 
Scenario 14: Optional Put ................................................................................................... 123 
Scenario 15: Put (Mor tga ge-Back ed ) .................................................................................... 125 
Scenario 16: Mandatory  Put for Cas h with Rig ht to  Retain ....................................................... 127 
Scenario 17: Mandatory Put for [[securities]] with Right to Retain    (Put Extendable) ...................... 129 
Scenario 18: Righ ts Su bscription ......................................................................................... 131 
Scenario 19: CD Early Redemptions and Survivor Options (“Death Puts”) .................................. 134 

---

## Page 8

An Introduction to ISO 20022 Messaging  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 8 
AN INTRODUCTION TO ISO 20022 MESSAGING 
What is ISO 20022 Messaging? 
ISO 20022 is an international messaging standard that is designed to simplify global business 
communication by creating a common language for communicating financial information that is 
unrestricted by national borders or regional conventions.  
Even though the Depository has maintained its own proprietary formats for many years, [[DTC]] recognized 
that it needed to respond to an evolving business environment and to accommodate an increasingly 
global investment business. [[DTC]]'s clients and customers had expanded their businesses throughout the 
world and wanted to streamline, as much as possible, the standards and formats used to communicate. 
ISO 20022 meets those needs and offers a host of benefits. 
[[DTC]] is therefore moving all of its corporate actions announcements and processing files from proprietary 
formats to this external, international format. 
Benefits of Using ISO 20022 Messaging for Corporate Actions 
One of the greatest benefits of ISO 20022 is its consistency and universality across the industry and 
around the globe. It provides a common language with its own ever-growing dictionary, enabling 
businesses in the financial industry to communicate corporate action information quickly, easily, and 
precisely.  
On a more local scale, the automation of previously manual processes via ISO 20022 messaging 
provides a significant cost savings to clients and a tremendous reduction in risk to the industry. With the 
advent of real-time messaging via ISO 20022, clients receive their data in a much more timely fashion, 
which allows them to manage their risk and streamline their processes. 
The Corporate Actions Transformation Learning Center provides a more comprehensive list of benefits.  
  

---

## Page 9

An Introduction to ISO 20022 Messaging  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 9 
Benefits of Using ISO 20022 for Reorganizations Processing 
The advantages of the ISO 20022 message arise from the use of more fielded data in a globally 
accepted, non-proprietary standard. This in turn facilitates logical, streamlined handling via straight-
through processing of Reorganization events. The flexibility inherent in the ISO 20022 standards allows 
for expanded usage of the [[DTC]] Corporate Actions messages that already exist (for Distribution and 
Redemption Events) via extension information, providing you with the most complete picture possible of 
your Reorganization events.  
The assignment of a single Event [[ID]] enables you to follow the results of each event from its 
announcement through the allocation of cash, [[securities]], or cash and [[securities]]. Rather than requiring 
access to several different screens (or functional entitlements) that performed different functions, you now 
have the ability to view and process Reorganizations directly at the corporate action composite record 
level.  
How Can I Learn More? 
Visit the Corporate Actions area of the [[Asset]] Services Learning Center at 
https://dtcclearning.com/products-and-services/[[Asset]]-services.html to view a wealth of business and 
technical information about the initiative, including the Benefits page and video, a Getting Started section, 
and a Readiness Checklist that provides you with a convenient method for determining your 
organization’s ability to begin processing ISO 20022 messages.  

---

## Page 10

An Introduction to ISO 20022 Messaging  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 10 
 
The Learning Center also contains introductory videos, extensive documentation, a link to FAQs, and 
further information regarding ISO 20022 messages and message scenarios. 
Note: You need to log in to see the full range of information available to you. First -time users should click Register 
Now in order to create an account. You need to be registered in order to view the Learning Center.  
 


---

## Page 11

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 11 
DATA DICTIONARIES, SCENARIOS, MESSAGE 
USAGE GUIDELINES, AND EVENT TEMPLATES 
Scenarios and data dictionaries can be found on [[DTCC]]’s Web site at 
http://www.[[DTCC]].com/news/2016/february/02/scenarios. 
Message Usage Guidelines can be found with their associated message specifications at 
http://www.[[DTCC]].com/matching-[[settlement]]-and-[[Asset]]-services/corporate-actions-processing/iso-20022-
messaging-specifications. 
Specific messaging scenarios for reorganization events can be found in Appendix A of this document. 
Data Dictionaries and Applicability to Reorganization Events 
Each data dictionary provides an overview of each event type in the ISO 20022 model and its relationship 
to existing [[DTC]] event types (function codes). It also provides a list of data elements, their level, and a 
cross reference from existing [[DTC]] elements to the ISO 20022 element. This allows clients to map 
elements from [[DTC]]’s legacy function code-based data model to the new ISO 20022 messages. An 
indication is also provided as to the level of compliance with global and U.S. industry norms. 
The data dictionaries are presented in a series of Excel spreadsheets. Each spreadsheet describes the 
data model as it relates to announcements, the corporate actions lifecycle, and instructions; each one 
describes the new data model, its relation to the existing [[DTC]] legacy model, and ISO standards.  
Each spreadsheet contains a number of tabs. [[DTC]] recommends that clients familiarize themselves with 
the tabs in each applicable data dictionary, and the type of information contained on each. Note that 
updates, additions, and deletions to any item in the dictionary are noted using red text and crossouts in 
the dictionary itself. 
Different data dictionaries exist for different phases in the Corporate Action event lifecycle. Within each 
spreadsheet, information is presented for Distributions, Redemptions, and Reorganizations. 
These data dictionaries apply to Reorganization events:  
• Announcements, 
• Entitlements and Allocations, and 
• Instructions (CAST message only)  
Note that the instructions data dictionary is only used for the CAST statement, which contains 
instructions that were input via [[DTC]] processing systems.  
• ISO 20022 messaging for reorg instructions will be performed at a later date. 

---

## Page 12

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 12 
Columns of applicability in each data dictionary allow you to filter each spreadsheet to display only items 
that apply to Reorganization events. 
Announcements Data Dictionary 
The Announcements Data Dictionary includes the following tabs. It is recommended that users start with 
the Legend tab as it provides a description of the information provided in the spreadsheet’s remaining 
tabs, which offer specific data element detail. 
• Legend. Start here to learn about the column names used throughout the data dictionary. 
• Events. View a complete list of [[DTC]]-defined event types, sub-event types, and their corresponding 
ISO codes. This is a good way to see the relationship between the [[DTC]] event structure and the 
equivalent ISO information.  
Use the “[[DTCC]] Event Group” column to limit the spreadsheet to view only Reorganization events. 
• Event Descriptions. These definitions explain all of the events covered in the previous tab. 
• Elements. A list of data elements contained in the new model.  
Use the “Event Category” column to limit this list to elements present in Reorganization 
announcement messages. 
• Options. A list of [[Option]] types and descriptions.  
Use the “Reorg Applicability” column to limit this list to elements present in Reorganization 
announcement messages. 
• Payouts. A list of payout types, payout descriptions, and associated ISO tags. 
• Security Rates. A list of payout indicators for [[securities]] that define products, processing, valid 
amounts, and event/payout security classes. 
• Cash Rates. A list of payout indicators for cash that define rules and event groups. 
• Event Statuses. A list of status codes for each event. 
• [[Asset]] Types. A list of sub issue type codes and descriptions. 
• IRS Tax Codes. A list of ISO Income Type codes and descriptions. 
• Pay Date – Earliest Pay Date. This lists the ISO Payment Dates and the ISO Earliest Payment 
Dates for a list of event types.  
These events may be mapped against the “Event Name” and/or “Event Code” columns on the Events tab 
to determine applicability to Reorganization events. 
The tabs that you will find the most helpful are the Events tab and the Elements tab. You can sort the 
columns on these sheets to display information that is relevant to reorganization events (as noted in 
italics above). 
 
 

---

## Page 13

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 13 
Using the Events Tab 
Sorting column F is the easiest way to limit the display to information for Reorganization events only. 
 
1. Click the Sort & Filter button. 
2. Click Filter. 
An arrow appears in the top right of each column. 
3. Click the arrow. 
The Sort/Filter box appears. 
4. Make your selections in the “Text Filters” list: 
• Uncheck the “Select All” checkbox. 
• Check the “[[DTCC]] Event Group” checkbox (to keep the column heading). 
• Check the “RedemptionReorganization” checkbox (to view changes). 
• Check the “Reorganization” checkbox. 
5. Click OK. 
The table is filtered to display Reorganization events only. 


---

## Page 14

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 14 
 
6. Use the scrollbar at the bottom right of the Excel window to view all of the columns on the 
sheet. 
 
• Columns I and J provide the legacy ([[DTC]]) activity codes that tie into the ISO event type 
codes and names (columns M and N).  
  


---

## Page 15

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 15 
Using the Elements Tab 
The Elements tab is also useful for understanding the content of Announcements messages for 
Reorganization events.  
Column L denotes the elements that specifically refer to Reorganizations. By removing the rows that [[DO]] 
not have a check in this column, you can view only those message elements that apply to Reorganization 
announcements. 
 
1. Click the Sort & Filter button. 
The Sort/Filter menu appears. 
2. Click Filter. 
Arrows appear in the top left corners of the column headers. 
3. Click the arrow in the top right of the L column. 
The Sort/Filter box appears. 
4. Click ü. This is the symbol for the check mark that appears in this field, meaning that the 
element applies to Reorganization events. 
5. Click OK. 
The spreadsheet is displayed using only the elements applicable to Reorganizations.  


---

## Page 16

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 16 
 
Note: Columns C and D provide each element’s name and description.  
 
6. Use the scrollbar at the bottom right of the Excel window to view all of the columns on the 
sheet. You can find information such as data source, data type, name changes, valid values, 
and automated/mapped delivery.  


---

## Page 17

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 17 
 
Note that columns Q and R provide the x-path for each element: 
• Q provides the location of the element in the schema for the core message. 
• R provides the location of the element in the schema for the message extension. 
Entitlements and Allocations Data  
The Entitlements and Allocations Data Dictionary includes tabs for each ISO lifecycle message type. The 
tab contains a spreadsheet of data elements contained in that message type.  
Each row presents an element as well as its associated information: an explanation of what it is, which 
event group (Distributions, Redemptions, Reorganizations) it is applicable to, and the name of the legacy 
[[CCF]] file this information can be traced back to. Notes are included for Distributions, Redemptions, and 
Reorganizations where applicable.  
In addition to tabs dedicated to specific message information, separate tabs list the reason codes for 
CAPA, CACO, and CAPS messages, as well as sub reason codes and unallocated codes for CAPA and 
CACO messages, [[Option]] information, payout information, security rates, cash rates, and Reorg cash 
rates. 
You can limit each message type to display elements that apply only to Reorganization events. Where 
applicable, you can limit some of the informational tabs as well. 
Note that the CARE and CAPC tabs [[DO]] not apply to Reorganization events.  
For cash rate information, please use the Reorg Cash Rates tab. It is optimized for reorganization 
events.  


---

## Page 18

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 18 
To view information about cash rates for Reorganization events, use the Reorg Cash Rates tab. 
 
1. Click the arrow in the Applicability Reorganization column: 
• On the CANO-E, CAPA, and CACO tabs, this is the I column. 
• On the CAPS tab, this is the J column. 
• On the Options tab, this is the F column. 
2. Uncheck Select All. 
3. Click the checkbox next to Y. 
4. Click OK. 
The sheet is then limited to message elements that apply to Reorganization events. Column 
A, ISO Message Field Name (or “ISO Message Field” in some cases), lists all of these 
elements. 
5. Use the scroll bar to see all of the columns on this sheet.  
Note: The “X-Path” column on each message sheet (CANO -E, CAPA, CACO, etc.) provides the location 
of each element within that message’s schema.  
Click another tab on the bottom to see information for a different message type or information 
related to these messages. 


---

## Page 19

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 19 
Elections (Instructions) Data Dictionary (CAST Message) 
The core CAST message is used for Reorganization events to provide each subscribed customer with 
their instructed and uninstructed balances for each CA event. The message extension provides 
information about options that fall within the eligible [[DTC]] service’s reporting period. For the purposes of 
Reorganization events, the CAST message extension compiles instruction information that was entered 
elsewhere and reports it to the customer, saving research time and reducing errors. 
The CAST message contains many new elements to accommodate its use for reorgs. You can limit the 
CAST message information to display only the elements that apply to reorganization events. 
 
1. On the CAST tab, select the I (“Reorg Applicability”) column. 
2. Click Filter on the home menu. 
Column I displays a “down arrow” button.  
3. Click the  button. 
The text filter menu appears. 


---

## Page 20

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 20 
 
4. Click the checkboxes next to X and Reorg Applicability. Deselect “(Blanks).” 
5. Click OK. 
The spreadsheet is displayed using only the events applicable to Reorganizations.  
• Columns D and E define the elements used in the CAST message and provide their rules 
for use as per their context in Reorganization events: 
 
  


---

## Page 21

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 21 
• Note that column H provide s the x-path for each element: 
 
Reorganization Scenarios 
The Corporate Action Event Announcements Business Scenarios for Reorganizations spreadsheet 
contains an array of event type tabs. The spreadsheet on each tab presents at least one scenario for 
each event type. The scenario contains the major data elements for the event type and the values you 
can expect to see for each. 
 
Specific messaging scenarios for reorganization events can be found in Appendix A of this document.  


---

## Page 22

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 22 
Reorganization Event Templates 
Introduction 
In addition to providing message usage guidelines for announcements, you can now see a subset of the 
announcements data that applies to Reorganization events only.  
These Reorganization event templates restrict the announcements information at the Reorganization 
event level (such as tender offers, mergers, etc.) at both the core message and extension message 
levels.  
This allows you greater insight into the contexts of Reorganization events. You can see relevant metadata 
about these elements: rules and comments that are specific to each element’s usage during a specific 
event, as well as annotations and synonyms that explain where each data element came from and the 
legacy data attribute name for each. 
To view these event templates, please visit Swift’s My Standards Web site at 
https://www2.swift.com/mystandards/. 
Reorganizations Message Usage Guidelines 
While you can obtain the SR 2017 standards from the [[DTC]] website, you can also access the full suite of 
messages on SWIFT’s MyStandards website. The benefit to this is a more in-depth view of the data and 
its usage. 
Message Usage Guidelines (MUGs) define [[DTC]]’s restrictions of the base standard message for each ISO 
20022 message. They provide the ability to show all required and optional fields utilized in the message. 
In addition to usage rules, comments and synonyms help describe each data element and its context in 
relation to the [[DTC]] data model or legacy [[CCF]] file.  
The MUGs are stored on the MyStandards area of the SWIFT Website at 
https://www2.swift.com/mystandards/. They can be exported as PDF files, Excel spreadsheets, or Zip files 
that contain XML schemas of your choice (enriched XML schemas, plain XML schemas, or XML schema 
packages). Each MUG refers to a specific message (CANO, etc.) or message extension.  
The MUG can be used to cross-reference an ISO 20022 component with its [[DTC]] name. Each [[DTC]] 
element’s name, definition, and usage rules listed in the dictionary are noted with the corresponding ISO 
element in this document. 
  

---

## Page 23

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 23 
To download a MUG from MyStandards: 
1. Log in to MyStandards at https://login.swift.com/swift/login/login_mystandards.html. 
 
  


---

## Page 24

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 24 
2. Click Groups on the top menu. 
 
This brings you to the Groups page. It displays all industry groups that use MyStandards. 
  


---

## Page 25

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 25 
3. Click [[DTCC]] – Corporate Action Transformation. 
 
This brings you to the home page for [[DTCC]]’s Corporate Actions Transformation group. 
  


---

## Page 26

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 26 
4. Under Usage Guidelines, click more guidelines. 
 
  


---

## Page 27

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 27 
5. Click the schema name that you want to download. 
Notes: 
● Make sure that you are working with the latest Standard Release (“SR”).  
● The list available on the SWIFT website may differ from the image below.  
 
The list of guidelines within that grouping appears. 
  


---

## Page 28

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 28 
6. Click the folders to the right of the CANO message and the CANO message extension (a) to 
select them for downloading. 
 
The folder icon at the top displays “2.” 
  


---

## Page 29

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 29 
7. Click the My Selection folder. 
 
The list of message guidelines appears on the left and an action menu appears on the right. 
 
8. Click your download method. Note that you can go back and download any number of 
formats you want. 
A list of export options appears for your download type. 
  


---

## Page 30

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 30 
9. Click the export [[Option]] you want to use. 
 
An information box appears when your download is in process. 
  


---

## Page 31

Reorganization  Data Dictionar ies, Scenar ios, Message Usage Guidelines, and E vent Templates 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 31 
10. Click My Downloads section to get to the My Downloads page. 
 
(You can also click Close to dismiss the window.) 
The My Downloads page appears. 
 
11. Click the item you want to save to your computer. 
 
[[PBS]] – ISO 20022 System Mapping for Reorganizations 
Documentation regarding Legacy Mappings can be found at 
http://[[DTCC]].com/news/2013/january/01/legacy-mapping.aspx. 
This documentation includes: 
• Legacy Data Files: Provides a list of existing [[DTCC]] data files that will be replaced by ISO 20022 
messages under this initiative.  
• Mapping Legacy to [[DTCC]] New Model (zip). Contains a PDF file “[[DTCC]] Corporate Action Legacy 
Mapping Overview” as well as a series of Excel spreadsheets that enable users to map from legacy 
[[CCF]] files to ISO 20022 publication files.  


---

## Page 32

Messaging for Reorganizations  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 32 
REORGANIZATION EVENT MESSAGING 
Corporate Actions Messages in the Reorganization Lifecycle 
There are seven types of messages in the ISO 20022 group that pertain to reorganization events: 
 
• Corporate Action Notification (CANO) 
• Corporate Action Cancellation Advice (CACN) 
• Corporate Action Notification with Eligible Balance (CANO-E)  
• Corporate Action Movement Preliminary Advice (CAPA) 
• Corporate Action Movement Confirmation (CACO) 
• Corporate Action Event Processing Status Advice (CAPS) 
• Corporate Action Instruction Statement Report (CAST) 
The last two digits in the MX Identifier and the Extension code signify the version number. The MX 
version number and/or the Supplementary version number may change during the SWIFT annual release 
based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center
. 
The messages that are discussed in this guide include the CANO-E, CAPA, CACO, CAPS, and 
CAST messages. 
Note: These messages w ork differently for Reorganizations than they have for Distributions and Redemptions.  
• The CANO-E provides the eligible balance for reorganization events based on event key date(s). 
Additionally, it provides instructed, uninstructed, and uncovered protect balances for these events. A 
replacement CANO message is sent when changes are made to eligible balances or instructed 
position. Some event scenarios will have “CANO-E Only” messaging. CANO-E messages are also 
sent for those events not processed at [[DTC]] (52N/tenders, 54N/conversions, 58N/repayments, and 


---

## Page 33

Messaging for Reorganizations  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 33 
60N/[[Warrants]]), providing clients with their position if they wish to participate directly with the [[issuer]] / 
Agent. 
• The CAPA message provides pre-advice of payment for [[securities]] or cash payments relating to 
reorganization events. It also provides instruction level pre-advice of [[securities]] or cash entitlements 
as well as event-level instructed and uninstructed balances.  
The CAPA extension provides information for instruction processing including Transaction [[ID]] (VOI) 
and Transaction Sequence Number. 
The CAPA is only applicable for voluntary put events, warrant redemptions, and full call / maturity 
conversions. It provides pre-advice of payment on events with a defined payment date. Since other 
reorganization events project and allocate on the same day, they will not produce CAPA messages. 
• CACO messages in the Reorganization lifecycle provide extension information that details 
entitlements at the instruction level for a given cash or [[securities]] allocation. They also show 
expanded information involving events with [[Option]] proration by adding extended elements such as 
accepted / unaccepted balances. CACO messages also provide greater detail relating to Rights 
Subscription events, including instruction entitlements for subscriptions and oversubscriptions, 
subscription charges, and subscription refund details. 
• The CAST messages for the Reorganization lifecycle are greatly expanded for use with Reorg 
events. A message extension now provides the transaction detail related to Reorg instruction totals, 
which have been manually entered utilizing other systems. They show open Reorganization events 
with instructed / uninstructed balances and are sent intraday close to the [[DTC]] instruction deadlines. 
CAST messages also provide per-event instructions or protect instructions that have been processed 
that day, and provide instruction status for those instructions that are not in a final state. 
• The CAPS messages provide unallocated balance information at an account level. They are 
applicable to events with a declared payable date that have not allocated. CAPS messages are only 
sent for events that send a CAPA message (e.g., PUT events). The messages provide high-level 
reason codes (such as fail reason codes and unallocated reason codes) for reorganization events. 
All of the messages involved in this process are contingent upon the client having an eligible balance in 
the event. Certain reorganization events will produce a CANO-E message only. Unless you have an 
eligible balance, you will only see the announcement message for the event.  
Messages Out of Scope for the Reorganization Life Cycle 
The following messages are out of scope for Reorganizations: 
• CAPC. Corporate Actions Preliminary Advice Cancellation 
• CARE. Corporate Actions Movement Reversal Advice. 
Note: Reversals for reorganization allocations will be done via CACO adjustments.  
  

---

## Page 34

Messaging for Reorganizations  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 34 
How to Read an MX Identifier 
The MX Identifier identifies the business area, message [[ID]], and version of an ISO Message. 
As an example, for the identifier seev.035.002.08: 
• The first four alphabetic characters (“seev”) identify the business area. In this case, it is “[[securities]] 
Events.” You can see the full list of business areas on the ISO 20022 Web site at 
http://www.iso20022.org/documents/general/ISO20022_BusinessAreas.pdf. 
• The next three characters (035) are the message identifier. The message in this example is a CAPA 
message. 
• The next three characters (002) are the “variant” identifier. Since “001” is always the main ISO 
message, “002” would be the second variant (and the one that is compatible with ISO 15022). [[DTC]] is 
using the second variant in order to comply with the industry’s requirement that the ISO 20022 
messages we generate be backward compatible with ISO 15022. 
• The last two characters (08) are the “version.” In this example, this is the sixth version of this 
message, representing SR 2017.  
Note: The final two digits have the potential to change with each release.  
For your coding purposes, be sure to consult the latest documentation for the most current version 
number. 
Supplementary Data and Message Extensions 
The [[DTC]] implementation of ISO 20022 will make use of an ISO 20022 concept of supplementary data, 
also called “extensions.” 
Certain [[DTC]] corporate actions elements are not covered by the standard ISO messages. These elements 
are implemented using the supplementary data components. The data fields within the supplementary 
data have been modeled using the ISO 20022 principles and will reside in the ISO 20022 
data 
dictionaries. 
In terms of Reorganization messaging, the supplementary data is provided in message extensions. These 
extensions allow [[DTC]] to provide an agreed-upon and machine-readable structure within the messages 
for those data elements that have not been globally agreed to form part of the main message. Note that 
the structure of the extension must be validated by the ISO community and registered within ISO 20022, 
and this process includes the addition of the elements to the ISO 20022 data dictionaries. This allows for 
improved interoperability while avoiding an impact on the messages themselves which may have been 
implemented in other communities. 

---

## Page 35

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 35 
Reorganization Events and their Associated ISO 20022 Messages 
The majority of Reorganization event types are covered by ISO 20022 messaging for corporate actions.  
Reorganization Events and Their Identifiers 
Reorganization events are referred to in a number of ways in this document.  
The legacy [[DTC]] activity codes and function codes group events with similar behavior throughout the 
event lifecycle. The newer ISO codes allow for greater specificity with particular event and sub event 
types. 
When this document refers to particular behaviors, the legacy codes are often used.  
Reorganization 
Event Codes  
This document shows the mapping per ISO event type code, sub event type, 
and extended sub event type code. It links these SWIFT codes to their relevant 
legacy activity codes. 
Documents at the beginning of each message chapter map the codes for all reorganization events that 
apply to that message type. 
Event Descriptions 
Event Name Event Description 
CD Early 
Redemption 
A feature of a security that allows an [[issuer]] to make a payment to the 
security holder. This event will be used for [[securities]] subject to 
redemptions other than those categorized as full and partial calls (e.g., 
early CD redemptions). 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
REDM VOLU   53 CDRD  
  

---

## Page 36

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 36 
Change  
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
PLAC MAND Domicile Identifies an event 
in which the [[issuer]] 
has changed the 
domicile of the 
corporation. 
or 
A change in the 
place of 
incorporation of the 
legal entity of the 
issuing company. 
93   
CHAN MAND Reclassified Identifies a change 
in classification of a 
security. For 
example, Class A 
common [[shares]] are 
reclassified as 
Class B. 
93   
Conversion Conversion of [[securities]] (generally convertible [[Bonds]] or preferred 
[[shares]]) into another form of [[securities]] (usually common [[shares]]) at a pre-
stated price or rate. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
CONV MAND  Non-specific 
conversion event. 
93   
CONV VOLU   52 
54 
54N 
  
  

---

## Page 37

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 37 
Dutch Auction Identifies a tender event in which [[The Corporation]] offers to purchase up to 
a certain amount of [[securities]] within a price range. Holders must submit a 
specific price within that range that they would be willing to accept. The 
actual tender price is not determined until the end of the offer. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
DTCH VOLU Dutch 
Auction 
 52 
52N 
  
Exchange Offer An offer to surrender [[securities]] in exchange for other [[securities]] or a 
combination of [[securities]] and cash. The exchange may also include a 
consent solicitation. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
EXOF VOLU  Non-specific 
exchange offer 
event. 
52 
52N 
  
EXOF VOLU   52N TMTN  
EXOF VOLU 144a Identifies an event 
in which the 
security is a 144a 
[[Private Placement]] 
security. 
52 
52N 
 A114 
EXOF VOLU Cash and 
[[securities]] 
Identifies an event 
with a combination 
of Cash and 
[[securities]] as 
payout. 
52 
52N 
 CASE 
EXOF VOLU Consent Identifies an event 
that includes a 
consent fee. 
52 
52N 
  
EXOF VOLU [[Reg S]] Identifies an event 
in which the 
security is a 
[[Regulation S]] type. 
52 
52N 
 REGS 
  

---

## Page 38

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 38 
EXOF VOLU Unwind Identifies an event 
in which 
"unwinding" of the 
basket of [[securities]] 
occurs.  
51  UNWD 
   Example: in order to participate in the tender offer of one of 
the underlying [[securities]], the holder must unwind the 
basket. [[DTC]] creates the event for the holder to respond - 
"unwind." The tender offer itself would be a separate event.  
Or, this is a notification that a [[UIT]] can be unwound in 
IVORs (a separate instruction system) with the expiration 
dates supplied. 
Full Call The security is redeemed for cash in its entirety on a date that is prior to 
the maturity date, and for which the holders receive the principal amount 
of the security. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
MCAL MAND Full Call  69   
General Information General information provided by the [[issuer]] that should not result in 
material changes to the security. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
OTHR MAND  Non-specific 
General Information 
event. 
93 
58 
  
OTHR MAND Important 
Notice 
Identifies an 
information-only 
event of [[DTC]] 
Money Market 
Instrument (MMI) 
Important Notice 
announcements.  
96  NOTI 
   Announcements are based on changes to the MMI security 
that are entered by the agent. These are specific to MMI 
Important notices only. 
  

---

## Page 39

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 39 
[[liquidation]] A company reports its intentions to dismantle its business, paying off 
debts in order of priority and distributing the remaining assets in cash 
and/or [[securities]] to the owners of the [[securities]]. The payment of 
proceeds may require the presentation of [[securities]]. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
LIQU MAND Presentation 
Required 
Identifies an event 
processed as Reorg 
event and may 
include options. 
79 
93 
 PREQ 
Mandatory 
Exchange 
A corporate action requiring the surrender of certificates to be exchanged 
for a new security or cash. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
EXOF MAND  Non-specific 
Mandatory 
Exchange event. 
93   
Mandatory Put The mandatory exchange of all outstanding [[Bonds]] (with a putable 
feature) for cash or a new security where the event security is 
remarketed. The [[issuer]] may offer holders the right to retain their 
[[securities]] instead of exchanging them. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
BPUT MAND  Non-specific 
Mandatory Put 
event. 
65 
65G 
  
BPUT CHOS Retain Identifies an event 
that includes an 
[[Option]] to retain the 
event [[securities]] 
rather than 
exchange them. 
65B 
65R 
  
  

---

## Page 40

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 40 
Maturity The final repayment, usually in cash, by an [[issuer]] for the entire issue, or 
for remaining outstanding [[securities]] of a specific security on a specified 
date. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
REDM MAND  Non-specific 
Maturity event. 
69  CONV 
REDM MAND [[securities]] Identifies an event 
in which the 
payment will be 
made in the form of 
[[securities]]. 
93  SECU 
Meeting 
([[Proxy]] message) 
A meeting of a company's share or bond holders to address resolutions 
put forth by the [[issuer]]. 
Meeting 
Type 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event Description Function 
/ Activity 
Code 
Classification 
Code 
GMET MAND Annual Identifies an annual meeting 
event of the company on 
behalf of security holders. 
80 AMET 
XMET MAND Extraordinary  80  
GMET MAND General Identifies a meeting event 
called by the company on 
behalf of security holders at 
which the company can 
present corporate 
resolutions that may require 
a [[vote]] by the holders. 
80  
SPCL MAND Special  80  
  

---

## Page 41

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 41 
Merger The exchange of one company's security for another company's security, 
cash, or a combination of cash and [[securities]]. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
MRGR MAND  Non-specific 
election merger 
event. 
93   
MRGR VOLU   52M (s)   
MRGR MAND Cash Identifies an event 
with a payout of 
cash only. 
72  CASH 
MRGR MAND Cash and 
[[securities]] 
Identifies an event 
with a combination 
of cash and 
[[securities]] payout 
only. 
90  CASE 
MRGR MAND [[securities]] Identifies an event 
with a payout of 
[[securities]] only. 
71  SECU 
Name Change The [[issuer]] changes its name or the name of its security/[[securities]]. This 
may involve surrendering physical [[securities]]. A new security identifier 
may be assigned to the new name, especially if new [[securities]] are 
issued.  
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
CHAN MAND   91 
93 
  
CHAN MAND Presentation 
Required 
 91 
93 
 PREQ 
  

---

## Page 42

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 42 
Odd Lot Offer Identifies a tender offer event made by [[The Corporation]] or its agent to 
purchase [[shares]] from odd-lot shareholders. An odd-lot shareholder 
typically refers to a holder of less than 100 [[shares]] of [[Stock]]. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
ODLT VOLU   52 
52N 
  
Partial Mandatory 
Put 
The mandatory exchange of a portion of [[Bonds]] in which the exchanged 
[[securities]] are usually remarketed. The [[issuer]] may offer holders the right 
to retain instead of exchanging their [[securities]]. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
BPUT MAND   65P   
BPUT CHOS Retain Identifies an event 
that includes an 
[[Option]] to retain the 
event [[securities]] 
rather than 
exchange them. 
65 
65R 
  
Plan of 
Reorganization 
Reorganization plan devised by the company or trustees that is usually 
associated with a bankruptcy filing.  
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
BRUP VOLU [[vote]] Identifies an event 
in which a 
[[vote]]/consent is 
sought for the plan 
of reorganization. 
94   
BRUP MAND  Identifies an 
information-only 
event for the plan of 
reorganization. 
94   

---

## Page 43

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 43 
Put A feature of a bond that entitles the holder to elect to surrender the bond 
for cash during a predetermined time period and with a predetermined 
payable date. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
BPUT VOLU  Non-specific put 
event. 
52 
58 
58B 
58N 
  
BPUT VOLU Mortgage-
Backed 
Indicates an event 
in which the Issue 
has an early 
redemption feature 
that allows the 
holder to elect to 
sell [[Bonds]] back to 
the [[issuer]] on a 
monthly basis, 
according to 
specified 
conditions. 
62 
62B 
 MBCK 
BPUT VOLU Survivor 
Options 
Indicates an event 
in which the issue 
has an early 
redemption feature. 
This feature allows 
the holder to elect 
to sell [[Bonds]] back 
to the [[issuer]] on a 
predetermined 
basis (excluding 
monthly) according 
to specific priorities. 
66P  SOPT 
  

---

## Page 44

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 44 
Redemption of 
[[Warrants]] 
An event in which the [[issuer]] pays proceeds to holders at or after the 
expiration date of the warrant rather than expire the warrant for no cash 
(worthless). 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
REDM MAND   61   
Reorganization A reorganization event announced by the [[issuer]] that cannot be classified 
as another event. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
OTHR MAND   93   
OTHR VOLU   52 
52N 
  
Reverse [[Stock]] Split The exchange of a company's security for the same company's new 
security at a preset rate. This corporate action reduces the number of 
[[shares]] outstanding.  
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
SPLR MAND   73   
Rights Subscription A privilege granted to holders of rights to purchase new or additional 
[[securities]]. Rights are often tradable in a [[secondary market]]. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
EXRI VOLU   59 
93 
  
  

---

## Page 45

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 45 
Security Separation The separation of a “unit” security (that consists of two or more [[securities]] 
that were originally issued individually) back into individual components.  
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
 MAND   93   
DETI VOLU   54N   
[[Stock]] Split The increase in a company's number of [[outstanding shares]] of [[Stock]] 
without any change in the shareholder's [[Equity]] or the aggregate market 
value at the time of the split. The share price is normally reduced. 
Forward split events are included here.  
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
SPLF MAND Presentation 
Required 
 93  PREQ 
  

---

## Page 46

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 46 
Tender Offer An offer made to security holders, normally by a third party, requesting 
them to sell (tender) their [[securities]] for a specified price (usually at a 
[[Premium]] over prevailing market prices). Generally, the objective of a 
tender offer is to take control of the target company. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
BIDS 
([[issuer]]) 
TEND 
(offeror) 
VOLU Bid Tender / 
Sealed 
Tender 
Identifies a tender 
offer event in which 
the holder can 
choose the price at 
which they are 
willing to tender 
their [[securities]]. This 
price may or may 
not be accepted by 
the offeror.   
52 
52N 
 BTST 
BIDS 
([[issuer]]) 
TEND 
(offeror) 
VOLU Cash and 
[[securities]] 
Identifies an event 
with a combination 
of Cash and 
[[securities]] as 
payout. 
52 
52N 
 CASE 
TEND VOLU Cash in Lieu Identifies a [[DTC]]-
specific sub-event 
in which holders 
can elect to "sell" 
whole [[shares]] to 
satisfy fractional 
entitlements 
(usually as a result 
of a merger) at the 
[[Beneficial Owner]] 
level. 
52  CILI 
BIDS VOLU Consent Identifies a tender 
offer event that 
includes a consent 
fee. 
52 
52N 
  
BIDS 
([[issuer]]) 
TEND 
(offeror) 
VOLU Convert and 
Tender 
Identifies a tender 
offer event in which 
the holder must 
convert [[securities]] in 
order to take part in 
the event. 
54T  COTE 

---

## Page 47

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 47 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
NOOF VOLU Mini Tender Identifies a tender 
offer event 
presented by a third 
party to 
shareholders of the 
target company, in 
which the 
conditions of the 
offer (e.g., quantity 
sought) are less 
than the 
requirements 
established by 
market regulators. 
As such, regulatory 
approval is not 
required. 
52 
52N 
 MITE 
TEND VOLU Offer to 
Purchase 
Identifies a tender 
offer event made by 
another company or 
the issuing 
company (buy 
back) to purchase a 
portion or all of the 
[[outstanding shares]]. 
52 
52N 
 FTPR 
BIDS VOLU Self-Tender Identifies a tender 
offer event made by 
the issuing 
company (buy 
back) to purchase a 
portion or all of the 
[[outstanding shares]]. 
52 
52N 
 SETE 
  

---

## Page 48

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 48 
Termination A security, usually a form of a derivative (e.g., [[ADR]] or [[UIT]]), for which the 
agent or [[issuer]] has decided to terminate the derivative based on a 
change to the underlying security/[[securities]] or a change in strategy. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
EXOF MAND [[ADR]] Identifies when the 
event security is an 
[[ADR]]. 
93 TMTN ADRS 
EXOF MAND GDR Identifies when the 
event security is a 
GDR. 
93 TMTN GDRS 
EXOF VOLU [[ADR]] Identifies when the 
event security is an 
[[ADR]]. 
52N TMTN ADRS 
EXOF VOLU GDR Identifies when the 
event security is a 
GDR. 
52N TMTN GDRS 
[[Warrants]] Exercise A feature of a security that permits the holder to exercise an [[Option]] to 
exchange the security into another form (usually, [[Warrants]] into [[shares]]). 
The exercise will commonly require a payment based upon a 
predetermined value and time. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
EXWA VOLU  Non-specific 
[[Warrants]] exercise 
event. 
60 
60N 
52 
  
Worthless [[DTC]] is advising its participants that their positions in that security will be 
taken down. The announcement is created when [[DTC]] receives a formal 
letter advising that [[securities]] held are worthless. 
Event 
Code 
Mandatory, 
Voluntary, 
or Choice? 
Sub Event 
Name 
Sub Event 
Description 
Function
/ Activity 
Code 
Extended 
Event 
Type 
Extended 
Sub Event 
Type 
WRTH MAND   93   
 

---

## Page 49

Reorganization Events and their Associated Messages  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 49 
ISO 20022 Messages per Event 
Not all ISO 20022 messages apply to all event types. 
Messages per 
Reorg Event  
This document specifies the individual messages that apply to each event type. 
 
Out-of-Scope 
The following function codes are out of scope for lifecycle messaging for reorganization events: 
ACTIVITY CODE CA WEB EVENT TYPE ACTIVITY CODE DESCRIPTION 
51 Exchange Offer / Unwind [[UIT]] Rollover  
80 Consent with No Exchange  [[Proxy]]  
91 Name Change Name Change 
94 Plan of Reorganization 
([[vote]]) Bankruptcy  
96 General Information 
(Important Notice)  General Information  
 
See the Reorganization Event Codes mapping document for full event type information. 
 

---

## Page 50

Message Flows and Timing 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 50 
[[BASIC]] Message Flows for Reorganization Events  
The following diagrams illustrate the overall message flow for mandatory and voluntary events in general 
terms. Particular situations deviate from these simplified flows.  
Please see Appendix A: Messaging Scenarios for Reorganizations for individual event types and detailed 
message flows. 
Mandatory Event Message Flows 
At its simplest, the most common message flow for mandatory events can be summed up as follows:  
 
Flow for [[Warrants]], Put Events, and Maturities 
An event is announced. A client is notified of their eligibility for the event. Payment pre-advice is sent to 
the client. After the payment is made, a confirmation for that payment is sent to the client. 
  


---

## Page 51

Message Flows and Timing 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 51 
Variation One: Other Mandatory Events  
 
Flow for Mergers, Reverse Splits, Mergers (CASE), and General Corporate Actions 
An event is announced with a CANO NEWM and is later updated (for example, with a payment date) in a 
CANO REPL. This drives the production of the CANO-E. The allocation is then made without a preadvice, 
and a CACO message confirms the allocation. 
 
Voluntary Event Message Flows 
Voluntary events can take a greater variety of messaging paths than mandatory events. They are 
presented in summary below. 
At its simplest, the most common message flow for voluntary events can be summed up as follows:  
 
Flow for Tenders, Exchanges, Election Mergers, Conversions, Convert and Tenders,  
Rights Subscriptions, and Warrant Exercises 


---

## Page 52

Message Flows and Timing 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 52 
An event is announced. A client is notified of their eligibility for the event. During an instruction period, the 
client can enter instructions using a method outside of ISO 20022 messaging. At some point after the 
close of the messaging period, a payment is made based on the client’s eligibility and the sum of any 
instructions that were received. After the payment is made, a confirmation for that payment is sent to the 
client (without preadvice of the allocation). 
Variation One: Voluntary Events 
 
Flow for CD Early Redemptions 
This flow illustrates messaging behavior for long-term events. The event is announced. At some point 
later on, instructions are made on the event. The allocation is driven by the instructions. A confirmation is 
sent after the allocation is made (without preadvice of the allocation). 
 
  


---

## Page 53

Message Flows and Timing 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 53 
Variation Two: Voluntary Events 
A second variation on this flow is as follows: 
 
Flow for Mortgage-Backed PUTs and Survivor [[Option]] PUTs 
This flow also illustrates messaging behavior for long-term events. The event is announced. At some 
point later on, instructions are made on the event.  
A CAPA message that projects the payment may be sent if the agent selects a Transaction [[ID]] for the 
payment, allowing for a partial payment of the instructions. A CACO message is sent to confirm the 
partially paid instruction; it also notes the remaining balance to be paid at a future time. 
 
  


---

## Page 54

Message Flows and Timing 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 54 
Variation Three: Voluntary Events 
 
Flow for Voluntary Puts (Repayments and Retainments) 
An event is announced. A client is notified of their eligibility for the event. During an instruction period, the 
client can enter instructions using a method outside of ISO 20022 messaging. Pre-advice is sent one or 
more times during a messaging period. At some point after the close of the messaging period, a payment 
is made based on the client’s eligibility and the sum of any instructions that were received. A confirmation 
for that payment is then sent to the client. 
 
Please see Appendix A: Messaging Scenarios for Reorganizations
 for individual event types and detailed 
message flows. 
For a complete list of data elements for each message, their origins, and their usage, please utilize the 
Message Usage Guidelines available at [[DTCC]].com, the Learning Center, or My Standards at 
https://www2.swift.com/mystandards/.  
  


---

## Page 55

Message Flows and Timing 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 55 
Message Subscriptions and Timing  
There is one [[BASIC]] subscription for reorganization event messaging. You can subscribe to individual 
messages within that regular subscription.  
The following tables describe general message times, as well as general processing times and holiday 
schedules. 
Message Times 
All times are given in Eastern Standard Time. These times [[DO]] not reflect holiday processing. 
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
MESSAGE MESSAGE TIMES APPLIES TO EVENTS: 
CANO-E 
Both file and real time at:  
• 12:00 p.m. 
• 1:30 p.m. 
• 4:00 p.m. 
• 4:30 p.m. 
• 5:00 p.m. 
• 8:00 p.m. 
Mandatory:  61, 65, 65G, 65P, 69, 71, 72, 
73, 79, 90, 93 
Voluntary:  52, 52M, 54, 54T, 58, 58B, 
59, 60, 65B, 65R 
Not processed at [[DTC]]:  
52N, 54N, 58N, 60N  
CAPA 
Both file and real time at:  
• 1:30 a.m. 
Mandatory:  61, 65, 65G, 65P, 69  
Voluntary:  58, 58B, 62, 62B, 65B, 65R, 
66P 
CACO 
Via file:  
• 4:00 p.m. 
Real time:  
• Every 20 minutes between  
8:00 a.m. and 3:30 p.m.  
Mandatory:  61, 65, 65G, 65P, 69, 71, 72, 
73, 79, 90, 93 
Voluntary:  52, 52M, 53, 54, 54T, 58, 
58B, 59, 60, 62, 62B, 65B, 
65R, 66P 
CAPS 
Via file:  
• 4:00 p.m. 
Real time:  
• Between 1:00 p.m. and 4:00 
p.m. 
Mandatory:  65, 65G, 65P 
Voluntary:  58, 58B, 65B, 65R 
CAST 
Both file and real time at:  
• 12:00 p.m. 
• 1:30 p.m. 
• 4:00 p.m. 
• 4:30 p.m. 
• 8:00 p.m. 
Mandatory:  N/A 
Voluntary:  52, 52M, 53, 54, 54T, 58, 
58B, 59, 60, 62, 62B, 65B, 
65R, 66P 
  

---

## Page 56

Message Flows and Timing 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 56 
Weekly Messaging Times  
Generally, messages for reorganization events are sent Monday through Friday.  
No messages are sent on Saturday or Sunday aside from the original CANO announcement: 
MESSAGE MONDAY – FRIDAY  SATURDAY AND SUNDAY 
CANO Normal message volumes.  
Files transmitted based on customer 
subscription.  
Saturday:  
• Limited volumes.  
• No files transmitted. 
Sunday:  
• Limited volumes.  
• Files transmitted based on 
customer subscription.  
 
Please see the holiday processing schedule for exceptions to the weekday schedule. 
  

---

## Page 57

Message Flows and Timing 
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 57 
Holiday Processing Schedule 
MESSAGES/ 
HOLIDAYS 
U.S. AND 
CANADIAN 
HOLIDAYS  
(BOTH [[DTC]] AND 
CANADA CLOSED) 
U.S. HOLIDAYS 
([[DTC]] CLOSED, 
CANADA OPEN) 
U.S. HOLIDAYS 
([[DTC]] OPEN, 
CANADA OPEN, 
U.S. BANKS 
CLOSED) 
CANADIAN 
HOLIDAYS 
([[DTC]] OPEN,  
CANADA CLOSED) 
CANO 
Limited volumes.  
Files transmitted 
based on customer 
subscription.  
Limited volumes.  
Files transmitted 
based on customer 
subscription.  
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
CANO-E 
No messages.  No messages or files 
transmitted. 
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
CAPA 
No messages.  Normal volumes.  
Files transmitted 
based on customer 
subscription.  
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
CACO 
No messages.  Only for Canadian 
payments.  
[[Stock]] allocation only 
(no cash allocation).  
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
CAPS 
No messages.  1:00 p.m., 2:00 p.m., 
and 3:00 p.m. 
eastern time for P&I 
and foreign 
payments.  
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
CAST 
No messages.  No messages or files 
trans mitted. 
Not sent for rights 
subscriptions (59) or 
warrant exercises 
(60). 
Normal volumes / 
transmission for all 
other event types.  
Normal volumes.  
Files transmitted 
based on customer 
subscription.  
For these 
holidays:  
• New Year's Day 
• Labor Day  
• Christmas Day  
• Dr. Martin Luther 
King, Jr. Day  
• Presidents' Day  
• Memorial Day  
• Independence 
Day  
• Thanksgiving Day  
• Columbus Day  
• Veterans’ Day  
• Good Friday (All)  
• Victoria Day  
• Canada Day  
• CDN 
Thanksgiving Day  
• Boxing Day  
 

---

## Page 58

Account Balances  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 58 
Account Balances  
The ISO 20022 messages contain several balance types to explain your position as it is affected by a 
corporate action reorganization event. 
TERM DEFINITION 
[[collateral]] Out Balance 
This is your pledged position that is not eligible for payment. It is the 
portion of the original b alance posit ion held in a [[DTC]] Pledged account.  
For non- debt [[securities]], this refers to units. For debt [[securities]], this 
refers to the face amount.  
Confirmed Balance This balance only relates to CACO messages. It  is the balance on 
which the payment is occurring.  
Instructed Balance 
For CANO-E and CAPA messages , the Instructed balance is the sum 
of event -level instructed balances across all options. For CAST 
messages, this  can be at either the event level or the [[Option]] level . 
Investment Pledged Balance The total quantity of [[securities]] segregated from the General Free 
account of a firm, partner, officer, stockholder, or an omnibus account.  
Investment Unpledged Balance The p osition held that rep resents the total quantity of [[securities]] 
segregated from the Regular Unpledged account  (Account 10) .  
Memo Segregation Balance 
The position held in a [[DTC]] segregated account. It is the c ounter used 
to protect customer fully paid for [[securities]] from being d elivered out of 
a [[participant]] account.  
Obligated Balance An obligated balance is displayed when you have a negative balance 
(“short”) in your Regular Unpledged account  (Account 10).  
[[Option]] Daily Instructed 
Balance 
This appears only on the CAST message. It is t he d aily total of 
instructions for a given [[Option]]  for the current day . This balance 
include s only “made” instructions.   
[[Option]] Unaccepted Balance 
This appears only on the CACO message. For election merger events, 
this is the balance that is being moved into another [[Option]] number for 
payment due to the proration of the original [[Option]].  
[[Option]] Uncovered Protect 
Balance 
This appears only on the CAST message, It is t he balance of 
uncovered protect transactions at an [[Option]] level . 

---

## Page 59

Account Balances  
ISO 20022 Messaging for Reorganiz ations: Entitlem ents and All ocati ons 59 
TERM DEFINITION 
[[settlement]] Position Balance 
This is your position in these accounts:  
• 10: Regular Unpledged account.  
• 11: Regular Paid account.  
• 14: Regular Pledged account.  
• 18: Investment Regular Pledged account.  
• 22: Investment Regular Unpledged account.  
“Settled position” is not the same as “eligible position” for voluntary 
events. The 14, 18, and 22 are restricted accounts and will not result in 
[[Entitlement]] unless the position is moved into your Regular Unpledged 
account (10).  
Total Eligible Balance 
For voluntary events, this is t he total eligible balance upon which you 
can instruct. It is the position in your Regular Pledged and Regular 
Paid accounts (10 and 11).  
For mandatory events, this is the position in any or all of these 
accounts:  
• 10: Regular Unpledged account.  
• 11: Regular Paid account.  
• 14: Regular Pledged account.  
• 18: Investment Regular Pledged account.  
• 22: Investment Regular Unpledged account.  Total Instructed Balance 
Provides information about the total instructed balance for the event. 
This is either the sum of the instructions for the event or the position in 
the contra [[CUSIP]] for the event.  
For most reorganization events, this is a cumulative total.  
For long- lived events (53 {CD early redemption} , 54 {conversion} , 60 
{warrant} , 66P {MMI survivor options} ), this is not cumulative. It is 
based solely on the instructions for that day (i.e., the day the message 
is generated).  
This balance is r epeated for each [[Option]] in the: 
[[Option]] Balance Details  
[[Option]] Instruction Details  
[[Option]] Protect Instruction Details  
Total Uncovered Protect 
Balance 
On the CAST, this is the event-level uncovered protect balance. It is 
the sum of all of the [[Option]]- level balances. 
Uncovered Protect Balance On the CANO-E and CAPA messages, this is an event -level 
uncovered protect balance.  
Uninstructed Balance For voluntary events, this is the position eligible for instruction.  

---

## Page 60

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 60 
CORPORATE ACTION NOTIFICATION WITH ELIGIBLE 
BALANCE (CANO-E) MESSAGES 
What is a CANO-E Message? 
The Corporate Action Notification with Eligible Balance (CANO-E) message captures a customer’s [[DTC]] 
eligible position on a particular date for a reorganization event (announced in the original CANO). This 
message provides information about your eligible, instructed, and uninstructed balance(s).  
After the initial message is sent, replacement messages are sent for a predetermined period of time 
(based on the event type), generally leading up to a payment date.  
The identifying information for a CANO-E message is: 
MX IDENTIFIER ISO 20022  
MESSAGE 
NAMES 
EXTENSION SHORT NAME EQUIVALENT 
ISO 15022 
EQUIVALENT 
[[DTCC]] 
PROCESSES 
seev.031.002.xx 1 CA Notification 
with Eligible 
Balance 
supl.007.001.xx  CANO-E MT 564 Eligible 
Balances  
 
The purpose of this message is to provide clients with balance information, including eligible balances. 
Certain balances in the CANO-E will be marked as “eligible” or “not eligible” based on whether the event 
is mandatory or voluntary. 
Many event details can be traced back to the CANO message through the Corporate Action Event [[ID]]. By 
using this identifier, the body of the CANO message is not repeated in the CANO-E. 
Important information in the CANO-E main message includes: 
• Corporate Action Event [[ID]], 
• Event Type, 
• Mandatory/Voluntary Indicator, 
• Eligible Balance, 
• Instructed Balance,  
• Uninstructed Balance, and 
 
1 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version 
number may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 61

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 61 
• [[Option]]-Level Information (including Response Deadline Date and Expiry Date). 
Additional information specific to the reorg event type is provided in the message extension (also called 
“SD,” or supplemental data). This may include: 
• Sub Event Type, 
• Memo Segregation Balance, and 
• Investment Pledged /Unpledged Balance. 
Balance Eligibility 
Eligibility is based on either [[Entitlement]] for mandatory events or instructions for voluntary events.  
ISO TAG  MANDATORY 
ELIGIBLE / INELIGIBLE 
VOLUNTARY 
ELIGIBLE / INELIGIBLE 
Total Eligible Balance  (10, 11, 14, 18, 22)  (10, 11) 
[[collateral]] Out Balance Eligible Balance  Not Eligible Balance  
Investment Pledged Balance Eligible Balance  Not Eligible Balance  
Investment Unpledged Balance  Eligible Balance  Not Eligible Balance  
Affected Balance Not Eligible Balance  Not Eligible Balance  
Out For Registration Balance Not Eligible Balance  Not Eligible Balance  
Memo Segregation Balance Not Eligible Balance  Not Eligible Balance  
The [[DTC]] accounts that relate to these balances are: 
• 10: Regular Unpledged account. 
• 11: Regular Paid account. 
• 14: Regular Pledged account. 
• 18: Investment Regular Pledged account. 
• 22: Investment Regular Unpledged account. 
• 26: Call with Interest account. 
• 28: Call No Interest account. 
• 40: Withdrawal by Transfer account. 
• Position Memo Segregation account. 
 
  

---

## Page 62

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 62 
Reorganization Events Using CANO-E Messages 
Reorg Events Using 
CANO-Es  
This document shows the mapping for CANO-E messages per ISO event type 
code, sub event type, and extended sub event type. It links these SWIFT codes 
to their relevant legacy activity codes. 
 
When Are CANO-E Messages Generated? 
In general, generation of the CANO-E is triggered by the presence of a balance in any of your accounts. If 
you have position at all in the event [[CUSIP]], you will receive a CANO-E message. 
After [[DTCC]] determines that you have an associated balance, a check is then made as to your eligible 
balance. This balance eligibility differs based on whether this is a mandatory or voluntary event. 
For example, your affected balance and your withdrawal by transfer balances [[DO]] not determine eligibility, 
but the presence of either of these balances will still trigger a CANO-E message. 
The NEWM generation date and REPL message period for the CANO-E varies according to event type. 
The following subsections list the eligible balances and provide tables explaining the message periods for 
mandatory and voluntary events. 
Mandatory Events 
CANO-E Messaging Period for Mandatory Events 
The eligible balance for mandatory events is determined by the following: 
• For Partial Mandatory Puts, you have position in the contra [[CUSIP]] regular unpledged (“free”) 
account. 
• For all other mandatory events, you have position in the event [[CUSIP]] in one of the following 
accounts: 
o 10: Regular Unpledged account. 
o 11: Regular Paid account. 
o 14: Regular Pledged account. 
o 18: Investment Regular Pledged account. 
o 22: Investment Regular Unpledged account. 
o 26: Call with Interest account. 
o 28: Call No Interest account. 
o 40: Withdrawal by Transfer account. 
o Position Memo Segregation account.  

---

## Page 63

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 63 
The final column in the following table specifies the balance that triggers each event type. 
See the Reorg Events Using CANO-Es mapping document for full event type information. 
ACTIVITY 
CODE 
CA WEB 
EVENT TYPE 
CAEV CODE / 
SUB EVENT TYPE 
CANO-E MESSAGE 
START / END DATE  
MESSAGE 
TRIGGER 
61 
Redemptions 
of [[Warrants]]  
REDM BEGINS: Payment Date – 7 
ENDS: Payment Date 
Event 
Security 
balance 
65 
Mandatory Put 
(No Retain)  
BPUT BEGINS: Payment Date – 7 
ENDS: Payment Date 
Event 
Security 
balance 
65G 
Mandatory Put 
(Book Entry)  
BPUT BEGINS: Payment Date – 7  
ENDS: Payment Date 
Event 
Security 
balance 
65P 
Partial 
Mandatory Put 
BPUT BEGINS: Payment Date – 7  
ENDS: Payment Date 
Contra 
[[CUSIP]] 
balance 
69 
Full Call MCAL BEGINS: Payment Date – 7 
ENDS: Payment Date 
Event 
Security 
balance 
71 
Merger 
([[securities]])  
MRGR / SECU BEGINS: Payment Date ([[DTC]] Anticipated 
Payment Date) – 1 
ENDS:  Payment Date ([[DTC]] Anticipated 
Payment Date)  
Event 
Security 
balance 
72 
Merger (Cash)  MRGR / CASH BEGINS: Payment Date ([[DTC]] Anticipated 
Payment Date) – 1 
ENDS: Payment Date([[DTC]] Anticipated 
Payment Date)  
Event 
Security 
balance 
73 
Reverse [[Stock]] 
Split  
SPLR BEGINS: Payment Date ([[DTC]] Anticipated 
Payment Date) – 1 
ENDS: Payment Date ([[DTC]] Anticipated 
Payment Date)  
Event 
Security 
balance 
79 
[[liquidation]] 
(Presentation 
Required)  
LIQU / PREQ BEGINS: Payment Date ([[DTC]] Anticipated 
Payment Date) – 1 
ENDS: Payment Date ([[DTC]] Anticipated 
Payment Date)  
Event 
Security 
balance 
90 
Merger (Cash 
and 
[[securities]])  
MRGR / CASE BEGINS: Payment Date ([[DTC]] Anticipated 
Payment Date) – 1 
ENDS: Payment Date ([[DTC]] Anticipated 
Payment Date)  
Event 
Security 
balance 

---

## Page 64

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 64 
93 
Various  • PLAC 
• CHAN 
• CHAN / PREQ 
• CONV 
• EXOF 
• EXOF / ADRS 
(TMTN) 
• EXOF / ADRS 
(TMTN) 
• EXRI 
• LIQU / PREQ 
• MRGR 
• OTHR 
• REDM / SECU 
• SPLF / PREQ 
• SPLR 
• WRTH 
BEGINS: Payment Date ([[DTC]] Anticipated 
Payment Date) – 1 
ENDS: Payment Date ([[DTC]] Anticipated 
Payment Date)  
Event 
Security 
balance 
CANO-E Daily Messaging Times for Mandatory Events 
Messages for mandatory events are sent daily at 8:00 p.m. during the range specified above. 
Voluntary Events 
CANO-E Messaging Period for Voluntary Events 
For voluntary events, the messaging period is the widest relevant period for the individual reorganization 
event type and could include early response deadlines and cover protect periods. The CANO-E message 
is sent during this period when you have any position (eligible or non-eligible) in this event.  
ACTIVITY 
CODE 
CA WEB 
EVENT TYPE 
CAEV CODE / 
SUB EVENT TYPE 
CANO-E MESSAGE 
START / END DATE  
MESSAGE 
TRIGGER 
52 
Various  • BIDS 
• BIDS / BTST 
• BIDS / CASE 
• BIDS / COTE 
• BIDS / SETE 
• BPUT 
• CONS / WITH 
• CONS / WITO  
BEGINS earliest of: 
Early Response Deadline – 7 
 or 
Action Period Start Date – 7 
ENDS latest of: 
Expiry Date  
 or 
Cover Expiration Date  
Event 
Security 
balance 

---

## Page 65

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 65 
ACTIVITY 
CODE 
CA WEB 
EVENT TYPE 
CAEV CODE / 
SUB EVENT TYPE 
CANO-E MESSAGE 
START / END DATE  
MESSAGE 
TRIGGER 
• CONV 
• DTCH 
• EXOF 
• EXOF / A114 
• EXOF / CASE 
• EXOF / REGS 
• EXWA 
• NOOF / MITE 
• ODLT 
• OTHR 
• TEND / BTST  
• TEND / CASE 
• TEND / CILI 
• TEND / COTE 
• TEND / FTPR 
52N 
Various  
(NON-[[DTC]]) 
• BIDS 
• BIDS / BTST 
• BIDS / CASE 
• BIDS / SETE 
• DTCH 
• EXOF 
• EXOF / A114 
• EXOF / ADRS 
(TMTN) 
• EXOF / CASE 
• EXOF / GDRS 
(TMTN) 
• EXOF / REGS 
• EXOF (TMTN)  
• NOOF / MITE 
• ODLT 
• OTHR 
• TEND / BTST 
• TEND / CASE 
• TEND / FTPR 
BEGINS earliest of: 
Actual Early Expiration Date –  7 
 or 
Expiry Date – 7 
ENDS latest of: 
Expiry Date  
 or 
Cover Expiration Date 
Event 
Security 
balance 
52M 
Merger  MRGR BEGINS earliest of: 
Early Response Deadline –  7 
 or 
Event 
Security 
balance 

---

## Page 66

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 66 
ACTIVITY 
CODE 
CA WEB 
EVENT TYPE 
CAEV CODE / 
SUB EVENT TYPE 
CANO-E MESSAGE 
START / END DATE  
MESSAGE 
TRIGGER 
Action Period Start Date – 7  
 
ENDS latest of: 
Expiry Date  
 or 
Cover Expiration Date 
54 
Conversion  CONV BEGINS: Response Deadline Date – 7 
ENDS: Expiry Date 
Event 
Security 
balance 
54N 
Conversion  
(Non- [[DTC]]) 
Security 
Separation  
(Non -[[DTC]]) 
CONV 
 
DETI 
BEGINS: Expiry Date – 7 
ENDS: Expiry Date 
Event 
Security 
balance 
54T 
Tender Offer 
(Convert and 
Tender)  
• BIDS / COTE 
• TEND / COTE 
BEGINS earliest of: 
Early Response Deadline –  7 
 or 
Action Period Start Date – 7 
 
ENDS latest of: 
Expiry Date  
 or 
Cover Expiration Date 
Event 
Security 
balance 
58 
Put 
General 
Information  
BPUT 
OTHR 
BEGINS: VOI Entry  Start Date 
Send REPL message if instruction activity.  
If not, send from Response Deadline Date – 
3 
 
ENDS: Response Deadline Date 
Event 
Security 
balance 
58B 
Put BPUT BEGINS: VOI Entry Start Date 
Send REPL message if instruction activity.  
If not, send from Response Deadline Date – 
3 
 
ENDS: Response Deadline Date 
Event 
Security 
balance 
58N 
Put  
(Non -[[DTC]]) 
BPUT BEGINS: Expiry Date – 7 
ENDS: Expiry Date 
Event 
Security 
balance 
59 
Rights 
Subscription  
EXRI BEGINS: Response Deadline Date – 7 
ENDS latest of: 
Expiry Date 
 or 
Cover Expiration Date  
Event 
Security 
balance 

---

## Page 67

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 67 
ACTIVITY 
CODE 
CA WEB 
EVENT TYPE 
CAEV CODE / 
SUB EVENT TYPE 
CANO-E MESSAGE 
START / END DATE  
MESSAGE 
TRIGGER 
60 
Warrant 
Exercise  
EXWA BEGINS: Response Deadline Date – 7 
ENDS: Expiry Date 
Event 
Security 
balance 
60N 
Warrant 
Exercise 
(Non -[[DTC]]) 
EXWA BEGINS: Expiry Date – 7 
ENDS: Expiry Date 
Event 
Security 
balance 65B 
Mandatory Put 
(Retain Book 
Entry)  
BPUT FIRST RANGE BEGINS: 
VOI Entry Start Date –  7 
FIRST RANGE ENDS: 
Response Deadline Date 
 
SECOND RANGE 
BEGINS earliest of: 
Payment Date – 7 
(if greater than 5 business day difference 
between Response Deadline Date and 
Payment Date)  
SECOND RANGE ENDS : Payment Date 
Event 
Security 
balance 
65R 
Mandatory Put 
(Retain)  
BPUT FIRST RANGE BEGINS: 
VOI Entry Start Date –  7 
FIRST RANGE ENDS: 
Response Deadline Date 
 
SECOND RANGE 
BEGINS earliest of:  
Payment Date – 7 
(if greater than 5 business day difference 
between Response Deadline Date and 
Payment Date)  
SECOND RANGE ENDS : Payment Date 
Event 
Security 
balance 
 
  

---

## Page 68

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 68 
CANO-E Daily Messaging Times for Voluntary Events 
CANO-E replacement messages are sent daily throughout the time range specified above.  
Intraday messages are also generated as the expiration date approaches: 
MESSAGE BEGIN 
DATE 
   8:00 p.m. 
THROUGH… 
Msg End Date – 4    8:00 p.m. 
Msg End Date –3   5:00 p.m. 8:00 p.m. 
Msg End Date – 2   5:00 p.m. 8:00 p.m. 
Msg End Date – 1   5:00 p.m. 8:00 p.m. 
Message End Date 12:00 p.m. 1:30 p.m. 4:00 p.m. 4:30 p.m. 
 
Events Out of Scope 
These event types will not generate a CANO-E message. 
See the Reorganization Event Codes mapping document for full event type information. 
ACTIVITY 
CODE CA WEB EVENT TYPE CAEV CODE / SUB EVENT TYPE 
51 Exchange Offer / Unwind  UNWD 
53 CD Early Redemption CDRD 
62 Put  
(Mortgage Backed)  BPUT / MBCK 
62B Put  
(Mortgage Backed)  BPUT / MBCK 
66P Put (Survivor Options)  BPUT / SOBT 
91 Name Change CHAN 
94 Plan of Reorganization 
([[vote]]) BRUP 
96 General Information 
(Important Notice)  OTHR / NOTI 
 
  

---

## Page 69

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 69 
CANO-E Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times 
specified above. Messages are not sent on Saturday or Sunday. Exceptions are noted in the holiday 
processing schedule. 
 
CANO-E Holiday Processing Schedule 
In addition to the timing specifications above, CANO-E message generation also conforms to the 
following holiday schedule: 
U.S. AND CANADIAN 
HOLIDAYS  
(BOTH [[DTC]] AND 
CANADA CLOSED) 
U.S. HOLIDAYS 
([[DTC]] CLOSED,  
CANADA OPEN) 
U.S. HOLIDAYS 
([[DTC]] OPEN,  
CANADA OPEN) 
CANADIAN HOLIDAYS 
([[DTC]] OPEN,  
CANADA CLOSED) 
No messages  or files are 
sent on:  
• New Year's Day 
• Labor Day  
• Christmas Day.  
No messages or files are 
sent on:  
• Dr. Martin Luther 
King, Jr. Day  
• Presidents' Day  
• Memorial Day  
• Independence Day  
• Thanksgiving Day  
For these days, U.S. 
banks are closed but 
[[DTC]] is open:  
• Columbus Day  
• Veterans’ Day  
Files are transmitted 
based on customer 
subscription.  
Normal volumes occur 
on these days:  
• Good Friday ( All) 
• Victoria Day  
• Canada Day  
• CDN Thanksgiving 
Day 
• Boxing Day  
Files are transmitted 
based on customer 
subscription.  
 
CANO-E Message Subscriptions 
There is a single subscription for reorganization events. CANO-E messages are sent via file and in real 
time at 12:00 p.m., 1:30 p.m., 4:00 p.m., 4:30 p.m., 5:00 p.m., and 8:00 p.m. as specified above. 
  

---

## Page 70

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 70 
Information Contained on the CANO-E Message 
The following table contains some of the important elements in the CANO-E message. 
For more detailed technical information about message contents and elements, please see the Data 
Dictionary and/or My Standards for this message. 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Notification Type  • “NEWM” for new messages . 
• “REPL” for replacement messages . 
Event Processing Type Always set to “REOG.”  
CA [[ID]] Corporate Actions Identifier. This is [[DTC]]’s unique identifier for the 
corporate action event.  
Official Corporate Actions 
Event [[ID]] 
Official Corporate Actions Identifier. This is the official, unique identifier for 
the corporate action. It is made up of th e CA [[ID]] preceded by “US.” In order 
for this instruction to be accepted and processed, the COAF on the 
instruction must match the COAF on the announcement messages.  
Event Type 
The “CAEV” refers to the event type.  
See the Reorganization Event Codes table for a list of possible codes.  
Event Security Includes security description and [[CUSIP]] code.  
Mandatory/Voluntary 
Indicator 
Indicates whether the event is mandatory (MAND), voluntary (VOLU), or 
mandatory with options (CHOS).  
Balance Information  
Several fields provide balance information according to the event type:  
• Safekeeping Account . Your client [[ID]]. 
• Instructed Balance. Your balance in the event for which 
instructions have already been made. This includes cover protects. 
• Uninstructed Balance. Your balance in the event for which no 
instructions have been made. For voluntary events, this is the 
position eligible for instruction.  
• Eligible Balance. For voluntary or choice events, this is t he balance 
upon which you ca n instruct. For mandatory events, this is  the 
balance relating to your [[Entitlement]].  
• [[collateral]] Out Balance. The portion of the original balance position 
held in a [[DTC]] pledged account and deposited with a third party for 
the purpose of collateralization . 
Note that not every balance will apply to every event type.  
 
  

---

## Page 71

CANO-E Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 71 
The extension for the CANO-E message varies based on the individual event and sub event type. Some 
of the following information may be included, depending on the event type represented by the message: 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Sub Event Information  
Codes that represent the extended sub event type for this particular 
corporate action event. See the Reorganization Event Codes table for a 
list of these codes and associated information.  
Balance Information  
• Unpledged Balance. T he total number of [[shares]] you have pledged 
to any number of pledgee banks for this security. Individual pledge 
records record the security, number of [[shares]], [[participant]], pledgee 
bank, and loan date.  
• Investment Pledged Balance. The total quantity o f [[securities]] 
segregated from the General Free account of a firm, partner, officer, 
stockholder, or an omnibus account.  
• Investment Unpledged Balance. Position held that represents the 
total quantity of [[securities]] segregated from the General Free 
account.  
• Memo Segregation Balance.  The counter used to protect customer 
fully paid for [[securities]] from being delivered out of a [[participant]] 
account.  
• Uncovered Protect Balance. The balance of all uncovered protect 
instructions across all options.  

---

## Page 72

CAPA Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 72 
CORPORATE ACTION MOVEMENT PRELIMINARY 
ADVICE (CAPA) MESSAGES 
What is a CAPA Message? 
The CAPA message provides pre-advice of payment for [[securities]] or cash payments relating to 
reorganization events. For voluntary events, the CAPA also projects entitlements at an instruction-based 
level. 
The body of the CAPA message provides balances and the associated projected cash and/or [[securities]] 
movements at an [[Option]] level. The message extension displays details at the instruction level that break 
down the [[Entitlement]] for each VOI instruction. Additionally, the extension provides information regarding 
reorg or [[custody]] deposits. 
The CAPA message is only applicable to put events, warrant redemptions, full call conversions, and 
maturity conversion events. Since other reorganization events project and allocate on the same day, they 
will not produce a CAPA message. 
In the case of mortgage-backed puts and puts with survivor options, you will receive a CAPA message 
without receiving a CANO-E. 
The identifying information for a CAPA message is: 
MX IDENTIFIER ISO 20022  
MESSAGE 
NAMES 
EXTENSION SHORT NAME EQUIVALENT 
ISO 15022 
EQUIVALENT 
[[DTCC]] 
PROCESSES 
seev.035.002.xx 2 CA Movement 
Preliminary 
Advice  
supl.009.001.xx  CAPA MT 564 Projected 
Payments 
  
 
2 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version 
number may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 73

CAPA Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 73 
Reorganization Events Using CAPA Messages 
Reorg Events Using 
CAPAs  
This document shows the mapping for CAPA messages per ISO event type 
code, sub event type, and extended sub event type. It links these SWIFT codes 
to their relevant legacy activity codes. 
 
Events Not Generating a CAPA 
Of the reorganization events that are handled by ISO 20022 messaging, these event types will not 
generate a CAPA message. See the Reorganization Event Codes mapping document for full event type 
information. 
ACTIVITY 
CODE 
CA WEB EVENT TYPE CAEV CODE / SUB EVENT TYPE 
52 Various  
• BIDS 
• BIDS / BTST 
• BIDS / CASE 
• BIDS / COTE 
• BIDS / SETE 
• BPUT 
• CONS / WITH  
• CONS / WITO  
• CONV 
• DTCH 
• EXOF 
• EXOF / A114 
• EXOF / CASE 
• EXOF / REGS 
• EXWA 
• NOOF / MITE 
• ODLT 
• OTHR 
• TEND / BTST  
• TEND / CASE 
• TEND / CILI 
• TEND / COTE 
• TEND / FTPR 
52M Merger (Voluntary)  MRGR 
52N Various (Non -[[DTC]]) 
• BIDS 
• BIDS / BTST 
• BIDS / CASE 
• BIDS / SETE 
• DTCH 
• EXOF 
• EXOF / A114 
• EXOF / ADRS (TMTN)  
• EXOF / CASE 
• EXOF / GDRS (TMTN)  
• EXOF / REGS 
• EXOF (TMTN)  
• NOOF / MITE 
• ODLT 
• OTHR 
• TEND / BTST 
• TEND / CASE 
• TEND / FTPR 
53 CD Early Redemption  CDRD 

---

## Page 74

CAPA Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 74 
54 Conversion  CONV 
54N 
Conversion  
(Non -[[DTC]]) 
Security Separation  
(Non -[[DTC]]) 
CONV 
 
DETI 
54T Tender Offer  
(Convert and Tender)  
• BIDS / COTE 
• TEND / COTE 
58N Put 
(Non -[[DTC]]) 
BPUT 
59 Rights Subscription  EXRI 
60 Warrant Exercise EXWA 
60N Warrant Exercise 
(Non -[[DTC]]) 
EXWA 
 
When Are CAPA Messages Generated? 
CAPA Message Triggers and Periods 
The notification types for preliminary advice messages include NEWM (new messages) and REPL 
(replacement messages).  
Rules for CAPA message generation are outlined in the table below. It specifies the key dates for each 
CAPA’s message period.  
The table below also specifies which balance (per event type) will trigger a CAPA when position is 
captured. CAPA messages are sent when the position captured contains a particular balance that is 
greater than zero.  
ACTIVITY 
CODE 
CA WEB 
EVENT TYPE 
CAEV CODE / 
SUB EVENT 
TYPE 
CAPA MESSAGE KEY DATES:  
NEW / REPLACEMENT SENT  MESSAGE TRIGGER  
58 
Optional Put  BPUT 
OTHR 
NEWM: Payment Date – 7  
REPL: Payment Date – 1 
Contra [[CUSIP]] balance 
58B 
Optional Put 
(Book Entry)  
BPUT NEWM: Payment Date – 7  
REPL: Payment Date – 1 
Contra [[CUSIP]] balance 
61 
Redemptions of 
[[Warrants]]  
REDM NEWM: Anticipated Payment Date – 7  
REPL: Payment Date – 1 
Event security balance 

---

## Page 75

CAPA Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 75 
ACTIVITY 
CODE 
CA WEB 
EVENT TYPE 
CAEV CODE / 
SUB EVENT 
TYPE 
CAPA MESSAGE KEY DATES:  
NEW / REPLACEMENT SENT  MESSAGE TRIGGER  
62 
Put  
(Mortgage 
Backed)  
BPUT / MBCK NEWM: Payment Date – 7  
Note: Item must be selected 
for payment via APUT 
REPL: Payment Date – 1 
Contra [[CUSIP]] balance 
62B 
Put  
(Mortgage 
Backed, Book 
Entry)  
BPUT / MBCK NEWM: Payment Date – 7  
Note: Item must be selected 
for payment via APUT 
REPL: Payment Date – 1 
Contra [[CUSIP]] balance 
65 
Mandatory Put 
(No Retain) 
BPUT NEWM: Payment Date – 7  
REPL: Payment Date – 1 
Event security balance 
65B 
Mandatory Put 
(Retain  Book 
Entry)  
BPUT NEWM: Payment Date – 7  
REPL: Payment Date – 1 
Contra [[CUSIP]] balance  
or 
Event security 
uninstructed balance 
(CASH) 
65G 
Mandatory Put 
(Book Entry)  
BPUT NEWM: Payment Date – 7  
REPL: Payment Date – 1 
Event security balance 
65P 
Partial 
Mandatory Put 
BPUT NEWM: Payment Date – 7  
REPL: Payment Date – 1 
Event security balance 
for positions held 
under Contra [[CUSIP]] 
65R 
Mandatory Put 
(Retain)  
Partial 
Mandatory Put 
(Retain)  
BPUT 
 
BPUT 
NEWM: Payment Date – 7  
REPL: Payment Date – 1 
Contra position in 
SECU [[Option]] 
Event security 
uninstructed balance 
in CASH [[Option]]  
66P 
Put 
(Survivor 
Options ) 
BPUT / SOPT NEWM: Payment Date – 7  
Note: Item must be selected 
for payment via APUT 
REPL: Payment Date – 1 
RRG (segregated) 
balance 
69 
Full Call 
Maturity 
(Conversion)  
MCAL 
REDM 
NEWM: Anticipated Payment Date – 7  
REPL: Anticipated Payment Date – 1 
Event security balance 
  

---

## Page 76

CAPA Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 76 
Additional Rules for CAPA Generation 
• CAPA NEWM messages begin generating on the applicable key date – 7. If the rate is not available, 
the projected cash [[Entitlement]] will be marked as unknown (“UKWN”). 
• Between the key date – 7 and key date – 1, CAPA REPL messages are sent when a rate has been 
received for an event for which the rate was previously unknown. 
• If an event is generated fewer than 7 days prior to the key date, the CAPA message is generated on 
the first night it is available. After that point, it will follow the regular CAPA message flow until key date 
– 1. 
• If there is a change to the [[Entitlement]], a replacement (REPL) message will be generated for the 
[[participant]] for the event. 
• For applicable events, a CAPA message will automatically be generated on key date – 1 regardless 
of the subscription [[Option]]. 
• No CAPA message will be sent on applicable events if the event is created on or after key date and 
allocation occurs the same day. 
• Choice events (65R and 65B) generate two CAPA messages: one for each [[Option]] type (Retain/Cash 
or [[securities]]). Eligible balance for the “Retain” [[Option]] is based on your instructed position. Eligibility 
for the CASH or SECU [[Option]] ([[default]]) will be based on the uninstructed position. 
CAPA Message Subscriptions 
There are two types of CAPA subscriptions for all event types: 
• Key Date – 7 and Key Date – 1 only, 
or 
• Key Date – 7 and Key Date – 1 plus any interim activity. 
Note:  “Key Date” refers to the date specified in the above table.  
CAPA Daily Messaging Times  
Messages are available both real time and via file at 1:30 a.m. 
CAPA Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times 
specified above. Messages are not sent on Saturday or Sunday. Exceptions are noted in the holiday 
processing schedule. 
  

---

## Page 77

CAPA Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 77 
CAPA Holiday Processing Schedule 
In addition to the timing specifications above, CAPA message generation also conforms to the following 
holiday schedule: 
U.S. AND CANADIAN 
HOLIDAYS  
(BOTH [[DTC]] AND 
CANADA CLOSED) 
U.S. HOLIDAYS 
([[DTC]] CLOSED,  
CANADA OPEN) 
U.S. HOLIDAYS 
([[DTC]] OPEN,  
CANADA OPEN) 
CANADIAN HOLIDAYS 
([[DTC]] OPEN,  
CANADA CLOSED) 
No messages or files are 
sent on:  
• New Year's Day 
• Labor Day  
• Christmas Day  
Normal volumes occur on 
these days:  
• Dr. Martin Luther 
King, Jr. Day  
• Presidents' Day  
• Memorial Day  
• Independence Day  
• Thanksgiving Day  
 
For these days, U.S. 
banks are closed but 
[[DTC]] is open:  
• Columbus Day  
• Veterans’ Day  
Files are transmitted 
based on customer 
subscription.  
Normal volumes occur on 
these days:  
• Good Friday ( All) 
• Victoria Day  
• Canada Day  
• CDN Thanksgiving 
Day 
• Boxing Day  
Files are transmitted 
based on customer 
subscription.  
Information Contained on the CAPA Message 
CAPA Obligated Balance 
The CAPA will display an “Obligated Balance” when you have a negative balance (“short”) in your 
Regular Unpledged account (Account 10). 
CAPA Instructed / Uninstructed Balance 
For voluntary (VOLU) or choice (CHOS) events, the instructed and uninstructed balances are based on 
the instructions received and processed through [[PTS]]/[[PBS]] legacy systems. 
  

---

## Page 78

CAPA Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 78 
CAPA Message Body 
The following table contains some of the important elements in the CAPA message. 
For more detailed technical information about message contents and elements, please see the Data 
Dictionary and/or My Standards for this message. 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Notification Type  • “NEWM” for new messages . 
• “REPL” for replacement messages . 
Event Type The four -letter code that defines the event type. See the Reorganization 
Event Codes table for a list of possible codes.  
Corporate Action Event 
Identification (CA [[ID]])  
Corporate Actions Identifier. This is [[DTC]]’s unique identifier for the 
corporate action event.  
Official Corporate Actions 
Event [[ID]] 
Official Corporate Actions Identifier. This is the official, unique identifier for 
the corporate action. It is made up of th e CA [[ID]] preceded by “US.” In order 
for this instruction to be accepted and processed, the COAF on the 
instruction must match the COAF on the announcement messages.  
Underlying Security The security affected by the corporate action. Includes security descri ption 
and [[CUSIP]] code . 
Mandatory/Voluntary 
Indicator 
Indicates whether the event is mandatory (MAND), voluntary (VOLU), or 
mandatory with options (CHOS).  
Balance Information  
Several fields provide balance information according to the event type:  
• Safekeeping Account . Your client [[ID]]. 
• Total Eligible Balance. For voluntary or choice events, this is t he 
balance upon which you can instruct.  For mandatory events, this is 
the balance relating to your [[Entitlement]].  
• [[settlement]] Position Balance. Your  current eligible balance (for 
elections, allocations, etc.) . 
Note that not every balance will apply to every event type.  
Security Movement Details 
For events in which a payment is being made, these are details about the 
upcoming movement of [[securities]]. These details may include:  
• Security Identification . A description of the financial instrument 
related to [[securities]] movement.  
• Entitled Quantity . The quantity of [[securities]] to be debited from your 
account.  
• Payment Date. The [[issuer]] -announced date on which the [[securities]] 
will be paid.  

---

## Page 79

CAPA Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 79 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Cash Movement Details 
For events in which a cash allocation is being made, these are details 
about the upcoming payment. These details may include:  
• Payment Date. The [[issuer]] -announced date on which the cash  will 
be paid.  
• Entitled Amount. The projected cash amount based on the terms 
of the corporate action event . 
• [[DTC]] Cash Rate . The [[DTC]] rate used for calculating the cash 
[[Entitlement]] on the reorganization event . 
CAPA Message Extension 
The extension for the CAPA message varies based on the individual event and sub event type, as well as 
the [[Option]] and instruction information it represents.  
The [[Option]] transaction details section provides each instruction that adds up to the projected allocation. 
An individual instruction is presented in an information block that is distinguished by its Transaction [[ID]] 
(VOI number). The CAPA extension contains as many repeating blocks of information as there are 
instructions. 
The ability to view all instructions gathered in a single report allows for greater instruction-level 
transparency into everything that comprises your total allocation. 
Some of the following information may be included, depending on the event type represented by the 
message: 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
RDP Reference Number  Unique [[DTCC]] legacy reference used for matching and reconciling legacy 
[[CCF]] records. It indicates  how values are sourced from [[CCF]] legacy files.  
Sub Event Type  
Codes that represent the extended sub event type for this particular 
corporate action event. See the Reorganization Event Codes table for a 
list of these codes and associated information.  
Payout Type  The type of payout associated with the event (e.g., principal, cash, 
[[securities]], interest, [[Dividend]]).  

---

## Page 80

CAPA Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 80 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
[[Option]] Transaction Details  
(repeating block)  
Each block of information represents a single instruction. This block is 
repeated per individual instruction.  
• Transaction [[ID]] . Unique number assigned by [[DTC]] (VOI). This is the 
identifier for each individual instruction.  
• Transaction [[ID]] Quantity . Resulting quantity of cash or security 
involved in this transaction (as a result of this instruction).  
For reorganizati on and [[custody]] reorganization deposits, this is the 
deposit quantity. For reorganization instructions, this is the 
instructed quantity.  
• Entitled Amount . The cash amount based on the [[DTC]] cash rate for 
this instruction. 
• Entitled Quantity . The [[securities]] quan tity to be debited or credited 
based upon the [[DTC]] security rate per this instruction.  
• Customer Reference [[ID]] . Your own identification information for this 
instruction. It can be a number, free- format text, or whatever you 
used to identify this instruction in your own system.  
Agent-Entered Quantities 
These fields are only applicable to mortgage- backed PUTs. 
• Agent Entered Quantity . The quantity entered by the agent on 
PUT (mortgage backed) instructions to be paid. This quantity can be 
for the full or partial instructed quantity.  
• Agent Remaining Quantity . The instructed quantit y less the 
quantity entered by the agent on PUT (mortgage b acked) 
instructions. Remaining unpaid quantity.  
 

---

## Page 81

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 81 
CORPORATE ACTION INSTRUCTION STATEMENT 
REPORT (CAST) MESSAGES 
What is a CAST Message? 
The Corporate Action Movement Instruction Statement Report message (CAST) for reorganization events 
is an outbound message that provides a comprehensive statement of instruction processing information. 
It applies to voluntary (VOLU) events as well as PUT events with the right to retain (CHOS). 
Use of the CAST message is expanded for reorganization events. Starting prior to the instruction period, 
the CAST message provides you with your eligible, instructed, and uninstructed balances. The message 
period itself covers as wide a range as possible, ending on the latest possible date on which you can 
submit instructions. Each [[Option]] for a given event displays the [[DTC]] instruction deadline (except for those 
events not processed by [[DTC]]). 
For reorganization CASTs, the core message still provides your instruction-level balances. However, the 
message extension lists all instructions that occurred at the instruction level or at the protect instruction 
level. Each day, any instructions (or status changes related to those instructions) are sent in CAST 
messages. This includes instruction-level details that were entered into [[DTC]] processing systems (e.g., 
PTOP and PSOP) prior to the generation of the CAST message. The goal is to capture all instruction 
activity associated with an event (whether it occurred on a terminal or later via ISO messaging), gathering 
all instruction information in one place for comprehensive reference. 
CAST messages are sent daily until the day before the applicable expiration date, at which point multiple 
intraday messages are sent. See the timing table for details on message generation. 
CAST messages also provide instruction statuses that detail pending instructions (“Recycled”) as well as 
final statuses (such as “Made,” ”Canceled,” or “Withdrawn”). 
In short, this message: 
• Details all active voluntary events or PUT events with the right to retain per customer account,  
• Provides event-level instructed and uninstructed balances per event, 
• Provides instructed balances per [[Option]] number, 
• Provides instruction or protect instruction status (in the message extension), and 
• Provides [[Option]]-level VOI instruction detail (in the message extension).  
  

---

## Page 82

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 82 
The identifying information for a CAST message is: 
MX IDENTIFIER ISO 20022  
MESSAGE 
NAMES 
EXTENSION SHORT NAME EQUIVALENT 
ISO 15022 
EQUIVALENT 
[[DTCC]] 
PROCESSES 
seev.042.002.xx 3 CA Instruction 
Statement 
Report  
n/a CAST n/a NEW 
 
Reorganization Events Using CAST Messages 
Reorg Events Using 
CASTs  
This document shows the mapping for CAST messages per ISO event type 
code, sub event type, and extended sub event type. It links these SWIFT codes 
to their relevant legacy activity codes. 
 
When Are CAST Messages Generated? 
CAST Message Generation 
For certain long-term events: 
• 54 (conversion) and  
• 60 (warrant),  
 
…CAST messages are generated only when there is instruction activity until Actual Expiration Date – 7. It 
will then follow the normal CAST daily message timing.  
For activities 53 (CD early redemption) and 66P (MMI survivor options), CAST messages are generated 
only upon instruction. Replacement activity occurs only when there is a transaction [[ID]] status change. It is 
possible to receive a replacement CAST if an instruction is awaiting paperwork. These messages may be 
sent until the [[DTC]] instruction expiration date.  
For all other activity types, CAST messages are triggered by the instruction start dates and expiration 
dates. 
Generally, instructions cannot be accepted after the [[DTC]] instruction expiration date. However, CAST 
messages will continue to be sent until after the actual expiration date to allow you the opportunity to 
 
3 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version 
number may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 83

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 83 
consult with your agent outside of [[DTC]]. Note that the period would also include the actual cover protect 
expiration date (if applicable). This provides you with the longest possible time period to take action 
outside of [[DTC]], if necessary.  
CAST Messaging Periods 
ACTIVITY CODE(S) / 
TYPE(S) 
NOTIFICATION 
PERIOD “FROM”  
MESSAGE ACTIVITY 
PERIOD 
NOTIFICATION 
PERIOD “TO”  
[[Option]] DEADLINE 
DATE 
The CAST message 
applies to this event 
type. 
The day on which the 
CAST NEWM is sent 
and the start of the 
messaging period. 
Replacement rules 
(REPL messages) for 
the length of the 
message period. 
The last day on which 
a CAST REPL 
message may be sent 
and the end of the 
messaging period. 
[[DTC]]’s deadline date 
for the [[Option]]. 
52: See list above 
52M: MRGR 
54T: BIDS / COTE,  
TEND / COTE 
The earlier of: 
[[DTC]] Early Expiration 
Date – 7 
 or 
[[DTC]] Instruction Start 
Date – 7  
If instruction activity: 
Send REPL if 
instruction activity  
If no instruction 
activity:  
Send every day 
from [[DTC]] 
Expiration Date –  3 
through [[DTC]] 
Expiration Date  
Actual Expirat ion 
Date 
 or 
Actual Cover Protect 
Expiration Date  
[[DTC]] Early Expiration 
Date unless it has 
already passed  
If it has passed, the 
[[DTC]] Instruction 
Expiration Date is 
used instead  
Note: The code 
“EARD” signifies that 
the [[DTC]] Early 
Expiration Date is 
being used  
53: CDRD 
66P: BPUT / SOBT 
Driven by instruction 
activity  
NEWM: Replacement 
activity occurs only 
when there is a 
transaction [[ID]] status 
change  
[[DTC]] Instruction 
Expiration Date  
[[DTC]] Instruction 
Expiration Date  
 
54: CONV  
60: EXWA 
Driven by instruction 
activity  
 until 
Actual Expiration  
Date – 7  
Driven by instruction 
activity  
 until 
Actual Expiration  
Date – 7  
Send every day from  
Actual Expiration 
Date – 7  
through Actual 
Expiration Date  
Date of the instruction  
 or 
Actual Expiration 
Date, if known  
[[DTC]] Instruction  
Expiration Date, if 
known  
 or 
Current Date (if [[DTC]] 
Instruction  Expiration 
Date is unknown)  

---

## Page 84

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 84 
ACTIVITY CODE(S) / 
TYPE(S) 
NOTIFICATION 
PERIOD “FROM”  
MESSAGE ACTIVITY 
PERIOD 
NOTIFICATION 
PERIOD “TO”  
[[Option]] DEADLINE 
DATE 
58: OTHR 
BPUT 
58B: BPUT 
62: BPUT / MBCK 
62B: BPUT / MBCK 
65B: BPUT 
65R: BPUT 
[[DTC]] Instruction Start 
Date – 7  
If instruction activity: 
Send REPL if 
instruction activity. 
If no instruction 
activity:  
Send every day 
from Actual 
Expiration End Date 
– 3  
through Actual 
Expiration End 
Date. 
Actual Expiration 
Date  
[[DTC]] Instruction 
Expirat ion Date 
59: EXRI [[DTC]] Sell Expiration 
Date – 7 
 or 
[[DTC]] Subscription 
Expiration Date –  7  
If instruction activity: 
Send REPL if 
instruction activity  
If no instruction 
activity:  
Send every day 
from Subscription  
Expiration Date –  3  
through 
Subscription 
Expiration Date  
Actual Expiration 
Date 
 or 
Actual Cover Protect 
Expiration Date  
[[DTC]] Instruction 
Expiration Date  
CAST Message Subscriptions / Daily Messaging Times 
CAST messages (delivered either via file or in real time) for most event types are sent at the times in the 
table below.  
• For events serviced by [[DTC]], the CAST is sent intraday five times on [[DTC]] Expiration Date (i.e., Actual 
Expiration Date – 1).  
• Additionally, it is sent four times on Actual Expiration Date (in the event that you need to instruct 
directly with the agent). 
  

---

## Page 85

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 85 
 
Message Begin Date     8:00 p.m. 
If Instruction Activity      8:00 p.m. 
Actual Expiration –  7 
through Actual 
Expiration – 2  
    8:00 p.m. 
Actual Expiration –  1 12:00 p.m. 1:30 p.m. 4:00 p.m. 4:30 p.m. 8:00 p.m. 
Actual Expiration  
or 
Actual Cover 
Expiration Date 
12:00 p.m. 1:30 p.m. 4:00 p.m. 4:30 p.m.  
There are some exceptions to these times (detailed above). 
CAST Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times 
specified above. Exceptions are noted in the holiday processing schedule. 
CAST Holiday Processing Schedule 
In addition to the timing specifications above, CAST message generation also conforms to the following 
holiday schedule: 
U.S. AND CANADIAN 
HOLIDAYS  
(BOTH [[DTC]] AND 
CANADA CLOSED) 
U.S. HOLIDAYS 
([[DTC]] CLOSED,  
CANADA OPEN) 
U.S. HOLIDAYS 
([[DTC]] OPEN,  
CANADA OPEN) 
CANADIAN HOLIDAYS 
([[DTC]] OPEN,  
CANADA CLOSED) 
No messages or files are 
sent on:  
• New Year's Day 
• Labor Day  
• Christmas Day.  
No messages or files are 
sent on:  
• Dr. Martin Luther 
King, Jr. Day  
• Presidents' Day  
• Memorial Day  
• Independence 
Day  
• Thanksgiving Day  
 
For these days, U.S. 
banks are closed but 
[[DTC]] is open:  
• Columbus Day  
• Veterans’ Day  
Messages are not sent 
for rights subscriptions 
(59) or warrant exercises 
(60). 
Normal volumes / 
transmission for all othe r 
event types.  
Normal volumes occur 
on these days:  
• Good Friday (All)  
• Victoria Day  
• Canada Day  
• CDN Thanksgiving 
Day 
• Boxing Day  
Files are transmitted 
based on customer 
subscription.  
 

---

## Page 86

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 86 
Pagination and CAST Messaging 
Pagination breaks a large message down into separate messages that are chained together using 
minimal repeated (mandatory) elements. It is used in cases in which there is too much data to fit inside a 
single message (given the SWIFT network’s 100K size limit).  
[[DTC]] will be using pagination for voluntary reorganization CAST messages when there is a large amount 
of extension-level instruction data (that is, repeating blocks of information populating the [[Option]] 
Instruction Details section). 
For example, a CAST message is sent for an event containing 50 separate instructions, of which only 30 
will fit into the initial message (on the first page). The additional 20 instructions are then included in the 
next chained message (on the second page). 
Limited event information (mandatory elements) will be repeated in each of the chained messages (for 
identification purposes and quick reference).  
The balance details and [[Option]] details
 are not repeated in the extension; all other information in the core 
message is carried over to the chained messages.  
A “Last Page” Y/N indicator is displayed on the final page of the CAST message extension.  
When the indicator is “Y,” the message is complete. 
Information Contained on the CAST Message 
The following table contains some of the important elements in the CAST message. 
For more detailed technical information about message contents and elements, please see the Data 
Dictionary and/or My Standards for this message. 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
From/To BIC The Business Identifier Code that represents the system that created the 
instruction message ([[DTCC]]) and the system that received it (your system).  
Business Message 
Identifier A unique identifier for an individual business message.  
Message Definition 
Identifier 
Contains the message identifier that defines the business message. It 
contains a message identifier published on the ISO 20022 website.  
Creation Date/Time The date and time the message was created, adjusted to UTC 
(Coordinated Universal Time).  
Page Number/Indicator  For messages over 100K, the page number is displayed and the last page 
is indicated by “Y.”  
Statement Type Set to “ALLL” (statement contains all instructions).   
Reporting Type Set to “MASE” (multiple accounts).  

---

## Page 87

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 87 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Statement Identification  Reference of the statement. Contains the CA [[ID]]  (Corporate Actions 
Identifier, [[DTC]]’s unique identifier for the corporate action event ). 
Frequency Code  
Frequency of the statement:  
• DAIL. Daily. 
• INDA. Intraday. This occurs toward the end of the messaging period 
only. See the timing table for specific times. 
Update Type 
Indicates whether the report is complete or contains changes only:  
• COMP. The transaction [[ID]] or protect information status fields are in a 
final status (such as “Made” o r “Dropped”).  
• DELT. Only used for intraday messages on Actual Expiration Date –  
1 or Actual Expiration Date when there is response activity from the 
previous CAST message.  
Activity Indicator  A Y/N indicator that states whether there is activity or an information upda t e 
reported in the statement.  
From/To Date and Time  
Defines the beginning and the end of the period range at which the 
deadline has been set. It begins with the Instruction Start Date and ends 
with the Actual Expiration Date or the Actual Cover Protect Expiration Date. 
If multiple dates apply, then the widest date range is used.  
Account and Statement 
Details 
This section includes the following information:  
• Safekeeping Account . Your client [[ID]]. 
• Corporate Actions Identification . Also known as the “CA [[ID]].” This 
is [[DTC]]’s unique identifier for the corporate action event.  
• Official Reference Corporate Actions Event Identification . Also 
known as the “Official Reference CA [[ID]].”  This is the official, unique 
identifier for the corporate action.  It is made up of the CA [[ID]] 
preceded by “US.” The COAF on the instruction must match the 
COAF on the announcement messages.  
• Event Type. The “CAEV” refers to the event type. See the 
Reorganization Event Codes table for a list of possible codes.  
• [[DTC]] Mandatory/Voluntary. An indicator that the event is mandatory 
(MAND) or voluntary (VOLU).  
• Underlying Security [[ID]] . The [[CUSIP]] for the security underlying the 
corporate action event.  

---

## Page 88

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 88 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Balance Details 
This section includes the following information:  
• Total Eligible Balance. The total eligible balance upon which you 
can instruct.  
• Uninstructed Balance. The balance in the event for which no 
instructions have been made.  
• Total Instructed Balance. The total instructed balance across al l 
options for the event. This is either the sum of  the instructions for the 
event or the position in the c ontra [[CUSIP]] for the event .  
o For most reorganization events, this is a cumulative total.  
o For long- lived events (53, 54, 60, 66P), this is not cumulativ e. 
It is based solely on the instructions for that day (i.e., the day 
the message is generated).  
[[Option]] Details 
Details about the selected [[Option]] for this CA event that pertain to this cash 
and/or security movement. These include:  
• [[Option]] Number. The [[Option]] identifier as specified on the 
announcement.  
• [[Option]] Type. The type of [[Option]] that is represented, e.g., “CASE” for 
cash and [[securities]]. See the Options tab in the Announcements 
data dictionary for the full list. 
• Instructed Balance. The balance of instructed position for this 
individual [[Option]].  
• [[default]] [[Option]] Indicator . “Y” indicates that this is the [[default]] [[Option]]. 
“N” indicates that it is not. 
• Deadline Date/Time. The [[DTC]] instruction expiration date.  
• Deadline Type. Specifies the t ype of deadline for instructing. The 
early deadline date will be shown until it expires; after that point, the 
expiration date is shown.  
o EARD. [[DTC]] Consent Payment Expiration Date.  
o RDDT. [[DTC]] Instruction Expiration Date. 
The extension for the CAST message contains the instructions associated with this event: either the full 
list of existing instructions in the NEWM or any new/edited instructions in the REPL messages. The full list 
of instructions is not repeated in REPL messages.  
The extension contains summary information as well as repeating blocks of information. Each repeating 
block represents [[Option]] instruction details and/or [[Option]] protect cover details.  
  

---

## Page 89

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 89 
Some of the following information may be included in the message extension: 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Total Uncovered Protect 
Balance The balance of uncovered protect transactions at an event level.  
Total Instructed Balance:  
[[Option]] Balance Details  
This section contains information such as:  
• [[Option]] Uncovered Protect Balance. The balance of uncovered 
protect transactions at an [[Option]] level.  
• [[Option]] Daily Instructed Balance.  The d aily total of instructions for 
a given [[Option]] for the current day. This b alance includes  only 
“Made” instructions.  
• [[Option]] Oversubscription Quantity . For rights subscription events, 
this is the total number of oversubscribed units.  
When there  is an oversubscription privilege, this quantity is not 
included within the “Instructed Q uantity ” specified in the core 
message. 
• [[Option]] Unaccepted Balance. For election m erger events, this is 
the balance that is being moved into another [[Option]] number for 
payment due to the proration of the original [[Option]].  
Total Instructed Balance:  
[[Option]] Balance  
(Repeating Block)  
Each block of informat ion represents a single instruction. This block is 
repeated per individual instruction.  
This information includes:  
[[Option]] Number. The identifying [[Option]] number for the instruction.  
• Transaction Identification . The instruction reference number 
assigned by DT C (also referred to as the VOI Number) . 
• Transaction Sequence Number . An additional r eference number 
used to uniquely identify this instruction . 
• Transaction Identification Date. The date of your instruction.  
• Transaction Contra [[CUSIP]]. The [[ID]] of the contra CU SIP for this 
[[Option]].  
• Transaction Identification Quantity . The quantity specified on this 
instruction.  
• Transaction Identification Oversubscription Quantity . The 
quantity relating only to the oversubscription. This pertains to rights 
subscriptions only.  
• Transaction Identification Status . The status of the instruction. 
Values here include:  
o CANC. Cancel . Applies when the instruction  is canceled by a 
client or when  instructions relate to an event that is terminated, 
rescinded , or canceled by the [[issuer]].  
o CCAN. Conversion Cancellation . The cancellation of a 
Conversion i nstruction (upon agent approval only ). 
o  DROP. Dropped. The i nstruction was dropped due to 
insufficient position . 
o MADE. Made. The instruction has been fully process ed. 

---

## Page 90

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 90 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
o PDOC. Pending Documentation . The instruction for a CD Early 
Redemption is awaiting paperwor k. The instruction will become 
MADE when [[DTC]] releases instruction upon receiving the 
necessary paperwork . 
o PENA. Pending Approval . The instruction is pending rele ase or 
deletion  from the external approval function (RTOP) . 
o PEND. Pending. The i nstruction is waiting for an update after 
submission.  
o RECY. Recycle . The instruction is waiting for position. By end 
of day, the i nstruction will subsequently become either MADE 
or DROP. 
o REJA. Rejected by Agent . The i nstruc tion or withdr awal 
rejected by the agent relating to a Survivor [[Option]] event  
o REJT. Reject. The instruction d [[ID]] not pass initial validation. You 
can edit the rejection via the ATAM system.  
o REMD. Recycle Made.  Previously recycl ed transactions have 
been MADE and the system is processing the updates . 
o RESC. Rescinded . The instruction has been rescinded by the 
[[issuer]].  
o SWUN. Swung. For Put events, the i nstruction has been move d 
from one client account to another . 
o WITH. The c lient instruction was withdrawn for  events with 
withdrawal privile ge. 
• Transaction Identification Protect Date. The date of the client 
protect instruction. 
• Transaction Identification Cover Protect Date. The date of the 
cover protect instruction.  
• Transaction Conditional Quantity . The conditional quantity of the 
instruction. This pertains to tender offers.  
• Transaction Tender Bid Price . The tender bid price of the 
instruction. This pertains to tender offers.  
• Customer Reference Identification . Your own internal identifier for 
this instruction, entered when the instruction was originally 
submitted. It can be a number, free- format text, or whatever you 
used to identify this instruction in your own system.  

---

## Page 91

CAST Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 91 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Total Instructed Balance:  
[[Option]] Protect Instruction 
Details 
(Repeating Block)  
Each block of information represents a single  protect  instruction. This block 
is repeated per individual protect.  
This information includes:  
• [[Option]] Number. The identifying opti on number of the protect 
instruction.  
• Protect Identification . The instruction r eference number assigned 
by [[DTC]] to the uncovered protect instruction (also known as the VOI 
number). 
• Protect Sequence Number . An additional reference number used to 
uniquely identify an uncovered protect instruction.  
• Customer Reference [[ID]] . Your own internal identifier for this 
instruction, entered when the instruction was originally submitted. It 
can be a number, free- format text, or whatever you used to identify 
this instruction  in your own system.  
• Protect Date. The date of the protect instruction. 
• Cover Protect Date. The d ate of the cover protect. If a partial cover 
transaction occurs, this will be the latest cover date.  
• Protect Identification Quantity . The quantity of the prote ct 
instruction. For protects that  are partially covered, the quan tity is 
reduced by the amount partially covered.  
• Protect Identification Uncovered Quantity. The quantity of the 
protect instruction that has not been covered.  
• Protect Identification Oversubscription Quantity . The quantity of 
the protect oversubscription.  
• Protect Identification Status . The status of the p rotec t instruction. 
Possible values include the following:   
o WITH. The p rotect instruction has been withdrawn . 
o COVR: The p rotect instruction has been fully covered.  
o EXPI: Protect instruction has expired.  
o OPEN: The p rotect instruction has not been fully covered. This 
status also applies to  partial covers.  
• Protect Conditional Quantity . The conditional quan tity for the 
protect i nstruction . This pertains to tender offers.  
• Protect Tender Bid Price. The tender bid price of the protect 
instruction . This pertains to tender offers.  

---

## Page 92

CACO Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 92 
CORPORATE ACTION MOVEMENT CONFIRMATION 
(CACO) MESSAGES 
What is a CACO Message? 
The Corporate Action Movement Confirmation (CACO) message primarily provides [[securities]] or cash 
payment notification for reorganization events. This message also: 
• Notifies you of charges for rights subscriptions or warrant exercises,  
• Provides instruction-level breakdown of cash or [[securities]] payments, 
• Provides [[Option]]-level accepted and unaccepted balances for prorated reorganization events, 
• Provides instruction-level detail of prorated entitlements for accepted and unaccepted instructions, 
and 
• Provides expanded detail for rights subscription events (including instruction entitlements for 
subscription and oversubscriptions, subscription charges, and subscription refund details). 
The identifying information for a CACO message is: 
MX IDENTIFIER ISO 20022  
MESSAGE 
NAMES 
EXTENSION SHORT NAME EQUIVALENT 
ISO 15022 
EQUIVALENT 
[[DTCC]] 
PROCESSES 
seev.036.002.xx 4 CA Movement 
Confirmation 
supl.011.001.xx  CACO MT 566 Allocations/ 
Payments 
  
 
4 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version 
number may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 93

CACO Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 93 
Reorganization Events Using CACO Messages 
Reorg Events Using 
CACOs  
This document shows the mapping for CACO messages per ISO event type 
code, sub event type, and extended sub event type. It links these SWIFT codes 
to their relevant legacy activity codes. 
Information events: 
• 51 ([[UIT]]),  
• 91 (name change), and  
• 96 (MMI important notice)  
…and events not processed by [[DTC]]: 
• 52N (tender),  
• 54N conversion),  
• 58N (repayment), and  
• 60N ([[Warrants]])  
…will not generate a CACO. See the Reorganization Event Codes mapping document for full event type 
information. 
 
When Are CACO Messages Generated? 
CACO Message Generation 
CACO messages are triggered by a movement of cash and/or [[securities]] into your account due to a 
reorganization event. They are created according to the subscriptions below. 
CACO Message Subscriptions / Daily Messaging Times 
The subscriptions for CACO events are for either file or real-time messages for all event types: 
• Via file at 4:00 p.m. eastern time, or 
• Real-time throughout the day between 8:00 a.m. and 3:30 p.m. eastern time. 
  

---

## Page 94

CACO Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 94 
CACO Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times 
specified above. Messages are not sent on Saturday or Sunday. Exceptions are noted in the holiday 
processing schedule. 
 
CACO Holiday Processing Schedule 
In addition to the timing specifications above, CACO message generation also conforms to the following 
holiday schedule: 
U.S. AND CANADIAN 
HOLIDAYS  
(BOTH [[DTC]] AND 
CANADA CLOSED) 
U.S. HOLIDAYS 
([[DTC]] CLOSED,  
CANADA OPEN) 
U.S. HOLIDAYS 
([[DTC]] OPEN,  
CANADA OPEN) 
CANADIAN HOLIDAYS 
([[DTC]] OPEN,  
CANADA CLOSED) 
No messages  or files are 
sent on:  
• New Year's Day 
• Labor Day  
• Christmas Day.  
Messages are only sent 
for Canadian payments 
on these days:  
• Dr. Martin Luther 
King, Jr. Day  
• Presidents' Day  
• Memorial Day  
• Independence Day  
• Thanksgiving Day  
Files are transmitted 
based on customer 
subscription.  
For these days, U.S. 
banks are closed but 
[[DTC]] is open:  
• Columbus Day 
• Veterans’ Day  
[[Stock]] allocation only (no 
cash allocation).  
Normal volumes occur 
on these days:  
• Good Friday ( All) 
• Victoria Day  
• Canada Day  
• CDN Thanksgiving 
Day 
• Boxing Day  
Files are transmitted 
based on customer 
subscription.  
 
[[custody]] Reorg and Reorg Deposits 
CACO messages for [[custody]] reorg deposits and reorg deposits are created when [[DTC]] allocates 
[[securities]] and/or cash entitlements for that deposit. These deposits will normally contain a unique event 
reference number (CA [[ID]]).  
• If available, the deposit will use the CA [[ID]] to identify the event.  
• In cases where there is no unique CA [[ID]] tied to a deposit, the DAM deposit [[ID]] will be utilized.  
  

---

## Page 95

CACO Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 95 
Debit Movements on the CACO 
Debit movements occur on CACOs for both mandatory and voluntary reorgs. In situations that produce 
more than one CACO message for a given [[Option]] (e.g., CASE), there will only be one debit security 
movement. 
Multiple Movements and CACO Messages 
Events with multiple credit movements that allocate on the same day may have those movements 
recorded on a single message or on multiple messages. When credit movements occur within different 
time periods on the same day, each movement is recorded on a separate message. Credit movements 
occurring within the same time period will be shown on a single CACO message. 
Pagination and CACO Messaging for Reorganizations 
Pagination breaks a large message down into separate messages that are chained together using 
minimal repeated (mandatory) elements. It is used in cases where there is too much data to fit inside a 
single message (given the SWIFT network’s 100K size limit).  
[[DTC]] will be using pagination for voluntary reorganization CACO messages when there is a large amount 
of extension-level instruction data (that is, repeating blocks of information populating the [[Option]] 
Transaction Details section) for the CACO payment.  
For example, a payment for a given CACO message was made according to instruction details for 50 
separate instructions, of which only 30 will fit into the initial message (the first page). The additional 20 
instructions are then included in the next chained message (the second page). 
Limited event information (mandatory elements) will be repeated in each of the chained messages (for 
identification purposes and quick reference): 
• Corporate Action Event [[ID]], 
• Official Corporate Action Event [[ID]], 
• Event Type, 
• Safekeeping Account, 
• Confirmed Balance, 
• [[Option]] Number, and 
• [[Option]] Type. 
These fields are defined in the table below
. 
A “Last Page” Y/N indicator is displayed on the final page of the CACO message extension.  
When the indicator is “Y,” the message is complete. 
  

---

## Page 96

CACO Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 96 
Information Contained on the CACO Message 
The following table contains some of the important elements in the CACO message. 
For more detailed technical information about message contents and elements, please see the Data 
Dictionary and/or My Standards for this message. 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Corporate Action Event 
Identification  
Also known as the “CA [[ID]].”  This is [[DTC]]’s unique identifier for the corporate 
action event.  
Official Corporate Action 
Event Identification  
Also known as the “Official Reference CA [[ID]].”  This is the official, unique 
identifier for the corporate action. It is made up of the CA [[ID]] preceded by 
“US.” In order for this instruction to be accepted and processed, the COAF 
on the instruction must match the COAF on the announcement  messages.  
Event Type 
The “CAEV” refers to the event type.  
See the Reorganization Event Codes table for a list of ISO 20022 event 
codes.  
Event Security Includes security description, type, and [[CUSIP]] code . 
Balance Information  
Several fields provide balance information according to the event type:  
• Safekeeping Account . Your client [[ID]]. 
• Confirmed Balance. The balance upon which your payment is 
based. 
• Total Eligible Balance. The total eligible balance upon which you 
can instruct.  
• [[collateral]] Out of Balance. Your pledged position that is not eligible 
for payment.  
Note that not every balance will apply to every event type.  
Corporate Action Details 
Details about the corporate action:  
• Additional Business Process Indicator . This is used for partial 
mandatory puts (PPUT). This indicator  shows that there is a 
previously extended [[DTC]] event name.  
[[Option]] Details 
Details about the selected [[Option]] for this CA event that pertain to this cash 
and/or security movement. These include:  
• [[Option]] Number. The [[Option]] identifier as specified on the 
announcement.  
• [[Option]] Type. The type of [[Option]] that is represented, e.g., “CASE” 
for cash and [[securities]]. See the Options tab in the 
Announcements data dictionary for the full list. 
• Proration Rate. The rate used to determine the accepted quantity.  
• [[Option]] Features. The code “PROR” indicates that this [[Option]] is 
prorated.  

---

## Page 97

CACO Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 97 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Security Movement Details 
For events in which a payment was made in [[securities]] , this section 
provides information about the movement of those [[securities]]. These details 
may include:  
• Security Information. Information that identifies the [[DTC]] disbursed 
security and type, as well as contra [[CUSIP]] indication.  
• Credit/Debit Indicator . 
• New to Old Rate. The [[DTC]] [[securities]] rate.  
• Fraction Disposition . A code that explains the way fractional 
[[shares]] were handled in the movement of [[securities]]:  
o CINL. Cash in Lieu of Fractional Share (CL) . 
o RDDN. Drop (DF).  
o RDUP. Round U p (RU). Note that this value is used in conjunction 
with the Rounding Factor  field in the message extension.  
• Posting Quantity. The quantity of s ecurities that were debited from 
or credited to your account.  
• Posting Date. The [[DTC]] allocation date and time.  
• Payment Date. The [[issuer]] -announced date on which the [[securities]] 
were paid.  
Cash Movement Details 
For events in which a cash allocation is being made, these are details 
about the cash payment. These details may include:  
• Credit/Debit Indicator. Normally, an allocation results in a credit to 
your account (and the indicator  is set to “Credit”). The debit indicator 
is utilized when charges occur.  
• Posting Amount . The cash amount for a cash payout, principal 
payout, or [[Premium]] payout.  
• Accrued Interest Amount . The cash amount for an interest payout.  
• Charges Amount . Any charges applicable to warrant exercise or  
rights subscription events.  
• Posting Date. The [[DTC]] allocation date and time.  
• Payment Date. The [[issuer]] -announced date on which the cash was  
paid.  
• [[DTC]] Cash Rates. The [[DTC]] rate used for calculating the cash 
[[Entitlement]] on the distribution.  Based on the reorg event type, this 
rate could be principal, interest, [[Dividend]], or cash.  
• Prices. These may include the generic cash price paid per product 
or the generic cash price received per product.  
  

---

## Page 98

CACO Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 98 
Information Contained in the CACO Message Extension 
This portion of the message provides additional payment information, such as payout type and RDP 
reference number. In addition to this, the CACO extension for reorganizations provides [[Option]] instruction 
details for voluntary events, which provides the [[Entitlement]] at an instruction level. The sum of these 
instructions makes up your allocation for this event. The inclusion of all instructions creates transparency 
into this sum and allows you to improve your balancing process.  
Some of the following information may be included, depending on the event type represented by the 
message: 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Sub Event Type  
Codes that represent the extended sub event type for this particular 
corporate action event. See the Event Type for a list of these codes and 
associated information.  
[[Option]] Transaction Details  
(repeating block)  
Each block of information represents a single instruction. This block is 
repeated per individual instruction and is used for voluntary events, [[custody]] 
deposits, and reorg deposits only.  
Some of the information in this message section may include:  
• Transaction [[ID]] /Sequence Number : 
o For voluntary events, this is the VOI reference number.  
o For [[custody]] reorg deposits, this is the [[custody]] [[ID]].  
o For reorg deposits, this is the Deposit [[ID]].  
• Transaction Date/Time. The date and time of the voluntary reorg 
instructions, or the deposit date/time for reorg or [[custody]] reorg 
deposits.  
• Transaction Quantity/Oversubscription . Resulting quantity of 
cash or security involved in this transaction, as well as the 
oversubscription transaction quantity for rights subscrip tion offers. 
• Accepted/Unaccepted Quantity. The portion of the transaction [[ID]] 
quantity that was accepted or not by the [[issuer]]/agent  for prorated 
events . 
• Entitled Amount/Units . The accepted quantity multiplied by the 
cash or [[securities]] payment rate.  
• Agent Entered Quantity. The quantity entered by the agent on 
PUT (mortgage backed) instructions to be paid. This quantity can be 
for the full or partial instructed quantity.  
• Customer Reference [[ID]] . Your own identification information for this 
instruction. It can be  a number, free- format text, or whatever you 
used to identify this instruction in your own system.  

---

## Page 99

CACO Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 99 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Cash / [[securities]] 
Movement Details 
(repeating block)  
Each block of information represents a single cash or [[securities]] movement 
for a particular event. There can be more than one movement of cash or 
[[securities]] within a single CACO message.  
Some of the information in this portion of the message may include:  
• Credit/Debit Indicator . 
• Payout Type . The type of payout associated with the event (e.g., 
principal, cash, [[securities]], interest, or [[Dividend]]).  
• Reason/Sub Reason Code . Where applicable, the reason code 
and sub reason code associated with the transaction. See the 
Reason Code and Sub Reason Code t [[ABS]] in the Entitlements and 
Allocations Data Dictionary for a full list of codes. 
• Rounding Factor . For [[securities]], the decimal above which numbers 
are rounded (e.g., if the rounding factor is 0.6, numbers of 0.6 and 
above will be rounded up).  
• RDP Reference Number . Unique [[DTCC]] legacy reference used for 
matching and reconciling legacy [[CCF]]  records. It indicates how 
values are sourced from [[CCF]] legacy files.  
 

---

## Page 100

CAPS Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 100 
CORPORATE ACTION EVENT PROCESSING STATUS 
ADVICE (CAPS) MESSAGES 
What is a CAPS Message? 
Corporate Action Event Processing Status Advice (CAPS) messages provide unallocated balance information 
at an account level. They are sent to indicate non-allocation on an event on or past its payable date. CAPS 
messages are generated in real time during the afternoon to reflect any change in the status of an event. 
The message provides a high-level reason code for the failure to allocate. For reorganization events, these can 
be Fail Reason and Unallocated Reason codes. 
The identifying information for a CAPS message is: 
MX IDENTIFIER ISO 20022  
MESSAGE 
NAMES 
EXTENSION SHORT NAME EQUIVALENT 
ISO 15022 
EQUIVALENT 
[[DTCC]] 
PROCESSES 
seev.032.002.xx 5 CA Event 
Processing  
Status Advice  
supl.010.001.xx  CAPS MT 567 Unallocated  
Positions  
 
Reorganization Events Using CAPS Messages 
Reorg Events Using 
CAPS  
CAPS messages apply to put events with known declared payable dates that 
have not allocated when expected. This document maps the old and new codes 
for Reorganization events that use CAPS messages. 
 
  
 
5 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version number 
may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 101

CAPS Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 101 
When Are CAPS Messages Generated? 
CAPS messages are available in real time hourly between 1:00 p.m. and 4:00 p.m. eastern time. They are 
available via file at 4:00 p.m. eastern time. 
CAPS Messaging Notes 
1. The CAPS message is based on a CAPA that was previously sent for an event (when available).  
2. It is possible to receive a CAPS message on an event that never had a CAPA. This can occur for late 
events in a same-day position capture. A late event would come into the system and generate a 
CANO-E at 1:30 p.m., then generate a CAPS message later that day if it does not allocate. 
3. Reason codes are provided to explain why a given event was not allocated. Please see the “Reason 
Codes for CAPS” tab in the Entitlements and Allocations data dictionary for a list of these codes. 
4. A time stamp in the Business Application Header (BAH) allows you to verify message order. 
5. If an item is past payable date, the CAPA message is only sent once. The CAPS message will 
continue to be sent on a daily basis. 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during these times: 
• Messages between 1:00 p.m. and 4:00 p.m. 
• Files transmitted at 4:00 p.m. eastern time. 
Exceptions are noted in the holiday processing schedule. 
  

---

## Page 102

CAPS Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 102 
CAPS Holiday Processing Schedule 
In addition to the timing specifications above, CAPS message generation also conforms to the following holiday 
schedule: 
U.S. AND CANADIAN 
HOLIDAYS  
(BOTH [[DTC]] AND 
CANADA CLOSED)  
U.S. HOLIDAYS 
([[DTC]] CLOSED,  
CANADA OPEN) 
U.S. HOLIDAYS 
([[DTC]] OPEN,  
CANADA OPEN) 
CANADIAN HOLIDAYS 
([[DTC]] OPEN,  
CANADA CLOSED)  
No messages  or files are 
sent on:  
• New Year's Day 
• Labor Day  
• Christmas Day.  
Messages are sent at:  
• 1:00 p.m.,  
• 2:00 p.m., and  
• 3:00 p.m. 
eastern ti me for P&I and 
foreign payments for 
these holidays:  
• Dr. Martin Luther 
King, Jr. Day  
• Presidents' Day  
• Memorial Day  
• Independence Day  
• Thanksgiving Day  
(The 4:00 message is 
not sent.)  
For these days, U.S. 
banks are closed but 
[[DTC]] is open:  
• Columbus Day  
• Veterans’ Day  
Files are transmitted 
based on customer 
subscription.  
Normal volumes occur 
on these days:  
• Good Friday ( All) 
• Victoria Day  
• Canada Day  
• CDN Thanksgiving 
Day 
• Boxing Day  
Files are transmitted 
based on customer 
subscription.  
 
Information Contained on the CAPS Message 
For more detailed technical information about message contents and elements, please see the Data Dictionary 
and/or My Standards for this message. 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Corporate Action Event 
Identification (CA [[ID]])  
Corporate Actions Identifier. This is [[DTC]]’s unique identifier for the 
corporate action event.  
Official Corporate Action 
Event [[ID]] 
Official Corporate Actions Identifier. This is the official, unique identifier for 
the corporate action. It is made up of the CA [[ID]] preceded by “US.”  
Event Type The four -letter code that defines the event type. This is always “BPUT.” 
Event Processing Status 
Information 
This section provides you with information regarding the allocation status. 
Since CAPS messages indicate that an allocation has not been made, this 
section provides you with the reason why the allocation is pending:  
• Pending / No Specified Reason . This field appears when a reason 
is not given for the allocation not being made. It is used with the 
code “NORE,” meaning “No reason to report or no reason available 
to report.”  

---

## Page 103

CAPS Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 103 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
• Pending / Reason Code . This field is us ed when there is a reason 
code associated with the non- allocation. Options are: 
o NSEC. [[securities]] not delivered . 
o NPAY. No payment . 
o OTHR. Other; see narrative.  
• Additional Reason Information . This field provides any informa t ion 
that was given regarding the non -allocation. It is an optional, free-
text field that displays a descriptive whenever one is given.  
Supplementary Data 
This section displays additional information related to the reorganization 
event: 
• Security Identification . The [[CUSIP]] number and description of the 
security involved in this event.  
• Safekeeping Account . Your client [[ID]].  
Unallocated Details: 
Unallocated 
Reorganization Balance 
The fields in this category are specific to unallocated reorganization 
balances:  
• Total Eligible Balance. The total eligible balance upon which you 
can instruct.  
• Pledged Balance. The portion of the original b alance position held 
in a [[DTC]] general f ree account as of the day prior t o publication d ate 
• Investment Pledged Balance. The portion of the original balance 
position held in a [[DTC]] i nvestment account as of  the day prior to 
publication d ate. 
• Investment Unpledged Balance. The portion of the original 
balance position held in a [[DTC]] segregated  account as of the day 
prior to publication date.  
• Memo Segregation Balance . An amount set aside in order  to 
protect a customer’s fully paid for [[securities]] from being delivered out 
of a [[participant]] account  
Unallocated [[securities]] 
Transaction Details 
The fields in this category refer specifically to [[securities]] that have not been 
allocated:  
• Credit Debit Indicator . The code “CRED” or “DEBT” indicates 
whether the cash movement would be a credit or debit.  
• Reason Code . The reason why the [[securities]] allocation was being 
made in the first place. Please see the “Reason C odes for CAPS” 
tab in the Entitlements and Allocations data dictionary for the 
full list of reason codes.  
• Transaction Amount . The resulting quantity of [[securities]]  
concerned in this transaction.  
• Unallocated Reason Code.  The reason why the allocation was not 
made. Please see the “Unallocated Reason C odes for CAPS” tab in 
the Entitlements and Allocations data dictionary for the full list 
of codes.  
• Earliest Payment Date.  The d ate and time on which the [[securities]] 
movement wa s scheduled to take place.  

---

## Page 104

CAPS Messages  
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 104 
DATA ELEMENT OR 
DATA CATEGORY DEFINITION / INFORMATION  
Unallocated Cash 
Transaction Details 
The fields in thi s category refer specifically to cash that has not been 
allocated:  
• Credit Debit Indicator . The code “CRED” or “DEBT” indicates 
whether the cash movement would be a credit or debit.  
• Reason Code . The reason why the cash allocation was being made 
in the first place. Please see the “Reason C odes for CAPS” tab in 
the Entitlements and Allocations data dictionary for the full list 
of reason codes.  
• Transaction Amount . The resulting cash amount concerned in this 
transaction . 
• Unallocated Reason Code.  The reason why the cash allocation 
was not made. Please see the “Unallocated Reason C odes for 
CAPS” tab in the Entitlements and Allocations data dictionary 
for the full list of cod es. 
• Earliest Payment Date.  The d ate and time on which the cash 
movement wa s scheduled to take place.  
Corporate Action Details This section provides some important dates for the corporate action.  
• Payment Date. Payable date as ann ounced by the [[issuer]] or offeror.  

---

## Page 105

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 105 
 
APPENDIX A: MESSAGING SCENARIOS FOR 
REORGANIZATION EVENTS 
Scenario 1: Mandatory Reorganization Event Flow 
Activity Codes: 71, 72, 73, 79, 90, 91, 93.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 1: Mandatory Reorg Event 
 
  


---

## Page 106

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 106 
Scenario 2: Events “Not Processed at [[DTCC]]” 
Activity Codes: 52N, 54N, 58N, 60N.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 2: Events Not Processed at [[DTCC]] 
 
 
  


---

## Page 107

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 107 
Scenario 3: Tender Offers 
Activity Codes: 52, 54T.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
Tender Offer Types: 
• Bid Tender / Sealed Tender 
• Cash In Lieu 
• Mini Tender 
• Self-Tender 
• Offer to Purchase 
• Convert and Tender 
• No Sub Event 
• Cash and [[securities]] 
 
This scenario describes a range of tender offers. 
 
 
Scenario 3a: Tender Offers (1 of 2) 


---

## Page 108

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 108 
 
 
Scenario 3b: Tender Offers (2 of 2) 
  


---

## Page 109

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 109 
Scenario 4: Exchange (144A or REGS) 
Activity Code: 52.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
Exchange Offer Types: 
• 144a 
• [[Regulation S]] 
 
 
Scenario 4: Exchange – 144A or REGS 
 
  


---

## Page 110

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 110 
Scenario 5: Exchange Offer (Cash and [[securities]], No Sub Event) 
Activity Code: 52.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
Exchange Offer Types: 
• Cash and [[securities]] 
• (No Sub Event) 
This scenario describes non-specific exchange offer events, as well as events that offer payout in a 
combination of cash and [[securities]].  
 
 
Scenario 5a: Exchange Offer: No Sub Event, Cash and [[securities]] (1 of 2) 
 


---

## Page 111

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 111 
 
Scenario 5b: Exchange Offer: No Sub Event, Cash and [[securities]] (2 of 2) 
 
  


---

## Page 112

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 112 
Scenario 6: Tender Offer (Consent) 
Activity Code: 52.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 6a: Tender Offer – Consent (1 of 2) 
 


---

## Page 113

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 113 
 
Scenario 6b: Tender Offer – Consent (2 of 2) 
 
  


---

## Page 114

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 114 
Scenario 7: Voluntary Merger 
Activity Code: 52M.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
Note that the unelected position is paid via Activity Code 93. Please see Scenario 1 for details regarding 
mandatory events.  
 
Scenario 7a: Voluntary Merger (1 of 2) 


---

## Page 115

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 115 
 
Scenario 7b: Voluntary Merger (2 of 2) 
 
 
  


---

## Page 116

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 116 
Scenario 8: Warrant Exercise 
Activity Code: 60.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
 
Scenario 8a: Warrant Exercise (1 of 2) 
 


---

## Page 117

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 117 
 
Scenario 8b: Warrant Exercise (2 of 2) 
 
  


---

## Page 118

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 118 
Scenario 9: Redemption of [[Warrants]] 
Activity Code: 61.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
A redemption of [[Warrants]] is based on a related warrant exercise event expiration. 
 
 
Scenario 9: Redemption of [[Warrants]] 
 
  


---

## Page 119

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 119 
Scenario 10: Conversion 
Activity Code: 54.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
Partial call conversions are announced via the contra [[CUSIP]]. 
 
 
Scenario 10: Conversion 
 
  


---

## Page 120

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 120 
Scenario 11: Full Call / Maturity (Convertible [[securities]]) 
Activity Code: 69.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 11: Full Call / Maturity (Convertible [[securities]]) 
 
 
  


---

## Page 121

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 121 
Scenario 12: Mandatory Put 
Activity Codes: 65, 65G.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 12: Mandatory Put 
  


---

## Page 122

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 122 
Scenario 13: Partial Mandatory Put 
Activity Code: 65P.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
This partial mandatory put is based on a DRAW event. Only selected holders are affected. 
 
 
Scenario 13: Partial Mandatory Put 
 
  


---

## Page 123

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 123 
Scenario 14: Optional Put 
Activity Codes: 58, 58B.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 14a: Optional Put (1 of 2) 


---

## Page 124

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 124 
 
Scenario 14b: Optional Put (2 of 2) 
 
  


---

## Page 125

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 125 
Scenario 15: Put (Mortgage-Backed) 
Activity Codes: 62, 62B.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 15a: Mortgage-Backed Put (1 of 2) 


---

## Page 126

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 126 
 
Scenario 15b: Mortgage-Backed Put (2 of 2) 
 
  


---

## Page 127

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 127 
Scenario 16: Mandatory Put for Cash with Right to Retain 
Activity Code: 65B.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 16a: Mandatory Put for Cash with Right to Retain (1 of 2) 


---

## Page 128

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 128 
 
Scenario 16b: Mandatory Put for Cash with Right to Retain (2 of 2) 
 
  


---

## Page 129

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 129 
Scenario 17: Mandatory Put for [[securities]] with Right to Retain 
   (Put Extendable) 
Activity Codes: 65R.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 17a: Mandatory Put for [[securities]] with Right to Retain (1 of 2) 


---

## Page 130

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 130 
 
Scenario 17b: Mandatory Put for [[securities]] with Right to Retain (2 of 2) 
 
  


---

## Page 131

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 131 
Scenario 18: Rights Subscription 
Activity Code: 59.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 18a: Rights Subscription (1 of 3) 


---

## Page 132

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 132 
 
Scenario 18b: Rights Subscription (2 of 3) 


---

## Page 133

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 133 
 
Scenario 18c: Rights Subscription (3 of 3) 
 
  


---

## Page 134

Appendix A: Messaging Scenar ios for Reorganization Events 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 134 
Scenario 19: CD Early Redemptions and Survivor Options (“Death 
Puts”) 
Activity Codes: 53 and 66P.  
See the Reorganization Event Codes table for a list of ISO 20022 event codes. 
 
 
Scenario 19: CD Early Redemptions / Survivor Options 
 
 


---

## Page 135

 
ISO 20022 M essagi ng for Reor ganiz ations: Entitlements and Allocations 135 
 
 
 
 
FOR MORE INFORMATION 
 
 
Email [[DTCC]] Learning at: 
corelearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
FOR MORE INFORMATION 
 
 
Email [[DTCC]] Learning at: 
corelearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 