---
title: "ISO 20022 Messaging For Distributions Entitlements and Allocations"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO_20022_EntAlloc_UG.pdf"
pages: 88
size: "3841.7 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO 20022 Messaging For Distributions Entitlements and Allocations

**Original File:** [ISO_20022_EntAlloc_UG.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO_20022_EntAlloc_UG.pdf)  
**Category:** Other  
**Total Pages:** 88  
**File Size:** 3841.7 KB  

---

## Page 1

 
 
 
[[DTC]] CORPORATE ACTIONS 
USER GUIDE: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS 
AND ALLOCATIONS 
VERSION 2.2 
DECEMBER 21, 2022 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
This guide is meant as an educational tool to assist in your understanding of ISO 20022 messaging as it relates to 
corporate action processing at [[DTCC]]. It should not be used as a basis for systems applications coding. For coding 
purposes, please refer to specific schemas and message implementation guides that can be found at 
http://www.[[DTCC]].com/[[settlement]]-and-[[Asset]]-services/corporate-actions-processing/iso-20022-messaging-specifications. 
 
Doc Date: December 21, 2022 
Publication Code: CA234 
Service: [[Asset]] Services 
Title: User Guide: ISO 20022 Messaging for Distributions Entitlements and Allocations 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
An Introduction to ISO 20022 Messaging .......................................................................................................... 7 
What is ISO 20022 Messaging? ......................................................................................................................... 7 
Benefits of Using ISO 20022 Messaging for Corporate Actions ......................................................................... 7 
Benefits of Using ISO 20022 Schemas for Entitlements and Allocations Processing ...................................... 7 
Corporate Actions Messages in the Entitlements and Allocations Workflow ..................................................... 7 
How to Read an MX Identifier ............................................................................................................................. 8 
[[BASIC]] Message Flow of the Distribution Lifecycle ............................................................................................... 9 
Entitlements and Allocations Messaging ........................................................................................................ 11 
Entitlements/Allocations Event Types Currently Supported by ISO 20022 Messaging for Distributions  .........11 
Message Extensions and [[Stock]] Loan, REPO, and Fail Tracking ....................................................................15 
Messages and Zero Amounts ...........................................................................................................................15 
[[Entitlement]] and Allocation Message Flows ......................................................................................................15 
[[BASIC]] Flow .......................................................................................................................................................15 
Exception Flow ................................................................................................................................................16 
Example of a Cash [[Dividend]]–[[BASIC]] Message Flow ........................................................................................19 
Example of a Same-Day Reversal ..................................................................................................................20 
Example of a Post-Payable Allocation Adjustment .........................................................................................21 
Late Announcements ......................................................................................................................................22 
Scenario 1: All Details Known .......................................................................................................................23 
Scenario 2: Most Details Known ....................................................................................................................23 
Scenario 3: Few Details Known .....................................................................................................................24 
Scenario 4: No Details Known .......................................................................................................................24 
Message Subscriptions and Timing ..................................................................................................................24 
Subscription Options .......................................................................................................................................25 
Weekly Messaging Times ...............................................................................................................................26 
Holiday Processing Schedule .........................................................................................................................27 
What is a CANO-E Message? ..........................................................................................................................28 
When Are CANO-E Messages Generated? .....................................................................................................29 

---

## Page 4

 
 
Intraday Position Capture ................................................................................................................................30 
Message Timing ..............................................................................................................................................30 
Weekly Messaging Times ...............................................................................................................................30 
Holiday Processing Schedule .........................................................................................................................31 
Information Contained on the CANO-E Message .............................................................................................31 
Examples and Scenarios for CANO-E Messages ............................................................................................34 
CANO-E for Position Adjustments ..................................................................................................................34 
CANO-E for Market Record Date or New York Record Date ..........................................................................36 
Announcement Deleted; CA [[ID]] Remains in CA Web .....................................................................................37 
What is a CAPA Message? ..............................................................................................................................38 
CAPA Message Creation and Timing ...............................................................................................................39 
What are the CAPA Subscription Options?.....................................................................................................39 
When are CAPA NEWM/REPL Messages Sent? ...........................................................................................40 
CAPA and CAPC Messages ...........................................................................................................................42 
Messaging Notes .............................................................................................................................................42 
Intraday Position Capture ................................................................................................................................42 
CAPA Messages and Reversals .....................................................................................................................43 
Messages and Zero Amounts .........................................................................................................................43 
Late Announcements ......................................................................................................................................43 
Weekly Messaging Times ...............................................................................................................................43 
Holiday Processing Schedule .........................................................................................................................43 
Information Contained on the CAPA Message .................................................................................................44 
CAPA Message Data ........................................................................................................................................48 
What is a CAPC Message? ..............................................................................................................................51 
CAPA and CAPC Messages ...........................................................................................................................51 
When Are CAPC Messages Generated? .........................................................................................................51 
Messaging Note ..............................................................................................................................................52 
Weekly Messaging Times ...............................................................................................................................52 
Holiday Processing Schedule .........................................................................................................................52 
Information Contained on the CAPC Message .................................................................................................52 

---

## Page 5

 
 
CAPC Message Data ........................................................................................................................................53 
What is a CACO Message? ..............................................................................................................................54 
When Are CACO Messages Generated? .........................................................................................................55 
Messaging Notes .............................................................................................................................................56 
CACO Message Sequence for Late Announcements .....................................................................................56 
Weekly Messaging Times ...............................................................................................................................56 
CACO Holiday Processing Schedule ..............................................................................................................57 
CACO Adjustment Codes................................................................................................................................57 
Information Contained on the CACO Message ................................................................................................57 
Message Body .................................................................................................................................................58 
CACO Message Data .......................................................................................................................................61 
What is a CARE Message? ..............................................................................................................................63 
When Are CARE Messages Generated? .........................................................................................................64 
Messaging Notes .............................................................................................................................................64 
Weekly Messaging Times ...............................................................................................................................64 
CARE Holiday Processing Schedule ..............................................................................................................65 
Information Contained on the CARE Message .................................................................................................65 
Message Body .................................................................................................................................................65 
CARE Message Data ........................................................................................................................................66 
What is a CAPS Message? ..............................................................................................................................68 
When Are CAPS Messages Generated? .........................................................................................................69 
Messaging Notes .............................................................................................................................................69 
Weekly Messaging Times ...............................................................................................................................69 
CAPS Holiday Processing Schedule ...............................................................................................................70 
Information Contained on the CAPS Message .................................................................................................70 
Message Body .................................................................................................................................................70 
CAPS Message Data ........................................................................................................................................73 
CAPS Reason Codes .......................................................................................................................................73 
Appendix A: Reason Codes .............................................................................................................................. 74 
Adjustment Reason Codes (CAPA/CACO Message).......................................................................................74 

---

## Page 6

 
 
CAPA/CACO Sub Reason Codes ....................................................................................................................75 
Unallocated Reason Codes (CAPS Message) .................................................................................................84 
OTHR vs. NPAY ISO Codes ...........................................................................................................................85 
 

---

## Page 7

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
An Introduction to ISO 20022 Messaging 7 
 
AN INTRODUCTION TO ISO 20022 MESSAGING 
What is ISO 20022 Messaging? 
ISO 20022 is an international messaging standard that is designed to simplify global busines s communication 
by creating a common language for communicating financial information that is unrestricted by national borders 
or regional conventions. 
Even though the Depository has maintained its own proprietary formats for many years, [[DTCC]] recognized th at 
it needed to respond to an evolving business environment and to accommodate an increasingly global 
investment business. [[DTCC]]'s clients and customers had expanded their businesses throughout the world and 
wanted to streamline, as much as possible, the standards and formats used to communicate. ISO 20022 meets 
those needs and offers a host of benefits. 
[[DTCC]] is therefore moving all of its corporate actions announcements and processing files from proprietary 
formats to this external, international format. 
Benefits of Using ISO 20022 Messaging for Corporate Actions 
One of the greatest benefits of ISO 20022 is its consistency and universality across the industry and around 
the globe. It provides a common language with its own ever-growing dictionary, enabling businesses in the 
financial industry to communicate corporate action information quickly, easily, and precisely.  
On a more local scale, the automation of previously manual processes via ISO 20022 messaging provides a 
significant cost savings to clients and a tremendous reduction in risk to the industry. With the advent of real - 
time messaging via ISO 20022, clients receive their data in a much more timely fashion, which allows them to 
manage their risk and streamline their processes. 
Benefits of Using ISO 20022 Schemas for Entitlements and Allocations 
Processing 
The six messages used in this portion of the Distributions lifecycle are more streamlined and contain fewer 
data elements than the CANO announcements message. These messages [[DO]] not replay all of the original 
CANO information, but instead use the Corporate Actions Identifier (CAID) and the Official Corporate Action 
Event Identification (COAF) to link back to the original announcement. 
This allows the six messages to focus on specific pieces of information related to the movement of cash and 
[[Stock]] entitlements. 
Corporate Actions Messages in the Entitlements and Allocations 
Workflow 
There are fifteen types of messages in the ISO 20022 group: 

---

## Page 8

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
An Introduction to ISO 20022 Messaging 8 
 
 
The messages specifically involved in the [[Entitlement]] and allocation process are: 
• Corporate Action Notification with Eligible Balance (CANO-E) 
• Corporate Action Movement Preliminary Advice (CAPA) 
• Corporate Action Movement Preliminary Advice Cancellation Advice (CAPC)  
• Corporate Action Movement Confirmation (CACO) 
• Corporate Action Movement Reversal Advice (CARE) 
• Corporate Action Event Processing Status Advice (CAPS) 
 
The messages illustrate the record date position capture, interim tracking, projected allocations, canceled 
projections, allocations, post-allocation adjustments, unallocated positions, and same-day payable date 
reversals. 
All of the messages involved in this process are contingent upon the client having position in an event. Unless 
you have position, you will not see any of these messages. 
How to Read an MX Identifier 
The MX Identifier identifies the business area, message [[ID]], and version of an ISO Message.  
As an example, for the identifier seev.036.002.06: 
• The first four alphabetic characters (“seev”) identify the business area. In this case, it is “[[securities]] 
Events.” You can see the full list of business areas on the ISO 20022 Web site at 
https://www.iso20022.org/iso-20022-message-definitions?business-domain=6 


---

## Page 9

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
An Introduction to ISO 20022 Messaging 9 
 
• The next three characters (036) are the message identifier. The message in this example is a CACO 
message. 
• The next three characters (002) are the “variant” identifier. Since “001” is always the main ISO message, 
“002” would be the second variant (and the one that is compatible with ISO 15022). [[DTCC]] is using the 
second variant in order to comply with the industry’s requirement that the ISO 20022 messages we 
generate be backward compatible with ISO 20022. 
• The last two characters (06) are the “version.” In this example, this is the sixth version of this message, 
representing SR 2015. 
Note: 
The final two digits have the potential to change with each release. 
For your coding purposes, be sure to consult the latest documentation for the most curre nt version 
number. 
[[BASIC]] Message Flow of the Distribution Lifecycle 
The following graphic provides a high-level view of the [[BASIC]] flow of the distributions lifecycle. 
It does not include exceptions such as event cancellations, instruction withdrawals, allocation reversals, 
unallocated funds, etc. It is meant to give the user a high-level overview of the message and business flows as 
a starting point for understanding ISO 20022 messaging. 
Note: 
Throughout this document, blue boxes represent inbound messages to [[DTCC]] from the client and green boxes represent 
outbound messages to the client from [[DTCC]]. 
 
1. [[DTCC]] sends a CANO to the client that announces the corporate action event. The CANO contains an 
indicator signaling that the event is eligible for ISO 20022 instruction messaging. 
2. On Record Date, [[DTCC]] sends a CANO-E to inform the client about how it is specifically affected by the 
corporate action: its eligibilities and options. 
3. The client submits a CAIN message to [[DTCC]], providing instructions for that event. 
4. [[DTCC]] sends a CAIS message containing status information about the instructions back to the client.  
5. [[DTCC]] sends a CAPA message to the client projecting its payment/allocation.  


---

## Page 10

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
An Introduction to ISO 20022 Messaging 10 
 
6. After all actions specified in the CAIN (and any in the follow-up messages not specified in this flow) have 
been taken, [[DTCC]] sends the client a CACO message to confirm movement of payment/allocation 
proceeds. 
Note: 
The CAIN and CAIS messages are discussed in the Instructions User Guide, as they are instruction messages. 
Please see the Entitlements/Allocations Messaging section for a more detailed explanation and examples of 
alternate process flows. For specific message information, visit the Learning Center’s Messages and Scenarios 
page. 

---

## Page 11

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 11 
 
ENTITLEMENTS AND ALLOCATIONS MESSAGING 
Entitlements/Allocations Event Types Currently Supported by ISO 
20022 Messaging for Distributions 
In the new data model, these events and event subtypes represent function codes 02 through 49 in the legacy 
[[DTCC]] data model. 
Event Name Sub 
Event 
Name 
Function 
Code/Activity 
Code 
Function Code Name/Activity 
Code Name 
ISO 
Event 
Code 
Event Type 
Name 
Extended 
([[DTCC]]) 
Event 
Subtype 
Automatic 
[[Dividend]] 
Reinvestment 
 FC-31 Automatic [[Dividend]] 
Reinvestment 
DRIP [[Dividend]] 
Reinvestment 
 
Capital Gains 
Distribution 
 FC-32 
FC-33 
FC-49 
Long Term Capital Gains 
Short term Capital Gains 
Capital Gains 
CAPG Capital Gains 
Distribution 
 
Capital Gains 
Distribution 
DRIP 
([[DTCC]] 
only) 
FC-32 
FC-33 
FC-49 
FC-30 
Long Term Capital Gains 
Short term Capital Gains 
Capital Gains 
[[Dividend]] Reinvestment 
CAPG Capital Gains 
Distribution 
 
Capital Gains 
Distribution 
Opt Out 
([[DTCC]] 
Only) 
FC-32 
FC-33  
FC-49 
FC-30 
Long Term Capital Gains  
Short term Capital Gains 
Capital Gains 
[[Dividend]] Reinvestment 
CAPG Capital Gains 
Distribution 
 
Cash [[Dividend]]  FC-07 
FC-08 
FC-09 
Cash Div. on Increased [[shares]] 
Cash [[Dividend]] 
Foreign Cash [[Dividend]] 
DVCA Cash [[Dividend]]  
Cash [[Dividend]]  FC-08 
FC-09 
FC-35 
FC-37 
Cash [[Dividend]] 
Foreign Cash [[Dividend]] 
Tax Exempt Div Service 
Foreign Cash Div Favorable 
DVCA Cash [[Dividend]]  
Cash [[Dividend]] Currency 
Election 
FC-08 
FC-09 
Cash [[Dividend]] 
Foreign Cash [[Dividend]] 
DVCA Cash 
[[Dividend]] 
 

---

## Page 12

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 12 
 
Event Name Sub 
Event 
Name 
Function 
Code/Activity 
Code 
Function Code Name/Activity 
Code Name 
ISO 
Event 
Code 
Event Type 
Name 
Extended 
([[DTCC]]) 
Event 
Subtype 
Cash 
[[Dividend]] 
DRIP 
([[DTCC]] 
only) 
FC-08 
FC-09 
FC-30 
FC-35 
FC-37 
Cash [[Dividend]] 
Foreign Cash [[Dividend]] DRIP 
Tax Exempt Div Service 
Foreign Cash Div Favorable 
DVCA Cash [[Dividend]]  
Cash 
[[Dividend]] 
Opt Out 
([[DTCC]] 
Only) 
FC-08 
FC-09 
FC-30 
FC-35 
FC-37 
Cash [[Dividend]] 
Foreign Cash [[Dividend]] DRIP 
Tax Exempt Div Service 
Foreign Cash Div Favorable 
DVCA Cash [[Dividend]]  
[[default]] Interim 
Payment 
AC-86P Interim [[default]] Distribution DFLT Bond [[default]]  
Distribution  FC-43 Special Distributions OTHR Other Event  
Distribution  FC-43 
FC-06/11/12 
Special Distributions 
[[Stock]] [[Dividend]]/SpinOff 
Eligible/SpinOff InEligible 
OTHR Other Event  
Distribution DRIP 
([[DTCC]] 
only) 
FC-43 
FC-30 
Special Distributions 
DRIP ([[UIT]]-related) 
OTHR Other Event  
Distribution Opt Out 
([[DTCC]] 
only) 
FC-43 
FC-30 
Special Distributions 
DRIP ([[UIT]]-related) 
OTHR   
Distribution 
[[Dividend]] with 
[[Option]] 
Tax 
Credit 
FC 24 
FC-14 
FC-15 
FC-16 
FC-17 
FC-18 
FC-19 
FC-20 
FC-21 
Tax Credit (Build America 
[[Bonds]]) 
Optional [[Dividend]] 
Optional [[Dividend]]–[[Stock]] 
Optional [[Dividend]]-Cash [[Stock]] 
Optional [[Dividend]]-Cash 
Optional [[Dividend]]-Fractions 
Optional [[Dividend]]-Fractions 
Optional [[Dividend]]-Fractions 
Optional [[Dividend]]-Fractions 
OTHR 
DVOP 
Other Event 
[[Dividend]] 
[[Option]] 
 
Interest  FC-13 
FC-23 
Bond Interest 
Muni Bond Interest 
INTR Interest 
Payment 
 

---

## Page 13

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 13 
 
Event Name Sub 
Event 
Name 
Function 
Code/Activity 
Code 
Function Code Name/Activity 
Code Name 
ISO 
Event 
Code 
Event Type 
Name 
Extended 
([[DTCC]]) 
Event 
Subtype 
Interest  FC-03 
 
FC-04 
 
FC-05 
Foreign Debt Unfavorable Tax 
Rate 
Foreign Debt Favorable Tax 
Rate* 
Foreign Debt Exempt Tax Rate* 
INTR Interest 
Payment 
 
Interest DRIP 
([[DTCC]] 
only) 
FC-13 
FC-03 
 
FC-04 
 
FC-05 
FC-23 
FC-30 
Bond Interest 
Foreign Debt Unfavorable Tax 
Rate 
Foreign Debt Favorable Tax 
Rate* 
Foreign Debt Exempt Tax Rate* 
Muni Bond Interest 
DRIP 
INTR Interest 
Payment 
 
[[liquidation]] Based on 
Record 
Date 
Holdings 
FC-45  
FC-11/12 
[[liquidation]] 
SpinOff Eligible/SpinOff 
InEligible 
LIQU [[liquidation]] 
[[Dividend]] 
 
Pay in Kind  FC-38 Pay in Kind-[[Bonds]] PINK Payment in 
Kind 
 
Principal  FC-25 Principal Payment PRED Partial 
Redemption 
Without 
Nominal Value 
Reduction 
 
Principal DRIP 
([[DTCC]] 
only) 
FC-25  
FC-30 
Principal Payment 
DRIP 
PRED Partial 
Redemption 
Without 
Nominal Value 
Reduction 
 
Return of 
Capital 
 FC-34 Return of Capital CAPD Capital 
Distribution 
 
Return of 
Capital 
DRIP 
([[DTCC]] 
only) 
FC-34  
FC-30 
Return of Capital  
DRIP 
CAPD Capital 
Distribution 
 
Return of 
Capital 
DRIP 
([[issuer]]) 
FC-34 Return of Capital CAPD Capital 
Distribution 
DRPI 

---

## Page 14

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 14 
 
Event Name Sub 
Event 
Name 
Function 
Code/Activity 
Code 
Function Code Name/Activity 
Code Name 
ISO 
Event 
Code 
Event Type 
Name 
Extended 
([[DTCC]]) 
Event 
Subtype 
Return of 
Capital 
Opt Out 
([[DTCC]] 
Only) 
FC-34  
FC-30 
Return of Capital  
DRIP 
CAPD Capital 
Distribution 
 
Return of 
Capital 
Sale of 
Assets 
FC-46 Sale of Assets DRCA Capital 
Distribution 
SALE 
Rights 
Distribution 
 FC-39  
FC-47 
Rights Distributions  
Redemption of Rights 
RHDI Rights Issue  
Rights 
Distribution 
Physical 
Rights 
not 
Issued 
FC-39 Rights Distributions RHDI Rights Issue PRNI 
Sale Of Rights [[ADR]] FC-36 Sale of Rights on ADRs DRCA Cash 
Distribution 
From Non 
Eligible 
[[securities]] 
Sales 
 
Sale Of Rights Poison 
Pill 
FC-47 Redemption of Rights EXRI Call on 
Intermediate 
[[securities]] 
POPI 
Special 
[[Dividend]] 
 FC-43 Special Cash Distributions DVCA Cash [[Dividend]]  
Special 
[[Dividend]] 
Currency 
Election 
FC-43 Special Cash Distributions DVCA Cash [[Dividend]]  
Special 
[[Dividend]] 
DRIP 
([[DTCC]] 
only) 
FC-43 
FC-30 
Special Cash Distributions  
DRIP 
DVCA Cash [[Dividend]]  
Special 
[[Dividend]] 
Opt Out 
([[DTCC]] 
Only) 
FC-43  
FC-30 
Special Cash Distributions  
DRIP 
DVCA Cash [[Dividend]]  
Spin-Off  FC-12 FC-11 SpinOff Eligible SpinOff 
Ineligible 
SOFF Spin-Off  
Spin-Off  FC-14  
FC-15  
FC-17  
FC-18 
FC-19 
Optional [[Dividend]] 
Optional [[Dividend]]-[[Stock]] 
Optional [[Dividend]]-Cash 
Optional [[Dividend]]-Fractions 
Optional [[Dividend]]-Fractions 
SOFF Spin-Off  

---

## Page 15

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 15 
 
Event Name Sub 
Event 
Name 
Function 
Code/Activity 
Code 
Function Code Name/Activity 
Code Name 
ISO 
Event 
Code 
Event Type 
Name 
Extended 
([[DTCC]]) 
Event 
Subtype 
[[Stock]] 
[[Dividend]] 
 FC-48  
FC-06 
[[ADR]] Issuance Fee  
[[Stock]] [[Dividend]] 
DVSE [[Stock]] [[Dividend]]  
[[Stock]] Split  FC-02 [[Stock]] Split SPLF [[Stock]] Split  
Tax Refund  FC-09  
FC-40(s) 
Foreign Cash [[Dividend]]  
Foreign Tax Refunds 
TREC Tax Reclaim  
 
Message Extensions and [[Stock]] Loan, REPO, and Fail Tracking 
[[Stock]] loan, REPO, and Fail balances can be found in the core section of the CAPA and CACO messages. You 
can find contra party balances in the extension for each message. 
Note: 
CANO-E messages [[DO]] not have Fail tracking. [[Stock]] loan and REPO balances (as well as contra information) can be found 
in the message extension. 
Please see the CANO-E, CAPA, and CACO sections for more information. 
Messages and Zero Amounts 
Projection amounts of zero are possible in the [[DTCC]] ISO 20022 messages. This may occur in several cases, 
including: 
1. A CAPA message projecting on an event that has a rate of “0” prior to the payable date.  
You can see an example of this in the second scenario for Late Announcements, in which some of the 
corporate actions details are known but the rate is not. 
2. Any [[Stock]] Loan, REPO, and/or Fail activity in which the trade is still pending. 
[[Entitlement]] and Allocation Message Flows 
[[BASIC]] Flow 
The [[BASIC]] message flow for Distributions was presented above. Entitlements and allocations messages 
comprise a subset of this flow1. 
 
1 These message flows will become more complicated and include other message types when exceptions such as event cancellations,  instructions 
withdrawals, allocation reversals, etc. occur. 

---

## Page 16

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 16 
 
The simplest message flow for entitlements and allocations, assuming that there are no changes to the event 
or the allocation process, follows this sequence: 
 
1. A CANO message announces a corporate actions event. 
2. This is followed by a CANO-E message on the [[DTCC]] Position Capture Date, which informs the client of 
its eligible balance related to the announcement. 
3. On Payable Date-7, a CAPA message is sent to the client. This contains the [[Entitlement]] amount that will 
be moved. 
4. On the [[DTCC]] Allocation Date, [[DTCC]] sends a CACO message confirming that the [[Entitlement]] has been 
moved. One CACO is sent per position type. CACO messages are only sent as NEWMs.  
Exception Flow 
The purpose of the following diagrams is to present different messages that can occur, such as an event being 
canceled, a payment cancellation, a payment change, an allocation reversal, etc. 
If there are any such changes to the announcement, then the message flow contains more stages.  
The three diagrams immediately following present this flow with variations. Boxes in green represent the usual 
message flow, and boxes in gray represent some variations that can occur. 


---

## Page 17

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 17 
 
 
Diagram 1 of 3 
1. A CANO message announces a corporate actions event. 
2. If the event is then canceled or withdrawn before [[DTCC]]’s Position Capture Date, a CACN cancellation 
message is sent. 
3. If the event has not been canceled or withdrawn, a CANO-E is sent to clients that are eligible for a 
distribution on the Position Capture Date. 
4. After Payable Date-7, [[DTCC]] sends a CAPA message to inform the client of the amount that will be 
moved. 
5. If the CAPA was sent in error, or if the event is canceled or withdrawn before the Allocation Date, a 
Preliminary Cancellation message (CAPC) is sent to the client. 
 
The process continues with the following diagram: 


---

## Page 18

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 18 
 
 
Diagram 2 of 3 
6. If the event was not canceled or withdrawn, or if the CAPA was not sent in error, then a CACO message is 
sent on the [[DTCC]] Allocation Date that confirms the movement of the [[Entitlement]] amount. One CAPA and 
one CACO are sent per position type ([[Stock]], cash, [[Stock]] loan, fail, or REPO).  
7. A reversal only occurs when a change takes place after the [[Entitlement]] has already been allocated (after 
the CACO has been sent on the [[DTCC]] Allocation Date) and it occurs on the same day that the funds are 
being allocated (i.e., Payment Date). In addition, a reversal only takes place on P&I events.  
A CANO replacement message is sent communicating the rate change. 
8. A CAPA message is sent containing the preadvice of this reversal. 
9. If a reversal is happening because of a rate change, a CARE message is sent to reverse the payment. 
The CARE message is only used when the rate change is on payment date and after the funds have been 
allocated. This is only applicable to P&I events. The reversal will always have to match exactly what is 
being reversed from the original CACO–if the original CACO was allocating [[shares]] using CRED, then the 
CARE message would be reversing the CRED. 
 
The process concludes with the following diagram: 


---

## Page 19

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 19 
 
 
 
Diagram 3 of 3 
10. If the payment occurs as specified on the new rate communicated via the CANO, [[DTCC]] sends a CACO 
message to confirm that the payment of the new [[Entitlement]] amount was made.  
11. If at any point in the process an allocation cannot occur on the payment date (or any date thereafter), 
[[DTCC]] sends an Event Status message (CAPS). This message contains supplementary data and reason 
codes to explain why the payment was not made. 
12. A CACO is sent after payable date for 2 reasons: 
a. The [[issuer]] did not allocate on payable date, and therefore no CACO was sent at that time, or  
b. A post-allocation adjustment was made and a CACO containing that adjustment amount is sent.  
Example of a Cash [[Dividend]]–[[BASIC]] Message Flow 
Corporation XYZ announced that its Board of Directors has declared an ordinary cash [[Dividend]] on its common 
[[Stock]] of $0.20 per share. The [[Dividend]] will be paid on August 8, 2014 to stockholders of record at the close of 
business on July 30, 2014. 


---

## Page 20

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 20 
 
 
 
1. A CANO message containing the details of the cash [[Dividend]] announcement is sent to clients.  
2. Stockholders on record as of close of business on July 30, 2014 are sent CANO-E messages that detail 
their entitlements. 
3. On [[settlement]] Date-7, CAPA messages are sent to the clients. They contain the [[Entitlement]] amount that 
will be moved. 
4. On August 8, 2014 (the [[DTCC]] Allocation Date), [[DTCC]] sends CACO messages to clients that confirm that 
their stated entitlements have been moved. 
Example of a Same-Day Reversal 
For Principal and Interest (P&I) events only, a same-day reversal is performed by executing a reversal for the 
full amount of the [[Entitlement]], then re-allocating the new amount. 
In this example, a CACO arrives on Wednesday morning for an event that carries a rate of $1.00. The 
[[Entitlement]] amount, $1000, has been delivered. 
Later that day, the rate is adjusted to $1.50. The client is then entitled to $1500, not $1000.  
The messages involved in this sequence are as follows: 


---

## Page 21

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 21 
 
 
1. The original CACO confirms that $1000 was paid out to the customer. 
2. A new CANO comes in, announcing the rate change. 
3. A CAPA comes in that states what will happen: the original payment of $1000 will be reversed. 
4. The CARE message is the confirmation of the reversal: $1000 has been debited.  
5. After the reversal has been performed, the new payment is made. A CACO message confirms that the 
payment of $1500 has been paid to the client. 
Example of a Post-Payable Allocation Adjustment 
For adjustments on allocations made after the payable date (such as funds that are received after payable date 
or additional funds allocated by the [[issuer]] or agent), the difference will be handled in a separate payment via a 
CACO message. A full reversal will not take place, but the change of [[Entitlement]] will be credited to or debited 
from the customer’s account. 
This is true for any item other than a same-day rate change on a P&I event. 
In this example, the same rate change is taking place as before: the original rate of $1.00 is changing to $1.50. 
However, instead of the rate change occurring intraday, the rate change is announced two days later.  
The messages involved in this sequence are as follows: 


---

## Page 22

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 22 
 
 
 
6. On Wednesday, the original CACO confirms that $1000 was paid out to the customer.  
7. On Friday, a new CANO comes in that announces the rate change. 
8. The CAPA announcing the anticipated credit balance of $500 would go out overnight  if [[DTCC]] received the 
adjustments during the start-of-day processing. 
If the adjustment came intraday, no CAPA is generated. 2 
In this example, no CAPA is sent. 
9. The new payment is made with the adjusted amount only. A CACO message confirms that the differe nce 
of $500 has been paid to the client. 
Late Announcements 
In most cases, the payable date occurs long after the record date–often by weeks or months. Sometimes, you 
will know the payable date well before that date arrives. 
Often, however, you will receive “late announcements.” This occurs when the announcement details (including 
rates and critical dates) are not made available to [[DTCC]] until the payable date.  
Whenever position is captured, a CANO-E will be sent. For late announcements, however, position is not 
always captured until the payable date. This happens when the rate is unknown: if no rate is captured, then no 
[[Entitlement]] can be calculated. If no [[Entitlement]] is calculated, a CAPA is not sent.  
The following scenarios present four examples of message flows for an event with a record date of August 7th 
and a payment date of October 1st. The key details of this event, including the payable date and rate, may not 
be known until October 1st, or may be known at any point in between the record date and the payable date.  
 
2 The only time a CAPA would be sent is when an adjustment is received during the overnight processing. 
The message sequence would then be CANO–CANO-E–CAPA–CACO–CAPA–CACO. 
If the adjustment comes in intraday, then no CAPA is sent for the adjustment.  


---

## Page 23

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 23 
 
Scenario 1: All Details Known 
In this case, all details are known on record date. This is not a late announcement.  
Scenario 2: Most Details Known 
Here, most of the details have been sent to [[DTCC]]. Since the rate is unknown, but all other details are known, 
[[DTCC]] will project a zero [[Entitlement]]. As soon as the rate is known prior to payable date, the projection will 
reflect the updated [[Entitlement]] in the CAPA message. 


---

## Page 24

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 24 
 
Scenario 3: Few Details Known 
In this scenario, the record date information has been sent to [[DTCC]], but the payable date and the rate have 
not. As the payable date is not known, a projection will not be sent: this is because the CAPA is sent on 
payable date minus 7, 6, 5, 4, 3, 2, and 1. 
Scenario 4: No Details Known 
In this case, all details are unknown until Payment Date. 
Message Subscriptions and Timing 
[[Entitlement]] and allocation messages will be sent to you based on your subscriptions. The timing for each is 
determined by your subscription options. 
The following tables describe message subscription options and their related times, as well as general 
processing times and holiday schedules. 


---

## Page 25

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 25 
 
Subscription Options 
Message Message Times Notes 
CANO-E • Daily 2:00 p.m. eastern time (P&I). 
Note: 
This is ONLY for late announcements created 
before 1:45PM on payable date. 
and/or 
• Daily 11:30 p.m. eastern time (P&I, MMI). 
1. Messages are available with or without 
Position Adjustment 
(Interim Accounting). 
2. Timing is the same for MQ or File delivery. 
3. A time stamp in the Business Application 
Header (BAH) allows you to verify message 
order. 
CAPA Two message creation options: 
• New messages sent on payable date minus 7 
days and REPL messages on payable date 
minus 1. 
or 
• New messages sent on payable date minus 7 
days and REPL (replacement/delta) messages 
sent each applicable day thereafter until 
payable date minus 1. 
Daily messages are sent at 1:30 a.m. eastern 
time (CAD, P&I, MMI, STKD). 
1. Daily processing is triggered at 1:00 a.m. 
and can run up until 2:00 a.m. eastern time. 
2. MQ messages can be received starting at 
about 1:02 a.m. and will end by 2:00 a.m. 
eastern time. 
3. Files (depending on volume) are usually 
delivered at about 1:30 a.m. eastern time. 
4. For [[Option]] 2, messages are sent only on 
days when a change has occurred. These 
messages are always REPL
 messages. 
CAPC Via file: 
• Daily, 1:30a.m. eastern time (CAD, P&I, MMI, 
STKD). 
Via MQ: 
• Real time, every half hour between 10:30 a.m. 
eastern time and 6:30 p.m. eastern time. 
• 1:30 a.m. eastern time for CAD, P&I, MMI, and 
STKD. 
1. A CAPC subscription will always require a 
CAPA subscription as well. 
2. Conversely, a CAPA subscription does not 
require CAPC subscription. However, if you 
subscribe to CAPA messages, it is 
suggested that you subscribe to CAPC 
messages. 
3. A time stamp in the Business Application 
Header (BAH) allows you to verify 
message order. 

---

## Page 26

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 26 
 
Message Message Times Notes 
CACO CARE 
(P&I only) 
Via file: 
• Daily 4:00 p.m. eastern time (P&I, MMI) 
and/or 
• Daily 7:00 p.m. eastern time (STKD*) 
and/or 
• 1:30 a.m. eastern time (STKD*). 
Via MQ: 
• Real time, every 20 minutes between 8:20 
a.m. and 4:30 p.m. eastern time (P&I, MMI). 
• Real time, 8:20 a.m. and 7:00 p.m. eastern 
time (STKD*). 
 
* CACO only. 
1. Each message will be sent per one 
[[participant]] account and will include: 
• total eligible balance, 
• [[Stock]] loans, 
• repurchase agreements (REPOs), and 
• failed deliveries (Fails). 
2. Post-allocation adjustments will be 
represented by additional CACO messages 
under the same CA [[ID]]. These only take 
place post-allocation, and reversals will only 
take place on payable date. 
3. In case of a rate change on payable date, a 
reversal on the initial change will be 
allowed. 
4. A time stamp in the Business 
Application Header (BAH) allows you to 
verify message order. 
CAPS • Daily 4:00 p.m. eastern time (CAD, MMI). 
• Daily 5:00 p.m. eastern time (P&I). 
• Daily 7:00 p.m. eastern time (STKD). 
Times are the same for file and MQ formats, 
except: 
• Real time [[Option]] for P&I, hourly between 1:00 
p.m. and 7:00 p.m. eastern time. 
1. The CAPS message is sent based on the 
CAPA that was previously sent. 
2. Reason codes are provided to explain why a 
given event was not allocated. 
3. A time stamp in the Business Application 
Header (BAH) allows you to verify 
message order. 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times specified 
below. Exceptions are noted in the holiday processing schedule. 
Message Monday–Friday Saturday and Sunday 
CANO-E Messages at 2:00 p.m. and 11:30 p.m. eastern time. 
2:00 p.m. message is ONLY for late announcements 
created before 1:45 p.m. on payable date. 
Files transmitted based on customer subscription. 
No messages or files transmitted. 
CAPA Messages between 1:00 a.m. and 2:00 a.m. eastern time. 
Files transmitted at 1:30 a.m. eastern time. 
No messages or files transmitted. 
CAPC Messages between 10:30 a.m. and 6:30 p.m. eastern 
time. 
Files transmitted at 1:30 a.m. eastern time. 
No messages or files transmitted. 

---

## Page 27

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 27 
 
Message Monday–Friday Saturday and Sunday 
CACO CARE Messages between 8:20 a.m. and 7:00 p.m. eastern time 
based on customer subscription. 
Files transmitted at 4:00 p.m., 7:00 p.m., and 1:30 a.m. 
eastern time, based on customer subscription. 
No messages or files transmitted. 
CAPS Messages between 1:00 p.m. and 7:00 p.m. eastern time 
based on customer subscription. 
Files transmitted at 4:00 p.m., 5:00 p.m. and 7:00 p.m. 
eastern time based on customer subscription. 
No messages or files transmitted. 
Holiday Processing Schedule 
Messages/Holidays U.S. and Canadian 
Holidays 
(both closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada 
closed) 
CANO-E No messages. No messages or files 
transmitted. 
Normal volumes. 
Files transmitted based on 
customer subscription. 
CAPA CAPC No messages. Normal volumes. 
Files transmitted based on 
customer subscription. 
Normal volumes. 
Files transmitted based on 
customer subscription. 
CACO CARE No messages. Only for Canadian payments. Normal volumes. 
Files transmitted based on 
customer subscription. 
CAPS No messages. 1:00 p.m., 2:00 p.m., and 3:00 
p.m. eastern time for P&I and 
Foreign payments. 
Normal volumes. 
Files transmitted based on 
customer subscription. 
For these holidays: • New Year's Day 
• Labor Day 
• Christmas Day 
• Dr. Martin Luther King, Jr. 
Day 
• Presidents' Day 
• Memorial Day 
• Juneteenth 
• Independence Day 
• Thanksgiving Day 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day 
• Boxing Day 
Note: 
In addition to this chart, please note that [[DTCC]] operates on two U.S. bank holidays: 
• Columbus Day ([[Stock]] allocation only; no cash allocation) 
• Veterans’ Day ([[Stock]] allocation only; no cash allocation) 

---

## Page 28

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 28 
 
 
What is a CANO-E Message? 
The Corporate Action Notification with Eligible Balance (CANO-E) captures a customer’s [[DTCC]] position on 
Record Date for a particular corporate action (announced in the original CANO). It determines whether a given 
customer is eligible to receive an allocation (of either cash, [[Stock]], or both) on that event. The CANO -E is also 
used to capture interim accounting activity between Record Date and Payable Date.  
The identifying information for a CANO-E message is: 
MX Identifier ISO 20022 
Message Name 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.031.002.xx3 CA Notification with 
Eligible Balance 
supl.007.001.xx3 CANO-E MT 564 Record Date 
Entitlements 
 
The CANO-E message is created on a daily basis for items for which the record date has been reached and 
position capture has occurred. The message will be created once per event, unless there is interim accounting 
 
3 The last two digits in the MX Identifier and the Extension code signify th e version number. The MX version number and/or the Supplementary version number 
may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards and [[DTCC]].com. 


---

## Page 29

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 29 
 
activity taking place between Record and Payable Date. If such activity occurs and the customer is subscribed 
to receive such notifications, a CANO-E REPL will be sent. 
If a CANO message is not produced before record date, a CANO-E message will not be produced for the 
event. Fails [[DO]] not appear on the CANO-E. 
Some main characteristics of the CANO-E are: 
• General details about the event (including the CA [[ID]] and the COAF) replace the full CANO message. By 
using these identifiers, the body of the CANO message is not repeated in the CANO -E. 
• The Eligible Balance Indicator is set to “Y,” meaning that the customer has a balance affected by this 
corporate action. The CANO-E is a notification of this balance. 
 
Corresponding legacy [[CCF]] files for the record date statement are: 
• DIVRDP, 
• REORDP, and 
• MMIRDP. 
 
[[Stock]] Loan and Repo Record Date Position will be part of the Record Date Position message with a repeating 
block of supplemental data for each of the contra participants associated with the transaction. The net total for 
each balance type will be in the balance section and the transaction activity (with contra party details for each 
[[Stock]] loan, repo, or fail) will be in the message extension. 
The message extension includes: 
• Transaction Type–Long or Short, 
• Transaction [[shares]], and 
• Contra [[participant]] Number. 
When Are CANO-E Messages Generated? 
A CANO with eligible balance message (CANO-E) will be generated on Position Capture Date, which is 
generally Record Date or any other date on which interim accounting activity is taking place. The position 
capture date can be found on the CANO. If there is both a market record date and a New York record date, the 
message will only be generated once (for the earlier record date). 
They are generated in two instances: 
• Position capture, which can occur on various critical dates. 
• Position adjustments, also known as “interim accounting activity.” 
 
The first CANO-E received by a [[participant]] will always be a NEWM: this is the ISO notification type signifying a 
new message. All subsequent CANO-Es are REPLs, or replacement messages. 
Items can get captured for interim-only activity without having had position on record date, in which case a 
NEWM is generated. 

---

## Page 30

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 30 
 
Intraday Position Capture 
Intraday Position Capture processes late announcements that are due to be paid today.  
ISO messages are generated for intraday position capture processing. These include only Cash Principal and 
Interest items, along with [[Stock]] Loans and Repos that are due to be paid today.  
Foreign items that are EDS-eligible and MMI payments will not be included in the intraday CANO-E message 
process. 
Message Timing 
The subscription options allow customers to receive the CANO-E messages once or twice daily on regular 
business processing days: 
• Daily 2:00 p.m. eastern time (P&I) 
and/or 
• Daily 11:30 p.m. eastern time (P&I, MMI) 
Note: 
The CANO-E subscription at 2:00 p.m. is ONLY for late announcements created before 1:45 p.m. on payable date. 
The messages are available with or without position adjustment (Interim Accounting).  
The timing of the messages is the same for both MQ and File formats. 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times specified 
below. Exceptions are noted in the holiday processing schedule. 
Message Monday–Friday Saturday and Sunday 
CANO-E Messages at 2:00 p.m. and 11:30 p.m. eastern time. 
2:00 p.m. message is ONLY for late announcements 
created before 1:45 p.m. on payable date. 
Files transmitted based on customer subscription. 
No messages or files transmitted. 

---

## Page 31

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 31 
 
Holiday Processing Schedule 
U.S. and Canadian Holidays (both 
closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada closed) 
No messages or files are sent on: 
• New Year's Day 
• Labor Day, and 
• Christmas Day. 
No messages or files are sent on: 
• Dr. Martin Luther King, Jr. Day 
• Presidents' Day 
• Memorial Day 
• Juneteenth 
• Independence Day, and 
• Thanksgiving Day. 
Normal volumes occur on these days: 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day, and 
• Boxing Day. 
Files are transmitted based on 
customer subscription. 
 
Note: 
In addition to this chart, please note that [[DTCC]] operates on two U.S. bank holidays: 
• Columbus Day ([[Stock]] allocation only; no cash allocation) 
• Veterans’ Day ([[Stock]] allocation only; no cash allocation) 
Information Contained on the CANO-E Message 
Mapping for the message layout will conform to the ISO message rules. When applicable, supplemental data 
will be included with sub balances for [[Stock]] Loan and Repo transaction information.  
For more detailed technical information and source material for client coding, please refer to the message 
usage guidelines (MUGs) and message schemas located at http://www.[[DTCC]].com/[[settlement]]- and-[[Asset]]-
services/corporate-actions-processing/iso-20022-messaging-specifications. 
ISO Message Field Name [[DTCC]] Field Name/Notes 
NotificationType Notification Type 
Specifies the type of message: new message (NEWM) or replacement 
message (REPL). 
EventCompletenessStatus Event Status 
Workflow status of the event, based on the statuses of options, payouts, 
lottery, etc. 
EventConfirmationStatus Event Status 
Workflow status of the event; defaults to “CONF.” 
EligibleBalanceIndicator Eligible Balance Indicator 
This indicator differentiates this message from the original CANO: when it is 
set to “True,” this message is identified as an “Eligible Balance” message 
(containing account and balances) only. 

---

## Page 32

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 32 
 
ISO Message Field Name [[DTCC]] Field Name/Notes 
 It carries the current eligible balance, which can contain a position captured 
on position capture date as well as possibly a [[Stock]] loan balance, a REPO 
balance, or a Fail balance. 
PreviousNotificationIdentification Previous Message [[ID]] 
This is the identification of a previously sent notification document. It is 
mandatory when the notification type is “REPL.” 
CorporateActionEventIdentification CA [[ID]] 
This is the [[DTC]]-unique identifier of the event. 
OfficialCorporateActionEvent 
Identification 
Official Reference CA [[ID]] 
This is the official corporate action unique identifier. 
EventType Event Type 
MandatoryVoluntaryEventType This specifies the nature of the event: 
• [[DTC]] Mandatory/Voluntary 
• Declared Mandatory/Voluntary 
UnderlyingSecurity Security identification code of the event issue: 
• Event Security [[ID]] 
• Event Security Type 
• Event Security Description 
SafekeepingAccount [[participant]] Number 
This is the [[DTC]]-assigned [[participant]] identification number for the 
safekeeping account. 
TotalEligibleBalance Total Eligible Balance 
This represents the current eligible balance for elections and allocations. It is 
the total net position as of the day the message is sent. 
• For long positions, map to “Long” 
• For short positions, map to “Short” 
• For non-debt security, map to “Unit” 
• For debt security, map to “Face Amount.” 
BorrowedBalance Borrowed Balance (Total [[Stock]] Loan Short) 
This represents the negative net balance of the [[Stock]] loans. 
• For non-debt [[securities]], use “Unit.” 
• For debt [[securities]], use “Face Amount.” 
“Long” is the [[default]] value for Qty choice. 
CollateralInBalance [[collateral]] In Balance (Total REPO Long) 
This represents the positive net balance of the repurchase agreements. 
• For non-debt [[securities]], use “Unit.” 
• For debt [[securities]], use “Face Amount.” 
“Long” is the [[default]] value for Qty choice. 

---

## Page 33

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 33 
 
ISO Message Field Name [[DTCC]] Field Name/Notes 
CollateralOutBalance [[collateral]] Out of Balance (Total REPO Short Distributions); Pledged Balance 
(Redemptions) 
This represents the negative net balance of the repurchase agreements. 
• For non-debt [[securities]], use “Unit.” 
• For debt [[securities]], use “Face Amount.” 
“Long” is the [[default]] value for Qty choice. 
OnLoanBalance On Loan Balance (Total [[Stock]] Loan Long) 
This represents the positive net balance of the [[Stock]] loans. 
• For non-debt [[securities]], use “Unit.” 
• For debt [[securities]], use “Face Amount.” 
“Long” is the [[default]] value for Qty choice. 
PendingDeliveryBalance Pending Delivery Balance (Total Fails Short) 
This represents the negative net balance of the fail trades. 
• For non-debt [[securities]], use “Unit.” 
• For debt [[securities]], use “Face Amount.” 
“Long” is the [[default]] value for Qty choice. 
PendingReceiptBalance Pending Receipt Balance (Total Fail Long) 
This represents the positive net balance of the fail trades. 
• For non-debt [[securities]], use “Unit.” 
• For debt [[securities]], use “Face Amount.” 
“Long” is the [[default]] value for Qty choice. 
SettlementPositionBalance [[settlement]] Position Balance 
This represents the current eligible balance for elections and allocations. 
• For non-debt [[securities]], use “Unit.” 
• For debt [[securities]], use “Face Amount.” 
Quantity choice is “LONG” for positive balances and “SHORT” for negative 
balances. 
Supplementary Data 
Extended data. This is the breakdown of sub balances (adjustments) 
Transaction Details–header 
Start of the block. The entire section repeats for each transaction 
StockLoan [[Stock]] Loan Transaction 
This is the [[Stock]] loan transaction position. The [[Stock]] is loaned to/borrowed 
from a third party. It is mutually exclusive with REPO transactions. 
Quantity choice is “LONG” for positive balances and “SHORT” for negative 
balances. 

---

## Page 34

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 34 
 
ISO Message Field Name [[DTCC]] Field Name/Notes 
Repo REPO Transaction 
This indicates a repurchase agreement between a [[Seller]] and a [[Buyer]] 
whereby the [[Seller]] agrees to repurchase the [[securities]] at an agreed-upon 
price and (usually) at a stated time. 
REPOs are mutually exclusive with [[Stock]] loans and fails. 
Quantity choice is “LONG” for positive balances and “SHORT” for negative 
balances. 
ContraParticipantNumber Contra [[participant]] Number 
This is the transaction contra [[participant]] identification for [[Stock]] loans, 
REPOs, and fails. 
Examples and Scenarios for CANO-E Messages 
CANO-E for Position Adjustments 
Position adjustments (commonly known as “interim accounting”) refer to any changes of eligible bala nce 
between Record Date and Payable Date. 
Position adjustments occur for any of these events: 
1. [[participant]] swings, 
2. Internal position adjustments, or 
3. Interim accounting. 
 
[[participant]] Swings 
Client position can be swung from one client to another. It affects the [[participant]]’s overall record date balance 
and a CANO-E REPL will be sent (unless a CANO-E NEWM was not previously generated). Examples A and B 
illustrate client swings. 
In Example A, the record date is 12/01/2010. A client’s eligible balance swings over time: 
Activity Date Position Activity 
12/01/2010 16,509 Record Position 
03/05/2012 33,772 Swingover from 0123 
03/05/2012 1,600 Swingover from 0123 
04/23/2013 7,960 Swingover from 0000 
 

---

## Page 35

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 35 
 
12/01/2010 Generate CANO-E (NEWM) Total Eligible Balance of 16,509 
03/05/2012 Generate CANO-E (REPL) Total Eligible Balance of 51,881 
04/23/2013 Generate CANO-E (REPL) Total Eligible Balance of 59,841 
In Example B, the record date is 09/30/2011. The record date capture and swing happen on the same day:  
Activity Date Position Activity 
07/26/2013 5,050,000 Record Position (L) 
07/26/2013 -5,050,000 Swingover to 0000 
 
In this case, a CANO-E message will not be generated: record date position was captured and was swung to 
another client on the same day, leaving an eligible balance of zero. 
Manual Position Adjustments 
Manual position adjustments occur either when adjustments are entered by [[DTCC]] staff or when interim 
monitoring is performed by [[DTCC]]. Examples C and D will focus on manual position adjustments.  
In Example C, the record date is 11/24/2010. There is an adjustment with no record date position:  
Activity Date Position Activity 
07/23/2013 1,765,000 Record Date position adjustment 
 
07/23/2013 Generate CANO-E (NEWM)-Total Eligible Balance of 1,765,000 
In Example D, the record date is 07/19/2013. There is an adjustment to a record date position:  
Activity Date Position Activity 
07/17/2013 3,398,424 Record Position (L) 
07/18/2013 -3,398,424 Treasury buy-back 
 
07/17/2013 Generate CANO-E (NEWM) Total Eligible Balance of 3,398,424 
07/18/2013 Generate CANO-E (REPL) Total Eligible Balance of 0 
Interim Accounting 
Position can be adjusted by [[DTCC]] based on client activity (for example, a Deliver Order {[[DO]]}).  
Example E focuses on interim accounting. The record date for this example is 07/05/2013:  

---

## Page 36

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 36 
 
Activity Date Position Activity 
07/05/2013 26,675,000 Record Position 
07/08/2013 420,000 Interim 
([[DTC]] Activity: [[DO]] {Receive}) 
07/15/2013 650,000 Interim 
([[DTC]] Activity: [[DO]] {Receive}) 
 
07/05/2013 Generate CANO-E (NEWM) Total Eligible Balance of 26,725,000 
07/08/2013 Generate CANO-E (REPL) Total Eligible Balance of 27,145,000 
07/15/2013 Generate CANO-E (REPL) Total Eligible Balance of 27,795,000 
Note: 
In this case, a CAPA NEWM is sent out on 07/11/2013, and a CAPA REPL is sent out on 07/15/2013 along with the CANO- 
E REPL. 
Other Cases 
It is possible to have a case in which the record date position is captured, but due to [[Stock]] loan or repo activity, 
the resulting position is zero. 
In Example F, the record date is 08/07/2013. The record date position is captured for [[Stock]] Loan/Repos:  
Activity Date Position Activity 
08/07/2013 5,700,000 Record Position 
08/07/2013 -5,700,000 Record Date Position–REPO ([[DTC]] Activity: 
REPO) 
 
08/07/2013 Generate CANO-E (NEWM) Total Eligible Balance of 0 
  [[collateral]] Out Balance of 5,700,000 
  [[settlement]] Position Balance of 5,700,000 
CANO-E for Market Record Date or New York Record Date 
The CANO-E will be generated when position is captured, on the position capture date as determined on the 
announcement. If there is both a market record date and a New York record date, the message will only be 
generated once for the earlier date. 

---

## Page 37

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 37 
 
Standard CANO-E Processing 
As long as the customer is not subscribed to receive interim position adjustments, CANO -E messages will be 
generated once and all messages will be designated as NEWM. These messages are created when position is 
captured. 
In Example G, the record date is 7/28/2013: 
Activity Date Position Activity 
07/26/2013 74,626 Record Position 
 
Position is captured on New York record date which is 2 days prior to market record date. The CANO -E 
message is generated on 7/26/2013. 
In Example H, the record date is 07/23/2013: 
Activity Date Position Activity 
07/23/2013 4,211 Record Position 
07/26/2013 -70,100 Record Position–[[Stock]] Loan ([[DTC]] Activity–SLN) 
 
Position is captured on market record date. The CANO-E message is generated on 07/23/2013 for a Total 
Eligible Balance of -65,889. 
Announcement Deleted; CA [[ID]] Remains in CA Web 
If a CANO-E message was already created for an event and there is no change in position with the “new” 
announcement, a CANO-E will not be generated. 

---

## Page 38

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 38 
 
 
What is a CAPA Message? 
The Corporate Action Movement Preliminary Advice (CAPA) message projects payments and allocations on a 
corporate action event according to a client’s eligibility as communicated in the CANO-E message. Projections 
occur on payable date minus 7 up until payable date minus 1, depending upon your subscription.  
The identifying information for a CAPA message is: 
MX Identifier ISO 20022 
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.035.002.xx4 CA Movement 
Preliminary Advice 
supl.009.001.xx4 CAPA MT 564 Projected Payments 
 
 
4 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version number 
may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards and [[DTCC]].com. 


---

## Page 39

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 39 
 
The notification types for preliminary advice messages include NEWM (New Messages) and REPL 
(Replacement Messages). NEWM messages are sent on payable date minus 7; any subsequent messages for 
that same COAF will be a REPL message. 
If there is a change to the [[Entitlement]], a replacement (REPL) message will be generated for the [[participant]] for 
the event. 
A REPL CAPA message is generated if one or more of the following pieces of information has changed:  
• [[settlement]] Position Balance, 
• Borrowed Balance, 
• On Loan Balance, 
• [[collateral]] In Balance, 
• [[collateral]] Out Balance, and/or 
• Pending Delivery Balance. 
 
Individual CAPA messages will be created for [[Stock]] Loan, REPO, and Fail adjustments. All other types of 
adjustments for an individual event will be consolidated into one CAPA message (with a type of “MISC”). The 
aggregate total calculated within the individual transaction is listed in the extension portion of the message.  
For [[Stock]] Loans, REPOs, and Fails, the CAPA is sent on payable date minus 5 only when:  
• The number of days between record date (position capture) and payable date is greater t han 5, and 
• The event is not a late announcement. 
 
Legacy [[CCF]] files for projections include: 
• CSHPRJ, 
• STKPND, 
• CSHFGP, 
• CSHDPJ, and 
• CSHRPJ. 
CAPA Message Creation and Timing 
What are the CAPA Subscription Options? 
CAPA messages are generated on each business day based on a client’s subscription rules. Messages will be 
sent per balance type per [[participant]]. 
There are two message creation options: 

---

## Page 40

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 40 
 
Subscription [[Option]] When Generated 
Subscription 1 Payable date (PD)-7 days  
Payable Date (PD)-1 day 
Subscription 2 PD-7  
PD-6  
PD-5  
PD-4  
PD-3  
PD-2 
PD-1 
 
• Subscription [[Option]] 1. New messages (NEWM) are sent on payable date minus 7 days and replacement 
messages (REPL) are sent on payable date minus 1 day. 
(The final CAPA is actually generated in the early morning of pay date.) 
or 
• Subscription [[Option]] 2. New messages are sent on payable date minus 7 days. REPL 
(replacement/delta) messages are sent, if applicable, each day thereafter until payable date minus 1 day. 
(The final CAPA is actually generated in the early morning of pay date.) 
 
When are CAPA NEWM/REPL Messages Sent? 
You will receive a CAPA NEWM for each payout. Separate CAPA NEWMs are sent for each balance type.  
You will receive separate CAPA REPL messages for each balance type as well, according to your subscription.  
If you subscribe to the second [[Option]] that sends messages between Payable Date (PD) -7 and PD-1, you will 
only receive REPL messages on the days in between (PD-6 through PD-2, inclusive) if there is a position or 
[[Entitlement]] change between PD-7 and PD-1. If there are no changes, you will receive the messages only on 
PD-7 and PD-1. 
Note: 
The PD-1 CAPA messages represent processing from Payable Date minus 1 day, but the messages are not sent until 1:00 
a.m. on Payable Date. 
In the following example, a client has [[settlement]] position, on-loan, and pending delivery balances in a 
particular corporate action. 
This first table represents changes in balance that have occurred for this client on this corporate action 
between Payable Date -7 days and Payable Date-1 day: 

---

## Page 41

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 41 
 
Change in Balance for: PD-7 PD-6 PD-5 PD-4 PD-3 PD-2 PD-1 
[[settlement]] Position  yes      
On-Loan   yes  yes   
Pending Delivery      yes  
 
Clients with Subscription [[Option]] 1 would receive CAPA messages according to this calendar:  
SUN MON TUE WED THU FRI SAT 
   12/24 
PD-7 
NEWM 
NEWM 
NEWM 
12/25 
Holiday: no 
processing 
12/26 
PD-6 
12/27 
Weekend: no 
processing 
12/28 
Weekend: no 
processing 
12/29 
PD-5 
12/30 
PD-4 
12/31 
PD-3 
1/1 
Holiday: no 
processing 
1/2 
PD-2 
1/3 
Weekend: no 
processing 
1/4 
Weekend: no 
processing 
1/5 
PD-1* 
REPL 
REPL 
REPL 
1/6 
PAYABLE 
DATE 
    
 
*Information processed from PD-1. Report is actually received at approximately 1:00 a.m. eastern time on PD.  
  

---

## Page 42

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 42 
 
Clients with Subscription [[Option]] 2 would receive CAPA messages according to this calendar:  
SUN MON TUE WED THU FRI SAT 
   12/24 
PD-7 
NEWM 
NEWM 
NEWM 
12/25 
Holiday: no 
processing 
12/26 
PD-6 
REPL 
12/27 
Weekend: no 
processing 
12/28 
Weekend: no 
processing 
12/29 
PD-5 
REPL 
12/30 
PD-4 
12/31 
PD-3 
REPL 
1/1 
Holiday: no 
processing 
1/2 
PD-2 
REPL 
1/3 
Weekend: no 
processing 
1/4 
Weekend: no 
processing 
1/5 
PD-1* 
REPL 
REPL 
REPL 
1/6 
PAYABLE 
DATE 
    
 
*Information processed from PD-1. Report is actually received at approximately 1:00 a.m. eastern time on PD.  
CAPA and CAPC Messages 
There are separate subscriptions for CAPA and CAPC. 
Clients must subscribe to CAPC separately. However, a CAPC subscription will always require a CAPA 
subscription (to subscription [[Option]] 1, [[Option]] 2, or both). 
If you subscribe to CAPA messages, it is recommended that you subscribe to CAPC messages. 
Messaging Notes 
1. Daily processing is triggered at 1:00 a.m. and can run up until 2:00 a.m. eastern time.  
2. MQ messages can be received starting at about 1:02 a.m. and will end by 2:00 a.m. eastern time.  
3. Files (depending on volume) are usually delivered at about 1:30 a.m. eastern time.  
Intraday Position Capture 
There will be no CAPA messages generated for intraday position capture. Any items not allocated will be 
accounted for in a CAPS (Corporate Action Event Processing Status Advice) message on the same day. A 
CAPA will also be sent out the next morning in the 1:00 a.m.–1:30 a.m. cycle. 

---

## Page 43

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 43 
 
CAPA Messages and Reversals 
When a reversal occurs, the CAPA (NEWM) generated should be a “pre-advice” message for the reversal. The 
Movement Confirmation [[ID]] from the original CACO will be included in the message as well as the debit of the 
original CACO amount. 
Messages and Zero Amounts 
Projection amounts of zero are possible in the CAPA messages. This may occur in several cases, including:  
1. Events that have a rate of “0” prior to the payable date. 
You can see an example of this in the second scenario for Late Announcements , in which some of the 
corporate actions details are known but the rate is not. 
2. Any [[Stock]] Loan, REPO, and/or Fail activity in which the trade is still pending. 
Late Announcements 
A CAPA message will be produced when all details (rate, payable date, eligible holder, and total eli gible 
balance) are known on the record date. However, some or all of the details are often not known until payable 
date. 
• If the rate is zero prior to payable date but the payable date itself is known, a CAPA will be sent with a rate 
of “0” and a “0” projected [[Entitlement]]. 
• If the payable date is unknown, a CAPA will not be sent. This is because the CAPA message is sent on 
payable date minus 7, 6, 5, 4, 3, 2, and 1. 
 
Please see the Late Announcements section for more information. 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times specified 
below. Exceptions are noted in the holiday processing schedule. 
Message Monday–Friday Saturday and Sunday 
CAPA Messages between 1:00 a.m. and 2:00 a.m. eastern time. 
Files transmitted at 1:30 a.m. eastern time. 
No messages or files transmitted. 
Holiday Processing Schedule 
The CAPA is generated in normal volumes for all U.S. and Canadian holidays except: 
• New Year’s Day, 
• Labor Day, and 
• Christmas Day. 

---

## Page 44

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 44 
 
Information Contained on the CAPA Message 
Mapping for the message layout will conform to the ISO message rules. When applicable, supplemental data 
will be included with sub balances for [[Stock]] Loan and Repo transaction information.  
[[Stock]] loan, REPO, and Fail balances can be found in the core section of the CAPA message. Contra party 
balances can be found in the message extension. 
For more detailed technical information and source material for client coding, please refer to the message 
usage guidelines (MUGs) and message schemas located at http://www.[[DTCC]].com/[[settlement]]- and-[[Asset]]-
services/corporate-actions-processing/iso-20022-messaging-specifications. 
ISO Message Field Name [[DTCC]] Field Name/Notes 
NotificationType Specifies the type of message: new message (NEWM) or replacement 
message (REPL). The first message is always NEWM; all subsequent 
messages are REPL. 
PreviousMovement 
PreliminaryAdvice 
Identification 
When an update (REPL) is being sent, this is the message [[ID]] of the 
previously sent CAPA. 
MovementConfirmation 
Identification 
When a movement confirmation (CACO) is being reversed, this is the 
CACO’s message [[ID]]. 
ReversalReason This is the reason for the reversal, used when the CAPA is sent as a 
reversal preadvice. The ISO code “IPRI” is used as a [[default]]. 
CorporateActionEvent Identification CA [[ID]] 
This is the [[DTC]]-unique identifier of the event. 
OfficialCorporateAction 
EventIdentification 
Official Reference CA [[ID]] 
This is the official corporate action unique identifier. 
EventType Event Type 
MandatoryVoluntaryEventType This specifies the nature of the event: 
[[DTC]] Mandatory/Voluntary 
Declared Mandatory/Voluntary 
UnderlyingSecurity Security identification code of the event issue: 
• Event Security [[ID]] 
• Event Security Type 
• Event Security Description 
SafekeepingAccount [[participant]] Number 
This is the [[DTC]]-assigned [[participant]] identification number for the 
safekeeping account. 

---

## Page 45

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 45 
 
ISO Message Field Name [[DTCC]] Field Name/Notes 
BorrowedBalance Borrowed Balance (Total [[Stock]] Loan Short) 
This represents the negative net balance of the [[Stock]] loans. 
Note: 
Separate CAPAs are sent for each balance type. Therefore, only one balance 
type (of the seven in this table) is used per CAPA message. 
OnLoanBalance On Loan Balance (Total [[Stock]] Loan Long) 
This represents the positive net balance of the [[Stock]] loans. 
Note: 
Separate CAPAs are sent for each balance type. Therefore, only one balance 
type (of the seven in this table) is used per CAPA message. 
CollateralInBalance [[collateral]] In Balance (Total REPO Long) 
This represents the positive net balance of the repurchase agreements. 
Note: 
Separate CAPAs are sent for each balance type. Therefore, only one balance 
type (of the seven in this table) is used per CAPA message. 
CollateralOutBalance [[collateral]] Out of Balance (Total REPO Short); 
Pledged Balance (Redemptions) 
This represents the negative net balance of the repurchase agreements. 
Note: 
Separate CAPAs are sent for each balance type. Therefore, only one balance 
type (of the seven in this table) is used per CAPA message. 
PendingDeliveryBalance Pending Delivery Balance (Total Fails Short) 
This represents the negative net balance of the fail trades. 
Note: 
Separate CAPAs are sent for each balance type. Therefore, only one balance 
type (of the seven in this table) is used per CAPA message. 
PendingReceiptBalance Pending Receipt Balance (Total Fail Long) 
This represents the positive net balance of the fail trades. 
Note: 
Separate CAPAs are sent for each balance type. Therefore, only one balance 
type (of the seven in this table) is used per CAPA message. 

---

## Page 46

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 46 
 
ISO Message Field Name [[DTCC]] Field Name/Notes 
SettlementPositionBalance [[settlement]] Position Balance 
This represents the current eligible balance for elections and allocations. 
Note: 
Separate CAPAs are sent for each balance type. Therefore, only one balance 
type (of the seven in this table) is used per CAPA message. 
RecordDate The record date of the corporate action. Beneficial owners on this date will 
receive the relevant amount of [[Entitlement]] due for distribution on payment 
date. 
ExDividendDate “Ex Date.” The as-of date from which trading occurs on the underlying 
security without the benefit. 
CorporateActionMovementDetails–header 
OptionNumber The number that uniquely identifies an [[Option]] within an event. 
OptionType Describes the type of [[Option]] associated with the event. 
CurrencyOption Currency election (sub event type). The currency in which the cash 
disbursed from an interest or [[Dividend]] payment is offered. 
DefaultOptionIndicator Identifies whether the [[Option]] is processed as a [[default]] [[Option]] by [[DTCC]]. 
SecuritiesMovementDetails–header 
SecurityIdentification The [[DTC]] Disbursed Security and Type. This provides a description of the 
financial instrument related to the [[securities]] movement. 
CreditDebitIndicator Indicates whether the operation is an increase (CRED) or a decrease 
(DEBT). When this message is sent as preadvice of a CACO, this code is 
the opposite value of this field in the CACO message. 
EntitledQuantity [[securities]] Quantity. 
The quantity of [[securities]] to be debited or credited. 
PaymentDate Declared Payable Date. 
The [[issuer]]-announced Payment Date. 
EarliestPaymentDate [[DTC]] Anticipated Payment Date. 
The date on which [[DTC]] expects the payment to allocate. 
CashInLieuOfSharePrice [[DTC]] Cash In Lieu Price. 
Cash disbursement in lieu of equities, usually in lieu of fractional quantity. 
CashMovementDetails–header 
CreditDebitIndicator Indicates whether the operation is an increase (CRED) or a decrease 
(DEBT). When this message is sent as preadvice of a CACO, this code is 
the opposite value of this field in the CACO message. 
NetCashAmount Cash Amount (Payout: [[Dividend]]) 
Amount of money after deductions and allowances have been made; the 
total amount plus or minus any applicable charges and/or fees. 

---

## Page 47

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 47 
 
ISO Message Field Name [[DTCC]] Field Name/Notes 
CapitalGain • Cash Amount (Payout: Capital Gains) 
• Cash Amount (Payout: Short Term Capital Gains) 
• Cash Amount (Payout: Long Term Capital Gains) 
• Cash Amount (Payout: Return of Capital) 
The amount of money distributed as the result of a capital gain. 
PaymentDate Declared Payable Date. 
The payable date as announced by the [[issuer]] or offeror. 
EarliestPaymentDate [[DTC]] Anticipated Payable Date. 
The date on which [[DTC]] anticipates receiving funds/[[securities]] and will make 
a distribution. 
Supplementary Data 
SecuritiesMovementDetails (extended)–header 
Start of the block. The entire section repeats for each transaction 
Debit/Credit Indicates whether the operation is an increase (CRED) or a decrease 
(DEBT). 
TransactionQuantity Transaction [[securities]] Quantity 
The resulting quantity of [[securities]] concerned in the transaction. 
• For non-debt [[securities]], use “Unit.” 
• For debt [[securities]], use “Face Amount.” 
ReasonCode Transaction reason. 
See the Reason Code section in Appendix A for more information. 
SubReasonCode Sub Reason Code. 
See the Sub Reason Code section in Appendix A for more information. 
ContraParticipantNumber Contra [[participant]] Number. 
This is the [[DTCC]] [[participant]] [[ID]] for the contra party involved when [[shares]] 
are distributed/delivered to/from another [[participant]]. It is used for fails, 
REPOs, and [[Stock]] loans. 
EarliestPaymentDate Payable Date. 
The date/time on which the posting/draft of the [[securities]] is scheduled to 
take place for a transaction. 
TaxAdjustmentRate Sub Reason Code. 
The set of the [[DTC]] legacy sub reason codes representing the tax rate. Used 
with the following reason codes to identify the correct tax rate: 
• TJXD 
• TJXF 
• TJXI 
• TJXL 
• TJXR 
• TJXT 
• TJXU 
• TJXV 

---

## Page 48

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 48 
 
ISO Message Field Name [[DTCC]] Field Name/Notes 
• TJXO 
CashMovementDetails (extended)–header 
Debit/Credit Indicates whether the operation is an increase (CRED) or a decrease 
(DEBT). 
TransactionAmount Transaction cash amount. 
This is the resulting cash amount concerned in this transaction. 
ReasonCode Transaction reason. 
See the Reason Code section in Appendix A for more information. 
SubReasonCode Sub Reason Code. 
See the Sub Reason Code section in Appendix A for more information. 
ContraParticipantNumber Contra [[participant]] Number. 
This is the [[DTCC]] [[participant]] [[ID]] for the contra party involved when [[shares]] 
are distributed/delivered to/from another [[participant]]. It is used for fails, 
REPOs, and [[Stock]] loans. 
EarliestPaymentDate Payable Date. 
The date/time on which the posting/draft of the [[securities]] is scheduled to 
take place for a transaction. 
TaxAdjustmentRate Sub Reason Code. 
The set of the [[DTC]] legacy sub reason codes representing the tax rate. Used 
with the following reason codes to identify the correct tax rate: 
• TJXD 
• TJXF 
• TJXI 
• TJXL 
• TJXR 
• TJXT 
• TJXU 
• TJXV 
• TJXO 
 
CAPA Message Data 
CAPA messages are made up of the following building blocks: 

---

## Page 49

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 49 
 
Message Building Block Definition/Information 
Pagination Page number of the message and continuation indicator to indicate that the 
multi-part preliminary advice is to continue or that the message is the last 
page of the multi-parts preliminary advice. 
MovementPreliminaryAdviceGeneralIn 
formation 
General information about the movement preliminary advice document. 
PreviousMovement  
PreliminaryAdvice 
Identification 
Identification of a previously sent movement preliminary advice document. 
NotificationIdentification Identification of a previously sent notification document. 
MovementConfirmationIdentification Identification of a previously sent movement confirmation document. 
InstructionIdentification Identification of a related instruction document. 
OtherDocumentIdentification Identification of other documents as well as the document number. 
EventsLinkage Identification of another corporate action event that needs to be closely 
linked to the processing of the event notified in this document. 
ReversalReason Reason for the reversal. 
CorporateActionGeneralInformation General information about the corporate action event. 
AccountDetails General information about the safekeeping account, owner and account 
balance. 
CorporateActionMovementDetails Information about the corporate action [[Option]]. 
AdditionalInformation Provides additional information. 
IssuerAgent Party appointed to administer the event on behalf of the [[issuer]] 
company/offeror. The party may be contacted for more information about the 
event. 
PayingAgent Agent (principal or fiscal paying agent) appointed to execute the payment for 
the corporate action event on behalf of the [[issuer]] company/offeror. 
SubPayingAgent Sub-agent appointed to execute the payment for the corporate action event 
on behalf of the [[issuer]] company/offeror. 
Registrar Party/agent responsible for maintaining the register of a security. 
ResellingAgent A [[Broker]]-dealer responsible for reselling to new investors [[securities]] (usually 
[[Bonds]]) that have been tendered for purchase by their owner. 
PhysicalSecuritiesAgent A trust company, bank or similar financial institution assigned by an [[issuer]] to 
accept presentations of instruments, usually [[Bonds]], for transfer and or 
exchange. 
DropAgent A trust company, bank or similar financial institution who acts on behalf of an 
out of town agent or event agent where [[securities]] can be delivered in 
person. 
SolicitationAgent A trust company, bank or similar financial institution assigned by an [[issuer]] to 
maintain records of investors and account balances and transactions for the 
consent of a material change. 

---

## Page 50

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 50 
 
Message Building Block Definition/Information 
InformationAgent A trust company, bank or similar financial institution assigned by an [[issuer]] to 
provide information and copies of the offering documentation. 
SupplementaryData Additional information that cannot be captured in the structured fields and/or 
any other specific block. 
 
Complete mapping and technical information is available in the Message Usage Guidelines (MUG) for CAPA 
messages. In this document, you can also find: 
• message functionality, 
• restriction summary, 
• message structure, 
• message rules, 
• message components, 
• message datatypes, and 
• usage restriction guidelines. 
 
Please consult this guide in order to complete your technical mapping. 
 


---

## Page 51

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 51 
 
What is a CAPC Message? 
A Corporate Action Movement Preliminary Advice Cancellation Advice (CAPC) message is sent when a 
payment is no longer expected to be made (due to an announcement being canceled) and a CAPA message 
has already been sent. This message effectively cancels a CAPA. 
The identifying information for a CAPC message is: 
MX Identifier ISO 20022 
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.044.002.xx5 CA Movement 
Preliminary Advice 
Cancellation Advice 
n/a CAPC MT 564 New 
 
CAPC messages are sent when events are canceled or a CAPA message has been sent in error.  
They are triggered when: 
• An event is deleted after a CAPA message has already been sent for that event,  
• The CA [[ID]] on the CANO changes after a CAPA message has already been sent, or  
• The NILP (New Indicator field) in the CANO message equals “Y.” 
 
There are no legacy [[CCF]] files for the CAPC message. 
CAPA and CAPC Messages 
Although the CAPC will never be sent without a CAPA being generated, it is a separate message subscription. 
Clients can opt whether or not to receive the CAPC in addition to the CAPA. As such, a CAPC subscription 
cannot be created without the existence of a CAPA subscription. 
Please see the CAPA section for more information regarding message subscription options . 
When Are CAPC Messages Generated? 
CAPC message generation differs for file and MQ formats. 
Via file: 
• Daily, 1:30 a.m. eastern time (CAD, P&I, MMI, STKD). 
 
Via MQ: 
• Real time, every half hour between 10:30 a.m. eastern time and 6:30 p.m. eastern time.  
 
5 The last two digits in the MX Identifier signify the version number. The MX version number may change during the SWIFT annual  release based on 
mandatory or optional updates to the standards. 
Current schemas are available on MyStandards and [[DTCC]].com. 

---

## Page 52

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 52 
 
• 1:30 a.m. eastern time for CAD, P&I, MMI, and STKD. 
Messaging Note 
A time stamp in the Business Application Header (BAH) allows you to verify message order.  
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times specified 
below. Exceptions are noted in the holiday processing schedule. 
Message Monday–Friday Saturday and Sunday 
CAPC Messages between 10:30 a.m. and 6:30 p.m. eastern 
time. 
Files transmitted at 1:30 a.m. eastern time. 
No messages or files transmitted. 
Holiday Processing Schedule 
The CAPC is generated in normal volumes for all U.S. and Canadian holidays except:  
• New Year’s Day, 
• Labor Day, and 
• Christmas Day. 
Information Contained on the CAPC Message 
Mapping for the message layout will conform to the ISO message rules. When applicable, supplemental data 
will be included with sub balances for [[Stock]] Loan and Repo transaction information. 
For more detailed technical information, please see the CAPC Message Data section.  
ISO Message Field Name [[DTCC]] Field Name/Notes 
MovementPreliminaryAdvice 
Identification 
Message [[ID]]. 
This is the message [[ID]] of the previously sent CAPA that is being canceled. 
CorporateActionEventIdentification CA [[ID]] 
This is the [[DTC]]-unique identifier of the event. 
OfficialCorporateAction 
EventIdentification 
Official Reference CA [[ID]] 
This is the official corporate action unique identifier. 
EventType Event Type 
MandatoryVoluntaryEventType This specifies the nature of the event: 
• [[DTC]] Mandatory/Voluntary 
• Declared Mandatory/Voluntary 

---

## Page 53

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 53 
 
ISO Message Field Name [[DTCC]] Field Name/Notes 
UnderlyingSecurity Security identification code of the event issue: 
• Event Security [[ID]] 
• Event Security Type 
• Event Security Description 
SafekeepingAccount [[participant]] Number 
This is the [[DTC]]-assigned [[participant]] identification number for the 
safekeeping account. 
CAPC Message Data 
CAPC messages are made up of the following building blocks: 
Message Building Block Definition/Information 
MovementPreliminaryAdvice 
Identification 
Identification of a previously sent movement preliminary advice document. 
CorporateActionGeneral Information General information about the corporate action event. 
AccountDetails General information about the safekeeping account and the account owner. 
CorporateActionDetails Information about the corporate action event. 
 
Complete mapping and technical information is available in the Message Usage Guideline (MUG) for CAPC 
messages. In this document, you can also find: 
• message functionality, 
• restriction summary, 
• message structure, 
• message rules, 
• message components, 
• message datatypes, 
• a restriction appendix, and 
• usage restriction guidelines. 
 
Please consult this guide in order to complete your technical mapping. 

---

## Page 54

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 54 
 
 
What is a CACO Message? 
A Corporate Action Movement Confirmation (CACO) message is available in real time or in batch files on the 
day that the allocation or the post-allocation adjustment takes place. CACO messages are generated per client 
account and per balance type. It indicates that a payment has been made as a result of an earlier corporate 
action. 
The identifying information for a CACO message is: 
MX Identifier ISO 20022 Message 
Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.036.002.xx6 CA Movement 
Confirmation 
supl.011.001.xx6 CACO MT 566 Allocations/Payments 
 
6 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version number 
may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards and [[DTCC]].com. 


---

## Page 55

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 55 
 
 
CACO messages are triggered: 
• When an item specified in the related CAPA message has allocated. The CACO confirms the amount that 
has been debited or credited as projected by the CAPA. 
• When a reversal amount has been settled. The CACO message follows the CARE message in a reversal. 
It confirms the new amount that has been debited or credited. 
• When an adjustment occurs on a previously sent CACO. This can take place for rate changes, tax 
withholding adjustments, post-allocation adjustments, and other miscellaneous adjustments. In the case of 
events that are not same-day rate changes for P&I events, adjustments will be represented with an 
additional CACO message. 
 
CACO messages include the confirmed allocation amount. 
For [[Stock]] Loans, REPOs, and Fails, these messages contain the associated balance.  
Balance types that may be represented include: 
• Confirmed Balance, 
• [[settlement]] Position Balance, 
• Borrowed Balance, 
• On Loan Balance, 
• [[collateral]] In Balance, 
• [[collateral]] Out Balance, 
• Pending Delivery Balance, and/or 
• Pending Receipt Balance. 
 
Legacy [[CCF]] files for the CACO message include: 
• CSHSET, 
• CSHSTA–CSHSTG, 
• CSHS01–CSHS13, 
• CSHDAL, 
• CSHFGA, 
• STKSTA–STKSTI, and 
• STKDIS. 
When Are CACO Messages Generated? 
CACO message generation differs for file and MQ formats. 
Via file: 
• Daily 4:00 p.m. eastern time (P&I, MMI) 
and/or 

---

## Page 56

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 56 
 
• Daily 7:00 p.m. eastern time (STKD) 
and/or 
• 1:30 a.m. eastern time (STKD). 
 
Via MQ: 
• Real time, every 20 minutes between 8:20 a.m. and up until approximately 4:30 p.m. eastern time (P&I, 
MMI). 
• Real time, 8:20 a.m. and 7:00 p.m. eastern time (STKD). 
Messaging Notes 
1. Each message will be sent per one [[participant]] account and will include [[Stock]] Loans, REPOs, and Fails 
(where applicable). 
2. Each CACO message will be generated for each payout within an event. For example, in the case of an 
event with both a cash and a [[Stock]] payout, and/or multiple cash payouts, you will receive separate 
CACOs for each (using the same CA [[ID]]). 
3. Post-allocation adjustments will be represented by additional CACO messages under the same CA [[ID]]. 
These only take place post-allocation, and reversals will only take place on payable date for P&I events. 
4. In case of a rate change on payable date, a reversal on the initial change will be allowed for P&I events. 
5. Any same day or post allocation rate adjustments on [[Stock]] loans, repos or fails will be represented with an 
additional CACO message showing the delta amount to be debited or credited.  
6. A time stamp in the Business Application Header (BAH) allows you to verify message order.  
7. Separate CACO messages will be generated for each post payable allocation.  
8. When a post payable adjustment is submitted during the day, the CACO message is only sent with the 
adjustment amount. 
9. For overnight adjustments, the CAPA is sent with preadvice of the adjustment. The CACO is then sent 
with the adjustment amount. 
CACO Message Sequence for Late Announcements 
Usually, a CACO message will follow a CAPA message. However, a CAPA message will not be sent when a  
late announcement is processed intraday. In this case, position is captured, a CANO -E is created, and (if the 
item has allocated) a CACO message is created. 
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Fr iday during the times specified 
below. Exceptions are noted in the holiday processing schedule. 

---

## Page 57

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 57 
 
Message Monday–Friday Saturday and Sunday 
CACO Messages between 8:20 a.m. and 7:00 p.m. eastern 
time based on customer subscription. 
Files transmitted at 4:00 p.m., 7:00 p.m., and 1:30 a.m. 
eastern time, based on customer subscription. 
No messages or files transmitted. 
CACO Holiday Processing Schedule 
U.S. and Canadian Holidays (both 
closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada closed) 
No messages are sent on: 
• New Year's Day 
• Labor Day, and 
• Christmas Day. 
For Canadian payments only, 
messages are sent on: 
• Dr. Martin Luther King, Jr. Day 
• Presidents' Day 
• Memorial Day 
• Juneteenth 
• Independence Day, and 
• Thanksgiving Day. 
Normal volumes occur on these days: 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day, and 
• Boxing Day. 
Files are transmitted based on 
customer subscription. 
Note: 
In addition to this chart, please note that [[DTCC]] operates on two U.S. bank holidays: 
• Columbus Day ([[Stock]] allocation only; no cash allocation) 
• Veterans’ Day ([[Stock]] allocation only; no cash allocation) 
CACO Adjustment Codes 
Please refer to Appendix A for a list of CAPA and CACO adjustment codes. 
Information Contained on the CACO Message 
Mapping for the message layout will conform to the ISO message rules. 
When applicable, supplemental data will be included with sub balances for [[Stock]] Loan and REPO transaction 
information. 
[[Stock]] loan, REPO, and Fail balances can be found in the body of the CACO message. Contra party balances 
can be found in the message extension. 

---

## Page 58

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 58 
 
Message Body 
ISO Message Fields [[DTCC]] Field Name/Notes 
MovementPreliminaryAdvice 
Identification 
Movement Preliminary Advice Identification 
The Message [[ID]] of the previously sent CAPA; used to link this 
CACO to the associated CAPA 
CorporateActionEventIdentification CA [[ID]] 
OfficialCorporateActionEvent 
Identification 
Official Reference CA [[ID]] 
EventType Event Type 
FinancialInstrumentIdentification • Event Security [[ID]] 
• Event Security [[ID]] Type 
• Event Security Description 
Account Details–header 
Note: 
Separate CACOs are sent for each balance type. 
Only one balance type is used per message. 
SafekeepingAccount [[participant]] Number 
ConfirmedBalance Confirmed Balance 
Used with one of the following balance types unless the 
adjustment is “miscellaneous” 
BorrowedBalance Borrowed Balance 
SL net negative 
OnLoanBalance On Loan Balance  
SL net positive 
CollateralInBalance [[collateral]] In Balance  
REPO net positive 
CollateralOutOfBalance [[collateral]] Out of Balance  
REPO net negative 
PendingDeliveryBalance Pending Delivery Balance  
Fail net positive 
PendingReceiptBalance Pending Receipt Balance  
Fail net negative 
SettlementPositionBalance [[settlement]] Position Balance  
Total eligible balance 
Corporate Action Details-header 
RecordDate Record Date 
ExDividendDate Ex Date 

---

## Page 59

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 59 
 
ISO Message Fields [[DTCC]] Field Name/Notes 
CorporateActionConfirmationDetails-header 
OptionNumber [[Option]] Number 
OptionType [[Option]] Type 
SecuritiesMovementDetails-header 
FinancialInstrumentIdentification [[DTC]] Disbursed Security [[ID]] and Type; Redemption Contra- 
[[CUSIP]] 
CreditDebitIndicator Indicates whether the operation is an increase (CRED) or a 
decrease (DEBT) 
TemporaryFinancialInstrumentIndicator Yes/No indicator to indicate when Contra [[CUSIP]] is used 
PostingQuantity [[securities]] Quantity 
Quantity that is being paid; allocated positions 
PostingDate [[DTC]] Allocation date and time  
Date that payment is made 
PaymentDate Declared payable date ([[issuer]] payable date) 
CashMovementDetails-header 
CreditDebitIndicator Indicates whether the operation is an increase (CRED) or a 
decrease (DEBT) 
PostingAmount Cash amount for cash, principal, or [[Premium]] payouts when the 
event type is not one of the following: 
• Dutch Auction 
• Exchange 
• Full Call 
• Full Prefunding 
• Final Paydown, 
• Partial Call 
• Reorganization 
• Tender Offer 
Valid ISO currency code (e.g., USD, CAD) is used in this field 
NetCashAmount Cash amount for a [[Dividend]] payout 
Valid ISO currency code (e.g., USD, CAD) is used in this field 
CapitalGain Cash amount for a capital gains, short-term capital gains, long- 
term capital gains, or return of capital payout 
Valid ISO currency code (e.g., USD, CAD) is used in this field 
CashInLieuOfShare Used when a CAPA is sent for a Cash in Lieu payment 
InterestAmount Cash amount for an interest payment when the event is a 
straight P&I 
Valid ISO currency code (e.g., USD, CAD) is used in this field 

---

## Page 60

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 60 
 
ISO Message Fields [[DTCC]] Field Name/Notes 
AccruedInterestAmount Cash amount for an interest payment when the event is 
another that pays accrued interest 
Valid ISO currency code (e.g., USD, CAD) is used in this field 
PostingDate [[DTC]] allocation date and time (date that payment was made) 
PaymentDate Declared payable date ([[issuer]] payment date) 
Supplementary Data: The breakdown of sub balances (adjustments) 
CorporateActionConfirmationSecuritiesMovementDetails (extended)–header (this section repeats) 
CreditDebitIndicator Indicates whether the operation is an increase (CRED) or a 
decrease (DEBT) 
TransactionQuantity Transaction [[securities]] Quantity 
The resulting quantity of [[securities]] concerned in this 
transaction 
ReasonCode Transaction Reason 
See the CACO Reason Codes section for more information 
SubReasonCode Sub Reason Code 
See the CACO Sub Reason Codes section for more 
information 
ContraParticipantNumber Contra [[participant]] Number 
The transaction’s contra [[participant]] [[ID]] when [[shares]] are 
distributed/delivered to/from another [[participant]] 
PostingDate [[DTC]] Allocation Date and Time 
The date and time on which the posting/draft of the [[securities]] 
took place for a transaction 
TaxAdjustmentRate Sub Reason Code 
A set of the [[DTC]] legacy sub reason codes representing tax 
rate 
Used with the following 
reason codes to identify the correct 
tax rate: 
• TJXD 
• TJXF 
• TJXI 
• TJXL 
• TJXO 
• TJXR 
• TJXT 
• TJXU 
• TJXV 
CorporateActionConfirmationCashMovementDetails (extended)–header (this section repeats) 
CreditDebitIndicator Indicates whether the operation is an increase (CRED) or a 
decrease (DEBT) 

---

## Page 61

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 61 
 
ISO Message Fields [[DTCC]] Field Name/Notes 
TransactionAmount Transaction Cash Amount 
The resulting cash amount involved in this transaction 
ReasonCode Transaction Reason 
See the CACO Reason Codes section for more information 
SubReasonCode Sub Reason Code 
See the CACO Sub Reason Codes section for more 
information 
ContraParticipantNumber Contra [[participant]] Number 
This is the transaction’s contra [[participant]] [[ID]] when [[shares]] are 
distributed/delivered to/from another [[participant]] 
PostingDate [[DTC]] Allocation Date and Time 
The date and time on which the posting/draft of the [[securities]] 
took place for a transaction 
TaxAdjustmentRate Sub Reason Code 
A set of the [[DTC]] legacy sub reason codes representing tax 
rate 
Used with the following reason codes to identify the correct 
tax rate: 
• TJXD 
• TJXF 
• TJXI 
• TJXL 
• TJXO 
• TJXR 
• TJXT 
• TJXU 
• TJXV 
CACO Message Data 
CACO messages are made up of the following building blocks: 
Message Building Block Definition/Information 
NotificationIdentification Identifying information associated with a previously sent 
notification document 
MovementPreliminaryAdviceIdentification Identifying information associated with a previously sent 
movement preliminary advice document 
OtherDocumentIdentification Provides identifying information, including document 
numbers, for any other documents 
CorporateActionGeneralInformation Provides general information about the corporate action 
event 

---

## Page 62

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 62 
 
Message Building Block Definition/Information 
AccountDetails Contains general information about the safekeeping 
account, owner, and account balance 
CorporateActionConfirmationDetails Provides information about the corporate action [[Option]] 
AdditionalInformation Provides additional information 
SupplementaryData Provides additional information that cannot be captured in 
the structured fields and/or any other specific block 
 
Complete mapping and technical information is available in the Message Usage Guideline (MUG) for CAPC 
messages. In this document, you can also find: 
• message functionality, 
• restriction summary, 
• message structure, 
• message rules, 
• message components, 
• message datatypes, 
• a restriction appendix, and 
• usage restriction guidelines. 
 
Please consult this guide in order to complete your technical mapping. 

---

## Page 63

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 63 
 
 
What is a CARE Message? 
A Corporate Action Movement Reversal (CARE) message is sent when a rate change occurs on an allocated 
payment for which a CACO message was already generated. CARE messages are generated per client 
account and per balance type for any difference from the original CACO amount. 
Note: 
Reversals only take place on principal and interest (P&I) payments. 
The identifying information for a CARE message is: 
MX Identifier ISO 20022 
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.037.002.xx7 CA Movement Reversal 
Advice 
supl.025.001.xx7 CARE MT 566 NEW 
 
7 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version number 
may change during the SWIFT annual release based on mand atory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards and [[DTCC]].com. 


---

## Page 64

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 64 
 
A CARE message contains a reversal for the full payment amount. CARE messages apply to primary 
allocation amounts. 
CARE messages are created in real time and are coupled with associated CACO messages. They are sent out 
as part of the intraday process and transmitted in real time to subscribing customers. Customers who take files 
will receive their CACO and CARE messages in the same file. 
There are no legacy files for the CARE message. 
When Are CARE Messages Generated? 
CARE messages are only sent on an event’s pay date. They are created in real-time between 8:20 a.m. and 
4:30 p.m. and are coupled with associated CACO messages. CARE messages are only available on P&I 
events. 
Via MQ: 
• Real time, every 20 minutes between 8:20 a.m. and 4:30 p.m. eastern time (P&I only).  
 
Via file: 
• Daily 4:00 p.m. eastern time (P&I only) 
Messaging Notes 
1. Each message will be sent per one [[participant]] account and will include the total eligible balance.  
• total eligible balance, 
2. The reversal message flow is CAPA–CARE–CACO: 
• The CAPA is sent as a preadvice of the reversal. 
• This is followed by a CARE CRED for the amount that is being reversed. 
• Finally, a CACO CRED is sent for the new amount. 
3. Post-allocation adjustments will be represented by additional CACO messages under the same CA [[ID]]. 
These only take place post-allocation, and reversals will only take place on payable date. 
4. A time stamp in the Business Application Header (BAH) allows you to verify message order.  
5. Separate CARE messages will be generated for each allocation reversal.  
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times specified 
below. Exceptions are noted in the holiday processing schedule. 

---

## Page 65

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 65 
 
Message Monday–Friday Saturday and Sunday 
CARE Messages between 8:20 a.m. and 4:30 p.m. eastern 
time based on customer subscription. 
Files transmitted at 4:00 p.m. eastern time, based on 
customer subscription. 
No messages or files transmitted. 
CARE Holiday Processing Schedule 
U.S. and Canadian Holidays (both 
closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada closed) 
No messages are sent on: 
• New Year's Day 
• Labor Day, and 
• Christmas Day. 
For Canadian payments only, 
messages are sent on: 
• Dr. Martin Luther King, Jr. Day 
• Presidents' Day 
• Memorial Day 
• Juneteenth 
• Independence Day, and 
• Thanksgiving Day. 
Normal volumes occur on these days: 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day, and 
• Boxing Day. 
Files are transmitted based on 
customer subscription. 
Note: 
In addition to this chart, please note that [[DTCC]] operates on two U.S. bank holidays: 
• Columbus Day ([[Stock]] allocation only; no cash allocation) 
• Veterans’ Day ([[Stock]] allocation only; no cash allocation) 
Information Contained on the CARE Message 
Mapping for the message layout will conform to the ISO message rules. 
Message Body 
ISO Message Fields [[DTCC]] Field Name/Definition 
MovementConfirmationIdentification Movement Confirmation Identification 
ReversalReason Reversal Reason8 
CorporateActionEventIdentification CA [[ID]] 
OfficialCorporateActionEventIdentification Official Reference CA [[ID]] 
EventType Event Type 
FinancialInstrumentIdentification Event Security [[ID]] 
Event Security [[ID]] Type 
Event Security Description 
 
8 Incorrect price (IPRI)-Reversals are limited to the same rate change reversals. Only this value will be used.  

---

## Page 66

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 66 
 
ISO Message Fields [[DTCC]] Field Name/Definition 
SafekeepingAccount [[participant]] Number 
ConfirmedBalance Confirmed Balance 
Corporate Action Details 
RecordDate Record Date 
Ex DividendDate Ex Date 
Corporate Action Confirmation Details 
OptionNumber [[Option]] Number 
OptionType [[Option]] Type 
[[securities]] Movement Details 
FinancialInstrumentIdentification Security Identification 
CreditDebitIndicator Credit Debit Indicator 
PostingQuantity Posting Quantity 
PostingDate Posting Date 
OriginalPostingDate [[DTC]] Allocation Date and Time 
Cash Movement Details 
CreditDebitIndicator Credit Debit Indicator 
PostingAmount Posting Amount 
PostingDate Posting Date 
OriginalPostingDate [[DTC]] Allocation Date and Time 
OriginalPostingDate [[DTC]] Allocation Date and Time 
CARE Message Data 
CARE messages are made up of the following building blocks: 
Message Building Block Definition/Information 
MovementConfirmationIdentification Identification of a previously sent movement confirmation 
document 
OtherDocumentIdentification Identification of other documents as well as the document 
number 
EventsLinkage Identification of an other corporate action event that needs to 
be closely linked to the processing of the event notified in this 
document 
ReversalReason Reason for the reversal 

---

## Page 67

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 67 
 
Message Building Block Definition/Information 
CorporateActionGeneralInformation Contains general information about the corporate action event. 
AccountDetails Contains general information about the safekeeping account, 
owner, and account balance 
CorporateActionConfirmationDetails Provides information about the corporate action [[Option]] 
AdditionalInformation Provides additional information 
SupplementaryData 
Note: 
This field will be removed for SR 2015 
Provides additional information that cannot be captured in the 
structured fields and/or any other specific block 
 
Complete mapping and technical information is available in the Message Usage Guideline (MUG) for CAPC 
messages. In this document, you can also find: 
• message functionality, 
• restriction summary, 
• message structure, 
• message rules, 
• message guidelines, 
• message components, 
• message datatypes, and 
• usage restriction guidelines. 
 
Please consult this guide in order to complete your technical mapping. 

---

## Page 68

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 68 
 
 
What is a CAPS Message? 
A Corporate Action Event Processing Status Advice (CAPS) message is created for payments that were not 
allocated on payment date. If a same-day position capture event does not allocate, a CAPS message will be 
sent at the end of the day. 
The identifying information for a CAPS message is: 
MX Identifier SR 
2104 
ISO 20022 
Message Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTCC]] 
Processes 
seev.032.002.xx9 CA Event Processing 
Status Advice 
supl.010.001.xx9 CAPS MT 567 Unallocated Positions 
 
9 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version number 
may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on MyStandards and [[DTCC]].com. 


---

## Page 69

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 69 
 
Legacy [[CCF]] files for non-allocations include: 
• CSHUNL, 
• CSHEUD, 
• CSHEU1, 
• CSHEU2, 
• CSHIUA–CSHIUC, 
• CSHDUN, and 
• STKUND. 
 
When Are CAPS Messages Generated? 
CAPS messages are generated: 
• Daily at 4:00 p.m. eastern time for unallocated positions resulting from Canadian Dollar and Money Market 
Instrument (MMI) Distribution events. 
• Daily at 5:00 p.m. for unallocated positions resulting from P&I Distribution events. 
• Daily at 7:00 p.m. for unallocated positions resulting from [[Stock]] Distribution events. This could also 
include any unallocated positions resulting from P&I Distribution events.  
 
Times are the same for file and MQ formats, except: 
• Real time [[Option]] hourly between 1:00 p.m. and 7:00 p.m. eastern time. 
Messaging Notes 
1. The CAPS message is sent based on the CAPA that was previously sent. 
2. It is possible to receive a CAPS message on an event that never had a CAPA. This can occur for late 
events in a same-day position capture. A late event would come into the system and generate a CANO -E 
at 1:45 p.m., then generate a CAPS message later that day if it does not allocate.  
3. Reason codes are provided to explain why a given event was not allocated. 
4. A time stamp in the Business Application Header (BAH) allows you to verify message order.  
5. If an item is past payable date, the CAPA message is only sent once. The CAPS message will continue to 
be sent on a daily basis. 
6. Since the CAPC (cancellation) message is generated intraday, a CAPS message is not gener ated at the 
end of the day if an announcement is both unallocated and marked for deletion.  
Weekly Messaging Times 
Generally, entitlements and allocations messages are sent Monday through Friday during the times specified 
below. Exceptions are noted in the holiday processing schedule. 

---

## Page 70

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 70 
 
Message Monday–Friday Saturday and Sunday 
CAPS Messages between 1:00 p.m. and 7:00 p.m. eastern 
time based on customer subscription. 
Files transmitted at 4:00 p.m., 5:00 p.m., and 7:00 p.m. 
eastern time. 
No messages or files transmitted. 
CAPS Holiday Processing Schedule 
U.S. and Canadian Holidays  
(both closed) 
U.S. Holidays 
([[DTCC]] closed, Canada open) 
Canadian Holidays 
([[DTCC]] open, Canada closed) 
No messages are sent on: 
• New Year's Day 
• Labor Day, and 
• Christmas Day. 
Messages are sent at 
• 1:00 p.m. eastern time, 
• 2:00 p.m. eastern time, and 
• 3:00 p.m. eastern time 
for P&I and Foreign payments For 
these holidays: 
• Dr. Martin Luther King, Jr. Day 
• Presidents' Day 
• Memorial Day 
• Juneteenth 
• Independence Day, and 
• Thanksgiving Day 
Normal volumes occur on these days: 
• Good Friday (All) 
• Victoria Day 
• Canada Day 
• CDN Thanksgiving Day, and 
• Boxing Day. 
Files are transmitted based on 
customer subscription. 
Note: 
In addition to this chart, please note that [[DTCC]] operates on two U.S. bank holidays: 
• Columbus Day ([[Stock]] allocation only; no cash allocation) 
• Veterans’ Day ([[Stock]] allocation only; no cash allocation) 
Information Contained on the CAPS Message 
Mapping for the message layout will conform to the ISO message rules. 
Message Body 
ISO Message Fields [[DTCC]] Field Name/Notes 
CorporateActionEventIdentification CA [[ID]] 
OfficialCorporateActionEvent Identification Official Reference CA [[ID]] 
EventType Event Type 
EventProcessingStatus-header 
Pending/NoSpecifiedReason No Reason Code 
Unallocated, no reason code available. For use with code “NORE.” 

---

## Page 71

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 71 
 
ISO Message Fields [[DTCC]] Field Name/Notes 
Pending/ReasonCode Reason Code 
If the reason code is known, the choices are: 
• NSEC-[[securities]] not delivered 
• NPAY-no Payment 
• OTHR-other; see narrative 
AdditionalReasonInformation Text 
Optional. This field may contain additional information explaining why 
the event did not allocate 
Supplementary Data 
CorporateActionGeneralInformation-header 
SecurityIdentification Consists of the following: 
• Event Security [[ID]] 
• Event Security [[ID]] Type 
• Event Security Description 
SafekeepingAccount [[participant]] Number 
Unallocated Details–header 
Note: 
Separate CAPS messages are sent for each balance type. Only one balance type listed below is used per message. 
TotalEligibleBalance Total Eligible Balance 
Current balance eligible for elections and allocations. 
BorrowedBalance Borrowed Balance 
Represents the negative net balance of the [[Stock]] loans 
OnLoanBalance On Loan Balance 
Represents the positive net balance of he [[Stock]] loans 
CollateralInBalance [[collateral]] In Balance 
Represents the positive net balance of the repurchase agreements 
(REPOs) 
CollateralOutBalance [[collateral]] Out of Balance 
Represents the negative net balance of the repurchase agreements 
(REPOs) 
PendingDeliveryBalance Pending Delivery Balance 
Represents the negative net balance of the fail trades 
PendingReceiptBalance Pending Receipt Balance 
Represents the positive net balance of the fail trades 
UnallocatedSecuritiesTransactionDetails-header 
CreditDebitIndicator Indicates whether the operation is an increase or decrease 

---

## Page 72

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 72 
 
ISO Message Fields [[DTCC]] Field Name/Notes 
ReasonCode Transaction Reason: 
• FL-Fail Payment/Charge maps to FAIL 
• RP-Repo Payment/Charge maps to REPO 
• SL-[[Stock]] Loan Payment/Charge maps to STOK 
• AD-Misc Payment/Charge maps to MISC 
TransactionQuantity Transaction [[securities]] Quantity 
The resulting quantity of [[securities]] concerned in this transaction 
“FaceAmount is used for Debt and “Unit” is used for non-debt 
UnallocatedReasonCode Unallocated Reason Code 
See the Reason Codes section for more information 
Contra [[participant]] Number Contra [[participant]] Number 
When [[shares]] are distributed/delivered to/from another [[participant]], 
this is the transaction contra [[participant]] [[ID]] 
Used for fails, REPOs, and [[Stock]] loans 
Earliest Payment date Payable Date 
The date/time on which the posting/draft of the [[securities]] is 
scheduled to take place for a transaction. 
UnallocatedCashTransactionDetails-header 
CreditDebitIndicator Indicates whether the operation is an increase or a decrease 
ReasonCode Transaction Reason 
• FL-Fail Payment/Charge maps to FAIL 
• RP-Repo Payment/Charge maps to REPO 
• SL-[[Stock]] Loan Payment/Charge maps to STOK 
• AD-Misc Payment/Charge maps to MISC 
TransactionAmount Transaction Cash Amount 
The resulting cash amount involved in this transaction 
UnallocatedReasonCode Unallocated Reason Code 
See the Reason Codes section for more information 
Contra [[participant]] Number Contra [[participant]] Number 
When [[shares]] are distributed/delivered to/from another [[participant]], 
this is the transaction contra [[participant]] [[ID]] 
Used for fails, REPOs, and [[Stock]] loans 
Earliest Payment date Payable Date 
The date/time on which the posting/draft of the [[securities]] is 
scheduled to take place for a transaction. 
CorporateActionDetails-header 
Record Date Record Date 
The record date for the event (set by the [[issuer]]/agent) that 
determines [[Entitlement]] 

---

## Page 73

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Entitlements and Allocations Messaging 73 
 
ISO Message Fields [[DTCC]] Field Name/Notes 
Payment Date Declared Payable Date 
The payable date as announced by the [[issuer]] or offeror 
CAPS Message Data 
CAPS messages are made up of the following building blocks: 
Message Building Block Definition/Information 
NotificationIdentification Identification of a previously sent notification document 
OtherDocumentIdentification Identification of other documents as well as the document 
number 
CorporateActionGeneralInformation Contains general information about the corporate action event 
EventProcessingStatus Contains information about the status of a corporate action 
AdditionalInformation Provides additional information 
SupplementaryData Provides additional information that cannot be captured in the 
structured fields and/or any other specific block 
 
Complete mapping and technical information is available in the Message Usage Guideline (MUG) for CAPC 
messages. In this document, you can also find: 
• message functionality, 
• restriction summary, 
• message structure, 
• message rules, 
• message components, 
• message datatypes, and 
• usage restriction guidelines. 
 
Please consult this guide in order to complete your technical mapping. 
CAPS Reason Codes 
A CAPS reason code provides an explanation for why payment on an event has not allocated.  
Please see Appendix A for a list of these reason codes. 

---

## Page 74

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 74 
 
APPENDIX A: REASON CODES 
Adjustment Reason Codes (CAPA/CACO Message) 
ISO Code Reason Code Name Reason Code Description 
FAIL Fail [[settlement]] Fail [[settlement]]-related adjustment 
MISC Miscellaneous [[settlement]] Miscellaneous [[settlement]]-related adjustment 
OTHR Other Reserved for new user-defined reason codes 
RADC ADRIssueFeeCharge [[ADR]] issue fee charge adjustment 
RADR ADRIssueFeeReversal [[ADR]] issue fee reversal adjustment 
RCDP CustodyDividendPayment [[Dividend]] payment on a [[DTC]] [[custody]]-held security related 
adjustment 
RCIL CashInLieu Cash in lieu-related adjustment 
REPO RepoSettlement Repurchasing agreement-related adjustment 
REVA Reversal Reversal-related adjustment 
RRCD CustodyReorganization Deposit [[custody]] reorganization deposit-related adjustment 
RRCL ClaimSettlement Claim [[settlement]]-related adjustment 
RRD1 ReorgDepositPhase1 [[participant]] deposited a security within 10 days after a 
corporate action event has occurred 
RRD2 ReorgDepositPhase2 [[participant]] deposited a security 10 days after a corporate 
action event has occurred 
RRDR DynamicRateChange Dynamic rate change-related adjustment 
RRLR MandatoryLegalReorg Deposit Mandatory legal reorganization deposit-related adjustment 
RRMD MandatoryReorganization Deposit Mandatory reorganization deposit-related adjustment 
RRML LegalReorgDeposits Legal reorganization deposit-related adjustment 
RRR3 MandatoryOverThreeYear 
ReorganizationDeposit 
Mandatory over three year reorganization deposit-related 
adjustment 
RRRA AdjustedforRights Subscription Adjusted for rights subscription-related adjustment 
RRRE RightsSubscription Rights subscription related adjustment 
RRRI RightsProtect Rights protect related adjustment 
RRRL LastDayProtect Last day protect related adjustment 
RRRS RightsSales Rights sales-related adjustment 
RRRU RightsStepUp Rights step up-related adjustment 
RRT2 TenderOfferFraction Tender offer fraction-related adjustment 

---

## Page 75

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 75 
 
ISO Code Reason Code Name Reason Code Description 
RRWC WarrantRateChange Warrant rate change-related adjustment 
RRWT WarrantParticipantDelete Warrant [[participant]] delete-related adjustment 
STOK StockLoanSettlement [[Stock]] loan related adjustment 
TJXD ReclassificationTax Withholding Reclassification tax withholding-related adjustment 
TJXF FailTrackingTaxWithholding Fail tracking tax withholding-related adjustment 
TJXI TaxInstructionChange Tax instruction change-related adjustment. 
TJXL OriginalLateTaxWithholding Original late tax withholding-related adjustment 
TJXO OriginalInitialTaxWithholding Original (initial) tax withholding-related adjustment 
TJXR ReversalofTaxWithholding Reversal of tax withholding-related adjustment 
TJXT RateChangeTaxWithholding Rate change tax withholding-related adjustment 
TJXU ManualUserTax Manual user tax adjustment 
TJXV Intra-DayReversalofOriginal 
TaxWithholding 
Intra-day reversal of original tax withholding-related 
adjustment 
CAPA/CACO Sub Reason Codes 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
S777 ReorganizationRelatedAdjustment Reorganization-related adjustment on user- 
defined date 
S66P InterestDueWasErroneouslyPaidToYouByTheIssuer The interest due on the above [[CUSIP]] was 
erroneously paid by the [[issuer]] although the 
certificate of deposit was transferred to 
CEDE ([[DTCC]]) prior to the interest payment 
date 
SABA AllocationofBabyBondsAmountToBeExited Allocation of baby [[Bonds]] amount to be exited 
in USD 
SAC7 InterestorDividendDueonConversion Interest or [[Dividend]] due on conversion 
related adjustment 
SACA AccruedInterestWrongRate The accrued interest previously paid was at 
the wrong rate; this adjustment is to correct 
that erroneous payment 
SACB InterestAdjustedDueToEarlyWithdrawal Interest adjusted due to early withdrawal 
(certificate of deposit) 
SACP AccruedInterestNotPaid Accrued interest was not previously paid for 
the redemption in this issue; this adjustment 
is to pay this accrued interest. 
SADA CompanyInDefault Company in [[default]]-related adjustment. 

---

## Page 76

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 76 
 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
SADM IssueInDefault Issue in [[default]] related adjustment. 
SAEA InterestAllocatedInError Interest allocated in error first payment on 
[date user defined]. 
SAF7 TenderFeeDeduction Interest adjusted due to tender fee 
deduction. 
SAFA SupplementaryInterimOn Supplementary interim on user-defined date. 
SAGA GracePeriod Company is taking 30 day grace period. 
SAHA PaymentOfFullAvoidFiscalTaxRefund Payment of full avoid fiscal tax refund (equal 
to 42.5% of the [[Dividend]]) 
SAIA AdjustmentToAvoidFiscalPayment Adjustment to avoid fiscal payment. 
SAJA RevisionOfChargeForWithholdingTax Revision of charge for withholding tax. 
SAM7 InterestOrDividendDueOnMerger Interest or [[Dividend]] due on merger related 
adjustment. 
SAMA InterestPaysAtMaturity Interest pays at maturity. Allocated in error 
on user defined date. 
SANA CompanyDidNotDeclareDividend Company never declared [[Dividend]] adjust 
allocation on user defined date. 
SAP7 InterestOrDividendDueOnRepaymentOption Interest or [[Dividend]] due on repayment 
[[Option]]. 
SAPA PaymentOfPartialAvoidFiscalTaxRefund Payment of partial avoid fiscal tax refund 
(equal to 15% of the [[Dividend]]). 
SAPP CalledCertificatesAccruedErroneousInterestChargeBack Certificates you deposited prior to publication 
date were subsequently called. The agent 
paid [[DTCC]] the principal redemption 
proceeds but erroneously paid you the 
accrued interest. 
SAR7 InterestOrDividendDueOnRedemption Interest or [[Dividend]] due on redemption. 
SARA AssumedByYourGoodselves Allocation for a [[participant]] position that was 
assumed by your goodselves paid on— 
retired [[participant]] number. 
SASA ScriptSharesExited Allocation of script [[shares]] amount to be 
exited in dollar value. 
SAT7 InterestOrDividendDueOnTender Interestor [[Dividend]] due on tender. 
SAWA UninsuredInterestWithheld Uninsured interest withheld as per FSLICN. 
SSBB DWACBuyBackWithdrawal Your record date position was adjusted for a 
[[DWAC]] buy back withdrawal. 
SBB1 CODBuyBackWithdrawal Your record date position was adjusted for a 
COD buy back withdrawal. 

---

## Page 77

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 77 
 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
SBB2 WithdrawalTransferBuyBackWithdrawal Your record date position was adjusted for a 
w/t buy back withdrawal. 
SBDB CODWithdrawalNotDeliveredAndCertificatesInTheNameOf 
YourGoodselves 
Your COD withdrawal was not delivered. 
However, the certificate(s) were issued and 
outstanding over the record date in the name 
of your goodselves. 
SBEB CODWithdrawalNotDeliveredAndCertificatesIssuedInThe 
NameOfYourNominee 
Your COD withdrawal was not delivered. 
However, the certificate(s) were issued and 
outstanding over the record date in the name 
of your [[nominee]] 
SBRH ReversalOfACODWithdrawal Reversal of a COD withdrawal-related 
adjustment. 
SCDP CustodyPayment [[custody]] payment. 
SCKS CalledCertificatesCheckInParticipantsNameChargeBack Certificates you deposited prior to publication 
date were subsequently called. The agent 
paid [[DTCC]] the principal proceeds via check, 
but in your customer’s name. We are 
forwarding the check today. This adjustment 
is to charge you for the funds. 
SCLU PacificDepository Adjustment made for the Pacific depository 
(3097). 
SCMU MidwestDepository Adjustment made for the Midwest depository 
(6942). 
SCNU PhiladelphiaDepository Adjustment made for the Philadelphia 
depository (6070). 
SCPK AccrualClaimPayment Accrual claim payment related to a [[Stock]] 
distribution payable on user defined date. 
SCPP Part-ClaimPayment Part claim payment. 
SCRK ReversalOfAnAccrualClaimPayment Reversal of an accrual claim payment related 
to a [[Stock]] distribution payable on user 
defined date. 
SCRP Part-ClaimReversal Part-claim reversal. 
SCSM CouponCollectionService Coupon collection service adjustment for 
coupon deposit. 
SDAD Deposit— 
LostCertificateOverTheRecordDateWasRegisteredInThe 
NameOfYour 
Adjustment related to the deposit of lost 
certificate over the record date was 
registered in the name of your [user defined]. 
SDBD LostCertificateRegisteredInTheNameOfYourGoodselves Adjustment related to the deposit of lost 
certificate over the record date was 
registered in the name of your goodselves. 

---

## Page 78

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 78 
 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
SDCD DepositTransferredIntoTheNameOfTheCEDEandCo. Deposit after cut off date-transferred into the 
name of the CEDE on record date. 
SDDD PositionAdjustedForDepositActivity Your record date position was adjusted for 
deposit activity. 
SDED LostCertificateWasRegisteredInTheNameofYourNominee Adjustment related to the deposit of lost 
certificate over the record date was 
registered in the name of your [[nominee]]. 
SDEP PreviouslyCalledCertificatesFundsDelivery You deposited [[securities]] that were previously 
called. The agent paid [[DTCC]] the redemption 
proceeds. This adjustment is to pass these 
proceeds on to you. Your free account 
security position will be adjusted (shorted) 
today for the called quantity. 
SDMT CTFSHeldOverRecordDateOnWhichWeGuaranteeToHold 
YouFreeAndHarmlessOfAnyFurtherClaimonThisDividend 
CTF(s) held over record date on which we 
guarantee to hold you free and harmless of 
any further claim on this [[Dividend]]. 
SDRH ReversalOfADeposit Reversal of a deposit adjustment. 
SEEE DeliverOrderActivity Your record date position was adjusted for 
deliver order ([[DO]]) activity. 
SETO ReverseoftheSharesEscheatedtoNYStateInError [[shares]] escheated to New York state in error; 
affidavit to follow. This is to reverse the 
escheated amount. 
SFAF ChargeForFrenchAvoidFiscalTaxCredit As per agent, this charge is for French avoid 
fiscal tax credit. 
SFAP ReverseOfEscheatedAmountOfClaim Funds previously escheated to New York 
state, affidavit to follow This is to reverse the 
escheated amount of claim paid on user- 
defined date. 
SFE8 ForeignCashDividendsOrBondInterestAllocationAtExempt 
Rate 
Foreign cash dividends/bond interest 
allocation at exempt rate. 
SFF8 ForeignCashDividendsOrBondsInterestAllocation 
AtFavorableRate 
Foreign cash dividends/[[Bonds]] interest 
allocation at favorable rate. 
SFG8 15%FrenchWithholdingTax 15% French withholding tax, based on your 
[[Option]] election of 100% ADRs at the 
favorable rate. 
SFG9 25%FrenchWithholdingTax 25% French withholding tax, based on your 
[[Option]] election of 100% ADRs at the 
unfavorable rate. 
SFH9 10%FrenchWithholdingTax 10% French withholding tax, based on your 
revised instructions to reduce favorable tax 
status to unfavorable. 

---

## Page 79

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 79 
 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
SFI9 ChargeAtWithholdingRate Required lists contained discrepancies or 
were not forwarded to French paying agent. 
This charge at user defined withholding rate. 
SFJ9 RefundedTaxRate The 25% French withholding rate has been 
revised. This adjustment is based on the 
refunded tax rate. 
SFL0 RateUnknown Rate unknown for fail tracking related 
adjustment. 
SFL1 Delete Delete for fail tracking related adjustment. 
SFL2 Reinstate Reinstate for fail tracking related adjustment. 
SFL3 PostDateChangeforFailTracking Post date change for fail tracking related 
adjustment. 
SFLD AnnouncementDeletedOrFailTracking Announcement deleted for fail tracking 
related adjustment. 
SFLE DueBill Due bill for fail tracking related adjustment. 
SFLL LateAnnouncement Fail tracking for fail tracking related 
adjustment. 
SFLN DateRevision Date revision for fail tracking related 
adjustment. 
SFLR RateRevision Rate revision for fail tracking related 
adjustment. 
SFLS NonAllocation Non allocation for fail tracking related 
adjustment. 
SFRA RefundOfFrenchTaxFortheJune1992 Refund of French tax based on acceptance 
of global reclamation for the June 1992 
distribution refer to important notice b # 
1352-93 
SFRB RefundOfFrenchTaxJuly1992 Refund of French tax based on acceptance 
of global reclamation for the July 1992 
distribution refer to important notice b # 
1352-93 
SFU9 ForeignCashDividendsorBondInterestAllocation 
AtUnfavorableRate 
Foreign cash dividends or bond interest 
allocation at unfavorable rate. 
SGL7 RedemptionCash Redemption cash [[settlement]]. 
SGLA AllocationAdjustment Allocation adjustment. 
SGLM MuniBearerBond MUNI bearer bond coupon adjustment (same 
as line 118). 
SGLP RedemptionPaymentDuetoPledgeRelease Redemption payment due to pledge release. 

---

## Page 80

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 80 
 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
SGLQ DTCCClaimOnRegisteredHolderInTheNameOfYour 
Goodselves 
[[DTCC]] claim on registered holder in the name 
of your goodselves. 
SGLT InSettlementOfATradeDTCCReorgAccount In [[settlement]] of a trade-[[DTCC]] reorg account 
428-10271-1-2-039. 
SGLZ DTCCClaimOnRegisteredHolderInTheNameOfYour 
Customer 
[[DTCC]] claim on registered holder in the name 
of your customer. 
SIGE InterimPositionAdjustedForDeliverOrderActivity Your interim position was adjusted for deliver 
order activity. 
SILL LateAnnouncementActivityDueBillActivity Late announcement activity, due bill activity 
related adjustment. 
SJCB CODWithdrawal [[DTCC]] COD withdrawal adjustment. 
SJDD DepositAdjustment [[DTCC]] deposit-related adjustment. 
SJE7 RedemptionAdjustment [[DTCC]] redemption-related adjustment. 
SJEE PledgeReleaseAdjustment [[DTCC]] pledge release-related adjustment. 
SJEW WriteOffReorganization Write off reorganization-related adjustment. 
SJIE InvestmentIdAdjustment [[DTCC]] investment [[ID]]-related adjustment. 
SJEF PledgeAdjustment [[DTCC]] pledge related adjustment. 
SJEG DeliverOrder [[DTCC]] deliver order-related adjustment. 
SJR7 ReorganizationAdjustment [[DTCC]] reorganization-related adjustment. 
SJWT WithdrawalTransferAdjustment [[DTCC]] WT-related adjustment. 
SLCP DTCCClaimAgainstRegisteredHolderInTheNameof 
YourCustomerLateTransfer 
[[DTCC]] claim against registered holder in the 
name of your customer. Late identification of 
missed transfer by [[transfer agent]]. 
SLGP DTCCClaimAgainstRegisteredHolderInTheNameofYour 
GoodselvesLateTransfer 
[[DTCC]] claim against registered holder in the 
name of your goodselves. Late identification 
of missed transfer by [[transfer agent]]. 
SLNP DTCCClaimAgainstRegisteredHolderInTheNameofYour 
[[nominee]]. 
[[DTCC]] claim against registered holder in the 
name of your [[nominee]]. Late identification of 
missed transfer by [[transfer agent]]. 
SMAM MuniBearerBondCoupon Muni bearer bond coupon-related 
adjustment. 
SMBM MuniBearerBondCouponAdjustmentForCouponsMissing 
FromaDeposit 
Muni bearer bond coupon adjustment for 
coupon(s) missing from a deposit-related 
adjustment. 
SMCM MuniBearerBondCouponAdjustmentForCouponsMissing 
FromaWithdrawal 
Muni bearer bond coupon adjustment for 
coupon(s) missing from a withdrawal 

---

## Page 81

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 81 
 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
SMDM MuniBearerBondCouponAdjustmentExcessCoupons 
WithdrawnOn 
Muni bearer bond coupon adjustment excess 
coupon(s) withdrawn on user defined date. 
SMEM MuniBearerBondCouponAdjustmentExcessCoupons 
DepositedOn 
Muni bearer bond coupon adjustment excess 
coupon(s) deposited on user defined date. 
SMMM MuniBearerBondCouponPositionAdjustedForDepositActivity Muni bearer bond coupon adjustment-your 
interim position was adjusted for deposit 
activity 
SNNG AdjustmentForCashOnIncreasedShares Adjustment for cash on increased [[shares]] 
due to a [[Stock]] distribution payable. 
SOP2 OptionalDividendAllocationAdjustment Optional [[Dividend]] (ops) allocation-related 
adjustment. 
SPCP DTCCClaimAgainstRegisteredHolderInTheNameOfYour 
Customer 
[[DTCC]] claim against registered holder in the 
name of your customer. 
SPFS ProceedsFromSaleOf Proceeds from sale of. 
SPGP DTCCClaimAgainstRegisteredHolderInTheNameofYour 
Goodselves 
[[DTCC]] claim against registered holder in the 
name of your goodselves. 
SPNP DTCCClaimAgainstRegisteredHolderInTheNameOfYour 
NomineeLateTransfer 
[[DTCC]] claim against registered holder in the 
name of your [[nominee]]. 
SPRA WrongRatePrincipal The principal previously paid to you was at 
the wrong rate. This adjustment is to correct 
that erroneous payment. 
SRAH AdjustmentForWrittenInquiry This adjustment is in response to your written 
inquiry. 
SRDA ChangeInTheRecordDate Allocation adjustment due to a change in the 
record date. 
SRIH ThisAdjustmentIsInResponseToYourInquiry This adjustment is in response to your 
inquiry. refer to control number: 
SRPO RepPayment/Charge Rep payment or charge. 
SRPP SupplementalInterimActivity Supplemental interim activity related 
adjustment. 
SPRG InLieuofReorgDepositActivity This adjustment represents credits/debits to 
your account in lieu of reorg deposit activity. 
SRTA RateChange This allocation was adjusted for a rate 
change. Please refer to DIVA comment field 
for additional information. 
SSA6 PriceCorrectionDividendReinvestment Allocation adjustment for [[Dividend]] 
reinvestment due to price correction by the 
agent. 

---

## Page 82

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 82 
 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
SSBK CashDueOnAnAccruedStockPayment Adjustment for cash due on an accrued [[Stock]] 
payment. 
SSC6 DividendReinvestmentAllocation [[Dividend]] reinvestment allocation why not on 
normal event. 
SSCK CashDueOnaStockDividend Accrued cash due on a [[Stock]] [[Dividend]] 
adjustment made on user defined date. 
SSD6 AdjustmentToYourDividendReinvestmentPosition Adjustment to your [[Dividend]] reinvestment 
(DRP) position related adjustment. 
SSDK CashDueOnDRPShareAllocation Accrued cash due on DRP share allocation. 
SSE6 DividendReinvestmentAllocationOfCash-In-LieuOfFractions [[Dividend]] reinvestment (DRP) allocation of 
cash in lieu of fractions related adjustment. 
SSJJ AdjustmentForCash-In-LieuOfFractionalShares Adjustment for [[Cash-in-Lieu]] of fractional 
[[shares]] related adjustment. 
SSLA StockLoanAdjustment [[Stock]] loan related payment or charge. 
SSME SupplementalInterimActivityFromMidwest Supplemental interim activity from Midwest 
(6942). 
SSP4 ProceedsfromBuyTransactionInOurDTCCDividendTrading 
Account 
Proceeds resulting from a (buy) transaction 
affected in our [[DTCC]]/[[Dividend]] trading 
account (#428-10288-1-3-039). 
SSPE SupplementalInterimActivityFromPhiladelphia Supplemental interim activity from 
Philadelphia (6070). 
SSPO StockLoanorRepoPaymentOrder [[Stock]] loan or repo payment order related 
adjustment. 
SSR4 ShareAdjustmentFromABuyTransactionInOur 
[[DTCC]]/DividendTradingAccount 
Share adjustment resulting from a (buy) 
transaction affected in our [[DTCC]]/[[Dividend]] 
trading account (#428-10288-1-3-039). 
SSR5 ShareAdjustmentResultingFromASellTransactionAffectedIn 
OurDTCC/DividendTradingAccount 
Share adjustment resulting from a (sell) 
transaction affected in our [[DTCC]]/[[Dividend]] 
trading account (#428-10288-1-3-039). 
SSR6 ChargeInLieuOfReceiptOfDividendReinvestment As per your authorization, we are charging 
your account in lieu of receipt of [[Dividend]] 
reinvestment related [[shares]] related 
adjustment. 
SSRJ AllocationAdjustmentDueToFractionsRoundedUpBy 
TheAgent 
Allocation adjustment due to fractions 
rounded up by the agent related adjustment. 
SSS5 ProceedsResultingFromaSellTransactionAffectedInOurDTC 
C/DividendTradingAccount 
Proceeds resulting from a (sell) transaction 
affected in our [[DTCC]]/[[Dividend]] trading 
account (#428-10288-1-3-039) 
SSS6 DividendReinvestmentAllocationAdjustmentDueToYourSub 
AccountingInstructionsToTheAgent 
DRP allocation adjustment due to your sub 
accounting instructions to the agent. 

---

## Page 83

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 83 
 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
SST6 AllocationOfDRPTEDSInstruction Allocation of [[Dividend]] reinvestment [[shares]]- 
DRP/TEDS instruction @100%. 
STEA TaxExemptInstructions To adjust allocation at 100% on your tax 
exempt instructions. 
SWG1 LostCertificateWasRegisteredInTheNameOfYourCustomer Withdrawal by transfer-lost certificate over 
the record date was registered in the name 
of your customer. 
SWHT RecordDatePositionAdjustedForaWithdrawalByTransfer Our record date position was adjusted for a 
withdrawal by transfer activity 
SWL1 AdjustmentForaWithdrawalByTransferNotTransferredInto 
YourClientsName 
Adjustment made for a withdrawal by transfer 
that was not transferred into your clients 
name by the record date. 
SWM1 AdjustmentMadeForaWithdrawalByTransferSetUpAfterThe 
CutOffDateMadeTransferIntoYourClientsName 
Adjustment made for a withdrawal by transfer 
set up after the cutoff date made transfer into 
your client’s name. 
SWN1 PositionReinstatedCertificate(s)IssuedandOutstandingIn 
TheNameOfYourCustomer(s) 
Your position was reinstated for a withdrawal 
by transfer. However, the certificate(s) were 
issued and outstanding over the record date 
in the name of your customer(s). 
SWRH ReversalOfaWithdrawalByTransfer Reversal of a withdrawal by transfer 
adjustment. 
SWTA WithholdingTaxAdjustmentinUserDefinedCountry Adjustment to allocation to charge [user 
defined percentage] withholding tax in [user 
defined] country. 
SAA7 UnfavorableRateMerger Your account is being credited at the 
unfavorable rate (20%) as a result of the 
reorg merger paid on 4/2/93 (Armstrong 
Pharm to Medeva plc, eff 1/15/93; if entitled 
to the favorable rate (15%), you must follow 
attached. 
SAFR FractionalRights Allocation of fractional rights. 
SBB3 DWACAdjustment Your record date position was adjusted for a 
[[DWAC]] withdrawal to effect a buy- 
back/treasury purchase 
SFL9 ForeignCashDividendUnfavorableRate Foreign cash dividends allocation at 
unfavorable rate. 
SFRO FrozenLetterMovement As per memo requesting a frozen letter 
movement from [[participant]] (#). 
SRRA VodaphoneADR [[Option]] to receive Vodafone Group ADRs at 
11.354392 for every 100 ADRs.m 

---

## Page 84

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 84 
 
ISO 
Code 
SubReasonCodeName Sub Reason Code Description 
SRTJ AdditionalRightsforBeneficialOwner Distribution of additional rights for round up 
of fractions as requested for your beneficial 
owners. 
SSDJ BabyBondPayment Bond pays in baby [[Bonds]] that are issued in 
minimum/incremental denominations; this is 
to adjust for the amount of pending unissued 
[[Bonds]]. 
SSFR DueBillReversal Due bill fail tracking reversal. 
SSFF DueBillFailTracking Due bill fail tracking. 
SSOS SpinOffAllocation Allocation of spinoff security. 
SSPA PaynInKindDistribution Allocation of a Pay in Kind distribution. 
SSPJ AgentPaidBasedOnCombinedFractions Agent paid [[DTC]] based on combined 
fractions for all public service–new hamp. 
(new) spinoffs distributed on July 25, 1991. 
OTHR Other Reserved for new user defined reason 
codes. 
Unallocated Reason Codes (CAPS Message) 
The CAPS (Event Status) message is sent at any point in the [[Entitlement]]/Allocation process when an 
allocation cannot be processed. This message contains a reason code to explain why the payment was not 
made. 
Values for the ISO reason codes include the following: 
ISO Code Unallocated Adjustment Reason Code 
ISO Name 
Unallocated Adjustment Reason Code Description 
SAGA GracePeriod Company is taking a 30 day grace period 
APRR ApproximateRate Rate is approximate and not final 
ANNG BadAnnouncement Incorrect announcement 
BDPD BadPayableDate Incorrect payable date 
CSHR CashRateUnknown Cash rate for allocation is not known 
COND ConditionalPayment Payment is conditional and conditions have not been met yet 
DFLT [[default]] Issue is in [[default]] 
ANFI FundsNotReceivedByAgent Funds were not received by the agent 
HICO HolidayInCountryOfOrigin Holiday in country of origin 
MASF InsufficientFundsReceivedFromAgent Insufficient funds were received from the agent 

---

## Page 85

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 85 
 
ISO Code Unallocated Adjustment Reason Code 
ISO Name 
Unallocated Adjustment Reason Code Description 
ISNF IssueNotFunded Issue was not funded 
NMAT IssueNotMaturing Issue is not maturing 
LFID AfterCycleCutOff Issues funded and/or identified after the cycle cut off 
PEND ItemIsPending Item is pending 
LIQD [[liquidation]] Issue is being liquidated 
NOTL NotionalBalance Notional balance principal will not be paid 
OTHR Other Reserved for new user-defined reason codes 
PCHK PaidUponReceiptOfCheck Paid upon receipt of check 
RRFX PendingConversionOfFunds Pending conversion of funds 
RCNF RecapitalizationNotFunded Recapitalization: issue not funded 
RRNF RedemptionOfRatesNotYetFunded Redemption of rates: issue not funded 
RPLG ReleasedPledgePosition Released pledge position 
SANF SaleOfAssetsNotYetFunded Sale of [[Asset]]: issue not funded 
SDPC SameDayPositionCapture Same day position capture 
SPNF SpecialDistributionNotYetFunded Special distribution: issue not funded 
PUVF SpecificIssuesSuppressed Specific issues have been suppressed 
OTHR vs. NPAY ISO Codes 
The ISO reason codes NPAY and OTHR both refer to codes that exist outside of the ISO code set.  
When an event comes in with a reason code that is entirely unknown (such as one that has been created by a 
client in response to a specific, emergent reason), the ISO reason code “OTHR” is assigned. This signifies the 
existence of an undefined code for not allocating on an event. 
[[DTCC]] has a set of more specific extension codes that are recognized by CA Web. These codes account for 
more situations than are covered by the ISO codes. When CA Web recognizes a reason code from this 
extension set transmitted on an event, it assigns “NPAY” as the ISO code. In these cases, NPAY will be 
mapped to the core of the message and the corresponding, more granular [[DTC]] reason code (listed below) will 
be mapped to the extension. 

---

## Page 86

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 86 
 
ISO Code 
Pending/ 
ReasonCode/ 
Code 
[[DTC]] Reason Code 
Unallocated ReasonCode 
(extended) 
Description Notes 
NPAY ANFI Funds not received by agent n/a 
NPAY ANNG Bad announcement For redemptions only. 
NPAY APRR Approximate rate Rate of distribution is still 
approximate. 
NPAY BDPD Bad payable date For dividends: the pay date is 
incorrect and will not be known until 
the overnight allocations process 
occurs. The announcement gets 
updated, but allocations will not be 
updated until the end-of-day 
process takes place. 
NPAY COND Conditional payment For redemptions: Payment may 
happen but it is conditional upon 
certain requirements. 
NPAY CSHR Cash rate zero For redemptions and distributions: 
this code communicates when the 
cash rate is “0.” 
NPAY DFLT Issue in [[default]] n/a 
NPAY FX Pending conversion of funds For Canadian issues where 
Canadian dollars are converted to 
U.S. dollars. 
NPAY HICO Holiday in country of origin The pay date is accurate but 
funding is disallowed because the 
pay date falls on a holiday. 
NPAY ISNF Issue not funded A general code that appears until 
funding is received. 
NPAY LFID Issues funded or identified after 
cutoff 
This code is used when [[DTCC]] gets 
funded after cutoff time. [[DTCC]] will 
allocate on the next business day. 
NPAY LIQD [[liquidation]] A [[liquidation]] cash event. Automatic 
payment will be suppressed 
although the money comes in and 
matches. [[DTCC]] must manually 
release the payment. 
NPAY MASF Insufficient funds received to 
allow allocation 
Funds need to reach a particular 
threshold before they can be 
allocated. This code is used when 
funds have not reached that 
threshold. 
NPAY NMAT Issue not maturing For redemptions only. 

---

## Page 87

User Guide: ISO 20022 MESSAGING FOR DISTRIBUTIONS ENTITLEMENTS AND ALLOCATIONS 
 
Appendix A: Reason Codes 87 
 
ISO Code 
Pending/ 
ReasonCode/ 
Code 
[[DTC]] Reason Code 
Unallocated ReasonCode 
(extended) 
Description Notes 
NPAY NOTL Notional balance/no principal 
payment 
For redemptions only: used for 
interest-only products. 
NPAY PCHK Paid upon receipt of check Funding sometimes takes place by 
check. This code indicates that the 
allocation will be paid when the 
check is received. 
NPAY PEND Item is pending This code is not used in cases 
where a company is going out of 
business and the issuing agent 
cannot pay due to potential 
insolvency. 
NPAY PUVF Paid upon verification of funds n/a 
NPAY RCNF Recapitalization-not funded Similar to LIQU. 
NPAY RESC Call rescinded For redemptions only. 
NPAY RPLG Released pledge position For redemptions only. 
NPAY RRNF Redemption of RTS-not yet 
funded 
For redemptions only. 
NPAY SANF Sale of assets-not yet funded Used for [[ADR]] payments. 
NPAY SDPC Same-day position capture item “Same-day” applies until 1:45 p.m. 
daily. 
NPAY SPNF Special distribution-not yet 
funded 
Similar to LIQU. 
NPAY 30DG 30-day grace period n/a 
NPAY OTHR Other This code applies to ISO 20022 
messaging only. It appears in a 
message when a user requires a 
code for unforeseen circumstances 
that are not represented by a 
current code. 
NSEC n/a End of day SDARSTK 
unallocated records 
All [[Stock]] distributions that did not 
allocate are reported on the last 
SDARSTK. The ISO equivalent is 
sent out with NSEC. 
 
 

---

## Page 88

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 