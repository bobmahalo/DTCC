---
title: "EPN Overview"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs142_nov_epn_overview.pdf"
pages: 28
size: "400.1 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# EPN Overview

**Original File:** [mbs142_nov_epn_overview.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs142_nov_epn_overview.pdf)  
**Category:** MBSD  
**Total Pages:** 28  
**File Size:** 400.1 KB  

---

## Page 1

 
FIXED INCOME CLEARING CORPORATION 
EPN OVERVIEW 
VERSION 1.04 
FEBRUARY 10, 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the Interlocker graphic are registered and 
unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself 
does not provide such services.  Each of these affiliates is a separate legal entity, subject to the laws and regulations of the particular country or countries in whic h 
such entity operates. Please see www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: February 10, 2023 
Publication Code:  MBS142 
Service: Fixed Income Clearing Corporation 
Title: EPN Overview  
 
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ........................................................................................................................................................................ 5 
1. [[FICC]] Accounts for [[Novation]]........................................................................................................................................................... 6 
2. Valid EPN Message Types for [[Novation]] .......................................................................................................................................... 7 
2.1. ON .................................................................................................................................  7 
2.1.1. Bid List Allocation ............................................................................................................. 8 
2.2. CC .................................................................................................................................  9 
2.3. DK ............................................................................................................................... 10 
3. Additional Fields in EPN Header and Pool Detail ........................................................................................................................... 12 
3.1. Trade [[ID]] in EPN Message Header Special Instructions Field................................................. 12 
3.2. EPNX in EPN Pool Detail Special Instructions–EPN Pool Reference ...................................... 13 
3.3. TRID  and  EPNX Us ag e by  EPN Mess ag e Typ es.................................................................  14 
4. [[FICC]] Input Validation By EPN Message Types and Processing Mode.............................................................................................. 15 
4.1. Reminders on EPN Header Fields Validatio n: ..................................................................... 16 
4.2. Reminders on EPN Pool Detail Fields Validation: ................................................................ 16 
5. [[FICC]] Output to Members via EPN ................................................................................................................................................. 17 
5.1. Reminders on EPN Header Fields:.................................................................................... 17 
5.2. Reminders on EPN Pool Detail Fields: ............................................................................... 17 
6. EPN DK Reason Code .................................................................................................................................................................. 18 
7. EPN Reject Reason Code ............................................................................................................................................................. 20 
8. General EPN Guidelines............................................................................................................................................................... 23 
8.1. General EPN Guidelines:.................................................................................................  23 

---

## Page 4

 
 
8.2. [[FICC]] Processing Rules: .................................................................................................. 24 
Appendix A: Example DK Scenarios................................................................................................................................................. 25 
Appendix B: Example Scenarios for EPN Rejects.............................................................................................................................. 27 
 

---

## Page 5

EPN Overview 
 
Version C ontrol Page  5 
VERSION CONTROL PAGE 
Date Version # Name Description of Change  
07/17/2015 1.0 Jie Xie Initial version  
2/19/2016 1.01 Jie Xie Updated on TRID and EPNX descriptions  
Updated New EPN Reject Reason Code  
Correction on Reject Reason Code in Appendix II  
4/13/2016 1.03 Jie Xie Updated section 2 ON message on STIP allocations that bid list lots are not validated for 
SIFMA compliance, while regular STIP allocations/lots are.  
8/04/2016 1.04 Jie Xie 1. Updated ON processing rule that [[FICC]] match price on the first 6 decimal points when 
targeted Trade [[ID]] is included in the ON message. [[FICC]] match price on 9 decimal points 
when targeted Trade [[ID]] is NOT included in the ON submission.  
2. Matching pool term for DK and CC messages mandates price to match on the first 6 
decimal points.  
9/02/2016 1.04 Jie Xie Add 2 new DK reason codes 0140 and 0141 in section 6.  
n/a n/a [[DTCC]] Learning  Updated formatting only. Content is unchanged.  
02/10/2023 1.04 J. Sheeran  Updated document title from, “ MBS [[Novation]]: EPN OVERVIEW AND CHANGES” to “ EPN 
Overview”  
 

---

## Page 6

EPN Overview 
 
Version C ontrol Page  6 
1. [[FICC]] ACCOUNTS FOR [[Novation]] 
The table below contains the list of [[FICC]] account IDs that members would submit their EPN messages to. Different [[FICC]] account IDs are used for 
novated TBA trades based on the trade type. Members need to target the appropriate [[FICC]] account [[ID]] in the EPN Header, Contra field. 
 Pool 
Allocation 
Pool 
Obligation  
Generic TBA (SBON, TFT/TBA)  FTBA [[FICC]] 
Stipulated (TFT/STIP)  FSTI FSTI 
Specified (TFT /SPT)* FSPT FSPT 
 
*SPT Trades are not eligible for EPN processing. 

---

## Page 7

EPN Overview 
 
Version C ontrol Page  7 
2. VALID EPN MESSAGE TYPES FOR [[Novation]] 
Members are allowed to submit ON, DK, CC to [[FICC]]. CX submitted to [[FICC]] account IDs will be rejected by EPN. 
2.1. ON 
As central counterparty to all TBA trades, allocations must be submitted by sellers versus the appropriate [[FICC]] account via an EPN ON message. 
[[FICC]] will turn the validated ON message to the [[Buyer]](s) via EPN, and decrement the members’ open TBA position accordingly. [[FICC]] Pool Instructs 
against [[Seller]] and buyers will be created upon EPN allocations being processed. Members will receive an MT518 Pool Comparison Advisory from 
Pool Netting as the system does currently. Members may choose, but are not required to submit their matching Pool Instruct versus [[FICC]]; by the 
end of day, all unmatched [[FICC]] Pool Instructs versus members will be force compared, members’ Pool Instruct will be created on their behalf during 
the force comparison process. 
Allocation to Generic TBA positions (SBON, TFT/TBA, Contra being “FTBA”) are referred to as “generic allocations” in this document. Generic 
allocations target the [[Member]]’s TBA Sell trades by TBA term, or by TBA Trade [[ID]] if a valid Trade [[ID]] is included. [[FICC]] validates that the generic 
allocations are compliant with SIFMA good delivery guidelines, and that there is sufficient matching TBA position to fit the allocations. 
Below EPN Header fields defines the matching TBA term: 
1. Submitter 
2. Contra 
3. TBA [[CUSIP]] 
4. [[settlement]] Date 
5. Price–If Trade [[ID]] is included in the ON message, [[FICC]] will match up price to (including) the 6
th decimal points. If Trade [[ID]] is not included in the 
ON submission, [[FICC]] will match price up to (including) the 9th decimal points. 
6. Trade Date 
7. Original Trade PAR (part of matching term only for tail lot allocation) 
8. Trade [[ID]] (when included in the ON submission) 
 
Allocation to TFT/STIP positions (Contra being “FSTI”) are referred to as “STIP allocations” in this document. STIP allocations target a TBA position 
by a specific STIP Trade [[ID]] in addition to the TBA term. Since the stipulations of the trade are outside of [[FICC]]’s validation scope, STIP allocations 
are validated differently from generic allocations. For STIP allocations using bid list lot terminator, [[FICC]] does not validate the SIFMA compliance. 

---

## Page 8

EPN Overview 
 
Version C ontrol Page  8 
Regular GDM or Odd lot STIP allocations will still be validated on SIFMA variance compliance, in the same way as generic allocations are. Members 
may use bid list pool allocations to bypass SIFMA variance checks. 
2.1.1. Bid List Allocation 
8888, 8889 and 6888,6889,7888,7889 are the bad lot terminator used in EPN ON or CC messages. It is also referred to as list type 8 lot terminator, 
or, a Bid list lot that is only allowed for STIP allocations. The system applies the rules below on a bid list lot: 
1. All pools targeting the same STIP Trade that are processed as bid list pool across multiple EPN messaged across multiple days, are treated as 
a single lot of pools and are NOT validated for SIFMA compliance in terms of lot variance, lot pool count, and pool minimum PAR. 
2. 8889 terminator indicates the last pool of the bid list lot, upon processing such pool, the system fully decrements the residual open position for 
allocation from the STIP Trade, regardless of variance incurred. 
3. When bid list pool with 8888 terminator results the STIP trade’s residual open position for allocation <= maximum SIFMA variance of the trade, 
and there is no 8889 pool in the same EPN message, [[FICC]] DKs all the bid list pools in the EPN message. This validation is to prevent the STIP 
Trade from being marked as fully settled unintentionally. Refer to the example below. 
4. Once a bid list pool is processed, no more regular allocation lots (with GDM or odd lot terminator) are allowed, [[FICC]] DKs any regular lot 
received after the processing of a bid list lot on the STIP trade. 
5. CC on bid list pool(s), is treated as a CC against a single lot of pools. The system does not validate replacement pools for SIFMA compliance as 
described in rule 1) above. 
6. If a bid list lot terminator is used in an ON message, all regular lots (GDM and/or Odd Lot) must appear before the bid list pool lot. Else, [[FICC]] 
DKs the entire ON message. 
7. Allocations from a bid list can only be CCed as bid list lot. i.e., once the allocation is processed as part of a bid list, it must stay in the bid list lot 
until it reaches its end of life, using list type 8 in the lot terminator. 
8. 6889 and 7889 are the terminators used for the last pool in the CC message’s original lot and replacement lot. 6889 and 7889 [[DO]] not have to 
relate to the 8889 (final bid list pool allocation that closes the STIP trade position). 
 

---

## Page 9

EPN Overview 
 
Version C ontrol Page  9 
Example: Trade of 100MM with 101MM allocation via 2 EPN messages, assume CSD Factor equals 1. 
EPN [[ID]] Lot Pool Original Face Terminator Note 
1 1 123456 49,500M 8888 This would decrement the trade to 50,500M 
Open Par for allocation, but will be DKed  due to 
pool in lot 2.  
1 2 123456 50,500M 8888 The bidlist  pools in this message will be DKed 
since residual open TBA reaches within SIFMA 
variance and the terminator suggests leaving an 
open position on a trade  already decremented to 
0 
2 3 123456 1MM 8889 System will process this last pool in bid list lot 
and for the STIP trade. 
 
Note: 
In this example, EPN message [[ID]] 1 has 2 pools, Pool 123456 from Lot 1 would decrement the trade down to 50,500M, pool 2 would  decrement the trade open par 
for allocation down to 0, but there is no 8889 pool in the same message, [[FICC]] DKs the bidlist pools in this message.  
Upon EPN Message [[ID]] 2, system would decrement open TBA PAR of 100mm trade, implying 99mm of variance. [[Buyer]] [[Member]] would most  likely need to DK the 
terminating pool due to unintended large variance.  
2.2. CC 
EPN CC messages are available for members to change their allocations or [[obligations]] versus the appropriate [[FICC]] accounts via matching pool 
term. CC against generic POIDs (Pool [[obligations]] originated from Pools that targets SBON and TFT/TBA positions, not STIP positions) stay 
unchanged from current systems. 
When CC targeting allocations are successfully validated, [[FICC]] will turn the CC to the associated [[Buyer]](s). The original pool allocations will be 
cancelled, and the replacement pool allocations are created. Corresponding original [[FICC]] Pool Instructs are cancelled; if compared, [[Member]]’s Pool 
Instructs will become un-compared due to this cancellation; New [[FICC]] Pool Instructs for the replacement pools are created versus members. As in 
the Pool Netting systems current messaging flow, members will receive real time SWIFT messages regarding [[FICC]] Pool Instructs’ cancellation and 
creation. 
CC processing has no impact on members open TBA position for allocation. 

---

## Page 10

EPN Overview 
 
Version C ontrol Page  10 
Below are EPN header and pool detail fields which define the Pool Terms to identify the [[Seller]]’s original pools to CC. 
1. Submitter 
2. Contra 
3. TBA [[CUSIP]] 
4. [[settlement]] Date 
5. Price–match up to (including) the 6th decimal point. 
6. Trade Date 
7. Trade [[ID]] (TRID) for STIP allocations or [[obligations]] 
8. Pool number 
9. Pool original face 
10. EPNX–when included in CC against generic TBA, will need to match the EPNX of the original pool submitted originally. Refer to section 3.2 
EPNX in EPN Pool Detail Special Instructions–EPN Pool Reference for detailed description. 
2.3. DK 
DK messages are sent by [[FICC]] to the submitter if EPN messages received fail validations. Members can send DK messages (DK of ON or DK of 
CC) to the appropriate [[FICC]] accounts should they detect any conditions that render the allocations unacceptable1. For allocations targeting 
TFT/STIP positions, [[FICC]] will not perform all SIFMA compliance checks, buy side members are expected to DK allocations (ON or CC) when 
necessary to ensure allocations received are conforming with the stipulations of the targeted Trade [[ID]]. 
• Allocations are available for DK actions until they become Pool [[obligations]]. 
• Generic pool [[obligations]] are not allowed to be DKed and are rejected by EPN. 
• CC of Generic POID (Pool [[obligations]]) from [[FICC]] is not available for DK action, and will be rejected by EPN as system does currently. 
• CC on STIP pool [[obligations]] will be supported. 
 
When [[Member]]’s DK message targeting an ON message are successfully validated, [[FICC]] will cancel the underlying allocations and open members 
TBA position accordingly. [[FICC]] Pool Instructs associated with the allocations are also cancelled. If [[FICC]] Pool Instructs are in a compared state, the 
matching [[Member]]’s Pool Instructs will become un-compared due to this cancellation. As with the Pool Netting systems current messaging flow, 
members will receive real time SWIFT messages regarding [[FICC]] Pool Instructs’ cancellation. 
 
1 [[FICC]] may process allocatio ns aroun d EPN cu t off times (12:15pm for CC, 3pm for ON) in auto flip mode, in which certain validations are deferred to enable system processing incoming allocations in adequate 
speed. 

---

## Page 11

EPN Overview 
 
Version C ontrol Page  11 
When [[Member]]’s DK message targeting a CC message are successfully validated, [[FICC]] will cancel the underlying replacement allocations or 
replacement STIP pool [[obligations]], and recreate the original allocations or original STIP pool [[obligations]]. [[FICC]] Pool Instructs associated with the 
replacement allocations being DKed are cancelled. New [[FICC]] Pool Instructs for the original pools are created versus members. As with the Pool 
Netting systems current messaging flow, members will receive real time SWIFT messages regarding [[FICC]] Pool Instructs’ cancellation and creation. 
Note: 
DK of CC has no impact on members’ open TBA position for allocation.  
Below EPN header and pool detail fields defines Pool Term to identify the submitter’s pools to DK. 
1. Target Message [[ID]] 
2. Submitter 
3. Contra 
4. TBA [[CUSIP]] 
5. [[settlement]] Date 
6. Price–match up to (including) the 6th decimal point. 
7. Trade Date 
8. Trade [[ID]] (TRID) for STIP allocations or [[obligations]] 
9. Pool number 
10. Pool original face 

---

## Page 12

EPN Overview 
 
Version C ontrol Page  12 
3. ADDITIONAL FIELDS IN EPN HEADER AND POOL DETAIL 
3.1. Trade [[ID]] in EPN Message Header Special Instructions Field 
When allocating STIP positions, members must target a STIP Trade by including the Trade [[ID]] in their ON, CC and DK messages. For ON and CC 
messages submitted against FSTI without a valid TRID value, [[FICC]] DKs the EPN message. For DK message submitted against FSTI without a valid 
TRID value, EPN rejects the DK message. 
When allocating Generic TBA positions, members may choose to include a Trade [[ID]] in their ON message, to target the allocation against the trade. 
ON Messages received by FTBA with an incorrect Trade [[ID]] will be DKed. 
Incorrect Trade [[ID]] refers to when Trade [[ID]] does not exist in the system or disagrees with the trade term included in ON message. [[FICC]] System 
does not attempt to match it on terms. 
• “TRID=value=” is added in EPN header, special instructions field to enable members to target a TBA Generic or STIP Trade for their allocations. 
Its value can be up to 16 characters long, ended with another “=” sign. System will search for “TRID=” string in the special instruction field and 
extract 16 characters that follows the position of “TRID=”, or until the ending “=” is encountered before the 16th character. Any leading and 
trailing space extracted are trimmed for matching Trade [[ID]] in the system. 
For example: 
o “TRID=0040454925=”, system reads in TRID value as “0040454925” 
o “TRID= 0040454925 =”, system reads in TRID value as “0040454925” 
o “TRID=00404549250123456789=”, system reads in TRID value as “0040454925012345” 
o “TRID=00404549250123456789”, system reads in TRID value as “0040454925012345” 
o “TRID=0040454925”, system reads in TRID value as “0040454925” 
o “TRID=0040454925=other memo text”, system reads in TRID value as “0040454925” 
o “TRID=0040454925 other memo text”, system reads in TRID value as “0040454925 other” 
• TRID’s value should be alphanumeric. 
• TRID is mandatory when EPN message has [[FICC]] STIP Account (FSTP) as the contra party. 
• TRID is optional when submitting EPN ON against [[FICC]] Generic TBA Account (FTBA). 
• TRID is used for all EPN submission against STIP positions or ON messages against generic TBA positions. 
• [[FICC]] system will attempt to process ON messages using matching TBA terms if the ON is submitted against FTBA without any Trade [[ID]]. 
• [[FICC]] system always populates the TRID in ON sent to members. 

---

## Page 13

EPN Overview 
 
Version C ontrol Page  13 
3.2. EPNX in EPN Pool Detail Special Instructions–EPN Pool Reference 
In order to provide a linkage of EPN activities to Pool Instruct records, “EPNX=value=” is introduced to Pool Detail Special Instruction field. EPNX 
enables members to link EPN allocations with Pool Instructs Comparison Advisory in Pool Netting system. EPNX can also be included in CC 
messages subsequently to target the original generic (non STIP) pools. 
When used as a linkage, [[Member]] can include EPNX in the ON and the replacement pool records of CC message. When used to target generic 
original pools in CC, EPNX can be included in the original pool records. 
EPNX is designed for allocation activities before they resulted into Pool [[obligations]] (POIDs). EPNX is ignored if included in a CC message targeting 
POIDs. 
• When included in ON or the replacement pools of CC, the validated allocation will carry the value through to Pool Netting. [[Member]] will receive 
Pool Instruct Advisory from [[FICC]] with EPNX value included in the MT518 Pool Advisory message in 70E::TPRO/EPNX. In addition, when 
[[Member]]’s Pool Instruct are created by [[FICC]] during force comparison, [[Member]] will receive MT518 “Screen Input Replay–Force Compare” 
message with 70E::TPRO/EPNX field echoing [[Member]]’s input in their EPN submission. 
• When EPNX is included, all pools in a lot must have EPNX populated. Else, [[FICC]] DKs the ON or CC message. 
• [[FICC]] does not validate EPNX uniqueness across the submitter's pools. 
• Generic CC Messages received with an incorrect EPNX in the original pools will be DKed; EPNX is incorrect when it does not exist in the 
system or disagree with the rest of the pool term. 
• When generic CC Messages are received with an ambiguous EPNX in the original pool, i.e., EPNX submitted exists in the system but is 
associated with multiple pools, [[FICC]] system attempts to use on any of the associated original pool with matching pool term to process the CC. 
• System attempts to match original pool(s) on pool term for the generic CC received without any EPNX. 
• System ignores the EPNX on the original pool of STIP CC messages, system attempts to match original pool by pool term included in the CC 
message. 
• Generic ON, CC, and STIP ON messages sent by [[FICC]] to members always populate the EPNX on all pool detail lines, to uniquely identify 
[[FICC]]’s pool allocation. Members may choose to link the ON/CC messages received with the Pool Netting SWIFT MT518 messages received. 
• STIP CC messages sent by [[FICC]] are always populated with EPNX in replacement pool details, but not in the original pools. 
• Format is EPNX=value=. The value should be alphanumeric. Its value can be up to 16 characters long, ended with another “=” sign. System will 
search for “EPNX=” string in the special instruction field and extract 16 characters that follows the position of “EPNX=”, or until the ending “=” is 
encountered before the 16
th character. Any leading and trailing space extracted are trimmed for matching Trade [[ID]] in the system 
• EPNX field format and parsing rule are the same as TRID field. For example: “EPNX=1234567890123=”, system reads in EPNX value as 
“1234567890123”. 

---

## Page 14

EPN Overview 
 
Version C ontrol Page  14 
3.3. TRID and EPNX Usage by EPN Message Types 
EPN New 
Fields 
Members Submit To FTBA (Generic)  FTBA Submits To Members 
 ON CC 
ORG 
Section 
CC 
RPL Section 
DK of ON DK of CC ON CC 
ORG 
Section 
CC 
RPL Section 
DK of 
ON 
DK of 
CC 
TRID O IG IG IG IG AP NP NP NP NP 
EPNX O O* O IG IG AP AP* AP NP NP 
 
EPN New 
Fields 
Members Submit To FSTI (STIP)  FSTI Submits To Members  
 ON CC 
ORG 
Section 
CC 
RPL Section 
DK of ON DK of CC ON CC 
ORG 
Section 
CC 
RPL Section 
DK of 
ON 
DK of 
CC 
TRID M M M M M AP AP AP AP AP 
EPNX O IG O IG IG AP NP AP NP NP 
 
Where 
• O: stands for Optional, TRID is used for allocation assignment to TBA, EPNX will be echoed in Pool Netting system and visible for PID 
Comparison Advisory and MROs 
• M: stands for Mandatory 
• AP: stands for Always Populated, even though it is optional field 
• NP: stands for Not Populated, for optional field 
• IG: stands for Ignored or unsupported 
• O*: stands for Optional, included to target Original pools matching on EPNX 
• AP*: stands for Always populated to target Original Pools by EPNX 
• ORG Section: Original Pool Section in CC message 
• RPL Section: Replacement Pool Section in CC message 

---

## Page 15

EPN Overview 
 
Version C ontrol Page  15 
4. [[FICC]] INPUT VALIDATION BY EPN MESSAGE TYPES AND PROCESSING 
MODE 
ON: [[FICC]] validates [[Member]]’s ON Message submitted against [[FICC]] accounts to ensure input fields are valid, pool allocations are compliant with 
SIFMA Good Delivery Guideline2, EPN Guideline, and that there is sufficient open TBA position with matching term to assign the allocations 
to. 
DK: [[FICC]] validates members DK message submitted against [[FICC]] accounts to ensure input fields are valid, targeted EPN message and 
allocation lot(s) being DKed exist with matching pool term, and allocations have not reached end of life3. DK must be performed on the entire 
Lot content; else it will be rejected by EPN. Bid list pools4 can be DKed individually, i.e., DKing one or a subset of bid list pools from the 
single bid list lot is allowed. 
CC: [[FICC]] validates members CC Message submitted against [[FICC]] accounts to ensure input fields are valid, original allocations or pool 
[[obligations]] with matching term exist, and generic replacement pools are compliant with SIFMA Good Delivery Guideline. CC targeting 
generic pool [[obligations]] (originated from SBON and TFT/TBA pool allocations) remains unchanged from the current system. 
[[FICC]] may process EPN inputs in Auto flip mode during the short time range before EPN cut off times (12:15pm for ON, 3pm for CC). In auto flip 
mode, certain input validations are deferred to post cut off time, and a subset of optional fields will be left blank. 
When validation fails, there are two possible outcomes: 
A) EPN rejects the message upfront 
or 
B) [[FICC]] DKs the submitter on all or a sub set of the allocation lots. 
  
 
2 [[FICC]] validates SIFMA compliance in terms of 1) Lot variance 2) number of pools for each lot 3)minimum Pool Original Face is > SIFMA Minimum PAR 
3 If DK targets an allocation CC message, only replacement pools are required to be active for DK action. If replacement pools have reached end of life, i.e, cancelled or resulted into pool [[obligations]], such CC 
message will be rejected with the new reject reason code 0248 (Matching lot not found). If DK targets a STIP Pool Obligation CC message, replacement pool [[obligations]] must be active, i.e, not in cancelled or 
settled state.  
4 Allocations submitted using bad lot terminator, and targets STIP Positions. Bid list pools are not required to be SIFMA compliant, [[FICC]] suppress SIFMA Good Delivery validation on bid list pools. 

---

## Page 16

EPN Overview 
 
Version C ontrol Page  16 
4.1. Reminders on EPN Header Fields Validation: 
• Submitter: Must NOT be an EPN-only [[Member]] if contra is an [[FICC]] account, else EPN rejects. 
 
• Contra: EPN will reject if contra is [[FICC]] SPT Account (“FSPT”). 
 
• Message Type: If message type is CX, and contra is an [[FICC]] account, EPN rejects. 
 
• Original Trade Par: System only validates if an odd lot is included in the ON message, tail PAR portion of this field will be part of the matching 
term for the targeted TBA position for allocation. If tail portion of this field is not found in [[Member]]’s matching open TBA position, [[FICC]] DKs the 
odd Lot. 
 
• Price: Part of the matching term for the targeted TBA position for allocation. Must match to the 6th decimal point when Trade [[ID]] is included in 
the ON input. Must match to the 9th decimal point when Trade [[ID]] is not included in the ON submission. For DK and CC messages, price must 
match to the 6th decimal point of the targeted pool. 
 
• Special Instructions: STIP Position must include Trade [[ID]]. Generic TBA positions may include Trade [[ID]]. Syntax: “TRID=VALUE=”, else 
system DKs the message. 
4.2. Reminders on EPN Pool Detail Fields Validation: 
• Lot terminator: Bad lot terminator 8888, 8889 is only allowed for STIP allocations. System DKs generic allocation lot with 8888 or 8889 lot 
terminator. Bid list pool lot can only be submitted after all the regular allocation lots, else [[FICC]] DKs the entire message. If a bid list pool with 
8888 terminator leave the STIP’s residual open TBA position for allocation <= maximum SIFMA variance, and there is no 8889 pool in the same 
message, system DKs all the bid list pools in the message. 

---

## Page 17

EPN Overview 
 
Version C ontrol Page  17 
5. [[FICC]] OUTPUT TO MEMBERS VIA EPN 
5.1. Reminders on EPN Header Fields: 
• Original Trade Par: For [[FICC]] outbound ON message to members, system populates it with Original Trade PAR of the targeted TBA Trade, and 
drop the digits higher from the billionth place values if original Trade PAR $1 billion or higher. For CC message, system populates it with Sum of 
Original Face of the pools being cancelled in the CC message (same as current system logic CC on POID). 
 
• Special Instructions: [[FICC]] system populates “TRID=VALUE=” in all outbound ON messages to members; it is also populated to all EPN 
messages targeting STIP positions. 
5.2. Reminders on EPN Pool Detail Fields: 
• Special Instructions: [[FICC]] system populates “EPNX=value=” to uniquely identify the pool allocation in all outbound ON and generic CC 
messages.5 
 
5 EPNX value is echoed in Pool Netting Comparison Advisory and Pool Instruct created on [[Member]]’s behalf during Pool Netting force comparison step. 

---

## Page 18

EPN Overview 
 
Version C ontrol Page  18 
6. EPN DK REASON CODE 
 
Code Description 
0100 Incorrect Submitter [[ID]]  
0101 Incorrect Contra [[ID]]  
0102 Trade Unknown  
0103 Incorrect Variance 
0104 Pool Outside Trade Requirements  
0105 Coupon Outside Trade Requirements  
0106 Pool Unknown 
0107 Incorrect Price  
0108 Incorrect Pool Number  
0109 Incorrect Amortized Value 
0110 Incorrect Amortized Value for Pool Number  
0111 Trade Already Settled  
0112 Incorrect TBA [[CUSIP]] 
0113 Pool Already Settled  
0114 Incorrect Trade Date 
0115 Incorrect [[settlement]] Date  
0116 Incorrect Delivery Date 
0117 Incorrect Par Value 
0118 Incorrect Special Instructions  
0119 Duplicate Message 

---

## Page 19

EPN Overview 
 
Version C ontrol Page  19 
Code Description 
0120 Incorrect Number of Good Delivery Millions  
0121 Pool Substitution  
0122 Binary Characters Received  
0123 Original Face > Original Issue Amount  
0124 Incorrect or missing Sub -Account  
0125 Incorrect Lot Terminator  
0126 Incorrect Use of Pos Dup Indicator  
0127 Trade Already Paired -Off/Round Robin 
0128 Inappropriate use of Sub- Account ZZZZ  
0129 Canceled Pools are Invalid  
0130 Substituted Pools are Invalid  
0131 Canceled and Substituted Pools are invalid  
0132 Incorrect message type 
0133 Matching lot not found 
0134 Incorrect number of pools in Lot  
0135 Invalid residual Open Position  
0136 Pool Matures on/before Delivery Date 
0137 Incorrect New Issue Indicator  
0138 Valid Pool Factor unavailable 
0139 Blockpool not divisible to good delivery  
0140 Multiple tail lot  
0141 Invalid Regular Lot after Bid list Lot.  

---

## Page 20

EPN Overview 
 
Version C ontrol Page  20 
7. EPN REJECT REASON CODE 
 
Code Description 
0248 Matching lot not found 
0200 Message Accepted  
0201 Invalid Logon  
0202 Invalid EPN Version Control  
0203 Invalid Subscriber  
0204 Invalid User [[ID]]  
0205 Invalid Submitter  
0206 Invalid Contra  
0207 Invalid TBA [[CUSIP]]  
0208 Invalid Message Type  
0209 Invalid Original Trade Par  
0210 Invalid Price  
0211 Invalid Good Delivery Millions  
0212 Invalid Reason Code  
0213 Message Not Received  
0214 Logon Not Established  
0215 Invalid Connection Type  
0216 End of Message Indicator Not Found  

---

## Page 21

EPN Overview 
 
Version C ontrol Page  21 
Code Description 
0217 Invalid Status Request Message  
0218 Already Established Logon  
0219 More than 250 Pool Details  
0220 Terminator Blank  
0221 Invalid Status Request Message  
0222 Invalid Retransmission Request message  
0223 Invalid Retransmission Request message  
0224 Invalid Last Sequence Message  
0225 Invalid Heartbeat Message  
0226 Retrans Request System Limit Exceeded  
0227 Retrans Request Firm Limit Exceeded  
0228 ON Messages Disabled  
0229 DK Messages Disabled  
0230 CX Messages Disabled  
0232 Sequential Duplicate Sequence Number Rejected  
0233 Invalid Report Request Message  
0234 Too Many Rpt Reqs  on EPN - Try Later  
0235 Too Many Rpt Reqs for Firm - Try Later  
0236 Sending Connection Broken while receiving a message  
0237 Timeout while receiving a message  
0238 Unacceptable Message Formatting  

---

## Page 22

EPN Overview 
 
Version C ontrol Page  22 
Code Description 
0239 Invalid submitter and Timeout while receiving a message  
0240 No canceled pools submitted  
0241 No replacement pools submitted  
0242 Incorrect number of pools  
0243 Pool Substitution message disabled  
0244 Canceled pools missing  
0245 Substituted pool missing  
0246 Invalid terminators  
0247 Invalid [[settlement]] date  
0248 Matching lot not found 

---

## Page 23

EPN Overview 
 
Version C ontrol Page  23 
8. GENERAL EPN GUIDELINES 
8.1. General EPN Guidelines: 
a. Price in all the DK, CC, and the ON message that includes the targeted Trade [[ID]], needs to match to the 6th decimal point. 
Price in the ON messages without including the Trade [[ID]] will need to match to 9th decimal point. 
b. [[FICC]] validates GDM Count header field only for ON message. [[FICC]] will not validate this field for DK, CC messages. 
c. Trade Date–Trade Date is part of matching term to target the TBA position and will be ground for DK if does not match to open TBA 
position. 
d. Odd Lot Terminator interpretation in ON or DK message–All contiguous pools in the lot that starts with 9999 and ends on 9999 lot 
terminators are considered as one odd lot, regardless of the Lot [[ID]] value in the EPN message [[ID]]. 
 
Example: 
EPN Lot [[ID]] PAR LOT TERMINATOR  
1A 500K 9999 
1B 250K 9999 
- OR - 
1A 500K 0 
1B 250K 9999 
- OR - 
1 500K 9999 
2 250K 9999 
 
For all above examples, system would process the 2 pools as a single odd lot. 

---

## Page 24

EPN Overview 
 
Version C ontrol Page  24 
8.2. [[FICC]] Processing Rules: 
a. EPN Input Cutoff is 4:30pm. 
 
b. Allocations must target corresponding [[FICC]] Account [[ID]] based on the targeted TBA Position. Refer to section 1 [[FICC]] Accounts for 
[[Novation]] for details. 
 
c. CX to [[FICC]] is not allowed and will be rejected by EPN. 
 
d. STIP allocations via bid list pools are validated against bid list lot terminator validation rules. Refer to section 2.1.1Bid List Allocation for 
details.  
 
e. STIP allocations (ON, CC, DK) must include a valid Trade [[ID]] (TRID). Refer to section 3.1 Trade [[ID]] in EPN Message Header Special 
Instructions Field for detail. 
 
f. Optional field -- EPNX (EPN Pool Reference) field is added in pool detail special instructions to link EPN pool submissions to Pool Instruct 
records, or to target original pool(s) in CC messages on generic(non STIP) allocations. 
 
g. Generic allocations are available for DK action until they result into POIDs (Pool Obligation). 
 
h. Generic POIDs are not available for DK. 
 
i. CC of STIP POIDs are available for DK. 

---

## Page 25

EPN Overview 
 
Appendix A: Example DK Sc enarios  25 
APPENDIX A: EXAMPLE DK SCENARIOS 
ON/CC DK Scenario Reason Code Reason Code Description  
No matching TBA position found  0102 Trade Unknown  
Original Trade Par not matching any of open TBA trade under the term specified 0102 Trade Unknown  
Price not matching any of open TBA trade under the term specified 0102 Trade Unknown  
TBA [[CUSIP]] not matching any of open TBA trade under the term  specified  0102 Trade Unknown  
CSD not matching any of open TBA trade under the term specified 0102 Trade Unknown  
TRADE_ID not matching trade term specified or not found 0102 Trade Unknown  
GDMs not matching the GDM counts in the message body  0120 Incorrect Number of Good Deli very Millions 
Non SIFMA Variance in Lot based on the Lot terminator  0103 Incorrect Variance 
Incompliant number of pools in Lot based on the Lot terminator  0134 Incorrect number of pools in Lot  
Pool Number not qualifying for TBA or not MBSD eligible  0108 Incorrect Pool Number  
Original Face not meeting minimum or maximum or  multiples PAR requirement  0117 Incorrect Par Value 
Bad lot terminator for Non- STIP allocations or regular lot  terminator submitted after 
bid list pool allocation.  
0125 Incorrect Lot Terminator  
Remaining open TBA position for Allocation less than SIFMA or  Fedwire minimum  0135 Invalid residual Open Position  
DD >= Pool's maturity date based on [[FICC]]'s pool master  0136 Pool Matures on/before Delivery Date 
New Issue Flag incorrect, ie, X value for non -new issue pools or non X value on new 
issue pools  
0137 Incorrect New Issue Indicator  
If missing factor on non -new issue, non -blackout pool or if CSD factor is 0 0138 Valid Pool Factor unavailable 
Missing Pool  [[CUSIP]] information from [[FICC]] Pool Master  0106 Pool Unknown 
Cannot divide block allocation into multiple good delivery units  0139 Block allocation cannot be broken down to Good 
Delivery units  

---

## Page 26

EPN Overview 
 
Appendix A: Example DK Sc enarios  26 
ON/CC DK Scenario Reason Code Reason Code Description  
Additional for CC of Allocation  
Allocation lot [[ID]] from Ops submission for CC exception  processing does not exist or 
not match the term 
0118 Incorrect Special Instructions  
If original pool lot with matching term not found 0129 Canceled Pools are Invalid  
 

---

## Page 27

EPN Overview 
 
Appendix B: Example Scenarios for EPN Rejects  27 
APPENDIX B: EXAMPLE SCENARIOS FOR EPN REJECTS 
Reject Scenario Reject Code Reject Code Description  
Inbound ON/DK/CC Message  
EPN Only [[Member]] submits to [[FICC]] Account [[ID]]  0206 Invalid Contra [[ID]]  
Message type is CX and submitter or contra is 
[[FICC]] account  
0208 invalid message type 
Inbound DK Message 
Price not matching any of pending allocation 
under the term specified  
0248 Matching lot not found 
EPN Target Message [[ID]] not found or not 
originally sent to the submitter [[ID]], or target EPN 
message [[ID]] type not matching system record.  
0248 Matching lot not found 
TBA [[CUSIP]] not matching pending allocation 
under the term specified  
0248 Matching lot not found 
CSD not matching any of pending allocation 
under the term specified  
0248 Matching lot not found 
Pool Number not matching any of pending 
allocation under the term s pecified  
0248 Matching lot not found 
Original Face not matching any of pending 
allocation under the term specified  
0248 Matching lot not found 
Incomplete number of pools in Lot  0248 Matching lot not found 
 
 

---

## Page 28

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 