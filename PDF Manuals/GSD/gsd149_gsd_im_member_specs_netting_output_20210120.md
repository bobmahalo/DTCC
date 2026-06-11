---
title: "GSD IM Member Specs for Netting Output_v2.0"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd149_gsd_im_member_specs_netting_output_20210120.pdf"
pages: 381
size: "2939.9 KB"
category: "GSD"
ingested_on: "2026-06-05"
---

# GSD IM Member Specs for Netting Output_v2.0

**Original File:** [gsd149_gsd_im_member_specs_netting_output_20210120.pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/gsd149_gsd_im_member_specs_netting_output_20210120.pdf)  
**Category:** GSD  
**Total Pages:** 381  
**File Size:** 2939.9 KB  

---

## Page 1

  
 
 
 
[[FICC]] – [[GSD]] 
[[GSD]] INTERACTIVE MESSAGING (IM) [[Member]] SPECIFICATIONS FOR 
NETTING OUTPUT 
VERSION 2.0.0 
JANUARY 20, 2021 
 


---

## Page 2

 
  
© 2021 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
Doc Date: January 20, 2021 
Publication Code: GSD149 
Service: [[FICC]] – [[GSD]]   
Title: [[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
 
 
The [[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output (hereinafter, the "document") is provided as 
a convenience to Members and is for information purposes only. Although [[FICC]] may make this document available to 
Members, it shall be under no obligation to [[DO]] so, nor having once or more done so, shall [[FICC]] have a continuing 
obligation to make available this document or other related information of a certain type.  
 
[[FICC]] does not represent the accuracy, adequacy, timeliness, completeness, or fitness for any particular purpose 
of any information provided to Members in this document, which is provided as-is. [[FICC]] shall not be liable for any 
loss related to such information (or the act or process of providing such information) resulting directly or 
indirectly from mistakes, errors, or omissions, other than those caused directly by gross negligence or willful 
misconduct on the part of [[FICC]]. [[FICC]] shall not be liable for: (1) any loss resulting directly or indirectly from 
interruptions, delays, or defects arising from or related to providing this guide; and (2) any special, consequential, 
exemplary, incidental, or punitive damages.  
 
Further, the information contained in this document is subject to change. Members and other authorized users of the 
document will find the most current version of the document on [[DTCC]]’s Learning Center site, 
www.dtcclearning.com. 
[[FICC]] shall bear no responsibility for any losses associated with the failure of Members or other authorized users to follow 
[[FICC]]’s most current document. 
 
 

---

## Page 3

 
  
TABLE OF CONTENTS 
Overview ............................................................................................................................................................... 5 
Introduction .......................................................................................................................................................... 6 
Netting Interactive Message Overview .............................................................................................................. 7 
Message Overview ............................................................................................................................................. 7 
Message Formatting Structure .......................................................................................................................... 8 
Formatting Structure Overview ........................................................................................................................ 8 
Message Header ............................................................................................................................................. 9 
Blocks and Sub-blocks .................................................................................................................................... 9 
Fields ............................................................................................................................................................. 10 
Message Formatting Rules ............................................................................................................................. 11 
Message Rules .............................................................................................................................................. 11 
Message Field Rules ..................................................................................................................................... 11 
Formatting Conventions ................................................................................................................................. 12 
[[GSD]] Application Modules ............................................................................................................................... 14 
Netting Interactive Message Specifications – MT509 ..................................................................................... 15 
MT509 Netting Status Message Description .................................................................................................... 15 
MT509 Netting Status Message Specifications ................................................................................................ 17 
MT509 General Format ................................................................................................................................... 17 
MT509 Field Specifications ............................................................................................................................. 20 
MT509 Field Analysis ...................................................................................................................................... 23 
Netting Interactive Message Specifications – MT548 ..................................................................................... 27 
MT548 [[settlement]] Status Message Description .............................................................................................. 27 
MT548 [[settlement]] Status Message Specifications .......................................................................................... 29 
MT548 General Format ................................................................................................................................... 29 
MT548 Field Specifications ............................................................................................................................. 36 
MT548 Message Mapping ............................................................................................................................... 46 
Netting Interactive Message Specifications – MT590 ..................................................................................... 62 
MT590 Message Description ............................................................................................................................ 62 

---

## Page 4

 
  
MT590 Message Specifications ........................................................................................................................ 63 
MT590 General Format ................................................................................................................................... 63 
MT590 Field Specifications ............................................................................................................................. 65 
MT590 Message Mapping ............................................................................................................................... 67 
Netting Interactive Message Specifications – MT950 ..................................................................................... 73 
MT950 Statement Message Description .......................................................................................................... 73 
MT950 Statement Message Specifications ...................................................................................................... 75 
MT950 General Format ................................................................................................................................... 75 
MT950 Field Specifications ............................................................................................................................. 79 
MT950 Message Mapping ............................................................................................................................... 86 
Appendices ....................................................................................................................................................... 134 
List of Appendices...........................................................................................................................................134 
Appendix A – Message Flows .......................................................................................................................135 
Flows ............................................................................................................................................................138 
Supplementary Flows ..................................................................................................................................166 
Appendix B – Message Samples ..................................................................................................................176 
Sample # B1 – Comparison, Netting and [[settlement]] Messages Resulting from a Next Day Settling Buy/Sell 
Transaction ..................................................................................................................................................178 
Sample # B2 – Comparison, Netting and [[settlement]] Messages Resulting from a Next Day Starting Repo 
Transaction ..................................................................................................................................................204 
Sample # B3 – Comparison, Netting and [[settlement]] Messages Resulting from a Same-Day Starting Repo 
Transaction ..................................................................................................................................................234 
Sample # B4 – Comparison, Netting and [[settlement]] Messages Resulting from a Same-Day Starting Repo 
Transaction Cancelled Post Comparison/Pre-Net .......................................................................................262 
Sample # B5 – Comparison and Netting Messages Resulting from a Forward Settling Buy/Sell Transaction 
Cancelled/Removed from Net Post Comparison .........................................................................................302 
Sample # B6 – Demand Comparison, Netting and [[settlement]] Messages Resulting from a Same-Day 
Starting Repo Transaction ...........................................................................................................................334 
Sample # B7 – [[settlement]] Messages Resulting from an Intraday Partial [[settlement]] ................................358 
Sample # B8 – [[settlement]] and Funds [[settlement]] Messages Resulting from the Pair-Off of a Same-Day 
Settling Obligation and a Netted Obligation .................................................................................................365 
Appendix C – Message Timing Matrix ..........................................................................................................375 
 

---

## Page 5

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Overview 5 
 
OVERVIEW 
Interactive Messaging for Netting   
This document provides Members of the Fixed Income Clearing Corporation‘s (“[[FICC]]”) Government [[securities]] 
Division (“[[GSD]]”) with interactive messaging specifications for [[GSD]]’s netting output.  
Audience 
This document was written for systems and development personnel, including managers, analysts and 
programmers of [[GSD]] [[Member]] firms. It presumes readers are familiar with technical concepts and terms as 
well as having a [[BASIC]] understanding of [[GSD]]'s products and services. 
Related Materials 
The “[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output” is not a standalone document. 
The specifications for interactive messages supporting netting output are based on SWIFT messages. Users of 
this document are therefore strongly urged to refer to SWIFT user documentation to obtain a complete and 
comprehensive understanding of these message standards. SWIFT information (including message formats) 
can be found at www.iso15022.org. Additionally, users must refer to the latest version of the “[[GSD]] Interactive 
Messaging (IM) [[Member]] Specifications for Comparison Input and Output” document to obtain an 
understanding of interactive messaging specifications for [[GSD]]’s comparison input and output used to support 
[[GSD]] products and services. 
Additional inquiries regarding Netting services may be directed to your [[FICC]] Relationship Manager. 
Communication 
For information on [[FICC]] Connectivity, please contact [[FICC]] Integration at ficcintegration@[[DTCC]].com
. 
  

---

## Page 6

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Introduction 6 
 
INTRODUCTION 
This document provides the specifications for Interactive Messaging related to the support of [[GSD]]’s Netting 
process, enabling [[GSD]] Members to receive netting and [[settlement]] output on an interactive basis using 
standardized SWIFT formats.  
Messages discussed in this document will give Members the ability to take in Clearance and Funds [[settlement]] 
as well as other important trade netting status information on a real-time basis. 
It should be noted that this document is a technical specification and is not, in any way, intended to 
communicate legal definitions as to when trades are guaranteed or novated by [[GSD]]. Members should refer to 
the [[FICC]] [[GSD]] Rulebook for such information. 
For additional service details, please refer to the Clearing Services > Fixed Income – [[GSD]] section available at 
www.[[DTCC]].com. 
Note: 
[[GSD]] utilizes SWIFT standardized messages, but it does not utilize the SWIFT network. [[GSD]] currently utilizes its 
proprietary network for communication between [[GSD]] and its Members. The SWIFT outbound and inbound messaging 
format [[GSD]] employs is meant to be compliant with SWIFT standards so that the SWIFT network could be used in the 
future. [[GSD]] utilizes the flexible ISO 15022 message formats for its outbound and inbound real-time messaging, such 
flexibility allows [[GSD]] to deploy new coding for these formats as new functionalities or services are added.  

---

## Page 7

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Overview 7 
 
NETTING INTERACTIVE MESSAGE OVERVIEW 
Message Overview 
The Comparison Interactive Messaging (supporting trade input and trade status output) currently utilized by 
[[GSD]] in support of its comparison process are message types: 
• MT515 – The MT515 (Trade Input) message is used by [[GSD]] Members to submit trades to [[GSD]], enter 
trade cancellations, modify [[Member]] reference numbers on previously submitted trades and to submit DK 
notification on trades submitted against them.  
• MT509 – The MT509 Trade Status Message is used by [[GSD]] to communicate the status of each input 
(submission, modification, cancellation or DK) message that has been submitted to [[GSD]] for processing by 
a [[GSD]] [[Member]].  
• MT518 – The MT518 Message is used by [[GSD]] to communicate to [[GSD]] Members that a trade input 
(submission, modification, cancellation or DK) message has been submitted for a transaction for which 
they are a party to. 
• MT599 – The MT599 Message is used by [[GSD]] to communicate to [[GSD]] Members system administrative 
information such as system availability and major system events to Members. 
 
Details on the Comparison Interactive Messaging can be found in the latest version of the “[[GSD]] Interactive 
Messaging (IM) [[Member]] Specifications for Comparison Input and Output” document. 
 
The Netting Interactive Messaging (supporting netting and [[settlement]] output), currently utilized by [[GSD]] in 
support of its netting and [[settlement]] process are message types: 
• MT509 – The MT509 Netting Status Message is used by [[GSD]] to communicate to [[GSD]] Members 
additional trade/event changes on trades related to the netting process. These netting output related 
messages will be sent in addition to the MT509 comparison messages and are not a replacement of any 
status messages previously defined or communicated. 
• MT548 – The MT548 [[settlement]] Status Message is used by [[GSD]] to notify [[GSD]] Members of the following 
clearance and [[settlement]] events: 
o Creation of [[obligations]] to be Settled (instructions to be sent by the [[GSD]] [[Member]] to their Clearing 
bank for the purposes of [[settlement]]) 
o Cancellation of Clearance Instructions  
o Clearance of an Obligation 
• MT590 – The MT590 Advice of Charges, Interest and Other Adjustments is used by [[GSD]] to communicate 
to [[GSD]] Members the following events: 
o Coupon/Maturity Debit or Credit related to an outstanding Repo Transaction or Failed [[securities]] 
[[settlement]] Obligation. 
o Per Trade Forward [[Margin]] Debit or Credit. 
• MT950 – The MT950 Statement Message is used by [[GSD]] to provide [[GSD]] Members with the following 
Funds [[settlement]] and Reconciliation information: 

---

## Page 8

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Overview 8 
 
o [[participant]] Net Summary - This message reflects the components of each [[Member]]’s Funds 
[[settlement]] Obligation. 
o Security Net Summary - This message provides to each [[Member]] a balancing and reconciliation tool 
for Money Movements and Positions on a per security basis. 
 
The upcoming sections will contain message formatting information and the detailed specifications for the 
MT509 (Netting), MT548, MT590 and MT950 Messages. 
Message Formatting Structure 
This document presents specifications for the SWIFT Message Types previously mentioned. Two of the 
message types (MT509 and MT548) utilize ISO 15022 Formats. The other two message types (MT590 and 
MT950) being used to support the remainder of [[GSD]] netting output [[DO]] not always adhere to the same 
message structure specifications. The MT590 and MT950 use an older SWIFT Format, ISO 7775, which has 
the following “structural” differences from the other formats used: 
• There are no Beginning and End-of-Block Tags (16R and 16S). 
• Tags [[DO]] not always include the optional one-character suffix to specify the format of the field. 
• There are no generic fields, qualifiers, [[issuer]] codes or repeating subsequences. 
• Date fields may be in six, rather than eight-character formats.  
 
A [[BASIC]] overview of the ISO 15022 Message Structure can be found below.  
Formatting Structure Overview 
This section of the document provides some background information that may be useful for interpreting the 
detailed message specifications that follow. Much of the information that appears in this section of the 
document has been derived from the “SWIFT Standards Category 5 [[securities]] Market Message Usage 
Guidelines - September, 2000 Edition.” 
ISO 15022 SWIFT message formats are constructed using a modular methodology based on the premise that 
information can be identified and programmed once, then reused wherever needed. Using this approach, data 
is configured into logical groups (e.g., generic fields and blocks) according to business purpose. These groups 
are then uniquely identified (using tags, qualifiers and start/end of block designators) so that they can be used 
whenever needed to fulfill particular business purposes across a number of messages without requiring 
extensive reprogramming. 
If the [[BASIC]] message structure were diagramed from the top down (going from the more general to the more 
specific), you would have a Message Header followed by one or more information blocks (potentially containing 
sub-blocks), composed of one or more fields. Each of these components is defined below. 
Note: 
While [[GSD]] has elected to use SWIFT standardized messages, it is not utilizing the SWIFT network. [[GSD]] utilizes its 
proprietary network for communication between [[GSD]] and its members. The messages are intended, however, to be 
compliant with SWIFT standards. 

---

## Page 9

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Overview 9 
 
Message Header 
The message header specifies the sending and receiving parties of the message and provides the message 
type. The message header is the first component of every message and are in a fixed format. The header is 
populated as a continuous string of data (complying with the requirement specifying the allowable characters 
for a given line in a message) and terminates as a regular data field (with a carriage return line feed “CRLF”). 
Within the header is a “Password” field, which is a unique identifier provided by [[GSD]] for each [[Member]] to input 
on their MT515 messages sent to [[GSD]]. For all [[GSD]] outbound netting messages, the password field will be 
blank-filled. 
Message Header Format 
The Message Type Field contained in the message header defines the purpose of the message. This message 
header will be utilized on [[GSD]] netting interactive messages: MT509, MT548, MT590 and MT950.  
M/O Tag Block/Qualifier Subqualifier/Options Field Description Data Format 
    Message Header  
M    Password 12!c 
M    Sender 8!c 
M    Message Type 3!n/3!n/4!c 
M    Receiver 8!c 
Blocks and Sub-blocks 
A block may be defined as a group of fields containing related business information that is framed by Start of 
Block and End of Block designators. The use of a block is not restricted to any given message. It can be 
reused across a number of messages and combined with other blocks to fulfill a variety of business purposes. 
For example, the General Information (GENL) block found in the outbound netting messages, contains general 
information, such as trade and/or [[obligations]] reference numbers.  
Each message contains one or more blocks. A typical message contains a General Information block, followed 
by a series of detail blocks. These blocks may be mandatory or optional within a particular message, and are 
structured as follows: 
• A Start of Block designator (represented by the tag 16R), indicating the start of a group of related 
information 
• One or more sub-blocks and/or fields 
• An End of Block designator (represented by the tag 16S), indicating the end of a group of related 
information. 
  

---

## Page 10

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Overview 10 
 
Fields 
There are two types of fields: generic fields and discrete fields. As the names imply, generic fields are multi-
purpose fields used across messages and message types, whereas discrete fields in messages are limited to a 
single purpose. Generic fields further support the flexibility and modular message structure of the message 
formats. Each generic field is a [[BASIC]] group of business data that is common throughout all messages, such as 
date and/or [[settlement]] amount. 
At a minimum, each field is composed of an identifying tag and its associated field data. A tag may be thought 
of simply as a 2-digit number that represents the type of data contained in the field followed by an alpha 
character that provides format information associated with the field contents. For example, 98A is the generic 
tag used to indicate a date/time field in a particular format (YYYYMMDD).1 The format for a tag includes two 
delimiters – one to indicate the start of the tag, and a second to indicate the end of the tag. These delimiters 
are indicated using a colon. Continuing with 98A tag as an example, the proper format for the generic tag used 
to indicate a date in the YYYYMMDD format would be “:98A:”. 
Because there are a number of different types of dates that may be associated with any given trade, the 
generic field tag must be further described if it is to be useful. Qualifiers are used to provide this additional level 
of description. For example, the tag 98A followed by the qualifier SETT means that the corresponding field data 
is the [[settlement]] date for the clearance instruction on a MT548 message. Qualifiers for generic tags are always 
preceded by an additional colon “:”. 
The generic field for a [[settlement]] date of September 28, 2020 in the YYYYMMDD format, including the generic 
tag, the qualifier and the field data would be “:98A::SETT//20200928”. 
Although tags are numeric, they generally [[DO]] not need to be placed in sequence, except if there is a sequence 
dependency as part of the format. Tags that are part of a block must remain within the “start” and “end” block 
tags. 
  
 
1 The alpha character in the tag is used to indicate which format [[Option]] has been applied. If the alpha character in the tag is  lowercase in 
the SWIFT format documentation, this means that there are several format options for the field and that there is free choice to use any of 
these options. If the alpha character in the tag is uppercase, this means that, while there are several format options for the field, the [[Option]] 
designated by the uppercase alpha character must be used. For example, 98A refers to a date in the YYYYMMDD format. 98C refers to a 
date that also includes the time in the YYYYMMDDHHMMSS format. [[GSD]] has mandated the options that Members must use in the 
layouts.
 

---

## Page 11

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Overview 11 
 
Message Formatting Rules 
The following Message and Message Field rules apply to all interactive messages used to support [[GSD]]’s 
products and services: 
Message Rules 
Message Rules 
1 Direction Messages are sent either to or from [[GSD]] 
2 Variable Length All messages can vary in length up to a maximum allowable number of characters 
per message type 
3 Header All messages begin with a standard fixed length header 
4 Terminator All messages end with a standard terminator sequence reflected by a Carriage 
Return/Line Feed (“CRLF”) and a Dash (“–”) 
5 Message Type Each message belongs to a specified message type 
6 Message Fields A message is composed of one or more message fields 
7 Character Set A-Z, a-z, 0-9, white space and the following punctuation “:/,-” 
 
Message Field Rules 
Message Field Rules 
1 Field Tag Each field begins with a field tag 
2 Tag Format Each tag is composed of 2 digits and an optional character (2!c[1a]) 
3 Tag Delimiter Each tag is prefixed and suffixed by the character “:” (e.g., :23G:) 
4 Field Data Field data (including qualifiers and subqualifiers) immediately follows the tag suffix 
delimiter. Generic tags are prefixed by an additional “:” 
5 Data Format Data conforms to format rules for a specified tag 
6 Data Elements Field data may be divided into multiple elements or sub fields 
7 Qualifiers Qualifiers within a data field provide additional format definition. If a qualifier is used, 
it must appear immediately after the tag suffix delimiter (e.g., :98A::SETT). If further 
data is required after the qualifier, and the data complies with SWIFT standards, the 
qualifier is delimited by the characters “//” and the data follows (e.g., 
:98A::SETT//20200928 or :20C::MAST//202000928815). If the data is [[GSD]] specific, 
then the [[GSD]] [[issuer]] code is included (e.g., :95R::BUYR/GSCC/PART88T2). 
 Field Delimiter The field delimiter sequence is Carriage Return Line Feed , “CRLF”  (ASCII 
Character  13, ASCII Character 10). This sequence immediately follows the data. 
The combination of Carriage Return Line Feed, Colon (“CRLF:”) indicates the end of 
one field and the beginning of the next. 
  

---

## Page 12

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Overview 12 
 
Formatting Conventions 
All the layouts for each of the messages included in this document are organized using the following columns 
of data:  
Column Heading Description 
M/O The M/O column defines whether the field is always Mandatory or is Optional in the 
particular message according to SWIFT standards. This column does not provide 
information as to whether the field is required or optional for [[FICC]] [[GSD]]. Refer to 
Appendix A within the [[GSD]] Interactive Messaging (IM) [[Member]] Specifications for 
Comparison Input and Output” document, which provides a list of required fields for 
both REPO and CASH trades. 
Tag The Tag column defines the exact tag value that must precede the field. Tags are 
always delimited by “:” (meaning a “:” would be the character immediately before and 
after the tag (e.g., “:98A:” indicates a date with a format of YYYYMMDD will follow). 
Block/Qualifier The Block or Qualifier column specifies the Block Name in the case of a start of block 
(16R) or end of block (16S) tag. Otherwise, it specifies the required qualifier for the 
tag (e.g., :98A::SETT indicates a [[settlement]] Date field). 
Subqualifier/Options The Options column specifies the different options available for individual qualifiers for 
a tag. Each tag, qualifier and [[Option]] combination uniquely specifies a data element 
(e.g., 22H::REDE//RECE indicates the clearance instruction being reported is for an 
obligation to “Receive”). 
Field Description The Field Description column provides a text description of the purpose or use of a 
data field. 
Data Field Format The Data Format column specifies the size and characters allowed within a data field, 
as specified by SWIFT. The Field Specifications that follow each layout indicate how 
each field should be populated for [[GSD]] output.  
 
The Data Format field on the layouts is intended to reflect the format of the data that Members and/or [[GSD]] 
must use to populate the field. For example, the format for the [[settlement]] Date field (:98A::SETT//20200928) is 
reflected as “YYYYMMDD.” 
All fields are, by definition, variable in length with a maximum field size specified, unless a fixed length format is 
defined by inclusion of the “!”, in which case the size specified is the fixed field size. In the case where the data 
value in the fixed length field is smaller than the field size specified, the data should be left justified with trailing 
blanks. There are not only differences in data field sizes (as noted previously in this document), but field 
formats can also be different for the population of the SWIFT standard. For example, date fields on the [[GSD]] 
MT509 and MT548 SWIFT records in this document are reflected as “YYYYMMDD” rather than the SWIFT 
format of “MMDDYYYY”, which also is used on the [[GSD]] proprietary layout.  
In addition, all fields on the SWIFT messages are left justified, and if the field has a decimal format (d), it must 
use a decimal comma, rather than a decimal (i.e. 50.01 should be 50,01.). 
  

---

## Page 13

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Overview 13 
 
As a supplement to the message format, a detailed description of each field format is shown in the below table. 
The table displays when a field can contain optional elements, defines the fields usage and shows an example 
for each field. The following characters may appear in the Data Format Column or in any discussion of data 
format and content: 
Character Meaning Example Format Example Usage 
A  Upper Case Alpha Characters  6a  ABCDEF  
C  Alphanumeric Characters (upper case only)  6c  AB12EF  
D  Decimal Number (decimal comma)  15d  2035,45  
E  Space  1e  (1blank space)  
N  Numeric Characters  8n  20200928  
X  Any Printable ASCII Symbol  20x  Anytime & Anyplace  
/  The literal “/” as a separator  6c/2a  AB12EF/NY  
[ ]  Optional element format  [/4c]  [optional data]  
[N]  Optional “sign” (negative) format  [N]  :92A::REPO//N3,45  
!  Fixed length field  12!c  ABCDEFGHIJKL  
 
Typical Message Form 
Form Example 
<SENDER><MESSAGE TYPE> <RECEIVER><cr><lf> 
:<BLOCK START TAG>:<BLOCK NAME><cr><lf> 
:<GENERIC TAG 1>::QUALIFIER//DATA FIELD 1 <cr><lf> 
:<TAG 2>:DATA FIELD 2<cr><lf> 
:<GENERIC TAG 3>::QUALIF/[[issuer]] CODE/DATA FIELD 3<cr><lf> 
:<BLOCK START TAG>:<BLOCK NAME><cr><lf> 
:<GENERIC TAG 4>::QUALIFIER//DATA FIELD 4<cr><lf> 
:<BLOCK END TAG>:<BLOCK NAME><cr><lf> 
:<BLOCK END TAG>:<BLOCK NAME><cr><lf> 
509/000/GSCC95XX 
:16R:GENL 
:20C::SEME//000315976306 
:23G:INST 
:98C::PREP//20180928081211 
:16R:LINK 
:20C::MAST//2B00076976315 
:16S:LINK 
:16S:GENL 
 
Generic fields, as previously described in this document, are designed to serve a particular function, with a 
qualifier code specifying a specific business purpose to that function. In the preceding example, the “20C” tag 
is a generic reference number, and the “SEME” qualifier in the GENL block indicates that this is the Sender’s 
Message identifier. In the LINK subsequence, however, 20C is used to provide a Master Reference Number 
([[Member]]’s External Reference). The generic fields can thereby be designed to be reused for creating or 
validating generic fields as the fields are reused within a message, or across messages. 
  

---

## Page 14

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Overview 14 
 
[[GSD]] Application Modules 
Even though this document is meant to provide message specification details relating to the support of [[GSD]]’s 
Netting system processing, various [[GSD]] application modules related to comparison, netting and/or [[settlement]] 
system processing will be reflected in the flow section (Appendix A) of this document. “GSCCTRRS” ([[GSD]] 
Trade Registration and Reconciliation System) or “GCFCTRRS” (GCF/CCIT Trade Registration and 
Reconciliation System) can be found in the Message Headers, representing either the receiver or the sender 
and will always be the source (sender) of all outbound comparison related SWIFT messages generated for 
Members. However, the mnemonic GSCCTRRS will be found in the Message Headers, representing the 
source (sender) of all outbound netting related SWIFT formatted messages discussed in this document. 
 
  

---

## Page 15

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 15 
 
NETTING INTERACTIVE MESSAGE SPECIFICATIONS – 
MT509 
This section contains the detailed specifications including layout and field descriptions for MT509 Messages 
supporting netting output for [[GSD]]’s products and services.  
Note: 
Where we have included new fields or have amended already existing fields within the MT509 Netting Status Messages, 
such updates have been indicated and highlighted in yellow and italics in the below section. 
MT509 Netting Status Message Description 
The SWIFT MT509 Message is specified as a Netting Status Message and will be used by [[GSD]] as a means to 
communicate status messages related to the [[GSD]] Netting process. These messages are generated in addition 
to those MT509 Trade Status Messages specified for the [[GSD]] Comparison process as noted in the “[[GSD]] 
Interactive Messaging (IM) [[Member]] Specifications for Comparison Input and Output” document. The MT509 
Message does not contain full trade details, but rather provides the trade status along with the full set of 
reference numbers to enable the [[Member]] to identify the trade being reported on (e.g., [[Member]] Reference 
Number, Secondary Reference Number, Counterparty External Reference Number, [[Broker]] Reference Number 
(or [[Broker]] TID) and the [[GSD]] Assigned Reference Number (Receiver’s TID), where appropriate).  
Field 25D in the Status (STAT) Block will continue to indicate to the recipient the type of record being sent. 
Because these MT509 Messages [[DO]] not contain “Ack” or “Nack” Statuses, many fields are not applicable for 
the messages in this Netting Output Specification and have therefore been omitted from this document. They 
still continue to be applicable for Comparison related messages as stated in the Comparison specifications 
referenced above. The qualifiers representing the type of record being sent in Field 25D, are shown below. 
As it relates to [[GSD]]’s Netting process, MT509 Messages will be generated for each of the following netting 
statuses seen below: 
Message Type This message will be sent to: 
Trade Bound to Net 
(:25D::IPRC/GSCC/NBTD) 
the submitting party indicating that the trade is anticipated to be net settled 
by [[GSD]]. 
Trade Comparison Only 
(:25D::IPRC/GSCC/NNCO) 
the submitting party to indicate that that the trade is not netting eligible. 
Buy/Sell Transaction in Net 
(:25D::IPRC/GSCC/NECT) 
the submitting party indicating that the Buy/Sell Transaction has been Net 
Settled. 
Repo Start Leg in Net 
(:25D::IPRC/GSCC/NESL) 
the submitting party indicating that the Repo Start Leg has been Net Settled. 
Repo Close Leg in Net 
(:25D::IPRC/GSCC/NECL) 
the submitting party indicating that the Repo Close Leg has been Net 
Settled. 

---

## Page 16

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 16 
 
Forward Trade Pended / No Longer in 
Net-Repo [[collateral]] Matured-No New 
[[collateral]] Assigned 
(:25D::IPRC/GSCC/NNNC) 
the submitting party indicating that the underlying Repo [[collateral]] has 
matured, and no new [[collateral]] has been assigned to the trade. The trade is, 
therefore, no longer included in [[GSD]]’s netting process. 
Forward Trade Pended / No Longer in 
Net-No [[collateral]] Assigned to GC 
Trade (:25D::IPRC/GSCC/NNGC) 
the submitting party indicating that a previously Compared and Netted 
Forward Starting General [[collateral]] Repo did not have specific [[collateral]] 
assigned to the trade within the required time frame. Because of this, the 
trade is no longer included in [[GSD]]’s netting process. 
Forward Trade Pended / No Longer in 
Net-Trade Cancelled 
(:25D::IPRC/GSCC/NNTC) 
indicate that a previously Netted Trade has been Cancelled. This will be sent 
to the [[Member]] in addition to the related cancellation messages. 
Forward Trade Pended / No Longer in 
Net - [[GSD]] Excluded Trade 
(:25D::IPRC/GSCC/NNGD) 
inform the trade submitter that [[GSD]] has excluded the trade from the netting 
process. 
  

---

## Page 17

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 17 
 
MT509 Netting Status Message Specifications 
MT509 General Format 
This section provides the general format for the MT509 Message. As described in the MT509 Message 
Description, the MT509 will be sent by [[GSD]] to Members for the following trade status events: 
• Trade Bound to Net 
• Trade Comparison Only 
• Buy/Sell Transaction in Net 
• Repo Start Leg in Net 
• Repo Close Leg in Net 
• Forward Trade Pended / No Longer in Net-Repo [[collateral]] Matured-No New [[collateral]] Assigned 
• Forward Trade Pended / No Longer in Net-No [[collateral]] Assigned to GC Trade 
• Forward Trade Pended / No Longer in Net-Trade Cancelled 
• Forward Trade Pended / No Longer in Net-[[GSD]] Excluded Trade 
 
MT509 Netting Status Message 
General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
    Message Header  
M       Password 12!c 
M       Sender 8!c 
M       Message Type 3!n/3!n/4!c 
M       Receiver 8!c 
M :16R: GENL   Mandatory Start of Block   
M :20C: :SEME//   Sender's Message Reference 16x 
M :23G: INST   Message Function – Instruct 4!c 
O :98C: :PREP//   Preparation Date/Time YYYYMMDDHHMMSS 
M :16R: LINK   Mandatory Repeat Start of 
Block 
  
M :20C: :MAST//   Master ([[Member]])  Reference 
Number 
16x 
M :16S: LINK   End of Block   
M :16R: LINK   Mandatory Repeat Start of 
Block 
  
O :20C: :INDX//  Secondary Reference Number 16x 

---

## Page 18

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 18 
 
MT509 Netting Status Message 
General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
M :16S: LINK   End of Block   
M :16R: LINK   Mandatory Repeat Start of 
Block 
  
O :20C: :LIST//   [[GSD]] Assigned Reference 
Number (Receiver’s TID) 
16x 
M :16S: LINK   End of Block   
M :16R: LINK   Mandatory Repeat Start of 
Block 
  
O :13B: :LINK/ GSCC/CASH Linked Message – Cash Trade 
Indicator 
 or 
4!c 
   GSCC/REPO Repo Trade Indicator 
 or 
 
   GSCC/TRLK Locked-in Cash Trade Indicator 
or 
 
   GSCC/TRLR Locked-in Repo Trade Indicator 
or 
 
   GSCC/TRDC Demand Cash Trade Indicator 
or 
 
   GSCC/TRDR Demand Repo Trade Indicator  
O :20C: :BASK//   [[Broker]] Reference Number 16x 
M :16S: LINK   End of Block   
M :16R: STAT   Mandatory Start of Block   
M :25D: :IPRC/ GSCC/NBTD Trade Bound to Net                                                   
or  
4!c 
      GSCC/NNCO Trade Comparison Only                                     
or  
 
   GSCC/NECT Buy/Sell Transaction in Net 
or 
 
      GSCC/NESL Repo Start Leg in Net                        
or 
 
      GSCC/NECL Repo Close Leg in Net                     
or 
 

---

## Page 19

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 19 
 
MT509 Netting Status Message 
General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
   GSCC/NNNC Forward Trade Pended / No 
Longer in Net-Repo [[collateral]] 
Matured-No New [[collateral]] 
Assigned 
or 
 
   GSCC/NNGC Forward Trade Pended / No 
Longer in Net-No [[collateral]] 
Assigned to GC Trade  
or 
 
      GSCC/NNTC Forward Trade Pended / No 
Longer in Net-Trade Cancelled  
or 
 
   GSCC/NNGD Forward Trade Pended / No 
Longer in Net-[[GSD]] Excluded the 
Trade 
 
M :16S:  STAT       End of Block  
M :16S:  GENL   End of Block  
  

---

## Page 20

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 20 
 
MT509 Field Specifications 
This section provides the detailed field specifications for the MT509 Message.   
MT509 Netting Status Message  
Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format 
with trailing blanks, where required. 
Password   12!c This field will be blank-filled on all MT509 Messages. 
Sender   8!c “GSCCTRRS” ([[GSD]] Trade Registration and Reconciliation System) will always be the 
sender of the MT509 messages in this document. 
Message Type 3!n/3!n/4!c  The first 3 characters indicate to the recipient the message type (509); the second 3 
positions reflect the version of the message interface (currently always 000). The last 
4 characters indicate the [[issuer]] code to be used in the message (GSCC). 
Receiver 8!c [[Member]] [[ID]] 
GENL This mandatory block provides general information regarding the message. It appears only 
once in a Trade Status message. 
20C Sender's Message Reference  
• SEME// – This mandatory field contains the Sender’s ([[GSD]]) Message Reference Number.  
It is used on all messages sent by [[GSD]] and will contain a unique number to 
unambiguously identify each message. This is a Communications Message Number, not a 
Trade Number. 
e.g., :20C::SEME//GS3REFNUM2 
Note: 
This field must be populated with an uppercase alphanumeric value. It cannot contain symbols or 
hyphens. 
 
23G Function of the Message  
This mandatory field is used on all messages to identify the Function of the Message. It will either be 
the status of an Instruct or Modify. 
• INST – This qualifier will be used for Trade Status messages usually referring to Instructs or 
Modifies. All netting related MT509 messages defined in this document will use this qualifier. 
e.g., :23G:INST   
98C Preparation Date and Time  
• PREP// – This field contains the date and time the message sent by [[GSD]] was prepared.  
e.g., :98C::PREP//20200115110459 
Note: 
The “C” Format for this (98) tag indicates a Date/Time Format of “YYYYMMDDHHMMSS”. 
LINK The LINK Block will be repeated for as many reference qualifiers as need to be included in a 
Trade Status Message. Each subsequence contains reference numbers to identify the trade or 

---

## Page 21

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 21 
 
MT509 Netting Status Message  
Field Specifications 
Block/Tag Notes 
record for which the status is being reported. Each reference number will be enclosed within a 
Start Link Block (:16R:LINK) and End Link Block (:16S:LINK). All LINK repeating subsequences 
are within the GENL Block. 
20C Reference 
The Reference Numbers that have been provided by Members must contain uppercase alphanumeric 
characters and should not contain symbols. As indicated above, each Reference Number will be 
enclosed in a LINK Start and End Block. 
• MAST// – Master Reference Number - This qualifier contains the [[Member]]’s Reference 
Number for the trade (External Reference Number). The MAST qualifier will be present on all 
MT509’s messages specified in this document. 
• INDX// – Secondary Reference Number - This qualifier will contain the [[Member]]’s 
Secondary Reference Number on Trade Status Messages for Repo Transactions, where the 
number was originally provided by the [[Member]]. 
• LIST// – [[GSD]] Reference Number - This qualifier will contain the [[GSD]] Reference Number 
(TID - Transaction Identification) for the trade. 
• BASK// – [[Broker]] Reference Number - This field specifies the [[Member]]’s [[Broker]] Reference 
and will be reflected only where the receiving [[Member]] is a [[Broker]].  This field is required for 
[[Broker]] Submitted Trades. The [[Broker]] Reference Number field will be preceded by a Linked 
Message Trade Indicator field.                                                                                                          
e.g., :20C::MAST//PARTREF3 
Note:  
This field will be populated with an uppercase alphanumeric value. It will not contain symbols or 
hyphens except where the Reference Number has been assigned by [[GSD]]. 
13B Linked Message  
The Link Message field indicates the Message type number/message identifier of the message 
referenced in the linkage sequence in this sequence, this field indicates that the trade is being 
reported as a Repo and whether the trade is Demand. This field will only appear on a record if a 
[[Broker]] Reference Number (:20C::BASK//) is also included on the record. 
• LINK/GSCC/CASH – This qualifier/[[Option]] will be used on Cash trades.                              
• LINK/GSCC/REPO – This qualifier/[[Option]] will be used on Repo trades requiring Bilateral 
comparison. 
• LINK/GSCC/TRLK – This qualifier/[[Option]] will be used on Locked-in Cash trades   
• LINK/GSCC/TRLR – This qualifier/[[Option]] will be used on Locked-in Repo trades.                              
• LINK/GSCC/TRDC – This qualifier/[[Option]] will be used on Demand Cash trades. 
• LINK/GSCC/TRDR – This qualifier/[[Option]] will be used on Demand Repo trades. 
e.g., :13B::LINK/GSCC/TRDR 
Note:  
This field is not a LINK Block and will only appear when the trade being reported includes a [[Broker]] 
Reference. 

---

## Page 22

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 22 
 
MT509 Netting Status Message  
Field Specifications 
Block/Tag Notes 
STATUS The Status Block will appear on every MT509 message and will notify the [[Member]] of the type of 
MT509 record being sent, as well as the status of the trade, or record, that was submitted to 
[[GSD]]. 
25D Status Code 
The Status Code indicates the record type/type of Status Message being sent by [[GSD]]. The following 
are the various message types, which will be used for Interactive Messaging to support [[GSD]]’s netting 
output. 
• IPRC/GSCC/NBTD - This qualifier/[[Option]] is used to indicate to the submitter that [[GSD]] is 
intending to Net Settle the trade. 
•  IPRC/GSCC/NNCO - This qualifier/[[Option]] is used to indicate to the submitter that the trade is 
not netting eligible; it is considered by the [[GSD]] to be Comparison only.  
Note:  
The “IPRC/GSCC/NNCO" field will appear when the trade being reported is an As-of Overnight Repo 
Transaction where the Start Leg and End Leg of such transaction is eligible for [[settlement]] through 
[[GSD]]'s Same-Day Settling Service. 
• IPRC/GSCC/NECT - This qualifier/[[Option]] is used to indicate to the submitter that the Buy/Sell 
Transaction has been Net Settled. 
• IPRC/GSCC/NESL - This qualifier/[[Option]] is used to indicate to the submitter that the Repo 
Start Leg has been Net Settled. 
• IPRC/GSCC/NECL - This qualifier/[[Option]] is used to indicate to the submitter that the Repo 
Close Leg has been Net Settled. 
• IPRC/GSCC/NNNC - This qualifier/[[Option]] is used to indicate to the submitter that the trade is 
no longer netting eligible because the Repo [[collateral]] has matured, and no new [[collateral]] 
has been assigned. 
• IPRC/GSCC/NNGC - This qualifier/[[Option]] is used to indicate to the submitter that the trade is 
no longer netting eligible because no specific [[collateral]] has been assigned to a GC Repo 
Transaction. 
• IPRC/GSCC/NNTC - This qualifier/[[Option]] is used to indicate to the submitter that the trade is 
no longer netting eligible because it has been Cancelled. 
• IPRC/GSCC/NNGD - This qualifier/[[Option]] is used to indicate to the submitter that [[GSD]]  
has excluded the trade from the netting process. 
 
e.g., :25D::IPRC/GSCC/NBTD   
 
 
 
 
  

---

## Page 23

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 23 
 
MT509 Field Analysis 
This section contains an analysis of the fields that may be found on each MT509 Netting Message. For each applicable record type, a check mark will 
be found where it is possible for that field to appear on that record. It should be noted, however, that where a check mark appears, the check mark is 
not intended to indicate that a field is mandatory for a given record type. Where there is no check mark in a given box, that field is not applicable for the 
record type in question. 
MT509 Netting Status Message  
Field Analysis 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description IPRC/ 
GSCC/ 
NBTD 
IPRC/ 
GSCC/ 
NNCO 
IPRC/ 
GSCC/ 
NECT 
IPRC/ 
GSCC/ 
NESL 
IPRC/ 
GSCC/ 
NECL 
IPRC/ 
GSCC/ 
NNNC 
IPRC/ 
GSCC/ 
NNGC 
IPRC/ 
GSCC/ 
NNTC 
IPRC/ 
GSCC/ 
NNGD 
        Message Header                  
M       Password          
M       Sender          
M       Message Type          
M       Receiver          
M :16R: GENL   Mandatory Start of Block                  
M :20C: :SEME//   Sender's Message 
Reference 
         
M :23G: INST   Message Function – Instruct          
O :98C: :PREP//   Preparation Date/Time          
M :16R: LINK   Repeat Block Start                  
M :20C: :MAST//   Master ([[Member]]) Reference 
Number 
         
M :16S: LINK   End of Block                  
M :16R: LINK   Repeat Block Start                  

---

## Page 24

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 24 
 
MT509 Netting Status Message  
Field Analysis 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description IPRC/ 
GSCC/ 
NBTD 
IPRC/ 
GSCC/ 
NNCO 
IPRC/ 
GSCC/ 
NECT 
IPRC/ 
GSCC/ 
NESL 
IPRC/ 
GSCC/ 
NECL 
IPRC/ 
GSCC/ 
NNNC 
IPRC/ 
GSCC/ 
NNGC 
IPRC/ 
GSCC/ 
NNTC 
IPRC/ 
GSCC/ 
NNGD 
O :20C: :INDX//   Secondary Reference 
Number 
         
M :16S: LINK   End of Block                  
M :16R: LINK   Repeat Block Start                  
O :20C: :LIST//   [[GSD]] Assigned Reference 
Number (Receiver’s TID) 
         
M :16S: LINK   End of Block                  
M :16R: LINK   Repeat Block Start                  
O :13B: :LINK/ GSCC/CASH Linked Message – Cash 
Trade Indicator 
 or 
         
      GSCC/REPO Repo Trade Indicator 
 or 
         
   GSCC/TRLK Locked-in Cash Trade 
Indicator 
or 
         
   GSCC/TRLR Locked-in Repo Trade 
Indicator 
or 
         
   GSCC/TRDC Demand Cash Trade 
Indicator 
or 
         

---

## Page 25

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 25 
 
MT509 Netting Status Message  
Field Analysis 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description IPRC/ 
GSCC/ 
NBTD 
IPRC/ 
GSCC/ 
NNCO 
IPRC/ 
GSCC/ 
NECT 
IPRC/ 
GSCC/ 
NESL 
IPRC/ 
GSCC/ 
NECL 
IPRC/ 
GSCC/ 
NNNC 
IPRC/ 
GSCC/ 
NNGC 
IPRC/ 
GSCC/ 
NNTC 
IPRC/ 
GSCC/ 
NNGD 
   GSCC/TRDR Demand Repo Trade 
Indicator 
         
O :20C: :BASK//   [[Broker]] Reference Number           
M :16S: LINK   End of Block                  
M :16R: STAT   Repeat Block Start                  
M :25D: :IPRC/ GSCC/NBTD Trade Bound to Net                                                   
or  
                
      GSCC/NNCO Trade Comparison Only                                     
or  
      
 
    
 
  
   GSCC/NECT Buy/Sell Transaction in Net 
or 
         
      GSCC/NESL Repo Start Leg in Net                        
or 
                
      GSCC/NECL Repo Close Leg in Net                     
or 
         
 
      
      GSCC/NNNC Forward Trade Pended / No 
Longer in Net-Repo 
[[collateral]] Matured-No New 
[[collateral]] Assigned 
or 
           
 
    
      GSCC/NNGC Forward Trade Pended / No 
Longer in Net-No [[collateral]] 
Assigned to GC Trade  
or 
               
 

---

## Page 26

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT509 26 
 
MT509 Netting Status Message  
Field Analysis 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description IPRC/ 
GSCC/ 
NBTD 
IPRC/ 
GSCC/ 
NNCO 
IPRC/ 
GSCC/ 
NECT 
IPRC/ 
GSCC/ 
NESL 
IPRC/ 
GSCC/ 
NECL 
IPRC/ 
GSCC/ 
NNNC 
IPRC/ 
GSCC/ 
NNGC 
IPRC/ 
GSCC/ 
NNTC 
IPRC/ 
GSCC/ 
NNGD 
      GSCC/NNTC Forward Trade Pended / No 
Longer in Net-Trade 
Cancelled  
or 
                 
   GSCC/NNGD Forward Trade Pended / No 
Longer in Net-[[GSD]] Excluded 
the Trade 
         
M :16S: STAT   End of Block                  
M :16S: GENL   End of Block                  

---

## Page 27

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 27 
 
NETTING INTERACTIVE MESSAGE SPECIFICATIONS – 
MT548 
This section contains the detailed specifications including layout and field descriptions for MT548 Messages 
supporting comparison input and output for [[GSD]]’s products and services. 
Note:  
Where we have included new fields or have amended already existing fields within the MT548 [[settlement]] Status 
Messages, such updates have been indicated and highlighted in yellow and italics in the below section. 
MT548 [[settlement]] Status Message Description 
The SWIFT MT548 Message is specified as a [[settlement]] Status and Processing Advice / Clearance 
Instruction. Field 22F SETR in the [[settlement]] Transaction Details (SETTRAN) Block indicates to the recipient 
the type of record being sent. The qualifiers representing the type of record being sent in Field 22F, are shown 
below. The MT548 Message will be sent to support the following record types: 
• MT548 Clearance Instruction – The Clearance Instruction Message will be sent by [[GSD]] to notify the 
[[Member]] of those Clearance Instructions that must be sent by the [[Member]] to their Clearing bank to satisfy 
[[GSD]] [[obligations]]. 
• MT548 Clearance Instruction Cancel – The Clearance Instruction Cancel Record will be sent to the 
[[Member]] in the event that a previously sent Clearance Instruction has been canceled. The Cancel Record 
will be an exact duplicate of the original Clearance Instruction with the exception of required fields to 
indicate the record is a Cancellation. (Fields :23G: CAST in the General (GENL) block, and 
:25D::IPRC//CAND in the Status (STAT) block denote that the record is a cancel.) 
• MT548 Cleared Obligation – This message will be sent by [[GSD]] to notify the [[Member]] that an Obligation 
has been cleared. 
 
  

---

## Page 28

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 28 
 
The following MT548 Clearance Instruction (or Clearance Instruction Cancel) Messages will be generated to 
notify Members of their required [[obligations]] to be Settled (or Cancellation of those Clearance Instructions): 
Message Type This message will be sent to: 
“Next Day” 
(:22F::SETR/GSCC/NETX) 
the [[Member]] indicating that the Obligation is to be settled. 
Note: 
“Next Day” (NETX) will be used to support Next Day, as well as Same Day, 
[[settlement]] instructions, where applicable. 
Fail (:22F::SETR/GSCC/FOBL) the [[Member]] indicating that the Obligation is based on a Fail. 
Held Fail 
(:22F::SETR/GSCC/HFOB) 
the [[Member]] indicating that the Obligation is a Held Fail/Fail held from the 
previous night’s netting process. 
[[Broker]] Fail 
(:22F::SETR/GSCC/BKFL) 
the [[Member]] indicating that the Obligation is based on a [[Broker]] Fail.  
Repo Substitution 
(:22F::SETR/GSCC/SUBS) 
the [[Member]] indicating that the Obligation is based on a Repo Substitution. 
 
 The following MT548 Cleared Obligation Messages will be generated to notify Members that their [[obligations]] 
have Settled/Cleared: 
Message Type This message will be sent to: 
Paired Off 
 (:22F::SETR//PAIR) 
the [[Member]] indicating that the Obligation settled/cleared via the Pair-Off Service. 
Bought In 
(:22F::SETR/GSCC/BTIN) 
the [[Member]] indicating that [[GSD]] has Bought In the [[securities]] for the Obligation to 
be settled/cleared. 
Held Fail Matured 
(:22F::SETR/GSCC/HDFM) 
the [[Member]] indicating that the [[securities]] for the Held Fail Obligation Matured. 
Matured 
(:22F::SETR/GSCC/MATR) 
the [[Member]] indicating that the [[securities]] for the Fail Obligation has Matured. 
Cleared 
(:22F::SETR/GSCC/CLRD) 
the [[Member]] indicating that the Obligation pending [[settlement]], has Cleared. 
Netted  
(:22F::SETR/GSCC/FLRN) 
the [[Member]] indicating that the Obligation pending [[settlement]], has been Netted. 
 
  

---

## Page 29

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 29 
 
MT548 [[settlement]] Status Message Specifications 
MT548 General Format 
This section provides the general format for the MT548 Message. The general format is separated into two 
categories; 1) Clearance Instruction / Clearance Instruction Cancel and 2) Cleared Obligation. As described in 
the MT548 Message Description in this document, the MT548 will be sent by [[GSD]] to the [[Member]] for the 
following [[settlement]] events: 
For Clearance Instruction / Clearance Instruction Cancel 
• “Next Day” 
• Fail  
• Held Fail  
• [[Broker]] Fail  
• Repo Substitution  
 
For Cleared Obligation 
• Paired Off  
• Bought In  
• Held Fail Matured  
• Fail Matured  
• Cleared  
• Fail Netted  
 
  

---

## Page 30

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 30 
 
MT548 [[settlement]] Status Message (Clearance Instruction & Clearance Instruction Cancel)  
General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
        Message Header   
M        Password 12!c 
M        Sender 8!c 
M        Message Type 3!n/3!n/4!c 
M        Receiver 8!c 
M :16R: GENL   Mandatory Start of Block   
M :20C: :SEME//   Sender's Message Reference 16x 
M :23G: INST   Message Function – Instruct  
or 
4!c 
    CAST   Cancel   
O :98C: :PREP//   Preparation Date/Time YYYYMMDDHHMMSS 
M :16R: LINK   Mandatory Repeat Start of Block   
M :20C: :POOL//   Pool Reference Number ([[GSD]] 
Reference Number of Obligation to 
be Cleared) (OID) 
16x 
M :16S: LINK   End of Block   
M :16R: LINK   Mandatory Repeat Start of Block   
O :20C: :PREV//   Previous Reference Number 
(Previous [[GSD]] Reference Number 
of the Obligation to be Cleared) 
(OID) 
16x 
M :16S: LINK   End of Block   
M :16R: LINK   Mandatory Repeat Start of Block   
O :20C: :RELA//   Related Reference Number 
(Original [[GSD]] Obligation 
Reference Number) (OID) or [[GSD]] 
Reference Number (Receiver's TID 
or [[Broker]] Counterparty's TID) 
16x 
M :16S: LINK   End of Block   
M :16R: STAT   Mandatory Repeat Start of Block   
M :25D: :IPRC/ GSCC/CITS Status – Instruction to be Sent to 
Clearing Facility 
or 
4!c 

---

## Page 31

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 31 
 
MT548 [[settlement]] Status Message (Clearance Instruction & Clearance Instruction Cancel)  
General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
      /CAND Cancellation of a Previously Sent 
Clearance Instruction 
  
M :16R: REAS   Optional Repeat Start of Block    
M :24B: :CAND/ GSCC/GSER Reason Code 4!c 
M :16S: REAS   End of Block   
M :16S: STAT   End of Block   
M :16S: GENL   End of Block   
M :16R: SETTRAN   Optional Start of Block    
M :35B: /US/   Identification of Financial 
Instrument/Security ([[CUSIP]]) 
4*35x 
M :36B: :SETT// FAMT/ Quantity of Financial Instrument/ 
Security to be Settled 
15d 
O :19A: :SETT// USD [[settlement]] Amount 15d 
M :97B: :SAFE/ GSCC/PART/ Safekeeping Account - [[GSD]] 
[[Member]] [[ID]] 
35x 
M :22F: :SETR/ GSCC/NETX Type of [[settlement]] Transaction - 
Same Day or Next Day 
or        
4!c 
   GSCC/FOBL Type of [[settlement]] Transaction – 
Fail 
or        
 
   GSCC/HFOB Type of [[settlement]] Transaction – 
Held Fail 
or        
 
   GSCC/BKFL Type of [[settlement]] Transaction – 
[[Broker]] Fail 
or        
 
   GSCC/SUBS Type of [[settlement]] Transaction – 
Repo Substitution 
 
M :22H: :REDE// RECE Receive/Deliver Indicator – 
Receive 
or 
4!c 
      DELI Deliver   
M :22H: :PAYM// APMT Payment Indicator – vs. Payment 4!c 

---

## Page 32

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 32 
 
MT548 [[settlement]] Status Message (Clearance Instruction & Clearance Instruction Cancel)  
General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
M :98A: :SETT//   [[settlement]] Date  YYYYMMDD  
M :16R: SETPRTY   Optional Repeat Start of Block    
M :95R: :DEAG/ GSCC/ Party – Delivering Agent (or [[Seller]]) 
and Clearing Instruction 
Information for [[GSD]] 
or 
34x                                        
(9!c25x) 
    :REAG/ GSCC/ Receiving Agent (or [[Buyer]]) and 
Clearing Instruction Information for 
[[GSD]] 
  
M :16S: SETPRTY   End of Block   
M :16R: SETPRTY   Optional Repeat Start of Block    
M :95R: :DEI1/ GSCC/ Party – Delivering [[Broker]] 
Counterparty [[ID]] 
or 
34x                                         
M   :REI1/ GSCC/ Party – Receiving [[Broker]] 
Counterparty [[ID]] 
  
M :16S: SETPRTY   End of Block   
M :16S: SETTRAN   End of Block   
  

---

## Page 33

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 33 
 
MT548 [[settlement]] Status Message (Cleared Obligation)  
General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
        Message Header   
M       Password 12!c 
M       Sender 8!c 
M       Message Type 3!n/3!n/4!c 
M       Receiver 8!c 
M :16R: GENL   Mandatory Start of Block   
M :20C: :SEME//   Sender's Message Reference 16x 
M :23G: INST   Message Function – Instruct 4!c 
O :98C: :PREP//   Preparation Date/Time YYYYMMDDHHMMSS 
M :16R: LINK   Mandatory Repeat Start of Block   
M :20C: :POOL//   Pool Reference Number ([[GSD]] 
Reference Number of Obligation 
Cleared) (OID) 
16x 
M :16S: LINK   End of Block   
M :16R: LINK   Mandatory Repeat Start of Block   
O :20C: :PREV//   Previous Reference Number 
(Previous [[GSD]] Reference Number 
of the Obligation Cleared) (OID) 
16x 
M :16S: LINK   End of Block   
M :16R: LINK   Mandatory Repeat Start of Block   
O :20C: :RELA//   Related Reference Number 
(Original [[GSD]] Obligation 
Reference Number) (OID) or [[GSD]] 
Reference Number (Receiver's TID 
or [[Broker]] Counterparty's TID) 
16x 
M :16S: LINK   End of Block   
M :16R: STAT   Mandatory Repeat Start of Block   
M :25D: :SETT/ GSCC/CLOB Status – Cleared Obligation 
Record 
4!c 
M :16S: STAT   End of Block   
M :16R: GENL   End of Block   
M :16R: SETTRAN   Optional Start of Block    

---

## Page 34

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 34 
 
MT548 [[settlement]] Status Message (Cleared Obligation)  
General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
M :35B: /US/   Identification of Financial 
Instrument/Security ([[CUSIP]]) 
4*35x 
M :36B: :SETT// FAMT/ Quantity of Financial Instrument/ 
Security Settled 
15d 
O :19A: :SETT// USD [[settlement]] Amount 15d 
M :97B: :SAFE/ GSCC/PART/ Safekeeping Account – [[GSD]] 
[[Member]] [[ID]] 
35x 
M :22F: :SETR/ /PAIR Type of [[settlement]] Transaction – 
Paired-Off 
or 
4!c 
      GSCC/BTIN Type of [[settlement]] Transaction – 
Bought In 
or 
  
      GSCC/HDFM Type of [[settlement]] Transaction – 
Held Fail Matured 
or 
  
      GSCC/MATR Type of [[settlement]] Transaction – 
Matured 
or 
  
      GSCC/CLRD Type of [[settlement]] Transaction – 
Cleared 
or                                
  
   GSCC/FLRN Type of [[settlement]] Transactions – 
Fail Netted 
 
M :22H: :REDE// RECE Receive/Deliver Indicator – 
Receive 
or 
4!c 
      DELI Deliver   
M :22H: :PAYM// APMT Payment Indicator – vs. Payment 4!c 
M :98A: :SETT//   [[settlement]] Date  YYYYMMDD  
O :70E: :SPRO// GSCC [[settlement]] Instruction Processing 
Narrative  
(10*35x) 
   /RSTTFAMT Quantity of Financial Instrument 
Remaining to be Settled 
15d 
   /RSMTUSD [[settlement]] Amount Remaining  15d 

---

## Page 35

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 35 
 
MT548 [[settlement]] Status Message (Cleared Obligation)  
General Format 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field Format 
      /DCDFUSD Debit Clearance Difference 
or 
15d 
      /CCDFUSD Credit Clearance Difference   
   /DFMKUSD Debit Fail Mark Due to Netting 
or 
15d 
   /CFMKUSD Credit Fail Mark Due to Netting  
      /OPARFAMT Opening Par  15d 
      /OPSTUSD Opening [[settlement]] Amount 15d 
M :16S: SETTRAN   End of Block   
  

---

## Page 36

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 36 
 
MT548 Field Specifications 
This section provides the layout and field descriptions for the MT548 Message. The MT548 field specifications 
is separated into two categories; 1) Clearance Instruction / Clearance Instruction Cancel and 2) Cleared 
Obligation.  
 
MT548 [[settlement]] Status Message (Clearance Instruction & Clearance Instruction Cancel)  
Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format 
with trailing blanks, where required. 
Password 12!c This field will be blank-filled on all MT548 Messages. 
Sender 8!c “GSCCTRRS” ([[GSD]] Trade Registration and Reconciliation System) will always be the 
sender of the MT548 messages in this document. 
Message 
Type 
3!n/3!n/4!c The first 3 characters indicate to the recipient the message type (548); the second 3 
positions reflect the version of the message interface (currently always 000); the last 4 
characters indicate the [[issuer]] code to be used in the message (GSCC). 
Receiver 8!c [[participant]] [[ID]] 
GENL  This mandatory block provides General Information regarding the message. It appears only 
once in an MT548 [[settlement]] Status Message. 
20C Sender's Message Reference 
• SEME// – This mandatory field contains the Sender’s ([[GSD]]) Message Reference Number.  It is 
used on all messages sent by [[GSD]] and will contain a unique number to unambiguously identify 
each message. (This is a Communications Message Number, not a Trade Number.) 
e.g., :20C::SEME//000000184321 
23G Function of the Message 
This mandatory field identifies the Function of the Message. It will either refer to an Instruction for 
[[Member]] Clearing Bank Instructions (INST) or to a Cancellation of a previously sent Clearance 
Instruction (CAST). 
• INST – This qualifier will be used to inform Members of [[GSD]] [[obligations]] and related Clearance 
Instructions. 
• CAST – This qualifier will be used to inform Members of Canceled Clearance Instructions 
previously sent by [[GSD]]. 
e.g., :23G:INST    
98C Preparation Date and Time 
• PREP// – This field will be reflected on all messages to indicate the Date and Time the 
message was prepared by [[GSD]]. 
e.g. :98C::PREP//20200214101328 
Note:  
The “C” Format for this (98) tag indicates a Date/Time Format of “YYYYMMDDHHMMSS”. 

---

## Page 37

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 37 
 
MT548 [[settlement]] Status Message (Clearance Instruction & Clearance Instruction Cancel)  
Field Specifications 
Block/Tag Notes 
LINK The LINK Block will be repeated for the many reference qualifiers required on a [[settlement]] 
Status Message. It is intended to provide the required information to identify the Obligation to be 
Cleared and the trade for which the Obligation was generated for. Each Reference Number will 
be enclosed within a Start Link Block (:16R:LINK) and End Link Block (:16S:LINK). All LINK 
repeating subsequences are within the GENL Block. At least one LINK sequence is required on 
the MT548 Message. 
20C Reference 
This field will be populated with the 11-character OID (Obligation Reference Number) assigned by [[GSD]] 
to each Obligation or the TID (Trade Reference Number) assigned by [[GSD]] to the trade for which Same-
Day Settling Obligation(s) were created for the purposes of [[settlement]] through the Same-Day Settling 
Service. As indicated above, each Reference Number will be enclosed in a LINK Start and End Block. 
Two of the reference qualifiers Current (POOL) and Previous (PREV) are assigned at the time an initial 
obligation is created. The third reference qualifier Original OID (RELA) is either the identifier assigned to 
the trade for which the created Obligation is to be settled for or the original identifier assigned to the 
obligation. All three fields will be populated on all [[settlement]] Status messages. 
• POOL – This qualifier is used for the [[GSD]] Obligation Reference Number of the Obligation to 
be Cleared (OID). It appears on all Clearance Instructions and reflects the reference of the 
current OID. Where an obligation is an original instruction, this number will be identical to the 
values in the Previous field on this record. 
• PREV – This qualifier is used to reflect the previous [[GSD]] Obligation Reference Number (OID). 
Where an obligation is an original instruction, this number will be identical to the values in the 
Current (POOL) field on this record. 
• RELA – This qualifier is used to provide the Original [[GSD]] Obligation Reference Number (OID). 
For [[obligations]] created to settle a Same-Day Settling Trade, this qualifier would be used to 
provide either the [[GSD]] Trade Reference Number (TID) assigned to the Receiver’s Same-Day 
Settling Trade or the [[GSD]] Trade Reference Number assigned to the Receiver’s [[Broker]] 
Counterparty Demand Same-Day Settling Trade that was submitted against the Receiver. If a 
TID is displayed, this identifier will be a “link back” to the trade that was submitted for 
[[settlement]] via the Same-Day Settling Service. This field will only display a TID on the 1st 
business day the Obligation was created for [[settlement]] via the Same-Day Settling Service. 
e.g., :20C::POOL//701883-9904                                                                                                            
Note:  
As regards to the Same-Day Settling Service, an Obligation can be generated to settle both the Start Leg 
and End Leg of an eligible Same-Day Settling Trade. This would mean that two [[obligations]] (with 
difference OIDs) can have the same TID populated in the Original (RELA) field, as both [[obligations]] will 
be created to settle both legs of a repo transaction same-day. 
Note: 
This field size (16x) is different from the 11-character reference number used on the traditional [[GSD]] 
Proprietary Layout.  
 

---

## Page 38

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 38 
 
MT548 [[settlement]] Status Message (Clearance Instruction & Clearance Instruction Cancel)  
Field Specifications 
Block/Tag Notes 
It should be noted that, on occasion, [[GSD]] may “replicate” or create in reverse an already cleared 
obligation. In this instance a [[Member]] will receive a new clearance instruction reflecting a new Obligation 
[[ID]] (OID) dissimilar to the OID assigned to the “original” instruction. 
It should also be noted that intra-day partials will generate new intraday clearance instructions for each 
partial [[settlement]] obligation. Each new obligation generated as a result of a partial will have a new 
Obligation [[ID]] (OID). This does not apply to [[obligations]] created to settle a Same-Day Settling Trade as 
such [[obligations]] cannot be settled through partial settlements. 
STATUS The Status Block will appear on every MT548 Message and will notify the [[Member]] of the type of 
MT548 Record being sent, as well as the Status of the Obligation. The Status Code will be 
enclosed within a Start Status Block (:16R:STAT) and End Status Block (:16S:STAT). The STAT 
Block is within the GENL Block. 
25D Status Code 
The Status Code indicates the type of [[settlement]] Status Message being sent by [[GSD]]. The following are 
the various record types, which will be used for Interactive Messaging to support the netting process. 
• IPRC/GSCC/CITS – This qualifier/[[Option]] is used to indicate that the Receiving Party must send 
instructions to their bank for [[obligations]] created by [[GSD]]. 
• IPRC//CAND – This qualifier/[[Option]] is used to notify the Receiving Party when a previously 
sent [[settlement]] Instruction has been canceled. 
e.g., :25D::IPRC/GSCC/CITS 
REASON The Reason Block will only appear on MT548 Cancellation Messages. Each Reason Code must 
be enclosed within a Start Reason (:16R:REAS) and End Reason (:16S:REAS) Block. The REAS 
Block is within the STAT Block. 
24B Reason Code 
This field is mandatory in the block and will appear on all Cancellation Messages. Each Reason Code 
must be enclosed within a Start Reason (:16R:REAS) and End Reason (:16S:REAS) Block. Currently, 
only one Reason Code has been defined. The Reason Code will be populated with the following value: 
• CAND/GSCC/GSER – This qualifier will be reflected on all CAST messages to indicate to the 
[[Member]] that the MT548 previously sent was canceled. 
e.g., :24B::CAND/GSCC/GSER 
SETTRAN The [[settlement]] Transaction Detail Block will be reflected on all MT548 messages to identify the 
details of the Obligation to be Settled. 
35B Identification of Financial Instrument/Security ([[CUSIP]]) 
The security/[[collateral]] involved is identified in the US by specifying the ISO 2-character Country Code 
(/US/), followed by the [[CUSIP]]. 
e.g., :35B:/US/912810SF6 
Note:  
This field will only populate a value of 9!c (alpha numeric) for the [[CUSIP]]. 
36B Quantity of Financial Instrument/Security to be Settled (SETT) 

---

## Page 39

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 39 
 
MT548 [[settlement]] Status Message (Clearance Instruction & Clearance Instruction Cancel)  
Field Specifications 
Block/Tag Notes 
• SETT//FAMT/ – This field is mandatory, and for the purposes of [[GSD]], will use the [[Option]] 
"FAMT" indicating Face Amount (Par). The quantity of the Financial Instrument is left justified, 
with commas removed, and a comma used instead of a decimal. 
e.g., :36B::SETT//FAMT/50000000, 
Note:  
This field can accommodate a value of 15d. 
19A [[settlement]] Amount 
• SETT// – This field is used to specify the [[settlement]] Amount for [[obligations]] created by [[GSD]]. 
The amount is left justified, with commas removed, and a comma used instead of a decimal. 
The amount is always preceded by the ISO 3-character Currency Code (“USD” for [[GSD]] 
Trades). 
e.g., :19A::SETT//USD62750000,25 
Note:  
This field can accommodate a value of 15d. 
97B Safekeeping Account 
• SAFE/GSCC/PART/ – This field specifies the [[GSD]] [[Member]] [[ID]] (4-character alphanumeric [[GSD]] 
[[Member]] Identifier. 
e.g., :97B::SAFE/GSCC/PART/8Z66 
22F [[settlement]] Indicator (SETR) 
This mandatory field indicates the [[settlement]] Status of the Obligation. 
• SETR/GSCC/NETX – This qualifier/[[Option]] indicates that the Obligation is to be settled. It will be 
used to facilitate both Next Day and Same-Day [[settlement]] Instructions. 
• SETR/GSCC/FOBL – This qualifier/[[Option]] indicates that the Obligation is based on a Fail. 
• SETR/GSCC/HFOB – This qualifier/[[Option]] indicates that the Obligation is a Held Fail (where 
[[GSD]] cannot make delivery). 
• SETR/GSCC/BKFL – This qualifier/[[Option]] indicates that the Obligation is based on a [[Broker]] 
Fail. 
• SETR/GSCC/SUBS – This qualifier/[[Option]] indicates that the Obligation is based on a Repo 
Substitution. 
 
e.g., :22F::SETR/GSCC/NETX 
22H Receive/Deliver Indicator (REDE) 
This mandatory field indicates whether the instruction is either a Receive or Deliver. 
• REDE//RECE – This qualifier/[[Option]] indicates that to satisfy this Obligation, the [[Member]] must 
Receive in [[securities]] (from [[GSD]]). 
• REDE//DELI – This qualifier/[[Option]] indicates that, to satisfy the Obligation, the [[Member]] must 
Deliver [[securities]] (to [[GSD]]). 

---

## Page 40

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 40 
 
MT548 [[settlement]] Status Message (Clearance Instruction & Clearance Instruction Cancel)  
Field Specifications 
Block/Tag Notes 
e.g., :22H::REDE//RECE 
22H Payment Indicator (PAYM) 
This mandatory Payment Indicator field indicates whether the Instruction is to be settled Free or Against 
Payment. 
• PAYM//APMT – This qualifier/[[Option]] indicates that this Obligation will be settled versus 
Payment. 
e.g., :22H::PAYM//APMT 
Note:  
All [[GSD]] Settlements are vs. Payment. 
98A [[settlement]] Date 
• SETT// – This field is used on all messages to specify the [[settlement]] Date of the Obligation. 
(The “A” Format for this tag (98) indicates a Date Format of “YYYYMMDD”.) 
e.g., :98A::SETT//20190904 
SETPRTY [[settlement]] Parties is an optional repeatable sequence. 
95R Party (Proprietary Code) 
Two Party Repeating Sequences may appear on a given MT548 Clearance Instruction Message. All 
Clearance Instructions will contain the Delivering or Receiving Agent Block (DEAG/REAG) reflecting 
[[GSD]] Clearance Instruction Information. 
This field specifies [[GSD]] Bank Clearance Instructions and will indicate whether [[GSD]] is either the 
Receiving or Delivering Party (the opposite side to that indicated in Tag :22H::REDE). The first 9 
characters of this field will be populated with [[GSD]]’s Clearing Bank ABA. Positions 10-34 will contain the 
up to 25 characters of the Bank’s Fed Address for [[GSD]] Settlements. 
• DEAG/GSCC/ – Delivering Agent or [[Seller]] - This qualifier/[[Option]] will be used where [[GSD]] is 
Delivering [[securities]] to the [[Member]]. 
• REAG/GSCC/ – Receiving Agent or [[Buyer]] - This qualifier/[[Option]] will be used where [[GSD]] is 
Receiving [[securities]] from a [[Member]]. 
e.g., :95R::DEAG/GSCC/021000018BK OF NYC/GSCC 
A second party sequence will be populated with the [[GSD]] [[participant]] [[ID]] of the Contra [[Broker]] when the 
type of [[settlement]] transaction, field 22F, is “[[Broker]] Fail” (SETR/GSCC/BKFL). 
• DEI1/GSCC/ – This qualifier/[[Option]] will be used to identify the Delivering [[Broker]]’s Contra-party 
[[ID]]. If the Instruction/Cancel is a Receive, then the Delivering [[Broker]]’s Contra-party [[ID]] will 
appear. 
• REI1/GSCC/ – This qualifier/[[Option]] will be used to identify the Receiving [[Broker]]’s Contra-party 
[[ID]]. If the Instruction/Cancel is a Deliver, then the Receiving [[Broker]]’s Contra-party [[ID]] will appear. 
e.g., :95R::REI1/GSCC/8G02 
  

---

## Page 41

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 41 
 
 
MT548 [[settlement]] Status Message (Cleared Obligation)  
Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format with 
trailing blanks, where required. 
Password 12!c Password Fields will be blank-filled on all MT548 Messages 
Sender 8!c GSCCTRRS will always be the sender of the MT548 messages in this document. 
Message 
Type 
3!n/3!n/4!c The first 3 characters indicate to the recipient the message type (548); the second 3 
positions reflect the version of the message interface (currently always 000); the last 4 
characters indicate the [[issuer]] code to be used in the message (GSCC). 
Receiver 8!c [[participant]] [[ID]] 
GENL  This mandatory block provides General Information regarding the message. It appears only once 
in an MT548 [[settlement]] Status Message. 
20C Sender's Message Reference 
• SEME// – This mandatory field contains the Sender’s ([[GSD]]) Message Reference Number. It is 
used on all messages sent by [[GSD]] and will contain a unique number to unambiguously identify 
each message. (This is a Communications Message Number, not a Trade Number.) 
e.g., :20C::SEME//000000754669 
23G Function of the Message 
This mandatory field identifies the Function of the Message. For the purposes of Cleared Obligation 
Messages, this field will always refer to an Instruct (INST). 
• INST – This qualifier will be used to indicate to Participants that an Obligation has Cleared or 
partially cleared. 
e.g., :23G:INST   
98C Preparation Date and Time 
• PREP// – This field will be reflected on all messages to indicate the Date and Time the message 
was prepared by [[GSD]]. 
e.g., :98C::PREP//20190904162935 
Note:  
The “C” Format for this (98) tag indicates a Date/Time Format of “YYYYMMDDHHMMSS”. 
LINK The LINK Block will be repeated for the many reference qualifiers required on a [[settlement]] Status 
Message. It is intended to provide the required information to identify the Obligation being 
Cleared. Each Reference Number will be enclosed within a Start Link Block (:16R:LINK) and End 
Link Block (:16S:LINK). All LINK repeating subsequences are within the GENL Block. At least one 
LINK sequence is required on the MT548 Message. 

---

## Page 42

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 42 
 
MT548 [[settlement]] Status Message (Cleared Obligation)  
Field Specifications 
Block/Tag Notes 
20C Reference 
This field will be populated with the 11-character OID (Obligation Reference Number) assigned by [[GSD]] 
to each Obligation or the TID (Trade Reference Number) assigned by [[GSD]] to the trade for which Same-
Day Settling Obligation(s) were created for the purposes of [[settlement]] through the Same-Day Settling 
Service. As indicated above, each Reference Number will be enclosed in a LINK Start and End Block. 
Two of the reference qualifiers Current (POOL) and Previous (PREV) are assigned at the time an initial 
obligation is created. The third reference qualifier Original OID (RELA) is either the identifier assigned to 
the trade for which the created Obligation is to be settled for or the original identifier assigned to the 
obligation. All three fields will be populated on all [[settlement]] Status messages. 
Where an Obligation settles in full via one clearance on the Obligation’s original Scheduled [[settlement]] 
Date, the Cleared Obligation record will reflect the identical reference numbers as the original Clearance 
Instruction record. 
Where an Obligation is partially settled in installments on its original Scheduled [[settlement]] Date, the 
RELA field will retain the OID from the original Clearance Instruction record, but the Current and 
Previous OIDs may change, as partial [[obligations]] are created and cleared that day. It should be noted 
that this does not apply to [[obligations]] created to settle a Same-Day Settling Trade.  
• POOL – This qualifier is used for the [[GSD]] Obligation Reference Number of the Obligation to be 
Cleared (OID). It appears on all Clearance Instructions and reflects the reference of the current 
OID. It should be noted that a new OID is generated for each partial clearance that takes place. 
• PREV – This qualifier is used to reflect the previous [[GSD]] Obligation Reference Number (OID). 
It should be noted that a new OID is generated for each partial clearance that takes place. In 
the future, if an obligation has been cleared through the Pair-off Service, an additional PREV 
field may be included on the record. This additional PREV field will reflect the related Obligation 
[[ID]](s) that were in the paired off set. 
• RELA – This qualifier is used to provide the Original [[GSD]] Obligation Reference Number (OID). 
For [[obligations]] created to settle a Same-Day Settling Trade, this qualifier would be used to 
provide either the [[GSD]] Trade Reference Number (TID) assigned to the Receiver’s Same-Day 
Settling Trade or the [[GSD]] Trade Reference Number assigned to the Receiver’s [[Broker]] 
Counterparty Demand Same-Day Settling Trade that was submitted against the Receiver. If a 
TID is displayed, this identifier will be a “link back” to the trade that was submitted for [[settlement]] 
via the Same-Day Settling Service. This field will only display a TID on the 1st business day the 
Obligation was created for [[settlement]] via the Same-Day Settling Service. 
e.g., :20C::POOL//701887-9904 
Note:  
As regards to the Same-Day Settling Service, an Obligation can be generated to settle both the Start Leg 
and End Leg of an eligible Same-Day Settling Trade. This would mean that two [[obligations]] (with 
difference OIDs) can have the same TID populated in the Original (RELA) field, as both [[obligations]] will be 
created to settle both legs of a repo transaction same-day. 
Note: 
This field size (16x) is different from the 11-character reference number used on the traditional [[GSD]] 
Proprietary Layout. 

---

## Page 43

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 43 
 
MT548 [[settlement]] Status Message (Cleared Obligation)  
Field Specifications 
Block/Tag Notes 
It should be noted that, on occasion, [[GSD]] may “reinstate” an already cleared obligation. In this instance a 
[[Member]] will receive a new clearance instruction reflecting new [[obligations]] IDs (OIDs) dissimilar to those 
assigned to the “original” instruction. 
It should also be noted that intra-day partials will generate new intraday clearance instructions for each 
partial [[settlement]] obligation. Each new obligation generated as a result of a partial will have a new 
Obligation [[ID]] (OID). This does not apply to [[obligations]] created to settle a Same-Day Settling Trade as 
such [[obligations]] cannot be settled through partial settlements. 
STATUS The Status Block will appear on every MT548 Message and will notify the [[Member]] of the type of 
MT548 Record being sent, as well as the Status of the Obligation. The Status Code will be 
enclosed within a Start Status Block (:16R:STAT) and End Status Block (:16S:STAT). The STAT 
Block is within the GENL Block. 
25D Status Code 
The Status Code indicates the type of [[settlement]] Status Message being sent by [[GSD]]. The following 
qualifier will be used for Interactive Messaging to support the Same-Day Settling Service and Pair-off 
Service, as applicable. 
• SETT/GSCC/CLOB – This qualifier/[[Option]] indicates this is a Cleared Obligation Record. 
e.g., :25D::SETT/GSCC/CLOB 
SETTRAN The [[settlement]] Transaction Detail Block will be reflected on all MT548 messages to identify the 
details of the Settled Obligation. 
35B Identification of Financial Instrument/Security ([[CUSIP]]) 
The security/[[collateral]] involved is identified in the US by specifying the ISO 2-character Country Code 
(/US/), followed by the [[CUSIP]]. 
e.g., :35B:/US/912810SF6 
Note:  
This field will only populate a value of 9!c (alpha numeric) for the [[CUSIP]]. 
36B Quantity of Financial Instrument/Security to be Settled (SETT) 
• SETT//FAMT/ – This field is mandatory, and for the purposes of [[GSD]], will use the [[Option]] 
"FAMT" indicating Face Amount (Par). It provides the Quantity of the security that was actually 
Settled. The quantity of the Financial Instrument is left justified, with commas removed, and a 
comma used instead of a decimal. 
e.g., :36B::SETT//FAMT/50000000, 
Note:  
This field can accommodate a value of 15d. 

---

## Page 44

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 44 
 
MT548 [[settlement]] Status Message (Cleared Obligation)  
Field Specifications 
Block/Tag Notes 
19A [[settlement]] Amount 
• SETT// – This field is used to specify the [[settlement]] Amount Cleared for the Obligation, which 
was Settled. The amount is left justified, with commas removed, and a comma used instead of a 
decimal. The amount is always preceded by the ISO 3-character Currency Code (“USD” for 
[[GSD]] Trades). 
e.g., :19A::SETT//USD62750000,25 
Note:  
This field can accommodate a value of 15d. 
97B Safekeeping Account 
• SAFE/GSCC/PART/ – This field specifies the [[GSD]] [[Member]] [[ID]] (4-character alphanumeric [[GSD]] 
[[Member]] Identifier. 
e.g., :97B::SAFE/GSCC/PART/8ZX1 
22F [[settlement]] Indicator (SETR) 
This field is mandatory for the block and indicates the [[settlement]] Status of the Obligation. 
• SETR//PAIR – This qualifier/[[Option]] indicates that the Obligation Settled via Pair-Off. 
• SETR/GSCC/BTIN – This qualifier/[[Option]] indicates [[GSD]] has Bought In the [[securities]] for the 
Obligation to be cleared. 
• SETR/GSCC/HDFM – This qualifier/[[Option]] indicates that the [[securities]] for a Held Fail Obligation 
has Matured. 
• SETR/GSCC/MATR – This qualifier/[[Option]] indicates that the [[securities]] for a Failed Obligation 
have Matured. 
• SETR/GSCC/CLRD – This qualifier/[[Option]] indicates that the Obligation has Cleared. 
e.g., :22F::SETR/GSCC/CLRD 
22H Receive/Deliver Indicator (REDE) 
This mandatory field indicates whether the instruction is either a Receive or Deliver. 
• REDE//RECE – This qualifier/[[Option]] indicates that the Cleared Obligation was a [[Member]] 
Receive from [[GSD]]. 
• REDE//DELI – This qualifier/[[Option]] indicates that the Cleared Obligation was a [[Member]] Deliver 
to [[GSD]]. 
e.g., :22H::REDE//DELI 
22H Payment Indicator (PAYM) 
This mandatory Payment Indicator field indicates whether the Obligation settled Free or Against 
Payment. All [[obligations]] Cleared by [[GSD]] will provide the following qualifier: 
• PAYM//APMT – This qualifier/[[Option]] indicates that this Obligation settled versus Payment. 
e.g., :22H::PAYM//APMT 
Note:  
All [[GSD]] Settlements are vs. Payment. 

---

## Page 45

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 45 
 
MT548 [[settlement]] Status Message (Cleared Obligation)  
Field Specifications 
Block/Tag Notes 
98A [[settlement]] Date 
• SETT// – This field is used on all messages to specify the [[settlement]] Date of the Obligation. 
(The “A” Format for this tag (98) indicates a Date Format of “YYYYMMDD”.) 
e.g., :98A::SETT//20190904 
70E [[settlement]] Instruction Processing Narrative (SPRO) 
• SPRO//GSCC - This narrative field is included on all Cleared Obligation Messages. 
o /RSTTFAMT – This field indicates the Quantity of Financial Instrument Remaining to be 
settled. This field is populated if the Quantity Cleared on this record is less than the 
Quantity indicated in the Opening Par Field (OPARFAMT found in this narrative field). 
o /RSMTUSD – This field indicates the [[settlement]] Amount Remaining to be settled. This 
field is populated if the [[settlement]] Amount Cleared on the record is less than the Amount 
indicated in the opening [[settlement]] Amount field (OPSTUSD found in this narrative field). 
o /DCDFUSD – This field indicates that there is a Debit Clearance Difference on the cleared 
obligation. This field is populated when there is a Debit Clearance Difference Remaining 
after [[settlement]] (ISO Currency Code preceding amount required, always USD for [[GSD]] 
domestic business). 
o /CCDFUSD – This field indicates that there is a Credit Clearance Difference on the cleared 
obligation. This field is populated when there is a Debit Clearance Difference Remaining 
after [[settlement]] (ISO Currency Code preceding amount required, always USD for [[GSD]] 
domestic business). 
o /DFMKUSD – This field indicates that there is a Debit mark to market on the fail item 
before it was cleared due to netting. This field is populated when there is a Debit Mark to 
Market before the item was cleared (ISO Currency Code preceding amount required, 
always USD for [[GSD]] domestic business). 
o /CFMKUSD – This field indicates that there is a Credit mark to market on the fail item 
before it was cleared due to netting. This field is populated when there is a Credit Mark to 
Market before the item was cleared (ISO Currency Code preceding amount required, 
always USD for [[GSD]] domestic business). 
o /OPARFAMT – This field indicates that day’s Opening Par of the Obligation to be settled. 
In the case of a partial [[settlement]], this field will be decremented by the quantity already 
settled intraday. This field will be reflected on all Cleared Obligation Messages. 
o /OPSTUSD – This field indicates that day’s Opening [[settlement]] Amount of the Obligation 
to be settled. In the case of a partial [[settlement]], this field will be decremented by the 
money amount already settled intraday. This field will be reflected on all Cleared Obligation 
messages. 
e.g., :70E::SPRO//GSCC/OPARFAMT50000000/OPSTUSD62750000,25                                           
Note:  
This field can accommodate a value of 15d. 
  

---

## Page 46

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 46 
 
MT548 Message Mapping 
This section contains a message mapping for the fields that may be found on each MT548 [[settlement]] Status Message. The mapping is separated into 
two categories; 1) Clearance Instruction / Clearance Instruction Cancel (mapped to MRO Record Type 18) and 2) Cleared Obligation (mapped to MRO 
Record Type 23).  
MT548 [[settlement]] Status (Clearance Instruction & Clearance Instruction Cancel)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 18 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
        Message Header          
M        Password 12!c       [[GSD]] will blank fill the 
Password fields on all 
outgoing messages. 
M        Sender 8!c       GSCCTRRS 
M        Message Type 3!n/3!n/4!c       All 3 fixed-length sub 
fields will be populated. 
M        Receiver 8!c [[Member]] [[ID]] 4 30 33 A/N 4-character [[GSD]] 
[[Member]] [[ID]]. 
M :16R: GENL   Mandatory Start of 
Block 
         
M :20C: :SEME//   Sender's Message 
Reference 
16x       Sender's ([[GSD]]) 
Message Reference 
Number. 
M :23G: INST   Message Function – 
Instruct 
or 
4!c       This qualifier indicates 
to Members that this 
record reflects those 
Clearing Instructions to 

---

## Page 47

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 47 
 
MT548 [[settlement]] Status (Clearance Instruction & Clearance Instruction Cancel)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 18 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
be sent by them to their 
bank. 
    CAST   Cancel         This qualifier is used by 
[[GSD]] to inform 
Members of Canceled 
Clearance Instruction 
Records. 
O :98C: :PREP//   Preparation 
Date/Time 
YYYYMMDD 
HHMMSS 
      Date/Time [[GSD]] 
prepared message. 
M :16R: LINK   Mandatory Repeat 
Start of Block 
         
M :20C: :POOL//   Pool Reference 
Number ([[GSD]] 
Reference Number of 
Obligation to be 
Cleared) (OID) 
16x Transaction [[ID]] 11 19 29 A/N [[GSD]] Reference 
Number of Obligation to 
be Cleared (OID). 
M :16S: LINK   End of Block          
M :16R: LINK   Mandatory Repeat 
Start of Block 
         
O :20C: :PREV//   Previous Reference 
Number (Previous 
[[GSD]] Reference 
Number of the 
Obligation to be 
Cleared) (OID) 
16x Transaction [[ID]] 11 172 182 A/N Previous [[GSD]] 
Reference Number of 
Obligation to be 
Cleared (OID). This 
field will appear on all 
clearance instructions. 
M :16S: LINK   End of Block          

---

## Page 48

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 48 
 
MT548 [[settlement]] Status (Clearance Instruction & Clearance Instruction Cancel)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 18 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
M :16R: LINK   Mandatory Repeat 
Start of Block 
         
O :20C: :RELA//   Related Reference 
Number (Original 
[[GSD]] Obligation 
Reference Number) 
(OID) or [[GSD]] 
Reference Number 
(Receiver's TID or 
[[Broker]] 
Counterparty's TID) 
16x Original 
Transaction [[ID]]  
11 183 193 A/N [[GSD]] Reference 
Number (Identifier of 
the Original Obligation 
to be Cleared or the 
Identifier assigned to 
the Same-Day Settling 
Trade). This appears on 
all clearance 
instructions. 
M :16S: LINK   End of Block          
M :16R: STAT   Mandatory Repeat 
Start of Block 
         
M :25D: :IPRC/ GSCC/CITS Status – Instruction 
to be Sent to 
Clearing Facility 
or 
4!c       [[GSD]] to generate when 
Instructions must be 
sent by the [[Member]] to 
their bank. 
      /CAND Cancellation of a 
Previously Sent 
Clearance Instruction 
        [[GSD]] to generate when 
previously sent 
Clearance Instructions 
must be Cancelled. 
M :16R: REAS   Optional Repeat 
Start of Block  
        This block will only be 
used for MT548 
Cancels. 
M :24B: :CAND/ GSCC/GSER Reason Code 4!c       Cancellation due to 
[[GSD]] Action. 

---

## Page 49

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 49 
 
MT548 [[settlement]] Status (Clearance Instruction & Clearance Instruction Cancel)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 18 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
M :16S: REAS   End of Block          
M :16S: STAT   End of Block          
M :16S: GENL   End of Block          
M :16R: SETTRAN   Optional Start of 
Block  
         
M :35B: /US/   Identification of 
Financial 
Instrument/Security 
([[CUSIP]]) 
4*35x [[CUSIP]] 
 
9 41 49 A/N [[CUSIP]] is always 
preceded by the ISO 2-
character Country Code 
"/US/". 
M :36B: :SETT// FAMT/ Quantity of Financial 
Instrument/ Security 
to be Settled 
15d Quantity  18 56 73 A/N Decimal comma 
mandatory-different 
field sizes. 
O :19A: :SETT// USD [[settlement]] Amount 15d Amount 18 74 91 A/N Amount is always 
preceded by ISO 3-
character Currency 
Code "USD" (USD used 
for all [[GSD]] domestic 
activity). Decimal 
comma mandatory-
different field sizes. 
M :97B: :SAFE/ GSCC/PART/ Safekeeping Account 
– [[GSD]] [[Member]] [[ID]] 
35x [[Member]] [[ID]] 4 30 33 A/N 4-character [[GSD]] 
[[Member]] [[ID]]. 
M :22F: :SETR/ GSCC/NETX Type of [[settlement]] 
Transaction – Same 
Day or Next Day           
4!c Clearance Type 1 161 161 A/N Value in [[GSD]] Field = N. 

---

## Page 50

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 50 
 
MT548 [[settlement]] Status (Clearance Instruction & Clearance Instruction Cancel)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 18 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
   GSCC/FOBL Type of [[settlement]] 
Transaction – Fail 
Obligation 
or        
       Value in [[GSD]] Field = F. 
   GSCC/HFOB Type of [[settlement]] 
Transaction – Held 
Fail Obligation 
or        
      Value in [[GSD]] Field = H.  
 
   GSCC/BKFL Type of [[settlement]] 
Transaction – [[Broker]] 
Fail 
or        
      Value in [[GSD]] Field = F. 
   GSCC/SUBS Type of [[settlement]] 
Transaction – Repo 
Substitution 
      Value in [[GSD]] Field = N.  
M :22H: :REDE// RECE Receive/Deliver 
Indicator – Receive 
or 
4!c Transaction 
Code  
1 40 40 A/N Transaction Code = L.   
      DELI Deliver         Transaction Code = S. 
M :22H: :PAYM// APMT Payment Indicator – 
vs. Payment 
4!c       All Clearance 
Instructions will be vs. 
Payment. 
M :98A: :SETT//   [[settlement]] Date  YYYYMMDD  [[settlement]] Date 10 162 171 A/N Intended [[settlement]] 
Date of Obligation. 

---

## Page 51

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 51 
 
MT548 [[settlement]] Status (Clearance Instruction & Clearance Instruction Cancel)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 18 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
M :16R: SETPRTY   Optional Repeat 
Start of Block  
         
M :95R: :DEAG/ GSCC/ Party – Delivering 
Agent (or [[Seller]]) and 
Clearing Instruction 
Information for [[GSD]] 
or 
34x see 
Note in 
Comments 
column 
(9!c25x) 
Clearing Bank 
ABA 
9 92 100 A/N Where 22H = RECE 
populate "DEAG". 
Note: The first nine 
characters of this field 
will be used for the 
[[GSD]] Clearing Bank’s 
ABA. The last 25 
characters will be used 
for the Fed Address. 
      Fed Address 40 101 140 A/N Note: Should the Fed 
Address be greater 
than 25 characters, the 
remaining 15 
characters (of the 40-
byte field) will be placed 
in the last 15 bytes of 
the Safekeeping 
Account (97A) Field 
following the 20-
character [[GSD]] Contra 
[[ID]] at the bank (see 
below). 
    :REAG/ GSCC/ Receiving Agent (or 
[[Buyer]]) and Clearing 
Instruction 
Information for [[GSD]] 
 34x see 
Note in 
Comments 
column 
(9!c25x) 
Clearing Bank 
ABA 
9 92 100 A/N Where 22H = DELI 
populate "REAG". 
Note: The first nine 
characters of this field 
will be used for the 
[[GSD]] Clearing bank’s 

---

## Page 52

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 52 
 
MT548 [[settlement]] Status (Clearance Instruction & Clearance Instruction Cancel)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 18 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
ABA. The last 25 
characters will be used 
for the Fed Address. 
      Fed Address 40 101 140 A/N Note: Should the Fed 
address be greater than 
25 characters, the 
remaining 15 
characters (of the 40-
byte field) will be placed 
in the last 15 bytes of 
the Safekeeping 
Account (97A) Field 
following the 20-
character [[GSD]] Contra 
[[ID]] at the bank (see 
below). 
M :16S: SETPRTY   End of Block          
M :16R: SETPRTY   Optional Repeat 
Start of Block  
         
M :95R: :DEI1/ GSCC/ Party – Delivering 
[[Broker]] Contra-party 
[[ID]] 
or 
34x                                               Where 22H = RECE 
and 22F = BKFL, we 
will populate DEI1. (No 
existing [[GSD]] field.) 
M   :REI1/ GSCC/ Party – Receiving 
[[Broker]] Contra-party 
[[ID]] 
       Where 22H = DELI and 
22F = BKFL, we will 
populate REI1. (No 
existing [[GSD]] field.) 
M :16S: SETPRTY   End of Block          

---

## Page 53

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 53 
 
MT548 [[settlement]] Status (Clearance Instruction & Clearance Instruction Cancel)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 18 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
M :16S: SETTRAN   End of Block          
  

---

## Page 54

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 54 
 
MT548 [[settlement]] Status (Cleared Obligation)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 23 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
        Message Header          
M        Password 12!c       [[GSD]] will blank fill the 
Password fields on all 
outgoing messages. 
M        Sender 8!c       GSCCTRRS 
M        Message Type 3!n/3!n/4!c       All 3 fixed-length sub 
fields will be populated. 
M        Receiver 8!c [[Member]] [[ID]] 4 30 33 A/N 4-character [[GSD]] 
[[Member]] [[ID]] 
M :16R: GENL   Mandatory Start of 
Block 
         
M :20C: :SEME//   Sender's Message 
Reference 
16x       Sender's ([[GSD]]) 
Message Reference 
Number. 
M :23G: INST   Message Function – 
Instruct 
4!c       All Cleared Obligation 
Messages should refer 
to “INST”. 
O :98C: :PREP//   Preparation 
Date/Time 
YYYYMMDD 
HHMMSS 
      Date/Time [[GSD]] 
prepared message. 
M :16R: LINK   Mandatory Repeat 
Start of Block 
         
M :20C: :POOL//   Pool Reference 
Number ([[GSD]] 
Reference Number of 
16x Transaction [[ID]] 11 19 29 A/N [[GSD]] Reference 
Number of Obligation to 
be Cleared (OID). 

---

## Page 55

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 55 
 
MT548 [[settlement]] Status (Cleared Obligation)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 23 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
Obligation to be 
Cleared) (OID) 
M :16S: LINK   End of Block          
M :16R: LINK   Mandatory Repeat 
Start of Block 
         
O :20C: :PREV//   Previous Reference 
Number (Previous 
[[GSD]] Reference 
Number of the 
Obligation to be 
Cleared) (OID) 
16x Transaction [[ID]] 11 19 29 A/N Previous [[GSD]] 
Reference Number of 
Obligation to be 
Cleared (OID).  
M :16S: LINK   End of Block          
M :16R: LINK   Mandatory Repeat 
Start of Block 
         
O :20C: :RELA//   Related Reference 
Number (Original 
[[GSD]] Obligation 
Reference Number) 
(OID) or [[GSD]] 
Reference Number 
(Receiver's TID or 
[[Broker]] 
Counterparty's TID) 
16x Original 
Transaction [[ID]]  
11 130 140 A/N [[GSD]] Reference 
Number (Identifier of 
the Original Obligation 
to be Cleared or the 
Identifier assigned to 
the Same-Day Settling 
Trade). This appears on 
all clearance 
instructions. 
M :16S: LINK   End of Block          
M :16R: STAT   Mandatory Repeat 
Start of Block 
         

---

## Page 56

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 56 
 
MT548 [[settlement]] Status (Cleared Obligation)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 23 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
M :25D: :IPRC/ GSCC/CLOB Status – Cleared 
Obligation  
4!c       [[GSD]] to generate when 
an Obligation has been 
marked Cleared. 
M :16S: STAT   End of Block          
M :16S: GENL   End of Block          
M :16R: SETTRAN   Optional Start of 
Block  
         
M :35B: /US/   Identification of 
Financial 
Instrument/Security 
([[CUSIP]]) 
4*35x [[CUSIP]] 
 
9 41 49 A/N [[CUSIP]] is always 
preceded by the ISO 2-
character Country Code 
"/US/". 
M :36B: :SETT// FAMT/ Quantity of Financial 
Instrument/ Security 
to be Settled 
15d Quantity  
Cleared 
18 56 73 A/N Decimal comma 
mandatory-different 
field sizes. 
O :19A: :SETT// USD [[settlement]] Amount 15d Amount Cleared 18 74 91 A/N Amount is always 
preceded by ISO 3-
character Currency 
Code "USD" (USD used 
for all [[GSD]] domestic 
activity). Decimal 
comma mandatory-
different field sizes. 
M :97B: :SAFE/ GSCC/PART/ Safekeeping Account 
– [[GSD]] [[Member]] [[ID]] 
35x [[Member]] [[ID]] 4 30 33 A/N 4-character [[GSD]] 
[[Member]] [[ID]]. 
M :22F: :SETR/ /PAIR Type of [[settlement]] 
Transaction – Paired-
Off 
4!c Clearance 
Method 
1 110 110 A/N Clearance Method = P 

---

## Page 57

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 57 
 
MT548 [[settlement]] Status (Cleared Obligation)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 23 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
or 
   GSCC/BTIN Type of [[settlement]] 
Transaction – Bought 
In 
or 
       Clearance Method = B 
   GSCC/HDFM Type of [[settlement]] 
Transaction – Held 
Fail Matured 
or 
      Clearance Method = H 
   GSCC/MATR Type of [[settlement]] 
Transaction – 
Matured 
or 
      Clearance Method = M 
   GSCC/CLRD Type of [[settlement]] 
Transaction – 
Cleared 
or 
      Clearance Method = C 
   GSCC/FLRN Type of [[settlement]] 
Transaction – Fail  
Netted 
      Clearance Method = N 
M :22H: :REDE// RECE Receive/Deliver 
Indicator – Receive 
or 
4!c Transaction 
Code  
1 40 40 A/N Transaction Code = L 
      DELI Deliver         Transaction Code = S. 
M :22H: :PAYM// APMT Payment Indicator – 
vs. Payment 
4!c       All Cleared [[obligations]] 
will be vs. Payment. 

---

## Page 58

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 58 
 
MT548 [[settlement]] Status (Cleared Obligation)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 23 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
M :98A: :SETT//   [[settlement]] Date  YYYYMMDD       Intended [[settlement]] 
Date of Obligation. 
O :70E: :SPRO// GSCC [[settlement]] 
Instruction 
Processing Narrative  
(10*35x)       Include below fields on 
all Cleared Obligation 
Messages. 
   /RSTTFAMT Quantity of Financial 
Instrument 
Remaining to be 
Settled 
15d Quantity 
Remaining 
Clearance 
 18 92 109 A/N Populate if the 
obligation is partially 
Cleared. 
   /RSMTUSD [[settlement]] Amount 
Remaining  
15d           Populate if the 
obligation is partially 
Cleared. (No current 
[[GSD]] field.) 
Amount is always 
preceded by the ISO 3- 
character Currency 
Code “USD” (USD used 
for all [[GSD]] domestic 
activity). Decimal 
comma mandatory.) 
      /DCDFUSD Debit Clearance 
Difference 
or 
15d Credit / Debit 
Indicator 
1 129  129 A/N  Clearance Difference 
on Maturity = Debit, use 
qualifier "DCDF". 
Amount is always 
preceded by the ISO 3-
character Currency 
Code “USD” (USD used 
for all [[GSD]] domestic 

---

## Page 59

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 59 
 
MT548 [[settlement]] Status (Cleared Obligation)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 23 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
activity). Decimal 
comma mandatory. 
      Clearance 
Difference on 
Maturity 
18 111 128 A/N Decimal comma 
mandatory 
      /CCDFUSD Credit Clearance 
Difference 
  Credit / Debit 
Indicator 
1 129  129 A/N  Clearance Difference 
on Maturity = Credit, 
use qualifier "CCDF". 
Amount is always 
preceded by the ISO 3-
character Currency 
Code “USD” (USD used 
for all [[GSD]] domestic 
activity). Decimal 
comma mandatory. 
      Clearance 
Difference on 
Maturity 
18 111 128 A/N Decimal comma 
mandatory 
   /DFMKUSD Debit Fail Mark Due 
to Netting 
or 
15d Credit / Debit 
Indicator 
1 177 177 A/N Fail Mark = Debit, use 
qualifier "DFMK". 
Amount is always 
preceded by the ISO 3- 
character Currency 
Code "USD" (USD used 
for all [[GSD]] domestic 
activity). Decimal 
comma mandatory. 

---

## Page 60

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 60 
 
MT548 [[settlement]] Status (Cleared Obligation)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 23 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
      Fail Mark 18 159 176 A/N Decimal comma 
mandatory 
   /CFMKUSD Credit Fail Mark Due 
to Netting 
 Credit / Debit 
Indicator 
1 177 177 A/N Fail Mark = Credit, use 
qualifier "CFMK". 
Amount is always 
preceded by the ISO 3- 
character Currency 
Code "USD" (USD used 
for all [[GSD]] domestic 
activity). Decimal 
comma mandatory. 
      Fail Mark 18 159 176 A/N Decimal comma 
mandatory 
      /OPARFAMT Opening Par  15d  Opening Par 18 141 158 A/N Decimal comma 
mandatory. This field 
will appear on all 
cleared [[obligations]]. 
      /OPSTUSD Opening [[settlement]] 
Amount 
15d       Populate if security 
partially Cleared. 
Decimal comma 
mandatory. This field 
will appear on all 
cleared [[obligations]]. (No 
current [[GSD]] field.) 
Amount is always 
preceded by the ISO 3- 
character Currency 
Code "USD" (USD used 
for all [[GSD]] domestic 

---

## Page 61

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT548 61 
 
MT548 [[settlement]] Status (Cleared Obligation)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 23 Fields 
M/O Tag Block/ 
Qualifier 
Subqualifier/ 
Options 
Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comments 
activity). Decimal 
comma mandatory. 
M :16S: SETTRAN   End of Block           
 

---

## Page 62

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 62 
 
NETTING INTERACTIVE MESSAGE SPECIFICATIONS – 
MT590 
This section contains the detailed specifications including layout and field descriptions for the MT590 
Messages. The message type will be used for Advice of Charges, Interest and Other Adjustments as described 
in the MT590 Overview in this document. 
MT590 Message Description 
The MT590 Message is specified as an Advice of Charges, Interest and Other Adjustments. The MT590 
message type supports Coupon/Maturity Payments for Outstanding Failed [[obligations]] and Repo Transactions, 
as well as the debits or credits associated with per trade forward [[Margin]]. This message type is sent to the 
[[Member]] to advise it of monies, which have been Debited or Credited to the [[participant]]’s Account, based on 
outstanding Fails, Repo Transactions or on [[Margin]] applied. All MT590 Messages in this specification contain 
information on a per trade or per obligation basis. 
The MT590 is an older SWIFT Message Type, which contains tags with concatenated data fields. In addition, 
the tags on this message have specific definitions, and contain no qualifiers or sub-qualifiers. Because of this, 
we have removed from the layout, the columns supporting qualifier/sub-qualifier information, and added 
columns reflecting the “sub field” components of concatenated tags/fields. 
[[GSD]] will use the MT590 Message for two general categories of records; 1) Coupon/Maturity Debit/Credit for 
Outstanding Repo or Fail and 2) Per Trade Forward [[Margin]]. Within those two categories are a total of five 
system events. Field 71B indicates to the recipient the type of record being sent. The following SWIFT MT590 
Messages may be generated to provide such information to Members: 
Message Type This message is used to: 
Repo Coupon Payment 
(:71B:/GSCC/DRCR/CPRP/US/…) 
inform a [[Member]] of the Coupon Payment outstanding on their Repo 
transaction. 
Fail Coupon Payment 
(:71B:/GSCC/DRCR/CPFL/US/…) 
inform Members of the Coupon Payment outstanding on their Fail. 
Repo Maturity Payment 
(:71B:/GSCC/DRCR/MARP/US/…) 
inform Members of the Maturity Principal Payment on an outstanding Repo 
transaction. 
Fail Maturity Payment 
(:71B:/GSCC/DRCR/MAFL/US/…) 
inform Members of the Maturity Principal Payment on an outstanding Fail. 
Per Trade Forward [[Margin]] 
(:71B:/GSCC/DRCR/FMFF/US/) 
inform Members of the Forward [[Margin]] and Forward Finance on a per trade 
basis. These two amounts have been aggregated on the Per Trade Forward 
[[Margin]] MT590 to reflect one Debit or Credit amount. 
  

---

## Page 63

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 63 
 
MT590 Message Specifications 
MT590 General Format 
This section provides the general format for the MT590 Message. As described in the MT590 Message 
Description, the MT590 will be sent by [[GSD]] to Members for the following events: 
• Repo Coupon Payment 
• Fail Coupon Payment 
• Repo Maturity Payment 
• Fail Maturity Payment  
• Per Trade Forward [[Margin]] 
 
MT590 Advice of Charges, Interest and Other Adjustments Message 
General Format 
M/O Tag Field Description Data Field 
Format 
Sub Field 
Description 
Sub Field Format 
  Message Header    
M   Password 12!c   
M   Sender 8!c   
M   Message Type 3!n/3!n/4!c   
M   Receiver 8!c   
M :20: Transaction Reference Number 
([[GSD]] Reference Number – TID or 
OID) 
16x   
M :21: Related Reference ([[Member]] 
External Reference Number) 
16x   
M :25: Account Identification ([[Member]] [[ID]]) 35x   
M :32C: Value Date, Currency Code, 
Amount Credited 
or 
6!n3!a15d This tag/field includes the following sub 
fields: 
Value Date YYMMDD 
Currency Code 3!a 
Amount 15d 
 :32D: Value Date, Currency Code, 
Amount  Debited 
6!n3!a15d This tag/field includes the following sub 
fields: 
Value Date YYMMDD 
Currency Code 3!a 
Amount 15d 

---

## Page 64

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 64 
 
MT590 Advice of Charges, Interest and Other Adjustments Message 
General Format 
M/O Tag Field Description Data Field 
Format 
Sub Field 
Description 
Sub Field Format 
M :71B: Details of Charges (6*35x)   
  /GSCC/DRCR/CPRP/US/  
or 
20x   
  /GSCC/DRCR/CPFL/US/  
or 
   
  /GSCC/DRCR/MARP/US/  
or 
   
  /GSCC/DRCR/MAFL/US/ 
or 
   
  /GSCC/DRCR/FMFF/US/  
and 
   
  /SECO 16x   
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 65

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 65 
 
MT590 Field Specifications 
This section provides the detailed field specifications for the MT590 Advice of Charges, Interest and Other 
Adjustments Message.   
MT599 Advice of Charges, Interest and Other Adjustments Message  
Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format 
with trailing blanks, where required. 
Password   12!c This field will be blank-filled on all MT590 Messages. 
Sender   8!c “GSCCTRRS” ([[GSD]] Trade Registration and Reconciliation System) will always be 
the sender of the MT590 messages in this document. 
Message Type 3!n/3!n/4!c  The first 3 characters indicate to the recipient the message type (590); the second 3 
positions reflect the version of the message interface (currently always 000). The 
last 4 characters indicate the [[issuer]] code to be used in the message (GSCC). 
Receiver 8!c [[Member]] [[ID]] 
20 Transaction Reference Number 
To uniquely identify this message, this mandatory field will be populated with the [[GSD]] Assigned 
Reference Number (TID or OID) of the trade or obligation that generated this entry. Where the 
advice refers to a trade, as in the case of a financing trade, a Trade [[ID]] (TID) will be reflected. 
Where the advice refers to an obligation, as in the case of a fail, an Obligation [[ID]] (OID) will be 
reflected.  
e.g., :20:000042-6149                                                                                   
 
21 Related Reference 
This mandatory field will be populated with the [[Member]]’s X-Ref Number (External Reference 
Number) of the trade that has generated this entry. 
e.g., :21:1234ABC1 
Note:  
Where an MT590 reflects a debit or credit associated with a fail, [[GSD]] will generate a [[Member]] X-Ref. 
25 Account Identification 
This tag contains the 4-character [[GSD]] [[Member]] [[ID]]. 
e.g., :25:8X61 
32C/32D Date and Amount 
This field specifies the Value Date, Currency Code and Amount (Credited or Debited) for the entry.  
• Where the entry is a Credit, the “C” Format will be used for Tag 32 (32C).  
• Where it is a Debit, the “D” format will be used for Tag 32 (32D).  
• The Value Date sub field provides the Date of the Payment to be made (to or from the 
[[Member]]).  
• The Currency Code is the ISO 3-character Currency Code, which always precedes an 
amount field. For [[GSD]] domestic business, this will always contain the value “USD”.  

---

## Page 66

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 66 
 
MT599 Advice of Charges, Interest and Other Adjustments Message  
Field Specifications 
Block/Tag Notes 
• The amount sub field is a 15-character decimal field that includes the Amount of the 
Payment. 
e.g., :32C:200630USD10000, 
Note:  
The field can accommodate a value of 15d. 
71B Details of Charges 
This field specifies the type of record being sent which indicates the nature of the monetary entry 
being made to the [[Member]]’s account. 
• /GSCC/DRCR/CPRP/US/ – This set of qualifiers is used to indicate that the Debit/Credit 
entry is for a Coupon Payment on an outstanding or maturing Repo Transaction. The 
qualifiers will be followed by the Security Identifier ([[CUSIP]]). The [[CUSIP]] will be preceded by 
“/US/”. 
• /GSCC/DRCR/CPFL/US/ – This set of qualifiers is used to indicate that the Debit/Credit 
entry is for a Coupon Payment on an outstanding or maturing Fail. The qualifiers will be 
followed by the Security Identifier ([[CUSIP]]). The [[CUSIP]] will be preceded by “/US/”. 
• /GSCC/DRCR/MARP/US/ – This set of qualifiers is used to indicate that the Debit/Credit 
entry is for a Maturity Principal Payment on an outstanding Repo. The qualifiers will be 
followed by the Security Identifier ([[CUSIP]]). The [[CUSIP]] will be preceded by “/US/”. 
• /GSCC/DRCR/MAFL/US/ – This set of qualifiers is used to indicate that the Debit/Credit 
entry is for a Maturity Principal Payment on an outstanding Fail. The qualifiers will be 
followed by the Security Identifier ([[CUSIP]]). The [[CUSIP]] will be preceded by “/US/”. 
• /GSCC/DRCR/FMFF/US/ – This qualifier is used to indicate that the entry is for Per Trade 
Forward [[Margin]] The qualifiers will be followed by the Security Identifier ([[CUSIP]]). The 
[[CUSIP]] will be preceded by “/US/”. 
Note:  
While the Forward [[Margin]] and Forward Finance Amounts are reflected as two separate Debits or 
Credits on the [[GSD]] Proprietary MRO (Machine Readable Output), they are aggregated and reflected 
as one Amount (Debit/Credit) in Tag 32 on the MT590 Per Trade Forward [[Margin]] Record. 
• /SECO – (Secondary External Reference) – This sub field is optional but will be reflected 
on Repo transaction related Records if the Secondary Reference Number were originally 
provided by the Submitting [[Member]]. 
e.g., :71B:/GSCC/DRCR/CPRP/US/912810SF6/SECO1234ABC1 
 
 
  

---

## Page 67

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 67 
 
MT590 Message Mapping 
This section contains a message mapping for the fields that may be found on each MT590 Message. The mapping is separated into two categories; 1) 
Repo Coupon Payment (mapped to MRO Record Type 38) and 2) Per Trade Forward [[Margin]] (mapped to MRO Record Type 39). 
MT590 (Repo Coupon / Maturity Payment)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 38 Fields 
M/O Tag Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  Message Header         
M   Password 12!c      [[GSD]] will blank fill the Password 
fields on all outgoing messages. 
M   Sender 8!c      GSCCTRRS 
M   Message Type 3!n/3!n/4!c      All 3 fixed-length sub fields will be 
populated. 
M   Receiver 8!c [[Member]] [[ID]] 4 19 22 A/N 4-character [[GSD]] [[Member]] [[ID]]. 
M :20: Transaction Reference Number 
([[GSD]] Assigned Reference Number 
– TID or OID) 
16x Transaction 
[[ID]] 
11 64 74 A/N 
[[GSD]] Transaction / Obligation 
Reference Number (TID or OID). 
The TID will be used for repo 
transaction records and the OID 
will be used for fail related records.
 
M :21: Related Reference ([[Member]] 
External Reference Number) 
16x External 
Reference 
Number 
16 44 59 A/N [[Member]] External Reference 
Number. 
M :25: Account Identification ([[Member]] [[ID]]) 35x [[Member]] [[ID]] 4 19 22 A/N 4-character [[GSD]] [[Member]] [[ID]]. 
M :32C: Value Date, Currency Code, 
Amount Credited 
or 
6!n3!a15d Credit / 
Debit 
1 93 93 A/N If Credit, use “C” Format. 
    Date     No current [[GSD]] field. 

---

## Page 68

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 68 
 
MT590 (Repo Coupon / Maturity Payment)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 38 Fields 
M/O Tag Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
    Payment 
Amount 
18 75 92 A/N Amount is always preceded by 
ISO Currency Code “USD” (“USD” 
used for all [[GSD]] domestic 
activity). Decimal comma 
mandatory-different field sizes. 
M :32D: Value Date, Currency Code, 
Amount Debited 
6!n3!a15d Credit / 
Debit 
1 93 93 A/N If Debit, use “D” Format. 
    Date     No current [[GSD]] field. 
    Payment 
Amount 
18 75 92 A/N Amount is always preceded by 
ISO Currency Code “USD” (“USD” 
used for all [[GSD]] domestic 
activity). Decimal comma 
mandatory-different field sizes. 
M :71B: Details of Charges (6*35x)       
  /GSCC/DRCR/CPRP/US/  
or 
20x  9 29 37 A/N Used for Coupon Payment on 
outstanding Repo (Repo Coupon 
Payment). 
  /GSCC/DRCR/CPFL/US/  
or 
  9 29 37 A/N Used for Coupon Payment on 
outstanding Fail (Fail Coupon 
Payment). 
  /GSCC/DRCR/MARP/US/  
or 
  9 29 37 A/N Used for Maturity Principal on 
outstanding Repo (Repo Maturity 
Payment). 
  /GSCC/DRCR/MAFL/US/ 
and 
  9 29 37 A/N Used for Maturity Principal on 
outstanding Fail (Fail Maturity 
Payment). 

---

## Page 69

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 69 
 
MT590 (Repo Coupon / Maturity Payment)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 38 Fields 
M/O Tag Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  /SECO 16x  16 94 109 A/N Sub-qualifier for Secondary 
Reference Number will be 
populated where provided by 
[[Member]] on Repo Transactions. 
  

---

## Page 70

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 70 
 
MT590 (Per Trade Forward [[Margin]])  
Message Mapping 
SWIFT Record [[GSD]] Record Type 39 Fields 
M/O Tag Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comment 
  Message Header        
M   Password 12!c      [[GSD]] will blank fill the Password 
fields on all outgoing messages. 
M   Sender 8!c      GSCCTRRS 
M   Message Type 3!n/3!n/4!c      All 3 fixed-length sub fields will be 
populated. 
M   Receiver 8!c [[Member]] [[ID]] 4 54 57 A/N 4-character [[GSD]] [[Member]] [[ID]]. 
M :20: Transaction Reference Number 
([[GSD]] Assigned Reference Number 
– TID) 
16x Transaction 
[[ID]] 
11 39 49 A/N [[GSD]] Transaction Reference 
Number (TID). The TID will be 
used for trade related records. 
M :21: Related Reference ([[Member]] 
External Reference Number) 
16x External 
Reference 
Number 
16 19 34 A/N [[Member]] External Reference 
Number. 
M :25: Account Identification ([[Member]] [[ID]]) 35x [[Member]] [[ID]] 4 54 57 A/N 4-character [[GSD]] [[Member]] [[ID]]. 
M :32C: Value Date, Currency Code, 
Forward [[Margin]] and Forward 
Finance Amount Credited 
or 
6!n3!a15d Credit / Debit 1 111 / 
130 
111 / 
130 
A/N If Sum of Forward [[Margin]] (Credit / 
Debit) and Forward Finance 
(Credit / Debit) is a Credit, “C” 
Format will be used. Amount is 
always preceded by ISO 3- 
character Currency Code "USD” 
(USD used for all [[GSD]] domestic 
activity). Decimal comma 
mandatory-different field sizes. 
    Date     No current [[GSD]] field. 

---

## Page 71

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 71 
 
MT590 (Per Trade Forward [[Margin]])  
Message Mapping 
SWIFT Record [[GSD]] Record Type 39 Fields 
M/O Tag Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comment 
    Forward 
[[Margin]] 
18 93 110 A/N Map Sum of Forward [[Margin]] 
(Credit/Debit) and Forward 
Finance (Credit/Debit) to 32C 
where sum is a Credit value. 
    Forward 
Finance 
18 112 129 A/N  
M :32D: Value Date, Currency Code, 
Forward [[Margin]] and Forward 
Finance Amount Debited 
6!n3!a15d Credit / Debit 1 111 / 
130 
111 / 
130 
A/N If Sum of Forward [[Margin]] 
(Credit/Debit) and Forward 
Finance (Credit/Debit) is a Debit, 
“D” Format will be used. Amount is 
always preceded by ISO 3-
character Currency Code "USD” 
(USD used for all [[GSD]] domestic 
activity). Decimal comma 
mandatory-different field sizes. 
    Date     No current [[GSD]] field. 
    Forward 
[[Margin]] 
18 93 110 A/N Map sum of Forward [[Margin]] 
(Credit/Debit) and Forward 
Finance (Credit/Debit) to 32D 
where sum is a Debit value. 
Decimal comma mandatory-
different field sizes. 
    Forward 
Finance 
18 112 129 A/N  
M :71B: Details of Charges (6*35x)       

---

## Page 72

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT590 72 
 
MT590 (Per Trade Forward [[Margin]])  
Message Mapping 
SWIFT Record [[GSD]] Record Type 39 Fields 
M/O Tag Field Description Data Field 
Format 
[[GSD]] Field Length Start End Format Comment 
  /GSCC/DRCR/FMFF/US/  
and 
20x      Used for Per Trade Forward 
[[Margin]]/Forward Finance. (No [[GSD]] 
field available for the [[CUSIP]]). 
  /SECO 16x  16 64 79 A/N Sub-qualifier for Secondary 
Reference Number will be 
populated where provided by 
[[Member]] on Repo Transactions. 
  

---

## Page 73

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 73 
 
NETTING INTERACTIVE MESSAGE SPECIFICATIONS – 
MT950 
This section contains the detailed specifications including layout and field descriptions for the MT950 
Messages supporting output for [[GSD]]’s products and services. 
MT950 Statement Message Description 
The MT950 Message is specified as a Statement Message. The message is basically structured like a Bank 
Statement reflecting an Opening Balance, a series of entries, and a Closing Balance.  
Each entry on the Statement Message is represented by a statement line, which is a concatenation of virtually 
all pertinent data for that entry. The structure of each MT950 message differs slightly by the type of message. 
These messages will be used to transmit detailed information to Members for funds [[settlement]] and/or 
reconciliation purposes. [[GSD]] will use the MT950 Message for two categories of records:  
1. The [[participant]] Net Summary reflects all components of a [[Member]]’s Funds [[settlement]] Obligation with 
[[GSD]]. It is sent to the [[Member]] twice per day and includes the following components (reflected as 
statement lines/entries): 
 
Trans Type [[ID]] Code Funds [[settlement]] Component 
FTAP Next Day TAP 
FFMK Fail Mark 
FCPN Coupon Payment 
FFLM Matured Items 
FCDF Clearance Difference 
FMAD Miscellaneous Adjustments 
FFMA Forward Mark Allocation 
FFMR Forward Mark Allocation Return 
FCPD Collected/Paid 
FINV Invoice (Billing Statement) 
FDDF Delivery Differential 
FGCF GCF Statement Balance * 
FMGN [[Margin]] Interest  
Note:  
The FGCF component is only collected once daily. This field will be either blank or “0,” for the intra-day MT950 [[participant]] 
Net Summary. 

---

## Page 74

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 74 
 
 
2. The Security Net Summary, which is an “aggregation” of two MRO Record Types that are currently 
generated by [[GSD]], 1) Record Type 20 (Security Net Summary) and 2) Record Type 28 (Forward Position 
Summary). The [[Member]] will receive one MT950 Security Net Summary message for each security in 
which it has activity for netting eligible [[securities]] for a given day. It is sent to the [[Member]] twice per day 
and includes the following components (reflected as statement lines/entries): 
 
Trans Type [[ID]] Code Funds [[settlement]] Component 
FNDP Next Day Position 
FFLP Fail Position 
FFMK Fail Mark 
FCPN Coupon Payment 
FFLM Matured Items 
FTAP Next Day TAP 
FCDF Clearance Difference 
FFAI Fail Accrued Interest 
FDDF Delivery Differential 
FFPS Forward Position 
FFAM Forward Amount 
FFWM Forward Mark 
FFMA Forward Mark Allocation 
FPOS [[GSD]] Position Offset 
FCAS [[GSD]] Cash Offset  
 
Note:  
The Opening and Closing Balances on MT950 messages are required mandatory fields. Because the MT950 is a 
statement vehicle and SWIFT requires that one statement’s Ending Balance must be the next statement’s Opening 
Balance, the Opening and Closing Balances must tie in. To [[DO]] this,  [[GSD]] zeroes out these balance fields by including 
offsetting entries/lines on the statement. The last two entries on each Security Net Summary (prior to the Ending Balance) 
are Position Offset (FPOS) and Cash Offset (FCAS) Amounts, which will force the Ending Balance to calculate to zero (“0”). 
All Security Net Summary Statements will, therefore, have Opening and Closing Credit Balances of “0,”. 
Note:  
All entries are reflected as either Debits or Credits. Therefore, where position rather than money entries are provided on 
statement, a Long Position = Credit and a [[short position]] = Debit. 
  

---

## Page 75

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 75 
 
MT950 Statement Message Specifications 
MT950 General Format 
This section provides the general format for the MT950 Message. The general format is separated into two  
categories; 1) [[participant]] Net Summary and 2) Security Net Summary. 
 
MT950 Statement Message  ([[participant]] Net Summary) 
General Format 
M/O Tag Field Description Data Field 
Format 
Sub Field 
Description 
Sub Field Format 
  Message Header    
M   Password 12!c   
M   Sender 8!c   
M   Message Type 3!n/3!n/4!c   
M   Receiver 8!c   
M :20: Transaction Reference Number  16x 
(1!a2!c1!c9!c1!a) 
This tag/field includes the following sub 
fields: 
Report Type 1!a 
Sequence Number 2!c 
Security [[ID]] Type 1!c 
Security [[ID]] 9!c 
Source Business 1!a 
M :25: Account Identification ([[Member]] [[ID]]) 35x   
M :28C: Statement Number 5n   
M :60F: Opening Balance 1!a6!n3!a15d This tag/field includes the following sub 
fields: 
Debit / Credit Mark 1!a 
Date YYMMDD 
Currency Code 3!a 
Amount 15d 
O :61: Statement Line 6!n2a15d1!a3!c 
16x[//16x] 
[34x] 
This tag/field is a repeating sequence within 
the message, for each entry (transaction 
type) on the statement, and includes the 
following sub fields: 
Date YYMMDD 
Debit / Credit Mark 2!a 

---

## Page 76

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 76 
 
MT950 Statement Message  ([[participant]] Net Summary) 
General Format 
M/O Tag Field Description Data Field 
Format 
Sub Field 
Description 
Sub Field Format 
Amount 15d 
Transaction Type 1!a3!c 
Account Owner 
Reference 
16x 
Account’s Servicing 
Institution Reference 
[//16x] 
Supplementary 
Details 
[34x] 
M :62F: Closing Balance 1!a6!n3!a15d This tag/field includes the following sub 
fields: 
Debit / Credit Mark 1!a 
Date YYMMDD 
Currency Code 3!a 
Amount 15d 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

---

## Page 77

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 77 
 
 
MT950 Statement Message  (Security Net Summary) 
General Format 
M/O Tag Field Description Data Field 
Format 
Sub Field 
Description 
Sub Field Format 
  Message Header    
M   Password 12!c   
M   Sender 8!c   
M   Message Type 3!n/3!n/4!c   
M   Receiver 8!c   
M :20: Transaction Reference Number  16x 
(1!a2!c1!c9!c1!a) 
This tag/field includes the following sub 
fields: 
Report Type 1!a 
Sequence Number 2!c 
Security [[ID]] Type 1!c 
Security [[ID]] 9!c 
Source Business 1!a 
M :25: Account Identification ([[Member]] [[ID]]) 35x   
M :28C: Statement Number 5n   
M :60F: Opening Balance 1!a6!n3!a15d This tag/field includes the following sub 
fields: 
Debit / Credit Mark 1!a 
Date YYMMDD 
Currency Code 3!a 
Amount 15d 
O :61: Statement Line 6!n2a15d1!a3!c 
16x[//16x] 
[34x] 
This tag/field is a repeating sequence within 
the message, for each entry (transaction 
type) on the statement, and includes the 
following sub fields: 
Date YYMMDD 
Debit / Credit Mark 2!a 
Amount 15d 
Transaction Type 1!a3!c 
Account Owner 
Reference 
16x 

---

## Page 78

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 78 
 
MT950 Statement Message  (Security Net Summary) 
General Format 
M/O Tag Field Description Data Field 
Format 
Sub Field 
Description 
Sub Field Format 
Account’s Servicing 
Institution Reference 
[//16x] 
Supplementary 
Details 
[34x] 
Supplementary Details will contain the 
following sub fields in the first repeating 
sequence 
Coupon Indicator 1!a 
Coupon Rate 15d 
[[settlement]] Price 3!a15d 
M :62F: Closing Balance 1!a6!n3!a15d This tag/field includes the following sub 
fields: 
Debit / Credit Mark 1!a 
Date YYMMDD 
Currency Code 3!a 
Amount 15d 
 
 
  

---

## Page 79

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 79 
 
MT950 Field Specifications 
This section provides the layout and field descriptions for the MT590 Message. The MT548 field specifications 
is separated into two categories; 1) [[participant]] Net Summary and 2) Security Net Summary. 
MT950 Statement Message ([[participant]] Net Summary)  
Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format 
with trailing blanks, where required. 
Password   12!c This field will be blank-filled on all MT950 Messages. 
Sender   8!c “GSCCTRRS” ([[GSD]] Trade Registration and Reconciliation System) will always be the 
sender of the MT950 messages in this document. 
Message Type 3!n/3!n/4!c  The first 3 characters indicate to the recipient the message type (950); the second 3 
positions reflect the version of the message interface (currently always 000). The last 
4 characters indicate the [[issuer]] code to be used in the message (GSCC). 
Receiver 8!c [[Member]] [[ID]] 
20 Transaction Reference Number 
This field contains [[GSD]]’s Sender’s Message Reference for each [[Member]]’s Funds Statement. In order 
to ensure uniqueness of the Reference Number, and to enable the [[Member]] to identify the report being 
sent, [[GSD]] will generate a Transaction Reference Number for the [[participant]] Net Summary, which is 
comprised of the following four (concatenated) sub fields: 
• Report Type – The value “P” will indicate that this MT950 Record reflects the [[participant]] Net 
Summary Report. 
• Sequence Number – A 3-character Sequence Number will be assigned by [[GSD]]. 
• [[Member]] Number – This field will be populated with a 4-character [[GSD]] [[Member]] [[ID]]. 
• Source Business – A 1-character code will identify the business source of the information. 
Currently it will always be “G” representing the Fixed Income Clearing Corporation ([[FICC]]) 
Government [[securities]] Division’s ([[GSD]]) DVP business. 
e.g., :20:PI018X61G 
25 Account Identification 
This tag contains a 4-character [[GSD]] [[Member]] [[ID]]. 
e.g., :25:8X61 
28C Statement Number 
[[GSD]] will generate a 5-character numeric Statement Number for each [[participant]] Summary Report. 
The 5-character Statement Number will be used as the basis for the [[GSD]] Transaction Reference 
Numbers found in each line of this statement (Tag 61). 
e.g., :28C:12345 
60F Opening Balance 
The Opening Balance Tag/Field is a concatenation of the following sub fields: 
• Debit/Credit Mark (Type of Entry) – This field will reflect either “D” for Debit Balances or “C” 
for Credit Balances. 
• Date – [[GSD]] will populate this sub field with the Date the funds must be paid. 

---

## Page 80

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 80 
 
MT950 Statement Message ([[participant]] Net Summary)  
Field Specifications 
Block/Tag Notes 
• Currency Code – A 3-character ISO Currency Code must precede all amounts. For the 
purposes of [[GSD]] domestic business “USD” will always be used. 
• Amount – This field will be populated with an 11-character Opening Balance (and a 
mandatory decimal comma). 
e.g., :60F:C200630USD5127535, 
61 Statement Line 
The Statement Line Tag/Field is a repeating field, which contains the details of each component of a 
[[participant]]’s Funds [[settlement]] Statement. Each line represents an entry for each individual Funds 
[[settlement]] Component and all pertinent information related to each component. The data is presented 
as a (concatenated) continuous string of data made up of the following sub fields: 
• Date – This sub field will contain the Date of the entry (the date payment is required). 
• Debit/Credit Mark (Type of Entry) – This field will contain either a “D” in the case of a Debit 
entry or a “C” in the case of a Credit to the [[Member]]’s Funds [[settlement]] Balance. 
• Amount – This field will contain the Debit/Credit Amount of the specific Funds [[settlement]] 
Component identified in the Transaction Type Identification sub field (that follows). 
• Transaction Type Identification Code – This 4-character code identifies the Funds 
[[settlement]] Component reported in each statement line. The following codes will be used for 
each component/statement line of the [[participant]] Net Summary Report: 
Trans Type [[ID]] Code Funds [[settlement]] Component 
FTAP Next Day TAP 
FFMK Fail Mark 
FCPN Coupon Payment 
FFLM Matured Items 
FCDF Clearance Difference 
FMAD Miscellaneous Adjustments 
FFMA Forward Mark Allocation 
FFMR Forward Mark Allocation Return 
FCPD Collected/Paid 
FINV Invoice (Billing Statement) 
FDDF Delivery Differential 
FGCF GCF Statement Balance  
FMGN [[Margin]] Interest  
 

---

## Page 81

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 81 
 
MT950 Statement Message ([[participant]] Net Summary)  
Field Specifications 
Block/Tag Notes 
Note:  
Where the Transaction Type Identification Code represents a transaction/entry generated by [[GSD]] (the 
Account Servicing Institution), the first character of the code must be “F”. 
• Account Owner Reference – This required sub field will always be populated with the value 
“NONREF”. 
• Account’s Servicing Institution Reference – This sub field will be populated with an 8-
character Reference Number. Positions 1 through 5 of this field will contain the Statement 
Reference Number found in Tag 28C. Positions 6 through 8 will contain a [[GSD]] generated 
Sequence Number to ensure the entry has a unique Reference Number. The data in this sub 
field is preceded by a double slash “//”. 
• Supplementary Details (optional) – This sub field is not applicable on the [[participant]] Net 
Summary except on the statement line pertaining to Miscellaneous Adjustments (Transaction 
Type Indicator sub field = FMAD). It will potentially contain a 30-byte Miscellaneous Reason. 
This sub field is always preceded by a Carriage Return Line Feed (CRLF). 
e.g., :61:200630D1500000,FTAPNONREF//12345AB1  
Note: 
It can be assumed that all statement line entries refer to the same currency as that of the Opening and 
Closing Balances on this statement. For [[GSD]] domestic business “USD” will be the applicable currency. 
It should also be reiterated that the Supplementary Details sub field is the only one separated out from 
the rest by a Carriage Return Line Feed (CRLF). All other sub fields in this tag are concatenated. 
62F Closing Balance 
The Closing Balance, like the Opening Balance, is a concatenation of the following sub fields: 
• Debit/Credit Mark (Type of Entry) – This field will reflect either “D” for Debit Balances or “C” 
for Credit Balances. 
• Date – [[GSD]] will populate this sub field with the Date the funds must be paid. 
• Currency Code – A 3-character ISO Currency Code must precede all amounts. For the 
purposes of [[GSD]] domestic business “USD” will always be used. 
• Amount – This field will be populated with an 11-character “Total Funds Obligation” (and a 
mandatory decimal comma). 
e.g., :62F:C200630USD5127535, 
 
 
 
  

---

## Page 82

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 82 
 
MT950 Statement Message (Security Net Summary)  
Field Specifications 
Block/Tag Notes 
Message 
Header 
Each message must contain a Message Header. All header fields are mandatory fixed format 
with trailing blanks, where required. 
Password   12!c This field will be blank-filled on all MT950 Messages. 
Sender   8!c “GSCCTRRS” ([[GSD]] Trade Registration and Reconciliation System) will always be the 
sender of the MT950 messages in this document. 
Message Type 3!n/3!n/4!c  The first 3 characters indicate to the recipient the message type (950); the second 3 
positions reflect the version of the message interface (currently always 000). The last 
4 characters indicate the [[issuer]] code to be used in the message (GSCC). 
Receiver 8!c [[Member]] [[ID]] 
20 Transaction Reference Number 
This field contains [[GSD]]’s Sender’s Message Reference for each [[Member]]’s Security Net Summary 
pertaining to activity in a specific security ([[CUSIP]]). In order to ensure uniqueness of the Reference 
Number, and to enable the [[Member]] to identify the report being sent, [[GSD]] will generate a Transaction 
Reference Number for the Security Net Summary which is comprised of the following five 
(concatenated) sub fields: 
• Report Type – The value “S” will indicate to the [[Member]] that this MT950 Record reflects the 
Security Net Summary Report. 
• Sequence Number – A 2-character Sequence Number will be assigned by [[GSD]]. 
• Security Identifier Type – A 1-character Code will be reflected to identify the Type of 
Security Identifier provided. At this time, the value “1” will always be used for [[GSD]] domestic 
business, indicating that a [[CUSIP]] will follow. 
• Security Identifier – This will always be populated with a 9-character [[CUSIP]] for [[GSD]] 
domestic business. 
• Source Business – A 1-character code will identify the business source of the information. 
Currently it will always be “G” representing the Fixed Income Clearing Corporation ([[FICC]]) 
Government [[securities]] Division’s ([[GSD]]) DVP business. 
e.g., :20:S011912810SF6G 
25 Account Identification 
This tag contains a 4-character [[GSD]] [[Member]] [[ID]]. 
e.g., :25:8X61 
28C Statement Number 
[[GSD]] will generate a 5-character numeric Statement Number for each Security Net Summary Report. 
A [[Member]] will receive a separate MT950 Security Net Summary Report each day for each security in 
which it has activity. The 5-character Statement Number will be used as the basis for the [[GSD]] 
Transaction Reference Numbers in each line of this statement (Tag 61). 
e.g., :28C:12345 

---

## Page 83

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 83 
 
MT950 Statement Message (Security Net Summary)  
Field Specifications 
Block/Tag Notes 
60F Opening Balance 
The Opening Balance Tag/Field is a concatenation of the following sub fields: 
• Debit/Credit Mark (Type of Entry) – This field (for Opening Balanced) will always be 
populated with “C” for Credit Balances. 
• Date – This field will always be populated with the appropriate Date for the beginning of day 
positions and cash entries in this report for the security identified in Tag 20. 
• Currency Code – A 3-character ISO Currency Code must precede all amounts. For the 
purposes of [[GSD]] domestic business “USD” will always be used. 
• Amount – This field will always be populated with “0,”. 
e.g., :60F:C200630USD5127535, 
Note: 
There is no applicable Opening Balance for this report, but this field is a required mandatory field for 
the SWIFT format. Because of this, the Opening (and Closing) Balance will always be populated with a 
zero (“0,”) Credit Balance. 
61 Statement Line 
The Statement Line Tag/Field is a repeating field, which contains the details of each component of a 
[[Member]]’s Security Net Summary. Each line represents an entry for each Position and Funds Activity 
Component for a given security. It should be noted that this statement is a combination of the Security 
Net Summary (Record Type 20) and the Forward Position Summary Report (Record Type 28) which 
are currently provided separately in [[GSD]]’s Proprietary MRO. 
• Date – This sub field will contain the Date of the entry (equal to the date in Tag 60F). 
• Debit/Credit Mark (Type of Entry) – This field will contain either a “D” in the case of a Debit 
entry or a “C” in the case of a Credit. 
Note:  
Entries referring to Positions rather than cash will reflect a “D” in the case of a [[Member]] Short (S) 
Position, and a “C” where the [[Member]] is Long (L). 
• Amount – This field will contain the Debit/Credit Amount of the specific Security Net 
[[settlement]] Component identified in the Transaction Type Identification sub field (that 
follows). 
• Transaction Type Identification Code – This 4-character code identifies the Funds 
[[settlement]] Component reported in each statement line. The following codes will be used for 
each component/statement line of each Security Summary Report at the [[CUSIP]] level: 
Trans Type [[ID]] Code Funds [[settlement]] Component 
FNDP Next Day Position 
FFLP Fail Position 
FFMK Fail Mark 
FCPN Coupon Payment 

---

## Page 84

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 84 
 
MT950 Statement Message (Security Net Summary)  
Field Specifications 
Block/Tag Notes 
FFLM Matured Items 
FTAP Next Day TAP 
FCDF Clearance Difference 
FFAI Fail Accrued Interest 
FDDF Delivery Differential 
FFPS Forward Position 
FFAM Forward Amount 
FFWM Forward Mark 
FFMA Forward Mark Allocation 
 
Because each statement must balance, each sequential statement must be linked between 
the Closing Balance of one report to the Opening Balance of the next. [[GSD]] will, therefore, 
add the following two statement lines that include offsetting Position and Cash Entries that 
will force the Closing Balance to be zero (“0”) for each security. Please ignore the statement 
lines including the following two codes. These are not intended as entries to be processed by 
[[Member]], they are on the message only to ensure compliance with SWIFT standards: 
Trans Type [[ID]] Code Funds [[settlement]] Component 
FPOS [[GSD]] Position Offset 
FCAS [[GSD]] Cash Offset  
Note:  
Where the Transaction Type Identification Code represents a transaction/entry generated by [[GSD]] (the 
Account Servicing Institution), the first character of the code must be “F”. 
• Account Owner Reference – This required sub field will always be populated with the value 
“NONREF”. 
• Account’s Servicing Institution Reference – This sub field will be populated with an 8-
character Reference Number. Positions 1 through 5 of this field will contain the Statement 
Reference Number found in Tag 28C. Positions 6 through 8 will contain a [[GSD]] generated 
Sequence Number to ensure the entry has a unique Reference Number. The data in this sub 
field is preceded by a double slash “//”. 
• Supplementary Details (optional) – This sub field will only be populated on records 
pertaining to non-generic CUSIPs/[[securities]], and will only appear in the first repeating 
statement line of each Security Net Summary message to reflect the following information: 
o Coupon Indicator – This sub field indicates if the Coupon is Real “R” or Assumed 
“A”. 
o Coupon Rate – This sub field will indicate the Coupon Rate of the security pertaining 
to this Security Summary Report. 

---

## Page 85

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 85 
 
MT950 Statement Message (Security Net Summary)  
Field Specifications 
Block/Tag Notes 
o [[settlement]] Price – This sub field will indicate the [[GSD]] [[settlement]] Price for the given 
security. The Price is always prefixed by a 3-character ISO Currency Code, which, 
for the purposes of [[GSD]] domestic business, will be “USD”. 
This Supplementary Details sub field is always preceded by a Carriage Return Line Feed 
(CRLF). 
 
e.g., :61:200630D1500000,FTAPNONREF//12345AB1R3,5USD99,5  
Note: 
Only the first repeating statement line will reflect the Coupon Indicator, Coupon and [[settlement]] Price. 
62F Closing Balance 
The Closing Balance, like the Opening Balance, is a concatenation of the following sub fields: 
• Debit/Credit Mark (Type of Entry) – This field will reflect either “D” for Debit Balances or “C” 
for Credit Balances. 
• Date – This field will always be populated with the appropriate Date for the beginning of day 
Positions and cash entries reflected in this report for the security identified in Tag 20. 
• Currency Code – A 3-character ISO Currency Code must precede all amounts. For the 
purposes of [[GSD]] domestic business “USD” will always be used. 
• Amount – This field will always be populated with “0,”. 
e.g., :62F:C200630USD0, 
Note: 
There is no applicable Closing Balance for this report, but this field is a required mandatory field for the 
SWIFT format. Because of this, the Closing Balance will always be populated with a zero (“0,”) Credit 
Balance. 
  

---

## Page 86

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 86 
 
MT950 Message Mapping 
This section contains a message mapping for the fields that may be found on each MT950 Message. The mapping is separated into two categories; 1) 
[[participant]] Net Summary (mapped to MRO Record Type  21) and 2) Security Net Summary (mapped to MRO Record Type 20 and 28, respectively). 
Note:  
In addition to comparing [[GSD]] Proprietary Records to SWIFT Records, the message mappings indicate where there are differences in data requirements, field sizes and 
field formats. The mappings are presented using the MT950 Format. 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Message Header GSCC        
M    Password 12!c      [[GSD]] will blank fill the Password 
fields on all outgoing messages. 
M    Sender 8!c      GSCCTRRS 
M    Message Type 3!n/3!n/4!c      All 3 fixed-length sub fields will 
be populated. 
M    Receiver 8!c [[Member]] [[ID]] 4 19 22 A/N 4-character [[GSD]] [[Member]] [[ID]]. 
M :20:  Transaction Reference 
Number 
16x (1!a3!c4!c1!a)      
[[GSD]] Sender’s Message 
Reference for Funds Statement 
– This field should be used by 
the recipient to determine the 
type of output from [[GSD]]. For 
the [[participant]] Net Summary, 
[[GSD]] will generate a Transaction 

---

## Page 87

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 87 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Reference Number comprised of 
the following four fields: 
• Report Type = P 
([[participant]] summary) 
• Sequence Number 
• [[Member]] Number 
• Source Business = G for 
[[GSD]] DVP Business 
   Report Type 1!a      P = [[participant]] Summary 
   Sequence Number 3!c      3-character sequence number 
assigned by [[GSD]]. 
   [[Member]] Number 4!c [[Member]] [[ID]] 4 19 22 A/N 4-character [[GSD]] [[Member]] [[ID]]. 
   Source Business 1!a      Source Business = G for [[GSD]] 
DVP Business. 
M :25:  Account Identification 
([[Member]] [[ID]]) 
35x [[Member]] [[ID]] 4 19 22 A/N 4-character [[GSD]] [[Member]] [[ID]]. 
M :28C:  Statement Number 5n      [[GSD]] to create Statement 
Number. The 5-character 
Statement Number will be used 
as the basis for the Transaction 
Reference Numbers for each 
line of this statement. 
M :60F:  Opening Balance, which 
includes the following sub 
fields: 
1!a6!n3!a15d      The Opening Balance field is a 
concatenation of the remaining 
fields in this tag sequence. 

---

## Page 88

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 88 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  D or C Debit / Credit Mark 1!a Cr / Dr 
Indicator 
1 40 40 A/N Credit = "C" and Debit = "D". 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  USD Currency Code 3!a      For US Business the ISO 
Currency Code = USD. 
   Amount 15d Opening 
Balance 
11 29 39 A/N Decimal comma mandatory. 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 52 52 A/N Credit = "C" and Debit = "D". 
   Amount  15d Next Day TAP 11 41 51 A/N Decimal comma mandatory. 
  FTAP Transaction Type 
Identification Code 
1!a3!c      Next Day Tap = "FTAP". 
“F” is always used for the first 
character of the code. 

---

## Page 89

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 89 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 

---

## Page 90

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 90 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 64 64 A/N Credit = "C" and Debit = "D". 
   Amount  15d Fail Mark 11 53 63 A/N Decimal comma mandatory. 
  FFMK Transaction Type 
Identification Code 
1!a3!c      Fail Mark = "FFMK". 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     
Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 

---

## Page 91

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 91 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 76 76 A/N Credit = "C" and Debit = "D". 
   Amount  15d Coupon 
Payment 
11 65 75 A/N Decimal comma mandatory. 
  FCPN Transaction Type 
Identification Code 
1!a3!c      Coupon Payment = "FCPN". 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 

---

## Page 92

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 92 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 88 88 A/N Credit = "C" and Debit = "D". 
   Amount  15d Fail that 
Matured 
11 77 87 A/N Decimal comma mandatory. 
  FFLM Transaction Type 
Identification Code 
1!a3!c      Matured Items = "FFLM". 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      
[[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 

---

## Page 93

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 93 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 100 100 A/N Credit = "C" and Debit = "D". 
   Amount  15d Clearance 
Difference 
11 89 99 A/N Decimal comma mandatory. 
  FCDF Transaction Type 
Identification Code 
1!a3!c      Clearance Difference = "FCDF". 

---

## Page 94

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 94 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 

---

## Page 95

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 95 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 112 112 A/N Credit = "C" and Debit = "D". 
   Amount  15d Miscellaneous 
Adjustment 
11 101 111 A/N Decimal comma mandatory. 
  FMAD Transaction Type 
Identification Code 
1!a3!c      Miscellaneous Adjustments = 
"FMAD". 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] Miscellaneous 
Reason 
30 113 142 A/N Reason for Miscellaneous 
Adjustment – This sub field is 
always preceded / separated by 
a Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 

---

## Page 96

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 96 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 154 154 A/N Credit = "C" and Debit = "D". 
   Amount  15d Forward Mark 
Allocation 
11 143  153 A/N Decimal comma mandatory. 
  FFMA Transaction Type 
Identification Code 
1!a3!c      Forward Mark Allocation = 
"FFMA". 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 

---

## Page 97

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 97 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 166 166 A/N Credit = "C" and Debit = "D". 
   Amount  15d Forward Mark 
Allocation 
Return 
11 155 165 A/N Decimal comma mandatory. 
  FFMR Transaction Type 
Identification Code 
1!a3!c      Forward Mark Allocation Return 
= "FFMR". 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 

---

## Page 98

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 98 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 178 178 A/N Credit = "C" and Debit = "D". 
   Amount  15d Collected / 
Paid 
11 167 177 A/N Decimal comma mandatory. 

---

## Page 99

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 99 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  FCPD Transaction Type 
Identification Code 
1!a3!c      Collected/Paid = "FCPD". 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 

---

## Page 100

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 100 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 190 190 A/N Credit = "C" and Debit = "D". 
   Amount  15d Invoice 11 179 189 A/N Decimal comma mandatory. 
  FINV Transaction Type 
Identification Code 
1!a3!c      Invoice = “FINV”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
     
Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 

---

## Page 101

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 101 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
[34x] each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 226 226 A/N Credit = "C" and Debit = "D". 
   Amount  15d Delivery 
Differential 
11 215 225 A/N Decimal comma mandatory. 
  FDDF Transaction Type 
Identification Code 
1!a3!c      Delivery Differential = "FDDF". 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 

---

## Page 102

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 102 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
    Credit = "C" and Debit = "D". 
   Amount  15d      Decimal comma mandatory. 
  FGCF Transaction Type 
Identification Code 
1!a3!c      FGCF (No current [[GSD]] field.) 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      
[[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 

---

## Page 103

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 103 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the fields in 
each repeating sequence. 
Only the Supplementary 
Details sub field, where 
populated, should always be 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
1 238 238 A/N Credit = "C" and Debit = "D". 
   Amount  15d [[Margin]] 
Interest 
11 227 237 A/N Decimal comma mandatory. 
  FMGN Transaction Type 
Identification Code 
1!a3!c      [[Margin]] Interest = "FMGN". 

---

## Page 104

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 104 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Funds [[settlement]] Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
M :62F:  Closing Balance (Booked 
Funds) 
1!a6!n3!a15d       
  D or C Debit / Credit Mark 1!a Cr / Dr 
Indicator 
1 202 202 A/N Credit = "C" and Debit = "D". 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  USD Currency Code 3!a      For US Business, ISO Currency 
Code = USD. 

---

## Page 105

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 105 
 
MT950 Statement ([[participant]] Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Type 21 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Amount  15d Total Funds 
Obligation 
11 191 201 A/N Decimal comma mandatory. 
  

---

## Page 106

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 106 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Message Header GSCC        
M    Password 12!c      [[GSD]] will blank fill the Password 
fields on all outgoing messages. 
M    Sender 8!c      GSCCTRRS 
M    Message Type 3!n/3!n/4!c      All 3 fixed-length sub fields will 
be populated. 
M    Receiver 8!c [[Member]] [[ID]] 4 19 22 A/N 4-character [[GSD]] [[Member]] [[ID]]. 
M :20:  Transaction Reference 
Number 
16x 
(1!a2!c1!c9!c1!a) 
     [[GSD]] Sender’s Message 
Reference Number for Security 
Summary. This field should be 
used, by the recipient, to 
determine the type of output 
from [[GSD]]. For the Security 
Summary, [[GSD]] will generate a 
Transaction Reference Number 
comprised of the following five 
fields, specific to the Security 
Summary: 
• Report Type = S (Security 
Summary) 
• Sequence Number 
• Security Identifier Type = 
"1" (1 = [[CUSIP]]) 
• Security Identifier 
• Source Business = G for 
[[GSD]] DVP Business 
   Report Type 1!a      S = Security Summary. 

---

## Page 107

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 107 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Sequence Number 2!c      2-character sequence number 
assigned by [[GSD]]. 
   Security Identifier Type 1!c      [[CUSIP]] = “1”. 
   Security Identifier 9!c [[CUSIP]] 
Number 
(Record 20) 
9 29 37 A/N For US business, [[CUSIP]] will be 
used. 
   Source Business 1!a      Source Business = G for [[GSD]] 
DVP Business. 
M :25:  Account Identification 
([[Member]] [[ID]]) 
35x [[Member]] [[ID]] 4 19 22 A/N 4-character [[GSD]] [[Member]] [[ID]]. 
M :28C:  Statement Number 5n      A [[Member]] will receive a 
separate report for each security 
in which it has activity. A 5-
character Statement Number 
will be used as the basis for the 
Transaction Reference Numbers 
for each line of this statement. 
M :60F:  Opening Balance which 
includes the following sub 
fields: 
1!a6!n3!a15d      The Opening Balance field is a 
concatenation of the remaining 
fields in this tag sequence. 
Opening Balance must always 
by “C”, given that the Balance 
will always be “0,". Decimal 
comma mandatory. 
  D or C Debit / Credit Mark 1!a      Credit = "C" and Debit = "D". 

---

## Page 108

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 108 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Opening Balance should always 
be “0,” For this report, “C” must 
be used. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  USD Currency Code 3!a      For US Business the ISO 
Currency Code = USD. 
   Amount 15d      The Opening Balance will 
always be “0,”. 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 

---

## Page 109

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 109 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  D or C Debit / Credit Mark 2a Long / Short 
Indicator 
(Record 20) 
1 76 76 A/N Long = Credit = L = “C” 
Short = Debit = S = “D” 
   Amount  15d Next Day 
Position 
(Record 20) 
18 58 75 A/N Decimal comma mandatory-
different field sizes. 
  FNDP Transaction Type 
Identification Code 
1!a3!c      Next Day Position = “FNDP”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     The remaining fields listed here 
(Coupon Indicator, Coupon and 
[[settlement]] Price) will only be 
placed in the first repeating 
sequence. This sub field, where 
populated, will always be 
preceded / separated by a 

---

## Page 110

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 110 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Carriage Return Line Feed 
(CRLF). 
   Coupon Indicator 1!a Coupon 
Indicator 
(Record 28) 
1 134 134 A/N Assumed = "A" 
Real = "R" 
   Coupon Rate 15d Coupon Rate 
(Record 28) 
10 135 144 A/N Decimal comma mandatory. 
  USD [[settlement]] Price 3!a15d [[settlement]] 
Price Type / 
Price  
(Record 20) 
14 44 57 A/N Field prefixed with 3-character 
ISO Currency Code (USD will 
always be used for [[GSD]] 
domestic activity). Decimal 
comma mandatory. 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 

---

## Page 111

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 111 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Long / Short 
Indicator 
(Record 20) 
1 95 95 A/N Long = Credit = L = “C” 
Short = Debit = S = “D” 
   Amount  15d Fail Position 18 77 94 A/N Decimal comma mandatory-
different field sizes. 
  FFLP Transaction Type 
Identification Code 
1!a3!c      Fail Position = “FFLP”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always be preceded / 
separated by a Carriage Return 
Line Feed (CRLF). 

---

## Page 112

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 112 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 20) 
1 114 114 A/N Credit = "C" and Debit = "D". 
   Amount  15d Fail Mark 
(Record 20) 
18 96 113 A/N Decimal comma mandatory-
different field sizes. 
  FFMK Transaction Type 
Identification Code 
1!a3!c      Fail Mark = “FFMK”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 

---

## Page 113

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 113 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always be preceded / 
separated by a Carriage Return 
Line Feed (CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 

---

## Page 114

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 114 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 20) 
1 133 133 A/N Credit = "C" and Debit = "D". 
   Amount  15d Coupon 
Payment 
(Record 20) 
18 115 132 A/N Decimal comma mandatory-
different field sizes. 
  FCPN Transaction Type 
Identification Code 
1!a3!c      Coupon Payment = "FCPN". 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      
[[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 

---

## Page 115

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 115 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always be preceded / 
separated by a Carriage Return 
Line Feed (CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 20) 
1 152 152 A/N Credit = "C" and Debit = "D". 
   Amount  15d Fails that 
Matured 
18 134 151 A/N Decimal comma mandatory-
different field sizes. 

---

## Page 116

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 116 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  FFLM Transaction Type 
Identification Code 
1!a3!c      Matured Items = “FFLM”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always be preceded / 
separated by a Carriage Return 
Line Feed (CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 

---

## Page 117

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 117 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 20) 
1 171 171 A/N Credit = "C" and Debit = "D". 
   Amount  15d Next Day TAP 
(Record 20) 
18 153 170 A/N Decimal comma mandatory-
different field sizes. 
  FTAP Transaction Type 
Identification Code 
1!a3!c      Next Day TAP = “FTAP”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      
[[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 

---

## Page 118

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 118 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always be preceded / 
separated by a Carriage Return 
Line Feed (CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 20) 
1 190 190 A/N Credit = "C" and Debit = "D". 

---

## Page 119

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 119 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Amount  15d Clearance 
Differences 
(Record 20) 
18 172  189 A/N Decimal comma mandatory-
different field sizes. 
  FCDF Transaction Type 
Identification Code 
1!a3!c      Clearance Differences = 
“FCDF”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     
Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 

---

## Page 120

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 120 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 20) 
1 209 209 A/N Credit = "C" and Debit = "D". 
   Amount  15d Fail Accrued 
Interest 
(Record 20) 
18 191 208 A/N Decimal comma mandatory-
different field sizes. 
  FFAI Transaction Type 
Identification Code 
1!a3!c      Fail Accrued Interest = “FFAI”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      
[[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 

---

## Page 121

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 121 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always preceded / separated 
by a Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 

---

## Page 122

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 122 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 20) 
1 228 228 A/N Credit = "C" and Debit = "D". 
   Amount  15d Delivery 
Differential 
(Record 20) 
18 210 227 A/N Decimal comma mandatory-
different field sizes. 
  FDDF Transaction Type 
Identification Code 
1!a3!c      Delivery Differential = “FDDF”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always preceded / separated 
by a Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 

---

## Page 123

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 123 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
[34x] fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Long / Short 
Indicator 
(Record 28) 
1 66 66 A/N Short = Debit = L = “C” 
Long = Credit = S = “D” 
   Amount  15d Forward 
Position 
(Record 28) 
18 48 65 A/N Decimal comma mandatory-
different field sizes. 
  FFPS Transaction Type 
Identification Code 
1!a3!c      Forward Position = “FFPS”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      
[[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 

---

## Page 124

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 124 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always preceded / separated 
by a Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 

---

## Page 125

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 125 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 28) 
1 85 85 A/N Credit = "C" and Debit = "D". 
   Amount  15d Forward 
Amount 
(Record 28) 
18 67 84 A/N Decimal comma mandatory-
different field sizes. 
  FFAM Transaction Type 
Identification Code 
1!a3!c      Forward Amount = “FFAM”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always preceded / separated 
by a Carriage Return Line Feed 
(CRLF). 

---

## Page 126

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 126 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 28) 
1 104 104 A/N Credit = "C" and Debit = "D". 
   Amount  15d Forward Mark 
(Record 28) 
18 86 103 A/N Decimal comma mandatory-
different field sizes. 
  FFWM Transaction Type 
Identification Code 
1!a3!c      Forward Mark = “FFWM”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 

---

## Page 127

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 127 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field, where populated, 
will always preceded / separated 
by a Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 

---

## Page 128

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 128 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a Cr / Dr 
Indicator 
(Record 28) 
1 123 123 A/N Credit = "C" and Debit = "D". 
   Amount  15d Forward Mark 
Allocation 
(Record 28) 
18 105 122 A/N Decimal comma mandatory-
different field sizes. 
  FFMA Transaction Type 
Identification Code 
1!a3!c      Forward Mark Allocation = 
“FFMA”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 

---

## Page 129

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 129 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This sub field is always 
preceded / separated by a 
Carriage Return Line Feed 
(CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
Note:  
This statement line / entry 
(FPOS) should be ignored by the 
[[Member]]. It is required to offset 
above Position information to 
create an Ending Balance of “0,” 
for this statement. [[DO]] NOT USE. 

---

## Page 130

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 130 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a      Debit = "D" and Credit = "C". 
Where sum of FNDP, FFLP, and 
FFPS is a Debit Amount, a “C” 
will be placed in this field. 
Where sum of FNDP, FFLP and 
FFPS is a Credit Amount, a “D” 
will be placed in this field. 
   Amount  15d      The sum of FNDP, FFLP and 
FFPS is placed in this field. 
Decimal comma mandatory. 
  FPOS Transaction Type 
Identification Code 
1!a3!c      [[GSD]] Position Offset = “FPOS”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      [[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 

---

## Page 131

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 131 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Supplementary Details [34x] N/A     This subfield, where populated, 
will always be preceded / 
separated by a Carriage Return 
Line Feed (CRLF). 
O :61:  Statement Line 6!n2a15d1!a3!c16
x[//16x] 
[34x] 
     Each Statement Line (:61:) is 
a continuous string of data, 
concatenating all the sub 
fields in each repeating 
sequence. Only the 
Supplementary Details sub 
field, where populated, should 
always be preceded / 
separated by a Carriage 
Return Line Feed (CRLF). 
Note:  
Only the first repeating sequence 
will reflect the Coupon Indicator, 
Coupon and [[settlement]] Price. 
Note:  
This statement line / entry 
(FCAS) should be ignored by the 
[[Member]]. It is required to offset 
above Position information to 
create an Ending Balance of “0,” 
for this statement. [[DO]] NOT USE. 

---

## Page 132

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 132 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  D or C Debit / Credit Mark 2a      Debit = "D" and Credit = "C". 
Where sum of FFMK, FCPN, 
FFLM, FTAP, FCDF, FFAI, 
FDDF, FFAM, FFWM and FFMA 
is a Debit Amount, a “C” will be 
placed in this field. 
Where sum of FFMK, FCPN, 
FFLM, FTAP, FCDF, FFAI, 
FDDF, FFAM, FFWM and FFMA 
is a Credit Amount, a “D” will be 
placed in this field. 
   Amount  15d      The sum of FFMK, FCPN, 
FFLM, FTAP, FCDF, FFAI, 
FDDF, FFAM, FFWM and FFMA 
will be placed in this field. 
Decimal comma mandatory. 
  FCAS Transaction Type 
Identification Code 
1!a3!c      [[GSD]] Money Offset = “FCAS”. 
   Account Owner Reference 16x      “NONREF” will be used to 
populate this field. 
  // Account’s Servicing 
Institution Reference 
[//16x]      
[[GSD]] to generate unique 
Reference Number for each 
Security Summary Component. 
Reference Number will be 8 
characters, with the first 5 
characters coming from the 
Statement Number in the first 

---

## Page 133

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Netting Interactive Message Specifications – MT950 133 
 
MT950 Statement (Security Net Summary)  
Message Mapping 
SWIFT Record [[GSD]] Record Types 20 and 28 Fields 
M/O Tag Block/ 
Qualifier 
Field Description Data Field Format [[GSD]] Field Length Start End Format Comment 
sequence (:28C:). The last 3 
characters will be a sequence 
number to make the Transaction 
Reference unique in the 
statement. 
   Supplementary Details [34x] N/A     This subfield, where populated, 
will always be preceded / 
separated by a Carriage Return 
Line Feed (CRLF). 
M :62F:  Closing Balance (Booked 
Funds) 
1!a6!n3!a15d       
  D or C Debit / Credit Mark 1!a      Credit = "C" and Debit = "D". 
“C” must always be used in this 
field, given that the Closing 
Balance will always be zero. 
   Date YYMMDD      [[GSD]] Systems to generate 
Processing / Statement Date. 
  USD Currency Code 3!a      For US Business the ISO 
Currency Code = USD. 
   Amount 15d      Closing Balance amount will 
alwaysbe“0,”. 
Decimal comma mandatory. 
  

---

## Page 134

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 134 
 
APPENDICES 
List of Appendices 
A. Message Flows 
B. Message Samples 
C. Message Timing Matrix 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  

---

## Page 135

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 135 
 
Appendix A – Message Flows 
This appendix of Message Flows contains detailed diagrams depicting the flows of messages to and from [[GSD]] 
for a various transaction related scenarios. 
The following should be noted:  
1. Rather than using the terminology “[[participant]] A” and “[[participant]] B,” [[GSD]] has amended all flows to 
reflect “[[Member]] A” and “[[Member]] B”.  
2. The [[GSD]] Risk and Compliance Management System (Risk) is responsible for providing Members with 
all Risk-related Interactive Reporting, such as information on Guarantees and Netting Eligibility. 
3. The [[GSD]] Clearance Instruction Management System (Clearance) is responsible for capturing and 
processing [[settlement]] information as well as providing all [[settlement]]-related [[Member]] Output.  
4. The [[GSD]] Funds [[settlement]] Management System (Funds) is responsible for providing Members with 
information regarding their [[Margin]], Coupon, Principal Entitlements and Funds [[settlement]] Obligation 
with [[GSD]]. 
5. There are flows in this appendix that may start with the [[GSD]] comparison process and include netting 
and [[settlement]] related message flows for added clarity. Because of this, some flows may not fit on one 
page. Fields marked with an asterisk (*) will be used to mark where flows are continued onto the next 
available page.  
 
  

---

## Page 136

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 136 
 
Listed below are the flows contained in this section: 
Flows 
A.A1 Bilateral Trades Compared 
A.A2 Trade Bound to Net 
A.A3 Trade Comparison Only (End of Processing Life for a "Non-Netting Eligible Trade") 
A.A4 Buy/Sell Transaction in Net (Next Day Settling Cash Trade) 
A.A5 Buy/Sell Transaction in Net (Forward Settling Cash Trade) 
A.A6 Same-Day Settling Start Leg / Close Leg in Net (Overnight Repo) 
A.A7 Same-Day Settling Start Leg / Close Leg in Net (Term Repo) 
A.A8  Next-Day or Forward Settling Start Leg  / Start Leg in Net / Close Leg in Net 
A.A9 Forward Trade Pended/No Longer in Net - No [[collateral]] Assigned to GC Trade (GC [[collateral]] Trade 
Submitted for Forward [[settlement]]) 
A.A10 Forward Trade Pended/No Longer in Net - [[collateral]] Matured - No New [[collateral]] Assigned (Term 
Repo Submitted on / after Start Leg [[settlement]] Date) 
A.A11 Forward Trade Pended/No Longer in Net – Trade Cancelled (Term Repo Submitted on / after Start Leg 
[[settlement]] Date)  
A.A12 Clearance Instruction (Same-Day) 
A.A13 Clearance Instruction (Next Day) 
A.A14 Cleared Obligation (Next Day or Same-Day) 
A.A15    Cleared Obligation via Pair-off  
A.A16 Failed Obligation Netted (for Next Day or Same-Day) 
A.A17 Held Fail (for Next Day or Same-Day) *UPDATED 
A.A18 [[Broker]] Fail 
A.A19 Partial [[settlement]] (Intra-Day – Two Deliveries) *Not applicable to Same-Day Settling Trades 
A.A20 Partial [[settlement]] (Fail Portion Netted) *Not applicable to Same-Day Settling Trades 
A.A21 Repo Substitution [[settlement]] Instruction (New [[collateral]] Provided at the Time of Initial Substitution) 
A.A22 Repo Substitution Notification (New [[collateral]] Not Provided at the Time of Initial Substitution) 
A.A23 Repo Substitution Allocation (New [[collateral]] Provided After Initial Substitution Notification) 

---

## Page 137

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 137 
 
A.A24 Repo Substitution [[settlement]] Instruction ([[collateral]] Substituted Prior to Forward Settling Start Leg) 
A.A25 Fail Coupon Payment and Subsequent Clearance 
A.A26 Fail Maturity Payment 
A.A27 Repo Coupon Payment (Term Repo Submitted After Start Leg [[settlement]] Date) 
A.A28 Repo to Maturity (Forward Settling Start Leg Repo)  
Note: 
In all Repo flows listed above, [[Member]] A is either the Repo Dealer or the Repo [[Broker]] and [[Member]] B is the Reverse 
Dealer. 
 
Supplementary Flows 
A.B1 Bilateral Same-Day Settling Trade – Compared, then Canceled Pre-[[settlement]] 
A.B2  Bilateral Same-Day Settling Trade – Compared then Canceled Post Start Leg [[settlement]] 
A.B3    Brokered (Balanced) Same-Day Settling Trade – Canceled Pre-[[settlement]] 
A.B4    Brokered (Balanced) Same-Day Settling Trade – Canceled Post Start Leg [[settlement]] 
A.B5    Brokered (Unbalanced) Same-Day Settling Trade – Canceled Pre-[[settlement]] 
A.B6 Brokered (Balanced) Same-Day Settling Trade – Contra Dealer DKs/[[Broker]] Cancels Pre-[[settlement]]  
A.B7 Bilateral Overnight As-of Repo Transaction – Uncompared (Day 1), Matched As-of trade by Contra 
(Day 2)   

---

## Page 138

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 138 
 
Flows 
A.A1 Bilateral Trades Compared 
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3. MT515 Trade 
Submission
4b. MT518 Comparison 
Requested
4a. MT509 Trade 
Accepted
[[Member]] A
 [[Member]] B
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
[[GSD]] 
RTTM 
(Match)
Comparison Results
A9
 A28
A11
 A24
A10
 A27
   

---

## Page 139

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 139 
 
A.A2 Trade Bound to Net 
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3. MT515 Trade 
Submission
4b. MT518 Comparison 
Requested
4a. MT509 Trade 
Accepted
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B
[[Member]] A
 [[Member]] B
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
Comparison Results
  

---

## Page 140

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 140 
 
A.A3 Trade Comparison Only ("Non-Netting Eligible Trade") 
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3. MT515 Trade 
Submission
4b. MT518 Comparison 
Requested
4a. MT509 Trade 
Accepted
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B
[[Member]] A
 [[Member]] B
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
6b. MT509 Trade 
Comparison Only
6a. MT509 Trade 
Comparison Only
Comparison Results
  

---

## Page 141

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 141 
 
A.A4 Buy/Sell Transaction in Net (Next Day Settling Cash Trade) 
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3. MT515 Trade 
Submission
4b. MT518 Comparison 
Requested
4a. MT509 Trade 
Accepted
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B
[[Member]] A
 [[Member]] B
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT509 Buy/Sell 
Trade In Net
7a. MT509 Buy/Sell 
Trade In Net
Comparison Results
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
  

---

## Page 142

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 142 
 
A.A5 Buy/Sell Transaction in Net (Forward Settling Cash Trade) 
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3. MT515 Trade 
Submission
4b. MT518 Comparison 
Requested
4a. MT509 Trade 
Accepted
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B
[[Member]] A
 [[Member]] B
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT590 Per Trade 
Forward [[Margin]] *
7a. MT590 Per Trade 
Forward [[Margin]] *
8b. MT509 Buy/Sell 
Trade In Net
8a. MT509 Buy/Sell 
Trade In Net
Comparison Results
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
* Message sent during nightly processing when [[GSD]] marks the trade to market.
  

---

## Page 143

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 143 
 
A.A6 Same-Day Settling Start Leg / Close Leg in Net (Overnight Repo) * 
 
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3. MT515 Trade 
Submission
4b. MT518 Comparison 
Requested
4a. MT509 Trade 
Accepted
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B
[[Member]] A
 [[Member]] B
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT509 Close 
Leg In Net
7a. MT509 Close 
Leg In Net
Comparison Results
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
A14
Assumption
• Same-Day Settling Trade(s) submitted for Bilateral Comparison
• No Same-Day Netting of Start Leg Positions Start Leg Settles at 
Contract Value (Refer to A14 for [[settlement]] of Start Leg)
   

---

## Page 144

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 144 
 
A.A7 Same-Day Settling Start Leg / Close Leg in Net (Term Repo) * 
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3. MT515 Trade 
Submission
4b. MT518 Comparison 
Requested
4a. MT509 Trade 
Accepted
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B
[[Member]] A
 [[Member]] B
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
7b. MT590 Per Trade 
Forward [[Margin]] *
7a. MT590 Per Trade 
Forward [[Margin]] *
9b. MT509 Close 
Leg In Net
9a. MT509 Close 
Leg In Net
Comparison Results
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
Assumption
• Same-Day Settling Trade(s) submitted for Bilateral Comparison
• No Same-Day Netting of Start Leg Positions Start Leg Settles at 
Contract Value (Refer to A14 for [[settlement]] of Start Leg)
A14
* Message sent during nightly processing when [[GSD]] marks the trade to market.
   

---

## Page 145

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 145 
 
A.A8 Next-Day or Forward Settling Start Leg  / Start Leg in Net / Close Leg in Net * 
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
3. MT515 Trade 
Submission
4b. MT518 Comparison 
Requested
4a. MT509 Trade 
Accepted
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B
[[Member]] A
 [[Member]] B
5a. MT509 Trade 
Compared
5b. MT509 Trade 
Compared
5c. MT518 Comparison 
Request Cancel (due to match)
5d. MT518 Comparison 
Request Cancel (due to match)
9b. MT509 Close 
Leg In Net
9a. MT509 Close 
Leg In Net
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
* Message sent during nightly processing when [[GSD]] marks the trade to market.
Comparison Results
8b. MT509 Start Leg 
In Net
8a. MT509 Start Leg 
In Net
7b. MT590 Per Trade 
Forward [[Margin]] *
7a. MT590 Per Trade 
Forward [[Margin]] *
   

---

## Page 146

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 146 
 
A.A9 Forward Trade Pended/No Longer in Net - No [[collateral]] Assigned to GC Trade (GC [[collateral]] 
Trade Submitted for Forward [[settlement]]) * 
A1
[[GSD]] 
(Risk)
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
[[Member]] A
 [[Member]] B
7b. MT590 Per Trade 
Forward [[Margin]] *
7a. MT590 Per Trade 
Forward [[Margin]] *
Comparison Results
8b. MT509 Forward Trade Pended/
No Longer in Net – No [[collateral]] 
Assigned to GC Trade **
8a. MT509 Forward Trade Pended/
No Longer in Net – No [[collateral]] 
Assigned to GC Trade **
 * Message sent during nightly processing when [[GSD]] marks the trade to market.
** Message generated Night of Start Leg [[settlement]] Date - 1.    

---

## Page 147

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 147 
 
A.A10 Forward Trade Pended/No Longer in Net - [[collateral]] Matured - No New [[collateral]] Assigned 
(Term Repo Submitted on / after Start Leg [[settlement]] Date) * 
A1
[[GSD]] 
(Risk)
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
[[Member]] A
 [[Member]] B
7b. MT590 Per Trade 
Forward [[Margin]] *
7a. MT590 Per Trade 
Forward [[Margin]] *
Comparison Results
8b. MT509 Forward Trade Pended/
No Longer in Net – [[collateral]] 
Matured
(No New [[collateral]] Assigned) **
8a. MT509 Forward Trade Pended/
No Longer in Net – [[collateral]] 
Matured 
(No New [[collateral]] Assigned) **
 * Message sent during nightly processing when [[GSD]] marks the trade to market.
** Message generated Night of [[collateral]] Maturity Date - 1.    

---

## Page 148

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 148 
 
A.A11 Forward Trade Pended/No Longer in Net – Trade Cancelled (Term Repo Submitted on / after 
Start Leg [[settlement]] Date) * 
[[Member]] A
 [[Member]] B
A1
[[GSD]] 
(Risk)
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
[[Member]] B
7b. MT590 Per Trade 
Forward [[Margin]] *
7a. MT590 Per Trade 
Forward [[Margin]] *
Comparison Results
 * Message sent during nightly processing when [[GSD]] marks the trade to market.
9b. MT518 Cancel 
Requested
9a. MT509 Cancel 
Accepted
8. MT515 Trade Cancel 10. MT515 Trade Cancel
11b. MT518 Cancel 
Requested
11a. MT509 Cancel 
Accepted
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
[[Member]] A
12a. MT509 Trade 
Cancelled
12b. MT509 Trade 
Cancelled
[[GSD]] 
(Risk)
Cancel Details
13b. MT509 Forward 
Trade Pended/No 
Longer in Net – Trade 
Cancelled
13a. MT509 Forward 
Trade Pended/No 
Longer in Net – Trade 
Cancelled
   

---

## Page 149

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 149 
 
A.A12 Clearance Instruction (Same-Day) 
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
Comparison OutputComparison Output
Trades Trades
[[GSD]] 
(Risk)
[[GSD]] 
(Clearance)
[[Member]] B
1b. MT548 Clearance 
Instruction (Same-Day)
[[Member]] A
1a. MT548 Clearance 
Instruction (Same-Day)
Clearance Instructions
[[GSD]] Clearing Bank
[[Member]] A
 [[Member]] BRisk Related OutputRisk Related Output
Assumption
• Same-Day Settling Trade(s) submitted for Bilateral Comparison
• No Same-Day Netting of Positions
• A = Dealer who is the Deliverer of [[securities]] to [[GSD]]
• B = Dealer who is the Receiver of [[securities]] from [[GSD]] 
• [[Member]] A's delivery is bound to [[Member]] B's receive at [[GSD]]’s 
Clearing Bank
Comparison Results
  

---

## Page 150

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 150 
 
A.A13 Clearance Instruction (Next Day) 
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
Comparison OutputComparison Output
Trades Trades
[[GSD]] 
(Risk)
[[GSD]] 
(Clearance)
[[Member]] B
1b. MT548 Clearance 
Instruction (Next Day)
[[Member]] A
1a. MT548 Clearance 
Instruction (Next Day)
Clearance Instructions
[[GSD]] Clearing Bank
[[Member]] A
 [[Member]] BRisk Related OutputRisk Related Output
Assumption
• Next Day Settling Trade(s) submitted for Bilateral Comparison
• A = Dealer who is the Deliverer of [[securities]] to [[GSD]]
• B = Dealer who is the Receiver of [[securities]] from [[GSD]] 
• [[Member]] A's delivery is bound to [[Member]] B's receive at [[GSD]]’s 
Clearing Bank
Comparison Results
Netting Position 
Results
  

---

## Page 151

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 151 
 
A.A14 Cleared Obligation (Next Day or Same-Day) 
[[GSD]] 
(Clearance)
[[Member]] B
1b. MT548 Clearance 
Instruction 
[[Member]] A
1a. MT548 Clearance 
Instruction
Clearance Instructions
[[GSD]] Clearing Bank
Funds Funds
[[securities]] [[securities]]
[[GSD]]  
(Clearance)
[[Member]] B
[[Member]] A 
2b. MT548 Cleared 
Obligation (Cleared)
2a. MT548 Cleared 
Obligation (Cleared)
Clearance Results
  

---

## Page 152

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 152 
 
A.A15   Cleared Obligation via Pair-off  
[[Member]] A 
Assumption
• [[Member]] A has opted into [[GSD]]’s Pair-off Service
• [[Member]] A has a Netted Obligation to receive 50,000,000 vs. $50,687,125.50 of [[CUSIP]] 912828XYZ from [[GSD]].
• [[Member]] A is also the repo party on a term Brokered Same-Day Starting Repo Demand Trade which resulted in a Same-Day Settling Obligation to deliver 
50,000,000 vs. $50,625,000.00 of [[CUSIP]] 912828XYZ to [[GSD]].
• The Netted Obligation and the Same-Day Settling Obligation are in the same netting eligible security ([[CUSIP]] 912828XYZ) but are not bound to one another.
• At the time the Pair-Off process begins, both the Same-Day Settling Obligation and the Netted Obligation are still pending clearance.
• The above mentioned [[obligations]] are the only [[obligations]] pending clearance for [[Member]] A at the time Pair-Off process begins.
• Through [[GSD]]’s systemic Pair-Off process, the system pairs off the Same-Day Settling Obligation with the Netted Obligation resulting in a money difference 
debit of $62,125.50. 
• The money difference debit is included in [[Member]]’s A Intraday Funds [[settlement]] cash obligation and is settled same day through the Intraday Funds-Only 
[[settlement]] process.
[[GSD]] 
(Clearance)
[[Member]] A 
3. MT548 Cleared 
Obligation (Pair)
RECEIVE ORDER
 Cancel Instructions (3)
[[GSD]] 
Clearing Bank
Pair-off Process Completes
[[GSD]] 
(Clearance)
[[GSD]] 
Clearing Bank
Clearance Instructions (1)
1. MT548 Clearance 
Instruction (Next Day) 
RECEIVE ORDER
2. MT548 Clearance 
Instruction (Same Day) 
DELIVER ORDER
Clearance Instructions (2)
4. MT548 Cleared 
Obligation (Pair)
DELIVER ORDER
Cancel Instructions (4)
[[GSD]] 
(Funds)
5. MT950 [[participant]] Net 
Summary
Pending Cash Movements
  

---

## Page 153

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 153 
 
A.A16 Failed Obligation Netted (Next Day or Same-Day) 
[[GSD]] 
(Clearance)
[[Member]] B
1b. MT548 Clearance 
Instruction
[[Member]] A
1a. MT548 Clearance 
Instruction
Clearance Instructions
[[GSD]] Clearing Bank
[[GSD]]  
(Clearance)
[[Member]] B
[[Member]] A 
2b. Cleared Obligation 
(Netted)
2a. Cleared Obligation 
(Netted)
Clearance Results
[[GSD]] 
(Risk)
Failed [[obligations]]
  

---

## Page 154

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 154 
 
A.A17 Held Fail (Next Day or Same-Day) *UPDATED 
[[GSD]] 
(Clearance)
[[Member]] B
1b. MT548 Clearance 
Instruction 
[[Member]] A
1a. MT548 Clearance 
Instruction
Clearance Instructions
[[GSD]] Clearing Bank
Funds
[[securities]]
[[GSD]]  
(Clearance)
[[Member]] B
[[Member]] A 
Clearance Results
2b. MT548 Clearance 
Instruction Cancel (1b)
2a. MT548 Cleared 
Obligation (Cleared 1a)
2c. MT548 Clearance 
Obligation (Held Fail 1b)
Note: Due to new [[GSD]] [[settlement]] enhancements, any obligation that is to be held from the net, will be canceled and regenerated. The new MT548 Clearance 
Instruction message sent to the [[Member]] will have the Held Fail [[settlement]] indicator (HFOB) and a new Obligation [[ID]]. 
Assumption
• [[Member]] A delivers [[securities]] to [[GSD]] late in the day. [[GSD]] 
is unable to deliver to [[Member]] B.
• [[Member]] B’s obligation will be held from the net and 
delivered on the following business day. 
  

---

## Page 155

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 155 
 
A.A18 [[Broker]] Fail 
[[GSD]] Clearing Bank
[[GSD]]  
(Clearance)
[[Member]] B
[[Member]] A 
2b. MT548 Clearance 
Instruction ([[Broker]] Fail)
1a. MT548 Clearance 
Instruction ([[Broker]] Fail)
[[Broker]] Fails
[[GSD]] 
(Risk)
Failed [[obligations]]
2b. Cleared Obligation 
(Netted)
2a. Cleared Obligation 
(Netted)
  

---

## Page 156

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 156 
 
A.A19 Partial [[settlement]] (Intra-Day – Two Deliveries) for Next Day Settling [[obligations]] 
[[GSD]] 
(Clearance)*
[[Member]] B
1b. MT548 Clearance 
Instruction (Next Day)
[[Member]] A
1a. MT548 Clearance 
Instruction (Next Day)
Clearance Instructions
[[GSD]] Clearing Bank
[[GSD]] 
(Clearance)
[[Member]] B
[[Member]] A 
 Clearance Instructions
[[GSD]] Clearing Bank
3b. MT548 Clearance 
Instruction
3a. MT548 Clearance 
Instruction
3d. MT548 Clearance 
Instruction
3c. MT548 Clearance 
Instruction
Funds (3a) Funds (3b)
[[securities]] (3a) [[securities]] (3b)
[[GSD]] 
(Clearance)
[[Member]] B
[[Member]] A 
4b. MT548 Cleared 
Obligation (Cleared 3b)
4a. MT548 Cleared 
Obligation (Cleared 3a)
Clearance Results
4d. MT548 Cleared 
Obligation (Cleared 3d)
4c. MT548 Cleared 
Obligation (Cleared 3c)
Funds (3c) Funds (3d)
[[securities]] (3c) [[securities]] (3d)
Assumption: 
• [[Member]] A & B agreed to a partial (two deliveries)
• [[Member]] A's deliveries were bound to [[Member]] B's receives 
• [[Member]] A made two (2) deliveries to [[GSD]]
• [[Member]] B received two (2) deliveries from [[GSD]]
Note: The initiation of intraday partials will NOT generate MT548 Clearance Instruction / Cancel messages that will be sent to Members. Items 2a-3d in this flow 
are displayed only for reference purposes. However, as each partial item clears, a new MT548 Cleared Obligation Message will be generated.
Clearance Instruction 
Cancels
2b. MT548 Clearance 
Instruction Cancel 
(Next Day 1b)
2a. MT548 Clearance 
Instruction Cancel 
(Next Day 1a)
  

---

## Page 157

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 157 
 
A.A20 Partial [[settlement]] (Fail Portion Netted) for Next Day Settling [[obligations]] 
[[GSD]] 
(Clearance)*
[[Member]] B
1b. MT548 Clearance 
Instruction (Next Day)
[[Member]] A
1a. MT548 Clearance 
Instruction (Next Day)
Clearance Instructions
[[GSD]] Clearing Bank
[[GSD]] 
(Clearance)
[[Member]] B
[[Member]] A 
 Clearance Instructions
[[GSD]] Clearing Bank
3b. MT548 Clearance 
Instruction
3a. MT548 Clearance 
Instruction
3d. MT548 Clearance 
Instruction
3c. MT548 Clearance 
Instruction
Funds (3a) Funds (3b)
[[securities]] (3a) [[securities]] (3b)
[[GSD]] 
(Clearance)
[[Member]] B
[[Member]] A 
4b. MT548 Cleared 
Obligation (Cleared 3b)
4a. MT548 Cleared 
Obligation (Cleared 3a)
Clearance Results
5b. MT548 Cleared 
Obligation (Netted 3d)
5a. MT548 Cleared 
Obligation (Netted 3c)
Note: The initiation of intraday partials will NOT generate MT548 Clearance Instruction / Cancel messages that will be sent to Members. Items 2a-3d in this flow 
are displayed only for reference purposes. However, as each partial item clears, a new MT548 Cleared Obligation Message will be generated.
Clearance Instruction 
Cancels
2b. MT548 Clearance 
Instruction Cancel 
(Next Day 1b)
2a. MT548 Clearance 
Instruction Cancel 
(Next Day 1a)
Assumption: 
• [[Member]] A & B agreed to a partial (two deliveries)
• [[Member]] A's deliveries were bound to [[Member]] B's receives 
• [[Member]] A failed to deliver one (1) of the two (2) partial deliveries to [[GSD]]
• [[Member]] B failed to receive one (1) of the two (2) partial deliveries from [[GSD]]
• [[Member]] A & B’s remaining fail [[obligations]] will go into the net.
[[GSD]] 
(Risk)
Failed [[obligations]]
  

---

## Page 158

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 158 
 
A.A21 Repo Substitution [[settlement]] Instruction (New [[collateral]] Provided at the Time of Initial 
Substitution) * 
[[Member]] A
 [[Member]] B
2b. MT518 Notification of 
Repo Substitution Details
2a. MT518 Notification of 
Repo Substitution Details
3b. MT509 Repo 
Substitution Processed
3a. MT509 Repo 
Substitution Processed
1. Repo Sub Request 
entered (via RTTM)
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B4b. MT509 Trade 
Bound to Net
4a. MT509 Trade 
Bound to Net
Substitution Details
[[GSD]] 
(Clearance)
[[Member]] B
5b. MT548 Clearance 
Instruction (Deliver Old 
[[collateral]])
[[Member]] A
5a. MT548 Clearance 
Instruction (Receive Old 
[[collateral]])
Clearance Instructions
[[GSD]] Clearing Bank
6b. MT548 Clearance 
Instruction (Receive New 
[[collateral]])
6a. MT548 Clearance 
Instruction (Deliver New 
[[collateral]])
[[GSD]]  
(Clearance)
[[Member]] B
[[Member]] A 
7b. MT548 Cleared 
Obligation (Delivered Old 
[[collateral]])
7a. MT548 Cleared 
Obligation (Received Old 
[[collateral]])
Clearance Results
[[securities]] (5a) [[securities]] (5b)
Funds (5a) Funds (5b)
Funds (6a) Funds (6b)
[[securities]] (6a) [[securities]] (6b)
8b. MT548 Clearance 
Instruction (Received New 
[[collateral]])
8a. MT548 Clearance 
Instruction (Delivered New 
[[collateral]])
Note: This flow assumes a [[collateral]] substitution, not a rate change nor a General [[collateral]] substitution prior to Repo Start. 
[[GSD]] 
RTTM 
(Match)
  

---

## Page 159

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 159 
 
A.A22 Repo Substitution Notification (New [[collateral]] Not Provided at the Time of Initial Substitution) * 
[[Member]] A
 [[Member]] B
2b. MT518 Notification of 
Repo Substitution Details
2a. MT518 Notification of 
Repo Substitution Details
3b. MT509 Repo 
Substitution Processed
3a. MT509 Repo 
Substitution Processed
1. Repo Sub Request 
entered (via RTTM)
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B4b. MT509 Trade 
Bound to Net
4a. MT509 Trade 
Bound to Net
Substitution Details
[[GSD]] 
(Clearance)
[[Member]] B
5b. MT548 Clearance 
Instruction (Deliver Old 
[[collateral]])
[[Member]] A
5a. MT548 Clearance 
Instruction (Receive Old 
[[collateral]])
Clearance Instructions
[[GSD]] Clearing Bank
[[GSD]]  
(Clearance)
[[Member]] B
[[Member]] A 
6b. MT548 Cleared 
Obligation (Delivered Old 
[[collateral]])
6a. MT548 Cleared 
Obligation (Received Old 
[[collateral]])
Clearance Results
[[securities]] (5a) [[securities]] (5b)
Funds (5a) Funds (5b)
Note: This flow assumes a [[collateral]] substitution, not a rate change nor a General [[collateral]] substitution prior to Repo Start. 
[[GSD]] 
RTTM 
(Match)
  

---

## Page 160

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 160 
 
A.A23 Repo Substitution Allocation (New [[collateral]] Provided After Initial Substitution Notification) * 
[[Member]] A
 [[Member]] B
2b. MT518 Notification of 
Repo Substitution Details
2a. MT518 Notification of 
Repo Substitution Details
3b. MT509 Repo 
Substitution Processed
3a. MT509 Repo 
Substitution Processed
1. Repo Sub Request 
entered (via RTTM)
[[GSD]] 
(Risk)
[[Member]] A
 [[Member]] B4b. MT509 Trade 
Bound to Net
4a. MT509 Trade 
Bound to Net
Substitution Details
[[GSD]] 
(Clearance)
[[Member]] B
[[Member]] A
Clearance Instructions
[[GSD]] Clearing Bank
[[GSD]]  
(Clearance)
[[Member]] B
[[Member]] A 
Clearance Results
Note: This flow assumes a [[collateral]] substitution, not a rate change nor a General [[collateral]] substitution prior to Repo Start. 
[[GSD]] 
RTTM 
(Match)
5b. MT548 Clearance 
Instruction (Receive New 
[[collateral]])
5a. MT548 Clearance 
Instruction (Deliver New 
[[collateral]])
Funds (5a) Funds (5b)
[[securities]] (5a) [[securities]] (5b)
6b. MT548 Clearance 
Instruction (Received New 
[[collateral]])
6a. MT548 Clearance 
Instruction (Delivered New 
[[collateral]])
  

---

## Page 161

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 161 
 
A.A24 Repo Substitution [[settlement]] Instruction ([[collateral]] Substituted Prior to Forward Settling Start 
Leg) * 
9b. MT518 Notification of 
Repo Substitution Details
9a. MT518 Notification of 
Repo Substitution Details
8. Repo Sub Request 
entered (via RTTM)
[[GSD]] 
(Risk)
[[GSD]] 
RTTM 
(Match)
A1
[[GSD]] 
(Risk)
6b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
[[Member]] A
 [[Member]] B
Comparison Results
7b. MT590 Per Trade 
Forward [[Margin]] *
7a. MT590 Per Trade 
Forward [[Margin]] *
10a. MT509 Repo 
Substitution Processed
10b. MT509 Repo 
Substitution Processed
[[Member]] A
 [[Member]] B
12b. MT590 Per Trade 
Forward [[Margin]] *
12a. MT590 Per Trade 
Forward [[Margin]] *
13b. MT509 
Start Leg In Net
13a. MT509 
Start Leg In Net
11b. MT509 Trade 
Bound to Net
11a. MT509 Trade 
Bound to Net
* Message sent during nightly processing when [[GSD]] marks the trade to market.
Substitution Details
  

---

## Page 162

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 162 
 
A.A25 Fail Coupon Payment and Subsequent Clearance 
[[Member]] A
 Repo [[Broker]]
 [[Member]] B
[[GSD]] 
(Match)
[[GSD]] 
(Funds)
[[GSD]] 
(Clearance)
[[GSD]] 
(Risk)
Comparison Results
TradesTrades
Trades
Netting Position 
Results
[[Member]] B
[[Member]] A
 [[GSD]] Clearing Bank
[[Member]] B
[[Member]] A 
Clearance Results
1b. MT548 Clearance 
Instruction (Next Day)
1a. MT548 Clearance 
Instruction (Next Day)
3b. MT548 Cleared 
Obligation (Netted)
Clearance Instructions
[[GSD]] 
(Risk)
Failed [[obligations]]
[[Member]] A 
[[Member]] B
Pending Cash 
Movements
2b. MT590 Fail 
Coupon Payment
[[GSD]]  
(Clearance)
3a. MT548 Cleared 
Obligation (Netted)
2a. MT590 Fail 
Coupon Payment
Assumption
• Next Day Settling Trade(s) submitted for Bilateral Comparison
• A = Dealer who is the Deliverer of [[securities]] to [[GSD]]
• B = Dealer who is the Receiver of [[securities]] from [[GSD]]
• Repo [[Broker]] has no Netted [[obligations]] due to flat position 
• [[Member]] A's delivery is bound to [[Member]] B's receive at [[GSD]]’s 
Clearing Bank
  

---

## Page 163

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 163 
 
A.A26 Fail Maturity Payment 
[[Member]] A
 Repo [[Broker]]
 [[Member]] B
[[GSD]] 
(Match)
[[GSD]] 
(Funds)
[[GSD]] 
(Risk)
Comparison Results
TradesTrades
Trades
Netting Position 
Results
[[Member]] B
[[Member]] A 
3b. MT548 Cleared 
Obligation (Matured)
[[Member]] A 
 [[Member]] B
Pending Cash 
Movements
1b. MT590 Fail 
Coupon Payment
[[GSD]]  
(Clearance)
3a. MT548 Cleared 
Obligation (Matured)
1a. MT590 Fail 
Coupon Payment
Assumption
• Next Day Settling Trade(s) submitted for Bilateral Comparison
• A = Dealer who is the Deliverer of [[securities]] to [[GSD]]
• B = Dealer who is the Receiver of [[securities]] from [[GSD]] 
• Repo [[Broker]] has no Netted [[obligations]] due to flat position
• [[Member]] A's delivery is bound to [[Member]] B's receive at [[GSD]]’s 
Clearing Bank
2b. MT590 Fail 
Maturity Payment
2a. MT590 Fail 
Maturity Payment
  

---

## Page 164

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 164 
 
A.A27 Repo Coupon Payment (Term Repo Submitted After Start Leg [[settlement]] Date) * 
[[GSD]] 
(Risk)
A1
[[Member]] A
 [[Member]] B
7b. MT590 Per Trade 
Forward [[Margin]] *
7a. MT590 Per Trade 
Forward [[Margin]] *
5b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
Comparison Results
[[GSD]] 
(Funds)
[[Member]] A
 [[Member]] B8b. MT590 Repo Coupon 
Payment **
8a. MT590 Repo Coupon 
Payment **
Pending Cash Movements
  

---

## Page 165

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 165 
 
A.A28 Repo to Maturity (Forward Settling Repo Start Leg) * 
[[GSD]] 
(Risk)
A1
[[Member]] A
 [[Member]] B
7b. MT590 Per Trade 
Forward [[Margin]] *
7a. MT590 Per Trade 
Forward [[Margin]] *
8b. MT509 
Start Leg In Net
8a. MT509 
Start Leg In Net
5b. MT509 Trade 
Bound to Net
6a. MT509 Trade 
Bound to Net
Comparison Results
[[GSD]] 
(Funds)
[[Member]] A
 [[Member]] B
10b. MT590 Repo Coupon 
Payment **
10a. MT590 Repo Coupon 
Payment **
9b. MT590 Repo Maturity 
Payment **
9a. MT590 Pero Maturity 
Payment **
 * Message sent during nightly processing when [[GSD]] marks the trade to market.
** Message generated on the night of Maturity / Payable Date -1.   

---

## Page 166

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 166 
 
Supplementary Flows 
A.B1  Bilateral Same-Day Settling Trade – Compared, then Canceled Pre-[[settlement]] 
[[GSD]] 
(Match) 
[[Member]] A
 [[Member]] B
[[Member]] A
 [[Member]] B
2b. MT518 Cancel 
Requested
2a. MT509 Cancel 
Accepted
1. MT515 Trade Cancel 3. MT515 Trade Cancel
5a. MT509 Trade 
Cancelled
5b. MT509 Trade 
Cancelled
4b. MT518 Cancel 
Requested
4a. MT509 Cancel 
Accepted
[[GSD]]
(Clearance)
[[Member]] B
6b. MT548 Clearance 
Instruction Cancel 
( Same-Day)
[[Member]] A 
6a. MT548 Clearance 
Instruction Cancel 
( Same-Day)
Clearance Instruction 
Cancels
Assumption
• Repo Trade is an overnight trade
• Same-Day Settling [[obligations]] have been generated for [[Member]] 
A & [[Member]] B on their compared Same-Day Starting Repo 
Transactions
• [[Member]] A = Repo Dealer & [[Member]] B = Reverse Dealer
• [[Member]] A submits a cancel & B submits a matching cancel 
• [[Member]] A & B’s Same-Day Settling [[obligations]] are pending 
clearance at time the cancel is processed 
 
[[GSD]] 
Clearing Bank 
Clearance Instruction 
Cancel Results
  

---

## Page 167

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 167 
 
A.B2  Bilateral Same-Day Settling Trade – Compared then Canceled Post Start Leg [[settlement]]  
[[GSD]] 
(Match)
[[Member]] A
 [[Member]] B
5b. MT518 Cancel 
Requested
2b. MT518 Cancel 
Requested
2a. MT509 Cancel 
Accepted
Assumption
• Repo Trade is an overnight trade
• Same-Day Settling [[obligations]] have been generated for [[Member]] 
A & [[Member]] B on their compared Same-Day Starting Repo 
Transactions
• [[Member]] A = Repo Dealer & [[Member]] B = Reverse Dealer
• [[Member]] B submits a cancel action on its trade vs. [[Member]] A
• [[Member]] A Delivers the [[securities]] to [[GSD]]
• [[Member]] B Receives the [[securities]] from [[GSD]]
• [[Member]] A & B’s Same-Day Settling [[obligations]] have cleared 
prior to the processing of the trade cancellation 
• [[Member]] A then submits a matching cancel
 
5a. MT509 Cancel 
Accepted
Funds (3a) Funds (3b)
[[securities]] (3a) [[securities]] (3b)
*Flow is continued on next page
[[GSD]] 
(Clearance)
[[Member]] B
[[Member]] A
Clearance Results
[[GSD]] 
Clearing Bank 
3b. MT548 Cleared 
Obligation (Cleared)
3a. MT548 Cleared 
Obligation (Cleared)
[[Member]] A
 [[Member]] B6a. MT509 Trade 
Cancelled
6b. MT509 Trade 
Cancelled
Clearance Instruction 
Cancel Results*
1. MT515 Trade Cancel4. MT515 Trade Cancel
  

---

## Page 168

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 168 
 
A.B2  Bilateral Same-Day Settling Trade – Compared then Canceled Post Start Leg [[settlement]] (Cont.) 
[[GSD]] 
(Clearance)
[[Member]] B
7b. MT548 Clearance 
Instruction (Same-Day)
[[Member]] A 
7a. MT548 Clearance 
Instruction (Same-Day)
Reverse Clearance 
Instructions
[[securities]] (7a)
Funds (7a) Funds (7b)
[[GSD]]  
(Clearance)
[[Member]] B
[[Member]] A
8b. MT548 Cleared 
Obligation (Cleared 7b)
8a. MT548 Cleared 
Obligation (Cleared 7a)
[[GSD]] 
Clearing Bank 
Reverse Clearance Results
Clearance Instruction 
Cancel Results
Assumption
• For  Same-Day Settling [[obligations]] that have cleared prior to or at the time the underlying repo trades are cancelled, the system will generate reverse 
[[obligations]] for the affected Dealer counterparties. 
• [[Member]] B would have a new obligation to deliver to [[GSD]] and [[Member]] A would have a new obligation to receive from [[GSD]]. 
  

---

## Page 169

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 169 
 
A.B3   Brokered (Balanced) Same-Day Settling Trade – Canceled Pre-[[settlement]] 
Repo [[Broker]] 
1. MT515 Trade Cancel 
(Reverse)
3. MT515 Trade Cancel 
(Repo)
2a. MT509 Cancel 
Accepted
4a. MT509 Cancel 
Accepted
[[Member]] A
[[Member]] B
Assumption
• [[Member]] A & [[Member]] B [[DO]] not submit matching trade details against the Brokered Same-Day Starting Repo Demand Trades submitted by the Repo [[Broker]] 
• [[Member]] A = Repo Dealer & [[Member]] B = Reverse Dealer, Repo [[Broker]]  = Reverse Side to [[Member]] A and Repo Side to [[Member]] B
• Same-Day Settling [[obligations]] have been generated for [[Member]] A & B based on the Repo [[Broker]] ’s trade submissions
• Repo [[Broker]]  has no [[obligations]] due to flat position
• Repo [[Broker]]  submits cancels for both the Same-Day Starting Repo & Reverse Repo Demand Trades
• The Same-Day Starting Repo & Reverse Repo Demand Trades are unilaterally cancelled during the Demand Period
• [[Member]] A & B’s Same-Day Settling [[obligations]] are pending clearance at the time the trades are cancelled
2b. MT518 Comparison  
Request Cancel
4b. MT518 Comparison 
Request Cancel
Repo [[Broker]] 
5a. MT509 Trade 
Cancelled
[[GSD]]
(Clearance)
[[Member]] B
6b. MT548 Clearance 
Instruction Cancel 
( Same-Day)
[[Member]] A 
6a. MT548 Clearance 
Instruction Cancel 
( Same-Day)
Clearance Instruction 
Cancels
[[GSD]] 
Clearing Bank 
Clearance Instruction 
Cancel Results
5b. MT509 Trade 
Cancelled
[[GSD]] 
(Match)
Note: For any Brokered (Balanced) Same-Day Starting Repo Demand Trade that is cancelled during the demand period, its’ corresponding Same-Day Settling 
Obligation will be cancelled. If only one side of a “balanced set” is cancelled, the remaining Same-Day Starting Repo transaction within the “balanced set” will be 
unbalanced until either 1) the remaining Same-Day Starting Repo transaction that was a part of the “balanced set” is cancelled or 2) a new Brokered Same-Day 
Starting Repo Demand trade is submitted with the balancing criteria to re-establish the “balanced set” in order to replace the cancelled demand trade.   

---

## Page 170

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 170 
 
A.B4   Brokered (Balanced) Same-Day Settling Trade – Canceled Post Start Leg [[settlement]] 
Repo [[Broker]] 
1. MT515 Trade Cancel 
(Reverse)
3. MT515 Trade Cancel 
(Repo)
2a. MT509 Cancel 
Accepted
4a. MT509 Cancel 
Accepted
[[Member]] A
[[Member]] B
Assumption
• [[Member]] A & [[Member]] B [[DO]] not submit matching trade details against the Brokered Same-Day Starting Repo Demand Trades submitted by the Repo [[Broker]] 
• [[Member]] A = Repo Dealer & [[Member]] B = Reverse Dealer, Repo [[Broker]]  = Reverse Side to [[Member]] A and Repo Side to [[Member]] B
• Same-Day Settling [[obligations]] have been generated for [[Member]] A & B based on the Repo [[Broker]] ’s trade submissions
• Repo [[Broker]]  has no [[obligations]] due to flat position
• Repo [[Broker]]  submits cancels for both the Same-Day Starting Repo & Reverse Repo Demand Trades
• The Same-Day Starting Repo & Reverse Repo Demand Trades are unilaterally cancelled during the Demand Period
• [[Member]] A & B’s Same-Day Settling [[obligations]] have cleared at the same time the trades are cancelled
[[GSD]] 
(Match)
2b. MT518 Comparison  
Request Cancel
4b. MT518 Comparison 
Request Cancel
Repo [[Broker]] 
6a. MT509 Trade 
Cancelled
[[GSD]]
(Clearance)
[[Member]] B
5b. MT548 Cleared 
Obligation (Cleared)
[[Member]] A
5a. MT548 Cleared 
Obligation (Cleared)
[[GSD]] 
Clearing Bank 
Clearance Results
Funds (5a) Funds (5b)
[[securities]] (5a) [[securities]] (5b)
*Flow is continued on next page
Clearance Instruction 
Cancel Results*
6b. MT509 Trade 
Cancelled
  

---

## Page 171

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 171 
 
A.B4   Brokered (Balanced) Same-Day Settling Trade – Canceled Post Start Leg [[settlement]] (Cont.) 
[[GSD]]
 (Clearance)
[[Member]] B
7b. MT548 Clearance 
Instruction (Same-Day)
[[Member]] A 
7a. MT548 Clearance 
Instruction (Same-Day)
Reverse Clearance 
Instructions
[[securities]] (7a)
Funds (7a)
[[securities]] (7b)
[[GSD]] 
(Clearance)
[[Member]] B
[[Member]] A
8b. MT548 Cleared 
Obligation (Cleared 7b)
8a. MT548 Cleared 
Obligation (Cleared 7a)
[[GSD]] 
Clearing Bank 
Clearance Instruction 
Cancel Results
Reverse Clearance Results
Assumption
• For  Same-Day Settling [[obligations]] that have cleared prior to or at the time the underlying repo trades are cancelled, the system will generate reverse 
[[obligations]] for the affected Dealer counterparties. 
• [[Member]] B would have a new obligation to deliver to [[GSD]] and [[Member]] A would have a new obligation to receive from [[GSD]].  
  

---

## Page 172

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 172 
 
A.B5   Brokered (Unbalanced) Same-Day Settling Trade – Canceled Pre-[[settlement]]   
Repo [[Broker]] 
2a. MT509 Trade 
Accepted
[[Member]] A
2b. MT518 Comparison 
Requested
Assumption
• Repo [[Broker]]  submits a Same-Day Starting Reverse Repo trade against [[Member]] A during the Demand Period
• Repo [[Broker]]  does not submit a Demand Repo trade with balancing criteria against another [[Member]], to offset the Reverse Repo submitted against [[Member]] A 
• [[Member]] A does not submit matching trade details.
• Since it is during the Demand Period, no [[obligations]] have been generated to settle the start leg of the Same-Day Starting Reverse Repo trade because the 
Brokered Repo is unbalanced in the system. 
• Repo [[Broker]]  submits a cancel on the Same-Day Starting Reverse Repo trade 
• The Same-Day Starting Reverse Repo Trade is unilaterally cancelled during the Demand Period
Repo [[Broker]] 
3. MT515 Trade Cancel 
(Reverse)
4a. MT509 Cancel 
Accepted
1. MT515 Trade 
Submission (Reverse)
[[GSD]]  
(Match)
4b. MT518 Comparison  
Request Cancel
4c. MT509 Trade 
Cancelled
  

---

## Page 173

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 173 
 
A.B6 Brokered (Balanced) Same-Day Settling Trade – Contra Dealer DKs/[[Broker]] Cancels Pre-
[[settlement]]  
Repo [[Broker]]
2b. MT518 DK Advice
5b. MT509 Trade 
Canceled (Reverse)
[[Member]] A
[[Member]] B
7b. MT518 Comparison 
Request Cancel
[[GSD]] 
(Clearance)
[[Member]] B
8. MT548 Clearance Cancel 
(Same Day)
[[Member]] A 
3. MT548 Clearance Cancel 
(Same Day)
Clearance Instruction 
Cancels
[[GSD]] 
Clearing Bank
2a. MT509 DK Accepted
5a. MT509 Cancel 
Accepted
7a. MT509 Cancel 
Accepted
1. MT515 Trade DK
2c. MT518 Comparison  
Request Cancel 
(due to DK)
[[GSD]] 
(Match)
2d. MT509 DK Processed
7c. MT509 Trade 
Canceled (Repo)
Assumption
• Repo [[Broker]] submits Demand overnight Repo transaction against [[Member]] B & a Reverse transaction against [[Member]] A
• [[Member]] A & [[Member]] B [[DO]] not submit matching trade details against the Brokered Same-Day Starting Repo Demand Trades
• [[Member]] A = Repo Dealer & [[Member]] B = Reverse Dealer, Repo [[Broker]] = Reverse Side to [[Member]] A and Repo Side to [[Member]] B
• Same-Day Settling [[obligations]] have been generated for [[Member]] A & B based on the submission of the Brokered Same-Day Starting Repo Demand Trades
• Repo [[Broker]] has no [[obligations]] due to flat position
• [[Member]] A submits DK against the Repo [[Broker]] submitted Demand Trade
• Repo [[Broker]] submits cancels for both the Same-Day Starting Repo & Reverse Repo Demand Trades
• The Same-Day Starting Repo & Reverse Repo Demand Trades are cancelled
• [[Member]] A & B’s Same-Day Settling [[obligations]] are pending clearance at the time the trades are cancelled so the [[obligations]] are cancelled from the bank
6. MT515 Trade Cancel 
(Repo)
Clearance Instruction 
Cancel Results
4. MT515 Trade Cancel 
(Reverse)
Note: For any Brokered (Balanced) Same-Day Starting Repo Demand Trade that is cancelled during the demand period, its’ corresponding Same-Day Settling 
Obligation will be cancelled. If only one side of a “balanced set” is cancelled, the remaining Same-Day Starting Repo transaction within the “balanced set” will be 
unbalanced until either 1) the remaining Same-Day Starting Repo transaction that was a part of the “balanced set” is cancelled or 2) a new Brokered Same-Day 
Starting Repo Demand trade is submitted with the balancing criteria to re-establish the “balanced set” in order to replace the cancelled demand trade.   

---

## Page 174

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 174 
 
A.B7 Bilateral Overnight As-of Repo Transaction – Uncompared (Day 1), Matched As-of trade by 
Contra (Day 2) 
[[GSD]]  
(Match)
[[Member]] A
 [[Member]] B
2b. MT518 Comparison 
Requested
2a. MT509 Trade 
Accepted
1. MT515 Trade 
Submission
Day 2
Day 1
Assumption
• On Day 1, [[Member]] A submits an overnight Same-Day Starting Repo transaction against [[Member]] B for bilateral comparison. 
• The Repo trade starts today and closes tomorrow.  
• [[Member]] B does not submit trade details to compare against [[Member]] A’s trade on Day 1. 
• [[Member]] A’s trade is uncompared at end of day on Day 1. [[obligations]] are not generated.
Assumption
• On Day 2, [[Member]] B submits a Reverse Repo transaction against [[Member]] A for bilateral comparison.  
• [[Member]] B’s trade details match against the trade [[Member]] A’s submitted on Day 1. 
• Both trades are compared. At the time of match, [[obligations]] are generated. 
• [[GSD]] will generate [[obligations]] for [[Member]] A & [[Member]] B to settle the start leg and end leg because the trade is considered an “As-of” Same-Day Starting 
Repo Transaction. 
[[GSD]] 
(Risk)
5a. MT509 Trade 
Comparison Only
6c. MT518 Comparison 
Request Cancel (due to match)
[[Member]] A
3. MT515 Trade 
Submission
5b. MT509 Trade 
Comparison Only
[[GSD]]  
(Match)
[[GSD]] 
(Clearance)*
*Flow is continued on next page
Comparison Results
[[Member]] B
6d. MT518 Comparison 
Request Cancel (due to match)
4a. MT509 Trade 
Accepted
4b. MT518 Comparison 
Requested
6a. MT509 Trade 
Compared
6b. MT509 Trade 
Compared
  

---

## Page 175

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 175 
 
A.B7 Bilateral Overnight As-of Repo Transaction – Uncompared (Day 1), Matched As-of trade by 
Contra (Day 2) (Cont.) 
[[GSD]] 
(Clearance)
[[Member]] B
7b. MT548 Clearance 
Instruction (Same Day) / 
Start Leg
[[Member]] A
7a. MT548 Clearance 
Instruction (Same Day) /  
Start Leg
Clearance Instructions
[[GSD]] 
Clearing Bank
Funds (7a) Funds (7b)
[[securities]] (7a) [[securities]] (7b)
Clearance Results
Note: If a compared & eligible “As-of” Same-Day Starting Repo transaction is a term trade, where the End Leg [[settlement]] Date is at least one (1) business date 
greater than the current business date, the End Leg on such transaction will settle through [[GSD]]’s normal processing (BAU). 
Also note that [[GSD]] will provide its clearing services for the start leg and end leg of other “As-of” repo trades that are submitted, compared and have 1) a trade 
date & start date = to the previous business date or 2) a trade date = to previous business date & start date = to current business date. This applies to both 
Demand and Bilateral repo transactions that fit the above criteria. 
Assumption
• The [[settlement]] amount for the Same-Day Settling Obligation created to settle the Start Leg will be equal to the contract value on the trade. 
• The [[settlement]] amount for the Same-Day Settling Obligation created to settle the End Leg will be equal to the final money calculated on the trade. 
• [[Member]] A = Repo Dealer who is the Deliverer of [[securities]] to [[GSD]] for the obligation created to settle the Start Leg 
• [[Member]] B = Reverse Dealer who is the Receiver of [[securities]] from [[GSD]] for the obligation created to settle the Start Leg 
• [[Member]] A's delivery is bound to [[Member]] B's receive at [[GSD]]’s Clearing Bank. 
• [[Member]] A = Repo Dealer who is the Receiver of [[securities]] from [[GSD]] for the obligation created to settle the End Leg 
• [[Member]] B = Reverse Dealer who is the Deliverer of [[securities]] to [[GSD]] for the obligation created to settle the End Leg 
• [[Member]] A's receive is bound to [[Member]] B's delivery at [[GSD]]’s Clearing Bank.
8b. MT548 Clearance 
Instruction (Same Day) / 
End Leg
8a. MT548 Clearance 
Instruction (Same Day) / 
End Leg
[[securities]] (8a) [[securities]] (8b)
Funds (8a) Funds (8b)
[[GSD]]  
(Clearance)
[[Member]] B
[[Member]] A 
9b. MT548 Cleared 
Obligation (Cleared 7b)
9a. MT548 Cleared 
Obligation (Cleared 7a)
10b. MT548 Cleared 
Obligation (Cleared 8b)
10a. MT548 Cleared 
Obligation (Cleared 8a)
  

---

## Page 176

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 176 
 
Appendix B – Message Samples 
 
This appendix of Message Samples provides examples of a variety of messages that may be generated for 
Buy/Sell and Repo Transactions. It should be noted that the message samples contained in this appendix are 
not necessarily intended to represent the actual flow of events that would generate messages Members would 
receive, but rather individual samples to help Members become familiar with the message structure. The 
introductory text for each scenario is intended to clarify how the different message samples were populated. 
The following also should be noted: 
1. The scenarios provided in this appendix will include [[GSD]] comparison interactive message samples as 
well as netting and [[settlement]] status related messages, where applicable. An asterisk (*) will be used to 
mark [[GSD]] comparison interactive message samples in the upcoming pages. 
2. Most comparison and netting related message samples displayed in this document are based on SWIFT 
15022 Standard Formats. The exception would be for the MT950 and MT590 message samples which are 
based on the older SWIFT Format, ISO 7775. 
3. The netting and [[settlement]] status related message samples in this document are generated out of the 
Netting System but are not solely based on [[GSD]] netting output. 
4. The term “Same-Day Settling Obligation” for the purpose of this document means a [[securities]] [[settlement]] 
Obligation created to settle a Same-Day Settling Trade pursuant to Rule 12 of the [[FICC]] [[GSD]] Rulebook. 
5. The term “Netted Obligation” for the purpose of this document means a [[securities]] [[settlement]] Obligation 
calculated for the [[settlement]] of Net [[settlement]] Positions pursuant to Rule 12 of [[FICC]] [[GSD]] Rulebook. 
6. Whether the MT548 Clearance Instruction message is for same-day or next day [[settlement]], the 
[[settlement]] Indicator is the same. Both will have the [[settlement]] Indicator “:22F::SETR/GSCC/NETX.” 
 
  

---

## Page 177

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 177 
 
Listed below are the sample scenarios depicted in this appendix: 
B1 – Comparison, Netting and [[settlement]] Messages Resulting from a Next Day Settling Buy/Sell Transaction  
B2 – Comparison, Netting and [[settlement]] Messages Resulting from a Next Day Starting Repo Transaction 
B3 – Comparison, Netting and [[settlement]] Messages Resulting from a Same-Day Starting Repo Transaction  
B4 – Comparison, Netting and [[settlement]] Messages Resulting from a Same-Day Starting Repo Transaction 
Cancelled/Removed from Net Post Comparison 
B5 – Comparison, Netting and [[settlement]] Messages Resulting from a Same-Day Starting Repo Transaction 
Cancelled/Removed from Net Post Comparison 
B6 – Demand Comparison, Netting and [[settlement]] Messages Resulting from a Same-Day Starting Repo 
Transaction  
B7 – [[settlement]] Messages Resulting from an Intraday Partial [[settlement]] 
B8 – [[settlement]] and Funds [[settlement]] Messages Resulting from the Pair-off of a Same-Day Settling 
Obligation and a Netted Obligation 
 
Note: 
Where we have included new fields or have amended already existing fields within the messages, such updates have been 
indicated and highlighted in yellow and italics in this appendix. 
 
  

---

## Page 178

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 178 
 
Sample # B1 – Comparison, Netting and [[settlement]] Messages Resulting from a Next Day 
Settling Buy/Sell Transaction  
On June 21, 2020, Dealer [[Member]] 8437 executes a next day settling buy trade for 13,500,000 of US Treasury 
Note 0.500% of 6/30/27 – [[CUSIP]] 912828ZV5 with Dealer [[Member]] 8905 for [[settlement]] on June 22, 2020, at a 
price of 100.25. The final money ([[settlement]] amount) is $13,537,968.75. The next day settling buy/sell 
transaction is submitted to [[GSD]] for comparison and [[settlement]] by both Dealer Members 8437 and 8905, 
respectively.   
[[Member]] Reference Numbers 8437 8905 
Message Reference 001324592671 000007390022 
External Reference WLR50025609 GDEX00022695 
New External Reference N/A N/A 
[[Broker]] Reference N/A N/A 
[[GSD]] Assigned Reference (TID) 000E4D-0621 000E57-0621 
Secondary Reference N/A N/A 
[[GSD]] Assigned Reference (OID) 700547-0621 700548-0621 
 
The message samples presented on the following pages are all based on the above scenario.  
For the purposes of this example, we assume the following:  
1. The trade executed by the above reference Members in [[CUSIP]] 912828ZV5 was the only trade executed 
submitted and compared where the [[settlement]] date is on June 22, 2020. Therefore, the Par/Quantity on 
the Netted [[obligations]] for Members is equal to the Par of the underlying trades.  
2. The [[settlement]] Amount for the Netted [[obligations]] is based on the current day’s system price. 
3. The delivering party, Dealer [[Member]] 8905 will settle its deliver obligation with [[GSD]] on June 22, 2020 
enabling the [[settlement]] of the receive obligation for Dealer [[Member]] 8437. 
 
B1.a MT515 Dealer [[Member]] 8437 Submits Buy Transaction to [[GSD]]* 
B1.b MT509 Trade Accepted Record sent to Dealer [[Member]] 8437* 
B1.c MT518 Comparison Request sent to Dealer [[Member]] 8905* 
B1.d MT515 Dealer [[Member]] 8905 Submits Sell Transaction to [[GSD]]* 
B1.e MT509 Trade Accepted Record sent to Dealer [[Member]] 8905* 
B1.f. MT518 Comparison Request sent to Dealer [[Member]] 8437* 
B1.g MT509 Trade Compared Record sent to Dealer [[Member]] 8437* 
B1.h MT518 Comparison Request Cancel (due to match) sent to Dealer [[Member]] 8905* 
B1.i MT509 Trade Compared Record sent to Dealer [[Member]] 8905* 

---

## Page 179

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 179 
 
B1.j MT518 Comparison Request Cancel (due to match) sent to Dealer [[Member]] 8437* 
B1.k MT509 Trade Bound for Net sent to Dealer [[Member]] 8437 
B1.l MT509 Trade Bound for Net sent to Dealer [[Member]] 8905 
B1.m MT509 Buy/Sell Trade in Net sent to Dealer [[Member]] 8437 
B1.n MT509 Buy/Sell Trade in Net sent to Dealer [[Member]] 8905 
B1.o MT548 Clearance Instruction sent to Dealer [[Member]] 8437 
B1.p MT548 Clearance Instruction sent to Dealer [[Member]] 8905 
B1.q MT548 Cleared Obligation sent to Dealer [[Member]] 8437 
B1.r MT548 Cleared Obligation sent to Dealer [[Member]] 8905 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated.  
 
 
  

---

## Page 180

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 180 
 
Sample B1.a MT515 Dealer [[Member]] 8437 Submits Buy Transaction to [[GSD]]* 
Message Content Comments 
1KLONT [[GSD]] Assigned Unique Identifier 
8437 Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//001324592671 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200621110823 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::MAST//WLR50025609 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200621110812 Trade Date and Time 
:98A::SETT//20200622 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT//100,25  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD13537968,75 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828ZV5 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
- End of Message 

---

## Page 181

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 181 
 
 
Sample B1.b MT509 Trade Accepted Record sent to Dealer [[Member]] 8437* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809112 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621110830 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLR50025609 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//001324592671 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK  
:16R:LINK  
:20C::LIST//000E4D-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 182

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 182 
 
Sample B1.c MT518 Comparison Request sent to Dealer [[Member]] 8905* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809115 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200621110823 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200621110812 Trade Date and Time 
:98A::SETT//20200622 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT//100,25  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD13537968,75 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:20C::PROC// WLR50025609 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828ZV5 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
- End of Message 
  

---

## Page 183

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 183 
 
Sample B1.d MT515 Dealer [[Member]] 8905 Submits Sell Transaction to [[GSD]]* 
Message Content Comments 
D5GKNC [[GSD]] Assigned Unique Identifier 
8905 Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//000007390022 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200621110842 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::MAST//GDEX00022695 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200621110812 Trade Date and Time 
:98A::SETT//20200622 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT//100,25  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD13537968,75 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828ZV5 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
- End of Message 

---

## Page 184

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 184 
 
 
Sample B1.e MT509 Trade Accepted Record sent to Dealer [[Member]] 8905* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809200 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621110850 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDEX00022695 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//000007390022 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK  
:16R:LINK  
:20C::LIST//000E57-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 185

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 185 
 
Sample B1.f MT518 Comparison Request sent to Dealer [[Member]] 8437* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809211 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200621110859 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200621110812 Trade Date and Time 
:98A::SETT//20200622 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT//100,25  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD13537968,75 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:20C::PROC//GDEX00022695 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828ZV5 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
- End of Message 
  

---

## Page 186

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 186 
 
Sample B1.g MT509 Trade Compared Record sent to Dealer [[Member]] 8437* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809215 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621110905 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLR50025609 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000E4D-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16R:LINK  
:20C::PROG//GDEX00022695 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 187

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 187 
 
Sample B1.h MT518 Comparison Request Cancel sent to Dealer [[Member]] 8905* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809217 Sender’s Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200621110905 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200621110812 Trade Date and Time 
:98A::SETT//20200622 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT//100,25  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD13537968,75 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:20C::PROC//WLR50025609 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828ZV5 Identification of Financial Instrument/Security ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 188

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 188 
 
Sample B1.h MT518 Comparison Request Cancel sent to Dealer [[Member]] 8905* 
Message Content Comments 
:16S:CONFDET   
- End of Message 
  

---

## Page 189

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 189 
 
Sample B1.i MT509 Trade Compared Record sent to Dealer [[Member]] 8905* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809219 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621110905 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDEX00022695 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000E57-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16R:LINK  
:20C::PROG//WLR50025609 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 190

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 190 
 
Sample B1.j MT518 Comparison Request Cancel sent to Dealer [[Member]] 8437* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809220 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200621110905 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200621110812 Trade Date and Time 
:98A::SETT//20200622 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT//100,25  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD13537968,75 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:20C::PROC//GDEX00022695 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828ZV5 Identification of Financial Instrument/Security ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 191

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 191 
 
Sample B1.j MT518 Comparison Request Cancel sent to Dealer [[Member]] 8437* 
Message Content Comments 
:16S:CONFDET   
- End of Message 
  

---

## Page 192

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 192 
 
Sample B1.k MT509 Trade Bound to Net Record sent to Dealer [[Member]] 8437 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809222 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621110906 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLR50025609 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000E4D-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 193

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 193 
 
Sample B1.l MT509 Trade Bound to Net Record sent to Dealer [[Member]] 8905 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019809224 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621110906 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDEX00022695 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000E57-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 194

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 194 
 
Sample B1.m MT509 Buy/Sell Trade in Net Record sent to Dealer [[Member]] 8437 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019813024 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621200209 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLR50025609 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000E4D-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NECT Buy/Sell Trade in Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 195

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 195 
 
Sample B1.n MT509 Buy/Sell Trade in Net Record sent to Dealer [[Member]] 8905 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019813025 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621200209 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDEX00022695 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000E57-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NECT Buy/Sell Trade in Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 196

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 196 
 
Sample B1.o MT548 Clearance Instruction sent to Dealer [[Member]] 8437 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
95C0 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019814022 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621205206 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700547-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700547-0621 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700547-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828ZV5 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD13539540,33 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8437 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Next Day) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200622 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 197

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 197 
 
:95R::DEAG/GSCC/021000018BK OF 
NYC/GSCC 
Delivering Agent ([[Seller]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
  

---

## Page 198

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 198 
 
Sample B1.p MT548 Clearance Instruction sent to Dealer [[Member]] 8905 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019814024 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200621205206 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700548-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700548-0621 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700548-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828ZV5 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD13539540,33 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8905 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Next Day) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200622 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 199

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 199 
 
:95R::REAG/GSCC/021000018BK OF 
NYC/GSCC 
Receiving Agent ([[Buyer]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
 
  

---

## Page 200

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 200 
 
Sample B1.q MT548 Cleared Obligation sent to Dealer [[Member]] 8437 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019841024 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200622082052 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700547-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700547-0621 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700547-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828ZV5 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD13539540,33 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8437 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/CLRD Type of [[settlement]] Transaction (Cleared) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200622 [[settlement]] Date 
:70E::SPRO//GSCC Opening Par Amount and Opening [[settlement]] Amount 

---

## Page 201

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 201 
 
/OPARFAMT15000000,/OPSTUSD13539540,33 
:16S:SETTRAN   
- End of Message 
 
 
 
 
  

---

## Page 202

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 202 
 
Sample B1.r MT548 Cleared Obligation sent to Dealer [[Member]] 8905 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019841023 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200622082052 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700548-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700548-0621 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700548-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828ZV5 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/13500000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD13539540,33 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8905 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/CLRD Type of [[settlement]] Transaction (Cleared) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200622 [[settlement]] Date 
:70E::SPRO//GSCC Opening Par Amount and Opening [[settlement]] Amount 

---

## Page 203

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 203 
 
/OPARFAMT15000000,/OPSTUSD13539540,33 
:16S:SETTRAN   
- End of Message 
 
 
 
 
 
  

---

## Page 204

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 204 
 
Sample # B2 – Comparison, Netting and [[settlement]] Messages Resulting from a Next Day 
Starting Repo Transaction 
On June 21, 2020, Repo Dealer [[Member]] 8X77 executes a next-day starting repo transaction with Repo Dealer 
[[Member]] 89XA for 50,000,000 of US Treasury Note 2.000% of 11/15/21 – [[CUSIP]] 912828RR3. The Contract 
Repo Rate is 1.00%. The Start Leg [[settlement]] Date is June 22, 2020 and the End Leg [[settlement]] Date is June 
23, 2020. The Start Leg [[settlement]] Amount is $50,000,000.00 and the End Leg [[settlement]] Amount is 
$50,001,388.89. The next day starting repo transaction is submitted to [[GSD]] for comparison and [[settlement]] by 
both Repo Dealer Members 8X77 and 89XA, respectively.   
[[Member]] Reference Numbers 8X77 89XA 
Message Reference 000024560732 0000090073 
External Reference 000NE50061506 0001G2069501 
New External Reference N/A N/A 
[[Broker]] Reference N/A N/A 
[[GSD]] Assigned Reference (TID) 000D8B-0621 000D97-0621 
Secondary Reference N/A N/A 
[[GSD]] Assigned Reference (OID) 700514-0621 700515-0621 
 
The message samples presented on the following pages are all based on the above scenario.  
For the purposes of this example, we assume the following:  
1. The trade executed by the above reference Members in [[CUSIP]] 912828RR3 was the only trade executed, 
submitted and compared where the Start Leg [[settlement]] Date is June 22, 2020. Therefore, the 
Par/Quantity on the Netted [[obligations]] for Members is equal to the Par of the underlying trades.  
2. The [[settlement]] Amount for the Netted [[obligations]] is based on the current day’s system price. 
3. The delivering party, Repo Dealer [[Member]] 8X77 will settle its deliver obligation with [[GSD]] on June 22, 
2020 enabling the [[settlement]] of the receive obligation for Repo Dealer [[Member]] 89XA. 
4. The End Leg will go into the net on June 22, 2020. Note: The netting and [[settlement]] of the End Leg will 
not be covered in this scenario. 
 
B2.a MT515 Repo Dealer [[Member]] 8X77 Submits Repo Transaction to [[GSD]]* 
B2.b MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 8X77* 
B2.c MT518 Comparison Request sent to Repo Dealer [[Member]] 89XA* 
B2.d MT515 Repo Dealer [[Member]] 89XA Submits Revere Repo Transaction to [[GSD]]* 
B2.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 89XA* 
B2.f. MT518 Comparison Request sent to Repo Dealer [[Member]] 8X77* 
B2.g MT509 Trade Compared Record sent to Repo Dealer [[Member]] 8X77* 

---

## Page 205

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 205 
 
B2.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 89XA* 
B2.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 89XA* 
B2.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8X77* 
B2.k MT509 Trade Bound to Net sent to Repo Dealer [[Member]] 8X77 
B2.l MT509 Trade Bound to Net sent to Repo Dealer [[Member]] 89XA 
B2.m MT509 Start Leg in Net sent to Repo Dealer [[Member]] 8X77 
B2.n MT509 Start Leg in Net sent to Repo Dealer [[Member]] 89XA 
B2.o MT548 Clearance Instruction sent to Repo Dealer [[Member]] 8X77 
B2.p MT548 Clearance Instruction sent to Repo Dealer [[Member]] 89XA 
B2.q MT548 Cleared Obligation sent to Repo Dealer [[Member]] 8X77 
B2.r MT548 Cleared Obligation sent to Repo Dealer [[Member]] 89XA 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated.  
 
  

---

## Page 206

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 206 
 
Sample B2.a MT515 Dealer [[Member]] 8X77 Submits Repo Transaction to [[GSD]]* 
Message Content Comments 
1GSOXT [[GSD]] Assigned Unique Identifier 
8X77 Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//000024560732 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608082728 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//000NE50061506 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608082702 Trade Date and Time 
:98A::SETT//20200608 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD50000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE/SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828RR3 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  

---

## Page 207

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 207 
 
Sample B2.a MT515 Dealer [[Member]] 8X77 Submits Repo Transaction to [[GSD]]* 
Message Content Comments 
:98A::REPU//20200622 Close Leg [[settlement]] Date 
:92A::REPO//1, Repo Rate 
:19A::REPA//USD50001388,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 208

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 208 
 
Sample B2.b MT509 Trade Accepted Record sent to Dealer [[Member]] 8X77* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019807112 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608082737 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//000NE50061506 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//000024560732 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D8B-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 209

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 209 
 
Sample B2.c MT518 Comparison Request sent to Dealer [[Member]] 89XA* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019807115 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608082738 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608082702 Trade Date and Time 
:98A::SETT//20200608 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD50000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:20C::PROC//000NE50061506 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828RR3 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200622 Close Leg [[settlement]] Date 
:92A::REPO//1, Repo Rate 

---

## Page 210

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 210 
 
Sample B2.c MT518 Comparison Request sent to Dealer [[Member]] 89XA* 
Message Content Comments 
:19A::REPA//USD50001388,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 211

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 211 
 
Sample B2.d MT515 Dealer [[Member]] 89XA Submits Reverse Repo Transaction to [[GSD]]* 
Message Content Comments 
G1LKNL [[GSD]] Assigned Unique Identifier 
89XA Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//00000090073 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608082847 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//0001G2069501 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608082702 Trade Date and Time 
:98A::SETT//20200608 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD50000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE/BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828RR3 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  

---

## Page 212

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 212 
 
Sample B2.d MT515 Dealer [[Member]] 89XA Submits Reverse Repo Transaction to [[GSD]]* 
Message Content Comments 
:98A::REPU//20200622 Close Leg [[settlement]] Date 
:92A::REPO//1, Repo Rate 
:19A::REPA//USD50001388,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 213

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 213 
 
Sample B2.e MT509 Trade Accepted Record sent to Dealer [[Member]] 89XA* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019808900 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608082849 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//0001G2069501 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//00000090073 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D97-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 214

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 214 
 
Sample B2.f MT518 Comparison Request sent to Dealer [[Member]] 8X77* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019808911 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608082850 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608082702 Trade Date and Time 
:98A::SETT//20200608 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD50000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:20C::PROC//0001G2069501 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828RR3 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200622 Close Leg [[settlement]] Date 
:92A::REPO//1, Repo Rate 

---

## Page 215

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 215 
 
Sample B2.f MT518 Comparison Request sent to Dealer [[Member]] 8X77* 
Message Content Comments 
:19A::REPA//USD50001388,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 216

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 216 
 
Sample B2.g MT509 Trade Compared Record sent to Dealer [[Member]] 8X77* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019808915 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608082851 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//000NE50061506 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D8B-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16R:LINK  
:20C::PROG//0001G2069501 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 217

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 217 
 
Sample B2.h MT518 Comparison Request Cancel sent to Dealer [[Member]] 89XA* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019808917 Sender’s Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200608082851 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608082702 Trade Date and Time 
:98A::SETT//20200608 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD50000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:20C::PROC//000NE50061506 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828RR3 Identification of Financial Instrument/Security ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 218

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 218 
 
Sample B2.h MT518 Comparison Request Cancel sent to Dealer [[Member]] 89XA* 
Message Content Comments 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200622 Close Leg [[settlement]] Date 
:92A::REPO//1, Repo Rate 
:19A::REPA//USD50001388,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 219

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 219 
 
Sample B2.i MT509 Trade Compared Record sent to Dealer [[Member]] 89XA* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019808919 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608082851 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//0001G2069501 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D97-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16R:LINK  
:20C::PROG//000NE50061506 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 220

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 220 
 
Sample B2.j MT518 Comparison Request Cancel sent to Dealer [[Member]] 8X77* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019808920 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608082852 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608082702 Trade Date and Time 
:98A::SETT//20200608 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD50000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:20C::PROC//0001G2069501 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828RR3 Identification of Financial Instrument/Security ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 221

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 221 
 
Sample B2.j MT518 Comparison Request Cancel sent to Dealer [[Member]] 8X77* 
Message Content Comments 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200622 Close Leg [[settlement]] Date 
:92A::REPO//1, Repo Rate 
:19A::REPA//USD50001388,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 222

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 222 
 
Sample B2.k MT509 Trade Bound to Net Record sent to Dealer [[Member]] 8X77 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019808922 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608082852 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//000NE50061506 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D8B-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 223

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 223 
 
Sample B2.l MT509 Trade Bound to Net Record sent to Dealer [[Member]] 89XA 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019808924 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608082852 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//0001G2069501 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D97-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 224

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 224 
 
Sample B2.m MT509 Start Leg in Net Record sent to Dealer [[Member]] 8X77 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019815023 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608200423 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//000NE50061506 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D8B-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NESL Start Leg in Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 225

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 225 
 
Sample B2.n MT509 Start Leg in Net Record sent to Dealer [[Member]] 89XA 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019815025 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608200423 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//0001G2069501 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D97-0621 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NESL Start Leg in Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 226

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 226 
 
Sample B2.o MT548 Clearance Instruction sent to Dealer [[Member]] 8X77 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000198112022 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608205206 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700514-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700514-0621 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700514-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828RR3 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD49992601,09 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8X77 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Next Day) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200622 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 227

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 227 
 
Sample B2.o MT548 Clearance Instruction sent to Dealer [[Member]] 8X77 
Message Content Comments 
:95R::REAG/GSCC/021000018BK OF 
NYC/GSCC 
Receiving Agent ([[Buyer]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
  

---

## Page 228

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 228 
 
Sample B2.p MT548 Clearance Instruction sent to Dealer [[Member]] 89XA 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000198112024 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608205206 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700515-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700515-0621 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700515-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828RR3 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD49992601,09 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/89XA Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Next Day) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200622 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 229

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 229 
 
Sample B2.p MT548 Clearance Instruction sent to Dealer [[Member]] 89XA 
Message Content Comments 
:95R::DEAG/GSCC/021000018BK OF 
NYC/GSCC 
Delivering Agent ([[Seller]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
 
  

---

## Page 230

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 230 
 
Sample B2.q MT548 Cleared Obligation sent to Dealer [[Member]] 8X77 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000198210331 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200622082052 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700514-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700514-0621 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700514-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828RR3 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD49992601,09 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8X77 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/CLRD Type of [[settlement]] Transaction (Cleared) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200622 [[settlement]] Date 
:70E::SPRO//GSCC Opening Par Amount and Opening [[settlement]] Amount 

---

## Page 231

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 231 
 
Sample B2.q MT548 Cleared Obligation sent to Dealer [[Member]] 8X77 
Message Content Comments 
/OPARFAMT50000000,/OPSTUSD49992601,09 
:16S:SETTRAN   
- End of Message 
 
 
 
 
  

---

## Page 232

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 232 
 
Sample B2.r MT548 Cleared Obligation sent to Dealer [[Member]] 89XA 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000198210330 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200622082052 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700515-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700515-0621 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700515-0621 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828RR3 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD49992601,09 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/89XA Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/CLRD Type of [[settlement]] Transaction (Cleared) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200622 [[settlement]] Date 
:70E::SPRO//GSCC Opening Par Amount and Opening [[settlement]] Amount 

---

## Page 233

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 233 
 
Sample B2.r MT548 Cleared Obligation sent to Dealer [[Member]] 89XA 
Message Content Comments 
/OPARFAMT50000000,/OPSTUSD49992601,09 
:16S:SETTRAN   
- End of Message 
 
 
 
 
 
  

---

## Page 234

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 234 
 
Sample # B3 – Comparison, Netting and [[settlement]] Messages Resulting from a Same-Day 
Starting Repo Transaction  
On July 22, 2020, Repo Dealer [[Member]] 8X77 executes a same-day starting repo transaction with Repo Dealer 
[[Member]] 89XA for 50,000,000 of US Treasury Note 2.625% of 3/31/2 – [[CUSIP]] 9128284F4. The Contract Repo 
Rate is 2.00%. The Start Leg [[settlement]] Date is July 22, 2020 and the End Leg [[settlement]] Date is July 23, 
2020. The Start Leg [[settlement]] Amount is $49,750,000.00 and the End Leg [[settlement]] Amount is 
$49,752,763.89. The same-day starting repo transaction is submitted to [[GSD]] for comparison and [[settlement]] by 
both Repo Dealer Members 8X77 and 89XA, respectively.   
[[Member]] Reference Numbers 8X77 89XA 
Message Reference 000024596732 0000094373 
External Reference 000RN70096516 0001G2094591 
New External Reference N/A N/A 
[[Broker]] Reference N/A N/A 
[[GSD]] Assigned Reference (TID) 000F33-0722 000F72-0722 
Secondary Reference N/A N/A 
[[GSD]] Assigned Reference (OID) 700321-0722 700322-0722 
 
The message samples presented on the following pages are all based on the above scenario.  
For the purposes of this example, we assume the following:  
1. Because this scenario is for a Same-Day Starting Repo Transaction, the Start Leg will settle trade-for-
trade at contract value on its original scheduled [[settlement]] date. Therefore, the Par/Quantity and 
[[settlement]] amount on the [[obligations]] for the Members is equal to the Par and Contract Value (the start leg 
[[settlement]] amount) on the underlying repo trades.   
2. The delivering party, Repo Dealer [[Member]] 8X77 will settle its deliver obligation with [[GSD]] on July 22, 
2020 enabling the [[settlement]] of the receive obligation for Repo Dealer [[Member]] 89XA. 
3. The End Leg will go into the net on July 22, 2020. Note: The netting and [[settlement]] of the End Leg will not 
be covered in this scenario. 
 
B3.a MT515 Repo Dealer [[Member]] 8X77 Submits Repo Transaction to [[GSD]]* 
B3.b MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 8X77* 
B3.c MT518 Comparison Request sent to Repo Dealer [[Member]] 89XA* 
B3.d MT515 Repo Dealer [[Member]] 89XA Submits Revere Repo Transaction to [[GSD]]* 
B3.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 89XA* 
B3.f. MT518 Comparison Request sent to Repo Dealer [[Member]] 8X77* 

---

## Page 235

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 235 
 
B3.g MT509 Trade Compared Record sent to Repo Dealer [[Member]] 8X77* 
B3.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 89XA* 
B3.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 89XA* 
B3.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8X77* 
B3.k MT509 Trade Bound to Net sent to Repo Dealer [[Member]] 8X77 
B3.l MT509 Trade Bound to Net sent to Repo Dealer [[Member]] 89XA 
B3.m MT548 Clearance Instruction sent to Repo Dealer [[Member]] 8X77 
B3.n MT548 Clearance Instruction sent to Repo Dealer [[Member]] 89XA 
B3.o MT548 Cleared Obligation sent to Repo Dealer [[Member]] 8X77 
B3.p MT548 Cleared Obligation sent to Repo Dealer [[Member]] 89XA 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated.  
 
  

---

## Page 236

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 236 
 
Sample B3.a MT515 Dealer [[Member]] 8X77 Submits Repo Transaction to [[GSD]]* 
Message Content Comments 
1GSOXT [[GSD]] Assigned Unique Identifier 
8X77 Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//000024596732 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200722070244 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//000RN70096516 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200722070228 Trade Date and Time 
:98A::SETT//20200722 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD49750000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE/SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128284F4 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  

---

## Page 237

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 237 
 
Sample B3.a MT515 Dealer [[Member]] 8X77 Submits Repo Transaction to [[GSD]]* 
Message Content Comments 
:98A::REPU//20200723 Close Leg [[settlement]] Date 
:92A::REPO//2, Repo Rate 
:19A::REPA//USD49752763,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 238

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 238 
 
Sample B3.b MT509 Trade Accepted Record sent to Dealer [[Member]] 8X77* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807189 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722070247 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//000RN70096516 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//000024596732 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK  
:16R:LINK  
:20C::LIST//000F33-0722 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 239

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 239 
 
Sample B3.c MT518 Comparison Request sent to Dealer [[Member]] 89XA* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807191 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200722070247 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200722070228 Trade Date and Time 
:98A::SETT//20200722 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD49750000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:20C::PROC//000RN70096516 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128284F4 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200723 Close Leg [[settlement]] Date 
:92A::REPO//2, Repo Rate 

---

## Page 240

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 240 
 
Sample B3.c MT518 Comparison Request sent to Dealer [[Member]] 89XA* 
Message Content Comments 
:19A::REPA//USD49752763,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 241

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 241 
 
Sample B3.d MT515 Dealer [[Member]] 89XA Submits Reverse Repo Transaction to [[GSD]]* 
Message Content Comments 
G1LKNL [[GSD]] Assigned Unique Identifier 
89XA Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//00000094373 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200722070338 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//0001G2094591 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200722070228 Trade Date and Time 
:98A::SETT//20200722 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD49750000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE/BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128284F4 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  

---

## Page 242

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 242 
 
Sample B3.d MT515 Dealer [[Member]] 89XA Submits Reverse Repo Transaction to [[GSD]]* 
Message Content Comments 
:98A::REPU//20200723 Close Leg [[settlement]] Date 
:92A::REPO//2, Repo Rate 
:19A::REPA//USD49752763,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 243

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 243 
 
Sample B3.e MT509 Trade Accepted Record sent to Dealer [[Member]] 89XA* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807201 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722070339 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//0001G2094591 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//00000090073 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK  
:16R:LINK  
:20C::LIST//000F72-0722 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 244

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 244 
 
Sample B3.f MT518 Comparison Request sent to Dealer [[Member]] 8X77* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807203 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200722070339 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200722070228 Trade Date and Time 
:98A::SETT//20200722 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD49750000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:20C::PROC//0001G2094591 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128284F4 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200723 Close Leg [[settlement]] Date 
:92A::REPO//2, Repo Rate 

---

## Page 245

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 245 
 
Sample B3.f MT518 Comparison Request sent to Dealer [[Member]] 8X77* 
Message Content Comments 
:19A::REPA//USD49752763,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 246

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 246 
 
Sample B3.g MT509 Trade Compared Record sent to Dealer [[Member]] 8X77* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807205 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722070339 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//000RN70096516 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000F33-0722 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16R:LINK  
:20C::PROG//0001G2094591 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 247

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 247 
 
Sample B3.h MT518 Comparison Request Cancel sent to Dealer [[Member]] 89XA* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807208 Sender’s Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200722070340 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200722070228 Trade Date and Time 
:98A::SETT//20200722 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD49750000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:20C::PROC//000RN70096516 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128284F4 Identification of Financial Instrument/Security ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 248

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 248 
 
Sample B3.h MT518 Comparison Request Cancel sent to Dealer [[Member]] 89XA* 
Message Content Comments 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200723 Close Leg [[settlement]] Date 
:92A::REPO//2, Repo Rate 
:19A::REPA//USD49752763,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 249

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 249 
 
Sample B3.i MT509 Trade Compared Record sent to Dealer [[Member]] 89XA* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807210 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722070340 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//0001G2094591 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000F72-0722 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16R:LINK  
:20C::PROG//000RN70096516 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 250

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 250 
 
Sample B3.j MT518 Comparison Request Cancel sent to Dealer [[Member]] 8X77* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807213 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200722070340 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200722070228 Trade Date and Time 
:98A::SETT//20200722 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD49750000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART89XA [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:20C::PROC//0001G2094591 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8X77 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128284F4 Identification of Financial Instrument/Security ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 251

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 251 
 
Sample B3.j MT518 Comparison Request Cancel sent to Dealer [[Member]] 8X77* 
Message Content Comments 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200723 Close Leg [[settlement]] Date 
:92A::REPO//2, Repo Rate 
:19A::REPA//USD49752763,89 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 252

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 252 
 
Sample B3.k MT509 Trade Bound to Net Record sent to Dealer [[Member]] 8X77 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807215 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722070341 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//000RN70096516 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000F33-0722 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 253

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 253 
 
Sample B3.l MT509 Trade Bound to Net Record sent to Dealer [[Member]] 89XA 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807219 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722070341 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//0001G2094591 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000F72-0722 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 254

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 254 
 
Sample B3.m MT548 Clearance Instruction sent to Dealer [[Member]] 8X77 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807221 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722070343 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700321-0722 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700321-0722 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000F33-0722 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/9128284F4 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD49750000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8X77 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Same Day) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200722 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 255

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 255 
 
Sample B3.m MT548 Clearance Instruction sent to Dealer [[Member]] 8X77 
Message Content Comments 
:95R::REAG/GSCC/021000018BK OF 
NYC/GSCC 
Receiving Agent ([[Buyer]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
  

---

## Page 256

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 256 
 
Sample B3.n MT548 Clearance Instruction sent to Dealer [[Member]] 89XA 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021807224 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722070344 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700322-0722 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700322-0722 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000F72-0722 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/9128284F4 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD49750000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/89XA Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Same Day) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200722 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 257

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 257 
 
Sample B3.n MT548 Clearance Instruction sent to Dealer [[Member]] 89XA 
Message Content Comments 
:95R::DEAG/GSCC/021000018BK OF 
NYC/GSCC 
Delivering Agent ([[Seller]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
 
  

---

## Page 258

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 258 
 
Sample B3.o MT548 Cleared Obligation sent to Dealer [[Member]] 8X77 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
8X77 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021809157 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722072802 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700321-0722 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700321-0722 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000F33-0722 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/9128284F4 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD49750000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8X77 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/CLRD Type of [[settlement]] Transaction (Cleared) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200722 [[settlement]] Date 
:70E::SPRO//GSCC Opening Par Amount and Opening [[settlement]] Amount 

---

## Page 259

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 259 
 
Sample B3.o MT548 Cleared Obligation sent to Dealer [[Member]] 8X77 
Message Content Comments 
/OPARFAMT50000000,/OPSTUSD49750000, 
:16S:SETTRAN   
- End of Message 
 
 
 
 
  

---

## Page 260

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 260 
 
Sample B3.p MT548 Cleared Obligation sent to Dealer [[Member]] 89XA 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
89XA Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021809156 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200722072802 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700322-0722 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700322-0722 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000F72-0722 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/9128284F4 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD49750000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/89XA Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/CLRD Type of [[settlement]] Transaction (Cleared) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200722 [[settlement]] Date 
:70E::SPRO//GSCC Opening Par Amount and Opening [[settlement]] Amount 

---

## Page 261

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 261 
 
Sample B3.p MT548 Cleared Obligation sent to Dealer [[Member]] 89XA 
Message Content Comments 
/OPARFAMT50000000,/OPSTUSD49750000, 
:16S:SETTRAN   
- End of Message 
 
 
 
 
  

---

## Page 262

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 262 
 
Sample # B4 – Comparison, Netting and [[settlement]] Messages Resulting from a Same-Day 
Starting Repo Transaction Cancelled Post Comparison/Pre-Net 
On July 27, 2020, Repo Dealer [[Member]] 87E7 executes a term same-day starting repo transaction with Repo 
Dealer [[Member]] 808A for 50,000,000 of US Treasury Note 3.625% of 2/15/21 ([[CUSIP]] 912828PX2). The 
Contract Repo Rate is 2.01%. The Start Leg [[settlement]] Date is July 27, 2020 and the End Leg [[settlement]] 
Date is July 30, 2020. The Start Leg [[settlement]] Amount is $51,000,000.00 and the End Leg [[settlement]] 
Amount is $51,008,542.50. The same-day starting repo transaction is submitted to [[GSD]] for comparison and 
[[settlement]] by both Repo Dealer Members 87E7 and 808A, respectively on the morning of July 27, 2020 but the 
trade is canceled by both parties that same afternoon.   
[[Member]] Reference Numbers 87E7 808A 
Message Reference (Instruct) 00001011 00000025876 
Message Reference (Cancel) 00001610 00000027857 
External Reference RF2020362504 GS0012082020 
New External Reference N/A N/A 
[[Broker]] Reference N/A N/A 
[[GSD]] Assigned Reference (TID) 000B56-0727 000B98-0727 
Secondary Reference N/A N/A 
[[GSD]] Assigned Reference (OID) 000737-0727 000738-0727 
 
The message samples presented on the following pages are all based on the above scenario.  
For the purposes of this example, we assume the following:  
1. Because this scenario is for a Same-Day Starting Repo Transaction, the Start Leg will settle trade-for-
trade at contract value on its original scheduled [[settlement]] date. Therefore, the Par/Quantity and 
[[settlement]] amount on the [[obligations]] for the Members is equal to the Par and Contract Value (the start leg 
[[settlement]] amount) on the underlying repo trades.   
2. The delivering party, Repo Dealer [[Member]] 87E7 has failed to deliver to [[GSD]] its obligation for 50,000,000 
vs. $51,000,000.00 of [[CUSIP]] 912828PX2, at the time the cancellation of the trade is processed.  
 
B4.a MT515 Repo Dealer [[Member]] 87E7 Submits Repo Transaction to [[GSD]]* 
B4.b MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 87E7* 
B4.c MT518 Comparison Request sent to Repo Dealer [[Member]] 808A* 
B4.d MT515 Repo Dealer [[Member]] 808A Submits Reverse Repo Transaction to [[GSD]]* 
B4.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 808A* 
B4.f. MT518 Comparison Request sent to Repo Dealer [[Member]] 87E7* 
B4.g MT509 Trade Compared Record sent to Repo Dealer [[Member]] 87E7* 

---

## Page 263

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 263 
 
B4.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 808A* 
B4.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 808A* 
B4.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 87E7* 
B4.k MT509 Trade Bound for Net sent to Repo Dealer [[Member]] 87E7* 
B4.l MT509 Trade Bound for Net sent to Repo Dealer [[Member]] 808A* 
B4.m MT548 Clearance Instruction sent to Repo Dealer [[Member]] 87E7  
B4.n MT548 Clearance Instruction sent to Repo Dealer [[Member]] 808A  
B4.o MT515 Repo Dealer [[Member]] 87E7 Submits Cancel (post comparison) to [[GSD]] 
B4.p MT509 Cancel Accepted Record sent to Repo Dealer [[Member]] 87E7* 
B4.q MT518 Cancel Requested sent to Repo Dealer [[Member]] 808A* 
B4.r MT515 Repo Dealer [[Member]] 808A Submits Cancel (post comparison) to [[GSD]] 
B4.s MT509 Cancel Accepted Record sent to Repo Dealer [[Member]] 808A 
B4.t MT518 Cancel Requested sent to Repo Dealer [[Member]] 87E7* 
B4.u MT509 Trade Canceled sent to Repo Dealer [[Member]] 87E7* 
B4.v MT509 Trade Canceled sent to Repo Dealer [[Member]] 808A* 
B4.w MT548 Clearance Instruction Cancel sent to Repo Dealer [[Member]] 87E7 
B4.x MT548 Clearance Instruction Cancel sent to Repo Dealer [[Member]] 808A 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated.  
 
  

---

## Page 264

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 264 
 
Sample B4.a MT515 Repo Dealer [[Member]] 87E7 Submits Repo Transaction to [[GSD]]* 
Message Content Comments 
GSD001 [[GSD]] Assigned Unique Identifier 
87E7 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//00001011 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200727070210 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//RF2020362504 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  

---

## Page 265

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 265 
 
Sample B4.a MT515 Repo Dealer [[Member]] 87E7 Submits Repo Transaction to [[GSD]]* 
Message Content Comments 
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 266

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 266 
 
Sample B4.b MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930718 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200727070216 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//RF2020362504 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//00001011 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK   
:16R:LINK   
:20C::LIST//000B56-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
 
  

---

## Page 267

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 267 
 
Sample B4.c MT518 Comparison Request sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930720 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator 
:98C::PREP//20200727070226 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:20C::PROC//RF2020362504 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 

---

## Page 268

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 268 
 
Sample B4.c MT518 Comparison Request sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
 
  

---

## Page 269

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 269 
 
Sample B4.d MT515 Repo Dealer [[Member]] 808A Submits Reverse Repo Transaction to [[GSD]]* 
Message Content Comments 
GSD023 [[GSD]] Assigned Unique Identifier 
808A Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//00000025876 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200727070456 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//GS0012082020 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  

---

## Page 270

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 270 
 
Sample B4.d MT515 Repo Dealer [[Member]] 808A Submits Reverse Repo Transaction to [[GSD]]* 
Message Content Comments 
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
 
  

---

## Page 271

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 271 
 
Sample B4.e MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930817 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200727070502 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GS0012082020 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//00000025876 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK   
:16R:LINK   
:20C::LIST//000B98-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 272

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 272 
 
Sample B4.f MT518 Comparison Request sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930819 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator 
:98C::PREP//20200727070511 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:20C::PROC//GS0012082020 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 

---

## Page 273

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 273 
 
Sample B4.f MT518 Comparison Request sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
 
  

---

## Page 274

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 274 
 
Sample B4.g MT509 Trade Compared Record sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930821 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200727070335 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//RF2020362504 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000A08-9829 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:LINK   
:20C::PROG//GS0012082020 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
 
 
  

---

## Page 275

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 275 
 
Sample B4.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930823 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200727070342 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:20C::PROC//RF2020362504 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 276

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 276 
 
Sample B4.h MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 277

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 277 
 
Sample B4.i MT509 Trade Compared Record sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930825 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200727070347 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GS0012082020 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000B98-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:LINK   
:20C::PROG//RF2020362504 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 278

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 278 
 
Sample B4.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930827 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200727070352 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:20C::PROC//GS0012082020 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 279

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 279 
 
Sample B4.j MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 280

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 280 
 
Sample B4.k MT509 Trade Bound to Net sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930829 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20190829070354 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//RF2020362504 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//000B56-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status  
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 281

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 281 
 
Sample B4.l MT509 Trade Bound to Net sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930831 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20190829070356 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GS0012082020 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//000B98-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status  
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 282

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 282 
 
Sample B4.m MT548 Clearance Instruction sent to Repo Dealer [[Member]] 87E7 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930835 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200727070358 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//000737-0727 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//000737-0727 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000B56-0727 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD51000000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/87E7 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Same Day) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200727 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 283

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 283 
 
Sample B4.m MT548 Clearance Instruction sent to Repo Dealer [[Member]] 87E7 
Message Content Comments 
:95R::REAG/GSCC/021000018BK 
OF NYC/GSCC 
Receiving Agent ([[Buyer]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
 
 
  

---

## Page 284

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 284 
 
Sample B4.n MT548 Clearance Instruction sent to Repo Dealer [[Member]] 808A 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021930837 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200727070358 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//000738-0727 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//000738-0727 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000B98-0727 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD51000000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/808A Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Same Day) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200727 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 285

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 285 
 
Sample B4.n MT548 Clearance Instruction sent to Repo Dealer [[Member]] 808A 
Message Content Comments 
:95R::DEAG/GSCC/021000018BK 
OF NYC/GSCC 
Delivering Agent ([[Seller]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
 
 
 
  

---

## Page 286

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 286 
 
Sample B4.o MT515 Repo Dealer [[Member]] 87E7 Submits Cancel (post comparison) to [[GSD]]* 
Message Content Comments 
GSD001 [[GSD]] Assigned Unique Identifier 
87E7 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//00001610 Sender’s Message Reference Number  
:23G:CANC Cancel Message 
:98C::PREP//20200727093816 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//RF2020362504 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CANC Cancel Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 

---

## Page 287

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 287 
 
Sample B4.o MT515 Repo Dealer [[Member]] 87E7 Submits Cancel (post comparison) to [[GSD]]* 
Message Content Comments 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 288

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 288 
 
Sample B4.p MT509 Cancel Accepted Record sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021931721 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200727093822 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//RF2020362504 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//00001610 Related Reference ([[Member]]'s SEME from MT515 Cancel Record) 
:16S:LINK   
:16R:LINK   
:20C::LIST//000B56-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::CPRC//PACK Cancel Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 289

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 289 
 
Sample B4.q MT518 Cancel Requested sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021931723 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200727093829 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK  
:16R:LINK  
:20C::LIST//000B98-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CREQ Cancel Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 

---

## Page 290

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 290 
 
Sample B4.q MT518 Cancel Requested sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 291

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 291 
 
Sample B4.r MT515 Repo Dealer [[Member]] 808A Submits Cancel (post comparison) to [[GSD]]* 
Message Content Comments 
GSD023 [[GSD]] Assigned Unique Identifier 
808A Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//00000027857 Sender’s Message Reference Number  
:23G:CANC Cancel Message 
:98C::PREP//20200727094432 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//GS0012082020 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CANC Cancel Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 

---

## Page 292

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 292 
 
Sample B4.r MT515 Repo Dealer [[Member]] 808A Submits Cancel (post comparison) to [[GSD]]* 
Message Content Comments 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 293

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 293 
 
Sample B4.s MT509 Cancel Accepted Record sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021931818 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200727094440 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GS0012082020 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//00000027857 Related Reference ([[Member]]'s SEME from MT515 Cancel Record) 
:16S:LINK   
:16R:LINK   
:20C::LIST//000B98-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::CPRC//PACK Cancel Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 294

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 294 
 
Sample B4.t MT518 Cancel Requested sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021931821 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200727094445 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK  
:20C::MAST//RF2020362504 Master External Reference Number  
:16S:LINK  
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK  
:16R:LINK  
:20C::LIST//000B56-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200727070102 Trade Date and Time 
:98A::SETT//20200727 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD51000000, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CREQ Cancel Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART808A [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   

---

## Page 295

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 295 
 
Sample B4.t MT518 Cancel Requested sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
:95R::SELL/GSCC/PART87E7 [[Seller]] (Repo Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200730 Close Leg [[settlement]] Date 
:92A::REPO//2,01 Repo Rate 
:19A::REPA//USD51008542,5 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 296

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 296 
 
Sample B4.u MT509 Trade Canceled Record sent to Repo Dealer [[Member]] 87E7* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021931824 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200727094451 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//RF2020362504 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000B56-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::CPRC//CAND Cancel Processed 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 297

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 297 
 
Sample B4.v MT509 Trade Canceled Record sent to Repo Dealer [[Member]] 808A* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021931826 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200727094458 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GS0012082020 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000B98-0727 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::CPRC//CAND Cancel Processed 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 298

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 298 
 
 
Sample B4.w MT548 Clearance Instruction Cancel sent to Repo Dealer [[Member]] 87E7 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
87E7 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021931830 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200727094503 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//000737-0727 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//000737-0727 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000B56-0727 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//CAND Status (Previous Instruction sent to bank must be canceled) 
:16R:REAS  
:24B::CAND/GSCC/GSER Reason Code for Cancel Messages 
:16S:REAS  
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD51000000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/87E7 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Same Day) 

---

## Page 299

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 299 
 
Sample B4.w MT548 Clearance Instruction Cancel sent to Repo Dealer [[Member]] 87E7 
Message Content Comments 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200727 [[settlement]] Date 
:16R:SETPRTY   
:95R::REAG/GSCC/021000018BK 
OF NYC/GSCC 
Receiving Agent ([[Buyer]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
 
  

---

## Page 300

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 300 
 
Sample B4.x MT548 Clearance Instruction Cancel sent to Repo Dealer [[Member]] 808A 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
808A Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000021931832 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200727094505 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//000738-0727 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//000738-0727 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000B98-0727 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//CAND Status (Previous Instruction sent to bank must be canceled) 
:16R:REAS  
:24B::CAND/GSCC/GSER Reason Code for Cancel Messages 
:16S:REAS  
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828PX2 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD51000000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/808A Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Same Day) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 

---

## Page 301

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 301 
 
Sample B4.x MT548 Clearance Instruction Cancel sent to Repo Dealer [[Member]] 808A 
Message Content Comments 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200727 [[settlement]] Date 
:16R:SETPRTY   
:95R::DEAG/GSCC/021000018BK 
OF NYC/GSCC 
Delivering Agent ([[Seller]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
 
  

---

## Page 302

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 302 
 
Sample # B5 – Comparison and Netting Messages Resulting from a Forward Settling 
Buy/Sell Transaction Cancelled/Removed from Net Post Comparison 
On June 8, 2020, Dealer [[Member]] 8437 executes a next day settling buy trade for 15,000,000 of US Treasury 
Note 2.750% of 2/28/25 – [[CUSIP]] 9128283Z1 with Dealer [[Member]] 8905 for forward [[settlement]] on June 11, 
2020, at a price of 99.375. The final money ([[settlement]] amount) is $14,961,933.38. The forward settling 
buy/sell transaction is submitted to [[GSD]] for comparison and [[settlement]] by both Dealer Members 8437 and 
8905, respectively on June 8, 2020 but is subsequently canceled by both parties on June 9, 2020.   
[[Member]] Reference Numbers 8437 8905 
Message Reference (Instruct) 001324516710 000007317092 
Message Reference (Cancel) 001324521671 000007321709 
External Reference WLP50016590 GDETV2026953 
New External Reference N/A N/A 
[[Broker]] Reference N/A N/A 
[[GSD]] Assigned Reference (TID) 000D4B-0608 000D58-0608 
Secondary Reference N/A N/A 
[[GSD]] Assigned Reference (OID) N/A N/A 
 
The message samples presented on the following pages are all based on the above scenario.  
B5.a MT515 Dealer [[Member]] 8437 Submits Buy Transaction to [[GSD]]* 
B5.b MT509 Trade Accepted Record sent to Dealer [[Member]] 8437* 
B5.c MT518 Comparison Request sent to Dealer [[Member]] 8905* 
B5.d MT515 Dealer [[Member]] 8905 Submits Sell Transaction to [[GSD]]* 
B5.e MT509 Trade Accepted Record sent to Dealer [[Member]] 8905* 
B5.f. MT518 Comparison Request sent to Dealer [[Member]] 8437* 
B5.g MT509 Trade Compared Record sent to Dealer [[Member]] 8437* 
B5.h MT518 Comparison Request Cancel (due to match) sent to Dealer [[Member]] 8905* 
B5.i MT509 Trade Compared Record sent to Dealer [[Member]] 8905* 
B5.j MT518 Comparison Request Cancel (due to match) sent to Dealer [[Member]] 8437* 
B5.k MT509 Trade Bound for Net sent to Dealer [[Member]] 8437 
B5.l MT509 Trade Bound for Net sent to Dealer [[Member]] 8905 
B5.m MT590 Per Trade Forward [[Margin]] sent to Dealer [[Member]] 8437 

---

## Page 303

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 303 
 
B5.n MT590 Per Trade Forward [[Margin]] sent to Dealer [[Member]] 8905 
B5.o MT515 Dealer [[Member]] 8437 Submits Cancel (post comparison) to [[GSD]]* 
B5.p MT509 Cancel Accepted Record sent to Dealer [[Member]] 8437* 
B5.q MT518 Cancel Requested sent to Dealer [[Member]] 8905* 
B5.r MT515 Dealer [[Member]] 8905 Submits Cancel (post comparison) to [[GSD]]* 
B5.s MT509 Cancel Accepted Record sent to Dealer [[Member]] 8905* 
B5.t MT518 Cancel Requested sent to Dealer [[Member]] 8437* 
B5.u MT509 Trade Canceled sent to Dealer [[Member]] 8437* 
B5.v MT509 Trade Canceled sent to Dealer [[Member]] 8905* 
B5.w MT509 Forward Trade Pended No Longer in Net – Trade Canceled sent to Dealer [[Member]] 8437 
B5.x MT509 Forward Trade Pended No Longer in Net – Trade Canceled sent to Dealer [[Member]] 8905 
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated.  
 
 
  

---

## Page 304

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 304 
 
Sample B5.a MT515 Dealer [[Member]] 8437 Submits Buy Transaction to [[GSD]]* 
Message Content Comments 
1KLONT [[GSD]] Assigned Unique Identifier 
8437 Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//001324516710 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608081123 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::MAST//WLP50016590 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128283Z1 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
- End of Message 

---

## Page 305

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 305 
 
 
Sample B5.b MT509 Trade Accepted Record sent to Dealer [[Member]] 8437* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793191 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608081128 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLP50016590 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//001324516710 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D4B-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 306

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 306 
 
Sample B5.c MT518 Comparison Request sent to Dealer [[Member]] 8905* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793193 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608081128 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:20C::PROC// WLP50016590 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128283Z1 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
- End of Message 
  

---

## Page 307

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 307 
 
Sample B5.d MT515 Dealer [[Member]] 8905 Submits Sell Transaction to [[GSD]]* 
Message Content Comments 
D5GKNC [[GSD]] Assigned Unique Identifier 
8905 Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//000007390022 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608081212 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::MAST//GDETV2026953 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128283Z1 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
- End of Message 

---

## Page 308

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 308 
 
 
Sample B5.e MT509 Trade Accepted Record sent to Dealer [[Member]] 8905* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793256 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608081216 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDETV2026953 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//000007390022 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D58-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 309

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 309 
 
Sample B5.f MT518 Comparison Request sent to Dealer [[Member]] 8437* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793258 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608081216 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:20C::PROC//GDETV2026953 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128283Z1 Identification of Financial Instrument/Security ([[CUSIP]]) 
:16S:CONFDET   
- End of Message 
  

---

## Page 310

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 310 
 
Sample B5.g MT509 Trade Compared Record sent to Dealer [[Member]] 8437* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793265 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608081218 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLP50016590 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D4B-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16R:LINK  
:20C::PROG//GDETV2026953 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 311

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 311 
 
Sample B5.h MT518 Comparison Request Cancel sent to Dealer [[Member]] 8905* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793267 Sender’s Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200608081218 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – Contra-party [[ID]] 
:20C::PROC//WLP50016590 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – [[Member]] [[ID]]  
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128283Z1 Identification of Financial Instrument/Security ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 312

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 312 
 
Sample B5.h MT518 Comparison Request Cancel sent to Dealer [[Member]] 8905* 
Message Content Comments 
:16S:CONFDET   
- End of Message 
  

---

## Page 313

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 313 
 
Sample B5.i MT509 Trade Compared Record sent to Dealer [[Member]] 8905* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793269 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608081218 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDETV2026953 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D58-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16R:LINK  
:20C::PROG//WLP50016590 Contra-party External Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 314

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 314 
 
Sample B5.j MT518 Comparison Request Cancel sent to Dealer [[Member]] 8437* 
Message Content Comments  
Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793271 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200608081218 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8437 [[Buyer]] (Reverse Party) Information – [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8905 [[Seller]] (Repo Party) Information – Contra-party [[ID]]  
:20C::PROC//GDETV2026953 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128283Z1 Identification of Financial Instrument/Security ([[CUSIP]]) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 315

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 315 
 
Sample B5.j MT518 Comparison Request Cancel sent to Dealer [[Member]] 8437* 
Message Content Comments 
:16S:CONFDET   
- End of Message 
  

---

## Page 316

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 316 
 
Sample B5.k MT509 Trade Bound to Net Record sent to Dealer [[Member]] 8437 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793275 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608081220 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLP50016590 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D4B-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 317

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 317 
 
Sample B5.l MT509 Trade Bound to Net Record sent to Dealer [[Member]] 8905 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019793278 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200608081220 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDETV2026953 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D58-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 318

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 318 
 
Sample B5.m MT590 Per Trade Forward [[Margin]] sent to Dealer [[Member]] 8437 
Message Content Comments 
  Password - Blank on MT590 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
590/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:20:000D4B-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:21:WLP50016590 [[Member]]’s External Reference Number 
:25:8437 Account [[ID]] ([[Member]] [[ID]]) 
:32C:200609USD18096,32 Date and Amount of Credit 
:71B:/GSCC/DRCR/FMFF/US/9128283Z1 Details of Charges – Forward [[Margin]]/Forward Finance/[[CUSIP]] 
- End of Message 
 
  

---

## Page 319

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 319 
 
Sample B5.n MT590 Per Trade Forward [[Margin]] sent to Dealer [[Member]] 8905 
Message Content Comments 
  Password - Blank on MT590 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
590/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:20:000D58-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:21:GDETV2026953 [[Member]]’s External Reference Number 
:25:8905 Account [[ID]] ([[Member]] [[ID]]) 
:32D:200609USD18096,32 Date and Amount of Debit 
:71B:/GSCC/DRCR/FMFF/US/9128283Z1 Details of Charges – Forward [[Margin]]/Forward Finance/[[CUSIP]] 
- End of Message 
 
 
 
 
 
 
  

---

## Page 320

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 320 
 
Sample B5.o MT515 Dealer [[Member]] 8437 Submits Cancel (post comparison) to [[GSD]]* 
Message Content Comments 
1KLONT [[GSD]] Assigned Unique Identifier 
8437 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//001324521671 Sender’s Message Reference Number  
:23G:CANC Cancel Message 
:98C::PREP//20200609120836 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::MAST//WLP50016590 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CANC Cancel Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8905 [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8437 [[Seller]] (Repo Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 

---

## Page 321

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 321 
 
Sample B5.o MT515 Dealer [[Member]] 8437 Submits Cancel (post comparison) to [[GSD]]* 
Message Content Comments 
:35B:/US/9128283Z1 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
- End of Message 
 
  

---

## Page 322

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 322 
 
Sample B5.p MT509 Cancel Accepted Record sent to Dealer [[Member]] 8437* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019879130 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200609120839 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLP50016590 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//001324521671 Related Reference ([[Member]]'s SEME from MT515 Cancel Record) 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D4B-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::CPRC//PACK Cancel Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 323

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 323 
 
Sample B5.q MT518 Cancel Requested sent to Dealer [[Member]] 8905* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019879133 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200609120839 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D58-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CREQ Cancel Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8905 [[Buyer]] (Reverse Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8437 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 

---

## Page 324

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 324 
 
Sample B5.q MT518 Cancel Requested sent to Dealer [[Member]] 8905* 
Message Content Comments 
:35B:/US/9128283Z1 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
- End of Message 
 
  

---

## Page 325

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 325 
 
Sample B5.r MT515 Dealer [[Member]] 8905 Submits Cancel (post comparison) to [[GSD]]* 
Message Content Comments 
D5GKNC [[GSD]] Assigned Unique Identifier 
8905 Sender [[ID]] ([[participant]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//000007321709 Sender’s Message Reference Number  
:23G:CANC Cancel Message 
:98C::PREP//20200609120925 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK   
:20C::MAST//GDETV2026953 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CANC Cancel Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8905 [[Buyer]] (Reverse Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8437 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 

---

## Page 326

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 326 
 
Sample B5.r MT515 Dealer [[Member]] 8905 Submits Cancel (post comparison) to [[GSD]]* 
Message Content Comments 
:35B:/US/9128283Z1 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
- End of Message 
  

---

## Page 327

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 327 
 
Sample B5.s MT509 Cancel Accepted Record sent to Dealer [[Member]] 8905* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019879313 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200609120928 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDETV2026953 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//000007321709 Related Reference ([[Member]]'s SEME from MT515 Cancel Record) 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D58-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::CPRC//PACK Cancel Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 328

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 328 
 
Sample B5.t MT518 Cancel Requested sent to Dealer [[Member]] 8437* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019879315 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200609120928 Date and Time of Message Preparation 
:22F::TRTR/GSCC/CASH Cash Trade Indicator 
:16R:LINK  
:20C::MAST//WLP50016590 Master External Reference Number  
:16S:LINK  
:16R:LINK  
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK  
:16R:LINK  
:20C::LIST//000D4B-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK  
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200608081108 Trade Date and Time 
:98A::SETT//20200611 [[settlement]] Date 
:90A::DEAL//PRCT/99,375  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD14961933,38 [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CREQ Cancel Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8905 [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   

---

## Page 329

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 329 
 
Sample B5.t MT518 Cancel Requested sent to Dealer [[Member]] 8437* 
Message Content Comments 
:95R::SELL/GSCC/PART8437 [[Seller]] (Repo Party) Information - [[participant]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/15000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/9128283Z1 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
- End of Message 
  

---

## Page 330

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 330 
 
Sample B5.u MT509 Trade Canceled Record sent to Dealer [[Member]] 8437* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019879317 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200609120930 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLP50016590 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D4B-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::CPRC//CAND Cancel Processed 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 331

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 331 
 
Sample B5.v MT509 Trade Canceled Record sent to Dealer [[Member]] 8905* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019879319 Sender’s ([[GSD]]) Message Reference Number  
:23G:CAST Message Function (for Cancel) 
:98C::PREP//20200609120930 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDETV2026953 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D58-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::CPRC//CAND Cancel Processed 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 332

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 332 
 
Sample B5.w MT509 Forward Trade Pended No Longer in Net – Trade Canceled sent to Dealer [[Member]] 8437 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8437 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019978137 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruct) 
:98C::PREP//20200609205512 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//WLP50016590 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D4B-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NNTC Forward Trade Pended No Longer in Net – Trade Canceled 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 333

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 333 
 
Sample B5.x MT509 Forward Trade Pended No Longer in Net – Trade Canceled sent to Dealer [[Member]] 8905 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8905 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019978139 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruct) 
:98C::PREP//20200609205512 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//GDETV2026953 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000D58-0608 [[GSD]] Assigned Reference Number (Receiver’s TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NNTC Forward Trade Pended No Longer in Net – Trade Canceled 
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 334

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 334 
 
Sample # B6 – Demand Comparison, Netting and [[settlement]] Messages Resulting from a 
Same-Day Starting Repo Transaction 
On August 20, 2020, Repo [[Broker]] [[Member]] 8KR1 executes an overnight same-day starting reverse repo 
transaction for 25,000,000 of US Treasury Note 2.500% of 8/15/23 – [[CUSIP]] 912828VS6 with Repo Dealer 
[[Member]] 8D23. The Contract Repo Rate is 1.75%.  The Start Leg [[settlement]] Date is August 20, 2020 and the 
End Leg [[settlement]] Date is August 21, 2020. The Start Leg [[settlement]] Amount is $24,937,500.00 and the End 
Leg [[settlement]] Amount is $24,938,712.24. 
[[Member]] Reference Numbers 8KR1 8D23 
Message Reference 000129 000053 
External Reference 08219KR129 999100015 
New External Reference N/A N/A 
[[Broker]] Reference BKRREF123 N/A 
[[GSD]] Assigned Reference (TID) 000B14-0820 000C02-0820 
Secondary Reference N/A N/A 
[[GSD]] Assigned Reference (OID) N/A 000322-0820 
 
The message samples presented on the following pages are all based on the above scenario.  
For the purposes of this example, we assume the following:  
1. Repo [[Broker]] 8KR1 has also executed an overnight same-day starting Repo transaction of equal contract 
value with another Repo Dealer [[Member]], the details of which will not be included in this scenario.  
2. The Repo [[Broker]] [[Member]] will have no [[obligations]] due to having a flat position.  
3. Both Brokered Repo Transactions were submitted during the demand period and are therefore compared 
upon receipt from the Demand Trade Source who in this scenario is Repo [[Broker]] [[Member]] 8KR1. 
4. Repo Dealer 8D23 submits matching trade details on the trade with Repo [[Broker]] [[Member]] 8KR1. 
5. Because this scenario is for a Same-Day Starting Repo Transaction, the Start Leg will settle trade-for-
trade at contract value on its original scheduled [[settlement]] date. Therefore, the Par/Quantity and 
[[settlement]] amount on the obligation for the Repo Dealer [[Member]] 8D23 is equal to the Par and Contract 
Value (the start leg [[settlement]] amount) on the underlying repo trade.   
6. The delivering party Repo Dealer [[Member]] 8D23 will settle its deliver obligation with [[GSD]] on August 20, 
2020 enabling the [[settlement]] of the receive obligation for the receiving party (who is not covered in this 
scenario). 
7. The End Leg will go into the net on August 20, 2020. Note: The netting and [[settlement]] of the End Leg will 
not be covered in this scenario. 
 
B6.a MT515 IDB [[Member]] 8KR1 Submits Reverse Trade to [[GSD]]* 
B6.b MT509 Trade Accepted Record sent to IDB [[Member]] 8KR1* 
B6.c MT518 Comparison Request sent to Repo Dealer [[Member]] 8D23* 

---

## Page 335

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 335 
 
B6.d MT548 Clearance Instruction sent to Repo Dealer [[Member]] 8D23 
B6.e MT515 Repo Dealer [[Member]] 8D23 Submits Repo Trade to [[GSD]]* 
B6.f MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 8D23* 
B6.g MT518 Comparison Request sent to IDB [[Member]] 8KR1* 
B6.h MT509 Trade Compared Record sent to IDB [[Member]] 8KR1* 
B6.i MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8D23* 
B6.j MT509 Trade Compared Record sent to Repo Dealer [[Member]] 8D23*  
B6.k MT518 Comparison Request Cancel (due to match) sent to IDB [[Member]] 8KR1* 
B6.l MT509 Trade Bound for Net sent to IDB [[Member]] 8KR1* 
B6.m MT509 Trade Bound for Net sent to Repo Dealer [[Member]] 8D23*  
B6.n MT548 Cleared Obligation sent to Repo Dealer [[Member]] 8D23  
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated.  
 
  

---

## Page 336

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 336 
 
Sample B6.a MT515 Repo [[Broker]] [[Member]] 8KR1 Submits Reverse Repo Transaction to [[GSD]]* 
Message Content Comments 
KR13E2 [[GSD]] Assigned Unique Identifier 
8KR1 Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//000129 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200820100928 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//08129KR129 Receiving [[Member]]’s External Reference Number 
:16S:LINK  
:16R:LINK  
:20C::BASK//BKRREF123 [[Broker]] Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200820100854 Trade Date and Time 
:98A::SETT//20200820 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD24937500, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE/BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8KR1 [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8D23 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/25000000, Quantity of Security (FAMT = Face Amount) 

---

## Page 337

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 337 
 
Sample B6.a MT515 Repo [[Broker]] [[Member]] 8KR1 Submits Reverse Repo Transaction to [[GSD]]* 
Message Content Comments 
:35B:/US/912828VS6 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200821 Close Leg [[settlement]] Date 
:92A::REPO//1,75 Repo Rate 
:19A::REPA//USD24938712,24 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 338

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 338 
 
Sample B6.b MT509 Trade Accepted Record sent to Repo [[Broker]] [[Member]] 8KR1* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8KR1 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900428 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200820100936 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//08129KR129 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//000129 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK   
:16R:LINK   
:20C::LIST//000B14-0820 [[GSD]] Assigned Reference Number (TID) 
:16S:LINK   
:16R:LINK   
:13B::LINK/GSCC/TRDR Demand Repo Trade Indicator 
:20C::BASK//BKRREF123 [[Broker]] Reference Number 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 339

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 339 
 
Sample B6.c MT518 Comparison Request sent to Repo Dealer [[Member]] 8D23* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8D23 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900431 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator 
:98C::PREP//20200820100951 Date and Time of Message Preparation 
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200820100854 Trade Date and Time 
:98A::SETT//20200820 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD24937500, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8KR1 [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:20C::PROC//08219KR129 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8D23 [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/25000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828VS6 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO   
:98A::REPU//20200821 Close Leg [[settlement]] Date 
:92A::REPO//1,75 Repo Rate 

---

## Page 340

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 340 
 
Sample B6.c MT518 Comparison Request sent to Repo Dealer [[Member]] 8D23* 
Message Content Comments 
:19A::REPA//USD24938712,24 Close Leg [[settlement]] Amount 
:16S:REPO   
- End of Message 
 
  

---

## Page 341

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 341 
 
Sample B6.d MT548 Clearance Instruction sent to Repo Dealer [[Member]] 8D23 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
8D23 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900434 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200820100956 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//000322-0820 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//000322-0820 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000B14-0820 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828VS6 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/25000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD24937500, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8D23 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Same Day) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200820 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 342

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 342 
 
Sample B6.d MT548 Clearance Instruction sent to Repo Dealer [[Member]] 8D23 
Message Content Comments 
:95R::REAG/GSCC/021000018BK OF 
NYC/GSCC 
Receiving Agent ([[Buyer]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
 
  

---

## Page 343

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 343 
 
Sample B6.e MT515 Repo Dealer [[Member]] 8D23 Submits Repo Transaction to [[GSD]]* 
Message Content Comments 
GSD001 [[GSD]] Assigned Unique Identifier 
8D23 Sender [[ID]] ([[Member]] [[ID]]) 
515/000/GSCC Message Type 
GSCCTRRS Receiver [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
:16R:GENL   
:20C::SEME//000053 Sender’s Message Reference Number  
:23G:NEWM New Trade (or Modify) Input 
:98C::PREP//20200820101201 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::MAST//999100015 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200820100854 Trade Date and Time 
:98A::SETT//20200820 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0,  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD24937500, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE/SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/INST Instruct Processing Indicator 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8KR1 [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8D23 [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/25000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828VS6 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  

---

## Page 344

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 344 
 
Sample B6.e MT515 Repo Dealer [[Member]] 8D23 Submits Repo Transaction to [[GSD]]* 
Message Content Comments 
:98A::REPU//20200821 Close Leg [[settlement]] Date 
:92A::REPO//1,75 Repo Rate 
:19A::REPA//USD24938712,24 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 345

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 345 
 
Sample B6.f MT509 Trade Accepted Record sent to Repo Dealer [[Member]] 8D23* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8D23 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900511 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200820101203 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//999100015 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::RELA//000053 Related Reference ([[Member]]'s SEME from MT515 Instruct Message) 
:16S:LINK   
:16R:LINK   
:20C::LIST//000C02-0820 [[GSD]] Assigned Reference Number (TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC//PACK Trade Input Accepted Status 
:16S:STAT   
:16S:GENL   
- End of Message 
* 
  

---

## Page 346

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 346 
 
Sample B6.g MT518 Comparison Request sent to Repo [[Broker]] [[Member]] 8KR1* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8KR1 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900515 Sender’s ([[GSD]]) Message Reference Number  
:23G:NEWM Instruct Record Indicator 
:98C::PREP//20200820101206 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200820100854 Trade Date and Time 
:98A::SETT//20200820 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD24937500, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CMPR Comparison Requested Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8KR1 [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8D23 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:20C::PROC//999100015 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/25000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828VS6 Identification of Financial Instrument ([[CUSIP]] Number) 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200821 Close Leg [[settlement]] Date 
:92A::REPO//1,75 Repo Rate 

---

## Page 347

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 347 
 
Sample B6.g MT518 Comparison Request sent to Repo [[Broker]] [[Member]] 8KR1* 
Message Content Comments 
:19A::REPA//USD24938712,24 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
  

---

## Page 348

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 348 
 
Sample B6.h MT509 Trade Compared Record sent to Repo [[Broker]] [[Member]] 8KR1* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8KR1 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900519 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200820101209 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//08219KR129 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000B14-0820 [[GSD]] Assigned Reference Number (TID) 
:16S:LINK   
:16R:LINK   
:20C::PROG//999100015 Contra-party External Reference Number 
:16S:LINK  
:16R:LINK  
:13B::LINK/GSCC/TRDR Demand Repo Trade Indicator 
:20C::BASK//BKRREF123 [[Broker]] Reference Number 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 349

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 349 
 
Sample B6.i MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8D23* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8D23 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900520 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200820101210 Date and Time of Message Preparation 
:22F::TRTR/GSCC/TRDR Demand Repo Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200820100854 Trade Date and Time 
:98A::SETT//20200820 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD24937500, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//SELL Sell (REPO) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8KR1 [[Buyer]] (Reverse Party) Information - Contra-party [[ID]] 
:20C::PROC//08219KR129 [[Buyer]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8D23 [[Seller]] (Repo Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:36B::CONF//FAMT/25000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828VS6 Identification of Financial Instrument ([[CUSIP]] Number) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 350

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 350 
 
Sample B6.i MT518 Comparison Request Cancel (due to match) sent to Repo Dealer [[Member]] 8D23* 
Message Content Comments 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200821 Close Leg [[settlement]] Date 
:92A::REPO//1,75 Repo Rate 
:19A::REPA//USD24938712,24 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 351

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 351 
 
Sample B6.j MT509 Trade Compared Record sent to Repo Dealer [[Member]] 8D23* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8D23 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900521 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200820101214 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//999100015 Receiving [[Member]]’s External Reference Number 
:16S:LINK   
:16R:LINK   
:20C::LIST//000C02-0820 [[GSD]] Assigned Reference Number (TID) 
:16S:LINK   
:16R:LINK   
:20C::PROG//08219KR129 Contra-party External Reference Number 
:16S:LINK   
:16R:LINK   
:13B::LINK/GSCC/REPO Repo Trade Indicator 
:20C::BASK//000B14-0820 [[Broker]] Reference Number ([[Broker]] C/P’s [[GSD]] Assigned Reference Number (TID) - 
only sent to Receiver on eligible Demand Same-Day Settling Trades) 
:16S:LINK   
:16R:STAT   
:25D::MTCH//MACH Trade Compared Status 
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 352

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 352 
 
Sample B6.k MT518 Comparison Request Cancel (due to match) sent to Repo [[Broker]] [[Member]] 8KR1* 
Message Content Comments 
  Password - Blank on MT518 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
518/000/GSCC Message Type 
8KR1 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900523 Sender’s ([[GSD]]) Message Reference Number  
:23G:CANC Cancel Record Indicator 
:98C::PREP//20200820101214 Date and Time of Message Preparation 
:22F::TRTR/GSCC/REPO Repo Trade Indicator 
:16R:LINK   
:20C::PREV//NONREF Previous Reference = NONREF for cancel messages 
:16S:LINK   
:16S:GENL   
:16R:CONFDET   
:98C::TRAD//20200820100854 Trade Date and Time 
:98A::SETT//20200820 [[settlement]] Date (or Start Leg [[settlement]] Date if REPO) 
:90A::DEAL//PRCT/0  PRCT = Rate Price Type, and ‘0,’ Price (for Repo Trade) 
:19A::SETT//USD24937500, [[settlement]] Amount (or Start Leg [[settlement]] Amount if REPO) 
:22H::BUSE//BUYI Buy (REVR) Trade Record 
:22F::PROC/GSCC/CADV Comparison Request Cancel Record 
:22H::PAYM//APMT Against Payment Indicator 
:16R:CONFPRTY   
:95R::BUYR/GSCC/PART8KR1 [[Buyer]] (Reverse Party) Information - [[Member]] [[ID]] 
:16S:CONFPRTY   
:16R:CONFPRTY   
:95R::SELL/GSCC/PART8D23 [[Seller]] (Repo Party) Information - Contra-party [[ID]] 
:20C::PROC//999100015 [[Seller]]’s (Contra) External Reference Number 
:16S:CONFPRTY   
:36B::CONF//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:35B:/US/912828VS6 Identification of Financial Instrument ([[CUSIP]] Number) 
:70E::TPRO//GSCC/MSGRMACH Trade Instruction Processing Narrative- Message Reason due to Match 

---

## Page 353

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 353 
 
Sample B6.k MT518 Comparison Request Cancel (due to match) sent to Repo [[Broker]] [[Member]] 8KR1* 
Message Content Comments 
:16S:CONFDET   
:16R:REPO  
:98A::REPU//20200821 Close Leg [[settlement]] Date 
:92A::REPO//1,75 Repo Rate 
:19A::REPA//USD24938712,24 Close Leg [[settlement]] Amount 
:16S:REPO  
- End of Message 
 
  

---

## Page 354

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 354 
 
Sample B6.l MT509 Trade Bound to Net sent to Repo [[Broker]] [[Member]] 8KR1* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8KR1 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900525 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200820101220 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//08219KR129 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//000B14-0820 [[GSD]] Assigned Reference Number (TID) 
:16S:LINK  
:16R:LINK  
:13B::LINK/GSCC/TRDR Demand Repo Trade Indicator 
:20C::BASK//BKRREF123 [[Broker]] Reference Number 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status  
:16S:STAT   
:16S:GENL   
- End of Message 
 
  

---

## Page 355

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 355 
 
Sample B6.m MT509 Trade Bound to Net sent to Repo Dealer [[Member]] 8D23* 
Message Content Comments 
  Password - Blank on MT509 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
509/000/GSCC Message Type 
8D23 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019900527 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200820101220 Date and Time of Message Preparation 
:16R:LINK   
:20C::MAST//999100015 Receiving [[Member]]’s External Reference Number  
:16S:LINK   
:16R:LINK   
:20C::LIST//000C02-0820 [[GSD]] Assigned Reference Number (TID) 
:16S:LINK  
:16R:LINK  
:13B::LINK/GSCC/REPO Repo Trade Indicator 
:20C::BASK//BKRREF123 [[Broker]] Reference Number 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/NBTD Trade Bound to Net Status  
:16S:STAT   
:16S:GENL   
- End of Message 
  

---

## Page 356

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 356 
 
Sample B6.n MT548 Cleared Obligation sent to Repo Dealer [[Member]] 8D23 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
8D23 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//000019901568 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200820111623 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//000322-0820 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//000322-0820 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//000B14-0820 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828VS6 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/25000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD24937500, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/8D23 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/CLRD Type of [[settlement]] Transaction (Cleared) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200820 [[settlement]] Date 

---

## Page 357

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 357 
 
Sample B6.n MT548 Cleared Obligation sent to Repo Dealer [[Member]] 8D23 
Message Content Comments 
:70E::SPRO/GSCC/OPARFAMT25000000, 
/OPSTUSD24937500, 
Opening Par Amount and Opening [[settlement]] Amount 
:16S:SETTRAN   
- End of Message 
 
  

---

## Page 358

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 358 
 
Sample # B7 – [[settlement]] Messages Resulting from an Intraday Partial [[settlement]] 
On June 25, 2020, [[GSD]] creates a Netted Obligation for Dealer [[Member]] 95C0 to deliver 50,000,000 of US 
Treasury Note 2.000% of 8/28/21 ([[CUSIP]] 912828B90) to [[GSD]] for [[settlement]] on June 26, 2020.  
On June 26, 2020, Dealer [[Member]] 95C0 contacts [[GSD]] Operations requesting an intraday partial [[settlement]]  
by splitting the above referenced Netted Obligation into two [[settlement]] [[obligations]]. Per [[GSD]] Operations 
procedures, [[GSD]] obtains agreement from the linked party of the Dealer [[Member]] 95C0’s Netted Obligation to 
partially settle the Netted [[obligations]] during the day. The Netted Obligation is partially settled on June 26, 2020 
as follows: 25,000,000 and 25,000,000.  
[[Member]] 8C82 Reference Numbers Netted Obligation Partial Settled Obligation Partial Settled Obligation 
Quantity  50,000,000 25,000,000  25,000,000 
[[settlement]] Amount  53,750,000.00 26,875,000.00  26,875,000.00 
Senders Reference   0000000798010132 0000000798011232  0000000798011342 
[[GSD]] Assigned Reference (TID)  N/A  N/A  N/A 
[[GSD]] Assigned Reference (OID) (POOL)  700767-0625  700835-0626  700836-0626 
[[GSD]] Assigned Reference (OID) (PREV)  700767-0625  700767-0625  700835-0626 
[[GSD]] Assigned Reference (OID) (RELA)  700767-0625  700767-0625  700767-0625 
 
The message samples presented on the following pages are all based on the above scenario. Please note that 
the messages displayed are depicting the [[settlement]] status of only one party.  
For the purposes of this example, we assume the following:  
1. Dealer [[Member]] who is bound (Obligation is linked to another [[Member]]) to the original Clearance 
Instruction has agreed to the partial [[settlement]]. 
2. Both parties agree to split the [[settlement]] [[obligations]] in to two parts. 
3. The last two cleared message samples depict the trade fully settled (b) & (c). 
 
B7.a MT548 Clearance Instruction sent to Dealer [[Member]] 95C0 
B7.b MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 
B7.c MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated.  
Note:  
Partial [[settlement]] of [[securities]] [[settlement]] [[obligations]] does not apply to [[obligations]] created to settle a Same-Day Settling 
Trade as such [[obligations]] will not be partial settled.   

---

## Page 359

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 359 
 
Sample B7.a MT548 Clearance Instruction sent to Dealer [[Member]] 95C0 (Netted Obligation) 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
95C0 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000000798010132 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200625205014 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700767-0625 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700767-0625 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700767-0625 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828B90 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/50000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD53750000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/95C0 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Next Day) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200626 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 360

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 360 
 
Sample B7.a MT548 Clearance Instruction sent to Dealer [[Member]] 95C0 (Netted Obligation) 
Message Content Comments 
:95R::REAG/GSCC/021000018BK OF 
NYC/GSCC 
Receiving Agent ([[Buyer]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
  

---

## Page 361

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 361 
 
Sample B7.b MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Partial [[settlement]] of Netted Obligation) 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
95C0 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000000798011232 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200626115343 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700835-0626 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700767-0625 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700767-0625 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828B90 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/25000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD26875000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/95C0 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/CLRD Type of [[settlement]] Transaction (Cleared) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200626 [[settlement]] Date 

---

## Page 362

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 362 
 
Sample B7.b MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Partial [[settlement]] of Netted Obligation) 
Message Content Comments 
:70E::SPRO//GSCC/RSTTFAMT25000000, 
/RSMTUSD26875000, 
/OPARFAMT50000000,/OPSTUSD53750000, 
Quantity of Financial Instrument Remaining, Remaining [[settlement]] 
Amount, Opening Par Amount and Opening [[settlement]] Amount 
:16S:SETTRAN   
- End of Message 
  

---

## Page 363

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 363 
 
Sample B7.c MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Partial [[settlement]] of Netted Obligation) 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
95C0 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000000798011342 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200626123534 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700836-0626 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700835-0626 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700767-0625 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/912828B90 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/25000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD26875000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/95C0 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/CLRD Type of [[settlement]] Transaction (Cleared) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200626 [[settlement]] Date 
:70E::SPRO//GSCC Opening Par Amount and Opening [[settlement]] Amount 

---

## Page 364

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 364 
 
Sample B7.c MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Partial [[settlement]] of Netted Obligation) 
Message Content Comments 
/OPARFAMT25000000,/OPSTUSD26875000, 
:16S:SETTRAN   
- End of Message 
  

---

## Page 365

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 365 
 
Sample # B8 – [[settlement]] and Funds [[settlement]] Messages Resulting from the Pair-Off of 
a Same-Day Settling Obligation and a Netted Obligation  
On [[settlement]] date July 20, 2020, Dealer [[Member]] 95C0 has a Netted Obligation to receive 30,000,000 of US 
Treasury Note 2.125% of 5/31/21 ([[CUSIP]] 9128286V7) from [[GSD]] as a result of netting output from the 
previous business day, July 17, 2020.The [[settlement]] amount of the Netted Obligation is $30,602,790.16.  
Also, on July 20, 2020, Dealer [[Member]] 95C0 has a Same-Day Settling Obligation to deliver 30,000,000 of US 
Treasury Note 2.125% of 5/31/21 ([[CUSIP]] 9128286V7) to [[GSD]] settle a Same-Day Settling Trade compared on 
July 20, 2020.  The [[settlement]] amount of the Same-Day Settling Obligation is $31,750,000.00.  
[[Member]] 95C0 Reference Numbers Netted Obligation Same-Day Obligation 
Quantity  30,000,000  30,000,000 
[[settlement]] Amount  30,602,790.16  31,750,000.00 
Senders Reference  0000000798011432  0000000798041832 
[[GSD]] Assigned Reference (TID)  N/A  005403-0720 
[[GSD]] Assigned Reference (OID)  700917-0717  003836-0720 
 
The message samples presented on the following pages are all based on the above scenario. Please note the 
[[settlement]] amount on the Netted Obligation is based on the system price. The Same-Day Settling Trade will 
settle trade-for-trade at contract value. Therefore, the [[settlement]] amount for the Same-Day Settling obligation 
is equal to the value of the underlying trade (the Start Leg [[settlement]] Amount).   
For the purposes of this example, we assume the following:  
1. Dealer [[Member]] 95C0 has opted into [[GSD]]’s Pair-Off Service 
2. Both the Netted Obligation and Same-Day Settling Obligation in the above referenced scenario are 
pending clearance at the time the systemic pair-off process commences on July 20, 2020.  
 
B8.a MT548 Clearance Instruction sent to Dealer [[Member]] 95C0 (Netted Obligation)  
B8.b MT548 Clearance Instruction sent to Dealer [[Member]] 95C0 (Same-Day Settling Obligation)  
B8.c MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Netted Obligation) 
B8.d MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Same-Day Settling Obligation)  
B8.e MT950 [[participant]] Net Summary sent to Dealer [[Member]] 95C0  
 
Note:  
These message samples are not intended to represent a “flow” of events; they are solely intended to demonstrate how 
various records might be populated.  

---

## Page 366

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 366 
 
Sample B8.a MT548 Clearance Instruction sent to Dealer [[Member]] 95C0 (Netted Obligation) 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
95C0 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000000798011432 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200717205143 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700917-0717 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700917-0717 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700917-0717 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/9128286V7 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/30000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD30602790,16 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/95C0 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Next Day) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200720 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 367

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 367 
 
Sample B8.a MT548 Clearance Instruction sent to Dealer [[Member]] 95C0 (Netted Obligation) 
Message Content Comments 
:95R::DEAG/GSCC/021000018BK OF 
NYC/GSCC 
Delivering Agent ([[Seller]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
  

---

## Page 368

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 368 
 
Sample B8.b MT548 Clearance Instruction sent to Dealer [[Member]] 95C0 (Same-Day Settling Obligation)  
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
95C0 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000000798041832 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200720100143 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//003836-0720 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//003836-0720 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//005403-0720 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::IPRC/GSCC/CITS Status (Instruction to be Sent to Clearing Bank) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/9128286V7 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/30000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD31175000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/95C0 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR/GSCC/NETX Clearance Type (Same Day) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200720 [[settlement]] Date 
:16R:SETPRTY   

---

## Page 369

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 369 
 
Sample B8.b MT548 Clearance Instruction sent to Dealer [[Member]] 95C0 (Same-Day Settling Obligation)  
Message Content Comments 
:95R::REAG/GSCC/021000018BK OF 
NYC/GSCC 
Receiving Agent ([[Buyer]]) – Clearing Bank ABA – Fed Address 
:16S:SETPRTY   
:16S:SETTRAN   
- End of Message 
 
  

---

## Page 370

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 370 
 
Sample B8.c MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Netted Obligation) 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
95C0 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000000798046520 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200720153343 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//700917-0717 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//700917-0717 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//700917-0717 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/9128286V7 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/30000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD30602790,16 [[settlement]] Amount 
:97B::SAFE/GSCC/PART/95C0 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR//PAIR Type of [[settlement]] Transaction (Paired-off) 
:22H::REDE//RECE Receive/Deliver Indicator (Receive) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200720 [[settlement]] Date 
:70E::SPRO//GSCC Opening Par Amount and Opening [[settlement]] Amount 

---

## Page 371

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 371 
 
Sample B8.c MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Netted Obligation) 
Message Content Comments 
/OPARFAMT30000000,/OPSTUSD30602790,16 
:16S:SETTRAN   
- End of Message 
 
 
 
 
  

---

## Page 372

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 372 
 
Sample B8.d MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Same-Day Settling Obligation) 
Message Content Comments 
  Password - Blank on MT548 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
548/000/GSCC Message Type 
95C0 Receiver [[ID]] ([[Member]] [[ID]]) 
:16R:GENL   
:20C::SEME//0000000798046472 Sender’s ([[GSD]]) Message Reference Number  
:23G:INST Message Function (for Instruction) 
:98C::PREP//20200720153343 Date and Time of Message Preparation 
:16R:LINK   
:20C::POOL//003836-0720 [[GSD]] Assigned Reference Number (OID) 
:16S:LINK   
:16R:LINK   
:20C::PREV//003836-0720 Previous Reference Number (Previous OID) 
:16S:LINK   
:16R:LINK   
:20C::RELA//005403-0720 [[GSD]] Assigned Reference Number (Receiver’s TID or [[Broker]] C/P TID) 
:16S:LINK   
:16R:STAT   
:25D::SETT/GSCC/CLOB Status (Cleared Obligation Record) 
:16S:STAT   
:16S:GENL   
:16R:SETTRAN   
:35B:/US/9128286V7 Identification of Financial Instrument ([[CUSIP]] Number) 
:36B::SETT//FAMT/30000000, Quantity of Security (FAMT = Face Amount) 
:19A::SETT//USD31175000, [[settlement]] Amount 
:97B::SAFE/GSCC/PART/95C0 Safekeeping Account ([[Member]] [[ID]]) 
:22F::SETR//PAIR Type of [[settlement]] Transaction (Paired-off) 
:22H::REDE//DELI Receive/Deliver Indicator (Deliver) 
:22H::PAYM//APMT Against Payment Indicator 
:98A::SETT//20200720 [[settlement]] Date 
:70E::SPRO//GSCC Opening Par Amount and Opening [[settlement]] Amount 

---

## Page 373

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 373 
 
Sample B8.d MT548 Cleared Obligation sent to Dealer [[Member]] 95C0 (Same-Day Settling Obligation) 
Message Content Comments 
/OPARFAMT30000000,/OPSTUSD31750000,00 
:16S:SETTRAN   
- End of Message 
 
 
 
 
 
  

---

## Page 374

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 374 
 
Sample B8.e MT950 [[participant]] Net Summary sent to Dealer [[Member]] 95C0 
Message Content Comments 
  Password - Blank on MT950 
GSCCTRRS Sender [[ID]] ([[GSD]] Trade Registration and Reconciliation System) 
950/000/GSCC Message Type 
95C0 Receiver [[ID]] ([[Member]] [[ID]]) 
:20:PI019560G  Transaction Reference Number 
:25:9560 Account Identification ([[Member]] [[ID]]) 
:28C:10001 Statement Number 
:60F:C200720USD27825218,79 Opening Balance  
:61:200720D27825218,79FCPDNONREF//10001001 Statement Line – Collected/Paid  
:61:200720D271200774,12FFMANONREF//10001002 Statement Line – Forward Mark Allocation  
:61:200720C270972695,03FFMRNONREF//10001003 Statement Line – Forward Mark Allocation Return  
:61:200720C1147209,84FMADNONREF//10001004 
PAIR-OFF  ADJUSTMENT  2020-07-20 
Statement Line – Miscellaneous Adjustments / Miscellaneous   
Reason 
:62F:C200720USD1825837,38 Closing Balance 
- End of Message 
 
 
 
 
 
 
   

---

## Page 375

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 375 
 
Appendix C – Message Timing Matrix 
This appendix contains two views of the timing of when Members should expect to receive netting related messages from [[GSD]]. This appendix, using 
either view, places a timing perspective to the messages detailed in the flows in Appendix A. 
• View 1 provides a quick reference, depicting, by message type, when a specific record type is sent to the [[Member]]. 
• View 2 also denotes the timing the message is sent to the [[Member]]. It distinguishes, however, between trade related and obligation related record 
types. The trade related view further distinguishes between those messages sent for Buy / Sell (Cash) Transactions vs. Repo Transactions; 
records sent for obligation related events [[DO]] not make the distinction. 
Message Timing 
Message 
Type 
Record 
Type / Event 
Upon 
Match 
Start Leg 
[[settlement]] 
Date - 1 
After Match 
through Close Leg 
[[settlement]] Date - 2 
or 
Settle Date - 2 
Repo Close Leg 
[[settlement]] Date - 1 
or 
[[settlement]] Date - 1 
Maturity Date - 1 
or 
Coupon Payment 
Date - 1 
[[settlement]] 
Date 
Action Date 
View 1 – Trade and Obligation Related Messages  
MT509 Trade Bound to Net*                                                  X       
 Trade Comparison 
Only*           
X       
 Buy/Sell Transaction in 
Net 
   X    
 Repo Start Leg in Net                         X      
 Repo Close Leg in Net     X    
 Forward Trade Pended 
/ No Longer in Net-
Repo [[collateral]] 
Matured-No New 
[[collateral]] Assigned 
    X   
 Forward Trade Pended 
/ No Longer in Net-No 
 X      

---

## Page 376

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 376 
 
Message Timing 
Message 
Type 
Record 
Type / Event 
Upon 
Match 
Start Leg 
[[settlement]] 
Date - 1 
After Match 
through Close Leg 
[[settlement]] Date - 2 
or 
Settle Date - 2 
Repo Close Leg 
[[settlement]] Date - 1 
or 
[[settlement]] Date - 1 
Maturity Date - 1 
or 
Coupon Payment 
Date - 1 
[[settlement]] 
Date 
Action Date 
[[collateral]] Assigned to 
GC Trade  
 Forward Trade Pended 
/ No Longer in Net-
Trade Cancelled  
      X 
 Forward Trade Pended 
/ No Longer in Net-
[[GSD]] Excluded the 
Trade 
      X 
MT548 – 
Clearance 
Instruction 
Next Day (Same-Day 
or Next Day) 
X X  X  X  
 Failed Obligation      X  
 Held Fail      X  
 [[Broker]] Fail      X  
 Repo Substitution       X 
 Cancel Record (All)       X 
MT548 – 
Cleared 
Obligation 
Paired Off      X  
 Bought In      X  
 Held Fail Matured     X   
 Matured     X   

---

## Page 377

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 377 
 
Message Timing 
Message 
Type 
Record 
Type / Event 
Upon 
Match 
Start Leg 
[[settlement]] 
Date - 1 
After Match 
through Close Leg 
[[settlement]] Date - 2 
or 
Settle Date - 2 
Repo Close Leg 
[[settlement]] Date - 1 
or 
[[settlement]] Date - 1 
Maturity Date - 1 
or 
Coupon Payment 
Date - 1 
[[settlement]] 
Date 
Action Date 
 Cleared      X  
 Netted      X  
MT590 Repo Coupon Payment     X   
 Fail Coupon Payment     X   
 Repo Maturity Payment     X   
 Fail Maturity Payment     X   
 Per Trade Forward 
[[Margin]] 
  X     
* These messages are intended to be a one-time event. However, if the netting status of a trade changes prior to the trade being included in the net, multiple messages 
may be sent. 
  

---

## Page 378

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 378 
 
Message Timing 
Message 
Type 
Record Category Record 
Type / Event 
Message Timing – Buy / Sell (Cash)  Message Timing – Repo  
View 2 – Trade Related Messages 
MT509 Netting Status 
Messages 
Trade Bound to Net*                                                  Upon Match Upon Match 
  Trade Comparison Only*           Upon Match Upon Match 
  Buy/Sell Transaction in Net Night of [[settlement]] - 1  N/A 
  Repo Start Leg in Net                        N/A Night of Start Leg [[settlement]] Date - 1  
  Repo Close Leg in Net  N/A Night of Close Leg [[settlement]] Date - 1  
  Forward Trade Pended / No 
Longer in Net-Repo [[collateral]] 
Matured-No New [[collateral]] 
Assigned 
N/A Night of [[collateral]] Maturity Date - 1 (From 
Match Date + 1) 
  Forward Trade Pended / No 
Longer in Net-No [[collateral]] 
Assigned to GC Trade  
N/A Night of Start Leg [[settlement]] Date - 1 (From 
Match Date + 1) 
  Forward Trade Pended / No 
Longer in Net-Trade Cancelled  
Upon Post Match Cancellation (From Match Date 
+ 1) 
Upon Post Match Cancellation (From Match 
Date + 1) 
  Forward Trade Pended / No 
Longer in Net-[[GSD]] Excluded 
the Trade 
Upon being Excluded (From Match Date + 1 
through Night of [[settlement]] Date - 1) 
Upon being Excluded (From Match Date + 1 
through Night of Close Leg [[settlement]] Date - 
1) 
MT590 Per Trade Debit / 
Credit Advice 
Repo Coupon Payment N/A Night of Coupon Payment Date - 1  
  Repo Maturity Payment N/A Night of [[collateral]] Maturity Date - 1 
  Per Trade Forward [[Margin]] Nightly from Match Date through Night of 
[[settlement]] Date - 2 
(Or until the night trade is Cancelled or Excluded 
from Net) 
Nightly from Match Date through Night of Close 
Leg [[settlement]] Date - 2 
(Or until the night trade is Cancelled or 
Excluded from Net) 

---

## Page 379

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 379 
 
Message Timing 
Message 
Type 
Record Category Record 
Type / Event 
Message Timing – Buy / Sell (Cash)  Message Timing – Repo  
*These messages are intended to be a one-time event. However, if the netting status of a trade changes prior to the trade being included in the net, multiple messages 
may be sent. 
  

---

## Page 380

[[GSD]] Interactive Messaging (IM) [[Member]] Specifications for Netting Output 
Appendices 380 
 
Message Timing 
Message 
Type 
Record Category Record 
Type / Reason 
Message Timing – [[obligations]] 
View 2 – Obligation Related Messages 
MT548  Clearance 
Instruction 
Next Day (Same-Day or Next 
Day) 
Night of [[settlement]] Date - 1 (or [[settlement]] Date for Same-Day Settlements) 
  Failed Obligation Night of [[settlement]] Date 
  Held Fail Night of [[settlement]] Date 
  [[Broker]] Fail [[settlement]] Date 
  Repo Substitution Substitution Date 
MT548 Clearance 
Instruction Cancel 
Next Day (Same-Day or Next 
Day) 
Cancellation Date 
  Failed Obligation Cancellation Date 
  Held Fail Cancellation Date 
  [[Broker]] Fail Cancellation Date 
  Repo Substitution Cancellation Date 
MT548  Cleared Obligation Paired Off [[settlement]] Date or Substitution Date 
  Bought In [[settlement]] Date 
  Held Fail Matured Night of [[collateral]] Maturity Date - 1  
  Matured Night of [[collateral]] Maturity Date - 1  
  Cleared [[settlement]] Date 
  Netted Night of [[settlement]] Date of the Failed Obligation 
MT590  Fail Coupon Payment Night of Coupon Payment Date - 1  
  Fail Maturity Payment Night of [[collateral]] Maturity Date - 1  
  

---

## Page 381

 
  
 
FOR MORE INFORMATION 
 
Email [[DTCC]] Learning at: 
CoreLearning@[[DTCC]].com 
or visit us on the web at: 
www.dtcclearning.com 