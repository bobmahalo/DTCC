---
title: "CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cmu115-input-output-spec_2022Mar23.pdf"
pages: 348
size: "5382.4 KB"
category: "Connectivity_MQ"
ingested_on: "2026-06-05"
---

# CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide

**Original File:** [cmu115-input-output-spec_2022Mar23.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/cmu115-input-output-spec_2022Mar23.pdf)  
**Category:** Connectivity_MQ  
**Total Pages:** 348  
**File Size:** 5382.4 KB  

---

## Page 1

CORPORATE, MUNICIPAL, AND [[UIT]] 
(CMU) 
CMU RTTM INTERACTIVE MESSAGING SPECIFICATIONS FOR TRADE 
INPUT AND OUTPUT
VERSION 2.5 
MARCH 23, 2022 


---

## Page 2

© 2022 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
Doc Date: March 23, 2022 
Publication Code: CMU115 
Service: Corporate, Municipal, and [[UIT]] (CMU) 
Title: CMU RTTM Interactive Messaging Specifications for Trade Input and Output

---

## Page 3

 
 
TABLE OF CONTENTS 
1. Overview ........................................................................................................................................................... 7 
Scope .................................................................................................................................................................. 7 
Audience ............................................................................................................................................................. 8 
Related Information............................................................................................................................................. 8 
Contact Us .......................................................................................................................................................... 8 
2. [[NSCC]] Interactive Messaging for CMU Real-Time Trade Matching (CMU RTTM) ........................................ 9 
CMU RTTM Service Features ............................................................................................................................ 9 
CMU RTTM Role in Regulatory Reporting to the MSRB .................................................................................... 9 
Submission Rules to Facilitate Regulatory Reporting ......................................................................................10 
MSRB Reporting .............................................................................................................................................11 
Customer and Interdealer Regulatory-Only Trades ........................................................................................12 
3. Interactive Message Guidelines.................................................................................................................... 13 
ISO 15022 Message Structure .........................................................................................................................13 
Message Header .............................................................................................................................................14 
Blocks and Sub-blocks ....................................................................................................................................14 
Fields ...............................................................................................................................................................15 
Tag and Field Format Illustrations and Chart ..................................................................................................16 
Illustrating the Message Structure ...................................................................................................................17 
CMU RTTM Trade Flow ....................................................................................................................................18 
CMU RTTM Trade Flow Showing MSRB Messages ........................................................................................21 
Data Format Differences ...................................................................................................................................23 
4. Communication Overview ............................................................................................................................. 24 
Message Exchange ..........................................................................................................................................24 
5. Message Specifications ................................................................................................................................. 25 
Message Format Guidelines .............................................................................................................................26 
Typical Message Form ....................................................................................................................................28 
Message Header Format .................................................................................................................................29 
MT515 Message................................................................................................................................................30 

---

## Page 4

 
 
MT515 Message Specification ........................................................................................................................31 
MT515 General Format ...................................................................................................................................31 
MT515 Field Specifications .............................................................................................................................36 
MT515 Field Analysis ......................................................................................................................................44 
MT509 Message ...............................................................................................................................................48 
MT509 General Format ...................................................................................................................................51 
MT509 Message Specification ........................................................................................................................52 
MT509 Field Specifications .............................................................................................................................53 
MT509 Field Analysis ......................................................................................................................................56 
Table 1 (PACK, REJT, MODA, MODP, DELE, DEDK, DEME, DEPE, DESD) .............................................56 
Table 2 (PADK, DKRJ, DPPR, ASME, ASPE, RVME, RVPE) ......................................................................60 
Table 3 (CPRC//PACK, CRPC//REJT, CRPC//CAND and MTCH) ...............................................................63 
MT518 Message ...............................................................................................................................................65 
MT518 Message Specification ........................................................................................................................66 
MT518 General Format ...................................................................................................................................68 
MT518 Field Specifications .............................................................................................................................71 
MT518 Field Analysis (CMPM, DFVA, SITR, NAFI, DCCX, YTPR, STLD) ....................................................79 
MT518 Field Analysis Table 2 (CMPR, CRQM, CADV, CMDS, LCTA) ..........................................................84 
MT599 Message ...............................................................................................................................................88 
MT599 Message Specification ........................................................................................................................88 
MT599 Format Differences ..............................................................................................................................89 
MT599 General Format ..................................................................................................................................89 
MT599 Field Specifications .............................................................................................................................90 
LISTING OF APPENDICES ................................................................................................................................. 91 
Appendix A: Mandatory Data for [[NSCC]] CMU RTTM ....................................................................................... 92 
Appendix B: Message Flows ............................................................................................................................. 94 
Bilateral Trade Flows .........................................................................................................................................95 
Demand Trade Flows ......................................................................................................................................129 
Locked-in Trade Flows ....................................................................................................................................154 
Appendix C: Message Samples ...................................................................................................................... 174 

---

## Page 5

 
 
Sample Trade 1: Municipal Bond (Bilateral Regular Way Match) ..................................................................174 
Part A – Regular Way Trade Match ..............................................................................................................176 
Part B – Regular Way Trade – Cancel ..........................................................................................................190 
Part C – Regular Way Trade – DK ................................................................................................................193 
Part D – Regular Way Trade – Modify ..........................................................................................................196 
Part E – Regular Way Trade – Miscellaneous ..............................................................................................201 
Sample Trade 2: Municipal Bond (New Issue/Repriced) .................................................................................206 
Sample Trade 3: Municipal Bond [[syndicate]] (Demand) Submission ..............................................................222 
Part A - [[syndicate]] Manager (Client A) Submits ............................................................................................224 
Part B - [[syndicate]] [[Member]] (Client B) Submits Without Target Indicator .....................................................233 
Part C - [[syndicate]] [[Member]] (Client B) Submits with Target Indicator ...........................................................241 
Part D - [[syndicate]] Manager (Client A) Submits Reversal ............................................................................248 
Sample Trade #4: Municipal Bond - Pending Status (Assigned, Removed or Trade Deleted) .......................249 
Sample Trade #5: Municipal Bond - Memo Status (Assigned, Removed or Trade Deleted) .........................253 
MT509 Trade Accepted Sent to Client B .....................................................................................................255 
MT509 Memo Status Assigned Sent to Client B .........................................................................................256 
MT509 Memo Status Removed sent to Client B .........................................................................................256 
Sample Trade #6: Corporate Bond - Regular Way Trade ..............................................................................259 
Part A - Regular Way Trade Match ...............................................................................................................260 
Part B - Regular Way Trade – Unmatched ....................................................................................................273 
Part C - Regular Way Trade Reversal ...........................................................................................................275 
Sample Trade #7: Corporate Bond Regular Way (Modify and Match) ............................................................276 
Part A - Trade Modify and Trade Match ........................................................................................................278 
Part B - Post Matching Modification of Internal Reference Number .............................................................296 
Sample Trade #8: Corporate Bond Regular Way DK Processing ..................................................................298 
Part A - DK and Delete ..................................................................................................................................303 
Part B - DK and Modify ..................................................................................................................................308 
Part C - DK Remove ......................................................................................................................................312 
Sample Trade #9: Unit Investment Trust QSR (Locked-in) Trade .................................................................314 
Part A - QSR Submitter (Client B) Submits Buy Trade – Administrative Match (no contra submission) .......316 

---

## Page 6

 
 
Part B - QSR Contra (Client A) Submits a Sell Trade With Target Indicator.................................................326 
Part C - QSR Contra (Client A) Submits a Sell Trade Without Target Indicator ...........................................328 
Part D - QSR Submits a Reversal .................................................................................................................333 
Appendix D: Message Structure Diagrams ................................................................................................... 336 
Message Structure Diagrams – MT515 ..........................................................................................................336 
Message Structure Diagrams – MT509 ...........................................................................................................337 
Message Structure Diagrams – MT518 ...........................................................................................................338 
Appendix E: CMU RTTM Code Tables ............................................................................................................ 339 
Message Reject Reason Codes ......................................................................................................................339 
[[settlement]] Disposition Codes .........................................................................................................................341 
DK Reason Codes ..........................................................................................................................................341 
Message Reason Codes ................................................................................................................................342 
Destination Codes...........................................................................................................................................342 
Issue Type .......................................................................................................................................................342 
Appendix F: MT518 Processing of Regulatory Fields .................................................................................. 343 
Appendix G: MSRB Regulatory Information .................................................................................................. 344 
MSRB Regulatory Fields ................................................................................................................................344 
MSRB Special Condition Indicator Codes ......................................................................................................345 
Message Originator (MEOR) Codes ...............................................................................................................346 
Appendix H: [[settlement]] Type Indicator Field Mapping ................................................................................ 347 
 

---

## Page 7

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Overview 7 
1. OVERVIEW 
This document provides an updated overview of interactive messaging for Corporate, Municipal, and [[UIT]] 
(CMU) real-time trade matching (RTTM) for the fixed income products of the National [[securities]] Clearing 
Corporation ([[NSCC]]). Its main purpose is to provide the required detailed input and output specifications for 
messages that are used to support the process. An effort was made to ensure that they are  consistent with 
interactive messaging specifications developed by the Fixed Income Clearing Corporation ([[FICC]]) to support 
both government and mortgage-backed [[securities]]. This was done to minimize the coding efforts of clients that 
subscribe to interactive services of several fixed income products and to promote standardized messaging 
conventions, whenever possible. 
A brief overview of the service features includes: 
• Establishing a hub for fixed income markets.  The hub facilitates routing information received through a 
single pipeline to the appropriate destination, such as clearing corporation or regulator. 
• Utilizing a standardized messaging for fixed income products. CMU RTTM supports international 
organization of standardization (ISO) 15022 formats for all inbound and outbound messages. 
• Real-time input, for bilateral or unilateral submission through messages or a web based interface, of trade 
data for matching or price reporting purposes. 
• Real-time output, through messaging or  a web based interface, to manage intra-day risks associated 
with unmatched trades. 
As new features are added to the existing service, additions and modifications to these specifications may be 
required. 
Scope 
The service offered to [[NSCC]] clients includes the ability to submit messages to facilitate matching and 
[[settlement]] and to also direct those messages to the Municipal [[securities]] Rulemaking Board (MSRB). Clients 
can submit one message for the purpose of both real-time trade matching and regulatory price reporting. The 
Regulatory Reporting service and related information are described in CMU RTTM Role in Regulatory 
Reporting to the MSRB and Submission Rules to Facilitate Regulatory Reporting sections. 
This document provides the detailed specification for all [[NSCC]] client input to and output from CMU RTTM. It 
also provides the ability to submit to the MSRB. The following items are outside the scope of this document: 
• Detail of how the formats and data in this specification relate to regulatory requirements for clients. 
• Interactive output specifications from the regulators. 
  

---

## Page 8

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Overview 8 
Audience 
This document is intended for systems and development personnel including managers, analysts, and 
programmers. It is intended for clients of [[NSCC]] fixed income products only. It presumes you are familiar with 
technical concepts and terms and that you have a [[BASIC]] understanding of [[NSCC]] fixed income products and 
services. 
Related Information 
The specifications for interactive messages supporting trade matching are based on ISO15022 SWIFT 
messages. For a high-level overview of the structure of Society for Worldwide Interbank Financial 
Telecommunications (SWIFT) messages, see Interactive Message Guidelines. This section provides readers 
with a general idea of how SWIFT messages are structured; it is not intended to replace SWIFT 
documentation in any way. Readers are strongly urged to see the SWIFT user documentation to obtain 
a complete and comprehensive understanding of these message standards. Resources include: the 
SWIFT User Handbook. SWIFT information (including message formats) available at www.iso15022.org. 
For more information about real-time trade matching for CMU, access content in the CMU Division section of 
the [[DTCC]] Learning Center at: 
 https://www.dtcclearning.com/products-and-services/equities-clearing/cmu-division.html  
For real-time reporting of municipal [[securities]] transactions, see: 
http://www.msrb.org/Market-Transparency/Submission-Tutorials.aspx  
Contact Us 
Use the following [[NSCC]] contacts for information about CMU RTTM. You can also contact your [[DTCC]] 
Relationship Manager or obtain general assistance by visiting the [[DTCC]] Client Center . 
For… Contact… 
General questions and product 
support 
[[NSCC]] Support by email at NSCCSupport@[[DTCC]].com 
Setup and testing [[NSCC]] Integration by email at NSCCIntegration@[[DTCC]].com 
Issues with logging on to the 
system 
[[DTCC]] Client Support. Call the following number, and then follow the prompt for 
product support. 
• For US and Canada, call 1 888–382–2721. 
• For the UK, Europe, and Asia, call +1 212–855–8099. 
 

---

## Page 9

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
[[NSCC]] Interactive Messaging for CMU Real-Time Trade Matching (CMU RTTM) 9 
2. [[NSCC]] INTERACTIVE MESSAGING FOR CMU REAL-
TIME TRADE MATCHING (CMU RTTM) 
CMU RTTM Service Features 
[[NSCC]] members and submitters can take advantage of the following CMU real-time trade matching (RTTM) 
and regulatory reporting features: 
• Submitting trade input to CMU RTTM intraday, as trades are executed, using the SWIFT MT515 message 
format. The MT515 inbound message specification supports all information required for CMU RTTM to 
facilitate [[settlement]], as well as that information required for the regulatory reporting municipal trades to 
the MSRB. 
• Immediately receive CMU RTTM trade status information (for example, notify whether the trade has been 
accepted or rejected) through the SWIFT MT509 message format. This format is also used to provide up-
to-the-minute trade status information to members as CMU RTTM processes transactions. For example, a 
message is sent when a trade match is canceled or modified. 
• Immediately notified immediately through a SWIFT MT518 message when a trade has been submitted 
against trade countraparties. The SWIFT MT518 message contains full trade details, like the MT515. It is 
also used to communicate to the client those changes that CMU RTTM may have made to trade records 
that were previously submitted. 
• Receive real-time regulatory reporting data, which is immediately forwarded to the MSRB for price 
transparency and surveillance purposes. 
• Submit regulator only (reporting-only) messages. 
• Kept informed of CMU RTTM system availability and major system events through MT599 
Administrative Messages. 
[[NSCC]]’s matching process runs in real-time, enabling members to match trades as close as possible to their 
execution. With interactive messaging, members submit trade data to CMU RTTM, review output, and 
identify and correct any errors, all within minutes of execution. 
CMU RTTM Role in Regulatory Reporting to the MSRB 
CMU RTTM serves as a single conduit for clients to submit their fixed income trades for both trade 
matching and regulatory reporting. Clients submit a single trade message to CMU RTTM for both matching 
and real-time reporting of their street-side municipal bond trades to comply with applicable price 
transparency requirements. The MSRB requires firms to report and match municipal bond trades within 15 
minutes of execution, and that a single submission for both clearance and price reporting of street-side 
trades are required. 
While regulatory reporting only transactions are not stored in the CMU RTTM matching application, interactive 
messages for regulatory reporting only trade activity received from clients are forwarded to the MSRB as 
specified by the client. 
The MT515 layout supports input requirements for CMU RTTM as well as for MSRB customer and inter- 
dealer transactions; specific fields have been allocated for regulatory reporting. While CMU RTTM validates all 
matching-related fields, it does not validate that regulatory fields are populated or that they are populated with 
the valid data. CMU RTTM checks regulatory fields for correct format, when SWIFT messages can be 
created for the MSRB based on client supplied information, where applicable. MSRB is responsible for 

---

## Page 10

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
[[NSCC]] Interactive Messaging for CMU Real-Time Trade Matching (CMU RTTM) 10 
ensuring required information is submitted accurately by its members. For a list of regulatory fields applicable 
to MSRB, see Appendix G. 
CMU RTTM sends to MSRB all significant events through interactive messages. These messages are time 
stamped with the date and time of receipt from clients. The messages contain reasons to identify the event 
that triggered them. Where CMU RTTM rejects a record for CMU RTTM specific edits, a reject message is 
sent to MSRB. For regulatory requirements and information on MSRB messaging, see MSRB Specifications 
for Real - Time Reporting of Municipal [[securities]] Transactions. 
The trade flow reflects the regulator messages generated by CMU RTTM and the events that trigger output 
sent by CMU RTTM to the MSRB. In addition, the message flows presented in Appendix B reflect CMU 
RTTM output to the MSRB, as instructed by clients. All inbound customer trades and system events are 
forwarded based on client instructions and market of execution. 
Submission Rules to Facilitate Regulatory Reporting 
The MT515 interactive message layout enables clients to submit one record that facilitates matching and 
[[settlement]] as well as regulatory reporting. Clients are able, through MT515, to indicate whether to send the 
record to CMU RTTM and/or the MSRB for municipal bond trades. 
The header of the MT515 enables a client to designate in the Receiver field whether the record goes to 
CMU RTTM and MSRB (NSCCTRRS), where applicable, or whether the record goes only to the MSRB 
(NSCCREGO). 
In addition, the Transaction Processing Narrative field (:70E::TPRO//) in the Confirmation Details block 
(CONFDET) contains a repeating field that is required to inform the CMU RTTM router where to direct a 
record. Clients must indicate in the SWIFT message header whether the trade goes to one of the options 
listed in the following table: 
CMU RTTM/Regulator Destination (:70E::TPRO//) Header-Receiver 
CMU RTTM only /DEST01 NSCCTRRS 
MSRB only /DEST02 NSCCREGO 
CMU RTTM and MSRB /DEST01/DEST02 NSCCTRRS 
 
Note:   
If the recipient in the message header does not agree with the destinations reflected in the:70E::TPRO// field; the message 
is rejected for inconsistent recipient information. Where an unknown value is found in the Receiver field, the message is 
rejected for unknown target application. 
  

---

## Page 11

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
[[NSCC]] Interactive Messaging for CMU Real-Time Trade Matching (CMU RTTM) 11 
MSRB Reporting 
The requirements for the MSRB Reporting are described in the following sections: 
• Input Street Trades 
• Output Street Trades 
• Customer and Interdealer Regulatory-Only Trades 
Input Street Trades 
On interactive messages, clients are required to indicate if an MT515 record should be sent to CMU RTTM, 
MSRB, or both. 
A destination of MSRB (/DEST02) in the Transaction Processing Narrative field (:70E::TPRO//) is required for a 
trade to be sent to the MSRB for reporting purposes. CMU RTTM also forwards r elated system generated 
events to MSRB (based on this indicator and trade market of execution). Populate the header and destinations 
on MT515 messages as follows: 
• Mark trades intended for CMU RTTM only with NSCCTRRS in the header and with /DEST01 (CMU 
RTTM) in the :70E::TPRO// field. 
• Mark trades intended for both CMU RTTM and MSRB with NSCCTRRS in the header and with  
• /DEST01/DEST02 (CMU RTTM and MSRB) in the :70E::TPRO// field. 
• Mark trades intended for MSRB only with NSCCREGO in the MT515 header and with /D EST02 (MSRB) in 
the :70E::TPRO// field. 
Note:  
Continue to submit modifications for Street Trades for regulatory-only purposes to NSCCTRRS (CMU RTTM) until 
the trade is no longer on the CMU RTTM system, after which time direct the trade modification to NSCCREGO. Trades 
remain on CMU RTTM as follows: 
• All matched trades, other than comparison-only, are available for regulatory modifies through end-of-day 
delivery date (anticipated actual [[settlement]] date). 
• Comparison-only matched trades are available through end-of-day contractual [[settlement]] date. 
• All unmatched trades remain on CMU RTTM through the end-of-day submission day + 2. 
  

---

## Page 12

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
[[NSCC]] Interactive Messaging for CMU Real-Time Trade Matching (CMU RTTM) 12 
Output Street Trades 
MT509 Accept/Reject (ACK/NAK) messages are sent from CMU RTTM for all records sent to CMU RT TM 
(NSCCTRRS) for matching. Where an ACK is sent by CMU RTTM, the MSRB can then send out additional 
information to clients if the street-side trade meets MSRB requirements, MSRB does not send an ACK. 
Where a NAK is sent (other than when a trade is not SWIFT compliant), CMU RTTM forwards the reject to the 
MSRB. To understand MSRB output and implementation plans and 15-minute reporting, see the MSRB 
documentation. 
Reporting-only trade records sent to MSRB receive no CMU RTTM- generated ACK/NAK messages. No output 
is generated from CMU RTTM for regulatory-only submissions, although CMU RTTM acts as a pass- through 
vehicle for all MSRB interactive output (unless the record is non-SWIFT compliant, in which case, NSCCTRRS 
is the sender of the NAK information). MSRB will respond with an ACK or NAK to Regulatory Only 
submissions. (Typically used for Customer trades or IDRO trades). 
Customer and Interdealer Regulatory-Only Trades 
Input 
[[NSCC]] clients are required to indicate on the MT515 messages that customer trades are to be sent to the 
MSRB by placing NSCCREGO in the header, and by indicating /DEST02 in the :70E::TPRO// field. 
Output 
Where an MT515 record is deemed to be non-SWIFT compliant, CMU RTTM creates a NAK for the client, 
where possible. (This reject for non-SWIFT compliance is not passed to the MSRB by CMU RTTM.) All 
other MT509 ACK/NAK output for regulatory-only records is generated by the MSRB, rather than by CMU 
RTTM CMU. 

---

## Page 13

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 13 
3. INTERACTIVE MESSAGE GUIDELINES 
This section provides some background information that may be useful for interpreting the detailed message 
specifications that follow. 
[[FICC]] has adapted the ISO 15022 message formats for interactive matching input and output. These ISO 
formats were developed in coordination with international [[securities]] industry working groups (for example, 
the ISO Technical Committee, TC68) to establish a viable and efficient industry standard. This standard 
defines messages composed of required and optional variable-length sequences of tags and data fields, 
maximizing the flexibility and practical application of the messages. 
The important aspect of this format is the ability to include only the data necessary for a specific business 
transaction. Each trade message can require different fields. Coding for these formats allows new features to 
be added without requiring extensive retesting. 
The flexible format of the ISO 15022, continuing evolution message standards, and the ongoing 
deployment of new [[FICC]] services, makes it likely that new fields will be added to the standard. For 
information about the generic SWIFT standards for the messages used in this interface, see 
https://www2.swift.com/uhbonline/books/a2z/standards_mt.htm  
While [[FICC]] has elected to use SWIFT standardized messages, it does not utilize the SWIFT network. We 
utilize our proprietary network for communication between [[FICC]] and its clients. The messages are intended, 
however, to be compliant with SWIFT regulations. 
ISO 15022 Message Structure 
ISO 15022 SWIFT message formats are constructed using a modular methodology based on the premise 
that information can be identified and programmed once, and then reused wherever needed. Using this 
approach, data is configured into logical groups (for example, generic fields and blocks) according to business 
purpose. These groups are then uniquely identified (using tags, qualifiers, and start/end of block designators) 
to fulfill particular business purposes across a number of messages without requiring extensive 
reprogramming. 
If the [[BASIC]] message structure were diagramed from the top down (going from the more general to the more 
specific), you would have a Message Header followed by one or more information blocks (potentially containing 
sub-blocks), composed of one or more fields. The following sections define each of these components.  
  

---

## Page 14

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 14 
Message Header 
The message header specifies the sending and receiving parties of the message and provides the message 
type. [[FICC]] has added a password to this header to provide an extra level of security for [[NSCC]] clients. The 
message header is the first component of every message. [[FICC]] requires that the fields in the header have a 
fixed format. The header is populated as a continuous string of data and terminates as a regular data field 
(with a carriage return line feed CRLF). 
Blocks and Sub-blocks 
A block is a group of fields containing related business information that is framed by start -of-block and end-of-
block designators. The use of a block is not restricted to any given message; it can be reused across a number 
of messages and combined with other blocks to fulfill various business requirements. For example, t he General 
Information block (found in the MT515, MT509 and MT518) contains general information regarding the trade, 
such as trade reference numbers. The Confirmation Details block (found in the MT515 and MT518) contains 
specific trade information such as trade date, [[settlement]] date, price, security, and information regarding the 
confirming parties. 
Each message contains one or more blocks. A typical message contains a General Information block followed 
by a series of detail blocks. These blocks are mandatory or optional within a particular message. They are 
structured as follows: 
• Start-of-block designator (represented by the tag 16R) that indicates the start of a group of related 
information. 
• One or more sub-blocks, fields, or a combination of sub-blocks and fields. 
• End-of-block designator (represented by the tag 16S) that indicates the end of a group of related 
information. 
The structure of a sub-block is the same as that of a block, the only difference being that it is nested or 
contained within another block. For example, the Confirming Parties blocks are sub-blocks of the 
Confirmation Details block. Under certain circumstances, you can repeat sub-blocks in a block. For example, 
you can repeat the Confirming Party sub-blocks (once for [[Buyer]] and once for [[Seller]]). 
  

---

## Page 15

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 15 
Fields 
There are two types of fields: generic fields and discrete fields. As the names imply, generic fields are multi -
purpose fields used across messages and message types, whereas discrete fields in messages are limited to a 
single purpose. Generic fields further support the flexibility and modular message structure of the message 
formats. Each generic field is a [[BASIC]] type of business data that is common across all messages, such as date 
or amount. 
At a minimum, each field is composed of an identifying tag and its associated field data. A tag is a two- digit 
number that represents the type of data contained in the field followed by an alpha character that provides 
format information for the field contents. For example, 98A is the generic tag used to indicate a date field in a 
particular format (YYYYMMDD). The format for a tag includes two delimiters – one to indicate the start of the 
tag, and a second to indicate the end of the tag. These delimiters are colon characters “:”. Continuing with the 
example, the proper format for the generic tag used to indicate a date in the YYYYMMDD format is “:98A:”  
Notes:  
For each field, there can be several format options for expressing the data. The alpha character in the tag is used 
to indicate which format [[Option]] has been applied. If the alpha character in the tag is lowercase in the SWIFT 
documentation, this means that there are several format options for the field and that there is free choice to use any 
of these options. If the alpha character in the tag is uppercase, this means that, while there are several format 
options for the field, the [[Option]] designated by the uppercase alpha character must be used. For example, 98A refers 
to a date in the YYYYMMDD format. 98C refers to a date that also includes the time.  
[[FICC]] has mandated the options that clients must use in the layouts. 
Usually, there are a number of different types of dates that are associated with any given trade; 
therefore, the generic field tag must be further described to make it more useful. Qualifiers are used to 
provide this additional level of description. For example, the tag 98A followed by the qualifier SETT 
means that the corresponding field data is the [[settlement]] date for the trade. The tag 98A followed by the 
qualifier TRAD corresponding field data is the trade date for the trade. Qualifiers for generic tags are always 
preceded by an additional colon (:). 
Thus, the generic field for a [[settlement]] date of March 31, 2003 in the YYYYMMDD format, including the 
generic tag, qualifier, and field data is: :98A::SETT//20030331 
Although tags, qualifiers, options [[DO]] not need to be placed in any particular sequence, unless there is a 
sequence dependency as part of the format. A best practice is to place tags in the same sequence as 
they appear in this specification. Tags that are part of a block must remain between the start and end block 
tags. 
  

---

## Page 16

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 16 
Tag and Field Format Illustrations and Chart 
This figure shows the format for a generic field tag (such as :98A:) and its associated field data. The charts in 
this section provide the definitions of the elements delineated in the following figure: 
 
Field Tag 
Components 
Format Definition 
Delimiter 1 : Shows the start of the field tag. 
Type of Field 2!n Two-digit number representing the data type. Note: An exclamation 
mark (!) indicates a fixed field size. 
Field Format 1!a Format of the contents of the data field. 
Delimiter 2 : Shows the end of the field tag. 
Example - Field Tag :98A: Denotes the Generic Date field with 98. 
Denotes the date 8!n (YYYYMMDD) format with A. 
Generic Field Marker : Identifies the field as generic. 
Qualifier 4!c Provides the business significance of the data. Mandatory. 
Delimiter 1 / Mandatory delimiter. 
Optional [[issuer]] Code [8c] Allows market or [[issuer]] codes when SWIFT defined codes are not 
used. Codes, such as GSCC, have a maximum of 8 characters. 
Delimiter 2 / Mandatory delimiter. 
Data Field 98A Provides the data for the field. The format is specified by the letter 
[[Option]] of the field format. For example, 98A specifies a date format of 
8!n = YYYYMMDD. 
Example - 
Tag/Qualifier/Data 
Field 
:98A::SETT//20030331 Indicates that this is a generic field by preceding the colon with the 
SETT qualifier. The :SETT// qualifier combined with the 98A tag 
denotes that this field is a [[settlement]] date in  the YYYYMMDD format. 
  


---

## Page 17

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 17 
Illustrating the Message Structure 
This figure shows the [[BASIC]] SWIFT Message structure for ISO 15022 messages. For generic structural 
illustrations of the MT515, MT509, and MT518 messages (as specified by SWIFT), see Appendix D: 
Message Structure Diagrams.  
 
  


---

## Page 18

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 18 
CMU RTTM Trade Flow 
Here is a typical message flow for a trade submitted for bilateral matching. This flow does not include the 
messages that are intended to go to the MSRB. View the complete flow that shows the CMU 
RTTM-generated regulator messages. 
This figure shows much of the logic used by CMU RTTM in processing interactive messages. For each 
MT515 submitted by a client conveying information to CMU RTTM, an MT509 message is generated 
indicating that the information has been accepted or rejected. In the example, when Client A and Client B 
submit MT515 Instruct Messages, each receives an MT509 Trade Accepted Message. This [[BASIC]] logic, of 
each input being acknowledged as either accepted or rejected, carries throughout all CMU RTTM-related 
messaging. For example, submitting an MT515 Cancel results in an MT509 Cancel Accepted or Rejected 
message being generated, and submitting an MT515 Modify results in an MT509 Modify Accepted or 
Rejected message being generated. 
Another rule of CMU RTTM interactive messaging is that each time a client submits a record (MT515) that is 
accepted by CMU RTTM, its contraparty receives a notification (MT518) of matching information. In the 
example, submitting the MT515 Instruct message by Client A resulted in generating an MT518 Match 
Request message for Client B. 
Any request messages generated by CMU RTTM (for example, MT518 Match Requests) are then canceled by 
CMU RTTM if the request is no longer valid. In the example, after the trade is matched, Client A and Client 
B receive an MT518 Match Request Cancel, effectively nullifying the previously generated MT518 Match 
Requests, as the trade is now matched, and no further input is required. 
Finally, CMU RTTM indicates when transactions are sent to [[settlement]], informing clients of anticipated 
[[settlement]] information. For a set of detailed message flows for various scenarios, see Appendix B. 
  

---

## Page 19

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 19 
 
 
Bilateral Trade Matched 
  


---

## Page 20

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 20 
The following table shows the message flow for Figure 4. Bilateral Trade Matched. 
Message 
Number 
Message Type Description 
1 MT515 INST Input message that conveys the trade data submitted by Client A for matching 
within CMU RTTM. 
1a MT509 PACK Output message sent to Client A acknowledging that its trade has been accepted 
by CMU RTTM and is waiting for further processing. This message also provides 
the Transaction [[ID]] (TID) assigned by CMU RTTM. 
1b MT518 CMPR After Client A’s input is accepted by CMU RTTM, this output message containing 
full trade details as entered by Client A is sent to the contraparty, Client B. 
This message informs Client B that a trade has been submitted against it for 
which Client B must submit a corresponding MT515 Instruct to effect a match. 
2 MT515 INST Input message that conveys the trade data submitted by Client B for matching 
within CMU RTTM. 
2a MT509 PACK Output message sent to Client B acknowledging that its trade has been accepted 
by CMU RTTM and is waiting for further processing. This message also provides 
the Transaction [[ID]] (TID) assigned by CMU RTTM. 
2b MT518 CMPR After Client B’s input is accepted by CMU RTTM, this output message containing 
full trade details as entered by Client B is sent to the contraparty, Client A. 
This message informs Client A that a trade has been submitted against it for 
which Client A must submit a corresponding MT515 Instruct to effect a match. 
3a MT509 MACH Output message sent to Client A informing it that the data submitted on its 
MT515 Instruct message has been matched to the data submitted on Client 
B’s MT515 Instruct message, and the trade is matched. This message also 
contains the match control number (shared with Client B) assigned upon 
matching. 
3b MT509 MACH Output message sent to Client B informing it that the data submitted on its 
MT515 Instruct message has been matched to the data submitted on Client 
A’s MT515 Instruct message, and the trade is matched. This message also 
contains the match control number (shared with Client A) assigned upon 
matching. 
3c MT518 CADV Output message sent to Client A to cancel the MT518 Match Request message 
previously sent (2b), since the trade is now matched. 
3d MT518 CADV Output message sent to Client B to cancel the MT518 Match Request message 
previously sent (1b), since the trade is now matched. 
4a MT518 STLD Message generated for Client A when CMU RTTM sends the trade to 
[[settlement]]. This message indicates the anticipated [[settlement]] method and 
delivery date of the trade. 
4b MT518 STLD Message generated for Client B when CMU RTTM sends the trade to 
[[settlement]]. This message indicates the anticipated [[settlement]] method and 
delivery date of the trade. 
 
  

---

## Page 21

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 21 
CMU RTTM Trade Flow Showing MSRB Messages 
CMU RTTM generates messages to the regulator based on messages received from the clients (Instructs, 
Modifies, Cancels, and DKs). It also generates messages to the MSRB for system-generated events. For 
example, upon matching, CMU RTTM sends matched messages (for both Client A and Client B) to the MSRB.  
 
CMU RTTM Trade Flow Showing MSRB Messages 
For more information about regulatory flows, see MSRB Specifications for Real-Time Reporting of Municipal 
[[securities]] Transactions. 
  


---

## Page 22

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 22 
Message Flow Explanation 
Message 
Number 
Message Type Description 
1 MT515 INST Input message that conveys the trade data submitted by Client A for matching 
within CMU RTTM. 
1a MT509 PACK Output message sent to Client A acknowledging that its trade has been accepted 
by CMU RTTM and is waiting for further processing. This message also provides 
the Transaction [[ID]] (TID) assigned by CMU RTTM. 
1b MT518 CMPR After Client A’s input is accepted by CMU RTTM, this output message containing 
full trade details as entered by Client A is sent to the contraparty, Client B. 
This message informs Client B that a trade has been submitted against it for 
which Client B must submit a corresponding  MT515 Instruct to effect a match. 
1c MT515 INST 
to MSRB 
CMU RTTM generates a copy of Client A’s trade, timestamps it, and sends it to 
the Regulator. 
2 MT515 INST Input message that conveys the trade data submitted by Client B for matching within 
CMU RTTM. 
2a MT509 PACK Output message sent to Client B acknowledging that its trade has been accepted 
by CMU RTTM and is waiting for further processing. This message also provides 
the Transaction [[ID]] (TID) assigned by CMU RTTM. 
2b MT518 CMPR After Client B’s input is accepted by CMU RTTM, this output message containing 
full trade details as entered by Client B is sent to the contraparty, Client A. This 
message informs Client A that a trade has been submitted against it for which 
Client A must submit a corresponding MT515 Instruct to effect a match. 
2c MT515 INST 
to MSRB 
CMU RTTM generates a copy of Client B’s trade, timestamps it, and sends it to 
the Regulator. 
3a MT509 MACH Output message sent to Client A informing it that the data submitted on its MT515 
Instruct message has been matched to the data submitted on Client B’s MT515 
Instruct message, and the trade is matched. This message also contains the 
match control number (shared with Client B) assigned upon matching. 
3b MT509 MACH Output message sent to Client B informing it that the data submitted on its MT515 
Instruct message has been matched to the data submitted on Client A’s MT515 
Instruct message, and the trade is matched. This message also contains the 
match control number (shared with Client A) assigned upon matching. 
3c MT515 MDFC 
sent to MSRB 
CMU RTTM generates a copy of Client A’s matched trade, timestamps it, and 
sends it to the MSRB. The message has all trade details, including the match 
control number. 
3d MT515 MDFC 
sent to MSRB 
CMU RTTM generates a copy of Client B’s matched trade, timestamps it, and 
sends it to the MSRB. The message has all trade details, including match 
control 
3e MT518 CADV Output message sent to Client A to cancel the MT518 Match Request message 
previously sent (2b), since the trade is now matched. 
3f MT518 CADV Output message sent to Client B to cancel the MT518 Match Request message 
previously sent (1b), since the trade is now matched. 
4a MT518 STLD Message generated for Client A when CMU RTTM sends the trade to [[settlement]]. 
This message indicates the anticipated [[settlement]] method and delivery date of 
the trade. 
4b MT518 STLD Message generated for Client B when CMU RTTM sends the trade to [[settlement]]. 
This message indicates the anticipated [[settlement]] method and delivery date of 
the trade. 
 
  

---

## Page 23

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Interactive Message Guidelines 23 
Data Format Differences 
SWIFT messages employ certain standards for some data fields that are different from those currently 
supported by [[NSCC]]. In these cases, CMU RTTM supports a smaller size field than SWIFT records allow. 
These differences are summarized in the following chart. 
Note:  
Where the CMU RTTM field is smaller than the SWIFT field, CMU RTTM supports the smaller value. Populate these fields 
with a value no larger than the CMU RTTM maximum. 
Field Swift 
Maximum 
CMU 
RTTM 
Maximum 
[[NSCC]] Format Restrictions 
Dollar Price 
(DEAL//PRCT) 
15d 13d 4 whole numbers and 8 decimal places using a comma 
as the decimal separator. 
Yield (DEAL//YIEL) 15d 8d 3 whole numbers and 4 decimal places using a comma 
as the decimal separator. 
[[settlement]] Amount11 15d 13d 10 whole dollars 2 decimal places using a comma as the 
decimal separator. 
Accrued Interest 
Amount 
16d 9d 7 whole dollars 2 decimal places using a comma as 
the decimal separator. 
Quantity 15d 10d 9 whole numbers with a trailing comma as the decimal 
separator. 
 
 
1 All amount fields preceded by USD have two decimal places. 

---

## Page 24

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Communication Overview 24 
4. COMMUNICATION OVERVIEW 
To ensure safe, reliable submission of trade messages and delivery of status messages, [[FICC]] has 
implemented a message exchange facility and a private communications network as part of its real-time 
processing architecture. 
Message Exchange 
CMU RTTM has a message exchange facility in place to support receipt of trade messages from and 
delivery of status and advisory messages to Client systems. A message exchange facility provides support 
for implementing queues, which are typically time-ordered lists of messages (such as trade messages, 
cancellation messages, and status messages). This allows Client systems to generate trade messages as 
trades are executed, and these trade messages are queued onto the “To CMUCMU RTTM” queue. If the 
communications connection is enabled (including all the links, from the dial-up or leased line up to the 
messaging product itself), the message is immediately sent to CMU RTTM. Otherwise, messages 
accumulate on the queue until a connection is established. 
The same procedure holds true on the return side – meaning as CMU RTTM processes trades, from trade 
acceptance through matching – status updates are queued for delivery back to Client systems. Clients’ 
systems must have a connection enabled and a program (for example, a process or thread) that is waiting for 
messages to appear on the “From CMU RTTM” queue to process CMU RTTM responses interactively. CMU 
RTTM utilizes the MQ Series product from IBM to support CMU RTTM Interactive Message 
Specifications. This product facilitates a reliable message exchange protocol that deals with sequence 
numbers, connection recovery, and other messaging-related issues. The use of this product precludes the 
traditional requirement of developing a custom message exchange protocol for each new clearing corporation 
interface. MQ Series is available for the majority, if not all, of the systems platf orms in use at Clients' data 
centers (including MVS, VMS, most common versions of UNIX, and Windows). Many [[DTCC]] members already 
use this product in-house, to connect with the clearing banks, to connect with [[FICC]]'s existing CMU RTTM 
products supporting Government [[securities]] and Mortgage Backed [[securities]], or for other [[DTCC]] services.  
CMU RTTM's messaging implementation provides a To CMUCMU RTTM queue and a From CMU RTTM 
queue for each Client. Additional details, including the full naming convention utilized, are distributed to 
Clients separately. 
  

---

## Page 25

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 25 
5. MESSAGE SPECIFICATIONS 
This section contains the detailed specification for the MT515, MT509, MT518, and MT599 messages to be 
used to support Real-Time Matching, and is organized into the following subsections: 
Section Description 
Message Format 
Guidelines 
Provides formatting rules and conventions for [[NSCC]] interactive messaging using SWIFT ISO 
messages. 
MT515 Message Lists the types of MT515 messages and their uses. 
• MT515 Message Specification 
Provides information that identifies the use of each MT515 message type. 
• MT515 General Format 
Provides a table that lists all the tags, options, and qualifiers that can appear on the 
MT515 messages 
• MT515 Field Specifications 
A table that lists the detailed specifications for each block, [[Option]], qualifier, and 
subqualifier. 
• MT515 Field Analysis 
Provides a table with detailed analysis of those tags, options and qualifiers that can 
appear on each of the MT515 message types.
 
MT509 Message Lists the types of MT509 messages and their uses. 
• MT509 Message Specification 
Provides information that identifies the use of each MT509 message type. 
• MT509 General Format 
Provides a table that lists all the tags, options, and qualifiers that can appear on the 
MT5009 messages 
• 509 Field Specifications 
A table that lists the detailed specifications for each block, [[Option]], qualifier, and 
subqualifier. 
• MT509 Field Analysis 
Provides a table with detailed analysis of those tags, options and qualifiers that can 
appear on each of the MT509 message types. 
MT518 Message Lists the types of MT518 messages and their uses. 
• MT518 Message Specification 
Provides information that identifies the use of each MT518 message type. 
• MT518 General Format 
Provides a table that lists all the tags, options, and qualifiers that can appear on the 
MT518 messages. 
• MT518 Field Specifications 
A table that lists the detailed specifications for each block, [[Option]], qualifier and 
subqualifier. 
• MT518 Field Analysis 
Provides a table with detailed analysis of those tags, options and qualifiers that can 
appear on each of the MT518 message types. 
MT599 Message Lists the types of MT599 messages and their uses. 
• MT599 Message Specification 
Provides information that identifies the use of each MT599 message type. 
• MT599 General Format 
Provides a table that lists all the tags, options, and qualifiers that can appear on the 
MT599 messages. 
• MT599 Field Specifications 

---

## Page 26

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 26 
Section Description 
A table that lists the detailed specifications for each block, [[Option]], qualifier and 
subqualifier. 
Message Format Guidelines 
The following table shows the Message Rules that apply to all messages in the CMU RTTM Interactive 
Message Specification: 
Message Rule Description 
Direction Messages are sent either to or from CMU RTTM. 
Variable Length All messages can vary in length up to a maximum allowable number of characters 
per message type. 
Header All messages begin with a standard fixed length header. 
Terminator All messages end with a standard terminator sequence reflected by a carriage 
return/line feed and a dash (CRLF –). 
Message Type Each message belongs to a specified message type. 
Message Fields A message is composed of one or more message fields. 
Character Set A-Z, a-z, 0–9, white space, and the following punctuation: :/,-  
 
The following table shows the Message Field Rules that apply to all messages in the CMU RTTM Interactive 
Message Specification: 
Message Field Rule Description 
Field Tag Each field begins with a field tag. 
Tag Format Each tag is composed of 2 digits and an optional character (2!c[1a]). 
Tag Delimiter Each tag is prefixed and suffixed by a colon (:). For example, :23G:. 
Field Data Field data (including qualifiers and subqualifiers) immediately follows the tag suffix 
delimiter. Generic tags are prefixed by an extra colon (:). 
Data Format Data conforms to format rules for a specified tag. 
Data Elements Field data may be divided into multiple elements or subfields. 
Qualifiers Qualifiers within a data field provide additional format definition. If a qualifier is 
used, it must appear immediately after the tag suffix delimiter (such as 
:98A::SETT). If further data is required after the qualifier and the data complies with 
SWIFT standards, the qualifier is delimited by the // characters and the data follows. 
For example, :98A::SETT//20030331 or :20C::MAST//19960815. If the data is CMU 
RTTM specific, the GSCC [[issuer]] code is included. For example, 
:95R::BUYR/GSCC/PART8520. 
Field Delimiter Field delimiter sequence is carriage return line feed, CRLF (ASCII Character 13, 
ASCII Character 10). This sequence immediately follows the data. The combination 
of the carriage return, line feed, colon (CRLF:) indicates the end of one field and the 
beginning of the next 
 
  

---

## Page 27

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 27 
Format Conventions 
Note:  
Layouts for each of the messages included in this section are organized using the following columns of data: 
Column Heading Description 
M/O/O* Defines whether the field is always mandatory or is optional in the particular message and 
sequence according to SWIFT requirements. 
A value of O* indicates that although the value is optional for SWIFT, it is required for CMU RTTM. 
For a list of CMU RTTM required fields, see Appendix A. 
Tag Defines the exact tag value that must precede the field. Tags are always delimited by a colon (:). 
The colon is the character immediately before and after the tag. For example, :98A: indicates a 
date with a format of YYYYMMDD follows. 
Block or Qualifier Specifies the block name in the case of a start block (16R) or end block (16S) tag. Otherwise, it 
specifies the required qualifier for the tag. For example, :98A::SETT indicates  a  [[settlement]] Date 
field. 
Subqualifier/Options Specifies the different options available for individual qualifiers for a tag. Each tag, qualifier, and 
[[Option]] combination uniquely specify a data element. For example, the 90A::DEAL//YIEL/ tag 
indicates that a trade price follows with a yield price type. 
Data Format Specifies the size and characters allowed within a data field, as specified by SWIFT. The field 
specifications that follow each layout indicate how to populate each field for CMU RTTM 
input/output. The format provided in this column reflects the data that the Client must populate the 
field with. 
For example, :98A::SETT// has a format of YYYYMMDD. 
Field Description Provides a text description of the purpose or use of a data field. 
 
Note:  
The Mandatory/Optional (M/O) field on the layout indicates if the field is SWIFT mandatory or optional for the 
message/sequence. A value of O* indicates that although the value is optional for SWIFT, it is required for CMU 
RTTM, For information about [[NSCC]] required fields for the various products, see Appendix A and for regulatory fields, see 
Appendix G. Those fields that are SWIFT mandatory, [[NSCC]] mandatory, or both SWIFT and [[NSCC]] mandatory must be 
reflected on the MT515. Otherwise, the message (instruct, modify, cancel, or DK) is rejected. 
The Data Format field on the layouts is intended to reflect the format of the data that Clients/ CMU RTTM 
must use to populate the field. For example, the format for the [[settlement]] Date field 
(:98A::SETT//20030331) is reflected as YYYYMMDD. 
Note:  
There are differences in data field sizes and field formats for populating the SWIFT record. For example, date fields 
on the MT515, MT509, and MT518 SWIFT records are reflected as YYYYMMDD, not MMDDYYYY, which is the format 
used on some of the [[NSCC]] proprietary layouts. 
In addition, all fields on the SWIFT messages are left justified. If the field has a decimal format (d), use a 
decimal comma, not a decimal point. 
As a supplement to the layout, here is a detailed description of each field format. Thi s reflects the options, 
defines the usage, and provides an example of each field. 

---

## Page 28

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 28 
The following characters can appear in the Data Format column or in any discussion of data format and 
content: 
Character Meaning Example Format Example Usage 
a Upper Case Alpha Characters 6a ABCDEF 
c Alphanumeric Characters (upper case 
only) 
6c AB12EF 
d Decimal Number (decimal comma) 15d 2035,45 
e Space 1e (1blank space) 
n Numeric Characters 8n 20011228 
x Any Printable ASCII Symbol 20x Anytime & Anyplace 
/ The literal / as a separator 6c/2a AB12EF/NY 
[ ] Optional element format [/4c] [optional data - /4 characters] 
[N] Optional sign (negative) format [N] :19A::SPCN//USDN500,45 
! Fixed length field 12!c ABCDEFGHIJKL 
 
By definition, all fields are variable in length with a maximum field size specified, unless a fixed length format is 
defined by including the exclamation mark (!). In this case, the size specified is the fixed field size. If the data 
value in the fixed length field is smaller than the field size specified, the data is left justified with trailing blanks. 
Typical Message Form 
The following table shows the typical message form: 
Form Example 
<PASSWORD><SENDER><MESSAGE TYPE> 
<RECEIVER><cr><lf> 
:<BLOCK START TAG>:<BLOCK NAME><cr><lf> 
:<GENERIC TAG 1>::QUALIFIER//DATA FIELD 1 <cr><lf> 
:<TAG2>:DATA FIELD2<cr><lf> 
:<GENERIC TAG 3>::QUALIF/[[issuer]] CODE/DATA 
FIELD3<cr><lf> 
:<BLOCK START TAG>:<BLOCK NAME><cr><lf> 
:<GENERIC TAG 4>::QUALIFIER//DATA FIELD 3<cr><lf> 
:<BLOCK END TAG>:<BLOCK NAME><cr><lf> 
:<BLOCK END TAG>:<BLOCK NAME><cr><lf> 
ABCDEFGH 9500 515/000/GSCC NSCCTRRS 
:16R:GENL 
:20C::SEME//004354NY4355 
:23G:NEWM 
:22F::TRTR/GSCC/CASH 
:16R:LINK 
:20C::MAST//ABCD1234 
:16S:LINK 
:16S:GENL 
 
Blocks are demarcated by the start (:16R:) and end (:16S:) block tags, with an associated block name like 
GENL. The tags contained within the block provide the data associated with the block. You can repeat certain 
blocks, such as the confirming party block, as necessary (for example, to identify the [[Buyer]] or [[Seller]] of 
[[securities]]) as specified by SWIFT. 
Generic fields are designed to serve a particular function, with a qualifier code specifying a specific 
business purpose to that function. In the preceding example, the 20C tag is a generic reference identifier, 
and the SEME qualifier in the GENL block indicates that this is the Sender’s Message Reference for that 
message. In each LINK subsequence, 20C can be used to provide one of the MAST-Master Reference 
Number (Client External Reference), a LIST-CMU RTTM assigned reference or TID, a COMM-Match 
Control Number and the TRRF-the Regulator Control Number. 

---

## Page 29

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 29 
Message Header Format 
M/O Tag Block or Qualifier Options Data Format Field Description 
M    12!c Password 
M    8!c Sender 
M    3!n/3!n/4!c Message Type 
M    8!c Receiver 
 
The Message Type field contained in the message header identifies the type of message. This message header is 
utilized on all CMU RTTM messages: MT515, MT509, MT518, and MT599. The password field is left blank on all CMU 
RTTM outgoing messages (MT509, MT518, and MT599) but must be populated with the assigned password on all 
incoming messages. 
  

---

## Page 30

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 30 
MT515 Message 
The SWIFT MT515 is specified as a Client Confirmation of Purchase or Sale. It can also serve as a binding 
electronic contract. The MT515 message is used by [[NSCC]] members and authorized locked-in submitters to 
submit trades to CMU RTTM, enter trade cancellations, modify previously submitted trades, DK trades 
submitted against them, and submit reversals of previously submitted (and matched) trades. Field 22F 
PROC in the Confirmation Details (CONFDET) block enables the Client to indicate to CMU RTTM the type of 
record being sent. This field is populated for each record type. The following table shows the formats 
supported for the MT515 message types: 
 Message Type Usage 
1 Instruct Message 
(:22F::PROC/GSCC/INST) 
Used to submit trade details to CMU RTTM for trades executed by 
Clients or approved locked-in or demand submitters. This message 
supports: 
• All fields required to effect trade matching. 
• Certain other SWIFT mandatory fields. 
• Regulatory reporting fields. 
2 Cancel Message 
(:22F::PROC/GSCC/CANC) 
Used to initiate the cancellation of a previously submitted unmatched 
trade. A Cancel message is an exact copy of an Instruct message and 
contains full trade details. (It contains the last version of the trade on the 
CMU RTTM system.) If the trade has already been matched or sent to 
[[settlement]], it cannot be canceled. Instead, submit a reversal to CMU 
RTTM. 
After a trade has been canceled, you can submit a new trade to CMU 
RTTM using the same Client reference number as the original instruct 
message. 
If the trade has not been matched or the trade has been recorded and 
registered based on the input of a valid locked-in or demand submitter, 
only the original or locked- in/demand submitter can submit a cancel 
against this trade. 
3 Modify Message 
(:22F::PROC/GSCC/MDFC)  
Used to submit a modification to a previously submitted trade. 
Pre-matching – Modifications of matching fields can be made for bilateral 
trades (before a trade is matched) to all MT515 fields except 94B TRAD 
(Market of Execution) and 35B ([[CUSIP]]). To change the market of 
execution or the [[CUSIP]], the trade must be canceled and rebooked.  
[[syndicate]] trades can only be Modified pre-match on Submission date. 
Post-matching – The only fields that can be modified using this message 
are the Client Reference Number (X-ref) and regulatory fields. 
Submit all trade modifications (for street trades) to CMU RTTM until the 
trade is purged off CMU RTTM. After a trade is no longer available on 
CMU RTTM, submit all regulatory-only changes to the REGO system. 
4 DK Message 
(:22F::PROC/GSCC/TDDK) 
Used to submit a notification to CMU RTTM (and the contraparty) that a 
Client does not know, or agree with, the trade submitted against it by the 
contraparty. The DK message reflects the entire details of the Match 
Request received by the DKing party, along with a reason for the DK. 
Submit DKs only against unmatched trades. 
 
Note:  
All of these record types apply to reversals and trades. A Reversal (RVSL) indicator must be included in the Transaction 
Processing Narrative field (:70E::TPRO//) in the Confirmation Detail block (CONFDET) to identify that the record 
applies to a reversal. Clients using interactive input can submit data to CMU RTTM in real-time as trades/events occur, 
and CMU RTTM generates immediate notification regarding the trade’s status through the MT509. 

---

## Page 31

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 31 
MT515 Message Specification 
This section includes the detailed specification for the MT515 message. The message type is used by 
Clients to send instructions to CMU RTTM. The MT515 is used for the following record types: 
• Instruct 
• Cancel 
• Modify 
• DK 
These record types support trades and reversals of previously submitted trades. Throughout this section, 
data fields that support regulatory reporting requirements are marked with the regulatory field label. For 
more information about these fields, see MSRB Specifications for Real - Time Reporting of Municipal 
[[securities]] Transactions. 
MT515 General Format 
The following table provides the MT515 general format details: 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
    Message Header  
M    Password 12!c 
M    Sender 8!c 
M    Message Type 3!n/3!n/4!c 
M    Receiver 8!c 
M :16R: GENL  Mandatory Block Start  
M :20C: :SEME//  Sender’s Reference for 
this Msg 
16x 
M :23G: NEWM  Message Function = 
New or 
4!c 
  CANC  Cancel  
O* :98C: :PREP//  Preparation Date/Time YYYYMMDDHHMMSS 
M :22F: :TRTR/ GSCC/CASH Bilateral Trade Indicator 
or 
4!c 
   GSCC/TRLK Locked-in Trade 
Indicator or 
 
   GSCC/TRDC Demand Trade Indicator  
M :16R: LINK  Mandatory Repeat 
Block Start 
 
M :20C: :MAST//  Master Reference 
Number (External 
Reference) 
16x 

---

## Page 32

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 32 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
 :20C: :PREV//  Previous Reference 
Number 
(Previous External 
Reference) 
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :LIST//  CMU RTTM 
Assigned Reference 
(TID) 
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :TRRF//  Regulator Control 
Number 
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :COMM//  Match Control Number 16x 
M :16S: LINK  Repeat Block End  
M :16S: GENL  Block End  
M :16R: CONFDET  Mandatory Block Start  
M :98C: :TRAD//  Trade Date & Time YYYYMMDDHHMMSS 
M :98A: :SETT//  [[settlement]] Date or YYYYMMDD 
M :98B: :SETT// WISS [[settlement]] to be 
completed when the 
security is issued 
4!c 
M :90A: :DEAL/ /PRCT/ Deal Price – Percentage 
or 
15d 
   /YIEL/ Yield  
O* :94B: :TRAD/ GSCC/OTCP Place of Execution 
[[Over-The-Counter]] 
Corporate or 
4!c 
   GSCC/OTMU [[Over-The-Counter]] 
Municipal or 
 
   GSCC/OTUI [[Over-The-Counter]] Unit 
Investment Trust 
 
O :19A: :SETT/ /USD [[settlement]] Amount 15d 
M :22H: :BUSE/ /BUYI Trade Type – Buy or 4!c 
   /SELL Sell  

---

## Page 33

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 33 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
O :22F: :PRIC/ GSCC/WGTP Type of Price – 
Weighted Price 
4!c 
O* :22F: :PROC/ GSCC/INST MT515 Record Type 
– Instruct or 
4!c 
   GSCC/CANC Cancel or  
   GSCC/MDFC Modify or  
   GSCC/TDDK DK  
O :22F: :TTCO/ GSCC/TSQS Trade Type/Target 
Indicator – Qualified 
Special Representative 
(QSR) Trade or 
4!c 
   GSCC/TTQS Target QSR Trade  
M :22H: :PAYM/ /APMT Against Payment 
Indicator 
4!c 
M :16R: CONFPRTY  Mandatory Repeat 
Block Start 
 
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]] 34x 
O :20C: :PROC//  [[Buyer]] (Contra) X-ref 16x 
O :70C: :PACO/ /GSCC [[participant]] Contact 
Narrative 
(4*35x) 
   /TDID [[Buyer]] (Contra) Trader 
[[ID]] 
20c 
O :70E: :DECL/ /GSCC Narrative/ Additional 
Reference Numbers/ 
Information 
(10*35x) 
   /CORR Party = MPID of [[Buyer]]’s 
Correspondent firm 
4c 
O :22F: :TRCA/ /AGEN Capacity Indicator – 
Acting as Agent 
Indicator or 
4!a 
   /PRIN Acting as Principal 
Indicator 
 
M :16S: CONFPRTY  Repeat Block End  
M :16R: CONFPRTY  Mandatory Repeat 
Block Start 
 
M :95R: :SELL/ GSCC/PART Party = [[Seller]] 34x 
O :20C: :PROC//  [[Seller]] (Contra) X-ref 16x 
O :70C: :PACO/ /GSCC [[participant]] Contact 
Narrative 
(4*35x) 
   /TDID [[Seller]] (Contra) Trader 
[[ID]] 
20c 

---

## Page 34

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 34 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
O :70E: :DECL/ /GSCC Narrative/ Additional 
Reference Numbers/ 
Information 
(10*35x) 
   /CORR Party = MPID of [[Seller]]’s 
Correspondent Firm 
4c 
O :22F: :TRCA/ /AGEN Capacity Indicator – 
Acting as Agent 
Indicator or 
4!a 
   /PRIN Acting as Principal 
Indicator 
 
M :16S: CONFPRTY  Repeat Block End  
M :36B: :CONF/ /FAMT/ Quantity as Face 
Amount (Par) or 
15d 
   /UNIT/ Quantity as Units / 
[[shares]] 
 
M :35B: /US/  Security Identifier – 
[[CUSIP]] 
4 * 35x 
O :70E: :TPRO/ /GSCC Trade Instruction 
Processing Narrative 
(10*35x) 
   /DKRS DK Reason (see 
Appendix E) 
4!c 
   /DEST Destination Indicator 
(see Appendix E) 
2!c 
   /ITYP Issue Type (see 
Appendix E) 
2!c 
   /SDAD [[settlement]] Date 
Adjustment 
4n 
   /RVSL Trade Reversal Indicator 4!c 
   /SPXR MSRB Special 
Condition Indicators 
4!c 
   /RCTL Reversal Control 
Number 
16x 
   /YIEL Yield [N]15d 
   /RGDP Regulatory dollar price 13d 
   /MISC Miscellaneous 9d 
M :16S: CONFDET  Block End  
M :16R: SETDET  Optional Block Start  

---

## Page 35

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 35 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
M :22F: :SETR/ /RPTO [[settlement]] Indicator – 
Reporting-only or 
4!c 
   GSCC/STRD [[settlement]] Type 
Indicator – Special 
Trade or 
4!c 
   GSCC/CPRO Comparison Only  
M :16R: AMT  Optional Block Start  
M :19A: :SPCN/ /USD Special Concessions or [N]15d 
  :EXEC/ /USD Executing [[Broker]] 
Commission 
15d 
M :16S: AMT  Block End  
M :16R: AMT  Optional Block Start  
M :19A: :ACRU/ /USD Accrued Interest 
Amount 
15d 
M :16S: AMT  Block End  
M :16S: SETDET  Block End  
M :16R: OTHRPRTY  Optional Block Start  
M :95Q: :MEOR//  Originator of message (if 
other than the Sender) 
4!c//6c 
M :16S: OTHRPRTY  Block End  
 
  

---

## Page 36

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 36 
MT515 Field Specifications 
The following table shows the field specifications for MT515: 
Block/ Tag Notes 
Message Header Each message must contain a message header. All header fields are mandatory fixed format 
with trailing blanks, where required. 
Password 
12!c 
[[FICC]] assigns a password that enables the sender to submit trades on behalf of specific 
clients. 
Sender 
8!c 
[[participant]] [[ID]] 
Message Type 
3!n/3!n/4!c 
The first three characters indicate to the recipient the message type (515); the second three 
positions reflect the version of the message interface (currently always 000). The last four 
characters indicate the [[issuer]] code used in the message (“GSCC”). 
Receiver 
8!c 
NSCCTRRS ([[NSCC]] Trade Registration and Reconciliation System) is always the recipient of 
the MT515 messages sent to CMU RTTM-only or sent to both CMU RTTM and a regulator. 
NSCCREGO ([[NSCC]] Trade Reporting – Regulatory- Only) is the only recipient of the MT515 
(regulatory- only) messages. 
GENL This mandatory block provides general information regarding he message. It appears only 
once in a trade contract. 
20C Sender Message Reference 
SEME// – Contains the sender’s message reference number. It is mandatory and must 
contain a unique number to unambiguously identify each message sent to CMU RTTM. (This 
is a communications message number, not a trade number.) It is suggested that clients use a 
number that includes a date followed by either a timestamp or a sequence number, ensuring 
uniqueness. 
Note: While the SWIFT message accommodates both uppercase and lowercase 
alphanumeric and certain symbols, populate this field with an uppercase alphanumeric 
value for CMU RTTM purposes. It cannot contain symbols or hyphens.  
Example: :20C::SEME//200303310001 
23G Function of the Message 
This mandatory field identifies the function of the message. It is either a new message 
(NEWM) for instruct, modify, or DK messages, or it is a CANC for a cancellation of a previous 
message. 
• NEWM – Used for a new trade, a trade modification, or a DK message. 
• CANC – Used to request the cancellation of a trade. 
Example: :23G:NEWM 
98C Preparation Date and Time 
• PREP// –This CMU RTTM mandatory field contains the date and time the message 
sent to CMU RTTM was prepared. 
Note:  The “C” format for this (98) tag indicates  a date /time format of 
“YYYYMMDDHHMMSS”. 
Example: :98C::PREP//20151201083005 
22F Trade Transaction Type Indicator (TRTR) 
This mandatory field specifies whether  the trade (or reversal) is bilateral, locked-in, or 
demand. 
• TRTR/GSCC/CASH – Use on all trades requiring two-sided (bilateral) matching. 
Trades targeting [[syndicate]] or QSR trades must also use this qualifier [[Option]]. 
• TRTR/GSCC/TRLK – Use on locked-in trades. QSR source trades must use this 
qualifier [[Option]]. 
• TRTR/GSCC/TRDC – Use on demand trades. [[syndicate]] source trades must use 
this qualifier [[Option]]. 
Example: :22F::TRTR/GSCC/TRLK 
 
LINK The LINK block can be repeated for the various reference qualifiers required on a trade 
contract. It is intended to provide the required information to identify the trade. Enclose 
each reference number within a Start Link block (:16R:LINK) and End Link block 
(:16S:LINK). Each LINK repeating subsequence is within the GENL block. At least one LINK 
sequence is required on the MT515 message. 

---

## Page 37

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 37 
Block/ Tag Notes 
20C Reference 
The reference numbers provided by the client must contain uppercase alphanumeric 
characters – and must not contain symbols or hyphens. Each reference number must be 
enclosed in a LINK Start and End block. MT515 DK messages (submitted against 
contraparty trades) [[DO]] not contain reference numbers in this sequence but require the 
MAST qualifier to include on the record. 
• MAST// – Master Reference Number – Contains the client’s reference number 
for the trade (external reference number). This field must be unique for instructs, and 
it should be populated with the primary reference number that the client uses to 
track trades on the CMU RTTM system. It is mandatory for inbound MT515 
INSTRUCT and DK messages. For DKs, this field should be populated with 
the value “NONREF”. For cancels and modifies, the client can send the external 
reference number (MAST), CMU RTTM reference number (LIST), or both. 
Otherwise, after matching, the match control number (COMM) can be used on 
modifies. 
• PREV// – Previous Reference Number – Used on either the Trade Modify or 
Trade Cancel MT515 records. On modify records, it is used to modify the 
reference number and should contain the client’s previous external reference 
number. For MT515 Cancel records (where you are submitting :23G:CANC and 
:22F::PROC/GSCC/CANC in the Confirmation Details (CONFDET) block), this field 
should be populated with the “NONREF” value. [[DO]] not use this field on instruct or 
DK records. 
• LIST// – CMU RTTM Reference Number – Contains CMU RTTM’s reference 
number (TID) generated for the trade upon submission. For pre-match cancels 
and modifies, the client can send the external reference number (MAST), CMU 
RTTM reference number (LIST), or both to identify the trade. For post- match 
modifies, the client must include either X-ref (MAST), the CMU RTTM assigned 
TID (LIST), or the match control number (COMM). [[DO]] not use this field on instruct 
or for DK records. 
• TRRF// – Regulator Control Number – regulatory field – Specifies the control 
number generated by the applicable Regulator application. It may be used on 
MT515 Modify and MT515 Cancel messages to identify trades being modified 
or canceled. 
• COMM// –Match Control Number – Contains the Match Control Number assigned to 
a pair of trades by CMU RTTM at the time of matching. It can be used by clients 
only on MT515 Modify records submitted post-matching. 
Note: While the SWIFT message accommodates both uppercase and lowercase 
alphanumeric and certain symbols, populate this field with an uppercase alphanumeric 
value for CMU RTTM purposes. It cannot contain symbols or hyphens, except where CMU 
RTTM assigns the reference number. 
Example: :20C::MAST//PARTREF1 
CONFDET The mandatory CONFDET (confirmation details) block appears only once in a trade 
contract. It contains trade and confirming party details. 
98C Trade Date 
TRAD// –This mandatory field is used on all messages to specify the trade date and trade 
time. (The “C” format for this (98) tag indicates a date and time format of 
“YYYYMMDDHHMMSS”.) 
Example: :98C::TRAD//20150331095510 
 
98A 
98B 
[[settlement]] Date 
This mandatory field is used on all MT515 messages. One of the following options must 
appear for this field: 
• SETT// – Used on all messages to specify [[settlement]] date. It is required on all 
regular way trade and new issue (NI) final money trades. (The “A” format for this tag 
(98) indicates a date format of “YYYYMMDD”.) 
• SETT//WISS – Used on all new issue trades where the [[settlement]] date is not 
known, and no final money is reflected on the trade. (This is the “B” format of tag 
(98).) 
Example: :98A::SETT//20150331 
 
 

---

## Page 38

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 38 
Block/ Tag Notes 
90A Deal Price 
This field is reflected on all messages. It contains the execution price type and price. Price 
is required where no final money is provided (applicable only to WI trades). Only one Tag 
90A is allowed per trade contract. The price is in SWIFT standard format, which is left 
justified, with commas removed, and a comma used instead of a decimal. The following price 
types can be specified: 
• DEAL//PRCT/ – Used for dollar prices. Where a trade is executed on price and 
no final money is provided in the [[settlement]] Amount field (:19A::SETT//), the 
dollar price should be reflected. Final money trades, where a [[settlement]] amount 
is entered, should reflect a value of zero “0,” in this field. 
DEAL//YIEL/ – Used for yield priced trades. When a trade is executed on yield, no final 
money is provided in the [[settlement]] Amount field (:19A::SETT//). 
Note: While the SWIFT format accommodates 15d characters (with decimal), the [[NSCC]] 
system supports a maximum field size of 13d for the dollar price (DEAL//PRCT). The format 
must be 9999,99999999. Yield price (DEAL//YIEL) must not exceed a maximum field size of 
8d in the format of 999,9999. 
Example:  :90A::DEAL//PRCT/99,625 
94B Place of Trade – Market of Execution (TRAD) 
This field is used to specify the market of execution for the trade. Modification of this field 
is not supported on CMU RTTM. If the market of execution changes, clients need to cancel 
and resubmit the trade. One of the following entries is required on all MT515 messages: 
• TRAD/GSCC/OTCP – [[Over-The-Counter]] Corporate 
• TRAD/GSCC/OTMU – [[Over-The-Counter]] Municipal 
•  TRAD/GSCC/OTUI – [[Over-The-Counter]] Unit Investment Trust.  
Note: The Market of Execution of the trade should be consistent with the Destination 
designated in the :70E::TPRO// (DEST) for regulatory reporting field.  For example, OTMU 
trades should populate the DEST field as DEST01(CMU RTTM), DEST02 (MSRB), or both. 
Example: :94B::TRAD/GSCC/OTMU 
19A [[settlement]] Amount 
• SETT// – Used to specify the [[settlement]] amount. It is required for all Regular Way 
trades; however, it can be omitted on WI trades where the [[settlement]] date is not 
available, and the final money cannot be calculated. 
The amount is in SWIFT standard format–left justified, with commas removed, and 
a comma used instead of a decimal. The amount is always preceded by a 3-
character ISO currency code (“USD” for [[NSCC]] trades). 
Note: While the SWIFT format can accommodate a value of 15d (with decimal), the 
[[NSCC]] system supports a field size of 13d. 
Example: :19A::SETT//USD1000500,5 
22H Trade Type Indicator (BUSE) 
This field is required on all MT515 messages.  There are two allowable values for the BUSE 
qualifier: 
• BUSE//BUYI – Indicates that the record submitted is a buy. 
• BUSE//SELL – Indicates that the record submitted is a sell. 
Example: :22H::BUSE//BUYI 
22F Type of Price – Weighted Price 
• PRIC/GSCC/WGTP – regulatory field – This indicator can be used on MT515 
instruct, cancel, or modify messages to notify the regulator if the price of the trade 
was based on the weighted average of previous transactions. 
Example: :22F::PRIC/GSCC/WGTP 
22F Processing Indicator (PROC) 
This processing indicator enables the client to indicate to CMU RTTM the type of record/ 
command being submitted on the MT515. 
• PROC/GSCC/INST – Indicates that the MT515 is an INSTRUCT record. 
• PROC/GSCC/CANC – Indicates that the MT515 is a CANCEL record. Only pre-match 
cancels are allowed on [[NSCC]] CMU RTTM. 
• PROC/GSCC/MDFC – Indicates that the MT515 is a MODIFY record. Modify records 
can update matching fields where the trade is not matched or sent to [[settlement]]. After 
matching, only the client X-ref or regulatory fields can be modified on CMU RTTM. 
• PROC/GSCC/TDDK – Indicates that the MT515 is a DK record.  

---

## Page 39

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 39 
Block/ Tag Notes 
Note: All of the above record types also apply to reversals. The reversal indicator 
(:70E::TPRO//GSCC/RVSL) is used to flag reversal records. 
Example: :22F::PROC/GSCC/INST 
22F Trade Type / Target Indicator (TTCO) 
This indicator field is used to identify a QSR trade submission as well as trades targeting 
QSR trades. Allowable options for this field are as follows: 
• TTCO/GSCC/TSQS – Indicates that this is a QSR Trade Submission. This 
[[Option]] applies to all QSR submitted MT515 messages. 
• TTCO/GSCC/TTQS – Indicates that the trade is targeting a QSR trade. This [[Option]] 
applies to all Target QSR MT515 messages. 
Note: [[Option]] TSQS must have selected a Trade Transaction Type Indicator (:22F::TRTR) of 
TRLK (Locked-In). [[Option]] TTQS must have selected a TRTR of CASH (Bilateral). 
Example: :22F::TTCO/GSCC/TSQS 
22H Payment Indicator (PAYM) 
This Payment Indicator field is mandatory for the MT515 message. All trades submitted to 
CMU RTTM must provide the following qualifier: 
• PAYM//APMT – Indicates that the trade settles against payment. 
Example: :22H::PAYM//APMT 
36B Quantity of [[securities]] (CONF)2 
This field is mandatory for all MT515 messages. The quantity of the financial instrument is 
in SWIFT Standard Format, which is left justified, with commas removed, and a comma 
used instead of a decimal. Valid options are as follows: 
• CONF//FAMT/ – FAMT indicates the face amount (par), and it should be used 
on all municipal and corporate bond trade records. 
• CONF//UNIT/ – Indicates the quantity in units or [[shares]]. This applies only to 
unit investment trust ([[UIT]]) trades. 
Note: While the SWIFT format can accommodate a value of 15d in this field, the CMU RTTM 
system can only accommodate a maximum field size of 10d. 
Example: :36B::CONF//FAMT/1000000, 
35B Identification of Security6 
The security involved is identified in the US by specifying the ISO country identifier 
(‘/US/’), followed by the [[CUSIP]] number. Modification of this field is not supported on CMU 
RTTM. 
Note: While the SWIFT layout accommodates a format of 4 * 35x, a 9!c (alpha numeric) 
value should populate the field for the [[CUSIP]]. 
Example: :35B:/US/78764HAD6 
70E Trade Instruction Processing Narrative (TPRO)5 
This field reflects additional transaction related information that is unsupported elsewhere 
in the SWIFT MT515 layout. Clients use it to provide CMU RTTM specific and regulatory 
fields. Regulatory data, however, is not required on any MT515 messages. If present, 
regulatory data is validated for SWIFT compliance. (For information about regulatory fields, 
see Appendix G.) 
• TPRO//GSCC – Denotes narrative trade instruction processing information 
related to CMU RTTM. 
• /DKRS – Use on all MT515 DK messages to specify the reason for the DK. For 
the four character code, see Appendix E. 
• /DEST – Use to specify the destination of the message as CMU RTTM (01), 
MSRB (02). This is a repeating field allowing multiple entries. This field should be 
populated according to the following rules: 
• Specify DEST01 (CMU RTTM) for all MT515 records requiring 
matching/processing by CMU RTTM. 
• Specify DEST02 (MSRB) to indicate that the record should be 
forwarded to the MSRB. All records other than DK may reflect a 
DEST02 value. 
• /ITYP – Used by [[syndicate]] managers and members to specify a [[syndicate]] 
(ITYPSY) or target [[syndicate]] (ITYPTS) trade. 
• /SDAD – [[settlement]] date adjustment subqualifier is used to specify the number of 
extended [[settlement]] days. This field must be included on all extended [[settlement]] 

---

## Page 40

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 40 
Block/ Tag Notes 
WI trades. Optionally, it can be populated for Regular Way (RW) extended 
[[settlement]] trades. This field is not applicable to [[syndicate]] trades. 
• /RVSL – Indicates that the MT515 record is a reversal. To cancel a trade post-
matching, a reversal trade must be entered to offset a previously submitted trade. 
CMU RTTM does not link a reversal to the trade it is intended to reverse and 
treats a reversal as a completely new trade. All MT515 record types also apply for 
reversal trades; therefore, this [[Option]] should be included in all MT515 
messages for reversals. 
• /SPXR – regulatory field – Special Condition Indicator Code field is used for trades 
executed at a price different from the prevailing market price. See MSRB Special 
Condition Indicators. 
• /RCTL – regulatory field – Reversal Control Number field should be populated 
with the client X-ref (MAST) or the CMU RTTM reference number (LIST) of the 
trade being reversed. 
• /YIEL – regulatory field – Subqualifier used on MT515 messages where the yield 
price is not reflected in the :90A::DEAL// field (such  as, where :90A::DEAL// is 
populated as :90A::DEAL//PRCT/, followed by either a dollar price or zero "0,"). 
Inter-dealer trades should report yield in the DEAL//YIEL field if executed on that 
basis. 
• /RGDP – regulatory field – Subqualifier used on all MT515 MUNI messages to 
report dollar price to MSRB. The regulatory dollar price must be in the “13D” 
format and cannot exceed “9999,99999999”. Regulatory dollar price is used to 
report the contractual dollar price on inter-dealer trades. This field must be 
populated for all inter-dealer trades where the [[settlement]] date is known (for 
example, regular way trades with final money) and for all when-issued inter-dealer 
trades effected on the basis of dollar price or final money. For when-issued trades 
effected on the basis of yield when the [[settlement]] date is not known, this field must 
be left blank. Note that the Dollar Price field continues to be used only for 
dealers submitting When Issue or [[syndicate]] Takedown trades with dollar price 
(Tag :90A: Block/Qualifier :DEAL/ Subqualifier/Options /PRCT/ Description Deal 
Price) and in these cases, dealers must separately report the contractual dollar 
price in the Regulatory Dollar Price field. 
• /MISC – regulatory field – For future use. It must be in the “9D” format and 
cannot exceed “999999,99”. 
Note:  
A continuous string of all applicable subqualifiers (to a maximum of 35 characters per 
line) follows the TPRO//GSCC qualifier. A best practice is not to split qualifiers or 
options across lines and to add qualifiers in the order they appear in this spec. 
Example: 
:70E::TPRO//GSCC//DEST01/DEST02 
/RVSL 
/SPXRR001 
/YIEL3,5/RGDP96,98 
CONFPRTY The Mandatory Confirming Party block must be repeated for each party to a trade. 
Enclose each party’s details within its own Start Party block (:16R:CONFPRTY) and 
End Party block (:16S:CONFPRTY). On every trade, there should be two (one [[Buyer]] 
and one [[Seller]]) Confirming Party sequences. One of these parties is also the 
submitter of the MT515 record. Certain fields in the CONFDET block (36B, 35B, and 
70E) must follow the Confirming Party subsequences. 
95R Party 
• BUYR/GSCC/PART – Specifies the buying party. (The “GSCC” [[issuer]] code 
allows the specification to include the [[NSCC]] client or contra [[ID]], depending on who 
is acting as [[Buyer]] or [[Seller]]). 
• SELL/GSCC/PART – Specifies the selling party. 
Note:  
While the SWIFT layout supports a format of 35x for this field, the client must populate 
the field with the appropriate qualifier and four character [[participant]] [[ID]] for the [[Buyer]] or 
[[Seller]]. Customer records have either the [[Buyer]] or [[Seller]] party with a [[default]] value of 
“CUST”. 

---

## Page 41

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 41 
Block/ Tag Notes 
For example, :95R::BUYR/GSCC/PART9501 
20C Processing Reference 
• PROC// – Used on DK messages in the appropriate [[Buyer]] or [[Seller]] 
subsequence to indicate the contraparty’s external reference number of the trade 
being DKed. 
Example: :20C::PROC//CONTRAXREF1 
70C [[participant]] Contact Narrative (PACO) 
Used in the appropriate [[Buyer]] or [[Seller]] confirming party sequence on MT515 instructs, 
cancels, or modifies submitted to provide information regarding the individual/desk at the 
contraparty that executed the trade. The trader [[ID]] field is only for informational purposes, 
and it is captured for the purposes of passing the information to the contraparty on 
MT518 Match Request messages. This field is not matched or validated, and it is not a basis 
for rejection or DK capabilities. 
• PACO//GSCC  –  Denotes  client  contact  narrative  information specific to CMU 
RTTM. 
• /TDID – Used in the appropriate BUYR or SELL confirming party sequence to 
indicate the following: 
• For MT515 instruct, cancel, or modify records, used by the submitter to 
indicate the [[Buyer]] or [[Seller]] contraparty [[ID]] of the trader that executed the trade. 
• For MT515 DK messages, used to reflect the buying or selling submitter’s [[ID]] of 
the trader that executed the trade (as originally submitted by the contraparty). 
• For STEPOUT trades this field is populated with STEP 
 
Example: 
:70C::PACO//GSCC/TDIDTRADER1 
:70C::PACO//GSCC/TDIDSTEP 
70E Narrative (DECL) 
Used in each party subsequence to identify the executing/correspondent firm, where 
applicable. 
• DECL//GSCC – Denotes narrative information specific to CMU RTTM. 
• /CORR – Used in the BUYR and/or SELL confirming party sequences to indicate 
the four-character MPID of the [[NSCC]] client's correspondent. Where there is no 
other effecting or correspondent firm, place the four character MPID of the [[NSCC]] 
client in this field. 
Note: 
While this field can support a narrative 10 * 35x, the client, at this time, should only provide 
the above qualifiers and the [[FINRA]] assigned executing [[Broker]] symbol in the CORR field. 
 
Example: :70E::DECL//GSCC/CORRATGN 
22F Trading Capacity (TRCA) 
Used to identify the dealer’s trading capacity as principal or agent. Populate this field as 
follows: 
• QSR should populate the appropriate [[Buyer]] or [[Seller]] block to reflect the 
contraparty trading capacity. 
• [[syndicate]] managers should populate both their own as well as the contraparty's 
capacity in the appropriate [[Buyer]] or [[Seller]] block 
– regulatory field. 
• Bilateral trade submitters should populate their own capacity in the appropriate 
[[Buyer]] or [[Seller]] block – regulatory field. 
Valid options for this field are: 
• TRCA//AGEN – Denotes that the party, contraparty, or both is acting as the 
agent for a customer. 
• TRCA//PRIN – Denotes that the party contraparty, or both is acting as 
principal. 
 
Example: :22F::TRCA//AGEN 
SETDET This optional block and the nested AMT blocks are necessary only when Commission 
and/or Accrued Interest is specified on the trade. 

---

## Page 42

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 42 
Block/ Tag Notes 
22F [[settlement]] Indicator (SETR) 
This field is SWIFT mandatory for the block, and it must be included on all MT515 
messages that contain a SETDET block. The available options are: 
• SETR//RPTO – Select if the trade is not a special trade (for example, if the trade 
does not reflect one of the following options for this field). 
• SETR/GSCC/STRD – Indicates that the trade is a special trade and settles trade-
for-Trade. 
• SETR/GSCC/CPRO – Indicates that the trade is comparison only and will not go to 
[[settlement]]. 
Note:  
For a mapping of the above [[settlement]] type indicators to those used on batch input/output, 
see Appendix H. 
Example: :22F::SETR//RPTO or :22F::SETR/GSCC/STRD 
AMT This optional repeating block is only necessary to support including commission, 
concession, accrued interest, or both. This block should always be included within 
the [[settlement]] Details (SETDET) block. 
19A Commission Amount 
Used to support the submission of commissions or concessions, which are specified as an 
amount per trade (rather than amount per hundred). Valid options for this field are: 
• SPCN//USD – Specifies the special concession amount on WI trades. 
Concessions appear only on trades submitted with a yield price (:90A::DEAL//YIEL/). 
This field allows for positive and negative entries. 
• EXEC//USD – regulatory field – Specifies the executing [[Broker]] commission on 
customer and/or regulatory agency trades. 
Example: A commission/concession rate of .125 per 100 PAR equals 
1.25 per 1,000 PAR. The commission/concession amount for a Face 
22F [[settlement]] Indicator (SETR) 
This field is SWIFT mandatory for the block, and it must be included on all MT515 
messages that contain a SETDET block. The available options are: 
• SETR//RPTO – Select if the trade is not a special trade (for example, if the trade 
does not reflect one of the following options for this field). 
• SETR/GSCC/STRD – Indicates that the trade is a special trade and settles trade-
for-Trade. 
• SETR/GSCC/CPRO – Indicates that the trade is comparison only and will not go to 
[[settlement]]. 
Note:  
For a mapping of the above [[settlement]] type indicators to those used on batch input/output, 
see Appendix H. 
 
Example: :22F::SETR//RPTO or :22F::SETR/GSCC/STRD 
AMT This optional repeating block is only necessary to support including commission, 
concession, accrued interest, or both. This block should always be included within 
the [[settlement]] Details (SETDET) block. 
19A Commission Amount 
Used to support the submission of commissions or concessions, which are specified as an 
amount per trade (rather than amount per hundred). Valid options for this field are: 
• SPCN//USD – Specifies the special concession amount on WI trades. 
Concessions appear only on trades submitted with a yield price (:90A::DEAL//YIEL/). 
This field allows for positive and negative entries. 
• EXEC//USD – regulatory field – Specifies the executing [[Broker]] commission on 
customer and/or regulatory agency trades. 
Example: A commission/concession rate of .125 per 100 PAR equals 
1.25 per 1,000 PAR. The commission/concession amount for a Face Value of 10,000 = 
1.25 *10 or 12.5. This amount is populated as USD12,5. 
Note:  
The value in this field is an amount per trade. The commission amount field is in SWIFT 
standard format–left justified, with commas removed, and a comma used in lieu of a decimal. 
The amount must be preceded by a three- character ISO currency code. 
Example: :19A::SPCN//USDN12,5 

---

## Page 43

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 43 
Block/ Tag Notes 
19A Accrued Interest 
This required field should be populated on all MT515 messages for final money trades. 
• ACRU//USD – Specifies the accrued interest amount required on all MT515 
submissions. It is populated where a trade should settle with accrued interest. 
Note:  
While SWIFT format allows for a field size of 15d, the [[NSCC]] system can support a 
maximum size of 10d. 
For example, :19A::ACRU//USD1040, 
OTHRPRTY This optional block is only necessary if the originator of the message is not the 
same as the sender of the message. 
95Q Originator of Message (MEOR) 
MEOR// – regulatory field – Specifies the originator of the message if NOT the sender 
identified in the header of the message. 
For example, :95Q::MEOR//ORGN 
 

---

## Page 44

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 44 
MT515 Field Analysis 
This section contains an analysis of the fields available in each MT515 message. For each record type, a check mark shows that it is possible for that 
field to appear on that record. This check mark does not indicate that a field is mandatory for a given record type. If there is no check mark, that field is 
not applicable for the record type in question, 
M/O Tag Block/ Qualifier Subqualifier Field Description INST CANC MDFC TDDK 
    Message Header     
    Password     
    Sender     
    Message Type     
    Receiver     
M :16R: GENL  Start of Block     
M :20C: :SEME//  Sender’s Reference for this message     
M :23G: NEWM  Message Function = New Message or     
  CANC  Cancel     
O* :98C: :PREP//  Preparation Date/Time     
M :22F: :TRTR/ GSCC/CASH Trade Indicator = Bilateral Trade or     
   GSCC/TRLK Locked-in Trade or     
   GSCC/TRDC Demand Trade     
M :16R: LINK  Repeat Block Start     
O :20C: :MAST//  Master Reference Number     
M :16S: LINK  End of Block     
M :16R: LINK  Repeat Block Start     
O :20C: :PREV//  Previous Reference Number     
M :16S: LINK  End of Block     
M :16R: LINK  Repeat Block Start     
O :20C: :LIST//  CMU RTTM Reference Number (TID)     
M :16S: LINK  End of Block     
M :16R: LINK  Repeat Block Start     
O :20C: :TRRF//  Regulator Control Number     
M :16S: LINK  End of Block     
M :16R: LINK  Repeat Block Start     
O :20C: :COMM//  Match Control Number     
M :16S: LINK  End of Block     
M :16S: GENL  End of Block     

---

## Page 45

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 45 
M/O Tag Block/ Qualifier Subqualifier Field Description INST CANC MDFC TDDK 
M :16R: CONFDET  Start of Block     
M :98C: :TRAD//  Trade Date/Time     
M :98A: :SETT//  [[settlement]] Date or     
M :98B: :SETT// WISS [[settlement]] Date – [[settlement]] to be 
completed when Security is issued 
    
M :90A: :DEAL/ /PRCT/ Deal Price Percentage or     
   /YIEL/ Yield     
O :94B: :TRAD/ GSCC/OTCP Market of Execution 
[[Over-The-Counter]] Corporate or 
    
   GSCC/OTMU [[Over-The-Counter]] Municipal or     
   GSCC/OTUI [[Over-The-Counter]] Unit Investment Trust     
O :19A: :SETT/ /USD [[settlement]] Amount     
M :22H: :BUSE/ /BUYI Trade Type Buy or     
   /SELL Sell     
O :22F: :PRIC/ GSCC/WGTP Type of Price – Weighted Price     
O* :22F: :PROC/ GSCC/INST MT515 Record Type – Instructor     
   GSCC/CANC Cancel or     
   GSCC/MDFC Modify or     
   GSCC/TDDK DK     
O :22F: :TTCO/ GSCC/TSQS Trade Type/Target Indicator – QSR     
   GSCC/TTQS Target QSR Trade     
M :22H: :PAYM/ /APMT Against Payment Trade     
M :16R: CONFPRTY  Mandatory Repeat Block Start     
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]]     
O :20C: :PROC//  [[Buyer]] (Contra) reference     
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative     
   /TDID [[Buyer]] (Contra) Trader [[ID]]     
O :70E: :DECL/ /GSCC Narrative/ Additional Reference Numbers/ 
Information 
    
   /CORR Party = MPID of [[Buyer]]’s Correspondent 
firm 
    
O :22F: :TRCA/ /AGEN Capacity Indicator – Acting as Agent 
Indicator or 
    
   /PRIN Acting as Principal Indicator     
M :16S: CONFPRTY  Repeat Block End     
M :16R: CONFPRTY  Mandatory Repeat Block Start     
M :95R: :SELL/ GSCC/PART Party = [[Seller]]     

---

## Page 46

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 46 
M/O Tag Block/ Qualifier Subqualifier Field Description INST CANC MDFC TDDK 
O :20C: :PROC//  [[Seller]] (Contra) reference     
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative     
   /TDID [[Seller]] (Contra) Trader [[ID]]     
O :70E: :DECL/ /GSCC Narrative/ Additional Reference Numbers/ 
Information 
    
   /CORR Party = MPID of [[Seller]]’s Correspondent 
Firm 
    
O :22F: :TRCA/ /AGEN Capacity Indicator – Acting as Agent 
Indicator or 
    
   /PRIN Acting as Principal Indicator     
M :16S: CONFPRTY  Repeat Block End     
M :36B: :CONF/ /FAMT/ Quantity as Face Amount (Par) or     
   /UNIT/ Quantity as Units / [[shares]]     
M :35B:  /US/ Identification of Financial Instrument- 
[[CUSIP]] 
    
O :70E: :TPRO/ /GSCC Trade Instruction Processing Narrative     
   /DKRS DK Reason (see Appendix E)     
   /DEST Destination Indicator (Note: This is a 
repeating field) 
01 = CMU RTTM 
    
   /DEST 02 = MSRB     
   /ITYP Issue Type – SY = [[syndicate]] or     
    TS = Target [[syndicate]] or     
    RW = Regular Way or     
    NI = New Issue     
   /SDAD [[settlement]] Date Adjustment     
   /RVSL Trade Reversal Indicator     
   /SPXR MSRB Special Condition Indicators     
   /RCTL Reversal Control Number     
   /YIEL Yield     
   /RGDP Regulatory Dollar Price     
   /MISC Miscellaneous     
M :16S: CONFDET  End of Block     
M :16R: SETDET  Start of Optional Sequence     
M :22F: :SETR/ /RPTO [[settlement]] Indicator = Reporting-Only or     
   GSCC/STRD [[settlement]] Type Indicator – Special Trade 
or 
    

---

## Page 47

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 47 
M/O Tag Block/ Qualifier Subqualifier Field Description INST CANC MDFC TDDK 
   GSCC/CPRO Comparison Only     
M :16R: AMT  Repeat Block Start     
M :19A: :SPCN/ /USD Special Concessions or     
  :EXEC/ /USD Executing [[Broker]] Commission     
M :16S: AMT  End of Block     
M :16R: AMT  Repeat Block Start     
M :19A: :ACRU/ /USD Accrued Interest Amount     
M :16S: AMT  End of Block     
M :16S: SETDET  End of Block     
M :16R: OTHRPRTY  Optional Block Start     
 :95Q: :MEOR//  Originator of message (if other than the 
Sender) 
    
M :16S: OTHRPRTY  End of Block     

---

## Page 48

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 48 
MT509 Message 
The SWIFT MT509 message is specified as a Trade Status message. It is used to convey the status of each 
input message that has been submitted to CMU RTTM by an [[NSCC]] [[Member]] or an authorized locked- in 
submitter. The MT509 message does not contain full trade details. The message provides the trade status 
along with the full set of reference numbers to enable the client to identify the trade or record submitted. 
Certain status messages also include additional fields, such as reason codes for reject messages. Fi eld 25D in 
the status (STAT) block indicates to the recipient the type of message being sent (in the case of a modify or DK 
reject, a second field, 70D in the Reason (REAS) block, must also be read to determine the record type). The 
qualifiers for these fields are shown for each example. The following table shows the SWIFT MT509 messages 
that are generated for each of the trade statuses: 
 Status Message Usage 
1 Trade Input Accepted 
(:25D::IPRC//PACK) 
Sent to the trade submitter to acknowledge that its trade has been validated 
and is waiting for further processing within CMU RTTM. 
2 Trade Input Rejected 
(:25D::IPRC//REJT) 
Sent to the trade submitter to indicate that its trade has been rejected by 
CMU RTTM as part of the validation process. The reason for the 
rejection is also indicated on the message (:24B::REJT in the Reason 
(REAS) Block). 
This message is always used whenever an MT515 has been rejected 
because the message was non-SWIFT compliant. 
3 Modify Accepted 
(:25D::IPRC/GSCC/MODA) 
Sent to the submitter of a trade modification to acknowledge that the 
modification message has been validated and is waiting for further 
processing within CMU RTTM. 
4 Modify Rejected 
(:25D::IPRC//REJT and 
:70D::REAS//GSCC/MDRJ) 
Sent to the submitter of a trade modification to indicate that the 
modification message has been rejected by CMU RTTM as part of the 
validation process. The reason for the rejection is also indicated on the 
message (:24B::REJT in the Reason (REAS) Block). 
 
Note: Where CMU RTTM cannot read an MT515 Modify and it is not 
SWIFT compliant, CMU RTTM does not generate a Modify Rejected 
Record. Instead, a Trade Input Rejected message is generated with the 
reason code indicating the MT515 message was not SWIFT compliant. 
5 Modify Processed 
(:25D::IPRC/GSCC/MODP) 
Sent to the submitting party when a trade modification has been 
successfully performed within CMU RTTM. The contraparty receives an 
MT518 reflecting new CMU RTTM-related trade details. 
6 Deleted Unmatched Transaction 
(:25D::IPRC/GSCC/DELE) 
Sent to the submitting party indicating that an unmatched trade has been 
deleted from CMU RTTM's processing system. Trades can remain 
unmatched in the system for a maximum of three days before they are 
deleted. The contraparty receives an MT518 indicating that the advisory 
has been deleted. 
7 Deleted due to DK 
(:25D::IPRC/GSCC/DEDK) 
Sent to the trade submitter to inform it that the trade it submitted has 
been administratively deleted by the CMU RTTM system because it was 
DKed by the contraparty. This message is applicable only to demand and 
bilateral trades, not for locked-in trades. 
8 Deleted due to Memo 
(:25D::IPRC/GSCC/DEME) 
Sent to the trade submitter to inform it that the trade it submitted has 
been administratively deleted by the CMU RTTM system because it was 
in Memo Status. Trades are deleted if they remain in Memo Status for 
three days. This message is applicable only to New Issue Trades. 
9 Deleted due to Pending 
(:25D::IPRC/GSCC/DEPE) 
Sent to the trade submitter to inform it that the trade it submitted has 
been administratively deleted by the CMU RTTM system because it was in 
Pending Status. Trades that remain in Pending Status at the end of the 
day are deleted on the night of submission date. This message is 
applicable only to New Issue Trades. 

---

## Page 49

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 49 
 Status Message Usage 
10 Deleted due to Security Detail 
Differences 
(:25D::IPRC/GSCC/DESD) 
Sent to the trade submitter to inform it that the trade it submitted has 
been administratively deleted by the CMU RTTM system because of 
security detail differences. This message is generated when a previously 
submitted Memo trade has a [[settlement]] date different from the issue date 
of the security. This message is applicable only to new issue trades. 
11 DK Accepted 
(:25D::IPRC/GSCC/PADK) 
Sent to the DK submitter to acknowledge that the DK sent has been 
validated and is waiting for further processing within CMU RTTM. 
12 DK Rejected 
(:25D::IPRC//REJT and 
:70D::REAS//GSCC/DKRJ) 
Sent to DK submitter to indicate that the DK sent has been rejected by 
CMU RTTM as part of the validation process. The reason for the 
rejection is also indicated on the message (:24B::REJT in the Reason 
(REAS) Block). 
Note: Where an MT515 DK cannot be read by CMU RTTM and is not 
SWIFT compliant, CMU RTTM does not generate a DK Rejected Record. 
Instead, a Trade Input Rejected message is generated with the reason 
code indicating the MT515 message was not SWIFT compliant. 
13 DK Processed 
(:25D::IPRC/GSCC/DPPR) 
Sent to the DK submitter to indicate that a trade submitted against it has 
been marked with a DK Status. The contraparty (the original trade 
submitter) has been notified of the DK and the reason for the DK through an 
MT518. 
14 Memo Status Assigned 
(:25D::IPRC/GSCC/ASME) 
Sent to the trade submitter to inform it that the trade submitted has 
been placed in Memo Status. The trade is not available for matching until 
the Memo Status is removed. This message is applicable only to New 
Issue Trades. 
15 Pending Status Assigned 
(:25D:: IPRC/GSCC/ASPE) 
Sent to the trade submitter to inform it that the trade submitted has 
been placed in Pending Status. The trade is not available for matching 
until the Pending Status is removed. This message is applicable only to 
New Issue Trades. 
16 Memo Status Removed 
(:25D:: IPRC/GSCC/RVME) 
Sent to the trade submitter to inform it that the trade previously placed 
in Memo Status has had the Memo Status removed and is available for 
matching. This message is applicable only to New Issue Trades. 
17 Pending Status Removed 
(:25D:: IPRC/GSCC/RVPE) 
Sent to the trade submitter to inform it that the trade previously placed 
in Pending Status has had the Pending Status removed and is available 
for matching. This message is applicable only to New Issue Trades. 
18 Cancel Accepted 
(:25D::CPRC//PACK) 
Sent to the submitter of a Trade Cancel to acknowledge that the message 
has been validated and is waiting for further processing within CMU RTTM. 
19 Cancel Rejected 
(:25D::CPRC//REJT) 
Sent to the submitter of a Trade Cancel to indicate that the message has 
been rejected by CMU RTTM as part of the validation process. Cancels 
submitted post- matching or after the trade has been sent to [[settlement]], are 
rejected. The reason for the rejection is also indicated on the message 
(:24B::REJT in the Reason (REAS) Block). 
 
Note: Where an MT515 Cancel cannot be read by CMU RTTM and is not 
SWIFT compliant, CMU RTTM does not generate a Cancel Rejected 
record. Instead, a Trade Input Rejected message is generated with the 
reason code indicating the MT515 message was not SWIFT compliant. 
20 Cancel Processed 
(:25D::CPRC//CAND) 
Sent to the submitter of the cancel when a trade is successfully 
canceled in CMU RTTM. 
21 Trade Matched 
(:25D::MTCH//MACH) 
Sent to all trade parties when a submitted trade has been matched, 
either as a result of matched Bilateral input or the administrative match of 
unilateral input by a valid Locked-in or Demand submitter. 
 
  

---

## Page 50

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 50 
Generating MT509 status messages described in the matrix is restricted as follows: 
• Where MT515 records are submitted for regulatory reporting-only, MT509 messages are not sent by 
CMU RTTM to the client. The MSRB message application (using CMU RTTM as a pass-through 
vehicle) generates all applicable outputs, except MT509 rejects for non-SWIFT compliance. This 
output is specified for clients in MSRB Specifications for Real - Time Reporting of Municipal [[securities]] 
Transactions. 
• Where MT515 records are submitted for both CMU RTTM and regulatory reporting, CMU RTTM 
sends all appropriate MT509 output related to CMU RTTM processing. Where the CMU RTTM 
application rejects a record, it is not forwarded to the regulator. However, a rejection notification is 
forwarded to the MSRB. MSRB specifies and sends MT509 status messages related to MSRB 
regulatory status to clients/MSRB members. 
• Where a record is rejected for submission to CMU RTTM for non-SWIFT compliance, it is not 
passed for processing to the MSRB. Rejection notifications are not forwarded to MSRB. 
  

---

## Page 51

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 51 
MT509 General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
    Message Header  
    Password 12!c 
    Sender 8!c 
    Message Type 3!n/3!n/4!c 
    Receiver 8!c 
M :16R: GENL  Block Start  
M :20C: :SEME//  Sender’s Reference for this Message 16x 
M :23G: INST  Message Function – Instruct or 4!c 
  CAST  Cancel  
O* :98C: :PREP//  Preparation Date/Time YYYYMMDDHHMMSS 
M :16R: LINK  Repeat Block Start  
M
2 :20C: :MAST//  [[participant]] External Reference 
Number 
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PREV//  Previous External Reference Number 16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :RELA//  Related Reference Number (Sender’s 
Reference) 
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :LIST//  CMU RTTM Assigned Reference 
(TID) 
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PROG//  Contraparty Reference Number 16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :COMM//  Match Control Number 16x 
M :16S: LINK  Repeat Block End  
M :16R: STAT  Repeat Block Start  
M :25D: :IPRC/ /PACK Trade Input Accepted or 4!c 
   /REJT Trade Input Rejected or  
   GSCC/MODA Modify Accepted or  
   GSCC/MODP Modify Processed or  
   GSCC/DELE Deleted Unmatched Transaction or  
   GSCC/DEDK Deleted due to DK or  
   GSCC/DEME Deleted due to Memo or  
   GSCC/DEPE Deleted due to Pending or  
   GSCC/DESD Deleted due to Security Detail 
Differences or 
 
 
2 MAST exists on all MT509 messages, except in the case where the MT509 message has been generated in 
response to an MT515 DK submitted or is a reject in response to receiving a non -SWIFT-compliant MT515. 

---

## Page 52

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 52 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
   GSCC/PADK DK Accepted or  
   GSCC/DPPR DK Processed or  
   GSCC/ASME Memo Status Assigned or  
   GSCC/ASPE Pending Status Assigned or  
   GSCC/RVME Memo Status Removed or  
   GSCC/RVPE Pending Status Removed or  
  :CPRC/ /PACK Cancel Accepted or  
   /REJT Cancel Rejected or  
   /CAND Cancel Processed or  
  :MTCH/ /MACH Trade Matched  
M :16R: REAS  Optional Repeat Block Start  
M :24B: :REJT/  Reject Reason Code (see Appendix 
E) 
4!c 
O :70D: :REAS/ /GSCC Reject Reason Narrative (6*35x) 
   /MDRJ Modify Rejected or 4!c 
   /DKRJ DK Rejected  
M :16S: REAS  Repeat Block End  
M :16S: STAT  Repeat Block End  
M :16S: GENL  Block End  
 
MT509 Message Specification 
This section provides the detailed specification for the MT509 message. RTMM uses these message types 
to notify clients of the status of trades or records submitted. As described in the MT509 Message 
Overview, CMU RTTM sends the MT509 message to the client for the following events: 
• Trade Input Accepted 
• Trade Input Rejected 
• Modify Accepted 
• Modify Rejected 
• Modify Processed 
• Deleted Unmatched Transaction 
• Deleted due to DK 
• Deleted due to Memo 
• Deleted due to Pending 
• Deleted due to Security Detail Differences 
• DK Accepted 
• DK Rejected 
• DK Processed 
• Memo Status Assigned 
• Pending Status Assigned 
• Memo Status Removed 
• Pending Status Removed 
• Cancel Accepted 
• Cancel Rejected 
• Cancel Processed 
• Trade Matched 
  

---

## Page 53

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 53 
MT509 Field Specifications 
Block/ 
Tag 
 Notes 
Message 
Header 
Each message must contain a message header. All header fields are mandatory fixed format with 
trailing blanks, where required. 
Password 12!c Blank filled on MT509 messages. 
Sender 8!c NSCCTRRS ([[NSCC]] Trade Registration and Reconciliation System) will always be the 
sender of the MT509 messages. 
Message 
Type 
3!n/3!n/4!c The first three characters indicate to the recipient the message type (509); the second 
three positions reflect the version of the message interface (currently always 000). The 
last four characters indicate the [[issuer]] code to be used in the message (“GSCC”). 
Receiver 8!c [[participant]] [[ID]] 
GENL This mandatory block provides general information regarding the message. It appears only 
once in a status message. 
20C Sender Message Reference 
SEME// – Mandatory field that contains the sender’s (CMU RTTM) message reference number. It is 
used on all messages sent by CMU RTTM and contains a unique number to unambiguously identify 
each message. (This is a communications message number, not a trade number). 
Note: While the SWIFT message accommodates both uppercase and lowercase alphanumeric and 
certain symbols, this field is populated with an uppercase alphanumeric value for CMU RTTM purposes. 
It does not contain symbols or hyphens. 
Example: :20C::SEME//CMU RTTMCOMREF1 
23G Function of the Message 
This mandatory field is used on all messages to identify the function of the message. It will either be 
the status of an Instruct, Modify, or DK (INST), or regarding the submission of a cancellation of a 
previous message (CAST). 
INST – Used for trade status messages usually referring to instructs, modifies, or DKs. It is also reflected 
on all MT509 reject messages where the MT515 was rejected for not being SWIFT compliant. 
CAST – Used on the various messages referring to cancellations. 
Example: :23G:INST 
98C Preparation Date and Time 
PREP// – Reflected on all messages to indicate the date and time the message was prepared by 
CMU RTTM. 
Note:  The  “C”  format  for  this  (98)  tag  indicates  a  date/time  format  of “YYYYMMDDHHMMSS”. 
For example, :98C::PREP//20150331101510 
LINK The LINK block is repeated for as many reference qualifiers as need to be included in a trade status 
message. Each subsequence contains reference numbers to identify the trade or record for which the 
status is being reported. Each reference number will be enclosed within a Start Link Block 
(:16R:LINK) and End Link Block (:16S:LINK). All LINK repeating subsequences are within the GENL 
Block. 
20C Reference 
As indicated above, each reference number is enclosed in a LINK Start and End block. 
MAST// – Master Reference Number – Contains the client’s reference number for the trade 
(External Reference Number). The MAST qualifier appears on all MT509 messages, except where 
an MT515 message was rejected for not being SWIFT compliant and on MT509 messages referring 
to MT515 DK submitted records. 
PREV// – Previous Reference Number – Used only on records where the External Reference Number 
has been modified by the client and contains the client’s previous reference number. 
RELA// – MT515 Sender’s Message Reference Number – Contains the Sender’s Message Reference 
Number (20C::SEME//) from the MT515 submitted by the client. It only appears on those MT509 
messages that are acknowledgements of receipt or rejections of MT515 client messages. This is the 
only 20C qualifier in the LINK block where an MT509 Reject message is being created for a non-
SWIFT compliant MT515. 
LIST// – CMU RTTM Assigned Reference Number – Contains CMU RTTM’s assigned reference 
number (TID). 
PROG// – Contraparty X-Ref  – Reflects the Contraparty External Reference Number. It only 
appears on MT509 messages related to matching notification, such as Trade Matched 
(:25D::MTCH//MACH) and on MT509 messages providing the status of MT515 DK records submitted 
to CMU RTTM. 

---

## Page 54

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 54 
Block/ 
Tag 
 Notes 
COMM// – Match Control Number – Contains the Match Control Number assigned by CMU RTTM upon 
matching. It is included on the MT509 post-match messages: 
MTCH//MACH – Trade Matched 
IPRC/GSCC/MODA – Modify Accepted (for modifies of X- ref, regulatory data, or both, submitted post-
matching. 
IPRC/GSCC/MDRJ – Modify Rejected (for rejects of modifies of X-ref, regulatory data, or both, 
submitted post- matching. 
IPRC/GSCC/MODP – Modify Processed (for modifies of X- ref, regulatory data, or both, submitted post-
matching. 
Note: While the SWIFT message accommodates both uppercase and lowercase alphanumeric and 
certain symbols, this field is populated with an uppercase alphanumeric value for CMU RTTM purposes. 
It does not contain symbols or hyphens, except where CMU RTTM assigns the reference number. 
Example: :20C::MAST//PARTREF1 
STATUS  The Status block appears on every MT509 message and notifies the client of the type of MT509 
record being sent and the status of the trade or record that was submitted to CMU RTTM. 
25D Status Code  
The status code indicates the record type or type of status message being sent by CMU RTTM. The 
following message types are used for interactive messaging to support real-time matching: 
IPRC//PACK – Indicates that an instruction message has been accepted by CMU RTTM. 
IPRC//REJT – Indicates that CMU RTTM has rejected the instruct, modify, or DK message. Where 
this is used to indicate that a modify or DK record has been rejected, field 70D in the REAS block 
populates with one of the following: 
• :70D::REAS//GSCC/MDRJ 
• :70D::REAS//GSCC/DKRJ 
The IPRC//REJT qualifier is used in all instances where an incoming MT515 is rejected for not being 
SWIFT compliant (:24B::REJT/GSCC/F999). 
IPRC/GSCC/MODA – Indicates to the submitter that a trade modification record has been accepted. 
IPRC/GSCC/MODP – Indicates to the submitter that the trade modification requested has been 
processed. 
IPRC/GSCC/DELE – Indicates to the submitter that a trade that was pending matching has been 
deleted. 
IPRC/GSCC/DEDK – Indicates that a trade previously submitted to CMU RTTM has been deleted due to 
DK. 
IPRC/GSCC/DEME – Indicates that a trade previously submitted to CMU RTTM and assigned a Memo 
status has been deleted. 
IPRC/GSCC/DEPE – Indicates that a trade previously submitted to CMU RTTM and assigned a Pending 
status has been deleted. 
IPRC/GSCC/DESD – Indicates that a trade previously submitted to CMU RTTM has been deleted due to 
security detail differences. 
IPRC/GSCC/PADK – Indicates to the submitter that a DK record has been accepted and is waiting for 
further processing. 
IPRC/GSCC/DPPR – Indicates to the submitter that a DK record accepted by the system has been 
processed. 
IPRC/GSCC/ASME – Indicates to the submitter that a trade submitted to CMU RTTM has been 
assigned a Memo status and is unavailable for matching. 
IPRC/GSCC/ASPE – Indicates to the submitter that a trade submitted to CMU RTTM has been 
assigned a Pending status and is unavailable for matching. 
IPRC/GSCC/RVME – Indicates to the submitter that a trade previously assigned a Memo status by 
CMU RTTM has had the Memo status removed. The trade is now available for matching. 
IPRC/GSCC/RVPE – Indicates to the submitter that a trade previously assigned a Pending status by 
CMU RTTM has had the Pending status removed. The trade is now available for matching. 
CPRC//PACK – Indicates to the submitter that a cancel record has been accepted by CMU RTTM. 
CPRC//REJT – Indicates to the submitter that a cancel record submitted to CMU RTTM has been 
rejected. 
CPRC//CAND – Indicates that a Cancel instruction has been processed (trade instruction has been 
canceled). 
MTCH//MACH – Indicates to the parties on a trade that a trade has matched. 
Example: :25D::IPRC//PACK 

---

## Page 55

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 55 
Block/ 
Tag 
 Notes 
REASON The Reason block appears only on MT509 messages where an MT515 (instruct, modify, cancel, 
or DK) submitted by the client has been rejected by CMU RTTM. Each reason code must be 
enclosed within a Start Reason (:16R:REAS) and End Reason (:16S:REAS) block. 
24B Reason Code 
This field is mandatory in the block and appears on all Reject messages. There can be multiple reason 
codes on any MT509 Reject message; each Reason Code must be enclosed within a Start Reason 
(:16R:REAS) and End Reason (:16S:REAS) block. The Reason Code populates with the following value: 
REJT/ – Reflected on all messages to indicate to the client that RTMM rejected the submitted MT515. 
Note: For a list of all error conditions (and associated codes) that would result in the rejection of a 
client MT515 message, see Appendix E. 
Example: :24B::REJT/GSCC/E201 
70D Reason Narrative (REAS) 
REAS//GSCC – The reason narrative field can contain narrative on those MT509 reject messages 
created in response to receiving a non-SWIFT compliant MT515, or can contain one of the following 
qualifiers: 
/MDRJ – Included on an MT509 Instruct Reject message when CMU RTTM rejects a trade modification 
MT515. 
/DKRJ – Included on an MT509 Instruct Reject message when CMU RTTM rejects a submitted MT515 
DK. 
Note: This narrative field appears in the first repeating REAS sequence. 
Example: :70D::REAS//GSCC/MDRJ 
 

---

## Page 56

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 56 
MT509 Field Analysis 
The following tables show the MT509 Field Analysis layouts: 
• Table 1 (PACK, REJT, MODA, MODP, DELE, DEDK, DEME, DEPE, DESD) 
• Table 2 (PADK, DKRJ, DPPR, ASME, ASPE, RVME, RVPE) 
• Table 3 (CPRC//PACK, CRPC//REJT, CRPC//CAND and MTCH) 
Table 1 (PACK, REJT, MODA, MODP, DELE, DEDK, DEME, DEPE, DESD) 
SWIFT MT509 Layout MT509 Records 
M/O Tag Block/ 
Qualifier 
Subqualifi
er 
Field Description IPRC 
PACK 
IPRC 
REJT 
IPRC 
GSCC 
MODA 
IPRC 
GSCC 
MDRJ 
IPRC 
GSCC 
MODP 
IPRC 
GSCC 
DELE 
IPRC 
GSCC 
DEDK 
IPRC 
GSCC 
DEME 
IPRC 
GSCC 
DEPE 
IPRC 
GSCC 
DESD 
    Message Header           
    Password           
    Sender           
    Message Type           
    Receiver           
M :16R: GENL  Block Start           
M :20C: :SEME//  Sender’s Reference 
for this Message 
          
M :23G: INST  Message Function- 
Instruct or 
          
  CAST  Cancel           
O* :98C: :PREP//  Preparation 
Date/Time 
          
M :16R: LINK  Repeat Block Start           
M :20C: :MAST//  [[participant]] 
Reference No. 
          
M :16S: LINK  Repeat Block End           
M :16R: LINK  Repeat Block Start           
O :20C: :PREV//  Previous Reference 
No. 
          
M :16S: LINK  Repeat Block End           
M :16R: LINK  Repeat Block Start           

---

## Page 57

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 57 
SWIFT MT509 Layout MT509 Records 
M/O Tag Block/ 
Qualifier 
Subqualifi
er 
Field Description IPRC 
PACK 
IPRC 
REJT 
IPRC 
GSCC 
MODA 
IPRC 
GSCC 
MDRJ 
IPRC 
GSCC 
MODP 
IPRC 
GSCC 
DELE 
IPRC 
GSCC 
DEDK 
IPRC 
GSCC 
DEME 
IPRC 
GSCC 
DEPE 
IPRC 
GSCC 
DESD 
O :20C: :RELA//  Related Reference 
No. (MT515 Sender’s 
Reference) 
          
M :16S: LINK  Repeat Block End           
M :16R: LINK  Repeat Block Start           
O :20C: :LIST//  CMU RTTM Assigned 
Reference Number 
(TID) 
          
M :16S: LINK  Repeat Block End           
M :16R: LINK  Repeat Block Start           
O :20C: :PROG//  Contraparty 
Reference No. 
          
M :16S: LINK  Repeat Block End           
M :16R: LINK  Repeat Block Start           
M :16S: LINK  Repeat Block End           
M :16R: LINK  Repeat Block Start           
O :20C: :COMM//  Match Control 
Number 
          
M :16S: LINK  Repeat Block End           
M :16R: STAT  Repeat Block Start           
M :25D: :IPRC/ /PACK Trade Accepted/ 
Validated 
          
   /REJT Trade Rejected or           
   GSCC/MO
DA 
Modify Accepted or           
   GSCC/MO
DP 
Modify Processed or           
   GSCC/DE
LE 
Deleted Unmatched 
Transaction or 
          
   GSCC/DEDK Trade Deleted 
due to DK 
or 
          
   GSCC/DEME Deleted due to 
Memo or 
          
   GSCC/DEPE Deleted due to 
Pending or 
          

---

## Page 58

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 58 
SWIFT MT509 Layout MT509 Records 
M/O Tag Block/ 
Qualifier 
Subqualifi
er 
Field Description IPRC 
PACK 
IPRC 
REJT 
IPRC 
GSCC 
MODA 
IPRC 
GSCC 
MDRJ 
IPRC 
GSCC 
MODP 
IPRC 
GSCC 
DELE 
IPRC 
GSCC 
DEDK 
IPRC 
GSCC 
DEME 
IPRC 
GSCC 
DEPE 
IPRC 
GSCC 
DESD 
   GSCC/DESD Deleted due to 
Security Detail 
Differences or 
          
   GSCC/PADK DK Accepted or           
   GSCC/DPPR DK Processed or           
   GSCC/ASME Memo Status 
Assigned or 
          
   GSCC/ASPE Pending Status 
Assigned 
or 
          
   GSCC/RVME Memo Status 
Removed or 
          
   GSCC/RVPE Pending Status 
Removed 
          
  :CPRC/ /PACK Cancel Accepted 
or 
          
   /REJT Cancel Rejected 
or 
          
   /CAND Cancel Processed           
  :MTCH/ /MACH Trade Matched           
M :16R: REAS  Optional Repeat 
Block Start 
          
M :24B: :REJT/  Reject Reason 
Code (see 
Appendix E) 
          
O :70D: :REAS/ /GSCC Reject Reason 
Narrative 
          
   /MDRJ Modify Rejected           
   /DKRJ DK Rejected           
M :16S: REAS  Repeat Block 
End 
          
M :16S: STAT  Repeat Block 
End 
          
M :16S: GENL  Block End           
 

---

## Page 59

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 59 
  

---

## Page 60

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 60 
Table 2 (PADK, DKRJ, DPPR, ASME, ASPE, RVME, RVPE) 
SWIFT MT509 Layout MT509 Records 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description IPRC 
GSCC 
PADK 
IPRC 
GSCC 
DKRJ 
IPRC 
GSCC 
DPPR 
IPRC 
GSCC 
ASME 
IPRC 
GSCC 
ASPE 
IPRC 
GSCC 
RVME 
IPRC 
GSCC 
RVPE 
    Message Header        
    Password        
    Sender        
    Message Type        
    Receiver        
M :16R: GENL  Block Start        
M :20C: :SEME//  Sender’s Reference for 
this Message 
       
M :23G: INST  Message Function- 
Instruct or 
       
  CAST  Cancel        
O* 
:98C: :PREP//  Preparation Date/Time        
M :16R: LINK  Repeat Block Start        
M :20C: :MAST//  [[participant]] Reference No.        
M :16S: LINK  Repeat Block End        
M :16R: LINK  Repeat Block Start        
O :20C: :PREV//  Previous Reference No.        
M :16S: LINK  Repeat Block End        
M :16R: LINK  Repeat Block Start        
O :20C: :RELA//  Related Reference No. 
(MT515 Sender’s 
Reference) 
       
M :16S: LINK  Repeat Block End        
M :16R: LINK  Repeat Block Start        
O :20C: :LIST//  CMU RTTM Assigned 
Reference Number (TID) 
       
M :16S: LINK  Repeat Block End        
M :16R: LINK  Repeat Block Start        
O :20C: :PROG//  Contraparty Reference 
No. 
       
M :16S: LINK  Repeat Block End        
273 :16R: LINK  Repeat Block Start        
O :20C: :COMM//  Match Control Number        
M :16S: LINK  Repeat Block End        

---

## Page 61

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 61 
SWIFT MT509 Layout MT509 Records 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description IPRC 
GSCC 
PADK 
IPRC 
GSCC 
DKRJ 
IPRC 
GSCC 
DPPR 
IPRC 
GSCC 
ASME 
IPRC 
GSCC 
ASPE 
IPRC 
GSCC 
RVME 
IPRC 
GSCC 
RVPE 
M :16R: STAT  Repeat Block Start        
M :25D: :IPRC/ /PACK Trade Accepted/ Validated 
or 
       
   /REJT Trade Rejected or        
   GSCC/MODA Modify Accepted or        
   GSCC/MODP Modify Processed or        
   GSCC/DELE Deleted Unmatched 
Transaction or 
       
   GSCC/DEDK Trade Deleted due to DK 
or 
       
   GSCC/DEME Deleted due to Memo or        
   GSCC/DEPE Deleted due to Pending or        
   GSCC/DESD Deleted due to Security 
Detail Differences or 
       
   GSCC/PADK DK Accepted or        
   GSCC/DPPR DK Processed or        
   GSCC/ASME Memo Status Assigned or        
   GSCC/ASPE Pending Status Assigned 
or 
       
   GSCC/RVME Memo Status Removed or        
   GSCC/RVPE Pending Status Removed 
or 
       
  :CPRC/ /PACK Cancel Accepted or        
   /REJT Cancel Rejected or        
   /CAND Cancel Processed or        
  :MTCH/ /MACH Trade Matched        
M :16R: REAS  Optional Repeat Block 
Start 
       
M :24B: :REJT/  Reject Reason Code (see 
Appendix E) 
       
O :70D: :REAS/ /GSCC Reject Reason Narrative        
   /MDRJ Modify Rejected        
   /DKRJ DK Rejected        
M :16S: REAS  Repeat Block End        

---

## Page 62

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 62 
SWIFT MT509 Layout MT509 Records 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description IPRC 
GSCC 
PADK 
IPRC 
GSCC 
DKRJ 
IPRC 
GSCC 
DPPR 
IPRC 
GSCC 
ASME 
IPRC 
GSCC 
ASPE 
IPRC 
GSCC 
RVME 
IPRC 
GSCC 
RVPE 
M :16S: STAT  Repeat Block End        
M :16S: GENL  Block End        
  

---

## Page 63

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 63 
Table 3 (CPRC//PACK, CRPC//REJT, CRPC//CAND and MTCH) 
SWIFT MT509 Layout MT509 Records 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CPRC//PACK CPRC// 
REJT 
CPRC// 
CAND 
MTCH// 
    Message Header     
    Password     
    Sender     
    Message Type     
    Receiver     
M :16R: GENL  Block Start     
M :20C: :SEME//  Sender’s Reference for this Message     
M :23G: INST  Message Function – Instruct or     
  CAST  Cancel     
O* :98C: :PREP//  Preparation Date/Time     
M :16R: LINK  Repeat Block Start     
M :20C: :MAST//  [[participant]] Reference No.     
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :PREV//  Previous Reference No.     
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :RELA//  Related Reference No. (MT515 
Sender’s Ref.) 
    
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :LIST//  CMU RTTM Assigned Reference 
Number (TID) 
    
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :PROG//  Contraparty Reference No.     
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
M :16S: LINK  Repeat Block End     
M :16R: LINK  Repeat Block Start     
O :20C: :COMM  Match Control Number     
M :16S: LINK  Repeat Block End     
M :16R: STAT  Repeat Block Start     

---

## Page 64

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 64 
SWIFT MT509 Layout MT509 Records 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CPRC//PACK CPRC// 
REJT 
CPRC// 
CAND 
MTCH// 
M :25D: :IPRC/ /PACK Trade Accepted/ Validated or     
   /REJT Trade Rejected or     
   GSCC/MODA Modify Accepted or     
   GSCC/MODP Modify Processed or     
   GSCC/DELE Deleted Unmatched Transaction or     
   GSCC/DEDK Trade Deleted due to DK or     
   GSCC/DEME Deleted due to Memo or     
   GSCC/DEPE Deleted due to Pending or     
   GSCC/DESD Deleted due to Security Detail 
Differences or 
    
   GSCC/PADK DK Accepted or     
   GSCC/DPPR DK Processed or     
   GSCC/ASME Memo Status Assigned or     
   GSCC/ASPE Pending Status Assigned or     
   GSCC/RVME Memo Status Removed or     
   GSCC/RVPE Pending Status Removed or     
  :CPRC/ /PACK Cancel Accepted or     
   /REJT Cancel Rejected or     
   /CAND Cancel Processed or     
  :MTCH/ /MACH Trade Matched     
M :16R: REAS  Optional Repeat Block Start     
M :24B: :REJT/  Reject Reason Code (see Appendix E)     
O :70D: :REAS/ /GSCC Reject Reason Narrative     
   /MDRJ Modify Rejected or     
   /DKRJ DK Rejected     
M :16S: REAS  Repeat Block End     
M :16S: STAT  Repeat Block End     
M :16S: GENL  Block End     

---

## Page 65

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 65 
MT518 Message 
The SWIFT MT518 message is specified as a Market Side [[securities]] Trade Confirmation. It is used to convey 
full trade information to the transaction contraparty associated with Instruct, Cancel, and Modify messages 
submitted against it. This message is also used to provide information to clients where CMU RTTM or the 
contraparty has taken action regarding your trade, such as re-pricing, [[default]] values applied, DK and DK 
removal. As in the MT515, field :22F::PROC in the Confirmation Details (CONFDET) block indicates to the 
client the record type being sent. Additionally, field :70E:: TPRO// can indicate the reason for the event 
occurring, preceded by the mnemonic MSGR (message reason). On DK messages, this narrative field also 
provides the reason for the DK having been submitted against the recipient’s trade (preceded by the mnemonic 
DKRS (DK reason). SWIFT MT518 Messages include the following types: 
 Message Usage 
1 Match Request 
(:22F::PROC/GSCC/CMPR) 
Used to inform a [[Member]] that an Instruct Message has been 
submitted to CMU RTTM against it. 
To effect bilateral matching, the [[Member]] must submit 
corresponding trade data to CMU RTTM for matching, if it has 
not already done so. (Where the record is marked as Locked-in 
or Demand, the client can allow the trade to match administratively 
without submitting a corresponding matching trade.) 
2 Match Request Modify 
(:22F::PROC/GSCC/CRQM) 
Used to inform a [[Member]] that a Modify Message has been 
submitted by its contraparty for a trade that is Pending matching. 
To effect bilateral matching, the [[Member]] must submit 
corresponding trade data to CMU RTTM for matching, if it has 
not already done so. (Where the record is marked as Locked-in 
or Demand, the client can allow the trade to match administratively 
without submitting a corresponding matching trade.) 
3 Match Request Cancel 
(:22F::PROC/GSCC/CADV) 
Used to inform a [[Member]] that its contraparty or CMU RTTM has 
canceled an advice for trade that has not yet or has just matched. 
The request for matching has been canceled. The [[Member]] does 
not need to take any action within CMU RTTM. 
4 Post Match Contra Trade 
Modification 
(:22F::PROC/GSCC/CMDA) 
Used to provide full trade details for the modifications the 
contraparty has made to its (already matched) trade record (that 
does not change the details of the client’s trade). This message is 
only sent when a contraparty has modified the X-ref of an already 
matched trade. It reflects both the previous and the new external 
reference number for a contraparty trade record that previously 
matched against a client's trade. 
5 Locked-in Trade Advice 
(:22F::PROC/GSCC/LCTA) 
Used to inform a [[Member]] that a trade has been booked on the 
client’s behalf based on submitting either a locked-in or demand 
trade against that client. This message is only generated by CMU 
RTTM where a locked-in or demand trade is still available for 
matching, as part of administrative matching. 
Note: Only limited regulatory fields are populated on this 
message. 
6 Trade Matched with Modifications 
(:22F::PROC/GSCC/CMPM) 
Used to reflect new trade details based on changes CMU RTTM 
may have made to a client's trade during the matching process. 
Changes include change of trade date, final money, and target 
trade indicator. The earlier of the two trade dates is applied where a 
difference exists for any bilateral trades. The locked-in or demand 
submitter’s information continues to prevail, as does the [[Seller]]’s 
money on a bilateral trade. 
7 (Notification of) [[default]] Values 
Applied (:22F::PROC/GSCC/DFVA) 
Used to provide full trade details back to the client where CMU 
RTTM has completed trade records upon receipt/acceptance to 
the system. This message is applicable to When Issue trades 
where the client has not provided final money and [[settlement]] 
date and where CMU RTTM can calculate the trade and/or 

---

## Page 66

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 66 
 Message Usage 
assign a [[settlement]] date. In addition, CMU RTTM will provide this 
message when CMU has assigned the trade to be for 
Comparison Only because the trade does not meet the rules for 
[[settlement]] at [[DTCC]]. 
8 Screen Input Trade Replay 
(:22F::PROC/GSCC/SITR) 
Used to provide full trade details to the client where a trade has 
been added, modified, or canceled through screen input, rather 
than an automated interface. Using this message, a client can 
ensure that the same transaction events exist within its application. 
Note: This record contains all regulatory fields entered to CMU 
RTTM by the client. 
9 DK Advice 
(:22F::PROC/GSCC/NAFI) 
Used to inform a [[Member]] that its contraparty has submitted a DK 
against the recipient’s previously submitted trade. The message 
also contains the contra’s reason for submitting the DK. If a 
demand or bilateral trade remains with a DK status, at the end 
of the day, CMU RTTM administratively cancels the trade from the 
system. 
10 DK Remove Advice 
(:22F::PROC/GSCC/DCCX) 
Used to inform a [[Member]] that its contraparty has removed the DK 
it previously submitted against the recipient’s trade. The [[Member]] 
does not need to take any action. The trade is pending matching. 
11 Repricing - Yield to Price 
(:22F::PROC/GSCC/YTPR) 
Used to inform all parties to a new issue trade of the recalculated 
final money, accrued interest, and [[settlement]] date. 
12 [[settlement]] Disposition 
(:22F::PROC/GSCC/STLD) 
Used to inform a [[Member]] that a [[settlement]] disposition has been 
assigned to the trade and that it has been sent to [[settlement]]. 
The message indicates the method of [[settlement]] ([[CNS]]®, non-[[CNS]], 
trade-for-trade) and anticipated delivery (actual [[settlement]]) date, or 
that a trade has been assigned a comparison-only status. 
 
As with MT509 events, MT518 messages are sent to the client and/or its contraparty where a change 
has been made in the CMU RTTM system. Changes to regulatory fields made by a client are not reported 
to the contraparty on advisories except for the following fields, which appear only on advisories prior to 
match: Time of Trade, [[Buyer]] and [[Seller]] Capacity and Regulatory Dollar Price. However, where records are 
submitted only for regulatory reporting, CMU RTTM does not generate any MT518 messages for the 
submitter or contraparty. 
MT518 Message Specification 
This section contains the detailed specification for the MT518 message. The SWIFT layout for MT518 
is almost identical to that of the MT515 message used by clients to submit instructions to CMU RTTM. 
Various types of MT518 messages described previously in this document can be divided into the following 
three categories of messages: 
• Advisories 
• Locked-in trade advices 
• Advices referring to modifications and events based on your trades 
As with the MT515 messages, all MT518 record types can apply to both trades and reversals. 
  

---

## Page 67

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 67 
Advisories 
Advisories sent to a client reflect the trade record as submitted by the contraparty. The Buy/Sell indicator 
(transaction type) on the record is from the perspective of the recipient of the MT518. 
The following MT518 record types are advisories: 
• Match Request – CMPR 
• Match Request Modify – CRQM 
• Match Request Cancel – CADV 
• Post-Match Contra Trade Modification – CMDA 
Locked-in Trade Advices 
Locked-in Trade Advice MT518 messages are intended to notify a recipient that a trade was booked on CMU 
RTTM on behalf of the client and submitted by an authorized locked-in or demand submitter. 
The following MT518 is the only locked-in advice used by CMU RTTM: 
• Locked-in trade advice – LCTA 
Advices Referring to Modifications/Events Based on Your Trades 
These MT518 messages primarily reflect your trade records after changes have been made. In most 
cases, the changes have been made by CMU RTTM to your trade. The following MT518 messages 
reflect modifications or events based on your trade: 
• Trade matched with modifications – CMPM 
• [[default]] values applied – DFVA 
• Screen input trade replay – SITR 
• DK advice – NAFI 
• DK remove advice – DCCX 
• Repricing - yield to price – YTPR 
• [[settlement]] disposition – STLD 
Throughout this section, data fields that support regulatory reporting requirements are marked with the 
regulatory field label. For more information about these fields, see MSRB Specifications for Real - Time 
Reporting of Municipal [[securities]] Transactions. 
  

---

## Page 68

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 68 
MT518 General Format 
The following table shows the MT518 general format details: 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
    Message Header  
M    Password 12!c 
M    Sender 8!c 
M    Message Type 3!n/3!n/4!c 
M    Receiver 8!c 
M :16R: GENL  Mandatory Block Start  
M :20C: :SEME//  Sender’s Reference for this Msg 16x 
M :23G: NEWM  Message Function = New or 4!c 
  CANC  Cancel  
O* :98C: :PREP//  Preparation Date/Time YYYYMMDDHHMMSS 
M :22F: :TRTR/ GSCC/CASH Bilateral Trade Indicator or 4!c 
   GSCC/TRLK Locked-in Trade Indicator or  
   GSCC/TRDC Demand Trade Indicator  
M :16R: LINK  Optional Repeat Block Start  
O :20C: :MAST//  Master Reference Number 
(External Reference) 
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :PREV//  Previous Reference Number 
(Previous External Reference) 
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :LIST//  CMU RTTM Assigned Reference 
(TID) 
16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :TRRF//  Regulator Control Number 16x 
M :16S: LINK  Repeat Block End  
M :16R: LINK  Repeat Block Start  
O :20C: :COMM//  Match Control Number 16x 
M :16S: LINK  Repeat Block End  
M :16S: GENL  Block End  
M :16R: CONFDET  Mandatory Block Start  
M :98C: :TRAD//  Trade Date & Time YYYYMMDDHHMMSS 
M :98A: :SETT//  [[settlement]] Date or YYYYMMDD 
M :98B: :SETT// WISS [[settlement]] to be completed when 
the security is issued. 
4!c 
M :90A: :DEAL/ /PRCT/ Deal Price – Percentage or 15d 
   /YIEL/ Yield  
O* :94B: :TRAD/ GSCC/OTCP Place of Execution Over-the-
Counter Corporate 
or 
4!c 
   GSCC/OTMU [[Over-The-Counter]] Municipal or  
   GSCC/ OTUI [[Over-The-Counter]] Unit Investment 
Trust 
 
O :19A: :SETT/ /USD [[settlement]] Amount 15d 
M :22H: :BUSE/ /BUYI Trade Type – Buy or 4!c 

---

## Page 69

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 69 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
   /SELL Sell  
O :22F: :PRIC/ GSCC/WGTP Type of Price – Weighted Price 4!c 
O* :22F: :PROC/ GSCC/CMPR Match Request or 4!c 
   GSCC/CRQM Match Request Modify or  
   GSCC/CADV Match Request Cancel or  
   GSCC/CMDA Post Match Contra Trade 
Modification or 
 
   GSCC/LCTA Locked-in Trade Advice or  
   GSCC/CMPM Trade Matched with Modifications 
or 
 
   GSCC/DFVA Notification of [[default]] Values 
Applied or 
 
   GSCC/SITR Screen Input Trade Replay or  
   GSCC/NAFI Trade DK Advice or  
   GSCC/DCCX DK Remove Advice or  
   GSCC/YTPR Repricing -Yield to Price or  
   GSCC/STLD [[settlement]] Disposition  
O :22F: :TTCO/ GSCC/TSQS Trade Type/Target Indicator 
– QSR Trade or 
4!c 
   GSCC/TTQS Target QSR Trade  
M :22H: :PAYM/ /APMT Against Payment Indicator 4!c 
M :16R: CONFPRTY  Mandatory Repeat Block Start  
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]] 34x 
O :20C: :PROC//  [[Buyer]] (Contra) Xref 16x 
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative 4*35x 
   /TDID [[Buyer]] (Contra) Trader [[ID]] 20c 
 
O 
:70E: :DECL/ /GSCC Narrative/ Additional Reference 
Numbers/ Information 
(10*35x) 
   /PREV [[Buyer]] (Contra) Previous Xref 16x 
   /CORR Party = MPID of [[Buyer]]’s 
Correspondent firm 
4c 
O :22F: :TRCA/ /AGEN Capacity Indicator – Acting as 
Agent Indicator or 
4!a 
   /PRIN Acting as Principal Indicator 4!a 
M :16S: CONFPRTY  Repeat Block End  
M :16R: CONFPRTY  Mandatory Repeat Block Start  
M :95R: :SELL/ GSCC/PART Party = [[Seller]] 34x 
O :20C: :PROC//  [[Seller]] (Contra) Xref 16x 
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative 4*35x 
   /TDID [[Seller]] (Contra) Trader [[ID]] 20c 
 
O 
:70E: :DECL/ /GSCC Narrative/ Additional Reference 
Numbers/ Information 
(10*35x) 
   /PREV [[Seller]] (Contra) Previous Xref 16x 
   /CORR Party = MPID of [[Seller]]’s 
Correspondent Firm 
4c 
O :22F: :TRCA/ /AGEN Capacity Indicator – Acting as 
Agent Indicator or 
4!a 
   /PRIN Acting as Principal Indicator  
M :16S: CONFPRTY  Repeat Block End  
M :36B: :CONF/ /FAMT/ Quantity as Face Amount (Par) or 15d 
   /UNIT/ Quantity as Units / [[shares]] 15d 

---

## Page 70

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 70 
M/
O 
Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
M :35B: /US/  Security Identifier – [[CUSIP]] 4 * 35x 
O :70E: :TPRO/ /GSCC Trade Instruction Processing 
Narrative 
10*35x 
   /MSGR Message Reason (see Appendix 
E) 
4!c 
   /DKRS DK Reason (see Appendix E) 4!c 
   /DEST Destination Indicator (see 
Appendix E) 
2!c 
   /ITYP Issue Type (see Appendix E) 2!c 
   /SDAD [[settlement]] Date Adjustment 4n 
   /RVSL Trade Reversal Indicator 4!c 
   /SPXR MSRB Special Condition 
Indicators 
4!c 
   /RCTL Reversal Control Number 16x 
   /YIEL Yield [N]15d 
   /SDSP [[settlement]] Disposition (see 
Appendix E) 
4!c 
   /DDTE Delivery Date YYYYMMDD 
   /RGDP Regulatory dollar price 13d 
   /MISC Miscellaneous 9d 
M :16S: CONFDET  Block End  
M :16R: SETDET  Optional Block Start  
M :22F: :SETR/ /RPTO [[settlement]] Indicator = Reporting-
Only or 
4!c 
   GSCC/STRD [[settlement]] Type Indicator – 
Special Trade or 
 
   GSCC/CPRO Comparison Only  
M :16R: AMT  Optional Block Start  
M :19A: :SPCN/ /USD Special Concessions or [N]15d 
  :EXEC/ /USD Executing [[Broker]] Commission 15d 
M :16S: AMT  Block End  
M :16R: AMT  Optional Block Start  
M :19A: :ACRU/ /USD Accrued Interest Amount 15d 
M :16S: AMT  Block End  
M :16S: SETDET  Block End  
M :16R: OTHRPRTY  Optional Block Start  
M :95Q: :MEOR//  Originator of message (if other 
than the Sender) 
4!c//6c 
M :16S: OTHRPRTY  Block End  
 
  

---

## Page 71

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 71 
MT518 Field Specifications 
Block/ 
Tag 
Notes 
Message 
Header 
Each message must contain a message header.  All header fields are mandatory fixed format 
with trailing blanks, where required. 
Password 12!c Blank-filled on MT518 messages. 
Sender 8!c NSCCTRRS ([[NSCC]] Trade Registration and Reconciliation System) will be the sender of 
the MT518 messages in this document. 
Message 
Type 
3!n/3!n/4!c The first three characters indicate to the recipient the message type (518); the 
second three positions reflect the version of the message interface (currently always 
000). The last four characters indicate the [[issuer]] code to be used in the message 
(“GSCC”). 
Receiver 8!c [[participant]] [[ID]] 
GENL This mandatory block provides general information regarding the message. It appears only once 
in a trade confirm. 
20C Sender Message Reference 
• SEME// - Mandatory field that contains the sender’s (CMU RTTM) message reference 
number. It is used on all messages and contains a unique number to unambiguously 
identify each message sent by CMU RTTM. (This is a communications message 
number, not a trade number.) 
Note: While the SWIFT message accommodates both uppercase and lowercase alphanumeric and 
certain symbols, this field is populated with an uppercase alphanumeric value for CMU RTTM purposes. It 
does not contain symbols or hyphens. 
Example: :20C::SEME//CMU RTTMCOMREF1 
23G Function of the Message 
This mandatory field is used on all messages to identify the function of the message. It is 
either a new message (NEWM) related to an instruct, modify, or DK or the cancellation of a previous 
trade (CANC). 
• NEWM - Used for the following MT518 messages: 
o Match Requests and Match Request Modifies 
o Screen Input Trade Replays that reflect an instruct or modify submitted through the 
screen 
o DK Advices and DK Remove Advices where the receiver of the advices is the 
submitter of the trade that is being DKed 
o Post Match Contra Trade Modification  and  Trade  Matched   with Modifications 
o Notification of [[default]] Values Applied and Repricing (Yield to Price) 
o [[settlement]] Disposition 
• CANC - Used for the following MT518 messages that reflect a cancel submitted through a 
screen: 
o Match Request Cancels 
o Screen Input Trade Replays 
Example: :23G:NEWM 
98C Preparation Date and Time 
• PREP// - Reflected on all messages to indicate the date and time the message sent by 
CMU RTTM was prepared. 
Note: The C format for this (98) tag indicates a date and time format of 
YYYYMMDDHHMMSS. 
For example, :98C::PREP//20030331112515 
22F Trade Transaction Type Indicator (TRTR) 
This mandatory field specifies whether the trade being reported is bilateral, locked-in, or 
demand. 
• TRTR/GSCC/CASH - Used on trades requiring two-sided (bilateral) matching. All MT518 
messages originating from a bilateral submission have this qualifier. Locked-in trade advices 
created for the demand or locked-in recipient also reflect the CASH qualifier [[Option]]. MT518 
advisories resulting from a demand or locked-in submission does NOT use this qualifier 
[[Option]]. However, they reflect the submission type of the demand or locked-in submitter. 

---

## Page 72

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 72 
Block/ 
Tag 
Notes 
• TRTR/GSCC/TRLK - Used on Locked-in trades. MT518 messages resulting from a QSR 
locked-in submission reflect this qualifier [[Option]], with the exception of locked-in trade advices 
(LCTA)). 
• TRTR/GSCC/TRDC - Used on Demand trades. MT518 messages resulting from a [[syndicate]] 
demand submission reflect this qualifier [[Option]], with the exception of locked-in trade advices 
(LCTA)). 
Example: :22F::TRTR/GSCC/CASH 
LINK Repeat LINK blocks for as many reference qualifiers as need to include in a trade 
contract. It is intended to provide the required information to identify the trade. Each 
reference number must be enclosed within a Start Link Block (:16R:LINK) and End 
Link Block (:16S:LINK). Each LINK repeating subsequence is within the GENL block. 
20C Reference 
This set of fields in the MT518 contains the relevant reference numbers associated with 
your trade. The following types of reference numbers can appear in the LINK block: 
• Master reference number (MAST), generally referred to as the external reference number 
or X-ref 
• Previous reference number for the trade (PREV) 
• CMU RTTM reference number (LIST), also referred to as the TID 
• Regulator Control Number (TRRF) 
• Match Control Number (COMM) 
The data provided in these reference number fields for any given trade are determined based 
upon a number of criteria. These include: 
• Submitter type (bilateral, demand, or locked-in submitter) 
• Message category (advisory, locked-in trade advices, or advices referring to trades 
submitted by the message receiver (“your trades”) 
• Message type, such as Cancel or Modify 
Here are the [[BASIC]] rules for reporting data for each reference number type. 
Note: On MT518 advisories where contraparty trade reference numbers are provided, the 
contraparty’s external and previous reference numbers appear in the appropriate [[Buyer]] or [[Seller]] 
confirming party subsequence, not in this subsequence. 
• MAST// - Master Reference Number – On advices referring to your trades, this field 
contains your external reference number. On Locked-in Trade Advices supporting 
Locked-in or Demand trades, this field will contain the external reference number 
generated by CMU RTTM on your behalf. This field will not appear on advisories. 
• PREV// - Previous Reference Number – Under most circumstances, this field does 
not appear on MT518’s (advisories, locked-in trade advices, or advices referring to your 
trades). 
One exception to this rule is for cancels. There is a SWIFT requirement that the data field associated 
with the PREV qualifier is populated on all MT518 and MT515 Cancel (:23G:CANC) records. 
Therefore, all MT518 cancel records reflect the PREV qualifier populated with the NONREF value. 
The second exception to this rule is for Screen Input Trade Replay Records 
(:22F::PROC/GSCC/SITR) where the client has made entries through the screen. For these trades, the 
data field associated with the PREV qualifier is populated in the following way: 
• If the screen input was a trade cancellation, the data field associated with the PREV qualifier is 
populated with NONREF value. 
• If the screen input was a trade modification, which included the modification of an 
external reference number, the data field associated with the PREV qualifier contains the 
Client’s Previous External Reference Number. 
If the contraparty has changed its external reference number, the contraparty’s previous reference 
number appears in the appropriate [[Buyer]] or [[Seller]] confirming party subsequence, not in this field. 
• LIST// - CMU RTTM Reference Number – On locked-in trade advices, for locked-in 
or demand trades and advices referring to your trades, this field contains the CMU 
RTTM assigned reference number (TID) for the trade. This field does not appear on 
advisories. 
 

---

## Page 73

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 73 
Block/ 
Tag 
Notes 
• TRRF// - Regulator Control Number – regulatory field – This qualifier specifies the control 
number generated by the Regulator application. This field appears on MT518 messages 
referring to your trades where you submitted this reference number to CMU RTTM. 
• COMM// - Match Control Number – This qualifier specifies the match control number 
generated by CMU RTTM for a pair of trades upon matching. It appears on the 
following MT518 messages generated upon or post-matching: 
• PROC/GSCC/CMPM – Trade Matched with Modifications 
• PROC/GSCC/YTPR –Repricing – Yield to Price 
• PROC/GSCC/CMDA – Post Match Contra Trade Modification 
• PROC/GSCC/SITR – Screen Input Trade Replay of a post-match modify 
• PROC/GSCC/STLD – [[settlement]] Disposition 
Note: While the SWIFT message accommodates both uppercase and lowercase alphanumeric and 
certain symbols, this field is populated with an uppercase alphanumeric value for CMU RTTM purposes. 
It does not contain symbols or hyphens, except where CMU RTTM assigns the reference number. 
Example: :20C::MAST//PARTREF1 
CONFDET The CONFDET (Confirmation Details) block appears only once in a trade contract. It 
contains trade and confirming party details. 
98C Trade Date 
TRAD// – Used on all MT518 messages to specify the trade date and time. (The “C” format for this 
(98) tag indicates a date/time format of “YYYYMMDDHHMMSS”). 
Example: :98C::TRAD//20030331121212 
98A 
98B 
[[settlement]] Date 
This mandatory field appears on all MT518 messages.  One of the following values appears: 
• SETT// – Appears on all MT518 messages to specify [[settlement]] date. It appears on all 
regular way trades and new issue final money trades. (The “A” format for this tag (98) indicates 
a date format of YYYYMMDD.) 
• SETT//WISS – This [[Option]] will appear on all MT518 messages of New Issue trades where 
the [[settlement]] date is not known, and final money is not provided. This [[Option]] should never 
appear on [[settlement]] Disposition (STLD) messages. 
 
Example: :98A::SETT//20030331 
98A 
98B 
[[settlement]] Date 
This mandatory field appears on all MT518 messages.  One of the following values 
appears: 
• SETT// – Appears on all MT518 messages to specify [[settlement]] date. It appears on all 
regular way trades and new issue final money trades. (The “A” format for this tag (98) indicates 
a date format of YYYYMMDD.) 
• SETT//WISS – This [[Option]] will appear on all MT518 messages of New Issue trades where 
the [[settlement]] date is not known, and final money is not provided. This [[Option]] should never 
appear on [[settlement]] Disposition (STLD) messages. 
 
Example: :98A::SETT//20030331 
98A 
98B 
[[settlement]] Date 
This mandatory field appears on all MT518 messages.  One of the following values 
appears: 
• SETT// – Appears on all MT518 messages to specify [[settlement]] date. It appears on all 
regular way trades and new issue final money trades. (The “A” format for this tag (98) 
indicates a date format of YYYYMMDD.) 
• SETT//WISS – This [[Option]] will appear on all MT518 messages of New Issue trades where 
the [[settlement]] date is not known, and final money is not provided. This [[Option]] should 
never appear on [[settlement]] Disposition (STLD) messages. 
Example, :98A::SETT//20030331 
90A Deal Price 
This mandatory field will be reflected on all MT518 messages. It contains the Execution Price Type 
and Price. Only one Tag 90A is allowed per trade contract. The following price types may be specified: 

---

## Page 74

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 74 
Block/ 
Tag 
Notes 
• DEAL//PRCT/ – Used for dollar prices. Where a trade is executed on price, and no final 
money is provided in the [[settlement]] Amount field (:19A::SETT//), the dollar price will be 
reflected. Final Money trades, i.e., trades where a [[settlement]] amount is entered, will 
reflect a value of zero “0,” in this field. 
• DEAL//YIEL/ – Used for trades executed on yield, where no final money is reflected on 
the record. 
Note: While the SWIFT format accommodates 15d characters (with decimal), the MT518 messages will 
reflect the maximum allowed on input, i.e., 13d for DEAL/PRCT and 8d for DEAL//YIEL. 
Example: :90A::DEAL//YIEL/4,5 
94B Place of Trade – Market of Execution (TRAD) 
This field is used to specify the Market of Execution for the trade. One of the following entries will 
be reflected on all MT518 messages: 
• TRAD/GSCC/OTCP – Over– the– Counter Corporate 
• TRAD/GSCC/OTMU – Over– the– Counter Municipal 
• TRAD/GSCC/OTUI – Over– the– Counter Unit Investment Trust 
Example: :94B::TRAD/GSCC/OTMU 
19A [[settlement]] Amount 
• SETT// – This field is used to specify the [[settlement]] Amount for trades. Where a 
[[settlement]] Amount is available, it will be reflected on MT518 messages. 
The amount is in SWIFT Standard format, which is left justified, with commas removed, 
and a comma used in lieu of a decimal. The amount is always preceded by a 3– 
character ISO currency code (“USD” for [[NSCC]] trades). 
Note: The [[settlement]] Amount may not be available for NI trades. The SWIFT format can accommodate 
a value of 15d in this field. The field will reflect the maximum allowed on input, i.e., 13d. 
Example: :19A::SETT//USD2000000, 
22H Trade Type Indicator (BUSE) 
This field is reflected on all messages and has only two allowable values for this qualifier: 
• BUSE//BUYI – Indicates that the record represents a buy. 
BUSE//SELL – Indicates that the record represents a sell. 
Example: :22H::BUSE//SELL 
22F Type of Price – Weighted Price 
• PRIC/GSCC/WTGP – regulatory field – Indicates that the price of the trade was based on the 
weighted average of previous transactions as defined by [[FINRA]]. It will be reflected on MT518 
messages referring to your own trades where provided on trade input. 
Example: :22F::PRIC/GSCC/WTGP 
22F Processing Indicator (PROC) 
This processing indicator enables CMU RTTM to indicate to the client the type of record/ command 
being sent on the MT518 message. 
The allowable values for this field are: 
• PROC/GSCC/CMPR – Indicates that the MT518 record is a Match Request. 
• PROC/GSCC/CRQM – Indicates that the MT518 record is a Match Request Modify. 
• PROC/GSCC/CADV – Indicates that the MT518 record is a Match Request Cancel Advice. 
• PROC/GSCC/CMDA – Indicates that the MT518 record is a Post Match Contra Trade Modification. 
• PROC/GSCC/LCTA – Indicates that the MT518 record is a Locked– in Trade Advice. 
• PROC/GSCC/CMPM – Indicates that the MT518 record is a Matched with Modifications. 
• PROC/GSCC/DFVA – Indicates that the MT518 record is a Notification of [[default]] Values 
Applied. 
• PROC/GSCC/SITR – Indicates that the MT518 record is a Screen Input Trade Replay. 
• PROC/GSCC/NAFI – Indicates that the MT518 record is a DK Advice (DK of the recipient’s 
previously submitted trade). 
• PROC/GSCC/DCCX – Indicates that the MT518 record is a DK Remove Advice (removing 
the DK status from the recipient’s trade). 
• PROC/GSCC/YTPR – Indicates that the MT518 record is a Yield to Price recalculation 
(Repricing). 

---

## Page 75

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 75 
Block/ 
Tag 
Notes 
• PROC/GSCC/STLD – Indicates that the MT518 record is a notification of [[settlement]] 
disposition. This message indicates that a trade has been sent to [[settlement]]. 
Example: :22F::PROC/GSCC/YTPR 
22F Trade Type / Target Indicator (TTCO) 
This indicator field is used to identify QSR trade submissions as well as trades targeting 
QSR trades. Options for this field on MT518 messages are as follows: 
• TTCO/GSCC/TSQS – Indicates that this MT518 is a QSR trade record. This [[Option]] 
appears on the following MT518 messages: 
• Advisories resulting from a QSR submission. 
• Advices to QSRs regarding their submissions. 
Note: Not applicable to Locked-in Trade Advices (LCTA) based on QSR 
submissions. 
• TTCO/GSCC/TTQS – Indicates that the MT518 record is targeting a QSR trade. This 
[[Option]] appears on the following MT518 messages: 
• Advisories resulting from a Target QSR trade submission. 
• Advices referring to your Target QSR trade. 
• Locked-In Trade Advice (LCTA) resulting from an administrative match of a QSR 
submission. 
Note: The Trade Transaction Type Indicator (:22F::TRTR) of TRLK (locked-in) appears in 
conjunction with options TSQS. For TTQS, CASH is reflected in the :22F::TRTR field. 
Example, :22F::TTCO/GSCC/TSQS 
22H Payment Indicator (PAYM) 
This Payment indicator field is mandatory for the MT518 message. All MT518 records reflect the 
following tag/qualifier: 
• PAYM//APMT – Indicates that the trade settles against payment. 
Example, :22H::PAYM//APMT 
36B Quantity of [[securities]] (CONF)3 
This field is reported on all MT518 messages with one of the following options: 
• CONF//FAMT/ – The FAMT [[Option]] indicates the face amount (par) reflected on all 
municipal and corporate bond trades. 
• CONF//UNIT/ – The UNIT [[Option]] indicates quantity in units or [[shares]]. This applies 
only to unit investment trust ([[UIT]]) trades. 
Note: The quantity of the financial instrument is in SWIFT Standard Format, which is left 
justified, with commas removed, and a comma used instead of a decimal. While the 
SWIFT format can accommodate a value of 15d in this field, the [[NSCC]] system can only 
accommodate a maximum field size of 10d. 
Example, :36B::CONF//FAMT/2000000, 
35B Identification of Security 
The security involved is identified in the US by specifying the ISO country identifier (‘/US/’), followed by 
the [[CUSIP]] number. This field appears on all MT518 messages. 
Note:  
While the SWIFT layout accommodates a format of 4 * 35x, a 9!c (alpha numeric) value populates the 
field for [[CUSIP]]. 
Example, :35B:/US/78764HAD6 
70E Trade Instruction Processing Narrative (TPRO)6 
This field is intended to reflect transaction related information unsupported by the MT518 layout. It is 
used on all MT518 DK messages to indicate the reason for the DK. It can also be used on MT518 
messages to indicate the reason for the message/event being reported. A number of other data 
fields are also included to provide additional CMU RTTM information and regulatory fields. For 
 
3 Tags 36B, 35B and 70E::TPRO// in the CONFDET block must be placed on the message following the confirming party subsequences. 

---

## Page 76

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 76 
Block/ 
Tag 
Notes 
information about how regulatory fields are reflected on CMU RTTM MT518 messages, see 
Appendix F. 
• TPRO//GSCC – Denotes narrative trade instruction processing information related to 
CMU RTTM. 
• /MSGR – Advisories and advices regarding your trades can contain a message reason 
to further define an event on the CMU RTTM system. For message reasons, see 
Appendix E. 
• /DKRS – All DK advices contain a DK reason to specify why a message was DKed. For 
a list of DK reason codes, see Appendix E. 
• /DEST – Used to specify the destination of the message as CMU RTTM (01), MSRB (02). 
This is a repeating field allowing multiple entries. The DEST field is reflected on the 
following MT518 records: 
• MT518 Screen Input Trade Replay - The DEST fields are populated based on what 
was entered on the screen by the client. 
• MT518 Locked-in Trade Advice - The DEST fields are populated based on what was 
submitted by the locked-in submitter, indicating where your trade was routed. 
• /ITYP –Issue type used to specify [[syndicate]] (ITYPSY) and target [[syndicate]] (ITYPTS) 
trades. 
o [[syndicate]] (ITYPSY) appears on MT518 advisories resulting from a [[syndicate]] 
submission and advices referring to your [[syndicate]] submissions. 
o Target [[syndicate]] (ITYPTS) appears on MT518 advisories resulting from Target 
[[syndicate]] trade submissions; advices referring to your Target [[syndicate]] trades and 
locked-in trade advices (LCTA) resulting from administrative matches of [[syndicate]] 
submissions. 
• /SDAD – Used to specify the number of extended [[settlement]] days. It appears on all 
MT518 messages were submitted on the original MT515 trade record. 
• /RVSL – Used to indicate that the record is for a reversal. To cancel a trade post-
matching, a reversal trade must be entered to offset a previously submitted trade on 
CMU RTTM. CMU RTTM does not link a reversal to the trade it is reversing and treats 
a reversal as a completely new trade. This indicator appears on all MT518 messages 
pertaining to Reversal trades. 
• /SPXR – regulatory field – This subqualifier (with a reason code) can be used if the trade 
was executed at a price different from the prevailing market price. The MSRB Special 
Condition Indicators referring to your trade appear on MT518 advices. See MSRB 
Special Condition Indicators. 
• /RCTL – regulatory field –Reversal control number that reflects the client X-ref (MAST) or 
the CMU RTTM Assigned Reference (LIST) of the trade being reversed, as submitted 
on the Reversal record. It appears only on MT518 advices referring to your reversal 
trades. 
• /YIEL – regulatory field – This subqualifer representing the yield appears only on MT518 
advices referring to your trades where it was provided on the MT515 record. 
• /SDSP– The [[settlement]] disposition appears on all MT518 [[settlement]] Disposition 
messages. The disposition of the trade is reflected as one of the following: 
o CNSE – [[CNS]] 
o CNSN – Not [[CNS]] 
o CPRO – Comparison only 
o TFTD – Trade-for-trade 
• DDTE – The delivery date appears on all MT518 [[settlement]] Disposition messages 
indicating the anticipated actual [[settlement]] date of the trade. Otherwise, for Comparison-
only trades, it is the contractual [[settlement]] date. 
• /RGDP – regulatory field – This subqualifier is provided on all MT518 MUNI messages. 
The “Regulatory Dollar Price” is in the 13D format with the 0 minimum value and 
does not exceed 9999,99999999. 
• /MISC – regulatory field – For future use. The Miscellaneous will be in the 9D format and 
will not exceed 999999,99. 

---

## Page 77

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 77 
Block/ 
Tag 
Notes 
Note: A string of all applicable subqualifiers (maximum of 35 characters per line) follows the 
TPRO//GSCC qualifier. 
For example, : 70E::TPRO//GSCC/DEST02/SPXRR001/0030A/YIEL3,5/RGDP96,98 
CONFPRTY The Confirming Party block must be repeated for each party to a trade. Each party 
specified must be enclosed within a start party block (:16R:CONFPRTY) and end party 
block (:16S:CONFPRTY). For every MT518 record, there are at least two (one [[Buyer]] 
and one [[Seller]]) Confirming Party sequences. 
95R Party 
This field appears on all MT518 messages. 
• BUYR/GSCC/PART – Specifies the buying party. (The GSCC [[issuer]] code allows the 
specification to reflect the [[NSCC]] client or Contraparty [[participant]] [[ID]], depending on who 
is acting as [[Buyer]] or [[Seller]]). 
• SELL/GSCC/PART – Specifies the selling party. 
Note: While the SWIFT layout supports a format of 35x for this field, CMU RTTM populates with the 
appropriate qualifier and four-character [[participant]] [[ID]] for [[Buyer]] or [[Seller]]. 
For example, :95R::SELL/GSCC/PART9538 
20C Reference 
• PROC// – Processing Reference Number – Reflects the Contraparty External 
Reference in the appropriate [[Buyer]] or [[Seller]] confirming party subsequence. It only 
appears on MT518 Advisory and Locked-in Trade Advice records. 
For example, :20C::PROC//CONTRAREF2 
70C [[participant]] Contact Narrative (PACO) 
This field is used in the appropriate [[Buyer]] or [[Seller]] confirming party sequence on MT518 messages to 
provide information regarding the individual/desk that executed the trade. 
• PACO//GSCC – Denotes client contact narrative information specific to CMU RTTM. 
• /TDID – Used in the appropriate [[Buyer]] or [[Seller]] sequence to indicate the following: 
o On MT518s sent to the trade submitter, this represents the contraparty’s trader [[ID]]. 
o On MT518 advisories, this represents the recipient’s trader [[ID]]. 
For example, :70C::PACO//GSCC/TDIDFRED1 
70E Narrative (DECL) 
This field is used in each MT518 subsequence to identify the contraparty’s previous reference number 
(where the contra has changed their external reference number), the executing firm of the [[Buyer]], 
[[Seller]], or both, where applicable. 
• DECL//GSCC – Denotes declaration narrative information specific to CMU RTTM. 
• /PREV – Used in the BUYR or SELL confirming party sequence to indicate the 
Previous Contra External Reference Number on a Trade Modification Advisory 
(Match Request Modify or Post Match Contra Modification Advice). Where this field is 
populated, this communicates to the recipient of the MT518 that the contra’s X-ref has 
changed. The recipient should use this reference number to [[Locate]] the original 
advisory/trade that has changed. Where this field is populated, the current X-ref is 
always in the field described above (:20C::PROC). 
• /CORR – Used in the BUYR, SELL, or both confirming party sequences to indicate the 
executing (correspondent) firms of the [[Buyer]], [[Seller]], or both. This field appears on all 
MT518 messages, where submitted. 
Notes:  
• If none of the above options are populated on input for either the [[Buyer]] or [[Seller]] confirming party, 
this field will not appear on the MT518 record. 
• Effective April 2016, /CORR is required by CMU RTTM for trade acceptance. 
For example, :70E::DECL//GSCC/PREVCONTRAREF1/CORRATGN 
22F Trading Capacity (TRCA) 
This field is used to identify the dealer’s, contraparty’s, or both dealer’s and contraparty’s trading 
capacity as principal or agent. For information about where this field is reflected on the MT518 
messages, see Appendix F. Valid options for this field are: 

---

## Page 78

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 78 
Block/ 
Tag 
Notes 
• TRCA//AGEN – Denotes that the party, contraparty, or both act as the agent for a 
customer. 
• TRCA//PRIN – Denotes that the party, contraparty, or both act as principal. 
For example, :22F::TRCA//AGEN 
SETDET This block, and the AMT subsequence are necessary only when commission or accrued interest is 
specified on the trade. 
22F [[settlement]] Indicator (SETR) 
This field is SWIFT mandatory for the block and is reflected on all MT518 messages where the 
SETDET block is included. The available options are as follows: 
• SETR//RPTO – This [[Option]] must be reflected if the trade is not a special trade (i.e., if the 
trade does not reflect one of the following options for the field). 
• SETR/GSCC/STRD – This indicates that the trade is a Special Trade and will settle Trade 
for Trade. 
• SETR/GSCC/CPRO – This indicates that the trade is Comparison Only and will not go 
to [[settlement]]. 
Note: See Appendix H for a mapping of the above [[settlement]] Type Indicators to those used on batch 
input/output. 
For example, :22F::SETR//RPTO or :22F::SETR/GSCC/STRD 
AMT This Optional Repeating block is necessary only to support including commission, accrued 
interest, or both. This block should always be included within the [[settlement]] Details (SETDET) 
block. 
19A Commission Amount 
This field is used to reflect commissions or concessions specified as an amount per trade (rather than 
amount per hundred). SPCN appears on all MT518 messages as they appeared on the trade 
submission. EXEC only appears on MT518 advices referring to your own trades. 
• SPCN//USD – Specifies the concession amount on yield trades. The field is signed to 
allow both positive and negative values. 
• EXEC//USD – regulatory field – Specifies the executing [[Broker]] commission on customer 
and/or regulatory agency trades. 
Note: The value in this field is an amount per trade. The commission amount field is in SWIFT 
Standard Format, which is left justified, with  commas removed, and a comma used in lieu of a decimal. 
The amount must be preceded by a 3– character ISO currency code. 
For example, :19A::SPCN//USDN12,5 
19A Accrued Interest 
This field appears on all MT518 messages, where provided by the client, recalculated by the system, or 
both. 
• ACRU//USD – Specifies the accrued interest amount. 
Note: Swift format allows for a field size of 15d, however, a maximum of 10d is supported for the 
application. 
For example, :19A::ACRU//USD1040, 
OTHRPRTY This Optional block is only necessary if the originator of the message is not the same as 
the sender of the message. 
95Q Originator of Message (MEOR) 
• MEOR// – regulatory field - Specifies the originator of the message if NOT the sender of 
the message. It appears only on MT518 advices referring to your own trades. 
For example :95Q::MEOR//ORGN 

---

## Page 79

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 79 
MT518 Field Analysis (CMPM, DFVA, SITR, NAFI, DCCX, YTPR, STLD) 
 
SWIFT MT518 Layout Advices Referring to Your Trades 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPM DFVA SITR NAFI DCCX YTPR STLD 
    Message Header        
    Password        
    Sender        
    Message Type        
    Receiver        
M :16R: GENL  Start of Block        
M :20C: :SEME//  Sender’s Reference for this message        
M :23G: NEWM  Message Function = New Message or        
  CANC  Cancel        
O* :98C: :PREP//  Preparation Date/Time        
M :22F: :TRTR/ GSCC/CASH Trade Indicator = Bilateral Trade or        
   GSCC/TRLK Locked-in Trade or        
   GSCC/TRDC Demand Trade        
M :16R: LINK  Repeat Block Start        
O :20C: :MAST//  Master Reference Number        
M :16S: LINK  End of Block        
M :16R: LINK  Repeat Block Start        
O :20C: :PREV//  Previous Reference Number        
M :16S: LINK  End of Block        
M :16R: LINK  Repeat Block Start        
O :20C: :LIST//  CMU RTTM Assigned Reference Number        
M :16S: LINK  End of Block        
M :16R: LINK  Repeat Block Start        
O :20C: :TRRF//  Regulator Control Number        
M :16S: LINK  End of Block        
M :16R: LINK  Repeat Block Start        
O :20C: :COMM//  Match Control Number        
M :16S: LINK  End of Block        
M :16S: GENL  End of Block        
M :16R: CONFDET  Start of Block        

---

## Page 80

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 80 
SWIFT MT518 Layout Advices Referring to Your Trades 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPM DFVA SITR NAFI DCCX YTPR STLD 
M :98C: :TRAD//  Trade Date/Time        
M :98A: :SETT//  [[settlement]] Date or        
M :98B: :SETT// WISS [[settlement]] Date – [[settlement]] to be completed when 
Security is issued 
       
M :90A: :DEAL/ /PRCT/ Deal Price Percentage or        
   /YIEL/ Yield or        
O* :94B: :TRAD/ GSCC/OTCP Market of Execution 
[[Over-The-Counter]] Corporate or 
       
   GSCC/OTMU [[Over-The-Counter]] Municipal or        
   GSCC/OTUI [[Over-The-Counter]] Unit Investment Trust        
O :19A: :SETT/ /USD [[settlement]] Amount        
M :22H: :BUSE/ /BUYI Trade Type Buy or        
   /SELL Sell        
O :22F: :PRIC/ GSCC/WGTP Type of Price – Weighted Price        
O* :22F: :PROC/ GSCC/CMPR Match Request or        
   GSCC/CRQM Match Request Modify or        
   GSCC/CADV Match Request Cancel or        
   GSCC/CMDA Post-Match Contra Trade Modification or        
   GSCC/LCTA Locked-In Trade Advice or        
   GSCC/CMPM Trade Matched with Modifications or        
   GSCC/DFVA Notification of [[default]] Values Applied or        
   GSCC/SITR Screen Input Trade Replay or        
   GSCC/NAFI Trade DK Advice or        
   GSCC/DCCX DK Remove Advice or        
   GSCC/YTPR Repricing – Yield to Price or        
   GSCC/STLD [[settlement]] Disposition        
O :22F: :TTCO/ GSCC/TSQS Trade Type/Target Indicator – QSR Trade or        
   GSCC/TTQS Target QSR Trade or        
M :22H: :PAYM/ /APMT Against Payment Trade        
M :16R: CONFPRTY  Repeat Block Start        
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]]        
O :20C: :PROC//  [[Buyer]] (Contra) reference        
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative        
   /TDID [[Buyer]] (Contra) Trader [[ID]]        

---

## Page 81

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 81 
SWIFT MT518 Layout Advices Referring to Your Trades 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPM DFVA SITR NAFI DCCX YTPR STLD 
O :70E: :DECL/ /GSCC Narrative/ Additional Reference Numbers/ 
Information 
       
   /PREV [[Buyer]] (Contra) Previous External Reference 
Number 
       
   /CORR Party = MPID of [[Buyer]]’s Correspondent firm        
O :22F: :TRCA/ /AGEN Capacity Indicator – Acting as Agent Indicator or        
   /PRIN Acting as Principal Indicator        
M :16S: CONFPRTY  Repeat Block End        
M :16R: CONFPRTY  Repeat Block Start        
M :95R: :SELL/ GSCC/PART Party = [[Seller]]        
O :20C: :PROC//  [[Seller]] (Contra) reference        
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative        
   /TDID [[Seller]] (Contra) Trader [[ID]]        
O :70E: :DECL/ /GSCC Narrative/ Additional Reference Numbers/ Information        
   /PREV [[Buyer]] (Contra) Previous External Reference Number        
   /CORR Party = MPID of [[Seller]]’s Correspondent Firm        
O :22F: :TRCA/ /AGEN Capacity Indicator – Acting as Agent Indicator or        
  

---

## Page 82

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 82 
SWIFT MT518 Layout Advices Referring to Your Trades 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPM DFVA SITR NAFI DCCX YTPR STLD 
   /PRIN Acting as Principal Indicator        
M :16S: CONFPRTY  Repeat Block End        
M :36B: :CONF/ /FAMT/ Quantity as Face Amount (Par) or        
   /UNIT/ Quantity as Units / [[shares]]        
M :35B:  /US/ Identification of Financial Instrument- [[CUSIP]]    
 
    
O :70E: :TPRO/ /GSCC Trade Instruction Processing Narrative        
   /MSGR Message Reason        
   /DKRS DK Reason (see Appendix E)        
   /DEST Destination Indicator (Note: This is a repeating field)        
   /DEST 01 = CMU RTTM, 02 = MSRB        
   /ITYP Issue Type – SY = [[syndicate]] or        
    TS = Target [[syndicate]] or        
   /SDAD [[settlement]] Date Adjustment        
    /RVSL Trade Reversal Indicator        
   /SPXR MSRB Special Condition Indicators        
   /RCTL Reversal Control Number        
   /YIEL Additional Yield        
   /SDSP [[CNS]] Eligibility = CNSE - [[CNS]] or        
    CNSN - Not [[CNS]] or        
    CPRO - Comparison Only or        
    TFTD - Trade for Trade        
   /DDTE Delivery Date        
   /RGDP Regulatory Dollar Price        
   /MISC Miscellaneous        
M :16S: CONFDET  End of Block        
M :16R: SETDET  Start of Optional Sequence        
M :22F: :SETR/ /RPTO [[settlement]] Indicator – Reporting-Only or        
 

---

## Page 83

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 83 
SWIFT MT518 Layout Advices Referring to Your Trades 
M/O Tag Block/ 
Qualifier 
Subqualifier Field Description CMPM DFVA SITR NAFI DCCX YTPR STLD 
   GSCC/STRD 
 
[[settlement]] Type Indicator – Special 
Trade or 
       
   GSCC/CPRO Comparison Only        
M :16R: AMT  Repeat Block Start        
M :19A: :SPCN/ /USD Special Concessions or        
  :EXEC/ /USD Executing [[Broker]] Commission        
M :16S: AMT  End of Block        
M :16R: AMT  Repeat Block Start        
M :19A: :ACRU/ /USD Accrued Interest Amount        
M :16S: AMT  End of Block        
M :16S: SETDET  End of Block        
M :16R: OTHRPRTY  Optional Block Start        
M :95Q: :MEOR//  Originator of message (if other than 
the Sender) 
       
M :16S: OTHRPRTY  End of Block        
  

---

## Page 84

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 84 
MT518 Field Analysis Table 2 (CMPR, CRQM, CADV, CMDS, LCTA) 
SWIFT MT518 Layout Advisories Locked-in Advices 
M/O Tag Block/Qualifier Subqualifier Field Description CM
PR 
CRQM CADV CMDA LCT
A 
          
    Message Header      
    Password      
    Sender      
    Message Type      
    Receiver      
M :16R: GENL  Start of Block      
M :20C: :SEME//  Sender’s Reference for this message      
M :23G: NEWM  Message Function = New Message or      
  CANC  Cancel      
O* :98C: :PREP//  Preparation Date/Time      
M :22F: :TRTR/ GSCC/CASH Trade Indicator = Bilateral Trade or      
   GSCC/TRLK Locked-in Trade or      
   GSCC/TRDC Demand Trade      
M :16R: LINK  Repeat Block Start      
O :20C: :MAST//  Master Reference Number      
M :16S: LINK  End of Block      
M :16R: LINK  Repeat Block Start      
O :20C: :PREV//  Previous Reference Number      
M :16S: LINK  End of Block      
M :16R: LINK  Repeat Block Start      
O :20C: :LIST//  CMU RTTM Assigned Reference Number      
M :16S: LINK  End of Block      
M :16R: LINK  Repeat Block Start      
O :20C: :TRRF//  Regulator Control Number      
M :16S: LINK  End of Block      
M :16R: LINK  Repeat Block Start      
O :20C: :COMM//  Match Control Number      
M :16S: LINK  End of Block      
M :16S: GENL  End of Block      
M :16R: CONFDET  Start of Block      
M :98C: :TRAD//  Trade Date/Time      

---

## Page 85

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 85 
SWIFT MT518 Layout Advisories Locked-in Advices 
M/O Tag Block/Qualifier Subqualifier Field Description CM
PR 
CRQM CADV CMDA LCT
A 
M :98A: :SETT//  [[settlement]] Date or      
M :98B: :SETT// WISS [[settlement]] Date – [[settlement]] to be 
completed when Security is issued 
     
M :90A: :DEAL/ /PRCT/ Deal Price Percentage or      
   /YIEL/ Yield      
O* :94B: :TRAD/ GSCC/OTCP Market of Execution [[Over-The-Counter]] 
Corporate or 
     
   GSCC/OTMU [[Over-The-Counter]] Municipal or      
   GSCC/OTUI [[Over-The-Counter]] Unit Investment Trust      
O :19A: :SETT/ /USD [[settlement]] Amount      
M :22H: :BUSE/ /BUYI Trade Type Buy or      
   /SELL Sell      
O :22F: :PRIC/ GSCC/WGTP Type of Price – Weighted Price      
O* :22F: :PROC/ GSCC/CMPR Match Request or      
   GSCC/CRQM Match Request Modify or      
   GSCC/CADV Match Request Cancel or      
   GSCC/CMDA Post Match Contra Trade Modification or      
   GSCC/LCTA Locked-In Trade Advice or      
   GSCC/CMPM Trade Matched with Modifications or      
   GSCC/DFVA Notification of [[default]] Values Applied or      
   GSCC/SITR Screen Input Trade Replay or      
   GSCC/NAFI Trade DK Advice or      
   GSCC/DCCX DK Remove Advice or      
   GSCC/YTPR Yield to Price – Repricing or      
   GSCC/STLD [[settlement]] Disposition      
O :22F: :TTCO/ GSCC/TSQS Trade Type/Target Indicator – QSR 
Trade or 
     
   GSCC/TTQS Target QSR Trade      
M :22H: :PAYM/ /APMT Against Payment Trade      
M :16R: CONFPRTY  Repeat Block Start      
M :95R: :BUYR/ GSCC/PART Party = [[Buyer]]      
O :20C: :PROC//  [[Buyer]] (Contra) reference      
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative      
   /TDID [[Buyer]] (Contra) Trader [[ID]]      

---

## Page 86

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 86 
SWIFT MT518 Layout Advisories Locked-in Advices 
M/O Tag Block/Qualifier Subqualifier Field Description CM
PR 
CRQM CADV CMDA LCT
A 
O :70E: :DECL/ /GSCC Narrative/ Additional Reference Numbers/ 
Information 
     
   /PREV [[Buyer]] (Contra) Previous External 
Reference Number 
     
   /CORR Party = MPID of [[Buyer]]’s Correspondent 
firm 
     
O :22F: :TRCA/ /AGEN Capacity Indicator – Acting as Agent 
Indicator or 
     
   /PRIN Acting as Principal Indicator      
M :16S: CONFPRTY  Repeat Block End      
M :16R: CONFPRTY  Repeat Block Start      
M :95R: :SELL/ GSCC/PART Party = [[Seller]]      
O :20C: :PROC//  [[Seller]] (Contra) reference      
O :70C: :PACO/ /GSCC [[participant]] Contact Narrative      
   /TDID [[Seller]] (Contra) Trader [[ID]]      
O :70E: :DECL/ /GSCC Narrative/ Additional Reference Numbers/ 
Information 
     
   /PREV [[Seller]] (Contra) Previous External 
Reference Number 
     
   /CORR Party = MPID of [[Seller]]’s Correspondent 
Firm 
     
O :22F: :TRCA/ /AGEN Capacity Indicator – Acting as Agent 
Indicator or 
     
   /PRIN Acting as Principal Indicator      
M :16S: CONFPRTY  Repeat Block End      
M :36B: :CONF/ /FAMT/ Quantity as Face Amount (Par) or      
   /UNIT/ Quantity as Units / [[shares]]      
M :35B:  /US/ Identification of Financial Instrument- 
[[CUSIP]] 
     
O :70E: :TPRO/ /GSCC Trade Instruction Processing Narrative      
   /MSGR Message Reason      
   /DKRS DK Reason (see Appendix E)      
   /DEST Destination Indicator (Note: This is a 
repeating field) 
     
   /DEST 01=CMU RTTM, 02 = MSRB      
   /ITYP Issue Type – SY = [[syndicate]] or      

---

## Page 87

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 87 
SWIFT MT518 Layout Advisories Locked-in Advices 
M/O Tag Block/Qualifier Subqualifier Field Description CM
PR 
CRQM CADV CMDA LCT
A 
    TS = Target [[syndicate]] or      
   /SDAD [[settlement]] Date Adjustment      
   /RVSL Trade Reversal Indicator      
   /SPXR MSRB Special Condition Indicators      
   /RCTL Reversal Control Number      
   /YIEL Yield      
   /SDSP [[CNS]] Eligibility = CNSE - [[CNS]] or      
    CNSN - Not [[CNS]] or      
    CPRO - Comparison Only or      
    TFTD - Trade for Trade      
   /DDTE Delivery Date      
   /RGDP Regulatory Dollar Price      
   /MISC Miscellaneous      
M :16S: CONFDET  End of Block      
M :16R: SETDET  Start of Optional Sequence      
M :22F: :SETR/ /RPTO [[settlement]] Indicator = Reporting-Only or      
   GSCC/STRD [[settlement]] Type Indicator – Special 
Trade or 
     
   GSCC/CPRO Comparison Only      
M :16R: AMT  Repeat Block Start      
M :19A: :SPCN/ /USD Special Concessions or      
  :EXEC/ /USD Executing [[Broker]] Commission      
M :16S: AMT  End of Block      
M :16R: AMT  Repeat Block Start      
M :19A: :ACRU/ /USD Accrued Interest Amount      
M :16S: AMT  End of Block      
M :16S: SETDET  End of Block      
M :16R: OTHRPRTY  Optional Block Start      
M :95Q: :MEOR//  Originator of message (if other than the 
Sender) 
     
M :16S: OTHRPRTY  End of Block      
 

---

## Page 88

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 88 
MT599 Message 
The MT599 message is specified by SWIFT as a free format message. CMU RTTM uses this message 
to convey system administrative information to clients. 
 Message Usage 
1 CMU RTTM Start-of-Day Notification 
(:79:GSCC/GADM…/GSOD/) 
Sent in the beginning of each business day to inform a [[Member]] that 
the CMU RTTM system is available. 
2 CMU RTTM Submission Cutoff End-of-
Day Message (:79:GSCC/GADM…/EDCS/) 
Sent when clients may no longer submit transactions to be included 
in processing for that day. Any transaction submitted to CMU RTTM 
after this point is queued to be included in the next business day’s 
processing. 
3 CMU RTTM Processing End- of- 
Day Message 
(:79:GSCC/GADM…/EODC/) 
Sent to members to inform them that the CMU RTTM system has 
completed processing for that business day, and that all interactive 
output to be generated that day has been transmitted. 
MT599 Message Specification 
This section includes the MT599 message specification. The MT599 message is a free-format SWIFT 
message that CMU RTTM utilizes to communicate administrative messages to clients (and their service 
providers, where appropriate). CMU RTTM uses this message type to notify clients regarding start and 
end-of-day processing, as well as cutoffs for trade submission. 
When the CMU RTTM system is open for trade submission, one start-of-day message is sent out for each 
business day: 
• /GSOD/ - This start-of-day message signals to clients that the CMU RTTM system is available for 
submitting trades to include in that day’s processing. 
The following two end-of-day messages are sent to clients on a nightly basis: 
• /EDCS/ - Indicates to clients that CMU RTTM does not accept any more trade submissions for inclusion 
in that day’s processing. Any trades submitted after this point are held and included in the next business 
day’s matching process. No acknowledgements or rejections are sent to clients for these trades 
until the system is next available (after the ‘/GSOD/’ start-of-day message is sent). 
• /EODC/ - Indicates to clients that CMU RTTM has completed batch processing, and that CMU RTTM 
does not send any more interactive messages for that business day. 
All MT599 messages sent by CMU RTTM provide the client with the date and time of the message 
preparation and the date for the business day in question. End-of-day messages also contain the next 
CMU RTTM valid trade submission date. 
NSCCTRRS ([[NSCC]] Trade Registration and Reconciliation System) is the sender of the MT599 
Administrative System messages specified in this document. 
  

---

## Page 89

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 89 
MT599 Format Differences 
It is important to note that this MT599 message is an older SWIFT message type, which is slightly different 
in format from the other ISO 15022 messages. For MT599 messages, the following applies: 
• No beginning-of-block and end-of-block tags (16R and 16S). 
• Tags [[DO]] not always include the optional one-character format suffix. 
• No generic fields, qualifiers, or repeating sequences. 
Qualifiers are included in Tag 79 in an attempt to maintain similar formats to other messages 
implemented, given that SWIFT allows any type of text to be included in narrative fields. For this purpose, 
[[FICC]] has attempted to delineate, and label, the ‘subfields’ included in this tag in a similar manner to those 
on other messages in the interactive messaging specification. Tag 79 reflects a reference to the record 
type being sent, which always follows the message preparation date and time. 
MT599 General Format 
M/O Tag Block/ Qualifier Subqualifier / 
Options 
Field Description Data Field Format 
    Message Header  
M    Password 12!c 
M    Sender 8!c 
M    Message Type 3!n/3!n/4!c 
M    Receiver 8!c 
 
M 
 
:20: 
  Transaction (sender’s message) 
Reference Number 
16x 
M :79:   Narrative (35*50x) 
  GSCC/GADM  CMU RTTM Administrative 
Message 
4!c/4!c 
  /PREP/  Preparation Date/Time (8!n6!n) YYYYMMDDHHMMSS 
  /GSOD/  CMU RTTM Start-of-Day 
Notification or 
YYYYMMDD 
  /EDCS/  CMU RTTM Submission Cutoff 
End-of-Day Message or 
YYYYMMDD 
  /EODC/  CMU RTTM Processing End-of-
Day Message 
YYYYMMDD 
  /NXTD/  Next CMU RTTM ‘Trade 
Submission’ Day 
YYYYMMDD 
  

---

## Page 90

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 90 
MT599 Field Specifications 
Block/ Tag  Notes 
Message Header Each message must contain a message header. All header fields are mandatory fixed format 
with trailing blanks, where required. 
Password 12!c Blank filled on MT599 messages. 
Sender 8!c NSCCTRRS ([[NSCC]] Trade Registration and Reconciliation System) will be the 
sender of the MT599 Administrative messages in this document. 
Message Type 3!n/3!n/4!c The first three characters indicate to the recipient the message type (599); the 
second three positions reflect the version of the message interface (currently 
always 000). The last four characters indicate the [[issuer]] code to be used in the 
message (“GSCC”). 
Receiver 8!c [[participant]] [[ID]] 
20 Transaction (Sender’s Message) Reference Number 
Contains the sender’s message reference number. It is mandatory and contains a unique 
number to unambiguously identify each message sent from CMU RTTM. (This is a 
communications message number, not a trade number.) 
Note: While the SWIFT message accommodates both uppercase and lowercase alphanumeric 
and certain symbols, this field is populated with an uppercase alphanumeric value for CMU 
RTTM purposes. It does not contain symbols or hyphens. 
For example, :20:ABCDEFG1 
70 Narrative 
Contains the various administrative message data, including the type of message. This field 
uses the following qualifiers: 
GSCC/GADM - Indicates that this is an administrative message being sent by CMU RTTM. 
/PREP/ - Contains the message preparation date and time. 
/GSOD/ - Indicates to clients that this MT599 message is CMU RTTM’s beginning of day 
notification for the business date noted. Subsequent to receiving this message, clients can 
begin to send transactions to CMU RTTM to be included in that day’s processing. Any 
messages received by CMU RTTM after this point, and before the end-of-day submission 
cutoff, results in immediate acknowledgement/rejection. CMU RTTM also begins sending 
acknowledgement/rejection MT509 output for all trades received after the prior business 
day’s cutoff point. 
/EDCS/ - Indicates that this MT599 message is CMU RTTM’s notification to the client that any 
trades received by CMU RTTM after this time are not included in that day’s processing. All 
trades received by CMU RTTM after this cutoff (until the next night’s cutoff/ “EDCS” 
message) are included in processing for the next processing/trade date indicated below 
(following the qualifier ‘/NXTD/’). 
/EODC/ - Indicates that this MT599 message is CMU RTTM’s notification to clients that CMU 
RTTM has completed its batch processes and no more interactive matching output is generated 
for CMU RTTM for that business day. Any matching-related output sent by CMU RTTM 
after this point (through the generation of the next ‘EODC’ message) is for the business 
day indicated below (following the qualifier ‘/NXTD/’). 
/NXTD/ - Provides the next valid CMU RTTM trade submission date, and it is included on all 
CMU RTTM end-of- day messages. 
For example, 
:79:GSCC/GADM/PREP/20030331200150/EDCS/20030331 
/NXTD/20030401 
 

---

## Page 91

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 91 
LISTING OF APPENDICES 
The documents included in this section are provided as a supplement to the specifications 
included in this document. 
Appendix Description 
Appendix A Mandatory Data for [[NSCC]] CMU RTTM contains CMU RTTM/[[NSCC]] Mandatory Data fields for trade 
input. 
Appendix B Message Flows contains detailed diagrams depicting the flows of messages to and from CMU 
RTTM for various transaction related scenarios. 
Appendix C Message Samples provides samples of a variety of MT515, MT509, and MT518 messages for 
bilateral, demand, and locked-in trades. Only one set of message samples (Municipal RW Bilateral 
trade messages) is included in this document. The remaining message samples are provided under 
separate cover. 
Appendix D Message Structure Diagrams contains diagrams from the SWIFT manual reflecting the structure of 
the MT515, MT509, and MT518 messages. 
Appendix E CMU RTTM Code Tables contains tables of reason codes for Rejects, DK’s and messages used in 
the MT515, MT509, and MT518 messages. 
Appendix F MT518 Processing of Regulatory Fields provides a table that specifies MT518 message treatment 
of regulatory data. 
Appendix G Regulatory Information contains regulatory fields for MSRB and regulator code tables. 
Appendix H [[settlement]] Type Indicator Field Mapping provides a cross- reference of the [[settlement]] Type Codes 
(special trade codes) used on interactive messages to the codes used on batch input and output.   

---

## Page 92

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 92 
APPENDIX A: MANDATORY DATA FOR [[NSCC]] CMU 
RTTM 
This appendix lists mandatory data for CMU RTTM trade input. MT515 Instruct records require the fields 
listed below in alphabetical order (not the order they appear on the message). 
Field Description Tag Comments 
Accrued Interest Amount :19A::ACRU// Optional, not used for 
matching 
Business Use - Buy Business Use - Sell :22H::BUSE//BUYI or 
:22H::BUSE//SELL 
 
Concession :19A::SPCN// Optional Muni WI submitted 
with Yield and Concession 
Contraparty ([[Buyer]] or [[Seller]]) :95R::SELL/GSCC/PART 
:95R::BUYR/GSCC/PART 
 
Contraparty Correspondent :70E::DECL/GSCC/CORR  
Trade Type/Target Indicator - QSR Source Trade 
Type/Target Indicator - QSR Target 
:22F::TTCO/GSCC/TSQS 
:22F::TTCO/GSCC/TTQS 
Used only for QSR trades 
[[CUSIP]] :35B::/US/  
Destination Indicator - CMU RTTM Only Destination 
Indicator - MSRB Only Destination Indicator - CMU 
RTTM and MSRB 
:70E::TPRO//GSCC/DEST01 
:70E::TPRO//GSCC/DEST02 
:70E::TPRO//GSCC/DEST01 
/DEST02 
 
Issue Type - [[syndicate]] Source Issue Type - [[syndicate]] 
Target 
:70E::TPRO//GSCC/ITYPSY 
:70E::TPRO//GSCC/ITYPTS 
Used only for Municipal 
[[syndicate]] trades 
Trade Transaction Type Indicator: 
• Bilateral 
• Demand ([[syndicate]]) 
• Locked-in (QSR) 
 
:22F::TRTR/GSCC/CASH 
:22F::TRTR/GSCC/TRDC 
:22F::TRTR/GSCC/TRLK 
 
Place of Trade-Market of Execution & Product: 
• [[OTC]] Corporate 
• [[OTC]] Municipal 
• [[OTC]] [[UIT]] 
 
:94B::TRAD/GSCC/OTCP 
:94B::TRAD/GSCC/OTMU 
:94B::TRAD/GSCC/OTUI 
 
[[participant]] ([[Buyer]] or [[Seller]]) :95R::SELL/GSCC/PART 
:95R::BUYR/GSCC/PART 
 
[[participant]] Correspondent :70E::DECL/GSCC/CORR  
Master Reference Number 
(External Reference also called Xref) 
:20C::MAST//  
Preparation Date and Time :98C::PREP//  
Price (Dollar Price) Yield :90A::DEAL//PRCT/ or 
:90B::DEAL//YIEL/ 
 
Quantity as Face Amount (Par) (Corp, Muni) or Quantity 
as Units [[shares]] ([[UIT]]) 
:36B::CONF/FAMT/ 
:36B::CONF/UNIT/ 
 
Record Type of MT515 Instruct or 
Cancel or Modify or DK 
 
:22F::PROC/INST 
:22F::PROC/CANC 
:22F::PROC/MDFC 
:22F::PROC/TDDK 
 
Reversal Indicator (Reversals only) :70E::TPRO//GSCC/RVSL  
[[settlement]] Amount :19A::SETT//USD  
[[settlement]] Date :98A::SETT//  

---

## Page 93

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 93 
Field Description Tag Comments 
[[settlement]] Date Adjustment (Extended [[settlement]] Days) :70E::TPRO//GSCC/SDAD  
[[settlement]] Type Indicator - Normal [[settlement]] 
[[settlement]] Type Indicator - Special Trade for Trade 
[[settlement]] Type Indicator - Comparison Only 
:22F::SETR//RPTO or 
:22F::SETR/GSCC/STRD or 
:22F::SETR/GSCC/CPRO 
 
Trade Date & Time :98C::TRAD//  
  

---

## Page 94

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 94 
APPENDIX B: MESSAGE FLOWS 
This appendix includes bilateral, demand, and locked-in trade flows between [[NSCC]] clients and CMU 
RTTM. Where the flows depict scenarios for demand ([[syndicate]]) or locked-in (QSR), Client A is always the 
demand or locked-in submitter. Client B is always the demand or locked-in recipient. All demand and 
locked-in flows assume Bilateral Matching, unless "Administrative Matching" has been indicated. All locked- in 
trade flows reflected apply to QSR trades. 
The major portion of client and CMU RTTM actions and related flows are represented in the bilateral trade 
section. An asterisk indicates that the bilateral flows are also applicable to demand and locked-in trades 
and they might not be repeated throughout all of the sections. All actions and flows reflected for bilateral 
trades apply to the bilateral submission side (target side) of all demand and locked-in submissions. Therefore, 
these flows are not repeated for all actions that the bilateral side of a demand or locked-in flow might be 
subject to. 
All flows show the messages that will be generated by CMU RTTM for the MSRB. MSRB receives all the 
messages as they appear in the flows. 
The flows illustrated in this appendix are grouped in the following order: 
• Bilateral Trade Flows 
• Demand Trade Flows (applies to [[syndicate]] trades) 
• Locked-in Trade Flows (applies to QSR trades) 
  

---

## Page 95

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 95 
Bilateral Trade Flows 
B-1. Bilateral Trade Accepted * 
 
B-2. Bilateral Trade Accepted (through the web) * 
 
  


---

## Page 96

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 96 
B-3. Bilateral Trade Rejected * 
 
B-4. Bilateral Trades Matched * 
 
  


---

## Page 97

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 97 
B-5. Bilateral Trades Matched with Modifications (by CMU RTTM with B as [[Buyer]]) * 
 
  


---

## Page 98

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 98 
B-6. Bilateral Trade Modified Pre-Match * 
 
B-7. Bilateral Trade Modify Pre-Match Rejected* 
 
  


---

## Page 99

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 99 
B-8. Bilateral Trade Modified Pre-Match (through the web) * 
 
  


---

## Page 100

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 100 
B-9. Bilateral Trade X-ref Modified Post-Match (before [[settlement]] Disposition 
determined) * 
 
  


---

## Page 101

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 101 
B-10. Bilateral Trade X-ref Modified Post-Match (through the web before [[settlement]] 
Disposition determined) * 
 
  


---

## Page 102

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 102 
B-11. Bilateral Trade X-ref Modified Post-Match (after [[settlement]] Disposition 
determined) * 
 
  


---

## Page 103

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 103 
B-12. Bilateral Trade Canceled Pre-Match * 
 
B-13. Bilateral Trade Canceled Pre-Match (through the web) * 
 
  


---

## Page 104

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 104 
B-14. Bilateral Trade Post-Match Cancel Rejected * 
  


---

## Page 105

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 105 
B-15. Bilateral Trade DKed * 
 
B-16. Bilateral Trade DKed (through the web) * 
 
  


---

## Page 106

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 106 
B-17. Bilateral Trade DK Rejected * 
 
B-18. Bilateral Trade Deleted due to DK 
 
  


---

## Page 107

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 107 
B-19. Bilateral Trade DKed - Canceled Pre-Match 
 
  


---

## Page 108

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 108 
B-20. Bilateral Trade DKed – Modified * 
 
  


---

## Page 109

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 109 
B-21. Bilateral Trade DK Removed * 
  


---

## Page 110

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 110 
B-22. Bilateral Trade DKed – DK Removed (through the web) - Matched 
 
B-23. Bilateral Trade DKed – Modified (through the web) – Matched 


---

## Page 111

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 111 
  


---

## Page 112

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 112 
B-24. Bilateral Trade Deleted Unmatched Transaction * 
 
  


---

## Page 113

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 113 
B-25. Bilateral Trade [[default]] Values Applied * 
 
  


---

## Page 114

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 114 
B-26. Bilateral Trades Pre-Match Repricing * 
 
  


---

## Page 115

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 115 
B-27. Bilateral Trades Post-Match Repricing * 
 
B-28. Bilateral Trade Memo Status Assigned * 


---

## Page 116

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 116 
 
  


---

## Page 117

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 117 
B-29. Bilateral Trade Memo Status Removed – Matched * 
  


---

## Page 118

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 118 
B-30. Bilateral Trades Memo Status Removed – Trades Repriced – Matched * 
 
  


---

## Page 119

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 119 
B-31. Bilateral Trade in Memo Status Deleted due to Security Detail Differences * 
 
  


---

## Page 120

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 120 
B-32. Bilateral Trade in Memo Status Deleted * 
 
  


---

## Page 121

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 121 
B-33. Bilateral Trade Pending Status Assigned – Trade Deleted * 
 
  


---

## Page 122

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 122 
B-34. Bilateral Trade Pending Status Assigned – Removed – Trades Matched* 
 
  


---

## Page 123

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 123 
B-35. Bilateral Trade Pending Status Removed – Trade Repriced * 
 
  


---

## Page 124

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 124 
B-36. Bilateral Trades Pending Status Assigned – Removed – Trades Matched – 
Repriced * 
 
  


---

## Page 125

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 125 
B-37. Bilateral Trades – Trades Submitted on or after [[settlement]] Date (with Delivery 
Date Re-assigned) * 
 
  


---

## Page 126

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 126 
B-38. Bilateral Trade Comparison Only Assigned – Trade Matched 
 
  


---

## Page 127

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 127 
B-39. Bilateral Trades Submitted for Comparison Only – Matched 
 
  


---

## Page 128

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 128 
B-40. Bilateral Reversal Trades Matched * 
 
B-41. Bilateral Trade Regulatory Field Modified Post-Match * 
 
  


---

## Page 129

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 129 
Demand Trade Flows 
B-D01. [[syndicate]] Trade - Bilaterally Matched 
(Client B Submits with Target Indicator) 
 
  


---

## Page 130

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 130 
B-D02. [[syndicate]] Trade - Administrative Match 
 
  


---

## Page 131

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 131 
B-D03. [[syndicate]] Recipient Trade Bilaterally Matched with Modifications 
(No Target Indicator Submitted) 
 
 
B-D04. [[syndicate]] Trade Repriced Pre-Match – Administrative Match 
  


---

## Page 132

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 132 
B-D05. [[syndicate]] Trade Modified Pre-Match 
 
B-D06. [[syndicate]] Trade Pre-Match Modify Rejected 
 
  


---

## Page 133

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 133 
B-D07. [[syndicate]] Trade X-ref Modified Post-Match (before [[settlement]] Disposition 
Determined) 
 
  


---

## Page 134

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 134 
B-D08. [[syndicate]] Target Trade Modified Pre-Match – Matched 
 
  


---

## Page 135

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 135 
B-D09. [[syndicate]] Target Trade Modified Post-Match 
 
  


---

## Page 136

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 136 
B-D10. [[syndicate]] Trade Cancelled Pre-Match 
 
B-D11. [[syndicate]] Target Trade Cancelled Pre-Match 
 
  


---

## Page 137

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 137 
B-D12. [[syndicate]] Trade Post-Match Cancel Rejected 
 
  


---

## Page 138

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 138 
B-D13. [[syndicate]] Trade DKed (by [[syndicate]] [[Member]]) 
 
  


---

## Page 139

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 139 
B-D14 [[syndicate]] Trade DK Rejected 
 
  


---

## Page 140

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 140 
B-D15 [[syndicate]] Trade Deleted due to DK 
 
  


---

## Page 141

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 141 
B-D16 [[syndicate]] Trade DKed/Canceled Pre-Match 
 
  


---

## Page 142

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 142 
B-D17 [[syndicate]] DKed/Modified Pre-Match 
 
  


---

## Page 143

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 143 
B-D18 [[syndicate]] Trade DK Removed 
 
  


---

## Page 144

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 144 
B-D19 [[syndicate]] Trade DKed/DK Removed/Matched 
 
  


---

## Page 145

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 145 
B-D20 Target [[syndicate]] Trade Deleted due to DK 
 
  


---

## Page 146

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 146 
B-D21 [[syndicate]] Trade Memo Status Assigned 
 
  


---

## Page 147

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 147 
B-D22 [[syndicate]] Trades Memo Status Removed/Trades Matched 
 
  


---

## Page 148

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 148 
B-D23 [[syndicate]] Trade in Memo Status Deleted due to Security Detail Differences 
 
B-D24 [[syndicate]] Trade in Memo Status Deleted 
 
  


---

## Page 149

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 149 
B-D25 [[syndicate]] Trade Pending Status Assigned/Removed 
 
  


---

## Page 150

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 150 
B-D26 [[syndicate]] Trade Pending Status Assigned/Trade Deleted 
 
  


---

## Page 151

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 151 
B-D27 [[syndicate]] Trades Pending Status Assigned/Removed/Trades Matched 
 
  


---

## Page 152

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 152 
B-D28 [[syndicate]] Trade Submitted on [[settlement]] Date Rejected 
 
  


---

## Page 153

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 153 
B-D29 [[syndicate]] Reversal Trades Bilaterally Matched (Client B submits Reversal with 
Target Indicator) 
 
  


---

## Page 154

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 154 
Locked-in Trade Flows 
B-LQ01 Locked-in Trade Bilaterally Matched (Client B submits trade with Target 
Indicator) 
 
  


---

## Page 155

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 155 
B-LQ02 Locked-in Trade Administrative Match 
 
  


---

## Page 156

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 156 
B-LQ03 Locked-in Recipient Trade Matched with Modifications (no Target Indicator 
submitted) 
 
  


---

## Page 157

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 157 
B-LQ04 Locked-in Trade Modified Pre-Match 
 
  


---

## Page 158

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 158 
B-LQ05 Locked-in Trade X-ref Modified Post-Match (before [[settlement]] Disposition 
determined) 
 
B-LQ06 Target Locked-in Trade Modified Pre-Match 


---

## Page 159

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 159 
 
  


---

## Page 160

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 160 
B-LQ07 Target Locked-in Trade Xref Modified Post-Match (before [[settlement]] 
Disposition determined) 
 
B-LQ08 Locked-in Trade Canceled Pre-Match 


---

## Page 161

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 161 
 
B-LQ09 Target Locked-in Trade Canceled Pre-Match 
 
  


---

## Page 162

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 162 
B-LQ10 Locked-in Trade DKed 
 
 
B-LQ11 Locked-in Trade DK Rejected 
 
  


---

## Page 163

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 163 
B-LQ12. Locked-in Trade DKed (through the screen) 
 
  


---

## Page 164

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 164 
B-LQ13 Locked-in Trade DKed/Administratively Matched 
 


---

## Page 165

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 165 
B-LQ14. Locked-in Trade DKed/Canceled Pre-Match 
 
  


---

## Page 166

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 166 
B-LQ15. Locked-in Trade DKed/Modified/Administratively Matched 
 
  


---

## Page 167

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 167 
B-LQ16 Locked-in Trade DKed/DK Removed (through the screen)/Matched 
 
B-LQ17. Locked-in Trade DKed/Matched (Client B’s Instruct generates the DK Remove 
Advice) 
  


---

## Page 168

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 168 
B-LQ18. Target Locked-in Trade DKed 
 
  


---

## Page 169

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 169 
B-LQ19. Target Locked-in Trade Deleted due to DK 
 
  


---

## Page 170

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 170 
B-LQ20. Locked-in Trades Memo Status Assigned/Removed/Trade Matched 
 
  


---

## Page 171

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 171 
B-LQ21. Locked-in Trade Pending Status Assigned/Removed/Trade 
Repriced/Administratively Matched 
 
  


---

## Page 172

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 172 
B-LQ22 Locked-in Trade Pending Status Assigned/Removed/Trade Bilaterally Matched  
(Client B submits trade with Target Indicator) 
 
  


---

## Page 173

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Message Specifications 173 
B-LQ23 Locked-in Reversal Trades Bilaterally Matched (Client B submits Target 
Reversal trade) 
 
  


---

## Page 174

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 174 
APPENDIX C: MESSAGE SAMPLES 
This appendix provides the following sets of message samples to enable clients to obtain more information 
regarding the formation of messages. It should be noted that these message samples are intended to provide a 
view of how messages should be formatted/structured, rather than reflect a complete flow of events.  
Sample Trade 1: Municipal Bond (Bilateral Regular Way Match) 
On February 11, 2003, Dealer Client 1563 sells Regular Way Municipal Bond ([[CUSIP]] 78764HAD6) at a 
contract amount of $10,206.89 to Dealer Client 1511. 
Field Description Client A – 1563 ([[Seller]]) Client B – 1511 ([[Buyer]]) 
Password PW7326 PW5263 
Sender [[ID]] 1563 1511 
SEME 10045FEB1103 02112003A0001 
MAST M0001570203 02112003T00011 
Preparation Date & Time 2/11/2003 7:52:59 2/11/2003 7:53:16 
Trade Date & Time 2/11/2003 7:52:50 2/11/2003 7:52:58 
[[settlement]] Date 2/14/2003 2/14/2003 
Price 0 (Final Money Trade) 0 (Final Money Trade) 
Contract Amount 10206,89 10206,89 
Contra [[participant]] 1511 1563 
Contra Correspondent EJLD FRSD 
Contra Trader [[ID]] AJ101  
[[participant]] Correspondent FRSD EJLD 
[[participant]] Capacity Principal Principal 
[[CUSIP]] 78764HAD6 78764HAD6 
PAR 10000, 10000, 
CMU RTTM Reference Number (TID) 0423008597 0423009016 
Accrued Interest 206,89 206,89 
Match Control Number 0423008597 0423008597 
Regulatory Dollar Price 98,56 98,56 
  

---

## Page 175

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 175 
The following message samples for Trade #1 are all based on the scenario presented on the previous page.  
Part A – Regular Way Trade Match 
•  1a.  MT515 Client A submits Sell Trade to CMU RTTM  
• 1b.  MT509 Trade Accepted sent to Client A 
•  1c.  MT509 Trade Rejected sent to Client A  
• 1d.  MT518 Match Request sent to Client B 
•  1e.  MT515 Client B submits Buy Trade to CMU RTTM  
• 1f. MT509 Trade Accepted sent to Client B 
• 1g. MT518 Match Request sent to Client A  
•  1h. MT509 Trade Matched sent to Client A  
• 1i.   MT509 Trade Matched sent to Client B 
•  1j. MT518 Match Request Cancel (due to Match) sent to Client A  
•  1k. MT518 Match Request Cancel (due to Match) sent to Client B  
• 1l.   MT518 [[settlement]] Disposition sent to Client A 
• 1m. MT518 [[settlement]] Disposition sent to Client B 
Part B – Regular Way Trade – Cancel 
• 1n. MT515 Client A submits Cancel of Sell Trade to CMU RTTM (Pre-matching)  
• 1o. MT518 Match Request Cancel (Due to Contra Action) sent to Client B 
Part C – Regular Way Trade – DK 
• 1p. MT515 Client B submits DK of Trade  
• 1q. MT518 DK Advice sent to Client A 
• 1r. MT518 DK Remove Advice sent to Client A 
Part D – Regular Way Trade – Modify 
• 1s. MT515 Client A submits Modify Sell Trade to CMU RTTM (Pre-matching)  
• 1t. MT518 Match Request Modify sent to Client B 
• 1u. MT515 Client A submits Modify Sell Trade to CMU RTTM (Post-matching)  
• 1v. MT518 Post-match Contra Trade Modification sent to Client B 
Part E – Regular Way Trade – Miscellaneous 
• 1w. MT518 Matched With Modifications sent to Client B 
• 1x. MT515 Client B submits Reversal to CMU RTTM (Reversal of BUY) 
• 1y. MT518 Screen Input Trade Replay of Sell Trade (SITR) sent to Client A 
  

---

## Page 176

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 176 
Part A – Regular Way Trade Match 
Sample #1a: MT515 Client A submits Sell Trade to CMU RTTM 
Message Content Comments 
Message Header 
PW7326 CMU RTTM Assigned Password 
1563 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//10045FEB1103 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075259 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0001570203 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02 
/RGDP98,56 
Trade Instruction Processing – Destination Indicator = CMU RTTM and MSRB; 
Regulatory Dollar Price. 
Note: The message content in this sample is split into two lines with new line 
starting with forward slash followed by regulatory dollar price tag and value. 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
End of Message 
  

---

## Page 177

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 177 
Sample #1b: MT509 Trade Accepted Sent to [[participant]] A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1563 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250001 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030211075311 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0001570203 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//10045FEB1103 Related Reference ([[participant]]’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423008597 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
  

---

## Page 178

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 178 
Sample #1c: MT509 Trade Rejected Sent to [[participant]] A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1563 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000500011 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030211075311 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0001570203 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//10045FEB1103 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//REJT Trade Input Rejected Status 
:16R:REAS Optional Repeat Block Start 
:24B::REJT/GSCC/E001 Reject Reason Code: E001 = External Reference Number Error 
:16S:REAS Optional Repeat Block End 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 179

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 179 
Sample #1d: MT518 Match Request Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1511 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250008 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075312 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade)` 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//M0001570203 Contra [[Seller]] X-ref 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/RGDP98,56 Trade Instruction Processing – Regulatory Dollar Price. 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
End of Message 
  

---

## Page 180

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 180 
Sample #1e: MT515 Client B Submits Buy Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PW5263 CMU RTTM Assigned Password 
1511 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//02112003A0001 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075316 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//02112003T00011 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075258 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02 
/RGDP98,56 
Trade Instruction Processing – Destination Indicator CMU RTTM 
and MSRB; Regulatory Dollar Price. 
Note: The message content in this sample is split into two lines 
with new line starting with forward slash followed by regulatory 
dollar price tag and value. 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
– End of Message 
  

---

## Page 181

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 181 
Sample #1f: MT509 Trade Accepted Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1511 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250011 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030211075325 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//02112003T00011 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//02112003A0001 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423009016 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
– End of Message 
  

---

## Page 182

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 182 
Sample #1g: MT518 Match Request Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1563 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250137 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075327 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075258 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//02112003T00011 Contra [[Buyer]] X-ref 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/RGDP98,56 Trade Instruction Processing – Regulatory Dollar Price. 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
– End of Message 
  

---

## Page 183

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 183 
Sample #1h: MT509 Trade Matched Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1563 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100002250261 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030211075328 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0001570203 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423008597 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//02112003T00011 Contraparty Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0423008597 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
– End of Message 
 
  

---

## Page 184

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 184 
Sample #1i: MT509 Trade Matched Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1511 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000251039 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030211075328 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//02112003T00011 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423009016 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//M0001570203 Contraparty Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0423008597 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
– End of Message 
  

---

## Page 185

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 185 
Sample #1j: MT518 Match Request Cancel (due to Match) Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1563 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000750137 Sender’s Message Reference Number 
:23G:CANC Cancel 
:98C::PREP//20030211075329 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075258 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//02112003T00011 Contra [[Buyer]] X-ref BIC 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm SIP 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH 
/RGDP98,56 
Trade Instruction Processing – Message Reason = due to Match, 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
End of Message 
 
  

---

## Page 186

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 186 
Sample #1k: MT518 Match Request Cancel (due to Match) Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1511 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000750337 Sender’s Message Reference Number 
:23G:CANC Cancel 
:98C::PREP//20030211075330 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information - [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information - Contraparty [[ID]] 
:20C::PROC//M0001570203 Contra [[Seller]] X-ref SIC 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH 
/RGDP98,56 
Trade Instruction Processing – Message Reason = due to Match, 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
– End of Message 
  

---

## Page 187

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 187 
Sample #1l: MT518 [[settlement]] Disposition Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1563 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000500684 Sender’s Message Reference Number 
:23G:NEWM New Message Advice 
:98C::PREP//20030211181500 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0001570203 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423008597 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0423008597 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC 
/SDSPTFTD/DDTE20030214 
/RGDP98,56 
Trade Instruction Processing – Message Reason = due to CMU 
RTTM Action / [[settlement]] Disposition = Trade for Trade / Delivery 
Date; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 

---

## Page 188

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 188 
Message Content Comments 
:16S:SETDET Optional Block End 
– End of Message 
 
 
Sample #1m: MT518 [[settlement]] Disposition Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1511 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000500677 Sender’s Message Reference Number 
:23G:NEWM New Message Advice 
:98C::PREP//20030211181500 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//02112003T00011 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423009016 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0423008597 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075258 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information - [[participant]] [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information - Contraparty [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 

---

## Page 189

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 189 
Message Content Comments 
:70E::TPRO//GSCC/MSGRGSAC 
/SDSPTFTD/DDTE20030214/RGDP98,56 
Trade Instruction Processing – Message Reason = due to 
CMU RTTM Action / [[settlement]] Disposition = Trade for 
Trade / Delivery Date; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
– End of Message 
 
  

---

## Page 190

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 190 
Part B – Regular Way Trade – Cancel 
Sample #1n: MT515 Client A Submits Cancel Sell to CMU RTTM (Pre-matching) 
Message Content Comments 
Message Header 
PW7326 CMU RTTM Assigned Password 
1563 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//10051FEB1103 Sender’s Message Reference Number 
:23G:CANC Cancel a Trade 
:98C::PREP//20030211075306 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0001570203 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Mandatory for Cancel Message 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423008597 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CANC Cancel Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02 
/RGDP98,56 
Trade Instruction Processing – Destination Indicator = CMU RTTM and 
MSRB Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 

---

## Page 191

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 191 
Message Content Comments 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
– End of Message 
 
  

---

## Page 192

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 192 
Sample #1o: MT518 Match Request Cancel (Due to Contra Action) Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1511 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250333 Sender’s Message Reference Number 
:23G:CANC Cancel Message Input 
:98C::PREP//20030211075307 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information - [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information - Contraparty [[ID]] 
:20C::PROC//M0001570203 Contra [[Seller]] X-ref 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRCOAC 
/RGDP98,56 
Trade Instruction Processing – Message Reason = due to contra action; 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
– End of Message 
 
  

---

## Page 193

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 193 
Part C – Regular Way Trade – DK 
Sample #1p: MT515 Client B Submits DK of Trade 
Message Content Comments 
 Message Header 
PW5263 CMU RTTM Assigned Password 
1511 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//02112003A0007 Sender’s Message Reference Number 
:23G:NEWM New message input 
:98C::PREP//20030211075414 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//NONREF SWIFT Mandatory Field 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/TDDK DK Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//M0001570203 Contra [[Seller]] X-ref 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
– End of Message 
 
  

---

## Page 194

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 194 
Sample #1q: MT518 DK Advice Sent to Client A 
Message Content Comments 
Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1563 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250198 Sender’s Message Reference Number 
:23G:NEWM New message input 
:98C::PREP//20030211075415 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0001570203 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423008597 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/NAFI DK Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = [[Buyer]]’s Contra’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DKRSE009 Trade Instruction Processing – DK Reason Code – E009 Bad Amount 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
– End of Message 
  

---

## Page 195

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 195 
Sample #1r: MT518 DK Remove Advice Sent to Client A 
Message Content Comments 
Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1563 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250308 Sender’s Message Reference Number 
:23G:NEWM New message input 
:98C::PREP//20030211075710 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0001570203 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423008597 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/DCCX DK Remove Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = [[Buyer]]’s Contra’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRDCTD 
/RGDP98,56 
Trade Instruction Processing – Message Reason Code – DCTD = 
Due to DK Remove 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
– End of Message 
  

---

## Page 196

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 196 
Part D – Regular Way Trade – Modify 
Sample 1s: MT515 Client A Submits Modify Sell Trade to CMU RTTM (Pre-matching) 
(Modified Fields: Quantity: From: 10,000 to: 100,000 Client XREF; From: M0001570203 to: M00Y1930203) 
Message Content Comments 
Message Header 
PW7326 CMU RTTM Assigned Password 
1563 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//10099FEB1103 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075327 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M00Y1930203 [[participant]] External Reference Number (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//M0001570203 [[participant]] External Reference Number (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423008597 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD102068,90 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/MDFC Modify Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/100000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02 
/RGDP98,56 
Trade Instruction Processing – Destination Indicator = CMU RTTM and MSRB 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 

---

## Page 197

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 197 
Message Content Comments 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD2068,90 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
– End of Message 
  

---

## Page 198

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 198 
Sample 1t: MT518 Match Request Modify Sent to Client B 
(Client A’s Modifications: Quantity: From: 10,000 to: 100,000 Client XREF; From: M0001570203 to: 
M00Y1930203) 
Message Content Comments 
Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1511 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250787 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075332 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade)` 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD102068,90 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CRQM Match Request Modify Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information - Contraparty [[ID]] 
:20C::PROC//M00Y1930203 Contra [[Seller]] X-ref (NEW) 
:70E::DECL//GSCC/PREVM0001570203 
/CORRFRSD 
Party = [[Seller]]’s previous external reference number and [[Seller]]’s 
Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/100000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD2068,90 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
– End of Message 
 
  

---

## Page 199

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 199 
Sample 1u: MT515 Client A Submits Modify Sell Trade to CMU RTTM (Post-matching) 
(Modified Fields: Client XREF; From: M0001570203 to: M00Y1930203) 
Message Content Comments 
Message Header 
PW7326 CMU RTTM Assigned Password 
1563 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//10099FEB1103 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075428 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M00Y1930203 [[participant]] External Reference Number (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//M0001570203 [[participant]] External Reference Number (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423008597 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0423008597 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/MDFC Modify Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02 
/RGDP98,56 
Trade Instruction Processing – Destination Indicator = CMU RTTM and 
MSRB Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 

---

## Page 200

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 200 
Message Content Comments 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
– End of Message 
  

---

## Page 201

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 201 
Part E – Regular Way Trade – Miscellaneous 
Sample 1v: MT518 Post-match Contra Trade Modification sent to Client B 
(Client A’s Modifications: Quantity: Client XREF; From: M0001570203 to: M00Y1930203)  
Message Content Comments 
Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1511 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250965 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075438 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0423008597 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade)` 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMDA Contra Trade Modification Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information - Contraparty [[ID]] 
:20C::PROC//M00Y1930203 Contra [[Seller]] X-ref (NEW) 
:70E::DECL//GSCC/PREVM0001570203 
/CORRFRSD 
Party = [[Seller]]’s previous external reference number and [[Seller]]’s 
Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
– End of Message 
  

---

## Page 202

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 202 
Sample #1w: MT518 Matched with Modifications sent to Client B 
(Money Difference of $0.51) 
Message Content Comments 
Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1511 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250962 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075328 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//02112003T00011 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423009016 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0423008597 CMU RTTM Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075258 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade)` 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10207,40 [[settlement]] Amount ([[settlement]] amount difference of $0.51) 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPM Match With Modifications Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information - Contraparty [[ID]] 
:20C::PROC//M0001570203 Contra [[Seller]] X-ref 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC 
/RGDP98,56 
Trade Instruction Processing / Message Reason = Due to CMU RTTM 
Action; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 

---

## Page 203

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 203 
Message Content Comments 
:19A::ACRU//USD207,40 Accrued Interest Amount (Difference) 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
End of Message 
  

---

## Page 204

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 204 
Sample #1x: MT515 Client B Submits Reversal to CMU RTTM (Reversal of BUY) 
Message Content Comments 
Message Header 
PW5263 CMU RTTM Assigned Password 
1511 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//02112003A0028 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075716 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//02112003T00011R [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075258 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record (Buy Reversal) 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1563 [[Buyer]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1511 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02 
/RVSL/RCTL02112003T00011/RGDP98,56 
Trade Instruction Processing – Destination Indicator = CMU RTTM 
and MSRB / Reversal of a Trade / Reversal Control #; Regulatory 
Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
End of Message 
 
  

---

## Page 205

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 205 
Sample 1y: MT518 Screen Input Trade Replay of Sell Trade (SITR) sent to Client A 
Message Content Comments 
Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1563 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021100000250371 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030211075328 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0001570203 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0423008597 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030211075250 Trade Date and Time 
:98A::SETT//20030214 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD10206,89 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/SITR Screen Input Trade Replay Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1511 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDAJ101 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORREJLD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1563 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRFRSD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/10000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/78764HAD6 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRYRAC/DEST01 
/DEST02/RGDP98,56 
Trade Instruction Processing – Message Reason due to [[participant]] Action / 
Destination Indicator = CMU RTTM and MSRB; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD206,89 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
– End of Message 
  

---

## Page 206

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 206 
Sample Trade 2: Municipal Bond (New Issue/Repriced) 
On February 6, 2003, Dealer Client 1571 sells New Issue Municipal Bond ([[CUSIP]] 529284VR9) to Dealer Client 
1514 at a yield of 4.63%. When the [[settlement]] Date is available the issue is repriced.  Client entered 2 
Extended [[settlement]] Days which instructs CMU RTTM that the trade should settle two business days after 
Issue Date. 
Field Description Client A – 1571 ([[Seller]]) Client B – 1514 ([[Buyer]]) 
Password PW8457 PW7861 
Sender [[ID]] 1571 1514 
SEME 000034MB02063 FEB06000364 
MAST T00023RT001 0206200301154W 
Preparation Date & Time 2/6/2003 14:36:33 2/6/2003 14:35:56 
Trade Date and Time 2/6/2003 14:35:01 2/6/2003 14:35:47 
[[settlement]] Date Post Reprice 2/17/2003 2/17/2003 
Price YIELD 4,63 YIELD 4,63 
Contract Amount 246560, 246560, 
Contra [[participant]] 1514 1571 
Contra Correspondent MRLE ELLY 
Contra Trader [[ID]]  TRDID4EAM 
[[participant]] Correspondent ELLY MRLE 
[[participant]] Capacity PRINCIPAL PRINCIPAL 
[[CUSIP]] 529284VR9 529284VR9 
PAR 250000, 250000, 
CMU RTTM Reference Number (TID) 0373011087 0373001348 
Accrued Interest 500, 500, 
Match Control Number 0373001348 0373001348 
Regulatory Dollar Price 101,34 101,34 
Extended [[settlement]] Days 2 2 
 
The following message samples for Trade #2 are all based on the scenario. 
•  2a.  MT515 Client B submits New Issue Buy Trade to CMU RTTM  
• 2b.  MT509 Trade Accepted sent to Client B 
•  2c.  MT509 Trade Rejected sent to Client B  
• 2d.  MT518 Match Request sent to Client A 
•  2e.  MT515 Client A submits New Issue Sell Trade to CMU RTTM  
• 2f. MT509 Trade Accepted sent to Client A 
•  2g. MT518 Match Request sent to Client B  
•  2h. MT509 Trade Matched sent to Client A  
• 2i.   MT509 Trade Matched sent to Client B 
•  2j. MT518 Match Request Cancel (due to Match) sent to Client A  
•  2k. MT518 Match Request Cancel (due to Match) sent to Client B  
• 2l.   MT518 Repricing sent to Client A 
•  2m. MT518 [[settlement]] Disposition sent to Client B  
• 2n.  MT 518 [[default]] Values Applied sent to Client B 
  

---

## Page 207

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 207 
Sample #2a: MT515 Client B Submits New Issue Buy Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PW7861 CMU RTTM Assigned Password 
1514 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//FEB06000364 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030206143556 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0206200301154W [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206143547 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/4,63 Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1514 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMRLE Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1571 [[Seller]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDTRDID4EAM [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRELLY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/250000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/529284VR9 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02 
/SDAD2/RGDP101,34 
Trade Instruction Processing – Destination Indicator = CMU 
RTTM and MSRB / [[settlement]] Date Adjustment = Distribution 
Date + 2; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
- End of Message 
  

---

## Page 208

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 208 
Sample #2b: MT509 Trade Accepted sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1514 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600001250158 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206143612 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0206200301154W [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//FEB06000364 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001348 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
  

---

## Page 209

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 209 
Sample #2c: MT509 Trade Rejected sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]]) 
509/000/GSCC Message Type 
1514 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600001250159 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206143612 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0203200301154W [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//FEB06000364 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//REJT Trade Input Rejected Status 
:16R:REAS Optional Repeat Block Start 
:24B::REJT/GSCC/E016 Reject Reason Code: E016 = Password Error 
:16S:REAS Optional Repeat Block End 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 210

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 210 
Sample #2d: MT518 Match Request sent to Client A 
Message Content Comments 
Message Header 
 CMU RTTM Assigned Password – blank filled on MT 518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1571 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//302060000325000
1 
Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030206143627 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206143547 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/4,63 Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1514 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//0206200301154W Contra [[Buyer]] X-Ref 
:70E::DECL//GSCC/CORRMRL
E 
Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1571 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDTRDI
D4EAM 
[[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRELLY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/250000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/529284VR9 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/SDAD2/RG
DP101,34 
Trade Instruction Processing – [[settlement]] Date Adjustment = Distribution Date + 2; 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 211

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 211 
Sample #2e: MT515 Client A Submits New Issue Sell Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PW8457 CMU RTTM Assigned Password 
1571 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//000034MB02063 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030206143633 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//T00023RT001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206143501 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/4,63 Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution–[[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1514 [[Buyer]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRMRLE Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1571 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRELLY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/250000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/529284VR9 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02/SDAD 
2/RGDP101,34 
Trade Instruction Processing – Destination Indicator = CMU RTTM and 
MSRB / [[settlement]] Date Adjustment = Distribution + 2; Regulatory 
Dollar Price 
:16S:CONFDET Mandatory Block End 
- End of Message 
 
  

---

## Page 212

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 212 
Sample #2f: MT509 Trade Accepted sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1571 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600002250233 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206143638 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//T00023RT001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//000034MB02063 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373011087 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
  

---

## Page 213

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 213 
Sample #2g: MT518 Match Request Sent to Client B 
Message Content Comments 
Message Header 
 CMU RTTM Assigned Password – blank filled on MT 518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1514 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600004750054 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030206143639 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206143501 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/4,63 Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1514 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMRLE Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1571 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//T00023RT001 Contra [[Seller]] X-Ref 
:70E::DECL//GSCC/CORRELLY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/250000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/529284VR9 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/SDAD2 
/RGDP101,34 
Trade Instruction Processing – [[settlement]] Date Adjustment = Distribution 
Date + 2 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16S:SETDET Optional Block End 
End of Message 
 
  

---

## Page 214

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 214 
Sample #2h: MT509 Trade Matched sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT 509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1571 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600003250028 Sender’s (Message Reference Number) 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206143640 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//T00023RT001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373011087 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20S::PROG//0206200301154W Contraparty External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0373001348 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 215

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 215 
Sample #2i: MT509 Trade Matched sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1514 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600001250163 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206143641 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0206200301154W [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001348 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//T00023RT001 Contraparty External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0373001348 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
  

---

## Page 216

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 216 
Sample #2j: MT518 Match Request Cancel (due to Match) sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1571 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600003250337 Sender’s Message Reference Number 
:23G:CANC Cancel Trade Advice 
:98C::PREP//20030206143659 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF Mandatory for Cancel Message 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206143547 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/4,63 Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1514 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//0206200301154W Contra [[Buyer]] X-Ref 
:70E::DECL//GSCC/CORRMRLE Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1571 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDTRDID4EAM [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRELLY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/250000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/529284VR9 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH/SDAD2 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to Match / 
[[settlement]] Date Adjustment = Distribution Date + 2; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
  

---

## Page 217

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 217 
Sample #2k: MT518 Match Request Cancel (due to Match) Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1514 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600001250374 Sender’s Message Reference Number 
:23G:CANC Cancel Trade Advice 
:98C::PREP//20030206143703 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S: LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206143501 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL4,63 Price type = Percent 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1514 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMRLE Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1571 [[Seller]] Information - Contraparty [[ID]] 
:20C::PROC//T00023RT001 Contra [[Seller]] X-Ref 
:70E::DECL//GSCC/CORRELLY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/250000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/529284VR9 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH/SDAD2 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to Match / 
[[settlement]] Date = Distribution Date + 2; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
  

---

## Page 218

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 218 
Sample #2l: MT518 Repricing Sent to Client A 
Message Content Comments 
Message Header CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1571 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600003250851 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030206203712 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Optional Repeat Block Start 
:20C::MAST//T00023RT001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Optional Repeat Block Start 
:20C::LIST//0373011087 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Optional Repeat Block Start 
:20C::COMM//0373001348 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206143501 Trade Date and Time 
:98A::SETT//20030217 [[settlement]] Date 
:90A::DEAL//YIEL/4,63 Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution–[[OTC]] Municipal 
:19A::SETT//USD246560, [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/YTPR Yield to Price Repricing 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1514 [[Buyer]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRMRLE Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1571 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRELLY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/250000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/529284VR9 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/SDAD2 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to CMU 
RTTM Action / Destination Indicator = CMU RTTM / [[settlement]] Date 
Adjustment = Distribution Date + 2; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD500, Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
End of Message 

---

## Page 219

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 219 
Sample #2m: MT518 [[settlement]] Disposition sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT 518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1514 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600001500773 Sender’s Message Reference Number 
:23G:NEWM New Message Advice 
:98C::PREP//20030211143713 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0206200301154W [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001348 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0373001348 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206143547 Trade Date and Time 
:98A::SETT//20030217 [[settlement]] Date 
:90A::DEAL//YIEL/4,63 Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD246560, [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1514 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMRLE Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1571 [[Seller]] Information - Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDTRDID4EAM [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRELLY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/250000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/529284VR9 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/SDAD2 
/SDSPTFTD/DDTE20030217/RGDP101,34 
Trade Instruction Processing – Message Reason = due to CMU 
RTTM Action / [[settlement]] Date Adjustment = Distribution Date + 
2 
/ [[settlement]] Disposition = Trade for Trade / Delivery Date = 
02/17/2003; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 

---

## Page 220

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 220 
Message Content Comments 
:19A::ACRU//USD500, Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET  Optional Block End 
End of Message 
  

---

## Page 221

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 221 
Sample 2n: MT518 [[default]] Values Applied Sent to Client B 
(CMU RTTM Security Record on File at time of Trade Entry) 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT 518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1514 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600004750079 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030206143636 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0206200301154W [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001348 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206143547 Trade Date and Time 
:98B::SETT//20030217 [[settlement]] Date 
:90A::DEAL//YIEL/4,63 Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD246560, [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/DFVA [[default]] Values Applied Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1514 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMRLE Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1571 [[Seller]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDTRDID4EAM [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRELLY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/250000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/529284VR9 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/SDAD2 
/RGDP101,34 
Trade Instruction Processing – Message Reason = Due to CMU RTTM 
Action / [[settlement]] Date Adjustment = Distribution Date + 2; Regulatory 
Dollar Price 
:16S:CONFDET Mandatory Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 222

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 222 
Sample Trade 3: Municipal Bond [[syndicate]] (Demand) Submission 
On February 10, 2003, [[syndicate]] Manager (Client 1555) sells 815M of New Issue Municipal Bond ([[CUSIP]] 
87971HBR4) to Dealer Client 1529 at a yield of 5%. The repriced contract amount was $887,702.08.  
Field Description Client A – 1555  
([[Seller]] - [[syndicate]] 
Manager) 
Client B – 1529  
([[Buyer]] - [[syndicate]] [[Member]]) 
Field [[Seller]] ([[syndicate]] Manager) [[Buyer]] ([[syndicate]] Target) 
Password PW6825 PW5438 
Sender [[ID]] 1555 1529 
SEME 000049SM02103 
000063SM02181 (Part D) 
TSEQ021003003 
MAST S00546MY019 SMY019REVA 
(Part D) 
30210TRDC475054 
3TS302100014 (Parts B and C) 
Preparation Date & Time 2/10/2003 08:16:43 2/10/2003 20:36:39 
Trade Date and Time 2/10/2003 08:15:51 SEE [[Seller]] TIME 2/10/2003 08:16:58 
(Parts B and C) 
[[settlement]] Date Post Reprice 2/19/2003 2/19/2003 
Price YIELD 5, YIELD 5, 
Contract Amount 887702,08 887702,08 
Contra [[participant]] 1529 1555 
Contra Correspondent ABCD WXYZ 
Contra Trader [[ID]] 86SMIT  
[[participant]] Correspondent WXYZ ABCD 
[[participant]] Capacity Principal Principal 
[[CUSIP]] 87971HBR4 87971HBR4 
PAR 815000, 815000, 
CMU RTTM Reference Number (TID) 0413002287 0413055962 
Accrued Interest 2139,38 2139,38 
Match Control Number 0413002287 0413002287 
  

---

## Page 223

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 223 
The following message samples for Trade 3 are all based on the scenario presented on the previous page. 
Part A - [[syndicate]] Manager (Client A) Submits 
•  3a. MT515 Client A ([[syndicate]] Manager) submits Sell trade to CMU RTTM  
• 3b. MT509 Trade Accepted sent to Client A 
• 3c.      MT518 Match Request sent to Client B 
•  3d. MT518 Locked-in Trade Advice sent to Client B  
• 3e. MT509 Trade Matched sent to Client A 
• 3f.       MT509 Trade Matched sent to Client B 
•  3g.   MT518 Match Request Cancel (due to Match) sent to Client B  
•  3h.    MT518 Match Request Cancel (due to Match) sent to Client A  
• 3i.       MT518 [[settlement]] Disposition sent to Client B 
Part B - [[syndicate]] [[Member]] (Client B) Submits Without Target Indicator 
•  3j. MT 515 Client B ([[syndicate]] [[Member]]) submits Buy trade to CMU RTTM (No Target Indicator)  
• 3k. MT 509 Trade Accepted sent to Client B 
• 3l.  MT518 Match Request sent to Client A  
•  3m. MT509 Trade Matched sent to Client A  
• 3n.      MT509 Trade Matched sent to Client B 
• 3o.      MT518 Trade Matched with Modifications sent to Client B 
•  3p. MT518 Match Request Cancel (due to match) sent to Client B  
• 3q. MT518 Match Request Cancel (due to match) sent to Client A 
Part C - [[syndicate]] [[Member]] (Client B) Submits with Target Indicator 
•  3r. MT 515 Client B ([[syndicate]] [[Member]]) submits Buy trade to CMU RTTM (with Target Indicator)  
• 3s. MT509 Trade Accepted sent to Client B 
• 3t. MT518 Match Request to Client A ([[syndicate]] Manager)  
• 3u. MT509 Trade Matched sent to Client A 
• 3v.      MT509 Trade Matched sent to Client B 
•  3w. MT518 Match Request Cancel (due to match) sent to Client B  
• 3x. MT518 Match Request Cancel (due to match) sent to Client A 
C.5 Part D - [[syndicate]] Manager (Client A) Submits Reversal 
• 3y.      MT515 Client A ([[syndicate]] Manager) submits Reversal to CMU RTTM (Reversal of Sell) 
  

---

## Page 224

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 224 
Part A - [[syndicate]] Manager (Client A) Submits 
Sample 3a: MT515 Client A ([[syndicate]] Manager) Submits Sell Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PW6825 CMU RTTM Assigned Password 
1555 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//000049SM02103 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030210081643 Date and Time of message preparation 
:22F::TRTR/GSCC/TRDC Demand Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//S00546MY019 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081551 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDID86SMIT [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02/ITYPS 
Y/RGDP101,34 
Trade Instruction Processing – Destination Indicator = CMU RTTM 
and MSRB / Issue Type = [[syndicate]]; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 225

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 225 
Sample #3b: MT509 Trade Accepted sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1555 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//302100000250459 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210081658 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//S00546MY019 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//000049SM02103 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413002287 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 226

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 226 
Sample #3c: MT518 Match Request Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000004750054 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030210081702 Date and Time of message preparation 
:22F::TRTR/GSCC/TRDC Demand Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081551 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID86SMIT [[Buyer]] [[participant]] Contact Narrative Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information - Contraparty [[ID]] 
:20C::PROC//S00546MY019 Contra [[Seller]] X-Ref 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/ITYPSY 
/RGDP101,34 
Trade Instruction Processing – Issue Type = [[syndicate]] Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16S:SETDET Optional Block End 
End of Message 
 
  

---

## Page 227

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 227 
Sample #3d: MT518 Locked-in Trade Advice Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000004750067 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030210203639 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//30210TRDC475054 Reference Generated by CMU RTTM on [[Buyer]]’s behalf 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413055962 CMU RTTM Reference Number for trade 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0413002287 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081551 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/LCTA Locked-in Trade Advice 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID86SMIT [[Buyer]] [[participant]] Contact Information – Trader [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information - Contraparty [[ID]] 
:20C::PROC//S00546MY019 Contra [[Seller]] X-Ref 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/IT
YPTS 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to CMU RTTM Action / 
Issue Type = Target [[syndicate]] 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16S:SETDET Optional Block End 
End of Message 
 
  

---

## Page 228

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 228 
Sample #3e: MT509 Trade Matched sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled MT 509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1555 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000000759853 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210203653 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//S00546MY019 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413002287 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//30210TRDC475054 Contraparty External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0413002287 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 229

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 229 
Sample #3f: MT509 Trade Matched sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled MT 509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000000759903 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210203654 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//30210TRDC475054 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413055962 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//S00546MY019 Contraparty External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0413002287 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
  

---

## Page 230

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 230 
Sample #3g: MT518 Match Request Cancel (due to Match) Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000002250005 Sender’s Message Reference Number 
:23G:CANC Cancel Trade Advice 
:98C::PREP//20030210203703 Date and Time of message preparation 
:22F::TRTR/GSCC/TRDC Demand Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S: LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081551 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID86SMIT [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//S00546MY019 Contra [[Seller]] X-Ref 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH/ITYPSY 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to Match / 
Issue Type = [[syndicate]] 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 231

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 231 
Sample #3h: MT518 Match Request Cancel (due to Match) Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1555 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000002500009 Sender’s Message Reference Number 
:23G:CANC Cancel Trade Advice 
:98C::PREP//20030210203704 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Demand Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S: LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081551 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//30210TRDC475054 Contra [[Buyer]] X-Ref 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH/ITYPTS 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to Match / 
Issue Type = Target [[syndicate]] 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 232

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 232 
Sample #3i: MT518 [[settlement]] Disposition Sent to Client B  
Message Content Comments 
Message Header CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021700002000099 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030217203513 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//30210TRDC475054 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413055962 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0413002287 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081551 Trade Date and Time 
:98A::SETT//20030219 [[settlement]] Date 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD887702,08 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/ 
SDSPTFTD/DDTE20030219/ITYPTS 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to CMU RTTM 
Action / [[settlement]] Disposition = Trade for Trade / Delivery Date = 
02/19/2003 / Issue Type = Target [[syndicate]] Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD2139,38 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
End of Message 

---

## Page 233

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 233 
Part B - [[syndicate]] [[Member]] (Client B) Submits Without Target Indicator 
Sample #3j: MT515 Client B ([[syndicate]] [[Member]]) Submits Buy Trade to CMU RTTM (No 
Target Indicator) 
Message Content Comments 
 Message Header 
PW5438 CMU RTTM Assigned Password 
1529 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//TSEQ021003003 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030210081704 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//3TS302100014 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081658 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information - Contraparty [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02 
/RGDP101,34 
Trade Instruction Processing – Destination Indicator = CMU RTTM and MSRB 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 234

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 234 
Sample #3k: MT509 Trade Accepted Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//302100001250954 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210081706 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//3TS302100014 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//TSEQ0210030003 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413055962 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 235

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 235 
Sample #3l: MT518 Match Request sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1555 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000003750045 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030210081707 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081658 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//3TS3021000014 Contra [[Buyer]] X-Ref 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
:16S:SETDET Optional Block End 
End of Message 
  

---

## Page 236

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 236 
Sample #3m: MT509 Trade Matched Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled MT 509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1555 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000004759308 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210203653 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//S00546MY019 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413002287 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::PROG//3TS302100014 Contraparty External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0413002287 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
  

---

## Page 237

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 237 
Sample #3n: MT509 Trade Matched sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled MT 509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000001750003 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210203654 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//3TS302100014 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413055962 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::PROG//S00546MY019 Contraparty External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0413002287 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
  

---

## Page 238

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 238 
Sample #3o: MT518 Matched With Modifications sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000002250961 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030210203659 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//3TS302100014 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413055962 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0413002287 CMU RTTM Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//2003021020081658 Trade Date and Time 
:98A::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPM Match With Modifications Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information - Contraparty [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/ITYPTS 
/RGDP101,34 
Trade Instruction Processing / Message Reason = Due to CMU 
RTTM Action / Issue Type = Target [[syndicate]] 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
  

---

## Page 239

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 239 
Sample #3p: MT518 Match Request Cancel (due to Match) sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000002250005 Sender’s Message Reference Number 
:23G:CANC Cancel Trade Advice 
:98C::PREP//20030210203703 Date and Time of message preparation 
:22F::TRTR/GSCC/TRDC Demand Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S: LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081551 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID86SMIT [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//S00546MY019 Contra [[Seller]] X-Ref 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH/ITYPSY 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to Match / 
Issue Type = [[syndicate]]; 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
  

---

## Page 240

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 240 
Sample #3q: MT518 Match Request Cancel (due to Match) sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1555 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000002500009 Sender’s Message Reference Number 
:23G:CANC Cancel Trade Advice 
:98C::PREP//20030210203704 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Demand Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S: LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081658 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//3TS302100014 Contra [[Buyer]] X-Ref 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to Match; Regulatory 
Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 241

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 241 
Part C - [[syndicate]] [[Member]] (Client B) Submits with Target Indicator 
Sample #3r: MT515 Client B ([[syndicate]] [[Member]]) Submits Buy Trade to CMU RTTM 
(with Target Indicator) 
Message Content Comments 
 Message Header 
PW5438 CMU RTTM Assigned Password 
1529 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//TSEQ021003003 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030210081704 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//3TS302100014 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081658 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02/ITYPTS 
/RGDP101,34 
Trade Instruction Processing – Destination Indicator = CMU 
RTTM and MSRB / Issue Type = Target [[syndicate]]; 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 242

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 242 
Sample #3s: MT509 Trade Accepted sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//302100000250188 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210081706 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//3TS302100014 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//TSEQ0210030003 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413055962 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 243

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 243 
Sample #3t: MT518 Match Request sent to Client A ([[syndicate]] Manager) 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1555 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000002750021 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//200302102081708 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081658 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price Type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//3TS302100014 Contra [[Buyer]] X-Ref 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/ITYPTS 
/RGDP101,34 
Trade Instruction Processing Narrative 
/ Issue Type = Target [[syndicate]]; Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16S:SETDET Optional Block End 
End of Message 
 
  

---

## Page 244

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 244 
Sample #3u: MT509 Trade Matched sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled MT 509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1555 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000004759308 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210081709 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//S00546MY019 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413002287 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::PROG//3TS302100014 Contraparty External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0413002287 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
 
End of Message 
 
  

---

## Page 245

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 245 
Sample #3v: MT509 Trade Matched sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled MT 509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000000750011 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210081710 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//3TS302100014 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0413055962 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::PROG//S00546MY019 Contraparty External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block 
:20C::COMM//0413002287 Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 246

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 246 
Sample #3w: MT518 Match Request Cancel (due to Match) sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1529 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000002250005 Sender’s Message Reference Number 
:23G:CANC Cancel Trade Advice 
:98C::PREP//20030210081715 Date and Time of message preparation 
:22F::TRTR/GSCC/TRDC Demand Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S: LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081551 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID86SMIT [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//S00546MY019 Contra [[Seller]] X-Ref 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH/ITYPSY 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to Match / 
Issue Type = [[syndicate]]; 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 247

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 247 
Sample #3x: MT518 Match Request Cancel (due to Match) sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1555 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3021000002500009 Sender’s Message Reference Number 
:23G:CANC Cancel Trade Advice 
:98C::PREP//20030210081716 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Demand Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S: LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030210081658 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1529 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//3TS302100014 Contra [[Buyer]] X-Ref 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1555 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH/ITYPTS 
/RGDP101,34 
Trade Instruction Processing – Message Reason = due to Match / 
Issue Type = Target [[syndicate]]; 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
  

---

## Page 248

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 248 
Part D - [[syndicate]] Manager (Client A) Submits Reversal 
Sample #3y: MT515 Client A ([[syndicate]] Manager) Submits Reversal to CMU RTTM 
(Reversal of Sell) 
Message Content Comments 
 Message Header 
PW6825 CMU RTTM Assigned Password 
1555 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//000063SM02181 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030218080105 Date and Time of message preparation 
:22F::TRTR/GSCC/TRDC Demand Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//SMY019REVA [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030218080101 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/5, Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1555 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRWXYZ Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1529 [[Seller]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRABCD Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/815000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/87971HBR4 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02/ITYPSY/RVSL/ 
RCTLS00546MY019 
/RGDP101,34 
Trade Instruction Processing – Destination Indicator = CMU 
RTTM and MSRB / Issue Type = [[syndicate]] / Message is a 
Reversal / Reversal Control # Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 249

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 249 
Sample Trade #4: Municipal Bond - Pending Status (Assigned, 
Removed or Trade Deleted) 
Client A submits a New Issue trade with no contract amount as [[settlement]] date is unknown. A Pending 
Status is assigned to the trade (sample 3c). If security information is later available, the Pending Status is 
removed (sample 3d); otherwise, the Trade is deleted as part of the purge process (sample 3e). 
Field Description Client A – 1595 ([[Seller]]) Client B – 1588 ([[Buyer]]) 
Password PW8433  
Sender [[ID]] 1595  
SEME W0019702062003AS  
MAST 0373065637  
Preparation Date & Time 2/6/2003 09:02:25 2/6/2003 09:02:26 
Trade Date And Time 2/6/2003 09:02:07 2/6/2003 09:02:13 
[[settlement]] Date Post Reprice   
Price YIELD 4,85 YIELD 4,85 
Contra [[participant]] 1588 1595 
Contra Correspondent APLL ZZTP 
Contra Trader [[ID]] 1TRD  
[[participant]] Correspondent ZZTP APLL 
[[participant]] Capacity PRIN  
[[CUSIP]] 040677AV8 040677AV8 
PAR 120000, 120000, 
CMU RTTM Reference Number (TID) 0373001353 03730001444 
Accrued Interest   
Match Control Number   
 
The following message samples for Trade #4 are all based on the scenario presented on the previous page.  
• 4a. MT515 Client A submits New Issue Sell Trade to CMU RTTM 4b. MT509 Trade Accepted sent to 
Client A 
•  4c. MT509 Pending Status Assigned sent to Client A  
• 4d. MT509 Pending Status Removed sent to Client A 
• 4e. MT509 Trade Deleted due to Pending sent to Client A 
  

---

## Page 250

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 250 
Sample #4a: MT515 Client A Submits New Issue Sell Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PW8433 CMU RTTM Assigned Password 
1595 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//W0019702062003AS Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030206090225 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0373065637 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206090207 Trade Date and Time 
:98B::SETT//WISS [[settlement]] Date Not Yet Known 
:90A::DEAL//YIEL/4,85 Price type = Yield 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1588 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDID1TRD [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRAPLL Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1595 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRZZTP Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/120000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/040677AV8 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02 
/RGDP101,34 
Trade Instruction Processing – Destination Indicator CMU RTTM and MSRB 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 251

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 251 
Sample #4b: MT509 Trade Accepted sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1595 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600000250778 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206090230 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0373065637 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//W0019702062003AS Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001353 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
Sample #4c: MT509 Pending Status Assigned sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1595 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600000250785 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206090231 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0373065637 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001353 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/ASPE Pending Status Assigned 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
  

---

## Page 252

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 252 
Sample #4d: MT509 Pending Status Removed sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1595 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600000250788 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206200030 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0373065637 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001353 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/RVPE Trade Input Pending Status Removed 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
Sample #4e: MT509 Trade Deleted due to Pending Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1595 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600000250788 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206200030 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0373065637 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001353 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/DEPE Trade Input Deleted (Due to Pending) 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
  

---

## Page 253

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 253 
Sample Trade #5: Municipal Bond - Memo Status (Assigned, Removed 
or Trade Deleted) 
Client B submits a final money New Issue Municipal Buy trade with a Contract Amount of $118,560.17, and a 
[[settlement]] Date of 02/12/2003. The trade is placed in Memo Status. 
Field Description Client A – 1595 ([[Seller]]) Client B – 1588 ([[Buyer]]) 
Password  PW8987 
Sender [[ID]]  1588 
SEME  S02062003000354N 
MAST 0373065637 NI006480373 
Preparation Date & Time 2/6/2003 09:02:25 2/6/2003 09:02:26 
Trade Date And Time 2/6/2003 09:02:07 2/6/2003 09:02:13 
[[settlement]] Date 2/12/2003 2/12/2003 
Price 0, 0, 
Contract Amount 118560,17 118560,17 
Contra [[participant]] 1588 1595 
Contra Correspondent APLL ZZTP 
Contra Trader [[ID]] 1TRD  
[[participant]] Correspondent ZZTP APLL 
[[participant]] Capacity PRIN PRIN 
[[CUSIP]] 040677AV8 040677AV8 
PAR 120000, 120000, 
CMU RTTM Reference Number (TID) 0373001353 0373001444 
Accrued Interest 174,17 174,17 
Match Control Number   
 
The following message samples for Trade #5 are all based on the scenario presented on the previous page.  
•  5a. MT515 Client B submits New Issue Buy Trade to CMU RTTM  
• 5b. MT509 Trade Accepted sent to Client B 
•  5c. MT509 Memo Status Assigned sent to Client B  
• 5d. MT509 Memo Status Removed sent to Client B 
• 5e. MT509 Trade Deleted due to Memo sent to Client B 
• 5f. MT509 Trade Deleted (due to Security Detail Differences) sent to Client B 
  

---

## Page 254

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 254 
Sample #5a: MT515 Client B Submits New Issue Buy Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PW8987 CMU RTTM Assigned Password 
1588 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//S02062003000354N Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030206090226 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//NI006480373 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030206090213 Trade Date and Time 
:98A::SETT//20030212 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero Indicates final money trade) 
:94B::TRAD/GSCC/OTMU Place of Trade/Market of Execution – [[OTC]] Municipal 
:19A::SETT//USD118560,17 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1588 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRAPLL Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1595 [[Seller]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRZZTP Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/120000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/040677AV8 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/DEST02/YIEL4,85 
/RGDP101,34 
Trade Instruction Processing – Destination Indicator CMU 
RTTM and MSRB, and Yield 
Regulatory Dollar Price 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Start of Optional Sequence 
:22F::SETR//RPTO [[settlement]] Indicator – Reporting Only 
:16R:AMT Repeat Block Start 
:19A::ACRU//USD174,17 Accrued Interest 
:16S:AMT End of Block 
:16S:SETSET End of Block 
End of Message 
 
  

---

## Page 255

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 255 
MT509 Trade Accepted Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1588 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600000500886 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206090230 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//NI006480373 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//S02062003000354N Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001444 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 256

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 256 
MT509 Memo Status Assigned Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1588 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600000250785 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206090231 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//NI006480373 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001444 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/ASME Memo Status Assigned 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
MT509 Memo Status Removed sent to Client B  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1588 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600000250788 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206200030 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//NI006480373 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001444 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/RVME Memo Status Removed 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 257

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 257 
Sample #5e: MT509 Trade Deleted due to Memo Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1588 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600000250788 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030210200030 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//NI006480373 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001444 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/DEME Trade Input Deleted (Due to Memo) 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
Sample #5f: MT509 Trade Deleted (due to Security Detail Differences) Sent to Client B 
Message Content Comments 
Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1588 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020600000250788 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030206200030 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//NI006480373 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0373001444 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/DESD Trade Input Deleted (Due to Security Detail Difference) 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 258

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 258 
Sample Trade #6: Corporate Bond - Regular Way Trade 
On January 30, 2003, Dealer Client 1410 sells Regular Way Corporate Bond ([[CUSIP]] 00130HAP0) at a 
contract amount of $12,726.11 to Dealer Client 1400. 
Field Description Client A – 1410 ([[Seller]]) Client B – 1400 ([[Buyer]]) 
Password PM4657 PM1234 
Sender [[ID]] 1410 1400 
SEME TSEQ00122013003 01302003SEQ01 
MAST REF01300001 0301300001 
Preparation Date & Time 1/30/2003 10:58:17 1/30/2003 10:56:16 
Trade Date And Time 1/30/2003 10:58:06 1/30/2003 10:56:06 
[[settlement]] Date 2/4/2003 2/4/2003 
Price 0 (Final Money Trade) 0 (Final Money Trade) 
Contract Amount 12726,11 12726,11 
Contra [[participant]] 1400 1410 
Contra Correspondent SAMP TULL 
Contra Trader [[ID]]  TRDID00200 
[[participant]] Correspondent TULL SAMP 
[[participant]] Capacity PRIN PRIN 
[[CUSIP]] 00130HAP0 00130HAP0 
PAR 20000, 20000, 
CMU RTTM Reference Number (TID) 0303012225 0303010005 
Accrued Interest 151,11 151,11 
Match Control Number 0303010005 0303010005 
 

---

## Page 259

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 259 
Sample Trade #6: Corporate Bond - Regular Way Trade 
The following message samples for Trade #6 are all based on the scenario presented on the previous page.  
Part A - Regular Way Trade Match 
•  6a. MT515 Client B submits Buy Trade to CMU RTTM  
• 6b. MT509 Trade Accepted sent to Client B 
•  6c. MT509 Trade Rejected sent to Client B  
• 6d. MT518 Match Request sent to Client A 
•  6e. MT518 Screen Input Trade Replay (Instruct) sent to Client A  
• 6f. MT518 Match Request sent to Client B 
•  6g. MT509 Trade Matched sent to Client B  
• 6h. MT509 Trade Matched sent to Client A 
•  6i. MT518 Match Request Cancel (due to Match) sent to Client B  
•  6j. MT518 Match Request Cancel (due to Match) sent to Client A  
• 6k. MT518 [[settlement]] Disposition sent to Client B 
• 6l.  MT518 [[settlement]] Disposition sent to Client A 
Part B - Regular Way Trade – Unmatched 
• 6m.     MT509 Deleted Unmatched Transaction sent to Client B 
• 6n.      MT515 Client A submits Pre-Match Cancel of Sell Trade to CMU RTTM 
Part C - Regular Way Trade Reversal 
• 6o.      MT515 Client A submits Reversal to CMU RTTM (Reversal of Sell) 
  

---

## Page 260

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 260 
Part A - Regular Way Trade Match 
Sample #6a MT515 Client B Submits Buy Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PM1234 CMU RTTM Assigned Password 
1400 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//01302003SEQ01 Sender’s Message Reference Number 
:23G:NEWM New Trade Input 
:98C::PREP//20030130105616 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0301300001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105606 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDTRDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
End of Message 
 
  

---

## Page 261

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 261 
Sample #6b. MT509 Trade Accepted sent to Client B  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000250005 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130105618 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0301300001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//01302003SEQ01 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303010005 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
 
  

---

## Page 262

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 262 
Sample #6c. MT509 Trade Rejected sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000250015 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130105620 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0301300001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//01302003SEQ01 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//REJT Trade Input Rejected Status 
:16R:REAS Optional Repeat Block Start 
:24B::REJT/GSCC/E999 Reject Reason Code: E999 = Other Bad Data 
:16S:REAS Optional Repeat Block End 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
End of Message 
  

---

## Page 263

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 263 
Sample #6d. MT518 Match Request sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000750235 Sender’s Message Reference Number 
:23G:NEWM New Message Advice 
:98C::PREP//20030130105624 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105606 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//0301300001 [[Buyer]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDTRDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 264

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 264 
Sample #6e. MT518 Screen Input Trade Replay (Instruct) sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – Blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000750375 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030130105824 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//REF01300001 Message Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303012225 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105806 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/SITR Screen Input Trade Replay 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 
 
  

---

## Page 265

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 265 
Sample #6f: MT518 Match Request sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000001250025 Sender’s Message Reference Number 
:23G:NEWM New Message Advice 
:98C::PREP//20030130105834 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105806 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//REF01300001 [[Seller]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
 
  

---

## Page 266

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 266 
Sample #6g: MT509 Trade Matched sent to Client B 
  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000250145 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130105916 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0301300001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303010005 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//REF01300001 Contraparty External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0303010005 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 

---

## Page 267

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 267 
Sample #6h: MT509 Trade Matched sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000002250125 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130105916 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//REF01300001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303012225 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//0301300001 Contra External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0303010005 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 268

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 268 
Sample #6i. MT518 Match Request Cancel (due to Match) sent to Client B  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000003250055 Sender’s Message Reference Number 
:23G:CANC Cancel Instruction 
:98C::PREP//20030130105926 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Mandatory Field 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105806 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//REF01300001 [[Seller]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing – Message Reason = Due to Match 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
 
  

---

## Page 269

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 269 
Sample #6j. MT518 Match Request Cancel (due to Match) sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000003250455 Sender’s Message Reference Number 
:23G:CANC Cancel Instruction 
:98C::PREP//20030130105924 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Mandatory Field 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105606 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//0301300001 [[Buyer]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDTRDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing – Message Reason = Due to Match 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 270

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 270 
Sample #6k. MT518 [[settlement]] Disposition sent to Client B  
Message Content Comments 
Message Header CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000003250035 Sender’s Message Reference Number 
:23G:NEWM New Message Advice 
:98C::PREP//20030130181500 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0301300001 Master Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//0303010005 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//0303010005 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105606 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money 
trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] 
Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – Contraparty [[ID]] 
:70E::PACO//GSCC/TDIDTRDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/SDSPCNSE/DDTE2 0030204 Trade Instruction Processing – [[settlement]] 
Disposition / Message Reason = due to CMU 
RTTM Action / [[CNS]] Eligible / Delivery Date 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 

---

## Page 271

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 271 
Message Content Comments 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 272

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 272 
Sample #6l. MT518 [[settlement]] Disposition sent to Client A 
Message Content Comments 
Message Header CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC  Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000003250625 Sender’s Message Reference Number 
:23G:NEWM New Message Advice 
:98C::PREP//20030130181500 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Repeat Block Start 
:20C::MAST//REF01300001 Master Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//0303012225 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//0303010005 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105806 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/SDSPCNSE/DDTE 
20030204 
Trade Instruction Processing – [[settlement]] Disposition / 
Message Reason = due to CMU RTTM Action / [[CNS]] Eligible / 
Delivery Date 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 

---

## Page 273

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 273 
Part B - Regular Way Trade – Unmatched  
Sample #6m. MT509 Deleted Unmatched Transaction sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3020300003250116 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030203203514 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//0301300001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303010005 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//DELE Deleted Unmatched Transaction Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
  

---

## Page 274

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 274 
Sample #6n. MT515 Client A submits Pre-Match Cancel of Sell Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PM4657 CMU RTTM Assigned Password 
1410 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//TSEQ00144713003 Sender’s Message Reference Number 
:23G:CANC Cancel Message 
:98C::PREP//20030130105901 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//REF1300001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Mandatory Field for Cancel Records 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303012225 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105806 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CANC Cancel Message 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator = CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 

---

## Page 275

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 275 
Part C - Regular Way Trade Reversal 
Sample #6o: MT515 Client A submits Reversal to CMU RTTM (Reversal of Sell) 
Message Content Comments 
 Message Header 
PM4657 CMU RTTM Assigned Password 
1410 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//TSEQ00784013103 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//2003013112621 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//REF01300001REVB [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130112536 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1410 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1400 [[Seller]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/RVSL/ 
RCTLREF01300001 
Trade Instruction Processing – Destination Indicator = CMU RTTM / Trade 
Reversal Indicator = RVSL / Reversal Control Number 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
 

---

## Page 276

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 276 
Sample Trade #7: Corporate Bond Regular Way (Modify and Match) 
On January 31, 2003, Dealer Client 1401 sells Regular Way Corporate Bond ([[CUSIP]] 001957AV1) at a contract 
amount of $15,197.50 to Dealer Client 1411. Dealer Client 1401 submits an Instruct record to CMU RTTM with 
incorrect money and later submits a Modify record to change the amount fields. Post matching Client 1411 
submits a modification changing the internal reference number. 
Field Description Client A – 1401 ([[Seller]]) Client B – 1411 ([[Buyer]]) 
Password PM4321 PM4567 
Sender [[ID]] 1401 1411 
SEME NS20030131SE001 00114031SQ 
MAST MOR013103T001 (old) 
MOR013103T002 (new) 
C0000601312003N (old) 
M0000601312003A (new) 
Preparation Date & Time 1/31/2003 11:05:30 1/31/2003 11:05:55 
Trade Date And Time 1/31/2003 11:05:25 1/31/2003 11:05:49 
[[settlement]] Date 2/5/2003 2/5/2003 
Price 0, (Final Money Trade) 0, (Final Money Trade) 
Contract Amount 18237, 
15197,50 (Modified amt) 
15197,50 
Contra [[participant]] 1411 1401 
Contra Correspondent HOME MOST 
Contra Trader [[ID]] 00054  
[[participant]] Correspondent MOST HOME 
[[participant]] Capacity PRIN PRIN 
[[CUSIP]] 001957AV1 001957AV1 
PAR 18000, 
15000, (modified par) 
15000, 
CMU RTTM Reference Number (TID) 0313003004 0313003506 
Accrued Interest 417, 
347,50 (Modified Int) 
347,50 
Match Control Number 0313003004 0313003004 
 
  

---

## Page 277

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 277 
The following message samples for Trade #7 are all based on the scenario presented on the previous 
page. 
Part A - Trade Modify and Trade Match 
• 7a. MT515 Client A Submits Sell Trade to CMU RTTM  
• 7b. MT509 Trade Accepted sent to Client A 
• 7c. MT509 Trade Rejected sent to Client A 7d. MT518 Match Request sent to Client B 
• 7e. MT515 Client B submits Buy Trade to CMU RTTM 7f. MT518 Match Request sent to Client A 
• 7g. MT515 Client A submits a Trade Modification to CMU RTTM 7h. MT509 Modify Accepted sent to 
Client A 
• 7i. MT509 Modify Rejected sent to Client A 
• 7j. MT518 Match Request Modify sent to Client B 7k. MT509 Modify Processed sent to Client A 
• 7l. MT509 Trade Matched sent to Client A 7m. MT509 Trade Matched sent to Client B 
• 7n.  MT518 Match Request Cancel (due to Match) sent to Client A 7o.   MT518 Match Request Cancel 
(due to Match) sent to Client B 7p.      MT518 [[settlement]] Disposition sent to Client A 
• 7q.  MT518 [[settlement]] Disposition sent to Client B 
Part B - Post Matching Modification of Internal Reference Number 
•  7r. MT515 Client B submits a Trade Modification (Post-Matching) to CMU RTTM  
• 7s. MT518 Post Match Contra Trade Modification sent to Client A 
  

---

## Page 278

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 278 
Part A - Trade Modify and Trade Match 
Sample #7a. MT515 Client A Submits Sell Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PM4321 CMU RTTM Assigned Password 
1401 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//NS20030131SE001 Sender’s Message Reference Number 
:23G:NEWM New Message Input 
:98C::PREP//20030131110530 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//MOR013103T001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110525 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD18237, [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDID00054 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/18000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD417, Accrued Interest Amount 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 279

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 279 
Sample #7b. MT509 Trade Accepted sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1401 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100000500004 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030131110545 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//MOR013103T001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//NS20030131SE001 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0313003004 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
  

---

## Page 280

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 280 
Sample #7c. MT509 Trade Rejected sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1401 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100000500004 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030131110545 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//MOR013103T001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//NS20030131SE001 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//REJT Trade Input Rejected Status 
:16R:REAS Optional Block Start 
:24B::REJT/GSCC/E999 Reject Reason Code: E999 = Other Bad Data 
:16S:REAS Optional Repeat Block End 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 281

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 281 
7d. MT518 Match Request sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1411 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100000750009 Sender’s Message Reference Number 
:23G:NEWM New Message Advice 
:98C::PREP//20030131110546 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110525 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD18237, [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID00054 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//MOR013103T001 [[Seller]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/18000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD417, Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 282

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 282 
7e. MT515 Client B submits Buy Trade to CMU RTTM 
Message Content Comments 
 Message Header 
PM4567 CMU RTTM Assigned Password 
1411 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//00114031SQ Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030131110555 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//C0000601312003N [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110549 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final Money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
  

---

## Page 283

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 283 
7f. MT518 Match Request sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1401 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100000500044 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030131110601 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110549 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//C0000601312003N [[Buyer]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 284

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 284 
7g. MT515 Client A submits a Trade Modification to CMU RTTM 
Message Content Comments 
 Message Header 
PM4321 CMU RTTM Assigned Password 
1401 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//NS20030131SE007 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030131110720 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//MOR013103T002 [[participant]] External Reference Number (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//MOR013103T001 [[participant]] Previous External Reference (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0313003004 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110525 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount (field modified) 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/MDFC Modify Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDID00054 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) (field modified) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount (field modified) 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
End of Message 

---

## Page 285

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 285 
7h. MT509 Modify Accepted sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1401 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100001000127 Sender’s ([[NSCC]]) Message Reference 
:23G:INST Message Function (for Instruction or Modify) 
:98C::PREP//20030131110728 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//MOR013103T002 [[participant]] External Reference (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//MOR013103T001 Previous Reference No. (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//NS20030131SE007 Related Reference (client’s SEME from MT515 Modify Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0313003004 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/MODA Trade Modify Accepted 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 286

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 286 
7i. MT509 Modify Rejected sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]]) 
509/000/GSCC Message Type 
1401 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100001000127 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030131110730 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//MOR013103T002 [[participant]] External Reference (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//MOR013103T001 Previous Reference No. (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//NS20030131SE007 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0313003004 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Start Status Block 
:25D:IPRC//REJT Trade Input Rejected Status 
:16R:REAS Optional Repeat Block Start 
:24B::REJT/GSCC/E030 Reject Reason Code: E030 = Trade not in same state 
:70D::REAS//GSCC/MDRJ Message Type: Modify Rejected 
:16S:REAS Optional Repeat Block End 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 287

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 287 
7j. MT518 Match Request Modify sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1411 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100002000931 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030131110729 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110525 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CRQM Match Request Modify Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID00054 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//MOR013103T002 [[Seller]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/PREVMOR013103T001/ 
CORRMOST 
Party = [[Seller]]’s previous reference number and Correspondent 
Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRCOAC Message Reason – Due to Contra Action 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 288

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 288 
7k. MT509 Modify Processed sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1401 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100001000328 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030131110730 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//MOR013103T002 [[participant]] External Reference Number (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//MOR013103T001 Previous Reference No. (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0313003004 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/MODP Trade Modification Processed 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
  

---

## Page 289

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 289 
7l. MT509 Trade Matched sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1401 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100000750944 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030131110732 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//MOR013103T002 [[participant]] External Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0313003004 CMU RTTM Assigned Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//C0000601312003N Contra External Reference Number (of trade matched against client trade) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0313003004 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 290

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 290 
7m. MT509 Trade Matched sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1411 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100003500945 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030131110733 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//C0000601312003N [[participant]] External Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0313003506 CMU RTTM Assigned Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//MOR013103T002 Contra External Reference Number (of trade matched against client trade) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0313003004 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 291

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 291 
7n. MT518 Match Request Cancel (due to Match) sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1401 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100003250109 Sender’s Message Reference Number 
:23G:CANC Cancel Record 
:98C::PREP//20030131110735 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Mandatory Field for Cancel Records 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110549 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//C0000601312003N [[Buyer]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing – Message Reason = due to Match 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 292

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 292 
7o. MT518 Match Request Cancel (due to Match) sent to Client B  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1411 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100000750975 Sender’s Message Reference Number 
:23G:CANC Cancel Record 
:98C::PREP//20030131110736 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Mandatory Field for Cancel Records 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110525 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID00054 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//MOR013103T002 [[Seller]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing – Message Reason = due to Match 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 293

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 293 
7p. MT518 [[settlement]] Disposition Sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1401 Receiver [[ID]] ([[NSCC]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100000751002 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030131203803 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//MOR013103T002 Master Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//0313003004 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//0313003004 CMU RTTM Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110525 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDID00054 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/SDSPCNSE 
/DDTE20030205 
Trade Instruction Processing – Message Reason = due to 
CMU RTTM Action / [[settlement]] through [[CNS]] / Delivery Date 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount 
:16S:AMT Optional Block End 

---

## Page 294

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 294 
Message Content Comments 
:16S:SETDET Optional Block End 
- End of Message 
 
7q. MT518 [[settlement]] Disposition Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1411 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100000750986 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030131203804 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//C0000601312003N Master Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//0313003506 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//0313003004 CMU RTTM Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110549 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/SDSPCNSE 
/DDTE20030205 
Trade Instruction Processing – Message Reason = due to CMU 
RTTM Action / [[settlement]] through [[CNS]] / Delivery Date 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 

---

## Page 295

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 295 
Message Content Comments 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 296

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 296 
Part B - Post Matching Modification of Internal Reference Number 
7r. MT515 Client B Submits a Trade Modification (Post-Matching) to CMU RTTM  
Message Content Comments 
 Message Header 
PM4567 CMU RTTM Assigned Password 
1411 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//01003031SQ Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030131110741 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0000601312003A [[participant]] External Reference Number (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//C0000601312003N [[participant]] Previous External Reference (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0313003506 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110549 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/MDFC Modify Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRHOME Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – Contraparty [[ID]] 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount 
:16S:AMT Block End 

---

## Page 297

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 297 
Message Content Comments 
:16S:SETDET Optional Block End 
- End of Message 
 
7s. MT518 Post Match Contra Trade Modification Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1401 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013100001000614 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030131110743 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0313003004 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030131110549 Trade Date and Time 
:98A::SETT//20030205 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD15197,50 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMDA Post Match Contra Trade Modification Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1411 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//M0000601312003A [[Buyer]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRHOME/PREVC0000601312003N Party = MPID of [[Buyer]]’s Correspondent Firm / [[Buyer]]’s Previous 
Reference Number 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1401 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRMOST Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/15000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/001957AV1 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRCOAC Message Reason – Due to Contra Action 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD347,50 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
End of Message 
  

---

## Page 298

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 298 
Sample Trade #8: Corporate Bond Regular Way DK Processing 
A Regular Way Corporate Buy Trade is submitted to CMU RTTM by Dealer Client 1400. Client 1410 DK's 
the trade. If Client 1410 does nothing, the trade is administratively deleted. However, Client 1400 can 
modify its trade, or Client 1410 may choose to remove the DK. 
Field Description Client A – 1410 ([[Seller]]) DK’s 
Transaction 
Client B – 1400 ([[Buyer]]) 
Submitter 
Password PM4657 PM1234 
Sender [[ID]] 1410 1400 
SEME Q0015301302003NS NS01302003SE001 
MAST  1400T0001 (Modify – 1400T0116) 
Preparation Date & Time  1/30/2003 10:15:20 
Trade Date and Time  1/30/2003 10:15:07 
[[settlement]] Date  2/4/2003 
Price  0 (Final Money Trade) 
Contract Amount  12726,11 
Contra [[participant]]  1410 
Contra Correspondent  TULL 
(Modify – AUTI) 
Contra Trader [[ID]]  00200 
[[participant]] Correspondent  SAMP 
[[participant]] Capacity  PRIN 
[[CUSIP]]  00130HAP0 
PAR  20000, 
CMU RTTM Reference Number (TID)  0303040506 
Accrued Interest  151,11 
Match Control Number  0303010005 
  

---

## Page 299

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 299 
The following message samples for Trade #8 are all based on the scenario presented on the previous 
page. 
•  8a. MT515 Client B submits Buy Trade to CMU RTTM  
• 8b. MT509 Trade Accepted sent to Client B 
• 8c. MT518 Match Request sent to Client A 
Part A - DK and Delete 
•  8d. MT515 Client A submits DK of Client B's Trade to CMU RTTM  
• 8e. MT509 DK Accepted sent to Client A 
• 8f. MT509 DK Rejected sent to Client A 
• 8g. MT518 DK Advice sent to Client B 
•  8h. MT518 Match Request Cancel (due to DK) sent to Client A  
• 8i. MT509 DK Processed sent to Client A 
• 8j. MT509 Trade Deleted (due to DK) sent to Client B 
Part B - DK and Modify 
•  8k. MT515 Client B submits Modify of Trade to CMU RTTM  
• 8l. MT509 Modify Accepted sent to Client B 
•  8m. MT518 Match Request (due to Contra Action) sent to Client A  
• 8n. MT509 Modify Processed sent to Client B 
Part C - DK Remove 
• 8o: Client A enters a DK Remove through the screen (no message sample)  
• 8p: MT518 DK Remove Advice sent to Client B 
• 8q. MT518 Match Request (due to DK Remove) sent to Client A 
  

---

## Page 300

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 300 
8a. MT515 Client B Submits Buy Trade to CMU RTTM  
Message Content Comments 
 Message Header 
PM1234 CMU RTTM Assigned Password 
1400 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//NS01302003SE001 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030130101520 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//1400T0001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130101507 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
  

---

## Page 301

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 301 
8b. MT509 Trade Accepted sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000750022 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130101525 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//1400T0001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//NS01302003SE001 Related Reference (client’s SEME from MT515 Instruct Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303040506 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 302

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 302 
8c. MT518 Match Request Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000001750724 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030130101528 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130101507 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//1400T0001 [[Buyer]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 303

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 303 
Part A - DK and Delete 
8d. MT515 Client A Submits DK of Client B's Trade to CMU RTTM  
Message Content Comments 
 Message Header 
PM4657 CMU RTTM Assigned Password 
1410 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//Q0015301302003NS Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030130101628 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//NONREF [[participant]] External Reference Number (SWIFT Mandatory Field - 
[[default]] Value “NONREF” for DK Records) 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130101507 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/TDDK DK Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//1400T0001 Contraparty ([[Buyer]]’s) External Reference Number 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DKRSE998/DEST01 Trade Instruction Processing – DK Reason = E998 (Trade not found) / 
Destination Indicator = CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
  

---

## Page 304

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 304 
8e. MT509 DK Accepted Sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000001750652 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130101648 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//Q0015301302003NS Related Reference (client’s SEME from MT515 Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//1400T0001 Contraparty’s External Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/PADK DK Accepted 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
8f. MT509 DK Rejected sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000003750822 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130101641 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//Q0015301302003NS Related Reference (client’s SEME from MT515 DK Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//1400T0001 Contraparty’s External Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC//REJT Instruct Rejected Status 
:16R:REAS Mandatory Block Start 
:24B::REJT/GSCC/E999 Reject Reason Code: E999 – Other Bad Data 
:70D::REAS//GSCC/DKRJ Reject Reason Narrative – DK Rejected 
:16S:REAS Mandatory Block End 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 305

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 305 
8g. MT518 DK Advice Sent to Client B  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000003750932 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030130101728 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//1400T0001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303040506 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130101507 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/NAFI DK Advice 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DKRSE998 Trade Instruction Processing – DK Reason = E998 (Trade Not Found) 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 306

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 306 
8h. MT518 Match Request Cancel (due to DK) sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000001500092 Sender’s Message Reference Number 
:23G:CANC Cancel Message 
:98C::PREP//20030130101729 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Repeat Block Start 
:20C::PREV//NONREF SWIFT mandatory for Cancel Message 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130101507 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//1400T0001 [[Buyer]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRTULL Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRDKTD Trade Instruction Processing – Message Reason = due to DK 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 307

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 307 
8i. MT509 DK Processed Sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000002250712 Sender’s (CMU RTTM) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130101730 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//1400T0001 Contraparty’s External Reference No. 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/DPPR DK Processed 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
8j. MT509 Trade Deleted (due to DK) sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000500085 Sender’s ([[NSCC]]) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130201528 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//1400T0001 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303040506 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/DEDK Deleted due to DK Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 308

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 308 
Part B - DK and Modify 
8k. MT515 Client B Submits Modify of Trade to CMU RTTM  
Message Content Comments 
 Message Header 
PM1234 CMU RTTM Assigned Password 
1400 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//NS01302003SE128 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030130101820 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//1400T0116 [[participant]] External Reference Number (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//1400T0001 [[participant]] Previous External Reference Number (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303040506 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130101507 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/MDFC Modify Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRAUTI Party = MPID of [[Seller]]’s Correspondent Firm (NEW) 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator CMU RTTM 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 

---

## Page 309

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 309 
Message Content Comments 
:16S:AMT Block End 
:16S:SETDET Block End 
- End of Message 
 
8l. MT509 Modify Accepted Sent to Client B  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000003250114 Sender’s (CMU RTTM) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130101825 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//1400T0116 [[participant]] External Reference Number (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//1400T0001 Previous Reference No. (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::RELA//NS01302003SE128 Related Reference (client’s SEME from MT515 Modify Message) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303040506 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/MODA Trade Modify Accepted 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 310

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 310 
8m. MT518 Match Request (due to Contra Action) Sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[participant]] [[ID]]) 
518/000/GSCC Message Type 
1410 Receiver [[ID]] ([[NSCC]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000001750022 Sender’s (CMU RTTM) Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030130101826 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130101507 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//1400T0116 [[Buyer]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRAUTI Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amt) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRCOAC Trade Instruction Processing – Message Reason = due to Contra Action 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Block End 
:16S:SETDET Optional Block End 
- End of Message 
 
  

---

## Page 311

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 311 
8n. MT509 Modify Processed Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[participant]] [[ID]]) 
509/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000003250115 Sender’s (CMU RTTM) Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130101830 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//1400T0116 [[participant]] External Reference Number (NEW) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//1400T0001 Previous Reference No. (OLD) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303040506 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::IPRC/GSCC/MODP Trade Modify Processed 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
  

---

## Page 312

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 312 
Part C - DK Remove  
8o: Client A Enters a DK Remove Through Screen (no message sample)  
No message sample submitted through screen input. 
8p: MT518 DK Remove Advice Sent to Client B  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1400 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000004500322 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030130102237 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//1400T0116 [[participant]]’s External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303040506 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130101507 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/DCCX DK Remove Advice 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRAUTI Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRCOAC Trade Instruction Processing – Message Reason = due to Contra Action 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 

---

## Page 313

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 313 
Message Content Comments 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 
8q. MT518 Match Request (due to DK Remove) sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1410 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000500776 Sender’s (CMU RTTM) Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030130102251 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130101507 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTCP Place of Trade/Market of Execution – [[OTC]] Corporate 
:19A::SETT//USD12726,11 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1400 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//1400T0116 [[Buyer]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRSAMP Party = MPID of [[Buyer]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1410 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDID00200 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRAUTI Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//FAMT/20000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/00130HAP0 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRDCTD Trade Instruction Processing – Message Reason = due to DK Remove 
:16S:CONFDET Mandatory Block End 
:16R:SETDET Optional Block Start 
:22F::SETR//RPTO [[settlement]] Indicator = Reporting Only 
:16R:AMT Optional Block Start 
:19A::ACRU//USD151,11 Accrued Interest Amount 
:16S:AMT Optional Block End 
:16S:SETDET Optional Block End 
- End of Message 
  

---

## Page 314

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 314 
Sample Trade #9: Unit Investment Trust QSR (Locked-in) Trade 
On January 30, 2003, a Locked-in Regular Way QSR [[UIT]] Trade is executed between Client B (QSR-[[Buyer]]) 
and Client A (QSR Contra) for a contract amount of $1038.22. 
Field Description Client A – 1477 ([[Seller]]) Client B – 1488 ([[Buyer]]) 
QSR Locked-In Submitter 
Password PM3299 PM4332 
Sender [[ID]] 1477 1488 
SEME E00052130399TY (Part B) C00052130131SQ 
MAST 30130TRDC1750246 M0130200300141 
(Parts B and C) R0130200300141B 
(Reversal – Part D) 
S0130200300124 R0130200300154A 
(Reversal) 
Preparation Date & Time 1/30/2003 20:44:23 1/30/2003 09:21:40 
Trade Date and Time 1/30/2003 09:21:33 1/30/2003 09:21:33 
[[settlement]] Date 2/4/2003 2/4/2003 
Price 0 0 
Contract Amount 1038,22 1038,22 
Contra [[participant]] 1488 1477 
Contra Correspondent  POPY 
Contra Trader [[ID]]  TM021 
[[participant]] Correspondent POPY  
[[participant]] Capacity PRIN AGEN 
[[CUSIP]] 30264S247 30264S247 
PAR 146 UNITS 146 UNITS 
CMU RTTM Reference Number 
(TID) 
0303052146 0303000524 
Accrued Interest 0 0 
Match Control Number 0303000524 0303000524 
 
  

---

## Page 315

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 315 
The following message samples for Trade #9 are all based on the scenario presented on the previous 
page. 
Part A - QSR Submitter (Client B) Submits Buy Trade – Administrative Match (no contra submission) 
•  9a. MT515 Client B (QSR Locked-in Submitter) submits Buy Trade to CMU RTTM  
• 9 b. MT518 Match Request sent to Client A (QSR Contra) 
• 9c. MT518 Locked-in Trade Advice sent to Client A (Locked-in Recipient)  
• 9d. MT518 Match Request sent to Client B (QSR Submitter) 
•  9e. MT509 Trade Matched sent to Client A  
• 9f. MT509 Trade Matched sent to Client B 
• 9g. MT518 Match Request Cancel (due to Match) sent to Client A  
•  9h. MT518 Match Request Cancel (due to Match) sent to Client B  
• 9i MT518 [[settlement]] Disposition sent to Client A 
• 9j. MT518 [[settlement]] Disposition sent to Client B 
Part B - QSR Contra (Client A) Submits a Sell Trade With Target Indicator 
•  9k. MT515 Client A (QSR Contra) submits a Target QSR Sell Trade  
• 9l. MT518 Match Request sent to Client B (QSR Submitter) 
Part C - QSR Contra (Client A) Submits a Sell Trade Without Target Indicator 
•  9m. MT515 Client A (QSR Contra) Submits Sell Trade (Without QSR Targeted Field)  
• 9n. MT518 Match Request sent to Client B (QSR Submitter) 
• 9o. MT509 Trade Matched sent to Client A 10p. MT509 Trade Matched sent to Client B 
• 9q.  MT518 Matched with Modifications sent to Client A 
Part D - QSR Submits a Reversal 
•  9r. MT515 Client B (QSR) submits Reversal to CMU RTTM (Reversal of Buy)  
• 9s. MT518 Match Request sent to Client A 
• 9t. MT515 Client A (QSR Target) Submits Reversal to CMU RTTM (Reversal of Sell) 
  

---

## Page 316

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 316 
Part A - QSR Submitter (Client B) Submits Buy Trade – Administrative Match 
(no contra submission) 
Sample #9a: MT515 Client B (QSR Locked-in Submitter) Submits Buy Trade to CMU 
RTTM 
Message Content Comments 
 Message Header 
PM4332 CMU RTTM Assigned Password 
1488 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//C00052130131SQ Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030130092140 Date and Time of message preparation 
:22F::TRTR/GSCC/TRLK Locked-In Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//S0130200300124 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22F::TTCO/GSCC/TSQS Trade Type – QSR Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – [[participant]] [[ID]] 
:22F::TRCA//AGEN Capacity Indicator – Acting as Agent 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDTM021 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (UNIT = units or [[shares]]) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing Narrative – Destination = CMU RTTM 
:16S:CONFDET Mandatory Block End 
- End of Message 
 
  

---

## Page 317

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 317 
Sample #9b: MT518 Match Request sent to Client A (QSR Contra) 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1477 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303000003750545 Sender’s Message Reference Number 
:23G:NEWM New Message 
:98C::PREP//20030130092150 Date and Time of message preparation 
:22F::TRTR/GSCC/TRLK Locked-In Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22F::TTCO/GSCC/TSQS Trade Type – QSR Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//S0130200300124 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDTM021 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Unit = Share) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 318

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 318 
Sample #9c: MT518 Locked-in Trade Advice sent to Client A (Locked-in Recipient) 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1477 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3030000001500544 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030130204423 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Locked In Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//30130TRDC1750246 Reference Generated by CMU RTTM on [[Seller]]’s behalf 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303052146 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0303000524 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution–[[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/LCTA Locked-In Trade Advice 
:22F::TTCO/GSCC/TTQS Trade Type = QSR Targeted Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//S0130200300124 Contra [[Buyer]] External Reference Number 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDTM021 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Unit = Share) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing Narrative – Destination = CMU RTTM 
:16S:CONFDET Mandatory Block End 
- End of Message 
  

---

## Page 319

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 319 
Sample #9d: MT518 Match Request sent to Client B (QSR Submitter) 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1488 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303000003750875 Sender’s Message Reference Number 
:23G:NEWM New Message 
:98C::PREP//20030130204425 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Locked-In Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22F::TTCO/GSCC/TTQS Trade Type – QSR Target Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – [[participant]] [[ID]] 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//30130TRDC1750246 [[Seller]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Unit = Share) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
- End of Message 
  

---

## Page 320

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 320 
Sample #9e: MT509 Trade Matched sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1477 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303000000750621 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130204431 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//30130TRDC1750246 [[participant]] External Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303052146 CMU RTTM Assigned Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//S0130200300124 Contra External Reference Number (of trade matched against client trade) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0303000524 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
  

---

## Page 321

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 321 
Sample #9f: MT509 Trade Matched sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1488 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000250265 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130204432 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//S0130200300124 [[participant]] External Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303000524 CMU RTTM Assigned Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//30130TRDC1750246 Contra External Reference Number (of trade matched against client trade) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0303000524 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 322

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 322 
9g. MT518 Match Request Cancel (due to Match) Sent to Client A  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1477 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303100001750185 Sender’s Message Reference Number 
:23G:CANC Cancel Message 
:98C::PREP//20030130204436 Date and Time of message preparation 
:22F::TRTR/GSCC/TRLK Locked-In Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:22C::PREV//NONREF SWIFT Required for Cancel Message 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22F::TTCO/GSCC/TSQS Trade Type – QSR Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//S0130200300124 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDTM021 [[Seller]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Unit = Share) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing – Message Reason = due to Match 
:16S:CONFDET Mandatory Block End 
- End of Message 
 
  

---

## Page 323

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 323 
9h. MT518 Match Request Cancel (due to Match) sent to Client B  
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1488 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303100000750255 Sender’s Message Reference Number 
:23G:CANC Cancel Message 
:98C::PREP//20030130204437 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::PREV//NONREF SWIFT Required for Cancel Message 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CADV Match Request Cancel Record 
:22F::TTCO/GSCC/TTQS Trade Type – Target QSR Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – [[participant]] [[ID]] 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//30130TRDC1750246 [[Seller]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Unit = Share) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing – Message Reason = due to Match 
:16S:CONFDET Mandatory Block End 
End of Message 
 
  

---

## Page 324

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 324 
9i MT518 [[settlement]] Disposition Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1477 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303100001750193 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030131204438 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Locked-in Trade Indicator 
:16R:LINK Repeat Block Start 
:20C::MAST//30130TRDC1750246 [[participant]]’s External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//0303052146 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//0303000524 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] – [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition Message 
:22F::TTCO/GSCC/TTQS Trade Type – Target QSR Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – Contraparty [[ID]] 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Units = [[shares]]) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/SDSPCNSE 
/DDTE20030204 
Trade Instruction Processing – Message Reason = due to CMU 
RTTM Action / [[settlement]] Disposition = [[CNS]] Eligible / Delivery 
Date = 02/04/2003 
:16S:CONFDET Mandatory Block End 
- End of Message 
 
  

---

## Page 325

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 325 
9j. MT518 [[settlement]] Disposition sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1488 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303100001500226 Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030130204440 Date and Time of message preparation 
:22F::TRTR/GSCC/TRLK Locked-in Trade Indicator 
:16R:LINK Repeat Block Start 
:20C::MAST//S0130200300124 [[participant]]’s External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::LIST//0303000524 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Repeat Block Start 
:20C::COMM//0303000524 Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] – [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/STLD [[settlement]] Disposition Message 
:22F::TTCO/GSCC/TSQS Trade Type – QSR Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – [[participant]] [[ID]] 
:22F::TRCA//AGEN Capacity – Acting as Agent 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDM021 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Units = [[shares]]) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC/SDSPCNSE 
/DDTE20030204 
Trade Instruction Processing – Message Reason = due to CMU 
RTTM Action / [[settlement]] Disposition = [[CNS]] Eligible / Delivery 
Date = 02/04/2003 
:16S:CONFDET Mandatory Block End 
- End of Message 
 

---

## Page 326

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 326 
Part B - QSR Contra (Client A) Submits a Sell Trade With Target Indicator 
9k. MT515 Client A (QSR Contra) submits a Target QSR Sell Trade 
Message Content Comments 
 Message Header 
PM3299 CMU RTTM Assigned Password 
1477 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//E00052130399TY Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030130092140 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0130200300141 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//2003013092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//1038,22 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22F::TTCO/GSCC/TTQS Trade type/Target QSR Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – Contraparty [[ID]] 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (UNIT = [[shares]] ) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator = CMU RTTM 
:16S:CONFDET Mandatory Block End 
- End of Message 
 
  

---

## Page 327

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 327 
9l. MT518 Match Request sent to Client B (QSR Submitter) 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1488 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303000003750874 Sender’s Message Reference Number 
:23G:NEWM New Message 
:98C::PREP//20030130092150 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22F::TTCO/GSCC/TTQS Trade Type – Targeted Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – [[participant]] [[ID]] 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//M0130200300141 [[Seller]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Unit = Share) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
- End of Message 
  

---

## Page 328

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 328 
Part C - QSR Contra (Client A) Submits a Sell Trade Without Target Indicator  
Sample #9m: MT515 Client A (QSR Contra) Submits Sell Trade (Without QSR Target) 
Message Content Comments 
 Message Header 
PM3299 CMU RTTM Assigned Password 
1477 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//E00052130399TY Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030130092140 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0130200300141 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//2003013092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//1038,22 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – Contraparty [[ID]] 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (UNIT = [[shares]] ) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01 Trade Instruction Processing – Destination Indicator = CMU RTTM 
:16S:CONFDET Mandatory Block End 
- End of Message 
 
  

---

## Page 329

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 329 
Sample #9n: MT518 Match Request sent to Client B (QSR Submitter) 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1488 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303000003750875 Sender’s Message Reference Number 
:23G:NEWM New Message 
:98C::PREP//20030130092150 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – [[participant]] [[ID]] 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//M0130200300141 [[Seller]]’s (Contra) External Reference Number 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Unit = Share) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:16S:CONFDET Mandatory Block End 
- End of Message 
 
  

---

## Page 330

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 330 
Sample #9o: MT509 Trade Matched Sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1477 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303000003750126 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130204437 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M0130200300141 [[participant]] External Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303052146 CMU RTTM Assigned Reference Number (of trade being matched) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//S0130200300124 Contra External Reference Number (of trade matched against client trade) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0303000524 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
 
  

---

## Page 331

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 331 
Sample #9p: MT509 Trade Matched Sent to Client B 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT509 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
509/000/GSCC Message Type 
1488 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000250562 Sender’s Message Reference Number 
:23G:INST Message Function (for Instruction) 
:98C::PREP//20030130204438 Date and Time of message preparation 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//S0130200300124 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303000524 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::PROG//M0130200300141 Contra External Reference Number (of trade matched against client trade) 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0303000524 CMU RTTM Assigned Match Control Number 
:16S:LINK Repeat Block End 
:16R:STAT Mandatory Block Start 
:25D::MTCH//MACH Trade Matched Status 
:16S:STAT Mandatory Block End 
:16S:GENL Mandatory Block End 
- End of Message 
  

---

## Page 332

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 332 
Sample #9q: MT518 Matched With Modifications sent to Client A 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1477 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//3013000000250824 Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030130204441 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//M013200300141 [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::LIST//0303052146 CMU RTTM Assigned Reference Number 
:16S:LINK Repeat Block End 
:16R:LINK Mandatory Repeat Block Start 
:20C::COMM//0303000524 CMU RTTM Match Control Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130092133 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade)` 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] -- [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/CMPM Match With Modifications Record 
:22F::TTCO/GSCC/TTQS Target QSR Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1488 [[Buyer]] Information – Contraparty [[ID]] 
:20C::PROC//S0130200300124 Contra [[Buyer]] X-ref 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1477 [[Seller]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (UNIT = [[shares]]) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRGSAC Trade Instruction Processing / Message Reason = Due to CMU RTTM 
Action 
:16S:CONFDET Mandatory Block End 
– End of Message 
 
  

---

## Page 333

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 333 
Part D - QSR Submits a Reversal 
Sample #9r: MT515 Client B (QSR) submits Reversal to CMU RTTM (Reversal of Buy) 
Message Content Comments 
 Message Header 
PM4332 CMU RTTM Assigned Password 
1488 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//C00855130131SQ Sender’s Message Reference Number 
:23G:NEWM New trade (or modify) input 
:98C::PREP//20030130105635 Date and Time of message preparation 
:22F::TRTR/GSCC/TRLK Locked-In Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//R0130200300154A [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105632 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//SELL Sell Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22F::TTCO/GSCC/TSQS Trade Type – QSR Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1477 [[Buyer]] Information – Contraparty [[ID]] 
:70C::PACO//GSCC/TDIDTM021 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1488 [[Seller]] Information – [[participant]] [[ID]] 
:22F::TRCA//AGEN Capacity Indicator – Acting as Agent 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Units = [[shares]]) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/RVSL Trade Instruction Processing Narrative – Destination Indicator = CMU 
RTTM / Reversal Indicator = message is a Reversal. 
:16S:CONFDET Mandatory Block End 
- End of Message 
 
  

---

## Page 334

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 334 
Sample #9s: MT518 Match Request sent to Client A 
 
Message Content Comments 
 Message Header 
 CMU RTTM Assigned Password – blank filled on MT518 
NSCCTRRS Sender [[ID]] ([[NSCC]] CMU RTTM) 
518/000/GSCC Message Type 
1477 Receiver [[ID]] ([[participant]] [[ID]]) 
:16R:GENL Mandatory Block Start 
:20C::SEME//303000000750455 Sender’s Message Reference Number 
:23G:NEWM New Message 
:98C::PREP//20030130105640 Date and Time of message preparation 
:22F::TRTR/GSCC/TRLK Locked-In Trade Indicator 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105632 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//USD1038,22 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/CMPR Match Request Record 
:22F::TTCO/GSCC/TSQS Trade Type – QSR Trade 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1477 [[Buyer]] Information – [[participant]] [[ID]] 
:70C::PACO//GSCC/TDIDTM021 [[Buyer]] [[participant]] Contact Information - Trader [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Buyer]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1488 [[Seller]] Information – Contraparty [[ID]] 
:20C::PROC//R0130200300154A [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (Unit = Share) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/RVSL Trade Instruction Processing Narrative -- Reversal Indicator = message is 
a Reversal. 
:16S:CONFDET Mandatory Block End 
- End of Message 
 
  

---

## Page 335

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix C: Message Samples 335 
Sample #9t: MT515 Client A (QSR Contra) submits a Reversal to CMU RTTM (Reversal 
of Sell) 
Message Content Comments 
 Message Header 
PM3299 CMU RTTM Assigned Password 
1477 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
NSCCTRRS Receiver [[ID]] ([[NSCC]] CMU RTTM) 
:16R:GENL Mandatory Block Start 
:20C::SEME//E00972130399TY Sender’s Message Reference Number 
:23G:NEWM New trade input 
:98C::PREP//20030130105703 Date and Time of message preparation 
:22F::TRTR/GSCC/CASH Bilateral Trade Indicator 
:16R:LINK Mandatory Repeat Block Start 
:20C::MAST//R0130200300141B [[participant]] External Reference Number 
:16S:LINK Repeat Block End 
:16S:GENL Mandatory Block End 
:16R:CONFDET Mandatory Block Start 
:98C::TRAD//20030130105637 Trade Date and Time 
:98A::SETT//20030204 [[settlement]] Date 
:90A::DEAL//PRCT/0, Price type = Percent (Zero indicates final money trade) 
:94B::TRAD/GSCC/OTUI Place of Trade/Market of Execution – [[OTC]] [[UIT]] 
:19A::SETT//1038,22 [[settlement]] Amount 
:22H::BUSE//BUYI Buy Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22F::TTCO/GSCC/TTQS Trade type/Target QSR Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::BUYR/GSCC/PART1477 [[Buyer]] Information – [[participant]] [[ID]] 
:70E::DECL//GSCC/CORRPOPY Party = MPID of [[Seller]]’s Correspondent Firm 
:22F::TRCA//PRIN Capacity Indicator – Acting as Principal 
:16S:CONFPRTY Mandatory Repeat Block End 
:16R:CONFPRTY Mandatory Repeat Block Start 
:95R::SELL/GSCC/PART1488 [[Seller]] Information – Contraparty [[ID]] 
:16S:CONFPRTY Mandatory Repeat Block End 
:36B::CONF//UNIT/146, Quantity of Security (UNIT = [[shares]] ) 
:35B:/US/30264S247 Security [[ID]] ([[CUSIP]]) 
:70E::TPRO//GSCC/DEST01/RVSL Trade Instruction Processing – Destination Indicator = CMU RTTM / Trade is a 
Reversal 
:16S:CONFDET Mandatory Block End 
End of Message 
 

---

## Page 336

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix D: Message Structure Diagrams 336 
APPENDIX D: MESSAGE STRUCTURE DIAGRAMS 
This appendix provides message structure diagrams for MT515, MT509, and MT518 messages. 
Message Structure Diagrams – MT515 
 
  


---

## Page 337

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix D: Message Structure Diagrams 337 
Message Structure Diagrams – MT509 
 
  


---

## Page 338

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix D: Message Structure Diagrams 338 
Message Structure Diagrams – MT518 
 
  


---

## Page 339

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix E: CMU RTTM Code Tables 339 
APPENDIX E: CMU RTTM CODE TABLES 
This appendix provides the following codes: 
• Message Reject Reason Codes 
• [[settlement]] Disposition Codes 
[[settlement]] Disposition Codes (to be used in field 
:70E::TPRO//GSCC/SDSP) 
[[settlement]] Disposition Method 
CNSE [[CNS]] Eligible 
CNSN Non [[CNS]] Netting 
CPRO Comparison Only 
TFTD Trade for Trade 
Message Reject Reason Codes 
Note:  
While most of the codes contained in the following table are used to support GSCC, MBSCC and [[NSCC]] CMU RTTM, 
some codes are used only by one clearing corporation, and may not be used by another. 
Reject Error Code Qualifiers (to be used on 
MT509) in field :24B::REJT/ 
Error Conditions Which Can Cause an MT515 to be 
Rejected by CMU RTTM 
GSCC/E001 External Reference Error 
GSCC/E002 Previous External Reference Error 
GSCC/E003 Trade Not Eligible For Cancellation 
GSCC/E004 Unknown Security 
GSCC/E005 Bad Quantity 
GSCC/E006 Bad Trade Date 
GSCC/E007 Bad [[settlement]] Date 
GSCC/E008 Bad Price 
GSCC/E009 Bad Amount 
GSCC/E010 Bad [[Buyer]] Party 
GSCC/E011 Bad [[Seller]] Party 
GSCC/E012 [[Broker]] Reference Number Error 
GSCC/E013 Transaction Type Error 
GSCC/E014 Price Method Error 
GSCC/E015 Commission Error 
GSCC/E016 Password Error 
GSCC/E017 [[Buyer]] Executing Firm Error 
GSCC/E018 [[Seller]] Executing Firm Error 
GSCC/E019 Start Amount Error4 
GSCC/E020 Start Date Error 
 
4 Supports only GSCC and MBSCC products. 

---

## Page 340

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix E: CMU RTTM Code Tables 340 
Reject Error Code Qualifiers (to be used on 
MT509) in field :24B::REJT/ 
Error Conditions Which Can Cause an MT515 to be 
Rejected by CMU RTTM 
GSCC/E021 End Amount Error 
GSCC/E022 End Date Error 
GSCC/E023 Repo Rate Error 
GSCC/E024 Secondary X-ref Error 
GSCC/E025 Substitution Type Error 
GSCC/E026 Substitution Number Error 
GSCC/E027 Substitution [[collateral]] Error 
GSCC/E028 Substitution Variance Error 
GSCC/E029 Substitution Frequency Error 
GSCC/E030 Trade Not in Same State 
GSCC/E101 Give Up Period Error 
GSCC/E102 Trade Service Type Error 
GSCC/E103 [[Option]] Type Error 
GSCC/E104 [[Option]] Expiry Date Error 
GSCC/E105 Account Trade Restricted 
GSCC/E202 Market of Execution Error 
GSCC/E203 Trade Type/Target Indicator Error 
GSCC/E204 Destination Indicator Error 
GSCC/E205 Inconsistent Recipient Information 
GSCC/E020 Start Date Error 
GSCC/E021 End Amount Error 
GSCC/E022 End Date Error 
GSCC/E023 Repo Rate Error 
GSCC/E024 Secondary X-ref Error 
GSCC/E025 Substitution Type Error 
GSCC/E026 Substitution Number Error 
GSCC/E027 Substitution [[collateral]] Error 
GSCC/E028 Substitution Variance Error 
GSCC/E029 Substitution Frequency Error 
GSCC/E030 Trade Not in Same State 
GSCC/E101 Give Up Period Error 
GSCC/E102 Trade Service Type Error 
GSCC/E103 [[Option]] Type Error 
GSCC/E104 [[Option]] Expiry Date Error 
GSCC/E202 Market of Execution Error 
GSCC/E203 Trade Type/Target Indicator Error 
GSCC/E204 Destination Indicator Error 
GSCC/E205 Inconsistent Recipient Information 
GSCC/E206 Issue Type Error 
GSCC/E207 [[settlement]] Date Adjustment Error 
GSCC/E208 [[settlement]] Type Error 
GSCC/E209 Interest Error 
GSCC/E210 Concession Error 
GSCC/E211 Branch Sequence Number Error 
GSCC/E212 Unknown Target Application 
GSCC/E998 Trade Not Found 
GSCC/E999 Other Bad Data 
GSCC/F001 Illegal Operation Attempted 
GSCC/F002 Internal Process Error 
GSCC/F999 Non-SWIFT Compliant Message 

---

## Page 341

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix E: CMU RTTM Code Tables 341 
[[settlement]] Disposition Codes 
[[settlement]] Disposition Codes (to be used in 
field :70E::TPRO//GSCC/SDSP) 
[[settlement]] Disposition Method 
CNSE [[CNS]] Eligible 
CNSN Non [[CNS]] Netting 
CPRO Comparison Only 
TFTD Trade for Trade 
Don’t Know (DK) Reason Codes 
Note:  
While most of the codes contained in the following table are used to support GSCC, MBSCC and [[NSCC]] CMU RTTM, 
some codes are used only by one clearing corporation, and may not be used by another. 
The following table shows the don’t know (DK) reason codes that are used on MT515 and MT518 in the 
:70E::TPRO//GSCC/DKRS field: 
DK Reason Code Description 
E004 Unknown Security 
E005 Bad Quantity 
E006 Bad Trade Date 
E007 Bad [[settlement]] Date 
E008 Bad Price 
E009 Bad Amount 
E010 Bad [[Buyer]] Party 
E011 Bad [[Seller]] Party 
E013 Transaction Type Error 
E014 Price Method Error 
E015 Commission Error 
E017 [[Buyer]] Correspondent Error 
E018 [[Seller]] Correspondent Error 
E100 Unknown Cancel 
E102 Trade Service Type Error 
E106 Incorrect Account Symbol 
E107 Duplicate Trade 
E202 Market of Execution Error 
E203 Trade Type/Target Indicator Error 
E206 Issue Type Error 
E207 [[settlement]] Date Adjustment Error 
E208 [[settlement]] Type Error 
E209 Interest Error 
E210 Concession Error 
E998 Trade not found 
E999 Other Bad Data 
  

---

## Page 342

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix E: CMU RTTM Code Tables 342 
Message Reason Codes 
The following table shows the message reason codes used in MT518 in the :70E::TPRO//GSCC/MSGR field:  
Message Reason Code Description 
DKTD Due to DK 
DCTD Due to DK Remove 
MACH Due to Match 
COAC Due to Contra Action 
GSAC Due to CMU RTTM Action 
YRAC Due to your Action 
Destination Codes 
Destination Codes (to be used in field 
:70E::TPRO//GSCC/DEST) 
Destination 
01 CMU RTTM 
02 MSRB 
Issue Type 
Issue Type Codes (to be used in field 
:70E::TPRO//GSCC/ITYP) 
Issue Type 
SY [[syndicate]] Trade 
TS Target [[syndicate]] Trade 
 

---

## Page 343

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix E: CMU RTTM Code Tables 343 
APPENDIX F: MT518 PROCESSING OF REGULATORY 
FIELDS 
Regulatory data fields, with the exception of Trade Date/Time field, are optional for CMU RTTM purposes. 
Therefore, if they appear on the MT515 message submitted to CMU RTTM, they are reflected on MT518 
messages as indicated in the following table. The fields indicated with ** apply to both regulator and CMU 
RTTM applications. 
Regulatory Fields 
Submitted on MT515 
 
Field Names 
MT518 
Advisories 
MT518 
Locked-In 
Advices 
MT518 Advices 
Referring to Your 
Trades 
Destination MSRB :70E::TPRO//GSCC/DEST02 NO YES Screen Input Trade 
Replay 
only 
Executing [[Broker]] 
Commission 
:19A::EXEC//USD NO NO YES 
Message Originator :95Q::MEOR NO NO YES 
[[participant]] / Contraparty 
Correspondent**  
:70E::DECL//GSCC/CORR 
 
YES 
 
YES 
 
YES 
Price Indicator - Weighted 
Price 
:22F::PRIC/GSCC/WGTP NO NO YES 
Regulator Control Number :20C::TRRF// NO NO YES 
Reversal Control Number :70E::TPRO//GSCC/RCTL NO NO YES 
MSRB Special 
Condition Indicators 
:70E::TPRO//GSCC/SPXR NO NO YES 
Trade Date/Time** :98C::TRAD// YES YES YES 
Trading Capacity - 
Contraparty** 
:22F::TRCA YES YES YES 
Trading Capacity - 
[[participant]] 
:22F::TRCA NO NO YES 
Yield :70E::TPRO//GSCC/YIEL NO NO YES 
Regulatory Dollar Price :70E::TPRO//GSCC/RGDP YES YES YES 
Miscellaneous :70E::TPRO//GSCC/MISC NO NO YES 
  

---

## Page 344

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix E: CMU RTTM Code Tables 344 
APPENDIX G: MSRB REGULATORY INFORMATION 
MSRB Regulatory Fields 
Although CMU RTTM accepts all regulatory fields, only the fields indicated as Y in the MSRB column are 
forwarded to MSRB. 
[[Option]]/Qualifier Web Screen Field MSRB 
DEST 
Note: /DEST01 CMU RTTM Only messages are not 
forwarded to MSRB 
Trade Reporting Indicator Y 
/EXEC N/A Y 
/MEOR Originator of message Y 
/WGTP Price Indicator - Weighted Price Y 
/TRRF Regulator Control Number Y 
/RCTL Reversal Control Number Y 
/SPXR Special Condition Indicator Code Y 
:98C::TRAD//yyyymmddhhmmss Trade Time Y 
/AGEN or /PRIN Trading Capacity - Contraparty Y 
/AGEN or /PRIN Trading Capacity - [[participant]] Y 
:70E::TPRO//GSCC - /YIEL Regulatory Yield Y 
:70E::TPRO//GSCC - /RGDP Regulatory Dollar Price Y 
:70E::TPRO//GSCC - /MISC Miscellaneous Y 
  

---

## Page 345

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix E: CMU RTTM Code Tables 345 
MSRB Special Condition Indicator Codes 
The following table shows the special condition indicators that are used on MT515 and MT518 in the 
:70E::TPRO//GSCC/SPXR field. The RFRNC_CODE_CTGRY_NM for each MSRB special condition indicator is 
CMUPRICEREASON. Review the MSRB Specifications for Real - Time Reporting of Municipal [[securities]] 
Transactions document to determine which code to assign t o a trade. If you have any questions , email 
MSRBSupport@MSRB.org. 
MSRB Indicator Codes Special Condition 
M001 15 min – Alternative trading system ([[ATS]]) 
M020 End of Day ([[EOD]]) List Offering Price/Takedown (LOP/TD) 
M021 [[EOD]] LOP/TD – [[ATS]] 
M030 [[EOD]] mat less than 9 mos 
M031 [[EOD]] mat less than 9 mos – [[ATS]] 
M040 [[EOD]] ineligible on trade date 
M041 [[EOD]] ineligible on trade date – [[ATS]] 
M050 [[EOD]] resubmission of CMU RTTM cancel 
M051 [[EOD]] resubmission of CMU RTTM cancel – [[ATS]] 
M100 15 min - Trade flat 
M101 15 min - Trade flat – [[ATS]] 
M130 [[EOD]] mat less than 9 months - Trade flat 
M131 [[EOD]] mat less than 9 months - Trade flat – [[ATS]] 
M140 [[EOD]] ineligible on trade date - trade flat 
M141 [[EOD]] ineligible on trade date - trade flat – [[ATS]] 
M150 [[EOD]] resubmission of RTTM cancel - trade flat 
M151 [[EOD]] resubmission of RTTM cancel - trade flat – [[ATS]] 
M900 15 min - Not mkt price (other) 
M901 [[EOD]] - Not mkt Price (other) – [[ATS]] 
M930 [[EOD]] mat less than 9 months - Not mkt price (other) 
M931 [[EOD]] mat less than 9 months - Not mkt price (other) – [[ATS]] 
M940 [[EOD]] ineligible on trade date - Not mkt price other. 
M941 [[EOD]] ineligible on trade date - Not mkt price (other) – [[ATS]] 
M950 [[EOD]] resubmission of CMU RTTM cancel - Not mkt price other 
M951 [[EOD]] resubmission of CMU RTTM cancel - Not mkt price (other) – [[ATS]] 

---

## Page 346

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix E: CMU RTTM Code Tables 346 
Message Originator (MEOR) Codes 
For a list of MEOR Identifier that are used on MT515 and MT518 in the :95Q::MEOR// field, see MSRB 
Specifications for Real - Time Reporting of Municipal [[securities]] Transactions.  

---

## Page 347

CMU RTTM Interactive Messaging Specifications for Trade Input and Output Specifications Guide 
Appendix E: CMU RTTM Code Tables 347 
APPENDIX H: [[settlement]] TYPE INDICATOR FIELD 
MAPPING 
This appendix provides the mapping of the MT515 [[settlement]] Type Indicator fields with the codes on the 
[[NSCC]] batch output layouts. 
Field Description MT515 Field Values [[NSCC]] Batch Input/output Layout Value 
Special Trade :22F::SETR/GSCC/STRD X 
Comparison Only :22F::SETR/GSCC/CPRO F 
Trade Not a Special Trade*5 :22F::SETR//RPTO SPACE 
 
 
 
5 Required only where [[settlement]] Block appears, and none of the above values are applicable. 

---

## Page 348

 
Appendix H: [[settlement]] Type Indicator Field Mapping 348 
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 