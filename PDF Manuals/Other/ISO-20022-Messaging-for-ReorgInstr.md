---
title: "ISO-20022-Messaging-for-ReorgInstr.pdf"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO-20022-Messaging-for-ReorgInstr.pdf"
pages: 71
size: "1354.2 KB"
category: "Other"
ingested_on: "2026-06-05"
---

# ISO-20022-Messaging-for-ReorgInstr.pdf

**Original File:** [ISO-20022-Messaging-for-ReorgInstr.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/ISO-20022-Messaging-for-ReorgInstr.pdf)  
**Category:** Other  
**Total Pages:** 71  
**File Size:** 1354.2 KB  

---

## Page 1

Corporate Actions 
ISO 20022 MESSAGING FOR REORGANIZATIONS 
INSTRUCTIONS USER GUIDE 
OCTOBER 30, 2023 
[[DTCC]] Public (White)

---

## Page 2

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 2 
TABLE OF CONTENTS 
An Introduction to ISO 20022 Messaging .......................................................................................................... 5 
What is ISO 20022 Messaging? ......................................................................................................................... 5 
Benefits of Using ISO 20022 Messaging for Corporate Actions ......................................................................... 5 
How Can I Learn More? ...................................................................................................................................... 5 
Events in Scope for Corporate Action Reorganization Instructions .................................................................... 7 
Events Out of Scope for Corporate Action Reorganization Instructions ............................................................. 8 
Processors Out of Scope for Corporate Action Reorganization Instructions .................................................... 8 
Corporate Actions Messages in the Instructions Workflow ................................................................................ 9 
How to Read an MX Identifier ...........................................................................................................................10 
[[BASIC]] Message Flow of the Reorganization Lifecycle ......................................................................................11 
Lifecycle of an Instruction .................................................................................................................................12 
Date and Time for Reorganization Instruction Messages ...............................................................................13 
Cano Message Elements ................................................................................................................................... 14 
CANO Message Elements: All Events ..............................................................................................................14 
CANO Message Elements: Tender and Exchange Events ..............................................................................16 
CANO Message Elements: Rights Exercise Events .........................................................................................17 
Date Fields Applicable to Reorg Instructions ....................................................................................................18 
Cain Messages ................................................................................................................................................... 19 
What Is a CAIN Message? ...............................................................................................................................19 
General Rules ...................................................................................................................................................19 
Tender and Exchange Event Instructions .........................................................................................................20 
Event Types in Scope .....................................................................................................................................20 
[[Option]] Types in Scope ....................................................................................................................................21 
Mandatory Fields within all Tender / Exchange events processed via PTOP ................................................22 
Optional Fields based on Event Details ..........................................................................................................24 
Event Condition Rules for Tender and Exchange Instructions .......................................................................25 
Tender and Exchange Events Involving Shareholder Number (Allocation Codes)  ........................................26 
Narrative within the CAIN for Tender and Exchange Events ..........................................................................26 
Shareholder Number (allocation code) ...........................................................................................................26 
[[DTCC]] Public (White)

---

## Page 3

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 3 
Event Scenarios for Tender and Exchange Events ........................................................................................26 
Dutch Auction / Sealed Tender / Bid Tender .................................................................................................26 
Bid Price Rules: ............................................................................................................................................26 
Unspecified Price .........................................................................................................................................27 
Modified Dutch Auctions ..............................................................................................................................28 
Odd Lot Priority Flag (OPLF) .........................................................................................................................28 
Tender and Exchange events involving Conditional Quantity .......................................................................28 
Full Conditional [[Option]] Scenarios .................................................................................................................28 
Canadian Currency Options Scenario ...........................................................................................................28 
Submitting a Protect, Cover Protect Instruction for Tender and Exchange Events .......................................29 
Rules Regarding Protect / Cover Protect instructions .................................................................................29 
Required ISO Fields .....................................................................................................................................29 
Rights Exercise Events ...................................................................................................................................29 
Mandatory Fields for Rights Events ...............................................................................................................29 
Transaction Sequence (Extension) ...............................................................................................................31 
Optional Fields for Rights Events ..................................................................................................................32 
Rights Exercise Event Instruction Rules ........................................................................................................33 
Submitting a Protect or Cover Protect Instruction for Rights Events .............................................................34 
Required ISO Fields .....................................................................................................................................34 
Rules Regarding Protect / Cover Protect instructions for Rights Events ......................................................34 
Canadian Currency Options Scenario .........................................................................................................35 
PUT Event Instruction General Rules .............................................................................................................35 
Mandatory Fields for events processed via PUTS ........................................................................................36 
CAIS Messages................................................................................................................................................... 38 
What Is a CAIS message? ................................................................................................................................38 
CAIS messages for instructions submitted via [[PTS]] / [[PBS]] ...............................................................................38 
Instruction Cancellations ...................................................................................................................................39 
CAIS messages for Events Cancelled in the Market ......................................................................................39 
CAIS messages for Instructions Withdrawn by the Client ...............................................................................39 
CAIS messages for Instructions Cancelled by the System .............................................................................39 
[[DTCC]] Public (White)

---

## Page 4

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 4 
CAIS message for Instructions Requiring Agent Approval .............................................................................39 
Information Contained on the CAIS Message ..................................................................................................39 
CAIS Reject Codes ...........................................................................................................................................44 
Instruction Processing Status: Rjctd (Rejected) ..............................................................................................44 
CAIC Messages .................................................................................................................................................. 54 
What Is a CAIC Message? ...............................................................................................................................54 
General Rules ...................................................................................................................................................55 
Fields in CAIC Core Message .........................................................................................................................56 
Fields in CAIC Supplement Message .............................................................................................................57 
What is a CACS Message? ..............................................................................................................................58 
Information Contained on the CACS Core Message ........................................................................................59 
Information Contained on the CACS Supplemental Message .........................................................................60 
CACS Reject Codes .........................................................................................................................................60 
Instruction Processing Status: Rjctd (Rejected) ..............................................................................................60 
Appendix A: Instruction Messaging Eligibility ................................................................................................ 63 
Revision History ................................................................................................................................................. 69 
[[DTCC]] Public (White)

---

## Page 5

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 5 
AN INTRODUCTION TO ISO 20022 MESSAGING 
The primary purpose of this user guide is to familiarize participants with ISO 20022 Messaging for Corporate 
Action Instructions. This guide is not intended to serve as a legal document. No statement in this guide should 
be construed as a legally binding rule or [[regulation]], or as creating an obligation on the part of [[DTCC]] or any of 
its subsidiaries. In addition, any time schedules or time requirements set forth herein are subject to change 
without notice. 
This guide is meant as an educational tool to assist in your understanding of ISO 20022 messaging as it 
relates to corporate action processing at [[DTCC]]. It should not be used as a basis for systems applications 
coding. For coding purposes, please refer to specific schemas and message implementation guides that can 
be found on found on the “ISO 20022 Messaging Specifications” page on [[DTC]] c.com. 
What is ISO 20022 Messaging? 
ISO 20022 is an international messaging standard that is designed to simplify global business communication 
by creating a common language for communicating financial information that is unrestricted by national borders 
or regional conventions. Since 2013, [[DTC]] has been moving its corporate actions processing from proprietary 
formats to this ISO messaging standard. The final set of messages to be converted are instruction messages 
for reorganization events. 
Even though the Depository has maintained its own proprietary formats since its creation in 1973, [[DTC]] 
recognized that it needed to respond to an evolving business environment and to accommodate an 
increasingly global investment business. [[DTC]]'s participants and customers had expanded their businesses 
throughout the world and wanted to streamline, as much as possible, the standards and formats used to 
communicate. ISO 20022 meets those needs and offers a host of benefits.  
Benefits of Using ISO 20022 Messaging for Corporate Actions 
One of the greatest benefits of ISO 20022 is its consistency and universality across the industry and around 
the globe. It provides a common language with its own ever-growing dictionary that allows businesses in the 
financial industry to communicate corporate action information quickly, easily, and precisely. Considering that 
approximately 200 [[DTCC]] customers submit about 600,000 reorganization instructions in a single year, ISO 
20022 messages are powerful tools for risk mitigation. 
How Can I Learn More? 
The [[DTCC]] Learning Center website provides a wealth of information about Corporate Actions Processing and 
ISO 20022 Messaging. You can either search for the content you want from its home page (see image below) 
or navigate to [[Asset]] Services > Corporate Actions Processing > ISO 20022 Messaging  via the Main 
Products & Services Menu to learn more. The [[DTCC]] Learning Center hosts videos, documentation, answers 
to FAQs, and other resources regarding ISO 20022 messages and message scenarios.  
[[DTCC]] Public (White)

---

## Page 6

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 6 
 
Be s ure to register and log in with your account to access all the available content. 
[[DTCC]] Public (White)

---

## Page 7

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 7 
Events in Scope for Corporate Action Reorganization Instructions 
Processors Event Type Code Event Code 
PSOP Rights Subscription AC 59 EXRI 
PTOP Exchange AC 52 EXOF 
PTOP Tender AC 52 TEND if Offeror / 
BIDS if [[issuer]] 
PTOP Mini-Tender AC 52 NOOF 
PTOP Consents AC 52 CONS 
PTOP Dutch Auctions AC 52 DTCH 
PTOP Conversions AC 52 CONV 
PTOP [[Warrants]] AC 52 EXWA 
PTOP Odd Lot Offers AC 52 ODLT 
PTOP Redemption of Rights AC 52 OTHR 
PTOP Reorganization AC 52 OTHR 
PTOP Put AC 52 BPUT 
PTOP Mergers with Elections AC 52M MRGR 
PUTS Optional Repayments AC 58 AC 58B BPUT 
PUTS Mortgage-Backed Puts AC 62 AC 62B BPUT 
PUTS Mandatory Tender with the Right to 
Retain 
AC 65B/R BPUT 
PUTS Survivor [[Option]] Puts AC 66P BPUT 
[[DTCC]] Public (White)

---

## Page 8

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 8 
Events Out of Scope for Corporate Action Reorganization 
Instructions 
Event Type Code Event Code 
Voluntary Non-[[DTC]] AC 52N BIDS if [[issuer]] / TEND if Offeror 
CD Early Redemptions AC 53 REDM 
Conversions AC 54 CONV 
Conversion Non-[[DTC]] AC 54N CONV 
Repayment Non-[[DTC]] AC 58N BPUT 
Redemption of Rights CA 52N OTHR 
Event Type Code Event Code 
Warrant Subscriptions AC 60 EXWA 
Warrant Subscription Non-[[DTC]] AC 60N EXWA 
Processors Out of Scope for Corporate Action Reorganization Instructions 
Processor Notes 
CERR (CD Early Redemptions)  
Available in a future ISO release 
WARR (Warrant Exercise) 
Available in a future ISO release 
RCNV (Conversion Instructions) Available in a future ISO release 
RTOP (Voluntary Instruction Release) 
No immediate plans for modernization. VRI does not have 
maker/checker capability. 
IVORS (Investors Voluntary Redemptions / Sales)  
No immediate plans for modernization 
CMOP (Change Mode of Payment) 
No immediate plans for modernization 
[[DTCC]] Public (White)

---

## Page 9

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 9 
Corporate Actions Messages in the Instructions Workflow 
There are fifteen types of messages in the ISO 20022 group: 
MX Identifier ISO 20022 Message 
Names 
Extension (SD) Short 
Name 
Equivalent ISO 
15022 
Equivalent [[DTCC]] 
Processes 
seev.031.002.XX CA Notification supl.001.001.XX CANO MT 564 Announcements 
seev.039.002.XX CA Cancellation Advice supl.006.001.XX CACN MT 564 Announcement 
Cancellations 
seev.031.002.XX CA Notification with Eligible 
Balance 
supl.007.001.XX CANO-E MT 564 Record Date 
Entitlements 
seev.035.002.XX CA Movement Preliminary 
Advice 
supl.009.001.XX CAPA MT 564 Projected Payments 
seev.044.002.XX CA Movement Preliminary 
Advice Cancellation Advice 
supl.034.001.XX CAPC MT 564 Projection Cancellation 
seev.036.002.XX CA Movement Confirmation supl.011.001.XX CACO MT 566 Allocations / Payments 
seev.037.002.XX CA Movement Reversal 
Advice 
supl.025.001.XX CARE MT 566 Payment Reversal 
Advice 
seev.032.002.XX CA Event Processing 
Status Advice 
supl.010.001.XX CAPS MT 567 Unallocated Positions 
seev.033.002.XX CA Instruction supl.008.001.XX CAIN MT 565 Instructions / Elections 
seev.034.002.XX CA Instruction Status 
Advice 
supl.030.001.XX CAIS MT 567 Instruction Reply 
seev.040.002.XX CA Instruction Cancellation 
Request 
supl.032.001.XX CAIC MT 565 Instruction Withdrawal 
seev.041.002.XX CA Instruction Cancellation 
Request Status Advice 
supl.033.001.XX CACS MT 567 Withdrawal Reply 
seev.042.002.XX Corporate Actions 
Instruction Statement 
Report 
supl.031.001.XX CAST n/a Instruction Statement 
Report 
seev.001.001.XX Meeting Notification n/a MTNO MT 564* Announcements (AC 80) 
seev.002.001.XX Meeting Cancellation n/a MTCN MT 564* Announcements (AC 80) 
Cancellations 
*Limited. Not backwards compatible 
The messages specifically involved in the instructions process are: 
• Corporate Action Announcement Message (CANO) 
• Corporate Action Instruction Message (CAIN) 
• Corporate Action Instruction Status Advice Message (CAIS) 
• Corporate Action Cancellation Request Message (CAIC) 
[[DTCC]] Public (White)

---

## Page 10

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 10 
• Corporate Action Cancellation Status Advice Message (CACS) 
• Corporate Action Statement Report Message (CAST) 
The CANO message is an essential component of the instruction process in that it outlines the critical elements 
of the event such as identifier and [[Option]] numbers, among others. Information from the CANO message 
informs the primary messages involved in the Instructions processes: CAIN, CAIC, CAIS, CACS, and CAST.  
How to Read an MX Identifier 
The MX Identifier identifies the business area, message [[ID]], and version of an ISO Message.  
As an example, for the identifier seev.033.002.09: 
• The first four alphabetic characters (“seev”) identify the business area. In this case, it is “[[securities]] 
Events.” You may wish to visit the official ISO 20022 (Universal Financial Industry Message Scheme) 
website for additional information. 
• The next three characters (033) are the message identifier. The message in this example is a CAIN 
message. 
• The next three characters (002) are the “variant” identifier. Since “001” is always the main ISO message, 
“002” would be the second variant (and the one that is compatible with ISO 15022). [[DTC]] is using the 
second variant to comply with the industry’s requirement that the ISO 20022 messages we generate be 
backward compatible with ISO 20022. 
• The last two characters (09) are the “version.” In this example, this is the ninth version of this message, 
representing SR 2019. 
For your coding purposes, be sure to consult the “ISO 20022 Messaging Specifications”  page on [[DTCC]].com. 
[[DTCC]] Public (White)

---

## Page 11

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 11 
[[BASIC]] Message Flow of the Reorganization Lifecycle 
The following graphics provide a high-level view of the [[BASIC]] flow of the reorganization event lifecycle. 
Note: 
Throughout this document, blue boxes represent inbound instructions to [[DTC]] from the [[participant]] and green boxes 
represent outbound instructions to the [[participant]] from [[DTC]]. 
 
OR 
 
1. [[DTC]] sends a CANO to the [[participant]] that announces the corporate action event. The CANO contains an 
indicator signaling that the event is eligible for ISO 20022 instruction messaging.  
Note: 
The CANO messages are not discussed at length in this User Guide as they are announcement messages only. 
2. [[DTC]] sends a follow-up message (CANO-E) to inform the [[participant]] about how it is specifically affected by 
the corporate action: its eligibilities and options. 
3. The [[participant]] submits instructions for that event, either via a CAIN message or via PTOP, PSOP, or 
PUTS input. 
4. [[DTC]] sends a CAIS message containing status information about the instructions back to the [[participant]].  
[[DTCC]] Public (White)

---

## Page 12

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 12 
5. After all actions specified in the CAIN (and any in the follow-up messages not specified in this flow) have 
been taken, [[DTC]] sends the [[participant]] a CACO message to confirm movement of payment/allocation 
proceeds. 
For specific message information, visit the ISO 20022 Messaging Specifications  page on [[DTCC]].com or view the 
Resources tab in the Learning Center’s ISO 20022 Messaging section. 
Lifecycle of an Instruction 
The following diagram illustrates the gateways that an instruction must pass through to advance through the 
system. 
 
After a CAIN message has been submitted to [[DTC]], the [[participant]] / sender initially receives an ACK / NAK 
message confirming receipt of the instruction. 
• If there is a subscription failure or a schema validation issue, a Not Acknowledged (NAK) message will be 
returned and a new instruction must be sent. 
• Otherwise, the message will be Acknowledged (ACK). 
Please note that for instructions submitted close to the expiration time of the event, an ACK message confirms 
that [[DTC]] has received the instruction and will act upon it (see (1) in the diagram. Reception of the ACK 
message means that [[DTC]] has taken ownership of the instruction). 
After the ACK is generated, the message undergoes business validation rules checking the instruction details 
for the offer. If the instruction fails business rule validation, a CAIS Reject message is sent (2) . If it passes 
business rule validation, then a CAIS Pending (PEND) message is sent to the user (3) . 
[[DTCC]] Public (White)

---

## Page 13

ISO 20022 Messaging for Reorganizations Instructions User Guide 
AN INTRODUCTION TO ISO 20022 MESSAGING 13 
Note: 
Instructions sent close to the [[DTC]] Instruction expiration date and time may still be rejected even if you receive an initial 
ACK message described above. 
Finally, the instruction checks the event for position validation. If there is sufficient account position for the 
event, then the instruction is accepted and a CAIS Accepted status message is sent (4) . Position will be moved 
from your general free account to the Contra position (for Tender and Exchange events) or RRG account (for 
Rights events). For PUTS events, the position will move either into a Contra [[CUSIP]] or RRG based on the Put 
Event type. 
Instructions with no position will recycle and a PEND message is sent with a Recycle (RECY) extended reason 
code. This recycling occurs until Recycle Cutoff time (1:30 p.m. or 3:30 p.m.) for that event, at which point a 
PEND / LACK (5) will be generated. 
• If [[DTC]] does not receive position by the recycle cutoff time, then the instruction is dropped and a CAIS 
Reject message is sent with a transaction identification status of REJT / DROP.  
If [[DTC]] receives position before the Recycle Cutoff time, the instruction becomes “made” and a CAIS Accepted 
message is sent with an extended transaction identification status of MADE. If position is not received by the 
Recycle Cutoff Time, then a CAIS Reject message is sent with a transaction identification status of DROP. 
Processing Periods and Expiration Information 
Date and Time for Reorganization Instruction Messages 
Processor cutoff times and submission times for ISO 20022 Reorganization instruction messaging largely 
remain the same and are outlined below. 
Function Activity Codes Processor Start Time Processor Cutoff Time Notes 
PTOP 52 and 52M 01:00:00 a.m. 05:00:00 p.m. 
06:00:00 p.m. 
On selective events 
with midnight closing 
and only on the [[DTC]] 
Instruction Expiration 
Date 
PUTS 58, 58B, 62, 62B, 
65B, 65R, and 66P 
07:00:00 a.m. 01:00:00 p.m. 
05:00:00 p.m. 
All activity codes listed 
except 66P. 
Put (Survivor Options) 
only (66P) 
PSOP 59 08:00:00 a.m. 02:15:00 p.m. 
05:00:00 p.m. 
Start Time and Cutoff 
Time are specified on 
the event. On selective 
events and only on the 
[[DTC]] Instruction 
Expiration Date, the 
cutoff time may be 
extended from  
03:30:00 PM to 
05:00:00 PM. 
[[DTCC]] Public (White)

---

## Page 14

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CANO MESSAGE ELEMENTS 14 
CANO MESSAGE ELEMENTS 
Elements of the CANO messages inform the ISO 20022 messages involved in the instruction process for 
reorganization events. 
CANO Message Elements: All Events 
Field Name Notes Tag(s) 
Instruction Messaging 
Eligibility Flag 
To determine whether an event is eligible for 
ISO 20022 reorganization instruction 
messaging, an indicator "Instruction 
Messaging Eligibility Flag" will be published 
in CANO SD for all Mandatory, Voluntary 
Reorg and Choice Events. If the event is not 
eligible, the flag is set to "false;" otherwise, 
eligible events are set to “Yes.” Please see 
the attached table for a list of event types in 
the former and current models. This flag is 
visible in the last column of the table. 
/Document/DTCCCANOCSDDataSD1/ 
CorpActnGnlInf/InstrMsggElgbltyFlg 
See Appendix A f or rules regarding the instruction 
messaging eligibility flag. 
[[DTC]] Automated Offer 
Program 
Indicator that identifies the type of interface 
an event agent has with [[DTC]] (The 
Depository Trust Corporation) for all events 
processed on PTOP. It defines how time 
sensitive instruction and withdrawal process 
is. Offline (non-automated) agent will have 
earlier deadlines which will be reflected in 
response deadlines but importantly 
withdrawal procedures for manual agent 
require hard copy sign off from the agent 
that has to be delivered to [[DTC]] to proceed 
with withdrawal. Deadline for Online agents 
will be 5:00pm eastern time and for Offline 
1:00 pm eastern time unless otherwise 
indicated within external comments 
(narrative). 
/Document/DTCCCANOCSDDataSD1/ 
CorpActnDtls/DTCAutomtdOfferPrgm/Online or 
Offline 
Odd Lot Priority Flag Some offers stipulate that instructions 
submitted on odd lot positions will be 
exempted from any proration if submitted in 
full. This indicator identifies whether the 
exemption is in effect. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
OptnFeatrs/Cd/OPLF 
[[DTCC]] Public (White)

---

## Page 15

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CANO MESSAGE ELEMENTS 15 
Field Name Notes Tag(s) 
Back End Odd Lot 
Quantity 
Determines the disposition of odd lot 
quantities resulting from proration. 
Depending on the event, while the initial 
instruction may be accepted (ACK / MADE), 
if, after proration, the remaining quantity 
(instructed quantity less accepted prorated 
quantity) is an odd lot, the final disposition of 
the instruction will not be known until the 
offer expires and depends on the rules 
established by the [[issuer]] to either (a) accept 
the instruction in full, (b) reject the 
instruction or (c) accept amount that returns 
the minimum back to the target. Note, the 
rule may apply to the underlying position – 
i.e., if the position to be received is an odd 
lot, acceptance will depend on the rule (a), 
(b) or (c). 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
SctiesQty/BckEndOddLotQty/Unit or FaceAmt 
Maximum Quantity to 
Instruct 
[[Option]] is applicable only for positions below 
and including this quantity. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
SctiesQty/MaxQtyToInst/Unit or FaceAmt 
Minimum Quantity to 
Instruct (Minimum 
Instruction 
Denomination) 
Identifies that the [[Option]] is applicable only 
for positions above and including this 
quantity. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
SctiesQty/ MinQtyToInst/Unit or FaceAmt 
Minimum Multiple 
Quantity to Instruct 
(Multiple Instruction 
Amount) 
Indicates whether the instructions have to 
be submitted in multiples of a certain 
quantity. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
SctiesQty/MinMltplQtyToInst/Unit or FaceAmt 
[[DTC]] Recycle Cutoff 
Indicator 
Indicates whether the recycling of 
instructions for eligible positions is set to 
end early or late at [[DTC]]. 
Anticipated Early Cutoff [AERL] - Cut-off 
may change to early. 
Early [EARL] - Cut-off occurs before the 
[[DTC]] standard [[settlement]] cut-off. Early cut- 
off usually 130 Eastern time 
Late [LATE] - Cut-off is after [[settlement]] at 
[[DTC]]. 
/Document/DTCCCANOCSDDataSD1/ 
CorpActnDtls/DTCRcyclCutOffInd 
Conditions 1-6 For certain events, conditions may apply for 
a particular [[Option]] that need to be 
responded to in order to instruct. The 
conditions information will be maintained 
within comments and in the CANO within 
the Additional Information / Information to 
Comply With. The condition number, the 
terms of condition and a Required Y/N is 
output. If the Required Indicator is Y, then 
the condition number must be instructed as 
Y in order to participate in that [[Option]]. 
/Document/DTCCCANOCSDDataSD1/OptnDtls/ 
OptnConds/CondNb 
/Document/DTCCCANOCSDDataSD1/OptnDtls/ 
OptnConds/CondTxt 
/Document/DTCCCANOCSDDataSD1/OptnDtls/ 
OptnConds/CondReqrdFlg 
Number of Conditions Number of conditions for a given [[Option]] that 
must be acknowledged upon submission of 
instruction for voluntary reorganization 
events. 
/Document/DTCCCANOCSDDataSD1/ 
OptnDtls/NbOfConds 
[[DTCC]] Public (White)

---

## Page 16

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CANO MESSAGE ELEMENTS 16 
CANO Message Elements: Tender and Exchange Events 
Field Name Notes Tag(s) 
Maximum 
Price 
For Bid Tender or Dutch Auction events, maximum 
price at which a holder can bid 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
PricDtls/MaxPric 
Minimum 
Price 
For Bid Tender or Dutch Auction events, minimum 
price at which a holder can bid 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
PricDtls/MinPric 
Bid Interval Acceptable price increment used for submitting a bid. 
The acceptable prices as dictated by the terms of the 
offer and presented on the Letter of Transmittal LT) 
are either (a) fully divisible by the increment from the 
minimum up to the maximum (inclusive of min and 
max), [10.20, 10.30, 10.40, 10.50, 10.60] (b) multiples 
of the increment (excluding the minimum to the 
maximum), [10.22, 10.30, 10.40, 10.50, 10.60, 10.62 
or (c) incremental from the minimum to the maximum 
[10.22, 10.32, 10.42, 10.52, 10.62] 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
RateAndAmtDtls/BidIntrvl 
Unspecified 
Bid Price 
Indicates that the [[Option]] for a Dutch Auction requires 
acknowledging the instruction to be of an unspecified 
price (UNSP) which means you are not indicating a 
price and are deemed to have bid at the lowest price. 
For a Modified Dutch Auction, unless the notice states 
otherwise, your position instructed will be accepted at 
the “strike” price – i.e., the final accepted price (as per 
the [[issuer]]/agent) Note, it is possible that an event be 
set up where unspecified price instructions in a 
Modified Dutch Auction are not automatically accepted 
if, for instance, the offer is prorated and the cap is 
reached without accepting any of the unspecified 
instructed positions. For bid tenders, bids are normally 
accepted low to high at the price bid up to the price 
that brings the [[issuer]] to the cap (i.e., the available 
cash to be paid out in the offer). 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
CshMvmntDtls/PricDtls/GncCshPricRcvdPerPdct/ 
NotSpcfdPric/UNSP 
Proration 
Flag 
Indicator that states whether the [[Option]] is subject to 
proration. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
OptnFeatrs/Cd/PROR 
Conditional 
Tenders 
Accepted 
Flag 
Identifies event options that allow holders to submit an 
instruction conditionally (e.g., to process the instruction 
only if a minimum of 1000 [[shares]] are accepted after 
pro-ration). 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
OptnFeatrs/Cd/COND 
Shareholder 
Number 
(allocation 
code) 
Indicates usage of a reference number (provided by 
the [[issuer]]/agent) to identify qualifying [[investor]] or a 
shareholder with the [[issuer]] or the registration provider 
(for instance, allocation code) identifying the 
instruction as meeting the requirements/qualifications 
to be accepted in this [[Option]]. This code must be 
entered on an instruction if this indicator is announced 
for a particular [[Option]]. The Shareholder Number 
cannot be used in the CAIN message if the 
Shareholder Indicator is No (false). If no Shareholder 
indicator is on the CANO, a Shareholder Number 
could be sent in CAIN. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
OptnFeatrs/Cd/SHAR 
[[DTCC]] Public (White)

---

## Page 17

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CANO MESSAGE ELEMENTS 17 
Field Name Notes Tag(s) 
FULL 
Conditions 
Indicator 
If the Conditional Tenders Accepted flag equals Y, and 
the Full Conditional Flag is Y on CA Web, then the 
conditional quantity must be 0 or equal to the 
instructed quantity. 
For certain events where the acceptance could be pro-
rated, an [[Option]] may have a full condition indicator 
meaning that you must either instruct the Conditional 
Quantity in Full (equal to the Instructed quantity) or 
instruct Zero. This means if you instruct an amount 
and indicate that you wish the instruction to be 
accepted in Full ONLY or else be rejected (i.e., if the 
offer is pro-rated). If you instruct zero, this means that 
you have no conditions and will accept any quantity of 
that instruction in the offer. Please note for the initial 
release of the Instructions Project, the Full Conditions 
indicator will only be supplied via the CA Web 
announcement via the Full Conditional Flag field. 
/Document/DTCCCANOCSDDataSD1/OptnDtls/ 
FullCondFlg 
CANO Message Elements: Rights Exercise Events 
Field Name Notes Tag(s) 
Oversubscription Type Type of oversubscription for the event. 
Unlimited [UNLD] - Unlimited 
oversubscription 
Limited By Quantity Or Percentage 
[LTDB] - The subscription is limited by 
quantity or percentage. 
No Oversubscription [NONE] - No 
oversubscription is allowed. 
/Document/DTCCCANOCSDDataSD1/ 
CorpActnDtls/OvrsbcptTp 
Rights Oversubscription 
Flag 
Indicates whether holders of rights will 
be afforded the opportunity to subscribe 
to purchase extra [[shares]] that are not 
picked up by the remaining holders 
/Document/DTCCCANOCSDDataSD1/ 
CorpActnDtls/RghtsOvrsbcptFlg 
Maximum Allowed 
Oversubscription Rate 
Maximum oversubscription percentage 
for the [[Option]]. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
RateAndAmtDtls/MaxAllwdOvrsbcptRate/Rate 
Solicitation Dealer Fee Flag Indicates whether there is a solicitation 
fee on the event. This fee is paid by the 
soliciting dealer. 
/Document/DTCCCANOCSDDataSD1/ 
CorpActnDtls/SlctnDealrFeeFlg 
[[Option]] Availability Status (CANC) tells that an [[Option]] is canceled 
and not eligible for instruction. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
OptnAvlbtySts/CANC 
[[DTCC]] Public (White)

---

## Page 18

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CANO MESSAGE ELEMENTS 18 
Date Fields Applicable to Reorg Instructions 
Field Name Notes Tag(s) 
[[DTC]] Instruction Start Date The date at which the instruction 
process will open for instruction 
purposes at [[DTC]]. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
PrdDtls/ActnPrd/Prd/StartDt 
[[DTC]] Instruction Expiration 
Date (Response Deadline 
Date) 
Deadline (last day) on which the 
instruction process for this [[Option]] will 
close at [[DTC]]. 
If time is available: 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
DtDtls/RspnDdln/Dt/DtTm 
Cover Expiration Date Actual Cover Expiration Date of the 
[[issuer]] / agent. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
DtDtls/CoverXprtnDdln/DtCd/Cd 
Protect Date Last day on which a protect 
instruction can be submitted to [[DTC]]. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
DtDtls/PrtctDdln/DtCd 
Market Deadline Actual Expiration Date and Time of 
the [[issuer]] / agent for a particular 
event. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
DtDtls/MktDdln/Dt/DtTm 
Depository Cover Expiration 
Date 
Last day on which cover protects can 
be submitted to [[DTC]]. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
DtDtls/DpstryCoverXprtnDt/Dt/DtTm 
Actual Protect Expiration 
Date (extension) 
Actual protect expiration of the 
[[issuer]]/agent. 
/Document/DTCCCANOCSDDataSD1/OptnDtDtls/ 
ActlPrtctXprtnDt 
Revocability Period End 
Date (Actual) 
Used to identify instruction withdrawal 
deadline by the [[issuer]] / offeror. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
PrdDtls/RvcbltyPrd/Prd/EndDt/Dt 
Account Servicer 
Revocability Period End 
Date ([[DTC]]) 
Used to identify instruction withdrawal 
deadline by [[DTC]]. Only end date will 
be used. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/ 
PrdDtls/AcctSvcrRvcbltyPrd/Prd/EndDt/Dt/DtTm 
[[DTCC]] Public (White)

---

## Page 19

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 19 
CAIN MESSAGES 
What Is a CAIN Message? 
The Corporate Action Instruction Message (CAIN) is an inbound message sent by participants to [[DTC]] to 
communicate voluntary corporate action reorganization instructions. 
MX Identifier ISO 20022 Message 
Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTC]] 
Processes 
seev.033.002.xx1 Corporate Action 
Instruction 
supl.008.001.xx1 CAIN MT 565 Instructions/Elections 
A CAIN message is a [[participant]]’s instruction to [[DTC]] based on the event and [[Option]] details communicated in a 
CANO message. With this information, a [[participant]] can determine the appropriate instructions to be submitted 
to [[DTC]] in a CAIN message. 
Note 
While CAIN messages contain information and rules that apply across event types, some information and some rules will 
only apply to specific event types. 
General Rules 
1. CAIN messages cannot be updated. To change a corporate action instruction, you must first withdraw the 
original instruction and send a new CAIN message. 
2. [[participant]] must have the Business Message Identifier [BizMsgIdr] within the Business Application 
Header. Each BizMsgIdr must be unique for a customer for each message. When message is received 
by [[DTC]], the schema and subscription will be validated, and the message will be checked against the 
“restricted” CAIN schema. 
3. The Safekeeping Account must be a [[DTC]] assigned [[participant]] number. Format is 8 digits with leading 
zeros as applicable. (i.e., part# 902 should read “00000902,” Part# 5 should read “00000005”).  
If both checks are successful, then an ACK message will be sent. If not, a NACK message will be sent 
back to the client. 
4. All CAIN messages that receive a network ACK will also receive a CAIS response accepting, rejecting, or 
pending the instruction. If the instruction is pended, then another CAIS accept or reject message will be 
sent after the business rules validation is completed. 
Normally, you will receive a PEND message first, followed by a CAIS accepted message if the instruction 
is made. However, you could receive a CAIS reject message if there is an error in your instruction. 
5. Each instruction message must contain an instruction for only one [[Option]]. You cannot instruct for two 
options on a single message. However, a user can submit more than one instruction message for an 
[[Option]]. The subsequent instruction messages will be processed in an incremental manner and will be 
added to the instructed units previously received. 
6. If an instruction is entered manually on the terminal on an event, the [[participant]] will be allowed to instruct 
on the same event via ISO 20022 messaging thereafter. 
 
1 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version number 
may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on the “MyStandards” section of the official SWIFT website and [[DTCC]].com . 
[[DTCC]] Public (White)

---

## Page 20

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 20 
7. If a CAIN message is rejected by [[DTC]], the [[participant]] will be allowed to send a new CAIN message on 
that same event as long as the account is not fully instructed. Otherwise, it will be rejected.  
8. Instructions will be processed in ‘real time’ if instruction is received during normal processing time. The 
process of receiving the instruction into the database will be real time. The subsequent instruction 
validation process should not take any longer than processing an instruction on the PT S/[[PBS]] system. 
9. Participants cannot elect on deleted (DE) or canceled (CN) events and/or options. If they submit a CAIN 
on a deleted or canceled events or options, a CAIS reject message will be sent. 
10. [[DTC]] Instruction Start Date – instructions cannot be sent unless the current date is equal to or greater than 
the [[DTC]] Instruction Start Date. [[DTC]] will not hold instructions before the instruction window is open.  
11. [[DTC]] Instruction Deadline – clients may instruct up to the instruction deadline time for the particular event 
based on the [[DTC]] Instruction Expiration Date within the announcement (ISO or CA Web). For instructions 
submitted close to the deadline time, a successful ACK message will be the indication that [[DTC]] will seek 
to process the instruction. However, it is not a guarantee of acceptance as it must still be validated against 
all processing rules described in this document. 
12. Instructed / Uninstructed Position – instructions will be checked against the [[DTC]] Account Transaction 
Processor (ATP) against your 10 account (regular unpledged) or 11 account (regular paid). Position in 
segregated accounts such as 14 regular pledged or 40 withdrawal by transfer will not be considered as 
uninstructed. 
13. The CAIN message will have mandatory and optional fields. Please see the Message Usage Guideline 
and Instruction Data Dictionary for a list of these fields. As well the fields will be documented in this guide.  
14. If an instruction is entered manually on the terminal, on an event, the [[participant]] will be allowed to instruct 
on the same event via ISO 20022 messaging thereafter. 
15. If a CAIN message is rejected by [[DTC]], the [[participant]] will be allowed to send a new CAIN message on 
that same event as long as the account is not fully instructed. 
16. Messages cannot be sent after [[DTC]] daily processor cutoff time. (Refer to the Date and Time for 
Reorganization Instruction Processor Cut-off times). 
17. Please note that unsolicited [[Option]] instructions ([[Option]] Type Code UNSO) will not be accepted.  
[[DTC]] will allow instructions for NOAC/ABST options (999). A NOAC/ABST instruction will not affect your [[DTC]] 
positions or your instructed or uninstructed balances on the message. Also, if you respond with a NOAC/ABST 
instruction, you [[DO]] not need to withdraw this instruction if you wish to send an instruction for a different [[Option]]. 
Tender and Exchange Event Instructions 
All tender and exchange events are processed via PTOP. 
Event Types in Scope 
• Consents (with payout) 
• Consents (without payouts) 
• Conversion (Cash or TBD) - Processed via PTOP 
• Dutch Auction (including Modified Dutch auction with specified and unspecified)  
• Exchange Offer- (144-A) 
• Exchange Offer 
• Exchange Offer (Cash and [[securities]]) 
• Exchange Offer (Consent) 
• Exchange Offer ([[Reg S]]) 
[[DTCC]] Public (White)

---

## Page 21

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 21 
• Merger (Vol) 
• Odd Lot Offer 
• Put (with withdrawal privilege) 
• Reorganization 
• Tender Offer (Bid Tender / Sealed Tender) 
• Tender Offer (Cash and [[securities]]) 
• Tender Offer (CIL) 
• Tender Offer (Consent) 
• Tender Offer (Mini-tender) 
• Tender Offer (Offer to Purchase) 
• Tender Offer (Self-tender) 
• [[Warrants]] Exercise (Cashless) 
[[Option]] Types in Scope 
[[DTC]] [[Option]] Type [[Option]] Type Description ISO 20022 
[[Option]] Type 
Applicable Event Types 
Cash and [[securities]] Holder will receive a combination of cash 
and [[securities]] 
CASE All Reorg Event Types 
Cash Holder will receive cash CASH All Reorg Event Types 
[[securities]] Holder will receive [[securities]]. SECU All Reorg Event Types 
Exercise Holder elects to exercise the intermediate 
security or warrant. 
EXER Rights Exercise, Warrant 
Exercise 
Subscribe and 
Oversubscribe 
Holder elects to subscribe to more 
[[securities]] than underlying [[securities]] 
position allows. 
OVER Rights Exercise 
Abstain Holder elects to abstain from voting on the 
proposal. 
ABST Consent Events 
Consent and Exchange Holder submits [[securities]] for exchange in 
addition to voting to approve the proposal. 
CEXC Exchange and Consent 
Consent and Tender Holder submits [[securities]] for tender in 
addition to voting to approve the proposal. 
CTEN Consent and Tender Events 
Consent Denied Holder elects not to approve the proposal. CONN Consent and Tender Events 
Consent Granted Holder elects to approve the proposal. CONY Consent only 
Retain Holder elects to keep/retain their existing 
security rather than receive a new 
security. 
MPUT Put Events 
No Action Holder elects not to take part in the event. NOAC All Reorg Event Type 
[[DTCC]] Public (White)

---

## Page 22

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 22 
[[DTC]] [[Option]] Type [[Option]] Type Description ISO 20022 
[[Option]] Type 
Applicable Event Types 
Proceeds Unknown Holder elects to convert security into a 
new security, cash or a combination of 
cash and [[securities]]. 
PRUN All Reorg Event Types 
Sell Holder elects to sell their security. SLLE Rights Exercise 
Mandatory Fields within all Tender / Exchange events processed via PTOP 
Field Name Notes Tag(s) 
Official Corporate Action 
Event Identification (COAF) 
If provided, must match the 
announcement. 
/Document/CorpActnInstr/CorpActnGnlInf/ 
OffclCorpActnEvtId 
Corporate Action Event 
Identification (CA [[ID]]) 
Corporate Action Event Identification [If 
client did not provide the COAF, the 
CA [[ID]] must match the CA [[ID]] provided 
in the announcement. 
Note: 
If client provides the COAF, then CA 
[[ID]] validation is not required. 
Otherwise, the CA [[ID]] must be provided 
and m
ust match the announcement 
from CA Web or the CANO message. 
/Document/CorpActnInstr/CorpActnGnlInf/ 
CorpActnEvtId 
Safekeeping Account [[DTC]] [[participant]] number. /Document/CorpActnInstr/AcctDtls/SfkpgAcct 
Event Type Code Must match the event type from the 
announcement message. 
/Document/CorpActnInstr/CorpActnGnlInf/ 
EvtTp/Cd/(CONS, CONV, DTCH, EXOF, MRGR, 
NOOF, ODLT, OTHR, BIDS, TEND, EXWA) 
[[Option]] Number Must be active [[Option]] number provided 
from the announcement. Please note 
that [[DTC]] will note accept UNSO 
unsolicited instructions within the 
[[Option]] Number tag. 
Note: 
[[Option]] number and [[Option]] type must 
match the event detail (i.e., if [[Option]] 1 
is cash, then [[Option]] Number should  
= 1 and [[Option]] Type = CASH). 
/Document/CorpActnInstr/CorpActnInstr/ 
OptnNb/Nb 
[[DTCC]] Public (White)

---

## Page 23

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 23 
Field Name Notes Tag(s) 
[[Option]] Type Must match [[Option]] type from the 
announcement. 
Note: 
[[Option]] number and [[Option]] type must 
match the event detail (i.e., if [[Option]] 1 
is cash, then [[Option]] Number should 
= 1 and [[Option]] Type = CASH). 
Document/CorpActnInstr/CorpActnInstr/ OptnTp/Cd 
Security Identification 
([[Option]] Level / Contra) 
Required for PTOP events only. /Document/CorpActnInstr/CorpActnInstr/ 
SctyId/OthrId/[[ID]] 
Instructed Quantity Must be less than a billion. Must be a 
whole number. 
Note: 
Instructions will be checked against the 
[[DTC]] Account Transaction Processor 
(ATP) against your 10 account (regular 
unpledged) or 11 account (regular 
paid). Position in segregated accounts 
such as 14 regular pledged or 40 
withdrawal by transfer will not be 
considered as uninstructed. 
/Document/CorpActnInstr/CorpActnInstr/ 
SctiesQtyOrInstdAmt/SctiesQty/InstdQty/Unit or 
FaceAmt 
Terms Acknowledgement 
Indicator (Suppl) 
Must be true. Document/DTCCCAINSD1/ReorgInstrDtls/ 
AckDtls/TermsAckInd 
Contact name (Suppl) Must be all alphabetic characters. /Document/DTCCCAINSD1/ReorgInstrDtls/ 
CtctPrsn/Nm 
Contact Phone number 
(Suppl) 
The formatting for the phone number 
follows the ISO convention and is 
treated as follows: 
• Start with plus sign and country 
code followed by dash. 
• Include 10 numeric digits after the 
dash. 
Note: 
Users are permitted to type 
parentheses and dashes (e.g., +1- 
212-855-1000 and +1-2128551000 are 
both acceptable). [[DTC]] strips out the 
non-numeric characters and saves the 
10 numeric digits after the dash. 
/Document/DTCCCAINSD1/ReorgInstrDtls/ 
CtctPrsn/PhneNb 
[[DTCC]] Public (White)

---

## Page 24

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 24 
Optional Fields based on Event Details 
Field Name Notes Tag(s) 
Security Identification (Underlying) Not required but will be checked 
against the underlying security of the 
event. If it does not match the 
announcement, a CAIS reject message 
would then occur. 
/Document/CorpActnInstr/ 
CorpActnGnlInf/UndrlygScty/ 
FinInstrmId/OthrId/[[ID]] 
Odd Lot Preference When a tender event has the ability to 
indicate that the instruction contains 
odd lot holders and should not be pro- 
rated 
/Document/CorpActnInstr/ 
CorpActnInstr/OptnFeatrs/ Cd/OPLF 
Conditional Quantity Please see details below concerning 
the usage of this field 
/Document/CorpActnInstr/ 
CorpActnInstr/SctiesQtyOrInstdAmt/ 
SctiesQty/CondlQty 
Generic Cash Price Received Per 
Product 
(BID PRICE) 
For Bid Tender or Dutch Auction 
events only. Can be either Specific 
Price or Unspecified Price depending 
on the [[Option]]. The Specific Price [[Option]] 
could be in Amount Price, Percentage 
or (Basis) Index Points format. 
/Document/CorpActnInstr/ 
CorpActnInstr/PricDtls/ 
GncCshPricRcvdPerPdct/AmtPric 
/Document/CorpActnInstr/CorpActnInst
r/PricDtls/GncCshPricRcvdPerPdct/Pct
gPric/PctgPricTp/PRCT 
/Document/CorpActnInstr/CorpActnInst
r/PricDtls/GncCshPricRcvdPerPdct/Ind
xPts 
Or 
Document/CorpActnInstr/ 
CorpActnInstr/PricDtls/ 
GncCshPricRcvdPerPdct/ 
NotSpcfdPric/UNSP 
Shareholder Number For certain events which allow the 
Shareholder number to be instructed 
within a certain [[Option]]. [[Option]] must be 
indicated within the Announcement (CA 
Web or CANO that there is a 
Shareholder Number feature Please 
see further details in the document. 
If the above is true, then the number 
can be sent in the instruction with a 
maximum of 25 alpha-numeric 
characters. 
/Document/CorpActnNtfctn/ 
CorpActnOptnDtls/OptnFeatrs/SHAR 
 
Document/CorpActnInstr/ 
CorpActnInstr/ShrhldrNb 
[[DTCC]] Public (White)

---

## Page 25

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 25 
Field Name Notes Tag(s) 
Conditions 1 through 6 If an [[Option]] has Conditions which must 
be replied to, then Conditions 1-6 tags 
need to be within the instruction 
extension details. (Please see details 
below concerning Conditions for further 
information). 
• For every instance where the 
Conditional Required Indicator = Y, 
then the Condition Indicator must 
be "true" on the CAIN message. 
• If the Conditional Required 
Indicator = N, then the condition 
does NOT need to be responded 
to. However, a CAIN message for 
such a condition can be sent with 
“false”. 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond1Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond2Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond3Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond4Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond5Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond6Ind 
Protect Instruction Fields 
(Used for Protect or Cover Protect 
Instructions) 
• Transaction Type 
o Protect Transaction (PROT) 
o Cover Protect Transaction 
(COVR) 
• Transaction Identification (used for 
COVR) identifies the transaction [[ID]] 
of the protect. 
• Protect Date – (used for COVR) 
date of the protect instruction. 
/Document/CorpActnInstr/ 
PrtctInstr/TxTp/PROT 
/Document/CorpActnInstr/ 
PrtctInstr/TxId 
/Document/CorpActnInstr/ 
PrtctInstr/PrtctSfkpgAcct 
/Document/CorpActnInstr/ 
PrtctInstr/PrtctDt 
Event Condition Rules for Tender and Exchange Instructions 
Options for tender and exchange events may have conditions that need to be responded to within the 
CAIN message. 
The CANO announcement has two fields that need to be checked to determine whether an instruction will 
require these conditions: 
1. Number of conditions which will state how many conditions there are for a particular [[Option]].  
/Document/DTCCCANOCSDDataSD1/OptnDtls/NbOfConds 
2. Each condition will be stated in the CANO extension showing the condition number, text and required flag 
(true /false). 
/Document/DTCCCANOCSDDataSD1/OptnDtls/OptnConds/CondNb 
/Document/DTCCCANOCSDDataSD1/OptnDtls/OptnConds/CondTxt 
/Document/DTCCCANOCSDDataSD1/OptnDtls/OptnConds/CondReqrdFlg  
All conditions with a Condition Required = true in the CANO must be responded to on the CAIN message. For 
every instance where the Conditional Required Indicator = true in the announcement message, then the 
Condition Indicator must be "true" on the CAIN message. 
If a condition does not require a response (Condition Required = false), then it does not have to be sent in the 
CAIN message. An instruction in which the Conditional Required Indicator = false in the announcement can be 
responded to in the CAIN message with “false” but you are not required to [[DO]] so.  
[[DTCC]] Public (White)

---

## Page 26

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 26 
Tender and Exchange Events Involving Shareholder Number (Allocation 
Codes) 
For certain events, an agent may distribute a Shareholder Number (Allocation Code) to certain Participants to 
be included with their instruction details. The CANO Announcement contains a Shareholder Number Flag 
(/Document/CorpActnNtfctn/CorpActnOptnDtls/OptnFeatrs/SHAR) at the [[Option]] level of the message to st ate 
that the particular [[Option]] requires a Shareholder Number. Please be advised that [[DTC]] can create separate 
options with a different Contra-[[CUSIP]] when this is applicable. 
If there is an event with ONLY ONE [[Option]] on which you can instruct and the Shareholder [[Option]] Feature is 
not present, you may still include a Shareholder Number in the CAIN instruction. [[DTC]] will allow the number to 
be sent and the agent/[[issuer]] will determine the course of action. Otherwise, if there is more than one [[Option]], 
you must have a Shareholder Number in the CAIN instruction for an [[Option]] where the CANO [[Option]] has the 
Shareholder Number indicator. 
Narrative within the CAIN for Tender and Exchange Events 
Additional Information (Instruction Narrative): narrative comments will be accepted within the CAIN instruction 
within the element (/Document/CorpActnInstr/CorpActnInstr/AddtlInf/InstrAddtlInf).  
Please be advised that the PTOP processor will only accept 80 characters of information.  
Shareholder Number (allocation code) 
An allocation code is a number which is provided to clients from an [[issuer]] / Agent which needs to be instructed 
for certain options for PTOP events only. Information about the Shareholder number is provided within the 
CANO detailing whether a Shareholder number is applicable for a certain [[Option]] within the [[Option]] Features 
Tag. 
/Document/CorpActnNtfctn/CorpActnOptnDtls/OptnFeatrs/SHAR 
Event Scenarios for Tender and Exchange Events 
Dutch Auction / Sealed Tender / Bid Tender 
Bid Price Rules: 
Options on these events can have either a specified or unspecified price. The announcement details on CA 
Web or in the CANO message will detail the price type required. 
If these three fields are in the CANO, then this [[Option]] requires a bid price. For options requiring a bid price, the 
CANO / CA Web will show the minimum price, maximum price and bid interval (increment). Below are the 
paths of those fields: 
 
/Document/CorpActnNtfctn/CorpActnOptnDtls/PricDtls/MaxPric 
/Document/CorpActnNtfctn/CorpActnOptnDtls/PricDtls/MinPric 
/Document/CorpActnNtfctn/CorpActnOptnDtls/PricDtls/MaxPric  
/Document/CorpActnNtfctn/CorpActnOptnDtls/RateAndAmtDtls/BidIntrvl  
 
 
T
he offeror may require the bid price to be expressed in one of the 3 different forms as follows:  
1. Amount Price - Price expressed as a currency and amount. 
[[DTCC]] Public (White)

---

## Page 27

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 27 
2. Percentage Price – Price expressed as a percentage. 
3. (Basis) Index Points - Price expressed as an index points. 
For bid price in Amount Price format, bid price must be output in CAIN in the following xPath:  
 
Document/CorpActnInstr/CorpActnInstr/PricDtls/GncCshPricRcvdPerPdct/AmtPric/AmtPricTp/ACTU  
Document/CorpActnInstr/CorpActnInstr/PricDtls/GncCshPricRcvdPerPdct/AmtPric/PricVal  
 
For bid price in Percentage format, the bid price must be output in CAIN in the following xPath:  
 
/Document/CorpActnInstr/CorpActnInstr/PricDtls/GncCshPricRcvdPerPdct/PctgPric/PctgPricTp/PRCT  
/Document/CorpActnInstr/CorpActnInstr/PricDtls/GncCshPricRcvdPerPdct/PctgPric/PricVal  
 
For bid price in (Basis) Index Point, the bid price must be output in CAIN in the following xPath:  
 
/Document/CorpActnInstr/CorpActnInstr/PricDtls/GncCshPricRcvdPerPdct/IndxPts  
 
[[DTC]] will process the instruction with a Bid Price and check minimum bid, maximum bid and bid increment. 
Based on these limits, the instruction will either be accepted or rejected. 
 
Bid Price rules: 
Must not be greater than the maximum, less than the minimum and must be in multiple.  
Must contain a decimal and no other non-numeric values.  
Cannot exceed 4 bytes to the left of the decimal. 
Cannot exceed 5 bytes to the right of the decimal. 
Example: 1234.20222 
 
Unspecified Price 
Some options (e.g., the Modified Dutch Auction) will allow for an instruction at an unspecified price. This means 
that for this [[Option]], the instruction is to be identified as UNSP and no price is required with the instruction.  
Note: 
All instructions for this [[Option]] will be deemed to be at the lowest price and accepted at whatever price is determined as the 
accepted price by the [[issuer]] (i.e., the “strike”. Failure to identify an instruction to be for an unspecified price (UNSP) for an 
[[Option]] requiring one will result in a CAIS rejection message. 
Document/CorpActnInstr/CorpActnInstr/PricDtls/GncCshPricRcvdPerPdct/NotSpcfdPric/UNSP  
If the unspecified price allowed flag in CA Web is “Y,” then the unspecified price will be noted on the CANO as 
the following: 
/Document/CorpActnNtfctn/CorpActnOptnDtls/CshMvmntDtls/PricDtls/GncCshPricRcvdPerPdct/ 
NotSpcfdPric/UNSP 
And the CAIN instruction must contain the “UNSP” unspecified tag for that [[Option]] as below: 
/Document/CorpActnInstr/CorpActnInstr/PricDtls/GncCshPricRcvdPerPdct/NotSpcfdPric/UNSP  
[[DTCC]] Public (White)

---

## Page 28

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 28 
 
 
Modified Dutch Auctions 
On a Modified Dutch Auction, the accepted (or “strike”) price determined by the [[issuer]] will normally be the pric e 
everyone receives (including those that chose “unspecified”). For a bid tender, every instruction on or below 
the [[issuer]]’s accepted (strike) price will be accepted at the price they instructed.  
Odd Lot Priority Flag (OPLF) 
Certain events can have the capability of utilizing the Odd Lot Priority Flag within the instruction to state that 
the instruction has odd lot holders and are requesting that the instruction not be prorated.  
If the CAIN indicates OPLF in the [[Option]] feature tag, it will be validated against the [[Option]] details in the 
announcement that an Odd Lot Preference feature exists for the particular [[Option]].  
The path for the odd lot preference flag within the instruction is: 
/Document/CorpActnInstr/CorpActnInstr/OptnFeatrs/Cd 
Tender and Exchange events involving Conditional Quantity 
Conditional Quantity can be indicated on certain events utilizing the tag in the CAIN message. This indicates 
that the instruction should only be accepted if the accepted prorated instruction is greater or equal to the 
conditional quantity. This would be indicated in the CAIN message using the following tags:  
/Document/CorpActnInstr/CorpActnInstr/SctiesQtyOrInstdAmt/SctiesQty/CondlQty/Unit  
/Document/CorpActnInstr/CorpActnInstr/SctiesQtyOrInstdAmt/SctiesQty/CondlQty/FaceAmt  
[[DTC]] will verify the instruction against the announcement details within the CANO [[Option]] Features Conditional 
flag or on CA Web with the Conditional Tenders Acceptance Flag being Yes. 
Note: 
The conditional quantity cannot exceed the instructed quantity. 
If a client wants to instruct without a conditional quantity for an event where the Conditional Indicator appears, 
then the conditional quantity field on the CAIN must have a value of zero. 
If the [[Option]] Feature Conditional Tenders Acceptance Flag on CA Web says N, the CAIN message must not 
have the Conditional Quantity field populated. The instruction will be rejected if this occurs.  
Full Conditional [[Option]] Scenarios 
For certain events, an [[Option]] may have a full condition indicator meaning that you must either instruct the 
conditional quantity “In Full” (equal to the instructed quantity) or instruct “0.” In other words, if you instruct “In 
Full,” you wish the instruction to be accepted in Full ONLY or else not be accepted (i.e., have full position 
returned to the target [[CUSIP]] if the offer is prorated). If you instruct “0,” this means that you have no conditions 
and will accept any quantity for the instruction (i.e., the full amount or the prorated amount).  
/Document/CorpActnInstr/CorpActnInstr/SctiesQtyOrInstdAmt/SctiesQty/CondlQty/Unit  
/Document/CorpActnInstr/CorpActnInstr/SctiesQtyOrInstdAmt/SctiesQty/CondlQty/FaceAmt  
 
 
Canadian Currency Options Scenario  
[[DTCC]] Public (White)

---

## Page 29

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 29 
 
For events with a Canadian currency [[Option]], your account must be eligible for Canadian Dollar [[settlement]]. 
Instructions from accounts which are not eligible will receive a CAIS reject message.  
Submitting a Protect, Cover Protect Instruction for Tender and Exchange Events 
For clients wishing to input a Protect and Cover Protect instruction to [[DTC]] relating to a Tender or Rights 
Exercise event, the instruction can be sent in ISO 20022. 
Cover on Behalf of Another [[participant]] functionality cannot be sent via ISO 20022 and will be available in the 
future. 
 
Rules Regarding Protect / Cover Protect Instructions 
• All fields listed above must be present for the instruction to be accepted. 
• Partial Covers will be accepted. Each cover will have its own reference number if accepted.  
• Protects will not be accepted after [[DTC]] Protect Expiration Date. 
• Cover protect instructions will not be accepted after the [[DTC]] Cover Protect Expiration Date.  
• For partial and full  cover scenarios, the cover quantity cannot exceed the amount of the open protect.  
• When submitting a Cover Protect for a "Specified Price” instruction on a Tender (Bid/Sealed Price) and 
Dutch Auction, the bid price is not required in the CAIN message. The VRI application will verify the 
details of the instruction, including the bid price based on the Protect [[ID]] provided.  
 
Required ISO Fields 
Submitting a Protect Instruction 
• The transaction type field must be in the message as PROT 
Transaction Type: /Document/CorpActnInstr/PrtctInstr/TxTp/PROT 
 
Submitting a Cover Protect Instruction 
• The transaction type field must be in the message as COVR 
Transaction Type: /Document/CorpActnInstr/PrtctInstr/TxTp/COVR 
• The VOI number of the protect instruction must be entered in the Transaction Identification field. 
/Document/CorpActnInstr/PrtctInstr/TxId 
• The date of the protect instruction must be entered as Protect Date. 
/Document/CorpActnInstr/PrtctInstr/PrtctDt 
Rights Exercise Events 
Mandatory Fields for Rights Events 
[[DTCC]] Public (White)

---

## Page 30

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 30 
Field Name Notes Tag(s) 
Official Corporate 
Action Event 
Identification 
(COAF) 
If provided, it must 
match the value in CA 
Web. 
/Document/CorpActnInstr/CorpActnGnlInf/ OffclCorpActnEvtId 
Corporate Action 
Event 
Identification (CA 
[[ID]]) 
Corporate Action 
Event Identification. 
If client did not provide 
the COAF, the CA [[ID]] 
must match the CA [[ID]] 
provided in the 
announcement. 
Note: 
If client provides the 
COAF, then CA [[ID]] 
validation is not 
required. Otherwise, 
the CA [[ID]] must be 
provided and must 
match the 
announcement from 
CA Web or the CANO 
message. 
/Document/CorpActnInstr/CorpActnGnlInf/ CorpActnEvtId 
Event Type Code Must match the value 
in CA Web. 
/Document/CorpActnInstr/CorpActnGnlInf/ EvtTp/EXRI 
[[Option]] Number Must match the value 
in CA Web. 
/Document/CorpActnInstr/CorpActnInstr/ OptnNb/Nb 
[[Option]] Type Must match 
announcement and 
must be only EXER, 
OVER, or SELL. 
Note: 
[[Option]] number and 
[[Option]] type have to 
match the event detail. 
(i.e., if [[Option]] 1 is 
EXER then [[Option]] 
number should say “1” 
and [[Option]] Type = 
“EXER”) 
Document/CorpActnInstr/CorpActnInstr/ OptnTp/EXER, OVER, or SELL 
Security 
Identification 
(Event Security [[ID]]) 
Must match the value 
in the Announcement. 
/Document/CorpActnInstr/CorpActnGnlInf/UndrlygScty/FinInstrmId/OthrId/[[ID]] 
Safekeeping 
Account 
[[DTC]] [[participant]] 
number 
/Document/CorpActnInstr/AcctDtls/ SfkpgAcct 
Instructed Quantity 
(core message) 
Must equal the total of 
all instructed quantity 
/Document/CorpActnInstr/CorpActnInstr/ 
SctiesQtyOrInstdAmt/SctiesQty/InstdQty/Qty/Unit or FaceAmt 
[[DTCC]] Public (White)

---

## Page 31

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 31 
Field Name Notes Tag(s) 
sequences described 
below. 
The instruction must contain a breakdown sequentially up to 99 times. The following fields are in the sequential 
breakdown: 
 
 
Transaction Sequence (Extension) 
Field Name Notes Tag(s) 
Transaction Sequence Must be sequential in order from 1 up 
to 99. 
/Document/DTCCCAINSD1 
ReorgInstrDtls/TxSeq/TxSeqNb 
Instruction Quantity For the sequence /Document/DTCCCAINSD1/ 
ReorgInstrDtls/TxSeq/InstrQty/Unit or FaceAmt 
Customer Reference 
Identification 
Repeatable free format field /Document/DTCCCAINSD1/ 
ReorgInstrDtls/TxSeq/CstmrRefId 
Oversubscription Quantity 
(if the instruction is an OVER 
[[Option]]) 
The instructed units at the core must 
equal the sum of the instructed units 
within each customer breakdown in 
the extension. 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/TxSeq/OvrsbcptQty/Unit or 
FaceAmt 
Total Oversubscription 
Quantity 
(if the instruction is an OVER 
[[Option]]) 
This must equal the sum of all 
oversubscription quantities from each 
sequence within the Transaction 
Sequence. 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/TtlOvrsbcptQty/Unit or FaceAmt 
Terms Acknowledgement 
Indicator 
(extension) 
Must be true. /Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/TermsAckInd 
Contact name (extension) Must be all alphabetic characters. 
Maximum length is 20 bytes 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/CtctPrsn/Nm 
Phone number (extension) The formatting for the phone number 
follows the ISO convention and is 
treated as follows: 
• Start with plus sign and country 
code followed by dash 
• Include 10 numeric digits after the 
dash 
Note: 
Users are permitted to type 
parentheses and dashes (e.g., +1-
212-855-1000 and +1-2128551000 
are both acceptable). [[DTC]] strips out 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/CtctPrsn/PhneNb 
[[DTCC]] Public (White)

---

## Page 32

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 32 
Field Name Notes Tag(s) 
the non-numeric characters and saves 
the 10 numeric digits after the dash. 
Optional Fields for Rights Events 
Field Name Notes Tag(s) 
Conditions 1 through 6 • For every instance where the Conditional 
Required Indicator = Y, then the Condition 
Indicator must be “true on the CAIN message. 
• If the Conditional Required Indicator = N, then 
the condition does NOT need to be responded 
to. However, a CAIN message for such a 
condition can be sent with “false”. 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond1Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond2Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond3Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond4Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond5Ind 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/AckDtls/Cond6Ind 
Additional Information 
(Instruction Narrative) 
Additional Information (narrative text) can be input 
for Rights Exercise instructions. A maximum of 
150 characters will be utilized within the 
processing system. 
/Document/CorpActnInstr/ 
CorpActnInstr/AddtlInf/InstrAddtlInf 
Solicitation Fee Indicator An instruction can utilize the Solicitation Fee 
Indicator field within the extension. This will be 
allowed only for those events in which the 
Solicitation Dealer Fee Flag is set to Y on the 
event announcement (CANO / CA Web) 
If the Solicitation Fee indicator is Y on the CAIN 
message, then Additional Information is required 
containing to whom and where payment should 
be made as payment will be made outside of [[DTC]] 
/Document/DTCCCAINSD1/ 
ReorgInstrDtls/SlctnFeeInd 
Protect Instruction Fields 
(Used for Protect or Cover 
Protect Instructions) 
• Transaction Type 
o Protect Transaction (PROT) 
o Cover Protect Transaction (COVR) 
• Transaction Identification (used for COVR) 
identifies the transaction [[ID]] of the protect. 
• Protect Date – (used for COVR) date of the 
protect instruction. 
/Document/CorpActnInstr/PrtctInstr/ 
TxTp/PROT 
/Document/CorpActnInstr/PrtctInstr/ 
TxId 
/Document/CorpActnInstr/PrtctInstr/ 
PrtctSfkpgAcct 
/Document/CorpActnInstr/PrtctInstr/ 
PrtctDt 
[[DTCC]] Public (White)

---

## Page 33

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 33 
Rights Exercise Event Instruction Rules 
1. The Underlying Security must be present in the CAIN instruction. The Security Identification within the 
Corporate Action Instruction block should not be submitted for a Rights Exercise event.  
2. Instructed Units – Instructed units in the core message must equal the sum of all sequence level 
instructed quantities. Please see point 2 below. 
3. The Instructed quantity minimum and multiple rules will apply at the sequence level. That is the instructed 
quantity within each sequence must be greater than the [[Option]] minimum quantity and must follow the 
instruction integral multiple rules (when applicable) within the CANO 
4. Transaction Sequence Rules: 
o Every instruction for a Rights Exercise event must contain the Transaction Sequence details even if 
there is only one customer sequence being entered for that instruction. 
o The Transaction sequence can be repeated up to 99 times. If you have more than 99 customer 
breakdowns, then separate instructions must be sent. 
o Transaction Sequence numbers must be present on a customer breakdown and must be in 
sequential order. A CAIS reject will occur if the instruction is received with non-sequential ordering. 
5. The instructed units at the core 
(/Document/CorpActnInstr/CorpActnInstr/SctiesQtyOrInstdAmt/SctiesQty/InstdQty/Qty/Unit) must equal 
the sum of the instructed units within each customer breakdown in the extension:  
/Document/DTCCCAINSD1/ReorgInstrDtls/TxSeq/OvrsbcptQty/Unit or FaceAmt.  
6. The Total Oversubscription field must be indicated for an OVER [[Option]] and must equal the sum of all 
Oversubscription units within each customer breakdown in the extension. 
/Document/DTCCCAINSD1/ReorgInstrDtls/TtlOvrsbcptQty or FaceAmt. 
…must equal sum: 
/Document/DTCCCAINSD1/ReorgInstrDtls/TxSeq/OvrsbcptQty/Unit or FaceAmt.  
7. Oversubscription can only occur for an [[Option]] which the [[Option]] Type Code is OVER. Oversubscription 
can be limited by quantity or percentage, or it can be unlimited. An instruction will be checked against the 
Oversubscription Type to see which applies for the OVER [[Option]]. If a client instructs on an OVER [[Option]] 
which is limited (by percentage or quantity) for more oversubscription units than allowed, a CAIS reject 
message will occur. This oversubscription type will be checked against each sequence oversubscription 
amount within a message. 
8. Sell [[Option]] Rules: 
o For instructions with SLLE options, the quantity of rights to be sold must be equal to or less than the 
client’s holdings. 
9. Solicitation FEE Indicator Rules 
o If the Solicitation Dealer Fee Flag = true on the CANO, then it can be included in the CAIN message.  
In the Additional Information section, you must provide the payment information of the payee as 
payment will be made outside of [[DTC]]. 
/Document/DTCCCAINSD1/ReorgInstrDtls/SlctnFeeInd 
/Document/CorpActnInstr/CorpActnInstr/AddtlInf/InstrAddtlInf 
10. Conditions Rules: 
o Conditions 1 through 6 may be required for a PSOP event. Based upon the CANO announcement, 
each [[Option]] will state the number of conditions within CANO message and within CA Web.  
[[DTCC]] Public (White)

---

## Page 34

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 34 
o All conditions with a Condition Required = true must be responded to on the CAIN message. For 
every instance where the Conditional Required Indicator = true in the announcement message, then 
the Condition Indicator must be “true” on the CAIN message. 
o If a condition does not require a response (Condition Required = false), then it does not have to be 
sent in the CAIN message. An instruction in which the Conditional Required Indicator = false in the 
announcement can be responded to in the CAIN message with “false” but you are not required to [[DO]] 
so. 
/Document/DTCCCANOCSDDataSD1/OptnDtls/OptnConds/CondNb 
/Document/DTCCCANOCSDDataSD1/OptnDtls/OptnConds/CondTxt 
/Document/DTCCCANOCSDDataSD1/OptnDtls/OptnConds/CondReqrdFlg  
11. You will also be able to view the total number of conditions for an [[Option]] in the Number of Conditio ns 
field. 
o /Document/DTCCCANOCSDDataSD1/OptnDtls/NbOfConds 
o Based on the [[Option]] information within the CANO, a CAIN instruction must include responses within 
the extension for [[Option]] 1-6 with a Boolean indicator (true / false) 
o If a condition does not require a response, then it does not have to be sent in the CAIN message. An 
instruction in which the Conditional Required Indicator = false in the announcement can be 
responded to in the CAIN message with false but you are not required to [[DO]] so. 
12. Customer Name and Phone number must be populated in the extension of the message for Rights 
Exercise Instructions. 
Submitting a Protect or Cover Protect Instruction for Rights Events 
Required ISO Fields 
Submitting a Protect Instruction 
The transaction type field must be in the message as PROT 
Transaction Type: /Document/CorpActnInstr/PrtctInstr/TxTp/PROT  
Submitting a Cover Protect Instruction 
• The transaction type field must be in the message as COVR 
Transaction Type: /Document/CorpActnInstr/PrtctInstr/TxTp/COVR 
• The VOI number of the protect instruction must be entered in the Transaction Identification field.  
/Document/CorpActnInstr/PrtctInstr/TxId 
• The date of the protect instruction must be entered as Protect Date. 
/Document/CorpActnInstr/PrtctInstr/PrtctDt 
 
Submitti ng a Cover on Behalf of Another [[participant]] (Future build)  
Rules Regarding Protect / Cover Protect instructions for Rights Events 
For clients wishing to input a Protect or guarantee of delivery instruction to [[DTC]] relating to a Tender or Rights 
Exercise event, the instruction can be sent in ISO20022. 
• All fields listed in the previous section must be present for the instruction to be accepted.  
• Partial Covers will be accepted. Each cover will have its own reference number if accepted.  
• Protects will not be accepted after [[DTC]] Protect Expiration Date. 
[[DTCC]] Public (White)

---

## Page 35

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 35 
• Cover protect instructions will not be accepted after the [[DTC]] Cover Protect Expiration Date.  
• For partial cover scenarios, the cover quantity cannot exceed the amount of the open protect.  
• For Rights Exercise events, a protect instruction can contain up to 99 sequences per message. Please 
note that previous capability in PSOP was 12 sequences. The Cover Protect instruction for this scenario 
must contain only one sequence per message. 
• For Rights Exercise Protect instruction, the Instructed quantity in the core message must equal the sum of 
all the instructed quantity sequences in the extension. In the extension, a repeating Transaction sequence 
should be output containing the transaction sequence number, the instruction quantity, the 
oversubscription quantity, and the customer reference number. The total oversubscription quantity field in 
the extension should equal the sum of all oversubscription quantities from all sequences.  
• Sequence numbers in the Transaction Sequence should be in numerical order within the protect 
instruction. 
• Cover Protect instructions are one sequence per instruction. Instructions containing multiple sequences 
will be rejected. The Cover Protect instruction should contain the instructed quantity of the sequence 
being covered in the core message. 
• The core message should also include the Protect Instruction / Transaction Type “COVR,” the Transaction 
[[ID]] of the Protect instruction, and the Protect Date of the Instruction. In the extension, utilize the 
Transaction Sequence Block and output the Transaction Sequence Number and Instruction Quantity only.  
• The Customer Reference Identification must not be input for the Cover instruction as this was input on the 
Protect instruction. This will be ignored if sent. 
• When there is a cover protect with [[Option]] type “OVER,” participants would be able to cover a [[BASIC]] 
quantity and the oversubscription quantity will be systemically calculated. If the Oversubscription Quantity 
or Total Oversubscription Quantity are provided in the CAIN message for the Cover instruction, it will be 
rejected. Please note, that oversubscription details provided on the Protect will be output on the CAIS 
response message based upon the percentage of the protect [[BASIC]] quantity.  
• Cover Protect instructions must include ONLY one transaction sequence per message. Once a protect is 
covered, a new VOI is created and the sequence number from the protect [[ID]] that was covered carries 
over to the new VOI. 
Canadian Currency Options Scenario 
For rights events with a Canadian currency [[Option]], your account must be eligible for Canadian Dollar 
[[settlement]] and the Canadian [[settlement]] account must have a balance equivalent to the subscription fees that 
will be charged. Instructions from accounts that are not eligible will receive a CAIS reject message. Instructions 
for an account eligible for Canadian [[settlement]] will receive a conditionally accepted instruction subject to 
rejection if the account has not been funded sufficiently. 
PUT Event Instruction General Rules 
The following fields are required in order to create a CAIN message for a PUT event:  
1. The instructed quantity must meet the [[Option]] minimum quantity and instruction integral multiple. Ex: [[Option]] 
minimum quantity = 1000 integral multiple = 1000. 
Narrative comments will be accepted within the CAIN instruction for PUT events within the element 
(/Document/CorpActnInstr/CorpActnInstr/AddtlInf/InstrAddtlInf). Please be advised that the PUTS 
processor will only accept 35 characters of information. 
2. The Terms and Acknowledgement Indicator is not required for PUTS events. Values true and blank will be 
accepted and false will be rejected if included in the CAIN message. 
3. For Mandatory Put and Partial Mandatory Put with [[Option]] to Retain events, VRI will only accept 
instructions on the MPUT [[Option]]. If client chooses to receive the [[default]] [[Option]] of CASH, no instruction is 
required. If a CAIN instruction is sent for the [[default]] [[Option]], it will result to a CAIS reject with a reject 
reason code of OPTY.  
[[DTCC]] Public (White)

---

## Page 36

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 36 
4. When submitting instructions for Put events, the event security [[ID]] is required while contra [[CUSIP]] is 
optional.   
5. Put events with withdrawal privilege are processed via PTOP, therefore, the rules for mandatory fields in 
the CAIN message for PTOP events such as Tenders and Exchange also apply. (Example: Contra [[CUSIP]] 
is a mandatory field in CAIN) 
Mandatory Fields for events processed via PUTS 
Field Name Notes Tag(s) 
Official 
Corporate 
Action Event 
Identification 
(COAF) 
If provided, it must match the 
announcement. 
/Document/CorpActnInstr/CorpActnGnlInf/OffclCorpActnEvtId 
Corporate 
Action Event 
Identification 
(CA [[ID]]) 
Corporate Action Event Identification. 
If client did not provide the COAF, the 
CA [[ID]] must match the CA [[ID]] provided in 
the announcement. 
Note: 
If client provides the COAF, then CA [[ID]] 
validation is not required. Otherwise, the 
CA [[ID]] must be provided and must match 
the announcement from CA Web or the 
CANO message. 
/Document/CorpActnInstr/CorpActnGnlInf/ CorpActnEvtId 
Safekeeping 
Account 
Account number for the Safekeeping 
account. 
/Document/CorpActnInstr/AcctDtls/SfkpgAcct 
Event Type 
Code 
Must match the event type from the 
announcement message. 
/Document/CorpActnInstr/CorpActnGnlInf/ EvtTp/Cd (BPUT) 
Security 
Identification 
(Underlying) 
Required for PUTS events. Must match 
announcement. 
/Document/CorpActnInstr/CorpActnGnlInf/ 
UndrlygScty/FinInstrmId/OthrId/[[ID]] 
[[Option]] Number Must be active [[Option]] number provided 
from the announcement. 
Note: 
[[DTC]] will not accept UNSO unsolicited 
instructions within the [[Option]] Number 
tag. 
/Document/CorpActnInstr/CorpActnInstr/ OptnNb/Nb 
[[Option]] Type Must match [[Option]] type from the 
announcement. 
Note: 
[[Option]] number and [[Option]] type must 
match the event detail (i.e., if [[Option]] 1 is 
cash, then [[Option]] number should say “1” 
and [[Option]] Type = “CASH”) 
Document/CorpActnInstr/CorpActnInstr/ OptnTp/Cd 
[[DTCC]] Public (White)

---

## Page 37

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIN MESSAGES 37 
Field Name Notes Tag(s) 
Instructed 
Quantity (core 
message) 
Must be less than a billion and must be a 
whole number. 
/Document/CorpActnInstr/CorpActnInstr/ 
SctiesQtyOrInstdAmt/SctiesQty/InstdQty/ Qty/Unit or 
FaceAmt 
Customer 
Reference [[ID]] 
Customer identification entered by client 
upon instruction submission. (It is 
required for BPUT 62 and 62B events 
and optional for 66P). This is a 
mandatory alpha numeric field. 
/Document/DTCCCAINSD1/ReorgInstrDtls/CstmrRefId 
Contact Name 
(Suppl) 
Must be all alphabetic characters. 
Maximum length is 20 bytes 
/Document/DTCCCAINSD1/ReorgInstrDtls/ CtctPrsn/Nm 
Contact Phone 
Number 
(Suppl) 
The formatting for the phone number 
follows the ISO convention and is treated 
as follows: 
• Start with plus sign and country code 
followed by dash. 
• Include 10 numeric digits after the 
dash. 
Note: 
Users are permitted to type parentheses 
and dashes (e.g., +1-212-855-1000 and 
+1-2128551000 are both acceptable). 
[[DTC]] strips out the non-numeric 
characters and saves the 10 numeric 
digits after the dash. Must be all 
alphabetic characters. 
/Document/DTCCCAINSD1/ReorgInstrDtls/ CtctPrsn/PhneNb 
[[DTCC]] Public (White)

---

## Page 38

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 38 
CAIS MESSAGES 
What Is a CAIS message? 
A Corporate Action Instruction Status Advice message (CAIS) is an ISO message representing the 
confirmation of a Corporate Action CAIN instruction. A CAIS message confirms the information provided within 
the CAIN Corporate Action instruction message and provides a status for that instruction.  
MX Identifier ISO 20022 Message 
Names 
Extension Short 
Name 
Equivalent ISO 
15022 
Equivalent [[DTC]] 
Processes 
seev.034.002.xx2 Corporate Action Instruction 
Status Advice 
supl.030.001.xx CAIS MT 567 Instruction Reply 
For Reorganization events, four instruction processing status codes will be used:  
• Accepted for Further Processing (Accepted) 
• Rejected 
• Pending 
• Cancelled 
The Reorganization instruction confirmation message contains additional data fields supplied in the extension 
that provide further information regarding the instruction. For example, the message may use extended reason 
codes and instruction status codes to further describe the reject or pending scenario. Information such as 
Conditions, Bid Price, or Conditional Quantity contained in the CAIN message will be confirmed in the CAIS 
extension. 
Please see the Lifecycle of an Instruction section for more details on how the CAIS is generated. 
CAIS messages for instructions submitted via [[PTS]] / [[PBS]] 
A CAIS message will be generated to confirm an instruction that was input and accepted via [[PTS]] / [[PBS]]. This 
capability provides participants the ability to fully reconcile all instructions submitted to [[DTC]] regardless of the 
method of input. Also, participants are able to differentiate an instruction submitted via [[PTS]] / [[PBS]] from an ISO - 
based instruction within the Transaction Identification (VOI) number in the extension of the message.  
Note: 
You will be able to determine that an instruction was entered on [[PTS]] / [[PBS]] by the lack of an “XM” in the second and third 
characters in the Transaction Identification (VOI) number. 
 
2 The last two digits in the MX Identifier signify the version number. The MX version number may change during the SWIFT annual release based on mandatory 
or optional updates to the standards. 
Current schemas are available on the “MyStandards” section of the official SWIFT website and [[DTCC]].com . 
[[DTCC]] Public (White)

---

## Page 39

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 39 
Instruction Cancellations 
CAIS messages for Events Cancelled in the Market 
For events that have been withdrawn in the market in which there have been previously accepted instructions, 
a CAIS message for each instruction is sent with an Instruction Processing Status of “Cancelled” and a Reason 
Code of “CSUB” (Cancelled by Agent) and an extended Transaction Identification Status Code of “RESC.”  
CAIS messages for Instructions Withdrawn by the Client 
When client submits a withdrawal on an instruction via PTOP, a CAIS message is generated with the 
Instruction processing status of Cancelled and a reason code of CANI (Cancelled by Yourself) in the core and 
a Transaction [[ID]] Status of WITH in the extension. When client submits a withdrawal via CAIC message, client 
will also receive a CAIS message confirmation with CANI/WITH reason code and status, in addition to the 
CACS withdrawal confirmation message. 
CAIS messages for Instructions Cancelled by the System 
When an instruction is withdrawn by [[DTC]] on behalf of a [[participant]], a CAIS message is generated with the 
Instruction processing status of Cancelled and a reason code of CANS (Cancelled by System) in the core and 
a Transaction [[ID]] Status of WITH in the extension. 
CAIS message for Instructions Requiring Agent Approval 
If an instruction withdrawal requires agent approval, a CAIS Pending message with an extended Transaction 
Identification Status Code of “PENA” (Pending Agent Approval) is generated. Once the agent approves the 
withdrawal instruction, an additional message is sent with a CAIS Cancellation and Reason Code of “CANI and 
a Transaction [[ID]] Status of WITH in the extension.” 
Information Contained on the CAIS Message 
The following table contains all of the information elements presented on a CAIS message, along with an 
explanation of what each element means and/or applicable details. 
Data Element Definition/Information Received from 
CA
IN 
Instruction? 
Instruction 
Identification 
The Business Message Identifier of the received instruction. This 16- 
character identifier matches the status message to a previously submitted 
CAIN message. Every ISO message must have a Business Message 
Identifier, or BAH. 
/Document/CorpActnInstrStsAdvc/InstrId/[[ID]] 
YES 
Corporate Action 
Event Identification 
Specified on the received instruction. Leading zeroes will be suppressed. 
If a [[participant]] / sender provides their own CA [[ID]], then this will appear on 
the CAIS message. 
/Document/CorpActnInstrStsAdvc/CorpActnGnlInf/CorpActnEvtId 
YES 
Official Corporate 
Action Event 
Identification 
The COAF, or the Official Corporate Action Identification, on the received 
instruction. This is the CA [[ID]] preceded by “US.” 
YES 
[[DTCC]] Public (White)

---

## Page 40

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 40 
/Document/CorpActnInstrStsAdvc/CorpActnGnlInf/OffclCorpActnEvtId 
Event Type The type of corporate action event that the original instruction message 
was responding to. Specified on the received instruction. For rejected 
messages, the event type instructed will appear on the CAIS message. 
/Document/CorpActnInstrStsAdvc/CorpActnGnlInf/EvtTp 
YES 
Instruction 
Processing Status 
Status of the instruction. Valid values are Cancelled, Accepted for Further 
Processing, Rejected, Pending 
/Document/CorpActnInstrStsAdvc/InstrPrcgSts 
 
Accepted for 
Further Processing 
This field defaults to “NORE” if the instruction message was accepted 
(MADE). 
/Document/CorpActnInstrStsAdvc/InstrPrcgSts/AccptdForFrthrPrcg/ 
NoSpcfdRsn 
 
Solicitation Dealer 
Fee Indicator 
Indicates that the client wants the solicitation fee on the event. 
 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/SlctnDealrFeeInd 
YES 
Rejected This field defaults to “NORE” if the instruction message was accepted. 
If the instruction has been rejected, this field can have up to 6 reason 
codes. If the code “OTHR” is utilized, then additional extension information 
will be used. 
Please see the Reject Reason Codes section for all extended reject 
reason codes. 
Account Servicer Deadline  
Missed [ADEA] Incorrect  
Certification [CERT]Invalid  
[[Option]] Type [OPTY] Invalid  
Reference [ULNK] Invalid  
Security [DSEC] Lack of [[securities]] [LACK] 
Market Deadline Missed [LATE]  
Mismatch [NMTY] 
[[Option]] Cancelled [CANC]  
[[Option]] Inactive [INTV] 
[[Option]] Number Rejection [OPNM]  
Other [OTHR] 
Quantity Rejection [DQUA]  
Safekeeping Account Rejection [SAFE]  
Unrecognized Identification [EVNM]  
Invalid Bid Value [DQBV] 
Invalid Bid Increment [DQBI]  
Shareholder Number Rejection [SHAR] 
/Document/CorpActnInstrStsAdvc/InstrPrcgSts/Rjctd/Rsn 
 
Pending No Specified Reason: Sent after full business validation is successful but 
before account position validation. 
 
[[DTCC]] Public (White)

---

## Page 41

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 41 
LACK: Sent when an instruction is recycling due to insufficient position. 
/Document/CorpActnInstrStsAdvc/InstrPrcgSts/Pdg/NoSpcfdRsn 
/Document/CorpActnInstrStsAdvc/InstrPrcgSts/Pdg/Rsn/RsnCd/Cd 
(Instructed Balance) Total of all accepted instructions submitted. Please note that NOAC/ABST 
instructions will not display as an instructed balance total. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/InstdBal 
 
Instructed Balance 
(Short/Long 
Position) 
This defaults to “LONG” for a positive value. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/InstdBal/ShrtLngPos 
 
Instructed Balance 
(Unit) 
When the Event Security is “[[Equity]]” (non-debt), then the Instructed Balance 
(Amount) equals the total of all instructions submitted for this event. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/InstdBal/QtyChc/Qty/ Unit 
 
Instructed Balance 
(Face Amount) 
When the Event Security is “Debt,” then the Instructed Balance (Amount) 
equals the total of all instructions submitted for this event. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/InstdBal/QtyChc/Qty/ 
FaceAmt 
 
Uninstructed 
Balance 
The current balance remaining in the General Free account. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/UinstdBal 
 
Uninstructed 
Balance 
(Short/Long 
Position) 
This defaults to “LONG” for a positive value. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/UinstdBal/ShrtLngPos 
 
Uninstructed 
Balance (Unit) 
When the Event Security is “[[Equity]] (non-debt),” then the Uninstructed 
Balance (Unit) is equal to the current balance remaining in the General 
Free Account for this event minus the total of all instructions submitted for 
this event. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/UinstdBal/QtyChc/Qty/Unit 
 
Uninstructed 
Balance (Face 
Amount) 
When the Event Security is “Debt,” then the Uninstructed Balance 
(Amount) is equal to the current balance remaining in the General Free 
Account for this event minus the total of all instructions submitted for this 
event. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/UinstdBal/QtyChc/Qty/ 
FaceAmt 
 
Status Quantity 
(Unit) 
Instructed quantity (units) from the CAIN Instruction. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/StsQty/Qty/Unit 
YES 
Status Quantity 
(Face Amount) 
Instructed quantity (face amount) from the CAIN Instruction. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/StsQty/Qty/FaceAmt 
YES 
Protect Balance Balance of all open protects for a given event. 
/Document/CorpActnInstrStsAdvc/CorpActnInstr/PrtctBal/QtyChc/Qty/Unit 
or FaceAmt 
NO 
Protect Instruction 
Transaction Type 
Indicates whether the instruction is for a Protect (PROT), Cover Protect 
(COVR) or Cover on Behalf of Another [[participant]] (COVP). 
YES 
[[DTCC]] Public (White)

---

## Page 42

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 42 
/Document/CorpActnInstrStsAdvc/PrtctInstr/TxTp 
Protect Instruction 
Status 
Status of the Protect Instruction. Valid values are Open (OPEN), Fully 
Covered (COVR), and Expired (EXPI). 
/Document/CorpActnInstrStsAdvc/PrtctInstr/PrtctTxSts 
 
Transaction 
Identification 
Transaction [[ID]] of the Protect Instruction. 
/Document/CorpActnInstrStsAdvc/PrtctInstr/TxId 
 
Protect Safekeeping 
Account 
Account which submitted the protect. Will be output for Cover on Behalf of 
Another [[participant]] instructions. 
/Document/CorpActnInstrStsAdvc/PrtctInstr/PrtctSfkpgAcct 
YES 
Protect Date Date of the Protect Instruction. Will be output on instructions for Cover or 
Cover on Behalf of Another [[participant]]. 
/Document/CorpActnInstrStsAdvc/PrtctInstr/PrtctDt 
YES 
Uncovered Protect 
Quantity 
Remaining quantity of protect instruction which has not been covered. 
/Document/CorpActnInstrStsAdvc/PrtctInstr/UcvrdPrtctQty/Unit OR 
FaceAmt 
 
EXTENSION ELEMENTS 
Transaction 
Identification 
VOI number assigned by [[DTC]] for the instruction.  
New format for XML and API: 
1: Char. (Follow current Mainframe pattern, “T’,’P’, etc.)  
2-3: Source. “XM” for XML or “AP” for API 
4-8: YYDDD year + Julian Day 
9-14: Sequence Counter (6 digits) 
/Document/DTCCCAISSD1/ReorgInstrDtls/TxId 
 
Transaction 
Sequence 
Used for Rights Exercise events to display sequence level information. For 
Cover Protect instructions regarding Rights instructions, there will be only 
one sequence confirmed per each CAIS advice. 
/Document/DTCCCAISSD1/ReorgInstrDtls/TxSeq 
YES 
Transaction 
Sequence Number 
Sequence number for that sequence. 
/Document/DTCCCAISSD1/ReorgInstrDtls/TxId/TxSeqNb 
YES 
Instruction Quantity Quantity for the sequence. 
/Document/DTCCCAISSD1/ReorgInstrDtls/TxSeq/InstrQty/Unit OR 
FaceAmt 
YES 
Oversubscription 
Quantity 
Oversubscription quantity for the sequence. 
/Document/DTCCCAISSD1/ReorgInstrDtls/TxSeq/OvrsbcptQty/Unit OR 
FaceAmt 
YES 
Customer 
Reference 
Identification 
(Rights Offer) 
Free format information supplied by the customer for the sequence. 
/Document/DTCCCAISSD1/ReorgInstrDtls/TxSeq/CstmrRefId 
YES 
[[DTCC]] Public (White)

---

## Page 43

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 43 
Customer 
Reference 
Identification (Puts) 
Free format information supplied by the customer for the sequence. 
/Document/DTCCCAISSD1/ReorgInstrDtls/CstmrRefId 
YES 
Transaction 
Identification Status 
RECY: Recycled 
DROP: Dropped 
MADE: Instruction Accepted  
REJA: Rejected by Agent  
PENA: Pending Agent Approval 
/Document/DTCCCAISSD1/ReorgInstrDtls/TxIdSts 
 
Rejection Reason Extended information further describing the reason for rejection. 
/Document/DTCCCAISSD1/ReorgInstrDtls/Rsn 
 
Total 
Oversubscription 
Quantity 
Total quantity of all sequence oversubscription quantities for the instruction. 
/Document/DTCCCAISSD1/ReorgInstrDtls/SctiesQtyDtls/TtlOvrsbcptQty 
YES 
Conditional 
Quantity 
Conditional Quantity instructed from CAIN message. 
/Document/DTCCCAISSD1/ReorgInstrDtls/SctiesQtyDtls/CondlQty 
YES 
Shareholder 
Number 
Reference number (provided by the [[issuer]]/agent) to identify qualifying 
[[investor]] or a shareholder with the [[issuer]] or the registration provider (for 
instance allocation code) identifying the instruction as meeting the 
requirements/qualifications to be accepted in this [[Option]]. 
/Document/DTCCCAISSD1/ReorgInstrDtls/ShrhldrNb 
YES 
ACKNOWLEDGMENT DETAILS 
Terms 
Acknowledgement 
Indicator 
Acknowledgement by the client of all terms of the offer. 
/Document/DTCCCAISSD1/ReorgInstrDtls/AckDtls/TermsAckInd 
YES 
Condition 1-6 
Indicator 
True / False indicator based on the CAIN instruction for each applicable 
condition. true = Yes; false = No 
/Document/DTCCCAISSD1/ReorgInstrDtls/AckDtls/Cond1Ind 
/Document/DTCCCAISSD1/ReorgInstrDtls/AckDtls/Cond2Ind 
/Document/DTCCCAISSD1/ReorgInstrDtls/AckDtls/Cond3Ind 
/Document/DTCCCAISSD1/ReorgInstrDtls/AckDtls/Cond4Ind 
/Document/DTCCCAISSD1/ReorgInstrDtls/AckDtls/Cond5Ind 
/Document/DTCCCAISSD1/ReorgInstrDtls/AckDtls/Cond6Ind 
YES 
Contact Person 
Name 
Contact name from the instruction. Maximum length is 20 bytes. 
/Document/DTCCCAISSD1/ReorgInstrDtls/CtctPrsn/Nm 
YES 
Contact Phone 
Number 
Contact Phone Number from the instruction. 
/Document/DTCCCAISSD1/ReorgInstrDtls/CtctPrsn/PhneNb 
YES 
Bid Price Bid Price received from the CAIN instruction. 
/Document/DTCCCAISSD1/ReorgInstrDtls/BidPric/AmtPric 
YES 
[[DTCC]] Public (White)

---

## Page 44

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 44 
/Document/DTCCCAISSD1/ReorgInstrDtls/BidPric/NotSpcfdPric/UNSP 
CAIS Reject Codes 
The following table contains lists of error codes and their explanations, including an elaboration on the “OTHR” 
error code. It provides a list of the real-text reasons that can accompany this code on a rejection message.  
Instruction Processing Status: Rjctd (Rejected) 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
ADEA Account Servicer 
Deadline Missed 
CUTT REJT Cut-off time has 
passed. 
Instruction must be 
received within the 
election window 
ADEA  PROC REJT Current date has 
passed cover 
protect submission 
end date. 
Cover protect 
instruction must be 
received prior to 
the cover protect 
expiration date and 
time 
ADEA  PROE REJT Current date is 
greater than 
Protect 
Submission End 
Date. 
Protect instruction 
must be received 
prior to the cover 
protect expiration 
date and time 
BSTR Before Instruction 
Period 
PROS REJT Current date is 
less than protect 
submission start 
date 
Submission of 
protect instruction 
must be within the 
Protect Instruction 
Start and End Date 
and time. 
BSTR  SUBE REJT Submission Date 
Not Reached 
Instruction must be 
submitted within 
the Instruction 
Start and End Date 
and time. 
CANC [[Option]] is not valid; 
it has been 
cancelled by the 
market or service 
provider and 
cannot be 
responded to. 
N/A REJT [[Option]] has been 
cancelled. 
Chosen [[Option]] 
must be active. 
CERT Instruction is 
rejected since the 
provided 
certification is 
incorrect or 
incomplete. 
ACKA REJT Acknowledgement 
not agreed 
Acknowledgement 
must be agreed 
using the value 
"true" 
[[DTCC]] Public (White)

---

## Page 45

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 45 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
CERT  ACKS REJT Acknowledgement 
Indicator missing 
Acknowledgement 
cannot be blank 
CERT  CN1N REJT Conditional 
required indicator 
1 is not available 
 
CERT  CN2N REJT Conditional 
required indicator 
2 is not available 
 
CERT  CN3N REJT Conditional 
required indicator 
3 is not available 
 
CERT  CN4N REJT Conditional 
required indicator 
4 is not available 
 
CERT  CN5N REJT Conditional 
required indicator 
5 is not available 
 
CERT  CN6N REJT Conditional 
required indicator 
6 is not available 
 
CERT  CN1R REJT Condition 1 is 
Missing 
Conditional 
Required cannot 
be blank. 
CERT  CN1Y REJT Condition 1 Invalid 
- Must be Yes 
Conditional 
Required must be 
Yes 
CERT  CN2R REJT Condition 2 is 
Missing 
Conditional 
Required cannot 
be blank 
CERT  CN2Y REJT Condition 2 Invalid 
- Must be Yes 
Conditional 
Required must be 
Yes 
CERT  CN3R REJT Condition 3 is 
Missing 
Conditional 
Required cannot 
be blank 
CERT  CN3Y REJT Condition 3 Invalid 
- Must be Yes 
Conditional 
Required must be 
Yes 
CERT  CN4R REJT Condition 4 is 
Missing 
Conditional 
Required cannot 
be blank 
[[DTCC]] Public (White)

---

## Page 46

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 46 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
CERT  CN4Y REJT Condition 4 Invalid 
- Must be Yes 
Conditional 
Required must be 
Yes 
CERT  CN5R REJT Condition 5 is 
Missing 
Conditional 
Required cannot 
be blank 
CERT  CN5Y REJT Condition 5 Invalid 
- Must be Yes 
Conditional 
Required must be 
Yes 
CERT  CN6R REJT Condition 6 is 
Missing 
Conditional 
Required cannot 
be blank 
CERT  CN6Y REJT Condition 6 Invalid 
- Must be Yes 
Conditional 
Required must be 
Yes 
CTCT Missing Contact CNAM REJT Contact Name 
Missing 
Contact Name 
must be provided 
CTCT  CNPM REJT Contact Phone 
Number Missing 
Phone Number 
must be provided 
DQBI Bid price / basis 
points / 
percentage 
increments 
rejected due to 
invalid bid 
increment for the 
event. 
N/A REJT Invalid bid 
increments for bid 
price / basis points 
Bid increment must 
be in accordance 
with the terms of 
the offer 
DQBV Bid price / basis 
points / 
percentage falls 
outside of bid 
range for the 
event. 
BIDE REJT 
Bid Price exceeds 
maximum bid price 
allowed for the 
offer 
Bid amount cannot 
exceed the 
maximum bid price 
allowed 
DQBV  BIDI REJT Bid price is 
missing or invalid 
Bid amount must 
be provided 
DQBV  BIDM REJT Bid Price is less 
than the minimum 
bid price allowed 
for the offer 
Bid amount cannot 
be less than the 
minimum bid price 
allowed 
DQCC Currency 
Rejection 
N/A REJT Invalid/Incorrect 
Currency Code 
Currency code 
must match the 
currency code in 
CANO 
[[DTCC]] Public (White)

---

## Page 47

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 47 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
DQUA Quantity Rejection COQ0 REJT Conditional 
Quantity of zero is 
missing 
Conditional 
Quantity Zero is 
required 
DQUA  COQE REJT Conditional 
Quantity exceeds 
the Transaction 
Quantity 
Conditional 
quantity cannot 
exceed the 
transaction 
quantity. 
DQUA  COQI REJT Conditional 
Quantity missing 
or invalid 
Conditional 
quantity is required 
and must be valid 
DQUA  COTQ REJT Conditional 
Quantity does not 
equal Transaction 
Quantity 
Conditional 
quantity must be 
equal the 
transaction 
quantity whilst this 
offer accepts only 
full conditional 
quantity. 
DQUA  COVR REJT Cover Quantity 
Greater Than 
Remaining Protect 
Quantity 
Cover quantity 
cannot exceed the 
total protect 
quantity. 
DQUA  FRAQ REJT Customer has 
fractional 
underlying 
quantity, adjust 
quantity. 
Instructed quantity 
must not include 
decimals. 
DQUA  FUNU REJT Function is not 
available at this 
time. Please check 
expiration start 
and end times for 
the event. 
Instructions must 
be received within 
the election 
window time 
frame. 
DQUA  N/A REJT Instructed Quantity 
exceed 9 digits 
Instructed Quantity 
including 
oversubscription 
cannot exceed 9 
digits 
DQUA  ODLI REJT Cannot have both 
Odd Lot and 
Conditional 
Quantity 
Instruction can 
only have either 
the Odd Lot or the 
Conditional 
Quantity. 
DQUA  OVRG REJT Oversubscription 
quantity is greater 
Oversubscription 
quantity cannot be 
greater than 
[[DTCC]] Public (White)

---

## Page 48

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 48 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
than percentage of 
underlying [[shares]]. 
percentage of 
underlying [[shares]]. 
DQUA  OVRI REJT Oversubscription 
quantity is invalid. 
Oversubscription 
is provided on 
Cover Protect. 
Oversubscription 
quantity is invalid. 
Oversubscription 
quantity should not 
be provided on 
Cover Protect. 
[This is 
systemically 
calculated] 
DQUA  OVRX REJT Oversubscription 
is not allowed. 
Oversubscription 
quantity must not 
be included when 
there is no 
oversubscription 
privilege. 
DQUA  RQDV REJT Rights Quantity 
Not Divisible By 
the required 
instruction integral 
multiple. 
Rights quantity for 
this subscription 
must be divisible 
by the required 
instruction integral 
multiple. 
DQUA  SUME REJT Core Instruction 
Quantity and 
Extension 
Transaction 
Details Difference 
Total instructed 
quantity in the core 
must equal the 
sum of all the 
instruction quantity 
transaction details 
at the extension. 
DQUA  SUMO REJT Core Instruction 
Oversubscription 
Quantity and 
Extension 
Transaction 
Details Difference 
Total instructed 
oversubscription 
quantity in the core 
must equal the 
sum of all the 
oversubscription 
instruction quantity 
transaction details 
at the extension. 
DQUA  TRQ0 REJT Transaction 
quantity is zero. 
Transaction 
Quantity Cannot 
Be Zero 
DQUA  TRQI REJT Transaction 
Quantity Missing 
or Invalid 
Transaction 
Quantity must be 
provided and must 
be in the right 
format. 
DQUA  TRQM REJT Transaction 
Quantity Less 
Transaction 
quantity must meet 
[[DTCC]] Public (White)

---

## Page 49

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 49 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
Than Transaction 
Minimum 
the minimum 
required. 
DSEC Unrecognized or 
invalid financial 
instrument 
identification. 
CUSI REJT Target [[CUSIP]] or 
Contra [[CUSIP]] 
identification is 
missing or invalid 
[[CUSIP]] must be 
provided ad must 
match the [[CUSIP]] 
on the 
announcement of 
the event being 
instructed. 
DUPL Duplicate 
Instruction 
 REJT Transaction 
Identification 
Invalid 
Business Message 
Identifier in CAIN 
cannot be a 
duplicate or re- 
used. It must be a 
unique identifier. 
EVNM Unrecognized CA 
[[ID]] or COAF [[ID]] 
ASOP REJT PSOP offer not yet 
approved by the 
agent 
Event must be 
approved by agent 
before submitting 
instructions. 
EVNM  ATOP REJT PTOP Offer is not 
yet approved by 
agent. 
Event must be 
approved by agent 
before submitting 
instructions. 
EVNM  CAID REJT Corporate action 
event identification 
is invalid or out of 
scope. Event is 
cancelled or 
deleted. 
Event must be 
valid and active. If 
client provides the 
COAF, then CA [[ID]] 
validation is not 
required. 
Otherwise, the CA 
[[ID]] must be 
provided and must 
match CA Web. 
EVNM  EVNT REJT Incorrect Event 
Type 
Event Type must 
correspond to the 
given CA or COAF 
[[ID]] from CANO 
EVNM  OFFP REJT PUTS Offer is not 
yet approved by 
agent. 
Event must be 
approved by agent 
before submitting 
instructions. 
ISOL Invalid Solicitation 
Dealer Fee Use 
SOCR REJT Solicitation Fee 
Comments is 
missing. 
Solicitation Fee 
Comments 
Required 
[[DTCC]] Public (White)

---

## Page 50

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 50 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
ISOL  SOLX REJT Solicitation Fee 
Indicator is not 
required. 
Solicitation Fee 
Indicator cannot be 
populated when 
not required. 
LACK Instructed position 
exceeds the 
eligible balance. 
CHIL REJT [[CUSIP]] is 
Depository Deliver 
Chilled 
[[CUSIP]] must not be 
chilled. 
LACK   RECY Recycle Instruction with 
insufficient position 
will subsequently 
become either 
“Made” or 
“Dropped” by end 
of day. 
LACK   DROP Dropped Instruction dropped 
due to insufficient 
position.  
NMTY Mismatch between 
[[Option]] number and 
[[Option]] type. 
N/A REJT Mismatch between 
[[Option]] number and 
[[Option]] type. 
[[Option]] number and 
[[Option]] type must 
match as 
announced. 
NORE No reason  REJA Withdrawal 
rejected by agent 
 
OPNM Unrecognized 
[[Option]] number. 
N/A REJT [[Option]] number is 
invalid. 
[[Option]] number 
must match the 
one in the 
announcement. 
OPTY Invalid [[Option]] 
Type 
 REJT [[Option]] Type 
Invalid 
The [[Option]] type in 
CAIN must be an 
[[Option]] supported 
by [[DTC]]. Non- 
supported options 
will have the [[Option]] 
feature code of 
“NOSE” in CANO. 
 
OTHR Other reason BNDU REJT Bond Check on 
Master Is Table 
Not Available 
The Security 
Masterfile Table 
must be available, 
in order to validate 
the security. 
OTHR  CSEQ REJT Customer 
Sequence number 
is invalid or out of 
sequence 
Customer 
sequence number 
must be in 
chronological order 
[[DTCC]] Public (White)

---

## Page 51

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 51 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
and must be valid [ 
up to 99 ]. 
OTHR  CUST REJT Customer 
Reference 
Identification is 
missing or invalid 
Customer 
Reference 
Identification must 
be populated for 
each sequence 
OTHR  ODLY REJT Odd Lot Indicator 
Yes is invalid. 
Cannot submit odd 
lot indicator 'Yes' 
for the offer. 
OTHR  QUIE REJT Instruction 
received after 
business hours 
Instruction must be 
sent within the 
[[DTC]] Start and End 
Time 
OTHR  RTOP REJT Protect is pending 
client RTOP 
approval 
Protects submitted 
via RTOP must be 
approved by the 
client before 
covering. 
OTHR  SEQ0 REJT Customer 
Sequence number 
is zero 
Customer 
Sequence number 
cannot be zero. It 
must be from 1- 
99. 
OTHR  SEQD REJT Transaction 
sequence number 
is duplicated. 
Transaction 
sequence number 
cannot be 
duplicated. 
OTHR  SEQM REJT Sequence Number 
Missing 
Sequence number 
is required. 
OTHR  SEQP REJT Sequence Number 
Invalid Bounds 
Customer 
sequence number 
must be between 1 
and 1 or for PUTS 
between 9999901 
and 9999912. 
OTHR  SEQP REJT Instruction to 
cover a protect on 
oversubscription 
whereby the 
transaction 
sequence does 
not exist 
Transaction 
sequence number 
of the protect 
instruction is 
required when 
covering a protect. 
OTHR  SEQP REJT Instruction to 
cover protect on 
oversubscription is 
Instruction to cover 
protect on 
oversubscription 
[[DTCC]] Public (White)

---

## Page 52

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 52 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
covering more 
than one 
transaction 
sequence 
cannot cover more 
than one 
transaction 
sequence. 
OTHR  SEQP REJT Instruction to 
cover a protect on 
oversubscription 
where the 
transaction 
sequence exceeds 
99. 
Transaction 
sequence number 
cannot exceed 99 
when instructing to 
cover a protect. 
OTHR  TRNS REJT Transaction 
Sequence Number 
Transaction 
Sequence Number 
not applicable 
OTHR  TRTI REJT Transaction Type 
Invalid 
COVP is currently 
not available 
PROI Missing Protect 
Identification  
 REJT Protect 
identification is 
missing or invalid. 
When submitting 
an instruction to 
cover a protect, the 
Protect [[ID]] must be 
provided as part of 
the instruction. 
PROI   REJT Protect 
Identification not 
used 
Protect [[ID]] should 
not be provided 
when submitting a 
Protect. 
PRON No Protect 
Privilege 
TNFN REJT Transaction Type 
And Event 
Incompatible 
Transaction type is 
not required or 
invalid. 
PROT Missing Protect 
Date 
 REJT Protect Date 
Missing or Invalid 
When submitting a 
protect instruction, 
Protect Date is not 
required. 
When submitting 
an instruction to 
cover a protect, a 
valid Protect Date 
is required as part 
of the instruction. 
[Protect Date is the 
date the protect 
was submitted on 
the instruction that 
is being covered]. 
REJA Rejected by [[issuer]] 
Agent 
 REJT Rejected by [[issuer]] 
Agent 
Instruction rejected 
by the agent. 
[[DTCC]] Public (White)

---

## Page 53

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIS MESSAGES 53 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
SAFE Unrecognized or 
invalid message 
sender's 
safekeeping 
account. 
PACH REJT [[participant]] is [[DO]] 
chilled. 
[[participant]] [[ID]] must 
not be chilled for 
delivery orders. 
SAFE  PAPI REJT [[participant]] No 
Match on Protect 
Identification 
When submitting 
an instruction to 
cover a protect, a 
valid [[participant]] 
number is required 
as part of the 
instruction. [It must 
be the [[participant]] 
number associated 
with the protect 
that is being 
covered.] 
SAFE  PARL REJT [[participant]] is 
globally locked. 
[[participant]] must 
not be globally 
locked. 
SAFE  PART REJT [[participant]] 
Number Invalid 
When submitting a 
protect instruction, 
[[participant]] number 
is not required. 
SAFE  PARX REJT Not a CDS 
[[participant]] 
Must be a 
Canadian 
Depository 
[[participant]] 
SHAR Unrecognized, 
missing, or invalid 
shareholder 
number. 
 REJT Unrecognized, 
missing, or invalid 
shareholder 
number. The 
shareholder 
number exceeds 
25 characters. 
Shareholder 
number must be 
provided when the 
[[Option]] requires 
Allocation Identifier 
Code. It must not 
exceed 25 
characters. 
[[DTCC]] Public (White)

---

## Page 54

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIC MESSAGES 54 
CAIC MESSAGES 
 
OR 
 
What Is a CAIC Message? 
The Corporate Action Instruction Cancellation Message (CAIC) is an inbound message sent by participants to 
[[DTC]] to communicate withdrawal of a previously submitted and accepted voluntary corporate action 
reorganization instructions. 
MX Identifier ISO 20022 Message 
Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTC]] 
Processes 
seev.040.002.xx3 Corporate Action 
Instruction Cancellation 
supl.032.001.xx1 CAIC MT 565 Instructions 
Withdrawal 
 
3 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Supplementary version number  
may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on the “MyStandards” section of the official SWIFT website and [[DTCC]].com . 
[[DTCC]] Public (White)

---

## Page 55

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIC MESSAGES 55 
General Rules 
1. To withdraw an existing instruction, the [[DTC]] Withdrawal Privilege Flag on the event must be set to Y in 
CA Web. In CANO, the Withdrawal Allowed Indicator at the [[Option]] level is set to True.  
2. Withdrawals only apply to events that are PTOP eligible and have a withdrawal privilege (e.g., Tenders, 
Exchange Offers, Merger (VOLU), Tender (Bid/Sealed) and Dutch Auction. 
3. Instructions must be in MADE status and must not have been allocated. 
4. Partial withdrawals are not allowed when withdrawing via CAIC. 
5. [[participant]] must have the Business Message Identifier [BizMsgIdr] within the Business Application 
Header of the CAIC message. Each BizMsgIdr must be unique for a customer for each message. When 
message is received by [[DTC]], the schema and subscription will be validated, and the message will be 
checked against the “restricted” CAIC schema. 
6. The Safekeeping Account must be a [[DTC]] assigned [[participant]] number. The format is 8 digits with leading 
zeros as applicable. (i.e., part# 902 should read “00000902,” Part# 5 should read “00000005”).  
7. If both the schema and subscription validations are successful, an ACK message goes out to the sender. 
If not, a NAK message will be sent back to the client. If the CAIC schema is not well -formed, a NAK 
message with a reason code of SCHM is generated. If the CAIC schema is well-formed but the 
subscription validation failed, a NAK message with a reason code of SECU is generated.  
8. All CAIC messages that receive a network ACK will also receive a CACS response.  
If the withdrawal instruction failed the business rule validation, a CACS Reject will be sent to the sender 
with the appropriate reject code. If it passes the business rule validation, a CACS message with the status 
of PENA (Pending Agent Approval) will be sent to the sender. Once the agent approves the withdrawal 
instruction, a final CACS with the status of WITH (Withdrawn) goes out to the sender. The timing of the 
final CACS depends on when the agent approves or rejects the withdrawal request. Additionally, a CAIS 
message will generate with the Instruction processing status of Cancelled and a reason code of CANI 
(Cancelled by Yourself) in the core and a Transaction [[ID]] Status of WITH (Withdrawn).  
9. Each withdrawal message must contain an instruction for only one [[Option]]. You cannot withdraw for two 
different instructions on a single message. 
10. Instructions submitted manually via PTOP may be withdrawn via CAIC if the amount is being withdrawn in 
full, with the exception of instructions submitted via PTOP on events with Early and Late Options. These 
can only be withdrawn via PTOP. 
11. The CAIC message will have mandatory and optional fields. Please see the Message Usage Guideline 
and Instruction Data Dictionary for a list of these fields. They will be documented in this guide also.  
[[DTCC]] Public (White)

---

## Page 56

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIC MESSAGES 56 
Fields in CAIC Core Message 
Field Name Mandatory Notes Tag(s) 
Instruction 
Identification 
Y [[DTCC]] will match it to the Business 
Message Identifier of the CAIN Instruction 
that is being cancelled. If instruction being 
withdrawn was submitted via PTOP, this 
field should be populated with the text 
NONREF. 
/Document/CorpActnInstrCxlReq/InstrI d 
Corporate Action 
Event Identification 
(CA [[ID]]) 
Y Must match what was on the CAIN 
instruction that is being cancelled. 
Note: 
If client uses their own internal CA [[ID]], the 
[[DTCC]] COAF [[ID]] must also be provided in 
the message. 
/Document/CorpActnInstrCxlReq/Corp 
ActnGnlInf/CorpActnEvtId 
Official Corporate 
Action Event 
Identification 
(COAF) 
N Must match what was on the CAIN 
instruction that is being cancelled. This is 
an optional field unless the CA [[ID]] provided 
is a non-[[DTC]] CA [[ID]]. 
/Document/CorpActnInstrCxlReq/Corp 
ActnGnlInf/OffclCorpActnEvtId 
Event Type Code Y Must match the event type from the CAIN 
message being cancelled. 
/Document/CorpActnInstrCxlReq/Corp 
ActnGnlInf/EvtTp/Cd 
Security 
Identification 
([[Option]] Level / 
Contra) 
Y Identification of the security concerned by 
the corporate action. Must use the Contra 
[[CUSIP]]. 
/Document/CorpActnInstrCxlReq/Corp 
ActnGnlInf/FinInstrmId/OthrId/[[ID]] 
Safekeeping 
Account 
Y [[DTC]] [[participant]] number. /Document/CorpActnInstrCxlReq/AcctD 
tls/SfkpgAcct 
[[Option]] Number Y Number that uniquely identifies an [[Option]] 
within an event. 
Note:  
Must be the same [[Option]] number provided 
from the CAIN being cancelled. 
/Document/CorpActnInstrCxlReq/Corp 
ActnInstr/OptnNb/Nb 
[[Option]] Type Y Describes the type of [[Option]] associated 
with the event. 
Note: 
Must match [[Option]] type from the CAIN 
being cancelled 
/Document/CorpActnInstrCxlReq/Corp 
ActnInstr/OptnTp/Cd 
[[DTCC]] Public (White)

---

## Page 57

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIC MESSAGES 57 
Field Name Mandatory Notes Tag(s) 
Instructed Quantity Y Quantity of [[securities]] to which this 
instruction applies. Must be less than a 
billion. 
Must be a whole number. 
Note: 
The withdrawn quantity must be the full 
amount of the original instructed quantity. 
/Document/CorpActnInstrCxlReq/Corp 
ActnInstr/InstdQty/Qty/Unit or Amt 
Protect Instruction 
(Transaction Type) 
N (unless 
instruction 
being 
withdrawn is 
a Protect) 
Indicates that the instruction is a protect. 
(This applies when the instruction being 
withdrawn is a Protect instruction.) 
Note: 
This is mandatory for protect withdrawal. 
The transaction type is PROT. Covered 
Protect withdrawals are treated like any 
regular instruction withdrawal and 
therefore this tag will not be required when 
withdrawing a Covered Protect. 
/Document/CorpActnInstrCxlReq/PrtctI 
nstr/TxTp 
Protect Date N (unless 
instruction 
being 
withdrawn is 
a Protect) 
Date at which the protect instruction was 
created. 
Note: 
This field is mandatory when withdrawing a 
protect instruction. 
/Document/CorpActnInstrCxlReq/PrtctI 
nstr/PrtctDt 
Additional 
Information 
N Provides additional information or specifies 
in more detail the content of a message. 
/Document/CorpActnInstrCxlReq/AddtlI
nf/AddtlTxt 
Fields in CAIC Supplement Message 
Field Name Mandatory Notes Tag(s) 
Transaction 
Identification 
Y Unique number assigned by the 
depository. Transaction identification will 
be either the [[DTC]] instruction reference 
number for reorganization instructions 
(VOI) or the Protect [[ID]]. 
/Document/DTCCCAICSD1/ReorgInstr 
CxlDtls/TxId 
Customer 
Reference 
Identification 
N Customer identification entered by client 
upon instruction submission. 
Note: 
Maximum length of 30 characters. 
/Document/DTCCCAICSD1/ReorgInstr 
CxlDtls/CstmrRefId 
Contact Person 
Name 
Y Name by which a party is known, and 
which is usually used to identify that 
party. Maximum length is 20 bytes 
/Document/DTCCCAICSD1/ReorgInstr 
CxlDtls/CtctPrsn/Nm 
[[DTCC]] Public (White)

---

## Page 58

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIC MESSAGES 58 
Field Name Mandatory Notes Tag(s) 
Contact Person 
Phone Number 
Y Phone number, as defined by telecom 
services. 
/Document/DTCCCAICSD1/ReorgInstr 
CxlDtls/CtctPrsn/PhneNb 
What is a CACS Message? 
A Corporate Action Cancellation Status Advise message (CACS) is an outbound response that indicates 
whether a Corporate Action Instruction Cancellation (CAIC) message submitted by a [[participant]] has been 
accepted or rejected. [[DTC]] sends a CACS to inform a [[participant]] of a cancellation message’s status.  
MX Identifier ISO 20022 Message 
Names 
Extension Short 
Name 
Equivalent 
ISO 15022 
Equivalent [[DTC]] 
Processes 
seev.041.002.xx4 Corporate Action 
Cancellation Status 
supl.033.001.xx1 CACS MT 567 Instructions 
Withdrawal 
If a CAIC message is successfully accepted and processed, [[DTC]] will send a CACS message to the originating 
[[participant]] which indicates the status of the CAIC message as follows: 
Upon receipt of the valid CAIC message, a CACS message with the Instruction Cancellation Request status of 
Pending Cancellation and a reason code NORE (No reason) in the core and a Transaction [[ID]] status of PENA 
(Pending Approval) in the extension will be sent out. 
Once the agent reviews and approves the instruction withdrawal and the position has been moved back from 
the contra [[CUSIP]] to the event [[CUSIP]], a CACS message with the Instruction Cancellation Request status of 
Accepted with a reason code NORE (No reason) in the core and a Transaction [[ID]] status of WITH (Withdrawn) 
in the extension goes out to the sender. 
If the agent rejects the instruction withdrawal, a CACS message with the Instruction Cancellation Request 
status of Rejected with a reason code REJA (Rejected by [[issuer]] Agent) in the core is generated. There will be 
no Rejection Reason code in the extension. 
If the instruction withdrawal failed any of the business validation rules before sending to the agent for review, a 
CACS message with the Instruction Cancellation Request status of Rejected with the appropriate reason code 
(See CACS Reject Codes table) in the core and a Transaction [[ID]] status of REJT (R ejected – did not pass 
initial validation) plus the corresponding reject reason code in the extension will be sent out.  
 
4 The last two digits in the MX Identifier and the Extension code signify the version number. The MX version number and/or the Su pplementary version number 
may change during the SWIFT annual release based on mandatory or optional updates to the standards and extensions.  
Current schemas are available on the “MyStandards” section of the official SWIFT website and [[DTCC]].com . 
[[DTCC]] Public (White)

---

## Page 59

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIC MESSAGES 59 
Information Contained on the CACS Core Message 
The following table contains all the information elements presented on a CACS message, along with an 
explanation of what each element means and/or applicable details. 
Data Element Definition/Information Received from 
CAIC 
Instruction? 
Instruction 
Cancellation Request 
Identification 
The Business Message Identifier of the received CAIC instruction. (Minimum 
length of 1 and maximum length of 16). 
/Document/CorpActnInstrCxlReqStsAdvc/InstrCxlReqId/[[ID]] 
YES 
Corporate Action 
Event Identification 
Specified on the received instruction. 
If a [[participant]] / sender provides their own CA [[ID]], then this will appear on the 
CAIS message. 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnGnlInf/CorpActnEvtId 
YES 
Official Corporate 
Action Event 
Identification 
Must match what was on the CAIC instruction. This is an optional field unless 
the CA [[ID]] provided is a non-[[DTC]] CA [[ID]]. 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnGnlInf/OffclCorpActnEvtI d 
YES 
Event Type The type of corporate action event that was being referred to in the CAIC 
message. 
/Document/CorpActnInstrStsAdvc/CorpActnGnlInf/EvtTp 
YES 
[[Option]] Number Number identifying the available corporate action [[Option]] stated on the CAIC 
being withdrawn. 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnInstr/OptnNb 
YES 
[[Option]] Type The type of [[Option]] stated on the CAIC being withdrawn. 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnInstr/OptnTp 
YES 
Safekeeping Account [[participant]] [[ID]] stated on the CAIC 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnInstr/SfkpgAcct 
YES 
Financial Instrument 
Identification 
Identifies the financial instrument and its type (Proprietary type is used for 
Contra [[CUSIP]]) 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnInstr/FinInstrmId/OthrId/Tp/
Prtry 
YES 
Total Eligible Balance Total balance of [[securities]] eligible for this corporate action event. The 
[[Entitlement]] calculation is based on this balance. 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnInstr/TtlElgblBal/QtyChc/Qty 
NO 
Instructed Balance Balance of instructed position. 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnInstr/InstdBal/QtyChc/Qty 
NO 
Uninstructed Balance Balance of uninstructed position. 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnInstr/UinstdBal/QtyChc/Qty 
NO 
Protect Balance Balance of [[securities]] which are in protect status. NO 
[[DTCC]] Public (White)

---

## Page 60

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIC MESSAGES 60 
Data Element Definition/Information Received from 
CAIC 
Instruction? 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnInstr/PrtctBal/QtyChc/Qty 
Status Quantity Quantity of [[securities]] that has been assigned the status indicated. 
/Document/CorpActnInstrCxlReqStsAdvc/CorpActnInstr/StsQty 
NO 
Protect Instruction 
Transaction Type 
Indicates whether the instruction is a protect or a cover protect instruction. 
/Document/CorpActnInstrCxlReqStsAdvc/PrtctInstr/TxTp 
YES 
Protect Date Date at which the protect instruction was created 
/Document/CorpActnInstrCxlReqStsAdvc/PrtctInstr/PrtctDt 
YES 
Additional Information Additional Information provided 
/Document/CorpActnInstrCxlReqStsAdvc/AddtlInf/AddtlTxt 
NO 
Information Contained on the CACS Supplemental Message 
Data Element Definition/Information Received from 
CAIC 
Instruction? 
Transaction [[ID]] Transaction [[ID]] (VOI) of the instruction being withdrawn. 
/Document/DTCCCACSSD1/ReorgInstrCxlDtls/TxId 
YES 
Transaction [[ID]] Status Status of the instruction. (REJT, WITH). 
/Document/DTCCCACSSD1/ReorgInstrCxlDtls/TxIdSts 
NO 
Rejection Reason Reason for which a cancellation instruction message is rejected. 
/Document/DTCCCACSSD1/ReorgInstrCxlDtls/RjctnRsn 
NO 
Customer Reference 
Identification 
Customer identification entered by client upon instruction submission. 
/Document/DTCCCACSSD1/ReorgInstrCxlDtls/CstmrRefId 
YES 
Contact Person Name Name by which a party is known, and which is usually used to identify that 
party. 
/Document/DTCCCACSSD1/ReorgInstrCxlDtls/CtctPrsn/Nm 
YES 
Contact Phone 
Number 
Phone number of the CAIC Sender 
/Document/DTCCCACSSD1/ReorgInstrCxlDtls/CtctPrsn/PhneNb 
YES 
CACS Reject Codes 
The following table contains lists of error codes and their explanations, including an elaboration on the “OTHR” error code. 
It provides a list of the real-text reasons that can accompany this code on a rejection message.  
Instruction Processing Status: Rjctd (Rejected) 
[[DTCC]] Public (White)

---

## Page 61

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIC MESSAGES 61 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
CTCT Missing Contact 
Information 
CNAM  REJT Contact Name 
Missing 
Contact Name of the 
submitter of 
instruction is 
mandatory. 
CTCT Missing Contact 
Information 
 CNPM REJT Contact Phone 
Number Missing 
Phone Number of the 
submitter of 
instruction is 
mandatory. 
DCAN Rejected since 
instruction is 
already cancelled. 
 REJT  Instruction already 
withdrawn or 
withdrawal is in 
progress cannot be 
withdrawn again. 
DQUA Invalid Quantity  TRQI REJT Transaction 
Quantity incorrect 
Amount being 
withdrawn must 
match the original 
instruction’s amount. 
It cannot be above or 
below the original 
instructed quantity. 
DSEC Invalid Security CUSI REJT [[CUSIP]] missing or 
invalid 
A valid contra [[CUSIP]] 
must be provided 
DUPL Duplicate 
Instruction 
 REJT  Business Message [[ID]] 
on each message 
must be unique for 
each [[participant]]. 
INIR Instruction 
Irrevocable 
NWIT REJT No withdrawal 
privilege 
Events without 
withdrawal privilege 
cannot be withdrawn 
or cancelled. 
OTHR Other Reason ALLO REJT Payment on the 
event has already 
been allocated. 
Instructions cannot be 
withdrawn on events 
that have been paid 
by the agent. 
OTHR Other Reason CHIL REJT [[CUSIP]]  
Depository Deliver 
Chilled 
Instruction cannot be 
withdrawn on a 
chilled [[CUSIP]] 
OTHR Other Reason EVNM REJT Invalid Event Type Event Type must 
match the event type 
of the instruction 
being withdrawn 
OTHR Other Reason FUNU REJT Function not 
available 
System outage or 
database not 
available when 
[[DTCC]] Public (White)

---

## Page 62

ISO 20022 Messaging for Reorganizations Instructions User Guide 
CAIC MESSAGES 62 
Instruction 
Processing 
Status Rejected 
Reason Code 
[Core Message] 
Reject Reason 
Code Description 
Rejection Reason 
Code [Extension] 
Transaction 
Identification 
Status 
[Extension] 
Description 
Reject Reason 
Code [Extension] 
Rules 
instruction was 
received. 
OTHR Other Reason NELG REJT Instruction is not in 
MADE status. 
Instruction with status 
other than MADE 
cannot be withdrawn. 
(eg. PEND, DROP, 
RECY, RESC). 
OTHR Other Reason OPNM REJT Invalid [[Option]] 
Number 
[[Option]] Number must 
match the [[Option]] 
number of the 
instruction being 
withdrawn 
OTHR Other Reason OPTY REJT Invalid [[Option]] Type [[Option]] Type must 
match the [[Option]] type 
of the instruction 
being withdrawn 
OTHR Other Reason TRNI REJT Transaction [[ID]] 
invalid 
The VOI number of 
the instruction being 
withdrawn must be 
valid. 
PROI Missing or Invalid 
Protect [[ID]] 
 REJT  When withdrawing a 
Protect, a valid 
Protect [[ID]] must be 
provided. 
PROT Missing Protect 
Date 
 REJT  When withdrawing a 
protect, Protect Date 
is required. 
REJA Rejected by Agent  REJA Agent rejected the 
withdrawal 
Withdrawal must be 
approved by the 
agent 
SAFE Safekeeping 
Account  
PARL REJT [[participant]] Locked The [[participant]] 
Number must not be 
locked. 
TRTI  Missing or Invalid 
Transaction Type 
 REJT  When withdrawing a 
protect, Tran Type 
PROT is required. 
ULNK   REJT Business Message 
Identifier invalid 
The Business 
Message Identifier of 
the CAIN being 
withdrawn must be 
valid 
ULNK Invalid Reference CAID REJT Corporate Action 
event [[ID]] or Official 
Corporate Action 
[[ID]] invalid 
Must be a valid COAF 
or CA [[ID]] 
[[DTCC]] Public (White)

---

## Page 63

ISO 20022 Messaging for Reorganizations Instructions User Guide 
APPENDIX A: INSTRUCTION MESSAGING ELIGIBILITY 63 
APPENDIX A: INSTRUCTION MESSAGING ELIGIBILITY 
At this time, clients can only instruct on items containing a Y in the final column.  
Other voluntary event types currently listed as N may be considered at a later phase. 
Note: 
[[DTC]] mandatory events will always have the instruction messaging eligibility flag set to “N.” 
NEW MODEL [[DTC]] LEGACY 
Event Name Sub Event 
Name 
[[issuer]]/Offeror 
MAND /  
CHOS / VOLU 
[[DTC]] 
when applicable 
MAND / CHOS / VOLU 
Function 
Code / 
Activity Code 
Instructions Messaging 
Eligibility Flag 
CD Early 
Redemption 
 VOLU VOLU AC-53 N 
Change Domicile MAND MAND AC-93 N 
Change Domicile New 
[[CUSIP]] 
MAND MAND AC-93 N 
Change Domicile 
Presentation 
Required 
MAND MAND AC-93 N 
Change Domicile / 
New [[CUSIP]] / 
Presentation 
Required 
MAND MAND AC-93 N 
Consent With Payout VOLU VOLU AC-80 
AC-52 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Consent Without 
Payout 
VOLU VOLU AC-80 
AC-52 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Conversion  MAND MAND AC-93 N 
Conversion  VOLU VOLU AC-54 
AC-54N 
AC-52 
AC 54/54N: Set Flag to N 
AC 52 Processed at [[DTC]] 
= Yes / Flag Y 
Dutch Auction  VOLU VOLU AC-52 
AC-52N 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
[[DTCC]] Public (White)

---

## Page 64

ISO 20022 Messaging for Reorganizations Instructions User Guide 
APPENDIX A: INSTRUCTION MESSAGING ELIGIBILITY 64 
NEW MODEL [[DTC]] LEGACY 
Event Name Sub Event 
Name 
[[issuer]]/Offeror 
MAND /  
CHOS / VOLU 
[[DTC]] 
when applicable 
MAND / CHOS / VOLU 
Function 
Code / 
Activity Code 
Instructions Messaging 
Eligibility Flag 
Dutch Auction Consent VOLU VOLU AC-52 
AC-52N 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Exchange Offer 144a VOLU VOLU AC-52 
AC-52N 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Exchange Offer  VOLU VOLU AC-52 
AC-52N 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Exchange Offer Cash and 
[[securities]] 
VOLU VOLU AC-52 AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Exchange Offer Consent VOLU VOLU AC-52 
AC-52N 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Exchange Offer [[Reg S]] VOLU VOLU AC-52 
AC-52N 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Exchange Offer Unwind VOLU VOLU AC-51 Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Exchange Offer  VOLU VOLU AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Full Call Conversion MAND MAND AC-69 N 
[[DTCC]] Public (White)

---

## Page 65

ISO 20022 Messaging for Reorganizations Instructions User Guide 
APPENDIX A: INSTRUCTION MESSAGING ELIGIBILITY 65 
NEW MODEL [[DTC]] LEGACY 
Event Name Sub Event 
Name 
[[issuer]]/Offeror 
MAND /  
CHOS / VOLU 
[[DTC]] 
when applicable 
MAND / CHOS / VOLU 
Function 
Code / 
Activity Code 
Instructions Messaging 
Eligibility Flag 
General 
Information 
 MAND MAND AC-93 N 
General 
Information 
Important 
Notice 
MAND MAND AC-96 N 
[[liquidation]] Presentation 
Required 
MAND MAND AC-79 
AC-93 
N 
Mandatory 
Exchange 
 MAND MAND AC-93 N 
Mandatory Put  MAND MAND AC-65 AC-65G N 
Mandatory Put Retain CHOS CHOS AC-65B AC-
65R 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No  
Flag N 
Maturity Conversion MAND MAND AC-69 N 
Maturity [[securities]] MAND MAND AC-93 N 
Meeting Annual MAND MAND AC - 80 N 
Meeting Extraordinary MAND MAND AC - 80 N 
Meeting General MAND MAND AC - 80 N 
Meeting Special MAND MAND AC - 80 N 
Merger  MAND MAND AC-93 N 
Merger  VOLU VOLU AC-52M (s) Processed at [[DTC]] = Yes  
Flag Y 
Processed at [[DTC]] = No  
Flag N 
Merger Cash MAND MAND AC-72 N 
Merger Cash and 
[[securities]] 
MAND MAND AC-90 N 
Merger [[securities]] MAND MAND AC-71 N 
Name Change  MAND MAND AC-91 AC- 93 N 
Name Change Presentation 
Required 
MAND MAND AC-91 AC-93 N 
[[DTCC]] Public (White)

---

## Page 66

ISO 20022 Messaging for Reorganizations Instructions User Guide 
APPENDIX A: INSTRUCTION MESSAGING ELIGIBILITY 66 
NEW MODEL [[DTC]] LEGACY 
Event Name Sub Event 
Name 
[[issuer]]/Offeror 
MAND /  
CHOS / VOLU 
[[DTC]] 
when applicable 
MAND / CHOS / VOLU 
Function 
Code / 
Activity Code 
Instructions Messaging 
Eligibility Flag 
Name Change [[CUSIP]] 
Change / 
Presentation 
Required 
MAND MAND AC-91 AC-93 N 
Name Change New [[CUSIP]] MAND MAND AC-91 AC-93 N 
Odd Lot Offer  VOLU VOLU AC-52 AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Partial 
Mandatory Put 
 MAND MAND AC-65P N 
Partial 
Mandatory Put 
Retain CHOS CHOS AC-65 AC-65R Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Plan of 
Reorganization 
[[vote]] VOLU VOLU AC-94 N 
Plan of 
Reorganization 
 MAND MAND AC-94 N 
Put  VOLU VOLU AC-52 AC-58 
AC-58B AC-
58N 
Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Put Mortgage- 
Backed 
VOLU VOLU AC-62 AC-62B N 
Put Survivor 
Options 
VOLU VOLU AC-66P N 
Redemption of 
[[Warrants]] 
 MAND MAND AC-61 N 
Reorganization  MAND MAND AC-93 N 
Reorganization  VOLU VOLU AC-52 AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
[[DTCC]] Public (White)

---

## Page 67

ISO 20022 Messaging for Reorganizations Instructions User Guide 
APPENDIX A: INSTRUCTION MESSAGING ELIGIBILITY 67 
NEW MODEL [[DTC]] LEGACY 
Event Name Sub Event 
Name 
[[issuer]]/Offeror 
MAND /  
CHOS / VOLU 
[[DTC]] 
when applicable 
MAND / CHOS / VOLU 
Function 
Code / 
Activity Code 
Instructions Messaging 
Eligibility Flag 
Reverse [[Stock]] 
Split 
 MAND MAND AC-73 AC-93 N 
Rights 
Subscription 
 VOLU VOLU AC-59 AC-93 Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Security 
Separation 
 MAND MAND AC-93 N 
Security 
Separation 
 VOLU  AC-54N N 
[[Stock]] Split Presentation 
Required 
MAND MAND AC-93 N 
Tender Offer Bid Tender/ 
Sealed 
Tender 
VOLU VOLU AC-52 AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Tender Offer Cash and 
[[securities]] 
VOLU VOLU AC-52 AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Tender Offer Cash in Lieu  VOLU AC-52 Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Tender Offer Consent VOLU VOLU AC-52 AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Tender Offer Mini Tender VOLU VOLU AC-52 AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
[[DTCC]] Public (White)

---

## Page 68

ISO 20022 Messaging for Reorganizations Instructions User Guide 
APPENDIX A: INSTRUCTION MESSAGING ELIGIBILITY 68 
NEW MODEL [[DTC]] LEGACY 
Event Name Sub Event 
Name 
[[issuer]]/Offeror 
MAND /  
CHOS / VOLU 
[[DTC]] 
when applicable 
MAND / CHOS / VOLU 
Function 
Code / 
Activity Code 
Instructions Messaging 
Eligibility Flag 
Tender Offer Offer to 
Purchase 
VOLU VOLU AC-52 AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Tender Offer Self Tender VOLU VOLU AC-52 AC-52N Processed at [[DTC]] = Yes 
Flag Y 
Processed at [[DTC]] = No 
Flag N 
Termination [[ADR]] MAND MAND AC-93 N 
Termination GDR MAND MAND AC-93 N 
Termination [[ADR]] VOLU VOLU AC-52N N 
Termination GDR VOLU VOLU AC-52N N 
[[Warrants]] 
Exercise 
 VOLU VOLU AC-60 
AC-60N AC-52 
AC 60/60N: Set Flag to N 
AC 52: Processed at [[DTC]] 
= Yes / Flag Y 
Worthless  MAND MAND AC-93 N 
[[DTCC]] Public (White)

---

## Page 69

ISO 20022 Messaging for Reorganizations Instructions User Guide 
REVISION HISTORY 69 
REVISION HISTORY 
10/30/23 Deleted fields in CACS Reject Codes Table (pages 64-66) 
10/30/23 Added CACS Reject Codes Table (page 61) 
10/30/23 Instruction Processing Status Rjctd (Rejected) Table 
Reformatted (page 51) 
10/30/23 Rejection Reason Code: RECY removed from Instruction 
Processing Status Rjctd (Rejected) Table (page 50) 
10/30/23 The following text added on page 29: “When submitting a 
Cover Protect for a ‘Specified Price’ instruction on a Tender 
(Bid/Sealed Price) and Dutch Auction, the bid price is not 
required in the CAIN message. The VRI application will 
verify the details of the instruction, including the bid price 
based on the Protect [[ID]] provided.” 
10/30/23 The phrase “and full” added to this sentence on page 29: 
“For partial and full cover scenarios, the cover quantity 
cannot exceed the amount of the open protect.” 
10/30/23 Text struck through (page 28). 
10/30/23 Font italicized and highlighted (pages 26 and 27). 
10/30/23 Font changed (page 24). 
10/30/23 Text struck through (page 17). 
10/30/23 Document reformatted to fit latest template. 
04/10/23 Added CAIC/CACS instructions for withdrawal. 
04/10/23 Added the “Redemption of Rights” Event Type to the 
“Events in Scope” and “Events Out of Scope” tables. 
04/10/23 Removed the “Pending Queue” section under “Lifecycle of 
an Instruction 
04/10/23 Added FaceAmt as a tag to Oversubscription Quantity and 
Total Oversubscription Quantity 
04/10/23 Added FaceAmt to Steps #5 and #6 under Rights Exercise 
Event Instruction Rules 
04/10/23 Removed Transaction Sequence and Transaction 
Sequence Instructed Quality rows in PUT Event Instruction 
General Rules Table. Also amended Customer Reference 
[[ID]] Field and xPath in this same table. 
04/10/23 Added “Protect Balance” field to the Information Contained 
on the CAIS Message Table. 
04/10/23 In the “Extension Elements” subtable, /TxSeqNb was 
removed from the Transaction Sequence field, and was 
added to the Transaction Sequence Number field. 
[[DTCC]] Public (White)

---

## Page 70

ISO 20022 Messaging for Reorganizations Instructions User Guide 
REVISION HISTORY 70 
FaceAmt was added to the Oversubscription Quantity field, 
(Rights Offer) was added to the Customer Reference 
Identification field, and a new Customer Reference 
Identification field was added for Puts Events. 
04/10/23 EVNM/ASOP, REJA, and OTHR/RTOP, three new reject 
codes, were added to the CAIS Reject Codes section. 
Amended the description of the EVNM/ATOP and 
EVNM/OFFP fields. Removed the reject code 
EVNM/OTHR. 
 
[[DTCC]] Public (White)

---

## Page 71

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
Doc Date: September 25, 2023 
Publication Code: CA223 
Service: Corporate Actions 
Title: ISO 20022 Messaging for Reorganizations Instructions User Guide 
For More Information 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 
[[DTCC]] Public (White)