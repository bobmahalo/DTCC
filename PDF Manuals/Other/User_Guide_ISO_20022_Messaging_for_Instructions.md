---
title: "ISO 20022 Messaging for Distributions Instructions"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/User_Guide_ISO_20022_Messaging_for_Instructions.pdf"
pages: 61
size: "2360.5 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO 20022 Messaging for Distributions Instructions

**Original File:** [User_Guide_ISO_20022_Messaging_for_Instructions.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/User_Guide_ISO_20022_Messaging_for_Instructions.pdf)  
**Category:** Other  
**Total Pages:** 61  
**File Size:** 2360.5 KB  

---

## Page 1

 
 
 
USER GUIDE 
ISO 20022 MESSAGING FOR DISTRIBUTIONS INSTRUCTIONS  
VERSION 2.1 
MARCH 09, 2021 
 


---

## Page 2

 
 
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by  certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in wh ich such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
This guide is meant as an educational tool to assist in your understanding o f ISO 20022 messaging as it relates to 
corporate action processing at [[DTCC]]. It should not be used as a basis for systems applications coding. For coding 
purposes, please refer to specific schemas and message implementation guides that can be found h ere
. 
 
Doc Info: March 09, 2021 
Publication Code:  CA221 
Service: Corporate Actions  
Title: User Guide: ISO 20022 Messaging for Distributions Instructions  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
An Introduction to ISO 20022 Messaging ........................................................................................... 5 
What is ISO 20022 Messaging? ........................................................................................................ 5 
Benefits of Using ISO 20022 Messaging for Corporate Actions .............................................................. 5 
How Can I Learn More?................................................................................................................... 6 
Co rpo rate Actio ns  Mess ag es  in the Instructio ns Wo rkflo w..................................................................... 7 
How to Read an MX Identifier ........................................................................................................... 7 
[[BASIC]] Message Flow of the Distribution Lifecycle ................................................................................. 8 
Instructions Services Currently Supported by ISO 20022 Messaging for Distributions................................ 9 
Ins tructio ns Proc es sing.................................................................................................................. 10 
[[BASIC]] Instruction Message Flow..................................................................................................... 10 
Instruction Flow with Instruction Cancellation ................................................................................... 12 
Processing Periods and Cutoff Information ...................................................................................... 13 
Example of a Corporate Action Event Processed via ISO 20022 ......................................................... 15 
Corporate Action Instruction Messages (CAIN) ................................................................................ 19 
What Is  a CAIN Mess ag e? ............................................................................................................. 19 
Information Contained on the CAIN Message.................................................................................... 20 
Supp lementary Data .................................................................................................................... 22 
Ex amp les ................................................................................................................................... 22 
Rules .......................................................................................................................................... 24 
Rules fo r All Instruc tio n Mess ag es .................................................................................................  24 
Additional Rules .......................................................................................................................... 25 
Instructions: Specific Rules ........................................................................................................... 26 
Corporate Action Instruction Status Advice Messages (CAIS)........................................................... 29 
What Is a CAIS message? ............................................................................................................. 29 
Information Contained on the CAIS Message .................................................................................... 30 
CAIS Reject Codes ....................................................................................................................... 33 
Reject Codes .............................................................................................................................. 33 
“OTHR” Code Reasons ................................................................................................................ 34 

---

## Page 4

 
 
Troubleshooting Mess ag e Rejec tion ................................................................................................ 35 
General...................................................................................................................................... 36 
Corporate Action Instruction .......................................................................................................... 37 
Supplementary  D ata .................................................................................................................... 38 
Co untry Cod es ............................................................................................................................. 40 
Corporate Action Instruction Cancellation Request Messages (CAIC) ............................................... 48 
What Is  a CAIC Mess ag e? ............................................................................................................. 48 
Information Contained on the CAIC Message.................................................................................... 49 
Rules for All Cancellation Messages ................................................................................................ 49 
General Message Processing Rules ............................................................................................... 49 
Additional Rules .......................................................................................................................... 50 
Corporate Action Cancellation Status Advice Messages (CACS) ....................................................... 52 
What is a CACS message? ............................................................................................................ 52 
Information Contained on the CACS Mess ag e .................................................................................. 53 
Reject Codes ............................................................................................................................... 55 
Reject Codes .............................................................................................................................. 55 
“OTHR” Code Reasons ................................................................................................................ 56 
Troubleshooting Message Rejection ................................................................................................ 56 
Corporate Action Statement Report (CAST) ..................................................................................... 58 
What is a CAST Message? ............................................................................................................ 58 
Information contained  o n the CAST mes s age.................................................................................... 59 
Rules for CAST Mess ag es ............................................................................................................. 59 
General Message Processing Rules ............................................................................................... 59 
Inclusions in the CAST Messages ................................................................................................ .. 59 
Mess ag e Timing.......................................................................................................................... 60 
 

---

## Page 5

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 5 
AN INTRODUCTION TO ISO 20022 MESSAGING 
What is ISO 20022 Messaging? 
ISO 20022 is an international messaging standard that is designed to simplify global business communication 
by creating a common language for communicating financial information that is unrestricted by national borders 
or regional conventions.  
Even though the Depository has maintained its own proprietary formats since its creation in 1973, [[DTC]] 
recognized that it needed to respond to an evolving business environment and to accommodate an 
increasingly global investment business. [[DTC]]'s participants and customers had expanded their businesses 
throughout the world and wanted to streamline, as much as possible, the standards and formats used to 
communicate. ISO 20022 meets those needs and offers a host of benefits. 
[[DTC]] is therefore moving all of its corporate actions processing from proprietary formats to this external, 
international format. 
Benefits of Using ISO 20022 Messaging for Corporate Actions 
One of the greatest benefits of ISO 20022 is its consistency and universality across the industry and around 
the globe. It provides a common language with its own ever-growing dictionary, enabling businesses in the 
financial industry to communicate corporate action information quickly, easily, and precisely.  
On a more local scale, [[DTC]] currently processes 500,000 Elective [[Dividend]] Service (EDS) instructions entered 
manually by clients via [[DTC]]’s [[participant]] Terminal System ([[PTS]]) and [[participant]] Browser Service ([[PBS]]). The 
automation of this manual process via ISO 20022 messaging provides a significant cost savings to participants 
and a tremendous reduction in risk to the industry. 
The Corporate Actions Transformation Learning Center provides a more comprehensive list of benefits
. 

---

## Page 6

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 6 
How Can I Learn More? 
Visit the Corporate Actions area of the [[Asset]] Services Learning Center at https://dtcclearning.com/products-
and-services/[[Asset]]-services.html to view a wealth of business and technical information about the initiative, 
including the Benefits page and video, a Getting Started section, and a Readiness Checklist that provides you 
with a convenient method for determining your organization’s ability to begin processing ISO 20022 messages. 
 
The Learning Center also contains introductory videos, extensive documentation, a link to FAQs, and further 
information regarding ISO 20022 messages and message scenarios. 
First-time users should click Register Now in order to create an account. You need to be registered in order to 
view the Learning Center. 


---

## Page 7

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 7 
Corporate Actions Messages in the Instructions Workflow 
There are fifteen types of messages in the ISO 20022 group: 
 
The messages specifically involved in the instructions process are: 
• Corporate Action Announcement Message (CANO) 
• Corporate Action Instruction Message (CAIN) 
• Corporate Action Instruction Status Advice Message (CAIS) 
• Corporate Action Cancellation Request Message (CAIC) 
• Corporate Action Cancellation Status Advice Message (CACS) 
• Corporate Action Statement Report Message (CAST) 
 
The CANO message is an essential component of the instruction process in that it outlines the critical elements 
of the event such as identifier and [[Option]] numbers, among others. While the CANO is important, this User 
Guide explores five messages on the list: CAIN, CAIC, CAIS, CACS, and CAST. 
How to Read an MX Identifier 
The MX Identifier identifies the business area, message [[ID]], and version of an ISO Message. 
As an example, for the identifier seev.040.002.06: 


---

## Page 8

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 8 
• The first four alphabetic characters (“seev”) identify the business area. In this case, it is “[[securities]] 
Events.” You can see the full list of business areas on the ISO 20022 Web site at 
http://www.iso20022.org/documents/general/ISO20022_BusinessAreas.pdf. 
• The next three characters (040) are the message identifier. The message in this example is a CAIC 
message. 
• The next three characters (002) are the “variant” identifier. Since “001” is always the main ISO message, 
“002” would be the second variant (and the one that is compatible with ISO 15022). [[DTC]] is using the 
second variant in order to comply with the industry’s requirement that the ISO 20022 messages we 
generate be backward compatible with ISO 20022. 
• The last two characters (06) are the “version.” In this example, this is the sixth version of this message, 
representing SR 2015. 
For your coding purposes, be sure to consult the latest documentation for the most current 
version number. 
[[BASIC]] Message Flow of the Distribution Lifecycle 
The following graphic provides a high-level view of the [[BASIC]] flow of the distribution lifecycle.  
Note: 
Throughout this document, blue boxes represent inbound instructions to [[DTC]] from the [[participant]] and green boxes 
represent outbound instructions to the [[participant]] from [[DTC]].  
 
1. [[DTC]] sends a CANO to the [[participant]] that announces the corporate action event. The CANO contains an 
indicator signaling that the event is eligible for ISO 20022 instruction messaging. 
Note: 
The CANO messages are not discussed in this User Guide as they are announcement messages only.  
2. [[DTC]] sends a follow-up message (CANO-E) to inform the [[participant]] about how it is specifically affected by 
the corporate action: its eligibilities and options. 
3. The [[participant]] submits a CAIN message to [[DTC]], providing instructions for that event. 
4. [[DTC]] sends a CAIS message containing status information about the instructions back to the [[participant]]. 
5. [[DTC]] sends a CAPA message to the [[participant]] projecting its payment/allocation. 


---

## Page 9

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 9 
6. After all actions specified in the CAIN (and any in the follow-up messages not specified in this flow) have 
been taken, [[DTC]] sends the [[participant]] a CACO message to confirm movement of payment/allocation 
proceeds.  
Note: 
The CAPA and CACO messages are not discussed in this User Guide, as they are payment processing messages.  
Please see the Instructions Processing section for a more detailed explanation and examples of alternate 
process flows. For specific message information, visit the Learning Center’s Messages and Scenarios 
page at https://dtcclearning.com/learning/assetservices/products/corporate-actions-reengineering-
new/technology-information/messages-and-scenarios.html. 
Instructions Services Currently Supported by ISO 20022 Messaging 
for Distributions 
Foreign Currency Payments (FCP) and Foreign Tax Relief (FOR) may be instructed on singly or as multiple 
options. Depending on the structure of the event, FCP and FOR may be combined with each other, as well as 
combined with [[Dividend]] Reinvestment (DRIP). 
• Foreign Currency Payments (FCP). A foreign currency payment instruction is one in which a [[participant]] 
can elect to receive dividends in U.S. dollars or in foreign currency. 
• Foreign Tax Withholdings (Tax Relief) (FOR). Qualifying beneficial owners can obtain tax relief "at-
source" or via an accelerated refund on certain foreign issues as a result of tax relief arrangements 
established with issuers, agents, or the tax authorities of various countries. 
Not every jurisdiction and event type is supported. Clients should consult with [[DTC]] and the ISO 20022 
Message Usage Guidelines for those details. Additionally, all events that are in scope for automated 
instructions messaging are indicated by a “Yes/No” value for the EDS Messaging Eligibility Flag on the 
ISO 20022 CANO Announcement message. 
Note: 
In SR 2019, this flag will be renamed “Instructions Messaging Eligibility Flag.”  
• Optional Dividends (OPS). The Optional [[Dividend]] service (OPS) allows participants to receive income 
payments in the form of cash, [[Stock]], or a combination of both. “[[Dividend]] with [[Option]]” is the only event 
type eligible for the Optional [[Dividend]] service. 
The Optional [[Dividend]] service can be instructed as an [[Option]] singly or be combined with Foreign 
Currency Payments (FCP) and Foreign Tax Withholdings (Tax Relief) (FOR) for cash distributions.  
Likewise, the event structure will allow Foreign Currency Payments and Foreign Tax Relief to b e 
instructed on singly or as multiple options. 
• DRIPs including Opt-outs (DRP). The [[Dividend]] Reinvestment program allows participants to instruct to 
reinvest income payments for additional [[shares]] of [[Stock]] for eligible issues which have a [[Dividend]] 
Reinvestment program. Participants will be able to send DRP instructions, including DRP OPT-OUT f or 
uninstructed positions. 
 
The following services are not supported by ISO 20022 messaging: 

---

## Page 10

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 10 
• [[Cash-in-Lieu]]/Round-up Service, 
• US Tax Withholding,  
• Tax Reclaim, and 
• Direct Payment Service. 
Note: 
You can submit instructi ons for these services via the Corporate Actions browser.  
Instructions Processing 
[[BASIC]] Instruction Message Flow 
The process in its most [[BASIC]] form was presented above. This section illustrates the flow in more detail and 
discusses some of the variants that may occur within that flow. 
The two diagrams immediately following present a more detailed version of the [[BASIC]] flow. 
 
1. [[DTC]] distributes the corporate action announcement with the information specified abov e. 


---

## Page 11

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 11 
2. On the [[DTC]] Position Capture Date, [[DTC]] distributes the CANO-E with specific eligibility information for the 
[[participant]] (for instance, total eligible balance for instructions and the [[participant]]’s instruction options). 
3. Once the [[DTC]] instruction period begins, the [[participant]] sends a CAIN message to [[DTC]] that contains the 
information specified above. 
4. After the CAIN is received, [[DTC]] sends back a CAIS status message. This status message will inform the 
[[participant]] whether the CAIN was accepted or rejected, giving the [[participant]] the opportunity to send a 
corrected CAIN if necessary. 
Note: 
Steps 3 and 4 of this process can be repeated multiple times during the instruction period.  
The process continues with the following diagram. 
 
5. Beginning on cutoff date minus five through cutoff date minus one, [[DTC]] sends a CAST report at the end 
of every day on which instructions are received from the [[participant]]. This report summarizes all of the 
instruction information that has taken place on that business day, takes into consideration any instructions 
that have been sent and confirmed on prior days in the instruction period, and aggregates it into an end-
of -day report. The CAST includes instructions received both via ISO 20022 messaging and via the 
Corporate Actions browser. 


---

## Page 12

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 12 
Note: 
A firm does not need to employ ISO messaging in order to receive the CAST report; the CAST report is available to all 
firms. 
6. On Payable Date minus 7, [[DTC]] sends a CAPA message to the [[participant]]. This recaps the total actions 
that will be taken on the allocation date. 
7. On the Allocation Date, [[DTC]] makes the final cash/[[securities]] movements, including moving any 
uninstructed positions to the [[default]], and sends the [[participant]] an allocation confirmation message, or 
CACO. 
Instruction Flow with Instruction Cancellation 
As mentioned above, the [[participant]] can send multiple instruction messages to [[DTC]] during the instruction 
period. Likewise, the [[participant]] can cancel one or more of those instruction messages. 
 
1. On the [[DTC]] Position Capture Date, [[DTC]] distributes the CANO-E that captures the total eligible balance 
with specific eligibility instructions for the [[participant]]. 
2. Once the [[DTC]] instruction period begins, the [[participant]] sends a CAIN message to [[DTC]] that contains the 
information specified above. 
3. After the CAIN is received, [[DTC]] sends back a CAIS status message. This status message will inform the 
[[participant]] whether the CAIN was accepted or rejected, giving the [[participant]] the opportunity to send a 
corrected CAIN, if necessary. 
Note: 


---

## Page 13

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 13 
Steps 3 and 4 of this process can be repeated multiple times during the open instruction period.  
4. If the [[participant]] opts to cancel a CAIN message sent in step 3 above, the [[participant]] sends a CAIC 
cancellation message request to [[DTC]] during the instruction period. 
5. [[DTC]] responds to the cancellation request with a CACS status message. This status message will inform 
the [[participant]] whether the CAIC was accepted or rejected, giving the [[participant]] the opportunity to send a 
corrected CAIC, if necessary. 
Note: 
The likeliest reason for a C AIC rejection would be submission outside of the instruction period.  
Note: 
Steps 3 and 4 of this process can be repeated multiple times during the instruction period.  
Note: 
The CAIN, CAIS, CAIC, and CACS are sent real -time except during down time periods.  
Processing Periods and Cutoff Information 
Cutoff Times for Instruction Messages 
Business Rule: The instruction period begins at 12:00 a.m. midnight and ends at 8:00 p.m. each business day 
for the majority of CA events (there are instances in which a CA event cutoff is 12:00 p.m., but this occurs in 
the minority of cases). Instruction ISO 20022 messages may be submitted until the end of the instruction period 
minus two hours. The exact instruction cutoff times are communicated in the CANO message. 
Note: 
The scenarios throughout this guide show a 6:00 p.m. cutoff for messages in order to demonstrate the end of the 
instruction period minus 2 hours. However, if the instruction period cutoff for the event were 12:00 p.m., then the message 
cutoff would be 10:00 a. m. 
• The cutoff time to submit ISO 20022 instruction messages to [[DTC]] is the instruction period cutoff time minus 2 
hours on business days.  
• Instructions may be manually entered via the browser right up until the instruction cutoff time. In the majority of 
instances, this is 8:00 p.m. eastern time. This allows firms two additional hours after the ISO 20022 message 
cutoff time to correct an instruction via the browser.  
 
Cutoff Times for Cancellation Messages 
Business Rule: Cancellation messages follow the same cutoff submission rules that apply to instructions. The 
submission period begins at 12:00 a.m. midnight and closes at 8:00 p.m. each business day for the majority of 
CA events (there are instances in which a CA event cutoff is 12:00 p.m., but this occurs in the minority of 
cases). Instruction ISO 20022 messages may be submitted until the instruction period cutoff minus two hours.  

---

## Page 14

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 14 
Sample Processing Period 
The following table provides a list of sample messages entering the flow at particular times within a given 
period: 
• [[DTC]] Instruction Start Date: Monday 05/15/2012 12:00 a.m. 
• [[DTC]] Instruction End Date: Friday 05/17/2012 8:00 p.m. 
Note: 
The scenarios throughout this guide show a 6:00 p.m. cutoff for messages in order to demonstrate an instruction period 
cutoff of 8:00 p.m. minus two hours. However, if the cutoff for the event were 12:00 p.m., then the message cutoff would be 
10:00 a.m. 
Message Date/Time Received Expected Results 
1 05/15/2012 9:00 a.m. An instruction for 100 [[shares]] is submitted versus a total 
eligible balance of 1000 [[shares]] to [[DTC]]. Since this is received 
within the processing period, the instruction is accepted. The 
Instructio n Statement Report shows 1,000 total, 100 
instructed and 900 uninstructed on May 15 th. 
2 05/16/2012 9:00 a.m. An instruct ion for 900 [[shares]] is submitted. The instruction is 
accepted. Since this is received within the processing period, 
the instruction is accepted. At this point, all 1,000 of the total 
eligible [[shares]] have been accepted and zero [[shares]] remain 
uninstructed.  
3 05/16/2012 2:00 p.m.  Later in the day, the [[participant]] submits a cancellation 
request for the 100 [[shares]] submitted on the 15 th. Since this is 
received within the processing period, the cancellation 
request is accepted. At this point, 900 of the 1,000 total 
eligible [[shares]] have been instructed and 100 [[shares]] remain 
uninstructed.  
Note: 
All uninstructed positions will be moved to the [[default]] [[Option]] 
after cutoff and will be reflected in CAST.  

---

## Page 15

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 15 
Example of a Corporate Action Event Processed via ISO 20022 
Scenario 1: Instructions 
Four Instructions Submitted and Accepted 
In this scenario, the [[participant]]’s record date balance is 400 [[shares]]. These [[shares]] are eligible to be instructed 
upon. The instruction period begins at 12:00 a.m. on May 15th and ends at 6:00 p.m. on May 17th. The 
[[participant]] has submitted four instructions in total: one on May 15th, one on May 16th, and two on May 17th at 
4:00 p.m. for 100 [[shares]] each. All are accepted. Because instructions accumulate, [[DTC]] will process 
instructions for all 400 [[shares]]. 
 
  


---

## Page 16

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 16 
Scenario 2: Rejected 
Message Rejected after Cutoff Time 
In this scenario, the [[participant]]’s record date balance is 200 [[shares]]. These [[shares]] are eligible to be instructed 
upon. The instruction period begins at 12:00 a.m. on May 15th and ends at 6:00 p.m. on May 17th. The 
[[participant]] has submitted two instructions for 100 [[shares]] each on May 17th. The first instruction is accepted, 
since it was submitted within the instruction period. The second instruction is rejected, since it was submitted 
past the message cutoff time of 6:00 p.m. 
Tip: 
The rejected instruction may be submitted on the Corporate Actions browser until 8:00 p.m. on May 17th. 
Note: 
All uninstructed positions will be moved to the [[default]] [[Option]] after cutoff and will be reflected in the CA ST. 
 


---

## Page 17

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 17 
Scenario 3: Submitted Next Business Day 
One Instruction Accumulated for Next Business Day  
In this scenario, the [[participant]]’s record date balance is 200 [[shares]]. These [[shares]] are eligible to be instructed 
upon. The instruction period begins at 12:00 a.m. on May 15th and ends at 6:00 p.m. on May 17th. The 
[[participant]] has submitted two instructions for 100 [[shares]] each: one on May 15th and one on May 16th. The first 
instruction is accepted since it was submitted within the processing day. The second instruction will be 
accumulated for processing on the next business day: it missed the daily processing cutoff, but it may still be 
accepted because it was submitted within the overall instruction period. 
 
Scenario 4: Withdrawal 
One Instruction Cancelled 
In this scenario, the [[participant]]’s record date balance is 1,000 [[shares]]. These [[shares]] are eligible to be 
instructed upon. The instruction period begins at 12:00 a.m. on May 15th and ends at 6:00 p.m. on May 17th. 
The [[participant]] submitted an instruction for 100 [[shares]] on May 15th. The [[participant]] submitted another 
instruction for 900 additional [[shares]] on May 16th. Because instructions accrue, the total 1,000 [[shares]] are 


---

## Page 18

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 18 
instructed. However, the [[participant]] then cancels the May 15th instruction for 100 [[shares]], leaving 100 [[shares]] 
still uninstructed. 
Note: 
All uninstructed positions will be moved to the [[default]] [[Option]] after cutoff and w ill be reflected in the CAST.  
 
  


---

## Page 19

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 19 
 
What Is a CAIN Message? 
The Corporate Action Instruction Message (CAIN) is a message sent by participants to [[DTC]] to communicate 
distribution instructions. 
MX Identifier ISO 20022 Message 
Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTC]] 
Processes 
seev.033.002.xx 1 Corporate Action 
Instruction  
supl.008.001.xx 1 CAIN MT 565 Instructions/Elections  
 
A CAIN message is a [[participant]]’s instruction to [[DTC]] based on underlying options and details communicated in 
the CANO message. The CANO message communicates what the corporate action is and how it specifically 
af f ects the [[participant]]. With this information, a [[participant]] can determine the appropriate instructions to be 
submitted to [[DTC]] in a CAIN message. 
 
1 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary vers ion num ber 
may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions. 
Current schemas are available on MyStandards and [[DTCC]].com. 


---

## Page 20

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 20 
A CAIN message cannot be updated. Each CAIN represents a new instruction. As such, instructions are 
“accumulated”: for example, three messages specifying different instructions may be submitted for 100 [[shares]] 
each, totaling 300 [[shares]] instructed. If the instruction must be changed for any reason, it must be withdrawn 
using a CAIC message and a new CAIN must be submitted. 
Information Contained on the CAIN Message 
The CAIN message contains Event General Details. These include: 
• Corporate Action Event Identification (CORP). [[DTC]]’s unique identifier for the corporate action event. 
Mandatory for schema validation. 
• Official Corporate Action Event Identification (COAF). Official corporate action unique identification. 
This is the CA [[ID]] preceded by “US.” In order for this instruction to be accepted and processed, the COAF 
on the instruction must match the COAF on the announcement messages. 
• Event Type. The type of corporate action event that the CAIN message is responding to (e.g., optional 
[[Dividend]], etc.). 
• Underlying Security. The security affected by the corporate action.  
• Safekeeping Account. A [[DTC]]-assigned internal [[participant]] number. 
 
The CAIN message also contains Corporate Action Instruction details. These are specific items that detail how 
you want to react to the event. They include: 
• [[Option]] Number. The number that uniquely identifies an [[Option]] within an event. 
• [[Option]] Type. This describes the type of [[Option]] associated with the event (e.g., retain, sell). 
• Currency [[Option]]. The currency in which the amount disbursed from an interest or [[Dividend]] payment is 
offered: 
 
New [[DTCC]] 
Model [[Option]] 
Type 
[[Option]] Type Description  ISO 
20022 
[[Option]]  
Type 
(Extended) 
ExtendedOptionFeature  
Cash and 
[[securities]] 
Holder will receive a combination of cash and [[securities]] 
(may be applicable to Optional [[Dividend]] Service [OPS]).  
CASE 
 
Cash Holder will receive cash (may be applicable to Optional 
[[Dividend]] Servic e [OPS]). 
CASH 
 
DRIP Holder elects to receive additional [[securities]] instead of 
the cash distribution. [[Option]] may be declared by the 
[[issuer]] or as a service offered by [[DTC]].  
SECU 
 
Foreign Tax 
Unfavorable 
[[DTC]]-only [[Option]]. The event and security are eligible for 
the Foreign Tax Relief service at [[DTC]]. [[Option]] to selec t 
unfavorable tax rate. The Foreign Tax Unfavorable [[Option]] 
is the [[default]] [[Option]].  
CASH FORU 

---

## Page 21

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 21 
New [[DTCC]] 
Model [[Option]] 
Type 
[[Option]] Type Description  ISO 
20022 
[[Option]]  
Type 
(Extended) 
ExtendedOptionFeature  
Foreign Tax 
Favorable 
[[DTC]]-only [[Option]]. The event and security are eligible for 
the Foreign Tax Relief ser vice at [[DTC]]. [[participant]] 
receives their payment at a favor able tax withholding 
rate.  
CASH FORF 
Foreign Tax 
Exempt 
[[DTC]]-only [[Option]]. The event and security are eligible for 
the Foreign Tax Relief service at [[DTC]]. [[participant]] is 
exempt from any tax withholdi ng.  
CASH FORX 
DRIP 
Unfavorable 
[[DTC]]-only [[Option]]. The event and security are eligible for 
both the [[Dividend]] Reinvest ment and Foreign Tax 
Services at [[DTCC]]. Participants will receive additional 
[[shares]] and the tax withholding on those [[shares]] will be at 
the unfavorable tax rate.  
SECU DRPU 
DRIP Favorable [[DTC]]-only [[Option]]. The event and security are eligible for 
both the Div idend Reinvestment and Foreign Tax Relief 
Services at [[DTCC]]. Participants will receive additional 
[[shares]] and the tax withholding on those sha res will be at 
the favorable tax rate.  
SECU DRPF 
DRIP Exempt [[DTC]]-only [[Option]]. The event and security are eligible for 
both the [[Dividend]] Reinvestment and the Foreign Tax 
Relief service at [[DTCC]]. Participants will receive 
additional [[shares]] and will be exemp t from any tax 
withholding.  
SECU DRPX 
Foreign 
Currency 
Payment 
[[DTC]]-only [[Option]]. The event and security are eligible for 
the Foreign Currency Payment service at [[DTCC]]. 
Participants will receive their distribution in the foreign 
currency instructed.  
CASH FCPP 
Foreign 
Currency 
Payment 
Unfavorable 
[[DTC]]-only [[Option]]. The event and security are eligible for 
both the Foreign Currency and Foreign Tax services at 
[[DTCC]]. Participants will receive their distribution in a 
foreign currency and the tax withholding on that 
distribution will be subject to unfavorable tax withholding.  
CASH FCPU 
Foreign 
Currency 
Payment 
Favorable 
[[DTC]]-only [[Option]]. The event and security are eligible for 
both the Foreign Currency and Foreign Tax services at 
[[DTCC]]. Participants will receive their  distribution in a 
foreign currency and the tax withholding on that 
distribution will be subject to favorable tax withholding.  
CASH FCPF 
Foreign 
Currency 
Payment 
Exempt 
[[DTC]]-only [[Option]]. The event and security are eligible for 
both the Foreign Currency and Foreign Tax services at 
[[DTCC]]. Participants will receive their distribution in a 
foreign currency and will be exempt from any tax 
withholding.  
CASH FCPX 
[[securities]] Hold er will receive [[securities]] (may be applicable to 
Optional [[Dividend]] Service [OPS]).  
SECU 
 
 

---

## Page 22

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 22 
o Instructed Quantity. This cannot exceed the eligible balance minus what was already instructed. 
o Requested Taxation Rate. Used to identify [[DTC]] tax options. 
Note: 
The options will appear in the core of the message using standard ISO codes (CASH, SECU o r CASE). [[DTC]]-specific [[Option]] 
codes will be noted in the extension in the ExtendedOptionFeature component.  
The following fields will only be used after a cancellation message (CAIC) is sent. They are not used for the 
first CAIN sent to [[DTC]] in response to a corporate action event: 
• Change Instruction Indicator. Indicates that the current instruction is replacing a previous CAIN that was 
cancelled earlier.  
• Cancelled Instruction Identification. Identification of a previously sent cancelled instruction message. 
• Instruction Cancellation Request Identification. Identification of a previously sent instruction 
cancellation request document. 
Supplementary Data 
A CAIN message also contains supplementary data for [[DTC]] special options: 
• Optional Dividends ([[Beneficial Owner]] information): 
o Number of Accounts  
o [[Beneficial Owner]] Quantity 
• Foreign Tax Withholdings (rate information): 
o Control Identification (Canada only) 
o Quantity (Canada only) 
• Foreign Currency Payments (wire information): 
o Wire Instruction 
o Wire Quantity 
o Bank Name 
o Bank Address 
o Bank City 
o Bank Country 
o Bank Attention To 
o Bank Comments 
o Beneficiary Account 
o Beneficiary Account Identification 
o Beneficiary Account Comments 
Examples 
Two examples are provided below for two of the services offered for ISO 20022 messaging. 
Note: 
There are other scenarios and combinations not pictured here.  

---

## Page 23

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 23 
Optional [[Dividend]] Information 
This is a distribution of a [[Dividend]] to shareholders with a choice of payment method. The shareholder has the 
[[Option]] to choose the form of payment (e.g. [[securities]], cash, or both). There are separate events for Cash 
Dividends, and [[Dividend]] with Options. 
The following scenario illustrates an optional [[Dividend]]. 
 
DVCA with [[DTC]] DRIP [[Option]] 
This is a distribution of a [[Dividend]] to shareholders of an issue that is eligible for the [[DTC]] [[Dividend]] 
Reinvestment program.  
The following scenario illustrates a cash [[Dividend]] with a [[DTC]] DRIP [[Option]]. 
 
The following scenario illustrates a cash [[Dividend]] with a [[DTC]] DRIP Opt Out [[Option]]. 
 


---

## Page 24

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 24 
Rules 
Rules for All Instruction Messages 
Instruction messages will be validated similarly to manual instructions. Where possible, multiple errors may be 
reported on the Reject Advice. 
1. Each instruction message provides instruction information for only one [[Option]] on the event.  
2. While instructions can be submitted via the browser for eight different services, instruction messages will 
only be accepted for the following four services: 
• Foreign Currency Payments (FCP), 
• Foreign Tax Relief (FOR),  
• Optional Dividends (OPS), and 
• [[Dividend]] Reinvestment Program (DRP) including OPT-OUT. 
3. A user can send more than one instruction message for an [[Option]]. The subsequent instruction messages 
will be added to the instructions previously received. 
4. The messages will be processed on a first-in, first-out basis. All instructions will accumulate as such and 
be processed in the original order in which they are received. 
5. Instruction messages will not be accepted if final instructions have been manually entered for the event.  
Note: 
Manual input overrides messages: once a change is made t o an instruction via the browser, no further changes may be 
made to an instruction via ISO message. Further changes after that point can o nly be made via the browser.  
6. Both Group Users and Participants can submit instructions for the same safekeeping account on the same 
CA [[ID]] and options. 
7. An instruction message will be rejected if additional text is provided in the CAIN. 
8. An instruction message must contain all of the following mandatory items: 
• Business Message Identifier (BAH), 
• Corporate Action Event Identification (CORP), 
• Official Corporate Action Event Identification (COAF), 
• Event Type (CAEV), 
• Safekeeping Account, 
• [[Option]] Number, 
• [[Option]] Type, and 
• Instructed Quantity (unit for [[Equity]]/amount for debt). 
Note: 
The information contained in each CAIN must correlat e directly to the CANO message that was sent by [[DTC]] that outlines 
the event terms and options.  

---

## Page 25

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 25 
Additional Rules 
Field-Specific Rules 
Field Rule Comments 
Official Corporate Action 
Event Identification  
1. Must match the CA [[ID]] in the browser and 
begin with ‘US’ in the first two positions.  
2. Must also be a Distribution event that is eligible 
for instructions via messaging.  
See rule 2 above in the Rules for 
All Instruction Messages  section.  
Event Type 3. Must match the Corporate Action Notification 
(CANO) that the client received from [[DTC]].  
 
Underlying Security 4. The underlying security must match the [[CUSIP]] 
found on the CANO that the client received 
from [[DTCC]]. 
 
[[Option]] Type 5. Must match the Corporate Action Notificatio n 
(CANO) that the client received from [[DTC]].  
 
Instruction Identification  6. Must be less than or equal to 16 characters.  
7. A duplicat e must not exist. 
The underlying security must 
match the [[CUSIP]] contained in 
the CANO from [[DTC]].  
Safekeeping Account  8. Must be numeric (without leading zeroes) only.  
9. Must match the [[participant]] [[ID]] provided by 
[[DTC]]. 
 
Currency [[Option]]  10. If provided, must match the currency on the 
Payout Rate for the FCP [[Option]].  
 
Requested Taxation Rate 11. Must match the Tax Withholding Rate on the 
[[Option]].  
12. For USD, the Requested Taxation Rate must 
be blank.  
 
Instructed Quantity (Unit)  13. Must be provided.  
14. Event Security Issue Type must be “[[Equity]].”  
 
Instructed Quantity 
(Amount)  
15. Must be provided.  
16. Event Security Issue Type must be “Debt.”  
 
 
  

---

## Page 26

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 26 
Cutoff Rules: General 
Click here to read about cutoff information. 
Item Rule 
General Submission Times 1. Instruction messages will be processed within the Instruction Period (12 
a.m. to 8 p.m. each business day) and  within the [[Option]] Cutoff Period for 
the specific [[Option]].  
[[Option]] Cutoff Start Date/Time 
(USD Cash [[Option]])  
2. This will be the Start Date/Time for the associated services (DDRP, FCCP, 
or a combination of the two).  
[[Option]] Cutoff End Date/Time (USD 
Cash optio n)  
3. This  will be the Expiration Date/Time for the associated services (DDRP, 
FCCP, or a combination of the two).  
Cutoff Rules: Specific 
Click here to read about cutoff information. 
If a CAIN message is 
submitted/received… 
It will… Comments 
Outside the [[Option]] Cutoff period 
minus 2 hours  
1. Be rejected.  See reason code ADEA  
Outside of the Instruction Period  2. Be accumulated along with other 
messages received and processed 
when the Instruction Period opens 
on the next business day.  
 
Outside of the [[Option]] Cutoff 
Period minus 2 hours  
3. Be rejected.  Time of submission is determined by 
a timestamp from [[DTC]].  
This is done to provide you with the 
opportunity to provide manual 
instructions if an ISO instruction 
message is rejected near the 
instruction cutoff time.  
Instructions: Specific Rules 
Rules for Foreign Currency Payments 
All Foreign Currency Payment Instructions require wire instructions. The EDS Messaging Country Code on the 
CANO announcement (SR-2013 version) message will be populated with a two-letter country code value. 
When an FCP [[Option]] is available, wire instructions must be included in the extension. An exception to this rule 
is as follows:  
• The country associated with the [[CUSIP]] is Canada and the [[participant]] is a Canadian [[participant]] eligible for 
the Canadian Link Service.  
 

---

## Page 27

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 27 
The instruction message will be rejected if wire instructions are required and not provided. The Reject Reason 
Code will be “OTHR” with a reason of “Wire Information is Missing.” 
The instruction message will also be rejected if wire instructions are provided when they are not required. The 
Reject Reason Code will be “OTHR” with a reason of “Wire Information Not Applicable.” 
If wire instructions are required: 
1. The Wire block is repeatable up to a maximum of 45 times. If there are more than 45 Wire blocks, the 
instruction message will be rejected. It will have a Reject Reason Code of “OTHR” with a reason of “Wire 
Max Instances Exceeded.” 
2. The Wire Quantity (Unit/Amount) must be numeric and greater than zero. If not, the message is rejected 
with a Reject Reason Code of “DQUA.” The total quantities submitted must match the amount instructed 
on the specific [[Option]].  
3. The instruction message will be rejected if a value has not been provided for the items in the table below. 
All items missing a value will have a Reject Reason Code of “OTHR” with a reason of “(Item Name) Not 
Provided.” 
4. The message must have a two-digit ISO 3166 country code. This code must correlate to the “Country” 
field displayed on the browser. If it does not, the message is rejected with a Reject Reason Code of 
“OTHR” with a reason of “Invalid Country Code.” 
5. The message will be rejected with a code of “DQUA” if the Wire Quantity (Unit/Amount) total for all wire 
instructions provided in the message does not equal the Instructed Quantity. 
Rules for Foreign Tax Withholdings 
Foreign Tax Relief Instructions on Canadian issues at the exempt tax withholding rates require that the 
[[participant]] provides tax exempt control numbers and the associated share quantities.  
If the EDS Messaging Country Code found on the SR-2013 version of the CANO announcement message 
equals “CA” (Canada), and the [[Option]] types = FCPX (Foreign Currency Payment Exempt), FORX (Foreign Tax 
Relief Exempt), or DRPX (DRIP Exempt)) the Tax Exempt component must be populated in the CAIN 
extension. This information is provided in the TaxExempt block in the Control Identification and Quantity fields.  
The validation rules are as follows: 
1. The Tax Exempt block is repeatable up to a maximum of 300 times. If it repeats more than 300 times, it 
will be rejected with a Reject Reason Code of “OTHR” and a reason of “Tax Exempt Max Instances 
Exceeded.” 
2. Tax Exempt Control information is required for Instruction Messaging for FCPX, FORX, or DRPX options 
that are marked as Tax Exempt (with a Withholding Rate of 0) for Canadian issues.  
If Tax Control Information is provided for an issue from any country other than Canada, then the message 
will be rejected with a Reject Reason Code of “OTHR” with a reason of “Tax Exempt provided for non-
Canadian issue.” 
3. The Control Identification must be either a 6 digit number, IRA001, CRC001, or a combination of all three. 
This is applicable at the [[Option]] level, so another [[Option]] can have IRA001. If the Control Identification 
dif fers from this, then the message will be rejected with a Reject Reason Code of “CERT.” 

---

## Page 28

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 28 
4. The Quantity (Unit/Amount) must be numeric and greater than zero. Additionally, the sum of the Quantity 
for all occurrences must equal the Instructed Quantity (Unit/Amount). If the Quantity differs from this, then 
the message will be rejected with a Reject Reason Code of “DQUA.” 
Rules for Optional Dividends 
Participants can receive income payments in the form of cash, [[Stock]], or a combination of both. “[[Dividend]] with 
[[Option]]” is the only event type eligible for these optional dividends.  
This requires that the [[participant]] provides the Optional [[Dividend]] block. If the Optional [[Dividend]] Supplementary 
Data Required Flag is marked as “True” in the extension of the CANO (announcement) message and the 
[[Option]] type includes the Certification Breakdown Type (code) PABD in the [[Option]] details block, the beneficial 
accounting information will have to be included in the extension of the CAIN message. The NumberOfAccounts 
that is part of this block provides the number of accounts for the associated [[Beneficial Owner]] Quantity.  
The validation rules are as follows: 
1. The Optional [[Dividend]] block is repeatable up to a maximum of 500 times. If it repeats more than 500 
times, it will be rejected with a Reject Reason Code of “OTHR” and a reason of “Optional [[Dividend]] Max 
Instances Exceeded.” 
2. Optional [[Dividend]] [[Beneficial Owner]] information will be accepted if the Optional [[Dividend]] Supplementary 
Data Required Flag is set to True and the Certification Breakdown Type (code) PABD is set on the [[Option]]. 
If the flag is not set, the instruction will be rejected with a Reject Reason Code of “OTHR” and a reason of 
“Optional [[Dividend]] mismatch.” 
3. The NumberOfAccounts must be numeric and greater than zero. If it is not, the message will be rejected 
with a Reject Reason Code of “OTHR” and a reason of “Invalid Account [[ID]] on Optional [[Dividend]].” 
4. The [[Beneficial Owner]] Quantity (Unit/Amount) must be numeric and greater than zero. Additionally, if the 
Instructed Quantity (Unit/Amount) is present, it must equal the product of the Safekeeping Account times 
the [[Beneficial Owner]] Quantity (Unit/Amount) for all occurrences. If any of these are invalid, then the 
message is rejected with a Reject Reason Code of “DQUA.” The total quantities input must match the 
amount instructed on the specific [[Option]].  
Rules for DRIPs including Opt-Outs (DRP) 
The [[Dividend]] Reinvestment Program allows Participants to instruct to reinvest income payments for additional 
[[shares]] of [[Stock]] for any eligible issues that have a [[Dividend]] Reinvestment (DRP) program. Participants will be 
able to send DRP instructions, including DRP OPT-OUT events. 
  

---

## Page 29

ISO 20022 Messaging for Distributions Instructions 
An Introduction to ISO 20022 Mess aging 29 
 
What Is a CAIS message? 
A Corporate Action Instruction Status Advice message (CAIS) is a [[DTC]] response that indicates whether the 
CAIN message containing instructions and submitted by the [[participant]] has been accepted or rejected. In other 
words, [[DTC]] sends a CAIS message to inform a [[participant]] of a CAIN message’s status. 
MX Identifier ISO 20022 Message Names Extension Short 
Name 
Equivalent ISO 
15022 
Equivalent [[DTC]] 
Processes 
seev.034.002.xx 2 Corporate Action Instruction 
Status Advice  
n/a CAIS MT 567 Instruction Reply  
 
If the CAIN message is successfully accepted and processed, [[DTC]] will send a CAIS message to the 
originating [[participant]] that indicates its acceptance. Likewise, if the CAIN is rejected, [[DTC]] will indicate that in 
 
2 The last two digits in the MX Identifier signify the version number. The MX version number may change during the SWIFT annual release based on 
mandatory or optional updates to the standards. 
Current schemas are available on MyStandards, and [[DTCC]].com. 


---

## Page 30

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 30 
the corresponding CAIS message. Additionally, when an [[Option]] or an event is deleted after a [[participant]] has 
already acted upon it, a “Reject” message will also be generated and sent to the originating [[participant]].  
For example, a CAIN instruction is submitted by [[participant]] 001 on [[Option]] #1. The event and [[Option]] are valid 
at the time of instruction, so [[DTC]] accepts the CAIN message by sending [[participant]] 001 a CAIS message in 
confirmation. However, two days later (prior to the instruction cut-off and pay date), [[DTC]] then deletes [[Option]] 
#1 because the [[issuer]] is no longer supporting it. [[DTC]] then sends [[participant]] 001 a CAIS message rejecting 
the previously confirmed instruction. 
Information Contained on the CAIS Message 
The following table contains all of the information elements presented on a CAIS message, along with an 
explanation of what each element means and/or applicable details. 
Data Element Definition/Information  
Instruction 
Identification  
The Business Message Identifier of the received i nstruction. This 16- character identifier 
matches the status message to a previously submitted CAIN message.  Every ISO message 
must have a Business Message Identifier, or BAH.  
Corporate Action 
Event Identification  
Specified on the received instruction. Leading zeroes will be suppressed.  
Official Corporate 
Action Event 
Identification  
The COAF, or the Official Corporate Action Identification , on the received instruction. This is 
the CA [[ID]] preceded by “US.”  
Event Type The type of corporate action event that the original instruction message was responding  to. 
Specified on the received i nstruction.  
[[Option]] Number Specified on the received instr uction.  
[[Option]] Type Specified on the received instruction:  
New [[DTCC]] 
Model [[Option]] 
Type 
[[Option]] Type Description  ISO 20022 
[[Option]] Type 
(Extended) 
Extended 
[[Option]] 
Feature 
Cash and 
[[securities]] 
Holder will receive a combination of 
cash and [[securities]] (may be 
applicable to Optional [[Dividend]] 
Service [OPS]). 
CASE 
 
Cash Holder will receive cash (may be 
applicable to Optional [[Dividend]] 
Service [OPS]). 
CASH 
 
DRIP Holder elects to receive additional 
[[securities]] instead of the cash 
distribution. [[Option]] may be declared 
by the [[issuer]] or as a service offered 
by [[DTC]]. 
SECU 
 

---

## Page 31

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 31 
Data Element Definition/Information  
Foreign Tax 
Unfavorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for the Foreign 
Tax Relief service at [[DTC]]. [[Option]] to 
select unfavorable tax rate. The 
Foreign Tax Unfavorable [[Option]] is 
the [[default]] [[Option]].  
CASH FORU 
Foreign Tax 
Favorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for the Foreign 
Tax Relief service at [[DTC]]. 
[[participant]] receives their payment at 
a favorable tax wi thholding rate.  
CASH FORF 
Foreign Tax 
Exempt 
[[DTC]]-only [[Option]]. The event and 
security are eligible for the Foreign 
Tax Relief service at [[DTC]]. 
[[participant]] is exempt from any tax 
withholding.  
CASH FORX 
DRIP 
Unfavorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
[[Dividend]] Reinvest ment and Foreign 
Tax Services at [[DTCC]]. Participants 
will receive additional [[shares]] and the 
tax withholding on those [[shares]] will 
be at the unfavorable tax rate.  
SECU DRPU 
DRIP Favorable [[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
[[Dividend]] Reinv estment and Foreign 
Tax Relief Services at [[DTCC]]. 
Participants will receive additional 
[[shares]] and the tax withholding on 
those [[shares]] will be at the favorable 
tax rate.  
SECU DRPF 
DRIP Exempt [[DTC]]-only [[Option]]. The event and 
security are eligible for both th e 
[[Dividend]] Reinvestment and the 
Foreign Tax Relief service at [[DTCC]]. 
Participants will receive additional 
[[shares]] and will be exempt from any 
tax withholding.  
SECU DRPX 
Foreign 
Currency 
Payment 
[[DTC]]-only [[Option]]. The event and 
security are eligible for the Fo reign 
Currency Payment service at [[DTCC]]. 
Participants will receive their 
distribution in the foreign currency 
instructed.  
CASH FCPP 

---

## Page 32

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 32 
Data Element Definition/Information  
Foreign 
Currency 
Payment 
Unfavorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
Foreign Currency and Foreign Tax 
services at [[DTCC]]. Participants will 
receive their distribution in a foreign 
currency and the tax withholding on 
that distribution will be subject to 
unfavor able tax withholding.  
CASH FCPU 
Foreign 
Currency 
Payment 
Favorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
Foreign Currency and Foreign Tax 
services at [[DTCC]]. Participants will 
receive their distribution in a foreign 
currency and the tax withholding on 
that distribution will be subject to 
favorabl e tax withholding.  
CASH FCPF 
Foreign 
Currency 
Payment 
Exempt 
[[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
Foreign Currency and Foreign Tax 
services at [[DTCC]]. Participants will 
receive their distribution in a foreign 
currency and will be exempt from 
any tax withholding.  
CASH FCPX 
[[securities]] Holder will receive [[securities]] (may 
be applicable to Optional [[Dividend]] 
Service [OPS]). 
SECU 
 
 
Safekeeping Account  Specified on the received instruction. Leading zeroes will be suppressed.  
(Instructed Balance) In g eneral, this is the total elected for that [[Option]] so far.  
For example, three CAIN messages are submitted for 100 [[shares]] each.  
CAIS #1 will have 100 as instructed and 100 in total instructions on that [[Option]].  
CAIS #2 will have 100 as instructed and 200 as t otal instructions for that [[Option]].  
CAIS #3 will have 100 as instructed and 300 as total instructions for that [[Option]].  
Instructed Balance 
(Short/Long Position)  
This defaults to “LONG” for a positive value.   
Instructed Balance 
(Unit) 
When the Event Securit y is “[[Equity]] (non -debt),” then the Instructed Balance (Unit) eq uals the 
total of all instructions submitted for this event.  
Instructed Balance 
(Amount)  
When the Event Security is “Debt,” then the Instructed Balance (Amount) equals the total of all  
instruc tions submitted for this event.  
(Uninstructed 
Balance) 
In general, this is the total uninstructed  position for the event  so far. 
Uninstructed Balance 
(Short/Long Position)  
This defaults to “LONG”  for a positive value.   

---

## Page 33

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 33 
Data Element Definition/Information  
Uninstructed Balance 
(Unit) 
When the Event Security is “[[Equity]] (non -debt),” then the Uninstructed Balance (Unit) is equal 
to the record date position for this event minus the total of all instructions submitted for  this 
event. 
Uninstructed Balance 
(Amount)  
When the Event Security is  “Debt,” then the Uninstructed Balance (Amount) is equal to the 
record date position for this event minus the total of all instructions submitted for this event.  
Status Quantity (Unit) Obtained from the r eceived i nstruction (Instructed Quantity [Unit]) . 
Status Quantity 
(Amount)  
Obtained from the received i nstruction (Instructed Quantity [Amount]) . 
Accept Advice:   
Instruction 
Processing Status 
(/NoSpcfdRsn)  
This field defaults to ‘NORE’ if the instruction message was accepted.  
Reject Advice:  
Instruction 
Processing Status 
(/Cd) 
Please see the  reject reason codes immediately following this table.  
Additional Reason 
Information 
When an error code of “
OTHR” is used, [[DTC]] often provides a descrip tive error message in 
this field.  
CAIS Reject Codes 
The following tables contain lists of error codes and their explanations. The first table provides the full list of 
regular codes. The second table elaborates on the “OTHR” error code and provides a list of the real-text 
reasons that can accompany this code on a rejection message. 
Reject Codes 
Reject Code Description 
ADEA Account Servicer Deadline Missed  
CANC [[Option]] deleted 
CERT Incorrect certification for one of the following reasons:  
• Valid tax exemp t Control [[ID]] missing for special Canadian security  
• Tax exempt Control [[ID]] missing 
• Tax exempt Control [[ID]] is not one of these values:  
o “IRA001” 
o “CRC001” 
o A six -digit number 

---

## Page 34

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 34 
Reject Code Description 
DQUA Quantity rejection for one of the following reasons:  
• Accumulated total does not match the instructed value on the CAIN (applies to 
supplementary data on CAIN when provided)  
• [[Asset]] class does not correspond with the associated, provided unit or amount.  
• Provided value is “0”  
• Provided value is not numer ic (applies to supplementary data on C AIN when applicable)  
DSEC Rejected for one of the following reasons:  
• More than one underlying security was provided  
• Underlying security is not a [[CUSIP]]  
EVNM Unrecognized identification for one of the following reasons:  
• Event not found 
• Event is not a distr ibution event  
• Event is not eligible for messaging 
LACK Lack of [[securities]] for one of the following reasons:  
• Instructed value is greater than record date position 
• Record date position is “0”  
NMTY Mismatch for one of the following reasons:  
• Legacy announcem ent not found 
• [[Option]] not found  
• [[Option]] type validation failed  
OPTY Invalid [[Option]] type /[[Option]] type validation failed  
OTHR Other (see table) 
SAFE Safekeeping account rejection for one of the following reasons:  
• BAH Acco unt [[ID]] does not match safekeeping account  
• Safekeeping account has leading zeroes  
• Safekeeping account is not numeric  
ULNK Invalid reference/ canceled instruction identification not found 
“OTHR” Code Reasons 
ISO Code Reason 
OTHR Business Message Identifier  length exceeds 16 characters  
OTHR Corporate Action Event is either Deleted or Canceled  
OTHR Currency [[Option]] mismatch  
OTHR Duplicate request received  
OTHR Incorrect Event Type  
OTHR Invalid Account on Optional [[Dividend]]  

---

## Page 35

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 35 
ISO Code Reason 
OTHR Invalid Bank Country  
OTHR Mandatory Business Message Identifier is missing 
OTHR Mandatory Event Type is missing 
OTHR Mandatory Official Corporate Action Event Identification is missing 
OTHR Mandatory [[Option]] Number is missing  
OTHR Mandatory [[Option]] Type is missing  
OTHR Mandator y Safekeeping Account is missing  
OTHR Manual Election Instruction(s) exist(s)  
OTHR Maximum [[DTCC]] -allowed Requested Taxation Rate exceeded  
OTHR Not a CDS [[participant]]  
OTHR Optional [[Dividend]] information is missing  
OTHR Optional [[Dividend]] max instances exceeded  
OTHR Optional [[Dividend]] mismatch  
OTHR Requested Taxation Rate mismatch  
OTHR Some or all Wire Information is missing  
OTHR Tax Exempt information is missing  
OTHR Tax Exempt max instances exceeded  
OTHR Tax Exempt provided for non -Canadian issue 
OTHR Unsupported Additional Text block found  
OTHR Wire information not applicable  
OTHR Wire maximum instances exceeded  
Troubleshooting Message Rejection 
The following table contains a list of common errors that may occur within particular data elements. It provides 
possible reasons for the errors and suggests corrective actions for them. 

---

## Page 36

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 36 
General 
Data Element Error Code  Problem/Corrective Action  
Cancelled Instruction Indicator  ULNK When the Change Instruction Indicator is set to “True,” [[DTC]] 
matches this fie ld to the Business Message Identifier of the 
instruction that was canceled. The message is rejected if not 
matched.  
• Check Change Instruction Indicator and set it to the correct 
value. 
• Correct this field to match the cancelled message’s Business 
Message Identifier. 
Instruction Cancellation Request 
Identification  
ULNK When the Change Instruction Indicator is set to “True,” [[DTC]] 
matches this field t o the Business Message Identifier of the 
instruction that was cancelled. The message is rejected if not 
matched.  
• Check Change Instruction Indicator and set it to the correct 
value. 
• Correct this field to match the cancelled message’s Business 
Message Identifier. 
Corporate Action Event 
Identification  
EVNM Corporate Action Event Identification does not match that on 
the original CANO.  
• Edit the value of the Corporate Action Event Indicator to 
match that on the original CANO.  
Official Corporate Action Event 
Identification  
EVNM (Optional)  Official Corpor ate Action Event Identification does 
not match that on the original C ANO. 
• Edit the value of the Official Corpor ate Action Event Indica t or 
to match that on the original CANO.  
Event Type OTHR Event Type does not match that on the original CANO. 
Additional Reason Information field reads “Incorrect Event 
Type.”  
• Edit the value of the Event Type to match that on the origina l 
CANO. 
Underlying Security DSEC (Optional; recommended by the Standards Ma rket Practice 
Group [SMPG]) Underlying Security does not match that on the 
original CANO. Additionally, only one underlying security i s 
accepted. That security identifier must be a [[CUSIP]].  
• Edit the value of the Underlying Security to match that on the 
origi nal CANO. 
• Ensure that only one security is referenced.  
• Ensure the security identifier is a [[CUSIP]].  

---

## Page 37

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 37 
Data Element Error Code  Problem/Corrective Action  
Safekeeping Account  SAFE Safekeepin g account information does not match validity rules:  
1. Must be a [[DTC]] [[participant]] account.  
2. Number must not contain leading zeroes (for example: “1” 
instead of “0001,” “11” instead of “0011,” etc.).  
• Edit the Safekeeping Account number to match the rules 
above. 
Corporate Action Instruction 
Data Element Error Code  Problem/Corrective Action  
[[Option]] Number OPNM [[Option]] number does not match that on original CANO.  
• Edit the value of the [[Option]] Number so it matches the 
original CANO.  
 NMTY [[Option]] number does not matc h the [[Option]] type selected.  
• Check the value of the [[Option]] Type. If it doesn’t match this 
[[Option]] numbe r, change the [[Option]] type.  
Note: 
The [[Option]] Type must still match that in the original CANO. If 
there is still a discrepancy, trace the error back via the COAF to 
investigate the original information.  
[[Option]] Type OPTY [[Option]] type does not match that of the original CANO.  
• Edit the value of the [[Option]] Type to match the original 
CANO. 
Currency [[Option]]  OTHR (Optional)  Currency [[Option]] does not match against tha t on the 
original CANO.  
When a mismatch occurs, the “OTHR” error code is displayed 
with “InvalidCur rencyOption” in the 
AdditionalReasonInformation field.  
• Edit the value of the Currency [[Option]] to match the original 
CANO. 
Instructed Quantity  DQUA Instructe d Quantity is not a valid amount.  
• If face amount was used for debt per market practice, make 
sure that it was correctly converted to quantity.  
• Edit the value of the Instructed Quantity to reflect a valid 
amount. 
 LACK Instructed Quantity is greater than the eligible quantity.  
• Edit the Instructed Quantity to be less than or equal to the 
eligible quantity.  

---

## Page 38

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 38 
Data Element Error Code  Problem/Corrective Action  
Requested Taxation Rate OTHR Requested Taxation Rate does not match the Withholding Tax 
Rate on the original CANO.  
When a mismatch occurs, the “OTHR” er ror code is displayed 
with “Requested Taxation Rate Mismatch” in the 
AdditionalReasonInformat ion field. 
• Edit the Requested Taxation Rate to match the Withholding 
Tax Rate on the original CANO.  
Supplementary Data 
Data Element Error Code  Problem/Corrective Action 
Optional [[Dividend]] (0… n) repeats OTHR More than 500 iterations are included on the instruction.  
When this occurs, the “OTHR” error code is displayed with 
“Optional [[Dividend]] Max Instances exceeded” in the 
AdditionalReasonInformation field.  
• Edit the n umber of iterations to be fewer than the maximum of 
500. 
 DQUA In this repetitive service block, the Instructed Quantity is not 
equal to the sum of all instances of [[Beneficial Owner]] Quantity 
times Safekeeping Account.  
• Check the number of instances of [[Beneficial Owner]] Quantity, 
Safekeeping Account, and the value of Instructed Quantity to 
balanc e out the amounts.  
 OTHR Another service block(s) is/are being used in addition to this one .  
When this occurs, the “OTHR” error code is displayed with “Max 
Allowable  Service Block is 1” in the AdditionalReasonInformation 
field.  
• Delete whichever service block(s) should not be used.  
Number of Accounts  OTHR Number of accounts is in an invalid format. 
When this occurs, the “OTHR” error code is displayed with 
“Invalid Ac count [[ID]] on Optional [[Dividend]]” in the 
AdditionalReasonInformation field.  
• Check that the value contains only numbers. No letters or 
characters are allowed.  
• Check that the number does no t contain leading zeroes (for 
example: “1” instead of “0001,” “11” instead of “0011,” etc.).  
[[Beneficial Owner]] Quantity DQUA Face Amount was not used for debt security or Owner Amount 
was not used for [[shares]].  
• Ensure that Face Amount is used for Debt Security. 
• Ensure that Owner Amount is used for [[shares]].  

---

## Page 39

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 39 
Data Element Error Code  Problem/Corrective Action 
Tax Exempt (0… n) repeats OTHR More than 300 iterations are included on the instruction.  
When this occurs, the “OTHR” error code is displayed with “Tax 
Exempt Max Instances exceeded” displayed in the 
AdditionalReasonInformation field.  
• Edit the number of iterations to be fewer th an the maximum of 
300. 
 DQUA In this repetitive service block, the Instructed Quantity is not 
equal to the sum of all instances of Control Identification times 
Quantity.  
• Check the values of Quantity, the number of instances of 
Control Identification, and the Instructed Quantity to balance 
out the amounts.  
 OTHR Another service block(s) is/are being used in addition to this one .  
When this occurs, the “OTHR” error code is displayed with “Max 
Allowable Service Block is 1” in the AdditionalReasonInformation 
field.  
• Delete whichever service block(s) should not be used.  
Control Identification  CERT The Tax Exempt Control Number is not a valid Tax Exempt 
Control [[ID]].  
Note: 
This is a Canadian Revenue Control number that is required for 
TaxRelief  for Canada. You must include it to receive the tax relief.  
• Check that the number is six digits.  
• Check that no letters or symbols are used.  
• Ensure that it is an existing Tax [[ID]].  
Quantity DQUA Face Amount was not used for debt security or Owner Amount 
was not used for share s. 
• Ensure that Face Amount is used for Debt Security.  
• Ensure that Owner Amount is used for [[shares]].  
Wire Instruction (0… n) repeats OTHR More than 45 iterations are included on the instruction.  
When this occurs, the “OTHR” error  code is displayed with “Wire  
Instruction Max Instances exceeded” in the 
AdditionalReasonInformation field.  
• Edit the number of iterations to be fewer than the maximum of 
45. 
 OTHR Another service block(s) is/are being used in addition to this one .  
When this occurs, the “OTHR” error c ode is displayed with “Max 
Allowable Service Block is 1” in the AdditionalReasonInformation 
field.  
• Delete whichever service block(s) should not be used.  

---

## Page 40

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 40 
Data Element Error Code  Problem/Corrective Action 
Wire Quantity DQUA Either Face Amount was not used for debt security or Owner 
Amount was not used for  [[shares]], or Wire Quantity is greater 
than Instruction Quantity. 
• Ensure that Face Amount is used for Debt Security.  
• Ensure that Owner Amount is used for [[shares]].  
• Ensure that the Wire Quantity is less than or equal to the 
Instruction Quantity. 
Country Codes 
Note: 
This list is for reference only. [[DTC]] will adhere to the list of official ISO country codes which is updated biannually. As su ch, 
this list of country codes is subject to change.  
Country Code Country Name 
AD ANDORRA 
AE UNITED ARAB EMIRATES 
AF AFGHANISTAN 
AL ALBANIA 
AM ARMENIA 
AN NETHERLANDS ANTILLES 
AO ANGOLA 
AR ARGENTINA 
AS AMERICAN SAMOA 
AT AUSTRIA 
AU AUSTRALIA 
AW ARUBA 
AZ AZERBAIJAN 
BB BARBADOS 
BD BANGLADESH 
BE BELGIUM 
BG BULGARIA 
BH BAHRAIN 
BI BURUNDI 
BJ BENIN 

---

## Page 41

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 41 
Country Code Country Name 
BM BERMUDA 
BN BRUNEI 
BO BOLIVIA 
BR BRAZIL 
BS BAHAMAS 
BT BHUTAN 
BW BOTSWANA 
BY BYELORUSSIA SOVIET SOCIALIST REPUBLIC  
BZ BELIZE 
CA CANADA 
CC COCOS (KEELING) ISLANDS 
CD CONGO, THE DEMOCRATIC REPUBLIC OF THE  
CF CENTRAL AFRICAN REPUBLIC 
CG CONGO 
CH SWITZERLAND 
CI IVORY COAST-CÔTE D'IVOIRE 
CK COOK ISLANDS 
CL CHILE 
CM UNITED REPUBLIC OF CAMEROON 
CN CHINA 
CO COLOMBIA 
CR COSTA RICA 
CS CZECHOSLOVAKIA 
CT CANTON AND ENDERBURY ISLANDS  
CV CAPE VERDE 
CX CHRISTMAS ISLANDS, AUSTRALIA 
CY CYPRUS 
CZ CZECH REPUBLIC 
DE GERMANY, FEDERAL REPUBLIC OF  
DJ DJIBOUTI 
DK DENMARK 

---

## Page 42

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 42 
Country Code Country Name 
DM DOMINICA 
[[DO]] DOMINICAN REPUBLIC 
DZ ALGERIA 
EC ECUADOR 
EE ESTONIA 
EG EGYPT 
EH WESTERN SAHARA 
ES SPAIN 
ET ETHIOPIA 
FI FINLAND 
FJ FIJI 
FK FALKLAND ISLANDS 
FM FEDERATED STATES OF MICRONESIA 
FO FAEROE ISLANDS 
FR FRANCE 
GA GABON 
GB UNITED KINGDOM 
GD GRENADA 
GF FRENCH GUIANA 
GG GUERNSEY 
GH GHANA 
GI GIBRALTAR 
GL GREENLAND 
GM GAMBIA 
GN GUINEA 
GP GUADELOUPE 
GQ EQUATORIAL GUINEA 
GR GREECE 
GT GUATEMALA 
GU GUAM 
GW GUINEA-BISSAU 

---

## Page 43

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 43 
Country Code Country Name 
GY GUYANA 
HK HONG KONG  
HN HONDURAS 
HT HAITI 
HU HUNGARY 
HV UPPER VOLTA 
[[ID]] INDONESIA 
IE IRELAND 
IL ISRAEL 
IM ISLE OF MAN 
IN INDIA 
IO BRITISH INDIAN OCEAN TERRITORY  
IQ IRAQ 
IS ICELAND 
IT ITALY 
JE JERSEY CI 
JM JAMAICA 
JO JORDAN 
JP JAPAN 
JT JOHNSTON ISLANDS 
KE KENYA 
KH DEMOCRATIC KAMPUCHEA 
KI KIRIBATI 
KM COMOROS 
KR KOREA, REPUBLIC OF  
KW KUWAIT 
KY CAYMAN ISLANDS 
KZ KAZAKHSTAN 
LA LAO PEOPLES DEMOCRATIC REPUBLIC  
LB LEBANON 
LC SAINT LUCIA 

---

## Page 44

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 44 
Country Code Country Name 
LI LIECHTENSTEIN 
LK SRI LANKA 
LR LIBERIA 
LS LESOTHO 
LT LITHUANIA 
LU LUXEMBOURG 
LY LIBYAN ARAB JAMAHIRIYA 
MA MOROCCO 
MC MONACO 
MG MADAGASCAR 
MH MARSHALL ISLANDS 
MI MIDWAY ISLANDS 
ML MALI 
MN MONGOLIA 
MO MACAU 
MQ MARTINIQUE 
MR MAURITANIA 
MS MONTSERRAT 
MT MALTA 
MU MAURITIUS 
MV MALDIVES 
MW MALAWI 
MX MEXICO 
MY MALAYSIA 
MZ MOZAMBIQUE 
NA NAMIBIA 
NC NEW CALEDONIA 
NE NIGER 
NF NORFOLK ISLAND 
NG NIGERIA 
NI NICARAGUA 

---

## Page 45

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 45 
Country Code Country Name 
NL NETHERLANDS 
NO NORWAY 
NP NEPAL 
NR NAURU 
NU NIUE 
NZ NEW ZEALAND 
OM OMAN 
PA PANAMA 
PC PACIFIC ISLANDS 
PE PERU 
PF FRENCH POLYNESIA 
PG PAPUA NEW GUINEA 
PH PHILIPPINES 
PK PAKISTAN 
PL POLAND 
PM ST.PIERRE AND MIQUELON  
PN PITCAIRN ISLANDS 
PR PUERTO RICO  
PT PORTUGAL 
PY PARAGUAY 
QA QATAR 
RE REUNION 
RO ROMANIA 
RS SERBIA 
RU RUSSIA 
RW RWANDA 
SA SAUDI ARABIA 
SB SOLOMON ISLANDS 
SC SEYCHELLES 
SE SWEDEN 
SG SINGAPORE 

---

## Page 46

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 46 
Country Code Country Name 
SH ST.HELENA 
SJ SVALBARD AND JAN MAYEN ISLANDS 
SL SIERRA LEONE 
SM SAN MARINO 
SN SENEGAL 
SO SOMALIA 
SR SURINAME 
ST SAO TOME AND PRINCIPE 
SU UNION OF SOVIET SOCIALIST REPUBLICS 
SV EL SALVADOR 
SZ SWAZILAND 
TA TAHITI 
TC TURKS AND CAICOS ISLANDS 
TD CHAD 
TG TOGO 
TH THAILAND 
TK TOKELAU 
TL EAST TIMOR  
TN TUNISIA 
TO TONGA 
TR TURKEY 
TT TRINIDAD AND TOBAGO  
TV TUVALU 
TW TAIWAN 
TZ UNITED REPUBLIC OF TANZANIA  
UA UKRAINIAN SOVIET SOCIALIST R EPUBLIC 
UG UGANDA 
US UNITED STATES OF AMERICA 
UY URUGUAY 
VA HOLY SEE 
VC SAINT VINCENT AND THE GRENADINES 

---

## Page 47

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 47 
Country Code Country Name 
VE VENEZUELA 
VG BRITISH VIRGIN ISLANDS 
VI UNITED STATES VIRGIN ISLANDS 
VN VIET NAM 
VU VANUATU 
WF WALLIS AND FUTUNA ISLANDS  
WK WAKE ISLAND 
WS SAMOA 
XS CEDEL EUROCLEAR 
VR SPAIN 
YD DEMOCRATIC YEMEN 
YE YEMEN 
YU YUGOSLAVIA 
ZA SOUTH AFRICA 
ZM ZAMBIA 
ZW ZIMBABWE 
  

---

## Page 48

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 48 
 
What Is a CAIC Message? 
A Corporate Action Instruction Cancellation Request Message (CAIC) is an inbound message sent by 
participants to communicate withdrawal of a previously submitted and accepted Corporate Action Instruction 
Message (CAIN). 
In other words, a CAIC is a cancellation message related to an existing CAIN message. It is an indication to 
[[DTC]] that the previous CAIN should be cancelled and those instructions should not be processed. 
MX Identifier ISO 20022 Message 
Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTC]] 
Processes 
seev.040.002.xx 3 CA Instruction Cancellation 
Request 
n/a CAIC MT 565 Instruction Wi thdrawal 
 
3 The last two digits in the MX Identifier signify the version number. The MX version number may change during the SWIFT annual release based on 
mandatory or optional updates to the standards.  
Current schemas are available on MyStandards, and [[DTCC]].com. 


---

## Page 49

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 49 
Information Contained on the CAIC Message 
Because you are able to submit multiple instructions on the same event, cancelling your instructions requires 
detailed information in order to ensure that the cancellation corresponds to the correct CAIN instruction. You 
must provide detailed information for the CAIN message for which you are cancelling the instruction. For 
instance, you might submit ten instructions and cancel three of them. 
1. Instruction Cancellation Details. These are items that are specific to the CAIC message. 
• Change Instruction Indicator. Indicates that the cancelled instruction will be replaced by a new 
corporate action instruction to be sent later. Refer to the “Instruction Identification” item in the Rules 
for Required Fields table below. 
2. Instruction Identification. This 16-character identifier matches the cancellation to a previously submitted 
CAIN message.  
3. Event General Details. These are the details contained on the instruction that you are cancelling: 
• Corporate Action Event Identification (CORP). Required by the ISO message. This is the CA [[ID]] 
provided on a previously submitted CAIN.  
• Official Corporate Action Event Identification (COAF). Official Corporate Action Identification. 
This is the CA [[ID]] preceded by “US.” In order for this cancellation to be processed, the COAF on the 
cancellation must match the COAF on the original instruction and announcement messages. 
• Event Type. The type of corporate action event that the original instruction message was responding 
to. 
• Financial Instrument Identification. The security affected by the corporate action as on a previously 
submitted CAIN. 
4. Instruction Details. The information contained in the original instructions: 
• [[Option]] Number. Must match the [[Option]] number in the instruction you are cancelling. An explanation 
of [[Option]] numbers can be found in the Data Dictionary. 
• [[Option]] Type. Must match the [[Option]] type in the instruction you are cancelling. 
• Instructed quantity. This will reflect the quantity provided in the instruction you are cancelling. 
Rules for All Cancellation Messages 
General Message Processing Rules 
1. Each CAIC message will provide cancellation information for only one previously accepted CAIN 
message. 
2. Partial withdrawal of a CAIN message is not permitted.  
3. A user cannot send more than one CAIC message for a particular CAIN message. 
4. CAIC messages for events where the Overall Workflow Status is “Cancelled” will be rejected. 
5. CAIC messages for options where the [[Option]] status is “Deleted” will be rejected. 
6. Instruction cancellation messages will not be accepted if pending or final instructions have been manually 
entered for the event. 
7. A CAIC message must contain all of the following items: 
• Business Message Identifier (BAH), 
• Instruction Identification, 

---

## Page 50

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 50 
• Corporate Action Event Identification (CORP), 
• Official Corporate Action Event Identification (COAF) 
• (optional in the schema but required for processing at [[DTC]]), 
• Event Type (CAEV), 
• Safekeeping Account, 
• [[Option]] Number, 
• [[Option]] Type, and 
• Instructed Quantity (Unit/Amount). 
All other items are optional. 
Additional Rules 
Rules for Required Fields 
Field Rule Comments 
Business Message Identifier (BAH)  1. Must be less than or equal to 16 
characters.  
2. Must not exist in duplicate.  
 
Instruction Identification  3. Must contain a valid Business 
Message Identifier from the instruction 
you are cancelling.   
4. Must be less  than or equal to 16 
characters.  
 
Corporate Action Event 
Identification  
5. Mandatory by ISO schema.  This field is required by the ISO 
schema and it must be 
populated in order to pass 
schema validation. [[DTC]] will not 
process from this field.  
Official Corporate Action Event 
Identification (COAF)  
6. Must be an event that is eligible for 
instructions via ISO messaging  
The COAF will be validated and 
used in the Instruction 
processing by [[DTC]].  
Event Type 7. Must match the exact data that was 
sent in the previously submi tted CAIN.  
 
Safekeeping Account  8. Must be numeric (without leading 
zeroes) only and  
9. Must match the [[participant]] [[ID]] provide d 
by CDTS. 
 
[[Option]] Number 10. Must match the exact data that was 
sent in the previously submitted CAIN.  
 
[[Option]] Type 11. Must match the exac t data that was 
sent in the previously submitted CAIN.   
 

---

## Page 51

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 51 
Field Rule Comments 
Instructed Quantity (Unit/Amount)  12. Must match that on the instruction you 
are cancelling.  
13. Must have a Unit quantity greater than 
zero if the Event Security Type is “Non -
Debt.” 
14. Must have an Amount quantity greater 
than zero if Event Security Issue Type 
is “Debt.” 
 
Cutoff Rules: General 
Click here to see more detailed cutoff information. 
Item Rule 
General Submission Times 1. Cancellation messages follow the same cutoff submission rules that apply to 
instructions. The submission period opens at 12:00 a.m. midnight and closes at 
8:00 p.m. each business day for the majority of CA events (there are instanc es 
where a CA event cutoff is 12:00 p.m., but  this occurs in the minority of cases). 
Instruction ISO 20022 messages may be submitted until the instruction period 
cutoff minus two hours.  
[[Option]] Cutoff Start Date/Time 
(USD Cash [[Option]])  
2. This will be the ear liest [[Option]] Cutoff of the associated service s (DDRP, FCCP, 
or a combination of the two).  
[[Option]] Cutoff End Date/Time 
(USD Cash [[Option]])  
3. This will be the latest [[Option]] Cutoff of the associated services (DDRP, FCCP, 
or a combination of the two).  
  

---

## Page 52

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 52 
 
What is a CACS message? 
A Corporate Action Cancellation Status Advice message (CACS) is an outbound response that indicates 
whether a Corporate Action Instruction Cancellation (CAIC) message submitted by a [[participant]] has been 
accepted or rejected. In other words, [[DTC]] sends a CACS message to inform a [[participant]] of a cancellation 
message’s status. 
MX Identifier ISO 20022 Message 
Names 
Extension Short 
Name 
Equivalent ISO 
15022 
Equivalent [[DTC]] 
Processes 
seev.041.002.xx 4 Corporate Action 
Instruction Cancellat ion 
Request Status Advice 
n/a CACS MT 567 Withdrawa l Reply 
If a CAIC message is successfully accepted and processed, [[DTC]] will send a CACS message to the originating 
[[participant]] which indicates its acceptance. Likewise, if the CAIC is rejected, [[DTC]] will indicate that in the 
corresponding CACS message.  
 
4 The last two digits in the MX Identifier signify the version number. The MX version number may change during the SWIFT annual release based on 
mandatory or optional updates to the standards.  
Current schemas are available on MyStandards, and [[DTCC]].com. 


---

## Page 53

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 53 
Information Contained on the CACS Message 
The following table contains all of the information elements presented on a CACS message, along with an 
explanation of what each element means and/or applicable details. 
Data Element Definition/Information  
Instruction 
Identification 
The Business Message Identifier of the received cancellation instruction. This 16- character 
identifier matches the status message to a previously submitted CAIN message. Every ISO 
message must have a Business Message Identifier, or BAH.  
Corporate Action 
Event Identification  
The CORP, or Corporate Action Event Identification, is specified on the received cancellation 
instruction. Leading zeroes will be suppressed.  
Official Corporate 
Action Event 
Identification  
The COAF, or the Official Co rporate Action Identification, on the received cancellation 
instruction. This is the CA [[ID]] preceded by “US.”  
Event Type The type of corporate action event that the original instruction message was responding to. 
Specified on the received cancellation ins truction. 
[[Option]] Number Specified on the received cancellation instruction.  
[[Option]] Type Specified on the received cancellation instruction:  
New [[DTCC]] 
Model [[Option]] 
Type 
[[Option]] Type Description  ISO 20022 
[[Option]] Type 
(Extended) 
Extended 
[[Option]]  
Feature 
Cash and 
[[securities]] 
Holder will receive a combination of 
cash and [[securities]] (may be 
applicable to Optional [[Dividend]] 
Service [OPS]). 
CASE 
 
Cash Holder will receive cash (may be 
applicable to Optional [[Dividend]] 
Service [OPS]). 
CASH 
 
DRIP Holder elects to receiv e additional 
[[securities]] instead of the cash 
distribution. [[Option]] may be declared 
by the [[issuer]] or as a service offered 
by [[DTC]]. 
SECU 
 
Foreign Tax 
Unfavorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for the Foreign 
Tax Relief service at [[DTC]]. Op tion to 
select unfavorable tax rate. The 
Foreign Tax Unfavorable [[Option]] is 
the [[default]] [[Option]].  
CASH FORU 
Foreign Tax 
Favorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for the Foreign 
Tax Relief service at [[DTC]]. 
[[participant]] receives their payment at 
a favorable tax withholding rate.  
CASH FORF 

---

## Page 54

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 54 
Data Element Definition/Information  
Foreign Tax 
Exempt 
[[DTC]]-only [[Option]]. The event and 
security are eligible for the Foreign 
Tax Relief service at [[DTC]]. 
[[participant]] is exempt from any tax 
withholding.  
CASH FORX 
DRIP 
Unfavorable 
[[DTC]]-only opt ion. The event and 
security are eligible for both the 
[[Dividend]] Reinvestment and Foreign 
Tax Services at [[DTCC]]. Participants 
will receive additional [[shares]] and 
the tax withholding on those [[shares]] 
will be at the unfavorable tax rate.  
SECU DRPU 
DRIP 
Favorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
[[Dividend]] Reinvestment and Foreign 
Tax Relief Services at [[DTCC]]. 
Participants will receive additional 
[[shares]] and the tax withholding on 
those [[shares]] will be at the favorable 
tax rate.  
SECU DRPF 
DRIP Exempt [[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
[[Dividend]] Reinvestment and the 
Foreign Tax Relief service at [[DTCC]]. 
Participants will receive additional 
[[shares]] and will be exempt from any 
tax withholding.  
SECU DRPX 
Foreign 
Currency 
Payment 
[[DTC]]-only [[Option]]. The event and 
security are eligible for the Foreign 
Currency Payment service at [[DTCC]]. 
Participants will receive their 
distribution in the foreign currency 
instructed.  
CASH FCPP 
Foreign 
Currency 
Payment 
Unfavorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
Foreign Currency and Foreign Tax 
services at [[DTCC]]. Participants will 
receive their distribution in a foreign 
currency and the tax withholding on 
that dis tribution will be subject to 
unfavorable tax withholding.  
CASH FCPU 
Foreign 
Currency 
Payment 
Favorable 
[[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
Foreign Currency and Foreign Tax 
services at [[DTCC]]. Participants will 
receive their di stribution in a foreign 
currency and the t ax withholding on 
that distribution will be subject to 
favorable tax withholding.  
CASH FCPF 

---

## Page 55

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 55 
Data Element Definition/Information  
Foreign 
Currency 
Payment 
Exempt 
[[DTC]]-only [[Option]]. The event and 
security are eligible for both the 
Foreign Currency and Foreign Tax 
services at [[DTCC]]. Participants will 
receive their distribution in a foreign 
currency and will be exempt from 
any tax withholding.  
CASH FCPX 
[[securities]] Hold er will receive [[securities]] (may 
be applicable to Optional [[Dividend]] 
Service [OPS]). 
SECU 
 
 
Safekeeping Account  Specified on the r eceived cancellation instruction. Leading zeroes will be suppressed.  
Status Quantity (Unit) When the Event Security is “[[Equity]] (non- debt),” then the Status Quantity (Unit) equals the total 
of all instructions made under this event.  
This is the Instructed  Balance (Unit) specified on the received cancellation instruction. Leading 
zeroes will be suppressed.  
Status Quantity 
(Amount)  
When the Event Security is “Debt,” then the Status Quantity (Amount) equals the total of all 
Instructions made under this event . 
This is the Instructed Balance (Quantity) specified on the received cancellation instruction. 
Leading zeroes will be suppressed.  
Accept Advice:  The following field is populated if the cancellation was accepted.  
Instruction 
Processing Status 
(/NoSpcfdRsn) 
This field defaults to ‘NORE’ if the cancellation message was accepted.  
Reject Advice: The following fields are populated if the cancellation was rejected.  
Instruction 
Processing Status 
(/Cd) 
Please see the reject reason codes  immediately following this table.  
Additional Reason 
Information 
When an error code of ‘OTHR’ is used, [[DTC]] often provides a descriptive error message in this 
field. Please see the OTHR  code reasons later in this section.  
Reject Codes 
The following tables contain lists of error codes and their explanations. The first table provides the full list of 
regular codes. The second table elaborates on the “OTHR” error code and provides a list of the real-text 
reasons that can accompany this code on a rejection message. 
Reject Codes 
Reject Code Description 
ADEA Account Servicer Deadline Missed  

---

## Page 56

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 56 
Reject Code Description 
DESC More than one underlying security was provided  
or 
Underlying security is not a [[CUSIP]]  
OTHR Other (see table) 
ULNK Invalid reference: instruction identification not found 
“OTHR” Code Reasons 
ISO Code Reason 
OTHR Business Message Identifier length exceeds 16 characters  
OTHR Corporate Action Event is either Deleted or Cancelled  
OTHR Duplicate request received  
OTHR Incorrect Event Type  
OTHR Mandatory Business Message Identifier is missing 
OTHR Mandatory Event Type is missing 
OTHR Mandatory Instruction Identification is missing 
OTHR Mandatory Official Corporate Action Event Identification is missing  
OTHR Mandatory [[Option]] Number is missing  
OTHR Mandatory [[Option]] Type is missing  
OTHR Mandatory Safekeeping Account is missing  
OTHR Manual Election Instruction(s) exist(s)  
Troubleshooting Message Rejection 
The following table contains a list of common errors that may occur within particular data elements. It provides 
possible reasons for the errors and the bulleted items suggest corrective actions for them. 
Data Element Error 
Code 
Problem/Corrective Action  
Instruction 
Identification 
ULNK The Instruction Identifier does not match the Business Message Identifier of the 
instruction being cancelled.  
• Edit the Instruction Identification to match the Business Message Identifier of the 
instruction being cancelled.  
Corporate Action 
Event Identification  
EVNM The Corporate Action Event Identification does not match the CA [[ID]] on the 
instruction being canceled.  
• Edit the CA [[ID]] to match the CA [[ID]] on the instruction being cancelled.  

---

## Page 57

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 57 
Data Element Error 
Code 
Problem/Corrective Action  
Official Corporate 
Action Event 
Identification  
EVNM This field  is optional in the schema but mandatory for [[DTC]] processing. This error  
occurs when the value of this item does not match the Official CA [[ID]] on the 
instruction being cancelled.  
• Edit the Official CA [[ID]] to match the official CA [[ID]] on th e instruction being 
cancelled.  
Event Type OTHR Event Type does not match that on the instruction being cancelled. Additional 
Reason Information field reads “Incorrect Event Type.”  
• Edit the value of the Event Type to match that on the instruction being canceled.  
Financial Instrument 
Identification  
DSEC (Optional; recommended by the [[securities]] Market Practice Group [SMPG]). Value 
does not match that on the instruction being cancelle d. Additionally, only one 
underlying security is accepted. That value must be a [[CUSIP]] number.  
• Edit the value of the Financial Instrument Identification to match that on the 
instruction being cancelled.  
• Ensure that only one security is referenced.  
• Ensure th e security value is a [[CUSIP]] number.  
Safekeeping Account  SAFE Safekeeping account information [[DO]] es not match validity rules:  
• Must be a [[DTC]] [[participant]] account.  
• Number must not contain leading zeroes (for example: “1” instead of “0001,” “11” 
instead of “0011,” etc.). 
• Edit the Safekeeping Account number to match the rules above.  
[[Option]] Number NMTY [[Option]] number does not match the [[Option]] type selected.  
• Check the value of the [[Option]] Type. If it doesn’t match this [[Option]] number, 
change the [[Option]] type.  
Note: 
The [[Option]] Type must still match that in the instruction being cancelled. If there is 
still a dis crepancy, trace the error back via the COAF to inves tigate the original 
information.  
[[Option]] Type OPTY [[Option]] type does not match that of the instruction being cancelled.  
• Edit the value of the [[Option]] Type to match the instruction being cancelled for this 
[[Option]].  
Instructed Quantity  DQUA Instructed Quantity  is not a valid amount.  
• If face amount was used for debt per market practice, make sure that it was 
correctly converted to quantity.  
• Edit the value of the Instructed Quantity to reflect a valid amount.  
 LACK Instructed Quantity is greater than the eligible quantity.  
• Edit the Instructed Quantity to be less than or equal to the eligible quantity.  
 

---

## Page 58

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 58 
 
 
What is a CAST Message? 
The Corporate Action Statement Report (CAST) is an outbound message created at the end of each business 
day beginning five days prior to the end of the instruction period (i.e., cutoff date). It provides each subscribed 
customer with their instructed and uninstructed balances for each CA Event, as well as Options that fall within 
the eligible [[DTC]] service’s reporting period. 
One corporate action event is reported on each CAST statement. The CAST serves as a balance sheet that 
reports, per event, all of a [[participant]]’s eligible balances, instructed balances, and uninstructed balances per 
[[Option]] as of the statement date. 
MX Identifier ISO 20022 Message Name Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTC]] 
Processes 
seev.042.002.xx 5 Corporate Actions Instruction 
Statement Report  
n/a CAST n/a New 
 
5 The last two digits in the MX Identifier signify the version number. The MX version number may change during the SWIFT annual release based on 
mandatory or optional updates to the standards. 
Current schemas are available on MyStandards, and [[DTCC]].com. 


---

## Page 59

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 59 
Information contained on the CAST message 
1. [[participant]] Number/Safekeeping Account. The [[DTC]]-assigned internal [[participant]] identification number. 
2. Event General Details. These are the details that are specific to the event and carry over to all 
messages: 
• COAF. Official Corporate Action Identification. This is the CA [[ID]] preceded by “US.”  
• Event Type. The type of corporate action event (e.g., Exchange Offer, Final Paydown). 
• Underlying Security. The security affected by the corporate action. 
• Instruction Details. The information contained in the original instructions, including [[Option]] details: 
o Instructed quantity. 
o [[Option]] number. 
o [[Option]] type. 
o Instructed quantity. This cannot exceed the eligible balance. 
3. Balances: 
• Total Eligible Balance. This is the record date position. 
• Total Uninstructed Balance as of the statement date. 
• Total Instructed Balance per [[Option]] as of the statement date. 
• Breakdown by [[Option]]. 
• Other balances. 
Rules for CAST Messages 
General Message Processing Rules 
1. Each CAST message is unique per customer and per CA event level (with all instructed options reported). 
2. Customers can only receive messages regarding CA events and options to which they themselves are 
entitled 
Inclusions in the CAST Messages 
1. A maximum of 300 options for each CA event will be reported in each message.  
2. The report will exclude reporting of the following items: 
a. CA events with an overall workflow status of “Deleted” or “Cancelled.” 
b. Options with an [[Option]] status of “Deleted.” 
3. The following services will be included on the CAST messages: 
• Foreign Currency Payments (FCP) 
• Foreign Tax Relief (FOR) 
• Optional Dividends (OPS) 
• [[Dividend]] Reinvestment Program (DRP) 
• Direct Payment (FCP) 
a. For non-Canadian issues, this report will only be issued if the [[participant]] [[ID]] and [[CUSIP]] are 
found in the system. 
• [[Cash-in-Lieu]]/Round Up 

---

## Page 60

ISO 20022 Messaging for Distributions Instructions  
An Introduction to ISO 20022 Mess aging 60 
4. The remaining services, excepting U.S. Tax Withholding Instructions, are instructed and reported at the 
[[Option]] level. 
5. U.S. tax withholding instructions are made at the payout level; therefore, they are excluded from the CAST 
message reporting.  
6. This report will also include the cash instructions made from straight FCP/DRP services (Options are 
FCPP and DDRP). 
• CIL/Round-Up (CRS) 
Message Timing 
1. The reporting period is the same as the Instruction (or [[Option]] Cutoff) period between the Start Date and 
the Cutoff Date of the eligible service/[[Option]].  
2. If there are multiple services on the same event, the reporting will begin on the earliest Start Date of the 
services and end on the latest Cutoff Date of the services. 
3. The CAST report will be distributed each business day at approximately 11 p.m. 
4. On cutoff date, you will receive a CAST report detailing your final inventory of instructions. 
 

---

## Page 61

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 