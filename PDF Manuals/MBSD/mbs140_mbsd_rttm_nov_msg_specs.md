---
title: "MBSD RTTM Novation: SWIFT Interactive Messaging Specifications"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs140_mbsd_rttm_nov_msg_specs.pdf"
pages: 167
size: "2278.0 KB"
category: "MBSD"
ingested_on: "2026-06-05"
---

# MBSD RTTM Novation: SWIFT Interactive Messaging Specifications

**Original File:** [mbs140_mbsd_rttm_nov_msg_specs.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/mbs140_mbsd_rttm_nov_msg_specs.pdf)  
**Category:** MBSD  
**Total Pages:** 167  
**File Size:** 2278.0 KB  

---

## Page 1

 
 
 
FIXED INCOME CLEARING 
CORPORATION 
MBSD RTTM® [[Novation]]:  
SWIFT INTERACTIVE MESSAGING SPECIFICATIONS  
 
VERSION 3.05 
JULY 17, 2017 
 


---

## Page 2

 
 
© 2022 [[DTCC]]. All rights reserved. [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation.  
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of Th e Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. P lease see 
www.[[DTCC]].com  for more information on [[DTCC]], its affiliates and the services they offer.  
 
 
Doc Date: July 17, 2017 
Publication Code:  MBS140 
Service: Fixed Income Clearing Corporation 
Title: MBSD RTTM  [[Novation]]: SWIFT Interactive Messaging Specifications  
 

---

## Page 3

 
 
TABLE OF CONTENTS 
Introduction to the Documentation.................................................................................................... 6  
Interactive Messaging for Real-Time Trad e Matc hing  (RTTM®) .............................................................. 6  
Aud ienc e...................................................................................................................................... 6  
Related Materials .......................................................................................................................... 6  
Version Control Page ....................................................................................................................... 7  
1. Introduction ................................................................................................................................10  
2. Interactive Messaging Guidelines .................................................................................................11  
2.1 Overview....................................................................................................................... 11 
2.2 Mess ag e Struc ture ......................................................................................................... 11 
2.2.1 Mess ag e Head er ............................................................................................................ 11  
2.2.2 Bloc ks and  Sub-blocks .................................................................................................... 11 
2.2.3 Fields ........................................................................................................................... 12 
2.2.4 Tag  and Field  Fo rmat Illus tratio ns  and Chart ...................................................................... 13 
2.2.5 Illustration of Message Structure ....................................................................................... 14 
2.2.6 Non-ISO 15022 Formats.................................................................................................. 14 
2.3 MT515 Message Overview .............................................................................................. 15 
2.4 MT509 Message Overview .............................................................................................. 16 
2.5 MT518 Message Overview .............................................................................................. 20 
2.6 MT599 Message Overview .............................................................................................. 22 
2.7 [[BASIC]] Message Flow ....................................................................................................... 23 
2.8 Dealer Flow Supplemental Information .............................................................................. 25 
2.8.1 Matching versus Brokers-Sp lits  and Sp lic es........................................................................ 25 
2.8.2 Bro k er Co mmiss io ns  Submitted by Dealers ........................................................................ 26 
2.8.3 Cancel Processing Post [[Novation]] ..................................................................................... 27 
2.8.4 [[DO]] Not Allocate .............................................................................................................. 27 
2.9 [[Broker]] Input Overview..................................................................................................... 28 
2.9.1 Two Party MT515s ......................................................................................................... 28 
2.9.2 Balanc ed  Sets ............................................................................................................... 28 

---

## Page 4

 
 
2.10 Reference Numbers........................................................................................................ 29 
3. Communications .........................................................................................................................30  
4. Message Specifications ...............................................................................................................31  
4.1 Mess ag e Fo rmat Guid elines............................................................................................. 31 
4.1.1 Formatting Rules ............................................................................................................ 31 
4.1.2 Formatting Conventions .................................................................................................. 32 
4.2 MT515 Message ............................................................................................................ 34 
4.2.1 MT515 General Format ................................................................................................... 35 
4.2.2 MT515 Field Specifications .............................................................................................. 39 
4.2.3 MT515 Field Analysis ...................................................................................................... 49 
4.3 MT509 Message ............................................................................................................ 54 
4.3.1 MT509 General Format ........................................................................................................ 55 
4.3.2 MT509 Field Specifications .............................................................................................. 60 
4.3.3 MT509 Field Analysis (25D=IPRC) .................................................................................... 65 
4.3.4 MT509 Field Analysis (25D=CPRC) .................................................................................. 70 
4.3.5 MT509 Field Analysis (25D=MTCH) .................................................................................. 75 
4.4 MT518 Message ............................................................................................................ 77 
4.4.1 MT518 General Format ................................................................................................... 79 
4.4.2 MT518 Field Specifications .............................................................................................. 83 
4.4.3 MT518 Field Specifications .............................................................................................. 93 
4.4.3 MT518 Field Analysis (Advisories) .................................................................................... 97 
4.4.4 MT518 Field Analysis (Advices Referring to Your Trades)....................................................101  
4.5 MT599 Message ...........................................................................................................107  
4.5.1 MT599 General Format ..................................................................................................108  
4.5.2 MT599 Field Specifications .............................................................................................108  
Appendices .................................................................................................................................. 111 
Appendix A: Mandatory Data for MBSD Input...................................................................................111  
A.1 Dealer Input..................................................................................................................111  
A.2 Bro k er Inp ut..................................................................................................................112  
Appendix B: Reference Number Usage in Messages ........................................................................112  

---

## Page 5

 
 
Transaction -Related  Ref erenc e Numb ers  o n Mess ag es  [[FRO]] m D ealers  to  RTTM...................................112  
Transaction-Related Reference Numbers on Messages from Brokers to RTTM ...................................113  
Transaction-Related Reference Numbers on Messages from RTTM to Dealers ...................................114  
Transaction-Related Reference Numbers on Messages from RTTM to Brokers ...................................116  
App end ix  C: ISO 15022 Mes s ag e Struc ture D iag rams.......................................................................122  
Mess ag e Struc ture D iag ram: MT515 .............................................................................................122  
Mess ag e Struc ture D iag ram: MT509 .............................................................................................123  
Mess ag e Struc ture D iag ram: MT518 .............................................................................................124  
Appen dix D: Me ssa ge Flow s .........................................................................................................125  
Dealer/Dealer Message Flows ......................................................................................................125  
[[Broker]]/Dealer Message Flows ......................................................................................................146  
Rejection Message Flows ............................................................................................................166  
 

---

## Page 6

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Introduction to the Doc umentation 6 
INTRODUCTION TO THE DOCUMENTATION 
Interactive Messaging for Real-Time Trade Matching (RTTM®) 
This document provides an overview of Interactive Messaging to support Real-Time Trade Matching (RTTM®) 
along with detailed message specifications (input and output) that will be used to support the process.  
As new functionality is added to the existing service, additions and modifications to these specifications may be 
required. This is therefore a "living" document that will be updated as interactive services are expanded. 
Audience 
This document was written for systems and development personnel, including managers, analysts and 
programmers. It presumes readers are familiar with technical concepts and terms, understand [[FICC]]'s 
Interactive Messaging specifications for RTTM
® and have a [[BASIC]] knowledge of the MBSD's services. 
Related Materials 
SWIFT  
The specifications for Interactive Messages are based on SWIFT messages. Readers are therefore strongly 
urged to refer to SWIFT user documentation to obtain a complete and comprehensive understanding of 
these message standards. SWIFT information (including many applicable message formats) can also be 
found on the Internet at www.iso15022.org. 
RTTM 
For additional information regarding RTTM, readers can refer to documentation found on the internet at 
https://www.[[DTCC]].com/clearing-services/[[FICC]]-mbsd/mbsd-rttm. 

---

## Page 7

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 7 
VERSION CONTROL PAGE 
Date Version # Name Description of Change  
07/05/2015 3.0 C. Swords  Made following document corrections:  
• Removed information related to changes introduced with the 
original RTTM version 1 .0. 
• Incorporated changes introduced with Specified Pool Trades, as 
published in version 2.0.  
07/15/2015 3.0 C. Swords  Made following enhancements to support [[Novation]]:  
• Introd uction of MT518 Trade Novated message 
• Introduction of STIP trade service type  
• Introduction of DNA and Cancel DNA in MT515, MT509 and 
MT518. 
• Add MT599 message for start/end Pool Conversion, DNA and TBA 
Reprice process  
• Introduction of “[[Broker]] match” identifi er, returned in dealer 
messages when matched against a [[Broker]] trade via split/splice or 
exact. 
• Flat rate commissions no longer used  
• Introduction of additional methods to identify SPT pool, using 
[[issuer]] and/or pool [[CUSIP]].  
• GUP no longer supported for [[Novation]]- eligible trades 
8/24/2015 3.0.1 C. Swords  Made following updates:  
• Tag 17b:STAN on MT515 and MT518 is now optional, rather than 
mandatory.  
1/6/2016 3.0.2 C. Swords  Message Specification  
Made following updates:  
• Add support for targeting specific t rades in a DNA by identifying 
RTTM-assigned Trade Ids.  This includes:  
• MT515 “DNA” (:22F::PROC/GSCC/DNAL) –add Trade [[ID]] to target 
for DNA (:70E::DECL//GSCC/TRID), and remove Original Trade 
Par (:70E::DECL//GSCC/ORTP) 
• MT509 DNA “ack” (:25D::IPRC/GSCC/DNAL)-renamed from “DNA 
Accepted and Applied” to “DNA Accepted”.  
• MT518 “DNA Assigned” (:22F::PROC/GSCC/DNAP) –new 
message added, which will follow the MT509 “DNA Accepted” and 
return individual trades the DNA was assigned to.  
Other DNA updates include:  
• A single MT518 “Screen Input DNA Replay” (SDNA) will be used 
to cover replay of DNA Create and Cancel.  Therefore, MT518 
processing code SCDN is no longer necessary.  
• Update CONFPRTY description on MT515 and MT518 to clarify 
usage for DNA requests.  
• Update 70E::DECL description on MT515 and MT518 to clarify 
usage for DNA requests.  
• Update 98C::TRAD description on MT518 to indicate set to Dec 
31, 9999 for DNA messages.  

---

## Page 8

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 8 
Date Version # Name Description of Change  
• Update 19A::SETT description on M518 to indicate omitted for 
DNA messages.  
MT509 Reject Codes –updated table to reflect new DNA -related and 
obsolete codes.  
   Message Flows  
Added message flows with following changes.  
Formatting changes:  
• Converted document and flows into standard template and format  
• Consolidated reject message flows to end of document.  
Document corrections:  
• DD10 “DK Removed from Transaction (via Terminal)” obsolete as 
DK remove not supported.  
• DD17 “Post -Comparison Cancel (via Affirmation or Terminal Entry 
of Cancel)” updated to reflect that affirm of cancel request not 
available.  
• BD3 “Unbalanced Trade Create Transactions (3x with same 
[[Broker]] Ref.)” obsolete as invalid scenario as duplicate transaction 
would be rejected.  
• BD4 “Erroneous Trade Create Transaction Canceled to Enable 
Balancing” obsolete as invalid scenario as duplicate transaction 
would be rejected.  
• BD5 “[[Broker]] Reference Modified by [[Broker]] Before Balancing” 
obsolete as this is not allowed.  
• BD8: “Dealer Trade Create DK’ed by [[Broker]], then DK Removed 
(via Terminal)” obsolete as DK remove not supported.  
• BD21 “FMAT Trade Cancel Request DK’ed, then DK Removed” 
obsolete as DK remove not supported.  
Document updates for SPT:  
• Incorpor ated SPT flows previously included in separate SWIFT 
RTTM document.  
Enhancements to support [[Novation]]:  
• Added MT518 [[Novation]] for all flows related to compared 
dealer/dealer, and FMAT [[Broker]]/dealer trades.  
• Added DNA message flows.  
9/16/2016 3.0.3 C. Swords  Made following updates.  
Corrections/Clarifications:  
• Table 4.4.4. MT518 Field Analysis –typographical error correction; 
processing code should be NOVT, not NOVA.  
• Clarify that MT518 Comparison Request Cancel (due to match) 
tag 70E::DECL//GSCC/CTRD contains Trade [[ID]] assigned to the 
receiving/contraparty trade upon matching/[[Novation]].   
Additional error  code:  
• Added MT509 DNA rej ect code E170 for maximum number of 
DNA terms/trade ids exceeded  

---

## Page 9

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 9 
Date Version # Name Description of Change  
3/15/2017 3.0.4 C. Swords  Made following updates:  
• For MT509, added new error code E171 for “Action will result in 
undeliverable piece”, for example, if DNA request will result in 
remaining open position of less than 25K.  
   Made following updates:  
• Section 2.8.4 [[DO]] Not Allocate, 2.5 MT518 Message Overview, 
DD23 DNA Create and DD24 DNA Created via WFE –update 
verbiage to indicate that DNA Assigned message means DNA has 
been assigned to individual trades only; previously, it indicated 
that this message returned individual Trade [[ID]]’s of associated 
trades but this only occurs for DNA submitted via Trade [[ID]] (not 
terms). 
n/a n/a [[DTCC]] 
Learning  
Updated formatting only. Content is unchanged.  

---

## Page 10

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 10 
1. INTRODUCTION 
Upon the implementation of Interactive Messaging for Real-Time Trade Matching (RTTM): 
• Participants will have the ability to submit trade input to RTTM intra-day, as trades are executed, using the 
SWIFT MT515 message format. This format will also be used by members to submit “[[DO]] Not Allocate 
(DNA)” requests to RTTM intra-day to pair-off positions and exclude them from the allocation process. 
 
• Submitters will immediately receive trade status information (i.e., notification of whether the trade or DNA 
Request has been accepted or rejected) via the SWIFT MT509 message format. This format will also be 
used to provide up-to-the-minute trade status information to Participants as transactions are processed by 
RTTM (for example, a message will be sent when a trade compares, is canceled or is modified). 
 
• Trade contraparties will also be notified immediately via a SWIFT MT518 message when a trade has been 
submitted against them. The SWIFT MT518 message will contain full trade details. It will also be used to 
communicate to the [[participant]] those changes that RTTM may have made to transaction records 
previously submitted, trade records previously created, DNA trade assignments or when Participants enter 
information directly to the system via terminal service. This means that Participants will have the ability to 
submit trade data to RTTM, review output, and identify and correct any errors, all within minutes of 
execution. 
 
• Administrative messages using the MT599 format will be generated each day indicating: 
1. System open for input, 
2. AM pass submission cutoff, 
3. Start of Pool Conversion, DNA [[settlement]], and TBA Reprice 
4. End of Pool Conversion, DNA [[settlement]], and TBA Reprice 
5. PM pass submission cutoff, and 
6. Output generation completed. 

---

## Page 11

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 11 
2. INTERACTIVE MESSAGING GUIDELINES 
This section of the document provides some background information that may be useful for interpreting the 
detailed message specifications that follow. 
2.1 Overview 
[[FICC]]/MBSD has adapted the ISO 15022 message formats for real-time interactive input and output associated 
with matching. While MBSD has elected to use SWIFT standardized messages for the RTTM interface, it uses 
a proprietary network for communication between MBSD and its members rather that utilizing the SWIFT 
network. 
2.2 Message Structure 
SWIFT ISO 15022 message formats are constructed using a modular methodology based on the premise that 
information can be identified and programmed once, then reused wherever needed. Using this approach, data 
is configured into logical groups (i.e., generic fields and blocks) according to business purpose. These groups 
are then uniquely identified (using tags, qualifiers and start/end block designators) so that they can be used 
whenever needed to fulfill particular business purposes across a number of messages without requiring 
extensive reprogramming. 
If the [[BASIC]] message structure were diagramed from the top down (going from the more general to the more 
specific), you would have a Message Header followed by one or more information blocks (potentially containing 
sub-blocks), composed of one or more fields. Each of these components is defined in the text below. 
2.2.1 Message Header 
The Message Header specifies the sending and receiving parties of the message and provides the message 
type. MBSD has added a password to this header to provide an additional level of security. The Message 
Header is the first component of every message. RTTM requires that the fields in the header have a fixed 
format, unlike the standard SWIFT Message Header. The header is populated as a continuous string of data, 
which terminates as a regular data field (with a carriage return line feed “CRLF”). 
2.2.2 Blocks and Sub-blocks 
A block may be defined as a group of fields containing related business information that is framed by start-of-
block and end-of-block designators. The use of a block is not restricted to any given message; it can be reused 
across a number of messages and combined with other blocks to fulfill a variety of business requirements. For 
example, the General Information block contains general information regarding the trade, such as trade 
reference numbers. The Confirmation Details block contains specific trade information such as trade date, 
[[settlement]] date, price, security and information regarding the confirming parties. 

---

## Page 12

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 12 
Each message contains one or more blocks. A typical message contains a general information block, followed 
by a series of detail blocks. These blocks may be mandatory or optional within a particular message, and are 
structured as follows: 
• A start-of-block designator (represented by the tag 16R), indicating the start of a group of related 
information; 
• One or more sub-blocks and/or fields; and 
• An end-of-block designator (represented by the tag 16S), indicating the end of a group of related 
information. 
An information block may be further divided into sub-blocks containing groups of fields that further define the 
block. The structure of a sub-block is the same as that of a block, the difference being that it is "nested" or 
contained within the block. For example, Confirmation Parties would be sub-blocks of the Confirmation Details 
block. Sub-blocks, under certain circumstances, can be repeated in a block. 
2.2.3 Fields 
There are two types of fields: generic fields and discrete fields. As the names imply, generic fields are multi-
purpose fields used across messages and message types, whereas discrete fields in messages are limited to a 
single purpose. Generic fields further support the flexibility and modular message structure of the message 
formats. Each generic field is a [[BASIC]] group of business data that is common throughout all messages, such as 
date and amount. 
At a minimum, each field is composed of an identifying tag and its associated field data. A tag may be thought 
of simply as a two-digit number that represents the type of data contained in the field followed by an optional 
alpha character that provides format information associated with the field contents. For example, 98A is the 
generic tag used to indicate a date field in a particular format (YYYYMMDD).
1 The format for a tag includes two 
delimiters-one to indicate the start of the tag, and a second to indicate the end of the tag. These delimiters are 
indicated using a colon. Continuing with the example above, the proper format for the generic tag used to 
indicate a date in the YYYYMMDD format would be “:98A:”. 
Because there are a number of different types of dates that may be associated with any given trade, the 
generic field tag must be further described if it is to be useful. Qualifiers are used to provide this additional 
level of description. For example, the tag “:98A:” followed by the qualifier SETT means that the corresponding 
field data is the [[settlement]] date for the trade. The tag “:98A:” followed by the qualifier TRAD means the 
corresponding field data is the trade date for the trade. Qualifiers for generic tags are always preceded by a 
colon “:”. 
The generic field for a [[settlement]] date of December 28, 2000 in the YYYYMMDD format, including the generic 
tag, the qualifier and the field data would be: 
:98A::SETT//20001228 
 
1 Note that for each field, there may be several format options for expressing the data. The alpha character in the tag is used to indicate which format [[Option]] 
has been applied. If the alpha character in the tag is lowercase in the SWIFT documentation, this means that there are several format options for the field and 
that there is free choice to use any of these options. If the alpha character in the tag is uppercase, this means that, while there are several format options for 
the field, the [[Option]] designated by the uppercase alpha character must be used. For example, 98A refers to a date in the YYYYMMDD format. 98C refers to a 
date that also includes the time. Note that MBSD has mandated the options that Participants must use in the layouts. 

---

## Page 13

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 13 
Note: 
Although tags are numeric, they generally [[DO]] not need to be placed in sequence, except if there is a sequence dependency 
as part of the format. Tags that are part of a block must remain within the "start" and "end" block tags.  
2.2.4 Tag and Field Format Illustrations and Chart 
The illustration below shows the format for a generic field tag (e.g., “:98A:”) and its associated field data. The 
illustrations are followed by charts providing the definitions of the elements delineated in the illustrations: 
 
Field Tag Components  Format Definition 
Delimiter 1 : Shows the start of the field tag. 
Field Type  2!n 2-digit number representing the data type. Note that “!” indicates a fixed 
field size. 
Field Format  1!a The format o f the contents of the data field. 
Delimiter 2 : Shows the end of the field tag.  
Example-Field Tag  :98A: “98” denotes Generic Date Field. “A” denotes date 8!n (YYYYMMDD) 
format. 
 
Field Components  Format Definition 
Generic Field Marker  : Identifies the field as generic.  
Qualifier  4!c Provides the business significance of the data. M andatory.  
Delimiter 1 / Mandatory delimiter.  
Optional [[issuer]] Code  [8c] When SWIFT defined codes are not used, allows for the use of market, or 
[[issuer]], codes with a maximum of 8 characters (e.g., GSCC).  
Delimiter 2 / Mandatory delimiter.  
Data Field  34x Data for the field. The format is specified by the letter [[Option]] of the field 
format (e.g., 98A specifies a date format of 8!n = YYYYMMDD).  


---

## Page 14

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 14 
Field Components  Format Definition 
Example-Tag/Qualifier/Data 
Field  
:98A::SETT/
/20001228 
The colon preceding the qualifier “SETT” indicates that this is a generic 
field. “:SETT//” with the tag “:98A:”denotes that this field is a [[settlement]] 
Date in the YYYYMMDD format.  
2.2.5 Illustration of Message Structure 
The figure below illustrates the [[BASIC]] SWIFT Message structure. For generic structural diagrams of the MT515, 
MT509, and MT518 messages (as specified by SWIFT), refer to Appendix E of this document. 
 
2.2.6 Non-ISO 15022 Formats 
It should also be noted that, where necessary, SWIFT formats, which are not ISO 15022 compliant, may also 
be used to support the interactive interfaces for RTTM. The MT599 Free Form (General Administrative 
Message) uses one of these ‘older’ formats. 
As indicated later in the document, these messages: 
• [[DO]] not contain beginning and end of block tags (16R and 16S); 
• [[DO]] not always have tags which include the optional 1-character format suffix; 
• [[DO]] not contain generic fields, qualifiers, or repeating sequences. 


---

## Page 15

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 15 
2.3 MT515 Message Overview 
The SWIFT MT515 is specified as a Client Confirmation of Purchase or Sale. The MT515 message will be 
used by MBSD Participants to submit Trade Create transactions to RTTM, to enter transaction and trade 
cancellations, and to support modifications (such as [[participant]] X-ref and [[Broker]] Reference Numbers) to 
previously submitted transactions and trades. The MT515 will also support the submission of DK’s. Field 22F 
PROC in the Confirmation Details (CONFDET) block will enable the [[participant]] to indicate to RTTM the type of 
MT515 record being sent. How this field is populated for each record type is detailed below. 
Note: 
The scope of this document is limited to Interactive Messaging,  therefore, screen functions are not described. Sample 
message flows, however, have been included in this document to show messages resulting from terminal -based input (refer 
to Appendix B ). 
 
The MT515 format will support the following message types: 
1. Instruct Message (:22F::PROC/GSCC/INST): The Instruct Message will be used by Brokers and Dealers 
to submit trade details to RTTM for buy/sell trades executed by Participants. This message will support: 1) 
all fields required to effect trade matching and comparison; and 2) certain other SWIFT and RTTM 
mandatory and optional fields. It should be noted that MT515s only support two-party trades. Brokers will, 
therefore, be required to submit two MT515 Instruct Records for each two-sided transaction executed. 
(These submissions will be balanced in RTTM.) 
 
2. Cancel Message (:22F::PROC/GSCC/CANC): The Cancel Message will be used to initiate the 
cancellation of a previously submitted Trade Create, either matched or unmatched. A Cancel Message 
should be an exact copy of an Instruct Message, and as such should contain full trade details. For a 
Cancel of a matched trade to be effected, Cancel Messages must be submitted by both parties. Cancel 
records for brokered trades submitted by Dealers can be submitted against the original [[Broker]] or Give-Up 
Dealer. Cancels submitted by Brokers can only target one MT515 previously submitted, and therefore can 
only be used by the [[Broker]] prior to balancing [[Broker]] records. 
 
3. Cancel Set Message (:22F::PROC/GSCC/CASE): The Cancel Set Message will be used by Brokers to 
initiate the cancellation of a set of previously submitted records associated with a specific [[Broker]] 
Reference Number. Therefore, once two [[Broker]] submissions have been balanced, the [[Broker]] must 
submit a ‘Cancel Set’ record to effect a cancellation of either a transaction or a trade. The Cancel Set 
Message will always be submitted with a Buy/Sell Indicator set to “Buy” (:22H::BUSE//BUYI). 
 
4. Modify Message (Includes [[Broker]] Change) (:22F::PROC/GSCC/MDFC): The Modify Message will be 
used by a Dealer to modify or assign an x-ref to a previously matched trade. Brokers will also use this 
message to change the [[Broker]] Reference Number of an unbalanced submission. It will also be used by 
the [[Broker]] to effect the change of the commission and/or the contraparty on the unmatched side of a 
PMAT trade. In order to modify trade information other than x-ref, [[Broker]] Reference Number, commission 
or contraparty, the trade must be canceled and resubmitted by all parties. 
 

---

## Page 16

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 16 
5. Modify Set Message (:22F::PROC/GSCC/MDSE): The Modify Set Message will be used by Brokers to 
change the [[Broker]] Reference Number of a previously balanced set (i.e., to change the [[Broker]] Reference 
Number on both the buy and sell sides comprising a transaction/trade). Note that in order to change the 
commission or the contraparty on the unmatched buy or sell sides of a trade, the [[Broker]] must submit a 
Modify, rather than a Modify Set Message, to change the desired side separately. The Modify Set 
Message will always be submitted with a Buy/Sell Indicator set to “Buy” (:22H::BUSE//BUYI). 
 
6. DK Message (:22F::PROC/GSCC/TDDK): The DK (‘Don’t Know’) Message will be submitted by either the 
[[Broker]] or the Dealer to advise its contraparty that it does not know the Trade Create or Cancel submitted 
against it. A DK status on a record does not preclude the trade from being subsequently matched or 
canceled on RTTM. Additional action will need to be taken by either the original submitter or the DKing 
party to either compare or remove the Trade Create or Cancel record. 
 
7. DNA Message (:22F::PROC/GSCC/DNAL): The DNA (‘[[DO]] Not Allocate’) Message will be used by 
Dealers to identify offsetting positions to pair-off and exclude from the allocation process. Dealers may 
identify these pair-off positions in one of two methods; 1) identify positions by “terms” and let [[FICC]] select 
specific trades to DNA with matching criteria that satisfy the validation rules, or 2) identify specific trades 
to target by providing terms along with RTTM generated Trade Ids. 
 
8. Cancel DNA Message (:22F::PROC/GSCC/CDNA): The Cancel DNA Message will be used to reopen 
position previously withheld from allocation due to a DNA request. This is allowed as long as the DNA has 
not been settled. 
 
Participants using Interactive Messaging will submit data to RTTM in real-time as trades occur, and immediate 
notification regarding a transaction or trade status will be generated via the MT509. 
2.4 MT509 Message Overview 
The SWIFT MT509 Message is specified as a Trade Status Message. It will be used by RTTM to convey the 
status of each input message submitted to RTTM for processing. The MT509 message does not contain full 
trade details, but rather provides the trade status along with relevant reference numbers to enable the 
[[participant]] to identify the trade (i.e., Trade or Transaction Number, [[participant]] External Reference Number, 
[[Broker]] Reference Number, and DNA Identifier, as appropriate). Certain status messages also include 
additional fields, such as reason codes for reject messages, etc. Field 25D in the Status (STAT) Block will 
indicate to the recipient the type of message being sent. In the event that the MT509 indicates that an MT515 
is being rejected (25D::IPRC//REJT or CPRC//REJT), the recipient must look in field 70D in the reason (REAS) 
block to de termine if the record rejected is a DK, Modify, Modify Set or Cancel Set. The qualifiers for these 
fields are shown for each example below. 
A SWIFT MT509 message will be generated for each of the following trade statuses: 
1. Trade Create Accepted (:25D::IPRC//PACK): This status message will be sent to the trade submitter to 
acknowledge that its transaction has been validated and is awaiting further processing within RTTM. It 
should be noted that this record will provide a Transaction [[ID]] for Dealer submissions, and a Submission 
[[ID]] for [[Broker]] submissions (reflected in :20C::LIST// in the LINK subsequence of the GENL block). It 

---

## Page 17

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 17 
should be noted that until the [[Broker]] submission is completed/balanced, no Transaction [[ID]] will be 
assigned, nor will a match to the contra-side be attempted. Please refer to Appendix C for a description of 
the use of reference numbers in messages. 
 
2. Trade Create Rejected (:25D::IPRC//REJT): This status message will be sent to the transaction submitter 
to indicate that its Trade Create record has been rejected as part of the validation process. The reason for 
the rejection will also be indicated on the message. (:24B::REJT in the Reason (REAS) Block). This 
message will also be used whenever an MT515 has been rejected because the message was non-SWIFT 
compliant. 
 
3. Modify Accepted (:25D::IPRC/GSCC/MODA): This status message will be sent to the submitter of a 
Modify record to acknowledge that the Modify Message has been validated and is awaiting further 
processing within RTTM. 
 
4. Modify Rejected (:25D::IPRC//REJT and :70D::REAS//GSCC/MDRJ): This status message will be sent to 
the submitter of a Trade Modify to indicate that the Modify Message has been rejected as part of the 
validation process. The reason for the rejection will also be indicated on the message (:24B::REJT in the 
Reason (REAS) Block). 
 
5. Modify Processed (:25D::IPRC/GSCC/MODP): This status message will be sent to the submitting party 
when a trade modification has been successfully performed within RTTM. Where appropriate, the 
contraparty will receive an MT518 reflecting new trade details. 
 
6. Modify Set Accepted (:25D::IPRC/GSCC/PAMS): This status message will be sent to the [[Broker]] 
submitter of a Modify Set Message to acknowledge that the message has been validated and is awaiting 
further processing within RTTM. 
 
7. Modify Set Rejected (:25D::IPRC//REJT and :70D::REAS//GSCC/MSRJ): This status message will be 
sent to the [[Broker]] submitter of a Modify Set Message to indicate that the message has been rejected by 
the application as part of the validation process. The reason for the rejection will also be indicated on the 
message (:24B::REJT in the Reason (REAS) block). 
 
8. Modify Set Processed (:25D::IPRC/GSCC/YPPR): This status message will be sent to the [[Broker]] 
submitter of a Modify Set Message to indicate when a set of records associated with a given [[Broker]] 
Reference Number has been modified (e.g., both the buy and sell sides of a [[Broker]] transaction or trade 
have been modified). 
 
9. DK Accepted (:25D::IPRC/GSCC/PADK): This status message will be sent to the submitter of a DK 
Message to acknowledge that the message has been validated and is awaiting further processing within 
RTTM. 
 
10. DK Rejected (:25D::IPRC//REJT and :70D::REAS//GSCC/DKRJ): This status message will be sent to the 
submitter of a DK Message to indicate that the message has been rejected as part of the validation 
process. The reason for the rejection will also be indicated on the message (:24B::REJT in the Reason 

---

## Page 18

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 18 
(REAS) block). 
 
11. DK Processed (:25D::IPRC/GSCC/DPPR): This status message will be sent to the submitter of a DK 
Message to indicate that the DK has been processed within RTTM. The contraparty will receive an MT518 
DK Advice Message indicating that a DK has been submitted against it for a previously submitted Trade 
Create or (post comparison) Cancel record. 
 
12. Deleted Uncompared Transaction (:25D::IPRC/GSCC/DELE): This status message will be sent to the 
submitting party indicating that an uncompared transaction has been deleted from RTTM (where the 
deletion is not the result of a Cancel Message). The contraparty will also receive an MT518 indicating that 
the advisory has been deleted (Comparison Request Cancel). 
 
13. Trade Create Unbalanced (:25D::IPRC/GSCC/TUNB): This status message will be sent (to the [[Broker]]) 
upon acceptance of a [[Broker]] submission indicating that, until further notice, a balanced set of buy and sell 
Trade Create Messages for a specific transaction (as identified by the [[Broker]] Reference Number) has not 
been created. No further processing will be performed on unbalanced [[Broker]] transactions until RTTM 
receives one corresponding buy or sell transaction to complete the balanced set. (No trade 
matching/comparison will be attempted until the transaction is balanced.) Only one buy and one sell 
record can be submitted with a given [[Broker]] Reference Number for that set to be available for balancing. 
 
14. Trade Create Balanced (:25D::IPRC/GSCC/TBAL): This status message will be sent to the [[Broker]] 
submitter indicating that RTTM has received a balanced set of buy and sell Trade Create Messages for a 
specific transaction (as identified by the [[Broker]] Reference Number). This record will communicate the 
RTTM system-generated Transaction Reference to the [[Broker]] [[participant]] and is intended to indicate that 
the [[Broker]] transaction is now available for matching. 
This message will be followed by a MT518 DNA Assigned message, providing details on the specific 
trades targeted in the DNA. 
 
15. DNA Accepted (:25D::IPRC/GSCC/DNAL): This status message will be sent to the submitter indicating 
that the DNA request is accepted and associated position marked as DNA and withheld from the 
allocation process. This message will be followed by a MT518 DNA Assigned message, providing details 
on the specific trades targeted in the DNA. 
 
16. Cancel Accepted (:25D::CPRC//PACK): This status message will be sent to the submitter of a Cancel 
Record to acknowledge that the message has been validated and is awaiting further processing within 
RTTM. If  the trade was previously compared, the Cancel Request will be pending until a corresponding 
Cancel Message is sent to RTTM by the trade contraparty. 
 
17. Cancel Rejected (:25D::CPRC//REJT): This status message will be sent to the submitter of a Cancel 
Record to indicate that the message has been rejected by the RTTM application as part of the validation 
process. The reason for the rejection will also be indicated on the message (:24B::REJT in the Reason 
(REAS) Block). ( 

---

## Page 19

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 19 
Note:  
Where a Cancel MT515 cannot be read by  RTTM and is not SWIFT compliant, RTTM will not generate a Cancel 
Rejected Record. A Trade Create Rejected message will be generated in this instance with the reason code 
indicating the MT515 message was not SWIFT compliant.)  
18. Cancel Processed (:25D::CPRC//CAND): This status message will be sent to all trade parties when a 
transaction or trade is successfully canceled within RTTM. 
 
19. Cancel Set Accepted (:25D::CPRC/GSCC/PACS): This status message will be sent to the [[Broker]] 
submitter of a Cancel Set Message to acknowledge that the message has been validated and is awaiting 
further processing within RTTM. If the trade is partially matched (PMAT), the Cancel will be pending until a 
corresponding Cancel Message is sent to RTTM by the contraparty of the matched side of the trade. 
 
20. Cancel Set Rejected (:25D::CPRC//REJT and :70D::REAS//GSCC/CSRJ): This status message will be 
sent to the [[Broker]] submitter of a Cancel Set Message to indicate that the message has been rejected by 
the RTTM application as part of the validation process. The reason for the rejection will also be indicated 
on the message (:24B::REJT in the Reason (REAS) block). (As with the Cancel Rejected Message, 
should the incoming MT515 message not be readable, RTTM will generate a Trade Input Rejected MT509 
Message indicating that the record was not processed because it was not SWIFT compliant.) 
 
21. Cancel Set Processed (:25D::CPRC/GSCC/XPPR): This status message will be sent to the [[Broker]] 
submitter of a Cancel Set Message to indicate when a set of records associated with a given [[Broker]] 
Reference Number has been successfully canceled by RTTM. 
 
22. Cancel Lifted by [[participant]] (:25D::CPRC/GSCC/UPBP): This status message will be sent to a 
[[participant]] when a Cancel Record it previously submitted has been removed/lifted from the RTTM system 
due to an action it performed. (e.g., the [[participant]] has removed its Cancel from the system). 
 
23. Cancel Lifted by RTTM (:25D::CPRC/GSCC/UPBR): This status message will be sent to the [[participant]] 
when a Cancel Record it previously submitted has been removed/lifted from the system due to an action 
performed by RTTM. (For Future Use.) 
 
24. Cancel Lifted by Contra (:25D::CPRC/GSCC/UPBC): This status message will be sent advising the 
Cancel submitter that its previously entered Cancel Message has been removed/lifted due to an action by 
its contraparty. (For Future Use.) 
 
25. Cancel Set Lifted by [[participant]] (:25D::CPRC/GSCC/VPBP): This status message will be sent to the 
[[Broker]] submitter of a Cancel Set Message to indicate that the Cancel Set record has been removed/lifted 
from the system due to an action it performed. 
 
26. Cancel Set Lifted by RTTM (:25D::CPRC/GSCC/VPBR): This status message will be sent to the [[Broker]] 
submitter of a Cancel Set Record indicating that the Cancel Set Message has been removed due to action 
by RTTM. 
 

---

## Page 20

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 20 
27. Cancel Set Lifted by Contra (:25D::CPRC/GSCC/VPBC): This status message will be sent to the [[Broker]] 
submitter of a Cancel Set Record when the Cancel Set record has been removed from the system due to 
contra action. (For Future Use.) 
 
28. Cancel DNA Accepted and Processed (:25D::CPRC/GSCC/CDNA): This status message will be sent to 
the submitter when DNA Cancel request was successfully processed. 
 
29. Trade Create Matched (:25D::MTCH//MACH): This status message will be sent to all trade parties when 
a submitted Trade Create transaction has been compared. 
 
30. Trade Partially Matched-Long (:25D::MTCH/GSCC/MAPL): This status message will always be sent to 
the [[Broker]] submitter indicating that the [[Broker]]’s (buy, or long ) Trade Create Message has been matched 
to the selling Dealer’s corresponding Trade Create Message. 
 
31. Trade Partially Matched-Short (:25D::MTCH/GSCC/MAPS): This status message will always be sent to 
the [[Broker]] submitter indicating that the [[Broker]]’s (sell, or short) Trade Create Message has been matched 
to the buying Dealer’s corresponding Trade Create Message. 
 
32. Trade Fully Matched (:25D::MTCH/GSCC/MAFM): This status message will always be sent to the [[Broker]] 
submitter indicating that the [[Broker]]’s Transaction has been matched to both the buying and selling 
Dealers’ Trade Create Messages. 
2.5 MT518 Message Overview 
The SWIFT MT518 Message is specified as a Market Side [[securities]] Trade Confirmation. It will be used to 
convey full trade information to the transaction contraparty associated with Instruct, Cancel and Modify input 
messages submitted against it. This message will also be used to provide DK information, and information to 
the submitting party when changes are made to RTTM via terminal input. As in the MT515, field 22F PROC in 
the Confirmation Details (CONFDET) block will indicate to the [[participant]] the record type being sent. 
SWIFT MT518 Messages will include the following types: 
1. Comparison Request (:22F::PROC/GSCC/CMPR): This message will always be sent to inform a 
[[participant]] that a Trade Create Message has been submitted against it. In order to effect matching, the 
[[participant]] must submit a corresponding Trade Create Message to RTTM matching (if they have not 
already done so). 
 
2. Comparison Request Modify (:22F::PROC/GSCC/CRQM):This message will inform a [[participant]] that a 
Modify Message has been submitted by its contraparty for a transaction that is pending 
matching/comparison. It will also be sent to the party that has submitted a DK against a Trade Create to 
enable monitoring of all comparison requests that it has DKed. In order to effect matching, the [[participant]] 
must submit corresponding trade data to MBSD for matching, if they have not already done so. 
 
3. Comparison Request Cancel (:22F::PROC/GSCC/CADV): This message will inform a [[participant]] that its 
contraparty or RTTM has canceled an advice of a transaction that has not yet compared. The request for 

---

## Page 21

MBSD RTTM® [[Novation]] :  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 21 
comparison has been canceled; the [[participant]] does not need to submit anything to RTTM. 
 
4. Cancel Request (:22F::PROC/GSCC/CREQ): This message will inform a [[participant]] that its contraparty 
has submitted a Cancel Message for a trade that was previously matched. In order to cancel the trade, the 
[[participant]] must submit a corresponding Cancel Message to RTTM. 
 
5. Cancel Request Modify (:22F::PROC/GSCC/MCRQ): This message will be sent to the submitter of a DK 
targeting a Cancel Request to enable monitoring of all Cancel Requests that it has DKed. 
 
6. Cancel Request Cancel (:22F::PROC/GSCC/CCRQ)-This message will be sent to the contraparty of the 
submitter of a Cancel message notifying it that the Cancel Request has been removed. (The recipient no 
longer is requested to submit a Cancel Message for this trade.) 
 
7. DK Advice (:22F::PROC/GSCC/NAFI): This message will inform a [[participant]] that its contraparty has 
submitted a DK Message targeting either a Trade Create or a Cancel record previously submitted by the 
[[participant]]. 
 
8. DK Remove Advice (:22F::PROC/GSCC/DCCX): This message will inform a [[participant]] that its 
contraparty has removed a DK from a Trade Create or Cancel that the [[participant]] has previously 
submitted. 
 
9. Screen Input Trade Replay (:22F::PROC/GSCC/SITR): This message will provide full trade details to the 
[[participant]] if a transaction or trade has been added, modified, or canceled via screen input rather than an 
automated interface. Using this message, a [[participant]] can ensure that the same transaction events exist 
within its application. One Screen Input Trade Replay message will be generated for each side of a 
transaction when a [[Broker]] inputs a (two-sided, three party) transaction directly to the RTTM system via 
Terminal Service. It will also be sent to the [[Broker]] when RTTM converts the Unmatched side of a PMAT 
SBOD trade to TFTD. 
 
10. Screen Input Set Replay (:22F::PROC/GSCC/SISR): This message will provide full details to the [[Broker]] 
if a ‘trade set’ associated with a specific [[Broker]] Reference Number has been modified or canceled via 
screen input rather than an automated interface. A single record will include the details of the full set 
which are common to both (buy and sell) sides of the trade. Using this message, a [[Broker]] can ensure that 
the same transaction events exist within its application. This message will not be used, however, when a 
[[Broker]] inputs a (two-sided) Trade Create transaction to the RTTM system via the terminal. It will only be 
used for terminal based input of Modify Set and Cancel Set transactions. 
 
11. Post Comparison Modification Advice (:22F::PROC/GSCC/MDAD): This message, where appropriate, 
will provide full trade details for all modifications that have been made to a [[participant]]'s trade after 
matching (e.g., in the event where a SBOD PMAT trade is converted to TFTD on netting day). 
 
12. DNA Assigned (:22F::PROC/GSCC/DNAP): This message will inform the [[participant]] that the previously 
accepted DNA has been assigned to individual trades based on terms or specific trades, as submitted on 
the MT515 DNA Request. 
 

---

## Page 22

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 22 
13. Screen Input DNA Replay (:22F::PROC/GSCC/SDNA): This message will provide full details to the 
[[participant]] of a [[DO]] Not Allocate (DNA) request has been added or canceled via screen input rather than 
an automated interface, providing details on the DNA including individual trades the request was assigned 
to. Using this message, a [[participant]] can ensure that the same transaction events exist within its 
application. 
 
14. [[Novation]] Advice (:22F::PROC/GSCC/NOVT): This message will inform the Dealers that their submitted 
and compared trade has been novated and [[FICC]] is now counterparty to the trade. In o ther words, [[FICC]]'s 
[[Novation]] account will become the [[Buyer]] to every [[Seller]] and the [[Seller]] to every [[Buyer]]. 
2.6 MT599 Message Overview 
The MT599 is a free-format SWIFT message which RTTM is utilizing to communicate administrative 
information to Participants. For the first phase of RTTM, this message type will only be used to notify 
Participants regarding system events, such as start and end-of-day processing. All MT599 messages will 
provide the [[participant]] with the message preparation date and time, and the date for the business day in 
question. All MT599 end-of-day messages (/EDCS/ and /EODC/) will provide the [[participant]] with the next 
RTTM valid trade submission date. 
1. Start-of-day (/GSOD/): One start-of-day message will be sent out for each business day, when the RTTM 
system is open for comparison submission. This start-of-day message will signal to Participants that the 
RTTM system is available for submission of transactions to be included in that day’s matching process. 
 
2. AM Pass Submission Cutoff (/APSC/): This message will be generated each business day to signal 
Participants that any transaction submitted after this point will not be included in the clearing system AM 
pass. On Netting days, submissions that were received by RTTM after this point, which were due to net 
that day, will be rejected by RTTM. 
 
3. Start of Pool Conversion, DNA [[settlement]] and TBA Reprice (/SDNR): This message will notify 
members that the daily Pool Conversion process has started and, for SIFMA 24hr day, the DNA 
[[settlement]] and TBA Reprice Process has begun. Cancel of compared SPT trades and DNA submissions 
with CSD of next business day are no longer accepted and will be rejected by RTTM. 
 
4. End of DNA [[settlement]] and TBA Reprice (/EDNR): This message will notify members that Pool 
Conversion, DNA [[settlement]] and TBA Reprice Process has completed. 
 
5. End-of-day Matching Submission Cutoff (/EDCS/): This first end-of-day message will indicate to 
Participants that RTTM will not accept any more transaction submissions for inclusion in that day’s 
matching process. Any transactions submitted after this point will be held and included in the next 
business day’s matching process. No acknowledgements or rejections will be sent to Participants for 
these trades until the system is next available (after the next ‘/GSOD/’ start-of-day message is sent by 
RTTM). 
 

---

## Page 23

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 23 
6. End-of-day Interactive Output Completed (/EODC/): This second end-of-day message will indicate to 
Participants that the RTTM system has completed matching processing, and that no more interactive 
comparison messages will be sent by the system for that business day. 
2.7 [[BASIC]] Message Flow 
As shown in the preceding individual message sections, four SWIFT message types will be used to convey all 
transaction/trade and administrative information between RTTM and Participants. The number and complexity 
of messages exchanged will, of course, be based on transaction type (dealer/dealer vs. brokered trades) and 
whether or not additional action is taken by either trade party once a transaction has been submitted (for 
example, if a trade is modified, canceled or DKed). For illustrative purposes, the most [[BASIC]] message flow is 
depicted below, that of a typical dealer/dealer trade submitted bilaterally for matching: 
 
Each input and output message associated with this [[BASIC]] flow is described briefly below. 
1. MT515 Instruct: This input message conveys the transaction data submitted by Dealer A for matching within 
RTTM. 
 


---

## Page 24

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 24 
2a. MT509 Trade Create Accepted: This output message is sent to Dealer A acknowledging that its Trade 
Create has been accepted by RTTM and is awaiting further processing. This message also provides the 
Transaction [[ID]] assigned by RTTM to the transaction. 
 
2b. MT518 Comparison Request: Once Dealer A’s input is accepted by RTTM, this output message is sent to 
the transaction contraparty, Dealer B, containing full trade details as entered by Dealer A. This message 
instructs Dealer B that a transaction has been submitted against it for which Dealer B must submit a 
corresponding MT515 Instruct to effect a match. 
 
3. MT515 Instruct: This input message conveys the transaction data submitted by Dealer B for matching within 
RTTM. 
 
4a. MT509 Trade Create Accepted: This output message is sent to Dealer B acknowledging that its Trade 
Create has been accepted by RTTM and is awaiting further processing. This message also provides the 
Transaction [[ID]] assigned by RTTM to the transaction. 
 
4b. MT518 Comparison Request: Once Dealer B’s input is accepted by RTTM, this output message is sent to 
the transaction contraparty, Dealer A, containing full trade details as entered by Dealer B. This message 
instructs Dealer A that a transaction has been submitted against it for which Dealer A must submit a 
corresponding MT515 Instruct to effect a match. 
 
5a. MT509 Trade Create Matched: This output message is sent to Dealer A informing it that the data submitted 
on its MT515 Instruct message has been matched to the data submitted on Dealer B’s MT515 Instruct 
message, and the trade is compared. 
 
5b. MT509 Trade Create Matched: This output message is sent to Dealer B informing it that the data submitted 
on its MT515 Instruct message has been matched to the data submitted on Dealer A’s MT515 Instruct 
message, and the trade is compared. 
 
5c. MT518 Comparison Request Cancel (due to match): This output message is sent to Dealer A to cancel the 
MT518 Comparison Request message previously sent (4b), since the trade is now matched and compared. 
This message also contains the Trade [[ID]] assigned to the contraparty’s trade upon matching. 
 
5d. MT518 Comparison Request Cancel (due to match): This output message is sent to Dealer B to cancel the 
MT518 Comparison Request message previously sent (2b), since the trade is now matched and compared. 
This message also contains the Trade [[ID]] assigned to the contraparty’s trade upon matching. 
 
This simple illustration shows much of the logic used by RTTM in processing interactive messages. For each 
MT515 submitted by a [[participant]] conveying information to RTTM, an MT509 message is generated indicating 

---

## Page 25

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 25 
that the information has been accepted or rejected. In the example above, when Dealer A and Dealer B submit 
MT515 Instruct Messages, each receives an MT509 Trade Create Accepted Message. This [[BASIC]] logic, of 
each input being acknowledged as either accepted or rejected, carries throughout all messaging. For example, 
the submission of an MT515 Cancel results in the generation of an MT509 Cancel Accepted or Rejected 
Message, the submission of an MT515 Modify results in the generation of an MT509 Modify Accepted or 
Rejected Message, etc. 
Another generally applied rule of Interactive Messaging is that each time a [[participant]] submits a record 
(MT515), its contraparty will receive a notification (MT518). In the example above, the submission of the 
MT515 Instruct Message by Dealer A resulted in the generation of an MT518 Comparison Request Message 
for Dealer B. Again, this [[BASIC]] logic carries throughout all messaging. 
Finally, any Request Messages generated by RTTM (e.g., MT518 Comparison Requests) will be subsequently 
canceled by RTTM if the Request is no longer valid. In the example above, once the trade is matched and 
compared, Dealer A and Dealer B each receive an MT518 Comparison Request Cancel, effectively nullifying 
the previously generated MT518 Comparison Requests, as the trade is now matched and no further input is 
required. 
As noted above, this simple dealer/dealer flow has been included in the body of this document to impart a 
general understanding of how interactive RTTM messages will be generated. Because of the messaging 
complexities introduced when transactions are executed via Brokers and/or when additional action is taken on 
a transaction after it has been submitted, a comprehensive set of detailed message flows for various 
processing scenarios is provided in Appendix B
 of this document. In addition, special processing features 
associated with certain Dealer flows, brokered transactions and cancel processing are highlighted in the 
following sections. Information regarding how reference numbers are used in conjunction with Interactive 
Messaging and a table of significant data changes from existing formats are also provided. 
2.8 Dealer Flow Supplemental Information 
2.8.1 Matching versus Brokers-Splits and Splices 
RTTM will first attempt to compare a Dealer trade based on all trade terms matching exactly, involving a single 
buy and sell trade. 
If an exact match is not found and the trade is a brokered trade, RTTM will then apply the Net Position Match 
logic which involves multiple trades and requires the total net par of a set of trades with the same terms to 
match. In order to achieve Net Position Match, a process called “split/splice” is used. Once RTTM identifies a 
set of  trades that match on net position, it will “split” or “splice” the Dealer’s trades to match the [[Broker]]’s trades. 
Specifically, MBSD will cancel the Dealer trades, and create new Dealer trades that exactly match the [[Broker]]’s 
submissions. 
While Interactive Messaging provides the Dealers with MT509 Trade Matched messages and MT518 
Comparison Request Cancel (due to match) for each Dealer trade and [[Broker]] advisory involved in the 
split/splice (the same messaging returned for exact match), it does  

---

## Page 26

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 26 
not provide Dealers with messaging regarding the actual cancel or creation of involved trades. However, to 
assist members in identifying and linking trades involved in a match event versus brokers (for both split/splice 
as well as exact match), RTTM generates a unique “[[Broker]] match identifier” for each match event involving a 
[[Broker]] and returns this identifier on all associated messages - specifically the MT509 “Trade Matched”, MT518 
“Comparison Request Cancel (due to match)” and MT518 “Trade Novated” messages will reflect this identifier 
in the BASK field (tag 20C). 
2.8.2 [[Broker]] Commissions Submitted by Dealers 
Dealers have the ability to submit MT515 records with [[Broker]] commissions based on rate. 
Notes: 
The Give-up price is the deal price with the commission amount inc orporated. 
[[settlement]] price is the deal price with no commission amount included.  
For MT515s 
Pre-Comparison 
MT515’s submitted by the Dealer may reflect commission in two different manners; 
• Dealers may submit reflecting the give-up price in the Deal Price field (tag 90A), or 
• Dealers may submit commission separate from the price, by populating the Dealer Price field (tag 90A) 
with only the [[settlement]] price and including the commission amount per trade in the LOCO field (tag 19A). 
In this case, the Charges Indicator (tag 22F) must be populated with CATB//PERU. 
 
Comparison/[[Novation]] 
If the commission is reflected in the give-up price, upon comparison, RTTM will separate the price and 
commission components.  
Notes: 
This information will be returned to the Dealer in the MT518 Trade Novated message, using the Dealer Price field (tag 
90A), LOCO field (tag 19A) and Charges Indicator (tag 22F), as indicated above.  
Post-Comparison/[[Novation]] 
Any MT515 submitted by a Dealer, on a post-comparison/ [[Novation]] basis (e.g., modifications or cancels), 
containing a [[Broker]] commission, will need to reflect the price separated from the commission as indicated in 
the MT518 Trade Novated message. 
For MT518s 
Pre-Comparison 
All MT518’s based on the above-mentioned transactions submitted by the Dealer, that are generated on a pre-
comparison basis, will reflect the price and commission fields as submitted by the Dealer. 

---

## Page 27

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 27 
Comparison/[[Novation]] 
As indicated above, the MT518 Trade Novated message will reflect the separate the price and commission 
components. 
Post-Comparison/[[Novation]] 
All MT518’s generated on a post-comparison basis for Dealer submitted trades with commission will reflect the 
commission and price separately on the record. 
2.8.3 Cancel Processing Post [[Novation]] 
Prior to [[Novation]], RTTM requires that Dealer Participants submit MT515 Cancels and DKs of Cancels with the 
[[Broker]] [[ID]] reflected in the appropriate [[Buyer]] or [[Seller]] contraparty Confirming Party Block. All advisories 
mentioned above will reflect the [[Broker]] as either the [[Buyer]] or [[Seller]] contraparty. 
When [[Novation]] occurs, RTTM will notify the Dealers through a MT518 Trade Novated message, which 
provides full trade details, including the replacement of the [[Broker]] contraparty with [[FICC]]’s [[Novation]] account. 
While Dealers should reflect [[FICC]] as contraparty in any subsequent actions against this novated trade (e.g., 
cancel), RTTM will not reject a Cancel record targeting a brokered trade with an incorrect contraparty due to 
[[Novation]]. In other words, Dealers can either submit the original [[Broker]] or the [[FICC]] [[Novation]] account on the 
MT515 Cancel submitted to RTTM, as appropriate for their systems. 
Post -[[Novation]], RTTM will route the Request for Comparison Cancel, Cancel Requests (including Cancel 
Request Modifies and Cancels), DK (Cancel) Advices, and DK (Cancel) Remove Advices to the appropriate 
Dealer contraparty. 
2.8.4 [[DO]] Not Allocate 
Dealers notify RTTM of offsetting positions to pair-off and exclude from the allocation process by using the 
MT515 [[DO]] Not Allocate (DNA) message. Dealers identify these pair-off positions in one of two methods; 1) 
identify positions by “terms2” and let [[FICC]] select specific trades to DNA with matching criteria that satisfy the 
validation rules, or 2) identify specific trades to target by providing terms along with RTTM generated Trade 
Ids. 
When a DNA request is received and successfully processed, RTTM will return to Dealers a MT509 DNA 
Accepted message, indicating that position has been withheld from allocation. This message is always followed 
by an MT518 DNA Assigned message, indicating that the DNA has been assigned to individual trades. 
If the DNA request could not be processed, a MT509 DNA Rejected message is returned, providing reason 
codes for rejection.  
 
2 The terms are TBA [[CUSIP]], CSD, price and trade date. 

---

## Page 28

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 28 
2.9 [[Broker]] Input Overview 
2.9.1 Two Party MT515s 
For Interactive Messaging, Brokers will be required to submit two one-sided, two party records to RTTM, one 
where the [[Broker]] acts as [[Buyer]], the other representing the [[Broker]] sell. Each MT515 Trade Instruct record must 
contain a unique external reference number (MAST). A [[Broker]] Reference Number will also be required on 
each record submitted to give RTTM the ability to link both the buy and sell sides of the [[Broker]] Trade Create 
Transaction. This [[Broker]] Reference (BASK) is, therefore, not unique, but is, rather, unique to a pair of trades in 
the system. 
2.9.2 Balanced Sets 
It should be noted that RTTM expects one set of ‘matching’ buy and sell Trade Creates to be submitted with a 
given [[Broker]] Reference Number. Once a ‘matching’ buy and sell are received, RTTM will balance the set, and 
create a system-generated Transaction Reference Number. 
Because of this extra step, [[Broker]] processing can be viewed in three phases: 
Prebalancing: Once a [[Broker]] submits an MT515 Instruct record, if the record is accepted, it will be assigned a 
Submission [[ID]] and remain in an unbalanced state until a matching/offsetting record is received (based on 
[[Broker]] Reference Number). For example, until a sell MT515 is received by RTTM to balance a previously 
submitted buy, the record will remain in the system, unavailable for further processing. 
Precomparison: After balancing, a Transaction [[ID]] will be assigned by RTTM making the [[Broker]] submissions 
available for matching. 
Post Comparison: Once a [[Broker]] Trade Create becomes Partially Matched (PMAT), processing differs based 
on whether the trade is in PMAT or FMAT status. At this point, a Trade [[ID]] is assigned. 
As previously mentioned, upon receipt of each MT515, a [[Broker]] will receive an “acknowledgement” MT509 
record followed by another MT509 message indicating the record submitted is unbalanced (TUNB). The 
acknowledgement for receipt of a [[Broker]] record will contain a system-generated [[Broker]] Submission [[ID]], rather 
than a Transaction [[ID]]. Once two ‘matching/offsetting’ records are received by RTTM, RTTM will send a 
‘balanced’ (TBAL) MT509 message for each MT515 balanced. Once the [[Broker]] submissions are balanced, a 
‘two-sided’ three-party transaction will be available in the system for matching purposes. The ‘Balanced’ 
records will contain the system- generated Transaction [[ID]] now available for matching. 
Where RTTM has not received exactly one matching buy and sell with a given [[Broker]] Reference Number, no 
submissions will be balanced. For example, should a [[Broker]] submit two buys with [[Broker]] Reference 1, and 
then submit a sell with [[Broker]] Reference 1, none of these records will be balanced (i.e., the records will NOT 
be available for further processing in the RTTM system). The [[Broker]] will be required to cancel or modify the 
[[Broker]] Reference on the appropriate ‘buy’ record in order to create a balanced set comprised of the remaining 
buy and sell records. 

---

## Page 29

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 29 
2.10 Reference Numbers 
The following system-generated reference numbers will be used during different phases of a transaction life 
cycle 
[[participant]] 
Type 
Comparison Status  System Generated 
[[ID]] 
Assigned by RTTM  
Dealer Precomparison Transaction [[ID]]  Upon acceptance to RTTM  
 Post Comparison  Trade [[ID]] Upon Trade Creation 
[[Broker]]  Prebalancing  Submission [[ID]]  Upon acceptance to RTTM  
 Post Balancing/ 
Precomparison 
Transaction [[ID]]  Upon Balancing of Trade Creates/Transaction 
Creation  
 Post Comparison 
(PMAT and FMAT)  
Transaction [[ID]]  
or 
Upon Balancing/Transaction Creation (can be 
used when trade is PMAT)  
  Trade [[ID]] Upon Matching/Trade Creation  
 
Please see Appendix C for more detail on Reference Number Usage in RTTM Interactive Messages. 

---

## Page 30

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 30 
3. COMMUNICATIONS  
Members send messages to and receive messages from [[DTCC]] via [[DTCC]]’s Common Data Transfer System 
(CDTS). CDTS messaging uses IBM Websphere MQ to provide guaranteed delivery of messages. Members 
who are using interactive messaging specify the application/service in the destination field on the message 
header, noting that members can use existing communication channels with CDTS and specify the appropriate 
destination in the header. 

---

## Page 31

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 31 
4. MESSAGE SPECIFICATIONS 
This section contains the detailed specification for the MT515, MT509, MT518, and MT599 messages to be 
used to support Real-Time Trade Matching. 
4.1 Message Format Guidelines 
4.1.1 Formatting Rules 
The following Message and Message Field rules apply to all messages in the MBSD Interactive Message 
Specification: 
Message Rules 
1. Direction: Messages are sent either to or from RTTM. 
 
2. Variable Length: All messages can vary in length up to a maximum allowable number of characters per 
message type. 
 
3. Header: All messages begin with a standard fixed-length header. 
 
4. Terminator: All messages end with a standard terminator sequence Carriage Return/Line Feed 
( “CRLF–“). 
 
5. Message Type: Each message belongs to a specified message type. 
 
6. Message Fields: A message is composed of one or more message fields. 
 
7. Character Set: A-Z, a-z, 0-9, white space and the following punctuation ":/,-" 
 
Message Field Rules 
1. Field Tag: Each field begins with a field tag. 
 
2. Tag Format: Each tag is composed of 2 digits and an optional character (e.g., 2!c[1!a]). 
 
3. Tag Delimiter: Each tag is prefixed and suffixed by the character ":" (e.g., :23G:). 
 
4. Field Data: Field data (including qualifiers and subqualifiers) immediately follows the tag suffix delimiter. 
Generic data fields are prefixed by an additional ":" (e.g., :20C::). 
 
5. Data Format: Data conforms to format rules for a specified tag. 
 

---

## Page 32

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 32 
6. Data Elements: Field data may be divided into multiple elements or subfields. 
 
7. Qualifiers: Qualifiers within a data field provide additional format definition. If a qualifier is used, it must 
appear immediately after the tag suffix delimiter (e.g., :98A::SETT). If further data is required after the 
qualifier, and the data complies with SWIFT standards, the qualifier is delimited by the characters "//" and 
the data follows (e.g., :98A::SETT//20001228 or :20C::MAST//REF123). If the data/type is proprietary, 
rather than SWIFT defined, then an [[issuer]] code (GSCC) is included (e.g., 
:95R::BUYR/GSCC/PARTABCD). 
 
8. Field Delimiter: The field delimiter sequence is Carriage Return Line Feed , “CRLF” (ASCII Character 13, 
ASCII Character 10). This sequence immediately follows the data. 
4.1.2 Formatting Conventions 
Note: 
All layouts for the MT515, MT509 and MT518 messages (included in this Section of the document) are organized using the 
following columns of data:  
Column Heading  Description 
M/O The M/O column defines whether the field is always Mandatory , or whether it is Optional 
in the particular message according to SWIFT requirements. This column does not 
provide information as to whether the field is required or optional for RTTM. Please refer 
to the Appendix A , which provides a list of required fields for [[Broker]] and Dealer Trade 
Creates. 
Tag The Tag column defines the exact tag value that must precede the field. Tags are always 
delimited by “:” (meaning a “:” would be the character immediately before and after the 
tag-for example, “:98A:” indicates a date with a format of YYYYMMDD will follow).  
Block or Qualifier The Block or Qualifier column specifies the Block Name in the case of a start block (16R) 
or end block (16S) tag. Otherwise, it specifies the required  qualifier for the tag. e.g., 
:98A::SETT (indicates a [[settlement]] Date field).  
Subqualifier/Options  The Options column specifies the different options available for individual qualifiers for a 
tag. Each tag, qualifier and [[Option]] combination uniquely specif ies a data element. e.g., 
90A::DEAL//PRCT/ (indicates a trade price will follow with a percent/dollar price type).  
Field Description The Field Description column provides a text description of the purpose or use of a data 
field.  
Data Format  The Data Format column specifies the size and characters allowed within a data field, as 
specified by SWIFT. The Field Specifications that follow each layout indicate how each 
field should be populated for RTTM input/output. The format provided in this col umn 
reflects the data that the [[participant]]  must populate the field with ( e.g., :98A::SETT// has a 
format of YYYYMMDD). 
 
It should be reiterated that the Mandatory/Optional (M/O) Field on the layout indicates if the field is 
SWIFT mandatory or optional for the message/sequence. It does not denote, however, if the field is 
required for submission to RTTM. Participants must refer to Appendix A of this document to identify MBSD 

---

## Page 33

MBSD RTTM® [[Novation]]:  
SWIFT Interac tive Messaging Specifications  
Version C ontrol Page 33 
required fields. Those fields that are SWIFT mandatory and/or MBSD mandatory must be reflected on the 
MT515, or the message (Instruct, Modify, Modify Set, Cancel, Cancel Set or DK) will be rejected. 
The Data Format field on the layouts is intended to reflect the format of the data that Participants/MBSD must 
use to populate the field. For example, the format for the [[settlement]] Date field (:98A::SETT//20001228) is 
reflected as “YYYYMMDD.” 
As previously noted, there are not only differences in data field sizes, but field formats can also be different for 
the population of the SWIFT record. In addition, all fields on the SWIFT messages are left justified, and if the 
field has a decimal format (d), it must use a decimal comma, rather than a decimal. 
As a supplement to the layout, a detailed description of each field follows, which reflects the options, defines 
the usage and provides an example of each field. 
The following characters may appear in the Data Format Column or in any discussion of data format and 
content: 
Character Meaning Example Format Example Usage 
a Upper Case Alpha Characters  6a ABCDEF 
c Alphanumeric Characters (upper case only)  6c AB12EF 
d Decimal Number (decimal comma)  15d 2035,45 
e Space 1e (1blank space)  
n Numeric Characters  8n 19950131 
x Any Printable ASCII Symbol  20x Anytime & Anyplace  
/ The literal “/” as a separator  6a/2a AB12EF/NY 
[ ] Optional element format  [/4c] [optional data]  
[N] Optional “sign” (negative) format  [N] :92A::REPO//N5,45 
! Fixed length field  12!c ABCDEFGHIJKL 
 
All fields are, by definition, variable in length with a maximum field size specified, unless a fixed length format is 
defined by inclusion of the “!”, in which case the size specified is the fixed field size. In the case where the data 
value in the fixed length field is smaller than the field size specified, the data should be left justified with trailing 
blanks.  
Typical Message Form 
Form Example 
<PASSWORD><SENDER><MESSAGE TYPE>  
<RECEIVER><cr><lf> 
ABCDEFGH ABCD 515/000/GSCC 
MBSCTRRS 
:<BLOCK START TAG>:<BLOCK NAME><cr><lf>  :16R:GENL 
:<GENERIC TAG 1>::QUALIFIER//DATA FIELD 1 <cr><lf>  :20C::SEME//004354NY4355 

---

## Page 34

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 34 
Form Example 
:<TAG2>:DATA FIELD2<cr><lf> :23G:NEWM 
:<GENERIC TAG 3>::QUALIF/[[issuer]] CODE/DATA FIELD3<cr><lf>  :22F::TRTR/GSCC/CASH 
:<BLOCK START TAG>:<BLOCK NAME><cr><lf>  :16R:LINK 
:<GENERIC TAG 4>::QUALIFIER//DATA FIELD 3<cr><lf>  :20C::MAST//ABCD1234 
:<BLOCK END TAG>:<BLOCK NAME><cr><lf> :16S:LINK 
:<BLOCK END TAG>:<BLOCK NAME><cr><lf> :16S:GENL 
 
As can be seen from the above example, blocks are demarcated by “start” (16R) and “end” (16S) block tags, 
with an associated block name. The tags contained within provide the data associated with the purpose of the 
block. Subsequent blocks, (i.e., the confirming party block), may be repeated as necessary (i.e., to identify the 
[[Buyer]] of [[securities]], the [[Seller]] of [[securities]], etc.). 
Generic fields, as previously described in this document, are designed to serve a particular function, with a 
qualifier code specifying a specific business purpose to that function. In the preceding example, the “20C” tag 
is a generic reference number, and the “SEME” qualifier in the GENL block indicates that this is the Sender’s 
Message identifier. In the LINK subsequence, however, 20C is used to provide a Master Reference Number 
([[participant]] External Reference). Processing code can thereby be designed to be reused for creating or 
validating generic fields as the fields are reused within a message, or across messages. 
Message Header Format 
M/O Tag Block or 
Qualifier 
Options Data Format  Field Description 
M    12!c Password  
M    8!c Sender  
M    3!n/3!n/4!c  Message Type 
M    8!c Receiver  
 
The Message Type Field contained in the Message Header defines the purpose of the message. As indicated 
previously, this Message Header will be utilized on all interactive messages: MT515, MT509 and MT518. The 
password field will be blank filled on all RTTM outgoing messages (MT509 and MT518). 
4.2 MT515 Message 
This section includes the detailed specification for the MT515 message. The message type will be used by 
Participants to send instructions to RTTM. The MT515 will be used for the following record types: 
1. Instruct 
2. Cancel 

---

## Page 35

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 35 
3. Cancel Set 
4. Modify 
5. Modify Set 
6. DK 
7. DNA 
8. Cancel DNA 
 
This section is organized in the following manner: 
• Section 4.2.1: General Format 
• Section 4.2.2: Field Specifications 
• Section 4.2.3: Field Analysis 
 
Notes: 
The Field Analysis section contains an analysis of the fields that may be found on each MT515 message.  
• For each record type, a check mark will be found where it is possible for that field to appear on that record.  
• W here a check mark appears, the check mark is not  intended to indicate that a field is mandatory for a given record 
type.  
• Where there is  no check mark in a given box, that field is not applicable for the record type in question.  
4.2.1 MT515 General Format 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Format  
    Message Header   
M    Password  12!c 
M    Sender  8!c 
M    Message Type 3!n/3!n/4!c  
M    Receiver  8!c 
M :16R: GENL  Block Start  
M :20C: :SEME//  Sender’s Reference for this Msg  16x 
M :23G: NEWM  Msg Function = New or  4!c 
  CANC  Cancel   
O :98C: :PREP//  Preparation Date/Time YYYYMMDDHHMMSS 
M :22F: :TRTR/ GSCC/CASH Cash Buy/Sell Trade Indicator  4!c 
M :16R: LINK  Repeat Block Start  
O :20C: :MAST//  Master Reference Number  16x 

---

## Page 36

MBSD RTTM® [[Novation]]:  
SWIFT Interactive  Messaging Specifications  
Version C ontrol Page 36 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Format  
(External Reference)  
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PREV//  Previous Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :LIST//  RTTM Assigned Reference 16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :BASK//  [[Broker]] Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16S: GENL  Block End  
M :16R: CONFDET  Block Start  
M :98C: :TRAD//  Trade Date & Time YYYYMMDDHHMMSS 
M :98A: :SETT//  [[settlement]] Date YYYYMMDD 
M :90A: :DEAL/ /PRCT/ Deal Price–Percentage 15d 
O :19A: :SETT/ /USD [[settlement]] Amount  15d 
M :22H: :BUSE/ /BUYI Trade Type– Buy or 4!c 
   /SELL Sell  
O :22F: :PROC/ GSCC/INST Instruct (i.e., Trade Create) 
Processing Indicator or  
4!c 
   GSCC/CANC Cancel Processing Indicator or   
   GSCC/CASE Cancel Set Processing Indicator  
or 
 
   GSCC/MDFC Modify Processing Indicator or   
   GSCC/MDSE Modify Set Processing Indicator  
or 
 
   GSCC/TDDK DK Processing Indicator   
   GSCC/DNAL [[DO]] Not Allocate Indicator   
   GSCC/CDNA Cancel [[DO]] Not Allocate Indicator   
M :22H: :PAYM/ /APMT Against Payment Indicator  4!c 
O :22F: :CATB/ /PERU Per Unit Charges Indicator  4!c 

---

## Page 37

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 37 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Format  
M :16R: CONFPRTY  Repeat Block Start  
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]] 34x 
O :20C: :PROC//  Contra Transaction Reference 16x 
O :70E: :DECL/ /GSCC [[participant]] Financial Amount 
Declaration  
10*35x 
   /FAMT Individual Par amount to DNA  15d 
   /PRCT Individual Price to target for DNA  15d 
   /TDDT Individual Trade Date to target for 
DNA 
YYYYMMDD 
   /TRID Individual Trade [[ID]] to target for DNA  16x 
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative 4*35x 
   /TDID Contra Trader [[ID]] 20c 
M :16S: CONFPRTY  Repeat Block End  
M :16R: CONFPRTY  Repeat Block Start  
M :95R: :SELL/ GSCC/PART Party = [[Seller]]  34x 
O :20C: :PROC//  Contra Transaction Reference 16x 
O :70E: :DECL/ /GSCC [[participant]] Financial Amount 
Declaration  
10*35x 
   /FAMT Individual Par amount to DNA  15d 
   /PRCT Individual Price to target for DNA  15d 
   /TDDT Individual Trade Date to target for 
DNA 
YYYYMMDD 
   /TRID Individual Trade [[ID]] to target for DNA  16x 
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative 4*35x 
   /TDID Contra Trader [[ID]] 20c 
M :16S: CONFPRTY  Repeat Block End  
M :36B: :CONF/ /FAMT/ Quantity as Face Amount - 
Original Face Value(Par)  
15d 
M :35B: /US/  TBA [[CUSIP]] 9!c (4 * 35x)  
M :16R: FIA  Block Start  
O :12B: :OPTI/ /CALL [[Call option]] Type or  4!c 
   /PUTO [[Put Option]] Type   
O :98A: :EXPI//  Expiry Date YYYYMMDD 

---

## Page 38

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 38 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Format  
O :13B:  :POOL/  GSCC/ Pool Number and/or  9x (30x) 
   /ISSR/ Pool [[issuer]] or 1!c 
   CUSP/ Pool [[CUSIP]] 9!c 
M :16S: FIA  Block End  
O :70E: :TPRO/ /GSCC Trade Instruction Processing 
Narrative 
(10*35x) 
   /TDSVSBOD Trade Service Type– SBOD or 4!c 
   /TDSVTFTD Trade Service Type– Trade for Trade 
or 
 
   /TDSVSTIP Trade Service Type – STIP Trade  
for Trade or 
 
   /TDSVOPTN Trade Service Type– [[Option]]  
   /DKRS DK Reason (see table)  4!c 
   /GUPP Give Up Period  2n 
M :16S: CONFDET  Block End  
M :16R: SETDET  Block Start  
M :22F: :SETR/ /RPTO Indicator = Reporting Purposes  4!c 
O :17B: :STAN/ /N Standing Instruction Override  1!a 
M :16R: AMT  Block Start  
M :19A: :LOCO//USD  Commission Amount  15d 
M :16S: AMT  Block End  
M :16S: SETDET  Block End  
 
Subqualifier/Options  DK Reason Codes Data Format  
E004 Unknown Security  4!c 
E005 Bad Quantity   
E006 Bad Trade Date  
E007 Bad [[settlement]] Date  
E008 Bad Price  
E010 Bad [[Buyer]] Party   
E011 Bad [[Seller]] Party   
E013 Transaction Type Error   

---

## Page 39

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 39 
Subqualifier/Options  DK Reason Codes Data Format  
E015 Commission Error   
E100 Unknown Cancel   
E101 Give Up Period Error   
E102 Trade Service Type Error   
E103 [[Option]] Type Error   
E104 [[Option]] Expiry Date Error   
E106 Incorrect Account Symbol   
E107 Duplicate Trade  
E108 Invalid Pool Identifier   
E998 Trade not found  
E999 Other Bad Data  
Note: 
E101 is not used for [[Novation]] Eligible trades  
4.2.2 MT515 Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a message header.  All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password 12!c A password will be assigned by RTTM enabling the sender to submit trades on 
behalf of specific [[participant]](s).  
Sender 8!c MBSD account number of the [[participant]] sending the message.  
Message Type 3!n/3!n/4!c  The first three characters indicate to the recipient the message type (515); the 
second three positions reflect the version of the message interface (currently always 
000). The last four characters indicate the [[issuer]] code to be used in the mes sage 
(“GSCC”). 
Receiver 8!c MBSCTRRS (MBSD Trade Registration and Reconciliation System) will be the 
recipient of the MT515 messages.  
GENL This Mandatory Block provides general information regarding the message.  
It appears only once in a trade contract. 
20C Sender Message Reference 
• SEME//: This mandatory field contains the sender’s message reference number.  It is 
mandatory and must contain a unique number to unambiguously identify each message sent to 
RTTM. (This is a communications message number, not a trade number.)  It is suggested that 
Participants use a number that includes a date followed by either a time stamp or a sequence 
number. In this way uniqueness can be ensured.)  

---

## Page 40

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 40 
Block/Tag Notes 
Note: 
While the SWIFT message accommodates  both upper and lower case alphanumeric and certain 
symbols, for RTTM purposes, this field must be populated with an upper case alphanumeric value.  It 
cannot contain symbols or hyphens.  
e.g., :20C::SEME//ABCDEFG1 
23G Function of the Message 
This mandatory field identifies the function of the message.  It will either be a new message (NEWM) or 
a cancellation of a previous message (CANC):  
• NEWM: This qualifier will be used for an Instruct/Trade Create, a Modify, a Modify Set, a DK , or 
a DNA Message. 
• CANC: This qualifier will be used for a Cancel, a Cancel Set Message,  or a Cancel DNA 
Message 
e.g., :23G:NEWM 
98C Preparation Date and Time 
PREP// -This optional field contains the date and time the message sent to RTTM was prepared.  
Note: 
The “C” format for this (98) tag indicates a date/time format of “YYYYMMDDHHMMSS”. 
e.g., :98C::PREP//20011218102015 
22F Trade Transaction Type Indicator (TRTR)  
Since MBSD trades are bilateral cash (buy/sell) trades, this mandatory field should only contain at this 
time the value indicated below.  
• TRTR/GSCC/CASH: This qualifier/[[Option]] should be used on all messages to specify that they 
refer to buy/sell trades requiring two -sided comparison.  
e.g., :22F::TRTR/GSCC/CASH 
LINK The LINK Block can be repeated for the various reference qualifiers required on a trade 
contract. It is intended to provide the required information to identify the trade.  Each reference 
number must be enclosed within a Start Link Block (:16R:LINK) and End Link Block 
(:16S:LINK). Each LINK repeating subsequence is within the GENL Block.  At least one LINK 
sequence is required on the MT515 message.  
20C Reference 
The Reference Numbers provided by the [[participant]] must contain upper case alphanumeric 
characters, but not symbols or hyphens.  As indicated above, each reference number must be 
enclosed in a LINK Start and End block.  
• MAST//: Master Reference Number : This qualifier contains the [[participant]]’s External Reference 
Number, which must be unique for an Instruct record.  It is mandatory for an inbound MT515 
Instruct message.  The following table identifies what is needed for each message type:  
 For message type:  This field should be populated with the following:   

---

## Page 41

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 41 
Block/Tag Notes 
 Instruct • Dealers should populate this field with the primary 
reference number they use to track their trades on 
the RTTM system.  
• Brokers should populate this field with a unique 
reference number, which they use to identify any 
Trade Create messages until a balanced 
set/Transaction exists in the RTTM system.  
 
 
 Cancels and Modifies of 
trades, 
Cancels of DNA 
Participants should populate the MAST field with their 
current X-ref. 
 
 Cancel Set and Modify Set,  [[DO]] not populate this field.   
 DNA Participants should populate the MAST field with the X- ref 
they use to track their DNA requests on the  
RTTM system  
 
 DK Messages  • If the DK message targets a Trade Create, the 
MAST field should be populated with the value 
“NONREF". 
• If the DK message targets a Cancel Request, the 
MAST field should be populated with the X -ref. 
 
  
• PREV//: Previous Reference Number : This qualifier is used on Modify, Modify Set, Cancel and 
Cancel Set Messages.  
 For message type:  This field should be populated with the following:   
 Modify  • Dealers should populate this field with their 
previous X -ref, if relevant. 
• Brokers should not populate this field.  
 
 Modify Set • Brokers should populate this field with their 
previous [[Broker]] Reference for post comparison 
[[Broker]] ref changes.  
• This message type is not applicable to Dealers. 
 
 Cancel, Cancel Set, and 
Cancel DNA 
Populate with the value “NONREF”  
(when :23G:CANC and :22F::PROC/GSCC/CANC or 
:22F::PROC/GSCC/CASE in the Confirmation Details 
(CONFDET) block).  
 
 Instructs DK Messages,  DNA 
Requests  
[[DO]] not populate this field.   
• LIST//: RTTM Reference Number : This qualifier contains the RTTM assigned Reference 
Number. For Cancel DNA, RTTM Reference has to be DNA [[ID]]. For all other messages 
depending on the [[participant]] type and the comparison status of a transaction or a trade, the 
RTTM Reference Number can be a Submission [[ID]], a Transaction [[ID]] , or a Trade [[ID]]. This is 
illustrated in the table below:  
 [[participant]] Type Comparison Status  RTTM Reference Number   
Dealer Pre-Comparison Transaction [[ID]]  
Post-Comparison  Trade [[ID]] (Tran [[ID]])  

---

## Page 42

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 42 
Block/Tag Notes 
[[Broker]]  Pre-Balancing  Submission [[ID]]  
Post-Balancing  
Pre-Comparison 
Transaction [[ID]]  
Post-Comparison (PMAT and 
FMAT) 
Transaction [[ID]] (PMAT only) or  
Trade [[ID]] (PMAT and FMAT)  
 The RTTM Reference Number (LIST) should be used on Modify, Modify Set, Cancel, Cancel Set, 
and Cancel DNA records only –it does not apply to Instruct, DK, or  DNA records targeting a Trade 
Create. 
 For message type This field should be populated with the following:   
• Cancels  
• Modifies  
• Cancel Set 
• Modify Set 
• DK messages targeting a 
Cancel Request  
• Cancel DNA 
Participants should populate the (LIST) field with the 
RTTM Reference Number. 
Instructs, DNA and DK Messages 
targeting a Trade Create 
[[DO]] not populate this field.  
• BASK//: [[Broker]] Reference Number : This qualifier is used for [[Broker]] submitted messages only. 
All [[Broker]] submitted Instruct records must reflect the [[Broker]] Reference Number. This number will 
be used to ‘tie’ the long and short sides of a transaction together to create a balanced set. Each 
[[Broker]] Reference Number must be unique in the system for a set of buy/sell Trade Create 
records.  
Notes: 
• For more detailed information on the use of transaction- related reference numbers, see Appendix 
C. 
• Where it is supplied, the RTTM Reference Number will be used by RTTM to identify the trade or 
transaction, rather than the reference provided in the (MAST) or (BASK) field.  
• While the SWIFT message accommodates both upper and lower case alphanumeric and certain 
symbols, for MBSD purposes, this field must be populated with an upper case alphanumeric value.  
It cannot contain symbols or hyphens, except where the reference number is assigned by RTTM.  
e.g., :20C::MAST//REF010 
CONFDET The mandatory CONFDET (Confirmation Details) block appears only once in a trade contract.  It 
contains Trade and Confirming Party Details.   
98C Trade Date 
• TRAD//: This qualifier is used as indicated below.   
Message Type TRAD Field Value 
DNA Request,  Cancel DNA The field must be populated with a value of  December 31st 
9999 and a time of 00:00:00. 

---

## Page 43

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 43 
Block/Tag Notes 
All other MT515 The value must be populated with the Trade Date and 
Trade Time.  
Note: 
The “C” format for this (98) tag indicates a date/time format of “YYYYMMDDHHMMSS”.  
e.g., :98C::TRAD//20141218095510 
:98C::TRAD//99991231000000 
98A [[settlement]] Date 
• SETT//: This field is used on all messages to specify the [[settlement]] date. The “A” format for this 
tag (98) indicates a date format of “YYYYMMDD”.  
− For TFTD trades and DNA request s, this field must be populated with the full contractual 
[[settlement]] date using the format mentioned above. 
− For SBOD and OPTN trades, this field must be populated with the [[settlement]] year and 
month in question, while the day (“DD”) may be populated with “01” or with any other valid 
day for that month. RTTM will reject the message if it contains a [[settlement]] date for which 
the day part (“DD”) is left blank or if it is populated with “00” or with a day that is not valid 
for the given year and month. For SBOD and OPTN trades, the day part (“DD”) will not be 
reflected in the RTTM application– nor will it be used for comparison purposes.   
e.g., :98A::SETT//20011219 
90A Deal Price 
This field must be reflected on all MT515 messages.  The price is expressed as a decimal number in 
SWIFT Standard format, which is left justified, with commas removed, and a comma used instead of a 
decimal.  
• DEAL//PRCT/: This qualifier is used as indicated below.   
Message Type DEAL//PRCT Field Value  
DNA Request,  Cancel DNA The value must be set to “0”.  
All other MT515 The value is used for dollar prices, expressed as a decimal 
number.  
- The Dealer has the [[Option]] of submitting a Deal Price that 
includes the commission. However, on post -comparison 
MT515 messages, the Deal Price submitted by the Dealer 
must not incorporate the commission.  
- If the MT515 message is submitted by a [[Broker]], the Deal 
Price will not include any commissions.  
e.g., :90A::DEAL//PRCT/99,625 
:90A::DEAL//PRCT/0, 
19A [[settlement]] Amount  
SETT//: This optional field may be used by participants on Specified Pool Trades to submit final 
money on trades based on the factor available on their systems.  
 
The Amount is in SWIFT Standard format, which is left justified, with commas removed, and a 
comma used in lieu of a decimal.  The amount is always preceded by a 3- character ISO currency 
code (“USD” for MBSD trades).  

---

## Page 44

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 44 
Block/Tag Notes 
Message Type SETT// Field Value  
DNA Request,  Cancel DNA This qualifier is omitted.  
All other MT515 If trade is an SPT, this value contains the final money 
based on the most recent factor in members’ systems.  
For non- SPT trades, this qualifier is omitted.  
Note: 
The SWIFT format can accommodate a value of 15d in this field.  
e.g., :19A::SETT//USD1000000, 
22H Trade Type Indicator (BUSE)  
This field is required on all MT515 messages and has two allowable values for this BUSE qualifier:  
• BUSE//: This qualifier is used as indicated below  
Message Type BUSE// Field Value 
Modify Set, Cancel Set,  DNA 
Request, Cancel DNA 
The value must be set to “BUSE//BUYI”. 
All other MT515 Options are:  
• BUSE//BUYI: The trade submitted is a buy 
transaction  
• BUSE//SELL: The trade submitted is a sell 
transaction  
e.g., :22H::BUSE//BUYI 
22F Processing Indicator (PROC)  
This Processing Indicator  enables the [[participant]] to indicate to RTTM the record type/ command be ing 
submitted on an MT515 message.  
The allowable values for this field are:  
• PROC/GSCC/INST: This qualifier/[[Option]] indicates that the MT515 is an Instruct (i.e., Trade 
Create) record.  
• PROC/GSCC/CANC: This qualifier/[[Option]] indicates that the MT515 is a Cancel record.  
• PROC/GSCC/CASE: This qualifier/[[Option]] indicates that the MT515 is a Cancel Set record.  
• PROC/GSCC/MDFC: This qualifier/[[Option]] indicates that the MT515 is a Modify record.  
• PROC/GSCC/MDSE: This qualifier/[[Option]] indicates that the MT515 is a Modify Set record.  
• PROC/GSCC/TDDK: This qualifier/[[Option]] indicates that the MT515 is a DK record.  
• PROC/GSCC/DNAL: This qualifier/[[Option]] indicates that the MT515 is a DNA record  
• PROC/GSCC/CDNA: This qualifier/o ption indicates that the MT515 is a Cancel DNA  record  
e.g., :22F::PROC/GSCC/INST  
22H Payment Indicator (PAYM)  
This Payment Indicator field is mandatory for the MT515 message.  All trades submitted to RTTM must 
provide the following qualifier:  
• PAYM//APMT: This qualifier/[[Option]] indicates that the trade will settle against payment.  
e.g., :22H::PAYM//APMT 

---

## Page 45

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging S pecifications 
Version C ontrol Page 45 
Block/Tag Notes 
22F Charges Indicator (CATB)  
This indicator is mandatory on all MT515 messages that contain a commission amount in field 
:19A::LOCO//USD (Amount (AMT) subsequence within the [[settlement]] Details (SETDET) block).  This 
indicator specifies the commission rate that was applied  and has the following value:  
• CATB//PERU: This qualifier/[[Option]] indicates that the commission amount reflected on the 
message is the result of a commission rate that was applied.  
e.g., :22F::CATB//PERU  
36B Quantity of [[securities]] (CONF)  
• CONF//FAMT/: This field is mandatory, and for the purposes of RTTM, must use the [[Option]] 
‘FAMT’- indicating face amount (par).   
Message Type CONF//FAMT Field Value  
DNA Request  The value should be the SUM  value of buy par included in 
the DNA set which should be equal to SUM value of sell 
par. 
All other MT515 The value specifies the face amount, noting that for 
Specified Pool Trades, this must be populated with the 
Original Face Value of the trade.  
Note: 
This tag and the following tag must be placed on the message following the Confirming Party 
subsequences described below.  
e.g., :36B::CONF//FAMT/1000000,  
35B Identification of Security  
The mandatory qualifier specifies the security involved in this trade or DNA as identified by its TBA 
[[CUSIP]] number.  The TBA [[CUSIP]] must be identified  with the exception of Specified Pool Trades , as 
indicated below.  
• If the TBA [[CUSIP]] is known, it must be filled in by specifying the ISO country identifier (‘/US/’), 
followe d by the TBA [[CUSIP]] number.  
• If a Specified Pool Trade (SPT) in which the TBA [[CUSIP]] is not known, the value of the field 
must be populated with the value of "NONCUSIP".  
Note: 
While the SWIFT layout accommodates a format of 4 * 35x, a 9!c (alpha numeric) value should 
populate the field for the TBA [[CUSIP]].   
e.g., :35B:/US/01F070641 
70E Trade Instruction Processing Narrative (TPRO)  
This field (optional for SWIFT) will be used to support trade -related infor mation not included in the 
MT515 format. The field should not be populated for DNA and Cancel DNA messages. However, for 
all other message types, it must be populated with the trade service type, a DK reason and the give -up  
period, as appropr iate.  
TPRO//GSCC: denotes Trade Processing narrative in formation specific to MBSD. 
One Trade Service Type must be included on a message:  

---

## Page 46

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 46 
Block/Tag Notes 
• /TDSVSBOD: should be used for SBOD trades.  
• /TDSVTFTD: should be used for TFTD trades  
• /TDSVSTIP: should be used for STIP trades.  
• /TDSVOPTN: should be used for OPTN trades. 
A DK reason must be included on all inbound MT515 DK records  
• /DKRS: specifies the DK reason (on DK Messages only) –a table with DK reasons is attached 
to the layout.  
All [[Broker]] trades must reflect the give up period:  
• /GUPP: indicates the number of days (0- 9) in the give -up period.  *This field will not be used 
for [[Novation]] eligible trades .* 
Note: 
This tag must be placed on the message within the Confirmation Details (CONFDET) Block following 
the FIA subsequence described below.  
e.g., :70E::TPRO//GSCC/TDSVTFTD 
:70E::TPRO//GSCC/TDSVSTIP 
CONFPRTY The Mandatory Confirming Party Block must be repeated for each party to a trade.  Each party 
specified must be enclosed within a Start Party block (:16R:CONFPRTY) and an End Party 
block (:16S:CONFPRTY). 
Notes: 
• Modify Set and Cancel Set Messages submitted by Brokers and Cancel DNA submitted by 
Dealer will contain only one Confirming Party sequence (the [[Buyer]] Confirming Party 
sequence, which reflects information pertaining to the submitting [[Broker]] /Dealer).  
• For DNA Requests submitted by Dealers, the Confirming Party block contains information 
on the position to target and par amount to DNA; this block will be repeated for each 
buy/sell term in the request. As a DNA must have at least one buy and one sell, a 
minimum of two repeating Confirming Party blocks must appear in the message.  
• All other MT515 messages should contain two repeating Confirming Party sequences (one 
[[Buyer]] and one [[Seller]], and one of these parties will also be the su bmitter of the MT515 
message).  
95R Party 
• BUYR/GSCC/PART: specifies the Buying Party on all MT515 messages except on Cancel Set 
and Modify Set Messages , where this field always specifies the [[Broker]] or DNA Cancel 
Messages that specify the submitter of original DNA request who submits the MT515 message 
(the “GSCC” [[issuer]] code allows the specification to include the [[participant]] account [[ID]] of the 
submitter or the contra, depending on who is acting as [[Buyer]] or [[Seller]]).  
• SELL/GSCC/PART: specifies  the Selling Party on all MT515 messages except on Cancel Set, 
Modify Set and Cancel DNA  messages, where the [[Seller]] Confirming Party sequence is omitted.   
As previously noted, Brokers will always act either as [[Buyer]] or as [[Seller]] on any given MT515 message 
(with the exception of Modify Set and Cancel Set Messages, where Brokers are always reflected as 
[[Buyer]] only).  

---

## Page 47

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 47 
Block/Tag Notes 
Note: 
While the SWIFT layout supports a format of 35x for this field, the [[participant]] must populate the field 
with the appropriate 4 -character [[participant]] account [[ID]], for [[Buyer]] or [[Seller]].  
e.g., :95R::BUYR/GSCC/PARTDLRA 
20C Contra Transaction Reference (PROC)  
This field only applies to DK Messages targeting Trade Creates.  
• PROC//: The DKing party should use this field to indicate the contra’s Transaction [[ID]] on DK 
Messages targeting Trade Creates.  
e.g., :20C::PROC//7096000247 
70E [[participant]] Financial Amount Declaration (DECL)  
DECL//GSCC: denotes financial amount information related DNA Requests. For each individual DNA 
term specified, the FAMT, PRCT and TDDT must be specified. When targeting a specific trade for 
DNA, TRID contains the targeted Trade [[ID]].  
Note: 
If targeting trades via Trade [[ID]], all of the Confirming Party Blocks must have TRID; if targeting trades 
via terms onl y, none of the Confirming Party Blocks can have TRID.  
• /FAMT: the face quantity (par) to DNA.  
• /PRCT: the price of the trades to apply the DNA to, to 9 decimal places.  
• /TDDT: the trade date of the trades to apply the DNA to, in format YYYYMMDD  
• /TRID: the Trade [[ID]] of the trade to apply the DNA to.  
Notes: 
The amount fields are in SWIFT Standard Format, which is left justified, with thousands separators 
removed, and a comma used as the decimal separator  
e.g., :70E::DECL//GSCC/FAMT1000000,/PRCT101,5/TDDT20150214 
e.g., :70E::DECL//GSCC/FAMT1000000,/PRCT101,5/TDDT20150214/TRID7096000001 
70C [[participant]] Contact Narrative (PACO)  
This optional field should be used by trade submitters/Brokers/electronic trading systems to identify 
the trader [[ID]] at the counterparty Dealer that executed the trade.  
• PACO//GSCC: denotes narrative infor mation related to the [[participant]] contact specific to 
RTTM. 
• /TDID: should be used in the appropriate (counterparty) BUYR or SELL Confirming Party 
sequence to indicate the [[ID]] of the trader at the dealer contra that executed the trade.  
Note: 
While this field can support a 4 * 35x narrative, the [[participant]], at this time, should only provide data for 
the above qualifiers in this field.  In the future, this narrative field can be used to support additional 
information related to the [[Buyer]] or [[Seller]], where required.  
e.g., :70C::PACO//GSCC/TDIDTRADER456  

---

## Page 48

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Speci fications 
Version C ontrol Page 48 
Block/Tag Notes 
FIA This Optional Block is necessary for Specified Pool Trades to identify the specific pool traded.  
It is also required for OPTN trades (w here :70E::TPRO//GSCC/TDSVOPTN). 
12B [[Option]] Type (OPTI)  
• OPTI//CALL: specifies that a [[Call option]] on the underlying [[CUSIP]] was traded.  
• OPTI//PUTO: specifies that a [[Put Option]] on the underlying [[CUSIP]] was traded.  
e.g., :12B::OPTI//CALL  
98A Expiry Date (EXPI) 
• EXPI//: specifies the expiry date of the (put or call) [[Option]]. The “A” format for this tag (98) 
indicates a date format of “YYYYMMDD”. 
e.g., :98A::EXPI//20010918 
13B Number Identification  
This qualifier specifies the pool instrument (by pool [[issuer]] and number, or pool [[CUSIP]]) that is traded 
for a Specified Pool Trade (SPT). Possible qualifier/options are:  
• POOL/: This specifies the Pool identifier for the SPT trade and must be followed by either  
 
− GSCC/: Pool Number (up to 9 alphanumeric characters) and  
− ISSR/: [[issuer]] of the Pool (1 character identifier: F=FNMA, R=Freddie Mac, H=GNMAII, 
N=GNMAI) 
—OR— 
− CUSP/: Pool [[CUSIP]] (9 alphanumeric character unique pool [[CUSIP]] identifier)  
Note: 
If the TBA [[CUSIP]] is specified (in 35B above) and the [[Member]] wishes to submit a Pool Number 
(GSCC), the [[issuer]] (ISSR) is not required. However, if the TBA [[CUSIP]] is not known (35B is set to 
value “NONCUSIP”), then the [[Member]] must specify either 1) Pool [[CUSIP]] (CUSP) or 2) [[issuer]] and 
Pool Number ( GSCC and ISSR) 
e.g., :13B::POOL/GSCC/123456 
:13B::POOL/GSCC/123456/ISSR/R 
:13B::POOL/CUSP/3132GSRN1 
SETDET This Optional Block, and the AMT subsequence, is necessary only when the Commission 
Amount field is populated.  
22F [[settlement]] Indicator (SETR) 
This field is SWIFT Mandatory for the Block.  
• SETR//RPTO: Indicates that this trade confirmation is for repor ting purposes only.  
Note: 
This field is not used by RTTM although it is SWIFT mandatory in order to support the inclusion of the 
Commission Amount field.  
e.g., :22F::SETR//RPTO  
17B Standing Instructions Override  

---

## Page 49

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 49 
Block/Tag Notes 
This field is optional and, if specified, is ignored.  
• STAN//N  
Note: 
This field, previously a SWIFT mandatory field, is no longer required and will be ignored if specified.  
e.g., :17B::STAN//N 
AMT As indicated above, this Optional sequence is only necessary to support the inclusion of a 
[[Broker]] commission on a trade.  When used, this block should always be included within the 
[[settlement]] Details (SETDET) block.  
19A Commission Amount  
• LOCO//USD: This field specifies the [[Broker]]’s commission amount PER TRADE in USD that will 
be applied to that specific trade. The Commission Amount field is in SWIFT Standard Format, 
which is left justified, with commas removed, and a comm a used in lieu of a decimal.  
− If a commission rate is charged on a trade, entries for this field are as follows:  
 For all MT515 messages, the [[Broker]] must input a commission amount per trade in this 
field.  
 For Pre-comparison MT515 messages, the Dealer has the [[Option]] of inputting a 
commission amount in this field or incorporating the commission in the Deal Price.   
 Post-comparison dealer submissions (Modifies & Cancels) containing commission must 
reflect that commission in this field.  
− If a commission amount is r eflected in this field, the Confirmation Details (CONFDET) Block 
must reflect:  
 :22F::CATB//PERU 
Note: 
The value in this field is the commission amount that must be paid to the [[Broker]] –e.g., if a commission 
rate of 1/512 of a percent is charged on a two -million -dollar trade, then the Commission Amount field 
should be displayed as “LOCO//USD39,06”.  
e.g., :19A::LOCO//USD39,06 
4.2.3 MT515 Field Analysis 
M/
O 
Tag Block/ 
Qualifier  
Subqualifier / 
Options 
Field Description INST CANC CASE MDFC MDSE TDDK DNAL CDNA 
    Message Header          
M    Password         
M    Sender          
M    Message Type         
M    Receiver         
M :16R: GENL  Block Start         

---

## Page 50

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 50 
M/
O 
Tag Block/ 
Qualifier  
Subqualifier / 
Options 
Field Description INST CANC CASE MDFC MDSE TDDK DNAL CDNA 
M :20C: :SEME//  Sender’s 
Reference for this 
Msg 
        
M :23G:  NEWM  Msg Function = 
New 
or  
        
  CANC  Cancel         
O :98C: :PREP//   Preparation 
Date/Time 
        
M :22F: :TRTR/ GSCC/CASH Cash Buy/Sell 
Trade Indicator  
        
M :16R:  LINK  Repeat Block 
Start 
        
O :20C: :MAST//  Master Reference 
Number  
        
M :16S: LINK  Repeat Block 
End 
        
M :16R:  LINK  Repeat Block 
Start 
        
O :20C: :PREV//   Previous 
Reference Number 
        
M :16S: LINK  Repeat Block 
End 
        
M :16R:  LINK  Repeat Block 
Start 
        
O :20C: :LIST//  RTTM Assigned 
Ref 
        
M :16S: LINK  Repeat Block 
End 
        
M :16R:  LINK  Repeat Block 
Start 
        
O :20C: :BASK//   [[Broker]] Reference 
Number 
        
M :16S: LINK  Repeat Block 
End 
        
M :16S: GENL  Block End         
M :16R: CONFDET  Block Start         
M :98C: :TRAD//  Trade Date & Time         

---

## Page 51

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 51 
M/
O 
Tag Block/ 
Qualifier  
Subqualifier / 
Options 
Field Description INST CANC CASE MDFC MDSE TDDK DNAL CDNA 
M :98A:  :SETT//  [[settlement]] Date         
M :90A:  :DEAL/ /PRCT/ Deal Price–
Percentage 
        
O :19A:  :SETT/ /USD [[settlement]] 
Amount  
        
M :22H: :BUSE/ /BUYI  Trade Type–Buy 
or 
        
   /SELL  Sell         
O :22F: :PROC/ GSCC/INST Instruct 
Processing 
Indicator  
or 
        
   GSCC/CANC Cancel Processing 
Indicator  
or 
        
   GSCC/CASE Cancel Set 
Processing 
Indicator  
or 
        
   GSCC/MDFC Modify Processing 
Indicator  
or 
        
   GSCC/MDSE Modify Set 
Processing 
Indicator  
or 
        
   GSCC/TDDK DK Processing 
Indicator  
        
   GSCC/DNAL [[DO]] Not Allocate 
Indicator  
        
   GSCC/CDNA Cancel DNA 
Indicator  
        
M :22H: :PAYM/ /APMT Against Payment 
Indicator  
        
O :22F: :CATB/ /PERU Per Unit Charges 
Indicator  
or 
        
M :16R: CONFPRTY  Repeat Block 
Start 
        

---

## Page 52

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 52 
M/
O 
Tag Block/ 
Qualifier  
Subqualifier / 
Options 
Field Description INST CANC CASE MDFC MDSE TDDK DNAL CDNA 
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]]         
O :20C: :PROC//  Contra 
Transaction 
Reference 
        
O :70E:  :DECL/ /GSCC Financial Amount 
Declaration 
        
   /FAMT Par amount to 
DNA 
        
   /PRCT Price of the 
trade(s) to apply 
DNA to 
        
   /TDDT Trade Date of the 
trade(s) to apply 
DNA to 
        
   /TRID Trade [[ID]] of the 
trade to apply DN A 
to 
        
O :70C: :PACO/ /GSCC Narrative/ 
Additional 
Reference 
Numbers/ 
Information 
        
   /TDID Contra Trader 
[[ID]]/Trader [[ID]] 
        
M :16S: CONFPRTY  Repeat Block 
End  
        
M :16R: CONFPRTY  Repeat Block 
Start 
        
M :95R: :SELL/  GSCC/PART Party = [[Seller]]         
O :20C: :PROC//  Contra 
Transaction 
Reference 
        
O :70E:  :DECL/ /GSCC Financial Amount 
Declaration 
        
   /FAMT Par amount to 
DNA 
        
   /PRCT Price of the 
trade(s) to apply 
DNA to 
        

---

## Page 53

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 53 
M/
O 
Tag Block/ 
Qualifier  
Subqualifier / 
Options 
Field Description INST CANC CASE MDFC MDSE TDDK DNAL CDNA 
   /TDDT Trade Date of the 
trade(s) to apply 
DNA to 
        
   /TRID Trade [[ID]] of the 
trade to apply DN A 
to 
        
O :70C: :PACO/ /GSCC Narrative/ 
Additional 
Reference 
Numbers/ 
Information 
        
   /TDID Contra Trader 
[[ID]]/Trader [[ID]] 
        
M :16S: CONFPRTY  Repeat Block 
End  
        
M :36B:  :CONF/ /FAMT/ Quantity as Face 
Amount –Original 
Face Value (Par) 
        
M :35B:  /US/  TBA [[CUSIP]]         
M :16R: FIA  Optional Block 
Start 
        
O :12B:  :OPTI/ /CALL [[Call option]] Type 
or 
        
   /PUTO [[Put Option]] Type         
O :98A:  :EXPI//  Expiry Date         
O :13B:  :POOL/ GSCC/ Pool Number         
   /ISSR/ Pool [[issuer]]         
   CUSP/ Pool [[CUSIP]]         
M :16S: FIA  Block End         
O :70E:  :TPRO/ /GSCC Trade Instruction 
Processing 
Narrative 
        
   /TDSVSBOD Trade Service 
Type-SBOD 
Or 
        
   /TDSVTFTD Trade Service 
Type-TFTD 
Or 
        

---

## Page 54

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications 
Version C ontrol Page 54 
M/
O 
Tag Block/ 
Qualifier  
Subqualifier / 
Options 
Field Description INST CANC CASE MDFC MDSE TDDK DNAL CDNA 
   /TDSVSTIP Trade Service 
Type-STIP 
Or 
        
   /TDSVOPTN Trade Service 
Type-OPTN 
Or 
        
   /DKRS DK Reason         
M :16S: CONFDET  Block End         
M :16R: SETDET  Optional Block 
Start 
        
M :22F: :SETR/ /RPTO Indicator = 
Reporting 
Purposes  
        
O :17B:  :STAN/ /N Standing 
Instruction 
Override 
        
M :16R: AMT  Block Start         
M :19A:  :LOCO//USD  Commission 
Amount  
        
M :16S: AMT  Block End         
M :16S: SETDET  Block End         
4.3 MT509 Message 
This section provides the detailed specification for the MT509 message. The message type will be used by 
RTTM to notify Participants of the status of trades submitted. As described in the MT509 Overview in this 
document, the MT509 will be sent by RTTM to the [[participant]] for the following events: 
1. Trade Create Accepted 
2. Trade Create Rejected 
3. Modify Accepted 
4. Modify Rejected 
5. Modify Processed 
6. Modify Set Accepted 
7. Modify Set Rejected 
8. Modify Set Processed 
9. DK Accepted 
10. DK Rejected 
11. DK Processed 
12. Deleted Uncompared Transaction 

---

## Page 55

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 55 
13. Trade Create Unbalanced 
14. Trade Create Balanced 
15. DNA Accepted 
16. Cancel Accepted 
17. Cancel Rejected 
18. Cancel Processed 
19. Cancel Set Accepted 
20. Cancel Set Rejected 
21. Cancel Set Processed 
22. Cancel Lifted by [[participant]] 
23. Cancel Lifted by RTTM (For Future Use) 
24. Cancel Lifted by Contra (For Future Use) 
25. Cancel Set Lifted by [[participant]] 
26. Cancel Set Lifted by RTTM 
27. Cancel Set Lifted by Contra (For Future Use) 
28. Cancel DNA Accepted and Processed 
29. Trade Create Matched 
30. Trade Partially Matched (Long) 
31. Trade Partially Matched (Short) 
32. Trade Fully Matched 
 
The above record types are categorized as to whether the status relates to an Instruct or Cancel received, or 
regarding the matching status of a transaction. 
This section is organized in the following manner: 
• Section 4.3.1: General Format 
• Section 4.3.2: Field Specifications 
• Section 4.3.3: Field Analysis (25D=IPRC) 
• Section 4.3.4: Field Analysis (25D=CPRC) 
• Section 4.3.5: Field Analysis (25D=MTCH) 
Note: 
The Field Analysis section contains an analysis of the fields that may be found on each MT515 message. For each record 
type, a check mark will be found where it is possible for that field to appear on that record. It should be noted, however, t hat 
where a check mark appears, the check mark is not intended to indicate that a field is mandatory for a given record type. 
Where there is no check mark in a given box, that field is not applicable for the record type in question.  
 
4.3.1 MT509 General Format 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
    Message Header  

---

## Page 56

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 56 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
M    Password  12!c 
M    Sender  8!c 
M    Message Type 3!n/3!n/4!c  
M    Receiver  8!c 
M :16R: GENL  Block Start  
M :20C: :SEME//  Sender’s Message Reference 16x 
M :23G: INST  Message Function –Instruct or 4!c 
  CAST [/COPY] Cancel   
O :98C: :PREP//  Preparation Date/Time YYYYMMDDHHMMSS 
M :16R: LINK  Repeat Block Start  
M 
 
:20C: :MAST//  Master Reference Number  
(External Reference)  
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PREV//  Previous Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :RELA//  Related Reference Number  
(Sender’s Reference)  
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :LIST//  RTTM Assigned Reference 16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :BASK//  [[Broker]] Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PROG//  RTTM Assigned Contra Reference  16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :COMM//  Match Trade [[ID]]  16x 

---

## Page 57

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 57 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
M :16S: LINK  Repeat Block End  
M :16R: STAT  Repeat Block Start  
M :25D: :IPRC/ /PACK Trade Create is Acknowledged/ 
Validated or 
4!c 
   /REJT Trade Create, Modify, Modify Set, 
DNA or DK is rejected or  
 
   GSCC/MODA Modify Accepted or   
   GSCC/MODP Modify Processed or   
   GSCC/PAMS Modify Set Accepted or   
   GSCC/YPPR Modify Set Processed or   
   GSCC/PADK DK Accepted or  
   GSCC/DPPR DK Processed or  
   GSCC/DELE Deleted Uncompared Transaction 
or 
 
    GSCC/DEPS  Deleted Due to Fully Paid -Down  
Security or 
 
    GSCC/DESA  Deleted Due To System Action or  
   GSCC/TUNB Trade Create Unbalanced or  
   GSCC/TBAL Trade Create Balanced   
   GSCC/DNAL DNA Accepted   
  :CPRC/ /PACK Cancel Accepted or   
   /REJT Cancel or Cancel Set Rejected or  
   /CAND Cancel Processed or   
   GSCC/PACS Cancel Set Accepted or   
   GSCC/XPPR Cancel Set Processed or   
   GSCC/UPBP Cancel Lifted by [[participant]] or  
   GSCC/UPBR Cancel Lifted by RTTM or   
   GSCC/UPBC Cancel Lifted by Contra or  
   GSCC/VPBP Cancel Set Lifted by [[participant]] or  
   GSCC/VPBR Cancel Set Lifted by RTTM or   
   GSCC/VPBC Cancel Set Lifted by Contra  
   GSCC/CDNA Cancel DNA Accepted & Processed   

---

## Page 58

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 58 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
  :MTCH/ /MACH Trade Create has been Matched or  
   GSCC/MAPL Trade Partially Matched –Long 
Side or 
 
   GSCC/MAPS Trade Partially Matched –Short  
Side or 
 
   GSCC/MAFM Trade Fully Matched   
M :16R: REAS  Repeat Block Start  
M :24B: :REJT/  Reject Reason Code (see table)  4!c 
O :70D: :REAS/ /GSCC Reject Reason Narrative (6*35x) 
   /MDRJ Modify Rejected or  4!c 
   /MSRJ Modify Set Rejected or  
   /DKRJ DK Rejected or  
   /CSRJ Cancel Set Rejected   
   /DNRJ DNA Request Rejected or  
   /CDRJ Cancel DNA Rejected   
M :16S: REAS  Repeat Block End  
M :16S: STAT  Repeat Block End  
M :16S: GENL  Block End  
Note: 
MAST will exist on all MT509 messages except in the case where the MT509 message is a reject in response to receiving a 
non- SWIFT-compliant MT515. 
Error Code Qualifiers (to be used 
in field :24B::REJT/) 
Error Conditions (which can cause an MT515 to be 
rejected by RTTM)  
Data Field Format  
GSCC/E001 External Reference Error  4!c 
GSCC/E002 Previous External Reference Error   
GSCC/E003 Trade Not Eligible for Cancellation   
GSCC/E004 Unknown Secur ity  
GSCC/E005 Bad Quantity   
GSCC/E006 Bad Trade Date  
GSCC/E007 Bad [[settlement]] Date  
GSCC/E008 Bad Price  

---

## Page 59

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 59 
Error Code Qualifiers (to be used 
in field :24B::REJT/) 
Error Conditions (which can cause an MT515 to be 
rejected by RTTM)  
Data Field Format  
GSCC/E010 Bad [[Buyer]] Party   
GSCC/E011 Bad [[Seller]] Party   
GSCC/E012 [[Broker]] Reference Number Error   
GSCC/E013 Transaction Type Error   
GSCC/E014 Price Method Error   
GSCC/E015 Commission Error   
GSCC/E016 Password Error  
GSCC/E030 Trade Not In Same State  
GSCC/E102 Trade Service Type Error   
GSCC/E103 [[Option]] Type Error   
GSCC/E104 [[Option]] Expiry Date Error   
GSCC/E105 Account Trade Restricted   
GSCC/E108 Invalid Pool Identifier   
GSCC/E150 DNA not found  
GSCC/E152 Trade not eligible for cancellation due to DNA   
GSCC/E153 Trade not eligible for cancellation due to allocation  
GSCC/E154 [[settlement]] Date not eligible for DNA   
GSCC/E155 DNA Not Balanced   
GSCC/E156 No available TBA position for DNA   
GSCC/E157 DNA submitted after cutoff   
GSCC/E158 Duplicate DNA submission   
GSCC/E169 DNA not in valid state   
GSCC/E170 Maximum number DNA terms/trades exceeded   
GSCC/E171 Action will result in undeliverable piece 3.  
GSCC/E998 Trade Not Found  
GSCC/E999 Other Bad Data  
GSCC/F001 Illegal Operation Attempted   
GSCC/F002 Internal Process Error  
GSCC/F999 Non -SWIFT-Compliant Message   
 
3 For example, DNA will result in open position of <25K. 

---

## Page 60

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 60 
4.3.2 MT509 Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a message header.  All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password 12!c Password fields will be blank filled on MT509 messages.  
Sender 8!c MBSCTRRS (MBSD Trade Registration and Reconciliation System) will always be 
the sender of the MT509 matching -related messages.  
Message Type 3!n/3!n/4!c  The first three characters indicate to the recipient the message type (509); the 
second three positions reflect the version of the message interface (currently always 
000). The last four characters indicate the [[issuer]] code to be used in the message 
(“GSCC”). 
Receiver 8!c MBSD account number of the [[participant]] receiving the message 
GENL This Mandatory Block provides general information regarding the message.  
It appears only once in a trade contract.  
20C Sender Message Reference 
• SEME//: This mandatory field contains the sender’s (RTTM) message reference number.  It is 
used on all messages sent by RTTM and will contain a unique number to  unambiguously 
identify each message.)  
Note: 
While the SWIFT message accommodates both upper and lower case alphanumeric and certain 
symbols, for RTTM purposes, this field will be populat ed with an upper case alphanumeric value.  It will 
not contain symbols or hyphens.  
e.g., :20C::SEME//ABCDEFG1 
23G Function of the Message 
This mandatory field identifies the function of the message.  It will either be a status new message 
(INST) or a cancellation of a previous message (CAST):  
• INST: This qualifier will be used for following MT509 messages  
− all MT509 transaction/trade status messages referring to previously submitted Trade 
Creates, Modifies, Modify Sets, DKs  or DNA; 
− all MT509 Reject Messages where the MT515 was rejected for being non -SWIFT 
compliant, even where the original message may have been a Cancel or a Cancel Set;  
− all messages containing a matching status; and  
− all Deleted Uncompared Transaction, Trade Create Balanced and Trade Creat e 
Unbalanced Messages.  
• CAST[/COPY]: This qualifier will be used for MT509 messages referring to previously 
submitted Cancel, a Cancel Set Message, or a Cancel DNA Request . 
Note: 
When a brokered trade is canceled after it becomes fully matched (FMAT), the [[Broker]] will receive a 
copy, for informational purposes only, of the regular MT509 Cancel Processed (:25D::CPRC//CAND) 
Messages sent to both dealers. The informational nature of these Cancel Processed Messages will be 

---

## Page 61

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 61 
Block/Tag Notes 
reflected by adding “/COPY” to this field. At this time, the “/COPY” suffix will not be used for any other 
MT509 messages.  
e.g., :23G:INST 
98C Preparation Date and Time 
• PREP//: This optional field contains the date an d time the message by RTTM was prepared.  
Note: 
The “C” format for this (98) tag indicates a date/time format of “YYYYMMDDHHMMSS”.  
e.g., :98C::PREP//20011218102015 
LINK The LINK Block will be repeated for as many reference qualifiers as need to be included in a 
Trade Status Message. Each subsequence contains reference numbers to identify the 
transaction or trade for which the status is being reported. Each reference number will be 
enclosed within a Start Link Block (:16R:LINK) and End Link Block (:1 6S:LINK). All LINK 
repeating subsequences are within the GENL Block.  
20C Reference 
The Reference Numbers that have been provided by the [[participant]] must contain upper case 
alphanumeric characters, but not symbols or hyphens.  As indicated above, each reference number 
must be enclosed in a LINK Start and End block.  
• MAST//: Master Reference Number -This qualifier will always be populated with the 
− [[participant]]’s External Reference Number (x -ref). This number can be used by:  
− Dealers-to uniquely identify thei r transactions (trades or DNAs) 
− Brokers -to uniquely identify their submissions prior to balancing.  
This field may not be populated on MT509's under the following circumstances:  
− an MT515 DK Message targeting a Comparison Request  
− an MT515 Modify Set or Cancel Set message (submitted by a [[Broker]])  
− a Dealer’s transaction that has been compared after being split and/or spliced  
− any MT515 message that was rejected for being non -SWIFT compliant.  
 
• PREV//: Previous Reference Number  
− For MT509 messages sent to Deal ers, this qualifier is used only on records where the 
Dealer modifies the External Reference Number. On those records, the PREV field will 
reflect the Dealer’s previous External Reference Number.  
− For MT509 messages sent to Brokers, this qualifier is used o nly on the following records:  
 For message type:  This field should be populated with the following:   
All records where the [[Broker]]  
modifies the [[Broker]] Reference 
Number after balancing (i.e., 
using the Modify Set message)
 
• The PREV field will reflect the [[Broker]]’s previous 
[[Broker]] Reference Number.  
Trade Create Balanced  • the PREV field will reflect the previous RTTM 
assigned reference number (i.e., the Submission [[ID]])  
• the LIST field will reflect the new RTTM assigned 
reference number (i.e., the Transaction [[ID]])  

---

## Page 62

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 62 
Block/Tag Notes 
Trade Partially Matched (Short 
or Long Side)  
• the PREV field will reflect the previous RTTM 
assigned reference number (i.e., the Transaction [[ID]])
 
• the LIST field will reflect the new RTTM assigned 
reference number (i.e., the Trade [[ID]])  
• RELA//: MT515 Sender’s Message Reference Number : This qualifier will contain the 
Sender’s Message Reference Number (20C::SEME//) from the MT515 submitted by the 
[[participant]]. It will only appear on those MT509 messages that are acknowledgements  of 
receipt or rejections of MT515 messages. This will be the only 20C qualifier in the LINK block 
where an MT509 Reject Message is being created for a non -SWIFT compliant MT515. 
 
• LIST//: RTTM Reference Number : This qualifier contains the RTTM assigned Reference 
Number. For DNA and Cancel DNA Requests RTTM Reference will be DNA [[ID]]. For all other 
messages depending on the [[participant]] type and the comparison status of a transaction or a 
trade, the RTTM Reference Number will be a Submission [[ID]], a Transaction [[ID]] or a Trade [[ID]]. 
This is illustrated in the table below:  
 [[participant]] Type Comparison Status  RTTM Reference Number   
Dealer Pre-Comparison Transaction [[ID]]  
Post-Comparison  Trade [[ID]] (Tran [[ID]])  
[[Broker]] Pre-Balancing  Submission [[ID]]  
Post-Balancing  
Pre-Comparison 
Transaction [[ID]]  
Post-Comparison (PMAT and 
FMAT) 
Transaction [[ID]] (PMAT only) or Trade 
[[ID]] (PMAT and FMAT)  
• BASK//: [[Broker]]-Related Reference Number  - This qualifier contains a [[Broker]] -specified [[Broker]] 
reference number, or RTTM -assigned [[Broker]] match identifier, depending on [[participant]] type.  
[[participant]] Type BASK Reference Number  
[[Broker]] This field specifies the [[Broker]]’s Reference Number, and is reflected in 
all messages where receiving [[participant]] is a [[Broker]], except for 
MT509's sent in response to DK messages submitted by a [[Broker]] (vs. 
a Comparison Request)  
Dealer This field contains an RTTM assigned [[Broker]] Match Identifier,  used to 
associate the set of dealer trade(s) and [[Broker]]  advisory(s)  involved in 
a match. It will appear on MT509 Match  (MTCH//MACH) only, and is 
populated in any match event  versus a [[Broker]] trade, regardless of 
whether matched via Net Position (split/splice) or exact match.  
 
• PROG//: RTTM Assigned Contra Reference -  This field specifies the contra’s RTTM  assigned 
reference number. It is reflected only on MT509 messages where the receiving [[participant]] has 
DK’ed a Comparison Request submitted against the m. 
 
• COMM//: RTTM Assigned Match Trade [[ID]]  - This field specifies the [[participant]]’s RTTM 
assigned trade reference number at the time of match (Trade [[ID]]). This qualifier will only appear 
on MT509 Match (MTCH//MACH) in order to enable participants to link the RTTM Assigned 
Transaction [[ID]] (unmatched) to  the RTTM Assigned Trade [[ID]] (matched). After the match event, 

---

## Page 63

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 63 
Block/Tag Notes 
the RTTM Assigned Trade [[ID]] will continue to be reflected in :20C::LIST on all RTTM interactive 
output. 
Note: 
While the SWIFT message accommodates both upper and lower case alphanumeric and certain 
symbols, for MBSD purposes, this field will be populated with an upper case alphanumeric value. It will 
not contain symbols or hyphens, except where the reference number has been assigned by RTTM. For 
more detailed information on the use of transaction- related reference numbers, see Appendix C
. 
e.g., :20C::MAST//REF010 
STATUS The Status Block will appear on every MT509 message and will notify the [[Member]] of the type 
of MT509 record being sent, as well as the status of the trade, or record, that was submitted to 
RTTM.  
25D Status Code  
The Status Code indicates the record type/type of status message being sent by RTTM. The following 
are the various message types, which will be used for Interactive Messaging to support real -time 
comparison.  
• IPRC//PACK: This qualifier/[[Option]] is used to indicate that a Trade Create Message has  been 
accepted by RTTM.  
• IPRC//REJT-This qualifier/[[Option]] is used to indicate that a Trade Create, Modify, DK, or DNA 
Request Message has been rejected by RTTM.  The IPRC//REJT qualifier will be used in all 
instances where an incoming MT515 message is reject ed for being non- SWIFT compliant 
(:24B::REJT/GSCC/F999). 
• IPRC//GSCC/MODA: This qualifier/[[Option]] is used to indicate that Modify Request has been 
accepted  
• IPRC//GSCC/MODP: This qualifier/[[Option]] is used to indicate that Modify Request has been 
processed  
• IPRC//GSCC/PAMS: This qualifier/[[Option]] is used to indicate that Modify Set Request has been 
accepted  
• IPRC//GSCC/YPPR: This qualifier/[[Option]] is used to indicate that Modify Set Request has been 
processed  
• IPRC//GSCC/PADK: This qualifier/[[Option]] is used to indicat e that DK Request has been 
accepted  
• IPRC//GSCC/DPPR: This qualifier/[[Option]] is used to indicate that DK Request has been 
processed  
• IPRC//GSCC/DELE: This qualifier/[[Option]] is used to indicate that pending comparison 
transaction has been deleted by RTTM (used for uncompared SBOD records before TBA net)  
• IPRC//GSCC/DEPS: This qualifier/[[Option]] is used to indicate that transaction has been deleted 
by RTTM d ue to Pool Number specified was fully paid down  
• IPRC//GSCC/DESA: This qualifier/[[Option]] is used to indicate that transaction has been deleted 
by RTTM due to system -forced action 
• IPRC//GSCC/TUNB: This qualifier/[[Option]] is used to indicate that Trade Create submitted by 
[[Broker]] is Unbalanced  
• IPRC//GSCC/TBAL: This qualifier/[[Option]] is used to indicate that Trade Create submitted by 
[[Broker]] is balanced  
• IPRC//GSCC/DNAL: This qualifier/[[Option]] is used to indicate that DNA Request has been 
accepted  
• CPRC//PACK: This qualifier/[[Option]] is used to indicate that Cancel request has been accepted 
by RTTM 
• CPRC//REJT: This qualifier/[[Option]] is used to indicate that Cancel, Cancel Set , or Cancel DNA 
request has been rejected by RTTM  

---

## Page 64

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 64 
Block/Tag Notes 
• CPRC//CAND: This qualifier/[[Option]] is used to indicate that Cancel request has been processed 
by RTTM 
• CPRC/GSCC/PACS: This qualifier/[[Option]] is used to indicate that Cancel Set request has been 
accepted by RTTM. This record will only be sent to Brokers  
• CPRC/GSCC/XPPR: This qualifier/[[Option]] is used to indicate that Cancel Set request has been 
processed by RTTM. This record will only be sent to Brokers  
• CPRC/GSCC/UPBP: This qualifier/[[Option]] is used to indicate that Cancel has been lifted by the 
receiver of the MT509 
• CPRC/GSCC/UPBR: This qualifier/[[Option]] is used  to indicate that Cancel has been lifted by 
RTTM 
• CPRC/GSCC/UPBC: This qualifier/[[Option]] is used to indicate that Cancel has been lifted by the 
contra  
• CPRC/GSCC/VPBP: This qualifier/[[Option]] is used to indicate that Cancel Set has been lifted by 
the receiver of the MT509 
• CPRC/GSCC/VPBR: This qualifier/[[Option]] is used to indicate that Cancel Set has been lifted by 
RTTM 
• CPRC/GSCC/VPBC: This qualifier/[[Option]] is used to indicate that Cancel Set has been lifted by 
the contra  
• CPRC/GSCC/CDNA: This qualifier/[[Option]] is u sed to indicate that Cancel DNA request has 
been accepted and processed by RTTM.  
• MTCH//MACH: This qualifier/[[Option]] is used to indicate that Trade Create Transaction has been 
matched  
• MTCH//GSCC/MAPL: This qualifier/[[Option]] is used to indicate to a [[Broker]] that the long side of 
the transaction ([[Broker]]’s buy) has been compared with the dealer to create a partially matched 
trade 
• MTCH//GSCC/MAPS: This qualifier/[[Option]] is used to indicate to a [[Broker]] that the short side of 
the transaction ([[Broker]]’s sell) has been compared with the dealer to create a partially matched 
trade 
• MTCH//GSCC/MAFM: This qualifier/[[Option]] is used to indicate to a [[Broker]] that both sides of the 
transaction have been compared with the dealers to create a fully matched trade 
 e.g., :25D::IPRC//PACK 
REASON The Reason Block will appear on MT509 messages where an MT515 submitted by the [[Member]] 
has been rejected by RTTM.  Each Reason Code must be enclosed within a Start Reason 
(:16R:REAS) and End Reason (:16S:REAS) Block.  
24B Reason Code  
This field is mandatory in the block and will appear on all Reject Messages. There can be multiple 
Reason Codes on any MT509 Reject Message; each Reason Code must be enclosed within a Start 
Reason (:16R:REAS) and End Reason (:16S:REAS) Block. T he Reason Code will be populated with 
the following value:  
• REJT/: This qualifier/[[Option]] is used on all messages that indicate that submission was rejected 
by RTTM 
Note: 
As the list of error codes can be expanded in the future, the list will be amended, wit hout modifying the 
entire specification. Please see the MT509 layout, which details all error conditions (and associated 
codes) that would result in the rejection of a [[participant]] MT515 message.  
 e.g., :24B::REJT/GSCC/E004 
70D Reason Narrative (REAS) 

---

## Page 65

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 65 
Block/Tag Notes 
REAS//GSCC: The reason narrative field can contain narrative on those MT509 Reject  Messages 
created in response to receiving a non -SWIFT compliant MT515, or can contain one  of the following 
qualifiers:  
• /MDRJ: This qualifier/[[Option]] will be included on all MT509 Modify Rejected Message when 
MT515 Modify Request has been rejected by RTTM  
• /MSRJ: This qualifier/[[Option]] will be included on all MT509 Modify Set Rejected Message when 
MT515 Modify Set Request has been rejected by RTTM  
• /DKRJ: This qualifier/[[Option]] will be included on all MT509 DK Rejected Message when MT515 
DK Request has been rejected by RTTM  
• /CSRJ: This qualifier/[[Option]] will be included on all MT509 Cancel Set Rejected Message when 
MT515 Cancel Set Request has been rejected by RTTM  
• /DNRJ: This  qualifier/[[Option]] will be included on all MT509 DNA Rejected Message when 
MT515 DNA Request has been rejected by RTTM  
• /CDRJ: This qualifier/[[Option]] will be included on all MT509 Cancel DNA Rejected Message 
when MT515 Cancel DNA Request has been rejected by RTTM  
Note: 
This narrative field will appear in the first repeating REAS sequence 
 e.g., :70D::REAS//GSCC/MDRJ 
4.3.3 MT509 Field Analysis (25D=IPRC) 
M/
O 
Tag Block/ 
Qualifie
r 
Sub 
qualifier  
Field 
Description 
IPRC/ 
PACK 
IPRC// 
REJT 
(*) 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/
PAMS 
IPRC/ 
GSCC/
YPPR 
IPRC/ 
GSCC/
PADK 
IPRC/ 
GSCC/
DPPR 
IPRC/ 
GSCC/
DELE 
IPRC/ 
GSCC/
DEPS 
IPRC/ 
GSCC/
DESA 
IPRC/ 
GSCC/
TUNB  
IPRC/ 
GSCC/
TBAL 
IPRC/ 
GSCC/ 
DNAL 
    Message 
Header  
              
M    Password                
M    Sender               
M    Message 
Type 
              
M    Receiver                
M :16R: GENL  Block Start                
M :20C:  :SEME//  Sender’s 
Reference 
for this 
message  
              
M :23G: INST  Message 
Function - 
Instruct or  
              
  CAST [/COPY] Cancel               
O :98C:  :PREP//  Preparation 
Date/Time  
              

---

## Page 66

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 66 
M/
O 
Tag Block/ 
Qualifie
r 
Sub 
qualifier  
Field 
Description 
IPRC/ 
PACK 
IPRC// 
REJT 
(*) 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/
PAMS 
IPRC/ 
GSCC/
YPPR 
IPRC/ 
GSCC/
PADK 
IPRC/ 
GSCC/
DPPR 
IPRC/ 
GSCC/
DELE 
IPRC/ 
GSCC/
DEPS 
IPRC/ 
GSCC/
DESA 
IPRC/ 
GSCC/
TUNB  
IPRC/ 
GSCC/
TBAL 
IPRC/ 
GSCC/ 
DNAL 
M :16R: LINK  Repeat 
Block Start  
              
M :20C:  :MAST//   Master 
Reference 
No 
              
M :16S: LINK  Repeat 
Block End 
              
M :16R: LINK  Repeat 
Block Start  
              
O :20C:  :PREV//  Previous 
Reference 
No  
              
M :16S: LINK  Repeat 
Block End 
              
M :16R: LINK  Repeat 
Block Start  
              
O :20C:  :RELA//   Related 
Reference 
No (MT515 
sender’s ref)  
              
M :16S: LINK  Repeat 
Block End 
              
M :16R: LINK  Repeat 
Block Start  
              
O :20C:  :LIST//   RTTM 
Assigned 
Reference  
              
M :16S: LINK  Repeat 
Block End 
              
M :16R: LINK  Repeat 
Block Start  
              
O :20C:  :BASK//  [[Broker]] 
Reference 
No. 
              
M :16S: LINK  Repeat 
Block End 
              
M :16R: LINK  Repeat 
Block Start  
              
O :20C:  :PROG//   RTTM 
Assigned 
              

---

## Page 67

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 67 
M/
O 
Tag Block/ 
Qualifie
r 
Sub 
qualifier  
Field 
Description 
IPRC/ 
PACK 
IPRC// 
REJT 
(*) 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/
PAMS 
IPRC/ 
GSCC/
YPPR 
IPRC/ 
GSCC/
PADK 
IPRC/ 
GSCC/
DPPR 
IPRC/ 
GSCC/
DELE 
IPRC/ 
GSCC/
DEPS 
IPRC/ 
GSCC/
DESA 
IPRC/ 
GSCC/
TUNB  
IPRC/ 
GSCC/
TBAL 
IPRC/ 
GSCC/ 
DNAL 
Contra 
Reference 
M :16S: LINK  Repeat 
Block End 
              
M :16R: LINK  Repeat 
Block Start  
              
O :20C:  :COMM/
/ 
 RTTM 
Assigned 
Match Trade 
[[ID]] 
              
M :16S: LINK  Repeat 
Block End 
              
M :16R: STAT  Repeat 
Block Start  
              
M :25D:  :IPRC/  /PACK Trade is 
acknowledge
d/ validated 
              
   /REJT Trade, 
Modify, 
Modify Set, 
DK
 or DNA  
is rejected 
              
   GSCC/ 
MODA 
Modify 
Accepted  
              
   GSCC/ 
MODP 
Modify 
Processed 
              
   GSCC/ 
PAMS 
Modify Set 
Accepted  
              
   GSCC/ 
YPPR 
Modify Set 
Processed 
              
   GSCC/ 
PADK 
DK Accepted                
   GSCC/ 
DPPR 
DK 
Processed 
              
 
  GSCC/ 
DELE 
Deleted 
Uncompared 
Transaction 
              
   GSCC/ 
DEPS 
Deleted Due 
to Fully Paid-
Down 
Security or  
              

---

## Page 68

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 68 
M/
O 
Tag Block/ 
Qualifie
r 
Sub 
qualifier  
Field 
Description 
IPRC/ 
PACK 
IPRC// 
REJT 
(*) 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/
PAMS 
IPRC/ 
GSCC/
YPPR 
IPRC/ 
GSCC/
PADK 
IPRC/ 
GSCC/
DPPR 
IPRC/ 
GSCC/
DELE 
IPRC/ 
GSCC/
DEPS 
IPRC/ 
GSCC/
DESA 
IPRC/ 
GSCC/
TUNB  
IPRC/ 
GSCC/
TBAL 
IPRC/ 
GSCC/ 
DNAL 
   GSCC/ 
DESA 
Deleted Due 
To System 
Action or 
              
   GSCC/ 
TUNB 
Transaction 
Unbalanced 
              
   GSCC/ 
TBAL 
Transaction 
Balanced 
              
   GSCC/ 
DNAL 
DNA 
Accepted  
              
  :CPRC/  /PACK Cancel 
Accepted  
              
   /REJT Cancel (Se t, 
DNA)) 
Rejected  
              
   /CAND Cancel 
Processed 
              
   GSCC/ 
PACS 
Cancel Set 
Accepted  
              
   GSCC/ 
XPPR 
Cancel Set 
Processed 
              
   GSCC/ 
UPBP 
Cancel Lifted 
by 
[[participant]]  
              
   GSCC/ 
UPBR 
Cancel Lifted 
by RTTM 
              
   GSCC/ 
UPBC 
Cancel Lifted 
by Contra  
              
   GSCC/ 
VPBP 
Cancel Set 
Lifted by 
[[participant]]  
              
   GSCC/ 
VPBR 
Cancel Set 
Lifted by 
RTTM 
              
   GSCC/ 
VPBC 
Cancel Set 
Lifted by 
Contra 
              
   GSCC/ 
CDNA  
Cancel DNA                

---

## Page 69

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 69 
M/
O 
Tag Block/ 
Qualifie
r 
Sub 
qualifier  
Field 
Description 
IPRC/ 
PACK 
IPRC// 
REJT 
(*) 
IPRC/ 
GSCC/ 
MODA 
IPRC/ 
GSCC/ 
MODP 
IPRC/ 
GSCC/
PAMS 
IPRC/ 
GSCC/
YPPR 
IPRC/ 
GSCC/
PADK 
IPRC/ 
GSCC/
DPPR 
IPRC/ 
GSCC/
DELE 
IPRC/ 
GSCC/
DEPS 
IPRC/ 
GSCC/
DESA 
IPRC/ 
GSCC/
TUNB  
IPRC/ 
GSCC/
TBAL 
IPRC/ 
GSCC/ 
DNAL 
  :MTCH/  /MACH Trade Has 
Been 
Matched  
              
   GSCC/ 
MAPL 
Trade 
Partially 
Matched –
Long Side 
              
   GSCC/ 
MAPS 
Trade 
Partially 
Matched –
Short Side 
              
   GSCC/ 
MAFM 
Trade Fully 
Matched  
              
M :16R: REAS  Optional 
Repeat 
Block Start  
              
M :24B: :REJT/  GSCC/ Reject 
Reason 
Code 
              
O :70D:  :REAS/ /GSCC Reject 
Reason 
Narrative 
              
   /MDRJ  Modify 
Rejected  
              
   /MSRJ  Modify Set 
Rejected  
              
   /DKRJ  DK Rejected                
   /CSRJ  Cancel Set 
Rejected  
              
   /DNRJ  DNA 
Rejected  
              
   /CDRJ  Cancel DNA 
Rejected  
              
M :16S: REAS  Repeat 
Block End 
              
M :16S: STAT  Repeat 
Block End 
              
M :16S: GENL  Block End               
 

---

## Page 70

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 70 
Note: 
The following 5 records are covered within  the IPRC// REJT (*) column:   
• Trade Create Rejected Messages  
• Modify Rejected Messages  
• Modify Set Rejected Messages  
• DK Rejected Messages  
• DNA Rejected Messages  
4.3.4 MT509 Field Analysis (25D=CPRC) 
M/O Tag Block/ 
Qualifier  
Sub-
qualifier  
Field 
Description 
CPRC// 
PACK 
CPRC// 
REJT 
(*) 
CPRC// 
CAND 
CPRC/ 
GSCC/
PACS 
CPRC/ 
GSCC/
XPPR 
CPRC/ 
GSCC/
UPBP 
CPRC/ 
GSCC/
UPBR 
(**) 
CPRC/ 
GSCC/
UPBC 
(**) 
CPRC/ 
GSCC/
VPBP 
CPRC/ 
GSCC/
VPBR 
CPRC/ 
GSCC/
VPBC 
(**) 
CPRC/ 
GSCC/ 
CDNA 
    Message 
Header  
            
M    Password              
M    Sender             
M    Message 
Type 
            
M    Receiver              
M :16R: GENL  Block Start              
M :20C:  :SEME//  Sender’s 
Reference for 
this message  
            
M :23G: INST  Message 
Function - 
Instruct or  
            
  CAST [/COPY] Cancel             
O :98C:  :PREP//  Preparation 
Date/Time  
            
M :16R: LINK  Repeat Block 
Start 
            
M :20C:  :MAST//   Master 
Reference No 
            
M :16S: LINK  Repeat Block 
End 
            

---

## Page 71

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 71 
M/O Tag Block/ 
Qualifier  
Sub-
qualifier  
Field 
Description 
CPRC// 
PACK 
CPRC// 
REJT 
(*) 
CPRC// 
CAND 
CPRC/ 
GSCC/
PACS 
CPRC/ 
GSCC/
XPPR 
CPRC/ 
GSCC/
UPBP 
CPRC/ 
GSCC/
UPBR 
(**) 
CPRC/ 
GSCC/
UPBC 
(**) 
CPRC/ 
GSCC/
VPBP 
CPRC/ 
GSCC/
VPBR 
CPRC/ 
GSCC/
VPBC 
(**) 
CPRC/ 
GSCC/ 
CDNA 
M :16R: LINK  Repeat Block 
Start 
            
O :20C:  :PREV//  Previous 
Reference No  
            
M :16S: LINK  Repeat Block 
End 
            
M :16R: LINK  Repeat Block 
Start 
            
O :20C:  :RELA//   Related 
Reference No 
(MT515 
sender’s ref)  
            
M :16S: LINK  Repeat Block 
End 
            
M :16R: LINK  Repeat Block 
Start 
            
O :20C:  :LIST//   RTTM 
Assigned 
Reference  
            
M :16S: LINK  Repeat Block 
End 
            
M :16R: LINK  Repeat Block 
Start 
            
O :20C:  :BASK//  [[Broker]] 
Reference No.
 
            
M :16S: LINK  Repeat Block 
End 
            
M :16R: LINK  Repeat Block 
Start 
            
O :20C:  :PROG//  RTTM 
Assigned 
Contra 
Reference 
            
M :16S: LINK  Repeat Block 
End 
            
M :16R: LINK  Repeat Block 
Start 
            
O :20C:  :COMM//   RTTM 
Assigned 
            

---

## Page 72

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 72 
M/O Tag Block/ 
Qualifier  
Sub-
qualifier  
Field 
Description 
CPRC// 
PACK 
CPRC// 
REJT 
(*) 
CPRC// 
CAND 
CPRC/ 
GSCC/
PACS 
CPRC/ 
GSCC/
XPPR 
CPRC/ 
GSCC/
UPBP 
CPRC/ 
GSCC/
UPBR 
(**) 
CPRC/ 
GSCC/
UPBC 
(**) 
CPRC/ 
GSCC/
VPBP 
CPRC/ 
GSCC/
VPBR 
CPRC/ 
GSCC/
VPBC 
(**) 
CPRC/ 
GSCC/ 
CDNA 
Match Trade 
[[ID]] 
M :16S: LINK  Repeat Block 
End 
            
M :16R: STAT  Repeat Block 
Start 
            
M :25D:  :IPRC/  /PACK Trade is 
acknowledged
/ validated 
            
   /REJT Trade, Modify, 
Modify Set, 
DK, or DNA is 
rejected 
            
   GSCC/ 
MODA 
Modify 
Accepted  
            
   GSCC/ 
MODP 
Modify 
Processed 
            
   GSCC/ 
PAMS 
Modify Set 
Accepted  
            
   GSCC/ 
YPPR 
Modify Set 
Processed 
            
   GSCC/ 
PADK 
DK Accepted              
   GSCC/ 
DPPR 
DK Processed              
   GSCC/ 
DELE 
Deleted 
Uncompared 
Transaction 
            
   GSCC/ 
DEPS  
Deleted Due 
to Fully Paid-
Down Security 
or  
            
   GSCC/ 
DESA 
Deleted Due 
To System 
Action or 
            
   GSCC/ 
TUNB 
Transaction 
Unbalanced 
            
   GSCC/ 
TBAL 
Transaction 
Balanced 
            

---

## Page 73

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 73 
M/O Tag Block/ 
Qualifier  
Sub-
qualifier  
Field 
Description 
CPRC// 
PACK 
CPRC// 
REJT 
(*) 
CPRC// 
CAND 
CPRC/ 
GSCC/
PACS 
CPRC/ 
GSCC/
XPPR 
CPRC/ 
GSCC/
UPBP 
CPRC/ 
GSCC/
UPBR 
(**) 
CPRC/ 
GSCC/
UPBC 
(**) 
CPRC/ 
GSCC/
VPBP 
CPRC/ 
GSCC/
VPBR 
CPRC/ 
GSCC/
VPBC 
(**) 
CPRC/ 
GSCC/ 
CDNA 
   GSCC/ 
DNAL 
DNA 
Accepted  
            
  :CPRC/  /PACK Cancel 
Accepted  
            
   /REJT Cancel (Set  or 
DNA) 
Rejected  
            
   /CAND Cancel 
Processed 
            
   GSCC/ 
PACS 
Cancel Set 
Accepted  
            
   GSCC/ 
XPPR 
Cancel Set 
Processed 
            
   GSCC/ 
UPBP 
Cancel Lifted 
by [[participant]]  
            
   GSCC/ 
UPBR 
Cancel Lifted 
by RTTM 
            
   GSCC/ 
UPBC 
Cancel Lifted 
by Contra  
            
   GSCC/ 
VPBP 
Cancel Set 
Lifted by 
[[participant]]  
            
   GSCC/ 
VPBR 
Cancel Set 
Lifted by 
RTTM 
            
   GSCC/ 
VPBC 
Cancel Set 
Lifted by 
Contra 
            
   GSCC/ 
CDNA  
Cancel DNA 
Accepted and 
Processed  
            
  :MTCH/  /MACH Trade Has 
Been Matched 
            
   GSCC/ 
MAPL 
Trade Partially 
Matched –
Long Side 
            
   GSCC/ 
MAPS 
Trade Partially 
Matched –
Short Side 
            

---

## Page 74

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 74 
M/O Tag Block/ 
Qualifier  
Sub-
qualifier  
Field 
Description 
CPRC// 
PACK 
CPRC// 
REJT 
(*) 
CPRC// 
CAND 
CPRC/ 
GSCC/
PACS 
CPRC/ 
GSCC/
XPPR 
CPRC/ 
GSCC/
UPBP 
CPRC/ 
GSCC/
UPBR 
(**) 
CPRC/ 
GSCC/
UPBC 
(**) 
CPRC/ 
GSCC/
VPBP 
CPRC/ 
GSCC/
VPBR 
CPRC/ 
GSCC/
VPBC 
(**) 
CPRC/ 
GSCC/ 
CDNA 
   GSCC/ 
MAFM 
Trade Fully 
Matched  
            
M :16R: REAS  Optional 
Repeat Block 
Start 
            
M :24B: :REJT/  GSCC/ Reject 
Reason Code  
            
O :70D:  :REAS/ /GSCC Reject 
Reason 
Narrative 
            
   /MDRJ  Modify 
Rejected  
            
   /MSRJ  Modify Set 
Rejected  
            
   /DKRJ  DK Rejected              
   /CSRJ  Cancel Set 
Rejected  
            
   /DNRJ  DNA Rejected              
   /CDRJ  Cancel DNA 
Rejected  
            
M :16S: REAS  Repeat Block 
End 
            
M :16S: STAT  Repeat Block 
End 
            
M :16S: GENL  Block End             
 
Notes: 
The following records are covered within th e CPRC// REJT (*) column:  
• Cancel Rejected Messages  
• Cancel DNA Rejected  
(**) For Future Use  

---

## Page 75

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 75 
4.3.5 MT509 Field Analysis (25D=MTCH) 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier Field Description MTCH/ 
MACH 
MTCH/ 
GSCC/ 
MAPL 
MTCH/ 
GSCC/ 
MAPS 
MTCH/ 
GSCC/ 
MAFM 
    Message Header     
M    Password      
M    Sender      
M    Message Type     
M    Receiver      
M :16R: GENL  Block Start     
M :20C: :SEME//  Sender’s Reference for 
this message 
    
M :23G: INST  Message Function - 
Instruct or  
    
  CAST  [/COPY] Cancel      
O :98C: :PREP//  Preparation Date/Time     
M :16R: LINK  Repeat Block Start     
M :20C: :MAST//  Master Reference No      
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :PREV//  Previous Reference No       
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :RELA//  Related Reference No 
(MT515 sender’s ref)  
    
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :LIST//  RTTM Assigned 
Reference 
     
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :BASK//  [[Broker]] Reference No.      
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     

---

## Page 76

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 76 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier Field Description MTCH/ 
MACH 
MTCH/ 
GSCC/ 
MAPL 
MTCH/ 
GSCC/ 
MAPS 
MTCH/ 
GSCC/ 
MAFM 
O :20C: :PROG//  RTTM Assigned Contra 
Reference 
    
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :COMM//  RTTM Assigned Match 
Trade [[ID]] 
    
M :16S: LINK  Repeat Block End     
M :16R: STAT  Repeat Block Start     
M :25D: :IPRC/ /PACK Trade is acknowledged/ 
validated  
    
   /REJT Trade, Modify, Modify Set 
or DK is rejected  
    
   GSCC/MODA Modify Accepted      
   GSCC/MODP Modify Processed      
   GSCC/PAMS Modify Set Accepted      
   GSCC/YPPR Modify Set Processed      
   GSCC/PADK DK Accepted      
   GSCC/DPPR DK Processed      
   GSCC/DELE Deleted Uncompared 
Transaction  
    
   GSCC/TUNB Transaction Unbalanced      
   GSCC/TBAL Transaction Balanced      
   GSCC/DNAL DNA Accepted      
  :CPRC/ /PACK Cancel Accepted      
   /REJT Cancel (Set) Rejected      
   /CAND Cancel Processed      
   GSCC/PACS Cancel Set Accepted      
   GSCC/XPPR Cancel Set Processed      
   GSCC/UPBP Cancel Lifted by 
[[participant]]  
    
   GSCC/UPBR Cancel Lifted by RTTM      
   GSCC/UPBC Cancel Lifted by Contra     

---

## Page 77

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 77 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier Field Description MTCH/ 
MACH 
MTCH/ 
GSCC/ 
MAPL 
MTCH/ 
GSCC/ 
MAPS 
MTCH/ 
GSCC/ 
MAFM 
   GSCC/VPBP Cancel Set Lifted by 
[[participant]]  
    
   GSCC/VPBR Cancel Set Lifted by 
RTTM 
    
   GSCC/VPBC Cancel Set Lifted by 
Contra  
    
   GSCC/CDNA Cancel DNA Accepted 
and Processed  
    
  :MTCH/ /MACH Trade Has Been Matched      
   GSCC/MAPL Trade Partially Matched –
Long Side  
    
   GSCC/MAPS Trade Partially Matched –
Short Side  
    
   GSCC/MAFM Trade Fully Matched      
M :16R: REAS  Optional Repeat Block 
Start 
    
M :24B: :REJT/ GSCC/ Reject Reason Code     
O :70D: :REAS/ /GSCC Reject Reason Narrative     
   /MDRJ Modify Rejected      
   /MSRJ Modify Set Rejected      
   /DKRJ DK Rejected      
   /CSRJ Cancel Set Rejected      
   /DNRJ DNA Rejected      
   /CDRJ Cancel DNA Rejected      
M :16S: REAS  Repeat Block End     
M :16S: STAT  Repeat Block End     
M :16S: GENL  Block End     
 
4.4 MT518 Message 
This section contains the detailed specification for the MT518 message. The SWIFT layout for the MT518 is 
almost identical to that of the MT515 message used by Participants to submit instructions to RTTM. 
It should be noted that the various types of MT518s described previously in the document can be divided into 
one of the two message categories below: 

---

## Page 78

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 78 
• Advisories 
• Modifications/Events based on your Trades 
 
ADVISORIES 
Advisories sent to a [[participant]] reflect the trade record as submitted by the contraparty. The Buy/Sell indicator 
(transaction type) on the record is, however, from the perspective of the recipient of the MT518. 
The following MT518 record types are advisories, and reflect transaction information submitted against the 
[[participant]]: 
• Comparison Request: CMPR 
• Comparison Request Modify: CRQM 
• Comparison Request Cancel: CADV 
 
MODIFICATIONS/EVENTS BASED ON YOUR TRADES 
These MT518s primarily reflect your trade records after changes have been made. In the majority of cases, the 
changes have been made by RTTM to your trade. They are also used to reflect changes made by the 
submitting party to RTTM via terminal input.  
The following MT518s reflect modifications or events based on your trade: 
• Cancel Request (of already compared trade): CREQ 
• Cancel Request Modify (of already compared trade): MCRQ 
• Cancel Request Cancel (of already compared trade): CCRQ 
• DK Advice: NAFI 
• DK Remove Advice: DCCX 
• Screen Input Trade Replay: SITR 
• Screen Input Set Replay: SISR 
• DNA Assigned: DNAP 
• Screen Input DNA Replay: SDNA 
• Trade Novated: NOVT 
• Post Comparison Trade Modification: MDAD 
 
This section is organized in the following manner: 
• Section 4.4.1: General Format 
• Section 4.4.2: Field Specifications 
• Section 4.4.3: Field Analysis (Advisories) 
• Section 4.4.4: Field Analysis (Advices Referring to your Trades) 
Note: 
The Field Analysis section contains an analysis of the fields that may be found on each MT515 message. For each record 
type, a check mark will be found where it is possible for that field to appear on that record. It should be noted,  however, that 

---

## Page 79

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 79 
where a check mark appears, the check mark is not intended to indicate that a field is mandatory for a given record type. 
Where there is no check mark in a given box, that field is not applicable for the record type in question.  
4.4.1 MT518 General Format 
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
M :23G: NEWM  Msg Function = New or  4!c[/4!c] 
  CANC [/COPY] Cancel   
O :98C: :PREP//  Preparation Date/Time YYYYMMDDHHMMSS 
M :22F: :TRTR/ GSCC/CASH Cash Buy/Sell Trade Indicator  4!c 
M :16R: LINK  Repeat Block Start  
O :20C: :MAST//  Master Reference Number  
(External Reference)  
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PREV//  Previous Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :LIST//  RTTM Assigned Reference 16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :BASK//  [[Broker]] Reference Number  16x 
M :16S: LINK  Repeat Block End  
M :16S: GENL  Block End  
M :16R: CONFDET  Block Start  
M :98C: :TRAD//  Trade Date & Time YYYYMMDDHHMMSS 

---

## Page 80

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 80 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
M :98A: :SETT//  [[settlement]] Date YYYYMMDD 
M :90A: :DEAL/ /PRCT/ Deal Price–Percentage 15d 
O :19A: :SETT//  /USD [[settlement]] Amount  15d 
M :22H: :BUSE/ /BUYI Trade Type– Buy or 4!c 
   /SELL Sell  
O :22F: :PROC/ GSCC/CMPR Comparison Request or  4!c 
   GSCC/CRQM Comparison Request Modify or   
   GSCC/CADV Comparison Request Cancel or   
   GSCC/CREQ Cancel Request or  
   GSCC/MCRQ Cancel Request Modify or   
   GSCC/CCRQ Cancel Request Cancel or   
   GSCC/NAFI DK Advice or  
   GSCC/DCCX DK Remove Advice or  
   GSCC/SITR Screen Input Trade Replay or  
   GSCC/SISR Screen Input Set Replay or   
   GSCC/MDAD Post Comparison Modification  
Advice  
 
   GSCC/DFVA [[default]] Values Applied or  
   GSCC/YTPR Repricing or  
   GSCC/NOVT Trade Novated or  
   GSCC/DNAP DNA Assigned or  
   GSCC/SDNA Screen Input DNA Replay   
M :22H: :PAYM/ /APMT Against Payment Indicator  4!c 
O :22F: :CATB/ /PERU Per Unit Charges Indicator  4!c 
M :16R: CONFPRTY  Repeat Block Start  
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]] 34x 
O :20C: :PROC//  [[Buyer]] (Contra) Transaction Ref.  16x 
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative 4*35x 
   /TDID Trader [[ID]] 20c 
O :70E: :DECL/ /GSCC [[participant]] Declaration Details  
Narrative 
10*35x 

---

## Page 81

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 81 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
   /CTRD [[Buyer]] (Contra) Trade Reference 10c 
   /FAMT Individual Par amount to DNA  15d 
   /PRCT Individual Price to target for DNA  15d 
   /TDDT Individual Trade Date to target for 
DNA 
YYYYMMDD 
   /TRID Individual Trade [[ID]] to target for DNA  16x 
M :16S: CONFPRTY  Repeat Block End  
M :16R: CONFPRTY  Repeat Block Start  
M :95R: :SELL/ GSCC/PART Party = [[Seller]]  34x 
O :20C: :PROC//  [[Seller]] (Contra) Transaction Ref.  16x 
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative 4*35x 
   /TDID Trader [[ID]] 20c 
O :70E: :DECL/ /GSCC [[participant]] Declaration Details  
Narrative 
10*35x 
   /CTRD [[Seller]] (Contra) Trade Reference 10c 
   /FAMT Individual Par amount to DNA  15d 
   /PRCT Individual Price to target for DNA  15d 
   /TDDT Individual Trade Date to target for  YYYYMMDD 
   /TRID Individual Trade [[ID]] to target for DNA  16x 
M :16S: CONFPRTY  Repeat Block End  
M :36B: :CONF/ /FAMT/ Quantity as Face Amount (Par)  15d 
M :35B: /US/  Security Identifier –[[CUSIP]] 4 * 35x 
M :16R: FIA  Block Start  
O :12B: :OPTI/ /CALL [[Call option]] Type or  4!c 
   /PUTO [[Put Option]] Type   
O :98A: :EXPI//  Expiry Date YYYYMMDD 
 O :13B:  :POOL/  GSCC/  Pool Number  9x 
M :16S: FIA  Block End  
O :70E: :TPRO/ /GSCC Trade Instruction Processing 
Narrative 
10*35x 
   /TDSVSBOD Trade Service Type– SBOD or 4!c 

---

## Page 82

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 82 
M/ 
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format  
   /TDSVTFTD Trade Service Type– Trade for Trade 
or 
 
   /TDSVSTIP Trade Service Type – STIP or  
   /TDSVOPTN Trade Service Type– [[Option]]  
   /MSGR Message Reason (see table) 4!c 
   /DKRS DK Reason (see table) 4!c 
   /GUPP Give Up Period  2n 
M :16S: CONFDET  Block End  
M :16R: SETDET  Block Start  
M :22F: :SETR/ /RPTO Indicator = Reporting Purposes  4!c 
O :17B: :STAN/ /N Standing Instruction Override = No  1!a 
M :16R: AMT  Block Start  
M :19A: :LOCO//USD  Commission Amount  15d 
M :16S: AMT  Block End  
M :16S: SETDET  Block End  
 
Message Reason Codes 
DKTD Due to DK 4!c 
DCTD Due to DK Remove  
MACH Due to Match   
COAC Due to Contra Action  
GSAC Due to RTTM Action   
YRAC Due to Your Action   
 
DK Reason Codes 
E004 Unknown Security  4!c 
E005 Bad Quantity   
E006 Bad Trade Date  
E007 Bad [[settlement]] Date  
E008 Bad Price  
E010 Bad [[Buyer]] Party   

---

## Page 83

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 83 
DK Reason Codes 
E011 Bad [[Seller]] Party   
E013 Transaction Type Error   
E014 Price Method Error   
E015 Commission Error   
E100 Unknown Cancel   
E101 Give Up Period Error   
E102 Trade Service Type Error   
E103 [[Option]] Type Error   
E104 [[Option]] Expiry Date Error   
E106 Incorrect Account Symbol   
E107 Duplicate Trade  
E108 Invalid Pool Identifier   
E998 Trade not found  
E999 Other Bad Data  
Note: 
E101 is not used for [[Novation]] Eligible trades  
4.4.2 MT518 Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a message header. All header fields are mandatory fixed format 
with trailing blanks, where required.  
Password 12!c Password fields will be blank filled on MT518 messages.  
Sender 8!c MBSCTRRS (MBSD Trade Registration and Reconciliation System) will always be the 
sender of the MT518 messages.  
Message Type 3!n/3!n/4!c  The first three characters indicate to the recipient the message type (518); the second 
three positions reflect the version of the message interface (currently always 000). The 
last four characters indicate the [[issuer]] code to be used in the message (“GSCC”).  
Receiver 8!c MBSD account number of the [[participant]] receiving the message.  
GENL This mandatory block provides general information regarding the message. It appears only 
once in a Trade Confirm.  
20C Sender Message Reference 
• SEME//: This mandatory field contains the sender’s (RTTM) message reference number.  It is 
used on all messages sent by RTTM and will contain a unique number to unambiguously 
identify each message. (This is a communications message number, not a trade number.)  

---

## Page 84

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 84 
Block/Tag Notes 
Note: 
While the SWIFT message accommodates both upper and lower case alphanumeric and certain 
symbols, for RTTM purposes, this field will be populated with an upper case alphanumeric value. It will 
not contain symbols or hyphens.  
e.g., :20C::SEME//MBSDCOMREF1 
23G Function of the Message 
This mandatory field identifies the function of the message. It will either be a new message (NEWM) 
or a cancellation of a previous message (CANC):  
• NEWM: This NEWM qualifier will be used on the following MT518 messages:  
− Comparison Requests and Comparison Request Modifies;  
− Screen Input Trade Replays that reflect a Trade Create, or a Modify submitted via 
terminal;  
− Screen Input DNA Replays that reflect a DNA Create submitted via terminal;  
− Screen Input Set Replays that reflect a Modify Set submitted via terminal;  
− DK Advices and DK Remove Advices where the receiver of such advices is the submitter 
of a Trade Create that is being DKed  
− Post Comparison Modification Advices; and 
− DNA Assigned messages  
• CANC[/COPY]: This CANC qualifier will be used on the following MT518 messages:  
− Cancel Requests, Cancel Request Modifies and Cancel Request Cancels;  
− Comparison Request Cancels;  
− Screen Input Trade Replays that reflect a Cancel submitted via terminal;  
− Screen Input DNA Replays that reflect a DNA Cancel submitted via terminal;  
− Screen Input Set Replays that reflect a Cancel Set submitted via terminal; and  
− DK Advices and DK Remove Advices where the receiver of such advices is the submitter 
of a Cancel (or Cancel Set) Message that is being DKed.  
Note: 
When a Dealer submits an MT515 Cancel Message for a fully matched (FMAT) brokered trade, MT518 
messages related to this cancel are also sent to the [[Broker]] for informational purposes only. The 
informational nature of these messages will be reflected on the MT518 messages by adding "/COPY"  
to this field. At this time, the “/COPY” suffix can be used for MT518 Cancel Request, DK (Cancel) 
Advice, DK (Cancel) Remove Advice and Cancel Request Cancel messages.  
e.g., :23G:NEWM 
98C Preparation Date and Time 
• PREP//: This field will be reflected on all messages to indicate the date and time the message 
was prepared by RTTM.  
Notes: 
The “C” format for this (98) tag indicates a date/time format of “YYYYMMDDHHMMSS”.  
e.g., :98C::PREP//20011218143947 
22F Trade Transaction Type Indicator (TRTR)  
Since MBSD trades are bilateral cash (buy/sell) trades, this mandatory field will only contain the value 
indicated below at this time.  

---

## Page 85

MBSD RTTM® [[Novation]] :  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 85 
Block/Tag Notes 
• TRTR/GSCC/CASH-This qualifier/[[Option]] will be used on all MT518 messages to specify that they 
refer to buy/sell trades requiring two -sided comparison.  
e.g., :22F::TRTR/GSCC/CASH  
LINK The LINK Block will be repeated for as many reference qualifiers as need to be included in a 
Trade Confirm. It is intended to provide the required information to identify the trade. Each 
reference number must be enclosed within a Start Link Block (:16R:LINK) and End Link Block 
(:16S:LINK). Each LINK repeating subsequence is within the GENL Block.  
20C Reference 
The following reference qualifiers can be found on MT518 records:  
• MAST//: Master Reference Number  - This qualifier will contain the external reference number 
(x-ref) of the transaction/trade or DNA represented on the record. The field will be populated:  
− on all  MT518 records going to the original submitter of the transaction, and  
− only when the x -ref on a transaction or trade is still applicable.  
(e.g., MT518’s sent to Dealers reflecting their (post comparison) trades will only continue to 
contain an x -ref if the trade was compared via exact match. MT518’s sent to Brokers 
referring to the transactions they submitted will only have an x -ref when the record refers to 
one side of a transaction.)  
• PREV//: Previous Reference Number  - This qualifier will be reflected on all MT518 records 
sent to the original submitting party which are related to modifications of reference numbers. 
(The only exception to this rule is for records related to modifications of [[Broker]] Reference 
Number “prebalancing. ” On these records, only the Current [[Broker]] Reference will be reflected; 
the Previous [[Broker]] Reference, however, will not be reflected on these records.)  
The PREV qualifier will also be reflected on all Cancel MT518 records. The PREV qualifier will 
be populated on MT518 records as fol lows:  
− On all Cancel and Cancel Set records (:23G:CANC), this field will be populated with the value 
“NONREF”. 
− - For (post balancing) records related to [[Broker]] submissions, this field will reflect the Previous 
[[Broker]] Reference of the [[Broker]].  
• LIST//: RTTM Reference Number  - On MT518 messages referring to your trades, this field will 
contain the RTTM assigned reference number. On MT518 messages referring to your  DNA 
Requests, this field will contain the RTTM assigned DNA [[ID]].  For all other events transaction or  
trade [[ID]] (or for the [[Broker]]’s submission before balancing) will be used. This field will not appear 
on Comparison Requests, Comparison Request Modifies or Comparison Request Cancels.  
[[participant]] Type Comparison Status  RTTM Reference Number  
Dealer Pre-Comparison Transaction [[ID]]  
 Post-Comparison  Trade [[ID]] (Tran [[ID]])  
[[Broker]]  Pre-Balancing  Submission [[ID]]  
 Post-Balancing  
Pre-Comparison 
Transaction [[ID]]  
 Post-Comparison 
(PMAT and FMAT)  
Transaction [[ID]] (PMAT only) or Trade [[ID]] 
(PMAT and FMAT)  
 

---

## Page 86

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 86 
Block/Tag Notes 
 
Note: 
On Comparison Requests, Comparison Request Modifies and Comparison Request Cancels, 
the contraparty’s RTTM transaction reference is provided in the appropriate [[Buyer]] or [[Seller]] 
Confirming Party subsequence, and not in this LINK subsequence 
• BASK//: [[Broker]]-Related Reference Number  - This qualifier contains a [[Broker]] -specified  
[[Broker]] reference number , or RTTM assigned [[Broker]] match identifier , depending on [[participant]] 
type. With the exception of the below scenarios, the field will be blank.  
[[participant]] Type BASK Reference Number  
[[Broker]]  Any MT518 message that is received by a [[Broker]] and that refers 
to one of his trades will reflect the [[Broker]] Reference Number in 
this field.   
Dealer This field contains an RTTM assigned [[Broker]] Match Identifier, 
used to associate the set of dealer trade(s) and [[Broker]] 
advisory(s) involved in a match. It will appear on MT518 
Comparison Request Advisory (due to match) and MT518 Trade 
Novated messages only, and is populated in any match event 
versus a [[Broker]] trade, regardless of whether matched via Net 
Position (split/splice) or exact match.  
Note: 
While the SWIFT message accommodates both upper and lowercase alphanumeric and certain 
symbols, for MBSD purposes, this field will be populated with an uppercase alphanumeric value. It will 
not  contain symbols or hyphens, except where the reference number has been assigned by RTTM.  
e.g., :20C::MAST//PARTREF1 
CONFDET The mandatory CONFDET (Confirmation Details) block appears only once in a Trade  Confirm. It 
contains Trade and Confirming Party Details.  
98C Trade Date 
TRAD//: This qualifier is used as indicated below.   
Message Type TRAD Field Value 
DNA (screen replay and  
assigned)  
The field is populated with a value of December31st 9999 
and a time of 00:00:00. 
All other MT515 The value is populated with the Trade Date and Trade Time.  
Note: 
The “C” format for this (98) tag indicates a date/time format of “YYYYMMDDHHMMSS”.  
e.g., :98C::TRAD//20141218095510 
:98C::TRAD//99991231000000 
98A [[settlement]] Date 
• SETT//: This field is used on all messages to specify the [[settlement]] date. The “A” format for 
this tag (98) indicates a date format of “YYYYMMDD”.  

---

## Page 87

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 87 
Block/Tag Notes 
− For TFTD trades  and DNA requests , this field will be populated with the full contractual 
[[settlement]] date (YYYYMMDD). 
− For SBOD and OPTN trades, however, the day (“DD”) will always be populated with  “01” 
(by convention using a format of “YYYYMM01”).  
e.g., :98A::SETT//20011219 
90A Deal Price 
This field is reflected on all MT518 messages. The price is expressed as a decimal number in SWIFT 
Standard format, which is left justified, with commas removed, and a comma used instead of a 
decimal.  
• DEAL//PRCT/: This qualifier/[[Option]] is used for dollar prices, expressed as a decimal number.  
− If the original trade was submitted by a Dealer and a commission based on a rate is to be paid, 
the following scenarios occur:  
− Pre-comparison: The Deal Price populated on the MT518 message will reflect the price 
entered on the original trade create.  
− Post-comparison: The Deal Price will not in corpor ate the commission in this field on the 
MT518 message.  
− If the original trade was submitted by a [[Broker]] and a commission based on a rate is to be 
paid, then the Deal Price will not incorporate the commission in this field on the MT518 
messages.  
− F or DNA (Screen Replay and DNA Assigned) , the price will always be equal to 0 
e.g., :90A::DEAL//PRCT/99,625 
19A [[settlement]] Amount  
SETT//: This field is used to specify the [[settlement]] Amount for trades . 
The Amount is in SWIFT Standard format, whi ch is left justified, with commas removed, and a comma 
used in lieu of a decimal.  The amount is always preceded by a 3- character ISO currency code (“USD” 
for MBSD trades).  
Message Type SETT// Field Value  
DNA (Assigned and Screen 
Replay)  
This qualifier is omitted.  
All other MT515 If trade is an SPT, this value contains the final money based 
on the most recent factor in members’ systems.  
For non- SPT trades, the value is calculated based on a 
factor of 1.0. 
Note: 
The SWIFT format can accommodate a value of 15d in this field.   
e.g., :19A::SETT//USD2000000, 
22H Trade Type Indicator (BUSE)  
This field is reflected on all MT518 messages and will be set as follows:  
Message Type BUSE// Field Value 

---

## Page 88

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 88 
Block/Tag Notes 
Screen Input Set Replays,  
DNA (Assigned and Screen 
Replay)  
The value will be set to “BUSE//BUYI”.  
All other MT518 Options are:  
• BUSE//BUYI–The trade reflected is a buy.  
• BUSE//SELL–The trade reflected is a sell.  
e.g., :22H::BUSE//SELL 
22F Processing Indicator (PROC)  
This Processing Indicator  enables RTTM to indicate to the [[participant]] the type of record/command 
being submitted on this MT518.  
The allowable values for this field are:  
• PROC/GSCC/CMPR: This qualifier/[[Option]] indicates that the MT518 record is a Comparison 
Request. 
• PROC/GSCC/CRQM: This qualifier/[[Option]] indicates that the MT518 record is a Comparison 
Request Modify.  
• PROC/GSCC/CADV: This qualifier/[[Option]] indicates that the MT518 record is a Comparison 
Request Cancel (pre- comparison).  
• PROC/GSCC/CREQ: This qualifier/[[Option]] indicates that the MT518 record is a Cancel  Request 
(of an already compared trade).  
• PROC/GSCC/MCRQ: This qualifier/[[Option]] indicates that the MT518 record is a Cancel  
Request Modify.  
• PROC/GSCC/CCRQ: This qualifier/[[Option]] indicates that the MT518 record is a Cancel  Request 
Cancel.  
• PROC/GSCC/NAFI: This qualifier/[[Option]] indicates that the MT518 record is a DK Advice.  
• PROC/GSCC/DCCX: This qualifier/[[Option]] indicates that the MT518 record is a DK Remove 
Advice.  
• PROC/GSCC/SITR: This qualifier/[[Option]] ind icates that the MT518 record is a Screen  Input 
Trade Replay (applicable to screen inputs of Instruct, Modify, or Cancel records).  
• PROC/GSCC/SISR: This qualifier/[[Option]] indicates that the MT518 record is a Screen Input Set 
Replay (applicable only to [[Broker]] screen inputs of Cancel Set and Modify Set records.)  
• PROC/GSCC/MDAD: This qualifier/[[Option]] indicates that the MT518 record is a Post  
Comparison Modification Advice (of the recipient’s trade).  
• PROC/GSCC/NOVT: This qualifier/[[Option]] indicates that the MT518 record is a Trade Novated 
record.  
• PROC/GSCC/DNAP: This qualifier/[[Option]] indicates that the MT518 record is a DNA Assigned 
record.  
• PROC/GSCC/SDNA: This qualifier/[[Option]] indicates that the MT518 record is a Screen Input 
Replay for DNA (applicable to screen inputs of DNA Create or Cancel records)  
e.g., :22F::PROC/GSCC/CRQM  
22H Payment Indicator (PAYM)  
This Payment Indicator field is mandatory for the MT518 message. All MT518 records will reflect the 
following qualifier/tag:  
• PAYM//APMT: This qualifier/[[Option]] indicates that the trade will settle against payment.  
e.g., :22H::PAYM//APMT 
22F Charges Indicator (CATB)  

---

## Page 89

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 89 
Block/Tag Notes 
This indicator will be reflected on all MT518 messages that contain a commission amount per trade in 
field :19A::LOCO//USD of the Amount (AMT) subsequence within the Sett lement Details (SETDET) 
block. This field indicates a commission rate that was applied and has the following value:  
• CATB//PERU: This qualifier/[[Option]] indicates that the commission amount indicated on the 
message is the result of a commission rate.   
e.g., :22F::CATB//PERU  
36B Quantity of [[securities]] (CONF)  
• CONF//FAMT/: This field is mandatory, and for the purposes of RTTM, the [[Option]] ‘FAMT’ : 
indicating face amount (par) will be used.  
Message Type CONF//FAMT Field Value  
DNA related  The value reflects the SUM value of buy par included in the 
DNA set which should be equal to SUM value of sell par.  
All other MT518 The value reflects the face amount, noting that for Specified 
Pool Trades, this is populated with the Original Face Value 
of the trade. 
Note: 
This tag and the following tag are placed on the message following the confirming party subsequences 
described below.  
e.g., :36B::CONF//FAMT/2000000,  
35B Identification of Security  
The security (TBA) involved is identified in the US by specifying the ISO country identifier  (‘/US/’), 
followed by the [[CUSIP]] number.  
Note: 
While the SWIFT layout accommodates a format of 4 * 35x, a 9!c (alpha numeric) value will populate 
the field for the TBA [[CUSIP]]. 
e.g., :35B:/US/01F070641 

---

## Page 90

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 90 
Block/Tag Notes 
70E Trade Instruction Processing Narrative (TPRO)  
This field will be on all MT518 messages  except DNA-related messages  and will be used to reflect 
trade-related information not supported in the MT518 format : it will be used to reflect a trade service 
type, a message reason, a DK reason, and the give- up period, where appropriate.  
TPRO//GSCC: denotes narrative information specific to MBSD.  
One Trade Service Type will be included on each MT518 message:  
• /TDSVSBOD: will be used for SBOD trades.  
• /TDSVTFTD: will be used for TFTD trades  
• /TDSVSTIP: will be used for STIP trades.  
• /TDSVOPTN: will be used for OPTN trades.  
MT518 Advisories can contain a message reason to further define an event on RTTM.  
• /MSGR: specifies the message reason –a table with message reasons is attached to the layout.  
All DK and DK Remove advices will contain a DK Reason:  
• /DKRS: specifies the DK reason (on DK Messages only) –a table with DK reasons is attached 
to the layout  
All records reflecting [[Broker]] input will contain the give up period:  
• /GUPP: indicates the number of days (0- 9) in the give -up period.  *This field will not be used 
for [[Novation]] eligible trades. * 
Note: 
This tag will be placed on the me ssage within the Confirmation Details (CONFDET) Block following the 
FIA subsequence described below.  
e.g., :70E::TPRO//GSCC/TDSVTFTD  
CONFPRTY The Mandatory Confirming Party Block will be repeated for each party to a trade. Each party specified 
will be enclosed within a Start Party block (:16R:CONFPRTY) and an End Party block 
(:16S:CONFPRTY). 
Notes: 
• Screen Input Set and Cancel DNA Replay Messages will contain only one Confirming 
Party sequence (by convention, this is the [[Buyer]] Confirming Party sequence, reflecting 
the information pertaining to the [[Broker]] /Dealer).  
• For DNA Assigned and Screen Input DNA Replay Messages, the Confirming Party block 
contains information on the position to target and par amount to DNA; this block will 
be repeated for each buy/sell term in the request. As a DNA must have at least one buy 
and one sell, a minimum of two repeating Confirming Party blocks must appear in the 
message. 
• All other MT518 messages will contain two repeating Confirming Party sequences (one 
[[Buyer]] and one  [[Seller]], and one of these parties will also be the receiver of the MT518 
message). 

---

## Page 91

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 91 
Block/Tag Notes 
95R Party 
• BUYR/GSCC/PART: specifies the Buying Party on all MT518 messages except on Screen 
Input Set Replay Messages, where this field always specifies the information pertaining to the 
[[Broker]] (the “GSCC” [[issuer]] code allows the specification to include the MBSD account number 
of the [[participant]] or the contra, depending on who is acting as [[Buyer]] or [[Seller]]).  
• SELL/GSCC/PART: specifies the Selling Party on all MT 518 messages except on Screen 
Input Set Replay Messages, where the [[Seller]] Confirming Party sequence is omitted.  
As previously noted, Brokers will always be reflected either as [[Buyer]] or as [[Seller]] on any given  MT518 
message (with the exception of the Screen Input Set Replay (SISR) Message).  
Note: 
While the SWIFT layout supports a format of 35x for this field, this field will be populated with the 
appropriate 4 -character MBSD [[participant]] Account, for [[Buyer]] or [[Seller]].  
e.g., :95R::BUYR/GSCC/PARTABCD  
20C Contra Transaction Reference (PROC)  
• PROC//: Processing Reference Number - This field will reflect the RTTM assigned Contraparty 
Transaction Reference in the appropriate [[Buyer]] or [[Seller]] Confirming Party subsequence. It will 
only appear on Comparison Requests, Comparison Request Modifies and Comparison 
Request Cancels.  
e.g., :20C::PROC//7096000001 
70C [[participant]] Contact Narrative (PACO)  
This optional field will be reflected on advisories to identify party contact infor mation for the [[Buyer]] or 
[[Seller]] party.  
• PACO//GSCC: denotes [[participant]] contact narrative information specific to RTTM.  
• /TDID: will be used in the appropriate BUYR or SELL Confirming Party sequence to indicate 
the receiver’s trader [[ID]] of the individual that executed the trade. Where provided on the original 
MT515 submitted by an Electronic Trading System, the Trader [[ID]] will be passed along to the 
Dealer on the Request for Comparison advisory. This should enable the Dealer to [[Locate]] where 
to direct this advisory should it not match.  
Note: 
While this field can support a narrative 4 * 35x, the [[participant]], at this time, will only receive the above 
qualifier and related value in this field.  In the future, this narrative field can be used to support 
additional information related to the [[Buyer]] or [[Seller]], where required.  
e.g., :70C::PACO//GSCC/TDIDTRADER007  
70E Declaration Narrative (DECL)  
This optional field will be reflected on Comparison Request Cancel (due to match) records to reflect 
narrative information related to either the [[Buyer]] or [[Seller]] party . In addition, this field denotes financial 
amount information related DNA requests (screen input replay and assigned), providing details on 
each DNA term specified and assigned trade IDs. 
• DECL//GSCC: denotes narrative information spec ific to RTTM. 
• /CTRD: will be used in the Contra’s BUYR or SELL Confirming Party Sequence to enable the 
receiving party to identify the Trade created as a result of matching the Transaction referred to 
on this record (PROC in this sequence).  In other words,  the Trade [[ID]] assigned to the 

---

## Page 92

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 92 
Block/Tag Notes 
receiving/contraparty trade upon matching/[[Novation]].  As previously indicated , this will be found 
only on Comparison Request Cancel (due to match) Records.  
• /FAMT: the face quantity (par) in the DNA.  
• /PRCT: the price of the trade  in the DNA, to 9 decimal places.  
• /TDDT: the trade date of the trade in the DNA, in format YYYYMMDD  
• /TRID: the Trade [[ID]] of the targeted trade in the DNA  
e.g., :70E::DECL//GSCC/CTRD2049000001 
FIA This Optional Block will be included for Specified Pool Trades to identify the specific pool 
traded (where :70E::TPRO//GSCC/TDSVTFTD or :70E::TPRO//GSCC/TDSVTFTD) or OPTN 
trades (where :70E::TPRO//GSCC/TDSVOPTN).  
12B [[Option]] Type (OPTI)  
• OPTI//CALL–indicates that a [[Call option]] on the underlying [[CUSIP]] was traded.  
• OPTI//PUTO–indicates that a [[Put Option]] on the underlying [[CUSIP]] was traded.  
e.g., :12B::OPTI//CALL  
98A Expiry Date (EXPI) 
• EXPI//: specifies the expiry date of the (put or call) [[Option]]. The “A” format for this tag (98) 
indicates a date format of “YYYYMMDD”. 
e.g., :98A::EXPI//20010918 
13B Number Identification  
• POOL/GSCC/: will be used by RTTM to identify the pool number traded.  Pool number will be 
used in conjunction with the TBA [[CUSIP]] to ensure security identifier uniqueness.   
Note: 
The Pool number will be returned, regardless of whether the pool was identified by Pool [[CUSIP]] in the 
original submission or not.  
e.g., :13B::POOL/GSCC/123456  
SETDET This Optional Block, and the AMT subsequence, will only be included when the  Commission 
Amount field is populated.  
22F [[settlement]] Indicator (SETR)  
This field is SWIFT Mandatory for the Block.  
• SETR//RPTO-Indicates that this trade confirmation is for reporting purposes only.  
Note: 
Although it is SWIFT -mandatory, t his field is not used by RTTM in order to support the inclusion of the 
Commission Amount field.  
e.g., :22F::SETR//RPTO  

---

## Page 93

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 93 
Block/Tag Notes 
17B Standing Instructions Override  
• STAN//N: This indicates that standing instructions will not be overridden . *This field will not 
be specified for [[Novation]] -eligible trades.* 
Note: 
This field, previously mandatory for SWIFT, is no longer used for [[Novation]] eligible trades.  
e.g., :17B::STAN//N  
AMT As indicated above, this Optional sequence is only necessary to support the inclusion of a 
[[Broker]] commission on a trade. When used, this block will always be included within the 
[[settlement]] Details (SETDET) block.  
19A Commission Amount  
• LOCO//USD: This field specifies the [[Broker]]’s commission amount PER TRADE in USD that 
has been applied to that specific trade. The Commission Amount field is in SWIFT Standard 
Format, which is left justified, with commas removed, and a comma used in lieu of a decimal.  
− If a commission rate was charged on a trade, then this field will reflect a commission amount 
per trade for the following:  
 MT518 messages relating to Trade Creates originally submitted by a [[Broker]],  
 Pre-comparison: MT518 messages relating to Trade Creates originally submitted by a 
Dealer if the Trade Create contained a commission amount.  
 Post-comparison: MT518 messages received by both Dealers and Brokers.  
− If a commission amount is reflected in this field, the Confirmation Details (CONFDET) Block 
will reflect:  
 :22F::CATB//PERU 
Note: 
The value in this field is the commission Amount that must be paid to the [[Broker]] : e.g., if a commission 
rate of 1/512 is charged on a two -million -dollar trade, then the Commission Amount field will be 
displayed as “LOCO//USD39,06”  
e.g., :19A::LOCO//USD39,06  
4.4.3 MT518 Field Specifications 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
    Message Header    
    Password     
    Sender     
    Message Type    
    Receiver     
M :16R: GENL  Start of Block    

---

## Page 94

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 94 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
M :20C: :SEME//   Sender’s Reference for this 
message 
   
M :23G: NEWM  Message Function = New or     
  CANC [/COPY] Cancel     
O :98C: :PREP//  Preparation Date/Time    
M :22F: :TRTR/ GSCC/CASH Cash Buy/Sell Trade 
Indicator  
   
M :16R: LINK  Start of Optional 
Repetitive Subsequence 
   
O :20C: :MAST//   Master Reference Number     
M :16S: LINK  End of Block    
M :16R: LINK  Start of Optional 
Repetitive Subsequence 
   
O :20C: :PREV//   Previous Reference Number     
M :16S: LINK  End of Block    
M :16R: LINK  Start of Optional 
Repetitive Subsequence 
   
O :20C: :LIST//   RTTM Reference Number    
M :16S: LINK  End of Block    
M :16R: LINK  Start of Optional 
Repetitive Subsequence 
   
O :20C: :BASK//   [[Broker]] Reference Number      
M :16S: LINK  End of Block    
M :16S: GENL  End of Block    
M :16R: CONFDET  Start of Block    
M :98C: :TRAD//   Trade Date/Time    
M :98A: :SETT//   [[settlement]] Date    
M :90A: :DEAL/  /PRCT/ Deal Price- Percentage    
O :19A: :SETT/ /USD [[settlement]] Amount     
M :22H: :BUSE/ /BUYI  Trade Type Buy or     
   /SELL Sell    
O :22F: :PROC/ GSCC/CMPR Comparison Request or     
   GSCC/CRQM Comparison Request Modif y 
or 
   

---

## Page 95

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 95 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
   GSCC/CADV Comparison Request 
Cancel or  
   
   GSCC/CREQ Cancel Request or     
   GSCC/MCRQ Cancel Request Cancel or     
   GSCC/CCRQ Cancel Request Modify or     
   GSCC/NAFI DK Advice or     
   GSCC/DCCX DK Remove Advice or     
   GSCC/SITR Screen Input Trade Replay 
or 
   
   GSCC/SISR Screen Input Set Replay     
   GSCC/MDAD Post Comparison 
Modification Advice or  
   
   GSCC/DFVA [[default]] Values Applied     
   GSCC/YTPR Repricing     
   GSCC/NOVT Trade Novated     
   GSCC/SDNA Screen Replay DNA     
   GSCC/DNAP DNA Assigned     
M :22H: :PAYM/ /APMT Against Payment Trade    
O :22F: :CATB/ /PERU Per Unit Charges Indicator 
or 
   
M :16R: CONFPRTY  Start of Repetitive 
Mandatory Subsequence  
   
M :95R: :BUYR/ GSCC/PART Buying Party     
O :20C: :PROC//  [[Buyer]] (contra) trs. reference     
O :70C: :PACO/ /GSCC [[participant]] Contact 
Narrative 
   
   /TDID Trader [[ID]]    
O :70E: :DECL/ /GSCC [[participant]] Declaration 
Details Narrative 
   
   /CTRD [[Buyer]] (Contra) Trade 
Reference 
   
   /FAMT Individual Par for DNA     
   /PRCT Individual Price for DNA     

---

## Page 96

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 96 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
   /TDDT Individual Trade Date for 
DNA 
   
   /TRID Individual Trade [[ID]] to target 
for DNA 
   
M :16S: CONFPRTY  Repeat Block End    
M :16R: CONFPRTY  Start of Repetitive 
Mandatory Subsequence  
   
M :95R: :SELL/ GSCC/PART Selling Party     
O :20C: :PROC//   [[Seller]] (contra) trs. reference     
O :70C: :PACO/ /GSCC [[participant]] Contact 
Narrative 
   
   /TDID Trader [[ID]]    
O :70E: :DECL/ /GSCC [[participant]] Declaration 
Details Narrative 
   
   /CTRD [[Seller]] (Contra) Trade 
Reference 
   
   /FAMT Individual Par for DNA     
   /PRCT Individual Price for DNA     
   /TDDT Individual Trade Date for 
DNA 
   
   /TRID Individual Trade [[ID]] to target 
for DNA 
   
M :16S: CONFPRTY  Repeat Block End    
M :36B: :CONF/ /FAMT/ Quantity as Face Amount –
Original Face Value (Par)  
   
M :35B: /US/  Identification of Financial 
Instrument : TBA [[CUSIP]] 
   
M :16R: FIA  Start of Optional 
Subsequence 
   
O :12B: :OPTI/ /CALL [[Call option]] Type or     
   /PUTO [[Put Option]] Type     
O :98A: :EXPI//  Expiry Date    
O :13B: :POOL/ GSCC/ Pool Number    
M :16S: FIA  End of Optional 
Subsequence 
   

---

## Page 97

MBSD RTTM® [[Novation]]:  
SWIFT Interac tive Messaging Specifications  
Version C ontrol Page 97 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
O :70E: :TPRO/ /GSCC Trade Instruction 
Processing Narrative 
   
   /TDSVSBOD Trade Service– SBOD or    
   /TDSVTFTD Trade Service– TFTD or    
   /TDSVSTIP Trade Service – STIP or    
   /TDSVOPTN Trade Service– OPTN    
   /MSGR Message Reason     
   /DKRS DK Reason     
M :16S: CONFDET  End of Block    
M :16R: SETDET  Start of Optional 
Sequence 
   
M :22F: :SETR/ /RPTO Indicator = Reporting 
Purposes  
   
O :17B: :STAN/ /N Standing Instructions 
Override  
   
M :16R: AMT  Start of Repetitive 
Optional Subsequence  
   
M :19A: :LOCO/ /USD Commission Amount     
M :16S: AMT  End of Block    
M :16S: SETDET  End of Block    
4.4.3 MT518 Field Analysis (Advisories) 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
    Message Header    
    Password     
    Sender     
    Message Type    
    Receiver     
M :16R: GENL  Start of Block    
M :20C: :SEME//   Sender’s Reference for this 
message 
   
M :23G: NEWM  Message Function = New or    

---

## Page 98

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 98 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
  CANC [/COPY] Cancel     
O :98C: :PREP//  Preparation Date/Time    
M :22F: :TRTR/ GSCC/CASH Cash Buy/Sell Trade Indicator     
M :16R: LINK  Start of Optional Repetitive 
Subsequence 
   
O :20C: :MAST//   Master Reference Number     
M :16S: LINK  End of Block    
M :16R: LINK  Start of Optional Repetitive 
Subsequence 
   
O :20C: :PREV//   Previous Reference Number     
M :16S: LINK  End of Block    
M :16R: LINK  Start of Optional Repetitive 
Subsequence 
   
O :20C: :LIST//   RTTM Reference Number    
M :16S: LINK  End of Block    
M :16R: LINK  Start of Optional Repetitive 
Subsequence 
   
O :20C: :BASK//   [[Broker]] Reference Number      
M :16S: LINK  End of Block    
M :16S: GENL  End of Block    
M :16R: CONFDET  Start of Block    
M :98C: :TRAD//   Trade Date/Time    
M :98A: :SETT//   [[settlement]] Date    
M :90A: :DEAL/  /PRCT/ Deal Price- Percentage    
O :19A: :SETT/ /USD [[settlement]] Amount     
M :22H: :BUSE/ /BUYI  Trade Type Buy or     
   /SELL Sell    
O :22F: :PROC/ GSCC/ 
CMPR 
Comparison Request or     
   GSCC/ 
CRQM 
Comparison Request Modify or     
   GSCC/CADV Comparison Request Cancel or     
   GSCC/ 
CREQ 
Cancel Request or    

---

## Page 99

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 99 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
   GSCC/ 
MCRQ 
Cancel Request Cancel or     
   GSCC/ 
CCRQ 
Cancel Request Modify or     
   GSCC/NAFI DK Advice or    
   GSCC/DCCX DK Remove Advice or    
   GSCC/SITR Screen Input Trade Replay or    
   GSCC/SISR Screen Input Set Replay     
   GSCC/ 
MDAD 
Post Comparison Modification 
Advice or 
   
   GSCC/DFVA [[default]] Values Applied     
   GSCC/YTPR Repricing     
   GSCC/NOVT Trade Novated     
   GSCC/SDNA Screen Replay DNA    
   GSCC/DNAP DNA Assigned     
M :22H: :PAYM/ /APMT Against Payment Trade    
O :22F: :CATB/ /PERU Per Unit Charges Indicator     
M :16R: CONFPRTY  Start of Repetitive Mandatory 
Subsequence 
   
M :95R: :BUYR/ GSCC/PART Buying Party    
O :20C: :PROC//  [[Buyer]] (contra) trs. reference     
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative    
   /TDID Trader [[ID]]    
O :70E: :DECL/ /GSCC [[participant]] Declaration Details 
Narrative 
   
   /CTRD [[Buyer]] (Contra) Trade Reference    
   /FAMT Individual Par for DNA     
   /PRCT Individual Price for DNA     
   /TDDT Individual Trade Date for DNA     
   /TRID Individual Trade [[ID]] to target for 
DNA 
   
M :16S: CONFPRTY  Repeat Block End    
M :16R: CONFPRTY  Start of Repetitive Mandatory 
Subsequence 
   

---

## Page 100

MBSD RTTM® [[Novation]]:  
SWIFT Interactive  Messaging Specifications  
Version C ontrol Page 100 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
M :95R: :SELL/ GSCC/PART Selling Party     
O :20C: :PROC//   [[Seller]] (contra) trs. reference     
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative    
   /TDID Trader [[ID]]    
O :70E: :DECL/ /GSCC [[participant]] Declaration Details 
Narrative 
   
   /CTRD [[Seller]] (Contra) Trade Reference    
   /FAMT Individual Par for DNA     
   /PRCT Individual Price for DNA     
   /TDDT Individual Trade Date for DNA     
   /TRID Individual Trade [[ID]] to target for 
DNA 
   
M :16S: CONFPRTY  Repeat Block End    
M :36B: :CONF/ /FAMT/ Quantity as Face Amount –
Original Face Value (Par)  
   
M :35B: /US/  Identification of Financial 
Instrument - TBA [[CUSIP]] 
   
M :16R: FIA  Start of Optional Subsequence     
O :12B: :OPTI/ /CALL [[Call option]] Type or     
   /PUTO [[Put Option]] Type     
O :98A: :EXPI//  Expiry Date    
O :13B: :POOL/ GSCC/ Pool Number    
M :16S: FIA  End of Optional Subsequence     
O :70E: :TPRO/ /GSCC Trade Instruction Processing 
Narrative 
   
   /TDSVSBOD Trade Service– SBOD or    
   /TDSVTFTD Trade Service– TFTD or    
   /TDSVSTIP Trade Service – STIP or    
   /TDSVOPTN Trade Service– OPTN    
   /MSGR Message Reason     
   /DKRS DK Reason     
   /GUPP Give up Period     
M :16S: CONFDET  End of Block    

---

## Page 101

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 101 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier Field Description CMPR CRQM CADV 
M :16R: SETDET  Start of Optional Sequence     
M :22F: :SETR/ /RPTO Indicator = Reporting Purposes     
M :17B: :STAN/ /N Standing Instructions Override    
M :16R: AMT  Start of Repetitive Optional 
Subsequence 
   
M :19A: :LOCO/ /USD Commission Amount     
M :16S: AMT  End of Block    
M :16S: SETDET  End of Block    
4.4.4 MT518 Field Analysis (Advices Referring to Your Trades) 
M/ 
O 
Tag Block/ 
Qualifier  
Sub-
qualifier 
Field 
Description 
CREQ MCRQ CCRQ NAFI DCCX SITR SISR MDAD DFVA YTPR NOVT SDNA DNAP 
    Message 
Header 
             
    Password              
    Sender               
    Message Type               
    Receiver              
M :16R
: 
GENL  Start of Block              
M :20C: :SEME//   Sender’s 
Reference for 
this message 
             
M :23G: NEWM  Message 
Function = 
New or 
             
  CANC [/COPY] Cancel              
O :98C: :PREP//   Preparation 
Date/Time 
             
M :22F: :TRTR/ GSCC/ 
CASH 
Cash Buy/Sell 
Trade Indicator 
             
M :16R
: 
LINK  Start of 
Optional 
Repetitive 
Subsequence  
             

---

## Page 102

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 102 
M/ 
O 
Tag Block/ 
Qualifier  
Sub-
qualifier 
Field 
Description 
CREQ MCRQ CCRQ NAFI DCCX SITR SISR MDAD DFVA YTPR NOVT SDNA DNAP 
O :20C: :MAST//   Master 
Reference 
Number 
             
M :16S: LINK  End of Block              
M :16R
: 
LINK  Start of 
Optional 
Repetitive 
Subsequence  
             
O :20C: :PREV//    Previous 
Reference 
Number 
             
M :16S: LINK  End of Block              
M :16R
: 
LINK  Start of 
Optional 
Repetitive 
Subsequence  
             
O :20C: :LIST//   RTTM 
Reference 
Number 
             
M :16S: LINK  End of Block              
M :16R
: 
LINK  Start of 
Optional 
Repetitive 
Subsequence  
             
O :20C: :BASK//    [[Broker]] 
Reference 
Number  
             
M :16S: LINK  End of Block              
M :16S: GENL  End of Block              
M :16R
: 
CONFDE
T 
 Start of Block              
M :98C: :TRAD//   Trade 
Date/Time 
             
M :98A:  :SETT//   [[settlement]] 
Date 
             
M :90A:  :DEAL/  /PRCT/ Deal Price-
Percentage 
             
O :19A:  :SETT//  [[settlement]] 
Amount  
             

---

## Page 103

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 103 
M/ 
O 
Tag Block/ 
Qualifier  
Sub-
qualifier 
Field 
Description 
CREQ MCRQ CCRQ NAFI DCCX SITR SISR MDAD DFVA YTPR NOVT SDNA DNAP 
M :22H: :BUSE/ /BUYI  Trade Type 
Buy or  
             
   /SELL  Sell              
O :22F: :PROC/ GSCC/ 
CMPR 
Comparison 
Request or 
             
   GSCC/ 
CRQM 
Comparison 
Request 
Modify or 
             
   GSCC/ 
CADV 
Comparison 
Request 
Cancel or 
             
   GSCC/ 
CREQ 
Cancel 
Request or 
             
   GSCC/ 
MCRQ 
Cancel 
Request 
Cancel or 
             
   GSCC/ 
CCRQ 
Cancel 
Request 
Modify or 
             
   GSCC/ 
NAFI 
DK Advice or              
   GSCC/ 
DCCX 
DK Remove 
Advice or 
             
   GSCC/ 
SITR 
Screen Input 
Trade Replay 
or 
             
   GSCC/ 
SISR 
Screen Input 
Set Replay 
             
   GSCC/ 
MDAD 
Post 
Comparison 
Modification 
Advice or 
             
   GSCC/ 
DFVA 
[[default]] Values 
Applied 
             
   GSCC/ 
YTPR 
Repricing              
   GSCC/ 
NOVT 
Trade Novated               
   GSCC/ 
SDNA 
Screen Replay 
DNA 
             

---

## Page 104

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 104 
M/ 
O 
Tag Block/ 
Qualifier  
Sub-
qualifier 
Field 
Description 
CREQ MCRQ CCRQ NAFI DCCX SITR SISR MDAD DFVA YTPR NOVT SDNA DNAP 
   GSCC/ 
DNAP 
DNA Assigned               
M :22H: :PAYM/ /APMT Against 
Payment 
Trade 
             
O :22F: :CATB/ /PERU Per Unit 
Charges 
Indicator or 
             
M :16R
: 
CONFPR
TY 
 Start of 
Repetitive 
Mandatory 
Subsequence  
             
M :95R: :BUYR/ GSCC/ 
PART 
Buying Party              
O :20C: :PROC//  [[Buyer]] (contra) 
trs. reference 
             
O :70C: :PACO/ /GSCC [[participant]] 
Contact 
Narrative 
             
   /TDID Trader [[ID]]              
O :70E:  :DECL/ /GSCC [[participant]] 
Declaration 
Details 
Narrative 
             
   /CTRD [[Buyer]] (Contra) 
Trade 
Reference 
             
   /FAMT Individual Par 
for DNA 
             
   /PRCT Individual 
Price for DNA 
             
   /TDDT Individual 
Trade Date for 
DNA 
             
   /TRID Individual 
Trade [[ID]] to 
target for DNA 
             
M :16S: CONFPR
TY 
 Repeat Block 
End 
             
M :16R
: 
CONFPR
TY 
 Start of 
Repetitive 
             

---

## Page 105

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 105 
M/ 
O 
Tag Block/ 
Qualifier  
Sub-
qualifier 
Field 
Description 
CREQ MCRQ CCRQ NAFI DCCX SITR SISR MDAD DFVA YTPR NOVT SDNA DNAP 
Mandatory 
Subsequence  
M :95R: :SELL/  GSCC/ 
PART 
Selling Party              
O :20C: :PROC//   [[Seller]] (contra) 
trs. reference 
             
O :70C: :PACO/ /GSCC [[participant]] 
Contact 
Narrative 
             
   /TDID Trader [[ID]]              
O :70E:  :DECL/ /GSCC [[participant]] 
Declaration 
Details 
Narrative 
             
   /CTRD [[Seller]] (Contra) 
Trade 
Reference 
             
   /FAMT Individual Par 
for DNA 
             
   /PRCT Individual 
Price for DNA 
             
   /TDDT Individual 
Trade Date for 
DNA 
             
   /TRID Individual 
Trade [[ID]] to 
target for DNA 
             
M :16S: CONFPR
TY 
 Repeat Block 
End 
             
M :36B:  :CONF/ /FAMT/ Quantity as 
Original Face 
Amount (Par) 
             
M :35B:  /US/  Identification of 
Financial 
Instrument - 
TBA [[CUSIP]] 
             
M :16R
: 
FIA  Start of 
Optional 
Subsequence  
             
O :12B:  :OPTI/ /CALL [[Call option]] 
Type or 
               

---

## Page 106

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 106 
M/ 
O 
Tag Block/ 
Qualifier  
Sub-
qualifier 
Field 
Description 
CREQ MCRQ CCRQ NAFI DCCX SITR SISR MDAD DFVA YTPR NOVT SDNA DNAP 
   /PUTO [[Put Option]] 
Type 
               
O :98A:  :EXPI//  Expiry Date                
O :13B:  :POOL/ GSCC/ Pool Number              
                  
M :16S: FIA  End of 
Optional 
Subsequence  
             
O :70E:  :TPRO/ /GSCC Trade 
Instruction 
Processing 
Narrative 
             
   /TDSV 
SBOD 
Trade 
Service–
SBOD 
or 
             
   /TDSV 
TFTD 
Trade 
Service–
TFTD 
or 
              
   /TDSV 
STIP 
Trade Service 
– STIP or 
             
   /TDSV 
OPTN 
Trade 
Service–
OPTN 
             
   /MSGR Message 
Reason 
             
   /DKRS DK Reason              
M :16S: CONFDE
T 
 End of Block              
M :16R
: 
SETDET  Start of 
Optional 
Sequence  
             
M :22F: :SETR/ /RPTO Indicator = 
Reporting 
Purposes  
             
O :17B:  :STAN/ /N Standing 
Instructions 
Override 
             
M :16R
: 
AMT  Start of 
Repetitive 
Optional 
Subsequence  
             

---

## Page 107

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 107 
M/ 
O 
Tag Block/ 
Qualifier  
Sub-
qualifier 
Field 
Description 
CREQ MCRQ CCRQ NAFI DCCX SITR SISR MDAD DFVA YTPR NOVT SDNA DNAP 
M :19A:  :LOCO/ /USD Commission 
Amount  
             
M :16S: AMT  End of Block              
M :16S: SETDET  End of Block              
4.5 MT599 Message 
This section contains the detailed specification for the MT599 General Administrative Message. As previously 
indicated, the following messages will be generated by RTTM to notify Participants of significant system 
events: 
• Start of Day (/GSOD/) 
• AM Pass Submission Cutoff (/APSC/) 
• Start of Pool Conversion, DNA [[settlement]] and TBA Reprice (/SDNR/) 
• End of Pool Conversion, DNA [[settlement]] and TBA Reprice (/EDNR/) 
• End of Day Matching Submission Cutoff (/EDCS/) 
• End of Day Interactive Output Complete (/EODC/) 
 
MT599 Format Differences 
It is important to note that the MT599 message uses the older SWIFT message types, which are slightly 
different in format from the other ISO 15022 messages employed in this specification. 
As can be noted on the following pages: 
• There are no beginning and end of block tags (16R and 16S); 
• Tags [[DO]] not always include the optional 1-character format suffix; and 
• There are no generic fields, qualifiers, or repeating sequences. 
 
We have included qualifiers in Tag 79 (narrative field) in an attempt to maintain similar formats to other 
messages being implemented, given that any type of text can be included in narrative fields. MBSD, for this 
purpose, has attempted to delineate, and label, the ‘subfields’ included similarly to those on other messages in 
this specification. Tag 79 will provide a reference to the message type being sent, as well as other various 
dates applicable to the message. 
This section is organized in the following manner: 
• Section 4.5.1: General Format 
• Section 4.5.2: Field Specifications 

---

## Page 108

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 108 
4.5.1 MT599 General Format 
M/ 
O 
Tag Block/ Qualifier Subqualifier/ 
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
  GSCC/GADM  MBSD Administrative  Message 4!c/4!c 
  /PREP/  Preparation Date/Time (8!n6!n) 
YYYYMMDDHHMMSS 
  /GSOD/  MBSD Start-of-Day Notification or YYYYMMDD 
  /APSC/  AM Pass Submission Cutoff or YYYYMMDD 
  /SDNR/  Start of Pool Conversion, DNA 
[[settlement]] and TBA Reprice 
YYYYMMDD 
  /EDNR/  End of Pool Conversion, DNA 
[[settlement]] and TBA Reprice 
YYYYMMDD 
  /EDCS/  Comparison Submission Cutoff  
End-of-Day Message or 
YYYYMMDD 
  /EODC/  Comparison Processing End- of- 
day Message 
YYYYMMDD 
  /NXTD/  Next MBSD ‘Trade  Submission’ 
Day 
YYYYMMDD 
4.5.2 MT599 Field Specifications 
Block/Tag Notes 
Message 
Header 
Each Message must contain a message header. All header fields are mandatory fixed format 
with trailing blanks, where required. 
Password 12!c This field will be blank -filled on all outbound MT599 Messages  
Sender 8!c MBSCTRRS (MBSD Trade Registration and Reconciliation System) will be the 
sender of the MT599 Comparison messages.  
Message Type 3!n/3!n/4!c  The first three characters indicate to the recipient the message type (599); the 
second three positions reflect the version of the message interface (currently always 

---

## Page 109

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging S pecifications 
Version C ontrol Page 109 
Block/Tag Notes 
000). The last four characters indicate the [[issuer]] code to be used in the message 
(“GSCC”). 
Receiver 8!c MBSD account number of the [[participant]] receiving the message.  
20 Transaction (Sender Message) Reference Number  
This field contains the sender’s message reference number. It is mandatory and will contain a unique 
number to unambiguously identify each message sent from MBSD. (This is a communications 
message number, not a trade number.)  
Note: 
While the SWIFT message accommodates both Upper and Lower case alphanumeric and certain 
symbols, for RTTM purposes this field will be p opulated with an upper case alphanumeric value. It will 
not contain symbols or hyphens.  
e.g., :20:ABCDEFG1  
79 Narrative 
This field will contain the various administrative message data, including the type of message, using 
the following qualifiers:  
• GSCC/GADM: This qualifier/[[Option]] indicates that this is an administrative message being sent 
by MBSD. 
 
• /PREP/: This field contains the message preparation date and time  
 
• /GSOD/: This qualifier indicates to Participants that this MT599 message i s MBSD’s beginning 
of day notification for the business date noted. Subsequent to receiving this message 
Participants can begin to send transactions to MBSD to be included in that day’s comparison 
process. Any messages received by MBSD after this point will result in immediate 
acknowledgement/rejection. MBSD will also, at this point, begin sending acknowledgement/ 
rejection MT509 output for all trades received after the prior business day’s cutoff point.  
 
• /APSC/: This qualifier indicates to Participants tha t this MT599 message is MBSD’s notification 
that the AM pass has already started for the business day noted. Any transactions received by 
RTTM subsequent to this point will not be included in the AM pass for that day. On netting da ys 
transactions received after this point (which were due to net that day) will be rejected by RTTM.  
 
• /SDNR/: This qualifier indicates to Participants that this MT599 message is MBSD’s  notification 
that the Pool Conversion, DNA [[settlement]] and TBA Reprice process has already started for 
the business day noted. On SIFMA 24hr days, DNA requests received after this point (which 
were due to settle that day) will be rejected by RTTM.  
 
• /EDNR/: This qualifier indicates to Participants that this MT599 message is MBSD’s notification 
that the Pool Conversion, DNA [[settlement]] and TBA Reprice process has completed for the 
business day noted.  
 
• /EDCS/: This qualifier indicates that this MT599 message is MBSD’s notification to the 
[[participant]] that any trades received by MBSD after this time will not  be included in that day’s 
comparison process. All trades received by MBSD after this cutoff (until the next night’s cutoff/ 
“EDCS” message) will be included in the comparison process for the date indicated below 
(following the qualifier ‘/NXTD/’).  
 

---

## Page 110

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Version C ontrol Page 110 
Block/Tag Notes 
• /EODC/: This qualifier indicates that this MT599 message is MBSD’s notification to Participants 
that MBSD has completed the comparison process for the date indicated and no more 
interactive comparison output will be generated for MBSD for that business day. Any 
comparison -related output sent by MBSD after this point (through generation of the next 
‘EODC’ message) will be for the business day indicated below (following the qualifier ‘/NXTD/’).  
 
• /NXTD/: This field provides the next valid MBSD trade submission date and will be included on 
all MBSD end -of-day messages.  
e.g., :79:GSCC/GADM/PREP/20000322200150/EDCS/20000322/NXTD/20000323 

---

## Page 111

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 111 
APPENDICES 
The documents included in this section are provided as a supplement to the Specifications included in Section 
4 of this document. 
Appendix A Mandatory Data for MBSD Input contains MBSD Mandatory Data listings for Trade Input. 
Appendix B Reference Number Usage in Messages delineates how transaction-related reference 
numbers (i.e., X-Ref, [[Broker]] Reference, Transaction [[ID]], Trade [[ID]], Submission [[ID]], Contra 
Trade [[ID]] and Contra Transaction [[ID]]) are used in the various interactive messages. 
Appendix C ISO 15022 Message Structure Diagrams contains diagrams from the SWIFT manual 
reflecting the structure of the MT515, MT509 and MT518 messages. 
Appendix D Message Flows contains detailed diagrams depicting the flows of messages to and from 
RTTM for various transaction-related scenarios. These flows have been divided into 
multiple sections. 
Appendix E Message Samples provides samples of a variety of MT515, MT509 and MT518 messages 
dealer-to-dealer and brokered trades. 
Appendix A: Mandatory Data for MBSD Input 
The following are lists of data that are mandatory on MBSD input for TBA trades. 
A.1 Dealer Input 
1. External Reference Number 
2. Transaction Type (Buy/Sell) 
3. Trade Service Type 
4. Trade Date 
5. [[settlement]] Date 
6. Security 
7. Par Amount/Quantity 
8. Price 
9. [[Buyer]] [[participant]] Account 
10. [[Seller]] [[participant]] Account 
11. Commission amount per trade (where applicable) 
12. Rate commission indicator (where applicable) 
13. [[Option]] Type (for [[Option]] trades only) 
14. Expiry Date (for [[Option]] trades only) 

---

## Page 112

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 112 
A.2 [[Broker]] Input 
1. [[Broker]] Reference Number 
2. External Reference Number 
3. Transaction Type (Buy/Sell) 
4. Trade Service Type 
5. Trade Date 
6. [[settlement]] Date 
7. Security 
8. Par Amount/Quantity 
9. Price 
10. [[Buyer]] [[participant]] Account * 
11. [[Seller]] [[participant]] Account* 
12. Commission amount per trade 
13. Rate commission indicator 
 
Note: 
As previously mentioned, Cancel Set and Modify Set records will reflect only a [[Buyer]] Confirming Party Block.  This block will 
contain data specific to the [[Broker]], rather than the actual [[Buyer]] or [[Seller]] party.  
Appendix B: Reference Number Usage in Messages 
This appendix contains the following sections on Transaction-Related Reference Numbers on Messages from: 
• Dealers to RTTM (Dealer Input) 
• Brokers to RTTM ([[Broker]] Input) 
• RTTM to Dealers (Dealer Output) 
• RTTM to Brokers ([[Broker]] Output) 
Transaction -Related Reference Numbers on Messages from Dealers to RTTM 
Dealers wishing to …  Before matching  After matching 
Submit NEW trades, should 
input:  
MT515 Instruct/Trade Create 
• X-ref (MAST) 
N/A 
MODIFY their X-REF, should 
input:  
N/A MT515 Modify 
• New X-ref (MAST) 
• Previous X-ref (PREV) where 
applicable 
• Transaction [[ID]] or Trade [[ID]] (LIST)  
CANCEL their 
transactions/trades, should 
input:  
MT515 Cancel 
• X-ref (MAST) 
• Transaction [[ID]] (LIST)  
MT515 Cancel 
• X-ref (MAST) 
• Transaction [[ID]] or Trade [[ID]] (LIST)  

---

## Page 113

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 113 
Dealers wishing to …  Before matching  After matching 
DK Comparison Requests  
submitted against them, should 
input:  
MT515 DK 
• Transaction [[ID]] of Contra (PROC)  
DK Cancel Requests  submitted 
against them, should input:  
N/A MT515 DK 
• X-ref (MAST) 
• Trade [[ID]] (LIST)  
 
Transaction-Related Reference Numbers on Messages from Brokers to RTTM 
Brokers wishing to…  Before balancing  After balancing but 
before matching  
PMAT FMAT 
Submit NEW trades, 
should input:  
MT515 
Instruct/Trade 
Create 
• [[Broker]] Ref 
(BASK) 
• X-ref (MAST) 
N/A N/A N/A 
MODIFY their [[Broker]] 
REF, should input:  
MT515 Modify 
• New [[Broker]] Ref 
(BASK) 
• X-ref (MAST) 
• Submission [[ID]] 
(LIST) 
N/A MT515 Modify Set  
• New [[Broker]] Ref 
(BASK) 
• Previous Broke r 
Ref (PREV) 
• Transaction [[ID]] 
or Trade [[ID]] 
(LIST) 
MT515 Modify Set  
• New [[Broker]] Ref 
(BASK) 
• Previous [[Broker]] 
Ref (PREV) 
• Transaction [[ID]] 
or Trade [[ID]] 
(LIST) 
MODIFY the CONTRA 
and/or the 
COMMISSION on the 
unmatched side of a 
PMAT trade, should 
input:  
N/A N/A MT515 Modify 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
or Trade [[ID]] 
(LIST) 
N/A 
CANCEL their 
Submissions/ 
Transactions/Trades, 
should input:  
MT515 Cancel 
• X-ref (MAST) 
• Submission [[ID]] 
(LIST) 
MT515 Cancel Set 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
(LIST) 
MT515 Cancel Set 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
or Trade [[ID]] 
(LIST) 
N/A 
DK Comparison 
Requests submitted 
against them, should 
input:  
MT515 DK 
• Transaction [[ID]] of Contra (PROC)  

---

## Page 114

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 114 
Brokers wishing to…  Before balancing  After balancing but 
before matching  
PMAT FMAT 
DK Cancel Requests 
submitted against them, 
should input:  
N/A N/A MT515 DK 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
N/A 
 
Transaction-Related Reference Numbers on Messages from RTTM to Dealers 
Dealers receiving 
information on…  
Before matching  Upon or after matching  
New TRADE CREATES 
they submitted, will 
receive: 
MT509 Trade Create Accepted/ Rejected  
• X-ref (if avail. for REJT) (MAST) 
• Transaction [[ID]] (not for REJT) (LIST)  
OR (in case of Trade Creates input via screen)  
MT518 Screen Input Trade Replay 
• X-ref (MAST) 
• Transaction [[ID]] (LIST)  
N/A 
Their previously 
submitted TRADE 
CREATES that match, 
will receive:  
N/A MT509 Transaction Matched  
• X-ref (MAST) 
• Transaction [[ID]] (LIST)  
• [[Broker]] Match [[ID]] (BASK), if matched 
vs [[Broker]]  
MODIFIES they 
submitted interactively, 
will receive:  
N/A MT509 Modify Accepted/ Rejected/ 
Processed 
• New X-ref (if avail. for REJT) (MAST)  
• Previous X-ref (if avail. for REJT) 
(PREV) 
• Transaction or Trade [[ID]] (if avail. for 
REJT) (LIST) 
MODIFIES they 
submitted via screen, 
will receive:  
N/A MT518 Screen Input Trade Replay 
• New X-ref (MAST) 
• Trade [[ID]] (LIST)  
CANCELS they 
submitted interactively, 
will receive:  
MT509 Cancel Accepted/ Rejected/ 
Processed 
• X-ref (if avail. for REJT) (MAST) 
• Transaction [[ID]] (if avail. for REJT) (LIST)  
MT509 Cancel Accepted/ Rejected/ 
Processed 
• X-ref (if avail. for REJT) (MAST) 
• Transaction or  Trade [[ID]] (if avail. for 
REJT) (LIST) 
CANCELS they 
submitted via screen, 
will receive:  
MT518 Screen Input Trade Replay 
• X-ref (MAST) 
• Transaction [[ID]] (LIST)  
MT518 Screen Input Trade Replay 
• X-ref (MAST) 
• Trade [[ID]] (LIST)  

---

## Page 115

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 115 
Dealers receiving 
information on…  
Before matching  Upon or after matching  
MT509 Cancel Processed 
• X-ref (MAST) 
• Transaction [[ID]] (LIST)  
MT509 Cancel Processed 
• X-ref (MAST) 
• Trade [[ID]] (LIST)  
CANCEL REMOVES 
they submitted via 
screen, will receive:  
N/A MT509 Cancel Lifted by [[participant]]  
• X-ref (MAST) 
• Trade [[ID]] (LIST)  
DKs they submitted 
interactively, will receive : 
MT509 DK (of Comparison Request) 
Accepted/ Rejected/ Processed  
• Transaction [[ID]] of Contra (PROG)  
and  
MT518 Comparison Request Modify  
(due to DK)  
• Transaction [[ID]] of Contra (PROC)  
MT509 DK (of Cancel Request) 
Accepted/ Rejected/ Processed  
• X-ref (if avail. for REJT) (MAST) 
• Trade [[ID]] (if avail. for REJT) (LIST)  
and  
MT518 Cancel Request Modify  
(due to DK)  
• X-ref (MAST) 
• Trade [[ID]] (LIST)  
DKs or DK REMOVES 
they submitted via 
screen, will receive:  
MT518 Comparison Request Modify (due to 
DK/due to DK Remove)  
• Transaction [[ID]] of Contra (PROC)  
MT518 Cancel Request Modify (due to 
DK/due to  DK Remove)  
• X-ref (MAST) 
• Trade [[ID]] (LIST)  
Their UNCOMPARED 
transactions that are 
deleted by RTTM, will 
receive: 
MT509 Deleted Uncompared Transaction  
• X-ref (MAST) 
• Transaction [[ID]] (LIST)  
N/A 
New TRADE CREATES 
submitted by a Contra 
against them, will 
receive: 
MT518 Comparison Request  
• Transaction [[ID]] of Contra (PROC)  
N/A 
TRADE CREATES 
previously submitted by 
a Contra against them 
that match, will receive:  
N/A MT518 Comparison Request Cancel 
(due to Match)  
• Transaction [[ID]] of Contra (PROC)  
• Trade [[ID]] of Contra 
(DECL//GSCC/CTRD) 
• [[Broker]] Match [[ID]] (BASK), if matched 
vs [[Broker]]  
COMMISSION 
MODIFIES submitted by 
a Contra against them, 
will receive:  
MT518 Comparison Request Modify  
• Transaction [[ID]] of Contra (PROC)  
N/A 
CANCELS submitted by 
a Contra against them, 
will receive:  
MT518 Comparison Request Cancel (due to 
Contra) 
• Transaction [[ID]] of Contra (PROC)  
MT518 Cancel Request  
• X-ref (MAST) 
• Trade [[ID]] (LIST)  

---

## Page 116

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 116 
Dealers receiving 
information on…  
Before matching  Upon or after matching  
CANCEL REMOVES 
submitted by a Contra 
against them, will 
receive: 
N/A MT518 Cancel Request Cancel  
• X-ref (MAST) 
• Trade [[ID]] (LIST)  
DKs and DK REMOVES 
submitted by a Contra 
against their TRADE 
CREATES, will receive:  
MT518 DK Advice/ DK Remove Advice 
• X-ref (MAST) 
• Transaction [[ID]] (LIST)  
N/A 
DKs and DK REMOVES 
submitted by a Contra 
against their CANCELS , 
will receive:  
N/A MT518 DK (Cancel) Advice/ DK (Cancel) 
Remove Advice 
• X-ref (MAST) 
• Trade [[ID]] (LIST)  
Their previously 
submitted TRADE 
CREATES that are 
novated will receive:  
N/A MT518 Trade Novated  
• X-ref (MAST) 
• Trade [[ID]] (LIST)  
• [[Broker]] Match [[ID]] (BASK), if matched 
vs [[Broker]]  
 
Transaction-Related Reference Numbers on Messages from RTTM to Brokers 
Brokers receiving 
information on …  
Before balancing  After balancing but 
before matching  
PMAT FMAT 
New TRADE 
CREATES they 
submitted, will 
receive: 
MT509 Trade Create 
Accepted/ Rejected/ 
Unbalanced 
(1) 
• X-ref (if avail. for 
REJT) (MAST) 
• [[Broker]] Ref (if 
avail. For REJT) 
(BASK) 
• Submission [[ID]] 
(not for  REJT) 
(LIST) 
OR (in case of Trade 
Creates input via 
screen)  
MT518 Screen Input 
Trade Replay 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
(LIST) 
MT509 Trade Create 
Balanced 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Submission [[ID]] 
(PREV) 
• Transaction [[ID]] 
(LIST) 
N/A N/A 

---

## Page 117

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 117 
Brokers receiving 
information on …  
Before balancing  After balancing but 
before matching  
PMAT FMAT 
(1) In case of screen 
input, no MT 509 
TRADE CREATE 
ACCEPTED or 
REJECTED 
messages will be 
sent–MT509 
TRADE CREATE 
UNBALANCED 
messages will  be sen t 
however.  
Their previously 
submitted TRADE 
CREATES that 
match, will receive:  
N/A N/A MT509 Transaction 
Matched 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
(LIST) 
MT509 Trade 
Partially Matched 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
(PREV) 
• Trade [[ID]] (LIST)  
MT509 Trade Fully 
Matched 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
MODIFIES they 
submitted 
interactively, will 
receive: 
MT509 Modify 
Accepted/ Rejected/ 
Processed 
• X-ref (if avail. for 
REJT) (MAST) 
• New [[Broker]] Ref 
(if avail. for 
REJT) (BASK) 
• Submission [[ID]] (if 
avail. for REJT) 
(LIST) 
N/A MT509 Modify 
Accepted/ Rejected/ 
Processed 
• [[Broker]] Ref (if 
avail. for REJT) 
(BASK) 
• Transaction [[ID]] 
or Trade [[ID]] (if 
avail. for REJT) 
(LIST) 
• X-ref (MAST) 
N/A 
MODIFIES they 
submitted via 
screen, will receive:  
MT518 Screen Input 
Trade Replay 
• X-ref (MAST) 
• New [[Broker]] Ref 
(BASK) 
• Submission [[ID]] 
(LIST) 
N/A MT518 Screen Input 
Trade Replay 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
• X-ref (MAST) 
N/A 

---

## Page 118

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 118 
Brokers receiving 
information on …  
Before balancing  After balancing but 
before matching  
PMAT FMAT 
MODIFY SETS they 
submitted 
interactively, will 
receive: 
N/A N/A MT509 Modify Set 
Accepted/ Rejected/ 
Processed 
• New [[Broker]] Ref 
(if avail. for 
REJT) (BASK) 
• Previous [[Broker]] 
Ref (if avail. for 
REJT) (PREV) 
• Transaction [[ID]] 
or Trade [[ID]] (if 
avail. for REJT) 
(LIST) 
MT509 Modify Set 
Accepted/ Rejected/ 
Processed 
• New [[Broker]] Ref 
(if avail. for 
REJT) (BASK) 
• Previous [[Broker]] 
Ref (if avail. for 
REJT) (PREV) 
• Transaction [[ID]] 
or Trade [[ID]] (if 
avail. for REJT) 
(LIST) 
MODIFY SETS they 
submitted via 
screen, will receive:  
N/A N/A MT518 Screen Input 
Set Replay 
• New [[Broker]] Ref 
(BASK) 
• Previous [[Broker]] 
Ref (PREV) 
• Trade [[ID]] (LIST)  
MT518 Screen Input 
Set Replay 
• New [[Broker]] Ref 
(BASK) 
• Previous [[Broker]] 
Ref (PREV) 
• Trade [[ID]] (LIST)  
CANCELS or 
CANCEL SETS th ey  
submitted 
interactively, will 
receive: 
MT509 Cancel 
Accepted/ Rejected/ 
Processed 
• X-ref (if avail. for 
REJT) (MAST) 
• [[Broker]] Ref (if 
avail. for REJT) 
(BASK) 
• Submission [[ID]] (if 
avail. for REJT) 
(LIST) 
MT509 Cancel Set 
Accepted/ Rejected/ 
Processed 
• [[Broker]] Ref (if 
avail. for REJT) 
(BASK) 
• Transaction [[ID]] 
(if avail. for 
REJT) (LIST) 
MT509 Cancel Set 
Accepted/ Rejected/ 
Processed 
• [[Broker]] Ref (if 
avail. for REJT) 
(BASK) 
• Transaction [[ID]] 
or Trade [[ID]] (if 
avail. for REJT) 
(LIST) 
N/A 
CANCELS, 
CANCEL SETS, 
CANCEL 
REMOVES, or 
CANCEL SET 
REMOVES they 
submitted via 
screen, will receive:  
MT518 Screen Input 
Trade Replay 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Submission [[ID]] 
(LIST) 
MT509 Cancel 
Processed 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Submission [[ID]] 
(LIST) 
MT518 Screen Input 
Set Replay 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
(LIST) 
MT509 Cancel Set 
Processed 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
(LIST) 
MT518 Screen Input 
Set Replay 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
MT509 Cancel Set 
Processed/ Lifted  by 
[[participant]] 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
N/A 

---

## Page 119

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 119 
Brokers receiving 
information on …  
Before balancing  After balancing but 
before matching  
PMAT FMAT 
DKs they submitted 
interactively, will 
receive: 
MT509 DK (of 
Comparison 
Request) 
Accepted/Rejected/ 
Processed 
• Transaction [[ID]] 
of Contra (if 
avail. for REJT) 
(PROG) 
and  
MT518 Comparison 
Request Modify (due 
to DK) 
• Transaction [[ID]] 
of Contra 
(except if REJT) 
(PROC) 
N/A MT509 DK (of Cancel 
Request) Accepted/ 
Rejected/ Processed 
• [[Broker]] Ref (if 
avail. for REJT) 
(BASK) 
• Trade [[ID]] (if avail. 
for REJT) (LIST) 
• X-ref (MAST) 
and  
MT518 Cancel 
Request Modify (due 
to DK) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
• X-ref (MAST) 
N/A 
DKs or DK 
REMOVES they 
submitted via 
screen, will receive:  
MT518 Comparison 
Request Modify (due 
to DK/due to DK 
Remove) 
• Transaction [[ID]] 
of Contra 
(PROC) 
N/A MT518 Cancel 
Request Modify (due 
to DK/due to DK 
Remove) 
• [[Broker]] Ref (if 
avail. for REJT) 
(BASK) 
• Trade [[ID]] (if avail. 
for REJT) (LIST) 
• X-ref (MAST) 
N/A 
Their uncompared 
transactions that are 
deleted by RTTM, 
will receive:  
N/A MT509 Deleted 
Uncompared 
Transaction 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
(LIST) 
N/A N/A New TRADE 
CREATES 
submitted by a 
Dealer against them, 
will receive:  
MT518 Comparison Request  
• Transaction [[ID]] of Contra (PROC)  
TRADE CREATES 
previously submitted 
by a Dealer against 
them that match, will 
receive: 
N/A N/A MT518 Comparison 
Request Cancel (due 
to Match) 
• Transaction [[ID]] of  
Contra (PROC)  
• Trade [[ID]] of 
Contra  
MT518 Comparison 
Request Cancel (due 
to Match) 
• Transaction [[ID]] of 
Contra (PROC)  
• Trade [[ID]] of 
Contra  

---

## Page 120

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 120 
Brokers receiving 
information on …  
Before balancing  After balancing but 
before matching  
PMAT FMAT 
(DECL//GSCC/C
TRD) 
(DECL//GSCC/C
TRD) 
MODIFIES 
submitted by a 
Dealer against them, 
will receive:  
N/A N/A N/A N/A 
CANCELS 
submitted by a 
Dealer against them, 
will receive:  
MT518 Comparison Request Cancel (due to 
Contra) 
• Transaction [[ID]] of Contra (PROC)  
MT518 Cancel 
Request 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
MT518 Cancel 
Request (for 
informational 
purposes) 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
MT509 Cancel 
Processed (for 
informational 
purposes) 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
CANCEL 
REMOVES 
submitted by a 
Dealer against them, 
will receive:  
N/A MT518 Cancel 
Request Cancel 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
MT518 Cancel 
Request Cancel (For 
Informational 
Purposes) 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
DKs and DK 
REMOVES 
submitted by a 
Dealer against their 
TRADE CREATES, 
will receive:  
N/A MT518 DK Advice/ 
DK Remove Advice 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Transaction [[ID]] 
(LIST) 
MT518 DK Advice/ 
DK Remove Advice 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
N/A 
DKs and DK 
REMOVES 
submitted by a 
Dealer against their 
CANCELS SETS, 
will receive:  
N/A MT518 DK (Cancel) 
Advice/ DK (Cancel) 
Remove Advice 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
N/A 

---

## Page 121

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 121 
Brokers receiving 
information on …  
Before balancing  After balancing but 
before matching  
PMAT FMAT 
DKs and DK 
REMOVES 
submitted by a 
Dealer against 
another Dealer’s 
CANCELS in a 
brokered trade, will 
receive: 
N/A N/A MT518 DK (Cancel) 
Advice/ DK (Cancel) 
Remove Advice (For 
Informational 
Purposes) 
• X-ref (MAST) 
• [[Broker]] Ref 
(BASK) 
• Trade [[ID]] (LIST)  
 
  

---

## Page 122

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 122 
Appendix C: ISO 15022 Message Structure Diagrams 
This appendix contains diagrams for the following messages: 
• MT515 
• MT509 
• MT518 
Message Structure Diagram: MT515 
 


---

## Page 123

MBSD RTTM® [[Novation]] :  
SWIFT Interactive Messaging Specifications  
Appendices 123 
Message Structure Diagram: MT509 
 


---

## Page 124

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 124 
Message Structure Diagram: MT518 
  
  


---

## Page 125

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 125 
Appendix D: Message Flows 
Dealer/Dealer Message Flows 
This appendix contains 25 possible scenarios for message flows between Dealers. 
DD 1: Trade Create Transaction Accepted 
 
 
DD 2: Pre-Comparison Cancel 
This flow starts with Dealer A submitting a Trade Instruct against Dealer B, who receives a Comparison 
Request advice notifying them of this event (step 1-2b).  
Dealer A then unilaterally cancels the trade (step 3), which is accepted and processed by the system, including 
notif ying Dealer B that the previously received Comparison Request advice has been canceled (step 4a-c). 
 


---

## Page 126

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 126 
DD 3: Trade Create Transaction Matched and Novated 
In this flow, Dealer A submits a Trade Instruct against Dealer B (step 1-2b). Dealer B responds by sending a 
matching Trade Instruct (step 3-4b). When the two instructs compare, the dealers are notified of the match 
event (5a-b), and the previously received Comparison Request is canceled (5c-d). 
Once the comparison event occurs, the trades are automatically novated4 by the system (step 6a-b) and any 
further actions by the dealers against these trades must be submitted versus [[FICC]]. 
 
Note: 
The “Trade Novated”  message will identify [[FICC]] as the contra.  
  
 
4 Options are not novated. 


---

## Page 127

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 127 
DD 4: Trade Create Transaction Matched and Novated by Affirmation or Contra Trade Create (via WFE) 
In this flow, Dealer A submits a Trade Instruct against Dealer B (step 1-2b). Dealer B responds by affirming the 
trade or creating a matching trade via the WFE (s tep 3-4b). When the two instructs compare, the dealers are 
notified of the match event (5a-b), and the previously received Comparison Request is canceled (5c-d). 
Once the comparison event occurs, the trades are automatically novated5 by the system (step 6a-b) and any 
further actions by the dealers against these trades must be submitted versus [[FICC]]. 
 
Note: 
The “Trade Novated” message will identify [[FICC]] as the contra.  
 
  
 
5 Options are not novated. 


---

## Page 128

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 128 
DD 5: Trade Create Transaction DK’ed 
This flow starts with Dealer A submitting a Trade Instruct against Dealer B, who receives a Comparison 
Request advice notifying them of this event (step 1-2b).  
Dealer B then submits a DK, which is processed and causes a DK Advice to be sent to Dealer A informing 
them of the DK event, as well as a notification to Dealer B that their previously received Comparison Request 
has been updated due to this DK (step 3-4d). 
 
 
DD 6: Trade Create Transaction DK’ed (via WFE) 
This flow starts with Dealer A submitting a Trade Instruct against Dealer B, who receives a Comparison 
Request advice notifying them of this event (step 1-2b).  
Dealer B then DKs the trade advisory via the WFE, which is processed and causes a DK Advice to be sent to 
Dealer A informing them of the DK event, as well as a notification to Dealer B that their previously received 
Comparison Request has been updated due to this DK (step 3-4b). 
 


---

## Page 129

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 129 
DD 7: Trade Create Transaction DK’ed, then Canceled Pre-Comparison 
This flow starts with Dealer A submitting a Trade Instruct against Dealer B, who receives a Comparison 
Request advice notifying them of this event (step 1-2b).  
Dealer B then submits a DK, which is processed and causes a DK Advice to be sent to Dealer A informing 
them of the DK event, as well as a notification to Dealer B that their previously received Comparison Request 
has been updated due to this DK (step 3-4d). 
Dealer A then responds to the DK by unilaterally cancelling the instruct, with Dealer B notified that their 
previously received Comparison Request is now canceled (step 5-6c). 
Dealer A
1. 
MT
515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 DK5. 
MT515 Cancel
4c.
MT518 Comparison Request 
Modify (due to DK)
4a.
MT509 DK Accepted
4d.
MT509 DK Accepted
4b.
MT518 DK Advice
6a.
MT509 Cancel Accepted
6c.
MT509 Cancel Processed
RTTM
6b.
MT518 Comparison Request 
Cancel (due to contra)
 

---

## Page 130

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 130 
DD 8: Trade Create Transaction DK’ed then Compared and Novated (DK Removed due to Match) 
This flow starts with Dealer A submitting a Trade Instruct against Dealer B, who receives a Comparison 
Request advice notifying them of this event (step 1-2b).  
Dealer B DKs this trade advisory, resulting in a DK Advice to Dealer A informing them of the DK event (step 3-
4d). However, Dealer B then submits a matching Trade Instruct. Due to this comparison event, the 
corresponding Comparison Requests previously received are canceled and DK advice removed (step 5-6f). 
As the trades are now matched, they are automatically novated
6 by the system (step 7a-b) and any further 
actions by the dealers against these trades must be submitted versus [[FICC]]. 
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 DK
5. 
MT515 Instruct
4c.
MT518 Comparison Request 
Modify (due to DK)
4a.
MT509 DK Accepted
4d.
MT509 DK Accepted
4b.
MT518 DK Advice
6c.
MT518 DK Remove Advice
6a.
MT509 Trade Create Accepted
6b.
MT518 Comparison Request
6d.
MT509 Trade Create Matched
6f.
MT518 Comparison Request 
Cancel (due to Match)
6e. 
MT509 Trade Create Matched
6g.
MT518 Comparison Request 
Cancel (due to Match)
Dealer A Dealer B
RTTM
7a.
MT518 Trade Novated (*)
7b.
MT518 Trade Novated (*)
 
Note: 
The “Trade Novated” message will identify [[FICC]] as the contra.  
 
 
6 Options are not novated. 

---

## Page 131

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 131 
DD 9: Uncompared SBOD Transaction Deleted by RTTM (Prior to Net) 
In this flow, Dealer A submits a SBOD Trade Instruct against Dealer B, who receives a Comparison Request 
advice notifying them of this event (step 1-2b).  
At the onset of netting, this uncompared trade is automatically deleted by the system (step 3a-b). 
Dealer A 1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT
518 Comparison Request
3b.
MT
518 Comparison Request 
Cancel (due to RTTM)
3a.
MT
509 Deleted Uncompared 
Transaction
RTTM
Beginning of 
TBA Netting 
Process
 

---

## Page 132

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 132 
DD 10: Post-Comparison Modify (via Message) 
This flow starts with a compared novated7 trade between Dealer A and Dealer B (step 1-6b).  
Dealer A then modifies their trade (step 7), which is accepted and applied to their trade (step 8a-b). Note that 
only non-economic modifications are supported on compared trades; as such, Dealer B is not notified of this 
event. 
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 Instruct
4b.
MT518 Comparison Request
4a.
MT509 Trade Create Accepted
5a.
MT509 Trade Create Matched
5b.
MT509 Trade Create Matched
6a.
MT518 Trade Novated
6b.
MT518 Trade Novated
5c.
MT518 Comparison Request 
Cancel (due to Match)
5d.
MT518 Comparison Request 
Cancel (due to Match)
Dealer A
RTTM
7. 
MT515 Modify
8a.
MT509 Modify Accepted
8b.
MT509 Modify Processed
 
 
 
7 Options are not novated 

---

## Page 133

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 133 
DD 11: Post-Comparison Modify (via WFE) 
This flow starts with a compared novated8 trade between Dealer A and Dealer B (step 1-6b).  
Dealer A then modifies their trade via WFE, which is applied to their trade (step 7-8). As only non-economic 
modifications are supported on compared trades, Dealer B is not notified of this event. Note that as Dealer A 
initiated this modification via WFE rather than messaging, a MT518 Screen Input Trade Replay (Modify) 
message is returned in step7, which provides full details of the action initiated. 
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT
518 Comparison Request
3. 
MT
515 Instruct
4b.
MT
518 Comparison Request
4a.
MT
509 Trade Create Accepted
5a.
MT
509 Trade Create Matched
5b.
MT
509 Trade Create Matched
6a.
MT
518 Trade Novated
6b.
MT
518 Trade Novated
5c.
MT
518 Comparison Request 
Cancel (due to Match)
5d.
MT
518 Comparison Request 
Cancel (due to Match)
Dealer A
RTTM
7. 
MT
515 Modify
(via WFE)
8.
MT
518 Screen Input 
Trade Replay (Modify)
 
 
8 Options are not novated 

---

## Page 134

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 134 
DD 12: Post-Comparison Cancel 
This flow starts with a compared novated9 trade between Dealer A and Dealer B (step 1-6b).  
Dealer A initiates a Cancel, which results in a Cancel Request advice being sent to Dealer B (as the trade is 
compared, the cancel must be bilaterally agreed upon) (step 7-8b). Dealer B then responds to the Cancel 
Request advice by submitting a matching Cancel, resulting in the compared trade being canceled (step 9-11b). 
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 Instruct
4b.
MT518 Comparison Request
4a.
MT509 Trade Create Accepted
5a.
MT509 Trade Create Matched
6a.
MT518 Trade Novated
6b.
MT518 Trade Novated
5c.
MT518 Comparison Request 
Cancel (due to Match)
5d.
MT518 Comparison Request 
Cancel (due to Match)
Dealer A 7. 
MT515 Cancel
RTTM
8a.
MT509 Cancel Accepted
Dealer B9. 
MT515 Cancel
10b.
MT518 Cancel Request
11a.
MT509 Cancel Processed
5b.
MT509 Trade Create Matched
8b.
MT518 Cancel Request
10a.
MT509 Cancel Accepted
11b.
MT509 Cancel Processed
 
 
 
9 Options are not novated.  

---

## Page 135

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 135 
DD 13: Post-Comparison Cancel (via WFE) 
This flow starts with a compared novated10 trade between Dealer A and Dealer B (step 1-6b).  
Dealer A initiates a Cancel, which results in a Cancel Request advice being sent to Dealer B (as the trade is 
compared, the cancel must be bilaterally agreed upon) (step 7-8b). Dealer B then responds to the Cancel 
request advice by submitting a matching Cancel via WFE, resulting in the compared trade being canceled (step 
9-11b). Note that as Dealer B initiated this cancel via WFE rather than messaging, a MT518 Screen Input 
Trade Replay (Cancel) message is returned in step 10a, which provides full details of the action initiated. 
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 Instruct
4b.
MT518 Comparison Request
4a.
MT509 Trade Create Accepted
5a.
MT509 Trade Create Matched
6a.
MT518 Trade Novated
6b.
MT518 Trade Novated
5c.
MT518 Comparison Request 
Cancel (due to Match)
5d.
MT518 Comparison Request 
Cancel (due to Match)
Dealer A 7. 
MT515 Cancel
RTTM
8a.
MT509 Cancel Accepted
Dealer B
9. 
Cancel 
(via WFE)
10b.
MT518 Cancel Request
11a.
MT509 Cancel Processed
5b.
MT509 Trade Create Matched
8b.
MT518 Cancel Request
10a.
MT518 Screen Input 
Trade Replay (Cancel)
11b.
MT509 Cancel Processed
 
 
 
10 Options are not novated 

---

## Page 136

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 136 
DD 14: Post-Comparison Cancel Request Removed (via WFE) 
This flow starts with a compared novated11 trade between Dealer A and Dealer B (step 1-6b).  
Dealer A initiates a Cancel, which results in a Cancel Request advice being sent to Dealer B (step 7-8b). 
Dealer A subsequently removes the cancel request by issuing an “un-cancel” via WFE12, resulting in the cancel 
request being lifted (step 9-10b).  
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 Instruct
4b.
MT518 Comparison Request
4a.
MT509 Trade Create Accepted
5a.
MT509 Trade Create Matched
6a.
MT518 Trade Novated
6b.
MT518 Trade Novated
5c.
MT518 Comparison Request 
Cancel (due to Match)
5d.
MT518 Comparison Request 
Cancel (due to Match)
Dealer A
7. 
MT515 Cancel
RTTM
Dealer B
8a.
MT509 Cancel Accepted
5b.
MT509 Trade Create Matched
8b.
MT518 Cancel Request
10b.
MT518 Cancel Request 
Cancel (due to Contra)
10a.
MT509 Cancel Lifted (by 
[[participant]])
9. 
Cancel Remove 
(via WFE only)
 
 
11 Options are not novated 
12 “Un-cancel” action is only available via WFE; it cannot be submitted via SWIFT MT515. 

---

## Page 137

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 137 
DD 15: Post-Comparison Cancel Request DKed 
This flow starts with a compared novated13 trade between Dealer A and Dealer B (step 1-6b).  
Dealer A then initiates a Cancel, which results in a Cancel Request advice being sent to Dealer B (step 7-8b). 
Dealer B responds by DKing the cancel request, which is processed and results in a DK Advice being sent to 
Dealer A, along with an update notification for Dealer B’s cancel request (due to DK) (step 9-10d).  
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 Instruct
4b.
MT518 Comparison Request
4a.
MT509 Trade Create Accepted
5a.
MT509 Trade Create Matched
6a.
MT518 Trade Novated
6b.
MT518 Trade Novated
5c.
MT518 Comparison Request 
Cancel (due to Match)
5d.
MT518 Comparison Request 
Cancel (due to Match)
Dealer A 7. 
MT515 Cancel
RTTM
Dealer B
8a.
MT509 Cancel Accepted
5b.
MT509 Trade Create Matched
8b.
MT518 Cancel Request
10a.
MT509 DK (of Cancel 
Request) Accepted
10b.
MT518 DK (of Cancel) Advice
9. 
MT515 DK 
(of Cancel Request)
10c.
MT518 Cancel Request Modify 
(due to DK)
10d.
MT509 DK (of Cancel) Processed
 
 
13 Options are not novated 

---

## Page 138

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 138 
DD 16: Post-Comparison Cancel Request DKed Followed by Cancel Remove (via WFE) 
This flow starts with a compared novated14 trade between Dealer A and Dealer B (step 1-6b).  
Dealer A then initiates a Cancel, which results in a Cancel Request advice being sent to Dealer B (step 7-8b). 
Dealer B responds by DKing the cancel request, which is processed and results in a DK Advice being sent to 
Dealer A, along with an update notification for Dealer B’s cancel request (due to DK) (step 9-10d). Dealer A 
then responds to the DK by removing the cancel request by issuing an “un-cancel” request via WFE, which 
results in the cancel request being lifted (step 11-12b).  
Dealer A
1. 
MT
515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 Instruct
4b.
MT518 Comparison Request
4a.
MT509 Trade Create Accepted
5a.
MT509 Trade Create Matched
6a.
MT518 Trade Novated
6b.
MT518 Trade Novated
5c.
MT518 Comparison Request 
Cancel (due to Match)
5d.
MT518 Comparison Request 
Cancel (due to Match)
Dealer A
7. 
MT515 Cancel
Dealer B
RTTM
8a.
MT509 Cancel Accepted
5b.
MT509 Trade Create Matched
8b.
MT518 Cancel Request
10a.
MT509 DK (of Cancel 
Request) Accepted
10b.
MT518 DK (of Cancel) Advice
9. 
MT515 DK 
(of Cancel Request)
10c.
MT518 Cancel Request Modify 
(due to DK)
10d.
MT509 DK (of Cancel Request) 
Processed
11. 
Cancel Remove 
(via WFE only)
12a.
MT509 Cancel Lifted (by [[participant]]) 12b.
MT518 Cancel Request Cancel
(due to Contra)
 
 
14 Options are not novated 

---

## Page 139

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 139 
DD 17: Post-Comparison Cancel Request DK’ed (via WFE) Followed by Cancel Remove (via WFE) 
This flow starts with a compared novated15 trade between Dealer A and Dealer B (step 1-6b).  
Dealer A then initiates a Cancel, which results in a Cancel Request advice being sent to Dealer B (step 7-8b). 
Dealer B responds by DKing the cancel request via WFE, which is processed and results in a DK Advice being 
sent to Dealer A, along with an update notification for Dealer B’s cancel request (due to DK) (step 9-10b). 
Dealer A then responds to the DK by removing the cancel request by issuing an “un-cancel” request via WFE, 
which results in the cancel request being lifted (step 11-12b).  
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 Instruct
4b.
MT518 Comparison Request
4a.
MT509 Trade Create Accepted
5a.
MT509 Trade Create Matched
6a.
MT518 Trade Novated
6b.
MT518 Trade Novated
5c.
MT518 Comparison Request 
Cancel (due to Match)
5d.
MT518 Comparison Request 
Cancel (due to Match)
Dealer A
7. 
MT515 Cancel
Dealer B
RTTM
8a.
MT509 Cancel Accepted
5b.
MT509 Trade Create Matched
8b.
MT518 Cancel Request
10a.
MT518 DK (of Cancel) Advice
9. 
MT515 DK 
(of Cancel Request)
(via WFE)
10b.
MT518 Cancel Request Modify 
(due to DK)
11. 
Cancel Remove 
(via WFE only)
12a.
MT509 Cancel Lifted (by [[participant]])
12b.
MT518 Cancel Request Cancel
(due to Contra)
 
 
15 Options are not novated. 

---

## Page 140

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 140 
DD 18: SPT Trade Accepted with Modification ([[default]] Values Applied) 
In this flow, Dealer A submits a valid Specified Pool Trade (TFTD/SPT) against Dealer B; however, the final 
money is either incorrect or not specified. The system will accept the Trade Instruct (step 2a) but override the 
final money with a system-calculated value (step 2b). The contra Dealer B will receive a Comparison Request 
advice notifying them of this trade (step 2c). 
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2c.
MT518 Comparison Request
2b.
MT518 Notification of 
[[default]] Values Applied
RTTM
 
Note: 
The trade terms reflect the [[default]] applied values (e.g., final money).  
DD 19: SPT Trade Pre-Comparison Repricing 
This flow starts with Dealer A submitting a valid Specified Pool Trade (TFTD/SPT) against Dealer B, who 
receives a Comparison Request advice notifying them of this event (step 1-2b). 
The factor of the pool associated with this trade is updated and as such, the trade’s final money is recalculated. 
The system will notify Dealer A that their trade has been updated (step 3). 
Dealer A
1. 
MT
515 Instruct
2a.
MT509 Trade Create Accepted
Dealer B
2b.
MT518 Comparison Request
3.
MT518 Repricing (*)
RTTM
Factor 
Update
 
Note: 
The trade terms reflect the updated current face and  final money.  

---

## Page 141

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 141 
DD 20: SPT Trade Post-Comparison Repricing 
This flow starts with a compared novated Specified Pool Trade (TFTD/SPT) between Dealer A and Dealer B 
(step 1-6b). 
The factor of the pool associated with this trade is updated and as such, the trade’s final money is recalculated. 
The system will notify Dealer A and Dealer B that their Trade Instructs have been updated (step 7a-b). 
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 Instruct
4b.
MT518 Comparison Request
4a.
MT509 Trade Accepted
5a.
MT509 Trade Matched
5b.
MT509 Trade Matched
6a.
518 Trade Novated
7a.
MT518 Repricing (*)
6b.
518 
Trade Novated
RTTM
5c.
MT518 Comparison Request 
Cancel (due to Match)
5d.
MT518 Comparison Request 
Cancel (due to Match)
Factor 
Update
7b.
MT518 Repricing (*)
 
Note: 
The trade terms reflect the updated current face and  final money.  

---

## Page 142

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 142 
DD 21: SPT Trade Pre-Comparison Marked for Deletion (due to Fully Paid-Down Security) 
This flow starts with Dealer A submitting a valid Specified Pool Trade (TFTD/SPT) against Dealer B, who 
receives a Comparison Request advice notifying them of this event (step 1-2b). 
The factor of the pool associated with this trade is updated and as such, the trade’s final money is recalculated. 
The system will notify Dealer A that their trade has been updated (step 3). 
At End-of-Day, since the pool has been fully paid-down, the trade is now marked-for-delete and messages are 
sent to all parties notifying them of this (step 4a-b). 
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Accepted
Dealer B
2b.
MT518 Comparison Request
3.
MT518 Repricing (*)
4a.
MT509 Instruct Deleted (due to 
Fully Paid-Down Security)
RTTM
4b.
MT518 Comparison Request 
Cancel (due to System Action)
Factor 
Update
[[EOD]] 
Processing
 
Note: 
The trade terms reflect the updated current face and  final money.  

---

## Page 143

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 143 
DD 22: SPT Trade Post-Comparison Marked for Deletion (due to Fully Paid-Down Security) 
This flow starts with a compared novated Specified Pool Trade (TFTD/SPT) between Dealer A and Dealer B 
(step 1-6b). 
The factor of the pool associated with this trade is updated and as such, the trade’s final money is recalculated. 
The system will notify Dealer A and Dealer B that their Trade Instructs have been updated (step 7a-b). 
At End-of-Day, since the pool has been fully paid-down, the trade is now marked-for-delete and messages are 
sent to all parties notifying them of this (step 8a-b). 
Dealer A
1. 
MT515 Instruct
2a.
MT509 Trade Accepted
Dealer B
2b.
MT518 Comparison Request
3. 
MT515 Instruct
4b.
MT518 Comparison Request
4a.
MT509 Trade Accepted
5a.
MT509 Trade Matched
5b.
MT509 Trade Matched
6a.
518 Trade Novated
7a.
MT518 Repricing (*)
6b.
518 Trade Novated
RTTM
5c.
MT518 Comparison Request 
Cancel (due to Match)
5d.
MT518 Comparison Request 
Cancel (due to Match)
Factor 
Update
7b.
MT518 Repricing (*)
[[EOD]] 
Processing
8a.
M509 Instruct Deleted (due to 
Fully Paid-Down Security)
8b.
M509 Instruct Deleted (due to 
Fully Paid-Down Security)
 
Note: 
The trade terms reflect the updated current  face and  final money.  
  

---

## Page 144

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 144 
DD 23: DNA Create 
In this flow, Dealer A submits a valid DNA Request specifying position to be withheld from allocation (step 1). 
The system accepts the request and assigns to individual trades based on criteria submitted in the DNA 
request (step 2a-b). 
 
 
DD 24: DNA Create (via WFE) 
In this flow, Dealer A creates a valid DNA Request via WFE, specifying position to be withheld from allocation. 
The system accepts the request and assigns to individual trades based on criteria submitted in the DNA 
request (step 1-2). 
 
 
  


---

## Page 145

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 145 
DD 25: DNA Cancel 
In this flow, Dealer A submits a valid DNA Request specifying position to be withheld from allocation (step 1). 
The system accepts the request and assigns to individual trades based on criteria submitted in the DNA 
request (step 2a-b). 
Dealer A subsequently submits a DNA cancel request, which is accepted and processed by the system, 
thereby making the associated position available for allocation (step 3-4). 
 
 
 


---

## Page 146

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 146 
[[Broker]]/Dealer Message Flows 
This appendix contains 20 possible scenarios for message flows between Brokers and Dealers: 
BD 1: Trade Create Transaction Balanced 
In this flow, [[Broker]] B submits a Trade Instruct versus Dealer A, which is accepted and marked unbalanced 
(step1-2b). [[Broker]] B submits the other side of this trade versus Dealer C, which is also accepted and marked 
unbalanced (step 3-4b). As both sides of the [[Broker]] trade are now received, the trade is “balanced” and 
notifications are sent to the [[Broker]] indicating this (step 5a-b). As a result of the balanced trade, Comparison 
Request advices are sent to the [[Buyer]] and [[Seller]], notifying them of this event (step 5c-d).  
[[Broker]] B [[Broker]] B
5c.
MT
518 Comparison Request
Dealer C
RTTM
5d.
MT518 Comparison Request
[[Broker]] B
2b.
MT509 Trade Create Unbalanced
5a.
MT509 Trade Create Balanced
2a.
MT509 Trade Create Accepted
4a.
MT509 Trade Create Accepted
4b.
MT509  Trade Create Unbalanced
5b.
MT509 Trade Create Balanced
1. 
MT515 Instruct (vs. A)
3. 
MT515 Instruct (vs. C)
Dealer A
[[Broker]] B
 

---

## Page 147

MBSD RTTM® [[Novation]]:  
SWIFT Interac tive Messaging Specifications  
Appendices 147 
BD 2: Balanced Trade Create Transaction Submitted (via WFE) 
In this flow, [[Broker]] B creates a trade versus Dealer A and Dealer B via the WFE, resulting in a balanced trade 
(step 1-3b). Comparison Requests advices are sent to the [[Buyer]] and [[Seller]], notifying them of this event (step 
3c-d).  
[[Broker]] B [[Broker]] B
3c.
MT518 Comparison Request
Dealer C
RTTM
3d.
MT518 Comparison Request
[[Broker]] B
2b.
MT509 Trade Create Unbalanced
3a.
MT509 Trade Create Balanced
2a.
MT518 Screen Input Trade 
Replay (Instruct)
2c.
MT518 Screen Input Trade 
Replay (Instruct)
2d.
MT509  Trade Create Unbalanced
3b.
MT509 Trade Create Balanced
1. 
Instruct via WFE
(vs. A and C)
Dealer A
[[Broker]] B
 

---

## Page 148

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 148 
BD 3: PMAT Trade 
This flow starts with a balanced [[Broker]] trade from [[Broker]] B versus Dealer A and Dealer C (step 1-5b), with 
Comparison Request advices generated for Dealer A and Dealer C (step 5c-d). 
Dealer A responds by sending a matching Trade Instruct, generating a Comparison Request to [[Broker]] B (step 
6-7b). The trades are matched by the system, with Trade Matched messages sent to the [[Broker]] and Dealer A 
(step 8a-b), as well as notification to the [[Broker]] that their trade is PMAT (9a). Lastly, previously submitted 
Comparison Request advices to the [[Broker]] (for A’s trade) and Dealer A (for [[Broker]]’s trade) are canceled (9b-
c). 
[[Broker]] B [[Broker]] B
5c.
MT518 Comparison Request
Dealer C
5d.
MT518 Comparison Request
[[Broker]] B
2b.
MT509 Trade Create Unbalanced
5a.
MT509 Trade Create Balanced
2a.
MT509 Trade Create Accepted
4a.
MT509 Trade Create Accepted
4b.
MT509  Trade Create Unbalanced
5b.
MT509 Trade Create Balanced
1. 
MT515 Instruct (vs. A)
3. 
MT515 Instruct (vs. C)
Dealer A
[[Broker]] B
RTTM
7a.
MT509 Trade Create Accepted
8a.
MT509 Trade Create Matched
9b.
MT518 Comparison Request 
Cancel (due to match)
7b.
MT518 Comparison Request
8b.
MT509 Trade Create Matched
9a.
MT509 Trade PMAT (short side)
9c.
MT518 Comparison Request 
Cancel (due to match)
BD7
BD10
BD11
BD12
BD13
BD5
BD20
BD18
6. 
MT515 Instruct
 

---

## Page 149

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 149 
BD 4: Dealer Trade Create DK’ed by [[Broker]] 
This flow starts with Dealer A submitting a Trade Instruct against [[Broker]] B, who receives a Comparison 
Request advice notifying them of this event (step 1-2b).  
The [[Broker]] then submits a DK, which causes their own Comparison Request to be updated due to this action, 
as well as generating a DK Advice to Dealer A, informing them of the DK event and reason (step 3-4d). 
[[Broker]] BDealer A
RTTM
2a.
MT509 Trade Create Accepted
4c.
MT518 DK Advice
2b.
MT518 Comparison Request
4a.
MT509 DK Accepted
4b.
MT518 Comparison Request 
Modify (due to DK)
4d.
MT509 DK Processed
1. 
MT515 Instruct 
(vs. B)
3. 
MT515 DK
 

---

## Page 150

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 150 
BD 5: PMAT Trade DK’ed by Unmatched Dealer, [[Broker]] Modifies Contra 
This flow starts with a PMAT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) (flow 
BD3). 
Dealer C then submits a DK, which causes their own Comparison Request to be updated due to this action, as 
well as generating a DK Advice to [[Broker]] B, informing them of the DK event and reason (step 10-11d). 
[[Broker]] B responds by modifying the contra on the trade from Dealer C to Dealer D, which causes the 
Comparison Request previously sent to Contra C to be canceled, and a new one generated for Dealer D (step 
12-13d). Lastly, the DK Advice previously received by [[Broker]] B (from Dealer C) is now removed (step 13e) 
 
 


---

## Page 151

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 151 
DB 6: Commission Modified by [[Broker]] on Unmatched Side of PMAT Trade 
This flow starts with a PMAT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) (steps 
1-9c). 
[[Broker]] B then modifies the commission on the unmatched side of the trade, generating a Comparison Request 
advice update for Dealer C notifying them of this change (step 10-11c).
[[Broker]] B [[Broker]] B
5c.
MT
518 Comparison Request
Dealer C
5d.
MT
518 Comparison Request
[[Broker]] B
2b.
MT
509 Trade Create Unbalanced
5a.
MT
509 Trade Create Balanced
2a.
MT
509 Trade Create Accepted
4a.
MT
509 Trade Create Accepted
4b.
MT
509  Trade Create Unbalanced
5b.
MT
509 Trade Create Balanced
1. 
MT515 Instruct (vs. A)
3. 
MT515 Instruct (vs. C)
Dealer A
[[Broker]] B
RTTM
7a.
MT
509 Trade Create Accepted
8a.
MT
509 Trade Create Matched
9b.
MT
518 Comparison Request 
Cancel (due to match)
7b.
MT
518 Comparison Request
8b.
MT
509 Trade Create Matched
9a.
MT
509 Trade PMAT (short side)
9c.
MT
518 Comparison Request 
Cancel (due to match)
6. 
MT515 Instruct
10. 
MT515 Modify
11c.
MT
518 Comparison Request 
Modify (due to contra)
11a.
MT
509 Modify Accepted
11b.
MT
509 Modify Processed
 
 

---

## Page 152

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 152 
BD 7: PMAT [[Broker]] Trade Modify (on Contra [[ID]]) Results in FMAT 
This flow starts with a PMAT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) (flow 
BD3).  
The [[Broker]] modifies the contra of the trade to be Dealer D and notifications are sent to Dealer C (to cancel the 
Comparison Request advice) and Dealer D (to advise them of the new Comparison Request advice) (step 10-
11d). Dealer D responds by sending a matching Trade Instruct, resulting in Trade Matched messages to the 
[[Broker]] and dealer, as well as notification to the [[Broker]] that their trade is PMAT (12-15a). Previously submit 
Comparison Request advices are canceled (step 15b-c) and the [[Broker]] receives notification that their trade is 
now FMAT (step 16). Lastly, [[Novation]] occurs and Dealers A and B are informed of this event (step 17a-b). 
Dealer C [[Broker]] B
11d.
MT518 Comparison Request
[[Broker]] BDealer D
13a.
MT509 Trade Create Accepted
14a.
MT509 Trade Create Matched
15c.
MT518 Comparison Request 
Cancel (due to match)
13b.
MT518 Comparison Request
14b.
MT509 Trade Create Matched
15a.
MT509 Trade PMAT (long side)
15b.
MT518 Comparison Request 
Cancel (due to match)
12. 
MT515 Instruct
16.
MT509 Trade FMAT
(continued from 
PMAT flow BD3)
10. 
MT515 Modify
11a.
MT509 Modify Accepted
11b.
MT509 Modify Processed
17a.
MT518 Trade Novated
11c.
MT518 Comparison Request 
Cancel (due to contra)
Dealer A
RTTM
17b.
MT518 Trade Novated
 

---

## Page 153

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 153 
BD 8: [[Broker]] Reference Modified by [[Broker]] on Trade with PMAT Status 
This flow starts with a PMAT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) (steps 
1-9c). 
[[Broker]] B then modifies their [[Broker]] reference number, which is accepted and processed by the system (step 
10-11b). The contra dealers are not notified of this change.
 
[[Broker]] B [[Broker]] B
5c.
MT518 Comparison Request
Dealer C
5d.
MT518 Comparison Request
[[Broker]] B
2b.
MT509 Trade Create Unbalanced
5a.
MT509 Trade Create Balanced
2a.
MT509 Trade Create Accepted
4a.
MT509 Trade Create Accepted
4b.
MT509  Trade Create Unbalanced
5b.
MT509 Trade Create Balanced
1. 
MT515 Instruct (vs. A)
3. 
MT515 Instruct (vs. C)
Dealer A
[[Broker]] B
RTTM
7a.
MT509 Trade Create Accepted
8a.
MT509 Trade Create Matched
9b.
MT518 Comparison Request 
Cancel (due to match)
7b.
MT518 Comparison Request
8b.
MT509 Trade Create Matched
9a.
MT509 Trade PMAT (short side)
9c.
MT518 Comparison Request 
Cancel (due to match)
6. 
MT515 Instruct
10. 
MT515 Modify Set
11a.
MT509 Modify Set Accepted
11b.
MT509 Modify Set Processed
 

---

## Page 154

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 154 
BD 9: PMAT Modified ([[Broker]] Ref) by [[Broker]] (via WFE) 
This flow starts with a PMAT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) (steps 
1-9c). 
[[Broker]] B then modifies their [[Broker]] reference number via WFE, resulting in a screen input replay notification to 
the [[Broker]] of this event (step 10-11). The contra dealers are not notified of this change. 
[[Broker]] B [[Broker]] B
5c.
MT518 Comparison Request
Dealer C
5d.
MT518 Comparison Request
[[Broker]] B
2b.
MT509 Trade Create Unbalanced
5a.
MT509 Trade Create Balanced
2a.
MT509 Trade Create Accepted
4a.
MT509 Trade Create Accepted
4b.
MT509  Trade Create Unbalanced
5b.
MT509 Trade Create Balanced
1. 
MT515 Instruct (vs. A)
3. 
MT515 Instruct (vs. C)
Dealer A
[[Broker]] B
RTTM
7a.
MT509 Trade Create Accepted
8a.
MT509 Trade Create Matched
9b.
MT518 Comparison Request 
Cancel (due to match)
7b.
MT518 Comparison Request
8b.
MT509 Trade Create Matched
9a.
MT509 Trade PMAT (short side)
9c.
MT518 Comparison Request 
Cancel (due to match)
6. 
MT515 Instruct
10. 
Modify Set
(via WFE)
11.
MT518 Screen Input 
Set Replay (modify)
 

---

## Page 155

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 155 
BD 10: PMAT Trade Canceled (Initiated by [[Broker]]) 
This flow starts with a PMAT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) (flow 
BD3). 
[[Broker]] B then submits a cancel set, which causes a Cancel Request to be sent to the matching Dealer A, 
informing them of this event (step 10-11b). 
Dealer A responds by submitting a matching cancel, resulting in the both [[Broker]] and dealer trades being 
canceled, as well as the Comparison Request advice to the unmatching Dealer C (step 12-13e). 
Dealer A [[Broker]] B
[[Broker]] BDealer C
13d.
MT518 Comparison Request 
Cancel (due to contra)
(continued from 
PMAT flow BD3)
10. 
MT515 Cancel Set
11a.
MT509 Cancel Set Accepted
13b.
MT518 Cancel Request
RTTM 13e.
MT509 Cancel Set Processed
11b.
MT518 Cancel Request
13a.
MT509 Cancel Accepted
13c.
MT509 Cancel Processed
12. 
MT515 Cancel
 

---

## Page 156

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 156 
BD 11: Unsuccessful Attempt by [[Broker]] to Cancel a PMAT Trade 
This flow starts with a PMAT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) (flow 
BD3). 
[[Broker]] B submits a cancel set, which causes a Cancel Request to be sent to the matching Dealer A, informing 
them of this event (step 10-11b). However, unmatching Dealer C submits a matching Trade Instruct, resulting 
in Trade Matched messages to the [[Broker]] and dealer, as well as notification to the [[Broker]] that their trade is 
PMAT (12-15a). Previously submit Comparison Request advices are canceled (step 15b-c) and the [[Broker]] 
receives notification that their trade is now FMAT (step 16). In addition, previously initiated [[Broker]] cancel 
requests are lifted/canceled (step 17a-b). Lastly, [[Novation]] now occurs, with Dealers A and C being informed of 
this event (step 17a-b). 
Dealer A [[Broker]] B
[[Broker]] BDealer C
13a.
MT509 Trade Create Accepted
14a.
MT509 Trade Create Matched
15c.
MT518 Comparison Request 
Cancel (due to match)
13b.
MT518 Comparison Request
14b.
MT509 Trade Create Matched
15a.
MT509 Trade PMAT (long side)
15b.
MT518 Comparison Request 
Cancel (due to match)
12. 
MT515 Instruct
16.
MT509 Trade FMAT
(continued from 
PMAT flow BD3)
10. 
MT515 Cancel Set
11a.
MT509 Cancel Set Accepted
18a.
MT518 Trade Novated
Dealer A
11b.
MT518 Cancel Request
17a.
MT509 Cancel Set Lifted 
(due to RTTM)
18b.
MT518 Trade Novated
RTTM
17b.
MT518 Cancel Request 
Cancel (due to RTTM)
 

---

## Page 157

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications 
Appendices 157 
BD 12: Initially Unsuccessful Attempt by Dealer to Cancel a PMAT Trade 
This flow starts with a PMAT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) (flow 
BD3).  
Dealer A submits a cancel, which causes a Cancel Request advice to be sent to [[Broker]] B (step 10-11b). 
However, before the [[Broker]] can respond to this advice, Dealer C submits a matching Trade Instruct (step 12-
13b), causing the trade to be become fully matched (and therefore novated) (step 14a-17b). In addition, the 
Cancel Request is transferred from [[Broker]] to Dealer C (step 18a-c). Dealer C responds to the request by 
submitting a matching Cancel, resulting in trade cancellation with informational messages sent to the [[Broker]] on 
these events (19-20g). 
Dealer A [[Broker]] B
[[Broker]] BDealer C
13a.
MT509 Trade Create Accepted
14a.
MT509 Trade Create Matched
15c.
MT518 Comparison Request 
Cancel (due to match)
13b.
MT518 Comparison Request
14b.
MT509 Trade Create Matched
15a.
MT509 Trade PMAT (long side)
15b.
MT518 Comparison Request 
Cancel (due to match)
12. 
MT515 Instruct
16.
MT509 Trade FMAT
(continued from 
PMAT flow BD3)
10. 
MT515 Cancel
11a.
MT509 Cancel Accepted
Dealer A
11b.
MT518 Cancel Request
18a.
MT518 Cancel Request 
Cancel (due to RTTM)
18c.
MT518 Cancel Request
18b.
MT518 Cancel Request (A Info)
Dealer C 19.
MT515 Cancel
17a.
MT518 Trade Novated
20a.
MT509 Cancel Accepted
[[Broker]] B
20d.
MT509 Cancel Processed
20b.
MT518 Cancel Request (C Info)
20g.
MT518 Cancel Processed (A Info)
17b.
MT518 Trade Novated
20c.
MT518 Cancel request 20f.
MT518 Cancel Processed (C Info)
RTTM
20e.
MT509 Cancel Processed
 

---

## Page 158

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 158 
BD 1: PMAT SBOD Converted to TFTD 
This flow starts with a PMAT SBOD trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) 
(flow BD3). 
At the onset of TBA Netting, the PMAT SBOD trade is converted to a TFTD, with Dealer A and [[Broker]] B 
receiving Post-Comparison Modify Advices for their compared trades (step 10a-b), Dealer C receiving a 
Comparison Request Modify advice for their previously received advisory (step 10c), and [[Broker]] B receiving a 
Screen Input Trade Replay to inform them of the update to the uncompared side of their trade (step 10d). 
Dealer A [[Broker]] B
[[Broker]] BDealer C
10c.
MT518 Comparison Request 
Modify (due to RTTM)
(continued from 
PMAT flow BD3)
10a.
MT518 Post Comparison 
Modify Advice (due to RTTM)
RTTM
10d.
MT518 Screen Input Trade 
Replay (due to RTTM)
10b.
MT518 Post Comparison 
Modify Advice (due to RTTM)
TBA Net 
Pre-
Processing
 

---

## Page 159

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 159 
BD 14: FMAT and Novated Trade 
This flow starts with a PMAT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) (flow 
BD6).  
The unmatching Dealer C then submits in a matching Trade Instruct, resulting in Trade Matched messages to 
the [[Broker]] and dealer, as well as notification to the [[Broker]] that their trade is PMAT (10-13a). Previously 
submitted Comparison Request advices are canceled (step 13b-c) and the [[Broker]] receives notification that 
their trade is now FMAT (step 14). Lastly, [[Novation]] occurs and Dealers A and B are informed of this event (step 
15a-b). 
[[Broker]] B [[Broker]] B
5c.
MT518 Comparison Request
5d.
MT518 Comparison Request
[[Broker]] B
2b.
MT509 Trade Create Unbalanced
5a.
MT509 Trade Create Balanced
2a.
MT509 Trade Create Accepted
4a.
MT509 Trade Create Accepted
4b.
MT509  Trade Create Unbalanced
5b.
MT509 Trade Create Balanced
1. 
MT515 Instruct (vs. A)
3. 
MT515 Instruct (vs. C)
Dealer A
7a.
MT509 Trade Create Accepted
8a.
MT509 Trade Create Matched
9b.
MT518 Comparison Request 
Cancel (due to match)
7b.
MT518 Comparison Request
8b.
MT509 Trade Create Matched
9a.
MT509 Trade PMAT (short side)
9c.
MT518 Comparison Request 
Cancel (due to match)
6. 
MT515 Instruct
5d.
MT518 Comparison Request
[[Broker]] BDealer C
11a.
MT509 Trade Create Accepted
12a.
MT509 Trade Create Matched
13c.
MT518 Comparison Request 
Cancel (due to match)
11b.
MT518 Comparison Request
12b.
MT509 Trade Create Matched
13a.
MT509 Trade PMAT (long side)
13b.
MT518 Comparison Request 
Cancel (due to match)
10. 
MT515 Instruct
RTTM
14.
MT509 Trade FMAT
15a.
MT518 Trade Novated
15b.
MT518 Trade Novated
BD15 BD16 BD17
Go to 
flows
 

---

## Page 160

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 160 
BD 2: FMAT Trade Canceled 
This flow starts with a FMAT and novated trade between [[Broker]] B, Dealer A and Dealer C (flow BD14). 
Dealer A then initiates a Cancel Request, which results in a Cancel Request advice being sent to Dealer B (as 
the trade is compared, the cancel must be bilaterally agreed upon), as well as an informational message to the 
[[Broker]] (step 16-17c). Dealer C responds to the Cancel Request advice by submitting a matching Cancel 
Request, likewise resulting in a Cancel Request advice being sent to Dealer A, as well as an informational 
message to [[Broker]] B (step 18-19c). As the cancel is bilaterally agreed upon, the trade is canceled, with 
informational messages sent to the [[Broker]] (step 20a-d) 
Dealer A [[Broker]] B
[[Broker]] BDealer C
17c.
MT518 Cancel Request
(continued from FMAT 
flow BD14)
17b.
MT518 Cancel Request (A Info)
RTTM
19b.
MT518 Cancel Request (C Info)
17a.
MT509 Cancel Accepted
16. 
MT515 Cancel
18. 
MT515 Cancel
19a.
MT509 Cancel Accepted
20a.
MT509 Cancel Processed
20c.
MT509 Cancel Processed (A Info)
20d.
MT509 Cancel Processed (C Info)
19c.
MT518 Cancel Request
20b.
MT509 Cancel Processed
 

---

## Page 161

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 161 
BD 16: FMAT Trade Cancel Request DK’ed 
This flow starts with a FMAT and novated trade between [[Broker]] B, Dealer A and Dealer C (flow BD14). 
Dealer A then initiates a Cancel Request, which results in a Cancel Request advice being sent to [[Broker]] B (as 
the trade is compared, the cancel must be bilaterally agreed upon), as well as an informational message to the 
[[Broker]] (step 16-17c). Dealer C responds to the Cancel Request advice by submitting a valid DK (step 18-19b), 
thereby modifying this advice (step 19c), informing the [[Broker]] of this (step 19d) and generating a DK of Cancel 
Advice being sent to Dealer A (step 19e). 
Dealer A [[Broker]] B
[[Broker]] BDealer C
17c.
MT518 Cancel Request
(continued from FMAT 
flow BD14)
17b.
MT518 Cancel Request (A Info)
RTTM
17a.
MT509 Cancel Accepted
16. 
MT515 Cancel
18. 
MT515 DK (Cancel)
19a.
MT509 DK (Cancel) Accepted
19b.
MT509 DK (Cancel) Processed
19e.
MT518 DK (Cancel) Advice
19c.
MT518 Cancel Request 
Modify (due to DK)
19d.
MT518 DK (Cancel) Advice (Info)
 

---

## Page 162

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 162 
BD 17: FMAT Cancel Request DK’ed, Then Cancel Removed 
This flow starts with a FMAT and novated trade between [[Broker]] B, Dealer A and Dealer C (flow BD14). 
Dealer A then initiates a Cancel Request, which results in a Cancel Request advice being sent to [[Broker]] B (as 
the trade is compared, the cancel must be bilaterally agreed upon (step 16-17c). Dealer C responds to the 
Cancel Request advice by submitting a valid DK, thereby modifying this advice (due to DK) and generating a 
DK of Cancel Advice for Dealer A (step 18-19e). 
Dealer A then removes the Cancel via WFE, resulting in the Cancel Request advice to Dealer C being 
canceled (step 20-21c). Note that the [[Broker]] receives informational notification regarding these events (in step 
17b, 19b and 21c). 
Dealer A [[Broker]] B
[[Broker]] BDealer C
17c.
MT518 Cancel Request
(continued from FMAT 
flow BD14)
17b.
MT518 Cancel Request (A Info)
RTTM
17a.
MT509 Cancel Accepted
16. 
MT515 Cancel
18. 
MT515 DK (Cancel)
19a.
MT509 DK (Cancel) Accepted
19b.
MT509 DK (Cancel) Processed
19e.
MT518 DK (Cancel) Advice
19c.
MT518 Cancel Request 
Modify (due to DK)
19d.
MT518 DK (Cancel) Advice (Info)
20. 
Cancel Remove 
(via WFE)
21a.
MT509 Cancel Lifted (by [[participant]])
21b.
MT518 Cancel Request 
Cancel (due to contra)
21c.
MT518 Cancel Request 
Cancel (Info)
 

---

## Page 163

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 163 
BD 18: PMAT SPT Repricing 
This flow starts with a PMAT SPT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) 
(flow BD3).  
The factor of the pool associated with this trade is updated and as such, the trade’s final money is recalculated. 
The system will notify the [[Broker]], Dealer A and Dealer B that their Trade Instructs have been updated (step 
10a-c). Dealer A [[Broker]] B
10c.
MT518 Repricing (*)
10a.
MT518 Repricing (*) vs. A
RTTM
(continued from 
PMAT flow BD3)
Repricing
10b.
MT518 Repricing (*) vs. C
 
Note: 
The trade terms reflect the updated current face and  final money.  

---

## Page 164

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifi cations 
Appendices 164 
BD 19: [[Broker]] SPT Trade Accepted with Modifications ([[default]] Values Applied) 
In this flow, [[Broker]] B submits 2 Specified Pool Trade (TFTD/SPT) Trade Instructs, one versus Dealer A and 
one versus Dealer C (step 1 and 3); however, the final money is either incorrect or not specified. The system 
will accept the Trade Instructs (step 2a-b and 4a-b) but override the final money with a system-calculated value 
(step 2c and 4c). As both sides are received, notifications are sent to the [[Broker]] that this trade is balanced 
(step 5a-b), as well as Comparison Requests advices to the [[Buyer]] and [[Seller]], notifying them of this event (step 
5c-d). 
[[Broker]] B [[Broker]] B
5c.
MT518 Comparison Request
Dealer C
5d.
MT518 Comparison Request
[[Broker]] B
2b.
MT509 Trade Create Unbalanced
2a.
MT509 Trade Create Accepted
RTTM
4a.
MT509 Trade Create Accepted
4b.
MT509  Trade Create Unbalanced
4c.
MT518 [[default]] Values Applied (*)
1. 
MT515 Instruct (vs. A)
3. 
MT515 Instruct (vs. C)
Dealer A
[[Broker]] B
2c.
MT518 [[default]] Values Applied (*)
5a.
MT509 Trade Create Balanced
5b.
MT509 Trade Create Balanced
 
Note: 
The trade terms reflect the [[default]] applied values (e.g., final money).  

---

## Page 165

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 165 
BD 20: PMAT SPT Trade Marked for Deletion 
This flow starts with a PMAT SPT trade between [[Broker]] B, Dealer A (matching) and Dealer C (unmatching) 
(flow BD3).  
The factor of the pool associated with this trade is updated and as such, the trade’s final money is recalculated. 
The system will notify the [[Broker]], Dealer A and Dealer B that their Trade Instructs have been updated (step 
10a-c). 
At End-of-Day, since the pool has been fully paid-down, the trade is now marked-for-delete, and messages are 
sent to all parties notifying them of this (step 11a-d). Dealer A [[Broker]] B
10c.
MT518 Repricing (*)
10a.
MT518 Repricing (*) vs. A
RTTM
(continued from 
PMAT flow BD3)
Repricing
11a.
MT509 Instruct Deleted (due to 
Fully Paid-Down Security) vs. A
11b.
MT509 Instruct Deleted (due to 
Fully Paid-Down Security) vs. C
11c.
MT509 Instruct Deleted (due to 
Fully Paid-Down Security) [[EOD]] 
Processing
10b.
MT518 Repricing (*) vs. C
Dealer C
11d.
MT518 Comparison Request 
Cancel (due to System Action)
 
Note: 
The trade terms reflect the [[default]] applied values (e.g., final money).  
  

---

## Page 166

MBSD RTTM® [[Novation]]:  
SWIFT Interactive Messaging Specifications  
Appendices 166 
Rejection Message Flows 
When an invalid MT515 message is submitted, the system responses with a MT509 “rejection” message rather 
than MT509 “acknowledgement” message. Within this rejection message, the reason(s) for rejection are 
provided. 
Note: 
Rejection messages are not generated in response to invalid actions submitted via the WFE; in these cases, the WFE 
immediately displays the rejection reasons and as such, no rejection message is required.  
In the table below, the “rejection” messages generated in response to an invalid action initiated via messaging 
are shown. 
MT515 Input Message “Rejection” Response Message 
MT515 Instruct  MT509 Instruct Rejected  
MT515 Cancel  MT509 Cancel Rejected  
MT515 Cancel Set MT509 Cancel Set Rejected  
MT515 Modify  MT509 Modify Rejected  
MT515 Modify Set  MT509 Modify Set Rejected  
MT515 DK MT509 DK Rejected  
MT515 DNA MT509 DNA Rejected  
MT515 Cancel DNA MT509 Cancel DNA Rejected  
 
A single message flow sample is provided to demonstrate this flow; the flow is the same regardless of the input 
message type. 
[[participant]] A
1. 
MT515 Instruct
RTTM
2.
MT509 Instruct Rejected
 
 

---

## Page 167

 
 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
DTCCLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 