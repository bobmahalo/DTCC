---
title: "User Guide: ISO 20022 Messaging for Redemptions"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO_20022_RedemEntAlloc_UG_FINAL.pdf"
pages: 157
size: "5741.6 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# User Guide: ISO 20022 Messaging for Redemptions

**Original File:** [ISO_20022_RedemEntAlloc_UG_FINAL.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO_20022_RedemEntAlloc_UG_FINAL.pdf)  
**Category:** Other  
**Total Pages:** 157  
**File Size:** 5741.6 KB  

---

## Page 1

 
 
[[DTC]] CORPORATE ACTIONS 
USER GUIDE: ISO 20022 MESSAGING FOR REDEMPTIONS 
VERSION 7.1 
MARCH 8, 2021 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
Disclaimer 
The primary purpose of this user guide is to familiarize clients with ISO 20022 Messagi ng for Corpor ate Action 
Reorganizations. This guide is not intended to serve as a legal document. No statement in this guide should be construed 
as a legally binding rule or [[regulation]], or as creating an obligation on the part of [[DTCC]] or any of its subsidi aries. In addition, 
any time schedules or time requirements set forth herein are subject to change without notice.  
This guide is meant as an educational tool to assist in your understanding of ISO 20022 messaging as it relates to 
corporate action processi ng at [[DTCC]]. It should not be used as a basis for systems applications coding. For coding 
purposes, please refer to specific schemas and message implementation guides that can be found at 
http://www.[[DTCC]].com/[[settlement]]- and-[[Asset]]-services/corporate- actions-processing/iso -20022-messaging -specifications . 
 
Doc Info: March 8, 2021  
Publication Code: CA219 
Service: [[DTC]] Corporate Actions  
Title: User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations

---

## Page 3

 
 
TABLE OF CONTENTS 
An Introduction to ISO 20022 Messaging ....................................................................................8  
What is ISO 20022 Messaging? ................................................................................................. 8 
Benefits of Using ISO 20022 Messaging for Corporate Actions .......................................................8  
Benefits of Using ISO 20022 for Redemptio ns Proc es sing ............................................................8  
How Can I Learn More? ............................................................................................................9  
Introduction to Messaging for Redemptions ............................................................................. 11 
Co rpo rate Actio ns  Mess ag es  in the Red emp tions Lifecyc le .......................................................... 11 
How to Read an MX Identifier .................................................................................................. 12 
Supp lementary  D ata and  Mes s age Extens io ns ........................................................................... 12 
Data Dictionaries, Scenarios, Message Usage Guidelines, and Event Templates ......................... 14 
Redemptions Data Dictionaries ................................................................................................ 14 
Announcements Data Dictionary ............................................................................................. 14 
Entitlements and Allocations Data Dictionary ............................................................................ 18 
Using the Data Dictionary to Map from [[CCF]] to ISO 20022 .......................................................... 20 
Redemptions Message Usage Guidelines.................................................................................. 21 
Redemptions Scenarios .......................................................................................................... 22 
Redemption Event Templates .................................................................................................. 22 
Introduction.......................................................................................................................... 22 
Viewing Mess ag e D ata Elements  v ia MyStand ards .................................................................... 23 
[[PBS]] – ISO 20022 System Mapping for Redemptions .................................................................. 31 
Redemption Event Messaging.................................................................................................. 32 
Redemptions Messaging Terminology....................................................................................... 32 
Redemption Messaging Events ................................................................................................ 35 
Event Descriptions ................................................................................................................ 35 
In-Scope ............................................................................................................................. 38 
Out-of-Scope ....................................................................................................................... 38 
Lottery Events ....................................................................................................................... 40 

---

## Page 4

 
 
Account Balances and Lottery Events ...................................................................................... 40 
Mess ag es fo r Lo ttery Ev ents .................................................................................................. 43 
[[BASIC]] Message Flow for Lottery Events .................................................................................... 44 
Sample Scenarios for Partial Calls .......................................................................................... 44 
Sample Scenarios for Partial Defeasance and Partial Pre-Refund ing ............................................ 53 
Non-Lottery Events ................................................................................................................ 58 
[[BASIC]] Messa ge  Flow  for  N on-Lottery Events ............................................................................. 58 
Sample Scenarios for Non-Standard, Non-Lottery Events ........................................................... 59 
Mess ag e Sub sc riptio ns  and Timing .......................................................................................... 62 
Subs c riptio n Optio ns : Lo ttery  Ev ents ....................................................................................... 62 
Subs c riptio n Optio ns : No n-Lottery Events and Maturities ............................................................ 64 
Week ly Mess ag ing Times ...................................................................................................... 65 
Holiday Processing Schedule .................................................................................................  66 
Corporate Action Notification Message .................................................................................... 67 
What is a CANO Message? ..................................................................................................... 67 
When Are CANO Messages Generated? ................................................................................... 68 
Week ly Mess ag ing Times ...................................................................................................... 69 
Holiday Processing Schedule .................................................................................................  69 
Redemption Event Types ........................................................................................................ 69 
Redemption Event Info rmatio n Co ntained  o n the CANO Mess ag e ................................................. 70 
Corporate Action Notification with Eligible Balance Message..................................................... 74 
What is a CANO-E Mes sag e? .................................................................................................. 74 
When Are CANO-E Mess ag es  Generated ?................................................................................ 75 
CANO-E Mess ag es  and  Pend ing Trad es.................................................................................. 76 
CANO-E Mess ag e Subsc riptio ns  and Timing ............................................................................ 76 
Week ly Mess ag ing Times ...................................................................................................... 76 
Holiday Processing Schedule .................................................................................................  77 
Information Contained on the CANO-E Mes s age ........................................................................ 77 
Corporate Action Movement Preliminary Advice Message ......................................................... 79 

---

## Page 5

 
 
What is a CAPA Message? ..................................................................................................... 79 
CAPA Mess ag es  fo r Lottery  vs . No n-Lottery Events .................................................................... 80 
Lottery Events ...................................................................................................................... 80 
Non-Lottery Events ............................................................................................................... 81 
When Are CAPA Messages Generated? ................................................................................... 81 
Lottery Events ...................................................................................................................... 81 
Non-Lottery Events ............................................................................................................... 82 
CAPA Mess ag e Subsc rip tions and  Timing ................................................................................ 82 
Week ly Mess ag ing Times ...................................................................................................... 83 
Holiday Processing Schedule .................................................................................................  83 
Information Contained on the CAPA Message ............................................................................ 83 
Lottery Events ...................................................................................................................... 84 
Non-Lottery Events ............................................................................................................... 86 
Corporate Action Movement Preliminary Advice Cancellation Message ...................................... 87 
What is a CAPC Message? ..................................................................................................... 87 
When Are CAPC Mess ag es  Generated ? ................................................................................... 88 
Lottery Events ...................................................................................................................... 88 
Non-Lottery Events ............................................................................................................... 88 
CAPC Mess ag e Subsc rip tio ns  and Timing................................................................................ 89 
Week ly Mess ag ing Times ...................................................................................................... 89 
Holiday Processing Schedule .................................................................................................  89 
Information Contained on the CAPC Message............................................................................ 90 
Corporate Action Movement Confirmation Message .................................................................. 91 
What is a CACO Message? ..................................................................................................... 91 
When Are CACO Messages Generated? ................................................................................... 92 
CACO Mess ag e Subs c rip tio ns and  Timing ............................................................................... 92 
Week ly Mess ag ing Times ...................................................................................................... 93 
Holiday Processing Schedule .................................................................................................  93 
Information Contained on the CACO Message ........................................................................... 94 

---

## Page 6

 
 
Corporate Action Event Processing Status Advice Message ...................................................... 97 
What is a CAPS Message? ..................................................................................................... 97 
When Are CAPS Messages Generated? ................................................................................... 98 
CAPS Mess ag e Subsc rip tions and  Timing ................................................................................ 98 
Week ly Mess ag ing Times ...................................................................................................... 98 
Holiday Processing Schedule .................................................................................................  99 
Information Contained on the CAPS Message ............................................................................ 99 
Appendix A: Message Scenarios ............................................................................................ 102 
Messaging Scenarios for Lottery Events .................................................................................. 102 
Sc enario  1: Partial Call (Bas ic ) ............................................................................................. 102 
Scenario 2: Cancellation of a Partial Call (Pre-Lo ttery ) .......................................................... 104 
Scenario 3: Cancellation of a Partial Call (Pre-Allocation) ...................................................... 105 
Scenario 4: Cancellation of a Partial Call (Same-Day / Post-Allocation).................................... 106 
Scenario 5: Cancellation and Re-Run of a Partial Call (Pre-Lo ttery )......................................... 108 
Scenario 6: Cancellation and Re-Run of a Partial Call (Post-Lotter y, Pre-Allocation) .................. 110 
Scenario 7: Cancellation and Re-Run of a Partial Call (Post-Allocation) ................................... 112 
Messaging Scenarios for Supplemental Lotteries ...................................................................... 115 
Scenario 8: Supplemental Lottery....................................................................................... 115 
Scenario 9: Supplemental Lottery Post-Allocation .................................................................  117 
Scenario 10: Reversal / Re-Run of Original and Supplemental Lotteries .................................  119 
Scenario 11: Cancellation of Original and Supplemental Lotteries (Pre-Allocation) ................... 122 
Scenario 12: Cancellation of Original and Supplemental Lotteries (Same Day / Post-Allocation) 124 
Scenario 13: Partial Call with Variable Rate ....................................................................... 127 
Messaging Scenarios for PDEF Events ................................................................................... 129 
Scenario 14: Partial Pre-Ref unding........................................................................................ 129 
Scenario 15: Partial Pre-Ref und ing – Supplemental (Post-Lottery) ........................................ 131 
Scenario 16: Cancellation of a Partial Pre-Ref und ing  (Pre-Lo ttery ) ........................................ 133 
Scenario 17: Cancellation of a Partial Pre-Ref und ing  (Pos t-Lottery) ....................................... 134 
Scenario 18: Partial Defeasance ...................................................................................... 135 

---

## Page 7

 
 
Scenario 19: Partial Defeasance Supplemental Lottery (Pre-Lo ttery ) ..................................... 137 
Scenario 20: Partial Defeasance Supplemental Lottery (Post-Lottery) .................................... 138 
Scenario 21: Cancellation of a Partial Defeasance (Pre-Lo ttery )............................................ 140 
Scenario 22: Cancellation of a Partial Defeasance (Post-Lottery) .......................................... 141 
Scenario 23: Concurrent Late Partial Calls......................................................................... 142 
Scenario 24: Concurrent Partial Calls (No Contra-[[CUSIP]]) .................................................... 144 
Messa gin g Scenarios for  N on-Lottery Events ........................................................................... 146 
Scenario 25: Full Call ..................................................................................................... 146 
Scenario 26: Cancellation of a Full Call (Pre-Allocation) ....................................................... 147 
Scenario 27: Cancellation of a Full Call (Post-Allocation) ..................................................... 148 
Scenario 28: Cancellation and Re-Run of a Full Call (Pre-Allocation) ..................................... 150 
Scenario 29: Cancellation and Re-Run of a Full Call (Post-Allocation).................................... 152 
Scenario 30: Maturity...................................................................................................... 154 
Scenario 31: [[UIT]] Termination .......................................................................................... 155 
Scenario 32: Full Pre-Ref unding....................................................................................... 156 
 
 

---

## Page 8

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
An Introduction to ISO 20022 Mess aging 8 
AN INTRODUCTION TO ISO 20022 MESSAGING 
What is ISO 20022 Messaging? 
ISO 20022 is an international messaging standard that is designed to simplify global business 
communication by creating a common language for communicating financial information that is 
unrestricted by national borders or regional conventions. 
Even though the Depository has maintained its own proprietary formats for many years, [[DTCC]] 
recognized that it needed to respond to an evolving business environment and to accommodate an 
increasingly global investment business. [[DTCC]]'s clients and customers had expanded their businesses 
throughout the world and wanted to streamline, as much as possible, the standards and formats used to 
communicate. ISO 20022 meets those needs and offers a host of benefits. 
[[DTCC]] is therefore moving all of its corporate actions announcements and processing files from 
proprietary formats to this external, international format. 
 
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
 
Benefits of Using ISO 20022 for Redemptions Processing 
ISO 20022 messaging facilitates logical, streamlined handling via straight-through processing of both 
lottery and non-lottery  ev ents. 
The assignment of a single Event [[ID]] enables you to follow the results of that event from its 
announcement, through lottery results, to the allocation of cash, [[securities]], or cash and [[securities]].  
Through the realignment of ISO messaging functions to redemption event processing, [[DTC]] is also able to 
communicate non-standard processes such as reversals or recissions. Messages can now explain where 
you are in the process flow of an event. 

---

## Page 9

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
An Introduction to ISO 20022 Mess aging 9 
Non-lottery events are also handled simply and easily. A single Event [[ID]] follows the event from 
announcement, through projection, to allocation.  
 
How Can I Learn More? 
Visit the Corporate Actions area of the [[Asset]] Services Learning Center at 
https://dtcclearning.com/products-and-services/[[Asset]]-services.html to view a wealth of business and 
technical information about the initiative, including the Benefits page and video, a Getting Started section, 
and a Readiness Checklist that provides you with a convenient method for determining your 
organization’s ability to begin processing ISO 20022 messages. 

---

## Page 10

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
An Introduction to ISO 20022 Mess aging 10 
 
 
The Learning Center also contains introductory videos, extensive documentation, a link to FAQs, and 
further information regarding ISO 20022 messages and message scenarios. 
Note that you need to log in to see the full range of information available to you. First-time users should 
click Register Now in order to create an account. You need to be registered in order to view the Learning 
Center.


---

## Page 11

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Messaging for Redemptions 11 
Introduction to Messaging for Redemptions 
Corporate Actions Messages in the Redemptions Lifecycle 
There are eight types of messages in the ISO 20022 group that pertain to redemption events: 
 
• Corporate Action Notification (CANO) 
• Corporate Action Cancellation Advice (CACN) 
• Corporate Action Notification with Eligible Balance (CANO-E) Lottery events only 
• Corporate Action Movement Preliminary Advice (CAPA) 
• Corporate Action Movement Preliminary Advice Cancellation Advice (CAPC) 
• Corporate Action Movement Confirmation (CACO) 
• Corporate Action Movement Reversal Advice (CARE)1 
• Corporate Action Event Processing Status Advice (CAPS) 
 
The messages illustrate the corporate action event information, record date position capture (for lottery 
events), lottery results, projected allocations, canceled projections, allocations, post-allocation 
adjustments, unallocated positions, and same-day payable date reversals. 
Note that these messages work differently for Redemptions, especially for lottery events.  
• The CANO-E (sent on publication date -1) provides a pre-lottery balance before a lottery has 
been run. 
 
1 CARE messages will be accommodated in ISO 20022 messaging for Redemptions at a later date. 


---

## Page 12

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Messaging for Redemptions 12 
• The CAPA message provides information for lottery results, showing what position was 
affected (“called”) and unaffected (“remaining”) by the lottery. It explains the lottery results 
and, based on affected position, projects the security or cash movements that you will 
receive. 
For example, if a CANO-E informs you that you have a pre-lottery eligible balance of 1000 units, the 
CAPA might inform you that, based on the original eligible balance, you were called on 100 units (affected 
balance). 900 units are remaining (unaffected balance). You can expect to receive a payout based on 
your affected position of 100 units. 
All of the messages involved in this process are contingent upon the client having an eligible balance in 
the event. Unless you have an eligible balance, you will only see the announcement message for the 
event. Please note that all participants eligible for a lottery-based event will receive a CAPA lottery results 
message regardless of whether they were affected by the lottery. 
How to Read an MX Identifier 
The MX Identifier identifies the business area, message [[ID]], and version of an ISO Message. 
As an example, for the identifier seev.036.002.06: 
• The first four alphabetic characters (“seev”) identify the business area. In this case, it is 
“[[securities]] Events.” You can see the full list of business areas on the ISO 20022 Web site at 
http://www.iso20022.org/documents/general/ISO20022_BusinessAreas.pdf. 
• The next three characters (036) are the message identifier. The message in this example is a 
CACO message. 
• The next three characters (002) are the “variant” identifier. Since “001” is always the main 
ISO message, “002” would be the second variant (and the one that is compatible with ISO 
15022). [[DTCC]] is using the second variant in order to comply with the industry’s requirement 
that the ISO 20022 messages we generate be backward compatible with ISO 20022. 
• The last two characters (06) are the “version.” In this example, this is the sixth version of this 
message, representing SR 2015. Please note that the final two digits have the potential to 
change with each release. 
For your coding purposes, be sure to consult the latest documentation for the most 
current version number. 
Supplementary Data and Message Extensions 
The [[DTCC]] implementation of ISO 20022 will make use of an ISO 20022 concept of supplementary data, 
also called “extensions.” 
Certain [[DTCC]] corporate actions elements are not covered by the standard ISO messages. These 
elements are implemented using the supplementary data components. The data fields within the 
supplementary data have been modeled using the ISO 20022 principles and will reside in the ISO 20022 
data dictionary. 

---

## Page 13

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Messaging for Redemptions 13 
In terms of Redemptions messaging, the supplementary data is provided in message extensions. These 
extensions allow [[DTCC]] to provide an agreed-upon and machine-readable structure within the messages 
for those data elements that have not been globally agreed to form part of the main message. Note that 
the structure of the extension must be validated by the ISO community and registered within ISO 20022, 
and this process includes the addition of the elements to the ISO 20022 data dictionary. This allows for 
improved interoperability while avoiding an impact on the messages themselves which may have been 
implemented in other communities.

---

## Page 14

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 14 
Data Dictionaries, Scenarios, Message Usage Guidelines, and Event Templates 
Scenarios and data dictionaries can be found on [[DTCC]]’s Web site at http://www.[[DTCC]].com/[[settlement]]-
and-[[Asset]]-services/corporate-actions-processing/scenarios. 
Message Usage Guidelines can be found with their associated message specifications at 
http://www.[[DTCC]].com/[[settlement]]-and-[[Asset]]-services/corporate-actions-processing/iso-20022-messaging-
specifications. 
 
Redemptions Data Dictionaries 
The Corporate Actions Data Dictionary is central to the new ISO standard. It is one of the main 
components of the new data model that provides clients with increased operability within their own 
systems and with other external processes. 
The data dictionary provides an overview of each event type in the ISO 20022 model and its relationship 
to existing [[DTC]] event types (function codes). It also provides a list of data elements, their level, and a 
cross reference from existing [[DTC]] elements to the new ISO 20022 element. This allows clients to map 
elements from [[DTC]]’s legacy function code-based data model to the new ISO 20022 messages. An 
indication is also provided as to the level of compliance with global and U.S. industry norms. 
The data dictionaries are presented in a series of Excel spreadsheets. Each spreadsheet describes the 
data model as it relates to announcements, the corporate actions lifecycle, and instructions; each one 
describes the new data model, its relation to the existing [[DTCC]] legacy model, and ISO standards.  
Each spreadsheet contains a number of tabs. [[DTCC]] recommends that clients familiarize themselves with 
the tabs in each applicable data dictionary, and the type of information contained on each. Note that 
updates, adds and deletes to any item in the dictionary are noted in the dictionary itself. 
The spreadsheets that apply specifically to Redemptions include the Announcements and the 
Entitlements and Allocations data dictionaries. 
 
Announcements Data Dictionary 
The Announcements Data Dictionary includes the following tabs. It is recommended that users start with 
the Legend tab as it provides a description of the information provided in the spreadsheet’s remaining 
tabs, which offer specific data element detail. 
• Legend. Start here to learn about the column names used throughout the data dictionary. 
• Events. View a complete list of [[DTCC]]-defined event types, sub-ev ent types, and their 
corresponding ISO codes. This is a good way to see the relationship between the [[DTCC]] 
event structure and the equivalent ISO information. 
• Event Descriptions. These definitions explain all of the events covered in the previous tab. 
• Elements. A list of data elements contained in the new model. 

---

## Page 15

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 15 
• Options. A list of [[Option]] types and descriptions. 
• Payouts. A list of payout types, payout descriptions, and associated ISO tags. 
• Security Rates. A list of payout indicators for [[securities]] that define products, processing, 
valid amounts, and event/payout security classes. 
• Cash Rates. A list of payout indicators for cash that define rules and event groups. 
• Event Statuses. A list of status codes for each event. 
• [[Asset]] Types. A list of sub issue type codes and descriptions. 
• NRA Tax Codes. A list of NRA tax codes and descriptions, mapped to ISO Income Type 
codes. Note that this sheet is not applicable to Redemptions. 
The tabs that you will find the most helpful are the Events tab and the Elements tab. You can sort the 
columns on these sheets to display information that is relevant to redemption events. 
 
Using the Events Tab 
Sorting columns N through Q is the easiest way to limit the information for Redemptions. In particular, 
column Q allows you to display redemption events only. 
 
1. Click the arrow in the Q column, Extended Event Group. 
2. Uncheck “Blank” so that only “REDM” is selected. 
3. Click OK. 
The sheet is then limited to redemption events only. Column A lists all of these events. 


---

## Page 16

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 16 
 
4. Use the scrollbar at the bottom right of the Excel window to view all of the columns on the 
sheet. 
Column O denotes the extended event types that differentiate partial defeasance, partial pre-refunding, 
and full defeasance for PDEF events: 
• FLPR. Full Pre-Refunding. 
• PDEF. Partial Defeasance. 
• PPRE. Partial Pre-Refunding. 
• TMTN. Termination. 
 
The Elements tab is also useful for understanding the contents of Announcements messages for 
redemption events.  
Column M denotes the elements that specifically refer to Redemptions. By removing the rows that [[DO]] not 
have a check in this column, you can view only those message elements that apply to Redemptions 
announcements. 


---

## Page 17

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 17 
 
1. Click the arrow in the M column, Redemptions. 
2. Uncheck “Blank” so that only the check symbol is selected. 
3. Click OK. 
The sheet is then limited to elements that apply to redemption events. Column C, Data 
Element Name, lists all of these elements. 


---

## Page 18

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 18 
 
4. Use the scroll bar to see all of the columns on this sheet. 
 
Entitlements and Allocations Data Dictionary 
The Entitlements and Allocations Data Dictionary includes tabs for each ISO lifecycle message type. The 
tab contains a spreadsheet of data elements contained in that message type.  
Each row presents an element as well as its associated information: an explanation of what it is, which 
event group (Distributions, Redemptions, Reorganizations) it is applicable to, and the name of the legacy 
[[CCF]] file this information can be traced back to. Notes are included for both Distributions and 
Redemptions where applicable.  
In addition to specific message information, separate sheets list the reason codes for CAPA, CACO, and 
CAPS messages, as well as sub reason codes for CAPA and CACO messages. 
 
  


---

## Page 19

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 19 
You can limit each message type to display elements that apply only to redemption events. 
 
1. Click the arrow in the G column, Redemptions. 
2. Uncheck “Blank” so that only “Y” is selected. 
3. Click OK. 
The sheet is then limited to message elements that apply to redemption events. Column A, 
ISO Message Field Name, lists all of these elements. 


---

## Page 20

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 20 
 
4. Use the scroll bar to see all of the columns on this sheet. 
 Click another tab on the bottom to see information for a different message type. You can limit 
all message sheets using Column G. 
 
For additional details, see the User Guide: ISO 20022 Messaging for Distributions Entitlements and 
Allocations, [[DTCC]] Corporate Actions. 
 
Using the Data Dictionary to Map from [[CCF]] to ISO 20022 
To determine the mapping of a legacy file field to the corresponding ISO message type, field, and tag, 
use the value from the Legacy Mapping Spreadsheet (CA Data Element Names) and cross-reference 
this value with the same data element name in the Corporate Actions Data Dictionary. 
The Corporate Actions Data Dictionary provides the corresponding ISO message type, field, and tag in 
the Corporate Actions ISO Message Specifications, which represents the ISO message standards 
used to communicate with [[DTCC]]. 
 


---

## Page 21

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 21 
For example, to find the corresponding ISO 20022 message path, extension, field, or XML tag for the data 
field “Ex-[[Dividend]] Date” in the legacy [[CCF]] file DIVANN, you would: 
1. Open a Legacy mapping spreadsheet (here, “Divann”). 
2. Go to the Legacy mapping tab (“Divann”) and look under the column heading CA Data 
Element Name (2010). Here, we can see that the value is “Ex Date.”  
 
3. To look up the ISO 20022 path and extension, look in the Announcements Data Dictionary’s 
Elements tab. Find the value of “Ex Date” in the Data Element Name column.   
4. Scroll to the right to see all information associated with “Ex Date.”  
The path value, for example, is detailed in the Path column, and the value is 
“CorporateActionDetails/DateDetails/ExDividendDate.” 
 
5. The extension value, when applicable, is detailed in the Extension columns.  
In this instance, it is blank because this data element is not a [[DTC]]-specific data element. 
 
Redemptions  Message Usage Guidelines 
Message Usage Guidelines (MUGs) define the guidelines for [[DTCC]]’s restrictions of the base standard 
message for each ISO 20022 message. They provide the ability to show all required and optional fields 
utilized in the message. In addition to usage rules, comments and synoyms help describe each data 
element and its context in relation to the [[DTC]] data model or legacy [[CCF]] file.  
The MUGs are saved as PDF documents that can be found in the separate Zip files containing the ISO 
20022 message specifications for both Announcements and Entitlements and Allocations. Each MUG 
refers to a specific message (CANO-E, CAPA, etc.) or message extension.  
The MUG can be used to cross-reference an ISO 20022 component with its [[DTCC]] name. Each [[DTCC]] 
element’s name, definition, and usage rules listed in the dictionary are noted with the corresponding ISO 
element in this document. 


---

## Page 22

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 22 
 
Redemptions Scenarios 
The Redemptions scenarios spreadsheet contains an array of event type tabs. The spreadsheet on each 
tab presents at least one scenario for each event type. The scenario contains the major data elements for 
the event type and the values you can expect to see for each. 
 
Redemption Event Templates 
Introduction 
In addition to providing message usage guidelines for announcements, you can now see a subset of the 
announcements data that applies to redemption events only.  
These redemption event templates restrict the announcements information at the redemption event level 
(such as partial call, full call, etc.) at both the core message and extension message levels.  
This allows you greater insight into the contexts of redemption events. You can see relevant metadata 
about these elements: rules and comments that are specific to each element’s usage during a specific 
event, as well as annotations and synonyms that explain where each data element came from and the 
legacy data attribute name for each. 
To view these event templates, please visit Swift’s My Standards Web site at 
https://www2.swift.com/mystandards/. 
 
 
  

---

## Page 23

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 23 
Viewing Message Data Elements via MyStandards 
Click Homepages to reach the list of organization standards. 
 
 
 
  


---

## Page 24

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 24 
Click [[DTCC]] to reach [[DTCC]]’s set of standards. 
 
 
  


---

## Page 25

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 25 
Click Usage Guidelines to reach the list of available standards and click the link for the message 
collection you want to view. 
Note that you can view message groups for different event types. For example, you can view CANO 
guidelines for Distributions and Reorganization events as well as Redemptions. 
 
 
 
  


---

## Page 26

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 26 
The collection contains a list of event types for this particular message. Each listed event type contains a 
subset of the data elements from the general message. 
Here, we see a list of the restricted subsets of the general CANO message that apply to particular 
redemption event types.  
Note that each message type is followed with an “SD” entry for each type.  
• The initial listing is for the core message. 
• The “SD” listing that follows refers to the message extension. It contains the supplemental 
data for each message type. 
 
 
 
Click the link for the event template that you want to view.  
  


---

## Page 27

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 27 
You are brought to the Description tab for that template. Here, you can read a summary of the type 
of information covered in this event template. 
 
 
 
Click the Content tab to view the template data. 
The Content page contains the data elements as they pertain to this message for this event type. 


---

## Page 28

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 28 
 


---

## Page 29

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 29 
a) Click the View only restricted elements and Hide removed elements check boxes to limit your 
view to only those elements that actively pertain to this event type. 
b) Orange triangles indicate that there is metadata available for this element. Click the element to 
view this additional information. 
Gray triangles indicate that a change has been made to this element.  
c) Click the + and – signs to drill down into data elements. 
d) When you click on an element name, its metadata appears to the right of the element list. 
• The top blue line states the full name of the element. 
• Any Rules that apply to this element are listed out and clearly defined. 
• An Annotation specifies the [[CCF]] origin for the element. In this example, you can see 
that the “Results Publication Date” has been used for Redemptions in five “REDEM” [[CCF]] 
files.  
• A Comment presents any useful details about this element that are not covered by a rule 
or a definition. 
• A Synonym tells you what this element was named when it was used in another context 
at [[DTCC]]. In this example, you can see that this same element was previously referred to 
by two other names. 
• Multiplicity tells you the number of times that an element can be used. This indicator 
defines the minimum and maximum number of times that the element may be used in a 
message. 
o The initial number is the “Min” value. This defines whether the element is optional 
or required in the message. A value of “0” means that the element is optional; “1” 
means that the element is mandatory. 
o The second number (or “Max” value) refers to repeatability. A value of “0” means 
that the element can appear only once in the message. An asterisk (*) in this 
position means that the element may repeat any number of times.  
• The Type specifies the format for this element. 
• The Definition provides a glossary-level explanation for this element. See the Comments 
list (above) for further hints about specific usage. 
• The XML Tag tells you what the element is named in the XML message. As opposed to 
the real name (provided at the top of this list), the tag delineates this element in the code 
for this message. 
• When enabled, the Comments area allows users with the appropriate access level to 
comment on this data element. 
e) Click Export As to export this message template in XML, Excel, or PDF format. 

---

## Page 30

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Scenarios, Data Dictionaries, and Ev ent Templates 30 
f) Click the Base Message link to access the original, unrestricted message. In this example, the 
link will bring you to the Description page for the general CANO message. It will not be limited by 
event type or usage.

---

## Page 31

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
[[PBS]] – ISO 20022 System Mapping for Redemptions 31 
[[PBS]] – ISO 20022 System Mapping for Redemptions 
These [[PBS]] functions will be handled by the following ISO 20022 messages at the indicated points in the 
Redemptions life cycle. 
Process Announcement 
Process Lottery Process Projections Allocation 
Redemption 
Deposits/ 
[[custody]] 
Processing 
Message 
Type 
[[CCF]] ISO [[CCF]] ISO [[CCF]] ISO [[CCF]] ISO [[CCF]] only 
Publication 
Date 
REDEM 
G, X, A 
CANO 
CACN 
n/a  
 
CANO-E 
 
CAPA 
(NEWM) 
CAPC 
n/a n/a n/a n/a RDCERT 
Mainline 
(Lottery) 
Date 
n/a CANO 
CACN 
(Announce-
ment 
updates)  
REDEM L 
Reds sends 
message to 
ATP for 
security 
movement for 
segregation to 
26/28 account  
n/a n/a n/a n/a n/a 
Payment 
Date – 5 
([[CCF]]) or  
PD – 7 
(ISO)  
through  
Payment 
Date – 1  
n/a CANO 
CACN 
(Announce-
ment 
Updates)  
n/a n/a CASHPRJ 
CASHRPJ 
CAPA 
(REPL) 
CAPC 
(REPL) 
n/a n/a n/a 
Payment 
Date 
n/a n/a n/a n/a n/a n/a CASHSET 
CSHTA-G 
CSHRAL 
CACO  
 
 
CSHRAL 
Post-
Payment 
Date 
n/a n/a n/a n/a n/a n/a CSHUNL, 
CSHEU-1 
CSHDUN 
CACO 
CAPA (REPL) 
for post-
payment 
reversals 
CAPS 
(Unallocated 
redemption 
proceeds night 
of Payment 
Date 
CACO 
(Redemption 
Deposits) 

---

## Page 32

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Event Messaging 32 
Redemption Event Messaging 
In the initial phase of the project, only mandatory redemption events will be handled. Redemption events 
involving a choice of options will be addressed during the reorganization processing phase of the 
Corporate Actions Transformation initiative (please see the Out of Scope items for reference).  
The ISO 20022 messages for Redemptions are the same that are used in the Entitlements and 
Allocations process for Distribution events, however: 
• The messages have content specific to redemption events. 
• Some of the messages are used for a different purpose. For example, the CAPA message is 
used in Redemptions for communicating lottery results. In Distributions, however, it is used 
for communicating projected balances, payments, and allocations. 
Redemptions Messaging Terminology  
 
Term Definition 
Affected Balance The account-level called quantity of a lottery event. The portion 
of the account eligible balance that has been affected (“called”) 
by a lottery. 
Corporate Action Event 
Type Code (CAEV) 
The event type of the corporate action. The CAEV codes used 
for redemptions messaging are located here. 
For PDEF events, the event type code plus the extended 
[[DTCC]] extended event type code must be used together. For 
example, if the event type is PDEF, and the extended [[DTCC]] 
event type is PPRE, this signifies a partial pre-refunding.  
For redemptions-based messaging, the CAEV code identifies 
the SWIFT event type. 
Corporate Action Event [[ID]] 
(CA [[ID]]) 
The unique Corporate Action Event [[ID]] for each event with the 
exception of a supplemental lottery. A supplemental lottery will 
carry the same CA [[ID]] as the original lottery. 
Concurrent Call The situation in which two partial calls are announced with the 
same Redemption and/or Publication dates, but with different 
rates. A contra [[CUSIP]] is required in this scenario (previously, a 
contra [[CUSIP]] was only required for late announcements. 
Otherwise, the second redemption will be processed once the 
first redemption is mainlined).  
Contra [[CUSIP]] Some partial calls (e.g., concurrent calls, among others) [[DO]] not 
segregate the called portion into a “Call with Interest” or “Call 
without Interest” account. The called portion is instead 

---

## Page 33

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Event Messaging 33 
Term Definition 
segregated into the free account under the contra [[CUSIP]] that 
is assigned to the issue at the time of the lottery. 
Defeased / Non-Defeased 
Indicator 
This is an indicator type that appears under the New Security 
Issuance Indicator field. It accounts for two of the possible four 
values for a new security issue.  
It is used for partial defeasement event types, in which new 
[[securities]] are issued for the portion defeased. It indicates which 
CUSIPS will be defeased (the new [[CUSIP]]) and which CUSIPs 
will be non-defeased (the original [[CUSIP]]). 
Event Stage This is a code that defines a non-standard lottery process. It is 
used in conjunction with the Lottery Type field.  
“FULL” is the only value for this field that applies to 
Redemptions processing. It refers to the cancellation and re-
run of an original lottery or an original and supplemental lottery. 
A subsequent lottery will be performed under a new event. 
Final Paydown The final distribution of principal due on a security, typically 
CMOs. 
Lottery Swing Date “Lottery Date” (originally “Mainline Date”). This describes the 
date on which called positions are moved into a segregated 
account or a contra [[CUSIP]]. 
Lottery Type Defines the type of lottery being run. Values are: 
ORIG The “Original Lottery” that has been 
announced for a specific amount and 
date. 
SUPP “Supplemental Lottery.” The 
supplemental or additional called 
quantity on a previously announced 
original lottery. 
  

---

## Page 34

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Event Messaging 34 
Term Definition 
New Security Issuance 
Indicator 
For partial defeasance or partial pre-refunding events, this field 
is used to indicate the type of [[CUSIP]] being issued. There are 
four possible values for this indicator: 
Defeased “DEFE.” A new security issued whereby 
funds have been placed in escrow by a 
trustee or agent on a portion of the 
outstanding balance of the original 
security on maturity date.  
Non-
defeased 
“NDEF.” A new security issued that has 
not been defeased and the maturity date 
of the underlying security is unchanged. 
Refunded “REFU.” A new security has been issued 
and refunded to an earlier maturity date. 
Non-
refunded 
“NREF.” A new security that has not 
been refunded and the maturity date of 
the of the original underlying security is 
unchanged. 
All four indicators are applicable only in the frame of a partial 
defeasance (“PDEF”) corporate action event. 
Obligated Balance For partial call lottery (DRAW) events, that balance which has 
been called (“affected”) by lottery (based on the record date 
eligible balance) but is not available for redemption. This 
balance must be returned to [[DTCC]]. 
For instance, if you have been called for 400 units but only 
have 300 available on hand, you have an obligated balance of 
100 units.  
Redemption Processing 
System 
(REDS) 
[[DTC]]’s internal [[PTS]] function that was used to create all 
Redemption-related events (with the exception of maturities). 
Refunded / Non-refunded 
Indicator 
This is an indicator type that appears under the New Security 
Issuance Indicator field. It is used for partial prerefunded event 
types and indicates which CUSIPS will be refunded (CUSIPs 
bearing an earlier maturity date) and which CUSIPs will be non-
refunded (CUSIPs bearing the same maturity date as the 
original event [[CUSIP]]).  

---

## Page 35

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Event Messaging 35 
Term Definition 
Reorg Inquiry for 
Participants 
(RIPS) 
[[DTC]]’s function on the [[participant]] Terminal System ([[PTS]]) that 
communicates all redemption announcement and allocation 
information. 
Unaffected Balance The portion of the account eligible balance that has not been 
affected (“called”) by a lottery. 
 
Redemption Messaging Events 
This phase of the Corporate Actions Transformation effort will cover the majority of redemption event 
types. Some redemption events will be out of scope until the reorganization processing phase.  
 
Event Descriptions 
Event Name Event 
Description 
Sub Event 
Name 
Sub Event Description 
[[default]] 
(Interim / Final) 
A notice of failure by the 
[[issuer]] to honor 
commitments made within 
the terms of the issued 
security. It usually relates 
to making timely payments 
of interest and principal as 
they come due. A p ayment 
may be made in lieu of 
reinstituting the original 
payments. 
  
  Interim 
Payment 
Identifies an event that 
includes notification of an 
interim payment in lieu of the 
original commitment. 
  Final Payment Identifies an event that 
includes notification of a final 
payment in lieu of the original 
commitment. 

---

## Page 36

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Event Messaging 36 
Event Name Event 
Description 
Sub Event 
Name 
Sub Event Description 
Final Paydown 
(CMO) 
The final distribution of 
principal due on a security, 
typically CMOs.  
  
Full Call The security is redeemed 
for cash in its entirety on a 
date that is prior to the 
maturity date. The holders 
receive the principal 
amount of the security. 
  
Full Pre-
Refunding 
The exercise of a privilege 
by the [[issuer]] to repay, in 
full, any debt security prior 
to maturity when the [[issuer]] 
deposits assets in trust. 
This irrevocably restricts 
their use to satisfaction of 
the debt. 
  
Maturity The final repayment, 
usually in cash, by an 
[[issuer]] for the entire issue 
or for remaining 
outstanding [[securities]] of a 
specific security on a 
specified date. 
  
  - Non-specific maturity event. 
  [[securities]] Identifies an event where the 
payment will be made in the 
form of [[securities]]. 
Partial Call [[securities]] are redeemed 
by the [[issuer]] for cash, in 
part, before their 
scheduled maturity date. 
The outstanding amount of 
[[securities]] will be 
proportionally reduced 
  

---

## Page 37

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Event Messaging 37 
Event Name Event 
Description 
Sub Event 
Name 
Sub Event Description 
based on a specific 
percentage of holding. A 
lottery may be run where 
pooled [[securities]] are held. 
Partial 
Defeasance 
The [[issuer]] sets aside cash 
in escrow to pay off a 
portion of the issue before 
the maturity date. New 
[[securities]] are issued for 
the portion defeased. 
  
Partial Pre-
Refunding 
Similar to a full pre-
refunding, a partial pre-
refunding is the exercise of 
a privilege by the [[issuer]] to 
repay, in part, any debt 
security prior to maturity 
when the [[issuer]] deposits 
assets in trust. This 
irrevocably restricts their 
use to satisfaction of the 
debt. New [[securities]] are 
issued for the portion 
prerefunded. 
  
Termination 
([[UIT]]) 
A security, usually a form 
of a derivative (e.g., [[ADR]] 
or [[UIT]]), for which the 
agent or [[issuer]] has 
decided to terminate the 
derivative based on a 
change to the underlying 
security/[[securities]] or a 
change in strategy. 
  
  - Non-specific termination 
event. 

---

## Page 38

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Event Messaging 38 
Event Name Event 
Description 
Sub Event 
Name 
Sub Event Description 
  [[ADR]] Identifies when the event 
security is an [[ADR]]. 
  GDR Identifies when the event 
security is a GDR. 
 
In-Scope 
Event Name Function Code SWIFT Event 
Type 
[[DTC]] Extended 
Event Type 
MAN / VOL / 
CHOS 
Partial Call 74 (Corporate) 
76 (Muni) 
DRAW  MAN 
Full Call 75 (Corporate) 
77 (Muni) 
MCAL  MAN 
Full Pre-
Refunding 
77P, 
77L (Late) 
PDEF FLRP MAN 
Final Paydown 
(CMO) 
89 MCAL  MAN 
Maturity 70 (CD) 
75M (Corporate) 
77M (Muni) 
REDM  MAN 
[[default]] 
(Interim / Final) 
86P (Interim) 
86F (Final) 
DFLT  MAN 
Partial 
Defeasance 
76D PDEF PDEF MAN 
Partial Pre-
Refunding 
76P PDEF PPRE MAN 
Termination 
([[UIT]]) Term 
87F REDM TMTN MAN 
 
Out-of-Scope 
Event Name Function Code SWIFT Event 
Type 
[[DTC]] Extended 
Event Type 
MAN / VOL / 
CHOS 
Maturity for 
[[securities]] 
93 REDM  MAN 

---

## Page 39

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti on Event Messaging 39 
Event Name Function Code SWIFT Event 
Type 
[[DTC]] Extended 
Event Type 
MAN / VOL / 
CHOS 
Convertible 
Full Call 
Redemption 
69 MCAL  CHOS 
Convertible 
Maturity 
69 REDM  CHOS 
Partial Call 
Conversion 69P (Convertible 
Partial Call) 
74 (Corporate 
Partial Call) 
54 (Conversion) 
MCAL  CHOS 
Partial 
Mandatory Put 
with [[Option]] to 
Retain 
65 (Partial 
Mandatory Put 
No Retainment) 
65R (Put 
Retainment) 
74 (Corporate 
Partial Call) 
76 (MUNI Partial 
Call) 
BPUT  CHOS 

---

## Page 40

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 40 
Lottery Events 
ISO messaging for lottery events conforms to global market practice. Lottery events are announced in 
real time, and recissions and reversals are incorporated into the ISO workflow. 
Lottery events include: 
• Partial call, 
• Partial defeasance, and 
• Partial pre-refunding. 
Partial calls result in cash paid for [[securities]] that are redeemed in part.  
Partial defeasances and partial pre-refundings both result in the creation of new [[securities]]. Redemptions 
for these two lottery types are made into these new [[securities]] rather than in cash. 
 
Account Balances and Lottery Events 
The ISO 20022 messages contain several balance types to explain your position as it is affected by a 
corporate actions event. 
Term Definition 
Eligible Balance On the CANO-E, this is the amount eligible to be called based 
on the client’s record date position.  
For supplemental lotteries, the eligible balance will be based on 
the unaffected position of the original lottery. 
[[settlement]] Position The [[settlement]] position will normally equal your eligible 
position.  
As the balance maintained within your general position, 
[[settlement]] position may not equal eligible position if position 
has moved subsequent to record date capture.  
For lottery-based CAPA messages, this will be your remaining 
unaffected position. For situations in which an obligated 
position occurs due to going short, the [[settlement]] position will 
be indicated by a short (SHOR) distinction. 
Original Position Original position is generally equal to your eligible position. It 
will remain constant for the life of the event. On a supplemental 
call, the original position will indicate what your original balance 
was before the original call took place. 
Unaffected Balance This is the portion of the eligible position that is not called by 
the lottery. For partial pre-refundings, this is the non-refunded 

---

## Page 41

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 41 
Term Definition 
balance; for partial defeasements, this is the non-defeased 
balance. 
Affected Balance This is the portion of the eligible position that is called by the 
lottery. For partial pre-refundings, this is the refunded balance; 
for partial defeasements, this is the defeased balance. 
Obligated Position Obligated position occurs when the affected balance is greater 
than the settled position. This can happen when a call notice is 
received late and the prior record date position is greater than 
what is currently settled.  
 
The balances appear in the Redemptions messages as follows: 
 
 
 
• The eligible balance is consistent through the CANO-E and CAPA.  
• The unaffected balance from the CAPA becomes the eligible balance in a supplemental 
lottery.  
• The affected and unaffected balances are reported on the CAPA.The original position is the 
same through the event’s life cycle. 
• The supplemental call is processed under the same event [[ID]] as the original call. 
 
For example, Client A has an original eligible balance of 100. A standard lottery is run, followed by a 
supplemental lottery: 
  


---

## Page 42

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 42 
 
  
The eligible balance, settled position, and original position as stated on the CANO-E are all 100. After the 
lottery is run, 40 of the original 100 [[shares]] are affected by the lottery; 60 of the 100 [[shares]] are 
unaffected. After the first lottery settles, the unaffected balance of 60 becomes the new eligible balance 
for the supplemental lottery. 
 
In the next example, a late call was announced with a prior publication date.  
 
 
 
The client has an original eligible balance of 200 [[shares]], based on the prior publication date. However, 
the client only has 50 [[shares]] on hand in settled position. As a result of the lottery, the client was called for 
80 [[shares]] (affected balance) out of the original 200. This leaves the client with a settled position of -30, 
and therefore an obligated balance of 30 (the absolute value of the settled position).  
 
  


---

## Page 43

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 43 
Messages for Lottery Events 
CANO-E Messages 
CANO-E messages in their Redemptions usage only apply to lottery events: this pre-lottery balance 
notification is new to redemptions event handling. CANO-E messages specify your eligibility in an event 
before the lottery is run. 
View the CANO-E section for further information. 
 
CAPA Messages for Lottery Events 
CAPA messages for lottery events inform you whether your position has been called or not.  
• If your position has been called, the CAPA outlines your affected and unaffected position, the 
payment you can expect, and when you can expect it.  
• If your position was not called in the lottery, you will still receive a CAPA lottery results 
message stating zero affected balance.  
• If a supplemental call is announced, it will be processed under the same Corporate Action 
Event [[ID]] (COAF) but with a supplemental lottery type.  
CAPA lottery result messages are sent five times per day.  
View the CAPA section for further information. 
 
CAPC, CACO, CARE, and CAPS Messages for Lottery Events 
The CAPC, CACO, CARE, and CAPS messages function the same as for non-lottery events: they 
surround the payment flow and serve the same function as in Distributions, but with the addition of 
specific fields to customize them for Redemptions usage.  
These flows [[DO]] not include exceptions such as event cancellations, lottery event reversals, supplemental 
calls, allocation reversals, unallocated funds, etc. They are meant to give the user a high-level overview 
of the message and business flows as a starting point for understanding ISO 20022 messaging. 
 
  

---

## Page 44

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 44 
[[BASIC]] Message Flow for Lottery Events 
At its simplest, the message flow for lottery events can be summed up as follows: 
 
 
1. [[DTCC]] sends a CANO to the client that announces the corporate action lottery event.  
2. On Publication Date, [[DTCC]] sends a CANO-E to inform the client of their position prior to the 
lottery being run on lottery date. 
3. [[DTCC]] sends a CAPA message to the client containing the lottery results, affected and unaffected 
positions, and projected allocation based on the lottery results. 
4. [[DTCC]] sends the client a CACO message to confirm movement of payment/allocation proceeds.  
Often, particular situations deviate from this simplified flow: exceptions such as event cancellations, 
lottery event reversals, supplemental calls, allocation reversals, unallocated funds, etc. The following 
scenarios (as well as the scenario appendix) explain these situations in greater detail.  
For specific message information, see this guide’s chapter for that message type. 
 
Sample Scenarios for Partial Calls  
This section details several of the most common process flows for redemption event messaging for partial 
calls. While these are the simplest and most likely scenarios, there are many more that might occur.  
For additional, more complex scenarios, please see Appendix A: Additional Scenarios. Note that, for 
consistency, scenarios are numbered based on their appearance in the Appendix. 
For a complete list of data elements for each message, their origins, and their usage, please utilize the 
Message Usage Guidelines available at [[DTCC]].com, the Learning Center, or My Standards at 
https://www2.swift.com/mystandards/.  
 
  


---

## Page 45

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 45 
Scenario 1: Partial Call ([[BASIC]]) 
This scenario illustrates the flow of messages that you can expect to receive for a partial call event. An 
announcement is made, your eligible balances are determined, the lottery is run, your affected balances 
and associated entitlements are determined, and your allocations are made and documented. 
 
Scenario 1: Partial Call 
 
The process starts with the Partial Call Announcement message (CANO). This message presents you 
with details about the event, including record date, [[CUSIP]], and lottery date. The Redemption [[ID]] is given 
in the message extension. 
The CANO is followed by the Eligible Balance message (CANO-E). This message provides information 
about your eligible balance prior to the lottery being run. Your total eligible balance is contained in the 
main body of the message, while additional balances describing the position you may have can be found 
in both the core message and the message extension (when applicable). You are informed of your 
eligible position based on the details of the partial call. 
  


---

## Page 46

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 46 
The CAPA message is sent after the lottery has been run. This message has two purposes. 
• First, it informs you of the [[DTC]] lottery results.  
• Based on these results, this message also explains what portion of your eligible balance was 
affected (“called”) by the lottery, and what you can therefore expect to see in cash as a result 
of this event.  
The CAPA message also specifies the payment date and payment rate (if available) in the 
credit cash movement. The message shows a debit projection of the underlying [[CUSIP]]. 
The first CAPA sent is always a CAPA NEWM, or “new message.” CAPA REPL (“replacement”) 
messages are sent if any information on the CAPA NEWM has changed, such as the rate. 
Finally, the CACO message serves as a payment confirmation for the event. On payment date, your 
underlying [[CUSIP]] is debited and cash is moved to your account. The CACO message details the 
payment information regarding the partial call as well as lottery detail. 
 
  

---

## Page 47

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 47 
Scenario 2: Cancellation of a Partial Call (Pre-Lo ttery) 
This scenario demonstrates the message flow for a situation in which an announcement was made for an 
event, but the event was canceled before the lottery was run. 
In this case, you are informed of your eligibility, but the event is canceled before any determination has 
been made regarding your affected position. 
 
Scenario 2: Cancellation of a Partial Call (Pre- Lottery) 
 
The CANO and CANO-E messages are sent out as for a [[BASIC]] partial call. However, before the CAPA 
gets sent, a CACN message informs you that the event will not take place. 
 
  


---

## Page 48

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 48 
Scenario 3: Cancellation of a Partial Call (Pre-Allocation) 
As in Scenario 2, this scenario deals with the cancellation of a partial call event. In this case, however, the 
cancellation occurs after the lottery has been run but before the cash has been allocated.  
 
Scenario 3: Cancellation of a Partial Call (Pre- Allocation) 
 
The CANO, CANO-E, and CAPA messages are sent out as for a [[BASIC]] partial call: you are not only 
informed of the event and your eligible balance, but the lottery has been run and you are informed of your 
affected balance, the rate (if known), the projected debit to your underlying [[CUSIP]], your projected 
allocation, and the payment date. 
This time, the event is canceled between the pre-advice and the allocation. Since the lottery has already 
been run and the allocation has already been projected, there are two types of cancellation messages 
that are sent. 
The Event Cancellation (CACN) message cancels the CANO message: it is sent to inform you that the 
event itself has been canceled. This refers only to the event, not to the lottery. 
The projection itself – that is, the lottery results and how they affect your position – must be canceled as 
well. The Lottery Projection Cancellation (CAPC) message retracts the CAPA: it informs you that the 
lottery results have been canceled. 


---

## Page 49

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 49 
Scenario 6: Cancellation and Rerun of a Partial Call 2 
As in Scenario 3, the event is canceled post-lottery and pre-allocation. As before, the event is withdrawn 
and must be reversed. 
Here, however, a new event will take the place of the initial event.  
 
Scenario 6a: Cancellation and Rerun of a Partial Call: 1 of 2 
 
The first portion of this cancellation happens as in Scenario 3: a CANO message announces the event, a 
CANO-E message informs you of your eligibility, a CAPA message informs you of the lottery results and 
your affected balance, and a CACN message cancels the initial event.  
The CACN, however, contains an event stage indicator that informs you that this is a non-standard lottery 
process. It is used in conjunction with the Lottery Type. The value “FULL” refers to the cancellation and 
re-run of an original lottery or an original and supplemental lottery. A subsequent lottery will be performed 
under a new event. 
 
2 Please note that all scenario numbers are consistent with the scenarios in Appendix A. 


---

## Page 50

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 50 
After the cancellation, a new event is announced via a CANO message, as was indicated by the event 
stage within the CACN message. This CANO contains the details for the replacement event. 
 
Scenario 6b: Cancellation and Rerun of a Partial Call: 2 of 2 
 
The process continues from this point as for a regular Partial Call.  
The lottery is re-run and a new CAPA is sent, informing you of the lottery results and the effect the lottery 
will have on your position and balances.  
On the new Payment Date, all allocations are made and a CACO message is sent as a payment 
confirmation for the event. On payment date, your underlying [[CUSIP]] is debited and cash is moved to your 
account.  
 
  


---

## Page 51

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 51 
Scenario 8: Supplemental Lotte ry 3 
Supplemental lotteries are additional lotteries run on an individual event when the [[issuer]] needs to call 
more of the security. They are processed under the same Event [[ID]] as the original lottery. In the event 
messages, they can be distinguished by a value of “SUPP” for the Lottery Type element.  
The eligible balance is based on the unaffected balance of the original lottery. Please see the Account 
Balances section for more information on balance flows. 
The example that follows is of a supplemental lottery that has been run after an original lottery has been 
run but before the cash has been allocated. 
 
Scenario 8a: Supplemental Lottery (Post -Lottery, Pre-Allocation): 1 of 2 
 
A partial call occurs as usual: the CANO, CANO-E, and CAPA messages are sent out. You are informed 
of the event and your eligible balance, the lottery is run, and you are informed of your affected balance, 
the rate (if known), the projected debit to your underlying [[CUSIP]], your projected allocation, and the 
payment date. 
 
3 Please note that all scenario numbers are consistent with the scenarios in Appendix A. 


---

## Page 52

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 52 
After you receive the CAPA with the lottery results, you receive an announcement message for a 
supplemental lottery on the same event. This second CANO-E specifies the supplemental lottery with the 
Lottery Type “SUPP.” 
This scenario continues with the following diagram (8b). 
 
 
Scenario 8b: Supplemental Lottery (Post -Lottery, Pre-Allocation): 2 of 2 
 
A second CANO-E (REPL) is sent; this one applies to the supplemental lottery. It specifies your eligibility 
based on the original lottery. Your unaffected balance in the original lottery becomes your eligible balance 
for the supplemental.  
After the supplemental lottery is run, a CAPA message is sent that details the lottery results. It does not 
replace the CAPA that was sent on the original lottery; the results detailed here are for the supplemental 
lottery only. The CAPA message will contain the original Event [[ID]]. 
Two CACO messages (also containing the original Event [[ID]]) are then sent after pay date: one to confirm 
payment for the original lottery, and one to confirm payment for the supplemental. The Lottery Type 
element specifies which lottery the message applies to: “ORIG” for the original lottery and “SUPP” for the 
supplemental.  


---

## Page 53

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 53 
Sample Scenarios for Partial Defeasance and Partial Pre-Refunding  
This section details several of the most common process flows for redemption event messaging for partial 
defeasances and partial pre-refundings.  
These events involve lottery processing but [[DO]] not result in cash allocations. Instead, an [[issuer]] defeases 
a portion of its outstanding debt into two [[securities]]: one for the defeased security and one for the non-
defeased security. For a partial pre-refunding, the [[issuer]] partially refunds a portion of its outstanding 
balance to an earlier maturity date, resulting in two new [[securities]]: one for the refunded maturity and one 
for the non-refunded maturity.   
• The “refunded” or “defeased” security represents the portion that was called into early 
maturity (or that is guaranteed payment for that portion of the security at the time of maturity). 
• The “non-refunded” or “non-defeased” security represents the portion that retains the original 
maturity date. 
 
While these are the simplest and most likely scenarios, there are many more that might occur.  
For additional, more complex scenarios, please see Appendix A: Additional Scenarios. Note that, for 
consistency, scenarios are numbered based on their appearance in the Appendix. 
For a complete list of data elements for each message, their origins, and their usage, please utilize the 
Message Usage Guidelines available at [[DTCC]].com, the Learning Center, or My Standards at 
https://www2.swift.com/mystandards/.  
 
  

---

## Page 54

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 54 
Scenario 18: Partial Defeasance4 
In the case of a partial defeasance, the [[issuer]] sets aside cash in escrow to pay off a portion of the issue. 
The original [[CUSIP]] is surrendered and new [[securities]] are issued for the portion defeased.  
 
Scenario 18: Partial Defeasance 
The CANO message identifies the [[CUSIP]] that is being defeased (here, [[CUSIP]] A). In the Security 
Movement Details, you can see that [[CUSIP]] A is being debited and that two new CUSIPS are being 
created. 
• [[CUSIP]] B is identified as a new security for the defeased portion. You can see the earlier 
payment date for [[CUSIP]] B as well as the new-to-old ratio. 
• [[CUSIP]] C is identified as a new security for the non-defeased portion. It retains the original 
payment date. You can see the new-to-old ratio here as well. 
A CANO-E message informs you of your eligibility. The only [[CUSIP]] relevant here is [[CUSIP]] A, the original 
security. 
 
4 Please note that all scenario numbers are consistent with the scenarios in Appendix A. 


---

## Page 55

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 55 
Next, the lottery is run and a CAPA message is sent to inform you of the lottery results. Since the original 
[[CUSIP]] is being replaced by two new CUSIPS – defeased and non-defeased – you will have two new 
balances, one in each [[CUSIP]].  
• Your affected balance becomes your balance in [[CUSIP]] B, the defeased [[CUSIP]].  
• Your unaffected balance becomes your balance in [[CUSIP]] C, the non-defeased [[CUSIP]]. 
• Your entire balance in [[CUSIP]] A is debited. 
 
Additionally, if your balance in the original security decreased between the record date and the lottery 
date (for instance, if you delivered out [[shares]] after record date), your obligated balance is noted on the 
CAPA. 
After all [[shares]] have been moved, a CACO message confirms the movement of all [[shares]] into the new 
defeased and non-defeased [[securities]]. 
 
  

---

## Page 56

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 56 
Scenario 14: Partial Pre-Refunding5 
In the case of a partial pre-refunding, the [[issuer]] has exercised its privilege to repay part of the debt 
security prior to maturity. The lottery determines how much of your balance in the original security will be 
affected. Functionally, it is very similar to a partial defeasance. The original [[CUSIP]] is surrendered, and 
new [[securities]] are issued for the portion refunded and the portion non-refunded. 
 
Scenario 14: Partial Pre- Refunding 
The CANO message identifies the [[CUSIP]] that is being partially refunded (here, [[CUSIP]] A). In the Security 
Movement Details, you can see that [[CUSIP]] A is being debited and that two new CUSIPS are being 
created. 
• [[CUSIP]] B is identified as a new security for the refunded portion. You can see the earlier 
payment date for [[CUSIP]] B as well as the new-to-old ratio. 
• [[CUSIP]] C is identified as a new security for the non-refunded portion. It retains the original 
payment date. You can see the new-to-old ratio here as well. 
 
5 Please note that all scenario numbers are consistent with the scenarios in Appendix A. 


---

## Page 57

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: Lottery Ev ents 57 
A CANO-E message informs you of your eligibility. The only [[CUSIP]] relevant here is [[CUSIP]] A, the original 
security. 
Next, the lottery is run and a CAPA message is sent to inform you of the lottery results. Since the original 
[[CUSIP]] is being replaced by two new CUSIPS – refunded and non-refunded – you will have two new 
balances, one in each [[CUSIP]].  
• Your affected balance becomes your balance in [[CUSIP]] B, the refunded [[CUSIP]].  
• Your unaffected balance becomes your balance in [[CUSIP]] C, the non-refunded [[CUSIP]]. 
• Your entire balance in [[CUSIP]] A is debited. 
 
Additionally, if your balance in the original security decreased between the record date and the lottery 
date (for instance, if you delivered out [[shares]] after record date), your obligated balance is noted on the 
CAPA. 
After all [[shares]] have been moved, a CACO message confirms the movement of all [[shares]] into the new 
refunded and non-refunded [[securities]].

---

## Page 58

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: N on-Lottery Events 58 
Non-Lottery Events 
As with all corporate action events, a CANO message announces the event that is taking place. No 
CANO-E message is sent for non-lottery redemption events. The CAPA message (sent on  
Payment Date – 7) informs you of the amount you will be paid on payment date.  
The CAPC, CACO, CARE, and CAPS messages surround the payment flow. They function much the 
same as they [[DO]] for Distributions, but with additional fields that make the messages specific to the 
Redemptions flow.  
Non-lottery events include: 
• Full Call, 
• Final Paydown,  
• Termination, and 
• [[default]]. 
 
[[BASIC]] Message Flow for Non-Lottery Events 
 
Generally, non-lottery events have a simpler message flow than lottery events. Barring cancellations and 
reruns, events such as full calls, maturities, [[UIT]] terminations, and partial pre-refundings all follow this 
f low: 
1. [[DTCC]] sends a CANO to the client that announces the corporate action event.  
2. [[DTCC]] sends a CAPA message to the client projecting the associated payment/allocation, 
including balance and movement details. 
3. [[DTCC]] sends the client a CACO message to confirm movement of payment/allocation 
proceeds.  
The following subsections detail some common exceptions to this flow. For more exceptions and 
alternate process flows, please see Appendix A.  
  


---

## Page 59

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: N on-Lottery Events 59 
Sample Scenarios for Non-Standard, Non-Lottery Events 
Scenario 26: Full Call Cancellation (Pre-Allocation)6 
The security [[issuer]] announces a full call: all [[shares]] of a security are called back for redemption by the 
[[issuer]]. Before the redemption occurs, however, the event is rescinded. 
 
Scenario 26: Full Call Cancellation (Pre- Allocation) 
 
The CANO and CAPA messages are sent out as for a [[BASIC]] full call: you are informed of the event, the 
projected debit to your underlying [[CUSIP]], your projected allocation, and the payment date. 
In this case, though, the event is canceled between the pre-advice and the allocation. Since the allocation 
has been projected, there are two cancellation messages that are sent by [[DTCC]]: 
• The Event Cancellation (CACN) message corresponds to the CANO: it is sent to inform you 
that the event itself has been rescinded and will no longer take place. The 
• The Projection Cancellation (CAPC) message corresponds to the CAPA: it informs you that 
the projected allocation will not take place. The Preliminary Movement [[ID]] has the same value 
as the Business Message Identifier on the CAPA. 
 
  
 
6 Please note that all scenario numbers are consistent with the scenarios in Appendix A. 


---

## Page 60

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: N on-Lottery Events 60 
Scenario 27: Full Call Cancellation (Post-Allo [[CAT]] io n) 
This scenario deals with the cancellation of a full call event. In this case, however, the cancellation occurs 
on the same day after the cash has been allocated. 
 
 
Scenario 27a: Full Call Cancellation (Post -Allocation): 1 of 2 
 
The CANO and CAPA messages are sent out as for a [[BASIC]] full call: you are not only informed of the 
event, but also of the affected balance, the rate (if known), the projected debit to the underlying [[CUSIP]], 
the projected allocation, and the payment date. 
On payment date, allocation is made and the CACO message serves as a payment confirmation for the 
event. On payment date, the underlying [[CUSIP]] is debited and cash is moved to your account.  
At this point, however, the event is canceled. A CACN message is sent to rescind the event that was 
originally announced in the CANO.  
After the event is rescinded, it needs to be reversed. A new CAPA is sent after the CACN, detailing what 
it is that will be reversed. Note that the details of the CAPA for the reversal mirror the CAPA for the event: 
they reflect what is being reversed, not what will happen as a result of the reversal. 
This scenario concludes in the next diagram.  
 


---

## Page 61

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Redempti ons Mess agi ng: N on-Lottery Events 61 
 
Scenario 27b: Full Call Cancellation (Post-Allocation): 2 of 2 
 
Note: The CARE message in gray (above) is not currently in use. In the near future, it will be 
used for same-day allocation reversals. At the moment, all post-allocation reversals – 
same-day or otherwise – are made via the CACO message. 
 
The CACO message presents the reversal details after the allocation has been reversed. Note that the 
details represent opposite movement from the CAPA messages: cash is debited from and [[securities]] are 
credited to your account.


---

## Page 62

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Message Subscriptions and Timing 62 
Message Subscriptions and Timing 
Redemptions messages will be sent to you based on your subscriptions. The timing for each is 
determined by your subscription options. Subscription options are based on event types rather than [[Asset]] 
types. 
The following tables describe message subscription options and their related times, as well as general 
processing times and holiday schedules. 
 
Subscription Options : Lottery  Events 
All times are given in Eastern Standard Time. 
Message Message Times Notes 
CANO-E Via file: 
• 12:30 a.m. 
• 1:45 p.m. 
• 5:30 p.m. 
• 6:50 p.m. 
Real time: 
• 8:00 a.m. – 5:30 p.m. 
• 6:50 p.m. 
• 12:30 a.m. 
1. CANO-E messages apply to 
lottery events only. 
2. Messages are available with or 
without Position Adjustment  
(Interim Accounting). 
3. A time stamp in the Business 
Application Header (BAH) allows 
you to verify message order. 
CAPA Available via both file and real time 
at: 
• 12:30 a.m. 
• 10:45 a.m. 
• 1:30 p.m. 
• 2:30 p.m. 
• 3:30 p.m. 
CAPA REPL (replacement) 
messages are available after 
mainline date at 1:30 a.m.  
N/A 

---

## Page 63

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Message Subscriptions and Timing 63 
Message Message Times Notes 
CAPC Via file:  
• 1:30 a.m. 
Real time:  
• Hourly 10:30 a.m. – 6:30 
p.m. 
• 1:30 a.m. 
1. A CAPC subscription will always 
require a CAPA subscription as 
well.  
2. Conversely, a CAPA subscription 
does not require CAPC 
subscription. However, if you 
subscribe to CAPA messages, it 
is suggested that you subscribe 
to CAPC messages. 
3. A time stamp in the Business 
Application Header (BAH) allows 
you to verify message order. 
CACO 
CARE  
Via file:  
• 12:30 a.m. 
• 1:30 p.m. 
• 2:30 p.m. 
• 3:30 p.m. 
• 4:00 p.m. 
Real time:  
• Every 20 minutes between 
8:20 a.m. and 4:30 p.m. 
A time stamp in the Business 
Application Header (BAH) allows you 
to verify message order. 
 
CAPS Via file:  
• 4:00 p.m. 
• 5:00 p.m. 
• 7:00 p.m. 
Real time:  
• Hourly between 1:00 p.m. 
and 7:00 p.m. 
1. The CAPS message is sent 
based on the CAPA that was 
previously sent. 
2. Reason codes are provided to 
explain why a given event was 
not allocated. 
3. A time stamp in the Business 
Application Header (BAH) allows 
you to verify message order. 
 
  

---

## Page 64

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Message Subscriptions and Timing 64 
Subscription Options : Non-Lottery Events and Maturities 
Message Message Times Notes 
CANO-E Not available for these events Not available for these events 
CAPA Available via both file and real time 
at: 
• 1:30 a.m. 
1. CAPA messages are sent on 
Payment Date – 7 for CAPA 
NEWM (new messages).  
2. Between Payment Date – 6 and 
Payment Date – 1, CAPA REPL 
(replacement messages) are sent. 
CAPC Via file:  
• 1:30 a.m. 
Real time:  
• Hourly 10:30 a.m. – 6:30 
p.m. 
• 1:30 a.m. 
1. A CAPC subscription will always 
require a CAPA subscription as 
well.  
2. Conversely, a CAPA subscription 
does not require CAPC 
subscription. However, if you 
subscribe to CAPA messages, it is 
suggested that you subscribe to 
CAPC messages. 
3. A time stamp in the Business 
Application Header (BAH) allows 
you to verify message order. 
CACO 
CARE  
Via file:  
• 4:00 p.m. 
Real time:  
• Every 20 minutes between 
8:20 a.m. and 4:30 p.m. 
A time stamp in the Business 
Application Header (BAH) allows you 
to verify message order. 
 
CAPS Via file:  
• 4:00 p.m. 
• 5:00 p.m. 
• 7:00 p.m. 
Real time:  
• Hourly between 1:00 p.m. 
and 7:00 p.m. 
1. The CAPS message is sent based 
on the CAPA that was previously 
sent. 
2. Reason codes are provided to 
explain why a given event was not 
allocated. 
3. A time stamp in the Business 
Application Header (BAH) allows 
you to verify message order. 
 
  

---

## Page 65

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Message Subscriptions and Timing 65 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times 
specified below. Exceptions are noted in the holiday processing schedule. 
 
Message Monday – Friday Saturday and Sunday 
CANO Normal message volumes. 
Files transmitted based on customer 
subscription. 
Saturday:  
• Limited volumes. 
• No files transmitted. 
Sunday: 
• Limited volumes. 
• Files transmitted based 
on customer subscription. 
CANO-E Messages at 2:00 p.m. and 11:30 p.m. 
eastern time. 
Files transmitted based on customer 
subscription. 
No messages or files transmitted. 
CAPA Messages between 1:00 a.m. and 2:00 
a.m. eastern time. 
Files transmitted at 1:30 a.m. eastern 
time. 
No messages or files transmitted. 
CAPC Messages between 10:30 a.m. and 6:30 
p.m. eastern time. 
Files transmitted at 1:30 a.m. eastern 
time. 
No messages or files transmitted. 
CACO 
CARE 
Messages between 8:20 a.m. and 7:00 
p.m. eastern time based on customer 
subscription. 
Files transmitted at 4:00 p.m., 7:00 
p.m., and 1:30 a.m. eastern time, based 
on customer subscription. 
No messages or files transmitted. 
CAPS Messages between 1:00 p.m. and 7:00 
p.m. eastern time based on customer 
subscription. 
Files transmitted at 5:00 p.m. and 7:00 
p.m. eastern time based on customer 
subscription. 
No messages or files transmitted. 
 

---

## Page 66

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Message Subscriptions and Timing 66 
Holiday Processing Schedule 
Messages/ 
Holidays 
U.S. and Canadian 
Holidays  
(both closed) 
U.S. Holidays 
([[DTCC]] closed, Canada 
open) 
Canadian Holidays 
([[DTCC]] open,  
Canada closed) 
CANO Limited volumes. 
Files transmitted based 
on customer 
subscription. 
Limited volumes. 
Files transmitted based 
on customer 
subscription. 
Normal volumes. 
Files transmitted 
based on customer 
subscription. 
CANO-E No messages. No messages or files 
transmitted. 
Normal volumes. 
Files transmitted 
based on customer 
subscription. 
CAPA 
CAPC 
No messages. Normal volumes. 
Files transmitted based 
on customer 
subscription. 
Normal volumes. 
Files transmitted 
based on customer 
subscription. 
CACO 
CARE 
No messages. Only for Canadian 
payments. 
Normal volumes. 
Files transmitted 
based on customer 
subscription. 
CAPS No messages. 1:00 p.m., 2:00 p.m., 
and 3:00 p.m. eastern 
time f or P&I and foreign 
payments. 
Normal volumes. 
Files transmitted 
based on customer 
subscription. 
For these 
holidays: 
• New Year's Day 
• Labor Day  
• Christmas Day 
• Dr. Martin Luther King, 
Jr. Day  
• Presidents' Day  
• Memorial Day  
• Independence Day  
• Thanksgiving Day 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving 
Day 
• Boxing Day 
 
In addition to this chart, please note that [[DTCC]] operates on two U.S. bank holidays: 
• Columbus Day ([[Stock]] allocation only; no cash 
allocation) 
• Veterans’ Day ([[Stock]] allocation only; no cash 
allocation) 
 

---

## Page 67

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification (CANO) 67 
CANO 
 
 
Corporate Action Notification 
 
What is a CANO Message? 
A Corporate Action Notification (CANO) message is an announcement of a corporate action.  
It contains all of the information known about a corporate action: event details, event status, security 
description and details, relevant dates, and more. 
This guide focuses only on CANO messages for redemption events. Clients are encouraged to consult 
the [[DTCC]] Product Migration Guide and My Standards for more general information regarding CANO 
messages. 
  


---

## Page 68

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification (CANO) 68 
The identifying information for a CANO message is: 
 
MX Identifier ISO 20022  
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.031.002.xx7 CA Notif ication supl.001.001.xx7 CANO MT 564 Announcements 
 
The CANO is the first message a client will receive regarding a corporate action of any type. As such, it 
contains identifiers such as the Corporate Action Event [[ID]] that remain with the event throughout its 
lifecycle.  
The message is sent per client account number regardless of whether the client has position in this 
security. The message contains event details only without account-related position or [[Entitlement]] 
information.  
 
When Are CANO Messages Generated?  
CANO messages are available via file at: 
• 1:30 a.m. 
• 3:30 a.m. 
• 6:00 a.m. 
• 9:00 a.m. 
• 11:00 a.m. 
 
• 12:00 p.m. 
• 1:00 p.m. 
• 2:00 p.m. 
• 3:00 p.m. 
• 4:00 p.m. 
• 5:00 p.m. 
• 6:00 p.m. 
• 7:00 p.m. 
• 8:00 p.m. 
• 9:00 p.m. 
• 11:30 p.m. 
Note: All times listed above represent Eastern Standard Time. 
A client may subscribe to one, all, or any combination of these message times. 
The messages are also available in real time via MQ. 
 
  
 
7 The last two digits in the MX Identifier and the Extension code signify the version number. The MX 
version number and/or the Supplementary version number may change during the SWIFT annual release 
based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 69

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification (CANO) 69 
Weekly Messaging Times 
Generally, announcement messages are sent Monday through Friday during the times specified below. 
Exceptions are noted in the holiday processing schedule. 
Message Monday – Friday Saturday Sunday 
CANO Normal message 
volumes. 
Files are transmitted 
based on customer 
subscription. 
Limited message 
volumes. 
No files transmitted. 
Limited message 
volumes. 
Files are transmitted 
based on customer 
subscription. 
 
Holiday Processing Schedule 
U.S. and Canadian 
Holidays  
(both closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada closed) 
Limited message 
volumes are sent on: 
• New Year's Day, 
• Labor Day, and 
• Christmas Day. 
Files are transmitted 
based on customer 
subscription. 
Limited message volumes are 
sent on: 
• Dr. Martin Luther King, Jr. 
Day,  
• Presidents' Day,  
• Memorial Day,  
• Independence Day, and 
• Thanksgiving Day. 
Files are transmitted based on 
customer subscription. 
Normal volumes are sent on: 
• Good Friday (All), 
• Victoria Day, 
• Canada Day, 
• CDN Thanksgiving Day, and   
• Boxing Day. 
Files are transmitted based on 
customer subscription. 
 
Redemption Event Types 
For redemption events, CANO messages will announce one of the following event types: 
Event Name Event Description 
[[default]] A notice of failure by the [[issuer]] to honor commitments made within 
the terms of the issued security. It usually relates to making timely 
payments of interest and principal as they come due. A payment 
may be made in lieu of reinstituting the original payments. 
Final Paydown The final distribution of principal due on a security (typically CMOs). 

---

## Page 70

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification (CANO) 70 
Full Call The security is redeemed for cash in its entirety on a date that is 
prior to the maturity date, and for which the holders receive the 
principal amount of the security. 
Full Pre-Refunding The exercise of a privilege by the [[issuer]] to repay, in full, any debt 
security prior to maturity when the [[issuer]] deposits assets in trust. 
This irrevocably restricts their use to satisfaction of the debt. 
Maturity The final repayment, usually in cash, by an [[issuer]] for the entire 
issue, or remaining outstanding [[securities]] of a specific security on a 
specified date. 
Partial Call [[securities]] are redeemed by the [[issuer]] for cash, in part, before their 
scheduled maturity date. The outstanding amount of [[securities]] will 
be proportionally reduced based on a specific percentage of 
holding. A lottery may be run where pooled [[securities]] are held. 
Partial Defeasance The [[issuer]] sets aside cash in escrow to pay off a portion of the 
issue before the maturity date. New [[securities]] are issued for the 
portion defeased. 
Partial Pre-Refunding Similar to a full pre-refunding, a partial pre-refunding is the exercise 
of a privilege by the [[issuer]] to repay, in part, any debt security prior 
to maturity when the [[issuer]] deposits assets in trust. This 
irrevocably restricts their use to satisfaction of the debt. New 
[[securities]] are issued for the portion pre-refunded. 
[[UIT]] Termination A security, usually a form of a derivative (e.g., [[ADR]] or [[UIT]]), for 
which the agent or [[issuer]] has decided to terminate the derivative 
based on a change to the underlying security/ies or a change in 
strategy. 
 
Redemption Event Information Contained on the CANO Message 
Mapping for the message layout will conform to the ISO message rules.  
CANO messages for redemption events have “levels” of information that categorize the data elements. 
These levels tell you whether the information refers to: 
• The event in general, 
• Event details, including lottery information (if applicable) 
• Event text, 
• Certificate number(s), if applicable, 
• Options, 
• Payouts, 

---

## Page 71

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification (CANO) 71 
• Agent information, or 
• Related events. 
The following table contains only data elements that refer specifically to redemption events, or common 
data elements that have a particular meaning in redemption event messages.  
There are many more fields on the CANO message. For more detailed technical information about CANO 
message contents and elements, including ISO field names, please see the Data Dictionary and/or My 
Standards for this message. 
 
Information Definition / Notes 
Message Type Part of the message header. Always set to “CANO.” 
Notification Type NEWM for new messages 
Official Corporate 
Actions Event [[ID]] 
The “Official Corporate Actions Identifier” is the official, unique 
identifier for the corporate action that will stay with the event 
throughout its lifecycle.  
It is made up of the CA [[ID]] preceded by “US.” In order for this 
instruction to be accepted and processed, the COAF on the 
instruction must match the COAF on the announcement messages. 
Event Type • DRAW for partial calls 
• PDEF for partial defeasances and partial pre-refundings  
• MCAL for full calls, final paydowns, and maturities 
• REDM for final maturities and [[UIT]] terminations 
• DFLT for defaults 
Extended Event Group The code REDM is used to specify that a redemption event is 
being announced. It is the general event category; individual 
redemption events are specified in the Event Code field. 
For events other than redemption events, “Event Processing Type” 
is used to specify the event type. Redemption events [[DO]] not use 
this field. 
Underlying Security Includes security description and [[CUSIP]] code 
Redemption 
Identification 
Unique number assigned by the system to all lottery and non-lottery  
events announced in [[DTC]]’s legacy systems. 
Notice Type This indicates whether the notice received was universal or specific 
to [[securities]] registered in [[DTC]]’s [[nominee]] name. 
Security Description This piece of [[Option]] information provides the description 
associated with the contra [[CUSIP]]. 

---

## Page 72

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification (CANO) 72 
Lottery Information 
Lottery Events Only 
Lotteries only apply to some redemption events. They are, 
however, unique to redemptions. 
Some fields in the CANO message only appear for these events. 
They include: 
• Lottery Type. Defines the type of lottery being processed: 
o ORIG. Original lottery. 
o SUPP. Supplemental lottery. 
• Event Stage. The stage in the corporate action life cycle as it 
specifically relates to lotteries. Values include: 
o FULL. Cancellation and re-run, 
o RESC. Supplemental cancellation, and  
o PART. Supplemental cancellation and re-run. 
• Lottery Date. The date on which called positions will be 
moved into either a segregated account or a [[DTC]] contra 
[[CUSIP]]. 
• Lottery Contra [[CUSIP]]. A [[DTC]] user [[CUSIP]] associated with 
the event for the purpose of segregating positions affected by 
the upcoming lottery. 
• Base Denomination. The denomination of the security used 
to run a lottery. This is a decimal value that uses units of the 
face amount depending on the security type. 
• Denomination Increments. Supplemental increments the 
lottery is run in. This is a decimal value that uses units of the 
face amount depending on the security type. 
Refunding / 
Defeasement 
information  
Lottery Events Only 
Partial pre-refunding and partial defeasements are lottery sub-
types. Some fields only appear on the CANO for these events: 
• Originating Security Information / Type. This represents the 
original security identifier in partial defeasance and partial pre-
refunding events, in which a secondary [[CUSIP]] is created for 
the amount defeased or refunded. The “type” for this security 
is always a [[CUSIP]]. 
• Defeasement Indicator. For partial defeasement events, this 
identifies which distributing security is defeased and which is 
non-defeased. 
o DEFE. Defeased. 
o NDEF. Non-defeased. 
• Refunded Indicator. For partial pre-refunding events, this 
identifies which distributing security is refunded and which is 
non-refunded. 
o REFU. Refunded. 
o NREF. Non-refunded. 
• Refunded Maturity Date. For partial pre-refunding events 
only, this represents the new maturity date for a pre-refunded 
security. 

---

## Page 73

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification (CANO) 73 
Mandatory / Voluntary 
Indicator 
Redemption events are mandatory. The indicator is always set to 
MAND. 
Declared Payable Date The payable date for the redemption as announced by the agent or 
[[issuer]]. 
• This is mapped to all non-security payouts. 
• UKWN is used if the value is not available and is expe cted. 
• ONGO is used for ongoing events in which the concept of 
payable date does not exist. 
[[Option]] Type Only three [[Option]] types apply to redemption events: 
• CASH. Holder will receive cash as a result of the redemption. 
• SECU. Holder will receive [[securities]] as a result of the 
redemption. 
• CASE. Holder will receive a combination of cash and 
[[securities]] as a result of the redemption. 
Flags These are yes/no indicators that specify certain pieces of 
information: 
• Conditional Payment Applicable. An Event flag that 
indicates whether the payment made by the [[issuer]] is based on 
a stated condition. 
• Debit/Credit. A Payout flag that signals that the movement 
specified in the announcement is a debit or a credit. Note that 
for redemption events, a debit of the underlying security will 
always take place. A credit for either [[securities]] or cash is then 
made. 
 
 

---

## Page 74

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification with Eligible Balance (CANO-E) 74 
CANO-E 
 
 
Corporate Action Notification 
with  
Eligible Balance 
 
What is a CANO-E Message? 
The Corporate Action Notification with Eligible Balance (CANO-E) message will be generated upon 
subscription for partial call, partial pre-refunding, and partial defeasance events. CANO-E messages will 
not be generated for non-lottery events. 
The CANO-E captures a customer’s [[DTCC]] eligible position on Record Date for a particular corporate 
action (announced in the original CANO). This message provides information about your eligible balance 
(based on the details of the lottery) prior to the lottery being run. 
Your settled and total eligible balances are contained in the core portion of the message, while additional 
segregated balances can be found in the message extension (when applicable). 
  


---

## Page 75

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification with Eligible Balance (CANO-E) 75 
The identifying information for a CANO-E message is: 
 
MX Identifier ISO 20022  
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.031.002.xx8 CA Notification with 
Eligible Balance 
supl.007.001.xx8 CANO-E MT 564 Pre-Lottery 
Positions 
 
The purpose of this message is to provide clients with eligibility information, and as such most event 
details are not provided within the CANO-E. These event details can be traced back to the CANO 
message through the Corporate Action Event [[ID]]. By using these identifiers, the body of the CANO 
message is not repeated in the CANO-E. 
The important fields on the CANO-E include: 
• Corporate Action Event [[ID]], 
• Event Type, 
• Lottery Type, 
• Mandatory/Voluntary indicator, and 
• Record Date. 
The corresponding legacy [[CCF]] file for the record date statement is REDEM L. Elements from the [[CCF]] file 
that are not market practice compliant and cannot be contained in the CANO-E message are contained in 
the message extension as supplementary data. 
 
When Are CANO-E Messages Generated?  
A CANO with eligible balance message will be generated once per event on position capture date 
(publication date – 1), in between a lottery event’s announcement and the running of the lottery. The date 
of the upcoming lottery can be found on the CANO. 
The f irst CANO-E received by a [[participant]] will always be a NEWM: this is the ISO notification type 
signifying a new message. All subsequent CANO-Es are REPLs, or replacement messages.  
CANO-E NEWM messages are created on a daily basis for items for which the record date has been 
reached and position capture has occurred. In the case of a lottery re-run, a new Event [[ID]] has been 
assigned; therefore, a NEWM is sent for that new [[ID]], 
 
8 The last two digits in the MX Identifier and the Extension code signify the version number. The MX 
version number and/or the Supplementary version number may change during the SWIFT annual release 
based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 76

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification with Eligible Balance (CANO-E) 76 
CANO-E REPL messages are sent in two cases: 
• When updates / adjustments are made to the pre-lottery position for client balances. 
• After the lottery-based event has occurred and a supplemental lottery has been called in a 
CANO REPL message. Supplemental lotteries require the re-announcement of eligibility 
based upon the unaffected balances from the original lottery. These messages will contain a 
lottery type of “SUPP” to indicate the supplemental lottery. 
 
CANO-E Messages and Pending Trades 
Note that pending trades (as they relate to the lottery process) are not incorporated into the CANO-E 
message. Therefore, clients with pending trades due to settle between the publication date and the lottery 
date of an event will not see the potential [[short position]] within the CANO-E message. If you are driven 
short after the lottery has been run, that will be indicated by the Obligated Balance on the CAPA 
message. Please see the Account Balances and Lottery Events section for more information. 
 
CANO-E Message Subscriptions and Timing 
Subscription to the CANO-E message is mandatory for DRAW and PDEF events. 
Via file: 
• 12:30 a.m. 
• 1:45 p.m. 
• 5:30 p.m. 
• 6:50 p.m. 
Real time: 
• 8:00 a.m. – 5:30 p.m. 
• 6:50 p.m. 
• 12:30 a.m. 
 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times 
specified below. Exceptions are noted in the holiday processing schedule. 
 
Message Monday – Friday Saturday and Sunday 
CANO-E Messages at 2:00 p.m. and 11:30 p.m. eastern 
time. 
Files transmitted based on customer 
subscription. 
No messages or files 
transmitted. 
 

---

## Page 77

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification with Eligible Balance (CANO-E) 77 
Holiday Processing Schedule 
U.S. and Canadian 
Holidays 
(both closed) 
U.S. Holidays 
([[DTCC]] closed, Canada 
open) 
Canadian Holidays 
([[DTCC]] open, Canada closed) 
No messages or files are 
sent on: 
• New Year's Day 
• Labor Day, and 
• Christmas Day. 
No messages or files are 
sent on: 
• Dr. Martin Luther King, 
Jr. Day  
• Presidents' Day  
• Memorial Day  
• Independence Day, and 
• Thanksgiving Day. 
Normal volumes occur on these 
days:  
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day, and  
• Boxing Day. 
Files are transmitted based on 
customer subscription. 
 
Information Contained on the CANO-E Message 
Mapping for the message layout will conform to the ISO message rules.  
The following table contains some of the important elements in the CANO-E message. 
For more detailed technical information about message contents and elements, please see the Data 
Dictionary and/or My Standards for this message. 
 
Data Element Definition / Information 
Message Type Always set to “CANO-E.” 
Official Corporate 
Actions Event [[ID]] 
Official Corporate Actions Identifier. This is the official, unique 
identifier for the corporate action. It is made up of the CA [[ID]] 
preceded by “US.” In order for this instruction to be accepted and 
processed, the COAF on the instruction must match the COAF on 
the announcement messages. 
Event Type • “DRAW” for partial calls. 
• “PDEF” for partial defeasances and partial pre-refundings. 
Underlying Security Includes security description and [[CUSIP]] code. 
Lottery Type • “ORIG” for original lottery. 
• “SUPP” for supplemental lottery. 
Record Date (Pub Date) Date/time at which positions are struck at the end of the day to 
determine eligible balances for the upcoming lottery. 

---

## Page 78

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Notification with Eligible Balance (CANO-E) 78 
Notification Type • “NEWM” for new messages. 
• “REPL” for replacement messages. 
CA [[ID]] Corporate Actions Identifier. This is [[DTC]]’s unique identifier for the 
corporate action event.  
Total Eligible Balance Represents the current eligible balance that could be called. 
[[settlement]] Position 
Balance 
Balance of [[securities]] representing only settled transactions; 
pending transactions not included. 
[[collateral]] Out Balance Balance of [[securities]] that belong to the safekeeping account 
indicated within this message and are deposited with a third party 
for the purpose of collateralization. 
 
The extension for the CANO-E message includes the following information: 
Data Element Definition / Information 
Balance Information • Original Balance. The original eligible balance as determined 
on record date. The original balance will remain constant for 
the life of the event, including any subsequent supplemental 
lottery CANO-E messages. 
• Adjusted Balance. Total eligible balance containing manual 
adjustments. 
• Unpledged Balance. Total number of [[shares]] this [[participant]] 
has pledged to any number of pledgee banks for this security. 
Individual pledge records record the security, number of 
[[shares]], [[participant]], pledgee bank, and loan date. 
• Investment Pledged Balance. The total quantity of [[securities]] 
segregated from the General Free account of a firm, partner, 
officer, stockholder, or an omnibus account. This account is 
used for reporting information to the IRS about [[securities]] 
purchased for investment purposes. Individual investment [[ID]] 
records contain position, serial number, and trad e date. 
• Investment Unpledged Balance. Position held that 
represents the total quantity of [[securities]] segregated from the 
General Free account. Individual segregated records contain 
security, serial number and number of [[shares]]. Only serial 
numbers 1 – 5 can be accessed directly by participants. 
Redemption [[ID]] Unique number systemically assigned to all lottery and non-lottery 
events in CA Web. 
 

---

## Page 79

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice (CAPA) 79 
CAPA 
 
 
Corporate Action Movement 
Preliminary Advice 
 
What is a CAPA Message?  
The Corporate Action Movement Preliminary Advice (CAPA) message will be generated upon 
subscription for both lottery and non-lottery events. 
• For lottery events, the CAPA message provides the lottery results, showing what position was 
affected (“called”) and unaffected (“remaining”) by the lottery. Based on the affected position, 
it will also state the cash amount to be received by the client. For PDEF events, it will provide 
the new [[securities]] to be received (either refunded and non-refunded or defeased and non-
defeased). 
 
• For non-lottery events, the CAPA message projects payments and allocations on a corporate 
action event. 
 
  


---

## Page 80

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice (CAPA) 80 
The identifying information for a CAPA message is: 
MX Identifier ISO 20022  
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.035.002.xx9 
CA Movement 
Preliminary Advice 
supl.009.001.xx9 CAPA MT 564 
Lottery Results 
and Projected 
Payments 
 
The notification types for preliminary advice messages include NEWM (New Messages) and REPL 
(Replacement Messages). NEWM messages are sent on Payment Date minus 7; any subsequent 
messages for that same Corporate Action Event [[ID]] will be a REPL message. 
If there is a change to the [[Entitlement]], a replacement (REPL) message will be generated for the 
[[participant]] for the event. 
 
CAPA Messages for Lottery vs. Non-Lottery Events 
Lottery Events 
CAPA messages for lottery events inform you whether your position has been called or not.  
• If your position has been called, the CAPA outlines your affected and unaffected position, the 
payment you can expect, and when you can expect it.  
• The CAPA provides an obligated position if the amount to be called (“affected position”) is 
greater than your [[settlement]] position on lottery date.  
Note: Your [[settlement]] position will be considered short (SHOR) if this occurs.  
Please see the Account Balances and Lottery Events section for more information. 
• If your position was not called in the lottery, you will still receive a CAPA lottery results 
message stating zero affected balance.  
• If a supplemental call is announced, it will be processed under the same Corporate Action 
Event [[ID]] but with a supplemental lottery type.  
• CAPA lottery result messages are sent five times a day (at 12:30 a.m., 10:45 a.m., 1:30 p.m., 
2:30 p.m., and 3:30 p.m.). CAPA messages for non-lottery events and maturities are sent at 
1:30 a.m. 
 
  
 
9 The last two digits in the MX Identifier and the Extension code signify the version number. The MX 
version number and/or the Supplementary version number may change during the SWIFT annual release 
based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 81

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice (CAPA) 81 
Lottery Events and Pending Trades 
For lottery events, clients with pending trades due to settle between the publication date and the lottery 
date of an event will not see the potential [[short position]] within the CANO-E message. If you are driven 
short after the lottery has been run, that will be indicated by the Obligated Balance on the CAPA 
message. Please see the Account Balances and Lottery Events section for more information. 
The important information on the CAPA for lottery events includes: 
• Event General Details 
• Lottery Details 
• Balance Information 
• Cash/Security Movement Details 
 
Non-Lottery Events 
CAPA messages for non-lottery events include the projected allocation information for full calls, 
maturities, [[UIT]] terminations, and full pre-refunding.  
The important information on the CAPA for non-lottery events includes: 
• Event General Details 
• Balance Information 
• Cash/Security Movement Details 
 
When Are CAPA Messages Generated?  
Lottery Events 
• CAPA messages are only sent for lottery events if a CANO-E has been sent for that client 
account. 
• CAPA NEWMs are created on Lottery Date for lottery-based events (DRAW, PDEF) once the 
lottery has been run. If a rate is available, then the projected cash movement will be 
published. No subsequent updates will be sent until Payment Date – 1 unless the rate 
changes. If no rate is available, the projected cash [[Entitlement]] will be marked as unknown 
(“UKWN”). 
• Between Payment Date – 7 and Payment Date – 1, CAPA REPL messages are sent when a 
rate has been received for an event in which the rate was previously unknown.  
• On Payment Date – 1, a CAPA REPL message is automatically generated based on a 
projection by [[DTCC]]. 
• CAPA NEWMs are also sent when supplemental lotteries are called.  
In this case, the CAPA is used to project the supplemental amount only. 
 

---

## Page 82

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice (CAPA) 82 
Non-Lottery Events 
• CAPA messages are created for clients subscribing to these non-lottery events: 
o REDM (Maturity FC 70; 75M; 77M;), 
o MCAL (Full Call FC 75F; 77F), and 
o DFLT ([[default]] FC 86P Interim and 86F Final). 
• CAPA messages begin generating on Payment Date -7. If the rate is not available, the projected 
cash [[Entitlement]] will be marked as unknown (“UKWN”). 
• Between Payment Date – 7 and Payment Date – 1, CAPA REPL messages are sent when a rate 
has been received for an event for which the rate was previously unknown. 
• A CAPA message will automatically be generated on Payment Date – 1 regardless of the 
subscription [[Option]]. 
• Full calls, maturities, defaults, [[UIT]] terminations, and full pre-refundings will only generate a CAPA 
message on Payment Date – 1. 
 
CAPA Message Subscriptions and Timing 
Lottery Events 
CAPA messages are available via both file and real time at: 
• 12:30 a.m. 
• 10:45 a.m. 
• 1:30 p.m. 
• 2:30 p.m. 
• 3:30 p.m. 
CAPA REPL (replacement) messages are available after mainline date at 1:30 a.m. 
 
Non-Lottery Events 
CAPA messages are available via both file and real time at 1:30 a.m. 
• CAPA messages are sent on Payment Date – 7 for CAPA NEWM (new messages).  
• Between Payment Date – 6 and Payment Date – 1, CAPA REPL (replacement messages) 
are sent. 
 
  

---

## Page 83

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice (CAPA) 83 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times 
specified below. Exceptions are noted in the holiday processing schedule. 
Message Monday – Friday Saturday and Sunday 
CAPA Messages between 1:00 a.m. and 2:00 a.m. 
eastern time. 
Files transmitted based on customer 
subscription. 
No messages or files 
transmitted. 
 
Holiday Processing Schedule 
U.S. and Canadian 
Holidays  
(both closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada 
closed) 
No messages or files are 
sent on: 
• New Year's Day 
• Labor Day, and 
• Christmas Day. 
Normal volumes occur on these 
days:  
• Dr. Martin Luther King, Jr. 
Day  
• Presidents' Day  
• Memorial Day  
• Independence Day, and 
• Thanksgiving Day. 
Files are transmitted based on 
customer subscription. 
Normal volumes occur on 
these days: 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day, 
and  
• Boxing Day. 
Files are transmitted based on 
customer subscription. 
 
Information Contained on the CAPA Message 
Mapping for the message layout will conform to the ISO message rules.  
The following two tables contain some of the important information in the CAPA messages for lottery and 
non-lottery events. 
For more detailed technical information about message contents and elements, please see the Data 
Dictionary and/or My Standards for this message. 
 
  

---

## Page 84

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice (CAPA) 84 
Lottery Events 
Information Definition / Notes 
Message Type Part of the message header. Always set to “CAPA.” 
Official Corporate 
Actions Event [[ID]] 
Official Corporate Actions Identifier. This is the official, unique 
identifier for the corporate action. It is made up of the CA [[ID]] 
preceded by “US.” In order for this instruction to be accepted and 
processed, the COAF on the instruction must match the COAF on 
the announcement messages. 
Event Type • DRAW for partial calls. 
• PDEF for partial defeasances and partial pre-refundings. 
Underlying Security Includes security description and [[CUSIP]] code. 
Lottery Type • ORIG for original lottery. 
• SUPP for supplemental lottery. 
Record Date  
(Pub Date - 1) 
Date/time at which positions are struck at the end of the day to 
determine eligible balances for the upcoming lottery. 
Notification Type • NEWM for new messages. 
• REPL for replacement messages. 
Balance Information The balances contained in the core CAPA message for lottery 
events include: 
• Total Eligible Balance. Represents the current eligible 
balance that could be called. 
• [[settlement]] Position Balance. Balance of [[securities]] 
representing only settled transactions; pending transactions 
not included. 
• [[collateral]] Out Balance. Balance of [[securities]] that belong to 
the safekeeping account indicated within this message and are 
deposited with a third party for the purpose of collateralization. 
• Affected Balance. The portion of the eligible position that is 
called by the lottery. For partial pre-refundings, this is the 
refunded balance; for partial defeasements, this is the 
defeas ed balance. 
• Unaffected Balance. The portion of the eligible position that is 
not called by the lottery. For partial pre-refundings, this is the 
non-refunded balance; for partial defeasements, this is the 
non-defeased balance. 
• Obligated Balance. Obligated position occurs when the 
affected balance is greater than the settled position. This can 
happen when a call notice is received late and the prior record 
date position is greater than what is currently settled.  

---

## Page 85

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice (CAPA) 85 
This is position that account holders should return to the 
account servicer to participate in the event or to fulfill their 
obligation for the event to be complete (for example, return of 
[[securities]] for a late-announced drawing). 
New [[securities]] 
Issuance Indicator 
For PDEF events (partial defeasances and partial pre-refundings), 
this indicates the new security type based on the lottery being run. 
Values include: 
• DEFE. Defeased 
• NDEF. Non-defeased 
• REFU. Refunded 
• NREF Non-refunded 
Called Amount The principal amount (for debt issues) or number of [[shares]] (for 
[[Equity]] issues) that has been called for redemption for a particular 
certificate number 
 
The extension for the CAPA message includes the following information: 
Information Definition / Notes 
Redemption [[ID]] A unique number systemically assigned to all lottery and non-lottery  
events in CA Web. 
Lottery Sequence 
Number 
A system-generated number to distinguish between the series of 
lotteries run against a particular redemption 
Balance Information • Original Balance. The original eligible balance as determined 
on record date. The original balance will remain constant for 
the life of the event, including any subsequent supplemental 
lottery CANO-E messages. 
• Adjusted Balance. Total eligible balance containing manual 
adjustments. 
• Unpledged Balance. Total number of [[shares]] this [[participant]] 
has pledged to any number of pledgee banks for this security. 
Individual pledge records record the security, number of 
[[shares]], [[participant]], pledgee bank, and loan date. 
• Investment Pledged Balance. The total quantity of [[securities]] 
segregated from the General Free account of a firm, partner, 
officer, stockholder, or an omnibus account. This account is 
used for reporting information to the IRS about [[securities]] 
purchased for investment purposes. Individual investment [[ID]] 
records contain position, serial number, and trade date. 
• Investment Unpledged Balance. Position held that 
represents the total quantity of [[securities]] segregated from the 
General Free account. Individual segregated records contain 
security, serial number and number of [[shares]]. Only serial 
numbers 1 – 5 can be accessed directly by participants. 

---

## Page 86

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice (CAPA) 86 
Non-Lottery Events 
Information Definition / Notes 
Message Type Part of the message header. Always set to “CAPA.” 
Official Corporate 
Actions Event [[ID]] 
Official Corporate Actions Identifier. This is the official, unique 
identifier for the corporate action. It is made up of the CA [[ID]] 
preceded by “US.” In order for this instruction to be accepted and 
processed, the COAF on the instruction must match the COAF on 
the announcement messages. 
Event Type • MCAL for corporate full calls, municipal full calls, and CMO 
final paydowns. 
• REDM for [[UIT]] termination and final maturity (corporate 
maturity, municipal maturity, and CD redemption). 
Underlying Security Includes security description and [[CUSIP]] code. 
Record Date  
(Pub Date - 1) 
Date/time at which positions are struck at the end of the day to 
determine eligible balances for the upcoming lottery. 
Notification Type • NEWM for new messages. 
• REPL for replacement messages. 
Balance Information • Total Eligible Balance. Represents the current eligible 
balance that could be called. 
• [[settlement]] Position Balance. Balance of [[securities]] 
representing only settled transactions; pending transactions 
not included. 
• [[collateral]] Out Balance. Balance of [[securities]] that belong to 
the safekeeping account indicated within this message and are 
deposited with a third party for the purpose of collateralization. 
Debit/Credit Indicator Note that for redemption events, a debit of the underlying security 
will always take place. A credit for either [[securities]] or cash is then 
made.  
Payment Date The date on which the redemption payment is made to the client 
account. 
[[Entitlement]] Units Units of face amount depending upon the security type (debt / non-
debt). 
 
 

---

## Page 87

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice Cancellati on (CAPC) 87 
CAPC 
 
 
Corporate Action Movement 
Preliminary Advice Cancellation 
 
What is a CAPC Message?  
The Corporate Action Movement Preliminary Advice Cancellation (CAPC) message cancels a CAPA 
message, indicating that the projected allocation will not take place. CAPC messages are always 
associated with a particular CAPA message through information provided in the Preliminary Movement [[ID]] 
– Business Message Identifier. 
CAPC messages will be generated upon subscription for both lottery and non-lottery events. 
  


---

## Page 88

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice Cancellati on (CAPC) 88 
The identifying information for a CAPC message is: 
MX Identifier ISO 20022  
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.044.002.xx10 
CA Movement 
Preliminary Advice 
Cancellation  
n/a CAPC MT 564 New 
 
When Are CAPC Messages Generated?  
Lottery Events 
CAPC messages for lottery events (DRAW, PDEF) are cancellations for previously sent CAPA messages 
(that detailed lottery results and their effect on a client’s account). CAPC messages are used for 
Redemption lottery events in these situations:  
1. An original lottery is canceled before allocation due to an event cancellation.  
2. A reversal / rerun of a partial call before allocation in which: 
• The original lottery results (detailed in the CAPA message) are canceled, and  
• A new event is being created and re-run. 
3. Both original and supplemental events are being canceled before allocation.  
A CAPC message is sent for each CAPA: one for the original event and one for the 
supplemental. The “Lottery Type” field links each CAPC message to its associated CAPA 
message. 
CAPC messages are not sent post-allocation. 
 
Non-Lottery Events 
CAPC messages are sent when a non-lottery event (MCAL, REDM) is canceled before allocation. They 
are not sent post-allocation. 
 
  
 
10 The last two digits in the MX Identifier signify the version number. The MX version number may change 
during the SWIFT annual release based on mandatory or optional updates to the standards.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 89

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice Cancellati on (CAPC) 89 
CAPC Message Subscriptions and Timing 
For both lottery and non-lottery events: 
• CAPC messages are available via file at 1:30 a.m. 
• In real time, CAPC messages are available hourly from 10:30 a.m. – 6:30 p.m. 
• CAPC messages are available after mainline date at 1:30 a.m. 
• A time stamp in the Business Application Header (BAH) allows you to verify message order. 
A CAPC subscription always requires a client’s subscription to CAPA messages.  
Conversely, a CAPA subscription does not require CAPC subscription. However, if a client subscribes to 
CAPA messages, it is suggested that the client subscribes to CAPC messages. 
 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times 
specified below. Exceptions are noted in the holiday processing schedule. 
 
Message Monday – Friday Saturday and Sunday 
CAPC Messages between 10:30 a.m. and 6:30 p.m. 
eastern time. 
Files transmitted at 1:30 a.m. eastern time. 
No messages or files 
transmitted. 
 
Holiday Processing Schedule 
U.S. and Canadian 
Holidays  
(both closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada 
closed) 
No messages or files are 
sent on: 
• New Year's Day 
• Labor Day, and 
• Christmas Day. 
Normal volumes occur on these 
days:  
• Dr. Martin Luther King, Jr. 
Day  
• Presidents' Day  
• Memorial Day  
• Independence Day, and 
• Thanksgiving Day. 
Files are transmitted based on 
customer subscription. 
Normal volumes occur on 
these days: 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day, 
and  
• Boxing Day. 
Files are transmitted based on 
customer subscription. 

---

## Page 90

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Preliminary Advice Cancellati on (CAPC) 90 
Information Contained on the CAPC Message 
Mapping for the message layout will conform to the ISO message rules.  
The following table contains some of the important information in the CAPC messages for lottery and 
non-lottery events. 
For more detailed technical information about message contents and elements, please see the Data 
Dictionary and/or My Standards for this message. 
 
Information Definition / Notes 
Message Type Part of the message header. Always set to “CAPC.” 
Official Corporate 
Actions Event [[ID]] 
Official Corporate Actions Identifier. This is the official, unique 
identifier for the corporate action. It is made up of the CA [[ID]] 
preceded by “US.” In order for this instruction to be accepted and 
processed, the COAF on the instruction must match the COAF on 
the announcement messages. 
Event Type • DRAW for partial calls. 
• PDEF for partial defeasances and partial pre-refundings. 
• MCAL for full calls and maturities. 
• REDM for final maturities and exchanges. 
• DFLT for defaults. 
Underlying Security Includes security description and [[CUSIP]] code. 
Lottery Information 
Lottery Events Only 
Includes items specific to lottery events, such as: 
• Lottery Type: 
o ORIG for original lottery. 
o SUPP for supplemental lottery. 
• Event Stage. 
• Lottery Sequence Number. 
• Lottery Date. 
Notification Type CAPC messages are always NEWM for new messages. 
Preliminary Movement 
[[ID]] 
This identification number links the CAPC message to the original 
CAPA message. It allows clients to associate the cancellation with 
a particular projected allocation. 
 
 

---

## Page 91

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Confirmation (CACO) 91 
CACO 
 
 
Corporate Action  
Movement Confirmation 
 
What is a CACO Message? 
The Corporate Action Movement Confirmation (CACO) message will be generated upon subscription for 
both lottery and non-lottery events. It confirms the movement of the redemption allocation (as projected in 
the CAPA message) into a client’s account. 
 
  


---

## Page 92

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Confirmation (CACO) 92 
The identifying information for a CACO message is: 
MX Identifier ISO 20022  
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.036.002.xx11 
CA Movement 
Confirmation 
supl.011.001.xx11 CACO MT 566 
Allocations/ 
Payments 
 
The message is sent per client account number. It is used to inform a client that a debit of the underlying 
security has been made from the client account for the redemption, and that a payment (of cash or 
[[securities]], depending upon the event) has taken place as a result. It contains a brief event summary and 
the payment information. 
Since CACO messages represent movement of cash and/or [[securities]] to and from your account, they are 
always new messages (NEWM). 
 
When Are CACO Messages Generated?  
CACO messages are generated and sent on the day that the allocation takes place.  
 
CACO Message Subscriptions and Timing 
Subscriptions  and Timing for Lotte ry Events 
Clients that subscribe to both CAPA and CACO for lottery events will not receive a CACO without having 
received a CAPA.  
For some events, generation of the CACO and CAPA happen simultaneously (e.g., in PDEF events: the 
lottery is run and the positions are moved directly afterward, causing the CAPA and CACO messages to 
be output at the same time). This does not happen for DRAW events.  
CACO messages are available via file at: 
• 12:30 a.m. 
• 1:30 p.m. 
• 2:30 p.m. 
• 3:30 p.m. 
 
11 The last two digits in the MX Identifier and the Extension code signify the version number. The MX 
version number and/or the Supplementary version number may change during the SWIFT annual release 
based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 93

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Confirmation (CACO) 93 
• 4:00 p.m. 
The messages are also available in real time every 20 minutes between 8:20 a.m. and 4:30 p.m. 
Subscriptions  and Timing for Non-Lottery Events 
Clients that subscribe to messaging for non-lottery events are required to receive CACO messages as 
part of the service. If a client opts not to receive CAPA/CAPC messages, the client must receive a CANO 
announcement message in order to receive a CACO message. 
CACO messages are available: 
• Via file at 4:00 p.m. 
• In real time every 20 minutes between 8:30 a.m. and 4:30 p.m.  
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times 
specified below. Exceptions are noted in the holiday processing schedule. 
 
Message Monday – Friday Saturday and Sunday 
CACO Messages between 8:20 a.m. and 7:00 p.m. 
eastern time based on customer subscription. 
Files transmitted at 4:00 p.m., 7:00 p.m., and 
1:30 a.m. eastern time, based on customer 
subscription. 
No messages or files 
transmitted. 
 
Holiday Processing Schedule 
U.S. and Canadian 
Holidays  
(both closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada 
closed) 
No messages or files are 
sent on: 
• New Year's Day 
• Labor Day, and 
• Christmas Day. 
Only Canadian payments occur 
on these days: 
• Dr. Martin Luther King, Jr. 
Day  
• Presidents' Day  
• Memorial Day  
• Independence Day, and 
• Thanksgiving Day. 
Files are transmitted based on 
customer subscription. 
Normal volumes occur on 
these days: 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day, 
and  
• Boxing Day. 
Files are transmitted based on 
customer subscription. 

---

## Page 94

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Confirmation (CACO) 94 
Information Contained on the CACO Message 
Mapping for the message layout will conform to the ISO message rules.  
All CACO messages contain [[securities]] debit information for the redemption event. Messages for all 
DRAW and PDEF events contain the “Lottery Type” field; REDM, DFLT, and MCAL events [[DO]] not. 
The following two tables contain some of the important information in the CACO messages for lottery and 
non-lottery events. 
For more detailed technical information about message contents and elements, please see the Data 
Dictionary and/or My Standards for this message. 
 
Information Definition / Notes 
Message Type Part of the message header. Always set to “CACO.” 
Official Corporate 
Actions Event [[ID]] 
Official Corporate Actions Identifier. This is the official, unique 
identifier for the corporate action. It is made up of the CA [[ID]] 
preceded by “US.” In order for this instruction to be accepted and 
processed, the COAF on the instruction must match the COAF on 
the announcement messages. 
Event Type • DRAW for partial calls. 
• PDEF for partial defeasances and partial pre-refundings. 
• MCAL for full calls. 
• REDM for final maturities and exchanges. 
• DFLT for defaults. 
Underlying Security Includes security description and [[CUSIP]] code. 
Lottery Information 
Lottery Events Only 
Includes items specific to lottery events, such as: 
• Lottery Type: 
o ORIG for original lottery. 
o SUPP for supplemental lottery. 
• Event Stage. 
• Lottery Sequence Number. 
• Lottery Date. 
Record Date  
(Pub Date – 1) 
Date/time at which positions are struck at the end of the day. 
Notification Type “NEWM” for new messages. 

---

## Page 95

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Confirmation (CACO) 95 
Balance Information Lottery and non-lottery events: 
• Confirmed Balance. 
• Total Eligible Balance. The current eligible balance for the 
event. For lottery events, this is the total amount that could 
be called. 
• [[settlement]] Position Balance. Balance of [[securities]] 
representing only settled transactions; pending transactions 
not included. 
• [[collateral]] Out Balance. The balance of [[securities]] that 
belong to the safekeeping account indicated within this 
message and are deposited with a third party for the 
purpose of collateralization. 
Lottery Events only: 
• Affected Balance. The portion of the eligible position that 
is called by the lottery. For partial pre-refundings, this is the 
refunded balance; for partial defeasements, this is the 
defeased balance. 
• Unaffected Balance. The portion of the eligible position 
that is not called by the lottery. For partial pre-refundings, 
this is the non-refunded balance; for partial defeasements, 
this is the non-defeased balance. 
Debit/Credit Indicator Note that for redemption events, a debit of the underlying security 
will always take place. A credit for either [[securities]] or cash is then 
made.  
Payment Date This applies to either: 
• The date on which cash was moved into your account for 
the redemption of the security that was debited above, or 
• The date on which your position was moved into new 
[[securities]] for PDEF events.  
 
The extension for the CACO message includes the following information: 
Information Definition / Notes 
Redemption [[ID]] A unique number systemically assigned to all lottery and non-lottery  
events in CA Web. 
Lottery Sequence 
Number 
for lottery events only 
A system-generated number to distinguish between the series of 
lotteries run against a particular redemption 

---

## Page 96

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Mov ement Confirmation (CACO) 96 
Balance Information 
for lottery events only 
• Original Balance. The original eligible balance as determined 
on record date. The original balance will remain constant for the 
life of the event, including any subsequent supplemental lottery 
CANO-E messages. 
• Unpledged Balance. The total number of [[shares]] this 
[[participant]] has pledged to any number of pledgee banks for this 
security. Individual pledge records record the security, number 
of [[shares]], [[participant]], pledgee bank, and loan date. 
• Investment Pledged Balance. The total quantity of [[securities]] 
segregated from the General Free account of a firm, partner, 
officer, stockholder, or an omnibus account. This account is 
used for reporting information to the IRS about [[securities]] 
purchased for investment purposes. Individual investment [[ID]] 
records contain position, serial number, and trade date. 
• Investment Unpledged Balance. The position held that 
represents the total quantity of [[securities]] segregated from the 
General Free account. Individual segregated records contain 
security, serial number and number of [[shares]]. Only serial 
numbers 1 – 5 can be accessed directly by participants. 
 
 
 
 

---

## Page 97

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Event Proc essing Status Advice Message (CAPS) 97 
 
What is a CAPS Message? 
The Corporate Action Event Processing Status Advice (CAPS) message is created for payments that were 
anticipated but not allocated on payment date. If a same-day position capture event does not allocate, a CAPS 
message will be sent per client account number at the end of the day. A reason code on the CAPS message 
explains why the allocation was not made. 
  
CAPS 
  
Corporate Action Event 
Processing Status Advice 


---

## Page 98

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Event Proc essing Status Advice Message (CAPS) 98 
The identifying information for a CAPS message is: 
 
MX Identifier ISO 20022  
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.032.002.xx12 
CA Movement 
Preliminary Advice 
Cancellation  
supl.010.001.xx12 CAPS MT 567 
Unallocated 
Positions 
 
When Are CAPS Messages Generated?  
CAPS messages for both lottery events (DRAW, PDEF) and non-lottery events (MCAL, REDM) are sent for 
non-allocated payments every day from payment date forward until the allocation is made. Each CAPS 
message is sent per CAPA message whenever the allocation specified in the CAPA does not occur. 
 
CAPS Message Subscriptions and Timing 
For both lottery and non-lottery events: 
• CAPS messages are available via file at 4:00, 5:00, and 7:00 p.m. 
• In real time, CAPS messages are available hourly from 1:00 p.m. – 7:00 p.m. 
• A time stamp in the Business Application Header (BAH) allows you to verify message order. 
 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times specified 
below. Exceptions are noted in the holiday processing schedule. 
 
Message Monday – Friday Saturday and Sunday 
CAPS Messages between 1:00 p.m. and 7:00 p.m. 
eastern time based on customer subscription. 
Files transmitted at 4:00 p.m., 5:00 p.m., and 
7:00 p.m. eastern time based on customer 
subscription 
No messages or files 
transmitted. 
 
12 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version 
number and/or the Supplementary version number may change during the SWIFT annual release based on 
mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards, [[DTCC]].com, and [[DTCC]]’s Learning Center. 

---

## Page 99

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Event Proc essing Status Advice Message (CAPS) 99 
Holiday Processing Schedule 
U.S. and Canadian 
Holidays  
(both closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada 
closed) 
No messages or files are 
sent on: 
• New Year's Day 
• Labor Day, and 
• Christmas Day. 
1:00 p.m., 2:00 p.m., and 3:00 
p.m. eastern time for P&I and 
foreign payments on these days: 
• Dr. Martin Luther King, Jr. 
Day  
• Presidents' Day  
• Memorial Day  
• Independence Day, and 
• Thanksgiving Day. 
Files are transmitted based on 
customer subscription. 
Normal volumes occur on 
these days: 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day, 
and  
• Boxing Day. 
Files are transmitted based on 
customer subscription. 
 
Information Contained on the CAPS Message 
Mapping for the message layout will conform to the ISO message rules.  
The following table contains some of the important information in the CAPS messages for lottery and non-
lottery events. 
For more detailed technical information about message contents and elements, please see the Data Dictionary 
and/or My Standards for this message. 
 
Information Definition / Notes 
Message Type Part of the message header. Always set to “CAPS.” 
Official Corporate 
Actions Event [[ID]] 
Official Corporate Actions Identifier. This is the official, unique 
identifier for the corporate action. It is made up of the CA [[ID]] 
preceded by “US.” In order for this instruction to be accepted and 
processed, the COAF on the instruction must match the COAF on 
the announcement messages. 
Event Type • DRAW for partial calls. 
• PDEF for partial defeasances, partial pre-refundings, and full 
pre-refundings. 
• MCAL for full calls and final paydowns. 
• REDM for final maturities and [[UIT]] terminations. 

---

## Page 100

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Event Proc essing Status Advice Message (CAPS) 100 
• DFLT for defaults. 
Non-Allocation Reason 
Information 
This series of fields explains why the allocation was not made. It 
includes: 
• Pending / No Specified Reason. This is used when an 
unallocated item has no ISO reason code available. It uses 
the code “NORE,” meaning that there is no reason code 
available or there is nothing to report. 
• Pending / Reason Code. If an ISO reason code is 
available, it is specified here: 
o NPAY. No payment made. See the Unallocated 
Reason Code in the message extension for more 
information. 
o OTHR. Indicates that there is another reason for 
the non-allocation. See the narrative in Additional 
Reason Information for details. 
• Additional Reason Information. This is a text field that, 
when present, details any additional information about the 
non-allocation. 
• Unallocated Reason Code. These codes appear in the 
message extension. They apply to the CAPS message 
when an event’s processing status is “Pending” and the 
reason code given in the core message is “NPAY” (for 
cash). 
The message extension provides the detailed reason for 
non-payment. 
Balance Information Lottery and non-lottery events: 
• Total Eligible Balance. Represents the eligible balance. 
• Original Balance. The original eligible balance as 
determined on record date. The original balance will remain 
constant for the life of the event, including any subsequent 
supplemental lottery CANO-E messages. 
• Pledged Balance. Portion of the Original Balance position 
held in the [[DTC]] General Free account as of the day prior to 
publication date. Position held in this account is subject to 
redemption lottery call. 
• Unpledged Balance. Total number of [[shares]] this 
[[participant]] has pledged to any number of pledgee banks for 
this security. Individual pledge records record the security, 
number of [[shares]], [[participant]], pledgee bank, and loan 
date. 
• Investment Pledged Balance. The total quantity of 
[[securities]] segregated from the General Free account of a 
firm, partner, officer, stockholder, or an omnibus account. 
This account is used for reporting information to the IRS 
about [[securities]] purchased for investment purposes. 
Individual investment [[ID]] records contain position, serial 
number, and trade date. 

---

## Page 101

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Corporate Acti on Event Proc essing Status Advice Message (CAPS) 101 
• Investment Unpledged Balance. Position held that 
represents the total quantity of [[securities]] segregated from 
the General Free account. Individual segregated records 
contain security, serial number and number of [[shares]]. Only 
serial numbers 1 – 5 can be accessed directly by 
participants. 
Lottery Events only: 
• Affected Balance. The portion of the eligible position that 
is called by the lottery. For partial pre-refundings, this is the 
refunded balance; for partial defeasements, this is the 
defeased balance. 
• Unaffected Balance. The portion of the eligible position 
that is not called by the lottery. For partial pre-refundings, 
this is the non-refunded balance; for partial defeasements, 
this is the non-defeased balance. 
• Obligated Balance. Obligated position occurs when the 
affected balance is greater than the settled position. This 
can happen when a call notice is received late and the prior 
record date position is greater than what is currently 
settled.  
Lottery Information 
for Lottery Events Only 
Includes items specific to lottery events, such as: 
• Lottery Type: 
o ORIG for original lottery, or 
o SUPP for supplemental lottery. 
• Lottery Date. 

---

## Page 102

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 102 
Appendix A: Message Scenarios 
Messaging Scenarios for Lottery Events 
Scenario 1: Partial Call ([[BASIC]]) 
This scenario illustrates the flow of messages that a client can expect to receive for a partial call event. An 
announcement is made, eligible balances are determined, the lottery is run, affected balances and associated 
entitlements are determined, and allocations are made and documented. 
 
Scenario 1: Partial Call 
 
The process starts with the Partial Call Announcement message (CANO). This message presents clients with 
details about the event, including record date, [[CUSIP]], and lottery date. The Redemption [[ID]] is given in the 
message extension. 
 


---

## Page 103

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 103 
The CANO is followed by the Eligible Balance message (CANO-E). This message provides information about a 
client’s eligible balance prior to the lottery being run. The total eligible balance is contained in the main body of 
the message, while additional balances describing the position the client may have can be found in both the 
core message and the message extension (when applicable). The client is informed of your eligible position 
based on the details of the partial call. 
 
The CAPA message is first sent when the lottery has been run. This message has two purposes. 
• First, it informs the client of the [[DTC]] lottery results.  
• Based on these results, this message also explains what portion of your eligible balance was 
affected (“called”) by the lottery, and what you can therefore expect to see in cash as a result of 
this event.  
The CAPA message also specifies the payment date and payment rate (if available) in the credit 
cash movement. The message shows a debit projection of the underlying [[CUSIP]]. 
 
 
The first CAPA sent is always a CAPA NEWM, or “new message.” CAPA REPL (“replacement”) messages are 
sent if any information on the CAPA NEWM has changed, such as the rate. 
Finally, the CACO message serves as a payment confirmation for the event. On payment date, your underlying 
[[CUSIP]] is debited and cash is moved to your account. The CACO message details the payment information 
regarding the partial call as well as lottery detail. 
 
  

---

## Page 104

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 104 
Scenario 2: Cancellation of a Partial Call (Pre-Lottery) 
This scenario demonstrates the message flow for a situation in which an announcement was made for an 
event, but the event was canceled before the lottery was run.  
In this case, you are informed of your eligibility, but the event is canceled before any determination has been 
made regarding your affected position. 
 
Scenario 2: Cancellation of a Partial Call (Pre- Lottery) 
 
The CANO and CANO-E messages are sent out as for a [[BASIC]] partial call. However, before the CAPA gets 
sent, a CACN message informs you that the event will not take place. 
 
  


---

## Page 105

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 105 
Scenario 3: Cancellation of a Partial Call (Pre-Allocation) 
As in Scenario 2, this scenario deals with the cancellation of a partial call event. In this case, however, the 
cancellation occurs after the lottery has been run but before the cash has been allocated.  
 
Scenario 3: Cancellation of a Partial Call (Pre-Allocation) 
 
The CANO, CANO-E, and CAPA messages are sent out as for a [[BASIC]] partial call: you are not only informed of 
the event and your eligible balance, but the lottery has been run and you are informed of your affected balance, 
the rate (if known), the projected debit to your underlying [[CUSIP]], your projected allocation, and the payment 
date. 
This time, the event is canceled between the pre-advice and the allocation. Since the lottery has already been 
run and the allocation has already been projected, there are two types of cancellation messages that are sent. 
The Event Cancellation (CACN) message cancels the CANO: it is sent to inform you that the event itself has 
been canceled. This refers only to the event, not to the lottery. 
The projection itself – that is, the lottery results and how they affect your position – must be canceled as well. 
The Lottery Projection Cancellation (CAPC) message retracts the CAPA: it informs you that the lottery results 
have been canceled. 


---

## Page 106

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 106 
Scenario 4: Cancellation of a Partial Call (Same-Day / Post-Allocation) 
As in Scenarios 2 and 3, this scenario deals with the cancellation of a partial call event. In this case, however, 
the cancellation occurs on the same day after the lottery has been run and after the cash has been allocated. 
 
 
Scenario 4a: Cancellation of a Partial Call (Same- Day, Post-Allocation): 1 of 2 
 
The CANO, CANO-E, and CAPA messages are sent out as for a [[BASIC]] partial call: you are not only informed of 
the event and your eligible balance, but the lottery has been run and you are informed of your affected balance, 
the rate (if known), the projected debit to your underlying [[CUSIP]], your projected allocation, and the payment 
date. 
On payment date, allocation is made and the CACO message serves as a payment confirmation for the event. 
On payment date, your underlying [[CUSIP]] is debited and cash is moved to your account.  
At this point, however, the event is canceled. A CACN message is sent to rescind the event that was originally 
announced in the CANO. 
This scenario concludes in the next diagram.  


---

## Page 107

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 107 
 
Scenario 4b: Cancellation of a Partial Call (Same- Day, Post-Allocation): 2 of 2 
 
After the event is rescinded, it needs to be reversed. A new CAPA is sent after the CACN, detailing what it is 
that will be reversed. Note that the details of the CAPA for the reversal mirror the CAPA for the event: they 
reflect what is being reversed, not what will happen as a result of the reversal. 
Note: The CARE message in gray (above) is not currently in use. In the near future, it will be used for 
same-day allocation reversals. At the moment, all post-allocation reversals – same-day or otherwise – 
are made via the CACO message. 
The CACO message will be used for adjustments if the CARE is not utilized. This occurs after payment date as 
CARE Messages will be sent only on payment date. Note that the details represent opposite movement from 
the CAPA messages: cash is debited from and [[securities]] are credited to the client account. 
 
  


---

## Page 108

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 108 
Scenario 5: Cancellation and Re-Run of a Partial Call (Pre-L ottery) 
As in Scenario 2, this scenario deals with the cancellation of a partial call event before a lottery has been run. 
In this case, the event is re-run after cancellation. 
  
 
Scenario 5a: Cancellation / Re- run of a Partial Call (Pre- Lottery): 1 of 2 
 
The CANO and CANO-E messages are sent out as for a [[BASIC]] partial call. A CAPA is not sent because no 
lottery has been run. The CACN message informs you that the event will not take place. 
After the event is canceled, a new Corporate Actions Event [[ID]] is assigned to the event. A new CANO is se nt: 
because the event was assigned a new [[ID]], this is therefore a NEWM.  
The scenario continues in the next diagram. 
 


---

## Page 109

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 109 
 
Scenario 5b: Cancellation / Re- run of a Partial Call (Pre- Lottery): 2 of 2 
 
The CANO-E is sent, detailing eligibility for the event under the new Corporate Actions Event [[ID]].  The lottery is 
then re-run, and a new CAPA message details the lottery results. 
On [[DTC]] Payment Date, the allocations are made. The CACO details the cash and security movements for the 
new event. 
 
  


---

## Page 110

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 110 
Scenario 6: Cancellation and Re-Run of a Partial Call (Po st-Lottery, Pre-Allocation) 
As in Scenario 3, the event is canceled post-lottery and pre-allocation. As before, the event is withdrawn and 
must be reversed. 
Here, however, a new event will take the place of the initial event.  
 
Scenario 6a: Cancellation and Rerun of a Partial Call (Post -Lottery, Pre-Allocation): 1 of 2 
 
The first portion of this cancellation happens as in Scenario 3: a CANO message announces the event, a 
CANO-E message details a client’s eligibility, a CAPA message informs the client of the lottery results and its 
affected balance, and a CACN message cancels the initial event.  
The CACN, however, contains an event stage indicator that informs the client that this is a non-standard lottery 
process. It is used in conjunction with the Lottery Type. The value “FULL” refers to the cancellation and re-run 
of an original lottery or an original and supplemental lottery. A subsequent lottery will be performed under a 
new event. 
After the cancellation, a new event is announced via a new CANO message, as was indicated by the event 
stage within the CACN message. This CANO contains the details for the replacement event. 
This process continues in the following diagram. 


---

## Page 111

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 111 
 
Scenario 6b: Cancellation and Rerun of a Partial Call (Post -Lottery, Pre-Allocation): 2 of 2  
 
The process continues from this point as for a regular Partial Call.  
The lottery is re-run and a new CAPA is sent, informing you of the lottery results and the effect the lottery will 
have on the client’s position and balances.  
On the new Payment Date, all allocations are made and a CACO message is sent as a payment confirmation 
for the event. On payment date, the client’s underlying [[CUSIP]] is debited and cash is moved to its account.  
  


---

## Page 112

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 112 
Scenario 7: Cancellation and Re-Run of a Partial Call (Po st-Allocation) 
In this situation, the event is canceled after the lottery has been run and allocation has occurred. All allocations 
made on the canceled event have to be reversed before the allocations on the second event can take place. 
 
Scenario 7a: Cancellation and Rerun of a Partial Call (Post -Allocation): 1 of 3 
 
The full event proceeds as in Scenario 1: The CANO is sent announcing the event, the CANO-E informs a 
client of its eligibility, the lottery is run, and the CAPA is sent announcing the lottery results. Allocation is made 
on payment date, and the CACO is sent post-allocation to confirm payment. 
At this point, however, the announcement is canceled and the lottery is re-run. The CACN is sent, announcing 
that the lottery is canceled. On the CACN, the Event Stage field’s value of “FULL” (used in conjunction with the 
Lottery Type field’s value of “ORIG”) informs you that this is a cancellation and re-run of an original lottery. A 
subsequent lottery will be performed under a new event. 
This process continues in the next diagram. 
 


---

## Page 113

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 113 
 
Scenario 7b: Cancellation and Rerun of a Partial Call (Post -Allocation): 2 of 3 
 
After the event is rescinded, it needs to be reversed. A new CAPA is sent after the CACN, detailing what it is 
that will be reversed. Note that the details of the CAPA for the reversal mirror the CAPA for the event: they 
reflect what is being reversed, not what will happen as a result of the reversal. 
Note: The CARE message in gray (above) is not currently in use. In the near future, it will be used 
for same-day allocation reversals. At the moment, all post-allocation reversals – same-day or 
otherwise – are made via the CACO message. 
The CACO message will be used for adjustments if the CARE is not utilized. This occurs after payment date as 
CARE Messages will be sent only on payment date. Note that the details represent opposite movement from 
the CAPA messages: cash is debited from and [[securities]] are credited to the client account. 
After the reversal is completed, a new event is announced via a new CANO message (as was indicated by the 
event stage within the CACN message). This CANO contains the details for the replacement event. 
This scenario concludes in the following diagram. 


---

## Page 114

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 114 
 
Scenario 7c: Cancellation and Rerun of a Partial Call (Post -Allocation): 3 of 3 
 
The CANO-E is sent, detailing eligibility for the event under the new Corporate Actions Event [[ID]].  The lottery is 
then re-run, and a new CAPA message details the lottery results. 
On the new [[DTC]] Payment Date, the allocations are made. The CACO details the cash and security 
movements for the new event. 
 
  


---

## Page 115

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 115 
Messaging Scenarios for Supplemental Lotteries 
Scenario 8: Supplementa l Lottery  
Supplemental lotteries are additional lotteries run on an event when the [[issuer]] needs to call additional quantity. 
They are processed under the same Event [[ID]] as the original lottery, and have many of the same 
characteristics as the original lottery (such as the record date and payment date). In the event messages, they 
can be distinguished by a value of “SUPP” for the Lottery Type element.  
The eligible balance is based on the unaffected balance of the original lottery. Please see the Account 
Balances section for more information on balance flows. 
The example that follows is of a supplemental lottery that has been run after an original lottery has been run 
but before the cash has been allocated. 
 
Scenario 8a: Supplemental Lottery (Post -Lottery, Pre-Allocation): 1 of 2 
 
A partial call occurs as usual: the CANO, CANO-E, and CAPA messages are sent out. You are informed of the 
event and your eligible balance, and the lottery has been run and you are informed of your affected balance, 
the rate (if known), the projected debit to your underlying [[CUSIP]], your projected allocation, and the payment 
date. 


---

## Page 116

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 116 
After you receive the CAPA with the lottery results, you receive an announcement message for a supplemental 
lottery on the same event. This second CANO specifies the supplemental lottery with the Lottery Type “SUPP.” 
This scenario continues with the following diagram (8b). 
 
 
Scenario 8b: Supplemental Lottery (Post -Lottery, Pre-Allocation): 2 of 2 
 
A second CANO-E (REPL) is sent; this one applies to the supplemental lottery. It specifies your eligibility 
based on the original lottery. Your unaffected balance in the original lottery becomes your eligible balance for 
the supplemental.  
After the supplemental lottery is run, a CAPA message is sent that details the lottery results. It does not 
replace the CAPA that was sent on the original lottery; the results detailed here are for the supplemental lottery 
only. The CAPA message will contain the original Event [[ID]]. 
Two CACO messages (also containing the original Event [[ID]]) are then sent after pay date: one to confirm 
payment for the original lottery, and one to confirm payment for the supplemental. The Lottery Type element 
specifies which lottery the message applies to: “ORIG” for the original lottery and “SUPP” for the supplemental. 
  


---

## Page 117

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 117 
Scenario 9: Supplementa l Lottery Pos t-Allocation 
Please see the introduction to Scenario 8 for an explanation of supplemental lotteries. 
The example that follows is of a supplemental lottery that has been run after an original lottery has been run 
and after the cash has been allocated.  
Essentially, the message flow is the same as for two partial calls. The major difference is that the second 
partial call is based on the first, composed of replacement messages for the CANO and CANO-E, and linked 
through the Corporate Action Event [[ID]]. 
 
Scenario 9a: Supplemental Lottery (Post -Lottery, Post-Allocation): 1 of 2 
 
The full event proceeds as in Scenario 1: The CANO is sent announcing the event, the CANO-E informs a 
client of its eligibility, the lottery is run, and the CAPA is sent announcing the lottery results. Allocation is made 
on payment date, and the CACO is sent post-allocation to confirm payment. 
This scenario concludes with the following diagram. 


---

## Page 118

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 118 
 
Scenario 9b: Supplemental Lottery (Post -Lottery, Post-Allocation): 2 of 2 
 
After payment date and allocation on the original lottery, a supplemental lottery is announced via a second 
CANO message. This replacement message uses the same Corporate Actions Event [[ID]] as the original lottery, 
but its “REPL” message type and its “SUPP” lottery type distinguish it as being an announcement of a 
supplemental lottery. 
 This is followed by a second CANO-E (REPL); this also refers to the supplemental lottery (SUPP). It specifies 
your eligibility based on the original lottery. Your unaffected balance in the original lottery becomes your eligible 
balance for the supplemental.  
After the supplemental lottery is run, a CAPA message is sent that details the lottery results. It does not 
replace the CAPA that was sent on the original lottery; the results detailed here are for the supplemental lottery 
only (SUPP). The CAPA message also contains the original Event [[ID]]. 
The CACO message (also containing the original Event [[ID]]) is then sent after allocation is made. The Lottery 
Type element of “SUPP” specifies that this was the payout for the supplemental lottery. 
 
  


---

## Page 119

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 119 
Scenario 10: Reversal / Re-Run of Original and Supplemental Lotteries 
This scenario deals with the reversal and re-run of a partial call event after both an initial lottery and a 
supplemental lottery have been called and run. Since no allocations have been processed, both lotteries will be 
re-run after the cancellation of the original event. 
 
Scenario 10a: Reversal / Re- Run of Original and Supplemental Lotteries: 1 of 3 
 
The partial call announcement is made in the original CANO, eligibility is announced in the original CANO-E, 
the lottery is run and its results are given in the original CAPA. Following this, a supplemental lottery is called 
in a CANO (REPL) message. The “SUPP” value for “Lottery Type” on this last message indicates that this is a 
supplemental lottery based on the first CANO message. 
This scenario continues in the following diagram. 


---

## Page 120

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 120 
 
Scenario 10b: Reversal / Re- Run of Original and Supplemental Lotteries: 2 of 3 
 
After the CANO is sent for the supplemental lottery, a CANO-E (REPL) message is sent, detailing the client’s 
eligibility under the supplemental lottery. After the supplemental lottery is run, a CAPA is sent that details how 
the client was affected by the supplemental lottery.  
At this point, the original event is canceled. A CACN reversal announcement is sent, announcing cancellation 
of the original event. Since the entire event is canceled, the cancellation applies to both the original and 
supplemental lotteries. 
The following CAPC message rescinds the results of the supplemental lottery (the CAPA message shown in 
the above diagram). 
This scenario concludes with the following diagram. 
 


---

## Page 121

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 121 
 
Scenario 10c: Reversal / Re- Run of Original and Supplemental Lotteries: 3 of 3 
 
Just as the results of the supplemental lottery were canceled with the CAPC message in the previous diagram 
(10b), the results of the original lottery are canceled with a second CAPC message (shown above). 
After the event and its associated lotteries have been canceled, the event is re-run. This re-running is now 
considered an original lottery (ORIG). A new Corporate Action Event [[ID]] is assigned and a CANO (NEWM) is 
sent, announcing the re-run. After the new [[DTC]] Position Capture Date, a CANO-E (NEWM) is sent, informing 
the client of its eligibility for the new lottery.  
The lottery is re-run and new lottery results are obtained. A CAPA containing the lottery results is sent to the 
client. A CACO is sent after payment date, informing the client of the payment that was made in satisfaction of 
the lottery.  
 
  


---

## Page 122

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 122 
Scenario 11: Cancellati on of Origina l and Suppl ementa l Lotteries  (Pre-Allocation) 
This scenario deals with the cancellation of a partial call event after both an initial lottery and a supplemental 
lottery have been called and run, but before any allocations have been made.  
 
Scenario 11a: Cancellation of Original and Supplemental Lotteries (Pre- Allocation): 1 of 2 
 
As in Scenario 10, the partial call announcement is made in the original CANO, eligibility is announced in the 
original CANO-E, the lottery is run and its results are given in the original CAPA. Following this, a 
supplemental lottery is called in a CANO (REPL) message. The “SUPP” value for “Lottery Type” on this last 
message indicates that this is a supplemental lottery based on the first CANO message. 
After the CANO is sent for the supplemental lottery, a CANO-E (REPL) message is sent, detailing the client’s 
eligibility under the supplemental lottery.  
This scenario concludes in the following diagram. 
 


---

## Page 123

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 123 
 
Scenario 11b: Cancellation of Original and Supplemental Lotteries (Pre- Allocation): 2 of 2 
 
After the supplemental lottery is run, a CAPA is sent that details how the client was affected by the 
supplemental lottery.  
At this point, the partial call event is canceled and a CACN message is sent. When an event is canceled, any 
associated lotteries are canceled as well. CAPC messages are sent for both the original and for the 
supplemental lotteries. 
  


---

## Page 124

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 124 
Scenario 12: Cancellati on of Origina l and Supplemental Lotteries (Same Day / Post-Allocation) 
 
 
Scenario 12a: Cancellation of Original and Supplemental Lotteries (Same- Day, Post-Allocation): 1 of 3 
 
As in Scenario 11, the partial call announcement is made in the original CANO, eligibility is announced in the 
original CANO-E, the lottery is run and its results are given in the original CAPA. Following this, a 
supplemental lottery is called in a CANO (REPL) message. The “SUPP” value for “Lottery Type” on this last 
message indicates that this is a supplemental lottery based on the first CANO message. 
After the CANO is sent for the supplemental lottery, a CANO-E (REPL) message is sent, detailing the client’s 
eligibility under the supplemental lottery.  
This scenario continues in the following diagram. 
 


---

## Page 125

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 125 
 
Scenario 12b: Cancellation of Original and Supplemental Lotteries (Same- Day, Post-Allocation): 2 of 3 
 
After the eligibility is announced, the supplemental lottery is run and a CAPA (NEWM) details the results. The 
allocation for both lotteries is made, and a CACO message confirms the movement of cash and [[securities]].  
After allocation is made, however, the event is canceled and a CACN message is sent. An event cancellation 
serves to cancel any and all lotteries that have taken place attached to that event. 
This scenario concludes in the following diagram. 
 
  


---

## Page 126

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 126 
 
 
Scenario 12c: Cancellation of Original and Supplemental Lotteries (Same- Day, Post -Allocation): 3 of 3 
 
After the event is rescinded, it needs to be reversed. This will happen using a message for each lottery. 
Note: The CARE message in gray (above) is not currently in use. In the near future, it will be used for 
same-day allocation reversals. At the moment, all post-allocation reversals – same-day or otherwise – 
are made via the CACO message. 
The CACO message presents the reversal details after the allocation has been reversed. Note that the details 
represent opposite movement from the CAPA messages: cash is debited from and [[securities]] are credited to 
the client account. 
 
  


---

## Page 127

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 127 
Scenario 13: Partial Call with Variable Rate 
In this scenario, off-cycle interest information is received on an event after the lottery has been run. 
 
 
Scenario 13a: Partial Call with Variable Rate: 1 of 2 
 
As for any partial call, the CANO (NEWM) announces the event, the CANO-E (NEWM) specifies a client’s 
eligibility under the event, the lottery is run, and the CAPA (NEWM) states the lottery results for individual 
clients. 
After the CAPA is sent to the client, accrued interest information is received on this off-cycle partial call. A 
replacement announcement containing this information must be sent. As such, a second CANO (REPL) is sent 
for the event, containing the rate information. 
This scenario concludes in the following diagram. 
 


---

## Page 128

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 128 
 
Scenario 13b: Partial Call with Variable Rate: 2 of 2 
 
After the replacement CANO has been sent, a replacement CAPA (REPL) must be sent.  
Note: A replacement CANO-E message is not necessary because the client’s eligibility has not 
changed. The allocations must be recalculated, however, to take the accrued interest rate into account. 
This requires a new projection and therefore a replacement CAPA. 
  


---

## Page 129

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 129 
Messaging Scenarios for PDEF Events 
Scenario 14: Partial Pre-Refunding 
In the case of a partial pre-refunding, the [[issuer]] has exercised its privilege to repay part of the debt security 
prior to maturity. The lottery determines how much of your balance in the original security will be affected. 
Functionally, it is very similar to a partial defeasance. The original [[CUSIP]] is surrendered and new [[securities]] 
are issued for the portion refunded and the portion non-refunded. 
 
Scenario 14: Partial Pre- Refunding 
 
The CANO message identifies the [[CUSIP]] that is being partially refunded (here, [[CUSIP]] A). In the Security 
Movement Details, you can see that [[CUSIP]] A is being debited and that two new CUSIPS are being created. 
• [[CUSIP]] B is identified as a new security for the refunded portion. You can see the earlier payment 
date for [[CUSIP]] B as well as the new-to-old ratio. 
• [[CUSIP]] C is identified as a new security for the non-refunded portion. It retains the original payment 
date. You can see the new-to-old ratio here as well. 


---

## Page 130

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 130 
A CANO-E message informs you of your eligibility. The only [[CUSIP]] relevant here is [[CUSIP]] A, the original 
security. 
Next, the lottery is run and a CAPA message is sent to inform you of the lottery results. Since the original 
[[CUSIP]] is being replaced by two new CUSIPS – refunded and non-refunded – you will have two new balances, 
one in each [[CUSIP]].  
• Your affected balance becomes your balance in [[CUSIP]] B, the refunded [[CUSIP]].  
• Your unaffected balance becomes your balance in [[CUSIP]] C, the non-refunded [[CUSIP]]. 
• Your entire balance in [[CUSIP]] A will be debited. 
Additionally, if your balance in the original security decreased between the record date and the lottery date (for 
instance, if you delivered out [[shares]] after record date), your obligated balance is noted on the CAPA. 
After all [[shares]] have been moved, a CACO message confirms the movement of all [[shares]] into the new 
refunded and non-refunded [[securities]]. 
 
  

---

## Page 131

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 131 
Scenario 15: Partial Pre-Refunding – Supple mental  (Pos t-L ottery) 
In this scenario, a supplemental lottery cannot occur under the original [[CUSIP]] because an original lottery has 
occurred and new [[securities]] have been allocated.  
Instead, a new lottery will be run: the position of the non-refunded balance from the original lottery becomes 
the "eligible balance" of the new lottery.   
 
Scenario 15a: Partial Pre- Refunding Supplemental (Post -Lottery): 1 of 2 
 
The CANO, CANO-E, CAPA, and CACO messages are sent just as in Scenario 14, detailing the underlying 
[[CUSIP]] (“A”) and the two new CUSIPs (“B” = refunded; “C” = non-refunded) that will result from the pre-
refunding event. A client’s eligibility is detailed in the CANO-E, a CAPA is sent to inform the client of the lottery 
results, the allocations from the old [[CUSIP]] to the two new CUSIPs are made on Payment Date, and a CACO 
confirms the movement of all [[shares]] from the underlying [[CUSIP]] to the refunded and non-refunded CUSIPs. 
At this point, the underlying [[CUSIP]] “A” is deleted. The affected balance in [[CUSIP]] “B” has a new maturity date. 
The remaining unaffected balance in [[CUSIP]] “C” has the same maturity date as the deleted underlying security. 
This scenario concludes in the following diagram. 


---

## Page 132

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 132 
 
 
Scenario 15b: Partial Pre- Refunding Supplemental (Post -Lottery): 2 of 2 
 
A new Corporate Action Event [[ID]] is assigned to the event.  
After this occurs, a supplemental lottery is called on the new event. The supplemental pre-refunding will be a 
new event based on the non-refunded [[CUSIP]] “C” for the additional called amount. [[CUSIP]] “C” will be debited 
for the additional amount. The balance of [[CUSIP]] “B” will be credited with that refunded amount. A new CANO 
message (NEWM) is sent for this supplemental lottery. 
Eligibility is determined and reported on a CANO-E (NEWM). A client’s eligibility is based on [[CUSIP]] “C.” 
The supplemental lottery is run and the results are reported on a CAPA (NEWM). The CAPA details the 
amount of [[CUSIP]] “C” that will be pre-refunded into [[CUSIP]] “B.” 
Allocation takes place on Payment Date. The CACO message confirms the movement of the called amount of 
[[CUSIP]] “C” into [[CUSIP]] “B.”  


---

## Page 133

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 133 
Scenario 16: Cancellation of a Partial Pre-Refunding (Pre-Lottery) 
This scenario demonstrates the message flow for a situation in which an announcement was made for a partial 
pre-refunding event, but the event was canceled before the lottery was run.  
In this case, you are informed of your eligibility, but the event is canceled before any determination has been 
made regarding your affected position. 
 
Scenario 16: Cancellation of a Partial Pre- Refunding (Pre- Lottery) 
 
The CANO and CANO-E messages are sent out as for a [[BASIC]] partial pre-refunding. However, before the 
CAPA gets sent, a CACN message informs you that the event will not take place. 
 
  


---

## Page 134

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 134 
Scenario 17: Cancellation of a Partial Pre-Refunding (Post-Lottery) 
This scenario demonstrates the message flow for a situation in which a lottery for a partial pre-refunding event 
has been run and allocated, but the event was canceled after allocations were made.  
 
 
Scenario 17: Cancellation of a Partial Pre- Refunding (P ost-Lottery) 
 
The CANO, CANO-E, CAPA, and CACO messages are sent just as in Scenario 14. A client’s eligibility is 
detailed in the CANO-E, a CAPA is sent to inform the client of the lottery results, the allocations are made on 
Payment Date, and a CACO confirms the movement of all [[shares]] from the underlying [[CUSIP]] to the refunded 
and non-refunded CUSIPs. 
At this point, the underlying [[CUSIP]] “A” is deleted. The affected balance in [[CUSIP]] “B” has a new maturity date. 
The remaining unaffected balance in [[CUSIP]] “C” has the same maturity date as the deleted underlying security. 
After this has taken place, the event is canceled. A CACN event recission message is sent to inform clients of 
the cancellation. 
Note: Position movements back to the original [[CUSIP]] (here, [[CUSIP]] “A”) will not currently appear via 
ISO 20022 messaging. These movements will be handled as adjustments that cannot currently be 
linked to the Corporate Action Event [[ID]] (COAF). 


---

## Page 135

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 135 
Scenario 18: Partial Defeasance 
In the case of a partial defeasance, the [[issuer]] sets aside cash in escrow to pay off a portion of the issue. The 
original [[CUSIP]] is surrendered, and new [[securities]] are issued for the portion defeased and the portion non-
defeased.  
 
Scenario 18: Partial Defeasance 
 
The CANO message identifies the [[CUSIP]] that is being defeased (here, [[CUSIP]] A). In the Security Movement 
Details, [[CUSIP]] A is being debited and two new CUSIPS are being created. 
• [[CUSIP]] B is identified as a new security for the defeased portion. The message details the earlier 
payment date for [[CUSIP]] B as well as the new-to-old ratio. 
• [[CUSIP]] C is identified as a new security for the non-defeased portion. It retains the original 
payment date. The message details the the new-to-old ratio here as well. 
A CANO-E message informs a client of its eligibility. The only [[CUSIP]] relevant here is [[CUSIP]] A, the original 
security. 


---

## Page 136

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 136 
Next, the lottery is run and a CAPA message is sent to inform the client of the lottery results. Since the original 
[[CUSIP]] is being replaced by two new CUSIPS – defeased and non-defeased – the client will have two new 
balances, one in each [[CUSIP]].  
• The affected balance becomes the balance in [[CUSIP]] B, the defeased [[CUSIP]].  
• The unaffected balance becomes the balance in [[CUSIP]] C, the non-defeased [[CUSIP]]. 
• The entire balance in [[CUSIP]] A is debited. 
Additionally, if the balance in the original security decreased between the record date and the lottery date (for 
instance, if you delivered out [[shares]] after record date), the obligated balance is noted on the CAPA. 
After all [[shares]] have been moved, a CACO message confirms the movement of all [[shares]] into the new 
defeased and non-defeased [[securities]]. 
 
 
  

---

## Page 137

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 137 
Scenario 19: Partial Defeasance Supplemental Lottery (Pre-Lottery) 
In this scenario, a supplemental lottery is called on a partial defeasance after initial eligibility has been 
announced but before the original lottery has been run. 
 
 
Scenario 19: Partial Defeasance Supplemental Lottery (Pre- Lottery) 
 
The CANO and CANO-E messages are sent just as in Scenario 18, detailing the underlying [[CUSIP]] (“A”) and 
the two new CUSIPs (“B” = defeased; “C” = non-defeased) that will result from the pre-refunding event. A 
client’s eligibility is detailed in the CANO-E.  
Before that lottery is run, however, a supplemental lottery is announced in a replacement CANO-E message 
(REPL). The CAPA message that follows serves as the results message for both the original and supplemental 
lotteries.  
Following this, the amounts outlined in the CAPA are allocated on Payment Date, and the CACO message 
confirms the amounts that were allocated as a result of both lotteries. After the CACO is sent, the underlying 
[[CUSIP]] (here, “[[CUSIP]] A”) is deleted. The new [[CUSIP]] (“B”) has a new maturity date for the affected balance. 
The remaining unaffected balance in [[CUSIP]] “C” has the same maturity date as the deleted underlying [[CUSIP]] 
(“A”).  


---

## Page 138

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 138 
Scenario 20: Partial Defeasance Supplemental Lottery (Post-Lottery) 
 
 
Scenario 20a: Partial Defeasance Supplemental (Post -Lottery): 1 of 2 
 
The CANO, CANO-E, CAPA, and CACO messages are sent just as in Scenario 18, detailing the underlying 
[[CUSIP]] (“A”) and the two new CUSIPs (“B” = defeased; “C” = non-defeased) that will result from the pre-
refunding event. A client’s eligibility is detailed in the CANO-E, a CAPA is sent to inform the client of the lottery 
results, the allocations from the old [[CUSIP]] to the two new CUSIPs are made on Payment Date, and a CACO 
confirms the movement of all [[shares]] from the underlying [[CUSIP]] to the refunded and non-refunded CUSIPs. 
At this point, the underlying [[CUSIP]] “A” is deleted. The affected balance in [[CUSIP]] “B” has a new maturity date. 
The remaining unaffected balance in [[CUSIP]] “C” has the same maturity date as the deleted underlying security. 
This scenario concludes in the following diagram. 
 


---

## Page 139

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 139 
 
Scenario 20b: Partial Defeasance Supplemental (Post -Lottery): 2 of 2 
 
A new Corporate Action Event [[ID]] is assigned to the event.  
After this occurs, a supplemental lottery is called on the new event. The supplemental defeasance will be a 
new event based on the non-refunded [[CUSIP]] “C” for the additional called amount. [[CUSIP]] “C” will be debited 
for the additional amount. The balance of [[CUSIP]] “B” will be credited with the portion defeased. A new CANO 
message (NEWM) is sent for this supplemental lottery. 
Eligibility is determined and reported on a CANO-E (NEWM). A client’s eligibility is based on [[CUSIP]] “C.” 
The supplemental lottery is run and the results are reported on a CAPA (NEWM). The CAPA details the 
amount of [[CUSIP]] “C” that will be pre-refunded into [[CUSIP]] “B.” 
Allocation takes place on Payment Date. The CACO message confirms the movement of the called amount of 
[[CUSIP]] “C” into [[CUSIP]] “B.” 
 
  


---

## Page 140

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 140 
Scenario 21: Cancellation of a Partial Defeasance (Pre-Lo ttery) 
This scenario demonstrates the message flow for a situation in which an announcement was made for a partial 
defeasance event, but the event was canceled before the lottery was run.  
In this case, you are informed of your eligibility, but the event is canceled before any determination has been 
made regarding your affected position. 
 
Scenario 21: Cancellation of a Partial Defeasance (Pre- Lottery) 
 
The CANO and CANO-E messages are sent out as for a [[BASIC]] partial defeasance. However, before the CAPA 
gets sent, a CACN message informs you that the event will not take place. 
 
  


---

## Page 141

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 141 
Scenario 22: Cancellation of a Partial Defeasance (Post-Lottery) 
This scenario demonstrates the message flow for a situation in which a lottery for a partial defeasance event 
has been run and allocated, but the event was canceled after allocations were made.  
 
 
Scenario 22: Cancellation of a Partial Defeasance (Post -Lottery) 
 
The CANO, CANO-E, CAPA, and CACO messages are sent just as in Scenario 18. A client’s eligibility is 
detailed in the CANO-E, a CAPA is sent to inform the client of the lottery results, the allocations are made on 
Payment Date, and a CACO confirms the movement of all [[shares]] from the underlying [[CUSIP]] to the defeased 
and non-defeased CUSIPs. 
At this point, the underlying [[CUSIP]] “A” is deleted. The new defeased [[CUSIP]] (“B”) has a new maturity date. The 
remaining unaffected balance in [[CUSIP]] “C” has the same maturity date as the deleted underlying security. 
After this has taken place, the event is canceled. A CACN event recission message is sent to inform clients of 
the cancellation. 
Note: Position movements back to the original [[CUSIP]] (here, [[CUSIP]] “A”) will not currently appear via 
ISO20022 messaging. These movements will be handled as adjustments that cannot currently be linked to the 
Corporate Action Event [[ID]] (COAF). 


---

## Page 142

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 142 
Scenario 23: Concurrent Late Partial Calls 
 
 
Scenario 23a: Concurrent Late Partial Calls: 1 of 2 
 
An initial partial call event (“Event A”) is announced and eligibility is determined (on CANO and CANO-E 
messages, respectively). 
Concurrently (and under a different Corporate Actions Event [[ID]]), a CANO (NEWM) is received for a second 
event (“Event B”) on the same security with a different payment rate for the same payment date. Since the 
lottery has not yet been run for Event A, a contra-[[CUSIP]] must be created. This contra-[[CUSIP]] is announced on 
the CANO for Event B. The following CANO-E (NEWM) message details the client’s eligibility for Event B. 
This scenario concludes in the following diagram. 
 


---

## Page 143

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 143 
 
Scenario 23b: Concurrent Late Partial Calls: 2 of 2 
 
After the lottery is run for Event A, the client receives a CAPA message detailing the lottery results for that 
event. The unaffected balance specified on the CAPA becomes the affected balance for Event B. Each client’s 
eligibility for Event B is re-determined and reported on the CANO-E (REPL) message. 
At this point, the lottery is run for Event B. Lottery results are reported in a second CAPA (NEWM). The 
underlying [[CUSIP]] is debited and the contra-[[CUSIP]] is credited. The contra-[[CUSIP]] will then be debited to credit 
the cash. 
On the payment date for each event, two CACO (NEWM) messages announce the allocation of their 
associated events. The CACO for Event A shows the cash allocation from the underlying [[CUSIP]]. The CACO 
for Event B shows the credit to the contra-[[CUSIP]] and .its movement into cash. 
  


---

## Page 144

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 144 
Scenario 24: Concurrent Partial Calls (No Contra-[[CUSIP]]) 
 
 
Scenario 24a: Concurrent Partial Calls (no Contra- [[CUSIP]]): 1 of 2  
 
An initial partial call event (“Event A”) is announced and eligibility is determined (on CANO and CANO-E 
messages, respectively).The lottery is run and the CAPA message details the lottery results and pre-advice. 
Meanwhile, a CANO (NEWM) is received for a second event (“Event B”) on the same security under a different 
Corporate Actions Event [[ID]]. It has a different payment rate for the same payment date. Because the lottery for 
Event A has already been run, Event B does not require a contra-[[CUSIP]].  
The following CANO-E (NEWM) message details the client’s eligibility for Event B. The unaffected balance on 
the CAPA for Event A becomes the total eligible balance on the CANO-E for Event B. 
This scenario concludes in the following diagram. 
 


---

## Page 145

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 145 
 
Scenario 24b: Concurr ent Partial Calls (No Contra- [[CUSIP]]):2 of 2 
 
After the lottery is run for Event B, the client receives a CAPA message detailing the lottery results for that 
event. The underlying security is debited and the client receives a cash credit. 
On the payment date for each event, two CACO (NEWM) messages announce the allocation of their 
associated events. The CACO for Event A shows the cash allocation from the underlying [[CUSIP]]. The CACO 
for Event B shows the cash allocation from the “unaffected” portion of the balance remaining after Event A has 
been allocated. 
  


---

## Page 146

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 146 
Messaging Scenarios for Non-Lottery Events 
Scenario 25: Full Call 
In a full call, all [[shares]] are called back for redemption by the [[issuer]]. 
 
Scenario 25: Full Call 
 
The CANO message announces the event. The CAPA message details what a particular client will be 
receiving as a result of the full call. After payment date, the CACO message details the allocations that were 
made. 
 
  


---

## Page 147

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 147 
Scenario 26: Cancellation of a Full Call (Pre-Allocation) 
The security [[issuer]] announces a full call: all [[shares]] of a security are called back for redemption by the [[issuer]]. 
Before the redemption occurs, however, the event is rescinded. 
 
 
Scenario 26: Full Call Cancellation (Pre- Allocation) 
 
The CANO and CAPA messages are sent out as for a [[BASIC]] full call: clients are informed of the event, the 
projected debit to the underlying [[CUSIP]], the projected allocation, and the payment date. 
In this case, though, the event is canceled between the pre-advice and the allocation. Since the allocation has 
been projected, there are two cancellation messages that are sent by [[DTCC]]: 
• The Event Cancellation (CACN) message corresponds to the CANO: it is sent to inform clients that 
the event itself has been rescinded and will no longer take place.  
• The Projection Cancellation (CAPC) message corresponds to the CAPA: it informs clients that the 
projected allocation will not take place. The Preliminary Movement [[ID]] has the same value as the 
Business Message Identifier on the CAPA. 
 
  


---

## Page 148

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 148 
Scenario 27: Cancellation of a Full Call (Post-Allocation) 
This scenario deals with the cancellation of a full call event. In this case, however, the cancellation occurs on 
the same day after the cash has been allocated. 
 
 
Scenario 27a: Full Call Cancellation (Post -Allocation): 1 of 2 
 
The CANO and CAPA messages are sent out as for a [[BASIC]] full call: a client is not only informed of the event, 
but also of the affected balance, the rate (if known), the projected debit to the underlying [[CUSIP]], the projected 
allocation, and the payment date. 
On payment date, allocation is made and the CACO message serves as a payment confirmation for the event. 
On payment date, the underlying [[CUSIP]] is debited and cash is moved to the client account.  
At this point, however, the event is canceled. A CACN message is sent to rescind the event that was originally 
announced in the CANO.  
After the event is rescinded, it needs to be reversed. A new CAPA is sent after the CACN, detailing what it is 
that will be reversed. Note that the details of the CAPA for the reversal mirror the CAPA for the event: they 
reflect what is b eing reversed, not what will happen as a result of the reversal. 
This scenario concludes in the next diagram. 
 


---

## Page 149

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 149 
 
Scenario 27b: Full Call Cancellation (Post -Allocation): 2 of 2 
 
Note: The CARE message in gray (above) is not currently in use. In the near future, it will be used for 
same-day allocation reversals. At the moment, all post-allocation reversals – same-day or otherwise – 
are made via the CACO message. 
The CACO message presents the reversal details after the allocation has been reversed. Note that the details 
represent opposite movement from the CAPA messages: cash is debited from and [[securities]] are credited to 
the client account. 
 
  


---

## Page 150

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 150 
Scenario 28: Cancellation and Re-Run of a Full Call (Pre-Allocation) 
As before, the security [[issuer]] announces a full call: all [[shares]] of a security are called back for redemption by 
the [[issuer]]. Before the redemption occurs, the event is rescinded. Here, however, a new event will take the 
place of the initial event.  
 
 
Scenario 28a: Cancellation and Re- Run of a Full Call (Pre- Allocation): 1 of 2 
 
The first portion of this cancellation happens as in Scenario 26. The CANO and CAPA messages are sent out 
as for a [[BASIC]] full call: clients are informed of the event, the projected debit to the underlying [[CUSIP]], the 
projected allocation, and the payment date. 
After the projection advice is sent, the event is canceled. A CACN message rescinds the original CANO that 
was sent. Since the allocations were projected in the CAPA, those projections must be canceled as well: the 
CAPC message cancels those projections. 
After the cancellation, a new event is announced via a new CANO message. This CANO contains the details 
for the replacement event, including the new Corporate Actions Event [[ID]]. 
This scenario concludes in the following diagram. 


---

## Page 151

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 151 
 
Scenario 28b: Cancellation and Re- Run of a Full Call (Pre- Allocation): 2 of 2 
 
The process continues from this point as for a regular full call.  
A new CAPA is sent, informing the client of its projected allocation associated with the new event.  
On the new payment date, all allocations are made and a CACO message is sent as a payment confirmation 
for the event. On payment date, the client’s underlying [[CUSIP]] is debited and cash is moved to the client’s 
account. 
 
 
  


---

## Page 152

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 152 
Scenario 29: Cancellation and Re-Run of a Full Call (Post-Allocation) 
In this situation, the event is canceled after allocation has occurred. All allocations made on the canceled event 
have to be reversed before the allocations on the second event can take place. 
 
Scenario 29a: Cancellation and Rerun of a Full Call (Post -Allocation): 1 of 2 
 
The full event proceeds as in Scenario 27. The CANO and CAPA messages are sent out as for a [[BASIC]] full 
call: a client is not only informed of the event, but also of the affected balance, the rate (if known), the projected 
debit to the underlying [[CUSIP]], the projected allocation, and the payment date. 
On payment date, allocation is made and the CACO message serves as a payment confirmation for the event. 
On payment date, the underlying [[CUSIP]] is debited and cash is moved to the client account. 
In this example, the event is canceled due to an invalid payment date. A CACN message is sent to rescind the 
event that was originally announced in the CANO. 
After the event is rescinded, it needs to be reversed. A new CAPA is sent after the CACN, detailing what it is 
that will be reversed. 
• The details of the CAPA for the reversal mirror the CAPA for the event: they reflect what is being 
reversed, not what will happen as a result of the reversal. 
• A Reversal Reason Code gives an explanation for why this projection is being reversed: in this 
case, the invalid payment date. 
This scenario concludes in the following diagram. 
 


---

## Page 153

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 153 
 
Scenario 29b: Cancellation and Rerun of a Full Call (Post -Allocation): 2 of 2 
 
The CACO message confirms the reversal details after the allocation has been reversed. Note that the details 
represent opposite movement from the CAPA messages: cash is debited from and [[securities]] are credited to 
the client account. 
After the reversal is completed, a new event is announced via a new CANO message (as was indicated by the 
event stage within the CACN message). This CANO contains the details for the replacement event. 
The new CAPA message specifies the allocation projections. After payment is made, the CACO details the 
cash and security movements for the new event. 
 
  


---

## Page 154

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 154 
Scenario 30: Maturity  
Functionally, the message sequence for a maturity is identical to that of a full call.  
 
Scenario 30: Maturity 
 
The CANO message announces the event. The CAPA message details what a particular client will be 
receiving as a result of the maturity. After payment date, the CACO message details the allocations that were 
made. 
 
 
  


---

## Page 155

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 155 
Scenario 31: [[UIT]] Termina ti on 
Functionally, the message sequence for the termination of a unit investment trust is identical to that of a full 
call.  
 
Scenario 31: [[UIT]] Termination 
 
The CANO message announces the event. The CAPA message details what a particular client will be 
receiving as a result of the [[UIT]] termination. After payment date, the CACO message details the allocations that 
were made. 
 
 


---

## Page 156

User Guide: ISO 20022 Messaging for Redemptions Entitlements and Allocations  
Appendix A: Mess age Sc enarios 156 
Scenario 32: Full Pre-Refunding 
Functionally, the message sequence for a full pre-refunding is identical to that of a full call.  
 
Scenario 32: Full Pre- Refunding 
 
The CANO message announces the event. The CAPA message details what a particular client will be 
receiving as a result of the full pre-refunding. After payment date, the CACO message details the allocations 
that were made. 
 


---

## Page 157

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 