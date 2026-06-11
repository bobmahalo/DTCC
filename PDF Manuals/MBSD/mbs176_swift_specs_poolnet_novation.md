---
title: "MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs176_swift_specs_poolnet_novation.pdf"
pages: 58
size: "920.8 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications

**Original File:** [mbs176_swift_specs_poolnet_novation.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs176_swift_specs_poolnet_novation.pdf)  
**Category:** MBSD  
**Total Pages:** 58  
**File Size:** 920.8 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
MBS CCP POOL NETTING: SWIFT INTERACTIVE MESSAGING 
SPECIFICATIONS  
VERSION 2.0.2 
JUNE 5, 2023 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”). [[DTCC]] itself does not provide such services. Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
The Interactive Messaging Specifications for MBS Central Counterparty (CCP) Pool Netting (hereinaf ter, the "Document") is 
provided as a convenience to participants and for information only. Although [[FICC]] may make this Document available to 
participants, [[FICC]] shall be under no obligation to [[DO]] so, or having done so once or more, have a continuing obliga tion to 
make available the Document, or other related information of a certain type.  
 
[[FICC]] DOES NOT REPRESENT THE ACCURACY, ADEQUACY, TIMELINESS, COMPLETENESS, OR FITNESS FOR 
ANY PARTICULAR PURPOSE OF ANY INFORMATION PROVIDED TO MEMBERS IN THIS DOCUMENT, W HICH IS 
PROVIDED AS-IS. [[FICC]] SHALL NOT BE LIABLE FOR ANY LOSS RELATED TO SUCH INFORMATION (OR THE ACT 
OR PROCESS OF PROVIDING SUCH INFORMATION) RESULTING DIRECTLY OR INDIRECTLY FROM MISTAKES, 
ERRORS, OR OMISSIONS, OTHER THAN THOSE CAUSED DIRECTLY BY GROSS NEGLIGENCE OR WILLFUL 
MISCONDUCT ON THE PART OF [[FICC]]. [[FICC]] SHALL NOT BE LIABLE FOR: (1) ANY LOSS RESULTING DIRECTLY 
OR INDIRECTLY FROM INTERRUPTIONS, DELAYS, OR DEFECTS ARISING FROM OR RELATED TO PROVIDING 
THIS GUIDE; AND (2) ANY SPECIAL, CONSEQUENTIAL, EX EMPLARY, INCIDENTAL, OR PUNITIVE DAMAGES.  
 
Further, the information contained in this Document is subject to change. Participants and other authorized users of the 
Document will find the most current version of the Document on [[DTCC]]’s internet site, www.[[DTC]] c.com. [[FICC]] shall bear no 
responsibility for any losses associated with the failure of participants or other authorized users to follow [[FICC]]’s most 
current Document.  
 
Doc Date: June 5, 2023 
Publication Code:  MBS176 
Service: Fixed Income Clearing Corporatio n 
Title: MBS CCP Pool Netting: SW IFT Interactive Messaging Specifications  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Version Control Page ....................................................................................................................... 5  
About this Document ....................................................................................................................... 6  
Aud ienc e ....................................................................................................................................... 6  
Related Materials............................................................................................................................ 6  
1. Introduction ................................................................................................................................. 7  
1.1 Mes s ag es Overview................................................................................................................... 7  
2. MT515 POOL NETTING INPUT MESSAGES..................................................................................... 9  
2.1 MT515 Pool Netting Input Messages–General Format .................................................................... 9  
2.2 MT515 Pool Netting Input Messages–Field Specifications ............................................................. 11 
2.3 Mt515 Poo l Netting  Inp ut Mess ag es–Field Analysis ...................................................................... 16 
3. MT509 Pool Netting Output Messages ..........................................................................................19  
3.1 MT509 Pool Netting Output Messages–General Format ................................................................ 19 
3.2 MT509 Pool Netting Output–Field  Sp ec ific atio ns .......................................................................... 21 
3.3.1-MT509 Pool Netting Output Field Analysis–Part 1 of 3 (25D = IPRC) ........................................... 26 
3.3.2-MT509 Pool Netting Output Field Analysis–Part 2 of 3 (25D = IPRC) ........................................... 29 
3.3.3-MT509 Pool Netting Output Field Analysis–Part 3 of 3 (25D = CPRC or MTCH) ............................ 33 
4. MT518 Pool Netting Output Messages ..........................................................................................37  
4.1 MT518 Pool Netting Output Messages–General Format ................................................................ 37 
4.2 MT518 Pool Netting Output Messages–Field Specifications ........................................................... 40 
4.3 MT518 Pool Netting Output Messages–Field Analysis................................................................... 46 
5. MT599 Pool Netting System Event Messages ................................................................................50  
5.1 MT599 Pool Netting Output Messages–General Format ................................................................ 50 
5.2 MT599 Pool Netting Output Messages–Field Specifications ........................................................... 51 
Appendices ....................................................................................................................................53  
Appendix A: Reason Codes ........................................................................................................... 53 
Reject Reason Codes .................................................................................................................. 53 
Mess ag e Reaso n Cod es .............................................................................................................. 54 
DK Reason Codes....................................................................................................................... 54 

---

## Page 4

 
 
Appendix B: SWIFT Outp ut Mess ag e Gro up ings ............................................................................... 55 
 

---

## Page 5

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
Version C ontrol Page 5 
VERSION CONTROL PAGE 
Date Version # Name Description of Change  
07/05/2015 2.0 C. Swords  Made following document corrections:  
• Removed change-marks related to modifications introduced 
with prior version. 
• Updated format to conform to new standards, and updated 
general comments as deemed necessary. 
07/15/2015 2.0 C. Swords  Made following enhancements to support [[Novation]]:  
• Add MT599 message for start/end expanded pool net process 
• On MT515 (and MT518), Trade Date must specify date of 
targeted TBA position. 
• On MT509, new messages for non-netting eligible and STIP 
PIDs converted to pool [[obligations]] (NECV and PDCV 
respectively) 
• On MT518, add pool reference from EPN submission (EPNX) 
• MT518 SITR (force-compare) generated by system 
• Added table for Reason Codes (previously in separate 
document) 
08/26/2015 2.0.1 C. Swords  Made following updates:  
• On MT518, update verbiage describing EPNX as “reflects the 
Pool Reference specified by the [[Seller]] in their corresponding 
EPN submission”. Note that the [[Seller]] can be a [[Member]]-
[[Seller]], or [[FICC]]. 
n/a n/a [[DTCC]] 
Learning  
Updated formatting only. Content  is unchanged. 
6/5/2023 2.0.2 J.Sheeran  Removed references of “pending pool add”  

---

## Page 6

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 6 
ABOUT THIS DOCUMENT 
This document provides an overview of Interactive Messaging to support MBS Central Counterparty (CCP) 
Pool Netting and the MBS [[Novation]] initiative, along with detailed message specifications (input and output) that 
will be used to support the process. In developing these specifications, an effort was made to ensure that they 
are consistent with existing Interactive Messaging specifications for MBS RTTM and Pool Netting. 
As new functionality is added to the existing service, additions and modifications to these specifications may be 
required. This is therefore a "living" document that will be updated as interactive services are expanded. 
Audience 
This document was written for systems and development personnel, including managers, analysts, and 
programmers. It presumes readers are familiar with technical concepts and terms, understand [[FICC]]'s 
Interactive Messaging specifications for both MBS RTTM and MBS CCP Pool Netting, and have a [[BASIC]] 
knowledge of the MBSD's services. 
Related Materials 
SWIFT 
The specifications for Interactive Messages are based on SWIFT messages. Readers are therefore strongly 
urged to refer to SWIFT user documentation to obtain a complete and comprehensive understanding of 
these message standards. SWIFT information (including many applicable message formats) can also be 
found on the Internet at www.iso15022.org
. 
RTTM 
For additional information regarding RTTM®, readers can refer to documentation found on the internet at 
https://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbsd-rttm. 

---

## Page 7

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 7 
1. INTRODUCTION  
Upon the implementation of the MBS CCP Pool Netting System: 
• Participants will have the ability to submit pool input to Pool Netting intra-day, using the SWIFT MT515 
message format. 
• Submitters will immediately receive pool status information (i.e., notification of whether the pool input has 
been accepted or rejected) via the SWIFT MT509 message format. This format will also be used to 
provide up-to-the-minute pool status information to Participants as transactions are processed by Pool 
Netting (for example, a message will be sent when a Pool Instruct compares, is canceled or is modified). 
• Pool Instruct counterparties will also be notified immediately via a SWIFT MT518 message when an 
Instruct has been submitted against them. The SWIFT MT518 message will contain full Pool Instruct 
details. It will also be used to communicate to participants those changes that Pool Netting may have 
made to transaction records previously submitted, Instructs previously created Pool Instructs automatically 
generated on [[Member]]’s behalf, or when participants enter information directly into the system via terminal 
service. 
• Administrative messages using the MT599 format will be generated indicating: 
Daily Messages 
1. Pool Netting Start of Day Notification, 
2. Start of Pool Netting, 
3. End of Pool Netting, 
4. Comparison Submission Cutoff End-of-Day Message, and 
5. End-of-Day Cycle Message  
 
SIFMA-Calendar based Messages: 
6. Start of Expanded Pool Netting, and 
7. End of Expanded Pool Netting, 
1.1 Messages Overview 
1. The following table summarizes the SWIFT message types that will be used for Pool Netting. 
 
SWIFT Message 
Type 
Used for Generated By See Section 
MT515 All the SWIFT Pool Inputs to [[FICC]]  Participants  2 
MT509 and   
MT518 
Pool Netting real -time SWIFT MRO to 
participants  
[[FICC]] 3 (for MT509) and  
4 (for MT518) 
MT599 Pool Netting real -time SWIFT MRO to 
participants on System Events  
[[FICC]] 5 
 
  

---

## Page 8

MBS CCP Pool Netting: SWIFT Interactive Messaging Specif ications 
About this Docum ent 8 
2.       Detailed Messaging Specifications 
Sections 2-5 contain the detailed messaging specifications for the message types summarized in the table 
above. While this document provides the full specifications for MBS Pool Netting and [[Novation]] service, the 
information has been color coded to highlight changes introduced with the [[Novation]] service. For members 
currently communicating via the MBS Pool Netting Interactive Messaging service, these highlighted section 
represent changes that may need to be supported, based on the [[Member]]’s needs. Please refer to the following 
table for details. 
If the text is shaded in:  That indicates: 
Yellow (or dark  gray)  * 
Example: new Pool  Netting  fields 
The fields  are either: 
New sub-qualifiers  introduced for MBS [[Novation]],  or 
Existing  tags/qualifiers/sub- qualifiers modified for MBS 
[[Novation]].  
No shading  Existing  MBS messaging  specifications  that are unchanged 
for MBS [[Novation]].  
 
1.2 Additional Details 
Please refer to the following appendices for further detail: 
A Reason Codes for MBS CCP Pool Netting 
B Real-time SWIFT Output Message Groupings 
C Message Flows for MBS CCP Pool Netting 
D Message Samples for MBS CCP Pool Netting 
Note: 
The Messaging Flows and Message Samples (Appendices B and C) have been included to further bolster the reader's 
comprehension of the specifications and to assist in the coding effort. These Messaging Flows and Message Samples are 
for illustrative purposes and are not intended to be comprehensive. They [[DO]] not include all potential messaging flows, nor 
[[DO]] they contain all data that may be conveyed in the messages.  

---

## Page 9

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 9 
2. MT515 POOL NETTING INPUT MESSAGES 
This section contains the following sub-sections: 
2.1 General Format 
2.2 Field Specifications 
2.3 Field Analysis 
Note:  
See Item #2 in Section 1.1 for a description of what the shaded colors indicates.  
2.1 MT515 Pool Netting Input Messages–General Format 
M/ O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
    Message Header  
M    Password  12!c 
M    Sender  8!c 
M    Message Type 3!n/3!n/4!c  
M    Receiver  8!c 
M :16R: GENL  Block Start  
M :20C: :SEME//  Sender’s Reference for this Msg.  16x 
M :23G: NEWM  Msg. Function = New Instruct or  4!c 
  CANC  Cancel   
M :22F: :TRTR/ DTCY/CASH Cash Buy/Sell Trade Indicator  4!c 
M :16R: LINK  Repeat Block Start  
O :20C: :MAST//  Master Reference Number  
(External Reference)  
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PREV//  Previous Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :LIST//  Pool Netting Assigned Reference  (PID) 16x 
M :16S: LINK  Repeat Block End  

---

## Page 10

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 10 
M/ O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
M :16S: GENL  Block End  
M :16R: CONFDET  Block Start  
M :98C: :TRAD//  Trade Date & Time YYYYMMDDHHMMSS 
M :98A: :SETT//  [[settlement]] Date YYYYMMDD 
M :90A: :DEAL/ /PRCT/ Deal Price–Percentage 15d 
O :19A: :SETT/ /USD [[settlement]] Amount  15d 
M :22H: :BUSE/ /BUYI Trade Type– Buy or 4!c 
   /SELL Sell  
O :22F: :PROC/ DTCY/INST Instruct (i.e., Pool Instruct) Processing 
Indicator or  
4!c 
   DTCY/CANC Cancel Processing Indicator or   
   DTCY/MDFC Modify Processing Indicator or   
   DTCY/TDDK DK Processing Indicator or   
   DTCY/CDRQ CDR Request Indicator or   
   DTCY/CDRL CDR Release Indicator   
M :22H: :PAYM/ /APMT Against Payment Indicator  4!c 
M :16R: CONFPRTY  Repeat Block Start  
M :95R: :BUYR/ DTCY/PART Party = [[Buyer]] 34x 
O :20C: :PROC//  Pool Netting Assigned Contra  
Reference (Contra's PID)  
16x 
M :16S: CONFPRTY  Repeat Block End  
M :16R: CONFPRTY  Repeat Block Start  
M :95R: :SELL/ DTCY/PART Party = [[Seller]]  34x 
O :20C: :PROC//  Pool Netting Assigned Contra  
Reference (Contra's PID)  
16x 
M :16S: CONFPRTY  Repeat Block End  
M :36B: :CONF/ /FAMT/ Quantity as Face Amount–Original Face 
Value (Par) 
15d 
M :35B: /US/  TBA [[CUSIP]] 9!c (4 * 35x) 
M :16R: FIA  Block Start  
O :13B: :POOL/ DTCY/ Pool Number 9x (30x) 
M :16S: FIA  Block End  

---

## Page 11

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications 
About this Docum ent 11 
M/ O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
O :70E: :TPRO/ /DTCY Trade Instruction Processing 
Narrative 
(10*35x) 
   /TDSVPOOL Trade Service Type– Pool Input  for Pool 
Netting  
4!c 
   /CDRY CDR Indicator   
   /DDTE Delivery Date YYYYMMDD 
   /DKRS DK Reason (see Appendix A)  4!c 
M :16S: CONFDET  Block End  
2.2 MT515 Pool Netting Input Messages–Field Specifications 
 
Block/Tag Notes 
Message 
Header 
Each message must contain a message header. All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password 12!c A password will be assigned by Pool Netting enabling the sender to submit 
pool inputs on behalf of specific [[participant]](s).  
Sender 8!c MBSD account number of the [[participant]] sending the message.  
Message Type 3!n/3!n/4!c  The first three characters indicate to the recipient the message type (515); 
the second three positions reflect the version of the message interface 
(currently always 000). The last four characters indicate the [[issuer]] code to 
be used in the message (“DTCY”).  
Receiver 8!c MBSCPNET (MBSD Pool Netting System) will always be the recipient  of 
the MT515 messages.  
GENL This Mandatory Block provides general information regarding the message. It appears only 
once in a trade contract.  
20C Sender Message Reference 
• SEME//-This mandatory field contains the sender’s message reference number. It is mandatory 
and must contain a unique number to unambiguously identify each message sent to Pool Netting. 
(This is a communications message number, not a trade number.) (It is suggested that participants 
use a number that includes a date follow ed by either a time stamp or a sequence number. In this 
way uniqueness can be ensured.)  
Note: 
While the SWIFT message accommodates both upper and lower case alphanumeric and certain 
symbols, for Pool Netting purposes, this field must be populated with an u pper case alphanumeric 
value. It cannot contain symbols or hyphens.  
e.g., :20C::SEME//11012007ABCDEFG 

---

## Page 12

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 12 
Block/Tag Notes 
23G Function of the Message 
This mandatory field identifies the function of the message. It will either be a new message (NEWM) 
or a cancellation of a previous message (CANC):  
• NEWM–This qualifier will be used for a Pool Instruct, a Modify, CDR, CDR Release or a DK 
Message. 
• CANC–This qualifier will be used for a Cancel Message.  
e.g., :23G:NEWM 
22F Trade Transaction Type Indicator (TRTR)  
Since MBSD Pool Instructs are bilateral cash (buy/sell) transactions, this mandatory field should only 
contain the value indicated below.  
• TRTR/DTCY/CASH-This qualifier/[[Option]] should be used on all messages to specify that the 
messages refer to buy/sell Pool Instructs requiring two -sided comparison.  
e.g., :22F::TRTR/DTCY/CASH  
LINK The LINK Block can be repeated for the various reference qualifiers required on a trade 
contract. It is intended to provide the required information to identify the trade. Each reference 
number must be enclosed within a Start Link Block (:16R:LINK) and End Link Block 
(:16S:LINK). Each LINK repeating subsequence is within the GENL Block. At least one LINK 
sequence is required on the MT515 message.  
20C Reference 
The Reference Numbers provided by the [[participant]] must contain upper case alphanumeric 
characters, but not symbols or hyphens. As indicated above, each reference number must be 
enclosed in a LINK Start and End block.  
• MAST//- Master Reference Number -This  qualifier contains the [[participant]]’s External Reference 
Number, which must be unique for an Instruct record. It is mandatory for an inbound MT515 
Instruct message. The following table identifies what is needed for each message type:  
For message type:  The MAST field should be populated with:  
Instruct • The primary reference number used by participants to track 
their Instructs in the Pool  Netting  system. 
CDR, CDR Release, Cancel 
and Modify  
• The [[participant]]'s current X -ref. 
DK Message • The value “NONREF," if the DK message targets a Pool 
Instruct. 
 
• PREV//- Previous Reference Number - This qualifier is used on Modify and Cancel Messages.  
For message type:  The PREV field should be populated with:  
Modify  • The [[participant]]'s previous X -ref, if relevant. 
Cancel  • The value “NONREF” for all Cancel records (when 
:23G:CANC and :22F::PROC/DTCY/CANC are in the 
Confirmation Details (CONFDET) block). 

---

## Page 13

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 13 
Block/Tag Notes 
Instruct, CDR, CDR Release, 
and DK Message 
• [[DO]] not  populate this field. It should be left blank.  
 
• LIST//- Pool Netting Reference Number -This qualifier contains the Pool Identifier (PID) assigned 
by Pool Netting to a Pool Instruct.  
The Pool Netting Reference Number (LIST)  can be used on CDR, CDR Release, Modify, and 
Cancel records only –- it does not apply to Instruct or DK records targeting a Pool Instruct.  
For message type:  This field should be populated with the following:  
• CDR 
• CDR Release 
• Cancel  
• Modify  
Participants should populate the (LIST) field with the Pool 
Netting Reference Number.  
Instruct and DK Messages 
targeting a Pool Instruct  
[[DO]] not populate this field. It should be left lank.  
 
Notes: 
Where it is supplied, the PID will be used by Pool Netting to identify the Pool Instructs, rather than the 
reference provided in the (MAST) field.  
While the SWIFT message accommodates both upper and lower case alphanumeric and certain 
symbols, for MBSD purposes, this field must be populated with an upper case alphanumeric value. It 
cannot contain symbols or hyphens, except where the reference number is assigned by Pool Netting.  
e.g., :20C::MAST//REF010 
CONFDET The mandatory CONFDET (Confirmation Details) block appears only once in a trade contract. 
It contains Trade and Confirming Party Details.  
98C Trade Date & Time 
• TRAD//-This field is used on all Pool Netting input messages  to specify the trade date and must be 
populated with the trade date of the targeted TBA position.  . 
Note: 
The “C” format for this (98) tag indicates a date/time format of “Y YYYMMDDHHMMSS”; although the 
time is not used and may be set to ‘000000’.  
e.g., :98C::TRAD//20011218000000 
98A [[settlement]] Date 
• SETT//-This field is used on all messages to specify the [[settlement]] date. The “A” format for this tag 
(98) indicates a date format of “YYYYMMDD." This field must be populated with the full contractual 
[[settlement]] date of the targeted TBA position, using the format mentioned above.  
− Pool Netting will reject the message if it contains a [[settlement]] date for which the day (“DD”) is 
left blank, is populated with “00,” or is a day that is not valid for the given year and month.  
e.g., :98A::SETT//20011219 
90A Deal Price 

---

## Page 14

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 14 
Block/Tag Notes 
This field must be reflected on all MT515 messages. It contains the targeted TBA position's Price 
Type and Price. Only  one Tag 90A is allowed per Pool Instruct. The price is expressed as a decimal 
number in SWIFT Standard format, which is left justified, with commas removed, and a comma used 
instead of a decimal.  
• DEAL//PRCT/-This qualifier/[[Option]] is used for dollar prices , expressed as a decimal number. 
− This is a Deal Price that does not include commission.  
e.g., :90A::DEAL//PRCT/99,625 
19A [[settlement]] Amount  
• SETT//USD-This optional field may be used by participants to submit final money on pool inputs 
based on the factor available in their systems.  
The Amount is in SWIFT Standard format, which is left justified, with commas removed, and a 
comma used in lieu of a decimal. The amount is always preceded by a 3- character ISO currency 
code (“USD” for MBSD pool inputs).  
Note: 
The SWIFT format can accommodate a value of 15d in this field.  
e.g., :19A::SETT//USD1000000, 
22H Trade Type Indicator (BUSE)  
This field is required on all MT515 messages and has two allowable values:  
• BUSE//BUYI-This qualifier/[[Option]] indicates that the Pool Instruct submitted is a buy.  
• BUSE//SELL-This qualifier/[[Option]] indicates that the Pool Instruct submitted is a sell.  
e.g., :22H::BUSE//BUYI 
22F Processing Indicator (PROC)  
This Processing Indicator  enables the [[participant]] to indicate to Pool Netting the record 
type/command being submitted on an MT515 message.  
The allowable values for this field are:  
• PROC/DTCY/INST-This qualifier/[[Option]] indicates that the MT515 is an Instruct record.  
• PROC/DTCY/CANC-This qualifier/[[Option]] indicates that the MT515 is a Cancel record.  
• PROC/DTCY/MDFC-This qualifier/[[Option]] indicates that the MT515 is a Modify record.  
• PROC/DTCY/TDDK-This qualifier/[[Option]] indicates that the MT515 is a DK record.  
• PROC/DTCY/CDRQ-This qualifier/opti on indicates that the MT515 is a CDR record.  
• ROC/DTCY/CDRL-This qualifier/[[Option]] indicates that the MT515 is a CDR Release record.  
e.g., :22F::PROC/DTCY/INST  
22H Payment Indicator (PAYM)  
This Payment Indicator field is mandatory for the MT515 message. All  Pool Instructs submitted to 
Pool Netting must provide the following qualifier:  
• PAYM//APMT-This qualifier/[[Option]] indicates that the Pool Instruct will settle against payment.  
e.g., :22H::PAYM//APMT 
CONFPRTY The Mandatory Confirming Party Block must be repeated for each party to a trade. Each party 
specified must be enclosed within a Start Party block (:16R:CONFPRTY) and an End Party 
block (:16S:CONFPRTY). All MT515 messages should contain two repeating Confirming Party 
sequences (one [[Buyer]] and one [[Seller]], and one of these parties will also be the submitter of 
the MT515 message). 

---

## Page 15

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 15 
Block/Tag Notes 
95R Party 
• BUYR/DTCY/PART-specifies the Buying Party on all MT515 messages.  
• SELL/DTCY/PART-specifies the Selling Party on all MT515 messages.  
Note: 
While the SWIFT layout supports a format of 34x for this field, the [[participant]] must populate the field 
with the appropriate 4 character [[participant]] Account [[ID]], for [[Buyer]] or [[Seller]].  
e.g., :95R::BUYR/DTCY/PARTDLRA  
20C Contra Transaction Reference (PROC)  
This field only applies to DK Messages targeting Pool Instructs.  
• PROC//-The DK’ing party should use this field to indicate the contra’s PID on DK Messages 
targeting Pool Instructs.  
e.g., :20C::PROC//7096000247 
36B Quantity of [[securities]] (CONF)  
• CONF//FAMT/-This field is mandatory, and for the purposes of Pool Netting, must use the [[Option]] 
‘FAMT’- indicating face amount (par). Participants must populate this field with the Original Face 
Value of the Transaction. The quantity of the financial instrument is in SWIFT Standard Format, 
which is left justified, with commas removed, and one comma used instead of a decimal.  
e.g., :36B::CONF//FAMT/1000000,  
35B Identification of Security  
This mandatory field identifies the security (TBA) involved. US [[securities]] are identified by specifying 
the ISO country identifier (‘/US/’), followed by the [[CUSIP]] number. This field must contain the TBA 
[[CUSIP]] pertaining to the targeted TBA position.  
Note: 
While the SWIFT layout accommodates a format of 4 * 35x, a 9!c (alpha n umeric) value should be 
used to populate the field for the TBA [[CUSIP]].  
FIA In Pool Netting, this optional block is necessary to identify the pool being submitted against a 
TBA position. 
13B Number Identification  
• POOL/DTCY/-must be used by the [[participant]] to identify the pool number submitted. The pool 
number will be used in conjunction with the TBA [[CUSIP]] to ensure security identifier uniqueness.  
e.g., :13B::POOL/DTCY/123456  
70E Trade Instruction Processing Narrative (TPRO)  
This field (optional for SWIFT, but mandatory for the purposes of MBSD Pool Netting) will be used to 
support trade -related information not included in the MT515 format. At this point, it will be used to 
indicate the trade service type, the CDR indicator, the Delivery  Date, and a DK reason, where 
appropriate.  
• TPRO//DTCY-denotes Trade Processing narrative information specific to MBSD. The following 
Trade Service Type must be included on a message:  
− /TDSVPOOL- will be used for pool input messages.  

---

## Page 16

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 16 
Block/Tag Notes 
• /CDRY–specifies the pool  has a CDR status. Only disclosed on the message destined to the 
submitter. 
Note: 
In the MT515 pool input message, this indicator  is designed to only be used on Pool Instruct 
messages to indicate that this Pool Instruct will have a CDR status. However, if this indicator is 
included in non- Instruct input messages, the Pool Netting system will NOT reject the input message 
and will ignore the /CDRY indicator. To request or release the CDR status on an already accepted 
Instruct, the [[participant]] has to explicitl y submit the CDR request or CDR Release request.  
In the MT518 Pool Netting output messages, this indicator is designed to inform the submitter that the 
underlying Pool Instruct currently has the CDR status applied.  
• /DDTE–specifies the delivery date of the pool.  
• A DK reason must be included on all inbound MT515 DK records.  
− /DKRS–specifies the DK reason (on DK Messages only) –for a list of DK reasons, see 
Appendix A.  
e.g., :70E::TPRO//DTCY/TDSVPOOL  
2.3 Mt515 Pool Netting Input Messages–Field Analysis 
M/
O 
Tag Block/ 
Qualifier  
Subqualifier/  
Options 
Field Description INST CANC MDFC TDDK CDRQ CDRL 
    Message Header        
M    Password       
M    Sender        
M    Message Type       
M    Receiver       
M :16R: GENL  Block Start       
M :20C: :SEME//  Sender’s Reference for this 
Msg 
      
M :23G: NEWM  Msg Function = New or        
  CANC  Cancel       
M :22F: :TRTR/ DTCY/CASH Cash Buy/Sell Trade Indicator        
M :16R:  LINK  Repeat Block Start       
O :20C: :MAST//  Master Reference Number       
M :16S: LINK  Repeat Block End       
M :16R:  LINK  Repeat Block Start       
O :20C: :PREV//   Previous Reference Number        

---

## Page 17

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 17 
M/
O 
Tag Block/ 
Qualifier  
Subqualifier/  
Options 
Field Description INST CANC MDFC TDDK CDRQ CDRL 
M :16S: LINK  Repeat Block End       
M :16R:  LINK  Repeat Block Start       
O :20C: :LIST//  Pool Netting Assigned 
Reference (PID) 
      
M :16S: LINK  Repeat Block End       
M :16S: GENL  Block End       
M :16R: CONFDET  Block Start       
M :98C: :TRAD//  Pool Input Date & Time       
M :98A:  :SETT//  [[settlement]] Date       
M :90A:  :DEAL/ /PRCT/ Deal Price–Percentage       
O :19A:  :SETT/ /USD [[settlement]] Amount        
M :22H: :BUSE/ /BUYI  Trade Type–Buy or       
   /SELL  Sell       
O :22F: :PROC/ DTCY/INST Instruct Processing Indicator  or       
   DTCY/CANC Cancel Processing Indicator  or       
   DTCY/MDFC Modify Processing Indicator  or       
   DTCY/TDDK DK Processing Indicator  or       
   DTCY/CDRQ CDR Request Indicator  or       
   DTCY/CDRL CDR Release Indicator        
M :22H: :PAYM/ /APMT Against Payment Indicator        
M :16R: CONFPRTY  Repeat Block Start       
M :95R: :BUYR/ DTCY/PART Party = [[Buyer]]       
O :20C: :PROC//  Contra Transaction Reference       
M :16S: CONFPRTY  Repeat Block End        
M :16R: CONFPRTY  Repeat Block Start       
M :95R: :SELL/  DTCY/PART Party = [[Seller]]       
O :20C: :PROC//  Contra Transaction Reference       
M :16S: CONFPRTY  Repeat Block End        
M :36B:  :CONF/ /FAMT/ Quantity as Face Amount –
Original Face Value (Par) 
      
M :35B:  /US/  TBA [[CUSIP]]       

---

## Page 18

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 18 
M/
O 
Tag Block/ 
Qualifier  
Subqualifier/  
Options 
Field Description INST CANC MDFC TDDK CDRQ CDRL 
M :16R: FIA  Optional Block Start       
O :13B:  :POOL/ DTCY/ Pool Number       
M :16S: FIA  Block End       
O :70E:  :TPRO/ /DTCY Trade Instruction Processing 
Narrative or 
      
   /TDSVPOOL  Trade Service Type-Pool Input 
for Pool Netting or 
      
   /CDRY CDR Indicator or       
   /DDTE Delivery Date or       
   /DKRS DK Reason       
M :16S: CONFDET  Block End       

---

## Page 19

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 19 
3. MT509 POOL NETTING OUTPUT MESSAGES 
This section contains the following sub-sections: 
3.1 General Format 
3.2 Field Specifications 
3.3 Field Analysis 
Note: 
See Item #2 in Section 1.1 for a description of what the shaded color indicates.  
3.1 MT509 Pool Netting Output Messages–General Format 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
    Message Header  
M    Password  12!c 
M    Sender  8!c 
M    Message Type 3!n/3!n/4!c  
M    Receiver  8!c 
M :16R: GENL  Block Start  
M :20C: :SEME//  Sender’s Reference for this Msg.  16x 
M :23G: INST  Message Function –Pool Instruct or  4!c 
  CAST  Cancel   
O :98C: :PREP//  Preparation Date/Time YYYYMMDDHHMMSS 
M :16R: LINK  Repeat Block Start  
M :20C: :MAST//  Master Reference Number  
(External Reference)  
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PREV//  Previous Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :RELA//  Related Reference Number  (Sender’s 
Reference)  
16x 

---

## Page 20

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 20 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :LIST//  Pool Netting Assigned Reference  (PID) 16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PROG//  Pool Netting Assigned Contra  
Reference (Contra's PID)  
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :COMM//  Pool Netting Assigned Compared [[ID]]  
(CID) 
16x 
M :16S: LINK  Repeat Block End  
M :16R: STAT  Repeat Block Start  
M :25D: :IPRC/ /PACK Pool Instruct is  Acknowledged/Validated 
or 
4!c 
   /REJT Pool Instruct, Modify, DK, CDR, CDR 
Release is rejected or  
 
   DTCY/MODA Modify Accepted or   
   DTCY/MODP Modify Processed or   
   DTCY/PADK DK Accepted or   
   DTCY/DPPR DK Processed or   
   DTCY/PACD CDR Accepted/Validated or   
   DTCY/PACL CDR Release Accepted/Validated or   
   DTCY/DELE Deleted Unmatched Transaction or   
   DTCY/DEPE Deleted Due to Pending or   
   DTCY/DEIP Deleted Due to Insufficient TBA  Position 
or 
 
   DTCY/DEPS Deleted Due to Fully Paid -Down  
Security or  
 
   DTCY/DESA Deleted Due To System Action or   
   DTCY/NBTD Trade Bound to Net or   
   DTCY/NNCT Trade Not Netted or   
   DTCY/NECT Trade in Net or   

---

## Page 21

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 21 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
   DTCY/NECV Non -Net Pool Instruct Converted   
   DTCY/PDCV STIP Pool Instruct Converted   
  :CPRC/ /PACK Cancel Accepted or   
   /REJT Cancel Rejected or   
   /CAND Cancel Processed or   
  :MTCH/ /MACH Pool Instruct has been Matched or   
   /NMAT Pool Instruct has been Unmatched   
M :16R: REAS  Repeat Block Start  
M :24B: :REJT/ DTCY/ Reject Reason Code (see Appendix  A) 
or 
4!c 
  :NMAT/ /CPCA Unmatched due to the counterparty  has 
cancelled its instruction.  
4!c 
O :70D: :REAS/ /DTCY Reject Reason Narrative or  (6*35x) 
   /MDRJ Modify Rejected or  4!c 
   /DKRJ DK Rejected or   
   /CQRJ CDR Rejected or   
   /CLRJ CDR Release Rejected   
M :16S: REAS  Repeat Block End  
M :16S: STAT  Repeat Block End  
M :16S: GENL  Block End  
3.2 MT509 Pool Netting Output–Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a message header. All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password 12!c Password fields will be blank filled on MT509 messages.  
Sender 8!c MBSCPNET (MBSD Pool Netting System) will always be the sender of the 
MT509 matching -related messages.  
Message Type 3!n/3!n/4!c  The first three characters indicate to the recipient the message type (509); the 
second three positions reflect the version of the message interface (currently always 
000). The last four characters indicate the [[issuer]] code to be used in  the message 
(“DTCY”). 
Receiver 8!c MBSD account number of the [[participant]] receiving the message.  

---

## Page 22

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 22 
Block/Tag Notes 
GENL This Mandatory Block provides general information regarding the message. It appears only 
once in a Status Message. 
20C Sender Message Reference 
SEME//-This mandatory field contains the sender’s (Pool Netting) message reference number. It is 
used on all messages sent by Pool Netting and will contain a unique number to unambiguously 
identify each message. (This is a communications message number, not a trade number.)  
Note: 
While the SWIFT message accommodates both upper and lower case alphanumeric and certain 
symbols, for Pool Netting purposes, this field will be populated with an upper case alphanumeric value. 
It will not contain symbols or hyphens.  
e.g., :20C::SEME//110107090000000 
23G Function of the Message 
This mandatory field is used on all messages to identify the function of the message. It will either 
reflect the status of a new message (INST) or the status of the cancellation of a previous message 
(CAST). 
• INST-This qualifier will be used on the following MT509 messages:  
− all MT509 transaction/trade status messages referring to previously submitted Pool  Instructs, 
Modifies, CDRs, CDR Releases or DKs;  
− all MT509 Reject Messages where the MT515 was rejected for being non -SWIFT compliant, 
even where the original message may have been a Cancel;  
− all messages containing a matching status;  
− all Deleted Messages; and  
− all status messages as pending status assigned or removed, trade bound to net, trade in net, 
or trade not netted.  
• CAST-The CAST qualifier will be used for MT509 trade status messages referring to prev iously 
submitted Cancels.  
e.g., :23G:INST  
98C Preparation Date and Time 
• PREP//-This field will be reflected on all MT509 messages to indicate the date and time the 
message was prepared by Pool Netting.  
Note: 
The “C” format for this (98) tag indicates a date/time format of “YYYYMMDDHHMMSS." 
e.g., :98C::PREP//20011218111914 
LINK The LINK Block will be repeated for as many reference qualifiers as need to be included in a 
Trade Status Message. Each subsequence contains reference numbers to ident ify the 
transaction or trade for which the status is being reported. Each reference number will be 
enclosed within a Start Link Block (:16R:LINK) and End Link Block (:16S:LINK). All LINK 
repeating subsequences are within the GENL Block.  
20C Reference 
The Reference Numbers that have been provided by participants must contain upper case 
alphanumeric characters, but not symbols. As indicated above, each reference number will be 
enclosed in a LINK Start and End Block.  

---

## Page 23

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 23 
Block/Tag Notes 
• MAST//- Master Reference Num ber-This qualifier will always be populated with the [[participant]]’s 
External Reference Number (x -ref). 
This field may not be populated on MT509's under the following circumstances:  
− A MT515 DK Message targeting a Comparison Request  
− Any MT515 message that was rejected for being non -SWIFT compliant.  
• PREV//- Previous Reference Number  – 
− This qualifier is used only on records where the [[participant]] modifies the External Reference 
Number. On those records, the PREV field will reflect the submitter’s previous External 
Reference Number. 
• RELA//- MT515 Sender’s Message Reference Number -This qualifier will contain the Sender’s 
Message Reference Number (20C::SEME//) from the MT515 submitted by the [[participant]]. It will 
only appear on those MT509 messages that are acknowledgements of receipt or rejections of 
MT515 messages. This will be the only 20C qualifier in the LINK block where an MT509 Reject 
Message is being created for a non -SWIFT compliant MT515. 
• LIST//- Pool Netting Assigned Reference Number –This qualifier contains the Pool Netting 
Assigned Reference Number. It will appear on all MT509s, when it relates to your Pool Instructs. 
The Pool Netting Reference Number represents a PID.  
• PROG//- Pool Netting Assigned Contra Reference -This field specifies the co ntra’s Pool Netting 
assigned reference number (PID). It is reflected on MT509 messages where the receiving 
[[participant]] has DK’ed a Comparison Request submitted against it as well as on all the 
:25D::MTCH//MACH records. 
• COMM//-Pool Netting Assigned Compared  [[ID]] (CID)–This field specifies the [[participant]]’s Pool 
Netting Assigned Compared [[ID]] at the time of match. This qualifier will appear on MT509s for all 
matched records in order to enable participants to link the Pool Netting Assigned PID to the Pool 
Netting Assigned Compared [[ID]] (CID).  
Note: 
While the SWIFT message accommodates both upper and lower case alphanumeric and certain 
symbols, for MBSD purposes, this reference field will be populated with an upper case alphanumeric 
value. It will not contain symbols or hyphens, except where the reference number has been assigned 
by Pool Netting.  
e.g., :20C::MAST//PARTREF1 
STATUS The Status Block will appear on every MT509 message and will notify the [[participant]] of the 
type of MT509 record being sent, as well as the status of the transaction or trade that was 
submitted to Pool Netting.  
 Status Code  
The Status Code indicates the record type/type of status message being sent by Pool Netting. The 
following are the various message types which will be used for Interactive Messaging to support real -
time comparison.  
• IPRC//PACK-This qualifier/[[Option]] is used to indicate that a Pool Instruct Message has been 
accepted by Pool Netting.  
• IPRC//REJT-This qualifier/[[Option]] is used to indicate that a Pool Instruct, a Modify,  a CDR, a CDR 
Release or a DK Message has been rejected by Pool Netting. Field 70D in the REAS block will be 
populated as follows:  
− :70D::REAS//DTCY/MDRJ to indicate that a Modify record has been rejected;  
− :70D::REAS//DTCY/DKRJ to indicate that a DK record has been rejected;  
− :70D::REAS//DTCY/CQRJ to indicate that a CDR record has been rejected; or  
− :70D::REAS//DTCY/CLRJ to indicate that a CDR Release record has been rejected.  
The IPRC//REJT qualifier will be used in all instances where an incoming MT515 message is 
rejected for being non -SWIFT compliant (:24B::REJT/DTCY/F999).  

---

## Page 24

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 24 
Block/Tag Notes 
• IPRC/DTCY/MODA-This qualifier/[[Option]] is used to indicate to the submitter that a Modify record 
has been accepted.  
• IPRC/DTCY/MODP-This qualifier/[[Option]] is used to indicate to the submitter  that a Modify record 
has been processed.  
• IPRC/DTCY/PADK-This qualifier/[[Option]] is used to indicate to the submitter that a DK record has 
been accepted.  
• IPRC/DTCY/DPPR-This qualifier/[[Option]] is used to indicate to the submitter that a DK record has 
been processed.  
• IPRC/DTCY/PACD-This qualifier/[[Option]] is used to indicate to the submitter that a CDR message 
has been accepted and processed.  
• IPRC/DTCY/PACL-This qualifier/[[Option]] is used to indicate to the submitter that a CDR Release 
message has been accepted and processed.  
• IPRC/DTCY/DELE-This qualifier/[[Option]] is used to indicate to the submitter that a transaction that 
was pending comparison has been deleted by Pool Netting (now only used where an unmatched 
Pool Instruct is deleted from the system just prior to netting) .  
• IPRC/DTCY/DEPE-This qualifier/[[Option]] is used to indicate to the submitter that a transaction has 
been deleted by Pool Netting due to pending status (only used where matched Pool Instructs with 
pending status are deleted from the system just prior to netting).  
• IPRC/DTCY/DEIP-This qualifier/[[Option]] is used to indicate to the submitter that a transaction has 
been deleted by Pool Netting due to insufficient open TBA position (only used where matched Pool 
Instructs are deleted from the system either intraday or just prior to netting).  
• IPRC/DTCY/DEPS-This qualifier/[[Option]] is used to indicate to the submitter that a transaction has 
been deleted by Pool Netting due to the fact that the Pool Number specified has been fully paid -
down, i.e., the pool numb er has a factor of 0 (only used where matched Pool Instructs are deleted 
from the system either intraday or just prior to netting).  
• IPRC/DTCY/DESA-This qualifier/[[Option]] is used to indicate to the submitter that a transaction has 
been deleted by Pool Netting due to system -forced actions. (For example, a change to the security 
master record changes the validity of the pool for the TBA position.)  
• IPRC/DTCY/NBTD-This qualifier/[[Option]] is used to indicate to the submitter that Pool Netting is 
intending to Net the  Instruct. 
• IPRC/DTCY/NNCT-This qualifier/[[Option]] is used to indicate to the submitter that the Pool Instruct 
has been determined as NOT Nettable and will settle outside MBSD.  This is not applicable to 
[[Novation]]- eligible TBA CUSIPs.  
• IPRC/DTCY/NECT-This quali fier/[[Option]] is used to indicate to the submitter that the Pool Instruct 
has been Netted. 
• IPRC/DTCY/NECV - This qualifier/[[Option]] is used to indicate to the submitter that the Pool Instruct 
targeting a generic TBA trade was not netting eligible and therefore  converted to a pool obligation.  
• IPRC/DTCY/PDCV - This qualifier/[[Option]] is used to indicate to the submitter that the Pool Instruct 
targeting a STIP trade was converted to a pool obligation.  
• CPRC//PACK-This qualifier/[[Option]] is used to indicate to the submitter that a Cancel record has 
been accepted by Pool Netting.  
• CPRC//REJT-This qualifier/[[Option]] is used to indicate to the submitter that a Cancel submitted to 
Pool Netting has been rejected.  
• CPRC//CAND-This qualifier/[[Option]] is used to indicate that a Cancel  has been processed.  This 
record will be sent when Pool Netting has processed a Cancel submitted by a [[participant]].  
• MTCH//MACH-This record will be generated for every Pool Instruct that matches.  
• MTCH//NMAT-This record will be generated for every Pool Instru ct that becomes unmatched after 
its match event.  
e.g., :25D::IPRC//PACK 
REASON The Reason Block will only appear on MT509 messages where an MT515 message submitted 
by the [[participant]] has been rejected by Pool Netting or has become unmatched due to the 

---

## Page 25

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 25 
Block/Tag Notes 
contra’s cancellation. Each Reason Code must be enclosed within a Start Reason (:16R:REAS) 
and End Reason (:16S:REAS) Block.  
24B Reason Code  
This field is mandatory in the block and will appear on all Reject Messages and Unmatched 
Messages. There can be multiple Reason Codes on any MT509 Reject Message; each Reason Code 
must be enclosed within a Start Reason (:16R:REAS) and End Reason (:16S:REAS) Block. The 
Reason Code will be populated with the following values:  
• REJT/DTCY/-this qualifier will be reflected on all messages to indicate to the [[participant]] that the 
MT515 it submitted  was rejected by Pool Netting.  
• NMAT//CPCA–this qualifier/reason code will be reflected on all messages to indicate to the 
[[participant]] that the Instruct it submitted became unmatched as a result of the contra canceling its 
Instruct  
Note: 
As the list of error codes can be expanded in the future, the list will be amended, without modifying the 
entire specification. Please see Appendix A, which details all error conditions (and associated codes) 
that would result in the rejection of a [[participant]] MT515 mess age. 
e.g., :24B::REJT/DTCY/E004 
:24B::NMAT//CPCA 
70D Reason Narrative (REAS)  
• REAS//DTCY-The reason narrative field can contain narrative on those MT509 Reject Messages 
created in response to receiving a non -SWIFT compliant MT515, or can contain one of the  following 
qualifiers:  
• /MDRJ-this qualifier will be included on an MT509 Modify Rejected Message when an MT515 
Modify Message has been rejected by Pool Netting.  
• /DKRJ-this qualifier will be included on an MT509 DK Rejected Message when an MT515 DK 
Message has been rejected by Pool Netting.  
• /CQRJ-this qualifier will be included on an MT509 CDR Rejected Message when an MT515 CDR 
message has been rejected by Pool Netting.  
• /CLRJ-this qualifier will be included on an MT509 CDR Release Rejected Message when an 
MT515 CDR Release message has been rejected by Pool Netting.  
Note: 
This narrative field will appear in the first repeating REAS sequence.  
e.g., :70D::REAS//DTCY/MDRJ 
 
  

---

## Page 26

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 26 
3.3.1-MT509 Pool Netting Output Field Analysis–Part 1 of 3 (25D = IPRC) 
SWIFT MT509 LAYOUT MT509 Records 
M/
O 
Tag Block/ 
Qualifier  
Sub-
qualifier 
Field 
Description 
IPRC// 
PACK 
IPRC// 
REJT 
(*) 
IPRC/ 
DTCY/ 
MODA 
IPRC/ 
DTCY/ 
MODP 
IPRC/ 
DTCY/ 
PADK 
IPRC/ 
DTCY/ 
DPPR 
IPRC/ 
DTCY/ 
PACD 
IPRC/ 
DTCY/ 
PACL 
IPRC/ 
DTCY/ 
ASPP 
IPRC/ 
DTCY/ 
RVPP 
    Message 
Header 
          
M    Password           
M    Sender            
M    Message Type           
M    Receiver           
M :16R: GENL  Block Start           
M :20C: :SEME//  Sender’s 
Reference for 
this message 
          
M :23G: INST  Message 
Function- 
Instruct or  
          
  CAST  Cancel           
O :98C: :PREP//   Preparation 
Date/Time 
          
M :16R: LINK  Repeat Block 
Start 
          
M :20C: :MAST//  Master 
Reference No 
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: LINK  Repeat Block 
Start 
          
O :20C: :PREV//   Previous 
Reference No  
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: LINK  Repeat Block 
Start 
          
O :20C: :RELA//  Related 
Reference No 
(MT515 
sender’s ref) 
          

---

## Page 27

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 27 
SWIFT MT509 LAYOUT MT509 Records 
M :16S: LINK  Repeat Block 
End 
          
M :16R: LINK  Repeat Block 
Start 
          
O :20C: :LIST//  Pool Netting 
Assigned 
Reference  
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: LINK  Repeat Block 
Start 
          
O :20C: :PROG//  Pool Netting 
Assigned 
Contra 
Reference 
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: LINK  Repeat Block 
Start 
          
O :20C: :COMM//  Pool Netting 
Assigned 
Compared [[ID]] 
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: STAT  Repeat Block 
Start 
          
M :25D: :IPRC/ /PACK Pool Instruct is 
acknowledged/ 
validated or 
          
   /REJT Pool Instruct, 
Modify, DK, 
CDR, or CDR 
Release is 
rejected or 
          
   DTCY/ 
MODA 
Modify 
Accepted or  
          
   DTCY/ 
MODP 
Modify 
Processed or 
          
   DTCY/ 
PADK 
DK Accepted or            
   DTCY/ 
DPPR 
DK Processed 
or 
          

---

## Page 28

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 28 
SWIFT MT509 LAYOUT MT509 Records 
   DTCY/ 
PACD 
CDR 
Accepted/Valid
ated or 
          
   DTCY/ 
PACL 
CDR Release 
Accepted/Valid
ated or 
          
   DTCY/ 
DELE 
Deleted 
Uncompared 
Transaction or 
          
   DTCY/ 
DEPE 
Deleted 
Pending 
Transaction or 
          
   DTCY/ 
DEIP 
Deleted Due to 
Insufficient 
Position  
          
   DTCY/ 
DEPS 
Deleted Due to 
Fully Paid-
Down Security 
or 
          
   DTCY/ 
DESA 
Deleted Due to 
System Action 
or 
          
   DTCY/ 
NBTD 
Trade Bound to 
Net or 
          
   DTCY/ 
NNCT 
Trade Not 
Netted or 
          
   DTCY/ 
NECT 
Trade in Net or           
   DTCY/ 
NECV 
Non -Net PID 
Converted  
          
   DTCY/ 
PDCV 
STIP PID 
Converted  
          
  :CPRC/ /PACK Cancel 
Accepted or  
          
   /REJT Cancel 
Rejected or 
          
   /CAND Cancel 
Processed 
          
  :MTCH/ /MACH Trade Has 
Been Matched 
or 
          

---

## Page 29

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 29 
SWIFT MT509 LAYOUT MT509 Records 
   /NMAT Trade has been 
Unmatched 
          
M :16R: REAS  Optional 
Repeat Block 
Start 
          
M :24B:  :REJT/ DTCY/ Reject Reason 
Code or 
          
  :NMAT/ /CPCA Unmatched due 
to the contra’s 
cancellation 
          
O :70D: :REAS/ /DTCY Reject Reason 
Narrative or 
          
   /MDRJ Modify Rejected 
or 
          
   /DKRJ DK Rejected or           
   /CQRJ CDR Rejected 
or 
          
   /CLRJ CDR Release 
Rejected 
          
M :16S: REAS  Repeat Block 
End 
          
M :16S: STAT  Repeat Block 
End 
          
M :16S: GENL  Block End           
(*) The following 5 records are covered within the column labeled IPRC//REJT:  1. Pool instruct Rejected Messages  
2. Modify Rejected Messages  
3. DK Rejected Messages  
4. CDR Rejected Messages  
5. CDR Release Rejected Messages  
3.3.2-MT509 Pool Netting Output Field Analysis–Part 2 of 3 (25D = IPRC) 
SWIFT MT509 LAYOUT MT509 Records   
M/
O 
Tag Block/ 
Qualifier  
Sub-
qualifier 
Field 
Description 
IPRC// 
DTCY/ 
DELE 
IPRC// 
DTCY/ 
DEPE 
IPRC/ 
DTCY/ 
DEIP 
IPRC/ 
DTCY/ 
DEPS 
IPRC/ 
DTCY/ 
DESA 
IPRC/ 
DTCY/ 
NBTD 
IPRC/ 
DTCY/ 
NNCT 
IPRC/ 
DTCY/ 
NECT 
IPRC/ 
DTCY/ 
NECV 
IPRC/ 
DTCY/ 
PDCV 
    Message 
Header 
          
M    Password           

---

## Page 30

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 30 
SWIFT MT509 LAYOUT MT509 Records   
M    Sender            
M    Message Type           
M    Receiver           
M :16R: GENL  Block Start           
M :20C: :SEME//  Sender’s 
Reference for 
this message 
          
M :23G: INST  Message 
Function- 
Instruct or  
          
  CAST  Cancel           
O :98C: :PREP//   Preparation 
Date/Time 
          
M :16R: LINK  Repeat Block 
Start 
          
M :20C: :MAST//  Master 
Reference No.  
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: LINK  Repeat Block 
Start 
          
O :20C: :PREV//   Previous 
Reference No.  
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: LINK  Repeat Block 
Start 
          
O :20C: :RELA//  Related 
Reference No. 
(MT515 
sender’s ref) 
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: LINK  Repeat Block 
Start 
          
O :20C: :LIST//  Pool Netting 
Assigned 
Reference  
          
M :16S: LINK  Repeat Block 
End 
          

---

## Page 31

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 31 
SWIFT MT509 LAYOUT MT509 Records   
M :16R: LINK  Repeat Block 
Start 
          
 :20C: :PROG//  Pool Netting 
Assigned 
Contra 
Reference 
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: LINK  Repeat Block 
Start 
          
O :20C: :COMM//  Pool Netting 
Assigned 
Compared [[ID]] 
          
M :16S: LINK  Repeat Block 
End 
          
M :16R: STAT  Repeat Block 
Start 
          
M :25D: :IPRC/ /PACK Pool Instruct is 
acknowledged/ 
validated or 
          
   /REJT Pool Instruct, 
Modify, DK, 
CDR, or CDR 
Release is 
rejected or 
          
   DTCY/ 
MODA 
Modify 
Accepted or  
          
   DTCY 
/MODP 
Modify 
Processed or 
          
   DTCY/ 
PADK 
DK Accepted or           
   DTCY/ 
DPPR 
DK Processed 
or 
          
   DTCY/ 
PACD 
CDR 
Accepted/Valid
ated or 
          
   DTCY/ 
PACL 
CDR Release 
Accepted/Valid
ated or 
          
   DTCY/ 
DELE 
Deleted 
Uncompared 
Transaction or 
          

---

## Page 32

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 32 
SWIFT MT509 LAYOUT MT509 Records   
   DTCY/ 
DEPE 
Deleted 
Pending 
Transaction or 
          
   DTCY/ 
DEIP 
Deleted Due to 
Insufficient 
Position or 
          
   DTCY/ 
DEPS 
Deleted Due to 
Fully Paid-
Down Security 
or 
          
   DTCY/ 
DESA 
Deleted Due to 
System Action 
or 
          
   DTCY/ 
NBTD 
Trade Bound to 
Net or 
          
   DTCY/ 
NNCT 
Trade Not 
Netted or 
          
   DTCY/ 
NECT 
Trade In Net or           
   DTCY/NEC
V 
Non-Net Pool 
Instruct 
Converted 
          
   DTCY/PDC
V 
STIP Pool 
Instruct 
Converted 
          
  :CPRC/ /PACK Cancel 
Accepted or  
          
   /REJT Cancel 
Rejected or 
          
   /CAND Cancel 
Processed 
          
  :MTCH/ /MACH Trade Has 
Been Matched 
or 
          
   /NMAT Trade has been 
Unmatched 
          
M :16R: REAS  Optional 
Repeat Block 
Start 
          
M :24B:  :REJT/ DTCY/ Reject Reason 
Code or 
          

---

## Page 33

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 33 
SWIFT MT509 LAYOUT MT509 Records   
  :NMAT/ /CPCA Unmatched due 
to the contra’s 
cancellation 
          
O :70D: :REAS/ /DTCY Reject Reason 
Narrative or 
          
   /MDRJ Modify 
Rejected or 
          
   /DKRJ DK Rejected or           
   /CQRJ CDR Rejected 
or 
          
   /CLRJ CDR Release 
Rejected 
          
M :16S: REAS  Repeat Block 
End 
          
M :16S: STAT  Repeat Block 
End 
          
M :16S: GENL  Block End           
3.3.3-MT509 Pool Netting Output Field Analysis–Part 3 of 3 (25D = CPRC or 
MTCH) 
SWIFT MT509 LAYOUT  MT509 Records 
M/O Tag Block/ 
Qualifier 
Sub-
qualifier 
Field Description CPRC// 
PACK 
CPRC// 
REJT 
CPRC// 
CAND 
MTCH// 
MACH 
MTCH// 
NMAT 
    Message Header       
M    Password       
M    Sender       
M    Message Type      
M    Receiver       
M :16R: GENL  Block Start      
M :20C: :SEME//  Sender’s Reference for 
this message  
     
M :23G: INST  Message Function - 
Instruct or  
     
  CAST  Cancel       
O :98C: :PREP//  Preparation Date/Time      
M :16R: LINK  Repeat Block Start      

---

## Page 34

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 34 
SWIFT MT509 LAYOUT  MT509 Records 
M :20C: :MAST//  Master Reference No       
M :16S: LINK  Repeat Block End      
M :16R: LINK  Repeat Block Start      
O :20C: :PREV//  Previous Reference No        
M :16S: LINK  Repeat Block End      
M :16R: LINK  Repeat Block Start      
O :20C: :RELA//  Related Reference No 
(MT515 sender’s ref)  
     
M :16S: LINK  Repeat Block End      
M :16R: LINK  Repeat Block Start      
O :20C: :LIST//  Pool Netting Assigned 
Reference  
     
M :16S: LINK  Repeat Block End      
M :16R: LINK  Repeat Block Start      
O :20C: :PROG//  Pool Netting Assigned 
Contra Reference 
     
M :16S: LINK  Repeat Block End      
M :16R: LINK  Repeat Block Start      
O :20C: : COMM//  Compared [[ID]]       
M :16S: LINK  Repeat Block End      
M :16R: STAT  Repeat Block Start      
M :25D: :IPRC/ /PACK Pool Instruct is 
acknowledged/ 
validated or  
     
   /REJT Pool Instruct, Modify, 
DK, CDR, or CDR 
Release is rejected or  
     
   DTCY/ 
MODA 
Modify Accepted or       
   DTCY/ 
MODP 
Modify Processed or       
   DTCY/ 
PADK 
DK Accepted or       
   DTCY/ 
DPPR 
DK Processed or       

---

## Page 35

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 35 
SWIFT MT509 LAYOUT  MT509 Records 
   DTCY/ 
PACD 
CDR 
Accepted/Validated or  
     
   DTCY/ 
PACL 
CDR Release 
Accepted/Validated or  
     
   DTCY/ 
DELE 
Deleted Uncompared 
Transaction or  
     
   DTCY/ 
DEPE 
Deleted Pending 
Transaction or  
     
   DTCY/ 
DEIP 
Deleted Due to 
Insufficient Position or  
     
   DTCY/ 
DEPS 
Deleted Due to Fully 
Paid-Down Security or 
     
   DTCY/ 
DESA 
Deleted Due to System 
Action or  
     
   DTCY/ 
NBTD 
Trade Bound to Net or       
   DTCY/ 
NNCT 
Trade Not Netted or       
   DTCY/ 
NECT 
Trade In Net or       
   DTCY/NE
CV 
Non -Net Pool Instruct 
Converted  
     
   DTCY/PD
CV 
STIP Pool Instruct 
Converted  
     
   DTCY/ 
NECV 
Non -Net Pool Instruct 
Converted  
     
   DTCY/ 
PDCV 
STIP Pool Instruct 
Converted  
     
  :CPRC/ /PACK Cancel Accepted or       
   /REJT Cancel Rejected or       
   /CAND Cancel Processed       
  :MTCH/ /MACH Trade Has Been 
Matched or  
     
   /NMAT Trade Has been 
Unmatched  
     
M :16R: REAS  Optional Repeat Block 
Start 
     
M :24B: :REJT/ DTCY/ Reject Reason Code      

---

## Page 36

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 36 
SWIFT MT509 LAYOUT  MT509 Records 
  :NMAT/ /CPCA Unmatched due to the 
contra’s cancellation 
     
O :70D: :REAS/ /DTCY Reject Reason 
Narrative or  
     
   /MDRJ Modify Rejected or       
   /DKRJ DK Rejected or       
   /CQRJ CDR Rejected or       
   /CLRJ CDR Release Rejected       
M :16S: REAS  Repeat Block End      
M :16S: STAT  Repeat Block End      
M :16S: GENL  Block End      

---

## Page 37

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 37 
4. MT518 POOL NETTING OUTPUT MESSAGES 
This section contains the following sub-sections: 
4.1 General Format 
4.2 Field Specifications 
4.3 Field Analysis 
Note:  
See Item #2 in Section 1.1 for a description of what the shaded color indicates.   
4.1 MT518 Pool Netting Output Messages–General Format 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
    Message Header  
M    Password  12!c 
M    Sender  8!c 
M    Message Type 3!n/3!n/4!c  
M    Receiver  8!c 
M :16R: GENL  Mandatory Block Start   
M :20C: :SEME//  Sender’s Reference for this Msg  16x 
M :23G: NEWM [/COPY] Msg Function = New Instruct or  4!c[/4!c] 
  CANC [/COPY] Cancel   
O :98C: :PREP//  Preparation Date/Time YYYYMMDDHHMMSS 
M :22F: :TRTR/ DTCY/CASH Cash Buy/Sell Trade Indicator  4!c 
M :16R:  LINK  Repeat Block Start  
O :20C: :MAST//  Master Reference Number  (External 
Reference)  
16x 
M :16S: LINK  Repeat Block End  
M :16R:  LINK  Repeat Block Start  
O :20C: :PREV//  Previous Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16R:  LINK  Repeat Block Start  
O :20C: :LIST//  Pool Netting Assigned Reference (PID)  16x 

---

## Page 38

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 38 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
M :16S: LINK  Repeat Block End  
M :16R:  LINK  Repeat Block Start  
O :20C: :COMM  Pool Netting Assigned Compared [[ID]] 
(CID) 
16x 
M :16S: LINK  Repeat Block End  
M :16R:  LINK  Repeat Block Start  
O :20C: :BASK//  [[Broker]] Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16S: GENL  Block End  
M :16R: CONFDET  Block Start  
M :98C: :TRAD//  Pool Instruct Date & Time  YYYYMMDDHHMMSS 
M :98A: :SETT//  [[settlement]] Date YYYYMMDD 
M :90A: :DEAL/ /PRCT/ Deal Price–Percentage 15d 
O :19A: :SETT/ /USD [[settlement]] Amount  15d 
M :22H: :BUSE/ /BUYI Trade Type– Buy or 4!c 
   /SELL Sell  
O :22F: :PROC/ DTCY/CMPR Comparison Request or  4!c 
   DTCY/CRQM Comparison Request Modify or   
   DTCY/CADV Comparison Request Cancel or   
   DTCY/NAFI DK Advice or   
   DTCY/DCCX DK Remove Advice or   
   DTCY/SITR Screen Input Replay or   
   GSCC/SISR Screen Input Set Replay or   
   DTCY/MDAD Post Comparison Modification Advice or   
   DTCY/CMPM Pool Instruct Matched with Modifica t ions 
or 
 
   DTCY/DFVA [[default]] Values Applied or   
   DTCY/YTPR Repricing   
M :22H: :PAYM/ /APMT Against Payment Indicator  4!c 
M :16R: CONFPRTY  Repeat Block Start  
M :95R: :BUYR/ DTCY/PART Party = [[Buyer]] 34x 

---

## Page 39

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 39 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
O :20C: :PROC//  Pool Netting Assigned Contra 
Reference (Contra’s PID)  
16x 
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative or  4*35x 
   /TDID Trader [[ID]] 20c 
M :16S: CONFPRTY  Repeat Block End   
M :16R: CONFPRTY  Repeat Block Start  
M :95R: :SELL/ DTCY/PART Party = [[Seller]]  34x 
O :20C: :PROC//  Pool Netting Assigned Contra 
Reference (Contra’s PID)  
16x 
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative or  4*35x 
   /TDID Trader [[ID]] 20c 
M :16S: CONFPRTY  Repeat Block End   
M :36B: :CONF/ /FAMT/ Quantity as Face Amount - Original Fa ce 
Value (Par) 
15d 
M :35B: /US/  TBA [[CUSIP]] 9!c (4 * 35x) 
M :16R: FIA  Block Start  
O :12B: :OPTI/ /CALL [[Call option]] Type or  4!c 
   /PUTO [[Put Option]] Type   
O :98A: :EXPI//  Expiry Date YYYYMMDD 
O :13B: :POOL/ DTCY/ Pool Number 9x 
M :16S: FIA  Block End  
O :70E: :TPRO/ /DTCY Trade Instruction Processing Narrative 10*35x 
   /TDSVSBOD Trade Service Type– SBOD or 4!c 
   /TDSVTFTD Trade Service Type– Trade for Trade or  
   /TDSVCMPT Trade Service Type– Comparison Only 
or 
 
   /TDSVOPTN Trade Service Type– [[Option]] or   
   /TDSVPOOL Trade Service Type– Pool Instruct for 
Pool Netting or  
4!c 
   /CDRY CDR Indicator or (Only populated on the 
message destined for the 
submitter) 
   /DDTE Delivery Date or  
   /MSGR Message Reason (see Appendix A) or   4!c 

---

## Page 40

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 40 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
   /DKRS DK Reason (see Appendix A)  4!c 
   /GUPP Give Up Period  2n 
   /EPNX Pool Reference from EPN submission  16x 
M :16S: CONFDET  Block End  
4.2 MT518 Pool Netting Output Messages–Field Specifications 
Block/Tag Notes  
Message 
Header 
Each message must contain a message header. All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password 12!c Password fields will be blank filled on MT518 messages.  
Sender 8!c MBSCPNET (MBSD Pool Netting System) will alw ays be the sender of the Pool Netting 
MT518 messages.  
Message Type 3!n/3!n/4!c  The first three characters indicate to the recipient the message type (518); the second 
three positions reflect the version of the message interface (currently always 000). The 
last four characters indicate the [[issuer]] code to be used in the message (“DTCY”).  
Receiver 8!c MBSD account number of the [[participant]] receiving the message.  
GENL This mandatory block provides general information regarding the message.  
It appears only once in a Trade Confirm.  
20C Sender Message Reference 
• SEME//-This mandatory field contains the sender’s (Pool Netting) message reference number. It is 
used on all messages sent by Pool Netting and will contain a unique number to unambiguously 
identify each message. (This is a communications message number, not a trade number.)  
Note: 
While the SWIFT message accommodates both upper and lower case alphanumeric and certain 
symbols, for Pool Netting purposes, this field will be populat ed with an upper case alphanumeric value. 
It will not contain symbols or hyphens.  
e.g., :20C::SEME/1101070900000 

---

## Page 41

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 41 
Block/Tag Notes  
23G Function of the Message 
This mandatory field identifies the function of the message. It will either be a new message (NEWM) 
or a cancellation of a previous message (CANC):  
• NEWM-This NEWM qualifier will be used on the following MT518 messages:  
− Comparison Requests and Comparison Request Modifies;  
− Screen Input Replays that reflect a Pool Instruct, CDR, CDR Release or a Modify submitted  via 
terminal;  
− DK Advices and DK Remove Advices where the receiver of such advices is the submitter of a 
Pool Instruct that is being DK’ed 
− Trade Matched with Modifications;  
− Notification of [[default]] Values Applied; and  
− Repricing.  
• CANC-This CANC qualifier will be used on the following MT518 messages:  
− Comparison Request Cancels;  
− Screen Input Replays that reflect a Cancel submitted via terminal;  
e.g., :23G:NEWM 
98C Preparation Date and Time 
• PREP// -This field will be reflected on all messages to indicate the date and time the message was 
prepared by Pool Netting.  
Note: 
The “C” format for this (98) tag indicates a date/time format of “YYYYMMDDHHMMSS”.  
e.g., :98C::PREP//20011218143947 
22F Trade Transaction Type Indicator (TRTR)  
Since MBSD trades Pool Instructs are bilateral cash (buy/sell) transactions, this mandatory field 
should only contain the value indicated below at this time.  
• TRTR/DTCY/CASH-This qualifier/[[Option]] will be used on all MT518 messages to specify that they 
refer to buy/sel l trades Pool Instructs requiring two -sided comparison.  
e.g., :22F::TRTR/DTCY/CASH  
LINK The LINK Block will be repeated for as many reference qualifiers as need to be included in a 
Trade Confirm. It is intended to provide the required information to identify the trade. Each 
reference number must be enclosed within a Start Link Block (:16R:LINK) and E nd Link Block 
(:16S:LINK). Each LINK repeating subsequence is within the GENL Block.  

---

## Page 42

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 42 
Block/Tag Notes  
20C Reference 
The following reference qualifiers can be found on MT518 records:  
• MAST//-Master Reference Number -This qualifier will contain the external reference number (x -ref) 
of the transaction/trade represented on the record. The field will be populated:  
− On all MT518 records going to the original submitter of the transaction. , and 
Note:  
While the SWIFT message accommodates both upper and lowercase alphanumeric  and certain 
symbols, for MBSD purposes, this field will be populated with an uppercase alphanumeric value. It will 
not contain symbols or hyphens, except where the reference number has been assigned by Pool 
Netting. 
• PREV//-Previous Reference Number -This q ualifier will be reflected on all MT518 records sent to the 
original submitting party which are related to modifications of reference numbers.  
The PREV qualifier will also be reflected on all Cancel MT518 records. The PREV qualifier will be 
populated on MT 518 records as follows:  
− On all Cancel and Cancel Set records (:23G:CANC), this field will be populated with the value 
“NONREF”. 
• LIST//-Pool Netting Reference Number –On MT518 messages referring to your trades  
transactions, this field will contain the Pool Netting assigned reference number for the transaction 
or trade (or for the [[Broker]]'s submission before balancing. This field will not appear on Comparison 
Requests, Comparison Request Modifies or Comparison Request Cancels.  
Note: 
On Comparison Requests, Comparison Request Modifies and Comparison Request Cancels, the 
counterparty’s Pool Netting Transaction reference is provided in the appropriate [[Buyer]] or [[Seller]] 
Confirming Party subsequence, and not in this LINK  subsequence.  
• COMM//-Pool Netting Assigned Compared [[ID]] (CID) –This field specifies the [[participant]]’s Pool 
Netting Assigned Compared [[ID]] at the time of match. This qualifier will appear on MT518 for all 
matched records in order to enable participants to link the Pool Netting Assigned PID to the Pool 
Netting Assigned Compared [[ID]] (CID).  
e.g., :20C::MAST//PARTREF1 
CONFDET The mandatory CONFDET (Confirmation Details) block appears only once in a Trade Confirm. It 
contains Trade and Confirming Party Details.  
98C Trade Date 
• TRAD// - This field will be populated with the trade date of the targeted TBA position, and 
timestamp of ‘000000’ 
 
Note: 
The “C” format for this (98) tag indicates a date/time format of “YYYYMMDDHHMMSS”.  
e.g., :98C::TRAD//20011218000000 

---

## Page 43

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 43 
Block/Tag Notes  
98A [[settlement]] Date 
• SETT//-This field is used on all messages to specify the [[settlement]] date. The “A” format for this tag 
(98) indicates a date format of “YYYYMMDD”.  
e.g., :98A::SETT//20011219 
90A Deal Price 
This field is reflected on all MT518 messages. It contains the targeted TBA position’s Price Type and 
Price. Only one Tag 90A is allowed per Pool Instruct. The price is expressed as a decimal number in 
SWIFT Standard format, which is left justified, with commas removed, and a comma used instead of a 
decimal.  
• DEAL//PRCT/-This qualifier/[[Option]] is used for dollar prices, expressed as a decimal number.  
e.g., :90A::DEAL//PRCT/99,625 
19A [[settlement]] Amount  
• SETT//USD-This field is used to specify the [[settlement]] Amount for transactions . This field would 
not be include d in the MT518 messages if the final money has not been submitted by the 
[[participant]]/owner of the Pool Instruct.  
The Amount is in SWIFT Standard format, which is left justified, with commas removed, and a 
comma used in lieu of a decimal. The amount is always preceded by a 3- character ISO currency 
code (“USD” for MBSD transactions ).  
Note: 
The SWIFT format can accommodate a value of 15d in this field.  
e.g., :19A::SETT//USD2000000, 
22H Trade Type Indicator (BUSE)  
This field is reflected on all MT518 messages and has two allowable values for this BUSE qualifier:  
• BUSE//BUYI-This qualifier/[[Option]] indicates that the trade Pool Instruct reflected is a buy.  
• BUSE//SELL-This qualifier/[[Option]] indicates that the trade Pool Instruct reflected is a sell.  
e.g., :22H::BUSE//SELL 

---

## Page 44

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 44 
Block/Tag Notes  
22F Processing Indicator (PROC)  
This Processing Indicator  enables Pool Netting to indicate to the [[participant]] the type of 
record/command being submitted sent on this MT518.  
The allowable values for this field are:  
• PROC/DTCY/CMPR-This qualifier/[[Option]] indicates that the MT518 record is a Comparison 
Request. 
• PROC/DTCY/CRQM-This qualifier/[[Option]] indicates that the MT518 record is a Comparison 
Request Modify.  
• PROC/DTCY/CADV-This qualifier/[[Option]] indicates that the MT518 record is a Comparison Request 
Cancel (pre- comparison).  
• PROC/DTCY/NAFI-This qualifier/[[Option]] indicates that the MT518 record is a DK Advice.  
• PROC/DTCY/DCCX-This qualifier/[[Option]] indicates that the MT518 record is a DK Remove Advice.  
• PROC/DTCY/SITR-This qualifier/[[Option]] indicates that the MT518 record is a Screen Input Replay 
(applicable to screen inputs of Instruct, CDR, CDR Release, Modify, or Cancel records ; as well as 
RTTM generation of Pool Instructs due to forc e-compare ).  
• PROC/DTCY/MDAD-This qualifier/[[Option]] indicates that the MT518 record is a Post Comparison 
Modification Advice (of the recipient’s trade).  
• PROC/DTCY/CMPM–This qualifier/[[Option]] indicates that the MT518 record is a Matched with 
Modification Recor d. 
• PROC/DTCY/DFVA–This qualifier/[[Option]] indicates that the MT518 record is a [[default]] Values 
Applied Record.  
• PROC/DTCY/YTPR–This qualifier/[[Option]] indicates that the MT518 record is a Repricing Record.  
e.g., :22F::PROC/DTCY/CRQM  
22H Payment Indicator (PAYM)  
This Payment Indicator field is mandatory for the MT518 message. All MT518 records will reflect the 
following qualifier/tag:  
• PAYM//APMT-This qualifier/[[Option]] indicates that the Pool Instruct will settle against payment.  
e.g., :22H::PAYM//APMT 
CONFPRTY The Mandatory Confirming Party Block will be repeated for each party to a trade. Each party 
specified will be enclosed within a Start Party block (:16R:CONFPRTY) and an End Party block 
(:16S:CONFPRTY). MT518 messages will contain  two repeating Confirming Party sequences 
(one [[Buyer]] and one [[Seller]], and one of these parties will also be the receiver of the MT518 
message). 
95R Party 
• BUYR/DTCY/PART-specifies the Buying Party on all MT518 messages  
• SELL/DTCY/PART-specifies the Selling Party on all MT518 messages  
Note: 
While the SWIFT layout supports a format of 34x for this field, this field will be populated with the 
appropriate 4 character MBSD [[participant]] Account, for [[Buyer]] or [[Seller]].  
e.g., :95R::BUYR/DTCY/PARTABCD  

---

## Page 45

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifi cations 
About this Docum ent 45 
Block/Tag Notes  
20C Contra Transaction Reference (PROC)  
• PROC//-Processing Reference Number -This field will reflect the Pool Netting assigned 
Counterparty Transaction Reference (Contra's PID) in the ap propriate [[Buyer]] or [[Seller]] Confirming 
Party subsequence. It will only appear on Comparison Requests, Comparison Request Modifies 
and Comparison Request Cancels.  
e.g., :20C::PROC//7096000001 
36B Quantity of [[securities]] (CONF)  
• CONF//FAMT/-This field is mandatory, and for the purposes of Pool Netting, the [[Option]] ‘FAMT’ 
indicates that the face amount (par) will be used. This field will reflect the Original Face Value of the 
Pool Instruct. The quantity of the financial instrument is in SWIFT Standard Format , which is left 
justified, with commas removed, and a comma used instead of a decimal.  
e.g., :36B::CONF//FAMT/2000000,  
35B Identification of Security  
The security involved is identified in the US by specifying the ISO country identifier (‘/US/’), followed  
by the TBA [[CUSIP]] number of the targeted TBA position.  
Note: 
While the SWIFT layout accommodates a format of 4 * 35x, a 9!c (alpha numeric) value will populate 
the field for the TBA [[CUSIP]]. 
e.g., :35B:/US/01F070641 
FIA In Pool Netting, this Optional Block will be included to identify the pool being submitted 
against a TBA position.  
13B Number Identification  
• POOL/DTCY/-will be used by Pool Netting to identify the pool number allocated. The pool number 
will be used in conjunction with the TBA [[CUSIP]] to ensure security identifier uniqueness.  
e.g., :13B::POOL/DTCY/123456  
70E Trade Instruction Processing Narrative (TPRO)  
This field will be on all MT518 messages and will be used to reflect trade related information not 
supported in the MT518 fo rmat–it will be used to reflect a trade service type, a message reason, a 
CDR indicator, a Delivery Date, a DK reason  and EPN Pool Reference,  where appropriate.  
• TPRO//DTCY-denotes narrative information specific to MBSD. The following Trade Service Type 
will be included on each MT518 message:  
− /TDSVPOOL- will be used for pool output messages.  
• /CDRY–specifies the pool has a CDR status. Only being disclosed on the message destined to the 
submitter. 
Note: 
This indicator is designed to be only used along with Pool Instruct messages to indicate that this Pool 
Instruct will have a CDR status. However, if this indicator is included in non- instruct input messages, 
the Pool Netting system will NOT reject the input message and will ignore the /CDRY indicator. To 
request or release the CDR status on an already accepted instruct, the [[participant]] has to submit 
explicitly the CDR request or CDR Release request.  

---

## Page 46

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 46 
Block/Tag Notes  
In the MT518 Pool Netting output messages, this indicator  is designed to inform the submitter that the 
underlying Pool Instruct currently has the CDR status applied.  
• /DDTE–specifies the delivery date of the pool.  
MT518 Advisories can contain a message reason to further define an event on the Pool Netting 
system. 
• /MSGR–specifies the message reason –(see Appendix A for message reasons used in Pool 
Netting). 
All DK and DK Remove advices will contain a DK Reason:  
• /DKRS–specifies the DK reason (on DK Messages only) –(see Appendix A for DK reasons used in 
Pool Netting).  
 
Comparison requests generated as a result of EPN submission, and instructs compared against them, 
may have the following reference number if provided by the [[Seller]] on their corresponding EPN 
submission.  
• /EPNX – reflects the Pool Reference specified by the [[Seller]] in their corresponding EPN 
submission.  
e.g., :70E::TPRO//DTCY/TDSVPOOL  
4.3 MT518 Pool Netting Output Messages–Field Analysis 
M/O Tag Block/ 
Qualifier  
Sub-qualifier Field Description CMPR CRQM CADV NAFI DCCX SITR MDAD CMPM DFVA YTPR 
    Message Header            
    Password           
    Sender            
    Message Type           
    Receiver           
M :16R: GENL  Start of Block           
M :20C: :SEME//  Sender’s Reference for 
this message 
          
M :23G: NEWM  Message Function = 
New or 
          
  CANC  Cancel           
O :98C: :PREP//   Preparation Date/Time            
M :22F: :TRTR/ DTCY/CAS
H 
Cash Buy/Sell Trade 
Indicator  
          
M :16R: LINK  Start of Optional 
Repetitive 
Subsequence  
          

---

## Page 47

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 47 
M/O Tag Block/ 
Qualifier  
Sub-qualifier Field Description CMPR CRQM CADV NAFI DCCX SITR MDAD CMPM DFVA YTPR 
O :20C: :MAST//  Master Reference 
Number 
          
M :16S: LINK  End of Block           
M :16R: LINK  Start of Optional 
Repetitive 
Subsequence  
          
O :20C: :PREV//   Previous Reference 
Number 
          
M :16S: LINK  End of Block           
M :16R: LINK  Start of Optional 
Repetitive 
Subsequence  
          
O :20C: :LIST//  Pool Netting Assigned 
Reference Number 
(PID) 
          
M :16S: LINK  End of Block           
M :16R: LINK  Start of Optional 
Repetitive 
Subsequence  
          
O :20C: : COMM //  Pool Netting Assigned 
Compared [[ID]] 
          
M :16S: LINK  End of Block           
M :16S: GENL  End of Block           
M :16R: CONFDET  Start of Block           
M :98C: :TRAD//  Trade Date/Time           
M :98A:  :SETT//  [[settlement]] Date           
M :90A:  :DEAL/ /PRCT/ Deal Price-Percentage            
M :19A:  :SETT/ /USD [[settlement]] Amount            
M :22H: :BUSE/ /BUYI Trade Type Buy or           
   /SELL  Sell           
O :22F: :PROC/ DTCY/ 
CMPR 
Comparison Request or           
   DTCY/ 
CRQM 
Comparison Request 
Modify or 
          
   DTCY/ 
CADV 
Comparison Request 
Cancel or 
          

---

## Page 48

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 48 
M/O Tag Block/ 
Qualifier  
Sub-qualifier Field Description CMPR CRQM CADV NAFI DCCX SITR MDAD CMPM DFVA YTPR 
   DTCY/ NAFI DK Advice or           
   DTCY/ 
DCCX 
DK Remove Advice or           
   DTCY/ SITR Screen Input Replay or            
   DTCY/ 
MDAD 
Post Comparison 
Modification Advice or 
          
   DTCY/ 
CMPM 
Trade Matched with 
Modification or 
          
   DTCY/ 
DFVA 
[[default]] Value Applied 
or 
          
   DTCY/ 
YTPR 
Repricing           
M :22H: :PAYM/ /APMT Against Payment Trade            
M :16R: CONFPRTY  Start of Repetitive 
Mandatory 
Subsequence  
          
M :95R: :BUYR/ DTCY/ 
PART 
Buying Party           
O :20C: :PROC//  Pool Netting Assigned 
Contra Reference 
(Contra's PID) 
          
M :16S: CONFPRTY  Repeat Block End           
M :16R: CONFPRTY  Start of Repetitive 
Mandatory 
Subsequence  
          
M :95R: :SELL/  DTCY/ 
PART 
Selling Party           
O :20C: :PROC//  Pool Netting Assigned 
Contra Reference 
(Contra's PID) 
          
M :16S: CONFPRTY  Repeat Block End           
M :36B:  :CONF/ /FAMT/ Quantity as Face 
Amount (Par) 
          
M :35B:  /US/  TBA [[CUSIP]]           
M :16R: FIA  Start of Optional 
Subsequence  
          
M :13B:  :POOL/ /DTCY/ Pool Number           

---

## Page 49

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 49 
M/O Tag Block/ 
Qualifier  
Sub-qualifier Field Description CMPR CRQM CADV NAFI DCCX SITR MDAD CMPM DFVA YTPR 
M :16S: FIA  End of Optional 
Subsequence  
          
O :70E:  :TPRO/ /DTCY/ Trade Instruction 
Processing Narrative 
          
   /TDSVPOOL Trade Service–Pool 
Instruct for Pool Netting  
          
   /CDRY CDR indicator           
   /DDTE Delivery Date           
   /MSGR Message Reason           
   /DKRS DK Reason           
   /EPNX Pool Reference from 
EPN Submission 
          
M :16S: CONFDET  End of Block           

---

## Page 50

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 50 
5. MT599 POOL NETTING SYSTEM EVENT MESSAGES 
This section contains the following sub-sections: 
5.1 General Format 
5.2 Field Specifications 
Note: 
See Item #2 in Section 1.1 for a description of what the shaded color indicates.   
5.1 MT599 Pool Netting Output Messages–General Format 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
    Message Header   
M    Password  12!c 
M    Sender  8!c 
M    Message Type 3!n/3!n/4!c  
M    Receiver  8!c 
M :20:   Transaction (sender’s message) 
Reference Number 
16x 
M :79:   Narrative (35*50x) 
  DTCY/GADM  MBSD Administrative Message 4!c/4!c 
  /PREP/  Preparation Date/Time (8!n6!n) 
YYYYMMDDHHMMSS 
  /GSOD/  Pool Netting Start -of-Day Notification  or YYYYMMDD 
  /SOPN/  Start of Pool Netting  or YYYYMMDD 
  /EOPN/  End of Pool Netting or YYYYMMDD 
  /SEPN/  Start of Expanded Pool Netting or  YYYYMMDD 
  /EEPN/  End of Expanded Pool Netting or  YYYYMMDD 
  /EDCS/  Comparison Submission Cutoff  
End-of-Day Message or 
YYYYMMDD 
  /EODC/  End-of-Day Cycle Message YYYYMMDD 
  /NXTD/  Next MBSD ‘Trade Submission’ Day  YYYYMMDD 

---

## Page 51

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 51 
5.2 MT599 Pool Netting Output Messages–Field Specifications 
Block/Tag Notes  
Message 
Header 
Each Message must contain a message header. All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password 12!c This field will be blank -filled on all outbound MT599 Messages  
Sender 8!c MBSCPNET (MBSD Pool Netting System) will be the sender of the MT599 
messages.  
Message Type 3!n/3!n/4!c  The first three characters indicate to the recipient the message type (599); the 
second three positions reflect the version of the message interface (currently always 
000). The last four characters indicate the [[issuer]] code to be used in the message 
(“DTCY”). 
Receiver 8!c MBSD account number of the [[participant]] receiving the message. 
20 Transaction (Sender Message) Reference Number  
This field contains the sender’s message reference number. It is mandatory and will contain a unique 
number to unambiguously identify each message sent from MBSD. (This is a communications 
message number, not a trade number.)  
Note: 
While the SWIFT message accommodates both Upper and Lower case alphanumeric and certain 
symbols, for Pool Netting purposes, this field will be populated with an upper case alphanumeric value. 
It will not contain symbols or hyphens.  
e.g., :20:ABCDEFG1 
79 Narrative 
This field will contain the various administrative message data, including the type of message, using 
the following qualifiers:  
• DTCY/GADM–This qualifier/[[Option]] indicates that this is an administrative message being sent by 
MBSD. 
• /PREP/-This field contains the message preparation date and time.  
• /PSOD/ /GSOD/-This qualifier indicates to participants that this MT599 message is MBSD’s Pool 
Netting System beginning of day notification for the business date noted. Subsequent to receiving 
this message, participants can begin to send Pool Instructs to MBSD to be included in that day’s 
comparison process. Any messages received by MBSD after this point will result in immediate 
acknowledgement/rejection. Pool Netting will also, at this point, begin sending ack nowledgement/ 
rejection MT509 output for all trades inputs received after the prior business day’s cutoff point (i.e., 
the prior business day’s EDCS message).  
• /SOPN/-This qualifier indicates that this MT599 message is MBSD Pool Netting’s notification to th e 
[[participant]] that the current day’s pool netting process is starting. All inputs received by Pool Netting 
after this SOPN event (until the current day’s “EDCS” message) will still be included in the current 
day’s comparison process, but not eligible for t he current day’s pool netting process. The delivery 
day of all inputs received during this time range has to be greater than the next business date, 
otherwise Pool Netting will reject the input.  
• /EOPN/-This qualifier indicates that this MT599 message is MBSD Pool Netting’s notification to the 
[[participant]] that the current day’s pool netting process has completed.  
• /SEPN/ - This qualifier indicates that this MT599 message is MBSD Pool Netting’s notification to the 
[[participant]] that the current day’ s expanded pool netting process is starting. This occurs on SIFMA 
24hr day only.  

---

## Page 52

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
About this Docum ent 52 
Block/Tag Notes  
• /EEPN/ - This qualifier indicates that this MT599 message is MBSD Pool Netting’s notification to the 
[[participant]] that the current day’s expanded pool netting process has compl eted. This occurs on 
SIFMA 24hr day only.  
• /EDCS/-This qualifier indicates that this MT599 message is MBSD’s Pool Netting System’s 
notification to the [[participant]] that any inputs received by MBSD after this time will not be included in 
that day’s comparison  process. All inputs received by MBSD after this cutoff (until the next night’s 
cutoff/“EDCS” message) will be included in the comparison process for the date indicated below 
(following the qualifier ‘/NXTD/’).  
• /EODC/-This qualifier indicates that this MT 599 message is MBSD Pool Netting's notification to 
participants that MBSD has completed the Pool Netting process for the date indicated and no more 
interactive output will be generated for that business day. Any comparison -related output sent by 
MBSD after this point (through generation of the next ‘EODC’ message) will be for the business day 
indicated below (following the qualifier ‘/NXTD/’).  
• /NXTD/-This field provides the next valid MBSD trade submission date, and will be included on all 
MBSD end -of-day messages.  
e.g., :79:DTCY/GADM/PREP/20000322200150/EDCS/20000322/NXTD/20000323  

---

## Page 53

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
Appendices 53 
APPENDICES 
The documents included in this section are provided as a supplement to the Specifications included in this 
document. 
Appendix A Reason Codes for reject, message and DK.  
Appendix B SWIFT Output Message Groupings  available to provide members various levels of subscriptions 
to its SWIFT output messages.  
Appendix C Message Flows contains detailed diagrams depicting the flows of messages to and from RTTM 
for various transaction -related scenarios.  These flows have been divided into multiple sections.  
Appendix D Message Samples provides samples of a variety of MT515, MT509 and MT518 messages.  
Appendix A: Reason Codes 
This appendix contains the reason codes used for Rejects, Messages, and DKs. 
Reject Reason Codes 
Error Code Qualifiers  (to be used in 
field :24B::REJT/) 
Error Conditions (Which Can Cause  An MT515 
To Be Rejected By Pool Netting)  
Data Field Format 
DTCY/E001 External Reference Error  4!c 
DTCY/E002 Previous External Reference Error   
DTCY/E003 Trade Not Eligible for Cancellation   
DTCY/E004 Unknown Security (TBA [[CUSIP]])   
DTCY/E005 Bad Quantity   
DTCY/E007 Bad [[settlement]] Date  
DTCY/E008 Bad Price  
DTCY/E010 Bad [[Buyer]] Party   
DTCY/E011 Bad [[Seller]] Party   
DTCY/E013 Transaction Type Error   
DTCY/E014 Price Method Error   
DTCY/E016 Password Error  
DTCY/E030 Trade Not In  Same State  
DTCY/E033 Bad Delivery Date  
DTCY/E035 Bad Payment Indicator   
DTCY/E036 Unknown DK Reason  

---

## Page 54

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
Appendices 54 
Error Code Qualifiers  (to be used in 
field :24B::REJT/) 
Error Conditions (Which Can Cause  An MT515 
To Be Rejected By Pool Netting)  
Data Field Format 
DTCY/E102 Trade Service Type Error   
DTCY/E105 Account Trade Restricted   
DTCY/E108 Bad Pool Number  
DTCY/E112 Already CDRed   
DTCY/E113 CDR is not on  
DTCY/E132 Insufficient TBA position   
DTCY/E998 Trade Not Found  
DTCY/E999 Other Bad Data  
DTCY/F001 Illegal Operation Attempted   
DTCY/F002 Internal Process Error  
DTCY/F999 Non -SWIFT-Compliant Message   
Message Reason Codes 
Subqualifier/Options  Field Description Data Field Format  
DKTD Due to DK 4!c 
DCTD Due to DK Remove  
MACH Due to Match  
COAC Due to Contra Action  
GSAC Due to System Action  
YRAC Due to Your Action  
MODF Due to Pool Instruct Modified via screen  
CDRD Due to Pool Instruct CDRed via screen  
CDLD Due to Pool Instruct CDR Released via screen  
FCMP Due to Pool Instruct Force Compare by RTTM  
DK Reason Codes 
Subqualifier/Options  Field Description Data Field Format  
E004 Unknown Security (TBA [[CUSIP]]) 4!c 
E005 Bad Quantity   
E007 Bad [[settlement]] Date  
E008 Bad Price  
E009 Bad Amount  

---

## Page 55

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
Appendices 55 
Subqualifier/Options  Field Description Data Field Format  
E010 Bad [[Buyer]] Party   
E011 Bad [[Seller]] Party   
E013 Transaction Type Error   
E033 Bad Delivery Date  
E102 Trade Service Type Error   
E106 Incorrect Account Symbol   
E107 Duplicate Trade  
E108 Invalid Pool Number   
E998 Trade not found  
E999 Other Bad Data  
Appendix B: SWIFT Output Message Groupings 
Pool Netting offers the participants various levels of subscription to its SWIFT output messages. The 
participants can choose to enable/disable receiving the pool netting real-time SWIFT message by groups. 
All the groups are listed in the table below. 
Description 
Group 1. Administrative Messages  
MT599 GSOD (Pool Netting Start -of-Day Notification)  
MT599 SOPN (Start of Pool Netting)  
MT599 EOPN (End of Pool Netting)  
MT599 SEPN (Start of Expanded Pool Netting)  
MT599 EEPN (End of Expanded Pool Netting)  
MT599 EDCS (Comparison Submission Cutoff End -of-Day Message) 
MT599 ECDO (End -of-Day Cycle Message)  
Group 2. Pool Input Response (mandatory)  
MT509 Pool Trade Accepted  
MT509 Pool Trade Rejected  
MT509 Modify Accepted  
MT509 Modify Rejected  
MT509 DK Accepted  
MT509 DK Rejected  

---

## Page 56

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
Appendices 56 
Description 
MT509 Cancel Accepted  
MT509 Cancel Rejected  
MT509 CDR Reject  
MT509 CDR Accepted  
MT509 CDR Released  
MT509 CDR Release Rejected  
Group 3. Processed Messages 
MT509 Modify Processed  
MT509 DK Processed  
MT509 Cancel Processed  
Group 4. Match Messages 
MT509 Pool Trade Matched  
MT509 Unmatched due to Contra’s Cancellation 
Group 5. System Generated End of Life Messages 
MT509 Pool Trade Deleted (due to Unmatched)  
MT509 Pool Trade Deleted (due to Insufficient TBA Position)  
MT509 Pool Trade Deleted (due to Pending Status)  
MT509 Pool Instruct Deleted (due to Fully Paid -Down Pool)  
MT509 Pool Instruct Deleted (due to System Actions)  
MT509 Pool Bound to Net 
MT509 Pool In Net 
MT509 Non -Net Pool Instruct Converted  
MT509 STIP Pool Instruct Converted  
Group 6. Advice Messages 
MT518 Repricing  
MT518 Notification of [[default]] Value Applied  
MT518 Post Match Modify  
MT518 Pool Trade Matched with Modification 
MT518 DK Advice 
MT518 DK Removed Advice 
MT518 Screen Input Pool Trade Replay (Instruct)  

---

## Page 57

MBS CCP Pool Netting: SWIFT Interactive Messaging Specifications  
Appendices 57 
Description 
MT518 Screen Input Pool Trade Replay (Modify)  
MT518 Screen Input Pool Trade Replay (Cancel)  
MT518 Screen Input Pool Trade Replay (Force- Compare)  
MT509 Bound to Net 
Group 7. Advisories 
MT518 Comparison Request Modify  
MT518 Comparison Request  
MT518 Comparison Request Cancel  
Group 8. CDR Screen Replay 
MT518 Screen Input Trade Replay (CDR)  
MT518 Screen Input Trade Replay (CDR Release)  
 
 

---

## Page 58

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 